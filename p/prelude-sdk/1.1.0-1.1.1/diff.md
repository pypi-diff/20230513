# Comparing `tmp/prelude-sdk-1.1.0.tar.gz` & `tmp/prelude-sdk-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "prelude-sdk-1.1.0.tar", last modified: Sun May  7 12:44:09 2023, max compression
+gzip compressed data, was "prelude-sdk-1.1.1.tar", last modified: Sat May 13 20:30:41 2023, max compression
```

## Comparing `prelude-sdk-1.1.0.tar` & `prelude-sdk-1.1.1.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.742916 prelude-sdk-1.1.0/
--rw-r--r--   0 pack       (501) staff       (20)     1069 2023-01-24 13:01:01.000000 prelude-sdk-1.1.0/LICENSE
--rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-07 12:44:09.742997 prelude-sdk-1.1.0/PKG-INFO
--rw-r--r--   0 pack       (501) staff       (20)      697 2023-04-11 22:16:02.000000 prelude-sdk-1.1.0/README.md
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.738330 prelude-sdk-1.1.0/prelude_sdk/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.0/prelude_sdk/__init__.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.740270 prelude-sdk-1.1.0/prelude_sdk/controllers/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)     2230 2023-05-07 12:16:47.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/build_controller.py
--rw-r--r--   0 pack       (501) staff       (20)     4077 2023-05-03 13:30:52.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/detect_controller.py
--rw-r--r--   0 pack       (501) staff       (20)     3201 2023-05-03 13:30:52.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/iam_controller.py
--rw-r--r--   0 pack       (501) staff       (20)     2046 2023-05-03 13:30:52.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/partner_controller.py
--rw-r--r--   0 pack       (501) staff       (20)      443 2023-05-03 13:30:52.000000 prelude-sdk-1.1.0/prelude_sdk/controllers/probe_controller.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.740854 prelude-sdk-1.1.0/prelude_sdk/models/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.0/prelude_sdk/models/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)     2816 2023-04-07 19:23:14.000000 prelude-sdk-1.1.0/prelude_sdk/models/account.py
--rw-r--r--   0 pack       (501) staff       (20)     2609 2023-04-08 00:28:18.000000 prelude-sdk-1.1.0/prelude_sdk/models/codes.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.738908 prelude-sdk-1.1.0/prelude_sdk.egg-info/
--rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-07 12:44:09.000000 prelude-sdk-1.1.0/prelude_sdk.egg-info/PKG-INFO
--rw-r--r--   0 pack       (501) staff       (20)      806 2023-05-07 12:44:09.000000 prelude-sdk-1.1.0/prelude_sdk.egg-info/SOURCES.txt
--rw-r--r--   0 pack       (501) staff       (20)        1 2023-05-07 12:44:09.000000 prelude-sdk-1.1.0/prelude_sdk.egg-info/dependency_links.txt
--rw-r--r--   0 pack       (501) staff       (20)        9 2023-05-07 12:44:09.000000 prelude-sdk-1.1.0/prelude_sdk.egg-info/requires.txt
--rw-r--r--   0 pack       (501) staff       (20)       18 2023-05-07 12:44:09.000000 prelude-sdk-1.1.0/prelude_sdk.egg-info/top_level.txt
--rw-r--r--   0 pack       (501) staff       (20)      103 2023-01-24 13:01:01.000000 prelude-sdk-1.1.0/pyproject.toml
--rw-r--r--   0 pack       (501) staff       (20)      532 2023-05-07 12:44:09.743225 prelude-sdk-1.1.0/setup.cfg
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.742595 prelude-sdk-1.1.0/tests/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-04-07 19:23:14.000000 prelude-sdk-1.1.0/tests/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)     1101 2023-04-11 22:16:02.000000 prelude-sdk-1.1.0/tests/conftest.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:44:09.742820 prelude-sdk-1.1.0/tests/templates/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-04-07 19:23:14.000000 prelude-sdk-1.1.0/tests/templates/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)     2188 2023-05-07 12:16:47.000000 prelude-sdk-1.1.0/tests/test_build_controller.py
--rw-r--r--   0 pack       (501) staff       (20)     3734 2023-05-03 13:30:52.000000 prelude-sdk-1.1.0/tests/test_detect_controller.py
--rw-r--r--   0 pack       (501) staff       (20)     3327 2023-05-04 16:11:50.000000 prelude-sdk-1.1.0/tests/test_iam_controller.py
--rw-r--r--   0 pack       (501) staff       (20)      785 2023-05-02 14:19:17.000000 prelude-sdk-1.1.0/tests/test_partner_controller.py
--rw-r--r--   0 pack       (501) staff       (20)      682 2023-04-07 19:23:14.000000 prelude-sdk-1.1.0/tests/test_probe_controller.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.680450 prelude-sdk-1.1.1/
+-rw-r--r--   0 pack       (501) staff       (20)     1069 2023-01-24 13:01:01.000000 prelude-sdk-1.1.1/LICENSE
+-rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-13 20:30:41.680502 prelude-sdk-1.1.1/PKG-INFO
+-rw-r--r--   0 pack       (501) staff       (20)      697 2023-04-11 22:16:02.000000 prelude-sdk-1.1.1/README.md
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.676136 prelude-sdk-1.1.1/prelude_sdk/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.1/prelude_sdk/__init__.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.678264 prelude-sdk-1.1.1/prelude_sdk/controllers/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)     2230 2023-05-07 12:16:47.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/build_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)     4115 2023-05-12 13:56:19.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/detect_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)     3266 2023-05-12 13:56:19.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/iam_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)     2046 2023-05-03 13:30:52.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/partner_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)      443 2023-05-03 13:30:52.000000 prelude-sdk-1.1.1/prelude_sdk/controllers/probe_controller.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.678822 prelude-sdk-1.1.1/prelude_sdk/models/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-sdk-1.1.1/prelude_sdk/models/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)     2816 2023-04-07 19:23:14.000000 prelude-sdk-1.1.1/prelude_sdk/models/account.py
+-rw-r--r--   0 pack       (501) staff       (20)     2698 2023-05-09 16:39:45.000000 prelude-sdk-1.1.1/prelude_sdk/models/codes.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.676729 prelude-sdk-1.1.1/prelude_sdk.egg-info/
+-rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-13 20:30:41.000000 prelude-sdk-1.1.1/prelude_sdk.egg-info/PKG-INFO
+-rw-r--r--   0 pack       (501) staff       (20)      806 2023-05-13 20:30:41.000000 prelude-sdk-1.1.1/prelude_sdk.egg-info/SOURCES.txt
+-rw-r--r--   0 pack       (501) staff       (20)        1 2023-05-13 20:30:41.000000 prelude-sdk-1.1.1/prelude_sdk.egg-info/dependency_links.txt
+-rw-r--r--   0 pack       (501) staff       (20)        9 2023-05-13 20:30:41.000000 prelude-sdk-1.1.1/prelude_sdk.egg-info/requires.txt
+-rw-r--r--   0 pack       (501) staff       (20)       18 2023-05-13 20:30:41.000000 prelude-sdk-1.1.1/prelude_sdk.egg-info/top_level.txt
+-rw-r--r--   0 pack       (501) staff       (20)      103 2023-01-24 13:01:01.000000 prelude-sdk-1.1.1/pyproject.toml
+-rw-r--r--   0 pack       (501) staff       (20)      532 2023-05-13 20:30:41.680703 prelude-sdk-1.1.1/setup.cfg
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.680099 prelude-sdk-1.1.1/tests/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-04-07 19:23:14.000000 prelude-sdk-1.1.1/tests/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)     1101 2023-04-11 22:16:02.000000 prelude-sdk-1.1.1/tests/conftest.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:30:41.680359 prelude-sdk-1.1.1/tests/templates/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-04-07 19:23:14.000000 prelude-sdk-1.1.1/tests/templates/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)     2188 2023-05-07 12:16:47.000000 prelude-sdk-1.1.1/tests/test_build_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)     3734 2023-05-03 13:30:52.000000 prelude-sdk-1.1.1/tests/test_detect_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)     3359 2023-05-12 13:56:19.000000 prelude-sdk-1.1.1/tests/test_iam_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)      785 2023-05-02 14:19:17.000000 prelude-sdk-1.1.1/tests/test_partner_controller.py
+-rw-r--r--   0 pack       (501) staff       (20)      682 2023-04-07 19:23:14.000000 prelude-sdk-1.1.1/tests/test_probe_controller.py
```

### Comparing `prelude-sdk-1.1.0/LICENSE` & `prelude-sdk-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/PKG-INFO` & `prelude-sdk-1.1.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prelude-sdk
-Version: 1.1.0
+Version: 1.1.1
 Summary: For interacting with the Prelude API
 Home-page: https://github.com/preludeorg
 Author: Prelude Research
 Author-email: support@preludesecurity.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `prelude-sdk-1.1.0/README.md` & `prelude-sdk-1.1.1/README.md`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/prelude_sdk/controllers/build_controller.py` & `prelude-sdk-1.1.1/prelude_sdk/controllers/build_controller.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/prelude_sdk/controllers/detect_controller.py` & `prelude-sdk-1.1.1/prelude_sdk/controllers/detect_controller.py`

 * *Files 6% similar despite different names*

```diff
@@ -64,20 +64,21 @@
             return res.json()
         raise Exception(res.text)
 
     @verify_credentials
     def list_queue(self):
         """ List all tests in the queue """
         res = requests.get(
-            f'{self.account.hq}/detect/queue',
+            f'{self.account.hq}/iam/account',
             headers=self.account.headers,
             timeout=10
         )
         if res.status_code == 200:
