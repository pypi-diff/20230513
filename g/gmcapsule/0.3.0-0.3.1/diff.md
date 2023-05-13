# Comparing `tmp/gmcapsule-0.3.0.tar.gz` & `tmp/gmcapsule-0.3.1.tar.gz`

## Comparing `gmcapsule-0.3.0.tar` & `gmcapsule-0.3.1.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1263 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/example.ini
--rw-r--r--   0        0        0    22960 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/__init__.py
--rw-r--r--   0        0        0    24276 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/gemini.py
--rw-r--r--   0        0        0     4034 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/markdown.py
--rwxr-xr-x   0        0        0    18475 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/80_gitview.py
--rw-r--r--   0        0        0     6368 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/90_cgi.py
--rw-r--r--   0        0        0     2347 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/gmcapsule/modules/99_static.py
--rw-r--r--   0        0        0       70 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/.gitignore
--rw-r--r--   0        0        0     2340 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/README.md
--rw-r--r--   0        0        0     1739 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     3253 2020-02-02 00:00:00.000000 gmcapsule-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1263 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/example.ini
+-rw-r--r--   0        0        0    22960 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/__init__.py
+-rw-r--r--   0        0        0    24276 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/gemini.py
+-rw-r--r--   0        0        0     4034 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/markdown.py
+-rwxr-xr-x   0        0        0    18475 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/modules/80_gitview.py
+-rw-r--r--   0        0        0     6357 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/modules/90_cgi.py
+-rw-r--r--   0        0        0     2347 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/gmcapsule/modules/99_static.py
+-rw-r--r--   0        0        0       70 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/.gitignore
+-rw-r--r--   0        0        0     2399 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/README.md
+-rw-r--r--   0        0        0     1739 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0     3312 2020-02-02 00:00:00.000000 gmcapsule-0.3.1/PKG-INFO
```

### Comparing `gmcapsule-0.3.0/example.ini` & `gmcapsule-0.3.1/example.ini`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/gmcapsule/__init__.py` & `gmcapsule-0.3.1/gmcapsule/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -436,15 +436,15 @@
 import subprocess
 from pathlib import Path
 
 from .gemini import Server, Cache
 from .markdown import to_gemtext as markdown_to_gemtext
 
 
-__version__ = '0.3.0'
+__version__ = '0.3.1'
 __all__ = [
     'Config', 'Capsule', 'Cache',
     'get_mime_type', 'markdown_to_gemtext'
 ]
 
 
 class Config:
```

### Comparing `gmcapsule-0.3.0/gmcapsule/gemini.py` & `gmcapsule-0.3.1/gmcapsule/gemini.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/gmcapsule/markdown.py` & `gmcapsule-0.3.1/gmcapsule/markdown.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/gmcapsule/modules/80_gitview.py` & `gmcapsule-0.3.1/gmcapsule/modules/80_gitview.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/gmcapsule/modules/90_cgi.py` & `gmcapsule-0.3.1/gmcapsule/modules/90_cgi.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,29 +19,29 @@
         self.base_path = url_path
         if self.base_path.endswith('/*'):
             self.base_path = self.base_path[:-2]
         self.work_dir = work_dir
 
     def __call__(self, req):
         try:
-            query = urllib.parse.unquote(req.query)
             env_vars = dict(os.environ)
 
             # Standard CGI variables.
             env_vars['GATEWAY_INTERFACE'] = 'CGI/1.1'
             env_vars['REMOTE_ADDR'] = '%s:%d' % req.remote_address
-            env_vars['QUERY_STRING'] = req.query
+            if req.query != None:
+                env_vars['QUERY_STRING'] = req.query
             env_vars['PATH_INFO'] = req.path
             env_vars['SCRIPT_NAME'] = self.base_path
             env_vars['SERVER_SOFTWARE'] = 'GmCapsule/' + gmcapsule.__version__
             env_vars['SERVER_PROTOCOL'] = req.scheme.upper()
             env_vars['SERVER_NAME'] = req.hostname
             env_vars['SERVER_PORT'] = str(Capsule.config().port())
             env_vars[req.scheme.upper() + '_URL'] = f"{req.scheme}://{req.hostname}{req.path}" + (
-                '?' + req.query if len(req.query) else '')
+                '?' + req.query if req.query != None else '')
             env_vars[req.scheme.upper() + '_URL_PATH'] = req.path
 
             # TLS client certificate.
             if req.identity:
                 env_vars['AUTH_TYPE'] = 'Certificate'
                 id_sub = req.identity.subject()
                 env_vars['REMOTE_USER'] = id_sub['CN'] if 'CN' in id_sub else ''
```

### Comparing `gmcapsule-0.3.0/gmcapsule/modules/99_static.py` & `gmcapsule-0.3.1/gmcapsule/modules/99_static.py`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/README.md` & `gmcapsule-0.3.1/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -47,14 +47,18 @@
 ## Change log
 
 ### v0.3
 
 * Added a shutdown event for custom background workers.
 * `Request.query` is None if there is no query string present. Previously, the query string was an empty string in this case. This allows making a distinction between empty and absent query strings.
 
+v0.3.1:
+
+* CGI: Fixed handling of a missing query string.
+
 ### v0.2
 
 * Added `[cgi] bin_root` configuration option for automatically and dynamically mapping all executables in a directory tree to URL entry points.
 * Minor documentation updates.
 * Published on PyPi as "gmcapsule".
 
 v0.2.1:
```

### Comparing `gmcapsule-0.3.0/pyproject.toml` & `gmcapsule-0.3.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `gmcapsule-0.3.0/PKG-INFO` & `gmcapsule-0.3.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gmcapsule
-Version: 0.3.0
+Version: 0.3.1
 Summary: Extensible Gemini/Titan server
 Project-URL: Home-page, https://geminispace.org/gmcapsule/
 Project-URL: Documentation, https://geminispace.org/gmcapsule/gmcapsule.html
 Project-URL: Source, https://codeberg.org/skyjake/gmcapsule
 Project-URL: Issues, https://codeberg.org/skyjake/gmcapsule/issues
 Author-email: Jaakko Keränen <jaakko.keranen@iki.fi>
 Keywords: gemini,internet,server,titan
@@ -69,14 +69,18 @@
 ## Change log
 
 ### v0.3
 
 * Added a shutdown event for custom background workers.
 * `Request.query` is None if there is no query string present. Previously, the query string was an empty string in this case. This allows making a distinction between empty and absent query strings.
 
+v0.3.1:
+
+* CGI: Fixed handling of a missing query string.
+
 ### v0.2
 
 * Added `[cgi] bin_root` configuration option for automatically and dynamically mapping all executables in a directory tree to URL entry points.
 * Minor documentation updates.
 * Published on PyPi as "gmcapsule".
 
 v0.2.1:
```

