# Comparing `tmp/domino-py-0.2.4.tar.gz` & `tmp/domino-py-0.2.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "domino-py-0.2.4.tar", last modified: Fri May 12 11:33:33 2023, max compression
+gzip compressed data, was "domino-py-0.2.5.tar", last modified: Sat May 13 14:33:06 2023, max compression
```

## Comparing `domino-py-0.2.4.tar` & `domino-py-0.2.5.tar`

### file list

```diff
@@ -1,71 +1,71 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.176880 domino-py-0.2.4/
--rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-05-12 11:33:20.000000 domino-py-0.2.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    10074 2023-05-12 11:33:33.176880 domino-py-0.2.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8278 2023-05-12 11:33:20.000000 domino-py-0.2.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.168880 domino-py-0.2.4/domino/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14950 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/base_piece.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.168880 domino-py-0.2.4/domino/cli/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10761 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.168880 domino-py-0.2.4/domino/cli/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/utils/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)    17348 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/utils/pieces_repository.py
--rw-r--r--   0 runner    (1001) docker     (123)    24061 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/cli/utils/platform.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.168880 domino-py-0.2.4/domino/client/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2581 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/airflow_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     1862 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/domino_backend_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     2176 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/fs_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/github_rest_client.py
--rw-r--r--   0 runner    (1001) docker     (123)      844 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/local_files_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     2739 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/client/s3_client.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/custom_operators/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7052 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/docker_operator.py
--rw-r--r--   0 runner    (1001) docker     (123)     5833 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/external_python_operator.py
--rw-r--r--   0 runner    (1001) docker     (123)    17007 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/k8s_operator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/python_operator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/custom_operators/sidecar/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/sidecar/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      911 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/sidecar/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)    11284 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/custom_operators/sidecar/mount.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/exceptions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/exceptions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1423 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/exceptions/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)      896 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/logger.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/schemas/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      427 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/container_resources.py
--rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/deploy_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)      246 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/from_upstream.py
--rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/piece_metadata.py
--rw-r--r--   0 runner    (1001) docker     (123)     1553 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/schemas/shared_storage.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/build_docker_images_pieces.py
--rw-r--r--   0 runner    (1001) docker     (123)     6767 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/create_docker_compose_file.py
--rw-r--r--   0 runner    (1001) docker     (123)    11790 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/docker_compose_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2560 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/docker_compose_scripts.py
--rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/load_piece.py
--rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/piece_dry_run.py
--rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/run_piece_bash.py
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/run_piece_docker.py
--rw-r--r--   0 runner    (1001) docker     (123)     1817 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/scripts/run_piece_k8s.py
--rw-r--r--   0 runner    (1001) docker     (123)    11046 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/task.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.172880 domino-py-0.2.4/domino/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      231 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      455 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/utils/metadata_default.py
--rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/utils/piece_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)      272 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/utils/workflow_shared_storage.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-12 11:33:21.000000 domino-py-0.2.4/domino/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:33:33.176880 domino-py-0.2.4/domino_py.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    10074 2023-05-12 11:33:32.000000 domino-py-0.2.4/domino_py.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-05-12 11:33:33.000000 domino-py-0.2.4/domino_py.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 11:33:32.000000 domino-py-0.2.4/domino_py.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-12 11:33:32.000000 domino-py-0.2.4/domino_py.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      437 2023-05-12 11:33:32.000000 domino-py-0.2.4/domino_py.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-12 11:33:32.000000 domino-py-0.2.4/domino_py.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 11:33:33.176880 domino-py-0.2.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1765 2023-05-12 11:33:21.000000 domino-py-0.2.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.514493 domino-py-0.2.5/
+-rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-05-13 14:32:51.000000 domino-py-0.2.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    10074 2023-05-13 14:33:06.514493 domino-py-0.2.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8278 2023-05-13 14:32:51.000000 domino-py-0.2.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.506493 domino-py-0.2.5/domino/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14950 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/base_piece.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.506493 domino-py-0.2.5/domino/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10929 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.506493 domino-py-0.2.5/domino/cli/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/utils/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17622 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/utils/pieces_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24061 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/cli/utils/platform.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/client/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2581 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/airflow_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1862 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/domino_backend_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2176 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/fs_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/github_rest_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      844 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/local_files_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2739 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/client/s3_client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/custom_operators/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7052 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/docker_operator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5833 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/external_python_operator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17007 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/k8s_operator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/python_operator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/custom_operators/sidecar/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/sidecar/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      911 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/sidecar/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11284 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/custom_operators/sidecar/mount.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/exceptions/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/exceptions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1423 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/exceptions/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      896 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/logger.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/schemas/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      427 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/container_resources.py
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/deploy_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)      246 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/from_upstream.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/piece_metadata.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1553 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/schemas/shared_storage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/build_docker_images_pieces.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6767 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/create_docker_compose_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11790 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/docker_compose_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2560 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/docker_compose_scripts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/load_piece.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/piece_dry_run.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/run_piece_bash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/run_piece_docker.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1817 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/scripts/run_piece_k8s.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11046 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/task.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      231 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      455 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/utils/metadata_default.py
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/utils/piece_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      272 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/utils/workflow_shared_storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 14:32:51.000000 domino-py-0.2.5/domino/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:06.510493 domino-py-0.2.5/domino_py.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    10074 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      437 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 14:33:06.000000 domino-py-0.2.5/domino_py.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:33:06.514493 domino-py-0.2.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1765 2023-05-13 14:32:51.000000 domino-py-0.2.5/setup.py
```

### Comparing `domino-py-0.2.4/LICENSE` & `domino-py-0.2.5/LICENSE`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/PKG-INFO` & `domino-py-0.2.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: domino-py
-Version: 0.2.4
+Version: 0.2.5
 Summary: Python package for the Domino platform
 Home-page: UNKNOWN
 Author: Luiz Tauffer and Vinicius Vaz
 Author-email: luiz@taufferconsulting.com
 License: UNKNOWN
 Description:
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: domino-py Version: 0.2.4 Summary: Python package
+Metadata-Version: 2.1 Name: domino-py Version: 0.2.5 Summary: Python package
 for the Domino platform Home-page: UNKNOWN Author: Luiz Tauffer and Vinicius
 Vaz Author-email: luiz@taufferconsulting.com License: UNKNOWN Description:
    [https://raw.githubusercontent.com/Tauffer-Consulting/domino/main/media/
                                    logo.png]
                     [https://img.shields.io/pypi/v/domino-
   py?color=%231BA331&label=PyPI&logo=python&logoColor=%23F7F991%20] [https://
  img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/domino]
```

