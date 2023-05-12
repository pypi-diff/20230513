# Comparing `tmp/strongdm-3.8.0.zip` & `tmp/strongdm-3.9.0.zip`

## zipinfo {}

```diff
@@ -1,85 +1,85 @@
-Zip file size: 231112 bytes, number of entries: 83
-drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-21 21:52 strongdm-3.8.0/
-drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-21 21:52 strongdm-3.8.0/strongdm/
-drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/
--rw-r--r--  2.0 unx     2652 b- defN 23-Mar-21 21:52 strongdm-3.8.0/README.md
--rw-r--r--  2.0 unx     1908 b- defN 23-Mar-21 21:52 strongdm-3.8.0/setup.py
--rw-r--r--  2.0 unx     3957 b- defN 23-Mar-21 21:52 strongdm-3.8.0/PKG-INFO
--rw-r--r--  2.0 unx       38 b- defN 23-Mar-21 21:52 strongdm-3.8.0/setup.cfg
--rw-r--r--  2.0 unx      808 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/__init__.py
--rw-r--r--  2.0 unx     8901 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_attachments_history_pb2.py
--rw-r--r--  2.0 unx     3493 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_attachments_history_pb2_grpc.py
--rw-r--r--  2.0 unx    17037 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_attachments_pb2.py
--rw-r--r--  2.0 unx     8102 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_attachments_pb2_grpc.py
--rw-r--r--  2.0 unx     8550 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_grants_history_pb2.py
--rw-r--r--  2.0 unx     3353 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_grants_history_pb2_grpc.py
--rw-r--r--  2.0 unx    16584 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_grants_pb2.py
--rw-r--r--  2.0 unx     7980 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_grants_pb2_grpc.py
--rw-r--r--  2.0 unx     8396 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_permissions_pb2.py
--rw-r--r--  2.0 unx     3470 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_permissions_pb2_grpc.py
--rw-r--r--  2.0 unx     8609 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_resources_pb2.py
--rw-r--r--  2.0 unx     3388 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/account_resources_pb2_grpc.py
--rw-r--r--  2.0 unx     8138 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/accounts_history_pb2.py
--rw-r--r--  2.0 unx     3198 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/accounts_history_pb2_grpc.py
--rw-r--r--  2.0 unx    22252 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/accounts_pb2.py
--rw-r--r--  2.0 unx     9494 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/accounts_pb2_grpc.py
--rw-r--r--  2.0 unx    16055 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/activities_pb2.py
--rw-r--r--  2.0 unx     4905 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/activities_pb2_grpc.py
--rw-r--r--  2.0 unx    17425 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/client.py
--rwxr-xr-x  2.0 unx    16248 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/constants.py
--rw-r--r--  2.0 unx     8369 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/control_panel_pb2.py
--rw-r--r--  2.0 unx     4879 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/control_panel_pb2_grpc.py
--rw-r--r--  2.0 unx   756938 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/drivers_pb2.py
--rw-r--r--  2.0 unx      741 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/drivers_pb2_grpc.py
--rw-r--r--  2.0 unx     2196 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/errors.py
--rw-r--r--  2.0 unx   509088 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/models.py
--rw-r--r--  2.0 unx     7818 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/nodes_history_pb2.py
--rw-r--r--  2.0 unx     3111 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/nodes_history_pb2_grpc.py
--rw-r--r--  2.0 unx    23038 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/nodes_pb2.py
--rw-r--r--  2.0 unx     9837 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/nodes_pb2_grpc.py
--rw-r--r--  2.0 unx    14750 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/options_pb2.py
--rw-r--r--  2.0 unx      741 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/options_pb2_grpc.py
--rw-r--r--  2.0 unx    16748 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/organization_history_pb2.py
--rw-r--r--  2.0 unx     3320 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/organization_history_pb2_grpc.py
--rw-r--r--  2.0 unx   289680 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/plumbing.py
--rw-r--r--  2.0 unx    12050 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/queries_pb2.py
--rw-r--r--  2.0 unx     3423 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/queries_pb2_grpc.py
--rw-r--r--  2.0 unx     8650 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identities_history_pb2.py
--rw-r--r--  2.0 unx     3424 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identities_history_pb2_grpc.py
--rw-r--r--  2.0 unx    19858 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identities_pb2.py
--rw-r--r--  2.0 unx     9790 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identities_pb2_grpc.py
--rw-r--r--  2.0 unx     9027 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2.py
--rw-r--r--  2.0 unx     3561 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2_grpc.py
--rw-r--r--  2.0 unx     9971 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identity_groups_pb2.py
--rw-r--r--  2.0 unx     6176 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/remote_identity_groups_pb2_grpc.py
--rw-r--r--  2.0 unx     8320 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/replays_pb2.py
--rw-r--r--  2.0 unx     3361 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/replays_pb2_grpc.py
--rw-r--r--  2.0 unx     8132 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/resources_history_pb2.py
--rw-r--r--  2.0 unx     3223 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/resources_history_pb2_grpc.py
--rw-r--r--  2.0 unx    19105 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/resources_pb2.py
--rw-r--r--  2.0 unx    10693 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/resources_pb2_grpc.py
--rw-r--r--  2.0 unx     8474 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/role_resources_history_pb2.py
--rw-r--r--  2.0 unx     3350 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/role_resources_history_pb2_grpc.py
--rw-r--r--  2.0 unx     7476 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/role_resources_pb2.py
--rw-r--r--  2.0 unx     3295 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/role_resources_pb2_grpc.py
--rw-r--r--  2.0 unx     7818 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/roles_history_pb2.py
--rw-r--r--  2.0 unx     3111 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/roles_history_pb2_grpc.py
--rw-r--r--  2.0 unx    18385 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/roles_pb2.py
--rw-r--r--  2.0 unx     9042 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/roles_pb2_grpc.py
--rw-r--r--  2.0 unx    31259 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_store_types_pb2.py
--rw-r--r--  2.0 unx      741 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_store_types_pb2_grpc.py
--rw-r--r--  2.0 unx     8412 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_stores_history_pb2.py
--rw-r--r--  2.0 unx     3322 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_stores_history_pb2_grpc.py
--rw-r--r--  2.0 unx    17214 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_stores_pb2.py
--rw-r--r--  2.0 unx     9376 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/secret_stores_pb2_grpc.py
--rw-r--r--  2.0 unx    15880 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/spec_pb2.py
--rw-r--r--  2.0 unx      741 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/spec_pb2_grpc.py
--rw-r--r--  2.0 unx   108624 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/svc.py
--rw-r--r--  2.0 unx     4600 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/tags_pb2.py
--rw-r--r--  2.0 unx      741 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm/tags_pb2_grpc.py
--rw-r--r--  2.0 unx     3957 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/PKG-INFO
--rw-r--r--  2.0 unx     2492 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/SOURCES.txt
--rw-r--r--  2.0 unx        1 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/dependency_links.txt
--rw-r--r--  2.0 unx       50 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/requires.txt
--rw-r--r--  2.0 unx        9 b- defN 23-Mar-21 21:52 strongdm-3.8.0/strongdm.egg-info/top_level.txt
-83 files, 2263329 bytes uncompressed, 217374 bytes compressed:  90.4%
+Zip file size: 231216 bytes, number of entries: 83
+drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-23 00:01 strongdm-3.9.0/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-23 00:01 strongdm-3.9.0/strongdm/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/
+-rw-r--r--  2.0 unx     2652 b- defN 23-Mar-23 00:01 strongdm-3.9.0/README.md
+-rw-r--r--  2.0 unx     1908 b- defN 23-Mar-23 00:01 strongdm-3.9.0/setup.py
+-rw-r--r--  2.0 unx     3957 b- defN 23-Mar-23 00:01 strongdm-3.9.0/PKG-INFO
+-rw-r--r--  2.0 unx       38 b- defN 23-Mar-23 00:01 strongdm-3.9.0/setup.cfg
+-rw-r--r--  2.0 unx      808 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/__init__.py
+-rw-r--r--  2.0 unx     8901 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_attachments_history_pb2.py
+-rw-r--r--  2.0 unx     3493 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_attachments_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    17037 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_attachments_pb2.py
+-rw-r--r--  2.0 unx     8102 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_attachments_pb2_grpc.py
+-rw-r--r--  2.0 unx     8550 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_grants_history_pb2.py
+-rw-r--r--  2.0 unx     3353 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_grants_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    16584 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_grants_pb2.py
+-rw-r--r--  2.0 unx     7980 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_grants_pb2_grpc.py
+-rw-r--r--  2.0 unx     8396 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_permissions_pb2.py
+-rw-r--r--  2.0 unx     3470 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_permissions_pb2_grpc.py
+-rw-r--r--  2.0 unx     8609 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_resources_pb2.py
+-rw-r--r--  2.0 unx     3388 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/account_resources_pb2_grpc.py
+-rw-r--r--  2.0 unx     8138 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/accounts_history_pb2.py
+-rw-r--r--  2.0 unx     3198 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/accounts_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    22252 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/accounts_pb2.py
+-rw-r--r--  2.0 unx     9494 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/accounts_pb2_grpc.py
+-rw-r--r--  2.0 unx    16055 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/activities_pb2.py
+-rw-r--r--  2.0 unx     4905 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/activities_pb2_grpc.py
+-rw-r--r--  2.0 unx    17425 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/client.py
+-rwxr-xr-x  2.0 unx    16466 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/constants.py
+-rw-r--r--  2.0 unx     8369 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/control_panel_pb2.py
+-rw-r--r--  2.0 unx     4879 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/control_panel_pb2_grpc.py
+-rw-r--r--  2.0 unx   756938 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/drivers_pb2.py
+-rw-r--r--  2.0 unx      741 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/drivers_pb2_grpc.py
+-rw-r--r--  2.0 unx     2196 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/errors.py
+-rw-r--r--  2.0 unx   509088 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/models.py
+-rw-r--r--  2.0 unx     7818 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/nodes_history_pb2.py
+-rw-r--r--  2.0 unx     3111 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/nodes_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    23038 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/nodes_pb2.py
+-rw-r--r--  2.0 unx     9837 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/nodes_pb2_grpc.py
+-rw-r--r--  2.0 unx    14750 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/options_pb2.py
+-rw-r--r--  2.0 unx      741 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/options_pb2_grpc.py
+-rw-r--r--  2.0 unx    16748 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/organization_history_pb2.py
+-rw-r--r--  2.0 unx     3320 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/organization_history_pb2_grpc.py
+-rw-r--r--  2.0 unx   289680 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/plumbing.py
+-rw-r--r--  2.0 unx    12050 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/queries_pb2.py
+-rw-r--r--  2.0 unx     3423 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/queries_pb2_grpc.py
+-rw-r--r--  2.0 unx     8650 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identities_history_pb2.py
+-rw-r--r--  2.0 unx     3424 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identities_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    19858 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identities_pb2.py
+-rw-r--r--  2.0 unx     9790 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identities_pb2_grpc.py
+-rw-r--r--  2.0 unx     9027 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2.py
+-rw-r--r--  2.0 unx     3561 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2_grpc.py
+-rw-r--r--  2.0 unx     9971 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identity_groups_pb2.py
+-rw-r--r--  2.0 unx     6176 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/remote_identity_groups_pb2_grpc.py
+-rw-r--r--  2.0 unx     8320 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/replays_pb2.py
+-rw-r--r--  2.0 unx     3361 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/replays_pb2_grpc.py
+-rw-r--r--  2.0 unx     8132 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/resources_history_pb2.py
+-rw-r--r--  2.0 unx     3223 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/resources_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    19105 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/resources_pb2.py
+-rw-r--r--  2.0 unx    10693 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/resources_pb2_grpc.py
+-rw-r--r--  2.0 unx     8474 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/role_resources_history_pb2.py
+-rw-r--r--  2.0 unx     3350 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/role_resources_history_pb2_grpc.py
+-rw-r--r--  2.0 unx     7476 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/role_resources_pb2.py
+-rw-r--r--  2.0 unx     3295 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/role_resources_pb2_grpc.py
+-rw-r--r--  2.0 unx     7818 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/roles_history_pb2.py
+-rw-r--r--  2.0 unx     3111 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/roles_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    18385 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/roles_pb2.py
+-rw-r--r--  2.0 unx     9042 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/roles_pb2_grpc.py
+-rw-r--r--  2.0 unx    31259 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_store_types_pb2.py
+-rw-r--r--  2.0 unx      741 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_store_types_pb2_grpc.py
+-rw-r--r--  2.0 unx     8412 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_stores_history_pb2.py
+-rw-r--r--  2.0 unx     3322 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_stores_history_pb2_grpc.py
+-rw-r--r--  2.0 unx    17214 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_stores_pb2.py
+-rw-r--r--  2.0 unx     9376 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/secret_stores_pb2_grpc.py
+-rw-r--r--  2.0 unx    15880 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/spec_pb2.py
+-rw-r--r--  2.0 unx      741 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/spec_pb2_grpc.py
+-rw-r--r--  2.0 unx   108624 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/svc.py
+-rw-r--r--  2.0 unx     4600 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/tags_pb2.py
+-rw-r--r--  2.0 unx      741 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm/tags_pb2_grpc.py
+-rw-r--r--  2.0 unx     3957 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/PKG-INFO
+-rw-r--r--  2.0 unx     2492 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/SOURCES.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/dependency_links.txt
+-rw-r--r--  2.0 unx       50 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/requires.txt
+-rw-r--r--  2.0 unx        9 b- defN 23-Mar-23 00:01 strongdm-3.9.0/strongdm.egg-info/top_level.txt
+83 files, 2263547 bytes uncompressed, 217478 bytes compressed:  90.4%
```

