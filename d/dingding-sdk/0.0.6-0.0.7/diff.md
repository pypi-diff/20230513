# Comparing `tmp/dingding-sdk-0.0.6.tar.gz` & `tmp/dingding-sdk-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dingding-sdk-0.0.6.tar", last modified: Tue May  9 01:57:53 2023, max compression
+gzip compressed data, was "dingding-sdk-0.0.7.tar", last modified: Sat May 13 02:20:52 2023, max compression
```

## Comparing `dingding-sdk-0.0.6.tar` & `dingding-sdk-0.0.7.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-09 01:57:53.526119 dingding-sdk-0.0.6/
--rw-r--r--   0 root         (0) root         (0)      825 2023-05-09 01:57:53.526119 dingding-sdk-0.0.6/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)       59 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-09 01:57:53.522119 dingding-sdk-0.0.6/dingding_sdk.egg-info/
--rw-r--r--   0 root         (0) root         (0)      825 2023-05-09 01:57:52.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      687 2023-05-09 01:57:53.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-09 01:57:52.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)        9 2023-05-09 01:57:53.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       15 2023-05-09 01:57:53.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/dingding_sdk.egg-info/zip-safe
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-09 01:57:53.526119 dingding-sdk-0.0.6/dingtalk/
--rw-r--r--   0 root         (0) root         (0)      226 2023-05-08 05:44:25.000000 dingding-sdk-0.0.6/dingtalk/__init__.py
--rw-r--r--   0 root         (0) root         (0)    18453 2023-05-08 13:32:50.000000 dingding-sdk-0.0.6/dingtalk/contact.py
--rw-r--r--   0 root         (0) root         (0)     3812 2023-05-09 00:58:58.000000 dingding-sdk-0.0.6/dingtalk/core.py
--rw-r--r--   0 root         (0) root         (0)     1376 2023-05-09 00:37:27.000000 dingding-sdk-0.0.6/dingtalk/dingtalk.py
--rw-r--r--   0 root         (0) root         (0)     1864 2023-05-08 14:04:56.000000 dingding-sdk-0.0.6/dingtalk/document.py
--rw-r--r--   0 root         (0) root         (0)     1033 2023-05-08 14:36:30.000000 dingding-sdk-0.0.6/dingtalk/exceptions.py
--rw-r--r--   0 root         (0) root         (0)     2256 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/dingtalk/hr.py
--rw-r--r--   0 root         (0) root         (0)     2780 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/dingtalk/message.py
--rw-r--r--   0 root         (0) root         (0)     2224 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/dingtalk/oauth.py
--rw-r--r--   0 root         (0) root         (0)     1954 2023-05-09 01:14:29.000000 dingding-sdk-0.0.6/dingtalk/robot.py
--rw-r--r--   0 root         (0) root         (0)     2061 2023-05-09 01:53:43.000000 dingding-sdk-0.0.6/dingtalk/session.py
--rw-r--r--   0 root         (0) root         (0)      829 2023-05-08 15:00:28.000000 dingding-sdk-0.0.6/dingtalk/space.py
--rw-r--r--   0 root         (0) root         (0)     1542 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/dingtalk/workflow.py
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-09 01:57:53.530119 dingding-sdk-0.0.6/setup.cfg
--rw-r--r--   0 root         (0) root         (0)     1448 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-09 01:57:53.526119 dingding-sdk-0.0.6/tests/
--rw-r--r--   0 root         (0) root         (0)        0 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/__init__.py
--rw-r--r--   0 root         (0) root         (0)     5584 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/test_contact.py
--rw-r--r--   0 root         (0) root         (0)      648 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/test_core.py
--rw-r--r--   0 root         (0) root         (0)      773 2023-05-08 03:41:13.000000 dingding-sdk-0.0.6/tests/test_document.py
--rw-r--r--   0 root         (0) root         (0)     1103 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/test_hr.py
--rw-r--r--   0 root         (0) root         (0)     1892 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/test_message.py
--rw-r--r--   0 root         (0) root         (0)     1300 2023-05-09 01:13:00.000000 dingding-sdk-0.0.6/tests/test_robot.py
--rw-r--r--   0 root         (0) root         (0)      861 2023-05-09 01:49:34.000000 dingding-sdk-0.0.6/tests/test_session.py
--rw-r--r--   0 root         (0) root         (0)     1981 2023-05-08 14:05:59.000000 dingding-sdk-0.0.6/tests/test_space.py
--rw-r--r--   0 root         (0) root         (0)      953 2023-05-08 02:57:45.000000 dingding-sdk-0.0.6/tests/test_workflow.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:20:52.689391 dingding-sdk-0.0.7/
+-rw-r--r--   0 root         (0) root         (0)      825 2023-05-13 02:20:52.689391 dingding-sdk-0.0.7/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)       59 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:20:52.665391 dingding-sdk-0.0.7/dingding_sdk.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      825 2023-05-13 02:20:52.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      687 2023-05-13 02:20:52.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 02:20:52.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)        9 2023-05-13 02:20:52.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       15 2023-05-13 02:20:52.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/dingding_sdk.egg-info/zip-safe
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:20:52.681391 dingding-sdk-0.0.7/dingtalk/
+-rw-r--r--   0 root         (0) root         (0)      226 2023-05-13 02:20:48.000000 dingding-sdk-0.0.7/dingtalk/__init__.py
+-rw-r--r--   0 root         (0) root         (0)    18453 2023-05-08 13:32:50.000000 dingding-sdk-0.0.7/dingtalk/contact.py
+-rw-r--r--   0 root         (0) root         (0)     3812 2023-05-09 00:58:58.000000 dingding-sdk-0.0.7/dingtalk/core.py
+-rw-r--r--   0 root         (0) root         (0)     1376 2023-05-09 00:37:27.000000 dingding-sdk-0.0.7/dingtalk/dingtalk.py
+-rw-r--r--   0 root         (0) root         (0)     1864 2023-05-08 14:04:56.000000 dingding-sdk-0.0.7/dingtalk/document.py
+-rw-r--r--   0 root         (0) root         (0)     1033 2023-05-08 14:36:30.000000 dingding-sdk-0.0.7/dingtalk/exceptions.py
+-rw-r--r--   0 root         (0) root         (0)     2256 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/dingtalk/hr.py
+-rw-r--r--   0 root         (0) root         (0)     2780 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/dingtalk/message.py
+-rw-r--r--   0 root         (0) root         (0)     2224 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/dingtalk/oauth.py
+-rw-r--r--   0 root         (0) root         (0)     2536 2023-05-13 02:09:31.000000 dingding-sdk-0.0.7/dingtalk/robot.py
+-rw-r--r--   0 root         (0) root         (0)     2061 2023-05-09 01:53:43.000000 dingding-sdk-0.0.7/dingtalk/session.py
+-rw-r--r--   0 root         (0) root         (0)      829 2023-05-08 15:00:28.000000 dingding-sdk-0.0.7/dingtalk/space.py
+-rw-r--r--   0 root         (0) root         (0)     1542 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/dingtalk/workflow.py
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 02:20:52.689391 dingding-sdk-0.0.7/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)     1448 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:20:52.689391 dingding-sdk-0.0.7/tests/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     5584 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/test_contact.py
+-rw-r--r--   0 root         (0) root         (0)      648 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/test_core.py
+-rw-r--r--   0 root         (0) root         (0)      773 2023-05-08 03:41:13.000000 dingding-sdk-0.0.7/tests/test_document.py
+-rw-r--r--   0 root         (0) root         (0)     1103 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/test_hr.py
+-rw-r--r--   0 root         (0) root         (0)     1892 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/test_message.py
+-rw-r--r--   0 root         (0) root         (0)     1880 2023-05-13 02:13:08.000000 dingding-sdk-0.0.7/tests/test_robot.py
+-rw-r--r--   0 root         (0) root         (0)      861 2023-05-09 01:49:34.000000 dingding-sdk-0.0.7/tests/test_session.py
+-rw-r--r--   0 root         (0) root         (0)     1981 2023-05-08 14:05:59.000000 dingding-sdk-0.0.7/tests/test_space.py
+-rw-r--r--   0 root         (0) root         (0)      953 2023-05-08 02:57:45.000000 dingding-sdk-0.0.7/tests/test_workflow.py
```

### Comparing `dingding-sdk-0.0.6/PKG-INFO` & `dingding-sdk-0.0.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dingding-sdk
-Version: 0.0.6
+Version: 0.0.7
 Summary: DingTalk Python SDK
 Home-page: https://github.com/jellyhappy/dingding-sdk
 Author: blackcat
 Author-email: kfx2007@163.com
 License: GNU
 Keywords: dingding sdk
 Platform: UNKNOWN
