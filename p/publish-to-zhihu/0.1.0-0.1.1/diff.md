# Comparing `tmp/publish_to_zhihu-0.1.0.tar.gz` & `tmp/publish_to_zhihu-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "publish_to_zhihu-0.1.0.tar", max compression
+gzip compressed data, was "publish_to_zhihu-0.1.1.tar", max compression
```

## Comparing `publish_to_zhihu-0.1.0.tar` & `publish_to_zhihu-0.1.1.tar`

### file list

```diff
@@ -1,10 +1,9 @@
--rw-r--r--   0        0        0     1090 2022-06-11 15:01:11.658782 publish_to_zhihu-0.1.0/LICENSE
--rw-r--r--   0        0        0       23 2022-06-11 15:01:11.750592 publish_to_zhihu-0.1.0/publish_to_zhihu/__init__.py
--rw-r--r--   0        0        0      338 2022-06-11 15:01:11.742961 publish_to_zhihu-0.1.0/publish_to_zhihu/console.py
--rw-r--r--   0        0        0     1177 2022-06-11 23:26:20.579194 publish_to_zhihu-0.1.0/publish_to_zhihu/convert_latex.py
--rw-r--r--   0        0        0     2483 2022-06-11 23:36:40.517244 publish_to_zhihu-0.1.0/publish_to_zhihu/prepare_md.py
--rw-r--r--   0        0        0     2725 2022-06-11 23:36:01.631362 publish_to_zhihu-0.1.0/publish_to_zhihu/upload_images.py
--rw-r--r--   0        0        0      932 2022-06-11 23:32:59.590670 publish_to_zhihu-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1224 2022-06-11 23:39:49.819748 publish_to_zhihu-0.1.0/README.md
--rw-r--r--   0        0        0     2271 2022-06-11 23:40:33.866356 publish_to_zhihu-0.1.0/setup.py
--rw-r--r--   0        0        0     1877 2022-06-11 23:40:33.866356 publish_to_zhihu-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1090 2023-05-11 23:45:42.640554 publish_to_zhihu-0.1.1/LICENSE
+-rw-r--r--   0        0        0       23 2023-05-11 23:45:42.645559 publish_to_zhihu-0.1.1/publish_to_zhihu/__init__.py
+-rw-r--r--   0        0        0      338 2023-05-11 23:45:42.646554 publish_to_zhihu-0.1.1/publish_to_zhihu/console.py
+-rw-r--r--   0        0        0     1177 2023-05-11 23:45:42.646554 publish_to_zhihu-0.1.1/publish_to_zhihu/convert_latex.py
+-rw-r--r--   0        0        0     3623 2023-05-13 18:13:22.429142 publish_to_zhihu-0.1.1/publish_to_zhihu/prepare_md.py
+-rw-r--r--   0        0        0     2725 2023-05-11 23:45:42.647555 publish_to_zhihu-0.1.1/publish_to_zhihu/upload_images.py
+-rw-r--r--   0        0        0      932 2023-05-13 18:18:27.674336 publish_to_zhihu-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     1224 2023-05-11 23:45:42.641554 publish_to_zhihu-0.1.1/README.md
+-rw-r--r--   0        0        0     1928 1970-01-01 00:00:00.000000 publish_to_zhihu-0.1.1/PKG-INFO
```

### Comparing `publish_to_zhihu-0.1.0/LICENSE` & `publish_to_zhihu-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `publish_to_zhihu-0.1.0/publish_to_zhihu/convert_latex.py` & `publish_to_zhihu-0.1.1/publish_to_zhihu/convert_latex.py`

 * *Files identical despite different names*

### Comparing `publish_to_zhihu-0.1.0/publish_to_zhihu/upload_images.py` & `publish_to_zhihu-0.1.1/publish_to_zhihu/upload_images.py`

 * *Files identical despite different names*

### Comparing `publish_to_zhihu-0.1.0/pyproject.toml` & `publish_to_zhihu-0.1.1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "publish_to_zhihu"
-version = "0.1.0"
+version = "0.1.1"
 description = "Publish markdown to Zhihu"
 authors = ["Anselm Wang <anselmwang@gmail.com>"]
 homepage = "https://github.com/anselmwang/publish_to_zhihu"
 repository = "https://github.com/anselmwang/publish_to_zhihu"
 readme= "README.md"
 
 [tool.poetry.dependencies]
@@ -15,15 +15,15 @@
 [tool.poetry.dev-dependencies]
 pytest = "^5.2"
 keyring = "^23.5.0"
 artifacts-keyring = "^0.3.1"
 twine = "^3.8.0"
 pre-commit = "^2.17.0"
 black = "^22.1.0"
-isort = "^5.10.1"
+isort = "^5.12.0"
 ipykernel = "^6.9.1"
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.isort]
```

### Comparing `publish_to_zhihu-0.1.0/README.md` & `publish_to_zhihu-0.1.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Usage
 
 ```bash
-pipx install publish_to_zhihu
+pipx install publish-to-zhihu
 
 # convert latex math formula to zhihu format
 zhihu_convert_latex to_be_convert.md
 
 # upload a list of images to azure storage container
 zhihu_upload_images azure_storage_container_name azure_storage_account_connection_string file_root file_rel_path_0 file_rel_path_1
```

### Comparing `publish_to_zhihu-0.1.0/PKG-INFO` & `publish_to_zhihu-0.1.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,29 +1,30 @@
 Metadata-Version: 2.1
 Name: publish-to-zhihu
-Version: 0.1.0
+Version: 0.1.1
 Summary: Publish markdown to Zhihu
 Home-page: https://github.com/anselmwang/publish_to_zhihu
 Author: Anselm Wang
 Author-email: anselmwang@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: azure-storage-blob (>=12.12.0,<13.0.0)
 Requires-Dist: click (>=8.0.4,<9.0.0)
 Project-URL: Repository, https://github.com/anselmwang/publish_to_zhihu
 Description-Content-Type: text/markdown
 
 # Usage
 
 ```bash
-pipx install publish_to_zhihu
+pipx install publish-to-zhihu
 
 # convert latex math formula to zhihu format
 zhihu_convert_latex to_be_convert.md
 
 # upload a list of images to azure storage container
 zhihu_upload_images azure_storage_container_name azure_storage_account_connection_string file_root file_rel_path_0 file_rel_path_1
```

