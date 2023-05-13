# Comparing `tmp/czsc-0.9.8.tar.gz` & `tmp/czsc-0.9.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "czsc-0.9.8.tar", last modified: Sun Feb 19 03:53:49 2023, max compression
+gzip compressed data, was "czsc-0.9.9.tar", last modified: Sun Feb 26 12:12:42 2023, max compression
```

## Comparing `czsc-0.9.8.tar` & `czsc-0.9.9.tar`

### file list

```diff
@@ -1,112 +1,115 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.089856 czsc-0.9.8/
--rw-r--r--   0 runner    (1001) docker     (123)      553 2023-02-19 03:53:07.000000 czsc-0.9.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     8452 2023-02-19 03:53:49.089856 czsc-0.9.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6922 2023-02-19 03:53:07.000000 czsc-0.9.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/
--rw-r--r--   0 runner    (1001) docker     (123)     1247 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/ai/
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/ai/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3114 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/ai/sk.py
--rw-r--r--   0 runner    (1001) docker     (123)     1856 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/ai/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    13897 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/analyze.py
--rw-r--r--   0 runner    (1001) docker     (123)    54710 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/aphorism.py
--rw-r--r--   0 runner    (1001) docker     (123)     1979 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/cmd.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/connectors/
--rw-r--r--   0 runner    (1001) docker     (123)      156 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/connectors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    19022 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/connectors/qmt_connector.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/data/
--rw-r--r--   0 runner    (1001) docker     (123)     1417 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4241 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/data/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    19840 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/data/jq.py
--rw-r--r--   0 runner    (1001) docker     (123)     4813 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/data/ts.py
--rw-r--r--   0 runner    (1001) docker     (123)    25868 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/data/ts_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)      614 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/eda.py
--rw-r--r--   0 runner    (1001) docker     (123)     1097 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/enum.py
--rw-r--r--   0 runner    (1001) docker     (123)     1875 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/envs.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/fsa/
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/fsa/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6518 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/fsa/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5175 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/fsa/im.py
--rw-r--r--   0 runner    (1001) docker     (123)    10604 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/fsa/spreed_sheets.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/gms/
--rw-r--r--   0 runner    (1001) docker     (123)      139 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/gms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16629 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/gms/gm_base.py
--rw-r--r--   0 runner    (1001) docker     (123)    16972 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/gms/gm_stocks.py
--rw-r--r--   0 runner    (1001) docker     (123)    28762 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/objects.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc/sensors/
--rw-r--r--   0 runner    (1001) docker     (123)      342 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/sensors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9228 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/sensors/plates.py
--rw-r--r--   0 runner    (1001) docker     (123)    28016 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/sensors/stocks.py
--rw-r--r--   0 runner    (1001) docker     (123)     9271 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/sensors/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/czsc/signals/
--rw-r--r--   0 runner    (1001) docker     (123)     2856 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21485 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/bar.py
--rw-r--r--   0 runner    (1001) docker     (123)    35473 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/bxt.py
--rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/byi.py
--rw-r--r--   0 runner    (1001) docker     (123)     2333 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/coo.py
--rw-r--r--   0 runner    (1001) docker     (123)    12340 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/cxt.py
--rw-r--r--   0 runner    (1001) docker     (123)    44875 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/jcc.py
--rw-r--r--   0 runner    (1001) docker     (123)    42815 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/tas.py
--rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/signals/vol.py
--rw-r--r--   0 runner    (1001) docker     (123)     9309 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/strategies.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/czsc/traders/
--rw-r--r--   0 runner    (1001) docker     (123)      340 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/traders/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12926 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/traders/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    16038 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/traders/performance.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/czsc/utils/
--rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8729 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/bar_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)      703 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/corr.py
--rw-r--r--   0 runner    (1001) docker     (123)    18368 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/echarts_plot.py
--rw-r--r--   0 runner    (1001) docker     (123)     1286 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/io.py
--rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/qywx.py
--rw-r--r--   0 runner    (1001) docker     (123)     9869 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/sig.py
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/ta.py
--rw-r--r--   0 runner    (1001) docker     (123)     2125 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/ta1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4883 2023-02-19 03:53:07.000000 czsc-0.9.8/czsc/utils/word_writer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.081856 czsc-0.9.8/czsc.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     8452 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2175 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-02-19 03:53:48.000000 czsc-0.9.8/czsc.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.025856 czsc-0.9.8/examples/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/examples/dropit/
--rw-r--r--   0 runner    (1001) docker     (123)      115 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3160 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/gm_backtest.py
--rw-r--r--   0 runner    (1001) docker     (123)      684 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/gm_check_point.py
--rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/gm_realtime.py
--rw-r--r--   0 runner    (1001) docker     (123)     1643 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/jq_check_point.py
--rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/quick_start.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/ts_continue_simulator.py
--rw-r--r--   0 runner    (1001) docker     (123)      855 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/ts_dummy_trader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1207 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/dropit/ts_trade_replay.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/examples/signals_dev/
--rw-r--r--   0 runner    (1001) docker     (123)      116 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/signals_dev/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/signals_dev/bar_big_solid.py
--rw-r--r--   0 runner    (1001) docker     (123)     3667 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/signals_dev/tas_first_bs_V230217.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/examples/strategies/
--rw-r--r--   0 runner    (1001) docker     (123)      138 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/strategies/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6184 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/strategies/cat_sma.py
--rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/strategies/check_signal.py
--rw-r--r--   0 runner    (1001) docker     (123)     4188 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/strategies/czsc_strategy_sma5.py
--rw-r--r--   0 runner    (1001) docker     (123)     1531 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/strategies/tcs_sma.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.085856 czsc-0.9.8/examples/test_offline/
--rw-r--r--   0 runner    (1001) docker     (123)      137 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/test_offline/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3538 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/test_offline/test_fsa.py
--rw-r--r--   0 runner    (1001) docker     (123)     7149 2023-02-19 03:53:07.000000 czsc-0.9.8/examples/test_offline/test_ts_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-19 03:53:49.089856 czsc-0.9.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-02-19 03:53:07.000000 czsc-0.9.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-19 03:53:49.089856 czsc-0.9.8/test/
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_ai_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3807 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_analyze.py
--rw-r--r--   0 runner    (1001) docker     (123)     3157 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_bar_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1172 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_data.py
--rw-r--r--   0 runner    (1001) docker     (123)     8926 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_objects.py
--rw-r--r--   0 runner    (1001) docker     (123)     1245 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_plot.py
--rw-r--r--   0 runner    (1001) docker     (123)      487 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_sensors.py
--rw-r--r--   0 runner    (1001) docker     (123)    11154 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_trader_base.py
--rw-r--r--   0 runner    (1001) docker     (123)      368 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-02-19 03:53:07.000000 czsc-0.9.8/test/test_word_writer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.637994 czsc-0.9.9/
+-rw-r--r--   0 runner    (1001) docker     (123)      553 2023-02-26 12:11:52.000000 czsc-0.9.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     8452 2023-02-26 12:12:42.637994 czsc-0.9.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6922 2023-02-26 12:11:52.000000 czsc-0.9.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.625994 czsc-0.9.9/czsc/
+-rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/ai/
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/ai/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3114 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/ai/sk.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1856 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/ai/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13897 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/analyze.py
+-rw-r--r--   0 runner    (1001) docker     (123)    54710 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/aphorism.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1979 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/cmd.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/connectors/
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/connectors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26923 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/connectors/gm_connector.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26619 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/connectors/qmt_connector.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/data/
+-rw-r--r--   0 runner    (1001) docker     (123)     1417 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4241 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/data/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19840 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/data/jq.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4813 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/data/ts.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25868 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/data/ts_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)      614 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/eda.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1097 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1875 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/envs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/fsa/
+-rw-r--r--   0 runner    (1001) docker     (123)      867 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/fsa/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6516 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/fsa/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5175 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/fsa/im.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10604 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/fsa/spreed_sheets.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31218 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/objects.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/sensors/
+-rw-r--r--   0 runner    (1001) docker     (123)      342 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/sensors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9228 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/sensors/plates.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28016 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/sensors/stocks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9271 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/sensors/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/signals/
+-rw-r--r--   0 runner    (1001) docker     (123)     2929 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22736 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/bar.py
+-rw-r--r--   0 runner    (1001) docker     (123)    35473 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/bxt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/byi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2333 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/coo.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16834 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/cxt.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44875 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/jcc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42815 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/tas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/signals/vol.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14847 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/strategies.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc/traders/
+-rw-r--r--   0 runner    (1001) docker     (123)      340 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/traders/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14045 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/traders/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16006 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/traders/performance.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.633994 czsc-0.9.9/czsc/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)     1856 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8689 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/bar_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      703 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/corr.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18368 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/echarts_plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1286 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/io.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6648 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/plotly_plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/qywx.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9869 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/sig.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/ta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2125 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/ta1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4883 2023-02-26 12:11:52.000000 czsc-0.9.9/czsc/utils/word_writer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.629994 czsc-0.9.9/czsc.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8452 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2347 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      272 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-02-26 12:12:42.000000 czsc-0.9.9/czsc.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.625994 czsc-0.9.9/examples/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.633994 czsc-0.9.9/examples/dropit/
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3160 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/gm_backtest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      684 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/gm_check_point.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/gm_realtime.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1643 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/jq_check_point.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/quick_start.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/ts_continue_simulator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      855 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/ts_dummy_trader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1207 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/dropit/ts_trade_replay.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.633994 czsc-0.9.9/examples/signals_dev/
+-rw-r--r--   0 runner    (1001) docker     (123)      116 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/bar_big_solid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/bar_vol_bs1_V230224.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4321 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/cxt_bi_end_V230222.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2780 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/cxt_bi_end_V230224.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3667 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/signals_dev/tas_first_bs_V230217.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.633994 czsc-0.9.9/examples/strategies/
+-rw-r--r--   0 runner    (1001) docker     (123)      138 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/strategies/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6184 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/strategies/cat_sma.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/strategies/check_signal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4188 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/strategies/czsc_strategy_sma5.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1531 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/strategies/tcs_sma.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.633994 czsc-0.9.9/examples/test_offline/
+-rw-r--r--   0 runner    (1001) docker     (123)      137 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/test_offline/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3538 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/test_offline/test_fsa.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7149 2023-02-26 12:11:52.000000 czsc-0.9.9/examples/test_offline/test_ts_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-26 12:12:42.637994 czsc-0.9.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-02-26 12:11:52.000000 czsc-0.9.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 12:12:42.637994 czsc-0.9.9/test/
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_ai_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3807 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_analyze.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3157 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_bar_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1172 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8926 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_objects.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1245 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1430 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_plotly_plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)      487 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_sensors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_strategy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11398 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_trader_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      368 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-02-26 12:11:52.000000 czsc-0.9.9/test/test_word_writer.py
```

### Comparing `czsc-0.9.8/LICENSE` & `czsc-0.9.9/LICENSE`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/PKG-INFO` & `czsc-0.9.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: czsc
-Version: 0.9.8
+Version: 0.9.9
 Summary: 缠中说禅技术分析工具
 Home-page: https://github.com/zengbin93/czsc
 Author: zengbin93
 Author-email: zeng_bin8888@163.com
 License: Apache Software License
 Description: # czsc - 缠中说禅技术分析工具
```

