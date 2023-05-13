# Comparing `tmp/hahomematic-2023.5.0.tar.gz` & `tmp/hahomematic-2023.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hahomematic-2023.5.0.tar", last modified: Wed May  3 05:22:29 2023, max compression
+gzip compressed data, was "hahomematic-2023.5.1.tar", last modified: Sat May 13 11:35:13 2023, max compression
```

## Comparing `hahomematic-2023.5.0.tar` & `hahomematic-2023.5.1.tar`

### file list

```diff
@@ -1,78 +1,79 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.052802 hahomematic-2023.5.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-05-03 05:22:29.052802 hahomematic-2023.5.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1982 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.044802 hahomematic-2023.5.0/hahomematic/
--rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/backport.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.044802 hahomematic-2023.5.0/hahomematic/caches/
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/caches/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7789 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/caches/dynamic.py
--rw-r--r--   0 runner    (1001) docker     (123)    17167 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/caches/persistent.py
--rw-r--r--   0 runner    (1001) docker     (123)    24401 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/caches/visibility.py
--rw-r--r--   0 runner    (1001) docker     (123)    49209 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/central_unit.py
--rw-r--r--   0 runner    (1001) docker     (123)    44779 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/client.py
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    12849 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/const.py
--rw-r--r--   0 runner    (1001) docker     (123)     4888 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)     1481 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/exporter.py
--rw-r--r--   0 runner    (1001) docker     (123)     4469 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/hmcli.py
--rw-r--r--   0 runner    (1001) docker     (123)    28383 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/json_rpc_client.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.048802 hahomematic-2023.5.0/hahomematic/platforms/
--rw-r--r--   0 runner    (1001) docker     (123)     4308 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.048802 hahomematic-2023.5.0/hahomematic/platforms/custom/
--rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    24881 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/climate.py
--rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/const.py
--rw-r--r--   0 runner    (1001) docker     (123)    23747 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/cover.py
--rw-r--r--   0 runner    (1001) docker     (123)    27916 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/definition.py
--rw-r--r--   0 runner    (1001) docker     (123)    11421 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/entity.py
--rw-r--r--   0 runner    (1001) docker     (123)    33824 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/light.py
--rw-r--r--   0 runner    (1001) docker     (123)     8117 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/lock.py
--rw-r--r--   0 runner    (1001) docker     (123)    10021 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/siren.py
--rw-r--r--   0 runner    (1001) docker     (123)     1129 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/support.py
--rw-r--r--   0 runner    (1001) docker     (123)     5683 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/custom/switch.py
--rw-r--r--   0 runner    (1001) docker     (123)    19415 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/device.py
--rw-r--r--   0 runner    (1001) docker     (123)    19910 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/entity.py
--rw-r--r--   0 runner    (1001) docker     (123)     4876 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/event.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.048802 hahomematic-2023.5.0/hahomematic/platforms/generic/
--rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      943 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/action.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/binary_sensor.py
--rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/button.py
--rw-r--r--   0 runner    (1001) docker     (123)     7447 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/entity.py
--rw-r--r--   0 runner    (1001) docker     (123)     2232 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/number.py
--rw-r--r--   0 runner    (1001) docker     (123)     1454 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/select.py
--rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/sensor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1714 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/switch.py
--rw-r--r--   0 runner    (1001) docker     (123)      452 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/generic/text.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.048802 hahomematic-2023.5.0/hahomematic/platforms/hub/
--rw-r--r--   0 runner    (1001) docker     (123)     8985 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      705 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/binary_sensor.py
--rw-r--r--   0 runner    (1001) docker     (123)     2152 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/button.py
--rw-r--r--   0 runner    (1001) docker     (123)     4545 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/entity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/number.py
--rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/select.py
--rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/sensor.py
--rw-r--r--   0 runner    (1001) docker     (123)      444 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/switch.py
--rw-r--r--   0 runner    (1001) docker     (123)      583 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/hub/text.py
--rw-r--r--   0 runner    (1001) docker     (123)    15070 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/platforms/support.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.052802 hahomematic-2023.5.0/hahomematic/rega_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)     2339 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/rega_scripts/fetch_all_device_data.fn
--rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/rega_scripts/get_serial.fn
--rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/rega_scripts/get_system_variables_ext_marker.fn
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/rega_scripts/set_system_variable.fn
--rw-r--r--   0 runner    (1001) docker     (123)     6902 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/support.py
--rw-r--r--   0 runner    (1001) docker     (123)     4881 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/xml_rpc_proxy.py
--rw-r--r--   0 runner    (1001) docker     (123)     8867 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/hahomematic/xml_rpc_server.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 05:22:29.044802 hahomematic-2023.5.0/hahomematic.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-05-03 05:22:28.000000 hahomematic-2023.5.0/hahomematic.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2277 2023-05-03 05:22:29.000000 hahomematic-2023.5.0/hahomematic.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-03 05:22:28.000000 hahomematic-2023.5.0/hahomematic.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-03 05:22:27.000000 hahomematic-2023.5.0/hahomematic.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-03 05:22:28.000000 hahomematic-2023.5.0/hahomematic.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-03 05:22:28.000000 hahomematic-2023.5.0/hahomematic.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     7508 2023-05-03 05:21:52.000000 hahomematic-2023.5.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-03 05:22:29.052802 hahomematic-2023.5.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.251598 hahomematic-2023.5.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-05-13 11:35:13.251598 hahomematic-2023.5.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1982 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.235598 hahomematic-2023.5.1/hahomematic/
+-rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/backport.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.239598 hahomematic-2023.5.1/hahomematic/caches/
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/caches/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7789 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/caches/dynamic.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16907 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/caches/persistent.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24401 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/caches/visibility.py
+-rw-r--r--   0 runner    (1001) docker     (123)    50182 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/central_unit.py
+-rw-r--r--   0 runner    (1001) docker     (123)    45773 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14403 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4888 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1481 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/exporter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4469 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/hmcli.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28383 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/json_rpc_client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.239598 hahomematic-2023.5.1/hahomematic/platforms/
+-rw-r--r--   0 runner    (1001) docker     (123)     4307 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.243598 hahomematic-2023.5.1/hahomematic/platforms/custom/
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24881 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/climate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23747 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/cover.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27916 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/definition.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11421 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33824 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/light.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8117 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/lock.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10021 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/siren.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1129 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/support.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5683 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/custom/switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24351 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/device.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19910 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4876 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/event.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.247598 hahomematic-2023.5.1/hahomematic/platforms/generic/
+-rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      943 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/action.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/binary_sensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/button.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7447 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2232 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/number.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1454 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/select.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/sensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1714 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)      452 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/generic/text.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.251598 hahomematic-2023.5.1/hahomematic/platforms/hub/
+-rw-r--r--   0 runner    (1001) docker     (123)     8985 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      705 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/binary_sensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2152 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/button.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4545 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/number.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/select.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/sensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)      444 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)      583 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/hub/text.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15070 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/support.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2594 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/platforms/update.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.251598 hahomematic-2023.5.1/hahomematic/rega_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)     2339 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/rega_scripts/fetch_all_device_data.fn
+-rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/rega_scripts/get_serial.fn
+-rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/rega_scripts/get_system_variables_ext_marker.fn
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/rega_scripts/set_system_variable.fn
+-rw-r--r--   0 runner    (1001) docker     (123)     6902 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/support.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4881 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/xml_rpc_proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8867 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/hahomematic/xml_rpc_server.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:35:13.239598 hahomematic-2023.5.1/hahomematic.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-05-13 11:35:12.000000 hahomematic-2023.5.1/hahomematic.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2309 2023-05-13 11:35:13.000000 hahomematic-2023.5.1/hahomematic.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:35:12.000000 hahomematic-2023.5.1/hahomematic.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:35:10.000000 hahomematic-2023.5.1/hahomematic.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-13 11:35:12.000000 hahomematic-2023.5.1/hahomematic.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 11:35:13.000000 hahomematic-2023.5.1/hahomematic.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     7508 2023-05-13 11:34:37.000000 hahomematic-2023.5.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-13 11:35:13.251598 hahomematic-2023.5.1/setup.cfg
```

### Comparing `hahomematic-2023.5.0/LICENSE` & `hahomematic-2023.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/PKG-INFO` & `hahomematic-2023.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hahomematic
-Version: 2023.5.0
+Version: 2023.5.1
 Summary: Homematic interface for Home Assistant running on Python 3.
 Home-page: https://github.com/danielperna84/hahomematic
 Author-email: Daniel Perna <danielperna84@gmail.com>, SukramJ <sukramj@icloud.com>
 License: MIT License
 Project-URL: Source Code, https://github.com/danielperna84/hahomematic
 Project-URL: Bug Reports, https://github.com/danielperna84/hahomematic/issues
 Project-URL: Docs: Dev, https://github.com/danielperna84/hahomematic