### Comparing `domino-py-0.2.4/README.md` & `domino-py-0.2.5/README.md`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/base_piece.py` & `domino-py-0.2.5/domino/base_piece.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/cli/cli.py` & `domino-py-0.2.5/domino/cli/cli.py`

 * *Files 2% similar despite different names*

```diff
@@ -240,20 +240,26 @@
 )
 @click.option(
     '--registry-token',
     prompt='Github Container Registry token',
     default=get_registry_token_from_env,
     help='Your Github Container Registry token with access to where the image will be published.'
 )
-def cli_organize_pieces_repository(build_images, publish_images, registry_token):
+@click.option(
+    '--source-url',
+    prompt='Url of source repository',
+    default="",
+    help='The base url for this Pieces repository.'
+)
+def cli_organize_pieces_repository(build_images, publish_images, registry_token, source_url):
     """Prepare local folder for running a Domino platform."""
     if registry_token:
         os.environ['GHCR_PASSWORD'] = registry_token
     console.print(f"Using registry token to publish images")
-    pieces_repository.organize_pieces_repository(build_images, publish_images)
+    pieces_repository.organize_pieces_repository(build_images, publish_images, source_url)
 
 
 @click.command()
 def cli_create_release():
     """
     Get release version for the Pieces repository in github stdout format.
     Used by github actions to set the release version.
```

### Comparing `domino-py-0.2.4/domino/cli/utils/pieces_repository.py` & `domino-py-0.2.5/domino/cli/utils/pieces_repository.py`

 * *Files 2% similar despite different names*

```diff
@@ -239,15 +239,15 @@
     with open(f"{repository_name}/config.toml", "wb") as f:
         tomli_w.dump(repo_config, f)
 
     console.print(f"Pieces repository successfully create at: {repository_folder}", style=f"bold {COLOR_PALETTE.get('success')}")
     console.print("")
 
 
-def create_compiled_pieces_metadata() -> None:  
+def create_compiled_pieces_metadata(source_url: str=None) -> None:  
     """
     Create compiled metadata from Pieces metadata.json files and include input_schema generated from models.py
     """
     from domino.scripts.load_piece import load_piece_models_from_path, load_piece_class_from_path
     from domino.utils.metadata_default import metadata_default
 
     pieces_path = Path(".") / "pieces"
@@ -271,14 +271,19 @@
                 pieces_folder_path=str(pieces_path), 
                 piece_name=op_dir.name
             )
             metadata["input_schema"] = input_model_class.schema()
             metadata["output_schema"] = output_model_class.schema()
             metadata["secrets_schema"] = secrets_model_class.schema() if secrets_model_class else None
 
+            # Add source code url
+            metadata["source_url"] = None
+            if source_url and len(source_url) > 0:
+                metadata["source_url"] = source_url + f"/tree/main/pieces/{piece_name}"
+
             # Add to compiled metadata
             compiled_metadata[piece_name] = metadata
     
     # Save compiled_metadata.json file
     organized_domino_path = Path(".") / ".domino/"
     with open(str(organized_domino_path / "compiled_metadata.json"), "w") as f:
         json.dump(compiled_metadata, f, indent=4)
@@ -357,15 +362,15 @@
     """
     if any([a.isspace() for a in repo_name]):
         raise ValueError("Repository name should not contain blank spaces")
     if any([a in repo_name for a in ["!", "@", "#", "$", "%", "^", "&", "*", "(", ")", "+", "=", "{", "}", "[", "]", ":", ";", "'", '"', "<", ">", "?", "/", "\\", "|", "~", "`"]]):
         raise ValueError("Repository name should not contain special characters")
 
 
