# Comparing `tmp/bose-1.3.1.tar.gz` & `tmp/bose-1.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bose-1.3.1.tar", last modified: Sat May 13 11:32:18 2023, max compression
+gzip compressed data, was "bose-1.4.1.tar", last modified: Sat May 13 13:34:39 2023, max compression
```

## Comparing `bose-1.3.1.tar` & `bose-1.4.1.tar`

### file list

```diff
@@ -1,21 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 11:32:18.457363 bose-1.3.1/
--rw-rw-rw-   0        0        0     1460 2023-05-13 11:32:18.458361 bose-1.3.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 11:32:18.457363 bose-1.3.1/bose/
--rw-rw-rw-   0        0        0      340 2023-05-13 11:28:45.126433 bose-1.3.1/bose/__init__.py
--rw-rw-rw-   0        0        0     3657 2023-05-10 09:24:37.900794 bose-1.3.1/bose/base_data.py
--rw-rw-rw-   0        0        0     5228 2023-05-13 11:28:17.686088 bose-1.3.1/bose/base_task.py
--rw-rw-rw-   0        0        0     9026 2023-05-13 11:28:17.686088 bose-1.3.1/bose/boss_driver.py
--rw-rw-rw-   0        0        0     9038 2023-05-13 11:28:17.686088 bose-1.3.1/bose/boss_undetected_driver.py
--rw-rw-rw-   0        0        0     7295 2023-05-13 11:28:17.686088 bose-1.3.1/bose/create_driver.py
--rw-rw-rw-   0        0        0     1391 2023-05-10 10:36:24.892682 bose-1.3.1/bose/download_driver.py
--rw-rw-rw-   0        0        0     2901 2023-05-13 11:28:17.687091 bose-1.3.1/bose/local_storage.py
--rw-rw-rw-   0        0        0     1728 2023-05-09 15:44:16.700182 bose-1.3.1/bose/local_storage_driver.py
--rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.3.1/bose/opponent.py
--rw-rw-rw-   0        0        0     3169 2023-05-13 11:28:17.687091 bose-1.3.1/bose/output.py
--rw-rw-rw-   0        0        0     1650 2023-05-13 11:28:17.687091 bose-1.3.1/bose/task_info.py
--rw-rw-rw-   0        0        0     7361 2023-05-10 09:24:37.900794 bose-1.3.1/bose/user_agent.py
--rw-rw-rw-   0        0        0     6050 2023-05-10 10:34:20.625623 bose-1.3.1/bose/utils.py
--rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.3.1/bose/wait.py
--rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.3.1/bose/window_size.py
--rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.3.1/setup.cfg
--rw-rw-rw-   0        0        0     2297 2023-05-13 11:31:51.928114 bose-1.3.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:39.800462 bose-1.4.1/
+-rw-rw-rw-   0        0        0     1460 2023-05-13 13:34:39.801461 bose-1.4.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:39.800462 bose-1.4.1/bose/
+-rw-rw-rw-   0        0        0      340 2023-05-13 11:28:45.126433 bose-1.4.1/bose/__init__.py
+-rw-rw-rw-   0        0        0     3657 2023-05-10 09:24:37.900794 bose-1.4.1/bose/base_data.py
+-rw-rw-rw-   0        0        0     5228 2023-05-13 11:28:17.686088 bose-1.4.1/bose/base_task.py
+-rw-rw-rw-   0        0        0     9026 2023-05-13 11:28:17.686088 bose-1.4.1/bose/boss_driver.py
+-rw-rw-rw-   0        0        0     9038 2023-05-13 11:28:17.686088 bose-1.4.1/bose/boss_undetected_driver.py
+-rw-rw-rw-   0        0        0     7295 2023-05-13 11:28:17.686088 bose-1.4.1/bose/create_driver.py
+-rw-rw-rw-   0        0        0     1391 2023-05-10 10:36:24.892682 bose-1.4.1/bose/download_driver.py
+-rw-rw-rw-   0        0        0     2901 2023-05-13 11:28:17.687091 bose-1.4.1/bose/local_storage.py
+-rw-rw-rw-   0        0        0     1728 2023-05-09 15:44:16.700182 bose-1.4.1/bose/local_storage_driver.py
+-rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.4.1/bose/opponent.py
+-rw-rw-rw-   0        0        0     3169 2023-05-13 11:28:17.687091 bose-1.4.1/bose/output.py
+-rw-rw-rw-   0        0        0     1650 2023-05-13 11:28:17.687091 bose-1.4.1/bose/task_info.py
+-rw-rw-rw-   0        0        0     3977 2023-05-13 13:31:08.141431 bose-1.4.1/bose/temp_mail.py
+-rw-rw-rw-   0        0        0     7361 2023-05-10 09:24:37.900794 bose-1.4.1/bose/user_agent.py
+-rw-rw-rw-   0        0        0     6050 2023-05-10 10:34:20.625623 bose-1.4.1/bose/utils.py
+-rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.4.1/bose/wait.py
+-rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.4.1/bose/window_size.py
+-rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.4.1/setup.cfg
+-rw-rw-rw-   0        0        0     2328 2023-05-13 13:34:15.193389 bose-1.4.1/setup.py
```

### Comparing `bose-1.3.1/PKG-INFO` & `bose-1.4.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: bose
-Version: 1.3.1
+Version: 1.4.1
 Summary: The Ultimate Web Scraping Framework
 Home-page: UNKNOWN
 Author: Chetan Jain
 Author-email: chetan@omkar.cloud
 License: MIT
 Description: # Bose - The Ultimate Web Scraping Framework!
```

### Comparing `bose-1.3.1/bose/base_data.py` & `bose-1.4.1/bose/base_data.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/base_task.py` & `bose-1.4.1/bose/base_task.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/boss_driver.py` & `bose-1.4.1/bose/boss_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/boss_undetected_driver.py` & `bose-1.4.1/bose/boss_undetected_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/create_driver.py` & `bose-1.4.1/bose/create_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/download_driver.py` & `bose-1.4.1/bose/download_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/local_storage.py` & `bose-1.4.1/bose/local_storage.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/local_storage_driver.py` & `bose-1.4.1/bose/local_storage_driver.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/output.py` & `bose-1.4.1/bose/output.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/task_info.py` & `bose-1.4.1/bose/task_info.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/user_agent.py` & `bose-1.4.1/bose/user_agent.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/utils.py` & `bose-1.4.1/bose/utils.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/bose/window_size.py` & `bose-1.4.1/bose/window_size.py`

 * *Files identical despite different names*

### Comparing `bose-1.3.1/setup.py` & `bose-1.4.1/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 
 install_requires = [
     "requests",
     "chromedriver-autoinstaller==0.4.0",
     "selenium>=4.0.0",
     "undetected_chromedriver>=3.4.6",
     "openpyxl>=3.0.3",
+    "beautifulsoup4>=4.11.2",
 
 ]
 extras_require = {}
 cpython_dependencies = [
     "PyDispatcher>=2.0.5",
 ]
 
@@ -20,15 +21,15 @@
     except:
       return None
     
 
 setup(
     name='bose',
     packages=['bose'],
-    version='1.3.1',
+    version='1.4.1',
     license='MIT',
     project_urls={
         "Documentation": "https://omkar.cloud/bose/docs/",
         "Source": "https://github.com/omkarcloud/boss",
         "Tracker": "https://github.com/omkarcloud/boss/issues",
     },
```

