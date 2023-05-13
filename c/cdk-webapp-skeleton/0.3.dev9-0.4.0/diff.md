# Comparing `tmp/cdk_webapp_skeleton-0.3.dev9.tar.gz` & `tmp/cdk_webapp_skeleton-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk_webapp_skeleton-0.3.dev9.tar", max compression
+gzip compressed data, was "cdk_webapp_skeleton-0.4.0.tar", max compression
```

## Comparing `cdk_webapp_skeleton-0.3.dev9.tar` & `cdk_webapp_skeleton-0.4.0.tar`

### file list

```diff
@@ -1,10 +1,11 @@
--rw-r--r--   0        0        0        0 2023-03-18 20:08:26.095902 cdk_webapp_skeleton-0.3.dev9/README.md
--rw-r--r--   0        0        0      357 2023-03-19 05:12:26.210544 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/__init__.py
--rw-r--r--   0        0        0     3546 2023-03-06 04:54:06.784822 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/auth_stack.py
--rw-r--r--   0        0        0     1544 2023-04-18 21:19:44.807699 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/branch_cicd_pipeline.py
--rw-r--r--   0        0        0     1909 2023-03-11 14:21:41.833987 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/branch_config.py
--rw-r--r--   0        0        0     4717 2023-03-19 05:12:26.218545 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/react_website.py
--rw-r--r--   0        0        0      344 2023-03-05 18:01:24.075619 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/test_utils.py
--rw-r--r--   0        0        0     4442 2023-04-18 23:59:14.698730 cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/webapp_lambda.py
--rw-r--r--   0        0        0      593 2023-04-18 23:59:14.686730 cdk_webapp_skeleton-0.3.dev9/pyproject.toml
--rw-r--r--   0        0        0      561 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.3.dev9/PKG-INFO
+-rw-r--r--   0        0        0       64 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/README.md
+-rw-r--r--   0        0        0      449 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/__init__.py
+-rw-r--r--   0        0        0     3546 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/auth_stack.py
+-rw-r--r--   0        0        0     1544 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/branch_cicd_pipeline.py
+-rw-r--r--   0        0        0     1909 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/branch_config.py
+-rw-r--r--   0        0        0     3124 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/monitored_lambda_function.py
+-rw-r--r--   0        0        0     4717 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/react_website.py
+-rw-r--r--   0        0        0      344 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/test_utils.py
+-rw-r--r--   0        0        0     4344 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/webapp_lambda.py
+-rw-r--r--   0        0        0     1315 2023-05-13 05:10:42.443941 cdk_webapp_skeleton-0.4.0/pyproject.toml
+-rw-r--r--   0        0        0      622 1970-01-01 00:00:00.000000 cdk_webapp_skeleton-0.4.0/PKG-INFO
```

### Comparing `cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/auth_stack.py` & `cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/auth_stack.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/branch_cicd_pipeline.py` & `cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/branch_cicd_pipeline.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/branch_config.py` & `cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/branch_config.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/react_website.py` & `cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/react_website.py`

 * *Files identical despite different names*

### Comparing `cdk_webapp_skeleton-0.3.dev9/cdk_webapp_skeleton/webapp_lambda.py` & `cdk_webapp_skeleton-0.4.0/cdk_webapp_skeleton/webapp_lambda.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,89 +1,71 @@
+import warnings
 from typing import Optional
 
+import aws_cdk as cdk
 from aws_cdk import aws_apigateway as apigateway
 from aws_cdk import aws_certificatemanager as certificatemanager
-from aws_cdk import aws_cloudwatch as cloudwatch
-from aws_cdk import aws_codeguruprofiler as codeguruprofiler
+from aws_cdk import aws_events as events
+from aws_cdk import aws_events_targets as events_targets
 from aws_cdk import aws_lambda as _lambda
-from aws_cdk import aws_logs as logs
 from aws_cdk import aws_route53 as route53
 from aws_cdk import aws_route53_targets as route53_targets
 from constructs import Construct
 
 from .branch_config import BranchConfig
+from .monitored_lambda_function import MonitoredLambdaFunction
 
 
 class WebappLambda(Construct):
     """Assumes a local folder called "webapp-backend" with a Dockerfile in it."""
 
     def __init__(
         self,
         scope: "Construct",
         _id: str,
         branch_config: BranchConfig,
-        image_directory="webapp-backend",
+        code: _lambda.DockerImageCode = None,
+        image_directory=None,
         lambda_runtime_environment=None,
         memory_size: Optional[int] = 256,
     ):
-        super().__init__(scope, _id)
-        if lambda_runtime_environment is None:
-            lambda_runtime_environment = {}
+        super().__init__(scope, branch_config.construct_id(_id) + "Construct")
 