### Comparing `czsc-0.9.8/README.md` & `czsc-0.9.9/README.md`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/__init__.py` & `czsc-0.9.9/czsc/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -11,20 +11,22 @@
 from czsc import sensors
 from czsc import aphorism
 from czsc.analyze import CZSC
 from czsc.objects import Freq, Operate, Direction, Signal, Factor, Event, RawBar, NewBar, Position
 from czsc.utils.cache import home_path, get_dir_size, empty_cache_path
 from czsc.traders import CzscTrader, CzscSignals, generate_czsc_signals
 from czsc.traders import PairsPerformance, combine_holds_and_pairs, combine_dates_and_pairs
+from czsc.strategies import CzscStrategyBase
+from czsc.utils import KlineChart, BarGenerator, resample_bars, dill_dump, dill_load, read_json, save_json
 
 
-__version__ = "0.9.8"
+__version__ = "0.9.9"
 __author__ = "zengbin93"
 __email__ = "zeng_bin8888@163.com"
-__date__ = "20230210"
+__date__ = "20230220"
 
 
 if envs.get_welcome():
     print(f"欢迎使用CZSC！当前版本标识为 {__version__}@{__date__}\n")
     aphorism.print_one()
 
     print(f"CZSC环境变量："
```

### Comparing `czsc-0.9.8/czsc/ai/sk.py` & `czsc-0.9.9/czsc/ai/sk.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/ai/utils.py` & `czsc-0.9.9/czsc/ai/utils.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/analyze.py` & `czsc-0.9.9/czsc/analyze.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/aphorism.py` & `czsc-0.9.9/czsc/aphorism.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/cmd.py` & `czsc-0.9.9/czsc/cmd.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/data/__init__.py` & `czsc-0.9.9/czsc/data/__init__.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/data/base.py` & `czsc-0.9.9/czsc/data/base.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/data/jq.py` & `czsc-0.9.9/czsc/data/jq.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/data/ts.py` & `czsc-0.9.9/czsc/data/ts.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/data/ts_cache.py` & `czsc-0.9.9/czsc/data/ts_cache.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/eda.py` & `czsc-0.9.9/czsc/eda.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/enum.py` & `czsc-0.9.9/czsc/enum.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/envs.py` & `czsc-0.9.9/czsc/envs.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/fsa/__init__.py` & `czsc-0.9.9/czsc/fsa/__init__.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/fsa/base.py` & `czsc-0.9.9/czsc/fsa/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 import time
 import requests
 from loguru import logger
 from tenacity import retry, stop_after_attempt, wait_random
 from requests_toolbelt import MultipartEncoder
 
 
-@retry(stop=stop_after_attempt(10), wait=wait_random(min=3, max=10))
+@retry(stop=stop_after_attempt(3), wait=wait_random(min=1, max=5))
 def request(method, url, headers, payload=None) -> dict:
     """飞书API标准请求
 
     :param method: 请求方法
     :param url: 请求地址
     :param headers: 请求头
     :param payload: 传参
```

### Comparing `czsc-0.9.8/czsc/fsa/im.py` & `czsc-0.9.9/czsc/fsa/im.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/fsa/spreed_sheets.py` & `czsc-0.9.9/czsc/fsa/spreed_sheets.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/gms/gm_base.py` & `czsc-0.9.9/czsc/connectors/gm_connector.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,41 +1,43 @@
 # -*- coding: utf-8 -*-
 """
 author: zengbin93
 email: zeng_bin8888@163.com
-create_dt: 2021/11/17 22:11
-describe: 配合 CzscAdvancedTrader 进行使用的掘金工具
+create_dt: 2023/2/26 18:49
+describe: 掘金量化终端对接
 """
 import os
 import dill
 import czsc
+import inspect
 import pandas as pd
 from loguru import logger
 try:
     from gm.api import *
 except:
     logger.warning(f"gm 模块没有安装")
 from datetime import datetime, timedelta
 from collections import OrderedDict
-from typing import List, Callable
-from czsc import CzscAdvancedTrader, create_advanced_trader
+from typing import List
+from czsc import CzscTrader, CzscStrategyBase
 from czsc.data import freq_cn2gm
 from czsc.utils import qywx as wx
 from czsc.utils import BarGenerator
 from czsc.objects import RawBar, Freq
 
 
 dt_fmt = "%Y-%m-%d %H:%M:%S"
 date_fmt = "%Y-%m-%d"
 
-assert czsc.__version__ >= "0.8.29"
+assert czsc.__version__ >= "0.9.8"
 
 
 def set_gm_token(token):
-    with open(os.path.join(os.path.expanduser("~"), "gm_token.txt"), 'w', encoding='utf-8') as f:
+    __file_token = os.path.join(os.path.expanduser("~"), "gm_token.txt")
+    with open(__file_token, 'w', encoding='utf-8') as f:
         f.write(token)
 
 
 file_token = os.path.join(os.path.expanduser("~"), "gm_token.txt")
 if not os.path.exists(file_token):
     print("{} 文件不存在，请单独启动一个 python 终端，调用 set_gm_token 方法创建该文件，再重新执行。".format(file_token))
 else:
@@ -185,56 +187,37 @@
     ExecType_Trade: "成交(有效)",
     ExecType_OrderStatus: "委托状态",
     ExecType_CancelRejected: "撤单被拒绝(有效)",
 }
 
 
 def on_order_status(context, order):
-    """
+    """订单状态更新通知
+
     https://www.myquant.cn/docs/python/python_object_trade#007ae8f5c7ec5298
 
     :param context:
     :param order:
     :return:
     """
     if not is_trade_time(context.now):
         return
 
     symbol = order.symbol
     latest_dt = context.now.strftime("%Y-%m-%d %H:%M:%S")
 
-    if symbol not in context.symbols_info.keys():
-        msg = f"订单状态更新通知：\n{'*' * 31}\n" \
-              f"更新时间：{latest_dt}\n" \
-              f"标的名称：{symbol} {context.stocks.get(symbol, '无名')}\n" \
-              f"操作类型：{order_side_map[order.side]}{pos_effect_map[order.position_effect]}\n" \
-              f"操作描述：非机器交易标的\n" \
-              f"下单价格：{round(order.price, 2)}\n" \
-              f"最新状态：{order_status_map[order.status]}\n" \
-              f"委托（股）：{int(order.volume)}\n" \
-              f"已成（股）：{int(order.filled_volume)}\n" \
-              f"均价（元）：{round(order.filled_vwap, 2)}"
-
-    else:
-        trader: CzscAdvancedTrader = context.symbols_info[symbol]['trader']
-        if trader.long_pos.operates:
-            last_op_desc = trader.long_pos.operates[-1]['op_desc']
-        else:
-            last_op_desc = ""
-
-        msg = f"订单状态更新通知：\n{'*' * 31}\n" \
-              f"更新时间：{latest_dt}\n" \
-              f"标的名称：{symbol} {context.stocks.get(symbol, '无名')}\n" \
-              f"操作类型：{order_side_map[order.side]}{pos_effect_map[order.position_effect]}\n" \
-              f"操作描述：{last_op_desc}\n" \
-              f"下单价格：{round(order.price, 2)}\n" \
-              f"最新状态：{order_status_map[order.status]}\n" \
-              f"委托（股）：{int(order.volume)}\n" \
-              f"已成（股）：{int(order.filled_volume)}\n" \
-              f"均价（元）：{round(order.filled_vwap, 2)}"
+    msg = f"订单状态更新通知：\n{'*' * 31}\n" \
+          f"更新时间：{latest_dt}\n" \
+          f"标的名称：{symbol} {context.stocks.get(symbol, '无名')}\n" \
+          f"操作类型：{order_side_map[order.side]}{pos_effect_map[order.position_effect]}\n" \
+          f"下单价格：{round(order.price, 2)}\n" \
+          f"最新状态：{order_status_map[order.status]}\n" \
+          f"委托（股）：{int(order.volume)}\n" \
+          f"已成（股）：{int(order.filled_volume)}\n" \
+          f"均价（元）：{round(order.filled_vwap, 2)}"
 
     logger.info(msg.replace("\n", " - ").replace('*', ""))
     if context.mode != MODE_BACKTEST and order.status in [1, 3, 5, 8, 9, 12]:
         wx.push_text(content=str(msg), key=context.wx_key)
 
 
 def on_execution_report(context, execrpt):
@@ -312,51 +295,28 @@
 
     logger.info("回测结果：{}".format(row))
     content = ""
     for k, v in row.items():
         content += "{}: {}\n".format(k, v)
     wx.push_text(content=content, key=wx_key)
 
-    trades = []
-    operates = []
-    performances = []
-    for symbol in symbols:
-        trader: CzscAdvancedTrader = context.symbols_info[symbol]['trader']
-        trades.extend(trader.long_pos.pairs)
-        operates.extend(trader.long_pos.operates)
-        performances.append(trader.long_pos.evaluate_operates())
-
-    df = pd.DataFrame(trades)
-    df['开仓时间'] = df['开仓时间'].apply(lambda x: x.strftime("%Y-%m-%d %H:%M"))
-    df['平仓时间'] = df['平仓时间'].apply(lambda x: x.strftime("%Y-%m-%d %H:%M"))
-    df.to_excel(file, sheet_name='交易汇总', index=False)
-
-    dfo = pd.DataFrame(operates)
-    dfo['dt'] = dfo['dt'].apply(lambda x: x.strftime("%Y-%m-%d %H:%M"))
-    dfo.to_excel(file, sheet_name='操作汇总', index=False)
-
-    dfp = pd.DataFrame(performances)
-    dfp.to_excel(file, sheet_name='表现汇总', index=False)
-    file.close()
-
-    wx.push_file(file_xlsx, wx_key)
-
 
 def on_error(context, code, info):
     if not is_trade_time(context.now):
         return
 
     msg = "{} - {}".format(code, info)
     logger.warning(msg)
     if context.mode != MODE_BACKTEST:
         wx.push_text(content=msg, key=context.wx_key)
 
 
 def on_account_status(context, account):
     """响应交易账户状态更新事件，交易账户状态变化时被触发
+
     https://www.myquant.cn/docs/python/python_trade_event#4f07d24fc4314e3c
     """
     status = account['status']
     if status['state'] == 3:
         return
 
     if not is_trade_time(context.now):
@@ -412,55 +372,341 @@
     :param max_count:
     :return:
     """
     if not end_dt:
         end_dt = datetime.now().strftime(dt_fmt)
 
     bg, data = get_init_bg(gm_symbol, end_dt, freqs[0], freqs[1:], max_count, adjust)
-    ct = CzscAdvancedTrader(bg)
+    ct = CzscTrader(bg)
     for bar in data:
         ct.update(bar)
 
     if file_html:
         ct.take_snapshot(file_html)
         print(f'saved into {file_html}')
     else:
         ct.open_in_browser()
     return ct
 
 
-def strategy_snapshot(symbol, strategy: Callable, end_dt=None, file_html=None, adjust=ADJUST_PREV, max_count=1000):
-    """使用掘金的数据对任意标的、任意时刻的状态进行策略快照
-
-    :param symbol: 交易标的
-    :param strategy: 择时交易策略
-    :param end_dt: 结束时间，精确到分钟
-    :param file_html: 结果文件
-    :param adjust: 复权类型
-    :param max_count: 最大K线数量
-    :return: trader
-    """
-    tactic = strategy(symbol)
-    base_freq = tactic['base_freq']
-    freqs = tactic['freqs']
-    bg, data = get_init_bg(symbol, end_dt, base_freq, freqs, max_count, adjust)
-    trader = create_advanced_trader(bg, data, strategy)
-    if file_html:
-        trader.take_snapshot(file_html)
-        print(f'saved into {file_html}')
-    else:
-        trader.open_in_browser()
-    return trader
-
-
 def save_traders(context):
     """实盘：保存交易员快照"""
     if context.now.isoweekday() > 5:
         print(f"save_traders: {context.now} 不是交易时间")
         return
 
     for symbol in context.symbols_info.keys():
-        trader: CzscAdvancedTrader = context.symbols_info[symbol]['trader']
+        trader: CzscTrader = context.symbols_info[symbol]['trader']
         if context.mode != MODE_BACKTEST:
-            file_trader = os.path.join(context.data_path, f'traders/{symbol}.cat')
+            file_trader = os.path.join(context.data_path, f'traders/{symbol}.ct')
             dill.dump(trader, open(file_trader, 'wb'))
 
+
+indices = {
+    "上证指数": 'SHSE.000001',
+    "上证50": 'SHSE.000016',
+    "沪深300": "SHSE.000300",
+    "中证1000": "SHSE.000852",
+    "中证500": "SHSE.000905",
+
+    "深证成指": "SZSE.399001",
+    "创业板指数": 'SZSE.399006',
+    "深次新股": "SZSE.399678",
+    "中小板指": "SZSE.399005",
+    "国证2000": "SZSE.399303",
+    "小盘成长": "SZSE.399376",
+    "小盘价值": "SZSE.399377",
+}
+
+
+def get_index_shares(name, end_date=None):
+    """获取某一交易日的指数成分股列表
+
+    symbols = get_index_shares("上证50", "2019-01-01 09:30:00")
+    """
+    if not end_date:
+        end_date = datetime.now().strftime(date_fmt)
+    else:
+        end_date = pd.to_datetime(end_date).strftime(date_fmt)
+    constituents = get_history_constituents(indices[name], end_date, end_date)[0]
+    symbol_list = [k for k, v in constituents['constituents'].items()]
+    return list(set(symbol_list))
+
+
+def on_bar(context, bars):
+    """订阅K线回调函数"""
+    context.unfinished_orders = get_unfinished_orders()
+    cancel_timeout_orders(context, max_m=30)
+
+    for bar in bars:
+        symbol = bar['symbol']
+        trader: CzscTrader = context.symbols_info[symbol]['trader']
+
+        # 确保数据更新到最新时刻
+        base_freq = trader.base_freq
+        bars = context.data(symbol=symbol, frequency=freq_cn2gm[base_freq], count=100,
+                            fields='symbol,eob,open,close,high,low,volume,amount')
+        bars = format_kline(bars, freq=trader.bg.freq_map[base_freq])
+        bars_new = [x for x in bars if x.dt > trader.bg.bars[base_freq][-1].dt]
+        if bars_new:
+            for bar_ in bars_new:
+                trader.update(bar_)
+
+        # sync_long_position(context, trader)
+
+
+def report_account_status(context):
+    """报告账户持仓状态"""
+    if context.now.isoweekday() > 5:
+        return
+
+    latest_dt = context.now.strftime(dt_fmt)
+    account = context.account(account_id=context.account_id)
+    cash = account.cash
+    positions = account.positions()
+
+    logger.info("=" * 30 + f" 账户状态【{latest_dt}】 " + "=" * 30)
+    cash_report = f"净值：{int(cash.nav)}，可用资金：{int(cash.available)}，" \
+                  f"浮动盈亏：{int(cash.fpnl)}，标的数量：{len(positions)}"
+    logger.info(cash_report)
+
+    for p in positions:
+        p_report = f"标的：{p.symbol}，名称：{context.stocks.get(p.symbol, '无名')}，" \
+                   f"数量：{p.volume}，成本：{round(p.vwap, 2)}，方向：{p.side}，" \
+                   f"当前价：{round(p.price, 2)}，成本市值：{int(p.volume * p.vwap)}，" \
+                   f"建仓时间：{p.created_at.strftime(dt_fmt)}"
+        logger.info(p_report)
+
+    # 实盘或仿真，推送账户信息到企业微信
+    if context.mode != MODE_BACKTEST:
+
+        msg = f"股票账户状态报告\n{'*' * 31}\n"
+        msg += f"账户净值：{int(cash.nav)}\n" \
+               f"持仓市值：{int(cash.market_value)}\n" \
+               f"可用资金：{int(cash.available)}\n" \
+               f"浮动盈亏：{int(cash.fpnl)}\n" \
+               f"标的数量：{len(positions)}\n"
+        wx.push_text(msg.strip("\n *"), key=context.wx_key)
+
+        results = []
+        for symbol, info in context.symbols_info.items():
+            name = context.stocks.get(symbol, '无名')
+            trader: CzscTrader = context.symbols_info[symbol]['trader']
+            p = account.position(symbol=symbol, side=PositionSide_Long)
+
+            row = {'交易标的': symbol, '标的名称': name,
+                   '最新时间': trader.end_dt.strftime(dt_fmt),
+                   '最新价格': trader.latest_price}
+
+            if "日线" in trader.kas.keys():
+                bar1, bar2 = trader.kas['日线'].bars_raw[-2:]
+                row.update({'昨日收盘': round(bar1.close, 2),
+                            '今日涨幅': round(bar2.close / bar1.close - 1, 4)})
+
+            if p:
+                row.update({"实盘持仓数量": p.volume,
+                            "实盘持仓成本": round(p.vwap, 2),
+                            "实盘持仓市值": int(p.volume * p.vwap)})
+            else:
+                row.update({"实盘持仓数量": 0,  "实盘持仓成本": 0, "实盘持仓市值": 0})
+
+            results.append(row)
+
+        df = pd.DataFrame(results)
+        df.sort_values(['多头持仓', '多头收益'], ascending=False, inplace=True, ignore_index=True)
+        file_xlsx = os.path.join(context.data_path, f"holds_{context.now.strftime('%Y%m%d_%H%M')}.xlsx")
+        df.to_excel(file_xlsx, index=False)
+        wx.push_file(file_xlsx, key=context.wx_key)
+        os.remove(file_xlsx)
+
+        # 提示非策略交易标的持仓
+        process_out_of_symbols(context)
+
+
+def sync_long_position(context, trader: CzscTrader):
+    """同步多头仓位到交易账户"""
+    if not trader.positions:
+        return
+
+    symbol = trader.symbol
+    name = context.stocks.get(symbol, "无名标的")
+    long_pos = trader.get_ensemble_pos(method='vote')
+    max_sym_pos = context.symbols_info[symbol]['max_sym_pos']  # 最大标的仓位
+    if context.mode == MODE_BACKTEST:
+        account = context.account()
+    else:
+        account = context.account(account_id=context.account_id)
+    cash = account.cash
+
+    price = trader.latest_price
+    sym_position = account.position(symbol, PositionSide_Long)
+    if long_pos == 0 and not sym_position:
+        # 如果多头仓位为0且掘金账户没有对应持仓，直接退出
+        return
+
+    if long_pos == 0 and sym_position and sym_position.volume > 0:
+        # 如果多头仓位为0且掘金账户依然还有持仓，清掉仓位
+        order_target_volume(symbol=symbol, volume=0, position_side=PositionSide_Long,
+                            order_type=OrderType_Limit, price=price, account=account.id)
+        return
+
+    if not trader.pos_changed:
+        return
+
+    assert long_pos > 0
+    if cash.available < price * 120:
+        logger.info(f"{context.now} {symbol} {name} 可用资金不足，无法开多仓，最少所需资金{int(price * 120)}元")
+        return
+
+    if is_order_exist(context, symbol, PositionSide_Long):
+        logger.info(f"{context.now} {symbol} {name} 同方向订单已存在")
+        return
+
+    percent = max_sym_pos * long_pos
+    volume = int((cash.nav * percent / price // 100) * 100)     # 单位：股
+    order_target_volume(symbol=symbol, volume=volume, position_side=PositionSide_Long,
+                        order_type=OrderType_Limit, price=price, account=account.id)
+
+
+def process_out_of_symbols(context):
+    """实盘：处理不在交易列表的持仓股"""
+    if context.now.isoweekday() > 5:
+        print(f"process_out_of_symbols: {context.now} 不是交易时间")
+        return
+
+    if context.mode == MODE_BACKTEST:
+        print(f"process_out_of_symbols: 回测模式下不需要执行")
+        return
+
+    account = context.account(account_id=context.account_id)
+    positions = account.positions(symbol="", side=PositionSide_Long)
+
+    oos = []
+    for p in positions:
+        symbol = p.symbol
+        if p.volume > 0 and p.symbol not in context.symbols_info.keys():
+            oos.append(symbol)
+            # order_target_volume(symbol=symbol, volume=0, position_side=PositionSide_Long,
+            #                     order_type=OrderType_Limit, price=p.price, account=account.id)
+    if oos:
+        wx.push_text(f"不在交易列表的持仓股：{', '.join(oos)}", context.wx_key)
+
+
+def init_context_universal(context, name):
+    """通用 context 初始化：1、创建文件目录和日志记录
+
+    :param context:
+    :param name: 交易策略名称，建议使用英文
+    """
+    path_gm_logs = os.environ.get('path_gm_logs', None)
+    if context.mode == MODE_BACKTEST:
+        data_path = os.path.join(path_gm_logs, f"backtest/{name}_{datetime.now().strftime('%Y%m%d_%H%M%S')}")
+    else:
+        data_path = os.path.join(path_gm_logs, f"realtime/{name}")
+    os.makedirs(data_path, exist_ok=True)
+
+    context.name = name
+    context.data_path = data_path
+    context.stocks = get_symbol_names()
+
+    logger.add(os.path.join(data_path, "gm_trader.log"), rotation="500MB",
+               encoding="utf-8", enqueue=True, retention="1 days")
+    logger.info("运行配置：")
+    logger.info(f"data_path = {data_path}")
+
+    if context.mode == MODE_BACKTEST:
+        logger.info("backtest_start_time = " + str(context.backtest_start_time))
+        logger.info("backtest_end_time = " + str(context.backtest_end_time))
+
+
+def init_context_env(context):
+    """通用 context 初始化：2、读入环境变量
+
+    :param context:
+    """
+    context.wx_key = os.environ['wx_key']
+    context.account_id = os.environ.get('account_id', '')
+    if context.mode != MODE_BACKTEST:
+        assert len(context.account_id) > 10, "非回测模式，必须设置 account_id "
+
+    # 单个标的仓位控制[0, 1]，按资金百分比控制，1表示满仓，仅在开仓的时候控制
+    context.max_sym_pos = float(os.environ['max_sym_pos'])
+    assert 0 <= context.max_sym_pos <= 1
+
+    logger.info(f"环境变量读取结果如下：")
+    logger.info(f"单标的控制：context.max_sym_pos = {context.max_sym_pos}")
+
+
+def init_context_traders(context, symbols: List[str], strategy):
+    """通用 context 初始化：3、为每个标的创建 trader
+
+    :param context:
+    :param symbols: 交易标的列表
+    :param strategy: 交易策略
+    :return:
+    """
+    assert issubclass(strategy, CzscStrategyBase), "strategy 必须是 CzscStrategyBase 的子类"
+    with open(os.path.join(context.data_path, f'{strategy.__name__}.txt'), mode='w') as f:
+        f.write(inspect.getsource(strategy))
+
+    tactic = strategy(symbol="000001")
+    base_freq, freqs = tactic.sorted_freqs[0], tactic.sorted_freqs[1:]
+    frequency = freq_cn2gm[base_freq]
+    unsubscribe(symbols='*', frequency=frequency)
+
+    data_path = context.data_path
+    logger.info(f"输入交易标的数量：{len(symbols)}")
+    logger.info(f"交易员的周期列表：base_freq = {base_freq}; freqs = {freqs}")
+
+    os.makedirs(os.path.join(data_path, 'traders'), exist_ok=True)
+    symbols_info = {symbol: dict() for symbol in symbols}
+    for symbol in symbols:
+        try:
+            symbols_info[symbol]['max_sym_pos'] = context.max_sym_pos
+            file_trader = os.path.join(data_path, f'traders/{symbol}.cat')
+
+            if os.path.exists(file_trader) and context.mode != MODE_BACKTEST:
+                trader: CzscTrader = dill.load(open(file_trader, 'rb'))
+                logger.info(f"{symbol} Loaded Trader from {file_trader}")
+
+            else:
+                tactic = strategy(symbol=symbol)
+                bg, data = get_init_bg(symbol, context.now, base_freq, freqs, 1000, ADJUST_PREV)
+                trader = CzscTrader(bg, get_signals=tactic.get_signals, positions=tactic.positions)
+                dill.dump(trader, open(file_trader, 'wb'))
+
+            symbols_info[symbol]['trader'] = trader
+            logger.info("{} Trader 构建成功，最新时间：{}，多仓：{}".format(symbol, trader.end_dt, trader.long_pos.pos))
+
+        except Exception as e1:
+            del symbols_info[symbol]
+            logger.exception(f"{e1}：{symbol} - {context.stocks.get(symbol, '无名')} 初始化失败，当前时间：{context.now}")
+
+    subscribe(",".join(symbols_info.keys()), frequency=frequency, count=300, wait_group=False)
+    logger.info(f"订阅成功数量：{len(symbols_info)}")
+    logger.info(f"交易标的配置：{symbols_info}")
+    context.symbols_info = symbols_info
+
+
+def init_context_schedule(context):
+    """通用 context 初始化：设置定时任务"""
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='09:31:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='10:01:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='10:31:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='11:01:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='11:31:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='13:01:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='13:31:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='14:01:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='14:31:00')
+    schedule(schedule_func=report_account_status, date_rule='1d', time_rule='15:01:00')
+
+    # 以下是 实盘/仿真 模式下的定时任务
+    if context.mode != MODE_BACKTEST:
+        schedule(schedule_func=save_traders, date_rule='1d', time_rule='11:40:00')
+        schedule(schedule_func=save_traders, date_rule='1d', time_rule='15:10:00')
+        # schedule(schedule_func=realtime_check_index_status, date_rule='1d', time_rule='17:30:00')
+        # schedule(schedule_func=process_out_of_symbols, date_rule='1d', time_rule='09:40:00')
+
+
+
+
```

### Comparing `czsc-0.9.8/czsc/objects.py` & `czsc-0.9.9/czsc/objects.py`

 * *Files 11% similar despite different names*

```diff
@@ -2,14 +2,17 @@
 """
 author: zengbin93
 email: zeng_bin8888@163.com
 create_dt: 2021/3/10 12:21
 describe: 常用对象结构
 """
 import math
+import pandas as pd
+import numpy as np
+from copy import deepcopy
 from dataclasses import dataclass
 from datetime import datetime
 from loguru import logger
 from deprecated import deprecated
 from typing import List, Callable
 from czsc.enum import Mark, Direction, Freq, Operate
 from czsc.utils.corr import single_linear
@@ -623,23 +626,24 @@
             assert event.operate in [Operate.LO, Operate.LE, Operate.SO, Operate.SE]
 
         self.interval = interval
         self.timeout = timeout
         self.stop_loss = stop_loss
         self.T0 = T0
 
+        self.pos_changed = False  # 仓位是否发生变化
         self.operates = []  # 事件触发的操作列表
-        self.holds = []     # 持仓状态列表
+        self.holds = []  # 持仓状态列表
         self.pos = 0
 
         # 辅助判断的缓存数据
         self.last_event = {'dt': None, 'bid': None, 'price': None, "op": None, 'op_desc': None}
-        self.last_lo_dt = None      # 最近一次开多交易的时间
-        self.last_so_dt = None      # 最近一次开空交易的时间
-        self.end_dt = None          # 最近一次信号传入的时间
+        self.last_lo_dt = None  # 最近一次开多交易的时间
+        self.last_so_dt = None  # 最近一次开空交易的时间
+        self.end_dt = None  # 最近一次信号传入的时间
 
     def __repr__(self):
         return f"Position(name={self.name}, symbol={self.symbol}, opens={[x.name for x in self.opens]}, " \
                f"timeout={self.timeout}, stop_loss={self.stop_loss}BP, T0={self.T0}, interval={self.interval}s)"
 
     def dump(self, with_data=False):
         """将对象转换为 dict"""
@@ -650,36 +654,17 @@
             "exits": [x.dump() for x in self.exits],
             "interval": self.interval,
             "timeout": self.timeout,
             "stop_loss": self.stop_loss,
             "T0": self.T0,
         }
         if with_data:
-            raw.update({"pairs": self.pairs,  "holds": self.holds})
+            raw.update({"pairs": self.pairs, "holds": self.holds})
         return raw
 
-    def __two_operates_pair(self, op1, op2):
-        assert op1['op'] in [Operate.LO, Operate.SO]
-        pair = {
-            '标的代码': self.symbol,
-            '策略标记': self.name,
-            '交易方向': "多头" if op1['op'] == Operate.LO else "空头",
-            '开仓时间': op1['dt'],
-            '平仓时间': op2['dt'],
-            '开仓价格': op1['price'],
-            '平仓价格': op2['price'],
-            '持仓K线数': op2['bid'] - op1['bid'],
-            '事件序列': f"{op1['op_desc']} -> {op2['op_desc']}",
-            '持仓天数': (op2['dt'] - op1['dt']).total_seconds() / (24 * 3600),
-            '盈亏比例': op2['price'] / op1['price'] - 1 if op1['op'] == Operate.LO else 1 - op2['price'] / op1['price'],
-        }
-        # 盈亏比例 转换成以 BP 为单位的收益，1BP = 0.0001
-        pair['盈亏比例'] = round(pair['盈亏比例'] * 10000, 2)
-        return pair
-
     @property
     def pairs(self):
         """开平交易列表
 
         返回样例：
 
         [{'标的代码': '000001.SH',
@@ -706,17 +691,35 @@
         数据说明：
 
         1. 盈亏比例，单位是 BP
         2. 持仓天数，单位是 自然日
         3. 持仓K线数，指基础周期K线数量
         """
         pairs = []
+
         for op1, op2 in zip(self.operates, self.operates[1:]):
-            if op1['op'] in [Operate.LO, Operate.SO]:
-                pairs.append(self.__two_operates_pair(op1, op2))
+            if op1['op'] not in [Operate.LO, Operate.SO]:
+                continue
+
+            ykr = op2['price'] / op1['price'] - 1 if op1['op'] == Operate.LO else 1 - op2['price'] / op1['price']
+            pair = {
+                '标的代码': self.symbol,
+                '策略标记': self.name,
+                '交易方向': "多头" if op1['op'] == Operate.LO else "空头",
+                '开仓时间': op1['dt'],
+                '平仓时间': op2['dt'],
+                '开仓价格': op1['price'],
+                '平仓价格': op2['price'],
+                '持仓K线数': op2['bid'] - op1['bid'],
+                '事件序列': f"{op1['op_desc']} -> {op2['op_desc']}",
+                '持仓天数': (op2['dt'] - op1['dt']).total_seconds() / (24 * 3600),
+                '盈亏比例': round(ykr * 10000, 2),  # 盈亏比例 转换成以 BP 为单位的收益，1BP = 0.0001
+            }
+            pairs.append(pair)
+
         return pairs
 
     def evaluate_pairs(self, trade_dir: str = "多空") -> dict:
         """评估交易表现
 
         :param trade_dir: 交易方向，可选值 ['多头', '空头', '多空']
         :return: 交易表现
@@ -754,24 +757,82 @@
             p['单笔亏损'] = round(p['累计亏损'] / p['亏损次数'], 4)
 
             p['累计盈亏比'] = round(p['累计盈利'] / abs(p['累计亏损']), 4)
             p['单笔盈亏比'] = round(p['单笔盈利'] / abs(p['单笔亏损']), 4)
 
         return p
 
+    def evaluate_holds(self, trade_dir: str = "多空") -> dict:
+        """按持仓信号评估交易表现
+
+        :param trade_dir: 交易方向，可选值 ['多头', '空头', '多空']
+        :return: 交易表现
+        """
+        holds = deepcopy(self.holds)
+        if trade_dir != '多空':
+            _OD = 1 if trade_dir == "多头" else -1
+            for hold in holds:
+                if hold['pos'] != 0 and hold['pos'] != _OD:
+                    hold['pos'] = 0
+
+        p = {"交易标的": self.symbol, "策略标记": self.name, "交易方向": trade_dir,
+             "开始时间": "", "结束时间": "",
+             '覆盖率': 0, '夏普': 0, '卡玛': 0, '最大回撤': 0, '年化收益': 0, '日胜率': 0}
+
+        if len(holds) == 0 or all(x['pos'] == 0 for x in holds):
+            return p
+
+        dfh = pd.DataFrame(holds)
+        dfh['n1b'] = (dfh['price'].shift(1) - dfh['price']) / dfh['price']
+        dfh['trade_date'] = dfh['dt'].apply(lambda x: x.strftime('%Y-%m-%d'))
+        dfh['edge'] = dfh['n1b'] * dfh['pos']  # 持有下一根K线的边际收益
+
+        # 按日期聚合
+        dfv = dfh.groupby('trade_date')['edge'].sum()
+        dfv = dfv.cumsum()
+
+        yearly_n = 252
+        yearly_ret = dfv.iloc[-1] * (yearly_n / len(dfv))
+        sharp = dfv.diff().mean() / dfv.diff().std() * pow(yearly_n, 0.5) if dfv.diff().std() != 0 else 0
+        df0 = dfv.shift(1).ffill().fillna(0)
+        mdd = (1 - (df0 + 1) / (df0 + 1).cummax()).max()
+        calmar = yearly_ret / mdd if mdd != 0 else 1
+
+        p.update({
+            "开始时间": dfh['dt'].iloc[0].strftime('%Y-%m-%d'),
+            "结束时间": dfh['dt'].iloc[-1].strftime('%Y-%m-%d'),
+            '覆盖率': round(len(dfh[dfh['pos'] != 0]) / len(dfh), 4),
+            '夏普': round(sharp, 4),
+            '卡玛': round(calmar, 4),
+            '最大回撤': round(mdd, 4),
+            '年化收益': round(yearly_ret, 4),
+            '日胜率': round(sum(dfv > 0) / len(dfv), 4)})
+        return p
+
+    def evaluate(self, trade_dir: str = "多空") -> dict:
+        """评估交易表现
+
+        :param trade_dir: 交易方向，可选值 ['多头', '空头', '多空']
+        :return: 交易表现
+        """
+        p = self.evaluate_pairs(trade_dir)
+        p.update(self.evaluate_holds(trade_dir))
+        return p
+
     def update(self, s: dict):
         """更新持仓状态
 
         :param s: 最新信号字典
         :return:
         """
         if self.end_dt and s['dt'] <= self.end_dt:
             logger.warning(f"请检查信号传入：最新信号时间{s['dt']}在上次信号时间{self.end_dt}之前")
             return
 
+        self.pos_changed = False
         op = Operate.HO
         op_desc = ""
         for event in self.events:
             m, f = event.is_match(s)
             if m:
                 op = event.operate
                 op_desc = f"{event.name}@{f}"
@@ -781,14 +842,15 @@
         self.end_dt = dt
 
         # 当有新的开仓 event 发生，更新 last_event
         if op in [Operate.LO, Operate.SO]:
             self.last_event = {'dt': dt, 'bid': bid, 'price': price, 'op': op, 'op_desc': op_desc}
 
         def __create_operate(_op, _op_desc):
+            self.pos_changed = True
             return {'symbol': self.symbol, 'dt': dt, 'bid': bid, 'price': price,
                     'op': _op, 'op_desc': _op_desc, 'pos': self.pos}
 
         # 更新仓位
         if op == Operate.LO:
             if self.pos != 1 and (not self.last_lo_dt or (dt - self.last_lo_dt).total_seconds() > self.interval):
                 # 与前一次开多间隔时间大于 interval，直接开多
@@ -847,9 +909,8 @@
                 self.operates.append(__create_operate(Operate.SE, f"平空@{self.stop_loss}BP止损"))
 
             # 空头超时
             if bid - self.last_event['bid'] > self.timeout:
                 self.pos = 0
                 self.operates.append(__create_operate(Operate.SE, f"平空@{self.timeout}K超时"))
 
-        self.holds.append({"dt": self.end_dt, 'pos': self.pos})
-
+        self.holds.append({"dt": self.end_dt, 'pos': self.pos, 'price': price, 'bid': bid})
```

### Comparing `czsc-0.9.8/czsc/sensors/plates.py` & `czsc-0.9.9/czsc/sensors/plates.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/sensors/stocks.py` & `czsc-0.9.9/czsc/sensors/stocks.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/sensors/utils.py` & `czsc-0.9.9/czsc/sensors/utils.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/signals/__init__.py` & `czsc-0.9.9/czsc/signals/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -17,14 +17,16 @@
 from czsc.signals.cxt import (
     cxt_fx_power_V221107,
     cxt_first_buy_V221126,
     cxt_first_sell_V221126,
     cxt_bi_break_V221126,
     cxt_sub_b3_V221212,
     cxt_zhong_shu_gong_zhen_V221221,
+    cxt_bi_end_V230222,
+    cxt_bi_end_V230224,
 )
 
 
 from czsc.signals.byi import (
     byi_symmetry_zs_V221107,
 )
 
@@ -50,14 +52,15 @@
     bar_accelerate_V221110,
     bar_accelerate_V221118,
     bar_fang_liang_break_V221216,
     bar_fake_break_V230204,
     bar_single_V230214,
     bar_amount_acc_V230214,
     bar_big_solid_V230215,
+    bar_vol_bs1_V230224,
 )
 
 from czsc.signals.jcc import (
     jcc_san_xing_xian_V221023,
     jcc_ten_mo_V221028,
     jcc_bai_san_bin_V221030,
     jcc_san_fa_V20221115,
```

### Comparing `czsc-0.9.8/czsc/signals/bar.py` & `czsc-0.9.9/czsc/signals/bar.py`

 * *Files 3% similar despite different names*

```diff
@@ -668,8 +668,43 @@
     max_solid_mid = min(max_solid_bar.open, max_solid_bar.close) + 0.5 * max_solid_bar.solid
 
     v1 = '看多' if c.bars_raw[-1].close > max_solid_mid else '看空'
     v2 = '大阳' if max_solid_bar.close > max_solid_bar.open else '大阴'
     return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1, v2=v2)
 
 
+def bar_vol_bs1_V230224(c: CZSC, di: int = 1, n: int = 20, **kwargs):
+    """量价配合的高低点判断
 
+    **信号逻辑：**
+
+    1. 高点看空：窗口内最近一根K线上影大于下影的两倍，同时最高价和成交量同时创新高
+    2. 反之，低点看多
+
+    **信号列表：**
+
+    - Signal('15分钟_D2N34量价_BS1辅助_看多_任意_任意_0')
+    - Signal('15分钟_D2N34量价_BS1辅助_看空_任意_任意_0')
+
+    :param c: CZSC 对象
+    :param di: 倒数第i根K线
+    :param n: 窗口大小
+    :return: 信号字典
+    """
+    k1, k2, k3 = f"{c.freq.value}_D{di}N{n}量价_BS1辅助".split('_')
+    _bars = get_sub_elements(c.bars_raw, di=di, n=n)
+    mean_vol = np.mean([x.amount for x in _bars])
+
+    short_c1 = _bars[-1].high == max([x.high for x in _bars]) and _bars[-1].upper > 2 * _bars[-1].lower > 0
+    short_c2 = _bars[-1].amount > mean_vol * 3
+
+    long_c1 = _bars[-1].low == min([x.low for x in _bars]) and _bars[-1].lower > 2 * _bars[-1].upper > 0
+    long_c2 = _bars[-1].amount < mean_vol * 0.7
+
+    if short_c1 and short_c2:
+        v1 = '看空'
+    elif long_c1 and long_c2:
+        v1 = '看多'
+    else:
+        v1 = '其他'
+
+    return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1)
```

### Comparing `czsc-0.9.8/czsc/signals/bxt.py` & `czsc-0.9.9/czsc/signals/bxt.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/signals/byi.py` & `czsc-0.9.9/czsc/signals/byi.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/signals/coo.py` & `czsc-0.9.9/czsc/signals/coo.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/signals/cxt.py` & `czsc-0.9.9/czsc/signals/cxt.py`

 * *Files 15% similar despite different names*

```diff
@@ -4,17 +4,17 @@
 email: zeng_bin8888@163.com
 create_dt: 2022/11/7 19:29
 describe:  cxt 代表 CZSC 形态信号
 """
 import numpy as np
 from loguru import logger
 from typing import List
-from czsc import CZSC, Signal
+from czsc import CZSC
 from czsc.traders.base import CzscSignals
-from czsc.objects import FX, BI, Direction, ZS
+from czsc.objects import FX, BI, Direction, ZS, Mark
 from czsc.utils import get_sub_elements, create_single_signal
 from collections import OrderedDict
 
 
 def cxt_fx_power_V221107(c: CZSC, di: int = 1) -> OrderedDict:
     """倒数第di个分型的强弱
 
@@ -327,7 +327,125 @@
 
         if small_zs.gg < big_zs.zz and min_freq.bi_list[-1].direction == Direction.Up:
             v1 = "看空"
 
     return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1)
 
 