```

### Comparing `hahomematic-2023.5.0/README.md` & `hahomematic-2023.5.1/README.md`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/__init__.py` & `hahomematic-2023.5.1/hahomematic/__init__.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/backport.py` & `hahomematic-2023.5.1/hahomematic/backport.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/caches/dynamic.py` & `hahomematic-2023.5.1/hahomematic/caches/dynamic.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/caches/persistent.py` & `hahomematic-2023.5.1/hahomematic/caches/persistent.py`

 * *Files 2% similar despite different names*

```diff
@@ -116,68 +116,57 @@
             persistant_cache=self._raw_device_descriptions,
         )
         # {interface_id, {device_address, [channel_address]}}
         self._addresses: Final[dict[str, dict[str, list[str]]]] = {}
         # {interface_id, {address, device_descriptions}}
         self._device_descriptions: Final[dict[str, dict[str, dict[str, Any]]]] = {}
 
-    def _add_device_descriptions(
-        self, interface_id: str, device_descriptions: list[dict[str, Any]]
-    ) -> None:
-        """Add device_descriptions to cache."""
-        if interface_id not in self._raw_device_descriptions:
-            self._raw_device_descriptions[interface_id] = []
-        self._raw_device_descriptions[interface_id] = device_descriptions
-
-        self._convert_device_descriptions(
-            interface_id=interface_id, device_descriptions=device_descriptions
-        )
-
     def add_device_description(
         self, interface_id: str, device_description: dict[str, Any]
     ) -> None:
         """Add device_description to cache."""
         if interface_id not in self._raw_device_descriptions:
             self._raw_device_descriptions[interface_id] = []
 
-        if device_description not in self._raw_device_descriptions[interface_id]:
-            self._raw_device_descriptions[interface_id].append(device_description)
+        self._remove_device(
+            interface_id=interface_id, deleted_addresses=[device_description[HM_ADDRESS]]
+        )
+        self._raw_device_descriptions[interface_id].append(device_description)
 
         self._convert_device_description(
             interface_id=interface_id, device_description=device_description
         )
 
     def get_raw_device_descriptions(self, interface_id: str) -> list[dict[str, Any]]:
         """Find raw device in cache."""
         return self._raw_device_descriptions.get(interface_id, [])
 
     async def remove_device(self, device: HmDevice) -> None:
         """Remove device from cache."""
         deleted_addresses: list[str] = [device.device_address]
         deleted_addresses.extend(device.channels)
-        self._add_device_descriptions(
-            interface_id=device.interface_id,
-            device_descriptions=[
-                raw_device
-                for raw_device in self.get_raw_device_descriptions(device.interface_id)
-                if raw_device[HM_ADDRESS] not in deleted_addresses
-            ],
-        )
+        self._remove_device(interface_id=device.interface_id, deleted_addresses=deleted_addresses)
+        await self.save()
+
+    def _remove_device(self, interface_id: str, deleted_addresses: list[str]) -> None:
+        """Remove device from cache."""
+        self._raw_device_descriptions[interface_id] = [
+            raw_device
+            for raw_device in self.get_raw_device_descriptions(interface_id)
+            if raw_device[HM_ADDRESS] not in deleted_addresses
+        ]
 
         for address in deleted_addresses:
             try:
-                if ":" not in address and self._addresses.get(device.interface_id, {}).get(
-                    address, []
-                ):
-                    del self._addresses[device.interface_id][address]
-                if self._device_descriptions.get(device.interface_id, {}).get(address, {}):
-                    del self._device_descriptions[device.interface_id][address]
+                if ":" not in address and self._addresses.get(interface_id, {}).get(address, []):
+                    del self._addresses[interface_id][address]
+                if self._device_descriptions.get(interface_id, {}).get(address, {}):
+                    del self._device_descriptions[interface_id][address]
             except KeyError:
                 _LOGGER.warning("REMOVE_DEVICE failed: Unable to delete: %s", address)
-        await self.save()
 
     def get_addresses(self, interface_id: str) -> dict[str, list[str]]:
         """Return the addresses by interface."""
         return self._addresses.get(interface_id, {})
 
     def get_channels(self, interface_id: str, device_address: str) -> dict[str, Channel]:
         """Return the device channels by interface and device_address."""
@@ -238,18 +227,21 @@
         if interface_id not in self._addresses:
             self._addresses[interface_id] = {}
         if interface_id not in self._device_descriptions:
             self._device_descriptions[interface_id] = {}
 
         address = device_description[HM_ADDRESS]
         self._device_descriptions[interface_id][address] = device_description
+
         if ":" not in address and address not in self._addresses[interface_id]:
             self._addresses[interface_id][address] = []
         if ":" in address:
             device_address = get_device_address(address)
+            if device_address not in self._addresses[interface_id]:
+                self._addresses[interface_id][device_address] = []
             self._addresses[interface_id][device_address].append(address)
 
     async def load(self) -> HmDataOperationResult:
         """Load device data from disk into _device_description_cache."""
         if not self._central.config.use_caches:
             _LOGGER.debug("load: not caching paramset descriptions for %s", self._central.name)
             return HmDataOperationResult.NO_LOAD
```

