# Comparing `tmp/dali-rp2-0.6.8.tar.gz` & `tmp/dali-rp2-0.6.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dali-rp2-0.6.8.tar", last modified: Sun Apr  9 03:08:33 2023, max compression
+gzip compressed data, was "dali-rp2-0.6.9.tar", last modified: Sat May 13 14:16:02 2023, max compression
```

## Comparing `dali-rp2-0.6.8.tar` & `dali-rp2-0.6.9.tar`

### file list

```diff
@@ -1,101 +1,103 @@
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.038009 dali-rp2-0.6.8/
--rw-r--r--   0 marcoz     (501) staff       (20)    10454 2023-04-09 02:57:20.000000 dali-rp2-0.6.8/CHANGELOG.md
--rw-r--r--   0 marcoz     (501) staff       (20)     3098 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/CONTRIBUTING.md
--rw-r--r--   0 marcoz     (501) staff       (20)    11357 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/LICENSE
--rw-r--r--   0 marcoz     (501) staff       (20)      214 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/MANIFEST.in
--rw-r--r--   0 marcoz     (501) staff       (20)    22439 2023-04-09 03:08:33.038101 dali-rp2-0.6.8/PKG-INFO
--rw-r--r--   0 marcoz     (501) staff       (20)    25113 2023-04-09 02:57:52.000000 dali-rp2-0.6.8/README.dev.md
--rw-r--r--   0 marcoz     (501) staff       (20)    10422 2023-04-09 02:57:52.000000 dali-rp2-0.6.8/README.md
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.015135 dali-rp2-0.6.8/docs/
--rw-r--r--   0 marcoz     (501) staff       (20)    43363 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/docs/configuration_file.md
--rw-r--r--   0 marcoz     (501) staff       (20)     7936 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/docs/developer_faq.md
--rw-r--r--   0 marcoz     (501) staff       (20)     9765 2023-03-15 01:40:20.000000 dali-rp2-0.6.8/docs/user_faq.md
--rw-r--r--   0 marcoz     (501) staff       (20)      276 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/pyproject.toml
--rw-r--r--   0 marcoz     (501) staff       (20)     2227 2023-04-09 03:08:33.039127 dali-rp2-0.6.8/setup.cfg
--rw-r--r--   0 marcoz     (501) staff       (20)       92 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/setup.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.009644 dali-rp2-0.6.8/src/
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.020733 dali-rp2-0.6.8/src/dali/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/__init__.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)    32063 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/abstract_ccxt_input_plugin.py
--rw-r--r--   0 marcoz     (501) staff       (20)     2682 2023-03-15 01:25:21.000000 dali-rp2-0.6.8/src/dali/abstract_input_plugin.py
--rw-r--r--   0 marcoz     (501) staff       (20)    11488 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/abstract_pair_converter_plugin.py
--rw-r--r--   0 marcoz     (501) staff       (20)     9563 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/abstract_transaction.py
--rw-r--r--   0 marcoz     (501) staff       (20)     1393 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/cache.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     8482 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/ccxt_pagination.py
--rw-r--r--   0 marcoz     (501) staff       (20)     7310 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/configuration.py
--rw-r--r--   0 marcoz     (501) staff       (20)     3792 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/configuration_generator.py
--rw-r--r--   0 marcoz     (501) staff       (20)    18169 2023-04-09 02:57:52.000000 dali-rp2-0.6.8/src/dali/dali_main.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.021144 dali-rp2-0.6.8/src/dali/data/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/data/__init__.py
--rw-r--r--   0 marcoz     (501) staff       (20)    18654 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/data/template.ods
--rw-r--r--   0 marcoz     (501) staff       (20)     2221 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/historical_bar.py
--rw-r--r--   0 marcoz     (501) staff       (20)     6570 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/in_transaction.py
--rw-r--r--   0 marcoz     (501) staff       (20)     5428 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/intra_transaction.py
--rw-r--r--   0 marcoz     (501) staff       (20)      674 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/logger.py
--rw-r--r--   0 marcoz     (501) staff       (20)    10623 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/ods_generator.py
--rw-r--r--   0 marcoz     (501) staff       (20)     6323 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/out_transaction.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.021414 dali-rp2-0.6.8/src/dali/plugin/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/__init__.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.021884 dali-rp2-0.6.8/src/dali/plugin/country/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/country/__init__.py
--rw-r--r--   0 marcoz     (501) staff       (20)      728 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/country/jp.py
--rw-r--r--   0 marcoz     (501) staff       (20)      722 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/country/us.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.022048 dali-rp2-0.6.8/src/dali/plugin/input/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/input/__init__.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.024173 dali-rp2-0.6.8/src/dali/plugin/input/csv/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/__init__.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     7468 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/binance_com_supplemental.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     6750 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/bitbank_supplemental.py
--rw-r--r--   0 marcoz     (501) staff       (20)    13269 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/blockfi.py
--rw-r--r--   0 marcoz     (501) staff       (20)     3660 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/coincheck_supplemental.py
--rw-r--r--   0 marcoz     (501) staff       (20)     5980 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/ledger.py
--rw-r--r--   0 marcoz     (501) staff       (20)    10885 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/manual.py
--rw-r--r--   0 marcoz     (501) staff       (20)     7544 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/nexo.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     8410 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/pionex.py
--rw-r--r--   0 marcoz     (501) staff       (20)     4988 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor.py
--rw-r--r--   0 marcoz     (501) staff       (20)     4636 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor_old.py
--rw-r--r--   0 marcoz     (501) staff       (20)     5016 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor_v2.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.024514 dali-rp2-0.6.8/src/dali/plugin/input/ods/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-15 01:07:08.000000 dali-rp2-0.6.8/src/dali/plugin/input/ods/__init__.py
--rw-r--r--   0 marcoz     (501) staff       (20)     6845 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/ods/rp2_input.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.025478 dali-rp2-0.6.8/src/dali/plugin/input/rest/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/input/rest/__init__.py
--rw-r--r--   0 marcoz     (501) staff       (20)    50065 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/rest/binance_com.py
--rw-r--r--   0 marcoz     (501) staff       (20)     5042 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/rest/bitbank.py
--rw-r--r--   0 marcoz     (501) staff       (20)    47529 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/rest/coinbase.py
--rw-r--r--   0 marcoz     (501) staff       (20)    24564 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/src/dali/plugin/input/rest/coinbase_pro.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.026261 dali-rp2-0.6.8/src/dali/plugin/pair_converter/
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/__init__.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)    21072 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     1101 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt_binance.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     1185 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt_kraken.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.026531 dali-rp2-0.6.8/src/dali/plugin/pair_converter/csv/
--rwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/csv/__init__.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)    15590 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/csv/kraken.py
--rw-r--r--   0 marcoz     (501) staff       (20)     2880 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/plugin/pair_converter/historic_crypto.py
--rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/src/dali/py.typed
--rw-r--r--   0 marcoz     (501) staff       (20)    30848 2023-04-05 05:17:09.000000 dali-rp2-0.6.8/src/dali/transaction_resolver.py
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.034496 dali-rp2-0.6.8/src/dali_rp2.egg-info/
--rw-r--r--   0 marcoz     (501) staff       (20)    22439 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/PKG-INFO
--rw-r--r--   0 marcoz     (501) staff       (20)     2728 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/SOURCES.txt
--rw-r--r--   0 marcoz     (501) staff       (20)        1 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/dependency_links.txt
--rw-r--r--   0 marcoz     (501) staff       (20)      106 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/entry_points.txt
--rw-r--r--   0 marcoz     (501) staff       (20)      323 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/requires.txt
--rw-r--r--   0 marcoz     (501) staff       (20)        5 2023-04-09 03:08:32.000000 dali-rp2-0.6.8/src/dali_rp2.egg-info/top_level.txt
-drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-04-09 03:08:33.037889 dali-rp2-0.6.8/tests/
--rw-r--r--   0 marcoz     (501) staff       (20)     4772 2023-04-09 03:00:13.000000 dali-rp2-0.6.8/tests/ods_diff.py
--rw-r--r--   0 marcoz     (501) staff       (20)     4479 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/tests/test_cache.py
--rw-r--r--   0 marcoz     (501) staff       (20)     4868 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/tests/test_historical_bar.py
--rw-r--r--   0 marcoz     (501) staff       (20)     4541 2023-04-09 03:00:13.000000 dali-rp2-0.6.8/tests/test_ods_output_diff.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)    47912 2023-04-09 02:54:12.000000 dali-rp2-0.6.8/tests/test_plugin_binance_com.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     6070 2023-03-15 01:34:26.000000 dali-rp2-0.6.8/tests/test_plugin_binance_com_supplemental_csv.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     2696 2023-03-15 01:34:26.000000 dali-rp2-0.6.8/tests/test_plugin_bitbank_supplemental_csv.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)    22733 2023-03-18 05:56:18.000000 dali-rp2-0.6.8/tests/test_plugin_ccxt.py
--rw-r--r--   0 marcoz     (501) staff       (20)     8194 2023-03-15 01:35:08.000000 dali-rp2-0.6.8/tests/test_plugin_coinbase.py
--rw-r--r--   0 marcoz     (501) staff       (20)     5550 2023-03-15 01:34:26.000000 dali-rp2-0.6.8/tests/test_plugin_coinbase_pro.py
--rw-r--r--   0 marcoz     (501) staff       (20)     1782 2023-03-15 01:34:26.000000 dali-rp2-0.6.8/tests/test_plugin_coincheck_supplemental.py
--rw-r--r--   0 marcoz     (501) staff       (20)     3805 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/tests/test_plugin_historic_crypto.py
--rw-r--r--   0 marcoz     (501) staff       (20)     2646 2023-03-18 05:56:18.000000 dali-rp2-0.6.8/tests/test_plugin_kraken_csv_download.py
--rw-r--r--   0 marcoz     (501) staff       (20)     7436 2023-04-09 03:00:13.000000 dali-rp2-0.6.8/tests/test_plugin_ods_rp2_input.py
--rwxr-xr-x   0 marcoz     (501) staff       (20)     6300 2023-03-15 01:34:26.000000 dali-rp2-0.6.8/tests/test_plugin_pionex.py
--rw-r--r--   0 marcoz     (501) staff       (20)     3463 2023-03-12 00:51:26.000000 dali-rp2-0.6.8/tests/test_transaction_resolver.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.152169 dali-rp2-0.6.9/
+-rw-r--r--   0 marcoz     (501) staff       (20)    10941 2023-05-13 14:08:37.000000 dali-rp2-0.6.9/CHANGELOG.md
+-rw-r--r--   0 marcoz     (501) staff       (20)     3098 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/CONTRIBUTING.md
+-rw-r--r--   0 marcoz     (501) staff       (20)    11357 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/LICENSE
+-rw-r--r--   0 marcoz     (501) staff       (20)      214 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/MANIFEST.in
+-rw-r--r--   0 marcoz     (501) staff       (20)    22997 2023-05-13 14:16:02.152260 dali-rp2-0.6.9/PKG-INFO
+-rw-r--r--   0 marcoz     (501) staff       (20)    25116 2023-05-13 14:09:36.000000 dali-rp2-0.6.9/README.dev.md
+-rw-r--r--   0 marcoz     (501) staff       (20)    10493 2023-05-13 14:09:36.000000 dali-rp2-0.6.9/README.md
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.124248 dali-rp2-0.6.9/docs/
+-rw-r--r--   0 marcoz     (501) staff       (20)    45281 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/docs/configuration_file.md
+-rw-r--r--   0 marcoz     (501) staff       (20)     7936 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/docs/developer_faq.md
+-rw-r--r--   0 marcoz     (501) staff       (20)     9765 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/docs/user_faq.md
+-rw-r--r--   0 marcoz     (501) staff       (20)      276 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/pyproject.toml
+-rw-r--r--   0 marcoz     (501) staff       (20)     2269 2023-05-13 14:16:02.153531 dali-rp2-0.6.9/setup.cfg
+-rw-r--r--   0 marcoz     (501) staff       (20)       92 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/setup.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.120561 dali-rp2-0.6.9/src/
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.127079 dali-rp2-0.6.9/src/dali/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/__init__.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)    32063 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/abstract_ccxt_input_plugin.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     2682 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/abstract_input_plugin.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    12844 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/abstract_pair_converter_plugin.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    10022 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/abstract_transaction.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     1393 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/cache.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     8482 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/ccxt_pagination.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     7310 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/configuration.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     3792 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/configuration_generator.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    18811 2023-05-13 14:09:36.000000 dali-rp2-0.6.9/src/dali/dali_main.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.127393 dali-rp2-0.6.9/src/dali/data/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/data/__init__.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    18654 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/data/template.ods
+-rw-r--r--   0 marcoz     (501) staff       (20)     2221 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/historical_bar.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     6570 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/in_transaction.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5428 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/intra_transaction.py
+-rw-r--r--   0 marcoz     (501) staff       (20)      674 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/logger.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    10892 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/ods_generator.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     6323 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/out_transaction.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.127553 dali-rp2-0.6.9/src/dali/plugin/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/__init__.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.127928 dali-rp2-0.6.9/src/dali/plugin/country/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/country/__init__.py
+-rw-r--r--   0 marcoz     (501) staff       (20)      728 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/country/jp.py
+-rw-r--r--   0 marcoz     (501) staff       (20)      722 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/country/us.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.128064 dali-rp2-0.6.9/src/dali/plugin/input/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/__init__.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.129866 dali-rp2-0.6.9/src/dali/plugin/input/csv/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/__init__.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     7468 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/binance_com_supplemental.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     6750 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/bitbank_supplemental.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    13269 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/blockfi.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     3660 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/coincheck_supplemental.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5980 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/ledger.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    10885 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/manual.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     7544 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/nexo.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     8410 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/pionex.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     4988 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     4636 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor_old.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5016 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor_v2.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.130164 dali-rp2-0.6.9/src/dali/plugin/input/ods/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/ods/__init__.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     6845 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/ods/rp2_input.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.131337 dali-rp2-0.6.9/src/dali/plugin/input/rest/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/rest/__init__.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    50065 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/rest/binance_com.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5046 2023-05-13 13:48:18.000000 dali-rp2-0.6.9/src/dali/plugin/input/rest/bitbank.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    47529 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/rest/coinbase.py
+-rw-r--r--   0 marcoz     (501) staff       (20)    24564 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/input/rest/coinbase_pro.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.132584 dali-rp2-0.6.9/src/dali/plugin/pair_converter/
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/__init__.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)    21033 2023-05-13 13:48:18.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     1101 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt_binance.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     1153 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt_coinbase_pro.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     1185 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt_kraken.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.132874 dali-rp2-0.6.9/src/dali/plugin/pair_converter/csv/
+-rwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/csv/__init__.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)    15601 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/csv/kraken.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     2880 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/plugin/pair_converter/historic_crypto.py
+-rw-r--r--   0 marcoz     (501) staff       (20)        0 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/py.typed
+-rw-r--r--   0 marcoz     (501) staff       (20)    30848 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/src/dali/transaction_resolver.py
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.143164 dali-rp2-0.6.9/src/dali_rp2.egg-info/
+-rw-r--r--   0 marcoz     (501) staff       (20)    22997 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/PKG-INFO
+-rw-r--r--   0 marcoz     (501) staff       (20)     2818 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/SOURCES.txt
+-rw-r--r--   0 marcoz     (501) staff       (20)        1 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/dependency_links.txt
+-rw-r--r--   0 marcoz     (501) staff       (20)      106 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/entry_points.txt
+-rw-r--r--   0 marcoz     (501) staff       (20)      364 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/requires.txt
+-rw-r--r--   0 marcoz     (501) staff       (20)        5 2023-05-13 14:16:02.000000 dali-rp2-0.6.9/src/dali_rp2.egg-info/top_level.txt
+drwxr-xr-x   0 marcoz     (501) staff       (20)        0 2023-05-13 14:16:02.152058 dali-rp2-0.6.9/tests/
+-rw-r--r--   0 marcoz     (501) staff       (20)     4772 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/ods_diff.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     1624 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_abstract_pair_converter.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     4479 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_cache.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     4868 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_historical_bar.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5005 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_ods_output_diff.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)    47912 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_binance_com.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     6070 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_binance_com_supplemental_csv.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     2696 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_bitbank_supplemental_csv.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)    23668 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_ccxt.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     8194 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_coinbase.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     5550 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_coinbase_pro.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     1782 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_coincheck_supplemental.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     3805 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_historic_crypto.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     2646 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_kraken_csv_download.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     7436 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_ods_rp2_input.py
+-rwxr-xr-x   0 marcoz     (501) staff       (20)     6300 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_plugin_pionex.py
+-rw-r--r--   0 marcoz     (501) staff       (20)     3463 2023-05-11 00:10:51.000000 dali-rp2-0.6.9/tests/test_transaction_resolver.py
```

### Comparing `dali-rp2-0.6.8/CHANGELOG.md` & `dali-rp2-0.6.9/CHANGELOG.md`

 * *Files 3% similar despite different names*

```diff
@@ -10,14 +10,24 @@
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
 # RP2 Change Log
 
