# Comparing `tmp/mktrader-0.0.4.tar.gz` & `tmp/mktrader-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mktrader-0.0.4.tar", last modified: Sat May 13 15:49:12 2023, max compression
+gzip compressed data, was "mktrader-0.0.5.tar", last modified: Sat May 13 17:50:03 2023, max compression
```

## Comparing `mktrader-0.0.4.tar` & `mktrader-0.0.5.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.401894 mktrader-0.0.4/
--rw-r--r--   0 mmurphy  (433907835) 1133555842     1068 2023-05-11 23:09:55.000000 mktrader-0.0.4/LICENSE
--rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 15:49:12.401731 mktrader-0.0.4/PKG-INFO
--rw-r--r--   0 mmurphy  (433907835) 1133555842      213 2023-05-11 23:10:15.000000 mktrader-0.0.4/README.md
-drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.400484 mktrader-0.0.4/mktrader/
--rw-r--r--   0 mmurphy  (433907835) 1133555842      185 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/__init__.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     5507 2023-05-13 13:56:42.000000 mktrader-0.0.4/mktrader/brokers.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     4300 2023-05-12 03:52:25.000000 mktrader-0.0.4/mktrader/engines.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     6195 2023-05-13 15:23:27.000000 mktrader-0.0.4/mktrader/feeds.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     3894 2023-05-12 03:57:48.000000 mktrader-0.0.4/mktrader/helpers.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     4754 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/indicators.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     1244 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/logger.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     7590 2023-05-13 13:53:12.000000 mktrader-0.0.4/mktrader/models.py
--rw-r--r--   0 mmurphy  (433907835) 1133555842     1055 2023-05-12 03:59:20.000000 mktrader-0.0.4/mktrader/strategies.py
-drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.401511 mktrader-0.0.4/mktrader.egg-info/
--rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/PKG-INFO
--rw-r--r--   0 mmurphy  (433907835) 1133555842      368 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/SOURCES.txt
--rw-r--r--   0 mmurphy  (433907835) 1133555842        1 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/dependency_links.txt
--rw-r--r--   0 mmurphy  (433907835) 1133555842       26 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/requires.txt
--rw-r--r--   0 mmurphy  (433907835) 1133555842        9 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/top_level.txt
--rw-r--r--   0 mmurphy  (433907835) 1133555842       38 2023-05-13 15:49:12.401939 mktrader-0.0.4/setup.cfg
--rw-r--r--   0 mmurphy  (433907835) 1133555842     1017 2023-05-13 15:33:41.000000 mktrader-0.0.4/setup.py
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 17:50:03.184641 mktrader-0.0.5/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1068 2023-05-11 23:09:55.000000 mktrader-0.0.5/LICENSE
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 17:50:03.184512 mktrader-0.0.5/PKG-INFO
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      213 2023-05-11 23:10:15.000000 mktrader-0.0.5/README.md
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 17:50:03.183627 mktrader-0.0.5/mktrader/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      185 2023-05-11 23:10:15.000000 mktrader-0.0.5/mktrader/__init__.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     5507 2023-05-13 13:56:42.000000 mktrader-0.0.5/mktrader/brokers.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     4300 2023-05-12 03:52:25.000000 mktrader-0.0.5/mktrader/engines.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     6389 2023-05-13 17:46:41.000000 mktrader-0.0.5/mktrader/feeds.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     3894 2023-05-12 03:57:48.000000 mktrader-0.0.5/mktrader/helpers.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     4754 2023-05-11 23:10:15.000000 mktrader-0.0.5/mktrader/indicators.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1244 2023-05-11 23:10:15.000000 mktrader-0.0.5/mktrader/logger.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     7590 2023-05-13 13:53:12.000000 mktrader-0.0.5/mktrader/models.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1055 2023-05-12 03:59:20.000000 mktrader-0.0.5/mktrader/strategies.py
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 17:50:03.184324 mktrader-0.0.5/mktrader.egg-info/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 17:50:03.000000 mktrader-0.0.5/mktrader.egg-info/PKG-INFO
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      368 2023-05-13 17:50:03.000000 mktrader-0.0.5/mktrader.egg-info/SOURCES.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842        1 2023-05-13 17:50:03.000000 mktrader-0.0.5/mktrader.egg-info/dependency_links.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842       26 2023-05-13 17:50:03.000000 mktrader-0.0.5/mktrader.egg-info/requires.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842        9 2023-05-13 17:50:03.000000 mktrader-0.0.5/mktrader.egg-info/top_level.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842       38 2023-05-13 17:50:03.184679 mktrader-0.0.5/setup.cfg
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1017 2023-05-13 17:48:29.000000 mktrader-0.0.5/setup.py
```

### Comparing `mktrader-0.0.4/LICENSE` & `mktrader-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/PKG-INFO` & `mktrader-0.0.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mktrader
-Version: 0.0.4
+Version: 0.0.5
 Summary: Stock Market Trading Framework
 Home-page: https://github.com/matthewkurtis/mktrader.git
 Author: Matthew K Murphy (MatthewKurtis)
 Author-email: <mkmurphy526@gmail.com>
 Keywords: python,trading,stock,market
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Financial and Insurance Industry
```

### Comparing `mktrader-0.0.4/mktrader/brokers.py` & `mktrader-0.0.5/mktrader/brokers.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/engines.py` & `mktrader-0.0.5/mktrader/engines.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/feeds.py` & `mktrader-0.0.5/mktrader/feeds.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,31 +54,36 @@
                 start = (datetime.utcnow() - timedelta(minutes=1000)).strftime("%Y-%m-%dT%H:%M:%SZ")
             elif time_period == "Hour":
                 start = (datetime.utcnow() - timedelta(hours=1000)).strftime("%Y-%m-%dT%H:%M:%SZ")
             url = f"{url}&start={start}"
             logger.debug(f"URL = {url}")
             logger.debug(f"fetching candles from {url}")
             response = requests.get(url=url, headers=headers)
