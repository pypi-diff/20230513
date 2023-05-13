# Comparing `tmp/binance_klines-0.1.0.tar.gz` & `tmp/binance_klines-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "binance_klines-0.1.0.tar", max compression
+gzip compressed data, was "binance_klines-0.1.1.tar", max compression
```

## Comparing `binance_klines-0.1.0.tar` & `binance_klines-0.1.1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1074 2023-04-14 09:56:25.241806 binance_klines-0.1.0/LICENSE
--rw-r--r--   0        0        0     3560 2023-05-13 16:15:29.646514 binance_klines-0.1.0/README.md
--rw-r--r--   0        0        0        0 2023-04-14 09:05:29.591522 binance_klines-0.1.0/binance_klines/__init__.py
--rw-r--r--   0        0        0     3973 2023-05-13 15:47:22.358917 binance_klines-0.1.0/binance_klines/cli.py
--rw-r--r--   0        0        0      180 2023-04-14 09:05:29.592475 binance_klines-0.1.0/binance_klines/constants.py
--rw-r--r--   0        0        0     8038 2023-05-13 16:15:50.822357 binance_klines-0.1.0/binance_klines/downloader.py
--rw-r--r--   0        0        0     1279 2023-04-15 15:43:06.755961 binance_klines-0.1.0/binance_klines/utils.py
--rw-r--r--   0        0        0      663 2023-05-13 16:35:12.081890 binance_klines-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     4458 1970-01-01 00:00:00.000000 binance_klines-0.1.0/setup.py
--rw-r--r--   0        0        0     4034 1970-01-01 00:00:00.000000 binance_klines-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1074 2023-04-14 09:56:25.241806 binance_klines-0.1.1/LICENSE
+-rw-r--r--   0        0        0     3560 2023-05-13 16:15:29.646514 binance_klines-0.1.1/README.md
+-rw-r--r--   0        0        0        0 2023-04-14 09:05:29.591522 binance_klines-0.1.1/binance_klines/__init__.py
+-rw-r--r--   0        0        0     3973 2023-05-13 15:47:22.358917 binance_klines-0.1.1/binance_klines/cli.py
+-rw-r--r--   0        0        0      180 2023-04-14 09:05:29.592475 binance_klines-0.1.1/binance_klines/constants.py
+-rw-r--r--   0        0        0     8038 2023-05-13 16:15:50.822357 binance_klines-0.1.1/binance_klines/downloader.py
+-rw-r--r--   0        0        0     1279 2023-04-15 15:43:06.755961 binance_klines-0.1.1/binance_klines/utils.py
+-rw-r--r--   0        0        0      763 2023-05-13 16:45:53.185887 binance_klines-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     4558 1970-01-01 00:00:00.000000 binance_klines-0.1.1/setup.py
+-rw-r--r--   0        0        0     4134 1970-01-01 00:00:00.000000 binance_klines-0.1.1/PKG-INFO
```

### Comparing `binance_klines-0.1.0/LICENSE` & `binance_klines-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `binance_klines-0.1.0/README.md` & `binance_klines-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `binance_klines-0.1.0/binance_klines/cli.py` & `binance_klines-0.1.1/binance_klines/cli.py`

 * *Files identical despite different names*

### Comparing `binance_klines-0.1.0/binance_klines/downloader.py` & `binance_klines-0.1.1/binance_klines/downloader.py`

 * *Files identical despite different names*

### Comparing `binance_klines-0.1.0/binance_klines/utils.py` & `binance_klines-0.1.1/binance_klines/utils.py`

 * *Files identical despite different names*

### Comparing `binance_klines-0.1.0/setup.py` & `binance_klines-0.1.1/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,16 +11,16 @@
 ['ccxt>=3.0.61,<4.0.0', 'python-dotenv>=1.0.0,<2.0.0', 'pytz>=2023.3,<2024.0']
 
 entry_points = \
 {'console_scripts': ['binance-klines = binance_klines.cli:main']}
 
 setup_kwargs = {
     'name': 'binance-klines',
-    'version': '0.1.0',
-    'description': '',
+    'version': '0.1.1',
+    'description': 'BinanceKlines - A tool to download OHLCV candlestick data (K-Lines) from Binance. Written in Python.',
     'long_description': '# BinanceKlines downloader\n\nBinanceKlines downloader is a simple command line tool and Python library used to download OHLCV k-lines from Binance. It works asynchronously to download candlestick market data from multiple symbols concurrently.\n\n\n## Installation\n\n```console\n$ git clone git@github.com:fievelk/binance-klines.git  # Clone the project\n$ cd binance-klines/\n$ pip install .\n```\n\n## Usage\n\nBinanceKlines can be used both as command line tool and Python module. The tool fetches data from Binance\'s [`GET /api/v3/klines`](https://binance-docs.github.io/apidocs/spot/en/#kline-candlestick-data) endpoint.\n\n\n### From command line\n\nYou can check all the available options using `binance-klines --help`.\n\n```console\n$ binance-klines --help\nusage: binance-klines [-h] [-v] --start-date START_DATE [--end-date END_DATE] [-o OUTPUT_DIR]\n                      [--timeframe {1m,3m,5m,15m,30m,1h,2h,4h,6h,8h,12h,1d,3d,1w,1M}]\n                      symbols [symbols ...]\n\npositional arguments:\n  symbols               The list of currencies whose OHLCV will be fetched.\n\noptions:\n  -h, --help            show this help message and exit\n  -v, --verbose         Increase output verbosity. -v: INFO, -vv: DEBUG.\n                        Default: WARNING.\n  --start-date START_DATE\n                        (Required) Start downloading data from this date. E.g.: 2019-01-24 00:00:00\n  --end-date END_DATE   Download data up to this date. E.g.: 2020-05-30 00:00:00.\n                        Default: now.\n  -o OUTPUT_DIR, --output-dir OUTPUT_DIR\n                        The data directory to store the output CSV files.\n                        Default: the current directory.\n  --timeframe {1m,3m,5m,15m,30m,1h,2h,4h,6h,8h,12h,1d,3d,1w,1M}\n                        The frequency of the OHLCV data to be downloaded.\n                        Default: 1h.\n```\n\nHere is an example of how to download 1-minutes candlestick data for BTC/USDT and ETH/USDT from 18th July 2022 to 20th July 2022:\n\n```console\n$ binance-klines --start-date "2022-07-18 00:00:00" \\\n    --end-date "2022-07-20 23:59:00" --timeframe \'1m\' --output-dir .data/ \\\n    --symbols BTC/USDT ETH/USDT\n```\n\n### As a Python module\n\n```py\nimport asyncio\nimport datetime\n\nimport pytz\n\nfrom binance_klines.downloader import BinanceKLinesDownloader\n\n\nasync def main():\n    downloader = BinanceKLinesDownloader()\n    start_date = datetime.datetime(2020, 9, 1).replace(tzinfo=pytz.utc)\n    end_date = datetime.datetime(2020, 9, 2).replace(tzinfo=pytz.utc)\n\n    # Download data for a single symbol. Data is downloaded in batches.\n    results = await downloader.fetch_klines(\n        symbols=["BTC/USDT", "ETH/USDT"],\n        start_date=start_date,\n        end_date=end_date,\n        timeframe="30m",\n    )\n\n    # Results contain the klines for each symbol, in the order that was passed to the\n    # `symbols` argument.\n    btc_batches = results[0]\n    eth_batches = results[1]\n\n\nif __name__ == "__main__":\n    asyncio.run(main())\n```\n\n## Tests\n\nTests are written using `pytest`. To test compatibility among several Python versions, install the dev dependencies using Poetry and run tests using tox:\n\n```console\n$ poetry install --with dev  # Install dependencies\n$ poetry shell  # Activate Poetry environment\n$ tox\n```\n\n## Contributing\n\nYou are welcome to contribute by opening a PR with your improvements. Please make sure to run the Black linter before you do. You can use `tox` for this:\n\n```console\n$ tox -e lint\n```\n\n\n# TODO\n\n- [ ] Change logging of utils.timeit to DEBUG\n- [ ] Remove ccxt and use aiohttp directly\n',
     'author': 'Pierpaolo Pantone',
     'author_email': '24alsecondo@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
     'packages': packages,
```

### Comparing `binance_klines-0.1.0/PKG-INFO` & `binance_klines-0.1.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: binance-klines
-Version: 0.1.0
-Summary: 
+Version: 0.1.1
+Summary: BinanceKlines - A tool to download OHLCV candlestick data (K-Lines) from Binance. Written in Python.
 Author: Pierpaolo Pantone
 Author-email: 24alsecondo@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: ccxt (>=3.0.61,<4.0.0)
```

