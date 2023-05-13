# Comparing `tmp/myfuncs-0.1.0.tar.gz` & `tmp/myfuncs-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "myfuncs-0.1.0.tar", last modified: Sat May 13 18:52:49 2023, max compression
+gzip compressed data, was "myfuncs-0.1.1.tar", last modified: Sat May 13 19:13:34 2023, max compression
```

## Comparing `myfuncs-0.1.0.tar` & `myfuncs-0.1.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 18:52:49.286688 myfuncs-0.1.0/
--rw-r--r--   0 work       (501) staff       (20)     1068 2023-05-13 16:42:37.000000 myfuncs-0.1.0/LICENSE
--rw-r--r--   0 work       (501) staff       (20)      704 2023-05-13 18:52:49.286550 myfuncs-0.1.0/PKG-INFO
--rw-r--r--   0 work       (501) staff       (20)       40 2023-05-13 16:42:37.000000 myfuncs-0.1.0/README.md
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 18:52:49.285909 myfuncs-0.1.0/myfuncs/
--rw-r--r--   0 work       (501) staff       (20)       21 2023-05-13 18:23:34.000000 myfuncs-0.1.0/myfuncs/__init__.py
--rw-r--r--   0 work       (501) staff       (20)     3183 2023-05-13 18:51:04.000000 myfuncs-0.1.0/myfuncs/funcs.py
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 18:52:49.286385 myfuncs-0.1.0/myfuncs.egg-info/
--rw-r--r--   0 work       (501) staff       (20)      704 2023-05-13 18:52:49.000000 myfuncs-0.1.0/myfuncs.egg-info/PKG-INFO
--rw-r--r--   0 work       (501) staff       (20)      187 2023-05-13 18:52:49.000000 myfuncs-0.1.0/myfuncs.egg-info/SOURCES.txt
--rw-r--r--   0 work       (501) staff       (20)        1 2023-05-13 18:52:49.000000 myfuncs-0.1.0/myfuncs.egg-info/dependency_links.txt
--rw-r--r--   0 work       (501) staff       (20)        8 2023-05-13 18:52:49.000000 myfuncs-0.1.0/myfuncs.egg-info/top_level.txt
--rw-r--r--   0 work       (501) staff       (20)       38 2023-05-13 18:52:49.286728 myfuncs-0.1.0/setup.cfg
--rw-r--r--   0 work       (501) staff       (20)      843 2023-05-13 18:19:51.000000 myfuncs-0.1.0/setup.py
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:13:34.059495 myfuncs-0.1.1/
+-rw-r--r--   0 work       (501) staff       (20)     1068 2023-05-13 16:42:37.000000 myfuncs-0.1.1/LICENSE
+-rw-r--r--   0 work       (501) staff       (20)      778 2023-05-13 19:13:34.059365 myfuncs-0.1.1/PKG-INFO
+-rw-r--r--   0 work       (501) staff       (20)       40 2023-05-13 16:42:37.000000 myfuncs-0.1.1/README.md
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:13:34.058718 myfuncs-0.1.1/myfuncs/
+-rw-r--r--   0 work       (501) staff       (20)       21 2023-05-13 18:23:34.000000 myfuncs-0.1.1/myfuncs/__init__.py
+-rw-r--r--   0 work       (501) staff       (20)     3354 2023-05-13 19:09:56.000000 myfuncs-0.1.1/myfuncs/funcs.py
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:13:34.059191 myfuncs-0.1.1/myfuncs.egg-info/
+-rw-r--r--   0 work       (501) staff       (20)      778 2023-05-13 19:13:34.000000 myfuncs-0.1.1/myfuncs.egg-info/PKG-INFO
+-rw-r--r--   0 work       (501) staff       (20)      187 2023-05-13 19:13:34.000000 myfuncs-0.1.1/myfuncs.egg-info/SOURCES.txt
+-rw-r--r--   0 work       (501) staff       (20)        1 2023-05-13 19:13:34.000000 myfuncs-0.1.1/myfuncs.egg-info/dependency_links.txt
+-rw-r--r--   0 work       (501) staff       (20)        8 2023-05-13 19:13:34.000000 myfuncs-0.1.1/myfuncs.egg-info/top_level.txt
+-rw-r--r--   0 work       (501) staff       (20)       38 2023-05-13 19:13:34.059538 myfuncs-0.1.1/setup.cfg
+-rw-r--r--   0 work       (501) staff       (20)      916 2023-05-13 19:12:58.000000 myfuncs-0.1.1/setup.py
```

### Comparing `myfuncs-0.1.0/LICENSE` & `myfuncs-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `myfuncs-0.1.0/PKG-INFO` & `myfuncs-0.1.1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 Metadata-Version: 2.1
 Name: myfuncs
-Version: 0.1.0
-Summary: Personal utility functions for Cary Carter
+Version: 0.1.1
+Summary: Personal utility functions that I use across different codebases.
 Home-page: https://github.com/cc-d/myfuncs
 Author: Cary Carter
 Author-email: ccarterdev@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # myfuncs
 For my 'myfuncs' pip package.
```

