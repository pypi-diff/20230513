# Comparing `tmp/xhs-0.2.0.tar.gz` & `tmp/xhs-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xhs-0.2.0.tar", last modified: Wed May 10 02:36:50 2023, max compression
+gzip compressed data, was "xhs-0.2.1.tar", last modified: Sat May 13 03:35:20 2023, max compression
```

## Comparing `xhs-0.2.0.tar` & `xhs-0.2.1.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 02:36:50.052827 xhs-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1769 2023-05-10 02:36:33.000000 xhs-0.2.0/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-05-10 02:36:33.000000 xhs-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-10 02:36:33.000000 xhs-0.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4242 2023-05-10 02:36:50.052827 xhs-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3336 2023-05-10 02:36:33.000000 xhs-0.2.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-10 02:36:33.000000 xhs-0.2.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      282 2023-05-10 02:36:50.052827 xhs-0.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1434 2023-05-10 02:36:33.000000 xhs-0.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 02:36:50.052827 xhs-0.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-10 02:36:33.000000 xhs-0.2.0/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-05-10 02:36:33.000000 xhs-0.2.0/tests/test_help.py
--rw-r--r--   0 runner    (1001) docker     (123)     5607 2023-05-10 02:36:33.000000 xhs-0.2.0/tests/test_xhs.py
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-10 02:36:33.000000 xhs-0.2.0/tests/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 02:36:50.052827 xhs-0.2.0/xhs/
--rw-r--r--   0 runner    (1001) docker     (123)      405 2023-05-10 02:36:33.000000 xhs-0.2.0/xhs/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      448 2023-05-10 02:36:33.000000 xhs-0.2.0/xhs/__version__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21588 2023-05-10 02:36:33.000000 xhs-0.2.0/xhs/core.py
--rw-r--r--   0 runner    (1001) docker     (123)      209 2023-05-10 02:36:33.000000 xhs-0.2.0/xhs/exception.py
--rw-r--r--   0 runner    (1001) docker     (123)    11732 2023-05-10 02:36:33.000000 xhs-0.2.0/xhs/help.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 02:36:50.052827 xhs-0.2.0/xhs.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4242 2023-05-10 02:36:50.000000 xhs-0.2.0/xhs.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-10 02:36:50.000000 xhs-0.2.0/xhs.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 02:36:50.000000 xhs-0.2.0/xhs.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 02:36:49.000000 xhs-0.2.0/xhs.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-10 02:36:50.000000 xhs-0.2.0/xhs.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-10 02:36:50.000000 xhs-0.2.0/xhs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:35:20.098182 xhs-0.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1852 2023-05-13 03:35:06.000000 xhs-0.2.1/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-05-13 03:35:06.000000 xhs-0.2.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:35:06.000000 xhs-0.2.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4470 2023-05-13 03:35:20.098182 xhs-0.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3564 2023-05-13 03:35:06.000000 xhs-0.2.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 03:35:06.000000 xhs-0.2.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      282 2023-05-13 03:35:20.098182 xhs-0.2.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1434 2023-05-13 03:35:06.000000 xhs-0.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:35:20.094182 xhs-0.2.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-13 03:35:06.000000 xhs-0.2.1/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-05-13 03:35:06.000000 xhs-0.2.1/tests/test_help.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5684 2023-05-13 03:35:06.000000 xhs-0.2.1/tests/test_xhs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 03:35:06.000000 xhs-0.2.1/tests/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:35:20.098182 xhs-0.2.1/xhs/
+-rw-r--r--   0 runner    (1001) docker     (123)      405 2023-05-13 03:35:06.000000 xhs-0.2.1/xhs/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      448 2023-05-13 03:35:06.000000 xhs-0.2.1/xhs/__version__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21617 2023-05-13 03:35:06.000000 xhs-0.2.1/xhs/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)      209 2023-05-13 03:35:06.000000 xhs-0.2.1/xhs/exception.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11732 2023-05-13 03:35:06.000000 xhs-0.2.1/xhs/help.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:35:20.098182 xhs-0.2.1/xhs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4470 2023-05-13 03:35:20.000000 xhs-0.2.1/xhs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-13 03:35:20.000000 xhs-0.2.1/xhs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:35:20.000000 xhs-0.2.1/xhs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:35:19.000000 xhs-0.2.1/xhs.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 03:35:20.000000 xhs-0.2.1/xhs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 03:35:20.000000 xhs-0.2.1/xhs.egg-info/top_level.txt
```

### Comparing `xhs-0.2.0/CHANGELOG.md` & `xhs-0.2.1/CHANGELOG.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,20 @@
 # Changelog
 
 ## dev
 
 - Improve documentation
 - Add more test function
 
+## 0.2.1
+
+### Fixed
+
+- fixed get_note_by_id_from_html with video note parse error
+
 ## 0.2.0
 
 ### Fixed
 
 - fixed save_files_from_note_id error
 - fixed get_user_all_notes abnormal notes catch error
