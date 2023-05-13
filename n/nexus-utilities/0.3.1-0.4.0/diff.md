# Comparing `tmp/nexus-utilities-0.3.1.tar.gz` & `tmp/nexus-utilities-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nexus-utilities-0.3.1.tar", last modified: Thu May 11 21:06:46 2023, max compression
+gzip compressed data, was "nexus-utilities-0.4.0.tar", last modified: Sat May 13 20:27:43 2023, max compression
```

## Comparing `nexus-utilities-0.3.1.tar` & `nexus-utilities-0.4.0.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 21:06:46.907196 nexus-utilities-0.3.1/
--rw-r--r--   0 runner    (1001) docker     (123)    35141 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-11 21:06:46.907196 nexus-utilities-0.3.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    12104 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 21:06:46.907196 nexus-utilities-0.3.1/nexus_utilities.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-11 21:06:46.000000 nexus-utilities-0.3.1/nexus_utilities.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      453 2023-05-11 21:06:46.000000 nexus-utilities-0.3.1/nexus_utilities.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 21:06:46.000000 nexus-utilities-0.3.1/nexus_utilities.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-11 21:06:46.000000 nexus-utilities-0.3.1/nexus_utilities.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-11 21:06:46.000000 nexus-utilities-0.3.1/nexus_utilities.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 21:06:46.907196 nexus-utilities-0.3.1/nexus_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1092 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/config_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11007 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/database_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2996 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/datetime_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      499 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/flatfile_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3249 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/package_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5209 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/password_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/nexus_utils/string_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 21:06:46.907196 nexus-utilities-0.3.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-11 21:06:33.000000 nexus-utilities-0.3.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:27:43.278534 nexus-utilities-0.4.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    35141 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-13 20:27:43.278534 nexus-utilities-0.4.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    13493 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:27:43.278534 nexus-utilities-0.4.0/nexus_utilities.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-13 20:27:43.000000 nexus-utilities-0.4.0/nexus_utilities.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      453 2023-05-13 20:27:43.000000 nexus-utilities-0.4.0/nexus_utilities.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 20:27:43.000000 nexus-utilities-0.4.0/nexus_utilities.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-13 20:27:43.000000 nexus-utilities-0.4.0/nexus_utilities.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 20:27:43.000000 nexus-utilities-0.4.0/nexus_utilities.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:27:43.278534 nexus-utilities-0.4.0/nexus_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1092 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/config_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11007 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/database_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11367 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/datetime_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      499 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/flatfile_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3249 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/package_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5209 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/password_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/nexus_utils/string_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 20:27:43.278534 nexus-utilities-0.4.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-13 20:27:27.000000 nexus-utilities-0.4.0/setup.py
```

### Comparing `nexus-utilities-0.3.1/LICENSE.txt` & `nexus-utilities-0.4.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/PKG-INFO` & `nexus-utilities-0.4.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nexus-utilities
-Version: 0.3.1
+Version: 0.4.0
 Summary: Common python utilities
 Home-page: https://github.com/james-larsen/nexus-utilities
 Author: James Larsen
 Author-email: james.larsen42@gmail.com
 License: UNKNOWN
 Description: This package is meant to hold various useful utilities for functionality I find myself using across multiple projects.  I will try to keep this documentation updated as I expand the toolkit.
 Platform: UNKNOWN
```

### Comparing `nexus-utilities-0.3.1/README.md` & `nexus-utilities-0.4.0/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -108,14 +108,34 @@
  * ***hours_between (int):*** Hours between two timestamps
  * ***minutes_between (int):*** Minutes between two timestamps
  * ***seconds_between (int):*** Seconds between two timestamps
  * ***duration_string (str):*** String representation of difference between two timestamps
 
 Calculates the difference between two timestamps.  Provides absolute number of total days, hours, minutes, and seconds, as well as a string representation of the normalized difference, Eg. "5 days, 4 hours, 3 minutes, 2 seconds" or "32 seconds"
 
+### **determine_date_format(date_list)**
+
+Arguments:
+ * ***date_list (list):*** List of dates to analyze
+
+Returns:
+ * ***date_format (str):*** Determined date format in plain text (Eg. "MM/DD/YYYY")
+ * ***format_string (str)*** Date format string to be passed into the Python "datetime" library (Eg. "%m/%d/%Y")
+
+Attempts to isolate the date portion of a list of string values, and return the likely format.  Some sample return values are "MM/DD/YYYY", "DD-MM-YYYY or "YYYYMMDD".  The primary value of this function is to tell MM/DD from DD/MM formats, which many more traditional means of date parsing may struggle with.
+
+A few notes:
+
+* Only delimiters supported are "-", "/" and no delimiter
+* It is assumed that all dates in a given list are the same format.  For example, the function will not work properly if a list contains both "05/06/2000" and "05-07-2000"
+* Timestamp portions are ignored
+* Only works for numerical dates.  For example, will not work with "June 5, 2000"
+* Limited support for 2 digit years
+* Requires some form of differentiation between the included dates.  For example, if all dates in the list are "05/06/2000", it will be impossible to infer the date format.  However, if it sees "05/06/2000", "05/07/2000" and "05/08/2000" in the list, it will assume a "MM/DD" format based on the limited variance in one segment, and a higher variance in another segment
+
 ---
 
 ## package_utils.py
 
 This module contains functions for working with Python packages.
 
 ### **add_package_to_path()**
```

### Comparing `nexus-utilities-0.3.1/nexus_utilities.egg-info/PKG-INFO` & `nexus-utilities-0.4.0/nexus_utilities.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nexus-utilities
-Version: 0.3.1
+Version: 0.4.0
 Summary: Common python utilities
 Home-page: https://github.com/james-larsen/nexus-utilities
 Author: James Larsen
 Author-email: james.larsen42@gmail.com
 License: UNKNOWN
 Description: This package is meant to hold various useful utilities for functionality I find myself using across multiple projects.  I will try to keep this documentation updated as I expand the toolkit.
 Platform: UNKNOWN
```

### Comparing `nexus-utilities-0.3.1/nexus_utils/config_utils.py` & `nexus-utilities-0.4.0/nexus_utils/config_utils.py`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/nexus_utils/database_utils.py` & `nexus-utilities-0.4.0/nexus_utils/database_utils.py`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/nexus_utils/package_utils.py` & `nexus-utilities-0.4.0/nexus_utils/package_utils.py`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/nexus_utils/password_utils.py` & `nexus-utilities-0.4.0/nexus_utils/password_utils.py`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/nexus_utils/string_utils.py` & `nexus-utilities-0.4.0/nexus_utils/string_utils.py`

 * *Files identical despite different names*

### Comparing `nexus-utilities-0.3.1/setup.py` & `nexus-utilities-0.4.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='nexus-utilities',
-    version='0.3.1',
+    version='0.4.0',
     author='James Larsen',
     author_email='james.larsen42@gmail.com',
     description='Common python utilities',
     long_description='This package is meant to hold various useful utilities for functionality I find myself using across multiple projects.  I will try to keep this documentation updated as I expand the toolkit.',
     long_description_content_type='text/markdown',
     url='https://github.com/james-larsen/nexus-utilities',
     packages=['nexus_utils'],
```

