# Comparing `tmp/pyrecdp-1.0.1b202304251.tar.gz` & `tmp/pyrecdp-1.0.1b202305131.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/pyrecdp-1.0.1b202304251.tar", last modified: Tue Apr 25 08:03:23 2023, max compression
+gzip compressed data, was "pyrecdp-1.0.1b202305131.tar", last modified: Sat May 13 19:41:33 2023, max compression
```

## Comparing `pyrecdp-1.0.1b202304251.tar` & `pyrecdp-1.0.1b202305131.tar`

### file list

```diff
@@ -1,116 +1,116 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.415924 pyrecdp-1.0.1b202304251/
--rw-r--r--   0 root         (0) root         (0)    94051 2023-04-25 02:53:10.000000 pyrecdp-1.0.1b202304251/LICENSE
--rw-r--r--   0 root         (0) root         (0)      189 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)     8858 2023-04-25 08:03:23.415924 pyrecdp-1.0.1b202304251/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     8315 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.401917 pyrecdp-1.0.1b202304251/ScalaProcessUtils/
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/ScalaProcessUtils/__init__.py
--rw-r--r--   0 root         (0) root         (0)      104 2023-04-25 02:53:10.000000 pyrecdp-1.0.1b202304251/pyproject.toml
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.401917 pyrecdp-1.0.1b202304251/pyrecdp/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.402918 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/__init__.py
--rw-r--r--   0 root         (0) root         (0)      624 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/spark-defaults.conf
--rw-r--r--   0 root         (0) root         (0)      455 2023-04-25 04:39:12.000000 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/spark-env.sh
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.402918 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/target/
--rw-r--r--   0 root         (0) root         (0)   114879 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/target/recdp-scala-extensions-0.1.0-jar-with-dependencies.jar
--rw-r--r--   0 root         (0) root         (0)     1001 2023-04-25 04:39:12.000000 pyrecdp-1.0.1b202304251/pyrecdp/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.404919 pyrecdp-1.0.1b202304251/pyrecdp/autofe/
--rw-r--r--   0 root         (0) root         (0)     2813 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/AutoFE.py
--rw-r--r--   0 root         (0) root         (0)    12498 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/BasePipeline.py
--rw-r--r--   0 root         (0) root         (0)     4330 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/DataEstimator.py
--rw-r--r--   0 root         (0) root         (0)     2189 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/FeatureProfiler.py
--rw-r--r--   0 root         (0) root         (0)     2810 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/FeatureWrangler.py
--rw-r--r--   0 root         (0) root         (0)     1655 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/RelationalBuilder.py
--rw-r--r--   0 root         (0) root         (0)      215 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/autofe/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.404919 pyrecdp-1.0.1b202304251/pyrecdp/core/
--rw-r--r--   0 root         (0) root         (0)      186 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/core/__init__.py
--rw-r--r--   0 root         (0) root         (0)     1394 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/core/dataframe.py
--rw-r--r--   0 root         (0) root         (0)     2849 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/core/di_graph.py
--rw-r--r--   0 root         (0) root         (0)     5696 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/core/schema.py
--rw-r--r--   0 root         (0) root         (0)     5496 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/core/utils.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.406920 pyrecdp-1.0.1b202304251/pyrecdp/datasets/
--rw-r--r--   0 root         (0) root         (0)     2942 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/CESM_breast_cancer.py
--rw-r--r--   0 root         (0) root         (0)      358 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/__init__.py
--rw-r--r--   0 root         (0) root         (0)      680 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/amazon_product_review.py
--rw-r--r--   0 root         (0) root         (0)     4186 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/base_api.py
--rw-r--r--   0 root         (0) root         (0)      288 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/download.py
--rw-r--r--   0 root         (0) root         (0)      689 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/ibm_fraud_detect.py
--rw-r--r--   0 root         (0) root         (0)     1208 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/nyc_taxi.py
--rw-r--r--   0 root         (0) root         (0)      905 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/outbrain.py
--rw-r--r--   0 root         (0) root         (0)      408 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/pretrained.py
--rw-r--r--   0 root         (0) root         (0)      428 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/datasets/twitter_recsys.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.406920 pyrecdp-1.0.1b202304251/pyrecdp/primitives/
--rw-r--r--   0 root         (0) root         (0)       76 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.407920 pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/__init__.py
--rw-r--r--   0 root         (0) root         (0)     2236 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/base.py
--rw-r--r--   0 root         (0) root         (0)     2878 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/lightgbm.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.408921 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/
--rw-r--r--   0 root         (0) root         (0)     1881 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/__init__.py
--rw-r--r--   0 root         (0) root         (0)      234 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/base.py
--rw-r--r--   0 root         (0) root         (0)      269 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/binned.py
--rw-r--r--   0 root         (0) root         (0)     1171 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/category.py
--rw-r--r--   0 root         (0) root         (0)     1648 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/datetime.py
--rw-r--r--   0 root         (0) root         (0)     1398 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/drop.py
--rw-r--r--   0 root         (0) root         (0)     4055 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/encode.py
--rw-r--r--   0 root         (0) root         (0)     1221 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/feature_transform.py
--rw-r--r--   0 root         (0) root         (0)     1334 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/featuretools_adaptor.py
--rw-r--r--   0 root         (0) root         (0)     1180 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/fillna.py
--rw-r--r--   0 root         (0) root         (0)     4607 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/geograph.py
--rw-r--r--   0 root         (0) root         (0)     1445 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/name.py
--rw-r--r--   0 root         (0) root         (0)     3100 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/nlp.py
--rw-r--r--   0 root         (0) root         (0)     4720 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/relation.py
--rw-r--r--   0 root         (0) root         (0)     5724 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/statics.py
--rw-r--r--   0 root         (0) root         (0)     7142 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/type.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.411922 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/
--rw-r--r--   0 root         (0) root         (0)      111 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/__init__.py
--rw-r--r--   0 root         (0) root         (0)     5712 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/base.py
--rw-r--r--   0 root         (0) root         (0)     1002 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/category.py
--rw-r--r--   0 root         (0) root         (0)      351 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/custom.py
--rw-r--r--   0 root         (0) root         (0)     1772 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/data.py
--rw-r--r--   0 root         (0) root         (0)     3291 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/dataframe.py
--rw-r--r--   0 root         (0) root         (0)      758 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/drop.py
--rw-r--r--   0 root         (0) root         (0)     3522 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/encode.py
--rw-r--r--   0 root         (0) root         (0)      950 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/featuretools_adaptor.py
--rw-r--r--   0 root         (0) root         (0)      674 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/fillna.py
--rw-r--r--   0 root         (0) root         (0)      682 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/geograph.py
--rw-r--r--   0 root         (0) root         (0)     1092 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/merge.py
--rw-r--r--   0 root         (0) root         (0)      709 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/name.py
--rw-r--r--   0 root         (0) root         (0)      712 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/tuple.py
--rw-r--r--   0 root         (0) root         (0)     1086 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/type.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.412923 pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/__init__.py
--rw-r--r--   0 root         (0) root         (0)    54029 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/data_processor.py
--rw-r--r--   0 root         (0) root         (0)     8145 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/encoder.py
--rw-r--r--   0 root         (0) root         (0)     8115 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/utils.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.413923 pyrecdp-1.0.1b202304251/pyrecdp/widgets/
--rw-r--r--   0 root         (0) root         (0)     1092 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/BaseWidget.py
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/PlotWidget.py
--rw-r--r--   0 root         (0) root         (0)        0 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/ProfilerWidget.py
--rw-r--r--   0 root         (0) root         (0)      821 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/TabWidget.py
--rw-r--r--   0 root         (0) root         (0)     2103 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/TableViewWidget.py
--rw-r--r--   0 root         (0) root         (0)      221 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.414924 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/
--rw-r--r--   0 root         (0) root         (0)      989 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/base.html
--rw-r--r--   0 root         (0) root         (0)       85 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/error.html
--rw-r--r--   0 root         (0) root         (0)      260 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/interactions.html
--rw-r--r--   0 root         (0) root         (0)     1340 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/overview.html
--rw-r--r--   0 root         (0) root         (0)     7111 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/scripts.html
--rw-r--r--   0 root         (0) root         (0)    16515 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/styles.html
--rw-r--r--   0 root         (0) root         (0)     9250 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/variables.html
--rw-r--r--   0 root         (0) root         (0)      166 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/pyrecdp/widgets/utils.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.402918 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/
--rw-r--r--   0 root         (0) root         (0)     8858 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     3447 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/not-zip-safe
--rw-r--r--   0 root         (0) root         (0)      207 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       26 2023-04-25 08:03:23.000000 pyrecdp-1.0.1b202304251/pyrecdp.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-04-25 08:03:23.415924 pyrecdp-1.0.1b202304251/setup.cfg
--rw-r--r--   0 root         (0) root         (0)     1513 2023-04-25 08:03:19.000000 pyrecdp-1.0.1b202304251/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-25 08:03:23.415924 pyrecdp-1.0.1b202304251/tests/
--rw-r--r--   0 root         (0) root         (0)     3034 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/tests/test_data_estimator.py
--rw-r--r--   0 root         (0) root         (0)     3431 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/tests/test_feature_wrangler.py
--rw-r--r--   0 root         (0) root         (0)     3838 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/tests/test_pipeline_json.py
--rw-r--r--   0 root         (0) root         (0)     1291 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/tests/test_relational_builder.py
--rw-r--r--   0 root         (0) root         (0)     9017 2023-04-25 03:08:58.000000 pyrecdp-1.0.1b202304251/tests/test_spark_dataprocessor.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.709789 pyrecdp-1.0.1b202305131/
+-rw-r--r--   0 root         (0) root         (0)    94051 2023-05-05 19:05:00.000000 pyrecdp-1.0.1b202305131/LICENSE
+-rw-r--r--   0 root         (0) root         (0)      189 2023-05-05 19:05:00.000000 pyrecdp-1.0.1b202305131/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)     8860 2023-05-13 19:41:33.709789 pyrecdp-1.0.1b202305131/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     8315 2023-05-05 19:05:00.000000 pyrecdp-1.0.1b202305131/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/ScalaProcessUtils/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:00.000000 pyrecdp-1.0.1b202305131/ScalaProcessUtils/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      104 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyproject.toml
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      624 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/spark-defaults.conf
+-rw-r--r--   0 root         (0) root         (0)      455 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/spark-env.sh
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/target/
+-rw-r--r--   0 root         (0) root         (0)   114879 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/target/recdp-scala-extensions-0.1.0-jar-with-dependencies.jar
+-rw-r--r--   0 root         (0) root         (0)     1001 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/autofe/
+-rw-r--r--   0 root         (0) root         (0)     2990 2023-05-13 19:16:46.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/AutoFE.py
+-rw-r--r--   0 root         (0) root         (0)    13319 2023-05-12 20:18:00.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/BasePipeline.py
+-rw-r--r--   0 root         (0) root         (0)     4455 2023-05-12 20:44:07.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureEstimator.py
+-rw-r--r--   0 root         (0) root         (0)     3016 2023-05-13 03:00:40.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureProfiler.py
+-rw-r--r--   0 root         (0) root         (0)     2915 2023-05-08 20:26:24.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureWrangler.py
+-rw-r--r--   0 root         (0) root         (0)     1684 2023-05-08 21:49:59.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/RelationalBuilder.py
+-rw-r--r--   0 root         (0) root         (0)      218 2023-05-08 21:21:08.000000 pyrecdp-1.0.1b202305131/pyrecdp/autofe/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/core/
+-rw-r--r--   0 root         (0) root         (0)      186 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/core/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     1394 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/core/dataframe.py
+-rw-r--r--   0 root         (0) root         (0)     2849 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/core/di_graph.py
+-rw-r--r--   0 root         (0) root         (0)     5696 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/core/schema.py
+-rw-r--r--   0 root         (0) root         (0)     5860 2023-05-12 21:35:22.000000 pyrecdp-1.0.1b202305131/pyrecdp/core/utils.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/datasets/
+-rw-r--r--   0 root         (0) root         (0)     2942 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/CESM_breast_cancer.py
+-rw-r--r--   0 root         (0) root         (0)      358 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      680 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/amazon_product_review.py
+-rw-r--r--   0 root         (0) root         (0)     4186 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/base_api.py
+-rw-r--r--   0 root         (0) root         (0)      288 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/download.py
+-rw-r--r--   0 root         (0) root         (0)      689 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/ibm_fraud_detect.py
+-rw-r--r--   0 root         (0) root         (0)     1208 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/nyc_taxi.py
+-rw-r--r--   0 root         (0) root         (0)      905 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/outbrain.py
+-rw-r--r--   0 root         (0) root         (0)      408 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/pretrained.py
+-rw-r--r--   0 root         (0) root         (0)      428 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/datasets/twitter_recsys.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/
+-rw-r--r--   0 root         (0) root         (0)       76 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/engines/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-03-01 06:07:04.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/engines/__init__.py
+-rw-r--r--   0 root         (0) root         (0)       93 2023-03-01 06:17:33.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/engines/runner.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     2005 2023-05-12 20:38:02.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/base.py
+-rw-r--r--   0 root         (0) root         (0)     2656 2023-05-12 20:38:27.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/lightgbm.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.705789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/
+-rw-r--r--   0 root         (0) root         (0)     1893 2023-05-11 20:09:42.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      234 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/base.py
+-rw-r--r--   0 root         (0) root         (0)      269 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/binned.py
+-rw-r--r--   0 root         (0) root         (0)     1171 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/category.py
+-rw-r--r--   0 root         (0) root         (0)     1620 2023-05-12 03:42:22.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/datetime.py
+-rw-r--r--   0 root         (0) root         (0)     1398 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/drop.py
+-rw-r--r--   0 root         (0) root         (0)     4047 2023-05-12 20:27:56.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/encode.py
+-rw-r--r--   0 root         (0) root         (0)     1221 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/feature_transform.py
+-rw-r--r--   0 root         (0) root         (0)     1334 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/featuretools_adaptor.py
+-rw-r--r--   0 root         (0) root         (0)     1180 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/fillna.py
+-rw-r--r--   0 root         (0) root         (0)     4666 2023-05-12 20:55:11.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/geograph.py
+-rw-r--r--   0 root         (0) root         (0)     1445 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/name.py
+-rw-r--r--   0 root         (0) root         (0)     3100 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/nlp.py
+-rw-r--r--   0 root         (0) root         (0)     4720 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/relation.py
+-rw-r--r--   0 root         (0) root         (0)     2975 2023-05-05 19:42:48.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/type.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.705789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/
+-rw-r--r--   0 root         (0) root         (0)      111 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     5743 2023-05-10 01:40:36.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/base.py
+-rw-r--r--   0 root         (0) root         (0)     1002 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/category.py
+-rw-r--r--   0 root         (0) root         (0)      351 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/custom.py
+-rw-r--r--   0 root         (0) root         (0)     1772 2023-05-08 22:27:09.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/data.py
+-rw-r--r--   0 root         (0) root         (0)     3291 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/dataframe.py
+-rw-r--r--   0 root         (0) root         (0)      758 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/drop.py
+-rw-r--r--   0 root         (0) root         (0)     3522 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/encode.py
+-rw-r--r--   0 root         (0) root         (0)      950 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/featuretools_adaptor.py
+-rw-r--r--   0 root         (0) root         (0)      674 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/fillna.py
+-rw-r--r--   0 root         (0) root         (0)      682 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/geograph.py
+-rw-r--r--   0 root         (0) root         (0)     1376 2023-05-08 22:20:11.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/merge.py
+-rw-r--r--   0 root         (0) root         (0)      709 2023-05-09 20:16:39.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/name.py
+-rw-r--r--   0 root         (0) root         (0)      712 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/tuple.py
+-rw-r--r--   0 root         (0) root         (0)     1086 2023-05-09 20:16:35.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/type.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.705789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/profilers/
+-rw-r--r--   0 root         (0) root         (0)      157 2023-05-08 18:34:18.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/profilers/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     5645 2023-05-13 19:16:22.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/profilers/statics.py
+-rw-r--r--   0 root         (0) root         (0)     4363 2023-05-12 03:42:15.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/profilers/type_infer.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.705789 pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/__init__.py
+-rw-r--r--   0 root         (0) root         (0)    54029 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/data_processor.py
+-rw-r--r--   0 root         (0) root         (0)     8145 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/encoder.py
+-rw-r--r--   0 root         (0) root         (0)     8115 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/utils.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.705789 pyrecdp-1.0.1b202305131/pyrecdp/widgets/
+-rw-r--r--   0 root         (0) root         (0)     1092 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/BaseWidget.py
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/PlotWidget.py
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/ProfilerWidget.py
+-rw-r--r--   0 root         (0) root         (0)      821 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/TabWidget.py
+-rw-r--r--   0 root         (0) root         (0)     2103 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/TableViewWidget.py
+-rw-r--r--   0 root         (0) root         (0)      221 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.709789 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/
+-rw-r--r--   0 root         (0) root         (0)      989 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/base.html
+-rw-r--r--   0 root         (0) root         (0)       85 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/error.html
+-rw-r--r--   0 root         (0) root         (0)      260 2023-05-11 22:08:36.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/interactions.html
+-rw-r--r--   0 root         (0) root         (0)     1340 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/overview.html
+-rw-r--r--   0 root         (0) root         (0)  3485304 2023-05-13 03:07:56.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/scripts.html
+-rw-r--r--   0 root         (0) root         (0)    16515 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/styles.html
+-rw-r--r--   0 root         (0) root         (0)     9250 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/variables.html
+-rw-r--r--   0 root         (0) root         (0)      166 2023-05-05 19:05:01.000000 pyrecdp-1.0.1b202305131/pyrecdp/widgets/utils.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:41:33.701789 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     8860 2023-05-13 19:41:33.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     3454 2023-05-13 19:41:33.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 19:41:33.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-01-13 19:42:06.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/not-zip-safe
+-rw-r--r--   0 root         (0) root         (0)      203 2023-05-13 19:41:33.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       26 2023-05-13 19:41:33.000000 pyrecdp-1.0.1b202305131/pyrecdp.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 19:41:33.709789 pyrecdp-1.0.1b202305131/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)     1457 2023-05-13 19:41:22.000000 pyrecdp-1.0.1b202305131/setup.py
```

### Comparing `pyrecdp-1.0.1b202304251/LICENSE` & `pyrecdp-1.0.1b202305131/LICENSE`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/PKG-INFO` & `pyrecdp-1.0.1b202305131/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 Metadata-Version: 2.1
 Name: pyrecdp
-Version: 1.0.1b202304251
+Version: 1.0.1b202305131
 Summary: A data processing bundle for spark based recommender system operations
 Home-page: https://github.com/intel/e2eAIOK/
 Author: INTEL AIA
-Author-email: chendi.xue@intel.com
+License: UNKNOWN
 Project-URL: Bug Tracker, https://github.com/intel/e2eAIOK/
+Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -213,7 +214,9 @@
 
 ## LICENSE
 * Apache 2.0
 
 ## Dependency
 * Spark 3.x
 * python 3.*
+
+
```

