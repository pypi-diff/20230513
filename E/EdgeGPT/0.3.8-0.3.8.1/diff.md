# Comparing `tmp/EdgeGPT-0.3.8.tar.gz` & `tmp/EdgeGPT-0.3.8.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "EdgeGPT-0.3.8.tar", last modified: Wed May 10 05:53:50 2023, max compression
+gzip compressed data, was "EdgeGPT-0.3.8.1.tar", last modified: Sat May 13 12:54:23 2023, max compression
```

## Comparing `EdgeGPT-0.3.8.tar` & `EdgeGPT-0.3.8.1.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 05:53:50.322965 EdgeGPT-0.3.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-10 05:53:19.000000 EdgeGPT-0.3.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     8273 2023-05-10 05:53:50.322965 EdgeGPT-0.3.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     7508 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-10 05:53:50.322965 EdgeGPT-0.3.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1644 2023-05-10 05:53:19.000000 EdgeGPT-0.3.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 05:53:50.318965 EdgeGPT-0.3.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 05:53:50.318965 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     8273 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      279 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-10 05:53:50.000000 EdgeGPT-0.3.8/src/EdgeGPT.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)    29675 2023-05-10 05:53:19.000000 EdgeGPT-0.3.8/src/EdgeGPT.py
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-10 05:53:19.000000 EdgeGPT-0.3.8/src/ImageGen.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:54:23.450954 EdgeGPT-0.3.8.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-13 12:53:51.000000 EdgeGPT-0.3.8.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     8275 2023-05-13 12:54:23.450954 EdgeGPT-0.3.8.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7508 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-13 12:54:23.450954 EdgeGPT-0.3.8.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-05-13 12:53:51.000000 EdgeGPT-0.3.8.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:54:23.446954 EdgeGPT-0.3.8.1/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:54:23.450954 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8275 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 12:54:23.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    29710 2023-05-13 12:53:51.000000 EdgeGPT-0.3.8.1/src/EdgeGPT.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-13 12:53:51.000000 EdgeGPT-0.3.8.1/src/ImageGen.py
```

### Comparing `EdgeGPT-0.3.8/LICENSE` & `EdgeGPT-0.3.8.1/LICENSE`

 * *Files identical despite different names*

### Comparing `EdgeGPT-0.3.8/PKG-INFO` & `EdgeGPT-0.3.8.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: EdgeGPT
-Version: 0.3.8
+Version: 0.3.8.1
 Summary: Reverse engineered Edge Chat API
 Home-page: https://github.com/acheong08/EdgeGPT
 Author: Antonio Cheong
 Author-email: acheong@student.dalat.org
 License: GNU General Public License v2.0
 Project-URL: Bug Report, https://github.com/acheong08/EdgeGPT/issues/new
 Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
```

#### html2text {}

```diff
@@ -1,17 +1,18 @@
-Metadata-Version: 2.1 Name: EdgeGPT Version: 0.3.8 Summary: Reverse engineered
-Edge Chat API Home-page: https://github.com/acheong08/EdgeGPT Author: Antonio
-Cheong Author-email: acheong@student.dalat.org License: GNU General Public
-License v2.0 Project-URL: Bug Report, https://github.com/acheong08/EdgeGPT/
-issues/new Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
-Classifier: Intended Audience :: Developers Classifier: Topic :: Software
-Development :: Libraries :: Python Modules Classifier: Programming Language ::
-Python :: 3.8 Classifier: Programming Language :: Python :: 3.9 Classifier:
-Programming Language :: Python :: 3.10 Classifier: Programming Language ::
-Python :: 3.11 Description-Content-Type: text/markdown License-File: LICENSE
+Metadata-Version: 2.1 Name: EdgeGPT Version: 0.3.8.1 Summary: Reverse
+engineered Edge Chat API Home-page: https://github.com/acheong08/EdgeGPT
+Author: Antonio Cheong Author-email: acheong@student.dalat.org License: GNU
+General Public License v2.0 Project-URL: Bug Report, https://github.com/
+acheong08/EdgeGPT/issues/new Classifier: License :: OSI Approved :: The
+Unlicense (Unlicense) Classifier: Intended Audience :: Developers Classifier:
+Topic :: Software Development :: Libraries :: Python Modules Classifier:
+Programming Language :: Python :: 3.8 Classifier: Programming Language ::
+Python :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
+Programming Language :: Python :: 3.11 Description-Content-Type: text/markdown
+License-File: LICENSE
    [EdgeGPT] # Edge GPT _The reverse engineering the chat feature of the new
     version of Bing_ English - ç®ä½ä¸­æ - ç¹é«ä¸­æ_(ä¸­åèºç£) -
                              EspaÃ±ol - æ¥æ¬èª
                [PyPI_version] [Python version] [Total downloads]
 --- ## Setup ### Install package ```bash python3 -m pip install EdgeGPT --
 upgrade ``` ### Requirements - python 3.8+ - A Microsoft Account with early
 access to
```

