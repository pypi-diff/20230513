# Comparing `tmp/material_zui-0.0.8.tar.gz` & `tmp/material_zui-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "material_zui-0.0.8.tar", max compression
+gzip compressed data, was "material_zui-0.0.9.tar", max compression
```

## Comparing `material_zui-0.0.8.tar` & `material_zui-0.0.9.tar`

### file list

```diff
@@ -1,46 +1,46 @@
--rw-r--r--   0        0        0      681 2023-05-12 03:05:25.421729 material_zui-0.0.8/pyproject.toml
--rw-r--r--   0        0        0      260 2023-05-01 15:33:57.972869 material_zui-0.0.8/src/material_zui/.pypirc
--rw-r--r--   0        0        0      555 2023-03-21 08:40:33.421115 material_zui-0.0.8/src/material_zui/ResizeImage.py
--rw-r--r--   0        0        0       42 2023-05-07 05:09:56.400820 material_zui-0.0.8/src/material_zui/compress/__init__.py
--rw-r--r--   0        0        0       74 2023-05-07 05:16:12.115224 material_zui-0.0.8/src/material_zui/compress/index.py
--rw-r--r--   0        0        0     2131 2023-05-07 05:22:45.101162 material_zui-0.0.8/src/material_zui/compress/text.py
--rw-r--r--   0        0        0       36 2023-05-02 13:44:44.126257 material_zui-0.0.8/src/material_zui/crawl/__init__.py
--rw-r--r--   0        0        0        0 2023-05-02 13:44:44.126257 material_zui-0.0.8/src/material_zui/crawl/index.py
--rw-r--r--   0        0        0       41 2023-05-11 04:24:47.172982 material_zui-0.0.8/src/material_zui/crontab/__init__.py
--rw-r--r--   0        0        0      638 2023-05-11 04:23:06.569200 material_zui-0.0.8/src/material_zui/crontab/index.py
--rw-r--r--   0        0        0       43 2023-05-07 14:15:59.556081 material_zui-0.0.8/src/material_zui/date_time/__init__.py
--rw-r--r--   0        0        0       60 2023-05-07 14:15:59.604081 material_zui-0.0.8/src/material_zui/date_time/date_time.py
--rw-r--r--   0        0        0       49 2023-05-07 14:16:28.308295 material_zui-0.0.8/src/material_zui/date_time/index.py
--rw-r--r--   0        0        0      692 2023-05-07 14:16:10.888166 material_zui-0.0.8/src/material_zui/date_time/time.py
--rw-r--r--   0        0        0      216 2023-05-11 09:54:07.451440 material_zui-0.0.8/src/material_zui/image/__init__.py
--rw-r--r--   0        0        0     2199 2023-05-05 09:48:58.874264 material_zui-0.0.8/src/material_zui/image/colorization.py
--rw-r--r--   0        0        0     2921 2023-05-11 09:52:23.138728 material_zui-0.0.8/src/material_zui/image/combine.py
--rw-r--r--   0        0        0     5490 2023-05-11 10:24:19.669145 material_zui-0.0.8/src/material_zui/image/common.py
--rw-r--r--   0        0        0     2808 2023-05-11 10:13:26.444992 material_zui-0.0.8/src/material_zui/image/convert.py
--rw-r--r--   0        0        0       78 2023-05-06 06:26:57.697131 material_zui-0.0.8/src/material_zui/image/data.py
--rw-r--r--   0        0        0      461 2023-05-11 10:14:50.303432 material_zui-0.0.8/src/material_zui/image/index.py
--rw-r--r--   0        0        0     9945 2023-05-05 03:49:43.138352 material_zui-0.0.8/src/material_zui/image/model/colorization_deploy_v2.prototxt
--rw-r--r--   0        0        0     5088 2023-05-05 03:49:53.225773 material_zui-0.0.8/src/material_zui/image/model/pts_in_hull.npy
--rw-r--r--   0        0        0      782 2023-05-11 04:50:18.808963 material_zui-0.0.8/src/material_zui/image/remove_background.py
--rw-r--r--   0        0        0     6445 2023-05-06 08:59:41.215230 material_zui-0.0.8/src/material_zui/image/to_svg.py
--rw-r--r--   0        0        0      520 2023-05-11 09:48:54.829117 material_zui-0.0.8/src/material_zui/image/transparent_background.py
--rw-r--r--   0        0        0      249 2023-04-28 09:24:02.020353 material_zui-0.0.8/src/material_zui/image/type.py
--rw-r--r--   0        0        0     4779 2023-05-11 10:15:27.410813 material_zui-0.0.8/src/material_zui/image/upscale.py
--rw-r--r--   0        0        0       48 2023-05-02 05:21:47.818631 material_zui-0.0.8/src/material_zui/language_model/__init__.py
--rw-r--r--   0        0        0      987 2023-05-02 05:36:54.809448 material_zui-0.0.8/src/material_zui/language_model/index.py
--rw-r--r--   0        0        0       37 2023-04-30 11:48:06.179161 material_zui-0.0.8/src/material_zui/log/__init__.py
--rw-r--r--   0        0        0       83 2023-05-11 10:20:42.114888 material_zui-0.0.8/src/material_zui/log/index.py
--rw-r--r--   0        0        0      559 2023-05-11 10:19:34.415566 material_zui-0.0.8/src/material_zui/log/log.py
--rw-r--r--   0        0        0      445 2023-05-11 10:34:20.938361 material_zui-0.0.8/src/material_zui/readme.md
--rw-r--r--   0        0        0       39 2023-05-02 05:15:13.799596 material_zui-0.0.8/src/material_zui/regex/__init__.py
--rw-r--r--   0        0        0     5344 2023-05-02 05:18:47.668155 material_zui-0.0.8/src/material_zui/regex/index.py
--rw-r--r--   0        0        0       43 2023-04-30 11:47:27.662335 material_zui-0.0.8/src/material_zui/replicate/__init__.py
--rw-r--r--   0        0        0     2481 2023-05-01 15:33:18.205379 material_zui-0.0.8/src/material_zui/replicate/index.py
--rw-r--r--   0        0        0      895 2023-05-11 10:31:29.010961 material_zui-0.0.8/src/material_zui/setup.py
--rw-r--r--   0        0        0       46 2023-05-02 13:44:38.645684 material_zui-0.0.8/src/material_zui/telegram_bot/__init__.py
--rw-r--r--   0        0        0      432 2023-05-07 05:43:32.880583 material_zui-0.0.8/src/material_zui/telegram_bot/index.py
--rw-r--r--   0        0        0       36 2023-04-30 11:48:06.223146 material_zui-0.0.8/src/material_zui/tmp/__init__.py
--rw-r--r--   0        0        0        0 2023-04-28 03:39:00.036364 material_zui-0.0.8/src/material_zui/tmp/index.py
--rw-r--r--   0        0        0       36 2023-05-01 14:11:23.375942 material_zui-0.0.8/src/material_zui/validate/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 14:11:23.379941 material_zui-0.0.8/src/material_zui/validate/index.py
--rw-r--r--   0        0        0     1271 1970-01-01 00:00:00.000000 material_zui-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0      778 2023-05-13 12:22:55.970961 material_zui-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0      260 2023-05-01 15:33:57.972869 material_zui-0.0.9/src/material_zui/.pypirc
+-rw-r--r--   0        0        0      555 2023-03-21 08:40:33.421115 material_zui-0.0.9/src/material_zui/ResizeImage.py
+-rw-r--r--   0        0        0       42 2023-05-07 05:09:56.400820 material_zui-0.0.9/src/material_zui/compress/__init__.py
+-rw-r--r--   0        0        0       74 2023-05-07 05:16:12.115224 material_zui-0.0.9/src/material_zui/compress/index.py
+-rw-r--r--   0        0        0     2131 2023-05-07 05:22:45.101162 material_zui-0.0.9/src/material_zui/compress/text.py
+-rw-r--r--   0        0        0       36 2023-05-02 13:44:44.126257 material_zui-0.0.9/src/material_zui/crawl/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-02 13:44:44.126257 material_zui-0.0.9/src/material_zui/crawl/index.py
+-rw-r--r--   0        0        0       41 2023-05-11 04:24:47.172982 material_zui-0.0.9/src/material_zui/crontab/__init__.py
+-rw-r--r--   0        0        0      638 2023-05-11 04:23:06.569200 material_zui-0.0.9/src/material_zui/crontab/index.py
+-rw-r--r--   0        0        0       43 2023-05-07 14:15:59.556081 material_zui-0.0.9/src/material_zui/date_time/__init__.py
+-rw-r--r--   0        0        0       60 2023-05-07 14:15:59.604081 material_zui-0.0.9/src/material_zui/date_time/date_time.py
+-rw-r--r--   0        0        0       49 2023-05-07 14:16:28.308295 material_zui-0.0.9/src/material_zui/date_time/index.py
+-rw-r--r--   0        0        0      692 2023-05-07 14:16:10.888166 material_zui-0.0.9/src/material_zui/date_time/time.py
+-rw-r--r--   0        0        0      216 2023-05-11 09:54:07.451440 material_zui-0.0.9/src/material_zui/image/__init__.py
+-rw-r--r--   0        0        0     2199 2023-05-05 09:48:58.874264 material_zui-0.0.9/src/material_zui/image/colorization.py
+-rw-r--r--   0        0        0     2921 2023-05-11 09:52:23.138728 material_zui-0.0.9/src/material_zui/image/combine.py
+-rw-r--r--   0        0        0     5490 2023-05-11 10:24:19.669145 material_zui-0.0.9/src/material_zui/image/common.py
+-rw-r--r--   0        0        0     2808 2023-05-11 10:13:26.444992 material_zui-0.0.9/src/material_zui/image/convert.py
+-rw-r--r--   0        0        0       78 2023-05-06 06:26:57.697131 material_zui-0.0.9/src/material_zui/image/data.py
+-rw-r--r--   0        0        0      461 2023-05-11 10:14:50.303432 material_zui-0.0.9/src/material_zui/image/index.py
+-rw-r--r--   0        0        0     9945 2023-05-05 03:49:43.138352 material_zui-0.0.9/src/material_zui/image/model/colorization_deploy_v2.prototxt
+-rw-r--r--   0        0        0     5088 2023-05-05 03:49:53.225773 material_zui-0.0.9/src/material_zui/image/model/pts_in_hull.npy
+-rw-r--r--   0        0        0      782 2023-05-11 04:50:18.808963 material_zui-0.0.9/src/material_zui/image/remove_background.py
+-rw-r--r--   0        0        0     6445 2023-05-06 08:59:41.215230 material_zui-0.0.9/src/material_zui/image/to_svg.py
+-rw-r--r--   0        0        0      520 2023-05-11 09:48:54.829117 material_zui-0.0.9/src/material_zui/image/transparent_background.py
+-rw-r--r--   0        0        0      249 2023-04-28 09:24:02.020353 material_zui-0.0.9/src/material_zui/image/type.py
+-rw-r--r--   0        0        0     4779 2023-05-11 10:15:27.410813 material_zui-0.0.9/src/material_zui/image/upscale.py
+-rw-r--r--   0        0        0       48 2023-05-02 05:21:47.818631 material_zui-0.0.9/src/material_zui/language_model/__init__.py
+-rw-r--r--   0        0        0      987 2023-05-02 05:36:54.809448 material_zui-0.0.9/src/material_zui/language_model/index.py
+-rw-r--r--   0        0        0       37 2023-04-30 11:48:06.179161 material_zui-0.0.9/src/material_zui/log/__init__.py
+-rw-r--r--   0        0        0       83 2023-05-11 10:20:42.114888 material_zui-0.0.9/src/material_zui/log/index.py
+-rw-r--r--   0        0        0      559 2023-05-11 10:19:34.415566 material_zui-0.0.9/src/material_zui/log/log.py
+-rw-r--r--   0        0        0      911 2023-05-12 10:39:11.524186 material_zui-0.0.9/src/material_zui/readme.md
+-rw-r--r--   0        0        0       39 2023-05-02 05:15:13.799596 material_zui-0.0.9/src/material_zui/regex/__init__.py
+-rw-r--r--   0        0        0     5344 2023-05-02 05:18:47.668155 material_zui-0.0.9/src/material_zui/regex/index.py
+-rw-r--r--   0        0        0       43 2023-04-30 11:47:27.662335 material_zui-0.0.9/src/material_zui/replicate/__init__.py
+-rw-r--r--   0        0        0     2481 2023-05-01 15:33:18.205379 material_zui-0.0.9/src/material_zui/replicate/index.py
+-rw-r--r--   0        0        0      895 2023-05-11 10:31:29.010961 material_zui-0.0.9/src/material_zui/setup.py
+-rw-r--r--   0        0        0       46 2023-05-02 13:44:38.645684 material_zui-0.0.9/src/material_zui/telegram_bot/__init__.py
+-rw-r--r--   0        0        0      432 2023-05-07 05:43:32.880583 material_zui-0.0.9/src/material_zui/telegram_bot/index.py
+-rw-r--r--   0        0        0       36 2023-04-30 11:48:06.223146 material_zui-0.0.9/src/material_zui/tmp/__init__.py
+-rw-r--r--   0        0        0        0 2023-04-28 03:39:00.036364 material_zui-0.0.9/src/material_zui/tmp/index.py
+-rw-r--r--   0        0        0       36 2023-05-01 14:11:23.375942 material_zui-0.0.9/src/material_zui/validate/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 14:11:23.379941 material_zui-0.0.9/src/material_zui/validate/index.py
+-rw-r--r--   0        0        0     1836 1970-01-01 00:00:00.000000 material_zui-0.0.9/PKG-INFO
```

### Comparing `material_zui-0.0.8/pyproject.toml` & `material_zui-0.0.9/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,19 @@
 [tool.poetry]
 name = "material_zui"