-        profiling_group = codeguruprofiler.ProfilingGroup(
-            scope,
-            "FlaskLambdaProfiler",
-            compute_platform=codeguruprofiler.ComputePlatform.AWS_LAMBDA,
-        )
-
-        lambda_runtime_environment.update(
-            {
-                "AWS_CODEGURU_PROFILER_GROUP_ARN": profiling_group.profiling_group_arn,
-            }
-        )
+        warn_stacklevel = 3
+        if code is None:
+            if image_directory is None:
+                warnings.warn(
+                    'image_directory defaults to "webapp-backend", but this will be deprecated in favor of "code"',
+                    DeprecationWarning,
+                    stacklevel=warn_stacklevel,
+                )
+                image_directory = "webapp-backend"
+            else:
+                warnings.warn(
+                    '"image_directory" will be deprecated in favor of "code"',
+                    DeprecationWarning,
+                    stacklevel=warn_stacklevel,
+                )
+            code = _lambda.DockerImageCode.from_image_asset(directory=image_directory)
+        else:
+            if image_directory is not None:
+                warnings.warn(
+                    "image_directory is ignored when code is specified",
+                    RuntimeWarning,
+                    stacklevel=warn_stacklevel,
+                )
 
-        self.webapp_lambda_func = _lambda.DockerImageFunction(
+        self.monitored_lambda = MonitoredLambdaFunction(
             scope,
-            "FlaskLambda",
-            code=_lambda.DockerImageCode.from_image_asset(directory=image_directory),
-            environment=lambda_runtime_environment,
+            branch_config.construct_id(_id),
+            code=code,
+            lambda_runtime_environment=lambda_runtime_environment,
             memory_size=memory_size,
-            tracing=_lambda.Tracing.ACTIVE,
-        )
-        profiling_group.grant_publish(self.webapp_lambda_func)
-
-        logs.MetricFilter(
-            scope,
-            "FlaskLambdaTimeouts",
-            log_group=self.webapp_lambda_func.log_group,
-            filter_pattern=logs.FilterPattern.literal('"Task timed out"'),
-            metric_name="Timeouts",
-            metric_namespace="FlaskLambda",
-            metric_value="1",
-            default_value=0,
-            unit=cloudwatch.Unit.COUNT,
-        )
-
-        cloudwatch.Alarm(
-            scope,
-            "FlaskLambdaThrottles",
-            metric=self.webapp_lambda_func.metric_throttles(),
-            evaluation_periods=1,
-            threshold=0,
-            comparison_operator=cloudwatch.ComparisonOperator.GREATER_THAN_THRESHOLD,
-        )
-
-        cloudwatch.Alarm(
-            scope,
-            "FlaskLambdaErrors",
-            metric=self.webapp_lambda_func.metric_errors(),
-            evaluation_periods=1,
-            threshold=0,
-            comparison_operator=cloudwatch.ComparisonOperator.GREATER_THAN_THRESHOLD,
         )
+        self.webapp_lambda_func = self.monitored_lambda.lambda_function
 
         root_hosted_zone = branch_config.get_hosted_zone(scope)
         if root_hosted_zone is not None:
             backend_domain_name = "api." + branch_config.domain_name
 
             backend_certificate = certificatemanager.Certificate(
                 scope,
@@ -103,21 +85,29 @@
             lambda_gateway = apigateway.LambdaRestApi(
                 scope,
                 branch_config.construct_id("WebappBackendApi"),
                 handler=self.webapp_lambda_func,
                 domain_name=apigateway.DomainNameOptions(
                     domain_name=backend_domain_name, certificate=backend_certificate
                 ),
-                disable_execute_api_endpoint=True,
+                # Used by the RestApiWarmup event rule below.
+                disable_execute_api_endpoint=False,
                 default_cors_preflight_options=cors_options,
                 deploy_options=apigateway.StageOptions(
                     tracing_enabled=True,
                 ),
             )
 
+            events.Rule(
+                scope,
+                "RestApiWarmup",
+                targets=[events_targets.ApiGateway(lambda_gateway, retry_attempts=0)],
+                schedule=events.Schedule.rate(cdk.Duration.minutes(1)),
+            )
+
             route53.ARecord(
                 scope,
                 "BackendApiARecord",
                 zone=root_hosted_zone,
                 target=route53.RecordTarget.from_alias(
                     route53_targets.ApiGateway(lambda_gateway)
                 ),
```

### Comparing `cdk_webapp_skeleton-0.3.dev9/PKG-INFO` & `cdk_webapp_skeleton-0.4.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 Metadata-Version: 2.1
 Name: cdk-webapp-skeleton
-Version: 0.3.dev9
+Version: 0.4.0
 Summary: 
 Author: Ilya Nekhay
 Author-email: nekhayiv@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: aws-cdk-lib (>=2.67.0,<3.0.0)
 Requires-Dist: cloudcomponents-cdk-static-website (>=2.0.0,<3.0.0)
 Description-Content-Type: text/markdown
 
+Collection of reusable AWS CDK constructs for building webapps.
```

