# Comparing `tmp/replicat-1.3.2.tar.gz` & `tmp/replicat-1.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "replicat-1.3.2.tar", last modified: Sun Nov 13 21:46:10 2022, max compression
+gzip compressed data, was "replicat-1.4.0.tar", last modified: Sat May 13 14:20:39 2023, max compression
```

## Comparing `replicat-1.3.2.tar` & `replicat-1.4.0.tar`

### file list

```diff
@@ -1,41 +1,43 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.698698 replicat-1.3.2/
--rw-r--r--   0 runner    (1001) docker     (121)      290 2022-11-13 21:46:03.000000 replicat-1.3.2/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1064 2022-11-13 21:46:03.000000 replicat-1.3.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       41 2022-11-13 21:46:03.000000 replicat-1.3.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)    22232 2022-11-13 21:46:10.698698 replicat-1.3.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)    21851 2022-11-13 21:46:03.000000 replicat-1.3.2/README.md
--rw-r--r--   0 runner    (1001) docker     (121)      566 2022-11-13 21:46:03.000000 replicat-1.3.2/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.694698 replicat-1.3.2/replicat/
--rw-r--r--   0 runner    (1001) docker     (121)     5040 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/__main__.py
--rw-r--r--   0 runner    (1001) docker     (121)      330 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/__version__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.698698 replicat-1.3.2/replicat/backends/
--rw-r--r--   0 runner    (1001) docker     (121)     9814 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/backends/b2.py
--rw-r--r--   0 runner    (1001) docker     (121)     2231 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/backends/base.py
--rw-r--r--   0 runner    (1001) docker     (121)     4365 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/backends/local.py
--rw-r--r--   0 runner    (1001) docker     (121)      369 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/backends/s3.py
--rw-r--r--   0 runner    (1001) docker     (121)    10432 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/backends/s3c.py
--rw-r--r--   0 runner    (1001) docker     (121)      136 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (121)    67547 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/repository.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.698698 replicat-1.3.2/replicat/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      393 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (121)    10481 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/test_adapters.py
--rw-r--r--   0 runner    (1001) docker     (121)     2492 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/test_local.py
--rw-r--r--   0 runner    (1001) docker     (121)    50681 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/test_repository.py
--rw-r--r--   0 runner    (1001) docker     (121)     8793 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/tests/test_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.698698 replicat-1.3.2/replicat/utils/
--rw-r--r--   0 runner    (1001) docker     (121)    19476 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     6377 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/utils/adapters.py
--rw-r--r--   0 runner    (1001) docker     (121)      286 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/utils/compat.py
--rw-r--r--   0 runner    (1001) docker     (121)      830 2022-11-13 21:46:03.000000 replicat-1.3.2/replicat/utils/fs.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.694698 replicat-1.3.2/replicat.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)    22232 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      784 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       52 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)      113 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       28 2022-11-13 21:46:10.000000 replicat-1.3.2/replicat.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      146 2022-11-13 21:46:10.698698 replicat-1.3.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     3585 2022-11-13 21:46:03.000000 replicat-1.3.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 21:46:10.698698 replicat-1.3.2/src/
--rw-r--r--   0 runner    (1001) docker     (121)     2798 2022-11-13 21:46:03.000000 replicat-1.3.2/src/adapters.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.198750 replicat-1.4.0/
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-13 14:20:31.000000 replicat-1.4.0/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 14:20:31.000000 replicat-1.4.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-13 14:20:31.000000 replicat-1.4.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    35102 2023-05-13 14:20:39.198750 replicat-1.4.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    34664 2023-05-13 14:20:31.000000 replicat-1.4.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      566 2023-05-13 14:20:31.000000 replicat-1.4.0/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.194750 replicat-1.4.0/replicat/
+-rw-r--r--   0 runner    (1001) docker     (123)     8269 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      330 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/__version__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.198750 replicat-1.4.0/replicat/backends/
+-rw-r--r--   0 runner    (1001) docker     (123)     9990 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/backends/b2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2481 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/backends/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4506 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/backends/local.py
+-rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/backends/s3.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10720 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/backends/s3c.py
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    74745 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/repository.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.198750 replicat-1.4.0/replicat/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13574 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/test_adapters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2492 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/test_local.py
+-rw-r--r--   0 runner    (1001) docker     (123)    64622 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/test_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24140 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/tests/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.198750 replicat-1.4.0/replicat/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)    12045 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8850 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/adapters.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13093 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/compat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6786 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 14:20:31.000000 replicat-1.4.0/replicat/utils/fs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.194750 replicat-1.4.0/replicat.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    35102 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      831 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      202 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 14:20:39.000000 replicat-1.4.0/replicat.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      146 2023-05-13 14:20:39.198750 replicat-1.4.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     3768 2023-05-13 14:20:31.000000 replicat-1.4.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:20:39.198750 replicat-1.4.0/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     2798 2023-05-13 14:20:31.000000 replicat-1.4.0/src/adapters.cpp
```

### Comparing `replicat-1.3.2/LICENSE` & `replicat-1.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `replicat-1.3.2/pyproject.toml` & `replicat-1.4.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `replicat-1.3.2/replicat/backends/b2.py` & `replicat-1.4.0/replicat/backends/b2.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from contextlib import suppress
 from urllib.parse import quote
 
 import backoff
 import httpx
 
 from .. import exceptions, utils
-from .base import Backend
+from .base import DEFAULT_STREAM_CHUNK_SIZE, Backend
 
 logger = logging.getLogger(__name__)
 
 
 def _check_403(e):
     return (
         isinstance(e, httpx.HTTPStatusError)
@@ -165,26 +165,30 @@
             'content-length': str(len(data)),
             'x-bz-content-sha1': 'do_not_verify',  # TODO
         }
         await self._client.post(upload_url, headers=upload_headers, content=data)
 
     @utils.requires_auth
     @backoff_reauth
-    async def upload_stream(self, name, stream, length):
+    async def upload_stream(
+        self, name, stream, length, chunk_size=DEFAULT_STREAM_CHUNK_SIZE
+    ):
         upload_url, upload_token = await self._get_upload_url_token()
         upload_headers = {
             'authorization': upload_token,
             'x-bz-file-name': quote(name),
             'content-type': 'application/octet-stream',
             'content-length': str(length),
             'x-bz-content-sha1': 'do_not_verify',  # TODO
         }
         try:
             await self._client.post(
-                upload_url, headers=upload_headers, content=utils.aiter_chunks(stream)
+                upload_url,
+                headers=upload_headers,
+                content=utils.aiter_chunks(stream, chunk_size=chunk_size),
             )
         except:
             stream.seek(0)
             raise
 
     @utils.requires_auth
     @backoff_reauth
@@ -193,27 +197,27 @@
         url = f'{self._auth.downloadUrl}/file/{bucket.name}/{name}'
         headers = {'authorization': self._auth.authorizationToken}
         response = await self._client.get(url, headers=headers)
         return await response.aread()
 
     @utils.requires_auth
     @backoff_reauth
-    async def download_stream(self, name, stream):
+    async def download_stream(self, name, stream, chunk_size=DEFAULT_STREAM_CHUNK_SIZE):
         bucket = await self._get_bucket()
         url = f'{self._auth.downloadUrl}/file/{bucket.name}/{name}'
         headers = {'authorization': self._auth.authorizationToken}
 
         async with self._client.stream('GET', url, headers=headers) as response:
             content_length = response.headers.get('content-length')
             if content_length is not None:
                 content_length = int(content_length)
 
             try:
                 stream.truncate(content_length)
-                async for chunk in response.aiter_bytes(128_000):
+                async for chunk in response.aiter_bytes(chunk_size):
                     stream.write(chunk)
             except:
                 stream.seek(0)
                 raise
 
     @utils.requires_auth
     @backoff_reauth
```

### Comparing `replicat-1.3.2/replicat/backends/base.py` & `replicat-1.4.0/replicat/backends/base.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,71 +1,80 @@
+from __future__ import annotations
+
 import abc
 import logging
 
 logger = logging.getLogger(__name__)
 
 
+DEFAULT_STREAM_CHUNK_SIZE = 128_000
+
+
 class Backend(abc.ABC):
 
     """All of the methods can be either async or plain functions. Backend adapters
     are responsible for implementing their own fault handling and retry strategies"""
 
-    def __init__(self, connection_string, **ka):
+    def __init__(self, connection_string, **ka) -> None:
         pass
 
     @abc.abstractmethod
     async def exists(self, name) -> bool:
         """Check whether a file with this name exists at the backend"""
         return True
 
     @abc.abstractmethod
-    async def upload(self, name, data):
+    async def upload(self, name, data) -> None:
         """Upload bytes-like data to the backend under this name"""
         return None
 
     @abc.abstractmethod
-    async def upload_stream(self, name, stream, length):
+    async def upload_stream(
+        self, name, stream, length, chunk_size=DEFAULT_STREAM_CHUNK_SIZE
+    ) -> None:
         """Upload seekable file-like stream to the backend under this name"""
         return None
 
     @abc.abstractmethod
     async def download(self, name) -> bytes:
         """Download file from the backend by name and return its contents as bytes"""
         return b''
 
     @abc.abstractmethod
-    async def download_stream(self, name, stream):
+    async def download_stream(
+        self, name, stream, chunk_size=DEFAULT_STREAM_CHUNK_SIZE
+    ) -> None:
         return None
 
     @abc.abstractmethod
     async def list_files(self, prefix=''):
         """Get the list of files from the backend. Restricts the results to
         non-deleted files starting with this prefix. The return value can be a
         plain iterable or an async iterator"""
         return None
 
     @abc.abstractmethod
-    async def delete(self, name):
+    async def delete(self, name) -> None:
         """Delete file by name"""
         return None
 
-    async def authenticate(self):
+    async def authenticate(self) -> None:
         """Called to authenticate the client (see the @requires_auth decorator).
         Must have the same type as the function that requires authentication"""
         raise NotImplementedError
 
-    async def clean(self):
+    async def clean(self) -> None:
         """Perform clean up at the backend"""
         pass
 
-    async def close(self):
+    async def close(self) -> None:
         """Close instance resources"""
         pass
 
-    def __init_subclass__(cls, /, short_name=None, display_name=None, **kwargs):
+    def __init_subclass__(cls, /, short_name=None, display_name=None, **kwargs) -> None:
         super().__init_subclass__(**kwargs)
 
         if short_name is None:
             short_name = cls.__name__
 
         if display_name is None:
             display_name = short_name
```

### Comparing `replicat-1.3.2/replicat/backends/local.py` & `replicat-1.4.0/replicat/backends/local.py`

 * *Files 11% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import shutil
 from pathlib import Path
 from tempfile import NamedTemporaryFile
 
 import backoff
 
 from ..utils.fs import iterative_scandir
-from .base import Backend
+from .base import DEFAULT_STREAM_CHUNK_SIZE, Backend
 
 logger = logging.getLogger(__name__)
 backoff_on_oserror = backoff.on_exception(backoff.fibo, OSError, max_tries=5)
 
 
 class Local(Backend):
     def __init__(self, connection_string):
@@ -47,37 +47,37 @@
             # replaced simultaneously from multiple threads (in CI, at least)
             temp.replace(destination)
         except:
             temp.unlink(missing_ok=True)
             raise
 
     @backoff_on_oserror
-    def upload_stream(self, name, stream, length):
+    def upload_stream(self, name, stream, length, chunk_size=DEFAULT_STREAM_CHUNK_SIZE):
         destination, temp = self._destination_temp(name)
         try:
             with temp.open('wb') as file:
-                shutil.copyfileobj(stream, file)
+                shutil.copyfileobj(stream, file, length=chunk_size)
             temp.replace(destination)
         except:
             temp.unlink(missing_ok=True)
             stream.seek(0)
             raise
 
     @backoff_on_oserror
     def download(self, name):
         return (self.path / name).read_bytes()
 
     @backoff_on_oserror
-    def download_stream(self, name, stream):
+    def download_stream(self, name, stream, chunk_size=DEFAULT_STREAM_CHUNK_SIZE):
         file = (self.path / name).open('rb')
         length = os.fstat(file.fileno()).st_size
         try:
             stream.truncate(length)
             with file:
-                shutil.copyfileobj(file, stream)
+                shutil.copyfileobj(file, stream, length=chunk_size)
         except:
             stream.seek(0)
             raise
 
     @backoff_on_oserror
     def list_files(self, prefix=''):
         path_length = len(str(self.path))
```

