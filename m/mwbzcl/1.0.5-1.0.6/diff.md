# Comparing `tmp/mwbzcl-1.0.5.tar.gz` & `tmp/mwbzcl-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "P:\CommandLineClients\MalwareBazaarClient\dist\.tmp-3jtyy71d\mwbzcl-1.0.5.tar", last modified: Sun Jan  8 10:28:02 2023, max compression
+gzip compressed data, was "P:\CommandLineClients\MalwareBazaarClient\dist\.tmp-ikh02ycx\mwbzcl-1.0.6.tar", last modified: Sat May 13 12:39:42 2023, max compression
```

## Comparing `mwbzcl-1.0.5.tar` & `mwbzcl-1.0.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/
--rw-rw-rw-   0        0        0     1090 2023-01-08 08:57:13.000000 mwbzcl-1.0.5/LICENSE
--rw-rw-rw-   0        0        0     2063 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/PKG-INFO
--rw-rw-rw-   0        0        0     1137 2023-01-08 09:04:08.000000 mwbzcl-1.0.5/README.md
-drwxrwxrwx   0        0        0        0 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl/
--rw-rw-rw-   0        0        0       75 2023-01-08 10:26:32.000000 mwbzcl-1.0.5/mwbzcl/__init__.py
--rw-rw-rw-   0        0        0     6796 2023-01-08 08:54:37.000000 mwbzcl-1.0.5/mwbzcl/client.py
-drwxrwxrwx   0        0        0        0 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/
--rw-rw-rw-   0        0        0     2063 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      254 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       39 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       18 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/mwbzcl.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       81 2023-01-08 10:28:02.000000 mwbzcl-1.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1337 2023-01-08 10:27:41.000000 mwbzcl-1.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/
+-rw-rw-rw-   0        0        0     1090 2023-01-08 08:57:13.000000 mwbzcl-1.0.6/LICENSE
+-rw-rw-rw-   0        0        0     2972 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0     2046 2023-05-13 12:39:02.000000 mwbzcl-1.0.6/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl/
+-rw-rw-rw-   0        0        0       75 2023-01-08 10:26:32.000000 mwbzcl-1.0.6/mwbzcl/__init__.py
+-rw-rw-rw-   0        0        0     7439 2023-05-13 12:36:27.000000 mwbzcl-1.0.6/mwbzcl/client.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/
+-rw-rw-rw-   0        0        0     2972 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      254 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       39 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       18 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/mwbzcl.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       81 2023-05-13 12:39:42.000000 mwbzcl-1.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1337 2023-05-13 12:38:19.000000 mwbzcl-1.0.6/setup.py
```

### Comparing `mwbzcl-1.0.5/LICENSE` & `mwbzcl-1.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `mwbzcl-1.0.5/mwbzcl/client.py` & `mwbzcl-1.0.6/mwbzcl/client.py`

 * *Files 9% similar despite different names*

```diff
@@ -107,14 +107,22 @@
         data = io.BytesIO()
         data.write(response.content)
         zip_file = pyzipper.AESZipFile(data)
         zip_file.setpassword(b'infected')
         for name in zip_file.namelist():
             return zip_file.read(name)
 
+    def query(self, hsh) -> typing.Dict:
+        response = self.session.post(self.base_url, data={'query': 'get_info', 'hash': hsh})
+        response.raise_for_status()
+        data = response.json()
+        if data['query_status'] != 'ok':
+            raise MalwareBazaarException(f'Query status of "{data["query_status"]}"')
+        return data['data'][0]
+
     def by_signature(self, signature_name: str, limit: int = 10) -> typing.Iterable[MalwareSample]:
         response = self.session.post(self.base_url, data={
             'query': 'get_siginfo',
             'signature': signature_name,
             'limit': limit
         })
         response.raise_for_status()
@@ -184,16 +192,21 @@
             for sha256 in args.sha256s:
                 sha256 = sha256.lower()
                 if os.path.exists(sha256):
                     logger.warning(F'File with name {sha256} already exists.')
                     skipped += 1
                     continue
                 if not sha256_r.match(sha256):
-                    logger.warning(F'Argument "{sha256}" not a valid SHA256 hash.')
-                    continue
+                    logger.warning(F'Argument "{sha256}" not a valid SHA256 hash...')
+                    try:
+                        sha256 = client.query(sha256).get('sha256_hash')
+                    except MalwareBazaarException as e:
+                        logger.error(str(e))
+                        continue
+                    logger.warning(F'Translated to "{sha256}".')
                 with open(sha256, 'wb') as fp:
                     fp.write(client.download(sha256))
                 downloaded += 1
             logger.info(F'Downloaded {downloaded} file(s), {skipped} skipped.')
 
     except MalwareBazaarException as e:
         logger.exception(e)
```

### Comparing `mwbzcl-1.0.5/setup.py` & `mwbzcl-1.0.6/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup
 
 with open('README.md', 'r', encoding='utf-8') as fp:
     long_description = fp.read()
 
 setup(
     name='mwbzcl',
-    version='1.0.5',
+    version='1.0.6',
     description='A command-line client to interact with the MalwareBazaar API',
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/larsborn/MalwareBazaarClient",
     project_urls={
         "Bug Tracker": "https://github.com/larsborn/MalwareBazaarClient/issues",
     },
```

