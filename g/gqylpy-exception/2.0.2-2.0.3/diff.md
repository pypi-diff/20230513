# Comparing `tmp/gqylpy_exception-2.0.2.tar.gz` & `tmp/gqylpy_exception-2.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gqylpy_exception-2.0.2.tar", last modified: Sat Apr 29 02:08:24 2023, max compression
+gzip compressed data, was "gqylpy_exception-2.0.3.tar", last modified: Sat May 13 02:44:00 2023, max compression
```

## Comparing `gqylpy_exception-2.0.2.tar` & `gqylpy_exception-2.0.3.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 02:08:24.015330 gqylpy_exception-2.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)    11389 2023-04-29 02:08:12.000000 gqylpy_exception-2.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-04-29 02:08:24.015330 gqylpy_exception-2.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-04-29 02:08:12.000000 gqylpy_exception-2.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 02:08:24.015330 gqylpy_exception-2.0.2/gqylpy_exception/
--rw-r--r--   0 runner    (1001) docker     (123)     8064 2023-04-29 02:08:12.000000 gqylpy_exception-2.0.2/gqylpy_exception/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9464 2023-04-29 02:08:12.000000 gqylpy_exception-2.0.2/gqylpy_exception/g exception.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 02:08:24.015330 gqylpy_exception-2.0.2/gqylpy_exception.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-04-29 02:08:24.000000 gqylpy_exception-2.0.2/gqylpy_exception.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      247 2023-04-29 02:08:24.000000 gqylpy_exception-2.0.2/gqylpy_exception.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-29 02:08:24.000000 gqylpy_exception-2.0.2/gqylpy_exception.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-04-29 02:08:24.000000 gqylpy_exception-2.0.2/gqylpy_exception.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-29 02:08:24.015330 gqylpy_exception-2.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1502 2023-04-29 02:08:12.000000 gqylpy_exception-2.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:44:00.619649 gqylpy_exception-2.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)    11389 2023-05-13 02:43:46.000000 gqylpy_exception-2.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-05-13 02:44:00.619649 gqylpy_exception-2.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-05-13 02:43:46.000000 gqylpy_exception-2.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:44:00.615649 gqylpy_exception-2.0.3/gqylpy_exception/
+-rw-r--r--   0 runner    (1001) docker     (123)     8261 2023-05-13 02:43:46.000000 gqylpy_exception-2.0.3/gqylpy_exception/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9472 2023-05-13 02:43:46.000000 gqylpy_exception-2.0.3/gqylpy_exception/g exception.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:44:00.619649 gqylpy_exception-2.0.3/gqylpy_exception.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-05-13 02:44:00.000000 gqylpy_exception-2.0.3/gqylpy_exception.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      247 2023-05-13 02:44:00.000000 gqylpy_exception-2.0.3/gqylpy_exception.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:44:00.000000 gqylpy_exception-2.0.3/gqylpy_exception.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 02:44:00.000000 gqylpy_exception-2.0.3/gqylpy_exception.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:44:00.619649 gqylpy_exception-2.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1666 2023-05-13 02:43:46.000000 gqylpy_exception-2.0.3/setup.py
```

### Comparing `gqylpy_exception-2.0.2/LICENSE` & `gqylpy_exception-2.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `gqylpy_exception-2.0.2/PKG-INFO` & `gqylpy_exception-2.0.3/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 Metadata-Version: 2.1
 Name: gqylpy_exception
-Version: 2.0.2
+Version: 2.0.3
 Summary: 在执行 raise 语句的同时创建异常类，无需事先定义异常类，方便快捷。
 Home-page: http://gqylpy.com
 Author: 竹永康
 Author-email: <gqylpy@outlook.com>
 License: Apache 2.0
 Project-URL: Source, https://github.com/gqylpy/gqylpy-exception
-Classifier: Environment :: Web Environment
+Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
+Classifier: Natural Language :: Chinese (Simplified)
+Classifier: Natural Language :: English
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
-Classifier: Topic :: Text Processing :: Indexing
-Classifier: Topic :: Utilities
-Classifier: Topic :: Internet
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Classifier: Topic :: Software Development :: Bug Tracking
+Classifier: Topic :: Software Development :: Widget Sets
+Classifier: Topic :: Artistic Software
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.12
 Requires-Python: >=3.6, <4
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 [<img alt="LOGO" src="http://www.gqylpy.com/static/img/favicon.ico" height="21" width="21"/>](http://www.gqylpy.com)
 [![Release](https://img.shields.io/github/release/gqylpy/gqylpy-exception.svg?style=flat-square")](https://github.com/gqylpy/gqylpy-exception/releases/latest)
 [![Python Versions](https://img.shields.io/pypi/pyversions/gqylpy_exception)](https://pypi.org/project/gqylpy_exception)
```

