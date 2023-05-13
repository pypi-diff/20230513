# Comparing `tmp/monero_usd_price-1.1.0.tar.gz` & `tmp/monero_usd_price-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "monero_usd_price-1.1.0.tar", last modified: Thu Apr 27 02:25:18 2023, max compression
+gzip compressed data, was "monero_usd_price-1.2.0.tar", last modified: Sat May 13 00:08:35 2023, max compression
```

## Comparing `monero_usd_price-1.1.0.tar` & `monero_usd_price-1.2.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-04-27 02:25:18.610567 monero_usd_price-1.1.0/
--rw-rw-rw-   0        0        0      466 2023-04-27 02:25:18.609567 monero_usd_price-1.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1622 2023-04-22 02:38:56.000000 monero_usd_price-1.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-04-27 02:25:18.605567 monero_usd_price-1.1.0/monero_usd_price/
--rw-rw-rw-   0        0        0       33 2023-04-22 02:06:02.000000 monero_usd_price-1.1.0/monero_usd_price/__init__.py
--rw-rw-rw-   0        0        0    12290 2023-04-27 02:22:31.000000 monero_usd_price-1.1.0/monero_usd_price/monero_usd_price.py
-drwxrwxrwx   0        0        0        0 2023-04-27 02:25:18.609567 monero_usd_price-1.1.0/monero_usd_price.egg-info/
--rw-rw-rw-   0        0        0      466 2023-04-27 02:25:18.000000 monero_usd_price-1.1.0/monero_usd_price.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      283 2023-04-27 02:25:18.000000 monero_usd_price-1.1.0/monero_usd_price.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-27 02:25:18.000000 monero_usd_price-1.1.0/monero_usd_price.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-04-27 02:25:18.000000 monero_usd_price-1.1.0/monero_usd_price.egg-info/requires.txt
--rw-rw-rw-   0        0        0       17 2023-04-27 02:25:18.000000 monero_usd_price-1.1.0/monero_usd_price.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-27 02:25:18.610567 monero_usd_price-1.1.0/setup.cfg
--rw-rw-rw-   0        0        0      609 2023-04-27 02:24:04.000000 monero_usd_price-1.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 00:08:35.321309 monero_usd_price-1.2.0/
+-rw-rw-rw-   0        0        0      466 2023-05-13 00:08:35.321309 monero_usd_price-1.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0     1622 2023-04-22 02:38:56.000000 monero_usd_price-1.2.0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 00:08:35.316695 monero_usd_price-1.2.0/monero_usd_price/
+-rw-rw-rw-   0        0        0       33 2023-04-22 02:06:02.000000 monero_usd_price-1.2.0/monero_usd_price/__init__.py
+-rw-rw-rw-   0        0        0    13910 2023-05-13 00:07:09.000000 monero_usd_price-1.2.0/monero_usd_price/monero_usd_price.py
+drwxrwxrwx   0        0        0        0 2023-05-13 00:08:35.320309 monero_usd_price-1.2.0/monero_usd_price.egg-info/
+-rw-rw-rw-   0        0        0      466 2023-05-13 00:08:35.000000 monero_usd_price-1.2.0/monero_usd_price.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      283 2023-05-13 00:08:35.000000 monero_usd_price-1.2.0/monero_usd_price.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 00:08:35.000000 monero_usd_price-1.2.0/monero_usd_price.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 00:08:35.000000 monero_usd_price-1.2.0/monero_usd_price.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       17 2023-05-13 00:08:35.000000 monero_usd_price-1.2.0/monero_usd_price.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 00:08:35.321309 monero_usd_price-1.2.0/setup.cfg
+-rw-rw-rw-   0        0        0      609 2023-05-13 00:07:37.000000 monero_usd_price-1.2.0/setup.py
```

### Comparing `monero_usd_price-1.1.0/README.md` & `monero_usd_price-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `monero_usd_price-1.1.0/monero_usd_price/monero_usd_price.py` & `monero_usd_price-1.2.0/monero_usd_price/monero_usd_price.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,130 +1,165 @@
+import time
+
 import requests
 
 
 # FUNCTIONS ############################################################################################################
 def coingecko(print_price_to_console=False):
-    # Make a GET request to the CoinGecko API for XMR/USD exchange rate
-    response = requests.get('https://api.coingecko.com/api/v3/simple/price?ids=monero&vs_currencies=usd')
-
-    # Check if the request was successful
-    if response.status_code == 200:
-        # Parse the response JSON and extract the XMR/USD exchange rate
-        xmr_usd_rate = response.json()['monero']['usd']
-        print(f"Coin Gecko: {xmr_usd_rate}") if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        print("Error: Could not retrieve XMR/USD exchange rate")
+    try:
+        # Make a GET request to the CoinGecko API for XMR/USD exchange rate
+        response = requests.get('https://api.coingecko.com/api/v3/simple/price?ids=monero&vs_currencies=usd')
+
+        # Check if the request was successful
+        if response.status_code == 200:
+            # Parse the response JSON and extract the XMR/USD exchange rate
+            xmr_usd_rate = response.json()['monero']['usd']
+            print(f"Coin Gecko: {xmr_usd_rate}") if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            print("Error: Could not retrieve XMR/USD exchange rate")
+    except:
+        pass
 
 
 def binance(print_price_to_console=False):
-    response = requests.get('https://api.binance.com/api/v3/ticker/price', params={'symbol': 'XMRUSDT'})
-    #print(response.content)  # Does not work from US ip address
-    if response.status_code == 200:
-        xmr_usd_rate = float(response.json()['price'])
-        print(f'Binance: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://api.binance.com/api/v3/ticker/price', params={'symbol': 'XMRUSDT'})
+        #print(response.content)  # Does not work from US ip address
+        if response.status_code == 200:
+            xmr_usd_rate = float(response.json()['price'])
+            print(f'Binance: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def coinmarketcap(print_price_to_console=False):
-    response = requests.get('https://coinmarketcap.com/currencies/monero/')
-    if response.status_code == 200:
-        xmr_usd_rate = round(float(str(response.content).split(
-            '"currency":"XMR","currentExchangeRate":{"@type":"UnitPriceSpecification","price":')[1].split(',"')[0]), 2)
-        print(f'CoinMarketCap: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://coinmarketcap.com/currencies/monero/')
+        if response.status_code == 200:
+            xmr_usd_rate = round(float(str(response.content).split(
+                '"currency":"XMR","currentExchangeRate":{"@type":"UnitPriceSpecification","price":')[1].split(',"')[0]), 2)
+            print(f'CoinMarketCap: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def cryptocompare(print_price_to_console=False):
-    response = requests.get('https://min-api.cryptocompare.com/data/price', params={'fsym': 'XMR', 'tsyms': 'USD'})
-    if response.status_code == 200:
-        xmr_usd_rate = response.json()['USD']
-        print(f'CryptoCompare: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://min-api.cryptocompare.com/data/price', params={'fsym': 'XMR', 'tsyms': 'USD'})
+        if response.status_code == 200:
+            xmr_usd_rate = response.json()['USD']
+            print(f'CryptoCompare: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def kraken(print_price_to_console=False):
-    response = requests.get('https://api.kraken.com/0/public/Ticker', params={'pair': 'XMRUSD'})
-    if response.status_code == 200:
-        xmr_usd_rate = float(response.json()['result']['XXMRZUSD']['c'][0])
-        print(f'Kraken: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://api.kraken.com/0/public/Ticker', params={'pair': 'XMRUSD'})
+        if response.status_code == 200:
+            xmr_usd_rate = float(response.json()['result']['XXMRZUSD']['c'][0])
+            print(f'Kraken: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def bitfinex(print_price_to_console=False):
-    response = requests.get('https://api-pub.bitfinex.com/v2/ticker/tXMRUSD')
-    if response.status_code == 200:
-        xmr_usd_rate = float(response.json()[6])
-        print(f'Bitfinex: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://api-pub.bitfinex.com/v2/ticker/tXMRUSD')
+        if response.status_code == 200:
+            xmr_usd_rate = float(response.json()[6])
+            print(f'Bitfinex: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def localmonero(print_price_to_console=False):
     # 'nehdddktmhvqklsnkjqcbpmb63htee2iznpcbs5tgzctipxykpj6yrid.onion'
-    response = requests.get('https://localmonero.co/buy-monero-with-usd-in-united-states-of-america')
-    if response.status_code == 200:
-        xmr_usd_rate = float(str(response.content).split(' USD<!-- --> ')[0].split('">')[-1])
-        print(f'LocalMonero: {xmr_usd_rate}') if print_price_to_console else None
-        return xmr_usd_rate
-    else:
-        return None
+    try:
+        response = requests.get('https://localmonero.co/buy-monero-with-usd-in-united-states-of-america')
+        if response.status_code == 200:
+            xmr_usd_rate = float(str(response.content).split(' USD<!-- --> ')[0].split('">')[-1])
+            print(f'LocalMonero: {xmr_usd_rate}') if print_price_to_console else None
+            return xmr_usd_rate
+        else:
+            return None
+    except:
+        pass
 
 
 def poloniex(print_price_to_console=False):
-    response = requests.get('https://poloniex.com/public?command=returnTicker')
-    if response.status_code == 200:
-        ticker = response.json().get('USDT_XMR')
-        if ticker:
-            xmr_usd_rate = float(ticker.get('last'))
-            print(f'Poloniex: {xmr_usd_rate}') if print_price_to_console else None
-            return xmr_usd_rate
-    return None
+    try:
+        response = requests.get('https://poloniex.com/public?command=returnTicker')
+        if response.status_code == 200:
+            ticker = response.json().get('USDT_XMR')
+            if ticker:
+                xmr_usd_rate = float(ticker.get('last'))
+                print(f'Poloniex: {xmr_usd_rate}') if print_price_to_console else None
+                return xmr_usd_rate
+        return None
+    except:
+        pass
 
 
 def huobi(print_price_to_console=False):
-    response = requests.get('https://api.huobi.pro/market/detail/merged?symbol=xmrusdt')
-    if response.status_code == 200:
-        ticker = response.json().get('tick')
-        if ticker:
-            xmr_usd_rate = float(ticker.get('close'))
-            print(f'Huobi: {xmr_usd_rate}') if print_price_to_console else None
-            return xmr_usd_rate
-    return None
+    try:
+        response = requests.get('https://api.huobi.pro/market/detail/merged?symbol=xmrusdt')
+        if response.status_code == 200:
+            ticker = response.json().get('tick')
+            if ticker:
+                xmr_usd_rate = float(ticker.get('close'))
+                print(f'Huobi: {xmr_usd_rate}') if print_price_to_console else None
+                return xmr_usd_rate
+        return None
+    except:
+        pass
 
 
 def kucoin(print_price_to_console=False):
-    response = requests.get('https://api.kucoin.com/api/v1/market/orderbook/level1?symbol=XMR-USDT')
-    if response.status_code == 200:
-        ticker = response.json().get('data')
-        if ticker:
-            xmr_usd_rate = float(ticker.get('price'))
-            print(f'KuCoin: {xmr_usd_rate}') if print_price_to_console else None
-            return xmr_usd_rate
-    return None
+    try:
+        response = requests.get('https://api.kucoin.com/api/v1/market/orderbook/level1?symbol=XMR-USDT')
+        if response.status_code == 200:
+            ticker = response.json().get('data')
+            if ticker:
+                xmr_usd_rate = float(ticker.get('price'))
+                print(f'KuCoin: {xmr_usd_rate}') if print_price_to_console else None
+                return xmr_usd_rate
+        return None
+    except:
+        pass
 
 
 def hitbtc(print_price_to_console=False):
-    response = requests.get('https://api.hitbtc.com/api/3/public/ticker/XMRUSDT')
-    if response.status_code == 200:
-        ticker = response.json()
-        if ticker:
-            xmr_usd_rate = round(float(ticker.get('last')), 2)  # round to 2 decimals
-            print(f'HitBTC: {xmr_usd_rate}') if print_price_to_console else None
-            return xmr_usd_rate
-    return None
+    try:
+        response = requests.get('https://api.hitbtc.com/api/3/public/ticker/XMRUSDT')
+        if response.status_code == 200:
+            ticker = response.json()
+            if ticker:
+                xmr_usd_rate = round(float(ticker.get('last')), 2)  # round to 2 decimals
+                print(f'HitBTC: {xmr_usd_rate}') if print_price_to_console else None
+                return xmr_usd_rate
+        return None
+    except:
+        pass
 
 
 def get_monero_price_from_all_exchanges_not_threaded(print_price_to_console=False):
     prices = []
 
     coingecko_price = coingecko(print_price_to_console=print_price_to_console)
     if coingecko_price:
@@ -260,14 +295,40 @@
 
         print(f'\nMedian price is: {median_price} out of {len(sorted_prices)} exchanges') if print_price_to_console else None
         return median_price
     else:
         return None
 
 
+def calculate_monero_from_usd(usd_amount, print_price_to_console=False):
+    monero_price = median_price(print_price_to_console=print_price_to_console)
+    monero_amount = round(usd_amount / monero_price, 12)
+    if print_price_to_console:
+        print(monero_amount)
+    return monero_amount
+
+
+def calculate_usd_from_monero(monero_amount, print_price_to_console=False):
+    monero_price = median_price(print_price_to_console=print_price_to_console)
+    usd_amount = round(monero_amount * monero_price, 2)
+    if print_price_to_console:
+        print(usd_amount)
+    return usd_amount
+
+
+def calculate_atomic_units_from_monero(monero_amount):
+    atomic_units = int(monero_amount * 1e12)
+    return atomic_units
+
+
+def calculate_monero_from_atomic_units(atomic_units):
+    monero = int(atomic_units) / 1e12
+    return monero
+
+
 def print_monero_logo():
     print('''
                     k                                     d                   
                     0Kx                                 dOX                   
                     KMWKx                             dONMN                   
                     KMMMWKx                         dONMMMN                   
                     KMMMMMWKk                     d0NMMMMMN                   
@@ -277,8 +338,8 @@
                     KMMMMMXkNMMMMMMXk     dKWMMMMMW00MMMMMN                   
                     KMMMMM0  xNMMMMMMXk dKWMMMMMWOc dMMMMMN                   
                     KMMMMM0    xNMMMMMMNWMMMMMWOc   dMMMMMN                   
                     KMMMMM0      dXMMMMMMMMMNkc     dMMMMMN                   
                     KMMMMM0        oXMMMMMNx;       dMMMMMN                   
 KMMMMMMMMMMMMMMMMMMMMMMMMM0          dNMWk:         dMMMMMMMMMMMMMMMMMMMMMMMMK
 KMMMMMMMMMMMMMMMMMMMMMMMMM0            o            dMMMMMMMMMMMMMMMMMMMMMMMMK
-KMMMMMMMMMMMMMWNNNNNNNNNNNO                         oNNNNNNNNNNNNMMMMMMMMMMMMO''')
+KMMMMMMMMMMMMMWNNNNNNNNNNNO                         oNNNNNNNNNNNNMMMMMMMMMMMMO''')
```

### Comparing `monero_usd_price-1.1.0/setup.py` & `monero_usd_price-1.2.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='monero_usd_price',
-    version='1.1.0',
+    version='1.2.0',
     author="Luke Profits",
     description="Monero-USD-Price is an easy way to get the current median or average price of Monero (median is recommended over average, because it less sensitive to outliers.)",
     url="https://github.com/lukeprofits/Monero-USD-Price",
     packages=['monero_usd_price'],
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
```

