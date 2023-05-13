# Comparing `tmp/pyvantage-0.0.44.tar.gz` & `tmp/pyvantage-0.0.45.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvantage-0.0.44.tar", last modified: Sat May 13 19:55:30 2023, max compression
+gzip compressed data, was "pyvantage-0.0.45.tar", last modified: Sat May 13 20:33:03 2023, max compression
```

## Comparing `pyvantage-0.0.44.tar` & `pyvantage-0.0.45.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.577146 pyvantage-0.0.44/
--rw-r--r--   0 greg       (501) staff       (20)     1179 2022-07-01 22:35:08.000000 pyvantage-0.0.44/LICENSE
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 19:55:30.577350 pyvantage-0.0.44/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)     2164 2022-07-01 22:35:08.000000 pyvantage-0.0.44/README.md
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.573556 pyvantage-0.0.44/pyvantage/
--rw-r--r--   0 greg       (501) staff       (20)    99685 2023-05-13 19:53:57.000000 pyvantage-0.0.44/pyvantage/__init__.py
-drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 19:55:30.576211 pyvantage-0.0.44/pyvantage.egg-info/
--rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/PKG-INFO
--rw-r--r--   0 greg       (501) staff       (20)      218 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/SOURCES.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/dependency_links.txt
--rw-r--r--   0 greg       (501) staff       (20)       10 2023-05-13 19:55:30.000000 pyvantage-0.0.44/pyvantage.egg-info/top_level.txt
--rw-r--r--   0 greg       (501) staff       (20)        1 2022-07-01 22:35:59.000000 pyvantage-0.0.44/pyvantage.egg-info/zip-safe
--rw-r--r--   0 greg       (501) staff       (20)       79 2023-05-13 19:55:30.578033 pyvantage-0.0.44/setup.cfg
--rw-r--r--   0 greg       (501) staff       (20)      769 2023-05-13 19:46:20.000000 pyvantage-0.0.44/setup.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 20:33:03.379623 pyvantage-0.0.45/
+-rw-r--r--   0 greg       (501) staff       (20)     1179 2022-07-01 22:35:08.000000 pyvantage-0.0.45/LICENSE
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 20:33:03.379736 pyvantage-0.0.45/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)     2164 2022-07-01 22:35:08.000000 pyvantage-0.0.45/README.md
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 20:33:03.377123 pyvantage-0.0.45/pyvantage/
+-rw-r--r--   0 greg       (501) staff       (20)    99977 2023-05-13 20:31:30.000000 pyvantage-0.0.45/pyvantage/__init__.py
+drwxr-xr-x   0 greg       (501) staff       (20)        0 2023-05-13 20:33:03.378971 pyvantage-0.0.45/pyvantage.egg-info/
+-rw-r--r--   0 greg       (501) staff       (20)      604 2023-05-13 20:33:03.000000 pyvantage-0.0.45/pyvantage.egg-info/PKG-INFO
+-rw-r--r--   0 greg       (501) staff       (20)      218 2023-05-13 20:33:03.000000 pyvantage-0.0.45/pyvantage.egg-info/SOURCES.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2023-05-13 20:33:03.000000 pyvantage-0.0.45/pyvantage.egg-info/dependency_links.txt
+-rw-r--r--   0 greg       (501) staff       (20)       10 2023-05-13 20:33:03.000000 pyvantage-0.0.45/pyvantage.egg-info/top_level.txt
+-rw-r--r--   0 greg       (501) staff       (20)        1 2022-07-01 22:35:59.000000 pyvantage-0.0.45/pyvantage.egg-info/zip-safe
+-rw-r--r--   0 greg       (501) staff       (20)       79 2023-05-13 20:33:03.380250 pyvantage-0.0.45/setup.cfg
+-rw-r--r--   0 greg       (501) staff       (20)      769 2023-05-13 20:31:48.000000 pyvantage-0.0.45/setup.py
```

### Comparing `pyvantage-0.0.44/LICENSE` & `pyvantage-0.0.45/LICENSE`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.44/PKG-INFO` & `pyvantage-0.0.45/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.44
+Version: 0.0.45
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.44/README.md` & `pyvantage-0.0.45/README.md`

 * *Files identical despite different names*