### Comparing `pyrecdp-1.0.1b202304251/README.md` & `pyrecdp-1.0.1b202305131/README.md`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/spark-defaults.conf` & `pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/spark-defaults.conf`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/ScalaProcessUtils/target/recdp-scala-extensions-0.1.0-jar-with-dependencies.jar` & `pyrecdp-1.0.1b202305131/pyrecdp/ScalaProcessUtils/target/recdp-scala-extensions-0.1.0-jar-with-dependencies.jar`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/__init__.py` & `pyrecdp-1.0.1b202305131/pyrecdp/__init__.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/autofe/BasePipeline.py` & `pyrecdp-1.0.1b202305131/pyrecdp/autofe/BasePipeline.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,14 +11,20 @@
 from IPython.display import display
 
 logging.basicConfig(format='%(asctime)s %(levelname)s:%(message)s', level=logging.ERROR, datefmt='%I:%M:%S')
 logger = logging.getLogger(__name__)
 
 class BasePipeline:
     def __init__(self, dataset, label, *args, **kwargs):
+        # properties
+        # self.main_table: main table names
+        # self.dataset: a dictionary, main_table will be indicated with key 'main_table'
+        # self.y: target label
+        # self.pipeline: a direct graph to store the operation
+
         if isinstance(dataset, pd.DataFrame):
             self.dataset = {'main_table': dataset}
         elif isinstance(dataset, list):
             self.dataset = dict((idx, data) for idx, data in enumerate(dataset))
         elif isinstance(dataset, dict):
             self.dataset = dataset
         else:
@@ -102,16 +108,18 @@
         #self.create_executable_pipeline()
         
     def create_executable_pipeline(self):
         node_chain = self.pipeline.convert_to_node_chain()
         executable_pipeline = DiGraph()
         executable_sequence = []
         for idx in node_chain:
-            executable_pipeline[idx] = self.pipeline[idx].instantiate()
-            executable_sequence.append(executable_pipeline[idx])
+            actual_op = self.pipeline[idx].instantiate()
+            if actual_op:
+                executable_pipeline[idx] = actual_op
+                executable_sequence.append(executable_pipeline[idx])
         return executable_pipeline, executable_sequence
     
     def add_operation(self, config):
         # check if below keys are existing
         # children: who is its child
         # next: who is will use this operation
         # inline_function: the function to process data
@@ -229,52 +237,61 @@
         for edge in edges:
             f.edge(*edge)
         return f  
 
     def to_chain(self):
         return self.pipeline.convert_to_node_chain()
         
-    def execute(self, engine_type = "pandas", start_op_idx = 0, no_cache = False, transformed_end = -1):
+    def execute(self, engine_type = "pandas", start_op_idx = -1, no_cache = False, transformed_end = -1, data = None):
         # prepare pipeline
-        executable_pipeline, executable_sequence = self.create_executable_pipeline()
+        if not hasattr(self, 'executable_pipeline') or not hasattr(self, 'executable_sequence'):
+            self.executable_pipeline, self.executable_sequence = self.create_executable_pipeline()
+        executable_pipeline = self.executable_pipeline
+        executable_sequence = self.executable_sequence
         print(executable_pipeline)
 
         # execute
         if engine_type == 'pandas':
             with Timer(f"execute with pandas"):
                 start = False
                 for op in executable_sequence:
-                    if op.op.idx == start_op_idx:
+                    if start_op_idx == -1 or op.op.idx == start_op_idx:
                         start = True
                     if not start:
                         continue
                     if isinstance(op, DataFrameOperation):
-                        input_df = self.dataset if start_op_idx == 0 else {'main_table': self.transformed_cache}
+                        if data:
+                            input_df = data
+                        else:
+                            input_df = self.dataset if start_op_idx == -1 else {'main_table': self.transformed_cache}
                         input_df = deepcopy(input_df) if no_cache else input_df
                         op.set(input_df)
                     with Timer(f"execute {op}"):
-                        op.execute_pd(executable_pipeline, no_cache)
+                        op.execute_pd(executable_pipeline)
             if transformed_end == -1:
                 df = executable_sequence[-1].cache
             else:
                 df = executable_pipeline[transformed_end].cache
         elif engine_type == 'spark':
             with Timer(f"execute with spark"):
                 start = False
                 for op in executable_sequence:
-                    if op.op.idx == start_op_idx:
+                    if start_op_idx == -1 or op.op.idx == start_op_idx:
                         start = True
                     if not start:
                         continue
-                    if isinstance(op, DataFrameOperation) and op.op.idx == start_op_idx:
-                        input_df = self.dataset if start_op_idx == 0 else {'main_table': self.transformed_cache}
+                    if isinstance(op, DataFrameOperation):
+                        if data:
+                            input_df = data
+                        else:
+                            input_df = self.dataset if start_op_idx == -1 else {'main_table': self.transformed_cache}
                         input_df = deepcopy(input_df) if no_cache else input_df
                         op.set(input_df)
                     print(f"append {op}")
-                    op.execute_spark(executable_pipeline, self.rdp, no_cache)
+                    op.execute_spark(executable_pipeline, self.rdp)
                 if transformed_end == -1:
                     ret = executable_sequence[-1].cache
                 else:
                     ret = executable_pipeline[transformed_end].cache
                 if isinstance(ret, SparkDataFrame):
                     df = self.rdp.transform(ret)
                 elif isinstance(ret, SparkRDD):
@@ -284,22 +301,22 @@
                     df = ret
         else:
             raise NotImplementedError('pipeline only support pandas and spark as engine')
         
         # fetch result
         return df
 
-    def fit_transform(self, engine_type = 'pandas', no_cache = False, *args, **kwargs):
+    def fit_transform(self, engine_type = 'pandas', no_cache = False, data = None, *args, **kwargs):
         if not no_cache and hasattr(self, 'transformed_cache') and self.transformed_cache is not None:
             print("Detect pre-transformed cache, return cached data")
             print("If re-transform is required, please use fit_transform(no_cache = True)")
             return self.transformed_cache
         if engine_type == "spark":
             self.rdp = SparkDataProcessor()
-        ret = self.execute(engine_type, no_cache)
+        ret = self.execute(engine_type = engine_type, no_cache = no_cache, data = data)
         if engine_type == "spark":
             del self.rdp 
             self.rdp = None
         self.transformed_cache = ret
         return ret
     
     def get_transformed_cache(self):
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/autofe/DataEstimator.py` & `pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureEstimator.py`

 * *Files 14% similar despite different names*

```diff
@@ -5,31 +5,31 @@
 from pyrecdp.core import DiGraph
 import copy
 from pyrecdp.core import SparkDataProcessor
 
 logging.basicConfig(format='%(asctime)s %(levelname)s:%(message)s', level=logging.ERROR, datefmt='%I:%M:%S')
 logger = logging.getLogger(__name__)
 
-class DataEstimator(BasePipeline):
-    def __init__(self, data_pipeline, method, config = None):
+class FeatureEstimator(BasePipeline):
+    def __init__(self, data_pipeline, config = None):
         """
         Parameters: data_pipeline, method and config
         config = {
             'model_file': string,
             'dataset': path or dataframe,
             'label': string,
             'model_name': string,
             'objective': string,
-            'metrics': string,
             'train_test_splitter': function
         }
         Two option:
         data_pipeline is json_file_path, specify config for ['dataset', 'label']
-        data_pipeline is pre created pipeline object, specify config for ['model_name', 'objective', 'metrics']
+        data_pipeline is pre created pipeline object, specify config for ['model_name', 'objective']
         """
+        method = 'train'
         model_file = config['model_file'] if 'model_file' in config else None
         label = config['label'] if 'label' in config else None
         self.transformed_cache = None
         if isinstance(data_pipeline, str):
             dataset = config['dataset'] 
             if dataset is not None:
                 super().__init__(dataset, label)
@@ -49,41 +49,49 @@
         max_idx = self.pipeline.get_max_idx()
         leaf_idx = self.pipeline.convert_to_node_chain()[-1]
         self.transformed_end_idx = leaf_idx
         
         if self.pipeline[leaf_idx].op not in ["lightgbm"]:
             model_name = config['model_name']
             objective = config['objective']
-            metrics = config['metrics']
+            if objective == 'binary':
+                config['metrics'] = 'auc'
+            elif objective == 'regression':
+                config['metrics'] = 'rmse'
             if method == 'train':
                 train_test_splitter = config['train_test_splitter'] if 'train_test_splitter' in config else None
             if model_file is None:
-                model_file = f"{model_name}_{objective}_{metrics}_{label}.mdl"
+                model_file = f"{model_name}_{objective}_{label}.mdl"
             cur_idx = max_idx + 1
             self.estimator_pipeline_start = cur_idx
             # we need to add two op, one to prepare dataset, one for estimator
-            op_config = {'label': label, 'metrics': metrics, 'objective': objective, 'model_file': model_file, 'method': method, 'train_test_splitter': train_test_splitter}
             op = Operation(cur_idx, [leaf_idx], None, 'DataFrame', 'main_table')
             self.pipeline[cur_idx] = op
             
             child_idx = cur_idx
             cur_idx += 1
-            op_config = {'label': label, 'metrics': metrics, 'objective': objective, 'model_file': model_file, 'method': method, 'train_test_splitter': train_test_splitter}
+            op_config = {'label': label, 'objective': objective, 'train_test_splitter': train_test_splitter}
+            if 'metrics' in config:
+                op_config['metrics'] = config['metrics']
             op = Operation(cur_idx, [child_idx], None, model_name, op_config)
             self.pipeline[cur_idx] = op
         else:
             self.pipeline[leaf_idx].config['method'] = method  
 
-    def fit_transform(self, engine_type = 'pandas', no_cache = False, *args, **kwargs):
+    def fit_transform(self, engine_type = 'pandas', no_cache = False, data = None, *args, **kwargs):
         if self.transformed_cache is not None and not no_cache: # we can skip data process steps
             start_op_idx = self.estimator_pipeline_start
         else:
-            start_op_idx = 0
+            start_op_idx = -1
         if engine_type == "spark":
             self.rdp = SparkDataProcessor()
-        ret = self.execute(engine_type, start_op_idx, no_cache, transformed_end = self.transformed_end_idx)
+        ret = self.execute(engine_type, start_op_idx, no_cache, data = data, transformed_end = self.transformed_end_idx)
         if engine_type == "spark":
             del self.rdp 
             self.rdp = None
         if self.transformed_cache is None:
             self.transformed_cache = ret
