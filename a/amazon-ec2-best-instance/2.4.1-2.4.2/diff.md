# Comparing `tmp/amazon-ec2-best-instance-2.4.1.tar.gz` & `tmp/amazon-ec2-best-instance-2.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "amazon-ec2-best-instance-2.4.1.tar", last modified: Wed Dec 21 12:34:06 2022, max compression
+gzip compressed data, was "/Users/alexey/PycharmProjects/kankou-aliaksei/amazon-ec2-best-instance/dist/.tmp-qd4x97g3/amazon-ec2-best-instance-2.4.2.tar", last modified: Sat May 13 18:19:21 2023, max compression
```

## Comparing `amazon-ec2-best-instance-2.4.1.tar` & `amazon-ec2-best-instance-2.4.2.tar`

### file list

```diff
@@ -1,34 +1,39 @@
-drwxr-xr-x   0 alexey     (501) staff       (20)        0 2022-12-21 12:34:06.461005 amazon-ec2-best-instance-2.4.1/
--rw-r--r--   0 alexey     (501) staff       (20)     7179 2022-12-21 12:34:06.461130 amazon-ec2-best-instance-2.4.1/PKG-INFO
--rw-r--r--   0 alexey     (501) staff       (20)     6615 2022-11-02 12:46:54.000000 amazon-ec2-best-instance-2.4.1/README.md
--rw-r--r--   0 alexey     (501) staff       (20)        0 2022-08-12 10:25:37.000000 amazon-ec2-best-instance-2.4.1/pyproject.toml
--rw-r--r--   0 alexey     (501) staff       (20)      792 2022-12-21 12:34:06.461876 amazon-ec2-best-instance-2.4.1/setup.cfg
--rw-r--r--   0 alexey     (501) staff       (20)      184 2022-10-18 08:25:13.000000 amazon-ec2-best-instance-2.4.1/setup.py
-drwxr-xr-x   0 alexey     (501) staff       (20)        0 2022-12-21 12:34:06.445723 amazon-ec2-best-instance-2.4.1/src/
-drwxr-xr-x   0 alexey     (501) staff       (20)        0 2022-12-21 12:34:06.448523 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/
--rw-r--r--   0 alexey     (501) staff       (20)     1677 2022-10-04 19:38:00.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/SpotUtils.py
--rw-r--r--   0 alexey     (501) staff       (20)       67 2022-10-04 18:54:26.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/__init__.py
--rw-r--r--   0 alexey     (501) staff       (20)    20299 2022-12-21 09:40:38.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/main.py
-drwxr-xr-x   0 alexey     (501) staff       (20)        0 2022-12-21 12:34:06.450440 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/
--rw-r--r--   0 alexey     (501) staff       (20)     7179 2022-12-21 12:34:06.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/PKG-INFO
--rw-r--r--   0 alexey     (501) staff       (20)      669 2022-12-21 12:34:06.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/SOURCES.txt
--rw-r--r--   0 alexey     (501) staff       (20)        1 2022-12-21 12:34:06.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/dependency_links.txt
--rw-r--r--   0 alexey     (501) staff       (20)       41 2022-12-21 12:34:06.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/requires.txt
--rw-r--r--   0 alexey     (501) staff       (20)       25 2022-12-21 12:34:06.000000 amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/top_level.txt
-drwxr-xr-x   0 alexey     (501) staff       (20)        0 2022-12-21 12:34:06.460337 amazon-ec2-best-instance-2.4.1/test/
--rw-r--r--   0 alexey     (501) staff       (20)      914 2022-08-20 13:56:38.000000 amazon-ec2-best-instance-2.4.1/test/test.py
--rw-r--r--   0 alexey     (501) staff       (20)     1822 2022-08-20 16:08:45.000000 amazon-ec2-best-instance-2.4.1/test/test1.py
--rw-r--r--   0 alexey     (501) staff       (20)      870 2022-11-02 12:30:41.000000 amazon-ec2-best-instance-2.4.1/test/test10.py
--rw-r--r--   0 alexey     (501) staff       (20)     1008 2022-12-21 12:28:36.000000 amazon-ec2-best-instance-2.4.1/test/test11.py
--rw-r--r--   0 alexey     (501) staff       (20)     1250 2022-11-01 11:48:35.000000 amazon-ec2-best-instance-2.4.1/test/test2.py
--rw-r--r--   0 alexey     (501) staff       (20)      242 2022-08-20 17:07:35.000000 amazon-ec2-best-instance-2.4.1/test/test3.py
--rw-r--r--   0 alexey     (501) staff       (20)     1257 2022-08-20 17:08:57.000000 amazon-ec2-best-instance-2.4.1/test/test4.py
--rw-r--r--   0 alexey     (501) staff       (20)     1397 2022-10-05 10:35:11.000000 amazon-ec2-best-instance-2.4.1/test/test5.py
--rw-r--r--   0 alexey     (501) staff       (20)      804 2022-09-30 10:10:02.000000 amazon-ec2-best-instance-2.4.1/test/test6.py
--rw-r--r--   0 alexey     (501) staff       (20)     1720 2022-10-04 21:30:51.000000 amazon-ec2-best-instance-2.4.1/test/test7.py
--rw-r--r--   0 alexey     (501) staff       (20)     1154 2022-10-24 15:16:04.000000 amazon-ec2-best-instance-2.4.1/test/test8.py
--rw-r--r--   0 alexey     (501) staff       (20)      517 2022-10-24 16:57:53.000000 amazon-ec2-best-instance-2.4.1/test/test9.py
--rw-r--r--   0 alexey     (501) staff       (20)     1086 2022-10-24 16:35:41.000000 amazon-ec2-best-instance-2.4.1/test/test_azs.py
--rw-r--r--   0 alexey     (501) staff       (20)     1836 2022-10-24 16:41:05.000000 amazon-ec2-best-instance-2.4.1/test/test_cache.py
--rw-r--r--   0 alexey     (501) staff       (20)     1869 2022-10-24 16:41:05.000000 amazon-ec2-best-instance-2.4.1/test/test_cache_2.py
--rw-r--r--   0 alexey     (501) staff       (20)     2138 2022-10-14 12:24:54.000000 amazon-ec2-best-instance-2.4.1/test/test_clients.py
+drwxr-xr-x   0 alexey     (501) staff       (20)        0 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/
+-rw-r--r--   0 alexey     (501) staff       (20)     7179 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/PKG-INFO
+-rw-r--r--   0 alexey     (501) staff       (20)     6615 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/README.md
+-rw-r--r--   0 alexey     (501) staff       (20)        0 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/pyproject.toml
+-rw-r--r--   0 alexey     (501) staff       (20)      792 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/setup.cfg
+-rw-r--r--   0 alexey     (501) staff       (20)      184 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/setup.py
+drwxr-xr-x   0 alexey     (501) staff       (20)        0 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/
+drwxr-xr-x   0 alexey     (501) staff       (20)        0 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/
+-rw-r--r--   0 alexey     (501) staff       (20)     1677 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/SpotUtils.py
+-rw-r--r--   0 alexey     (501) staff       (20)       67 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/__init__.py
+-rw-r--r--   0 alexey     (501) staff       (20)    20934 2023-05-13 18:09:20.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/main.py
+drwxr-xr-x   0 alexey     (501) staff       (20)        0 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/
+-rw-r--r--   0 alexey     (501) staff       (20)     7179 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/PKG-INFO
+-rw-r--r--   0 alexey     (501) staff       (20)      774 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/SOURCES.txt
+-rw-r--r--   0 alexey     (501) staff       (20)        1 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/dependency_links.txt
+-rw-r--r--   0 alexey     (501) staff       (20)       41 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/requires.txt
+-rw-r--r--   0 alexey     (501) staff       (20)       25 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/top_level.txt
+drwxr-xr-x   0 alexey     (501) staff       (20)        0 2023-05-13 18:19:21.000000 amazon-ec2-best-instance-2.4.2/test/
+-rw-r--r--   0 alexey     (501) staff       (20)      914 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1822 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test1.py
+-rw-r--r--   0 alexey     (501) staff       (20)      870 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test10.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1008 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test11.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1250 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test2.py
+-rw-r--r--   0 alexey     (501) staff       (20)      242 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test3.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1257 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test4.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1397 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test5.py
+-rw-r--r--   0 alexey     (501) staff       (20)      804 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test6.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1720 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test7.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1154 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test8.py
+-rw-r--r--   0 alexey     (501) staff       (20)      517 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test9.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1086 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test_azs.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1996 2023-05-13 17:39:20.000000 amazon-ec2-best-instance-2.4.2/test/test_cache.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1869 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_2.py
+-rw-r--r--   0 alexey     (501) staff       (20)      938 2023-05-13 17:42:39.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_3.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1040 2023-05-13 17:54:23.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_4.py
+-rw-r--r--   0 alexey     (501) staff       (20)     1028 2023-05-13 17:55:02.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_5.py
+-rw-r--r--   0 alexey     (501) staff       (20)      638 2023-05-13 18:06:28.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_6.py
+-rw-r--r--   0 alexey     (501) staff       (20)      599 2023-05-13 18:07:20.000000 amazon-ec2-best-instance-2.4.2/test/test_cache_7.py
+-rw-r--r--   0 alexey     (501) staff       (20)     2138 2023-05-13 17:32:45.000000 amazon-ec2-best-instance-2.4.2/test/test_clients.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive
+POSIX tar archive (GNU)
```

### Comparing `amazon-ec2-best-instance-2.4.1/PKG-INFO` & `amazon-ec2-best-instance-2.4.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: amazon-ec2-best-instance
-Version: 2.4.1
+Version: 2.4.2
 Summary: Amazon EC2 Best Instance (amazon-ec2-best-instance) allows you to choose the most optimal and cheap EC2 instance type for on-demand and spot and with a less reclaimed rate for a spot instance.
 Home-page: https://github.com/kankou-aliaksei/amazon-ec2-best-instance
 Author: Aliaksei Kankou
 Author-email: aliaksei.kankou@gmail.com
 Project-URL: Bug Tracker, https://github.com/kankou-aliaksei/amazon-ec2-best-instance/issues
 Requires-Python: >3.7.0
 Description-Content-Type: text/markdown