-version = "0.0.8"
+version = "0.0.9"
 description = "Material Zui"
 authors = ["chauhmnguyen <chauhoangminhnguyen@gmail.com>"]
 readme = "src/material_zui/readme.md"
+keywords = [
+	"material",
+	"zui",
+	"material zui",
+	"zui material"
+]
 include = ["src/material_zui/*"]
 exclude = ["src/material_zui/image/model/colorization_release_v2.caffemodel"]
 
 [tool.poetry.dependencies]
 python = "~3.10"
 opencv-python = "^4.7.0.72"
 pillow = "^9.5.0"
@@ -17,12 +23,12 @@
 requests = "^2.30.0"
 replicate = "^0.8.1"
 multipledispatch = "^0.6.0"
 pandas = "^2.0.1"
 pythonlangutil = "^0.1"
 python-crontab = "^2.7.1"
 rembg = "^2.0.36"
-
+pytelegrambotapi = "^4.11.0"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `material_zui-0.0.8/src/material_zui/ResizeImage.py` & `material_zui-0.0.9/src/material_zui/ResizeImage.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/compress/text.py` & `material_zui-0.0.9/src/material_zui/compress/text.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/crontab/index.py` & `material_zui-0.0.9/src/material_zui/crontab/index.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/date_time/time.py` & `material_zui-0.0.9/src/material_zui/date_time/time.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/colorization.py` & `material_zui-0.0.9/src/material_zui/image/colorization.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/combine.py` & `material_zui-0.0.9/src/material_zui/image/combine.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/common.py` & `material_zui-0.0.9/src/material_zui/image/common.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/convert.py` & `material_zui-0.0.9/src/material_zui/image/convert.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/model/colorization_deploy_v2.prototxt` & `material_zui-0.0.9/src/material_zui/image/model/colorization_deploy_v2.prototxt`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/model/pts_in_hull.npy` & `material_zui-0.0.9/src/material_zui/image/model/pts_in_hull.npy`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/remove_background.py` & `material_zui-0.0.9/src/material_zui/image/remove_background.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/to_svg.py` & `material_zui-0.0.9/src/material_zui/image/to_svg.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/transparent_background.py` & `material_zui-0.0.9/src/material_zui/image/transparent_background.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/image/upscale.py` & `material_zui-0.0.9/src/material_zui/image/upscale.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/language_model/index.py` & `material_zui-0.0.9/src/material_zui/language_model/index.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/log/log.py` & `material_zui-0.0.9/src/material_zui/log/log.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/regex/index.py` & `material_zui-0.0.9/src/material_zui/regex/index.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/replicate/index.py` & `material_zui-0.0.9/src/material_zui/replicate/index.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/src/material_zui/setup.py` & `material_zui-0.0.9/src/material_zui/setup.py`

 * *Files identical despite different names*