### Comparing `myfuncs-0.1.0/myfuncs/funcs.py` & `myfuncs-0.1.1/myfuncs/funcs.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 import re
 import time
 import inspect
 from datetime import datetime
 from functools import wraps
-from typing import Any, Callable, Optional, TypeVar
+from typing import Any, Callable, Optional, TypeVar, Union
 
 import logging
 
 logger = logging.getLogger(__name__)
 
 T = TypeVar("T", bound=Callable[..., Any])
 
@@ -19,37 +19,40 @@
 
     Returns:
         str: current asctime
     """
     now = datetime.now()
     return now.strftime(f"%Y-%m-%d %H:%M:%S")
 
-
 def logf(
-    level: Optional[int] = logging.DEBUG,
+    level: Optional[Union[int, str]] = logging.DEBUG,
     log_args: bool = True,
     log_return: bool = True,
     max_vlen: int = 1000,
     measure_time: bool = True
 ) -> Callable[[T], T]:
     """
     A decorator that logs the execution time, function name, arguments, keyword arguments,
     and return value of a function using a specified log level.
 
     Args:
-        level (int, optional): The log level to use for logging. Defaults to logging.DEBUG.
+        level (Union[int, str], optional): The log level to use for logging. Defaults to logging.DEBUG.
         log_args (bool, optional): Should the function arguments be logged? Defaults to True.
         log_return (bool, optional): Should function return be logged? Defaults to True.
         max_vlen (int, optional): Maximum length of the logged arguments and return values. Defaults to 1000.
         measure_time (bool, optional): Should the function execution time be measured? Defaults to True.
 
     Returns:
         Callable[[T], T]: The wrapped function.
     """
 
+    # Convert log level to integer if provided as string
+    if isinstance(level, str):
+        level = logging.getLevelName(level.upper())
+
     def decorator(func: T) -> T:
         @wraps(func)
         def wrapper(*args: Any, **kwargs: Any) -> Any:
             # Start the timer if required and execute the function.
             start_time = time.time() if measure_time else None
 
             # Log function arguments if required
```

### Comparing `myfuncs-0.1.0/myfuncs.egg-info/PKG-INFO` & `myfuncs-0.1.1/myfuncs.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 Metadata-Version: 2.1
 Name: myfuncs
-Version: 0.1.0
-Summary: Personal utility functions for Cary Carter
+Version: 0.1.1
+Summary: Personal utility functions that I use across different codebases.
 Home-page: https://github.com/cc-d/myfuncs
 Author: Cary Carter
 Author-email: ccarterdev@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # myfuncs
 For my 'myfuncs' pip package.
```

### Comparing `myfuncs-0.1.0/setup.py` & `myfuncs-0.1.1/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 from setuptools import setup, find_packages
 
 setup(
     name='myfuncs',
-    version='0.1.0',
+    version='0.1.1',
     packages=find_packages(),
     install_requires=[],
     author='Cary Carter',
     author_email='ccarterdev@gmail.com',
-    description='Personal utility functions for Cary Carter',
+    description='Personal utility functions that I use across different codebases.',
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url='https://github.com/cc-d/myfuncs',
     license='MIT',
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
+        'Programming Language :: Python :: 3.10',
     ],
 )
```

