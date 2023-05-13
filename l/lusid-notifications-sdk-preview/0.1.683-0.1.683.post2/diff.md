# Comparing `tmp/lusid-notifications-sdk-preview-0.1.683.tar.gz` & `tmp/lusid-notifications-sdk-preview-0.1.683.post2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/lusid-notifications-sdk-preview-0.1.683.tar", last modified: Sat May 13 11:33:44 2023, max compression
+gzip compressed data, was "dist/lusid-notifications-sdk-preview-0.1.683.post2.tar", last modified: Sat May 13 11:36:18 2023, max compression
```

## Comparing `lusid-notifications-sdk-preview-0.1.683.tar` & `lusid-notifications-sdk-preview-0.1.683.post2.tar`

### file list

```diff
@@ -1,67 +1,63 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/
--rw-r--r--   0 root         (0) root         (0)       54 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)      373 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     9642 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/
--rw-r--r--   0 root         (0) root         (0)     4427 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/__init__.py
--rw-r--r--   0 root         (0) root         (0)       24 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/__version__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/
--rw-r--r--   0 root         (0) root         (0)      501 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/__init__.py
--rw-r--r--   0 root         (0) root         (0)     6851 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/application_metadata_api.py
--rw-r--r--   0 root         (0) root         (0)    10524 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/deliveries_api.py
--rw-r--r--   0 root         (0) root         (0)    13990 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/event_types_api.py
--rw-r--r--   0 root         (0) root         (0)     6975 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/events_api.py
--rw-r--r--   0 root         (0) root         (0)   122660 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/notifications_api.py
--rw-r--r--   0 root         (0) root         (0)    47907 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/subscriptions_api.py
--rw-r--r--   0 root         (0) root         (0)    27436 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api_client.py
--rw-r--r--   0 root         (0) root         (0)    16635 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/configuration.py
--rw-r--r--   0 root         (0) root         (0)     5099 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/exceptions.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/
--rw-r--r--   0 root         (0) root         (0)     3073 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/__init__.py
--rw-r--r--   0 root         (0) root         (0)     7264 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/access_controlled_action.py
--rw-r--r--   0 root         (0) root         (0)     9027 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/access_controlled_resource.py
--rw-r--r--   0 root         (0) root         (0)     7232 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/action_id.py
--rw-r--r--   0 root         (0) root         (0)     6512 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/attempt.py
--rw-r--r--   0 root         (0) root         (0)     5557 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/attempt_status.py
--rw-r--r--   0 root         (0) root         (0)    11703 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_aws_sqs_notification.py
--rw-r--r--   0 root         (0) root         (0)    16290 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_email_notification.py
--rw-r--r--   0 root         (0) root         (0)     8814 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_sms_notification.py
--rw-r--r--   0 root         (0) root         (0)    10822 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_subscription.py
--rw-r--r--   0 root         (0) root         (0)    16161 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_webhook_notification.py
--rw-r--r--   0 root         (0) root         (0)    12397 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/delivery.py
--rw-r--r--   0 root         (0) root         (0)     4091 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/event_details.py
--rw-r--r--   0 root         (0) root         (0)     8514 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/event_type_schema.py
--rw-r--r--   0 root         (0) root         (0)     8025 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/id_selector_definition.py
--rw-r--r--   0 root         (0) root         (0)     9514 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/identifier_part_schema.py
--rw-r--r--   0 root         (0) root         (0)     6426 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/link.py
--rw-r--r--   0 root         (0) root         (0)     9540 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/lusid_problem_details.py
--rw-r--r--   0 root         (0) root         (0)    10705 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/lusid_validation_problem_details.py
--rw-r--r--   0 root         (0) root         (0)     7344 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/matching_pattern.py
--rw-r--r--   0 root         (0) root         (0)    18059 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/notification.py
--rw-r--r--   0 root         (0) root         (0)     5155 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/notification_status.py
--rw-r--r--   0 root         (0) root         (0)     6099 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_id.py
--rw-r--r--   0 root         (0) root         (0)     7775 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_access_controlled_resource.py
--rw-r--r--   0 root         (0) root         (0)     7327 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_delivery.py
--rw-r--r--   0 root         (0) root         (0)     7523 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_event_type_schema.py
--rw-r--r--   0 root         (0) root         (0)     7439 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_notification.py
--rw-r--r--   0 root         (0) root         (0)     7439 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_subscription.py
--rw-r--r--   0 root         (0) root         (0)    14416 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/subscription.py
--rw-r--r--   0 root         (0) root         (0)    15824 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/subscription_detail.py
--rw-r--r--   0 root         (0) root         (0)    11703 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_aws_sqs_notification.py
--rw-r--r--   0 root         (0) root         (0)    16290 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_email_notification.py
--rw-r--r--   0 root         (0) root         (0)     8814 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_sms_notification.py
--rw-r--r--   0 root         (0) root         (0)     9939 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_subscription.py
--rw-r--r--   0 root         (0) root         (0)    16161 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_webhook_notification.py
--rw-r--r--   0 root         (0) root         (0)    13561 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/rest.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/utilities/
--rw-r--r--   0 root         (0) root         (0)       65 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/utilities/__init__.py
--rw-r--r--   0 root         (0) root         (0)     1042 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/utilities/config_keys.json
--rw-r--r--   0 root         (0) root         (0)      295 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications/utilities/config_keys.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/
--rw-r--r--   0 root         (0) root         (0)      373 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     2742 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)      116 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       20 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 11:33:44.000000 lusid-notifications-sdk-preview-0.1.683/setup.cfg
--rw-r--r--   0 root         (0) root         (0)     2322 2023-05-13 11:31:14.000000 lusid-notifications-sdk-preview-0.1.683/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/
+-rw-r--r--   0 root         (0) root         (0)       54 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)      379 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     7731 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/
+-rw-r--r--   0 root         (0) root         (0)     4028 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/__init__.py
+-rw-r--r--   0 root         (0) root         (0)       26 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/__version__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/
+-rw-r--r--   0 root         (0) root         (0)      512 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     6855 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/application_metadata_api.py
+-rw-r--r--   0 root         (0) root         (0)    10528 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/deliveries_api.py
+-rw-r--r--   0 root         (0) root         (0)    13996 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/event_types_api.py
+-rw-r--r--   0 root         (0) root         (0)     7471 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/manual_event_api.py
+-rw-r--r--   0 root         (0) root         (0)    52531 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/notifications_api.py
+-rw-r--r--   0 root         (0) root         (0)    47919 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/subscriptions_api.py
+-rw-r--r--   0 root         (0) root         (0)    27440 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api_client.py
+-rw-r--r--   0 root         (0) root         (0)    16639 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/configuration.py
+-rw-r--r--   0 root         (0) root         (0)     5101 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/exceptions.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/
+-rw-r--r--   0 root         (0) root         (0)     2661 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     7266 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/access_controlled_action.py
+-rw-r--r--   0 root         (0) root         (0)     9029 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/access_controlled_resource.py
+-rw-r--r--   0 root         (0) root         (0)     7234 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/action_id.py
+-rw-r--r--   0 root         (0) root         (0)     6514 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/attempt.py
+-rw-r--r--   0 root         (0) root         (0)     5559 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/attempt_status.py
+-rw-r--r--   0 root         (0) root         (0)    10330 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/create_notification.py
+-rw-r--r--   0 root         (0) root         (0)    10824 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/create_subscription.py
+-rw-r--r--   0 root         (0) root         (0)    12399 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/delivery.py
+-rw-r--r--   0 root         (0) root         (0)     9340 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/event_type_schema.py
+-rw-r--r--   0 root         (0) root         (0)     8027 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/id_selector_definition.py
+-rw-r--r--   0 root         (0) root         (0)     9516 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/identifier_part_schema.py
+-rw-r--r--   0 root         (0) root         (0)     6428 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/link.py
+-rw-r--r--   0 root         (0) root         (0)     9542 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/lusid_problem_details.py
+-rw-r--r--   0 root         (0) root         (0)    10707 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/lusid_validation_problem_details.py
+-rw-r--r--   0 root         (0) root         (0)     5095 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/manual_event.py
+-rw-r--r--   0 root         (0) root         (0)     7866 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/manual_event_body.py
+-rw-r--r--   0 root         (0) root         (0)     6830 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/manual_event_header.py
+-rw-r--r--   0 root         (0) root         (0)     7346 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/matching_pattern.py
+-rw-r--r--   0 root         (0) root         (0)    18061 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/notification.py
+-rw-r--r--   0 root         (0) root         (0)     5157 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/notification_status.py
+-rw-r--r--   0 root         (0) root         (0)     6101 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_id.py
+-rw-r--r--   0 root         (0) root         (0)     7777 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_access_controlled_resource.py
+-rw-r--r--   0 root         (0) root         (0)     7329 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_delivery.py
+-rw-r--r--   0 root         (0) root         (0)     7525 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_event_type_schema.py
+-rw-r--r--   0 root         (0) root         (0)     7441 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_notification.py
+-rw-r--r--   0 root         (0) root         (0)     7441 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_subscription.py
+-rw-r--r--   0 root         (0) root         (0)    14433 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/subscription.py
+-rw-r--r--   0 root         (0) root         (0)    14673 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/subscription_detail.py
+-rw-r--r--   0 root         (0) root         (0)     8187 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/update_notification.py
+-rw-r--r--   0 root         (0) root         (0)     9941 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/update_subscription.py
+-rw-r--r--   0 root         (0) root         (0)    13563 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/rest.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/utilities/
+-rw-r--r--   0 root         (0) root         (0)       65 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/utilities/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     1042 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/utilities/config_keys.json
+-rw-r--r--   0 root         (0) root         (0)      295 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/utilities/config_keys.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      379 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     2493 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)      116 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       20 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 11:36:18.000000 lusid-notifications-sdk-preview-0.1.683.post2/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)     2322 2023-05-13 11:35:09.000000 lusid-notifications-sdk-preview-0.1.683.post2/setup.py
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/README.md` & `lusid-notifications-sdk-preview-0.1.683.post2/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # lusid-notifications-sdk
 FINBOURNE Technology
 
 This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:
 
