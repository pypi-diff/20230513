# Comparing `tmp/v4xyz-0.0.2.tar.gz` & `tmp/v4xyz-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "v4xyz-0.0.2.tar", last modified: Sat May 13 11:21:02 2023, max compression
+gzip compressed data, was "v4xyz-0.0.3.tar", last modified: Sat May 13 11:38:00 2023, max compression
```

## Comparing `v4xyz-0.0.2.tar` & `v4xyz-0.0.3.tar`

### file list

```diff
@@ -1,13 +1,14 @@
-drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:21:02.041088 v4xyz-0.0.2/
--rw-r--r--   0 john      (1000) john      (1000)     2305 2023-05-13 11:21:02.041088 v4xyz-0.0.2/PKG-INFO
--rw-r--r--   0 john      (1000) john      (1000)     1236 2023-05-13 11:01:36.000000 v4xyz-0.0.2/README.md
--rw-r--r--   0 john      (1000) john      (1000)       38 2023-05-13 11:21:02.041088 v4xyz-0.0.2/setup.cfg
--rw-r--r--   0 john      (1000) john      (1000)     1358 2023-05-13 11:20:46.000000 v4xyz-0.0.2/setup.py
--rw-r--r--   0 john      (1000) john      (1000)     4952 2023-05-13 11:19:45.000000 v4xyz-0.0.2/v4.py
-drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:21:02.041088 v4xyz-0.0.2/v4xyz.egg-info/
--rw-r--r--   0 john      (1000) john      (1000)     2305 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/PKG-INFO
--rw-r--r--   0 john      (1000) john      (1000)      200 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/SOURCES.txt
--rw-r--r--   0 john      (1000) john      (1000)        1 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/dependency_links.txt
--rw-r--r--   0 john      (1000) john      (1000)       32 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/entry_points.txt
--rw-r--r--   0 john      (1000) john      (1000)       41 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/requires.txt
--rw-r--r--   0 john      (1000) john      (1000)        3 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/top_level.txt
+drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:38:00.341093 v4xyz-0.0.3/
+-rw-r--r--   0 john      (1000) john      (1000)    11540 2023-05-13 11:27:28.000000 v4xyz-0.0.3/LICENSE
+-rw-r--r--   0 john      (1000) john      (1000)     3037 2023-05-13 11:38:00.341093 v4xyz-0.0.3/PKG-INFO
+-rw-r--r--   0 john      (1000) john      (1000)     1793 2023-05-13 11:37:16.000000 v4xyz-0.0.3/README.md
+-rw-r--r--   0 john      (1000) john      (1000)       38 2023-05-13 11:38:00.341093 v4xyz-0.0.3/setup.cfg
+-rw-r--r--   0 john      (1000) john      (1000)     1347 2023-05-13 11:29:25.000000 v4xyz-0.0.3/setup.py
+-rw-r--r--   0 john      (1000) john      (1000)     4952 2023-05-13 11:19:45.000000 v4xyz-0.0.3/v4.py
+drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:38:00.341093 v4xyz-0.0.3/v4xyz.egg-info/
+-rw-r--r--   0 john      (1000) john      (1000)     3037 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/PKG-INFO
+-rw-r--r--   0 john      (1000) john      (1000)      208 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/SOURCES.txt
+-rw-r--r--   0 john      (1000) john      (1000)        1 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/dependency_links.txt
+-rw-r--r--   0 john      (1000) john      (1000)       32 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/entry_points.txt
+-rw-r--r--   0 john      (1000) john      (1000)       41 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/requires.txt
+-rw-r--r--   0 john      (1000) john      (1000)        3 2023-05-13 11:38:00.000000 v4xyz-0.0.3/v4xyz.egg-info/top_level.txt
```

### Comparing `v4xyz-0.0.2/PKG-INFO` & `v4xyz-0.0.3/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,56 +1,81 @@
 Metadata-Version: 2.1
 Name: v4xyz
-Version: 0.0.2
+Version: 0.0.3
 Summary: A command line tool to chat with GPT4 and render markdown response.
 Home-page: https://github.com/imhuwq/v4xyz
 Author: imhuwq
 Author-email: imhuwq@gmail.com
 License: UNKNOWN
 Description: # v4xyz
         
         ---