```

### Comparing `amazon-ec2-best-instance-2.4.1/README.md` & `amazon-ec2-best-instance-2.4.2/README.md`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/setup.cfg` & `amazon-ec2-best-instance-2.4.2/setup.cfg`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = amazon-ec2-best-instance
-version = 2.4.1
+version = 2.4.2
 author = Aliaksei Kankou
 author_email = aliaksei.kankou@gmail.com
 description = Amazon EC2 Best Instance (amazon-ec2-best-instance) allows you to choose the most optimal and cheap EC2 instance type for on-demand and spot and with a less reclaimed rate for a spot instance.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/kankou-aliaksei/amazon-ec2-best-instance
 project_urls =
```

### Comparing `amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/SpotUtils.py` & `amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/SpotUtils.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance/main.py` & `amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance/main.py`

 * *Files 4% similar despite different names*

```diff
@@ -323,14 +323,17 @@
         if len(response['SpotPriceHistory']) == 0:
             return None
 
         history_events = response['SpotPriceHistory']
 
         az_price = {}
 
+        if availability_zones is None:
+            availability_zones = self.get_all_availability_zones_for_region()
+
         for i, availability_zone in enumerate(availability_zones):
             for history_event in history_events:
                 az = history_event['AvailabilityZone']
                 if availability_zone == az:
                     az_price[availability_zone] = history_event['SpotPrice']
                     break
 
