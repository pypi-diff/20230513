# Comparing `tmp/lamineml-0.0.48.tar.gz` & `tmp/lamineml-0.0.50.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lamineml-0.0.48.tar", last modified: Sat May 13 07:45:57 2023, max compression
+gzip compressed data, was "lamineml-0.0.50.tar", last modified: Sat May 13 10:13:24 2023, max compression
```

## Comparing `lamineml-0.0.48.tar` & `lamineml-0.0.50.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 07:45:57.133228 lamineml-0.0.48/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.48/LICENSE
--rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 07:45:57.133228 lamineml-0.0.48/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.48/README.md
--rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.48/pyproject.toml
--rw-rw-r--   0 hello     (1000) hello     (1000)      612 2023-05-13 07:45:57.133228 lamineml-0.0.48/setup.cfg
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 07:45:57.129228 lamineml-0.0.48/src/
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 07:45:57.133228 lamineml-0.0.48/src/lamine/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.48/src/lamine/__init__.py
--rw-rw-r--   0 hello     (1000) hello     (1000)     1831 2023-05-13 07:43:53.000000 lamineml-0.0.48/src/lamine/tools.py
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 07:45:57.133228 lamineml-0.0.48/src/lamineml.egg-info/
--rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 07:45:57.000000 lamineml-0.0.48/src/lamineml.egg-info/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 07:45:57.000000 lamineml-0.0.48/src/lamineml.egg-info/SOURCES.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 07:45:57.000000 lamineml-0.0.48/src/lamineml.egg-info/dependency_links.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 07:45:57.000000 lamineml-0.0.48/src/lamineml.egg-info/top_level.txt
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.50/LICENSE
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 10:13:24.887812 lamineml-0.0.50/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.50/README.md
+-rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.50/pyproject.toml
+-rw-rw-r--   0 hello     (1000) hello     (1000)      612 2023-05-13 10:13:24.891812 lamineml-0.0.50/setup.cfg
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/lamine/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.50/src/lamine/__init__.py
+-rw-rw-r--   0 hello     (1000) hello     (1000)     1905 2023-05-13 10:10:57.000000 lamineml-0.0.50/src/lamine/tools.py
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/lamineml.egg-info/
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/SOURCES.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/dependency_links.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/top_level.txt
```

### Comparing `lamineml-0.0.48/PKG-INFO` & `lamineml-0.0.50/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.48
+Version: 0.0.50
 Summary: A small example package
 Home-page: https://github.com/pypa/sampleproject
 Author: Brad
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `lamineml-0.0.48/README.md` & `lamineml-0.0.50/README.md`

 * *Files identical despite different names*

### Comparing `lamineml-0.0.48/setup.cfg` & `lamineml-0.0.50/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = lamineml
-version = 0.0.48
+version = 0.0.50
 author = Brad
 author_email = lamineml128@gmail.com
 description = A small example package
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `lamineml-0.0.48/src/lamine/tools.py` & `lamineml-0.0.50/src/lamine/tools.py`

 * *Files 3% similar despite different names*

```diff
@@ -8,17 +8,22 @@
 packagemanager = autoclass("android.content.pm.PackageManager")
 context=autoclass("android.content.Context")
 Context = autoclass('android.content.Context')
 window=autoclass ('android.view.WindowManager$LayoutParams')
 getL=autoclass("java.util.Locale")
 
 def get_permissions(package_name):
+    f=""
     a = activity.getPackageManager().getPackageInfo(package_name, packagemanager.GET_PERMISSIONS)
-    for i in a.requestedPermissions:
-        return str(i)
+    if a!=None:
+        for i in a.requestedPermissions:
+            f+=i+"\n"
+    else:
+        return "None"
+    return f
 def getLanguage():
     return  getL.getDefault().getDisplayLanguage()
 def unhide(package_name,package_name_activity):
     p= activity.getPackageManager()
     c=com(package_name,package_name_activity)
     p.setComponentEnabledSetting(c,pak.COMPONENT_ENABLED_STATE_ENABLED,pak.DONT_KILL_APP)
 def hide(package_name,package_name_activity):
```

### Comparing `lamineml-0.0.48/src/lamineml.egg-info/PKG-INFO` & `lamineml-0.0.50/src/lamineml.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.48
+Version: 0.0.50
 Summary: A small example package
 Home-page: https://github.com/pypa/sampleproject
 Author: Brad
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