### Comparing `hahomematic-2023.5.0/hahomematic/caches/visibility.py` & `hahomematic-2023.5.1/hahomematic/caches/visibility.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/central_unit.py` & `hahomematic-2023.5.1/hahomematic/central_unit.py`

 * *Files 2% similar despite different names*

```diff
@@ -61,14 +61,15 @@
 from hahomematic.platforms.device import HmDevice
 from hahomematic.platforms.entity import BaseEntity
 from hahomematic.platforms.event import GenericEvent
 from hahomematic.platforms.generic.entity import GenericEntity
 from hahomematic.platforms.hub import HmHub
 from hahomematic.platforms.hub.button import HmProgramButton
 from hahomematic.platforms.hub.entity import GenericHubEntity, GenericSystemVariable
+from hahomematic.platforms.update import HmUpdate
 from hahomematic.support import (
     check_or_create_directory,
     check_password,
     get_device_address,
 )
 from hahomematic.xml_rpc_proxy import XmlRpcProxy
 
@@ -122,14 +123,16 @@
 
         # {interface_id, client}
         self._clients: Final[dict[str, hmcl.Client]] = {}
         # {{channel_address, parameter}, event_handle}
         self._entity_event_subscriptions: Final[dict[tuple[str, str], Any]] = {}
         # {unique_identifier, entity}
         self._entities: Final[dict[str, BaseEntity]] = {}
+        # {unique_identifier, update_entity}
+        self._firmware_update_entities: Final[dict[str, HmUpdate]] = {}
         # {device_address, device}
         self._devices: Final[dict[str, HmDevice]] = {}
         # {sysvar_name, sysvar_entity}
         self.sysvar_entities: Final[dict[str, GenericSystemVariable]] = {}
         # {sysvar_name, program_button}U
         self.program_entities: Final[dict[str, HmProgramButton]] = {}
         # store last event received datetime by interface
@@ -224,30 +227,22 @@
         await self._start_clients()
         if self.config.enable_server:
             self._start_connection_checker()
         else:
             local_interface_id = f"{self.name}-{LOCAL_INTERFACE}"
             if self.has_client(interface_id=local_interface_id):
                 client = self.get_client(interface_id=local_interface_id)
-                if device_descriptions := await client.get_all_device_descriptions():
-                    await self._add_new_devices(
-                        interface_id=client.interface_id,
-                        device_descriptions=device_descriptions,
-                    )
+                await self._refresh_device_descriptions(client=client)
 
     async def start_direct(self) -> None:
         """Start the central unit for temporary usage. #CC."""
         await self.parameter_visibility.load()
         await self._create_clients()
         for client in self._clients.values():
-            if device_descriptions := await client.get_all_device_descriptions():
-                await self._add_new_devices(
-                    interface_id=client.interface_id,
-                    device_descriptions=device_descriptions,
-                )
+            await self._refresh_device_descriptions(client=client)
 
     async def stop(self) -> None:
         """Stop processing of the central unit. #CC."""
         self._stop_connection_checker()
         await self._stop_clients()
         if self.json_rpc_client.is_activated:
             await self.json_rpc_client.logout()
@@ -273,14 +268,43 @@
             await asyncio.sleep(1)
 
     async def restart_clients(self) -> None:
         """Restart clients."""
         await self._stop_clients()
         await self._start_clients()
 
+    async def refresh_firmware_data(self, device_address: str | None = None) -> None:
+        """Refresh device firmware data."""
+        if device_address and (device := self.get_device(device_address=device_address)):
+            await self._refresh_device_descriptions(
+                client=device.client, device_address=device_address
+            )
+            device.refresh_firmware_data()
+        else:
+            for client in self._clients.values():
+                await self._refresh_device_descriptions(client=client)
+            for device in self._devices.values():
+                device.refresh_firmware_data()
+
+    async def _refresh_device_descriptions(
+        self, client: hmcl.Client, device_address: str | None = None
+    ) -> None:
+        """Refresh device descriptions."""
+        if (
+            device_descriptions := await client.get_device_descriptions(
+                device_address=device_address
+            )
+            if device_address
+            else await client.get_all_device_descriptions()
+        ):
+            await self._add_new_devices(
+                interface_id=client.interface_id,
+                device_descriptions=device_descriptions,
+            )
+
     async def _start_clients(self) -> None:
         """Start clients ."""
         if await self._create_clients():
             await self._load_caches()
             await self._create_devices()
             await self._init_hub()
             await self._init_clients()
@@ -675,16 +699,16 @@
             known_addresses = [
                 dev_desc[HM_ADDRESS]
                 for dev_desc in self.device_descriptions.get_raw_device_descriptions(interface_id)
             ]
             client = self._clients[interface_id]
             for dev_desc in device_descriptions:
                 try:
+                    self.device_descriptions.add_device_description(interface_id, dev_desc)
                     if dev_desc[HM_ADDRESS] not in known_addresses:
-                        self.device_descriptions.add_device_description(interface_id, dev_desc)
                         await client.fetch_paramset_descriptions(dev_desc)
                 except Exception as err:  # pragma: no cover
                     _LOGGER.error("ADD_NEW_DEVICES failed: %s [%s]", type(err).__name__, err.args)
 
             await self.device_descriptions.save()
             await self.paramset_descriptions.save()
             await self.device_details.load()
```