-            return res.json()
+            account = res.json()
+            return account['queue']
         raise Exception(res.text)
 
     @verify_credentials
     def list_tests(self):
         """ List all tests available to an account """
         res = requests.get(
             f'{self.account.hq}/detect/tests',
```

### Comparing `prelude-sdk-1.1.0/prelude_sdk/controllers/iam_controller.py` & `prelude-sdk-1.1.1/prelude_sdk/controllers/iam_controller.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,18 +6,18 @@
 
 class IAMController:
 
     def __init__(self, account):
         self.account = account
 
     @verify_credentials
-    def new_account(self, handle: str):
+    def new_account(self, user_email: str, user_name: str):
         res = requests.post(
             url=f'{self.account.hq}/iam/account',
-            json=dict(handle=handle),
+            json=dict(handle=user_email, user_name=user_name),
             headers=self.account.headers,
             timeout=10
         )
         if res.status_code != 200:
             raise Exception(res.text)
 
         cfg = self.account.read_keychain_config()
@@ -60,19 +60,19 @@
             timeout=10
         )
         if res.status_code == 200:
             return res.json()
         raise Exception(res.text)
 
     @verify_credentials
-    def create_user(self, permission: int, handle: str, expires: datetime):
+    def create_user(self, permission: int, email: str, name: str, expires: datetime):
         """ Create a new user inside an account """
         res = requests.post(
             url=f'{self.account.hq}/iam/user',
-            json=dict(permission=permission, handle=handle, expires=expires.isoformat()),
+            json=dict(permission=permission, handle=email, name=name, expires=expires.isoformat()),
             headers=self.account.headers,
             timeout=10
         )
         if res.status_code == 200:
             return res.json()
         raise Exception(res.text)
