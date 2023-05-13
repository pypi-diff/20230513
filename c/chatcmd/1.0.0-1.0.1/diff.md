# Comparing `tmp/chatcmd-1.0.0.tar.gz` & `tmp/chatcmd-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chatcmd-1.0.0.tar", max compression
+gzip compressed data, was "chatcmd-1.0.1.tar", max compression
```

## Comparing `chatcmd-1.0.0.tar` & `chatcmd-1.0.1.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0        0 2023-04-26 12:02:06.350462 chatcmd-1.0.0/chatcmd/__init__.py
--rw-r--r--   0        0        0     1644 2023-05-13 16:35:10.169167 chatcmd-1.0.0/chatcmd/api.py
--rw-r--r--   0        0        0     3355 2023-05-13 20:34:19.254956 chatcmd-1.0.0/chatcmd/chatcmd.py
--rw-r--r--   0        0        0     3770 2023-05-02 11:20:31.998824 chatcmd-1.0.0/chatcmd/commands.py
--rw-r--r--   0        0        0     2147 2023-05-13 16:29:09.346061 chatcmd-1.0.0/chatcmd/helpers.py
--rw-r--r--   0        0        0   138838 2023-04-26 12:02:06.351951 chatcmd-1.0.0/chatcmd/images/help.png
--rw-r--r--   0        0        0    76959 2023-04-26 12:02:06.352459 chatcmd-1.0.0/chatcmd/images/library-info.png
--rw-r--r--   0        0        0    23781 2023-04-26 12:02:06.352705 chatcmd-1.0.0/chatcmd/images/lookup.png
--rw-r--r--   0        0        0     2615 2023-05-11 23:45:56.420188 chatcmd-1.0.0/chatcmd/lookup.py
--rw-r--r--   0        0        0     1856 2023-05-13 20:39:52.222552 chatcmd-1.0.0/pyproject.toml
--rw-r--r--   0        0        0      978 1970-01-01 00:00:00.000000 chatcmd-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-04-26 12:02:06.350462 chatcmd-1.0.1/chatcmd/__init__.py
+-rw-r--r--   0        0        0     1644 2023-05-13 16:35:10.169167 chatcmd-1.0.1/chatcmd/api.py
+-rw-r--r--   0        0        0     3355 2023-05-13 20:44:59.076329 chatcmd-1.0.1/chatcmd/chatcmd.py
+-rw-r--r--   0        0        0     3770 2023-05-02 11:20:31.998824 chatcmd-1.0.1/chatcmd/commands.py
+-rw-r--r--   0        0        0     2147 2023-05-13 16:29:09.346061 chatcmd-1.0.1/chatcmd/helpers.py
+-rw-r--r--   0        0        0   138838 2023-04-26 12:02:06.351951 chatcmd-1.0.1/chatcmd/images/help.png
+-rw-r--r--   0        0        0    76959 2023-04-26 12:02:06.352459 chatcmd-1.0.1/chatcmd/images/library-info.png
+-rw-r--r--   0        0        0    23781 2023-04-26 12:02:06.352705 chatcmd-1.0.1/chatcmd/images/lookup.png
+-rw-r--r--   0        0        0     2615 2023-05-11 23:45:56.420188 chatcmd-1.0.1/chatcmd/lookup.py
+-rw-r--r--   0        0        0     1856 2023-05-13 20:44:59.079013 chatcmd-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0      978 1970-01-01 00:00:00.000000 chatcmd-1.0.1/PKG-INFO
```

### Comparing `chatcmd-1.0.0/chatcmd/api.py` & `chatcmd-1.0.1/chatcmd/api.py`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/chatcmd.py` & `chatcmd-1.0.1/chatcmd/chatcmd.py`

 * *Files 0% similar despite different names*

```diff
@@ -48,15 +48,15 @@
         api_key = get_api_key(conn, cursor)
         if api_key is None:
             api_key = ask_for_api_key(conn, cursor)
 
         openai.api_key = api_key
 
         if args['--version']:
-            print('ChatCMD \033[32m1.0.0\033[0m')
+            print('ChatCMD \033[32m1.0.1\033[0m')
         elif args['--set-key']:
             ask_for_api_key(conn, cursor)
         elif args['--get-key']:
             output_api_key(conn, cursor)
         elif args['--get-cmd']:
             get_cmd(conn, cursor)
         elif args['--get-last']:
```

### Comparing `chatcmd-1.0.0/chatcmd/commands.py` & `chatcmd-1.0.1/chatcmd/commands.py`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/helpers.py` & `chatcmd-1.0.1/chatcmd/helpers.py`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/images/help.png` & `chatcmd-1.0.1/chatcmd/images/help.png`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/images/library-info.png` & `chatcmd-1.0.1/chatcmd/images/library-info.png`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/images/lookup.png` & `chatcmd-1.0.1/chatcmd/images/lookup.png`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/chatcmd/lookup.py` & `chatcmd-1.0.1/chatcmd/lookup.py`

 * *Files identical despite different names*

### Comparing `chatcmd-1.0.0/pyproject.toml` & `chatcmd-1.0.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [build-system]
 requires = ["poetry-core>=1.5.2"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry.dependencies]
 poetry-core = "1.5.2"
-setuptools = "67.7.2"
+setuptools = "44.1.1"
 wheel = "0.40.0"
 pyperclip = "1.8.2"
 docopt = "0.6.2"
 openai = "0.11.5"
 
 [tool.poetry]
 name = "chatcmd"
-version = "1.0.0"
+version = "1.0.1"
 description = "ChatCMD is an AI-driven CLI-based command lookup using ChatGPT to lookup relevant CLI commands based on user input."
 authors = ["Naif Alshaye <naif@naif.io>"]
 [project.license]
 text = "MIT"
 readme = "README.md"
 requires-python = ">=3.7.1"
 classifiers = [
```

### Comparing `chatcmd-1.0.0/PKG-INFO` & `chatcmd-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chatcmd
-Version: 1.0.0
+Version: 1.0.1
 Summary: ChatCMD is an AI-driven CLI-based command lookup using ChatGPT to lookup relevant CLI commands based on user input.
 Author: Naif Alshaye
 Author-email: naif@naif.io
 Classifier: Programming Language :: Python :: 2
 Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.4
@@ -15,9 +15,9 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: docopt (==0.6.2)
 Requires-Dist: openai (==0.11.5)
 Requires-Dist: poetry-core (==1.5.2)
 Requires-Dist: pyperclip (==1.8.2)
-Requires-Dist: setuptools (==67.7.2)
+Requires-Dist: setuptools (==44.1.1)
 Requires-Dist: wheel (==0.40.0)
```