@@ -452,18 +455,31 @@
         return records
 
     def __get_operating_systems_by_product_descriptions(self, product_descriptions):
         operating_systems = [self.__OS_PRODUCT_DESCRIPTION_MAP[product_description] for product_description in
                              product_descriptions]
         return Ec2BestInstance.unique(operating_systems)
 
+    def get_hash(self, dictionary):
+        dictionary_copy = dictionary.copy()
+        dictionary_copy['region'] = self.__region
+        dict_string = json.dumps(dictionary_copy)
+        hash_object = hashlib.md5(dict_string.encode())
+        return hash_object.hexdigest()
+
+    def get_all_availability_zones_for_region(self):
+        response = self.__ec2_client.describe_availability_zones()
+
+        availability_zones = []
+        for zone in response['AvailabilityZones']:
+            availability_zones.append(zone['ZoneName'])
+
+        if len(availability_zones) == 0:
+            raise Exception(f'Availability zones not found for the {self.__region} region')
+
+        return availability_zones
+
     @staticmethod
     def unique(list1):
         list_set = set(list1)
         unique_list = (list(list_set))
         return unique_list
-
-    @staticmethod
-    def get_hash(dictionary):
-        dict_string = json.dumps(dictionary)
-        hash_object = hashlib.md5(dict_string.encode())
-        return hash_object.hexdigest()
```

### Comparing `amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/PKG-INFO` & `amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: amazon-ec2-best-instance
-Version: 2.4.1
+Version: 2.4.2
 Summary: Amazon EC2 Best Instance (amazon-ec2-best-instance) allows you to choose the most optimal and cheap EC2 instance type for on-demand and spot and with a less reclaimed rate for a spot instance.
 Home-page: https://github.com/kankou-aliaksei/amazon-ec2-best-instance
 Author: Aliaksei Kankou
 Author-email: aliaksei.kankou@gmail.com
 Project-URL: Bug Tracker, https://github.com/kankou-aliaksei/amazon-ec2-best-instance/issues
 Requires-Python: >3.7.0
 Description-Content-Type: text/markdown