### Comparing `material_zui-0.0.8/PKG-INFO` & `material_zui-0.0.9/PKG-INFO`

 * *Files 26% similar despite different names*

```diff
@@ -1,50 +1,75 @@
 Metadata-Version: 2.1
 Name: material-zui
-Version: 0.0.8
+Version: 0.0.9
 Summary: Material Zui
+Keywords: material,zui,material zui,zui material
 Author: chauhmnguyen
 Author-email: chauhoangminhnguyen@gmail.com
 Requires-Python: >=3.10,<3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Requires-Dist: flask (>=2.3.2,<3.0.0)
 Requires-Dist: matplotlib (>=3.7.1,<4.0.0)
 Requires-Dist: multipledispatch (>=0.6.0,<0.7.0)
 Requires-Dist: numpy (>=1.24.3,<2.0.0)
 Requires-Dist: opencv-python (>=4.7.0.72,<5.0.0.0)
 Requires-Dist: pandas (>=2.0.1,<3.0.0)
 Requires-Dist: pillow (>=9.5.0,<10.0.0)
+Requires-Dist: pytelegrambotapi (>=4.11.0,<5.0.0)
 Requires-Dist: python-crontab (>=2.7.1,<3.0.0)
 Requires-Dist: pythonlangutil (>=0.1,<0.2)
 Requires-Dist: rembg (>=2.0.36,<3.0.0)
 Requires-Dist: replicate (>=0.8.1,<0.9.0)
 Requires-Dist: requests (>=2.30.0,<3.0.0)
 Description-Content-Type: text/markdown
 
 # Modules
 
 <ol>
   <li>Crawl</li>
   <li>
     Image
     <ul>
+      <li>grayscale</li>
       <li>colorization</li>
+      <li>sketch</li>
       <li>transparent background</li>
       <li>upscale</li>
-      <li>grayscale</li>
-      <li>sketch</li>
       <li>convert to jpg/png</li>
     </ul>
   </li>
   <li>Language Model</li>
   <li>Regex</li>
   <li>Log</li>
   <li>Replicate: AI Platform API</li>
   <li>Telegram Bot</li>
   <li>Validate</li>
 </ol>
 
+# Log
+
+- Example:
+
+```py
+from material_zui.log import debug, info, warning, error, critical, printTable
+
+debug('This is a debug message')
+info('This is an info message')
+warning('This is a warning message')
+error('This is an error message')
+critical('This is a critical message')
+
+printTable({
+    'Name': ['Alice', 'Bob', 'Charlie', 'Dave'],
+    'Age': [25, 31, 35, 19],
+    'Score': [85, 94, 76, 95]
+})
+```
+
+- Result:
+  ![Alt text](../../static/img/doc/log1.png)
+
 # Package
 
 - https://pypi.org/project/material-zui
```

