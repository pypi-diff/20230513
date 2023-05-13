# Comparing `tmp/cdk_webapp_skeleton-0.4.1.dev2.tar.gz` & `tmp/cdk_webapp_skeleton-0.4.1.dev3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk_webapp_skeleton-0.4.1.dev2.tar", max compression
+gzip compressed data, was "cdk_webapp_skeleton-0.4.1.dev3.tar", max compression
```

## Comparing `cdk_webapp_skeleton-0.4.1.dev2.tar` & `cdk_webapp_skeleton-0.4.1.dev3.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0       64 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/README.md
--rw-r--r--   0        0        0      449 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/__init__.py
--rw-r--r--   0        0        0     3546 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/auth_stack.py
--rw-r--r--   0        0        0     2158 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/branch_cicd_pipeline.py
--rw-r--r--   0        0        0     2089 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/branch_config.py
--rw-r--r--   0        0        0     3124 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/monitored_lambda_function.py
--rw-r--r--   0        0        0     4725 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/react_website.py
--rw-r--r--   0        0        0      344 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/test_utils.py
--rw-r--r--   0        0        0     4344 2023-05-13 15:48:01.329155 cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/webapp_lambda.py
--rw-r--r--   0        0        0     1321 2023-05-13 15:48:20.377338 cdk_webapp_skeleton-0.4.1.dev2/pyproject.toml
--rw-r--r--   0        0        0      627 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.4.1.dev2/PKG-INFO
+-rw-r--r--   0        0        0       64 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/README.md
+-rw-r--r--   0        0        0      449 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/__init__.py
+-rw-r--r--   0        0        0     3546 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/auth_stack.py
+-rw-r--r--   0        0        0     2158 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_cicd_pipeline.py
+-rw-r--r--   0        0        0     2089 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_config.py
+-rw-r--r--   0        0        0     3621 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/monitored_lambda_function.py
+-rw-r--r--   0        0        0     4725 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/react_website.py
+-rw-r--r--   0        0        0      344 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/test_utils.py
+-rw-r--r--   0        0        0     4466 2023-05-13 17:43:27.549418 cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/webapp_lambda.py
+-rw-r--r--   0        0        0     1473 2023-05-13 17:43:47.973719 cdk_webapp_skeleton-0.4.1.dev3/pyproject.toml
+-rw-r--r--   0        0        0      627 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.4.1.dev3/PKG-INFO
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/auth_stack.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/auth_stack.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/branch_cicd_pipeline.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_cicd_pipeline.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/branch_config.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/branch_config.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/monitored_lambda_function.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/monitored_lambda_function.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,26 +1,29 @@
 from typing import Dict, Optional
 
 import aws_cdk as cdk
 from aws_cdk import aws_cloudwatch as cloudwatch
+from aws_cdk import aws_cloudwatch_actions as cloudwatch_actions
 from aws_cdk import aws_codeguruprofiler as codeguruprofiler
 from aws_cdk import aws_lambda as _lambda
 from aws_cdk import aws_logs as logs
+from aws_cdk import aws_sns as sns
 from constructs import Construct
 
 
 class MonitoredLambdaFunction(Construct):
     def __init__(
         self,
         scope: "Construct",
         _id: str,
         code: _lambda.DockerImageCode = None,
         lambda_runtime_environment: Optional[Dict] = None,
         memory_size: Optional[int] = 256,
         timeout: Optional[cdk.Duration] = None,
+        alarm_topic: Optional[sns.ITopic] = None,
     ):
         super().__init__(scope, _id + "Monitor")
         if lambda_runtime_environment is None:
             lambda_runtime_environment = {}
         else:
             lambda_runtime_environment = lambda_runtime_environment.copy()
 
@@ -57,36 +60,41 @@
             metric_name="Timeouts",
             metric_namespace=_id,
             metric_value="1",
             default_value=0,
             unit=cloudwatch.Unit.COUNT,
         )
 
