# Comparing `tmp/azure_recommendations-0.3.2.tar.gz` & `tmp/azure_recommendations-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "azure_recommendations-0.3.2.tar", last modified: Fri May  5 06:56:48 2023, max compression
+gzip compressed data, was "azure_recommendations-0.3.3.tar", last modified: Sat May 13 15:13:50 2023, max compression
```

## Comparing `azure_recommendations-0.3.2.tar` & `azure_recommendations-0.3.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-05-05 06:56:48.778175 azure_recommendations-0.3.2/
--rw-rw-rw-   0        0        0        0 2023-03-24 12:23:56.000000 azure_recommendations-0.3.2/LICENCE
--rw-rw-rw-   0        0        0      533 2023-05-05 06:56:48.777181 azure_recommendations-0.3.2/PKG-INFO
--rw-rw-rw-   0        0        0      172 2023-03-24 12:23:56.000000 azure_recommendations-0.3.2/README.md
-drwxrwxrwx   0        0        0        0 2023-05-05 06:56:48.666175 azure_recommendations-0.3.2/azure_recommendations/
--rw-rw-rw-   0        0        0      602 2023-05-05 06:56:14.000000 azure_recommendations-0.3.2/azure_recommendations/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-05 06:56:48.775175 azure_recommendations-0.3.2/azure_recommendations/recommendation/
--rw-rw-rw-   0        0        0     7218 2023-05-05 06:34:46.000000 azure_recommendations-0.3.2/azure_recommendations/recommendation/__init__.py
--rw-rw-rw-   0        0        0     4848 2023-05-05 06:34:47.000000 azure_recommendations-0.3.2/azure_recommendations/recommendation/advisor_recommendations.py
--rw-rw-rw-   0        0        0    14586 2023-05-05 06:34:47.000000 azure_recommendations-0.3.2/azure_recommendations/recommendation/network_recommendations.py
--rw-rw-rw-   0        0        0    10016 2023-03-24 12:23:56.000000 azure_recommendations-0.3.2/azure_recommendations/recommendation/utils.py
--rw-rw-rw-   0        0        0    21180 2023-05-05 06:34:46.000000 azure_recommendations-0.3.2/azure_recommendations/recommendation/vm_recommendations.py
-drwxrwxrwx   0        0        0        0 2023-05-05 06:56:48.706177 azure_recommendations-0.3.2/azure_recommendations.egg-info/
--rw-rw-rw-   0        0        0      533 2023-05-05 06:56:48.000000 azure_recommendations-0.3.2/azure_recommendations.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      572 2023-05-05 06:56:48.000000 azure_recommendations-0.3.2/azure_recommendations.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-05 06:56:48.000000 azure_recommendations-0.3.2/azure_recommendations.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      142 2023-05-05 06:56:48.000000 azure_recommendations-0.3.2/azure_recommendations.egg-info/requires.txt
--rw-rw-rw-   0        0        0       22 2023-05-05 06:56:48.000000 azure_recommendations-0.3.2/azure_recommendations.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      718 2023-05-05 06:56:14.000000 azure_recommendations-0.3.2/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-05 06:56:48.779176 azure_recommendations-0.3.2/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 15:13:50.821438 azure_recommendations-0.3.3/
+-rw-rw-rw-   0        0        0        0 2023-03-24 12:23:56.000000 azure_recommendations-0.3.3/LICENCE
+-rw-rw-rw-   0        0        0      533 2023-05-13 15:13:50.819440 azure_recommendations-0.3.3/PKG-INFO
+-rw-rw-rw-   0        0        0      172 2023-03-24 12:23:56.000000 azure_recommendations-0.3.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 15:13:50.724440 azure_recommendations-0.3.3/azure_recommendations/
+-rw-rw-rw-   0        0        0      602 2023-05-13 15:13:20.000000 azure_recommendations-0.3.3/azure_recommendations/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:13:50.815438 azure_recommendations-0.3.3/azure_recommendations/recommendation/
+-rw-rw-rw-   0        0        0     7333 2023-05-13 15:13:20.000000 azure_recommendations-0.3.3/azure_recommendations/recommendation/__init__.py
+-rw-rw-rw-   0        0        0     4848 2023-05-05 06:34:47.000000 azure_recommendations-0.3.3/azure_recommendations/recommendation/advisor_recommendations.py
+-rw-rw-rw-   0        0        0    14586 2023-05-05 06:34:47.000000 azure_recommendations-0.3.3/azure_recommendations/recommendation/network_recommendations.py
+-rw-rw-rw-   0        0        0    10152 2023-05-13 14:55:05.000000 azure_recommendations-0.3.3/azure_recommendations/recommendation/utils.py
+-rw-rw-rw-   0        0        0    21178 2023-05-13 14:50:12.000000 azure_recommendations-0.3.3/azure_recommendations/recommendation/vm_recommendations.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:13:50.739439 azure_recommendations-0.3.3/azure_recommendations.egg-info/
+-rw-rw-rw-   0        0        0      533 2023-05-13 15:13:50.000000 azure_recommendations-0.3.3/azure_recommendations.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      572 2023-05-13 15:13:50.000000 azure_recommendations-0.3.3/azure_recommendations.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:13:50.000000 azure_recommendations-0.3.3/azure_recommendations.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      142 2023-05-13 15:13:50.000000 azure_recommendations-0.3.3/azure_recommendations.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       22 2023-05-13 15:13:50.000000 azure_recommendations-0.3.3/azure_recommendations.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      718 2023-05-13 15:13:20.000000 azure_recommendations-0.3.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:13:50.821438 azure_recommendations-0.3.3/setup.cfg
```

### Comparing `azure_recommendations-0.3.2/PKG-INFO` & `azure_recommendations-0.3.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: azure_recommendations
-Version: 0.3.2
+Version: 0.3.3
 Summary: Provides Azure recommendations
 Author-email: "dheeraj.banodha" <dheeraj.banodha@impetus.com>
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENCE
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations/__init__.py` & `azure_recommendations-0.3.3/azure_recommendations/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from azure_recommendations.recommendation import recommendation
 
 import logging
 logging.basicConfig(level=logging.INFO)
 logger = logging.getLogger()
 
 __author__ = 'Dheeraj Banodha'
