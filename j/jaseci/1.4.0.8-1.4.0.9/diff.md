# Comparing `tmp/jaseci-1.4.0.8.tar.gz` & `tmp/jaseci-1.4.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jaseci-1.4.0.8.tar", last modified: Wed Feb  8 14:13:32 2023, max compression
+gzip compressed data, was "jaseci-1.4.0.9.tar", last modified: Tue Feb 14 17:26:22 2023, max compression
```

## Comparing `jaseci-1.4.0.8.tar` & `jaseci-1.4.0.9.tar`

### file list

```diff
@@ -1,224 +1,231 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      173 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.141268 jaseci-1.4.0.8/jaseci/
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)     1032 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.145268 jaseci-1.4.0.8/jaseci/actions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9361 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/live_actions.py
--rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/remote_actions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.145268 jaseci-1.4.0.8/jaseci/actions/standard/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1881 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/date.py
--rw-r--r--   0 runner    (1001) docker     (123)     1714 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/elastic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/file.py
--rw-r--r--   0 runner    (1001) docker     (123)      431 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/internal.py
--rw-r--r--   0 runner    (1001) docker     (123)     1701 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/jaseci.py
--rw-r--r--   0 runner    (1001) docker     (123)      279 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/mail.py
--rw-r--r--   0 runner    (1001) docker     (123)     7166 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/net.py
--rw-r--r--   0 runner    (1001) docker     (123)     2121 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/rand.py
--rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5653 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/std.py
--rw-r--r--   0 runner    (1001) docker     (123)      356 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/task.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.145268 jaseci-1.4.0.8/jaseci/actions/standard/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1460 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_file_lib.py
--rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_mail_lib.py
--rw-r--r--   0 runner    (1001) docker     (123)     2215 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_net_lib.py
--rw-r--r--   0 runner    (1001) docker     (123)     1204 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_std_lib.py
--rw-r--r--   0 runner    (1001) docker     (123)     1050 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_url.py
--rw-r--r--   0 runner    (1001) docker     (123)     1285 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_vector.py
--rw-r--r--   0 runner    (1001) docker     (123)      971 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_webtool.py
--rw-r--r--   0 runner    (1001) docker     (123)      834 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/tests/test_zlib.py
--rw-r--r--   0 runner    (1001) docker     (123)     1855 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/url.py
--rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/vector.py
--rw-r--r--   0 runner    (1001) docker     (123)      724 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/webtool.py
--rw-r--r--   0 runner    (1001) docker     (123)      894 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/standard/zlib.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.145268 jaseci-1.4.0.8/jaseci/actions/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      782 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/tests/std_test_code.py
--rw-r--r--   0 runner    (1001) docker     (123)     1740 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/tests/test_actions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1792 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actions/tests/test_std.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.145268 jaseci-1.4.0.8/jaseci/actor/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2215 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actor/architype.py
--rw-r--r--   0 runner    (1001) docker     (123)     9304 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actor/sentinel.py
--rw-r--r--   0 runner    (1001) docker     (123)     8299 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/actor/walker.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.149268 jaseci-1.4.0.8/jaseci/api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6584 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/actions_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     5150 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/alias_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     7232 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/architype_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2406 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/config_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/global_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     5069 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/graph_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     9591 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/interface.py
--rw-r--r--   0 runner    (1001) docker     (123)     5835 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/jac_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    10609 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/jsorc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2798 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/logger_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     4135 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/master_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/object_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1487 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/prometheus_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      991 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/queue_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     9626 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/sentinel_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1960 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/super_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.149268 jaseci-1.4.0.8/jaseci/api/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_architype_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     6776 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_global_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2304 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_graph_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1476 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_logger_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_sentinel_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_user_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    11782 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/tests/test_walker_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     5397 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/user_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     8732 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/api/walker_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.149268 jaseci-1.4.0.8/jaseci/attr/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/attr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3311 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/attr/action.py
--rw-r--r--   0 runner    (1001) docker     (123)      613 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/attr/item.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.149268 jaseci-1.4.0.8/jaseci/element/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/element/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7664 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/element/element.py
--rw-r--r--   0 runner    (1001) docker     (123)     1618 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/element/master.py
--rw-r--r--   0 runner    (1001) docker     (123)     7167 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/element/obj_mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)      733 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/element/super_master.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.149268 jaseci-1.4.0.8/jaseci/graph/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/graph/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5030 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/graph/edge.py
--rw-r--r--   0 runner    (1001) docker     (123)      597 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/graph/graph.py
--rw-r--r--   0 runner    (1001) docker     (123)    17719 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/graph/node.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/hook/
--rw-r--r--   0 runner    (1001) docker     (123)      117 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/hook/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7209 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/hook/memory.py
--rw-r--r--   0 runner    (1001) docker     (123)     4325 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/hook/redis.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/interpreter/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5932 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/architype_interp.py
--rw-r--r--   0 runner    (1001) docker     (123)    70340 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/interp.py
--rw-r--r--   0 runner    (1001) docker     (123)     7164 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/sentinel_interp.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/interpreter/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/tests/test_interp.py
--rw-r--r--   0 runner    (1001) docker     (123)     9115 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/interpreter/walker_interp.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/ir/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/ast.py
--rw-r--r--   0 runner    (1001) docker     (123)     8399 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/ast_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/jac_code.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/ir/passes/
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      331 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/ast_prune_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)     9375 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/codegen_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)      560 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/ir_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)      822 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/printer_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)      811 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/pt_prune_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)      616 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/schedule.py
--rw-r--r--   0 runner    (1001) docker     (123)      468 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/ir/passes/stats_pass.py
--rw-r--r--   0 runner    (1001) docker     (123)     8925 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac.g4
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/jac_parse/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac_parse/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    34691 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac_parse/jacLexer.py
--rw-r--r--   0 runner    (1001) docker     (123)    29061 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac_parse/jacListener.py
--rw-r--r--   0 runner    (1001) docker     (123)   333597 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac_parse/jacParser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3360 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jac_set.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.153268 jaseci-1.4.0.8/jaseci/jac/jsci_vm/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3613 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/disasm.py
--rw-r--r--   0 runner    (1001) docker     (123)      768 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/inst_ptr.py
--rw-r--r--   0 runner    (1001) docker     (123)     5701 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/machine.py
--rw-r--r--   0 runner    (1001) docker     (123)     1781 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/op_codes.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/jac/jsci_vm/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1116 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/jsci_vm/tests/test_codegen.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/jac/machine/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/machine/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3273 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/machine/jac_scope.py
--rw-r--r--   0 runner    (1001) docker     (123)     6614 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/machine/jac_value.py
--rw-r--r--   0 runner    (1001) docker     (123)     9171 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/machine/machine_state.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/jac/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13323 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/tests/book_code.py
--rw-r--r--   0 runner    (1001) docker     (123)    13884 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/tests/test_book.py
--rw-r--r--   0 runner    (1001) docker     (123)     1488 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jac/tests/test_lang_14.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/jsctl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jsctl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16114 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jsctl/book_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)    12246 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jsctl/jsctl.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/jsctl/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jsctl/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20339 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/jsctl/tests/test_jsctl.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/actions_optimizer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/actions_optimizer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21169 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/actions_optimizer/actions_optimizer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2963 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/actions_optimizer/actions_state.py
--rw-r--r--   0 runner    (1001) docker     (123)    27118 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/common.py
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/elastic/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/elastic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/elastic/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/elastic/elastic.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/elastic/manifest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/
--rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      928 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/jaseci-redis.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6336 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/jsorc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/promon/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/promon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6892 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/jsorc-backup/promon/promon.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/mail/
--rw-r--r--   0 runner    (1001) docker     (123)      126 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/mail/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      875 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/mail/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4697 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/mail/mail.py
--rw-r--r--   0 runner    (1001) docker     (123)     5233 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/meta.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.157268 jaseci-1.4.0.8/jaseci/svc/postgres/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/postgres/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4322 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/postgres/manifest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/jaseci/svc/prometheus/
--rwxr-xr-x   0 runner    (1001) docker     (123)       82 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/prometheus/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/prometheus/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    53949 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/prometheus/manifest.py
--rw-r--r--   0 runner    (1001) docker     (123)     9888 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/prometheus/prometheus.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/jaseci/svc/redis/
--rw-r--r--   0 runner    (1001) docker     (123)       72 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/redis/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      215 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/redis/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/redis/manifest.py
--rw-r--r--   0 runner    (1001) docker     (123)     2071 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/redis/redis.py
--rw-r--r--   0 runner    (1001) docker     (123)      332 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/state.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/jaseci/svc/task/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/task/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10655 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/task/common.py
--rw-r--r--   0 runner    (1001) docker     (123)      440 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/task/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3876 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/svc/task/task.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/jaseci/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      900 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/infer.py
--rw-r--r--   0 runner    (1001) docker     (123)    25194 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/jac_test_code.py
--rw-r--r--   0 runner    (1001) docker     (123)    13249 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/jac_test_progs.py
--rw-r--r--   0 runner    (1001) docker     (123)     6121 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/test_core.py
--rw-r--r--   0 runner    (1001) docker     (123)    32292 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/test_jac.py
--rw-r--r--   0 runner    (1001) docker     (123)     4009 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/test_node.py
--rw-r--r--   0 runner    (1001) docker     (123)    22073 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/test_progs.py
--rw-r--r--   0 runner    (1001) docker     (123)     7587 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/tests/test_stack.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/jaseci/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5328 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/id_list.py
--rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/json_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/log_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1197 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/test_core.py
--rw-r--r--   0 runner    (1001) docker     (123)     7745 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/jaseci/utils/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.141268 jaseci-1.4.0.8/jaseci.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      173 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5547 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      352 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-02-08 14:13:32.000000 jaseci-1.4.0.8/jaseci.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-08 14:13:32.161268 jaseci-1.4.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1274 2023-02-08 14:13:11.000000 jaseci-1.4.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.104182 jaseci-1.4.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      173 2023-02-14 17:26:22.104182 jaseci-1.4.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.080181 jaseci-1.4.0.9/jaseci/
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)     1082 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.080181 jaseci-1.4.0.9/jaseci/actions/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9361 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/live_actions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/remote_actions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.084181 jaseci-1.4.0.9/jaseci/actions/standard/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1881 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/date.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1714 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/elastic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)      431 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/internal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1701 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/jaseci.py
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/mail.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7166 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/net.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2121 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/rand.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5653 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/std.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7497 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/stripe.py
+-rw-r--r--   0 runner    (1001) docker     (123)      356 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/task.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.084181 jaseci-1.4.0.9/jaseci/actions/standard/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1460 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_file_lib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_mail_lib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2215 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_net_lib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1204 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_std_lib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1050 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1285 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_vector.py
+-rw-r--r--   0 runner    (1001) docker     (123)      971 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_webtool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/tests/test_zlib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1855 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/vector.py
+-rw-r--r--   0 runner    (1001) docker     (123)      724 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/webtool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      894 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/standard/zlib.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.084181 jaseci-1.4.0.9/jaseci/actions/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      782 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/tests/std_test_code.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1740 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/tests/test_actions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1792 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actions/tests/test_std.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.084181 jaseci-1.4.0.9/jaseci/actor/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2215 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actor/architype.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9304 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actor/sentinel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8299 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/actor/walker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.088181 jaseci-1.4.0.9/jaseci/api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6584 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/actions_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5150 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/alias_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7232 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/architype_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2435 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/config_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/global_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5069 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/graph_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9591 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5835 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/jac_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10609 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/jsorc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2798 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/logger_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4135 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/master_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/object_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1487 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/prometheus_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      991 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/queue_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9626 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/sentinel_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1994 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/super_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.088181 jaseci-1.4.0.9/jaseci/api/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_architype_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6776 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_global_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2304 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_graph_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1476 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_logger_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_sentinel_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_user_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11782 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/tests/test_walker_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5397 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/user_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8732 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/walker_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1861 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/api/webhook_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.088181 jaseci-1.4.0.9/jaseci/attr/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/attr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3311 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/attr/action.py
+-rw-r--r--   0 runner    (1001) docker     (123)      613 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/attr/item.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/element/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/element/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7664 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/element/element.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1680 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/element/master.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7167 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/element/obj_mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)      733 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/element/super_master.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/graph/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/graph/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5030 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/graph/edge.py
+-rw-r--r--   0 runner    (1001) docker     (123)      597 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/graph/graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17719 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/graph/node.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/hook/
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/hook/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7209 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/hook/memory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4325 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/hook/redis.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/jac/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/jac/interpreter/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5932 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/architype_interp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    70340 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/interp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7164 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/sentinel_interp.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/jac/interpreter/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/tests/test_interp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9115 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/interpreter/walker_interp.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/jac/ir/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/ast.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8399 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/ast_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/jac_code.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.092181 jaseci-1.4.0.9/jaseci/jac/ir/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      331 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/ast_prune_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9375 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/codegen_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)      560 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/ir_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)      822 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/printer_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)      811 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/pt_prune_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/schedule.py
+-rw-r--r--   0 runner    (1001) docker     (123)      468 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/ir/passes/stats_pass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8925 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac.g4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jac/jac_parse/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac_parse/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    34691 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac_parse/jacLexer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29061 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac_parse/jacListener.py
+-rw-r--r--   0 runner    (1001) docker     (123)   333597 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac_parse/jacParser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3360 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jac_set.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jac/jsci_vm/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3613 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/disasm.py
+-rw-r--r--   0 runner    (1001) docker     (123)      768 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/inst_ptr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5701 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/machine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1781 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/op_codes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jac/jsci_vm/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1116 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/jsci_vm/tests/test_codegen.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jac/machine/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/machine/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3273 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/machine/jac_scope.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6614 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/machine/jac_value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9171 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/machine/machine_state.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jac/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13323 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/tests/book_code.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13884 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/tests/test_book.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1488 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jac/tests/test_lang_14.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jsctl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jsctl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16114 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jsctl/book_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12246 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jsctl/jsctl.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/jsctl/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jsctl/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20339 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/jsctl/tests/test_jsctl.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.096181 jaseci-1.4.0.9/jaseci/svc/
+-rw-r--r--   0 runner    (1001) docker     (123)      636 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/actions_optimizer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/actions_optimizer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21169 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/actions_optimizer/actions_optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2963 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/actions_optimizer/actions_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27118 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/elastic/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/elastic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/elastic/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/elastic/elastic.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/elastic/manifest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/
+-rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      928 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/jaseci-redis.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     6336 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/jsorc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/promon/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/promon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6892 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/jsorc-backup/promon/promon.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/mail/
+-rw-r--r--   0 runner    (1001) docker     (123)      126 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/mail/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      875 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/mail/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4697 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/mail/mail.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5397 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/meta.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/postgres/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/postgres/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4322 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/postgres/manifest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/prometheus/
+-rwxr-xr-x   0 runner    (1001) docker     (123)       82 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/prometheus/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/prometheus/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    53949 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/prometheus/manifest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9888 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/prometheus/prometheus.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/redis/
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/redis/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      215 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/redis/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/redis/manifest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2071 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/redis/redis.py
+-rw-r--r--   0 runner    (1001) docker     (123)      332 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/state.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/stripe/
+-rw-r--r--   0 runner    (1001) docker     (123)       66 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/stripe/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/stripe/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1943 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/stripe/stripe.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.100181 jaseci-1.4.0.9/jaseci/svc/task/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/task/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10655 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/task/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)      440 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/task/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3876 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/svc/task/task.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.104182 jaseci-1.4.0.9/jaseci/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      900 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/infer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25194 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/jac_test_code.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13249 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/jac_test_progs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6121 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_core.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32292 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_jac.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4009 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22073 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_progs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7587 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_stack.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8224 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/tests/test_stripe.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.104182 jaseci-1.4.0.9/jaseci/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5328 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/id_list.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/json_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/log_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1197 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/test_core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7745 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/jaseci/utils/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:22.080181 jaseci-1.4.0.9/jaseci.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      173 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5721 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      352 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-02-14 17:26:22.000000 jaseci-1.4.0.9/jaseci.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-14 17:26:22.104182 jaseci-1.4.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1274 2023-02-14 17:25:56.000000 jaseci-1.4.0.9/setup.py
```

### Comparing `jaseci-1.4.0.8/LICENSE` & `jaseci-1.4.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/__init__.py` & `jaseci-1.4.0.9/jaseci/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,10 +23,11 @@
     import jaseci.actions.standard.mail  # noqa
     import jaseci.actions.standard.task  # noqa
     import jaseci.actions.standard.internal  # noqa
     import jaseci.actions.standard.zlib  # noqa
     import jaseci.actions.standard.webtool  # noqa
     import jaseci.actions.standard.elastic  # noqa
     import jaseci.actions.standard.url  # noqa