### Comparing `replicat-1.3.2/replicat/backends/s3c.py` & `replicat-1.4.0/replicat/backends/s3c.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from urllib.parse import quote, urlencode
 from xml.etree.ElementTree import XMLPullParser
 
 import backoff
 import httpx
 
 from .. import utils
-from .base import Backend
+from .base import DEFAULT_STREAM_CHUNK_SIZE, Backend
 
 logger = logging.getLogger(__name__)
 
 
 def _get_data_hexdigest(data):
     return hashlib.sha256(data).hexdigest()
 
@@ -258,54 +258,64 @@
         )
 
     async def upload(self, name, data):
         payload_digest = _get_data_hexdigest(data)
         await self._put_object(name, data, payload_digest)
 
     @backoff_on_httperror
-    async def _put_object_stream(self, name, stream, length, payload_digest):
+    async def _put_object_stream(
+        self, name, stream, *, length, payload_digest, chunk_size
+    ):
         try:
             await self._make_request(
                 'PUT',
                 f'/{self.bucket_name}/{name}',
-                content=utils.aiter_chunks(stream),
+                content=utils.aiter_chunks(stream, chunk_size=chunk_size),
                 payload_digest=payload_digest,
                 headers={'content-length': str(length)},
             )
         except:
             stream.seek(0)
             raise
 
-    async def upload_stream(self, name, stream, length):
+    async def upload_stream(
+        self, name, stream, length, chunk_size=DEFAULT_STREAM_CHUNK_SIZE
+    ):
         payload_digest = _get_stream_hexdigest(stream)
-        await self._put_object_stream(name, stream, length, payload_digest)
+        await self._put_object_stream(
+            name,
+            stream,
+            length=length,
+            payload_digest=payload_digest,
+            chunk_size=chunk_size,
+        )
 
     @backoff_on_httperror
     async def download(self, name):
         response = await self._make_request(
             'GET',
             f'/{self.bucket_name}/{name}',
             payload_digest=_empty_payload_digest,
         )
         return await response.aread()
 
     @backoff_on_httperror
-    async def download_stream(self, name, stream):
+    async def download_stream(self, name, stream, chunk_size=DEFAULT_STREAM_CHUNK_SIZE):
         async with self._make_streaming_request(
             'GET',
             f'/{self.bucket_name}/{name}',
             payload_digest=_empty_payload_digest,
         ) as response:
             content_length = response.headers.get('content-length')
             if content_length is not None:
                 content_length = int(content_length)
 
             try:
                 stream.truncate(content_length)
-                async for chunk in response.aiter_bytes(128_000):
+                async for chunk in response.aiter_bytes(chunk_size):
                     stream.write(chunk)
             except:
                 stream.seek(0)
                 raise
 
     @backoff_on_httperror
     async def _list_objects(self, *, continuation_token=None, prefix=''):
```

### Comparing `replicat-1.3.2/replicat/repository.py` & `replicat-1.4.0/replicat/repository.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,11 @@
+from __future__ import annotations
+
 import asyncio
+import bisect
 import collections.abc
 import concurrent.futures
 import dataclasses
 import inspect
 import io
 import json
 import logging
@@ -10,89 +13,113 @@
 import os.path
 import posixpath
 import queue
 import re
 import sys
 import threading
 import time
-from collections import defaultdict, namedtuple
+from collections import defaultdict
 from concurrent.futures import ThreadPoolExecutor
 from contextlib import asynccontextmanager, contextmanager
-from datetime import datetime
+from datetime import datetime, timezone
 from decimal import Decimal
 from functools import cached_property
 from pathlib import Path
-from typing import Any, Dict, Optional
+from typing import Any, ByteString, Dict, Iterator, List, NamedTuple, Optional, Tuple
 
 from sty import ef, fg
 from tqdm import tqdm
 from tqdm.utils import CallbackIOWrapper
 
 from . import exceptions, utils
-from .utils.adapters import (
-    ChunkerAdapter,
-    CipherAdapter,
-    HashAdapter,
-    KDFAdapter,
-    MACAdapter,
-)
+from .backends.base import DEFAULT_STREAM_CHUNK_SIZE
+from .utils import FileListColumn, SnapshotListColumn, adapters
 from .utils.compat import Random
+from .utils.config import DEFAULT_CACHE_DIRECTORY
+from .utils.fs import flatten_paths
 
 logger = logging.getLogger(__name__)
-LocationParts = namedtuple('LocationParts', ['name', 'tag'])
 
 
-@dataclasses.dataclass(frozen=True)
-class _SnapshotChunk:
+class LocationParts(NamedTuple):
+    name: str
+    tag: str
+
+
+# dataclasses are hilariously slow when all you need is an
+# immutable typed thing with __init__ and attribute access
+class _SnapshotChunk(NamedTuple):
     contents: bytes
     index: int
     location: str
     stream_start: int
     stream_end: int
     counter: int
 
 
+@dataclasses.dataclass
+class _SnapshotFile:
+    path: str
+    stream_start: int
+    stream_end: int
+    metadata: Optional[Dict[str, Any]] = None
+    digest: Optional[bytes] = None
+
+
+@dataclasses.dataclass
+class _SnapshotState:
+    bytes_with_padding: int = 0
+    bytes_chunked: int = 0
+    bytes_reused: int = 0
+    chunk_counter: int = 0
+    current_file: Optional[_SnapshotFile] = None
+    files: List[Tuple[int, _SnapshotFile]] = dataclasses.field(default_factory=list)
+
+
 @dataclasses.dataclass(repr=False, frozen=True)
 class RepositoryProps:
-    chunker: ChunkerAdapter
-    hasher: HashAdapter
-    cipher: Optional[CipherAdapter] = None
+    chunker: adapters.ChunkerAdapter
+    hasher: adapters.HashAdapter
+    cipher: Optional[adapters.CipherAdapter] = None
     userkey: Optional[bytes] = None
-    authenticator: Optional[MACAdapter] = None
-    shared_kdf: Optional[KDFAdapter] = None
+    authenticator: Optional[adapters.MACAdapter] = None
+    shared_kdf: Optional[adapters.KDFAdapter] = None
     private: Optional[Dict[str, Any]] = None
 
     @cached_property
-    def encrypted(self):
+    def encrypted(self) -> bool:
         return self.cipher is not None
 
-    def hash_digest(self, data):
+    def hash_digest(self, data: bytes) -> bytes:
         return self.hasher.digest(data)
 
-    def encrypt(self, data, key):
+    def incremental_hasher(self) -> adapters.IncrementalHasher:
+        return self.hasher.incremental_hasher()
+
+    def encrypt(self, data: bytes, key: bytes) -> bytes:
         assert self.encrypted
         return self.cipher.encrypt(data, key)
 
-    def decrypt(self, data, key):
+    def decrypt(self, data: bytes, key: bytes) -> bytes:
         assert self.encrypted
         return self.cipher.decrypt(data, key)
 
-    def mac(self, data):
+    def mac(self, data: bytes) -> bytes:
         assert self.encrypted
         return self.authenticator.mac(data, params=self.private['mac_params'])
 
-    def derive_shared_subkey(self, ctx):
+    def derive_shared_subkey(self, ctx: bytes) -> bytes:
         assert self.encrypted
         return self.shared_kdf.derive(
             self.private['shared_key'],
             context=ctx,
             params=self.private['shared_kdf_params'],
         )
 
-    def chunkify(self, it):
+    def chunkify(self, it: Iterator[ByteString]) -> Iterator[bytes]:
         params = self.private['chunker_params'] if self.encrypted else None
         return self.chunker(it, params=params)
 
 
 class Repository:
     # NOTE: trailing slashes
     CHUNK_PREFIX = 'data/'
@@ -102,29 +129,47 @@
     DEFAULT_CIPHER_NAME = 'aes_gcm'
     DEFAULT_HASHER_NAME = 'blake2b'
     DEFAULT_MAC_NAME = 'blake2b'
     DEFAULT_USER_KDF_NAME = 'scrypt'
     # Fast KDF for high-entropy inputs (used for shared data)
     DEFAULT_SHARED_KDF_NAME = 'blake2b'
     EMPTY_TABLE_VALUE = '--'
-    DEFAULT_CACHE_DIRECTORY = utils.fs.DEFAULT_CACHE_DIRECTORY
+    DEFAULT_CACHE_DIRECTORY = DEFAULT_CACHE_DIRECTORY
+    SNAPSHOT_LIST_COLUMN_LABELS = {
+        SnapshotListColumn.NAME: 'name',
+        SnapshotListColumn.NOTE: 'note',
+        SnapshotListColumn.TIMESTAMP: 'timestamp (utc)',
+        SnapshotListColumn.FILE_COUNT: 'files',
+        SnapshotListColumn.SIZE: 'size',
+    }
+    FILE_LIST_COLUMN_LABELS = {
+        FileListColumn.SNAPSHOT_NAME: 'snapshot name',
+        FileListColumn.SNAPSHOT_DATE: 'snapshot date',
+        FileListColumn.PATH: 'path',
+        FileListColumn.CHUNK_COUNT: 'chunks',
+        FileListColumn.SIZE: 'size',
+        FileListColumn.DIGEST: 'digest',
+        FileListColumn.ATIME: 'accessed at',
+        FileListColumn.MTIME: 'modified at',
+        FileListColumn.CTIME: 'created at',
+    }
 
     def __init__(
         self,
         backend,
         *,
         concurrent,
         quiet=True,
         cache_directory=DEFAULT_CACHE_DIRECTORY,
     ):
         self._concurrent = concurrent
         self._quiet = quiet
         self._cache_directory = cache_directory
 
-        self._slots = asyncio.Queue(maxsize=concurrent)
+        self._slots = asyncio.PriorityQueue(maxsize=concurrent)
         # We need actual integers for TQDM slot management in CLI, but this queue
         # can also act as a semaphore in the general case. Note that numbering starts
         # from 2, leaving two topmost slots to non-slotable trackers
         for slot in range(2, concurrent + 2):
             self._slots.put_nowait(slot)
 
         self.backend = backend
@@ -283,14 +328,17 @@
 
         if not isinstance(result, collections.abc.AsyncIterable):
             result = utils.async_gen_wrapper(result)
 
         async for value in result:
             yield value
 
+    def _compile_or_none(self, pattern):
+        return re.compile(pattern) if pattern is not None else None
+
     def default_serialization_hook(self, data, /):
         return utils.type_hint(data)
 
     def serialize(self, object, /):
         string = json.dumps(
             object, separators=(',', ':'), default=self.default_serialization_hook
         )
@@ -327,16 +375,15 @@
         return LocationParts(name=name, tag=parts[1] + parts[2] + parts[3])
 
     def _chunk_digest_to_location_parts(self, digest, /):
         if self.props.encrypted:
             digest_mac = self.props.mac(digest)
             digest_mac_mac = self.props.mac(digest_mac)
         else:
-            digest_mac = digest
-            digest_mac_mac = digest
+            digest_mac = digest_mac_mac = digest
 
         return LocationParts(name=digest_mac.hex(), tag=digest_mac_mac.hex())
 
     def _chunk_digest_to_location(self, digest):
         name, tag = self._chunk_digest_to_location_parts(digest)
         return self.get_chunk_location(name=name, tag=tag)
 
@@ -416,39 +463,39 @@
             settings = {}
 
         config = {}
 
         # Hashing
         hashing_settings = settings.get('hashing', {})
         hashing_settings.setdefault('name', self.DEFAULT_HASHER_NAME)
-        hasher_type, hasher_args = utils.adapter_from_config(**hashing_settings)
+        hasher_type, hasher_args = adapters.from_config(**hashing_settings)
         config['hashing'] = dict(hasher_args, name=hasher_type.__name__)
 
         # Deduplication params
         chunking_settings = settings.get('chunking', {})
         chunking_settings.setdefault('name', self.DEFAULT_CHUNKER_NAME)
-        chunker_type, chunker_args = utils.adapter_from_config(**chunking_settings)
+        chunker_type, chunker_args = adapters.from_config(**chunking_settings)
         config['chunking'] = dict(chunker_args, name=chunker_type.__name__)
 
         if (encryption_settings := settings.get('encryption', {})) is not None:
             cipher_settings = encryption_settings.get('cipher', {})
             cipher_settings.setdefault('name', self.DEFAULT_CIPHER_NAME)
-            cipher_type, cipher_args = utils.adapter_from_config(**cipher_settings)
+            cipher_type, cipher_args = adapters.from_config(**cipher_settings)
             config['encryption'] = {
                 'cipher': dict(cipher_args, name=cipher_type.__name__)
             }
 
         return config
 
     def _instantiate_config(self, config):
