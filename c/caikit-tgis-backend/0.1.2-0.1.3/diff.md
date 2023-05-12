# Comparing `tmp/caikit-tgis-backend-0.1.2.tar.gz` & `tmp/caikit-tgis-backend-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "caikit-tgis-backend-0.1.2.tar", last modified: Mon May  8 20:24:48 2023, max compression
+gzip compressed data, was "caikit-tgis-backend-0.1.3.tar", last modified: Fri May 12 22:59:11 2023, max compression
```

## Comparing `caikit-tgis-backend-0.1.2.tar` & `caikit-tgis-backend-0.1.3.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0       65 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.coveragerc
--rw-r--r--   0        0        0      676 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0        0        0      579 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0        0        0      519 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/user_story.md
--rw-r--r--   0        0        0      105 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/dependabot.yml
--rw-r--r--   0        0        0     1280 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/workflows/build-library.yml
--rw-r--r--   0        0        0     1141 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/workflows/lint-code.yml
--rw-r--r--   0        0        0     1144 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.github/workflows/publish-library.yml
--rw-r--r--   0        0        0      183 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.gitignore
--rw-r--r--   0        0        0      318 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.isort.cfg
--rw-r--r--   0        0        0      440 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.pre-commit-config.yaml
--rw-r--r--   0        0        0       24 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.prettierignore
--rw-r--r--   0        0        0       12 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.prettierrc.yaml
--rw-r--r--   0        0        0    21406 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.pylintrc
--rw-r--r--   0        0        0       78 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/.whitesource
--rw-r--r--   0        0        0      314 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/CODEOWNERS
--rw-r--r--   0        0        0     7269 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/CONTRIBUTING.md
--rw-r--r--   0        0        0    11357 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/LICENSE
--rw-r--r--   0        0        0      138 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/README.md
--rw-r--r--   0        0        0      152 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/SECURITY.md
--rw-r--r--   0        0        0      723 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/__init__.py
--rw-r--r--   0        0        0     5727 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/generation.proto
--rw-r--r--   0        0        0      840 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/__init__.py
--rw-r--r--   0        0        0    13426 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/generation_pb2.py
--rw-r--r--   0        0        0     5685 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/generation_pb2_grpc.py
--rw-r--r--   0        0        0    12510 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/caikit_tgis_backend/tgis_backend.py
--rw-r--r--   0        0        0      169 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/code-of-conduct.md
--rw-r--r--   0        0        0      655 2023-05-08 20:24:44.215511 caikit-tgis-backend-0.1.2/pyproject.toml
--rwxr-xr-x   0        0        0      720 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/scripts/fmt.sh
--rwxr-xr-x   0        0        0      393 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/scripts/gen_tgis_protos.sh
--rw-r--r--   0        0        0       33 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/setup_requirements.txt
--rw-r--r--   0        0        0        0 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/tests/__init__.py
--rw-r--r--   0        0        0      342 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/tests/conftest.py
--rw-r--r--   0        0        0     9063 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/tests/test_tgis_backend.py
--rw-r--r--   0        0        0     7629 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/tests/tgis_mock.py
--rw-r--r--   0        0        0     1209 2023-05-08 20:24:41.083503 caikit-tgis-backend-0.1.2/tox.ini
--rw-r--r--   0        0        0      556 1970-01-01 00:00:00.000000 caikit-tgis-backend-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0       65 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.coveragerc
+-rw-r--r--   0        0        0      676 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      579 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0        0        0      519 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/user_story.md
+-rw-r--r--   0        0        0      105 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/dependabot.yml
+-rw-r--r--   0        0        0     1280 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/workflows/build-library.yml
+-rw-r--r--   0        0        0     1141 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/workflows/lint-code.yml
+-rw-r--r--   0        0        0     1144 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.github/workflows/publish-library.yml
+-rw-r--r--   0        0        0      183 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.gitignore
+-rw-r--r--   0        0        0      318 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.isort.cfg
+-rw-r--r--   0        0        0      440 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.pre-commit-config.yaml
+-rw-r--r--   0        0        0       24 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.prettierignore
+-rw-r--r--   0        0        0       12 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.prettierrc.yaml
+-rw-r--r--   0        0        0    21406 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.pylintrc
+-rw-r--r--   0        0        0       78 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/.whitesource
+-rw-r--r--   0        0        0      314 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/CODEOWNERS
+-rw-r--r--   0        0        0     7269 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/CONTRIBUTING.md
+-rw-r--r--   0        0        0    11357 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/LICENSE
+-rw-r--r--   0        0        0      138 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/README.md
+-rw-r--r--   0        0        0      152 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/SECURITY.md
+-rw-r--r--   0        0        0      723 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/__init__.py
+-rw-r--r--   0        0        0     5727 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/generation.proto
+-rw-r--r--   0        0        0      840 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/__init__.py
+-rw-r--r--   0        0        0    13426 2023-05-12 22:59:01.629061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/generation_pb2.py
+-rw-r--r--   0        0        0     5685 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/generation_pb2_grpc.py
+-rw-r--r--   0        0        0    12510 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/caikit_tgis_backend/tgis_backend.py
+-rw-r--r--   0        0        0      169 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/code-of-conduct.md
+-rw-r--r--   0        0        0      655 2023-05-12 22:59:06.245080 caikit-tgis-backend-0.1.3/pyproject.toml
+-rwxr-xr-x   0        0        0      720 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/scripts/fmt.sh
+-rwxr-xr-x   0        0        0      393 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/scripts/gen_tgis_protos.sh
+-rw-r--r--   0        0        0       33 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/setup_requirements.txt
+-rw-r--r--   0        0        0        0 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/tests/__init__.py
+-rw-r--r--   0        0        0      342 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/tests/conftest.py
+-rw-r--r--   0        0        0     9063 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/tests/test_tgis_backend.py
+-rw-r--r--   0        0        0     7629 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/tests/tgis_mock.py
+-rw-r--r--   0        0        0     1209 2023-05-12 22:59:01.633061 caikit-tgis-backend-0.1.3/tox.ini
+-rw-r--r--   0        0        0      556 1970-01-01 00:00:00.000000 caikit-tgis-backend-0.1.3/PKG-INFO
```

### Comparing `caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/bug_report.md` & `caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/feature_request.md` & `caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.github/ISSUE_TEMPLATE/user_story.md` & `caikit-tgis-backend-0.1.3/.github/ISSUE_TEMPLATE/user_story.md`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.github/workflows/build-library.yml` & `caikit-tgis-backend-0.1.3/.github/workflows/build-library.yml`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.github/workflows/lint-code.yml` & `caikit-tgis-backend-0.1.3/.github/workflows/lint-code.yml`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.github/workflows/publish-library.yml` & `caikit-tgis-backend-0.1.3/.github/workflows/publish-library.yml`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/.pylintrc` & `caikit-tgis-backend-0.1.3/.pylintrc`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/CONTRIBUTING.md` & `caikit-tgis-backend-0.1.3/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/LICENSE` & `caikit-tgis-backend-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/__init__.py` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/__init__.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/generation.proto` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/generation.proto`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/__init__.py` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/__init__.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/generation_pb2.py` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/generation_pb2.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/protobufs/generation_pb2_grpc.py` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/protobufs/generation_pb2_grpc.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/caikit_tgis_backend/tgis_backend.py` & `caikit-tgis-backend-0.1.3/caikit_tgis_backend/tgis_backend.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/pyproject.toml` & `caikit-tgis-backend-0.1.3/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 [build-system]
 requires = ["flit_core >=3.2,<4"]
 build-backend = "flit_core.buildapi"
 
 [project]
 name = "caikit-tgis-backend"
 # Not the actual current version: overwritten by CI
-version = "0.1.2"
+version = "0.1.3"
 description = "Caikit module backend for models run in TGIS"
 license = {text = "Apache-2.0"}
 readme = "README.md"
 requires-python = "~=3.8"
 classifiers=[
     "License :: OSI Approved :: Apache Software License"
 ]
 dependencies = [
-    "caikit>=0.2.0,<0.4.0", # Core abstractions
+    "caikit>=0.2.0,<0.5.0", # Core abstractions
     "grpcio>=1.35.0,<2.0", # Client calls to TGIS
     "requests>=2.28.2,<3", # Health check calls to TGIS
 ]
 
 [project.urls]
 Source = "https://github.com/caikit/caikit-tgis-backend"
```

