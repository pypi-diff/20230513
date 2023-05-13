# Comparing `tmp/cdk_webapp_skeleton-0.4.1.dev3.tar.gz` & `tmp/cdk_webapp_skeleton-0.4.1.dev4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk_webapp_skeleton-0.4.1.dev3.tar", max compression
+gzip compressed data, was "cdk_webapp_skeleton-0.4.1.dev4.tar", max compression
```

## Comparing `cdk_webapp_skeleton-0.4.1.dev3.tar` & `cdk_webapp_skeleton-0.4.1.dev4.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0       64 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/README.md
--rw-r--r--   0        0        0      449 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/__init__.py
--rw-r--r--   0        0        0     3546 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/auth_stack.py
--rw-r--r--   0        0        0     2158 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_cicd_pipeline.py
--rw-r--r--   0        0        0     2089 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_config.py
--rw-r--r--   0        0        0     3621 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/monitored_lambda_function.py
--rw-r--r--   0        0        0     4725 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/react_website.py
--rw-r--r--   0        0        0      344 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/test_utils.py
--rw-r--r--   0        0        0     4466 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/webapp_lambda.py
--rw-r--r--   0        0        0     1473 2023-05-13 17:43:47.973719 cdk_webapp_skeleton-0.4.1.dev3/pyproject.toml
--rw-r--r--   0        0        0      627 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.4.1.dev3/PKG-INFO
+-rw-r--r--   0        0        0       64 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/README.md
+-rw-r--r--   0        0        0      449 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/__init__.py
+-rw-r--r--   0        0        0     3546 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/auth_stack.py
+-rw-r--r--   0        0        0     2159 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/branch_cicd_pipeline.py
+-rw-r--r--   0        0        0     2089 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/branch_config.py
+-rw-r--r--   0        0        0     3621 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/monitored_lambda_function.py
+-rw-r--r--   0        0        0     4725 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/react_website.py
+-rw-r--r--   0        0        0      344 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/test_utils.py
+-rw-r--r--   0        0        0     4466 2023-05-13 19:40:31.358782 cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/webapp_lambda.py
+-rw-r--r--   0        0        0     1473 2023-05-13 19:40:58.083210 cdk_webapp_skeleton-0.4.1.dev4/pyproject.toml
+-rw-r--r--   0        0        0      627 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.4.1.dev4/PKG-INFO
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/auth_stack.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/auth_stack.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_cicd_pipeline.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/branch_cicd_pipeline.py`

 * *Files 1% similar despite different names*

```diff
@@ -40,15 +40,15 @@
                 ),
                 cache=codebuild.Cache.bucket(cache_bucket),
             ),
             cross_account_keys=False,
             publish_assets_in_parallel=False,
         )
 
-        self.alarm_topic = sns.Topic(self, "AlarmTopic")
+        self.alarm_topic = sns.Topic(scope, "AlarmTopic")
         if branch_config.notify_email is not None:
             self.alarm_topic.add_subscription(
                 subscriptions.EmailSubscription(branch_config.notify_email)
             )
 
     def add_stage(self, stage: cdk.Stage) -> pipelines.StageDeployment:
         return self.cdk_pipeline.add_stage(stage)
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_config.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/branch_config.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/monitored_lambda_function.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/monitored_lambda_function.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/react_website.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/react_website.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/webapp_lambda.py` & `cdk_webapp_skeleton-0.4.1.dev4/cdk_webapp_skeleton/webapp_lambda.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/pyproject.toml` & `cdk_webapp_skeleton-0.4.1.dev4/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "cdk-webapp-skeleton"
-version = "0.4.1.dev3"
+version = "0.4.1.dev4"
 description = ""
 authors = ["Ilya Nekhay <nekhayiv@gmail.com>"]
 readme = "README.md"
 packages = [{include = "cdk_webapp_skeleton"}]
 
 [tool.poetry.dependencies]
 python = "^3.8"
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev3/PKG-INFO` & `cdk_webapp_skeleton-0.4.1.dev4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-webapp-skeleton
-Version: 0.4.1.dev3
+Version: 0.4.1.dev4
 Summary: 
 Author: Ilya Nekhay
 Author-email: nekhayiv@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