-            json_response = response.json() 
+            json_response = response.json()
+            if json_response["bars"] is None:
+                print("no bars after 1000 latest pulled.. skipping")
         candles = []
+
+
         if self.engine.asset.asset_class == "us_equity":
             bars_list = json_response["bars"]
         elif self.engine.asset.asset_class == "crypto":
             bars_list = json_response["bars"][self.engine.asset.symbol]
-        for bar in bars_list:
-            candle = Candle(
-                ticker=self.engine.asset.symbol,
-                date=datetime.strptime(bar['t'], "%Y-%m-%dT%H:%M:%SZ"),
-                open=bar["o"],
-                high=bar["h"],
-                low=bar["l"],
-                close=bar["c"],
-                volume=bar["v"]
-            )
-            candles.append(candle)
+        if json_response["bars"]:
+            for bar in bars_list:
+                candle = Candle(
+                    ticker=self.engine.asset.symbol,
+                    date=datetime.strptime(bar['t'], "%Y-%m-%dT%H:%M:%SZ"),
+                    open=bar["o"],
+                    high=bar["h"],
+                    low=bar["l"],
+                    close=bar["c"],
+                    volume=bar["v"]
+                )
+                candles.append(candle)
 
         if minute_catch_up is not None:
             print(f"MINUTE CATCH UP: {minute_catch_up}")
             minute_candles = [candle for candle in candles if candle.date >= minute_catch_up]
             for minute_candle in minute_candles:
                 if minute_candle.date.minute == datetime.utcnow().minute:
                     print(f"IN PROCESS, REMOVING: {minute_candle}")
```

### Comparing `mktrader-0.0.4/mktrader/helpers.py` & `mktrader-0.0.5/mktrader/helpers.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/indicators.py` & `mktrader-0.0.5/mktrader/indicators.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/logger.py` & `mktrader-0.0.5/mktrader/logger.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/models.py` & `mktrader-0.0.5/mktrader/models.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader/strategies.py` & `mktrader-0.0.5/mktrader/strategies.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.4/mktrader.egg-info/PKG-INFO` & `mktrader-0.0.5/mktrader.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mktrader
-Version: 0.0.4
+Version: 0.0.5
 Summary: Stock Market Trading Framework
 Home-page: https://github.com/matthewkurtis/mktrader.git
 Author: Matthew K Murphy (MatthewKurtis)
 Author-email: <mkmurphy526@gmail.com>
 Keywords: python,trading,stock,market
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Financial and Insurance Industry
```

### Comparing `mktrader-0.0.4/setup.py` & `mktrader-0.0.5/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '0.0.4'
+VERSION = '0.0.5'
 DESCRIPTION = 'Stock Market Trading Framework'
 LONG_DESCRIPTION = 'A Framework for simple creation and deployment of trading strategies.'
 
 # Setting up
 setup(
     name="mktrader",
     version=VERSION,
```