+## 0.6.9
+* new Dijkstra-based pair converter implementation (#142)
+* added Coinbase Pro-based CCXT pair converter (#150)
+* fixed a bug in cache setup of CCXT pair converters (#149)
+* fixed a bug in Bitbank fee-only transactions (#155)
+* fixed spreadsheet size, which was set to a large value regardless of how many rows it contained (#147)
+* added XYMUSDT alternative market to CCXT pair converter (#158)
+* various optimizations (#151, #152))
+* various documentation fixes (#144, #148)
+
 ## 0.6.8
 * Coinbase data loader: added a new flavor of transfer transaction that was slightly different from the other ones (#137)
 
 ## 0.6.7
 * Coinbase data loader: fixed bug in advanced trade buy logic was not accounting for fee correctly
 * Coinbase data loader: added support for moving coins into staking pool (#132)
```

### Comparing `dali-rp2-0.6.8/CONTRIBUTING.md` & `dali-rp2-0.6.9/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/LICENSE` & `dali-rp2-0.6.9/LICENSE`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/PKG-INFO` & `dali-rp2-0.6.9/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dali-rp2
-Version: 0.6.8
+Version: 0.6.9
 Summary: Data loader and input generator for RP2 (https://pypi.org/project/rp2/), the privacy-focused, free, non-commercial, open-source, community-driven cryptocurrency tax calculator: DaLI removes the need to manually prepare RP2 input files. Just like RP2, DaLI is also free, open-source and it prioritizes user privacy.
 Home-page: https://github.com/eprbell/dali-rp2
 Author: eprbell
 License: Apache License 2.0
 Project-URL: Source Code, https://github.com/eprbell/dali-rp2
 Project-URL: Developer Documentation, https://github.com/eprbell/dali-rp2/blob/main/README.dev.md
 Project-URL: User Documentation, https://github.com/eprbell/dali-rp2/blob/main/README.md
@@ -35,26 +35,26 @@
 
 <!--- Unless required by applicable law or agreed to in writing, software --->
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
-# DaLI for RP2 v0.6.8
+# DaLI for RP2 v0.6.9
 
 Privacy-focused, free, extensible data loader for RP2 (the crypto tax calculator)
 
 [![Static Analysis / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml)
 [![Documentation Check / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml)
 [![Unix Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml)
 [![Windows Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml)
 [![CodeQL/Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml)
-
+<!-- markdown-link-check-disable -->
 [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=I%20use%20RP2,%20the%20privacy-focused,%20open%20source,%20free,%20non-commercial%20crypto%20tax%20calculator&url=https://github.com/eprbell/rp2/?anything)
-
+<!-- markdown-link-check-enable -->
 ## Table of Contents
 * **[Introduction](#introduction)**
 * **[License](#license)**
 * **[Download](#download)**
 * **[Installation](#installation)**
   * [Ubuntu Linux](#installation-on-ubuntu-linux)
   * [macOS](#installation-on-macos)
@@ -229,14 +229,24 @@
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
 # RP2 Change Log
 
+## 0.6.9
+* new Dijkstra-based pair converter implementation (#142)
+* added Coinbase Pro-based CCXT pair converter (#150)
+* fixed a bug in cache setup of CCXT pair converters (#149)
+* fixed a bug in Bitbank fee-only transactions (#155)
+* fixed spreadsheet size, which was set to a large value regardless of how many rows it contained (#147)
+* added XYMUSDT alternative market to CCXT pair converter (#158)
+* various optimizations (#151, #152))
+* various documentation fixes (#144, #148)
+
 ## 0.6.8
 * Coinbase data loader: added a new flavor of transfer transaction that was slightly different from the other ones (#137)
 
 ## 0.6.7
 * Coinbase data loader: fixed bug in advanced trade buy logic was not accounting for fee correctly
 * Coinbase data loader: added support for moving coins into staking pool (#132)
```

### Comparing `dali-rp2-0.6.8/README.dev.md` & `dali-rp2-0.6.9/README.dev.md`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 
 <!--- Unless required by applicable law or agreed to in writing, software --->
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
-# DaLI for RP2 v0.6.8 Developer Guide
+# DaLI for RP2 v0.6.9 Developer Guide
 [![Static Analysis / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml)
 [![Documentation Check / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml)
 [![Unix Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml)
 [![Windows Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml)
 [![CodeQL/Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml)
 
 ## Table of Contents
@@ -60,42 +60,42 @@
 ```
 sudo apt-get update
 sudo apt-get install python3 python3-pip virtualenv
 ```
 
 Then install DaLI Python package requirements:
 ```
-cd <rp2_directory>
+cd <dali_directory>
 virtualenv -p python3 .venv
 . .venv/bin/activate
 .venv/bin/pip3 install -e '.[dev]'
 ```
 ### Setup on macOS
 First make sure [Homebrew](https://brew.sh) is installed, then open a terminal window and enter the following commands:
 ```
 brew update
 brew install python3 virtualenv
 ```
 
 Then install DaLI Python package requirements:
 ```
-cd <rp2_directory>
+cd <dali_directory>
 virtualenv -p python3 .venv
 . .venv/bin/activate
 .venv/bin/pip3 install -e '.[dev]'
 ```
 ### Setup on Windows 10
 First make sure [Python](https://python.org) 3.7 or greater is installed (in the Python installer window be sure to click on "Add Python to PATH"), then open a PowerShell window and enter the following commands:
 ```
 python -m pip install virtualenv
 ```
 
 Then install DaLI Python package requirements:
 ```
-cd <rp2_directory>
+cd <dali_directory>
 virtualenv -p python .venv
 .venv\Scripts\activate.ps1
 python -m pip install -e ".[dev]"
 ```
 ### Setup on Other Unix-like Systems
 * install python 3.7 or greater
 * install pip3
```

### Comparing `dali-rp2-0.6.8/README.md` & `dali-rp2-0.6.9/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -8,26 +8,26 @@
 
 <!--- Unless required by applicable law or agreed to in writing, software --->
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
-# DaLI for RP2 v0.6.8
+# DaLI for RP2 v0.6.9
 
 Privacy-focused, free, extensible data loader for RP2 (the crypto tax calculator)
 
 [![Static Analysis / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml)
 [![Documentation Check / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml)
 [![Unix Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml)
 [![Windows Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml)
 [![CodeQL/Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml)
-
+<!-- markdown-link-check-disable -->
 [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=I%20use%20RP2,%20the%20privacy-focused,%20open%20source,%20free,%20non-commercial%20crypto%20tax%20calculator&url=https://github.com/eprbell/rp2/?anything)
-
+<!-- markdown-link-check-enable -->
 ## Table of Contents
 * **[Introduction](#introduction)**
 * **[License](#license)**
 * **[Download](#download)**
 * **[Installation](#installation)**
   * [Ubuntu Linux](#installation-on-ubuntu-linux)
   * [macOS](#installation-on-macos)
```

### Comparing `dali-rp2-0.6.8/docs/configuration_file.md` & `dali-rp2-0.6.9/docs/configuration_file.md`

 * *Files 4% similar despite different names*

```diff
@@ -30,14 +30,15 @@
   * [Trezor Old Section (CSV)](#trezor-old-section-csv)
   * [Trezor V2 Section (CSV)](#trezor-v2-section-csv)
   * [Manual Section (CSV)](#manual-section-csv)
   * [Existing RP2 Input (ODS)](#existing-rp2-input-ods)
 * **[Pair Converter Plugin Sections](#pair-converter-plugin-sections)**
   * [CCXT](#ccxt)
   * [Binance Locked CCXT](#binance-locked-ccxt)
+  * [Coinbase Pro Locked CCXT](#coinbase-pro-locked-ccxt)
   * [Kraken Locked CCXT](#kraken-locked-ccxt)
   * [Historic Crypto](#historic-crypto)
 * **[Builtin Sections](#builtin-sections)**
   * [Transaction Hints Section](#transaction-hints-section)
   * [Header Sections](#header-sections)
   * [Historical Market Data Section](#historical-market-data-section)
 
@@ -480,15 +481,15 @@
 
 
 ### Binance Locked CCXT
 This plugin makes use of the CCXT plugin, but locks all routes to Binance.com.
 
 Initialize this plugin section as follows:
 <pre>
-[dali.plugin.pair_converter.ccxt</em>]
+[dali.plugin.pair_converter.ccxt_binance</em>]
 historical_price_type = <em>&lt;historical_price_type&gt;</em>
 fiat_priority = <em>&lt;fiat_priority&gt;</em>
 </pre>
 
 Where:
 * `<historical_price_type>` is one of `open`, `high`, `low`, `close`, `nearest`. When DaLi downloads historical market data, it captures a `bar` of data surrounding the timestamp of the transaction. Each bar has a starting timestamp, an ending timestamp, and OHLC prices. You can choose which price to select for price lookups. The open, high, low, and close prices are self-explanatory. The `nearest` price is either the open price or the close price of the bar depending on whether the transaction time is nearer the bar starting time or the bar ending time.
 * `fiat_priority` is an optional list of strings in JSON format (e.g. `["_1stpriority_", "_2ndpriority_"...]`) that ranks the priority of fiat in the routing system. If no `fiat_priority` is given, the default priority is USD, JPY, KRW, EUR, GBP, AUD, which is based on the volume of the fiat market paired with BTC (ie. BTC/USD has the highest worldwide volume, then BTC/JPY, etc.).
@@ -498,20 +499,42 @@
 Be aware that:
 * Exchange rates for fiat transactions are based on the daily rate and not minute or hourly rates.
 * The router only uses Binance.com and the fiat exchange rates to build the graph to calculate the route.
 * `fiat_priority` determines what fiat the router will attempt to route through first while trying to find a path to your quote asset.
 * Binance.com might not be available in certain territories.
 
 
+### Coinbase Pro Locked CCXT
+This plugin makes use of the CCXT plugin, but locks all routes to Coinbase Pro.
+
+Initialize this plugin section as follows:
+<pre>
+[dali.plugin.pair_converter.ccxt_coinbase_pro</em>]
+historical_price_type = <em>&lt;historical_price_type&gt;</em>
+fiat_priority = <em>&lt;fiat_priority&gt;</em>
+</pre>
+
+Where:
+* `<historical_price_type>` is one of `open`, `high`, `low`, `close`, `nearest`. When DaLi downloads historical market data, it captures a `bar` of data surrounding the timestamp of the transaction. Each bar has a starting timestamp, an ending timestamp, and OHLC prices. You can choose which price to select for price lookups. The open, high, low, and close prices are self-explanatory. The `nearest` price is either the open price or the close price of the bar depending on whether the transaction time is nearer the bar starting time or the bar ending time.
+* `fiat_priority` is an optional list of strings in JSON format (e.g. `["_1stpriority_", "_2ndpriority_"...]`) that ranks the priority of fiat in the routing system. If no `fiat_priority` is given, the default priority is USD, JPY, KRW, EUR, GBP, AUD, which is based on the volume of the fiat market paired with BTC (ie. BTC/USD has the highest worldwide volume, then BTC/JPY, etc.).
+
+The Kraken Locked CCXT plugin still makes use of fiat exchange rate routing. Pricing will resolve to any major fiat currency even if it doesn't have a market (ie. not used to trade with) on Coinbase Pro.
+
+Be aware that:
+* Exchange rates for fiat transactions are based on the daily rate and not minute or hourly rates.
+* The router only uses Coinbase Pro and the fiat exchange rates to build the graph to calculate the route.
+* `fiat_priority` determines what fiat the router will attempt to route through first while trying to find a path to your quote asset.
+
+
 ### Kraken Locked CCXT
 This plugin makes use of the CCXT plugin, but locks all routes to Kraken(US).
 
 Initialize this plugin section as follows:
 <pre>
-[dali.plugin.pair_converter.ccxt</em>]
+[dali.plugin.pair_converter.ccxt_kraken</em>]
 historical_price_type = <em>&lt;historical_price_type&gt;</em>
 fiat_priority = <em>&lt;fiat_priority&gt;</em>
 google_api_key = <em>&lt;google_api_key&gt;</em>
 </pre>
 
 Where:
 * `<historical_price_type>` is one of `open`, `high`, `low`, `close`, `nearest`. When DaLi downloads historical market data, it captures a `bar` of data surrounding the timestamp of the transaction. Each bar has a starting timestamp, an ending timestamp, and OHLC prices. You can choose which price to select for price lookups. The open, high, low, and close prices are self-explanatory. The `nearest` price is either the open price or the close price of the bar depending on whether the transaction time is nearer the bar starting time or the bar ending time.
```

### Comparing `dali-rp2-0.6.8/docs/developer_faq.md` & `dali-rp2-0.6.9/docs/developer_faq.md`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/docs/user_faq.md` & `dali-rp2-0.6.9/docs/user_faq.md`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/setup.cfg` & `dali-rp2-0.6.9/setup.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = dali-rp2
-version = 0.6.8
+version = 0.6.9
 description = Data loader and input generator for RP2 (https://pypi.org/project/rp2/), the privacy-focused, free, non-commercial, open-source, community-driven cryptocurrency tax calculator: DaLI removes the need to manually prepare RP2 input files. Just like RP2, DaLI is also free, open-source and it prioritizes user privacy.
 long_description_content_type = text/markdown
 long_description = file: README.md, CHANGELOG.md
 keywords = accounting, altcoin, bitcoin, BTC, capital gains, cost basis, crypto, cryptocurrency, data loader, DeFi, ETH, ethereum, exchange, finance, form 8949, NFT, privacy, wallet, tax
 license = Apache License 2.0
 author = eprbell
 url = https://github.com/eprbell/dali-rp2
@@ -27,15 +27,16 @@
 	Contact = https://eprbell.github.io/eprbell/about.html
 
 [options]
 package_dir = 
 	= src
 packages = find:
 install_requires = 
-	ccxt==2.5.1
+	backports-datetime-fromisoformat==2.0.0
+	ccxt==3.0.79
 	Historic-Crypto>=0.1.6
 	jsonschema>=3.2.0
 	pandas
 	prezzemolo>=0.0.4
 	pyexcel-ezodf>=0.3.4
 	python-dateutil>=2.8.2
 	pytz>=2021.3
```

### Comparing `dali-rp2-0.6.8/src/dali/abstract_ccxt_input_plugin.py` & `dali-rp2-0.6.9/src/dali/abstract_ccxt_input_plugin.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/abstract_input_plugin.py` & `dali-rp2-0.6.9/src/dali/abstract_input_plugin.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/abstract_pair_converter_plugin.py` & `dali-rp2-0.6.9/src/dali/abstract_pair_converter_plugin.py`

 * *Files 13% similar despite different names*

```diff
@@ -9,18 +9,21 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from datetime import datetime, timedelta
-from json import JSONDecodeError, loads
+from json import JSONDecodeError
 from typing import Any, Dict, List, NamedTuple, Optional, cast
 
 import requests
+from prezzemolo.graph import Graph
+from prezzemolo.utility import ValueType
+from prezzemolo.vertex import Vertex
 from requests.exceptions import ReadTimeout
 from requests.models import Response
 from requests.sessions import Session
 from rp2.rp2_decimal import ZERO, RP2Decimal
 from rp2.rp2_error import RP2RuntimeError, RP2TypeError
 
 from dali.cache import load_from_cache, save_to_cache
@@ -39,24 +42,63 @@
 
 _DAYS_IN_SECONDS: int = 86400
 _FIAT_EXCHANGE: str = "exchangerate.host"
 
 # First on the list has the most priority
 # This is hard-coded for now based on volume of each of these markets for BTC on Coinmarketcap.com
 # Any change to this priority should be documented in "docs/configuration_file.md"
-_FIAT_PRIORITY: List[str] = ["USD", "JPY", "KRW", "EUR", "GBP", "AUD"]
+_FIAT_PRIORITY: Dict[str, float] = {
+    "USD": 1,
+    "JPY": 2,
+    "KRW": 3,
+    "EUR": 4,
+    "GBP": 5,
+    "AUD": 6,
+}
+
+# Other Weights
+_STANDARD_WEIGHT: float = 1
+_STANDARD_INCREMENT: float = 1
 
 
 class AssetPairAndTimestamp(NamedTuple):
     timestamp: datetime
     from_asset: str
     to_asset: str
     exchange: str
 
 
+class MappedGraph(Graph[ValueType]):
+    def __init__(self, vertexes: Optional[List["Vertex[ValueType]"]] = None) -> None:
+        super().__init__(vertexes)
+        self.__name_to_vertex: Dict[str, Vertex[ValueType]] = {vertex.name: vertex for vertex in vertexes} if vertexes else {}
+
+    def add_vertex(self, vertex: Vertex[ValueType]) -> None:
+        super().add_vertex(vertex)
+        self.__name_to_vertex[vertex.name] = vertex
+
+    def get_vertex(self, name: str) -> Optional[Vertex[ValueType]]:
+        return self.__name_to_vertex.get(name)
+
+    def get_or_set_vertex(self, name: str) -> Vertex[ValueType]:
+        existing_vertex: Optional[Vertex[ValueType]] = self.get_vertex(name)
+        if existing_vertex:
+            return existing_vertex
+
+        new_vertex: Vertex[ValueType] = Vertex[ValueType](name=name)
+        self.add_vertex(new_vertex)
+        return new_vertex
+
+    def add_neighbor(self, vertex_name: str, neighbor_name: str, weight: float = 0.0) -> None:
+        vertex: Vertex[ValueType] = self.get_or_set_vertex(vertex_name)
+        neighbor: Vertex[ValueType] = self.get_or_set_vertex(neighbor_name)
+        if not vertex.has_neighbor(neighbor):
+            vertex.add_neighbor(neighbor, weight)
+
+
 class AbstractPairConverterPlugin:
     __ISSUES_URL: str = "https://github.com/eprbell/dali-rp2/issues"
     __TIMEOUT: int = 30
 
     def __init__(self, historical_price_type: str, fiat_priority: Optional[str] = None) -> None:
         if not isinstance(historical_price_type, str):
             raise RP2TypeError(f"historical_price_type is not a string: {historical_price_type}")
@@ -65,16 +107,22 @@
                 f"historical_price_type must be one of {', '.join(sorted(HISTORICAL_PRICE_KEYWORD_SET))}, instead it was: {historical_price_type}"
             )
         result = cast(Dict[AssetPairAndTimestamp, HistoricalBar], load_from_cache(self.cache_key()))
         self.__cache: Dict[AssetPairAndTimestamp, HistoricalBar] = result if result is not None else {}
         self.__historical_price_type: str = historical_price_type
         self.__session: Session = requests.Session()
         self.__fiat_list: List[str] = []
-        self.__fiat_priority: List[str]
-        self.__fiat_priority = loads(fiat_priority) if fiat_priority is not None else _FIAT_PRIORITY
+        self.__fiat_priority: Dict[str, float]
+        if fiat_priority:
+            weight: float = _STANDARD_WEIGHT
+            for fiat in fiat_priority:
+                self.__fiat_priority[fiat] = weight
+                weight += _STANDARD_INCREMENT
+        else:
+            self.__fiat_priority = _FIAT_PRIORITY
 
     def name(self) -> str:
         raise NotImplementedError("Abstract method: it must be implemented in the plugin class")
 
     def cache_key(self) -> str:
         raise NotImplementedError("Abstract method: it must be implemented in the plugin class")
 
@@ -175,43 +223,36 @@
                     LOGGER.error("Error %d: %s: %s", response.status_code, _EXCHANGE_SYMBOLS_URL, data["message"])
                 response.raise_for_status()
 
         except JSONDecodeError as exc:
             LOGGER.info("Fetching of fiat symbols failed. The server might be down. Please try again later.")
             raise RP2RuntimeError("JSON decode error") from exc
 
-    def _add_fiat_edges_to_graph(self, graph: Dict[str, Dict[str, None]], markets: Dict[str, List[str]]) -> None:
+    def _add_fiat_edges_to_graph(self, graph: MappedGraph[str], markets: Dict[str, List[str]]) -> None:
         if not self.__fiat_list:
             self._build_fiat_list()
 
         for fiat in self.__fiat_list:
             to_fiat_list: Dict[str, None] = dict.fromkeys(self.__fiat_list.copy())
             del to_fiat_list[fiat]
-            if graph.get(fiat):
+            # We don't want to add a fiat vertex here because that would allow a double hop on fiat (eg. USD -> KRW -> JPY)
+            if graph.get_vertex(fiat):
                 for to_be_added_fiat in to_fiat_list:
-                    # add a pair if it doesn't exist
-                    if to_be_added_fiat not in graph[fiat]:
-                        graph[fiat][to_be_added_fiat] = None
-            else:
-                graph[fiat] = to_fiat_list
+                    graph.add_neighbor(
+                        fiat,
+                        to_be_added_fiat,
+                        self.__fiat_priority.get(fiat, _STANDARD_WEIGHT),
+                    )
+
+                LOGGER.debug("Added to assets for %s: %s", fiat, to_fiat_list)
 
             for to_fiat in to_fiat_list:
                 fiat_market = f"{fiat}{to_fiat}"
                 markets[fiat_market] = [_FIAT_EXCHANGE]
 
-            # Add prioritized fiat at the beginning
-            for priority_fiat in reversed(self.__fiat_priority):
-                if priority_fiat in graph[fiat]:
-                    graph[fiat].pop(priority_fiat)
-                    remainder: Dict[str, None] = graph[fiat]
-                    graph[fiat] = {priority_fiat: None}
-                    graph[fiat].update(remainder)
-
-            LOGGER.debug("Added to assets for %s: %s", fiat, graph[fiat])
-
     def _is_fiat_pair(self, from_asset: str, to_asset: str) -> bool:
         return self._is_fiat(from_asset) and self._is_fiat(to_asset)
 
     def _is_fiat(self, asset: str) -> bool:
         if not self.__fiat_list:
             self._build_fiat_list()
```

### Comparing `dali-rp2-0.6.8/src/dali/abstract_transaction.py` & `dali-rp2-0.6.9/src/dali/abstract_transaction.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,23 +9,26 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from datetime import datetime
-from inspect import signature
-from typing import Callable, Dict, List, NamedTuple, Optional, Union
+from inspect import Parameter, signature
+from typing import Callable, Dict, List, Mapping, NamedTuple, Optional, Type, Union
 
+from backports.datetime_fromisoformat import MonkeyPatch
 from dateutil.parser import parse
 from prezzemolo.utility import to_string
 from rp2.rp2_error import RP2RuntimeError
 
 from dali.configuration import Keyword, is_internal_field, is_unknown
 
+MonkeyPatch.patch_fromisoformat()
+
 
 class StringAndDatetime(NamedTuple):
     string: str
     value: datetime
 
 
 class AssetAndUniqueId(NamedTuple):
@@ -36,14 +39,16 @@
 class DirectionTypeAndNotes(NamedTuple):
     direction: str
     transaction_type: str
     notes: str
 
 
 class AbstractTransaction:
+    _parameter_cache: Dict[Type["AbstractTransaction"], Mapping[str, Parameter]] = {}
+
     @classmethod
     def _validate_string_field(cls, name: str, value: str, raw_data: str, disallow_empty: bool, disallow_unknown: bool) -> str:
         if not isinstance(name, str):
             raise RP2RuntimeError(f"Internal error: parameter name is not a string: {name}")
         if not isinstance(value, str):
             raise RP2RuntimeError(f"Internal error: {name} is not a string: {value}\n{raw_data}")
         if disallow_empty and len(value) == 0:
@@ -65,17 +70,20 @@
             raise RP2RuntimeError(f"Internal error parsing {name} as number: {value}\n{raw_data}\n{str(exc)}") from exc
         return value
 
     @classmethod
     def _validate_timestamp_field(cls, name: str, value: str, raw_data: str) -> StringAndDatetime:
         value = cls._validate_string_field(name, value, raw_data, disallow_empty=True, disallow_unknown=True)
         try:
-            result: datetime = parse(value)
-        except RP2RuntimeError as exc:
-            raise RP2RuntimeError(f"Internal error parsing {name} as datetime: {value}\n{raw_data}\n{str(exc)}") from exc
+            result: datetime = datetime.fromisoformat(value)
+        except ValueError:
+            try:
+                result = parse(value)
+            except RP2RuntimeError as exc:
+                raise RP2RuntimeError(f"Internal error parsing {name} as datetime: {value}\n{raw_data}\n{str(exc)}") from exc
         if result.tzinfo is None:
             raise RP2RuntimeError(f"Internal error: {name} has no timezone info: {value}\n{raw_data}")
         if result.microsecond == 0:
             return StringAndDatetime(result.strftime("%Y-%m-%d %H:%M:%S%z"), result)
         return StringAndDatetime(result.strftime("%Y-%m-%d %H:%M:%S.%f%z"), result)
 
     @classmethod
@@ -161,15 +169,18 @@
 
     def __hash__(self) -> int:
         return hash((self.unique_id, self.plugin, self.asset))
 
     # Build a dictionary of constructor initialization parameters. Return true if any of them have UNKNOWN value
     def _setup_constructor_parameter_dictionary(self, parameter_dictionary: Dict[str, Union[str, bool, Optional[str], Optional[bool]]]) -> bool:
         result: bool = False
-        for parameter in signature(self.__class__).parameters:
+        if self.__class__ not in self._parameter_cache:
+            self._parameter_cache[self.__class__] = signature(self.__class__).parameters
+
+        for parameter in self._parameter_cache[self.__class__]:
             value: str = getattr(self, parameter)
             parameter_dictionary[parameter] = value
             if is_internal_field(parameter) or parameter == Keyword.UNIQUE_ID.value:
                 continue
             if is_unknown(value):
                 result = True
         return result
```

### Comparing `dali-rp2-0.6.8/src/dali/cache.py` & `dali-rp2-0.6.9/src/dali/cache.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/ccxt_pagination.py` & `dali-rp2-0.6.9/src/dali/ccxt_pagination.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/configuration.py` & `dali-rp2-0.6.9/src/dali/configuration.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/configuration_generator.py` & `dali-rp2-0.6.9/src/dali/configuration_generator.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/dali_main.py` & `dali-rp2-0.6.9/src/dali/dali_main.py`

 * *Files 8% similar despite different names*

```diff
@@ -49,15 +49,15 @@
     PairConverterPlugin as CcxtPairConverterPlugin,
 )
 from dali.plugin.pair_converter.historic_crypto import (
     PairConverterPlugin as HistoricCryptoPairConverterPlugin,
 )
 from dali.transaction_resolver import resolve_transactions
 
-_VERSION: str = "0.6.8"
+_VERSION: str = "0.6.9"
 
 
 class _InputPluginHelperArgs(NamedTuple):
     input_plugin: AbstractInputPlugin
     package_name: str
     country: AbstractCountry
     use_cache: bool
@@ -153,14 +153,27 @@
             sys.exit(1)
 
         if not pair_converter_list:
             pair_converter_list.append(HistoricCryptoPairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value))
             pair_converter_list.append(CcxtPairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value))
             LOGGER.info("No pair converter plugins found in configuration file: using default pair converters.")
 
+        pair_converters_by_cache_key: Dict[str, AbstractPairConverterPlugin] = {}
+        for pair_converter in pair_converter_list:
+            cache_key = pair_converter.cache_key()
+            if cache_key in pair_converters_by_cache_key:
+                LOGGER.error(
+                    "Internal error: the following pair converter plugins both attempt to store at %s: %s, %s",
+                    cache_key,
+                    pair_converter.name(),
+                    pair_converters_by_cache_key[cache_key].name(),
+                )
+                sys.exit(1)
+            pair_converters_by_cache_key[cache_key] = pair_converter
+
         dali_configuration[Keyword.HISTORICAL_PAIR_CONVERTERS.value] = pair_converter_list
 
         with ThreadPool(args.thread_count) as pool:
             result_list = pool.map(_input_plugin_helper, input_plugin_args_list)
 
         transactions: List[AbstractTransaction] = [transaction for result in result_list for transaction in result]
```

### Comparing `dali-rp2-0.6.8/src/dali/data/template.ods` & `dali-rp2-0.6.9/src/dali/data/template.ods`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/historical_bar.py` & `dali-rp2-0.6.9/src/dali/historical_bar.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/in_transaction.py` & `dali-rp2-0.6.9/src/dali/in_transaction.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/intra_transaction.py` & `dali-rp2-0.6.9/src/dali/intra_transaction.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/logger.py` & `dali-rp2-0.6.9/src/dali/logger.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/ods_generator.py` & `dali-rp2-0.6.9/src/dali/ods_generator.py`

 * *Files 2% similar despite different names*

```diff
@@ -155,26 +155,32 @@
 
     transactions.sort(key=_transaction_sort_key)
 
     current_asset: Optional[str] = None
     current_sheet: Optional[Any] = None
     current_table: Optional[str] = None
     row_index: int = 0
+
+    transaction_count_by_asset: Dict[str, int] = {}
+    for transaction in transactions:
+        working_asset = transaction.asset
+        transaction_count_by_asset[working_asset] = transaction_count_by_asset.setdefault(working_asset, 0) + 1
+
     for transaction in transactions:
         if not isinstance(transaction, AbstractTransaction):
             raise RP2RuntimeError(f"Internal error: Parameter 'transaction' is not a subclass of AbstractTransaction. {transaction}")
         if transaction.asset == global_configuration[Keyword.NATIVE_FIAT.value]:
             continue
         table_type: str = _TRANSACTION_CLASS_TO_TABLE[transaction.__class__]
         if transaction.asset != current_asset:
             if current_sheet:
                 _fill_cell(current_sheet, row_index, 0, _TABLE_END, visual_style="bold")
             current_asset = transaction.asset
             current_sheet = ezodf.Table(current_asset)
-            current_sheet.reset(size=(len(transactions) + _MIN_ROWS, _MAX_COLUMNS))
+            current_sheet.reset(size=(transaction_count_by_asset[current_asset] + _MIN_ROWS, _MAX_COLUMNS))
             output_file.sheets += current_sheet
             row_index = 0
             current_table = None
         if table_type != current_table:
             if current_table is not None:
                 _fill_cell(current_sheet, row_index, 0, _TABLE_END, visual_style="bold")
                 row_index += 2
```

### Comparing `dali-rp2-0.6.8/src/dali/out_transaction.py` & `dali-rp2-0.6.9/src/dali/out_transaction.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/country/jp.py` & `dali-rp2-0.6.9/src/dali/plugin/country/jp.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/country/us.py` & `dali-rp2-0.6.9/src/dali/plugin/country/us.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/binance_com_supplemental.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/binance_com_supplemental.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/bitbank_supplemental.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/bitbank_supplemental.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/blockfi.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/blockfi.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/coincheck_supplemental.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/coincheck_supplemental.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/ledger.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/ledger.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/manual.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/manual.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/nexo.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/nexo.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/pionex.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/pionex.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor_old.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor_old.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/csv/trezor_v2.py` & `dali-rp2-0.6.9/src/dali/plugin/input/csv/trezor_v2.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/ods/rp2_input.py` & `dali-rp2-0.6.9/src/dali/plugin/input/ods/rp2_input.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/rest/binance_com.py` & `dali-rp2-0.6.9/src/dali/plugin/input/rest/binance_com.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/rest/bitbank.py` & `dali-rp2-0.6.9/src/dali/plugin/input/rest/bitbank.py`

 * *Files 1% similar despite different names*

```diff
@@ -117,15 +117,15 @@
 
     # Override the handling of trades since Bitbank has negative maker fees
     def _process_buy_and_sell(self, transaction: Any, notes: Optional[str] = None) -> ProcessOperationResult:
         fee_income: Optional[InTransaction] = None
         if RP2Decimal(str(transaction[_FEE][_COST])) < ZERO:
             fee_income = InTransaction(
                 plugin=self.plugin_name(),
-                unique_id=f"{transaction[_ID]}",
+                unique_id=f"{transaction[_ID]}/fee",
                 raw_data=json.dumps(transaction),
                 timestamp=self._rp2_timestamp_from_ms_epoch(transaction[_TIMESTAMP]),
                 asset=transaction[_FEE][_CURRENCY],
                 exchange=self.exchange_name(),
                 holder=self.account_holder,
                 transaction_type=Keyword.INCOME.value,
                 spot_price=Keyword.UNKNOWN.value,
```

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/rest/coinbase.py` & `dali-rp2-0.6.9/src/dali/plugin/input/rest/coinbase.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/input/rest/coinbase_pro.py` & `dali-rp2-0.6.9/src/dali/plugin/input/rest/coinbase_pro.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt.py` & `dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt.py`

 * *Files 5% similar despite different names*

```diff
@@ -12,35 +12,38 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import logging
 from datetime import datetime, timedelta
 from inspect import Signature, signature
 from time import sleep, time
-from typing import Any, Dict, List, NamedTuple, Optional, Union
+from typing import Any, Dict, Iterator, List, NamedTuple, Optional, Union
 
 from ccxt import (
     DDoSProtection,
     Exchange,
     ExchangeError,
     ExchangeNotAvailable,
     NetworkError,
     RequestTimeout,
     binance,
+    coinbasepro,
     gateio,
     huobi,
     kraken,
 )
+from prezzemolo.vertex import Vertex
 from rp2.logger import create_logger
 from rp2.rp2_decimal import RP2Decimal
 from rp2.rp2_error import RP2RuntimeError
 
 from dali.abstract_pair_converter_plugin import (
     AbstractPairConverterPlugin,
     AssetPairAndTimestamp,
+    MappedGraph,
 )
 from dali.configuration import Keyword
 from dali.historical_bar import HistoricalBar
 from dali.plugin.pair_converter.csv.kraken import Kraken as KrakenCsvPricing
 
 # Native format keywords
 _ID: str = "id"
@@ -51,39 +54,54 @@
 
 # Time in ms
 _MINUTE: str = "1m"
 _FIVE_MINUTE: str = "5m"
 _FIFTEEN_MINUTE: str = "15m"
 _ONE_HOUR: str = "1h"
 _FOUR_HOUR: str = "4h"
+_SIX_HOUR: str = "6h"
 _ONE_DAY: str = "1d"
 _TIME_GRANULARITY: List[str] = [_MINUTE, _FIVE_MINUTE, _FIFTEEN_MINUTE, _ONE_HOUR, _FOUR_HOUR, _ONE_DAY]
-_TIME_GRANULARITY_IN_SECONDS: List[int] = [60, 300, 900, 3600, 14400, 86400]
+_TIME_GRANULARITY_STRING_TO_SECONDS: Dict[str, int] = {
+    _MINUTE: 60,
+    _FIVE_MINUTE: 300,
+    _FIFTEEN_MINUTE: 900,
+    _ONE_HOUR: 3600,
+    _FOUR_HOUR: 14400,
+    _SIX_HOUR: 21600,
+    _ONE_DAY: 86400,
+}
 
 # Currently supported exchanges
 _BINANCE: str = "Binance.com"
+_COINBASE_PRO: str = "Coinbase Pro"
 _GATE: str = "Gate"
 _HUOBI: str = "Huobi"
 _KRAKEN: str = "Kraken"
 _FIAT_EXCHANGE: str = "Exchangerate.host"
 _DEFAULT_EXCHANGE: str = _KRAKEN
-_EXCHANGE_DICT: Dict[str, Any] = {_BINANCE: binance, _GATE: gateio, _HUOBI: huobi, _KRAKEN: kraken}
+_EXCHANGE_DICT: Dict[str, Any] = {_BINANCE: binance, _COINBASE_PRO: coinbasepro, _GATE: gateio, _HUOBI: huobi, _KRAKEN: kraken}
+_TIME_GRANULARITY_DICT: Dict[str, List[str]] = {
+    _COINBASE_PRO: [_MINUTE, _FIVE_MINUTE, _FIFTEEN_MINUTE, _ONE_HOUR, _SIX_HOUR, _ONE_DAY],
+}
+
 
 # Delay in fractional seconds before making a request to avoid too many request errors
 # Kraken states it has a limit of 1 call per second, but this doesn't seem to be correct.
 # It appears Kraken public API is limited to around 12 calls per minute.
 # There also appears to be a limit of how many calls per 2 hour time period.
 # Being authenticated lowers this limit.
 _REQUEST_DELAYDICT: Dict[str, float] = {_KRAKEN: 5.1}
 
 # CSV Pricing classes
 _CSV_PRICING_DICT: Dict[str, Any] = {_KRAKEN: KrakenCsvPricing}
 
 # Alternative Markets and exchanges for stablecoins or untradeable assets
 _ALT_MARKET_EXCHANGES_DICT: Dict[str, str] = {
+    "XYMUSDT": _GATE,
     "ATDUSDT": _GATE,
     "BETHETH": _BINANCE,
     "BNBUSDT": _BINANCE,
     "BSVUSDT": _GATE,
     "BOBAUSD": _GATE,
     "BUSDUSDT": _BINANCE,
     "EDGUSDT": _GATE,
@@ -91,14 +109,15 @@
     "NEXOUSDT": _BINANCE,
     "SGBUSD": _KRAKEN,
     "SOLOUSDT": _HUOBI,
     "USDTUSD": _KRAKEN,
 }
 
 _ALT_MARKET_BY_BASE_DICT: Dict[str, str] = {
+    "XYM": "USDT",
     "ATD": "USDT",
     "BETH": "ETH",
     "BNB": "USDT",
     "BOBA": "USD",
     "BSV": "USDT",
     "BUSD": "USDT",
     "EDG": "USDT",
@@ -107,37 +126,42 @@
     "SGB": "USD",
     "SOLO": "USDT",
     "USDT": "USD",
 }
 
 # Priority for quote asset. If asset is not listed it will be filtered out.
 # In principle this should be fiat in order of trade volume and then stable coins in order of trade volume
-_QUOTE_PRIORITY: Dict[str, None] = {
-    "USD": None,
-    "JPY": None,
-    "KRW": None,
-    "EUR": None,
-    "GBP": None,
-    "AUD": None,
-    "USDT": None,
-    "USDC": None,
-    "BUSD": None,
-    "TUSD": None,
-    "OUSD": None,
+_QUOTE_PRIORITY: Dict[str, float] = {
+    "USD": 1,
+    "JPY": 2,
+    "KRW": 3,
+    "EUR": 4,
+    "GBP": 5,
+    "AUD": 6,
+    "USDT": 7,
+    "USDC": 8,
+    "BUSD": 9,
+    "TUSD": 10,
+    "OUSD": 11,
 }
 
 # Time constants
 _MS_IN_SECOND: int = 1000
 
 # Cache
 _CACHE_INTERVAL: int = 200
 
 # CSV Reader
 _GOOGLE_API_KEY: str = "google_api_key"
 
+# Djikstra weights
+# Priority should go to quote assets listed above, then other assets, and finally alternatives
+_STANDARD_WEIGHT: float = 50
+_ALTERNATIVE_MARKET_WEIGHT: float = 51
+
 
 class AssetPairAndHistoricalPrice(NamedTuple):
     from_asset: str
     to_asset: str
     exchange: str
     historical_data: Optional[HistoricalBar] = None
 
@@ -147,93 +171,53 @@
         self,
         historical_price_type: str,
         default_exchange: Optional[str] = None,
         fiat_priority: Optional[str] = None,
         google_api_key: Optional[str] = None,
         exchange_locked: Optional[bool] = None,
     ) -> None:
+        exchange_cache_modifier = default_exchange.replace(" ", "_") if default_exchange and exchange_locked else ""
+        fiat_priority_cache_modifier = fiat_priority if fiat_priority else ""
+        self.__cache_modifier = "_".join(x for x in [exchange_cache_modifier, fiat_priority_cache_modifier] if x)
+
         super().__init__(historical_price_type=historical_price_type, fiat_priority=fiat_priority)
         self.__logger: logging.Logger = create_logger(f"{self.name()}/{historical_price_type}")
 
         self.__exchanges: Dict[str, Exchange] = {}
         self.__exchange_markets: Dict[str, Dict[str, List[str]]] = {}
         self.__google_api_key: Optional[str] = google_api_key
         self.__exchange_locked: bool = exchange_locked if exchange_locked is not None else False
-
-        # TO BE IMPLEMENTED - graph and vertex classes to make this more understandable
-        # https://github.com/eprbell/dali-rp2/pull/53#discussion_r924056308
         self.__default_exchange: str = _DEFAULT_EXCHANGE if default_exchange is None else default_exchange
         self.__exchange_csv_reader: Dict[str, Any] = {}
-        self.__exchange_graphs: Dict[str, Dict[str, Dict[str, None]]] = {}
+        # key: name of exchange, value: graph that prioritizes that exchange
+        self.__exchange_graphs: Dict[str, MappedGraph[str]] = {}
         self.__exchange_last_request: Dict[str, float] = {}
         if exchange_locked:
             self.__logger.debug("Routing locked to single exchange %s.", self.__default_exchange)
         else:
             self.__logger.debug("Default exchange assigned as %s. _DEFAULT_EXCHANGE is %s", self.__default_exchange, _DEFAULT_EXCHANGE)
 
     def name(self) -> str:
         return "CCXT-converter"
 
     def cache_key(self) -> str:
-        return self.name()
+        return self.name() + "_" + self.__cache_modifier if self.__cache_modifier else self.name()
 
     @property
     def exchanges(self) -> Dict[str, Exchange]:
         return self.__exchanges
 
     @property
     def exchange_markets(self) -> Dict[str, Dict[str, List[str]]]:
         return self.__exchange_markets
 
     @property
-    def exchange_graphs(self) -> Dict[str, Dict[str, Dict[str, None]]]:
+    def exchange_graphs(self) -> Dict[str, MappedGraph[str]]:
         return self.__exchange_graphs
 
-    def _bfs_cyclic(self, graph: Dict[str, Dict[str, None]], start: str, end: str) -> Optional[List[str]]:
-        # maintain a queue of paths
-        # TO BE IMPLEMENTED - using on vertex queue and one dict?
-        # https://github.com/eprbell/dali-rp2/pull/53#discussion_r924058754
-        queue: List[List[str]] = []
-        visited: Dict[str, None] = {}
-
-        # push the first path into the queue
-        queue.append([start])
-
-        while queue:
-            # get the first path from the queue
-            path: List[str] = queue.pop(0)
-
-            # get the last node from the path
-            node: str = path[-1]
-
-            # path found
-            if node == end:
-                return path
-
-            # enumerate all adjacent nodes, construct a new path and push it into the queue
-            for adjacent in graph.get(node, {}):
-                # prevents an infinite loop.
-                if adjacent not in visited:
-                    new_path: List[str] = list(path)
-                    new_path.append(adjacent)
-                    queue.append(new_path)
-                    visited[adjacent] = None
-
-        # No path found
-        return None
-
-    def _prioritize_quote_assets(self, current_graph: Dict[str, List[str]]) -> None:
-        for base_asset in current_graph.keys():
-            for priority_quote in reversed(_QUOTE_PRIORITY):
-                if priority_quote in current_graph[base_asset]:
-                    current_graph[base_asset].pop(current_graph[base_asset].index(priority_quote))
-                    remainder: List[str] = current_graph[base_asset]
-                    current_graph[base_asset] = [priority_quote]
-                    current_graph[base_asset].extend(remainder)
-
     def get_historic_bar_from_native_source(self, timestamp: datetime, from_asset: str, to_asset: str, exchange: str) -> Optional[HistoricalBar]:
         self.__logger.debug("Converting %s to %s", from_asset, to_asset)
 
         # If both assets are fiat, skip further processing
         if self._is_fiat_pair(from_asset, to_asset):
             return self._get_fiat_exchange_rate(timestamp, from_asset, to_asset)
 
@@ -252,40 +236,46 @@
                 self._add_exchange_to_memcache(exchange)
             else:
                 self.__logger.error("WARNING: Unrecognized Exchange: %s. Please open an issue at %s", exchange, self.issues_url)
                 return None
 
         current_markets = self.__exchange_markets[exchange]
         current_graph = self.__exchange_graphs[exchange]
-
+        from_asset_vertex: Optional[Vertex[str]] = current_graph.get_vertex(from_asset)
+        to_asset_vertex: Optional[Vertex[str]] = current_graph.get_vertex(to_asset)
         market_symbol = from_asset + to_asset
         result: Optional[HistoricalBar] = None
+        pricing_path: Optional[Iterator[Vertex[str]]] = None
 
         # TO BE IMPLEMENTED - bypass routing if conversion can be done with one market on the exchange
         if market_symbol in current_markets and (exchange in current_markets[market_symbol]):
             self.__logger.debug("Found market - %s on single exchange, skipping routing.", market_symbol)
             result = self.find_historical_bar(from_asset, to_asset, timestamp, exchange)
             return result
         # else:
         # Graph building goes here.
 
-        pricing_path: Optional[List[str]] = self._bfs_cyclic(current_graph, from_asset, to_asset)
+        if not from_asset_vertex or not to_asset_vertex:
+            raise RP2RuntimeError(f"The asset {from_asset} or {to_asset} is missing from graph")
+        pricing_path = current_graph.dijkstra(from_asset_vertex, to_asset_vertex, False)
+
         if pricing_path is None:
             self.__logger.debug("No path found for %s to %s. Please open an issue at %s.", from_asset, to_asset, self.issues_url)
             return None
 
-        self.__logger.debug("Found path - %s", pricing_path)
+        pricing_path_list: List[str] = [v.name for v in pricing_path]
+        self.__logger.debug("Found path - %s", pricing_path_list)
 
         conversion_route: List[AssetPairAndHistoricalPrice] = []
         last_node: Optional[str] = None
         hop_bar: Optional[HistoricalBar] = None
 
         # Build conversion stack, we will iterate over this to find the price for each conversion
         # Then multiply them together to get our final price.
-        for node in pricing_path:
+        for node in pricing_path_list:
             if last_node:
                 conversion_route.append(
                     AssetPairAndHistoricalPrice(
                         from_asset=last_node,
                         to_asset=node,
                         exchange=current_markets[(last_node + node)][0],
                         historical_data=None,
@@ -308,15 +298,14 @@
                     """No pricing data found for hop. This could be caused by airdropped
                     coins that do not have a market yet. Market - %s%s, Timestamp - %s, Exchange - %s""",
                     hop_data.from_asset,
                     hop_data.to_asset,
                     timestamp,
                     hop_data.exchange,
                 )
-
             if result is not None:
                 # TO BE IMPLEMENTED - override Historical Bar * to multiply two bars?
                 result = HistoricalBar(
                     duration=max(result.duration, hop_bar.duration),  # type: ignore
                     timestamp=timestamp,
                     open=(result.open * hop_bar.open),  # type: ignore
                     high=(result.high * hop_bar.high),  # type: ignore
@@ -367,16 +356,16 @@
 
             historical_bar = self._get_bar_from_cache(key)
             self.__exchange_csv_reader[exchange] = csv_reader
             if historical_bar is not None:
                 self.__logger.debug("Retrieved bar cache - %s for %s/%s->%s for %s", historical_bar, key.timestamp, key.from_asset, key.to_asset, key.exchange)
                 return historical_bar
 
-        while retry_count < len(_TIME_GRANULARITY):
-            timeframe: str = _TIME_GRANULARITY[retry_count]
+        while retry_count < len(_TIME_GRANULARITY_DICT.get(exchange, _TIME_GRANULARITY)):
+            timeframe: str = _TIME_GRANULARITY_DICT.get(exchange, _TIME_GRANULARITY)[retry_count]
             request_count: int = 0
             historical_data: List[List[Union[int, float]]] = []
 
             # Most exceptions are caused by request limits of the underlying APIs
             while request_count < 9:
                 try:
                     # Excessive calls to the API within a certain window might get an IP temporarily banned
@@ -414,15 +403,15 @@
 
                     self.__logger.debug("Server not available. Making attempt #%s of 10 after a ten second delay. Exception - %s", request_count, exc_na)
                     sleep(10)
 
             # If there is no candle the list will be empty
             if historical_data:
                 result = HistoricalBar(
-                    duration=timedelta(seconds=_TIME_GRANULARITY_IN_SECONDS[retry_count]),
+                    duration=timedelta(seconds=_TIME_GRANULARITY_STRING_TO_SECONDS[timeframe]),
                     timestamp=timestamp,
                     open=RP2Decimal(str(historical_data[0][1])),
                     high=RP2Decimal(str(historical_data[0][2])),
                     low=RP2Decimal(str(historical_data[0][3])),
                     close=RP2Decimal(str(historical_data[0][4])),
                     volume=RP2Decimal(str(historical_data[0][5])),
                 )
@@ -432,56 +421,54 @@
 
         # Save the individual pair to cache
         if result is not None:
             self._add_bar_to_cache(key, result)
 
         return result
 
-    def _add_alternative_markets(self, current_graph: Dict[str, Dict[str, None]], current_markets: Dict[str, List[str]]) -> None:
+    def _add_alternative_markets(self, graph: MappedGraph[str], current_markets: Dict[str, List[str]]) -> None:
         for base_asset, quote_asset in _ALT_MARKET_BY_BASE_DICT.items():
             alt_market = base_asset + quote_asset
             alt_exchange_name = _ALT_MARKET_EXCHANGES_DICT[alt_market]
 
-            # TO BE IMPLEMENTED - Add alt market to the end of list if another exchange exists already
+            # TO BE IMPLEMENTED - Add markets to a priority queue inside MappedGraph to prioritize higher volume exchanges
             current_markets[alt_market] = [alt_exchange_name]
 
             # Cache the exchange so that we can pull prices from it later
             if alt_exchange_name not in self.__exchanges:
                 self.__logger.debug("Added Alternative Exchange: %s", alt_exchange_name)
                 alt_exchange: Exchange = _EXCHANGE_DICT[alt_exchange_name]()
                 self.__exchanges[alt_exchange_name] = alt_exchange
 
-            if current_graph.get(base_asset) and (quote_asset not in current_graph[base_asset]):
-                current_graph[base_asset][quote_asset] = None
-            else:
-                current_graph[base_asset] = {quote_asset: None}
+            # If the asset name doesn't exist, the MappedGraph will create a vertex with that name and add it to the graph
+            # If it does exist it will look it up in the dictionary by name and add the neighbor to that vertex.
+            graph.add_neighbor(base_asset, quote_asset, _ALTERNATIVE_MARKET_WEIGHT)
 
     def _add_exchange_to_memcache(self, exchange: str) -> None:
         if exchange not in self.__exchanges:
             # initializes the cctx exchange instance which is used to get the historical data
             # https://docs.ccxt.com/en/latest/manual.html#notes-on-rate-limiter
             current_exchange: Exchange = _EXCHANGE_DICT[exchange]({"enableRateLimit": True})
         else:
             current_exchange = self.__exchanges[exchange]
 
         # key: market, value: exchanges where the market is available in order of priority
         current_markets: Dict[str, List[str]] = {}
-        current_graph: Dict[str, Dict[str, None]] = {}
+        current_graph: MappedGraph[str] = MappedGraph[str]()
 
         for market in filter(lambda x: x[_TYPE] == "spot" and x[_QUOTE] in _QUOTE_PRIORITY, current_exchange.fetch_markets()):
             self.__logger.debug("Market: %s", market)
 
             current_markets[f"{market[_BASE]}{market[_QUOTE]}"] = [exchange]
 
             # TO BE IMPLEMENTED - lazy build graph only if needed
 
-            # Add the quote asset to the graph if it isn't there already.
-            current_graph.setdefault(market[_BASE], {})[market[_QUOTE]] = None
-
-        self._prioritize_quote_assets(current_markets)
+            # If the asset name doesn't exist, the MappedGraph will create a vertex with that name and add it to the graph
+            # If it does exist it will look it up in the dictionary by name and add the neighbor to that vertex.
+            current_graph.add_neighbor(market[_BASE], market[_QUOTE], _QUOTE_PRIORITY.get(market[_QUOTE], _STANDARD_WEIGHT))
 
         # Add alternative markets if they don't exist
         if not self.__exchange_locked:
             self._add_alternative_markets(current_graph, current_markets)
 
         self._add_fiat_edges_to_graph(current_graph, current_markets)
         self.__logger.debug("Added graph for %s : %s", current_exchange, current_graph)
```

### Comparing `dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt_binance.py` & `dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt_binance.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/pair_converter/ccxt_kraken.py` & `dali-rp2-0.6.9/src/dali/plugin/pair_converter/ccxt_kraken.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/plugin/pair_converter/csv/kraken.py` & `dali-rp2-0.6.9/src/dali/plugin/pair_converter/csv/kraken.py`

 * *Files 1% similar despite different names*

```diff
@@ -348,15 +348,15 @@
                         self.__logger.error(
                             "Google API key is invalid. Please check that you have entered the key correctly and try again."
                             "If the problem persists, you can leave the field blank to use the REST API.\n%s",
                             error[_MESSAGE],
                         )
                         raise RP2RuntimeError("Google Drive key invalid")
             if not data.get(_FILES):
-                self.__logger.debug("The file '%s' was not found on the Kraken Google Drive.")
+                self.__logger.debug("The file '%s' was not found on the Kraken Google Drive.", file_name)
                 return None
 
             self.__logger.debug("Retrieved %s from %s", data, response.url)
 
             # Downloading the zipfile that contains the 6 files one for each of the standard durations of candles:
             # 1m, 5m, 15m, 1h, 12h, 24h.
             params = {_ALT: _MEDIA, _API_KEY: self.__google_api_key, _CONFIRM: 1}  # _CONFIRM: 1 bypasses large file warning
```

### Comparing `dali-rp2-0.6.8/src/dali/plugin/pair_converter/historic_crypto.py` & `dali-rp2-0.6.9/src/dali/plugin/pair_converter/historic_crypto.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali/transaction_resolver.py` & `dali-rp2-0.6.9/src/dali/transaction_resolver.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/src/dali_rp2.egg-info/PKG-INFO` & `dali-rp2-0.6.9/src/dali_rp2.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dali-rp2
-Version: 0.6.8
+Version: 0.6.9
 Summary: Data loader and input generator for RP2 (https://pypi.org/project/rp2/), the privacy-focused, free, non-commercial, open-source, community-driven cryptocurrency tax calculator: DaLI removes the need to manually prepare RP2 input files. Just like RP2, DaLI is also free, open-source and it prioritizes user privacy.
 Home-page: https://github.com/eprbell/dali-rp2
 Author: eprbell
 License: Apache License 2.0
 Project-URL: Source Code, https://github.com/eprbell/dali-rp2
 Project-URL: Developer Documentation, https://github.com/eprbell/dali-rp2/blob/main/README.dev.md
 Project-URL: User Documentation, https://github.com/eprbell/dali-rp2/blob/main/README.md
@@ -35,26 +35,26 @@
 
 <!--- Unless required by applicable law or agreed to in writing, software --->
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
-# DaLI for RP2 v0.6.8
+# DaLI for RP2 v0.6.9
 
 Privacy-focused, free, extensible data loader for RP2 (the crypto tax calculator)
 
 [![Static Analysis / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/static_analysis.yml)
 [![Documentation Check / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/documentation_check.yml)
 [![Unix Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/unix_unit_tests.yml)
 [![Windows Unit Tests / Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/windows_unit_tests.yml)
 [![CodeQL/Main Branch](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/eprbell/dali-rp2/actions/workflows/codeql-analysis.yml)
-
+<!-- markdown-link-check-disable -->
 [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=I%20use%20RP2,%20the%20privacy-focused,%20open%20source,%20free,%20non-commercial%20crypto%20tax%20calculator&url=https://github.com/eprbell/rp2/?anything)
-
+<!-- markdown-link-check-enable -->
 ## Table of Contents
 * **[Introduction](#introduction)**
 * **[License](#license)**
 * **[Download](#download)**
 * **[Installation](#installation)**
   * [Ubuntu Linux](#installation-on-ubuntu-linux)
   * [macOS](#installation-on-macos)
@@ -229,14 +229,24 @@
 <!--- distributed under the License is distributed on an "AS IS" BASIS, --->
 <!--- WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. --->
 <!--- See the License for the specific language governing permissions and --->
 <!--- limitations under the License. --->
 
 # RP2 Change Log
 
+## 0.6.9
+* new Dijkstra-based pair converter implementation (#142)
+* added Coinbase Pro-based CCXT pair converter (#150)
+* fixed a bug in cache setup of CCXT pair converters (#149)
+* fixed a bug in Bitbank fee-only transactions (#155)
+* fixed spreadsheet size, which was set to a large value regardless of how many rows it contained (#147)
+* added XYMUSDT alternative market to CCXT pair converter (#158)
+* various optimizations (#151, #152))
+* various documentation fixes (#144, #148)
+
 ## 0.6.8
 * Coinbase data loader: added a new flavor of transfer transaction that was slightly different from the other ones (#137)
 
 ## 0.6.7
 * Coinbase data loader: fixed bug in advanced trade buy logic was not accounting for fee correctly
 * Coinbase data loader: added support for moving coins into staking pool (#132)
```

### Comparing `dali-rp2-0.6.8/src/dali_rp2.egg-info/SOURCES.txt` & `dali-rp2-0.6.9/src/dali_rp2.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -53,25 +53,27 @@
 src/dali/plugin/input/rest/binance_com.py
 src/dali/plugin/input/rest/bitbank.py
 src/dali/plugin/input/rest/coinbase.py
 src/dali/plugin/input/rest/coinbase_pro.py
 src/dali/plugin/pair_converter/__init__.py
 src/dali/plugin/pair_converter/ccxt.py
 src/dali/plugin/pair_converter/ccxt_binance.py
+src/dali/plugin/pair_converter/ccxt_coinbase_pro.py
 src/dali/plugin/pair_converter/ccxt_kraken.py
 src/dali/plugin/pair_converter/historic_crypto.py
 src/dali/plugin/pair_converter/csv/__init__.py
 src/dali/plugin/pair_converter/csv/kraken.py
 src/dali_rp2.egg-info/PKG-INFO
 src/dali_rp2.egg-info/SOURCES.txt
 src/dali_rp2.egg-info/dependency_links.txt
 src/dali_rp2.egg-info/entry_points.txt
 src/dali_rp2.egg-info/requires.txt
 src/dali_rp2.egg-info/top_level.txt
 tests/ods_diff.py
+tests/test_abstract_pair_converter.py
 tests/test_cache.py
 tests/test_historical_bar.py
 tests/test_ods_output_diff.py
 tests/test_plugin_binance_com.py
 tests/test_plugin_binance_com_supplemental_csv.py
 tests/test_plugin_bitbank_supplemental_csv.py
 tests/test_plugin_ccxt.py
```

### Comparing `dali-rp2-0.6.8/tests/ods_diff.py` & `dali-rp2-0.6.9/tests/ods_diff.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_cache.py` & `dali-rp2-0.6.9/tests/test_cache.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_historical_bar.py` & `dali-rp2-0.6.9/tests/test_historical_bar.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_ods_output_diff.py` & `dali-rp2-0.6.9/tests/test_ods_output_diff.py`

 * *Files 11% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 import os
 import shutil
 import unittest
 from pathlib import Path
 from subprocess import run
 from typing import List
 
+import ezodf
 from ods_diff import ods_diff
 
 from dali.cache import CACHE_DIR
 
 ROOT_PATH: Path = Path(os.path.dirname(__file__)).parent.absolute()
 
 CACHE_PATH: Path = ROOT_PATH / CACHE_DIR
@@ -112,10 +113,20 @@
     # def test_lifo_rp2_full_report_ods(self) -> None:
     #     file_name: str = "test_lifo_rp2_full_report.ods"
     #     full_output_file_name: Path = self.output_dir / file_name
     #     full_golden_file_name: Path = GOLDEN_PATH / file_name
     #     diff = ods_diff(full_golden_file_name, full_output_file_name, generate_ascii_representation=True)
     #     self.assertFalse(diff, msg=diff)
 
+    def test_ods_sheet_size(self) -> None:
+        sizes = {"test_crypto_data.ods": {"BTC": 46}}
+        for basename, sheet_sizes in sizes.items():
+            filename = self.output_dir / basename
+            file: ezodf.document.PackagedDocument = ezodf.opendoc(str(filename))
+
+            for sheet in file.sheets:
+                assert sheet.name in sheet_sizes
+                assert file.sheets[sheet.name].nrows() == sheet_sizes[sheet.name]
+
 
 if __name__ == "__main__":
     unittest.main()
```

### Comparing `dali-rp2-0.6.8/tests/test_plugin_binance_com.py` & `dali-rp2-0.6.9/tests/test_plugin_binance_com.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_binance_com_supplemental_csv.py` & `dali-rp2-0.6.9/tests/test_plugin_binance_com_supplemental_csv.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_bitbank_supplemental_csv.py` & `dali-rp2-0.6.9/tests/test_plugin_bitbank_supplemental_csv.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_ccxt.py` & `dali-rp2-0.6.9/tests/test_plugin_ccxt.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,36 +12,31 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import os
 from datetime import datetime, timedelta, timezone
 from typing import Any, Dict, List, Union
 
+import pytest
 from ccxt import binance, kraken
+from prezzemolo.vertex import Vertex
 from rp2.rp2_decimal import ZERO, RP2Decimal
 
-from dali.abstract_pair_converter_plugin import AssetPairAndTimestamp
+from dali.abstract_pair_converter_plugin import AssetPairAndTimestamp, MappedGraph
 from dali.cache import CACHE_DIR, load_from_cache
 from dali.configuration import Keyword
 from dali.historical_bar import HistoricalBar
 from dali.plugin.pair_converter.ccxt import PairConverterPlugin
 from dali.plugin.pair_converter.csv.kraken import Kraken as KrakenCsvPricing
 
 # Default exchange
 TEST_EXCHANGE: str = "Kraken"
 ALT_EXCHANGE: str = "Binance.com"
 LOCKED_EXCHANGE: str = "Kraken"
 FIAT_EXHANGE: str = "fiat"
-TEST_GRAPH: Dict[str, List[str]] = {
-    "BETH": ["ETH"],
-    "BTC": ["USDT", "GBP"],
-    "ETH": ["USDT"],
-    "USDT": ["USD"],
-    "USD": ["JPY"],
-}
 TEST_MARKETS: Dict[str, List[str]] = {
     "BTCUSDT": [ALT_EXCHANGE],
     "BTCGBP": [ALT_EXCHANGE],
     "BETHETH": [ALT_EXCHANGE],
     "ETHUSDT": [ALT_EXCHANGE],
     "USDTUSD": [TEST_EXCHANGE],
     "USDJPY": [FIAT_EXHANGE],
@@ -106,15 +101,34 @@
 KRAKEN_CLOSE: RP2Decimal = RP2Decimal("1.5558")
 KRAKEN_VOLUME: RP2Decimal = RP2Decimal("15.15")
 
 _MS_IN_SECOND: int = 1000
 
 
 class TestCcxtPlugin:
-    def __btcusdt_mock(self, plugin: PairConverterPlugin, mocker: Any) -> None:
+    @pytest.fixture
+    def test_graph(self) -> MappedGraph[str]:
+        beth: Vertex[str] = Vertex[str](name="BETH")
+        btc: Vertex[str] = Vertex[str](name="BTC")
+        eth: Vertex[str] = Vertex[str](name="ETH")
+        gbp: Vertex[str] = Vertex[str](name="GBP")
+        jpy: Vertex[str] = Vertex[str](name="JPY")
+        usdt: Vertex[str] = Vertex[str](name="USDT")
+        usd: Vertex[str] = Vertex[str](name="USD")
+
+        beth.add_neighbor(eth, 1.0)
+        btc.add_neighbor(usdt, 1.0)
+        btc.add_neighbor(gbp, 1.0)
+        eth.add_neighbor(usdt, 1.0)
+        usdt.add_neighbor(usd, 1.0)
+        usd.add_neighbor(jpy, 2.0)
+
+        return MappedGraph[str]([beth, btc, eth, gbp, jpy, usdt, usd])
+
+    def __btcusdt_mock(self, plugin: PairConverterPlugin, mocker: Any, test_graph: MappedGraph[str]) -> None:
         exchange = kraken(
             {
                 "apiKey": "key",
                 "secret": "secret",
             }
         )
         alt_exchange = binance(
@@ -147,32 +161,32 @@
                 USDTUSD_HIGH,  # (H)ighest price, float
                 USDTUSD_LOW,  # (L)owest price, float
                 USDTUSD_CLOSE,  # (C)losing price, float
                 USDTUSD_VOLUME,  # (V)olume (in terms of the base currency), float
             ],
         ]
         mocker.patch.object(plugin, "_PairConverterPlugin__exchanges", {TEST_EXCHANGE: exchange, ALT_EXCHANGE: alt_exchange})
-        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: TEST_GRAPH})
+        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: test_graph})
 
-    def test_unknown_exchange(self, mocker: Any) -> None:
+    def test_unknown_exchange(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
-        self.__btcusdt_mock(plugin, mocker)
+        self.__btcusdt_mock(plugin, mocker, test_graph)
 
         data = plugin.get_historic_bar_from_native_source(BAR_TIMESTAMP, "BTC", "USD", "Bogus Exchange")
         assert data
 
-    def test_historical_prices(self, mocker: Any) -> None:
+    def test_historical_prices(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
         cache_path = os.path.join(CACHE_DIR, plugin.cache_key())
         if os.path.exists(cache_path):
             os.remove(cache_path)
 
         # Reinstantiate plugin now that cache is gone
         plugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
-        self.__btcusdt_mock(plugin, mocker)
+        self.__btcusdt_mock(plugin, mocker, test_graph)
 
         data = plugin.get_historic_bar_from_native_source(BAR_TIMESTAMP, "BTC", "USD", TEST_EXCHANGE)
 
         assert data
         assert data.timestamp == BAR_TIMESTAMP
         assert data.low == BAR_LOW * USDTUSD_LOW
         assert data.high == BAR_HIGH * USDTUSD_HIGH
@@ -211,17 +225,17 @@
         timestamp = datetime(2020, 6, 1, 0, 0)
 
         mocker.patch.object(plugin, "get_historic_bar_from_native_source").return_value = None
 
         data = plugin.get_historic_bar_from_native_source(timestamp, "BOGUSCOIN", "JPY", TEST_EXCHANGE)
         assert data is None
 
-    def test_missing_fiat_pair(self, mocker: Any) -> None:
+    def test_missing_fiat_pair(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
-        self.__btcusdt_mock(plugin, mocker)
+        self.__btcusdt_mock(plugin, mocker, test_graph)
 
         mocker.patch.object(plugin, "_get_fiat_exchange_rate").return_value = HistoricalBar(
             duration=timedelta(seconds=86400),
             timestamp=BAR_TIMESTAMP,
             open=RP2Decimal(str(JPY_USD_RATE)),
             high=RP2Decimal(str(JPY_USD_RATE)),
             low=RP2Decimal(str(JPY_USD_RATE)),
@@ -237,15 +251,15 @@
         assert data.high == BAR_HIGH * USDTUSD_HIGH * JPY_USD_RATE
         assert data.open == BAR_OPEN * USDTUSD_OPEN * JPY_USD_RATE
         assert data.close == BAR_CLOSE * USDTUSD_CLOSE * JPY_USD_RATE
         assert data.volume == BAR_VOLUME + USDTUSD_VOLUME
 
     # Some crypto assets have no fiat or stable coin pair; they are only paired with BTC or ETH (e.g. EZ or BETH)
     # To get an accurate fiat price, we must get the price in the base asset (e.g. BETH -> ETH) then convert that to fiat (e.g. ETH -> USD)
-    def test_no_fiat_pair(self, mocker: Any) -> None:
+    def test_no_fiat_pair(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
 
         exchange = kraken(
             {
                 "apiKey": "key",
                 "secret": "secret",
             }
@@ -294,28 +308,28 @@
                 USDTUSD_HIGH,  # (H)ighest price, float
                 USDTUSD_LOW,  # (L)owest price, float
                 USDTUSD_CLOSE,  # (C)losing price, float
                 USDTUSD_VOLUME,  # (V)olume (in terms of the base currency), float
             ],
         ]
         mocker.patch.object(plugin, "_PairConverterPlugin__exchanges", {TEST_EXCHANGE: exchange, ALT_EXCHANGE: alt_exchange})
-        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: TEST_GRAPH})
+        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: test_graph})
 
         data = plugin.get_historic_bar_from_native_source(BETHETH_TIMESTAMP, "BETH", "USD", TEST_EXCHANGE)
 
         assert data
         assert data.timestamp == BETHETH_TIMESTAMP
         assert data.low == BETHETH_LOW * ETHUSDT_LOW * USDTUSD_LOW
         assert data.high == BETHETH_HIGH * ETHUSDT_HIGH * USDTUSD_HIGH
         assert data.open == BETHETH_OPEN * ETHUSDT_OPEN * USDTUSD_OPEN
         assert data.close == BETHETH_CLOSE * ETHUSDT_CLOSE * USDTUSD_CLOSE
         assert data.volume == BETHETH_VOLUME + ETHUSDT_VOLUME + USDTUSD_VOLUME
 
     # Test to make sure the default stable coin is not used with a fiat market that does exist on the exchange
-    def test_nonusd_fiat_pair(self, mocker: Any) -> None:
+    def test_nonusd_fiat_pair(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value, default_exchange="Binance.com")
         alt_exchange = binance(
             {
                 "apiKey": "key",
                 "secret": "secret",
             }
         )
@@ -343,39 +357,39 @@
                 BTCGBP_HIGH,  # (H)ighest price, float
                 BTCGBP_LOW,  # (L)owest price, float
                 BTCGBP_CLOSE,  # (C)losing price, float
                 BTCGBP_VOLUME,  # (V)olume (in terms of the base currency), float
             ],
         ]
         mocker.patch.object(plugin, "_PairConverterPlugin__exchanges", {TEST_EXCHANGE: exchange, ALT_EXCHANGE: alt_exchange})
-        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: TEST_GRAPH})
+        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: test_graph})
 
         data = plugin.get_historic_bar_from_native_source(BTCGBP_TIMESTAMP, "BTC", "GBP", TEST_EXCHANGE)
 
         assert data
         assert data.timestamp == BTCGBP_TIMESTAMP
         assert data.low == BTCGBP_LOW
         assert data.high == BTCGBP_HIGH
         assert data.open == BTCGBP_OPEN
         assert data.close == BTCGBP_CLOSE
         assert data.volume == BTCGBP_VOLUME
 
     # Plugin should hand off the handling of a fiat to fiat pair to the fiat converter
-    def test_fiat_pair(self, mocker: Any) -> None:
+    def test_fiat_pair(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value)
         exchange = binance(
             {
                 "apiKey": "key",
                 "secret": "secret",
             }
         )
 
         # Need to be mocked to prevent logger spam
         mocker.patch.object(plugin, "_PairConverterPlugin__exchange_markets", {TEST_EXCHANGE: ["WHATEVER"]})
-        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: TEST_GRAPH})
+        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: test_graph})
         mocker.patch.object(plugin, "_get_fiat_exchange_rate").return_value = HistoricalBar(
             duration=timedelta(seconds=86400),
             timestamp=EUR_USD_TIMESTAMP,
             open=RP2Decimal(str(EUR_USD_RATE)),
             high=RP2Decimal(str(EUR_USD_RATE)),
             low=RP2Decimal(str(EUR_USD_RATE)),
             close=RP2Decimal(str(EUR_USD_RATE)),
@@ -389,15 +403,15 @@
         assert data.timestamp == EUR_USD_TIMESTAMP
         assert data.low == EUR_USD_RATE
         assert data.high == EUR_USD_RATE
         assert data.open == EUR_USD_RATE
         assert data.close == EUR_USD_RATE
         assert data.volume == ZERO
 
-    def test_kraken_csv(self, mocker: Any) -> None:
+    def test_kraken_csv(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value, google_api_key="whatever")
 
         cache_path = os.path.join(CACHE_DIR, "Test-" + plugin.cache_key())
         if os.path.exists(cache_path):
             os.remove(cache_path)
 
         kraken_csv = KrakenCsvPricing(google_api_key="whatever")
@@ -442,27 +456,27 @@
                 USDTUSD_HIGH,  # (H)ighest price, float
                 USDTUSD_LOW,  # (L)owest price, float
                 USDTUSD_CLOSE,  # (C)losing price, float
                 USDTUSD_VOLUME,  # (V)olume (in terms of the base currency), float
             ],
         ]
         mocker.patch.object(plugin, "_PairConverterPlugin__exchanges", {TEST_EXCHANGE: exchange, ALT_EXCHANGE: alt_exchange})
-        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: TEST_GRAPH})
+        mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {TEST_EXCHANGE: test_graph})
 
         data = plugin.get_historic_bar_from_native_source(KRAKEN_TIMESTAMP, "BTC", "USD", TEST_EXCHANGE)
 
         assert data
         assert data.timestamp == KRAKEN_TIMESTAMP
         assert data.low == BAR_LOW * KRAKEN_LOW
         assert data.high == BAR_HIGH * KRAKEN_HIGH
         assert data.open == BAR_OPEN * KRAKEN_OPEN
         assert data.close == BAR_CLOSE * KRAKEN_CLOSE
         assert data.volume == BAR_VOLUME + KRAKEN_VOLUME
 
-    def test_locked_exchange(self, mocker: Any) -> None:
+    def test_locked_exchange(self, mocker: Any, test_graph: MappedGraph[str]) -> None:
         plugin: PairConverterPlugin = PairConverterPlugin(Keyword.HISTORICAL_PRICE_HIGH.value, default_exchange=LOCKED_EXCHANGE, exchange_locked=True)
         # Name is changed to exchange_instance to avoid conflicts with the side effect function `add_exchange_side_effect`
         exchange_instance = kraken(
             {
                 "apiKey": "key",
                 "secret": "secret",
             }
@@ -497,15 +511,15 @@
                 USDTUSD_CLOSE,  # (C)losing price, float
                 USDTUSD_VOLUME,  # (V)olume (in terms of the base currency), float
             ],
         ]
 
         def add_exchange_side_effect(exchange: str) -> None:  # pylint: disable=unused-argument
             mocker.patch.object(plugin, "_PairConverterPlugin__exchanges", {LOCKED_EXCHANGE: exchange_instance})
-            mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {LOCKED_EXCHANGE: TEST_GRAPH})
+            mocker.patch.object(plugin, "_PairConverterPlugin__exchange_graphs", {LOCKED_EXCHANGE: test_graph})
             mocker.patch.object(plugin, "_PairConverterPlugin__exchange_markets", {LOCKED_EXCHANGE: LOCKED_MARKETS})
 
         mocker.patch.object(plugin, "_add_exchange_to_memcache", autospec=True).side_effect = add_exchange_side_effect
 
         data = plugin.get_historic_bar_from_native_source(BAR_TIMESTAMP, "BTC", "USD", "not-kraken")
 
         assert data
```

### Comparing `dali-rp2-0.6.8/tests/test_plugin_coinbase.py` & `dali-rp2-0.6.9/tests/test_plugin_coinbase.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_coinbase_pro.py` & `dali-rp2-0.6.9/tests/test_plugin_coinbase_pro.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_coincheck_supplemental.py` & `dali-rp2-0.6.9/tests/test_plugin_coincheck_supplemental.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_historic_crypto.py` & `dali-rp2-0.6.9/tests/test_plugin_historic_crypto.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_kraken_csv_download.py` & `dali-rp2-0.6.9/tests/test_plugin_kraken_csv_download.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_ods_rp2_input.py` & `dali-rp2-0.6.9/tests/test_plugin_ods_rp2_input.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_plugin_pionex.py` & `dali-rp2-0.6.9/tests/test_plugin_pionex.py`

 * *Files identical despite different names*

### Comparing `dali-rp2-0.6.8/tests/test_transaction_resolver.py` & `dali-rp2-0.6.9/tests/test_transaction_resolver.py`

 * *Files identical despite different names*

