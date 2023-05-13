# Comparing `tmp/signalation-0.0.0.tar.gz` & `tmp/signalation-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "signalation-0.0.0.tar", last modified: Sat May 13 09:00:23 2023, max compression
+gzip compressed data, was "signalation-1.0.0.tar", last modified: Sat May 13 09:14:58 2023, max compression
```

## Comparing `signalation-0.0.0.tar` & `signalation-1.0.0.tar`

### file list

```diff
@@ -1,28 +1,28 @@
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.308564 signalation-0.0.0/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     1064 2023-05-13 08:59:12.000000 signalation-0.0.0/LICENSE
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     9259 2023-05-13 09:00:23.308564 signalation-0.0.0/PKG-INFO
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     7523 2023-05-13 08:59:12.000000 signalation-0.0.0/README.md
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     1451 2023-05-13 08:59:12.000000 signalation-0.0.0/pyproject.toml
--rw-rw-r--   0 borea17   (1000) borea17   (1000)       38 2023-05-13 09:00:23.308564 signalation-0.0.0/setup.cfg
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.304564 signalation-0.0.0/src/
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.304564 signalation-0.0.0/src/signalation/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)        0 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/__init__.py
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.304564 signalation-0.0.0/src/signalation/conf/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)        0 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/conf/__init__.py
--rw-rw-r--   0 borea17   (1000) borea17   (1000)      374 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/conf/logger.py
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     2021 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/conf/logging_config.yaml
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     1086 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/conf/settings.py
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.308564 signalation-0.0.0/src/signalation/entities/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)        0 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/entities/__init__.py
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     2401 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/entities/attachment.py
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     4393 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/entities/signal_message.py
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.308564 signalation-0.0.0/src/signalation/services/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)        0 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/services/__init__.py
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     7596 2023-05-13 08:59:12.000000 signalation-0.0.0/src/signalation/services/producer.py
-drwxrwxr-x   0 borea17   (1000) borea17   (1000)        0 2023-05-13 09:00:23.304564 signalation-0.0.0/src/signalation.egg-info/
--rw-rw-r--   0 borea17   (1000) borea17   (1000)     9259 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/PKG-INFO
--rw-rw-r--   0 borea17   (1000) borea17   (1000)      627 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/SOURCES.txt
--rw-rw-r--   0 borea17   (1000) borea17   (1000)        1 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/dependency_links.txt
--rw-rw-r--   0 borea17   (1000) borea17   (1000)       76 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/entry_points.txt
--rw-rw-r--   0 borea17   (1000) borea17   (1000)      310 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/requires.txt
--rw-rw-r--   0 borea17   (1000) borea17   (1000)       12 2023-05-13 09:00:23.000000 signalation-0.0.0/src/signalation.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 09:14:44.000000 signalation-1.0.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     9573 2023-05-13 09:14:58.235059 signalation-1.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7837 2023-05-13 09:14:44.000000 signalation-1.0.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-05-13 09:14:44.000000 signalation-1.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:14:58.235059 signalation-1.0.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.231059 signalation-1.0.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/src/signalation/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/src/signalation/conf/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/conf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      374 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/conf/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2021 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/conf/logging_config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1086 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/conf/settings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/src/signalation/entities/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/entities/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2401 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/entities/attachment.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4393 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/entities/signal_message.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/src/signalation/services/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/services/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7596 2023-05-13 09:14:44.000000 signalation-1.0.0/src/signalation/services/producer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:14:58.235059 signalation-1.0.0/src/signalation.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9573 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      627 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       76 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 09:14:58.000000 signalation-1.0.0/src/signalation.egg-info/top_level.txt
```

### Comparing `signalation-0.0.0/LICENSE` & `signalation-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/PKG-INFO` & `signalation-1.0.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: signalation
-Version: 0.0.0
+Version: 1.0.0
 Summary: Produce your messages from your signal account to kafka.
 Author-email: Markus Borea <borea17@protonmail.com>
 License: MIT License
         
         Copyright (c) 2023 borea17
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -32,15 +32,15 @@
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # signal-kafka-producer a.k.a. signalation
 