```

### Comparing `dingding-sdk-0.0.6/dingding_sdk.egg-info/PKG-INFO` & `dingding-sdk-0.0.7/dingding_sdk.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dingding-sdk
-Version: 0.0.6
+Version: 0.0.7
 Summary: DingTalk Python SDK
 Home-page: https://github.com/jellyhappy/dingding-sdk
 Author: blackcat
 Author-email: kfx2007@163.com
 License: GNU
 Keywords: dingding sdk
 Platform: UNKNOWN
```

### Comparing `dingding-sdk-0.0.6/dingding_sdk.egg-info/SOURCES.txt` & `dingding-sdk-0.0.7/dingding_sdk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/contact.py` & `dingding-sdk-0.0.7/dingtalk/contact.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/core.py` & `dingding-sdk-0.0.7/dingtalk/core.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/dingtalk.py` & `dingding-sdk-0.0.7/dingtalk/dingtalk.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/document.py` & `dingding-sdk-0.0.7/dingtalk/document.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/exceptions.py` & `dingding-sdk-0.0.7/dingtalk/exceptions.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/hr.py` & `dingding-sdk-0.0.7/dingtalk/hr.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/message.py` & `dingding-sdk-0.0.7/dingtalk/message.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/oauth.py` & `dingding-sdk-0.0.7/dingtalk/oauth.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/robot.py` & `dingding-sdk-0.0.7/dingtalk/robot.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 #!/usr/bin/python3
 # @Time    : 2023-05-09
 # @Author  : Kevin Kong (kfx2007@163.com)
 