### Comparing `hahomematic-2023.5.0/hahomematic/client.py` & `hahomematic-2023.5.1/hahomematic/client.py`

 * *Files 1% similar despite different names*

```diff
@@ -41,15 +41,17 @@
     PROXY_DE_INIT_FAILED,
     PROXY_DE_INIT_SKIPPED,
     PROXY_DE_INIT_SUCCESS,
     PROXY_INIT_FAILED,
     PROXY_INIT_SUCCESS,
     HmCallSource,
     HmForcedDeviceAvailability,
+    HmInterface,
     HmInterfaceEventType,
+    HmProductGroup,
 )
 from hahomematic.exceptions import AuthFailure, BaseHomematicException, NoConnection
 from hahomematic.platforms.device import HmDevice
 from hahomematic.support import (
     ProgramData,
     SystemVariableData,
     build_headers,
@@ -301,14 +303,23 @@
         """Get device descriptions from CCU / Homegear."""
         try:
             return await self._proxy.listDevices()
         except BaseHomematicException as hhe:
             _LOGGER.warning("GET_ALL_DEVICE_DESCRIPTIONS failed: %s [%s]", hhe.name, hhe.args)
         return None
 
+    async def get_device_descriptions(self, device_address: str) -> Any:
+        """Get device descriptions from CCU / Homegear."""
+        try:
+            if device_descriptions := await self._proxy_read.getDeviceDescription(device_address):
+                return [device_descriptions]
+        except BaseHomematicException as hhe:
+            _LOGGER.warning("GET_DEVICE_DESCRIPTIONS failed: %s [%s]", hhe.name, hhe.args)
+        return None
+
     # pylint: disable=invalid-name
     async def set_install_mode(
         self,
         on: bool = True,
         t: int = 60,
         mode: int = 1,
         device_address: str | None = None,
@@ -572,14 +583,25 @@
             all_paramsets.update(
                 await self.get_paramset_descriptions(
                     device_description=device_description, only_relevant=False
                 )
             )
         return all_paramsets
 
+    async def update_device_firmware(self, device_address: str) -> bool:
+        """Update the firmware of a homematic device."""
+        if device := self.central.get_device(device_address=device_address):
+            return bool(
+                await self._proxy.installFirmware(device_address)
+                if device.product_group in (HmProductGroup.HMIPW, HmProductGroup.HMIP)
+                else await self._proxy.updateFirmware(device_address)
+            )
+
+        return False
+
     async def update_paramset_descriptions(self, device_address: str) -> None:
         """Update paramsets descriptions for provided device_address."""
         if not self.central.device_descriptions.get_device_descriptions(
             interface_id=self.interface_id
         ):
             _LOGGER.warning(
                 "UPDATE_PARAMSET_DESCRIPTIONS failed: "
@@ -1147,21 +1169,21 @@
 
 class InterfaceConfig:
     """interface config for a Client."""
 
     def __init__(
         self,
         central_name: str,
-        interface: str,
+        interface: HmInterface,
         port: int,
         remote_path: str | None = None,
         local_resources: LocalRessources | None = None,
     ) -> None:
         """Init the interface config."""
-        self.interface: Final[str] = LOCAL_INTERFACE if local_resources else interface
+        self.interface: Final[HmInterface] = HmInterface.LOCAL if local_resources else interface
         self.interface_id: Final[str] = f"{central_name}-{self.interface}"
         self.port: Final = port
         self.remote_path: Final = remote_path
         self.local_resources: Final = local_resources
         self.validate()
 
     def validate(self) -> None:
```

