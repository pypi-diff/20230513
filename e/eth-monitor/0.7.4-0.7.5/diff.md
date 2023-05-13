# Comparing `tmp/eth-monitor-0.7.4.tar.gz` & `tmp/eth-monitor-0.7.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eth-monitor-0.7.4.tar", last modified: Sat May 13 20:05:45 2023, max compression
+gzip compressed data, was "eth-monitor-0.7.5.tar", last modified: Sat May 13 20:45:28 2023, max compression
```

## Comparing `eth-monitor-0.7.4.tar` & `eth-monitor-0.7.5.tar`

### file list

```diff
@@ -1,61 +1,62 @@
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.299999 eth-monitor-0.7.4/
--rw-r--r--   0 lash      (1000) lash      (1000)     1513 2023-03-22 10:38:05.000000 eth-monitor-0.7.4/CHANGELOG
--rw-r--r--   0 lash      (1000) lash      (1000)    34523 2022-11-14 07:56:11.000000 eth-monitor-0.7.4/LICENSE
--rw-r--r--   0 lash      (1000) lash      (1000)      102 2023-05-13 20:03:31.000000 eth-monitor-0.7.4/MANIFEST.in
--rw-r--r--   0 lash      (1000) lash      (1000)      726 2023-05-13 20:05:45.299999 eth-monitor-0.7.4/PKG-INFO
--rw-r--r--   0 lash      (1000) lash      (1000)      871 2022-11-14 07:52:42.000000 eth-monitor-0.7.4/WAIVER
--rw-r--r--   0 lash      (1000) lash      (1000)     1634 2022-11-14 07:55:49.000000 eth-monitor-0.7.4/WAIVER.asc
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/
--rw-r--r--   0 lash      (1000) lash      (1000)      902 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/callback.py
--rw-r--r--   0 lash      (1000) lash      (1000)      524 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/chain.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/cli/
--rw-r--r--   0 lash      (1000) lash      (1000)       65 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/cli/__init__.py
--rw-r--r--   0 lash      (1000) lash      (1000)     3190 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/cli/arg.py
--rw-r--r--   0 lash      (1000) lash      (1000)     1923 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/cli/config.py
--rw-r--r--   0 lash      (1000) lash      (1000)      518 2022-11-14 07:56:11.000000 eth-monitor-0.7.4/eth_monitor/cli/log.py
--rw-r--r--   0 lash      (1000) lash      (1000)      271 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/cli/rules.py
--rw-r--r--   0 lash      (1000) lash      (1000)     1327 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/config.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/data/
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/data/config/
--rw-r--r--   0 lash      (1000) lash      (1000)       40 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/data/config/cache.ini
--rw-r--r--   0 lash      (1000) lash      (1000)       20 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/data/config/filter.ini
--rw-r--r--   0 lash      (1000) lash      (1000)      243 2022-10-13 07:08:18.000000 eth-monitor-0.7.4/eth_monitor/data/config/monitor.ini
--rw-r--r--   0 lash      (1000) lash      (1000)       22 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/data/config/renderer.ini
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/filters/
--rw-r--r--   0 lash      (1000) lash      (1000)       20 2022-01-30 14:12:19.000000 eth-monitor-0.7.4/eth_monitor/filters/__init__.py
--rw-r--r--   0 lash      (1000) lash      (1000)      580 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/filters/base.py
--rw-r--r--   0 lash      (1000) lash      (1000)      263 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/filters/block.py
--rw-r--r--   0 lash      (1000) lash      (1000)      732 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/filters/cache.py
--rw-r--r--   0 lash      (1000) lash      (1000)     2121 2023-02-23 02:16:57.000000 eth-monitor-0.7.4/eth_monitor/filters/out.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/importers/
--rw-r--r--   0 lash      (1000) lash      (1000)     1521 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/importers/etherscan.py
--rw-r--r--   0 lash      (1000) lash      (1000)     1450 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/index.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/mock/
--rw-r--r--   0 lash      (1000) lash      (1000)      274 2022-01-30 14:12:19.000000 eth-monitor-0.7.4/eth_monitor/mock/filter_plain.py
--rw-r--r--   0 lash      (1000) lash      (1000)      417 2022-01-30 14:12:19.000000 eth-monitor-0.7.4/eth_monitor/mock/filter_ruled.py
--rw-r--r--   0 lash      (1000) lash      (1000)     4240 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/rules.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor/runnable/
--rw-r--r--   0 lash      (1000) lash      (1000)     5735 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/runnable/import.py
--rw-r--r--   0 lash      (1000) lash      (1000)     3877 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/eth_monitor/runnable/list.py
--rw-r--r--   0 lash      (1000) lash      (1000)     3298 2023-02-26 19:39:52.000000 eth-monitor-0.7.4/eth_monitor/runnable/sync.py
--rw-r--r--   0 lash      (1000) lash      (1000)     5125 2022-01-30 14:12:19.000000 eth-monitor-0.7.4/eth_monitor/runnable/sync_thread_range.py
--rw-r--r--   0 lash      (1000) lash      (1000)    12626 2022-11-11 05:56:27.000000 eth-monitor-0.7.4/eth_monitor/settings.py
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/eth_monitor.egg-info/
--rw-r--r--   0 lash      (1000) lash      (1000)      726 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/PKG-INFO
--rw-r--r--   0 lash      (1000) lash      (1000)     1227 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/SOURCES.txt
--rw-r--r--   0 lash      (1000) lash      (1000)        1 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/dependency_links.txt
--rw-r--r--   0 lash      (1000) lash      (1000)      113 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/entry_points.txt
--rw-r--r--   0 lash      (1000) lash      (1000)      105 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/requires.txt
--rw-r--r--   0 lash      (1000) lash      (1000)       12 2023-05-13 20:05:45.000000 eth-monitor-0.7.4/eth_monitor.egg-info/top_level.txt
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.296666 eth-monitor-0.7.4/man/
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.299999 eth-monitor-0.7.4/man/build/
--rw-r--r--   0 lash      (1000) lash      (1000)     5946 2023-05-13 20:02:53.000000 eth-monitor-0.7.4/man/build/eth-monitor-import.1
--rw-r--r--   0 lash      (1000) lash      (1000)     5557 2023-05-13 20:02:53.000000 eth-monitor-0.7.4/man/build/eth-monitor-list.1
--rw-r--r--   0 lash      (1000) lash      (1000)    10183 2023-05-13 20:02:53.000000 eth-monitor-0.7.4/man/build/eth-monitor-sync.1
--rw-r--r--   0 lash      (1000) lash      (1000)    10183 2023-05-13 20:02:53.000000 eth-monitor-0.7.4/man/build/eth-monitor.1
--rw-r--r--   0 lash      (1000) lash      (1000)      105 2023-03-22 10:37:32.000000 eth-monitor-0.7.4/requirements.txt
--rw-r--r--   0 lash      (1000) lash      (1000)     1002 2023-05-13 20:05:45.299999 eth-monitor-0.7.4/setup.cfg
--rw-r--r--   0 lash      (1000) lash      (1000)      698 2023-05-13 20:02:13.000000 eth-monitor-0.7.4/setup.py
--rw-r--r--   0 lash      (1000) lash      (1000)       76 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/test_requirements.txt
-drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:05:45.299999 eth-monitor-0.7.4/tests/
--rw-r--r--   0 lash      (1000) lash      (1000)     3524 2022-04-20 19:19:25.000000 eth-monitor-0.7.4/tests/test_basic.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/
+-rw-r--r--   0 lash      (1000) lash      (1000)     1630 2023-05-13 20:44:55.000000 eth-monitor-0.7.5/CHANGELOG
+-rw-r--r--   0 lash      (1000) lash      (1000)    34523 2022-11-14 07:56:11.000000 eth-monitor-0.7.5/LICENSE
+-rw-r--r--   0 lash      (1000) lash      (1000)      110 2023-05-13 20:45:22.000000 eth-monitor-0.7.5/MANIFEST.in
+-rw-r--r--   0 lash      (1000) lash      (1000)    10473 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/PKG-INFO
+-rw-r--r--   0 lash      (1000) lash      (1000)     9706 2023-05-13 20:42:58.000000 eth-monitor-0.7.5/README.md
+-rw-r--r--   0 lash      (1000) lash      (1000)      871 2022-11-14 07:52:42.000000 eth-monitor-0.7.5/WAIVER
+-rw-r--r--   0 lash      (1000) lash      (1000)     1634 2022-11-14 07:55:49.000000 eth-monitor-0.7.5/WAIVER.asc
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/
+-rw-r--r--   0 lash      (1000) lash      (1000)      902 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/callback.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      524 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/chain.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/cli/
+-rw-r--r--   0 lash      (1000) lash      (1000)       65 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/cli/__init__.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     3190 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/cli/arg.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     1923 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/cli/config.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      518 2022-11-14 07:56:11.000000 eth-monitor-0.7.5/eth_monitor/cli/log.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      271 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/cli/rules.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     1327 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/config.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.139985 eth-monitor-0.7.5/eth_monitor/data/
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/data/config/
+-rw-r--r--   0 lash      (1000) lash      (1000)       40 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/data/config/cache.ini
+-rw-r--r--   0 lash      (1000) lash      (1000)       20 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/data/config/filter.ini
+-rw-r--r--   0 lash      (1000) lash      (1000)      243 2022-10-13 07:08:18.000000 eth-monitor-0.7.5/eth_monitor/data/config/monitor.ini
+-rw-r--r--   0 lash      (1000) lash      (1000)       22 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/data/config/renderer.ini
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/filters/
+-rw-r--r--   0 lash      (1000) lash      (1000)       20 2022-01-30 14:12:19.000000 eth-monitor-0.7.5/eth_monitor/filters/__init__.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      580 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/filters/base.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      263 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/filters/block.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      732 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/filters/cache.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     2121 2023-02-23 02:16:57.000000 eth-monitor-0.7.5/eth_monitor/filters/out.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/importers/
+-rw-r--r--   0 lash      (1000) lash      (1000)     1521 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/importers/etherscan.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     1450 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/index.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/mock/
+-rw-r--r--   0 lash      (1000) lash      (1000)      274 2022-01-30 14:12:19.000000 eth-monitor-0.7.5/eth_monitor/mock/filter_plain.py
+-rw-r--r--   0 lash      (1000) lash      (1000)      417 2022-01-30 14:12:19.000000 eth-monitor-0.7.5/eth_monitor/mock/filter_ruled.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     4240 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/rules.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor/runnable/
+-rw-r--r--   0 lash      (1000) lash      (1000)     5735 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/runnable/import.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     3877 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/eth_monitor/runnable/list.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     3298 2023-02-26 19:39:52.000000 eth-monitor-0.7.5/eth_monitor/runnable/sync.py
+-rw-r--r--   0 lash      (1000) lash      (1000)     5125 2022-01-30 14:12:19.000000 eth-monitor-0.7.5/eth_monitor/runnable/sync_thread_range.py
+-rw-r--r--   0 lash      (1000) lash      (1000)    12626 2022-11-11 05:56:27.000000 eth-monitor-0.7.5/eth_monitor/settings.py
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/eth_monitor.egg-info/
+-rw-r--r--   0 lash      (1000) lash      (1000)    10473 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/PKG-INFO
+-rw-r--r--   0 lash      (1000) lash      (1000)     1237 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/SOURCES.txt
+-rw-r--r--   0 lash      (1000) lash      (1000)        1 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/dependency_links.txt
+-rw-r--r--   0 lash      (1000) lash      (1000)      113 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/entry_points.txt
+-rw-r--r--   0 lash      (1000) lash      (1000)      105 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/requires.txt
+-rw-r--r--   0 lash      (1000) lash      (1000)       12 2023-05-13 20:45:28.000000 eth-monitor-0.7.5/eth_monitor.egg-info/top_level.txt
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.139985 eth-monitor-0.7.5/man/
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/man/build/
+-rw-r--r--   0 lash      (1000) lash      (1000)     5946 2023-05-13 20:02:53.000000 eth-monitor-0.7.5/man/build/eth-monitor-import.1
+-rw-r--r--   0 lash      (1000) lash      (1000)     5557 2023-05-13 20:02:53.000000 eth-monitor-0.7.5/man/build/eth-monitor-list.1
+-rw-r--r--   0 lash      (1000) lash      (1000)    10183 2023-05-13 20:02:53.000000 eth-monitor-0.7.5/man/build/eth-monitor-sync.1
+-rw-r--r--   0 lash      (1000) lash      (1000)    10183 2023-05-13 20:02:53.000000 eth-monitor-0.7.5/man/build/eth-monitor.1
+-rw-r--r--   0 lash      (1000) lash      (1000)      105 2023-03-22 10:37:32.000000 eth-monitor-0.7.5/requirements.txt
+-rw-r--r--   0 lash      (1000) lash      (1000)     1002 2023-05-13 20:45:28.146651 eth-monitor-0.7.5/setup.cfg
+-rw-r--r--   0 lash      (1000) lash      (1000)      852 2023-05-13 20:44:09.000000 eth-monitor-0.7.5/setup.py
+-rw-r--r--   0 lash      (1000) lash      (1000)       76 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/test_requirements.txt
+drwxr-xr-x   0 lash      (1000) lash      (1000)        0 2023-05-13 20:45:28.143318 eth-monitor-0.7.5/tests/
+-rw-r--r--   0 lash      (1000) lash      (1000)     3524 2022-04-20 19:19:25.000000 eth-monitor-0.7.5/tests/test_basic.py
```

### Comparing `eth-monitor-0.7.4/CHANGELOG` & `eth-monitor-0.7.5/CHANGELOG`

 * *Files 14% similar despite different names*

```diff
@@ -1,7 +1,12 @@
+- 0.7.5
+	* Add readme (from man page)
+	* Add package descriptino (from man page)
+- 0.7.4
+	* Add man pages to package
 - 0.7.3
 	* Upgrade deps
 - 0.7.2
 	* Fix tx index in default output for sync command
 - 0.7.1
 	* Change license to AGPL3 and copyright waived to public domain
 	* Add missing log module in cli lib
