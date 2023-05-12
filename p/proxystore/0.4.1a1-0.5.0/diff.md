# Comparing `tmp/proxystore-0.4.1a1.tar.gz` & `tmp/proxystore-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "proxystore-0.4.1a1.tar", last modified: Tue Jan 31 02:02:47 2023, max compression
+gzip compressed data, was "proxystore-0.5.0.tar", last modified: Fri May 12 22:52:30 2023, max compression
```

## Comparing `proxystore-0.4.1a1.tar` & `proxystore-0.5.0.tar`

### file list

```diff
@@ -1,182 +1,232 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/01_bug.yml
--rw-r--r--   0 runner    (1001) docker     (123)      718 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/02_feature.yml
--rw-r--r--   0 runner    (1001) docker     (123)      391 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/03_docs.yml
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/config.yml
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/dependabot.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/pull_request_template.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      911 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/workflows/integration.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/workflows/publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1846 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.github/workflows/tests.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1078 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      400 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/.readthedocs.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1057 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1050 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      634 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.672463 proxystore-0.4.1a1/docs/_templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/docs/_templates/autosummary/
--rw-r--r--   0 runner    (1001) docker     (123)      374 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/_templates/autosummary/module.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5356 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/advanced.rst
--rw-r--r--   0 runner    (1001) docker     (123)      349 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (123)    12854 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/changelog.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4218 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)     7795 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/contributing.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7076 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/getstarted.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/docs/guides/
--rw-r--r--   0 runner    (1001) docker     (123)     8113 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/guides/endpoints.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4468 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/guides/performance.rst
--rw-r--r--   0 runner    (1001) docker     (123)       95 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/guides.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1256 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/proxy.txt
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/docs/static/
--rw-r--r--   0 runner    (1001) docker     (123)    65884 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/static/dataflow.png
--rw-r--r--   0 runner    (1001) docker     (123)    77893 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/static/endpoints.png
--rw-r--r--   0 runner    (1001) docker     (123)    50662 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/docs/static/overview.png
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/examples/
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      527 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/examples/funcx/
--rw-r--r--   0 runner    (1001) docker     (123)      753 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/funcx/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     3898 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/funcx/mapreduce_funcx.py
--rw-r--r--   0 runner    (1001) docker     (123)      674 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/funcx/run.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.676463 proxystore-0.4.1a1/examples/parsl/
--rw-r--r--   0 runner    (1001) docker     (123)      266 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/parsl/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/parsl/mapreduce_parsl.py
--rw-r--r--   0 runner    (1001) docker     (123)      561 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/parsl/run.sh
--rw-r--r--   0 runner    (1001) docker     (123)       84 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2548 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/examples/store_stats.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.680463 proxystore-0.4.1a1/proxystore/
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.680463 proxystore-0.4.1a1/proxystore/endpoint/
--rw-r--r--   0 runner    (1001) docker     (123)      381 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6282 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)    12824 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)     5568 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)    17950 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/endpoint.py
--rw-r--r--   0 runner    (1001) docker     (123)      555 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/messages.py
--rw-r--r--   0 runner    (1001) docker     (123)     8554 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/serve.py
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/endpoint/storage.py
--rw-r--r--   0 runner    (1001) docker     (123)     2660 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/factory.py
--rw-r--r--   0 runner    (1001) docker     (123)     6866 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/globus.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.680463 proxystore-0.4.1a1/proxystore/p2p/
--rw-r--r--   0 runner    (1001) docker     (123)      688 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/chunks.py
--rw-r--r--   0 runner    (1001) docker     (123)     4469 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/client.py
--rw-r--r--   0 runner    (1001) docker     (123)    13768 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/connection.py
--rw-r--r--   0 runner    (1001) docker     (123)      966 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/counter.py
--rw-r--r--   0 runner    (1001) docker     (123)      406 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)    14116 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/messages.py
--rw-r--r--   0 runner    (1001) docker     (123)    12870 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/server.py
--rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/p2p/task.py
--rw-r--r--   0 runner    (1001) docker     (123)     6368 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/proxy.py
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/serialize.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/proxystore/store/
--rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    23789 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1787 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/cache.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/proxystore/store/dim/
--rw-r--r--   0 runner    (1001) docker     (123)      496 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/dim/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13285 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/dim/margo.py
--rw-r--r--   0 runner    (1001) docker     (123)    13484 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/dim/ucx.py
--rw-r--r--   0 runner    (1001) docker     (123)      988 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/dim/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11136 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/dim/websockets.py
--rw-r--r--   0 runner    (1001) docker     (123)     8151 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/endpoint.py
--rw-r--r--   0 runner    (1001) docker     (123)     1429 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2939 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/file.py
--rw-r--r--   0 runner    (1001) docker     (123)    22275 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/globus.py
--rw-r--r--   0 runner    (1001) docker     (123)     2340 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/local.py
--rw-r--r--   0 runner    (1001) docker     (123)     2141 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/redis.py
--rw-r--r--   0 runner    (1001) docker     (123)     7026 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     1862 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/store/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/proxystore/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.680463 proxystore-0.4.1a1/proxystore.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4006 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      476 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-01-31 02:02:47.000000 proxystore-0.4.1a1/proxystore.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     3356 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/testing/
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      585 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/compat.py
--rw-r--r--   0 runner    (1001) docker     (123)     2331 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/endpoint.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/testing/mocked/
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocked/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1949 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocked/globus.py
--rw-r--r--   0 runner    (1001) docker     (123)     5084 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocked/pymargo.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocked/redis.py
--rw-r--r--   0 runner    (1001) docker     (123)     3396 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocked/ucx.py
--rw-r--r--   0 runner    (1001) docker     (123)     1121 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/mocking.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/testing/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)      324 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/scripts/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     3904 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/scripts/peer_connection_bandwidth.py
--rw-r--r--   0 runner    (1001) docker     (123)     3973 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/scripts/peer_endpoint_bandwidth.py
--rw-r--r--   0 runner    (1001) docker     (123)     3405 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/scripts/peer_manager_bandwidth.py
--rw-r--r--   0 runner    (1001) docker     (123)     1522 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/signaling_server.py
--rw-r--r--   0 runner    (1001) docker     (123)     9501 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/stores.py
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/testing/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.684463 proxystore-0.4.1a1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       59 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2759 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/tests/endpoint/
--rw-r--r--   0 runner    (1001) docker     (123)       77 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3660 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/cli_test.py
--rw-r--r--   0 runner    (1001) docker     (123)    14211 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/commands_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4260 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/config_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     5647 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/endpoint_peering_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     2263 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/endpoint_solo_test.py
--rw-r--r--   0 runner    (1001) docker     (123)    11787 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/serve_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4200 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/endpoint/storage_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/factory_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4827 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/globus_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/integration/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6175 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/integration/endpoints_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/tests/p2p/
--rw-r--r--   0 runner    (1001) docker     (123)       72 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1612 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/chunks_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3095 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/client_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4496 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/connection_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/counter_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     8620 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/manager_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4401 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/messages_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3480 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/server_cli_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     7851 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/server_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      813 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/p2p/task_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/proxy_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      945 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/serialization_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/tests/store/
--rw-r--r--   0 runner    (1001) docker     (123)       75 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      861 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/cache_test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-31 02:02:47.688463 proxystore-0.4.1a1/tests/store/dim/
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/dim/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2556 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/dim/margo_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3862 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/dim/ucx_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      777 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/dim/websockets_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     2801 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/endpoint_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1031 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/file_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     8645 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/globus_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1876 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/init_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      500 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/local_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      331 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/redis_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     6513 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/stats_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3852 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/store_basics_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     5504 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/store_proxy_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     4556 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/store_stats_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     1137 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/store/utils_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3922 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tests/utils_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      746 2023-01-31 02:02:38.000000 proxystore-0.4.1a1/tox.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.652859 proxystore-0.5.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.608859 proxystore-0.5.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.608859 proxystore-0.5.0/.github/ISSUE_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/ISSUE_TEMPLATE/01_bug.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      718 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/ISSUE_TEMPLATE/02_feature.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      391 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/ISSUE_TEMPLATE/03_docs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/ISSUE_TEMPLATE/config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/dependabot.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1474 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/pull_request_template.md
+-rw-r--r--   0 runner    (1001) docker     (123)      694 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/release.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.608859 proxystore-0.5.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      886 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/cache.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/check-docs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/docs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      911 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/integration.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2551 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1846 2023-05-12 22:52:19.000000 proxystore-0.5.0/.github/workflows/tests.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1830 2023-05-12 22:52:19.000000 proxystore-0.5.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1010 2023-05-12 22:52:19.000000 proxystore-0.5.0/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1057 2023-05-12 22:52:19.000000 proxystore-0.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4336 2023-05-12 22:52:30.652859 proxystore-0.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-05-12 22:52:19.000000 proxystore-0.5.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/_overrides/
+-rw-r--r--   0 runner    (1001) docker     (123)      196 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/_overrides/base.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.604859 proxystore-0.5.0/docs/_templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.604859 proxystore-0.5.0/docs/_templates/python/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/_templates/python/material/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/_templates/python/material/docstring/
+-rw-r--r--   0 runner    (1001) docker     (123)      275 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/_templates/python/material/docstring/admonition.html
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/_templates/python/material/function.html
+-rw-r--r--   0 runner    (1001) docker     (123)     2039 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/_templates/python/material/module.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/api/
+-rw-r--r--   0 runner    (1001) docker     (123)      937 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/api/cli.md
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/api/legacy-docs.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/concepts/
+-rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/concepts/connector.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1449 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/concepts/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3577 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/concepts/proxy.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5230 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/concepts/store.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/contributing/
+-rw-r--r--   0 runner    (1001) docker     (123)     3540 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/contributing/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1730 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/contributing/issues-pull-requests.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1963 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/contributing/releases.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/contributing/style-guide.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.612859 proxystore-0.5.0/docs/css/
+-rw-r--r--   0 runner    (1001) docker     (123)      588 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/css/extra.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1282 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/css/mkdocstrings.css
+-rw-r--r--   0 runner    (1001) docker     (123)      601 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/examples.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1242 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/generate_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6278 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/get-started.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.616860 proxystore-0.5.0/docs/guides/
+-rw-r--r--   0 runner    (1001) docker     (123)     3856 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/guides/endpoints-debugging.md
+-rw-r--r--   0 runner    (1001) docker     (123)     8781 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/guides/endpoints.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5534 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/guides/globus-compute.md
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/guides/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6992 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/guides/performance.md
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2331 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/installation.md
+-rw-r--r--   0 runner    (1001) docker     (123)      452 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/known-issues.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.616860 proxystore-0.5.0/docs/static/
+-rw-r--r--   0 runner    (1001) docker     (123)   134472 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/endpoint-overview.svg
+-rw-r--r--   0 runner    (1001) docker     (123)   149176 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/endpoint-peering.svg
+-rw-r--r--   0 runner    (1001) docker     (123)    46990 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/favicon.png
+-rw-r--r--   0 runner    (1001) docker     (123)    45464 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/icon.png
+-rw-r--r--   0 runner    (1001) docker     (123)    31401 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/logo-dark.png
+-rw-r--r--   0 runner    (1001) docker     (123)    31236 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/logo-light.png
+-rw-r--r--   0 runner    (1001) docker     (123)   106893 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/proxystore-overview.svg
+-rw-r--r--   0 runner    (1001) docker     (123)   106939 2023-05-12 22:52:19.000000 proxystore-0.5.0/docs/static/proxystore-schematic.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.620859 proxystore-0.5.0/examples/
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      555 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.620859 proxystore-0.5.0/examples/globus-compute/
+-rw-r--r--   0 runner    (1001) docker     (123)      967 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/globus-compute/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3704 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/globus-compute/mapreduce_globus_compute.py
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/globus-compute/run.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.620859 proxystore-0.5.0/examples/parsl/
+-rw-r--r--   0 runner    (1001) docker     (123)      266 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/parsl/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2102 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/parsl/mapreduce_parsl.py
+-rw-r--r--   0 runner    (1001) docker     (123)      561 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/parsl/run.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1590 2023-05-12 22:52:19.000000 proxystore-0.5.0/examples/store_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-05-12 22:52:19.000000 proxystore-0.5.0/mkdocs.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.620859 proxystore-0.5.0/proxystore/
+-rw-r--r--   0 runner    (1001) docker     (123)      525 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.624859 proxystore-0.5.0/proxystore/connectors/
+-rw-r--r--   0 runner    (1001) docker     (123)     1551 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3193 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/connector.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.628859 proxystore-0.5.0/proxystore/connectors/dim/
+-rw-r--r--   0 runner    (1001) docker     (123)      357 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18851 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/margo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1728 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18547 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/ucx.py
+-rw-r--r--   0 runner    (1001) docker     (123)      698 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17477 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/dim/zmq.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8960 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/endpoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4788 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22457 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/globus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4148 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/local.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16020 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/multi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/connectors/redis.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.628859 proxystore-0.5.0/proxystore/endpoint/
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7929 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5559 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12712 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5916 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17315 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/endpoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)      555 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      973 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/messages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8807 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/serve.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5873 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/endpoint/storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9113 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/globus.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.632859 proxystore-0.5.0/proxystore/p2p/
+-rw-r--r--   0 runner    (1001) docker     (123)      683 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4099 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/chunks.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15126 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/connection.py
+-rw-r--r--   0 runner    (1001) docker     (123)      860 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/counter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      402 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14235 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5603 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/messages.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12636 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/relay.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8916 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/relay_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/p2p/task.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5975 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     2708 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/serialize.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.632859 proxystore-0.5.0/proxystore/store/
+-rw-r--r--   0 runner    (1001) docker     (123)     2915 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23797 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1702 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2529 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/endpoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2125 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3111 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/globus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/local.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7365 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2346 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/multi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2097 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/redis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/store/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1971 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5226 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      155 2023-05-12 22:52:19.000000 proxystore-0.5.0/proxystore/warnings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.624859 proxystore-0.5.0/proxystore.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4336 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5419 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      709 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-12 22:52:30.000000 proxystore-0.5.0/proxystore.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5116 2023-05-12 22:52:19.000000 proxystore-0.5.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:52:30.652859 proxystore-0.5.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.636860 proxystore-0.5.0/testing/
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      585 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/compat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6987 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/connectors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/endpoint.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.636860 proxystore-0.5.0/testing/mocked/
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocked/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocked/globus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4853 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocked/pymargo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocked/redis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3185 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocked/ucx.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/mocking.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/relay_server.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.636860 proxystore-0.5.0/testing/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)      324 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/scripts/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3793 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/scripts/peer_connection_bandwidth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/scripts/peer_endpoint_bandwidth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3395 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/scripts/peer_manager_bandwidth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7517 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/stores.py
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-05-12 22:52:19.000000 proxystore-0.5.0/testing/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.640859 proxystore-0.5.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       59 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3150 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.640859 proxystore-0.5.0/tests/connectors/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/connector_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.644859 proxystore-0.5.0/tests/connectors/dim/
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/dim/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6969 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/dim/margo_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6786 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/dim/ucx_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3565 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/dim/zmq_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2894 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/endpoint_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/file_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8487 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/globus_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      512 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/local_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6908 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/multi_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      243 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/connectors/redis_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.644859 proxystore-0.5.0/tests/endpoint/
+-rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9132 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/cli_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1905 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/client_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14342 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/commands_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4350 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/config_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5595 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/endpoint_peering_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2275 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/endpoint_solo_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11848 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/serve_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1621 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/endpoint/storage_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/factory_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5203 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/globus_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.644859 proxystore-0.5.0/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/integration/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6533 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/integration/endpoints_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.648859 proxystore-0.5.0/tests/p2p/
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1605 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/chunks_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7568 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/connection_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/counter_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9470 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/manager_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4414 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/messages_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/relay_cli_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5033 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/relay_client_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7676 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/relay_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      813 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/p2p/task_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2498 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/proxy_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      954 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/serialization_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:52:30.652859 proxystore-0.5.0/tests/store/
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      856 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/cache_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2138 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/init_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4109 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/metrics_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4198 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/store_basics_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3569 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/store_metrics_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5520 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/store_proxy_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1137 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/store/utils_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      930 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/timer_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4465 2023-05-12 22:52:19.000000 proxystore-0.5.0/tests/utils_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      835 2023-05-12 22:52:19.000000 proxystore-0.5.0/tox.ini
```

### Comparing `proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/01_bug.yml` & `proxystore-0.5.0/.github/ISSUE_TEMPLATE/01_bug.yml`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/.github/ISSUE_TEMPLATE/02_feature.yml` & `proxystore-0.5.0/.github/ISSUE_TEMPLATE/02_feature.yml`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/.github/workflows/integration.yml` & `proxystore-0.5.0/.github/workflows/integration.yml`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/.github/workflows/publish.yml` & `proxystore-0.5.0/.github/workflows/publish.yml`

 * *Files 21% similar despite different names*

```diff
@@ -10,14 +10,16 @@
 
 jobs:
   publish:
     runs-on: ubuntu-latest
     steps:
       - name: Checkout
         uses: actions/checkout@v3
+        with:
+          fetch-depth: 0
 
       - name: Extract package version from pyproject.toml
         run: |
           echo "PACKAGE_VERSION=$(grep -Po '^version\s*=\s*\"\K.*?(?=\")' pyproject.toml)" >> $GITHUB_ENV
           echo "Found version in pyproject.toml: ${{ env.PACKAGE_VERSION }}"
 
       - name: Check package version is PEP440 compliant
@@ -37,17 +39,14 @@
         run: |
           if [ "${{ format('ProxyStore v{0}', env.PACKAGE_VERSION) }}" != "${{ github.event.release.name }}" ]
           then
             echo "ProxyStore v\$\{PACKAGE_VERSION\} = ProxyStore v${{ env.PACKAGE_VERSION }} does not match release title: ${{ github.event.release.name }}"
             exit 1
           fi
 
-      - name: Check version section in changelog
-        run: grep -E "^Version ${{ env.PACKAGE_VERSION}}$" docs/changelog.rst
-
       - name: Setup Python 3.11
         uses: actions/setup-python@v4
         with:
           python-version: '3.11'
 
       - name: Install pypa/build and build
         run: |
@@ -61,7 +60,18 @@
           files: dist/*
 
       - name: Publish to PyPI
         if: startsWith(github.ref, 'refs/tags')
         uses: pypa/gh-action-pypi-publish@release/v1
         with:
           password: ${{ secrets.PYPI_TOKEN }}
+
+      - name: Configure git
+        run: |
+          git config --local user.name "GitHub Actions Bot"
+          git config --local user.email "41898282+github-actions[bot]@users.noreply.github.com"
+
+      - name: Deploy docs for release version to gh-pages branch
+        if: startsWith(github.ref, 'refs/tags/')
+        run: |
+          pip install .[docs]
+          mike deploy --push "${{ env.PACKAGE_VERSION }}"
```

### Comparing `proxystore-0.4.1a1/.github/workflows/tests.yml` & `proxystore-0.5.0/.github/workflows/tests.yml`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/.gitignore` & `proxystore-0.5.0/.gitignore`

 * *Files 6% similar despite different names*

```diff
@@ -65,14 +65,15 @@
 instance/
 .webassets-cache
 
 # Scrapy stuff:
 .scrapy
 
 # Sphinx documentation
+# docs/api/
 docs/_build/
 docs/_autosummary/
 
 # PyBuilder
 target/
 
 # Jupyter Notebook
```

### Comparing `proxystore-0.4.1a1/LICENSE` & `proxystore-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/PKG-INFO` & `proxystore-0.5.0/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -1,61 +1,81 @@
-Metadata-Version: 2.1
-Name: proxystore
-Version: 0.4.1a1
-Summary: Python lazy object proxy interface for distributed stores.
-Author-email: Greg Pauloski <jgpauloski@uchicago.edu>
-License: Copyright (c) 2022 Greg Pauloski
-        
-        Permission is hereby granted, free of charge, to any person obtaining a copy
-        of this software and associated documentation files (the "Software"), to deal
-        in the Software without restriction, including without limitation the rights
-        to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-        copies of the Software, and to permit persons to whom the Software is
-        furnished to do so, subject to the following conditions:
-        
-        The above copyright notice and this permission notice shall be included in
-        all copies or substantial portions of the Software.
-        
-        THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-        IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-        FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-        AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-        LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-        OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
-        THE SOFTWARE.
-        
-Project-URL: repository, https://github.com/proxystore/proxystore
-Project-URL: documentation, https://proxystore.readthedocs.io
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: Implementation :: CPython
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-Provides-Extra: dev
-Provides-Extra: endpoints
-License-File: LICENSE
-
 # ProxyStore
 
-[![Documentation Status](https://readthedocs.org/projects/proxystore/badge/?version=latest)](https://proxystore.readthedocs.io/en/latest/?badge=latest)
+[![docs](https://github.com/proxystore/proxystore/actions/workflows/docs.yml/badge.svg)](https://github.com/proxystore/proxystore/actions/workflows/docs.yml)
+[![tests](https://github.com/proxystore/proxystore/actions/workflows/tests.yml/badge.svg?label=tests)](https://github.com/proxystore/proxystore/actions)
 [![pre-commit.ci status](https://results.pre-commit.ci/badge/github/proxystore/proxystore/main.svg)](https://results.pre-commit.ci/latest/github/proxystore/proxystore/main)
-[![Tests](https://github.com/proxystore/proxystore/actions/workflows/tests.yml/badge.svg)](https://github.com/proxystore/proxystore/actions)
 
-Python Lazy Object Proxy Interface for Distributed Stores
+ProxyStore provides pass-by-reference semantics for distributed Python
+applications through transparent object proxies. Moving data via proxies
+(1) decouples control flow from data flow, (2) enables producers to
+unilaterally (i.e., without the agreement of or awareness by the consumer)
+choose the best storage and communication channel for the data, and (3)
+perform just-in-time data movement directly between producer and consumer.
+
+ProxyStore's goals are to:
+
+* **Improve productivity.** ProxyStore enables easy decoupling of
+  communication from the rest of the code, allowing developers to focus
+  on functionality and performance.
+* **Improve compatibility.** Consumers of data can be agnostic to the
+  communication method because object proxies handle the communication
+  behind the scenes.
+* **Improve performance.** Transport methods and object stores can be changed
+  at runtime to optimal choices for the given data without the consumers
+  being aware of the change.
+
+ProxyStore provides support for many third-party mediated communication methods
+out-of-the-box including
+[Globus Transfer](https://www.globus.org/data-transfer),
+[KeyDB](https://docs.keydb.dev/), and
+[Redis](https://redis.io/).
+Custom communication methods built on
+[Mochi](https://mochi.readthedocs.io/en/latest/margo.html),
+[UCX](https://openucx.org/),
+[WebRTC](https://webrtc.org/), and
+[ZeroMQ](https://zeromq.org/)
+are provided for high-performance and multi-site applications.
+
+Read more about ProxyStore's concepts [here](https://docs.proxystore.dev/main/concepts/).
+Complete documentation for ProxyStore is available at
+[docs.proxystore.dev](https://docs.proxystore.dev).
 
 ## Installation
 
-Install via pip:
 ```bash
-# Base install
-pip install proxystore
-# Extras install for serving Endpoints
-pip install proxystore[endpoints]
+$ pip install proxystore
+$ pip install proxystore[all]
 ```
 
-More details are available on the [Get Started](https://proxystore.readthedocs.io/en/latest/getstarted.html) guide.
-For local development, see the [Contributing](https://proxystore.readthedocs.io/en/latest/contributing.html) guide.
+See the [Installation](https://docs.proxystore.dev/main/installation) guide for more information about the available extra install options.
+For local development, see the [Contributing](https://docs.proxystore.dev/main/contributing) guide.
+
+Additional features are available in the [`proxystore-extensions`](https://github.com/proxystore/extensions) package.
+
+## Example
+
+Getting started with ProxyStore requires a few lines of code.
+
+```python
+from proxystore.connectors.redis import RedisConnector
+from proxystore.proxy import Proxy
+from proxystore.store import register_store
+from proxystore.store import Store
 
-## Documentation
+store = Store('my-store', RedisConnector('localhost', 6379))
+
+# Store the object and get a proxy. The proxy acts
+# like a reference to the object.
+data = MyDataType(...)
+proxy = store.proxy(data)
+assert isinstance(proxy, Proxy)
+
+def my_function(x: MyDataType) -> ...:
+    # x is resolved my-store on first use transparently to the
+    # function. Then x behaves as an instance of MyDataType.
+    assert isinstance(x, MyDataType)
+
+my_function(proxy)  # Succeeds
+```
 
-Complete documentation for ProxyStore available [here](https://proxystore.readthedocs.io/en/latest).
+Check out the [Get Started](https://docs.proxystore.dev/main/get-started)
+guide to learn more!
```

### Comparing `proxystore-0.4.1a1/docs/advanced.rst` & `proxystore-0.5.0/proxystore/proxy.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,184 +1,197 @@
-Advanced
-########
+"""Proxy implementation and helpers."""
+from __future__ import annotations
 
-Proxies
-=======
-
-Proxies can be created easily using ProxyStore.
-
-.. code-block:: python
-
-   from proxystore.proxy import Proxy
-
-   def resolve_object(...):
-       # Function that produces the object of interest
-       return obj
-
-   p = Proxy(resolve_object)
-
-:code:`resolve_object()` will be called when the proxy :code:`p` does its
-just-in-time resolution, and then :code:`p` will behave exactly like
-:code:`obj`.
-A factory for a :any:`Proxy <proxystore.proxy.Proxy>` can be
-any callable object (i.e., object which implements :code:`__call__`).
-
-Proxies are powerful because they can intercept and redefine functionality of
-an object while emulating the rest of the objects behavior.
-
-.. code-block:: python
-
-   import numpy as np
-   from proxystore.proxy import Proxy
-
-   x = np.array([1, 2, 3])
-
-   class MyFactory():
-       def __init__(self, obj):
-           self.obj = obj
-
-       def __class__(self):
-           return self.obj
-
-   p = Proxy(MyFactory(x))
-
-   # A proxy is an instance of its wrapped object
-   assert isinstance(p, Proxy)
-   assert isinstance(p, np.ndarray)
-
-   # The proxy can do everything the numpy array can
-   assert np.array_equal(p, [1, 2, 3])
-   assert np.sum(p) == 6
-   y = x + p
-   assert np.array_equal(y, [2, 4, 6])
-
-The ProxyStore :any:`Proxy <proxystore.proxy.Proxy>` is built on the proxy
-from `lazy-object-proxy <https://github.com/ionelmc/python-lazy-object-proxy>`_
-which intercepts all calls to the object's magic functions
-(:code:`__func_name__()` functions) and forwards the calls to the wrapped
-object. If the wrapped object has not been resolved yet, the proxy calls the
-factory that was passed to the proxy constructor to retrieve the object that
-should be wrapped.
-
-Generally, a proxy is only ever resolved once.
-However, when a proxy is serialized, only the factory is serialized, and when
-the proxy is deserialized again and used, the factory will be called again to
-resolve the object.
-
-Utilities
----------
-
-Proxystore provides some useful utility functions for dealing with proxies.
-
-.. code-block:: python
-
-   from proxystore import proxy
-
-   p = proxy.Proxy(...)
-
-   # Check if a proxy has been resolved yet
-   proxy.is_resolved(p)
-
-   # Force a proxy to resolve itself
-   proxy.resolve(p)
-
-   # Extract the wrapped object from the proxy
-   x = proxy.extract(p)
-   assert not isinstance(x, proxy.Proxy)
-
-Other Uses
-----------
-
-Proxies can be used add functionality to existing objects.
-Two common examples are access control and partial resoluion.
-
-Stores
-======
-
-Asynchronous Resolving
-----------------------
-
-It is common in distributed computation for inputs to functions executed
-remotely to not be needed immediately upon execution.
-Proxies created by a :class:`~proxystore.store.base.Store` support
-asynchronous resolution to overlap communication and computation.
-
-.. code-block:: python
-
-   from proxystore.store.utils import resolve_async
-
-   def complex_function(large_proxied_input):
-       resolve_async(large_proxied_input)
-
-       # More computation...
-
-       # First access to the proxy will not be as expensive because
-       # of the asynchronous resolution
-       compute_input(large_proxied_input)
-
-.. _advanced-caching:
-
-Caching
--------
-
-:class:`~proxystore.store.base.Store` provides built in caching functionality.
-Caches are local to the Python process but will speed up the resolution when
-multiple proxies refer to the same object.
-
-.. code-block:: python
-
-   from proxystore.store.file import FileStore
-
-   # Cache size of 16 is the default
-   FileStore('mystore', store_dir='/tmp/proxystore', cache_size=16)
-
-Transactional Guarantees
-------------------------
-
-ProxyStore is designed around optimizing the communication of ephemeral data
-(e.g., inputs and outputs of functions) which is typically write-once,
-read-many. Thus, ProxyStore does not provides any guarantees about object
-versions if a user manually overwrites an object.
-
-Serialization
--------------
-
-All :class:`~proxystore.store.base.Store` operation uses ProxyStore's provided
-serialization utilities (:py:mod:`~proxystore.serialize`) by default. However,
-all :class:`~proxystore.store.base.Store` methods that move data in or out of
-the store can be provided custom serializers or deserializers of the form:
-
-.. code-block:: python
-
-   serializer = Callable[[Any], bytes]
-   deserializer = Callable[[bytes], Any]
-
-In some cases, data may already be serialized in which case an identity
-function can be passed as the serializer/deserializer (e.g., ``lambda x: x``).
-Implementing a custom serializer may be beneficial for complex structures
-where pickle/cloudpickle (the default serializers used by ProxyStore) are
-innefficient. E.g.,
-
-.. code-block:: python
-
-   import torch
-   import io
-
-   from proxystore.serialize import serialize
-   from proxystore.store.redis import RedisStore
-
-   def serialize_torch_model(obj: Any) -> bytes:
-       if isinstance(obj, torch.nn.Module):
-           buffer = io.BytesIO()
-           torch.save(model, buffer)
-           return buffer.read()
-       else:
-           # Fallback for unsupported types
-           return serialize(obj)
-
-   mymodel = torch.nn.Module()
-
-   store = RedisStore(...)
-   key = store.set(mymodel, serializer=serialize_torch_model)
-
-See `Issue #146 <https://github.com/proxystore/proxystore/issues/146>`_ for
-further discussion.
+import sys
+from typing import Any
+from typing import Callable
+from typing import Generic
+from typing import TypeVar
+from typing import Union
+
+if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
+    from typing import SupportsIndex
+else:  # pragma: <3.8 cover
+    SupportsIndex = int
+
+if sys.version_info >= (3, 10):  # pragma: >=3.10 cover
+    from typing import TypeAlias
+else:  # pragma: <3.10 cover
+    from typing_extensions import TypeAlias
+
+from lazy_object_proxy import slots
+
+import proxystore
+
+T = TypeVar('T')
+FactoryType: TypeAlias = Callable[[], T]
+
+
+def _proxy_trampoline(factory: FactoryType[T]) -> Proxy[T]:
+    """Trampoline for helping Proxy pickling.
+
+    `#!python lazy_object_proxy.slots.Proxy` defines a property for
+    `__modules__` which confuses pickle when trying to locate the class in the
+    module. The trampoline is a top-level function so pickle can correctly
+    find it in this module.
+
+    Args:
+        factory: Factory to pass to the [`Proxy`][proxystore.proxy.Proxy]
+            constructor.
+
+    Returns:
+        Proxy initialized with `factory`.
+    """
+    return Proxy(factory)
+
+
+class Proxy(slots.Proxy, Generic[T]):
+    """Lazy Object Proxy.
+
+    An extension of the Proxy from
+    [lazy-object-proxy](https://github.com/ionelmc/python-lazy-object-proxy){target=_blank}
+    with modified pickling behavior.
+
+    An object proxy acts as a thin wrapper around a Python object, i.e.
+    the proxy behaves identically to the underlying object. The proxy is
+    initialized with a callable factory object. The factory returns the
+    underlying object when called, i.e. 'resolves' the proxy. The does
+    just-in-time resolution, i.e., the proxy
+    does not call the factory until the first access to the proxy (hence, the
+    lazy aspect of the proxy).
+
+    The factory contains the mechanisms to appropriately resolve the object,
+    e.g., which in the case for ProxyStore means requesting the correct
+    object from the backend store.
+
+    ```python
+    x = np.array([1, 2, 3])
+    f = ps.factory.SimpleFactory(x)
+    p = ps.proxy.Proxy(f)
+    assert isinstance(p, np.ndarray)
+    assert np.array_equal(p, [1, 2, 3])
+    ```
+
+    Note:
+        The `factory`, by default, is only ever called once during the
+        lifetime of a proxy instance.
+
+    Note:
+        When a proxy instance is pickled, only the `factory` is pickled, not
+        the wrapped object. Thus, proxy instances can be pickled and passed
+        around cheaply, and once the proxy is unpickled and used, the `factory`
+        will be called again to resolve the object.
+
+    Warning:
+        Python bindings to other languages (e.g., C, C++) may throw type
+        errors when receiving a [`Proxy`][proxystore.proxy.Proxy] instance.
+        Casting the proxy or extracting the target object may be needed.
+
+        ```python
+        >>> import io
+        >>> from proxystore.proxy import Proxy
+        >>> s = 'mystring'
+        >>> p = Proxy(lambda: s)
+        >>> io.StringIO(p)
+        Traceback (most recent call last):
+          File "<stdin>", line 1, in <module>
+        TypeError: initial_value must be str or None, not Proxy
+        >>> io.StringIO(str(p))  # succeeds
+        ```
+
+    Args:
+        factory: Callable object that returns the underlying object when
+            called.
+
+    Raises:
+        TypeError: If `factory` is not callable.
+    """
+
+    def __init__(self, factory: FactoryType[T]) -> None:
+        if not callable(factory):
+            raise TypeError('factory must be callable')
+        super().__init__(factory)
+
+    def __reduce__(
+        self,
+    ) -> tuple[Callable[[FactoryType[T]], Proxy[T]], tuple[FactoryType[T]]]:
+        # Use trampoline function for pickling and
+        # override `Proxy.__reduce__` so that we only pickle the Factory
+        # and not the object itself to reduce size of the pickle.
+        return _proxy_trampoline, (
+            object.__getattribute__(self, '__factory__'),
+        )
+
+    def __reduce_ex__(
+        self,
+        protocol: SupportsIndex,
+    ) -> tuple[Callable[[FactoryType[T]], Proxy[T]], tuple[FactoryType[T]]]:
+        return self.__reduce__()
+
+
+ProxyType: TypeAlias = Union[Proxy[T], T]
+
+
+def extract(proxy: proxystore.proxy.Proxy[T]) -> T:
+    """Return object wrapped by proxy.
+
+    If the proxy has not been resolved yet, this will force
+    the proxy to be resolved prior.
+
+    Args:
+        proxy: Proxy instance to extract from.
+
+    Returns:
+        Object wrapped by proxy.
+    """
+    return proxy.__wrapped__
+
+
+def is_resolved(proxy: proxystore.proxy.Proxy[T]) -> bool:
+    """Check if a proxy is resolved.
+
+    Args:
+        proxy: Proxy instance to check.
+
+    Returns:
+        `True` if `proxy` is resolved (i.e., the `factory` has been called) \
+        and `False` otherwise.
+    """
+    return proxy.__resolved__
+
+
+def resolve(proxy: proxystore.proxy.Proxy[T]) -> None:
+    """Force a proxy to resolve itself.
+
+    Args:
+        proxy: Proxy instance to force resolve.
+    """
+    proxy.__wrapped__  # noqa: B018
+
+
+class ProxyLocker(Generic[T]):
+    """Proxy locker that prevents resolution of wrapped proxies.
+
+    The class prevents unintended access to a wrapped proxy to ensure a proxy
+    is not resolved. The wrapped proxy can be retrieved with
+    `#!python proxy = ProxyLocker(proxy).unlock()`.
+
+    Args:
+        proxy: Proxy to lock.
+    """
+
+    def __init__(self, proxy: Proxy[T]) -> None:
+        self._proxy = proxy
+
+    def __getattribute__(self, attr: str) -> Any:
+        # Override to raise an error if the proxy is accessed.
+        if attr == '_proxy':
+            raise AttributeError('Cannot access proxy attribute of a Locker')
+        return super().__getattribute__(attr)
+
+    def unlock(self) -> Proxy[T]:
+        """Retrieve the locked proxy.
+
+        Returns:
+            Proxy object.
+        """
+        return super().__getattribute__('_proxy')
```

### Comparing `proxystore-0.4.1a1/docs/getstarted.rst` & `proxystore-0.5.0/docs/get-started.md`

 * *Files 18% similar despite different names*

```diff
@@ -1,37 +1,29 @@
-.. _get-started:
+# Get Started
 
-Get Started
-###########
+![ProxyStore Overview](static/proxystore-overview.svg){ width="75%" style="display: block; margin: 0 auto" }
+> **Figure 1:** ProxyStore allows developers to communicate objects via *proxies*.
+> Proxies act as lightweight references that resolve to a *target* object upon use.
+> Communication via proxies gives applications the illusion that objects are
+> moving through a specified path (e.g., through a network socket, cloud
+> server, workflow engine, etc.) while the true path the data takes is
+> different. Transporting the lightweight proxies through the application or
+> systems can be far more efficient and reduce overheads.
 
-.. figure:: static/overview.png
-   :align: center
-   :figwidth: 100 %
-   :alt: ProxyStore Overview
-
-   ProxyStore allows developers to communicate objects via *proxies*. Proxies
-   act as lightweight references that resolve to a *target* object upon use.
-   Communication via proxies gives applications the illusion that objects
-   are moving through a specified path (e.g., through a network
-   socket, cloud server, workflow engine, etc.) while the true path the data
-   takes is different. Transporting the lightweight proxies through the
-   application or systems can be far more efficient and reduce overheads.
-
-Overview
---------
+## Overview
 
 ProxyStore provides a unique interface to object stores through transparent
 object proxies that is designed to simplify the use of object stores for
 transferring large objects in distributed applications.
 
-`Proxies` are used to intercept and redefine operations on a `target` object.
-A `transparent` proxy behaves identically to its target object
+*Proxies* are used to intercept and redefine operations on a *target* object.
+A *transparent* proxy behaves identically to its target object
 because the proxy forwards all operations on itself to the target.
-A `lazy` proxy provides just-in-time `resolution` of the target object via
-a `factory` function. Factories return the target object when called, and a
+A *lazy* proxy provides just-in-time *resolution* of the target object via
+a *factory* function. Factories return the target object when called, and a
 proxy, initialized with a factory, will delay calling the factory to retrieve
 the target object until the first time the proxy is accessed.
 
 ProxyStore uses lazy transparent object proxies as the interface to object
 stores. When an object is proxied, the object is placed in the specified
 object store, a factory containing the information needed to retrieve the
 object from the store is created, and a proxy, initialized with the factory,
@@ -39,116 +31,106 @@
 The resulting proxy is essentially a lightweight reference to the target that
 will resolve itself to the target and behave as the target once the proxy
 is first used.
 Thus, proxies can be used anywhere in-place of the true object and will
 resolve themselves without the program being aware.
 
 ProxyStore provides the proxy interface to a number of commonly used object
-stores as well as the :any:`Proxy <proxystore.proxy.Proxy>` and
-:class:`~proxystore.factory.Factory` building blocks to allow developers
+stores as well as the [`Proxy`][proxystore.proxy.Proxy] and
+[`Factory`][proxystore.factory.Factory] building blocks to allow developers
 to create powerful just-in-time resolution functionality for Python objects.
 
-Installation
-------------
-
-.. code-block:: bash
-
-   $ pip install proxystore
-
-Serving :doc:`ProxyStore Endpoints <./guides/endpoints>` requires installing
-using the extras install.
-
-.. code-block:: bash
-
-   $ pip install proxystore[endpoints]
-
-See :doc:`Contributing <./contributing>` if you are installing for local
-development.
-
-Usage
------
+## Usage
 
 ProxyStore is intended to be used via the
-:class:`~proxystore.store.base.Store` interface which provide the
-:py:meth:`~proxystore.store.base.Store.proxy` method for placing objects
+[`Store`][proxystore.store.base.Store] interface which provide the
+[`Store.proxy()`][proxystore.store.base.Store.proxy] method for placing objects
 in stores and creating proxies that will resolve to the associated object in
 the store.
 
-ProxyStore provides many :class:`~proxystore.store.base.Store`
-implementations (list :py:mod:`here <proxystore.store>`) and more can be
-added by extending the :class:`~proxystore.store.base.Store` class.
+A [`Store`][proxystore.store.base.Store] is initialized with a
+[`Connector`][proxystore.connectors.connector.Connector] which serves as the
+low-level interface to an byte-level object store.
+ProxyStore provides many
+[`Connector`][proxystore.connectors.connector.Connector] implementations and
+third-party code can provide custom implementations provided they meet the
+[`Connector`][proxystore.connectors.connector.Connector] protocol
+specification.
 
 The following example uses the
-:class:`~proxystore.store.redis.RedisStore` to interface with a
-running Redis server using proxies.
+[`RedisConnector`][proxystore.connectors.redis.RedisConnector] to interface
+with an already running Redis server using proxies.
 
-.. code-block:: python
+```python title="Basic ProxyStore Usage" linenums="1"
+from proxystore.connectors.redis import RedisConnector
+from proxystore.store import get_store
+from proxystore.store import register_store
+from proxystore.store import Store
 
-   from proxystore.store import get_store
-   from proxystore.store import register_store
-   from proxystore.store.redis import RedisStore
+store = Store(name='my-store', RedisConnector(hostname='localhost', port=1234))
+register_store(store)
 
-   store = RedisStore(name='my-store', hostname='localhost', port=1234)
-   register_store(store)
+store = get_store('my-store')  # (1)!
 
-   # A registered store can be retrieved by name
-   store = get_store('my-store')
+key = store.put(my_object)  # (2)!
+assert my_object == store.get(key)
 
-   # Stores have basic get/set functionality
-   key = store.set(my_object)
-   assert my_object == store.get(key)
+p = store.proxy(my_object)  # (3)!
 
-   # Place an object in the store and return a proxy
-   p = store.proxy(my_object)
+assert isinstance(p, type(my_object))  # (4)!
+```
 
-   # The proxy, when used, will behave as the target
-   assert isinstance(p, type(my_object))
+1. A registered store can be retrieved by name.
+2. Stores have basic get/put functionality.
+3. Place an object in the store and return a proxy.
+4. The proxy, when used, will behave as the target.
 
-This proxy, :code:`p`, can be cheaply serialized and communicated to any
+This proxy, `p`, can be cheaply serialized and communicated to any
 arbitrary Python process as if it were the target object itself. Once the
 proxy is used on the remote process, the underlying factory function will
 be executed to retrieve the target object from the Redis server.
 
-Using the :class:`~proxystore.store.base.Store` store interface allows
+Using the [`Store`][proxystore.store.base.Store] store interface allows
 developers to write code without needing to worry about how data communication
 is handled and reduces the number of lines of code that need to be changed
 when adding or changing the communication methods.
 
 For example, if you want to execute a function and the input data may be
 passed directly, via a key to an object in Redis, or as a filepath to a
 serialized object on disk, you will need boilerplate code that looks like:
 
-.. code-block:: python
-
-   def my_function(input: MyDataType | str | ...) -> None:
-       if is_filepath(input_data):
-           data = read_and_deserialize(input)
-       elif is_redis_key(input_data):
-           data = redis_client.get(input)
-       elif is_other_communication_method(input_data):
-           ...
-       elif isinstance(input, MyDataType):
-           data = input
-       else:
-            raise ValueError(...)
+```python linenums="1"
+def my_function(input: MyDataType | str | ...) -> None:
+   if is_filepath(input_data):
+       data = read_and_deserialize(input)
+   elif is_redis_key(input_data):
+       data = redis_client.get(input)
+   elif is_other_communication_method(input_data):
+       ...
+   elif isinstance(input, MyDataType):
+       data = input
+   else:
+        raise ValueError(...)
 
-       # Compute using the data
+   # Compute using the data
+```
 
 This function is hard to type and must be extended every time a new
 communication method is used. With proxies, all of the boilerplate code
 can be removed because the proxy will contain within itself all of the
 necessary code to resolve the object.
 
-.. code-block:: python
+```python linenums="1"
+def my_function(input: MyDataType) -> None:
+   assert isinstance(input, MyDataType)  # (1)!
 
-   def my_function(input: MyDataType) -> None:
-       # Always true even if input is a proxy
-       assert isinstance(input, MyDataType)
+   # Compute using the data
+```
 
-       # Compute using the data
+1. Always true even if input is a proxy.
 
 In this model, only the producer of the data needs to be aware of which
 ProxyStore backend to use, and no modification to consumer code are ever
 required.
 
 **How is this more efficient?**
 
@@ -157,31 +139,10 @@
 1. Unused proxies are not resolved so not resources/time were wasted on the
    communication.
 2. Object communication always takes place between the producer, the store, and
    the consumer meaning communication is not wasted on intermediate processes
    which have a proxy but do not use it.
 3. Different backends can be used that are optimized for specific usage
    patterns.
-4. Proxies have built-in caching for frequently used objects
-   (:ref:`advanced-caching`).
-
-See :doc:`Advanced Usage <./advanced>` to learn more!
-
-Related
--------
+4. Proxies have built-in caching for frequently used objects.
 
-**Examples:**
-Examples of integrating ProxyStore into distributed applications built on
-`FuncX <https://funcx.org/>`_ and `Parsl <https://parsl-project.org/>`_ are
-`here <https://github.com/proxystore/proxystore/tree/main/examples>`_.
-
-**Benchmarks:**
-ProxyStore benchmarks are maintained at `<https://github.com/proxystore/proxystore-benchmarks>`_.
-
-Known Issues
-------------
-
-* :doc:`ProxyStore Endpoints <./guides/endpoints>` are not supported for
-  Python 3.7 on ARM-based Macs because
-  `aiortc <https://aiortc.readthedocs.io/>`_ does not have the corresponding
-  wheels. The base ProxyStore package can still be installed on this
-  software/hardware configurations---just not with the ``endpoints`` extras.
+See the [Concepts](concepts/index.md) to learn more!
```

### Comparing `proxystore-0.4.1a1/docs/guides/endpoints.rst` & `proxystore-0.5.0/docs/guides/endpoints.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,197 +1,197 @@
-.. _endpoints-guide:
+# Peer-to-Peer Endpoints
 
-Peer-to-Peer Endpoints
-######################
+*Last updated 2 May 2023*
 
 ProxyStore Endpoints are in-memory object stores
 with peering capabilities. Endpoints enable data transfer with proxies
 between multiple sites using NAT traversal.
 
-.. warning::
-
-   Endpoints are experimental and the interfaces and underlying
-   implementations will likely change. Refer to the API docs for the most
-   up-to-date information.
-
-.. warning::
-
-   Endpoints do not have user authentication yet, so use at your own risk.
-
-Overview
---------
-
-At its core, the :class:`~proxystore.endpoint.endpoint.Endpoint` is
-an in-memory data store built on asyncio. Endpoints provide a REST
-API, served using `Quart <https://pgjones.gitlab.io/quart/>`_, and ProxyStore
-provides the :class:`~proxystore.store.endpoint.EndpointStore` as
+!!! warning
+    Endpoints are experimental and the interfaces and underlying
+    implementations will likely change. Refer to the API docs for the most
+    up-to-date information.
+
+!!! warning
+    Endpoints do not have user authentication yet, so use at your own risk.
+
+## Overview
+
+At its core, the [`Endpoint`][proxystore.endpoint.endpoint.Endpoint] is
+an in-memory data store built on asyncio. Endpoints provide a REST API, served
+using [`Quart`](https://pgjones.gitlab.io/quart/), and ProxyStore provides the
+[`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector] as
 the primary interface for clients to interact with endpoints.
 
-.. figure:: ../static/endpoints.png
-   :align: center
-   :figwidth: 100 %
-   :alt: ProxyStore Endpoints
-
-   **Figure 1:** ProxyStore Endpoints overview. Clients can make requests to any endpoint
-   and those request will be forwarded to the correct endpoint. Endpoints
-   establish peer-to-peer connections using UDP hole-punching and a publicly
-   accessible signaling server.
+![ProxyStore Endpoints](../static/endpoint-peering.svg){ width="100%" }
+> <b>Figure 1:</b> ProxyStore Endpoints overview. Clients can make requests to
+> any endpoint and those request will be forwarded to the correct endpoint.
+> Endpoints establish peer-to-peer connections using UDP hole-punching and a
+> publicly accessible relay server.
 
 Unlike popular in-memory data stores (Redis, Memcached, etc.), ProxyStore
 endpoints can operate as peers even from behind different NATs without the need
 to open ports or SSH tunnels. To achieve direct data transfer between peers,
-endpoints use the `WebRTC <https://webrtc.org/>`_ standard to determine
+endpoints use the [WebRTC](https://webrtc.org/) standard to determine
 how the peers can connect.
 
-As shown in **Fig. 1**, endpoints use a commonly accessible *signaling server*
+As shown in **Fig. 1**, endpoints use a commonly accessible *relay server*
 to facilitate peer connections. When an endpoint is started, the Endpoint
-registers with the signaling server. Then, when an endpoint needs to make a
+registers with the relay server. Then, when an endpoint needs to make a
 request from a peer, (1) the endpoint creates an *offer* and asks the
-signaling server to forward the offer to the peer endpoint. The signaling
+relay server to forward the offer to the peer endpoint. The relay
 server forwards the offer (2) and the peer endpoint creates an *answer* to the
 received offer. The peer endpoint returns the *answer* to the original
-endpoint via the signaling server (3, 4).
+endpoint via the relay server (3, 4).
 
 The offer and answer contain information about the local and remote sessions
 of the endpoints which can be used to complete the peer-to-peer connection (5).
 (*Note*: this is a great simplification and more details can be found at
-`<https://webrtc.org/getting-started/peer-connections>`_.) The peers will then
+https://webrtc.org/getting-started/peer-connections.) The peers will then
 keep a data channel open between themselves for the remainder of their
 lifetime.
 
 Clients interacting with an endpoint via the REST API and typical object store
 operations (*get*, *set*, etc.) specify a *key* and an *endpoint UUID*.
 Endpoints that receive a request with a different endpoint UUID will attempt
 a peer connection to the endpoint if one does not exist already and forward
 the request along and facilitate returning the response back to the client.
 
-Endpoint CLI
-------------
+## Endpoint CLI
 
-Endpoints can be configure and started with the ``proxystore-endpoint``
+Endpoints can be configure and started with the `proxystore-endpoint`
 command.
 
-.. code-block:: bash
+```bash
+$ proxystore-endpoint configure my-endpoint --relay-server wss://relay-address.com
+Configured endpoint my-endpoint <12b8f3b6-6c0e-4141-b851-870895e3eb3c>.
 
-   $ proxystore-endpoint configure my-endpoint --port 9732 --server remote-server.com:3574
-   Configured endpoint my-endpoint <12b8f3b6-6c0e-4141-b851-870895e3eb3c>.
-
-   To start the endpoint:
-       $ proxystore-endpoint start my-endpoint
+To start the endpoint:
+   $ proxystore-endpoint start my-endpoint
+```
 
-Endpoint configurations are stored to ``$PROXYSTORE_HOME/{endpoint-name}``
-(see :py:func:`~proxystore.utils.home_dir`) and contain the name, UUID,
-host address, port, and singaling server address.
+Endpoint configurations are stored to `$PROXYSTORE_HOME/{endpoint-name}`
+or `$XDG_DATA_HOME/proxystore/{endpoint-name}`
+(see [`home_dir()`][proxystore.utils.home_dir]) and contain the name, UUID,
+host address, port, relay server address, and more.
+
+!!! tip
+
+    By default, `$XDG_DATA_HOME/proxystore` will usually resolve to
+    `~/.local/share/proxystore`. You can change this behavior by setting
+    `$PROXYSTORE_HOME` in your `~/.bashrc` or similar configuration file.
+    ```bash
+    export PROXYSTORE_HOME="$HOME/.proxystore"
+    ```
 
-#. **Name:** readable name of the endpoint. Used for management in the CLI and
+1. **Name:** readable name of the endpoint. Used for management in the CLI and
    to improve log readability.
-#. **UUID:** primary identifier of the endpoint. The signaling server will
+2. **UUID:** primary identifier of the endpoint. The relay server will
    use this UUID to keep track of endpoints.
-#. **Host address:** host address of the Quart app for the endpoint.
-   Defaults to the IP address of host the endpoint is configured on.
-   Note: this address is only used by clients within the local network and
-   can be set to *localhost* if the client and endpoints are on the same
-   host.
-#. **Port:** port the Quart app for the endpoint will listening on. Defaults to
-   9753.
-#. **Signaling server address**: address of signaling server to use for peer
+3. **Host address:** address of the host the endpoint was last started on.
+   Each time the endpoint is started, this address is updated.
+4. **Port:** port the endpoint will listening on. Defaults to 8765.
+5. **Relay server address**: address of relay server to use for peer
    connections. All endpoints that may peer with each other must use the same
-   signaling server. Signaling servers are optional, and if unspecified, the
+   relay server. Relay servers are optional, and if unspecified, the
    endpoint will operate without peering functionalities.
 
+!!! tip
+
+    Endpoints provide no data persistence by default, but this can be enabled
+    by passing the `--persist` flag when configuring the endpoint or by
+    setting `"database_path"` in the config. When set, blobs stored by the
+    endpoint will be written to a SQLite database file. Note this will
+    result in slower performance.
+
+An up-to-date configuration description can found in the
+[`EndpointConfig`][proxystore.endpoint.config.EndpointConfig] docstring.
+
 Starting the endpoint will load the configuration from the ProxyStore home
 directory, initialize the endpoint, and start a Quart app using the host and
 port.
 
-.. code-block:: bash
-
-   $ proxystore-endpoint start my-endpoint
+```bash
+$ proxystore-endpoint start my-endpoint
+```
 
-EndpointStore
--------------
+## EndpointConnector
 
 The primary interface to endpoints is the
-:class:`~proxystore.store.endpoint.EndpointStore`.
-
-.. note::
-
-   This section assumes familiarity with proxies and the
-   :class:`~proxystore.store.base.Store` interface. See the
-   :ref:`get-started` guide before getting started with endpoints.
+[`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector].
 
-.. code-block:: python
+!!! note
+    This section assumes familiarity with proxies and the
+    [`Store`][proxystore.store.base.Store] interface. See the
+    [Get Started](../get-started.md) guide before getting started with endpoints.
+
+```python title="Endpoint Client Example" linenums="1"
+from proxystore.connectors.endpoint import EndpointConnector
+from proxystore.store import Store
+
+connector = EndpointConnector(
+   endpoints=[
+       '5349ffce-edeb-4a8b-94a6-ab16ade1c1a1',
+       'd62910f6-0d29-452e-80b7-e0cd601949db',
+       ...
+   ],
+)
+store = Store(name='default', connector=connector)
 
-   from proxystore.store.endpoint import EndpointStore
+p = store.proxy(my_object)
+```
 
-   store = EndpointStore(
-       name='default',
-       endpoints=[
-           '5349ffce-edeb-4a8b-94a6-ab16ade1c1a1',
-           'd62910f6-0d29-452e-80b7-e0cd601949db',
-           ...
-       ],
-    )
-
-    p = store.proxy(my_object)
-
-The :class:`~proxystore.store.endpoint.EndpointStore` takes
+The [`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector] takes
 a list of endpoint UUIDs. This list represents any endpoint that proxies
 created by this store may interact with to resolve themselves. The
-:class:`~proxystore.store.endpoint.EndpointStore` will use this
+[`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector] will use this
 list to find its *home* endpoint, the endpoint that will be used to issue
 operations to. To find the *home* endpoint, the ProxyStore home directory
 will be scanned for any endpoint configurations matching
 the one of the UUIDs. If a match is found, the
-:class:`~proxystore.store.endpoint.EndpointStore` will attempt
+[`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector] will attempt
 to connect to the endpoint using the host and port in the configuration. This
 process is repeated until a reachable endpoint is found. While the user could
 specify the home endpoint directly, the home endpoint may change when a proxy
 travels to a different machine.
 
-Proxy Lifecycle
----------------
+## Proxy Lifecycle
 
-.. figure:: ../static/dataflow.png
-   :align: center
-   :figwidth: 100 %
-   :alt: Dataflow with Proxies and Endpoints
-
-   **Figure 2:** Flow of data when transferring objects via proxies and
-   endpoints.
+![Dataflow with Proxies and Endpoints](../static/endpoint-overview.svg){ width="75%" style="display: block; margin: 0 auto" }
+> <b>Figure 2:</b> Flow of data when transferring objects via proxies and endpoints.
 
 In distributed systems, proxies created from an
-:class:`~proxystore.store.endpoint.EndpointStore` can be used
+[`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector] can be used
 to facilitate simple and fast data communication.
 The flow of data and their associated proxies are shown in **Fig. 2**.
 
-#. Host A creates a proxy of the *target* object. The serialized *target*
+1. Host A creates a proxy of the *target* object. The serialized *target*
    is placed in Host A's home/local endpoint (Endpoint 1).
    The proxy contains the key referencing the *target*, the endpoint UUID with
    the *target* data (Endpoint 1's UUID), and the list of
    all endpoint UUIDs configured with the
-   :class:`~proxystore.store.endpoint.EndpointStore`
+   [`EndpointConnector`][proxystore.connectors.endpoint.EndpointConnector]
    (the UUIDs of Endpoints 1 and 2).
-#. Host A communicates the proxy object to Host B. This communication is
+2. Host A communicates the proxy object to Host B. This communication is
    cheap because the proxy is just a thin reference to the object.
-#. Host B receives the proxy and attempts to use the proxy initiating the
+3. Host B receives the proxy and attempts to use the proxy initiating the
    proxy *resolve* process. The proxy requests the data from Host B's
    home endpoint (Endpoint 2).
-#. Endpoint 2 sees that the proxy is requesting data from a different endpoint
+4. Endpoint 2 sees that the proxy is requesting data from a different endpoint
    (Endpoint 1) so Endpoint 2 initiates a peer connection to Endpoint 1 and
    requests the data.
-#. Endpoint 1 sends the data to Endpoint 2.
-#. Endpoint 2 replies to Host B's request for the data with the data received
+5. Endpoint 1 sends the data to Endpoint 2.
+6. Endpoint 2 replies to Host B's request for the data with the data received
    from Endpoint 2. Host B deserializes the target object and the proxy
    is resolved.
 
-Hosting a Signaling Server
---------------------------
+## Hosting a Relay Server
 
-Currently, ProxyStore does not provided any publicly host signaling servers,
-though we hope to in the future! Hosting your own signaling server is simple
+Currently, ProxyStore does not provided any publicly host relay servers,
+though we hope to in the future! Hosting your own relay server is simple
 if you have a host accessible from the internet (e.g., a compute instance from
 a cloud provider or a machine behind a NAT with an open port) and the
 ProxyStore package installed.
 
-.. code-block:: bash
-
-   $ signaling-server --port 3579
+```bash
+$ proxystore-relay --port 3579
+```
```

### Comparing `proxystore-0.4.1a1/examples/README.md` & `proxystore-0.5.0/examples/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Example ProxyStore Apps
 
 Configure a new environment to try out the example apps.
 ```
-$ virtualenv venv
+$ python -m venv venv  # or $ virtualenv venv
 $ . venv/bin/activate
 $ pip install -r examples/requirements.txt
 ```
 
 Notes:
 - Most of the examples use Redis and require `redis-server` to
   be installed. See https://redis.io/docs/getting-started/ for more details.
```

### Comparing `proxystore-0.4.1a1/examples/funcx/README.md` & `proxystore-0.5.0/examples/globus-compute/README.md`

 * *Files 21% similar despite different names*

```diff
@@ -1,21 +1,25 @@
-# MapReduce with FuncX and ProxyStore
+# MapReduce with Globus Compute and ProxyStore
 
-Example of integrating ProxyStore into a FuncX app.
+> Globus Compute was formerly called funcX.
+> Learn about upgrading from funcX to Globus Compute
+> [here](https://globus-compute.readthedocs.io/en/latest/funcx_upgrade.html).
+
+Example of integrating ProxyStore into a Globus Compute app.
 
 ```
-$ python mapreduce_funcx.py -e $ENDPOINT -n 10 -s 100 --ps-redis --ps-redis-port $PORT
+$ python mapreduce_globus_compute.py -e $ENDPOINT -n 10 -s 100 --ps-redis --ps-redis-port $PORT
 $ ENDPOINT={endpoint} bash run.sh
 ```
 
 The example app supports three ProxyStore backends. If no option is specified,
 ProxyStore is not used.
 
 - **File**: `--ps-file --ps-file-dir /tmp/proxystore-dump`
 - **Globus**: `--ps-globus --ps-globus-config globus-endpoint-config.json`
 - **Redis**: `--ps-redis --ps-redis-port 1234`
 
-See the [API docs](https://proxystore.readthedocs.io/en/latest/source/api.html)
+See the [API docs](https://docs.proxystore.dev/main/api/connectors/)
 for more info on any of the specific backend types.
 
-To learn more about using FuncX, checkout the
-[Tutorial](https://funcx.readthedocs.io/en/latest/Tutorial.html).
+To learn more about using Globus Compute, checkout the
+[Quickstart](https://globus-compute.readthedocs.io/en/latest/quickstart.html).
```

### Comparing `proxystore-0.4.1a1/examples/funcx/mapreduce_funcx.py` & `proxystore-0.5.0/examples/globus-compute/mapreduce_globus_compute.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,56 +1,53 @@
-"""FuncX and ProxyStore example."""
+"""Globus Compute and ProxyStore example."""
 from __future__ import annotations
 
 import argparse
 import sys
 import time
 from typing import Any
 
 import numpy as np
-from funcx.sdk.executor import FuncXExecutor
+from globus_compute_sdk import Executor
 
+from proxystore.connectors.file import FileConnector
+from proxystore.connectors.globus import GlobusConnector
+from proxystore.connectors.globus import GlobusEndpoints
+from proxystore.connectors.redis import RedisConnector
 from proxystore.store import register_store
 from proxystore.store.base import Store
-from proxystore.store.file import FileStore
-from proxystore.store.globus import GlobusEndpoints
-from proxystore.store.globus import GlobusStore
-from proxystore.store.redis import RedisStore
 
-# Note: types on function are not provided because FuncX has trouble
-# serializing them sometimes
 
-
-def app_double(x):  # type: ignore
+def app_double(x: np.ndarray) -> np.ndarray:
     """Doubles input array."""
     return 2 * x
 
 
-def app_sum(inputs):  # type: ignore
+def app_sum(inputs: np.ndarray) -> np.ndarray:
     """Sum all elements in list of arrays."""
     import numpy as np
 
     if len(inputs) == 0:
         return 0
 
     out = inputs[0]
     for x in inputs[1:]:
         out += x
     return np.sum(out)
 
 
 if __name__ == '__main__':
     parser = argparse.ArgumentParser(
-        description='MapReduce with FuncX and ProxyStore',
+        description='MapReduce with Globus Compute and ProxyStore',
     )
     parser.add_argument(
         '-e',
         '--endpoint',
         required=True,
-        help='FuncX endpoint for task execution',
+        help='Globus Compute endpoint for task execution',
     )
     parser.add_argument(
         '-n',
         '--num-arrays',
         type=int,
         default=10,
         help='Number of arrays to be mapreduced',
@@ -90,53 +87,44 @@
         required='--ps-globus' in sys.argv,
         help='Globus Endpoint config file to use with ProxyStore.',
     )
     ps_group.add_argument(
         '--ps-redis-port',
         type=int,
         required='--ps-redis' in sys.argv,
-        help=(
-            'Redis server running on the localhost ' 'to use with ProxyStore '
-        ),
+        help='Redis server running on the localhost to use with ProxyStore',
     )
     args = parser.parse_args()
 
     store: Store[Any] | None = None
     if args.ps_file:
-        store = FileStore('file', store_dir=args.ps_file_dir)
+        store = Store('file', FileConnector(store_dir=args.ps_file_dir))
     elif args.ps_globus:
         endpoints = GlobusEndpoints.from_json(args.ps_globus_config)
-        store = GlobusStore('globus', endpoints=endpoints)
+        store = Store('globus', GlobusConnector(endpoints=endpoints))
     elif args.ps_redis:
-        store = RedisStore(
-            'redis',
-            hostname='localhost',
-            port=args.ps_redis_port,
-        )
+        store = Store('redis', RedisConnector('localhost', args.ps_redis_port))
 
     if store is not None:
         register_store(store)
 
     start = time.perf_counter()
 
-    with FuncXExecutor(endpoint_id=args.endpoint) as fxe:
+    with Executor(endpoint_id=args.endpoint) as gce:
         futures = []
         for _ in range(args.num_arrays):
             x = np.random.rand(args.size, args.size)
             if store is not None:
                 x = store.proxy(x)
-            futures.append(fxe.submit(app_double, x))
+            futures.append(gce.submit(app_double, x))
 
         mapped_results = [future.result() for future in futures]
 
         if store is not None:
             mapped_results = store.proxy(mapped_results)
-        total = fxe.submit(app_sum, mapped_results).result()
+        total = gce.submit(app_sum, mapped_results).result()
 
     print(f'Sum: {total}')
     print(f'Time: {time.perf_counter() - start:.2f}')
 
     if store is not None:
-        if hasattr(store, 'cleanup'):
-            store.cleanup()
-        elif hasattr(store, 'close'):
-            store.close()
+        store.close()
```

### Comparing `proxystore-0.4.1a1/examples/funcx/run.sh` & `proxystore-0.5.0/examples/globus-compute/run.sh`

 * *Files 21% similar despite different names*

```diff
@@ -5,20 +5,20 @@
 REDIS=$!
 
 ARRAY_COUNT=10
 ARRAY_SIZE=10
 
 echo "Started Redis on localhost:$PORT"
 
-echo "Running mapreduce_funcx.py without ProxyStore"
-python mapreduce_funcx.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE
+echo "Running mapreduce_globus_compute.py without ProxyStore"
+python mapreduce_globus_compute.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE
 
-echo "Running mapreduce_funcx.py with ProxyStore (File)"
-python mapreduce_funcx.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE \
+echo "Running mapreduce_globus_compute.py with ProxyStore (File)"
+python mapreduce_globus_compute.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE \
     --ps-file --ps-file-dir /tmp/proxystore-dump
 
-echo "Running mapreduce_funcx.py with ProxyStore (Redis)"
-python mapreduce_funcx.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE \
+echo "Running mapreduce_globus_compute.py with ProxyStore (Redis)"
+python mapreduce_globus_compute.py -e $ENDPOINT -n $ARRAY_SIZE -s $ARRAY_SIZE \
     --ps-redis --ps-redis-port $PORT
 
 echo "Stopping Redis"
 kill $REDIS
```

### Comparing `proxystore-0.4.1a1/examples/parsl/mapreduce_parsl.py` & `proxystore-0.5.0/examples/parsl/mapreduce_parsl.py`

 * *Files 6% similar despite different names*

```diff
@@ -4,18 +4,18 @@
 import argparse
 from typing import Any
 
 import numpy as np
 import parsl
 from parsl import python_app
 
+from proxystore.connectors.local import LocalConnector
+from proxystore.connectors.redis import RedisConnector
 from proxystore.store import register_store
 from proxystore.store.base import Store
-from proxystore.store.local import LocalStore
-from proxystore.store.redis import RedisStore
 
 
 @python_app
 def app_double(x: np.ndarray) -> np.ndarray:
     """Doubles input array."""
     return 2 * x
 
@@ -61,20 +61,19 @@
     args = parser.parse_args()
 
     parsl.load()
 
     if args.proxy:
         store: Store[Any]
         if args.redis_port is None:
-            store = LocalStore('local')
+            store = Store('local', LocalConnector())
         else:
-            store = RedisStore(
+            store = Store(
                 'redis',
-                hostname='localhost',
-                port=args.redis_port,
+                RedisConnector('localhost', args.redis_port),
             )
         register_store(store)
 
     mapped_results = []
     for _ in range(args.num_arrays):
         x = np.random.rand(args.size, args.size)
         if args.proxy:
```

### Comparing `proxystore-0.4.1a1/examples/parsl/run.sh` & `proxystore-0.5.0/examples/parsl/run.sh`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/commands.py` & `proxystore-0.5.0/proxystore/endpoint/commands.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,29 +1,31 @@
 """Endpoint management commands.
 
 These are the implementations of the commands available via the
-:any:`proxystore-endpoint <proxystore.endpoint.cli.main>` command.
+[`proxystore-endpoint`](../cli.md#proxystore-endpoint) command.
 Subsequently, all commands log errors and results and return status codes
 (rather than raising errors and returning results).
 """
 from __future__ import annotations
 
 import contextlib
 import enum
 import logging
 import os
 import shutil
 import signal
+import socket
 import uuid
 from typing import Generator
 
 import daemon.pidfile
 import psutil
 
 from proxystore import utils
+from proxystore.endpoint.config import ENDPOINT_DATABASE_FILE
 from proxystore.endpoint.config import EndpointConfig
 from proxystore.endpoint.config import get_configs
 from proxystore.endpoint.config import get_log_filepath
 from proxystore.endpoint.config import get_pid_filepath
 from proxystore.endpoint.config import read_config
 from proxystore.endpoint.config import write_config
 from proxystore.endpoint.serve import serve
@@ -49,29 +51,29 @@
     """
 
 
 def get_status(name: str, proxystore_dir: str | None = None) -> EndpointStatus:
     """Check status of endpoint.
 
     Args:
-        name (str): name of endpoint to check.
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
+        name: Name of endpoint to check.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
 
     Returns:
-        :py:attr:`.EndpointStatus.RUNNING` if the endpoint has a valid
-        directory and the PID file points to a running process.
-        :py:attr:`.EndpointStatus.STOPPED` if the endpoint has a valid
-        directory and no PID file.
-        :py:attr:`.EndpointStatus.UNKNOWN` if the endpoint directory is
-        missing or the config file is missing/unreadable.
-        :py:attr:`.EndpointStatus.HANGING` if the endpoint has a valid
-        directory but the PID file does not point to a running process. This
-        can be due to the endpoint process dying unexpectedly or the endpoint
-        process is on a different host.
+        `EndpointStatus.RUNNING` if the endpoint has a valid directory and \
+        the PID file points to a running process. \
+        `EndpointStatus.STOPPED` if the endpoint has a valid directory and no \
+        PID file. \
+        `EndpointStatus.UNKNOWN` if the endpoint directory is missing or the \
+        config file is missing/unreadable. \
+        `EndpointStatus.HANGING` if the endpoint has a valid directory but \
+        the PID file does not point to a running process. This can be due to \
+        the endpoint process dying unexpectedly or the endpoint process is on \
+        a different host.
     """
     if proxystore_dir is None:
         proxystore_dir = home_dir()
 
     endpoint_dir = os.path.join(proxystore_dir, name)
     if not os.path.isdir(endpoint_dir):
         return EndpointStatus.UNKNOWN
@@ -94,60 +96,59 @@
         return EndpointStatus.HANGING
 
 
 def configure_endpoint(
     name: str,
     *,
     port: int,
-    server: str | None,
+    relay_server: str | None,
     proxystore_dir: str | None = None,
-    max_memory: int | None = None,
-    dump_dir: str | None = None,
     peer_channels: int = 1,
+    persist_data: bool = False,
 ) -> int:
     """Configure a new endpoint.
 
     Args:
-        name (str): name of endpoint.
-        port (int): port for endpoint to listen on.
-        server (str): optional address of signaling server for P2P endpoint
-            connections.
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
-        max_memory (int): optional max memory in bytes to use for storing
-            objects. If exceeded, LRU objects will be dumped to `dump_dir`
-            (default: None).
-        dump_dir (str): optional directory to dump objects to if the
-            memory limit is exceeded (default: None).
-        peer_channels (int): number of datachannels per peer connection
-            to another endpoint to communicate over (default: 1).
+        name: Name of endpoint.
+        port: Port for endpoint to listen on.
+        relay_server: Optional relay server address for P2P endpoint connections.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
+        peer_channels: Number of datachannels per peer connection
+            to another endpoint to communicate over.
+        persist_data: Persist data stored in the endpoint.
 
     Returns:
-        Exit code where 0 is success and 1 is failure. Failure messages
+        Exit code where 0 is success and 1 is failure. Failure messages \
         are logged to the default logger.
     """
+    if proxystore_dir is None:
+        proxystore_dir = home_dir()
+    endpoint_dir = os.path.join(proxystore_dir, name)
+
+    database_path = (
+        os.path.join(endpoint_dir, ENDPOINT_DATABASE_FILE)
+        if persist_data
+        else None
+    )
+
     try:
         cfg = EndpointConfig(
             name=name,
             uuid=uuid.uuid4(),
             host=None,
             port=port,
-            server=server,
-            max_memory=max_memory,
-            dump_dir=dump_dir,
+            relay_server=relay_server,
+            database_path=database_path,
             peer_channels=peer_channels,
         )
     except ValueError as e:
         logger.error(str(e))
         return 1
 
-    if proxystore_dir is None:
-        proxystore_dir = home_dir()
-    endpoint_dir = os.path.join(proxystore_dir, name)
-
     if os.path.exists(endpoint_dir):
         logger.error(f'An endpoint named {name} already exists.')
         logger.info('To reconfigure the endpoint, remove and try again.')
         return 1
 
     write_config(cfg, endpoint_dir)
 
@@ -160,19 +161,19 @@
 def list_endpoints(
     *,
     proxystore_dir: str | None = None,
 ) -> int:
     """List available endpoints.
 
     Args:
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
 
     Returns:
-        Exit code where 0 is success and 1 is failure. Failure messages
+        Exit code where 0 is success and 1 is failure. Failure messages \
         are logged to the default logger.
     """
     if proxystore_dir is None:
         proxystore_dir = home_dir()
 
     endpoints = get_configs(proxystore_dir)
 
@@ -197,20 +198,20 @@
     name: str,
     *,
     proxystore_dir: str | None = None,
 ) -> int:
     """Remove endpoint.
 
     Args:
-        name (str): name of endpoint to remove.
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
+        name: Name of endpoint to remove.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
 
     Returns:
-        Exit code where 0 is success and 1 is failure. Failure messages
+        Exit code where 0 is success and 1 is failure. Failure messages \
         are logged to the default logger.
     """
     if proxystore_dir is None:
         proxystore_dir = home_dir()
     endpoint_dir = os.path.join(proxystore_dir, name)
 
     if not os.path.exists(endpoint_dir):
@@ -236,22 +237,22 @@
     detach: bool = False,
     log_level: str = 'INFO',
     proxystore_dir: str | None = None,
 ) -> int:
     """Start endpoint.
 
     Args:
-        name (str): name of endpoint to start.
-        detach (bool): start the endpoint as a daemon process.
-        log_level (str): set logging level of endpoint.
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
+        name: Name of endpoint to start.
+        detach: Start the endpoint as a daemon process.
+        log_level: Logging level of the endpoint.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
 
     Returns:
-        Exit code where 0 is success and 1 is failure. Failure messages
+        Exit code where 0 is success and 1 is failure. Failure messages \
         are logged to the default logger.
     """
     if proxystore_dir is None:
         proxystore_dir = home_dir()
 
     status = get_status(name, proxystore_dir)
     if status == EndpointStatus.RUNNING:
@@ -260,15 +261,16 @@
     elif status == EndpointStatus.UNKNOWN:
         logger.error(f'A valid endpoint named {name} does not exist.')
         logger.error('Use `list` to see available endpoints.')
         return 1
 
     endpoint_dir = os.path.join(proxystore_dir, name)
     cfg = read_config(endpoint_dir)
-    hostname = utils.hostname()
+    # Use IP address here which is generally more reliable
+    hostname = socket.gethostbyname(utils.hostname())
 
     pid_file = get_pid_filepath(endpoint_dir)
 
     if (
         status == EndpointStatus.HANGING
         and cfg.host is not None
         and hostname != cfg.host
@@ -311,20 +313,20 @@
     return 0
 
 
 def stop_endpoint(name: str, *, proxystore_dir: str | None = None) -> int:
     """Stop endpoint.
 
     Args:
-        name (str): name of endpoint to start.
-        proxystore_dir (str): optionally specify the proxystore home directory.
-            Defaults to :py:func:`~proxystore.utils.home_dir`.
+        name: Name of endpoint to start.
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
 
     Returns:
-        Exit code where 0 is success and 1 is failure. Failure messages
+        Exit code where 0 is success and 1 is failure. Failure messages \
         are logged to the default logger.
     """
     if proxystore_dir is None:
         proxystore_dir = home_dir()
 
     status = get_status(name, proxystore_dir)
     if status == EndpointStatus.UNKNOWN:
```

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/config.py` & `proxystore-0.5.0/proxystore/endpoint/config.py`

 * *Files 10% similar despite different names*

```diff
@@ -5,82 +5,94 @@
 import json
 import os
 import re
 import uuid
 
 from proxystore.endpoint.constants import MAX_OBJECT_SIZE_DEFAULT
 
-_ENDPOINT_CONFIG_FILE = 'endpoint.json'
-_ENDPOINT_LOG_FILE = 'endpoint.log'
-_ENDPOINT_PID_FILE = 'daemon.pid'
+ENDPOINT_CONFIG_FILE = 'config.json'
+ENDPOINT_DATABASE_FILE = 'blobs.db'
+ENDPOINT_LOG_FILE = 'log.txt'
+ENDPOINT_PID_FILE = 'daemon.pid'
 
 
 @dataclasses.dataclass
 class EndpointConfig:
-    """Endpoint configuration."""
+    """Endpoint configuration.
+
+    Attributes:
+        name: Endpoint name.
+        uuid: Endpoint UUID.
+        host: Host endpoint is running on.
+        port: Port endpoint is running on.
+        relay_server: Optional relay server the endpoint should register with.
+        database_path: Optional path to SQLite database file that will be used
+            for storing endpoint data. If `None`, data will only be stored
+            in-memory.
+        max_object_size: Optional maximum object size.
+        peer_channels: Number of peer channels to multiplex communications
+            over.
+        verify_certificates: Validate the SSL certificates of the `relay`
+            server.
+
+    Raises:
+        ValueError: If the name does not contain only alphanumeric, dash, or
+            underscore characters, if the UUID cannot be parsed, or if the
+            port is not in the range [1, 65535].
+    """
 
     name: str
     uuid: uuid.UUID
     host: str | None
     port: int
-    server: str | None = None
-    max_memory: int | None = None
+    relay_server: str | None = None
+    database_path: str | None = None
     max_object_size: int | None = MAX_OBJECT_SIZE_DEFAULT
-    dump_dir: str | None = None
     peer_channels: int = 1
     verify_certificate: bool = True
 
     def __post_init__(self) -> None:
-        """Validate config contains reasonable values.
-
-        Raises:
-            ValueError:
-                if the name does not contain only alphanumeric, dash, or
-                underscore characters, if the UUID cannot be parsed, or if the
-                port is not in the range [1, 65535].
-        """
         if not validate_name(self.name):
             raise ValueError(
                 'Name must only contain alphanumeric characters, dashes, and '
                 f' underscores. Got {self.name}.',
             )
         if isinstance(self.uuid, str):
             try:
                 self.uuid = uuid.UUID(self.uuid, version=4)
             except ValueError:
                 raise ValueError(
                     f'{self.uuid} is not a valid UUID4 string.',
                 ) from None
         if self.port < 1 or self.port > 65535:
             raise ValueError('Port must be in range [1, 65535].')
-        if self.server is not None and not (
-            self.server.startswith('ws://') or self.server.startswith('wss://')
+        if self.relay_server is not None and not (
+            self.relay_server.startswith('ws://')
+            or self.relay_server.startswith('wss://')
         ):
             raise ValueError(
                 'Server must start with ws:// or wss://.',
             )
-        if self.max_memory is not None and self.max_memory < 1:
-            raise ValueError('Max memory must be None or greater than zero.')
         if self.max_object_size is not None and self.max_object_size < 1:
             raise ValueError(
                 'Max object size must be None or greater than zero.',
             )
         if self.peer_channels < 1:
             raise ValueError('Peer channels must be >= 1.')
 
 
 def get_configs(proxystore_dir: str) -> list[EndpointConfig]:
     """Get all valid endpoint configurations in parent directory.
 
     Args:
-        proxystore_dir (str): parent directory containing possible endpoint
+        proxystore_dir: Parent directory containing possible endpoint
             configurations.
 
     Returns:
-        list of :class:`~proxystore.endpoint.config.EndpointConfig`.
+        List of found configs.
     """
     endpoints: list[EndpointConfig] = []
 
     if not os.path.isdir(proxystore_dir):
         return endpoints
 
     for dirpath, _, _ in os.walk(proxystore_dir):
@@ -98,50 +110,48 @@
     return endpoints
 
 
 def get_log_filepath(endpoint_dir: str) -> str:
     """Return path to log file for endpoint.
 
     Args:
-        endpoint_dir (str): directory for the endpoint.
+        endpoint_dir: Directory for the endpoint.
 
     Returns:
-        path to log file.
+        Path to log file.
     """
-    return os.path.join(endpoint_dir, _ENDPOINT_LOG_FILE)
+    return os.path.join(endpoint_dir, ENDPOINT_LOG_FILE)
 
 
 def get_pid_filepath(endpoint_dir: str) -> str:
     """Return path to PID file for endpoint.
 
     Args:
-        endpoint_dir (str): directory for the endpoint.
+        endpoint_dir: Directory for the endpoint.
 
     Returns:
-        path to PID file.
+        Path to PID file.
     """
-    return os.path.join(endpoint_dir, _ENDPOINT_PID_FILE)
+    return os.path.join(endpoint_dir, ENDPOINT_PID_FILE)
 
 
 def read_config(endpoint_dir: str) -> EndpointConfig:
     """Read endpoint config file.
 
     Args:
-        endpoint_dir (str): directory containing endpoint configuration file.
+        endpoint_dir: Directory containing endpoint configuration file.
 
     Returns:
-        :class:`<.EndpointConfig>`
+        Config found in `endpoint_dir`.
 
     Raises:
-        FileNotFoundError:
-            if a config files does not exist in the directory.
-        ValueError:
-            if config contains an invalid value or cannot be parsed.
+        FileNotFoundError: If a config files does not exist in the directory.
+        ValueError: If config contains an invalid value or cannot be parsed.
     """
-    path = os.path.join(endpoint_dir, _ENDPOINT_CONFIG_FILE)
+    path = os.path.join(endpoint_dir, ENDPOINT_CONFIG_FILE)
 
     if os.path.exists(path):
         with open(path) as f:
             try:
                 cfg_json = json.load(f)
             except json.decoder.JSONDecodeError as e:
                 raise ValueError(
@@ -166,18 +176,18 @@
     return len(re.findall(r'[^A-Za-z0-9_\-]', name)) == 0 and len(name) > 0
 
 
 def write_config(cfg: EndpointConfig, endpoint_dir: str) -> None:
     """Write config to endpoint directory.
 
     Args:
-        cfg (EndpointConfig): configuration to write.
-        endpoint_dir (str): directory to write config to.
+        cfg: Configuration to write.
+        endpoint_dir: Directory to write config to.
     """
     os.makedirs(endpoint_dir, exist_ok=True)
-    path = os.path.join(endpoint_dir, _ENDPOINT_CONFIG_FILE)
+    path = os.path.join(endpoint_dir, ENDPOINT_CONFIG_FILE)
     with open(path, 'w') as f:
         data = dataclasses.asdict(cfg)
         data['uuid'] = str(data['uuid'])
         json.dump(data, f, indent=4)
         # Add newline so cat on the file looks better
         f.write('\n')
```

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/endpoint.py` & `proxystore-0.5.0/proxystore/endpoint/endpoint.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,24 +7,27 @@
 from types import TracebackType
 from typing import Any
 from typing import Generator
 from uuid import UUID
 from uuid import uuid4
 
 from proxystore.endpoint.constants import MAX_OBJECT_SIZE_DEFAULT
+from proxystore.endpoint.exceptions import ObjectSizeExceededError
 from proxystore.endpoint.exceptions import PeeringNotAvailableError
 from proxystore.endpoint.exceptions import PeerRequestError
 from proxystore.endpoint.messages import EndpointRequest
-from proxystore.endpoint.storage import EndpointStorage
+from proxystore.endpoint.storage import DictStorage
+from proxystore.endpoint.storage import Storage
 from proxystore.p2p.connection import log_name
 from proxystore.p2p.manager import PeerManager
 from proxystore.p2p.task import spawn_guarded_background_task
 from proxystore.serialize import deserialize
 from proxystore.serialize import SerializationError
 from proxystore.serialize import serialize
+from proxystore.utils import bytes_to_readable
 
 logger = logging.getLogger(__name__)
 
 
 class EndpointMode(enum.Enum):
     """Endpoint mode."""
 
@@ -33,185 +36,175 @@
     SOLO = 2
     """Endpoint is operating in isolation and will ignore peer requests."""
 
 
 class Endpoint:
     """ProxyStore Endpoint.
 
-    An endpoint is an object store with
-    :func:`get() <Endpoint.get()>`/:func:`set() <Endpoint.set()>`
-    functionality.
+    An endpoint is an object store with `get`/`set` functionality.
 
-    By default, an endpoint operates in :py:attr:`SOLO <.EndpointMode.SOLO>`
+    By default, an endpoint operates in
+    [`EndpointMode.SOLO`][proxystore.endpoint.endpoint.EndpointMode.SOLO]
     mode where the endpoint acts just as an isolated object store. Endpoints
-    can also be configured in :py:attr:`PEERING <.EndpointMode.PEERING>` mode
-    by initializing the endpoint with a signaling server address.
-    The signaling server is used to establish peer-to-peer connections with
+    can also be configured in
+    [`EndpointMode.PEERING`][proxystore.endpoint.endpoint.EndpointMode.PEERING]
+    mode by initializing the endpoint with a relay server address.
+    The relay server is used to establish peer-to-peer connections with
     other endpoints after which endpoints can forward operations between each
     other. Peering is available even when endpoints are being separate
-    NATs. See the :py:mod:`proxystore.p2p <proxystore.p2p>` module to learn
-    more about peering.
+    NATs. See the [proxystore.p2p][] module to learn more about peering.
 
     Warning:
         Requests made to remote endpoints will only invoke the request on
         the remote and return the result. I.e., invoking GET on a remote
         will return the value but will not store it on the local endpoint.
 
-    **Solo Mode Usage**
+    Example:
+        Solo Mode Usage
 
-        >>> async with Endpoint('ep1', uuid.uuid4()) as endpoint:
-        >>>     serialized_data = b'data string'
-        >>>     endpoint.set('key', serialized_data)
-        >>>     assert endpoint.get('key') == serialized_data
-        >>>     endpoint.evict('key')
-        >>>     assert not endpoint.exists('key')
-
-    **Peering Mode Usage**
-
-        >>> ep1 = await Endpoint('ep1', uuid.uuid4(), signaling_server)
-        >>> ep2 = await Endpoint('ep1', uuid.uuid4(), signaling_server)
-        >>>
-        >>> serialized_data = b'data string'
-        >>> ep1.set('key', serialized_data)
-        >>> assert ep2.get('key', endpoint=ep1.uuid) == serialized_data
-        >>> assert ep1.exists('key')
-        >>> assert not ep1.exists('key', endpoint=ep2.uuid)
-        >>>
-        >>> ep1.close()
-        >>> ep2.close()
+        ```python
+        async with Endpoint('ep1', uuid.uuid4()) as endpoint:
+            serialized_data = b'data string'
+            endpoint.set('key', serialized_data)
+            assert endpoint.get('key') == serialized_data
+            endpoint.evict('key')
+            assert not endpoint.exists('key')
+        ```
+
+    Example:
+        Peering Mode Usage
+
+        ```python
+        ep1 = await Endpoint('ep1', uuid.uuid4(), relay_server)
+        ep2 = await Endpoint('ep1', uuid.uuid4(), relay_server)
+
+        serialized_data = b'data string'
+        ep1.set('key', serialized_data)
+        assert ep2.get('key', endpoint=ep1.uuid) == serialized_data
+        assert ep1.exists('key')
+        assert not ep1.exists('key', endpoint=ep2.uuid)
+
+        ep1.close()
+        ep2.close()
+        ```
 
     Note:
         Endpoints can be configured and started via the
-        :code:`proxystore-endpoint` command-line interface.
+        `proxystore-endpoint` command-line interface.
+
+
+    Note:
+        If the endpoint is being used in peering mode, the endpoint should be
+        used as a context manager or initialized with await. This will ensure
+        [`Endpoint.async_init()`][proxystore.endpoint.endpoint.Endpoint.async_init]
+        is executed which connects to the relay server and established a
+        listener for incoming messages.
+
+        ```python
+        endpoint = await Endpoint(...)
+        endpoint.close()
+        ```
+
+        ```python
+        async with Endpoint(...) as endpoint:
+            ...
+        ```
+
+    Args:
+        name: Readable name of endpoint.
+        uuid: UUID of the endpoint.
+        relay_server: Address of relay server used for peer-to-peer
+            connections between endpoints. If None, endpoint will not be able
+            to communicate with other endpoints.
+        max_object_size: Optional max size in bytes for any single
+            object stored by the endpoint. If exceeded, an error is raised.
+        peer_channels: Number of datachannels per peer connection
+            to another endpoint to communicate over.
+        peer_timeout: Timeout for establishing p2p connection with
+            another endpoint.
+        storage: Storage interface to use. If `None`,
+            [`DictStorage`][proxystore.endpoint.storage.DictStorage] is used.
+        verify_certificate: Verify the relay server's SSL
+            certificate. This should almost never be disabled except for
+            testing with self-signed certificates.
     """
 
     def __init__(
         self,
         name: str,
         uuid: UUID,
-        signaling_server: str | None = None,
-        peer_timeout: int = 30,
-        max_memory: int | None = None,
+        relay_server: str | None = None,
+        *,
         max_object_size: int | None = MAX_OBJECT_SIZE_DEFAULT,
-        dump_dir: str | None = None,
         peer_channels: int = 1,
+        peer_timeout: int = 30,
+        storage: Storage | None = None,
         verify_certificate: bool = True,
     ) -> None:
-        """Init Endpoint.
-
-        Note:
-            If the endpoint is being used in peering mode, the endpoint should
-            be used as a context manager or initialized with await. This will
-            ensure :func:`async_init <Endpoint.async_init>` is executed which
-            connects to the signaling server and established a listener for
-            incoming messages.
-
-            >>> endpoint = await Endpoint(...)
-            >>> endpoint.close()
-            >>>
-            >>> async with Endpoint(...) as endpoint:
-            >>>     ...
-
-        Args:
-            name (str): readable name of endpoint.
-            uuid (str): uuid of the endpoint.
-            signaling_server (str, optional): address of signaling
-                server used for peer-to-peer connections between endpoints. If
-                None, endpoint will not be able to communicate with other
-                endpoints (default: None).
-            peer_timeout (int): timeout for establishing p2p connection with
-                another endpoint (default: 30).
-            max_memory (int): optional max memory in bytes to use for storing
-                objects. If exceeded, LRU objects will be dumped to `dump_dir`
-                (default: None).
-            max_object_size (int): optional max size in bytes for any single
-                object stored by the endpoint. If exceeded, an error is
-                raised (default: 1 GB).
-            dump_dir (str): optional directory to dump objects to if the
-                memory limit is exceeded (default: None).
-            peer_channels (int): number of datachannels per peer connection
-                to another endpoint to communicate over (default: 1).
-            verify_certificate (bool): verify the signaling server's SSL
-                certificate. This should almost never be disabled except for
-                testing with self-signed certificates (default: True).
-        """
-        # TODO(gpauloski): need to consider semantics of operations
-        #   - can all ops be triggered on remote?
-        #   - or just get? do we move data permanently on get? etc...
         self._name = name
         self._uuid = uuid
-        self._signaling_server = signaling_server
-        self._peer_timeout = peer_timeout
+        self._relay_server = relay_server
+        self._max_object_size = max_object_size
         self._peer_channels = peer_channels
+        self._peer_timeout = peer_timeout
         self._verify_certificate = verify_certificate
 
+        self._storage = DictStorage() if storage is None else storage
+
         self._mode = (
-            EndpointMode.SOLO
-            if signaling_server is None
-            else EndpointMode.PEERING
+            EndpointMode.SOLO if relay_server is None else EndpointMode.PEERING
         )
-
         self._peer_manager: PeerManager | None = None
-
-        self._data = EndpointStorage(
-            max_size=max_memory,
-            max_object_size=max_object_size,
-            dump_dir=dump_dir,
-        )
         self._pending_requests: dict[
             str,
             asyncio.Future[EndpointRequest],
         ] = {}
-
         self._async_init_done = False
         self._peer_handler_task: asyncio.Task[None] | None = None
 
         logger.info(
             f'{self._log_prefix}: initialized endpoint operating '
             f'in {self._mode.name} mode',
         )
 
     @property
     def _log_prefix(self) -> str:
         return f'{type(self).__name__}[{log_name(self.uuid, self.name)}]'
 
     @property
     def uuid(self) -> UUID:
-        """Get UUID of this endpoint."""
+        """UUID of this endpoint."""
         return self._uuid
 
     @property
     def name(self) -> str:
-        """Get name of this endpoint."""
+        """Name of this endpoint."""
         return self._name
 
     async def __aenter__(self) -> Endpoint:
-        """Enter async context manager."""
         await self.async_init()
         return self
 
     async def __aexit__(
         self,
         exc_type: type[BaseException] | None,
         exc_value: BaseException | None,
         exc_traceback: TracebackType | None,
     ) -> None:
-        """Exit async context manager."""
         await self.close()
 
     def __await__(self) -> Generator[Any, None, Endpoint]:
-        """Initialize endpoint awaitables."""
         return self.__aenter__().__await__()
 
     async def async_init(self) -> None:
         """Initialize connections and tasks necessary for peering."""
-        if self._signaling_server is not None and not self._async_init_done:
+        if self._relay_server is not None and not self._async_init_done:
             self._peer_manager = await PeerManager(
                 uuid=self.uuid,
-                signaling_server=self._signaling_server,
+                relay_server=self._relay_server,
                 name=self.name,
                 timeout=self._peer_timeout,
                 peer_channels=self._peer_channels,
                 verify_certificate=self._verify_certificate,
             )
             self._peer_handler_task = spawn_guarded_background_task(
                 self._handle_peer_requests,
@@ -328,22 +321,21 @@
         else:
             return True
 
     async def evict(self, key: str, endpoint: UUID | None = None) -> None:
         """Evict key from endpoint.
 
         Args:
-            key (str): key to evict.
-            endpoint (optional, UUID): endpoint to perform operation on. If
+            key: Key to evict.
+            endpoint: Endpoint to perform operation on. If
                 unspecified or if the endpoint is on solo mode, the operation
                 will be performed on the local endpoint.
 
         Raises:
-            PeerRequestError:
-                if request to a peer endpoint fails.
+            PeerRequestError: If request to a peer endpoint fails.
         """
         logger.debug(
             f'{self._log_prefix}: EVICT key={key} on endpoint={endpoint}',
         )
         if self._is_peer_request(endpoint):
             assert endpoint is not None
             request = EndpointRequest(
@@ -351,32 +343,30 @@
                 op='evict',
                 uuid=str(uuid4()),
                 key=key,
             )
             request_future = await self._request_from_peer(endpoint, request)
             await request_future
         else:
-            if key in self._data:
-                del self._data[key]
+            await self._storage.evict(key)
 
     async def exists(self, key: str, endpoint: UUID | None = None) -> bool:
         """Check if key exists on endpoint.
 
         Args:
-            key (str): key to check.
-            endpoint (optional, UUID): endpoint to perform operation on. If
+            key: Key to check.
+            endpoint: Endpoint to perform operation on. If
                 unspecified or if the endpoint is on solo mode, the operation
                 will be performed on the local endpoint.
 
         Returns:
-            True if key exists.
+            If the key exists.
 
         Raises:
-            PeerRequestError:
-                if request to a peer endpoint fails.
+            PeerRequestError: If request to a peer endpoint fails.
         """
         logger.debug(
             f'{self._log_prefix}: EXISTS key={key} on endpoint={endpoint}',
         )
         if self._is_peer_request(endpoint):
             assert endpoint is not None
             request = EndpointRequest(
@@ -386,35 +376,34 @@
                 key=key,
             )
             request_future = await self._request_from_peer(endpoint, request)
             response = await request_future
             assert isinstance(response.exists, bool)
             return response.exists
         else:
-            return key in self._data
+            return await self._storage.exists(key)
 
     async def get(
         self,
         key: str,
         endpoint: UUID | None = None,
     ) -> bytes | None:
         """Get value associated with key on endpoint.
 
         Args:
-            key (str): key to get value for.
-            endpoint (optional, UUID): endpoint to perform operation on. If
+            key: Key to get value for.
+            endpoint: Endpoint to perform operation on. If
                 unspecified or if the endpoint is on solo mode, the operation
                 will be performed on the local endpoint.
 
         Returns:
-            value (bytes) associated with key.
+            Value associated with key.
 
         Raises:
-            PeerRequestError:
-                if request to a peer endpoint fails.
+            PeerRequestError: If request to a peer endpoint fails.
         """
         logger.debug(
             f'{self._log_prefix}: GET key={key} on endpoint={endpoint}',
         )
         if self._is_peer_request(endpoint):
             assert endpoint is not None
             request = EndpointRequest(
@@ -423,63 +412,68 @@
                 uuid=str(uuid4()),
                 key=key,
             )
             request_future = await self._request_from_peer(endpoint, request)
             response = await request_future
             return response.data
         else:
-            if key in self._data:
-                return self._data[key]
-            else:
-                return None
+            return await self._storage.get(key, None)
 
     async def set(
         self,
         key: str,
         data: bytes,
         endpoint: UUID | None = None,
     ) -> None:
         """Set key with data on endpoint.
 
         Args:
-            key (str): key to associate with value.
-            data (bytes): value to associate with key.
-            endpoint (optional, UUID): endpoint to perform operation on. If
+            key: Key to associate with value.
+            data: Value to associate with key.
+            endpoint: Endpoint to perform operation on. If
                 unspecified or if the endpoint is on solo mode, the operation
                 will be performed on the local endpoint.
 
         Raises:
-            ObjectSizeExceededError:
-                if the max object size is configured and the data exceeds that
-                size.
-            PeerRequestError:
-                if request to a peer endpoint fails.
+            ObjectSizeExceededError: If the max object size is configured and
+                the data exceeds that size.
+            PeerRequestError: If request to a peer endpoint fails.
         """
         logger.debug(
             f'{self._log_prefix}: SET key={key} on endpoint={endpoint}',
         )
+
         if self._is_peer_request(endpoint):
             assert endpoint is not None
             request = EndpointRequest(
                 kind='request',
                 op='set',
                 uuid=str(uuid4()),
                 key=key,
                 data=data,
             )
             request_future = await self._request_from_peer(endpoint, request)
             await request_future
+        elif (
+            self._max_object_size is not None
+            and len(data) > self._max_object_size
+        ):
+            raise ObjectSizeExceededError(
+                f'Bytes value has size {bytes_to_readable(len(data))} which '
+                f'exceeds the {bytes_to_readable(self._max_object_size)} '
+                'object limit.',
+            )
         else:
-            self._data[key] = data
+            await self._storage.set(key, data)
 
     async def close(self) -> None:
         """Close the endpoint and any open connections safely."""
         if self._peer_handler_task is not None:
             self._peer_handler_task.cancel()
             try:
                 await self._peer_handler_task
             except asyncio.CancelledError:
                 pass
         if self._peer_manager is not None:
             await self._peer_manager.close()
-        self._data.cleanup()
-        logger.info(f'{self._log_prefix}: endpoint close')
+        await self._storage.close()
+        logger.info(f'{self._log_prefix}: endpoint closed')
```

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/exceptions.py` & `proxystore-0.5.0/proxystore/endpoint/exceptions.py`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/serve.py` & `proxystore-0.5.0/proxystore/endpoint/serve.py`

 * *Files 7% similar despite different names*

```diff
@@ -5,16 +5,16 @@
 import dataclasses
 import json
 import logging
 import os
 import uuid
 
 try:
-    import hypercorn
     import quart
+    import uvicorn
     import uvloop
     from quart import request
     from quart import Response
 except ImportError as e:  # pragma: no cover
     # Usually we would just print a warning, but this file requires
     # quart to be available to register functions to a top-level blueprint.
     raise ImportError(
@@ -22,14 +22,15 @@
         '"pip install proxystore[endpoints]".',
     ) from e
 
 from proxystore.endpoint.config import EndpointConfig
 from proxystore.endpoint.constants import MAX_CHUNK_LENGTH
 from proxystore.endpoint.endpoint import Endpoint
 from proxystore.endpoint.exceptions import PeerRequestError
+from proxystore.endpoint.storage import SQLiteStorage
 from proxystore.utils import chunk_bytes
 
 logger = logging.getLogger(__name__)
 
 routes_blueprint = quart.Blueprint('routes', __name__)
 
 
@@ -37,31 +38,30 @@
     endpoint: Endpoint,
     max_content_length: int | None = None,
     body_timeout: int = 300,
 ) -> quart.Quart:
     """Create quart app for endpoint and registers routes.
 
     Args:
-        endpoint (Endpoint): initialized endpoint to forward quart routes to.
-        max_content_length (int): max request body size in bytes
-            (default: None).
-        body_timeout (int): number of seconds to wait for the body to be
-            completely received (default: 300)
+        endpoint: Initialized endpoint to forward quart routes to.
+        max_content_length: Max request body size in bytes.
+        body_timeout: Number of seconds to wait for the body to be
+            completely received.
 
     Returns:
         Quart app.
     """
     app = quart.Quart(__name__)
 
     app.config['endpoint'] = endpoint
 
     app.register_blueprint(routes_blueprint, url_prefix='')
 
     logger.info(
-        'quart routes registered to endpoint '
+        'Quart routes registered to endpoint '
         f'{endpoint.uuid} ({endpoint.name})',
     )
 
     app.config['MAX_CONTENT_LENGTH'] = max_content_length
     app.config['BODY_TIMEOUT'] = body_timeout
 
     return app
@@ -76,19 +76,18 @@
 ) -> None:
     """Initialize endpoint and serve Quart app.
 
     Warning:
         This function does not return until the Quart app is terminated.
 
     Args:
-        config (EndpointConfig): configuration object.
-        log_level (int): logging level of endpoint (default: INFO).
-        log_file (str): optional file path to append log to.
-        use_uvloop (bool): install uvloop as the default event loop
-            implementation (default: True).
+        config: Configuration object.
+        log_level: Logging level of endpoint.
+        log_file: Optional file path to append log to.
+        use_uvloop: Install uvloop as the default event loop implementation.
     """
     if config.host is None:
         raise ValueError('EndpointConfig has NoneType as host.')
 
     if log_file is not None:
         parent_dir = os.path.dirname(log_file)
         if not os.path.isdir(parent_dir):
@@ -106,36 +105,55 @@
     logging.getLogger().setLevel(log_level)
 
     kwargs = dataclasses.asdict(config)
     # These are the only two EndpointConfig attributes not passed to the
     # Endpoint constructor
     kwargs.pop('host', None)
     kwargs.pop('port', None)
-    # Backwards compatibility hack because EndpointConfig and Endpoint call
-    # the signaling server fields differently
-    kwargs['signaling_server'] = kwargs.pop('server')
 
-    endpoint = Endpoint(**kwargs)
-    app = create_app(endpoint)
+    database_path = kwargs.pop('database_path', None)
+    storage: SQLiteStorage | None
+    if database_path is not None:
+        logger.info(
+            f'Using SQLite database for storage (path: {database_path})',
+        )
+        storage = SQLiteStorage(database_path)
+    else:
+        logger.warning(
+            'Database path not provided. Data will not be persisted',
+        )
+        storage = None
 
-    serve_config = hypercorn.config.Config()
-    serve_config.bind = [f'{config.host}:{config.port}']
-    serve_config.accesslog = logging.getLogger('hypercorn.access')
-    serve_config.errorlog = logging.getLogger('hypercorn.error')
+    endpoint = Endpoint(**kwargs, storage=storage)
+    app = create_app(endpoint)
 
     if use_uvloop:  # pragma: no cover
-        logger.debug('installing uvloop as default event loop')
+        logger.info('Installing uvloop as default event loop')
         uvloop.install()
+    else:
+        logger.warning(
+            'Not installing uvloop. Uvicorn may override and install anyways',
+        )
+
+    server_config = uvicorn.Config(
+        app,
+        host=config.host,
+        port=config.port,
+        log_config=None,
+        log_level=logger.level,
+        access_log=False,
+    )
+    server = uvicorn.Server(server_config)
 
     logger.info(
-        f'serving endpoint {endpoint.uuid} ({endpoint.name}) on '
+        f'Serving endpoint {endpoint.uuid} ({endpoint.name}) on '
         f'{config.host}:{config.port}',
     )
-    logger.info(f'config: {config}')
-    asyncio.run(hypercorn.asyncio.serve(app, serve_config))
+    logger.info(f'Config: {config}')
+    asyncio.run(server.serve())
 
 
 @routes_blueprint.before_app_serving
 async def _startup() -> None:
     endpoint = quart.current_app.config['endpoint']
     await endpoint.async_init()
```

### Comparing `proxystore-0.4.1a1/proxystore/endpoint/storage.py` & `proxystore-0.5.0/proxystore/connectors/endpoint.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,247 +1,277 @@
-"""Storage interface for blobs."""
+"""Endpoint connector implementation."""
 from __future__ import annotations
 
-import collections
-import enum
-import os
-import shutil
+import logging
 import sys
-from typing import Deque
-from typing import Iterator
+import uuid
+from types import TracebackType
+from typing import Any
+from typing import NamedTuple
+from typing import Sequence
+from uuid import UUID
 
-if sys.version_info >= (3, 9):  # pragma: >=3.9 cover
-    from collections.abc import MutableMapping
-else:  # pragma: <3.9 cover
-    from typing import MutableMapping
+if sys.version_info >= (3, 11):  # pragma: >=3.11 cover
+    from typing import Self
+else:  # pragma: <3.11 cover
+    from typing_extensions import Self
 
-from proxystore.endpoint.exceptions import FileDumpNotAvailableError
-from proxystore.endpoint.exceptions import ObjectSizeExceededError
-from proxystore.utils import bytes_to_readable
+import requests
 
+from proxystore.endpoint import client
+from proxystore.endpoint.config import EndpointConfig
+from proxystore.endpoint.config import get_configs
+from proxystore.utils import home_dir
 
-class BlobLocation(enum.Enum):
-    """Location of Blob."""
+logger = logging.getLogger(__name__)
 
-    MEMORY = 1
-    """Blob is loaded in memory."""
-    FILE = 2
-    """Blob is stored on disk."""
 
+class EndpointConnectorError(Exception):
+    """Exception resulting from request to Endpoint."""
 
-class Blob:
-    """Representation of entry in :class:`.EndpointStorage`."""
+    pass
+
+
+class EndpointKey(NamedTuple):
+    """Key to object in an Endpoint.
+
+    Attributes:
+        object_id: Unique object ID.
+        endpoint_id: Endpoint UUID where object is stored.
+    """
+
+    object_id: str
+    endpoint_id: str | None
+
+
+class EndpointConnector:
+    """Connector to ProxyStore Endpoints.
+
+    Warning:
+        Specifying a custom `proxystore_dir` can cause problems if the
+        `proxystore_dir` is not the same on all systems that a proxy
+        created by this store could end up on. It is recommended to leave
+        the `proxystore_dir` unspecified so the correct default directory
+        will be used.
+
+    Args:
+        endpoints: Sequence of valid and running endpoint
+            UUIDs to use. At least one of these endpoints must be
+            accessible by this process.
+        proxystore_dir: Optionally specify the proxystore home
+            directory. Defaults to [`home_dir()`][proxystore.utils.home_dir].
+
+    Raises:
+        ValueError: If endpoints is an empty list.
+        EndpointConnectorError: If unable to connect to one of the endpoints
+            provided.
+    """
 
     def __init__(
         self,
-        key: str,
-        value: bytes,
-        filepath: str | None = None,
+        endpoints: Sequence[str | UUID],
+        proxystore_dir: str | None = None,
     ) -> None:
-        """Init Blob.
+        if len(endpoints) == 0:
+            raise ValueError('At least one endpoint must be specified.')
+        self.endpoints: list[UUID] = [
+            e if isinstance(e, UUID) else UUID(e, version=4) for e in endpoints
+        ]
+        self.proxystore_dir = proxystore_dir
+
+        # Maintain single session for connection pooling persistence to
+        # speed up repeat requests to same endpoint.
+        self._session = requests.Session()
+
+        # Find the first locally accessible endpoint to use as our
+        # home endpoint
+        available_endpoints = get_configs(
+            home_dir() if self.proxystore_dir is None else self.proxystore_dir,
+        )
+        found_endpoint: EndpointConfig | None = None
+        for endpoint in available_endpoints:
+            if endpoint.uuid in self.endpoints:
+                logger.debug(f'Attempting connection to {endpoint.uuid}')
+                response = self._session.get(
+                    f'http://{endpoint.host}:{endpoint.port}/endpoint',
+                )
+                if response.status_code == 200:
+                    uuid = response.json()['uuid']
+                    if str(endpoint.uuid) == uuid:
+                        logger.debug(
+                            f'Connection to {endpoint.uuid} successful, using '
+                            'as local endpoint',
+                        )
+                        found_endpoint = endpoint
+                        break
+                    else:
+                        logger.debug(
+                            f'Connection to {endpoint.uuid} returned '
+                            'different UUID',
+                        )
+                else:
+                    logger.debug(f'Connection to {endpoint.uuid} failed')
+
+        if found_endpoint is None:
+            self._session.close()
+            raise EndpointConnectorError(
+                'Failed to find endpoint configuration matching one of the '
+                'provided endpoint UUIDs.',
+            )
+        self.endpoint_uuid = found_endpoint.uuid
+        self.endpoint_host = found_endpoint.host
+        self.endpoint_port = found_endpoint.port
 
-        Args:
-            key (str): key associated with the blob.
-            value (bytes): the blob being stored.
-            filepath (str): optional filepath for dumping the blob.
-        """
-        self.key = key
-        self.size = len(value)
-        self._value: bytes | None = value
-        self.filepath = filepath
+        self.address = f'http://{self.endpoint_host}:{self.endpoint_port}'
+
+    def __enter__(self) -> Self:
+        return self
 
-    @property
-    def location(self) -> BlobLocation:
-        """Get the location of the blob."""
+    def __exit__(
+        self,
+        exc_type: type[BaseException] | None,
+        exc_value: BaseException | None,
+        exc_traceback: TracebackType | None,
+    ) -> None:
+        self.close()
+
+    def __repr__(self) -> str:
         return (
-            BlobLocation.FILE if self._value is None else BlobLocation.MEMORY
+            f'{self.__class__.__name__}(connected to {self.endpoint_uuid} '
+            f'@ {self.address})'
         )
 
-    @property
-    def value(self) -> bytes:
-        """Get the blob bytes."""
-        if self._value is None:
-            self.load()
-        assert self._value is not None
-        return self._value
-
-    def delete_file(self) -> None:
-        """Delete the file dump of the blob if it exists."""
-        if self.filepath is not None and os.path.isfile(self.filepath):
-            os.remove(self.filepath)
-
-    def dump(self) -> None:
-        """Dump the blob to disk."""
-        if self.filepath is None:
-            raise FileDumpNotAvailableError(
-                'The blob was not initialized with a filepath '
-                'to dump data to.',
-            )
-        assert self._value is not None
-        with open(self.filepath, 'wb') as f:
-            f.write(self._value)
-        self._value = None
-
-    def load(self) -> None:
-        """Load the blob from disk."""
-        if self._value is not None:
-            return
-
-        assert self.filepath is not None
-        with open(self.filepath, 'rb') as f:
-            self._value = f.read()
-        self.delete_file()
-
-
-class EndpointStorage(MutableMapping[str, bytes]):
-    """Endpoint in-memory blob storage with filesystem fallback.
-
-    The :class:`.EndpointStorage` provides a dict-like storage of key-bytes
-    pairs. Optionally, a maximum in-memory size for the data structure can
-    be specified and least-recently used key-bytes pairs will be dumped
-    to a file in a specified directory.
-    """
+    def close(self) -> None:
+        """Close the connector and clean up."""
+        self._session.close()
 
-    def __init__(
-        self,
-        max_size: int | None = None,
-        max_object_size: int | None = None,
-        dump_dir: str | None = None,
-    ) -> None:
-        """Init EndpointStorage.
+    def config(self) -> dict[str, Any]:
+        """Get the connector configuration.
+
+        The configuration contains all the information needed to reconstruct
+        the connector object.
+        """
+        return {
+            'endpoints': [str(ep) for ep in self.endpoints],
+            'proxystore_dir': self.proxystore_dir,
+        }
+
+    @classmethod
+    def from_config(cls, config: dict[str, Any]) -> EndpointConnector:
+        """Create a new connector instance from a configuration.
+
+        Args:
+            config: Configuration returned by `#!python .config()`.
+        """
+        return cls(**config)
+
+    def evict(self, key: EndpointKey) -> None:
+        """Evict the object associated with the key.
 
         Args:
-            max_size (int): optional maximum size in bytes for in-memory
-                storage of blobs. If the memory limit is exceeded, least
-                recently used blobs will be dumped to disk (if configured).
-            max_object_size (int): optional maximum size in bytes for any
-                single blob.
-            dump_dir (str): optional directory to dump blobs to when
-                `max_size` is reached.
-        """
-        if (max_size is not None or dump_dir is not None) and (
-            max_size is None or dump_dir is None
-        ):
-            raise ValueError(
-                'Either both of max_size and dump_dir should be specified '
-                'or neither.',
+            key: Key associated with object to evict.
+        """
+        try:
+            client.evict(
+                self.address,
+                key.object_id,
+                key.endpoint_id,
+                session=self._session,
             )
-        self.max_size = max_size
-        self.max_object_size = max_object_size
-        self.dump_dir = dump_dir
-
-        if self.dump_dir is not None:
-            os.makedirs(self.dump_dir, exist_ok=True)
-
-        self._in_memory_size = 0
-        self._blobs: dict[str, Blob] = {}
-
-        # Only in-memory objects should be in this.
-        # Recently used keys are appended to right side, LRU keys are
-        # popped from left side.
-        self._lru_queue: Deque[str] = collections.deque()
-
-    def __getitem__(self, key: str) -> bytes:
-        """Get bytes associated with key."""
-        if key not in self._blobs:
-            raise KeyError(key)
-
-        blob = self._blobs[key]
-
-        if blob.location == BlobLocation.MEMORY:
-            # Move to right side because recently used
-            self._lru_queue.remove(key)
-            self._lru_queue.append(key)
-            return blob.value
-
-        self._make_space(blob.size)
-        self._in_memory_size += blob.size
-        blob.load()
-
-        # Add to queue because it is back in memory
-        self._lru_queue.append(key)
-
-        return blob.value
-
-    def __setitem__(self, key: str, value: bytes) -> None:
-        """Set key to value (bytes).
-
-        Raises:
-            ValueError:
-                if `value` is larger than `max_size`.
-        """
-        if (
-            self.max_object_size is not None
-            and len(value) > self.max_object_size
-        ):
-            raise ObjectSizeExceededError(
-                f'Bytes value has size {bytes_to_readable(len(value))} which '
-                f'exceeds the {bytes_to_readable(self.max_object_size)} '
-                'object limit.',
+        except requests.exceptions.RequestException as e:
+            raise EndpointConnectorError(
+                f'Evict failed with error code {e.response.status_code}.',
+            ) from e
+
+    def exists(self, key: EndpointKey) -> bool:
+        """Check if an object associated with the key exists.
+
+        Args:
+            key: Key potentially associated with stored object.
+
+        Returns:
+            If an object associated with the key exists.
+        """
+        try:
+            return client.exists(
+                self.address,
+                key.object_id,
+                key.endpoint_id,
+                session=self._session,
             )
-        if self.max_size is not None and len(value) > self.max_size:
-            raise ObjectSizeExceededError(
-                f'Bytes value has size {bytes_to_readable(len(value))} which '
-                f'exceeds the {bytes_to_readable(self.max_size)} '
-                'memory limit.',
+        except requests.exceptions.RequestException as e:
+            raise EndpointConnectorError(
+                f'Exists failed with error code {e.response.status_code}.',
+            ) from e
+
+    def get(self, key: EndpointKey) -> bytes | None:
+        """Get the serialized object associated with the key.
+
+        Args:
+            key: Key associated with the object to retrieve.
+
+        Returns:
+            Serialized object or `None` if the object does not exist.
+        """
+        try:
+            return client.get(
+                self.address,
+                key.object_id,
+                key.endpoint_id,
+                session=self._session,
             )
-        filepath = (
-            None if self.dump_dir is None else os.path.join(self.dump_dir, key)
+        except requests.exceptions.RequestException as e:
+            raise EndpointConnectorError(
+                f'Get failed with error code {e.response.status_code}.',
+            ) from e
+
+    def get_batch(self, keys: Sequence[EndpointKey]) -> list[bytes | None]:
+        """Get a batch of serialized objects associated with the keys.
+
+        Args:
+            keys: Sequence of keys associated with objects to retrieve.
+
+        Returns:
+            List with same order as `keys` with the serialized objects or \
+            `None` if the corresponding key does not have an associated object.
+        """
+        return [self.get(key) for key in keys]
+
+    def put(self, obj: bytes) -> EndpointKey:
+        """Put a serialized object in the store.
+
+        Args:
+            obj: Serialized object to put in the store.
+
+        Returns:
+            Key which can be used to retrieve the object.
+        """
+        key = EndpointKey(
+            object_id=str(uuid.uuid4()),
+            endpoint_id=str(self.endpoint_uuid),
         )
-        blob = Blob(key, value, filepath)
-        self._make_space(blob.size)
-        self._blobs[key] = blob
-        self._in_memory_size += blob.size
-        self._lru_queue.append(key)
-
-    def __delitem__(self, key: str) -> None:
-        """Remove a key from the storage."""
-        if key not in self._blobs:
-            raise KeyError(key)
-
-        blob = self._blobs.pop(key)
-        assert blob is not None
-        if blob.location == BlobLocation.MEMORY:
-            self._in_memory_size -= blob.size
-            self._lru_queue.remove(key)
-        blob.delete_file()
-
-    def __iter__(self) -> Iterator[str]:
-        """Iterate over keys in the storage."""
-        yield from self._blobs
-
-    def __len__(self) -> int:
-        """Return number of keys in the storage."""
-        return len(self._blobs)
-
-    def __contains__(self, key: object) -> bool:
-        """Check if storage contains a key."""
-        return key in self._blobs
-
-    def clear(self) -> None:
-        """Clear all keys in the storage."""
-        keys = list(self._blobs.keys())
-        for key in keys:
-            del self._blobs[key]
-        self._lru_queue.clear()
-
-    def cleanup(self) -> None:
-        """Clear all keys in the storage and remove the data dump."""
-        if self.dump_dir is not None:
-            shutil.rmtree(self.dump_dir)
-        self._blobs.clear()
-
-    def _fits(self, size: int) -> bool:
-        """Check if there is `size` bytes available in the storage."""
-        if self.max_size is None:
-            return True
-
-        assert size <= self.max_size
-        return self._in_memory_size + size <= self.max_size
-
-    def _make_space(self, size: int) -> None:
-        """Demote LRU keys to the file dump until `size` bytes is clear."""
-        while not self._fits(size) and len(self._lru_queue) > 0:
-            lru_key = self._lru_queue.popleft()
-            blob = self._blobs[lru_key]
-            blob.dump()
-            self._in_memory_size -= blob.size
+        try:
+            client.put(
+                self.address,
+                key.object_id,
+                obj,
+                key.endpoint_id,
+                session=self._session,
+            )
+        except requests.exceptions.RequestException as e:
+            raise EndpointConnectorError(
+                f'Put failed with error code {e.response.status_code}.',
+            ) from e
+
+        return key
+
+    def put_batch(self, objs: Sequence[bytes]) -> list[EndpointKey]:
+        """Put a batch of serialized objects in the store.
+
+        Args:
+            objs: Sequence of serialized objects to put in the store.
+
+        Returns:
+            List of keys with the same order as `objs` which can be used to \
+            retrieve the objects.
+        """
+        return [self.put(obj) for obj in objs]
```

### Comparing `proxystore-0.4.1a1/proxystore/factory.py` & `proxystore-0.5.0/proxystore/factory.py`

 * *Files 13% similar despite different names*

```diff
@@ -15,78 +15,69 @@
 T = TypeVar('T')
 
 
 class Factory(Generic[T]):
     """Abstract Factory Class.
 
     A factory is a callable object that when called, returns an object.
-    The :any:`Proxy <proxystore.proxy.Proxy>` constructor takes an instance of
+    The [`Proxy`][proxystore.proxy.Proxy] constructor takes an instance of
     a factory and calls the factory when the proxy does its just-in-time
     resolution.
 
     Note:
-        All factory implementations must be subclasses of
-        :class:`Factory <.Factory>`.
-
-    Note:
-        If a custom factory is not-pickleable,
-        :func:`__getnewargs_ex__` may need to be implemented.
-        Writing custom pickling functions is also beneifical to ensure that
-        a pickled factory does not contain the object itself, just what is
-        needed to resolve the object to keep the final pickled factory as
-        small as possible.
+        If a custom factory is not-pickleable, `__getnewargs_ex__` may need to
+        be implemented. Writing custom pickling functions is also beneifical
+        to ensure that a pickled factory does not contain the object itself,
+        just what is needed to resolve the object to keep the final pickled
+        factory as small as possible.
     """
 
     def __init__(self) -> None:
-        """Init Factory."""
         raise NotImplementedError
 
     def __call__(self) -> T:
-        """Aliases :func:`resolve()`."""
+        """Alias [`Factory.resolve()`][proxystore.factory.Factory.resolve]."""
         return self.resolve()
 
     def resolve(self) -> T:
         """Resolve and return object."""
         raise NotImplementedError
 
 
 class SimpleFactory(Factory[T]):
-    """Simple Factory that stores object as class attribute."""
+    """Simple Factory that stores object as class attribute.
 
-    def __init__(self, obj: T) -> None:
-        """Init Factory.
+    Args:
+        obj: Object to produce when factory is called.
+    """
 
-        Args:
-            obj (object): object to produce when factory is called.
-        """
+    def __init__(self, obj: T) -> None:
         self._obj = obj
 
     def resolve(self) -> T:
-        """Return object."""
+        """Return the object."""
         return self._obj
 
 
 class LambdaFactory(Factory[T]):
-    """Factory that takes any callable object."""
+    """Factory that takes any callable object.
+
+    Args:
+        target: Callable object (function, class, lambda) to be
+            invoked when the factory is resolved.
+        args: Argument tuple for target invocation.
+        kwargs: Dictionary of keyword arguments for target invocation.
+    """
 
     def __init__(
         self,
         target: Callable[..., T],
         *args: Any,
         **kwargs: Any,
     ) -> None:
-        """Init LambdaFactory.
-
-        Args:
-            target (callable): callable object (function, class, lambda) to be
-                invoked when the factory is resolved.
-            args (tuple): argument tuple for target invocation (default: ()).
-            kwargs (dict): dictionary of keyword arguments for target
-                invocation (default: {}).
-        """
         self._target = target
         self._args = args
         self._kwargs = kwargs
 
     def resolve(self) -> T:
-        """Return target object."""
+        """Return the target object."""
         return self._target(*self._args, **self._kwargs)
```

### Comparing `proxystore-0.4.1a1/proxystore/globus.py` & `proxystore-0.5.0/proxystore/globus.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,38 +1,35 @@
 """Globus OAuth tools.
 
-ProxyStore provides the ``proxystore-globus-auth`` CLI tool to give consent
+ProxyStore provides the `proxystore-globus-auth` CLI tool to give consent
 to the ProxyStore Globus Application.
 
-.. code-block:: bash
-
-   # basic authentication
-   proxystore-globus-auth
-   # delete old tokens
-   proxystore-globus-auth --delete
-   # give consent for specific collections
-   proxystore-globus-auth --collections [COLLECTION_UUID] [COLLECTION_UUID] ...
-   # specify additional scopes
-   proxystore-globus-auth --scopes [SCOPE] [SCOPE] ...
-
-Based on
-`Parsl's implementation <https://github.com/Parsl/parsl/blob/1.2.0/parsl/data_provider/globus.py>`_
-and the
-`Globus examples <https://github.com/globus/native-app-examples/blob/064569e103f7d328f3d6c4b1242234011c81dffb/example_copy_paste_refresh_token.py>`_.
-"""  # noqa: E501
+```bash
+# basic authentication
+proxystore-globus-auth
+# delete old tokens
+proxystore-globus-auth --delete
+# give consent for specific collections
+proxystore-globus-auth --collections COLLECTION_UUID COLLECTION_UUID ...
+# specify additional scopes
+proxystore-globus-auth --scopes SCOPE SCOPE ...
+```
+
+Based on [Parsl's implementation](https://github.com/Parsl/parsl/blob/1.2.0/parsl/data_provider/globus.py){target=_blank}
+and the [Globus examples](https://github.com/globus/native-app-examples/blob/064569e103f7d328f3d6c4b1242234011c81dffb/example_copy_paste_refresh_token.py){target=_blank}.
+"""
 from __future__ import annotations
 
-import argparse
 import functools
 import json
 import os
 from typing import Any
 from typing import Iterable
-from typing import Sequence
 
+import click
 import globus_sdk
 
 from proxystore.utils import home_dir
 
 # Registered `ProxyStore Application` by jgpauloski@uchicago.edu
 _APPLICATION_ID = 'a3379dba-a492-459a-a8df-5e7676a0472f'
 # https://docs.globus.org/globus-connect-server/migrating-to-v5.4/application-migration/#activation_is_replaced_by_consent  # noqa: E501
@@ -46,60 +43,93 @@
 class GlobusAuthFileError(Exception):
     """Exception raised if the Globus Auth token file cannot be read."""
 
     pass
 
 
 def load_tokens_from_file(filepath: str) -> dict[str, dict[str, Any]]:
-    """Load a set of saved tokens."""
-    with open(filepath) as f:
-        tokens = json.load(f)
+    """Load a set of saved tokens.
+
+    Args:
+        filepath: Filepath containing JSON tokens to load.
 
-    return tokens
+    Returns:
+        JSON data from tokens file.
+    """
+    with open(filepath) as f:
+        return json.load(f)
 
 
 def save_tokens_to_file(
     filepath: str,
     tokens: globus_sdk.OAuthTokenResponse,
 ) -> None:
-    """Save a set of tokens for later use."""
+    """Save a set of tokens for later use.
+
+    Args:
+        filepath: Filepath to write tokens to.
+        tokens: Tokens returned by the Globus API.
+    """
     with open(filepath, 'w') as f:
         json.dump(tokens.by_resource_server, f, indent=4)
 
 
 def authenticate(
     client_id: str,
-    redirect_uri: str,
+    redirect_uri: str | None = None,
     requested_scopes: Iterable[str] | None = None,
 ) -> globus_sdk.OAuthTokenResponse:
-    """Perform Native App auth flow."""
+    """Perform Native App auth flow.
+
+    This will print a link to `auth.globus.org` where the user will
+    continue the authentication process. Then the function will wait on
+    the user to input the authorization code.
+
+    Args:
+        client_id: Globus app ID.
+        redirect_uri: The page to direct users to after authentication.
+        requested_scopes: Iterable of scopes on the token being requested.
+
+    Returns:
+        Tokens returned by the Globus API.
+    """
     client = globus_sdk.NativeAppAuthClient(client_id=client_id)
     client.oauth2_start_flow(
         redirect_uri=redirect_uri,
         refresh_tokens=True,
         requested_scopes=requested_scopes,
     )
 
     url = client.oauth2_get_authorize_url()
-    print(f'Please visit the following url to authenticate:\n{url}')
+    click.secho('Please visit the following url to authenticate:', fg='cyan')
+    click.echo(url)
 
-    auth_code = input('Enter the auth code: ').strip()
+    auth_code = click.prompt(
+        click.style('Enter the auth code:', fg='cyan'),
+        prompt_suffix=' ',
+    )
+    auth_code = auth_code.strip()
     return client.oauth2_exchange_code_for_tokens(auth_code)
 
 
 def get_authorizer(
     client_id: str,
     tokens_file: str,
-    redirect_uri: str,
 ) -> globus_sdk.RefreshTokenAuthorizer:
     """Get an authorizer for the Globus SDK.
 
+    Args:
+        client_id: Globus app ID.
+        tokens_file: Filepath to saved Globus Auth tokens.
+
+    Returns:
+        Authorizer than can be used with other parts of the Globus SDK.
+
     Raises:
-        GlobusAuthFileError:
-            if `tokens_file` cannot be parsed.
+        GlobusAuthFileError: If `tokens_file` cannot be parsed.
     """
     try:
         tokens = load_tokens_from_file(tokens_file)
     except OSError as e:
         raise GlobusAuthFileError(
             f'Error loading tokens from {tokens_file}: {e}.',
         ) from e
@@ -136,94 +166,122 @@
     return scopes
 
 
 def proxystore_authenticate(
     proxystore_dir: str | None = None,
     collections: list[str] | None = None,
     additional_scopes: list[str] | None = None,
-) -> None:
-    """Perform auth flow for ProxyStore native app."""
+) -> str:
+    """Perform auth flow for ProxyStore native app.
+
+    This is a wrapper around [`authenticate()`][proxystore.globus.authenticate]
+    which stores tokens in the ProxyStore home directory and requests the
+    appropriate scopes for ProxyStore.
+
+    Alert:
+        Globus Connect Server v5 uses consents rather than activations so
+        users need to consent to the Transfer service accessing the
+        specific mapped collection on behalf of the user. Read more
+        [here](https://docs.globus.org/globus-connect-server/migrating-to-v5.4/application-migration/#activation_is_replaced_by_consent){target=_blank}.
+
+    Args:
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
+        collections: Globus Collection UUIDs to request transfer scopes for.
+        additional_scopes: Extra scopes to include in the authorization
+            request.
+
+    Returns:
+        Path to saved tokens file.
+    """
     proxystore_dir = home_dir() if proxystore_dir is None else proxystore_dir
     tokens_file = os.path.join(proxystore_dir, _TOKENS_FILE)
     os.makedirs(proxystore_dir, exist_ok=True)
 
     scopes = _get_proxystore_scopes(collections, additional_scopes)
 
     tokens = authenticate(
         client_id=_APPLICATION_ID,
         redirect_uri=_REDIRECT_URI,
         requested_scopes=scopes,
     )
     save_tokens_to_file(tokens_file, tokens)
+    return tokens_file
 
 
 def get_proxystore_authorizer(
     proxystore_dir: str | None = None,
 ) -> globus_sdk.RefreshTokenAuthorizer:
-    """Get an authorizer for the ProxyStore native app."""
+    """Get an authorizer for the ProxyStore native app.
+
+    [`proxystore_authenticate()`][proxystore.globus.proxystore_authenticate]
+    or the CLI `#!bash proxystore-globus-auth` should be performed prior to
+    calling this function to ensure tokens have been acquired.
+
+    Args:
+        proxystore_dir: Optionally specify the proxystore home directory.
+            Defaults to [`home_dir()`][proxystore.utils.home_dir].
+
+    Returns:
+        Authorizer than can be used with other parts of the Globus SDK.
+    """
     proxystore_dir = home_dir() if proxystore_dir is None else proxystore_dir
     tokens_file = os.path.join(proxystore_dir, _TOKENS_FILE)
 
-    return get_authorizer(
-        client_id=_APPLICATION_ID,
-        tokens_file=tokens_file,
-        redirect_uri=_REDIRECT_URI,
-    )
+    return get_authorizer(client_id=_APPLICATION_ID, tokens_file=tokens_file)
 
 
-def main(argv: Sequence[str] | None = None) -> int:
-    """Perform Globus authentication."""
-    parser = argparse.ArgumentParser(
-        'ProxyStore Globus Auth Tool',
-        formatter_class=argparse.ArgumentDefaultsHelpFormatter,
-    )
-    parser.add_argument(
-        '--collections',
-        nargs='+',
-        help='Collection UUIDs to request scopes for.',
-    )
-    parser.add_argument(
-        '--scopes',
-        nargs='+',
-        help='Additional scopes to request.',
-    )
-    parser.add_argument(
-        '--delete',
-        action='store_true',
-        help='Delete existing authentication tokens.',
-    )
-    args = parser.parse_args(argv)
+@click.command()
+@click.option(
+    '--collection',
+    '-c',
+    metavar='UUID',
+    multiple=True,
+    help='Globus Collection UUID to request transfer scopes for.',
+)
+@click.option(
+    '--scope',
+    '-s',
+    metavar='SCOPE',
+    multiple=True,
+    help='Additional scope to request.',
+)
+@click.option(
+    '--delete',
+    is_flag=True,
+    default=False,
+    help='Delete existing tokens.',
+)
+def cli(collection: list[str], scope: list[str], delete: bool) -> None:
+    """Perform Globus authentication for the Transfer service.
+
+    Collections or scopes options can be strung together. E.g.,
+    request transfer scope for multiple collections with:
 
-    if args.delete:
+    $ proxystore-globus-auth -c UUID -c UUID -c UUID
+    """
+    if delete:
         tokens_file = os.path.join(home_dir(), _TOKENS_FILE)
+        fp = click.format_filename(tokens_file)
         if os.path.exists(tokens_file):
             os.remove(tokens_file)
-            print('Deleted tokens file.')
-            return 0
+            click.echo(f'Deleted tokens file: {fp}')
+            return
         else:
-            print('No tokens file found.')
-            return 1
+            click.echo(f'Tokens file does not exist: {fp}')
+            raise SystemExit(1)
 
     try:
         get_proxystore_authorizer()
     except GlobusAuthFileError:
-        print(
-            'Performing authentication for the ProxyStore Globus Native app.',
-        )
-        proxystore_authenticate(
-            collections=args.collections,
-            additional_scopes=args.scopes,
+        tokens_file = proxystore_authenticate(
+            collections=collection,
+            additional_scopes=scope,
         )
         get_proxystore_authorizer()
-        print('Globus authorization complete.')
-        return 0
+        click.echo(f'Tokens saved to: {click.format_filename(tokens_file)}')
     else:
-        print(
-            'Globus authorization is already completed. To re-authenticate, '
-            'delete your tokens (proxystore-globus-auth --delete) and try '
-            'again.',
+        click.echo(
+            'Globus authorization is already completed.\n\n'
+            'To re-authenticate, delete your tokens and try again.\n'
+            '  $ proxystore-globus-auth --delete',
         )
-        return 1
-
-
-if __name__ == '__main__':
-    raise SystemExit(main())
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/chunks.py` & `proxystore-0.5.0/proxystore/p2p/chunks.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,38 +17,35 @@
     BYTES = 1
     """Data is bytes."""
     STRING = 2
     """Data is a string."""
 
 
 class Chunk:
-    """Representation of a chunk of a message."""
+    """Representation of a chunk of a message.
+
+    Args:
+        stream_id: Unique ID for the stream of chunks.
+        seq_id: Sequence number for this chunk in the stream.
+        seq_len: Length of the stream.
+        data: Data for this chunk.
+        dtype: Optionally specify data type otherwise inferred from data.
+
+    Raises:
+        ValueError: if the sequence ID is not less than the sequence length.
+    """
 
     def __init__(
         self,
         stream_id: int,
         seq_id: int,
         seq_len: int,
         data: bytes | str,
         dtype: ChunkDType | None = None,
     ) -> None:
-        """Init Chunk.
-
-        Args:
-            stream_id (int): unique ID for the stream of chunks.
-            seq_id (int): sequence number for this chunk in the stream.
-            seq_len (int): length of the stream.
-            data (bytes, str): data for this chunk.
-            dtype (ChunkDType): optionally specify data type otherwise inferred
-                from data (default: None).
-
-        Raises:
-            ValueError:
-                if the sequence ID is not less than the sequence length.
-        """
         if seq_len <= seq_id:
             raise ValueError(
                 f'seq_id ({seq_id}) must be less than seq_len ({seq_len}).',
             )
         self.stream_id = stream_id
         self.seq_id = seq_id
         self.seq_len = seq_len
@@ -110,20 +107,20 @@
     data: bytes | str,
     size: int,
     stream_id: int,
 ) -> Generator[Chunk, None, None]:
     """Generate chunks from data.
 
     Args:
-        data (bytes, str): data to chunk.
-        size (int): size of each chunk.
-        stream_id: unique ID for the stream of chunks.
+        data: Data to chunk.
+        size: Size of each chunk.
+        stream_id: Unique ID for the stream of chunks.
 
     Yields:
-        :class:`~proxystore.p2p.chunks.Chunk`
+        Chunks of data.
     """
     seq_len = math.ceil(len(data) / size)
 
     for i, x in enumerate(range(0, len(data), size)):
         chunk_data = data[x : min(x + size, len(data))]
         yield Chunk(
             stream_id=stream_id,
@@ -133,18 +130,18 @@
         )
 
 
 def reconstruct(chunks: list[Chunk]) -> bytes | str:
     """Reconstructs data from list of chunks.
 
     Args:
-        chunks: (list[Chunk]): list of chunks to order and join.
+        chunks: List of chunks to order and join.
 
     Returns:
-        reconstructed bytes or string.
+        Reconstructed bytes or string.
     """
     if len(chunks) == 0:
         raise ValueError('Chunks list cannot be empty.')
     seq_len = chunks[0].seq_len
     if len(chunks) != seq_len:
         raise ValueError(f'Got {len(chunks)} but expected {seq_len}.')
     chunks = sorted(chunks, key=lambda c: c.seq_id)
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/connection.py` & `proxystore-0.5.0/proxystore/p2p/connection.py`

 * *Files 13% similar despite different names*

```diff
@@ -2,117 +2,115 @@
 from __future__ import annotations
 
 import asyncio
 import logging
 import re
 import warnings
 from collections import defaultdict
+from typing import Any
+from typing import Awaitable
+from typing import Callable
 from uuid import UUID
 
 try:
     from aiortc import RTCDataChannel
     from aiortc import RTCIceCandidate
     from aiortc import RTCPeerConnection
     from aiortc import RTCSessionDescription
     from aiortc.contrib.signaling import BYE
     from aiortc.contrib.signaling import object_from_string
     from aiortc.contrib.signaling import object_to_string
     from cryptography.utils import CryptographyDeprecationWarning
-    from websockets.client import WebSocketClientProtocol
 
     warnings.simplefilter('ignore', CryptographyDeprecationWarning)
 except ImportError as e:  # pragma: no cover
     warnings.warn(
         f'{e}. To enable endpoint serving, install proxystore with '
         '"pip install proxystore[endpoints]".',
+        stacklevel=2,
     )
 
 from proxystore.p2p import messages
 from proxystore.p2p.chunks import Chunk
 from proxystore.p2p.chunks import chunkify
 from proxystore.p2p.chunks import reconstruct
 from proxystore.p2p.counter import AtomicCounter
 from proxystore.p2p.exceptions import PeerConnectionError
 from proxystore.p2p.exceptions import PeerConnectionTimeoutError
+from proxystore.p2p.relay_client import RelayServerClient
 
 logger = logging.getLogger(__name__)
 
 # These values were manually found using
 # testing/scripts/peer_connection_bandwidth.py
 MAX_CHUNK_SIZE_STRING = 2**15
 MAX_CHUNK_SIZE_BYTES = 2**15
 
 
 class PeerConnection:
     """Peer-to-peer connection.
 
     Interface for establishing a peer-to-peer connection via WebRTC
-    (`aiortc <https://aiortc.readthedocs.io/en/latest/>`_) and
+    [aiortc](https://aiortc.readthedocs.io/en/latest/){target=_blank} and
     sending/receiving messages between the two peers. The peer-to-peer
     connection is established using a central and publicly accessible
-    signaling server.
+    relay server.
 
     Warning:
         Applications should prefer using the
-        :any:`PeerManager <proxystore.p2p.manager.PeerManager>` rather than
-        using the :class:`PeerConnection <PeerConnection>` class.
+        [`PeerManager`][proxystore.p2p.manager.PeerManager] rather than using
+        the [`PeerConnection`][proxystore.p2p.connection.PeerConnection] class.
 
-    .. code-block:: python
-
-       from proxystore.p2p.connection import PeerConnection
-       from proxystore.p2p.messages import decode
-       from proxystore.p2p.server import connect
-
-       uuid1, name1, websocket1 = await connect(signaling_server_address)
-       connection1 = PeerConnection(uuid1, name1, websocket1)
-
-       uuid2, name2, websocket2 = await connect(signaling_server_address)
-       connection2 = PeerConnection(uuid2, name2, websocket2)
-
-       await connection1.send_offer(uuid2)
-       offer = decode(await websocket2.recv())
-       await connection2.handle_server_message(offer)
-       answer = decode(await websocket1.recv())
-       await connection1.handle_server_message(answer)
-
-       await connection1.ready()
-       await connection2.ready()
-
-       await connection1.send('hello')
-       assert await connection2.recv() == 'hello'
-       await connection2.send('hello hello')
-       assert await connection1.recv() == 'hello hello'
-
-       await websocket1.close()
-       await websocket2.close()
-       await connection1.close()
-       await connection2.close()
+    Example:
+        ```python
+        from proxystore.p2p.connection import PeerConnection
+        from proxystore.p2p.relay_client import RelayServerClient
+
+        client1 = RelayServerClient(relay_server_address)
+        await client1.connect()
+        connection1 = PeerConnection(client1)
+
+        client2 = RelayServerClient(relay_server_address)
+        await client2.connect()
+        connection2 = PeerConnection(client2)
+
+        await connection1.send_offer(client2.uuid)
+        offer = await client2.recv()
+        await connection2.handle_server_message(offer)
+        answer = await client1.recv()
+        await connection1.handle_server_message(answer)
+
+        await connection1.ready()
+        await connection2.ready()
+
+        await connection1.send('hello')
+        assert await connection2.recv() == 'hello'
+        await connection2.send('hello hello')
+        assert await connection1.recv() == 'hello hello'
+
+        await client1.close()
+        await client2.close()
+        await connection1.close()
+        await connection2.close()
+        ```
+
+    Args:
+        relay_client: Client connection to the relay server.
+        channels: Number of datachannels to open with peer.
     """
 
     def __init__(
         self,
-        uuid: UUID,
-        name: str,
-        websocket: WebSocketClientProtocol,
+        relay_client: RelayServerClient,
         *,
         channels: int = 1,
     ) -> None:
-        """Init P2PConnection.
-
-        Args:
-            uuid (str): uuid of this client.
-            name (str): readable name of this client for logging.
-            websocket (WebSocketClientProtocol): websocket connection to the
-                signaling server.
-            channels (int): number of datachannels to open with peer
-                (default: 1).
-        """
-        self._uuid = uuid
-        self._name = name
-        self._websocket = websocket
+        self._uuid = relay_client.uuid
+        self._name = relay_client.name
+        self._relay_client = relay_client
         self._max_channels = channels
 
         self._handshake_success: asyncio.Future[
             bool
         ] = asyncio.get_running_loop().create_future()
         self._pc = RTCPeerConnection()
 
@@ -140,39 +138,65 @@
         return f'{self.__class__.__name__}[{local} > {remote}]'
 
     @property
     def state(self) -> str:
         """Get the current connection state.
 
         Returns:
-            'connected', 'connecting', 'closed', 'failed', or 'new'.
+            One of 'connected', 'connecting', 'closed', 'failed', or 'new'.
         """
         return self._pc.connectionState
 
     async def close(self) -> None:
         """Terminate the peer connection."""
         logger.info(f'{self._log_prefix}: closing connection')
         # Flush send buffers before close
         # https://github.com/aiortc/aiortc/issues/547
         for channel in self._channels.values():
             transport = channel._RTCDataChannel__transport
             await transport._data_channel_flush()
             await transport._transmit()
+            channel.close()
         await self._pc.close()
 
+    def on_close_callback(
+        self,
+        callback: Callable[..., Awaitable[None]],
+        *args: Any,
+        **kwargs: Any,
+    ) -> None:
+        """Configure a callback for when the connection fails or closes.
+
+        Args:
+            callback: Callable to invoke when the peer connection state
+                changes to closed or failed.
+            args: Positional arguments to pass to the callback.
+            kwargs: Keyword arguments to pass to the callback.
+        """
+
+        async def _on_close() -> None:
+            if self.state in ('closed', 'failed'):
+                logger.info(
+                    f'{self._log_prefix}: connection entered {self.state} '
+                    'state, invoking callback',
+                )
+                await callback(*args, **kwargs)
+
+        self._pc.on('connectionstatechange', _on_close)
+
     async def send(self, message: bytes | str, timeout: float = 30) -> None:
         """Send message to peer.
 
         Args:
-            message (bytes, str): message to send to peer.
-            timeout (float): timeout to wait on peer connection to be ready.
+            message: Message to send to peer.
+            timeout: Timeout to wait on peer connection to be ready.
 
         Raises:
-            PeerConnectionTimeoutError:
-                if the peer connection is not established within the timeout.
+            PeerConnectionTimeoutError: If the peer connection is not
+                established within the timeout.
         """
         await self.ready(timeout)
 
         chunk_size = (
             MAX_CHUNK_SIZE_STRING
             if isinstance(message, str)
             else MAX_CHUNK_SIZE_BYTES
@@ -192,51 +216,63 @@
 
         logger.debug(f'{self._log_prefix}: sending message to peer')
 
     async def recv(self) -> bytes | str:
         """Receive next message from peer.
 
         Returns:
-            message (string or bytes) received from peer.
+            Message received from peer.
         """
         return await self._incoming_queue.get()
 
     async def send_offer(self, peer_uuid: UUID) -> None:
-        """Send offer for peering via signaling server.
+        """Send offer for peering via relay server.
 
         Args:
-            peer_uuid (str): uuid of peer client to establish connection with.
+            peer_uuid: UUID of peer client to establish connection with.
         """
+
+        def _on_close(label: str) -> Any:
+            # We use this factory method to avoid Flake8-BugBear B023
+            async def on_close() -> None:
+                if self._channels[label].readyState in ('closed', 'failed'):
+                    await self.close()
+
+            return on_close
+
         for i in range(self._max_channels):
             label = f'p2p-{i}-{self._max_channels}'
             channel = self._pc.createDataChannel(label, ordered=False)
             buffer_low = asyncio.Event()
-            channel.on('open', self._on_open)
+            channel.on('open', self._on_datachannel_open)
             channel.on('bufferedamountlow', buffer_low.set)
             channel.on('message', self._on_message)
+
             self._channels[label] = channel
             self._channel_buffer_low[label] = buffer_low
 
+            # We use the underlying RTCDtlsTransport as the channel status.
+            channel.transport.transport.on('statechange', _on_close(label))
+
         await self._pc.setLocalDescription(await self._pc.createOffer())
         message = messages.PeerConnection(
             source_uuid=self._uuid,
             source_name=self._name,
             peer_uuid=peer_uuid,
             description_type='offer',
             description=object_to_string(self._pc.localDescription),
         )
-        message_str = messages.encode(message)
         logger.info(f'{self._log_prefix}: sending offer to {peer_uuid}')
-        await self._websocket.send(message_str)
+        await self._relay_client.send(message)
 
     async def send_answer(self, peer_uuid: UUID) -> None:
-        """Send answer to peering request via signaling server.
+        """Send answer to peering request via relay server.
 
         Args:
-            peer_uuid (str): uuid of peer client that sent the initial offer.
+            peer_uuid: UUID of peer client that sent the initial offer.
         """
 
         @self._pc.on('datachannel')
         def on_datachannel(channel: RTCDataChannel) -> None:
             logger.info(f'{self._log_prefix}: peer channel established')
             # TODO: note this is first channel opened
             match = re.search(r'(\d+)-(\d+)$', channel.label)
@@ -248,60 +284,67 @@
 
             buffer_low = asyncio.Event()
             self._channels[channel.label] = channel
             self._channel_buffer_low[channel.label] = buffer_low
             channel.on('bufferedamountlow', buffer_low.set)
             channel.on('message', self._on_message)
 
+            async def _on_close() -> None:
+                if channel.readyState in ('closed', 'failed'):
+                    await self.close()
+                else:
+                    pass  # pragma: no cover
+
+            # We use the underlying RTCDtlsTransport as the channel status
+            channel.transport.transport.on('statechange', _on_close)
+
             if len(self._channels) >= total:
                 self._handshake_success.set_result(True)
 
         await self._pc.setLocalDescription(await self._pc.createAnswer())
         message = messages.PeerConnection(
             source_uuid=self._uuid,
             source_name=self._name,
             peer_uuid=peer_uuid,
             description_type='answer',
             description=object_to_string(self._pc.localDescription),
         )
-        message_str = messages.encode(message)
         logger.info(f'{self._log_prefix}: sending answer to {peer_uuid}')
-        await self._websocket.send(message_str)
+        await self._relay_client.send(message)
 
     async def _on_message(self, data: bytes) -> None:
         chunk = Chunk.from_bytes(data)
         self._incoming_chunks[chunk.stream_id].append(chunk)
 
         if len(self._incoming_chunks[chunk.stream_id]) == chunk.seq_len:
             chunks = self._incoming_chunks.pop(chunk.stream_id)
             message = reconstruct(chunks)
             await self._incoming_queue.put(message)
             logger.debug(f'{self._log_prefix}: received message from peer')
 
-    def _on_open(self) -> None:
+    def _on_datachannel_open(self) -> None:
         # Note: this callback is only used on the offerer/initiators side
         logger.info(f'{self._log_prefix}: peer channels established')
         self._ready += 1
         if self._ready >= self._max_channels:
             self._handshake_success.set_result(True)
 
     async def handle_server_message(
         self,
         message: messages.PeerConnection,
     ) -> None:
-        """Handle message from the signaling server.
+        """Handle message from the relay server.
 
         Args:
-            message (PeerConnection): message received from the
-                signaling server.
+            message: Message received from the relay server.
         """
         if message.error is not None:
             self._handshake_success.set_exception(
                 PeerConnectionError(
-                    'Received error message from signaling server: '
+                    'Received error message from relay server: '
                     f'{str(message.error)}',
                 ),
             )
             return
 
         if message.description_type == 'offer':
             logger.info(
@@ -325,42 +368,42 @@
             await self._pc.setRemoteDescription(obj)
             self._peer_uuid = message.source_uuid
             self._peer_name = message.source_name
             if obj.type == 'offer':
                 await self.send_answer(message.source_uuid)
         elif isinstance(obj, RTCIceCandidate):  # pragma: no cover
             # We should not receive an RTCIceCandidate message via the
-            # signaling server but this is here following the aiortc example.
+            # relay server but this is here following the aiortc example.
             # https://github.com/aiortc/aiortc/blob/713fb644b95328f8ec1ac2cbb54def0424cc6645/examples/datachannel-cli/cli.py#L30  # noqa: E501
             await self._pc.addIceCandidate(obj)
         elif obj is BYE:  # pragma: no cover
             raise AssertionError('received BYE message')
         else:
             raise AssertionError('received unknown message')
 
     async def ready(self, timeout: float | None = None) -> None:
         """Wait for connection to be ready.
 
         Args:
-            timeout (float, optional): maximum time in seconds to wait for
+            timeout: The maximum time in seconds to wait for
                 the peer connection to establish. If None, block until
-                the connection is established (default: None).
+                the connection is established.
 
         Raises:
-            PeerConnectionTimeoutError:
-                if the connection is not ready within the timeout.
-            PeerConnectionError:
-                if there is an error establishing the peer connection.
+            PeerConnectionTimeoutError: If the connection is not ready within
+                the timeout.
+            PeerConnectionError: If there is an error establishing the peer
+                connection.
         """
         try:
             await asyncio.wait_for(self._handshake_success, timeout)
         except asyncio.TimeoutError as e:
             raise PeerConnectionTimeoutError(
                 'Timeout waiting for peer to peer connection to establish '
                 f'in {self._log_prefix}.',
             ) from e
 
 
 def log_name(uuid: UUID, name: str) -> str:
-    """Return str formatted as `name(uuid-prefix)`."""
+    """Return string formatted as `#!python 'name(uuid-prefix)'`."""
     uuid_ = str(uuid)
     return f'{name}({uuid_[:min(8,len(uuid_))]})'
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/counter.py` & `proxystore-0.5.0/proxystore/p2p/counter.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,36 +1,33 @@
 """Atomic counting utilities."""
 from __future__ import annotations
 
 import threading
 
 
 class AtomicCounter:
-    """Thread-safe counter."""
+    """Thread-safe counter.
 
-    def __init__(self, size: int | None = None) -> None:
-        """Init AtomicCounter.
+    Args:
+        size: Optional max count upon which an exception will be raised.
+    """
 
-        Args:
-            size (int): optional max count upon which an exception will be
-                raised (default: None).
-        """
+    def __init__(self, size: int | None = None) -> None:
         self._size = size
         self._value = 0
         self._lock = threading.Lock()
 
     def increment(self) -> int:
         """Get current count and increment value.
 
         Returns:
-            current count (int).
+            Current count.
 
         Raises:
-            ValueError:
-                if current count is equal to or greater than size.
+            ValueError: If current count is equal to or greater than size.
         """
         with self._lock:
             value = self._value
             if self._size is not None and value >= self._size:
                 raise ValueError(f'Max counter size exceeded ({self._size}).')
             self._value += 1
             return value
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/manager.py` & `proxystore-0.5.0/proxystore/p2p/manager.py`

 * *Files 16% similar despite different names*

```diff
@@ -3,235 +3,226 @@
 
 import asyncio
 import logging
 import ssl
 from types import TracebackType
 from typing import Any
 from typing import Generator
+from typing import Iterable
 from uuid import UUID
 
 try:
     import websockets
-    from websockets.client import WebSocketClientProtocol
 except ImportError as e:  # pragma: no cover
     import warnings
 
     warnings.warn(
         f'{e}. To enable endpoint serving, install proxystore with '
         '"pip install proxystore[endpoints]".',
+        stacklevel=2,
     )
 
 from proxystore import utils
 from proxystore.p2p import messages
-from proxystore.p2p.client import connect
 from proxystore.p2p.connection import log_name
 from proxystore.p2p.connection import PeerConnection
 from proxystore.p2p.exceptions import PeerConnectionError
-from proxystore.p2p.exceptions import PeerRegistrationError
+from proxystore.p2p.exceptions import PeerConnectionTimeoutError  # noqa: F401
+from proxystore.p2p.relay_client import RelayServerClient
 from proxystore.p2p.task import SafeTaskExitError
 from proxystore.p2p.task import spawn_guarded_background_task
 
 logger = logging.getLogger(__name__)
 
 
 class PeerManager:
     """Peer Connections Manager.
 
     Handles establishing peer connections via
-    `aiortc <https://aiortc.readthedocs.io/>`_, responding to requests for
-    new peer connections from the signaling server, and sending and
-    receiving data to/from existing peer connections.
-
-    .. code-block:: python
-
-       from proxystore.p2p.manager import PeerManager
-
-       pm1 = await PeerManager(uuid.uuid4(), signaling_server_address)
-       pm2 = await PeerManager(uuid.uuid4(), signaling_server_address)
-
-       await pm1.send(pm2.uuid, 'hello hello')
-       source_uuid, message = await pm2.recv()
-       assert source_uuid == pm1.uuid
-       assert message == 'hello hello'
-
-       pm1.close()
-       pm2.close()
+    [aiortc](https://aiortc.readthedocs.io/){target=_blank}, responding to
+    requests for new peer connections from the relay server, and sending
+    and receiving data to/from existing peer connections.
+
+
+    Example:
+        ```python
+        from proxystore.p2p.manager import PeerManager
+
+        pm1 = await PeerManager(uuid.uuid4(), relay_server_address)
+        pm2 = await PeerManager(uuid.uuid4(), relay_server_address)
+
+        await pm1.send(pm2.uuid, 'hello hello')
+        source_uuid, message = await pm2.recv()
+        assert source_uuid == pm1.uuid
+        assert message == 'hello hello'
+
+        pm1.close()
+        pm2.close()
+        ```
 
     Note:
-        The :class:`PeerManager <.PeerManager>` can also be used as a context
-        manager.
+        The class can also be used as a context manager.
 
-        >>> async with PeerManager(..) as manager:
-        >>>     ...
+        ```python
+        async with PeerManager(..) as manager:
+            ...
+        ```
+
+    Warning:
+        The class must be initialized with await or inside an async with
+        statement to correctly configure all async tasks and connections.
+
+        ```python
+        manager = await PeerManager(...)
+        manager.close()
+        ```
+
+        ```python
+        async with PeerManager(...) as manager:
+            ...
+        ```
+
+    Args:
+        uuid: UUID of the client.
+        relay_server: Address of relay server to use for establishing
+            peer-to-peer connections.
+        name: Readable name of the client to use in logging. If unspecified,
+            the hostname will be used.
+        timeout: Timeout in seconds when waiting for a peer or relay server
+            connection to be established.
+        peer_channels: number of datachannels to split message sending over
+            between each peer.
+        verify_certificate: Verify the relay server's SSL certificate,
+
+    Raises:
+        ValueError: If the relay server address does not start with "ws://"
+            or "wss://".
     """
 
     def __init__(
         self,
         uuid: UUID,
-        signaling_server: str,
+        relay_server: str,
         name: str | None = None,
         *,
         timeout: int = 30,
         peer_channels: int = 1,
         verify_certificate: bool = True,
     ) -> None:
-        """Init PeerManager.
-
-        Warning:
-            The :class:`PeerManager <.PeerManager>` must be initialized
-            with await or inside an async with statement to correctly
-            configure all async tasks and connections.
-
-            >>> manager = await PeerManager(...)
-            >>> manager.close()
-            >>>
-            >>> async with PeerManager(...) as manager:
-            >>>     ...
-
-        Args:
-            uuid (str, UUID): uuid of the client.
-            signaling_server (str): address of signaling server to use for
-                establishing peer-to-peer connections.
-            name (str, optional): readable name of the client to use in
-                logging. If unspecified, the hostname will be used.
-            timeout (int): timeout in seconds when waiting for a peer
-                or signaling server connection to be established (default: 30).
-            peer_channels (int): number of datachannels to split message
-                sending over between each peer (default: 1).
-            verify_certificate (bool): verify the signaling server's SSL
-                certificate (default: True).
-
-        Raises:
-            ValueError:
-                if the signaling server address does not start with ws://
-                or wss://.
-        """
         if not (
-            signaling_server.startswith('ws://')
-            or signaling_server.startswith('wss://')
+            relay_server.startswith('ws://')
+            or relay_server.startswith('wss://')
         ):
             raise ValueError(
-                'Signaling server address must start with ws:// or wss://'
-                f'Got {signaling_server}.',
+                'Relay server address must start with ws:// or wss://'
+                f'Got {relay_server}.',
             )
         self._uuid = uuid
-        self._signaling_server = signaling_server
+        self._relay_server = relay_server
         self._name = name if name is not None else utils.hostname()
         self._timeout = timeout
         self._peer_channels = peer_channels
         self._verify_certificate = verify_certificate
 
         self._peers_lock = asyncio.Lock()
         self._peers: dict[frozenset[UUID], PeerConnection] = {}
 
         self._message_queue: asyncio.Queue[
             tuple[UUID, bytes | str]
         ] = asyncio.Queue()
         self._server_task: asyncio.Task[None] | None = None
         self._tasks: dict[frozenset[UUID], asyncio.Task[None]] = {}
-        self._websocket_or_none: WebSocketClientProtocol | None = None
+        self._relay_server_client_or_none: RelayServerClient | None = None
 
     @property
     def _log_prefix(self) -> str:
         return f'{self.__class__.__name__}[{log_name(self._uuid, self._name)}]'
 
     @property
-    def _websocket(self) -> WebSocketClientProtocol:
-        if self._websocket_or_none is not None:
-            return self._websocket_or_none
+    def _relay_server_client(self) -> RelayServerClient:
+        if self._relay_server_client_or_none is not None:
+            return self._relay_server_client_or_none
         raise RuntimeError(
             f'{self.__class__.__name__} has not established a connection '
-            'to the signaling server because async_init() has not been '
+            'to the relay server because async_init() has not been '
             'called yet. Is the manager being initialized with await?',
         )
 
     @property
     def uuid(self) -> UUID:
-        """Get UUID of the peer manager."""
+        """UUID of the peer manager."""
         return self._uuid
 
     @property
     def name(self) -> str:
-        """Get name of the peer manager."""
+        """Name of the peer manager."""
         return self._name
 
     async def async_init(self) -> None:
-        """Connect to signaling server."""
-        if self._websocket_or_none is None:
+        """Connect to relay server."""
+        if self._relay_server_client_or_none is None:
             ssl_context = ssl.create_default_context()
             if not self._verify_certificate:
                 ssl_context.check_hostname = False
                 ssl_context.verify_mode = ssl.CERT_NONE
 
-            uuid, _, socket = await connect(
-                address=self._signaling_server,
-                uuid=self._uuid,
-                name=self._name,
+            client = RelayServerClient(
+                address=self._relay_server,
+                client_uuid=self._uuid,
+                client_name=self._name,
                 timeout=self._timeout,
                 ssl=ssl_context
-                if self._signaling_server.startswith('wss://')
+                if self._relay_server.startswith('wss://')
                 else None,
             )
+            await client.connect()
 
-            if uuid != self._uuid:
-                raise PeerRegistrationError(
-                    'Signaling server responded to registration request '
-                    f'with non-matching UUID. Received {uuid} but expected '
-                    f'{self._uuid}.',
-                )
-            self._websocket_or_none = socket
+            self._relay_server_client_or_none = client
             logger.info(
-                f'{self._log_prefix}: registered as peer with signaling '
-                f'server at {self._signaling_server}',
+                f'{self._log_prefix}: registered as peer with relay '
+                f'server at {self._relay_server}',
             )
         if self._server_task is None:
             self._server_task = spawn_guarded_background_task(
                 self._handle_server_messages,
             )
 
     async def __aenter__(self) -> PeerManager:
-        """Enter async context manager."""
         await self.async_init()
         return self
 
     async def __aexit__(
         self,
         exc_type: type[BaseException] | None,
         exc_value: BaseException | None,
         exc_traceback: TracebackType | None,
     ) -> None:
-        """Leave async context manager and close manager."""
         await self.close()
 
     def __await__(self) -> Generator[Any, None, PeerManager]:
-        """Awaitable constructor."""
         return self.__aenter__().__await__()
 
     async def _check_connection(
         self,
         peer_uuid: UUID,
         connection: PeerConnection,
     ) -> None:
         """Wait on connection to be ready and handle errors.
 
-        If an error is raised, catch it and remove this PeerConnection.
+        If an error is raised, catch it and remove this `PeerConnection`.
 
         Warning:
             This method will cancel the task that is handling the peer
             messages.
         """
         try:
             await connection.ready(timeout=self._timeout)
-        except PeerConnectionError as e:  # pragma: >=3.8 cover
+        except PeerConnectionError as e:
             logger.error(str(e))
-            await connection.close()
-            peers = frozenset({self._uuid, peer_uuid})
-            async with self._peers_lock:
-                self._peers.pop(peers, None)
-            raise SafeTaskExitError() from None
+            await self.close_connection((self._uuid, peer_uuid))
 
     async def _handle_peer_messages(
         self,
         peer_uuid: UUID,
         connection: PeerConnection,
     ) -> None:
         await self._check_connection(peer_uuid, connection)
@@ -246,73 +237,67 @@
             await self._message_queue.put((peer_uuid, message))
             logger.debug(
                 f'{self._log_prefix}: placed message from {peer_name} on '
                 'queue',
             )
 
     async def _handle_server_messages(self) -> None:
-        """Handle messages from the signaling server.
+        """Handle messages from the relay server.
 
         Forwards the message to the correct P2PConnection instance.
         """
         logger.info(
-            f'{self._log_prefix}: listening for messages from signaling '
-            'server',
+            f'{self._log_prefix}: listening for messages from relay server',
         )
         while True:
             try:
-                message_str = await self._websocket.recv()
-                if isinstance(message_str, str):
-                    message = messages.decode(message_str)
-                else:
-                    raise AssertionError('Received non-str on websocket.')
+                message = await self._relay_server_client.recv()
             except websockets.exceptions.ConnectionClosedOK:
                 break
             except websockets.exceptions.ConnectionClosedError:
                 break
             except messages.MessageDecodeError as e:
                 logger.error(
                     f'{self._log_prefix}: error deserializing message from '
-                    f'signaling server: {e} ...skipping message',
+                    f'relay server: {e} ...skipping message',
                 )
                 continue
 
             if isinstance(message, messages.PeerConnection):
                 logger.debug(
-                    f'{self._log_prefix}: signaling server forwarded peer '
+                    f'{self._log_prefix}: relay server forwarded peer '
                     'connection message from '
                     f'{log_name(message.source_uuid, message.source_name)}',
                 )
                 peers = frozenset({message.source_uuid, message.peer_uuid})
                 if peers not in self._peers:
                     connection = PeerConnection(
-                        uuid=self._uuid,
-                        name=self._name,
-                        websocket=self._websocket,
+                        relay_client=self._relay_server_client,
                         channels=self._peer_channels,
                     )
                     async with self._peers_lock:
                         self._peers[peers] = connection
                     self._tasks[peers] = spawn_guarded_background_task(
                         self._handle_peer_messages,
                         message.source_uuid,
                         connection,
                     )
+                    connection.on_close_callback(self.close_connection, peers)
                 await self._peers[peers].handle_server_message(message)
             elif isinstance(message, messages.ServerResponse):
                 # The peer manager should never send something to the
-                # signaling server that warrants a ServerResponse
+                # relay server that warrants a ServerResponse
                 logger.exception(
                     f'{self._log_prefix}: got unexpected ServerResponse '
-                    f'from signaling server: {message}',
+                    f'from relay server: {message}',
                 )
             else:
                 logger.error(
                     f'{self._log_prefix}: received unknown message type '
-                    f'{type(message).__name__} from signaling server',
+                    f'{type(message).__name__} from relay server',
                 )
 
     async def close(self) -> None:
         """Close the connection manager."""
         if self._server_task is not None:
             self._server_task.cancel()
             try:
@@ -324,66 +309,95 @@
             try:
                 await task
             except (asyncio.CancelledError, SafeTaskExitError):
                 pass
         async with self._peers_lock:
             for connection in self._peers.values():
                 await connection.close()
-        if self._websocket_or_none is not None:
-            await self._websocket_or_none.close()
+        if self._relay_server_client_or_none is not None:
+            await self._relay_server_client_or_none.close()
         logger.info(f'{self._log_prefix}: peer manager closed')
 
+    async def close_connection(self, peers: Iterable[UUID]) -> None:
+        """Close a peer connection if it exists.
+
+        This will close the associated
+        [`PeerConnection`][proxystore.p2p.connection.PeerConnection] and
+        cancel the asyncio task handling peer messages. If the
+        [`PeerManager`][proxystore.p2p.manager.PeerManager] is used to
+        send a message from the peer again, a new connection will be
+        established.
+
+        Args:
+            peers: Iterable containing the two peer UUIDs taking part in the
+                connection that should be closed.
+        """
+        peers = frozenset(peers)
+        async with self._peers_lock:
+            connection = self._peers.pop(peers, None)
+        if connection is not None:
+            logger.info(
+                f'{self._log_prefix} Closing connection between peers: '
+                f'{", ".join(str(peer) for peer in peers)}',
+            )
+            await connection.close()
+        task = self._tasks.pop(peers, None)
+        if task is not None:
+            task.cancel()
+            try:
+                await task
+            except (asyncio.CancelledError, SafeTaskExitError):
+                pass
+
     async def recv(self) -> tuple[UUID, bytes | str]:
         """Receive next message from a peer.
 
         Returns:
-            tuple containing the UUID of the peer that sent the message
+            Tuple containing the UUID of the peer that sent the message \
             and the message itself.
         """
         return await self._message_queue.get()
 
     async def send(
         self,
         peer_uuid: UUID,
         message: bytes | str,
         timeout: float = 30,
     ) -> None:
         """Send message to peer.
 
         Args:
-            peer_uuid (str): UUID of peer to send message to.
-            message (bytes, str): message to send to peer.
-            timeout (float): timeout to wait on peer connection to be ready.
+            peer_uuid: UUID of peer to send message to.
+            message: Message to send to peer.
+            timeout: Timeout to wait on peer connection to be ready.
 
         Raises:
-            PeerConnectionTimeoutError:
-                if the peer connection is not established within the timeout.
+            PeerConnectionTimeoutError: If the peer connection is not
+                established within the timeout.
         """
         connection = await self.get_connection(peer_uuid)
         await connection.send(message, timeout)
 
     async def get_connection(self, peer_uuid: UUID) -> PeerConnection:
         """Get connection to the peer.
 
         Args:
-            peer_uuid (str, UUID): uuid of peer to make connection with.
+            peer_uuid: UUID of peer to make connection with.
 
         Returns:
-            :any:`PeerConnection <proxystore.p2p.connection.PeerConnection>`
+            The peer connection object.
         """
         peers = frozenset({self._uuid, peer_uuid})
 
         async with self._peers_lock:
             if peers in self._peers:
                 return self._peers[peers]
 
             connection = PeerConnection(
-                self._uuid,
-                self._name,
-                self._websocket,
+                self._relay_server_client,
                 channels=self._peer_channels,
             )
             self._peers[peers] = connection
 
         logger.info(
             f'{self._log_prefix}: opening peer connection with '
             f'{peer_uuid}',
@@ -391,8 +405,9 @@
         await connection.send_offer(peer_uuid)
 
         self._tasks[peers] = spawn_guarded_background_task(
             self._handle_peer_messages,
             peer_uuid,
             connection,
         )
+        connection.on_close_callback(self.close_connection, peers)
         return connection
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/messages.py` & `proxystore-0.5.0/proxystore/p2p/messages.py`

 * *Files 11% similar despite different names*

```diff
@@ -14,47 +14,71 @@
     from typing_extensions import Literal
 
 
 class MessageType(enum.Enum):
     """Types of messages supported."""
 
     server_response = 'ServerResponse'
+    """Server response message."""
     server_registration = 'ServerRegistration'
+    """Server registration message."""
     peer_connection = 'PeerConnection'
+    """Peer connection message."""
 
 
 @dataclasses.dataclass
 class Message:
     """Base message."""
 
     pass
 
 
 @dataclasses.dataclass
 class ServerRegistration(Message):
-    """Register with signaling server as peer."""
+    """Register with relay server as peer.
+
+    Attributes:
+        name: Name of peer requesting to register.
+        uuid: UUID of peer requesting to register.
+    """
 
     name: str
     uuid: uuid.UUID
     message_type: str = MessageType.server_registration.name
 
 
 @dataclasses.dataclass
 class ServerResponse(Message):
-    """Message returned by signaling server on success or error."""
+    """Message returned by relay server on success or error.
+
+    Attributes:
+        success: If the registration was successful.
+        message: Message from server.
+        error: If `message` is an error message.
+    """
 
     success: bool = True
     message: str | None = None
     error: bool = False
     message_type: str = MessageType.server_response.name
 
 
 @dataclasses.dataclass
 class PeerConnection(Message):
-    """Message used in establishing a peer-to-peer connection."""
+    """Message used in establishing a peer-to-peer connection.
+
+    Attributes:
+        source_uuid: UUID of sending peer.
+        source_name: Name of sending peer.
+        peer_uuid: UUID of destination peer.
+        description_type: One of `#!python 'answer'` or `#!python 'offer'`
+            indicating the type of message being sent.
+        description: Session description protocol message.
+        error: Error string if a problem occurs.
+    """
 
     source_uuid: uuid.UUID
     source_name: str
     peer_uuid: uuid.UUID
     description_type: Literal['answer', 'offer']
     description: str
     error: str | None = None
@@ -77,36 +101,37 @@
     """Cast any UUIDs to strings.
 
     Scans the input dictionary for any values where the associated key
     contains 'uuid' and value is a UUID instance and converts it to a
     string for jsonification.
 
     Returns:
-        Shallow copy of the input dictionary with values cast from UUID
+        Shallow copy of the input dictionary with values cast from UUID \
         to str if their key also contains UUID.
     """
     data = data.copy()
     for key in data:
         if 'uuid' in key.lower() and isinstance(data[key], uuid.UUID):
             data[key] = str(data[key])
     return data
 
 
 def str_to_uuid(data: dict[str, Any]) -> dict[str, Any]:
     """Cast any possible UUID strings to UUID objects.
 
-    The inverse operation of :func:`<._uuid_to_str>`.
+    The inverse operation of
+    [uuid_to_str()][proxystore.p2p.messages.uuid_to_str].
 
     Returns:
-        Shallow copy of the input dictionary with values cast from
+        Shallow copy of the input dictionary with values cast from \
         str to UUID if the key also contains UUID.
 
     Raises:
-        MessageDecodeError:
-            if a key contains 'uuid' but the value cannot be cast to a UUID.
+        MessageDecodeError: If a key contains 'uuid' but the value cannot be
+            cast to a UUID.
     """
     data = data.copy()
     for key in data:
         if 'uuid' in key.lower():
             try:
                 data[key] = uuid.UUID(data[key])
             except (AttributeError, TypeError, ValueError) as e:
@@ -116,24 +141,21 @@
     return data
 
 
 def decode(message: str) -> Message:
     """Decode JSON string into correct Message type.
 
     Args:
-        message (str): JSON string to decode.
+        message: JSON string to decode.
 
     Returns:
-        Instance of a subtype of
-        :any:`Message <proxystore.p2p.messages.Message>`.
+        Parsed message.
 
     Raises:
-        MessageDecodeError:
-            if the message cannot be decoded into a
-            :any:`Message <proxystore.p2p.messages.Message>`.
+        MessageDecodeError: If the message cannot be decoded.
     """
     try:
         data = json.loads(message)
     except json.JSONDecodeError as e:
         raise MessageDecodeError('Failed to load string as JSON.') from e
 
     try:
@@ -164,19 +186,18 @@
         ) from e
 
 
 def encode(message: Message) -> str:
     """Encode message as JSON string.
 
     Args:
-        message (Message): message to JSON encode.
+        message: Message to JSON encode.
 
     Raises:
-        MessageEncodeError:
-            if the message cannot be JSON encoded.
+        MessageEncodeError: If the message cannot be JSON encoded.
     """
     if not isinstance(message, Message):
         raise MessageEncodeError(
             f'Message is not an instance of {Message.__name__}. '
             f'Got {type(message).__name__}.',
         )
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/server.py` & `proxystore-0.5.0/proxystore/p2p/relay.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,217 +1,226 @@
-"""Signaling server implementation for WebRTC peer connections."""
+"""Relay server implementation for WebRTC peer connections.
+
+The relay server (or signaling server) is a lightweight server accessible by
+all peers (e.g., has a public IP address) that facilitates the establishment
+of peer WebRTC connections.
+"""
 from __future__ import annotations
 
-import argparse
 import asyncio
 import datetime
 import logging.handlers
 import os
 import signal
 import ssl
 import sys
 from dataclasses import dataclass
-from typing import Sequence
 from uuid import UUID
 
+import click
+
 try:
     import websockets.client
     import websockets.exceptions
     from websockets.server import WebSocketServerProtocol
 except ImportError as e:  # pragma: no cover
     import warnings
 
     warnings.warn(
         f'{e}. To enable endpoint serving, install proxystore with '
         '"pip install proxystore[endpoints]".',
+        stacklevel=2,
     )
 
 from proxystore.p2p import messages
 
 logger = logging.getLogger(__name__)
 
 
 @dataclass
 class Client:
-    """Representation of client connection."""
+    """Representation of client connection.
+
+    Attributes:
+        name: Name of client.
+        uuid: UUID of client.
+        websocket: WebSocket connection to the client.
+    """
 
     name: str
     uuid: UUID
     websocket: WebSocketServerProtocol
 
 
-class SignalingServer:
-    """Signaling Server implementation.
+class RelayServer:
+    """WebRTC relay server.
 
-    The Signaling Server acts as a public third-party that helps two peers
+    The relay server acts as a public third-party that helps two peers
     (endpoints) establish a peer-to-peer connection during the WebRTC
-    peer connection initiation process. The signaling server's responsibility
+    peer connection initiation process. The relay server's responsibility
     is just to forward session descriptions between two peers, so the
     server can be relatively lightweight and typically only needs to transfer
     two messages to establish a peer connection, after which the peers no
-    longer need the signaling server.
+    longer need the relay server.
 
     To learn more about the WebRTC peer connection process, check out
-    `<https://webrtc.org/getting-started/peer-connections>`_.
-
-    The signaling server is built on websockets and designed to be
-    served using :code:`websockets.serve`.
-
-    .. code-block:: python
+    https://webrtc.org/getting-started/peer-connections.
 
-       import websockets
-       from proxystore.p2p.server import SignalingServer
+    The relay server is built on websockets and designed to be
+    served using [`websockets.serve()`][websockets.server.serve].
 
-       signaling_server = SignalingServer()
-       async with websockets.serve(
-            signaling_server.handler, host='localhost', port=1234
-       ) as websocket_server:
-           ...
+    Example:
+        ```python
+        import websockets
+        from proxystore.p2p.relay import RelayServer
+
+        relay_server = RelayServer()
+        async with websockets.serve(
+             relay_server.handler, host='localhost', port=1234
+        ) as websocket_server:
+            ...
+        ```
     """
 
     def __init__(self) -> None:
-        """Init SignalingServer."""
         self._websocket_to_client: dict[WebSocketServerProtocol, Client] = {}
         self._uuid_to_client: dict[UUID, Client] = {}
 
     async def send(
         self,
         websocket: WebSocketServerProtocol,
         message: messages.Message,
     ) -> None:
         """Send message on the socket.
 
         Args:
-            websocket (WebSocketServerProtocol): websocket to send message on.
-            message (Message): message to json encode and send.
+            websocket: Websocket to send message on.
+            message: Message to json encode and send.
         """
         try:
             message_str = messages.encode(message)
         except messages.MessageEncodeError as e:
-            logger.error(f'failed to encode message: {e}')
+            logger.error(f'Failed to encode message: {e}')
             return
 
         try:
             await websocket.send(message_str)
         except websockets.exceptions.ConnectionClosed:
-            logger.error('connection closed while attempting to send message')
+            logger.error('Connection closed while attempting to send message')
 
     async def register(
         self,
         websocket: WebSocketServerProtocol,
         request: messages.ServerRegistration,
     ) -> None:
-        """Register peer with Signaling Server.
+        """Register peer with relay server.
 
         Args:
-            websocket (WebSocketServerProtocol): websocket connection with
-                client wanting to register.
-            request (ServerRegistration): registration request message.
+            websocket: Websocket connection with client wanting to register.
+            request: Registration request message.
         """
         if websocket not in self._websocket_to_client:
             # Check if previous client reconnected on new socket so unregister
             # old socket. Warning: could be a client impersontating another
             if request.uuid in self._uuid_to_client:
                 logger.info(
-                    f'previously registered client {request.uuid} attempting '
+                    f'Previously registered client {request.uuid} attempting '
                     'to reregister so old registration will be removed',
                 )
                 await self.unregister(
                     self._uuid_to_client[request.uuid].websocket,
                     False,
                 )
             client = Client(
                 name=request.name,
                 uuid=request.uuid,
                 websocket=websocket,
             )
             self._websocket_to_client[websocket] = client
             self._uuid_to_client[client.uuid] = client
             logger.info(
-                f'registered {client.uuid} ({client.name} at '
+                f'Registered {client.uuid} ({client.name} at '
                 f'{websocket.remote_address})',
             )
         else:
             client = self._websocket_to_client[websocket]
             logger.info(
-                f'previously registered client {client.uuid} attempting to '
+                f'Previously registered client {client.uuid} attempting to '
                 'reregister so previous registration will be returned',
             )
 
         await self.send(websocket, messages.ServerResponse(success=True))
 
     async def unregister(
         self,
         websocket: WebSocketServerProtocol,
         expected: bool,
     ) -> None:
         """Unregister the endpoint.
 
         Args:
-            websocket (WebSocketServerProtocol): websocket connection that
-                was closed.
-            expected (bool): if the connection was closed intentionally or
-                due to an error.
+            websocket: Websocket connection that was closed.
+            expected: If the connection was closed intentionally or due to an
+                error.
         """
         client = self._websocket_to_client.pop(websocket, None)
         if client is None:
             # Most likely websocket closed before registration was performed
             return
         reason = 'ok' if expected else 'unexpected'
         logger.info(
-            f'unregistering client {client.uuid} ({client.name}) '
+            f'Unregistering client {client.uuid} ({client.name}) '
             f'for {reason} reason',
         )
         self._uuid_to_client.pop(client.uuid, None)
         await client.websocket.close(code=1000 if expected else 1001)
 
     async def connect(
         self,
         websocket: WebSocketServerProtocol,
         message: messages.PeerConnection,
     ) -> None:
         """Pass peer connection messages between clients.
 
         Args:
-            websocket (WebSocketServerProtocol): websocket connection with
-                client that sent the peer connection message.
-            message (PeerConnectionMessage): message to forward to peer client.
+            websocket: Websocket connection with client that sent the peer
+                connection message.
+            message: Message to forward to peer client.
         """
         client = self._websocket_to_client[websocket]
         if message.peer_uuid not in self._uuid_to_client:
             logger.warning(
-                f'client {client.uuid} ({client.name}) attempting to send '
+                f'Client {client.uuid} ({client.name}) attempting to send '
                 f'message to unknown peer {message.peer_uuid}',
             )
             message.error = (
                 'Cannot forward peer connection message to peer '
                 f'{message.peer_uuid} because this peer is unknown.'
             )
             await self.send(websocket, message)
         else:
             peer_client = self._uuid_to_client[message.peer_uuid]
             logger.info(
-                f'transmitting message from {client.uuid} ({client.name}) '
+                f'Transmitting message from {client.uuid} ({client.name}) '
                 f'to {message.peer_uuid}',
             )
             await self.send(peer_client.websocket, message)
 
     async def handler(
         self,
         websocket: WebSocketServerProtocol,
         uri: str,
     ) -> None:
         """Websocket server message handler.
 
         Args:
-            websocket (WebSocketServerProtocol): websocket message was
-                received on.
-            uri (str): uri message was sent to.
+            websocket: Websocket message was received on.
+            uri: URI message was sent to.
         """
-        logger.info('signaling server listening for incoming connections')
+        logger.info('Relay server listening for incoming connections')
         while True:
             try:
                 message_str = await websocket.recv()
                 if isinstance(message_str, str):
                     message = messages.decode(message_str)
                 else:
                     raise AssertionError(
@@ -221,29 +230,29 @@
                 await self.unregister(websocket, expected=True)
                 break
             except websockets.exceptions.ConnectionClosedError:
                 await self.unregister(websocket, expected=False)
                 break
             except messages.MessageDecodeError as e:
                 logger.error(
-                    'caught deserialization error on message received from '
+                    'Caught deserialization error on message received from '
                     f'{websocket.remote_address}: {e} ...skipping message',
                 )
                 continue
 
             if isinstance(message, messages.ServerRegistration):
                 await self.register(websocket, message)
             elif isinstance(message, messages.PeerConnection):
                 if websocket in self._websocket_to_client:
                     await self.connect(websocket, message)
                 else:
                     # If message is not a registration request but this client
                     # has not yet registered, let them know
                     logger.info(
-                        'returning server error to message received from '
+                        'Returning server error to message received from '
                         f'unregistered client {message.source_uuid} '
                         f'({message.source_name})',
                     )
                     response = messages.ServerResponse(
                         success=False,
                         message='client has not registered yet',
                         error=True,
@@ -255,29 +264,29 @@
 
 async def serve(
     host: str,
     port: int,
     certfile: str | None = None,
     keyfile: str | None = None,
 ) -> None:
-    """Run the signaling server.
+    """Run the relay server.
 
-    Initializes a :class:`SignalingServer <.SignalingServer>` and starts a
-    websocket server listening on `host:port` for new connections and
-    incoming messages.
+    Initializes a [`RelayServer`][proxystore.p2p.relay.RelayServer]
+    and starts a websocket server listening on `host:port` for new connections
+    and incoming messages.
 
     Args:
-        host (str): host to listen on.
-        port (int): port to listen on.
-        certfile (str): optional certificate file (PEM format) to enable
-            TLS while serving.
-        keyfile (str): optional private key file. If not specified, the key
-            will be taken from the certfile.
+        host: Host to listen on.
+        port: Port to listen on.
+        certfile: Optional certificate file (PEM format) to enable TLS while
+            serving.
+        keyfile: Optional private key file. If not specified, the key will be
+            taken from the certfile.
     """
-    server = SignalingServer()
+    server = RelayServer()
 
     # Set the stop condition when receiving SIGINT (ctrl-C) and SIGTERM.
     loop = asyncio.get_running_loop()
     stop = loop.create_future()
     loop.add_signal_handler(signal.SIGINT, stop.set_result, None)
     loop.add_signal_handler(signal.SIGTERM, stop.set_result, None)
 
@@ -289,98 +298,94 @@
     async with websockets.server.serve(
         server.handler,
         host,
         port,
         logger=logger,
         ssl=ssl_context,
     ):
-        logger.info(f'serving signaling server on {host}:{port}')
-        logger.info('use ctrl-C to stop')
+        logger.info(f'Serving relay server on {host}:{port}')
+        logger.info('Use ctrl-C to stop')
         await stop
 
-    logger.info('server closed')
+    loop.remove_signal_handler(signal.SIGINT)
+    loop.remove_signal_handler(signal.SIGTERM)
 
+    logger.info('Server closed')
 
-def main(argv: Sequence[str] | None = None) -> int:
-    """CLI for starting the signaling server.
 
-    Usage:
-
-    .. code-block:: console
+@click.command()
+@click.option(
+    '--host',
+    default='0.0.0.0',
+    metavar='ADDR',
+    help='Address to listen on.',
+)
+@click.option(
+    '--port',
+    default=8765,
+    type=int,
+    metavar='PORT',
+    help='Port to listen on.',
+)
+@click.option(
+    '--certfile',
+    default=None,
+    metavar='PATH',
+    help='Certificate file for serving with TLS.',
+)
+@click.option(
+    '--keyfile',
+    default=None,
+    metavar='PATH',
+    help='Private key file associated with the certfile.',
+)
+@click.option(
+    '--log-dir',
+    default=None,
+    metavar='PATH',
+    help='Write server logs to this directory.',
+)
+@click.option(
+    '--log-level',
+    default='INFO',
+    type=click.Choice(
+        ['CRITICAL', 'ERROR', 'WARNING', 'INFO', 'DEBUG'],
+        case_sensitive=False,
+    ),
+    help='Minimum logging level.',
+)
+def cli(
+    host: str,
+    port: int,
+    certfile: str | None,
+    keyfile: str | None,
+    log_dir: str | None,
+    log_level: str,
+) -> None:
+    """Run a relay server instance.
 
-       $ signaling-server {options}
-       $ signaling-server --help
+    The relay server is used by clients to establish peer-to-peer
+    WebRTC connections.
     """
-    parser = argparse.ArgumentParser(
-        'Websocket-based Signaling Server',
-        formatter_class=argparse.ArgumentDefaultsHelpFormatter,
-    )
-    parser.add_argument(
-        '--host',
-        default='0.0.0.0',
-        help='host to listen on',
-    )
-    parser.add_argument(
-        '--port',
-        default=8765,
-        type=int,
-        help='port to listen on',
-    )
-    parser.add_argument(
-        '--certfile',
-        default=None,
-        help='certificate file for serving with TLS',
-    )
-    parser.add_argument(
-        '--keyfile',
-        default=None,
-        help='private key file associated with the certificate file',
-    )
-    parser.add_argument(
-        '--log-dir',
-        default=None,
-        help='write logs named server.log.{timestamp} to this dir',
-    )
-    parser.add_argument(
-        '--log-level',
-        choices=['CRITICAL', 'ERROR', 'WARNING', 'INFO', 'DEBUG'],
-        default='INFO',
-        help='logging level',
-    )
-    args = parser.parse_args(argv)
-
     handlers: list[logging.Handler] = [logging.StreamHandler(sys.stdout)]
-    if args.log_dir is not None:
-        os.makedirs(args.log_dir, exist_ok=True)
+    if log_dir is not None:
+        os.makedirs(log_dir, exist_ok=True)
         handlers.append(
             logging.handlers.TimedRotatingFileHandler(
-                os.path.join(args.log_dir, 'server.log'),
+                os.path.join(log_dir, 'server.log'),
                 # Rotate logs Sunday at midnight
                 when='W6',
                 atTime=datetime.time(hour=0, minute=0, second=0),
             ),
         )
 
     logging.basicConfig(
         format=(
             '[%(asctime)s.%(msecs)03d] %(levelname)-5s (%(name)s) :: '
             '%(message)s'
         ),
         datefmt='%Y-%m-%d %H:%M:%S',
-        level=args.log_level,
+        level=log_level,
         handlers=handlers,
     )
 
-    asyncio.run(
-        serve(
-            args.host,
-            args.port,
-            certfile=args.certfile,
-            keyfile=args.keyfile,
-        ),
-    )
-
-    return 0
-
-
-if __name__ == '__main__':
-    raise SystemExit(main())
+    asyncio.run(serve(host, port, certfile=certfile, keyfile=keyfile))
```

### Comparing `proxystore-0.4.1a1/proxystore/p2p/task.py` & `proxystore-0.5.0/proxystore/p2p/task.py`

 * *Files 14% similar despite different names*

```diff
@@ -31,29 +31,29 @@
     coro: Callable[..., Coroutine[Any, Any, None]],
     *args: Any,
     **kwargs: Any,
 ) -> asyncio.Task[Any]:
     """Run a coroutine safely in the background.
 
     Launches the coroutine as an asyncio task and sets the done
-    callback to :func:`exit_on_error() <.exit_on_error()>`. This is "safe"
-    because it will ensure exceptions inside the task get logged and cause
-    the program to exit. Otherwise, background tasks that are not awaited
-    may not have their exceptions raised such that programs hang with no
-    notice of the exception that caused the hang.
+    callback to [`exit_on_error()`][proxystore.p2p.task.exit_on_error].
+    This is "safe" because it will ensure exceptions inside the task get logged
+    and cause the program to exit. Otherwise, background tasks that are not
+    awaited may not have their exceptions raised such that programs hang with
+    no notice of the exception that caused the hang.
 
-    Tasks can raise :class:`SafeTaskExit <SafeTaskExit>` to signal the task
-    is finished but should not cause a system exit.
+    Tasks can raise [`SafeTaskExit`][proxystore.p2p.task.SafeTaskExitError] to
+    signal the task is finished but should not cause a system exit.
 
-    Source: `<https://stackoverflow.com/questions/62588076>`_
+    Source: https://stackoverflow.com/questions/62588076
 
     Args:
-        coro (Coroutine): coroutine to run as task.
-        args (list): positional arguments for the coroutine.
-        kwargs (dict): keyword arguments for the coroutine.
+        coro: Coroutine to run as task.
+        args: Positional arguments for the coroutine.
+        kwargs: Keyword arguments for the coroutine.
 
     Returns:
-        asyncio task handle.
+        Asyncio task handle.
     """
     task = asyncio.create_task(coro(*args, **kwargs))
     task.add_done_callback(exit_on_error)
     return task
```

### Comparing `proxystore-0.4.1a1/proxystore/serialize.py` & `proxystore-0.5.0/proxystore/serialize.py`

 * *Files 11% similar despite different names*

```diff
@@ -13,24 +13,26 @@
     pass
 
 
 def serialize(obj: Any) -> bytes:
     """Serialize object.
 
     Objects are serialized using
-    `pickle <https://docs.python.org/3/library/pickle.html>`_ (protocol 4)
-    except for ``bytes`` or ``str`` objects.
-    If pickle fails, `cloudpickle <https://github.com/cloudpipe/cloudpickle>`_
+    [pickle](https://docs.python.org/3/library/pickle.html){target=_blank}
+    (protocol 4) except for [bytes][] or [str][] objects.
+    If pickle fails,
+    [cloudpickle](https://github.com/cloudpipe/cloudpickle){target=_blank}
     is used as a fallback.
 
     Args:
-        obj: object to serialize.
+        obj: Object to serialize.
 
     Returns:
-        ``bytes`` that can be passed to :py:func:`~deserialize`.
+        Bytes that can be passed to \
+        [`deserialize()`][proxystore.serialize.deserialize].
     """
     if isinstance(obj, bytes):
         identifier = b'01\n'
     elif isinstance(obj, str):
         identifier = b'02\n'
         obj = obj.encode()
     else:
@@ -50,27 +52,27 @@
     return identifier + obj
 
 
 def deserialize(data: bytes) -> Any:
     """Deserialize object.
 
     Args:
-        data (bytes): bytes produced by :py:func:`~serialize`.
+        data: Bytes produced by
+            [`serialize()`][proxystore.serialize.serialize].
 
     Returns:
-        deserialized object.
+        The deserialized object.
 
     Raises:
-        ValueError:
-            if ``data`` is not of type ``bytes``.
-        SerializationError:
-            if the identifier of ``data`` is missing or invalid.
-            The identifier is prepended to the string in
-            :py:func:`~serialize` to indicate which serialization method was
-            used (e.g., no serialization, pickle, etc.).
+        ValueError: If `data` is not of type `bytes`.
+        SerializationError: If the identifier of `data` is missing or
+            invalid. The identifier is prepended to the string in
+            [`serialize()`][proxystore.serialize.serialize] to indicate which
+            serialization method was used (e.g., no serialization, pickle,
+            etc.).
     """
     if not isinstance(data, bytes):
         raise ValueError(
             f'Expected data to be of type bytes, not {type(data)}.',
         )
     identifier, separator, data = data.partition(b'\n')
     if separator == b'' or len(identifier) != len(b'00'):
```

### Comparing `proxystore-0.4.1a1/proxystore/store/cache.py` & `proxystore-0.5.0/proxystore/store/cache.py`

 * *Files 16% similar despite different names*

```diff
@@ -5,26 +5,24 @@
 from typing import TypeVar
 
 KeyT = TypeVar('KeyT')
 ValueT = TypeVar('ValueT')
 
 
 class LRUCache(Generic[KeyT, ValueT]):
-    """Simple LRU Cache."""
+    """Simple LRU Cache.
 
-    def __init__(self, maxsize: int = 16) -> None:
-        """Init LRUCache.
+    Args:
+        maxsize: Maximum number of value to cache.
 
-        Args:
-            maxsize (int): maximum number of value to cache (default: 16).
+    Raises:
+        ValueError: If `maxsize <= 0`.
+    """
 
-        Raises:
-            ValueError:
-                if `maxsize <= 0`.
-        """
+    def __init__(self, maxsize: int = 16) -> None:
         if maxsize < 0:
             raise ValueError('Cache size must by >= 0')
         self.maxsize = maxsize
         self.data: dict[KeyT, ValueT] = {}
         self.lru: list[KeyT] = []
 
         # Count hits/misses
```

### Comparing `proxystore-0.4.1a1/proxystore/store/dim/margo.py` & `proxystore-0.5.0/proxystore/connectors/dim/margo.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,44 +1,48 @@
-"""MargoStore implementation."""
+"""Margo RPC-based distributed in-memory connector implementation."""
 from __future__ import annotations
 
+import atexit
 import logging
+import multiprocessing
+import os
+import sys
+import time
+import uuid
 from enum import Enum
-from multiprocessing import Process
-from os import getpid
+from types import TracebackType
 from typing import Any
-from typing import NamedTuple
+from typing import Sequence
+
+if sys.version_info >= (3, 11):  # pragma: >=3.11 cover
+    from typing import Self
+else:  # pragma: <3.11 cover
+    from typing_extensions import Self
 
 try:
     import pymargo
     import pymargo.bulk as bulk
     from pymargo.bulk import Bulk
-    from pymargo.core import Address
     from pymargo.core import Engine
     from pymargo.core import Handle
     from pymargo.core import MargoException
-    from pymargo.core import RemoteFunction
 
     pymargo_import_error = None
 except ImportError as e:  # pragma: no cover
     pymargo_import_error = e
 
-
-import proxystore.utils as utils
+from proxystore.connectors.dim.exceptions import ServerTimeoutError
+from proxystore.connectors.dim.models import DIMKey
+from proxystore.connectors.dim.models import RPC
+from proxystore.connectors.dim.models import RPCResponse
+from proxystore.connectors.dim.utils import get_ip_address
 from proxystore.serialize import deserialize
 from proxystore.serialize import serialize
-from proxystore.store.base import Store
-from proxystore.store.dim.utils import get_ip_address
-from proxystore.store.dim.utils import Status
 
-server_process: Process | None = None
-client_pids: set[int] = set()
 logger = logging.getLogger(__name__)
-engine: Engine | None = None
-_rpcs: dict[str, RemoteFunction]
 
 
 class Protocol(Enum):
     """Available Mercury plugins and transports."""
 
     OFI_TCP = 'ofi+tcp'
     """libfabric tcp provider (TCP/IP)"""
@@ -52,410 +56,566 @@
     """UCX Verbs"""
     SM_SHM = 'sm+shm'
     """Shared memory shm"""
     BMI_TCP = 'bmi+tcp'
     """BMI tcp module (TCP/IP)"""
 
 
-class MargoStoreKey(NamedTuple):
-    """Key to objects in a MargoStore."""
+class MargoConnector:
+    """Margo RPC-based distributed in-memory connector.
 
-    margo_key: str
-    """Unique object key."""
-    obj_size: int
-    """Object size in bytes."""
-    peer: str
-    """Peer where object is located."""
-
-
-class MargoStore(Store[MargoStoreKey]):
-    """MargoStore implementation for intrasite communication."""
-
-    host: str
-    addr: str
-    protocol: Protocol
-    engine: Engine
-    _mochi_addr: Address
-    _rpcs: dict[str, RemoteFunction]
-    _pid: int
+    Note:
+        The first instance of this connector created on a process will
+        spawn a [`MargoServer`][proxystore.connectors.dim.margo.MargoServer]
+        that will store data. Hence, this connector just acts as an interface
+        to that server.
+
+    Args:
+        port: The desired port for the spawned server.
+        protocol: The communication protocol to use.
+        address: The network IP to use for transfer. Has precedence over `interface`
+            if both are provided.
+        interface: The network interface to use. `addr` has precedence over
+            this attribute if both are provided.
+        timeout: Timeout in seconds to try connecting to a local server before
+            spawning one.
+
+    Raises:
+        ServerTimeoutError: If a local server cannot be connected to within
+            `timeout` seconds, and a new local server does not respond within
+            `timeout` seconds after being started.
+    """
 
-    # TODO : make host optional and try to get infiniband path automatically
     def __init__(
         self,
-        name: str,
-        *,
-        interface: str,
         port: int,
-        protocol: Protocol = Protocol.OFI_VERBS,
-        cache_size: int = 16,
-        stats: bool = False,
+        protocol: Protocol | str,
+        address: str | None = None,
+        interface: str | None = None,
+        timeout: float = 1,
     ) -> None:
-        """Initialize a Margo client to issue RPCs to the Margo server.
-
-        This client will initialize a local Margo server (Peer service) that
-        it will store data to.
-
-        Args:
-            name (str): name of the store instance.
-            interface (str): The network interface to use
-            port (int): the desired port for the Margo server
-            protocol (str): The communication protocol to use
-                            (e.g., tcp, sockets, verbs). default = "verbs"
-            cache_size (int): size of LRU cache (in # of objects). If 0,
-                the cache is disabled. The cache is local to the Python
-                process (default: 16).
-            stats (bool): collect stats on store operations (default: False).
-        """
-        global server_process
-        global client_pids
-        global engine
-        global _rpcs
-
-        # raise error if modules not properly loaded
+        # Py-Mochi-Margo is not a required dependency and requires the user
+        # to install it themselves.
         if pymargo_import_error is not None:  # pragma: no cover
             raise pymargo_import_error
 
-        self.protocol = protocol
-
-        self.host = get_ip_address(interface)
+        self._address = address
+        self._interface = interface
         self.port = port
+        self.protocol = (
+            protocol if isinstance(protocol, str) else protocol.value
+        )
+
+        self.timeout = timeout
 
-        self.addr = f'{self.protocol}://{self.host}:{port}'
+        self.engine = Engine(
+            self.protocol,
+            mode=pymargo.client,
+            use_progress_thread=True,
+        )
+
+        if self._address is not None:
+            self.address = self._address
+        elif self._interface is not None:  # pragma: darwin no cover
+            self.address = get_ip_address(self._interface)
+        else:
+            eng_url = str(self.engine.addr())
+            self.address = eng_url.split(':')[1].split('/')[2]
+
+        self.url = f'{self.protocol}://{self.address}:{self.port}'
+
+        self._rpcs = {
+            'evict': self.engine.register('evict'),
+            'exists': self.engine.register('exists'),
+            'get': self.engine.register('get'),
+            'put': self.engine.register('put'),
+        }
 
-        if server_process is None:
-            server_process = Process(target=self._start_server)
-            server_process.start()
-
-        if engine is None:
-            # start client
-            engine = Engine(
+        self.server: multiprocessing.context.SpawnProcess | None
+        try:
+            logger.info(
+                f'Connecting to local server (address={self.url})...',
+            )
+            wait_for_server(
                 self.protocol,
-                mode=pymargo.client,
-                use_progress_thread=True,
+                self.address,
+                self.port,
+                self.timeout,
+            )
+            logger.info(
+                f'Connected to local server (address={self.url})',
             )
+        except ServerTimeoutError:
+            logger.info(
+                'Failed to connect to local server '
+                f'(address={self.url}, timeout={self.timeout})',
+            )
+            self.server = spawn_server(
+                self.protocol,
+                self.address,
+                self.port,
+                spawn_timeout=self.timeout,
+            )
+            logger.info(f'Spawned local server (address={self.url})')
+        else:
+            self.server = None
 
-            _rpcs = {
-                'set': engine.register('set'),
-                'get': engine.register('get'),
-                'exists': engine.register('exists'),
-                'evict': engine.register('evict'),
-            }
+    def __enter__(self) -> Self:
+        return self
 
-        self.engine = engine
-        self._rpcs = _rpcs
+    def __exit__(
+        self,
+        exc_type: type[BaseException] | None,
+        exc_value: BaseException | None,
+        exc_traceback: TracebackType | None,
+    ) -> None:
+        self.close()
 
-        self.server_started()
+    def _send_rpcs(self, rpcs: Sequence[RPC]) -> list[RPCResponse]:
+        """Send an RPC request to the server.
 
-        self._pid = getpid()
-        client_pids.add(self._pid)
+        Args:
+            rpcs: List of RPCs to invoke on local server.
 
-        super().__init__(
-            name,
-            cache_size=cache_size,
-            stats=stats,
-            kwargs={
-                'interface': interface,
-                'port': self.port,
-                'protocol': self.protocol,
-            },
-        )
+        Returns:
+            List of RPC responses.
 
-    def _start_server(self) -> None:
-        """Launch the local Margo server (Peer) process."""
-        logger.info(f'starting server {self.addr}')
-        server_engine = Engine(self.addr)
-
-        logger.info(f'Server running at address {str(server_engine.addr())}')
-
-        server_engine.on_finalize(when_finalize)
-        server_engine.enable_remote_shutdown()
-
-        # create server
-        receiver = MargoServer(server_engine)
-        server_engine.register('get', receiver.get)
-        server_engine.register('set', receiver.set)
-        server_engine.register('exists', receiver.exists)
-        server_engine.register('evict', receiver.evict)
-        server_engine.wait_for_finalize()
-
-    def server_started(self) -> None:  # pragma: no cover
-        """Loop until server has started."""
-        logger.debug('Checking if server has started')
-        while True:
-            assert engine is not None
-            try:
-                self._mochi_addr = engine.lookup(self.addr)
-                break
-            except MargoException:
-                pass
-
-    def create_key(self, obj: Any) -> MargoStoreKey:
-        return MargoStoreKey(
-            margo_key=utils.create_key(obj),
-            obj_size=len(obj),
-            peer=self.addr,
-        )
+        Raises:
+            Exception: Any exception returned by the local server.
+        """
+        responses = []
 
-    def evict(self, key: MargoStoreKey) -> None:
-        logger.debug(f'Client issuing an evict request on key {key}')
-        self.call_rpc_on(
-            self.engine,
-            key.peer,
-            self._rpcs['evict'],
-            '',
-            key.margo_key,
-            0,
-        )
+        for rpc in rpcs:
+            url = f'{self.protocol}://{rpc.key.peer_host}:{rpc.key.peer_port}'
+            server_url = self.engine.lookup(url)
+            logger.debug(
+                f'Sent {rpc.operation.upper()} RPC (key={rpc.key})',
+            )
+            result = self._rpcs[rpc.operation].on(server_url)(
+                rpc.data,
+                rpc.key.size,
+                rpc.key,
+            )
 
-        self._cache.evict(key)
+            response = deserialize(result)
+            logger.debug(
+                f'Received {rpc.operation.upper()} RPC response '
+                f'(key={response.key}, '
+                f'exception={response.exception is not None})',
+            )
 
-    def exists(self, key: MargoStoreKey) -> bool:
-        logger.debug(f'Client issuing an exists request on key {key}')
-        buff = bytearray(4)  # equivalent to malloc
+            if response.exception is not None:
+                raise response.exception
 
-        blk = self.engine.create_bulk(buff, bulk.write_only)
+            assert rpc.operation == response.operation
+            assert rpc.key == response.key
 
-        self.call_rpc_on(
-            self.engine,
-            key.peer,
-            self._rpcs['exists'],
-            blk,
-            key.margo_key,
-            len(buff),
-        )
+            responses.append(response)
 
-        return bool(int(deserialize(bytes(buff))))
+        return responses
 
-    def get_bytes(self, key: MargoStoreKey) -> bytes | None:
-        logger.debug(f'Client issuing get request on key {key}')
+    def close(self, kill_server: bool = True) -> None:
+        """Close the connector.
 
-        buff = bytearray(key.obj_size)
-        blk = self.engine.create_bulk(buff, bulk.read_write)
-        s = self.call_rpc_on(
-            self.engine,
-            key.peer,
-            self._rpcs['get'],
-            blk,
-            key.margo_key,
-            key.obj_size,
-        )
+        Args:
+            kill_server: Whether to kill the server process. If this instance
+                did not spawn the local node's server process, this is a
+                no-op.
+        """
+        if kill_server and self.server is not None:
+            self.engine.lookup(self.url).shutdown()
+            self.server.join()
+            logger.info(
+                'Terminated local server on connector close '
+                f'(pid={self.server.pid})',
+            )
 
-        if not s.success:
-            logger.error(f'{s.error}')
-            return None
-        return bytes(buff)
-
-    def set_bytes(self, key: MargoStoreKey, data: bytes) -> None:
-        logger.debug(f'Client {self.addr} issuing set request on key {key}')
-        blk = self.engine.create_bulk(data, bulk.read_only)
-        self.call_rpc_on(
-            self.engine,
-            self.addr,
-            self._rpcs['set'],
-            blk,
-            key.margo_key,
-            key.obj_size,
-        )
+        self.engine.finalize()
+        logger.info('Closed Margo connector')
 
-    def close(self) -> None:
-        """Terminate Peer server process."""
-        global server_process
-        global client_pids
-        global engine
-
-        client_pids.discard(self._pid)
-
-        logger.info('Clean up requested')
-
-        if len(client_pids) == 0 and server_process is not None:
-            engine = None
-            self._mochi_addr.shutdown()
-            self.engine.finalize()
-            server_process.join()
-            server_process = None
+    def config(self) -> dict[str, Any]:
+        """Get the connector configuration.
+
+        The configuration contains all the information needed to reconstruct
+        the connector object.
+        """
+        return {
+            'address': self._address,
+            'interface': self._interface,
+            'port': self.port,
+            'protocol': self.protocol,
+            'timeout': self.timeout,
+        }
+
+    @classmethod
+    def from_config(cls, config: dict[str, Any]) -> MargoConnector:
+        """Create a new connector instance from a configuration.
+
+        Args:
+            config: Configuration returned by `#!python .config()`.
+        """
+        return cls(**config)
+
+    def evict(self, key: DIMKey) -> None:
+        """Evict the object associated with the key.
+
+        Args:
+            key: Key associated with object to evict.
+        """
+        rpc = RPC(operation='evict', key=key)
+        self._send_rpcs([rpc])
 
-    @staticmethod
-    def call_rpc_on(
-        engine: Engine,
-        addr: str,
-        rpc: RemoteFunction,
-        array_str: Bulk,
-        key: str,
-        size: int,
-    ) -> Status:
-        """Initiate the desired RPC call on the specified provider.
-
-        Arguments:
-            engine (Engine): The client-side engine
-            addr (str): The address of Margo provider to access
-                        (e.g. tcp://172.21.2.203:6367)
-            rpc (RemoteFunction): the rpc to issue to the server
-            array_str (Bulk): the serialized data/buffer to send
-                             to the server.
-            key (str): the identifier of the data stored on the server
-            size (int): the size of the the data
+    def exists(self, key: DIMKey) -> bool:
+        """Check if an object associated with the key exists.
+
+        Args:
+            key: Key potentially associated with stored object.
 
         Returns:
-            A string denoting whether the communication was successful
+            If an object associated with the key exists.
+        """
+        rpc = RPC(operation='exists', key=key)
+        (response,) = self._send_rpcs([rpc])
+        assert response.exists is not None
+        return response.exists
 
+    def get(self, key: DIMKey) -> bytes | None:
+        """Get the serialized object associated with the key.
+
+        Args:
+            key: Key associated with the object to retrieve.
+
+        Returns:
+            Serialized object or `None` if the object does not exist.
         """
-        server_addr = engine.lookup(addr)
-        return deserialize(rpc.on(server_addr)(array_str, size, key))
+        buff = bytearray(key.size)
+        blk = self.engine.create_bulk(buff, bulk.write_only)
 
+        rpc = RPC(operation='get', key=key, data=blk)
+        (result,) = self._send_rpcs([rpc])
 
-class MargoServer:
-    """MargoServer implementation."""
+        if result.exists:
+            return bytes(buff)
 
-    data: dict[str, bytes]
-    engine: Engine
+        return None
 
-    def __init__(self, engine: Engine) -> None:
-        """Initialize the server and register all RPC calls.
+    def get_batch(self, keys: Sequence[DIMKey]) -> list[bytes | None]:
+        """Get a batch of serialized objects associated with the keys.
 
         Args:
-            engine (Engine): the server engine created at the
-                      specified network address
+            keys: Sequence of keys associated with objects to retrieve.
 
+        Returns:
+            List with same order as `keys` with the serialized objects or \
+            `None` if the corresponding key does not have an associated object.
         """
-        self.data = {}
+        rpcs: list[RPC] = []
+        buffers: list[bytearray] = []
 
-        self.engine = engine
+        for key in keys:
+            buff = bytearray(key.size)
+            blk = self.engine.create_bulk(buff, bulk.write_only)
+
+            buffers.append(buff)
+            rpcs.append(RPC(operation='get', key=key, data=blk))
+
+        responses = self._send_rpcs(rpcs)
+        return [
+            bytes(b) if responses[i].exists else None
+            for i, b in enumerate(buffers)
+        ]
+
+    def put(self, obj: bytes) -> DIMKey:
+        """Put a serialized object in the store.
 
-        logger.debug('Server initialized')
+        Args:
+            obj: Serialized object to put in the store.
 
-    def set(
+        Returns:
+            Key which can be used to retrieve the object.
+        """
+        key = DIMKey(
+            dim_type='margo',
+            obj_id=str(uuid.uuid4()),
+            size=len(obj),
+            peer_host=self.address,
+            peer_port=self.port,
+        )
+        blk = self.engine.create_bulk(obj, bulk.read_only)
+
+        rpc = RPC(operation='put', key=key, data=blk)
+        self._send_rpcs([rpc])
+        return key
+
+    def put_batch(self, objs: Sequence[bytes]) -> list[DIMKey]:
+        """Put a batch of serialized objects in the store.
+
+        Args:
+            objs: Sequence of serialized objects to put in the store.
+
+        Returns:
+            List of keys with the same order as `objs` which can be used to \
+            retrieve the objects.
+        """
+        keys = [
+            DIMKey(
+                dim_type='margo',
+                obj_id=str(uuid.uuid4()),
+                size=len(obj),
+                peer_host=self.address,
+                peer_port=self.port,
+            )
+            for obj in objs
+        ]
+        rpcs: list[RPC] = []
+
+        for key, obj in zip(keys, objs):
+            blk = self.engine.create_bulk(obj, bulk.read_only)
+            rpcs.append(RPC(operation='put', key=key, data=blk))
+
+        self._send_rpcs(rpcs)
+
+        return keys
+
+
+class MargoServer:
+    """MargoServer implementation."""
+
+    def __init__(self, engine: Engine) -> None:
+        self.data: dict[str, bytes] = {}
+        self.engine = engine
+
+    def evict(
         self,
         handle: Handle,
         bulk_str: Bulk,
         bulk_size: int,
-        key: str,
+        key: DIMKey,
     ) -> None:
-        """Obtain data from the client and store it in local dictionary.
+        """Remove key from local dictionary.
 
         Args:
-            handle (Handle): the client handle
-            bulk_str (Bulk): the buffer containing the data to be shared
-            bulk_size (int): the size of the data being transferred
-            key (str): the data key
+            handle: The client handle.
+            bulk_str: The buffer that will store shared data.
+            bulk_size: The size of the data to be received.
+            key: The data's key.
         """
-        logger.debug(f'Received set RPC for key {key}.')
+        self.data.pop(key.obj_id, None)
+        response = RPCResponse(operation='evict', key=key)
+        handle.respond(serialize(response))
 
-        s = Status(True, None)
-
-        local_buffer = bytearray(bulk_size)
-        local_bulk = self.engine.create_bulk(local_buffer, bulk.write_only)
-        self.engine.transfer(
-            bulk.pull,
-            handle.get_addr(),
-            bulk_str,
-            0,
-            local_bulk,
-            0,
-            bulk_size,
-        )
-        self.data[key] = local_buffer
+    def exists(
+        self,
+        handle: Handle,
+        bulk_str: Bulk,
+        bulk_size: int,
+        key: DIMKey,
+    ) -> None:
+        """Check if key exists within local dictionary.
 
-        handle.respond(serialize(s))
+        Args:
+            handle: The client handle.
+            bulk_str: The buffer that will store shared data.
+            bulk_size: The size of the data to be received.
+            key: The data's key.
+        """
+        exists = key.obj_id in self.data
+        response = RPCResponse(operation='exists', key=key, exists=exists)
+        handle.respond(serialize(response))
 
     def get(
         self,
         handle: Handle,
         bulk_str: Bulk,
         bulk_size: int,
-        key: str,
+        key: DIMKey,
     ) -> None:
         """Return data at a given key back to the client.
 
         Args:
-            handle (Handle): The client handle
-            bulk_str (Bulk): the buffer that will store shared data
-            bulk_size (int): the size of the data to be received
-            key (str): the data's key
-
+            handle: The client handle.
+            bulk_str: The buffer that will store shared data.
+            bulk_size: The size of the data to be received.
+            key: The data's key.
         """
-        logger.debug(f'Received get RPC for key {key}.')
-
-        s = Status(True, None)
-
-        try:
-            local_array = self.data[key]
+        local_array = self.data.get(key.obj_id, None)
+        if local_array is not None:
             local_bulk = self.engine.create_bulk(local_array, bulk.read_only)
             self.engine.transfer(
                 bulk.push,
                 handle.get_addr(),
                 bulk_str,
                 0,
                 local_bulk,
                 0,
                 bulk_size,
             )
-        except KeyError as error:
-            logger.error(f'key {error} not found.')
-            s = Status(False, error)
-
-        handle.respond(serialize(s))
+            response = RPCResponse(operation='get', key=key, exists=True)
+        else:
+            response = RPCResponse(operation='get', key=key, exists=False)
+        handle.respond(serialize(response))
 
-    def evict(
+    def put(
         self,
         handle: Handle,
-        bulk_str: str,
+        bulk_str: Bulk,
         bulk_size: int,
-        key: str,
+        key: DIMKey,
     ) -> None:
-        """Remove key from local dictionary.
+        """Obtain data from the client and store it in local dictionary.
 
         Args:
-            handle (Handle): the client issuing the requests' handle
-            bulk_str (str): the buffer containing any data to be shared
-            bulk_size (int): the size of the data to share
-            key (str): the identifier of the data
-
+            handle: The client handle.
+            bulk_str: The buffer containing the data to be shared.
+            bulk_size: The size of the data being transferred.
+            key: The data key.
         """
-        logger.debug(f'Received exists RPC for key {key}')
-
-        self.data.pop(key, None)
-        s = Status(True, None)
-
-        handle.respond(serialize(s))
-
-    def exists(
-        self,
-        handle: Handle,
-        bulk_str: str,
-        bulk_size: int,
-        key: str,
-    ) -> None:
-        """Check if key exists within local dictionary.
-
-        Args:
-            handle (Handle): the client issuing the requests' handle
-            bulk_str (str): the shared buffer
-            bulk_size (int): the size of the shared buffer
-            key (str): the identifier of the data
-
-        """
-        logger.debug(f'Received exists RPC for key {key}')
-
-        s = Status(True, None)
-
-        # converting to int then string because length appears to be 7 for
-        # True with pickle protocol 4 and cannot always guarantee that that
-        # protocol will be selected
-        local_array = serialize(str(int(key in self.data)))
-        local_bulk = self.engine.create_bulk(local_array, bulk.read_only)
-        size = len(local_array)
+        local_buffer = bytearray(bulk_size)
+        local_bulk = self.engine.create_bulk(local_buffer, bulk.write_only)
         self.engine.transfer(
-            bulk.push,
+            bulk.pull,
             handle.get_addr(),
             bulk_str,
             0,
             local_bulk,
             0,
-            size,
+            bulk_size,
         )
+        self.data[key.obj_id] = local_buffer
 
-        handle.respond(serialize(s))
+        response = RPCResponse(operation='put', key=key)
+        handle.respond(serialize(response))
 
 
-def when_finalize() -> None:
-    """Print a statement advising that engine finalization was triggered."""
-    logger.info('Finalize was called. Cleaning up.')
+def _when_finalize() -> None:
+    logger.info(f'Margo server finalized (pid={os.getpid()})')
+
+
+def start_server(url: str) -> None:
+    """Start and wait on a Margo server.
+
+    Args:
+        url: URL of the engine that will be started. Should take
+            the form `{protocol}://{host}:{port}`.
+    """
+    server_engine = Engine(url)
+    server_engine.on_finalize(_when_finalize)
+    server_engine.enable_remote_shutdown()
+
+    receiver = MargoServer(server_engine)
+    server_engine.register('evict', receiver.evict)
+    server_engine.register('exists', receiver.exists)
+    server_engine.register('get', receiver.get)
+    server_engine.register('put', receiver.put)
+    server_engine.wait_for_finalize()
+
+
+def spawn_server(
+    protocol: str,
+    address: str,
+    port: int,
+    *,
+    spawn_timeout: float = 5.0,
+    kill_timeout: float | None = 1.0,
+) -> multiprocessing.context.SpawnProcess:
+    """Spawn a local server running in a separate process.
+
+    Note:
+        An `atexit` callback is registered which will terminate the spawned
+        server process when the calling process exits.
+
+    Args:
+        protocol: Communication protocol.
+        address: Host IP of the server to wait on.
+        port: Port of the server to wait on.
+        spawn_timeout: Max time in seconds to wait for the server to start.
+        kill_timeout: Max time in seconds to wait for the server to shutdown
+            on exit.
+
+    Returns:
+        The process that the server is running in.
+    """
+    url = f'{protocol}://{address}:{port}'
+
+    ctx = multiprocessing.get_context('spawn')
+    server_process = ctx.Process(
+        target=start_server,
+        args=(url,),
+    )
+    server_process.start()
+
+    def _kill_on_exit() -> None:  # pragma: no cover
+        server_process.terminate()
+        server_process.join(timeout=kill_timeout)
+        if server_process.is_alive():
+            server_process.kill()
+            server_process.join()
+        logger.debug(
+            'Server terminated on parent process exit '
+            f'(pid={server_process.pid})',
+        )
+
+    atexit.register(_kill_on_exit)
+    logger.debug('Registered server cleanup atexit callback')
+
+    wait_for_server(protocol, address, port, timeout=spawn_timeout)
+    logger.debug(
+        f'Server started (address={url}, pid={server_process.pid})',
+    )
+
+    return server_process
+
+
+def wait_for_server(
+    protocol: str,
+    address: str,
+    port: int,
+    timeout: float = 0.1,
+) -> None:
+    """Wait until the server responds.
+
+    Warning:
+        Due to how Margo blocks internally, the timeout is not very accurate.
+
+    Args:
+        protocol: Communication protocol.
+        address: Host IP of the server to wait on.
+        port: Port of the server to wait on.
+        timeout: The max time in seconds to wait for server response.
+
+    Raises:
+        ServerTimeoutError: If the server does not respond within the timeout.
+    """
+    engine = Engine(protocol, mode=pymargo.client, use_progress_thread=True)
+    remote_function = engine.register('exists')
+    key = DIMKey(
+        'margo',
+        obj_id='ping',
+        size=0,
+        peer_host=address,
+        peer_port=port,
+    )
+    rpc = RPC('exists', key=key)
+    url = f'{protocol}://{address}:{port}'
+
+    sleep_time = 0.01
+    start = time.time()
+    while time.time() - start < timeout:
+        try:
+            local_url = engine.lookup(url)
+            result = remote_function.on(local_url)(
+                rpc.data,
+                rpc.key.size,
+                rpc.key,
+            )
+            response = deserialize(result)
+            assert response.exception is None
+            # We could call engine.finalize() now to be safe but Margo
+            # raises a _pymargo.MargoException: margo_addr_free() returned 11
+            # exception.
+            return
+        except MargoException:  # pragma: no cover
+            time.sleep(sleep_time)
+
+    raise ServerTimeoutError(
+        f'Failed to connect to server within timeout ({timeout} seconds).',
+    )
```

### Comparing `proxystore-0.4.1a1/proxystore/store/dim/ucx.py` & `proxystore-0.5.0/proxystore/connectors/dim/ucx.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,455 +1,599 @@
-"""UCXStore implementation."""
+"""UCX-based distributed in-memory connector implementation."""
 from __future__ import annotations
 
 import asyncio
+import atexit
 import logging
+import multiprocessing
 import signal
-from multiprocessing import Process
-from time import sleep
+import sys
+import uuid
+from types import TracebackType
 from typing import Any
-from typing import NamedTuple
+from typing import Sequence
+
+if sys.version_info >= (3, 11):  # pragma: >=3.11 cover
+    from typing import Self
+else:  # pragma: <3.11 cover
+    from typing_extensions import Self
 
 try:
     import ucp
 
     ucx_import_error = None
 except ImportError as e:  # pragma: no cover
     ucx_import_error = e
 
-import proxystore.utils as utils
+from proxystore.connectors.dim.exceptions import ServerTimeoutError
+from proxystore.connectors.dim.models import DIMKey
+from proxystore.connectors.dim.models import RPC
+from proxystore.connectors.dim.models import RPCResponse
 from proxystore.serialize import deserialize
-from proxystore.serialize import SerializationError
 from proxystore.serialize import serialize
-from proxystore.store.base import Store
-from proxystore.store.dim.utils import get_ip_address
-from proxystore.store.dim.utils import Status
-
-ENCODING = 'UTF-8'
 
-server_process = None
 logger = logging.getLogger(__name__)
 
 
-class UCXStoreKey(NamedTuple):
-    """Key to objects in a MargoStore."""
+class UCXConnector:
+    """UCX-based distributed in-memory connector.
+
+    Note:
+        The first instance of this connector created on a process will
+        spawn a [`UCXServer`][proxystore.connectors.dim.ucx.UCXServer]
+        that will store data. Hence, this connector just acts as an interface
+        to that server.
 
-    ucx_key: str
-    """Unique object key."""
-    obj_size: int
-    """Object size in bytes."""
-    peer: str
-    """Peer where object is located."""
-
-
-class UCXStore(Store[UCXStoreKey]):
-    """Implementation for the client-facing component of UCXStore."""
-
-    addr: str
-    host: str
-    port: int
-    server: Process
-    _loop: asyncio.events.AbstractEventLoop
+    Args:
+        port: The desired port for the spawned server.
+        address: The IP address of the network interface to use.
+            Has precedence over `interface` if both are provided.
+        interface: The network interface to use.
+            `address` has precedence if both args are defined.
+        timeout: Timeout in seconds to try connecting to local server before
+            spawning one.
+
+    Raises:
+        ServerTimeoutError: If a local server cannot be connected to within
+            `timeout` seconds, and a new local server does not response within
+            `timeout` seconds after being started.
+    """
 
-    # TODO : make host optional and try to get infiniband path automatically
     def __init__(
         self,
-        name: str,
-        *,
-        interface: str,
         port: int,
-        cache_size: int = 16,
-        stats: bool = False,
+        address: str | None = None,
+        interface: str | None = None,
+        timeout: float = 1,
     ) -> None:
-        """Initialize a UCX client to issue RPCs to the UCX server.
-
-        This client will initialize a local UCX server (Peer service) to
-        store data to.
-
-        Args:
-            name (str): name of the store instance.
-            interface (str): The network interface to use
-            port (int): the desired port for the UCX server
-            cache_size (int): size of LRU cache (in # of objects). If 0,
-                the cache is disabled. The cache is local to the Python
-                process (default: 16).
-            stats (bool): collect stats on store operations (default: False).
-        """
-        global server_process
-
         if ucx_import_error is not None:  # pragma: no cover
             raise ucx_import_error
 
-        logger.debug('Instantiating client and server')
-
-        self.host = get_ip_address(interface)
+        self._address = address
+        self._interface = interface
         self.port = port
+        self.timeout = timeout
+
+        if self._address is not None:
+            self.address = self._address
+        elif self._interface is not None:
+            self.address = ucp.get_address(ifname=self._interface)
+        else:
+            self.address = ucp.get_address()
 
-        self.addr = f'{self.host}:{self.port}'
+        self.url = f'{self.address}:{self.port}'
+
+        self.server: multiprocessing.context.SpawnProcess | None
+        try:
+            logger.info(
+                f'Connecting to local server (URL={self.url})...',
+            )
+            wait_for_server(self.address, self.port, self.timeout)
+            logger.info(
+                f'Connected to local server (URL={self.url})',
+            )
+        except ServerTimeoutError:
+            logger.info(
+                'Failed to connect to local server '
+                f'(URL={self.url}, timeout={self.timeout})',
+            )
+            self.server = spawn_server(
+                self.address,
+                self.port,
+                spawn_timeout=self.timeout,
+            )
+            logger.info(f'Spawned local server (address={self.url})')
+        else:
+            self.server = None
 
         try:
             self._loop = asyncio.get_running_loop()
         except RuntimeError:
             self._loop = asyncio.new_event_loop()
 
-        if server_process is None:
-            server_process = Process(
-                target=launch_server,
-                args=(self.host, self.port),
-            )
-            server_process.start()
-            self._loop.run_until_complete(
-                wait_for_server(self.host, self.port),
-            )
+    def __enter__(self) -> Self:
+        return self
 
-        # TODO: Verify if create_endpoint error handling will successfully
-        # connect to endpoint or if error handling needs to be done here
+    def __exit__(
+        self,
+        exc_type: type[BaseException] | None,
+        exc_value: BaseException | None,
+        exc_traceback: TracebackType | None,
+    ) -> None:
+        self.close()
 
-        super().__init__(
-            name,
-            cache_size=cache_size,
-            stats=stats,
-            kwargs={'interface': interface, 'port': self.port},
-        )
+    async def _send_rpcs_async(self, rpcs: Sequence[RPC]) -> list[RPCResponse]:
+        responses = []
 
-    def create_key(self, obj: Any) -> UCXStoreKey:
-        return UCXStoreKey(
-            ucx_key=utils.create_key(obj),
-            obj_size=len(obj),
-            peer=self.addr,
-        )
+        for rpc in rpcs:
+            ep = await ucp.create_endpoint(
+                rpc.key.peer_host,
+                rpc.key.peer_port,
+            )
 
-    def evict(self, key: UCXStoreKey) -> None:
-        logger.debug(f'Client issuing an evict request on key {key}.')
+            message = serialize(rpc)
+            await ep.send_obj(message)
+            logger.debug(
+                f'Sent {rpc.operation.upper()} RPC (key={rpc.key})',
+            )
+            response = deserialize(bytes(await ep.recv_obj()))
 
-        event = serialize({'key': key.ucx_key, 'data': None, 'op': 'evict'})
-        self._loop.run_until_complete(self.handler(event, key.peer))
+            logger.debug(
+                f'Received {rpc.operation.upper()} RPC response '
+                f'(key={response.key}, '
+                'exception={response.exception is not None})',
+            )
 
-        self._cache.evict(key)
+            if response.exception is not None:
+                raise response.exception
 
-    def exists(self, key: UCXStoreKey) -> bool:
-        logger.debug(f'Client issuing an exists request on key {key}.')
+            assert rpc.operation == response.operation
+            assert rpc.key == response.key
 
-        event = serialize(
-            {'key': key.ucx_key, 'data': None, 'op': 'exists'},
-        )
-        return deserialize(
-            self._loop.run_until_complete(self.handler(event, key.peer)),
-        )
+            responses.append(response)
 
-    def get_bytes(self, key: UCXStoreKey) -> bytes | None:
-        res: bytes | None
-        logger.debug(f'Client issuing get request on key {key}.')
+            await ep.close()
 
-        event = serialize({'key': key.ucx_key, 'data': '', 'op': 'get'})
-        res = self._loop.run_until_complete(self.handler(event, key.peer))
+        return responses
 
-        try:
-            s = deserialize(res)
+    def _send_rpcs(self, rpcs: Sequence[RPC]) -> list[RPCResponse]:
+        """Send an RPC request to the server.
 
-            if isinstance(s, Status) and not s.success:
-                return None
-            return res
-        except SerializationError:
-            return res
+        Args:
+            rpcs: List of RPCs to invoke on local server.
 
-    def set_bytes(self, key: UCXStoreKey, data: bytes) -> None:
-        logger.debug(
-            f'Client issuing set request on key {key} with addr {self.addr}',
-        )
+        Returns:
+            List of RPC responses.
 
-        event = serialize({'key': key.ucx_key, 'data': data, 'op': 'set'})
+        Raises:
+            Exception: Any exception returned by the local server.
+        """
+        return self._loop.run_until_complete(self._send_rpcs_async(rpcs))
 
-        self._loop.run_until_complete(self.handler(event, self.addr))
+    def close(self, kill_server: bool = False) -> None:
+        """Close the connector.
 
-    async def handler(self, event: bytes, addr: str) -> bytes:
-        host = addr.split(':')[0]  # quick fix
-        port = int(addr.split(':')[1])
+        Args:
+            kill_server: Whether to kill the server process. If this instance
+                did not spawn the local node's server process, this is a
+                no-op.
+        """
+        if kill_server and self.server is not None:
+            self.server.terminate()
+            self.server.join()
+            logger.info(
+                'Terminated local server on connector close '
+                f'(pid={self.server.pid})',
+            )
 
-        ep = await ucp.create_endpoint(host, port)
+        logger.debug('Closed UCX connector')
 
-        await ep.send_obj(event)
+    def config(self) -> dict[str, Any]:
+        """Get the connector configuration.
 
-        res = await ep.recv_obj()
+        The configuration contains all the information needed to reconstruct
+        the connector object.
+        """
+        return {
+            'address': self._address,
+            'interface': self._interface,
+            'port': self.port,
+            'timeout': self.timeout,
+        }
+
+    @classmethod
+    def from_config(cls, config: dict[str, Any]) -> UCXConnector:
+        """Create a new connector instance from a configuration.
 
-        await ep.close()
+        Args:
+            config: Configuration returned by `#!python .config()`.
+        """
+        return cls(**config)
 
-        return bytes(res)  # returns bytearray by default
+    def evict(self, key: DIMKey) -> None:
+        """Evict the object associated with the key.
 
-    def close(self) -> None:
-        """Terminate Peer server process."""
-        global server_process
+        Args:
+            key: Key associated with object to evict.
+        """
+        rpc = RPC(operation='evict', key=key)
+        self._send_rpcs([rpc])
 
-        logger.info('Clean up requested')
+    def exists(self, key: DIMKey) -> bool:
+        """Check if an object associated with the key exists.
 
-        if server_process is not None:
-            server_process.terminate()
-            server_process.join()
-            server_process = None
+        Args:
+            key: Key potentially associated with stored object.
 
-        logger.debug('Clean up completed')
+        Returns:
+            If an object associated with the key exists.
+        """
+        rpc = RPC(operation='exists', key=key)
+        (response,) = self._send_rpcs([rpc])
+        assert response.exists is not None
+        return response.exists
 
+    def get(self, key: DIMKey) -> bytes | None:
+        """Get the serialized object associated with the key.
 
-class UCXServer:
-    """UCXServer implementation."""
+        Args:
+            key: Key associated with the object to retrieve.
 
-    host: str
-    port: int
-    ucp_listener: ucp.core.Listener | None
-    data: dict[str, bytes]
+        Returns:
+            Serialized object or `None` if the object does not exist.
+        """
+        rpc = RPC(operation='get', key=key)
+        (result,) = self._send_rpcs([rpc])
+        return result.data
 
-    def __init__(self, host: str, port: int) -> None:
-        """Initialize the server and register all RPC calls.
+    def get_batch(self, keys: Sequence[DIMKey]) -> list[bytes | None]:
+        """Get a batch of serialized objects associated with the keys.
 
         Args:
-            host (str): the server host
-            port (int): the server port
+            keys: Sequence of keys associated with objects to retrieve.
 
+        Returns:
+            List with same order as `keys` with the serialized objects or \
+            `None` if the corresponding key does not have an associated object.
         """
-        self.host = host
-        self.port = port
-        self.data = {}
-        self.ucp_listener = None
+        rpcs = [RPC(operation='get', key=key) for key in keys]
+        responses = self._send_rpcs(rpcs)
+        return [r.data for r in responses]
 
-    def set(self, key: str, data: bytes) -> Status:
-        """Obtain data from the client and store it in local dictionary.
+    def put(self, obj: bytes) -> DIMKey:
+        """Put a serialized object in the store.
 
         Args:
-            key (str): object key to use
-            data (bytes): data to store
+            obj: Serialized object to put in the store.
 
-        Returns (bytes):
-            That the operation has successfully completed
+        Returns:
+            Key which can be used to retrieve the object.
         """
-        self.data[key] = data
-        return Status(success=True, error=None)
+        key = DIMKey(
+            dim_type='ucx',
+            obj_id=str(uuid.uuid4()),
+            size=len(obj),
+            peer_host=self.address,
+            peer_port=self.port,
+        )
+        rpc = RPC(operation='put', key=key, data=obj)
+        self._send_rpcs([rpc])
+        return key
 
-    def get(self, key: str) -> bytes | Status:
-        """Return data at a given key back to the client.
+    def put_batch(self, objs: Sequence[bytes]) -> list[DIMKey]:
+        """Put a batch of serialized objects in the store.
 
         Args:
-            key (str): the object key
-
-        Returns (bytes):
-            The data associated with provided key
+            objs: Sequence of serialized objects to put in the store.
 
+        Returns:
+            List of keys with the same order as `objs` which can be used to \
+            retrieve the objects.
         """
-        try:
-            return self.data[key]
-        except KeyError as e:
-            return Status(success=False, error=e)
+        keys = [
+            DIMKey(
+                dim_type='ucx',
+                obj_id=str(uuid.uuid4()),
+                size=len(obj),
+                peer_host=self.address,
+                peer_port=self.port,
+            )
+            for obj in objs
+        ]
+        rpcs = [
+            RPC(operation='put', key=key, data=obj)
+            for key, obj in zip(keys, objs)
+        ]
+        self._send_rpcs(rpcs)
+        return keys
 
-    def evict(self, key: str) -> Status:
-        """Remove key from local dictionary.
 
-        Args:
-            key (str): the object to evict's key
+class UCXServer:
+    """UCXServer implementation."""
+
+    def __init__(self) -> None:
+        self.data: dict[str, bytes] = {}
 
-        Returns (bytes):
-            That the evict operation has been successful
+    def evict(self, key: str) -> None:
+        """Evict the object associated with the key.
 
+        Args:
+            key: Key associated with object to evict.
         """
         self.data.pop(key, None)
-        return Status(success=True, error=None)
 
     def exists(self, key: str) -> bool:
-        """Check if a key exists within local dictionary.
+        """Check if an object associated with the key exists.
 
         Args:
-            key (str): the object's key
-
-        Returns (bytes):
-            whether key exists
+            key: Key potentially associated with stored object.
 
+        Returns:
+            If an object associated with the key exists.
         """
         return key in self.data
 
-    async def handler(self, ep: ucp.Endpoint) -> None:
-        """Handle endpoint requests.
+    def get(self, key: str) -> bytes | None:
+        """Get the serialized object associated with the key.
 
         Args:
-            ep (ucp.Endpoint): the endpoint to communicate with.
+            key: Key associated with the object to retrieve.
 
+        Returns:
+            Data or `None` if no data associated with the key exists.
         """
-        json_kv = await ep.recv_obj()
+        return self.data.get(key, None)
 
-        if json_kv == bytes(1):
-            await ep.send_obj(bytes(1))
-            return
+    def put(self, key: str, data: bytes) -> None:
+        """Put data in the store.
+
+        Args:
+            key: Key associated with data.
+            data: Data to put in the store.
+        """
+        self.data[key] = data
 
-        kv = deserialize(bytes(json_kv))
+    def handle_rpc(self, rpc: RPC) -> RPCResponse:
+        """Process an RPC request.
 
-        key = kv['key']
-        data = kv['data']
-        func = kv['op']
+        Args:
+            rpc: Client RPC to process.
 
-        if func == 'set':
-            res = self.set(key, data)
-        else:
-            if func == 'get':
-                func = self.get
-            elif func == 'exists':
-                func = self.exists
-            elif func == 'evict':
-                func = self.evict
+        Returns:
+            Response containing result or an exception if the operation failed.
+        """
+        response: RPCResponse
+
+        try:
+            if rpc.operation == 'exists':
+                exists = self.exists(rpc.key.obj_id)
+                response = RPCResponse('exists', key=rpc.key, exists=exists)
+            elif rpc.operation == 'evict':
+                self.evict(rpc.key.obj_id)
+                response = RPCResponse('evict', key=rpc.key)
+            elif rpc.operation == 'get':
+                data = self.get(rpc.key.obj_id)
+                response = RPCResponse('get', key=rpc.key, data=data)
+            elif rpc.operation == 'put':
+                assert rpc.data is not None
+                self.put(rpc.key.obj_id, rpc.data)
+                response = RPCResponse('put', key=rpc.key)
             else:
                 raise AssertionError('Unreachable.')
-            res = func(key)
+        except Exception as e:
+            response = RPCResponse(rpc.operation, key=rpc.key, exception=e)
+        return response
 
-        if isinstance(res, Status) or isinstance(res, bool):
-            serialized_res = serialize(res)
-        else:
-            serialized_res = res
+    async def handler(self, ep: ucp.Endpoint) -> None:
+        """Handle endpoint requests.
 
-        await ep.send_obj(serialized_res)
+        Args:
+            ep: The endpoint making the request.
+        """
+        rpc_bytes = bytes(await ep.recv_obj())
 
-    async def run(self) -> None:
-        """Run this UCXServer forever.
+        if rpc_bytes == b'ping':
+            await ep.send_obj(b'pong')
+            return
 
-        Creates a listener for the handler method and waits on SIGINT/TERM
-        events to exit. Also handles cleaning up UCP objects.
-        """
-        self.ucp_listener = ucp.create_listener(self.handler, self.port)
+        rpc: RPC = deserialize(rpc_bytes)
+        response = self.handle_rpc(rpc)
 
-        # Set the stop condition when receiving SIGINT (ctrl-C) and SIGTERM.
-        loop = asyncio.get_running_loop()
-        stop = loop.create_future()
-        loop.add_signal_handler(signal.SIGINT, stop.set_result, None)
-        loop.add_signal_handler(signal.SIGTERM, stop.set_result, None)
+        message = serialize(response)
+        await ep.send_obj(message)
 
-        await stop
-        self.close()
-        await reset_ucp_async()
 
-    def close(self) -> None:
-        if self.ucp_listener is not None:
-            self.ucp_listener.close()
+async def run_server(port: int) -> None:  # pragma: no cover
+    """Listen and reply to RPCs from clients.
+
+    Warning:
+        This function does not return until SIGINT or SIGTERM is received.
+
+    Args:
+        port: Port the server should listen on.
+    """
+    server = UCXServer()
+    ucp_listener = ucp.create_listener(server.handler, port)
+
+    loop = asyncio.get_running_loop()
+    close_future = loop.create_future()
+    loop.add_signal_handler(signal.SIGINT, close_future.set_result, None)
+    loop.add_signal_handler(signal.SIGTERM, close_future.set_result, None)
+
+    await close_future
+    ucp_listener.close()
 
-            while not self.ucp_listener.closed():
-                sleep(0.001)
+    while not ucp_listener.closed():
+        await asyncio.sleep(0.001)
 
-            # Need to lose reference to Listener because UCP does reference
-            # counting
-            del self.ucp_listener
-            self.ucp_listener = None
+    loop.remove_signal_handler(signal.SIGINT)
+    loop.remove_signal_handler(signal.SIGTERM)
 
+    # UCP does reference counting of open resources
+    del ucp_listener
+    await reset_ucp_async()
 
-def launch_server(host: str, port: int) -> None:
-    """Launch the UCXServer in asyncio.
+
+def start_server(port: int) -> None:  # pragma: no cover
+    """Run a local server.
+
+    Note:
+        This function creates an event loop and executes
+        [`run_server()`][proxystore.connectors.dim.ucx.run_server] within
+        that loop.
 
     Args:
-        host (str): host for server to listen on.
-        port (int): port for server to listen on.
+        port: Port the server should listen on.
     """
-    logger.info(f'starting server on host {host} with port {port}')
+    asyncio.run(run_server(port))
 
-    ps = UCXServer(host, port)
-    # CI occasionally timeouts when starting this server in the
-    # store_implementation session fixture. It seems to not happen when
-    # debug=True, but this is just a temporary fix.
-    asyncio.run(ps.run(), debug=True)
 
-    logger.info(f'server running at address {host}:{port}')
+def spawn_server(
+    address: str,
+    port: int,
+    *,
+    spawn_timeout: float = 5.0,
+    kill_timeout: float | None = 1.0,
+) -> multiprocessing.context.SpawnProcess:
+    """Spawn a local server running in a separate process.
+
+    Note:
+        An `atexit` callback is registered which will terminate the spawned
+        server process when the calling process exits.
 
+    Args:
+        address: IP address the server will listen on.
+        port: Port the server will listen on.
+        spawn_timeout: Max time in seconds to wait for the server to start.
+        kill_timeout: Max time in seconds to wait for the server to shutdown
+            on exit.
 
-def reset_ucp() -> None:  # pragma: no cover
-    """Hard reset all of UCP.
+    Returns:
+        The process that the server is running in.
+    """
+    ctx = multiprocessing.get_context('spawn')
+    # UCX seems to hang if you fork a process after calling ucp.init().
+    # If discovered this via a comment in Dask's distributed communication:
+    # https://github.com/dask/distributed/blob/76bbfaf9f4a14906cbf4500ed42c442c7a5bc971/distributed/comm/ucx.py#L40  # noqa: E501
+    server_process = ctx.Process(
+        target=start_server,
+        args=(port,),
+    )
+    server_process.start()
+
+    def _kill_on_exit() -> None:  # pragma: no cover
+        server_process.terminate()
+        server_process.join(timeout=kill_timeout)
+        if server_process.is_alive():
+            server_process.kill()
+            server_process.join()
+        logger.debug(
+            'Server terminated on parent process exit '
+            f'(pid={server_process.pid})',
+        )
 
-    UCP provides :code:`ucp.reset()`; however, this function does not correctly
-    shutdown all asyncio tasks and readers. This function wraps
-    :code:`ucp.reset()` and additionally removes all readers on the event loop
-    and cancels/awaits all asyncio tasks.
+    atexit.register(_kill_on_exit)
+    logger.debug('Registered server cleanup atexit callback')
+
+    wait_for_server(address, port, timeout=spawn_timeout)
+    logger.debug(
+        f'Server started (host={address}, port={port}, pid={server_process.pid})',
+    )
+
+    return server_process
+
+
+async def wait_for_server_async(
+    address: str,
+    port: int,
+    timeout: float = 0.1,
+) -> None:
+    """Wait until the server responds.
+
+    Args:
+        address: Host IP of the server to ping.
+        port: Port of the server to ping.
+        timeout: Max time in seconds to wait for server response.
+
+    Raises:
+        ServerTimeoutError: If the server does not respond within the timeout.
     """
+    sleep_time = 0.01
+    time_waited = 0.0
 
-    def inner_context() -> None:
-        ctx = ucp.core._get_ctx()
+    while True:
+        try:
+            ep = await ucp.create_endpoint(address, port)
+        except ucp._libs.exceptions.UCXNotConnected as e:  # pragma: no cover
+            if time_waited >= timeout:
+                raise ServerTimeoutError(
+                    'Failed to connect to server within timeout '
+                    f'({timeout} seconds).',
+                ) from e
+            await asyncio.sleep(sleep_time)
+            time_waited += sleep_time
+        else:
+            break  # pragma: no cover
 
-        for task in ctx.progress_tasks:
-            if task is None:
-                continue
-            task.event_loop.remove_reader(ctx.epoll_fd)
-            if task.asyncio_task is not None:
-                try:
-                    task.asyncio_task.cancel()
-                    task.event_loop.run_until_complete(task.asyncio_task)
-                except asyncio.CancelledError:
-                    pass
+    await ep.send_obj(b'ping')
+    assert bytes(await ep.recv_obj()) == b'pong'
+    await ep.close()
+    assert ep.closed()
+    del ep
 
-    # We access ucp.core._get_ctx() inside this nested function so our local
-    # reference to the UCP context goes out of scope before calling
-    # ucp.reset(). ucp.reset() will fail if there are any weak references to
-    # to the UCP context because it assumes those may be Listeners or
-    # Endpoints that were not properly closed.
-    inner_context()
 
-    try:
-        ucp.reset()
-    except ucp.UCXError:
-        pass
+def wait_for_server(address: str, port: int, timeout: float = 0.1) -> None:
+    """Wait until the server responds.
+
+    Note:
+        This function calls
+        [`wait_for_server_async()`][proxystore.connectors.dim.ucx.wait_for_server_async]
+        using [`asyncio.run()`][asyncio.run].
+
+    Args:
+        address: The host IP of the server to ping.
+        port: Theport of the server to ping.
+        timeout: The max time in seconds to wait for server response.
+
+    Raises:
+        ServerTimeoutError: If the server does not respond within the timeout.
+    """
+    asyncio.run(wait_for_server_async(address, port, timeout))
 
 
-async def reset_ucp_async() -> None:  # pragma: no cover
+async def reset_ucp_async(reset_ucp: bool = True) -> None:  # pragma: no cover
     """Hard reset all of UCP.
 
-    UCP provides :code:`ucp.reset()`; however, this function does not correctly
+    UCP provides `ucp.reset()`; however, this function does not correctly
     shutdown all asyncio tasks and readers. This function wraps
-    :code:`ucp.reset()` and additionally removes all readers on the event loop
+    `ucp.reset()` and additionally removes all readers on the event loop
     and cancels/awaits all asyncio tasks.
     """
 
     async def inner_context() -> None:
         ctx = ucp.core._get_ctx()
 
         for task in ctx.progress_tasks:
             if task is None:
                 continue
             task.event_loop.remove_reader(ctx.epoll_fd)
             if task.asyncio_task is not None:
                 try:
                     task.asyncio_task.cancel()
                     await task.asyncio_task
-                except asyncio.CancelledError:
+                # A RuntimeError can happen if the task if from a different
+                # event loop. We'll just skip these for now
+                except (asyncio.CancelledError, RuntimeError):
                     pass
 
     # We access ucp.core._get_ctx() inside this nested function so our local
     # reference to the UCP context goes out of scope before calling
     # ucp.reset(). ucp.reset() will fail if there are any weak references to
     # to the UCP context because it assumes those may be Listeners or
     # Endpoints that were not properly closed.
     await inner_context()
 
-    try:
-        ucp.reset()
-    except ucp.UCXError:
-        pass
-
-
-async def wait_for_server(host: str, port: int, timeout: float = 5.0) -> None:
-    """Wait until the UCXServer responds.
-
-    Args:
-        host (str): host of UCXServer to ping.
-        port (int): port of UCXServer to ping.
-        timeout (float): max time in seconds to wait for server response
-            (default: 5.0).
-    """
-    sleep_time = 0.01
-    time_waited = 0.0
-
-    while True:
+    if reset_ucp:
         try:
-            ep = await ucp.create_endpoint(host, port)
-        except ucp._libs.exceptions.UCXNotConnected as e:  # pragma: no cover
-            if time_waited >= timeout:
-                raise RuntimeError(
-                    'Failed to connect to server within timeout '
-                    f'({timeout} seconds).',
-                ) from e
-            await asyncio.sleep(sleep_time)
-            time_waited += sleep_time
-        else:
-            break  # pragma: no cover
-
-    await ep.send_obj(bytes(1))
-    _ = await ep.recv_obj()
-    await ep.close()
-    assert ep.closed()
+            ucp.reset()
+        except ucp.UCXError:
+            pass
```

### Comparing `proxystore-0.4.1a1/proxystore/store/exceptions.py` & `proxystore-0.5.0/proxystore/store/exceptions.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 """Exceptions for Stores."""
 from __future__ import annotations
 
-from typing import NamedTuple
+from typing import Any
 
 from proxystore.store import base
 
 
 class StoreError(Exception):
     """Base exception class for store errors."""
 
@@ -25,26 +25,25 @@
 
 
 class ProxyResolveMissingKeyError(Exception):
     """Exception raised when the key associated with a proxy is missing."""
 
     def __init__(
         self,
-        key: NamedTuple,
-        store_type: type[base.Store[base.KeyT]],
+        key: base.ConnectorKeyT,
+        store_type: type[base.Store[Any]],
         store_name: str,
     ) -> None:
         """Init ProxyResolveMissingKeyError.
 
         Args:
-            key (tuple): key associated with target object that could not be
-                found in the store.
-            store_type (Store): type of store that the key could not be found
-                in.
-            store_name (str): name of store that the key could not be found in.
+            key: Key associated with target object that could not be found in
+                the store.
+            store_type: Type of store that the key could not be found in.
+            store_name: Name of store that the key could not be found in.
         """
         self.key = key
         self.store_type = store_type
         self.store_name = store_name
         super().__init__(
             f"Proxy cannot resolve target object with key='{self.key}' "
             f"from {self.store_type.__name__}(name='{self.store_name}'): "
```

### Comparing `proxystore-0.4.1a1/proxystore/store/globus.py` & `proxystore-0.5.0/proxystore/connectors/globus.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,67 +1,70 @@
-"""Globus Endpoint Implementation."""
+"""Globus transfer connector implementation."""
 from __future__ import annotations
 
 import json
 import logging
 import os
 import re
 import sys
+import uuid
+from types import TracebackType
 from typing import Any
 from typing import Callable
 from typing import Collection
 from typing import Generator
 from typing import Iterator
 from typing import NamedTuple
 from typing import Pattern
 from typing import Sequence
 
+if sys.version_info >= (3, 11):  # pragma: >=3.11 cover
+    from typing import Self
+else:  # pragma: <3.11 cover
+    from typing_extensions import Self
+
 if sys.version_info >= (3, 9):  # pragma: >=3.9 cover
     from typing import Literal
 else:  # pragma: <3.9 cover
     from typing_extensions import Literal
 
 import globus_sdk
 
-import proxystore.utils as utils
 from proxystore.globus import get_proxystore_authorizer
 from proxystore.globus import GlobusAuthFileError
-from proxystore.serialize import serialize as default_serializer
-from proxystore.store.base import Store
+from proxystore.utils import hostname
 
 logger = logging.getLogger(__name__)
 GLOBUS_MKDIR_EXISTS_ERROR_CODE = 'ExternalError.MkdirFailed.Exists'
 
 SerializerT = Callable[[Any], bytes]
 
 
 class GlobusEndpoint:
-    """GlobusEndpoint Class."""
+    """Globus endpoint representation.
+
+    Args:
+        uuid: UUID of Globus endpoint.
+        endpoint_path: Path within endpoint to directory to use
+            for storing objects.
+        local_path: Local path (as seen by the host filesystem) that
+            corresponds to the directory specified by `endpoint_path`.
+        host_regex: String that matches the host where
+            the Globus endpoint exists or regex pattern than can be used
+            to match the host. The host pattern is needed so that proxies
+            can figure out what the local endpoint is when they are resolved.
+    """
 
     def __init__(
         self,
         uuid: str,
         endpoint_path: str,
         local_path: str | None,
         host_regex: str | Pattern[str],
     ) -> None:
-        """Init GlobusEndpoint.
-
-        Args:
-            uuid (str): UUID of Globus endpoint.
-            endpoint_path (str): path within endpoint to directory to use
-                for storing objects.
-            local_path (str): local path (as seen by the host filesystem) that
-                corresponds to the directory specified by `endpoint_path`.
-            host_regex (str, Pattern): `str` that matches the host where
-                the Globus endpoint exists or regex pattern than can be used
-                to match the host. The host pattern is needed so that proxies
-                can figure out what the local endpoint is when they are
-                resolved.
-        """
         if not isinstance(uuid, str):
             raise TypeError('uuid must be a str.')
         if not isinstance(endpoint_path, str):
             raise TypeError('endpoint_path must be a str.')
         if not isinstance(local_path, str):
             raise TypeError('local_path must be a str.')
         if not (
@@ -71,51 +74,48 @@
 
         self.uuid = uuid
         self.endpoint_path = endpoint_path
         self.local_path = local_path
         self.host_regex = host_regex
 
     def __eq__(self, endpoint: object) -> bool:
-        """Endpoints are equal if attributes match."""
         if not isinstance(endpoint, GlobusEndpoint):
             raise NotImplementedError
         if (
             self.uuid == endpoint.uuid
             and self.endpoint_path == endpoint.endpoint_path
             and self.local_path == endpoint.local_path
             and self.host_regex == endpoint.host_regex
         ):
             return True
         return False
 
     def __repr__(self) -> str:
-        """Represent GlobusEndpoint as string."""
         return (
             f"{self.__class__.__name__}(uuid='{self.uuid}', "
             f"endpoint_path='{self.endpoint_path}', "
             f"local_path='{self.local_path}', "
             f"host_regex='{self.host_regex}')"
         )
 
 
 class GlobusEndpoints:
-    """GlobusEndpoints Class."""
-
-    def __init__(self, endpoints: Collection[GlobusEndpoint]) -> None:
-        """Init GlobusEndpoints.
+    """A collection of Globus endpoints.
 
-        Args:
-            endpoints: iterable of
-                :class:`GlobusEndpoint <.GlobusEndpoint>` instances.
+    Args:
+        endpoints: Iterable of
+            [`GlobusEndpoints`][proxystore.store.globus.GlobusEndpoints]
+            instances.
+
+    Raises:
+        ValueError: If `endpoints` has length 0 or if multiple endpoints with \
+            the same UUID are provided.
+    """
 
-        Raises:
-            ValueError:
-                if `endpoints` has length 0 or if multiple endpoints with the
-                same UUID are provided.
-        """
+    def __init__(self, endpoints: Collection[GlobusEndpoint]) -> None:
         if len(endpoints) == 0:
             raise ValueError(
                 'GlobusEndpoints must be passed at least one GlobusEndpoint '
                 'object',
             )
         self._endpoints: dict[str, GlobusEndpoint] = {}
         for endpoint in endpoints:
@@ -123,94 +123,92 @@
                 raise ValueError(
                     'Cannot pass multiple GlobusEndpoint objects with the '
                     'same Globus endpoint UUID.',
                 )
             self._endpoints[endpoint.uuid] = endpoint
 
     def __getitem__(self, uuid: str) -> GlobusEndpoint:
-        """Index GlobusEndpoints with UUID."""
         try:
             return self._endpoints[uuid]
         except KeyError:
             raise KeyError(
                 f'Endpoint with UUID {uuid} does not exist.',
             ) from None
 
     def __iter__(self) -> Iterator[GlobusEndpoint]:
-        """Iterate over GlobusEndpoints."""
-
         def _iterator() -> Generator[GlobusEndpoint, None, None]:
             yield from self._endpoints.values()
 
         return _iterator()
 
     def __len__(self) -> int:
-        """Length of GlobusEndpoints."""
         return len(self._endpoints)
 
     def __repr__(self) -> str:
-        """Represent GlobusEndpoints as string."""
         s = f'{self.__class__.__name__}(['
         s += ', '.join(str(ep) for ep in self._endpoints.values())
         s += '])'
         return s
 
     @classmethod
     def from_dict(
         cls: type[GlobusEndpoints],
         json_object: dict[str, dict[str, str]],
     ) -> GlobusEndpoints:
-        """Construct a GlobusEndpoints object from a dictionary.
+        """Construct an endpoints collection from a dictionary.
 
         Example:
 
-        .. code-block:: text
-
-           {
-             "endpoint-uuid-1": {
-               "host_regex": "host1-regex",
-               "endpoint_path": "/path/to/endpoint/dir",
-               "local_path": "/path/to/local/dir"
-             },
-             "endpoint-uuid-2": {
-               "host_regex": "host2-regex",
-               "endpoint_path": "/path/to/endpoint/dir",
-               "local_path": "/path/to/local/dir"
-             }
-           }
+            ```python
+            {
+              "endpoint-uuid-1": {
+                "host_regex": "host1-regex",
+                "endpoint_path": "/path/to/endpoint/dir",
+                "local_path": "/path/to/local/dir"
+              },
+              "endpoint-uuid-2": {
+                "host_regex": "host2-regex",
+                "endpoint_path": "/path/to/endpoint/dir",
+                "local_path": "/path/to/local/dir"
+              }
+            }
+            ```
         """  # noqa: D412
         endpoints = []
-        for uuid, params in json_object.items():
+        for ep_uuid, params in json_object.items():
             endpoints.append(
                 GlobusEndpoint(
-                    uuid=uuid,
+                    uuid=ep_uuid,
                     endpoint_path=params['endpoint_path'],
                     local_path=params['local_path'],
                     host_regex=params['host_regex'],
                 ),
             )
         return GlobusEndpoints(endpoints)
 
     @classmethod
     def from_json(cls, json_file: str) -> GlobusEndpoints:
         """Construct a GlobusEndpoints object from a json file.
 
         The `dict` read from the JSON file will be passed to
-        :func:`from_dict()` and should match the format expected by
-        :func:`from_dict()`.
+        [`from_dict()`][proxystore.store.globus.GlobusEndpoints.from_dict] and
+        should match the format expected by
+        [`from_dict()`][proxystore.store.globus.GlobusEndpoints.from_dict].
         """
         with open(json_file) as f:
             data = f.read()
         return cls.from_dict(json.loads(data))
 
     def dict(self) -> dict[str, dict[str, str]]:
         """Convert the GlobusEndpoints to a dict.
 
-        Note that the :class:`.GlobusEndpoints` object can be reconstructed by
-        passing the `dict` to :func:`from_dict()`.
+        Note that the
+        [`GlobusEndpoints`][proxystore.store.globus.GlobusEndpoints]
+        object can be reconstructed by passing the `dict` to.
+        [`from_dict()`][proxystore.store.globus.GlobusEndpoints.from_dict].
         """
         data = {}
         for endpoint in self:
             data[endpoint.uuid] = {
                 'endpoint_path': endpoint.endpoint_path,
                 'local_path': endpoint.local_path,
                 'host_regex': endpoint.host_regex.pattern
@@ -222,120 +220,101 @@
     def get_by_host(self, host: str) -> GlobusEndpoint:
         """Get endpoint by host.
 
         Searches the endpoints for a endpoint who's `host_regex` matches
         `host`.
 
         Args:
-            host (str): host to match/
+            host: Host to match.
 
         Returns:
-            :class:`GlobusEndpoint <.GlobusEndpoint>`
+            Globus endpoint.
 
         Raises:
-            ValueError:
-                if `host` does not match any of the endpoints.
+            ValueError: If `host` does not match any of the endpoints.
         """
         for endpoint in self._endpoints.values():
             if re.fullmatch(endpoint.host_regex, host) is not None:
                 return endpoint
         raise ValueError(f'Cannot find endpoint matching host {host}')
 
 
-class GlobusStoreKey(NamedTuple):
-    """Key to object in a GlobusStore."""
+class GlobusKey(NamedTuple):
+    """Key to object transferred with Globus.
+
+    Attributes:
+        filename: Unique object filename.
+        task_id: Globus transfer task ID for the file.
+    """
 
     filename: str
-    """Unique object filename."""
     task_id: str
-    """Globus transfer task ID for the file."""
 
     def __eq__(self, other: Any) -> bool:
         """Match keys by filename only.
 
         This is a hack around the fact that the task_id is not created until
         after the filename is so there can be a state where the task_id
         is empty.
         """
         if isinstance(other, tuple):
             return self[0] == other[0]
         return False
 
     def __ne__(self, other: Any) -> bool:
-        """Match keys by filename only."""
+        # Match keys by filename only.
         return not self == other
 
 
-class GlobusStore(Store[GlobusStoreKey]):
-    """Globus backend class.
+class GlobusConnector:
+    """Globus transfer connector.
 
-    The :class:`GlobusStore <.GlobusStore>` is similar to a
-    :class:`FileStore <proxystore.store.file.FileStore>` in that objects in the
-    store are saved to disk but allows for the transfer of objects between two
-    remote file systems. The two directories on the separate file systems are
-    kept in sync via Globus transfers. The :class:`GlobusStore <.GlobusStore>`
+    The [`GlobusConnector`][proxystore.connectors.globus.GlobusConnector] is
+    similar to a [`FileConnector`][proxystore.connectors.file.FileConnector]
+    in that objects are saved to disk but allows for the transfer of objects
+    between two remote file systems. The two directories on the separate file
+    systems are kept in sync via Globus transfers. The
+    [`GlobusConnector`][proxystore.connectors.globus.GlobusConnector]
     is useful when moving data between hosts that have a Globus endpoint but
     may have restrictions that prevent the use of other store backends
     (e.g., ports cannot be opened for using a
-    :class:`RedisStore <proxystore.store.redis.RedisStore>`).
+    [`RedisConnector`][proxystore.connectors.redis.RedisConnector].
 
     Note:
         To use Globus for data transfer, Globus authentication needs to be
         performed otherwise an error will be raised. Authentication can be
-        performed on the command line with :code:`$ proxystore-globus-auth`.
+        performed on the command line with `#!bash proxystore-globus-auth`.
         Authentication only needs to be performed once per system.
 
-    Warning:
-        The :class:`GlobusStore <.GlobusStore>` encodes the Globus transfer
-        IDs into the keys, thus the keys returned by functions such
-        as :func:`set() <set>` will be different.
+    Args:
+        endpoints: Globus endpoints to keep in sync. If passed as a `dict`,
+            the dictionary must match the format expected by
+            [`GlobusEndpoints.from_dict()`][proxystore.store.globus.GlobusEndpoints.from_dict].
+        polling_interval: Interval in seconds to check if Globus
+            tasks have finished.
+        sync_level: Globus transfer sync level.
+        timeout: Timeout in seconds for waiting on Globus tasks.
+
+    Raises:
+        GlobusAuthFileError: If the Globus authentication file cannot be found.
+        ValueError: If `endpoints` is of an incorrect type.
+        ValueError: If the `#!python len(endpoints) != 2` because this
+            implementation can currently only keep two endpoints in sync.
     """
 
     def __init__(
         self,
-        name: str,
-        *,
         endpoints: GlobusEndpoints
         | list[GlobusEndpoint]
         | dict[str, dict[str, str]],
         polling_interval: int = 1,
         sync_level: int
         | Literal['exists', 'size', 'mtime', 'checksum'] = 'mtime',
         timeout: int = 60,
-        cache_size: int = 16,
-        stats: bool = False,
     ) -> None:
-        """Init GlobusStore.
-
-        Args:
-            name (str): name of the store instance.
-            endpoints (GlobusEndpoints): Globus endpoints to keep
-                in sync. If passed as a `dict`, the dictionary must match the
-                format expected by :func:`GlobusEndpoints.from_dict()`.
-            polling_interval (int): interval in seconds to check if Globus
-                tasks have finished.
-            sync_level (str, int): Globus transfer sync level.
-            timeout (int): timeout in seconds for waiting on Globus tasks.
-            cache_size (int): size of LRU cache (in # of objects). If 0,
-                the cache is disabled. The cache is local to the Python
-                process (default: 16).
-            stats (bool): collect stats on store operations (default: False).
-
-        Raise:
-            GlobusAuthFileError:
-                if the Globus authentication file cannot be found.
-            ValueError:
-                if `endpoints` is not a list of
-                :class:`GlobusEndpoint <.GlobusEndpoint>`, instance of
-                :class:`GlobusEndpoints <.GlobusEndpoints>`, or dict.
-            ValueError:
-                if the :code:`len(endpoints) != 2` because
-                :class:`GlobusStore <.GlobusStore>` can currently only keep
-                two endpoints in sync.
-        """
         if isinstance(endpoints, GlobusEndpoints):
             self.endpoints = endpoints
         elif isinstance(endpoints, list):
             self.endpoints = GlobusEndpoints(endpoints)
         elif isinstance(endpoints, dict):
             self.endpoints = GlobusEndpoints.from_dict(endpoints)
         else:
@@ -359,56 +338,52 @@
                 'authentication process with the proxystore-globus-auth tool.',
             ) from e
 
         self._transfer_client = globus_sdk.TransferClient(
             authorizer=authorizer,
         )
 
-        super().__init__(
-            name,
-            cache_size=cache_size,
-            stats=stats,
-            kwargs={
-                # Pass endpoints as a dict to make kwargs JSON serializable
-                'endpoints': self.endpoints.dict(),
-                'polling_interval': self.polling_interval,
-                'sync_level': self.sync_level,
-                'timeout': self.timeout,
-            },
-        )
+    def __enter__(self) -> Self:
+        return self
+
+    def __exit__(
+        self,
+        exc_type: type[BaseException] | None,
+        exc_value: BaseException | None,
+        exc_traceback: TracebackType | None,
+    ) -> None:
+        self.close()
 
-    def create_key(self, obj: Any) -> GlobusStoreKey:
-        # We do not know task ID at the time we need a filename so we leave
-        # task_id empty and update it later.
-        return GlobusStoreKey(filename=utils.create_key(obj), task_id='')
+    def __repr__(self) -> str:
+        return f'{self.__class__.__name__}(endpoints={self.endpoints})'
 
     def _get_filepath(
         self,
         filename: str,
         endpoint: GlobusEndpoint | None = None,
     ) -> str:
         """Get filepath from filename.
 
         Args:
-            filename (str): name of file in Globus
-            endpoint (GlobusEndpoint): optionally specify a GlobusEndpoint
+            filename: Name of file in Globus.
+            endpoint: Optionally specify a GlobusEndpoint
                 to get the filepath relative to. If not specified, the endpoint
                 associated with the local host will be used.
 
         Returns:
-            full local path to file.
+            Full local path to file.
         """
         if endpoint is None:
             endpoint = self._get_local_endpoint()
         local_path = os.path.expanduser(endpoint.local_path)
         return os.path.join(local_path, filename)
 
     def _get_local_endpoint(self) -> GlobusEndpoint:
         """Get endpoint local to current host."""
-        return self.endpoints.get_by_host(utils.hostname())
+        return self.endpoints.get_by_host(hostname())
 
     def _validate_task_id(self, task_id: str) -> bool:
         """Validate key contains a real Globus task id."""
         try:
             self._transfer_client.get_task(task_id)
         except globus_sdk.TransferAPIError as e:
             if e.http_status == 400:
@@ -422,32 +397,31 @@
             done = self._transfer_client.task_wait(
                 task,
                 timeout=self.timeout,
                 polling_interval=self.polling_interval,
             )
             if not done:
                 raise RuntimeError(
-                    f'Task {task} did not complete within the ' 'timeout',
+                    f'Task {task} did not complete within the timeout',
                 )
 
     def _transfer_files(
         self,
         filenames: str | list[str],
         delete: bool = False,
     ) -> str:
         """Launch Globus Transfer to sync endpoints.
 
         Args:
-            filenames (str, list): filename or list of filenames to transfer.
+            filenames: Filename or list of filenames to transfer.
                 Note must be filenames, not filepaths.
-            delete (bool): if `True`, delete the filenames rather than syncing
-                them.
+            delete: If `True`, delete the filenames rather than syncing them.
 
         Returns:
-            Globus Task UUID that can be used to check the status of the
+            Globus Task UUID that can be used to check the status of the \
             transfer.
         """
         src_endpoint = self._get_local_endpoint()
         dst_endpoints = [ep for ep in self.endpoints if ep != src_endpoint]
         assert len(dst_endpoints) == 1
         dst_endpoint = dst_endpoints[0]
 
@@ -491,18 +465,18 @@
             else:
                 raise AssertionError('Unreachable.')
 
         tdata = _submit_transfer_action(self._transfer_client, transfer_task)
         return tdata['task_id']
 
     def close(self) -> None:
-        """Cleanup directories used by ProxyStore in the Globus endpoints.
+        """Close the connector and clean up.
 
         Warning:
-            Will delete the directory at `local_path` on each endpoint.
+            This will delete the directory at `local_path` on each endpoint.
 
         Warning:
             This method should only be called at the end of the program when
             the store will no longer be used, for example once all proxies
             have been resolved.
         """
         for endpoint in self.endpoints:
@@ -514,103 +488,141 @@
             delete_task['notify_on_succeeded'] = False
             delete_task['notify_on_failed'] = False
             delete_task['notify_on_inactive'] = False
             delete_task.add_item(endpoint.endpoint_path)
             tdata = _submit_transfer_action(self._transfer_client, delete_task)
             self._wait_on_tasks(tdata['task_id'])
 
-    def evict(self, key: GlobusStoreKey) -> None:
+    def config(self) -> dict[str, Any]:
+        """Get the connector configuration.
+
+        The configuration contains all the information needed to reconstruct
+        the connector object.
+        """
+        return {
+            'endpoints': self.endpoints.dict(),
+            'polling_interval': self.polling_interval,
+            'sync_level': self.sync_level,
+            'timeout': self.timeout,
+        }
+
+    @classmethod
+    def from_config(cls, config: dict[str, Any]) -> GlobusConnector:
+        """Create a new connector instance from a configuration.
+
+        Args:
+            config: Configuration returned by `#!python .config()`.
+        """
+        return cls(**config)
+
+    def evict(self, key: GlobusKey) -> None:
+        """Evict the object associated with the key.
+
+        Args:
+            key: Key associated with object to evict.
+        """
         if not self.exists(key):
             return
 
         path = self._get_filepath(key.filename)
         os.remove(path)
-        self._cache.evict(key)
         self._transfer_files(key.filename, delete=True)
-        logger.debug(
-            f"EVICT key='{key}' FROM {self.__class__.__name__}"
-            f"(name='{self.name}')",
-        )
 
-    def exists(self, key: GlobusStoreKey) -> bool:
+    def exists(self, key: GlobusKey) -> bool:
+        """Check if an object associated with the key exists.
+
+        Note:
+            If the corresponding Globus transfer is still in progress, this
+            method will wait to make sure the transfers is successful.
+
+        Args:
+            key: Key potentially associated with stored object.
+
+        Returns:
+            If an object associated with the key exists.
+        """
         if not self._validate_task_id(key.task_id):
             return False
         self._wait_on_tasks(key.task_id)
         return os.path.exists(self._get_filepath(key.filename))
 
-    def get_bytes(self, key: GlobusStoreKey) -> bytes | None:
+    def get(self, key: GlobusKey) -> bytes | None:
+        """Get the serialized object associated with the key.
+
+        Args:
+            key: Key associated with the object to retrieve.
+
+        Returns:
+            Serialized object or `None` if the object does not exist.
+        """
         if not self.exists(key):
             return None
 
         path = self._get_filepath(key.filename)
         with open(path, 'rb') as f:
             return f.read()
 
-    def set_bytes(self, key: GlobusStoreKey, data: bytes) -> None:
-        path = self._get_filepath(key.filename)
-        if not os.path.isdir(os.path.dirname(path)):
-            os.makedirs(os.path.dirname(path), exist_ok=True)
+    def get_batch(self, keys: Sequence[GlobusKey]) -> list[bytes | None]:
+        """Get a batch of serialized objects associated with the keys.
+
+        Args:
+            keys: Sequence of keys associated with objects to retrieve.
+
+        Returns:
+            List with same order as `keys` with the serialized objects or \
+            `None` if the corresponding key does not have an associated object.
+        """
+        return [self.get(key) for key in keys]
+
+    def put(self, obj: bytes) -> GlobusKey:
+        """Put a serialized object in the store.
+
+        Args:
+            obj: Serialized object to put in the store.
+
+        Returns:
+            Key which can be used to retrieve the object.
+        """
+        filename = str(uuid.uuid4())
+
+        path = self._get_filepath(filename)
+        os.makedirs(os.path.dirname(path), exist_ok=True)
+
         with open(path, 'wb', buffering=0) as f:
-            f.write(data)
+            f.write(obj)
 
-    def set(
-        self,
-        obj: Any,
-        *,
-        serializer: SerializerT | None = None,
-    ) -> GlobusStoreKey:
-        if serializer is not None:
-            obj = serializer(obj)
-        else:
-            obj = default_serializer(obj)
+        task_id = self._transfer_files(filename)
 
-        if not isinstance(obj, bytes):
-            raise TypeError('Serializer must produce bytes.')
+        return GlobusKey(filename=filename, task_id=task_id)
 
-        temp_key = self.create_key(obj)
-        self.set_bytes(temp_key, obj)
-        tid = self._transfer_files(temp_key.filename)
-        key = temp_key._replace(task_id=tid)
-
-        logger.debug(
-            f"SET key='{key}' IN {self.__class__.__name__}"
-            f"(name='{self.name}')",
-        )
-        return key
+    def put_batch(self, objs: Sequence[bytes]) -> list[GlobusKey]:
+        """Put a batch of serialized objects in the store.
 
-    def set_batch(
-        self,
-        objs: Sequence[Any],
-        *,
-        serializer: SerializerT | None = None,
-    ) -> list[GlobusStoreKey]:
-        temp_keys = []
-        for obj in objs:
-            if serializer is not None:
-                obj = serializer(obj)
-            else:
-                obj = default_serializer(obj)
+        Args:
+            objs: Sequence of serialized objects to put in the store.
 
-            if not isinstance(obj, bytes):
-                raise TypeError('Serializer must produce bytes.')
+        Returns:
+            List of keys with the same order as `objs` which can be used to \
+            retrieve the objects.
+        """
+        filenames = [str(uuid.uuid4()) for _ in objs]
 
-            temp_key = self.create_key(obj)
-            temp_keys.append(temp_key)
-            self.set_bytes(temp_key, obj)
-
-        # Batch of objs written to disk so we can trigger Globus transfer
-        tid = self._transfer_files([k.filename for k in temp_keys])
-
-        keys = [key._replace(task_id=tid) for key in temp_keys]
-        logger.debug(
-            f"SET keys='{keys}' IN {self.__class__.__name__}"
-            f"(name='{self.name}')",
-        )
+        for filename, obj in zip(filenames, objs):
+            path = self._get_filepath(filename)
+            os.makedirs(os.path.dirname(path), exist_ok=True)
+
+            with open(path, 'wb', buffering=0) as f:
+                f.write(obj)
+
+        task_id = self._transfer_files(filenames)
 
-        return keys
+        return [
+            GlobusKey(filename=filename, task_id=task_id)
+            for filename in filenames
+        ]
 
 
 def _submit_transfer_action(
     client: globus_sdk.TransferClient,
     task: globus_sdk.DeleteData | globus_sdk.TransferData,
 ) -> globus_sdk.response.GlobusHTTPResponse:
     """Submit Globus transfer task via the client.
@@ -619,21 +631,31 @@
     exceptions.
 
     Args:
         client: Globus transfer client.
         task: Globus transfer task.
 
     Returns:
-        ``GlobusHTTPResponse``
+        A `GlobusHTTPResponse`.
     """
     try:
         if isinstance(task, globus_sdk.DeleteData):
-            return client.submit_delete(task)
+            response = client.submit_delete(task)
+            logger.debug(
+                'Submitted DeleteData Globus task with ID '
+                f'{response["task_id"]}',
+            )
+            return response
         elif isinstance(task, globus_sdk.TransferData):
-            return client.submit_transfer(task)
+            response = client.submit_transfer(task)
+            logger.debug(
+                'Submitted TransferData Globus task with ID '
+                f'{response["task_id"]}',
+            )
+            return response
         else:
             raise AssertionError('Unreachable.')
     except globus_sdk.TransferAPIError as e:  # pragma: no cover
         # https://github.com/globus/globus-sdk-python/blob/054a29167c86f66b77bb99beca45ce317b02a5a7/src/globus_sdk/exc/err_info.py#L93  # noqa: E501
         raise Exception(
             f'Failure initiating Globus Transfer. Error info: {e.info}',
         ) from e
```

### Comparing `proxystore-0.4.1a1/proxystore/store/local.py` & `proxystore-0.5.0/proxystore/store/local.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,78 +1,61 @@
 """LocalStore Implementation."""
 from __future__ import annotations
 
-import logging
-from typing import Any
-from typing import NamedTuple
+import warnings
 
-import proxystore.utils as utils
+from proxystore.connectors.local import LocalConnector
+from proxystore.connectors.local import LocalKey
+from proxystore.store.base import DeserializerT
+from proxystore.store.base import SerializerT
 from proxystore.store.base import Store
 
-logger = logging.getLogger(__name__)
 
+class LocalStore(Store[LocalConnector]):
+    """Store wrapper for local in-process storage.
 
-class LocalStoreKey(NamedTuple):
-    """Key to objects in a LocalStore."""
-
-    id: str
-    """Unique object ID."""
-
-
-class LocalStore(Store[LocalStoreKey]):
-    """Local Memory Key-Object Store."""
+    Warning:
+        This wrapper exists for backwards compatibility with ProxyStore
+        <=0.4.* and will be deprecated in version 0.6.0.
+
+    Args:
+        name: Name of the store instance.
+        store_dict: Dictionary to store data in. If not specified,
+            a new empty dict will be generated.
+        serializer: Optional callable which serializes the object. If `None`,
+            the default serializer
+            ([`serialize()`][proxystore.serialize.serialize]) will be used.
+        deserializer: Optional callable used by the factory to deserialize the
+            byte string. If `None`, the default deserializer
+            ([`deserialize()`][proxystore.serialize.deserialize]) will be
+            used.
+        cache_size: Size of LRU cache (in # of objects). If 0,
+            the cache is disabled. The cache is local to the Python process.
+        metrics: Enable recording operation metrics.
+    """
 
     def __init__(
         self,
         name: str,
+        store_dict: dict[LocalKey, bytes] | None = None,
         *,
-        store_dict: dict[LocalStoreKey, bytes] | None = None,
+        serializer: SerializerT | None = None,
+        deserializer: DeserializerT | None = None,
         cache_size: int = 16,
-        stats: bool = False,
+        metrics: bool = False,
     ) -> None:
-        """Init LocalStore.
-
-        Warning:
-            :class:`LocalStore <.LocalStore>` should typically be used for
-            testing proxystore locally as using proxy store within the same
-            Python process is unnecessary.
-
-        Args:
-            name (str): name of this store instance.
-            store_dict (dict): dictionary to store data in. If not specified,
-                a new empty dict will be generated (default: None).
-            cache_size (int): size of LRU cache (in # of objects). If 0,
-                the cache is disabled. The cache is local to the Python
-                process (default: 16).
-            stats (bool): collect stats on store operations (default: False).
-        """
-        self._store: dict[LocalStoreKey, bytes] = {}
-        if store_dict is not None:
-            self._store = store_dict
-
+        warnings.warn(
+            'The LocalStore will be deprecated in v0.6.0. Initializing a '
+            'Store with a Connector is preferred. See '
+            'https://github.com/proxystore/proxystore/issues/214 for details.',
+            DeprecationWarning,
+            stacklevel=2,
+        )
+        connector = LocalConnector(store_dict)
         super().__init__(
             name,
+            connector,
+            serializer=serializer,
+            deserializer=deserializer,
             cache_size=cache_size,
-            stats=stats,
-            kwargs={'store_dict': self._store},
+            metrics=metrics,
         )
-
-    def create_key(self, obj: Any) -> LocalStoreKey:
-        return LocalStoreKey(id=utils.create_key(obj))
-
-    def evict(self, key: LocalStoreKey) -> None:
-        if key in self._store:
-            del self._store[key]
-        self._cache.evict(key)
-        logger.debug(
-            f"EVICT key='{key}' FROM {self.__class__.__name__}"
-            f"(name='{self.name}')",
-        )
-
-    def exists(self, key: LocalStoreKey) -> bool:
-        return key in self._store
-
-    def get_bytes(self, key: LocalStoreKey) -> bytes | None:
-        return self._store.get(key, None)
-
-    def set_bytes(self, key: LocalStoreKey, data: bytes) -> None:
-        self._store[key] = data
```

### Comparing `proxystore-0.4.1a1/proxystore/store/stats.py` & `proxystore-0.5.0/proxystore/store/metrics.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,221 +1,225 @@
-"""Utilities for Tracking Stats on Store Operations."""
+"""Utilities for recording Store operation metrics.
+
+See the [Performance Guide](../../guides/performance.md) to learn more about
+interacting with metrics recorded for
+[`Store`][proxystore.store.base.Store] operations.
+"""
 from __future__ import annotations
 
+import copy
+import dataclasses
 import math
-from collections.abc import MutableMapping
-from dataclasses import dataclass
-from functools import partial
-from time import perf_counter_ns
+import sys
+import time
+from collections import defaultdict
 from typing import Any
-from typing import Callable
-from typing import cast
-from typing import Iterator
-from typing import KeysView
-from typing import NamedTuple
-from typing import TypeVar
+from typing import Sequence
+from typing import Tuple
+from typing import Union
+
+if sys.version_info >= (3, 11):  # pragma: >=3.11 cover
+    pass
+else:  # pragma: <3.11 cover
+    pass
 
 from proxystore.proxy import Proxy
 from proxystore.store.utils import get_key
 
-GenericCallable = TypeVar('GenericCallable', bound=Callable[..., Any])
-
-STORE_METHOD_KEY_IS_RESULT = {
-    'evict': False,
-    'exists': False,
-    'get': False,
-    'get_bytes': False,
-    'is_cached': False,
-    'proxy': True,
-    'set': True,
-    'set_bytes': False,
-}
-
+ConnectorKeyT = Tuple[Any, ...]
+KeyT = Union[ConnectorKeyT, Sequence[ConnectorKeyT]]
+"""Key types supported by [`StoreMetrics`][proxystore.store.metrics.StoreMetrics]."""  # noqa: E501
+ProxyT = Union[Proxy[Any], Sequence[Proxy[Any]]]
+"""Proxy types supported by [`StoreMetrics`][proxystore.store.metrics.StoreMetrics].
 
-class Event(NamedTuple):
-    """Event corresponding to a function called with a specific key."""
+When a `ProxyT` is passed, the keys are extracted from the proxies.
+"""
 
-    function: str
-    key: NamedTuple | None
 
-
-@dataclass
+@dataclasses.dataclass
 class TimeStats:
-    """Helper class for tracking time stats of an operation."""
+    """Tracks time statistics of a reoccuring event.
+
+    Attributes:
+        count: Number of times this event as occurred.
+        avg_time_ms: Average time in milliseconds of the event.
+        min_time_ms: Minimum time in milliseconds of all event occurrences.
+        max_time_ms: Maximum time in milliseconds of all event occurrences.
+        last_time_ms: Time in milliseconds of the most recent event occurrence.
+        last_timestamp: The UNIX timestamp (seconds) of when the last
+            event time was recorded.
+    """
 
-    calls: int = 0
+    count: int = 0
     avg_time_ms: float = 0
     min_time_ms: float = math.inf
     max_time_ms: float = 0
-    size_bytes: int | None = None
+    last_time_ms: float = 0
+    last_timestamp: float = 0
 
     def __add__(self, other: TimeStats) -> TimeStats:
-        """Add two instances together."""
+        if self.last_timestamp > other.last_timestamp:
+            last_time_ms = self.last_time_ms
+            last_timestamp = self.last_timestamp
+        else:
+            last_time_ms = other.last_time_ms
+            last_timestamp = other.last_timestamp
+
         return TimeStats(
-            calls=self.calls + other.calls,
-            avg_time_ms=self._weighted_avg(
+            count=self.count + other.count,
+            avg_time_ms=_weighted_avg(
                 self.avg_time_ms,
-                self.calls,
+                self.count,
                 other.avg_time_ms,
-                other.calls,
+                other.count,
             ),
             min_time_ms=min(self.min_time_ms, other.min_time_ms),
             max_time_ms=max(self.max_time_ms, other.max_time_ms),
+            last_time_ms=last_time_ms,
+            last_timestamp=last_timestamp,
         )
 
-    def add_time(self, time_ms: float, size_bytes: int | None = None) -> None:
-        """Add a new time to the stats.
-
-        Args:
-            time_ms (float): time (milliseconds) of a method execution.
-            size_bytes (int): optionally note the data size associated with
-                the operation that produced these statistics.
-        """
-        self.avg_time_ms = self._weighted_avg(
+    def add_time(self, time_ms: float) -> None:
+        self.avg_time_ms = _weighted_avg(
             self.avg_time_ms,
-            self.calls,
+            self.count,
             time_ms,
             1,
         )
-        self.min_time_ms = min(time_ms, self.min_time_ms)
-        self.max_time_ms = max(time_ms, self.max_time_ms)
-        self.calls += 1
-        self.size_bytes = size_bytes
-
-    def _weighted_avg(self, a1: float, n1: int, a2: float, n2: float) -> float:
-        """Compute weighted average between two separate averages.
+        self.max_time_ms = max(self.max_time_ms, time_ms)
+        self.min_time_ms = min(self.min_time_ms, time_ms)
+        self.last_time_ms = time_ms
+        self.last_timestamp = time.time()
+        self.count += 1
+
+    def as_dict(self) -> dict[str, Any]:
+        """Convert the dataclass to a [`dict`][dict]."""
+        return dataclasses.asdict(self)
+
+
+@dataclasses.dataclass
+class Metrics:
+    """Records metrics and attributes for events.
+
+    Attributes:
+        attributes: A mapping of attributes to their values.
+        counters: A mapping of counter names to the integer value of the
+            counter.
+        times: A mapping of events to a summary of the statistics recorded
+            over occurrences of that event.
+    """
+
+    attributes: dict[str, Any] = dataclasses.field(default_factory=dict)
+    counters: dict[str, int] = dataclasses.field(default_factory=dict)
+    times: dict[str, TimeStats] = dataclasses.field(default_factory=dict)
+
+    def as_dict(self) -> dict[str, Any]:
+        """Convert the dataclass to a [`dict`][dict]."""
+        return dataclasses.asdict(self)
 
-        Args:
-            a1 (float): first average.
-            n1 (float): number of samples in `a1`.
-            a2 (float): second average.
-            n2 (float): number of samples in `a2`.
 
-        Returns:
-            weighted average between `a1` and `a2`.
-        """
-        return ((a1 * n1) + (a2 * n2)) / (n1 + n2)
+class StoreMetrics:
+    """Record and query metrics on [`Store`][proxystore.store.base.Store] operations."""  # noqa: E501
 
+    def __init__(self) -> None:
+        self._metrics: dict[int, Metrics] = defaultdict(Metrics)
 
-class FunctionEventStats(MutableMapping):  # type: ignore
-    """Class for tracking stats of calls of functions that take a key."""
+    def add_attribute(self, name: str, key: KeyT, value: Any) -> None:
+        """Add an attribute associated with the key.
 
-    def __init__(self) -> None:
-        """Init FunctionEventStats."""
-        self._events: dict[Event, TimeStats] = {}
+        Args:
+            name: Name of attribute.
+            key: Key to add attribute to.
+            value: Attribute value.
+        """
+        self._metrics[_hash_key(key)].attributes[name] = value
 
-    def __delitem__(self, event: Event) -> None:
-        """Remove event from self."""
-        del self._events[event]
-
-    def __getitem__(self, event: Event) -> TimeStats:
-        """Get item corresponding to event."""
-        if not isinstance(event, Event):
-            raise TypeError(
-                f'key (event) must be of type {Event.__name__}. '
-                f'Got type {type(event)}.',
-            )
-        if event not in self._events:
-            self._events[event] = TimeStats()
-        return self._events[event]
-
-    def __iter__(self) -> Iterator[Event]:
-        """Get an iterator of events."""
-        return iter(self._events)
-
-    def __len__(self) -> int:
-        """Get number of tracked events."""
-        return len(self._events)
-
-    def __setitem__(self, event: Event, stats: TimeStats) -> None:
-        """Set stats for event."""
-        if not isinstance(event, Event):
-            raise TypeError(
-                f'key (event) must be of type {Event.__name__}. '
-                f'Got type {type(event)}.',
-            )
-        if not isinstance(stats, TimeStats):
-            raise TypeError(
-                f'value (stats) must be of type {TimeStats.__name__}. '
-                f'Got type {type(stats)}.',
-            )
+    def add_counter(self, name: str, key: KeyT, value: int) -> None:
+        """Add to a counter.
 
-        if event in self._events:
-            self._events[event] += stats
+        Args:
+            name: Name of counter.
+            key: Key associated with the counter.
+            value: Amount to increment counter by.
+        """
+        counters = self._metrics[_hash_key(key)].counters
+        if name in counters:
+            counters[name] += value
         else:
-            self._events[event] = stats
+            counters[name] = value
 
-    def keys(self) -> KeysView[Event]:
-        """Return list of events being tracked."""
-        return self._events.keys()
-
-    def _function(
-        self,
-        function: GenericCallable,
-        key_is_result: bool,
-        preset_key: NamedTuple | None,
-        *args: Any,
-        **kwargs: Any,
-    ) -> Any:
-        """Execute a wrapped function and store execution stats.
+    def add_time(self, name: str, key: KeyT, time_ns: int) -> None:
+        """Record a new time for an event.
 
         Args:
-            function (callable): function to wrap.
-            key_is_result (bool): if `True`, the key is the return value of
-                `function` rather than the first argument. (default: False).
-            preset_key (NamedTuple): optionally preset the key associated
-                with any calls to `function`. This overrides `key_is_returned`.
-            args: Arguments passed to `function`
-            kwargs: Keywords arguments passed to `function`.
+            name: Event or operation the time is for.
+            key: Key associated with the event.
+            time_ns: The time in nanoseconds of the event.
+        """
+        times = self._metrics[_hash_key(key)].times
+        if name not in times:
+            times[name] = TimeStats()
+        times[name].add_time(time_ns / 1000)
+
+    def aggregate_times(self) -> dict[str, TimeStats]:
+        """Aggregate time statistics over all keys.
 
         Returns:
-            Output of the function
+            Dictionary mapping event names to the time statistics aggregated \
+            for that event.
         """
-        start_ns = perf_counter_ns()
-        result = function(*args, **kwargs)
-        time_ns = perf_counter_ns() - start_ns
-
-        if key_is_result:
-            if isinstance(result, Proxy):
-                key = get_key(result)
-            else:
-                key = result
-        elif preset_key is not None:
-            key = preset_key
-        elif len(args) > 0:
-            key = args[0]
-        else:
-            key = None
+        times: dict[str, TimeStats] = defaultdict(TimeStats)
+        for metrics in self._metrics.values():
+            for key, value in metrics.times.items():
+                times[key] += value
+        return times
 
-        size_bytes: int | None = None
-        if function.__name__ == 'get_bytes':
-            size_bytes = len(result)
-        elif function.__name__ == 'set_bytes':
-            size_bytes = len(args[1])
-
-        event = Event(function=function.__name__, key=key)
-        self[event].add_time(time_ns / 1e6, size_bytes=size_bytes)
-
-        return result
-
-    def wrap(
-        self,
-        function: GenericCallable,
-        *,
-        key_is_result: bool = False,
-        preset_key: NamedTuple | None = None,
-    ) -> GenericCallable:
-        """Wrap a method to log stats on calls to the function.
+    def get_metrics(self, key_or_proxy: KeyT | ProxyT) -> Metrics | None:
+        """Get the metrics associated with a key.
 
         Args:
-            function (callable): function to wrap.
-            key_is_result (bool): if `True`, the key is the return value of
-                `function` rather than the first argument. (default: False).
-            preset_key (NamedTuple): optionally preset the key associated
-                with any calls to `function`. This overrides `key_is_returned`.
+            key_or_proxy: Key to get associated metrics. If a proxy or
+                sequence of proxies, the key(s) will be extracted.
 
         Returns:
-            callable with same interface as `function`.
+            Metrics associated with the key or `None` if the key does not \
+            exist.
         """
-        out_fun = partial(self._function, function, key_is_result, preset_key)
+        key_hash = _hash_key(key_or_proxy)
+        if key_hash in self._metrics:
+            return copy.deepcopy(self._metrics[key_hash])
+        return None
+
+
+def _hash_key(key_or_proxy: KeyT | ProxyT) -> int:
+    """Hashes a Store key or sequences of keys (or proxies)."""
+    key: KeyT
+    if isinstance(key_or_proxy, Proxy):
+        key = get_key(key_or_proxy)
+    elif isinstance(key_or_proxy, Sequence) and all(
+        isinstance(proxy, Proxy) for proxy in key_or_proxy
+    ):
+        key = tuple(
+            get_key(proxy) for proxy in key_or_proxy  # type: ignore[arg-type]
+        )
+    else:
+        key = key_or_proxy
 
-        return cast(GenericCallable, out_fun)
+    if isinstance(key, Sequence) and not isinstance(key, tuple):
+        return hash(tuple(key))
+    else:
+        return hash(key)
+
+
+def _weighted_avg(a1: float, n1: int, a2: float, n2: float) -> float:
+    """Compute weighted average between two separate averages.
+
+    Args:
+        a1: The first average.
+        n1: The number of samples in `a1`.
+        a2: The second average.
+        n2: The number of samples in `a2`.
+
+    Returns:
+        The weighted average between `a1` and `a2`.
+    """
+    return ((a1 * n1) + (a2 * n2)) / (n1 + n2)
```

### Comparing `proxystore-0.4.1a1/proxystore/store/utils.py` & `proxystore-0.5.0/proxystore/store/utils.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,35 +1,37 @@
 """Store utilities."""
 from __future__ import annotations
 
-from typing import NamedTuple
+from typing import Any
+from typing import Tuple
 from typing import TypeVar
 
 from proxystore.proxy import is_resolved
 from proxystore.proxy import Proxy
 from proxystore.store import base
 from proxystore.store.exceptions import ProxyStoreFactoryError
 
 T = TypeVar('T')
+ConnectorKeyT = Tuple[Any, ...]
+"""Connector key type alias."""
 
 
-def get_key(proxy: Proxy[T]) -> NamedTuple:
+def get_key(proxy: Proxy[T]) -> ConnectorKeyT:
     """Extract the key from the proxy's factory.
 
     Args:
-        proxy (Proxy): proxy instance to get key from.
+        proxy: Proxy instance to get key from.
 
     Returns:
-        The key, a NamedTuple unique to the
-        :class:`~proxystore.store.base.Store` that created the proxy..
+        The key, a NamedTuple unique to the \
+        [`Store`][proxystore.store.base.Store] that created the proxy..
 
     Raises:
-        ProxyStoreFactoryError:
-            if the proxy's factory is not an instance of
-            :class:`~proxystore.store.base.StoreFactory`.
+        ProxyStoreFactoryError: If the proxy's factory is not an instance of
+            [`StoreFactory`][proxystore.store.base.StoreFactory].
     """
     factory = proxy.__factory__
     if isinstance(factory, base.StoreFactory):
         return factory.key
     else:
         raise ProxyStoreFactoryError(
             'The proxy must contain a factory with type '
@@ -40,22 +42,26 @@
 
 def resolve_async(proxy: Proxy[T]) -> None:
     """Begin resolving proxy asynchronously.
 
     Useful if the user knows a proxy will be needed soon and wants to
     resolve the proxy concurrently with other computation.
 
-    >>> ps.proxy.resolve_async(my_proxy)
-    >>> computation_without_proxy(...)
-    >>> # p is hopefully resolved
-    >>> computation_with_proxy(my_proxy, ...)
+    ```python
+    from proxystore.store.utils import resolve_async
+
+    resolve_async(my_proxy)
+    computation_without_proxy(...)
+    # p is hopefully resolved
+    computation_with_proxy(my_proxy, ...)
+    ```
 
     Note:
         The asynchronous resolving functionality is implemented
-        by :class:`~proxystore.store.base.StoreFactory`. Factories that are not
-        of this type will error when used with this function.
+        by [`StoreFactory`][proxystore.store.base.StoreFactory]. Factories that
+        are not of this type will error when used with this function.
 
     Args:
-        proxy (Proxy): proxy instance to begin asynchronously resolving.
+        proxy: Proxy instance to begin asynchronously resolving.
     """
     if not is_resolved(proxy):
         proxy.__factory__.resolve_async()
```

### Comparing `proxystore-0.4.1a1/proxystore/utils.py` & `proxystore-0.5.0/proxystore/utils.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,75 +1,89 @@
 """General purpose utility functions."""
 from __future__ import annotations
 
 import decimal
+import importlib
 import os
-import random
 import re
 import socket
 from typing import Any
 from typing import Generator
 
 
 def chunk_bytes(
     data: bytes,
     chunk_size: int,
 ) -> Generator[bytes, None, None]:
     """Yield chunks of binary data.
 
     Args:
-        data (bytes): data to be chunked.
-        chunk_size (int): chunk size in bytes.
+        data: Data to be chunked.
+        chunk_size: Chunk size in bytes.
 
     Returns:
         Generator that yields chunks of bytes.
     """
     length = len(data)
     for index in range(0, length, chunk_size):
         yield data[index : min(index + chunk_size, length)]
 
 
-def create_key(obj: Any) -> str:
-    """Generate key for the object.
+def get_class_path(cls: type[Any]) -> str:
+    """Get the fully qualified path of a type.
 
-    .. todo::
-
-       * generate key based on object hash (Re: Issue #4)
-       * consider how to deal with key collisions
+    Example:
+        ```python
+        >>> from proxystore.connectors.connector import Connector
+        >>> get_class_path(Connector)
+        'proxystore.connectors.connector.Connector'
+        ```
 
     Args:
-        obj: object to create key for
+        cls: Class type to get fully qualified path of.
 
     Returns:
-        random 128 bit string.
+        Fully qualified path of `cls`.
     """
-    return str(random.getrandbits(128))
+    return f'{cls.__module__}.{cls.__qualname__}'
 
 
-def fullname(obj: Any) -> str:
-    """Return full name of object."""
-    if hasattr(obj, '__module__'):
-        module = obj.__module__
-    else:
-        module = obj.__class__.__module__
-    if hasattr(obj, '__name__'):
-        name = obj.__name__
-    else:
-        name = obj.__class__.__name__
-    if module is None or module == str.__module__:
-        return name
-    return f'{module}.{name}'
+def import_class(path: str) -> type[Any]:
+    """Import class via its fully qualified path.
+
+    Example:
+        ```python
+        >>> import_class('proxystore.connectors.connector.Connector')
+        <class 'proxystore.connectors.connector.Connector'>
+        ```
+
+    Args:
+        path: Fully qualified path of class to import.
+
+    Returns:
+        Imported class.
+
+    Raises:
+        ImportError: If a class at the `path` is not found.
+    """
+    module_path, _, name = path.rpartition('.')
+    if len(module_path) == 0:
+        raise ImportError(
+            f'Class path must contain at least one module. Got {path}',
+        )
+    module = importlib.import_module(module_path)
+    return getattr(module, name)
 
 
 def home_dir() -> str:
     """Return the absolute path to the proxystore home directory.
 
-    If set, ``$PROXYSTORE_HOME`` is preferred. Otherwise,
-    ``$XDG_DATA_HOME/proxystore`` is returned where ``$XDG_DATA_HOME`` defaults
-    to ``$HOME/.local/share`` if unset.
+    If set, `$PROXYSTORE_HOME` is preferred. Otherwise,
+    `$XDG_DATA_HOME/proxystore` is returned where `$XDG_DATA_HOME` defaults
+    to `$HOME/.local/share` if unset.
     """
     path = os.environ.get('PROXYSTORE_HOME')
     if path is None:
         prefix = os.environ.get('XDG_DATA_HOME') or os.path.expanduser(
             '~/.local/share',
         )
         path = os.path.join(prefix, 'proxystore')
@@ -85,23 +99,22 @@
     """Convert bytes to human readable value.
 
     Note:
         This method uses base-10 values for KB, MB, GB, etc. instead of
         base-2 values (i.e., KiB, MiB, GiB, etc.).
 
     Args:
-        size (int): byte count to make readable.
-        precision (int): number of decimal places (default: 3).
+        size: Byte value to make readable.
+        precision: Number of decimal places.
 
     Returns:
-        string with human readable number of bytes.
+        String with human readable number of bytes.
 
     Raises:
-        ValueError:
-            if size is negative.
+        ValueError: If size is negative.
     """
     kb = int(1e3)
     mb = int(1e6)
     gb = int(1e9)
     tb = int(1e12)
 
     size_ = float(size)
@@ -127,45 +140,45 @@
     return f'{value} {suffix}'
 
 
 def readable_to_bytes(size: str) -> int:
     """Convert string with bytes units to the integer value of bytes.
 
     Example:
+        ```python
         >>> readable_to_bytes('1.2 KB')
         1200
         >>> readable_to_bytes('0.6 MiB')
         629146
+        ```
 
     Args:
-        size (str): string to parse for bytes size.
+        size: String to parse for bytes size.
 
     Returns:
-        integer number of bytes parsed from the string.
+        Integer number of bytes parsed from the string.
 
     Raises:
-        ValueError:
-            if the input string contains more than two parts (i.e., a value
-            and a unit).
-        ValueError:
-            if the unit is not one of KB, MB, GB, TB, KiB, MiB, GiB, or TiB.
-        ValueError:
-            if the value cannot be cast to a float.
-    """
-    units_to_bytes = dict(
-        b=1,
-        kb=int(1e3),
-        mb=int(1e6),
-        gb=int(1e9),
-        tb=int(1e12),
-        kib=int(2**10),
-        mib=int(2**20),
-        gib=int(2**30),
-        tib=int(2**40),
-    )
+        ValueError: If the input string contains more than two parts (i.e., a
+            value and a unit).
+        ValueError: If the unit is not one of KB, MB, GB, TB, KiB, MiB, GiB,
+            or TiB.
+        ValueError: If the value cannot be cast to a float.
+    """
+    units_to_bytes = {
+        'b': 1,
+        'kb': int(1e3),
+        'mb': int(1e6),
+        'gb': int(1e9),
+        'tb': int(1e12),
+        'kib': int(2**10),
+        'mib': int(2**20),
+        'gib': int(2**30),
+        'tib': int(2**40),
+    }
 
     # Try casting size to value (will only work if no units)
     try:
         return int(float(size))
     except ValueError:
         pass
```

### Comparing `proxystore-0.4.1a1/proxystore.egg-info/SOURCES.txt` & `proxystore-0.5.0/proxystore.egg-info/SOURCES.txt`

 * *Files 24% similar despite different names*

```diff
@@ -1,105 +1,141 @@
 .gitignore
 .pre-commit-config.yaml
-.readthedocs.yaml
 LICENSE
 README.md
+mkdocs.yml
 pyproject.toml
 tox.ini
 .github/dependabot.yml
 .github/pull_request_template.md
+.github/release.yml
 .github/ISSUE_TEMPLATE/01_bug.yml
 .github/ISSUE_TEMPLATE/02_feature.yml
 .github/ISSUE_TEMPLATE/03_docs.yml
 .github/ISSUE_TEMPLATE/config.yml
+.github/workflows/cache.yml
+.github/workflows/check-docs.yml
+.github/workflows/docs.yml
 .github/workflows/integration.yml
 .github/workflows/publish.yml
 .github/workflows/tests.yml
-docs/Makefile
-docs/advanced.rst
-docs/api.rst
-docs/changelog.rst
-docs/conf.py
-docs/contributing.rst
-docs/getstarted.rst
-docs/guides.rst
-docs/index.rst
-docs/make.bat
-docs/proxy.txt
-docs/requirements.txt
-docs/_templates/autosummary/module.rst
-docs/guides/endpoints.rst
-docs/guides/performance.rst
-docs/static/dataflow.png
-docs/static/endpoints.png
-docs/static/overview.png
+docs/examples.md
+docs/generate_api.py
+docs/get-started.md
+docs/index.md
+docs/installation.md
+docs/known-issues.md
+docs/_overrides/base.html
+docs/_templates/python/material/function.html
+docs/_templates/python/material/module.html
+docs/_templates/python/material/docstring/admonition.html
+docs/api/cli.md
+docs/api/legacy-docs.md
+docs/concepts/connector.md
+docs/concepts/index.md
+docs/concepts/proxy.md
+docs/concepts/store.md
+docs/contributing/index.md
+docs/contributing/issues-pull-requests.md
+docs/contributing/releases.md
+docs/contributing/style-guide.md
+docs/css/extra.css
+docs/css/mkdocstrings.css
+docs/guides/endpoints-debugging.md
+docs/guides/endpoints.md
+docs/guides/globus-compute.md
+docs/guides/index.md
+docs/guides/performance.md
+docs/static/endpoint-overview.svg
+docs/static/endpoint-peering.svg
+docs/static/favicon.png
+docs/static/icon.png
+docs/static/logo-dark.png
+docs/static/logo-light.png
+docs/static/proxystore-overview.svg
+docs/static/proxystore-schematic.svg
 examples/.gitignore
 examples/README.md
 examples/requirements.txt
-examples/store_stats.py
-examples/funcx/README.md
-examples/funcx/mapreduce_funcx.py
-examples/funcx/run.sh
+examples/store_metrics.py
+examples/globus-compute/README.md
+examples/globus-compute/mapreduce_globus_compute.py
+examples/globus-compute/run.sh
 examples/parsl/README.md
 examples/parsl/mapreduce_parsl.py
 examples/parsl/run.sh
 proxystore/__init__.py
 proxystore/factory.py
 proxystore/globus.py
 proxystore/proxy.py
 proxystore/py.typed
 proxystore/serialize.py
+proxystore/timer.py
 proxystore/utils.py
+proxystore/warnings.py
 proxystore.egg-info/PKG-INFO
 proxystore.egg-info/SOURCES.txt
 proxystore.egg-info/dependency_links.txt
 proxystore.egg-info/entry_points.txt
 proxystore.egg-info/requires.txt
 proxystore.egg-info/top_level.txt
+proxystore/connectors/__init__.py
+proxystore/connectors/connector.py
+proxystore/connectors/endpoint.py
+proxystore/connectors/file.py
+proxystore/connectors/globus.py
+proxystore/connectors/local.py
+proxystore/connectors/multi.py
+proxystore/connectors/redis.py
+proxystore/connectors/dim/__init__.py
+proxystore/connectors/dim/exceptions.py
+proxystore/connectors/dim/margo.py
+proxystore/connectors/dim/models.py
+proxystore/connectors/dim/ucx.py
+proxystore/connectors/dim/utils.py
+proxystore/connectors/dim/zmq.py
 proxystore/endpoint/__init__.py
 proxystore/endpoint/cli.py
+proxystore/endpoint/client.py
 proxystore/endpoint/commands.py
 proxystore/endpoint/config.py
 proxystore/endpoint/constants.py
 proxystore/endpoint/endpoint.py
 proxystore/endpoint/exceptions.py
 proxystore/endpoint/messages.py
 proxystore/endpoint/serve.py
 proxystore/endpoint/storage.py
 proxystore/p2p/__init__.py
 proxystore/p2p/chunks.py
-proxystore/p2p/client.py
 proxystore/p2p/connection.py
 proxystore/p2p/counter.py
 proxystore/p2p/exceptions.py
 proxystore/p2p/manager.py
 proxystore/p2p/messages.py
-proxystore/p2p/server.py
+proxystore/p2p/relay.py
+proxystore/p2p/relay_client.py
 proxystore/p2p/task.py
 proxystore/store/__init__.py
 proxystore/store/base.py
 proxystore/store/cache.py
 proxystore/store/endpoint.py
 proxystore/store/exceptions.py
 proxystore/store/file.py
 proxystore/store/globus.py
 proxystore/store/local.py
+proxystore/store/metrics.py
+proxystore/store/multi.py
 proxystore/store/redis.py
-proxystore/store/stats.py
 proxystore/store/utils.py
-proxystore/store/dim/__init__.py
-proxystore/store/dim/margo.py
-proxystore/store/dim/ucx.py
-proxystore/store/dim/utils.py
-proxystore/store/dim/websockets.py
 testing/__init__.py
 testing/compat.py
+testing/connectors.py
 testing/endpoint.py
 testing/mocking.py
-testing/signaling_server.py
+testing/relay_server.py
 testing/stores.py
 testing/utils.py
 testing/mocked/__init__.py
 testing/mocked/globus.py
 testing/mocked/pymargo.py
 testing/mocked/redis.py
 testing/mocked/ucx.py
@@ -109,45 +145,50 @@
 testing/scripts/peer_manager_bandwidth.py
 tests/__init__.py
 tests/conftest.py
 tests/factory_test.py
 tests/globus_test.py
 tests/proxy_test.py
 tests/serialization_test.py
+tests/timer_test.py
 tests/utils_test.py
+tests/connectors/__init__.py
+tests/connectors/connector_test.py
+tests/connectors/endpoint_test.py
+tests/connectors/file_test.py
+tests/connectors/globus_test.py
+tests/connectors/local_test.py
+tests/connectors/multi_test.py
+tests/connectors/redis_test.py
+tests/connectors/dim/__init__.py
+tests/connectors/dim/margo_test.py
+tests/connectors/dim/ucx_test.py
+tests/connectors/dim/zmq_test.py
 tests/endpoint/__init__.py
 tests/endpoint/cli_test.py
+tests/endpoint/client_test.py
 tests/endpoint/commands_test.py
 tests/endpoint/config_test.py
 tests/endpoint/endpoint_peering_test.py
 tests/endpoint/endpoint_solo_test.py
 tests/endpoint/serve_test.py
 tests/endpoint/storage_test.py
 tests/integration/__init__.py
 tests/integration/endpoints_test.py
 tests/p2p/__init__.py
 tests/p2p/chunks_test.py
-tests/p2p/client_test.py
 tests/p2p/connection_test.py
 tests/p2p/counter_test.py
 tests/p2p/manager_test.py
 tests/p2p/messages_test.py
-tests/p2p/server_cli_test.py
-tests/p2p/server_test.py
+tests/p2p/relay_cli_test.py
+tests/p2p/relay_client_test.py
+tests/p2p/relay_test.py
 tests/p2p/task_test.py
 tests/store/__init__.py
 tests/store/cache_test.py
-tests/store/endpoint_test.py
-tests/store/file_test.py
-tests/store/globus_test.py
 tests/store/init_test.py
-tests/store/local_test.py
-tests/store/redis_test.py
-tests/store/stats_test.py
+tests/store/metrics_test.py
 tests/store/store_basics_test.py
+tests/store/store_metrics_test.py
 tests/store/store_proxy_test.py
-tests/store/store_stats_test.py
-tests/store/utils_test.py
-tests/store/dim/__init__.py
-tests/store/dim/margo_test.py
-tests/store/dim/ucx_test.py
-tests/store/dim/websockets_test.py
+tests/store/utils_test.py
```

### Comparing `proxystore-0.4.1a1/testing/compat.py` & `proxystore-0.5.0/testing/compat.py`

 * *Files 20% similar despite different names*

```diff
@@ -9,16 +9,16 @@
 def randbytes(size: int) -> bytes:
     """Get random byte string of specified size.
 
     Uses `random.randbytes()` in Python 3.9 or newer and
     `os.urandom()` in Python 3.8 and older.
 
     Args:
-        size (int): size of byte string to return.
+        size: The size of byte string to return.
 
     Returns:
-        random byte string.
+        A random byte string.
     """
     if sys.version_info >= (3, 9):  # pragma: >=3.9 cover
         return random.randbytes(size)
     else:  # pragma: <3.9 cover
         return os.urandom(size)
```

### Comparing `proxystore-0.4.1a1/testing/endpoint.py` & `proxystore-0.5.0/testing/endpoint.py`

 * *Files 3% similar despite different names*

```diff
@@ -45,15 +45,16 @@
 
     while True:
         try:
             r = requests.get(f'http://{host}:{port}/')
         except requests.exceptions.ConnectionError as e:
             if waited_s >= max_time_s:  # pragma: no cover
                 raise RuntimeError(
-                    'Unable to connect to endpoint with {max_time_s} seconds.',
+                    'Unable to connect to endpoint within the timeout '
+                    f'({max_time_s} seconds).',
                 ) from e
             time.sleep(sleep_s)
             waited_s += sleep_s
             continue
         if r.status_code == 200:  # pragma: no branch
             break
 
@@ -62,15 +63,15 @@
 def endpoint(use_uvloop: bool) -> Generator[EndpointConfig, None, None]:
     """Launch endpoint in subprocess."""
     config = EndpointConfig(
         name='endpoint-fixture',
         uuid=uuid.uuid4(),
         host='localhost',
         port=open_port(),
-        server=None,
+        relay_server=None,
     )
     server_handle = Process(
         target=serve_endpoint_silent,
         args=[config],
         kwargs={'use_uvloop': use_uvloop},
     )
     server_handle.start()
```

### Comparing `proxystore-0.4.1a1/testing/mocked/globus.py` & `proxystore-0.5.0/testing/mocked/globus.py`

 * *Files 14% similar despite different names*

```diff
@@ -7,19 +7,17 @@
 import globus_sdk
 
 
 class MockTransferData(globus_sdk.TransferData):
     """Mock the Globus TransferData."""
 
     def __init__(self, *args, **kwargs):
-        """Init MockTransferData."""
         pass
 
     def __setitem__(self, key, item):
-        """Set item."""
         self.__dict__[key] = item
 
     def add_item(
         self,
         source_path: str,
         destination_path: str,
         **kwargs: Any,
@@ -29,31 +27,28 @@
         assert isinstance(destination_path, str)
 
 
 class MockDeleteData(globus_sdk.DeleteData):
     """Mock the Globus DeleteData."""
 
     def __init__(self, *args, **kwargs):
-        """Init MockDeleteData."""
         pass
 
     def __setitem__(self, key, item):
-        """Set item."""
         self.__dict__[key] = item
 
     def add_item(self, path: str, **kwargs: Any) -> None:
-        """Add item."""
+        """Add an item to the object."""
         assert isinstance(path, str)
 
 
 class MockTransferClient:
     """Mock the Globus TransferClient."""
 
     def __init__(self, *args, **kwargs):
-        """Init MockTransferClient."""
         pass
 
     def get_task(self, task_id: str) -> Any:
         """Get task."""
         assert isinstance(task_id, str)
         return None
```

### Comparing `proxystore-0.4.1a1/testing/mocked/pymargo.py` & `proxystore-0.5.0/testing/mocked/pymargo.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,57 +1,62 @@
 """PyMargo mocker implementation."""
 from __future__ import annotations
 
 from typing import Any
 
+from proxystore.connectors.dim.models import DIMKey
+from proxystore.connectors.dim.models import RPCResponse
 from proxystore.serialize import serialize
 
 # pymargo vars
 client = 'client'
 server = 'server'
 
 # server dictionary
-data_dict = {}
+data_dict: dict[str, bytes] = {}
 
 
 class MargoException(Exception):  # pragma: no cover  # noqa: N818
     """Mock Exception implementation."""
 
     def __init__(self):
-        """Exception init implementation."""
         pass
 
 
 class Address:  # pragma: no cover
     """Mock Address implementation."""
 
-    def __init__(self) -> None:
-        """Mock Address initialization."""
-        pass
+    def __init__(self, url):
+        self.addr = url
 
     def shutdown(self) -> None:
         """Mock shutdown."""
         pass
 
+    def __str__(self) -> str:
+        return self.addr
+
 
 class Engine:
     """Mock Engine implementation."""
 
     def __init__(
         self,
         url: str,
         mode: str = server,
         use_progress_thread: bool = False,
     ) -> None:
-        """Mock Engine initialization."""
-        self.url = url
+        if url is None or '://' not in url:
+            self.address = Address('tcp://127.0.0.1:1234')
+        else:
+            self.address = Address(url)
 
-    def addr(self) -> str:
-        """Get Mock Engine address."""
-        return self.url
+    def addr(self) -> Address:
+        """Mock Engine addr implementation."""
+        return self.address
 
     def on_finalize(self, func: Any) -> None:
         """Mock engine on_finalize."""
         pass
 
     def enable_remote_shutdown(self) -> None:
         """Mock engine enable_remote_shutdown."""
@@ -61,21 +66,17 @@
         """Mock engine wait_for_finalize."""
         pass
 
     def create_bulk(self, data: bytes, bulk_type: str) -> Bulk:
         """Mock create_bulk implementation."""
         return Bulk(data)
 
-    def lookup(self, addr: str) -> Engine:
+    def lookup(self, addr: str) -> Address:
         """Mock lookup implementation."""
-        return self
-
-    def shutdown(self) -> None:
-        """Mock shutdown."""
-        pass
+        return self.address
 
     def finalize(self) -> None:
         """Mock finalize."""
         pass
 
     def transfer(
         self,
@@ -95,75 +96,69 @@
             assert isinstance(local_bulk.data, bytearray)
             local_bulk.data[:] = bulk_str.data
 
         else:
             assert isinstance(bulk_str.data, bytearray)
             bulk_str.data[:] = local_bulk.data
 
-    def register(self, funcname: str, *args: Any) -> RPC:
+    def register(self, funcname: str, *args: Any) -> RemoteFunction:
         """Mock register.
 
         Args:
-            funcname (str): the function name.
-            args (Any): additional positional arguments.
-
+            funcname: The function name.
+            args: Additional positional arguments.
         """
-        return RPC(funcname)
+        return RemoteFunction(funcname)
 
 
-class RPC:
-    """Mock RPC implementation."""
+class RemoteFunction:
+    """Mock RemoteFunction implementation."""
 
     def __init__(self, name: str) -> None:
-        """Mock RPC initialization."""
         self.name = name
 
     def on(self, addr: str) -> Any:
-        """Mock RPC on implementation."""
+        """Mock RemoteFunction on implementation."""
         return self.mockfunc
 
     def mockfunc(
         self,
         array_str: Bulk,
         size: int,
-        key: str,
+        key: DIMKey,
     ) -> Any:
         """Mockfunc implementation."""
-        from proxystore.store.dim.utils import Status
-
-        if self.name == 'set':
-            data_dict[key] = array_str.data
-            return serialize(Status(True, None))
+        if self.name == 'put':
+            data_dict[key.obj_id] = array_str.data
+            return serialize(RPCResponse(operation='put', key=key))
         elif self.name == 'get':
-            if key not in data_dict:
+            if key.obj_id not in data_dict:
                 return serialize(
-                    Status(
-                        False,
-                        Exception('MockException occurred in `get_bytes`'),
-                    ),
+                    RPCResponse(operation='get', key=key, exists=False),
                 )
             else:
                 assert isinstance(array_str.data, bytearray)
-                array_str.data[:] = data_dict[key]
-            return serialize(Status(True, None))
+                array_str.data[:] = data_dict[key.obj_id]
+            return serialize(
+                RPCResponse(operation='get', key=key, exists=True),
+            )
         elif self.name == 'evict':
-            if key not in data_dict:
-                return serialize(
-                    Status(
-                        False,
-                        Exception('MockException occurred in `evict`'),
-                    ),
-                )
+            if key.obj_id not in data_dict:
+                return serialize(RPCResponse(operation='evict', key=key))
             else:
-                del data_dict[key]
-            return serialize(Status(True, None))
+                del data_dict[key.obj_id]
+            return serialize(RPCResponse(operation='evict', key=key))
         else:
-            assert isinstance(array_str.data, bytearray)
-            array_str.data[:] = serialize(key in data_dict)
-            return serialize(Status(True, None))
+            return serialize(
+                RPCResponse(
+                    operation='exists',
+                    key=key,
+                    exists=(key.obj_id in data_dict),
+                ),
+            )
 
 
 class MockBulkMod:
     """MockBulkMod implementation."""
 
     # bulk variable
     read_write = 'rw'
@@ -175,42 +170,25 @@
 
 bulk = MockBulkMod()
 
 
 class Bulk:
     """Mock Bulk implementation."""
 
-    data: bytearray | bytes
-
     def __init__(self, data: bytearray | bytes) -> None:
-        """Mock Bulk initialization."""
         self.data = data
 
 
 class Handle:
     """Mock Handle implementation."""
 
-    response: Any
-
     def __init__(self) -> None:
-        """Mock handle initialization."""
-        from proxystore.store.dim.utils import Status
-
-        self.response = Status(True, None)
+        self.response: Any = None
 
-    def respond(
-        self,
-        status: Any,
-    ) -> Any:
+    def respond(self, response: Any) -> None:
         """Mock respond."""
-        self.response = status
-        return self.response
+        self.response = response
+        return None
 
     def get_addr(self) -> str:
         """Mock addr."""
         return 'addr'
-
-
-class RemoteFunction:
-    """Remote function implementation."""
-
-    pass
```

### Comparing `proxystore-0.4.1a1/testing/mocked/ucx.py` & `proxystore-0.5.0/testing/mocked/ucx.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 """UCX mocker implementation."""
 from __future__ import annotations
 
 from typing import Any
 
+from proxystore.connectors.dim.models import RPC
+from proxystore.connectors.dim.models import RPCResponse
 from proxystore.serialize import deserialize
-from proxystore.serialize import SerializationError
 from proxystore.serialize import serialize
 
-data = {}
+data: dict[str, bytes] = {}
 
 
 class Lib:
     """Mock ucp Lib implementation."""
 
     def __init__(self):
-        """Mock lib init implementation."""
         pass
 
     class exceptions:  # noqa: N801
         """Mock Lib exceptions implementation."""
 
         class UCXNotConnected(Exception):  # noqa: 818
             """Mock Exception implementation."""
@@ -26,120 +26,105 @@
             pass
 
 
 _libs = Lib()
 
 
 class MockEndpoint:
-    """Mock Endpoint."""
+    """Mock Endpoint.
 
-    last_event: str
-    key: str
-    response: str | int
-    req: Any
-    server: Any
-    is_closed: bool
-
-    def __init__(self, server=False):
-        """Initialize a MockEndpoint."""
-        self.key = ''
-        self.last_event = ''
-        self.response = ''
-        self.req = None
+    This class mocks all the expected behavior of the UCXServer
+    on the client side.
+    """
+
+    def __init__(self, server: bool = False):
+        self.last_rpc: RPC | None = None
         self.server = server
         self.is_closed = False
+        self.ping = False
 
-    async def send_obj(self, req: Any) -> None:
+    async def send_obj(self, payload: bytes) -> None:
         """Mock the `ucp.send_obj` function.
 
         Args:
-            req (Any): the object to communicate
-
+            payload: The serialized object communicated.
         """
-        self.req = None
-        if self.server:
-            self.req = req
-            return self.req
-
-        try:
-            event = deserialize(req)
-        except SerializationError:
-            event = {}
-            event['op'] = 'exists'
-            event['key'] = ''
-            self.response = 1
+        if payload == b'ping':
+            self.ping = True
+            return
 
-        if event['op'] == 'set':
-            data[event['key']] = event['data']
+        rpc = deserialize(payload)
 
-        self.key = event['key']
-        self.last_event = event['op']
+        if rpc.operation == 'evict':
+            data.pop(rpc.key.obj_id, None)
+        elif rpc.operation == 'put':
+            data[rpc.key.obj_id] = rpc.data
 
-    async def recv_obj(self) -> Any:
-        """Mock the `ucp.recv_obj` function."""
-        from proxystore.store.dim.utils import Status
+        self.last_rpc = rpc
 
-        if self.req is not None:
-            return self.req
+    async def recv_obj(self) -> bytes:
+        """Mock the `ucp.recv_obj` function."""
+        if self.ping:
+            self.ping = False
+            return b'pong'
+
+        if self.last_rpc is None:
+            raise AssertionError('Called recv_obj before send_obj.')
+
+        response = RPCResponse(
+            operation=self.last_rpc.operation,
+            key=self.last_rpc.key,
+        )
+        if response.operation == 'exists':
+            response.exists = response.key.obj_id in data
+        elif response.operation == 'get':
+            response.data = data.get(response.key.obj_id, None)
 
-        if self.last_event == 'get':
-            try:
-                return data[self.key]
-            except KeyError as e:
-                return serialize(Status(success=False, error=e))
-        elif self.last_event == 'exists':
-            if self.key != '':
-                return serialize(self.key in data)
-            else:
-                return self.response
-        elif self.last_event == 'evict':
-            data.pop(self.key, None)
-            return serialize(Status(success=True, error=None))
-        return serialize(True)
+        return serialize(response)
 
     async def close(self) -> None:
         """Mock close implementation."""
         self.is_closed = True
 
     def closed(self) -> bool:
         """Mock closed implementation."""
         return self.is_closed
 
 
-class Listener:
+class Listener:  # pragma: no cover
     """Mock listener implementation."""
 
     called: bool
 
     def __init__(self) -> None:
-        """Mock listener init implementation."""
         self.called = False
 
     def close(self) -> None:
         """Close implementation."""
         pass
 
     def closed(self) -> bool:
         """Mock closed."""
         if not self.called:
             self.called = True
             return False
         return True
 
 
-def create_listener(handler: Any, port: int) -> Any:
+def create_listener(handler: Any, port: int) -> Any:  # pragma: no cover
     """Create_listener mock implementation.
 
     Args:
-        handler (Any): the communication handler
-        port (int): the communication port
-
+        handler: The communication handler.
+        port: The communication port.
     """
     return Listener()
 
 
-async def create_endpoint(
-    host: str,
-    port: int,
-) -> MockEndpoint:
+async def create_endpoint(host: str, port: int) -> MockEndpoint:
     """Create endpoint mock implementation."""
     return MockEndpoint()
+
+
+def get_address(ifname: str | None = None) -> str:
+    """Mock get_address implementation."""
+    return '127.0.0.1'
```

### Comparing `proxystore-0.4.1a1/testing/mocking.py` & `proxystore-0.5.0/testing/mocking.py`

 * *Files 10% similar despite different names*

```diff
@@ -29,14 +29,14 @@
     amock.side_effect = return_once
 
     return amock
 
 
 @contextlib.contextmanager
 def mock_multiprocessing() -> Generator[None, None, None]:
-    """Mock Process.{start,join,terminate}."""
-    with mock.patch('multiprocessing.Process.start'), mock.patch(
-        'multiprocessing.Process.join',
+    """Mock `Process.{start,join,terminate}`."""
+    with mock.patch('multiprocessing.process.BaseProcess.start'), mock.patch(
+        'multiprocessing.process.BaseProcess.join',
     ), mock.patch(
-        'multiprocessing.Process.terminate',
+        'multiprocessing.process.BaseProcess.terminate',
     ):
         yield
```

### Comparing `proxystore-0.4.1a1/testing/scripts/peer_connection_bandwidth.py` & `proxystore-0.5.0/testing/scripts/peer_connection_bandwidth.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,55 +10,55 @@
 from typing import Sequence
 
 if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
     from typing import Literal
 else:  # pragma: <3.8 cover
     from typing_extensions import Literal
 
-from proxystore.p2p import messages
-from proxystore.p2p.client import connect
 from proxystore.p2p.connection import PeerConnection
+from proxystore.p2p.relay_client import RelayServerClient
 from testing.compat import randbytes
 
 
 async def get_connection(
     actor: Literal['producer', 'consumer'],
-    server: str,
+    relay: str,
     channels: int = 1,
 ) -> PeerConnection:
     """Return a ready PeerConnection."""
-    local_uuid, name, websocket = await connect(server)
-    connection = PeerConnection(local_uuid, name, websocket, channels=channels)
+    client = RelayServerClient(relay)
+    local_uuid = client.uuid
+    connection = PeerConnection(client, channels=channels)
 
     print(f'{actor} uuid: {local_uuid}')
     remote_uuid = uuid.UUID(input('enter the remote uuid: ').strip())
 
     if actor == 'producer':
         await connection.send_offer(remote_uuid)
-        answer = messages.decode(await websocket.recv())  # type: ignore
+        answer = await client.recv()
         await connection.handle_server_message(answer)  # type: ignore
     elif actor == 'consumer':
-        offer = messages.decode(await websocket.recv())  # type: ignore
+        offer = await client.recv()
         await connection.handle_server_message(offer)  # type: ignore
 
     await connection.ready()
 
     print(f'{actor} connection to remote with uuid {remote_uuid}')
 
     return connection
 
 
 async def amain(
     actor: Literal['producer', 'consumer'],
     size: int,
-    server: str,
+    relay: str,
     channels: int = 1,
 ) -> None:
     """Measure transfer speed between producer and consumer."""
-    connection = await get_connection(actor, server, channels)
+    connection = await get_connection(actor, relay, channels)
 
     data: str | bytes
     if actor == 'producer':
         data = randbytes(size)
         start = time.perf_counter()
         await connection.send(data)
         assert await connection.recv() == 'done'
@@ -92,16 +92,16 @@
     )
     parser.add_argument(
         '--size',
         type=int,
         help='message length in bytes',
     )
     parser.add_argument(
-        '--server',
-        help='signaling server address',
+        '--relay',
+        help='relay server address',
     )
     parser.add_argument(
         '--channels',
         type=int,
         default=1,
         help='number of datachannels to split message sending over',
     )
@@ -125,15 +125,15 @@
             print('using uvloop')
         except ImportError:
             print('uvloop unavailable... using default asyncio event loop')
 
     logging.basicConfig()
 
     asyncio.run(
-        amain(args.actor, args.size, args.server, args.channels),
+        amain(args.actor, args.size, args.relay, args.channels),
         debug=args.debug,
     )
 
     return 0
 
 
 if __name__ == '__main__':
```

### Comparing `proxystore-0.4.1a1/testing/scripts/peer_endpoint_bandwidth.py` & `proxystore-0.5.0/testing/scripts/peer_endpoint_bandwidth.py`

 * *Files 10% similar despite different names*

```diff
@@ -17,39 +17,39 @@
 
 from proxystore.endpoint.endpoint import Endpoint
 from testing.compat import randbytes
 
 
 async def get_endpoint(
     actor: Literal['local', 'remote'],
-    server: str,
+    relay: str,
 ) -> tuple[Endpoint, uuid.UUID | None]:
     """Return a ready PeerConnection."""
     endpoint = await Endpoint(
         name=socket.gethostname(),
         uuid=uuid.uuid4(),
-        signaling_server=server,
+        relay_server=relay,
     )
 
     print(f'Endpoint uuid: {endpoint.uuid}')
     if actor == 'local':
-        remote_uuid = uuid.UUID(input('Enter the remote\'s uuid: ').strip())
+        remote_uuid = uuid.UUID(input("Enter the remote's uuid: ").strip())
     else:
         remote_uuid = None
 
     return endpoint, remote_uuid
 
 
 async def amain(
     actor: Literal['local', 'remote'],
     size: int,
-    server: str,
+    relay: str,
 ) -> None:
     """Measure transfer speed between producer and consumer."""
-    endpoint, target_uuid = await get_endpoint(actor, server)
+    endpoint, target_uuid = await get_endpoint(actor, relay)
 
     if actor == 'local':
         print('Testing connection to remote')
         assert not await endpoint.exists('key', target_uuid)
         print('Connection established')
 
         print(f'Sending {size} bytes to remote')
@@ -94,16 +94,16 @@
     )
     parser.add_argument(
         '--size',
         type=int,
         help='size of data to move',
     )
     parser.add_argument(
-        '--server',
-        help='signaling server address',
+        '--relay',
+        help='relay server address',
     )
     parser.add_argument(
         '--no-uvloop',
         action='store_true',
         help='override using uvloop if available',
     )
     parser.add_argument(
@@ -125,14 +125,14 @@
             uvloop.install()
             print('using uvloop')
         except ImportError:
             print('uvloop unavailable... using default asyncio event loop')
 
     logging.basicConfig()
 
-    asyncio.run(amain(args.actor, args.size, args.server), debug=args.debug)
+    asyncio.run(amain(args.actor, args.size, args.relay), debug=args.debug)
 
     return 0
 
 
 if __name__ == '__main__':
     raise SystemExit(main())
```

### Comparing `proxystore-0.4.1a1/testing/scripts/peer_manager_bandwidth.py` & `proxystore-0.5.0/testing/scripts/peer_manager_bandwidth.py`

 * *Files 4% similar despite different names*

```diff
@@ -16,18 +16,18 @@
 
 from proxystore.p2p.manager import PeerManager
 from testing.compat import randbytes
 
 
 async def get_manager(
     actor: Literal['producer', 'consumer'],
-    server: str,
+    relay: str,
 ) -> tuple[PeerManager, uuid.UUID]:
     """Return a ready PeerManager."""
-    manager = await PeerManager(uuid.uuid4(), server)
+    manager = await PeerManager(uuid.uuid4(), relay)
 
     print(f'{actor} uuid: {manager.uuid}')
     remote_uuid = uuid.UUID(input('enter the remote uuid: ').strip())
 
     if actor == 'producer':
         await manager.send(remote_uuid, 'hello')
     elif actor == 'consumer':
@@ -41,18 +41,18 @@
 
     return manager, remote_uuid
 
 
 async def amain(
     actor: Literal['producer', 'consumer'],
     size: int,
-    server: str,
+    relay: str,
 ) -> None:
     """Measure transfer speed between producer and consumer."""
-    manager, remote_uuid = await get_manager(actor, server)
+    manager, remote_uuid = await get_manager(actor, relay)
 
     data: str | bytes
     if actor == 'producer':
         data = randbytes(size)
         start = time.perf_counter()
         await manager.send(remote_uuid, data)
         _, message = await manager.recv()
@@ -87,16 +87,16 @@
     )
     parser.add_argument(
         '--size',
         type=int,
         help='message length in bytes',
     )
     parser.add_argument(
-        '--server',
-        help='signaling server address',
+        '--relay',
+        help='relay server address',
     )
     parser.add_argument(
         '--no-uvloop',
         action='store_true',
         help='override using uvloop if available',
     )
     parser.add_argument(
@@ -113,14 +113,14 @@
             uvloop.install()
             print('using uvloop')
         except ImportError:
             print('uvloop unavailable... using default asyncio event loop')
 
     logging.basicConfig()
 
-    asyncio.run(amain(args.actor, args.size, args.server), debug=args.debug)
+    asyncio.run(amain(args.actor, args.size, args.relay), debug=args.debug)
 
     return 0
 
 
 if __name__ == '__main__':
     raise SystemExit(main())
```

### Comparing `proxystore-0.4.1a1/testing/signaling_server.py` & `proxystore-0.5.0/testing/relay_server.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,58 +1,58 @@
-"""Tools for running a local signaling server for unit tests."""
+"""Tools for running a local relay server for unit tests."""
 from __future__ import annotations
 
 from typing import AsyncGenerator
 from typing import NamedTuple
 
 import pytest
 import pytest_asyncio
 import websockets
 from websockets.server import WebSocketServer
 
-from proxystore.p2p.server import SignalingServer
+from proxystore.p2p.relay import RelayServer
 from testing.utils import open_port
 
 
-class SignalingServerInfo(NamedTuple):
-    """NamedTuple returned by signaling_server fixture."""
+class RelayServerInfo(NamedTuple):
+    """NamedTuple returned by relay_server fixture."""
 
-    signaling_server: SignalingServer
+    relay_server: RelayServer
     websocket_server: WebSocketServer
     host: str
     port: int
     address: str
 
 
 @pytest_asyncio.fixture(scope='session')
-@pytest.mark.asyncio
-async def signaling_server(
+@pytest.mark.asyncio()
+async def relay_server(
     event_loop,
-) -> AsyncGenerator[SignalingServerInfo, None]:
-    """Fixture that runs signaling server locally.
+) -> AsyncGenerator[RelayServerInfo, None]:
+    """Fixture that runs relay server locally.
 
     Warning:
-        This fixture has session scope so the signaling server will be shared
+        This fixture has session scope so the relay server will be shared
         between many tests.
 
     Yields:
-        `SignalingServerInfo <.SignalingServerInfo>`
+        `RelayServerInfo <.RelayServerInfo>`
     """
     host = 'localhost'
     port = open_port()
     address = f'ws://{host}:{port}'
 
-    signaling_server = SignalingServer()
+    relay_server = RelayServer()
     async with websockets.server.serve(
-        signaling_server.handler,
+        relay_server.handler,
         host,
         port,
     ) as websocket_server:
-        server_info = SignalingServerInfo(
-            signaling_server=signaling_server,
+        server_info = RelayServerInfo(
+            relay_server=relay_server,
             websocket_server=websocket_server,
             host=host,
             port=port,
             address=address,
         )
         assert websocket_server.is_serving()
         yield server_info
```

### Comparing `proxystore-0.4.1a1/tests/conftest.py` & `proxystore-0.5.0/tests/conftest.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 """Public fixtures for unit tests."""
 from __future__ import annotations
 
 import asyncio
 import contextlib
+import platform
 import sys
 from typing import Any
 from typing import ContextManager
 from typing import Generator
 from unittest import mock
 
 import pytest
@@ -24,28 +25,35 @@
 try:
     import ucp
 except ImportError:
     from testing.mocked import ucx
 
     sys.modules['ucp'] = ucx
 
-
 # Import fixtures from testing/ so they are known by pytest
 # and can be used with
+from testing.connectors import connectors
+from testing.connectors import endpoint_connector
+from testing.connectors import file_connector
+from testing.connectors import globus_connector
+from testing.connectors import local_connector
+from testing.connectors import margo_connector
+from testing.connectors import multi_connector
+from testing.connectors import redis_connector
+from testing.connectors import ucx_connector
+from testing.connectors import zmq_connector
 from testing.endpoint import endpoint
-from testing.signaling_server import signaling_server
+from testing.relay_server import relay_server
 from testing.stores import endpoint_store
 from testing.stores import file_store
 from testing.stores import globus_store
 from testing.stores import local_store
-from testing.stores import margo_store
+from testing.stores import multi_store
 from testing.stores import redis_store
 from testing.stores import store_implementation
-from testing.stores import ucx_store
-from testing.stores import websocket_store
 
 
 def pytest_addoption(parser):
     """Add custom command line options for tests."""
     parser.addoption(
         '--use-uvloop',
         action='store_true',
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/cli_test.py` & `proxystore-0.5.0/tests/p2p/relay_cli_test.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,134 +1,142 @@
 from __future__ import annotations
 
-import logging
+import asyncio
+import multiprocessing
 import os
 import pathlib
 import subprocess
-import uuid
-from typing import Generator
+import sys
 from unittest import mock
 
+import click
+import click.testing
 import pytest
+import websockets
 
-import proxystore
-from proxystore.endpoint.cli import main
-from proxystore.endpoint.config import read_config
-
-
-@pytest.fixture()
-def home_dir(tmp_path: pathlib.Path) -> Generator[str, None, None]:
-    with mock.patch(
-        'proxystore.utils.home_dir',
-        return_value=str(tmp_path),
-    ), mock.patch(
-        'proxystore.endpoint.commands.home_dir',
-        return_value=str(tmp_path),
-    ):
-        yield str(tmp_path)
-
-
-def test_no_args_prints_help(capsys) -> None:
-    with pytest.raises(SystemExit):
-        main([])
-    captured = capsys.readouterr()
-    assert captured.out.startswith('usage: proxystore-endpoint [-h]')
-
-
-def test_help_with_no_command(capsys) -> None:
-    with pytest.raises(SystemExit):
-        main(['help'])
-    captured = capsys.readouterr()
-    assert captured.out.startswith('usage: proxystore-endpoint [-h]')
-
-
-def test_help_with_command(capsys) -> None:
-    with pytest.raises(SystemExit):
-        main(['help', 'list'])
-    captured = capsys.readouterr()
-    assert captured.out.startswith('usage: proxystore-endpoint list [-h]')
-
-
-def test_configure(home_dir) -> None:
-    name = 'my-endpoint'
-    port = 4321
-    server = 'ws://server:1234'
-    main(
-        [
-            'configure',
-            name,
-            '--port',
-            str(port),
-            '--server',
-            server,
-        ],
-    )
+from proxystore.p2p.relay import cli
+from proxystore.p2p.relay import serve
+from proxystore.p2p.relay_client import RelayServerClient
+from testing.utils import open_port
 
-    endpoint_dir = os.path.join(home_dir, name)
-    assert os.path.isdir(endpoint_dir)
-    cfg = read_config(endpoint_dir)
-    assert cfg.name == name
-    assert cfg.port == port
-    assert cfg.server == server
-
-
-def test_list(home_dir, caplog) -> None:
-    # Note: because home_dir is mocked, there's nothing to list so we
-    # are really testing that the correct command in
-    # proxystore.endpoint.commands is called and leaving the testing of that
-    # command to tests/endpoint/commands_test.py.
-    caplog.set_level(logging.INFO)
-    main(['list'])
-    assert len(caplog.records) == 1
-    assert 'No valid endpoint configurations' in caplog.records[0].message
-
-
-def test_remove(home_dir, caplog) -> None:
-    # Note: similar to test_list()
-    caplog.set_level(logging.ERROR)
-    main(['remove', 'my-endpoint'])
-    assert len(caplog.records) == 1
-    assert any(
-        ['does not exist' in record.message for record in caplog.records],
-    )
+if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
+    from unittest.mock import AsyncMock
+else:  # pragma: <3.8 cover
+    from asynctest import CoroutineMock as AsyncMock
 
 
-def test_start(home_dir, caplog) -> None:
-    # Note: similar to test_list()
-    caplog.set_level(logging.ERROR)
-    main(['start', 'my-endpoint'])
-    assert len(caplog.records) == 2
-    assert any(
-        ['does not exist' in record.message for record in caplog.records],
-    )
+def test_invoke() -> None:
+    runner = click.testing.CliRunner()
+    with mock.patch('proxystore.p2p.relay.serve', AsyncMock()):
+        runner.invoke(cli)
 
 
-def test_stop(home_dir, caplog) -> None:
-    # Note: similar to test_list()
-    caplog.set_level(logging.ERROR)
-    main(['stop', 'my-endpoint'])
-    assert len(caplog.records) == 2
-    assert any(
-        ['does not exist' in record.message for record in caplog.records],
-    )
+def test_invoke_with_log_dir(tmp_path: pathlib.Path) -> None:
+    tmp_dir = os.path.join(tmp_path, 'log-dir')
+    assert not os.path.isdir(tmp_dir)
+    runner = click.testing.CliRunner()
+    with mock.patch('proxystore.p2p.relay.serve', AsyncMock()):
+        runner.invoke(cli, ['--log-dir', str(tmp_dir)])
+    assert os.path.isdir(tmp_dir)
 
 
-@pytest.mark.skipif('not config.getoption("extras")')
-def test_entry_point() -> None:  # pragma: no cover
-    result = subprocess.run(
-        ['proxystore-endpoint', '--version'],
-        capture_output=True,
-    )
-    assert result.returncode == 0
-    assert proxystore.__version__ in str(result.stdout)
+def test_logging_config(tmp_path: pathlib.Path) -> None:
+    with subprocess.Popen(
+        [
+            'proxystore-relay',
+            '--port',
+            str(open_port()),
+            '--log-dir',
+            str(tmp_path),
+            '--log-level',
+            'INFO',
+        ],
+        stdout=subprocess.PIPE,
+        stderr=subprocess.STDOUT,
+        universal_newlines=True,
+    ) as server_handle:
+        # Wait for server to log that it is listening
+        assert server_handle.stdout is not None
+        for line in server_handle.stdout:  # pragma: no cover
+            if 'Serving' in line:
+                break
+
+        server_handle.terminate()
+
+    logs = [
+        f
+        for f in os.listdir(tmp_path)
+        if os.path.isfile(os.path.join(tmp_path, f))
+    ]
+    for log in logs:
+        with open(os.path.join(tmp_path, log)) as f:
+            assert 'DEBUG' not in f.read()
+    assert len(logs) >= 1
+
+
+def _serve(host: str, port: int) -> None:
+    asyncio.run(serve(host, port))
+
+
+@pytest.mark.timeout(5)
+@pytest.mark.asyncio()
+async def test_server_without_ssl() -> None:
+    host = 'localhost'
+    port = open_port()
+    address = f'ws://{host}:{port}'
+
+    process = multiprocessing.Process(target=_serve, args=(host, port))
+    process.start()
+
+    while True:
+        try:
+            client = RelayServerClient(address)
+            client.initial_backoff_seconds = 0.01
+            websocket = await client.connect()
+        except OSError:  # pragma: no cover
+            await asyncio.sleep(0.01)
+        else:
+            # Coverage doesn't detect the singular break but it does
+            # get executed to break from the loop
+            break  # pragma: no cover
+
+    pong_waiter = await websocket.ping()
+    await asyncio.wait_for(pong_waiter, 1)
+
+    process.terminate()
+
+    with pytest.raises(websockets.exceptions.ConnectionClosedOK):
+        await websocket.recv()
+
+    process.join()
+
+
+@pytest.mark.timeout(5)
+@pytest.mark.asyncio()
+async def test_start_server_cli() -> None:
+    host = 'localhost'
+    port = str(open_port())
+    address = f'ws://{host}:{port}'
+
+    server_handle = subprocess.Popen(
+        ['proxystore-relay', '--host', host, '--port', port],
+        stdout=subprocess.PIPE,
+        stderr=subprocess.STDOUT,
+        universal_newlines=True,
+    )
+
+    # Wait for server to log that it is listening
+    assert server_handle.stdout is not None
+    for line in server_handle.stdout:  # pragma: no cover
+        if 'Serving relay server' in line:
+            break
+
+    client = RelayServerClient(address)
+    websocket = await client.connect()
+    pong_waiter = await websocket.ping()
+    await asyncio.wait_for(pong_waiter, 1)
 
-    result = subprocess.run(
-        ['proxystore-endpoint', 'list'],
-        capture_output=True,
-    )
-    assert result.returncode == 0
+    server_handle.stdout.close()
+    server_handle.terminate()
 
-    result = subprocess.run(
-        ['proxystore-endpoint', 'remove', str(uuid.uuid4())],
-        capture_output=True,
-    )
-    assert result.returncode == 1
+    with pytest.raises(websockets.exceptions.ConnectionClosedOK):
+        await websocket.recv()
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/commands_test.py` & `proxystore-0.5.0/tests/endpoint/commands_test.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 from proxystore.endpoint.commands import configure_endpoint
 from proxystore.endpoint.commands import EndpointStatus
 from proxystore.endpoint.commands import get_status
 from proxystore.endpoint.commands import list_endpoints
 from proxystore.endpoint.commands import remove_endpoint
 from proxystore.endpoint.commands import start_endpoint
 from proxystore.endpoint.commands import stop_endpoint
+from proxystore.endpoint.config import ENDPOINT_CONFIG_FILE
 from proxystore.endpoint.config import EndpointConfig
 from proxystore.endpoint.config import get_configs
 from proxystore.endpoint.config import get_pid_filepath
 from proxystore.endpoint.config import read_config
 from proxystore.endpoint.config import write_config
 
 _NAME = 'default'
@@ -69,27 +70,27 @@
 
 def test_configure_endpoint_basic(tmp_path: pathlib.Path, caplog) -> None:
     caplog.set_level(logging.INFO)
 
     rv = configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     assert rv == 0
 
     endpoint_dir = os.path.join(tmp_path, _NAME)
     assert os.path.exists(endpoint_dir)
 
     cfg = read_config(endpoint_dir)
     assert cfg.name == _NAME
     assert cfg.host is None
     assert cfg.port == _PORT
-    assert cfg.server == _SERVER
+    assert cfg.relay_server == _SERVER
 
     assert any(
         [
             str(cfg.uuid) in record.message and record.levelname == 'INFO'
             for record in caplog.records
         ],
     )
@@ -99,29 +100,29 @@
     with mock.patch(
         'proxystore.endpoint.commands.home_dir',
         return_value=str(tmp_path),
     ):
         rv = configure_endpoint(
             name=_NAME,
             port=_PORT,
-            server=_SERVER,
+            relay_server=_SERVER,
         )
     assert rv == 0
 
     endpoint_dir = os.path.join(tmp_path, _NAME)
     assert os.path.exists(endpoint_dir)
 
 
 def test_configure_endpoint_invalid_name(caplog) -> None:
     caplog.set_level(logging.ERROR)
 
     rv = configure_endpoint(
         name='abc?',
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
     )
     assert rv == 1
 
     assert any(['alphanumeric' in record.message for record in caplog.records])
 
 
 def test_configure_endpoint_already_exists_error(
@@ -129,23 +130,23 @@
     caplog,
 ) -> None:
     caplog.set_level(logging.ERROR)
 
     rv = configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     assert rv == 0
 
     rv = configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     assert rv == 1
 
     assert any(
         ['already exists' in record.message for record in caplog.records],
     )
@@ -158,15 +159,15 @@
     # Raise logging level while creating endpoint so we just get logs from
     # list_endpoints()
     with caplog.at_level(logging.CRITICAL):
         for name in names:
             configure_endpoint(
                 name=name,
                 port=_PORT,
-                server=_SERVER,
+                relay_server=_SERVER,
                 proxystore_dir=str(tmp_path),
             )
 
     rv = list_endpoints(proxystore_dir=str(tmp_path))
     assert rv == 0
 
     assert len(caplog.records) == len(names) + 2
@@ -190,15 +191,15 @@
 
 def test_remove_endpoint(tmp_path: pathlib.Path, caplog) -> None:
     caplog.set_level(logging.INFO)
 
     configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     assert len(get_configs(str(tmp_path))) == 1
 
     remove_endpoint(_NAME, proxystore_dir=str(tmp_path))
     assert len(get_configs(str(tmp_path))) == 0
 
@@ -251,29 +252,29 @@
     )
 
 
 def test_start_endpoint(tmp_path: pathlib.Path) -> None:
     configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     with mock.patch('proxystore.endpoint.commands.serve', autospec=True):
         rv = start_endpoint(_NAME, proxystore_dir=str(tmp_path))
     assert rv == 0
 
 
 def test_start_endpoint_detached(tmp_path: pathlib.Path, caplog) -> None:
     caplog.set_level(logging.INFO)
 
     configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
     with mock.patch(
         'proxystore.endpoint.commands.serve',
         autospec=True,
     ), mock.patch('daemon.DaemonContext', autospec=True):
         rv = start_endpoint(_NAME, detach=True, proxystore_dir=str(tmp_path))
@@ -331,15 +332,15 @@
 
 
 def test_start_endpoint_bad_config(tmp_path: pathlib.Path, caplog) -> None:
     caplog.set_level(logging.ERROR)
 
     endpoint_dir = os.path.join(tmp_path, _NAME)
     os.makedirs(endpoint_dir)
-    with open(os.path.join(endpoint_dir, 'endpoint.json'), 'w') as f:
+    with open(os.path.join(endpoint_dir, ENDPOINT_CONFIG_FILE), 'w') as f:
         f.write('not valid json')
 
     rv = start_endpoint(_NAME, proxystore_dir=str(tmp_path))
     assert rv == 1
 
     assert any(
         ['Unable to parse' in record.message for record in caplog.records],
@@ -403,15 +404,15 @@
 
 @pytest.mark.timeout(2)
 def test_stop_endpoint(tmp_path: pathlib.Path) -> None:
     endpoint_dir = os.path.join(tmp_path, _NAME)
     configure_endpoint(
         name=_NAME,
         port=_PORT,
-        server=_SERVER,
+        relay_server=_SERVER,
         proxystore_dir=str(tmp_path),
     )
 
     # Create a fake process to kill
     p = Process(target=time.sleep, args=(1000,))
     p.start()
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/config_test.py` & `proxystore-0.5.0/tests/endpoint/config_test.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 import os
 import pathlib
 import uuid
 from typing import Any
 
 import pytest
 
+from proxystore.endpoint.config import ENDPOINT_CONFIG_FILE
 from proxystore.endpoint.config import EndpointConfig
 from proxystore.endpoint.config import get_configs
 from proxystore.endpoint.config import get_log_filepath
 from proxystore.endpoint.config import get_pid_filepath
 from proxystore.endpoint.config import read_config
 from proxystore.endpoint.config import validate_name
 from proxystore.endpoint.config import write_config
@@ -22,15 +23,15 @@
     assert not os.path.exists(tmp_dir)
 
     cfg = EndpointConfig(
         name='name',
         uuid=uuid.uuid4(),
         host='host',
         port=1234,
-        server=None,
+        relay_server=None,
     )
     write_config(cfg, tmp_dir)
     assert os.path.exists(tmp_dir)
 
     # Overwriting is okay
     write_config(cfg, tmp_dir)
 
@@ -68,30 +69,30 @@
         )
 
     # Make invalid directory to make sure get_configs skips it
     os.makedirs(os.path.join(tmp_dir, 'ep4'))
     # Make a bad config to make sure its skipped
     ep5 = os.path.join(tmp_dir, 'ep5')
     os.makedirs(ep5)
-    with open(os.path.join(ep5, 'endpoint.json'), 'w') as f:
+    with open(os.path.join(ep5, ENDPOINT_CONFIG_FILE), 'w') as f:
         f.write('this is not json')
     # Make another bad config to make sure its skipped
     ep6 = os.path.join(tmp_dir, 'ep6')
     os.makedirs(ep6)
-    with open(os.path.join(ep6, 'endpoint.json'), 'w') as f:
+    with open(os.path.join(ep6, ENDPOINT_CONFIG_FILE), 'w') as f:
         f.write('{"name": "this is missing keys"}')
 
     configs = get_configs(tmp_dir)
     assert len(configs) == len(names)
     found_names = {cfg.name for cfg in configs}
     assert set(names) == found_names
 
 
 @pytest.mark.parametrize(
-    'name,valid',
+    ('name', 'valid'),
     (
         ('abc', True),
         ('ABC', True),
         ('aBc_', True),
         ('aBc-', True),
         ('aBc_-123', True),
         ('', False),
@@ -102,41 +103,40 @@
     ),
 )
 def test_validate_name(name: str, valid: bool) -> None:
     assert validate_name(name) == valid
 
 
 @pytest.mark.parametrize(
-    'bad_cfg,valid',
+    ('bad_cfg', 'valid'),
     (
         ({}, True),
         ({'name': 'bad name'}, False),
         ({'uuid': 'abc-abc-abc'}, False),
         ({'port': 0}, False),
         ({'port': 1000000}, False),
-        ({'server': 'ws://'}, True),
-        ({'server': 'wss://'}, True),
-        ({'server': ''}, False),
-        ({'server': 'https://'}, False),
-        ({'max_memory': -1}, False),
+        ({'relay_server': 'ws://'}, True),
+        ({'relay_server': 'wss://'}, True),
+        ({'relay_server': ''}, False),
+        ({'relay_server': 'https://'}, False),
         ({'peer_channels': 1}, True),
         ({'peer_channels': 0}, False),
         ({'max_object_size': 0}, False),
         ({'max_object_size': 1}, True),
         ({'max_object_size': -1}, False),
     ),
 )
 def test_validate_config(bad_cfg: Any, valid: bool) -> None:
-    options = dict(
-        name='name',
-        uuid=uuid.uuid4(),
-        host='host',
-        port=1234,
-        server='wss://myserver.com',
-    )
+    options = {
+        'name': 'name',
+        'uuid': uuid.uuid4(),
+        'host': 'host',
+        'port': 1234,
+        'relay_server': 'wss://myserver.com',
+    }
     options.update(bad_cfg)
 
     if valid:
         EndpointConfig(**options)  # type: ignore
     else:
         with pytest.raises(ValueError):
             EndpointConfig(**options)  # type: ignore
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/endpoint_peering_test.py` & `proxystore-0.5.0/tests/endpoint/endpoint_peering_test.py`

 * *Files 9% similar despite different names*

```diff
@@ -13,51 +13,51 @@
 from proxystore.endpoint.messages import EndpointRequest
 from proxystore.serialize import serialize
 from testing.compat import randbytes
 
 
 @pytest_asyncio.fixture(scope='module')
 async def endpoints(
-    signaling_server,
+    relay_server,
 ) -> AsyncGenerator[tuple[Endpoint, Endpoint], None]:
     async with Endpoint(
         name='test-endpoint-1',
         uuid=uuid.uuid4(),
-        signaling_server=signaling_server.address,
+        relay_server=relay_server.address,
     ) as endpoint1, Endpoint(
         name='test-endpoint-2',
         uuid=uuid.uuid4(),
-        signaling_server=signaling_server.address,
+        relay_server=relay_server.address,
     ) as endpoint2:
         yield (endpoint1, endpoint2)
 
 
-@pytest.mark.asyncio
-async def test_init(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_init(relay_server) -> None:
     endpoint = await Endpoint(
         name='test-init-endpoint',
         uuid=uuid.uuid4(),
-        signaling_server=signaling_server.address,
+        relay_server=relay_server.address,
     )
     # Calling async_init multiple times should be no-op
     await endpoint.async_init()
     await endpoint.async_init()
     await endpoint.close()
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_set(endpoints: tuple[Endpoint, Endpoint]) -> None:
     endpoint1, endpoint2 = endpoints
     key = str(uuid.uuid4())
     data = randbytes(100)
     await endpoint1.set(key, data, endpoint=endpoint2.uuid)
     assert (await endpoint2.get(key)) == data
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_get(endpoints: tuple[Endpoint, Endpoint]) -> None:
     endpoint1, endpoint2 = endpoints
     data1 = randbytes(100)
     key = str(uuid.uuid4())
     await endpoint1.set(key, data1, endpoint=endpoint2.uuid)
     assert (await endpoint1.get(key, endpoint=endpoint2.uuid)) == data1
     assert (await endpoint2.get(key)) == data1
@@ -66,74 +66,73 @@
     await endpoint2.set(key, data2)
     assert (await endpoint1.get(key)) is None
     assert (await endpoint2.get(key)) == data2
 
     assert (await endpoint2.get('missingkey', endpoint=endpoint1.uuid)) is None
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_evict(endpoints: tuple[Endpoint, Endpoint]) -> None:
     endpoint1, endpoint2 = endpoints
     data = randbytes(100)
     key = str(uuid.uuid4())
     await endpoint1.set(key, data)
     # Should not do anything because key is not on endpoint2
     await endpoint2.evict(key, endpoint=endpoint2.uuid)
     assert (await endpoint1.get(key)) == data
     # Evict on remote endpoint
     await endpoint2.evict(key, endpoint=endpoint1.uuid)
     assert (await endpoint1.get(key)) is None
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_exists(endpoints: tuple[Endpoint, Endpoint]) -> None:
     endpoint1, endpoint2 = endpoints
     data = randbytes(100)
     key = str(uuid.uuid4())
     assert not (await endpoint2.exists(key))
     await endpoint1.set(key, data, endpoint=endpoint2.uuid)
     assert await endpoint2.exists(key)
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_remote_error_propogation(
     endpoints: tuple[Endpoint, Endpoint],
 ) -> None:
     endpoint1, endpoint2 = endpoints
     key = str(uuid.uuid4())
     with pytest.raises(AssertionError):
-        ep = endpoint2.uuid
-        await endpoint1.set(key, None, endpoint=ep)  # type: ignore
+        await endpoint1.set(key, None, endpoint=endpoint2.uuid)  # type: ignore
 
 
-@pytest.mark.asyncio
-async def test_peering_not_available(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_peering_not_available(relay_server) -> None:
     endpoint = Endpoint(
         name='test',
         uuid=uuid.uuid4(),
-        signaling_server=signaling_server.address,
+        relay_server=relay_server.address,
     )
     # __await__ has not been called on endpoint so connection to server
     # has not been enabled
     with pytest.raises(PeeringNotAvailableError, match='await'):
         await endpoint.get('key', endpoint=uuid.uuid4())
 
 
-@pytest.mark.asyncio
-async def test_unknown_peer(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_unknown_peer(relay_server) -> None:
     async with Endpoint(
         name='test',
         uuid=uuid.uuid4(),
-        signaling_server=signaling_server.address,
+        relay_server=relay_server.address,
     ) as endpoint:
         with pytest.raises(PeerRequestError, match='unknown'):
             await endpoint.get('key', endpoint=uuid.uuid4())
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_unsupported_peer_message(
     endpoints: tuple[Endpoint, Endpoint],
     caplog,
 ) -> None:
     caplog.set_level(logging.ERROR)
     endpoint1, endpoint2 = endpoints
 
@@ -150,15 +149,15 @@
             'unable to decode message from peer' in record.message
             and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_unexpected_response(
     endpoints: tuple[Endpoint, Endpoint],
     caplog,
 ) -> None:
     caplog.set_level(logging.ERROR)
     endpoint1, endpoint2 = endpoints
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/endpoint_solo_test.py` & `proxystore-0.5.0/tests/endpoint/endpoint_solo_test.py`

 * *Files 9% similar despite different names*

```diff
@@ -8,71 +8,71 @@
 from proxystore.endpoint.exceptions import ObjectSizeExceededError
 from testing.compat import randbytes
 
 _NAME = 'test-endpoint'
 _UUID = uuid.uuid4()
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_init() -> None:
     endpoint = Endpoint(name=_NAME, uuid=_UUID)
     # Should not do anything
     await endpoint.close()
 
     # Try again with awaitable initialization
     endpoint = await Endpoint(name=_NAME, uuid=_UUID)
     await endpoint.close()
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_set() -> None:
     async with Endpoint(name=_NAME, uuid=_UUID) as endpoint:
         data = randbytes(100)
         await endpoint.set('key', data)
         assert (await endpoint.get('key')) == data
 
         # Check key gets overwritten
         data = randbytes(100)
         await endpoint.set('key', data)
         assert (await endpoint.get('key')) == data
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_set_exceeds_size() -> None:
     async with Endpoint(
         name=_NAME,
         uuid=_UUID,
         max_object_size=10,
     ) as endpoint:
         data = randbytes(100)
         with pytest.raises(ObjectSizeExceededError):
             await endpoint.set('key', data)
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_get() -> None:
     async with Endpoint(name=_NAME, uuid=_UUID) as endpoint:
         data = randbytes(100)
         await endpoint.set('key', data)
         assert (await endpoint.get('key')) == data
         assert (await endpoint.get('key', endpoint=uuid.uuid4())) == data
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_evict() -> None:
     async with Endpoint(name=_NAME, uuid=_UUID) as endpoint:
         data = randbytes(100)
         await endpoint.set('key', data)
         assert (await endpoint.get('key')) == data
         await endpoint.evict('key')
         assert (await endpoint.get('key')) is None
         # Should not raise error if key does not exists already
         await endpoint.evict('key')
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_exists() -> None:
     async with Endpoint(name=_NAME, uuid=_UUID) as endpoint:
         data = randbytes(100)
         assert not (await endpoint.exists('key'))
         await endpoint.set('key', data)
         assert await endpoint.exists('key')
```

### Comparing `proxystore-0.4.1a1/tests/endpoint/serve_test.py` & `proxystore-0.5.0/tests/endpoint/serve_test.py`

 * *Files 2% similar despite different names*

```diff
@@ -27,37 +27,37 @@
 if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
     from unittest.mock import AsyncMock
 else:  # pragma: <3.8 cover
     from asynctest import CoroutineMock as AsyncMock
 
 
 @pytest_asyncio.fixture
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def quart_app() -> AsyncGenerator[quart.typing.TestAppProtocol, None]:
     async with Endpoint(
         name='my-endpoint',
         uuid=uuid.uuid4(),
     ) as endpoint:
         app = create_app(endpoint)
         async with app.test_app() as test_app:
             test_app.endpoint = endpoint  # type: ignore
             yield test_app
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_running(quart_app) -> None:
     client = quart_app.test_client()
     response = await client.get('/')
     assert response.status_code == 200
 
     response = await client.get('/endpoint')
     assert len((await response.get_json())['uuid']) > 0
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_set_request(quart_app) -> None:
     client = quart_app.test_client()
     data = randbytes(100)
     set_response = await client.post(
         '/set',
         headers={'Content-Type': 'application/octet-stream'},
         query_string={'key': 'my-key'},
@@ -72,15 +72,15 @@
         headers={'Content-Type': 'application/octet-stream'},
         query_string={'key': 'my-key'},
         data=data,
     )
     assert set_response.status_code == 200
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_get_request(quart_app) -> None:
     client = quart_app.test_client()
     data = randbytes(100)
     set_response = await client.post(
         '/set',
         headers={'Content-Type': 'application/octet-stream'},
         query_string={'key': 'my-key'},
@@ -95,15 +95,15 @@
     get_response = await client.get(
         '/get',
         query_string={'key': 'missing-key'},
     )
     assert get_response.status_code == 400
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_chunked_data(quart_app) -> None:
     client = quart_app.test_client()
     # Data needs to be larger than MAX_CHUNK_LENGTH
     data = randbytes((2 * MAX_CHUNK_LENGTH) + 1)
 
     async with client.request(
         '/set',
@@ -120,30 +120,30 @@
     assert set_response.status_code == 200
 
     get_response = await client.get('/get', query_string={'key': 'my-key'})
     assert get_response.status_code == 200
     assert (await get_response.get_data()) == data
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_empty_chunked_data(quart_app) -> None:
     client = quart_app.test_client()
 
     async with client.request(
         '/set',
         method='POST',
         headers={'Content-Type': 'application/octet-stream'},
         query_string={'key': 'my-key'},
     ) as connection:
         await connection.send_complete()
     set_response = await connection.as_response()
     assert set_response.status_code == 400
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_exists_request(quart_app) -> None:
     client = quart_app.test_client()
     exists_response = await client.get(
         'exists',
         query_string={'key': 'my-key'},
     )
     assert exists_response.status_code == 200
@@ -162,15 +162,15 @@
         'exists',
         query_string={'key': 'my-key'},
     )
     assert exists_response.status_code == 200
     assert (await exists_response.get_json())['exists']
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_evict_request(quart_app) -> None:
     client = quart_app.test_client()
     evict_response = await client.post('evict', query_string={'key': 'my-key'})
     # No error if key does not exist
     assert evict_response.status_code == 200
 
     data = randbytes(100)
@@ -196,15 +196,15 @@
         'exists',
         query_string={'key': 'my-key'},
     )
     assert exists_response.status_code == 200
     assert not (await exists_response.get_json())['exists']
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_payload_too_big() -> None:
     async with Endpoint(
         name='my-endpoint',
         uuid=uuid.uuid4(),
     ) as endpoint:
         app = create_app(endpoint, max_content_length=10)
         async with app.test_app() as quart_app:
@@ -215,15 +215,15 @@
                 headers={'Content-Type': 'application/octet-stream'},
                 query_string={'key': 'my-key'},
                 data=data,
             )
             assert set_response.status_code == 413
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_bad_endpoint_uuid(quart_app) -> None:
     client = quart_app.test_client()
     bad_uuid = 'not a uuid'
 
     evict_response = await client.post(
         'evict',
         query_string={'key': 'my-key', 'endpoint': bad_uuid},
@@ -248,15 +248,15 @@
         headers={'Content-Type': 'application/octet-stream'},
         query_string={'key': 'my-key', 'endpoint': bad_uuid},
         data=data,
     )
     assert set_response.status_code == 400
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_unknown_endpoint_uuid(quart_app) -> None:
     client = quart_app.test_client()
     unknown_uuid = uuid.uuid4()
 
     with mock.patch(
         'proxystore.endpoint.endpoint.Endpoint._is_peer_request',
         return_value=True,
@@ -291,15 +291,15 @@
             headers={'Content-Type': 'application/octet-stream'},
             query_string={'key': 'my-key', 'endpoint': unknown_uuid},
             data=data,
         )
         assert set_response.status_code == 400
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_missing_key(quart_app) -> None:
     client = quart_app.test_client()
 
     evict_response = await client.post('evict')
     assert evict_response.status_code == 400
 
     exists_response = await client.get('exists')
@@ -320,14 +320,15 @@
 @pytest.mark.timeout(5)
 def test_serve(use_uvloop: bool) -> None:
     config = EndpointConfig(
         name='my-endpoint',
         uuid=uuid.uuid4(),
         host='localhost',
         port=open_port(),
+        database_path=':memory:',
     )
 
     process = multiprocessing.Process(
         target=serve,
         args=(config,),
         kwargs={'use_uvloop': use_uvloop},
     )
@@ -368,17 +369,17 @@
         loop = asyncio.new_event_loop()
         asyncio.set_event_loop(loop)
         config = EndpointConfig(
             name='name',
             uuid=uuid.uuid4(),
             host='0.0.0.0',
             port=open_port(),
-            server=None,
+            relay_server=None,
         )
-        with mock.patch('hypercorn.asyncio.serve', AsyncMock()):
+        with mock.patch('uvicorn.Server.serve', AsyncMock()):
             serve(
                 config,
                 log_level='INFO',
                 log_file=log_file,
                 use_uvloop=use_uvloop,
             )
         loop.close()
```

### Comparing `proxystore-0.4.1a1/tests/factory_test.py` & `proxystore-0.5.0/tests/factory_test.py`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/tests/globus_test.py` & `proxystore-0.5.0/tests/globus_test.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,27 +1,28 @@
 """Globus Auth Unit Tests."""
 from __future__ import annotations
 
-import contextlib
 import json
 import os
 import pathlib
 from unittest import mock
 
+import click
+import click.testing
 import globus_sdk
 import pytest
 
 from proxystore.globus import _get_proxystore_scopes
 from proxystore.globus import _TOKENS_FILE
 from proxystore.globus import authenticate
+from proxystore.globus import cli
 from proxystore.globus import get_authorizer
 from proxystore.globus import get_proxystore_authorizer
 from proxystore.globus import GlobusAuthFileError
 from proxystore.globus import load_tokens_from_file
-from proxystore.globus import main
 from proxystore.globus import proxystore_authenticate
 from proxystore.globus import save_tokens_to_file
 
 
 def test_save_load_tokens(tmp_path: pathlib.Path) -> None:
     os.makedirs(tmp_path, exist_ok=True)
     tmp_file = os.path.join(tmp_path, 'globus.json')
@@ -33,19 +34,17 @@
     save_tokens_to_file(tmp_file, tokens)
     assert load_tokens_from_file(tmp_file) == data
 
 
 def test_authenticate(capsys) -> None:
     # This test is heavily mocked so most just checks for simple errors
     with mock.patch('globus_sdk.NativeAppAuthClient'), mock.patch(
-        'builtins.input',
+        'click.prompt',
         return_value='123456789',
-    ), contextlib.redirect_stdout(
-        None,
-    ):
+    ), mock.patch('click.echo'), mock.patch('click.secho'):
         authenticate('1234', 'https://redirect')
 
 
 def test_get_authorizer(tmp_path: pathlib.Path) -> None:
     tokens = {
         'transfer.api.globus.org': {
             'refresh_token': 1234,
@@ -57,25 +56,25 @@
     filepath = os.path.join(tmp_path, 'tokens.json')
     with open(filepath, 'w') as f:
         json.dump(tokens, f)
 
     with mock.patch('globus_sdk.NativeAppAuthClient'), mock.patch(
         'globus_sdk.RefreshTokenAuthorizer',
     ):
-        get_authorizer('client id', filepath, 'redirect uri')
+        get_authorizer('client id', filepath)
 
 
 def test_get_authorizer_missing_file(tmp_path: pathlib.Path) -> None:
     filepath = os.path.join(tmp_path, 'missing_file')
     with pytest.raises(GlobusAuthFileError):
-        get_authorizer('client id', filepath, 'redirect uri')
+        get_authorizer('client id', filepath)
 
 
 @pytest.mark.parametrize(
-    'collections,additional_scopes,expected',
+    ('collections', 'additional_scopes', 'expected'),
     (
         (
             None,
             None,
             {'openid', 'urn:globus:auth:scope:transfer.api.globus.org:all'},
         ),
         (
@@ -117,35 +116,49 @@
 def test_proxystore_authenticate(tmp_path: pathlib.Path) -> None:
     data = {'tokens': {'token': '123456789'}}
     with mock.patch('globus_sdk.OAuthTokenResponse'):
         tokens = globus_sdk.OAuthTokenResponse()
         tokens.by_resource_server = data  # type: ignore
 
     with mock.patch('proxystore.globus.authenticate', return_value=tokens):
-        proxystore_authenticate(str(tmp_path))
+        path = proxystore_authenticate(str(tmp_path))
+        assert isinstance(path, str)
+        assert len(path) > 0
 
     assert load_tokens_from_file(os.path.join(tmp_path, _TOKENS_FILE)) == data
 
     with mock.patch('proxystore.globus.get_authorizer'):
         get_proxystore_authorizer(str(tmp_path))
 
 
-def test_main(tmp_path: pathlib.Path) -> None:
-    with mock.patch('proxystore.globus.proxystore_authenticate'), mock.patch(
+def test_cli(tmp_path: pathlib.Path) -> None:
+    with mock.patch(
+        'proxystore.globus.proxystore_authenticate',
+        return_value='/path/to/file',
+    ), mock.patch(
         'proxystore.globus.get_proxystore_authorizer',
         side_effect=[GlobusAuthFileError(), None, None],
-    ), contextlib.redirect_stdout(None):
+    ):
+        runner = click.testing.CliRunner()
         # First will raise auth file missing error and trigger auth flow
-        assert main([]) == 0
-        # Second will find auth file and already exits and exists
-        assert main([]) != 0
+        result = runner.invoke(cli)
+        assert result.exit_code == 0
+        # Second will find auth file and already exists and exits
+        result = runner.invoke(cli)
+        assert result.exit_code == 0
 
 
-def test_main_delete(tmp_path: pathlib.Path) -> None:
-    with mock.patch('proxystore.globus.home_dir', return_value=str(tmp_path)):
-        assert main(['--delete']) != 0
+def test_cli_delete(tmp_path: pathlib.Path) -> None:
+    with mock.patch(
+        'proxystore.globus.home_dir',
+        return_value=str(tmp_path),
+    ):
+        runner = click.testing.CliRunner()
+        result = runner.invoke(cli, ['--delete'])
+        assert result.exit_code != 0
 
         token_file = tmp_path / _TOKENS_FILE
         token_file.touch()
 
-        assert main(['--delete']) == 0
+        result = runner.invoke(cli, ['--delete'])
+        assert result.exit_code == 0
         assert not token_file.exists()
```

### Comparing `proxystore-0.4.1a1/tests/integration/endpoints_test.py` & `proxystore-0.5.0/tests/integration/endpoints_test.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,61 +1,66 @@
 from __future__ import annotations
 
 import asyncio
 import os
 import pathlib
+import tempfile
 import uuid
 from multiprocessing import Process
 from multiprocessing import Queue
 from typing import Any
 from typing import Generator
 from unittest import mock
 
 import pytest
 
+from proxystore.connectors.endpoint import EndpointConnector
 from proxystore.endpoint.config import EndpointConfig
 from proxystore.endpoint.config import write_config
-from proxystore.p2p.client import connect
-from proxystore.p2p.server import serve
+from proxystore.p2p.relay import serve
+from proxystore.p2p.relay_client import RelayServerClient
 from proxystore.proxy import Proxy
 from proxystore.store import get_store
-from proxystore.store.endpoint import EndpointStore
+from proxystore.store.base import Store
 from testing.endpoint import serve_endpoint_silent
 from testing.endpoint import wait_for_endpoint
 from testing.utils import open_port
 
 
 async def wait_for_server(host: str, port: int) -> None:
     """Wait for websocket server to be available for connections."""
     while True:
         try:
-            _, _, connection = await connect(f'ws://{host}:{port}')
+            client = RelayServerClient(f'ws://{host}:{port}')
+            await client.connect()
         except OSError:  # pragma: no cover
             await asyncio.sleep(0.01)
         else:
-            await connection.close()
+            await client.close()
             break
 
 
-def serve_signaling_server(host: str, port: int) -> None:
-    """Run signaling server."""
+def serve_relay_server(host: str, port: int) -> None:
+    """Run relay server."""
     asyncio.run(serve(host, port))
 
 
-@pytest.fixture
+@pytest.fixture(scope='module')
 def endpoints(
-    signaling_server,
-    tmp_path: pathlib.Path,
+    relay_server,
 ) -> Generator[tuple[list[uuid.UUID], list[str]], None, None]:
-    """Launch the signaling server and two endpoints."""
+    """Launch the relay server and two endpoints."""
+    tmp_dir = tempfile.TemporaryDirectory()
+    tmp_path = pathlib.Path(tmp_dir.name)
+
     ss_host = 'localhost'
     ss_port = open_port()
 
     ss = Process(
-        target=serve_signaling_server,
+        target=serve_relay_server,
         kwargs={'host': ss_host, 'port': ss_port},
     )
     ss.start()
 
     asyncio.run(wait_for_server(ss_host, ss_port))
 
     handles = []
@@ -63,15 +68,15 @@
     dirs = []
     for port in (open_port(), open_port()):
         cfg = EndpointConfig(
             name=f'test-endpoint-{port}',
             uuid=uuid.uuid4(),
             host='localhost',
             port=port,
-            server=f'ws://{ss_host}:{ss_port}',
+            relay_server=f'ws://{ss_host}:{ss_port}',
         )
         assert cfg.host is not None
 
         # We want a unique proxystore_dir for each endpoint to simulate
         # different systems
         proxystore_dir = os.path.join(tmp_path, str(port))
         endpoint_dir = os.path.join(proxystore_dir, cfg.name)
@@ -82,71 +87,79 @@
         handle = Process(target=serve_endpoint_silent, args=[cfg])
         handle.start()
         handles.append(handle)
 
         wait_for_endpoint(cfg.host, cfg.port)
 
     if not ss.is_alive():  # pragma: no cover
-        raise RuntimeError('Signaling server died.')
+        raise RuntimeError('Relay server died.')
 
     yield uuids, dirs
 
     for handle in handles:
         handle.terminate()
         handle.join()
 
     ss.terminate()
     ss.join()
 
+    tmp_dir.cleanup()
+
 
-@pytest.mark.integration
+@pytest.mark.integration()
 def test_endpoint_transfer(endpoints) -> None:
     """Test transferring data between two endpoints."""
     endpoints, proxystore_dirs = endpoints
 
-    store1 = EndpointStore(
+    store1 = Store(
         'store1',
-        endpoints=endpoints,
-        proxystore_dir=proxystore_dirs[0],
+        connector=EndpointConnector(
+            endpoints=endpoints,
+            proxystore_dir=proxystore_dirs[0],
+        ),
     )
-    store2 = EndpointStore(
+    store2 = Store(
         'store2',
-        endpoints=endpoints,
-        proxystore_dir=proxystore_dirs[1],
+        connector=EndpointConnector(
+            endpoints=endpoints,
+            proxystore_dir=proxystore_dirs[1],
+        ),
     )
 
     obj = [1, 2, 3]
-    key = store1.set(obj)
+    key = store1.put(obj)
     assert obj == store2.get(key)
     store2.evict(key)
     assert not store1.exists(key)
 
 
 def _produce_local(
     queue: Queue[Any],
     endpoints: list[uuid.UUID],
     home_dir: str,
 ) -> None:
-    store = EndpointStore(
+    store = Store(
         'store',
-        endpoints=endpoints,
-        proxystore_dir=home_dir,
+        connector=EndpointConnector(
+            endpoints=endpoints,
+            proxystore_dir=home_dir,
+        ),
     )
     obj = [1, 2, 3]
     proxy: Proxy[Any] = store.proxy(obj)
     queue.put(proxy)
 
 
 def _consume_local(queue: Queue[Any]) -> None:
     # access proxy to force resolve which will reconstruct store
     obj = queue.get()
     assert obj == [1, 2, 3]
 
 
-@pytest.mark.integration
+@pytest.mark.integration()
 def test_endpoint_proxy_transfer(endpoints) -> None:
     """Test transferring data via proxy between processes sharing endpoint."""
     endpoints, proxystore_dirs = endpoints
 
     queue: Queue[Any] = Queue()
 
     producer = Process(
@@ -171,40 +184,40 @@
 def _produce_remote(
     queue: Queue[Any],
     endpoints: list[uuid.UUID],
     home_dir: str,
 ) -> None:
     # Mock home_dir to simulate different systems
     with mock.patch(
-        'proxystore.store.endpoint.home_dir',
+        'proxystore.connectors.endpoint.home_dir',
         return_value=home_dir,
     ):
-        store = EndpointStore('store', endpoints=endpoints)
+        store = Store('store', EndpointConnector(endpoints))
         # Send port to other process to compare
-        proxy: Proxy[Any] = store.proxy(store.endpoint_port)
+        proxy: Proxy[Any] = store.proxy(store.connector.endpoint_port)
         queue.put(proxy)
 
 
 def _consume_remote(queue: Queue[Any], home_dir: str) -> None:
     # Mock home_dir to simulate different systems
     with mock.patch(
-        'proxystore.store.endpoint.home_dir',
+        'proxystore.connectors.endpoint.home_dir',
         return_value=home_dir,
     ):
         port = queue.get()
         # Just to force the proxy to resolve
         assert isinstance(port, int)
 
         # Make sure consumer is using different port
         store = get_store('store')
-        assert isinstance(store, EndpointStore)
-        assert store.endpoint_port != port
+        assert isinstance(store, Store)
+        assert store.connector.endpoint_port != port
 
 
-@pytest.mark.integration
+@pytest.mark.integration()
 def test_proxy_detects_endpoint(endpoints) -> None:
     """Test transferring data via proxy between two process and endpoints."""
     endpoints, proxystore_dirs = endpoints
 
     queue: Queue[Any] = Queue()
 
     producer = Process(
```

### Comparing `proxystore-0.4.1a1/tests/p2p/chunks_test.py` & `proxystore-0.5.0/tests/p2p/chunks_test.py`

 * *Files 12% similar despite different names*

```diff
@@ -38,15 +38,15 @@
         Chunk(0, 2, 1, '')
 
 
 @pytest.mark.parametrize('dtype', (bytes, str))
 def test_chunk_and_reconstruct(dtype: bytes | str) -> None:
     data: bytes | str = randbytes(1000) if dtype is bytes else 'x' * 1000
 
-    chunks = [c for c in chunkify(data, 100, 1)]
+    chunks = list(chunkify(data, 100, 1))
     new_data = reconstruct(chunks)
 
     assert data == new_data
 
 
 def test_reconstruct_validation() -> None:
     with pytest.raises(ValueError, match='empty'):
```

### Comparing `proxystore-0.4.1a1/tests/p2p/counter_test.py` & `proxystore-0.5.0/tests/p2p/counter_test.py`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/tests/p2p/manager_test.py` & `proxystore-0.5.0/tests/p2p/manager_test.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,138 +1,126 @@
 from __future__ import annotations
 
 import asyncio
 import logging
 import sys
 import uuid
-from unittest import mock
 
 import pytest
 
 from proxystore.p2p import messages
 from proxystore.p2p.exceptions import PeerConnectionError
-from proxystore.p2p.exceptions import PeerRegistrationError
 from proxystore.p2p.manager import PeerManager
 from testing.mocking import async_mock_once
 
 if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
-    from unittest.mock import AsyncMock
+    pass
 else:  # pragma: <3.8 cover
-    from asynctest import CoroutineMock as AsyncMock
+    pass
 
 
-@pytest.mark.asyncio
-async def test_awaitable(signaling_server) -> None:
-    manager = await PeerManager(uuid.uuid4(), signaling_server.address)
+@pytest.mark.asyncio()
+async def test_awaitable(relay_server) -> None:
+    manager = await PeerManager(uuid.uuid4(), relay_server.address)
     # Calling async_init again should do nothing
     await manager.async_init()
     await manager.close()
 
 
-@pytest.mark.asyncio
-async def test_not_awaited(signaling_server) -> None:
-    manager = PeerManager(uuid.uuid4(), signaling_server.address)
+@pytest.mark.asyncio()
+async def test_not_awaited(relay_server) -> None:
+    manager = PeerManager(uuid.uuid4(), relay_server.address)
     with pytest.raises(RuntimeError, match='await'):
         await manager.get_connection(uuid.uuid4())
     await manager.close()
 
 
-@pytest.mark.asyncio
-async def test_uuid_name_properties(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_uuid_name_properties(relay_server) -> None:
     uuid_ = uuid.uuid4()
     name = 'pm'
     async with PeerManager(
         uuid_,
-        signaling_server.address,
+        relay_server.address,
         name=name,
     ) as manager:
         assert manager.uuid == uuid_
         assert manager.name == name
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 async def test_address_validation() -> None:
     PeerManager(uuid.uuid4(), 'ws://example.com')
     PeerManager(uuid.uuid4(), 'wss://example.com')
     with pytest.raises(ValueError, match='wss://'):
         PeerManager(uuid.uuid4(), 'http://example.com')
 
 
-@pytest.mark.asyncio
-async def test_uuid_mismatch(signaling_server) -> None:
-    amock = AsyncMock(return_value=('wrong-uuid', None, None))
-    with mock.patch('proxystore.p2p.manager.connect', side_effect=amock):
-        with pytest.raises(PeerRegistrationError, match='non-matching UUID'):
-            await PeerManager(uuid.uuid4(), signaling_server.address)
-
-
-@pytest.mark.asyncio
-async def test_p2p_connection(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_p2p_connection(relay_server) -> None:
     async with PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager1, PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager2:
         connection1 = await manager1.get_connection(manager2.uuid)
         assert connection1 == await manager1.get_connection(manager2.uuid)
         await connection1.ready()
         assert connection1.state == 'connected'
 
         connection2 = await manager2.get_connection(manager1.uuid)
         await connection2.ready()
         assert connection2.state == 'connected'
 
 
-@pytest.mark.asyncio
-async def test_p2p_connection_error_unknown_peer(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_p2p_connection_error_unknown_peer(relay_server) -> None:
     async with PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager1:
         with pytest.raises(PeerConnectionError, match='unknown'):
             await manager1.send(uuid.uuid4(), 'hello', timeout=0.2)
 
 
-@pytest.mark.asyncio
+@pytest.mark.asyncio()
 @pytest.mark.skipif(
     sys.version_info < (3, 8),
     reason='aiortc in py37 raises InvalidStateError for unknown reason',
 )
 async def test_p2p_connection_error_from_server(
-    signaling_server,
+    relay_server,
 ) -> None:  # pragma: >=3.8 cover
     # Record current tasks so we know which not to clean up
     task_names = {task.get_name() for task in asyncio.all_tasks()}
 
     async with PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager1, PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager2:
         # Mock manager 1 to receive error peer connection from
-        # signaling server
-        assert manager1._websocket_or_none is not None
+        # relay server
+        assert manager1._relay_server_client_or_none is not None
         mock_recv = async_mock_once(
-            manager1._websocket_or_none.recv,
-            messages.encode(
-                messages.PeerConnection(
-                    source_uuid=manager2.uuid,
-                    source_name=manager2.name,
-                    peer_uuid=manager1.uuid,
-                    description_type='offer',
-                    description='',
-                    error='test error',
-                ),
+            manager1._relay_server_client_or_none.recv,
+            messages.PeerConnection(
+                source_uuid=manager2.uuid,
+                source_name=manager2.name,
+                peer_uuid=manager1.uuid,
+                description_type='offer',
+                description='',
+                error='test error',
             ),
         )
-        manager1._websocket_or_none.recv = mock_recv  # type: ignore
+        manager1._relay_server_client_or_none.recv = mock_recv  # type: ignore
 
         connection1 = await manager1.get_connection(manager2.uuid)
 
         while not mock_recv.await_count > 1:
             await asyncio.sleep(0.01)
 
         with pytest.raises(PeerConnectionError, match='test error'):
@@ -144,113 +132,154 @@
             task.cancel()
             try:
                 await task
             except asyncio.CancelledError:
                 pass
 
 
-@pytest.mark.asyncio
-async def test_p2p_messaging(signaling_server) -> None:
+@pytest.mark.asyncio()
+async def test_p2p_messaging(relay_server) -> None:
     async with PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
     ) as manager1, PeerManager(
         uuid.uuid4(),
-        signaling_server.address,
+        relay_server.address,
         verify_certificate=False,
     ) as manager2:
         await manager1.send(manager2.uuid, 'hello hello')
         source_uuid, message = await manager2.recv()
         assert source_uuid == manager1.uuid
         assert message == 'hello hello'
 
 
-@pytest.mark.asyncio
-async def test_expected_server_disconnect(signaling_server) -> None:
-    manager = await PeerManager(uuid.uuid4(), signaling_server.address)
+@pytest.mark.asyncio()
+async def test_expected_server_disconnect(relay_server) -> None:
+    manager = await PeerManager(uuid.uuid4(), relay_server.address)
     # TODO(gpauloski): should we log something or set a flag in the manager?
-    await signaling_server.signaling_server._uuid_to_client[
+    await relay_server.relay_server._uuid_to_client[
         manager.uuid
     ].websocket.close()
     await manager.close()
 
 
-@pytest.mark.asyncio
-async def test_unexpected_server_disconnect(signaling_server) -> None:
-    manager = await PeerManager(uuid.uuid4(), signaling_server.address)
+@pytest.mark.asyncio()
+async def test_unexpected_server_disconnect(relay_server) -> None:
+    manager = await PeerManager(uuid.uuid4(), relay_server.address)
     # TODO(gpauloski): should we log something or set a flag in the manager?
-    await signaling_server.signaling_server._uuid_to_client[
+    await relay_server.relay_server._uuid_to_client[
         manager.uuid
     ].websocket.close(code=1002)
     await manager.close()
 
 
-@pytest.mark.asyncio
-async def test_serialization_error(signaling_server, caplog) -> None:
+@pytest.mark.asyncio()
+async def test_serialization_error(relay_server, caplog) -> None:
     # PeerManager should log an error and skip the message but
     # not raise an exception.
     caplog.set_level(logging.ERROR)
-    async with PeerManager(uuid.uuid4(), signaling_server.address) as manager:
-        assert manager._websocket_or_none is not None
+    async with PeerManager(uuid.uuid4(), relay_server.address) as manager:
+        assert manager._relay_server_client_or_none is not None
+        assert manager._relay_server_client_or_none._websocket is not None
         mock_recv = async_mock_once(
-            manager._websocket_or_none.recv,
+            manager._relay_server_client_or_none._websocket.recv,
             'nonsense_string',
         )
-        manager._websocket_or_none.recv = mock_recv  # type: ignore
+        manager._relay_server_client_or_none._websocket.recv = mock_recv  # type: ignore
         while not mock_recv.await_count > 1:
             await asyncio.sleep(0.01)
 
     assert any(
         [
             'error deserializing' in record.message
             and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
 
 
-@pytest.mark.asyncio
-async def test_unexpected_server_response(signaling_server, caplog) -> None:
+@pytest.mark.asyncio()
+async def test_unexpected_server_response(relay_server, caplog) -> None:
     # PeerManager should log an exception and skip the message but
     # not raise an exception.
     caplog.set_level(logging.ERROR)
-    async with PeerManager(uuid.uuid4(), signaling_server.address) as manager:
-        assert manager._websocket_or_none is not None
+    async with PeerManager(uuid.uuid4(), relay_server.address) as manager:
+        assert manager._relay_server_client_or_none is not None
+        message = messages.ServerResponse(
+            success=True,
+            message='',
+            error=False,
+        )
         mock_recv = async_mock_once(
-            manager._websocket_or_none.recv,
-            messages.encode(
-                messages.ServerResponse(success=True, message='', error=False),
-            ),
+            manager._relay_server_client_or_none.recv,
+            message,
         )
-        manager._websocket_or_none.recv = mock_recv  # type: ignore
+        manager._relay_server_client_or_none.recv = mock_recv  # type: ignore
         while not mock_recv.await_count > 1:
             await asyncio.sleep(0.01)
 
     assert any(
         [
             'got unexpected' in record.message and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
 
 
-@pytest.mark.asyncio
-async def test_unknown_message_type(signaling_server, caplog) -> None:
+@pytest.mark.asyncio()
+async def test_unknown_message_type(relay_server, caplog) -> None:
     # PeerManager should log an error and skip the message but
     # not raise an exception.
     caplog.set_level(logging.ERROR)
-    async with PeerManager(uuid.uuid4(), signaling_server.address) as manager:
-        assert manager._websocket_or_none is not None
+    async with PeerManager(uuid.uuid4(), relay_server.address) as manager:
+        assert manager._relay_server_client_or_none is not None
+        message = messages.ServerRegistration('name', uuid.uuid4())
         mock_recv = async_mock_once(
-            manager._websocket_or_none.recv,
-            messages.encode(messages.ServerRegistration('name', uuid.uuid4())),
+            manager._relay_server_client_or_none.recv,
+            message,
         )
-        manager._websocket_or_none.recv = mock_recv  # type: ignore
+        manager._relay_server_client_or_none.recv = mock_recv  # type: ignore
         while not mock_recv.await_count > 1:
             await asyncio.sleep(0.01)
 
     assert any(
         [
             'unknown message' in record.message and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
+
+
+@pytest.mark.asyncio()
+async def test_close_connection(relay_server) -> None:
+    async with PeerManager(
+        uuid.uuid4(),
+        relay_server.address,
+    ) as manager1, PeerManager(
+        uuid.uuid4(),
+        relay_server.address,
+        verify_certificate=False,
+    ) as manager2:
+        # Send message to make sure connection is open
+        await manager1.send(manager2.uuid, 'hello hello')
+        source_uuid, message = await manager2.recv()
+        assert source_uuid == manager1.uuid
+        assert message == 'hello hello'
+
+        await manager1.get_connection(manager2.uuid)
+        await manager2.get_connection(manager1.uuid)
+
+        await manager1.close_connection((manager1.uuid, manager2.uuid))
+        # Should be idempotent
+        await manager1.close_connection((manager1.uuid, manager2.uuid))
+
+        # Yield event loop to make sure peer connection closed callbacks fire
+        await asyncio.sleep(0.001)
+
+        assert len(manager1._peers) == 0
+        assert len(manager2._peers) == 0
+
+        # Send another message to make sure connection is reopened
+        await manager1.send(manager2.uuid, 'hello hello again')
+        source_uuid, message = await manager2.recv()
+        assert source_uuid == manager1.uuid
+        assert message == 'hello hello again'
```

### Comparing `proxystore-0.4.1a1/tests/p2p/messages_test.py` & `proxystore-0.5.0/tests/p2p/messages_test.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 
 from proxystore.p2p import messages
 
 _TEST_UUID = uuid.uuid4()
 
 
 @pytest.mark.parametrize(
-    'data,result',
+    ('data', 'result'),
     (
         # Normal conversions
         ({'source_uuid': _TEST_UUID}, {'source_uuid': str(_TEST_UUID)}),
         ({'SOURCE_UUID': _TEST_UUID}, {'SOURCE_UUID': str(_TEST_UUID)}),
         (
             {'source_uuid': _TEST_UUID, 'uuid': _TEST_UUID},
             {'source_uuid': str(_TEST_UUID), 'uuid': str(_TEST_UUID)},
@@ -34,15 +34,15 @@
     data: dict[str, Any],
     result: dict[str, Any],
 ) -> None:
     assert messages.uuid_to_str(data) == result
 
 
 @pytest.mark.parametrize(
-    'data,result,exception',
+    ('data', 'result', 'exception'),
     (
         # Normal conversions
         ({'source_uuid': str(_TEST_UUID)}, {'source_uuid': _TEST_UUID}, False),
         ({'SOURCE_UUID': str(_TEST_UUID)}, {'SOURCE_UUID': _TEST_UUID}, False),
         (
             {'source_uuid': str(_TEST_UUID), 'uuid': str(_TEST_UUID)},
             {'source_uuid': _TEST_UUID, 'uuid': _TEST_UUID},
```

### Comparing `proxystore-0.4.1a1/tests/p2p/server_cli_test.py` & `proxystore-0.5.0/tests/connectors/dim/zmq_test.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,128 +1,123 @@
+"""ZMQConnector Unit Tests."""
 from __future__ import annotations
 
-import asyncio
-import multiprocessing
-import os
-import pathlib
-import subprocess
-import sys
+import platform
 from unittest import mock
 
 import pytest
-import websockets
 
-from proxystore.p2p.client import connect
-from proxystore.p2p.server import main
+from proxystore.connectors.dim.exceptions import ServerTimeoutError
+from proxystore.connectors.dim.models import DIMKey
+from proxystore.connectors.dim.models import RPC
+from proxystore.connectors.dim.models import RPCResponse
+from proxystore.connectors.dim.zmq import wait_for_server
+from proxystore.connectors.dim.zmq import ZeroMQConnector
+from proxystore.connectors.dim.zmq import ZeroMQServer
+from proxystore.serialize import serialize
+from testing.compat import randbytes
 from testing.utils import open_port
 
-if sys.version_info >= (3, 8):  # pragma: >=3.8 cover
-    from unittest.mock import AsyncMock
-else:  # pragma: <3.8 cover
-    from asynctest import CoroutineMock as AsyncMock
-
-
-def test_logging_dir(tmp_path: pathlib.Path) -> None:
-    tmp_dir = os.path.join(tmp_path, 'log-dir')
-    assert not os.path.isdir(tmp_dir)
-    with mock.patch('proxystore.p2p.server.serve', AsyncMock()):
-        main(['--log-dir', str(tmp_dir)])
-    assert os.path.isdir(tmp_dir)
-
-
-def test_logging_config(tmp_path: pathlib.Path) -> None:
-    with subprocess.Popen(
-        [
-            'signaling-server',
-            '--port',
-            str(open_port()),
-            '--log-dir',
-            str(tmp_path),
-            '--log-level',
-            'INFO',
-        ],
-        stdout=subprocess.PIPE,
-        stderr=subprocess.STDOUT,
-        universal_newlines=True,
-    ) as server_handle:
-        # Wait for server to log that it is listening
-        assert server_handle.stdout is not None
-        for line in server_handle.stdout:  # pragma: no cover
-            if 'serving' in line:
-                break
-
-        server_handle.terminate()
-
-    logs = [
-        f
-        for f in os.listdir(tmp_path)
-        if os.path.isfile(os.path.join(tmp_path, f))
-    ]
-    for log in logs:
-        with open(os.path.join(tmp_path, log)) as f:
-            assert 'DEBUG' not in f.read()
-    assert len(logs) >= 1
-
-
-@pytest.mark.timeout(5)
-@pytest.mark.asyncio
-async def test_server_with_mock_ssl() -> None:
-    host = 'localhost'
+if platform.system() == 'Darwin':  # pragma: no cover
+    # MacOS GitHub Actions runners are slow
+    TIMEOUT = 1.0
+else:  # pragma: no cover
+    TIMEOUT = 0.5
+
+TEST_KEY = DIMKey(
+    'zmq',
+    obj_id='key',
+    size=0,
+    peer_host='localhost',
+    peer_port=0,
+)
+
+
+def test_wait_for_server() -> None:
+    with pytest.raises(ServerTimeoutError, match='timeout'):
+        wait_for_server('127.0.0.1', open_port(), timeout=0.01)
+
+
+def test_large_message_sizes() -> None:
+    chunk_length = 1000
+    with ZeroMQConnector(
+        open_port(),
+        chunk_length=1000,
+        timeout=TIMEOUT,
+    ) as connector:
+        data = randbytes(3 * chunk_length)
+        key = connector.put(data)
+        assert connector.get(key) is not None
+        connector.evict(key)
+
+
+def test_multiple_connectors() -> None:
     port = open_port()
-    address = f'ws://{host}:{port}'
+    # C1 creates the server
+    c1 = ZeroMQConnector(port, timeout=TIMEOUT)
+    c2 = ZeroMQConnector(port, timeout=TIMEOUT)
 
-    process = multiprocessing.Process(
-        target=main,
-        args=(
-            ['--host', host, '--port', str(port), '--log-level', 'CRITICAL'],
-        ),
-    )
-    process.start()
+    key = c1.put(b'data')
+    assert c2.get(key) == b'data'
 
-    while True:
-        try:
-            _, _, websocket = await connect(address)
-        except OSError:
-            await asyncio.sleep(0.01)
-        else:
-            # Coverage doesn't detect the singular break but it does
-            # get executed to break from the loop
-            break  # pragma: no cover
-
-    pong_waiter = await websocket.ping()
-    await asyncio.wait_for(pong_waiter, 1)
-
-    process.terminate()
-
-    with pytest.raises(websockets.exceptions.ConnectionClosedOK):
-        await websocket.recv()
-
-
-@pytest.mark.timeout(5)
-@pytest.mark.asyncio
-async def test_start_server_cli() -> None:
-    host = 'localhost'
-    port = str(open_port())
-    address = f'ws://{host}:{port}'
-
-    server_handle = subprocess.Popen(
-        ['signaling-server', '--host', host, '--port', port],
-        stdout=subprocess.PIPE,
-        stderr=subprocess.STDOUT,
-        universal_newlines=True,
-    )
+    # C2 did not create the server so closing should not kill it
+    c2.close()
+    assert c1.get(key) == b'data'
+
+    # C1 will actually stop the server
+    c1.close()
 
-    # Wait for server to log that it is listening
-    assert server_handle.stdout is not None
-    for line in server_handle.stdout:  # pragma: no cover
-        if 'serving signaling server' in line:
-            break
-
-    _, _, websocket = await connect(address)
-    pong_waiter = await websocket.ping()
-    await asyncio.wait_for(pong_waiter, 1)
 
-    server_handle.stdout.close()
-    server_handle.terminate()
+def test_server_errors() -> None:
+    server = ZeroMQServer()
 
-    with pytest.raises(websockets.exceptions.ConnectionClosedOK):
-        await websocket.recv()
+    rpc = RPC('exists', key=TEST_KEY)
+    with mock.patch.object(server, 'exists', side_effect=RuntimeError('xyz')):
+        response = server.handle_rpc(rpc)
+        assert response.exception is not None
+        assert 'xyz' in str(response.exception)
+
+
+def test_handle_server_error_responses() -> None:
+    rpc = RPC('exists', TEST_KEY)
+    response = RPCResponse(
+        'exists',
+        key=TEST_KEY,
+        exception=RuntimeError('xyz'),
+    )
+
+    port = open_port()
+    with mock.patch('proxystore.connectors.dim.zmq.wait_for_server'):
+        with ZeroMQConnector(port, timeout=TIMEOUT) as connector:
+            with mock.patch.object(
+                connector.socket,
+                'send_multipart',
+            ), mock.patch.object(
+                connector.socket,
+                'recv_multipart',
+                return_value=[serialize(response)],
+            ):
+                with pytest.raises(RuntimeError, match='xyz'):
+                    connector._send_rpcs([rpc])
+
+
+def test_provide_ip() -> None:
+    host = '127.0.0.1'
+    with mock.patch(
+        'proxystore.connectors.dim.zmq.wait_for_server',
+    ):
+        with ZeroMQConnector(port=0, address=host) as connector:
+            assert connector.address == host
+
+
+@pytest.mark.skipif(
+    platform.system() == 'Darwin',
+    reason=(
+        'Resolving an IP address from an interface is not supported on MacOS'
+    ),
+)
+def test_provide_interface() -> None:  # pragma: darwin no cover
+    with mock.patch(
+        'proxystore.connectors.dim.zmq.wait_for_server',
+    ):
+        with ZeroMQConnector(port=0, interface='lo') as connector:
+            assert connector.address == '127.0.0.1'
```

### Comparing `proxystore-0.4.1a1/tests/p2p/server_test.py` & `proxystore-0.5.0/tests/p2p/relay_test.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,115 +4,120 @@
 import logging
 from uuid import uuid4
 
 import pytest
 import websockets
 
 from proxystore.p2p import messages
-from proxystore.p2p.client import connect
+from proxystore.p2p.relay_client import RelayServerClient
 
 # Use 200ms as wait_for/timeout to keep test short
 _WAIT_FOR = 0.2
 
 
-@pytest.mark.asyncio
-async def test_connect_twice(signaling_server) -> None:
-    uuid, _, websocket = await connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_connect_twice(relay_server) -> None:
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
     pong_waiter = await websocket.ping()
     await asyncio.wait_for(pong_waiter, _WAIT_FOR)
     await websocket.send(
         messages.encode(
             messages.ServerRegistration(
                 name='different-host',
-                uuid=uuid,
+                uuid=client.uuid,
             ),
         ),
     )
     message_ = await asyncio.wait_for(websocket.recv(), _WAIT_FOR)
     assert isinstance(message_, str)
     message = messages.decode(message_)
     assert isinstance(message, messages.ServerResponse)
     assert message.success
     assert not message.error
 
 
-@pytest.mark.asyncio
-async def test_connect_reconnect_new_socket(signaling_server) -> None:
-    uuid1, name, websocket1 = await connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_connect_reconnect_new_socket(relay_server) -> None:
+    client1 = RelayServerClient(relay_server.address)
+    websocket1 = await client1.connect()
     pong_waiter = await websocket1.ping()
     await asyncio.wait_for(pong_waiter, _WAIT_FOR)
 
-    uuid2, _, websocket2 = await connect(
-        signaling_server.address,
-        uuid=uuid1,
-        name=name,
+    client2 = RelayServerClient(
+        relay_server.address,
+        client_uuid=client1.uuid,
+        client_name=client1.name,
     )
-    assert uuid1 == uuid2
+    websocket2 = await client2.connect()
+    assert client1.uuid == client2.uuid
     await websocket1.wait_closed()
     assert websocket1.close_code != 1000
     pong_waiter = await websocket2.ping()
     await asyncio.wait_for(pong_waiter, _WAIT_FOR)
 
 
-@pytest.mark.asyncio
-async def test_expected_client_disconnect(signaling_server) -> None:
-    uuid, _, websocket = await connect(signaling_server.address)
-    client = signaling_server.signaling_server._uuid_to_client[uuid]
+@pytest.mark.asyncio()
+async def test_expected_client_disconnect(relay_server) -> None:
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
+    server_client = relay_server.relay_server._uuid_to_client[client.uuid]
     assert (
-        client
-        in signaling_server.signaling_server._websocket_to_client.values()
+        server_client
+        in relay_server.relay_server._websocket_to_client.values()
     )
 
     await websocket.close()
     # TODO(gpauloski): remove sleep. It is here to give time for the
     # server's unregister coroutine to finish
     await asyncio.sleep(0.05)
 
-    assert uuid not in signaling_server.signaling_server._uuid_to_client
+    assert client.uuid not in relay_server.relay_server._uuid_to_client
     assert (
-        client
-        not in signaling_server.signaling_server._websocket_to_client.values()
+        server_client
+        not in relay_server.relay_server._websocket_to_client.values()
     )
 
 
-@pytest.mark.asyncio
-async def test_unexpected_client_disconnect(signaling_server) -> None:
-    uuid, _, websocket = await connect(signaling_server.address)
-    client = signaling_server.signaling_server._uuid_to_client[uuid]
+@pytest.mark.asyncio()
+async def test_unexpected_client_disconnect(relay_server) -> None:
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
+    server_client = relay_server.relay_server._uuid_to_client[client.uuid]
     assert (
-        client
-        in signaling_server.signaling_server._websocket_to_client.values()
+        server_client
+        in relay_server.relay_server._websocket_to_client.values()
     )
 
     await websocket.close(code=1002)
     # TODO(gpauloski): remove sleep. It is here to give time for the
     # server's unregister coroutine to finish
     await asyncio.sleep(0.05)
 
-    assert uuid not in signaling_server.signaling_server._uuid_to_client
+    assert client.uuid not in relay_server.relay_server._uuid_to_client
     assert (
-        client
-        not in signaling_server.signaling_server._websocket_to_client.values()
+        server_client
+        not in relay_server.relay_server._websocket_to_client.values()
     )
 
 
-@pytest.mark.asyncio
-async def test_server_deserialization_fails_silently(signaling_server) -> None:
-    _, _, websocket = await connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_server_deserialization_fails_silently(relay_server) -> None:
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
     # This message should cause deserialization error on server but
     # server should catch and wait for next message
     await websocket.send('invalid message')
     pong_waiter = await websocket.ping()
     await asyncio.wait_for(pong_waiter, _WAIT_FOR)
 
 
-@pytest.mark.asyncio
-async def test_endpoint_not_registered_error(signaling_server) -> None:
-    # _, _, websocket = await connect(signaling_server.address)
-    websocket = await websockets.client.connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_endpoint_not_registered_error(relay_server) -> None:
+    websocket = await websockets.client.connect(relay_server.address)
     await websocket.send(
         messages.encode(
             messages.PeerConnection(
                 source_uuid=uuid4(),
                 source_name='',
                 peer_uuid=uuid4(),
                 description_type='offer',
@@ -125,127 +130,120 @@
     message = messages.decode(message_)
     assert isinstance(message, messages.ServerResponse)
     assert message.error
     assert message.message is not None
     assert 'not registered' in message.message
 
 
-@pytest.mark.asyncio
-async def test_p2p_message_passing(signaling_server) -> None:
-    peer1_uuid, peer1_name, peer1 = await connect(signaling_server.address)
-    peer2_uuid, peer2_name, peer2 = await connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_p2p_message_passing(relay_server) -> None:
+    client1 = RelayServerClient(relay_server.address)
+    await client1.connect()
+    peer1_name, peer1_uuid = client1.name, client1.uuid
+    client2 = RelayServerClient(relay_server.address)
+    await client2.connect()
+    peer2_name, peer2_uuid = client2.name, client2.uuid
 
     # Peer1 -> Peer2
-    await peer1.send(
-        messages.encode(
-            messages.PeerConnection(
-                source_uuid=peer1_uuid,
-                source_name=peer1_name,
-                peer_uuid=peer2_uuid,
-                description_type='offer',
-                description='',
-            ),
+    await client1.send(
+        messages.PeerConnection(
+            source_uuid=peer1_uuid,
+            source_name=peer1_name,
+            peer_uuid=peer2_uuid,
+            description_type='offer',
+            description='',
         ),
     )
-    message_ = await asyncio.wait_for(peer2.recv(), 1)
-    assert isinstance(message_, str)
-    message = messages.decode(message_)
+    message = await asyncio.wait_for(client2.recv(), 1)
     assert isinstance(message, messages.PeerConnection)
 
     # Peer2 -> Peer1
-    await peer2.send(
-        messages.encode(
-            messages.PeerConnection(
-                source_uuid=peer2_uuid,
-                source_name=peer2_name,
-                peer_uuid=peer1_uuid,
-                description_type='offer',
-                description='',
-            ),
+    await client2.send(
+        messages.PeerConnection(
+            source_uuid=peer2_uuid,
+            source_name=peer2_name,
+            peer_uuid=peer1_uuid,
+            description_type='offer',
+            description='',
         ),
     )
-    message_ = await asyncio.wait_for(peer1.recv(), 1)
-    assert isinstance(message_, str)
-    message = messages.decode(message_)
+    message = await asyncio.wait_for(client1.recv(), 1)
     assert isinstance(message, messages.PeerConnection)
 
     # Peer1 -> Peer1
-    await peer1.send(
-        messages.encode(
-            messages.PeerConnection(
-                source_uuid=peer1_uuid,
-                source_name=peer1_name,
-                peer_uuid=peer1_uuid,
-                description_type='offer',
-                description='',
-            ),
+    await client1.send(
+        messages.PeerConnection(
+            source_uuid=peer1_uuid,
+            source_name=peer1_name,
+            peer_uuid=peer1_uuid,
+            description_type='offer',
+            description='',
         ),
     )
-    message_ = await asyncio.wait_for(peer1.recv(), 1)
-    assert isinstance(message_, str)
-    message = messages.decode(message_)
+    message = await asyncio.wait_for(client1.recv(), 1)
     assert isinstance(message, messages.PeerConnection)
 
 
-@pytest.mark.asyncio
-async def test_p2p_message_passing_unknown_peer(signaling_server) -> None:
-    peer1_uuid, peer1_name, peer1 = await connect(signaling_server.address)
+@pytest.mark.asyncio()
+async def test_p2p_message_passing_unknown_peer(relay_server) -> None:
+    client1 = RelayServerClient(relay_server.address)
+    await client1.connect()
+    peer1_name, peer1_uuid = client1.name, client1.uuid
     peer2_uuid = uuid4()
 
-    await peer1.send(
-        messages.encode(
-            messages.PeerConnection(
-                source_uuid=peer1_uuid,
-                source_name=peer1_name,
-                peer_uuid=peer2_uuid,
-                description_type='offer',
-                description='',
-            ),
+    await client1.send(
+        messages.PeerConnection(
+            source_uuid=peer1_uuid,
+            source_name=peer1_name,
+            peer_uuid=peer2_uuid,
+            description_type='offer',
+            description='',
         ),
     )
-    message_ = await asyncio.wait_for(peer1.recv(), _WAIT_FOR)
-    assert isinstance(message_, str)
-    message = messages.decode(message_)
+    message = await asyncio.wait_for(client1.recv(), _WAIT_FOR)
     assert isinstance(message, messages.PeerConnection)
     assert message.error is not None
-    assert str(peer2_uuid) in message.error and 'unknown' in message.error
+    assert str(peer2_uuid) in message.error
+    assert 'unknown' in message.error
 
 
-@pytest.mark.asyncio
-async def test_signaling_server_send_encode_error(
-    signaling_server,
+@pytest.mark.asyncio()
+async def test_relay_server_send_encode_error(
+    relay_server,
     caplog,
 ) -> None:
     caplog.set_level(logging.ERROR)
 
-    _, _, websocket = await connect(signaling_server.address)
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
     # Error should be logged but not raised
-    await signaling_server.signaling_server.send(websocket, 'abc')
+    await relay_server.relay_server.send(websocket, 'abc')
 
     assert any(
         [
-            'failed to encode' in record.message
+            'Failed to encode' in record.message
             and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
 
 
-@pytest.mark.asyncio
-async def test_signaling_server_send_connection_closed(
-    signaling_server,
+@pytest.mark.asyncio()
+async def test_relay_server_send_connection_closed(
+    relay_server,
     caplog,
 ) -> None:
     caplog.set_level(logging.ERROR)
 
-    _, _, websocket = await connect(signaling_server.address)
+    client = RelayServerClient(relay_server.address)
+    websocket = await client.connect()
     # Error should be logged but not raised
     await websocket.close()
-    await signaling_server.signaling_server.send(websocket, messages.Message())
+    await relay_server.relay_server.send(websocket, messages.Message())
 
     assert any(
         [
-            'connection closed' in record.message
+            'Connection closed' in record.message
             and record.levelname == 'ERROR'
             for record in caplog.records
         ],
     )
```

### Comparing `proxystore-0.4.1a1/tests/p2p/task_test.py` & `proxystore-0.5.0/tests/p2p/task_test.py`

 * *Files identical despite different names*

### Comparing `proxystore-0.4.1a1/tests/proxy_test.py` & `proxystore-0.5.0/tests/proxy_test.py`

 * *Files 8% similar despite different names*

```diff
@@ -38,15 +38,15 @@
 
     # Test extracting
     x_ = ps.proxy.extract(p)
     assert isinstance(x_, list)
     assert not isinstance(x_, Proxy)
     assert x == x_
 
-    p = p + [1]
+    p = p + [1]  # noqa
     assert not isinstance(p, Proxy)
     assert p == [1, 2, 3, 1]
     assert len(p) == 4
     assert sum(p) == 7
 
     # Adding two proxies returns type of wrapped
     p = Proxy(f)
```

### Comparing `proxystore-0.4.1a1/tests/serialization_test.py` & `proxystore-0.5.0/tests/serialization_test.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 """Serialization Unit Tests."""
 from __future__ import annotations
 
-from pytest import raises
+import pytest
 
 from proxystore.serialize import deserialize
 from proxystore.serialize import SerializationError
 from proxystore.serialize import serialize
 
 
 def test_serialization() -> None:
@@ -22,18 +22,18 @@
     b = serialize(xa)
     assert deserialize(b) == xa
 
     b = serialize(lambda: [1, 2, 3])
     f = deserialize(b)
     assert f() == [1, 2, 3]
 
-    with raises(ValueError):
+    with pytest.raises(ValueError):
         # deserialize raises ValueError on non-bytes inputs
         deserialize('xxx')  # type: ignore
 
-    with raises(SerializationError):
+    with pytest.raises(SerializationError):
         # No identifier
         deserialize(b'xxx')
 
-    with raises(SerializationError):
+    with pytest.raises(SerializationError):
         # Fake identifier 'xxx'
         deserialize(b'99\nxxx')
```

### Comparing `proxystore-0.4.1a1/tests/store/cache_test.py` & `proxystore-0.5.0/tests/store/cache_test.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 """Cache Unit Tests."""
 from __future__ import annotations
 
-from pytest import raises
+import pytest
 
 from proxystore.store.cache import LRUCache
 
 
 def test_lru_raises() -> None:
     """Test LRU Error Handling."""
-    with raises(ValueError):
+    with pytest.raises(ValueError):
         LRUCache(-1)
 
 
 def test_lru_cache() -> None:
     """Test LRU Cache."""
     c: LRUCache[str, int] = LRUCache(4)
     # Put 1, 2, 3, 4 in cache
```

### Comparing `proxystore-0.4.1a1/tests/store/endpoint_test.py` & `proxystore-0.5.0/tests/connectors/endpoint_test.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,95 +1,88 @@
-"""EndpointStore Unit Tests."""
+"""EndpointConnector Unit Tests."""
 from __future__ import annotations
 
 import uuid
 from unittest import mock
 
 import pytest
 import requests
 
+from proxystore.connectors.endpoint import EndpointConnector
+from proxystore.connectors.endpoint import EndpointConnectorError
 from proxystore.endpoint.serve import MAX_CHUNK_LENGTH
-from proxystore.store.endpoint import EndpointStore
-from proxystore.store.endpoint import EndpointStoreError
 from testing.compat import randbytes
 
 
 def test_no_endpoints_provided() -> None:
     with pytest.raises(ValueError):
-        EndpointStore('name', endpoints=[])
+        EndpointConnector(endpoints=[])
 
 
-def test_no_endpoints_match(endpoint_store) -> None:
-    with pytest.raises(EndpointStoreError, match='Failed to find'):
-        EndpointStore(
-            'name',
+def test_no_endpoints_match(endpoint_connector) -> None:
+    with pytest.raises(EndpointConnectorError, match='Failed to find'):
+        EndpointConnector(
             endpoints=[str(uuid.uuid4())],
-            proxystore_dir=endpoint_store.kwargs['proxystore_dir'],
+            proxystore_dir=endpoint_connector.config()['proxystore_dir'],
         )
 
 
-def test_no_endpoints_accessible(endpoint_store) -> None:
+def test_no_endpoints_accessible(endpoint_connector) -> None:
     response = requests.Response()
     response.status_code = 400
 
-    with mock.patch('requests.get', return_value=response):
-        with pytest.raises(EndpointStoreError, match='Failed to find'):
-            EndpointStore('test', **endpoint_store.kwargs)
+    with mock.patch('requests.Session.get', return_value=response):
+        with pytest.raises(EndpointConnectorError, match='Failed to find'):
+            EndpointConnector.from_config(endpoint_connector.config())
 
 
-def test_endpoint_uuid_mismatch(endpoint_store) -> None:
+def test_endpoint_uuid_mismatch(endpoint_connector) -> None:
     response = requests.Response()
     response.status_code = 200
     response.json = lambda: {'uuid': str(uuid.uuid4())}  # type: ignore
 
-    with mock.patch('requests.get', return_value=response):
-        with pytest.raises(EndpointStoreError, match='Failed to find'):
-            EndpointStore('test', **endpoint_store.kwargs)
+    with mock.patch('requests.Session.get', return_value=response):
+        with pytest.raises(EndpointConnectorError, match='Failed to find'):
+            EndpointConnector.from_config(endpoint_connector.config())
 
 
-def test_bad_responses(endpoint_store) -> None:
+def test_bad_responses(endpoint_connector) -> None:
     """Test handling of bad responses from Endpoint."""
-    store = EndpointStore(
-        endpoint_store.name,
-        **endpoint_store.kwargs,
-        cache_size=0,
-    )
+    connector = EndpointConnector.from_config(endpoint_connector.config())
 
     response = requests.Response()
     response.status_code = 400
 
-    with mock.patch('requests.get', return_value=response):
-        key = store.set([1, 2, 3])
-        assert store.get(key) is None
+    with mock.patch('requests.Session.get', return_value=response):
+        key = connector.put(b'value')
+        assert connector.get(key) is None
 
     response.status_code = 401
 
-    with mock.patch('requests.get', return_value=response):
-        with pytest.raises(EndpointStoreError, match='401'):
-            store.exists(key)
-
-        with pytest.raises(EndpointStoreError, match='401'):
-            store.get(key)
-
-    with mock.patch('requests.post', return_value=response):
-        with pytest.raises(EndpointStoreError, match='401'):
-            store.evict(key)
-
-        with pytest.raises(EndpointStoreError, match='401'):
-            store.set([1, 2, 3])
-
-
-def test_chunked_requests(endpoint_store) -> None:
-    store = EndpointStore(
-        endpoint_store.name,
-        **endpoint_store.kwargs,
-        cache_size=0,
-    )
+    with mock.patch('requests.Session.get', return_value=response):
+        with pytest.raises(EndpointConnectorError, match='401'):
+            connector.exists(key)
+
+        with pytest.raises(EndpointConnectorError, match='401'):
+            connector.get(key)
+
+    with mock.patch('requests.Session.post', return_value=response):
+        with pytest.raises(EndpointConnectorError, match='401'):
+            connector.evict(key)
+
+        with pytest.raises(EndpointConnectorError, match='401'):
+            connector.put(b'value')
+
+    connector.close()
+
+
+def test_chunked_requests(endpoint_connector) -> None:
+    connector = EndpointConnector.from_config(endpoint_connector.config())
 
     # Set to 2*chunk_size + 1 to force there to be two full size chunks
     # and one partial chunk
     data = randbytes((2 * MAX_CHUNK_LENGTH) + 1)
-    key = store.set(data)
+    key = connector.put(data)
 
-    assert store.get(key) == data
+    assert connector.get(key) == data
 
-    store.close()
+    connector.close()
```

### Comparing `proxystore-0.4.1a1/tests/store/file_test.py` & `proxystore-0.5.0/tests/connectors/file_test.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,39 +1,40 @@
-"""FileStore Unit Tests."""
+"""FileConnector Unit Tests."""
 from __future__ import annotations
 
 import os
 import pathlib
 import tempfile
 
-from proxystore.store.file import FileStore
+from proxystore.connectors.file import FileConnector
 
 
-def test_file_store_close(tmp_path: pathlib.Path) -> None:
-    """Test FileStore Cleanup."""
-    store = FileStore('files', store_dir=str(tmp_path))
+def test_file_conenctor_close(tmp_path: pathlib.Path) -> None:
+    """Test FileConnector Cleanup."""
+    connector = FileConnector(store_dir=str(tmp_path))
 
     assert os.path.exists(tmp_path)
 
-    store.close()
+    connector.close()
 
     assert not os.path.exists(tmp_path)
 
 
 def test_cwd_change(tmp_path: pathlib.Path) -> None:
-    """Checks FileStore proxies still resolve when the CWD changes."""
+    """Checks FileConnector still resolve when the CWD changes."""
     current = os.getcwd()
 
     with tempfile.TemporaryDirectory() as tmp_dir:
         os.chdir(tmp_dir)
 
         # relative to tmp_dir
         store_dir = './store-dir'
         new_working_dir = os.path.join(tmp_dir, 'new-working-dir')
         os.makedirs(new_working_dir, exist_ok=True)
 
-        with FileStore('store', store_dir=store_dir, cache_size=0) as store:
-            key = store.set('data')
-            os.chdir(new_working_dir)
-            assert store.get(key) == 'data'
+        connector = FileConnector(store_dir=store_dir)
+        key = connector.put(b'data')
+        os.chdir(new_working_dir)
+        assert connector.get(key) == b'data'
+        connector.close()
 
     os.chdir(current)
```

### Comparing `proxystore-0.4.1a1/tests/store/globus_test.py` & `proxystore-0.5.0/tests/connectors/globus_test.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,24 +1,24 @@
-"""Globus Store Functionality Tests."""
+"""GlobusConnector Unit Tests."""
 from __future__ import annotations
 
 import json
 import os
 import re
 import uuid
 from unittest import mock
 
 import globus_sdk
 import pytest
 
+from proxystore.connectors.globus import GlobusConnector
+from proxystore.connectors.globus import GlobusEndpoint
+from proxystore.connectors.globus import GlobusEndpoints
+from proxystore.connectors.globus import GlobusKey
 from proxystore.globus import GlobusAuthFileError
-from proxystore.store.globus import GlobusEndpoint
-from proxystore.store.globus import GlobusEndpoints
-from proxystore.store.globus import GlobusStore
-from proxystore.store.globus import GlobusStoreKey
 
 EP1 = GlobusEndpoint(
     uuid='1',
     endpoint_path='/path',
     local_path='/path',
     host_regex='localhost',
 )
@@ -44,14 +44,19 @@
     uuid='1',
     endpoint_path='/path',
     local_path='/path',
     host_regex='localhost',
 )
 
 
+def test_reprs() -> None:
+    assert isinstance(str(EP1), str)
+    assert isinstance(str(GlobusEndpoints([EP1, EP2])), str)
+
+
 def test_globus_endpoint_objects() -> None:
     """Test GlobusEndpoint(s) Objects."""
     with pytest.raises(TypeError):
         GlobusEndpoint(
             uuid=1,  # type: ignore
             endpoint_path='1',
             local_path='1',
@@ -159,79 +164,68 @@
 
     # Ensure Patterns are converted to strings in .dict()
     data['UUID1']['host_regex'] = re.compile('host1')  # type: ignore
     endpoints = GlobusEndpoints.from_dict(data)
     assert isinstance(endpoints.dict()['UUID1']['host_regex'], str)
 
 
-def test_globus_store_init(globus_store) -> None:
-    """Test GlobusStore Initialization."""
+def test_globus_connector_init(globus_connector) -> None:
+    """Test GlobusConnector Initialization."""
     eps = GlobusEndpoints([EP1, EP2])
 
-    GlobusStore('globus', endpoints=[EP1, EP2])
-
-    s1 = GlobusStore('globus1', endpoints=[EP1, EP2])
-    s2 = GlobusStore('globus2', endpoints=eps)
-    s3 = GlobusStore('globus3', endpoints=eps.dict())
-    assert s1.kwargs == s2.kwargs == s3.kwargs
+    s1 = GlobusConnector(endpoints=[EP1, EP2])
+    s2 = GlobusConnector(endpoints=eps)
+    s3 = GlobusConnector(endpoints=eps.dict())
+    assert s1.config() == s2.config() == s3.config()
 
     with pytest.raises(ValueError):
         # Invalid endpoint type
-        GlobusStore('globus', endpoints=None)  # type: ignore[arg-type]
+        GlobusConnector(endpoints=None)  # type: ignore[arg-type]
 
     with pytest.raises(ValueError):
         # Too many endpoints
-        GlobusStore('globus', endpoints=[EP1, EP2, EP3])
+        GlobusConnector(endpoints=[EP1, EP2, EP3])
 
     with pytest.raises(ValueError):
         # Not enough endpoints
-        GlobusStore('globus', endpoints=[EP1])
+        GlobusConnector(endpoints=[EP1])
 
 
-def test_globus_store_internals(globus_store) -> None:
-    """Test GlobusStore internal mechanisms."""
-    store = GlobusStore('globus', **globus_store.kwargs)
+def test_globus_connector_internals(globus_connector) -> None:
+    """Test GlobusConnector internal mechanisms."""
+    connector = GlobusConnector.from_config(globus_connector.config())
 
     class PatchedError(globus_sdk.TransferAPIError):
         def __init__(self, status: int):
             self.http_status = status
 
     def _http_error(status: int):
         def _error(*args, **kwargs) -> None:
             raise PatchedError(status)
 
         return _error
 
-    store._transfer_client.get_task = _http_error(400)  # type: ignore
-    assert not store._validate_task_id('uuid')
-    assert not store.exists(GlobusStoreKey('fake', 'fake'))
+    connector._transfer_client.get_task = _http_error(400)  # type: ignore
+    assert not connector._validate_task_id('uuid')
+    assert not connector.exists(GlobusKey('fake', 'fake'))
 
-    store._transfer_client.get_task = _http_error(401)  # type: ignore
+    connector._transfer_client.get_task = _http_error(401)  # type: ignore
     with pytest.raises(globus_sdk.TransferAPIError):
-        store._validate_task_id('uuid')
+        connector._validate_task_id('uuid')
 
     def _fail_wait(*args, **kwargs) -> bool:
         return False
 
-    store._transfer_client.task_wait = _fail_wait  # type: ignore
+    connector._transfer_client.task_wait = _fail_wait  # type: ignore
     with pytest.raises(RuntimeError):
-        store._wait_on_tasks('1234')
-
-
-def test_globus_store_set_batch_type_error(globus_store) -> None:
-    """Test GlobusStore internal mechanisms."""
-    store = GlobusStore('globus', **globus_store.kwargs)
-
-    objs = [1, 2, 3]
-    with pytest.raises(TypeError):
-        store.set_batch(objs, serializer=lambda s: s)
+        connector._wait_on_tasks('1234')
 
 
-def test_get_filepath(globus_store) -> None:
-    """Test GlobusStore filepath building."""
+def test_get_filepath(globus_connector) -> None:
+    """Test GlobusConnector filepath building."""
     endpoints = GlobusEndpoints(
         [
             GlobusEndpoint(
                 uuid='EP1UUID',
                 endpoint_path='/~/',
                 local_path='/tmp/proxystore-test-1',
                 host_regex='localhost',
@@ -241,24 +235,24 @@
                 endpoint_path='/~/',
                 local_path='/tmp/proxystore-test-2',
                 host_regex='localhost',
             ),
         ],
     )
 
-    store = GlobusStore(globus_store.name, endpoints=endpoints)
+    connector = GlobusConnector(endpoints=endpoints)
 
     filename = 'test_file'
     for endpoint in endpoints:
         expected_path = os.path.join(endpoint.local_path, filename)
-        assert store._get_filepath(filename, endpoint) == expected_path
+        assert connector._get_filepath(filename, endpoint) == expected_path
 
 
-def test_expand_user_path(globus_store) -> None:
-    """Test GlobusStore expands user path."""
+def test_expand_user_path(globus_connector) -> None:
+    """Test GlobusConnector expands user path."""
     store_dir = '.cache/proxystore_cache'
     short_path = os.path.join('~', store_dir)
     full_path = os.path.join(os.path.expanduser('~'), store_dir)
 
     ep1 = GlobusEndpoint(
         uuid='EP1UUID',
         endpoint_path='/~/',
@@ -268,35 +262,35 @@
     ep2 = GlobusEndpoint(
         uuid='EP2UUID',
         endpoint_path='/~/',
         local_path=full_path,
         host_regex='localhost',
     )
 
-    store = GlobusStore('globus', endpoints=[ep1, ep2])
+    connector = GlobusConnector(endpoints=[ep1, ep2])
 
     filename = 'test_file'
-    assert '~' not in store._get_filepath(filename, ep1)
-    assert store._get_filepath(filename, ep1) == store._get_filepath(
+    assert '~' not in connector._get_filepath(filename, ep1)
+    assert connector._get_filepath(filename, ep1) == connector._get_filepath(
         filename,
         ep2,
     )
 
 
 def test_globus_auth_not_done() -> None:
     """Test Globus auth missing during Store init."""
     with mock.patch(
-        'proxystore.store.globus.get_proxystore_authorizer',
+        'proxystore.connectors.globus.get_proxystore_authorizer',
         side_effect=GlobusAuthFileError,
     ):
         with pytest.raises(GlobusAuthFileError, match='Complete the'):
-            GlobusStore('store', endpoints=[EP1, EP2])
+            GlobusConnector(endpoints=[EP1, EP2])
 
 
-def test_globus_store_key_equality() -> None:
-    """Test GlobusStoreKey custom equality."""
-    key = GlobusStoreKey('a', 'b')
-    assert key == GlobusStoreKey('a', 'b')
+def test_globus_connector_key_equality() -> None:
+    """Test GlobusKey custom equality."""
+    key = GlobusKey('a', 'b')
+    assert key == GlobusKey('a', 'b')
     assert key == ('a', 'b')
     assert key != ('b', 'b')
     assert key == ('a', 'c')
     assert key != 'a'
```

### Comparing `proxystore-0.4.1a1/tests/store/store_basics_test.py` & `proxystore-0.5.0/tests/store/store_basics_test.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,25 +23,26 @@
 def test_store_base(store_implementation: StoreFixtureType) -> None:
     """Test Store Base Functionality."""
     store, store_info = store_implementation
 
     key_fake = missing_key(store)
     value = 'test_value'
 
-    # Store.set()
-    key_bytes = store.set(str.encode(value))
-    key_str = store.set(value)
-    key_callable = store.set(lambda: value)
-    key_array = store.set([1, 2, 3])
+    # Store.put()
+    key_bytes = store.put(str.encode(value))
+    key_str = store.put(value)
+    key_callable = store.put(lambda: value)
+    key_array = store.put([1, 2, 3])
 
     # Store.get()
     assert store.get(key_bytes) == str.encode(value)
     assert store.get(key_str) == value
     c = store.get(key_callable)
-    assert c is not None and c.__call__() == value
+    assert c is not None
+    assert c.__call__() == value
     assert store.get(key_fake) is None
     assert store.get(key_fake, default='alt_value') == 'alt_value'
     assert store.get(key_array) == [1, 2, 3]
 
     # Store.exists()
     assert store.exists(key_bytes)
     assert store.exists(key_str)
@@ -55,35 +56,39 @@
     store.evict(key_fake)
 
 
 def test_store_caching(store_implementation: StoreFixtureType) -> None:
     """Test Store Caching Functionality."""
     store, _ = store_implementation
 
-    assert store._cache.maxsize == 0
+    assert store.cache.maxsize == 0
     value = 'test_value'
 
     # Test cache size 0
-    key1 = store.set(value)
+    key1 = store.put(value)
     assert store.get(key1) == value
     assert not store.is_cached(key1)
 
     # Manually change cache size to size 1
     new_cache: LRUCache[str, Any] = LRUCache(1)
-    with mock.patch.object(store, '_cache', new_cache):
+    with mock.patch.object(store, 'cache', new_cache):
         # Add our test value
-        key1 = store.set(value)
+        key1 = store.put(value)
 
         # Test caching
         assert not store.is_cached(key1)
+        # Cache exists is false but this is still true
+        assert store.exists(key1)
         assert store.get(key1) == value
         assert store.is_cached(key1)
+        # Cache exists is true shortcut
+        assert store.exists(key1)
 
         # Add second value
-        key2 = store.set(value)
+        key2 = store.put(value)
         assert store.is_cached(key1)
         assert not store.is_cached(key2)
 
         # Check cached value flipped since cache size is 1
         assert store.get(key2) == value
         assert not store.is_cached(key1)
         assert store.is_cached(key2)
@@ -93,38 +98,42 @@
     store_implementation: StoreFixtureType,
 ) -> None:
     """Test store custom serialization."""
     store, store_info = store_implementation
 
     # Pretend serialized string
     s = b'ABC'
-    key = store.set(s, serializer=lambda s: s)
+    key = store.put(s, serializer=lambda s: s)
     assert store.get(key, deserializer=lambda s: s) == s
 
     with pytest.raises(TypeError, match='bytes'):
         # Should fail because the array is not already serialized
-        store.set([1, 2, 3], serializer=lambda s: s)
+        store.put([1, 2, 3], serializer=lambda s: s)
+
+    with pytest.raises(TypeError, match='bytes'):
+        # Should fail because the array is not already serialized
+        store.put_batch([[1, 2, 3]], serializer=lambda s: s)
 
 
 def test_store_batch_ops(store_implementation: StoreFixtureType) -> None:
     """Test batch operations."""
     store, store_info = store_implementation
 
     values = ['test_value1', 'test_value2', 'test_value3']
 
     # Test without keys
-    keys = store.set_batch(values)
+    keys = store.put_batch(values)
     for key in keys:
         assert store.exists(key)
 
 
 def test_store_batch_ops_remote(
     store_implementation: StoreFixtureType,
 ) -> None:
     """Test batch operations with custom serialization."""
     store, store_info = store_implementation
 
     values = ['test_value1', 'test_value2', 'test_value3']
 
-    new_keys = store.set_batch(values, serializer=lambda s: str.encode(s))
+    new_keys = store.put_batch(values, serializer=lambda s: str.encode(s))
     for key in new_keys:
         assert store.exists(key)
```

### Comparing `proxystore-0.4.1a1/tests/store/store_proxy_test.py` & `proxystore-0.5.0/tests/store/store_proxy_test.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,23 @@
 """Store Factory and Proxy Tests for Store Subclasses."""
 from __future__ import annotations
 
-from typing import NamedTuple
+from typing import Any
 
 import pytest
 
 from proxystore.proxy import Proxy
 from proxystore.proxy import ProxyLocker
 from proxystore.serialize import deserialize
 from proxystore.serialize import serialize
 from proxystore.store import get_store
 from proxystore.store import register_store
 from proxystore.store import unregister_store
 from proxystore.store.base import StoreFactory
 from proxystore.store.exceptions import ProxyResolveMissingKeyError
-from proxystore.store.local import LocalStore
 from proxystore.store.utils import get_key
 from testing.stores import StoreFixtureType
 
 
 def test_store_factory(store_implementation: StoreFixtureType) -> None:
     """Test Store Factory."""
     _, store_info = store_implementation
@@ -26,102 +25,108 @@
     store = store_info.type(
         store_info.name,
         cache_size=16,
         **store_info.kwargs,
     )
     register_store(store)
 
-    key = store.set([1, 2, 3])
+    key = store.put([1, 2, 3])
 
     # Clear store to see if factory can reinitialize it
     unregister_store(store_info.name)
 
-    f: StoreFactory[NamedTuple, list[int]] = StoreFactory(
+    f: StoreFactory[Any, list[int]] = StoreFactory(
         key,
-        store_info.type,
-        store_info.name,
-        store_kwargs=store_info.kwargs,
+        store_config=store.config(),
     )
     assert f() == [1, 2, 3]
 
-    f2: StoreFactory[NamedTuple, list[int]] = StoreFactory(
+    f2: StoreFactory[Any, list[int]] = StoreFactory(
         key,
-        store_info.type,
-        store_info.name,
-        store_kwargs=store_info.kwargs,
+        store_config=store.config(),
         evict=True,
     )
     assert store.exists(key)
     assert f2() == [1, 2, 3]
     assert not store.exists(key)
 
-    key = store.set([1, 2, 3])
+    key = store.put([1, 2, 3])
     # Clear store to see if factory can reinitialize it
     unregister_store(store_info.name)
 
     f = StoreFactory(
         key,
-        store_info.type,
-        store_info.name,
-        store_kwargs=store_info.kwargs,
+        store_config=store.config(),
     )
     f.resolve_async()
     assert f._obj_future is not None
     assert f() == [1, 2, 3]
     assert f._obj_future is None
 
-    # Calling resolve_async should be no-op since value cached
-    f.resolve_async()
-    assert f._obj_future is None
-    assert f() == [1, 2, 3]
-
+    # Check factory serialization
     f_str = serialize(f)
     f = deserialize(f_str)
     assert f() == [1, 2, 3]
 
-    class _MyStore(LocalStore):
-        pass
+    unregister_store(store_info.name)
 
-    # Test raise error if store_name corresponds to store that does not
-    # match the type specified in the StoreFactory
-    f = StoreFactory(
+
+def test_factory_serialization(store_implementation: StoreFixtureType) -> None:
+    store, store_info = store_implementation
+
+    register_store(store)
+
+    key = store.put([1, 2, 3])
+    f1: StoreFactory[Any, list[int]] = StoreFactory(
         key,
-        _MyStore,
-        store_info.name,
-        store_kwargs=store_info.kwargs,
+        store_config=store.config(),
     )
-    with pytest.raises(ValueError, match='store of type'):
-        f()
+    f1_bytes = serialize(f1)
+    f2 = deserialize(f1_bytes)
+    assert f1() == f2() == [1, 2, 3]
 
-    unregister_store(store_info.name)
+    # Check serialize after async resolve
+    f3: StoreFactory[Any, list[int]] = StoreFactory(
+        key,
+        store_config=store.config(),
+    )
+    f3.resolve_async()
+    f3_bytes = serialize(f3)
+    f4 = deserialize(f3_bytes)
+    assert f3() == f4() == [1, 2, 3]
+
+    unregister_store(store)
 
 
 def test_store_proxy(store_implementation: StoreFixtureType) -> None:
     """Test Store Proxy."""
     store, store_info = store_implementation
 
     register_store(store)
 
     p: Proxy[list[int]] = store.proxy([1, 2, 3])
     assert isinstance(p, Proxy)
 
     # Check that we can get the associated store back
     s = get_store(p)
-    assert s is not None and s.name == store.name
+    assert s is not None
+    assert s.name == store.name
 
     assert p == [1, 2, 3]
     key = get_key(p)
-    assert key is not None and store.get(key) == [1, 2, 3]
+    assert key is not None
+    assert store.get(key) == [1, 2, 3]
 
     p = store.proxy_from_key(key)
     assert p == [1, 2, 3]
 
     p = store.proxy([2, 3, 4])
     key = get_key(p)
-    assert key is not None and store.get(key) == [2, 3, 4]
+    assert key is not None
+    assert store.get(key) == [2, 3, 4]
 
     with pytest.raises(TypeError):
         # String will not be serialized and should raise error when putting
         # array into Redis
         store.proxy('mystring', serializer=lambda s: s)
 
     assert isinstance(store.locked_proxy([1, 2, 3]), ProxyLocker)
@@ -144,16 +149,17 @@
 
     # Resolve the proxy
     assert p == [1, 2, 3]
 
     # The store that created the proxy had cache_size=0 so the restored
     # store should also have cache_size=0.
     s = get_store(store_info.name)
-    assert store._cache.maxsize == 0
-    assert s is not None and not s.is_cached(key)
+    assert store.cache.maxsize == 0
+    assert s is not None
+    assert not s.is_cached(key)
 
     unregister_store(store_info.name)
 
 
 def test_proxy_batch(store_implementation: StoreFixtureType) -> None:
     """Test Batch Creation of Proxies."""
     store, store_info = store_implementation
```

### Comparing `proxystore-0.4.1a1/tests/store/utils_test.py` & `proxystore-0.5.0/tests/store/utils_test.py`

 * *Files 11% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 from proxystore.store.local import LocalStore
 from proxystore.store.utils import get_key
 from proxystore.store.utils import resolve_async
 
 
 def test_get_key_from_proxy() -> None:
     with LocalStore('store') as store:
-        key = store.set('value')
+        key = store.put('value')
         proxy: Proxy[str] = store.proxy_from_key(key)
 
         assert get_key(proxy) == key
 
 
 def test_get_key_from_proxy_not_created_by_store() -> None:
     p = Proxy(SimpleFactory('value'))
```

### Comparing `proxystore-0.4.1a1/tests/utils_test.py` & `proxystore-0.5.0/tests/utils_test.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,52 +1,68 @@
 """Utils Unit Tests."""
 from __future__ import annotations
 
 import os
+from typing import Any
 from unittest import mock
 
 import pytest
 
-from proxystore import utils
-from proxystore.factory import SimpleFactory
+from proxystore.connectors.file import FileConnector
+from proxystore.connectors.local import LocalConnector
 from proxystore.utils import bytes_to_readable
 from proxystore.utils import chunk_bytes
+from proxystore.utils import get_class_path
 from proxystore.utils import home_dir
+from proxystore.utils import import_class
 from proxystore.utils import readable_to_bytes
 
 
 @pytest.mark.parametrize(
-    'data_size,chunk_size',
+    ('data_size', 'chunk_size'),
     ((100, 1), (1000, 100), (1000, 128)),
 )
 def test_chunk_bytes(data_size: int, chunk_size: int) -> None:
     data = os.urandom(data_size)
     result = bytearray()
     for chunk in chunk_bytes(data, chunk_size):
         result += chunk
     assert data == result
 
 
-def test_create_key() -> None:
-    """Test create_key()."""
-    assert isinstance(utils.create_key(42), str)
+@pytest.mark.parametrize(
+    ('cls', 'expected'),
+    (
+        (FileConnector, 'proxystore.connectors.file.FileConnector'),
+        (LocalConnector, 'proxystore.connectors.local.LocalConnector'),
+    ),
+)
+def test_get_class_path(cls: type[Any], expected: str) -> None:
+    assert get_class_path(cls) == expected
+
+
+@pytest.mark.parametrize(
+    ('path', 'expected'),
+    (
+        ('proxystore.connectors.file.FileConnector', FileConnector),
+        ('proxystore.connectors.local.LocalConnector', LocalConnector),
+        ('typing.Any', Any),
+    ),
+)
+def test_import_class(path: str, expected: type[Any]) -> None:
+    assert import_class(path) == expected
 
 
-def test_fullname() -> None:
-    """Test fullname()."""
-    assert utils.fullname(SimpleFactory) == 'proxystore.factory.SimpleFactory'
-    assert (
-        utils.fullname(SimpleFactory('string'))
-        == 'proxystore.factory.SimpleFactory'
-    )
-    assert utils.fullname('string') == 'str'
+def test_import_class_missing_path() -> None:
+    with pytest.raises(ImportError):
+        import_class('FileConnector')
 
 
 @pytest.mark.parametrize(
-    'env,expected',
+    ('env', 'expected'),
     (
         ({}, '~/.local/share/proxystore'),
         ({'PROXYSTORE_HOME': '/path/to/home'}, '/path/to/home'),
         ({'XDG_DATA_HOME': '/path/to/home'}, '/path/to/home/proxystore'),
         ({'PROXYSTORE_HOME': '/home1', 'XDG_DATA_HOME': '/home2'}, '/home1'),
     ),
 )
@@ -62,15 +78,15 @@
 
     # Exclude from coverage because not every OS will set $XDG_DATA_HOME
     if xdg_data_home is not None:  # pragma: no cover
         os.environ['XDG_DATA_HOME'] = xdg_data_home
 
 
 @pytest.mark.parametrize(
-    'value,precision,expected',
+    ('value', 'precision', 'expected'),
     (
         (0, 3, '0 B'),
         (1, 3, '1 B'),
         (int(1e3), 3, '1 KB'),
         (int(1e6), 3, '1 MB'),
         (int(1e9), 3, '1 GB'),
         (int(1e12), 3, '1 TB'),
@@ -88,15 +104,15 @@
 
 def test_bytes_to_readable_exceptions() -> None:
     with pytest.raises(ValueError, match='negative'):
         bytes_to_readable(-1)
 
 
 @pytest.mark.parametrize(
-    'value,expected',
+    ('value', 'expected'),
     (
         ('0 B', 0),
         ('1 B', 1),
         ('1 KB', int(1e3)),
         ('1 MB', int(1e6)),
         ('1 GB', int(1e9)),
         ('1 TB', int(1e12)),
```

### Comparing `proxystore-0.4.1a1/tox.ini` & `proxystore-0.5.0/tox.ini`

 * *Files 22% similar despite different names*

```diff
@@ -1,31 +1,34 @@
 [tox]
 envlist = py{37,38,39,310,311},py{37,38,39,310,311}-dim, pre-commit, docs
 
 [testenv]
-extras = dev,endpoints
+extras = dev,endpoints,redis,zmq
 commands =
     coverage erase
     coverage run -m pytest {posargs}
     coverage combine --quiet
     coverage report
 
 [testenv:py{37,38,39,310,311}-dim]
+allowlist_externals =
+    bash
+    timeout
 deps =
     pkgconfig
     pybind11
-    git+https://github.com/rapidsai/ucx-py.git
+    git+https://github.com/rapidsai/ucx-py.git@v0.30.00
 commands_pre =
-    python -m pip install git+https://github.com/mochi-hpc/py-mochi-margo.git
+    python -m pip install git+https://github.com/mochi-hpc/py-mochi-margo.git@v0.5.2
 commands =
-    pytest -k "margo or ucx" {posargs}
+    pytest -k margo {posargs}
+    # UCX is unreliable and will hang in CI
+    bash -c "timeout 60 pytest -k ucx {posargs} || true"
 
 [testenv:pre-commit]
 skip_install = true
 deps = pre-commit
 commands = pre-commit run --all-files --show-diff-on-failure
 
 [testenv:docs]
-extras = endpoints
-changedir = docs
-deps = -rdocs/requirements.txt
-commands = sphinx-build -W -E -b html . _build/html
+extras = docs
+commands = mkdocs build --strict
```

