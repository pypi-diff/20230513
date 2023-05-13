# Comparing `tmp/aioinsta-1.5.tar.gz` & `tmp/aioinsta-1.6.tar.gz`

## Comparing `aioinsta-1.5.tar` & `aioinsta-1.6.tar`

### file list

```diff
@@ -1,21 +1,21 @@
--rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/__init__.py
--rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/challenge.py
--rw-r--r--   0        0        0      229 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/client.py
--rw-r--r--   0        0        0      158 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/enums.py
--rw-r--r--   0        0        0      161 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/exceptions.py
--rw-r--r--   0        0        0     2940 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/extractors.py
--rw-r--r--   0        0        0      529 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/helpers.py
--rw-r--r--   0        0        0      939 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/idcodec.py
--rw-r--r--   0        0        0     6364 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/login.py
--rw-r--r--   0        0        0     1500 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/media.py
--rw-r--r--   0        0        0     2873 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/parametrs.py
--rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/password.py
--rw-r--r--   0        0        0     7766 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/request.py
--rw-r--r--   0        0        0     1268 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/user.py
--rw-r--r--   0        0        0      806 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/types/media.py
--rw-r--r--   0        0        0      591 2020-02-02 00:00:00.000000 aioinsta-1.5/aioinsta/types/user.py
--rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 aioinsta-1.5/.gitignore
--rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 aioinsta-1.5/LICENSE
--rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 aioinsta-1.5/README.md
--rw-r--r--   0        0        0      656 2020-02-02 00:00:00.000000 aioinsta-1.5/pyproject.toml
--rw-r--r--   0        0        0      821 2020-02-02 00:00:00.000000 aioinsta-1.5/PKG-INFO
+-rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/__init__.py
+-rw-r--r--   0        0        0     4488 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/challenge.py
+-rw-r--r--   0        0        0      229 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/client.py
+-rw-r--r--   0        0        0      147 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/enums.py
+-rw-r--r--   0        0        0      276 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/exceptions.py
+-rw-r--r--   0        0        0     5334 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/extractors.py
+-rw-r--r--   0        0        0      529 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/helpers.py
+-rw-r--r--   0        0        0      939 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/idcodec.py
+-rw-r--r--   0        0        0     6715 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/login.py
+-rw-r--r--   0        0        0     2013 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/media.py
+-rw-r--r--   0        0        0     2873 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/parametrs.py
+-rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/password.py
+-rw-r--r--   0        0        0     7979 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/request.py
+-rw-r--r--   0        0        0     1268 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/user.py
+-rw-r--r--   0        0        0      817 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/types/media.py
+-rw-r--r--   0        0        0      591 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/types/user.py
+-rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 aioinsta-1.6/.gitignore
+-rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 aioinsta-1.6/LICENSE
+-rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 aioinsta-1.6/README.md
+-rw-r--r--   0        0        0      677 2020-02-02 00:00:00.000000 aioinsta-1.6/pyproject.toml
+-rw-r--r--   0        0        0      850 2020-02-02 00:00:00.000000 aioinsta-1.6/PKG-INFO
```

### Comparing `aioinsta-1.5/aioinsta/helpers.py` & `aioinsta-1.6/aioinsta/helpers.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/aioinsta/idcodec.py` & `aioinsta-1.6/aioinsta/idcodec.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/aioinsta/login.py` & `aioinsta-1.6/aioinsta/login.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,26 +3,28 @@
 
 from aioinsta.challenge import ChallengeClient
 from aioinsta.helpers import generate_android_device_id, generate_jazoest, generate_uuid
 from aioinsta.media import MediaClient
 from aioinsta.password import PasswordClient
 from aioinsta.request import PrivateRequestClient, PublicRequestClient
 from aioinsta.user import UserClient
+from aioinsta.exceptions import IncorrectPassword
 
 
 class Login(
     PrivateRequestClient,
     PublicRequestClient,
     PasswordClient,
     ChallengeClient,
     UserClient,
     MediaClient,
 ):
     def __init__(self, settings: dict):
         self.settings: dict = settings
+        self.username = None
         self.user_agent = None
         self.authorization_data = {}
         self.device_settings = None
         self.uuid = None
         self.phone_id = None
         self.device_id = None
         self.client_session_id = None
@@ -117,14 +119,15 @@
 
     def user_id(self) -> int | None:
         user_id = self.authorization_data.get("ds_user_id")
         if user_id:
             return int(user_id)
 
     async def login(self, username: str, password: str):
+        self.username = username
         await self.pre_login_flow()
         enc_password = await self.password_encrypt(password)
         data = {
             "jazoest": generate_jazoest(self.phone_id),
             "country_codes": json.dumps(
                 [{"country_code": str(self.country_code), "source": ["default"]}]
             ),
@@ -136,14 +139,17 @@
             "device_id": self.android_device_id,
             "google_tokens": "[]",
             "login_attempt_count": "0",
         }
         loggin_data = await self.private_request(
             method="POST", path="accounts/login/", data=data, raise_for_status=True
         )
