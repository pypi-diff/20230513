# Comparing `tmp/upathlib-0.8.0.tar.gz` & `tmp/upathlib-0.8.1b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "upathlib-0.8.0.tar", last modified: Tue Apr 25 18:31:07 2023, max compression
+gzip compressed data, was "upathlib-0.8.1b1.tar", last modified: Sat May 13 05:40:25 2023, max compression
```

## Comparing `upathlib-0.8.0.tar` & `upathlib-0.8.1b1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0     1067 2022-12-13 07:44:37.384893 upathlib-0.8.0/LICENSE
--rw-r--r--   0        0        0      993 2023-03-30 16:49:23.794031 upathlib-0.8.0/README.rst
--rw-r--r--   0        0        0     1726 2023-04-25 03:21:53.568059 upathlib-0.8.0/pyproject.toml
--rw-r--r--   0        0        0     2319 2023-04-25 18:28:34.087864 upathlib-0.8.0/src/upathlib/__init__.py
--rw-r--r--   0        0        0     4694 2023-04-20 04:34:46.179551 upathlib-0.8.0/src/upathlib/_blob.py
--rw-r--r--   0        0        0    10954 2023-04-25 03:21:53.568059 upathlib-0.8.0/src/upathlib/_local.py
--rw-r--r--   0        0        0     7935 2023-04-20 04:34:46.179551 upathlib-0.8.0/src/upathlib/_tests.py
--rw-r--r--   0        0        0    34484 2023-04-25 03:21:53.568059 upathlib-0.8.0/src/upathlib/_upath.py
--rw-r--r--   0        0        0    12562 2023-04-10 08:06:32.346660 upathlib-0.8.0/src/upathlib/azure.py
--rw-r--r--   0        0        0    25613 2023-04-25 07:49:10.489394 upathlib-0.8.0/src/upathlib/gcs.py
--rw-r--r--   0        0        0        0 2022-12-13 07:44:37.384893 upathlib-0.8.0/src/upathlib/py.typed
--rw-r--r--   0        0        0     3763 2023-04-10 08:06:32.346660 upathlib-0.8.0/src/upathlib/serializer.py
--rw-r--r--   0        0        0     2381 1970-01-01 00:00:00.000000 upathlib-0.8.0/PKG-INFO
+-rw-r--r--   0        0        0     1067 2022-12-13 07:44:37.384893 upathlib-0.8.1b1/LICENSE
+-rw-r--r--   0        0        0      993 2023-03-30 16:49:23.794031 upathlib-0.8.1b1/README.rst
+-rw-r--r--   0        0        0     1726 2023-04-25 03:21:53.568059 upathlib-0.8.1b1/pyproject.toml
+-rw-r--r--   0        0        0     2321 2023-05-13 05:35:51.869975 upathlib-0.8.1b1/src/upathlib/__init__.py
+-rw-r--r--   0        0        0     4694 2023-04-20 04:34:46.179551 upathlib-0.8.1b1/src/upathlib/_blob.py
+-rw-r--r--   0        0        0    10749 2023-05-13 05:38:06.231654 upathlib-0.8.1b1/src/upathlib/_local.py
+-rw-r--r--   0        0        0     7935 2023-04-20 04:34:46.179551 upathlib-0.8.1b1/src/upathlib/_tests.py
+-rw-r--r--   0        0        0    34484 2023-04-25 03:21:53.568059 upathlib-0.8.1b1/src/upathlib/_upath.py
+-rw-r--r--   0        0        0    12562 2023-04-10 08:06:32.346660 upathlib-0.8.1b1/src/upathlib/azure.py
+-rw-r--r--   0        0        0    26057 2023-05-13 05:38:06.231654 upathlib-0.8.1b1/src/upathlib/gcs.py
+-rw-r--r--   0        0        0        0 2022-12-13 07:44:37.384893 upathlib-0.8.1b1/src/upathlib/py.typed
+-rw-r--r--   0        0        0     3763 2023-04-10 08:06:32.346660 upathlib-0.8.1b1/src/upathlib/serializer.py
+-rw-r--r--   0        0        0     2383 1970-01-01 00:00:00.000000 upathlib-0.8.1b1/PKG-INFO
```

### Comparing `upathlib-0.8.0/LICENSE` & `upathlib-0.8.1b1/LICENSE`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/README.rst` & `upathlib-0.8.1b1/README.rst`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/pyproject.toml` & `upathlib-0.8.1b1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/src/upathlib/__init__.py` & `upathlib-0.8.1b1/src/upathlib/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 
 One use case is the package `biglist <https://biglist.readthedocs.io/en/latest/>`__,
 where the class `Biglist <https://biglist.readthedocs.io/en/latest/#biglist.Biglist>`__ takes a Upath object to indicate its location of storage.
 It does not care whether the storage is local or in a cloud blob store---it
 simply uses the common API to operate the storage.
 """
 
-__version__ = "0.8.0"
+__version__ = "0.8.1b1"
 
 
 from pathlib import Path
 from typing import Union
 
 from ._blob import BlobUpath
 from ._local import LocalPathType, LocalUpath
```

### Comparing `upathlib-0.8.0/src/upathlib/_blob.py` & `upathlib-0.8.1b1/src/upathlib/_blob.py`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/src/upathlib/_local.py` & `upathlib-0.8.1b1/src/upathlib/_local.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,16 +15,14 @@
 
 # `filelock` is also called `py-filelock`.
 # Tried `fasteners` also. In one use case,
 # `filelock` worked whereas `fasteners.InterprocessLock` failed.
 #
 # Other options to look into include
 # `oslo.concurrency`, `pylocker`, `portalocker`.
-from deprecation import deprecated
-
 from ._upath import FileInfo, LockAcquireError, LockReleaseError, Upath
 
 # End user may want to do this:
 # logging.getLogger("filelock").setLevel(logging.WARNING)
 
 
 class LocalUpath(Upath, os.PathLike):
@@ -73,21 +71,14 @@
     def path(self) -> pathlib.Path:
         """
         Return the `pathlib.Path <https://docs.python.org/3/library/pathlib.html#pathlib.Path>`_ object
         of the path.
         """
         return pathlib.Path(self._path)
 
-    @property
-    @deprecated(
-        deprecated_in="0.6.9", removed_in="0.8.0", details="Use `path` instead."
-    )
-    def localpath(self):
-        return self.path
-
     def as_uri(self) -> str:
         """
         Represent the path as a file URI.
         On Linux, this is like 'file:///home/username/path/to/file'.
         On Windows, this is like 'file:///C:/Users/username/path/to/file'.
         """
         return self.path.as_uri()
```

### Comparing `upathlib-0.8.0/src/upathlib/_tests.py` & `upathlib-0.8.1b1/src/upathlib/_tests.py`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/src/upathlib/_upath.py` & `upathlib-0.8.1b1/src/upathlib/_upath.py`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/src/upathlib/azure.py` & `upathlib-0.8.1b1/src/upathlib/azure.py`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/src/upathlib/gcs.py` & `upathlib-0.8.1b1/src/upathlib/gcs.py`

 * *Files 4% similar despite different names*

```diff
@@ -41,14 +41,25 @@
 # 67108864 = 256 * 1024 * 256 = 64 MB
 MEGABYTES32 = 33554432
 MEGABYTES64 = 67108864
 LARGE_FILE_SIZE = MEGABYTES64
 
 # DEFAULT_RETRY has default timeout 120 seconds.
 
+# Workaround:
+# The availability of `Retry.with_timeout` is in a messy state
+# between versions of `google-api-core`.
+if not hasattr(DEFAULT_RETRY, 'with_timeout'):
+    if hasattr(DEFAULT_RETRY, 'with_deadline'):
+        DEFAULT_RETRY.with_timeout = DEFAULT_RETRY.with_deadline
+    else:
+        raise ImportError(
+            'Retry has neither `with_timeout` nor `with_deadline`; please look into the version of `google-api-core`'
+        )
+
 
 def get_google_auth(
     project_id=None,
     credentials=None,
     *,
     scopes: list[str] = None,
     valid_for_seconds: int = 300,
```

### Comparing `upathlib-0.8.0/src/upathlib/serializer.py` & `upathlib-0.8.1b1/src/upathlib/serializer.py`

 * *Files identical despite different names*

### Comparing `upathlib-0.8.0/PKG-INFO` & `upathlib-0.8.1b1/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: upathlib
-Version: 0.8.0
+Version: 0.8.1b1
 Summary: The package *upathlib*
 Author-email: Zepu Zhang <zepu.zhang@gmail.com>
 Requires-Python: >=3.8
 Description-Content-Type: text/x-rst
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
```

