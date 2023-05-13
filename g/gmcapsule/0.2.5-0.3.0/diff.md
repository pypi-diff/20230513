# Comparing `tmp/gmcapsule-0.2.5.tar.gz` & `tmp/gmcapsule-0.3.0.tar.gz`

## Comparing `gmcapsule-0.2.5.tar` & `gmcapsule-0.3.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1263 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/example.ini
--rw-r--r--   0        0        0    22676 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/__init__.py
--rw-r--r--   0        0        0    24122 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/gemini.py
--rw-r--r--   0        0        0     4034 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/markdown.py
--rwxr-xr-x   0        0        0    18475 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/modules/80_gitview.py
--rw-r--r--   0        0        0     6368 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/modules/90_cgi.py
--rw-r--r--   0        0        0     2347 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/gmcapsule/modules/99_static.py
--rw-r--r--   0        0        0       70 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/.gitignore
--rw-r--r--   0        0        0     2082 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/README.md
--rw-r--r--   0        0        0     1739 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/pyproject.toml
--rw-r--r--   0        0        0     2995 2020-02-02 00:00:00.000000 gmcapsule-0.2.5/PKG-INFO
+-rw-r--r--   0        0        0     1263 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/example.ini
+-rw-r--r--   0        0        0    22960 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/__init__.py
+-rw-r--r--   0        0        0    24276 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/gemini.py
+-rw-r--r--   0        0        0     4034 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/markdown.py
+-rwxr-xr-x   0        0        0    18475 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/80_gitview.py
+-rw-r--r--   0        0        0     6368 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/90_cgi.py
+-rw-r--r--   0        0        0     2347 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/99_static.py
+-rw-r--r--   0        0        0       70 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/.gitignore
+-rw-r--r--   0        0        0     2340 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/README.md
+-rw-r--r--   0        0        0     1739 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0     3253 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/PKG-INFO
```

### Comparing `gmcapsule-0.2.5/example.ini` & `gmcapsule-0.3.0/example.ini`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/gmcapsule/__init__.py` & `gmcapsule-0.3.0/gmcapsule/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -436,15 +436,15 @@
 import subprocess
 from pathlib import Path
 
 from .gemini import Server, Cache
 from .markdown import to_gemtext as markdown_to_gemtext
 
 
-__version__ = '0.2.5'
+__version__ = '0.3.0'
 __all__ = [
     'Config', 'Capsule', 'Cache',
     'get_mime_type', 'markdown_to_gemtext'
 ]
 
 
 class Config:
@@ -644,14 +644,23 @@
                     loader = importlib.machinery.SourceFileLoader(name, str(path))
                     spec = importlib.util.spec_from_loader(name, loader)
                     mod = importlib.util.module_from_spec(spec)
                     loader.exec_module(mod)
                     print('MODULE:', mod.__doc__)
                     mod.init(self)
 
+    def shutdown_event(self):
+        """
+        Returns:
+            threading.Event: Event that is set when the server is
+            shutting down. Background workers must wait on this and stop
+            when the event is set.
+        """
+        return self.sv.shutdown_event
+
     def run(self):
         """
         Start worker threads and begin accepting incoming connections. The
         server will run until stopped with a KeyboardInterrupt (^C).
         """
         self.sv.run(memtrace=self.cfg.debug_memtrace)
```

### Comparing `gmcapsule-0.2.5/gmcapsule/gemini.py` & `gmcapsule-0.3.0/gmcapsule/gemini.py`

 * *Files 1% similar despite different names*

```diff
@@ -247,22 +247,23 @@
         scheme (str): Request protocol scheme. Either ``gemini`` or ``titan``.
         identity (gmcapsule.gemini.Identity): Client certificate.
             May be ``None``.
         hostname (str): Hostname.
         path (str): URL path. Always begins with a ``/``.
         query (str): Encoded query string. You can use `urllib.parse.unquote()
             <https://docs.python.org/3/library/urllib.parse.html#urllib.parse.unquote>`_
