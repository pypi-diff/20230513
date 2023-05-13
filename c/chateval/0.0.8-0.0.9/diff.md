# Comparing `tmp/chateval-0.0.8.tar.gz` & `tmp/chateval-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chateval-0.0.8.tar", last modified: Fri Mar 31 17:41:29 2023, max compression
+gzip compressed data, was "chateval-0.0.9.tar", last modified: Fri Mar 31 18:15:51 2023, max compression
```

## Comparing `chateval-0.0.8.tar` & `chateval-0.0.9.tar`

### file list

```diff
@@ -1,67 +1,67 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)     4567 2023-03-31 17:41:29.745864 chateval-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3930 2023-03-31 17:40:37.000000 chateval-0.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.737864 chateval-0.0.8/chateval/
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3014 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/chateval.py
--rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.741864 chateval-0.0.8/chateval/constants/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/constants/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      470 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/constants/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.741864 chateval-0.0.8/chateval/kernels/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/kernels/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      540 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/kernels/kernel.py
--rw-r--r--   0 runner    (1001) docker     (123)     2343 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/kernels/openai.py
--rw-r--r--   0 runner    (1001) docker     (123)      627 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/kernels/openai_test.py
--rw-r--r--   0 runner    (1001) docker     (123)    39501 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/load.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.741864 chateval-0.0.8/chateval/metrics/
--rw-r--r--   0 runner    (1001) docker     (123)      732 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/accuracy.py
--rw-r--r--   0 runner    (1001) docker     (123)      689 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/count.py
--rw-r--r--   0 runner    (1001) docker     (123)    13888 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/gptscore.py
--rw-r--r--   0 runner    (1001) docker     (123)      344 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/metric.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.741864 chateval-0.0.8/chateval/metrics/protocols/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/protocols/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/protocols/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      937 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/metrics/rouge.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.741864 chateval-0.0.8/chateval/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      274 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/download.py
--rw-r--r--   0 runner    (1001) docker     (123)    13825 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/extract.py
--rw-r--r--   0 runner    (1001) docker     (123)    21552 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/file_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    14244 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/filelock.py
--rw-r--r--   0 runner    (1001) docker     (123)     6760 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/naming.py
--rw-r--r--   0 runner    (1001) docker     (123)      424 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/prompt_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4350 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/py_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-03-31 17:40:37.000000 chateval-0.0.8/chateval/utils/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.737864 chateval-0.0.8/chateval.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4567 2023-03-31 17:41:29.000000 chateval-0.0.8/chateval.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-03-31 17:41:29.000000 chateval-0.0.8/chateval.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-31 17:41:29.000000 chateval-0.0.8/chateval.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       98 2023-03-31 17:41:29.000000 chateval-0.0.8/chateval.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       37 2023-03-31 17:41:29.000000 chateval-0.0.8/chateval.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/integration_tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/integration_tests/artifacts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/artifacts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      334 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/artifacts/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/integration_tests/artifacts/yaml_config/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/artifacts/yaml_config/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/integration_tests/artifacts/yaml_config/write_email/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/artifacts/yaml_config/write_email/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      501 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/chateval_class_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4151 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/gptscore_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-03-31 17:40:37.000000 chateval-0.0.8/integration_tests/metric_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/scenarios/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/scenarios/metaeval_helpfulness/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/metaeval_helpfulness/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      184 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/metaeval_helpfulness/metaeval_helpfulness.py
--rw-r--r--   0 runner    (1001) docker     (123)      505 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/metaeval_helpfulness/metaeval_helpfulness_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 17:41:29.745864 chateval-0.0.8/scenarios/write_email/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/write_email/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      166 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/write_email/write_email.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-03-31 17:40:37.000000 chateval-0.0.8/scenarios/write_email/write_email_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-03-31 17:41:29.745864 chateval-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-03-31 17:40:37.000000 chateval-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     8775 2023-03-31 18:15:51.160034 chateval-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8138 2023-03-31 18:15:13.000000 chateval-0.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.156034 chateval-0.0.9/chateval/
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3014 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/chateval.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval/constants/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/constants/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      470 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/constants/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval/kernels/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/kernels/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      540 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/kernels/kernel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2343 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/kernels/openai.py
+-rw-r--r--   0 runner    (1001) docker     (123)      627 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/kernels/openai_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39501 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/load.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval/metrics/
+-rw-r--r--   0 runner    (1001) docker     (123)      732 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/accuracy.py
+-rw-r--r--   0 runner    (1001) docker     (123)      689 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/count.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13888 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/gptscore.py
+-rw-r--r--   0 runner    (1001) docker     (123)      344 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/metric.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval/metrics/protocols/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/protocols/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      139 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/protocols/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      937 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/metrics/rouge.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      274 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13825 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/extract.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21552 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/file_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14244 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/filelock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6760 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/naming.py
+-rw-r--r--   0 runner    (1001) docker     (123)      424 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/prompt_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4350 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/py_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-03-31 18:15:13.000000 chateval-0.0.9/chateval/utils/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/chateval.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8775 2023-03-31 18:15:51.000000 chateval-0.0.9/chateval.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-03-31 18:15:51.000000 chateval-0.0.9/chateval.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-31 18:15:51.000000 chateval-0.0.9/chateval.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       98 2023-03-31 18:15:51.000000 chateval-0.0.9/chateval.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       37 2023-03-31 18:15:51.000000 chateval-0.0.9/chateval.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/integration_tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/integration_tests/artifacts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/artifacts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      334 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/artifacts/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/integration_tests/artifacts/yaml_config/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/artifacts/yaml_config/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/integration_tests/artifacts/yaml_config/write_email/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/artifacts/yaml_config/write_email/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      501 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/chateval_class_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4151 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/gptscore_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-03-31 18:15:13.000000 chateval-0.0.9/integration_tests/metric_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/scenarios/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/scenarios/metaeval_helpfulness/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/metaeval_helpfulness/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      184 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/metaeval_helpfulness/metaeval_helpfulness.py
+-rw-r--r--   0 runner    (1001) docker     (123)      505 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/metaeval_helpfulness/metaeval_helpfulness_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:51.160034 chateval-0.0.9/scenarios/write_email/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/write_email/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      166 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/write_email/write_email.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-03-31 18:15:13.000000 chateval-0.0.9/scenarios/write_email/write_email_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-03-31 18:15:51.160034 chateval-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-03-31 18:15:13.000000 chateval-0.0.9/setup.py
```

### Comparing `chateval-0.0.8/chateval/chateval.py` & `chateval-0.0.9/chateval/chateval.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/config.py` & `chateval-0.0.9/chateval/config.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/kernels/kernel.py` & `chateval-0.0.9/chateval/kernels/kernel.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/kernels/openai.py` & `chateval-0.0.9/chateval/kernels/openai.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/kernels/openai_test.py` & `chateval-0.0.9/chateval/kernels/openai_test.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/load.py` & `chateval-0.0.9/chateval/load.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/metrics/__init__.py` & `chateval-0.0.9/chateval/metrics/__init__.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/metrics/accuracy.py` & `chateval-0.0.9/chateval/metrics/accuracy.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/metrics/count.py` & `chateval-0.0.9/chateval/metrics/count.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/metrics/gptscore.py` & `chateval-0.0.9/chateval/metrics/gptscore.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/metrics/rouge.py` & `chateval-0.0.9/chateval/metrics/rouge.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/extract.py` & `chateval-0.0.9/chateval/utils/extract.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/file_utils.py` & `chateval-0.0.9/chateval/utils/file_utils.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/filelock.py` & `chateval-0.0.9/chateval/utils/filelock.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/logging.py` & `chateval-0.0.9/chateval/utils/logging.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/naming.py` & `chateval-0.0.9/chateval/utils/naming.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/py_util.py` & `chateval-0.0.9/chateval/utils/py_util.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval/utils/version.py` & `chateval-0.0.9/chateval/utils/version.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/chateval.egg-info/SOURCES.txt` & `chateval-0.0.9/chateval.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/integration_tests/gptscore_test.py` & `chateval-0.0.9/integration_tests/gptscore_test.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/integration_tests/metric_test.py` & `chateval-0.0.9/integration_tests/metric_test.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/scenarios/write_email/write_email_test.py` & `chateval-0.0.9/scenarios/write_email/write_email_test.py`

 * *Files identical despite different names*

### Comparing `chateval-0.0.8/setup.cfg` & `chateval-0.0.9/setup.cfg`

 * *Files identical despite different names*

