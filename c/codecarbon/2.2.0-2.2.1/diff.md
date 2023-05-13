# Comparing `tmp/codecarbon-2.2.0.tar.gz` & `tmp/codecarbon-2.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "codecarbon-2.2.0.tar", last modified: Wed May 10 21:13:19 2023, max compression
+gzip compressed data, was "codecarbon-2.2.1.tar", last modified: Sat May 13 07:17:41 2023, max compression
```

## Comparing `codecarbon-2.2.0.tar` & `codecarbon-2.2.1.tar`

### file list

```diff
@@ -1,119 +1,119 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.224247 codecarbon-2.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-10 21:13:03.000000 codecarbon-2.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5856 2023-05-10 21:13:19.224247 codecarbon-2.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5364 2023-05-10 21:13:03.000000 codecarbon-2.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.204246 codecarbon-2.2.0/carbonserver/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.204246 codecarbon-2.2.0/carbonserver/carbonserver/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.204246 codecarbon-2.2.0/carbonserver/carbonserver/api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      670 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/dependencies.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.208246 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      506 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/experiments.py
--rw-r--r--   0 runner    (1001) docker     (123)      418 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/organizations.py
--rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/projects.py
--rw-r--r--   0 runner    (1001) docker     (123)      177 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/runs.py
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/teams.py
--rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/domain/users.py
--rw-r--r--   0 runner    (1001) docker     (123)      791 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/errors.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.208246 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      908 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/authenticate.py
--rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2871 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/experiments.py
--rw-r--r--   0 runner    (1001) docker     (123)     2735 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/organizations.py
--rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/projects.py
--rw-r--r--   0 runner    (1001) docker     (123)     3563 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/runs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1697 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/teams.py
--rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/routers/users.py
--rw-r--r--   0 runner    (1001) docker     (123)     9372 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/api/schemas.py
--rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.208246 codecarbon-2.2.0/carbonserver/carbonserver/database/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/database/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      626 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/database/database.py
--rw-r--r--   0 runner    (1001) docker     (123)      511 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/carbonserver/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     4161 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/container.py
--rw-r--r--   0 runner    (1001) docker     (123)     2771 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/main.py
--rw-r--r--   0 runner    (1001) docker     (123)     1047 2023-05-10 21:13:03.000000 codecarbon-2.2.0/carbonserver/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.208246 codecarbon-2.2.0/codecarbon/
--rw-r--r--   0 runner    (1001) docker     (123)      321 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.212246 codecarbon-2.2.0/codecarbon/cli/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1132 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/cli/cli_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2701 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/cli/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6551 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/api_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     3604 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/cloud.py
--rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/co2_signal.py
--rw-r--r--   0 runner    (1001) docker     (123)     3274 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    13758 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)    11305 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)     7478 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/gpu.py
--rw-r--r--   0 runner    (1001) docker     (123)     1914 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/rapl.py
--rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/schemas.py
--rw-r--r--   0 runner    (1001) docker     (123)     3281 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/units.py
--rw-r--r--   0 runner    (1001) docker     (123)     3098 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/core/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.204246 codecarbon-2.2.0/codecarbon/data/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/data/cloud/
--rw-r--r--   0 runner    (1001) docker     (123)    11411 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/cloud/impact.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/data/hardware/
--rw-r--r--   0 runner    (1001) docker     (123)    49423 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/hardware/cpu_power.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/data/private_infra/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/data/private_infra/2016/
--rw-r--r--   0 runner    (1001) docker     (123)     3690 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/private_infra/2016/canada_energy_mix.json
--rw-r--r--   0 runner    (1001) docker     (123)     3778 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/private_infra/2016/usa_emissions.json
--rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/private_infra/carbon_intensity_per_source.json
--rw-r--r--   0 runner    (1001) docker     (123)    81313 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/data/private_infra/global_energy_mix.json
--rw-r--r--   0 runner    (1001) docker     (123)    37320 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/emissions_tracker.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.216246 codecarbon-2.2.0/codecarbon/external/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/external/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/external/geography.py
--rw-r--r--   0 runner    (1001) docker     (123)    11030 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/external/hardware.py
--rw-r--r--   0 runner    (1001) docker     (123)     1685 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/external/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     1482 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/external/scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     4352 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/input.py
--rw-r--r--   0 runner    (1001) docker     (123)     6866 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/output.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.220247 codecarbon-2.2.0/codecarbon/viz/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.220247 codecarbon-2.2.0/codecarbon/viz/assets/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/assets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    25442 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/assets/car_icon.png
--rw-r--r--   0 runner    (1001) docker     (123)    29734 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/assets/house_icon.png
--rw-r--r--   0 runner    (1001) docker     (123)    29874 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/assets/tv_icon.png
--rw-r--r--   0 runner    (1001) docker     (123)    11004 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/carbonboard.py
--rw-r--r--   0 runner    (1001) docker     (123)    11141 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/carbonboard_on_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    27905 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/components.py
--rw-r--r--   0 runner    (1001) docker     (123)    11230 2023-05-10 21:13:03.000000 codecarbon-2.2.0/codecarbon/viz/data.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.212246 codecarbon-2.2.0/codecarbon.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5856 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3236 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-10 21:13:19.000000 codecarbon-2.2.0/codecarbon.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-10 21:13:19.224247 codecarbon-2.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1841 2023-05-10 21:13:03.000000 codecarbon-2.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:13:19.224247 codecarbon-2.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     2862 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_api_call.py
--rw-r--r--   0 runner    (1001) docker     (123)     2816 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_cloud.py
--rw-r--r--   0 runner    (1001) docker     (123)     1393 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_co2_signal.py
--rw-r--r--   0 runner    (1001) docker     (123)     5664 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)      562 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_core_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    10298 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)     6318 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)    12810 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_emissions_tracker.py
--rw-r--r--   0 runner    (1001) docker     (123)     3629 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_emissions_tracker_constant.py
--rw-r--r--   0 runner    (1001) docker     (123)     2890 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_emissions_tracker_flush.py
--rw-r--r--   0 runner    (1001) docker     (123)     1479 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_energy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2334 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_geography.py
--rw-r--r--   0 runner    (1001) docker     (123)     7180 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_gpu.py
--rw-r--r--   0 runner    (1001) docker     (123)      857 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_hardware.py
--rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_logging_output.py
--rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/test_ram.py
--rw-r--r--   0 runner    (1001) docker     (123)     7558 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/testdata.py
--rw-r--r--   0 runner    (1001) docker     (123)     1009 2023-05-10 21:13:03.000000 codecarbon-2.2.0/tests/testutils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.198661 codecarbon-2.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 07:17:25.000000 codecarbon-2.2.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5958 2023-05-13 07:17:41.194661 codecarbon-2.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5364 2023-05-13 07:17:25.000000 codecarbon-2.2.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.170661 codecarbon-2.2.1/carbonserver/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.170661 codecarbon-2.2.1/carbonserver/carbonserver/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.170661 codecarbon-2.2.1/carbonserver/carbonserver/api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      670 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/dependencies.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.174661 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      506 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      526 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/experiments.py
+-rw-r--r--   0 runner    (1001) docker     (123)      418 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/organizations.py
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/projects.py
+-rw-r--r--   0 runner    (1001) docker     (123)      177 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/runs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/teams.py
+-rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/domain/users.py
+-rw-r--r--   0 runner    (1001) docker     (123)      791 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/errors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.174661 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/authenticate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2871 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/experiments.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2735 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/organizations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/projects.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3563 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/runs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1697 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/teams.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/routers/users.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9372 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/api/schemas.py
+-rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.178660 codecarbon-2.2.1/carbonserver/carbonserver/database/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/database/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      626 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/database/database.py
+-rw-r--r--   0 runner    (1001) docker     (123)      511 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/carbonserver/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4161 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/container.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2771 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1047 2023-05-13 07:17:25.000000 codecarbon-2.2.1/carbonserver/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.178660 codecarbon-2.2.1/codecarbon/
+-rw-r--r--   0 runner    (1001) docker     (123)      321 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.182661 codecarbon-2.2.1/codecarbon/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1132 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/cli/cli_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2701 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/cli/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.182661 codecarbon-2.2.1/codecarbon/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6551 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/api_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3604 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/cloud.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/co2_signal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3274 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13758 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11305 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7478 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/gpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2066 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/rapl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/schemas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3281 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/units.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3098 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/core/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.166660 codecarbon-2.2.1/codecarbon/data/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.182661 codecarbon-2.2.1/codecarbon/data/cloud/
+-rw-r--r--   0 runner    (1001) docker     (123)    11411 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/cloud/impact.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.186661 codecarbon-2.2.1/codecarbon/data/hardware/
+-rw-r--r--   0 runner    (1001) docker     (123)    49423 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/hardware/cpu_power.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.186661 codecarbon-2.2.1/codecarbon/data/private_infra/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.186661 codecarbon-2.2.1/codecarbon/data/private_infra/2016/
+-rw-r--r--   0 runner    (1001) docker     (123)     3690 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/private_infra/2016/canada_energy_mix.json
+-rw-r--r--   0 runner    (1001) docker     (123)     3778 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/private_infra/2016/usa_emissions.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/private_infra/carbon_intensity_per_source.json
+-rw-r--r--   0 runner    (1001) docker     (123)    81313 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/data/private_infra/global_energy_mix.json
+-rw-r--r--   0 runner    (1001) docker     (123)    37320 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/emissions_tracker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.186661 codecarbon-2.2.1/codecarbon/external/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/external/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/external/geography.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11030 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/external/hardware.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1685 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/external/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1482 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/external/scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4352 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/input.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6866 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/output.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.190661 codecarbon-2.2.1/codecarbon/viz/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.190661 codecarbon-2.2.1/codecarbon/viz/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/assets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25442 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/assets/car_icon.png
+-rw-r--r--   0 runner    (1001) docker     (123)    29734 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/assets/house_icon.png
+-rw-r--r--   0 runner    (1001) docker     (123)    29874 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/assets/tv_icon.png
+-rw-r--r--   0 runner    (1001) docker     (123)    11004 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/carbonboard.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11141 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/carbonboard_on_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27905 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/components.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11230 2023-05-13 07:17:25.000000 codecarbon-2.2.1/codecarbon/viz/data.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.178660 codecarbon-2.2.1/codecarbon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5958 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3236 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 07:17:41.000000 codecarbon-2.2.1/codecarbon.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 07:17:41.198661 codecarbon-2.2.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1941 2023-05-13 07:17:25.000000 codecarbon-2.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:17:41.194661 codecarbon-2.2.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2862 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_api_call.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2816 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_cloud.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1393 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_co2_signal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5664 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      562 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_core_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10298 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6318 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12810 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_emissions_tracker.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3629 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_emissions_tracker_constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2890 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_emissions_tracker_flush.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1479 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_energy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2334 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_geography.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7180 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_gpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)      857 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_hardware.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_logging_output.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/test_ram.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7558 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/testdata.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1009 2023-05-13 07:17:25.000000 codecarbon-2.2.1/tests/testutils.py
```

### Comparing `codecarbon-2.2.0/LICENSE` & `codecarbon-2.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/PKG-INFO` & `codecarbon-2.2.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 Metadata-Version: 2.1
 Name: codecarbon