```

### Comparing `prelude-sdk-1.1.0/prelude_sdk/controllers/partner_controller.py` & `prelude-sdk-1.1.1/prelude_sdk/controllers/partner_controller.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/prelude_sdk/models/account.py` & `prelude-sdk-1.1.1/prelude_sdk/models/account.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/prelude_sdk/models/codes.py` & `prelude-sdk-1.1.1/prelude_sdk/models/codes.py`

 * *Files 4% similar despite different names*

```diff
@@ -12,14 +12,15 @@
     def _missing_(cls, value):
         return RunCode.INVALID
     
 
 class Mode(Enum):
      MANUAL = 0
      FROZEN = 1
+     AUTOPILOT = 2
 
      @classmethod
      def _missing_(cls, value):
          return Mode.MANUAL
      
 
 class Permission(Enum):
@@ -48,14 +49,15 @@
     CLEANUP_ERROR = 103
     NOT_RELEVANT = 104
     QUARANTINED_1 = 105
     OUTBOUND_SECURE = 106
     EXPLOIT_PREVENTED = 107
     ENDPOINT_BLOCKED = 126
     QUARANTINED_2 = 127
+    PROCESS_KILLED_3 = 137
     UNEXPECTED = 256
 
     @classmethod
     def _missing_(cls, value):
         return ExitCode.MISSING
 
     @property
