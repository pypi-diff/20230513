# Comparing `tmp/pyvantage-0.0.42.tar.gz` & `tmp/pyvantage-0.0.43.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvantage-0.0.42.tar", last modified: Mon Apr 24 16:02:50 2023, max compression
+gzip compressed data, was "pyvantage-0.0.43.tar", last modified: Sat May 13 18:22:11 2023, max compression
```

## Comparing `pyvantage-0.0.42.tar` & `pyvantage-0.0.43.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-04-24 16:02:50.398539 pyvantage-0.0.42/
--rw-r--r--   0 greg       (501) staff       (20)     1179 2021-06-03 17:37:04.000000 pyvantage-0.0.42/LICENSE
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-04-24 16:02:50.398643 pyvantage-0.0.42/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)     2164 2023-04-23 17:44:30.000000 pyvantage-0.0.42/README.md
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-04-24 16:02:50.396263 pyvantage-0.0.42/pyvantage/
--rw-r--r--   0 greg       (501) staff       (20)    99569 2023-04-24 16:00:56.000000 pyvantage-0.0.42/pyvantage/__init__.py
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-04-24 16:02:50.397921 pyvantage-0.0.42/pyvantage.egg-info/
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-04-24 16:02:50.000000 pyvantage-0.0.42/pyvantage.egg-info/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)      218 2023-04-24 16:02:50.000000 pyvantage-0.0.42/pyvantage.egg-info/SOURCES.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2023-04-24 16:02:50.000000 pyvantage-0.0.42/pyvantage.egg-info/dependency_links.txt
--rw-r--r--   0 greg       (501) staff       (20)       10 2023-04-24 16:02:50.000000 pyvantage-0.0.42/pyvantage.egg-info/top_level.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2023-04-23 18:11:37.000000 pyvantage-0.0.42/pyvantage.egg-info/zip-safe
--rw-r--r--   0 greg       (501) staff       (20)       79 2023-04-24 16:02:50.399045 pyvantage-0.0.42/setup.cfg
--rw-r--r--   0 greg       (501) staff       (20)      769 2023-04-24 16:01:39.000000 pyvantage-0.0.42/setup.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.651425 pyvantage-0.0.43/
+-rw-r--r--   0 greg       (501) staff       (20)     1179 2022-07-01 22:35:08.000000 pyvantage-0.0.43/LICENSE
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 18:22:11.651528 pyvantage-0.0.43/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)     2164 2022-07-01 22:35:08.000000 pyvantage-0.0.43/README.md
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.649236 pyvantage-0.0.43/pyvantage/
+-rw-r--r--   0 greg       (501) staff       (20)    99581 2023-05-13 18:20:07.000000 pyvantage-0.0.43/pyvantage/__init__.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.650839 pyvantage-0.0.43/pyvantage.egg-info/
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)      218 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/SOURCES.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/dependency_links.txt
+-rw-r--r--   0 greg       (501) staff       (20)       10 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/top_level.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2022-07-01 22:35:59.000000 pyvantage-0.0.43/pyvantage.egg-info/zip-safe
+-rw-r--r--   0 greg       (501) staff       (20)       79 2023-05-13 18:22:11.651924 pyvantage-0.0.43/setup.cfg
+-rw-r--r--   0 greg       (501) staff       (20)      769 2023-05-13 18:04:56.000000 pyvantage-0.0.43/setup.py
```

### Comparing `pyvantage-0.0.42/LICENSE` & `pyvantage-0.0.43/LICENSE`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.42/PKG-INFO` & `pyvantage-0.0.43/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.42
+Version: 0.0.43
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.42/README.md` & `pyvantage-0.0.43/README.md`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.42/pyvantage/__init__.py` & `pyvantage-0.0.43/pyvantage/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -319,15 +319,15 @@
             try:
                 readable, _, exceptional = select.select(self._sockets, [], [])
                 for i, sock in enumerate(self._sockets):
                     if sock in exceptional:
                         _LOGGER.error("Exceptional socket #%s: %s", i, t)
                         raise EOFError()
                     if sock in readable:
-                        line = self._read_until(b'\n', i)
+                        line = self._read_until(b'\r\n', i)
                         self._recv_cb(line.decode('ascii').rstrip(), i)
             except EOFError:
                 _LOGGER.warning("run got EOFError")
                 with self._lock:
                     self._disconnect_locked()
                 continue
             except BrokenPipeError:
@@ -1168,15 +1168,15 @@
                 this_cmd = self._cmds.popleft()
             else:
                 this_cmd = "__UNDERFLOW__"
         elif line[0] == 'S':
             cmds = self._s_cmds
             typ = 'S'
         else:
-            _LOGGER.error("#%s _recv got unknown line start character", i)
+            _LOGGER.error("#%s _recv got unknown line start character: %s", i, line)
             return
         parts = re.split(r'[ :]', line[2:])
         cmd_type = parts[0]
         vid = parts[1]
         args = parts[2:]
         if cmd_type not in cmds:
             _LOGGER.warning("#%s Unknown cmd %s (%s)", i, cmd_type, line)
```

### Comparing `pyvantage-0.0.42/pyvantage.egg-info/PKG-INFO` & `pyvantage-0.0.43/pyvantage.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.42
+Version: 0.0.43
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.42/setup.py` & `pyvantage-0.0.43/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 from setuptools import setup, find_packages
 
 setup(
     name='pyvantage',
-    version='0.0.42',
+    version='0.0.43',
     license='MIT',
     description='Python library for Vantage Controller (for Home Assistant)',
     author='Greg J. Badros',
     author_email='badros@gmail.com',
     url='http://github.com/gjbadros/pyvantage',
     packages=find_packages(),
     classifiers=[
```