### Comparing `gqylpy_exception-2.0.2/README.md` & `gqylpy_exception-2.0.3/README.md`

 * *Files identical despite different names*

### Comparing `gqylpy_exception-2.0.2/gqylpy_exception/__init__.py` & `gqylpy_exception-2.0.3/gqylpy_exception/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 """
 Create the exception class while executing the `raise` statement, you no longer
 need to define an exception class in advance, Convenient and Fast.
 
     >>> import gqylpy_exception as ge
     >>> raise ge.AnError(...)
 
-    @version: 2.0.2
+    @version: 2.0.3
     @author: 竹永康 <gqylpy@outlook.com>
     @source: https://github.com/gqylpy/gqylpy-exception
 
 ────────────────────────────────────────────────────────────────────────────────
 Copyright (c) 2022, 2023 GQYLPY <http://gqylpy.com>. All rights reserved.
 
 Licensed under the Apache License, Version 2.0 (the "License");
@@ -191,20 +191,26 @@
     gpack = globals()
     gpath = f'{__name__}.g {__name__[7:]}'
     gcode = __import__(gpath, fromlist=...)
 
     ge = gcode.GqylpyException()
 
     for gname in gpack:
-        if gname[0] == '_':
-            setattr(ge, gname, gpack[gname])
-        else:
+        if gname[0] != '_':
             try:
                 gfunc = getattr(gcode, gname)
                 assert gfunc.__module__ in (gpath, __package__)
             except (AttributeError, AssertionError):
                 continue
             gfunc.__module__ = __package__
             setattr(ge, gname, gfunc)
+        elif not hasattr(ge, gname):
+            setattr(ge.__class__, gname, gpack[gname])
 
-    ge.__module__ = __package__
-    sys.modules[__name__] = ge.GqylpyException = ge
+    setattr(ge, __package__, ge.__class__)
+
+    ge.__doc__                = __doc__
+    ge.__name__               = __package__
+    ge.__class__.__qualname__ = __package__
+    ge.__class__.__module__   = __package__
+
+    sys.modules[__name__] = ge
```

### Comparing `gqylpy_exception-2.0.2/gqylpy_exception/g exception.py` & `gqylpy_exception-2.0.3/gqylpy_exception/g exception.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,25 +37,25 @@
 class GqylpyException:
     __history__ = {}
 
     def __getattr__(self, ename: str) -> Type['GqylpyError']:
         try:
             eclass = self.__history__[ename]
         except KeyError:
-            if hasattr(builtins, ename):
-                raise self.ExceptionClassIsBuiltinsError(
-                    f'exception class "{ename}" is builtins.'
-                ) from None
-            # Some special modules may attempt to call non-built-in magic
-            # method, such as `copy`, `pickle`. Compatible for this purpose.
             if ename[:2] == ename[-2:] == '__' and \
                     ename[2] != '_' and ename[-3] != '_':
+                # Some special modules may attempt to call non-built-in magic
+                # method, such as `copy`, `pickle`. Compatible for this purpose.
                 raise AttributeError(
                     f'"{__package__}" has no attribute "{ename}".'
                 ) from None
