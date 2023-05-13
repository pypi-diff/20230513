# Comparing `tmp/autobean-0.1.3.tar.gz` & `tmp/autobean-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autobean-0.1.3.tar", last modified: Tue Apr 26 20:15:12 2022, max compression
+gzip compressed data, was "autobean-0.2.0.tar", last modified: Sat May 13 12:44:42 2023, max compression
```

## Comparing `autobean-0.1.3.tar` & `autobean-0.2.0.tar`

### file list

```diff
@@ -1,62 +1,63 @@
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.246589 autobean-0.1.3/
--rw-r--r--   0 seiarotg   (501) staff       (20)    18092 2019-09-03 05:14:19.000000 autobean-0.1.3/LICENSE
--rw-r--r--   0 seiarotg   (501) staff       (20)     2482 2022-04-26 20:15:12.246291 autobean-0.1.3/PKG-INFO
--rw-r--r--   0 seiarotg   (501) staff       (20)     1836 2021-01-03 13:47:48.000000 autobean-0.1.3/README.md
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.234913 autobean-0.1.3/autobean/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2021-01-02 21:42:25.000000 autobean-0.1.3/autobean/__init__.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.236527 autobean-0.1.3/autobean/include/
--rw-r--r--   0 seiarotg   (501) staff       (20)       67 2019-09-05 13:07:03.000000 autobean-0.1.3/autobean/include/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1950 2021-01-01 20:34:12.000000 autobean-0.1.3/autobean/include/plugin.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.236916 autobean-0.1.3/autobean/include/tests/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-09-05 14:56:04.000000 autobean-0.1.3/autobean/include/tests/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      784 2020-12-29 22:03:00.000000 autobean-0.1.3/autobean/include/tests/test_runner.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.237771 autobean-0.1.3/autobean/narration/
--rw-r--r--   0 seiarotg   (501) staff       (20)       69 2019-09-01 11:30:46.000000 autobean-0.1.3/autobean/narration/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      464 2022-04-26 19:47:16.000000 autobean-0.1.3/autobean/narration/comments.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1469 2021-01-04 22:32:34.000000 autobean-0.1.3/autobean/narration/plugin.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.238183 autobean-0.1.3/autobean/narration/tests/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-09-01 14:17:47.000000 autobean-0.1.3/autobean/narration/tests/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      187 2020-12-29 21:38:01.000000 autobean-0.1.3/autobean/narration/tests/test_runner.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.241799 autobean-0.1.3/autobean/share/
--rw-r--r--   0 seiarotg   (501) staff       (20)       65 2019-09-17 06:04:39.000000 autobean-0.1.3/autobean/share/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1669 2021-01-04 21:43:42.000000 autobean-0.1.3/autobean/share/fill_residuals.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     3875 2021-01-05 23:07:11.000000 autobean-0.1.3/autobean/share/include.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      140 2021-01-03 18:46:29.000000 autobean-0.1.3/autobean/share/include_context.py
--rw-r--r--   0 seiarotg   (501) staff       (20)    10034 2021-01-05 23:08:33.000000 autobean-0.1.3/autobean/share/link_accounts.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      994 2021-01-03 22:44:08.000000 autobean-0.1.3/autobean/share/map_residual_accounts.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1094 2021-01-04 16:19:17.000000 autobean-0.1.3/autobean/share/open_subaccounts.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1293 2021-01-05 23:06:21.000000 autobean-0.1.3/autobean/share/plugin.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      223 2021-01-03 15:27:51.000000 autobean-0.1.3/autobean/share/policy.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     1722 2021-05-08 10:42:03.000000 autobean-0.1.3/autobean/share/select_viewpoint.py
--rw-r--r--   0 seiarotg   (501) staff       (20)    13665 2021-01-05 23:08:51.000000 autobean-0.1.3/autobean/share/split_postings.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.242205 autobean-0.1.3/autobean/share/tests/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.1.3/autobean/share/tests/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      183 2020-12-29 21:38:01.000000 autobean-0.1.3/autobean/share/tests/test_runner.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     2906 2021-01-04 21:43:42.000000 autobean-0.1.3/autobean/share/utils.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.242757 autobean-0.1.3/autobean/sorted/
--rw-r--r--   0 seiarotg   (501) staff       (20)       66 2021-01-01 19:45:48.000000 autobean-0.1.3/autobean/sorted/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     3784 2021-04-11 13:51:16.000000 autobean-0.1.3/autobean/sorted/plugin.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.243220 autobean-0.1.3/autobean/truelayer/
--rw-r--r--   0 seiarotg   (501) staff       (20)       49 2020-12-29 22:03:00.000000 autobean-0.1.3/autobean/truelayer/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)    16844 2022-04-26 20:02:55.000000 autobean-0.1.3/autobean/truelayer/importer.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.244936 autobean-0.1.3/autobean/utils/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.1.3/autobean/utils/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      886 2020-12-29 22:09:39.000000 autobean-0.1.3/autobean/utils/compare.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     5397 2021-10-09 19:22:21.000000 autobean-0.1.3/autobean/utils/deduplicate.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      645 2021-01-03 15:27:51.000000 autobean-0.1.3/autobean/utils/error_logger.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      519 2019-09-07 15:44:04.000000 autobean-0.1.3/autobean/utils/plugin_base.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     5818 2021-01-04 16:24:06.000000 autobean-0.1.3/autobean/utils/plugin_test_utils.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.245448 autobean-0.1.3/autobean/xcheck/
--rw-r--r--   0 seiarotg   (501) staff       (20)       66 2019-08-10 06:00:31.000000 autobean-0.1.3/autobean/xcheck/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)     5391 2021-01-05 23:08:23.000000 autobean-0.1.3/autobean/xcheck/plugin.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.245932 autobean-0.1.3/autobean/xcheck/tests/
--rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.1.3/autobean/xcheck/tests/__init__.py
--rw-r--r--   0 seiarotg   (501) staff       (20)      786 2020-12-29 22:03:00.000000 autobean-0.1.3/autobean/xcheck/tests/test_runner.py
-drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2022-04-26 20:15:12.236085 autobean-0.1.3/autobean.egg-info/
--rw-r--r--   0 seiarotg   (501) staff       (20)     2482 2022-04-26 20:15:11.000000 autobean-0.1.3/autobean.egg-info/PKG-INFO
--rw-r--r--   0 seiarotg   (501) staff       (20)     1362 2022-04-26 20:15:12.000000 autobean-0.1.3/autobean.egg-info/SOURCES.txt
--rw-r--r--   0 seiarotg   (501) staff       (20)        1 2022-04-26 20:15:11.000000 autobean-0.1.3/autobean.egg-info/dependency_links.txt
--rw-r--r--   0 seiarotg   (501) staff       (20)       68 2022-04-26 20:15:12.000000 autobean-0.1.3/autobean.egg-info/requires.txt
--rw-r--r--   0 seiarotg   (501) staff       (20)        9 2022-04-26 20:15:12.000000 autobean-0.1.3/autobean.egg-info/top_level.txt
--rw-r--r--   0 seiarotg   (501) staff       (20)       38 2022-04-26 20:15:12.246726 autobean-0.1.3/setup.cfg
--rw-r--r--   0 seiarotg   (501) staff       (20)      958 2022-04-26 20:13:11.000000 autobean-0.1.3/setup.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.354304 autobean-0.2.0/
+-rw-r--r--   0 seiarotg   (501) staff       (20)    18092 2019-09-03 05:14:19.000000 autobean-0.2.0/LICENSE
+-rw-r--r--   0 seiarotg   (501) staff       (20)     2311 2023-05-13 12:44:42.353918 autobean-0.2.0/PKG-INFO
+-rw-r--r--   0 seiarotg   (501) staff       (20)     1701 2023-05-13 12:32:14.000000 autobean-0.2.0/README.md
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.334193 autobean-0.2.0/autobean/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2021-01-02 21:42:25.000000 autobean-0.2.0/autobean/__init__.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.337187 autobean-0.2.0/autobean/include/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       88 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/include/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     1028 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/include/plugin.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.337991 autobean-0.2.0/autobean/include/tests/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-09-05 14:56:04.000000 autobean-0.2.0/autobean/include/tests/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      869 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/include/tests/test_runner.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.339407 autobean-0.2.0/autobean/narration/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       69 2019-09-01 11:30:46.000000 autobean-0.2.0/autobean/narration/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      464 2022-06-11 14:47:44.000000 autobean-0.2.0/autobean/narration/comments.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     1458 2022-06-11 14:47:44.000000 autobean-0.2.0/autobean/narration/plugin.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.340221 autobean-0.2.0/autobean/narration/tests/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-09-01 14:17:47.000000 autobean-0.2.0/autobean/narration/tests/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      195 2022-06-11 14:47:44.000000 autobean-0.2.0/autobean/narration/tests/test_runner.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.344420 autobean-0.2.0/autobean/share/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       59 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     3340 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/include.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      826 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/include_context.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     8890 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/link_accounts.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     9345 2023-01-29 01:59:08.000000 autobean-0.2.0/autobean/share/plugin.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)    10792 2023-01-29 03:37:02.000000 autobean-0.2.0/autobean/share/policy_lib.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)    23168 2023-01-29 03:38:18.000000 autobean-0.2.0/autobean/share/policy_lib_test.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)    21459 2023-01-29 01:59:21.000000 autobean-0.2.0/autobean/share/split_account.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.345327 autobean-0.2.0/autobean/share/tests/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.2.0/autobean/share/tests/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      358 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/tests/test_runner.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      125 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/share/viewpoint_lib.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.346379 autobean-0.2.0/autobean/sorted/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       66 2021-01-01 19:45:48.000000 autobean-0.2.0/autobean/sorted/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     3836 2022-12-19 14:01:53.000000 autobean-0.2.0/autobean/sorted/plugin.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.347817 autobean-0.2.0/autobean/stock_split/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       58 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/stock_split/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     3057 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/stock_split/plugin.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     4040 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/stock_split/plugin_test.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.348733 autobean-0.2.0/autobean/truelayer/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       49 2020-12-29 22:03:00.000000 autobean-0.2.0/autobean/truelayer/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)    17780 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/truelayer/importer.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.351622 autobean-0.2.0/autobean/utils/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.2.0/autobean/utils/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      953 2022-06-11 14:47:44.000000 autobean-0.2.0/autobean/utils/compare.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     5637 2023-01-02 23:04:05.000000 autobean-0.2.0/autobean/utils/deduplicate.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     1124 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/utils/error_lib.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     7686 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/utils/plugin_lib.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     9373 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/utils/plugin_test_utils.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.352534 autobean-0.2.0/autobean/xcheck/
+-rw-r--r--   0 seiarotg   (501) staff       (20)       93 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/xcheck/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)     4205 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/xcheck/plugin.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.353361 autobean-0.2.0/autobean/xcheck/tests/
+-rw-r--r--   0 seiarotg   (501) staff       (20)        0 2019-08-10 06:00:31.000000 autobean-0.2.0/autobean/xcheck/tests/__init__.py
+-rw-r--r--   0 seiarotg   (501) staff       (20)      868 2023-01-29 01:35:33.000000 autobean-0.2.0/autobean/xcheck/tests/test_runner.py
+drwxr-xr-x   0 seiarotg   (501) staff       (20)        0 2023-05-13 12:44:42.336339 autobean-0.2.0/autobean.egg-info/
+-rw-r--r--   0 seiarotg   (501) staff       (20)     2311 2023-05-13 12:44:42.000000 autobean-0.2.0/autobean.egg-info/PKG-INFO
+-rw-r--r--   0 seiarotg   (501) staff       (20)     1360 2023-05-13 12:44:42.000000 autobean-0.2.0/autobean.egg-info/SOURCES.txt
+-rw-r--r--   0 seiarotg   (501) staff       (20)        1 2023-05-13 12:44:42.000000 autobean-0.2.0/autobean.egg-info/dependency_links.txt
+-rw-r--r--   0 seiarotg   (501) staff       (20)       47 2023-05-13 12:44:42.000000 autobean-0.2.0/autobean.egg-info/requires.txt
+-rw-r--r--   0 seiarotg   (501) staff       (20)        9 2023-05-13 12:44:42.000000 autobean-0.2.0/autobean.egg-info/top_level.txt
+-rw-r--r--   0 seiarotg   (501) staff       (20)       38 2023-05-13 12:44:42.354410 autobean-0.2.0/setup.cfg
+-rw-r--r--   0 seiarotg   (501) staff       (20)      959 2023-05-13 12:31:37.000000 autobean-0.2.0/setup.py
```

### Comparing `autobean-0.1.3/LICENSE` & `autobean-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `autobean-0.1.3/PKG-INFO` & `autobean-0.2.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,46 +1,41 @@
 Metadata-Version: 2.1
 Name: autobean
-Version: 0.1.3
+Version: 0.2.0
 Summary: A collection of plugins and scripts that help automating bookkeeping with beancount
 Home-page: https://github.com/SEIAROTg/autobean
 Author: SEIAROTg
 Author-email: seiarotg@gmail.com
-License: UNKNOWN
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v2 (GPLv2)
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Office/Business :: Financial :: Accounting
-Requires-Python: >=3.8
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # autobean
-
-[![travis](https://travis-ci.com/SEIAROTg/autobean.svg)](https://travis-ci.com/SEIAROTg/autobean)
+[![CircleCI](https://circleci.com/gh/SEIAROTg/autobean.svg?style=shield)](https://circleci.com/gh/SEIAROTg/autobean)
 [![pypi](https://img.shields.io/pypi/v/autobean)](https://pypi.org/project/autobean/)
 [![codecov](https://codecov.io/gh/SEIAROTg/autobean/branch/master/graph/badge.svg)](https://codecov.io/gh/SEIAROTg/autobean)
-[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/SEIAROTg/autobean.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/SEIAROTg/autobean/context:python)
 [![Maintainability](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/maintainability)](https://codeclimate.com/github/SEIAROTg/autobean/maintainability)
 [![Test Coverage](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/test_coverage)](https://codeclimate.com/github/SEIAROTg/autobean/test_coverage)
 [![license](https://img.shields.io/github/license/SEIAROTg/autobean.svg)](https://github.com/SEIAROTg/autobean)
 
 A collection of plugins and scripts that help automating bookkeeping with [beancount](http://furius.ca/beancount/).
 
 ## Components
 
-* [autobean.share](autobean/share): Manages shared accounts / transactions / postings with simple annotations and reuses joint ledgers among multiple parties.
+* [autobean.share](autobean/share): expense split, joint bookkeeping, and debt management for personal use cases.
 * [autobean.xcheck](autobean/xcheck): Cross-checks against external ledgers.
 * [autobean.narration](autobean/narration): Generates transaction narration from posting narration and posting narration from comments.
 * [autobean.include](autobean/include): Includes external beancount ledgers without disabling their plugins.
-* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), an bank API aggregator.
+* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), a bank API aggregator.
 * [autobean.sorted](autobean/sorted): Checks that transactions are in non-descending order in each file.
+* [autobean.stock_split](autobean/stock_split): Simplifies stock split.
 
 ## Install
 
 ```sh
 pip install autobean
 ```
-
-
```