-        cloudwatch.Alarm(
+        throttles_alarm = cloudwatch.Alarm(
             scope,
             _id + "Throttles",
             metric=self.lambda_function.metric_throttles(),
             evaluation_periods=1,
             threshold=0,
             comparison_operator=cloudwatch.ComparisonOperator.GREATER_THAN_THRESHOLD,
             treat_missing_data=cloudwatch.TreatMissingData.IGNORE,
         )
 
-        cloudwatch.Alarm(
+        errors_alarm = cloudwatch.Alarm(
             scope,
             _id + "Errors",
             metric=self.lambda_function.metric_errors(),
             evaluation_periods=1,
             threshold=0,
             comparison_operator=cloudwatch.ComparisonOperator.GREATER_THAN_THRESHOLD,
             treat_missing_data=cloudwatch.TreatMissingData.IGNORE,
         )
 
-        cloudwatch.Alarm(
+        timeouts_alarm = cloudwatch.Alarm(
             scope,
             _id + "Timeouts",
             metric=timeouts_metric_filter.metric(statistic=cloudwatch.Stats.SUM),
             evaluation_periods=1,
             threshold=0,
             comparison_operator=cloudwatch.ComparisonOperator.GREATER_THAN_THRESHOLD,
             treat_missing_data=cloudwatch.TreatMissingData.IGNORE,
         )
+
+        if alarm_topic is not None:
+            throttles_alarm.add_alarm_action(cloudwatch_actions.SnsAction(alarm_topic))
+            errors_alarm.add_alarm_action(cloudwatch_actions.SnsAction(alarm_topic))
+            timeouts_alarm.add_alarm_action(cloudwatch_actions.SnsAction(alarm_topic))
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/react_website.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/react_website.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/cdk_webapp_skeleton/webapp_lambda.py` & `cdk_webapp_skeleton-0.4.1.dev3/cdk_webapp_skeleton/webapp_lambda.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 from aws_cdk import aws_apigateway as apigateway
 from aws_cdk import aws_certificatemanager as certificatemanager
 from aws_cdk import aws_events as events
 from aws_cdk import aws_events_targets as events_targets
 from aws_cdk import aws_lambda as _lambda
 from aws_cdk import aws_route53 as route53
 from aws_cdk import aws_route53_targets as route53_targets
+from aws_cdk import aws_sns as sns
 from constructs import Construct
 
 from .branch_config import BranchConfig
 from .monitored_lambda_function import MonitoredLambdaFunction
 
 
 class WebappLambda(Construct):
@@ -23,14 +24,15 @@
         scope: "Construct",
         _id: str,
         branch_config: BranchConfig,
         code: _lambda.DockerImageCode = None,
         image_directory=None,
         lambda_runtime_environment=None,
         memory_size: Optional[int] = 256,
+        alarm_topic: Optional[sns.ITopic] = None,
     ):
         super().__init__(scope, branch_config.construct_id(_id) + "Construct")
 
         warn_stacklevel = 3
         if code is None:
             if image_directory is None:
                 warnings.warn(
@@ -56,14 +58,15 @@
 
         self.monitored_lambda = MonitoredLambdaFunction(
             scope,
             branch_config.construct_id(_id),
             code=code,
             lambda_runtime_environment=lambda_runtime_environment,
             memory_size=memory_size,
+            alarm_topic=alarm_topic,
         )
         self.webapp_lambda_func = self.monitored_lambda.lambda_function
 
         root_hosted_zone = branch_config.get_hosted_zone(scope)
         if root_hosted_zone is not None:
             backend_domain_name = "api." + branch_config.domain_name
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/pyproject.toml` & `cdk_webapp_skeleton-0.4.1.dev3/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "cdk-webapp-skeleton"
-version = "0.4.1.dev2"
+version = "0.4.1.dev3"
 description = ""
 authors = ["Ilya Nekhay <nekhayiv@gmail.com>"]
 readme = "README.md"
 packages = [{include = "cdk_webapp_skeleton"}]
 
 [tool.poetry.dependencies]
 python = "^3.8"
@@ -37,14 +37,16 @@
 version_type = "pep440"
 version_provider = "poetry"
 update_changelog_on_bump = true
 major_version_zero = true
 
 [tool.poetry-dynamic-versioning]
 enable = false
+# TODO: extract version from `cz bump` so that when there's a MINOR/MAJOR change coming, the dev version corresponds
+#  to the next MINOR/MAJOR version
 format-jinja = """
     {%- if distance == 0 -%}
         {{ serialize_pep440(base, stage, revision) }}
     {%- elif revision is not none -%}
         {{ serialize_pep440(base, stage, revision + 1, dev=distance) }}
     {%- else -%}
         {{ serialize_pep440(bump_version(base), stage, revision, dev=distance) }}
```

### Comparing `cdk_webapp_skeleton-0.4.1.dev2/PKG-INFO` & `cdk_webapp_skeleton-0.4.1.dev3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-webapp-skeleton
-Version: 0.4.1.dev2
+Version: 0.4.1.dev3
 Summary: 
 Author: Ilya Nekhay
 Author-email: nekhayiv@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

