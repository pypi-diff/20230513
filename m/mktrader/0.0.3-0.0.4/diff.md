# Comparing `tmp/mktrader-0.0.3.tar.gz` & `tmp/mktrader-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mktrader-0.0.3.tar", last modified: Fri May 12 04:02:34 2023, max compression
+gzip compressed data, was "mktrader-0.0.4.tar", last modified: Sat May 13 15:49:12 2023, max compression
```

## Comparing `mktrader-0.0.3.tar` & `mktrader-0.0.4.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)        0 2023-05-12 04:02:34.987712 mktrader-0.0.3/
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     1068 2023-05-11 23:09:55.000000 mktrader-0.0.3/LICENSE
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)      699 2023-05-12 04:02:34.987549 mktrader-0.0.3/PKG-INFO
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)      213 2023-05-11 23:10:15.000000 mktrader-0.0.3/README.md
-drwxr-xr-x   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)        0 2023-05-12 04:02:34.986477 mktrader-0.0.3/mktrader/
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)      185 2023-05-11 23:10:15.000000 mktrader-0.0.3/mktrader/__init__.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     3893 2023-05-12 03:48:43.000000 mktrader-0.0.3/mktrader/brokers.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     4300 2023-05-12 03:52:25.000000 mktrader-0.0.3/mktrader/engines.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     5510 2023-05-12 03:56:07.000000 mktrader-0.0.3/mktrader/feeds.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     3894 2023-05-12 03:57:48.000000 mktrader-0.0.3/mktrader/helpers.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     4754 2023-05-11 23:10:15.000000 mktrader-0.0.3/mktrader/indicators.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     1244 2023-05-11 23:10:15.000000 mktrader-0.0.3/mktrader/logger.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     7290 2023-05-12 03:40:29.000000 mktrader-0.0.3/mktrader/models.py
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     1055 2023-05-12 03:59:20.000000 mktrader-0.0.3/mktrader/strategies.py
-drwxr-xr-x   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)        0 2023-05-12 04:02:34.987338 mktrader-0.0.3/mktrader.egg-info/
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)      699 2023-05-12 04:02:34.000000 mktrader-0.0.3/mktrader.egg-info/PKG-INFO
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)      368 2023-05-12 04:02:34.000000 mktrader-0.0.3/mktrader.egg-info/SOURCES.txt
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)        1 2023-05-12 04:02:34.000000 mktrader-0.0.3/mktrader.egg-info/dependency_links.txt
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)       26 2023-05-12 04:02:34.000000 mktrader-0.0.3/mktrader.egg-info/requires.txt
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)        9 2023-05-12 04:02:34.000000 mktrader-0.0.3/mktrader.egg-info/top_level.txt
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)       38 2023-05-12 04:02:34.987764 mktrader-0.0.3/setup.cfg
--rw-r--r--   0 mmurphy  (433907835) CHCS\Domain Users (1133555842)     1017 2023-05-12 03:45:07.000000 mktrader-0.0.3/setup.py
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.401894 mktrader-0.0.4/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1068 2023-05-11 23:09:55.000000 mktrader-0.0.4/LICENSE
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 15:49:12.401731 mktrader-0.0.4/PKG-INFO
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      213 2023-05-11 23:10:15.000000 mktrader-0.0.4/README.md
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.400484 mktrader-0.0.4/mktrader/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      185 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/__init__.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     5507 2023-05-13 13:56:42.000000 mktrader-0.0.4/mktrader/brokers.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     4300 2023-05-12 03:52:25.000000 mktrader-0.0.4/mktrader/engines.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     6195 2023-05-13 15:23:27.000000 mktrader-0.0.4/mktrader/feeds.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     3894 2023-05-12 03:57:48.000000 mktrader-0.0.4/mktrader/helpers.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     4754 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/indicators.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1244 2023-05-11 23:10:15.000000 mktrader-0.0.4/mktrader/logger.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     7590 2023-05-13 13:53:12.000000 mktrader-0.0.4/mktrader/models.py
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1055 2023-05-12 03:59:20.000000 mktrader-0.0.4/mktrader/strategies.py
+drwxr-xr-x   0 mmurphy  (433907835) 1133555842        0 2023-05-13 15:49:12.401511 mktrader-0.0.4/mktrader.egg-info/
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      699 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/PKG-INFO
+-rw-r--r--   0 mmurphy  (433907835) 1133555842      368 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/SOURCES.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842        1 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/dependency_links.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842       26 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/requires.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842        9 2023-05-13 15:49:12.000000 mktrader-0.0.4/mktrader.egg-info/top_level.txt
+-rw-r--r--   0 mmurphy  (433907835) 1133555842       38 2023-05-13 15:49:12.401939 mktrader-0.0.4/setup.cfg
+-rw-r--r--   0 mmurphy  (433907835) 1133555842     1017 2023-05-13 15:33:41.000000 mktrader-0.0.4/setup.py
```

### Comparing `mktrader-0.0.3/LICENSE` & `mktrader-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/PKG-INFO` & `mktrader-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mktrader
-Version: 0.0.3
+Version: 0.0.4
 Summary: Stock Market Trading Framework
 Home-page: https://github.com/matthewkurtis/mktrader.git
 Author: Matthew K Murphy (MatthewKurtis)
 Author-email: <mkmurphy526@gmail.com>
 Keywords: python,trading,stock,market
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Financial and Insurance Industry
```

### Comparing `mktrader-0.0.3/mktrader/engines.py` & `mktrader-0.0.4/mktrader/engines.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/mktrader/feeds.py` & `mktrader-0.0.4/mktrader/feeds.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from .models import DataFeed, Candle
 from .logger import logger
 from typing import Optional, List
