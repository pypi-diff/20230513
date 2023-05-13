# Comparing `tmp/lamineml-0.0.50.tar.gz` & `tmp/lamineml-0.0.51.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lamineml-0.0.50.tar", last modified: Sat May 13 10:13:24 2023, max compression
+gzip compressed data, was "lamineml-0.0.51.tar", last modified: Sat May 13 11:14:05 2023, max compression
```

## Comparing `lamineml-0.0.50.tar` & `lamineml-0.0.51.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.50/LICENSE
--rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 10:13:24.887812 lamineml-0.0.50/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.50/README.md
--rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.50/pyproject.toml
--rw-rw-r--   0 hello     (1000) hello     (1000)      612 2023-05-13 10:13:24.891812 lamineml-0.0.50/setup.cfg
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/lamine/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.50/src/lamine/__init__.py
--rw-rw-r--   0 hello     (1000) hello     (1000)     1905 2023-05-13 10:10:57.000000 lamineml-0.0.50/src/lamine/tools.py
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 10:13:24.887812 lamineml-0.0.50/src/lamineml.egg-info/
--rw-rw-r--   0 hello     (1000) hello     (1000)     2792 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/SOURCES.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/dependency_links.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 10:13:24.000000 lamineml-0.0.50/src/lamineml.egg-info/top_level.txt
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.930258 lamineml-0.0.51/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.51/LICENSE
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:14:05.930258 lamineml-0.0.51/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.51/README.md
+-rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.51/pyproject.toml
+-rw-rw-r--   0 hello     (1000) hello     (1000)      626 2023-05-13 11:14:05.930258 lamineml-0.0.51/setup.cfg
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.926258 lamineml-0.0.51/src/
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.926258 lamineml-0.0.51/src/lamine/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.51/src/lamine/__init__.py
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2558 2023-05-13 11:12:37.000000 lamineml-0.0.51/src/lamine/tools.py
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.930258 lamineml-0.0.51/src/lamineml.egg-info/
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/SOURCES.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/dependency_links.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/top_level.txt
```

### Comparing `lamineml-0.0.50/PKG-INFO` & `lamineml-0.0.51/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.50
-Summary: A small example package
+Version: 0.0.51
+Summary: use this library in kivy android
 Home-page: https://github.com/pypa/sampleproject
-Author: Brad
+Author: Lamine ML
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `lamineml-0.0.50/README.md` & `lamineml-0.0.51/README.md`

 * *Files identical despite different names*

### Comparing `lamineml-0.0.50/setup.cfg` & `lamineml-0.0.51/setup.cfg`

 * *Files 22% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [metadata]
 name = lamineml
-version = 0.0.50
-author = Brad
+version = 0.0.51
+author = Lamine ML
 author_email = lamineml128@gmail.com
-description = A small example package
+description = use this library in kivy android
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls = 
 	Bug Tracker = https://github.com/pypa/sampleproject/issues
 classifiers = 
 	Programming Language :: Python :: 3
```

### Comparing `lamineml-0.0.50/src/lamine/tools.py` & `lamineml-0.0.51/src/lamine/tools.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,14 +6,35 @@
 from jnius import autoclass ,cast
 from android.runnable import run_on_ui_thread
 packagemanager = autoclass("android.content.pm.PackageManager")
 context=autoclass("android.content.Context")
 Context = autoclass('android.content.Context')
 window=autoclass ('android.view.WindowManager$LayoutParams')
 getL=autoclass("java.util.Locale")
+Intent = autoclass('android.content.Intent')
+uri = autoclass('android.net.Uri')
+def get_application():
+    al =[]
+    sendIntent = Intent(Intent.ACTION_MAIN, None)
+    sendIntent.addCategory(Intent.CATEGORY_LAUNCHER)
+    a = activity.getPackageManager().queryIntentActivities(sendIntent, 0)
+    for i in a:
+
+        if i.activityInfo.labelRes != 0:
+            res = activity.getPackageManager().getResourcesForApplication(i.activityInfo.applicationInfo)
+            dd = res.getString(i.activityInfo.labelRes)
+            al.append(dd)
+
+
+
+
+
+        else:
+            i.activityInfo.applicationInfo.loadLabel(activity.getPackageManager())
+    return al
 
 def get_permissions(package_name):
     f=""
     a = activity.getPackageManager().getPackageInfo(package_name, packagemanager.GET_PERMISSIONS)
     if a!=None:
         for i in a.requestedPermissions:
             f+=i+"\n"
```

### Comparing `lamineml-0.0.50/src/lamineml.egg-info/PKG-INFO` & `lamineml-0.0.51/src/lamineml.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.50
-Summary: A small example package
+Version: 0.0.51
+Summary: use this library in kivy android
 Home-page: https://github.com/pypa/sampleproject
-Author: Brad
+Author: Lamine ML
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