### Comparing `EdgeGPT-0.3.8/README.md` & `EdgeGPT-0.3.8.1/README.md`

 * *Files identical despite different names*

### Comparing `EdgeGPT-0.3.8/setup.py` & `EdgeGPT-0.3.8.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 if not PATH.exists():
     with open(DOCS_PATH, encoding="utf-8") as f1:
         with open(PATH, "w+", encoding="utf-8") as f2:
             f2.write(f1.read())
 
 setup(
     name="EdgeGPT",
-    version="0.3.8",
+    version="0.3.8.1",
     license="GNU General Public License v2.0",
     author="Antonio Cheong",
     author_email="acheong@student.dalat.org",
     description="Reverse engineered Edge Chat API",
     packages=find_packages("src"),
     package_dir={"": "src"},
     url="https://github.com/acheong08/EdgeGPT",
```

### Comparing `EdgeGPT-0.3.8/src/EdgeGPT.egg-info/PKG-INFO` & `EdgeGPT-0.3.8.1/src/EdgeGPT.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: EdgeGPT
-Version: 0.3.8
+Version: 0.3.8.1
 Summary: Reverse engineered Edge Chat API
 Home-page: https://github.com/acheong08/EdgeGPT
 Author: Antonio Cheong
 Author-email: acheong@student.dalat.org
 License: GNU General Public License v2.0
 Project-URL: Bug Report, https://github.com/acheong08/EdgeGPT/issues/new
 Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
```

#### html2text {}

```diff
@@ -1,17 +1,18 @@
-Metadata-Version: 2.1 Name: EdgeGPT Version: 0.3.8 Summary: Reverse engineered
-Edge Chat API Home-page: https://github.com/acheong08/EdgeGPT Author: Antonio
-Cheong Author-email: acheong@student.dalat.org License: GNU General Public
-License v2.0 Project-URL: Bug Report, https://github.com/acheong08/EdgeGPT/
-issues/new Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
-Classifier: Intended Audience :: Developers Classifier: Topic :: Software
-Development :: Libraries :: Python Modules Classifier: Programming Language ::
-Python :: 3.8 Classifier: Programming Language :: Python :: 3.9 Classifier:
-Programming Language :: Python :: 3.10 Classifier: Programming Language ::
-Python :: 3.11 Description-Content-Type: text/markdown License-File: LICENSE
+Metadata-Version: 2.1 Name: EdgeGPT Version: 0.3.8.1 Summary: Reverse
+engineered Edge Chat API Home-page: https://github.com/acheong08/EdgeGPT
+Author: Antonio Cheong Author-email: acheong@student.dalat.org License: GNU
+General Public License v2.0 Project-URL: Bug Report, https://github.com/
+acheong08/EdgeGPT/issues/new Classifier: License :: OSI Approved :: The
+Unlicense (Unlicense) Classifier: Intended Audience :: Developers Classifier:
+Topic :: Software Development :: Libraries :: Python Modules Classifier:
+Programming Language :: Python :: 3.8 Classifier: Programming Language ::
+Python :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
+Programming Language :: Python :: 3.11 Description-Content-Type: text/markdown
+License-File: LICENSE
    [EdgeGPT] # Edge GPT _The reverse engineering the chat feature of the new
     version of Bing_ English - ç®ä½ä¸­æ - ç¹é«ä¸­æ_(ä¸­åèºç£) -
                              EspaÃ±ol - æ¥æ¬èª
                [PyPI_version] [Python version] [Total downloads]
 --- ## Setup ### Install package ```bash python3 -m pip install EdgeGPT --
 upgrade ``` ### Requirements - python 3.8+ - A Microsoft Account with early
 access to
```

### Comparing `EdgeGPT-0.3.8/src/EdgeGPT.py` & `EdgeGPT-0.3.8.1/src/EdgeGPT.py`

 * *Files 1% similar despite different names*

```diff
@@ -685,15 +685,17 @@
         await self.chat_hub.close()
 
     async def reset(self) -> None:
         """
         Reset the conversation
         """
         await self.close()
-        self.chat_hub = _ChatHub(await _Conversation.create(self.cookies))
+        self.chat_hub = _ChatHub(
+            await _Conversation.create(self.cookies, self.proxy),
+        )
 
 
 async def _get_input_async(
     session: PromptSession = None,
     completer: WordCompleter = None,
 ) -> str:
     """
```

