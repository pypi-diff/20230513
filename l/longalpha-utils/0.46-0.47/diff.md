# Comparing `tmp/longalpha_utils-0.46.tar.gz` & `tmp/longalpha_utils-0.47.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "longalpha_utils-0.46.tar", last modified: Tue May  9 03:18:51 2023, max compression
+gzip compressed data, was "longalpha_utils-0.47.tar", last modified: Sat May 13 17:37:32 2023, max compression
```

## Comparing `longalpha_utils-0.46.tar` & `longalpha_utils-0.47.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 03:18:51.588094 longalpha_utils-0.46/
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-09 03:18:51.588094 longalpha_utils-0.46/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 03:18:51.588094 longalpha_utils-0.46/longalpha_utils/
--rw-r--r--   0 runner    (1001) docker     (123)      116 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/messenger.py
--rw-r--r--   0 runner    (1001) docker     (123)     9562 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/transfers.py
--rw-r--r--   0 runner    (1001) docker     (123)     4073 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/us_stock_holidays.py
--rw-r--r--   0 runner    (1001) docker     (123)      641 2023-05-09 03:18:40.000000 longalpha_utils-0.46/longalpha_utils/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 03:18:51.588094 longalpha_utils-0.46/longalpha_utils.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-09 03:18:51.000000 longalpha_utils-0.46/longalpha_utils.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      379 2023-05-09 03:18:51.000000 longalpha_utils-0.46/longalpha_utils.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 03:18:51.000000 longalpha_utils-0.46/longalpha_utils.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-09 03:18:51.000000 longalpha_utils-0.46/longalpha_utils.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-09 03:18:51.000000 longalpha_utils-0.46/longalpha_utils.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-09 03:18:51.588094 longalpha_utils-0.46/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1086 2023-05-09 03:18:40.000000 longalpha_utils-0.46/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:37:32.495860 longalpha_utils-0.47/
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 17:37:32.495860 longalpha_utils-0.47/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:37:32.491860 longalpha_utils-0.47/longalpha_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      116 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/messenger.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10698 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/transfers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4073 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/us_stock_holidays.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1121 2023-05-13 17:37:19.000000 longalpha_utils-0.47/longalpha_utils/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:37:32.495860 longalpha_utils-0.47/longalpha_utils.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 17:37:32.000000 longalpha_utils-0.47/longalpha_utils.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      379 2023-05-13 17:37:32.000000 longalpha_utils-0.47/longalpha_utils.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:37:32.000000 longalpha_utils-0.47/longalpha_utils.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-13 17:37:32.000000 longalpha_utils-0.47/longalpha_utils.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 17:37:32.000000 longalpha_utils-0.47/longalpha_utils.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:37:32.495860 longalpha_utils-0.47/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1086 2023-05-13 17:37:19.000000 longalpha_utils-0.47/setup.py
```

### Comparing `longalpha_utils-0.46/longalpha_utils/messenger.py` & `longalpha_utils-0.47/longalpha_utils/messenger.py`

 * *Files identical despite different names*

### Comparing `longalpha_utils-0.46/longalpha_utils/transfers.py` & `longalpha_utils-0.47/longalpha_utils/transfers.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,20 +1,74 @@
 import os
 import tempfile
 from io import BytesIO
-from typing import List, Optional, Dict, Any
+from typing import List, Optional, Dict, Any, Union
 import pandas as pd
 from minio import Minio
 from pyspark.conf import SparkConf
 from pyspark.sql import SparkSession, DataFrame
 from sqlalchemy import Engine
 from sqlalchemy import create_engine
 from sqlalchemy import text
 from minio.error import S3Error
+from datetime import date, timedelta
+from pyspark.sql.utils import AnalysisException
+from longalpha_utils.utils import  multi_union_by_name
+def init_spark(
+    spark_executor_memory: str = "30g",
+    spark_driver_memory: str = "90g",
+    minio_endpoint: Optional[str] = None,
+    minio_access_key: Optional[str] = None,
+    minio_secret_key: Optional[str] = None,
+) -> SparkSession:
+    """
+    get a spark instance.
+
+    if connect_psql is True, then we will connect to psql.
+    if minio_endpoint is not None, then we will connect to minio.
+    if both are None, then we will connect to local spark.
+
+    Note that we are not downloading jars here. We use spark.jars.packages to download jars.
+
+    Args:
+        minio_endpoint: minio_endpoint
+        minio_access_key:  minio_access_key
+        minio_secret_key:  minio_secret_key
+        spark_executor_memory: size of spark_executor_memory
+        spark_driver_memory: size of spark_driver_memory
+    Returns:
+
+    """
+    jars = [
+        "org.postgresql:postgresql:42.5.2",
+        "org.apache.hadoop:hadoop-aws:3.3.2",
+        "com.amazonaws:aws-java-sdk-bundle:1.12.405",
+    ]
+
+    spark_conf = (
+        SparkConf()
+        .set("spark.executor.memory", spark_executor_memory)
+        .set("spark.driver.memory", spark_driver_memory)
+        .set("spark.sql.execution.arrow.pyspark.enabled", "true")
+        .set("spark.ui.port", "4043")
+        .set(
+            "spark.jars.packages", ",".join(jars)
+        )  # if you set park.jars.packages more than once, only the last one will be used.
+        .set("spark.hadoop.fs.s3a.impl", "org.apache.hadoop.fs.s3a.S3AFileSystem")
+        .set("spark.hadoop.fs.s3a.path.style.access ", "true")
+    )
+    spark = SparkSession.builder.config(conf=spark_conf).getOrCreate()
+
+    if minio_endpoint is not None:
+        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.endpoint", minio_endpoint)
+        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.access.key", minio_access_key)
+        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.secret.key", minio_secret_key)
+        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.connection.ssl.enabled", "false")
 