@@ -82,15 +84,16 @@
                 ExitCode.QUARANTINED_1,
                 ExitCode.QUARANTINED_2,
                 ExitCode.PROCESS_KILLED_1,
                 ExitCode.PROCESS_KILLED_2,
                 ExitCode.NOT_RELEVANT,
                 ExitCode.OUTBOUND_SECURE,
                 ExitCode.ENDPOINT_BLOCKED,
-                ExitCode.EXPLOIT_PREVENTED
+                ExitCode.EXPLOIT_PREVENTED,
+                ExitCode.PROCESS_KILLED_3
             ],
             State.UNPROTECTED: [ExitCode.UNPROTECTED],
             State.ERROR: [
                 ExitCode.ERROR,
                 ExitCode.MALFORMED_VST,
                 ExitCode.TIMEOUT,
                 ExitCode.UNEXPECTED
```

### Comparing `prelude-sdk-1.1.0/prelude_sdk.egg-info/PKG-INFO` & `prelude-sdk-1.1.1/prelude_sdk.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prelude-sdk
-Version: 1.1.0
+Version: 1.1.1
 Summary: For interacting with the Prelude API
 Home-page: https://github.com/preludeorg
 Author: Prelude Research
 Author-email: support@preludesecurity.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `prelude-sdk-1.1.0/prelude_sdk.egg-info/SOURCES.txt` & `prelude-sdk-1.1.1/prelude_sdk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/setup.cfg` & `prelude-sdk-1.1.1/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = prelude-sdk
-version = 1.1.0
+version = 1.1.1
 author = Prelude Research
 author_email = support@preludesecurity.com
 description = For interacting with the Prelude API
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/preludeorg
 classifiers =
```

### Comparing `prelude-sdk-1.1.0/tests/conftest.py` & `prelude-sdk-1.1.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/tests/test_build_controller.py` & `prelude-sdk-1.1.1/tests/test_build_controller.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/tests/test_detect_controller.py` & `prelude-sdk-1.1.1/tests/test_detect_controller.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/tests/test_iam_controller.py` & `prelude-sdk-1.1.1/tests/test_iam_controller.py`

 * *Files 2% similar despite different names*

```diff
@@ -36,15 +36,15 @@
 class TestIAMController:
 
     @pytest.mark.order(1)
     def test_new_account(self, unwrap, pause_for_manual_action, email, api):
         """Test new_account method"""
         pytest.account = Account(hq=api)
         iam = IAMController(pytest.account)
-        res = unwrap(iam.new_account)(iam, handle=email)
+        res = unwrap(iam.new_account)(iam, user_email=email, user_name='Bob')
         if email.endswith('@auto-accept.developer.preludesecurity.com'):
             time.sleep(5)
         else:
             with pause_for_manual_action:
                 input("Press ENTER to continue testing after verifying the account...\n")
         pytest.account.headers['account'] = res['account_id']
         pytest.account.headers['token'] = res['token']
@@ -59,15 +59,15 @@
         assert res['whoami'] == email
         assert res['mode'] == 0
 
     @pytest.mark.order(3)
     def test_create_user(self, unwrap):
         """Test create_user method"""
         iam = IAMController(pytest.account)
-        res = unwrap(iam.create_user)(iam, handle='registration', permission=Permission.SERVICE.value, expires=(datetime.utcnow() + timedelta(days=1)))
+        res = unwrap(iam.create_user)(iam, email='registration', permission=Permission.SERVICE.value, name='Rob', expires=(datetime.utcnow() + timedelta(days=1)))
         assert check_if_string_is_uuid(res['token'])
         res = unwrap(iam.get_account)(iam)
         assert len([user for user in res['users'] if user['handle'] == 'registration']) == 1
 
     @pytest.mark.order(4)
     def test_delete_user(self, unwrap):
         """Test delete_user method"""
```

### Comparing `prelude-sdk-1.1.0/tests/test_partner_controller.py` & `prelude-sdk-1.1.1/tests/test_partner_controller.py`

 * *Files identical despite different names*

### Comparing `prelude-sdk-1.1.0/tests/test_probe_controller.py` & `prelude-sdk-1.1.1/tests/test_probe_controller.py`

 * *Files identical despite different names*

