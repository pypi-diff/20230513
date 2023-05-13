# Comparing `tmp/pyokx-0.6.0.tar.gz` & `tmp/pyokx-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyokx-0.6.0.tar", max compression
+gzip compressed data, was "pyokx-0.7.0.tar", max compression
```

## Comparing `pyokx-0.6.0.tar` & `pyokx-0.7.0.tar`

### file list

```diff
@@ -1,26 +1,28 @@
--rw-r--r--   0        0        0     1069 2022-09-05 16:43:35.224410 pyokx-0.6.0/LICENSE
--rw-r--r--   0        0        0     4093 2022-11-01 00:43:59.534484 pyokx-0.6.0/README.md
--rw-r--r--   0        0        0    28388 2022-12-20 00:27:42.515692 pyokx-0.6.0/pyokx/Account.py
--rw-r--r--   0        0        0    13013 2022-11-01 00:31:39.031058 pyokx-0.6.0/pyokx/Blocktrading.py
--rw-r--r--   0        0        0     3564 2022-12-20 00:27:42.899694 pyokx-0.6.0/pyokx/Convert.py
--rw-r--r--   0        0        0     6202 2022-12-20 00:27:42.687692 pyokx-0.6.0/pyokx/CopyTrading.py
--rw-r--r--   0        0        0     4452 2022-12-20 00:27:42.603692 pyokx-0.6.0/pyokx/Earn.py
--rw-r--r--   0        0        0    16522 2022-12-20 00:27:42.663692 pyokx-0.6.0/pyokx/Funding.py
--rw-r--r--   0        0        0     9261 2022-12-20 00:27:42.011689 pyokx-0.6.0/pyokx/Gridtrading.py
--rw-r--r--   0        0        0    15592 2022-12-20 00:27:42.831693 pyokx-0.6.0/pyokx/Marketdata.py
--rw-r--r--   0        0        0    13850 2022-12-20 00:27:42.571692 pyokx-0.6.0/pyokx/Publicdata.py
--rw-r--r--   0        0        0      668 2022-12-20 00:27:42.519692 pyokx-0.6.0/pyokx/Status.py
--rw-r--r--   0        0        0     6713 2022-12-20 00:27:42.759693 pyokx-0.6.0/pyokx/SubAccount.py
--rw-r--r--   0        0        0    23322 2022-12-20 00:27:42.263690 pyokx-0.6.0/pyokx/Trade.py
--rw-r--r--   0        0        0     7827 2022-12-20 00:27:42.739693 pyokx-0.6.0/pyokx/Tradingdata.py
--rw-r--r--   0        0        0      847 2022-11-01 00:35:11.386300 pyokx-0.6.0/pyokx/__init__.py
--rw-r--r--   0        0        0     2815 2022-12-20 00:35:47.417232 pyokx-0.6.0/pyokx/auth.py
--rw-r--r--   0        0        0     5422 2022-12-20 00:34:00.405028 pyokx-0.6.0/pyokx/base.py
--rw-r--r--   0        0        0      104 2022-07-22 22:58:12.311960 pyokx-0.6.0/pyokx/constants.py
--rw-r--r--   0        0        0      621 2022-07-19 00:36:15.425336 pyokx-0.6.0/pyokx/exceptions.py
--rw-r--r--   0        0        0        0 2022-07-18 23:25:32.339613 pyokx-0.6.0/pyokx/tests/__init__.py
--rw-r--r--   0        0        0     2632 2022-08-10 23:46:41.835054 pyokx-0.6.0/pyokx/tests/test_auth.py
--rw-r--r--   0        0        0     3639 2022-12-20 00:36:11.069270 pyokx-0.6.0/pyokx/tests/test_base.py
--rw-r--r--   0        0        0     1168 2022-12-20 00:30:58.188527 pyokx-0.6.0/pyproject.toml
--rw-r--r--   0        0        0     4965 2022-12-20 00:36:56.793888 pyokx-0.6.0/setup.py
--rw-r--r--   0        0        0     4923 2022-12-20 00:36:56.794183 pyokx-0.6.0/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-02-27 19:08:52.366512 pyokx-0.7.0/LICENSE
+-rw-r--r--   0        0        0     4093 2023-02-27 19:08:52.366512 pyokx-0.7.0/README.md
+-rw-r--r--   0        0        0      852 2023-05-13 15:42:08.252604 pyokx-0.7.0/pyokx/__init__.py
+-rw-r--r--   0        0        0    48364 2023-05-13 16:42:58.752139 pyokx-0.7.0/pyokx/account.py
+-rw-r--r--   0        0        0     2815 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/auth.py
+-rw-r--r--   0        0        0     5422 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/base.py
+-rw-r--r--   0        0        0    13013 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/block_trading.py
+-rw-r--r--   0        0        0      104 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/constants.py
+-rw-r--r--   0        0        0     5239 2023-05-13 16:42:58.992139 pyokx-0.7.0/pyokx/convert.py
+-rw-r--r--   0        0        0     9025 2023-05-13 16:42:58.632139 pyokx-0.7.0/pyokx/copy_trading.py
+-rw-r--r--   0        0        0     9278 2023-05-13 16:42:58.912139 pyokx-0.7.0/pyokx/earn.py
+-rw-r--r--   0        0        0      621 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/exceptions.py
+-rw-r--r--   0        0        0    27193 2023-05-13 16:42:57.692139 pyokx-0.7.0/pyokx/funding.py
+-rw-r--r--   0        0        0    22011 2023-05-13 16:42:57.822139 pyokx-0.7.0/pyokx/grid_trading.py
+-rw-r--r--   0        0        0    21916 2023-05-13 16:42:58.962139 pyokx-0.7.0/pyokx/market_data.py
+-rw-r--r--   0        0        0    22095 2023-05-13 16:42:58.862139 pyokx-0.7.0/pyokx/public_data.py
+-rw-r--r--   0        0        0     8166 2023-05-13 16:42:57.662139 pyokx-0.7.0/pyokx/recurring_buy.py
+-rw-r--r--   0        0        0     5855 2023-05-13 16:42:58.772139 pyokx-0.7.0/pyokx/savings.py
+-rw-r--r--   0        0        0      668 2023-03-28 01:48:16.349006 pyokx-0.7.0/pyokx/status.py
+-rw-r--r--   0        0        0    12553 2023-05-13 16:42:57.932139 pyokx-0.7.0/pyokx/subaccount.py
+-rw-r--r--   0        0        0        0 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/tests/__init__.py
+-rw-r--r--   0        0        0     2632 2023-02-27 19:08:52.376512 pyokx-0.7.0/pyokx/tests/test_auth.py
+-rw-r--r--   0        0        0     3639 2023-05-13 16:50:02.812087 pyokx-0.7.0/pyokx/tests/test_base.py
+-rw-r--r--   0        0        0    56254 2023-05-13 16:42:58.332139 pyokx-0.7.0/pyokx/trade.py
+-rw-r--r--   0        0        0    10825 2023-05-13 16:42:58.012139 pyokx-0.7.0/pyokx/trading_data.py
+-rw-r--r--   0        0        0     1272 2023-05-13 17:07:55.371950 pyokx-0.7.0/pyproject.toml
+-rw-r--r--   0        0        0     4973 1970-01-01 00:00:00.000000 pyokx-0.7.0/setup.py
+-rw-r--r--   0        0        0     4974 1970-01-01 00:00:00.000000 pyokx-0.7.0/PKG-INFO
```

### Comparing `pyokx-0.6.0/LICENSE` & `pyokx-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/README.md` & `pyokx-0.7.0/README.md`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/Account.py` & `pyokx-0.7.0/pyokx/market_data.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,859 +1,698 @@
 # auto-generated code #
 from .base import APIComponent, APIReturn, EndpointDetails
 
 
-class Account(APIComponent):
-    def get_balance(self, ccy: str = None, use_proxy: bool = False) -> APIReturn:
+class MarketData(APIComponent):
+    def get_tickers(
+        self,
+        instType: str,
+        uly: str = None,
+        instFamily: str = None,
+        use_proxy: bool = False,
+    ) -> APIReturn:
         """
-                        Get balance
-                        Retrieve a list of assets (with non-zero balance), remaining balance, and available amount in the trading account.
 
-        Interest-free quota and discount rates are public data and not displayed on the account interface.
+        Retrieve the latest price snapshot, best bid/ask price, and trading volume in the last 24 hours.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
 
-                        Rate Limit: 10 requests per 2 seconds
-                        Rate limit rule: UserID
+        Args:
+            instType: Instrument type  SPOT SWAP  FUTURES OPTION
+            uly: Underlying, e.g. BTC-USD Applicable to FUTURES/SWAP/OPTION
+            instFamily: Instrument family Applicable to FUTURES/SWAP/OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/balance",
+            request_path="/api/v5/market/tickers",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_positions(
-        self,
-        instType: str = None,
-        instId: str = None,
-        posId: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_ticker(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-        Get positions
-        Retrieve information on your positions. When the account is in net mode, net positions will be displayed, and when the account is in long/short mode, long or short positions will be displayed. Return in reverse chronological order using ctime.
-        Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the latest price snapshot, best bid/ask price, and trading volume in the last 24 hours.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/positions",
+            request_path="/api/v5/market/ticker",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_positions_history(
-        self,
-        instType: str = None,
-        instId: str = None,
-        mgnMode: str = None,
-        type: str = None,
-        posId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
+    def get_index_tickers(
+        self, quoteCcy: str = None, instId: str = None, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Get positions history
-        Retrieve the updated position data for the last 3 months. Return in reverse chronological order using utime.
-        Rate Limit: 1 request per 10 seconds
-        Rate limit rule: UserID
+
+        Retrieve index tickers.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            quoteCcy: Quote currency Currently there is only an index with USD/USDT/BTC as
+                the quote currency.
+            instId: Index, e.g. BTC-USD Either quoteCcy or instId is required.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/positions-history",
+            request_path="/api/v5/market/index-tickers",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_account_and_position_risk(self, use_proxy: bool = False) -> APIReturn:
+    def get_order_book(
+        self, instId: str, sz: str = None, use_proxy: bool = False
+    ) -> APIReturn:
         """
-                        Get account and position risk
-                        Get account and position risk
 
-        Obtain basic information about accounts and positions on the same time slice
+        Retrieve order book of the instrument.
+        Rate Limit: 40 requests per 2 seconds
+        Rate limit rule: IP
+
 
-                        Rate Limit: 10 requests per 2 seconds
-                        Rate limit rule: UserID
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT
+            sz: Order book depth per side. Maximum 400, e.g. 400 bids + 400 asks
+                Default returns to 1 depth data
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/account-position-risk",
+            request_path="/api/v5/market/books",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_bills_details_last_7_days(
-        self,
-        instType: str = None,
-        ccy: str = None,
-        mgnMode: str = None,
-        ctType: str = None,
-        type: str = None,
-        subType: str = None,
-        after: str = None,
-        before: str = None,
-        begin: str = None,
-        end: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_order_lite_book(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-        Get bills details (last 7 days)
-        Retrieve the bills of the account. The bill refers to all transaction records that result in changing the balance of an account. Pagination is supported, and the response is sorted with the most recent first. This endpoint can retrieve data from the last 7 days.
-        Rate Limit: 6 requests per second
-        Rate limit rule: UserID
+
+        Retrieve order top 25 book of the instrument more quickly
+        Rate Limit: 6 requests per 1 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/bills",
+            request_path="/api/v5/market/books-lite",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_bills_details_last_3_months(
+    def get_candlesticks(
         self,
-        instType: str = None,
-        ccy: str = None,
-        mgnMode: str = None,
-        ctType: str = None,
-        type: str = None,
-        subType: str = None,
+        instId: str,
+        bar: str = None,
         after: str = None,
         before: str = None,
-        begin: str = None,
-        end: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get bills details (last 3 months)
-        Retrieve the account’s bills. The bill refers to all transaction records that result in changing the balance of an account. Pagination is supported, and the response is sorted with most recent first. This endpoint can retrieve data from the last 3 months.
-        Rate Limit: 6 requests per second
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/bills-archive",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_account_configuration(self, use_proxy: bool = False) -> APIReturn:
-        """
-        Get account configuration
-        Retrieve current account configuration.
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/config",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
+        Retrieve the candlestick charts. This endpoint can retrieve the latest 1,440 data entries. Charts are returned in groups based on the requested bar.
+        Rate Limit: 40 requests per 2 seconds
+        Rate limit rule: IP
 
-    def set_position_mode(self, posMode: str, use_proxy: bool = False) -> APIReturn:
-        """
-                        Set position mode
-                        Single-currency mode and Multi-currency mode: FUTURES and SWAP support both long/short mode and net mode. In net mode, users can only have positions in one direction; In long/short mode, users can hold positions in long and short directions.
-        Portfolio margin mode: FUTURES and SWAP only support net mode
-                        Rate Limit: 5 requests per 2 seconds
-                        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/set-position-mode",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def set_leverage(
-        self,
-        lever: str,
-        mgnMode: str,
-        instId: str = None,
-        ccy: str = None,
-        posSide: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-                        Set leverage
-                        There are 9 different scenarios for leverage setting:
-        1. Set leverage for MARGIN instruments under isolated-margin trade mode at pairs level.
-        2. Set leverage for MARGIN instruments under cross-margin trade mode and Single-currency margin account mode at pairs level.
-        3. Set leverage for MARGIN instruments under cross-margin trade mode and Multi-currency margin at currency level.
-        4. Set leverage for FUTURES instruments under cross-margin trade mode at underlying level.
-        5. Set leverage for FUTURES instruments under isolated-margin trade mode and buy/sell position mode at contract level.
-        6. Set leverage for FUTURES instruments under isolated-margin trade mode and long/short position mode at contract and position side level.
-        7. Set leverage for SWAP instruments under cross-margin trade at contract level.
-        8. Set leverage for SWAP instruments under isolated-margin trade mode and buy/sell position mode at contract level.
-        9. Set leverage for SWAP instruments under isolated-margin trade mode and long/short position mode at contract and position side level.
-                        Note that the request parameter posSide is only required when margin mode is isolated in long/short position mode for FUTURES/SWAP instruments (see scenario 6 and 9 above).
-        Please refer to the request examples on the right side for each case.
-                        Rate Limit: 20 requests per 2 seconds
-                        Rate limit rule: UserID
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-190927-5000-C
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/2D/3D/1W/1M/3M] UTC time opening
+                price k-line：[/6Hutc/12Hutc/1Dutc/2Dutc/3Dutc/1Wutc/1Mutc/3Mutc]
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            limit: Number of results per request. The maximum is 300. The default is 100.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/set-leverage",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/market/candles",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_maximum_buy_sell_amount_or_open_amount(
+    def get_candlesticks_history(
         self,
         instId: str,
-        tdMode: str,
-        px: str = None,
-        leverage: str = None,
-        unSpotOffset: bool = None,
-        ccy: str = None,
+        after: str = None,
+        before: str = None,
+        bar: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-                        Get maximum buy/sell amount or open amount
 
-        Under the Portfolio Margin account, the cross mode of derivatives does not support the calculation of the maximum buy/sell amount or open amount.
+        Retrieve history candlestick charts from recent years.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
 
-                        Rate Limit: 20 requests per 2 seconds
-                        Rate limit rule: UserID
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-200927
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/2D/3D/1W/1M/3M] UTC time opening
+                price k-line：[6Hutc/12Hutc/1Dutc/2Dutc/3Dutc/1Wutc/1Mutc/3Mutc]
+            limit: Number of results per request. The maximum is 100. The default is 100.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/max-size",
+            request_path="/api/v5/market/history-candles",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_maximum_available_tradable_amount(
+    def get_index_candlesticks(
         self,
         instId: str,
-        tdMode: str,
-        reduceOnly: bool = None,
-        unSpotOffset: bool = None,
-        ccy: str = None,
+        after: str = None,
+        before: str = None,
+        bar: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get maximum available tradable amount
+
+        Retrieve the candlestick charts of the index. This endpoint can retrieve the latest 1,440 data entries. Charts are returned in groups based on the requested bar.
         Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Index, e.g. BTC-USD
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/1W/1M/3M] UTC time opening price
+                k-line：[/6Hutc/12Hutc/1Dutc/1Wutc/1Mutc/3Mutc]
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/max-avail-size",
+            request_path="/api/v5/market/index-candles",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def increase_decrease_margin(
+    def get_index_candlesticks_history(
         self,
         instId: str,
-        posSide: str,
-        type: str,
-        amt: str,
-        ccy: str = None,
-        auto: bool = None,
-        loanTrans: bool = None,
+        after: str = None,
+        before: str = None,
+        bar: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Increase/decrease margin
-        Increase or decrease the margin of the isolated position. Margin reduction may result in the change of the actual leverage.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/position/margin-balance",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_leverage(
-        self, instId: str, mgnMode: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get leverage
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/leverage-info",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
+        Retrieve the candlestick charts of the index from recent years.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
 
-    def get_the_maximum_loan_of_instrument(
-        self, instId: str, mgnMode: str, mgnCcy: str = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get the maximum loan of instrument
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Args:
+            instId: Index, e.g. BTC-USD
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/1W/1M] UTC time opening price
+                k-line：[/6Hutc/12Hutc/1Dutc/1Wutc/1Mutc]
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/max-loan",
+            request_path="/api/v5/market/history-index-candles",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_fee_rates(
+    def get_mark_price_candlesticks(
         self,
-        instType: str,
-        instId: str = None,
-        uly: str = None,
-        instFamily: str = None,
+        instId: str,
+        after: str = None,
+        before: str = None,
+        bar: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get fee rates
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the candlestick charts of mark price. This endpoint can retrieve the latest 1,440 data entries. Charts are returned in groups based on the requested bar.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/1W/1M/3M] UTC time opening price
+                k-line：[6Hutc/12Hutc/1Dutc/1Wutc/1Mutc/3Mutc]
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/trade-fee",
+            request_path="/api/v5/market/mark-price-candles",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_interest_accrued_data(
+    def get_mark_price_candlesticks_history(
         self,
-        type: str = None,
-        ccy: str = None,
-        instId: str = None,
-        mgnMode: str = None,
+        instId: str,
         after: str = None,
         before: str = None,
+        bar: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get interest accrued data
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/interest-accrued",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_interest_rate(self, ccy: str = None, use_proxy: bool = False) -> APIReturn:
-        """
-        Get interest rate
-        Get the user's current leveraged currency borrowing interest rate
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/interest-rate",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
+        Retrieve the candlestick charts of mark price from recent years.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
 
-    def set_greeks_pa_bs(self, greeksType: str, use_proxy: bool = False) -> APIReturn:
-        """
-        Set greeks (PA/BS)
-        Set the display type of Greeks.
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/set-greeks",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def isolated_margin_trading_settings(
-        self, isoMode: str, type: str, use_proxy: bool = False
-    ) -> APIReturn:
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            bar: Bar size, the default is 1m e.g. [1m/3m/5m/15m/30m/1H/2H/4H] Hong Kong
+                time opening price k-line：[6H/12H/1D/1W/1M] UTC time opening price
+                k-line：[6Hutc/12Hutc/1Dutc/1Wutc/1Mutc]
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
-        Isolated margin trading settings
-        You can set the currency margin and futures/perpetual Isolated margin trading mode
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/set-isolated-mode",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_maximum_withdrawals(
-        self, ccy: str = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get maximum withdrawals
-        Retrieve the maximum transferable amount from trading account to funding account. If no currency is specified, the transferable amount of all owned currencies will be returned.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/max-withdrawal",
+            request_path="/api/v5/market/history-mark-price-candles",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_account_risk_state(self, use_proxy: bool = False) -> APIReturn:
+    def get_trades(
+        self, instId: str, limit: str = None, use_proxy: bool = False
+    ) -> APIReturn:
         """
-        Get account risk state
-        Only applicable to Portfolio margin account
-        Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the recent transactions of an instrument.
+        Rate Limit: 100 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT
+            limit: Number of results per request. The maximum is 500; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/risk-state",
+            request_path="/api/v5/market/trades",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def manual_borrow_and_repay_in_quick_margin_mode(
-        self, instId: str, ccy: str, side: str, amt: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Manual borrow and repay in Quick Margin Mode
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/quick-margin-borrow-repay",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
-
-    def get_manual_borrow_and_repay_history_in_quick_margin_mode(
+    def get_trades_history(
         self,
-        instId: str = None,
-        ccy: str = None,
-        side: str = None,
+        instId: str,
+        type_: str = None,
         after: str = None,
         before: str = None,
-        begin: str = None,
-        end: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get manual borrow and repay history in Quick Margin Mode
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the recent transactions of an instrument from the last 3 months with pagination.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT
+            type_: Pagination Type 1: tradeId 2: timestamp  The default is 1
+            after: Pagination of data to return records earlier than the requested
+                tradeId or ts.
+            before: Pagination of data to return records newer than the requested tradeId.
+                Do not support timestamp for pagination
+            limit: Number of results per request. The maximum and default both are 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/quick-margin-borrow-repay-history",
+            request_path="/api/v5/market/history-trades",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def vip_loans_borrow_and_repay(
-        self, ccy: str, side: str, amt: str, ordId: str = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        VIP loans borrow and repay
-        Rate Limit: 6 requests per second
-        Rate limit rule: UserID
+    def get_option_trades(self, instFamily: str, use_proxy: bool = False) -> APIReturn:
         """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/borrow-repay",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_borrow_and_repay_history_for_vip_loans(
-        self,
-        ccy: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Get borrow and repay history for VIP loans
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+        Retrieve the recent transactions of an instrument under same instFamily. The maximum is 100.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instFamily: Instrument family, e.g. BTC-USD Applicable to OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/borrow-repay-history",
+            request_path="/api/v5/market/option/instrument-family-trades",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_vip_interest_accrued_data(
+    def get_24h_total_volume(
         self,
-        ccy: str = None,
-        ordId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
+        volUsd: str = None,
+        volCny: str = None,
+        ts: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get VIP interest accrued data
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+
+        The 24-hour trading volume is calculated on a rolling basis.
+        Rate Limit: 2 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            volUsd: 24-hour total trading volume from the order book trading in "USD"
+            volCny: 24-hour total trading volume from the order book trading in "CNY"
+            ts: Data return time, Unix timestamp format in milliseconds, e.g.
+                1597026383085
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/vip-interest-accrued",
+            request_path="/api/v5/market/platform-",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_vip_interest_deducted_data(
+    def get_oracle(
         self,
-        ccy: str = None,
-        ordId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
+        messages: str = None,
+        prices: str = None,
+        signatures: str = None,
+        timestamp: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get VIP interest deducted data
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Get the crypto price of signing using Open Oracle smart contract.
+        Rate Limit: 1 request per 5 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            messages: ABI-encoded values [kind, timestamp, key, value], where kind equals
+                'prices', timestamp is the time when price was obtained, key is the
+                asset ticker (e.g. btc) and value is the asset price.
+            prices: Readable asset prices
+            signatures: Ethereum-compatible ECDSA signatures for each message
+            timestamp: Time of latest datapoint, Unix timestamp, e.g. 1597026387
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/vip-interest-deducted",
+            request_path="/api/v5/market/open-oracle",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_vip_loan_order_list(
-        self,
-        ordId: str = None,
-        state: str = None,
-        ccy: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
+    def get_exchange_rate(
+        self, usdCny: str = None, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Get VIP loan order list
-        Rate Limit: 5次/2s
-        Rate limit rule: UserID
+
+        This interface provides the average exchange rate data for 2 weeks
+        Rate Limit: 1 request per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            usdCny: Exchange rate
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/vip-loan-order-list",
+            request_path="/api/v5/market/exchange-rate",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_vip_loan_order_detail(
-        self,
-        ordId: str = None,
-        ccy: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_index_components(self, index: str, use_proxy: bool = False) -> APIReturn:
         """
-        Get VIP loan order detail
-        Rate Limit: 5次/2s
-        Rate limit rule: UserID
+
+        Get the index component information data on the market
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            index: index, e.g BTC-USDT
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/vip-loan-order-detail",
+            request_path="/api/v5/market/index-components",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_borrow_interest_and_limit(
-        self, type: str = None, ccy: str = None, use_proxy: bool = False
+    def get_block_tickers(
+        self,
+        instType: str,
+        uly: str = None,
+        instFamily: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get borrow interest and limit
-        Rate Limit: 5 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the latest block trading volume in the last 24 hours.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instType: Instrument type  SPOT SWAP  FUTURES OPTION
+            uly: Underlying, e.g. BTC-USD Applicable to FUTURES/SWAP/OPTION
+            instFamily: Instrument family, e.g. BTC-USD Applicable to FUTURES/SWAP/OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/interest-limits",
+            request_path="/api/v5/market/block-tickers",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def position_builder(self, use_proxy: bool = False) -> APIReturn:
+    def get_block_ticker(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-                        Position builder
-                        Calculates portfolio margin information for simulated position or current position of the user.
-        You can add up to 200 simulated positions in one request.
-                        Rate Limit: 2 requests per 2 seconds
-                        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/simulated_margin",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_greeks(self, ccy: str = None, use_proxy: bool = False) -> APIReturn:
-        """
-        Get Greeks
-        Retrieve a greeks list of all assets in the account.
-        Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
+        Retrieve the latest block trading volume in the last 24 hours.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/greeks",
+            request_path="/api/v5/market/block-ticker",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_pm_limitation(
-        self,
-        instType: str,
-        uly: str = None,
-        instFamily: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_block_trades(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-        Get PM limitation
-        Retrieve cross position limitation of SWAP/FUTURES/OPTION under Portfolio margin mode.
-        Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the recent block trading transactions of an instrument. Descending order by tradeId.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/account/position-tiers",
+            request_path="/api/v5/market/block-trades",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
-
-    def set_risk_offset_type(self, type: str, use_proxy: bool = False) -> APIReturn:
-        """
-        Set risk offset type
-        Configure the risk offset type in portfolio margin mode.
-        Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/account/set-riskOffset-type",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
```