## zipnote {}

```diff
@@ -1,250 +1,250 @@
-Filename: strongdm-3.8.0/
+Filename: strongdm-3.9.0/
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/
+Filename: strongdm-3.9.0/strongdm/
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/
+Filename: strongdm-3.9.0/strongdm.egg-info/
 Comment: 
 
-Filename: strongdm-3.8.0/README.md
+Filename: strongdm-3.9.0/README.md
 Comment: 
 
-Filename: strongdm-3.8.0/setup.py
+Filename: strongdm-3.9.0/setup.py
 Comment: 
 
-Filename: strongdm-3.8.0/PKG-INFO
+Filename: strongdm-3.9.0/PKG-INFO
 Comment: 
 
-Filename: strongdm-3.8.0/setup.cfg
+Filename: strongdm-3.9.0/setup.cfg
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/__init__.py
+Filename: strongdm-3.9.0/strongdm/__init__.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_attachments_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_attachments_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_attachments_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_attachments_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_attachments_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_attachments_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_attachments_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_attachments_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_grants_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_grants_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_grants_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_grants_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_grants_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_grants_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_grants_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_grants_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_permissions_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_permissions_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_permissions_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_permissions_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_resources_pb2.py
+Filename: strongdm-3.9.0/strongdm/account_resources_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/account_resources_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/account_resources_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/accounts_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/accounts_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/accounts_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/accounts_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/accounts_pb2.py
+Filename: strongdm-3.9.0/strongdm/accounts_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/accounts_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/accounts_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/activities_pb2.py
+Filename: strongdm-3.9.0/strongdm/activities_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/activities_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/activities_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/client.py
+Filename: strongdm-3.9.0/strongdm/client.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/constants.py
+Filename: strongdm-3.9.0/strongdm/constants.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/control_panel_pb2.py
+Filename: strongdm-3.9.0/strongdm/control_panel_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/control_panel_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/control_panel_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/drivers_pb2.py
+Filename: strongdm-3.9.0/strongdm/drivers_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/drivers_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/drivers_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/errors.py
+Filename: strongdm-3.9.0/strongdm/errors.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/models.py
+Filename: strongdm-3.9.0/strongdm/models.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/nodes_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/nodes_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/nodes_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/nodes_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/nodes_pb2.py
+Filename: strongdm-3.9.0/strongdm/nodes_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/nodes_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/nodes_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/options_pb2.py
+Filename: strongdm-3.9.0/strongdm/options_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/options_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/options_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/organization_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/organization_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/organization_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/organization_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/plumbing.py
+Filename: strongdm-3.9.0/strongdm/plumbing.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/queries_pb2.py
+Filename: strongdm-3.9.0/strongdm/queries_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/queries_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/queries_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identities_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/remote_identities_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identities_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/remote_identities_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identities_pb2.py
+Filename: strongdm-3.9.0/strongdm/remote_identities_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identities_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/remote_identities_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identity_groups_pb2.py
+Filename: strongdm-3.9.0/strongdm/remote_identity_groups_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/remote_identity_groups_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/remote_identity_groups_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/replays_pb2.py
+Filename: strongdm-3.9.0/strongdm/replays_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/replays_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/replays_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/resources_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/resources_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/resources_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/resources_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/resources_pb2.py
+Filename: strongdm-3.9.0/strongdm/resources_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/resources_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/resources_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/role_resources_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/role_resources_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/role_resources_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/role_resources_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/role_resources_pb2.py
+Filename: strongdm-3.9.0/strongdm/role_resources_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/role_resources_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/role_resources_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/roles_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/roles_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/roles_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/roles_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/roles_pb2.py
+Filename: strongdm-3.9.0/strongdm/roles_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/roles_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/roles_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_store_types_pb2.py
+Filename: strongdm-3.9.0/strongdm/secret_store_types_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_store_types_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/secret_store_types_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_stores_history_pb2.py
+Filename: strongdm-3.9.0/strongdm/secret_stores_history_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_stores_history_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/secret_stores_history_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_stores_pb2.py
+Filename: strongdm-3.9.0/strongdm/secret_stores_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/secret_stores_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/secret_stores_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/spec_pb2.py
+Filename: strongdm-3.9.0/strongdm/spec_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/spec_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/spec_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/svc.py
+Filename: strongdm-3.9.0/strongdm/svc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/tags_pb2.py
+Filename: strongdm-3.9.0/strongdm/tags_pb2.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm/tags_pb2_grpc.py
+Filename: strongdm-3.9.0/strongdm/tags_pb2_grpc.py
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/PKG-INFO
+Filename: strongdm-3.9.0/strongdm.egg-info/PKG-INFO
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/SOURCES.txt
+Filename: strongdm-3.9.0/strongdm.egg-info/SOURCES.txt
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/dependency_links.txt
+Filename: strongdm-3.9.0/strongdm.egg-info/dependency_links.txt
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/requires.txt
+Filename: strongdm-3.9.0/strongdm.egg-info/requires.txt
 Comment: 
 
-Filename: strongdm-3.8.0/strongdm.egg-info/top_level.txt
+Filename: strongdm-3.9.0/strongdm.egg-info/top_level.txt
 Comment: 
 
 Zip file comment:
```