+    import jaseci.actions.standard.stripe  # noqa
 
 
 load_standard()
```

### Comparing `jaseci-1.4.0.8/jaseci/actions/live_actions.py` & `jaseci-1.4.0.9/jaseci/actions/live_actions.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/remote_actions.py` & `jaseci-1.4.0.9/jaseci/actions/remote_actions.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/date.py` & `jaseci-1.4.0.9/jaseci/actions/standard/date.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/elastic.py` & `jaseci-1.4.0.9/jaseci/actions/standard/elastic.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/file.py` & `jaseci-1.4.0.9/jaseci/actions/standard/file.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/jaseci.py` & `jaseci-1.4.0.9/jaseci/actions/standard/jaseci.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/net.py` & `jaseci-1.4.0.9/jaseci/actions/standard/net.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/rand.py` & `jaseci-1.4.0.9/jaseci/actions/standard/rand.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/request.py` & `jaseci-1.4.0.9/jaseci/actions/standard/request.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/std.py` & `jaseci-1.4.0.9/jaseci/actions/standard/std.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_file_lib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_file_lib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_mail_lib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_mail_lib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_net_lib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_net_lib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_std_lib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_std_lib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_url.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_url.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_vector.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_vector.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_webtool.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_webtool.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/tests/test_zlib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/tests/test_zlib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/url.py` & `jaseci-1.4.0.9/jaseci/actions/standard/url.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/vector.py` & `jaseci-1.4.0.9/jaseci/actions/standard/vector.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/webtool.py` & `jaseci-1.4.0.9/jaseci/actions/standard/webtool.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/standard/zlib.py` & `jaseci-1.4.0.9/jaseci/actions/standard/zlib.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/tests/std_test_code.py` & `jaseci-1.4.0.9/jaseci/actions/tests/std_test_code.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/tests/test_actions.py` & `jaseci-1.4.0.9/jaseci/actions/tests/test_actions.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actions/tests/test_std.py` & `jaseci-1.4.0.9/jaseci/actions/tests/test_std.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actor/architype.py` & `jaseci-1.4.0.9/jaseci/actor/architype.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actor/sentinel.py` & `jaseci-1.4.0.9/jaseci/actor/sentinel.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/actor/walker.py` & `jaseci-1.4.0.9/jaseci/actor/walker.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/actions_api.py` & `jaseci-1.4.0.9/jaseci/api/actions_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/alias_api.py` & `jaseci-1.4.0.9/jaseci/api/alias_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/architype_api.py` & `jaseci-1.4.0.9/jaseci/api/architype_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/config_api.py` & `jaseci-1.4.0.9/jaseci/api/config_api.py`

 * *Files 3% similar despite different names*

```diff
@@ -18,14 +18,15 @@
             "CONFIG_EXAMPLE",
             "ACTION_SETS",
             "REDIS_CONFIG",
             "TASK_CONFIG",
             "MAIL_CONFIG",
             "PROMON_CONFIG",
             "ELASTIC_CONFIG",
