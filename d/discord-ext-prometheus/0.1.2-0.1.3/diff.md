# Comparing `tmp/discord_ext_prometheus-0.1.2.tar.gz` & `tmp/discord_ext_prometheus-0.1.3.tar.gz`

## Comparing `discord_ext_prometheus-0.1.2.tar` & `discord_ext_prometheus-0.1.3.tar`

### file list

```diff
@@ -1,16 +1,18 @@
--rw-r--r--   0        0        0       74 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/.pylintrc
--rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/requirements.txt
--rw-r--r--   0        0        0     1195 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/.github/workflows/main.yml
--rw-r--r--   0        0        0      245 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/.vscode/settings.json
--rw-r--r--   0        0        0      164 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/discord/ext/prometheus/__init__.py
--rw-r--r--   0        0        0     5120 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/discord/ext/prometheus/prometheus_cog.py
--rw-r--r--   0        0        0      339 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/discord/ext/prometheus/prometheus_logging_handler.py
--rw-r--r--   0        0        0    34682 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/grafana/dashboard.json
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/tests/__init__.py
--rw-r--r--   0        0        0      559 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/tests/test_cog.py
--rw-r--r--   0        0        0      244 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/tests/test_logging.py
--rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/.gitignore
--rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/LICENSE
--rw-r--r--   0        0        0     3219 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/README.md
--rw-r--r--   0        0        0      794 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     3898 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0       75 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.pylintrc
+-rw-r--r--   0        0        0       59 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/requirements.txt
+-rw-r--r--   0        0        0       20 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.github/FUNDING.yml
+-rw-r--r--   0        0        0      780 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.github/workflows/build.yml
+-rw-r--r--   0        0        0      565 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.github/workflows/publish.yml
+-rw-r--r--   0        0        0      245 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.vscode/settings.json
+-rw-r--r--   0        0        0      164 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/discord/ext/prometheus/__init__.py
+-rw-r--r--   0        0        0     5120 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/discord/ext/prometheus/prometheus_cog.py
+-rw-r--r--   0        0        0      339 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/discord/ext/prometheus/prometheus_logging_handler.py
+-rw-r--r--   0        0        0    34682 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/grafana/dashboard.json
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/tests/__init__.py
+-rw-r--r--   0        0        0      559 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/tests/test_cog.py
+-rw-r--r--   0        0        0      244 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/tests/test_logging.py
+-rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/.gitignore
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/LICENSE
+-rw-r--r--   0        0        0     3414 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/README.md
+-rw-r--r--   0        0        0      992 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     4339 2020-02-02 00:00:00.000000 discord_ext_prometheus-0.1.3/PKG-INFO
```

### Comparing `discord_ext_prometheus-0.1.2/discord/ext/prometheus/prometheus_cog.py` & `discord_ext_prometheus-0.1.3/discord/ext/prometheus/prometheus_cog.py`

 * *Files identical despite different names*

### Comparing `discord_ext_prometheus-0.1.2/grafana/dashboard.json` & `discord_ext_prometheus-0.1.3/grafana/dashboard.json`

 * *Files identical despite different names*

### Comparing `discord_ext_prometheus-0.1.2/tests/test_cog.py` & `discord_ext_prometheus-0.1.3/tests/test_cog.py`

 * *Files identical despite different names*

### Comparing `discord_ext_prometheus-0.1.2/.gitignore` & `discord_ext_prometheus-0.1.3/.gitignore`

 * *Files identical despite different names*

### Comparing `discord_ext_prometheus-0.1.2/LICENSE` & `discord_ext_prometheus-0.1.3/LICENSE`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2022 Apollo-Roboto
+Copyright (c) 2023 Apollo-Roboto
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `discord_ext_prometheus-0.1.2/README.md` & `discord_ext_prometheus-0.1.3/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-![PyPi](https://img.shields.io/pypi/v/discord-ext-prometheus.svg)
 
 # discord-ext-prometheus
+![PyPi Version](https://img.shields.io/pypi/v/discord-ext-prometheus.svg) ![PyPI Python Version](https://img.shields.io/pypi/pyversions/discord-ext-prometheus.svg?logo=python&logoColor=gold) ![License MIT](https://img.shields.io/pypi/l/discord-ext-prometheus)
 
 This is a library that makes it easy to add prometheus metrics to your Python Discord bot.
 
 # Installation
 
 ```bash
 pip install discord-ext-prometheus
