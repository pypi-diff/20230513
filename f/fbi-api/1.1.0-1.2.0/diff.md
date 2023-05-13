# Comparing `tmp/fbi-api-1.1.0.tar.gz` & `tmp/fbi-api-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fbi-api-1.1.0.tar", last modified: Sat May 13 09:22:36 2023, max compression
+gzip compressed data, was "fbi-api-1.2.0.tar", last modified: Sat May 13 11:47:31 2023, max compression
```

## Comparing `fbi-api-1.1.0.tar` & `fbi-api-1.2.0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:22:36.168273 fbi-api-1.1.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:22:36.164273 fbi-api-1.1.0/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      501 2023-05-13 09:22:24.000000 fbi-api-1.1.0/.github/dependabot.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:22:36.164273 fbi-api-1.1.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-05-13 09:22:24.000000 fbi-api-1.1.0/.github/workflows/codeql.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-13 09:22:24.000000 fbi-api-1.1.0/.github/workflows/python-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)    35146 2023-05-13 09:22:24.000000 fbi-api-1.1.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    42318 2023-05-13 09:22:36.168273 fbi-api-1.1.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      911 2023-05-13 09:22:24.000000 fbi-api-1.1.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:22:36.164273 fbi-api-1.1.0/fbi/
--rw-r--r--   0 runner    (1001) docker     (123)     2456 2023-05-13 09:22:24.000000 fbi-api-1.1.0/fbi/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 09:22:24.000000 fbi-api-1.1.0/fbi/connection.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:22:36.168273 fbi-api-1.1.0/fbi_api.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    42318 2023-05-13 09:22:36.000000 fbi-api-1.1.0/fbi_api.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      309 2023-05-13 09:22:36.000000 fbi-api-1.1.0/fbi_api.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:22:36.000000 fbi-api-1.1.0/fbi_api.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 09:22:36.000000 fbi-api-1.1.0/fbi_api.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 09:22:36.000000 fbi-api-1.1.0/fbi_api.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-05-13 09:22:24.000000 fbi-api-1.1.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:22:36.168273 fbi-api-1.1.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:47:31.495931 fbi-api-1.2.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:47:31.491931 fbi-api-1.2.0/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      501 2023-05-13 11:47:18.000000 fbi-api-1.2.0/.github/dependabot.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:47:31.491931 fbi-api-1.2.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-05-13 11:47:18.000000 fbi-api-1.2.0/.github/workflows/codeql.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-13 11:47:18.000000 fbi-api-1.2.0/.github/workflows/python-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    35146 2023-05-13 11:47:18.000000 fbi-api-1.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    42318 2023-05-13 11:47:31.495931 fbi-api-1.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      911 2023-05-13 11:47:18.000000 fbi-api-1.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:47:31.495931 fbi-api-1.2.0/fbi/
+-rw-r--r--   0 runner    (1001) docker     (123)     2466 2023-05-13 11:47:18.000000 fbi-api-1.2.0/fbi/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-05-13 11:47:18.000000 fbi-api-1.2.0/fbi/connection.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:47:31.495931 fbi-api-1.2.0/fbi_api.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    42318 2023-05-13 11:47:31.000000 fbi-api-1.2.0/fbi_api.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      309 2023-05-13 11:47:31.000000 fbi-api-1.2.0/fbi_api.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:47:31.000000 fbi-api-1.2.0/fbi_api.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 11:47:31.000000 fbi-api-1.2.0/fbi_api.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 11:47:31.000000 fbi-api-1.2.0/fbi_api.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-05-13 11:47:18.000000 fbi-api-1.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:47:31.495931 fbi-api-1.2.0/setup.cfg
```

### Comparing `fbi-api-1.1.0/.github/workflows/codeql.yml` & `fbi-api-1.2.0/.github/workflows/codeql.yml`

 * *Files identical despite different names*

### Comparing `fbi-api-1.1.0/.github/workflows/python-publish.yml` & `fbi-api-1.2.0/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `fbi-api-1.1.0/LICENSE` & `fbi-api-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `fbi-api-1.1.0/PKG-INFO` & `fbi-api-1.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fbi-api
-Version: 1.1.0
+Version: 1.2.0
 Summary: A Python wrapper around the FBI API (unofficial)
 Author-email: Richard Mwewa <rly0nheart@duck.com>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