+    return spark
 
 class MinioWrapper:
     def __init__(self, minio_url, minio_access_key, minio_secret_key):
         self.minio_client = Minio(
             endpoint=minio_url,
             access_key=minio_access_key,
             secret_key=minio_secret_key,
@@ -118,66 +172,44 @@
         latest_obj = time_obj[latest_time]
         return self.get(bucket_name=bucket_name, object_name=latest_obj.object_name)
 
     def list(self, bucket_name: str) -> List[str]:
         return [i.object_name for i in self.minio_client.list_objects(bucket_name)]
 
 
-def init_spark(
-    spark_executor_memory: str = "30g",
-    spark_driver_memory: str = "90g",
-    minio_endpoint: Optional[str] = None,
-    minio_access_key: Optional[str] = None,
-    minio_secret_key: Optional[str] = None,
-) -> SparkSession:
-    """
-    get a spark instance.
 
-    if connect_psql is True, then we will connect to psql.
-    if minio_endpoint is not None, then we will connect to minio.
-    if both are None, then we will connect to local spark.
-
-    Note that we are not downloading jars here. We use spark.jars.packages to download jars.
-
-    Args:
-        minio_endpoint: minio_endpoint
-        minio_access_key:  minio_access_key
-        minio_secret_key:  minio_secret_key
-        spark_executor_memory: size of spark_executor_memory
-        spark_driver_memory: size of spark_driver_memory
-    Returns:
 
+def get_s3_data_spark(
+        spark: SparkSession, start_date: date, end_date: date, bucket: str, subfolder: str,
+) -> Union[DataFrame, None]:
     """
-    jars = [
-        "org.postgresql:postgresql:42.5.2",
-        "org.apache.hadoop:hadoop-aws:3.3.2",
-        "com.amazonaws:aws-java-sdk-bundle:1.12.405",
-    ]
+    Get options data from minio
+    Args:
+        spark: spark session
+        start_date: start date to get options data for
+        end_date: end date to get options data for
 
-    spark_conf = (
-        SparkConf()
-        .set("spark.executor.memory", spark_executor_memory)
-        .set("spark.driver.memory", spark_driver_memory)
-        .set("spark.sql.execution.arrow.pyspark.enabled", "true")
-        .set("spark.ui.port", "4043")
-        .set(
-            "spark.jars.packages", ",".join(jars)
-        )  # if you set park.jars.packages more than once, only the last one will be used.
-        .set("spark.hadoop.fs.s3a.impl", "org.apache.hadoop.fs.s3a.S3AFileSystem")
-        .set("spark.hadoop.fs.s3a.path.style.access ", "true")
-    )
-    spark = SparkSession.builder.config(conf=spark_conf).getOrCreate()
+    Returns: options data if exists, None otherwise.
+    Note returned options data is in wide format with calls and puts on the same row
 
-    if minio_endpoint is not None:
-        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.endpoint", minio_endpoint)
-        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.access.key", minio_access_key)
-        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.secret.key", minio_secret_key)
-        spark.sparkContext._jsc.hadoopConfiguration().set("fs.s3a.connection.ssl.enabled", "false")
+    """
+    options = []
+    while start_date <= end_date:
+        file_s3_path = "s3a://" +os.path.join(bucket, f"{subfolder}/{start_date}.parquet")
+        try:
+            option = spark.read.parquet(file_s3_path)
+            options.append(option)
+        except AnalysisException:
+            print(f"Options data for {start_date} does not exist.")
+        start_date += timedelta(days=1)
+    if len(options) == 0:
+        return None
+    unioned_options = multi_union_by_name(options)
+    return unioned_options
 
-    return spark
 
 
 def spark_read_psql(
     spark: SparkSession, psql_url: str, psql_db: str, psql_table: str, psql_usr: str, psql_pwd: str
 ) -> DataFrame:
     """
     use spark to read psql
```

### Comparing `longalpha_utils-0.46/longalpha_utils/us_stock_holidays.py` & `longalpha_utils-0.47/longalpha_utils/us_stock_holidays.py`

 * *Files identical despite different names*

### Comparing `longalpha_utils-0.46/longalpha_utils.egg-info/requires.txt` & `longalpha_utils-0.47/longalpha_utils.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `longalpha_utils-0.46/setup.py` & `longalpha_utils-0.47/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -38,11 +38,11 @@
     "typing_extensions==4.4.0",
     "urllib3==1.26.14",
     "yagmail==0.15.293",
 ]
 
 setup(
     name="longalpha_utils",
-    version="0.46",
+    version="0.47",
     long_description="Shared utilities for long alpha projects",
     install_requires=REQUIREMENTS,
 )
```