@@ -91,8 +91,8 @@
 
 ## Change the Prometheus port
 
 The default port is `8000` but can be changed while creating the cog.
 
 ```python
 await bot.add_cog(PrometheusCog(bot, port=7000))
-```
+```
```

### Comparing `discord_ext_prometheus-0.1.2/pyproject.toml` & `discord_ext_prometheus-0.1.3/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,28 +1,33 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "discord-ext-prometheus"
-version = "0.1.2"
+version = "0.1.3"
 authors = [
   { name="Apollo-Roboto", email="Apollo_Roboto@outlook.com" },
 ]
 description  = "An extension for the discord.py library that enables Prometheus metrics"
 readme = "README.md"
 license = "MIT"
 keywords = ["Prometheus", "Discord", "Metrics", "Bot", "Analytics", "Extension"]
 packages = [{ include = "discord" }]
 requires-python = ">=3.10"
 dependencies = [
-	"prometheus-client >= 0.15, < 1",
-	"discord.py >= 2.1.0, < 3",
+	"prometheus-client==0.16.0",
+	"discord.py==2.2.3",
 ]
 classifiers = [
 	"Programming Language :: Python :: 3",
+	"Programming Language :: Python :: 3.10",
 	"License :: OSI Approved :: MIT License",
 	"Operating System :: OS Independent",
+	"Natural Language :: English",
+	"Topic :: Software Development :: Libraries",
+	"Topic :: Software Development :: Libraries :: Python Modules",
+	"Topic :: Utilities",
 ]
 
 [project.urls]
 "Source" = "https://github.com/Apollo-Roboto/discord.py-ext-prometheus"
```

### Comparing `discord_ext_prometheus-0.1.2/PKG-INFO` & `discord_ext_prometheus-0.1.3/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,27 +1,32 @@
 Metadata-Version: 2.1
 Name: discord-ext-prometheus
-Version: 0.1.2
+Version: 0.1.3
 Summary: An extension for the discord.py library that enables Prometheus metrics
 Project-URL: Source, https://github.com/Apollo-Roboto/discord.py-ext-prometheus
 Author-email: Apollo-Roboto <Apollo_Roboto@outlook.com>
 License-Expression: MIT
 License-File: LICENSE
 Keywords: Analytics,Bot,Discord,Extension,Metrics,Prometheus
 Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Topic :: Software Development :: Libraries
+Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Classifier: Topic :: Utilities
 Requires-Python: >=3.10
-Requires-Dist: discord-py<3,>=2.1.0
-Requires-Dist: prometheus-client<1,>=0.15
+Requires-Dist: discord-py==2.2.3
+Requires-Dist: prometheus-client==0.16.0
 Description-Content-Type: text/markdown
 
-![PyPi](https://img.shields.io/pypi/v/discord-ext-prometheus.svg)
 
 # discord-ext-prometheus
+![PyPi Version](https://img.shields.io/pypi/v/discord-ext-prometheus.svg) ![PyPI Python Version](https://img.shields.io/pypi/pyversions/discord-ext-prometheus.svg?logo=python&logoColor=gold) ![License MIT](https://img.shields.io/pypi/l/discord-ext-prometheus)
 
 This is a library that makes it easy to add prometheus metrics to your Python Discord bot.
 
 # Installation
 
 ```bash
 pip install discord-ext-prometheus
@@ -108,8 +113,8 @@
 
 ## Change the Prometheus port
 
 The default port is `8000` but can be changed while creating the cog.
 
 ```python
 await bot.add_cog(PrometheusCog(bot, port=7000))
-```
+```
```

