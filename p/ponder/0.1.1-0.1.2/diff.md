# Comparing `tmp/ponder-0.1.1-cp39-cp39-win_amd64.whl.zip` & `tmp/ponder-0.1.2-cp39-cp39-win_amd64.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 1757792 bytes, number of entries: 7
--rw-rw-rw-  2.0 fat  4985856 b- defN 23-Apr-21 02:00 ponder.cp39-win_amd64.pyd
--rw-rw-rw-  2.0 fat    11254 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/LICENSE.txt
--rw-rw-rw-  2.0 fat      800 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/METADATA
--rw-rw-rw-  2.0 fat       94 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/WHEEL
--rw-rw-rw-  2.0 fat       53 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/entry_points.txt
--rw-rw-rw-  2.0 fat        7 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/top_level.txt
--rw-rw-r--  2.0 fat      563 b- defN 23-Apr-21 02:00 ponder-0.1.1.dist-info/RECORD
-7 files, 4998627 bytes uncompressed, 1756794 bytes compressed:  64.9%
+Zip file size: 1858145 bytes, number of entries: 7
+-rw-rw-rw-  2.0 fat  5309440 b- defN 23-May-13 02:09 ponder.cp39-win_amd64.pyd
+-rw-rw-rw-  2.0 fat    11254 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/LICENSE.txt
+-rw-rw-rw-  2.0 fat      759 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       94 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat       53 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/entry_points.txt
+-rw-rw-rw-  2.0 fat        7 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      563 b- defN 23-May-13 02:09 ponder-0.1.2.dist-info/RECORD
+7 files, 5322170 bytes uncompressed, 1857147 bytes compressed:  65.1%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: ponder.cp39-win_amd64.pyd
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/LICENSE.txt
+Filename: ponder-0.1.2.dist-info/LICENSE.txt
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/METADATA
+Filename: ponder-0.1.2.dist-info/METADATA
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/WHEEL
+Filename: ponder-0.1.2.dist-info/WHEEL
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/entry_points.txt
+Filename: ponder-0.1.2.dist-info/entry_points.txt
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/top_level.txt
+Filename: ponder-0.1.2.dist-info/top_level.txt
 Comment: 
 
-Filename: ponder-0.1.1.dist-info/RECORD
+Filename: ponder-0.1.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## Comparing `ponder-0.1.1.dist-info/LICENSE.txt` & `ponder-0.1.2.dist-info/LICENSE.txt`

 * *Files identical despite different names*

## Comparing `ponder-0.1.1.dist-info/METADATA` & `ponder-0.1.2.dist-info/METADATA`

 * *Files 10% similar despite different names*

```diff
@@ -1,29 +1,27 @@
 Metadata-Version: 2.1
 Name: ponder
-Version: 0.1.1
+Version: 0.1.2
 Summary: Ponder - An extension to Modin that runs pandas and numpy in your database or data warehouse.
 Home-page: https://ponder.io
 Author: Ponder
 Author-email: support@ponder.io
 License: Other/Proprietary License
 Platform: UNKNOWN
 Requires-Python: >=3.8
 License-File: LICENSE.txt
 Requires-Dist: snowflake-connector-python[pandas]
-Requires-Dist: big
 Requires-Dist: boto3
 Requires-Dist: cloudpickle (==2.0.0)
 Requires-Dist: db-dtypes
-Requires-Dist: dill
 Requires-Dist: duckdb
 Requires-Dist: fsspec[http]
 Requires-Dist: google-cloud-bigquery
 Requires-Dist: matplotlib
-Requires-Dist: modin (==0.19.0.post0)
+Requires-Dist: modin (==0.19.0.post1)
 Requires-Dist: numpy
 Requires-Dist: pandas
 Requires-Dist: pytest
 Requires-Dist: pytz
 Requires-Dist: scipy
 
 UNKNOWN
```

## Comparing `ponder-0.1.1.dist-info/RECORD` & `ponder-0.1.2.dist-info/RECORD`

 * *Files 20% similar despite different names*

```diff
@@ -1,7 +1,7 @@
-ponder.cp39-win_amd64.pyd,sha256=7xnkWMvc-n01mMzpjsqFySNY8WiZl04bgwBzpN6F6TM,4985856
-ponder-0.1.1.dist-info/LICENSE.txt,sha256=iqnxmgOMKpVZCxi2Rzl1vLVIc9z_P7u4uBe3-SHcmuM,11254
-ponder-0.1.1.dist-info/METADATA,sha256=DeOj0b6UR1rAnohY469Fqt7jwdUKu-VTAMzKkIcu0Os,800
-ponder-0.1.1.dist-info/WHEEL,sha256=4Js21CeqxstYuRusMkuxpu1_Dz5nsZfYBExpe3gMC24,94
-ponder-0.1.1.dist-info/entry_points.txt,sha256=j9DqjIapFzT7JCsB19AMXWMQHSU5bgE5V4nQx3tfHvc,53
-ponder-0.1.1.dist-info/top_level.txt,sha256=nm4x-AyOBZuo9B3GveAxl73Ufjo9WlivPtnED0YzZeA,7
-ponder-0.1.1.dist-info/RECORD,,
+ponder.cp39-win_amd64.pyd,sha256=N8yrdS-wIxciRbgpqKbGp4Vvd3mbFSesn0OM4FyT-Es,5309440
+ponder-0.1.2.dist-info/LICENSE.txt,sha256=iqnxmgOMKpVZCxi2Rzl1vLVIc9z_P7u4uBe3-SHcmuM,11254
+ponder-0.1.2.dist-info/METADATA,sha256=ktgWsvh9wrikeRKxmdS2CZf6SPTu_WHGIE4T9f3aET4,759
+ponder-0.1.2.dist-info/WHEEL,sha256=sZba66aXRqFq8h5d775hVgqk4tyAT6kysyGd2RlEpTo,94
+ponder-0.1.2.dist-info/entry_points.txt,sha256=j9DqjIapFzT7JCsB19AMXWMQHSU5bgE5V4nQx3tfHvc,53
+ponder-0.1.2.dist-info/top_level.txt,sha256=nm4x-AyOBZuo9B3GveAxl73Ufjo9WlivPtnED0YzZeA,7
+ponder-0.1.2.dist-info/RECORD,,
```

