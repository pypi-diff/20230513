# Comparing `tmp/lixinger-0.1.7.tar.gz` & `tmp/lixinger-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lixinger-0.1.7.tar", last modified: Wed May 10 14:14:40 2023, max compression
+gzip compressed data, was "lixinger-0.1.8.tar", last modified: Sat May 13 04:19:31 2023, max compression
```

## Comparing `lixinger-0.1.7.tar` & `lixinger-0.1.8.tar`

### file list

```diff
@@ -1,50 +1,58 @@
--rw-r--r--   0        0        0     1502 2023-05-10 14:14:08.343659 lixinger-0.1.7/README.md
--rw-r--r--   0        0        0        0 2023-05-01 04:05:58.277552 lixinger-0.1.7/lixinger/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:33:35.225361 lixinger-0.1.7/lixinger/api/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:08:22.152169 lixinger-0.1.7/lixinger/api/cn/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:09:36.967425 lixinger-0.1.7/lixinger/api/cn/company/__init__.py
--rw-r--r--   0        0        0     1849 2023-05-10 13:59:47.866336 lixinger-0.1.7/lixinger/api/cn/company/base.py
--rw-r--r--   0        0        0     1220 2023-05-10 14:14:09.173725 lixinger-0.1.7/lixinger/api/cn/company/block_deal.py
--rw-r--r--   0        0        0     1604 2023-05-10 14:14:09.173340 lixinger-0.1.7/lixinger/api/cn/company/candlestick.py
--rw-r--r--   0        0        0     1793 2023-05-10 14:14:09.173817 lixinger-0.1.7/lixinger/api/cn/company/dividend_and_alloment.py
--rw-r--r--   0        0        0     1164 2023-05-10 14:14:09.173179 lixinger-0.1.7/lixinger/api/cn/company/equity_change.py
--rw-r--r--   0        0        0      841 2023-05-10 14:14:09.108533 lixinger-0.1.7/lixinger/api/cn/company/indices.py
--rw-r--r--   0        0        0      850 2023-05-10 14:14:09.109062 lixinger-0.1.7/lixinger/api/cn/company/industries.py
--rw-r--r--   0        0        0     2004 2023-05-10 14:14:09.173348 lixinger-0.1.7/lixinger/api/cn/company/pledge.py
--rw-r--r--   0        0        0     1351 2023-05-10 14:14:09.173556 lixinger-0.1.7/lixinger/api/cn/company/senior_executive_shares_change.py
--rw-r--r--   0        0        0     1000 2023-05-10 14:14:09.173795 lixinger-0.1.7/lixinger/api/cn/company/shareholders_num.py
--rw-r--r--   0        0        0        0 2023-05-04 14:21:25.826889 lixinger-0.1.7/lixinger/api/cn/fund/__init__.py
--rw-r--r--   0        0        0     1136 2023-05-10 14:14:09.173426 lixinger-0.1.7/lixinger/api/cn/fund/exchange_traded_close_price.py
--rw-r--r--   0        0        0     1011 2023-05-10 14:14:09.173179 lixinger-0.1.7/lixinger/api/cn/fund/total_net_value.py
--rw-r--r--   0        0        0        0 2023-05-01 05:10:55.043163 lixinger-0.1.7/lixinger/api/cn/index/__init__.py
--rw-r--r--   0        0        0     1280 2023-05-10 14:14:09.173306 lixinger-0.1.7/lixinger/api/cn/index/candlestick.py
--rw-r--r--   0        0        0     1511 2023-05-10 14:14:09.173214 lixinger-0.1.7/lixinger/api/cn/index/fundamental.py
--rw-r--r--   0        0        0        0 2023-05-01 04:08:31.838744 lixinger-0.1.7/lixinger/api/hk/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:09:00.179536 lixinger-0.1.7/lixinger/api/macro/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:08:44.656824 lixinger-0.1.7/lixinger/api/us/__init__.py
--rw-r--r--   0        0        0     1644 2023-05-10 14:14:18.924307 lixinger-0.1.7/lixinger/config.py
--rw-r--r--   0        0        0        0 2023-05-03 09:27:58.212202 lixinger-0.1.7/lixinger/py.typed
--rw-r--r--   0        0        0       75 2023-05-03 10:06:41.922780 lixinger-0.1.7/lixinger/settings.toml
--rw-r--r--   0        0        0     5724 2023-05-10 14:14:09.115003 lixinger-0.1.7/lixinger/utils.py
--rw-r--r--   0        0        0      912 2023-05-10 14:14:40.078071 lixinger-0.1.7/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-01 04:43:15.660305 lixinger-0.1.7/tests/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:43:19.505533 lixinger-0.1.7/tests/api/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:43:24.536685 lixinger-0.1.7/tests/api/cn/__init__.py
--rw-r--r--   0        0        0        0 2023-05-01 04:43:30.757795 lixinger-0.1.7/tests/api/cn/company/__init__.py
--rw-r--r--   0        0        0      127 2023-05-10 13:55:25.017569 lixinger-0.1.7/tests/api/cn/company/test_base.py
--rw-r--r--   0        0        0      164 2023-05-08 14:09:59.839924 lixinger-0.1.7/tests/api/cn/company/test_block_deal.py
--rw-r--r--   0        0        0      187 2023-05-10 14:12:30.362480 lixinger-0.1.7/tests/api/cn/company/test_candlestick.py
--rw-r--r--   0        0        0      217 2023-05-06 05:43:46.770904 lixinger-0.1.7/tests/api/cn/company/test_dividend_and_alloment.py
--rw-r--r--   0        0        0      170 2023-05-06 02:12:57.131245 lixinger-0.1.7/tests/api/cn/company/test_equity_change.py
--rw-r--r--   0        0        0      127 2023-05-09 12:28:07.598154 lixinger-0.1.7/tests/api/cn/company/test_indices.py
--rw-r--r--   0        0        0      139 2023-05-10 12:17:30.914094 lixinger-0.1.7/tests/api/cn/company/test_industries.py
--rw-r--r--   0        0        0      144 2023-05-08 14:53:32.432310 lixinger-0.1.7/tests/api/cn/company/test_pledge.py
--rw-r--r--   0        0        0      235 2023-05-07 15:03:11.303695 lixinger-0.1.7/tests/api/cn/company/test_senior_executive_shares_change.py
--rw-r--r--   0        0        0      184 2023-05-07 14:29:15.357398 lixinger-0.1.7/tests/api/cn/company/test_shareholders_num.py
--rw-r--r--   0        0        0        0 2023-05-04 14:30:00.736254 lixinger-0.1.7/tests/api/cn/fund/__init__.py
--rw-r--r--   0        0        0      238 2023-05-07 02:06:30.724314 lixinger-0.1.7/tests/api/cn/fund/test_exchange_traded_close_price.py
--rw-r--r--   0        0        0      229 2023-05-04 14:32:35.703103 lixinger-0.1.7/tests/api/cn/fund/test_total_net_value.py
--rw-r--r--   0        0        0        0 2023-05-01 05:16:11.323717 lixinger-0.1.7/tests/api/cn/index/__init__.py
--rw-r--r--   0        0        0      182 2023-05-07 01:58:13.309631 lixinger-0.1.7/tests/api/cn/index/test_candlestick.py
--rw-r--r--   0        0        0      270 2023-05-10 13:23:11.920162 lixinger-0.1.7/tests/api/cn/index/test_fundamental.py
--rw-r--r--   0        0        0     2121 1970-01-01 00:00:00.000000 lixinger-0.1.7/PKG-INFO
+-rw-r--r--   0        0        0     1541 2023-05-13 04:11:28.122994 lixinger-0.1.8/README.md
+-rw-r--r--   0        0        0        0 2023-05-01 04:05:58.277552 lixinger-0.1.8/lixinger/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:33:35.225361 lixinger-0.1.8/lixinger/api/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:08:22.152169 lixinger-0.1.8/lixinger/api/cn/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:09:36.967425 lixinger-0.1.8/lixinger/api/cn/company/__init__.py
+-rw-r--r--   0        0        0     1859 2023-05-13 04:08:14.276289 lixinger-0.1.8/lixinger/api/cn/company/base.py
+-rw-r--r--   0        0        0     1230 2023-05-13 04:19:14.460488 lixinger-0.1.8/lixinger/api/cn/company/block_deal.py
+-rw-r--r--   0        0        0     1614 2023-05-13 04:19:14.460546 lixinger-0.1.8/lixinger/api/cn/company/candlestick.py
+-rw-r--r--   0        0        0     1803 2023-05-13 04:19:14.460598 lixinger-0.1.8/lixinger/api/cn/company/dividend_and_alloment.py
+-rw-r--r--   0        0        0     1174 2023-05-13 04:19:14.460648 lixinger-0.1.8/lixinger/api/cn/company/equity_change.py
+-rw-r--r--   0        0        0      851 2023-05-13 04:19:14.460700 lixinger-0.1.8/lixinger/api/cn/company/indices.py
+-rw-r--r--   0        0        0      860 2023-05-13 04:19:14.460763 lixinger-0.1.8/lixinger/api/cn/company/industries.py
+-rw-r--r--   0        0        0     2014 2023-05-13 04:19:14.460814 lixinger-0.1.8/lixinger/api/cn/company/pledge.py
+-rw-r--r--   0        0        0     1361 2023-05-13 04:19:14.460866 lixinger-0.1.8/lixinger/api/cn/company/senior_executive_shares_change.py
+-rw-r--r--   0        0        0     1010 2023-05-13 04:19:14.460914 lixinger-0.1.8/lixinger/api/cn/company/shareholders_num.py
+-rw-r--r--   0        0        0        0 2023-05-04 14:21:25.826889 lixinger-0.1.8/lixinger/api/cn/fund/__init__.py
+-rw-r--r--   0        0        0     1146 2023-05-13 04:19:14.460966 lixinger-0.1.8/lixinger/api/cn/fund/exchange_traded_close_price.py
+-rw-r--r--   0        0        0     1021 2023-05-13 04:19:14.461016 lixinger-0.1.8/lixinger/api/cn/fund/total_net_value.py
+-rw-r--r--   0        0        0        0 2023-05-01 05:10:55.043163 lixinger-0.1.8/lixinger/api/cn/index/__init__.py
+-rw-r--r--   0        0        0     1630 2023-05-13 04:19:14.461073 lixinger-0.1.8/lixinger/api/cn/index/base.py
+-rw-r--r--   0        0        0     1290 2023-05-13 04:19:14.461123 lixinger-0.1.8/lixinger/api/cn/index/candlestick.py
+-rw-r--r--   0        0        0     1279 2023-05-13 04:19:14.461171 lixinger-0.1.8/lixinger/api/cn/index/constituents.py
+-rw-r--r--   0        0        0     1002 2023-05-13 04:19:14.461221 lixinger-0.1.8/lixinger/api/cn/index/drawdown.py
+-rw-r--r--   0        0        0     1521 2023-05-13 04:19:14.461272 lixinger-0.1.8/lixinger/api/cn/index/fundamental.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:08:31.838744 lixinger-0.1.8/lixinger/api/hk/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:09:00.179536 lixinger-0.1.8/lixinger/api/macro/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:08:44.656824 lixinger-0.1.8/lixinger/api/us/__init__.py
+-rw-r--r--   0        0        0      520 2023-05-13 04:19:14.461320 lixinger-0.1.8/lixinger/client.py
+-rw-r--r--   0        0        0     1644 2023-05-10 14:14:18.924307 lixinger-0.1.8/lixinger/config.py
+-rw-r--r--   0        0        0        0 2023-05-03 09:27:58.212202 lixinger-0.1.8/lixinger/py.typed
+-rw-r--r--   0        0        0       75 2023-05-03 10:06:41.922780 lixinger-0.1.8/lixinger/settings.toml
+-rw-r--r--   0        0        0     5700 2023-05-13 03:33:48.391570 lixinger-0.1.8/lixinger/utils.py
+-rw-r--r--   0        0        0      935 2023-05-13 04:19:31.962265 lixinger-0.1.8/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-01 04:43:15.660305 lixinger-0.1.8/tests/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:43:19.505533 lixinger-0.1.8/tests/api/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:43:24.536685 lixinger-0.1.8/tests/api/cn/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-01 04:43:30.757795 lixinger-0.1.8/tests/api/cn/company/__init__.py
+-rw-r--r--   0        0        0      127 2023-05-10 13:55:25.017569 lixinger-0.1.8/tests/api/cn/company/test_base.py
+-rw-r--r--   0        0        0      164 2023-05-08 14:09:59.839924 lixinger-0.1.8/tests/api/cn/company/test_block_deal.py
+-rw-r--r--   0        0        0      187 2023-05-10 14:12:30.362480 lixinger-0.1.8/tests/api/cn/company/test_candlestick.py
+-rw-r--r--   0        0        0      217 2023-05-06 05:43:46.770904 lixinger-0.1.8/tests/api/cn/company/test_dividend_and_alloment.py
+-rw-r--r--   0        0        0      170 2023-05-06 02:12:57.131245 lixinger-0.1.8/tests/api/cn/company/test_equity_change.py
+-rw-r--r--   0        0        0      127 2023-05-09 12:28:07.598154 lixinger-0.1.8/tests/api/cn/company/test_indices.py
+-rw-r--r--   0        0        0      139 2023-05-10 12:17:30.914094 lixinger-0.1.8/tests/api/cn/company/test_industries.py
+-rw-r--r--   0        0        0      144 2023-05-08 14:53:32.432310 lixinger-0.1.8/tests/api/cn/company/test_pledge.py
+-rw-r--r--   0        0        0      235 2023-05-07 15:03:11.303695 lixinger-0.1.8/tests/api/cn/company/test_senior_executive_shares_change.py
+-rw-r--r--   0        0        0      184 2023-05-07 14:29:15.357398 lixinger-0.1.8/tests/api/cn/company/test_shareholders_num.py
+-rw-r--r--   0        0        0        0 2023-05-04 14:30:00.736254 lixinger-0.1.8/tests/api/cn/fund/__init__.py
+-rw-r--r--   0        0        0      238 2023-05-07 02:06:30.724314 lixinger-0.1.8/tests/api/cn/fund/test_exchange_traded_close_price.py
+-rw-r--r--   0        0        0      229 2023-05-04 14:32:35.703103 lixinger-0.1.8/tests/api/cn/fund/test_total_net_value.py
+-rw-r--r--   0        0        0        0 2023-05-01 05:16:11.323717 lixinger-0.1.8/tests/api/cn/index/__init__.py
+-rw-r--r--   0        0        0      119 2023-05-11 15:51:33.137778 lixinger-0.1.8/tests/api/cn/index/test_base.py
+-rw-r--r--   0        0        0      182 2023-05-07 01:58:13.309631 lixinger-0.1.8/tests/api/cn/index/test_candlestick.py
+-rw-r--r--   0        0        0      196 2023-05-13 03:50:07.787874 lixinger-0.1.8/tests/api/cn/index/test_constituents.py
+-rw-r--r--   0        0        0      212 2023-05-12 15:25:25.088245 lixinger-0.1.8/tests/api/cn/index/test_drawdown.py
+-rw-r--r--   0        0        0      270 2023-05-10 13:23:11.920162 lixinger-0.1.8/tests/api/cn/index/test_fundamental.py
+-rw-r--r--   0        0        0      112 2023-05-13 03:56:27.328013 lixinger-0.1.8/tests/conftest.py
+-rw-r--r--   0        0        0     2191 1970-01-01 00:00:00.000000 lixinger-0.1.8/PKG-INFO
```

### Comparing `lixinger-0.1.7/README.md` & `lixinger-0.1.8/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,50 +1,51 @@
 # lixinger
 
 理杏仁 Python SDK (非官方).
 