-__version__ = '0.3.2'
+__version__ = '0.3.3'
 
 
 class az_session(recommendation):
     def __init__(self, tenant_id: str, client_id: str, client_secret: str):
         """
         :param tenant_id: tenant Id from Azure
         :param client_id: Access ID
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations/recommendation/__init__.py` & `azure_recommendations-0.3.3/azure_recommendations/recommendation/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -35,32 +35,35 @@
         :return: list of recommendations
         """
         logger.info(" ---Inside recommendation :: get_recommendations()--- ")
 
         response = []
 
         subscriptions = self.list_subscriptions()
-        print('subscriptions')
-        print(subscriptions)
+        # print('subscriptions')
+        # print(subscriptions)
 
         vm_list = self.list_vms(subscriptions)
-
+        # print(vm_list)
         response.extend(self.check_for_ssh_authentication_type(vm_list))
         response.extend(self.disable_premium_ssd(vm_list))
         response.extend(self.enable_auto_shutdown(vm_list))
 
         disk_list = self.list_disks(subscriptions)
+        # print(disk_list)
         response.extend(self.remove_unattached_disk_volume(disk_list))
 
         snapshot_list = self.list_snapshots(subscriptions)
+        # print(snapshot_list)
         response.extend(self.remove_old_vm_disk_snapshot(snapshot_list))
 
         response.extend(self.azure_advisor_recommendations(subscriptions))
 
         nsg_list = self.list_nsg(subscriptions)
+        # print(nsg_list)
         response.extend(self.unrestricted_access(nsg_list))
 
         return response
 
     def get_reserved_instance_recommendations(self) -> list:
         """
         :return: list of recommendations for the reserved instances
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations/recommendation/advisor_recommendations.py` & `azure_recommendations-0.3.3/azure_recommendations/recommendation/advisor_recommendations.py`

 * *Files identical despite different names*

### Comparing `azure_recommendations-0.3.2/azure_recommendations/recommendation/network_recommendations.py` & `azure_recommendations-0.3.3/azure_recommendations/recommendation/network_recommendations.py`

 * *Files identical despite different names*

### Comparing `azure_recommendations-0.3.2/azure_recommendations/recommendation/utils.py` & `azure_recommendations-0.3.3/azure_recommendations/recommendation/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -185,15 +185,18 @@
                 return {
                     'unitOfMeasure': None,
                     'retail_price': 0
                 }
 
             for item in response_json_obj['value']:
                 # print(item)
-                resource_id = item['properties']['resourceId']
+                try:
+                    resource_id = item['properties']['resourceId']
+                except KeyError as e:
+                    return {'unitOfMeasure': None, 'retail_price': 0}
 
                 if resource.id == resource_id:
                     meter_id = item['properties']['meterId']
                     flag = True
                     break
             if flag:
                 break
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations/recommendation/vm_recommendations.py` & `azure_recommendations-0.3.3/azure_recommendations/recommendation/vm_recommendations.py`

 * *Files 0% similar despite different names*

```diff
@@ -323,15 +323,15 @@
         for subscription, vms in vm_list.items():
             resource_client = ResourceManagementClient(credential=self.credentials, subscription_id=subscription)
             for vm in vms:
                 auto_shutdown_status = resource_client.resources.get_by_id(vm.id, '2022-11-01'). \
                     properties.get('autoShutdownSettings')
                 if auto_shutdown_status is None or auto_shutdown_status == 'Disabled':
                     price = utils_obj.get_price(vm, subscription_id=subscription)
-                    # print(price)
+                    print(price)
                     current_price = 0
                     if price['unitOfMeasure'] == '1 Hour':
                         current_price = 730 * price['retail_price']
 
                     effective_price = current_price * 0.6666
                     savings = current_price - effective_price
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations.egg-info/PKG-INFO` & `azure_recommendations-0.3.3/azure_recommendations.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: azure-recommendations
-Version: 0.3.2
+Version: 0.3.3
 Summary: Provides Azure recommendations
 Author-email: "dheeraj.banodha" <dheeraj.banodha@impetus.com>
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENCE
```

### Comparing `azure_recommendations-0.3.2/azure_recommendations.egg-info/SOURCES.txt` & `azure_recommendations-0.3.3/azure_recommendations.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `azure_recommendations-0.3.2/pyproject.toml` & `azure_recommendations-0.3.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "azure_recommendations"
-version = "0.3.2"
+version = "0.3.3"
 authors = [
   { name="dheeraj.banodha", email="dheeraj.banodha@impetus.com" },
 ]
 description = "Provides Azure recommendations"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