+        <div align="center">
+        <p align="center">
+        
+        <!-- prettier-ignore -->
+        
+        **A command line tool to chat with GPT4 and render markdown response.**
+        
+        ---
+        ![PyPI - Python Version](https://img.shields.io/pypi/pyversions/v4xyz?style=social)
+        ![PyPI](https://img.shields.io/pypi/v/v4xyz?style=social)
+        ![PyPI - Downloads](https://img.shields.io/pypi/dm/v4xyz?style=social)
+        ![PyPI - License](https://img.shields.io/pypi/l/v4xyz?style=social)
+        
         ```
          ______   __    _              _             __    __            _      __             
         /_  __/  / /   (_)  ___       (_)  ___      / /_  / /  ___      | | /| / / ___ _  __ __
          / /    / _ \ / /  (_-<      / /  (_-<     / __/ / _ \/ -_)     | |/ |/ / / _ `/ / // /
         /_/    /_//_//_/  /___/     /_/  /___/     \__/ /_//_/\__/      |__/|__/  \_,_/  \_, / 
                                                                                         /___/  
         ```
-        A command line tool to chat with GPT4 and render markdown response.
+        
+        </p>
+        </div>
         
         ## 1. Installation
+        
         ### 1.1 Installing from pypi
+        
         ```shell
         pip install v4xyz
         ```
         
         ### 1.2 Installing from github
+        
         ```shell
         git clone https://github.com/imhuwq/v4xyz
         cd v4xyz
         python setup.py install
         ```
         
         ## 2. Setup config
+        
         Once you have `v4xyz` installed, you have to config the OpenAI API key and the proxies if necessary.
+        
         ```shell
         v4 -e # this will open the config file with your editor
         ```
         
         The config file is on json format:
+        
         ```json
         {
           "openai_secret": "",
           "http_proxy": "",
           "https_proxy": ""
         }
         ```
         
+        The `openai_secret` must be set to your OpenAI key.   
+        The `http_proxy` and `https_proxy` are optional if the OpenAI API is accessible from your region.
+        
         ## 3. Chat with GPT4 in Terminal
+        
         ```shell
         v4 'How to config a reverse proxy with Nginx?'
         v4 'send a HTTP GET request using telnet'
         v4 'any thing here'
         ```
         
 Platform: UNKNOWN
```

### Comparing `v4xyz-0.0.2/setup.py` & `v4xyz-0.0.3/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,10 @@
-import os
 from setuptools import setup
 
-version = "0.0.2"
+version = "0.0.3"
 description = "A command line tool to chat with GPT4 and render markdown response."
 with open("README.md") as fp:
     long_description = fp.read()
 url = "https://github.com/imhuwq/v4xyz"
 author = "imhuwq"
 author_email = "imhuwq@gmail.com"
 classifiers = [
```

### Comparing `v4xyz-0.0.2/v4.py` & `v4xyz-0.0.3/v4.py`

 * *Files identical despite different names*

### Comparing `v4xyz-0.0.2/v4xyz.egg-info/PKG-INFO` & `v4xyz-0.0.3/v4xyz.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,56 +1,81 @@
 Metadata-Version: 2.1
 Name: v4xyz
-Version: 0.0.2
+Version: 0.0.3
 Summary: A command line tool to chat with GPT4 and render markdown response.
 Home-page: https://github.com/imhuwq/v4xyz
 Author: imhuwq
 Author-email: imhuwq@gmail.com
 License: UNKNOWN
 Description: # v4xyz
         
         ---
+        <div align="center">
+        <p align="center">
+        
+        <!-- prettier-ignore -->
+        
+        **A command line tool to chat with GPT4 and render markdown response.**
+        
+        ---
+        ![PyPI - Python Version](https://img.shields.io/pypi/pyversions/v4xyz?style=social)
+        ![PyPI](https://img.shields.io/pypi/v/v4xyz?style=social)
+        ![PyPI - Downloads](https://img.shields.io/pypi/dm/v4xyz?style=social)
+        ![PyPI - License](https://img.shields.io/pypi/l/v4xyz?style=social)
+        
         ```
          ______   __    _              _             __    __            _      __             
         /_  __/  / /   (_)  ___       (_)  ___      / /_  / /  ___      | | /| / / ___ _  __ __
          / /    / _ \ / /  (_-<      / /  (_-<     / __/ / _ \/ -_)     | |/ |/ / / _ `/ / // /
         /_/    /_//_//_/  /___/     /_/  /___/     \__/ /_//_/\__/      |__/|__/  \_,_/  \_, / 
                                                                                         /___/  
         ```
-        A command line tool to chat with GPT4 and render markdown response.
+        
+        </p>
+        </div>
         
         ## 1. Installation
+        
         ### 1.1 Installing from pypi
+        
         ```shell
         pip install v4xyz
         ```
         
         ### 1.2 Installing from github
+        
         ```shell
         git clone https://github.com/imhuwq/v4xyz
         cd v4xyz
         python setup.py install
         ```
         
         ## 2. Setup config
+        
         Once you have `v4xyz` installed, you have to config the OpenAI API key and the proxies if necessary.
+        
         ```shell
         v4 -e # this will open the config file with your editor
         ```
         
         The config file is on json format:
+        
         ```json
         {
           "openai_secret": "",
           "http_proxy": "",
           "https_proxy": ""
         }
         ```
         
+        The `openai_secret` must be set to your OpenAI key.   
+        The `http_proxy` and `https_proxy` are optional if the OpenAI API is accessible from your region.
+        
         ## 3. Chat with GPT4 in Terminal
+        
         ```shell
         v4 'How to config a reverse proxy with Nginx?'
         v4 'send a HTTP GET request using telnet'
         v4 'any thing here'
         ```
         
 Platform: UNKNOWN
```