-Version: 2.2.0
+Version: 2.2.1
 Author: Mila, DataForGood, BCG GAMMA, Comet.ml, Haverford College
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >3.6
 Description-Content-Type: text/markdown
 Provides-Extra: viz
 Provides-Extra: dashboard
 License-File: LICENSE
```

### Comparing `codecarbon-2.2.0/README.md` & `codecarbon-2.2.1/README.md`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/dependencies.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/dependencies.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/domain/experiments.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/domain/experiments.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/errors.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/errors.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/authenticate.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/authenticate.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/emissions.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/emissions.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/experiments.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/experiments.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/organizations.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/organizations.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/projects.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/projects.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/runs.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/runs.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/teams.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/teams.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/routers/users.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/routers/users.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/api/schemas.py` & `codecarbon-2.2.1/carbonserver/carbonserver/api/schemas.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/carbonserver/database/database.py` & `codecarbon-2.2.1/carbonserver/carbonserver/database/database.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/container.py` & `codecarbon-2.2.1/carbonserver/container.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/main.py` & `codecarbon-2.2.1/carbonserver/main.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/carbonserver/setup.py` & `codecarbon-2.2.1/carbonserver/setup.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/cli/cli_utils.py` & `codecarbon-2.2.1/codecarbon/cli/cli_utils.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/cli/main.py` & `codecarbon-2.2.1/codecarbon/cli/main.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/api_client.py` & `codecarbon-2.2.1/codecarbon/core/api_client.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/cloud.py` & `codecarbon-2.2.1/codecarbon/core/cloud.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/co2_signal.py` & `codecarbon-2.2.1/codecarbon/core/co2_signal.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/config.py` & `codecarbon-2.2.1/codecarbon/core/config.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/cpu.py` & `codecarbon-2.2.1/codecarbon/core/cpu.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/emissions.py` & `codecarbon-2.2.1/codecarbon/core/emissions.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/gpu.py` & `codecarbon-2.2.1/codecarbon/core/gpu.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/rapl.py` & `codecarbon-2.2.1/codecarbon/core/rapl.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,22 +1,29 @@
-from dataclasses import dataclass
+from dataclasses import dataclass, field
 
 from codecarbon.core.units import Energy, Power, Time
 from codecarbon.external.logger import logger
 
 
 @dataclass
 class RAPLFile:
-    name: str  # RAPL device being measured
-    path: str  # Path to file containing RAPL reading
-    max_path: str  # Path to corresponding file containing maximum possible RAPL reading
-    energy_delta: Energy = Energy(0)  # Energy consumed in kWh
-    power: Power = Power(0)  # Power based on reading
-    last_energy: Energy = Energy(0)  # Last energy reading in kWh
-    max_energy_reading: Energy = Energy(0)  # Max value energy can hold before it wraps
+    # RAPL device being measured
+    name: str
+    # Path to file containing RAPL reading
+    path: str
+    # Path to corresponding file containing maximum possible RAPL reading
+    max_path: str
+    # Energy consumed in kWh
+    energy_delta: Energy = field(default_factory=lambda: Energy(0))
+    # Power based on reading
+    power: Power = field(default_factory=lambda: Power(0))
+    # Last energy reading in kWh
+    last_energy: Energy = field(default_factory=lambda: Energy(0))
+    # Max value energy can hold before it wraps
+    max_energy_reading: Energy = field(default_factory=lambda: Energy(0))
 
     def __post_init__(self):
         self.last_energy = self._get_value()
         with open(self.max_path, "r") as f:
             max_micro_joules = float(f.read())
 
             self.max_energy_reading = Energy.from_ujoules(max_micro_joules)
```