```

### Comparing `xhs-0.2.0/LICENSE` & `xhs-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `xhs-0.2.0/PKG-INFO` & `xhs-0.2.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xhs
-Version: 0.2.0
+Version: 0.2.1
 Summary: xiaohongshu crawl sdk.
 Home-page: https://github.com/ReaJason/xhs
 Author: ReaJason
 Author-email: reajason1225@gmail.com
 License: MIT
 Keywords: xhs crawl
 Classifier: Development Status :: 3 - Alpha
@@ -36,14 +36,16 @@
 [![](https://github.com/ReaJason/xhs/actions/workflows/test.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/test.yml)
 [![](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml)
 
 </div>
 
 > **Warning**
 >
+> I sincerely apologize for informing you that the sign is not functioning properly, indicating that certain APIs are experiencing issues. To address the anti-aliasing of the sign, I will devote time to further learning. 👋
+>
 > This is in expriemental, so the api is not stable, every update should be cautious
 
 **xhs** is a crawling tool designed to extract data from [xiaohongshu website](https://www.xiaohongshu.com/explore)
 
 ## Usage
 
 xhs is available on PyPI:
```

### Comparing `xhs-0.2.0/README.md` & `xhs-0.2.1/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -11,14 +11,16 @@
 [![](https://github.com/ReaJason/xhs/actions/workflows/test.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/test.yml)
 [![](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml)
 
 </div>
 
 > **Warning**
 >
+> I sincerely apologize for informing you that the sign is not functioning properly, indicating that certain APIs are experiencing issues. To address the anti-aliasing of the sign, I will devote time to further learning. 👋
+>
 > This is in expriemental, so the api is not stable, every update should be cautious
 
 **xhs** is a crawling tool designed to extract data from [xiaohongshu website](https://www.xiaohongshu.com/explore)
 
 ## Usage
 
 xhs is available on PyPI:
```

### Comparing `xhs-0.2.0/setup.py` & `xhs-0.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `xhs-0.2.0/tests/__init__.py` & `xhs-0.2.1/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `xhs-0.2.0/tests/test_help.py` & `xhs-0.2.1/tests/test_help.py`

 * *Files identical despite different names*

### Comparing `xhs-0.2.0/tests/test_xhs.py` & `xhs-0.2.1/tests/test_xhs.py`

 * *Files 1% similar despite different names*

```diff
@@ -29,17 +29,20 @@
     beauty_print(data)
     assert data["note_id"] == note_id
 
 
 def test_get_note_by_id_from_html(xhs_client: XhsClient):
     note_id = "6413cf6b00000000270115b5"
     data = xhs_client.get_note_by_id_from_html(note_id)
-    # pre_data = xhs_client.get_note_by_id(note_id)
     beauty_print(data)
-    # assert pre_data == data
+    assert data["note_id"] == note_id
+
+    note_id = "64426c3d000000001303eb83"
+    data = xhs_client.get_note_by_id_from_html(note_id)
+    beauty_print(data)
     assert data["note_id"] == note_id
 
 
 def test_get_self_info(xhs_client: XhsClient):
     data = xhs_client.get_self_info()
     beauty_print(data)
     assert isinstance(data, dict)
```

### Comparing `xhs-0.2.0/xhs/core.py` & `xhs-0.2.1/xhs/core.py`

 * *Files 0% similar despite different names*

```diff
@@ -200,15 +200,15 @@
                 new_key = camel_to_underscore(key)
                 if not value:
                     new_dict[new_key] = value
                 elif isinstance(value, dict):
                     new_dict[new_key] = transform_json_keys(json.dumps(value))
                 elif isinstance(value, list):
                     new_dict[new_key] = [transform_json_keys(json.dumps(
-                        item)) if item else item for item in value]
+                        item)) if (item and isinstance(item, dict)) else item for item in value]
                 else:
                     new_dict[new_key] = value
             return new_dict
 
         url = "https://www.xiaohongshu.com/explore/" + note_id
         res = self.session.get(url, headers={"user-agent": self.user_agent})
         html = res.text
```

### Comparing `xhs-0.2.0/xhs/help.py` & `xhs-0.2.1/xhs/help.py`

 * *Files identical despite different names*

### Comparing `xhs-0.2.0/xhs.egg-info/PKG-INFO` & `xhs-0.2.1/xhs.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xhs
-Version: 0.2.0
+Version: 0.2.1
 Summary: xiaohongshu crawl sdk.
 Home-page: https://github.com/ReaJason/xhs
 Author: ReaJason
 Author-email: reajason1225@gmail.com
 License: MIT
 Keywords: xhs crawl
 Classifier: Development Status :: 3 - Alpha
@@ -36,14 +36,16 @@
 [![](https://github.com/ReaJason/xhs/actions/workflows/test.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/test.yml)
 [![](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml/badge.svg)](https://github.com/ReaJason/xhs/actions/workflows/pypi.yml)
 
 </div>
 
 > **Warning**
 >
+> I sincerely apologize for informing you that the sign is not functioning properly, indicating that certain APIs are experiencing issues. To address the anti-aliasing of the sign, I will devote time to further learning. 👋
+>
 > This is in expriemental, so the api is not stable, every update should be cautious
 
 **xhs** is a crawling tool designed to extract data from [xiaohongshu website](https://www.xiaohongshu.com/explore)
 
 ## Usage
 
 xhs is available on PyPI:
```