-- API version: 0.1.683
-- Package version: 0.1.683
+- API version: 0.1.683-2
+- Package version: 0.1.683-2
 - Build package: org.openapitools.codegen.languages.PythonLegacyClientCodegen
 For more information, please visit [https://www.finbourne.com](https://www.finbourne.com)
 
 ## Requirements.
 
 Python 2.7 and 3.4+
 
@@ -49,28 +49,28 @@
 from __future__ import print_function
 
 import time
 import lusid_notifications
 from lusid_notifications.rest import ApiException
 from pprint import pprint
 
-# Defining the host is optional and defaults to https://www.lusid.com/notifications
+# Defining the host is optional and defaults to https://www.lusid.com/notification
 # See configuration.py for a list of all supported configuration parameters.
 configuration = lusid_notifications.Configuration(
-    host = "https://www.lusid.com/notifications"
+    host = "https://www.lusid.com/notification"
 )
 
 # The client must configure the authentication and authorization parameters
 # in accordance with the API server security policy.
 # Examples for each auth method are provided below, use the example that
 # satisfies your auth use case.
 
 # Configure OAuth2 access token for authorization: oauth2
 configuration = lusid_notifications.Configuration(
-    host = "https://www.lusid.com/notifications"
+    host = "https://www.lusid.com/notification"
 )
 configuration.access_token = 'YOUR_ACCESS_TOKEN'
 
 
 # Enter a context with an instance of the API client
 with lusid_notifications.ApiClient(configuration) as api_client:
     # Create an instance of the API class
@@ -83,77 +83,67 @@
     except ApiException as e:
         print("Exception when calling ApplicationMetadataApi->list_access_controlled_resources: %s\n" % e)
     
 ```
 
 ## Documentation for API Endpoints
 
-All URIs are relative to *https://www.lusid.com/notifications*
+All URIs are relative to *https://www.lusid.com/notification*
 
 Class | Method | HTTP request | Description
 ------------ | ------------- | ------------- | -------------
 *ApplicationMetadataApi* | [**list_access_controlled_resources**](docs/ApplicationMetadataApi.md#list_access_controlled_resources) | **GET** /api/metadata/access/resources | [EARLY ACCESS] ListAccessControlledResources: Get resources available for access control
 *DeliveriesApi* | [**list_deliveries**](docs/DeliveriesApi.md#list_deliveries) | **GET** /api/deliveries | [EXPERIMENTAL] ListDeliveries: List Deliveries
 *EventTypesApi* | [**get_event_type**](docs/EventTypesApi.md#get_event_type) | **GET** /api/eventtypes/{eventType} | [EXPERIMENTAL] GetEventType: Gets the specified event type schema.
 *EventTypesApi* | [**list_event_types**](docs/EventTypesApi.md#list_event_types) | **GET** /api/eventtypes | [EXPERIMENTAL] ListEventTypes: Lists all of the available event types.
-*EventsApi* | [**create_event**](docs/EventsApi.md#create_event) | **POST** /api/events | [EXPERIMENTAL] CreateEvent: Create a new event.
-*NotificationsApi* | [**create_aws_sqs_notification**](docs/NotificationsApi.md#create_aws_sqs_notification) | **POST** /api/subscriptions/{scope}/{code}/notifications/awssqs | [EXPERIMENTAL] CreateAwsSqsNotification: Add an AWS SQS notification to a subscription.
-*NotificationsApi* | [**create_email_notification**](docs/NotificationsApi.md#create_email_notification) | **POST** /api/subscriptions/{scope}/{code}/notifications/email | [EXPERIMENTAL] CreateEmailNotification: Add an email notification to a subscription.
-*NotificationsApi* | [**create_sms_notification**](docs/NotificationsApi.md#create_sms_notification) | **POST** /api/subscriptions/{scope}/{code}/notifications/sms | [EXPERIMENTAL] CreateSmsNotification: Add an SMS notification to a subscription.
-*NotificationsApi* | [**create_webhook_notification**](docs/NotificationsApi.md#create_webhook_notification) | **POST** /api/subscriptions/{scope}/{code}/notifications/webhook | [EXPERIMENTAL] CreateWebhookNotification: Add a Webhook notification to a subscription.
+*ManualEventApi* | [**trigger_manual_event**](docs/ManualEventApi.md#trigger_manual_event) | **POST** /api/manualevent | [EXPERIMENTAL] TriggerManualEvent: Trigger a manual event.
+*NotificationsApi* | [**create_notification**](docs/NotificationsApi.md#create_notification) | **POST** /api/subscriptions/{scope}/{code}/notifications | [EXPERIMENTAL] CreateNotification: Add a notification to a subscription.
 *NotificationsApi* | [**delete_notification**](docs/NotificationsApi.md#delete_notification) | **DELETE** /api/subscriptions/{scope}/{code}/notifications/{id} | [EXPERIMENTAL] DeleteNotification: Delete a notification for a given subscription.
 *NotificationsApi* | [**get_notification**](docs/NotificationsApi.md#get_notification) | **GET** /api/subscriptions/{scope}/{code}/notifications/{id} | [EXPERIMENTAL] GetNotification: Get a notification on a subscription.
 *NotificationsApi* | [**list_notifications**](docs/NotificationsApi.md#list_notifications) | **GET** /api/subscriptions/{scope}/{code}/notifications | [EXPERIMENTAL] ListNotifications: List all notifications on a subscription.
-*NotificationsApi* | [**update_aws_sqs_notification**](docs/NotificationsApi.md#update_aws_sqs_notification) | **PUT** /api/subscriptions/{scope}/{code}/notifications/awssqs/{id} | [EXPERIMENTAL] UpdateAwsSqsNotification: Update an AWS SQS notification for a given subscription.
-*NotificationsApi* | [**update_email_notification**](docs/NotificationsApi.md#update_email_notification) | **PUT** /api/subscriptions/{scope}/{code}/notifications/email/{id} | [EXPERIMENTAL] UpdateEmailNotification: Update an email notification for a given subscription.
-*NotificationsApi* | [**update_sms_notification**](docs/NotificationsApi.md#update_sms_notification) | **PUT** /api/subscriptions/{scope}/{code}/notifications/sms/{id} | [EXPERIMENTAL] UpdateSmsNotification: Update an SMS notification for a given subscription.
-*NotificationsApi* | [**update_webhook_notification**](docs/NotificationsApi.md#update_webhook_notification) | **PUT** /api/subscriptions/{scope}/{code}/notifications/webhook/{id} | [EXPERIMENTAL] UpdateWebhookNotification: Update a Webhook notification for a given subscription.
+*NotificationsApi* | [**update_notification**](docs/NotificationsApi.md#update_notification) | **PUT** /api/subscriptions/{scope}/{code}/notifications/{id} | [EXPERIMENTAL] UpdateNotification: Update an email notification for a given subscription.
 *SubscriptionsApi* | [**create_subscription**](docs/SubscriptionsApi.md#create_subscription) | **POST** /api/subscriptions | [EXPERIMENTAL] CreateSubscription: Create a new subscription.
 *SubscriptionsApi* | [**delete_subscription**](docs/SubscriptionsApi.md#delete_subscription) | **DELETE** /api/subscriptions/{scope}/{code} | [EXPERIMENTAL] DeleteSubscription: Delete a subscription.
 *SubscriptionsApi* | [**get_subscription**](docs/SubscriptionsApi.md#get_subscription) | **GET** /api/subscriptions/{scope}/{code} | [EXPERIMENTAL] GetSubscription: Get a subscription.
 *SubscriptionsApi* | [**list_subscriptions**](docs/SubscriptionsApi.md#list_subscriptions) | **GET** /api/subscriptions | [EXPERIMENTAL] ListSubscriptions: List subscriptions.
 *SubscriptionsApi* | [**update_subscription**](docs/SubscriptionsApi.md#update_subscription) | **PUT** /api/subscriptions/{scope}/{code} | [EXPERIMENTAL] UpdateSubscription: Update an existing subscription.
 
 
 ## Documentation For Models
 
  - [AccessControlledAction](docs/AccessControlledAction.md)
  - [AccessControlledResource](docs/AccessControlledResource.md)
  - [ActionId](docs/ActionId.md)
  - [Attempt](docs/Attempt.md)
  - [AttemptStatus](docs/AttemptStatus.md)
- - [CreateAwsSqsNotification](docs/CreateAwsSqsNotification.md)
- - [CreateEmailNotification](docs/CreateEmailNotification.md)
- - [CreateSmsNotification](docs/CreateSmsNotification.md)
+ - [CreateNotification](docs/CreateNotification.md)
  - [CreateSubscription](docs/CreateSubscription.md)
- - [CreateWebhookNotification](docs/CreateWebhookNotification.md)
  - [Delivery](docs/Delivery.md)
- - [EventDetails](docs/EventDetails.md)
  - [EventTypeSchema](docs/EventTypeSchema.md)
  - [IdSelectorDefinition](docs/IdSelectorDefinition.md)
  - [IdentifierPartSchema](docs/IdentifierPartSchema.md)
  - [Link](docs/Link.md)
  - [LusidProblemDetails](docs/LusidProblemDetails.md)
  - [LusidValidationProblemDetails](docs/LusidValidationProblemDetails.md)
+ - [ManualEvent](docs/ManualEvent.md)
+ - [ManualEventBody](docs/ManualEventBody.md)
+ - [ManualEventHeader](docs/ManualEventHeader.md)
  - [MatchingPattern](docs/MatchingPattern.md)
  - [Notification](docs/Notification.md)
  - [NotificationStatus](docs/NotificationStatus.md)
  - [ResourceId](docs/ResourceId.md)
  - [ResourceListOfAccessControlledResource](docs/ResourceListOfAccessControlledResource.md)
  - [ResourceListOfDelivery](docs/ResourceListOfDelivery.md)
  - [ResourceListOfEventTypeSchema](docs/ResourceListOfEventTypeSchema.md)
  - [ResourceListOfNotification](docs/ResourceListOfNotification.md)
  - [ResourceListOfSubscription](docs/ResourceListOfSubscription.md)
  - [Subscription](docs/Subscription.md)
  - [SubscriptionDetail](docs/SubscriptionDetail.md)
- - [UpdateAwsSqsNotification](docs/UpdateAwsSqsNotification.md)
- - [UpdateEmailNotification](docs/UpdateEmailNotification.md)
- - [UpdateSmsNotification](docs/UpdateSmsNotification.md)
+ - [UpdateNotification](docs/UpdateNotification.md)
  - [UpdateSubscription](docs/UpdateSubscription.md)
- - [UpdateWebhookNotification](docs/UpdateWebhookNotification.md)
 
 
 ## Documentation For Authorization
 
 
 ## oauth2
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/__init__.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -3,29 +3,29 @@
 # flake8: noqa
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
-__version__ = "0.1.683"
+__version__ = "0.1.683-2"
 
 # import apis into sdk package
 from lusid_notifications.api.application_metadata_api import ApplicationMetadataApi
 from lusid_notifications.api.deliveries_api import DeliveriesApi
 from lusid_notifications.api.event_types_api import EventTypesApi
-from lusid_notifications.api.events_api import EventsApi
+from lusid_notifications.api.manual_event_api import ManualEventApi
 from lusid_notifications.api.notifications_api import NotificationsApi
 from lusid_notifications.api.subscriptions_api import SubscriptionsApi
 
 # import ApiClient
 from lusid_notifications.api_client import ApiClient
 from lusid_notifications.configuration import Configuration
 from lusid_notifications.exceptions import OpenApiException
@@ -35,43 +35,39 @@
 from lusid_notifications.exceptions import ApiException
 # import models into sdk package
 from lusid_notifications.models.access_controlled_action import AccessControlledAction
 from lusid_notifications.models.access_controlled_resource import AccessControlledResource
 from lusid_notifications.models.action_id import ActionId
 from lusid_notifications.models.attempt import Attempt
 from lusid_notifications.models.attempt_status import AttemptStatus
-from lusid_notifications.models.create_aws_sqs_notification import CreateAwsSqsNotification
-from lusid_notifications.models.create_email_notification import CreateEmailNotification
-from lusid_notifications.models.create_sms_notification import CreateSmsNotification
+from lusid_notifications.models.create_notification import CreateNotification
 from lusid_notifications.models.create_subscription import CreateSubscription
-from lusid_notifications.models.create_webhook_notification import CreateWebhookNotification
 from lusid_notifications.models.delivery import Delivery
-from lusid_notifications.models.event_details import EventDetails
 from lusid_notifications.models.event_type_schema import EventTypeSchema
 from lusid_notifications.models.id_selector_definition import IdSelectorDefinition
 from lusid_notifications.models.identifier_part_schema import IdentifierPartSchema
 from lusid_notifications.models.link import Link
 from lusid_notifications.models.lusid_problem_details import LusidProblemDetails
 from lusid_notifications.models.lusid_validation_problem_details import LusidValidationProblemDetails
+from lusid_notifications.models.manual_event import ManualEvent
+from lusid_notifications.models.manual_event_body import ManualEventBody
+from lusid_notifications.models.manual_event_header import ManualEventHeader
 from lusid_notifications.models.matching_pattern import MatchingPattern
 from lusid_notifications.models.notification import Notification
 from lusid_notifications.models.notification_status import NotificationStatus
 from lusid_notifications.models.resource_id import ResourceId
 from lusid_notifications.models.resource_list_of_access_controlled_resource import ResourceListOfAccessControlledResource
 from lusid_notifications.models.resource_list_of_delivery import ResourceListOfDelivery
 from lusid_notifications.models.resource_list_of_event_type_schema import ResourceListOfEventTypeSchema
 from lusid_notifications.models.resource_list_of_notification import ResourceListOfNotification
 from lusid_notifications.models.resource_list_of_subscription import ResourceListOfSubscription
 from lusid_notifications.models.subscription import Subscription
 from lusid_notifications.models.subscription_detail import SubscriptionDetail
-from lusid_notifications.models.update_aws_sqs_notification import UpdateAwsSqsNotification
-from lusid_notifications.models.update_email_notification import UpdateEmailNotification
-from lusid_notifications.models.update_sms_notification import UpdateSmsNotification
+from lusid_notifications.models.update_notification import UpdateNotification
 from lusid_notifications.models.update_subscription import UpdateSubscription
-from lusid_notifications.models.update_webhook_notification import UpdateWebhookNotification
 
 # import utilities into sdk package
 from fbnsdkutilities.utilities.api_client_builder import ApiClientBuilder
 from fbnsdkutilities.utilities.api_configuration import ApiConfiguration
 from fbnsdkutilities.utilities.api_configuration_loader import ApiConfigurationLoader
 from fbnsdkutilities.utilities.refreshing_token import RefreshingToken
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/application_metadata_api.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/application_metadata_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -141,15 +141,15 @@
             ['text/plain', 'application/json', 'text/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "ResourceListOfAccessControlledResource",
         }
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/deliveries_api.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/deliveries_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -179,15 +179,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "ResourceListOfDelivery",
             400: "LusidValidationProblemDetails",
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/event_types_api.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/event_types_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -160,15 +160,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "EventTypeSchema",
             400: "LusidValidationProblemDetails",
@@ -292,15 +292,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "ResourceListOfEventTypeSchema",
             404: "str",
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/events_api.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/manual_event_api.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -19,70 +19,70 @@
 import six
 
 from lusid_notifications.api_client import ApiClient
 from lusid_notifications.exceptions import (  # noqa: F401
     ApiTypeError,
     ApiValueError
 )
-from lusid_notifications.models.event_details import EventDetails
 from lusid_notifications.models.lusid_problem_details import LusidProblemDetails
 from lusid_notifications.models.lusid_validation_problem_details import LusidValidationProblemDetails
+from lusid_notifications.models.manual_event import ManualEvent
 
 
-class EventsApi(object):
+class ManualEventApi(object):
     """NOTE: This class is auto generated by OpenAPI Generator
     Ref: https://openapi-generator.tech
 
     Do not edit the class manually.
     """
 
     def __init__(self, api_client=None):
         if api_client is None:
             api_client = ApiClient()
         self.api_client = api_client
 
-    def create_event(self, body, **kwargs):  # noqa: E501
-        """[EXPERIMENTAL] CreateEvent: Create a new event.  # noqa: E501
+    def trigger_manual_event(self, body, **kwargs):  # noqa: E501
+        """[EXPERIMENTAL] TriggerManualEvent: Trigger a manual event.  # noqa: E501
 
         This method makes a synchronous HTTP request by default. To make an
         asynchronous HTTP request, please pass async_req=True
 
-        >>> thread = api.create_event(body, async_req=True)
+        >>> thread = api.trigger_manual_event(body, async_req=True)
         >>> result = thread.get()
 
-        :param body: The data to create an event. (required)
+        :param body: The data required to trigger a manual event. (required)
         :type body: object
         :param async_req: Whether to execute the request asynchronously.
         :type async_req: bool, optional
         :param _preload_content: if False, the urllib3.HTTPResponse object will
                                  be returned without reading/decoding response
                                  data. Default is True.
         :type _preload_content: bool, optional
         :param _request_timeout: timeout setting for this request. If one
                                  number provided, it will be total request
                                  timeout. It can also be a pair (tuple) of
                                  (connection, read) timeouts.
         :return: Returns the result object.
                  If the method is called asynchronously,
                  returns the request thread.
-        :rtype: EventDetails
+        :rtype: ManualEvent
         """
         kwargs['_return_http_data_only'] = True
-        return self.create_event_with_http_info(body, **kwargs)  # noqa: E501
+        return self.trigger_manual_event_with_http_info(body, **kwargs)  # noqa: E501
 
-    def create_event_with_http_info(self, body, **kwargs):  # noqa: E501
-        """[EXPERIMENTAL] CreateEvent: Create a new event.  # noqa: E501
+    def trigger_manual_event_with_http_info(self, body, **kwargs):  # noqa: E501
+        """[EXPERIMENTAL] TriggerManualEvent: Trigger a manual event.  # noqa: E501
 
         This method makes a synchronous HTTP request by default. To make an
         asynchronous HTTP request, please pass async_req=True
 
-        >>> thread = api.create_event_with_http_info(body, async_req=True)
+        >>> thread = api.trigger_manual_event_with_http_info(body, async_req=True)
         >>> result = thread.get()
 
-        :param body: The data to create an event. (required)
+        :param body: The data required to trigger a manual event. (required)
         :type body: object
         :param async_req: Whether to execute the request asynchronously.
         :type async_req: bool, optional
         :param _return_http_data_only: response data without head status code
                                        and headers
         :type _return_http_data_only: bool, optional
         :param _preload_content: if False, the urllib3.HTTPResponse object will
@@ -96,15 +96,15 @@
         :param _request_auth: set to override the auth_settings for an a single
                               request; this effectively ignores the authentication
                               in the spec for a single request.
         :type _request_auth: dict, optional
         :return: Returns the result object, the HTTP status code, and the headers.
                  If the method is called asynchronously,
                  returns the request thread.
-        :rtype: (EventDetails, int, HTTPHeaderDict)
+        :rtype: (ManualEvent, int, HTTPHeaderDict)
         """
 
         local_var_params = locals()
 
         all_params = [
             'body'
         ]
@@ -119,18 +119,22 @@
             ]
         )
 
         for key, val in six.iteritems(local_var_params['kwargs']):
             if key not in all_params:
                 raise ApiTypeError(
                     "Got an unexpected keyword argument '%s'"
-                    " to method create_event" % key
+                    " to method trigger_manual_event" % key
                 )
             local_var_params[key] = val
         del local_var_params['kwargs']
+        # verify the required parameter 'body' is set
+        if self.api_client.client_side_validation and ('body' not in local_var_params or  # noqa: E501
+                                                        local_var_params['body'] is None):  # noqa: E501
+            raise ApiValueError("Missing the required parameter `body` when calling `trigger_manual_event`")  # noqa: E501
 
         collection_formats = {}
 
         path_params = {}
 
         query_params = []
 
@@ -150,26 +154,26 @@
 
         # HTTP header `Content-Type`
         header_params['Content-Type'] = self.api_client.select_header_content_type(  # noqa: E501
             ['application/json-patch+json', 'application/json', 'text/json', 'application/*+json'])  # noqa: E501
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
-            201: "EventDetails",
+            201: "ManualEvent",
             400: "LusidValidationProblemDetails",
         }
 
         return self.api_client.call_api(
-            '/api/events', 'POST',
+            '/api/manualevent', 'POST',
             path_params,
             query_params,
             header_params,
             body=body_params,
             post_params=form_params,
             files=local_var_files,
             response_types_map=response_types_map,
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api/subscriptions_api.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api/subscriptions_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -158,15 +158,15 @@
 
         # HTTP header `Content-Type`
         header_params['Content-Type'] = self.api_client.select_header_content_type(  # noqa: E501
             ['application/json-patch+json', 'application/json', 'text/json', 'application/*+json'])  # noqa: E501
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             201: "Subscription",
             400: "LusidValidationProblemDetails",
@@ -327,15 +327,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {}
 
         return self.api_client.call_api(
@@ -493,15 +493,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "SubscriptionDetail",
             400: "LusidValidationProblemDetails",
@@ -681,15 +681,15 @@
             ['application/json'])  # noqa: E501
 
         header_params['Accept-Encoding'] = "gzip, deflate, br"
 
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "ResourceListOfSubscription",
             400: "LusidValidationProblemDetails",
@@ -864,15 +864,15 @@
 
         # HTTP header `Content-Type`
         header_params['Content-Type'] = self.api_client.select_header_content_type(  # noqa: E501
             ['application/json-patch+json', 'application/json', 'text/json', 'application/*+json'])  # noqa: E501
 
         # set the LUSID header
         header_params['X-LUSID-SDK-Language'] = 'Python'
-        header_params['X-LUSID-SDK-Version'] = '0.1.683'
+        header_params['X-LUSID-SDK-Version'] = '0.1.683-2'
 
         # Authentication setting
         auth_settings = ['oauth2']  # noqa: E501
 
         response_types_map = {
             200: "Subscription",
             400: "LusidValidationProblemDetails",
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/api_client.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/api_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # coding: utf-8
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 from __future__ import absolute_import
 
 import atexit
@@ -75,15 +75,15 @@
 
         self.rest_client = rest.RESTClientObject(configuration)
         self.default_headers = {}
         if header_name is not None:
             self.default_headers[header_name] = header_value
         self.cookie = cookie
         # Set default User-Agent.
-        self.user_agent = 'OpenAPI-Generator/0.1.683/python'
+        self.user_agent = 'OpenAPI-Generator/0.1.683-2/python'
         self.client_side_validation = configuration.client_side_validation
 
     def __enter__(self):
         return self
 
     def __exit__(self, exc_type, exc_value, traceback):
         self.close()
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/configuration.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/configuration.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -95,15 +95,15 @@
                  server_index=None, server_variables=None,
                  server_operation_index=None, server_operation_variables=None,
                  ssl_ca_cert=None,
                  tcp_keep_alive=False,
                  ):
         """Constructor
         """
-        self._base_path = "https://www.lusid.com/notifications" if host is None else host
+        self._base_path = "https://www.lusid.com/notification" if host is None else host
         """Default Base url
         """
         self.server_index = 0 if server_index is None and host is None else server_index
         self.server_operation_index = server_operation_index or {}
         """Default server index
         """
         self.server_variables = server_variables or {}
@@ -392,26 +392,26 @@
         """Gets the essential information for debugging.
 
         :return: The report for debugging.
         """
         return "Python SDK Debug Report:\n"\
                "OS: {env}\n"\
                "Python Version: {pyversion}\n"\
-               "Version of the API: 0.1.683\n"\
-               "SDK Package Version: 0.1.683".\
+               "Version of the API: 0.1.683-2\n"\
+               "SDK Package Version: 0.1.683-2".\
                format(env=sys.platform, pyversion=sys.version)
 
     def get_host_settings(self):
         """Gets an array of host settings
 
         :return: An array of host settings
         """
         return [
             {
-                'url': "https://www.lusid.com/notifications",
+                'url': "https://www.lusid.com/notification",
                 'description': "No description provided",
             }
         ]
 
     def get_host_from_settings(self, index, variables=None, servers=None):
         """Gets host URL based on the index and variables
         :param index: array index of the host settings
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/exceptions.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/exceptions.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 import six
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/__init__.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/__init__.py`

 * *Files 24% similar despite different names*

```diff
@@ -2,50 +2,46 @@
 
 # flake8: noqa
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
 # import models into model package
 from lusid_notifications.models.access_controlled_action import AccessControlledAction
 from lusid_notifications.models.access_controlled_resource import AccessControlledResource
 from lusid_notifications.models.action_id import ActionId
 from lusid_notifications.models.attempt import Attempt
 from lusid_notifications.models.attempt_status import AttemptStatus
-from lusid_notifications.models.create_aws_sqs_notification import CreateAwsSqsNotification
-from lusid_notifications.models.create_email_notification import CreateEmailNotification
-from lusid_notifications.models.create_sms_notification import CreateSmsNotification
+from lusid_notifications.models.create_notification import CreateNotification
 from lusid_notifications.models.create_subscription import CreateSubscription
-from lusid_notifications.models.create_webhook_notification import CreateWebhookNotification
 from lusid_notifications.models.delivery import Delivery
-from lusid_notifications.models.event_details import EventDetails
 from lusid_notifications.models.event_type_schema import EventTypeSchema
 from lusid_notifications.models.id_selector_definition import IdSelectorDefinition
 from lusid_notifications.models.identifier_part_schema import IdentifierPartSchema
 from lusid_notifications.models.link import Link
 from lusid_notifications.models.lusid_problem_details import LusidProblemDetails
 from lusid_notifications.models.lusid_validation_problem_details import LusidValidationProblemDetails
+from lusid_notifications.models.manual_event import ManualEvent
+from lusid_notifications.models.manual_event_body import ManualEventBody
+from lusid_notifications.models.manual_event_header import ManualEventHeader
 from lusid_notifications.models.matching_pattern import MatchingPattern
 from lusid_notifications.models.notification import Notification
 from lusid_notifications.models.notification_status import NotificationStatus
 from lusid_notifications.models.resource_id import ResourceId
 from lusid_notifications.models.resource_list_of_access_controlled_resource import ResourceListOfAccessControlledResource
 from lusid_notifications.models.resource_list_of_delivery import ResourceListOfDelivery
 from lusid_notifications.models.resource_list_of_event_type_schema import ResourceListOfEventTypeSchema
 from lusid_notifications.models.resource_list_of_notification import ResourceListOfNotification
 from lusid_notifications.models.resource_list_of_subscription import ResourceListOfSubscription
 from lusid_notifications.models.subscription import Subscription
 from lusid_notifications.models.subscription_detail import SubscriptionDetail
-from lusid_notifications.models.update_aws_sqs_notification import UpdateAwsSqsNotification
-from lusid_notifications.models.update_email_notification import UpdateEmailNotification
-from lusid_notifications.models.update_sms_notification import UpdateSmsNotification
+from lusid_notifications.models.update_notification import UpdateNotification
 from lusid_notifications.models.update_subscription import UpdateSubscription
-from lusid_notifications.models.update_webhook_notification import UpdateWebhookNotification
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/access_controlled_action.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/access_controlled_action.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/access_controlled_resource.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/access_controlled_resource.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/action_id.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/action_id.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/attempt.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/attempt.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/attempt_status.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/attempt_status.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_email_notification.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/subscription_detail.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
@@ -18,15 +18,15 @@
 import pprint
 import re  # noqa: F401
 import six
 
 from lusid_notifications.configuration import Configuration
 
 
-class CreateEmailNotification(object):
+class SubscriptionDetail(object):
     """NOTE: This class is auto generated by OpenAPI Generator.
     Ref: https://openapi-generator.tech
 
     Do not edit the class manually.
     """
 
     """
@@ -35,305 +35,327 @@
                             and the value is attribute type.
       attribute_map (dict): The key is attribute name
                             and the value is json key in definition.
       required_map (dict): The key is attribute name
                            and the value is whether it is 'required' or 'optional'.
     """
     openapi_types = {
+        'id': 'ResourceId',
+        'display_name': 'str',
         'description': 'str',
-        'subject': 'str',
-        'plain_text_body': 'str',
-        'html_body': 'str',
-        'email_address_to': 'list[str]',
-        'email_address_cc': 'list[str]',
-        'email_address_bcc': 'list[str]'
+        'status': 'str',
+        'matching_pattern': 'MatchingPattern',
+        'created_at': 'datetime',
+        'user_id_created': 'str',
+        'modified_at': 'datetime',
+        'user_id_modified': 'str'
     }
 
     attribute_map = {
+        'id': 'id',
+        'display_name': 'displayName',
         'description': 'description',
-        'subject': 'subject',
-        'plain_text_body': 'plainTextBody',
-        'html_body': 'htmlBody',
-        'email_address_to': 'emailAddressTo',
-        'email_address_cc': 'emailAddressCc',
-        'email_address_bcc': 'emailAddressBcc'
+        'status': 'status',
+        'matching_pattern': 'matchingPattern',
+        'created_at': 'createdAt',
+        'user_id_created': 'userIdCreated',
+        'modified_at': 'modifiedAt',
+        'user_id_modified': 'userIdModified'
     }
 
     required_map = {
-        'description': 'required',
-        'subject': 'required',
-        'plain_text_body': 'required',
-        'html_body': 'optional',
-        'email_address_to': 'required',
-        'email_address_cc': 'optional',
-        'email_address_bcc': 'optional'
+        'id': 'required',
+        'display_name': 'required',
+        'description': 'optional',
+        'status': 'required',
+        'matching_pattern': 'required',
+        'created_at': 'required',
+        'user_id_created': 'required',
+        'modified_at': 'required',
+        'user_id_modified': 'required'
     }
 
-    def __init__(self, description=None, subject=None, plain_text_body=None, html_body=None, email_address_to=None, email_address_cc=None, email_address_bcc=None, local_vars_configuration=None):  # noqa: E501
-        """CreateEmailNotification - a model defined in OpenAPI"
+    def __init__(self, id=None, display_name=None, description=None, status=None, matching_pattern=None, created_at=None, user_id_created=None, modified_at=None, user_id_modified=None, local_vars_configuration=None):  # noqa: E501
+        """SubscriptionDetail - a model defined in OpenAPI"
         
-        :param description:  The summary of the services provided by the notification (required)
+        :param id:  (required)
+        :type id: lusid_notifications.ResourceId
+        :param display_name:  The name of the subscription (required)
+        :type display_name: str
+        :param description:  The summary of the services provided by the subscription
         :type description: str
-        :param subject:  The subject of the email (required)
-        :type subject: str
-        :param plain_text_body:  The plain text body of the email (required)
-        :type plain_text_body: str
-        :param html_body:  The HTML body of the email (if any)
-        :type html_body: str
-        :param email_address_to:  'To' recipients of the email (required)
-        :type email_address_to: list[str]
-        :param email_address_cc:  'Cc' recipients of the email
-        :type email_address_cc: list[str]
-        :param email_address_bcc:  'Bcc' recipients of the email
-        :type email_address_bcc: list[str]
+        :param status:  The current status of the subscription (required)
+        :type status: str
+        :param matching_pattern:  (required)
+        :type matching_pattern: lusid_notifications.MatchingPattern
+        :param created_at:  The time at which the subscription was made (required)
+        :type created_at: datetime
+        :param user_id_created:  The user who made the subscription (required)
+        :type user_id_created: str
+        :param modified_at:  The time at which the subscription was last modified (required)
+        :type modified_at: datetime
+        :param user_id_modified:  The user who last modified the subscription (required)
+        :type user_id_modified: str
 
         """  # noqa: E501
         if local_vars_configuration is None:
             local_vars_configuration = Configuration.get_default_copy()
         self.local_vars_configuration = local_vars_configuration
 
+        self._id = None
+        self._display_name = None
         self._description = None
-        self._subject = None
-        self._plain_text_body = None
-        self._html_body = None
-        self._email_address_to = None
-        self._email_address_cc = None
-        self._email_address_bcc = None
+        self._status = None
+        self._matching_pattern = None
+        self._created_at = None
+        self._user_id_created = None
+        self._modified_at = None
+        self._user_id_modified = None
         self.discriminator = None
 
+        self.id = id
+        self.display_name = display_name
         self.description = description
-        self.subject = subject
-        self.plain_text_body = plain_text_body
-        self.html_body = html_body
-        self.email_address_to = email_address_to
-        self.email_address_cc = email_address_cc
-        self.email_address_bcc = email_address_bcc
+        self.status = status
+        self.matching_pattern = matching_pattern
+        self.created_at = created_at
+        self.user_id_created = user_id_created
+        self.modified_at = modified_at
+        self.user_id_modified = user_id_modified
+
+    @property
+    def id(self):
+        """Gets the id of this SubscriptionDetail.  # noqa: E501
+
+
+        :return: The id of this SubscriptionDetail.  # noqa: E501
+        :rtype: lusid_notifications.ResourceId
+        """
+        return self._id
+
+    @id.setter
+    def id(self, id):
+        """Sets the id of this SubscriptionDetail.
+
+
+        :param id: The id of this SubscriptionDetail.  # noqa: E501
+        :type id: lusid_notifications.ResourceId
+        """
+        if self.local_vars_configuration.client_side_validation and id is None:  # noqa: E501
+            raise ValueError("Invalid value for `id`, must not be `None`")  # noqa: E501
+
+        self._id = id
+
+    @property
+    def display_name(self):
+        """Gets the display_name of this SubscriptionDetail.  # noqa: E501
+
+        The name of the subscription  # noqa: E501
+
+        :return: The display_name of this SubscriptionDetail.  # noqa: E501
+        :rtype: str
+        """
+        return self._display_name
+
+    @display_name.setter
+    def display_name(self, display_name):
+        """Sets the display_name of this SubscriptionDetail.
+
+        The name of the subscription  # noqa: E501
+
+        :param display_name: The display_name of this SubscriptionDetail.  # noqa: E501
+        :type display_name: str
+        """
+        if self.local_vars_configuration.client_side_validation and display_name is None:  # noqa: E501
+            raise ValueError("Invalid value for `display_name`, must not be `None`")  # noqa: E501
+        if (self.local_vars_configuration.client_side_validation and
+                display_name is not None and len(display_name) < 1):
+            raise ValueError("Invalid value for `display_name`, length must be greater than or equal to `1`")  # noqa: E501
+
+        self._display_name = display_name
 
     @property
     def description(self):
-        """Gets the description of this CreateEmailNotification.  # noqa: E501
+        """Gets the description of this SubscriptionDetail.  # noqa: E501
 
-        The summary of the services provided by the notification  # noqa: E501
+        The summary of the services provided by the subscription  # noqa: E501
 
-        :return: The description of this CreateEmailNotification.  # noqa: E501
+        :return: The description of this SubscriptionDetail.  # noqa: E501
         :rtype: str
         """
         return self._description
 
     @description.setter
     def description(self, description):
-        """Sets the description of this CreateEmailNotification.
+        """Sets the description of this SubscriptionDetail.
 
-        The summary of the services provided by the notification  # noqa: E501
+        The summary of the services provided by the subscription  # noqa: E501
 
-        :param description: The description of this CreateEmailNotification.  # noqa: E501
+        :param description: The description of this SubscriptionDetail.  # noqa: E501
         :type description: str
         """
-        if self.local_vars_configuration.client_side_validation and description is None:  # noqa: E501
-            raise ValueError("Invalid value for `description`, must not be `None`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                description is not None and len(description) > 512):
-            raise ValueError("Invalid value for `description`, length must be less than or equal to `512`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                description is not None and len(description) < 1):
-            raise ValueError("Invalid value for `description`, length must be greater than or equal to `1`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                description is not None and not re.search(r'^[\s\S]*$', description)):  # noqa: E501
-            raise ValueError(r"Invalid value for `description`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
 
         self._description = description
 
     @property
-    def subject(self):
-        """Gets the subject of this CreateEmailNotification.  # noqa: E501
+    def status(self):
+        """Gets the status of this SubscriptionDetail.  # noqa: E501
 
-        The subject of the email  # noqa: E501
+        The current status of the subscription  # noqa: E501
 
-        :return: The subject of this CreateEmailNotification.  # noqa: E501
+        :return: The status of this SubscriptionDetail.  # noqa: E501
         :rtype: str
         """
-        return self._subject
+        return self._status
 
-    @subject.setter
-    def subject(self, subject):
-        """Sets the subject of this CreateEmailNotification.
+    @status.setter
+    def status(self, status):
+        """Sets the status of this SubscriptionDetail.
 
-        The subject of the email  # noqa: E501
+        The current status of the subscription  # noqa: E501
 
-        :param subject: The subject of this CreateEmailNotification.  # noqa: E501
-        :type subject: str
+        :param status: The status of this SubscriptionDetail.  # noqa: E501
+        :type status: str
         """
-        if self.local_vars_configuration.client_side_validation and subject is None:  # noqa: E501
-            raise ValueError("Invalid value for `subject`, must not be `None`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                subject is not None and len(subject) > 1024):
-            raise ValueError("Invalid value for `subject`, length must be less than or equal to `1024`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and status is None:  # noqa: E501
+            raise ValueError("Invalid value for `status`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                subject is not None and len(subject) < 1):
-            raise ValueError("Invalid value for `subject`, length must be greater than or equal to `1`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                subject is not None and not re.search(r'^[\s\S]*$', subject)):  # noqa: E501
-            raise ValueError(r"Invalid value for `subject`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+                status is not None and len(status) < 1):
+            raise ValueError("Invalid value for `status`, length must be greater than or equal to `1`")  # noqa: E501
 
-        self._subject = subject
+        self._status = status
 
     @property
-    def plain_text_body(self):
-        """Gets the plain_text_body of this CreateEmailNotification.  # noqa: E501
+    def matching_pattern(self):
+        """Gets the matching_pattern of this SubscriptionDetail.  # noqa: E501
 
-        The plain text body of the email  # noqa: E501
 
-        :return: The plain_text_body of this CreateEmailNotification.  # noqa: E501
-        :rtype: str
+        :return: The matching_pattern of this SubscriptionDetail.  # noqa: E501
+        :rtype: lusid_notifications.MatchingPattern
         """
-        return self._plain_text_body
+        return self._matching_pattern
 
-    @plain_text_body.setter
-    def plain_text_body(self, plain_text_body):
-        """Sets the plain_text_body of this CreateEmailNotification.
+    @matching_pattern.setter
+    def matching_pattern(self, matching_pattern):
+        """Sets the matching_pattern of this SubscriptionDetail.
 
-        The plain text body of the email  # noqa: E501
 
-        :param plain_text_body: The plain_text_body of this CreateEmailNotification.  # noqa: E501
-        :type plain_text_body: str
+        :param matching_pattern: The matching_pattern of this SubscriptionDetail.  # noqa: E501
+        :type matching_pattern: lusid_notifications.MatchingPattern
         """
-        if self.local_vars_configuration.client_side_validation and plain_text_body is None:  # noqa: E501
-            raise ValueError("Invalid value for `plain_text_body`, must not be `None`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                plain_text_body is not None and len(plain_text_body) > 2147483647):
-            raise ValueError("Invalid value for `plain_text_body`, length must be less than or equal to `2147483647`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                plain_text_body is not None and len(plain_text_body) < 1):
-            raise ValueError("Invalid value for `plain_text_body`, length must be greater than or equal to `1`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                plain_text_body is not None and not re.search(r'^[\s\S]*$', plain_text_body)):  # noqa: E501
-            raise ValueError(r"Invalid value for `plain_text_body`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and matching_pattern is None:  # noqa: E501
+            raise ValueError("Invalid value for `matching_pattern`, must not be `None`")  # noqa: E501
 
-        self._plain_text_body = plain_text_body
+        self._matching_pattern = matching_pattern
 
     @property
-    def html_body(self):
-        """Gets the html_body of this CreateEmailNotification.  # noqa: E501
+    def created_at(self):
+        """Gets the created_at of this SubscriptionDetail.  # noqa: E501
 
-        The HTML body of the email (if any)  # noqa: E501
+        The time at which the subscription was made  # noqa: E501
 
-        :return: The html_body of this CreateEmailNotification.  # noqa: E501
-        :rtype: str
+        :return: The created_at of this SubscriptionDetail.  # noqa: E501
+        :rtype: datetime
         """
-        return self._html_body
+        return self._created_at
 
-    @html_body.setter
-    def html_body(self, html_body):
-        """Sets the html_body of this CreateEmailNotification.
+    @created_at.setter
+    def created_at(self, created_at):
+        """Sets the created_at of this SubscriptionDetail.
 
-        The HTML body of the email (if any)  # noqa: E501
+        The time at which the subscription was made  # noqa: E501
 
-        :param html_body: The html_body of this CreateEmailNotification.  # noqa: E501
-        :type html_body: str
+        :param created_at: The created_at of this SubscriptionDetail.  # noqa: E501
+        :type created_at: datetime
         """
-        if (self.local_vars_configuration.client_side_validation and
-                html_body is not None and len(html_body) > 2147483647):
-            raise ValueError("Invalid value for `html_body`, length must be less than or equal to `2147483647`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                html_body is not None and len(html_body) < 1):
-            raise ValueError("Invalid value for `html_body`, length must be greater than or equal to `1`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                html_body is not None and not re.search(r'^[\s\S]*$', html_body)):  # noqa: E501
-            raise ValueError(r"Invalid value for `html_body`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and created_at is None:  # noqa: E501
+            raise ValueError("Invalid value for `created_at`, must not be `None`")  # noqa: E501
 
-        self._html_body = html_body
+        self._created_at = created_at
 
     @property
-    def email_address_to(self):
-        """Gets the email_address_to of this CreateEmailNotification.  # noqa: E501
+    def user_id_created(self):
+        """Gets the user_id_created of this SubscriptionDetail.  # noqa: E501
 
-        'To' recipients of the email  # noqa: E501
+        The user who made the subscription  # noqa: E501
 
-        :return: The email_address_to of this CreateEmailNotification.  # noqa: E501
-        :rtype: list[str]
+        :return: The user_id_created of this SubscriptionDetail.  # noqa: E501
+        :rtype: str
         """
-        return self._email_address_to
+        return self._user_id_created
 
-    @email_address_to.setter
-    def email_address_to(self, email_address_to):
-        """Sets the email_address_to of this CreateEmailNotification.
+    @user_id_created.setter
+    def user_id_created(self, user_id_created):
+        """Sets the user_id_created of this SubscriptionDetail.
 
-        'To' recipients of the email  # noqa: E501
+        The user who made the subscription  # noqa: E501
 
-        :param email_address_to: The email_address_to of this CreateEmailNotification.  # noqa: E501
-        :type email_address_to: list[str]
+        :param user_id_created: The user_id_created of this SubscriptionDetail.  # noqa: E501
+        :type user_id_created: str
         """
-        if self.local_vars_configuration.client_side_validation and email_address_to is None:  # noqa: E501
-            raise ValueError("Invalid value for `email_address_to`, must not be `None`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and user_id_created is None:  # noqa: E501
+            raise ValueError("Invalid value for `user_id_created`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                email_address_to is not None and len(email_address_to) > 10):
-            raise ValueError("Invalid value for `email_address_to`, number of items must be less than or equal to `10`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                email_address_to is not None and len(email_address_to) < 1):
-            raise ValueError("Invalid value for `email_address_to`, number of items must be greater than or equal to `1`")  # noqa: E501
+                user_id_created is not None and len(user_id_created) < 1):
+            raise ValueError("Invalid value for `user_id_created`, length must be greater than or equal to `1`")  # noqa: E501
 
-        self._email_address_to = email_address_to
+        self._user_id_created = user_id_created
 
     @property
-    def email_address_cc(self):
-        """Gets the email_address_cc of this CreateEmailNotification.  # noqa: E501
+    def modified_at(self):
+        """Gets the modified_at of this SubscriptionDetail.  # noqa: E501
 
-        'Cc' recipients of the email  # noqa: E501
+        The time at which the subscription was last modified  # noqa: E501
 
-        :return: The email_address_cc of this CreateEmailNotification.  # noqa: E501
-        :rtype: list[str]
+        :return: The modified_at of this SubscriptionDetail.  # noqa: E501
+        :rtype: datetime
         """
-        return self._email_address_cc
+        return self._modified_at
 
-    @email_address_cc.setter
-    def email_address_cc(self, email_address_cc):
-        """Sets the email_address_cc of this CreateEmailNotification.
+    @modified_at.setter
+    def modified_at(self, modified_at):
+        """Sets the modified_at of this SubscriptionDetail.
 
-        'Cc' recipients of the email  # noqa: E501
+        The time at which the subscription was last modified  # noqa: E501
 
-        :param email_address_cc: The email_address_cc of this CreateEmailNotification.  # noqa: E501
-        :type email_address_cc: list[str]
+        :param modified_at: The modified_at of this SubscriptionDetail.  # noqa: E501
+        :type modified_at: datetime
         """
-        if (self.local_vars_configuration.client_side_validation and
-                email_address_cc is not None and len(email_address_cc) > 10):
-            raise ValueError("Invalid value for `email_address_cc`, number of items must be less than or equal to `10`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                email_address_cc is not None and len(email_address_cc) < 0):
-            raise ValueError("Invalid value for `email_address_cc`, number of items must be greater than or equal to `0`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and modified_at is None:  # noqa: E501
+            raise ValueError("Invalid value for `modified_at`, must not be `None`")  # noqa: E501
 
-        self._email_address_cc = email_address_cc
+        self._modified_at = modified_at
 
     @property
-    def email_address_bcc(self):
-        """Gets the email_address_bcc of this CreateEmailNotification.  # noqa: E501
+    def user_id_modified(self):
+        """Gets the user_id_modified of this SubscriptionDetail.  # noqa: E501
 
-        'Bcc' recipients of the email  # noqa: E501
+        The user who last modified the subscription  # noqa: E501
 
-        :return: The email_address_bcc of this CreateEmailNotification.  # noqa: E501
-        :rtype: list[str]
+        :return: The user_id_modified of this SubscriptionDetail.  # noqa: E501
+        :rtype: str
         """
-        return self._email_address_bcc
+        return self._user_id_modified
 
-    @email_address_bcc.setter
-    def email_address_bcc(self, email_address_bcc):
-        """Sets the email_address_bcc of this CreateEmailNotification.
+    @user_id_modified.setter
+    def user_id_modified(self, user_id_modified):
+        """Sets the user_id_modified of this SubscriptionDetail.
 
-        'Bcc' recipients of the email  # noqa: E501
+        The user who last modified the subscription  # noqa: E501
 
-        :param email_address_bcc: The email_address_bcc of this CreateEmailNotification.  # noqa: E501
-        :type email_address_bcc: list[str]
+        :param user_id_modified: The user_id_modified of this SubscriptionDetail.  # noqa: E501
+        :type user_id_modified: str
         """
+        if self.local_vars_configuration.client_side_validation and user_id_modified is None:  # noqa: E501
+            raise ValueError("Invalid value for `user_id_modified`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                email_address_bcc is not None and len(email_address_bcc) > 10):
-            raise ValueError("Invalid value for `email_address_bcc`, number of items must be less than or equal to `10`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                email_address_bcc is not None and len(email_address_bcc) < 0):
-            raise ValueError("Invalid value for `email_address_bcc`, number of items must be greater than or equal to `0`")  # noqa: E501
+                user_id_modified is not None and len(user_id_modified) < 1):
+            raise ValueError("Invalid value for `user_id_modified`, length must be greater than or equal to `1`")  # noqa: E501
 
-        self._email_address_bcc = email_address_bcc
+        self._user_id_modified = user_id_modified
 
     def to_dict(self, serialize=False):
         """Returns the model properties as a dict"""
         result = {}
 
         def convert(x):
             if hasattr(x, "to_dict"):
@@ -369,18 +391,18 @@
 
     def __repr__(self):
         """For `print` and `pprint`"""
         return self.to_str()
 
     def __eq__(self, other):
         """Returns true if both objects are equal"""
-        if not isinstance(other, CreateEmailNotification):
+        if not isinstance(other, SubscriptionDetail):
             return False
 
         return self.to_dict() == other.to_dict()
 
     def __ne__(self, other):
         """Returns true if both objects are not equal"""
-        if not isinstance(other, CreateEmailNotification):
+        if not isinstance(other, SubscriptionDetail):
             return True
 
         return self.to_dict() != other.to_dict()
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_sms_notification.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/matching_pattern.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
@@ -18,15 +18,15 @@
 import pprint
 import re  # noqa: F401
 import six
 
 from lusid_notifications.configuration import Configuration
 
 
-class CreateSmsNotification(object):
+class MatchingPattern(object):
     """NOTE: This class is auto generated by OpenAPI Generator.
     Ref: https://openapi-generator.tech
 
     Do not edit the class manually.
     """
 
     """
@@ -35,153 +35,113 @@
                             and the value is attribute type.
       attribute_map (dict): The key is attribute name
                             and the value is json key in definition.
       required_map (dict): The key is attribute name
                            and the value is whether it is 'required' or 'optional'.
     """
     openapi_types = {
-        'description': 'str',
-        'body': 'str',
-        'recipients': 'list[str]'
+        'event_type': 'str',
+        'filter': 'str'
     }
 
     attribute_map = {
-        'description': 'description',
-        'body': 'body',
-        'recipients': 'recipients'
+        'event_type': 'eventType',
+        'filter': 'filter'
     }
 
     required_map = {
-        'description': 'required',
-        'body': 'required',
-        'recipients': 'required'
+        'event_type': 'required',
+        'filter': 'optional'
     }
 
-    def __init__(self, description=None, body=None, recipients=None, local_vars_configuration=None):  # noqa: E501
-        """CreateSmsNotification - a model defined in OpenAPI"
+    def __init__(self, event_type=None, filter=None, local_vars_configuration=None):  # noqa: E501
+        """MatchingPattern - a model defined in OpenAPI"
         
-        :param description:  The summary of the services provided by the notification (required)
-        :type description: str
-        :param body:  The body of the SMS (required)
-        :type body: str
-        :param recipients:  The phone numbers to which the SMS will be sent to (E.164 format) (required)
-        :type recipients: list[str]
+        :param event_type:  The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType (required)
+        :type event_type: str
+        :param filter:  A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched
+        :type filter: str
 
         """  # noqa: E501
         if local_vars_configuration is None:
             local_vars_configuration = Configuration.get_default_copy()
         self.local_vars_configuration = local_vars_configuration
 
-        self._description = None
-        self._body = None
-        self._recipients = None
+        self._event_type = None
+        self._filter = None
         self.discriminator = None
 
-        self.description = description
-        self.body = body
-        self.recipients = recipients
+        self.event_type = event_type
+        self.filter = filter
 
     @property
-    def description(self):
-        """Gets the description of this CreateSmsNotification.  # noqa: E501
+    def event_type(self):
+        """Gets the event_type of this MatchingPattern.  # noqa: E501
 
-        The summary of the services provided by the notification  # noqa: E501
+        The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType  # noqa: E501
 
-        :return: The description of this CreateSmsNotification.  # noqa: E501
+        :return: The event_type of this MatchingPattern.  # noqa: E501
         :rtype: str
         """
-        return self._description
+        return self._event_type
 
-    @description.setter
-    def description(self, description):
-        """Sets the description of this CreateSmsNotification.
+    @event_type.setter
+    def event_type(self, event_type):
+        """Sets the event_type of this MatchingPattern.
 
-        The summary of the services provided by the notification  # noqa: E501
+        The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType  # noqa: E501
 
-        :param description: The description of this CreateSmsNotification.  # noqa: E501
-        :type description: str
+        :param event_type: The event_type of this MatchingPattern.  # noqa: E501
+        :type event_type: str
         """
-        if self.local_vars_configuration.client_side_validation and description is None:  # noqa: E501
-            raise ValueError("Invalid value for `description`, must not be `None`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and event_type is None:  # noqa: E501
+            raise ValueError("Invalid value for `event_type`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                description is not None and len(description) > 512):
-            raise ValueError("Invalid value for `description`, length must be less than or equal to `512`")  # noqa: E501
+                event_type is not None and len(event_type) > 512):
+            raise ValueError("Invalid value for `event_type`, length must be less than or equal to `512`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                description is not None and len(description) < 1):
-            raise ValueError("Invalid value for `description`, length must be greater than or equal to `1`")  # noqa: E501
+                event_type is not None and len(event_type) < 0):
+            raise ValueError("Invalid value for `event_type`, length must be greater than or equal to `0`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                description is not None and not re.search(r'^[\s\S]*$', description)):  # noqa: E501
-            raise ValueError(r"Invalid value for `description`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+                event_type is not None and not re.search(r'^[a-zA-Z]*$', event_type)):  # noqa: E501
+            raise ValueError(r"Invalid value for `event_type`, must be a follow pattern or equal to `/^[a-zA-Z]*$/`")  # noqa: E501
 
-        self._description = description
+        self._event_type = event_type
 
     @property
-    def body(self):
-        """Gets the body of this CreateSmsNotification.  # noqa: E501
+    def filter(self):
+        """Gets the filter of this MatchingPattern.  # noqa: E501
 
-        The body of the SMS  # noqa: E501
+        A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched  # noqa: E501
 
-        :return: The body of this CreateSmsNotification.  # noqa: E501
+        :return: The filter of this MatchingPattern.  # noqa: E501
         :rtype: str
         """
-        return self._body
+        return self._filter
 
-    @body.setter
-    def body(self, body):
-        """Sets the body of this CreateSmsNotification.
+    @filter.setter
+    def filter(self, filter):
+        """Sets the filter of this MatchingPattern.
 
-        The body of the SMS  # noqa: E501
+        A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched  # noqa: E501
 
-        :param body: The body of this CreateSmsNotification.  # noqa: E501
-        :type body: str
+        :param filter: The filter of this MatchingPattern.  # noqa: E501
+        :type filter: str
         """
-        if self.local_vars_configuration.client_side_validation and body is None:  # noqa: E501
-            raise ValueError("Invalid value for `body`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                body is not None and len(body) > 1024):
-            raise ValueError("Invalid value for `body`, length must be less than or equal to `1024`")  # noqa: E501
+                filter is not None and len(filter) > 16384):
+            raise ValueError("Invalid value for `filter`, length must be less than or equal to `16384`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                body is not None and len(body) < 1):
-            raise ValueError("Invalid value for `body`, length must be greater than or equal to `1`")  # noqa: E501
+                filter is not None and len(filter) < 0):
+            raise ValueError("Invalid value for `filter`, length must be greater than or equal to `0`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                body is not None and not re.search(r'^[\s\S]*$', body)):  # noqa: E501
-            raise ValueError(r"Invalid value for `body`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+                filter is not None and not re.search(r'^[\s\S]*$', filter)):  # noqa: E501
+            raise ValueError(r"Invalid value for `filter`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
 
-        self._body = body
-
-    @property
-    def recipients(self):
-        """Gets the recipients of this CreateSmsNotification.  # noqa: E501
-
-        The phone numbers to which the SMS will be sent to (E.164 format)  # noqa: E501
-
-        :return: The recipients of this CreateSmsNotification.  # noqa: E501
-        :rtype: list[str]
-        """
-        return self._recipients
-
-    @recipients.setter
-    def recipients(self, recipients):
-        """Sets the recipients of this CreateSmsNotification.
-
-        The phone numbers to which the SMS will be sent to (E.164 format)  # noqa: E501
-
-        :param recipients: The recipients of this CreateSmsNotification.  # noqa: E501
-        :type recipients: list[str]
-        """
-        if self.local_vars_configuration.client_side_validation and recipients is None:  # noqa: E501
-            raise ValueError("Invalid value for `recipients`, must not be `None`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                recipients is not None and len(recipients) > 10):
-            raise ValueError("Invalid value for `recipients`, number of items must be less than or equal to `10`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                recipients is not None and len(recipients) < 1):
-            raise ValueError("Invalid value for `recipients`, number of items must be greater than or equal to `1`")  # noqa: E501
-
-        self._recipients = recipients
+        self._filter = filter
 
     def to_dict(self, serialize=False):
         """Returns the model properties as a dict"""
         result = {}
 
         def convert(x):
             if hasattr(x, "to_dict"):
@@ -217,18 +177,18 @@
 
     def __repr__(self):
         """For `print` and `pprint`"""
         return self.to_str()
 
     def __eq__(self, other):
         """Returns true if both objects are equal"""
-        if not isinstance(other, CreateSmsNotification):
+        if not isinstance(other, MatchingPattern):
             return False
 
         return self.to_dict() == other.to_dict()
 
     def __ne__(self, other):
         """Returns true if both objects are not equal"""
-        if not isinstance(other, CreateSmsNotification):
+        if not isinstance(other, MatchingPattern):
             return True
 
         return self.to_dict() != other.to_dict()
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/create_subscription.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/create_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/delivery.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/delivery.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/event_type_schema.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/event_type_schema.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
@@ -36,74 +36,81 @@
       attribute_map (dict): The key is attribute name
                             and the value is json key in definition.
       required_map (dict): The key is attribute name
                            and the value is whether it is 'required' or 'optional'.
     """
     openapi_types = {
         'id': 'str',
-        'event_name': 'str',
+        'display_name': 'str',
         'description': 'str',
         'entity': 'str',
         'application': 'str',
-        'json_schema': 'object'
+        'json_schema': 'object',
+        'href': 'str'
     }
 
     attribute_map = {
         'id': 'id',
-        'event_name': 'eventName',
+        'display_name': 'displayName',
         'description': 'description',
         'entity': 'entity',
         'application': 'application',
-        'json_schema': 'jsonSchema'
+        'json_schema': 'jsonSchema',
+        'href': 'href'
     }
 
     required_map = {
         'id': 'optional',
-        'event_name': 'optional',
+        'display_name': 'optional',
         'description': 'optional',
         'entity': 'optional',
         'application': 'optional',
-        'json_schema': 'required'
+        'json_schema': 'required',
+        'href': 'optional'
     }
 
-    def __init__(self, id=None, event_name=None, description=None, entity=None, application=None, json_schema=None, local_vars_configuration=None):  # noqa: E501
+    def __init__(self, id=None, display_name=None, description=None, entity=None, application=None, json_schema=None, href=None, local_vars_configuration=None):  # noqa: E501
         """EventTypeSchema - a model defined in OpenAPI"
         
         :param id:  The identifier of the event type
         :type id: str
-        :param event_name:  Identifier name of the event
-        :type event_name: str
+        :param display_name:  Identifier name of the event
+        :type display_name: str
         :param description:  The summary of the event
         :type description: str
         :param entity:  The entity against which the event originated
         :type entity: str
         :param application:  The application associated with the event
         :type application: str
         :param json_schema:  The schema of the event (required)
         :type json_schema: object
+        :param href:  A URI for retrieving this schema
+        :type href: str
 
         """  # noqa: E501
         if local_vars_configuration is None:
             local_vars_configuration = Configuration.get_default_copy()
         self.local_vars_configuration = local_vars_configuration
 
         self._id = None
-        self._event_name = None
+        self._display_name = None
         self._description = None
         self._entity = None
         self._application = None
         self._json_schema = None
+        self._href = None
         self.discriminator = None
 
         self.id = id
-        self.event_name = event_name
+        self.display_name = display_name
         self.description = description
         self.entity = entity
         self.application = application
         self.json_schema = json_schema
+        self.href = href
 
     @property
     def id(self):
         """Gets the id of this EventTypeSchema.  # noqa: E501
 
         The identifier of the event type  # noqa: E501
 
@@ -121,35 +128,35 @@
         :param id: The id of this EventTypeSchema.  # noqa: E501
         :type id: str
         """
 
         self._id = id
 
     @property
-    def event_name(self):
-        """Gets the event_name of this EventTypeSchema.  # noqa: E501
+    def display_name(self):
+        """Gets the display_name of this EventTypeSchema.  # noqa: E501
 
         Identifier name of the event  # noqa: E501
 
-        :return: The event_name of this EventTypeSchema.  # noqa: E501
+        :return: The display_name of this EventTypeSchema.  # noqa: E501
         :rtype: str
         """
-        return self._event_name
+        return self._display_name
 
-    @event_name.setter
-    def event_name(self, event_name):
-        """Sets the event_name of this EventTypeSchema.
+    @display_name.setter
+    def display_name(self, display_name):
+        """Sets the display_name of this EventTypeSchema.
 
         Identifier name of the event  # noqa: E501
 
-        :param event_name: The event_name of this EventTypeSchema.  # noqa: E501
-        :type event_name: str
+        :param display_name: The display_name of this EventTypeSchema.  # noqa: E501
+        :type display_name: str
         """
 
-        self._event_name = event_name
+        self._display_name = display_name
 
     @property
     def description(self):
         """Gets the description of this EventTypeSchema.  # noqa: E501
 
         The summary of the event  # noqa: E501
 
@@ -235,14 +242,37 @@
 
         :param json_schema: The json_schema of this EventTypeSchema.  # noqa: E501
         :type json_schema: object
         """
 
         self._json_schema = json_schema
 
+    @property
+    def href(self):
+        """Gets the href of this EventTypeSchema.  # noqa: E501
+
+        A URI for retrieving this schema  # noqa: E501
+
+        :return: The href of this EventTypeSchema.  # noqa: E501
+        :rtype: str
+        """
+        return self._href
+
+    @href.setter
+    def href(self, href):
+        """Sets the href of this EventTypeSchema.
+
+        A URI for retrieving this schema  # noqa: E501
+
+        :param href: The href of this EventTypeSchema.  # noqa: E501
+        :type href: str
+        """
+
+        self._href = href
+
     def to_dict(self, serialize=False):
         """Returns the model properties as a dict"""
         result = {}
 
         def convert(x):
             if hasattr(x, "to_dict"):
                 args = getfullargspec(x.to_dict).args
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/id_selector_definition.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/id_selector_definition.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/identifier_part_schema.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/identifier_part_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/link.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/link.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/lusid_problem_details.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/lusid_problem_details.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/lusid_validation_problem_details.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/lusid_validation_problem_details.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/matching_pattern.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/manual_event_header.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
@@ -18,15 +18,15 @@
 import pprint
 import re  # noqa: F401
 import six
 
 from lusid_notifications.configuration import Configuration
 
 
-class MatchingPattern(object):
+class ManualEventHeader(object):
     """NOTE: This class is auto generated by OpenAPI Generator.
     Ref: https://openapi-generator.tech
 
     Do not edit the class manually.
     """
 
     """
@@ -35,113 +35,154 @@
                             and the value is attribute type.
       attribute_map (dict): The key is attribute name
                             and the value is json key in definition.
       required_map (dict): The key is attribute name
                            and the value is whether it is 'required' or 'optional'.
     """
     openapi_types = {
-        'event_type': 'str',
-        'filter': 'str'
+        'timestamp': 'datetime',
+        'event_id': 'str',
+        'user_id': 'str',
+        'request_id': 'str'
     }
 
     attribute_map = {
-        'event_type': 'eventType',
-        'filter': 'filter'
+        'timestamp': 'timestamp',
+        'event_id': 'eventId',
+        'user_id': 'userId',
+        'request_id': 'requestId'
     }
 
     required_map = {
-        'event_type': 'required',
-        'filter': 'optional'
+        'timestamp': 'optional',
+        'event_id': 'optional',
+        'user_id': 'optional',
+        'request_id': 'optional'
     }
 
-    def __init__(self, event_type=None, filter=None, local_vars_configuration=None):  # noqa: E501
-        """MatchingPattern - a model defined in OpenAPI"
+    def __init__(self, timestamp=None, event_id=None, user_id=None, request_id=None, local_vars_configuration=None):  # noqa: E501
+        """ManualEventHeader - a model defined in OpenAPI"
         
-        :param event_type:  The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType (required)
-        :type event_type: str
-        :param filter:  A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched
-        :type filter: str
+        :param timestamp:  The timestamp of the manual event
+        :type timestamp: datetime
+        :param event_id:  The event ID of the manual event
+        :type event_id: str
+        :param user_id:  The user ID of the manual event
+        :type user_id: str
+        :param request_id:  The request ID of the manual event
+        :type request_id: str
 
         """  # noqa: E501
         if local_vars_configuration is None:
             local_vars_configuration = Configuration.get_default_copy()
         self.local_vars_configuration = local_vars_configuration
 
-        self._event_type = None
-        self._filter = None
+        self._timestamp = None
+        self._event_id = None
+        self._user_id = None
+        self._request_id = None
         self.discriminator = None
 
-        self.event_type = event_type
-        self.filter = filter
+        if timestamp is not None:
+            self.timestamp = timestamp
+        self.event_id = event_id
+        self.user_id = user_id
+        self.request_id = request_id
 
     @property
-    def event_type(self):
-        """Gets the event_type of this MatchingPattern.  # noqa: E501
+    def timestamp(self):
+        """Gets the timestamp of this ManualEventHeader.  # noqa: E501
 
-        The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType  # noqa: E501
+        The timestamp of the manual event  # noqa: E501
 
-        :return: The event_type of this MatchingPattern.  # noqa: E501
+        :return: The timestamp of this ManualEventHeader.  # noqa: E501
+        :rtype: datetime
+        """
+        return self._timestamp
+
+    @timestamp.setter
+    def timestamp(self, timestamp):
+        """Sets the timestamp of this ManualEventHeader.
+
+        The timestamp of the manual event  # noqa: E501
+
+        :param timestamp: The timestamp of this ManualEventHeader.  # noqa: E501
+        :type timestamp: datetime
+        """
+
+        self._timestamp = timestamp
+
+    @property
+    def event_id(self):
+        """Gets the event_id of this ManualEventHeader.  # noqa: E501
+
+        The event ID of the manual event  # noqa: E501
+
+        :return: The event_id of this ManualEventHeader.  # noqa: E501
         :rtype: str
         """
-        return self._event_type
+        return self._event_id
 
-    @event_type.setter
-    def event_type(self, event_type):
-        """Sets the event_type of this MatchingPattern.
-
-        The type of event to subscribe to. Possible values are: Finbourne.Notifications.WebApi.Dtos.MatchingPattern.EventType  # noqa: E501
-
-        :param event_type: The event_type of this MatchingPattern.  # noqa: E501
-        :type event_type: str
-        """
-        if self.local_vars_configuration.client_side_validation and event_type is None:  # noqa: E501
-            raise ValueError("Invalid value for `event_type`, must not be `None`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                event_type is not None and len(event_type) > 512):
-            raise ValueError("Invalid value for `event_type`, length must be less than or equal to `512`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                event_type is not None and len(event_type) < 0):
-            raise ValueError("Invalid value for `event_type`, length must be greater than or equal to `0`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                event_type is not None and not re.search(r'^[a-zA-Z]*$', event_type)):  # noqa: E501
-            raise ValueError(r"Invalid value for `event_type`, must be a follow pattern or equal to `/^[a-zA-Z]*$/`")  # noqa: E501
+    @event_id.setter
+    def event_id(self, event_id):
+        """Sets the event_id of this ManualEventHeader.
 
-        self._event_type = event_type
+        The event ID of the manual event  # noqa: E501
+
+        :param event_id: The event_id of this ManualEventHeader.  # noqa: E501
+        :type event_id: str
+        """
+
+        self._event_id = event_id
 
     @property
-    def filter(self):
-        """Gets the filter of this MatchingPattern.  # noqa: E501
+    def user_id(self):
+        """Gets the user_id of this ManualEventHeader.  # noqa: E501
 
-        A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched  # noqa: E501
+        The user ID of the manual event  # noqa: E501
 
-        :return: The filter of this MatchingPattern.  # noqa: E501
+        :return: The user_id of this ManualEventHeader.  # noqa: E501
         :rtype: str
         """
-        return self._filter
+        return self._user_id
+
+    @user_id.setter
+    def user_id(self, user_id):
+        """Sets the user_id of this ManualEventHeader.
 
-    @filter.setter
-    def filter(self, filter):
-        """Sets the filter of this MatchingPattern.
-
-        A filter on the event. See https://support.lusid.com/filtering-results-from-lusid for more information. If not provided, all events will be matched  # noqa: E501
-
-        :param filter: The filter of this MatchingPattern.  # noqa: E501
-        :type filter: str
-        """
-        if (self.local_vars_configuration.client_side_validation and
-                filter is not None and len(filter) > 16384):
-            raise ValueError("Invalid value for `filter`, length must be less than or equal to `16384`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                filter is not None and len(filter) < 0):
-            raise ValueError("Invalid value for `filter`, length must be greater than or equal to `0`")  # noqa: E501
-        if (self.local_vars_configuration.client_side_validation and
-                filter is not None and not re.search(r'^[\s\S]*$', filter)):  # noqa: E501
-            raise ValueError(r"Invalid value for `filter`, must be a follow pattern or equal to `/^[\s\S]*$/`")  # noqa: E501
+        The user ID of the manual event  # noqa: E501
+
+        :param user_id: The user_id of this ManualEventHeader.  # noqa: E501
+        :type user_id: str
+        """
+
+        self._user_id = user_id
+
+    @property
+    def request_id(self):
+        """Gets the request_id of this ManualEventHeader.  # noqa: E501
+
+        The request ID of the manual event  # noqa: E501
+
+        :return: The request_id of this ManualEventHeader.  # noqa: E501
+        :rtype: str
+        """
+        return self._request_id
+
+    @request_id.setter
+    def request_id(self, request_id):
+        """Sets the request_id of this ManualEventHeader.
+
+        The request ID of the manual event  # noqa: E501
+
+        :param request_id: The request_id of this ManualEventHeader.  # noqa: E501
+        :type request_id: str
+        """
 
-        self._filter = filter
+        self._request_id = request_id
 
     def to_dict(self, serialize=False):
         """Returns the model properties as a dict"""
         result = {}
 
         def convert(x):
             if hasattr(x, "to_dict"):
@@ -177,18 +218,18 @@
 
     def __repr__(self):
         """For `print` and `pprint`"""
         return self.to_str()
 
     def __eq__(self, other):
         """Returns true if both objects are equal"""
-        if not isinstance(other, MatchingPattern):
+        if not isinstance(other, ManualEventHeader):
             return False
 
         return self.to_dict() == other.to_dict()
 
     def __ne__(self, other):
         """Returns true if both objects are not equal"""
-        if not isinstance(other, MatchingPattern):
+        if not isinstance(other, ManualEventHeader):
             return True
 
         return self.to_dict() != other.to_dict()
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/notification.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/notification.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/notification_status.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/notification_status.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_id.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_id.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_access_controlled_resource.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_access_controlled_resource.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_delivery.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_delivery.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_event_type_schema.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_event_type_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_notification.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_notification.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/resource_list_of_subscription.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/resource_list_of_subscription.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/subscription.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/subscription.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
@@ -41,90 +41,90 @@
     openapi_types = {
         'id': 'ResourceId',
         'display_name': 'str',
         'description': 'str',
         'status': 'str',
         'matching_pattern': 'MatchingPattern',
         'created_at': 'datetime',
-        'created_by': 'str',
-        'last_modified_at': 'datetime',
-        'last_modified_by': 'str'
+        'user_id_created': 'str',
+        'modified_at': 'datetime',
+        'user_id_modified': 'str'
     }
 
     attribute_map = {
         'id': 'id',
         'display_name': 'displayName',
         'description': 'description',
         'status': 'status',
         'matching_pattern': 'matchingPattern',
         'created_at': 'createdAt',
-        'created_by': 'createdBy',
-        'last_modified_at': 'lastModifiedAt',
-        'last_modified_by': 'lastModifiedBy'
+        'user_id_created': 'userIdCreated',
+        'modified_at': 'modifiedAt',
+        'user_id_modified': 'userIdModified'
     }
 
     required_map = {
         'id': 'required',
         'display_name': 'required',
         'description': 'optional',
         'status': 'required',
         'matching_pattern': 'required',
         'created_at': 'required',
-        'created_by': 'required',
-        'last_modified_at': 'required',
-        'last_modified_by': 'required'
+        'user_id_created': 'required',
+        'modified_at': 'required',
+        'user_id_modified': 'required'
     }
 
-    def __init__(self, id=None, display_name=None, description=None, status=None, matching_pattern=None, created_at=None, created_by=None, last_modified_at=None, last_modified_by=None, local_vars_configuration=None):  # noqa: E501
+    def __init__(self, id=None, display_name=None, description=None, status=None, matching_pattern=None, created_at=None, user_id_created=None, modified_at=None, user_id_modified=None, local_vars_configuration=None):  # noqa: E501
         """Subscription - a model defined in OpenAPI"
         
         :param id:  (required)
         :type id: lusid_notifications.ResourceId
         :param display_name:  The name of the subscription (required)
         :type display_name: str
         :param description:  The summary of the services provided by the subscription
         :type description: str
         :param status:  The current status of the subscription (required)
         :type status: str
         :param matching_pattern:  (required)
         :type matching_pattern: lusid_notifications.MatchingPattern
         :param created_at:  The time at which the subscription was made (required)
         :type created_at: datetime
-        :param created_by:  The user who made the subscription (required)
-        :type created_by: str
-        :param last_modified_at:  The time at which the subscription was last modified (required)
-        :type last_modified_at: datetime
-        :param last_modified_by:  The user who last modified the subscription (required)
-        :type last_modified_by: str
+        :param user_id_created:  The user who made the subscription (required)
+        :type user_id_created: str
+        :param modified_at:  The time at which the subscription was last modified (required)
+        :type modified_at: datetime
+        :param user_id_modified:  The user who last modified the subscription (required)
+        :type user_id_modified: str
 
         """  # noqa: E501
         if local_vars_configuration is None:
             local_vars_configuration = Configuration.get_default_copy()
         self.local_vars_configuration = local_vars_configuration
 
         self._id = None
         self._display_name = None
         self._description = None
         self._status = None
         self._matching_pattern = None
         self._created_at = None
-        self._created_by = None
-        self._last_modified_at = None
-        self._last_modified_by = None
+        self._user_id_created = None
+        self._modified_at = None
+        self._user_id_modified = None
         self.discriminator = None
 
         self.id = id
         self.display_name = display_name
         self.description = description
         self.status = status
         self.matching_pattern = matching_pattern
         self.created_at = created_at
-        self.created_by = created_by
-        self.last_modified_at = last_modified_at
-        self.last_modified_by = last_modified_by
+        self.user_id_created = user_id_created
+        self.modified_at = modified_at
+        self.user_id_modified = user_id_modified
 
     @property
     def id(self):
         """Gets the id of this Subscription.  # noqa: E501
 
 
         :return: The id of this Subscription.  # noqa: E501
@@ -269,93 +269,93 @@
         """
         if self.local_vars_configuration.client_side_validation and created_at is None:  # noqa: E501
             raise ValueError("Invalid value for `created_at`, must not be `None`")  # noqa: E501
 
         self._created_at = created_at
 
     @property
-    def created_by(self):
-        """Gets the created_by of this Subscription.  # noqa: E501
+    def user_id_created(self):
+        """Gets the user_id_created of this Subscription.  # noqa: E501
 
         The user who made the subscription  # noqa: E501
 
-        :return: The created_by of this Subscription.  # noqa: E501
+        :return: The user_id_created of this Subscription.  # noqa: E501
         :rtype: str
         """
-        return self._created_by
+        return self._user_id_created
 
-    @created_by.setter
-    def created_by(self, created_by):
-        """Sets the created_by of this Subscription.
+    @user_id_created.setter
+    def user_id_created(self, user_id_created):
+        """Sets the user_id_created of this Subscription.
 
         The user who made the subscription  # noqa: E501
 
-        :param created_by: The created_by of this Subscription.  # noqa: E501
-        :type created_by: str
+        :param user_id_created: The user_id_created of this Subscription.  # noqa: E501
+        :type user_id_created: str
         """
-        if self.local_vars_configuration.client_side_validation and created_by is None:  # noqa: E501
-            raise ValueError("Invalid value for `created_by`, must not be `None`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and user_id_created is None:  # noqa: E501
+            raise ValueError("Invalid value for `user_id_created`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                created_by is not None and len(created_by) < 1):
-            raise ValueError("Invalid value for `created_by`, length must be greater than or equal to `1`")  # noqa: E501
+                user_id_created is not None and len(user_id_created) < 1):
+            raise ValueError("Invalid value for `user_id_created`, length must be greater than or equal to `1`")  # noqa: E501
 
-        self._created_by = created_by
+        self._user_id_created = user_id_created
 
     @property
-    def last_modified_at(self):
-        """Gets the last_modified_at of this Subscription.  # noqa: E501
+    def modified_at(self):
+        """Gets the modified_at of this Subscription.  # noqa: E501
 
         The time at which the subscription was last modified  # noqa: E501
 
-        :return: The last_modified_at of this Subscription.  # noqa: E501
+        :return: The modified_at of this Subscription.  # noqa: E501
         :rtype: datetime
         """
-        return self._last_modified_at
+        return self._modified_at
 
-    @last_modified_at.setter
-    def last_modified_at(self, last_modified_at):
-        """Sets the last_modified_at of this Subscription.
+    @modified_at.setter
+    def modified_at(self, modified_at):
+        """Sets the modified_at of this Subscription.
 
         The time at which the subscription was last modified  # noqa: E501
 
-        :param last_modified_at: The last_modified_at of this Subscription.  # noqa: E501
-        :type last_modified_at: datetime
+        :param modified_at: The modified_at of this Subscription.  # noqa: E501
+        :type modified_at: datetime
         """
-        if self.local_vars_configuration.client_side_validation and last_modified_at is None:  # noqa: E501
-            raise ValueError("Invalid value for `last_modified_at`, must not be `None`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and modified_at is None:  # noqa: E501
+            raise ValueError("Invalid value for `modified_at`, must not be `None`")  # noqa: E501
 
-        self._last_modified_at = last_modified_at
+        self._modified_at = modified_at
 
     @property
-    def last_modified_by(self):
-        """Gets the last_modified_by of this Subscription.  # noqa: E501
+    def user_id_modified(self):
+        """Gets the user_id_modified of this Subscription.  # noqa: E501
 
         The user who last modified the subscription  # noqa: E501
 
-        :return: The last_modified_by of this Subscription.  # noqa: E501
+        :return: The user_id_modified of this Subscription.  # noqa: E501
         :rtype: str
         """
-        return self._last_modified_by
+        return self._user_id_modified
 
-    @last_modified_by.setter
-    def last_modified_by(self, last_modified_by):
-        """Sets the last_modified_by of this Subscription.
+    @user_id_modified.setter
+    def user_id_modified(self, user_id_modified):
+        """Sets the user_id_modified of this Subscription.
 
         The user who last modified the subscription  # noqa: E501
 
-        :param last_modified_by: The last_modified_by of this Subscription.  # noqa: E501
-        :type last_modified_by: str
+        :param user_id_modified: The user_id_modified of this Subscription.  # noqa: E501
+        :type user_id_modified: str
         """
-        if self.local_vars_configuration.client_side_validation and last_modified_by is None:  # noqa: E501
-            raise ValueError("Invalid value for `last_modified_by`, must not be `None`")  # noqa: E501
+        if self.local_vars_configuration.client_side_validation and user_id_modified is None:  # noqa: E501
+            raise ValueError("Invalid value for `user_id_modified`, must not be `None`")  # noqa: E501
         if (self.local_vars_configuration.client_side_validation and
-                last_modified_by is not None and len(last_modified_by) < 1):
-            raise ValueError("Invalid value for `last_modified_by`, length must be greater than or equal to `1`")  # noqa: E501
+                user_id_modified is not None and len(user_id_modified) < 1):
+            raise ValueError("Invalid value for `user_id_modified`, length must be greater than or equal to `1`")  # noqa: E501
 
-        self._last_modified_by = last_modified_by
+        self._user_id_modified = user_id_modified
 
     def to_dict(self, serialize=False):
         """Returns the model properties as a dict"""
         result = {}
 
         def convert(x):
             if hasattr(x, "to_dict"):
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/models/update_subscription.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/models/update_subscription.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 try:
     from inspect import getfullargspec
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/rest.py` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/rest.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     FINBOURNE Notifications API
 
     FINBOURNE Technology  # noqa: E501
 
-    The version of the OpenAPI document: 0.1.683
+    The version of the OpenAPI document: 0.1.683-2
     Contact: info@finbourne.com
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications/utilities/config_keys.json` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications/utilities/config_keys.json`

 * *Files identical despite different names*

### Comparing `lusid-notifications-sdk-preview-0.1.683/lusid_notifications_sdk_preview.egg-info/SOURCES.txt` & `lusid-notifications-sdk-preview-0.1.683.post2/lusid_notifications_sdk_preview.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -7,52 +7,48 @@
 lusid_notifications/configuration.py
 lusid_notifications/exceptions.py
 lusid_notifications/rest.py
 lusid_notifications/api/__init__.py
 lusid_notifications/api/application_metadata_api.py
 lusid_notifications/api/deliveries_api.py
 lusid_notifications/api/event_types_api.py
-lusid_notifications/api/events_api.py
+lusid_notifications/api/manual_event_api.py
 lusid_notifications/api/notifications_api.py
 lusid_notifications/api/subscriptions_api.py
 lusid_notifications/models/__init__.py
 lusid_notifications/models/access_controlled_action.py
 lusid_notifications/models/access_controlled_resource.py
 lusid_notifications/models/action_id.py
 lusid_notifications/models/attempt.py
 lusid_notifications/models/attempt_status.py
-lusid_notifications/models/create_aws_sqs_notification.py
-lusid_notifications/models/create_email_notification.py
-lusid_notifications/models/create_sms_notification.py
+lusid_notifications/models/create_notification.py
 lusid_notifications/models/create_subscription.py
-lusid_notifications/models/create_webhook_notification.py
 lusid_notifications/models/delivery.py
-lusid_notifications/models/event_details.py
 lusid_notifications/models/event_type_schema.py
 lusid_notifications/models/id_selector_definition.py
 lusid_notifications/models/identifier_part_schema.py
 lusid_notifications/models/link.py
 lusid_notifications/models/lusid_problem_details.py
 lusid_notifications/models/lusid_validation_problem_details.py
+lusid_notifications/models/manual_event.py
+lusid_notifications/models/manual_event_body.py
+lusid_notifications/models/manual_event_header.py
 lusid_notifications/models/matching_pattern.py
 lusid_notifications/models/notification.py
 lusid_notifications/models/notification_status.py
 lusid_notifications/models/resource_id.py
 lusid_notifications/models/resource_list_of_access_controlled_resource.py
 lusid_notifications/models/resource_list_of_delivery.py
 lusid_notifications/models/resource_list_of_event_type_schema.py
 lusid_notifications/models/resource_list_of_notification.py
 lusid_notifications/models/resource_list_of_subscription.py
 lusid_notifications/models/subscription.py
 lusid_notifications/models/subscription_detail.py
-lusid_notifications/models/update_aws_sqs_notification.py
-lusid_notifications/models/update_email_notification.py
-lusid_notifications/models/update_sms_notification.py
+lusid_notifications/models/update_notification.py
 lusid_notifications/models/update_subscription.py
-lusid_notifications/models/update_webhook_notification.py
 lusid_notifications/utilities/__init__.py
 lusid_notifications/utilities/config_keys.json
 lusid_notifications/utilities/config_keys.py
 lusid_notifications_sdk_preview.egg-info/PKG-INFO
 lusid_notifications_sdk_preview.egg-info/SOURCES.txt
 lusid_notifications_sdk_preview.egg-info/dependency_links.txt
 lusid_notifications_sdk_preview.egg-info/requires.txt
```

### Comparing `lusid-notifications-sdk-preview-0.1.683/setup.py` & `lusid-notifications-sdk-preview-0.1.683.post2/setup.py`

 * *Files identical despite different names*