### Comparing `hahomematic-2023.5.0/hahomematic/const.py` & `hahomematic-2023.5.1/hahomematic/const.py`

 * *Files 10% similar despite different names*

```diff
@@ -98,17 +98,20 @@
 
 HM_ARG_ON_TIME: Final = "on_time"
 HM_ARG_VALUE: Final = "value"
 HM_ARG_ON: Final = "on"
 HM_ARG_OFF: Final = "off"
 
 HM_ADDRESS: Final = "ADDRESS"
+HM_AVAILABLE_FIRMWARE: Final = "AVAILABLE_FIRMWARE"
 HM_CHILDREN: Final = "CHILDREN"
 HM_DEFAULT: Final = "DEFAULT"
 HM_FIRMWARE: Final = "FIRMWARE"
+HM_FIRMWARE_UPDATABLE: Final = "UPDATABLE"
+HM_FIRMWARE_UPDATE_STATE: Final = "FIRMWARE_UPDATE_STATE"
 HM_FLAGS: Final = "FLAGS"
 HM_MAX: Final = "MAX"
 HM_MIN: Final = "MIN"
 HM_NAME: Final = "NAME"
 HM_OPERATIONS: Final = "OPERATIONS"
 HM_PARAMSETS: Final = "PARAMSETS"
 HM_PARENT: Final = "PARENT"
@@ -309,14 +312,21 @@
 # dict with binary_sensor relevant value lists and the corresponding TRUE value
 BINARY_SENSOR_TRUE_VALUE_DICT_FOR_VALUE_LIST: Final[dict[tuple[str, ...], str]] = {
     ("CLOSED", "OPEN"): "OPEN",
     ("DRY", "RAIN"): "RAIN",
     ("STABLE", "NOT_STABLE"): "NOT_STABLE",
 }
 
+PG_BIDCOS_RF: Final = "BidCos-RF"
+PG_BIDCOS_WIRED: Final = "BidCos-Wired"
+PG_HMIP_RF: Final = "HmIP-RF"
+PG_HMIP_WIRED: Final = "HmIP-Wired"
+PG_UNKNOWN: Final = "unknown"
+PG_VIRTUAL_DEVICES: Final = "VirtualDevices"
+
 
 class HmDataOperationResult(IntEnum):
     """Enum with data operation results."""
 
     LOAD_FAIL: Final = 0
     LOAD_SUCCESS: Final = 1
     SAVE_FAIL: Final = 10
@@ -332,14 +342,28 @@
     CE_SECONDARY: Final = "ce_secondary"
     CE_VISIBLE: Final = "ce_visible"
     ENTITY: Final = "entity"
     ENTITY_NO_CREATE: Final = "entity_no_create"
     EVENT: Final = "event"
 
 
+class HmDeviceFirmwareState(StrEnum):
+    """Enum with homematic device firmware states."""
+
+    UP_TO_DATE: Final = "UP_TO_DATE"
+    NEW_FIRMWARE_AVAILABLE: Final = "NEW_FIRMWARE_AVAILABLE"
+    DELIVER_FIRMWARE_IMAGE: Final = "DELIVER_FIRMWARE_IMAGE"
+    READY_FOR_UPDATE: Final = "READY_FOR_UPDATE"
+    DO_UPDATE_PENDING: Final = "DO_UPDATE_PENDING"
+    PERFORMING_UPDATE: Final = "PERFORMING_UPDATE"
+    LIVE_UP_TO_DATE: Final = "LIVE_UP_TO_DATE"
+    LIVE_NEW_FIRMWARE_AVAILABLE: Final = "LIVE_NEW_FIRMWARE_AVAILABLE"
+    LIVE_DELIVER_FIRMWARE_IMAGE: Final = "LIVE_DELIVER_FIRMWARE_IMAGE"
+
+
 class HmPlatform(StrEnum):
     """Enum with platforms relevant for Home Assistant."""
 
     ACTION: Final = "action"
     BINARY_SENSOR: Final = "binary_sensor"
     BUTTON: Final = "button"
     CLIMATE: Final = "climate"
@@ -356,14 +380,36 @@
     LOCK: Final = "lock"
     NUMBER: Final = "number"
     SELECT: Final = "select"
     SENSOR: Final = "sensor"
     SIREN: Final = "siren"
     SWITCH: Final = "switch"
     TEXT: Final = "text"
+    UPDATE: Final = "update"
+
+
+class HmProductGroup(StrEnum):
+    """Enum with homematic product groups."""
+
+    UNKNOWN: Final = PG_UNKNOWN
+    HMIPW: Final = PG_HMIP_WIRED
+    HMIP: Final = PG_HMIP_RF
+    HMW: Final = PG_BIDCOS_WIRED
+    HM: Final = PG_BIDCOS_RF
+    VIRTUAL: Final = PG_VIRTUAL_DEVICES
+
+
+class HmInterface(StrEnum):
+    """Enum with homematic product groups."""
+
+    HMIP: Final = IF_HMIP_RF_NAME
+    HMW: Final = IF_BIDCOS_WIRED_NAME
+    HM: Final = IF_BIDCOS_RF_NAME
+    VIRTUAL: Final = IF_VIRTUAL_DEVICES_NAME
+    LOCAL: Final = LOCAL_INTERFACE
 
 
 class HmEventType(StrEnum):
     """Enum with hahomematic event types."""
 
     DEVICE_AVAILABILITY: Final = "homematic.device_availability"
     DEVICE_ERROR: Final = "homematic.device_error"
@@ -404,14 +450,15 @@
     HmPlatform.LOCK,
     HmPlatform.NUMBER,
     HmPlatform.SELECT,
     HmPlatform.SENSOR,
     HmPlatform.SIREN,
     HmPlatform.SWITCH,
     HmPlatform.TEXT,
+    HmPlatform.UPDATE,
 )
 
 AVAILABLE_HM_HUB_PLATFORMS: Final[tuple[HmPlatform, ...]] = (
     HmPlatform.HUB_BINARY_SENSOR,
     HmPlatform.HUB_BUTTON,
     HmPlatform.HUB_NUMBER,
     HmPlatform.HUB_SELECT,
```

