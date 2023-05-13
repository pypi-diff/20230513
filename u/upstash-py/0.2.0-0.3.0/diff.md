# Comparing `tmp/upstash_py-0.2.0.tar.gz` & `tmp/upstash_py-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "upstash_py-0.2.0.tar", max compression
+gzip compressed data, was "upstash_py-0.3.0.tar", max compression
```

## Comparing `upstash_py-0.2.0.tar` & `upstash_py-0.3.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0       37 2023-03-04 10:43:41.243570 upstash_py-0.2.0/README.md
--rw-r--r--   0        0        0      379 2023-05-11 14:14:38.035799 upstash_py-0.2.0/pyproject.toml
--rw-r--r--   0        0        0        0 2023-03-04 11:23:56.540070 upstash_py-0.2.0/upstash_py/__init__.py
--rw-r--r--   0        0        0    83393 2023-05-11 14:06:26.783008 upstash_py-0.2.0/upstash_py/client.py
--rw-r--r--   0        0        0      308 2023-05-11 14:05:49.019292 upstash_py-0.2.0/upstash_py/config.py
--rw-r--r--   0        0        0       44 2023-03-08 07:44:02.265644 upstash_py-0.2.0/upstash_py/exception.py
--rw-r--r--   0        0        0      755 2023-05-04 15:53:00.952164 upstash_py-0.2.0/upstash_py/http/decode.py
--rw-r--r--   0        0        0     1629 2023-04-13 15:37:48.050511 upstash_py-0.2.0/upstash_py/http/execute.py
--rw-r--r--   0        0        0     1030 2023-05-04 15:39:39.039487 upstash_py-0.2.0/upstash_py/play.py
--rw-r--r--   0        0        0      115 2023-05-03 17:44:20.513271 upstash_py-0.2.0/upstash_py/play2.py
--rw-r--r--   0        0        0      409 2023-04-14 12:17:17.899972 upstash_py-0.2.0/upstash_py/schema/commands/parameters.py
--rw-r--r--   0        0        0      932 2023-04-14 14:37:49.938942 upstash_py-0.2.0/upstash_py/schema/commands/returns.py
--rw-r--r--   0        0        0      761 2023-04-13 15:35:06.241703 upstash_py-0.2.0/upstash_py/schema/http.py
--rw-r--r--   0        0        0      107 2023-04-13 16:18:51.335437 upstash_py-0.2.0/upstash_py/utils/base.py
--rw-r--r--   0        0        0      242 2023-04-14 14:58:16.064260 upstash_py-0.2.0/upstash_py/utils/comparison.py
--rw-r--r--   0        0        0     3333 2023-05-04 07:39:00.163434 upstash_py-0.2.0/upstash_py/utils/exception.py
--rw-r--r--   0        0        0     4088 2023-05-04 15:26:27.420397 upstash_py-0.2.0/upstash_py/utils/format.py
--rw-r--r--   0        0        0      461 1970-01-01 00:00:00.000000 upstash_py-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0       37 2023-03-04 10:43:41.243570 upstash_py-0.3.0/README.md
+-rw-r--r--   0        0        0      379 2023-05-13 16:15:09.549732 upstash_py-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-03-04 11:23:56.540070 upstash_py-0.3.0/upstash_py/__init__.py
+-rw-r--r--   0        0        0    83443 2023-05-13 15:26:15.134417 upstash_py-0.3.0/upstash_py/client.py
+-rw-r--r--   0        0        0      308 2023-05-13 15:46:08.357723 upstash_py-0.3.0/upstash_py/config.py
+-rw-r--r--   0        0        0       44 2023-03-08 07:44:02.265644 upstash_py-0.3.0/upstash_py/exception.py
+-rw-r--r--   0        0        0      755 2023-05-04 15:53:00.952164 upstash_py-0.3.0/upstash_py/http/decode.py
+-rw-r--r--   0        0        0     1887 2023-05-13 15:33:46.517564 upstash_py-0.3.0/upstash_py/http/execute.py
+-rw-r--r--   0        0        0     1030 2023-05-04 15:39:39.039487 upstash_py-0.3.0/upstash_py/play.py
+-rw-r--r--   0        0        0       75 2023-05-13 15:44:19.293211 upstash_py-0.3.0/upstash_py/play2.py
+-rw-r--r--   0        0        0      409 2023-04-14 12:17:17.899972 upstash_py-0.3.0/upstash_py/schema/commands/parameters.py
+-rw-r--r--   0        0        0     1119 2023-05-13 16:00:21.639249 upstash_py-0.3.0/upstash_py/schema/commands/returns.py
+-rw-r--r--   0        0        0      761 2023-04-13 15:35:06.241703 upstash_py-0.3.0/upstash_py/schema/http.py
+-rw-r--r--   0        0        0      107 2023-04-13 16:18:51.335437 upstash_py-0.3.0/upstash_py/utils/base.py
+-rw-r--r--   0        0        0      242 2023-04-14 14:58:16.064260 upstash_py-0.3.0/upstash_py/utils/comparison.py
+-rw-r--r--   0        0        0     3333 2023-05-04 07:39:00.163434 upstash_py-0.3.0/upstash_py/utils/exception.py
+-rw-r--r--   0        0        0     4088 2023-05-04 15:26:27.420397 upstash_py-0.3.0/upstash_py/utils/format.py
+-rw-r--r--   0        0        0      461 1970-01-01 00:00:00.000000 upstash_py-0.3.0/PKG-INFO
```

### Comparing `upstash_py-0.2.0/upstash_py/client.py` & `upstash_py-0.3.0/upstash_py/client.py`

 * *Files 0% similar despite different names*

```diff
@@ -112,15 +112,16 @@
         return await execute(
             session=self._session,
             url=self.url,
             token=self.token,
             encoding=self.rest_encoding,
             retries=self.rest_retries,
             retry_interval=self.rest_retry_interval,
-            command=command
+            command=command,
+            allow_telemetry=self.allow_telemetry
         )
 
     async def bitcount(self, key: str, start: int | None = None, end: int | None = None) -> int:
         """
         See https://redis.io/commands/bitcount
         """
