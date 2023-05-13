# Comparing `tmp/dnsmule-0.1.0.post1.tar.gz` & `tmp/dnsmule-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dnsmule-0.1.0.post1.tar", last modified: Mon Mar 13 14:11:26 2023, max compression
+gzip compressed data, was "dnsmule-0.5.0.tar", last modified: Sat May 13 17:40:08 2023, max compression
```

## Comparing `dnsmule-0.1.0.post1.tar` & `dnsmule-0.5.0.tar`

### file list

```diff
@@ -1,75 +1,55 @@
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.061379 dnsmule-0.1.0.post1/
--rw-r--r--   0 jonium     (501) staff       (20)     1063 2023-02-15 09:31:46.000000 dnsmule-0.1.0.post1/LICENSE
--rw-r--r--   0 jonium     (501) staff       (20)       23 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/MANIFEST.in
--rw-r--r--   0 jonium     (501) staff       (20)     9439 2023-03-13 14:11:26.061218 dnsmule-0.1.0.post1/PKG-INFO
--rw-r--r--   0 jonium     (501) staff       (20)     2826 2023-03-13 14:08:31.000000 dnsmule-0.1.0.post1/README.md
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.052862 dnsmule-0.1.0.post1/rules/
--rw-r--r--   0 jonium     (501) staff       (20)     5807 2023-03-13 14:08:31.000000 dnsmule-0.1.0.post1/rules/README.md
--rw-r--r--   0 jonium     (501) staff       (20)       38 2023-03-13 14:11:26.061413 dnsmule-0.1.0.post1/setup.cfg
--rw-r--r--   0 jonium     (501) staff       (20)     1622 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/setup.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.051524 dnsmule-0.1.0.post1/src/
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.053536 dnsmule-0.1.0.post1/src/DNSMule.egg-info/
--rw-r--r--   0 jonium     (501) staff       (20)     9439 2023-03-13 14:11:26.000000 dnsmule-0.1.0.post1/src/DNSMule.egg-info/PKG-INFO
--rw-r--r--   0 jonium     (501) staff       (20)     1794 2023-03-13 14:11:26.000000 dnsmule-0.1.0.post1/src/DNSMule.egg-info/SOURCES.txt
--rw-r--r--   0 jonium     (501) staff       (20)        1 2023-03-13 14:11:26.000000 dnsmule-0.1.0.post1/src/DNSMule.egg-info/dependency_links.txt
--rw-r--r--   0 jonium     (501) staff       (20)       42 2023-03-13 14:11:26.000000 dnsmule-0.1.0.post1/src/DNSMule.egg-info/requires.txt
--rw-r--r--   0 jonium     (501) staff       (20)        8 2023-03-13 14:11:26.000000 dnsmule-0.1.0.post1/src/DNSMule.egg-info/top_level.txt
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.054093 dnsmule-0.1.0.post1/src/dnsmule/
--rw-r--r--   0 jonium     (501) staff       (20)      230 2023-03-13 14:10:18.000000 dnsmule-0.1.0.post1/src/dnsmule/__init__.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.055248 dnsmule-0.1.0.post1/src/dnsmule/backends/
--rw-r--r--   0 jonium     (501) staff       (20)       60 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/backends/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     1406 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/backends/abstract.py
--rw-r--r--   0 jonium     (501) staff       (20)     3273 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/backends/dnspython.py
--rw-r--r--   0 jonium     (501) staff       (20)      371 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/backends/noop.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.055647 dnsmule-0.1.0.post1/src/dnsmule/config/
--rw-r--r--   0 jonium     (501) staff       (20)       52 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/config/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)      242 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/config/defaults.py
--rw-r--r--   0 jonium     (501) staff       (20)      108 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/config/logs.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.056426 dnsmule-0.1.0.post1/src/dnsmule/definitions/
--rw-r--r--   0 jonium     (501) staff       (20)      131 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     1677 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/data.py
--rw-r--r--   0 jonium     (501) staff       (20)     1194 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/domain.py
--rw-r--r--   0 jonium     (501) staff       (20)     1491 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/record.py
--rw-r--r--   0 jonium     (501) staff       (20)     1875 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/result.py
--rw-r--r--   0 jonium     (501) staff       (20)     6995 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/definitions/rrtype.py
--rw-r--r--   0 jonium     (501) staff       (20)     5214 2023-03-13 14:08:31.000000 dnsmule-0.1.0.post1/src/dnsmule/loader.py
--rw-r--r--   0 jonium     (501) staff       (20)     3771 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/mule.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.056834 dnsmule-0.1.0.post1/src/dnsmule/plugins/
--rw-r--r--   0 jonium     (501) staff       (20)       29 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/plugins/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)      449 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/plugins/abstract.py
--rw-r--r--   0 jonium     (501) staff       (20)      166 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/plugins/noop.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.057524 dnsmule-0.1.0.post1/src/dnsmule/rules/
--rw-r--r--   0 jonium     (501) staff       (20)       77 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/rules/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     3000 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/rules/entities.py
--rw-r--r--   0 jonium     (501) staff       (20)      901 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/rules/factories.py
--rw-r--r--   0 jonium     (501) staff       (20)     1944 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/rules/rules.py
--rw-r--r--   0 jonium     (501) staff       (20)     3310 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/rules/ruletypes.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.058268 dnsmule-0.1.0.post1/src/dnsmule/utils/
--rw-r--r--   0 jonium     (501) staff       (20)      108 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     2383 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/async_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)     1549 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/comaparable.py
--rw-r--r--   0 jonium     (501) staff       (20)      864 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/data_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)      749 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/iter_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)     4693 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/src/dnsmule/utils/misc.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:26.061026 dnsmule-0.1.0.post1/test/
--rw-r--r--   0 jonium     (501) staff       (20)     2248 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_backends_abstract.py
--rw-r--r--   0 jonium     (501) staff       (20)     5701 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_backends_dnspython.py
--rw-r--r--   0 jonium     (501) staff       (20)     1763 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_comparable.py
--rw-r--r--   0 jonium     (501) staff       (20)     2494 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_creator.py
--rw-r--r--   0 jonium     (501) staff       (20)     4140 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_data.py
--rw-r--r--   0 jonium     (501) staff       (20)     1662 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_domain.py
--rw-r--r--   0 jonium     (501) staff       (20)     2355 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_dynamic_rule.py
--rw-r--r--   0 jonium     (501) staff       (20)     1234 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_factories.py
--rw-r--r--   0 jonium     (501) staff       (20)     1983 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_iter_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)     3454 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_loading.py
--rw-r--r--   0 jonium     (501) staff       (20)     6998 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_mule.py
--rw-r--r--   0 jonium     (501) staff       (20)      479 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_plugins_abstract.py
--rw-r--r--   0 jonium     (501) staff       (20)     2159 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_record.py
--rw-r--r--   0 jonium     (501) staff       (20)     3976 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_regex_rule.py
--rw-r--r--   0 jonium     (501) staff       (20)     3714 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_result.py
--rw-r--r--   0 jonium     (501) staff       (20)     1284 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_rrtype.py
--rw-r--r--   0 jonium     (501) staff       (20)     3454 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_rule.py
--rw-r--r--   0 jonium     (501) staff       (20)     5046 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_rules.py
--rw-r--r--   0 jonium     (501) staff       (20)     2383 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_rules_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)     3390 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_utils.py
--rw-r--r--   0 jonium     (501) staff       (20)     4278 2023-03-13 07:50:12.000000 dnsmule-0.1.0.post1/test/test_work_queue.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.226354 dnsmule-0.5.0/
+-rw-r--r--   0 jonium     (501) staff       (20)     1063 2023-02-15 09:31:46.000000 dnsmule-0.5.0/LICENSE
+-rw-r--r--   0 jonium     (501) staff       (20)     8013 2023-05-13 17:40:08.226134 dnsmule-0.5.0/PKG-INFO
+-rw-r--r--   0 jonium     (501) staff       (20)     7194 2023-05-13 11:50:37.000000 dnsmule-0.5.0/README.md
+-rw-r--r--   0 jonium     (501) staff       (20)       38 2023-05-13 17:40:08.226404 dnsmule-0.5.0/setup.cfg
+-rw-r--r--   0 jonium     (501) staff       (20)     1691 2023-05-13 11:50:37.000000 dnsmule-0.5.0/setup.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.211698 dnsmule-0.5.0/src/
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.214478 dnsmule-0.5.0/src/DNSMule.egg-info/
+-rw-r--r--   0 jonium     (501) staff       (20)     8013 2023-05-13 17:40:08.000000 dnsmule-0.5.0/src/DNSMule.egg-info/PKG-INFO
+-rw-r--r--   0 jonium     (501) staff       (20)     1377 2023-05-13 17:40:08.000000 dnsmule-0.5.0/src/DNSMule.egg-info/SOURCES.txt
+-rw-r--r--   0 jonium     (501) staff       (20)        1 2023-05-13 17:40:08.000000 dnsmule-0.5.0/src/DNSMule.egg-info/dependency_links.txt
+-rw-r--r--   0 jonium     (501) staff       (20)       88 2023-05-13 17:40:08.000000 dnsmule-0.5.0/src/DNSMule.egg-info/requires.txt
+-rw-r--r--   0 jonium     (501) staff       (20)        8 2023-05-13 17:40:08.000000 dnsmule-0.5.0/src/DNSMule.egg-info/top_level.txt
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.215765 dnsmule-0.5.0/src/dnsmule/
+-rw-r--r--   0 jonium     (501) staff       (20)      232 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/__init__.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.219038 dnsmule-0.5.0/src/dnsmule/backends/
+-rw-r--r--   0 jonium     (501) staff       (20)       60 2023-03-13 07:50:12.000000 dnsmule-0.5.0/src/dnsmule/backends/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)      860 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/backends/abstract.py
+-rw-r--r--   0 jonium     (501) staff       (20)     3081 2023-05-13 17:23:22.000000 dnsmule-0.5.0/src/dnsmule/backends/dnspython.py
+-rw-r--r--   0 jonium     (501) staff       (20)      330 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/backends/noop.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1210 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/baseclasses.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.220649 dnsmule-0.5.0/src/dnsmule/definitions/
+-rw-r--r--   0 jonium     (501) staff       (20)      129 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/definitions/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)       89 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/definitions/domain.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1265 2023-05-13 13:31:06.000000 dnsmule-0.5.0/src/dnsmule/definitions/record.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2077 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/definitions/result.py
+-rw-r--r--   0 jonium     (501) staff       (20)     6866 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/definitions/rrtype.py
+-rw-r--r--   0 jonium     (501) staff       (20)       80 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/definitions/tag.py
+-rw-r--r--   0 jonium     (501) staff       (20)     5573 2023-05-13 12:34:41.000000 dnsmule-0.5.0/src/dnsmule/loader.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.221042 dnsmule-0.5.0/src/dnsmule/logger/
+-rw-r--r--   0 jonium     (501) staff       (20)       31 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/logger/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)      108 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/logger/logger.py
+-rw-r--r--   0 jonium     (501) staff       (20)     3646 2023-05-13 12:53:27.000000 dnsmule-0.5.0/src/dnsmule/mule.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.221730 dnsmule-0.5.0/src/dnsmule/plugins/
+-rw-r--r--   0 jonium     (501) staff       (20)       38 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/plugins/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1191 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/plugins/abstract.py
+-rw-r--r--   0 jonium     (501) staff       (20)      189 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/plugins/noop.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.222984 dnsmule-0.5.0/src/dnsmule/rules/
+-rw-r--r--   0 jonium     (501) staff       (20)       77 2023-03-13 07:50:12.000000 dnsmule-0.5.0/src/dnsmule/rules/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2664 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/rules/entities.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1197 2023-05-09 14:36:29.000000 dnsmule-0.5.0/src/dnsmule/rules/factories.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2259 2023-03-21 09:59:05.000000 dnsmule-0.5.0/src/dnsmule/rules/rules.py
+-rw-r--r--   0 jonium     (501) staff       (20)     3308 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/rules/ruletypes.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.224567 dnsmule-0.5.0/src/dnsmule/storages/
+-rw-r--r--   0 jonium     (501) staff       (20)      323 2023-05-11 15:45:45.000000 dnsmule-0.5.0/src/dnsmule/storages/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     8021 2023-05-13 14:16:58.000000 dnsmule-0.5.0/src/dnsmule/storages/abstract.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1300 2023-05-10 13:59:37.000000 dnsmule-0.5.0/src/dnsmule/storages/dictstorage.py
+-rw-r--r--   0 jonium     (501) staff       (20)     4103 2023-05-11 18:44:21.000000 dnsmule-0.5.0/src/dnsmule/storages/mongodbstorage.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1731 2023-05-13 14:18:38.000000 dnsmule-0.5.0/src/dnsmule/storages/redisstorage.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.225125 dnsmule-0.5.0/src/dnsmule/utils/
+-rw-r--r--   0 jonium     (501) staff       (20)       20 2023-05-10 10:10:12.000000 dnsmule-0.5.0/src/dnsmule/utils/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     3653 2023-05-10 11:17:54.000000 dnsmule-0.5.0/src/dnsmule/utils/misc.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:40:08.225627 dnsmule-0.5.0/test/
+-rw-r--r--   0 jonium     (501) staff       (20)     1054 2023-05-10 10:10:12.000000 dnsmule-0.5.0/test/test_baseclasses.py
+-rw-r--r--   0 jonium     (501) staff       (20)     5105 2023-05-13 12:54:08.000000 dnsmule-0.5.0/test/test_mule.py
```

### Comparing `dnsmule-0.1.0.post1/LICENSE` & `dnsmule-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `dnsmule-0.1.0.post1/PKG-INFO` & `dnsmule-0.5.0/PKG-INFO`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnsmule
-Version: 0.1.0.post1
+Version: 0.5.0
 Summary: Rule based dependency scanning and service fingerprinting via DNS
 Home-page: https://github.com/joniumGit/dnsmule
 Author: joniumGit
 Author-email: 52005121+joniumGit@users.noreply.github.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/joniumGit/dnsmule/issues
 Project-URL: Source, https://github.com/joniumGit/dnsmule