## Comparing `strongdm-3.8.0/README.md` & `strongdm-3.9.0/README.md`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/setup.py` & `strongdm-3.9.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -19,24 +19,24 @@
 with open(path.join(this_directory, 'README.md'), encoding='utf-8') as f:
     long_description = f.read()
 
 from setuptools import setup
 setup(
     name='strongdm',
     packages=['strongdm'],
-    version='3.8.0',
+    version='3.9.0',
     license='apache-2.0',
     description='strongDM SDK for the Python programming language.',
     long_description=long_description,
     long_description_content_type='text/markdown',
     author='strongDM Team',
     author_email='sdk-feedback@strongdm.com',
     url='https://github.com/strongdm/strongdm-sdk-python',
     download_url=
-    'https://github.com/strongdm/strongdm-sdk-python/archive/v3.8.0.tar.gz',
+    'https://github.com/strongdm/strongdm-sdk-python/archive/v3.9.0.tar.gz',
     keywords=[
         'strongDM', 'sdm', 'api', 'automation', 'security', 'audit',
         'database', 'server', 'ssh', 'rdp'
     ],
     install_requires=[
         'grpcio>=1.42.0',
         'googleapis-common-protos>1.56.2,<2',
```

## Comparing `strongdm-3.8.0/PKG-INFO` & `strongdm-3.9.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: strongdm
-Version: 3.8.0
+Version: 3.9.0
 Summary: strongDM SDK for the Python programming language.
 Home-page: https://github.com/strongdm/strongdm-sdk-python
 Author: strongDM Team
 Author-email: sdk-feedback@strongdm.com
 License: apache-2.0
-Download-URL: https://github.com/strongdm/strongdm-sdk-python/archive/v3.8.0.tar.gz
+Download-URL: https://github.com/strongdm/strongdm-sdk-python/archive/v3.9.0.tar.gz
 Description: # strongDM SDK for Python
         
         This is the official [strongDM](https://www.strongdm.com/) SDK for the Python
         programming language.
         
         Learn more with our [📚strongDM API docs](https://www.strongdm.com/docs/api/) or
         [📓browse the SDK
```

## Comparing `strongdm-3.8.0/strongdm/__init__.py` & `strongdm-3.9.0/strongdm/__init__.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_attachments_history_pb2.py` & `strongdm-3.9.0/strongdm/account_attachments_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_attachments_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_attachments_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_attachments_pb2.py` & `strongdm-3.9.0/strongdm/account_attachments_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_attachments_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_attachments_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_grants_history_pb2.py` & `strongdm-3.9.0/strongdm/account_grants_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_grants_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_grants_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_grants_pb2.py` & `strongdm-3.9.0/strongdm/account_grants_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_grants_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_grants_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_permissions_pb2.py` & `strongdm-3.9.0/strongdm/account_permissions_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_permissions_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_permissions_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_resources_pb2.py` & `strongdm-3.9.0/strongdm/account_resources_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/account_resources_pb2_grpc.py` & `strongdm-3.9.0/strongdm/account_resources_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/accounts_history_pb2.py` & `strongdm-3.9.0/strongdm/accounts_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/accounts_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/accounts_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/accounts_pb2.py` & `strongdm-3.9.0/strongdm/accounts_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/accounts_pb2_grpc.py` & `strongdm-3.9.0/strongdm/accounts_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/activities_pb2.py` & `strongdm-3.9.0/strongdm/activities_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/activities_pb2_grpc.py` & `strongdm-3.9.0/strongdm/activities_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/client.py` & `strongdm-3.9.0/strongdm/client.py`

 * *Files 0% similar despite different names*

```diff
@@ -28,15 +28,15 @@
 
 # These defaults are taken from AWS. Customization of these values
 # is a future step in the API.
 DEFAULT_MAX_RETRIES = 3
 DEFAULT_BASE_RETRY_DELAY = 0.0030  # 30 ms
 DEFAULT_MAX_RETRY_DELAY = 300  # 300 seconds
 API_VERSION = '2021-08-23'
-USER_AGENT = 'strongdm-sdk-python/3.8.0'
+USER_AGENT = 'strongdm-sdk-python/3.9.0'
 
 
 class Client:
     '''Client interacts with the strongDM API.'''
     def __init__(self,
                  api_access_key,
                  api_secret,
```

## Comparing `strongdm-3.8.0/strongdm/constants.py` & `strongdm-3.9.0/strongdm/constants.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 #
-# @internal This file was generated by constgen. DO NOT EDIT.
+# @internal Code generated by constgen. DO NOT EDIT.
 
 
 # Permission Levels, shared by all entities capable of making authenticated requests against StrongDM.
 class PermissionLevel:
     ROOT_ADMIN = "root-admin"
     ADMIN = "admin"
     DATABASE_ADMIN = "database-admin"
@@ -371,7 +371,17 @@
 
 
 # OrgKind defines the types of organizations that may exist.
 class OrgKind:
     SOLO = "solo"
     ROOT = "root"
     CHILD = "child"
+
+
+# KeyType defines the supported SSH key types
+class SSHKeyType:
+    RSA_2048 = "rsa-2048"
+    RSA_4096 = "rsa-4096"
+    ECDSA_256 = "ecdsa-256"
+    ECDSA_384 = "ecdsa-384"
+    ECDSA_521 = "ecdsa-521"
+    ED_25519 = "ed25519"
```

## Comparing `strongdm-3.8.0/strongdm/control_panel_pb2.py` & `strongdm-3.9.0/strongdm/control_panel_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/control_panel_pb2_grpc.py` & `strongdm-3.9.0/strongdm/control_panel_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/drivers_pb2.py` & `strongdm-3.9.0/strongdm/drivers_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/drivers_pb2_grpc.py` & `strongdm-3.9.0/strongdm/drivers_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/errors.py` & `strongdm-3.9.0/strongdm/errors.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/models.py` & `strongdm-3.9.0/strongdm/models.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/nodes_history_pb2.py` & `strongdm-3.9.0/strongdm/nodes_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/nodes_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/nodes_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/nodes_pb2.py` & `strongdm-3.9.0/strongdm/nodes_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/nodes_pb2_grpc.py` & `strongdm-3.9.0/strongdm/nodes_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/options_pb2.py` & `strongdm-3.9.0/strongdm/options_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/options_pb2_grpc.py` & `strongdm-3.9.0/strongdm/options_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/organization_history_pb2.py` & `strongdm-3.9.0/strongdm/organization_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/organization_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/organization_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/plumbing.py` & `strongdm-3.9.0/strongdm/plumbing.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/queries_pb2.py` & `strongdm-3.9.0/strongdm/queries_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/queries_pb2_grpc.py` & `strongdm-3.9.0/strongdm/queries_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identities_history_pb2.py` & `strongdm-3.9.0/strongdm/remote_identities_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identities_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/remote_identities_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identities_pb2.py` & `strongdm-3.9.0/strongdm/remote_identities_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identities_pb2_grpc.py` & `strongdm-3.9.0/strongdm/remote_identities_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2.py` & `strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identity_groups_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/remote_identity_groups_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identity_groups_pb2.py` & `strongdm-3.9.0/strongdm/remote_identity_groups_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/remote_identity_groups_pb2_grpc.py` & `strongdm-3.9.0/strongdm/remote_identity_groups_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/replays_pb2.py` & `strongdm-3.9.0/strongdm/replays_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/replays_pb2_grpc.py` & `strongdm-3.9.0/strongdm/replays_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/resources_history_pb2.py` & `strongdm-3.9.0/strongdm/resources_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/resources_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/resources_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/resources_pb2.py` & `strongdm-3.9.0/strongdm/resources_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/resources_pb2_grpc.py` & `strongdm-3.9.0/strongdm/resources_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/role_resources_history_pb2.py` & `strongdm-3.9.0/strongdm/role_resources_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/role_resources_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/role_resources_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/role_resources_pb2.py` & `strongdm-3.9.0/strongdm/role_resources_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/role_resources_pb2_grpc.py` & `strongdm-3.9.0/strongdm/role_resources_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/roles_history_pb2.py` & `strongdm-3.9.0/strongdm/roles_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/roles_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/roles_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/roles_pb2.py` & `strongdm-3.9.0/strongdm/roles_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/roles_pb2_grpc.py` & `strongdm-3.9.0/strongdm/roles_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_store_types_pb2.py` & `strongdm-3.9.0/strongdm/secret_store_types_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_store_types_pb2_grpc.py` & `strongdm-3.9.0/strongdm/secret_store_types_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_stores_history_pb2.py` & `strongdm-3.9.0/strongdm/secret_stores_history_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_stores_history_pb2_grpc.py` & `strongdm-3.9.0/strongdm/secret_stores_history_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_stores_pb2.py` & `strongdm-3.9.0/strongdm/secret_stores_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/secret_stores_pb2_grpc.py` & `strongdm-3.9.0/strongdm/secret_stores_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/spec_pb2.py` & `strongdm-3.9.0/strongdm/spec_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/spec_pb2_grpc.py` & `strongdm-3.9.0/strongdm/spec_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/svc.py` & `strongdm-3.9.0/strongdm/svc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/tags_pb2.py` & `strongdm-3.9.0/strongdm/tags_pb2.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm/tags_pb2_grpc.py` & `strongdm-3.9.0/strongdm/tags_pb2_grpc.py`

 * *Files identical despite different names*

## Comparing `strongdm-3.8.0/strongdm.egg-info/PKG-INFO` & `strongdm-3.9.0/strongdm.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: strongdm
-Version: 3.8.0
+Version: 3.9.0
 Summary: strongDM SDK for the Python programming language.
 Home-page: https://github.com/strongdm/strongdm-sdk-python
 Author: strongDM Team
 Author-email: sdk-feedback@strongdm.com
 License: apache-2.0
-Download-URL: https://github.com/strongdm/strongdm-sdk-python/archive/v3.8.0.tar.gz
+Download-URL: https://github.com/strongdm/strongdm-sdk-python/archive/v3.9.0.tar.gz
 Description: # strongDM SDK for Python
         
         This is the official [strongDM](https://www.strongdm.com/) SDK for the Python
         programming language.
         
         Learn more with our [📚strongDM API docs](https://www.strongdm.com/docs/api/) or
         [📓browse the SDK
```

## Comparing `strongdm-3.8.0/strongdm.egg-info/SOURCES.txt` & `strongdm-3.9.0/strongdm.egg-info/SOURCES.txt`

 * *Files identical despite different names*