### Comparing `codecarbon-2.2.0/codecarbon/core/schemas.py` & `codecarbon-2.2.1/codecarbon/core/schemas.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/units.py` & `codecarbon-2.2.1/codecarbon/core/units.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/core/util.py` & `codecarbon-2.2.1/codecarbon/core/util.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/cloud/impact.csv` & `codecarbon-2.2.1/codecarbon/data/cloud/impact.csv`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/hardware/cpu_power.csv` & `codecarbon-2.2.1/codecarbon/data/hardware/cpu_power.csv`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/private_infra/2016/canada_energy_mix.json` & `codecarbon-2.2.1/codecarbon/data/private_infra/2016/canada_energy_mix.json`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/private_infra/2016/usa_emissions.json` & `codecarbon-2.2.1/codecarbon/data/private_infra/2016/usa_emissions.json`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/private_infra/carbon_intensity_per_source.json` & `codecarbon-2.2.1/codecarbon/data/private_infra/carbon_intensity_per_source.json`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/data/private_infra/global_energy_mix.json` & `codecarbon-2.2.1/codecarbon/data/private_infra/global_energy_mix.json`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/emissions_tracker.py` & `codecarbon-2.2.1/codecarbon/emissions_tracker.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/external/geography.py` & `codecarbon-2.2.1/codecarbon/external/geography.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/external/hardware.py` & `codecarbon-2.2.1/codecarbon/external/hardware.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/external/logger.py` & `codecarbon-2.2.1/codecarbon/external/logger.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/external/scheduler.py` & `codecarbon-2.2.1/codecarbon/external/scheduler.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/input.py` & `codecarbon-2.2.1/codecarbon/input.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/output.py` & `codecarbon-2.2.1/codecarbon/output.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/assets/car_icon.png` & `codecarbon-2.2.1/codecarbon/viz/assets/car_icon.png`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/assets/house_icon.png` & `codecarbon-2.2.1/codecarbon/viz/assets/house_icon.png`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/assets/tv_icon.png` & `codecarbon-2.2.1/codecarbon/viz/assets/tv_icon.png`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/carbonboard.py` & `codecarbon-2.2.1/codecarbon/viz/carbonboard.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/carbonboard_on_api.py` & `codecarbon-2.2.1/codecarbon/viz/carbonboard_on_api.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/components.py` & `codecarbon-2.2.1/codecarbon/viz/components.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon/viz/data.py` & `codecarbon-2.2.1/codecarbon/viz/data.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/codecarbon.egg-info/PKG-INFO` & `codecarbon-2.2.1/codecarbon.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 Metadata-Version: 2.1
 Name: codecarbon
