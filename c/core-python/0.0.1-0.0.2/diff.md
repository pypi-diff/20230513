# Comparing `tmp/core-python-0.0.1.tar.gz` & `tmp/core-python-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "core-python-0.0.1.tar", last modified: Sat May 13 15:13:23 2023, max compression
+gzip compressed data, was "core-python-0.0.2.tar", last modified: Sat May 13 15:24:02 2023, max compression
```

## Comparing `core-python-0.0.1.tar` & `core-python-0.0.2.tar`

### file list

```diff
@@ -1,13 +1,16 @@
-drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:13:23.543389 core-python-0.0.1/
--rw-r--r--   0 seunggabi   (501) staff       (20)     1070 2023-05-13 14:31:33.000000 core-python-0.0.1/LICENSE
--rw-r--r--   0 seunggabi   (501) staff       (20)      565 2023-05-13 15:13:23.543259 core-python-0.0.1/PKG-INFO
--rw-r--r--   0 seunggabi   (501) staff       (20)      279 2023-05-13 15:13:10.000000 core-python-0.0.1/README.md
-drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:13:23.542884 core-python-0.0.1/core_python.egg-info/
--rw-r--r--   0 seunggabi   (501) staff       (20)      565 2023-05-13 15:13:23.000000 core-python-0.0.1/core_python.egg-info/PKG-INFO
--rw-r--r--   0 seunggabi   (501) staff       (20)      182 2023-05-13 15:13:23.000000 core-python-0.0.1/core_python.egg-info/SOURCES.txt
--rw-r--r--   0 seunggabi   (501) staff       (20)        1 2023-05-13 15:13:23.000000 core-python-0.0.1/core_python.egg-info/dependency_links.txt
--rw-r--r--   0 seunggabi   (501) staff       (20)        4 2023-05-13 15:13:23.000000 core-python-0.0.1/core_python.egg-info/top_level.txt
--rw-r--r--   0 seunggabi   (501) staff       (20)       38 2023-05-13 15:13:23.543423 core-python-0.0.1/setup.cfg
--rw-r--r--   0 seunggabi   (501) staff       (20)      681 2023-05-13 15:07:25.000000 core-python-0.0.1/setup.py
-drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:13:23.543054 core-python-0.0.1/src/
--rw-r--r--   0 seunggabi   (501) staff       (20)       22 2023-05-13 15:08:10.000000 core-python-0.0.1/src/__init__.py
+drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:24:02.825125 core-python-0.0.2/
+-rw-r--r--   0 seunggabi   (501) staff       (20)     1070 2023-05-13 14:31:33.000000 core-python-0.0.2/LICENSE
+-rw-r--r--   0 seunggabi   (501) staff       (20)      563 2023-05-13 15:24:02.825013 core-python-0.0.2/PKG-INFO
+-rw-r--r--   0 seunggabi   (501) staff       (20)      351 2023-05-13 15:23:57.000000 core-python-0.0.2/README.md
+drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:24:02.824175 core-python-0.0.2/core-python/
+-rw-r--r--   0 seunggabi   (501) staff       (20)       22 2023-05-13 15:23:09.000000 core-python-0.0.2/core-python/__init__.py
+drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:24:02.824398 core-python-0.0.2/core-python/util/
+-rw-r--r--   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:22:13.000000 core-python-0.0.2/core-python/util/__init__.py
+-rw-r--r--   0 seunggabi   (501) staff       (20)      142 2023-05-13 14:44:24.000000 core-python-0.0.2/core-python/util/json_util.py
+drwxr-xr-x   0 seunggabi   (501) staff       (20)        0 2023-05-13 15:24:02.824867 core-python-0.0.2/core_python.egg-info/
+-rw-r--r--   0 seunggabi   (501) staff       (20)      563 2023-05-13 15:24:02.000000 core-python-0.0.2/core_python.egg-info/PKG-INFO
+-rw-r--r--   0 seunggabi   (501) staff       (20)      249 2023-05-13 15:24:02.000000 core-python-0.0.2/core_python.egg-info/SOURCES.txt
+-rw-r--r--   0 seunggabi   (501) staff       (20)        1 2023-05-13 15:24:02.000000 core-python-0.0.2/core_python.egg-info/dependency_links.txt
+-rw-r--r--   0 seunggabi   (501) staff       (20)       12 2023-05-13 15:24:02.000000 core-python-0.0.2/core_python.egg-info/top_level.txt
+-rw-r--r--   0 seunggabi   (501) staff       (20)       38 2023-05-13 15:24:02.825154 core-python-0.0.2/setup.cfg
+-rw-r--r--   0 seunggabi   (501) staff       (20)      679 2023-05-13 15:23:12.000000 core-python-0.0.2/setup.py
```

### Comparing `core-python-0.0.1/LICENSE` & `core-python-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `core-python-0.0.1/PKG-INFO` & `core-python-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: core-python
-Version: 0.0.1
+Version: 0.0.2
 Summary: A collection of core Python modules
 Home-page: https://github.com/seunggabi/core-python
 Author: seunggabi
-Author-email: seunggabi@example.com
+Author-email: seunggabi@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `core-python-0.0.1/core_python.egg-info/PKG-INFO` & `core-python-0.0.2/core_python.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: core-python
-Version: 0.0.1
+Version: 0.0.2
 Summary: A collection of core Python modules
 Home-page: https://github.com/seunggabi/core-python
 Author: seunggabi
-Author-email: seunggabi@example.com
+Author-email: seunggabi@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `core-python-0.0.1/setup.py` & `core-python-0.0.2/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 setup(
     name='core-python',
-    version='0.0.1',
+    version='0.0.2',
     description='A collection of core Python modules',
     author='seunggabi',
-    author_email='seunggabi@example.com',
+    author_email='seunggabi@gmail.com',
     url='https://github.com/seunggabi/core-python',
     packages=find_packages(),
     install_requires=[],
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
```