@@ -14,112 +14,60 @@
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Internet
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: dev
+Provides-Extra: full
 License-File: LICENSE
 
 # DNSMule
 
 [![codecov](https://codecov.io/gh/joniumGit/dnsmule/branch/master/graph/badge.svg?token=54DPREJIFU)](https://codecov.io/gh/joniumGit/dnsmule)
 
 Package for rule based dependency scanning and service fingerprinting via DNS.
 
 This package provides utilities for writing and evaluating verbose and easy to read rule definitions in _YAML_-format.
 There are two builtin rule formats with more available as plugins.
 
+## Installation
+
+```shell
+pip install dnsmule[full] dnsmule_plugins[full]
+```
+
+This will install everything available for DNSMule. You can also choose to install components as necessary.
+
+For installing from the repo you can use:
+
+```shell
+pip install -e .
+```
+
 ## Overview
 
 The DNSMule tool is composed in the following way:
 
 - DNSMule
     - Backend
     - Rules
         - Rule
     - Plugins
 
-#### Backends
-
-Any backend can be used and registered in YAML, the only requirement is extending the `dnsmule.backends.Backend` class.
-A backend is responsible for creating `dnsmule.definition.Record` instances for processing with `dnsmule.rules.Rules`.
+## Examples
 
-#### Plugins
+Check out the examples in the [examples](examples) folder. They should get you up and running quickly.
 
-Plugins provide DNSMule with additional functionality and/or rule(types).
-Plugins can be registered in YAML.
-It is required that all plugins extend the `dnsmule.plugins.Plugin` class.
-
-#### Rules
-
-This class is responsible for processing every`Record` and producing a `dnsmule.definition.Result` for them.
-The actual processing happens in individual `dnsmule.rules.Rule` instances that are ordered and orchestrated by this
-class.
-
-#### Rule
-
-These are user defined rules that process individual `Record` instances and append information to `record.data`
-or `record.tags`. The `record.data` is a storage for result metadata and additional information. The `record.tags` set
-is a collection of identifications for an input `Record`.
-
-#### Current State
-
-States (Complete, Testing, Developing, Refining) for every feature planned at this moment.
-
-- (Complete) Backends
-    - (Complete) DNSPythonBackend
-    - (Complete) YAML definition
-- (Complete) Rules
-    - (Complete) Builtin types
-    - (Complete) Custom rules
-    - (Complete) Custom rule factories
-    - (Complete) YAML definition
-- (Testing) Plugins
-    - (Complete) Registration in program
-    - (Complete) Registration in YAML
-    - (Complete) YAML definition
-    - (Developing) Increasing test coverage
-- (Refining) Result Storage
-    - (Refining) Registration in program
-    - (Refining) Registration in YAML
-    - (Refining) YAML definition
-- (Developing) DNSMule
-    - (Complete) Rules from YAML
-    - (Complete) Backend from YAML
-    - (Testing) Plugins from YAML
-    - (Developing) Processing and gathering results
-    - (Refining) Result storage
-    - (Refining) Result storage from YAML
-    - (Refining) Combined YAML definition
-
-#### Example server
-
-The repo has a `Dockerfile` for easily running the tool using an example server in Docker:
-
-```shell
-$ ./build-image
-$ ./run-server
-```
-
-#### Notice
-
-This package is under active development.
+## YAML Configuration
 
-#### Additional
-
-- RnD Scripts under [scripts](scripts)
-- Example server under [server](server) 
-
-# Rules
-
-## Summary
+### Summary
 
 The tool configuration is done through one or multiple rule configuration files. The file structure is defined in the
-[schema file](rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
+[schema file](rules/rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
 registering handlers or rules programmatically.
 
 Rules support registration per DNS record type and priority for controlling invocation order.
 
 ```yaml
 version: '0.0.1'
 rules:
@@ -146,30 +94,32 @@
 
 rules: Rules
 
 ...
 
 
 @rules.add.A[10]
-async def my_scan(record: Record) -> Result:
-    from dnsmule.config import get_logger
+def my_scan(record: Record) -> Result:
+    from dnsmule.logger import get_logger
     get_logger().info('Address %s', record)
-    return record.identify('MY::SCAN')
+    return record.tag('MY::SCAN')
 
 
 @rules.register('my.rule')
 def create_my_rule(**arguments) -> Rule:
     ...
 ```
 
 Here the `add` is used to directly register a new rule into the ruleset with a given priority. The `register` call
-creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from `yml` or code would be routed to
+creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from YAML or code would be routed to
 this factory function.
 
-## Other Components in YAML
+See the examples folder for more examples and how to use rules in code.
+
+### Plugins and Backends
 
 #### Plugins
 
 It is possible to register plugins using the YAML file:
 
 ```yaml
 plugins:
@@ -213,26 +163,23 @@
 
 This is configured in the schema using the custom intellij language injection tag:
 
 ```yml
 x-intellij-language-injection:
   language: Python
   prefix: |+0
-    from dnsmule.rules.entities import Type, Record, Result
-
-    def add_rule(record_type: Any, rule_type: str, name: str, priority: int = 0, **options) -> None:
-        pass
-
+    code hints go here
+    check the schema for more info
   suffix: ''
 ```
 
 Currently, this supports `dns.regex` pattern regex language injection and `dns.dynamic` rule code language injection.
 Type hints and quick documentation are available.
 
-## Builtin types
+## Builtin Rules
 
 #### Regex rules
 
 Regex rules can be defined with either one `pattern` or multiple `patterns`.
 An example is in the following snippet:
 
 ```yml
@@ -256,15 +203,15 @@
         - '^(.+)(?:-(?:site|domain))?-verification='
         - '^(.+)(?:site|domain)verification'
         - '^(.+)_verify_'
         - '^(\w+)-code:'
       group: 1
 ```
 
-The full definition is available from the schema file.
+The full definition and additional info is available from the schema file, examples, and code.
 
 #### Dynamic Rules
 
 Dynamic rules are defined as code snippets with one or two methods
 
 An init method that is invoked once after creation
 
@@ -281,34 +228,35 @@
     return record.result()
 ```
 
 Both of these functions have access to the following rule creation method:
 
 ```python
 def add_rule(
-        record_type: Any,
+        record_type: Union[str, int, RRType],
         rule_type: str,
         name: str,
+        *,
         priority: int = 0,
         **options,
 ) -> None:
     """
     :param record_type: Valid DNS record type as text, int, or type
     :param rule_type:   Valid rule type factory e.g. dns.regex
     :param name:        Name of the created rule
     :param priority:    Priority for the created rule, default 0
     :param options:     Any additional options for the rule factory
     """
-    pass
 ```
 
 The only globals passed to these methods are:
 
 - \_\_builtins\_\_
-- from dnsmule.definitions import RRType, Record, Result
+- RRType, Record, Result, Domain, Tag, Config
+    - The Config contains the `config` property passed to the rule from YAML
 - add_rule
 - Any additional globals created by the code itself
 
 When the code is exec'd the result is inspected for:
 
 - init function without parameters
 - process function with a single parameter
@@ -318,7 +266,28 @@
 - The init function is invoked exactly once.
 - The process function is invoked exactly once for every single Record.
 - Any rules created from the init method will be invoked for every suitable record.
 - Any rules created from the process method will be invoked for suitable records found after creation.
 - Creating DynamicRules from init or process is considered undefined behaviour and care should be taken
     - The user should call init manually and include fail-safes for only calling it once
     - The add_rule callback might not be available so you need to pass it manually to the rule
+
+## Other
+
+### Example server
+
+The repo has a `Dockerfile` for easily running the tool using an example server in Docker:
+
+```shell
+$ ./build-image
+$ ./run-server
+```
+
+### Notice
+
+This package is under active development.
+
+### Additional
+
+- RnD Scripts under [scripts](scripts)
+- Example server under [server](server)
+- Examples for coding under [examples](examples)
```

### Comparing `dnsmule-0.1.0.post1/rules/README.md` & `dnsmule-0.5.0/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,13 +1,50 @@
-# Rules
+# DNSMule
 
-## Summary
+[![codecov](https://codecov.io/gh/joniumGit/dnsmule/branch/master/graph/badge.svg?token=54DPREJIFU)](https://codecov.io/gh/joniumGit/dnsmule)
+
+Package for rule based dependency scanning and service fingerprinting via DNS.
+
+This package provides utilities for writing and evaluating verbose and easy to read rule definitions in _YAML_-format.
+There are two builtin rule formats with more available as plugins.
+
+## Installation
+
+```shell
+pip install dnsmule[full] dnsmule_plugins[full]
+```
+
+This will install everything available for DNSMule. You can also choose to install components as necessary.
+
+For installing from the repo you can use:
+
+```shell
+pip install -e .
+```
+
+## Overview
+
+The DNSMule tool is composed in the following way:
+
+- DNSMule
+    - Backend
+    - Rules
+        - Rule
+    - Plugins
+
+## Examples
+
+Check out the examples in the [examples](examples) folder. They should get you up and running quickly.
+
+## YAML Configuration
+
+### Summary
 
 The tool configuration is done through one or multiple rule configuration files. The file structure is defined in the
-[schema file](rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
+[schema file](rules/rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
 registering handlers or rules programmatically.
 
 Rules support registration per DNS record type and priority for controlling invocation order.
 
 ```yaml
 version: '0.0.1'
 rules:
@@ -34,30 +71,32 @@
 
 rules: Rules
 
 ...
 
 
 @rules.add.A[10]
-async def my_scan(record: Record) -> Result:
-    from dnsmule.config import get_logger
+def my_scan(record: Record) -> Result:
+    from dnsmule.logger import get_logger
     get_logger().info('Address %s', record)
-    return record.identify('MY::SCAN')
+    return record.tag('MY::SCAN')
 
 
 @rules.register('my.rule')
 def create_my_rule(**arguments) -> Rule:
     ...
 ```
 
 Here the `add` is used to directly register a new rule into the ruleset with a given priority. The `register` call
-creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from `yml` or code would be routed to
+creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from YAML or code would be routed to
 this factory function.
 
-## Other Components in YAML
+See the examples folder for more examples and how to use rules in code.
+
+### Plugins and Backends
 
 #### Plugins
 
 It is possible to register plugins using the YAML file:
 
 ```yaml
 plugins:
@@ -101,26 +140,23 @@
 
 This is configured in the schema using the custom intellij language injection tag:
 
 ```yml
 x-intellij-language-injection:
   language: Python
   prefix: |+0
-    from dnsmule.rules.entities import Type, Record, Result
-
-    def add_rule(record_type: Any, rule_type: str, name: str, priority: int = 0, **options) -> None:
-        pass
-
+    code hints go here
+    check the schema for more info
   suffix: ''
 ```
 
 Currently, this supports `dns.regex` pattern regex language injection and `dns.dynamic` rule code language injection.
 Type hints and quick documentation are available.
 
-## Builtin types
+## Builtin Rules
 
 #### Regex rules
 
 Regex rules can be defined with either one `pattern` or multiple `patterns`.
 An example is in the following snippet:
 
 ```yml
@@ -144,15 +180,15 @@
         - '^(.+)(?:-(?:site|domain))?-verification='
         - '^(.+)(?:site|domain)verification'
         - '^(.+)_verify_'
         - '^(\w+)-code:'
       group: 1
 ```
 
-The full definition is available from the schema file.
+The full definition and additional info is available from the schema file, examples, and code.
 
 #### Dynamic Rules
 
 Dynamic rules are defined as code snippets with one or two methods
 
 An init method that is invoked once after creation
 
@@ -169,34 +205,35 @@
     return record.result()
 ```
 
 Both of these functions have access to the following rule creation method:
 
 ```python
 def add_rule(
-        record_type: Any,
+        record_type: Union[str, int, RRType],
         rule_type: str,
         name: str,
+        *,
         priority: int = 0,
         **options,
 ) -> None:
     """
     :param record_type: Valid DNS record type as text, int, or type
     :param rule_type:   Valid rule type factory e.g. dns.regex
     :param name:        Name of the created rule
     :param priority:    Priority for the created rule, default 0
     :param options:     Any additional options for the rule factory
     """
-    pass
 ```
 
 The only globals passed to these methods are:
 
 - \_\_builtins\_\_
-- from dnsmule.definitions import RRType, Record, Result
+- RRType, Record, Result, Domain, Tag, Config
+    - The Config contains the `config` property passed to the rule from YAML
 - add_rule
 - Any additional globals created by the code itself
 
 When the code is exec'd the result is inspected for:
 
 - init function without parameters
 - process function with a single parameter
@@ -205,8 +242,29 @@
 
 - The init function is invoked exactly once.
 - The process function is invoked exactly once for every single Record.
 - Any rules created from the init method will be invoked for every suitable record.
 - Any rules created from the process method will be invoked for suitable records found after creation.
 - Creating DynamicRules from init or process is considered undefined behaviour and care should be taken
     - The user should call init manually and include fail-safes for only calling it once
-    - The add_rule callback might not be available so you need to pass it manually to the rule
+    - The add_rule callback might not be available so you need to pass it manually to the rule
+
+## Other
+
+### Example server
+
+The repo has a `Dockerfile` for easily running the tool using an example server in Docker:
+
+```shell
+$ ./build-image
+$ ./run-server
+```
+
+### Notice
+
+This package is under active development.
+
+### Additional
+
+- RnD Scripts under [scripts](scripts)
+- Example server under [server](server)
+- Examples for coding under [examples](examples)
```

### Comparing `dnsmule-0.1.0.post1/setup.py` & `dnsmule-0.5.0/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 from pathlib import Path
 
 from setuptools import setup, find_packages
 
 here = Path(__file__).parent.resolve()
 readme = (here / 'README.md').read_text(encoding='utf-8')
-readme += '\n\n' + (here / 'rules' / 'README.md').read_text(encoding='utf-8')
 repo = 'https://github.com/joniumGit/dnsmule'
 version = (here / 'src' / 'dnsmule' / '__init__.py').read_text(encoding='utf-8')
 version = version.strip().splitlines(keepends=False).pop().split('=')[1].strip(" '")
 
 # https://pypi.org/classifiers/
 setup(
     name='dnsmule',
@@ -37,21 +36,28 @@
         include=(
             'dnsmule',
             'dnsmule.*',
         )
     ),
     python_requires='>=3.7',
     install_requires=[
-        'dnspython',
         'pyyaml',
     ],
     extras_require={
         'dev': [
             'pytest',
             'pytest-cov',
-        ]
+            'redis',
+            'pymongo',
+            'dnspython',
+        ],
+        'full': [
+            'redis',
+            'pymongo',
+            'dnspython',
+        ],
     },
     project_urls={
         'Bug Reports': f'{repo}/issues',
         'Source': repo,
     },
 )
```

### Comparing `dnsmule-0.1.0.post1/src/DNSMule.egg-info/PKG-INFO` & `dnsmule-0.5.0/src/DNSMule.egg-info/PKG-INFO`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnsmule
-Version: 0.1.0.post1
+Version: 0.5.0
 Summary: Rule based dependency scanning and service fingerprinting via DNS
 Home-page: https://github.com/joniumGit/dnsmule
 Author: joniumGit
 Author-email: 52005121+joniumGit@users.noreply.github.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/joniumGit/dnsmule/issues
 Project-URL: Source, https://github.com/joniumGit/dnsmule
@@ -14,112 +14,60 @@
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Internet
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: dev
+Provides-Extra: full
 License-File: LICENSE
 
 # DNSMule
 
 [![codecov](https://codecov.io/gh/joniumGit/dnsmule/branch/master/graph/badge.svg?token=54DPREJIFU)](https://codecov.io/gh/joniumGit/dnsmule)
 
 Package for rule based dependency scanning and service fingerprinting via DNS.
 
 This package provides utilities for writing and evaluating verbose and easy to read rule definitions in _YAML_-format.
 There are two builtin rule formats with more available as plugins.
 
+## Installation
+
+```shell
+pip install dnsmule[full] dnsmule_plugins[full]
+```
+
+This will install everything available for DNSMule. You can also choose to install components as necessary.
+
+For installing from the repo you can use:
+
+```shell
+pip install -e .
+```
+
 ## Overview
 
 The DNSMule tool is composed in the following way:
 
 - DNSMule
     - Backend
     - Rules
         - Rule
     - Plugins
 
-#### Backends
-
-Any backend can be used and registered in YAML, the only requirement is extending the `dnsmule.backends.Backend` class.
-A backend is responsible for creating `dnsmule.definition.Record` instances for processing with `dnsmule.rules.Rules`.
+## Examples
 
-#### Plugins
+Check out the examples in the [examples](examples) folder. They should get you up and running quickly.
 
-Plugins provide DNSMule with additional functionality and/or rule(types).
-Plugins can be registered in YAML.
-It is required that all plugins extend the `dnsmule.plugins.Plugin` class.
-
-#### Rules
-
-This class is responsible for processing every`Record` and producing a `dnsmule.definition.Result` for them.
-The actual processing happens in individual `dnsmule.rules.Rule` instances that are ordered and orchestrated by this
-class.
-
-#### Rule
-
-These are user defined rules that process individual `Record` instances and append information to `record.data`
-or `record.tags`. The `record.data` is a storage for result metadata and additional information. The `record.tags` set
-is a collection of identifications for an input `Record`.
-
-#### Current State
-
-States (Complete, Testing, Developing, Refining) for every feature planned at this moment.
-
-- (Complete) Backends
-    - (Complete) DNSPythonBackend
-    - (Complete) YAML definition
-- (Complete) Rules
-    - (Complete) Builtin types
-    - (Complete) Custom rules
-    - (Complete) Custom rule factories
-    - (Complete) YAML definition
-- (Testing) Plugins
-    - (Complete) Registration in program
-    - (Complete) Registration in YAML
-    - (Complete) YAML definition
-    - (Developing) Increasing test coverage
-- (Refining) Result Storage
-    - (Refining) Registration in program
-    - (Refining) Registration in YAML
-    - (Refining) YAML definition
-- (Developing) DNSMule
-    - (Complete) Rules from YAML
-    - (Complete) Backend from YAML
-    - (Testing) Plugins from YAML
-    - (Developing) Processing and gathering results
-    - (Refining) Result storage
-    - (Refining) Result storage from YAML
-    - (Refining) Combined YAML definition
-
-#### Example server
-
-The repo has a `Dockerfile` for easily running the tool using an example server in Docker:
-
-```shell
-$ ./build-image
-$ ./run-server
-```
-
-#### Notice
-
-This package is under active development.
+## YAML Configuration
 
-#### Additional
-
-- RnD Scripts under [scripts](scripts)
-- Example server under [server](server) 
-
-# Rules
-
-## Summary
+### Summary
 
 The tool configuration is done through one or multiple rule configuration files. The file structure is defined in the
-[schema file](rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
+[schema file](rules/rules-schema.yml). In addition to some builtin rule types, it is possible to create new types by
 registering handlers or rules programmatically.
 
 Rules support registration per DNS record type and priority for controlling invocation order.
 
 ```yaml
 version: '0.0.1'
 rules:
@@ -146,30 +94,32 @@
 
 rules: Rules
 
 ...
 
 
 @rules.add.A[10]
-async def my_scan(record: Record) -> Result:
-    from dnsmule.config import get_logger
+def my_scan(record: Record) -> Result:
+    from dnsmule.logger import get_logger
     get_logger().info('Address %s', record)
-    return record.identify('MY::SCAN')
+    return record.tag('MY::SCAN')
 
 
 @rules.register('my.rule')
 def create_my_rule(**arguments) -> Rule:
     ...
 ```
 
 Here the `add` is used to directly register a new rule into the ruleset with a given priority. The `register` call
-creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from `yml` or code would be routed to
+creates a new handler for rules of type `my.rule`. Any future `my.rule` creations from YAML or code would be routed to
 this factory function.
 
-## Other Components in YAML
+See the examples folder for more examples and how to use rules in code.
+
+### Plugins and Backends
 
 #### Plugins
 
 It is possible to register plugins using the YAML file:
 
 ```yaml
 plugins:
@@ -213,26 +163,23 @@
 
 This is configured in the schema using the custom intellij language injection tag:
 
 ```yml
 x-intellij-language-injection:
   language: Python
   prefix: |+0
-    from dnsmule.rules.entities import Type, Record, Result
-
-    def add_rule(record_type: Any, rule_type: str, name: str, priority: int = 0, **options) -> None:
-        pass
-
+    code hints go here
+    check the schema for more info
   suffix: ''
 ```
 
 Currently, this supports `dns.regex` pattern regex language injection and `dns.dynamic` rule code language injection.
 Type hints and quick documentation are available.
 
-## Builtin types
+## Builtin Rules
 
 #### Regex rules
 
 Regex rules can be defined with either one `pattern` or multiple `patterns`.
 An example is in the following snippet:
 
 ```yml
@@ -256,15 +203,15 @@
         - '^(.+)(?:-(?:site|domain))?-verification='
         - '^(.+)(?:site|domain)verification'
         - '^(.+)_verify_'
         - '^(\w+)-code:'
       group: 1
 ```
 
-The full definition is available from the schema file.
+The full definition and additional info is available from the schema file, examples, and code.
 
 #### Dynamic Rules
 
 Dynamic rules are defined as code snippets with one or two methods
 
 An init method that is invoked once after creation
 
@@ -281,34 +228,35 @@
     return record.result()
 ```
 
 Both of these functions have access to the following rule creation method:
 
 ```python
 def add_rule(
-        record_type: Any,
+        record_type: Union[str, int, RRType],
         rule_type: str,
         name: str,
+        *,
         priority: int = 0,
         **options,
 ) -> None:
     """
     :param record_type: Valid DNS record type as text, int, or type
     :param rule_type:   Valid rule type factory e.g. dns.regex
     :param name:        Name of the created rule
     :param priority:    Priority for the created rule, default 0
     :param options:     Any additional options for the rule factory
     """
-    pass
 ```
 
 The only globals passed to these methods are:
 
 - \_\_builtins\_\_
-- from dnsmule.definitions import RRType, Record, Result
+- RRType, Record, Result, Domain, Tag, Config
+    - The Config contains the `config` property passed to the rule from YAML
 - add_rule
 - Any additional globals created by the code itself
 
 When the code is exec'd the result is inspected for:
 
 - init function without parameters
 - process function with a single parameter
@@ -318,7 +266,28 @@
 - The init function is invoked exactly once.
 - The process function is invoked exactly once for every single Record.
 - Any rules created from the init method will be invoked for every suitable record.
 - Any rules created from the process method will be invoked for suitable records found after creation.
 - Creating DynamicRules from init or process is considered undefined behaviour and care should be taken
     - The user should call init manually and include fail-safes for only calling it once
     - The add_rule callback might not be available so you need to pass it manually to the rule
+
+## Other
+
+### Example server
+
+The repo has a `Dockerfile` for easily running the tool using an example server in Docker:
+
+```shell
+$ ./build-image
+$ ./run-server
+```
+
+### Notice
+
+This package is under active development.
+
+### Additional
+
+- RnD Scripts under [scripts](scripts)
+- Example server under [server](server)
+- Examples for coding under [examples](examples)
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/backends/dnspython.py` & `dnsmule-0.5.0/src/dnsmule/backends/dnspython.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,102 +1,106 @@
-from typing import Union, Dict, AsyncGenerator, Any, Callable, Coroutine, Generator
+from os import getenv
+from random import choice
+from typing import Dict, Any, Callable, Coroutine, Iterable
 
-from dns.asyncquery import udp_with_fallback, https, quic, udp, tcp, tls
-from dns.exception import Timeout
+from dns.exception import DNSException
 from dns.message import Message, make_query
-from dns.name import Name
+from dns.query import udp_with_fallback, https, quic, udp, tcp, tls
 from dns.rdata import Rdata
 from dns.rdatatype import RdataType
 from dns.rrset import RRset
 
 from .abstract import Backend
-from ..config import get_logger, defaults
-from ..definitions import Record, RRType, Data, Domain
+from ..definitions import Record, RRType, Domain
+from ..logger import get_logger
 
-_Querier = Callable[..., Coroutine[Any, Any, Message]]
+Querier = Callable[..., Coroutine[Any, Any, Message]]
 
 
-async def _default_query(query: Message, *args, **kwargs):
-    response, used_tcp = await udp_with_fallback(query, *args, **kwargs)
+def default_query(query: Message, *args, **kwargs):
+    response, used_tcp = udp_with_fallback(query, *args, **kwargs)
     if used_tcp:
         get_logger().debug('Used TCP fallback query\n%s', query)
     return response
 
 
+def message_to_record(message: Message) -> Iterable[Record]:
+    result_set: RRset
+    record_data: Rdata
+    from itertools import chain
+    for result_set in chain(message.answer, message.additional):
+        for record_data in result_set:
+            rtype = RRType.from_any(record_data.rdtype)
+            yield DNSPythonRecord(
+                type=rtype,
+                domain=Domain(result_set.name.to_text(omit_final_dot=True)),
+                data=record_data,
+            )
+
+
+class DNSPythonRecord(Record):
+    data: Rdata
+
+    @property
+    def text(self) -> str:
+        return self.data.to_text().removeprefix('"').removesuffix('"')
+
+    def __getattr__(self, item):
+        return getattr(self.data, item)
+
+
 class DNSPythonBackend(Backend):
-    _MODE_MAPPING: Dict[str, _Querier] = {
+    _SUPPORTED_QUERY_TYPES: Dict[str, Querier] = {
         'tcp': tcp,
         'udp': udp,
         'tls': tls,
-        'http': https,
         'quic': quic,
-        'default': _default_query,
+        'https': https,
+        'default': default_query,
     }
 
+    _DEFAULT_RESOLVER = getenv('DNSMULE_DEFAULT_RESOLVER', choice([
+        '208.67.222.222',
+        '208.67.220.220',
+        '1.1.1.1',
+        '1.0.0.1',
+        '8.8.8.8',
+        '8.8.4.4',
+    ]))
+
     timeout: float = 2
     querier: str = 'default'
-    resolver: str = defaults.DEFAULT_RESOLVER
-    _querier: _Querier
+    resolver: str = _DEFAULT_RESOLVER
+
+    _querier: Querier
 
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
         try:
-            self._querier = DNSPythonBackend._MODE_MAPPING[self.querier]
+            self._querier = DNSPythonBackend._SUPPORTED_QUERY_TYPES[self.querier]
         except KeyError:
             raise ValueError(f'Invalid query mode ({self.querier})')
-        self.enable_data_extension()
+        get_logger().info('DNSPYTHON: Resolver: %s', self.resolver)
 
-    async def dns_query(
+    def _dns_query(
             self,
-            host: Union[str, Name],
+            host: str,
             *types: int,
-    ) -> AsyncGenerator[Any, Message]:
+    ) -> Iterable[Message]:
         for dns_type in types:
-            dns_type = RdataType.make(dns_type)
-            query = make_query(host, dns_type)
-            get_logger().debug('%s\n%s', 'Starting query', query)
+            query = make_query(host, RdataType.make(dns_type))
             try:
-                response = await self._querier(query, self.resolver, timeout=self.timeout)
+                response = self._querier(query, self.resolver, timeout=self.timeout)
                 yield response
-            except Timeout:
-                get_logger().error('%s\n%s', 'Timed out query', query)
+            except DNSException as e:
+                get_logger().error('%s\n%s', 'Failed query', query, exc_info=e)
 
-    @staticmethod
-    def _process_message(
-            domain: Domain,
-            message: Message,
-    ) -> Generator[Record, Any, Any]:
-        """Processes a dns message
-        """
-        result_set: RRset
-        record_data: Rdata
-        for result_set in message.answer:
-            for record_data in result_set:
-                rtype = RRType.from_any(record_data.rdtype)
-                yield Record(
-                    type=rtype,
-                    domain=domain,
-                    data=Data(
-                        type=rtype,
-                        value=record_data.to_text().removesuffix('"').removeprefix('"'),
-                        original=record_data,
-                    ),
-                )
-
-    async def process(self, target: Domain, *types: RRType) -> AsyncGenerator[Record, Any]:
-        async for message in self.dns_query(target.name, *iter(RdataType.make(t) for t in types)):
-            for record in self._process_message(target, message):
+    def _query(self, target: Domain, *types: RRType) -> Iterable[Record]:
+        for message in self._dns_query(target, *types):
+            for record in message_to_record(message):
                 yield record
 
-    @staticmethod
-    def enable_data_extension():
-
-        def _getattr(self: Data, item: str):
-            if 'original' in self.data:
-                return getattr(self.data['original'], item)
-
-        Data.register_adapter(_getattr)
-
 
 __all__ = [
     'DNSPythonBackend',
+    'DNSPythonRecord',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/definitions/record.py` & `dnsmule-0.5.0/src/dnsmule/definitions/result.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,54 +1,75 @@
 from dataclasses import dataclass
-from typing import Union
+from typing import Dict, Set, Union, List, Optional
 
-from .data import Data
 from .domain import Domain
-from .result import Result
 from .rrtype import RRType
+from .tag import Tag
+from ..utils import left_merge
 
+ResultData = Dict[str, Union['ResultData', List, str, int, float]]
 
-@dataclass(slots=True, frozen=False, init=False)
-class Record:
+
+@dataclass(frozen=False, init=False, repr=True, eq=False, unsafe_hash=False)
+class Result:
     domain: Domain
-    type: RRType
-    data: Data
-    _result: Result
+    type: Set[RRType]
+    tags: Set[Tag]
+    data: ResultData
 
     # noinspection PyShadowingBuiltins
-    def __init__(self, domain: Union[str, Domain], type: RRType, data: Union[str, Data]):
-        self.domain = domain if isinstance(domain, Domain) else Domain(name=domain)
-        self.type = type
-        self.data = data if isinstance(data, Data) else Data(type=type, value=data)
-        if self.data.type != self.type:
-            raise ValueError('Data was not the same RRtype', self.type, self.data.type)
-        self._result = None
-
-    def result(self):
-        if self._result is None:
-            self._result = Result(self.domain, self.type)
-        return self._result
-
-    def identify(self, identification: str):
-        r = self.result()
-        r.tags.add(identification)
-        return r
+    def __init__(self, domain: Domain, initial_type: RRType = None):
+        self.type = set()
+        if initial_type:
+            self.type.add(initial_type)
+        self.domain = domain
+        self.tags = set()
+        self.data = {}
+
+    def tag(self, tag: Union[str, Tag]):
+        self.tags.add(tag)
+
+    def __add__(self, other: 'Result') -> 'Result':
+        if other is None or other is self:
+            return self
+        elif not isinstance(other, Result):
+            raise TypeError(f'Can not add Result and {type(other)}')
+        elif self.domain != other.domain:
+            raise ValueError('Can not add different domains')
+        else:
+            self.type.update(other.type)
+            self.tags.update(other.tags)
+            left_merge(self.data, other.data)
+            return self
+
+    def __bool__(self):
+        return bool(self.tags or self.data)
 
     def __hash__(self):
-        return hash((self.domain, self.type))
+        return hash(self.domain)
+
+    def __eq__(self, other: 'Result'):
+        return isinstance(other, Result) and other.domain == self.domain or other == self.domain
+
+    def __contains__(self, item):
+        return item in self.tags
 
-    def __eq__(self, other: 'Record'):
-        return isinstance(other, Record) and other.domain == self.domain and other.type == self.type
+    def __len__(self):
+        return len(self.tags)
 
-    def __getitem__(self, item):
+    def __iter__(self):
+        return iter(self.tags)
+
+    def __lt__(self, other: 'Result'):
+        return self.domain < other.domain
+
+    def __getitem__(self, item: str) -> Optional[ResultData]:
         return self.data[item]
 
-    def __setitem__(self, key, value):
+    def __setitem__(self, key: str, value: Union[ResultData, List, str, int, float]) -> None:
         self.data[key] = value
 
-    def __contains__(self, item):
-        return item in self.data
-
 
 __all__ = [
-    'Record',
+    'Result',
+    'ResultData',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/definitions/result.py` & `dnsmule-0.5.0/src/dnsmule/definitions/record.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,74 +1,57 @@
 from dataclasses import dataclass
-from typing import Dict, Set
+from typing import Any, Union, Dict
 
 from .domain import Domain
+from .result import Result
 from .rrtype import RRType
-from ..utils import lmerge
+from .tag import Tag
 
 
-@dataclass(slots=True, init=False, frozen=False)
-class Result:
+@dataclass(init=False)
+class Record:
     domain: Domain
-    type: Set[RRType]
-    tags: Set[str]
-    data: Dict
+    type: RRType
+    data: Any
 
-    # noinspection PyShadowingBuiltins
-    def __init__(self, domain: Domain, type: RRType = None):
-        self.type = set()
-        if type:
-            self.type.add(type)
-        self.domain = domain
-        self.tags = set()
-        self.data = {}
+    context: Dict[str, Any]
+    """Provides a place to attach arbitrary metadata to the Record
+    """
 
-    def __getitem__(self, item):
-        return self.data[item]
+    _result: Result
 
-    def __setitem__(self, key, value):
-        self.data[key] = value
-
-    def __contains__(self, item):
-        return item in self.tags
-
-    def __add__(self, other: 'Result') -> 'Result':
-        if not isinstance(other, Result):
-            raise TypeError(f'Can not add Result and {type(other)}')
-        if self is not other:
-            if self.domain != other.domain:
-                raise ValueError('Can not add different domains')
-            self.type.update(other.type)
-            self.tags.update(other.tags)
-            lmerge(self.data, other.data)
-        return self
+    # noinspection PyShadowingBuiltins
+    def __init__(self, domain: Domain, type: RRType, data: Any):
+        self.domain = domain
+        self.type = type
+        self.data = data
+        self._result = Result(self.domain, initial_type=self.type)
+        self.context = {}
+
+    @property
+    def result(self):
+        return self._result
+
+    @result.setter
+    def result(self, value: Result):
+        self._result += value
+
+    @property
+    def text(self) -> str:
+        return str(self.data)
 
-    def __bool__(self):
-        return bool(self.tags or self.data)
+    def tag(self, tag: Union[Tag, str]) -> None:
+        self.result.tag(tag)
 
     def __hash__(self):
-        return hash(self.domain)
-
-    def __eq__(self, other: 'Result'):
-        return isinstance(other, Result) and other.domain == self.domain or other == self.domain
-
-    def __len__(self):
-        return len(self.tags)
+        return hash((self.domain, self.type))
 
-    def __iter__(self):
-        return iter(self.tags)
-
-    def to_json(self):
-        return {
-            'domain': self.domain.name,
-            'type': [
-                str(t)
-                for t in map(RRType.from_any, sorted(self.type))
-            ],
-            'tags': [*self.tags],
-            'data': self.data
-        }
+    def __eq__(self, other):
+        return (
+                isinstance(other, Record)
+                and (self.domain, self.type, self.data) == (other.domain, other.type, other.data)
+        )
 
 
 __all__ = [
-    'Result',
+    'Record',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/definitions/rrtype.py` & `dnsmule-0.5.0/src/dnsmule/definitions/rrtype.py`

 * *Files 6% similar despite different names*

```diff
@@ -14,40 +14,39 @@
 
     @classmethod
     def to_text(cls, value: Union['RRType', int]) -> str:
         RRType._check_range(value)
         for k, v in cls.__members__.items():
             if v == value:
                 return k
-        return f'RRType.of({value})'
+        return str(value)
 
     @classmethod
-    def from_any(cls, value: Union[int, str, Any]) -> Union['RRType', int]:
-        if isinstance(value, str):
-            value = value.upper()
-            prefix = 'RRtype.of('.upper()
-            if value in cls.__members__:
-                return cls.__members__[value]
-            elif value.startswith(prefix):
-                value = int(value.removeprefix(prefix).removesuffix(')'))
-            else:
-                value = int(value)
-        RRType._check_range(value)
-        for k, v in cls.__members__.items():
-            if k == value or v == value:
-                return v
-        return int(value)
+    def from_text(cls, value: str) -> Union['RRType', int]:
+        value = value.upper()
+        for v in cls.__members__.keys():
+            # Could be str derivative with different hash
+            if value == v:
+                return cls.__members__[v]
+        return cls.make(int(value))
 
     @classmethod
-    def from_text(cls, value: str) -> Union['RRType', int]:
-        return cls.from_any(value)
+    def make(cls, value: int):
+        RRType._check_range(value)
+        for v in cls.__members__.values():
+            if v == value:
+                return v
+        return value
 
     @classmethod
-    def of(cls, value: int) -> Union['RRType', int]:
-        return cls.from_any(value)
+    def from_any(cls, value: Union[int, str, Any]) -> Union['RRType', int]:
+        if isinstance(value, int):
+            return cls.make(value)
+        else:
+            return cls.from_text(str(value))
 
     def __str__(self):
         return RRType.to_text(self)
 
     def __repr__(self):
         return self.__str__()
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/loader.py` & `dnsmule-0.5.0/src/dnsmule/loader.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,80 +1,28 @@
-from dataclasses import dataclass
 from functools import partial
 from pathlib import Path
-from typing import Dict, List, Any, Type, TypeVar, Union, Optional, cast, Callable, Generic
+from typing import Dict, List, Any, Type, TypeVar, Union, cast, TYPE_CHECKING, Callable
 
 from .backends import Backend
-from .backends.noop import NOOPBackend
-from .config import get_logger
 from .definitions import RRType
+from .logger import get_logger
 from .plugins import Plugin
 from .rules import Rules, DynamicRule
-from .rules.entities import RuleFactory
-
-T = TypeVar('T')
-
-
-@dataclass
-class Initializer(Generic[T]):
-    type: str
-    f: Callable[[...], T]
-
-    def __call__(self, *args, **kwargs):
-        return self.f(*args, **kwargs)
-
-
-@dataclass
-class Config:
-    rules: Optional[Initializer[Rules]]
-    backend: Optional[Initializer[Backend]]
-    plugins: Optional[List[Initializer[Plugin]]]
-
-
-def load_and_append_rule(
-        rules: Rules,
-        record: RRType,
-        rule_type: str,
-        config: Dict[str, Any],
-) -> None:
-    """Creates a rule from rule definition
-
-    Initializes any dynamic rules created and passes the add_rule callback to them
-    """
-    rule = rules.create_rule(rule_type, config)
-    if isinstance(rule, DynamicRule):
-        rule.init(cast(RuleFactory, partial(load_and_append_rule, rules)))
-    rules.add_rule(record, rule)
+from .storages import Storage
+from .storages.dictstorage import DictStorage
 
+if TYPE_CHECKING:  # pragma: nocover
+    from .mule import DNSMule
 
-def load_rules(config: List[Dict[str, Any]], rules: Rules = None) -> Rules:
-    """Loads rules from the rules element in rules.yml
-
-    Provider rules in case of non-default handlers.
-    """
-    rules = Rules() if rules is None else rules
-    for rule_definition in config:
-        record = RRType.from_any(rule_definition['record'])
-        config = rule_definition.get('config', {})
-        rtype = rule_definition['type']
-        name = rule_definition['name']
-        if 'name' not in config:
-            config['name'] = name
-        if not rules.has_rule(record, name):
-            try:
-                load_and_append_rule(rules, record, rtype, config)
-            except KeyError as e:
-                get_logger().error(f'Failed to load rule: {rtype} RuleTypeNotFound({e})')
-        else:
-            raise ValueError(f'Can not add duplicate rule: {name} ({rtype})')
-    return rules
+T = TypeVar('T')
 
 
 def import_class(import_string: str, parent: Type[T], relative: bool = True, package: str = None) -> Type[T]:
-    """Imports a module and gets the last part as attribute from it
+    """
+    Imports a module and gets the last part as attribute from it
 
     **Note:** This allows arbitrary imports and code execution
     """
     module, _, cls = import_string.rpartition('.')
 
     import importlib
 
@@ -86,77 +34,124 @@
     cls = getattr(m, cls)
     if not issubclass(cls, parent):
         raise ImportError(f'Tried loading an incompatible class from {import_string} ({parent.__name__})')
     else:
         return cls
 
 
-def make_backend(document: Dict[str, Any]) -> Initializer[Backend]:
-    """Loads backend from yaml config
-    """
-    backend: Dict[str, Any] = document.get('backend', None)
-    if backend:
-        backend_type = backend['name']
-        backend_config = backend.get('config', {})
+def import_full(
+        name: str,
+        cls: Type[T],
+        package: str,
+) -> Type[T]:
+    """Helper for imports
+    """
+    try:
+        result = import_class(name, cls, relative=True, package=package)
+    except ImportError as e:
         try:
-            backend_class = import_class(backend_type, Backend, relative=True, package='dnsmule.backends')
-        except ImportError as e:
-            try:
-                backend_class = import_class(backend_type, Backend, relative=False)
-            except ImportError as ex:
-                raise ex from e
-            except AttributeError as ex:
-                raise ImportError from ex
-        except AttributeError as e:
-            raise ImportError from e
+            result = import_class(name, cls, relative=False)
+        except ImportError as ex:
+            raise ex from e
+        except AttributeError as ex:
+            raise ImportError from ex
+    except AttributeError as e:
+        raise ImportError from e
+    return result
 
-        return Initializer(type=backend_type, f=partial(backend_class, **backend_config))
-    else:
-        return Initializer(type=NOOPBackend.__name__, f=NOOPBackend)
 
+def load_and_append_rule(
+        rules: Rules,
+        record: RRType,
+        rule_type: str,
+        config: Dict[str, Any],
+) -> None:
+    """
+    Creates a rule from rule definition
 
-def make_rules(document: Dict[str, Any]) -> Initializer[Rules]:
-    """Loads rules from yaml config
+    Initializes any dynamic rules created and passes the add_rule callback to them
     """
-    config: List[Dict[str, Any]] = document.get('rules', [])
-    return Initializer(type='Rules', f=partial(load_rules, config))
+    rule = rules.create(rule_type, config)
+    if isinstance(rule, DynamicRule):
+        rule.init(cast(Callable[[RRType, str, Dict[str, Any]], None], partial(load_and_append_rule, rules)))
+    rules.append(record, rule)
 
 
-def make_plugins(document: Dict[str, Any]) -> List[Initializer[Plugin]]:
-    """Loads plugins from yaml config
-    """
-    plugins: List[Dict[str, Any]] = document.get('plugins', [])
-    out: List[Initializer[Plugin]] = []
-    for plugin in plugins:
-        plugin_type = plugin['name']
-        plugin_config = plugin.get('config', {})
-        try:
-            plugin_class = import_class(plugin_type, Plugin, relative=False)
-            out.append(Initializer(type=plugin_type, f=partial(plugin_class, **plugin_config)))
-        except ImportError as e:
-            get_logger().error(f'Failed to load plugin: {plugin_type} PluginNotFound({e})')
-    return out
+class ConfigLoader:
+    mule: 'DNSMule'
+    config: Dict[str, Union[List[Dict[str, Any]], Dict[str, Any]]]
 
+    def __init__(self, mule: 'DNSMule'):
+        self.mule = mule
 
-def load_config(
-        file: Union[str, Path],
-        rules: bool = True,
-        backend: bool = True,
-        plugins: bool = True,
-) -> Config:
-    """Loads a yaml config
-    """
-    import yaml
-    with open(file, 'r') as f:
-        document = yaml.safe_load(f)
-        return Config(
-            plugins=make_plugins(document) if plugins else None,
-            backend=make_backend(document) if backend else None,
-            rules=make_rules(document) if rules else None,
-        )
+    def set_storage(self):
+        storage_definition: Dict[str, Any] = self.config.get('storage', {})
+        if storage_definition:
+            storage_type = storage_definition['name']
+            try:
+                storage_class = import_full(storage_type, Storage, 'dnsmule.storages')
+                self.mule.storage = storage_class(**storage_definition.get('config', {}))
+            except Exception as e:
+                if storage_definition.get('fallback', False):
+                    self.mule.storage = DictStorage()
+                    get_logger().error(f'Failed to initialize storage {storage_type}', exc_info=e)
+                else:
+                    raise e
+
+    def set_backend(self):
+        backend_definition: Dict[str, Any] = self.config.get('backend', {})
+        if backend_definition:
+            backend_type = backend_definition['name']
+            backend_class = import_full(backend_type, Backend, 'dnsmule.backends')
+            self.mule.backend = backend_class(**backend_definition.get('config', {}))
+
+    def append_rules(self):
+        rule_definitions: List[Dict[str, Any]] = self.config.get('rules', [])
+        if rule_definitions:
+            for rule_definition in rule_definitions:
+                record = RRType.from_any(rule_definition['record'])
+                config = rule_definition.get('config', {})
+                rtype = rule_definition['type']
+                name = rule_definition['name']
+                if 'name' not in config:
+                    config['name'] = name
+                if not self.mule.rules.contains(record, name):
+                    try:
+                        load_and_append_rule(self.mule.rules, record, rtype, config)
+                    except KeyError as e:
+                        get_logger().error(f'Failed to load rule type {rtype}, {name}: {repr(e)}')
+                    except Exception as e:
+                        get_logger().error(f'Failed to load rule {rtype}, {name}', exc_info=e)
+                else:
+                    raise ValueError(f'Can not add duplicate rule: {name} ({rtype})')
+
+    def append_plugins(self):
+        plugin_definitions: List[Dict[str, Any]] = self.config.get('plugins', [])
+        if plugin_definitions:
+            for plugin in plugin_definitions:
+                plugin_type = plugin['name']
+                plugin_config = plugin.get('config', {})
+                try:
+                    plugin_class = import_class(plugin_type, Plugin, relative=False)
+                    if not self.mule.plugins.contains(plugin_class):
+                        plugin = plugin_class(**plugin_config)
+                        self.mule.plugins.add(plugin)
+                        plugin.register(self.mule)
+                except ImportError as e:
+                    get_logger().error(f'Failed to load plugin: {plugin_type}', exc_info=e)
+
+    def load_config(self, file: Union[str, Path]):
+        import yaml
+        with open(file, 'r') as f:
+            self.config = yaml.safe_load(f)
+
+    def all(self):
+        self.append_plugins()
+        self.append_rules()
+        self.set_storage()
+        self.set_backend()
 
 
 __all__ = [
-    'load_config',
-    'Config',
     'load_and_append_rule',
+    'ConfigLoader',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/rules/entities.py` & `dnsmule-0.5.0/src/dnsmule/rules/entities.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,69 +1,53 @@
-from typing import Dict, Callable, Any
+from typing import Callable, Optional, Union
 
+from ..baseclasses import KwargClass, Identifiable
 from ..definitions import RRType, Record, Result
-from ..utils import Comparable
 
-RuleFunction = Callable[[Record], Result]
+RuleFunction = Callable[[Record], Union[Result, None]]
 
 
-class Rule(metaclass=Comparable, key='priority', reverse=True):
+class Rule(KwargClass, Identifiable):
     """Wrapper class for rules to support priority based comparison
     """
     f: RuleFunction
-
     name: str = None
     priority: int = 0
 
     def __init__(self, f: RuleFunction = None, **kwargs):
-        super().__init__()
-        _keys = {
-            k: v
-            for k, v in kwargs.items()
-            if not k.startswith('_')
-        }
-        self.__dict__.update(_keys)
-        self._properties = [*_keys.keys()]
+        super(Rule, self).__init__(**kwargs)
         if 'name' not in self._properties:
             self._properties.insert(0, 'name')
         if f is not None and not callable(f):
             raise ValueError('Rule function not callable')
         elif f is None and type(self).__call__ is not Rule.__call__:
             self.f = self.__call__
         else:
             if f is None:
                 raise ValueError('Rule function was None')
             self.f = f
             self._properties.insert(1, 'f')
         if not self.name and hasattr(self.f, '__name__'):
             self.name = self.f.__name__
 
-    def __call__(self, record: Record):
+    def __call__(self, record: Record) -> Optional[Result]:
         if self.f == self.__call__:
             raise RecursionError('Illegal state, infinite recursion detected')
         return self.f(record)
 
-    def __repr__(self):
-        return self.__str__()
-
-    def __str__(self):
-        args = ','.join(
-            f'{k}={repr(getattr(self, k))}'
-            for k in self._properties
-        )
-        return f'{type(self).__name__}({args})'
-
     def __hash__(self):
         return hash(self.name)
 
     def __eq__(self, other: 'Rule'):
         return isinstance(other, Rule) and other.name == self.name or other == self.name
 
-
-RuleFactory = Callable[[RRType, str, Dict[str, Any]], Rule]
+    def __lt__(self, other):
+        """Supports comparison
+        """
+        return self.priority > other.priority
 
 
 class RuleCreator:
     """Helper for rule registration
     """
     priority: int
     type: str
@@ -91,10 +75,10 @@
         if self.type is not None:
             raise ValueError('Rule already has a type')
         return type(self)(self.callback, type=rtype)
 
 
 __all__ = [
     'Rule',
+    'RuleFunction',
     'RuleCreator',
-    'RuleFactory',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/rules/factories.py` & `dnsmule-0.5.0/src/dnsmule/rules/factories.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,37 +1,44 @@
-from typing import Dict, Any
+from typing import Dict, Any, Union, Type, Callable
 
-from .entities import Rule, RuleFactory
+from .entities import Rule
 from .ruletypes import DynamicRule, RegexRule
 
+RuleFactory = Union[Type[Rule], Callable[[...], Rule]]
+
 
 class RuleFactoryMixIn:
     _factories: Dict[str, RuleFactory]
 
     def __init__(self):
         self._factories = {}
-        add_default_factories(self)
+        self.register(RegexRule)
+        self.register(DynamicRule)
 
-    def create_rule(self, type_name: str, definition: Dict[str, Any]) -> Rule:
-        """Creates a rule from rule config
+    def create(self, type_name: str, definition: Dict[str, Any]) -> Rule:
+        """Creates a rule from rule logger
         """
         return self._factories[type_name](**definition)
 
-    def register(self, type_name: str):
+    def register(self, rule_type: Union[str, Type[Rule]]) -> Union[Callable[[RuleFactory], RuleFactory], Type[Rule]]:
         """Registers a handler for a rule type
         """
 
-        def decorator(f):
-            self._factories[type_name] = f
-            return f
-
-        return decorator
-
+        if isinstance(rule_type, type):
+            if not issubclass(rule_type, Rule):
+                raise TypeError('Not a Rule')
+            self._factories[rule_type.id] = rule_type
+
+            return rule_type
+        else:
+            def decorator(f: RuleFactory) -> RuleFactory:
+                self._factories[rule_type] = f
+                return f
 
-def add_default_factories(factory_storage: RuleFactoryMixIn) -> None:
-    factory_storage.register('dns.dynamic')(DynamicRule)
-    factory_storage.register('dns.regex')(RegexRule)
+            return decorator
 
 
 __all__ = [
     'RuleFactoryMixIn',
+    'RuleFactory',
+    'Rule',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/rules/rules.py` & `dnsmule-0.5.0/src/dnsmule/rules/rules.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,65 +1,76 @@
-from collections import defaultdict
-from typing import Dict, Union, List, Mapping
+from abc import ABC
+from typing import Dict, Union, List, Iterable, Tuple
 
 from .entities import Rule, RuleCreator
 from .factories import RuleFactoryMixIn
-from ..config import get_logger
-from ..definitions import Record, Result, RRType
+from ..definitions import Record, RRType
+from ..logger import get_logger
 
 
-class Rules(Mapping[Union[int, RRType], List[Rule]], RuleFactoryMixIn):
-    """Class for storing rules
-    """
+class RulesBase(RuleFactoryMixIn, ABC):
     _rules: Dict[Union[int, RRType], List[Rule]]
 
     def __init__(self):
-        super().__init__()
-        self.log = get_logger()
-        self._rules = defaultdict(list)
+        super(RulesBase, self).__init__()
+        self._rules = {}
 
-    async def process_record(self, record: Record) -> Result:
-        for r in self._rules.get(record.type, []):
+    def process(self, record: Record) -> None:
+        for rule in self._rules.get(record.type, []):
             try:
-                t = r(record)
-                if hasattr(t, '__await__'):
-                    await t
+                record.result += rule(record)
             except Exception as e:
-                self.log.error(f'Rule {r.name} raised an exception', exc_info=e)
-        return record.result()
+                get_logger().error(f'Rule {rule.name} raised an exception', exc_info=e)
 
-    def add_rule(self, rtype: Union[RRType, int, str], rule: Rule) -> None:
+    def append(self, record: Union[str, int, RRType], rule: Rule) -> None:
+        record = RRType.from_any(record)
+        if record not in self._rules:
+            self._rules[record] = []
+        if rule in self._rules[record]:
+            raise ValueError('Rule already exists')
+        self._rules[record].append(rule)
+        self._rules[record].sort()
+
+    def contains(self, record: Union[str, int, RRType], name: str) -> bool:
+        record = RRType.from_any(record)
+        return name in self._rules[record] if record in self._rules else False
+
+    def size(self):
+        return sum(len(c) for c in self._rules.values())
+
+    def get(self, rtype: Union[RRType, int, str]):
         rtype = RRType.from_any(rtype)
-        self._rules[rtype].append(rule)
-        self._rules[rtype].sort()
+        if rtype not in self._rules:
+            self._rules[rtype] = []
+        return self._rules[rtype]
 
-    def get_types(self) -> List[RRType]:
-        return [*self._rules.keys()]
+    def iterate(self) -> Iterable[Tuple[Union[int, RRType], List[Rule]]]:
+        yield from self._rules.items()
+
+    @property
+    def types(self) -> Iterable[RRType]:
+        return iter(self._rules.keys())
 
     @property
     def add(self) -> RuleCreator:
-        return RuleCreator(callback=self.add_rule)
+        return RuleCreator(callback=self.append)
 
-    def __getitem__(self, item: Union[RRType, int, str]) -> List[Rule]:
-        return self._rules[RRType.from_any(item)]
 
-    def __iter__(self):
-        yield from iter(self._rules)
+class Rules(RulesBase):
+
+    def __getitem__(self, key: Union[str, int, RRType]) -> List[Rule]:
+        return self.get(key)
 
     def __len__(self) -> int:
-        return len(self._rules)
+        return sum(map(len, self._rules.values()))
 
-    def __contains__(self, item: Union[int, RRType, str]):
-        return item in self._rules
+    def __iter__(self) -> Iterable[Tuple[Union[int, RRType], List[Rule]]]:
+        yield from self.iterate()
 
-    def has_rule(self, record: Union[int, RRType, str], name: str) -> bool:
-        record = RRType.from_any(record)
-        return name in self._rules[record] if record in self._rules else False
-
-    def rule_count(self):
-        return sum(len(c) for c in self._rules.values())
+    def keys(self):
+        yield from self._rules.keys()
 
 
 __all__ = [
     'Rules',
     'Rule',
 ]
```

### Comparing `dnsmule-0.1.0.post1/src/dnsmule/rules/ruletypes.py` & `dnsmule-0.5.0/src/dnsmule/rules/ruletypes.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 import functools
 import operator
 import re
-from typing import Any
-from typing import List
-from typing import Union
+from types import SimpleNamespace
+from typing import List, Union, Callable, Dict, Any
 
-from .entities import Rule, RuleFactory
-from ..definitions import Result, Record, RRType
+from .entities import Rule
+from ..definitions import Result, Record, RRType, Tag, Domain
 
 
 class RegexRule(Rule):
+    id = 'dns.regex'
+
     pattern: str
     patterns: List[str]
 
     identification: str = None
     flags: List[str] = None
-    attribute: str = 'to_text'
     group: Union[int, str] = None
 
     _patterns: List[re.Pattern]
 
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
         self.create_patterns()
@@ -37,58 +37,59 @@
 
         self._patterns = []
         if getattr(self, 'pattern', False):
             self._patterns.append(re.compile(self.pattern, flags=flags))
         if getattr(self, 'patterns', False):
             self._patterns.extend(re.compile(p, flags=flags) for p in self.patterns)
 
-    def get_attribute(self, record: Record):
-        """Resolves attribute from record
-
-        Also strips any leading or trailing quotes
-        """
-        attr = getattr(record.data, self.attribute)
-        if callable(attr):
-            out = str(attr())
-        else:
-            out = str(attr)
-        return out
-
     def __call__(self, record: Record):
         """Calls through all patterns and finds first identification
         """
         for p in self._patterns:
-            m = p.search(self.get_attribute(record))
+            m = p.search(record.text)
             if m:
                 _id = self.identification if self.group is None else m.group(self.group)
                 if _id:
                     _id = _id.upper()
                 else:
                     _id = 'UNKNOWN'
-                return record.identify(f'DNS::REGEX::{self.name.upper()}::{_id}')
+                record.tag(f'DNS::REGEX::{self.name.upper()}::{_id}')
+        return record.result
 
 
 class DynamicRule(Rule):
+    id = 'dns.dynamic'
+
     code: str
     globals: dict
 
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
         self.globals = {
             '__builtins__': __builtins__,
             'RRType': RRType,
             'Record': Record,
             'Result': Result,
+            'Domain': Domain,
+            'Tag': Tag,
+            'Config': SimpleNamespace(**self._kwargs)
         }
         if not self.code:
             raise ValueError('No code provided')
         self._code = compile(self.code, 'dynamic_rule.py', 'exec')
 
-    def init(self, create_callback: RuleFactory):
-        def add_rule(record_type: Any, rule_type: str, name: str, priority: int = 0, **options):
+    def init(self, create_callback: Callable[[Union[str, int, RRType], str, Dict[str, Any]], None]):
+        def add_rule(
+                record_type: Union[str, int, RRType],
+                rule_type: str,
+                name: str,
+                *,
+                priority: int = 0,
+                **options,
+        ):
             create_callback(
                 record_type,
                 rule_type,
                 {
                     **options,
                     'name': name,
                     'priority': priority,
```

