# Comparing `tmp/django_admob_ssv-2.0.0.tar.gz` & `tmp/django_admob_ssv-2.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_admob_ssv-2.0.0.tar", max compression
+gzip compressed data, was "django_admob_ssv-2.1.0.tar", max compression
```

## Comparing `django_admob_ssv-2.0.0.tar` & `django_admob_ssv-2.1.0.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1054 2020-02-02 17:21:08.157959 django_admob_ssv-2.0.0/LICENSE
--rw-r--r--   0        0        0     4692 2023-05-11 23:28:08.625387 django_admob_ssv-2.0.0/README.md
--rw-r--r--   0        0        0       53 2023-05-10 00:50:56.437043 django_admob_ssv-2.0.0/admob_ssv/__init__.py
--rw-r--r--   0        0        0       92 2023-05-10 00:50:56.437043 django_admob_ssv-2.0.0/admob_ssv/apps.py
--rw-r--r--   0        0        0      744 2023-05-12 14:01:57.966517 django_admob_ssv-2.0.0/admob_ssv/conf.py
--rw-r--r--   0        0        0       68 2023-05-10 01:06:06.824655 django_admob_ssv-2.0.0/admob_ssv/signals.py
--rw-r--r--   0        0        0     3665 2023-05-12 14:01:57.966517 django_admob_ssv-2.0.0/admob_ssv/views.py
--rw-r--r--   0        0        0     1661 2023-05-12 14:02:15.096857 django_admob_ssv-2.0.0/pyproject.toml
--rw-r--r--   0        0        0     6304 1970-01-01 00:00:00.000000 django_admob_ssv-2.0.0/PKG-INFO
+-rw-r--r--   0        0        0     1054 2020-02-02 17:21:08.157959 django_admob_ssv-2.1.0/LICENSE
+-rw-r--r--   0        0        0     5537 2023-05-13 00:12:00.214325 django_admob_ssv-2.1.0/README.md
+-rw-r--r--   0        0        0       53 2023-05-10 00:50:56.437043 django_admob_ssv-2.1.0/admob_ssv/__init__.py
+-rw-r--r--   0        0        0       92 2023-05-10 00:50:56.437043 django_admob_ssv-2.1.0/admob_ssv/apps.py
+-rw-r--r--   0        0        0      744 2023-05-12 14:01:57.966517 django_admob_ssv-2.1.0/admob_ssv/conf.py
+-rw-r--r--   0        0        0       68 2023-05-10 01:06:06.824655 django_admob_ssv-2.1.0/admob_ssv/signals.py
+-rw-r--r--   0        0        0     3767 2023-05-13 00:12:00.214325 django_admob_ssv-2.1.0/admob_ssv/views.py
+-rw-r--r--   0        0        0     1661 2023-05-13 00:12:02.401037 django_admob_ssv-2.1.0/pyproject.toml
+-rw-r--r--   0        0        0     7149 1970-01-01 00:00:00.000000 django_admob_ssv-2.1.0/PKG-INFO
```

### Comparing `django_admob_ssv-2.0.0/LICENSE` & `django_admob_ssv-2.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `django_admob_ssv-2.0.0/README.md` & `django_admob_ssv-2.1.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -78,14 +78,48 @@
 ADMOB_SSV_KEY_SERVER_URL = "https://www.gstatic.com/admob/reward/verifier-keys.json",
 
 ADMOB_SSV_KEYS_CACHE_TIMEOUT = timedelta(days=1)
 
 ADMOB_SSV_KEYS_CACHE_KEY = "admob_ssv.public_keys"
 ```
 