+def cxt_bi_end_V230222(c: CZSC, **kwargs) -> OrderedDict:
+    """当前是最后笔的第几次新低底分型或新高顶分型，用于笔结束辅助
+
+    **信号逻辑：**
+
+    1. 取最后笔及未成笔的分型，
+    2. 当前如果是顶分型，则看当前顶分型是否新高，是第几个新高
+    2. 当前如果是底分型，则看当前底分型是否新低，是第几个新低
+
+    **信号列表：**
+
+    - Signal('15分钟_D1MO3_结束辅助_新低_第1次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第2次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第1次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第2次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第3次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第4次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第3次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第4次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第5次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第5次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第6次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第6次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新高_第7次_任意_0')
+    - Signal('15分钟_D1MO3_结束辅助_新低_第7次_任意_0')
+
+    :param c: CZSC对象
+    :param kwargs:
+    :return: 信号识别结果
+    """
+    max_overlap = int(kwargs.get('max_overlap', 3))
+    k1, k2, k3 = f"{c.freq.value}_D1MO{max_overlap}_结束辅助".split('_')
+    v1 = '其他'
+    v2 = '其他'
+
+    if not c.ubi_fxs:
+        return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1, v2=v2)
+
+    # 为了只取最后一笔以来的分型，没有用底层fx_list
+    fxs = []
+    if c.bi_list:
+        fxs.extend(c.bi_list[-1].fxs[1:])
+    ubi_fxs = c.ubi_fxs
+    for x in ubi_fxs:
+        if not fxs or x.dt > fxs[-1].dt:
+            fxs.append(x)
+
+    # 出分型那刻出信号，或者分型和最后一根bar相差 max_overlap 根K线时间内
+    if (fxs[-1].elements[-1].dt == c.bars_ubi[-1].dt) or (c.bars_raw[-1].id - fxs[-1].raw_bars[-1].id <= max_overlap):
+        if fxs[-1].mark == Mark.G:
+            up = [x for x in fxs if x.mark == Mark.G]
+            high_max = float('-inf')
+            cnt = 0
+            for fx in up:
+                if fx.high > high_max:
+                    cnt += 1
+                    high_max = fx.high
+            if fxs[-1].high == high_max:
+                v1 = '新高'
+                v2 = cnt
+
+        else:
+            down = [x for x in fxs if x.mark == Mark.D]
+            low_min = float('inf')
+            cnt = 0
+            for fx in down:
+                if fx.low < low_min:
+                    cnt += 1
+                    low_min = fx.low
+            if fxs[-1].low == low_min:
+                v1 = '新低'
+                v2 = cnt
+
+    return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1, v2=f"第{v2}次")
+
+
+def cxt_bi_end_V230224(c: CZSC, **kwargs):
+    """量价配合的笔结束辅助
+
+    **信号逻辑：**
+
+    1. 向下笔结束：fx_b 内最低的那根K线下影大于上影的两倍，同时fx_b内的平均成交量小于当前笔的平均成交量的0.618
+    2. 向上笔结束：fx_b 内最高的那根K线上影大于下影的两倍，同时fx_b内的平均成交量大于当前笔的平均成交量的2倍
+
+    **信号列表：**
+
+    - Signal('15分钟_D1MO3_笔结束V230224_看多_任意_任意_0')
+    - Signal('15分钟_D1MO3_笔结束V230224_看空_任意_任意_0')
+
+    :param c: CZSC 对象
+    :return: 信号字典
+    """
+    max_overlap = int(kwargs.get('max_overlap', 3))
+    k1, k2, k3 = f"{c.freq.value}_D1MO{max_overlap}_笔结束V230224".split('_')
+    v1 = '其他'
+    if len(c.bi_list) <= 3:
+        return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1)
+
+    last_bi = c.bi_list[-1]
+    bi_bars = last_bi.raw_bars
+    bi_vol_mean = np.mean([x.vol for x in bi_bars])
+    fx_bars = last_bi.fx_b.raw_bars
+    fx_vol_mean = np.mean([x.vol for x in fx_bars])
+
+    bar1 = fx_bars[np.argmin([x.low for x in fx_bars])]
+    bar2 = fx_bars[np.argmax([x.high for x in fx_bars])]
+
+    if bar1.upper > bar1.lower * 2 and fx_vol_mean > bi_vol_mean * 2:
+        v1 = '看空'
+    elif 2 * bar2.upper < bar2.lower and fx_vol_mean < bi_vol_mean * 0.618:
+        v1 = '看多'
+    else:
+        v1 = '其他'
+
+    return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1)
+
+
+
```

### Comparing `czsc-0.9.8/czsc/signals/jcc.py` & `czsc-0.9.9/czsc/signals/jcc.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/signals/tas.py` & `czsc-0.9.9/czsc/signals/tas.py`

 * *Files 0% similar despite different names*

```diff
@@ -360,15 +360,15 @@
         b1_con2 = len(dn) > 3 and dn[-2]['慢线'] < 0 and dn[-3]['慢线'] < 0
         b1_con3 = len(macd) > 10 and macd[-1] > macd[-2]
         if low_n < low_m and (b1_con1a or b1_con1b) and b1_con2 and b1_con3:
             v1 = "一买"
 
         s1_con1a = len(cross) > 3 and cross[-1]['类型'] == '金叉' and cross[-1]['慢线'] > 0
         s1_con1b = len(cross) > 3 and cross[-1]['类型'] == '死叉' and up[-1]['慢线'] > 0