-        chunker_type, chunker_args = utils.adapter_from_config(**config['chunking'])
-        hasher_type, hasher_args = utils.adapter_from_config(**config['hashing'])
+        chunker_type, chunker_args = adapters.from_config(**config['chunking'])
+        hasher_type, hasher_args = adapters.from_config(**config['hashing'])
 
         if (encryption_config := config.get('encryption')) is not None:
-            cipher_type, cipher_args = utils.adapter_from_config(
+            cipher_type, cipher_args = adapters.from_config(
                 **encryption_config['cipher']
             )
             cipher = cipher_type(**cipher_args)
         else:
             cipher = None
 
         return {
@@ -461,32 +508,32 @@
         if settings is None:
             settings = {}
 
         encryption_settings = settings.get('encryption', {})
         # KDF for user personal data
         user_kdf_settings = encryption_settings.get('kdf', {})
         user_kdf_settings.setdefault('name', self.DEFAULT_USER_KDF_NAME)
-        user_kdf_type, user_kdf_args = utils.adapter_from_config(
+        user_kdf_type, user_kdf_args = adapters.from_config(
             **user_kdf_settings, length=cipher.key_bytes
         )
         user_kdf = user_kdf_type(**user_kdf_args)
 
         if private is None:
             # KDF for shared data
             shared_kdf_settings = encryption_settings.get('shared_kdf', {})
             shared_kdf_settings.setdefault('name', self.DEFAULT_SHARED_KDF_NAME)
-            shared_kdf_type, shared_args = utils.adapter_from_config(
+            shared_kdf_type, shared_args = adapters.from_config(
                 **shared_kdf_settings, length=cipher.key_bytes
             )
             shared_kdf = shared_kdf_type(**shared_args)
 
             # Message authentication
             mac_settings = encryption_settings.get('mac', {})
             mac_settings.setdefault('name', self.DEFAULT_MAC_NAME)
-            mac_type, mac_args = utils.adapter_from_config(**mac_settings)
+            mac_type, mac_args = adapters.from_config(**mac_settings)
             mac = mac_type(**mac_args)
 
             private = {
                 'shared_key': cipher.generate_key(),
                 'shared_kdf': dict(shared_args, name=shared_kdf_type.__name__),
                 'shared_kdf_params': shared_kdf.generate_derivation_params(),
                 'mac': dict(mac_args, name=mac_type.__name__),
@@ -498,31 +545,27 @@
             'kdf': dict(user_kdf_args, name=user_kdf_type.__name__),
             'kdf_params': user_kdf.generate_derivation_params(),
             'private': private,
         }
 
     def _instantiate_key(self, key, *, password, cipher):
         # User key derivation
-        kdf_type, kdf_args = utils.adapter_from_config(**key['kdf'])
+        kdf_type, kdf_args = adapters.from_config(**key['kdf'])
         userkey = kdf_type(**kdf_args).derive(password, params=key['kdf_params'])
 
         if isinstance(key['private'], bytes):
             # The 'private' portion of the key is still encrypted
             private = self.deserialize(cipher.decrypt(key['private'], userkey))
         else:
             private = key['private']
 
         # Message authentication
-        authenticator_type, authenticator_args = utils.adapter_from_config(
-            **private['mac']
-        )
+        authenticator_type, authenticator_args = adapters.from_config(**private['mac'])
         # KDF for shared data
-        shared_kdf_type, shared_kdf_args = utils.adapter_from_config(
-            **private['shared_kdf']
-        )
+        shared_kdf_type, shared_kdf_args = adapters.from_config(**private['shared_kdf'])
 
         return {
             'userkey': userkey,
             'authenticator': authenticator_type(**authenticator_args),
             'shared_kdf': shared_kdf_type(**shared_kdf_args),
             'private': private,
         }
@@ -605,15 +648,15 @@
             self.display_status('Unlocking repository')
             if password is None or key is None:
                 raise exceptions.ReplicatError(
                     'Both password and key are needed to unlock this repository'
                 )
 
             # TODO: Load keys from the backend as a fallback?
-            if isinstance(key, collections.abc.ByteString):
+            if isinstance(key, (str, collections.abc.ByteString)):
                 key = self.deserialize(key)
 
             props = dataclasses.replace(
                 props,
                 **self._instantiate_key(key, password=password, cipher=props.cipher),
             )
 
@@ -771,15 +814,15 @@
         # the second case should be rare, and to avoid potentially blocking unrelated
         # calls, but we still have to use slots to limit concurrent calls to the backend
         loader = ThreadPoolExecutor(
             max_workers=self._concurrent, thread_name_prefix='snapshot-loader'
         )
         future_to_path = {}
         loop = asyncio.get_running_loop()
-        snapshot_re = re.compile(snapshot_regex) if snapshot_regex is not None else None
+        snapshot_re = self._compile_or_none(snapshot_regex)
 
         def _download_snapshot(path):
             name, tag = self.parse_snapshot_location(path)
             if snapshot_re is not None and snapshot_re.search(name) is None:
                 logger.info('Skipping %s (does not match the filter)', path)
                 return
 
@@ -803,15 +846,15 @@
         files = snapshot_data['files']
         ranges_it = (chunk['range'] for file in files for chunk in file['chunks'])
         return sum(r[1] - r[0] for r in ranges_it)
 
     def _extract_snapshot_note(self, snapshot_data):
         return snapshot_data.get('note')
 
-    def _extract_snapshot_files_count(self, snapshot_data):
+    def _extract_snapshot_file_count(self, snapshot_data):
         return len(snapshot_data['files'])
 
     def _extract_snapshot_utc_timestamp(self, snapshot_data):
         return datetime.fromisoformat(snapshot_data['utc_timestamp'])
 
     def _format_snapshot_name(self, *, path, chunks, data):
         return self.parse_snapshot_location(path).name
@@ -822,40 +865,50 @@
     def _format_snapshot_utc_timestamp(self, *, path, chunks, data):
         if data is None:
             return None
 
         dt = self._extract_snapshot_utc_timestamp(data)
         return dt.isoformat(sep=' ', timespec='seconds')
 
-    def _format_snapshot_files_count(self, *, path, chunks, data):
-        return data and self._extract_snapshot_files_count(data)
+    def _format_snapshot_file_count(self, *, path, chunks, data):
+        return data and self._extract_snapshot_file_count(data)
 
     def _format_snaphot_size(self, *, path, chunks, data):
         return data and utils.bytes_to_human(self._extract_snapshot_size(data))
 
-    async def list_snapshots(self, *, snapshot_regex=None):
+    async def list_snapshots(self, *, snapshot_regex=None, header=True, columns=None):
+        if columns is None:
+            columns = [
+                SnapshotListColumn.NAME,
+                SnapshotListColumn.NOTE,
+                SnapshotListColumn.TIMESTAMP,
+                SnapshotListColumn.FILE_COUNT,
+                SnapshotListColumn.SIZE,
+            ]
+
         columns_getters = {
-            'snapshot': self._format_snapshot_name,
-            'note': self._format_snapshot_note,
-            'timestamp (utc)': self._format_snapshot_utc_timestamp,
-            'files': self._format_snapshot_files_count,
-            'size': self._format_snaphot_size,
+            SnapshotListColumn.NAME: self._format_snapshot_name,
+            SnapshotListColumn.NOTE: self._format_snapshot_note,
+            SnapshotListColumn.TIMESTAMP: self._format_snapshot_utc_timestamp,
+            SnapshotListColumn.FILE_COUNT: self._format_snapshot_file_count,
+            SnapshotListColumn.SIZE: self._format_snaphot_size,
         }
         columns_widths = {}
         snapshots = []
 
         self.display_status('Loading snapshots')
         async for snapshot_path, snapshot_body in self._load_snapshots(
             snapshot_regex=snapshot_regex
         ):
             row = {}
             snapshot_chunks = snapshot_body['chunks']
             snapshot_data = snapshot_body['data']
 
-            for column, getter in columns_getters.items():
+            for column in columns:
+                getter = columns_getters[column]
                 value = getter(
                     path=snapshot_path,
                     chunks=snapshot_chunks,
                     data=snapshot_data,
                 )
                 value = str(value if value is not None else self.EMPTY_TABLE_VALUE)
                 row[column] = value
@@ -869,74 +922,133 @@
             snapshots.append((snapshot_timestamp, row))
 
         if not snapshots:
             return
 
         snapshots.sort(key=lambda x: x[0] or '', reverse=True)
 
-        formatted_headers = []
-        for column in columns_widths:
-            width = columns_widths[column] = max(len(column), columns_widths[column])
-            formatted_headers.append(column.upper().center(width))
+        if header:
+            formatted_headers = []
+            for column, width in columns_widths.items():
+                label = self.SNAPSHOT_LIST_COLUMN_LABELS[column]
+                width = columns_widths[column] = max(len(label), columns_widths[column])
+                formatted_headers.append(label.upper().center(width))
+
+            print(*formatted_headers, sep='\t')
 
-        print(*formatted_headers, sep='\t')
         for _, row in snapshots:
             print(
                 *(value.ljust(columns_widths[col]) for col, value in row.items()),
                 sep='\t',
             )
 
+    def _format_file_snapshot_name(
+        self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
+    ):
+        return self.parse_snapshot_location(snapshot_path).name
+
     def _format_file_snapshot_date(
         self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
     ):
         dt = datetime.fromisoformat(snapshot_data['utc_timestamp'])
         return dt.isoformat(sep=' ', timespec='seconds')
 
     def _format_file_path(
         self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
     ):
         return file_data['path']
 
-    def _format_file_chunks_count(
+    def _format_file_chunk_count(
         self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
     ):
         return len(file_data['chunks'])
 
     def _format_file_size(
         self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
     ):
         ranges_it = (cd['range'] for cd in file_data['chunks'])
         return utils.bytes_to_human(sum(r[1] - r[0] for r in ranges_it))
 
-    async def list_files(self, *, snapshot_regex=None, files_regex=None):
+    def _format_file_digest(
+        self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
+    ):
+        return (digest := file_data.get('digest')) and digest.hex()
+
+    def _metadata_ts_to_dt(self, metadata, key):
+        try:
+            ts = metadata[key] / 1e9
+        except KeyError:
+            # NOTE: fall back to non-nanosecond timestamps for compatibility with
+            # snapshots that were created by older replicat versions (pre-1.3)
+            assert key.endswith('_ns'), key
+            ts = metadata[key[:-3]]
+
+        return datetime.fromtimestamp(ts, tz=timezone.utc).replace(tzinfo=None)
+
+    def _format_file_mtime(
+        self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
+    ):
+        dt = self._metadata_ts_to_dt(file_data['metadata'], 'st_mtime_ns')
+        return dt.isoformat(sep=' ', timespec='seconds')
+
+    def _format_file_ctime(
+        self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
+    ):
+        dt = self._metadata_ts_to_dt(file_data['metadata'], 'st_ctime_ns')
+        return dt.isoformat(sep=' ', timespec='seconds')
+
+    def _format_file_atime(
+        self, *, snapshot_path, snapshot_chunks, snapshot_data, file_data
+    ):
+        dt = self._metadata_ts_to_dt(file_data['metadata'], 'st_atime_ns')
+        return dt.isoformat(sep=' ', timespec='seconds')
+
+    async def list_files(
+        self, *, snapshot_regex=None, file_regex=None, header=True, columns=None
+    ):
+        if columns is None:
+            columns = [
+                FileListColumn.SNAPSHOT_DATE,
+                FileListColumn.PATH,
+                FileListColumn.CHUNK_COUNT,
+                FileListColumn.SIZE,
+                FileListColumn.MTIME,
+            ]
+
         columns_getters = {
-            'snapshot date': self._format_file_snapshot_date,
-            'path': self._format_file_path,
-            'chunks count': self._format_file_chunks_count,
-            'size': self._format_file_size,
+            FileListColumn.SNAPSHOT_NAME: self._format_file_snapshot_name,
+            FileListColumn.SNAPSHOT_DATE: self._format_file_snapshot_date,
+            FileListColumn.PATH: self._format_file_path,
+            FileListColumn.CHUNK_COUNT: self._format_file_chunk_count,
+            FileListColumn.SIZE: self._format_file_size,
+            FileListColumn.DIGEST: self._format_file_digest,
+            FileListColumn.ATIME: self._format_file_atime,
+            FileListColumn.MTIME: self._format_file_mtime,
+            FileListColumn.CTIME: self._format_file_ctime,
         }
         columns_widths = {}
         files = []
-        files_re = re.compile(files_regex) if files_regex is not None else None
+        file_re = self._compile_or_none(file_regex)
 
         self.display_status('Loading snapshots')
         async for snapshot_path, snapshot_body in self._load_snapshots(
             snapshot_regex=snapshot_regex
         ):
             snapshot_chunks = snapshot_body['chunks']
             snapshot_data = snapshot_body['data']
             if snapshot_data is None:
                 continue
 
             for file_data in snapshot_data['files']:
-                if files_re is not None and files_re.search(file_data['path']) is None:
+                if file_re is not None and file_re.search(file_data['path']) is None:
                     continue
 
                 row = {}
-                for column, getter in columns_getters.items():
+                for column in columns:
+                    getter = columns_getters[column]
                     value = getter(
                         snapshot_path=snapshot_path,
                         snapshot_chunks=snapshot_chunks,
                         snapshot_data=snapshot_data,
                         file_data=file_data,
                     )
                     value = str(value if value is not None else self.EMPTY_TABLE_VALUE)
@@ -948,146 +1060,136 @@
                 files.append((snapshot_data['utc_timestamp'], row))
 
         if not files:
             return
 
         files.sort(key=lambda x: x[0], reverse=True)
 
-        formatted_headers = []
-        for column in columns_widths:
-            width = columns_widths[column] = max(len(column), columns_widths[column])
-            formatted_headers.append(column.upper().center(width))
+        if header:
+            formatted_headers = []
+            for column, width in columns_widths.items():
+                label = self.FILE_LIST_COLUMN_LABELS[column]
+                width = columns_widths[column] = max(len(label), columns_widths[column])
+                formatted_headers.append(label.upper().center(width))
+
+            print(*formatted_headers, sep='\t')
 
-        print(*formatted_headers, sep='\t')
         for _, row in files:
             print(
                 *(value.ljust(columns_widths[col]) for col, value in row.items()),
                 sep='\t',
             )
 
-    def _flatten_paths(self, paths):
-        return list(utils.fs.flatten_paths(path.resolve(strict=True) for path in paths))
+    def _flatten_resolve_paths(self, paths):
+        return list(flatten_paths(path.resolve(strict=True) for path in paths))
 
     async def snapshot(self, *, paths, note=None, rate_limit=None):
         self.display_status('Collecting files')
-        files = self._flatten_paths(paths)
+        files = self._flatten_resolve_paths(paths)
         logger.info('Found %d files', len(files))
         # Small files are more likely to change than big files, read them quickly
         # and bundle them together
         files.sort(key=lambda file: (file.stat().st_size, str(file)))
 
-        state = utils.DefaultNamespace(
-            bytes_with_padding=0,
-            bytes_chunked=0,
-            bytes_reused=0,
-            chunk_counter=0,
-            # Preallocate this dictionary to avoid concurrent insertions
-            file_ranges=dict.fromkeys(files),
-            current_file=None,
-        )
-        chunks_table = {}
-        snapshot_files = {}
-        finished_files_metadata = {}
-        bytes_tracker = tqdm(
-            desc='Data processed',
-            unit='B',
-            unit_scale=True,
-            total=None,
-            position=0,
-            disable=self._quiet,
-            leave=True,
-        )
-        finished_tracker = tqdm(
-            desc='Files processed',
-            unit='',
-            total=len(files),
-            position=1,
-            disable=self._quiet,
-            leave=True,
-        )
         loop = asyncio.get_running_loop()
         chunk_queue = queue.Queue(maxsize=self._concurrent * 10)
         chunk_producer_executor = ThreadPoolExecutor(
             max_workers=1, thread_name_prefix='chunk-producer'
         )
-        rate_limiter = utils.RateLimiter(rate_limit) if rate_limit is not None else None
         abort = threading.Event()
 
+        if rate_limit is not None:
+            rate_limiter = utils.RateLimitedIO(rate_limit)
+            upload_chunk_size = max(rate_limit // (self._concurrent * 16), 1)
+        else:
+            rate_limiter = None
+            upload_chunk_size = DEFAULT_STREAM_CHUNK_SIZE
+
+        state = _SnapshotState()
+        chunks_table = {}
+        snapshot_files = {}
+
         def _chunk_done(chunk: _SnapshotChunk):
             finished_files_count = 0
+            bisect_point = bisect.bisect_left(state.files, (chunk.stream_end + 1,))
 
-            for file, ranges in state.file_ranges.items():
-                if ranges is None:
-                    continue
-
-                file_start, file_end = ranges
-                if file_start > chunk.stream_end or file_end < chunk.stream_start:
-                    continue
+            for index in range(bisect_point - 1, -1, -1):
+                _, file = state.files[index]
+                if file.stream_end < chunk.stream_start:
+                    break
 
                 try:
-                    file_data = snapshot_files[file]
+                    file_data = snapshot_files[file.path]
                 except KeyError:
-                    file_data = snapshot_files[file] = {
-                        'path': str(file.resolve()),
+                    file_data = snapshot_files[file.path] = {
+                        'path': file.path,
                         'chunks': [],
+                        'digest': None,
                         'metadata': None,
                     }
 
-                part_start = max(file_start - chunk.stream_start, 0)
-                part_end = min(file_end, chunk.stream_end) - chunk.stream_start
+                part_start = max(file.stream_start - chunk.stream_start, 0)
+                part_end = min(file.stream_end, chunk.stream_end) - chunk.stream_start
                 file_data['chunks'].append(
                     {
                         'range': [part_start, part_end],
                         'index': chunk.index,
                         'counter': chunk.counter,
                     }
                 )
 
-                if chunk.stream_end >= file_end:
-                    if (metadata := finished_files_metadata.get(file)) is not None:
-                        # File completed
-                        file_data['metadata'] = metadata
-                        logger.info('File %r fully processed', str(file))
-                        finished_files_count += 1
+                if chunk.stream_end >= file.stream_end and file.digest is not None:
+                    # File completed
+                    file_data['digest'] = file.digest
+                    file_data['metadata'] = file.metadata
+                    logger.info('File %r fully processed', file.path)
+                    finished_files_count += 1
 
             finished_tracker.update(finished_files_count)
             bytes_tracker.update(chunk.stream_end - chunk.stream_start)
 
         def _stream_files(chunk_size=16_777_216):
             for path in files:
-                # First chunk from this file
-                if state.current_file is not None:
+                if (prev_file := state.current_file) is not None:
                     # Produce padding for the previous file
                     # TODO: let the chunker generate the padding?
                     if alignment := self.props.chunker.alignment:
-                        cstart, cend = state.file_ranges[state.current_file]
-                        if padding_length := -(cend - cstart) % alignment:
+                        padding_length = (
+                            -(prev_file.stream_end - prev_file.stream_start) % alignment
+                        )
+                        if padding_length:
                             state.bytes_with_padding += padding_length
                             yield bytes(padding_length)
 
-                    logger.info('Finished streaming file %r', str(state.current_file))
+                    logger.info('Finished streaming file %r', prev_file.path)
 
                 logger.info('Started streaming file %r', str(path))
-                state.current_file = path
-                start = state.bytes_with_padding
 
-                with path.open('rb') as file:
-                    while True:
-                        chunk = file.read(chunk_size)
+                file = _SnapshotFile(
+                    path=str(path),
+                    stream_start=state.bytes_with_padding,
+                    stream_end=state.bytes_with_padding,
+                )
+                state.current_file = file
+                state.files.append((file.stream_start, file))
+                hasher = self.props.incremental_hasher()
+
+                with path.open('rb') as source_file:
+                    while chunk := source_file.read(chunk_size):
                         state.bytes_with_padding += len(chunk)
-                        state.file_ranges[path] = (start, state.bytes_with_padding)
+                        file.stream_end += len(chunk)
+                        hasher.feed(chunk)
                         yield chunk
-                        if len(chunk) < chunk_size:
-                            break
 
-                    finished_files_metadata[path] = self.read_metadata(file.fileno())
+                    file.digest = hasher.digest()
+                    file.metadata = self.read_metadata(source_file.fileno())
 
             if state.current_file is not None:
                 logger.info(
-                    'Finished streaming file %r, stopping', str(state.current_file)
+                    'Finished streaming file %r, stopping', state.current_file.path
                 )
 
         def _chunk_producer(queue_timeout=0.025):
             # Will run in a different thread, because most of these actions release GIL
             for output_chunk in self.props.chunkify(_stream_files()):
                 state.chunk_counter += 1
                 stream_start = state.bytes_chunked
@@ -1147,33 +1249,58 @@
                 if exists:
                     _chunk_done(chunk)
                     state.bytes_reused += chunk.stream_end - chunk.stream_start
                 else:
                     async with self._acquire_slot() as slot:
                         length = len(chunk.contents)
                         stream = io.BytesIO(chunk.contents)
-                        iowrapper = utils.TQDMIOReader(
-                            stream,
+
+                        if rate_limiter is not None:
+                            limited_wrapper = rate_limiter.wrap(stream)
+                        else:
+                            limited_wrapper = stream
+
+                        tqdm_wrapper = utils.TQDMIOReader(
+                            limited_wrapper,
                             desc=f'Chunk #{chunk.counter:06}',
                             total=length,
                             position=slot,
                             disable=self._quiet,
-                            rate_limiter=rate_limiter,
                         )
-                        with stream, iowrapper:
+                        with stream, limited_wrapper, tqdm_wrapper:
                             await self._maybe_run_in_executor(
                                 self.backend.upload_stream,
                                 chunk.location,
-                                iowrapper,
+                                tqdm_wrapper,
                                 length,
+                                upload_chunk_size,
                             )
 
                     _chunk_done(chunk)
 
         chunk_producer = loop.run_in_executor(chunk_producer_executor, _chunk_producer)
+
+        bytes_tracker = tqdm(
+            desc='Data processed',
+            unit='B',
+            unit_scale=True,
+            total=None,
+            position=0,
+            disable=self._quiet,
+            leave=True,
+        )
+        finished_tracker = tqdm(
+            desc='Files processed',
+            unit='',
+            total=len(files),
+            position=1,
+            disable=self._quiet,
+            leave=True,
+        )
+
         with finished_tracker, bytes_tracker:
             try:
                 await asyncio.gather(*(_worker() for _ in range(self._concurrent)))
             except:
                 abort.set()
                 raise
             finally:
@@ -1232,41 +1359,41 @@
 
         with file:
             file_end = file.seek(0, io.SEEK_END)
             file.truncate(max(file_end, offset + len(data)))
             file.seek(offset)
             file.write(data)
 
-    async def restore(self, *, snapshot_regex=None, files_regex=None, path=None):
+    async def restore(
+        self, *, snapshot_regex=None, file_regex=None, path=None, rate_limit=None
+    ):
         if path is None:
             path = Path()
 
         path = path.resolve()
         logger.info("Will restore files to %s", path)
 
         loop = asyncio.get_running_loop()
-        # We'll submit plain backend methods to this executor instead of the standard
-        # one. We still need to use slots to limit concurrent calls to the backend
         loader = ThreadPoolExecutor(
-            max_workers=self._concurrent, thread_name_prefix='chunk-loader'
+            max_workers=self._concurrent * 2, thread_name_prefix='chunk-loader'
         )
         writer = ThreadPoolExecutor(
-            max_workers=self._concurrent * 3, thread_name_prefix='file-writer'
+            max_workers=self._concurrent * 2, thread_name_prefix='file-writer'
         )
 
+        if rate_limit is not None:
+            rate_limiter = utils.RateLimitedIO(rate_limit)
+            download_chunk_size = max(rate_limit // (self._concurrent * 16), 1)
+        else:
+            rate_limiter = None
+            download_chunk_size = DEFAULT_STREAM_CHUNK_SIZE
+
         glock = threading.Lock()
         flocks = {}
         flocks_refcounts = {}
-        files_re = re.compile(files_regex) if files_regex is not None else None
-
-        chunks_references = defaultdict(list)
-        files_digests = {}
-        files_metadata = {}
-
-        total_bytes = 0
 
         def _write_chunk_ref(ref, contents):
             file_path, chunk_size, stream_start, start = ref
             restore_to, _ = files_metadata[file_path]
 
             with glock:
                 try:
@@ -1286,15 +1413,43 @@
                 bytes_tracker.update(chunk_size)
                 flocks_refcounts[restore_to] -= 1
                 if not flocks_refcounts[restore_to]:
                     del flocks_refcounts[restore_to], flocks[restore_to]
 
         def _download_chunk(digest, refs):
             location = self._chunk_digest_to_location(digest)
-            contents = self._download_threadsafe(location, loop=loop)
+            # TODO: async backend methods will naturally do the writing from the
+            # same (main) thread. This is suboptimal, even if we're more likely
+            # to be restricted by the bandwidth. Should we use async files/offload
+            # file IO to a dedicated executor?
+            stream = io.BytesIO()
+
+            if rate_limiter is not None:
+                limited_wrapper = rate_limiter.wrap(stream)
+            else:
+                limited_wrapper = stream
+
+            with self._acquire_slot_threadsafe(loop=loop) as slot:
+                logger.info('Downloading chunk %r', location)
+                tqdm_wrapper = utils.TQDMIOWriter(
+                    limited_wrapper,
+                    desc=location[:25],  # TODO: something even smarter?
+                    total=None,
+                    position=slot,
+                    disable=self._quiet,
+                )
+                with stream, limited_wrapper, tqdm_wrapper:
+                    self._maybe_run_coroutine_threadsafe(
+                        self.backend.download_stream,
+                        location,
+                        tqdm_wrapper,
+                        download_chunk_size,
+                        loop=loop,
+                    )
+                    contents = stream.getvalue()
 
             logger.info('Decrypting %s', location)
             if self.props.encrypted:
                 decrypted_contents = self.props.decrypt(
                     contents,
                     self.props.derive_shared_subkey(digest),
                 )
@@ -1325,29 +1480,36 @@
                     digests.remove(digest)
 
                 if not digests:
                     logger.info('Finished writing file %s', file_path)
                     with glock:
                         restore_path, metadata = files_metadata.pop(file_path)
                     self.restore_metadata(restore_path, metadata)
+                    finished_tracker.update()
 
         self.display_status('Loading snapshots')
         snapshots_gen = self._load_snapshots(snapshot_regex=snapshot_regex)
         snapshots = [x async for _, x in snapshots_gen if x['data'] is not None]
         snapshots.sort(key=lambda x: x['data']['utc_timestamp'], reverse=True)
 
+        file_re = self._compile_or_none(file_regex)
+        chunks_references = defaultdict(list)
+        files_digests = {}
+        files_metadata = {}
+        total_bytes = 0
+
         for snapshot_body in snapshots:
             snapshot_chunks = snapshot_body['chunks']
             snapshot_data = snapshot_body['data']
 
             for file_data in snapshot_data['files']:
                 if (file_path := file_data['path']) in files_digests:
                     continue
 
-                if files_re is not None and files_re.search(file_path) is None:
+                if file_re is not None and file_re.search(file_path) is None:
                     logger.info('Skipping %s (does not match the filter)', file_path)
                     continue
 
                 restore_to = Path(path, *Path(file_path).parts[1:]).resolve()
                 files_metadata[file_path] = (restore_to, file_data['metadata'])
                 digests = files_digests[file_path] = set()
 
@@ -1377,15 +1539,24 @@
             unit='B',
             unit_scale=True,
             total=total_bytes,
             position=0,
             disable=self._quiet,
             leave=True,
         )
-        with bytes_tracker:
+        finished_tracker = tqdm(
+            desc='Files restored',
+            unit='',
+            total=len(files_metadata),
+            position=1,
+            disable=self._quiet,
+            leave=True,
+        )
+
+        with finished_tracker, bytes_tracker:
             await asyncio.gather(
                 *(
                     loop.run_in_executor(loader, _download_chunk, *x)
                     for x in chunks_references.items()
                 )
             )
 
@@ -1393,19 +1564,19 @@
 
     def _format_snapshot_info_brief(self, snapshot_data):
         parts = []
         if (note := self._extract_snapshot_note(snapshot_data)) is not None:
             parts.append(note)
 
         dt = self._extract_snapshot_utc_timestamp(snapshot_data)
-        files_count = self._extract_snapshot_files_count(snapshot_data)
+        file_count = self._extract_snapshot_file_count(snapshot_data)
         size = self._extract_snapshot_size(snapshot_data)
         parts.append('from ' + dt.isoformat(sep=' ', timespec='seconds'))
         parts.append(
-            'with {} {}'.format(files_count, 'file' if files_count == 1 else 'files')
+            'with {} {}'.format(file_count, 'file' if file_count == 1 else 'files')
         )
         parts.append(utils.bytes_to_human(size))
         return ', '.join(parts)
 
     async def delete_snapshots(self, snapshots, /, *, confirm=True):
         # TODO: locking
         self.display_status('Loading snapshots')
@@ -1443,46 +1614,46 @@
             self.display_danger('\n'.join(danger_message_parts))
             if input('Proceed? [y/n] ').lower() != 'y':
                 logger.info('Aborting')
                 return
 
         chunks_to_delete.difference_update(chunks_to_keep)
 
+        async def _delete_snapshot(location):
+            await self._delete(location)
+            if self._cache_directory is not None:
+                self._delete_cached(location)
+            finished_snapshots_tracker.update()
+
+        async def _delete_chunk(digest):
+            location = self._chunk_digest_to_location(digest)
+            await self._delete(location)
+            finished_chunks_tracker.update()
+
         finished_snapshots_tracker = tqdm(
             desc='Snapshots deleted',
             unit='',
             total=len(snapshots_locations),
             position=0,
             disable=self._quiet,
             leave=True,
         )
 
-        async def _delete_snapshot(location):
-            await self._delete(location)
-            if self._cache_directory is not None:
-                self._delete_cached(location)
-            finished_snapshots_tracker.update()
-
         with finished_snapshots_tracker:
             await asyncio.gather(*map(_delete_snapshot, snapshots_locations))
 
         finished_chunks_tracker = tqdm(
             desc='Unreferenced chunks deleted',
             unit='',
             total=len(chunks_to_delete),
             position=0,
             disable=self._quiet,
             leave=True,
         )
 
-        async def _delete_chunk(digest):
-            location = self._chunk_digest_to_location(digest)
-            await self._delete(location)
-            finished_chunks_tracker.update()
-
         with finished_chunks_tracker:
             await asyncio.gather(*map(_delete_chunk, chunks_to_delete))
 
     async def clean(self):
         # TODO: locking
         self.display_status('Loading snapshots')
         referenced_digests = {
@@ -1507,27 +1678,27 @@
                     continue
 
             to_delete.add(location)
 
         if not to_delete:
             return
 
+        async def _delete_chunk(location):
+            await self._delete(location)
+            finished_tracker.update()
+
         finished_tracker = tqdm(
             desc='Unreferenced chunks deleted',
             unit='',
             total=len(to_delete),
             position=0,
             disable=self._quiet,
             leave=True,
         )
 
-        async def _delete_chunk(location):
-            await self._delete(location)
-            finished_tracker.update()
-
         with finished_tracker:
             await asyncio.gather(*map(_delete_chunk, to_delete))
 
         self.display_status('Running post-deletion cleanup')
         await self._clean()
 
     @utils.disable_gc
@@ -1557,38 +1728,89 @@
         )
 
     async def benchmark(self, name, settings=None):
         logger.info('Using provided settings: %r', settings)
         if settings is None:
             settings = {}
 
-        adapter_type, adapter_args = utils.adapter_from_config(name=name, **settings)
+        adapter_type, adapter_args = adapters.from_config(name=name, **settings)
         adapter = adapter_type(**adapter_args)
         argument_string = ', '.join(
             f'{name}={value!r}' for name, value in adapter_args.items()
         )
         self.display_status(f'Benchmarking {name}({argument_string})')
         benchmarker = ThreadPoolExecutor(
             max_workers=1, thread_name_prefix='benchmarker'
         )
 
-        if isinstance(adapter, ChunkerAdapter):
+        if isinstance(adapter, adapters.ChunkerAdapter):
             loop = asyncio.get_running_loop()
             await loop.run_in_executor(benchmarker, self._benchmark_chunker, adapter)
         else:
             raise RuntimeError('Sorry, not yet')
 
     async def upload_objects(self, paths, *, rate_limit=None, skip_existing=False):
         self.display_status('Collecting files')
-        files = self._flatten_paths(paths)
+        files = self._flatten_resolve_paths(paths)
+        logger.info('Found %d files to upload', len(files))
         if not files:
-            logger.info('No files found, nothing to do')
             return
+
+        working_directory = Path.cwd()
+
+        if rate_limit is not None:
+            rate_limiter = utils.RateLimitedIO(rate_limit)
+            upload_chunk_size = max(rate_limit // (self._concurrent * 16), 1)
         else:
-            logger.info('Found %d files', len(files))
+            rate_limiter = None
+            upload_chunk_size = DEFAULT_STREAM_CHUNK_SIZE
+
+        async def _upload_file(path):
+            name = path.relative_to(
+                os.path.commonpath([path, working_directory])
+            ).as_posix()
+
+            if skip_existing and await self._exists(name):
+                logger.info('Skipping file %r (exists)', name)
+            else:
+                async with self._acquire_slot() as slot:
+                    logger.info('Uploading file %r', name)
+                    # TODO: async backend methods will naturally do the reading from the
+                    # same (main) thread. This is suboptimal, even if we're more likely
+                    # to be restricted by the bandwidth. Should we use async files/offload
+                    # file IO to a dedicated executor?
+                    stream = path.open('rb')
+                    length = os.fstat(stream.fileno()).st_size
+
+                    if rate_limiter is not None:
+                        limited_wrapper = rate_limiter.wrap(stream)
+                    else:
+                        limited_wrapper = stream
+
+                    callback_wrapper = CallbackIOWrapper(
+                        bytes_tracker.update, limited_wrapper, 'read'
+                    )
+                    tqdm_wrapper = utils.TQDMIOReader(
+                        callback_wrapper,
+                        desc=name,
+                        total=length,
+                        position=slot,
+                        disable=self._quiet,
+                    )
+
+                    with stream, limited_wrapper, tqdm_wrapper:
+                        await self._maybe_run_in_executor(
+                            self.backend.upload_stream,
+                            name,
+                            tqdm_wrapper,
+                            length,
+                            upload_chunk_size,
+                        )
+
+            finished_tracker.update()
 
         bytes_tracker = tqdm(
             desc='Data uploaded',
             unit='B',
             unit_scale=True,
             total=None,
             position=0,
@@ -1599,52 +1821,14 @@
             desc='Files processed',
             unit='',
             total=len(files),
             position=1,
             disable=self._quiet,
             leave=True,
         )
-        base_directory = Path.cwd()
-        rate_limiter = utils.RateLimiter(rate_limit) if rate_limit is not None else None
-
-        async def _upload_file(path):
-            name = path.relative_to(
-                os.path.commonpath([path, base_directory])
-            ).as_posix()
-
-            if skip_existing and await self._exists(name):
-                logger.info('Skipping file %r (exists)', name)
-            else:
-                async with self._acquire_slot() as slot:
-                    logger.info('Uploading file %r', name)
-                    # TODO: async backend methods will naturally do the reading from the
-                    # same (main) thread. This is suboptimal, even if we're more likely
-                    # to be restricted by the bandwidth. Should we use async files/offload
-                    # file IO to a dedicated executor?
-                    with path.open('rb') as stream:
-                        length = os.fstat(stream.fileno()).st_size
-                        callback_wrapper = CallbackIOWrapper(
-                            bytes_tracker.update, stream, 'read'
-                        )
-                        with utils.TQDMIOReader(
-                            callback_wrapper,
-                            desc=name,
-                            total=length,
-                            position=slot,
-                            disable=self._quiet,
-                            rate_limiter=rate_limiter,
-                        ) as iowrapper:
-                            await self._maybe_run_in_executor(
-                                self.backend.upload_stream,
-                                name,
-                                iowrapper,
-                                length,
-                            )
-
-            finished_tracker.update()
 
         with finished_tracker, bytes_tracker:
             await asyncio.gather(*map(_upload_file, files))
 
         return utils.DefaultNamespace(files=files)
 
     async def download_objects(
@@ -1652,136 +1836,149 @@
         *,
         path=None,
         object_prefix='',
         object_regex=None,
         rate_limit=None,
         skip_existing=False,
     ):
-        base_directory = path if path is not None else Path.cwd()
-        object_re = re.compile(object_regex) if object_regex is not None else None
-        rate_limiter = utils.RateLimiter(rate_limit) if rate_limit is not None else None
-        write_mode = 'xb' if skip_existing else 'wb'
+        self.display_status('Loading object list')
+        object_re = self._compile_or_none(object_regex)
         objects = []
 
-        self.display_status('Loading object list')
         async for object_path in self._aiter(self.backend.list_files, object_prefix):
             if object_re is not None and object_re.search(object_path) is None:
                 logger.info('Skipping %s (does not match the filter)', object_path)
                 continue
 
             objects.append(object_path)
 
+        logger.info('Found %d objects to download', len(objects))
         if not objects:
-            logger.info('No objects selected, nothing to do')
             return
-        else:
-            logger.info('Found %d objects', len(objects))
 
-        bytes_tracker = tqdm(
-            desc='Data downloaded',
-            unit='B',
-            unit_scale=True,
-            total=None,
-            position=0,
-            disable=self._quiet,
-            leave=True,
-        )
-        finished_tracker = tqdm(
-            desc='Objects processed',
-            unit='',
-            total=len(objects),
-            position=1,
-            disable=self._quiet,
-            leave=True,
-        )
+        base_directory = path if path is not None else Path.cwd()
+        write_mode = 'xb' if skip_existing else 'wb'
+
+        if rate_limit is not None:
+            rate_limiter = utils.RateLimitedIO(rate_limit)
+            download_chunk_size = max(rate_limit // (self._concurrent * 16), 1)
+        else:
+            rate_limiter = None
+            download_chunk_size = DEFAULT_STREAM_CHUNK_SIZE
 
         async def _download_object(object_path):
             output_path = base_directory / object_path
 
             async with self._acquire_slot() as slot:
                 output_path.parent.mkdir(parents=True, exist_ok=True)
                 try:
-                    write_stream = output_path.open(write_mode)
+                    stream = output_path.open(write_mode)
                 except FileExistsError:
                     logger.info('Skipping object %r (file exists)', output_path)
                 else:
                     logger.info('Downloading object %r', object_path)
                     # TODO: async backend methods will naturally do the writing from the
                     # same (main) thread. This is suboptimal, even if we're more likely
                     # to be restricted by the bandwidth. Should we use async files/offload
                     # file IO to a dedicated executor?
-                    with write_stream:
-                        callback_wrapper = CallbackIOWrapper(
-                            bytes_tracker.update, write_stream, 'write'
+                    if rate_limiter is not None:
+                        limited_wrapper = rate_limiter.wrap(stream)
+                    else:
+                        limited_wrapper = stream
+
+                    callback_wrapper = CallbackIOWrapper(
+                        bytes_tracker.update, limited_wrapper, 'write'
+                    )
+                    tqdm_wrapper = utils.TQDMIOWriter(
+                        callback_wrapper,
+                        desc=object_path[:25],  # TODO: something even smarter?
+                        total=None,
+                        position=slot,
+                        disable=self._quiet,
+                    )
+
+                    with stream, limited_wrapper, tqdm_wrapper:
+                        await self._maybe_run_in_executor(
+                            self.backend.download_stream,
+                            object_path,
+                            tqdm_wrapper,
+                            download_chunk_size,
                         )
-                        with utils.TQDMIOWriter(
-                            callback_wrapper,
-                            desc=object_path[:25],  # TODO: something even smarter?
-                            total=None,
-                            position=slot,
-                            disable=self._quiet,
-                            rate_limiter=rate_limiter,
-                        ) as iowrapper:
-                            await self._maybe_run_in_executor(
-                                self.backend.download_stream, object_path, iowrapper
-                            )
 
             finished_tracker.update()
 
+        bytes_tracker = tqdm(
+            desc='Data downloaded',
+            unit='B',
+            unit_scale=True,
+            total=None,
+            position=0,
+            disable=self._quiet,
+            leave=True,
+        )
+        finished_tracker = tqdm(
+            desc='Objects processed',
+            unit='',
+            total=len(objects),
+            position=1,
+            disable=self._quiet,
+            leave=True,
+        )
+
         with finished_tracker, bytes_tracker:
             await asyncio.gather(*map(_download_object, objects))
 
         return utils.DefaultNamespace(objects=objects)
 
     async def list_objects(
         self,
         *,
         object_prefix='',
         object_regex=None,
     ):
-        object_re = re.compile(object_regex) if object_regex is not None else None
+        object_re = self._compile_or_none(object_regex)
         paths = []
 
         self.display_status('Loading object list')
         async for object_path in self._aiter(self.backend.list_files, object_prefix):
             if object_re is not None and object_re.search(object_path) is None:
                 logger.info('Skipping %s (does not match the filter)', object_path)
                 continue
 
             paths.append(object_path)
             print(object_path)
 
         return utils.DefaultNamespace(paths=paths)
 
-    async def delete_objects(self, objects_paths, /, *, confirm=True):
+    async def delete_objects(self, object_paths, /, *, confirm=True):
         if confirm:
             message_parts = ['The following objects will be deleted:']
-            message_parts.extend(f'    {x}' for x in objects_paths)
+            message_parts.extend(f'    {x}' for x in object_paths)
             self.display_danger('\n'.join(message_parts))
             if input('Proceed? [y/n] ').lower() != 'y':
                 logger.info('Aborting')
                 return
 
+        async def _delete_object(location):
+            await self._delete(location)
+            if self._cache_directory is not None:
+                self._delete_cached(location)
+            deleted_objects_tracker.update()
+
         deleted_objects_tracker = tqdm(
             desc='Objects deleted',
             unit='',
-            total=len(objects_paths),
+            total=len(object_paths),
             position=0,
             disable=self._quiet,
             leave=True,
         )
 
-        async def _delete_object(location):
-            await self._delete(location)
-            if self._cache_directory is not None:
-                self._delete_cached(location)
-            deleted_objects_tracker.update()
-
         with deleted_objects_tracker:
-            await asyncio.gather(*map(_delete_object, objects_paths))
+            await asyncio.gather(*map(_delete_object, object_paths))
 
     async def close(self):
         try:
             del self.props
         except AttributeError:
             pass
```

### Comparing `replicat-1.3.2/replicat/tests/test_local.py` & `replicat-1.4.0/replicat/tests/test_local.py`

 * *Files identical despite different names*

### Comparing `replicat-1.3.2/replicat/tests/test_repository.py` & `replicat-1.4.0/replicat/tests/test_repository.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import os
 import re
 import threading
 import time
-from unittest.mock import ANY, call, patch
+from unittest.mock import ANY, MagicMock, call, patch
 
 import pytest
 
 from replicat import exceptions
 from replicat.backends.local import Local
 from replicat.repository import Repository
 from replicat.utils import adapters
@@ -386,70 +386,79 @@
             file.write_bytes(data)
 
         result = await local_repo.snapshot(
             paths=list(file_contents),
             note='<associated note>',
         )
 
+        # Check that it was successfully uploaded
         snapshots = list(local_backend.list_files('snapshots'))
         assert snapshots == [result.location]
 
+        # Check that it was correctly encrypted and serialized
         encrypted_body = local_repo.deserialize(local_backend.download(result.location))
         assert encrypted_body.keys() == {'chunks', 'data'}
         assert result.chunks == local_repo.deserialize(
             local_repo.props.decrypt(
                 encrypted_body['chunks'],
                 local_repo.props.derive_shared_subkey(
                     local_repo.props.hash_digest(encrypted_body['data'])
                 ),
             )
         )
         assert result.data == local_repo.deserialize(
             local_repo.props.decrypt(encrypted_body['data'], local_repo.props.userkey)
         )
 
+        # Check the table of (padded) chunks, both order and digests
         expected_order = sorted(
             file_contents.items(), key=lambda x: (len(x[1]), x[0].name)
         )
-        # Add padding
-        stream = []
-        for _, data in expected_order[:-1]:
-            stream.append(data + bytes(-len(data) % 4))
+        stream = [data + bytes(-len(data) % 4) for _, data in expected_order[:-1]]
         stream.append(expected_order[-1][1])
 
-        expected_digests_it = map(
+        expected_chunk_digests_it = map(
             local_repo.props.hash_digest, local_repo.props.chunkify(stream)
         )
-        # Check the insertion order
-        assert result.chunks == list(dict.fromkeys(expected_digests_it))
-
-        assert result.data['note'] == '<associated note>'
+        assert result.chunks == list(dict.fromkeys(expected_chunk_digests_it))
 
+        # Check that the files were added correctly
         snapshot_files = result.data['files']
         assert len(file_contents) == len(snapshot_files)
-
         snapshot_files.sort(key=lambda x: x['path'])
-        restored_files = []
+        original_digests = [
+            local_repo.props.hash_digest(x) for x in file_contents.values()
+        ]
+        snapshot_digests = [x['digest'] for x in snapshot_files]
+        assert snapshot_digests == original_digests
+
+        # Check that the original files can be reconstructed from the snapshot
+        reconstructed_files = []
 
         for file_data in snapshot_files:
             contents = b''
             file_chunks = sorted(file_data['chunks'], key=lambda x: x['counter'])
 
             for chunk_data in file_chunks:
-                digest = result.chunks[chunk_data['index']]
-                chunk_location = local_repo._chunk_digest_to_location(digest)
+                chunk_digest = result.chunks[chunk_data['index']]
+                chunk_location = local_repo._chunk_digest_to_location(chunk_digest)
                 chunk_bytes = local_repo.props.decrypt(
                     local_backend.download(chunk_location),
-                    local_repo.props.derive_shared_subkey(digest),
+                    local_repo.props.derive_shared_subkey(chunk_digest),
                 )
                 contents += chunk_bytes[chunk_data['range'][0] : chunk_data['range'][1]]
 
-            restored_files.append(contents)
+            reconstructed_files.append(contents)
 
-        assert restored_files == [data for _, data in sorted(file_contents.items())]
+        assert reconstructed_files == [
+            data for _, data in sorted(file_contents.items())
+        ]
+
+        # Check the associated information
+        assert result.data['note'] == '<associated note>'
 
     @pytest.mark.asyncio
     async def test_unencrypted_data(self, local_backend, local_repo, tmp_path):
         await local_repo.init(
             settings={
                 'encryption': None,
                 'chunking': {
@@ -482,63 +491,73 @@
             file.write_bytes(data)
 
         result = await local_repo.snapshot(
             paths=list(file_contents),
             note='<associated note>',
         )
 
+        # Check that it was successfully uploaded
         snapshots = list(local_backend.list_files('snapshots'))
         snapshot_location = local_repo.get_snapshot_location(
             name=result.name, tag=result.tag
         )
         assert snapshots == [snapshot_location]
 
+        # Check that it was correctly serialized
         snapshot_body = local_repo.deserialize(
             local_backend.download(snapshot_location)
         )
         assert snapshot_body.keys() == {'chunks', 'data'}
         assert result.chunks == snapshot_body['chunks']
         assert result.data == snapshot_body['data']
 
+        # Check the table of (padded) chunks, both order and digests
         expected_order = sorted(
             file_contents.items(), key=lambda x: (len(x[1]), x[0].name)
         )
-        # Add padding
-        stream = []
-        for _, data in expected_order[:-1]:
-            stream.append(data + bytes(-len(data) % 4))
+        stream = [data + bytes(-len(data) % 4) for _, data in expected_order[:-1]]
         stream.append(expected_order[-1][1])
 
         expected_digests_it = map(
             local_repo.props.hash_digest, local_repo.props.chunkify(stream)
         )
         # Check the insertion order
         assert result.chunks == list(dict.fromkeys(expected_digests_it))
 
-        assert result.data['note'] == '<associated note>'
-
+        # Check that the files were added correctly
         snapshot_files = result.data['files']
         assert len(file_contents) == len(snapshot_files)
-
         snapshot_files.sort(key=lambda x: x['path'])
-        restored_files = []
+        original_digests = [
+            local_repo.props.hash_digest(x) for x in file_contents.values()
+        ]
+        snapshot_digests = [x['digest'] for x in snapshot_files]
+        assert snapshot_digests == original_digests
+
+        # Check that the original files can be reconstructed from the snapshot
+        reconstructed_files = []
 
         for snapshot_data in snapshot_files:
             contents = b''
             file_chunks = sorted(snapshot_data['chunks'], key=lambda x: x['counter'])
 
             for chunk_data in file_chunks:
                 digest = result.chunks[chunk_data['index']]
                 chunk_location = local_repo._chunk_digest_to_location(digest)
                 chunk_bytes = local_backend.download(chunk_location)
                 contents += chunk_bytes[chunk_data['range'][0] : chunk_data['range'][1]]
 
-            restored_files.append(contents)
+            reconstructed_files.append(contents)
 
-        assert restored_files == [data for _, data in sorted(file_contents.items())]
+        assert reconstructed_files == [
+            data for _, data in sorted(file_contents.items())
+        ]
+
+        # Check the associated information
+        assert result.data['note'] == '<associated note>'
 
     @pytest.mark.asyncio
     async def test_encrypted_deduplicated_references(self, local_repo, tmp_path):
         await local_repo.init(
             password=b'<password>',
             settings={
                 'encryption': {'kdf': {'n': 4}},
@@ -623,35 +642,111 @@
         data = Random(0).randbytes(1_024)
         file = tmp_path / 'file'
         file.write_bytes(data)
 
         upload_lock = threading.Lock()
         bytes_consumed = 0
 
-        def upldstream(name, contents, length):
+        def upldstream(name, contents, length, chunk_size):
             nonlocal bytes_consumed
             with upload_lock:
                 bytes_consumed += length
                 bytes_remaining = len(data) - bytes_consumed
 
             try:
-                return Local.upload_stream(local_backend, name, contents, length)
+                return Local.upload_stream(
+                    local_backend, name, contents, length, chunk_size
+                )
             finally:
                 if not bytes_remaining:
                     # Simulate work
                     time.sleep(0.5)
 
         with patch.object(local_backend, 'upload') as upload_mock, patch.object(
             local_backend, 'upload_stream', side_effect=upldstream
         ) as upload_stream_mock:
             result = await local_repo.snapshot(paths=[file])
 
         upload_mock.assert_called_once_with(result.location, ANY)
         assert upload_stream_mock.call_count == len(result.data['files'][0]['chunks'])
 
+    @pytest.mark.asyncio
+    async def test_streams_without_rate_limit(
+        self, local_backend, local_repo, tmp_path
+    ):
+        await local_repo.init(
+            settings={
+                'encryption': None,
+                'chunking': {
+                    'min_length': 256,
+                    'max_length': 256,
+                },
+            }
+        )
+
+        data = Random(0).randbytes(3 * 256)
+        file = tmp_path / 'file'
+        file.write_bytes(data)
+
+        with patch.object(local_backend, 'upload_stream') as upload_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.utils.TQDMIOReader') as tqdm_mock:
+                    await local_repo.snapshot(paths=[file])
+
+        rate_limited_io_mock.assert_not_called()
+        assert tqdm_mock.call_count == 3
+        assert upload_stream_mock.call_count == 3
+        upload_stream_mock.assert_has_calls(
+            3 * [call(ANY, tqdm_mock.return_value, 256, ANY)]
+        )
+
+    @pytest.mark.asyncio
+    async def test_streams_with_rate_limit(self, local_backend, local_repo, tmp_path):
+        await local_repo.init(
+            settings={
+                'encryption': None,
+                'chunking': {
+                    'min_length': 256,
+                    'max_length': 256,
+                },
+            }
+        )
+
+        data = Random(0).randbytes(3 * 256)
+        file = tmp_path / 'file'
+        file.write_bytes(data)
+
+        with patch.object(local_backend, 'upload_stream') as upload_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.utils.TQDMIOReader') as tqdm_mock:
+                    await local_repo.snapshot(paths=[file], rate_limit=12345)
+
+        rate_limited_io_mock.assert_called_once_with(12345)
+        wrap_mock = rate_limited_io_mock.return_value.wrap
+        assert wrap_mock.call_count == 3
+        assert tqdm_mock.call_count == 3
+        tqdm_mock.assert_has_calls(
+            3
+            * [
+                call(
+                    wrap_mock.return_value,
+                    desc=ANY,
+                    total=256,
+                    position=ANY,
+                    disable=ANY,
+                ),
+            ],
+            any_order=True,
+        )
+
+        assert upload_stream_mock.call_count == 3
+        upload_stream_mock.assert_has_calls(
+            3 * [call(ANY, tqdm_mock.return_value, 256, ANY)]
+        )
+
 
 class TestRestore:
     @pytest.mark.asyncio
     async def test_encrypted_data(self, local_repo, tmp_path):
         await local_repo.init(
             password=b'<password>',
             settings={
@@ -770,15 +865,15 @@
         await local_repo.snapshot(paths=[file])
 
         second_version = rnd.randbytes(4_096)
         file.write_bytes(second_version)
         await local_repo.snapshot(paths=[file])
 
         result = await local_repo.restore(
-            files_regex=re.escape(str(file)), path=tmp_path
+            file_regex=re.escape(str(file)), path=tmp_path
         )
         assert result.files == [str(file)]
         assert tmp_path.joinpath(*file.parts[1:]).read_bytes() == second_version
 
     @pytest.mark.asyncio
     async def test_specific_snapshot_version(self, local_repo, tmp_path):
         await local_repo.init(
@@ -801,14 +896,112 @@
 
         result = await local_repo.restore(
             snapshot_regex=first_snapshot.name, path=tmp_path
         )
         assert result.files == [str(file)]
         assert tmp_path.joinpath(*file.parts[1:]).read_bytes() == first_version
 
+    @pytest.mark.asyncio
+    async def test_streams_without_rate_limit(
+        self, local_backend, local_repo, tmp_path
+    ):
+        await local_repo.init(
+            settings={
+                'encryption': None,
+                'chunking': {
+                    'min_length': 256,
+                    'max_length': 256,
+                },
+            }
+        )
+
+        data = Random(0).randbytes(3 * 256)
+        file = tmp_path / 'file'
+        file.write_bytes(data)
+        await local_repo.snapshot(paths=[file])
+
+        tqdm_mocked = []
+
+        def _tqdm_side_effect(stream, **_):
+            mock = MagicMock(write=stream.write)
+            tqdm_mocked.append(mock)
+            return mock
+
+        with patch.object(
+            local_backend, 'download_stream', side_effect=local_backend.download_stream
+        ) as download_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch(
+                    'replicat.utils.TQDMIOWriter',
+                    side_effect=_tqdm_side_effect,
+                ) as tqdm_mock:
+                    await local_repo.restore(path=tmp_path)
+
+        rate_limited_io_mock.assert_not_called()
+        assert tqdm_mock.call_count == 3
+        assert download_stream_mock.call_count == 3
+        download_stream_mock.assert_has_calls(
+            [call(ANY, x, ANY) for x in tqdm_mocked], any_order=True
+        )
+
+    @pytest.mark.asyncio
+    async def test_streams_with_rate_limit(self, local_backend, local_repo, tmp_path):
+        await local_repo.init(
+            settings={
+                'encryption': None,
+                'chunking': {
+                    'min_length': 256,
+                    'max_length': 256,
+                },
+            }
+        )
+
+        data = Random(0).randbytes(3 * 256)
+        file = tmp_path / 'file'
+        file.write_bytes(data)
+        await local_repo.snapshot(paths=[file])
+
+        wrap_mocked = []
+        tqdm_mocked = []
+
+        def _wrap_mocked(stream):
+            mock = MagicMock(write=stream.write)
+            wrap_mocked.append(mock)
+            return mock
+
+        def _tqdm_side_effect(stream, **_):
+            mock = MagicMock(write=stream.write)
+            tqdm_mocked.append(mock)
+            return mock
+
+        with patch.object(
+            local_backend, 'download_stream', side_effect=local_backend.download_stream
+        ) as download_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                rate_limited_io_mock.return_value.wrap.side_effect = _wrap_mocked
+                with patch(
+                    'replicat.utils.TQDMIOWriter', side_effect=_tqdm_side_effect
+                ) as tqdm_mock:
+                    await local_repo.restore(path=tmp_path, rate_limit=12345)
+
+        rate_limited_io_mock.assert_called_once_with(12345)
+        assert rate_limited_io_mock.return_value.wrap.call_count == 3
+        assert tqdm_mock.call_count == 3
+        tqdm_mock.assert_has_calls(
+            [
+                call(x, desc=ANY, total=ANY, position=ANY, disable=ANY)
+                for x in wrap_mocked
+            ],
+            any_order=True,
+        )
+        assert download_stream_mock.call_count == 3
+        download_stream_mock.assert_has_calls(
+            [call(ANY, x, ANY) for x in tqdm_mocked], any_order=True
+        )
+
 
 class TestDeleteSnapshots:
     @pytest.mark.asyncio
     async def test_encrypted_referenced_independent_key(
         self, local_backend, local_repo, tmp_path
     ):
         file = tmp_path / 'file'
@@ -1291,14 +1484,121 @@
 
         repository = Repository(backend, concurrent=5)
 
         await repository.upload_objects([files_base_path / 'file'], skip_existing=True)
         assert set(backend.list_files()) == {'files/file'}
         assert backend.download('files/file') == b'<old data>'
 
+    @pytest.mark.asyncio
+    async def test_streams_without_rate_limit(
+        self, local_backend, local_repo, tmp_path
+    ):
+        await local_repo.init(settings={'encryption': None})
+
+        data = Random(0).randbytes(128)
+        first_file = tmp_path / 'first_file'
+        first_file.write_bytes(data * 2)
+        second_file = tmp_path / 'second_file'
+        second_file.write_bytes(data * 3)
+
+        with patch.object(local_backend, 'upload_stream') as upload_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.repository.CallbackIOWrapper') as callback_wrapper:
+                    with patch('replicat.utils.TQDMIOReader') as tqdm_mock:
+                        await local_repo.upload_objects(paths=[first_file, second_file])
+
+        rate_limited_io_mock.assert_not_called()
+        assert callback_wrapper.call_count == 2
+        assert tqdm_mock.call_count == 2
+        tqdm_mock.assert_has_calls(
+            [
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=256,
+                    position=ANY,
+                    disable=ANY,
+                ),
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=384,
+                    position=ANY,
+                    disable=ANY,
+                ),
+            ],
+            any_order=True,
+        )
+
+        assert upload_stream_mock.call_count == 2
+        upload_stream_mock.assert_has_calls(
+            [
+                call(ANY, tqdm_mock.return_value, 256, ANY),
+                call(ANY, tqdm_mock.return_value, 384, ANY),
+            ],
+            any_order=True,
+        )
+
+    @pytest.mark.asyncio
+    async def test_streams_with_rate_limit(self, local_backend, local_repo, tmp_path):
+        await local_repo.init(settings={'encryption': None})
+
+        data = Random(0).randbytes(128)
+        first_file = tmp_path / 'first_file'
+        first_file.write_bytes(data * 3)
+        second_file = tmp_path / 'second_file'
+        second_file.write_bytes(data * 4)
+
+        with patch.object(local_backend, 'upload_stream') as upload_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.repository.CallbackIOWrapper') as callback_wrapper:
+                    with patch('replicat.utils.TQDMIOReader') as tqdm_mock:
+                        await local_repo.upload_objects(
+                            paths=[first_file, second_file], rate_limit=12345
+                        )
+
+        rate_limited_io_mock.assert_called_once_with(12345)
+        wrap_mock = rate_limited_io_mock.return_value.wrap
+        assert wrap_mock.call_count == 2
+        assert callback_wrapper.call_count == 2
+        callback_wrapper.assert_has_calls(
+            2 * [call(ANY, wrap_mock.return_value, 'read')],
+            any_order=True,
+        )
+
+        assert tqdm_mock.call_count == 2
+        tqdm_mock.assert_has_calls(
+            [
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=384,
+                    position=ANY,
+                    disable=ANY,
+                ),
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=512,
+                    position=ANY,
+                    disable=ANY,
+                ),
+            ],
+            any_order=True,
+        )
+
+        assert upload_stream_mock.call_count == 2
+        upload_stream_mock.assert_has_calls(
+            [
+                call(ANY, tqdm_mock.return_value, 384, ANY),
+                call(ANY, tqdm_mock.return_value, 512, ANY),
+            ],
+            any_order=True,
+        )
+
 
 class TestDownloadObjects:
     @pytest.fixture(autouse=True)
     def populate_backend(self, local_backend):
         local_backend.upload('file', b'<backend data>')
         local_backend.upload('nested/file', b'<nested backend data>')
         local_backend.upload(
@@ -1342,14 +1642,93 @@
         target_path = tmp_path / 'downloaded_files'
         await local_repo.download_objects(path=target_path, object_regex='^very|^file')
         assert {x for x in target_path.rglob('*') if x.is_file()} == {
             target_path / 'file',
             target_path / 'very/very/nested/file',
         }
 
+    @pytest.mark.asyncio
+    async def test_streams_without_rate_limit(
+        self, local_backend, local_repo, tmp_path
+    ):
+        await local_repo.init(settings={'encryption': None})
+
+        with patch.object(local_backend, 'download_stream') as download_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.repository.CallbackIOWrapper') as callback_wrapper:
+                    with patch('replicat.utils.TQDMIOWriter') as tqdm_mock:
+                        await local_repo.download_objects(
+                            path=tmp_path,
+                            object_regex='file',
+                        )
+
+        rate_limited_io_mock.assert_not_called()
+        assert callback_wrapper.call_count == 3
+        assert tqdm_mock.call_count == 3
+        tqdm_mock.assert_has_calls(
+            3
+            * [
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=ANY,
+                    position=ANY,
+                    disable=ANY,
+                ),
+            ],
+            any_order=True,
+        )
+
+        assert download_stream_mock.call_count == 3
+        download_stream_mock.assert_has_calls(
+            3 * [call(ANY, tqdm_mock.return_value, ANY)],
+            any_order=True,
+        )
+
+    @pytest.mark.asyncio
+    async def test_streams_with_rate_limit(self, local_backend, local_repo, tmp_path):
+        await local_repo.init(settings={'encryption': None})
+
+        with patch.object(local_backend, 'download_stream') as download_stream_mock:
+            with patch('replicat.utils.RateLimitedIO') as rate_limited_io_mock:
+                with patch('replicat.repository.CallbackIOWrapper') as callback_wrapper:
+                    with patch('replicat.utils.TQDMIOWriter') as tqdm_mock:
+                        await local_repo.download_objects(
+                            path=tmp_path, object_regex='file', rate_limit=12345
+                        )
+
+        rate_limited_io_mock.assert_called_once_with(12345)
+        wrap_mock = rate_limited_io_mock.return_value.wrap
+        assert wrap_mock.call_count == 3
+        assert callback_wrapper.call_count == 3
+        callback_wrapper.assert_has_calls(
+            3 * [call(ANY, wrap_mock.return_value, 'write')],
+            any_order=True,
+        )
+
+        assert tqdm_mock.call_count == 3
+        tqdm_mock.assert_has_calls(
+            3
+            * [
+                call(
+                    callback_wrapper.return_value,
+                    desc=ANY,
+                    total=ANY,
+                    position=ANY,
+                    disable=ANY,
+                ),
+            ],
+            any_order=True,
+        )
+        assert download_stream_mock.call_count == 3
+        download_stream_mock.assert_has_calls(
+            3 * [call(ANY, tqdm_mock.return_value, ANY)],
+            any_order=True,
+        )
+
 
 class TestListObjects:
     @pytest.fixture(autouse=True)
     def populate_backend(self, local_backend):
         local_backend.upload('file', b'<backend data>')
         local_backend.upload('nested/file', b'<nested backend data>')
         local_backend.upload(
```

### Comparing `replicat-1.3.2/replicat/utils/adapters.py` & `replicat-1.4.0/replicat/utils/adapters.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,19 +1,16 @@
 from __future__ import annotations
 
 import hashlib
+import inspect
 import os
 from abc import ABC, abstractmethod
 from collections.abc import ByteString, Iterator
 from typing import Optional
 
-import cryptography.exceptions
-from cryptography.hazmat.primitives.ciphers import aead
-from cryptography.hazmat.primitives.kdf.scrypt import Scrypt
-
 import _replicat_adapters
 from .. import exceptions
 
 
 class CipherAdapter(ABC):
     @abstractmethod
     def encrypt(self, data: bytes, key: bytes) -> bytes:
@@ -58,20 +55,34 @@
 
     @abstractmethod
     def mac(self, message: bytes, *, params: bytes) -> bytes:
         """Generate MAC using the provided params (key)"""
         return b''
 
 
+class IncrementalHasher(ABC):
+    @abstractmethod
+    def feed(self, data: bytes) -> None:
+        return None
+
+    @abstractmethod
+    def digest(self) -> bytes:
+        return b''
+
+
 class HashAdapter(ABC):
     @abstractmethod
     def digest(self, data: bytes) -> bytes:
         """Compute the hash digest from data"""
         return b''
 
+    @abstractmethod
+    def incremental_hasher(self) -> IncrementalHasher:
+        raise NotImplementedError
+
 
 class ChunkerAdapter(ABC):
     @property
     @abstractmethod
     def alignment(self) -> Optional[int]:
         """Return the alignment"""
         return 0
@@ -83,66 +94,89 @@
 
     @abstractmethod
     def __call__(
         self,
         chunk_iterator: Iterator[ByteString],
         *,
         params: Optional[ByteString] = None,
-    ):
+    ) -> Iterator[bytes]:
         """Re-chunk the incoming stream of bytes using the provided params"""
         yield b''
 
 
+class HashlibIncrementalHasher(IncrementalHasher):
+    def __init__(self, hash_instance):
+        self.instance = hash_instance
+
+    def feed(self, data: bytes) -> None:
+        self.instance.update(data)
+
+    def digest(self) -> bytes:
+        return self.instance.digest()
+
+
 class AEADCipherAdapterMixin(CipherAdapter):
-    cipher = None
+    aead_cipher_name = None
 
     def __init__(self):
         self._key_bytes, self._nonce_bytes = self.key_bits // 8, self.nonce_bits // 8
 
+    @property
+    def cipher_class(self):
+        from cryptography.hazmat.primitives.ciphers import aead
+
+        return getattr(aead, self.aead_cipher_name)
+
     def encrypt(self, data, key):
-        cipher = self.cipher(key)
+        cipher = self.cipher_class(key)
         nonce = os.urandom(self._nonce_bytes)
         return nonce + cipher.encrypt(nonce, data, None)
 
     def decrypt(self, data, key):
-        cipher = self.cipher(key)
+        from cryptography.exceptions import InvalidTag
+
         nonce, ciphertext = data[: self._nonce_bytes], data[self._nonce_bytes :]
+        cipher = self.cipher_class(key)
         try:
             return cipher.decrypt(nonce, ciphertext, None)
-        except cryptography.exceptions.InvalidTag as e:
+        except InvalidTag as e:
             raise exceptions.DecryptionError from e
 
     @property
     def key_bytes(self):
         return self._key_bytes
 
 
 class aes_gcm(AEADCipherAdapterMixin):
-    cipher = aead.AESGCM
+    aead_cipher_name = 'AESGCM'
 
     def __init__(self, *, key_bits=256, nonce_bits=96):
+        if key_bits not in (128, 192, 256):
+            raise ValueError('Invalid key size')
         self.key_bits, self.nonce_bits = key_bits, nonce_bits
         super().__init__()
 
 
 class chacha20_poly1305(AEADCipherAdapterMixin):
-    cipher = aead.ChaCha20Poly1305
+    aead_cipher_name = 'ChaCha20Poly1305'
     key_bits = 256
     nonce_bits = 96
 
 
 class scrypt(KDFAdapter):
-    def __init__(self, *, length, n=1 << 22, r=8, p=1):
+    def __init__(self, *, length, n=1 << 20, r=8, p=1):
         self.length, self.n, self.r, self.p = length, n, r, p
 
     def generate_derivation_params(self):
         salt = os.urandom(self.length)
         return salt
 
     def derive(self, pwd, *, params, context=None):
+        from cryptography.hazmat.primitives.kdf.scrypt import Scrypt
+
         if context is None:
             context = b''
 
         # If we used hashlib's scrypt, we'd need to take care of maxmem limits
         # ourselves, plus they are small
         instance = Scrypt(
             n=self.n,
@@ -178,17 +212,45 @@
         return hashlib.blake2b(
             message, digest_size=self.digest_size, key=params
         ).digest()
 
     def digest(self, data):
         return hashlib.blake2b(data, digest_size=self.digest_size).digest()
 
+    def incremental_hasher(self):
+        return HashlibIncrementalHasher(hashlib.blake2b(digest_size=self.digest_size))
+
+
+class sha2(HashAdapter):
+    def __init__(self, *, bits=512):
+        if bits not in (224, 256, 384, 512):
+            raise ValueError('Invalid digest size')
+        self._hasher_class = getattr(hashlib, f'sha{bits}')
+
+    def digest(self, data):
+        return self._hasher_class(data).digest()
+
+    def incremental_hasher(self):
+        return HashlibIncrementalHasher(self._hasher_class())
 
-class gclmulchunker(ChunkerAdapter):
 
+class sha3(HashAdapter):
+    def __init__(self, *, bits=512):
+        if bits not in (224, 256, 384, 512):
+            raise ValueError('Invalid digest size')
+        self._hasher_class = getattr(hashlib, f'sha3_{bits}')
+
+    def digest(self, data):
+        return self._hasher_class(data).digest()
+
+    def incremental_hasher(self):
+        return HashlibIncrementalHasher(self._hasher_class())
+
+
+class gclmulchunker(ChunkerAdapter):
     # Chunk lengths in bytes
     MIN_LENGTH = 128_000
     MAX_LENGTH = 5_120_000
     alignment = 4
 
     def __init__(self, *, min_length=MIN_LENGTH, max_length=MAX_LENGTH):
         if min_length > max_length:
@@ -225,7 +287,39 @@
                 yield bytes(buffer[:pos])
                 del buffer[:pos]
 
             chunk = next_chunk
 
     def generate_chunking_params(self):
         return os.urandom(16)
+
+
+_adapters = [
+    aes_gcm,
+    chacha20_poly1305,
+    scrypt,
+    blake2b,
+    sha2,
+    sha3,
+    gclmulchunker,
+]
+_adapters_mapping = {a.__name__: a for a in _adapters}
+
+
+def from_config(name, **kwargs):
+    try:
+        adapter_type = _adapters_mapping[name]
+    except KeyError:
+        raise LookupError(f'Unrecognized adapter {name!r}') from None
+
+    signature = inspect.signature(adapter_type)
+
+    try:
+        bound_args = signature.bind(**kwargs)
+    except TypeError as e:
+        raise exceptions.ReplicatError(
+            f'Invalid configuration for adapter {name}'
+        ) from e
+
+    bound_args.apply_defaults()
+    adapter_args = bound_args.arguments
+    return adapter_type, adapter_args
```

### Comparing `replicat-1.3.2/replicat.egg-info/SOURCES.txt` & `replicat-1.4.0/replicat.egg-info/SOURCES.txt`

 * *Files 7% similar despite different names*

```diff
@@ -24,10 +24,12 @@
 replicat/tests/conftest.py
 replicat/tests/test_adapters.py
 replicat/tests/test_local.py
 replicat/tests/test_repository.py
 replicat/tests/test_utils.py
 replicat/utils/__init__.py
 replicat/utils/adapters.py
+replicat/utils/cli.py
 replicat/utils/compat.py
+replicat/utils/config.py
 replicat/utils/fs.py
 src/adapters.cpp
```

### Comparing `replicat-1.3.2/setup.py` & `replicat-1.4.0/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -77,30 +77,34 @@
 
 extras_require = {'test': ['pytest', 'pytest-asyncio<0.17']}
 extras_require['all'] = [y for x in extras_require.values() for y in x]
 
 setup(
     name='replicat',
     version=get_version(),
-    url="https://github.com/vaultah/replicat",
+    url='https://github.com/vaultah/replicat',
+    project_urls={
+        'Source': 'https://github.com/vaultah/replicat',
+    },
     maintainer='vaultah',
     maintainer_email='flwaultah+replicat@gmail.com',
-    python_requires=">=3.8",
+    python_requires='>=3.8',
     description='Configurable and lightweight backup utility with '
     'deduplication and encryption.',
     long_description=get_long_description(),
-    long_description_content_type="text/markdown",
+    long_description_content_type='text/markdown',
     packages=find_namespace_packages(include=['replicat', 'replicat.*']),
     install_requires=[
-        'httpx',
-        'cryptography',
-        'backoff',
-        'appdirs',
-        'tqdm',
-        'sty',
+        'httpx>=0.22,<1',
+        'cryptography>=35',
+        'backoff>=2,<3',
+        'appdirs>=1.4.4,<1.5',
+        'tqdm>=4.63,<5',
+        'sty>=1,<1.1',
+        'tomli >= 1.1.0 ; python_version < "3.11"',
     ],
     extras_require=extras_require,
     ext_modules=[CMakeExtension('_replicat_adapters')],
     cmdclass={'build_ext': CMakeBuild},
     entry_points={
         'console_scripts': ['replicat = replicat.__main__:main'],
     },
```

### Comparing `replicat-1.3.2/src/adapters.cpp` & `replicat-1.4.0/src/adapters.cpp`

 * *Files identical despite different names*