-包含以下功能：
+包含以下功能:
 
 - 自动将请求结果转换结果为 Dataframe.
 - 根据官方文档中的返回结果定义, 验证请求结果, 对缺少的列进行补齐, 对列类型进行相应转换.
-- 支持一次获取时间范围大于 10 年的数据.
-- 适当缓存请求结果，减少请求 API 次数.
+- 支持一次性获取时间范围大于 10 年的数据.
+- 适当缓存请求结果, 减少请求 API 次数.
+- 遇到网络错误时, 自动重试请求.
 
 ## 安装
 
 ```bash
 pip install lixinger
 ```
 
 ## 用法
 
 ### 设置 Token
 
-Token 获取地址为 [https://www.lixinger.com/open/api/token](https://www.lixinger.com/open/api/token)
+Token 获取地址为 [https://www.lixinger.com/open/api/token](https://www.lixinger.com/open/api/token).
 
-#### 方式 1：通过环境变量来设置 Token
+#### 方式 1: 通过环境变量来设置 Token
 
 ```bash
 export LIXINGER_TOKEN="你的 token"
 ```
 
-#### 方式 2：通过配置文件来设置 Token
+#### 方式 2: 通过配置文件来设置 Token
 
-打开配置文件（路径为 ~/.config/lixinger/settings.toml），并添加以下内容设置自己的 Token.
+打开配置文件(路径为 ~/.config/lixinger/settings.toml), 并添加以下内容设置自己的 Token.
 
 ```toml
 [default]
 token = "你的 token"
 ```
 
 ### 调用 API
 
-使用文档请参考 [理杏仁开放平台](https://www.lixinger.com/open/api/doc)
+使用文档请参考 [理杏仁开放平台](https://www.lixinger.com/open/api/doc).
 
-方法导入路径可以根据文档中的请求 URL 得出，例如下面代码中对应的请求 URL 为 `/api/cn/company` 则把 `/` 换成 `.` 即可.
+方法导入路径可以根据文档中的请求 URL 得出, 例如下面代码中对应的请求 URL 为 `/api/cn/company` 则把 `/` 换成 `.` 即可.
 
 ```python
 from lixinger.api.cn.company.base import get_company
 
 # 获取股票详细信息
 company = get_company(stock_codes=["600519"])
 print(company)
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/base.py` & `lixinger-0.1.8/lixinger/api/cn/company/base.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import annotations
 
 from typing import Literal, Optional
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, convert_column_list_to_str, get_response_df
 
 
 class Output(pa.DataFrameModel):
     name: pa.typing.Series[str] = pa.Field(nullable=True)
     stock_code: pa.typing.Series[str]
@@ -44,15 +44,15 @@
     if mutual_markets is not None:
         payload["mutualMarkets"] = mutual_markets
     if stock_codes is not None:
         payload["stockCodes"] = stock_codes
     if include_delisted is not None:
         payload["includeDelisted"] = include_delisted
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company",
         json=payload,
     )
     df = get_response_df(response, Output)
 
     if "mutual_markets" in df.columns:
         df["mutual_markets"] = [
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/block_deal.py` & `lixinger-0.1.8/lixinger/api/cn/company/block_deal.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     trading_price: pa.typing.Series[float]
@@ -34,13 +34,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/block-deal",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/candlestick.py` & `lixinger-0.1.8/lixinger/api/cn/company/candlestick.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import annotations
 
 from typing import Literal
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     open: pa.typing.Series[float]
@@ -45,13 +45,13 @@
     if limit is not None:
         payload["limit"] = limit
     if adjust_forward_date is not None:
         payload["adjustForwardDate"] = adjust_forward_date
     if adjust_backward_date is not None:
         payload["adjustBackwardDate"] = adjust_backward_date
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/candlestick",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/dividend_and_alloment.py` & `lixinger-0.1.8/lixinger/api/cn/company/dividend_and_alloment.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from __future__ import annotations
 
 import pandas as pd
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     bonus_shares_from_profit: pa.typing.Series[int]
@@ -39,15 +39,15 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/dividend-and-alloment",
         json=payload,
     )
     df = get_response_df(response, Output)
     df["date"] = pd.to_datetime(df["date"]).dt.tz_localize(None) + pd.Timedelta("8h")
     df["ex_date"] = pd.to_datetime(df["ex_date"]).dt.tz_localize(None) + pd.Timedelta(
         "8h"
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/equity_change.py` & `lixinger-0.1.8/lixinger/api/cn/company/equity_change.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     change_reason: pa.typing.Series[str]
@@ -32,13 +32,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/equity-change",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/indices.py` & `lixinger-0.1.8/lixinger/api/cn/company/indices.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     area_code: pa.typing.Series[str]
     stock_code: pa.typing.Series[str]
@@ -25,12 +25,12 @@
     payload = {
         "token": settings.token,
         "stockCode": stock_code,
     }
     if date is not None:
         payload["date"] = date
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/indices",
         json=payload,
     )
     return get_response_df(response, Output)
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/industries.py` & `lixinger-0.1.8/lixinger/api/cn/company/shareholders_num.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,36 +1,41 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
-    area_code: pa.typing.Series[str]
-    stock_code: pa.typing.Series[str]
-    source: pa.typing.Series[str]
+    date: pa.typing.Series[pa.typing.DateTime]
+    num: pa.typing.Series[int]
 
 
 @api
-def get_industries(
+def get_shareholders_num(
+    start_date: str,
     stock_code: str,
-    date: str | None = None,
+    end_date: str | None = None,
+    limit: int | None = None,
 ) -> pa.typing.DataFrame[Output]:
-    """获取股票所属行业信息.
+    """获取股东人数数据
 
-    参考文档: https://www.lixinger.com/open/api/doc?api-key=cn/company/industries
+    参考文档: https://www.lixinger.com/open/api/doc?api-key=cn/company/shareholders-num
     """
     payload = {
         "token": settings.token,
+        "startDate": start_date,
         "stockCode": stock_code,
     }
-    if date is not None:
-        payload["date"] = date
+    if end_date is not None:
+        payload["endDate"] = end_date
+    if limit is not None:
+        payload["limit"] = limit
 
-    response = requests.post(
-        f"{settings.base_url}/cn/company/industries",
+    response = client.post(
+        f"{settings.base_url}/cn/company/shareholders-num",
         json=payload,
     )
-    return get_response_df(response, Output)
+    df = get_response_df(response, Output)
+    return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/pledge.py` & `lixinger-0.1.8/lixinger/api/cn/company/pledge.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     pledgor: pa.typing.Series[str] = pa.Field(nullable=True)
@@ -45,13 +45,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/block-deal",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/senior_executive_shares_change.py` & `lixinger-0.1.8/lixinger/api/cn/company/senior_executive_shares_change.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     shareholder_name: pa.typing.Series[str]
     executive_name: pa.typing.Series[str]
@@ -36,13 +36,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/company/senior-executive-shares-change",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/company/shareholders_num.py` & `lixinger-0.1.8/lixinger/api/cn/company/industries.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,41 +1,36 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
-    date: pa.typing.Series[pa.typing.DateTime]
-    num: pa.typing.Series[int]
+    area_code: pa.typing.Series[str]
+    stock_code: pa.typing.Series[str]
+    source: pa.typing.Series[str]
 
 
 @api
-def get_shareholders_num(
-    start_date: str,
+def get_industries(
     stock_code: str,
-    end_date: str | None = None,
-    limit: int | None = None,
+    date: str | None = None,
 ) -> pa.typing.DataFrame[Output]:
-    """获取股东人数数据
+    """获取股票所属行业信息.
 
-    参考文档: https://www.lixinger.com/open/api/doc?api-key=cn/company/shareholders-num
+    参考文档: https://www.lixinger.com/open/api/doc?api-key=cn/company/industries
     """
     payload = {
         "token": settings.token,
-        "startDate": start_date,
         "stockCode": stock_code,
     }
-    if end_date is not None:
-        payload["endDate"] = end_date
-    if limit is not None:
-        payload["limit"] = limit
+    if date is not None:
+        payload["date"] = date
 
-    response = requests.post(
-        f"{settings.base_url}/cn/company/shareholders-num",
+    response = client.post(
+        f"{settings.base_url}/cn/company/industries",
         json=payload,
     )
-    df = get_response_df(response, Output)
-    return df
+    return get_response_df(response, Output)
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/fund/exchange_traded_close_price.py` & `lixinger-0.1.8/lixinger/api/cn/fund/exchange_traded_close_price.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     open: pa.typing.Series[float]
@@ -32,13 +32,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/fund/exchange-traded-close-price",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/fund/total_net_value.py` & `lixinger-0.1.8/lixinger/api/cn/fund/total_net_value.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     total_net_value: pa.typing.Series[float]
@@ -29,13 +29,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/fund/total-net-value",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/index/candlestick.py` & `lixinger-0.1.8/lixinger/api/cn/index/candlestick.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import annotations
 
 from typing import Literal
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     open: pa.typing.Series[float]
@@ -39,13 +39,13 @@
         "stockCode": stock_code,
     }
     if end_date is not None:
         payload["endDate"] = end_date
     if limit is not None:
         payload["limit"] = limit
 
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/index/candlestick",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/api/cn/index/fundamental.py` & `lixinger-0.1.8/lixinger/api/cn/index/fundamental.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import pandera as pa
-import requests
 
+from lixinger import client
 from lixinger.config import settings
 from lixinger.utils import api, get_response_df
 
 
 class Output(pa.DataFrameModel):
     date: pa.typing.Series[pa.typing.DateTime]
     stock_code: pa.typing.Series[str]
@@ -40,13 +40,13 @@
         payload["endDate"] = end_date
     if adjust_forward_date is not None:
         payload["adjustForwardDate"] = adjust_forward_date
     if adjust_backward_date is not None:
         payload["adjustBackwardDate"] = adjust_backward_date
     if limit is not None:
         payload["limit"] = limit
-    response = requests.post(
+    response = client.post(
         f"{settings.base_url}/cn/index/fundamental",
         json=payload,
     )
     df = get_response_df(response, Output)
     return df
```

### Comparing `lixinger-0.1.7/lixinger/config.py` & `lixinger-0.1.8/lixinger/config.py`

 * *Files identical despite different names*

### Comparing `lixinger-0.1.7/lixinger/utils.py` & `lixinger-0.1.8/lixinger/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -161,15 +161,14 @@
 
 def api(func: Callable | None = None, *, maxsize=16) -> Callable:
     """API decorator."""
 
     def wrapper(_func: Callable) -> Callable:
         @hashable_cache(maxsize=maxsize)
         @validate_arguments
-        @pa.check_types
         @wraps(_func)
         def _api(*args: any, **kwargs: any) -> Callable:
             parameters = inspect.signature(_func).parameters
             if "start_date" in parameters and "end_date" in parameters:
                 return adjust_request_date_range(_func)(*args, **kwargs)
             return _func(*args, **kwargs)
```

### Comparing `lixinger-0.1.7/pyproject.toml` & `lixinger-0.1.8/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -7,24 +7,25 @@
 [tool.pytest.ini_options]
 cache_dir = ".pytest_cache/"
 addopts = "-s -p no:warnings"
 asyncio_mode = "auto"
 
 [project]
 name = "lixinger"
-version = "0.1.7"
+version = "0.1.8"
 description = "Lixinger SDK for Python (Unofficial)"
 authors = [
     { name = "Chaoying", email = "chaoying2022@gmail.com" },
 ]
 dependencies = [
     "pandera>=0.14.5",
     "pydantic>=1.10.7",
     "requests>=2.29.0",
     "dynaconf>=3.1.12",
+    "tenacity>=8.2.2",
 ]
 requires-python = ">=3.8"
 readme = "README.md"
 keywords = [
     "lixinger",
 ]
 classifiers = [
```

### Comparing `lixinger-0.1.7/PKG-INFO` & `lixinger-0.1.8/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,69 +1,71 @@
 Metadata-Version: 2.1
 Name: lixinger
-Version: 0.1.7
+Version: 0.1.8
 Summary: Lixinger SDK for Python (Unofficial)
 Keywords: lixinger
 Author-Email: Chaoying <chaoying2022@gmail.com>
 License: MIT
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.8
 Requires-Dist: pandera>=0.14.5
 Requires-Dist: pydantic>=1.10.7
 Requires-Dist: requests>=2.29.0
 Requires-Dist: dynaconf>=3.1.12
+Requires-Dist: tenacity>=8.2.2
 Description-Content-Type: text/markdown
 
 # lixinger
 
 理杏仁 Python SDK (非官方).
 
-包含以下功能：
+包含以下功能:
 
 - 自动将请求结果转换结果为 Dataframe.
 - 根据官方文档中的返回结果定义, 验证请求结果, 对缺少的列进行补齐, 对列类型进行相应转换.
-- 支持一次获取时间范围大于 10 年的数据.
-- 适当缓存请求结果，减少请求 API 次数.
+- 支持一次性获取时间范围大于 10 年的数据.
+- 适当缓存请求结果, 减少请求 API 次数.
+- 遇到网络错误时, 自动重试请求.
 
 ## 安装
 
 ```bash
 pip install lixinger
 ```
 
 ## 用法
 
 ### 设置 Token
 
-Token 获取地址为 [https://www.lixinger.com/open/api/token](https://www.lixinger.com/open/api/token)
+Token 获取地址为 [https://www.lixinger.com/open/api/token](https://www.lixinger.com/open/api/token).
 
-#### 方式 1：通过环境变量来设置 Token
+#### 方式 1: 通过环境变量来设置 Token
 
 ```bash
 export LIXINGER_TOKEN="你的 token"
 ```
 
-#### 方式 2：通过配置文件来设置 Token
+#### 方式 2: 通过配置文件来设置 Token
 
-打开配置文件（路径为 ~/.config/lixinger/settings.toml），并添加以下内容设置自己的 Token.
+打开配置文件(路径为 ~/.config/lixinger/settings.toml), 并添加以下内容设置自己的 Token.
 
 ```toml
 [default]
 token = "你的 token"
 ```
 
 ### 调用 API
 
-使用文档请参考 [理杏仁开放平台](https://www.lixinger.com/open/api/doc)
+使用文档请参考 [理杏仁开放平台](https://www.lixinger.com/open/api/doc).
 
-方法导入路径可以根据文档中的请求 URL 得出，例如下面代码中对应的请求 URL 为 `/api/cn/company` 则把 `/` 换成 `.` 即可.
+方法导入路径可以根据文档中的请求 URL 得出, 例如下面代码中对应的请求 URL 为 `/api/cn/company` 则把 `/` 换成 `.` 即可.
 
 ```python
 from lixinger.api.cn.company.base import get_company
 
 # 获取股票详细信息
 company = get_company(stock_codes=["600519"])
 print(company)
```

