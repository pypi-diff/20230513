# Comparing `tmp/OctoBot-Pro-0.0.8.tar.gz` & `tmp/OctoBot-Pro-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OctoBot-Pro-0.0.8.tar", last modified: Fri Mar 24 13:26:04 2023, max compression
+gzip compressed data, was "OctoBot-Pro-0.0.9.tar", last modified: Tue May  2 13:53:27 2023, max compression
```

## Comparing `OctoBot-Pro-0.0.8.tar` & `OctoBot-Pro-0.0.9.tar`

### file list

```diff
@@ -1,66 +1,66 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)    35148 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      189 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/MANIFEST.in
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4669 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       65 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-03-24 13:26:04.000000 OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4669 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/octobot_pro/
--rw-r--r--   0 runner    (1001) docker     (123)     2290 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/octobot_pro/api/
--rw-r--r--   0 runner    (1001) docker     (123)      908 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/api/data_fetching.py
--rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/api/execution.py
--rw-r--r--   0 runner    (1001) docker     (123)     1157 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/api/ploting.py
--rw-r--r--   0 runner    (1001) docker     (123)     2460 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/octobot_pro/config/
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/config/config_mock.json
--rw-r--r--   0 runner    (1001) docker     (123)      697 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/config/logging_config.ini
--rw-r--r--   0 runner    (1001) docker     (123)      844 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/constants.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/octobot_pro/internal/
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/internal/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1429 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/internal/backtester_trading_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/internal/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/internal/octobot_mocks.py
--rw-r--r--   0 runner    (1001) docker     (123)     3608 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/internal/runners.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/octobot_pro/model/
--rw-r--r--   0 runner    (1001) docker     (123)      874 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6440 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/model/backtest_plot.py
--rw-r--r--   0 runner    (1001) docker     (123)     2592 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/model/backtest_result.py
--rw-r--r--   0 runner    (1001) docker     (123)      827 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/model/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/model/strategy.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/octobot_pro/resources/
--rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/css/
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/css/style.css
--rw-r--r--   0 runner    (1001) docker     (123)     1114 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/css/w2ui_template.css
--rw-r--r--   0 runner    (1001) docker     (123)     1890 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/default_report_template.html
--rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/header.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/common.js
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/data.js
--rw-r--r--   0 runner    (1001) docker     (123)     5875 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/graphs.js
--rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/tables.js
--rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/texts.js
--rw-r--r--   0 runner    (1001) docker     (123)      892 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/octobot_pro/resources/reports/scripts.html
--rw-r--r--   0 runner    (1001) docker     (123)      212 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.208446 OctoBot-Pro-0.0.8/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/tests/api/
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2999 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/api/test_data_fetching.py
--rw-r--r--   0 runner    (1001) docker     (123)     2031 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/api/test_execution.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/tests/functionnal/
--rw-r--r--   0 runner    (1001) docker     (123)     1331 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/functionnal/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-24 13:26:04.212446 OctoBot-Pro-0.0.8/tests/functionnal/example_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/functionnal/example_scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4865 2023-03-24 13:25:14.000000 OctoBot-Pro-0.0.8/tests/functionnal/example_scripts/test_precomputed_vs_iteration_rsi.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)      815 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)    35148 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      189 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/MANIFEST.in
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.575562 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4669 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-02 13:53:27.000000 OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4669 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.575562 OctoBot-Pro-0.0.9/octobot_pro/
+-rw-r--r--   0 runner    (1001) docker     (123)     2290 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/api/
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/api/data_fetching.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/api/execution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1157 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/api/ploting.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2460 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/config/
+-rw-r--r--   0 runner    (1001) docker     (123)      785 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/config/config_mock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      697 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/config/logging_config.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      844 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/constants.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/internal/
+-rw-r--r--   0 runner    (1001) docker     (123)      785 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/internal/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1429 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/internal/backtester_trading_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/internal/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/internal/octobot_mocks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3608 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/internal/runners.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/model/
+-rw-r--r--   0 runner    (1001) docker     (123)      874 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6440 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/model/backtest_plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2592 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/model/backtest_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)      827 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/model/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)      867 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/model/strategy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/resources/
+-rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/css/
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/css/style.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1114 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/css/w2ui_template.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1890 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/default_report_template.html
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/header.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.579562 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/common.js
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/data.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5875 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/graphs.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/tables.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/texts.js
+-rw-r--r--   0 runner    (1001) docker     (123)      892 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/octobot_pro/resources/reports/scripts.html
+-rw-r--r--   0 runner    (1001) docker     (123)      212 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.575562 OctoBot-Pro-0.0.9/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/tests/api/
+-rw-r--r--   0 runner    (1001) docker     (123)      785 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2999 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/api/test_data_fetching.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2031 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/api/test_execution.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/tests/functionnal/
+-rw-r--r--   0 runner    (1001) docker     (123)     1331 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/functionnal/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 13:53:27.583562 OctoBot-Pro-0.0.9/tests/functionnal/example_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)      785 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/functionnal/example_scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4865 2023-05-02 13:51:43.000000 OctoBot-Pro-0.0.9/tests/functionnal/example_scripts/test_precomputed_vs_iteration_rsi.py
```

### Comparing `OctoBot-Pro-0.0.8/CHANGELOG.md` & `OctoBot-Pro-0.0.9/CHANGELOG.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,13 +1,17 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
 and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
 
