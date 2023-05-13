# Comparing `tmp/mpcontribs-client-5.3.2.tar.gz` & `tmp/mpcontribs-client-5.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mpcontribs-client-5.3.2.tar", last modified: Fri May 12 18:36:15 2023, max compression
+gzip compressed data, was "mpcontribs-client-5.3.3.tar", last modified: Sat May 13 01:56:42 2023, max compression
```

## Comparing `mpcontribs-client-5.3.2.tar` & `mpcontribs-client-5.3.3.tar`

### file list

```diff
@@ -1,33 +1,33 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.154985 mpcontribs-client-5.3.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1838 2023-05-12 18:36:15.154985 mpcontribs-client-5.3.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.142984 mpcontribs-client-5.3.2/mpcontribs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.146984 mpcontribs-client-5.3.2/mpcontribs/client/
--rw-r--r--   0 runner    (1001) docker     (123)    85535 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/mpcontribs/client/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.150985 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1838 2023-05-12 18:36:14.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      851 2023-05-12 18:36:15.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 18:36:14.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 18:36:14.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      243 2023-05-12 18:36:14.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-12 18:36:14.000000 mpcontribs-client-5.3.2/mpcontribs_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.154985 mpcontribs-client-5.3.2/requirements/
--rw-r--r--   0 runner    (1001) docker     (123)     5622 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/deployment.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4922 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.10.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5774 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.10_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5105 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.8.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5957 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.8_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5028 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.9.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5880 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/macos-latest_py3.9_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4890 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.10.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5742 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.10_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5073 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.8.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5925 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.8_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4996 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.9.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5848 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.9_extras.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 18:36:15.154985 mpcontribs-client-5.3.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1450 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:36:15.154985 mpcontribs-client-5.3.2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      318 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     3020 2023-05-12 18:36:00.000000 mpcontribs-client-5.3.2/tests/test_client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.050608 mpcontribs-client-5.3.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1838 2023-05-13 01:56:42.050608 mpcontribs-client-5.3.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.042608 mpcontribs-client-5.3.3/mpcontribs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.042608 mpcontribs-client-5.3.3/mpcontribs/client/
+-rw-r--r--   0 runner    (1001) docker     (123)    85643 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/mpcontribs/client/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.046608 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1838 2023-05-13 01:56:41.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      851 2023-05-13 01:56:42.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 01:56:41.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 01:56:41.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      243 2023-05-13 01:56:41.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 01:56:41.000000 mpcontribs-client-5.3.3/mpcontribs_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.050608 mpcontribs-client-5.3.3/requirements/
+-rw-r--r--   0 runner    (1001) docker     (123)     5620 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/deployment.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4922 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.10.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5774 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.10_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5105 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.8.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5957 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.8_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5028 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.9.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5880 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/macos-latest_py3.9_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4890 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.10.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5742 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.10_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5073 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.8.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5925 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.8_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4996 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.9.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5848 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.9_extras.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 01:56:42.050608 mpcontribs-client-5.3.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1450 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:56:42.050608 mpcontribs-client-5.3.3/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      318 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3020 2023-05-13 01:56:26.000000 mpcontribs-client-5.3.3/tests/test_client.py
```

### Comparing `mpcontribs-client-5.3.2/LICENSE` & `mpcontribs-client-5.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `mpcontribs-client-5.3.2/PKG-INFO` & `mpcontribs-client-5.3.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mpcontribs-client
-Version: 5.3.2
+Version: 5.3.3
 Summary: client library for MPContribs API
 Home-page: https://github.com/materialsproject/MPContribs/tree/master/mpcontribs-client
 Author: Patrick Huck
 Author-email: phuck@lbl.gov
 License: MIT
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `mpcontribs-client-5.3.2/README.md` & `mpcontribs-client-5.3.3/README.md`

 * *Files identical despite different names*

### Comparing `mpcontribs-client-5.3.2/mpcontribs/client/__init__.py` & `mpcontribs-client-5.3.3/mpcontribs/client/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -992,22 +992,24 @@
         if not self.get_totals(query={"name": name}, resource="projects")[0]:
             raise MPContribsClientError(f"Project `{name}` doesn't exist!")
 
         resp = self.projects.deleteProjectByName(pk=name).result()
         if resp and "error" in resp:
             raise MPContribsClientError(resp["error"])
 
-    def get_contribution(self, cid: str) -> Type[Dict]:
-        """Retrieve full contribution entry
+    def get_contribution(self, cid: str, fields: list = None) -> Type[Dict]:
+        """Retrieve a contribution
 
         Args:
             cid (str): contribution ObjectID
+            fields (list): list of fields to include in response
         """
-        fields = list(self.get_model("ContributionsSchema")._properties.keys())
-        fields.remove("needs_build")  # internal field
+        if not fields:
+            fields = list(self.get_model("ContributionsSchema")._properties.keys())
+            fields.remove("needs_build")  # internal field
         return Dict(self.contributions.getContributionById(pk=cid, _fields=fields).result())
 
     def get_table(self, tid_or_md5: str) -> Type[Table]:
         """Retrieve full Pandas DataFrame for a table
 
         Args:
             tid_or_md5 (str): ObjectId or MD5 hash digest for table