### Comparing `pyokx-0.6.0/pyokx/Blocktrading.py` & `pyokx-0.7.0/pyokx/block_trading.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/CopyTrading.py` & `pyokx-0.7.0/pyokx/savings.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,206 +1,194 @@
 # auto-generated code #
 from .base import APIComponent, APIReturn, EndpointDetails
 
 
-class CopyTrading(APIComponent):
-    def get_existing_leading_positions(
-        self, instId: str = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get existing leading positions
-        Returns reverse chronological order with openTime
-        Rate limit: 2 requests per 2 seconds
-        Rate limit rule: UserID
+class Savings(APIComponent):
+    def get_saving_balance(self, ccy: str = None, use_proxy: bool = False) -> APIReturn:
         """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/copytrading/current-subpositions",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_leading_position_history(
-        self,
-        instId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Get leading position history
-        Returns reverse chronological order with closeTime.
-        Rate limit: 2 requests per 2 seconds
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/subpositions-history",
+            request_path="/api/v5/finance/savings/balance",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def place_leading_stop_order(
-        self,
-        subPosId: str,
-        tpTriggerPxType: str = None,
-        slTriggerPxType: str = None,
-        tpTriggerPx: str = None,
-        slTriggerPx: str = None,
-        use_proxy: bool = False,
+    def savings_purchase_redemption(
+        self, ccy: str, amt: str, side: str, rate: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Place leading stop order
-        Rate limit: 1 request per 2 seconds
+
+        Only the assets in the funding account can be used for saving.
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+            amt: Purchase/redemption amount
+            side: Action type. purchase: purchase saving shares redempt: redeem saving
+                shares
+            rate: Annual purchase rate Only applicable to purchase saving shares The
+                interest rate of the new subscription will cover the interest rate of
+                the last subscription The rate value range is between 1% and 365%
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/algo-order",
+            request_path="/api/v5/finance/savings/purchase-redempt",
             method="POST",
             body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def close_leading_position(
-        self, subPosId: str, use_proxy: bool = False
+    def set_lending_rate(
+        self, ccy: str, rate: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Close leading position
-        Rate limit: 2 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/copytrading/close-subposition",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_leading_instruments(self, use_proxy: bool = False) -> APIReturn:
-        """
-        Get leading instruments
-        Rate limit: 2 requests per 2 seconds
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/copytrading/instruments",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def amend_leading_instruments(
-        self, instId: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Amend leading instruments
-        Rate limit: 2 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Args:
+            ccy: Currency, e.g. BTC
+            rate: Annual lending rate The rate value range is between 1% and 365%
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/set-instruments",
+            request_path="/api/v5/finance/savings/set-lending-rate",
             method="POST",
             body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_profit_sharing_details(
+    def get_lending_history(
         self,
+        ccy: str = None,
         after: str = None,
         before: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get profit sharing details
-        Rate limit: 2 requests per 2 seconds
+
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+            after: Pagination of data to return records earlier than the requested ts,
+                Unix timestamp format in milliseconds, e.g. 1597026383085
+            before: Pagination of data to return records newer than the requested ts, Unix
+                timestamp format in milliseconds, e.g. 1597026383085
+            limit: Number of results per request. The maximum is 100. The default is 100.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/profit-sharing-details",
+            request_path="/api/v5/finance/savings/lending-history",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_total_profit_sharing(self, use_proxy: bool = False) -> APIReturn:
+    def get_public_borrow_info_public(
+        self, ccy: str = None, use_proxy: bool = False
+    ) -> APIReturn:
         """
-        Get total profit sharing
-        Rate limit: 2 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Authentication is not required for this public endpoint.
+        Rate Limit: 6 requests per second
+        Rate limit rule: IP
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/total-profit-sharing",
+            request_path="/api/v5/finance/savings/lending-rate-summary",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_unrealized_profit_sharing_details(
-        self, use_proxy: bool = False
+    def get_public_borrow_history_public(
+        self,
+        ccy: str = None,
+        after: str = None,
+        before: str = None,
+        limit: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get unrealized profit sharing details
-        Rate limit: 2 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Authentication is not required for this public endpoint.
+        Rate Limit: 6 requests per second
+        Rate limit rule: IP
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+            after: Pagination of data to return records earlier than the requested ts,
+                Unix timestamp format in milliseconds, e.g. 1597026383085
+            before: Pagination of data to return records newer than the requested ts, Unix
+                timestamp format in milliseconds, e.g. 1597026383085
+            limit: Number of results per request. The maximum is 100. The default is 100.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/copytrading/unrealized-profit-sharing-details",
+            request_path="/api/v5/finance/savings/lending-rate-history",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
```

### Comparing `pyokx-0.6.0/pyokx/Earn.py` & `pyokx-0.7.0/pyokx/convert.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,160 +1,178 @@
 # auto-generated code #
 from .base import APIComponent, APIReturn, EndpointDetails
 
 
-class Earn(APIComponent):
-    def get_offers(
-        self,
-        productId: str = None,
-        protocolType: str = None,
-        ccy: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+class Convert(APIComponent):
+    def get_convert_currencies(self, use_proxy: bool = False) -> APIReturn:
         """
-        Get offers
-        Rate Limit: 3 requests per second
+
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+                _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/offers",
+            request_path="/api/v5/asset/convert/currencies",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def purchase(
-        self,
-        productId: str,
-        investData: list,
-        ccy: str,
-        amt: str,
-        tag: str = None,
-        term: str = None,
-        use_proxy: bool = False,
+    def get_convert_currency_pair(
+        self, fromCcy: str, toCcy: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Purchase
-        Rate Limit: 2 requests per second
+
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            fromCcy: Currency to convert from, e.g. USDT
+            toCcy: Currency to convert to, e.g. BTC
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/purchase",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/asset/convert/currency-pair",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def redeem(
+    def estimate_quote(
         self,
-        ordId: str,
-        protocolType: str,
-        allowEarlyRedeem: bool = None,
+        baseCcy: str,
+        quoteCcy: str,
+        side: str,
+        rfqSz: str,
+        rfqSzCcy: str,
+        clQReqId: str = None,
+        tag: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Redeem
-        Rate Limit: 2 requests per second
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/redeem",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def cancel_purchases_redemptions(
-        self, ordId: str, protocolType: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-                        Cancel purchases/redemptions
+        Rate Limit: 10 requests per second
+        Rate limit rule: UserID
 
-        After cancelling, returning funds will go to the funding account.
 
-                        Rate Limit: 2 requests per second
-                        Rate limit rule: UserID
+        Args:
+            baseCcy: Base currency, e.g. BTC in BTC-USDT
+            quoteCcy: Quote currency, e.g. USDT in BTC-USDT
+            side: Trade side based on baseCcy buy sell
+            rfqSz: RFQ amount
+            rfqSzCcy: RFQ currency
+            clQReqId: Client Order ID as assigned by the client A combination of case-
+                sensitive alphanumerics, all numbers, or all letters of up to 32
+                characters.
+            tag: Order tag Applicable to broker user
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/cancel",
+            request_path="/api/v5/asset/convert/estimate-quote",
             method="POST",
             body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_active_orders(
+    def convert_trade(
         self,
-        productId: str = None,
-        protocolType: str = None,
-        ccy: str = None,
-        state: str = None,
+        quoteId: str,
+        baseCcy: str,
+        quoteCcy: str,
+        side: str,
+        sz: str,
+        szCcy: str,
+        clTReqId: str = None,
+        tag: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get active orders
-        Rate Limit: 3 requests per second
+
+        Rate Limit: 10 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            quoteId: Quote ID
+            baseCcy: Base currency, e.g. BTC in BTC-USDT
+            quoteCcy: Quote currency, e.g. USDT in BTC-USDT
+            side: Trade side based on baseCcy buy sell
+            sz: Quote amount The quote amount should no more then RFQ amount
+            szCcy: Quote currency
+            clTReqId: Client Order ID as assigned by the client A combination of case-
+                sensitive alphanumerics, all numbers, or all letters of up to 32
+                characters.
+            tag: Order tag Applicable to broker user
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/orders-active",
-            method="GET",
-            params=kwargs,
+            request_path="/api/v5/asset/convert/trade",
+            method="POST",
+            body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_order_history(
+    def get_convert_history(
         self,
-        productId: str = None,
-        protocolType: str = None,
-        ccy: str = None,
         after: str = None,
         before: str = None,
         limit: str = None,
+        tag: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get order history
-        Rate Limit: 3 requests per second
+
+        Rate Limit: 6 requests per second
         Rate limit rule: UserID
+
+
+        Args:
+            after: Pagination of data to return records earlier than the requested ts,
+                Unix timestamp format in milliseconds, e.g. 1597026383085
+            before: Pagination of data to return records newer than the requested ts, Unix
+                timestamp format in milliseconds, e.g. 1597026383085
+            limit: Number of results per request. The maximum is 100. The default is 100.
+            tag: Order tag Applicable to broker user
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/finance/staking-defi/orders-history",
+            request_path="/api/v5/asset/convert/history",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
```

### Comparing `pyokx-0.6.0/pyokx/Gridtrading.py` & `pyokx-0.7.0/pyokx/recurring_buy.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,313 +1,274 @@
 # auto-generated code #
 from .base import APIComponent, APIReturn, EndpointDetails
 from typing import *
 
 
-class Gridtrading(APIComponent):
-    def place_grid_algo_order(
+class RecurringBuy(APIComponent):
+    def place_recurring_buy_order(
         self,
-        instId: str,
-        algoOrdType: str,
-        maxPx: str,
-        minPx: str,
-        gridNum: str,
-        runType: str = None,
-        tpTriggerPx: str = None,
-        slTriggerPx: str = None,
+        stgyName: str,
+        recurringList: List[dict],
+        ccy: str,
+        ratio: str,
+        period: str,
+        recurringDay: str,
+        recurringTime: str,
+        timeZone: str,
+        amt: str,
+        investmentCcy: str,
+        tdMode: str,
+        algoClOrdId: str = None,
         tag: str = None,
-        quoteSz: str = None,
-        baseSz: str = None,
-        sz: str = None,
-        direction: str = None,
-        lever: str = None,
-        basePos: bool = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Place grid algo order
+
         Rate Limit: 20 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
+        Rate limit rule: UserID
+
+
+        Args:
+            stgyName: Custom name for trading bot, no more than 40 characters
+            recurringList: Recurring buy info
+            ccy: Recurring currency, e.g. BTC
+            ratio: Proportion of recurring currency assets, e.g. "0.2" representing 20%
+            period: Period monthly weekly daily
+            recurringDay: Recurring buy date When the period is monthly, the value range is an
+                integer of [1,28] When the period is weekly, the value range is an
+                integer of [1,7] When the period is daily, the value is 1
+            recurringTime: Recurring buy time, the value range is an integer of [0,23]
+            timeZone: UTC time zone，the value range is an integer of [-12,14] e.g. "8"
+                representing UTC+8 (East 8 District), Beijing Time
+            amt: Quantity invested per cycle
+            investmentCcy: The invested quantity unit, can only be USDT/USDC
+            tdMode: Trading mode Margin mode: cross Non-Margin mode: cash
+            algoClOrdId: Client-supplied Algo ID There will be a value when algo order
+                attaching algoClOrdId is triggered, or it will be "". A combination of
+                case-sensitive alphanumerics, all numbers, or all letters of up to 32
+                characters.
+            tag: Order tag A combination of case-sensitive alphanumerics, all numbers,
+                or all letters of up to 16 characters.
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/order-algo",
+            request_path="/api/v5/trading",
             method="POST",
             body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def amend_grid_algo_order(
-        self,
-        algoId: str,
-        instId: str,
-        slTriggerPx: str = None,
-        tpTriggerPx: str = None,
-        use_proxy: bool = False,
+    def amend_recurring_buy_order(
+        self, algoId: str, stgyName: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Amend grid algo order
-        Supported contract grid algo order amendment.
+
         Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID + Instrument ID
+        Rate limit rule: UserID
+
+
+        Args:
+            algoId: Algo ID
+            stgyName: New custom name for trading bot after adjustment, no more than 40
+                characters
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/amend-order-algo",
+            request_path="/api/v5/trading",
             method="POST",
             body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def stop_grid_algo_order(
+    def stop_recurring_buy_order(
         self, body: List[dict] = None, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Stop grid algo order
-        A maximum of 10 orders can be canceled per request.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
-        """
-        kwargs = body
-        details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/stop-order-algo",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_grid_algo_order_list(
-        self,
-        algoOrdType: str,
-        algoId: str = None,
-        instId: str = None,
-        instType: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Get grid algo order list
+        A maximum of 10 orders can be stopped per request.
         Rate Limit: 20 requests per 2 seconds
         Rate limit rule: UserID
+
+
+        Request format:
+            This function body should be formatted as an array. Eg.
+            ```python
+            ...
+            body = [
+                {
+                    "algoId": str
+                }
+                ...
+            ]
+            api_helper = RecurringBuy(client)
+            response = api_helper.stop_recurring_buy_order(body=body)
+            ```
+
+
+        Args:
+            algoId: Algo ID
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/orders-algo-pending",
-            method="GET",
-            params=kwargs,
+            request_path="/api/v5/trading",
+            method="POST",
+            body=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_grid_algo_order_history(
+    def get_recurring_buy_order_list(
         self,
-        algoOrdType: str,
         algoId: str = None,
-        instId: str = None,
-        instType: str = None,
         after: str = None,
         before: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get grid algo order history
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/orders-algo-history",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_grid_algo_order_details(
-        self, algoOrdType: str, algoId: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get grid algo order details
         Rate Limit: 20 requests per 2 seconds
         Rate limit rule: UserID
+
+
+        Args:
+            algoId: Algo ID
+            after: Pagination of data to return records earlier than the requested
+                algoId.
+            before: Pagination of data to return records newer than the requested algoId.
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/orders-algo-details",
+            request_path="/api/v5/trading",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_grid_algo_sub_orders(
+    def get_recurring_buy_order_history(
         self,
-        algoOrdType: str,
-        algoId: str,
-        type: str,
-        groupId: str = None,
+        algoId: str = None,
         after: str = None,
         before: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get grid algo sub orders
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/sub-orders",
-            method="GET",
-            params=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_grid_algo_order_positions(
-        self, algoOrdType: str, algoId: str, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Get grid algo order positions
         Rate Limit: 20 requests per 2 seconds
         Rate limit rule: UserID
+
+
+        Args:
+            algoId: Algo ID
+            after: Pagination of data to return records earlier than the requested
+                algoId.
+            before: Pagination of data to return records newer than the requested algoId.
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/positions",
+            request_path="/api/v5/trading",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def spot_moon_grid_withdraw_income(
+    def get_recurring_buy_order_details(
         self, algoId: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Spot/Moon grid withdraw income
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/withdraw-income",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def compute_margin_balance(
-        self, algoId: str, type: str, amt: str = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Compute margin balance
         Rate Limit: 20 requests per 2 seconds
         Rate limit rule: UserID
+
+
+        Args:
+            algoId: Algo ID
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/compute-margin-balance",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/trading",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def adjust_margin_balance(
+    def get_recurring_buy_sub_orders(
         self,
         algoId: str,
-        type: str,
-        amt: str = None,
-        percent: str = None,
+        ordId: str = None,
+        after: str = None,
+        before: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Adjust margin balance
+
         Rate Limit: 20 requests per 2 seconds
         Rate limit rule: UserID
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/margin-balance",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_grid_ai_parameter_public(
-        self,
-        algoOrdType: str,
-        instId: str,
-        duration: str = None,
-        direction: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Get grid AI parameter (public)
-        Authentication is not required for this public endpoint.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: IP
+
+        Args:
+            algoId: Algo ID
+            ordId: Sub order ID
+            after: Pagination of data to return records earlier than the requested
+                algoId.
+            before: Pagination of data to return records newer than the requested algoId.
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/tradingBot/grid/ai-param",
+            request_path="/api/v5/trading",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `pyokx-0.6.0/pyokx/Status.py` & `pyokx-0.7.0/pyokx/status.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/Trade.py` & `pyokx-0.7.0/pyokx/public_data.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,697 +1,691 @@
 # auto-generated code #
 from .base import APIComponent, APIReturn, EndpointDetails
-from typing import *
 
 
-class Trade(APIComponent):
-    def place_order(
+class PublicData(APIComponent):
+    def get_instruments(
         self,
-        instId: str,
-        side: str,
-        ordType: str,
-        sz: str,
-        tdMode: str,
-        banAmend: bool = None,
-        tpTriggerPxType: str = None,
-        slOrdPx: str = None,
-        slTriggerPx: str = None,
-        tpOrdPx: str = None,
-        tpTriggerPx: str = None,
-        slTriggerPxType: str = None,
-        tgtCcy: str = None,
-        reduceOnly: bool = None,
-        tag: str = None,
-        clOrdId: str = None,
-        ccy: str = None,
-        posSide: str = None,
-        px: str = None,
+        instType: str,
+        uly: str = None,
+        instFamily: str = None,
+        instId: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-                        Place order
-                        You can place an order only if you have sufficient funds.
-        For leading contracts, this endpoint supports placement, but can't close positions.
-                        Rate Limit: 60 requests per 2 seconds
-                        Rate Limit of leading contracts: 1 requests per 2 seconds
-                        Rate limit rule (except Options): UserID + Instrument ID
-                        Rate limit rule (Options only): UserID + Instrument Family
+
+        Retrieve a list of instruments with open contracts.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP + instrumentType
+
+
+        Args:
+            instType: Instrument type SPOT MARGIN SWAP FUTURES OPTION
+            uly: Underlying Only applicable to FUTURES/SWAP/OPTION.If instType is
+                OPTION, either uly or instFamily is required.
+            instFamily: Instrument family Only applicable to FUTURES/SWAP/OPTION. If instType
+                is OPTION, either uly or instFamily is required.
+            instId: Instrument ID
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/order",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/instruments",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def place_multiple_orders(
-        self, body: List[dict] = None, use_proxy: bool = False
+    def get_delivery_exercise_history(
+        self,
+        instType: str,
+        uly: str = None,
+        instFamily: str = None,
+        after: str = None,
+        before: str = None,
+        limit: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-                        Place multiple orders
-                        Place orders in batches. Maximum 20 orders can be placed per request. Request parameters should be passed in the form of an array.
-        For leading contracts, this endpoint supports placement, but can't close positions.
-                        Rate Limit: 300 orders per 2 seconds
-                        Rate Limit of leading contracts: 1 requests per 2 seconds
-                        Rate limit rule (except Options): UserID + Instrument ID
-                        Rate limit rule (Options only): UserID + Instrument Family
 
-        Unlike other endpoints, the rate limit of this endpoint is determined by the number of orders. If there is only one order in the request, it will consume the rate limit of `Place order`.
+        Retrieve delivery records of Futures and exercise records of Options in the last 3 months.
+        Rate Limit: 40 requests per 2 seconds
+        Rate limit rule: IP + (instrumentType + uly)
 
-        """
-        kwargs = body
-        details = EndpointDetails(
-            request_path="/api/v5/trade/batch-orders",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def cancel_order(
-        self,
-        instId: str,
-        ordId: str = None,
-        clOrdId: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Cancel order
-        Cancel an incomplete order.
-        Rate Limit: 60 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
+        Args:
+            instType: Instrument type  FUTURES OPTION
+            uly: Underlying, only applicable to FUTURES/OPTION Either uly or instFamily
+                is required. If both are passed, instFamily will be used.
+            instFamily: Instrument family, only applicable to FUTURES/OPTION Either uly or
+                instFamily is required. If both are passed, instFamily will be used.
+            after: Pagination of data to return records earlier than the requested ts
+            before: Pagination of data to return records newer than the requested ts
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/cancel-order",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/delivery-exercise-history",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def cancel_multiple_orders(
-        self, body: List[dict] = None, use_proxy: bool = False
+    def get_open_interest(
+        self,
+        instType: str,
+        uly: str = None,
+        instFamily: str = None,
+        instId: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-                        Cancel multiple orders
-                        Cancel incomplete orders in batches. Maximum 20 orders can be canceled per request. Request parameters should be passed in the form of an array.
-                        Rate Limit: 300 orders per 2 seconds
-                        Rate limit rule (except Options): UserID + Instrument ID
-                        Rate limit rule (Options only): UserID + Instrument Family
 
-        Unlike other endpoints, the rate limit of this endpoint is determined by the number of orders. If there is only one order in the request, it will consume the rate limit of `Cancel order`.
+        Retrieve the total open interest for contracts on OKX.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP +instrumentID
 
-        """
-        kwargs = body
-        details = EndpointDetails(
-            request_path="/api/v5/trade/cancel-batch-orders",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def amend_order(
-        self,
-        instId: str,
-        cxlOnFail: bool = None,
-        reqId: str = None,
-        ordId: str = None,
-        clOrdId: str = None,
-        newSz: str = None,
-        newPx: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Amend order
-        Amend an incomplete order.
-        Rate Limit: 60 requests per 2 seconds
-        Rate Limit of leading contracts: 1 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
+        Args:
+            instType: Instrument type SWAP FUTURES OPTION
+            uly: Underlying Applicable to FUTURES/SWAP/OPTION. If instType is OPTION,
+                either uly or instFamily is required.
+            instFamily: Instrument family Applicable to FUTURES/SWAP/OPTION If instType is
+                OPTION, either uly or instFamily is required.
+            instId: Instrument ID, e.g. BTC-USD-180216 Applicable to FUTURES/SWAP/OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/amend-order",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/open-interest",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def amend_multiple_orders(
-        self, body: List[dict] = None, use_proxy: bool = False
-    ) -> APIReturn:
+    def get_funding_rate(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-                        Amend multiple orders
-                        Amend incomplete orders in batches. Maximum 20 orders can be amended per request. Request parameters should be passed in the form of an array.
-                        Rate Limit: 300 orders per 2 seconds
-                        Rate Limit of leading contracts: 1 requests per 2 seconds
-                        Rate limit rule (except Options): UserID + Instrument ID
-                        Rate limit rule (Options only): UserID + Instrument Family
 
-        Unlike other endpoints, the rate limit of this endpoint is determined by the number of orders. If there is only one order in the request, it will consume the rate limit of `Amend order`.
+        Retrieve funding rate.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP +instrumentID
+
 
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP only applicable to SWAP
+        _____________
         """
-        kwargs = body
+
+        kwargs = {
+            k: v
+            for k, v in locals().items()
+            if k not in ["use_proxy", "self"] and v is not None
+        }
         details = EndpointDetails(
-            request_path="/api/v5/trade/amend-batch-orders",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/funding-rate",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def close_positions(
+    def get_funding_rate_history(
         self,
         instId: str,
-        mgnMode: str,
-        autoCxl: bool = None,
-        clOrdId: str = None,
-        tag: str = None,
-        posSide: str = None,
-        ccy: str = None,
+        before: str = None,
+        after: str = None,
+        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Close positions
-        Close all positions of an instrument via a market order.
+
+        Retrieve funding rate history. This endpoint can retrieve data from the last 3 months.
         Rate Limit: 20 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
+        Rate limit rule: IP +instrumentID
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-SWAP only applicable to SWAP
+            before: Pagination of data to return records newer than the requested
+                fundingTime
+            after: Pagination of data to return records earlier than the requested
+                fundingTime
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/close-position",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/funding-rate-history",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_order_details(
-        self,
-        instId: str,
-        ordId: str = None,
-        clOrdId: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_limit_price(self, instId: str, use_proxy: bool = False) -> APIReturn:
         """
-        Get order details
-        Retrieve order details.
-        Rate Limit: 60 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
+
+        Retrieve the highest buy limit and lowest sell limit of the instrument.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USDT-SWAP only applicable to
+                FUTURES/SWAP/OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/order",
+            request_path="/api/v5/public/price-limit",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_order_list(
+    def get_option_market_data(
         self,
-        instType: str = None,
         uly: str = None,
         instFamily: str = None,
-        instId: str = None,
-        ordType: str = None,
-        state: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
+        expTime: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get order List
-        Retrieve all incomplete orders under the current account.
-        Rate Limit: 60 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve option market data.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP +uly
+
+
+        Args:
+            uly: Underlying, only applicable to OPTION Either uly or instFamily is
+                required. If both are passed, instFamily will be used.
+            instFamily: Instrument family, only applicable to OPTION Either uly or instFamily
+                is required. If both are passed, instFamily will be used.
+            expTime: Contract expiry date, the format is "YYMMDD", e.g. "200527"
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/orders-pending",
+            request_path="/api/v5/public/opt-summary",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_order_history_last_7_days(
-        self,
-        instType: str = None,
-        uly: str = None,
-        instFamily: str = None,
-        instId: str = None,
-        ordType: str = None,
-        state: str = None,
-        category: str = None,
-        after: str = None,
-        before: str = None,
-        begin: str = None,
-        end: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
+    def get_estimated_delivery_exercise_price(
+        self, instId: str, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Get order history (last 7 days)
-        Retrieve the completed order data for the last 7 days, and the incomplete orders that have been canceled are only reserved for 2 hours.
-        Rate Limit: 40 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve the estimated delivery price which will only have a return value one hour before the delivery/exercise.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP +instId
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-200214 only applicable to FUTURES/OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/orders-history",
+            request_path="/api/v5/public/estimated-price",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_order_history_last_3_months(
-        self,
-        instType: str = None,
-        uly: str = None,
-        instFamily: str = None,
-        instId: str = None,
-        ordType: str = None,
-        state: str = None,
-        category: str = None,
-        after: str = None,
-        before: str = None,
-        begin: str = None,
-        end: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
+    def get_discount_rate_and_interest_free_quota(
+        self, ccy: str = None, discountLv: str = None, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Get order history (last 3 months)
-        Retrieve the completed order data of the last 3 months.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve discount rate level and interest-free quota.
+        Rate Limit: 2 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            ccy: Currency
+            discountLv: Discount level 1:level 1 2:level 2 3:level 3 4:level 4 5:level 5
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/orders-history-archive",
+            request_path="/api/v5/public/discount-rate-interest-free-quota",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_transaction_details_last_3_days(
-        self,
-        instType: str = None,
-        uly: str = None,
-        instFamily: str = None,
-        instId: str = None,
-        ordId: str = None,
-        after: str = None,
-        before: str = None,
-        begin: str = None,
-        end: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
+    def get_system_time(self, ts: str = None, use_proxy: bool = False) -> APIReturn:
         """
-        Get transaction details (last 3 days）
-        Retrieve recently-filled transaction details in the last 3 day.
-        Rate Limit: 60 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve API server time.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            ts: System time, Unix timestamp format in milliseconds, e.g. 1597026383085
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/fills",
+            request_path="/api/v5/public/time",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_transaction_details_last_3_months(
+    def get_mark_price(
         self,
-        instType: str = None,
+        instType: str,
         uly: str = None,
         instFamily: str = None,
         instId: str = None,
-        ordId: str = None,
-        after: str = None,
-        before: str = None,
-        begin: str = None,
-        end: str = None,
-        limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get transaction details (last 3 months)
-        Retrieve recently-filled transaction details in the last 3 months.
+
+        Retrieve mark price.
+        We set the mark price based on the SPOT index and at a reasonable basis to prevent individual users from manipulating the market and causing the contract price to fluctuate.
         Rate Limit: 10 requests per 2 seconds
-        Rate limit rule: UserID
+        Rate limit rule: IP +instrumentID
+
+
+        Args:
+            instType: Instrument type  MARGIN  SWAP FUTURES  OPTION
+            uly: Underlying Applicable to FUTURES/SWAP/OPTION
+            instFamily: Instrument family Applicable to FUTURES/SWAP/OPTION
+            instId: Instrument ID, e.g. BTC-USD-SWAP
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/fills-history",
+            request_path="/api/v5/public/mark-price",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def place_algo_order(
+    def get_position_tiers(
         self,
-        instId: str,
+        instType: str,
         tdMode: str,
-        side: str,
-        ordType: str,
-        pxSpread: str = None,
-        triggerPxType: str = None,
-        callbackRatio: str = None,
-        callbackSpread: str = None,
-        activePx: str = None,
-        pxVar: str = None,
-        szLimit: str = None,
-        triggerPx: str = None,
-        pxLimit: str = None,
-        orderPx: str = None,
-        slTriggerPxType: str = None,
-        slOrdPx: str = None,
-        slTriggerPx: str = None,
-        tpOrdPx: str = None,
-        tpTriggerPxType: str = None,
-        tpTriggerPx: str = None,
-        clOrdId: str = None,
-        tgtCcy: str = None,
-        reduceOnly: bool = None,
-        tag: str = None,
+        uly: str = None,
+        instFamily: str = None,
+        instId: str = None,
         ccy: str = None,
-        timeInterval: str = None,
-        closeFraction: str = None,
-        sz: str = None,
-        posSide: str = None,
+        tier: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Place algo order
-        The algo order includes trigger order, oco order, conditional order,iceberg order, twap order and trailing order.
-        Rate Limit: 20 requests per 2 seconds
-        Rate Limit of leading contracts: 1 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
-        """
-        kwargs = {
-            k: v
-            for k, v in locals().items()
-            if k not in ["use_proxy", "self"] and v is not None
-        }
-        details = EndpointDetails(
-            request_path="/api/v5/trade/order-algo",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def cancel_algo_order(
-        self, body: List[dict] = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Cancel algo order
-        Cancel unfilled algo orders (not including Iceberg order, TWAP order, Trailing Stop order). A maximum of 10 orders can be canceled per request. Request parameters should be passed in the form of an array.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
-        """
-        kwargs = body
-        details = EndpointDetails(
-            request_path="/api/v5/trade/cancel-algos",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
+        Retrieve position tiers information, maximum leverage depends on your borrowings and margin ratio.
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
 
-    def cancel_advance_algo_order(
-        self, body: List[dict] = None, use_proxy: bool = False
-    ) -> APIReturn:
-        """
-        Cancel advance algo order
-        Cancel unfilled algo orders (including Iceberg order, TWAP order, Trailing Stop order). A maximum of 10 orders can be canceled per request. Request parameters should be passed in the form of an array.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule (except Options): UserID + Instrument ID
-        Rate limit rule (Options only): UserID + Instrument Family
-        """
-        kwargs = body
-        details = EndpointDetails(
-            request_path="/api/v5/trade/cancel-advance-algos",
-            method="POST",
-            body=kwargs,
-            use_proxy=use_proxy,
-        )
-        return self.request(details)
 
-    def get_algo_order_list(
-        self,
-        ordType: str,
-        algoId: str = None,
-        clOrdId: str = None,
-        instType: str = None,
-        instId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
-    ) -> APIReturn:
-        """
-        Get algo order list
-        Retrieve a list of untriggered Algo orders under the current account.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
+        Args:
+            instType: Instrument type MARGIN SWAP FUTURES OPTION
+            tdMode: Trade mode Margin mode cross isolated
+            uly: Single underlying or multiple underlyings (no more than 3) separated
+                with comma. If instType is SWAP/FUTURES/OPTION, either uly or
+                instFamily is required. If both are passed, instFamily will be used.
+            instFamily: Single instrument familiy or multiple instrument families (no more
+                than 5) separated with comma. If instType is SWAP/FUTURES/OPTION,
+                either uly or instFamily is required. If both are passed, instFamily
+                will be used.
+            instId: Single instrument or multiple instruments (no more than 5) separated
+                with comma. Either instId or ccy is required, if both are passed,
+                instId will be used, ignore when instType is one of
+                SWAP,FUTURES,OPTION
+            ccy: Margin currency Only applicable to cross MARGIN. It will return
+                borrowing amount for Multi-currency margin and Portfolio margin when
+                ccy takes effect.
+            tier: Tiers
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/orders-algo-pending",
+            request_path="/api/v5/public/position-tiers",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_algo_order_history(
+    def get_interest_rate_and_loan_quota(
         self,
-        ordType: str,
-        instType: str = None,
-        instId: str = None,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        state: str = None,
-        algoId: str = None,
+        basic: list = None,
+        ccy: str = None,
+        rate: str = None,
+        quota: str = None,
+        vip: list = None,
+        level: str = None,
+        loanQuotaCoef: str = None,
+        irDiscount: str = None,
+        regular: list = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get algo order history
-        Retrieve a list of all algo orders under the current account in the last 3 months.
-        Rate Limit: 20 requests per 2 seconds
-        Rate limit rule: UserID
+
+        Retrieve interest rate
+        Rate Limit: 2 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            basic: Basic interest rate
+            ccy: Currency
+            rate: Daily rate
+            quota: Max borrow
+            vip: Interest info for vip users
+            level: VIP Level, e.g. VIP1
+            loanQuotaCoef: Loan quota coefficient
+            irDiscount: Interest rate discount
+            regular: Interest info for regular users
+            level: Regular user Level, e.g. Lv1
+            loanQuotaCoef: Loan quota coefficient
+            irDiscount: Interest rate discount
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/orders-algo-history",
+            request_path="/api/v5/public/interest-rate-loan-quota",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_easy_convert_currency_list(self, use_proxy: bool = False) -> APIReturn:
+    def get_interest_rate_and_loan_quota_for_vip_loans(
+        self,
+        ccy: str = None,
+        rate: str = None,
+        quota: str = None,
+        levelList: list = None,
+        level: str = None,
+        loanQuota: str = None,
+        use_proxy: bool = False,
+    ) -> APIReturn:
         """
-        Get easy convert currency list
-        Get list of small convertibles and mainstream currencies. Only applicable to the crypto balance less than $10.
-        Rate Limit: 1 request per 2 seconds
-        Rate limit rule: UserID
+
+        Rate Limit: 2 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            ccy: Currency, e.g. BTC
+            rate: Daily rate
+            quota: Max borrow
+            levelList: Loan quota information under different VIP levels
+            level: VIP Level, e.g. VIP5
+            loanQuota: Loan quota
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/easy-convert-currency-list",
+            request_path="/api/v5/public/vip-interest-rate-loan-quota",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def place_easy_convert(
-        self, fromCcy: list, toCcy: str, use_proxy: bool = False
-    ) -> APIReturn:
+    def get_underlying(self, instType: str, use_proxy: bool = False) -> APIReturn:
         """
-        Place easy convert
-        Convert small currencies to mainstream currencies. Only applicable to the crypto balance less than $10.
-        Rate Limit: 1 request per 2 seconds
-        Rate limit rule: UserID
+
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instType: Instrument type  SWAP FUTURES  OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/easy-convert",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/underlying",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_easy_convert_history(
+    def get_insurance_fund(
         self,
-        after: str = None,
+        instType: str,
+        type_: str = None,
+        uly: str = None,
+        instFamily: str = None,
+        ccy: str = None,
         before: str = None,
+        after: str = None,
         limit: str = None,
         use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get easy convert history
-        Get the history and status of easy convert trades.
-        Rate Limit: 1 request per 2 seconds
-        Rate limit rule: UserID
+
+        Get insurance fund balance information
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instType: Instrument type  MARGIN SWAP FUTURES  OPTION
+            type_: Type liquidation_balance_deposit bankruptcy_loss platform_revenue The
+                default is all type
+            uly: Underlying Required for FUTURES/SWAP/OPTION Either uly or instFamily
+                is required. If both are passed, instFamily will be used.
+            instFamily: Instrument family Required for FUTURES/SWAP/OPTION Either uly or
+                instFamily is required. If both are passed, instFamily will be used.
+            ccy: Currency, only applicable to MARGIN
+            before: Pagination of data to return records newer than the requested ts
+            after: Pagination of data to return records earlier than the requested ts
+            limit: Number of results per request. The maximum is 100; The default is 100
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/easy-convert-history",
+            request_path="/api/v5/public/insurance-fund",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_one_click_repay_currency_list(
-        self, debtType: str = None, use_proxy: bool = False
+    def unit_convert(
+        self,
+        instId: str,
+        sz: str,
+        type_: str = None,
+        px: str = None,
+        unit: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-        Get one-click repay currency list
-        Get list of debt currency data and repay currencies. Debt currencies include both cross and isolated debts.
-        Rate Limit: 1 request per 2 seconds
-        Rate limit rule: UserID
+
+        Convert the crypto value to the number of contracts, or vice versa
+        Rate Limit: 10 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, only applicable to FUTURES/SWAP/OPTION
+            sz: Quantity to buy or sell It is quantity of currency while converting
+                currency to contract; It is quantity of contract while contract to
+                currency. Quantity of coin needs to be positive integer
+            type_: Convert type  1: Convert currency to contract. It will be rounded up
+                when the value of contract is decimal 2: Convert contract to currency
+                The defautl is 1
+            px: Order price For crypto-margined contracts, it is necessary while
+                converting; For USDT-margined contracts, it is necessary while
+                converting between usdt and contract, it is optional while converting
+                between coin and contract. For OPTION, it is optional.
+            unit: The unit of currency. coin usds: usdt or usdc, only applicable to
+                USDⓈ-margined contracts from FUTURES/SWAP
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/one-click-repay-currency-list",
+            request_path="/api/v5/public/convert-contract-coin",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def trade_one_click_repay(
-        self, debtCcy: list, repayCcy: str, use_proxy: bool = False
+    def get_option_trades(
+        self,
+        instId: str = None,
+        instFamily: str = None,
+        optType: str = None,
+        use_proxy: bool = False,
     ) -> APIReturn:
         """
-                        Trade one-click repay
-                        Trade one-click repay to repay cross debts. Isolated debts are not applicable.
-        The maximum repayment amount is based on the remaining available balance of funding and trading accounts.
-                        Rate Limit: 1 request per 2 seconds
-                        Rate limit rule: UserID
+
+        The maximum is 100.
+        Rate Limit: 20 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instId: Instrument ID, e.g. BTC-USD-221230-4000-C, Either instId or instFamily
+                is required. If both are passed, instId will be used.
+            instFamily: Instrument family, e.g. BTC-USD
+            optType: Option type, C: Call P: put
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/one-click-repay",
-            method="POST",
-            body=kwargs,
+            request_path="/api/v5/public/option-trades",
+            method="GET",
+            params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
 
-    def get_one_click_repay_history(
-        self,
-        after: str = None,
-        before: str = None,
-        limit: str = None,
-        use_proxy: bool = False,
+    def get_option_tickbands(
+        self, instType: str, instFamily: str = None, use_proxy: bool = False
     ) -> APIReturn:
         """
-        Get one-click repay history
-        Get the history and status of one-click repay trades.
-        Rate Limit: 1 request per 2 seconds
-        Rate limit rule: UserID
+
+        Get option tickBands information
+        Rate Limit: 5 requests per 2 seconds
+        Rate limit rule: IP
+
+
+        Args:
+            instType: Instrument type OPTION
+            instFamily: Instrument family Only applicable to OPTION
+        _____________
         """
+
         kwargs = {
             k: v
             for k, v in locals().items()
             if k not in ["use_proxy", "self"] and v is not None
         }
         details = EndpointDetails(
-            request_path="/api/v5/trade/one-click-repay-history",
+            request_path="/api/v5/public/instrument-tick-bands",
             method="GET",
             params=kwargs,
             use_proxy=use_proxy,
         )
         return self.request(details)
```

### Comparing `pyokx-0.6.0/pyokx/__init__.py` & `pyokx-0.7.0/pyokx/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 from loguru import logger
 import sys
-from .Account import Account
-from .Blocktrading import Blocktrading
-from .Convert import Convert
-from .Earn import Earn
-from .Funding import Funding
-from .Gridtrading import Gridtrading
-from .Marketdata import Marketdata
-from .Publicdata import Publicdata
-from .Status import Status
-from .SubAccount import SubAccount
-from .Trade import Trade
-from .Tradingdata import Tradingdata
+from .account import Account
+from .block_trading import Blocktrading
+from .convert import Convert
+from .earn import Earn
+from .funding import Funding
+from .grid_trading import GridTrading
+from .market_data import MarketData
+from .public_data import PublicData
+from .status import Status
+from .subaccount import Subaccount
+from .trade import Trade
+from .trading_data import TradingData
 from .base import OKXClient
 
 
-__version__ = "0.4.0"
+__version__ = "0.7.0"
 
 
 def change_log_level(level: str = "INFO"):
     logger.remove()
     logger.add(sys.stdout, level=level)
 
 
@@ -27,17 +27,17 @@
 
 __all__ = [
     "Account",
     "Blocktrading",
     "Convert",
     "Earn",
     "Funding",
-    "Gridtrading",
-    "Marketdata",
-    "Publicdata",
+    "GridTrading",
+    "MarketData",
+    "PublicData",
     "Status",
-    "SubAccount",
+    "Subaccount",
     "Trade",
-    "Tradingdata",
+    "TradingData",
     "change_log_level",
     "OKXClient",
 ]
```

### Comparing `pyokx-0.6.0/pyokx/auth.py` & `pyokx-0.7.0/pyokx/auth.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/base.py` & `pyokx-0.7.0/pyokx/base.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/exceptions.py` & `pyokx-0.7.0/pyokx/exceptions.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/tests/test_auth.py` & `pyokx-0.7.0/pyokx/tests/test_auth.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyokx/tests/test_base.py` & `pyokx-0.7.0/pyokx/tests/test_base.py`

 * *Files identical despite different names*

### Comparing `pyokx-0.6.0/pyproject.toml` & `pyokx-0.7.0/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,23 +1,38 @@
 [tool.poetry]
 name = "pyokx"
-version = "0.6.0"
+version = "0.7.0"
 description = "Unofficial python wrapper for the OKX V5 API"
 authors = ["nicelgueta"]
 license = "MIT"
 readme="README.md"
 classifiers = [
     "Environment :: Console",
     "Operating System :: OS Independent",
     "Topic :: Software Development :: Documentation",
     "Topic :: Software Development :: Libraries :: Python Modules",
 ]
 include = [
     "LICENSE",
 ]
+[tool.poetry.group.dev.dependencies]
+mkdocs-material = "^9.1.8"
+mkdocstrings = "^0.21.2"
+mkdocstrings-python = "^0.9.0"
+pyyaml = "^6.0"
+mypy = "^1.3.0"
+black = "^22.3.0"
+pytest = "^7.1.2"
+pytest-cov = "^3.0.0"
+bs4 = "^0.0.1"
+types-requests = "^2.28.3"
+ipykernel = "^6.15.1"
+lxml = "^4.9.1"
+html5lib = "^1.1"
+autoflake = "^1.4"
 
 [tool.pytest.ini_options]
 addopts = "--cov=pyokx pyokx/tests/"
 
 [tool.coverage.run]
 include = [
     "pyokx/__init__.py",
@@ -36,22 +51,10 @@
 python = "^3.9"
 typeguard = "^2.13.3"
 loguru = "^0.6.0"
 requests = "^2.28.1"
 python-dotenv = "^0.20.0"
 pandas = "^1.4.3"
 
-[tool.poetry.dev-dependencies]
-black = "^22.3.0"
-pytest = "^7.1.2"
-mypy = "^0.950"
-pytest-cov = "^3.0.0"
-bs4 = "^0.0.1"
-types-requests = "^2.28.3"
-ipykernel = "^6.15.1"
-lxml = "^4.9.1"
-html5lib = "^1.1"
-autoflake = "^1.4"
-
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `pyokx-0.6.0/setup.py` & `pyokx-0.7.0/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -12,22 +12,22 @@
  'pandas>=1.4.3,<2.0.0',
  'python-dotenv>=0.20.0,<0.21.0',
  'requests>=2.28.1,<3.0.0',
  'typeguard>=2.13.3,<3.0.0']
 
 setup_kwargs = {
     'name': 'pyokx',
-    'version': '0.6.0',
+    'version': '0.7.0',
     'description': 'Unofficial python wrapper for the OKX V5 API',
     'long_description': '# pyokx \n[![Downloads](https://pepy.tech/badge/pyokx)](https://pepy.tech/project/pyokx)\n![Tests](https://github.com/nicelgueta/pyokx/actions/workflows/pyokx.yml/badge.svg)\n## Installation\n\n```shell\npip install pyokx\n```\n\n## Introduction\n\npyokx is a completely unofficial python API wrapper developed to interact with the OKX V5 API. \nIt\'s unique insofar as that it has been developed by scraping the API documentation to dynamically generate python code to provide an intuitive\npythonic interface for exact same API. This idea essentially is to avoid the need to create separate documentation for this wrapper and instead you can simply refer to the official OKX docs for API usage.\n\nIt\'s used by creating a base client instance to make and receive requests and passing that client to each API class (`APIComponent`), which has been dynamically generated from the API docs.\n\n\n**Let\'s start with an example.**\n\nLet\'s say we want to check all current positions.\n\nCheck out the docs for get balance here: https://www.okx.com/docs-v5/en/#rest-api-account-get-positions\n\nWe can see the endpoint belongs to the Account API and needs to be called with 3 parameters:\n![OKX-docs](get-pos.png)\n\nIn pyokx, you can see the method signature for the Account class is exactly the same:\n```python\ndef get_positions(\n        self,\n        instType: str = None,\n        instId: str = None,\n        posId: str = None,\n        use_proxy: bool = False,\n    ) -> APIReturn:\n```\n\nSo this can be easily implemented like so:\n\n1. Create `.env` file that contains your API information:\n```\n    KEY = replace_your_key_here\n    SECRET = replace_your_secret_here\n    PASSPHRASE = replace_your_passphrase_here\n```\n\n2. Read API information from `.env` and create the base client:\n```python\nimport os\n\n# python-dotenv should have been installed from the dependencies\nfrom dotenv import load_dotenv\nfrom pyokx import OKXClient, Account\n\n# read information from .env file\nload_dotenv()\n\n# create the base client:\nclient = OKXClient(\n    key = os.getenv(\'KEY\'),\n    secret = os.getenv(\'SECRET\'),\n    passphrase = os.getenv(\'PASSPHRASE\'),\n)\n...\n```\n\n3. Now you can create Account object and call endpoints\n```python\n...\n# create a component for the Account API by passing the client dependency\naccount = Account(client)\n\n# get positions\napi_response = account.get_positions()\n\n# you can convert to a pandas dataframe to make it more readable\ndf_response = api_response.to_df()\nprint(df_response)\n\n# or you can get the raw response\nraw_response = api_response.response\nprint(raw_response)\n```\n\nThat simple.\n\n______\n\n\n## Key features\n\n### APIReturn\n\nThis is essentially a wrapper around the response that is returned from every endpoint. This is to provide some useful helper methods such as dataframe conversion.\n\n### Proxies\n\nAs is common with a lot of exchange APIs, for calls that require authentication (usually account/trade-related), it is strongly encouraged to limit your API key to a select list IP addresses to protect your account. On some systems this may require routing traffic through a forward proxy. pyokx supports this pattern by allowing you to pass the necessary proxies to the base client and you can trigger this behaviour by setting the `use_proxy` parameter to `True`.\nFor example:\n```python\nproxies = {\n    "http": "http://your-proxy-server.com",\n    "https": "https://your-proxy-server.com",\n}\nclient = OKXClient(\n    key="key",\n    secret="secret",\n    passphrase="passphrase",\n    proxies=proxies\n)\n\n# trigger the use of the proxy server with use_proxy\naccount = Account(client)\napi_response = account.get_positions(use_proxy=True)\n\n```\n\n## Development progress\n\n**It\'s still a very early version - so issues, feature requests and bugs are very welcome!**\n\n- [x] REST API implementation.\n- [x] Fix pythonic naming conventions when API names contain special characters\n- [ ] Enhance documentation\n- [ ] Websocket API implementation. \n\n## Disclaimer\n> NB. pyokx is totally unofficial and is in no way affiliated with OKEX Crypto exchange and simply exists as a helpful wrapper to interact with the V5 API.',
     'author': 'nicelgueta',
-    'author_email': None,
-    'maintainer': None,
-    'maintainer_email': None,
-    'url': None,
+    'author_email': 'None',
+    'maintainer': 'None',
+    'maintainer_email': 'None',
+    'url': 'None',
     'packages': packages,
     'package_data': package_data,
     'install_requires': install_requires,
     'python_requires': '>=3.9,<4.0',
 }
```

### Comparing `pyokx-0.6.0/PKG-INFO` & `pyokx-0.7.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 Metadata-Version: 2.1
 Name: pyokx
-Version: 0.6.0
+Version: 0.7.0
 Summary: Unofficial python wrapper for the OKX V5 API
 License: MIT
 Author: nicelgueta
 Requires-Python: >=3.9,<4.0
 Classifier: Environment :: Console
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Documentation
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Dist: loguru (>=0.6.0,<0.7.0)
 Requires-Dist: pandas (>=1.4.3,<2.0.0)
 Requires-Dist: python-dotenv (>=0.20.0,<0.21.0)
 Requires-Dist: requests (>=2.28.1,<3.0.0)
 Requires-Dist: typeguard (>=2.13.3,<3.0.0)
```