### Comparing `hahomematic-2023.5.0/hahomematic/decorators.py` & `hahomematic-2023.5.1/hahomematic/decorators.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/exceptions.py` & `hahomematic-2023.5.1/hahomematic/exceptions.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/exporter.py` & `hahomematic-2023.5.1/hahomematic/exporter.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/hmcli.py` & `hahomematic-2023.5.1/hahomematic/hmcli.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/json_rpc_client.py` & `hahomematic-2023.5.1/hahomematic/json_rpc_client.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/__init__.py` & `hahomematic-2023.5.1/hahomematic/platforms/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -97,9 +97,8 @@
                     create_entity_and_append_to_device(
                         device=device,
                         channel_address=channel_address,
                         paramset_key=paramset_key,
                         parameter=parameter,
                         parameter_data=parameter_data,
                     )
-
     create_custom_entity_and_append_to_device(device=device)
```

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/__init__.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/__init__.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/climate.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/climate.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/const.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/const.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/cover.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/cover.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/definition.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/definition.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/entity.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/entity.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/light.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/light.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/lock.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/lock.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/siren.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/siren.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/support.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/support.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/custom/switch.py` & `hahomematic-2023.5.1/hahomematic/platforms/custom/switch.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/device.py` & `hahomematic-2023.5.1/hahomematic/platforms/device.py`

 * *Files 17% similar despite different names*

