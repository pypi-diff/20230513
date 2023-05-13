# Comparing `tmp/price2bq_zfullio-1.1.1.tar.gz` & `tmp/price2bq_zfullio-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "price2bq_zfullio-1.1.1.tar", max compression
+gzip compressed data, was "price2bq_zfullio-1.2.0.tar", max compression
```

## Comparing `price2bq_zfullio-1.1.1.tar` & `price2bq_zfullio-1.2.0.tar`

### file list

```diff
@@ -1,7 +1,6 @@
--rwxr-xr-x   0        0        0     1069 2022-08-09 03:27:15.960000 price2bq_zfullio-1.1.1/LICENSE
--rwxr-xr-x   0        0        0      160 2022-11-30 12:21:03.857881 price2bq_zfullio-1.1.1/README.md
--rwxr-xr-x   0        0        0      582 2022-11-30 12:51:48.361408 price2bq_zfullio-1.1.1/pyproject.toml
--rwxr-xr-x   0        0        0      122 2022-11-30 12:21:03.815936 price2bq_zfullio-1.1.1/src/price2bq_zfullio/__init__.py
--rwxr-xr-x   0        0        0     8969 2022-11-30 12:46:53.837203 price2bq_zfullio-1.1.1/src/price2bq_zfullio/main.py
--rw-r--r--   0        0        0     1067 2022-11-30 12:51:50.920710 price2bq_zfullio-1.1.1/setup.py
--rw-r--r--   0        0        0      808 2022-11-30 12:51:50.921259 price2bq_zfullio-1.1.1/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-13 11:01:28.045914 price2bq_zfullio-1.2.0/LICENSE
+-rw-r--r--   0        0        0      160 2023-05-13 11:01:28.045914 price2bq_zfullio-1.2.0/README.md
+-rw-r--r--   0        0        0     1334 2023-05-13 11:15:33.772366 price2bq_zfullio-1.2.0/pyproject.toml
+-rw-r--r--   0        0        0      122 2023-05-13 11:01:28.049247 price2bq_zfullio-1.2.0/src/price2bq_zfullio/__init__.py
+-rw-r--r--   0        0        0     8969 2023-05-13 11:01:28.049247 price2bq_zfullio-1.2.0/src/price2bq_zfullio/main.py
+-rw-r--r--   0        0        0      773 1970-01-01 00:00:00.000000 price2bq_zfullio-1.2.0/PKG-INFO
```

### Comparing `price2bq_zfullio-1.1.1/LICENSE` & `price2bq_zfullio-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `price2bq_zfullio-1.1.1/src/price2bq_zfullio/main.py` & `price2bq_zfullio-1.2.0/src/price2bq_zfullio/main.py`

 * *Files identical despite different names*

### Comparing `price2bq_zfullio-1.1.1/PKG-INFO` & `price2bq_zfullio-1.2.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 Metadata-Version: 2.1
 Name: price2bq-zfullio
-Version: 1.1.1
+Version: 1.2.0
 Summary: Экспорт файлов c площадок 'Яндекс Недвижимость', 'Авито' 'Циан' в BigQuery
 Author: viktor
 Author-email: vi.dave@yandex.ru
 Requires-Python: >=3.10,<3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Requires-Dist: bq-easy-zfullio (>=1,<2)
-Requires-Dist: loguru (>=0.6.0,<0.7.0)
-Requires-Dist: openpyxl (>=3.0.10,<4.0.0)
-Requires-Dist: pandas (>=1.5,<2.0)
-Requires-Dist: python-dotenv (>=0.21,<0.22)
-Requires-Dist: xlrd (>=2.0.1,<3.0.0)
+Requires-Dist: loguru (>=0,<1)
+Requires-Dist: openpyxl (>=3,<4)
+Requires-Dist: pandas (>=2,<3)
+Requires-Dist: python-dotenv (>=1,<2)
+Requires-Dist: xlrd (>=2,<3)
 Description-Content-Type: text/markdown
 
 # Price to BQ
 
 Экспорт файлов с площадок 'Яндекс Недвижимость', 'Циан', 'Avito', 'Новострой М' в BigQuery
```