```

### Comparing `mpcontribs-client-5.3.2/mpcontribs_client.egg-info/PKG-INFO` & `mpcontribs-client-5.3.3/mpcontribs_client.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mpcontribs-client
-Version: 5.3.2
+Version: 5.3.3
 Summary: client library for MPContribs API
 Home-page: https://github.com/materialsproject/MPContribs/tree/master/mpcontribs-client
 Author: Patrick Huck
 Author-email: phuck@lbl.gov
 License: MIT
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `mpcontribs-client-5.3.2/mpcontribs_client.egg-info/SOURCES.txt` & `mpcontribs-client-5.3.3/mpcontribs_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mpcontribs-client-5.3.2/requirements/deployment.txt` & `mpcontribs-client-5.3.3/requirements/deployment.txt`

 * *Files 2% similar despite different names*

```diff
@@ -28,23 +28,23 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.2
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
-fonttools==4.39.3
+fonttools==4.39.4
     # via matplotlib
 fqdn==1.5.1
     # via jsonschema
 future==0.18.3
     # via uncertainties
 idna==3.4
     # via
@@ -79,15 +79,15 @@
 monotonic==1.6
     # via bravado
 monty==2023.5.8
     # via
     #   emmet-core
     #   mp-api
     #   pymatgen
-mp-api==0.33.1
+mp-api==0.33.2
     # via pymatgen
 mpmath==1.3.0
     # via sympy
 msgpack==1.0.5
     # via
     #   bravado
     #   bravado-core
@@ -140,15 +140,15 @@
     #   pymatgen
 pydantic==1.10.7
     # via emmet-core
 pygments==2.15.1
     # via ipython
 pyisemail==2.0.1
     # via mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
-pymatgen==2023.3.23
+pymatgen==2023.5.10
     # via
     #   emmet-core
     #   mp-api
     #   mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
 pymongo==4.3.3
     # via mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
 pyparsing==3.0.9
@@ -181,15 +181,15 @@
     #   requests-futures
 requests-futures==1.0.0
     # via mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
 rfc3339-validator==0.1.4
     # via jsonschema
 rfc3987==1.3.8
     # via jsonschema
-ruamel-yaml==0.17.24
+ruamel-yaml==0.17.26
     # via pymatgen
 ruamel-yaml-clib==0.2.7
     # via ruamel-yaml
 scipy==1.10.1
     # via
     #   -r python/requirements.txt
     #   pymatgen
@@ -215,15 +215,15 @@
     #   pymatgen
 stack-data==0.6.2
     # via ipython
 swagger-spec-validator==3.0.3
     # via
     #   bravado-core
     #   mpcontribs-client (MPContribs/mpcontribs-client/setup.py)
-sympy==1.11.1
+sympy==1.12
     # via pymatgen
 tabulate==0.9.0
     # via pymatgen
 tenacity==8.2.2
     # via plotly
 tqdm==4.65.0
     # via
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.10.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.10.txt`

 * *Files 1% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.10_extras.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.10_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -32,15 +32,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.8.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.8.txt`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.8_extras.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.8_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -32,15 +32,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.9.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.9.txt`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/macos-latest_py3.9_extras.txt` & `mpcontribs-client-5.3.3/requirements/macos-latest_py3.9_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -32,15 +32,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.10.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.10.txt`

 * *Files 1% similar despite different names*

```diff
@@ -28,15 +28,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.10_extras.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.10_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.8.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.8.txt`

 * *Files 0% similar despite different names*

```diff
@@ -28,15 +28,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.8_extras.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.8_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.9.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.9.txt`

 * *Files 1% similar despite different names*

```diff
@@ -28,15 +28,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
 flatten-dict==0.4.2
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/requirements/ubuntu-latest_py3.9_extras.txt` & `mpcontribs-client-5.3.3/requirements/ubuntu-latest_py3.9_extras.txt`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
     # via matplotlib
 decorator==5.1.1
     # via ipython
 dnspython==2.3.0
     # via
     #   pyisemail
     #   pymongo
-emmet-core==0.54.6
+emmet-core==0.55.0
     # via mp-api
 exceptiongroup==1.1.1
     # via pytest
 executing==1.2.0
     # via stack-data
 filetype==1.2.0
     # via mpcontribs-client (setup.py)
```

### Comparing `mpcontribs-client-5.3.2/setup.py` & `mpcontribs-client-5.3.3/setup.py`

 * *Files identical despite different names*

### Comparing `mpcontribs-client-5.3.2/tests/test_client.py` & `mpcontribs-client-5.3.3/tests/test_client.py`

 * *Files identical despite different names*

