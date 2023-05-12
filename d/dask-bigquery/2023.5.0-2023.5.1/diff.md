# Comparing `tmp/dask-bigquery-2023.5.0.tar.gz` & `tmp/dask-bigquery-2023.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dask-bigquery-2023.5.0.tar", last modified: Wed May 10 18:11:30 2023, max compression
+gzip compressed data, was "dask-bigquery-2023.5.1.tar", last modified: Fri May 12 22:58:47 2023, max compression
```

## Comparing `dask-bigquery-2023.5.0.tar` & `dask-bigquery-2023.5.1.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-10 18:11:30.538303 dask-bigquery-2023.5.0/
--rw-r--r--   0 ncclementi   (501) staff       (20)     1514 2021-08-05 20:57:06.000000 dask-bigquery-2023.5.0/LICENSE
--rw-r--r--   0 ncclementi   (501) staff       (20)      133 2021-10-28 22:11:06.000000 dask-bigquery-2023.5.0/MANIFEST.in
--rw-r--r--   0 ncclementi   (501) staff       (20)     3683 2023-05-10 18:11:30.538367 dask-bigquery-2023.5.0/PKG-INFO
--rw-r--r--   0 ncclementi   (501) staff       (20)     3446 2023-05-10 16:54:19.000000 dask-bigquery-2023.5.0/README.md
-drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-10 18:11:30.537287 dask-bigquery-2023.5.0/dask_bigquery/
--rw-r--r--   0 ncclementi   (501) staff       (20)       62 2023-05-10 18:03:32.000000 dask-bigquery-2023.5.0/dask_bigquery/__init__.py
--rw-r--r--   0 ncclementi   (501) staff       (20)    12446 2023-05-09 17:54:09.000000 dask-bigquery-2023.5.0/dask_bigquery/core.py
-drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-10 18:11:30.538187 dask-bigquery-2023.5.0/dask_bigquery/tests/
--rw-r--r--   0 ncclementi   (501) staff       (20)     8275 2023-05-09 17:54:09.000000 dask-bigquery-2023.5.0/dask_bigquery/tests/test_core.py
-drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-10 18:11:30.538061 dask-bigquery-2023.5.0/dask_bigquery.egg-info/
--rw-r--r--   0 ncclementi   (501) staff       (20)     3683 2023-05-10 18:11:30.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/PKG-INFO
--rw-r--r--   0 ncclementi   (501) staff       (20)      366 2023-05-10 18:11:30.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/SOURCES.txt
--rw-r--r--   0 ncclementi   (501) staff       (20)        1 2023-05-10 18:11:30.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/dependency_links.txt
--rw-r--r--   0 ncclementi   (501) staff       (20)        1 2022-05-02 18:33:27.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/not-zip-safe
--rw-r--r--   0 ncclementi   (501) staff       (20)      133 2023-05-10 18:11:30.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/requires.txt
--rw-r--r--   0 ncclementi   (501) staff       (20)       14 2023-05-10 18:11:30.000000 dask-bigquery-2023.5.0/dask_bigquery.egg-info/top_level.txt
--rw-r--r--   0 ncclementi   (501) staff       (20)       88 2023-05-09 17:54:09.000000 dask-bigquery-2023.5.0/requirements.txt
--rw-r--r--   0 ncclementi   (501) staff       (20)      106 2023-05-10 18:11:30.538592 dask-bigquery-2023.5.0/setup.cfg
--rw-r--r--   0 ncclementi   (501) staff       (20)      619 2023-05-10 18:03:32.000000 dask-bigquery-2023.5.0/setup.py
+drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-12 22:58:47.474959 dask-bigquery-2023.5.1/
+-rw-r--r--   0 ncclementi   (501) staff       (20)     1514 2021-08-05 20:57:06.000000 dask-bigquery-2023.5.1/LICENSE
+-rw-r--r--   0 ncclementi   (501) staff       (20)      133 2021-10-28 22:11:06.000000 dask-bigquery-2023.5.1/MANIFEST.in
+-rw-r--r--   0 ncclementi   (501) staff       (20)     4687 2023-05-12 22:58:47.475047 dask-bigquery-2023.5.1/PKG-INFO
+-rw-r--r--   0 ncclementi   (501) staff       (20)     4450 2023-05-12 22:53:05.000000 dask-bigquery-2023.5.1/README.md
+drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-12 22:58:47.473346 dask-bigquery-2023.5.1/dask_bigquery/
+-rw-r--r--   0 ncclementi   (501) staff       (20)       62 2023-05-12 22:54:31.000000 dask-bigquery-2023.5.1/dask_bigquery/__init__.py
+-rw-r--r--   0 ncclementi   (501) staff       (20)    12370 2023-05-12 22:53:05.000000 dask-bigquery-2023.5.1/dask_bigquery/core.py
+drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-12 22:58:47.474703 dask-bigquery-2023.5.1/dask_bigquery/tests/
+-rw-r--r--   0 ncclementi   (501) staff       (20)    10021 2023-05-12 22:53:05.000000 dask-bigquery-2023.5.1/dask_bigquery/tests/test_core.py
+drwxr-xr-x   0 ncclementi   (501) staff       (20)        0 2023-05-12 22:58:47.474564 dask-bigquery-2023.5.1/dask_bigquery.egg-info/
+-rw-r--r--   0 ncclementi   (501) staff       (20)     4687 2023-05-12 22:58:47.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/PKG-INFO
+-rw-r--r--   0 ncclementi   (501) staff       (20)      366 2023-05-12 22:58:47.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/SOURCES.txt
+-rw-r--r--   0 ncclementi   (501) staff       (20)        1 2023-05-12 22:58:47.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/dependency_links.txt
+-rw-r--r--   0 ncclementi   (501) staff       (20)        1 2022-05-02 18:33:27.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/not-zip-safe
+-rw-r--r--   0 ncclementi   (501) staff       (20)      133 2023-05-12 22:58:47.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/requires.txt
+-rw-r--r--   0 ncclementi   (501) staff       (20)       14 2023-05-12 22:58:47.000000 dask-bigquery-2023.5.1/dask_bigquery.egg-info/top_level.txt
+-rw-r--r--   0 ncclementi   (501) staff       (20)       88 2023-05-09 17:54:09.000000 dask-bigquery-2023.5.1/requirements.txt
+-rw-r--r--   0 ncclementi   (501) staff       (20)      106 2023-05-12 22:58:47.475313 dask-bigquery-2023.5.1/setup.cfg
+-rw-r--r--   0 ncclementi   (501) staff       (20)      619 2023-05-12 22:54:44.000000 dask-bigquery-2023.5.1/setup.py
```

### Comparing `dask-bigquery-2023.5.0/LICENSE` & `dask-bigquery-2023.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `dask-bigquery-2023.5.0/PKG-INFO` & `dask-bigquery-2023.5.1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: dask-bigquery
-Version: 2023.5.0
+Version: 2023.5.1
 Summary: Dask + BigQuery integration
 License: BSD
 Platform: UNKNOWN
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # Dask-BigQuery
 
 [![Tests](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml) [![Linting](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml)
 
-Read data from [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
+Read/write data from/to [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
 
 This package uses the BigQuery Storage API. Please refer to the [data extraction pricing table](https://cloud.google.com/bigquery/pricing#data_extraction_pricing) for associated costs while using Dask-BigQuery.
 
 ## Installation
 
 `dask-bigquery` can be installed with `pip`:
 
@@ -27,17 +27,43 @@
 
 or with `conda`:
 
 ```
 conda install -c conda-forge dask-bigquery
 ```
 
+## Google Cloud permissions
+
+For reading from BiqQuery, you need the following roles to be enabled on the account:
+
+- `BigQuery Read Session User`
+- `BigQuery Data Viewer`, `BigQuery Data Editor`, or `BigQuery Data Owner`
+
+Alternately, `BigQuery Admin` would give you full access to sessions and data.
+
+For writing to BigQuery, the following roles are sufficient:
+
+- `BigQuery Data Editor`
+- `Storage Object Creator`
+
+The minimal permissions to cover reading and writing:
+
+- `BigQuery Data Editor`
+- `BigQuery Read Session User`
+- `Storage Object Creator`
+
 ## Authentication
 
-Default credentials can be provided by setting the environment variable `GOOGLE_APPLICATION_CREDENTIALS` to the file name:
+By default, `dask-bigquery` will use the [Application Default Credentials](https://cloud.google.com/docs/authentication/provide-credentials-adc). When running code locally, you can set this to use your user credentials by running
+
+```sh
+$ gcloud auth application-default login
+```
+
+User credentials require interactive login. For settings where this isn't possible, you'll need to create a service account. You can set the Application Default Credentials to the service account key using the `GOOGLE_APPLICATION_CREDENTIALS` environment variable:
 
 ```sh
 $ export GOOGLE_APPLICATION_CREDENTIALS=/home/<username>/google.json
 ```
 
 For information on obtaining the credentials, use [Google API documentation](https://developers.google.com/workspace/guides/create-credentials).
 
@@ -89,15 +115,15 @@
     project_id="my_project_id",
     dataset_id="my_dataset_id",
     table_id="my_table_name",
     credentials=credentials,
 )
 ```
 
-Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `dask-bigquery-tmp`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
+Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `<your_project_id>-dask-bigquery`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
 
 If you're using a persistent bucket, we recommend configuring a retention policy that ensures the data is cleaned up even in case of job failures.
 
 ## Run tests locally
 
 To run the tests locally you need to be authenticated and have a project created on that account. If you're using a service account, when created you need to select the role of "BigQuery Admin" in the section "Grant this service account access to project".
```

### Comparing `dask-bigquery-2023.5.0/README.md` & `dask-bigquery-2023.5.1/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Dask-BigQuery
 
 [![Tests](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml) [![Linting](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml)
 
-Read data from [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
+Read/write data from/to [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
 
 This package uses the BigQuery Storage API. Please refer to the [data extraction pricing table](https://cloud.google.com/bigquery/pricing#data_extraction_pricing) for associated costs while using Dask-BigQuery.
 
 ## Installation
 
 `dask-bigquery` can be installed with `pip`:
 
@@ -16,17 +16,43 @@
 
 or with `conda`:
 
 ```
 conda install -c conda-forge dask-bigquery
 ```
 
+## Google Cloud permissions
+
+For reading from BiqQuery, you need the following roles to be enabled on the account:
+
+- `BigQuery Read Session User`
+- `BigQuery Data Viewer`, `BigQuery Data Editor`, or `BigQuery Data Owner`
+
+Alternately, `BigQuery Admin` would give you full access to sessions and data.
+
+For writing to BigQuery, the following roles are sufficient:
+
+- `BigQuery Data Editor`
+- `Storage Object Creator`
+
+The minimal permissions to cover reading and writing:
+
+- `BigQuery Data Editor`
+- `BigQuery Read Session User`
+- `Storage Object Creator`
+
 ## Authentication
 
-Default credentials can be provided by setting the environment variable `GOOGLE_APPLICATION_CREDENTIALS` to the file name:
+By default, `dask-bigquery` will use the [Application Default Credentials](https://cloud.google.com/docs/authentication/provide-credentials-adc). When running code locally, you can set this to use your user credentials by running
+
+```sh
+$ gcloud auth application-default login
+```
+
+User credentials require interactive login. For settings where this isn't possible, you'll need to create a service account. You can set the Application Default Credentials to the service account key using the `GOOGLE_APPLICATION_CREDENTIALS` environment variable:
 
 ```sh
 $ export GOOGLE_APPLICATION_CREDENTIALS=/home/<username>/google.json
 ```
 
 For information on obtaining the credentials, use [Google API documentation](https://developers.google.com/workspace/guides/create-credentials).
 
@@ -78,15 +104,15 @@
     project_id="my_project_id",
     dataset_id="my_dataset_id",
     table_id="my_table_name",
     credentials=credentials,
 )
 ```
 
-Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `dask-bigquery-tmp`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
+Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `<your_project_id>-dask-bigquery`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
 
 If you're using a persistent bucket, we recommend configuring a retention policy that ensures the data is cleaned up even in case of job failures.
 
 ## Run tests locally
 
 To run the tests locally you need to be authenticated and have a project created on that account. If you're using a service account, when created you need to select the role of "BigQuery Admin" in the section "Grant this service account access to project".
```

### Comparing `dask-bigquery-2023.5.0/dask_bigquery/core.py` & `dask-bigquery-2023.5.1/dask_bigquery/core.py`

 * *Files 2% similar despite different names*

```diff
@@ -160,34 +160,30 @@
     read_kwargs = read_kwargs or {}
     arrow_options = arrow_options or {}
     with bigquery_clients(project_id) as (bq_client, bqs_client):
         table_ref = bq_client.get_table(f"{dataset_id}.{table_id}")
         if table_ref.table_type == "VIEW":
             raise TypeError("Table type VIEW not supported")
 
-        def make_create_read_session_request(row_filter="", max_stream_count=0):
+        def make_create_read_session_request():
             return bigquery_storage.types.CreateReadSessionRequest(
                 max_stream_count=max_stream_count,  # 0 -> use as many as BQ Storage will provide
                 parent=f"projects/{project_id}",
                 read_session=bigquery_storage.types.ReadSession(
                     data_format=bigquery_storage.types.DataFormat.ARROW,
                     read_options=bigquery_storage.types.ReadSession.TableReadOptions(
                         row_restriction=row_filter, selected_fields=columns
                     ),
                     table=table_ref.to_bqstorage(),
                 ),
             )
 
         # Create a read session in order to detect the schema.
         # Read sessions are light weight and will be auto-deleted after 24 hours.
-        session = bqs_client.create_read_session(
-            make_create_read_session_request(
-                row_filter=row_filter, max_stream_count=max_stream_count
-            )
-        )
+        session = bqs_client.create_read_session(make_create_read_session_request())
         schema = pyarrow.ipc.read_schema(
             pyarrow.py_buffer(session.arrow_schema.serialized_schema)
         )
         meta = schema.empty_table().to_pandas(**arrow_options)
 
         label = "read-gbq-"
         output_name = label + tokenize(
@@ -219,15 +215,15 @@
 
 def to_gbq(
     df,
     *,
     project_id: str,
     dataset_id: str,
     table_id: str,
-    bucket: str = "dask-bigquery-tmp",
+    bucket: str = None,
     credentials: Credentials = None,
     delete_bucket: bool = False,
     parquet_kwargs: dict = None,
     load_job_kwargs: dict = None,
 ):
     """Write dask dataframe as table using BigQuery LoadJob.
 
@@ -238,15 +234,15 @@
     project_id: str
       Name of the BigQuery project id. If service account credentials are specified, and this
       parameter is None, project_id will be taken from credentials.
     dataset_id: str
       BigQuery dataset within project
     table_id: str
       BigQuery table within dataset
-    bucket: str, default: dask-bigquery-tmp
+    bucket: str, default: {project_id}-dask-bigquery
       Google Cloud Storage bucket name, for intermediary parquet storage. If the bucket doesn't
       exist, it will be created. The account you're using will need Google Cloud Storage
       permissions (storage.objects.create, storage.buckets.create). If a persistent bucket is used,
       it is recommended to configure a retention policy that ensures the data is cleaned up in
       case of job failures.
     credentials : google.auth.credentials.Credentials, optional
       Credentials for accessing Google APIs. Use this parameter to override
@@ -276,14 +272,17 @@
         load_job_kwargs_used.update(load_job_kwargs)
 
     load_job_kwargs_used["autodetect"] = "schema" not in load_job_kwargs_used
 
     # override the following kwargs, even if user specified them
     load_job_kwargs_used["source_format"] = bigquery.SourceFormat.PARQUET
 
+    if bucket is None:
+        bucket = f"{project_id}-dask-bigquery"
+
     fs = gcs_fs(project_id, credentials=credentials)
     if fs.exists(bucket):
         if delete_bucket:
             # if we didn't create it, we shouldn't delete it
             warnings.warn(
                 "`delete_bucket=True` can only be used with a non-existing bucket.",
                 category=UserWarning,
```

### Comparing `dask-bigquery-2023.5.0/dask_bigquery/tests/test_core.py` & `dask-bigquery-2023.5.1/dask_bigquery/tests/test_core.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,69 +11,108 @@
 import pytest
 from dask.dataframe.utils import assert_eq
 from distributed.utils_test import cleanup  # noqa: F401
 from distributed.utils_test import client  # noqa: F401
 from distributed.utils_test import cluster_fixture  # noqa: F401
 from distributed.utils_test import loop  # noqa: F401
 from distributed.utils_test import loop_in_thread  # noqa: F401
+from google.api_core.exceptions import InvalidArgument
 from google.cloud import bigquery
 
 from dask_bigquery import read_gbq, to_gbq
 
 
-@pytest.fixture
+@pytest.fixture(scope="module")
 def df():
     records = [
         {
             "name": random.choice(["fred", "wilma", "barney", "betty"]),
             "number": random.randint(0, 100),
             "timestamp": datetime.now(timezone.utc) - timedelta(days=i % 2),
             "idx": i,
         }
         for i in range(10)
     ]
 
     yield pd.DataFrame(records)
 
 
-@pytest.fixture
-def dataset(df):
+@pytest.fixture(scope="module")
+def dataset():
     project_id = os.environ.get("DASK_BIGQUERY_PROJECT_ID")
     if not project_id:
         credentials, project_id = google.auth.default()
     dataset_id = uuid.uuid4().hex
+
+    with bigquery.Client() as bq_client:
+        dataset = bigquery.Dataset(f"{project_id}.{dataset_id}")
+        bq_client.create_dataset(dataset)
+
+        yield dataset
+
+        bq_client.delete_dataset(
+            dataset=f"{project_id}.{dataset_id}",
+            delete_contents=True,
+        )
+
+
+@pytest.fixture(scope="module")
+def table(dataset, df):
+    project_id = dataset.project
+    dataset_id = dataset.dataset_id
     table_id = "table_test"
-    # push data to gbq
 
     time_partitioning = bigquery.TimePartitioning(
         type_=bigquery.TimePartitioningType.DAY,
         field="timestamp",
-    )  # field to use for partitioning
+    )
 
     job_config = bigquery.LoadJobConfig(
         write_disposition="WRITE_TRUNCATE", time_partitioning=time_partitioning
     )
 
     with bigquery.Client() as bq_client:
-        dataset = bigquery.Dataset(f"{project_id}.{dataset_id}")
-        bq_client.create_dataset(dataset)
         job = bq_client.load_table_from_dataframe(
             df,
             destination=f"{project_id}.{dataset_id}.{table_id}",
             job_config=job_config,
         )  # Make an API request.
         job.result()
 
     yield (project_id, dataset_id, table_id)
 
+
+@pytest.fixture(scope="module")
+def required_partition_filter_table(dataset, df):
+    project_id = dataset.project
+    dataset_id = dataset.dataset_id
+    table_id = "partitioned_table_test"
+
+    time_partitioning = bigquery.TimePartitioning(
+        type_=bigquery.TimePartitioningType.DAY,
+        field="timestamp",
+    )
+
+    job_config = bigquery.LoadJobConfig(
+        write_disposition="WRITE_TRUNCATE",
+        time_partitioning=time_partitioning,
+    )
+
     with bigquery.Client() as bq_client:
-        bq_client.delete_dataset(
-            dataset=f"{project_id}.{dataset_id}",
-            delete_contents=True,
-        )
+        job = bq_client.load_table_from_dataframe(
+            df,
+            destination=f"{project_id}.{dataset_id}.{table_id}",
+            job_config=job_config,
+        )  # Make an API request.
+        job.result()
+        table = bq_client.get_table(f"{project_id}.{dataset_id}.{table_id}")
+        table.require_partition_filter = True
+        bq_client.update_table(table, ["require_partition_filter"])
+
+    yield (project_id, dataset_id, table_id)
 
 
 @pytest.fixture
 def bucket():
     credentials, project_id = google.auth.default()
     env_project_id = os.environ.get("DASK_BIGQUERY_PROJECT_ID")
     if env_project_id:
@@ -181,18 +220,19 @@
         assert not fs.exists(bucket)
     else:
         # bucket should be empty
         assert fs.exists(bucket)
         assert len(fs.ls(bucket, detail=False)) == 0
 
 
-def test_to_gbq_with_credentials(df, write_dataset):
+def test_to_gbq_with_credentials(df, write_dataset, monkeypatch):
     credentials, project_id, dataset_id = write_dataset
     ddf = dd.from_pandas(df, npartitions=2)
 
+    monkeypatch.delenv("GOOGLE_DEFAULT_CREDENTIALS", raising=False)
     # with explicit credentials
     result = to_gbq(
         ddf,
         project_id=project_id,
         dataset_id=dataset_id,
         table_id="table_to_write",
         credentials=credentials,
@@ -211,77 +251,96 @@
     assert result.state == "DONE"
 
     ddf_out = read_gbq(project_id=project_id, dataset_id=dataset_id, table_id=table_id)
     # bigquery does not guarantee ordering, so let's reindex
     assert_eq(ddf.set_index("idx"), ddf_out.set_index("idx"))
 
 
-def test_read_gbq(df, dataset, client):
-    project_id, dataset_id, table_id = dataset
+def test_read_gbq(df, table, client):
+    project_id, dataset_id, table_id = table
     ddf = read_gbq(project_id=project_id, dataset_id=dataset_id, table_id=table_id)
 
     assert list(ddf.columns) == ["name", "number", "timestamp", "idx"]
     assert assert_eq(ddf.set_index("idx"), df.set_index("idx"))
 
 
-def test_read_row_filter(df, dataset, client):
-    project_id, dataset_id, table_id = dataset
+def test_read_row_filter(df, table, client):
+    project_id, dataset_id, table_id = table
     ddf = read_gbq(
         project_id=project_id,
         dataset_id=dataset_id,
         table_id=table_id,
         row_filter="idx < 5",
     )
 
     assert list(ddf.columns) == ["name", "number", "timestamp", "idx"]
     assert assert_eq(ddf.set_index("idx").loc[:4], df.set_index("idx").loc[:4])
 
 
-def test_read_kwargs(dataset, client):
-    project_id, dataset_id, table_id = dataset
+def test_read_kwargs(table, client):
+    project_id, dataset_id, table_id = table
     ddf = read_gbq(
         project_id=project_id,
         dataset_id=dataset_id,
         table_id=table_id,
         read_kwargs={"timeout": 1e-12},
     )
 
     with pytest.raises(Exception, match="Deadline"):
         ddf.compute()
 
 
-def test_read_columns(df, dataset, client):
-    project_id, dataset_id, table_id = dataset
+def test_read_columns(df, table, client):
+    project_id, dataset_id, table_id = table
     assert df.shape[1] > 1, "Test data should have multiple columns"
 
     columns = ["name"]
     ddf = read_gbq(
         project_id=project_id,
         dataset_id=dataset_id,
         table_id=table_id,
         columns=columns,
     )
     assert list(ddf.columns) == columns
 
 
-def test_max_streams(df, dataset, client):
-    project_id, dataset_id, table_id = dataset
+def test_max_streams(df, table, client):
+    project_id, dataset_id, table_id = table
     ddf = read_gbq(
         project_id=project_id,
         dataset_id=dataset_id,
         table_id=table_id,
         max_stream_count=1,
     )
     assert ddf.npartitions == 1
 
 
-def test_arrow_options(dataset):
-    project_id, dataset_id, table_id = dataset
+def test_arrow_options(table):
+    project_id, dataset_id, table_id = table
     ddf = read_gbq(
         project_id=project_id,
         dataset_id=dataset_id,
         table_id=table_id,
         arrow_options={
             "types_mapper": {pa.string(): pd.StringDtype(storage="pyarrow")}.get
         },
     )
     assert ddf.dtypes["name"] == pd.StringDtype(storage="pyarrow")
+
+
+def test_read_required_partition_filter(df, required_partition_filter_table):
+    project_id, dataset_id, table_id = required_partition_filter_table
+
+    with pytest.raises(InvalidArgument):
+        read_gbq(
+            project_id=project_id,
+            dataset_id=dataset_id,
+            table_id=table_id,
+        ).head()
+
+    df = read_gbq(
+        project_id=project_id,
+        dataset_id=dataset_id,
+        table_id=table_id,
+        row_filter=f"DATE(timestamp)='{df.timestamp.min().date()}'",
+    ).head()
+    assert not df.empty
```

### Comparing `dask-bigquery-2023.5.0/dask_bigquery.egg-info/PKG-INFO` & `dask-bigquery-2023.5.1/dask_bigquery.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: dask-bigquery
-Version: 2023.5.0
+Version: 2023.5.1
 Summary: Dask + BigQuery integration
 License: BSD
 Platform: UNKNOWN
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # Dask-BigQuery
 
 [![Tests](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/tests.yml) [![Linting](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml/badge.svg)](https://github.com/coiled/dask-bigquery/actions/workflows/pre-commit.yml)
 
-Read data from [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
+Read/write data from/to [Google BigQuery](https://cloud.google.com/bigquery) with Dask.
 
 This package uses the BigQuery Storage API. Please refer to the [data extraction pricing table](https://cloud.google.com/bigquery/pricing#data_extraction_pricing) for associated costs while using Dask-BigQuery.
 
 ## Installation
 
 `dask-bigquery` can be installed with `pip`:
 
@@ -27,17 +27,43 @@
 
 or with `conda`:
 
 ```
 conda install -c conda-forge dask-bigquery
 ```
 
+## Google Cloud permissions
+
+For reading from BiqQuery, you need the following roles to be enabled on the account:
+
+- `BigQuery Read Session User`
+- `BigQuery Data Viewer`, `BigQuery Data Editor`, or `BigQuery Data Owner`
+
+Alternately, `BigQuery Admin` would give you full access to sessions and data.
+
+For writing to BigQuery, the following roles are sufficient:
+
+- `BigQuery Data Editor`
+- `Storage Object Creator`
+
+The minimal permissions to cover reading and writing:
+
+- `BigQuery Data Editor`
+- `BigQuery Read Session User`
+- `Storage Object Creator`
+
 ## Authentication
 
-Default credentials can be provided by setting the environment variable `GOOGLE_APPLICATION_CREDENTIALS` to the file name:
+By default, `dask-bigquery` will use the [Application Default Credentials](https://cloud.google.com/docs/authentication/provide-credentials-adc). When running code locally, you can set this to use your user credentials by running
+
+```sh
+$ gcloud auth application-default login
+```
+
+User credentials require interactive login. For settings where this isn't possible, you'll need to create a service account. You can set the Application Default Credentials to the service account key using the `GOOGLE_APPLICATION_CREDENTIALS` environment variable:
 
 ```sh
 $ export GOOGLE_APPLICATION_CREDENTIALS=/home/<username>/google.json
 ```
 
 For information on obtaining the credentials, use [Google API documentation](https://developers.google.com/workspace/guides/create-credentials).
 
@@ -89,15 +115,15 @@
     project_id="my_project_id",
     dataset_id="my_dataset_id",
     table_id="my_table_name",
     credentials=credentials,
 )
 ```
 
-Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `dask-bigquery-tmp`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
+Before loading data into BigQuery, `to_gbq` writes intermediary Parquet to a Google Storage bucket. Default bucket name is `<your_project_id>-dask-bigquery`. You can provide a diferent bucket name by setting the parameter: `bucket="my-gs-bucket"`. After the job is done, the intermediary data is deleted.
 
 If you're using a persistent bucket, we recommend configuring a retention policy that ensures the data is cleaned up even in case of job failures.
 
 ## Run tests locally
 
 To run the tests locally you need to be authenticated and have a project created on that account. If you're using a service account, when created you need to select the role of "BigQuery Admin" in the section "Grant this service account access to project".
```

### Comparing `dask-bigquery-2023.5.0/setup.py` & `dask-bigquery-2023.5.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from setuptools import setup
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description = f.read()
 
 setup(
     name="dask-bigquery",
-    version="2023.05.0",
+    version="2023.05.1",
     description="Dask + BigQuery integration",
     license="BSD",
     packages=["dask_bigquery"],
     long_description=long_description,
     long_description_content_type="text/markdown",
     python_requires=">=3.8",
     install_requires=open("requirements.txt").read().strip().split("\n"),
```