-            to decode the percent-coding.
+            to decode the percent-coding. ``None`` if the URL does not have a query
+            string.
         content_token (str): Encoded token specified in Titan URLs.
             May be ``None``.
         content_mime (str): MIME type specified in Titan URls. May be ``None``.
         content (bytes): Content uploaded by the client in a Titan request.
             May be ``None``.
     """
-    def __init__(self, identity=None, scheme='gemini', hostname='', path='', query='',
+    def __init__(self, identity=None, scheme='gemini', hostname='', path='', query=None,
                  remote_address=None, content_token=None, content_mime=None, content=None):
         self.remote_address = remote_address
         self.scheme = scheme
         self.identity = identity
         self.hostname = hostname
         self.path = path
         self.query = query
@@ -485,20 +486,20 @@
                 try:
                     response = entrypoint(Request(
                         identity,
                         remote_address=from_addr,
                         scheme=url.scheme,
                         hostname=hostname,
                         path=path,
-                        query=url.query,
+                        query=url.query if '?' in request else None,
                         content_token=req_token,
                         content_mime=req_mime,
                         content=data if len(data) else None
                     ))
-                except Exception as x:                    
+                except Exception as x:
                     import traceback
                     traceback.print_exception(x)
                     report_error(stream, 40, 'Temporary failure')
                     return
 
             # Determine status code, meta line, and body content.
             if type(response) == tuple:
@@ -570,14 +571,15 @@
         self.context.set_verify(SSL.VERIFY_PEER, verify_callback)
         if session_id:
             if type(session_id) != bytes:
                 raise Exception("session_id type must be `bytes`")
             self.context.set_session_id(session_id)
 
         # Spawn the worker threads.
+        self.shutdown_event = threading.Event()
         self.workers = []
         self.work_queue = queue.Queue()
         for worker_id in range(max(num_threads, 1)):
             worker = Worker(worker_id, self)
             self.workers.append(worker)
 
         self.sock = None
@@ -665,14 +667,15 @@
 
         # Close the server socket.
         self.sv_conn = None
         self.sock.close()
         self.sock = None
 
         # Stop all workers.
+        self.shutdown_event.set()
         if MULTITHREAD:
             for i in range(len(self.workers)):
                 self.work_queue.put((None, None))
             for worker in self.workers:
                 worker.join()
 
         print('Done')
```

### Comparing `gmcapsule-0.2.5/gmcapsule/markdown.py` & `gmcapsule-0.3.0/gmcapsule/markdown.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/gmcapsule/modules/80_gitview.py` & `gmcapsule-0.3.0/gmcapsule/modules/80_gitview.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/gmcapsule/modules/90_cgi.py` & `gmcapsule-0.3.0/gmcapsule/modules/90_cgi.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/gmcapsule/modules/99_static.py` & `gmcapsule-0.3.0/gmcapsule/modules/99_static.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/README.md` & `gmcapsule-0.3.0/README.md`

 * *Files 13% similar despite different names*

```diff
@@ -15,24 +15,24 @@
 ## Running via systemd
 
 Create the following service file and save it as _~/.config/systemd/user/gmcapsule.service_:
 
     [Unit]
     Description=GmCapsule: extensible Gemini/Titan server
     After=network.target
-    
+
     [Service]
     Type=simple
     ExecStart=<YOUR-INSTALL-PATH>/gmcapsuled
     Restart=always
     Environment="PYTHONUNBUFFERED=1"
     StandardOutput=syslog
     StandardError=syslog
     SyslogIdentifier=gmcapsule
-    
+
     [Install]
     WantedBy=default.target
 
 Replace `<YOUR-INSTALL-PATH>` with the actual path of `gmcapsuled`. `pip` will install it in a directory on your PATH.
 
 Then you can do the usual:
 
@@ -42,14 +42,19 @@
 
 The log can be viewed via journalctl (or syslog):
 
     journalctl -xe --user-unit=gmcapsule
 
 ## Change log
 
+### v0.3
+
+* Added a shutdown event for custom background workers.
+* `Request.query` is None if there is no query string present. Previously, the query string was an empty string in this case. This allows making a distinction between empty and absent query strings.
+
 ### v0.2
 
 * Added `[cgi] bin_root` configuration option for automatically and dynamically mapping all executables in a directory tree to URL entry points.
 * Minor documentation updates.
 * Published on PyPi as "gmcapsule".
 
 v0.2.1:
```

### Comparing `gmcapsule-0.2.5/pyproject.toml` & `gmcapsule-0.3.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.2.5/PKG-INFO` & `gmcapsule-0.3.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gmcapsule
-Version: 0.2.5
+Version: 0.3.0
 Summary: Extensible Gemini/Titan server
 Project-URL: Home-page, https://geminispace.org/gmcapsule/
 Project-URL: Documentation, https://geminispace.org/gmcapsule/gmcapsule.html
 Project-URL: Source, https://codeberg.org/skyjake/gmcapsule
 Project-URL: Issues, https://codeberg.org/skyjake/gmcapsule/issues
 Author-email: Jaakko Keränen <jaakko.keranen@iki.fi>
 Keywords: gemini,internet,server,titan
@@ -37,24 +37,24 @@
 ## Running via systemd
 
 Create the following service file and save it as _~/.config/systemd/user/gmcapsule.service_:
 
     [Unit]
     Description=GmCapsule: extensible Gemini/Titan server
     After=network.target
-    
+
     [Service]
     Type=simple
     ExecStart=<YOUR-INSTALL-PATH>/gmcapsuled
     Restart=always
     Environment="PYTHONUNBUFFERED=1"
     StandardOutput=syslog
     StandardError=syslog
     SyslogIdentifier=gmcapsule
-    
+
     [Install]
     WantedBy=default.target
 
 Replace `<YOUR-INSTALL-PATH>` with the actual path of `gmcapsuled`. `pip` will install it in a directory on your PATH.
 
 Then you can do the usual:
 
@@ -64,14 +64,19 @@
 
 The log can be viewed via journalctl (or syslog):
 
     journalctl -xe --user-unit=gmcapsule
 
 ## Change log
 
+### v0.3
+
+* Added a shutdown event for custom background workers.
+* `Request.query` is None if there is no query string present. Previously, the query string was an empty string in this case. This allows making a distinction between empty and absent query strings.
+
 ### v0.2
 
 * Added `[cgi] bin_root` configuration option for automatically and dynamically mapping all executables in a directory tree to URL entry points.
 * Minor documentation updates.
 * Published on PyPi as "gmcapsule".
 
 v0.2.1:
```