```

### Comparing `eth-monitor-0.7.4/LICENSE` & `eth-monitor-0.7.5/LICENSE`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/WAIVER` & `eth-monitor-0.7.5/WAIVER`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/WAIVER.asc` & `eth-monitor-0.7.5/WAIVER.asc`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/callback.py` & `eth-monitor-0.7.5/eth_monitor/callback.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/chain.py` & `eth-monitor-0.7.5/eth_monitor/chain.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/cli/arg.py` & `eth-monitor-0.7.5/eth_monitor/cli/arg.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/cli/config.py` & `eth-monitor-0.7.5/eth_monitor/cli/config.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/cli/log.py` & `eth-monitor-0.7.5/eth_monitor/cli/log.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/config.py` & `eth-monitor-0.7.5/eth_monitor/config.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/filters/base.py` & `eth-monitor-0.7.5/eth_monitor/filters/base.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/filters/cache.py` & `eth-monitor-0.7.5/eth_monitor/filters/cache.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/filters/out.py` & `eth-monitor-0.7.5/eth_monitor/filters/out.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/importers/etherscan.py` & `eth-monitor-0.7.5/eth_monitor/importers/etherscan.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/index.py` & `eth-monitor-0.7.5/eth_monitor/index.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/rules.py` & `eth-monitor-0.7.5/eth_monitor/rules.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/runnable/import.py` & `eth-monitor-0.7.5/eth_monitor/runnable/import.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/runnable/list.py` & `eth-monitor-0.7.5/eth_monitor/runnable/list.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/runnable/sync.py` & `eth-monitor-0.7.5/eth_monitor/runnable/sync.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/runnable/sync_thread_range.py` & `eth-monitor-0.7.5/eth_monitor/runnable/sync_thread_range.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor/settings.py` & `eth-monitor-0.7.5/eth_monitor/settings.py`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/eth_monitor.egg-info/SOURCES.txt` & `eth-monitor-0.7.5/eth_monitor.egg-info/SOURCES.txt`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 CHANGELOG
 LICENSE
 MANIFEST.in
+README.md
 WAIVER
 WAIVER.asc
 requirements.txt
 setup.cfg
 setup.py
 test_requirements.txt
 eth_monitor/callback.py
```

### Comparing `eth-monitor-0.7.4/man/build/eth-monitor-import.1` & `eth-monitor-0.7.5/man/build/eth-monitor-import.1`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/man/build/eth-monitor-list.1` & `eth-monitor-0.7.5/man/build/eth-monitor-list.1`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/man/build/eth-monitor-sync.1` & `eth-monitor-0.7.5/man/build/eth-monitor-sync.1`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/man/build/eth-monitor.1` & `eth-monitor-0.7.5/man/build/eth-monitor.1`

 * *Files identical despite different names*

### Comparing `eth-monitor-0.7.4/setup.cfg` & `eth-monitor-0.7.5/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = eth-monitor
-version = 0.7.4
+version = 0.7.5
 description = Monitor and cache transactions using match filters
 author = Louis Holbrook
 author_email = dev@holbrook.no
 url = https://git.defalsify.org/eth-monitor
 keywords = 
 	dlt
 	blockchain
```

### Comparing `eth-monitor-0.7.4/tests/test_basic.py` & `eth-monitor-0.7.5/tests/test_basic.py`

 * *Files identical despite different names*