-from datetime import datetime
+from datetime import datetime, timedelta
 import requests
 import websocket
 import json
 
 
 class Alpaca_Historical_Bars(DataFeed):
     ALPACA_DATA_API_URL = "https://data.alpaca.markets"
@@ -43,15 +43,26 @@
         headers = {
             'APCA-API-KEY-ID': self.api_key,
             'APCA-API-SECRET-KEY': self.api_secret
         }
         logger.debug(f"fetching candles from {url}")
         response = requests.get(url=url, headers=headers)
         json_response = response.json()
-        # logger.debug(json_response)
+        if json_response["bars"] is None:
+            logger.debug(json_response)
+            logger.error("No bars found (weekend?)..retrying with start time as limit 1000 prior periods")
+            if time_period == "Min":
+                start = (datetime.utcnow() - timedelta(minutes=1000)).strftime("%Y-%m-%dT%H:%M:%SZ")
+            elif time_period == "Hour":
+                start = (datetime.utcnow() - timedelta(hours=1000)).strftime("%Y-%m-%dT%H:%M:%SZ")
+            url = f"{url}&start={start}"
+            logger.debug(f"URL = {url}")
+            logger.debug(f"fetching candles from {url}")
+            response = requests.get(url=url, headers=headers)
+            json_response = response.json() 
         candles = []
         if self.engine.asset.asset_class == "us_equity":
             bars_list = json_response["bars"]
         elif self.engine.asset.asset_class == "crypto":
             bars_list = json_response["bars"][self.engine.asset.symbol]
         for bar in bars_list:
             candle = Candle(
```

### Comparing `mktrader-0.0.3/mktrader/helpers.py` & `mktrader-0.0.4/mktrader/helpers.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/mktrader/indicators.py` & `mktrader-0.0.4/mktrader/indicators.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/mktrader/logger.py` & `mktrader-0.0.4/mktrader/logger.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/mktrader/models.py` & `mktrader-0.0.4/mktrader/models.py`

 * *Files 2% similar despite different names*

```diff
@@ -151,15 +151,25 @@
 
     @abstractmethod
     def get_assets(self) -> List[Asset]:
         """
         A function that retrieves all assets from broker
 
         Returns:
-            List[Stock]: A list of Asset objects with properties for each asset
+            List[Asset]: A list of Asset objects with properties for each asset
+        """
+        pass
+
+    @abstractmethod
+    def get_asset(self) -> Asset:
+        """
+        A function that retrieves all assets from broker
+
+        Returns:
+            Asset: A single Asset
         """
         pass
 
     @abstractmethod
     def in_position(self, ticker: str) -> bool:
         """
         A function that checks if supplied symbol has open positions
@@ -260,9 +270,12 @@
         self.datasource = DataFeed(self)
         self.strategy = Strategy(self)
         self.broker = Broker(self)
 
     def set_log_level(self, log_level: str) -> None:
         set_logs(log_level)
 
+    def set_asset(self, symbol: str) -> Asset:
+        self.asset = self.broker.get_asset(symbol)
+
     def run():
         pass
```

### Comparing `mktrader-0.0.3/mktrader/strategies.py` & `mktrader-0.0.4/mktrader/strategies.py`

 * *Files identical despite different names*

### Comparing `mktrader-0.0.3/mktrader.egg-info/PKG-INFO` & `mktrader-0.0.4/mktrader.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mktrader
-Version: 0.0.3
+Version: 0.0.4
 Summary: Stock Market Trading Framework
 Home-page: https://github.com/matthewkurtis/mktrader.git
 Author: Matthew K Murphy (MatthewKurtis)
 Author-email: <mkmurphy526@gmail.com>
 Keywords: python,trading,stock,market
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Financial and Insurance Industry
```

### Comparing `mktrader-0.0.3/setup.py` & `mktrader-0.0.4/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '0.0.3'
+VERSION = '0.0.4'
 DESCRIPTION = 'Stock Market Trading Framework'
 LONG_DESCRIPTION = 'A Framework for simple creation and deployment of trading strategies.'
 
 # Setting up
 setup(
     name="mktrader",
     version=VERSION,
```