```

### Comparing `fbi-api-1.1.0/README.md` & `fbi-api-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `fbi-api-1.1.0/fbi/__init__.py` & `fbi-api-1.2.0/fbi/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from typing import Union, Literal
-from fbi.connection import get_api_response
+from fbi.connection import __get_api_response
 
 
 def wanted(person_classification: Union[Literal['Main'], Literal['Accomplice'], Literal['Victim']] = None,
            page_size: int = 20, page: int = 1, sort_order: Union[Literal['asc'], Literal['desc']] = None) -> dict:
     """
     Get listing of wanted people
     :param person_classification: person classification
@@ -18,25 +18,25 @@
         person_classification = f"&person_classification={person_classification}"
 
     if sort_order is None:
         sort_order = ""
     else:
         sort_order = f"&sort_order={sort_order}"
 
-    response = get_api_response(f"https://api.fbi.gov/@wanted?pageSize={page_size}&page={page}{person_classification}")
+    response = __get_api_response(f"https://api.fbi.gov/@wanted?pageSize={page_size}&page={page}{person_classification}")
     return response['items']
 
 
 def wanted_person(person_id: str) -> dict:
     """
     Retrieve information on wanted person
     :param person_id: id of wanted person
     :return: a dictionary of person's information
     """
-    return get_api_response(f"https://api.fbi.gov/@wanted-person/{person_id}")
+    return __get_api_response(f"https://api.fbi.gov/@wanted-person/{person_id}")
 
 
 def art_crimes(page_size: int = 20, page: int = 1, sort_order: Union[Literal['asc'], Literal['desc'], None] = None,
                reference_number: Union[int, str] = None) -> dict:
     """
     Get listing of national art theft
     :param page_size: number of items to return
@@ -51,19 +51,19 @@
         reference_number = f"&referenceNumber={reference_number}"
 
     if sort_order is None:
         sort_order = ""
     else:
         sort_order = f"&sort_order={sort_order}"
 
-    response = get_api_response(f"https://api.fbi.gov/@artcrimes?pageSize={page_size}&page={page}"
+    response = __get_api_response(f"https://api.fbi.gov/@artcrimes?pageSize={page_size}&page={page}"
                                 f"{sort_order}{reference_number}")
     return response['items']
 
 
 def art_crime(crime_id: str) -> dict:
     """
     Retrieve information on an art crime
     :param crime_id: id of an art crime
     :return: dictionary of an art crime's information
     """
-    return get_api_response(f"https://api.fbi.gov/@artcrimes/{crime_id}")
+    return __get_api_response(f"https://api.fbi.gov/@artcrimes/{crime_id}")
```

### Comparing `fbi-api-1.1.0/fbi_api.egg-info/PKG-INFO` & `fbi-api-1.2.0/fbi_api.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fbi-api
-Version: 1.1.0
+Version: 1.2.0
 Summary: A Python wrapper around the FBI API (unofficial)
 Author-email: Richard Mwewa <rly0nheart@duck.com>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
```

### Comparing `fbi-api-1.1.0/pyproject.toml` & `fbi-api-1.2.0/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools", "setuptools-scm"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "fbi-api"
-version = "1.1.0"
+version = "1.2.0"
 description = "A Python wrapper around the FBI API (unofficial)"
 readme = "README.md"
 requires-python = ">=3.9"
 license = {file = "LICENSE"}
 keywords = ["crime-data", "fbi", "most-wanted", "fbi-project", "fbi-crime-api", "wanted-persons"]
 authors = [{name = "Richard Mwewa", email = "rly0nheart@duck.com"}]
 classifiers = [
```

