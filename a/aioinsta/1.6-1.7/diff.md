# Comparing `tmp/aioinsta-1.6.tar.gz` & `tmp/aioinsta-1.7.tar.gz`

## Comparing `aioinsta-1.6.tar` & `aioinsta-1.7.tar`

### file list

```diff
@@ -1,21 +1,21 @@
--rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/__init__.py
--rw-r--r--   0        0        0     4488 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/challenge.py
--rw-r--r--   0        0        0      229 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/client.py
--rw-r--r--   0        0        0      147 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/enums.py
--rw-r--r--   0        0        0      276 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/exceptions.py
--rw-r--r--   0        0        0     5334 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/extractors.py
--rw-r--r--   0        0        0      529 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/helpers.py
--rw-r--r--   0        0        0      939 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/idcodec.py
--rw-r--r--   0        0        0     6715 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/login.py
--rw-r--r--   0        0        0     2013 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/media.py
--rw-r--r--   0        0        0     2873 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/parametrs.py
--rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/password.py
--rw-r--r--   0        0        0     7979 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/request.py
--rw-r--r--   0        0        0     1268 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/user.py
--rw-r--r--   0        0        0      817 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/types/media.py
--rw-r--r--   0        0        0      591 2020-02-02 00:00:00.000000 aioinsta-1.6/aioinsta/types/user.py
--rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 aioinsta-1.6/.gitignore
--rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 aioinsta-1.6/LICENSE
--rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 aioinsta-1.6/README.md
--rw-r--r--   0        0        0      677 2020-02-02 00:00:00.000000 aioinsta-1.6/pyproject.toml
--rw-r--r--   0        0        0      850 2020-02-02 00:00:00.000000 aioinsta-1.6/PKG-INFO
+-rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/__init__.py
+-rw-r--r--   0        0        0     4488 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/challenge.py
+-rw-r--r--   0        0        0      229 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/client.py
+-rw-r--r--   0        0        0      147 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/enums.py
+-rw-r--r--   0        0        0      276 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/exceptions.py
+-rw-r--r--   0        0        0     5389 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/extractors.py
+-rw-r--r--   0        0        0      529 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/helpers.py
+-rw-r--r--   0        0        0      939 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/idcodec.py
+-rw-r--r--   0        0        0     6715 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/login.py
+-rw-r--r--   0        0        0     2013 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/media.py
+-rw-r--r--   0        0        0     2873 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/parametrs.py
+-rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/password.py
+-rw-r--r--   0        0        0     7979 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/request.py
+-rw-r--r--   0        0        0     1268 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/user.py
+-rw-r--r--   0        0        0      817 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/types/media.py
+-rw-r--r--   0        0        0      591 2020-02-02 00:00:00.000000 aioinsta-1.7/aioinsta/types/user.py
+-rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 aioinsta-1.7/.gitignore
+-rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 aioinsta-1.7/LICENSE
+-rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 aioinsta-1.7/README.md
+-rw-r--r--   0        0        0      677 2020-02-02 00:00:00.000000 aioinsta-1.7/pyproject.toml
+-rw-r--r--   0        0        0      850 2020-02-02 00:00:00.000000 aioinsta-1.7/PKG-INFO
```

### Comparing `aioinsta-1.6/aioinsta/challenge.py` & `aioinsta-1.7/aioinsta/challenge.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/extractors.py` & `aioinsta-1.7/aioinsta/extractors.py`

 * *Files 1% similar despite different names*

```diff
@@ -31,14 +31,15 @@
     return User(
         profile_pic_url_hd=data.get("hd_profile_pic_url_info").get("url"),
         **data,
     )
 
 
 def extract_user_short(data: dict) -> UserShort:
+    data["pk"] = data.get("id", data.get("pk", None))
     return UserShort(**data)
 
 
 def extract_resource_gql(data: dict) -> Resource:
     media_type = MEDIA_TYPES_GQL[data.get("__typename")]
     display_url = data.get("display_url")
     if data.get("is_video", False):
```

### Comparing `aioinsta-1.6/aioinsta/helpers.py` & `aioinsta-1.7/aioinsta/helpers.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/idcodec.py` & `aioinsta-1.7/aioinsta/idcodec.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/login.py` & `aioinsta-1.7/aioinsta/login.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/media.py` & `aioinsta-1.7/aioinsta/media.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/parametrs.py` & `aioinsta-1.7/aioinsta/parametrs.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/password.py` & `aioinsta-1.7/aioinsta/password.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/request.py` & `aioinsta-1.7/aioinsta/request.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/user.py` & `aioinsta-1.7/aioinsta/user.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/types/media.py` & `aioinsta-1.7/aioinsta/types/media.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/aioinsta/types/user.py` & `aioinsta-1.7/aioinsta/types/user.py`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/.gitignore` & `aioinsta-1.7/.gitignore`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/LICENSE` & `aioinsta-1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/pyproject.toml` & `aioinsta-1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `aioinsta-1.6/PKG-INFO` & `aioinsta-1.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aioinsta
-Version: 1.6
+Version: 1.7
 Summary: Tool for parse instagram data
 Project-URL: Homepage, https://github.com/sheldygg/aioinsta
 Author: sheldy
 License-Expression: MIT
 License-File: LICENSE
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

