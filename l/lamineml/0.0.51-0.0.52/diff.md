# Comparing `tmp/lamineml-0.0.51.tar.gz` & `tmp/lamineml-0.0.52.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lamineml-0.0.51.tar", last modified: Sat May 13 11:14:05 2023, max compression
+gzip compressed data, was "lamineml-0.0.52.tar", last modified: Sat May 13 11:50:03 2023, max compression
```

## Comparing `lamineml-0.0.51.tar` & `lamineml-0.0.52.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.930258 lamineml-0.0.51/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.51/LICENSE
--rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:14:05.930258 lamineml-0.0.51/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.51/README.md
--rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.51/pyproject.toml
--rw-rw-r--   0 hello     (1000) hello     (1000)      626 2023-05-13 11:14:05.930258 lamineml-0.0.51/setup.cfg
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.926258 lamineml-0.0.51/src/
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.926258 lamineml-0.0.51/src/lamine/
--rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.51/src/lamine/__init__.py
--rw-rw-r--   0 hello     (1000) hello     (1000)     2558 2023-05-13 11:12:37.000000 lamineml-0.0.51/src/lamine/tools.py
-drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:14:05.930258 lamineml-0.0.51/src/lamineml.egg-info/
--rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/PKG-INFO
--rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/SOURCES.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/dependency_links.txt
--rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 11:14:05.000000 lamineml-0.0.51/src/lamineml.egg-info/top_level.txt
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:50:03.901011 lamineml-0.0.52/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2021-07-31 02:25:56.000000 lamineml-0.0.52/LICENSE
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:50:03.901011 lamineml-0.0.52/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2304 2021-07-31 02:25:56.000000 lamineml-0.0.52/README.md
+-rw-rw-r--   0 hello     (1000) hello     (1000)      126 2023-04-29 18:32:31.000000 lamineml-0.0.52/pyproject.toml
+-rw-rw-r--   0 hello     (1000) hello     (1000)      626 2023-05-13 11:50:03.901011 lamineml-0.0.52/setup.cfg
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:50:03.897010 lamineml-0.0.52/src/
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:50:03.901011 lamineml-0.0.52/src/lamine/
+-rw-rw-r--   0 hello     (1000) hello     (1000)        0 2023-04-29 17:24:39.000000 lamineml-0.0.52/src/lamine/__init__.py
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2781 2023-05-13 11:48:54.000000 lamineml-0.0.52/src/lamine/tools.py
+drwxrwxr-x   0 hello     (1000) hello     (1000)        0 2023-05-13 11:50:03.901011 lamineml-0.0.52/src/lamineml.egg-info/
+-rw-rw-r--   0 hello     (1000) hello     (1000)     2806 2023-05-13 11:50:03.000000 lamineml-0.0.52/src/lamineml.egg-info/PKG-INFO
+-rw-rw-r--   0 hello     (1000) hello     (1000)      229 2023-05-13 11:50:03.000000 lamineml-0.0.52/src/lamineml.egg-info/SOURCES.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        1 2023-05-13 11:50:03.000000 lamineml-0.0.52/src/lamineml.egg-info/dependency_links.txt
+-rw-rw-r--   0 hello     (1000) hello     (1000)        7 2023-05-13 11:50:03.000000 lamineml-0.0.52/src/lamineml.egg-info/top_level.txt
```

### Comparing `lamineml-0.0.51/PKG-INFO` & `lamineml-0.0.52/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.51
+Version: 0.0.52
 Summary: use this library in kivy android
 Home-page: https://github.com/pypa/sampleproject
 Author: Lamine ML
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `lamineml-0.0.51/README.md` & `lamineml-0.0.52/README.md`

 * *Files identical despite different names*

### Comparing `lamineml-0.0.51/setup.cfg` & `lamineml-0.0.52/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = lamineml
-version = 0.0.51
+version = 0.0.52
 author = Lamine ML
 author_email = lamineml128@gmail.com
 description = use this library in kivy android
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `lamineml-0.0.51/src/lamine/tools.py` & `lamineml-0.0.52/src/lamine/tools.py`

 * *Files 9% similar despite different names*

```diff
@@ -8,14 +8,19 @@
 packagemanager = autoclass("android.content.pm.PackageManager")
 context=autoclass("android.content.Context")
 Context = autoclass('android.content.Context')
 window=autoclass ('android.view.WindowManager$LayoutParams')
 getL=autoclass("java.util.Locale")
 Intent = autoclass('android.content.Intent')
 uri = autoclass('android.net.Uri')
+cipl =autoclass("android.content.ClipData")
+def copy_text(text):
+    myClipboard =activity.getSystemService(Context.CLIPBOARD_SERVICE)
+    clip =ClipData.newPlainText("copy text", text)
+    myClipboard.setPrimaryClip(clip)
 def get_application():
     al =[]
     sendIntent = Intent(Intent.ACTION_MAIN, None)
     sendIntent.addCategory(Intent.CATEGORY_LAUNCHER)
     a = activity.getPackageManager().queryIntentActivities(sendIntent, 0)
     for i in a:
```

### Comparing `lamineml-0.0.51/src/lamineml.egg-info/PKG-INFO` & `lamineml-0.0.52/src/lamineml.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lamineml
-Version: 0.0.51
+Version: 0.0.52
 Summary: use this library in kivy android
 Home-page: https://github.com/pypa/sampleproject
 Author: Lamine ML
 Author-email: lamineml128@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