```diff
@@ -9,38 +9,45 @@
 from typing import Any, Final
 
 from hahomematic import central_unit as hmcu, exporter as hmexp
 from hahomematic.const import (
     EVENT_CONFIG_PENDING,
     EVENT_STICKY_UN_REACH,
     EVENT_UN_REACH,
+    HM_AVAILABLE_FIRMWARE,
     HM_FIRMWARE,
+    HM_FIRMWARE_UPDATABLE,
+    HM_FIRMWARE_UPDATE_STATE,
     HM_SUBTYPE,
     HM_TYPE,
     INIT_DATETIME,
     MAX_CACHE_AGE,
     NO_CACHE_ENTRY,
     PARAMSET_KEY_MASTER,
     PARAMSET_KEY_VALUES,
     RELEVANT_INIT_PARAMETERS,
     HmCallSource,
+    HmDeviceFirmwareState,
     HmForcedDeviceAvailability,
+    HmInterface,
+    HmProductGroup,
 )
 from hahomematic.exceptions import BaseHomematicException
 from hahomematic.platforms import custom as cep
 from hahomematic.platforms.custom import entity as hmce
 from hahomematic.platforms.entity import BaseEntity, CallbackEntity
 from hahomematic.platforms.event import GenericEvent
 from hahomematic.platforms.generic.entity import GenericEntity, WrapperEntity
 from hahomematic.platforms.support import (
     PayloadMixin,
     config_property,
     get_device_name,
     value_property,
 )
+from hahomematic.platforms.update import HmUpdate
 from hahomematic.support import updated_within_seconds
 
 _LOGGER = logging.getLogger(__name__)
 
 
 class HmDevice(PayloadMixin):
     """Object to hold information about a device and associated entities."""
@@ -64,68 +71,124 @@
         self.generic_entities: Final[dict[tuple[str, str], GenericEntity]] = {}
         self.wrapper_entities: Final[dict[tuple[str, str], WrapperEntity]] = {}
         self.custom_entities: Final[dict[str, hmce.CustomEntity]] = {}
         self.events: Final[dict[tuple[str, str], GenericEvent]] = {}
         self._attr_last_update: datetime = INIT_DATETIME
         self._forced_availability: HmForcedDeviceAvailability = HmForcedDeviceAvailability.NOT_SET
         self._update_callbacks: Final[list[Callable]] = []
+        self._firmware_update_callbacks: Final[list[Callable]] = []
         self._attr_device_type: Final = str(
             self.central.device_descriptions.get_device_parameter(
                 interface_id=interface_id,
                 device_address=device_address,
                 parameter=HM_TYPE,
             )
         )
         self._attr_sub_type: Final = str(
             central.device_descriptions.get_device_parameter(
                 interface_id=interface_id,
                 device_address=device_address,
                 parameter=HM_SUBTYPE,
             )
         )
+        self._attr_product_group: Final = self._identify_product_group()
         # marker if device will be created as custom entity
         self._has_custom_entity_definition: Final = cep.has_custom_entity_definition_by_device(
             device=self
         )
-        self._attr_firmware: Final = str(
-            self.central.device_descriptions.get_device_parameter(
-                interface_id=interface_id,
-                device_address=device_address,
-                parameter=HM_FIRMWARE,
-            )
-        )
 
         self._attr_name: Final = get_device_name(
             central=central,
             device_address=device_address,
             device_type=self._attr_device_type,
         )
         self.value_cache: Final = ValueCache(device=self)
         self._attr_room: Final = central.device_details.get_room(device_address=device_address)
-
+        self._update_firmware_data()
+        self._attr_update_entity: Final = HmUpdate(device=self)
         _LOGGER.debug(
             "__INIT__: Initialized device: %s, %s, %s, %s",
             self._attr_interface_id,
             self._attr_device_address,
             self._attr_device_type,
             self._attr_name,
         )
 
+    def _update_firmware_data(self) -> None:
+        """Update firmware related data from device descriptions."""
+        self._attr_available_firmware: str | None = (
+            self.central.device_descriptions.get_device_parameter(
+                interface_id=self._attr_interface_id,
+                device_address=self._attr_device_address,
+                parameter=HM_AVAILABLE_FIRMWARE,
+            )
+            or None
+        )
+        self._attr_firmware = str(
+            self.central.device_descriptions.get_device_parameter(
+                interface_id=self._attr_interface_id,
+                device_address=self._attr_device_address,
+                parameter=HM_FIRMWARE,
+            )
+        )
+
+        try:
+            self._attr_firmware_update_state = HmDeviceFirmwareState(
+                str(
+                    self.central.device_descriptions.get_device_parameter(
+                        interface_id=self._attr_interface_id,
+                        device_address=self._attr_device_address,
+                        parameter=HM_FIRMWARE_UPDATE_STATE,
+                    )
+                )
+            )
+        except ValueError:
+            self._attr_firmware_update_state = HmDeviceFirmwareState.UP_TO_DATE
+
+        self._attr_firmware_updatable = bool(
+            self.central.device_descriptions.get_device_parameter(
+                interface_id=self._attr_interface_id,
+                device_address=self._attr_device_address,
+                parameter=HM_FIRMWARE_UPDATABLE,
+            )
+        )
+
+    def _identify_product_group(self) -> HmProductGroup:
+        """Identify the product group of the homematic device."""
+        if self.interface == HmInterface.HMIP:
+            l_device_type = self.device_type.lower()
+            if l_device_type.startswith("hmipw"):
+                return HmProductGroup.HMIPW
+            if l_device_type.startswith("hmip"):
+                return HmProductGroup.HMIP
+        if self.interface == HmInterface.HMW:
+            return HmProductGroup.HMW
+        if self.interface == HmInterface.HM:
+            return HmProductGroup.HM
+        if self.interface == HmInterface.VIRTUAL:
+            return HmProductGroup.VIRTUAL
+        return HmProductGroup.UNKNOWN
+
     @value_property
     def available(self) -> bool:
         """Return the availability of the device."""
         if self._forced_availability != HmForcedDeviceAvailability.NOT_SET:
             return self._forced_availability == HmForcedDeviceAvailability.FORCE_TRUE
         un_reach = self._e_unreach
         if un_reach is None:
             un_reach = self._e_sticky_un_reach
         if un_reach is not None and un_reach.value is not None:
             return not un_reach.value
         return True
 
+    @config_property
+    def available_firmware(self) -> str | None:
+        """Return the available firmware of the device."""
+        return self._attr_available_firmware
+
     @property
     def config_pending(self) -> bool:
         """Return if a config change of the device is pending."""
         if self._e_config_pending is not None and self._e_config_pending.value is not None:
             return self._e_config_pending.value is True
         return False
 
@@ -141,14 +204,24 @@
 
     @config_property
     def firmware(self) -> str:
         """Return the firmware of the device."""
         return self._attr_firmware
 
     @config_property
+    def firmware_updatable(self) -> bool:
+        """Return the firmware update state of the device."""
+        return self._attr_firmware_updatable
+
+    @config_property
+    def firmware_update_state(self) -> HmDeviceFirmwareState:
+        """Return the firmware update state of the device."""
+        return self._attr_firmware_update_state
+
+    @config_property
     def interface(self) -> str:
         """Return the interface of the device."""
         return self._attr_interface
 
     @config_property
     def interface_id(self) -> str:
         """Return the interface_id of the device."""
@@ -161,24 +234,34 @@
 
     @config_property
     def name(self) -> str:
         """Return the name of the device."""
         return self._attr_name
 
     @config_property
+    def product_group(self) -> HmProductGroup:
+        """Return the product group of the device."""
+        return self._attr_product_group
+
+    @config_property
     def room(self) -> str | None:
         """Return the room of the device."""
         return self._attr_room
 
     @config_property
     def sub_type(self) -> str:
         """Return the sub_type of the device."""
         return self._attr_sub_type
 
     @property
+    def update_entity(self) -> HmUpdate:
+        """Return the device firmware update entity of the device."""
+        return self._attr_update_entity
+
+    @property
     def _e_unreach(self) -> GenericEntity | None:
         """Return th UNREACH entity."""
         return self.generic_entities.get((f"{self._attr_device_address}:0", EVENT_UN_REACH))
 
     @property
     def _e_sticky_un_reach(self) -> GenericEntity | None:
         """Return th STICKY_UN_REACH entity."""
@@ -246,14 +329,27 @@
             self._update_callbacks.append(update_callback)
 
     def unregister_update_callback(self, update_callback: Callable) -> None:
         """Remove update callback."""
         if update_callback in self._update_callbacks:
             self._update_callbacks.remove(update_callback)
 
+    def register_firmware_update_callback(self, firmware_update_callback: Callable) -> None:
+        """Register firmware update callback."""
+        if (
+            callable(firmware_update_callback)
+            and firmware_update_callback not in self._firmware_update_callbacks
+        ):
+            self._firmware_update_callbacks.append(firmware_update_callback)
+
+    def unregister_firmware_update_callback(self, firmware_update_callback: Callable) -> None:
+        """Remove firmware update callback."""
+        if firmware_update_callback in self._firmware_update_callbacks:
+            self._firmware_update_callbacks.remove(firmware_update_callback)
+
     def _set_last_update(self) -> None:
         self._attr_last_update = datetime.now()
 
     def get_all_entities(self) -> list[hmce.CustomEntity | GenericEntity | WrapperEntity]:
         """Return all entities of a device."""
         all_entities: list[hmce.CustomEntity | GenericEntity | WrapperEntity] = []
         all_entities.extend(self.custom_entities.values())
@@ -276,14 +372,36 @@
         """Export the device definition for current device."""
         await hmexp.save_device_definition(
             client=self.client,
             interface_id=self._attr_interface_id,
             device_address=self._attr_device_address,
         )
 
+    def refresh_firmware_data(self) -> None:
+        """Refresh firmware data of the device."""
+        old_available_firmware = self._attr_available_firmware
+        old_firmware = self._attr_firmware
+        old_firmware_update_state = self._attr_firmware_update_state
+        old_firmware_updatable = self._attr_firmware_updatable
+
+        self._update_firmware_data()
+
+        if (
+            old_available_firmware != self._attr_available_firmware
+            or old_firmware != self._attr_firmware
+            or old_firmware_update_state != self._attr_firmware_update_state
+            or old_firmware_updatable != self._attr_firmware_updatable
+        ):
+            for _firmware_callback in self._firmware_update_callbacks:
+                _firmware_callback()
+
+    async def update_firmware(self) -> bool:
+        """Update the firmware of the homematic device."""
+        return await self.client.update_device_firmware(device_address=self._attr_device_address)
+
     async def load_value_cache(self) -> None:
         """Init the parameter cache."""
         if len(self.generic_entities) > 0:
             await self.value_cache.init_base_entities()
         if len(self.events) > 0:
             await self.value_cache.init_readable_events()
         _LOGGER.debug(
```

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/entity.py` & `hahomematic-2023.5.1/hahomematic/platforms/entity.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/event.py` & `hahomematic-2023.5.1/hahomematic/platforms/event.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/__init__.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/__init__.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/action.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/action.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/binary_sensor.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/binary_sensor.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/button.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/button.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/entity.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/entity.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/number.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/number.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/select.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/select.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/sensor.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/sensor.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/generic/switch.py` & `hahomematic-2023.5.1/hahomematic/platforms/generic/switch.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/__init__.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/__init__.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/binary_sensor.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/binary_sensor.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/button.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/button.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/entity.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/entity.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/number.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/number.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/select.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/select.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/sensor.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/sensor.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/hub/text.py` & `hahomematic-2023.5.1/hahomematic/platforms/hub/text.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/platforms/support.py` & `hahomematic-2023.5.1/hahomematic/platforms/support.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/rega_scripts/fetch_all_device_data.fn` & `hahomematic-2023.5.1/hahomematic/rega_scripts/fetch_all_device_data.fn`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/rega_scripts/get_serial.fn` & `hahomematic-2023.5.1/hahomematic/rega_scripts/get_serial.fn`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/rega_scripts/get_system_variables_ext_marker.fn` & `hahomematic-2023.5.1/hahomematic/rega_scripts/get_system_variables_ext_marker.fn`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/support.py` & `hahomematic-2023.5.1/hahomematic/support.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/xml_rpc_proxy.py` & `hahomematic-2023.5.1/hahomematic/xml_rpc_proxy.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic/xml_rpc_server.py` & `hahomematic-2023.5.1/hahomematic/xml_rpc_server.py`

 * *Files identical despite different names*