### Comparing `pyvantage-0.0.44/pyvantage/__init__.py` & `pyvantage-0.0.45/pyvantage/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -320,15 +320,15 @@
                 readable, _, exceptional = select.select(self._sockets, [], [])
                 for i, sock in enumerate(self._sockets):
                     if sock in exceptional:
                         _LOGGER.error("Exceptional socket #%s: %s", i, t)
                         raise EOFError()
                     if sock in readable:
                         line = self._read_until(b'\r\n', i)
-                        lines = line.split(b'[\r\n]+')
+                        lines = line.splitlines()
                         for each_line in lines:
                             self._recv_cb(each_line.decode('ascii').rstrip(), i)
             except EOFError:
                 _LOGGER.warning("run got EOFError")
                 with self._lock:
                     self._disconnect_locked()
                 continue
@@ -1153,15 +1153,15 @@
                 _LOGGER.debug(f"Repeated name `{oldname}' - adding vid to get {obj.name}")
         self._names[obj.name] = obj.vid
 
 
     # Note: invoked on VantageConnection thread.
     def _recv(self, line, i=0):
         """Invoked by the connection manager to process incoming data."""
-        _LOGGER.info(f"#{i} _recv got line: {line}")
+        _LOGGER.debug(f"#{i} _recv got line: {line}")
         if line == '':
             return
         typ = None
         # Only handle query response messages, which are also sent on remote
         # status updates (e.g. user manually pressed a keypad button)
         if line[0] == 'R':
             cmds = self._r_cmds
@@ -1173,14 +1173,17 @@
         elif line[0] == 'S':
             cmds = self._s_cmds
             typ = 'S'
         else:
             _LOGGER.error("#%s _recv got unknown line start character: %s", i, line)
             return
         parts = re.split(r'[ :]', line[2:])
+        if len(parts) < 2:
+            _LOGGER.error("#%s Got partial line: %s", i, line)
+            return
         cmd_type = parts[0]
         vid = parts[1]
         args = parts[2:]
         if cmd_type not in cmds:
             _LOGGER.warning("#%s Unknown cmd %s (%s)", i, cmd_type, line)
             return
         if cmd_type == 'LOGIN':
@@ -2429,15 +2432,19 @@
                 # and undouble internal quotes
                 value = args[0][1:-1].replace('""', '"')
             elif self._kind == 'variable_bool':
                 value = args[0] == '1'
             else:
                 value = float(args[0])
         except Exception:
-            value = args[0]
+            if len(args) >= 1:
+                value = args[0]
+            else:
+                _LOGGER.error("No args for sensor value (%s) %s (%d)", self._name, self._kind, self._vid)
+                return self
         _LOGGER.debug("Setting sensor (%s) %s (%d) to %s",
                       self._name, self._kind, self._vid, value)
         self._value = value
         return self
 
 
 class Variable(PollingSensor):
```

### Comparing `pyvantage-0.0.44/pyvantage.egg-info/PKG-INFO` & `pyvantage-0.0.45/pyvantage.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvantage
-Version: 0.0.44
+Version: 0.0.45
 Summary: Python library for Vantage Controller (for Home Assistant)
 Home-page: http://github.com/gjbadros/pyvantage
 Author: Greg J. Badros
 Author-email: badros@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pyvantage-0.0.44/setup.py` & `pyvantage-0.0.45/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 from setuptools import setup, find_packages
 
 setup(
     name='pyvantage',
-    version='0.0.44',
+    version='0.0.45',
     license='MIT',
     description='Python library for Vantage Controller (for Home Assistant)',
     author='Greg J. Badros',
     author_email='badros@gmail.com',
     url='http://github.com/gjbadros/pyvantage',
     packages=find_packages(),
     classifiers=[
```