-        s1_con2 = len(dn) > 3 and up[-2]['慢线'] > 0 and up[-3]['慢线'] > 0
+        s1_con2 = len(up) > 3 and up[-2]['慢线'] > 0 and up[-3]['慢线'] > 0
         s1_con3 = len(macd) > 10 and macd[-1] < macd[-2]
         if high_n > high_m and (s1_con1a or s1_con1b) and s1_con2 and s1_con3:
             v1 = "一卖"
 
         v2 = cross[-1]['类型']
 
     return create_single_signal(k1=k1, k2=k2, k3=k3, v1=v1, v2=v2)
```

### Comparing `czsc-0.9.8/czsc/signals/vol.py` & `czsc-0.9.9/czsc/signals/vol.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/traders/base.py` & `czsc-0.9.9/czsc/traders/base.py`

 * *Files 4% similar despite different names*

```diff
@@ -133,14 +133,15 @@
     :param get_signals: 信号计算函数
     :param freqs: K 线周期序列，不需要填写基础周期
     :param sdt: 信号计算开始时间
     :param init_n: 用于 BarGenerator 初始化的基础周期K线数量
     :param df: 是否返回 df 格式的信号计算结果，默认 False
     :return: 信号计算结果
     """
+    freqs = [freq for freq in freqs if freq != bars[0].freq.value]
     sdt = pd.to_datetime(sdt)
     bars_left = [x for x in bars if x.dt < sdt]
     if len(bars_left) <= init_n:
         bars_left = bars[:init_n]
         bars_right = bars[init_n:]
     else:
         bars_right = [x for x in bars if x.dt >= sdt]
@@ -222,17 +223,32 @@
                 ct.take_snapshot(file_html)
                 last_dt[signal.key] = bar.dt
 
 
 class CzscTrader(CzscSignals):
     """缠中说禅技术分析理论之多级别联立交易决策类（支持多策略独立执行）"""
 
-    def __init__(self, bg: BarGenerator = None, get_signals: Callable = None, positions: List[Position] = None):
+    def __init__(self, bg: BarGenerator = None, get_signals: Callable = None,
+                 positions: List[Position] = None, ensemble_method: Union[AnyStr, Callable] = "mean"):
+        """
+
+        :param bg: bar generator 对象
+        :param get_signals: 信号计算函数，输入是 CzscSignals 对象，输出是信号字典
+        :param ensemble_method: 多个仓位集成一个仓位的方法，可选值 mean, vote, max；也可以传入一个回调函数
+
+            假设有三个仓位对象，当前仓位分别是 1, 1, -1
+            mean - 平均仓位，pos = np.mean([1, 1, -1]) = 0.33
+            vote - 投票表决，pos = 1
+            max  - 取最大，pos = 1
+
+            对于传入回调函数的情况，输入是 self.positions
+        """
         super().__init__(bg, get_signals=get_signals)
         self.positions = positions
+        self.__ensemble_method = ensemble_method
 
     def update(self, bar: RawBar) -> None:
         """输入基础周期已完成K线，更新信号，更新仓位
 
         :param bar: 基础周期已完成K线
         :return: None
         """
@@ -260,15 +276,25 @@
         """输入基础周期已完成K线，更新信号，更新仓位
 
         :param bar: 基础周期已完成K线
         :return: None
         """
         self.update(bar)
 
-    def get_ensemble_pos(self, method: Union[AnyStr, Callable] = "mean"):
+    @property
+    def pos_changed(self) -> bool:
+        """判断仓位是否发生变化
+
+        :return: True/False
+        """
+        if not self.positions:
+            return False
+        return any([position.pos_changed for position in self.positions])
+
+    def get_ensemble_pos(self, method: Union[AnyStr, Callable] = None) -> float:
         """获取多个仓位的集成仓位
 
         :param method: 多个仓位集成一个仓位的方法，可选值 mean, vote, max；也可以传入一个回调函数
 
             假设有三个仓位对象，当前仓位分别是 1, 1, -1
             mean - 平均仓位，pos = np.mean([1, 1, -1]) = 0.33
             vote - 投票表决，pos = 1