-def organize_pieces_repository(build_images: bool, publish_images: bool) -> None:
+def organize_pieces_repository(build_images: bool, publish_images: bool, source_url: str) -> None:
     """
     Organize Piece's repository for Domino. This will: 
     - validate the folder structure, and create the pieces compiled_metadata.json and dependencies_map.json files
     - build Docker images for the Pieces
     - publish images at github container registry
     """        
     # Validate repository
@@ -377,15 +382,15 @@
     # Load config
     with open("config.toml", "rb") as f:
         repo_config = tomli.load(f)
     repo_name = repo_config["repository"]["REPOSITORY_NAME"]
     validate_repo_name(repo_name)
     
     # Create compiled metadata from Pieces metadata.json files and add data input schema
-    create_compiled_pieces_metadata()
+    create_compiled_pieces_metadata(source_url=source_url)
     
     # Generate dependencies_map.json file
     create_dependencies_map(save_map_as_file=True)
     console.print("Metadata and dependencies organized successfully!", style=f"bold {COLOR_PALETTE.get('success')}")
 
     # Build and publish the images
     if build_images:
```

### Comparing `domino-py-0.2.4/domino/cli/utils/platform.py` & `domino-py-0.2.5/domino/cli/utils/platform.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/airflow_client.py` & `domino-py-0.2.5/domino/client/airflow_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/domino_backend_client.py` & `domino-py-0.2.5/domino/client/domino_backend_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/fs_client.py` & `domino-py-0.2.5/domino/client/fs_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/github_rest_client.py` & `domino-py-0.2.5/domino/client/github_rest_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/local_files_client.py` & `domino-py-0.2.5/domino/client/local_files_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/client/s3_client.py` & `domino-py-0.2.5/domino/client/s3_client.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/docker_operator.py` & `domino-py-0.2.5/domino/custom_operators/docker_operator.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/external_python_operator.py` & `domino-py-0.2.5/domino/custom_operators/external_python_operator.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/k8s_operator.py` & `domino-py-0.2.5/domino/custom_operators/k8s_operator.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/python_operator.py` & `domino-py-0.2.5/domino/custom_operators/python_operator.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/sidecar/logger.py` & `domino-py-0.2.5/domino/custom_operators/sidecar/logger.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/custom_operators/sidecar/mount.py` & `domino-py-0.2.5/domino/custom_operators/sidecar/mount.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/exceptions/exceptions.py` & `domino-py-0.2.5/domino/exceptions/exceptions.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/logger.py` & `domino-py-0.2.5/domino/logger.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/schemas/piece_metadata.py` & `domino-py-0.2.5/domino/schemas/piece_metadata.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/schemas/shared_storage.py` & `domino-py-0.2.5/domino/schemas/shared_storage.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/build_docker_images_pieces.py` & `domino-py-0.2.5/domino/scripts/build_docker_images_pieces.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/create_docker_compose_file.py` & `domino-py-0.2.5/domino/scripts/create_docker_compose_file.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/docker_compose_constants.py` & `domino-py-0.2.5/domino/scripts/docker_compose_constants.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/docker_compose_scripts.py` & `domino-py-0.2.5/domino/scripts/docker_compose_scripts.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/load_piece.py` & `domino-py-0.2.5/domino/scripts/load_piece.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/piece_dry_run.py` & `domino-py-0.2.5/domino/scripts/piece_dry_run.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/run_piece_bash.py` & `domino-py-0.2.5/domino/scripts/run_piece_bash.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/run_piece_docker.py` & `domino-py-0.2.5/domino/scripts/run_piece_docker.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/scripts/run_piece_k8s.py` & `domino-py-0.2.5/domino/scripts/run_piece_k8s.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/task.py` & `domino-py-0.2.5/domino/task.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino/utils/piece_generator.py` & `domino-py-0.2.5/domino/utils/piece_generator.py`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/domino_py.egg-info/PKG-INFO` & `domino-py-0.2.5/domino_py.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: domino-py
-Version: 0.2.4
+Version: 0.2.5
 Summary: Python package for the Domino platform
 Home-page: UNKNOWN
 Author: Luiz Tauffer and Vinicius Vaz
 Author-email: luiz@taufferconsulting.com
 License: UNKNOWN
 Description:
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: domino-py Version: 0.2.4 Summary: Python package
+Metadata-Version: 2.1 Name: domino-py Version: 0.2.5 Summary: Python package
 for the Domino platform Home-page: UNKNOWN Author: Luiz Tauffer and Vinicius
 Vaz Author-email: luiz@taufferconsulting.com License: UNKNOWN Description:
    [https://raw.githubusercontent.com/Tauffer-Consulting/domino/main/media/
                                    logo.png]
                     [https://img.shields.io/pypi/v/domino-
   py?color=%231BA331&label=PyPI&logo=python&logoColor=%23F7F991%20] [https://
  img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/domino]
```

### Comparing `domino-py-0.2.4/domino_py.egg-info/SOURCES.txt` & `domino-py-0.2.5/domino_py.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `domino-py-0.2.4/setup.py` & `domino-py-0.2.5/setup.py`

 * *Files identical despite different names*

