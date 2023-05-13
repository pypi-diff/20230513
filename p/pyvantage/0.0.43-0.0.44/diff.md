# Comparing `tmp/pyvantage-0.0.43.tar.gz` & `tmp/pyvantage-0.0.44.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvantage-0.0.43.tar", last modified: Sat May 13 18:22:11 2023, max compression
+gzip compressed data, was "pyvantage-0.0.44.tar", last modified: Sat May 13 19:55:30 2023, max compression
```

## Comparing `pyvantage-0.0.43.tar` & `pyvantage-0.0.44.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.651425 pyvantage-0.0.43/
--rw-r--r--   0 greg       (501) staff       (20)     1179 2022-07-01 22:35:08.000000 pyvantage-0.0.43/LICENSE
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 18:22:11.651528 pyvantage-0.0.43/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)     2164 2022-07-01 22:35:08.000000 pyvantage-0.0.43/README.md
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.649236 pyvantage-0.0.43/pyvantage/
--rw-r--r--   0 greg       (501) staff       (20)    99581 2023-05-13 18:20:07.000000 pyvantage-0.0.43/pyvantage/__init__.py
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 18:22:11.650839 pyvantage-0.0.43/pyvantage.egg-info/
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)      218 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/SOURCES.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/dependency_links.txt
--rw-r--r--   0 greg       (501) staff       (20)       10 2023-05-13 18:22:11.000000 pyvantage-0.0.43/pyvantage.egg-info/top_level.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2022-07-01 22:35:59.000000 pyvantage-0.0.43/pyvantage.egg-info/zip-safe
--rw-r--r--   0 greg       (501) staff       (20)       79 2023-05-13 18:22:11.651924 pyvantage-0.0.43/setup.cfg
--rw-r--r--   0 greg       (501) staff       (20)      769 2023-05-13 18:04:56.000000 pyvantage-0.0.43/setup.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.577146 pyvantage-0.0.44/
+-rw-r--r--   0 greg       (501) staff       (20)     1179 2022-07-01 22:35:08.000000 pyvantage-0.0.44/LICENSE
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 19:55:30.577350 pyvantage-0.0.44/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)     2164 2022-07-01 22:35:08.000000 pyvantage-0.0.44/README.md
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.573556 pyvantage-0.0.44/pyvantage/
+-rw-r--r--   0 greg       (501) staff       (20)    99685 2023-05-13 19:53:57.000000 pyvantage-0.0.44/pyvantage/__init__.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.576211 pyvantage-0.0.44/pyvantage.egg-info/
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)      218 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/SOURCES.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/dependency_links.txt
+-rw-r--r--   0 greg       (501) staff       (20)       10 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/top_level.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2022-07-01 22:35:59.000000 pyvantage-0.0.44/pyvantage.egg-info/zip-safe
+-rw-r--r--   0 greg       (501) staff       (20)       79 2023-05-13 19:55:30.578033 pyvantage-0.0.44/setup.cfg
+-rw-r--r--   0 greg       (501) staff       (20)      769 2023-05-13 19:46:20.000000 pyvantage-0.0.44/setup.py
```

### Comparing `pyvantage-0.0.43/LICENSE` & `pyvantage-0.0.44/LICENSE`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.43/PKG-INFO` & `pyvantage-0.0.44/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.43
+Version: 0.0.44
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.43/README.md` & `pyvantage-0.0.44/README.md`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.43/pyvantage/__init__.py` & `pyvantage-0.0.44/pyvantage/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -25,15 +25,15 @@
 > cp /config/pyvantage/pyvantage/__init__.py /usr/local/lib/python3.7/site-packages/pyvantage
 # where /config in the docker image points to my home assistant config directory
 # which has a pyvantage subdirectory containing a clone of the github repo.
 
 """
 
 __Author__ = "Greg J. Badros"
-__copyright__ = "Copyright 2018, 2019, 2020 Greg J. Badros"
+__copyright__ = "Copyright 2018-2023 Greg J. Badros"
 
 # USAGE:
 #
 # Instantiate a Vantage controller object:
 #
 #   vc = Vantage("192.168.1.42", "myusername", "mypassword");
 #
@@ -320,15 +320,17 @@
                 readable, _, exceptional = select.select(self._sockets, [], [])
                 for i, sock in enumerate(self._sockets):
                     if sock in exceptional:
                         _LOGGER.error("Exceptional socket #%s: %s", i, t)
                         raise EOFError()
                     if sock in readable:
                         line = self._read_until(b'\r\n', i)
-                        self._recv_cb(line.decode('ascii').rstrip(), i)
+                        lines = line.split(b'[\r\n]+')
+                        for each_line in lines:
+                            self._recv_cb(each_line.decode('ascii').rstrip(), i)
             except EOFError:
                 _LOGGER.warning("run got EOFError")
                 with self._lock:
                     self._disconnect_locked()
                 continue
             except BrokenPipeError:
                 _LOGGER.warning("run got BrokenPipeError")
@@ -1151,15 +1153,15 @@
                 _LOGGER.debug(f"Repeated name `{oldname}' - adding vid to get {obj.name}")
         self._names[obj.name] = obj.vid
 
 
     # Note: invoked on VantageConnection thread.
     def _recv(self, line, i=0):
         """Invoked by the connection manager to process incoming data."""
-        _LOGGER.debug(f"#{i} _recv got line: {line}")
+        _LOGGER.info(f"#{i} _recv got line: {line}")
         if line == '':
             return
         typ = None
         # Only handle query response messages, which are also sent on remote
         # status updates (e.g. user manually pressed a keypad button)
         if line[0] == 'R':
             cmds = self._r_cmds
```

### Comparing `pyvantage-0.0.43/pyvantage.egg-info/PKG-INFO` & `pyvantage-0.0.44/pyvantage.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.43
+Version: 0.0.44
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.43/setup.py` & `pyvantage-0.0.44/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 from setuptools import setup, find_packages
 
 setup(
     name='pyvantage',
-    version='0.0.43',
+    version='0.0.44',
     license='MIT',
     description='Python library for Vantage Controller (for Home Assistant)',
     author='Greg J. Badros',
     author_email='badros@gmail.com',
     url='http://github.com/gjbadros/pyvantage',
     packages=find_packages(),
     classifiers=[
```

