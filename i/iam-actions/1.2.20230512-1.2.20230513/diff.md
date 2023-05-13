# Comparing `tmp/iam_actions-1.2.20230512.tar.gz` & `tmp/iam_actions-1.2.20230513.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "iam_actions-1.2.20230512.tar", max compression
+gzip compressed data, was "iam_actions-1.2.20230513.tar", max compression
```

## Comparing `iam_actions-1.2.20230512.tar` & `iam_actions-1.2.20230513.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0     1071 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/LICENSE
--rw-r--r--   0        0        0     2302 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/README.md
--rw-r--r--   0        0        0      228 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/__init__.py
--rw-r--r--   0        0        0  4252634 2023-05-12 02:26:03.608984 iam_actions-1.2.20230512/iam_actions/actions.json
--rw-r--r--   0        0        0      496 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/data.py
--rw-r--r--   0        0        0       80 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/__init__.py
--rw-r--r--   0        0        0     3097 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/action_map.py
--rw-r--r--   0        0        0    23329 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/aws_docs.py
--rw-r--r--   0        0        0     3739 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/generate.py
--rw-r--r--   0        0        0     3272 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/notifier.py
--rw-r--r--   0        0        0     1902 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/resource_type.py
--rw-r--r--   0        0        0     2277 2023-05-12 02:24:01.492382 iam_actions-1.2.20230512/iam_actions/generate/services.py
--rw-r--r--   0        0        0   546779 2023-05-12 02:26:03.608984 iam_actions-1.2.20230512/iam_actions/policies.json
--rw-r--r--   0        0        0   193791 2023-05-12 02:26:03.608984 iam_actions-1.2.20230512/iam_actions/resourcetypes.json
--rw-r--r--   0        0        0   530414 2023-05-12 02:26:03.608984 iam_actions-1.2.20230512/iam_actions/services.json
--rw-r--r--   0        0        0     1154 2023-05-12 02:26:04.456988 iam_actions-1.2.20230512/pyproject.toml
--rw-r--r--   0        0        0     3024 1970-01-01 00:00:00.000000 iam_actions-1.2.20230512/setup.py
--rw-r--r--   0        0        0     2915 1970-01-01 00:00:00.000000 iam_actions-1.2.20230512/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/LICENSE
+-rw-r--r--   0        0        0     2302 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/README.md
+-rw-r--r--   0        0        0      228 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/__init__.py
+-rw-r--r--   0        0        0  4253134 2023-05-13 02:25:58.575315 iam_actions-1.2.20230513/iam_actions/actions.json
+-rw-r--r--   0        0        0      496 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/data.py
+-rw-r--r--   0        0        0       80 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/__init__.py
+-rw-r--r--   0        0        0     3097 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/action_map.py
+-rw-r--r--   0        0        0    23329 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/aws_docs.py
+-rw-r--r--   0        0        0     3739 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/generate.py
+-rw-r--r--   0        0        0     3272 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/notifier.py
+-rw-r--r--   0        0        0     1902 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/resource_type.py
+-rw-r--r--   0        0        0     2277 2023-05-13 02:24:08.003716 iam_actions-1.2.20230513/iam_actions/generate/services.py
+-rw-r--r--   0        0        0   546948 2023-05-13 02:25:58.575315 iam_actions-1.2.20230513/iam_actions/policies.json
+-rw-r--r--   0        0        0   193815 2023-05-13 02:25:58.575315 iam_actions-1.2.20230513/iam_actions/resourcetypes.json
+-rw-r--r--   0        0        0   530553 2023-05-13 02:25:58.575315 iam_actions-1.2.20230513/iam_actions/services.json
+-rw-r--r--   0        0        0     1154 2023-05-13 02:25:59.331311 iam_actions-1.2.20230513/pyproject.toml
+-rw-r--r--   0        0        0     3024 1970-01-01 00:00:00.000000 iam_actions-1.2.20230513/setup.py
+-rw-r--r--   0        0        0     2915 1970-01-01 00:00:00.000000 iam_actions-1.2.20230513/PKG-INFO
```

### Comparing `iam_actions-1.2.20230512/LICENSE` & `iam_actions-1.2.20230513/LICENSE`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/README.md` & `iam_actions-1.2.20230513/README.md`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/actions.json` & `iam_actions-1.2.20230513/iam_actions/actions.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9998829117792573%*

 * *Differences: {"'elasticache'": "{'ModifyReplicationGroup': {'condition_keys': {insert: [(5, "*

 * *                  "'elasticache:ClusterModeEnabled')]}}}",*

 * * "'emr-containers'": "{'GetManagedEndpointSessionCredentials': OrderedDict([('access_level', "*

 * *                     "'Undocumented'), ('action', 'GetManagedEndpointSessionCredentials'), "*

 * *                     "('condition_keys', []), ('description', 'Not Documented by AWS'), ('orphan', "*

 * *                     "False), ('resources', [])])}",*

 * * "'mq'": "{'CreateReplicaBroke […]*

```diff
@@ -54222,14 +54222,15 @@
             "action": "ModifyReplicationGroup",
             "condition_keys": [
                 "aws:ResourceTag/${TagKey}",
                 "elasticache:AuthTokenEnabled",
                 "elasticache:AutomaticFailoverEnabled",
                 "elasticache:CacheNodeType",
                 "elasticache:CacheParameterGroupName",
+                "elasticache:ClusterModeEnabled",
                 "elasticache:EngineVersion",
                 "elasticache:MultiAZEnabled",
                 "elasticache:SnapshotRetentionLimit",
                 "elasticache:TransitEncryptionEnabled"
             ],
             "description": "Grants permission to modify the settings for a replication group",
             "orphan": false,
@@ -57308,14 +57309,22 @@
             "condition_keys": [],
             "description": "Grants permission to describe a virtual cluster",
             "orphan": false,
             "resources": [
                 "virtualCluster"
             ]
         },
+        "GetManagedEndpointSessionCredentials": {
+            "access_level": "Undocumented",
+            "action": "GetManagedEndpointSessionCredentials",
+            "condition_keys": [],
+            "description": "Not Documented by AWS",
+            "orphan": false,
+            "resources": []
+        },
         "ListJobRuns": {
             "access_level": "List",
             "action": "ListJobRuns",
             "condition_keys": [],
             "description": "Grants permission to list job runs associated with a virtual cluster",
             "orphan": false,
             "resources": [
@@ -99121,20 +99130,22 @@
                 "aws:TagKeys"
             ],
             "description": "Grants permission to create a new configuration for the specified configuration name. Amazon MQ uses the default configuration (the engine type and engine version)",
             "orphan": false,
             "resources": []
         },
         "CreateReplicaBroker": {
-            "access_level": "Undocumented",
+            "access_level": "Write",
             "action": "CreateReplicaBroker",
             "condition_keys": [],
-            "description": "Not Documented by AWS",
+            "description": "Grants permission to create a replica broker",
             "orphan": false,
-            "resources": []
+            "resources": [
+                "brokers"
+            ]
         },
         "CreateTags": {
             "access_level": "Tagging",
             "action": "CreateTags",
             "condition_keys": [
                 "aws:RequestTag/${TagKey}",
                 "aws:TagKeys"
@@ -142559,14 +142570,22 @@
             "orphan": false,
             "resources": [
                 "database",
                 "scheduled-query",
                 "table"
             ]
         },
+        "Unload": {
+            "access_level": "Undocumented",
+            "action": "Unload",
+            "condition_keys": [],
+            "description": "Not Documented by AWS",
+            "orphan": false,
+            "resources": []
+        },
         "UntagResource": {
             "access_level": "Tagging",
             "action": "UntagResource",
             "condition_keys": [
                 "aws:TagKeys"
             ],
             "description": "Grants permission to remove a tag from a resource",
```

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/action_map.py` & `iam_actions-1.2.20230513/iam_actions/generate/action_map.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/aws_docs.py` & `iam_actions-1.2.20230513/iam_actions/generate/aws_docs.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/generate.py` & `iam_actions-1.2.20230513/iam_actions/generate/generate.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/notifier.py` & `iam_actions-1.2.20230513/iam_actions/generate/notifier.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/resource_type.py` & `iam_actions-1.2.20230513/iam_actions/generate/resource_type.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/generate/services.py` & `iam_actions-1.2.20230513/iam_actions/generate/services.py`

 * *Files identical despite different names*

### Comparing `iam_actions-1.2.20230512/iam_actions/policies.json` & `iam_actions-1.2.20230513/iam_actions/policies.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9999769661854103%*

 * *Differences: {"'serviceMap'": "{'Amazon EMR on EKS (EMR Containers)': {'Actions': {insert: [(11, "*

 * *                 "'GetManagedEndpointSessionCredentials')]}}, 'AWS Outposts': {'conditionKeys': "*

 * *                 "['aws:RequestTag/${TagKey}', 'aws:ResourceTag/${TagKey}', 'aws:TagKeys']}, "*

 * *                 "'Amazon Timestream': {'Actions': {insert: [(29, 'Unload')]}}}"}*

```diff
@@ -6974,15 +6974,20 @@
                 "UntagResource",
                 "UpdateOutpost",
                 "UpdateSite",
                 "UpdateSiteAddress",
                 "UpdateSiteRackPhysicalProperties"
             ],
             "HasResource": true,
-            "StringPrefix": "outposts"
+            "StringPrefix": "outposts",
+            "conditionKeys": [
+                "aws:RequestTag/${TagKey}",
+                "aws:ResourceTag/${TagKey}",
+                "aws:TagKeys"
+            ]
         },
         "AWS Panorama": {
             "ARNFormat": "arn:aws:panorama:${Region}:${Account}:${ResourceType}/${ResourceName}",
             "ARNRegex": "^arn:aws:panorama:.+:.+:.+",
             "Actions": [
                 "CreateApplicationInstance",
                 "CreateJobForDevices",
@@ -12871,14 +12876,15 @@
                 "DeleteJobTemplate",
                 "DeleteManagedEndpoint",
                 "DeleteVirtualCluster",
                 "DescribeJobRun",
                 "DescribeJobTemplate",
                 "DescribeManagedEndpoint",
                 "DescribeVirtualCluster",
+                "GetManagedEndpointSessionCredentials",
                 "ListJobRuns",
                 "ListJobTemplates",
                 "ListManagedEndpoints",
                 "ListTagsForResource",
                 "ListVirtualClusters",
                 "StartJobRun",
                 "TagResource",
@@ -18883,14 +18889,15 @@
                 "PrepareQuery",
                 "ResumeBatchLoadTask",
                 "Select",
                 "SelectValues",
                 "StartAwsBackupJob",
                 "StartAwsRestoreJob",
                 "TagResource",
+                "Unload",
                 "UntagResource",
                 "UpdateDatabase",
                 "UpdateScheduledQuery",
                 "UpdateTable",
                 "WriteRecords"
             ],
             "HasResource": true,
```

### Comparing `iam_actions-1.2.20230512/iam_actions/resourcetypes.json` & `iam_actions-1.2.20230513/iam_actions/resourcetypes.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.999922624574435%*

 * *Differences: {"'gamelift'": "{'location': {'arn_pattern': 'arn:*:gamelift:*:*:location/*'}}",*

 * * "'logs'": "{'log-stream': {'condition_keys': 'aws:ResourceTag/${TagKey}'}}"}*

```diff
@@ -2800,15 +2800,15 @@
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
         "gameSessionQueue": {
             "arn_pattern": "arn:*:gamelift:*:*:gamesessionqueue/*",
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
         "location": {
-            "arn_pattern": "arn:*:gamelift:*::location/*",
+            "arn_pattern": "arn:*:gamelift:*:*:location/*",
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
         "matchmakingConfiguration": {
             "arn_pattern": "arn:*:gamelift:*:*:matchmakingconfiguration/*",
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
         "matchmakingRuleSet": {
@@ -3915,15 +3915,15 @@
         },
         "log-group": {
             "arn_pattern": "arn:*:logs:*:*:log-group:*",
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
         "log-stream": {
             "arn_pattern": "arn:*:logs:*:*:log-group:*:log-stream:*",
-            "condition_keys": null
+            "condition_keys": "aws:ResourceTag/${TagKey}"
         }
     },
     "lookoutequipment": {
         "dataset": {
             "arn_pattern": "arn:*:lookoutequipment:*:*:dataset/*/*",
             "condition_keys": "aws:ResourceTag/${TagKey}"
         },
```

### Comparing `iam_actions-1.2.20230512/iam_actions/services.json` & `iam_actions-1.2.20230513/iam_actions/services.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9998748176150684%*

 * *Differences: {"'emr-containers'": "{'Actions': {insert: [(11, 'GetManagedEndpointSessionCredentials')]}}",*

 * * "'outposts'": "{'ConditionKeys': ['aws:RequestTag/${TagKey}', 'aws:ResourceTag/${TagKey}', "*

 * *               "'aws:TagKeys']}",*

 * * "'timestream'": "{'Actions': {insert: [(29, 'Unload')]}}"}*

```diff
@@ -7825,14 +7825,15 @@
             "DeleteJobTemplate",
             "DeleteManagedEndpoint",
             "DeleteVirtualCluster",
             "DescribeJobRun",
             "DescribeJobTemplate",
             "DescribeManagedEndpoint",
             "DescribeVirtualCluster",
+            "GetManagedEndpointSessionCredentials",
             "ListJobRuns",
             "ListJobTemplates",
             "ListManagedEndpoints",
             "ListTagsForResource",
             "ListVirtualClusters",
             "StartJobRun",
             "TagResource",
@@ -14682,15 +14683,19 @@
             "TagResource",
             "UntagResource",
             "UpdateOutpost",
             "UpdateSite",
             "UpdateSiteAddress",
             "UpdateSiteRackPhysicalProperties"
         ],
-        "ConditionKeys": [],
+        "ConditionKeys": [
+            "aws:RequestTag/${TagKey}",
+            "aws:ResourceTag/${TagKey}",
+            "aws:TagKeys"
+        ],
         "HasResource": true,
         "ServiceNames": [
             "AWS Outposts"
         ]
     },
     "panorama": {
         "ARNFormats": [
@@ -19987,14 +19992,15 @@
             "PrepareQuery",
             "ResumeBatchLoadTask",
             "Select",
             "SelectValues",
             "StartAwsBackupJob",
             "StartAwsRestoreJob",
             "TagResource",
+            "Unload",
             "UntagResource",
             "UpdateDatabase",
             "UpdateScheduledQuery",
             "UpdateTable",
             "WriteRecords"
         ],
         "ConditionKeys": [
```

### Comparing `iam_actions-1.2.20230512/pyproject.toml` & `iam_actions-1.2.20230513/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "iam-actions"
-version = "1.2.20230512"
+version = "1.2.20230513"
 description = "JSON of AWS policy components"
 authors = ["Constable <info@constableapp.com>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/constableapp/iam_actions"
 packages = [{include = "iam_actions"}]
```

### Comparing `iam_actions-1.2.20230512/setup.py` & `iam_actions-1.2.20230513/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 ['iam_actions', 'iam_actions.generate']
 
 package_data = \
 {'': ['*']}
 
 setup_kwargs = {
     'name': 'iam-actions',
-    'version': '1.2.20230512',
+    'version': '1.2.20230513',
     'description': 'JSON of AWS policy components',
     'long_description': '# iam_actions\n\n`iam_actions` is a python module which contains a dictionary of AWS IAM information. Ideally, it is a complete catalog of all AWS services, actions, and resource types. The information is scraped from the AWS documentation pages.\n\nNightly, the scraping service runs, and publishes a new version with the date appended. \n\nThe package is meant to be used as a consumable package, but it also contains the code to generate the definitions for packaging.\n\nThere are three "roots" that you can consume: actions, resource_types, and services. They all currently return as dict\'s. *However, in a future release, it will be returned as python data structures*\n\n## Actions\n\nActions is a listing of all the actions for a given service. The structure is as follows:\n```\n{\n    "service_name": {\n        "action_name: {\n            "access_level": access_level,\n            "action": action_name,\n            "condition_keys": [condition_key1, ...],\n            "description": description\n        }\n    }\n}\n```\n\nTherefore, you can find information about an action as follows\n\n```\n>>> iam_actions.actions[\'s3\'][\'GetObject\']\n{\'access_level\': \'Read\', \'action\': \'GetObject\', \'condition_keys\': [\'s3:AccessPointNetworkOrigin\', \'s3:DataAccessPointAccount\', \'s3:DataAccessPointArn\', \'s3:ExistingObjectTag/<key>\', \'s3:ResourceAccount\', \'s3:TlsVersion\', \'s3:authType\', \'s3:signatureAge\', \'s3:signatureversion\', \'s3:x-amz-content-sha256\'], \'description\': \'Grants permission to retrieve objects from Amazon S3\', \'orphan\': False, \'resources\': [\'object\']}\n```\n\n## Services\n\nServices list information about the service. The structure is as follows:\n\n```\n{\n    "service_name": {\n        "Actions": [action1, ...]\n        "ServiceNames": [service_name1, ...]\n        "ARNFormats": [arn_format1, ...]\n        "ConditionKeys": [condition_key1, ...]\n        "HasResource": bool\n    }\n}\n```\n\n## Resource Types\n\nResource Types list information about the resource types for the service. The structure is as follows:\n\n```\n{\n    "service_name": {\n        "resource_name": {\n            "arn_pattern": arn_pattern,\n            "condition_keys": [condition_key1, ...]\n        }\n    }\n}\n```\n\n## Usage\n\n```python\nimport iam_actions\n\nprint(item_actions.services)\nprint(item_actions.actions)\nprint(item_actions.resource_types)\n```\n',
     'author': 'Constable',
     'author_email': 'info@constableapp.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/constableapp/iam_actions',
```

### Comparing `iam_actions-1.2.20230512/PKG-INFO` & `iam_actions-1.2.20230513/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iam-actions
-Version: 1.2.20230512
+Version: 1.2.20230513
 Summary: JSON of AWS policy components
 Home-page: https://github.com/constableapp/iam_actions
 License: MIT
 Author: Constable
 Author-email: info@constableapp.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

