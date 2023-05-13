# Comparing `tmp/dagster-toolbox-0.0.4.tar.gz` & `tmp/dagster-toolbox-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dagster-toolbox-0.0.4.tar", last modified: Sat May 13 09:21:57 2023, max compression
+gzip compressed data, was "dagster-toolbox-0.0.5.tar", last modified: Sat May 13 09:39:22 2023, max compression
```

## Comparing `dagster-toolbox-0.0.4.tar` & `dagster-toolbox-0.0.5.tar`

### file list

```diff
@@ -1,59 +1,59 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.672119 dagster-toolbox-0.0.4/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-13 09:21:57.672119 dagster-toolbox-0.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      172 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.660119 dagster-toolbox-0.0.4/dagster_toolbox/
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.660119 dagster-toolbox-0.0.4/dagster_toolbox/functions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2111 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/dataframe.py
--rw-r--r--   0 runner    (1001) docker     (123)     4070 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/ftp.py
--rw-r--r--   0 runner    (1001) docker     (123)    10778 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/google_analytics.py
--rw-r--r--   0 runner    (1001) docker     (123)      111 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/partitions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4062 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/sftp.py
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/functions/text.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.664119 dagster-toolbox-0.0.4/dagster_toolbox/resources/
--rw-r--r--   0 runner    (1001) docker     (123)     1011 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2391 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/abstract.py
--rw-r--r--   0 runner    (1001) docker     (123)     4799 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/csv_partitioned_io_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4412 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/json_partitioned_io_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1385 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/object_storage.py
--rw-r--r--   0 runner    (1001) docker     (123)     6597 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/postgres_io_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     6936 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/postgres_partitioned_io_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/resources/vault.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.664119 dagster-toolbox-0.0.4/dagster_toolbox/types/
--rw-r--r--   0 runner    (1001) docker     (123)     1008 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.668119 dagster-toolbox-0.0.4/dagster_toolbox/types/common/
--rw-r--r--   0 runner    (1001) docker     (123)      344 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/cities.py
--rw-r--r--   0 runner    (1001) docker     (123)      487 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/continents.py
--rw-r--r--   0 runner    (1001) docker     (123)      696 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/countries.py
--rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/postcodes.py
--rw-r--r--   0 runner    (1001) docker     (123)      537 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/regions.py
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/common/subregions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.668119 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/container_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)      442 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/continent_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)     4706 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/country_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/currency_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)      656 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/language_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)      802 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/subdivision_codes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1583 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/units_of_measure.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.668119 dagster-toolbox-0.0.4/dagster_toolbox/types/geonames/
--rw-r--r--   0 runner    (1001) docker     (123)       89 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/geonames/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/geonames/postal_codes.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.668119 dagster-toolbox-0.0.4/dagster_toolbox/types/google_analytics/
--rw-r--r--   0 runner    (1001) docker     (123)      220 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/google_analytics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8338 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/google_analytics/google_analytics.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.668119 dagster-toolbox-0.0.4/dagster_toolbox/types/open_data_fr/
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/open_data_fr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      974 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/dagster_toolbox/types/open_data_fr/agriculture_ministry.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:21:57.660119 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-13 09:21:57.000000 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-05-13 09:21:57.000000 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:21:57.000000 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 09:21:57.000000 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 09:21:57.000000 dagster-toolbox-0.0.4/dagster_toolbox.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:21:57.672119 dagster-toolbox-0.0.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 09:21:47.000000 dagster-toolbox-0.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      172 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox/
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox/functions/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2111 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/dataframe.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4070 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/ftp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10778 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/google_analytics.py
+-rw-r--r--   0 runner    (1001) docker     (123)      111 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/partitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4062 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/sftp.py
+-rw-r--r--   0 runner    (1001) docker     (123)      750 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/functions/text.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox/resources/
+-rw-r--r--   0 runner    (1001) docker     (123)     1011 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2391 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/abstract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4799 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/csv_partitioned_io_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4412 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/json_partitioned_io_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1385 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/object_storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6597 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/postgres_io_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6936 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/postgres_partitioned_io_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/resources/vault.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox/types/
+-rw-r--r--   0 runner    (1001) docker     (123)     1008 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox/types/common/
+-rw-r--r--   0 runner    (1001) docker     (123)      344 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/cities.py
+-rw-r--r--   0 runner    (1001) docker     (123)      487 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/continents.py
+-rw-r--r--   0 runner    (1001) docker     (123)      696 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/countries.py
+-rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/postcodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      537 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/regions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/common/subregions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/container_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      442 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/continent_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4706 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/country_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/currency_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      656 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/language_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      802 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/subdivision_codes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1583 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/units_of_measure.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/dagster_toolbox/types/geonames/
+-rw-r--r--   0 runner    (1001) docker     (123)       89 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/geonames/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/geonames/postal_codes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/dagster_toolbox/types/google_analytics/
+-rw-r--r--   0 runner    (1001) docker     (123)      220 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/google_analytics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8338 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/google_analytics/google_analytics.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/dagster_toolbox/types/open_data_fr/
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/open_data_fr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      974 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/dagster_toolbox/types/open_data_fr/agriculture_ministry.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:39:22.986111 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      727 2023-05-13 09:39:22.000000 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-05-13 09:39:22.000000 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:39:22.000000 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 09:39:22.000000 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 09:39:22.000000 dagster-toolbox-0.0.5/dagster_toolbox.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:39:22.990111 dagster-toolbox-0.0.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 09:39:14.000000 dagster-toolbox-0.0.5/setup.py
```

### Comparing `dagster-toolbox-0.0.4/LICENSE` & `dagster-toolbox-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/PKG-INFO` & `dagster-toolbox-0.0.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dagster-toolbox
-Version: 0.0.4
+Version: 0.0.5
 Summary: A set of tools to ease Dagster usage
 Home-page: https://github.com/nicolasramy/dagster-toolbox
 Author: Nicolas RAMY
 Author-email: nicolas.ramy@darkelda.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/functions/dataframe.py` & `dagster-toolbox-0.0.5/dagster_toolbox/functions/dataframe.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/functions/ftp.py` & `dagster-toolbox-0.0.5/dagster_toolbox/functions/ftp.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/functions/google_analytics.py` & `dagster-toolbox-0.0.5/dagster_toolbox/functions/google_analytics.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/functions/sftp.py` & `dagster-toolbox-0.0.5/dagster_toolbox/functions/sftp.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/functions/text.py` & `dagster-toolbox-0.0.5/dagster_toolbox/functions/text.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/__init__.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/__init__.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/abstract.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/abstract.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/csv_partitioned_io_manager.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/csv_partitioned_io_manager.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/json_partitioned_io_manager.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/json_partitioned_io_manager.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/object_storage.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/object_storage.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/postgres_io_manager.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/postgres_io_manager.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/postgres_partitioned_io_manager.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/postgres_partitioned_io_manager.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/resources/vault.py` & `dagster-toolbox-0.0.5/dagster_toolbox/resources/vault.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/__init__.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/__init__.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/common/cities.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/common/cities.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/common/countries.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/common/countries.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/common/postcodes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/common/postcodes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/common/regions.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/common/regions.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/common/subregions.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/common/subregions.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/__init__.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/__init__.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/container_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/container_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/country_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/country_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/currency_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/currency_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/language_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/language_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/subdivision_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/subdivision_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/datahub/units_of_measure.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/datahub/units_of_measure.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/geonames/postal_codes.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/geonames/postal_codes.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/google_analytics/google_analytics.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/google_analytics/google_analytics.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox/types/open_data_fr/agriculture_ministry.py` & `dagster-toolbox-0.0.5/dagster_toolbox/types/open_data_fr/agriculture_ministry.py`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox.egg-info/PKG-INFO` & `dagster-toolbox-0.0.5/dagster_toolbox.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dagster-toolbox
-Version: 0.0.4
+Version: 0.0.5
 Summary: A set of tools to ease Dagster usage
 Home-page: https://github.com/nicolasramy/dagster-toolbox
 Author: Nicolas RAMY
 Author-email: nicolas.ramy@darkelda.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `dagster-toolbox-0.0.4/dagster_toolbox.egg-info/SOURCES.txt` & `dagster-toolbox-0.0.5/dagster_toolbox.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `dagster-toolbox-0.0.4/setup.py` & `dagster-toolbox-0.0.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="dagster-toolbox",
-    version="0.0.4",
+    version="0.0.5",
     packages=find_packages(),
     author="Nicolas RAMY",
     author_email="nicolas.ramy@darkelda.com",
     license="MIT",
     description="A set of tools to ease Dagster usage",
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
@@ -19,15 +19,15 @@
         "google-api-python-client==2.68.0",
         "hvac==1.0.2",
         "minio==7.1.12",
         "oauth2client==4.1.3",
         "pandas==1.5.2",
         "python-slugify==7.0.0",
         "requests==2.28.1",
-        "SQLAlchemy==1.4.45",
+        "SQLAlchemy==1.4.46",
     ],
     url="https://github.com/nicolasramy/dagster-toolbox",
     classifiers=[
         "Development Status :: 3 - Alpha",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
         "Programming Language :: Python :: 3.10",
```