+        response = loggin_data.get("response")
+        if response.get("status") == "fail" and response.get("error_title") == "Incorrect password":
+            raise IncorrectPassword("Entered incorrect password, doblecheck please")
         headers = loggin_data.get("headers")
         self.authorization_data = self.parse_authorization(
             headers.get("ig-set-authorization")
         )
 
     def get_settings(self) -> dict:
         return {
```

### Comparing `aioinsta-1.5/aioinsta/media.py` & `aioinsta-1.6/aioinsta/media.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from urllib.parse import urlparse
 
 from aioinsta import login
-from aioinsta.extractors import extract_media_gql
+from aioinsta.extractors import extract_media_gql, extract_media_v1
 from aioinsta.idcodec import InstagramIdCodec
 from aioinsta.types.media import Media
+from aioinsta.exceptions import RateLimit
 
 
 class MediaClient:
     def __init__(self, login_client: "login.Login"):
         self.login_client = login_client
 
     @staticmethod
@@ -33,11 +34,23 @@
     async def media_info_a1(self, media_pk: str, max_id: str | None = None) -> Media:
         media_pk = self.media_pk(media_pk)
         shortcode = self.media_code_from_pk(media_pk)
         params = {"max_id": max_id} if max_id else None
         response = await self.login_client.public_a1_request(
             method="GET", path=f"/p/{shortcode}", params=params
         )
+        # raise RateLimit()
         return extract_media_gql(response.get("shortcode_media"))
 
+    async def media_info_v1(self, media_pk: str) -> Media:
+        response = await self.login_client.private_request(
+            method="GET",
+            path=f"media/{media_pk}/info/",
+            raise_for_status=True
+        )
+        return extract_media_v1(response.get("response").get("items", {}).pop())
+
     async def media_info(self, media_pk) -> Media:
-        return await self.media_info_a1(media_pk)
+        try:
+            return await self.media_info_a1(media_pk)
+        except RateLimit:
+            return await self.media_info_v1(media_pk)
```

### Comparing `aioinsta-1.5/aioinsta/parametrs.py` & `aioinsta-1.6/aioinsta/parametrs.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/aioinsta/password.py` & `aioinsta-1.6/aioinsta/password.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/aioinsta/request.py` & `aioinsta-1.6/aioinsta/request.py`

 * *Files 2% similar despite different names*

```diff
@@ -37,22 +37,22 @@
             try:
                 response = await resp.json()
             except ContentTypeError:
                 response = await resp.read()
             self.last_response = response
             if raise_for_status and not resp.ok:
                 error_type = response.get("error_type")
+                message = response.get("message")
                 if resp.status == 400:
                     if error_type == ErrorTypes.RATE_LIMIT_ERROR:
                         raise RateLimit(
                             "Please wait a few minutes before you try again."
                         )
-                    elif error_type == ErrorTypes.CHALLENGE_REQUIRED:
+                    elif message == ErrorTypes.CHALLENGE_REQUIRED:
                         raise ChallengeRequired("Challenge Required")
-            self.login_client.mid = response_headers.get("ig-set-x-mid")
             return dict(response=response, headers=response_headers)
 
     async def close(self):
         return await self.session.close()
 
     def set_user_agent(self, user_agent: str | None = None):
         data = dict(self.login_client.device_settings, locale=self.login_client.locale)
@@ -138,17 +138,17 @@
                 method=method,
                 url=url,
                 data=data,
                 params=params,
                 headers=self.base_headers(),
                 raise_for_status=raise_for_status,
             )
+            self.login_client.mid = response.get("headers", {}).get("ig-set-x-mid")
             return response
         except ChallengeRequired:
-            print("yes")
             return await self.login_client.resolve_challenge(self.last_response)
 
 
 class PublicRequestClient:
     def __init__(self, login_client: "login.Login"):
         self.login_client = login_client
         self.session = ClientSession()
@@ -181,9 +181,11 @@
         method: str,
         path: str,
         params: dict | None = None,
     ):
         url = urljoin(parametrs.PUBLIC_API_DOMAIN, path)
         params = params or {}
         params.update({"__a": 1, "__d": "dis"})
-        response = await self.public_request(method=method, url=url, params=params)
-        return response.get("response").get("graphql")
+        response = (await self.public_request(method=method, url=url, params=params)).get("response")
+        if response.get("message", "") == "Please wait a few minutes before you try again.":
+            raise RateLimit("Please wait a few minutes before you try again.")
+        return response.get("graphql", {})
```

### Comparing `aioinsta-1.5/aioinsta/user.py` & `aioinsta-1.6/aioinsta/user.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/aioinsta/types/media.py` & `aioinsta-1.6/aioinsta/types/media.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
     Photo = "photo"
     Album = "album"
 
 
 class Video(BaseModel):
     url: HttpUrl
     preview: HttpUrl
-    view_count: int
+    view_count: int | None = 0
     duration: float | None = 0.0
 
 
 class Photo(BaseModel):
     url: HttpUrl
```

### Comparing `aioinsta-1.5/aioinsta/types/user.py` & `aioinsta-1.6/aioinsta/types/user.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/.gitignore` & `aioinsta-1.6/.gitignore`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/LICENSE` & `aioinsta-1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `aioinsta-1.5/pyproject.toml` & `aioinsta-1.6/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 classifiers = [
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
 ]
 dependencies = [
     "aiohttp",
     "pydantic",
+    "pycryptodomex"
 ]
 
 [project.urls]
 Homepage = "https://github.com/sheldygg/aioinsta"
 
 [tool.hatch.version]
 path = "aioinsta/__init__.py"
```

### Comparing `aioinsta-1.5/PKG-INFO` & `aioinsta-1.6/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 Metadata-Version: 2.1
 Name: aioinsta
-Version: 1.5
+Version: 1.6
 Summary: Tool for parse instagram data
 Project-URL: Homepage, https://github.com/sheldygg/aioinsta
 Author: sheldy
 License-Expression: MIT
 License-File: LICENSE
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Requires-Dist: aiohttp
+Requires-Dist: pycryptodomex
 Requires-Dist: pydantic
 Description-Content-Type: text/markdown
 
 # aioINSTA
 
 # Still in development
```

