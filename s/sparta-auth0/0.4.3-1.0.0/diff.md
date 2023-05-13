# Comparing `tmp/sparta-auth0-0.4.3.tar.gz` & `tmp/sparta-auth0-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sparta-auth0-0.4.3.tar", last modified: Tue Jan 31 14:22:40 2023, max compression
+gzip compressed data, was "sparta-auth0-1.0.0.tar", last modified: Sat May 13 09:10:49 2023, max compression
```

## Comparing `sparta-auth0-0.4.3.tar` & `sparta-auth0-1.0.0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/
--rw-r--r--   0 root         (0) root         (0)     1073 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/LICENSE
--rw-r--r--   0 root         (0) root         (0)     1680 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     1258 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/README.md
--rw-r--r--   0 root         (0) root         (0)       38 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/setup.cfg
--rw-r--r--   0 root         (0) root         (0)     1415 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-01-31 14:22:40.331653 sparta-auth0-0.4.3/src/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/src/sparta/
--rw-r--r--   0 root         (0) root         (0)       56 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/src/sparta/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/src/sparta/auth0/
--rw-r--r--   0 root         (0) root         (0)      120 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/src/sparta/auth0/__init__.py
--rw-r--r--   0 root         (0) root         (0)     3179 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/src/sparta/auth0/token_provider.py
--rw-r--r--   0 root         (0) root         (0)     9685 2023-01-31 14:22:20.000000 sparta-auth0-0.4.3/src/sparta/auth0/token_verifier.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-01-31 14:22:40.335653 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/
--rw-r--r--   0 root         (0) root         (0)     1680 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      396 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)        7 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/namespace_packages.txt
--rw-r--r--   0 root         (0) root         (0)       27 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        7 2023-01-31 14:22:40.000000 sparta-auth0-0.4.3/src/sparta_auth0.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 09:10:49.215134 sparta-auth0-1.0.0/
+-rw-r--r--   0 root         (0) root         (0)     1073 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     1680 2023-05-13 09:10:49.215134 sparta-auth0-1.0.0/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     1258 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/README.md
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 09:10:49.215134 sparta-auth0-1.0.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)     1415 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 09:10:49.207133 sparta-auth0-1.0.0/src/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 09:10:49.211134 sparta-auth0-1.0.0/src/sparta/
+-rw-r--r--   0 root         (0) root         (0)       56 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/src/sparta/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 09:10:49.211134 sparta-auth0-1.0.0/src/sparta/auth0/
+-rw-r--r--   0 root         (0) root         (0)      120 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/src/sparta/auth0/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     3179 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/src/sparta/auth0/token_provider.py
+-rw-r--r--   0 root         (0) root         (0)     9762 2023-05-13 09:10:11.000000 sparta-auth0-1.0.0/src/sparta/auth0/token_verifier.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 09:10:49.215134 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     1680 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      396 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)        7 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/namespace_packages.txt
+-rw-r--r--   0 root         (0) root         (0)       27 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        7 2023-05-13 09:10:49.000000 sparta-auth0-1.0.0/src/sparta_auth0.egg-info/top_level.txt
```

### Comparing `sparta-auth0-0.4.3/LICENSE` & `sparta-auth0-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `sparta-auth0-0.4.3/PKG-INFO` & `sparta-auth0-1.0.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sparta-auth0
-Version: 0.4.3
+Version: 1.0.0
 Summary: Sparta Auth0 library
 Home-page: https://github.com/Spartan-Approach/sparta-auth0
 Author: Spartan Approach
 Author-email: sparta@spartanapproach.com
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `sparta-auth0-0.4.3/README.md` & `sparta-auth0-1.0.0/README.md`

 * *Files identical despite different names*

### Comparing `sparta-auth0-0.4.3/setup.py` & `sparta-auth0-1.0.0/setup.py`

 * *Files identical despite different names*

### Comparing `sparta-auth0-0.4.3/src/sparta/auth0/token_provider.py` & `sparta-auth0-1.0.0/src/sparta/auth0/token_provider.py`

 * *Files identical despite different names*

### Comparing `sparta-auth0-0.4.3/src/sparta/auth0/token_verifier.py` & `sparta-auth0-1.0.0/src/sparta/auth0/token_verifier.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,20 +7,21 @@
 
 
 class TokenPayload(dict):
     """
     Helper class to access properties inside the token payload
     """
 
-    def __init__(self, raw_payload: dict) -> None:
+    def __init__(self, raw_payload: dict, raw_token: str = None) -> None:
         super().__init__(raw_payload)
+        self.raw_token = raw_token
 
     @classmethod
     def parse(cls, raw_token: str):
-        return cls(jwt.get_unverified_claims(raw_token))
+        return cls(jwt.get_unverified_claims(raw_token), raw_token=raw_token)
 
     def get_claim(
         self, claim_name: str, claim_default_value: typing.Optional[typing.Any] = None
     ) -> typing.Any:
         """
         Returns the claim value if present, or claim_default_value
         """
@@ -279,14 +280,14 @@
                     if permission not in token_permissions:
                         raise AuthError(
                             status_code=403,
                             code="missing_permission",
                             description=f"You don't have access to this resource. Permission '{permission}' is missing.",
                         )
 
-            return token_payload_class(raw_payload=raw_payload)
+            return token_payload_class.parse(raw_token=token)
 
         raise AuthError(
             status_code=401,
             code="invalid_header",
             description="Unable to find appropriate key.",
         )
```

### Comparing `sparta-auth0-0.4.3/src/sparta_auth0.egg-info/PKG-INFO` & `sparta-auth0-1.0.0/src/sparta_auth0.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sparta-auth0
-Version: 0.4.3
+Version: 1.0.0
 Summary: Sparta Auth0 library
 Home-page: https://github.com/Spartan-Approach/sparta-auth0
 Author: Spartan Approach
 Author-email: sparta@spartanapproach.com
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