### Comparing `hahomematic-2023.5.0/hahomematic.egg-info/PKG-INFO` & `hahomematic-2023.5.1/hahomematic.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hahomematic
-Version: 2023.5.0
+Version: 2023.5.1
 Summary: Homematic interface for Home Assistant running on Python 3.
 Home-page: https://github.com/danielperna84/hahomematic
 Author-email: Daniel Perna <danielperna84@gmail.com>, SukramJ <sukramj@icloud.com>
 License: MIT License
 Project-URL: Source Code, https://github.com/danielperna84/hahomematic
 Project-URL: Bug Reports, https://github.com/danielperna84/hahomematic/issues
 Project-URL: Docs: Dev, https://github.com/danielperna84/hahomematic
```

### Comparing `hahomematic-2023.5.0/hahomematic.egg-info/SOURCES.txt` & `hahomematic-2023.5.1/hahomematic.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -28,14 +28,15 @@
 hahomematic/caches/persistent.py
 hahomematic/caches/visibility.py
 hahomematic/platforms/__init__.py
 hahomematic/platforms/device.py
 hahomematic/platforms/entity.py
 hahomematic/platforms/event.py
 hahomematic/platforms/support.py
+hahomematic/platforms/update.py
 hahomematic/platforms/custom/__init__.py
 hahomematic/platforms/custom/climate.py
 hahomematic/platforms/custom/const.py
 hahomematic/platforms/custom/cover.py
 hahomematic/platforms/custom/definition.py
 hahomematic/platforms/custom/entity.py
 hahomematic/platforms/custom/light.py
```

### Comparing `hahomematic-2023.5.0/pyproject.toml` & `hahomematic-2023.5.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools~=62.3", "wheel~=0.37.1"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name        = "hahomematic"
-version     = "2023.5.0"
+version     = "2023.5.1"
 license     = {text = "MIT License"}
 description = "Homematic interface for Home Assistant running on Python 3."
 readme      = "README.md"
 authors     = [
     {name = "Daniel Perna", email = "danielperna84@gmail.com"},
     {name = "SukramJ", email = "sukramj@icloud.com"},
 ]
```