-Version: 2.2.0
+Version: 2.2.1
 Author: Mila, DataForGood, BCG GAMMA, Comet.ml, Haverford College
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >3.6
 Description-Content-Type: text/markdown
 Provides-Extra: viz
 Provides-Extra: dashboard
 License-File: LICENSE
```

### Comparing `codecarbon-2.2.0/codecarbon.egg-info/SOURCES.txt` & `codecarbon-2.2.1/codecarbon.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/setup.py` & `codecarbon-2.2.1/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 ]
 
 TEST_DEPENDENCIES = ["mock", "pytest", "responses", "tox", "numpy", "requests-mock"]
 
 
 setuptools.setup(
     name="codecarbon",
-    version="2.2.0",
+    version="2.2.1",
     author="Mila, DataForGood, BCG GAMMA, Comet.ml, Haverford College",
     long_description=long_description,
     long_description_content_type="text/markdown",
     license_files=("LICENSE",),
     packages=setuptools.find_packages(
         exclude=["*.tests", "*.tests.*", "tests.*", "tests"]
     ),
@@ -34,14 +34,16 @@
         "dashboard": ["dash>=2.2.0", "plotly>=5.6.0", "dash_bootstrap_components"],
     },
     classifiers=[
         "Natural Language :: English",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
+        "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
         "License :: OSI Approved :: MIT License",
     ],
     package_data={
         "codecarbon": [
             "data/cloud/impact.csv",
             "data/hardware/cpu_power.csv",
             "data/private_infra/2016/usa_emissions.json",
```

### Comparing `codecarbon-2.2.0/tests/test_api_call.py` & `codecarbon-2.2.1/tests/test_api_call.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_cloud.py` & `codecarbon-2.2.1/tests/test_cloud.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_co2_signal.py` & `codecarbon-2.2.1/tests/test_co2_signal.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_config.py` & `codecarbon-2.2.1/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_core_util.py` & `codecarbon-2.2.1/tests/test_core_util.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_cpu.py` & `codecarbon-2.2.1/tests/test_cpu.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_emissions.py` & `codecarbon-2.2.1/tests/test_emissions.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_emissions_tracker.py` & `codecarbon-2.2.1/tests/test_emissions_tracker.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_emissions_tracker_constant.py` & `codecarbon-2.2.1/tests/test_emissions_tracker_constant.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_emissions_tracker_flush.py` & `codecarbon-2.2.1/tests/test_emissions_tracker_flush.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_energy.py` & `codecarbon-2.2.1/tests/test_energy.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_geography.py` & `codecarbon-2.2.1/tests/test_geography.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_gpu.py` & `codecarbon-2.2.1/tests/test_gpu.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_hardware.py` & `codecarbon-2.2.1/tests/test_hardware.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_logging_output.py` & `codecarbon-2.2.1/tests/test_logging_output.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/test_ram.py` & `codecarbon-2.2.1/tests/test_ram.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/testdata.py` & `codecarbon-2.2.1/tests/testdata.py`

 * *Files identical despite different names*

### Comparing `codecarbon-2.2.0/tests/testutils.py` & `codecarbon-2.2.1/tests/testutils.py`

 * *Files identical despite different names*