```

### Comparing `amazon-ec2-best-instance-2.4.1/src/amazon_ec2_best_instance.egg-info/SOURCES.txt` & `amazon-ec2-best-instance-2.4.2/src/amazon_ec2_best_instance.egg-info/SOURCES.txt`

 * *Files 20% similar despite different names*

```diff
@@ -21,8 +21,13 @@
 test/test6.py
 test/test7.py
 test/test8.py
 test/test9.py
 test/test_azs.py
 test/test_cache.py
 test/test_cache_2.py
+test/test_cache_3.py
+test/test_cache_4.py
+test/test_cache_5.py
+test/test_cache_6.py
+test/test_cache_7.py
 test/test_clients.py
```

### Comparing `amazon-ec2-best-instance-2.4.1/test/test.py` & `amazon-ec2-best-instance-2.4.2/test/test.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test1.py` & `amazon-ec2-best-instance-2.4.2/test/test1.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test10.py` & `amazon-ec2-best-instance-2.4.2/test/test10.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test11.py` & `amazon-ec2-best-instance-2.4.2/test/test11.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test2.py` & `amazon-ec2-best-instance-2.4.2/test/test2.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test4.py` & `amazon-ec2-best-instance-2.4.2/test/test4.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test5.py` & `amazon-ec2-best-instance-2.4.2/test/test5.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test6.py` & `amazon-ec2-best-instance-2.4.2/test/test6.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test7.py` & `amazon-ec2-best-instance-2.4.2/test/test7.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test8.py` & `amazon-ec2-best-instance-2.4.2/test/test8.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test9.py` & `amazon-ec2-best-instance-2.4.2/test/test9.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test_azs.py` & `amazon-ec2-best-instance-2.4.2/test/test_azs.py`

 * *Files identical despite different names*

### Comparing `amazon-ec2-best-instance-2.4.1/test/test_cache.py` & `amazon-ec2-best-instance-2.4.2/test/test_cache_2.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 import time
 
 from amazon_ec2_best_instance import Ec2BestInstance
 
-ec2_best_instance = Ec2BestInstance()
+ec2_best_instance = Ec2BestInstance({
+    'cache_ttl_in_minutes': 2
+})
 
 response = ec2_best_instance.get_best_instance_types({
     'vcpu': 16,
     'memory_gb': 20,
     'usage_class': 'spot',
     'burstable': False,
     'is_best_price': True,
```

### Comparing `amazon-ec2-best-instance-2.4.1/test/test_cache_2.py` & `amazon-ec2-best-instance-2.4.2/test/test_cache.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,17 @@
 import time
+import logging
 
 from amazon_ec2_best_instance import Ec2BestInstance
 
-ec2_best_instance = Ec2BestInstance({
-    'cache_ttl_in_minutes': 2
-})
+logging.basicConfig(level=logging.INFO, format='%(asctime)s: %(levelname)s: %(message)s')
+# Optional.
+logger = logging.getLogger()
+
+ec2_best_instance = Ec2BestInstance(logger=logger)
 
 response = ec2_best_instance.get_best_instance_types({
     'vcpu': 16,
     'memory_gb': 20,
     'usage_class': 'spot',
     'burstable': False,
     'is_best_price': True,
```

### Comparing `amazon-ec2-best-instance-2.4.1/test/test_clients.py` & `amazon-ec2-best-instance-2.4.2/test/test_clients.py`

 * *Files identical despite different names*