+## Usage without Django signals
+
+If you don't want to use Django signals, you may subclass the
+`admob_ssv.views.AdmobSSVView` view and override the `handle_valid_ssv`
+method.
+
+Note that unless you call `super().handle_valid_ssv(request)`,
+the `admob_ssv.signals.valid_admob_ssv` signal won't be sent.
+
+```python
+from admob_ssv.views import AdmobSSVView
+
+
+class MyAdmobSSVView(AdmobSSVView):
+    def handle_valid_ssv(self, request) -> None:
+        query = request.GET.dict()
+        ad_network = query.get('ad_network')
+        ad_unit = query.get('ad_unit')
+        custom_data = query.get('custom_data')
+        # ...
+```
+
+Finally add a `path` for your custom view to your `urlpatterns`.
+
+```python
+from django.urls import path
+from my_app.views import MyAdmobSSVView
+
+
+urlpatterns = [
+    path('admob-ssv/', MyAdmobSSVView.as_view()),
+]
+```
+
 ## Using a custom ECDSA library
 
 This project uses the [ecdsa](https://pypi.org/project/ecdsa/) Python
 package to verify the signature of incoming Admob SSV callbacks.
 
 If you want to use a different ECDSA library, you may subclass the
 `admob_ssv.views.AdmobSSVView` view and override the `verify_signature`
```

### Comparing `django_admob_ssv-2.0.0/admob_ssv/conf.py` & `django_admob_ssv-2.1.0/admob_ssv/conf.py`

 * *Files identical despite different names*

### Comparing `django_admob_ssv-2.0.0/admob_ssv/views.py` & `django_admob_ssv-2.1.0/admob_ssv/views.py`

 * *Files 4% similar despite different names*

```diff
@@ -28,15 +28,15 @@
         if public_key is None:
             return HttpResponseBadRequest("Unknown key_id")
 
         signature = self.get_signature(request)
         content = self.get_unverified_content(request)
 
         if self.verify_signature(public_key, signature, content):
-            valid_admob_ssv.send(sender=None, query=request.GET.dict())
+            self.handle_valid_ssv(request)
             return HttpResponse()
 
         return HttpResponseBadRequest("Invalid signature")
 
     def get_signature(self, request: HttpRequest) -> bytes:
         encoded_signature = request.GET[self.SIGNATURE_PARAM_NAME]
 
@@ -90,7 +90,10 @@
                 signature,
                 content,
                 hashfunc=hashlib.sha256,
                 sigdecode=sigdecode_der,
             )
         except BadSignatureError:
             return False
+
+    def handle_valid_ssv(self, request: HttpRequest) -> None:
+        valid_admob_ssv.send(sender=None, query=request.GET.dict())
```

### Comparing `django_admob_ssv-2.0.0/pyproject.toml` & `django_admob_ssv-2.1.0/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "django-admob-ssv"
-version = "2.0.0"
+version = "2.1.0"
 description = "Admob server-side verification for Django projects"
 authors = ["Jonathan Ehwald <github@ehwald.info>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "admob_ssv"}]
 homepage = "https://github.com/DoctorJohn/django-admob-ssv"
 repository = "https://github.com/DoctorJohn/django-admob-ssv"
```

### Comparing `django_admob_ssv-2.0.0/PKG-INFO` & `django_admob_ssv-2.1.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-admob-ssv
-Version: 2.0.0
+Version: 2.1.0
 Summary: Admob server-side verification for Django projects
 Home-page: https://github.com/DoctorJohn/django-admob-ssv
 License: MIT
 Author: Jonathan Ehwald
 Author-email: github@ehwald.info
 Requires-Python: >=3.8,<4.0
 Classifier: Environment :: Web Environment
@@ -116,14 +116,48 @@
 ADMOB_SSV_KEY_SERVER_URL = "https://www.gstatic.com/admob/reward/verifier-keys.json",
 
 ADMOB_SSV_KEYS_CACHE_TIMEOUT = timedelta(days=1)
 
 ADMOB_SSV_KEYS_CACHE_KEY = "admob_ssv.public_keys"
 ```
 
+## Usage without Django signals
+
+If you don't want to use Django signals, you may subclass the
+`admob_ssv.views.AdmobSSVView` view and override the `handle_valid_ssv`
+method.
+
+Note that unless you call `super().handle_valid_ssv(request)`,
+the `admob_ssv.signals.valid_admob_ssv` signal won't be sent.
+
+```python
+from admob_ssv.views import AdmobSSVView
+
+
+class MyAdmobSSVView(AdmobSSVView):
+    def handle_valid_ssv(self, request) -> None:
+        query = request.GET.dict()
+        ad_network = query.get('ad_network')
+        ad_unit = query.get('ad_unit')
+        custom_data = query.get('custom_data')
+        # ...
+```
+
+Finally add a `path` for your custom view to your `urlpatterns`.
+
+```python
+from django.urls import path
+from my_app.views import MyAdmobSSVView
+
+
+urlpatterns = [
+    path('admob-ssv/', MyAdmobSSVView.as_view()),
+]
+```
+
 ## Using a custom ECDSA library
 
 This project uses the [ecdsa](https://pypi.org/project/ecdsa/) Python
 package to verify the signature of incoming Admob SSV callbacks.
 
 If you want to use a different ECDSA library, you may subclass the
 `admob_ssv.views.AdmobSSVView` view and override the `verify_signature`
```

