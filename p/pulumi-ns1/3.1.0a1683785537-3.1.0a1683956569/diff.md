# Comparing `tmp/pulumi_ns1-3.1.0a1683785537.tar.gz` & `tmp/pulumi_ns1-3.1.0a1683956569.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pulumi_ns1-3.1.0a1683785537.tar", last modified: Thu May 11 06:21:12 2023, max compression
+gzip compressed data, was "pulumi_ns1-3.1.0a1683956569.tar", last modified: Sat May 13 05:50:37 2023, max compression
```

## Comparing `pulumi_ns1-3.1.0a1683785537.tar` & `pulumi_ns1-3.1.0a1683956569.tar`

### file list

```diff
@@ -1,41 +1,41 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/
--rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/
--rw-r--r--   0 runner    (1001) docker     (123)     3042 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    30487 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)    83734 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/api_key.py
--rw-r--r--   0 runner    (1001) docker     (123)    17715 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/application.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/config/
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/config/vars.py
--rw-r--r--   0 runner    (1001) docker     (123)    12324 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/data_feed.py
--rw-r--r--   0 runner    (1001) docker     (123)    11022 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/data_source.py
--rw-r--r--   0 runner    (1001) docker     (123)    13624 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/dnsview.py
--rw-r--r--   0 runner    (1001) docker     (123)     4031 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_dns_sec.py
--rw-r--r--   0 runner    (1001) docker     (123)     2406 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_networks.py
--rw-r--r--   0 runner    (1001) docker     (123)     8256 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_record.py
--rw-r--r--   0 runner    (1001) docker     (123)    10637 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_zone.py
--rw-r--r--   0 runner    (1001) docker     (123)    45700 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/monitoring_job.py
--rw-r--r--   0 runner    (1001) docker     (123)    10871 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/notify_list.py
--rw-r--r--   0 runner    (1001) docker     (123)    38381 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/outputs.py
--rw-r--r--   0 runner    (1001) docker     (123)    10590 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/provider.py
--rw-r--r--   0 runner    (1001) docker     (123)    17050 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/pulsar_job.py
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/pulumi-plugin.json
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    33237 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/record.py
--rw-r--r--   0 runner    (1001) docker     (123)    19239 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/subnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    81290 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/team.py
--rw-r--r--   0 runner    (1001) docker     (123)     9970 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/tsigkey.py
--rw-r--r--   0 runner    (1001) docker     (123)    85038 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/user.py
--rw-r--r--   0 runner    (1001) docker     (123)    41456 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1/zone.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      863 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 06:21:12.939162 pulumi_ns1-3.1.0a1683785537/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2097 2023-05-11 06:21:12.000000 pulumi_ns1-3.1.0a1683785537/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/
+-rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3042 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30487 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)    83734 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/api_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17715 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/application.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/config/
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/config/vars.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12324 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/data_feed.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11022 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/data_source.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13624 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/dnsview.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4031 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_dns_sec.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2406 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_networks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8256 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10637 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_zone.py
+-rw-r--r--   0 runner    (1001) docker     (123)    45700 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/monitoring_job.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10871 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/notify_list.py
+-rw-r--r--   0 runner    (1001) docker     (123)    38381 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10590 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17050 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/pulsar_job.py
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/pulumi-plugin.json
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    33237 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/record.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19239 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/subnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81290 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/team.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9970 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/tsigkey.py
+-rw-r--r--   0 runner    (1001) docker     (123)    85038 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/user.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41456 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1/zone.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      863 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 05:50:37.610158 pulumi_ns1-3.1.0a1683956569/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2097 2023-05-13 05:50:37.000000 pulumi_ns1-3.1.0a1683956569/setup.py
```

### Comparing `pulumi_ns1-3.1.0a1683785537/PKG-INFO` & `pulumi_ns1-3.1.0a1683956569/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi_ns1
-Version: 3.1.0a1683785537
+Version: 3.1.0a1683956569
 Summary: A Pulumi package for creating and managing ns1 cloud resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-ns1
 Keywords: pulumi ns1
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `pulumi_ns1-3.1.0a1683785537/README.md` & `pulumi_ns1-3.1.0a1683956569/README.md`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/__init__.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/_inputs.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/_utilities.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/_utilities.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/api_key.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/api_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/application.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/application.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/config/vars.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/config/vars.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/data_feed.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/data_feed.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/data_source.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/data_source.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/dnsview.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/dnsview.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_dns_sec.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_dns_sec.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_networks.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_networks.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_record.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_record.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/get_zone.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/get_zone.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/monitoring_job.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/monitoring_job.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/notify_list.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/notify_list.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/outputs.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/provider.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/provider.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/pulsar_job.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/pulsar_job.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/record.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/record.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/subnet.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/subnet.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/team.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/team.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/tsigkey.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/tsigkey.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/user.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/user.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1/zone.py` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1/zone.py`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/PKG-INFO` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi-ns1
-Version: 3.1.0a1683785537
+Version: 3.1.0a1683956569
 Summary: A Pulumi package for creating and managing ns1 cloud resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-ns1
 Keywords: pulumi ns1
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `pulumi_ns1-3.1.0a1683785537/pulumi_ns1.egg-info/SOURCES.txt` & `pulumi_ns1-3.1.0a1683956569/pulumi_ns1.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pulumi_ns1-3.1.0a1683785537/setup.py` & `pulumi_ns1-3.1.0a1683956569/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 
 import errno
 from setuptools import setup, find_packages
 from setuptools.command.install import install
 from subprocess import check_call
 
 
-VERSION = "3.1.0a1683785537"
-PLUGIN_VERSION = "3.1.0-alpha.1683785537+1188c0ff"
+VERSION = "3.1.0a1683956569"
+PLUGIN_VERSION = "3.1.0-alpha.1683956569+066550b3"
 
 class InstallPluginCommand(install):
     def run(self):
         install.run(self)
         try:
             check_call(['pulumi', 'plugin', 'install', 'resource', 'ns1', PLUGIN_VERSION])
         except OSError as error:
```