### Comparing `caikit-tgis-backend-0.1.2/scripts/fmt.sh` & `caikit-tgis-backend-0.1.3/scripts/fmt.sh`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/tests/test_tgis_backend.py` & `caikit-tgis-backend-0.1.3/tests/test_tgis_backend.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/tests/tgis_mock.py` & `caikit-tgis-backend-0.1.3/tests/tgis_mock.py`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/tox.ini` & `caikit-tgis-backend-0.1.3/tox.ini`

 * *Files identical despite different names*

### Comparing `caikit-tgis-backend-0.1.2/PKG-INFO` & `caikit-tgis-backend-0.1.3/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 Metadata-Version: 2.1
 Name: caikit-tgis-backend
-Version: 0.1.2
+Version: 0.1.3
 Summary: Caikit module backend for models run in TGIS
 Requires-Python: ~=3.8
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: Apache Software License
-Requires-Dist: caikit>=0.2.0,<0.4.0
+Requires-Dist: caikit>=0.2.0,<0.5.0
 Requires-Dist: grpcio>=1.35.0,<2.0
 Requires-Dist: requests>=2.28.2,<3
 Project-URL: Source, https://github.com/caikit/caikit-tgis-backend
 
 ## Caikit Text Generation Inference Service (TGIS) Backend
 
 This project provides a Caikit module backend that manages models run in TGIS
```