+## [0.0.9] - 2022-05-02
+### Update
+- Update to OctoBot 0.4.49
+
 ## [0.0.8] - 2022-03-24
 ### Update
 - Update to OctoBot 0.4.45
 
 ## [0.0.7] - 2022-03-07
 ### Update
 - Update to OctoBot 0.4.41
```

### Comparing `OctoBot-Pro-0.0.8/LICENSE` & `OctoBot-Pro-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/PKG-INFO` & `OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Pro
-Version: 0.0.8
+Version: 0.0.9
 Summary: Backtesting framework of the OctoBot Ecosystem
 Home-page: https://github.com/Drakkar-Software/OctoBot-Pro
 Author: Drakkar-Software
 Author-email: drakkar-software@protonmail.com
 License: GPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -13,15 +13,15 @@
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-# Octobot-Pro [0.0.8](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
+# Octobot-Pro [0.0.9](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
 [![PyPI](https://img.shields.io/pypi/v/octobot-pro.svg?logo=pypi)](https://pypi.python.org/pypi/octobot-pro/)
 [![Downloads](https://static.pepy.tech/badge/octobot-pro/month)](https://pepy.tech/project/octobot-pro)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Pro/workflows/OctoBot-Pro-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Pro/actions)
 
 ## Octobot-Pro Community
 [![Telegram Chat](https://img.shields.io/badge/telegram-chat-green.svg?logo=telegram&label=Telegram)](https://octobot.click/readme-telegram-octobot-pro)
 [![Discord](https://img.shields.io/discord/530629985661222912.svg?logo=discord&label=Discord)](https://octobot.click/gh-discord-octobot-pro)
```

### Comparing `OctoBot-Pro-0.0.8/OctoBot_Pro.egg-info/SOURCES.txt` & `OctoBot-Pro-0.0.9/OctoBot_Pro.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/PKG-INFO` & `OctoBot-Pro-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Pro
-Version: 0.0.8
+Version: 0.0.9
 Summary: Backtesting framework of the OctoBot Ecosystem
 Home-page: https://github.com/Drakkar-Software/OctoBot-Pro
 Author: Drakkar-Software
 Author-email: drakkar-software@protonmail.com
 License: GPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -13,15 +13,15 @@
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-# Octobot-Pro [0.0.8](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
+# Octobot-Pro [0.0.9](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
 [![PyPI](https://img.shields.io/pypi/v/octobot-pro.svg?logo=pypi)](https://pypi.python.org/pypi/octobot-pro/)
 [![Downloads](https://static.pepy.tech/badge/octobot-pro/month)](https://pepy.tech/project/octobot-pro)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Pro/workflows/OctoBot-Pro-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Pro/actions)
 
 ## Octobot-Pro Community
 [![Telegram Chat](https://img.shields.io/badge/telegram-chat-green.svg?logo=telegram&label=Telegram)](https://octobot.click/readme-telegram-octobot-pro)
 [![Discord](https://img.shields.io/discord/530629985661222912.svg?logo=discord&label=Discord)](https://octobot.click/gh-discord-octobot-pro)
```

### Comparing `OctoBot-Pro-0.0.8/README.md` & `OctoBot-Pro-0.0.9/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Octobot-Pro [0.0.8](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
+# Octobot-Pro [0.0.9](https://github.com/Drakkar-Software/OctoBot-Pro/tree/master/CHANGELOG.md)
 [![PyPI](https://img.shields.io/pypi/v/octobot-pro.svg?logo=pypi)](https://pypi.python.org/pypi/octobot-pro/)
 [![Downloads](https://static.pepy.tech/badge/octobot-pro/month)](https://pepy.tech/project/octobot-pro)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Pro/workflows/OctoBot-Pro-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Pro/actions)
 
 ## Octobot-Pro Community
 [![Telegram Chat](https://img.shields.io/badge/telegram-chat-green.svg?logo=telegram&label=Telegram)](https://octobot.click/readme-telegram-octobot-pro)
 [![Discord](https://img.shields.io/discord/530629985661222912.svg?logo=discord&label=Discord)](https://octobot.click/gh-discord-octobot-pro)
```

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/__init__.py` & `OctoBot-Pro-0.0.9/octobot_pro/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 #  General Public License for more details.
 #
 #  You should have received a copy of the GNU General Public
 #  License along with OctoBot-Pro. If not, see <https://www.gnu.org/licenses/>.
 
 PROJECT_NAME = "OctoBot-Pro"
 AUTHOR = "Drakkar-Software"
-VERSION = "0.0.8"  # major.minor.revision
+VERSION = "0.0.9"  # major.minor.revision
 
 
 def _use_module_local_tentacles():
     import sys
     import os
     import appdirs
     if os.getenv("USE_CUSTOM_TENTACLES", "").lower() == "true":
```

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/api/__init__.py` & `OctoBot-Pro-0.0.9/octobot_pro/api/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/api/data_fetching.py` & `OctoBot-Pro-0.0.9/octobot_pro/api/data_fetching.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/api/execution.py` & `OctoBot-Pro-0.0.9/octobot_pro/api/execution.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/api/ploting.py` & `OctoBot-Pro-0.0.9/octobot_pro/api/ploting.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/cli.py` & `OctoBot-Pro-0.0.9/octobot_pro/cli.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/config/config_mock.json` & `OctoBot-Pro-0.0.9/octobot_pro/config/config_mock.json`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/config/logging_config.ini` & `OctoBot-Pro-0.0.9/octobot_pro/config/logging_config.ini`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/constants.py` & `OctoBot-Pro-0.0.9/octobot_pro/constants.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/internal/__init__.py` & `OctoBot-Pro-0.0.9/octobot_pro/internal/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/internal/backtester_trading_mode.py` & `OctoBot-Pro-0.0.9/octobot_pro/internal/backtester_trading_mode.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/internal/logging_util.py` & `OctoBot-Pro-0.0.9/octobot_pro/internal/logging_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/internal/octobot_mocks.py` & `OctoBot-Pro-0.0.9/octobot_pro/internal/octobot_mocks.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/internal/runners.py` & `OctoBot-Pro-0.0.9/octobot_pro/internal/runners.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/model/__init__.py` & `OctoBot-Pro-0.0.9/octobot_pro/model/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/model/backtest_plot.py` & `OctoBot-Pro-0.0.9/octobot_pro/model/backtest_plot.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/model/backtest_result.py` & `OctoBot-Pro-0.0.9/octobot_pro/model/backtest_result.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/model/errors.py` & `OctoBot-Pro-0.0.9/octobot_pro/model/errors.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/model/strategy.py` & `OctoBot-Pro-0.0.9/octobot_pro/model/strategy.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/__init__.py` & `OctoBot-Pro-0.0.9/octobot_pro/resources/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/css/style.css` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/css/style.css`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/css/w2ui_template.css` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/css/w2ui_template.css`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/default_report_template.html` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/default_report_template.html`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/header.html` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/header.html`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/graphs.js` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/graphs.js`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/tables.js` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/tables.js`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/js/texts.js` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/js/texts.js`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/octobot_pro/resources/reports/scripts.html` & `OctoBot-Pro-0.0.9/octobot_pro/resources/reports/scripts.html`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/setup.py` & `OctoBot-Pro-0.0.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from setuptools import setup
 from distutils.command.install import install
 
 
 # from octobot_pro import PROJECT_NAME, VERSION
 # todo figure out how not to import octobot_pro.__init__.py here
 PROJECT_NAME = "OctoBot-Pro"
-VERSION = "0.0.8"  # major.minor.revision
+VERSION = "0.0.9"  # major.minor.revision
 
 
 def _post_install():
     import octobot_pro.cli
     asyncio.run(octobot_pro.cli.install_all_tentacles(True))
```

### Comparing `OctoBot-Pro-0.0.8/tests/api/__init__.py` & `OctoBot-Pro-0.0.9/tests/api/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/tests/api/test_data_fetching.py` & `OctoBot-Pro-0.0.9/tests/api/test_data_fetching.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/tests/api/test_execution.py` & `OctoBot-Pro-0.0.9/tests/api/test_execution.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/tests/functionnal/__init__.py` & `OctoBot-Pro-0.0.9/tests/functionnal/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/tests/functionnal/example_scripts/__init__.py` & `OctoBot-Pro-0.0.9/tests/functionnal/example_scripts/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Pro-0.0.8/tests/functionnal/example_scripts/test_precomputed_vs_iteration_rsi.py` & `OctoBot-Pro-0.0.9/tests/functionnal/example_scripts/test_precomputed_vs_iteration_rsi.py`

 * *Files identical despite different names*