-from dingtalk.core import Core,NEW_URL
+import json
+from dingtalk.core import Core, NEW_URL
 
 
 class RobotFile(object):
     def __init__(self, media_id, file_name, file_type):
         self.media_id = media_id
         self.file_name = file_name
         self.file_type = file_type
@@ -21,42 +22,60 @@
     def to_json(self):
         return {
             "mediaId": self.media_id,
             "fileName": self.file_name,
             "fileType": self.file_type
         }
 
-import json
 
 class Robot(Core):
 
     def __init__(self, code=None):
         self.code = code
 
-    def push_text_group_message(self, text,conver_id=None,coolAppCode=None):
+    def push_text_group_message(self, text, conver_id=None, coolAppCode=None):
         url = f"{NEW_URL}/v1.0/robot/groupMessages/send"
 
         data = {
             "msgParam": str({"content": text}),
             "msgKey": "sampleText",
             "robotCode": self.code,
         }
-        
 
         if conver_id:
             data['openConversationId'] = conver_id
         if coolAppCode:
             data['coolAppCode'] = coolAppCode
 
         # data = json.dumps(data)
 
-        res = self._v2_post(url,json=data)
+        res = self._v2_post(url, json=data)
         return res
 
-    def push_file_group_message(self, file, conver_id=None,coolAppCode=None):
+    def push_markdown_group_message(self, title, text, conver_id=None, coolAppCode=None):
+        url = f"{NEW_URL}/v1.0/robot/groupMessages/send"
+
+        data = {
+            "msgParam": str({"title": title, "text": text}),
+            "msgKey": "sampleMarkdown",
+            "robotCode": self.code,
+        }
+
+        if conver_id:
+            data['openConversationId'] = conver_id
+        if coolAppCode:
+            data['coolAppCode'] = coolAppCode
+
+        # data = json.dumps(data)
+        print('----')
+        print(data)
+        res = self._v2_post(url, json=data)
+        return res
+
+    def push_file_group_message(self, file, conver_id=None, coolAppCode=None):
         """
             push message to chat.
 
             :param file: Robot File
             :param conver_id: Conversation Id
 
             :return 
@@ -70,10 +89,10 @@
             "msgKey": file.key,
             "robotCode": self.code,
         }
         if conver_id:
             data['openConversationId'] = conver_id
         if coolAppCode:
             data['coolAppCode'] = coolAppCode
-            
-        res = self._v2_post(url,data)
+
+        res = self._v2_post(url, data)
         return res
```

### Comparing `dingding-sdk-0.0.6/dingtalk/session.py` & `dingding-sdk-0.0.7/dingtalk/session.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/space.py` & `dingding-sdk-0.0.7/dingtalk/space.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/dingtalk/workflow.py` & `dingding-sdk-0.0.7/dingtalk/workflow.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/setup.py` & `dingding-sdk-0.0.7/setup.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_contact.py` & `dingding-sdk-0.0.7/tests/test_contact.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_core.py` & `dingding-sdk-0.0.7/tests/test_core.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_document.py` & `dingding-sdk-0.0.7/tests/test_document.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_hr.py` & `dingding-sdk-0.0.7/tests/test_hr.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_message.py` & `dingding-sdk-0.0.7/tests/test_message.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_session.py` & `dingding-sdk-0.0.7/tests/test_session.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_space.py` & `dingding-sdk-0.0.7/tests/test_space.py`

 * *Files identical despite different names*

### Comparing `dingding-sdk-0.0.6/tests/test_workflow.py` & `dingding-sdk-0.0.7/tests/test_workflow.py`

 * *Files identical despite different names*