```

### Comparing `upstash_py-0.2.0/upstash_py/http/decode.py` & `upstash_py-0.3.0/upstash_py/http/decode.py`

 * *Files identical despite different names*

### Comparing `upstash_py-0.2.0/upstash_py/http/execute.py` & `upstash_py-0.3.0/upstash_py/http/execute.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,25 @@
 from upstash_py.exception import UpstashException
 from upstash_py.http.decode import decode
 from upstash_py.schema.http import RESTResult, RESTResponse, RESTEncoding
 from asyncio import sleep
 from aiohttp import ClientSession
 from json import dumps
+from platform import python_version
 
 
 async def execute(
     session: ClientSession,
     url: str,
     token: str,
     encoding: RESTEncoding,
     retries: int,
     retry_interval: int,
-    command: list
+    command: list,
+    allow_telemetry: bool
 ) -> RESTResult:
     """
     Execute the given command over the REST API.
     """
 
     # Serialize the command; more specifically, write string-incompatible types as JSON strings.
     command = [
@@ -28,14 +30,18 @@
         for element in command
     ]
 
     for i in range(retries + 1):
         try:
             headers: dict[str, str] = {"Authorization": f'Bearer {token}'}
 
+            if allow_telemetry:
+                headers["Upstash-Telemetry-Runtime"] = f'python@v.{python_version()}'
+                headers["Upstash-Telemetry-Sdk"] = "upstash_py@development"
+
             if encoding:
                 headers["Upstash-Encoding"] = encoding
 
             async with session.post(url, headers=headers, json=command) as response:
                 body: RESTResponse[RESTResult] = await response.json()
                 # Avoid the [] syntax to prevent KeyError from being raised.
                 if body.get("error"):
```

### Comparing `upstash_py-0.2.0/upstash_py/play.py` & `upstash_py-0.3.0/upstash_py/play.py`

 * *Files identical despite different names*

### Comparing `upstash_py-0.2.0/upstash_py/schema/commands/returns.py` & `upstash_py-0.3.0/upstash_py/schema/commands/returns.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,16 @@
 """
 The raw output returned by some Geo commands, usually the ones that return properties of members.
+
 If no additional properties are requested, the output is a list of strings, each string representing a member.
+
+If coordinates are requested, each member's properties will be represented by a list (the result itself being a list),
+where the coordinates themselves will be another one.
 """
-GeoMembersReturn = list[str | list[str]]
+GeoMembersReturn = list[str | list[str | list[str]]]
 
 """
 The output resulted by formatting "GeoMembersReturn".
 
 Note that this might differ from the "GeoMember" type that represents the initial properties of a geo member.
 """
 FormattedGeoMembersReturn = list[dict[str, str | float | int]]
```

### Comparing `upstash_py-0.2.0/upstash_py/schema/http.py` & `upstash_py-0.3.0/upstash_py/schema/http.py`

 * *Files identical despite different names*

### Comparing `upstash_py-0.2.0/upstash_py/utils/exception.py` & `upstash_py-0.3.0/upstash_py/utils/exception.py`

 * *Files identical despite different names*

### Comparing `upstash_py-0.2.0/upstash_py/utils/format.py` & `upstash_py-0.3.0/upstash_py/utils/format.py`

 * *Files identical despite different names*