@@ -277,14 +303,15 @@
             对于传入回调函数的情况，输入是 self.positions
 
         :return: pos, 集成仓位
         """
         if not self.positions:
             return 0
 
+        method = self.__ensemble_method if not method else method
         if isinstance(method, str):
             method = method.lower()
             pos_seq = [x.pos for x in self.positions]
 
             if method == 'mean':
                 pos = np.mean(pos_seq)
             elif method == 'vote':
```

### Comparing `czsc-0.9.8/czsc/traders/performance.py` & `czsc-0.9.9/czsc/traders/performance.py`

 * *Files 2% similar despite different names*

```diff
@@ -174,18 +174,18 @@
             "结束时间": df_pairs['平仓时间'].max(),
 
             "交易标的数量": df_pairs['标的代码'].nunique(),
             "总体交易次数": len(df_pairs),
             "平均持仓天数": round(df_pairs['持仓天数'].mean(), 2),
             "平均持仓K线数": round(df_pairs['持仓K线数'].mean(), 2),
 
-            "平均单笔收益": round(df_pairs['盈亏比例'].mean() * 10000, 2),
-            "单笔收益标准差": round(df_pairs['盈亏比例'].std() * 10000, 2),
-            "最大单笔收益": round(df_pairs['盈亏比例'].max() * 10000, 2),
-            "最小单笔收益": round(df_pairs['盈亏比例'].min() * 10000, 2),
+            "平均单笔收益": round(df_pairs['盈亏比例'].mean(), 4),
+            "单笔收益标准差": round(df_pairs['盈亏比例'].std(), 4),
+            "最大单笔收益": round(df_pairs['盈亏比例'].max(), 4),
+            "最小单笔收益": round(df_pairs['盈亏比例'].min(), 4),
 
             "交易胜率": win_pct,
             "单笔盈亏比": single_gain_loss_rate,
             "累计盈亏比": total_gain_loss_rate,
             "交易得分": round(total_gain_loss_rate * win_pct, 4),
             "赢面": round(single_gain_loss_rate * win_pct - (1 - win_pct), 4),
             "盈亏平衡点": round(cal_break_even_point(df_pairs['盈亏比例'].to_list()), 4),
```

### Comparing `czsc-0.9.8/czsc/utils/__init__.py` & `czsc-0.9.9/czsc/utils/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -9,14 +9,15 @@
 from .echarts_plot import kline_pro, heat_map
 from .word_writer import WordWriter
 from .corr import nmi_matrix, single_linear
 from .bar_generator import BarGenerator, freq_end_time, resample_bars
 from .io import dill_dump, dill_load, read_json, save_json
 from .sig import check_pressure_support, check_gap_info, is_bis_down, is_bis_up, get_sub_elements
 from .sig import same_dir_counts, fast_slow_cross, count_last_same, create_single_signal
+from .plotly_plot import KlineChart
 
 
 def x_round(x: [float, int], digit=4):
     """用去尾法截断小数
 
     :param x: 数字
     :param digit: 保留小数位数