### Comparing `autobean-0.1.3/README.md` & `autobean-0.2.0/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,26 +1,25 @@
 # autobean
-
-[![travis](https://travis-ci.com/SEIAROTg/autobean.svg)](https://travis-ci.com/SEIAROTg/autobean)
+[![CircleCI](https://circleci.com/gh/SEIAROTg/autobean.svg?style=shield)](https://circleci.com/gh/SEIAROTg/autobean)
 [![pypi](https://img.shields.io/pypi/v/autobean)](https://pypi.org/project/autobean/)
 [![codecov](https://codecov.io/gh/SEIAROTg/autobean/branch/master/graph/badge.svg)](https://codecov.io/gh/SEIAROTg/autobean)
-[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/SEIAROTg/autobean.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/SEIAROTg/autobean/context:python)
 [![Maintainability](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/maintainability)](https://codeclimate.com/github/SEIAROTg/autobean/maintainability)
 [![Test Coverage](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/test_coverage)](https://codeclimate.com/github/SEIAROTg/autobean/test_coverage)
 [![license](https://img.shields.io/github/license/SEIAROTg/autobean.svg)](https://github.com/SEIAROTg/autobean)
 
 A collection of plugins and scripts that help automating bookkeeping with [beancount](http://furius.ca/beancount/).
 
 ## Components
 
-* [autobean.share](autobean/share): Manages shared accounts / transactions / postings with simple annotations and reuses joint ledgers among multiple parties.
+* [autobean.share](autobean/share): expense split, joint bookkeeping, and debt management for personal use cases.
 * [autobean.xcheck](autobean/xcheck): Cross-checks against external ledgers.
 * [autobean.narration](autobean/narration): Generates transaction narration from posting narration and posting narration from comments.
 * [autobean.include](autobean/include): Includes external beancount ledgers without disabling their plugins.
-* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), an bank API aggregator.
+* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), a bank API aggregator.
 * [autobean.sorted](autobean/sorted): Checks that transactions are in non-descending order in each file.
+* [autobean.stock_split](autobean/stock_split): Simplifies stock split.
 
 ## Install
 
 ```sh
 pip install autobean
 ```
```

### Comparing `autobean-0.1.3/autobean/narration/plugin.py` & `autobean-0.2.0/autobean/narration/plugin.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,36 +1,37 @@
-from typing import List, Dict, Tuple, Set
+from typing import Any
 from beancount.core.data import Directive, Transaction
 from autobean.narration import comments
 
 
-def plugin(entries: List[Directive], options: Dict) -> Tuple[List[Directive], List]:
+def plugin(entries: list[Directive], options: dict[str, Any]) -> tuple[list[Directive], list]:
     filenames = collect_transaction_filenames(entries)
     comment_narrations = {
         filename: comments.extract_from_file(filename)
         for filename in filenames
     }
     return [merge_narration(entry, comment_narrations) for entry in entries], []
 
 
-def collect_transaction_filenames(entries: List[Directive]) -> Set[str]:
-    return set(
+def collect_transaction_filenames(entries: list[Directive]) -> set[str]:
+    return {
         entry.meta['filename']
         for entry in entries
-        if isinstance(entry, Transaction) and 'filename' in entry.meta)
+        if isinstance(entry, Transaction) and 'filename' in entry.meta
+    }
 
 
-def merge_narration(entry: Directive, comment_narrations: Dict[str, Dict[int, str]]) -> Directive:
+def merge_narration(entry: Directive, comment_narrations: dict[str, dict[int, str]]) -> Directive:
     if not isinstance(entry, Transaction):
         return entry
     narrations = []
     for posting in entry.postings:
         if posting.meta:
             narration = posting.meta.get('narration')
-            comment_narration = comment_narrations.get(posting.meta.get('filename')).get(posting.meta.get('lineno'))
+            comment_narration = comment_narrations[posting.meta.get('filename')].get(posting.meta.get('lineno'))
             if narration is None and comment_narration:
                 posting.meta['narration'] = comment_narration
                 narration = comment_narration
             if narration:
                 narrations.append(narration.strip())
     if entry.narration:
         return entry
```

### Comparing `autobean-0.1.3/autobean/share/link_accounts.py` & `autobean-0.2.0/autobean/share/link_accounts.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,117 +1,85 @@
-from dataclasses import dataclass
-from collections import namedtuple, defaultdict, deque, Counter
-from datetime import timedelta
-from decimal import Decimal
-import functools
-from typing import Dict, List, Iterable, Tuple, Optional
+import collections
+import dataclasses
+import datetime
+import decimal
+import re
+from typing import Any, Iterable, Optional
 from beancount.core import amount
-from beancount.core.data import Directive, Transaction, Custom, filter_txns, iter_entry_dates
-from beancount.core.account import TYPE as ACCOUNT_TYPE
-from autobean.utils.error_logger import ErrorLogger
-from autobean.share import utils
+from beancount.core.data import Custom, Directive, Transaction, filter_txns, iter_entry_dates
+from autobean.utils import error_lib
 
 
-InvalidDirectiveError = namedtuple('InvalidDirectiveError', 'source message entry')
-UnresolvedLinkError = namedtuple('UnresolvedLinkError', 'source message entry')
+_MAIN_ACCOUNT_REGEX = re.compile(r':\[.*\]$')
 
 
-@dataclass(repr=False, frozen=True)
+@dataclasses.dataclass(frozen=True)
 class Link:
-    directive: Custom
+    path: str
+    account: str
+    complement_path: str
+    complement_account: str
+    custom: Custom
 
-    @functools.cached_property
-    def _values(self) -> Tuple[str, str, str, str]:
-        return tuple(v.value for v in self.directive.values)
-
-    @property
-    def filename(self) -> str:
-        return self._values[0]
-
-    @property
-    def account(self) -> str:
-        return self._values[1]
-    
-    @property
-    def complement_filename(self) -> str:
-        return self._values[2]
-    
-    @property
-    def complement_account(self) -> str:
-        return self._values[3]
-
-    def __repr__(self) -> str:
-        return str(self._values)
-    
-    def valid(self) -> bool:
-        if len(self.directive.values) != 4:
-            return False
-        if (tuple(v.dtype for v in self.directive.values) !=
-                (str, ACCOUNT_TYPE, str, ACCOUNT_TYPE)):
-            return False
-        return True
+
+class UnresolvedLinkError(error_lib.Error):
+    pass
 
 
 def link_accounts(
-        entries_by_file: Dict[str, List[Directive]],
+        entries_by_file: dict[str, list[Directive]],
         links: Iterable[Link],
-        logger: ErrorLogger) -> List[Directive]:
+        logger: error_lib.ErrorLogger) -> list[Directive]:
 
     _check_links(entries_by_file, links, logger)
     edges = _build_graph(entries_by_file, links, logger)
     return _resolve_links(entries_by_file, edges, logger)
 
 
+def _main_account(account: str) -> str:
+    return re.sub(_MAIN_ACCOUNT_REGEX, '', account)
+
+
 def _check_links(
-        entries_by_file: Dict[str, List[Directive]],
+        entries_by_file: dict[str, list[Directive]],
         links: Iterable[Link],
-        logger: ErrorLogger):
+        logger: error_lib.ErrorLogger) -> None:
     all_endpoints = set()
     for link in links:
-        if not link.valid():
-            logger.log_error(InvalidDirectiveError(
-                link.directive.meta,
-                'autobean.share.link expects {filename} {account} '
-                '{complement filename} {complement account} as arguments',
-                link.directive,
-            ))
-            continue
         endpoints = [
-            (link.filename, link.account),
-            (link.complement_filename, link.complement_account),
+            (link.path, link.account),
+            (link.complement_path, link.complement_account),
         ]
         for ep in endpoints:
             if ep in all_endpoints:
-                logger.log_error(InvalidDirectiveError(
-                    link.directive.meta,
+                logger.log_error(error_lib.InvalidDirectiveError(
+                    link.custom.meta,
                     f'Account {ep[1]} in {ep[0]} has multiple links',
-                    link.directive,
+                    link.custom,
                 ))
             if ep[0] not in entries_by_file:
-                logger.log_error(InvalidDirectiveError(
-                    link.directive.meta,
+                logger.log_error(error_lib.InvalidDirectiveError(
+                    link.custom.meta,
                     f'Ledger {ep[0]} was not included with '
                     f'"autobean.share.include" from this ledger',
-                    link.directive,
+                    link.custom,
                 ))
             all_endpoints.add(ep)
 
 
 def _build_graph(
-        entries_by_file: Dict[str, List[Directive]],
+        entries_by_file: dict[str, list[Directive]],
         links: Iterable[Link],
-        logger: ErrorLogger) -> Dict[int, List[Tuple[Transaction, str]]]:
+        logger: error_lib.ErrorLogger) -> dict[int, list[tuple[Transaction, str]]]:
 
-    day = timedelta(days=1)
-    edges = defaultdict(list) # id(txn) -> [(complement txn, account)]
+    day = datetime.timedelta(days=1)
+    edges = collections.defaultdict(list) # id(txn) -> [(complement txn, account)]
     for link in links:
-        if not link.valid():
-            continue
-        entries = entries_by_file.get(link.filename, [])
-        complement_entries = entries_by_file.get(link.complement_filename, [])
+        entries = entries_by_file.get(link.path, [])
+        complement_entries = entries_by_file.get(link.complement_path, [])
 
         for entry in filter_txns(entries):
             expected_complement_feature = _transaction_feature(
                 entry, link.account, True)
             if not expected_complement_feature[1]:
                 continue
             # find complement txn and check duplicated complement
@@ -171,29 +139,30 @@
                     complement_txn,
                 ))
 
     return edges
 
 
 def _resolve_links(
-        entries_by_file: Dict[str, List[Directive]],
-        edges: Dict[int, List[Tuple[Transaction, str]]],
-        logger: ErrorLogger) -> List[Directive]:
+        entries_by_file: dict[str, list[Directive]],
+        edges: dict[int, list[tuple[Transaction, str]]],
+        logger: error_lib.ErrorLogger,
+) -> list[Directive]:
     ret = []
     all_visited = set()
     bad = set()
     for entries in entries_by_file.values():
         for entry in entries:
             if id(entry) in all_visited:
                 continue
             if id(entry) not in edges or id(entry) in bad:
                 ret.append(entry)
                 continue
 
-            q = deque([entry])
+            q = collections.deque([entry])
             visited = set()
             txns = []
             while q:
                 u = q.popleft()
                 if id(u) in visited:
                     continue
                 visited.add(id(u))
@@ -209,40 +178,42 @@
                 bad.update(visited)
     return ret
 
 
 def _transaction_feature(
         entry: Transaction,
         account: str,
-        negated: bool) -> Tuple[Optional[str], Counter]:
+        negated: bool,
+) -> tuple[Optional[str], collections.Counter]:
     link_key = entry.meta.get('share_link_key', None)
 
     posting_features = []
     for posting in entry.postings:
-        if utils.main_account(posting.account) != account:
+        if _main_account(posting.account) != account:
             continue
         if negated:
-            units = amount.mul(posting.units, Decimal(-1))
+            units = amount.mul(posting.units, decimal.Decimal(-1))
         else:
             units = posting.units
         posting_features.append(units)
-    return link_key, Counter(posting_features)
+    return link_key, collections.Counter(posting_features)
 
 
 def merge_transactions(
-        txns: List[Transaction],
-        edges: Dict[int, Tuple[Transaction, str]],
-        logger: ErrorLogger) -> Optional[Transaction]:
+        txns: list[Transaction],
+        edges: dict[int, list[tuple[Transaction, str]]],
+        logger: error_lib.ErrorLogger,
+) -> Optional[Transaction]:
     date = None
     flag = None
     payee = None
     narration = ''
-    tags = set()
-    links = set()
-    meta = {}
+    tags = set[str]()
+    links = set[str]()
+    meta = dict[str, Any]()
     postings = []
     compatible = True
     last_txn = None
     for txn in txns:
         last_txn = txn
         if date and txn.date and txn.date != date:
             compatible = False
@@ -253,27 +224,27 @@
         if payee and txn.payee and txn.payee != payee:
             compatible = False
         payee = payee or txn.payee
         if narration and txn.narration and txn.narration != narration:
             compatible = False
         narration = narration or txn.narration
         for k, v in txn.meta.items():
-            mv = meta.get(k, None)
+            mv = meta.get(k)
             meta[k] = mv or v
             if mv and mv != v and k not in ('filename', 'lineno'):
                 compatible = False
                 break
         if not compatible:
             break
         accounts_to_remove = set(edge[1] for edge in edges[id(txn)])
         for posting in txn.postings:
-            if utils.main_account(posting.account) not in accounts_to_remove:
+            if _main_account(posting.account) not in accounts_to_remove:
                 postings.append(posting)
 
-    if not compatible:
+    if not compatible and last_txn:
         logger.log_error(UnresolvedLinkError(
             last_txn.meta,
             'Transaction and its complement do not agree on flag, payee, '
             'narration or meta',
             last_txn,
         ))
         return None
```

### Comparing `autobean-0.1.3/autobean/sorted/plugin.py` & `autobean-0.2.0/autobean/sorted/plugin.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,31 +1,32 @@
-from collections import defaultdict, namedtuple
-from typing import List, Dict, Tuple, Any
+from typing import Any
+from collections import defaultdict
 from beancount.core.data import Directive, Custom
+from autobean.utils import error_lib
 
 
-InvalidDirectiveError = namedtuple('OutOfOrderDirectiveError', 'source message entry')
-OutOfOrderDirectiveError = namedtuple('OutOfOrderDirectiveError', 'source message entry')
+class OutOfOrderDirectiveError(error_lib.Error):
+    pass
 
 
-def plugin(entries: List[Directive], options: Dict) -> Tuple[List[Directive], List[Any]]:
-    entries_by_file = defaultdict(list)
-    ignored_files = set()
-    errors = []
+def plugin(entries: list[Directive], options: dict[str, Any]) -> tuple[list[Directive], list[error_lib.Error]]:
+    entries_by_file: defaultdict[str | None, list[Directive]] = defaultdict(list)
+    ignored_files: set[str] = set()
+    errors: list[error_lib.Error] = []
     for entry in entries:
         # Plugin-generated entries may not have associated file or line number.
         # We ignore entries in either case.
         if (hasattr(entry, 'date') and
                 hasattr(entry, 'meta') and
                 entry.meta.get('filename', None) and
                 entry.meta.get('lineno', None)):
             should_append = True
             if is_enabling_directive(entry):
                 if len(entry.values) != 1 or entry.values[0].dtype != bool:
-                    errors.append(InvalidDirectiveError(
+                    errors.append(error_lib.InvalidDirectiveError(
                         entry.meta,
                         'autobean.sorted.enabled directive accepts a single '
                         'boolean argument',
                         entry))
                     should_append = False
             if should_append:
                 entries_by_file[entry.meta['filename']].append(entry)
@@ -38,29 +39,29 @@
     return entries, errors
     
 
 def is_enabling_directive(entry: Directive) -> bool:
     return isinstance(entry, Custom) and entry.type == 'autobean.sorted.enabled'
 
 
-def check_file_entries(entries: List[Directive]) -> List[Any]:
+def check_file_entries(entries: list[Directive]) -> list[error_lib.Error]:
     """Checks entries are in order and finds out-of-order entries.
 
     We find a longest non-descending subsequence and assumes all other
     entries are out-of-order.
 
     When finding the longest non-descending subsequence, we prefer the one
     whose maximum date is minimal. For example, in time sequence 1 2 100 3
     it's more likely that 1 2 3 is correct and 100 is a mistake (compared to
     1 2 100 as correct and 3 as mistake).
     """
 
     prevs = []
     # [(length, -maxdate)]
-    scores = []
+    scores: list[tuple[int, int]] = []
 
     sorted_entries = []
     enabled = True
     for entry in sorted(entries, key=lambda e: e.meta['lineno']):
         if is_enabling_directive(entry):
             enabled = entry.values[0].value
             continue
@@ -90,15 +91,15 @@
     i = len(prevs) - 1
     while i >= 0:
         j = prevs[i]
         for k in range(i - 1, j, -1):
             misplaced_entries.append(sorted_entries[k])
         i = j
 
-    errors = []
+    errors: list[error_lib.Error] = []
     for misplaced_entry in misplaced_entries[::-1]:
         errors.append(OutOfOrderDirectiveError(
             misplaced_entry.meta,
             'Directive date does not follow non-descending order within the '
             'file',
             misplaced_entry))
```

### Comparing `autobean-0.1.3/autobean/truelayer/importer.py` & `autobean-0.2.0/autobean/truelayer/importer.py`

 * *Files 8% similar despite different names*

```diff
@@ -3,105 +3,109 @@
 import http.server
 import logging
 import os
 import re
 import time
 import secrets
 import sys
-from typing import Text, List, Dict, Any
+from typing import Any, Optional
 import urllib.parse
 import webbrowser
 
 from autobean.utils import deduplicate
 from beancount.core.amount import Amount
 from beancount.core.data import Transaction, Posting, Balance, Directive, new_metadata
 from beancount.core import inventory
 from beancount.ingest import importer
+from beancount.ingest import cache
 import dateutil.parser
 import requests
 import yaml
 
 
 CONFIG_SUFFIX = '.truelayer.yaml'
 ACCOUNT_TYPES = ('accounts', 'cards')
 
 
-def escape_account_component(s: Text) -> Text:
+def escape_account_component(s: str) -> str:
     s = re.sub(r'\W', '', s)
     s = s[:1].upper() + s[1:]
     return s
 
 
-def format_iso_datetime(timestamp_s: float) -> Text:
+def format_iso_datetime(timestamp_s: float) -> str:
     return datetime.datetime.utcfromtimestamp(int(timestamp_s)).isoformat()
 
 
 def currency_to_decimal(currency: float) -> Decimal:
     return Decimal(f'{currency:.2f}')
 
 
 class Importer(importer.ImporterProtocol):
 
-    def __init__(self, client_id: Text, client_secret: Text):
+    def __init__(self, client_id: str, client_secret: str):
         self._client_id = client_id
         self._client_secret = client_secret
 
-    def name(self):
+    def name(self) -> str:
         return 'autobean.truelayer'
 
-    def identify(self, file):
+    def identify(self, file: cache._FileMemo) -> bool:
         return file.name.endswith(CONFIG_SUFFIX)
 
-    def extract(self, file, existing_entries=None):
+    def extract(self, file: cache._FileMemo, existing_entries: Optional[list[Directive]] = None) -> list[Directive]:
         config = _Config(self._client_id, self._client_secret, file)
         extractor = _Extractor(config)
         return extractor.extract(existing_entries)
 
 
 class _Config:
-    def __init__(self, client_id, client_secret, file):
+    def __init__(self, client_id: str, client_secret: str, file: cache._FileMemo):
         self.client_id = client_id
         self.client_secret = client_secret
         self.data = yaml.safe_load(file.contents()) or {}
         self._filename = file.name
 
     @property
-    def name(self):
+    def name(self) -> str:
         return os.path.basename(self._filename).rsplit(CONFIG_SUFFIX, 1)[0]
 
-    def dump(self):
+    def dump(self) -> None:
         with open(self._filename, 'w') as f:
             yaml.safe_dump(self.data, f)
 
 
 class _Extractor:
     def __init__(self, config: _Config):
         self._config = config
         self._oauth_manager = _OAuthManager(config)
 
-    def extract(self, existing_entries=None):
+    def extract(self, existing_entries: Optional[list[Directive]] = None) -> list[Directive]:
         for type_ in ACCOUNT_TYPES:
             self._update_accounts(type_)
         entries = self._fetch_all_transactions()
         if existing_entries:
             entries = deduplicate.deduplicate(entries, existing_entries)
         return entries
 
     @property
-    def _auth_headers(self):
+    def _auth_headers(self) -> dict[str, str]:
         return {
             'Authorization': f'Bearer {self._oauth_manager.access_token}'
         }
 
-    def _update_accounts(self, type_: Text):
+    def _update_accounts(self, type_: str) -> None:
         url = {
             'accounts': 'https://api.truelayer.com/data/v1/accounts',
             'cards': 'https://api.truelayer.com/data/v1/cards',
         }
         r = requests.get(url[type_], headers=self._auth_headers)
+        if not r.ok:
+            logging.warning('Could not fetch %s: %s', type_, r.text)
+            return
         accounts = r.json().get('results', [])
         config_accounts = self._config.data.setdefault(type_, {})
         for account in accounts:
             config_account = config_accounts.setdefault(
                 account['account_id'], {})
             config_account.setdefault('name', account['display_name'])
             config_account.setdefault(
@@ -115,18 +119,18 @@
             ]))
             config_account.setdefault('from', int(time.time()) - 86400 * 90)
 
         self._config.dump()
 
     def _fetch_transactions(
             self,
-            account_id: Text,
-            account,
-            type_: Text,
-            is_pending: bool) -> List[Dict[Any, Any]]:
+            account_id: str,
+            account: dict[str, Any],
+            type_: str,
+            is_pending: bool) -> list[dict[str, Any]]:
         url = {
             ('accounts', False): (
                 f'https://api.truelayer.com/data/v1/accounts/{account_id}/transactions'),
             ('accounts', True): (
                 f'https://api.truelayer.com/data/v1/accounts/{account_id}/transactions/pending'),
             ('cards', False): (
                 f'https://api.truelayer.com/data/v1/cards/{account_id}/transactions'),
@@ -141,41 +145,47 @@
             url[(type_, is_pending)],
             headers=self._auth_headers,
             params={
                 'from': format_iso_datetime(account['from']),
                 'to': format_iso_datetime(time.time()),
             }
         )
+        if not r.ok:
+            logging.error('Error fetching transactions: %s', r.text)
+            r.raise_for_status()
         txns = r.json().get('results', [])
         logging.info(
             f'Fetched {len(txns)} {log_transaction} for account '
             f'{account["name"]} ({account_id}).')
         return txns
 
     def _fetch_balances(
             self,
-            account_id: Text,
-            account,
-            type_: Text) -> List[Dict[Any, Any]]:
+            account_id: str,
+            account: dict[str, Any],
+            type_: str) -> list[dict[str, Any]]:
         url = {
             'accounts': f'https://api.truelayer.com/data/v1/accounts/{account_id}/balance',
             'cards': f'https://api.truelayer.com/data/v1/cards/{account_id}/balance',
         }
         logging.info(
             f'Fetching balance for account {account["name"]} ({account_id}).')
         r = requests.get(url[type_], headers=self._auth_headers)
+        if not r.ok:
+            logging.error('Error fetching balance: %s', r.text)
+            r.raise_for_status()
         balances = r.json().get('results', [])
         logging.info(
             f'Fetched {len(balances)} balance entries for account '
             f'{account["name"]} ({account_id}).')
         return balances
 
 
-    def _fetch_all_transactions(self) -> List[Directive]:
-        entries = []
+    def _fetch_all_transactions(self) -> list[Directive]:
+        entries: list[Directive] = []
         for type_ in ACCOUNT_TYPES:
             for account_id, account in self._config.data[type_].items():
                 if not account['enabled']:
                     continue
                 truelayer_txns = self._fetch_transactions(
                     account_id, account, type_, False)
                 time_txns = [
@@ -201,18 +211,19 @@
                 for balance in balances:
                     entries.append(self._transform_balance(
                         balance, account, time_txns, pending_time_txns))
         return entries
 
     def _transform_balance(
             self,
-            truelayer_balance,
-            account,
-            time_txns,
-            pending_time_txns):
+            truelayer_balance: dict[str, Any],
+            account: dict[str, Any],
+            time_txns: list[tuple[datetime.datetime, Transaction]],
+            pending_time_txns: list[tuple[datetime.datetime, Transaction]],
+    ) -> Balance:
         """Transforms TrueLayer Balance to beancount Balance.
         
         Balance from TrueLayer can be effective at the middle of a day with
         pending transactions ignored, while beancount balance assertions
         must be applied at the beginning of a day and pending transactions
         are taken into account.
 
@@ -261,17 +272,17 @@
             amount=Amount(number, truelayer_balance['currency']),
             tolerance=None,
             diff_amount=None,
         )
 
     def _transform_transaction(
             self,
-            truelayer_txn,
-            beancount_account: Text,
-            is_pending: bool=False) -> Transaction:
+            truelayer_txn: dict[str, Any],
+            beancount_account: str,
+            is_pending: bool = False) -> Transaction:
         """Transforms TrueLayer Transaction to beancount Transaction."""
 
         number = abs(currency_to_decimal(truelayer_txn['amount']))
         if truelayer_txn['transaction_type'] == 'DEBIT':
             number = -number
         elif truelayer_txn['transaction_type'] == 'CREDIT':
             pass
@@ -306,70 +317,71 @@
     PORT = 3000
     REDIRECT_URI = 'http://localhost:3000/callback'
 
     def __init__(self, config: _Config):
         self._config = config
     
     @property
-    def access_token(self):
+    def access_token(self) -> str:
         access_token = self._get_valid_access_token()
         if access_token:
             return access_token
         self._refresh_access_token()
         access_token = self._get_valid_access_token()
         if access_token:
             return access_token
         self._request_access_token()
         access_token = self._get_valid_access_token()
         if access_token:
             return access_token
         raise RuntimeError('Unable to get a valid access token.')
 
-    def _get_valid_access_token(self):
+    def _get_valid_access_token(self) -> Optional[str]:
         """Get access token from config file."""
 
         access_token = self._config.data.get('access_token')
         expiry_time = self._config.data.get('access_token_expiry_time')
         now = int(time.time())
         if access_token and expiry_time and expiry_time > now:
             return access_token
+        return None
 
-    def _refresh_access_token(self):
+    def _refresh_access_token(self) -> None:
         """Refresh access token with refresh token."""
 
         logging.info('Attempt to refresh access token.')
         refresh_token = self._config.data.get('refresh_token', None)
         if not refresh_token:
             logging.info(
                 'Failed to refresh access token: refresh token not available.')
             return
         self._grant_access_token(refresh_token=refresh_token)
 
-    def _request_access_token(self):
+    def _request_access_token(self) -> None:
         """Get access token with regular OAuth flow."""
 
         logging.info('Attempt to request access token with regular OAuth flow.')
         code = self._request_code()
         self._grant_access_token(code=code)
         logging.info('Successfully requested access token.')
 
-    def _grant_access_token(self, code=None, refresh_token=None):
+    def _grant_access_token(self, code: Optional[str] = None, refresh_token: Optional[str] = None) -> None:
         """Grant access token with code or refresh_token."""
 
         logging.info('Attempt to grant access token.')
         req = {
             'client_id': self._config.client_id,
             'client_secret': self._config.client_secret,
         }
         if code:
             req['grant_type'] = 'authorization_code'
             req['redirect_uri'] = self.REDIRECT_URI
             req['code'] = code
         elif refresh_token:
-            req['grant_type'] = 'refresh_token',
+            req['grant_type'] = 'refresh_token'
             req['refresh_token'] = refresh_token
         else:
             assert False
         r = requests.post('https://auth.truelayer.com/connect/token', req)
         if r.status_code != 200:
             logging.warning(
                 f'Failed to grant access token: server returns '
@@ -379,29 +391,29 @@
         self._config.data['access_token'] = data['access_token']
         self._config.data['access_token_expiry_time'] = (
             int(time.time()) + data['expires_in'])
         self._config.data['refresh_token'] = data['refresh_token']
         self._config.dump()
         logging.info('Successfully granted access token.')
 
-    def _request_code(self):
+    def _request_code(self) -> str:
         """Get the code to redeem access token with regular OAuth flow."""
 
         state = secrets.token_urlsafe(16)
         code = None
         auth_link = None
 
         class HttpHandler(http.server.BaseHTTPRequestHandler):
-            def do_POST(self):
+            def do_POST(self) -> None:
                 logging.info('OAuth response received.')
                 length = int(self.headers.get('Content-Length'))
                 body = self.rfile.read(length).decode('utf-8')
-                data = urllib.parse.parse_qs(body)
-                received_state = data.get('state', [None])[0]
-                received_code = data.get('code', [None])[0]
+                data = dict(urllib.parse.parse_qsl(body))
+                received_state = data.get('state')
+                received_code = data.get('code')
 
                 if received_code and received_state == state:
                     nonlocal code
                     code = received_code
                     self.send_response(200)
                     response = b'You can now close this tab.\n'
                     self.send_header('Content-Type', 'text/plain')
@@ -410,14 +422,15 @@
                     self.wfile.write(response)
                 else:
                     if received_state != state:
                         logging.warning('OAuth response state mismatches.')
                     elif not received_code:
                         logging.warning('OAuth response misses code.')
                     self.send_response(302)
+                    assert auth_link
                     self.send_header('Location', auth_link)
 
         httpd = http.server.HTTPServer((self.ADDRESS, self.PORT), HttpHandler)
         socketname = httpd.socket.getsockname()
         logging.info(f'OAuth server listening at {socketname}')
         auth_link = self._build_auth_link(state)
         webbrowser.open_new(auth_link)
@@ -433,15 +446,15 @@
             file=sys.stderr)
 
         while not code:
             httpd.handle_request()
         httpd.server_close()
         return code
 
-    def _build_auth_link(self, state):
+    def _build_auth_link(self, state: str) -> str:
         qs = urllib.parse.urlencode({
             'response_type': 'code',
             'response_mode': 'form_post',
             'client_id': self._config.client_id,
             'redirect_uri': self.REDIRECT_URI,
             'scope': ' '.join([
                 'accounts',
@@ -450,8 +463,8 @@
                 'balance',
                 'offline_access',
             ]),
             'state': state,
         })
         return f'https://auth.truelayer.com/?{qs}'
 
-logging.basicConfig(level=os.getenv('LOG_LEVEL', 'WARNING'))
+logging.basicConfig(level=os.getenv('LOG_LEVEL', 'WARNING'))
```

### Comparing `autobean-0.1.3/autobean/utils/compare.py` & `autobean-0.2.0/autobean/utils/compare.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,16 +1,18 @@
-from typing import List
 from collections import Counter
 from beancount.core import data
 from beancount.core.data import Directive
 from beancount.core.compare import hash_entry
 
 
-# This is similar to beancount.core.comparer.compare_entries but allows duplicated entries
-def compare_entries(entries1: List[Directive], entries2: List[Directive]):
+def compare_entries(entries1: list[Directive], entries2: list[Directive]) -> tuple[bool, list[Directive], list[Directive]]:
+    """Compares two lists of entries.
+
+    Similiar to beancount.core.comparer.compare_entries but allows duplicated entries
+    """
     hashes1 = {
         hash_entry(entry, exclude_meta=True): entry for entry in entries1}
     hashes2 = {
         hash_entry(entry, exclude_meta=True): entry for entry in entries2}
 
     keys1 = Counter(hash_entry(entry, exclude_meta=True) for entry in entries1)
     keys2 = Counter(hash_entry(entry, exclude_meta=True) for entry in entries2)
```

### Comparing `autobean-0.1.3/autobean/utils/deduplicate.py` & `autobean-0.2.0/autobean/utils/deduplicate.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,47 +1,50 @@
 from collections import Counter, defaultdict, deque
 import copy
 import datetime
-from typing import List
+from typing import Iterable
 
 from beancount.core.data import Transaction, Directive, iter_entry_dates, filter_txns
 from beancount.ingest.extract import DUPLICATE_META
 
 
+_Node = tuple[bool, Directive]  # (is_new_entry, entry)
+
+
 def guess_transaction_duplicated(
         new_transaction: Transaction,
         existing_transaction: Transaction) -> bool:
     """Provides a rough guess that a new transaction already exists.
     
     Returns True iff for all the accounts that the new transaction describes,
     all postings under that account are the same in terms of units between
     the two transactions.
     """
 
-    relevant_accounts = set(
+    relevant_accounts = {
         posting.account
         for posting in new_transaction.postings
-    )
+    }
     relevant_existing_data = Counter(
         (posting.account, posting.units)
         for posting in existing_transaction.postings
         if posting.account in relevant_accounts
     )
     relevant_new_data = Counter(
         (posting.account, posting.units)
         for posting in new_transaction.postings
     )
 
     return relevant_existing_data == relevant_new_data
 
 
 def deduplicate(
-        new_entries: List[Directive],
-        existing_entries: List[Directive],
-        window_days: int = 5) -> List[Directive]:
+        new_entries: list[Directive],
+        existing_entries: list[Directive],
+        window_days: int = 10) -> list[Directive]:
     """De-duplicate entries.
 
     A new non-transaction entry is considered connected to an existing entry
     iff they are identical.
     
     A new transaction is considered connected to an existing transaction iff:
     * the new transaction is no earlier than the existing transaction.
@@ -76,16 +79,16 @@
             for existing_entry in iter_entry_dates(
                     existing_entries,
                     new_entry.date,
                     new_entry.date + window_tail):
                 if new_entry == existing_entry:
                     matcher.add_edge(id(new_entry), id(existing_entry))
     
-    duplicates = set()
-    possibly_duplicates = set()
+    duplicates: set[Directive] = set()
+    possibly_duplicates: set[Directive] = set()
 
     matches = matcher.matches()
     for subgraph in matcher.subgraphs():
         n = len([True for node in subgraph if node in matches])
         if n == len(subgraph):  # duplicated
             duplicates.update(node[1] for node in subgraph if node[0])
         elif n:  # possibly duplicated
@@ -102,31 +105,31 @@
         else:
             ret.append(new_entry)
 
     return ret
 
 
 class _Matcher:
-    def __init__(self):
-        self._new_nodes = set()
-        self._edges = defaultdict(set)
+    def __init__(self) -> None:
+        self._new_nodes: set[_Node] = set()
+        self._edges: defaultdict[_Node, set[_Node]] = defaultdict(set)
 
-    def add_edge(self, new_entry, existing_entry):
+    def add_edge(self, new_entry: Directive, existing_entry: Directive) -> None:
         new_node = (True, new_entry)
         existing_node = (False, existing_entry)
         self._new_nodes.add(new_node)
         self._edges[new_node].add(existing_node)
         self._edges[existing_node].add(new_node)
 
-    def matches(self):
+    def matches(self) -> set[_Node]:
         matches = set()
         for new_node in self._new_nodes:
             if new_node in matches:
                 continue
-            q = deque()
+            q: deque[_Node] = deque()
             q.append(new_node)
             visited = set()
             while q:
                 u = q.popleft()
                 if u in visited:
                     continue
                 visited.add(u)
@@ -134,21 +137,21 @@
                     matches.add(new_node)
                     matches.add(u)
                     break
                 for v in self._edges[u]:
                     q.append(v)
         return matches
 
-    def subgraphs(self):
+    def subgraphs(self) -> Iterable[set[_Node]]:
         visited = set()
         for new_node in self._new_nodes:
             if new_node in visited:
                 continue
             subgraph_nodes = set()
-            q = deque()
+            q: deque[_Node] = deque()
             q.append(new_node)
             while q:
                 u = q.popleft()
                 if u in visited:
                     continue
                 subgraph_nodes.add(u)
                 visited.add(u)
```

### Comparing `autobean-0.1.3/autobean.egg-info/PKG-INFO` & `autobean-0.2.0/autobean.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,46 +1,41 @@
 Metadata-Version: 2.1
 Name: autobean
-Version: 0.1.3
+Version: 0.2.0
 Summary: A collection of plugins and scripts that help automating bookkeeping with beancount
 Home-page: https://github.com/SEIAROTg/autobean
 Author: SEIAROTg
 Author-email: seiarotg@gmail.com
-License: UNKNOWN
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v2 (GPLv2)
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Office/Business :: Financial :: Accounting
-Requires-Python: >=3.8
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # autobean
-
-[![travis](https://travis-ci.com/SEIAROTg/autobean.svg)](https://travis-ci.com/SEIAROTg/autobean)
+[![CircleCI](https://circleci.com/gh/SEIAROTg/autobean.svg?style=shield)](https://circleci.com/gh/SEIAROTg/autobean)
 [![pypi](https://img.shields.io/pypi/v/autobean)](https://pypi.org/project/autobean/)
 [![codecov](https://codecov.io/gh/SEIAROTg/autobean/branch/master/graph/badge.svg)](https://codecov.io/gh/SEIAROTg/autobean)
-[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/SEIAROTg/autobean.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/SEIAROTg/autobean/context:python)
 [![Maintainability](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/maintainability)](https://codeclimate.com/github/SEIAROTg/autobean/maintainability)
 [![Test Coverage](https://api.codeclimate.com/v1/badges/65e79b66e57139ed8bd0/test_coverage)](https://codeclimate.com/github/SEIAROTg/autobean/test_coverage)
 [![license](https://img.shields.io/github/license/SEIAROTg/autobean.svg)](https://github.com/SEIAROTg/autobean)
 
 A collection of plugins and scripts that help automating bookkeeping with [beancount](http://furius.ca/beancount/).
 
 ## Components
 
-* [autobean.share](autobean/share): Manages shared accounts / transactions / postings with simple annotations and reuses joint ledgers among multiple parties.
+* [autobean.share](autobean/share): expense split, joint bookkeeping, and debt management for personal use cases.
 * [autobean.xcheck](autobean/xcheck): Cross-checks against external ledgers.
 * [autobean.narration](autobean/narration): Generates transaction narration from posting narration and posting narration from comments.
 * [autobean.include](autobean/include): Includes external beancount ledgers without disabling their plugins.
-* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), an bank API aggregator.
+* [autobean.truelayer](autobean/truelayer): Imports transactions from banks via [TrueLayer](https://truelayer.com/), a bank API aggregator.
 * [autobean.sorted](autobean/sorted): Checks that transactions are in non-descending order in each file.
+* [autobean.stock_split](autobean/stock_split): Simplifies stock split.
 
 ## Install
 
 ```sh
 pip install autobean
 ```
-
-
```

### Comparing `autobean-0.1.3/autobean.egg-info/SOURCES.txt` & `autobean-0.2.0/autobean.egg-info/SOURCES.txt`

 * *Files 25% similar despite different names*

```diff
@@ -13,34 +13,34 @@
 autobean/include/tests/test_runner.py
 autobean/narration/__init__.py
 autobean/narration/comments.py
 autobean/narration/plugin.py
 autobean/narration/tests/__init__.py
 autobean/narration/tests/test_runner.py
 autobean/share/__init__.py
-autobean/share/fill_residuals.py
 autobean/share/include.py
 autobean/share/include_context.py
 autobean/share/link_accounts.py
-autobean/share/map_residual_accounts.py
-autobean/share/open_subaccounts.py
 autobean/share/plugin.py
-autobean/share/policy.py
-autobean/share/select_viewpoint.py
-autobean/share/split_postings.py
-autobean/share/utils.py
+autobean/share/policy_lib.py
+autobean/share/policy_lib_test.py
+autobean/share/split_account.py
+autobean/share/viewpoint_lib.py
 autobean/share/tests/__init__.py
 autobean/share/tests/test_runner.py
 autobean/sorted/__init__.py
 autobean/sorted/plugin.py
+autobean/stock_split/__init__.py
+autobean/stock_split/plugin.py
+autobean/stock_split/plugin_test.py
 autobean/truelayer/__init__.py
 autobean/truelayer/importer.py
 autobean/utils/__init__.py
 autobean/utils/compare.py
 autobean/utils/deduplicate.py
-autobean/utils/error_logger.py
-autobean/utils/plugin_base.py
+autobean/utils/error_lib.py
+autobean/utils/plugin_lib.py
 autobean/utils/plugin_test_utils.py
 autobean/xcheck/__init__.py
 autobean/xcheck/plugin.py
 autobean/xcheck/tests/__init__.py
 autobean/xcheck/tests/test_runner.py
```

### Comparing `autobean-0.1.3/setup.py` & `autobean-0.2.0/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -4,15 +4,15 @@
     long_description = f.read()
 
 with open('requirements.txt', 'r') as f:
     requirements = list(filter(None, f.read().split('\n')))
 
 setuptools.setup(
     name='autobean',
-    version='0.1.3',
+    version='0.2.0',
     author='SEIAROTg',
     author_email='seiarotg@gmail.com',
     description='A collection of plugins and scripts that help automating bookkeeping with beancount',
     long_description=long_description,
     long_description_content_type='text/markdown',
     url='https://github.com/SEIAROTg/autobean',
     packages=setuptools.find_packages(),
@@ -20,9 +20,9 @@
     classifiers=[
         'Programming Language :: Python :: 3',
         'License :: OSI Approved :: GNU General Public License v2 (GPLv2)',
         'Operating System :: OS Independent',
         'Development Status :: 3 - Alpha',
         'Topic :: Office/Business :: Financial :: Accounting',
     ],
-    python_requires='>=3.8',
+    python_requires='>=3.10',
 )
```