+            if hasattr(builtins, ename):
+                raise self.ExceptionClassIsBuiltinsError(
+                    f'exception class "{ename}" is builtins.'
+                ) from None
             if ename[-5:] != 'Error':
                 warnings.warn(
                     f'strange exception class "{ename}", exception class name '
                     'should end with "Error".', UserWarning, stacklevel=2
                 )
             eclass = self.__history__[ename] = type(
                 ename, (self.GqylpyError,), {'__module__': 'builtins'}
```

### Comparing `gqylpy_exception-2.0.2/gqylpy_exception.egg-info/PKG-INFO` & `gqylpy_exception-2.0.3/gqylpy_exception.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 Metadata-Version: 2.1
 Name: gqylpy-exception
-Version: 2.0.2
+Version: 2.0.3
 Summary: 在执行 raise 语句的同时创建异常类，无需事先定义异常类，方便快捷。
 Home-page: http://gqylpy.com
 Author: 竹永康
 Author-email: <gqylpy@outlook.com>
 License: Apache 2.0
 Project-URL: Source, https://github.com/gqylpy/gqylpy-exception
-Classifier: Environment :: Web Environment
+Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
+Classifier: Natural Language :: Chinese (Simplified)
+Classifier: Natural Language :: English
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
-Classifier: Topic :: Text Processing :: Indexing
-Classifier: Topic :: Utilities
-Classifier: Topic :: Internet
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Classifier: Topic :: Software Development :: Bug Tracking
+Classifier: Topic :: Software Development :: Widget Sets
+Classifier: Topic :: Artistic Software
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.12
 Requires-Python: >=3.6, <4
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 [<img alt="LOGO" src="http://www.gqylpy.com/static/img/favicon.ico" height="21" width="21"/>](http://www.gqylpy.com)
 [![Release](https://img.shields.io/github/release/gqylpy/gqylpy-exception.svg?style=flat-square")](https://github.com/gqylpy/gqylpy-exception/releases/latest)
 [![Python Versions](https://img.shields.io/pypi/pyversions/gqylpy_exception)](https://pypi.org/project/gqylpy_exception)
```

### Comparing `gqylpy_exception-2.0.2/setup.py` & `gqylpy_exception-2.0.3/setup.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 import setuptools
 import gqylpy_exception as g
 
-with open(g.__file__, encoding='utf8') as f:
-    for line in f:
-        if line.startswith('@version: ', 4):
-            version = line.split()[-1]
-            break
-    author, email = f.readline().split(maxsplit=1)[-1].rstrip().split()
-    source = f.readline().split()[-1]
+gdoc: list = g.__doc__.split('\n')
+
+for index, line in enumerate(gdoc):
+    if line.startswith('@version: ', 4):
+        version = line.split()[-1]
+        break
+_, author, email = gdoc[index + 1].split()
+source = gdoc[index + 2].split()[-1]
 
 setuptools.setup(
     name=g.__name__,
     version=version,
     author=author,
     author_email=email,
     license='Apache 2.0',
@@ -19,23 +20,26 @@
     project_urls={'Source': source},
     description='在执行 raise 语句的同时创建异常类，无需事先定义异常类，方便快捷。',
     long_description=open('README.md', encoding='utf8').read(),
     long_description_content_type='text/markdown',
     packages=[g.__name__],
     python_requires='>=3.6, <4',
     classifiers=[
-        'Environment :: Web Environment',
+        'Development Status :: 5 - Production/Stable',
         'Intended Audience :: Developers',
+        'Natural Language :: Chinese (Simplified)',
+        'Natural Language :: English',
         'License :: OSI Approved :: Apache Software License',
         'Operating System :: OS Independent',
-        'Topic :: Text Processing :: Indexing',
-        'Topic :: Utilities',
-        'Topic :: Internet',
         'Topic :: Software Development :: Libraries :: Python Modules',
+        'Topic :: Software Development :: Bug Tracking',
+        'Topic :: Software Development :: Widget Sets',
+        'Topic :: Artistic Software',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
-        'Programming Language :: Python :: 3.11'
+        'Programming Language :: Python :: 3.11',
+        'Programming Language :: Python :: 3.12'
     ]
 )
```