+            "STRIPE_CONFIG",
             "META_CONFIG",
         ]
 
     @Interface.admin_api(cli_args=["name"])
     def config_get(self, name: str, do_check: bool = True):
         """
         Get a config
```

### Comparing `jaseci-1.4.0.8/jaseci/api/global_api.py` & `jaseci-1.4.0.9/jaseci/api/global_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/graph_api.py` & `jaseci-1.4.0.9/jaseci/api/graph_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/interface.py` & `jaseci-1.4.0.9/jaseci/api/interface.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/jac_api.py` & `jaseci-1.4.0.9/jaseci/api/jac_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/jsorc_api.py` & `jaseci-1.4.0.9/jaseci/api/jsorc_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/logger_api.py` & `jaseci-1.4.0.9/jaseci/api/logger_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/master_api.py` & `jaseci-1.4.0.9/jaseci/api/master_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/object_api.py` & `jaseci-1.4.0.9/jaseci/api/object_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/prometheus_api.py` & `jaseci-1.4.0.9/jaseci/api/prometheus_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/queue_api.py` & `jaseci-1.4.0.9/jaseci/api/queue_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/sentinel_api.py` & `jaseci-1.4.0.9/jaseci/api/sentinel_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/super_api.py` & `jaseci-1.4.0.9/jaseci/api/super_api.py`

 * *Files 4% similar despite different names*

```diff
@@ -33,15 +33,17 @@
                 mast, global_init, global_init_ctx
             )
         self.take_ownership(mast)
         ret["success"] = True
         return ret
 
     @Interface.admin_api()
-    def master_allusers(self, limit: int = 0, offset: int = 0, asc: bool = False):
+    def master_allusers(
+        self, limit: int = 0, offset: int = 0, asc: bool = False, search: str = None
+    ):
         """
         Returns info on a set of users, limit specifies the number of users to
         return and offset specfies where to start
         NOTE: Abstract interface to be overridden
         """
 
     @Interface.admin_api(cli_args=["mast"])
```

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_architype_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_architype_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_global_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_global_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_graph_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_graph_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_logger_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_logger_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_sentinel_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_sentinel_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_user_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_user_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/tests/test_walker_api.py` & `jaseci-1.4.0.9/jaseci/api/tests/test_walker_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/user_api.py` & `jaseci-1.4.0.9/jaseci/api/user_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/api/walker_api.py` & `jaseci-1.4.0.9/jaseci/api/walker_api.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/attr/action.py` & `jaseci-1.4.0.9/jaseci/attr/action.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/attr/item.py` & `jaseci-1.4.0.9/jaseci/attr/item.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/element/element.py` & `jaseci-1.4.0.9/jaseci/element/element.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/element/master.py` & `jaseci-1.4.0.9/jaseci/element/master.py`

 * *Files 10% similar despite different names*

```diff
@@ -12,14 +12,15 @@
 from jaseci.api.architype_api import ArchitypeApi
 from jaseci.api.config_api import ConfigApi
 from jaseci.api.interface import Interface
 from jaseci.api.master_api import MasterApi
 from jaseci.api.jac_api import JacApi
 from jaseci.api.user_api import UserApi
 from jaseci.api.queue_api import QueueApi
+from jaseci.api.webhook_api import WebhookApi
 
 
 class Master(
     Element,
     Interface,
     MasterApi,
     AliasAPI,
@@ -27,14 +28,15 @@
     ObjectApi,
     SentinelApi,
     WalkerApi,
     ArchitypeApi,
     JacApi,
     UserApi,
     QueueApi,
+    WebhookApi,
 ):
     """Main class for master functions for user"""
 
     def __init__(self, head_master=None, *args, **kwargs):
         kwargs["m_id"] = None
 
         Element.__init__(self, kind="Jaseci Master", *args, **kwargs)
```

### Comparing `jaseci-1.4.0.8/jaseci/element/obj_mixins.py` & `jaseci-1.4.0.9/jaseci/element/obj_mixins.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/element/super_master.py` & `jaseci-1.4.0.9/jaseci/element/super_master.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/graph/edge.py` & `jaseci-1.4.0.9/jaseci/graph/edge.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/graph/graph.py` & `jaseci-1.4.0.9/jaseci/graph/graph.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/graph/node.py` & `jaseci-1.4.0.9/jaseci/graph/node.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/hook/memory.py` & `jaseci-1.4.0.9/jaseci/hook/memory.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/hook/redis.py` & `jaseci-1.4.0.9/jaseci/hook/redis.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/interpreter/architype_interp.py` & `jaseci-1.4.0.9/jaseci/jac/interpreter/architype_interp.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/interpreter/interp.py` & `jaseci-1.4.0.9/jaseci/jac/interpreter/interp.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/interpreter/sentinel_interp.py` & `jaseci-1.4.0.9/jaseci/jac/interpreter/sentinel_interp.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/interpreter/tests/test_interp.py` & `jaseci-1.4.0.9/jaseci/jac/interpreter/tests/test_interp.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/interpreter/walker_interp.py` & `jaseci-1.4.0.9/jaseci/jac/interpreter/walker_interp.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/ast.py` & `jaseci-1.4.0.9/jaseci/jac/ir/ast.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/ast_builder.py` & `jaseci-1.4.0.9/jaseci/jac/ir/ast_builder.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/jac_code.py` & `jaseci-1.4.0.9/jaseci/jac/ir/jac_code.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/passes/codegen_pass.py` & `jaseci-1.4.0.9/jaseci/jac/ir/passes/codegen_pass.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/passes/ir_pass.py` & `jaseci-1.4.0.9/jaseci/jac/ir/passes/ir_pass.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/passes/printer_pass.py` & `jaseci-1.4.0.9/jaseci/jac/ir/passes/printer_pass.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/passes/pt_prune_pass.py` & `jaseci-1.4.0.9/jaseci/jac/ir/passes/pt_prune_pass.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/ir/passes/schedule.py` & `jaseci-1.4.0.9/jaseci/jac/ir/passes/schedule.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jac.g4` & `jaseci-1.4.0.9/jaseci/jac/jac.g4`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jac_parse/jacLexer.py` & `jaseci-1.4.0.9/jaseci/jac/jac_parse/jacLexer.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jac_parse/jacListener.py` & `jaseci-1.4.0.9/jaseci/jac/jac_parse/jacListener.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jac_parse/jacParser.py` & `jaseci-1.4.0.9/jaseci/jac/jac_parse/jacParser.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jac_set.py` & `jaseci-1.4.0.9/jaseci/jac/jac_set.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jsci_vm/disasm.py` & `jaseci-1.4.0.9/jaseci/jac/jsci_vm/disasm.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jsci_vm/inst_ptr.py` & `jaseci-1.4.0.9/jaseci/jac/jsci_vm/inst_ptr.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jsci_vm/machine.py` & `jaseci-1.4.0.9/jaseci/jac/jsci_vm/machine.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jsci_vm/op_codes.py` & `jaseci-1.4.0.9/jaseci/jac/jsci_vm/op_codes.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/jsci_vm/tests/test_codegen.py` & `jaseci-1.4.0.9/jaseci/jac/jsci_vm/tests/test_codegen.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/machine/jac_scope.py` & `jaseci-1.4.0.9/jaseci/jac/machine/jac_scope.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/machine/jac_value.py` & `jaseci-1.4.0.9/jaseci/jac/machine/jac_value.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/machine/machine_state.py` & `jaseci-1.4.0.9/jaseci/jac/machine/machine_state.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/tests/book_code.py` & `jaseci-1.4.0.9/jaseci/jac/tests/book_code.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/tests/test_book.py` & `jaseci-1.4.0.9/jaseci/jac/tests/test_book.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jac/tests/test_lang_14.py` & `jaseci-1.4.0.9/jaseci/jac/tests/test_lang_14.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jsctl/book_tools.py` & `jaseci-1.4.0.9/jaseci/jsctl/book_tools.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jsctl/jsctl.py` & `jaseci-1.4.0.9/jaseci/jsctl/jsctl.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/jsctl/tests/test_jsctl.py` & `jaseci-1.4.0.9/jaseci/jsctl/tests/test_jsctl.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/__init__.py` & `jaseci-1.4.0.9/jaseci/svc/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,23 +1,25 @@
 from .state import ServiceState
 from .common import CommonService, ProxyService, JsOrc, MetaProperties, Kube
 from .redis import RedisService
 from .task import TaskService
+from .stripe import StripeService
 from .mail import MailService
 from .prometheus import PrometheusService
 from .elastic import ElasticService
 from .meta import MetaService
 
 __all__ = [
     "ServiceState",
     "JsOrc",
     "MetaProperties",
     "CommonService",
     "ProxyService",
     "RedisService",
     "TaskService",
+    "StripeService",
     "MailService",
     "PrometheusService",
     "ElasticService",
     "MetaService",
     "Kube",
 ]
```

### Comparing `jaseci-1.4.0.8/jaseci/svc/actions_optimizer/actions_optimizer.py` & `jaseci-1.4.0.9/jaseci/svc/actions_optimizer/actions_optimizer.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/actions_optimizer/actions_state.py` & `jaseci-1.4.0.9/jaseci/svc/actions_optimizer/actions_state.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/common.py` & `jaseci-1.4.0.9/jaseci/svc/common.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/elastic/elastic.py` & `jaseci-1.4.0.9/jaseci/svc/elastic/elastic.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/jsorc-backup/jaseci-redis.yaml` & `jaseci-1.4.0.9/jaseci/svc/jsorc-backup/jaseci-redis.yaml`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/jsorc-backup/jsorc.py` & `jaseci-1.4.0.9/jaseci/svc/jsorc-backup/jsorc.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/jsorc-backup/promon/promon.py` & `jaseci-1.4.0.9/jaseci/svc/jsorc-backup/promon/promon.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/mail/config.py` & `jaseci-1.4.0.9/jaseci/svc/mail/config.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/mail/mail.py` & `jaseci-1.4.0.9/jaseci/svc/mail/mail.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/meta.py` & `jaseci-1.4.0.9/jaseci/svc/meta.py`

 * *Files 9% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 from jaseci.svc import (
     CommonService,
     JsOrc,
     MetaProperties,
     MailService,
     RedisService,
     TaskService,
+    StripeService,
     PrometheusService,
     ElasticService,
     ServiceState as Ss,
 )
 
 
 class MetaService(CommonService, MetaProperties):
@@ -90,20 +91,22 @@
         h.meta = self
         if self.run_svcs:
             h.promon = self.get_service("promon", h)
             h.redis = self.get_service("redis", h)
             h.task = self.get_service("task", h)
             h.mail = self.get_service("mail", h)
             h.elastic = self.get_service("elastic", h)
+            h.stripe = self.get_service("stripe", h)
 
             if not self.is_automated():
                 h.mail.start(h)
                 h.redis.start(h)
                 h.task.start(h)
                 h.elastic.start(h)
+                h.stripe.start(h)
 
         return h
 
     def build_master(self, *args, **kwargs):
         return self.__common("master", *args, **kwargs)
 
     def build_super_master(self, *args, **kwargs):
@@ -136,14 +139,15 @@
 
     def populate_services(self):
         self.add_service_builder("redis", RedisService)
         self.add_service_builder("task", TaskService)
         self.add_service_builder("mail", MailService)
         self.add_service_builder("promon", PrometheusService)
         self.add_service_builder("elastic", ElasticService)
+        self.add_service_builder("stripe", StripeService)
 
 
 def interval_check(signum, frame):
     meta = MetaService()
     if meta.is_automated():
         meta.app.interval_check()
         logger.info(
```

### Comparing `jaseci-1.4.0.8/jaseci/svc/postgres/manifest.py` & `jaseci-1.4.0.9/jaseci/svc/postgres/manifest.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/prometheus/manifest.py` & `jaseci-1.4.0.9/jaseci/svc/prometheus/manifest.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/prometheus/prometheus.py` & `jaseci-1.4.0.9/jaseci/svc/prometheus/prometheus.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/redis/manifest.py` & `jaseci-1.4.0.9/jaseci/svc/redis/manifest.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/redis/redis.py` & `jaseci-1.4.0.9/jaseci/svc/redis/redis.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/task/common.py` & `jaseci-1.4.0.9/jaseci/svc/task/common.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/svc/task/task.py` & `jaseci-1.4.0.9/jaseci/svc/task/task.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/infer.py` & `jaseci-1.4.0.9/jaseci/tests/infer.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/jac_test_code.py` & `jaseci-1.4.0.9/jaseci/tests/jac_test_code.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/jac_test_progs.py` & `jaseci-1.4.0.9/jaseci/tests/jac_test_progs.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/test_core.py` & `jaseci-1.4.0.9/jaseci/tests/test_core.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/test_jac.py` & `jaseci-1.4.0.9/jaseci/tests/test_jac.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/test_node.py` & `jaseci-1.4.0.9/jaseci/tests/test_node.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/test_progs.py` & `jaseci-1.4.0.9/jaseci/tests/test_progs.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/tests/test_stack.py` & `jaseci-1.4.0.9/jaseci/tests/test_stack.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/utils/id_list.py` & `jaseci-1.4.0.9/jaseci/utils/id_list.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/utils/json_handler.py` & `jaseci-1.4.0.9/jaseci/utils/json_handler.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/utils/log_utils.py` & `jaseci-1.4.0.9/jaseci/utils/log_utils.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/utils/test_core.py` & `jaseci-1.4.0.9/jaseci/utils/test_core.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci/utils/utils.py` & `jaseci-1.4.0.9/jaseci/utils/utils.py`

 * *Files identical despite different names*

### Comparing `jaseci-1.4.0.8/jaseci.egg-info/SOURCES.txt` & `jaseci-1.4.0.9/jaseci.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 jaseci/actions/standard/internal.py
 jaseci/actions/standard/jaseci.py
 jaseci/actions/standard/mail.py
 jaseci/actions/standard/net.py
 jaseci/actions/standard/rand.py
 jaseci/actions/standard/request.py
 jaseci/actions/standard/std.py
+jaseci/actions/standard/stripe.py
 jaseci/actions/standard/task.py
 jaseci/actions/standard/url.py
 jaseci/actions/standard/vector.py
 jaseci/actions/standard/webtool.py
 jaseci/actions/standard/zlib.py
 jaseci/actions/standard/tests/__init__.py
 jaseci/actions/standard/tests/test_file_lib.py
@@ -60,14 +61,15 @@
 jaseci/api/object_api.py
 jaseci/api/prometheus_api.py
 jaseci/api/queue_api.py
 jaseci/api/sentinel_api.py
 jaseci/api/super_api.py
 jaseci/api/user_api.py
 jaseci/api/walker_api.py
+jaseci/api/webhook_api.py
 jaseci/api/tests/__init__.py
 jaseci/api/tests/test_architype_api.py
 jaseci/api/tests/test_global_api.py
 jaseci/api/tests/test_graph_api.py
 jaseci/api/tests/test_logger_api.py
 jaseci/api/tests/test_sentinel_api.py
 jaseci/api/tests/test_user_api.py
@@ -159,26 +161,30 @@
 jaseci/svc/prometheus/config.py
 jaseci/svc/prometheus/manifest.py
 jaseci/svc/prometheus/prometheus.py
 jaseci/svc/redis/__init__.py
 jaseci/svc/redis/config.py
 jaseci/svc/redis/manifest.py
 jaseci/svc/redis/redis.py
+jaseci/svc/stripe/__init__.py
+jaseci/svc/stripe/config.py
+jaseci/svc/stripe/stripe.py
 jaseci/svc/task/__init__.py
 jaseci/svc/task/common.py
 jaseci/svc/task/config.py
 jaseci/svc/task/task.py
 jaseci/tests/__init__.py
 jaseci/tests/infer.py
 jaseci/tests/jac_test_code.py
 jaseci/tests/jac_test_progs.py
 jaseci/tests/test_core.py
 jaseci/tests/test_jac.py
 jaseci/tests/test_node.py
 jaseci/tests/test_progs.py
 jaseci/tests/test_stack.py
+jaseci/tests/test_stripe.py
 jaseci/utils/__init__.py
 jaseci/utils/id_list.py
 jaseci/utils/json_handler.py
 jaseci/utils/log_utils.py
 jaseci/utils/test_core.py
 jaseci/utils/utils.py
```

### Comparing `jaseci-1.4.0.8/setup.py` & `jaseci-1.4.0.9/setup.py`

 * *Files identical despite different names*