-        return ret    
+        self.feature_importance = self.executable_sequence[-1].cache
+        return ret
+    
+    def get_feature_importance(self):
+        return self.feature_importance
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/autofe/FeatureProfiler.py` & `pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureProfiler.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,17 @@
 from jinja2 import Environment, PackageLoader
+from pyrecdp.primitives.profilers import *
 from pyrecdp.primitives.generators import *
 from .BasePipeline import BasePipeline
+from pyrecdp.core.dataframe import DataFrameAPI
+from pyrecdp.core import SeriesSchema
+import pandas as pd
+import copy
+from IPython.display import display
+
 from bokeh.resources import INLINE
 ENV_LOADER = Environment(
     loader=PackageLoader("pyrecdp", "widgets/templates"),
 )
 
 CELL_HEIGHT_OVERRIDE = """<style>
                             div.output_scroll {
@@ -37,28 +44,39 @@
 
         display(HTML(self._repr_html_()))
 
     def _repr_html_(self) -> str:
         """
         Display report inside a notebook
         """
-        return f"{CELL_HEIGHT_OVERRIDE}<div style='background-color: #fff;'>{self.report}</div>"
+        return f"{CELL_HEIGHT_OVERRIDE}</script><div style='background-color: #fff;'>{self.report}</div>"
+
 class FeatureProfiler(BasePipeline):        
     def __init__(self, dataset, label, *args, **kwargs):
         super().__init__(dataset, label)
 
-        self.data_stats = None
-        self._processed_data = self.feature_data
-
-        self.generators.append([cls() for cls in feature_infer_list])
-
+        self.data_profiler = [cls() for cls in feature_infer_list]
+        self.generators.append([cls() for cls in profiler_feature_generator_list])
         self.fit_analyze()
+        
+    def fit_analyze(self, *args, **kwargs): 
+        child = list(self.pipeline.keys())[-1]
+        max_id = child
+        # sample data
+        X = DataFrameAPI().instiate(self.dataset[self.main_table])
+        sampled_data = X.may_sample()
+
+        self.pipeline[child].output.append(SeriesSchema(sampled_data[self.y]))
+        
+        # firstly, call data profiler to analyze data
+        for generator in self.data_profiler:
+            self.pipeline, child, max_id = generator.fit_prepare(self.pipeline, [child], max_id, sampled_data)
+            
+        child, max_id = super().fit_analyze(*args, **kwargs)
+        
+        feature_data = self.fit_transform()
+        self.data_stats = StatisticsFeatureGenerator().update_feature_statistics(feature_data, self.dataset[self.main_table][self.y])
     
     def visualize_analyze(self, engine_type = 'pandas', display = True):
         if not self.data_stats:
-            feature_data = self.fit_transform(engine_type)
-            self.data_stats = StatisticsFeatureGenerator().update_feature_statistics(feature_data, self.y)
-            self._processed_data = feature_data
+            raise NotImplementedError("We didn't detect data statistics for thiis data")            
         return FeatureVisulizer(self.data_stats)
-
-    def _debug_get_processed_data(self):
-        return self._processed_data
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/autofe/FeatureWrangler.py` & `pyrecdp-1.0.1b202305131/pyrecdp/autofe/FeatureWrangler.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,39 +1,42 @@
 from pyrecdp.primitives.generators import *
+from pyrecdp.primitives.profilers import *
 from .BasePipeline import BasePipeline
 import logging
 from pyrecdp.core.dataframe import DataFrameAPI
 from pyrecdp.core import SeriesSchema
 import pandas as pd
 import copy
 
 logging.basicConfig(format='%(asctime)s %(levelname)s:%(message)s', level=logging.ERROR, datefmt='%I:%M:%S')
 logger = logging.getLogger(__name__)
 
 class FeatureWrangler(BasePipeline):
-    def __init__(self, dataset, label, supplementary_datasets = None, *args, **kwargs):
+    def __init__(self, dataset, label, *args, **kwargs):
         super().__init__(dataset, label)
         self.data_profiler = [cls() for cls in feature_infer_list]
         self.pre_feature = [cls() for cls in label_feature_generator_list]
         # If we provided multiple datasets in this workload
         self.generators.append([cls() for cls in pre_feature_generator_list])
         self.generators.append([cls() for cls in transformation_generator_list])
         self.generators.append([cls() for cls in pre_enocode_feature_generator_list])
         self.generators.append([cls() for cls in local_encode_generator_list])
         self.generators.append([cls() for cls in global_dict_index_generator_list])
         self.generators.append([cls() for cls in post_feature_generator_list])
         self.generators.append([cls(final = True) for cls in final_generator_list])
 
         self.fit_analyze()
 
-    def fit_analyze(self, *args, **kwargs):
-        X = DataFrameAPI().instiate(self.dataset[self.main_table])
-        sampled_data = X.may_sample()
+    def fit_analyze(self, *args, **kwargs): 
         child = list(self.pipeline.keys())[-1]
         max_id = child
+        # sample data
+        X = DataFrameAPI().instiate(self.dataset[self.main_table])
+        sampled_data = X.may_sample()
+        
         if self.y is not None:
             # insert label process to pipeline            
             cur_id = child
             original_first_op = copy.deepcopy(self.pipeline[cur_id])
             self.pipeline[cur_id].output = [SeriesSchema(sampled_data[self.y])]
             
             for generator in self.data_profiler:
@@ -47,10 +50,11 @@
             original_first_op.children = [child]
             self.y = [i.name for i in self.pipeline[child].output][0]
             self.pipeline[cur_id] = original_first_op            
             max_id = cur_id
             child = cur_id
             sampled_data = sampled_data[self.feature_columns]
         
+        # firstly, call data profiler to analyze data
         for generator in self.data_profiler:
             self.pipeline, child, max_id = generator.fit_prepare(self.pipeline, [child], max_id, sampled_data)
-        super().fit_analyze(*args, **kwargs)
+        return super().fit_analyze(*args, **kwargs)
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/autofe/RelationalBuilder.py` & `pyrecdp-1.0.1b202305131/pyrecdp/autofe/RelationalBuilder.py`

 * *Files 8% similar despite different names*

```diff
@@ -30,8 +30,9 @@
 
     def fit_analyze(self, *args, **kwargs):
         child = self.children
         max_id = max(self.children)
         for i in range(len(self.generators)):
             for generator in self.generators[i]:
                 child = child if isinstance(child, list) else [child]
-                self.pipeline, child, max_id = generator.fit_prepare(self.pipeline, child, max_id)
+                self.pipeline, child, max_id = generator.fit_prepare(self.pipeline, child, max_id)
+        return child, max_id
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/core/dataframe.py` & `pyrecdp-1.0.1b202305131/pyrecdp/core/dataframe.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/core/di_graph.py` & `pyrecdp-1.0.1b202305131/pyrecdp/core/di_graph.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/core/schema.py` & `pyrecdp-1.0.1b202305131/pyrecdp/core/schema.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/core/utils.py` & `pyrecdp-1.0.1b202305131/pyrecdp/core/utils.py`

 * *Files 10% similar despite different names*

```diff
@@ -102,15 +102,25 @@
     if isinstance(s, type):
         ret = s
     elif isinstance(s, tuple) or isinstance(s, list):
         import importlib
         module = importlib.import_module(s[0])
         ret = eval("module." + s[1])
     return ret
-    
+
+def infer_problem_type(y):
+    unique_count = y.nunique()
+    if unique_count == 2:
+        problem_type = 'binary'
+    elif y.dtype.name in ['object', 'category', 'string']:
+        problem_type = 'multiclass'
+    else:
+        problem_type = 'regression'
+    return problem_type
+ 
 def is_text_series(s):
     from pandas.api import types as pdt
     import pandas as pd
     def try_text(s):
         if not pdt.is_string_dtype(s):
             return False
         if len(s) > 1000:
@@ -123,15 +133,18 @@
         except:
             return False
         return False
     
     return try_text(s)
 
 def is_tuple(s):
-    t = type(s.loc[s.first_valid_index()]) if s.first_valid_index() >= 0 else None
+    if isinstance(s.first_valid_index(), type(None)):
+        t = None
+    else:
+        t = type(s.loc[s.first_valid_index()]) if s.first_valid_index() >= 0 else None
     return isinstance(t, tuple)
        
 def is_integer_convertable(s):
     from pandas.api.types import is_numeric_dtype
     if not is_numeric_dtype(s.dtype):
         return False
     s = s.fillna(0)
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/CESM_breast_cancer.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/CESM_breast_cancer.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/amazon_product_review.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/amazon_product_review.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/base_api.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/base_api.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/ibm_fraud_detect.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/ibm_fraud_detect.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/nyc_taxi.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/nyc_taxi.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/datasets/outbrain.py` & `pyrecdp-1.0.1b202305131/pyrecdp/datasets/outbrain.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/base.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/base.py`

 * *Files 26% similar despite different names*

```diff
@@ -3,30 +3,23 @@
 from sklearn.metrics import mean_squared_error, roc_auc_score
 from pyrecdp.core.utils import callable_string_fix
 
 class BaseEstimator(BaseOperation):
     def __init__(self, op_base):
         super().__init__(op_base)
         self.config = self.op.config
-        if 'method' in self.config:
-            self.method = self.config['method']
-        else:
-            self.method = 'predict'
 
     def get_func_train(self):
         raise NotImplementedError("BaseEstimator is an abstract class")
 
     def get_func_predict(self):
         raise NotImplementedError("BaseEstimator is an abstract class")
 
     def get_function_pd(self):
-        if self.method == 'train':
-            return self.get_func_train()
-        else:
-            return self.get_func_predict()
+        return self.get_func_train()
         
     def get_evaluate_func(self, metric):
         if metric == 'rmse':
             def rmse_func(ground_truth, pred):
                 return np.sqrt(mean_squared_error(ground_truth, pred))
             return rmse_func
         if metric == 'auc':
@@ -46,11 +39,11 @@
                 print(splitter_func_str)
                 exec(splitter_func_str, globals())
                 return eval(func_name)
             else:
                 raise NotImplementedError(f"Unable to inteprete {splitter_func_str}as train_test_splitter")
         else:
             def splitter_func(df):
-                test_sample = df.sample(frac = 0.05)
+                test_sample = df.sample(frac = 0.1)
                 train_sample = df.drop(test_sample.index)
                 return train_sample, test_sample
             return splitter_func
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/estimators/lightgbm.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/estimators/lightgbm.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,56 +6,47 @@
     def __init__(self, op_base):
         super().__init__(op_base)
         self.support_spark_dataframe = False
         self.support_spark_rdd = False
 
     def get_func_train(self):
         label = self.config['label']
-        metrics = self.config['metrics']
         objective = self.config['objective']
-        model_file = self.config['model_file']
+        if 'metrics' in self.config:
+            metrics = self.config['metrics']
+        else:
+            metrics = None
         train_test_splitter = self.get_splitter_func(self.config['train_test_splitter'])
         def train(df):
             train_sample, test_sample = train_test_splitter(df)
-            
             x_train = train_sample.drop(columns=[label])
             y_train = train_sample[label].values
-
+            lgbm_train = lgbm.Dataset(x_train, y_train)
             x_val = test_sample.drop(columns=[label])
             y_val = test_sample[label].values
-
-            lgbm_train = lgbm.Dataset(x_train, y_train, silent=False)
-            lgbm_val = lgbm.Dataset(x_val, y_val, silent=False)
+            lgbm_val = lgbm.Dataset(x_val, y_val)
             
             params = {
                 'boosting_type':'gbdt',
                 'objective': objective,
-                'nthread': 4,
                 'num_leaves': 31,
-                'learning_rate': 0.05,
-                'max_depth': -1,
-                'subsample': 0.8,
-                'bagging_fraction' : 1,
-                'max_bin' : 5000 ,
-                'bagging_freq': 20,
-                'colsample_bytree': 0.6,
-                'metric': metrics,
-                'min_split_gain': 0.5,
-                'min_child_weight': 1,
-                'min_child_samples': 10,
-                'scale_pos_weight':1,
-                'zero_as_missing': True,
+                'learning_rate': 0.01,
                 'seed':0,
-                'num_rounds':2000,
-                'num_boost_round': 2000,
-                'early_stopping_rounds': 50
+                'verbose': 1
             }
+            if not isinstance(metrics, type(None)):
+                params['metrics'] = metrics
             model = lgbm.train(params=params, train_set=lgbm_train, valid_sets=lgbm_val, verbose_eval=100)
-            model.save_model(model_file, num_iteration=model.best_iteration) 
-            return model
+            #model.save_model(model_file, num_iteration=model.best_iteration)
+
+            f_imp = model.feature_importance(importance_type='split').tolist()
+            f_names = model.feature_name()
+            ret = dict((fn, fi) for fn, fi in zip(f_names, f_imp))
+            ret = sorted(ret.items(), key = lambda x:x[1], reverse = True)
+            return ret
         return train
         
     def get_func_predict(self):
         label = self.config['label']
         metrics = self.config['metrics']
         model_file = self.config['model_file']
         evalute_func = self.get_evaluate_func(metrics)
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/__init__.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,29 +1,30 @@
 from .binned import BinnedFeatureGenerator
 from .category import CategoryFeatureGenerator
 from .datetime import DatetimeFeatureGenerator
 from .drop import DropUselessFeatureGenerator
 from .name import RenameFeatureGenerator
 from .fillna import FillNaFeatureGenerator
-from .statics import StatisticsFeatureGenerator
-from .type import TypeInferFeatureGenerator, TypeCheckFeatureGenerator,TypeConvertFeatureGenerator
+from .type import TypeCheckFeatureGenerator,TypeConvertFeatureGenerator
 from .nlp import DecodedTextFeatureGenerator, TextFeatureGenerator
 from .geograph import GeoFeatureGenerator, CoordinatesInferFeatureGenerator
 from .relation import RelationalFeatureGenerator
 from .encode import OneHotFeatureGenerator, ListOneHotFeatureGenerator, TargetEncodeFeatureGenerator, LabelEncodeFeatureGenerator
 from .feature_transform import ConvertToNumberFeatureGenerator
 
-feature_infer_list = [
-    TypeInferFeatureGenerator,   
-]
-
 relation_builder_list = [
     RelationalFeatureGenerator
 ]
 
+profiler_feature_generator_list = [
+    CoordinatesInferFeatureGenerator,
+    ConvertToNumberFeatureGenerator,
+    TypeConvertFeatureGenerator,
+]
+
 label_feature_generator_list = [
     RenameFeatureGenerator,
     TypeConvertFeatureGenerator,
     FillNaFeatureGenerator,
     LabelEncodeFeatureGenerator,
 ]
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/category.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/category.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/datetime.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/datetime.py`

 * *Files 6% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 
 class DatetimeTransformer(TransformPrimitive):
     name = "astype_datetime"
     return_type = np.datetime64
 
     def get_function(self):
         def convert(array):
-            return pd.to_datetime(array, errors='coerce', infer_datetime_format=True)
+            return pd.to_datetime(array, errors='coerce')
 
         return convert
 
 class DatetimeFeatureGenerator(FeaturetoolsBasedFeatureGenerator):
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
         self.op_list = [
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/drop.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/drop.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/encode.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/encode.py`

 * *Files 5% similar despite different names*

```diff
@@ -58,15 +58,15 @@
     def fit_prepare(self, pipeline, children, max_idx):
         is_useful = False
         pa_schema = pipeline[children[0]].output
         config = {}
         for pa_field in pa_schema:
             if pa_field.is_list_string:
                 feature = pa_field.name
-                out_schema = [SeriesSchema(f"{feature}_{key}", int) for key in pa_field.config["is_list_string"][1] if key is not None or key is not ""]
+                out_schema = [SeriesSchema(f"{feature}_{key}", int) for key in pa_field.config["is_list_string"][1] if key != None or key != ""]
                 config[pa_field.name] = pa_field.config["is_list_string"]
                 is_useful = True
                 pa_schema.extend(out_schema)
         if is_useful:
             cur_idx = max_idx + 1
             pipeline[cur_idx] = Operation(cur_idx, children, pa_schema, op = 'list_onehot_encode', config = config)
             return pipeline, cur_idx, cur_idx
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/feature_transform.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/feature_transform.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/featuretools_adaptor.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/featuretools_adaptor.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/fillna.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/fillna.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/geograph.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/geograph.py`

 * *Files 2% similar despite different names*

```diff
@@ -94,14 +94,16 @@
                 
             for to_detect in coor_related_names:
                 if to_detect in f_name.lower():
                     if to_detect == "longitude":
                         point = Point(longitude = f_name, prefix = get_prefix(f_name, to_detect))
                     elif to_detect == "latitude":
                         point = Point(latitude = f_name, prefix = get_prefix(f_name, to_detect))
+                    else:
+                        continue
                     
                     update_inline = False
                     for exist_point in self.points:
                         if exist_point == point:
                             exist_point.update(point)
                             update_inline = True
                     if not update_inline:
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/name.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/name.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/nlp.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/nlp.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/relation.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/generators/relation.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/generators/statics.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/profilers/statics.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-from .base import BaseFeatureGenerator as super_class
 from pyrecdp.core import SeriesSchema
 from pyrecdp.core.utils import is_text_series
 from pyrecdp.core.utils import Timer
 import pandas as pd
 import numpy as np
 
 def draw_xy_scatter_plot(xy_scatter_features, feature_data, y, row_height, n_plot_per_row):
@@ -39,14 +38,15 @@
 
     fig_list.update_layout(height=row_height * n_row, width=400 * n_col)
     
     return fig_list
 
 def draw_mapbox_plot(mapbox_scatter_features, feature_data):
     import plotly.graph_objs as go
+
     from shapely.geometry import MultiPoint
     fig_list = go.Figure()
 
     for c_name in mapbox_scatter_features:
         feature = feature_data[c_name]
         if len(feature) > 10000:
             feature = feature.sample(n=10000, random_state=123)
@@ -72,27 +72,26 @@
             ),
             pitch=0,
             zoom=8
         ),
     )
         
     return fig_list
-class StatisticsFeatureGenerator(super_class):
+class StatisticsFeatureGenerator():
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
 
     def fit_prepare(self, pipeline, children, max_idx):
         return pipeline, children[0], max_idx
     
     def update_feature_statistics(self, X, y):
         overview_info = {}
         overview_detail = {}
         overview_info['Number of Features'] = X.shape[1]
         overview_info['Number of Rows'] = X.shape[0]
-        interactions_detail = self.get_interactive_plot(X, y)
         
         length = X.shape[0]
         for feature_name in X.columns:
             with Timer(f"prepare info for {feature_name}"):
                 feature = X[feature_name]
                 desc_info = dict((k, v) for k, v in feature.describe().to_dict().items() if k not in ['count'])
                 if 'unique' in desc_info:
@@ -105,21 +104,20 @@
                 
                 stat = {'type': feature_type, 'unique': {"u": n_unique, "m": length}, 'quantile':desc_info}
                 if feature_name not in overview_detail:
                     overview_detail[feature_name] = stat
         
         data_stats = {}
         data_stats["overview"] = (overview_info, overview_detail)
+        interactions_detail = self.get_interactive_plot(X, y)
         data_stats['interactions']=(dict(), interactions_detail)
         
         return data_stats
     
     def get_interactive_plot(self, feature_data, y):
-        from plotly.subplots import make_subplots
-        import plotly.graph_objs as go
         from plotly.offline import plot
         row_height = 300
         n_plot_per_row = 2
         
         # we will create types of plot
         xy_scatter_features = []
         mapbox_scatter_features = []
@@ -140,16 +138,16 @@
         ret = {}
         ret = {"error": False}
 
         # draw xy scatter
         if len(xy_scatter_features) > 0:
             with Timer("Draw xy scatter plot"):
                 fig_list = draw_xy_scatter_plot(xy_scatter_features, feature_data, y, row_height, n_plot_per_row)
-            ret['html'] = plot(fig_list, output_type='div')
+            ret['html'] = plot(fig_list, output_type='div', include_plotlyjs=False, auto_open=False)
         
         # draw mapbox
         if len(mapbox_scatter_features) > 0:
             with Timer("Draw mapbox plot"):
                 fig_list = draw_mapbox_plot(mapbox_scatter_features, feature_data)
-            ret['html'] += plot(fig_list, output_type='div')
-        
+            ret['html'] += plot(fig_list, output_type='div', include_plotlyjs=False, auto_open=False)
+
         return ret
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/base.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -79,24 +79,27 @@
         self.cache = None
         self.support_spark_dataframe = False
         self.support_spark_rdd = False
         self.fast_without_dpp = False
        
     def __repr__(self) -> str:
         return self.op.op
+
+    def describe(self) -> str:
+        return str(self.op.dump())
         
-    def execute_pd(self, pipeline, no_cache = False):
+    def execute_pd(self, pipeline):
         _proc = self.get_function_pd()
         if not self.op.children or len(self.op.children) == 0:
             pass
         else:
             child_output = pipeline[self.op.children[0]].cache
             self.cache = _proc(child_output)
             
-    def execute_spark(self, pipeline, rdp, no_cache = False):
+    def execute_spark(self, pipeline, rdp):
         _convert = None
         if not self.op.children or len(self.op.children) == 0:
             pass
         else:
             child_output = pipeline[self.op.children[0]].cache
             if isinstance(child_output, SparkDataFrame):
                 if self.support_spark_dataframe:
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/category.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/category.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/data.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/data.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/dataframe.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/dataframe.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/drop.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/drop.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/encode.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/encode.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/featuretools_adaptor.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/featuretools_adaptor.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/fillna.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/fillna.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/geograph.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/geograph.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/merge.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/merge.py`

 * *Files 23% similar despite different names*

```diff
@@ -10,14 +10,18 @@
         if self.cache is not None:
             return
         
         if len(self.op.children) != 2:
             raise ValueError("merge operation only accept num_children as 2")
         left_child = pipeline[self.op.children[0]].cache
         right_child = pipeline[self.op.children[1]].cache
+        if isinstance(left_child, type(None)):
+            print(f"left child is None, details: {pipeline[self.op.children[0]].describe()}")
+        if isinstance(right_child, type(None)):
+            print(f"right child is None, details: {pipeline[self.op.children[1]].describe()}")
         self.cache = pd.merge(left_child, right_child, on = self.config['on'], how = self.config['how'])
 
     def execute_spark(self, pipeline, rdp):
         if self.cache is not None:
             return
         
         if len(self.op.children) != 2:
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/name.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/name.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/tuple.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/tuple.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/operations/type.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/operations/type.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/data_processor.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/data_processor.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/encoder.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/encoder.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/primitives/spark_data_processor/utils.py` & `pyrecdp-1.0.1b202305131/pyrecdp/primitives/spark_data_processor/utils.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/BaseWidget.py` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/BaseWidget.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/TabWidget.py` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/TabWidget.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/TableViewWidget.py` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/TableViewWidget.py`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/base.html` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/base.html`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/overview.html` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/overview.html`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/styles.html` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/styles.html`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp/widgets/templates/variables.html` & `pyrecdp-1.0.1b202305131/pyrecdp/widgets/templates/variables.html`

 * *Files identical despite different names*

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp.egg-info/PKG-INFO` & `pyrecdp-1.0.1b202305131/pyrecdp.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 Metadata-Version: 2.1
 Name: pyrecdp
-Version: 1.0.1b202304251
+Version: 1.0.1b202305131
 Summary: A data processing bundle for spark based recommender system operations
 Home-page: https://github.com/intel/e2eAIOK/
 Author: INTEL AIA
-Author-email: chendi.xue@intel.com
+License: UNKNOWN
 Project-URL: Bug Tracker, https://github.com/intel/e2eAIOK/
+Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -213,7 +214,9 @@
 
 ## LICENSE
 * Apache 2.0
 
 ## Dependency
 * Spark 3.x
 * python 3.*
+
+
```

### Comparing `pyrecdp-1.0.1b202304251/pyrecdp.egg-info/SOURCES.txt` & `pyrecdp-1.0.1b202305131/pyrecdp.egg-info/SOURCES.txt`

 * *Files 12% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 pyrecdp.egg-info/top_level.txt
 pyrecdp/ScalaProcessUtils/__init__.py
 pyrecdp/ScalaProcessUtils/spark-defaults.conf
 pyrecdp/ScalaProcessUtils/spark-env.sh
 pyrecdp/ScalaProcessUtils/target/recdp-scala-extensions-0.1.0-jar-with-dependencies.jar
 pyrecdp/autofe/AutoFE.py
 pyrecdp/autofe/BasePipeline.py
-pyrecdp/autofe/DataEstimator.py
+pyrecdp/autofe/FeatureEstimator.py
 pyrecdp/autofe/FeatureProfiler.py
 pyrecdp/autofe/FeatureWrangler.py
 pyrecdp/autofe/RelationalBuilder.py
 pyrecdp/autofe/__init__.py
 pyrecdp/core/__init__.py
 pyrecdp/core/dataframe.py
 pyrecdp/core/di_graph.py
@@ -34,14 +34,16 @@
 pyrecdp/datasets/download.py
 pyrecdp/datasets/ibm_fraud_detect.py
 pyrecdp/datasets/nyc_taxi.py
 pyrecdp/datasets/outbrain.py
 pyrecdp/datasets/pretrained.py
 pyrecdp/datasets/twitter_recsys.py
 pyrecdp/primitives/__init__.py
+pyrecdp/primitives/engines/__init__.py
+pyrecdp/primitives/engines/runner.py
 pyrecdp/primitives/estimators/__init__.py
 pyrecdp/primitives/estimators/base.py
 pyrecdp/primitives/estimators/lightgbm.py
 pyrecdp/primitives/generators/__init__.py
 pyrecdp/primitives/generators/base.py
 pyrecdp/primitives/generators/binned.py
 pyrecdp/primitives/generators/category.py
@@ -51,15 +53,14 @@
 pyrecdp/primitives/generators/feature_transform.py
 pyrecdp/primitives/generators/featuretools_adaptor.py
 pyrecdp/primitives/generators/fillna.py
 pyrecdp/primitives/generators/geograph.py
 pyrecdp/primitives/generators/name.py
 pyrecdp/primitives/generators/nlp.py
 pyrecdp/primitives/generators/relation.py
-pyrecdp/primitives/generators/statics.py
 pyrecdp/primitives/generators/type.py
 pyrecdp/primitives/operations/__init__.py
 pyrecdp/primitives/operations/base.py
 pyrecdp/primitives/operations/category.py
 pyrecdp/primitives/operations/custom.py
 pyrecdp/primitives/operations/data.py
 pyrecdp/primitives/operations/dataframe.py
@@ -68,14 +69,17 @@
 pyrecdp/primitives/operations/featuretools_adaptor.py
 pyrecdp/primitives/operations/fillna.py
 pyrecdp/primitives/operations/geograph.py
 pyrecdp/primitives/operations/merge.py
 pyrecdp/primitives/operations/name.py
 pyrecdp/primitives/operations/tuple.py
 pyrecdp/primitives/operations/type.py
+pyrecdp/primitives/profilers/__init__.py
+pyrecdp/primitives/profilers/statics.py
+pyrecdp/primitives/profilers/type_infer.py
 pyrecdp/primitives/spark_data_processor/__init__.py
 pyrecdp/primitives/spark_data_processor/data_processor.py
 pyrecdp/primitives/spark_data_processor/encoder.py
 pyrecdp/primitives/spark_data_processor/utils.py
 pyrecdp/widgets/BaseWidget.py
 pyrecdp/widgets/PlotWidget.py
 pyrecdp/widgets/ProfilerWidget.py
@@ -85,13 +89,8 @@
 pyrecdp/widgets/utils.py
 pyrecdp/widgets/templates/base.html
 pyrecdp/widgets/templates/error.html
 pyrecdp/widgets/templates/interactions.html
 pyrecdp/widgets/templates/overview.html
 pyrecdp/widgets/templates/scripts.html
 pyrecdp/widgets/templates/styles.html
-pyrecdp/widgets/templates/variables.html
-tests/test_data_estimator.py
-tests/test_feature_wrangler.py
-tests/test_pipeline_json.py
-tests/test_relational_builder.py
-tests/test_spark_dataprocessor.py
+pyrecdp/widgets/templates/variables.html
```

### Comparing `pyrecdp-1.0.1b202304251/setup.py` & `pyrecdp-1.0.1b202305131/setup.py`

 * *Files 26% similar despite different names*

```diff
@@ -3,17 +3,16 @@
 from setuptools.command.install import install
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
     
 setuptools.setup(
     name="pyrecdp",
-    version="1.0.1b202304251",
+    version="1.0.1b202305131",
     author="INTEL AIA",
-    author_email="chendi.xue@intel.com",
     description=
     "A data processing bundle for spark based recommender system operations",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url = "https://github.com/intel/e2eAIOK/",
     project_urls={
         "Bug Tracker": "https://github.com/intel/e2eAIOK/",
@@ -46,11 +45,10 @@
         "plotly",
         "shapely",
         "graphviz",
         "requests",
         "distro",
         "pyspark==3.3.1",
         "lightgbm",
-        "jupyter",
-        "docx2txt",
-        "openpyxl"
+        "jupyterlab",
+        "matplotlib"
         ])
```

