# Comparing `tmp/pysml-0.0.8.tar.gz` & `tmp/pysml-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pysml-0.0.8.tar", max compression
+gzip compressed data, was "pysml-0.0.9.tar", max compression
```

## Comparing `pysml-0.0.8.tar` & `pysml-0.0.9.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1075 2021-04-08 12:21:32.849000 pysml-0.0.8/LICENSE
--rw-r--r--   0        0        0       81 2019-07-25 10:14:43.554000 pysml-0.0.8/README.md
--rwxr-xr-x   0        0        0    16411 2021-10-22 20:37:46.797000 pysml-0.0.8/examples/sml-mqtt-bridge.py
--rw-r--r--   0        0        0      321 2020-11-24 12:07:30.848000 pysml-0.0.8/examples/sml-mqtt-bridge.service
--rwxr-xr-x   0        0        0     2210 2019-07-25 11:13:20.016000 pysml-0.0.8/examples/test_asyncio.py
--rw-r--r--   0        0        0      682 2022-07-09 22:04:22.496961 pysml-0.0.8/pyproject.toml
--rw-r--r--   0        0        0    12725 2021-04-08 12:21:32.849000 pysml-0.0.8/sml/__init__.py
--rw-r--r--   0        0        0     5611 2022-07-09 22:04:22.496961 pysml-0.0.8/sml/asyncio.py
--rw-r--r--   0        0        0      914 2022-07-09 22:05:35.729101 pysml-0.0.8/setup.py
--rw-r--r--   0        0        0      762 2022-07-09 22:05:35.729356 pysml-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0     1075 2021-04-08 12:21:32.849000 pysml-0.0.9/LICENSE
+-rw-r--r--   0        0        0       81 2019-07-25 10:14:43.554000 pysml-0.0.9/README.md
+-rwxr-xr-x   0        0        0    16411 2021-10-22 20:37:46.797000 pysml-0.0.9/examples/sml-mqtt-bridge.py
+-rw-r--r--   0        0        0      321 2020-11-24 12:07:30.848000 pysml-0.0.9/examples/sml-mqtt-bridge.service
+-rwxr-xr-x   0        0        0     2210 2019-07-25 11:13:20.016000 pysml-0.0.9/examples/test_asyncio.py
+-rw-r--r--   0        0        0      682 2023-03-04 19:41:24.272000 pysml-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0    12725 2021-04-08 12:21:32.849000 pysml-0.0.9/sml/__init__.py
+-rw-r--r--   0        0        0     5642 2023-03-04 19:35:26.324000 pysml-0.0.9/sml/asyncio.py
+-rw-r--r--   0        0        0      920 1970-01-01 00:00:00.000000 pysml-0.0.9/setup.py
+-rw-r--r--   0        0        0      813 1970-01-01 00:00:00.000000 pysml-0.0.9/PKG-INFO
```

### Comparing `pysml-0.0.8/LICENSE` & `pysml-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pysml-0.0.8/examples/sml-mqtt-bridge.py` & `pysml-0.0.9/examples/sml-mqtt-bridge.py`

 * *Files identical despite different names*

### Comparing `pysml-0.0.8/examples/test_asyncio.py` & `pysml-0.0.9/examples/test_asyncio.py`

 * *Files identical despite different names*

### Comparing `pysml-0.0.8/pyproject.toml` & `pysml-0.0.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "pysml"
-version = "0.0.8"
+version = "0.0.9"
 description = "Python library for EDL21 smart meters using Smart Message Language (SML)"
 authors = ["Andreas Oberritter <obi@saftware.de>"]
 license = "MIT"
 readme = "README.md"
 packages = [
     { include = "sml" },
     { include = "sml-mqtt-bridge.py", from = "examples" },
```

### Comparing `pysml-0.0.8/sml/__init__.py` & `pysml-0.0.9/sml/__init__.py`

 * *Files identical despite different names*

### Comparing `pysml-0.0.8/sml/asyncio.py` & `pysml-0.0.9/sml/asyncio.py`

 * *Files 2% similar despite different names*

```diff
@@ -77,14 +77,15 @@
 
             delay = 1
 
         self._delay_reading(delay)
 
     def connection_lost(self, exc: Exception):
         logger.debug('port closed')
+        self._transport = None
         if self._running and not self._lock.locked():
             asyncio.ensure_future(self._reconnect(), loop=self._loop)
 
     def _dispatch(self, message_body: SmlSequence):
         for listener, types in self._listeners:
             if not types or type(message_body).__name__ in types:
                 listener(message_body)
```

### Comparing `pysml-0.0.8/setup.py` & `pysml-0.0.9/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -13,22 +13,22 @@
 modules = \
 ['sml-mqtt-bridge', 'test_asyncio']
 install_requires = \
 ['async-timeout>=4.0', 'bitstring>=3.1', 'pyserial-asyncio>=0.6']
 
 setup_kwargs = {
     'name': 'pysml',
-    'version': '0.0.8',
+    'version': '0.0.9',
     'description': 'Python library for EDL21 smart meters using Smart Message Language (SML)',
     'long_description': '# pysml\nPython library for EDL21 smart meters using Smart Message Language (SML)\n',
     'author': 'Andreas Oberritter',
     'author_email': 'obi@saftware.de',
-    'maintainer': None,
-    'maintainer_email': None,
-    'url': None,
+    'maintainer': 'None',
+    'maintainer_email': 'None',
+    'url': 'None',
     'package_dir': package_dir,
     'packages': packages,
     'package_data': package_data,
     'py_modules': modules,
     'install_requires': install_requires,
     'python_requires': '>=3.7,<4.0',
 }
```