```

### Comparing `czsc-0.9.8/czsc/utils/bar_generator.py` & `czsc-0.9.9/czsc/utils/bar_generator.py`

 * *Files 1% similar despite different names*

```diff
@@ -98,23 +98,21 @@
     :param target_freq: 目标周期
     :param raw_bars: 是否将转换后的K线序列转换为RawBar对象
     :return: 转换后的K线序列
     """
     if not isinstance(target_freq, Freq):
         target_freq = Freq(target_freq)
 
-    k_cols = ['symbol', 'dt', 'open', 'close', 'high', 'low', 'vol', 'amount']
-    df = df[k_cols]
     df['freq_edt'] = df['dt'].apply(lambda x: freq_end_time(x, target_freq))
     dfk1 = df.groupby('freq_edt').agg(
         {'symbol': 'first', 'dt': 'last', 'open': 'first', 'close': 'last', 'high': 'max',
          'low': 'min', 'vol': 'sum', 'amount': 'sum', 'freq_edt': 'last'})
     dfk1.reset_index(drop=True, inplace=True)
     dfk1['dt'] = dfk1['freq_edt']
-    dfk1 = dfk1[k_cols]
+    dfk1 = dfk1[['symbol', 'dt', 'open', 'close', 'high', 'low', 'vol', 'amount']]
 
     if raw_bars:
         _bars = []
         for i, row in enumerate(dfk1.to_dict("records"), 1):
             row.update({'id': i, 'freq': target_freq})
             _bars.append(RawBar(**row))
```

### Comparing `czsc-0.9.8/czsc/utils/cache.py` & `czsc-0.9.9/czsc/utils/cache.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/corr.py` & `czsc-0.9.9/czsc/utils/corr.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/echarts_plot.py` & `czsc-0.9.9/czsc/utils/echarts_plot.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/io.py` & `czsc-0.9.9/czsc/utils/io.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/qywx.py` & `czsc-0.9.9/czsc/utils/qywx.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/sig.py` & `czsc-0.9.9/czsc/utils/sig.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/ta.py` & `czsc-0.9.9/czsc/utils/ta.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/ta1.py` & `czsc-0.9.9/czsc/utils/ta1.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc/utils/word_writer.py` & `czsc-0.9.9/czsc/utils/word_writer.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/czsc.egg-info/PKG-INFO` & `czsc-0.9.9/czsc.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: czsc
-Version: 0.9.8
+Version: 0.9.9
 Summary: 缠中说禅技术分析工具
 Home-page: https://github.com/zengbin93/czsc
 Author: zengbin93
 Author-email: zeng_bin8888@163.com
 License: Apache Software License
 Description: # czsc - 缠中说禅技术分析工具
```

### Comparing `czsc-0.9.8/czsc.egg-info/SOURCES.txt` & `czsc-0.9.9/czsc.egg-info/SOURCES.txt`

 * *Files 25% similar despite different names*

```diff
@@ -16,27 +16,25 @@
 czsc.egg-info/entry_points.txt
 czsc.egg-info/requires.txt
 czsc.egg-info/top_level.txt
 czsc/ai/__init__.py
 czsc/ai/sk.py
 czsc/ai/utils.py
 czsc/connectors/__init__.py
+czsc/connectors/gm_connector.py
 czsc/connectors/qmt_connector.py
 czsc/data/__init__.py
 czsc/data/base.py
 czsc/data/jq.py
 czsc/data/ts.py
 czsc/data/ts_cache.py
 czsc/fsa/__init__.py
 czsc/fsa/base.py
 czsc/fsa/im.py
 czsc/fsa/spreed_sheets.py
-czsc/gms/__init__.py
-czsc/gms/gm_base.py
-czsc/gms/gm_stocks.py
 czsc/sensors/__init__.py
 czsc/sensors/plates.py
 czsc/sensors/stocks.py
 czsc/sensors/utils.py
 czsc/signals/__init__.py
 czsc/signals/bar.py
 czsc/signals/bxt.py
@@ -51,14 +49,15 @@
 czsc/traders/performance.py
 czsc/utils/__init__.py
 czsc/utils/bar_generator.py
 czsc/utils/cache.py
 czsc/utils/corr.py
 czsc/utils/echarts_plot.py
 czsc/utils/io.py
+czsc/utils/plotly_plot.py
 czsc/utils/qywx.py
 czsc/utils/sig.py
 czsc/utils/ta.py
 czsc/utils/ta1.py
 czsc/utils/word_writer.py
 examples/dropit/__init__.py
 examples/dropit/gm_backtest.py
@@ -67,14 +66,17 @@
 examples/dropit/jq_check_point.py
 examples/dropit/quick_start.py
 examples/dropit/ts_continue_simulator.py
 examples/dropit/ts_dummy_trader.py
 examples/dropit/ts_trade_replay.py
 examples/signals_dev/__init__.py
 examples/signals_dev/bar_big_solid.py
+examples/signals_dev/bar_vol_bs1_V230224.py
+examples/signals_dev/cxt_bi_end_V230222.py
+examples/signals_dev/cxt_bi_end_V230224.py
 examples/signals_dev/tas_first_bs_V230217.py
 examples/strategies/__init__.py
 examples/strategies/cat_sma.py
 examples/strategies/check_signal.py
 examples/strategies/czsc_strategy_sma5.py
 examples/strategies/tcs_sma.py
 examples/test_offline/__init__.py
@@ -82,11 +84,13 @@
 examples/test_offline/test_ts_cache.py
 test/test_ai_utils.py
 test/test_analyze.py
 test/test_bar_generator.py
 test/test_data.py
 test/test_objects.py
 test/test_plot.py
+test/test_plotly_plot.py
 test/test_sensors.py
+test/test_strategy.py
 test/test_trader_base.py
 test/test_utils.py
 test/test_word_writer.py
```

### Comparing `czsc-0.9.8/examples/dropit/gm_backtest.py` & `czsc-0.9.9/examples/dropit/gm_backtest.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/gm_check_point.py` & `czsc-0.9.9/examples/dropit/gm_check_point.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/gm_realtime.py` & `czsc-0.9.9/examples/dropit/gm_realtime.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/jq_check_point.py` & `czsc-0.9.9/examples/dropit/jq_check_point.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/quick_start.py` & `czsc-0.9.9/examples/dropit/quick_start.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/ts_continue_simulator.py` & `czsc-0.9.9/examples/dropit/ts_continue_simulator.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/ts_dummy_trader.py` & `czsc-0.9.9/examples/dropit/ts_dummy_trader.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/dropit/ts_trade_replay.py` & `czsc-0.9.9/examples/dropit/ts_trade_replay.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/signals_dev/bar_big_solid.py` & `czsc-0.9.9/examples/signals_dev/bar_big_solid.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/signals_dev/tas_first_bs_V230217.py` & `czsc-0.9.9/examples/signals_dev/tas_first_bs_V230217.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/strategies/cat_sma.py` & `czsc-0.9.9/examples/strategies/cat_sma.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/strategies/check_signal.py` & `czsc-0.9.9/examples/strategies/check_signal.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/strategies/czsc_strategy_sma5.py` & `czsc-0.9.9/examples/strategies/czsc_strategy_sma5.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/strategies/tcs_sma.py` & `czsc-0.9.9/examples/strategies/tcs_sma.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/test_offline/test_fsa.py` & `czsc-0.9.9/examples/test_offline/test_fsa.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/examples/test_offline/test_ts_cache.py` & `czsc-0.9.9/examples/test_offline/test_ts_cache.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/setup.py` & `czsc-0.9.9/setup.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_ai_utils.py` & `czsc-0.9.9/test/test_ai_utils.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_analyze.py` & `czsc-0.9.9/test/test_analyze.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_bar_generator.py` & `czsc-0.9.9/test/test_bar_generator.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_data.py` & `czsc-0.9.9/test/test_data.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_objects.py` & `czsc-0.9.9/test/test_objects.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_plot.py` & `czsc-0.9.9/test/test_plot.py`

 * *Files identical despite different names*

### Comparing `czsc-0.9.8/test/test_trader_base.py` & `czsc-0.9.9/test/test_trader_base.py`

 * *Files 2% similar despite different names*

```diff
@@ -219,15 +219,20 @@
         return pos
 
     # 通过 update 执行
     ct = CzscTrader(deepcopy(bg), get_signals=__get_signals,
                     positions=[__create_sma5_pos(), __create_sma10_pos(), __create_sma20_pos()])
     for bar in bars_right:
         ct.update(bar)
-        print(f"{bar.dt}: pos_seq = {[x.pos for x in ct.positions]}mean_pos = {ct.get_ensemble_pos('mean')}; vote_pos = {ct.get_ensemble_pos('vote')}; max_pos = {ct.get_ensemble_pos('max')}")
+        for _pos in ct.positions:
+            if _pos.pos_changed:
+                assert _pos.operates[-1]['dt'] == _pos.end_dt
+                print(_pos.name, _pos.operates[-1], _pos.end_dt, _pos.pos)
+                assert ct.pos_changed
+        # print(f"{bar.dt}: pos_seq = {[x.pos for x in ct.positions]}mean_pos = {ct.get_ensemble_pos('mean')}; vote_pos = {ct.get_ensemble_pos('vote')}; max_pos = {ct.get_ensemble_pos('max')}")
 
     assert list(ct.positions[0].dump(False).keys()) == ['symbol', 'name', 'opens', 'exits', 'interval', 'timeout', 'stop_loss', 'T0']
     assert list(ct.positions[0].dump(True).keys()) == ['symbol', 'name', 'opens', 'exits', 'interval', 'timeout', 'stop_loss', 'T0', 'pairs', 'holds']
     assert [x.pos for x in ct.positions] == [0, -1, 0]
 
     # 测试自定义仓位集成
     def _weighted_ensemble(positions: List[Position]):
```

### Comparing `czsc-0.9.8/test/test_word_writer.py` & `czsc-0.9.9/test/test_word_writer.py`

 * *Files identical despite different names*

