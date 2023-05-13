# Comparing `tmp/bose-1.2.0.tar.gz` & `tmp/bose-1.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bose-1.2.0.tar", last modified: Sat May 13 09:44:27 2023, max compression
+gzip compressed data, was "bose-1.2.1.tar", last modified: Sat May 13 10:16:44 2023, max compression
```

## Comparing `bose-1.2.0.tar` & `bose-1.2.1.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 09:44:27.369315 bose-1.2.0/
--rw-rw-rw-   0        0        0     1503 2023-05-13 09:44:27.370314 bose-1.2.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 09:44:27.368326 bose-1.2.0/bose/
--rw-rw-rw-   0        0        0      348 2023-05-10 06:44:37.337926 bose-1.2.0/bose/__init__.py
--rw-rw-rw-   0        0        0     3657 2023-05-10 09:24:37.900794 bose-1.2.0/bose/base_data.py
--rw-rw-rw-   0        0        0     5252 2023-05-13 08:16:49.683340 bose-1.2.0/bose/base_task.py
--rw-rw-rw-   0        0        0     7331 2023-05-10 09:27:31.379871 bose-1.2.0/bose/create_driver.py
--rw-rw-rw-   0        0        0     1391 2023-05-10 10:36:24.892682 bose-1.2.0/bose/download_driver.py
--rw-rw-rw-   0        0        0     2905 2023-05-10 10:11:04.901186 bose-1.2.0/bose/local_storage.py
--rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.2.0/bose/opponent.py
--rw-rw-rw-   0        0        0     3173 2023-05-09 15:50:46.922925 bose-1.2.0/bose/output.py
--rw-rw-rw-   0        0        0     1654 2023-05-09 12:06:31.715212 bose-1.2.0/bose/task_info.py
--rw-rw-rw-   0        0        0     7361 2023-05-10 09:24:37.900794 bose-1.2.0/bose/user_agent.py
--rw-rw-rw-   0        0        0     6050 2023-05-10 10:34:20.625623 bose-1.2.0/bose/utils.py
--rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.2.0/bose/wait.py
--rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.2.0/bose/window_size.py
--rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.2.0/setup.cfg
--rw-rw-rw-   0        0        0     2189 2023-05-10 08:18:54.462936 bose-1.2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:16:44.251335 bose-1.2.1/
+-rw-rw-rw-   0        0        0     1460 2023-05-13 10:16:44.251335 bose-1.2.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 10:16:44.250335 bose-1.2.1/bose/
+-rw-rw-rw-   0        0        0      348 2023-05-10 06:44:37.337926 bose-1.2.1/bose/__init__.py
+-rw-rw-rw-   0        0        0     3657 2023-05-10 09:24:37.900794 bose-1.2.1/bose/base_data.py
+-rw-rw-rw-   0        0        0     5252 2023-05-13 08:16:49.683340 bose-1.2.1/bose/base_task.py
+-rw-rw-rw-   0        0        0     7331 2023-05-10 09:27:31.379871 bose-1.2.1/bose/create_driver.py
+-rw-rw-rw-   0        0        0     1391 2023-05-10 10:36:24.892682 bose-1.2.1/bose/download_driver.py
+-rw-rw-rw-   0        0        0     2905 2023-05-10 10:11:04.901186 bose-1.2.1/bose/local_storage.py
+-rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.2.1/bose/opponent.py
+-rw-rw-rw-   0        0        0     3173 2023-05-09 15:50:46.922925 bose-1.2.1/bose/output.py
+-rw-rw-rw-   0        0        0     1654 2023-05-09 12:06:31.715212 bose-1.2.1/bose/task_info.py
+-rw-rw-rw-   0        0        0     7361 2023-05-10 09:24:37.900794 bose-1.2.1/bose/user_agent.py
+-rw-rw-rw-   0        0        0     6050 2023-05-10 10:34:20.625623 bose-1.2.1/bose/utils.py
+-rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.2.1/bose/wait.py
+-rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.2.1/bose/window_size.py
+-rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.2.1/setup.cfg
+-rw-rw-rw-   0        0        0     2189 2023-05-13 10:16:33.173248 bose-1.2.1/setup.py
```

### Comparing `bose-1.2.0/PKG-INFO` & `bose-1.2.1/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,19 +1,18 @@
 Metadata-Version: 1.1
 Name: bose
-Version: 1.2.0
+Version: 1.2.1
 Summary: The Ultimate Web Scraping Framework
 Home-page: UNKNOWN
 Author: Chetan Jain
 Author-email: chetan@omkar.cloud
 License: MIT
 Description: # Bose - The Ultimate Web Scraping Framework!
         
-        Read Bose Documentation at [https://www.omkar.cloud/bose/](https://www.omkar.cloud/bose/)
-        
+        Read Bose Documentation at https://www.omkar.cloud/bose/
 Keywords: crawler,framework,scraping,crawling,web-scraping,web-scraping-python,cloudflare-bypass,anti-detection,bot-detection,automation,webdriver,browser
 Platform: UNKNOWN
 Classifier: Framework :: Scrapy
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `bose-1.2.0/bose/base_data.py` & `bose-1.2.1/bose/base_data.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/base_task.py` & `bose-1.2.1/bose/base_task.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/create_driver.py` & `bose-1.2.1/bose/create_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/download_driver.py` & `bose-1.2.1/bose/download_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/local_storage.py` & `bose-1.2.1/bose/local_storage.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/output.py` & `bose-1.2.1/bose/output.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/task_info.py` & `bose-1.2.1/bose/task_info.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/user_agent.py` & `bose-1.2.1/bose/user_agent.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/utils.py` & `bose-1.2.1/bose/utils.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/bose/window_size.py` & `bose-1.2.1/bose/window_size.py`

 * *Files identical despite different names*

### Comparing `bose-1.2.0/setup.py` & `bose-1.2.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 cpython_dependencies = [
     "PyDispatcher>=2.0.5",
 ]
 
 setup(
     name='bose',
     packages=['bose'],
-    version='1.2.0',
+    version='1.2.1',
     license='MIT',
     project_urls={
         "Documentation": "https://omkar.cloud/bose/docs/",
         "Source": "https://github.com/omkarcloud/boss",
         "Tracker": "https://github.com/omkarcloud/boss/issues",
     },
```