-[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml)
+[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml) [![Python Publish](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-publish.yml) [![PyPI version](https://badge.fury.io/py/signalation.svg)](https://badge.fury.io/py/signalation)
 
 **[Motivation](https://github.com/borea17/signal-kafka-producer#motivation---why-should-i-use-it)** | **[Installation](https://github.com/borea17/signal-kafka-producer#installation---how-can-i-use-it)** | **[Implementation Details](https://github.com/borea17/signal-kafka-producer#implementation-details---how-does-it-work)**
 
 Python package to produce messages from your [signal](https://signal.org/) account to [kafka](https://kafka.apache.org/)
 by querying the [dockerized signal messenger API](https://github.com/bbernhard/signal-cli-rest-api).
 
 ## Motivation - Why should I use it?
```

### Comparing `signalation-0.0.0/README.md` & `signalation-1.0.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # signal-kafka-producer a.k.a. signalation
 
-[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml)
+[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml) [![Python Publish](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-publish.yml) [![PyPI version](https://badge.fury.io/py/signalation.svg)](https://badge.fury.io/py/signalation)
 
 **[Motivation](https://github.com/borea17/signal-kafka-producer#motivation---why-should-i-use-it)** | **[Installation](https://github.com/borea17/signal-kafka-producer#installation---how-can-i-use-it)** | **[Implementation Details](https://github.com/borea17/signal-kafka-producer#implementation-details---how-does-it-work)**
 
 Python package to produce messages from your [signal](https://signal.org/) account to [kafka](https://kafka.apache.org/)
 by querying the [dockerized signal messenger API](https://github.com/bbernhard/signal-cli-rest-api).
 
 ## Motivation - Why should I use it?
```

### Comparing `signalation-0.0.0/pyproject.toml` & `signalation-1.0.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "signalation"
-version = "0.0.0"
+version = "1.0.0"
 description = "Produce your messages from your signal account to kafka."
 readme = "README.md"
 authors = [{name="Markus Borea", email="borea17@protonmail.com"}]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

### Comparing `signalation-0.0.0/src/signalation/conf/logging_config.yaml` & `signalation-1.0.0/src/signalation/conf/logging_config.yaml`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/src/signalation/conf/settings.py` & `signalation-1.0.0/src/signalation/conf/settings.py`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/src/signalation/entities/attachment.py` & `signalation-1.0.0/src/signalation/entities/attachment.py`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/src/signalation/entities/signal_message.py` & `signalation-1.0.0/src/signalation/entities/signal_message.py`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/src/signalation/services/producer.py` & `signalation-1.0.0/src/signalation/services/producer.py`

 * *Files identical despite different names*

### Comparing `signalation-0.0.0/src/signalation.egg-info/PKG-INFO` & `signalation-1.0.0/src/signalation.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: signalation
-Version: 0.0.0
+Version: 1.0.0
 Summary: Produce your messages from your signal account to kafka.
 Author-email: Markus Borea <borea17@protonmail.com>
 License: MIT License
         
         Copyright (c) 2023 borea17
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -32,15 +32,15 @@
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # signal-kafka-producer a.k.a. signalation
 
-[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml)
+[![Python package](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml) [![Python Publish](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-package.yml/badge.svg?branch=main)](https://github.com/borea17/signal-kafka-producer/actions/workflows/python-publish.yml) [![PyPI version](https://badge.fury.io/py/signalation.svg)](https://badge.fury.io/py/signalation)
 
 **[Motivation](https://github.com/borea17/signal-kafka-producer#motivation---why-should-i-use-it)** | **[Installation](https://github.com/borea17/signal-kafka-producer#installation---how-can-i-use-it)** | **[Implementation Details](https://github.com/borea17/signal-kafka-producer#implementation-details---how-does-it-work)**
 
 Python package to produce messages from your [signal](https://signal.org/) account to [kafka](https://kafka.apache.org/)
 by querying the [dockerized signal messenger API](https://github.com/bbernhard/signal-cli-rest-api).
 
 ## Motivation - Why should I use it?
```

### Comparing `signalation-0.0.0/src/signalation.egg-info/SOURCES.txt` & `signalation-1.0.0/src/signalation.egg-info/SOURCES.txt`

 * *Files identical despite different names*

