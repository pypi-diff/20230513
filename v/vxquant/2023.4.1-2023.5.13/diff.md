# Comparing `tmp/vxquant-2023.4.1.tar.gz` & `tmp/vxquant-2023.5.13.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vxquant-2023.4.1.tar", max compression
+gzip compressed data, was "vxquant-2023.5.13.tar", max compression
```

## Comparing `vxquant-2023.4.1.tar` & `vxquant-2023.5.13.tar`

### file list

```diff
@@ -1,118 +1,101 @@
--rwxr-xr-x   0        0        0     1085 2023-03-06 04:47:42.000000 vxquant-2023.4.1/LICENSE
--rwxr-xr-x   0        0        0     1511 2023-03-06 04:47:42.000000 vxquant-2023.4.1/README.md
--rwxr-xr-x   0        0        0     2125 2023-04-02 14:06:17.873419 vxquant-2023.4.1/pyproject.toml
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/__init__.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/cache.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/collector/__init__.py
--rwxr-xr-x   0        0        0     1070 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/collector/__main__.py
--rwxr-xr-x   0        0        0     1362 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/collector/calendar1111.py
--rwxr-xr-x   0        0        0     5804 2023-03-27 07:01:09.525154 vxquant-2023.4.1/src/vxdataset/collector/dumpall.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/datasource/__init__.py
--rwxr-xr-x   0        0        0     9464 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/datasource/ifind.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/expr/__init__.py
--rwxr-xr-x   0        0        0      855 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/expr/functions.py
--rwxr-xr-x   0        0        0    13098 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/expr/ops.py
--rwxr-xr-x   0        0        0     2707 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/handler.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/loaders/__init__.py
--rwxr-xr-x   0        0        0     3425 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/loaders/base.py
--rwxr-xr-x   0        0        0     1621 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/loaders/csv.py
--rwxr-xr-x   0        0        0     2283 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/loaders/gm.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxdataset/loaders/mongo.py
--rwxr-xr-x   0        0        0        2 2023-03-11 03:14:18.000000 vxquant-2023.4.1/src/vxquant/__init__.py
--rwxr-xr-x   0        0        0     3816 2023-04-05 07:07:18.411840 vxquant-2023.4.1/src/vxquant/__main__.py
--rw-r--r--   0        0        0        0 2023-03-23 13:14:56.105985 vxquant-2023.4.1/src/vxquant/accountdb/__init__.py
--rw-r--r--   0        0        0    13968 2023-04-11 15:59:47.792209 vxquant-2023.4.1/src/vxquant/accountdb/base.py
--rw-r--r--   0        0        0        0 2023-03-23 13:15:20.240915 vxquant-2023.4.1/src/vxquant/accountdb/mongodb.py
--rw-r--r--   0        0        0    17753 2023-04-11 15:59:58.360985 vxquant-2023.4.1/src/vxquant/accountdb/sqlitedb.py
--rwxr-xr-x   0        0        0    28159 2023-04-11 13:44:50.562533 vxquant-2023.4.1/src/vxquant/apis.py
--rwxr-xr-x   0        0        0      839 2023-04-06 07:46:25.980939 vxquant-2023.4.1/src/vxquant/cli/__init__.py
--rwxr-xr-x   0        0        0     2680 2023-04-10 11:55:54.522545 vxquant-2023.4.1/src/vxquant/cli/base.py
--rwxr-xr-x   0        0        0    15084 2023-04-10 16:30:54.912797 vxquant-2023.4.1/src/vxquant/cli/gmagent.py
--rwxr-xr-x   0        0        0     7413 2023-04-10 14:28:30.379107 vxquant-2023.4.1/src/vxquant/cli/qmtagent.py
--rw-r--r--   0        0        0     7123 2023-04-11 13:56:37.619629 vxquant-2023.4.1/src/vxquant/config.py
--rwxr-xr-x   0        0        0     1536 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/exceptions.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/factor/__init__.py
--rwxr-xr-x   0        0        0     7158 2023-04-01 15:46:53.007537 vxquant-2023.4.1/src/vxquant/factor/builder.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/factor/expr/__init__.py
--rwxr-xr-x   0        0        0      855 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/factor/expr/functions.py
--rwxr-xr-x   0        0        0    13833 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/factor/expr/ops.py
--rw-r--r--   0        0        0     7029 2023-04-06 04:54:05.820330 vxquant-2023.4.1/src/vxquant/factor/loader.py
--rwxr-xr-x   0        0        0     4898 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/factor/normalizer.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/model/__init__.py
--rwxr-xr-x   0        0        0    17857 2023-03-07 09:00:59.000000 vxquant-2023.4.1/src/vxquant/model/account.py
--rwxr-xr-x   0        0        0     7035 2023-03-06 14:54:42.000000 vxquant-2023.4.1/src/vxquant/model/contants.py
--rwxr-xr-x   0        0        0    16434 2023-03-15 08:12:42.628178 vxquant-2023.4.1/src/vxquant/model/dbaccount.py
--rwxr-xr-x   0        0        0    14231 2023-04-07 07:20:20.284686 vxquant-2023.4.1/src/vxquant/model/exchange.py
--rwxr-xr-x   0        0        0    11471 2023-03-28 15:27:12.904581 vxquant-2023.4.1/src/vxquant/model/instruments.py
--rwxr-xr-x   0        0        0     2806 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/model/nomalize.py
--rwxr-xr-x   0        0        0    56399 2023-03-15 08:12:42.859226 vxquant-2023.4.1/src/vxquant/model/portfolio.py
--rwxr-xr-x   0        0        0    10767 2023-04-06 01:46:53.205883 vxquant-2023.4.1/src/vxquant/model/preset.py
--rwxr-xr-x   0        0        0       49 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/model/tools/__init__.py
--rwxr-xr-x   0        0        0     7506 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/model/tools/gmData.py
--rwxr-xr-x   0        0        0     9441 2023-03-31 07:55:40.405707 vxquant-2023.4.1/src/vxquant/model/tools/qmtData.py
--rwxr-xr-x   0        0        0     5410 2023-03-15 08:12:42.564695 vxquant-2023.4.1/src/vxquant/model/tools/tdxData.py
--rwxr-xr-x   0        0        0      155 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/model/typehint.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/agent/__init__.py
--rwxr-xr-x   0        0        0     4151 2023-03-07 12:31:01.000000 vxquant-2023.4.1/src/vxquant/modules/agent/__main__.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/agent/mod/__init__.py
--rwxr-xr-x   0        0        0     4837 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/agent.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/broker/__init__.py
--rwxr-xr-x   0        0        0     8563 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/broker/__main__.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/broker/mod/__init__.py
--rwxr-xr-x   0        0        0     1300 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/broker/mod/system.py
--rwxr-xr-x   0        0        0      861 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/broker/utils.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/gateway/__init__.py
--rwxr-xr-x   0        0        0      246 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/gateway/rpc.py
--rwxr-xr-x   0        0        0      440 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/modules/gateway/system.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/providers/__init__.py
--rw-r--r--   0        0        0     4567 2023-03-28 14:06:06.714095 vxquant-2023.4.1/src/vxquant/providers/baostock_api.py
--rwxr-xr-x   0        0        0    17004 2023-04-06 08:34:46.941091 vxquant-2023.4.1/src/vxquant/providers/base.py
--rwxr-xr-x   0        0        0     7023 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/providers/ftp.py
--rwxr-xr-x   0        0        0    13535 2023-04-10 15:06:33.571744 vxquant-2023.4.1/src/vxquant/providers/gmapi.py
--rwxr-xr-x   0        0        0     3010 2023-04-02 14:14:32.259786 vxquant-2023.4.1/src/vxquant/providers/local.py
--rwxr-xr-x   0        0        0    14199 2023-04-10 07:31:13.413999 vxquant-2023.4.1/src/vxquant/providers/miniqmt.py
--rwxr-xr-x   0        0        0     8406 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/providers/mongo.py
--rw-r--r--   0        0        0      131 2023-03-22 13:38:55.253234 vxquant-2023.4.1/src/vxquant/providers/spiders/__init__.py
--rwxr-xr-x   0        0        0     2008 2023-04-05 02:27:07.913696 vxquant-2023.4.1/src/vxquant/providers/spiders/calendar_sse.py
--rwxr-xr-x   0        0        0     4921 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/providers/spiders/hq_tencent.py
--rwxr-xr-x   0        0        0    18580 2023-04-04 05:59:26.900256 vxquant-2023.4.1/src/vxquant/providers/tdx.py
--rwxr-xr-x   0        0        0     7183 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/providers/zeromq.py
--rwxr-xr-x   0        0        0     2438 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/scripts/__init__.py
--rwxr-xr-x   0        0        0     8719 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/scripts/broker.py
--rwxr-xr-x   0        0        0     9813 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/scripts/gmagent.py
--rwxr-xr-x   0        0        0     9953 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/scripts/qmtagent.py
--rwxr-xr-x   0        0        0     4180 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/scripts/worker.py
--rwxr-xr-x   0        0        0        0 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/tdapi/__init__.py
--rwxr-xr-x   0        0        0     4274 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/tdapi/base.py
--rwxr-xr-x   0        0        0     4971 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/tdapi/gm.py
--rwxr-xr-x   0        0        0     1579 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/tdapi/gmtrade.py
--rwxr-xr-x   0        0        0     5736 2023-04-10 03:40:44.638089 vxquant-2023.4.1/src/vxquant/tdapi/miniqmt.py
--rwxr-xr-x   0        0        0     9231 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxquant/tdapi/sim.py
--rwxr-xr-x   0        0        0      523 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/__init__.py
--rwxr-xr-x   0        0        0      746 2023-03-11 01:03:48.000000 vxquant-2023.4.1/src/vxsched/__main__.py
--rwxr-xr-x   0        0        0     4641 2023-04-09 14:08:26.735530 vxquant-2023.4.1/src/vxsched/context.py
--rwxr-xr-x   0        0        0    11339 2023-04-10 12:08:34.700548 vxquant-2023.4.1/src/vxsched/core.py
--rwxr-xr-x   0        0        0     6888 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/event.py
--rwxr-xr-x   0        0        0      282 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/triggers/__init__.py
--rwxr-xr-x   0        0        0     1004 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/triggers/daily.py
--rwxr-xr-x   0        0        0      922 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/triggers/interval.py
--rwxr-xr-x   0        0        0      352 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/triggers/once.py
--rwxr-xr-x   0        0        0     2181 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxsched/triggers/weekly.py
--rwxr-xr-x   0        0        0     3017 2023-04-04 04:12:11.262998 vxquant-2023.4.1/src/vxutils/__init__.py
--rwxr-xr-x   0        0        0    17380 2023-04-07 07:09:07.289149 vxquant-2023.4.1/src/vxutils/cache.py
--rwxr-xr-x   0        0        0    11833 2023-04-09 14:38:13.867949 vxquant-2023.4.1/src/vxutils/convertors.py
--rwxr-xr-x   0        0        0     6015 2023-03-26 12:05:33.678819 vxquant-2023.4.1/src/vxutils/database/__init__.py
--rw-r--r--   0        0        0     5140 2023-04-07 12:46:03.338312 vxquant-2023.4.1/src/vxutils/database/base.py
--rwxr-xr-x   0        0        0    10294 2023-03-15 08:12:42.718770 vxquant-2023.4.1/src/vxutils/database/mongodb.py
--rwxr-xr-x   0        0        0    15430 2023-04-10 13:34:49.001153 vxquant-2023.4.1/src/vxutils/database/sqlite.py
--rwxr-xr-x   0        0        0    19092 2023-04-07 07:18:29.547245 vxquant-2023.4.1/src/vxutils/dataclass.py
--rwxr-xr-x   0        0        0     4963 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxutils/dbproxy.py
--rwxr-xr-x   0        0        0     1498 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxutils/debug.py
--rwxr-xr-x   0        0        0     7179 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxutils/decorators.py
--rwxr-xr-x   0        0        0     1797 2023-03-11 01:37:22.000000 vxquant-2023.4.1/src/vxutils/exceptions.py
--rwxr-xr-x   0        0        0     3416 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxutils/log.py
--rwxr-xr-x   0        0        0    12501 2023-03-23 11:18:42.541440 vxquant-2023.4.1/src/vxutils/net.py
--rwxr-xr-x   0        0        0     4320 2023-04-05 06:39:34.771258 vxquant-2023.4.1/src/vxutils/time.py
--rwxr-xr-x   0        0        0     7418 2023-04-10 08:02:25.257162 vxquant-2023.4.1/src/vxutils/wrappers.py
--rwxr-xr-x   0        0        0    12507 2023-03-06 04:47:42.000000 vxquant-2023.4.1/src/vxutils/zmqsocket.py
--rw-r--r--   0        0        0     2780 1970-01-01 00:00:00.000000 vxquant-2023.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1085 2023-05-04 10:33:28.669027 vxquant-2023.5.13/LICENSE
+-rw-r--r--   0        0        0     2178 2023-05-13 13:14:00.097256 vxquant-2023.5.13/pyproject.toml
+-rw-r--r--   0        0        0     1511 2023-05-04 10:33:28.670067 vxquant-2023.5.13/README.md
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.680910 vxquant-2023.5.13/src/vxdataset/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.681952 vxquant-2023.5.13/src/vxdataset/cache.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.682983 vxquant-2023.5.13/src/vxdataset/collector/__init__.py
+-rw-r--r--   0        0        0     1070 2023-05-04 10:33:28.683969 vxquant-2023.5.13/src/vxdataset/collector/__main__.py
+-rw-r--r--   0        0        0     1362 2023-05-04 10:33:28.684974 vxquant-2023.5.13/src/vxdataset/collector/calendar1111.py
+-rw-r--r--   0        0        0     5804 2023-05-04 10:33:28.685991 vxquant-2023.5.13/src/vxdataset/collector/dumpall.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.687561 vxquant-2023.5.13/src/vxdataset/datasource/__init__.py
+-rw-r--r--   0        0        0     9464 2023-05-04 10:33:28.688576 vxquant-2023.5.13/src/vxdataset/datasource/ifind.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.688576 vxquant-2023.5.13/src/vxdataset/expr/__init__.py
+-rw-r--r--   0        0        0      855 2023-05-04 10:33:28.690708 vxquant-2023.5.13/src/vxdataset/expr/functions.py
+-rw-r--r--   0        0        0    13098 2023-05-04 10:33:28.691752 vxquant-2023.5.13/src/vxdataset/expr/ops.py
+-rw-r--r--   0        0        0     2707 2023-05-04 10:33:28.693807 vxquant-2023.5.13/src/vxdataset/handler.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.693807 vxquant-2023.5.13/src/vxdataset/loaders/__init__.py
+-rw-r--r--   0        0        0     3425 2023-05-04 10:33:28.695890 vxquant-2023.5.13/src/vxdataset/loaders/base.py
+-rw-r--r--   0        0        0     1621 2023-05-04 10:33:28.696416 vxquant-2023.5.13/src/vxdataset/loaders/csv.py
+-rw-r--r--   0        0        0     2283 2023-05-04 10:33:28.697444 vxquant-2023.5.13/src/vxdataset/loaders/gm.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.697444 vxquant-2023.5.13/src/vxdataset/loaders/mongo.py
+-rw-r--r--   0        0        0        2 2023-05-04 10:33:28.699486 vxquant-2023.5.13/src/vxquant/__init__.py
+-rw-r--r--   0        0        0     1445 2023-05-12 13:07:18.804885 vxquant-2023.5.13/src/vxquant/__main__.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.701537 vxquant-2023.5.13/src/vxquant/accountdb/__init__.py
+-rw-r--r--   0        0        0    14550 2023-05-12 09:01:36.204394 vxquant-2023.5.13/src/vxquant/accountdb/base.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.702569 vxquant-2023.5.13/src/vxquant/accountdb/mongodb.py
+-rw-r--r--   0        0        0    19478 2023-05-12 09:01:36.206548 vxquant-2023.5.13/src/vxquant/accountdb/sqlitedb.py
+-rw-r--r--   0        0        0    70276 2023-05-13 12:52:05.932606 vxquant-2023.5.13/src/vxquant/apis.py
+-rw-r--r--   0        0        0      839 2023-05-04 10:33:28.706217 vxquant-2023.5.13/src/vxquant/cli/__init__.py
+-rw-r--r--   0        0        0     2680 2023-05-04 10:33:28.707252 vxquant-2023.5.13/src/vxquant/cli/base.py
+-rw-r--r--   0        0        0     9293 2023-05-12 15:55:49.169408 vxquant-2023.5.13/src/vxquant/cli/gmagent.py
+-rw-r--r--   0        0        0     5111 2023-05-13 12:43:33.895555 vxquant-2023.5.13/src/vxquant/cli/qmtagent.py
+-rw-r--r--   0        0        0     7139 2023-05-13 04:10:19.302071 vxquant-2023.5.13/src/vxquant/config.py
+-rw-r--r--   0        0        0     1536 2023-05-04 10:33:28.711908 vxquant-2023.5.13/src/vxquant/exceptions.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.712942 vxquant-2023.5.13/src/vxquant/factor/__init__.py
+-rw-r--r--   0        0        0     8916 2023-05-04 10:33:28.713984 vxquant-2023.5.13/src/vxquant/factor/builder.py
+-rw-r--r--   0        0        0       25 2023-05-04 10:33:28.715029 vxquant-2023.5.13/src/vxquant/factor/expr/__init__.py
+-rw-r--r--   0        0        0      855 2023-05-04 10:33:28.716057 vxquant-2023.5.13/src/vxquant/factor/expr/functions.py
+-rw-r--r--   0        0        0    14464 2023-05-04 10:33:28.717100 vxquant-2023.5.13/src/vxquant/factor/expr/ops.py
+-rw-r--r--   0        0        0     7410 2023-05-04 10:33:28.717100 vxquant-2023.5.13/src/vxquant/factor/loader.py
+-rw-r--r--   0        0        0     4340 2023-05-04 10:33:28.719155 vxquant-2023.5.13/src/vxquant/factor/normalizer.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.719155 vxquant-2023.5.13/src/vxquant/model/__init__.py
+-rw-r--r--   0        0        0    17857 2023-05-04 10:33:28.720735 vxquant-2023.5.13/src/vxquant/model/account.py
+-rw-r--r--   0        0        0     7035 2023-05-04 10:33:28.721764 vxquant-2023.5.13/src/vxquant/model/contants.py
+-rw-r--r--   0        0        0    16434 2023-05-04 10:33:28.722805 vxquant-2023.5.13/src/vxquant/model/dbaccount.py
+-rw-r--r--   0        0        0    14231 2023-05-04 10:33:28.723838 vxquant-2023.5.13/src/vxquant/model/exchange.py
+-rw-r--r--   0        0        0    12376 2023-05-04 10:33:28.724864 vxquant-2023.5.13/src/vxquant/model/instruments.py
+-rw-r--r--   0        0        0     2936 2023-05-04 10:33:28.725883 vxquant-2023.5.13/src/vxquant/model/nomalize.py
+-rw-r--r--   0        0        0    56399 2023-05-04 10:33:28.726915 vxquant-2023.5.13/src/vxquant/model/portfolio.py
+-rw-r--r--   0        0        0    10885 2023-05-04 10:33:28.727949 vxquant-2023.5.13/src/vxquant/model/preset.py
+-rw-r--r--   0        0        0       49 2023-05-04 10:33:28.729546 vxquant-2023.5.13/src/vxquant/model/tools/__init__.py
+-rw-r--r--   0        0        0     7506 2023-05-04 10:33:28.730595 vxquant-2023.5.13/src/vxquant/model/tools/gmData.py
+-rw-r--r--   0        0        0    10833 2023-05-04 10:33:28.731665 vxquant-2023.5.13/src/vxquant/model/tools/qmtData.py
+-rw-r--r--   0        0        0     5410 2023-05-04 10:33:28.731665 vxquant-2023.5.13/src/vxquant/model/tools/tdxData.py
+-rw-r--r--   0        0        0      155 2023-05-04 10:33:28.733751 vxquant-2023.5.13/src/vxquant/model/typehint.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.747318 vxquant-2023.5.13/src/vxquant/providers/__init__.py
+-rw-r--r--   0        0        0     4711 2023-05-04 10:33:28.748340 vxquant-2023.5.13/src/vxquant/providers/baostock_api.py
+-rw-r--r--   0        0        0    12913 2023-05-12 09:01:36.214325 vxquant-2023.5.13/src/vxquant/providers/base.py
+-rw-r--r--   0        0        0     7023 2023-05-04 10:33:28.750425 vxquant-2023.5.13/src/vxquant/providers/ftp.py
+-rw-r--r--   0        0        0     7357 2023-05-12 14:25:01.455505 vxquant-2023.5.13/src/vxquant/providers/gmapi.py
+-rw-r--r--   0        0        0     3270 2023-05-04 10:33:28.754276 vxquant-2023.5.13/src/vxquant/providers/local.py
+-rw-r--r--   0        0        0    16551 2023-05-13 12:59:56.330397 vxquant-2023.5.13/src/vxquant/providers/miniqmt.py
+-rw-r--r--   0        0        0     8415 2023-05-12 09:01:36.218112 vxquant-2023.5.13/src/vxquant/providers/mongo.py
+-rw-r--r--   0        0        0      136 2023-05-04 10:33:28.757880 vxquant-2023.5.13/src/vxquant/providers/spiders/__init__.py
+-rw-r--r--   0        0        0     2008 2023-05-04 10:33:28.757880 vxquant-2023.5.13/src/vxquant/providers/spiders/calendar_sse.py
+-rw-r--r--   0        0        0     4921 2023-05-04 10:33:28.758893 vxquant-2023.5.13/src/vxquant/providers/spiders/hq_tencent.py
+-rw-r--r--   0        0        0    19454 2023-05-12 09:01:36.221135 vxquant-2023.5.13/src/vxquant/providers/tdx.py
+-rw-r--r--   0        0        0     7183 2023-05-04 10:33:28.761910 vxquant-2023.5.13/src/vxquant/providers/zeromq.py
+-rw-r--r--   0        0        0      523 2023-05-04 10:33:28.773568 vxquant-2023.5.13/src/vxsched/__init__.py
+-rw-r--r--   0        0        0      898 2023-05-12 12:53:36.704705 vxquant-2023.5.13/src/vxsched/__main__.py
+-rw-r--r--   0        0        0     4641 2023-05-04 10:33:28.775589 vxquant-2023.5.13/src/vxsched/context.py
+-rw-r--r--   0        0        0    10804 2023-05-12 12:44:38.688644 vxquant-2023.5.13/src/vxsched/core.py
+-rw-r--r--   0        0        0     6888 2023-05-04 10:33:28.777660 vxquant-2023.5.13/src/vxsched/event.py
+-rw-r--r--   0        0        0      282 2023-05-04 10:33:28.778663 vxquant-2023.5.13/src/vxsched/triggers/__init__.py
+-rw-r--r--   0        0        0     1004 2023-05-04 10:33:28.779678 vxquant-2023.5.13/src/vxsched/triggers/daily.py
+-rw-r--r--   0        0        0      922 2023-05-04 10:33:28.780726 vxquant-2023.5.13/src/vxsched/triggers/interval.py
+-rw-r--r--   0        0        0      352 2023-05-04 10:33:28.781266 vxquant-2023.5.13/src/vxsched/triggers/once.py
+-rw-r--r--   0        0        0     2181 2023-05-04 10:33:28.781266 vxquant-2023.5.13/src/vxsched/triggers/weekly.py
+-rw-r--r--   0        0        0     2985 2023-05-12 09:01:36.223144 vxquant-2023.5.13/src/vxutils/__init__.py
+-rw-r--r--   0        0        0     8211 2023-05-12 09:01:36.225205 vxquant-2023.5.13/src/vxutils/cache.py
+-rw-r--r--   0        0        0    11833 2023-05-04 10:33:28.785292 vxquant-2023.5.13/src/vxutils/convertors.py
+-rw-r--r--   0        0        0     6015 2023-05-04 10:33:28.787294 vxquant-2023.5.13/src/vxutils/database/__init__.py
+-rw-r--r--   0        0        0     5315 2023-05-04 10:33:28.787294 vxquant-2023.5.13/src/vxutils/database/base.py
+-rw-r--r--   0        0        0     4963 2023-05-12 09:01:36.225757 vxquant-2023.5.13/src/vxutils/database/dbproxy.py
+-rw-r--r--   0        0        0    10294 2023-05-04 10:33:28.788298 vxquant-2023.5.13/src/vxutils/database/mongodb.py
+-rw-r--r--   0        0        0    15432 2023-05-12 09:01:36.228837 vxquant-2023.5.13/src/vxutils/database/sqlite.py
+-rw-r--r--   0        0        0    19092 2023-05-04 10:33:28.792364 vxquant-2023.5.13/src/vxutils/dataclass.py
+-rw-r--r--   0        0        0    15377 2023-05-13 12:55:37.010397 vxquant-2023.5.13/src/vxutils/dataorm.py
+-rw-r--r--   0        0        0        0 2023-05-04 10:33:28.794390 vxquant-2023.5.13/src/vxutils/dbutils/__init__.py
+-rw-r--r--   0        0        0    14716 2023-05-04 10:33:28.795898 vxquant-2023.5.13/src/vxutils/dbutils/dborm.py
+-rw-r--r--   0        0        0    22686 2023-05-04 10:33:28.796923 vxquant-2023.5.13/src/vxutils/dbutils/pool.py
+-rw-r--r--   0        0        0    28730 2023-05-04 10:33:28.797953 vxquant-2023.5.13/src/vxutils/dbutils/proxy.py
+-rw-r--r--   0        0        0     1498 2023-05-04 10:33:28.797953 vxquant-2023.5.13/src/vxutils/debug.py
+-rw-r--r--   0        0        0     7179 2023-05-04 10:33:28.798964 vxquant-2023.5.13/src/vxutils/decorators.py
+-rw-r--r--   0        0        0     1797 2023-05-04 10:33:28.799991 vxquant-2023.5.13/src/vxutils/exceptions.py
+-rw-r--r--   0        0        0     3416 2023-05-04 10:33:28.801010 vxquant-2023.5.13/src/vxutils/log.py
+-rw-r--r--   0        0        0    12501 2023-05-04 10:33:28.801010 vxquant-2023.5.13/src/vxutils/net.py
+-rw-r--r--   0        0        0     4352 2023-05-04 10:33:28.803078 vxquant-2023.5.13/src/vxutils/time.py
+-rw-r--r--   0        0        0     7483 2023-05-04 10:33:28.803078 vxquant-2023.5.13/src/vxutils/wrappers.py
+-rw-r--r--   0        0        0    12507 2023-05-04 10:33:28.804089 vxquant-2023.5.13/src/vxutils/zmqsocket.py
+-rw-r--r--   0        0        0     3328 1970-01-01 00:00:00.000000 vxquant-2023.5.13/setup.py
+-rw-r--r--   0        0        0     2769 1970-01-01 00:00:00.000000 vxquant-2023.5.13/PKG-INFO
```

### Comparing `vxquant-2023.4.1/LICENSE` & `vxquant-2023.5.13/LICENSE`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/README.md` & `vxquant-2023.5.13/README.md`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/pyproject.toml` & `vxquant-2023.5.13/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "vxquant"
-version = "2023.04.01"
+version = "2023.05.13"
 description = "一个简单、易用、面向中国股市实盘的python量化交易框架"
 license = "MIT"
 authors = ["vex1023 <vex1023@qq.com>"]
 homepage = "https://gitee.com/vxquant/vxquant"
 keywords = ["quant", "tools"]
 readme = "README.md"
 
@@ -24,27 +24,29 @@
     { include = "vxquant",from = "src/" },
     { include = "vxutils",from = "src/" },
     { include = "vxsched",from = "src/" },
     { include = "vxdataset",from = "src/" },
 ]
 
 [tool.poetry.scripts]
-vxquant = 'vxquant.__main__:main'
+vxrun = 'vxquant.__main__:main'
+vxsched = 'vxsched.__main__:main'
 
 [tool.poetry.dependencies]
 python = "^3.8"
 pyzmq = "*"
 pymongo = "*"
 python-dateutil = "*"
 requests = "*"
 six = "*"
 numpy = "*"
 pandas = "*"
 tqdm = "*"
 scipy = "*"
+sqlalchemy ="^2.0"
 polars = {version = "*", extras = ["pyarrow"]}
 
 [tool.poetry.dev-dependencies]
 pytest = "^5.2"
 flake8 = "*"
 pylint = "*"
 twine = "*"
```

### Comparing `vxquant-2023.4.1/src/vxdataset/collector/__main__.py` & `vxquant-2023.5.13/src/vxdataset/collector/__main__.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/collector/calendar1111.py` & `vxquant-2023.5.13/src/vxdataset/collector/calendar1111.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/collector/dumpall.py` & `vxquant-2023.5.13/src/vxdataset/collector/dumpall.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/datasource/ifind.py` & `vxquant-2023.5.13/src/vxdataset/datasource/ifind.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/expr/functions.py` & `vxquant-2023.5.13/src/vxdataset/expr/functions.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/expr/ops.py` & `vxquant-2023.5.13/src/vxdataset/expr/ops.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/handler.py` & `vxquant-2023.5.13/src/vxdataset/handler.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/loaders/base.py` & `vxquant-2023.5.13/src/vxdataset/loaders/base.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/loaders/csv.py` & `vxquant-2023.5.13/src/vxdataset/loaders/csv.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxdataset/loaders/gm.py` & `vxquant-2023.5.13/src/vxdataset/loaders/gm.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/accountdb/base.py` & `vxquant-2023.5.13/src/vxquant/accountdb/base.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,389 +1,393 @@
-"""账户数据库存储方案    """
-
-from contextlib import contextmanager
-from typing import Dict, List, Union, Type
-from vxquant.model.typehint import DateTimeType
-from vxquant.model.exchange import (
-    vxAccountInfo,
-    vxOrder,
-    vxTrade,
-    vxPortfolioInfo,
-    vxPosition,
-    vxCashPosition,
-    vxTransferInfo,
-)
-from vxutils.database.sqlite import vxSQLiteDB
-from vxutils.database.base import vxDataBase
-from vxutils import logger, vxtime, to_timestamp, to_timestring, combine_datetime
-
-
-class vxAccountDB:
-    """账户数据库"""
-
-    def __init__(
-        self,
-        db_uri: str = None,
-        database_factory: Type[vxDataBase] = None,
-    ) -> None:
-        if database_factory is None:
-            database_factory = vxSQLiteDB
-        self._dbconn: vxDataBase = database_factory.connect(db_uri)
-
-        # 账户信息
-        self.create_table("accounts", ["account_id"], vxAccountInfo)
-        self.create_table(
-            "history_accounts", ["account_id", "settle_date"], vxAccountInfo
-        )
-
-        self.create_table(
-            "broker_accounts", ["account_id", "settle_date"], vxAccountInfo
-        )
-        # 账号持仓
-        self.create_table(
-            "positions",
-            ["account_id", "symbol", "position_side"],
-            vxPosition,
-        )
-        self.create_table(
-            "history_positions",
-            ["account_id", "symbol", "settle_date", "position_side"],
-            vxPosition,
-        )
-        self.create_table(
-            "broker_positions",
-            ["account_id", "symbol", "settle_date", "position_side"],
-            vxPosition,
-        )
-        # 账户交易委托
-        self.create_table("orders", ["order_id"], vxOrder)
-        self.create_table("broker_orders", ["exchange_order_id"], vxOrder)
-        # 账户成交回报
-        self.create_table("trades", ["trade_id"], vxTrade)
-        self.create_table("broker_trades", ["trade_id"], vxTrade)
-        # 账户转账记录
-        self.create_table("transferinfos", ["transfer_id"], vxTransferInfo)
-        # 账户组合信息
-        self.create_table(
-            "portfolios", ["portfolio_id", "settle_date"], vxPortfolioInfo
-        )
-
-        self._settle_date = self._get_lastest_settle_date() or vxtime.today("23:59:59")
-        logger.info(f"账户数据库初始化完成: {to_timestring(self.settle_date)}")
-
-    def __getattr__(self, attr: str):
-        return getattr(self._dbconn, attr)
-
-    @contextmanager
-    def start_session(self):
-        """启动事务"""
-        with self._dbconn.lock, self._dbconn:
-            yield self
-
-    def create_account(
-        self,
-        portfolio_id: str,
-        account_id: str,
-        init_balance=0.0,
-        created_dt: DateTimeType = None,
-        if_exists: str = "ignore",
-        channel: str = "sim",
-    ) -> vxAccountInfo:
-        """创建新账户"""
-        if_exists = if_exists.lower()
-        created_dt = to_timestamp(created_dt or vxtime.today())
-        settle_date = self.settle_date
-
-        accountinfo = self.findone("accounts", account_id=account_id)
-
-        if if_exists == "ignore" and accountinfo:
-            return accountinfo
-        elif if_exists == "delete":
-            self.delete("accounts", account_id=account_id)
-            self.delete("history_accounts", account_id=account_id)
-            self.delete("positions", account_id=account_id)
-            self.delete("history_positions", account_id=account_id)
-            self.delete("orders", account_id=account_id)
-            self.delete("trades", account_id=account_id)
-            self.delete("transferinfos", account_id=account_id)
-        # elif accountinfo:
-        #    raise ValueError(f"账户id ({account_id})已存在，请勿重复创建")
-
-        cash = vxCashPosition(
-            account_id=account_id,
-            portfolio_id=portfolio_id,
-            volume_his=init_balance,
-            created_dt=created_dt,
-            settle_date=settle_date,
-        )
-
-        accountinfo = vxAccountInfo(
-            account_id=account_id,
-            portfolio_id=portfolio_id,
-            deposit=0.0,
-            balance=init_balance,
-            fund_shares=init_balance,
-            asset_yd=init_balance,
-            nav_yd=init_balance,
-            fund_nav_yd=1.0,
-            settle_date=settle_date,
-            created_dt=created_dt,
-            channel=channel,
-        )
-
-        transferinfo = vxTransferInfo(
-            account_id=account_id,
-            amount=init_balance,
-            transfer_direction="In",
-            created_dt=created_dt,
-        )
-
-        self.save("accounts", accountinfo)
-        self.save("positions", cash)
-        self.save("transferinfos", transferinfo)
-
-    def _get_lastest_settle_date(self) -> DateTimeType:
-        """获取最近的结算日期"""
-        return self.max("accounts", "settle_date")
-
-    @property
-    def settle_date(self) -> float:
-        """当前结算日期
-
-        Returns:
-            float -- 当前待结算日期的timestamp格式数据
-        """
-        return self._settle_date
-
-    @property
-    def broker_accountids(self) -> tuple:
-        return self.distinct("broker_accounts", "account_id")
-
-    def update_order(self, broker_order: vxOrder) -> None:
-        """处理委托状态更新事件"""
-
-    def update_trade(self, broker_trade: vxTrade) -> None:
-        """处理成交回报事件"""
-
-    def update_position_lasttrades(
-        self, *prices: List[Union[Dict, vxTrade, vxOrder]]
-    ) -> None:
-        """更新持仓股票最新价格
-        prices:[
-            {
-                "symbol":"SHSE.600000",
-                "lasttrade": 10.31  or "price": 10.31,
-                "created_dt": 16232132111.12 or "updated_dt": 16232132111.12
-                ...
-            }
-        ]
-        """
-
-    def _save_broker_account(self, broker_accountinfo: vxAccountInfo) -> None:
-        """保存broker的账户信息
-
-        Arguments:
-            broker_accountinfo {vxAccountInfo} -- 从broker获取的accountinfo信息
-        """
-        yesterday = self.max(
-            "accounts",
-            "settle_date",
-            f"settle_date < {self.settle_date}",
-            account_id=broker_accountinfo.account_id,
-        )
-        db_accountinfo = self.findone(
-            "accounts",
-            account_id=broker_accountinfo.account_id,
-            settle_date=yesterday,
-        )
-        if not db_accountinfo:
-            db_accountinfo = vxAccountInfo(broker_accountinfo.message)
-            db_accountinfo.portfolio_id = "default"
-            db_accountinfo.fund_shares = broker_accountinfo.nav
-            db_accountinfo.asset_yd = broker_accountinfo.asset
-            db_accountinfo.nav_yd = broker_accountinfo.nav
-            db_accountinfo.fund_nav_yd = broker_accountinfo.fund_nav
-            db_accountinfo.settle_date = self.settle_date
-            db_accountinfo.channel = "physical"
-        else:
-            db_accountinfo.debt = broker_accountinfo.debt
-            db_accountinfo.balance = broker_accountinfo.balance
-            db_accountinfo.frozen = broker_accountinfo.frozen
-            db_accountinfo.margin_available = broker_accountinfo.margin_available
-            db_accountinfo.marketvalue = broker_accountinfo.marketvalue
-            db_accountinfo.fnl = broker_accountinfo.fnl
-            db_accountinfo.fund_shares = broker_accountinfo.fund_shares
-            db_accountinfo.settle_date = self.settle_date
-
-        self.save("broker_accounts", db_accountinfo)
-        return db_accountinfo.account_id
-
-    def _save_broker_positions(
-        self,
-        broker_account_id: str,
-        broker_positions: Dict[str, Union[vxPosition, vxCashPosition]],
-    ) -> None:
-        self.delete(
-            "broker_positions",
-            account_id=broker_account_id,
-            settle_date=self.settle_date,
-        )
-        positions = []
-        for p in broker_positions.values():
-            p.portfolio_id = "default"
-            p.settle_date = self.settle_date
-            positions.append(p)
-        self.save("broker_positions", positions)
-
-    def sync_with_broker(
-        self,
-        broker_accountinfo: vxAccountInfo,
-        broker_positions: Dict,
-        broker_orders: Dict = None,
-        broker_trades: Dict = None,
-        settle_date: DateTimeType = None,
-    ) -> None:
-        """同步broker的持仓和信息"""
-        if settle_date is None:
-            settle_date = self.settle_date
-
-        logger.info(f"日结日期：{to_timestring(settle_date,'%Y-%m-%d')}")
-        broker_accountinfo.settle_date = settle_date
-        account_id = self._save_broker_account(broker_accountinfo)
-        logger.info(f"更新broker_accounts: {account_id} 基本信息")
-
-        if broker_positions:
-            self._save_broker_positions(account_id, broker_positions)
-            logger.info(f"更新broker_positions: {len(broker_positions)}个")
-
-        exchange_order_ids = self.distinct("orders", "exchange_order_id")
-
-        if broker_orders:
-            self.save("broker_orders", list(broker_orders.values()))
-            for exchange_order_id in exchange_order_ids:
-                if exchange_order_id not in broker_orders:
-                    continue
-                self.update_order(broker_orders[exchange_order_id])
-                logger.info(
-                    "更新broker_orders:"
-                    f" {exchange_order_id} 委托状态{broker_orders[exchange_order_id].status}"
-                )
-
-        if broker_trades:
-            self.save("broker_trades", list(broker_trades.values()))
-            saved_tradeids = self.distinct("trades", "trade_id")
-
-            for broker_trade in broker_trades.values():
-                if broker_trade.exchange_order_id not in exchange_order_ids or (
-                    broker_trade.trade_id in saved_tradeids
-                ):
-                    continue
-                self.update_trade(broker_trade)
-                logger.warning(f"新增成交回报: {broker_trade}")
-
-    def update_after_close(self) -> None:
-        """收盘后事件
-
-        1、将未成交的委托单状态更新为已超时
-        2、更新账户信息frozens
-
-        """
-
-    def update_settle_date(self, settle_date: DateTimeType) -> None:
-        """更新结算日期
-
-        Arguments:
-            settle_date {DateTimeType} -- 结算日期
-        """
-        if settle_date is None:
-            settle_date = vxtime.today("23:59:59")
-        else:
-            settle_date = combine_datetime(settle_date, "23:59:59")
-
-        if settle_date <= self.settle_date:
-            logger.error(
-                f"新设置的结算日期: {to_timestring(settle_date,'%Y-%m-%d')}"
-                f"小于当前结算日期({to_timestring(self.settle_date,'%Y-%m-%d')})"
-            )
-            return
-
-        logger.info(
-            f"结算日期：{to_timestring(self.settle_date,'%Y-%m-%d')} ==>"
-            f" {to_timestring(settle_date,'%Y-%m-%d')} 开始..."
-        )
-        cur = self.find("broker_accounts", settle_date=self.settle_date)
-        data = []
-        for broker_accountinfo in cur:
-            broker_accountinfo.deposit = 0
-            broker_accountinfo.withdraw = 0
-            broker_accountinfo.asset_yd = broker_accountinfo.asset
-            broker_accountinfo.nav_yd = broker_accountinfo.nav
-            broker_accountinfo.fund_nav_yd = broker_accountinfo.fund_nav
-            broker_accountinfo.settle_date = settle_date
-            data.append(broker_accountinfo)
-
-        if data:
-            self.save("broker_accounts", data)
-            logger.info(f"结转broker_accounts: {len(data)}个")
-
-        cur = self.find("broker_positions", settle_date=self.settle_date)
-        data = []
-        for broker_position in cur:
-            broker_position.volume_his = broker_position.volume
-            broker_position.volume_today = 0
-            broker_position.settle_date = settle_date
-            data.append(broker_position)
-
-        if data:
-            self.save("broker_positions", data)
-            logger.info(f"结转broker_positions: {len(data)}个")
-
-        cur = self.find("accounts")
-        data = []
-        for accountinfo in cur:
-            accountinfo.deposit = 0
-            accountinfo.withdraw = 0
-            accountinfo.asset_yd = accountinfo.asset
-            accountinfo.nav_yd = accountinfo.nav
-            accountinfo.fund_nav_yd = accountinfo.fund_nav
-            accountinfo.settle_date = settle_date
-            data.append(accountinfo)
-        if data:
-            self.save("history_accounts", data)
-            self.save("accounts", data)
-            logger.info(f"结转accounts: {len(data)}个")
-
-        cur = self.find("positions")
-        data = []
-        for position in cur:
-            if position.volume <= 0:
-                continue
-
-            position.volume_his = position.volume
-            position.volume_today = 0
-            position.settle_date = settle_date
-            data.append(position)
-        if data:
-            self.save("positions", data)
-            self.save("history_positions", data)
-            logger.info(f"结转positions: {len(data)}个")
-        self.delete("positions", volume=0)
-
-        self._settle_date = settle_date
-        self.update_cash_position_frozens([])
-        self.update_symbol_position_frozens([])
-        self.update_accountinfos([])
-        logger.info(
-            f"结转完成,当前结算日: {to_timestring(self.settle_date,'%Y-%m-%d')}"
-        )
-
-    def update_cash_position_frozens(self, account_ids: List = None) -> None:
-        """更新账户资金冻结"""
-
-    def update_symbol_position_frozens(self, account_ids: List = None) -> None:
-        """更新持仓冻结"""
-
-    def update_accountinfos(self, account_ids: List = None) -> None:
-        """更新账户信息"""
-
-    def update_order_filleds(self, account_ids: List = None) -> None:
-        """更新委托单成交数量"""
+"""账户数据库存储方案    """
+
+from contextlib import contextmanager
+from typing import Dict, List, Union, Type
+from vxquant.model.contants import OrderStatus, OrderDirection
+from vxquant.model.typehint import DateTimeType
+from vxquant.model.exchange import (
+    vxAccountInfo,
+    vxOrder,
+    vxTrade,
+    vxPortfolioInfo,
+    vxPosition,
+    vxCashPosition,
+    vxTransferInfo,
+)
+from vxutils.database.sqlite import vxSQLiteDB
+from vxutils.database.base import vxDataBase
+from vxutils.dataorm import vxDataBase as vxDataBase2, vxDBSession
+from vxutils import logger, vxtime, to_timestamp, to_timestring, combine_datetime
+
+
+class vxAccountDB:
+    """账户数据库"""
+
+    def __init__(
+        self,
+        db_uri: str = None,
+        database_factory: Type[vxDataBase] = None,
+    ) -> None:
+        if database_factory is None:
+            database_factory = vxSQLiteDB
+        self._dbconn: vxDataBase = database_factory.connect(db_uri)
+
+        # 账户信息
+        self.create_table("accounts", ["account_id"], vxAccountInfo)
+        self.create_table(
+            "history_accounts", ["account_id", "settle_date"], vxAccountInfo
+        )
+
+        self.create_table(
+            "broker_accounts", ["account_id", "settle_date"], vxAccountInfo
+        )
+        # 账号持仓
+        self.create_table(
+            "positions",
+            ["account_id", "symbol", "position_side"],
+            vxPosition,
+        )
+        self.create_table(
+            "history_positions",
+            ["account_id", "symbol", "settle_date", "position_side"],
+            vxPosition,
+        )
+        self.create_table(
+            "broker_positions",
+            ["account_id", "symbol", "settle_date", "position_side"],
+            vxPosition,
+        )
+        # 账户交易委托
+        self.create_table("orders", ["order_id"], vxOrder)
+        self.create_table("broker_orders", ["exchange_order_id"], vxOrder)
+        # 账户成交回报
+        self.create_table("trades", ["trade_id"], vxTrade)
+        self.create_table("broker_trades", ["trade_id"], vxTrade)
+        # 账户转账记录
+        self.create_table("transferinfos", ["transfer_id"], vxTransferInfo)
+        # 账户组合信息
+        self.create_table(
+            "portfolios", ["portfolio_id", "settle_date"], vxPortfolioInfo
+        )
+
+        self._settle_date = self._get_lastest_settle_date() or vxtime.today("23:59:59")
+        logger.info(f"账户数据库初始化完成: {to_timestring(self.settle_date)}")
+
+    def __getattr__(self, attr: str):
+        return getattr(self._dbconn, attr)
+
+    @contextmanager
+    def start_session(self):
+        """启动事务"""
+        with self._dbconn.lock, self._dbconn:
+            yield self
+
+    def create_account(
+        self,
+        portfolio_id: str,
+        account_id: str,
+        init_balance=0.0,
+        created_dt: DateTimeType = None,
+        if_exists: str = "ignore",
+        channel: str = "sim",
+    ) -> vxAccountInfo:
+        """创建新账户"""
+        if_exists = if_exists.lower()
+        created_dt = to_timestamp(created_dt or vxtime.today())
+        settle_date = self.settle_date
+
+        accountinfo = self.findone("accounts", account_id=account_id)
+
+        if if_exists == "ignore" and accountinfo:
+            return accountinfo
+        elif if_exists == "delete":
+            self.delete("accounts", account_id=account_id)
+            self.delete("history_accounts", account_id=account_id)
+            self.delete("positions", account_id=account_id)
+            self.delete("history_positions", account_id=account_id)
+            self.delete("orders", account_id=account_id)
+            self.delete("trades", account_id=account_id)
+            self.delete("transferinfos", account_id=account_id)
+        # elif accountinfo:
+        #    raise ValueError(f"账户id ({account_id})已存在，请勿重复创建")
+
+        cash = vxCashPosition(
+            account_id=account_id,
+            portfolio_id=portfolio_id,
+            volume_his=init_balance,
+            created_dt=created_dt,
+            settle_date=settle_date,
+        )
+
+        accountinfo = vxAccountInfo(
+            account_id=account_id,
+            portfolio_id=portfolio_id,
+            deposit=0.0,
+            balance=init_balance,
+            fund_shares=init_balance,
+            asset_yd=init_balance,
+            nav_yd=init_balance,
+            fund_nav_yd=1.0,
+            settle_date=settle_date,
+            created_dt=created_dt,
+            channel=channel,
+        )
+
+        transferinfo = vxTransferInfo(
+            account_id=account_id,
+            amount=init_balance,
+            transfer_direction="In",
+            created_dt=created_dt,
+        )
+
+        self.save("accounts", accountinfo)
+        self.save("positions", cash)
+        self.save("transferinfos", transferinfo)
+
+    def _get_lastest_settle_date(self) -> DateTimeType:
+        """获取最近的结算日期"""
+        return self.max("accounts", "settle_date")
+
+    @property
+    def settle_date(self) -> float:
+        """当前结算日期
+
+        Returns:
+            float -- 当前待结算日期的timestamp格式数据
+        """
+        return self._settle_date
+
+    @property
+    def broker_accountids(self) -> tuple:
+        return self.distinct("broker_accounts", "account_id")
+
+    def update_order(self, broker_order: vxOrder) -> None:
+        """处理委托状态更新事件"""
+
+    def update_trade(self, broker_trade: vxTrade) -> None:
+        """处理成交回报事件"""
+
+    def update_position_lasttrades(
+        self, *prices: List[Union[Dict, vxTrade, vxOrder]]
+    ) -> None:
+        """更新持仓股票最新价格
+        prices:[
+            {
+                "symbol":"SHSE.600000",
+                "lasttrade": 10.31  or "price": 10.31,
+                "created_dt": 16232132111.12 or "updated_dt": 16232132111.12
+                ...
+            }
+        ]
+        """
+
+    def _save_broker_account(self, broker_accountinfo: vxAccountInfo) -> None:
+        """保存broker的账户信息
+
+        Arguments:
+            broker_accountinfo {vxAccountInfo} -- 从broker获取的accountinfo信息
+        """
+        yesterday = self.max(
+            "accounts",
+            "settle_date",
+            f"settle_date < {self.settle_date}",
+            account_id=broker_accountinfo.account_id,
+        )
+        db_accountinfo = self.findone(
+            "accounts",
+            account_id=broker_accountinfo.account_id,
+            settle_date=yesterday,
+        )
+        if not db_accountinfo:
+            db_accountinfo = vxAccountInfo(broker_accountinfo.message)
+            db_accountinfo.portfolio_id = "default"
+            db_accountinfo.fund_shares = broker_accountinfo.nav
+            db_accountinfo.asset_yd = broker_accountinfo.asset
+            db_accountinfo.nav_yd = broker_accountinfo.nav
+            db_accountinfo.fund_nav_yd = broker_accountinfo.fund_nav
+            db_accountinfo.settle_date = self.settle_date
+            db_accountinfo.channel = "physical"
+        else:
+            db_accountinfo.debt = broker_accountinfo.debt
+            db_accountinfo.balance = broker_accountinfo.balance
+            db_accountinfo.frozen = broker_accountinfo.frozen
+            db_accountinfo.margin_available = broker_accountinfo.margin_available
+            db_accountinfo.marketvalue = broker_accountinfo.marketvalue
+            db_accountinfo.fnl = broker_accountinfo.fnl
+            db_accountinfo.fund_shares = broker_accountinfo.fund_shares
+            db_accountinfo.settle_date = self.settle_date
+
+        self.save("broker_accounts", db_accountinfo)
+        return db_accountinfo.account_id
+
+    def _save_broker_positions(
+        self,
+        broker_account_id: str,
+        broker_positions: Dict[str, Union[vxPosition, vxCashPosition]],
+    ) -> None:
+        self.delete(
+            "broker_positions",
+            account_id=broker_account_id,
+            settle_date=self.settle_date,
+        )
+        positions = []
+        for p in broker_positions.values():
+            p.portfolio_id = "default"
+            p.settle_date = self.settle_date
+            positions.append(p)
+        self.save("broker_positions", positions)
+
+    def sync_with_broker(
+        self,
+        broker_accountinfo: vxAccountInfo,
+        broker_positions: Dict,
+        broker_orders: Dict = None,
+        broker_trades: Dict = None,
+        settle_date: DateTimeType = None,
+    ) -> None:
+        """同步broker的持仓和信息"""
+        if settle_date is None:
+            settle_date = self.settle_date
+
+        logger.info(f"日结日期：{to_timestring(settle_date,'%Y-%m-%d')}")
+        broker_accountinfo.settle_date = settle_date
+        account_id = self._save_broker_account(broker_accountinfo)
+        logger.info(f"更新broker_accounts: {account_id} 基本信息")
+
+        if broker_positions:
+            self._save_broker_positions(account_id, broker_positions)
+            logger.info(f"更新broker_positions: {len(broker_positions)}个")
+
+        exchange_order_ids = self.distinct("orders", "exchange_order_id")
+
+        if broker_orders:
+            self.save("broker_orders", list(broker_orders.values()))
+            for exchange_order_id in exchange_order_ids:
+                if exchange_order_id not in broker_orders:
+                    continue
+                self.update_order(broker_orders[exchange_order_id])
+                logger.info(
+                    "更新broker_orders:"
+                    f" {exchange_order_id} 委托状态{broker_orders[exchange_order_id].status}"
+                )
+
+        if broker_trades:
+            self.save("broker_trades", list(broker_trades.values()))
+            saved_tradeids = self.distinct("trades", "trade_id")
+
+            for broker_trade in broker_trades.values():
+                if broker_trade.exchange_order_id not in exchange_order_ids or (
+                    broker_trade.trade_id in saved_tradeids
+                ):
+                    continue
+                self.update_trade(broker_trade)
+                logger.warning(f"新增成交回报: {broker_trade}")
+
+    def update_after_close(self) -> None:
+        """收盘后事件
+
+        1、将未成交的委托单状态更新为已超时
+        2、更新账户信息frozens
+        3、保存账户信息和持仓信息至历史表
+
+
+        """
+
+    def update_settle_date(self, settle_date: DateTimeType) -> None:
+        """更新结算日期
+
+        Arguments:
+            settle_date {DateTimeType} -- 结算日期
+        """
+        if settle_date is None:
+            settle_date = vxtime.today("23:59:59")
+        else:
+            settle_date = combine_datetime(settle_date, "23:59:59")
+
+        if settle_date <= self.settle_date:
+            logger.error(
+                f"新设置的结算日期: {to_timestring(settle_date,'%Y-%m-%d')}"
+                f"小于当前结算日期({to_timestring(self.settle_date,'%Y-%m-%d')})"
+            )
+            return
+
+        logger.info(
+            f"结算日期：{to_timestring(self.settle_date,'%Y-%m-%d')} ==>"
+            f" {to_timestring(settle_date,'%Y-%m-%d')} 开始..."
+        )
+        cur = self.find("broker_accounts", settle_date=self.settle_date)
+        data = []
+        for broker_accountinfo in cur:
+            broker_accountinfo.deposit = 0
+            broker_accountinfo.withdraw = 0
+            broker_accountinfo.asset_yd = broker_accountinfo.asset
+            broker_accountinfo.nav_yd = broker_accountinfo.nav
+            broker_accountinfo.fund_nav_yd = broker_accountinfo.fund_nav
+            broker_accountinfo.settle_date = settle_date
+            data.append(broker_accountinfo)
+
+        if data:
+            self.save("broker_accounts", data)
+            logger.info(f"结转broker_accounts: {len(data)}个")
+
+        cur = self.find("broker_positions", settle_date=self.settle_date)
+        data = []
+        for broker_position in cur:
+            broker_position.volume_his = broker_position.volume
+            broker_position.volume_today = 0
+            broker_position.settle_date = settle_date
+            data.append(broker_position)
+
+        if data:
+            self.save("broker_positions", data)
+            logger.info(f"结转broker_positions: {len(data)}个")
+
+        cur = self.find("accounts")
+        data = []
+        for accountinfo in cur:
+            accountinfo.deposit = 0
+            accountinfo.withdraw = 0
+            accountinfo.asset_yd = accountinfo.asset
+            accountinfo.nav_yd = accountinfo.nav
+            accountinfo.fund_nav_yd = accountinfo.fund_nav
+            accountinfo.settle_date = settle_date
+            data.append(accountinfo)
+        if data:
+            self.save("history_accounts", data)
+            self.save("accounts", data)
+            logger.info(f"结转accounts: {len(data)}个")
+
+        cur = self.find("positions")
+        data = []
+        for position in cur:
+            if position.volume <= 0:
+                continue
+
+            position.volume_his = position.volume
+            position.volume_today = 0
+            position.settle_date = settle_date
+            data.append(position)
+        if data:
+            self.save("positions", data)
+            self.save("history_positions", data)
+            logger.info(f"结转positions: {len(data)}个")
+        self.delete("positions", volume=0)
+
+        self._settle_date = settle_date
+        self.update_cash_position_frozens([])
+        self.update_symbol_position_frozens([])
+        self.update_accountinfos([])
+        logger.info(
+            f"结转完成,当前结算日: {to_timestring(self.settle_date,'%Y-%m-%d')}"
+        )
+
+    def update_cash_position_frozens(self, account_ids: List = None) -> None:
+        """更新账户资金冻结"""
+
+    def update_symbol_position_frozens(self, account_ids: List = None) -> None:
+        """更新持仓冻结"""
+
+    def update_accountinfos(self, account_ids: List = None) -> None:
+        """更新账户信息"""
+
+    def update_order_filleds(self, account_ids: List = None) -> None:
+        """更新委托单成交数量"""
```

### Comparing `vxquant-2023.4.1/src/vxquant/accountdb/sqlitedb.py` & `vxquant-2023.5.13/src/vxquant/accountdb/sqlitedb.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,494 +1,518 @@
-"""基于sqlite3 的accountdb"""
-
-from sqlite3 import IntegrityError
-from typing import Dict, List, Union, Type
-from vxquant.model.typehint import DateTimeType
-from vxquant.model.contants import OrderOffset, OrderStatus, OrderDirection
-from vxquant.model.exchange import vxOrder, vxTrade, vxTick, vxCashPosition, vxPosition
-from vxquant.model.preset import vxMarketPreset
-from vxquant.accountdb.base import vxAccountDB
-from vxquant.exceptions import NoEnoughPosition
-from vxutils.database.base import vxDataBase
-from vxutils.database.sqlite import vxSQLiteDB
-from vxutils import logger, vxtime
-
-
-def _sub_volume(
-    position: Union[vxCashPosition, vxPosition],
-    volume: Union[float, int],
-    allow_negative: bool = False,
-) -> Union[vxCashPosition, vxPosition]:
-    if volume > position.available and not allow_negative:
-        raise NoEnoughPosition(
-            f"{position.symbol}可用余额({position.available:,.2f})"
-            f" 小于需扣减{volume:,.2f}"
-        )
-
-    delta = position.volume_his - volume
-    position.volume_his = max(delta, 0)
-    position.volume_today += min(delta, 0)
-    return position
-
-
-class vxSQLiteAccountDB(vxAccountDB):
-    """账户数据库"""
-
-    def __init__(
-        self,
-        db_uri: str = None,
-        database_factory: Type[vxSQLiteDB] = None,
-    ) -> None:
-        super().__init__(db_uri, database_factory or vxSQLiteDB)
-
-    def update_position_lasttrades(
-        self, *prices: List[Union[Dict, vxTrade, vxTick]]
-    ) -> None:
-        if len(prices) == 1 and isinstance(prices[0], (list, tuple)):
-            prices = prices[0]
-
-        lasttrades = [
-            {
-                "symbol": price["symbol"],
-                "lasttrade": (
-                    price["lasttrade"] if "lasttrade" in price else price["price"]
-                ),
-                "created_dt": price["created_dt"],
-            }
-            for price in prices
-            if (price["lasttrade"] if "lasttrade" in price else price["price"]) > 0
-        ]
-        self.executemany(
-            f"""     
-            UPDATE `positions` as t
-            SET lasttrade=:lasttrade,
-                marketvalue=ROUND(t.volume * :lasttrade,2),
-                fnl = ROUND(t.volume * :lasttrade - t.cost,2),
-                updated_dt = :created_dt
-            WHERE t.symbol = :symbol
-            AND t.settle_date={self.settle_date};
-            """,
-            lasttrades,
-        )
-        cur = self.execute(f"""
-                SELECT  account_id,
-                        SUM(marketvalue) as marketvalue,
-                        SUM(fnl) as fnl
-                FROM positions
-                WHERE symbol !='CNY'
-                AND settle_date = {self.settle_date}
-                GROUP BY account_id;
-            """)
-        self.executemany(
-            f"""
-                UPDATE accounts
-                SET asset=ROUND(balance+:marketvalue,2),
-                    nav=ROUND(balance+:marketvalue - debt,2),
-                    marketvalue=ROUND(:marketvalue,2),
-                    today_profit = ROUND(balance+:marketvalue-nav_yd-deposit + withdraw,2),
-                    fnl=ROUND(:fnl,2),
-                    fund_nav=ROUND((balance+:marketvalue - debt)/fund_shares,4)
-                WHERE account_id = :account_id
-                AND settle_date= {self.settle_date};
-            """,
-            [dict(item) for item in cur],
-        )
-
-    def update_order_filleds(self, account_ids: List[str] = None) -> None:
-        """更新order成交情况
-
-        Arguments:
-            order_ids {List[str]} -- 待更新的order_ids
-        """
-        conditions = [
-            """ 
-                status in (
-                    'PendingNew', 
-                    'New',
-                    'PartiallyFilled'
-                ) 
-            """,
-            f"""created_dt > {vxtime.today()}""",
-            f"""created_dt < {self._settle_date}""",
-        ]
-        if account_ids:
-            conditions.append(f""" account_id in ('{"' , '".join(account_ids)}') """)
-
-        cur = self.execute(f"""
-                SELECT  order_id,
-                        SUM(volume) as filled_volume, 
-                        SUM(volume*price) as filled_amount,
-                        SUM(commission) as commission
-                FROM trades
-                WHERE account_id in ('{"','".join(account_ids)}')
-                GROUP BY order_id
-            """)
-        filleds = {item["order_id"]: item for item in cur}
-        if not filleds:
-            return
-
-        cur = self.find("orders", f"""order_id in ('{"','".join(filleds.keys())}')""")
-        orders = []
-        for order in cur:
-            order.filled_volume = filleds[order.order_id].filled_volume
-            order.filled_amount = (
-                (
-                    filleds[order.order_id].filled_amount
-                    + filleds[order.order_id].commission
-                )
-                if order.order_direction.name == "Buy"
-                else (
-                    filleds[order.order_id].filled_amount
-                    - filleds[order.order_id].commission
-                )
-            )
-            order.status = (
-                "PartiallyFilled" if order.volume > order.filled_volume else "Filled"
-            )
-            orders.append(order)
-
-        if orders:
-            self.save("orders", orders)
-
-    def update_cash_position_frozens(self, account_ids: List[str]) -> None:
-        """更新cash的frozens"""
-
-        conditions = [
-            """
-            status in (
-                'PendingNew',
-                'New',
-                'PartiallyFilled'
-            )
-            """,
-        ]
-        if account_ids:
-            conditions.append(f"""account_id in ('{"','".join(account_ids)}')""")
-
-        cur = self.execute(f"""
-            SELECT account_id, 
-                   sum((volume-filled_volume)*price*1.003) as frozen 
-            FROM orders
-            WHERE {' AND '.join(conditions)}
-            AND order_direction='Buy'
-            GROUP BY account_id ;
-            """)
-        cash_frozens = {
-            account_id: {"account_id": account_id, "frozen": 0}
-            for account_id in account_ids
-        }
-        cash_frozens.update({item["account_id"]: dict(item) for item in cur})
-        self.executemany(
-            f""" UPDATE positions
-                SET frozen=ROUND(:frozen,2) ,
-                    available=ROUND(volume-:frozen,2)
-                WHERE account_id=:account_id
-                AND symbol='CNY' 
-                AND settle_date={self.settle_date};
-            """,
-            list(cash_frozens.values()),
-        )
-        self.executemany(
-            f""" UPDATE accounts
-                SET frozen=ROUND(:frozen,2) ,
-                    available=ROUND(balance-:frozen,2)
-                WHERE account_id=:account_id 
-                AND settle_date={self.settle_date};
-            """,
-            list(cash_frozens.values()),
-        )
-
-    def update_symbol_position_frozens(self, account_ids: List[str]) -> None:
-        """更新cash的frozens"""
-        conditions = [
-            """ 
-                status in (
-                    'PendingNew', 
-                    'New',
-                    'PartiallyFilled'
-                ) 
-            """,
-            f"""created_dt<{self.settle_date}""",
-            f"""created_dt>{vxtime.today()}""",
-        ]
-        if account_ids:
-            conditions.append(f"""account_id in ('{"','".join(account_ids)}')""")
-
-        cur = self.execute(f"""
-                SELECT account_id, symbol, sum(volume-filled_volume) as frozen
-                FROM orders
-                WHERE {' AND '.join(conditions)}
-                AND order_direction='OrderDirection.Sell' 
-                GROUP BY account_id, symbol ;
-            """)
-        symbol_frozens = [dict(item) for item in cur]
-        self.execute(f"""
-                UPDATE positions
-                SET frozen=0.0,
-                    available=ROUND(volume,2)
-                WHERE account_id in ('{"','".join(account_ids)}')
-                AND allow_t0 = true
-                AND settle_date={self.settle_date}
-            """)
-        self.execute(f"""
-                UPDATE positions
-                SET frozen=0.0,
-                    available=ROUND(volume_his,2)
-                WHERE account_id in ('{"','".join(account_ids)}')
-                AND allow_t0 = false
-                AND settle_date={self.settle_date}
-            """)
-
-        self.executemany(
-            f"""
-                UPDATE positions
-                SET frozen=ROUND(:frozen,2),
-                    available=ROUND(volume-:frozen,2)
-                WHERE account_id=:account_id
-                AND symbol=:symbol
-                AND allow_t0 = true
-                AND settle_date={self.settle_date}
-            """,
-            symbol_frozens,
-        )
-        self.executemany(
-            f"""
-                UPDATE positions
-                SET frozen=ROUND(:frozen,2),
-                    available=ROUND(volume_his-:frozen,2)
-                WHERE account_id=:account_id
-                AND symbol=:symbol
-                AND allow_t0 = false
-                AND settle_date={self.settle_date}
-            """,
-            symbol_frozens,
-        )
-
-    def update_accountinfos(self, account_ids: List[str]) -> None:
-        if not account_ids:
-            account_ids = self.distinct(
-                "accounts", "account_id", settle_date=self.settle_date
-            )
-        accountinfos = []
-        cur_acc = self.find(
-            "accounts",
-            f"""account_id in ('{"','".join(account_ids)}')""",
-            settle_date=self._settle_date,
-        )
-        for accountinfo in cur_acc:
-            accountinfo.marketvalue = 0
-            accountinfo.fnl = 0
-            cur = self.find(
-                "positions",
-                account_id=accountinfo.account_id,
-                settle_date=self._settle_date,
-            )
-            for p in cur:
-                if p.symbol == "CNY":
-                    accountinfo.balance = p.marketvalue
-                    accountinfo.frozen = p.frozen
-                else:
-                    accountinfo.marketvalue += p.marketvalue
-                    accountinfo.fnl += p.fnl
-            accountinfos.append(accountinfo)
-        self.save("accounts", accountinfos)
-
-    def _handle_buy_position(self, trade: vxTrade) -> None:
-        filled_amount = trade.volume * trade.price + trade.commission
-        src_position = self.findone(
-            "positions",
-            account_id=trade.account_id,
-            symbol="CNY",
-            settle_date=self.settle_date,
-        )
-        src_position = vxCashPosition(src_position.message)
-        dst_position = self.findone(
-            "positions",
-            account_id=trade.account_id,
-            symbol=trade.symbol,
-            settle_date=self._settle_date,
-        )
-        if dst_position is None:
-            accountinfo = self.findone(
-                "accounts", account_id=trade.account_id, settle_date=self._settle_date
-            )
-            dst_position = vxPosition(
-                portfolio_id=accountinfo.portfolio_id,
-                account_id=trade.account_id,
-                symbol=trade.symbol,
-                security_type=vxMarketPreset(trade.symbol).security_type,
-                allow_t0=vxMarketPreset(trade.symbol).allow_t0,
-                settle_date=self._settle_date,
-            )
-        src_position = _sub_volume(src_position, filled_amount)
-        dst_position.volume_today += trade.volume
-        dst_position.cost += filled_amount
-        self.save("positions", src_position, dst_position)
-
-    def _handle_sell_position(self, trade: vxTrade) -> None:
-        filled_amount = trade.volume * trade.price - trade.commission
-        src_position = self.findone(
-            "positions",
-            account_id=trade.account_id,
-            symbol=trade.symbol,
-            settle_date=self.settle_date,
-        )
-
-        dst_position = self.findone(
-            "positions",
-            account_id=trade.account_id,
-            symbol="CNY",
-            settle_date=self.settle_date,
-        )
-        dst_position = vxCashPosition(dst_position.message)
-
-        src_position = _sub_volume(src_position, trade.volume)
-        src_position.cost -= filled_amount
-        dst_position.volume_today += filled_amount
-        self.save("positions", src_position, dst_position)
-
-    def update_order(self, broker_order: vxOrder) -> vxOrder:
-        """处理委托状态更新事件"""
-        if (not broker_order) or (not isinstance(broker_order, vxOrder)):
-            logger.error(
-                f"on_broker_order_status: 更新参数不正确，broker_order:{broker_order}"
-            )
-            return
-
-        vxorder = self.findone(
-            "orders", exchange_order_id=broker_order.exchange_order_id
-        )
-        if vxorder is None:
-            logger.error(f"找不到委托单:{broker_order.exchange_order_id}")
-            return None
-
-        if vxorder.status not in [
-            OrderStatus.PendingNew,
-            OrderStatus.New,
-            OrderStatus.PartiallyFilled,
-        ]:
-            logger.warning(
-                f"[忽略] 已存储的order已终止: {vxorder.status} //"
-                f" {vxorder.filled_volume} ===="
-                f" broker_order:{broker_order.status} // {broker_order.filled_volume} "
-            )
-            return None
-
-        if vxorder.filled_volume > broker_order.filled_volume:
-            logger.warning(
-                f"[忽略] 当前order: {vxorder.status} // {vxorder.filled_volume} ===="
-                f" broker_order:{broker_order.status} // {broker_order.filled_volume} "
-            )
-            return None
-
-        vxorder.filled_volume = broker_order.filled_volume
-        vxorder.filled_amount = broker_order.filled_amount
-        vxorder.reject_code = broker_order.reject_code
-        vxorder.reject_reason = broker_order.reject_reason
-        vxorder.status = broker_order.status
-
-        self.save("orders", vxorder)
-        if vxorder.order_direction == OrderDirection.Buy:
-            self.update_cash_position_frozens(account_ids=[vxorder.account_id])
-        else:
-            self.update_symbol_position_frozens(account_ids=[vxorder.account_id])
-        self.update_accountinfos([vxorder.account_id])
-        logger.info(f"[更新]委托状态: {vxorder}")
-        return vxorder
-
-    def update_trade(self, broker_trade: vxTrade) -> vxTrade:
-        """处理成交回报事件"""
-
-        if broker_trade and (not isinstance(broker_trade, vxTrade)):
-            logger.error(f"更新参数不正确，broker_trade:{broker_trade} ")
-            return
-
-        broker_order = self.findone(
-            "orders", exchange_order_id=broker_trade.exchange_order_id
-        )
-
-        if broker_order is None:
-            logger.debug(
-                "收到一个非法委托成交回报exchange_order_id :"
-                f" {broker_trade.exchange_order_id}"
-            )
-            return
-
-        # 更新account_id 和 order_id
-        broker_trade.account_id = broker_order.account_id
-        broker_trade.order_id = broker_order.order_id
-
-        try:
-            self.insert("trades", broker_trade)
-            logger.info(
-                f"插入成交回报trade_id({broker_trade.trade_id})@order_id({broker_order.order_id})"
-                f" volume({broker_trade.volume})"
-            )
-
-            self.update_order_filleds([broker_trade.account_id])
-            if broker_trade.order_direction == OrderDirection.Buy:
-                self.update_cash_position_frozens([broker_trade.account_id])
-                self._handle_buy_position(trade=broker_trade)
-            else:
-                self.update_symbol_position_frozens([broker_trade.account_id])
-                self._handle_sell_position(trade=broker_trade)
-
-            self.update_position_lasttrades(broker_trade)
-            self.update_accountinfos([broker_trade.account_id])
-            return broker_trade
-        except IntegrityError as e:
-            logger.error(f"插入数据已存在{broker_trade.trade_id}")
-            return None
-
-    def update_after_close(self) -> None:
-        """收盘后事件
-
-        1、持仓股票最新价格更新
-        2、更新账户信息
-
-        """
-        self.execute(
-            """UPDATE orders 
-                SET status='Expired' 
-                WHERE  status in ('PendingNew',"New",'Par')
-                AND created_dt > ?
-                AND created_dt < ?;
-            """,
-            (vxtime.today(), self.settle_date),
-        )
-        self.update_cash_position_frozens([])
-        self.update_symbol_position_frozens([])
-        self.update_accountinfos([])
-
-
-if __name__ == "__main__":
-    d = vxSQLiteAccountDB.connect("dist/test.db")
-    d.create_account(
-        portfolio_id="test", account_id="test", init_balance=300000, if_exists="delete"
-    )
-    # C(1)
-    broker_order = vxOrder(
-        account_id="test",
-        symbol="SHSE.600000",
-        order_direction=OrderDirection.Buy,
-        order_offset=OrderOffset.Open,
-        order_type="Limit",
-        exchange_order_id="xxxxx_exchange_order_id333",
-        volume=100,
-        price=10.2,
-    )
-    # print(broker_order)
-    d.update_order(broker_order)
-    broker_trade = vxTrade(
-        account_id="test1",
-        order_id="xxxxx_order_id1",
-        exchange_order_id="xxxxx_exchange_order_id333",
-        symbol="SHSE.600000",
-        volume=50,
-        price=10.1,
-        commission=5,
-        order_direction="Buy",
-        order_offset=OrderOffset.Open,
-        status="Trade",
-    )
-    d.update_trade(broker_trade)
-    print(broker_trade)
+"""基于sqlite3 的accountdb"""
+
+from sqlite3 import IntegrityError
+from typing import Dict, List, Union, Type
+from vxquant.model.typehint import DateTimeType
+from vxquant.model.contants import OrderOffset, OrderStatus, OrderDirection
+from vxquant.model.exchange import vxOrder, vxTrade, vxTick, vxCashPosition, vxPosition
+from vxquant.model.preset import vxMarketPreset
+from vxquant.accountdb.base import vxAccountDB
+from vxquant.exceptions import NoEnoughPosition
+from vxutils.database.sqlite import vxSQLiteDB
+from vxutils import logger, vxtime, combine_datetime, to_timestring
+
+
+def _sub_volume(
+    position: Union[vxCashPosition, vxPosition],
+    volume: Union[float, int],
+    allow_negative: bool = False,
+) -> Union[vxCashPosition, vxPosition]:
+    if volume > position.available and not allow_negative:
+        raise NoEnoughPosition(
+            f"{position.symbol}可用余额({position.available:,.2f})"
+            f" 小于需扣减{volume:,.2f}"
+        )
+
+    delta = position.volume_his - volume
+    position.volume_his = max(delta, 0)
+    position.volume_today += min(delta, 0)
+    return position
+
+
+class vxSQLiteAccountDB(vxAccountDB):
+    """账户数据库"""
+
+    def __init__(
+        self,
+        db_uri: str = None,
+        database_factory: Type[vxSQLiteDB] = None,
+    ) -> None:
+        super().__init__(db_uri, database_factory or vxSQLiteDB)
+
+    def update_position_lasttrades(
+        self, *prices: List[Union[Dict, vxTrade, vxTick]]
+    ) -> None:
+        if len(prices) == 1 and isinstance(prices[0], (list, tuple)):
+            prices = prices[0]
+
+        lasttrades = [
+            {
+                "symbol": price["symbol"],
+                "lasttrade": (
+                    price["lasttrade"] if "lasttrade" in price else price["price"]
+                ),
+                "created_dt": price["created_dt"],
+            }
+            for price in prices
+            if (price["lasttrade"] if "lasttrade" in price else price["price"]) > 0
+        ]
+        self.executemany(
+            f"""     
+            UPDATE `positions` as t
+            SET lasttrade=:lasttrade,
+                marketvalue=ROUND(t.volume * :lasttrade,2),
+                fnl = ROUND(t.volume * :lasttrade - t.cost,2),
+                updated_dt = :created_dt
+            WHERE t.symbol = :symbol
+            AND t.settle_date={self.settle_date};
+            """,
+            lasttrades,
+        )
+        cur = self.execute(f"""
+                SELECT  account_id,
+                        SUM(marketvalue) as marketvalue,
+                        SUM(fnl) as fnl
+                FROM positions
+                WHERE symbol !='CNY'
+                AND settle_date = {self.settle_date}
+                GROUP BY account_id;
+            """)
+        self.executemany(
+            f"""
+                UPDATE accounts
+                SET asset=ROUND(balance+:marketvalue,2),
+                    nav=ROUND(balance+:marketvalue - debt,2),
+                    marketvalue=ROUND(:marketvalue,2),
+                    today_profit = ROUND(balance+:marketvalue-nav_yd-deposit + withdraw,2),
+                    fnl=ROUND(:fnl,2),
+                    fund_nav=ROUND((balance+:marketvalue - debt)/fund_shares,4)
+                WHERE account_id = :account_id
+                AND settle_date= {self.settle_date};
+            """,
+            [dict(item) for item in cur],
+        )
+
+    def update_order_filleds(self, account_ids: List[str] = None) -> List[vxOrder]:
+        """更新order成交情况
+
+        Arguments:
+            account_ids {List[str]} -- 待更新的account_ids
+        """
+        conditions = [
+            """ 
+                status in (
+                    'PendingNew', 
+                    'New',
+                    'PartiallyFilled'
+                ) 
+            """,
+            f"""created_dt > {vxtime.today()}""",
+            f"""created_dt < {self._settle_date}""",
+        ]
+        if account_ids:
+            conditions.append(f""" account_id in ('{"' , '".join(account_ids)}') """)
+
+        cur = self.execute(f"""
+                SELECT  order_id,
+                        SUM(volume) as filled_volume, 
+                        SUM(volume*price) as filled_amount,
+                        SUM(commission) as commission
+                FROM trades
+                WHERE account_id in ('{"','".join(account_ids)}')
+                GROUP BY order_id
+            """)
+        filleds = {item["order_id"]: item for item in cur}
+        if not filleds:
+            return
+
+        cur = self.find("orders", f"""order_id in ('{"','".join(filleds.keys())}')""")
+        orders = []
+        for order in cur:
+            order.filled_volume = filleds[order.order_id].filled_volume
+            order.filled_amount = (
+                (
+                    filleds[order.order_id].filled_amount
+                    + filleds[order.order_id].commission
+                )
+                if order.order_direction.name == "Buy"
+                else (
+                    filleds[order.order_id].filled_amount
+                    - filleds[order.order_id].commission
+                )
+            )
+            order.status = (
+                "PartiallyFilled" if order.volume > order.filled_volume else "Filled"
+            )
+            orders.append(order)
+
+        if orders:
+            self.save("orders", orders)
+        return orders
+
+    def update_cash_position_frozens(self, account_ids: List[str]) -> None:
+        """更新cash的frozens"""
+
+        conditions = [
+            """
+            status in (
+                'PendingNew',
+                'New',
+                'PartiallyFilled'
+            )
+            """,
+        ]
+        if account_ids:
+            conditions.append(f"""account_id in ('{"','".join(account_ids)}')""")
+
+        cur = self.execute(f"""
+            SELECT account_id, 
+                   sum((volume-filled_volume)*price*1.003) as frozen 
+            FROM orders
+            WHERE {' AND '.join(conditions)}
+            AND order_direction='Buy'
+            GROUP BY account_id ;
+            """)
+        cash_frozens = {
+            account_id: {"account_id": account_id, "frozen": 0}
+            for account_id in account_ids
+        }
+        cash_frozens.update({item["account_id"]: dict(item) for item in cur})
+        self.executemany(
+            f""" UPDATE positions
+                SET frozen=ROUND(:frozen,2) ,
+                    available=ROUND(volume-:frozen,2)
+                WHERE account_id=:account_id
+                AND symbol='CNY' 
+                AND settle_date={self.settle_date};
+            """,
+            list(cash_frozens.values()),
+        )
+        self.executemany(
+            f""" UPDATE accounts
+                SET frozen=ROUND(:frozen,2) ,
+                    available=ROUND(balance-:frozen,2)
+                WHERE account_id=:account_id 
+                AND settle_date={self.settle_date};
+            """,
+            list(cash_frozens.values()),
+        )
+
+    def update_symbol_position_frozens(self, account_ids: List[str]) -> None:
+        """更新cash的frozens"""
+        conditions = [
+            """ 
+                status in (
+                    'PendingNew', 
+                    'New',
+                    'PartiallyFilled'
+                ) 
+            """,
+            f"""created_dt<{self.settle_date}""",
+            f"""created_dt>{vxtime.today()}""",
+        ]
+        if account_ids:
+            conditions.append(f"""account_id in ('{"','".join(account_ids)}')""")
+
+        cur = self.execute(f"""
+                SELECT account_id, symbol, sum(volume-filled_volume) as frozen
+                FROM orders
+                WHERE {' AND '.join(conditions)}
+                AND order_direction='OrderDirection.Sell' 
+                GROUP BY account_id, symbol ;
+            """)
+        symbol_frozens = [dict(item) for item in cur]
+        self.execute(f"""
+                UPDATE positions
+                SET frozen=0.0,
+                    available=ROUND(volume,2)
+                WHERE account_id in ('{"','".join(account_ids)}')
+                AND allow_t0 = true
+                AND settle_date={self.settle_date}
+            """)
+        self.execute(f"""
+                UPDATE positions
+                SET frozen=0.0,
+                    available=ROUND(volume_his,2)
+                WHERE account_id in ('{"','".join(account_ids)}')
+                AND allow_t0 = false
+                AND settle_date={self.settle_date}
+            """)
+
+        self.executemany(
+            f"""
+                UPDATE positions
+                SET frozen=ROUND(:frozen,2),
+                    available=ROUND(volume-:frozen,2)
+                WHERE account_id=:account_id
+                AND symbol=:symbol
+                AND allow_t0 = true
+                AND settle_date={self.settle_date}
+            """,
+            symbol_frozens,
+        )
+        self.executemany(
+            f"""
+                UPDATE positions
+                SET frozen=ROUND(:frozen,2),
+                    available=ROUND(volume_his-:frozen,2)
+                WHERE account_id=:account_id
+                AND symbol=:symbol
+                AND allow_t0 = false
+                AND settle_date={self.settle_date}
+            """,
+            symbol_frozens,
+        )
+
+    def update_accountinfos(self, account_ids: List[str]) -> None:
+        if not account_ids:
+            account_ids = self.distinct(
+                "accounts", "account_id", settle_date=self.settle_date
+            )
+        accountinfos = []
+        cur_acc = self.find(
+            "accounts",
+            f"""account_id in ('{"','".join(account_ids)}')""",
+            settle_date=self._settle_date,
+        )
+        for accountinfo in cur_acc:
+            accountinfo.marketvalue = 0
+            accountinfo.fnl = 0
+            cur = self.find(
+                "positions",
+                account_id=accountinfo.account_id,
+                settle_date=self._settle_date,
+            )
+            for p in cur:
+                if p.symbol == "CNY":
+                    accountinfo.balance = p.marketvalue
+                    accountinfo.frozen = p.frozen
+                else:
+                    accountinfo.marketvalue += p.marketvalue
+                    accountinfo.fnl += p.fnl
+            accountinfos.append(accountinfo)
+        self.save("accounts", accountinfos)
+
+    def _handle_buy_position(self, trade: vxTrade) -> None:
+        filled_amount = trade.volume * trade.price + trade.commission
+        src_position = self.findone(
+            "positions",
+            account_id=trade.account_id,
+            symbol="CNY",
+            settle_date=self.settle_date,
+        )
+        src_position = vxCashPosition(src_position.message)
+        dst_position = self.findone(
+            "positions",
+            account_id=trade.account_id,
+            symbol=trade.symbol,
+            settle_date=self._settle_date,
+        )
+        if dst_position is None:
+            accountinfo = self.findone(
+                "accounts", account_id=trade.account_id, settle_date=self._settle_date
+            )
+            dst_position = vxPosition(
+                portfolio_id=accountinfo.portfolio_id,
+                account_id=trade.account_id,
+                symbol=trade.symbol,
+                security_type=vxMarketPreset(trade.symbol).security_type,
+                allow_t0=vxMarketPreset(trade.symbol).allow_t0,
+                settle_date=self._settle_date,
+            )
+        src_position = _sub_volume(src_position, filled_amount)
+        dst_position.volume_today += trade.volume
+        dst_position.cost += filled_amount
+        self.save("positions", src_position, dst_position)
+
+    def _handle_sell_position(self, trade: vxTrade) -> None:
+        filled_amount = trade.volume * trade.price - trade.commission
+        src_position = self.findone(
+            "positions",
+            account_id=trade.account_id,
+            symbol=trade.symbol,
+            settle_date=self.settle_date,
+        )
+
+        dst_position = self.findone(
+            "positions",
+            account_id=trade.account_id,
+            symbol="CNY",
+            settle_date=self.settle_date,
+        )
+        dst_position = vxCashPosition(dst_position.message)
+
+        src_position = _sub_volume(src_position, trade.volume)
+        src_position.cost -= filled_amount
+        dst_position.volume_today += filled_amount
+        self.save("positions", src_position, dst_position)
+
+    def update_order(self, broker_order: vxOrder) -> vxOrder:
+        """处理委托状态更新事件"""
+        if (not broker_order) or (not isinstance(broker_order, vxOrder)):
+            logger.error(
+                f"on_broker_order_status: 更新参数不正确，broker_order:{broker_order}"
+            )
+            return
+
+        vxorder = self.findone(
+            "orders", exchange_order_id=broker_order.exchange_order_id
+        )
+        if vxorder is None:
+            logger.debug(f"找不到委托单:{broker_order.exchange_order_id}")
+            return None
+
+        if vxorder.status not in [
+            OrderStatus.PendingNew,
+            OrderStatus.New,
+            OrderStatus.PartiallyFilled,
+        ] and broker_order.status in [
+            OrderStatus.PendingNew,
+            OrderStatus.New,
+            OrderStatus.PartiallyFilled,
+        ]:
+            logger.warning(
+                f"[忽略] 已存储的order已终止: {vxorder.status} //"
+                f" {vxorder.filled_volume} ===="
+                f" broker_order:{broker_order.status} // {broker_order.filled_volume} "
+            )
+            return None
+
+        if vxorder.filled_volume > broker_order.filled_volume and broker_order.status:
+            logger.warning(
+                f"[忽略] 当前order: {vxorder.status} // {vxorder.filled_volume} ===="
+                f" broker_order:{broker_order.status} // {broker_order.filled_volume} "
+            )
+            return None
+
+        vxorder.filled_volume = broker_order.filled_volume
+        vxorder.filled_amount = broker_order.filled_amount
+        vxorder.reject_code = broker_order.reject_code
+        vxorder.reject_reason = broker_order.reject_reason
+        vxorder.status = broker_order.status
+
+        self.save("orders", vxorder)
+        if vxorder.order_direction == OrderDirection.Buy:
+            self.update_cash_position_frozens(account_ids=[vxorder.account_id])
+        else:
+            self.update_symbol_position_frozens(account_ids=[vxorder.account_id])
+        self.update_accountinfos([vxorder.account_id])
+        logger.info(f"[更新]委托状态: {vxorder}")
+        return vxorder
+
+    def update_trade(self, broker_trade: vxTrade) -> vxTrade:
+        """处理成交回报事件"""
+
+        if broker_trade and (not isinstance(broker_trade, vxTrade)):
+            logger.error(f"更新参数不正确，broker_trade:{broker_trade} ")
+            return None, None
+
+        broker_order = self.findone(
+            "orders", exchange_order_id=broker_trade.exchange_order_id
+        )
+
+        if broker_order is None:
+            logger.debug(
+                "收到一个非法委托成交回报exchange_order_id :"
+                f" {broker_trade.exchange_order_id}"
+            )
+            return None, None
+
+        # 更新account_id 和 order_id
+        broker_trade.account_id = broker_order.account_id
+        broker_trade.order_id = broker_order.order_id
+
+        try:
+            self.insert("trades", broker_trade)
+            logger.info(
+                f"插入成交回报trade_id({broker_trade.trade_id})@order_id({broker_order.order_id})"
+                f" volume({broker_trade.volume})"
+            )
+
+            vxorders = self.update_order_filleds([broker_trade.account_id])
+            vxorder = vxorders[0] if vxorders else None
+            if broker_trade.order_direction == OrderDirection.Buy:
+                self.update_cash_position_frozens([broker_trade.account_id])
+                self._handle_buy_position(trade=broker_trade)
+            else:
+                self.update_symbol_position_frozens([broker_trade.account_id])
+                self._handle_sell_position(trade=broker_trade)
+
+            self.update_position_lasttrades(broker_trade)
+            self.update_accountinfos([broker_trade.account_id])
+            return broker_trade, vxorder
+        except IntegrityError as e:
+            logger.error(f"插入数据已存在{broker_trade.trade_id}")
+            return None, None
+
+    def update_after_close(self) -> None:
+        """收盘后事件
+
+        1、持仓股票最新价格更新
+        2、更新账户信息
+
+        """
+        self.execute(
+            """UPDATE orders 
+                SET status='Expired' 
+                WHERE  status in ('PendingNew',"New",'PartiallyFilled')
+                AND created_dt > ?
+                AND created_dt < ?;
+            """,
+            (vxtime.today(), self.settle_date),
+        )
+        self.update_cash_position_frozens([])
+        self.update_symbol_position_frozens([])
+        self.update_accountinfos([])
+
+        accountinfos = list(self.find("accounts"))
+        self.save("history_accounts", *accountinfos)
+        logger.info(f"保存账户信息: {len(accountinfos)}个")
+
+        positions = list(self.find("positions"))
+        self.save("history_positions", *positions)
+        logger.info(f"保存持仓信息: {len(positions)}个")
+
+    def update_settle_date(self, settle_date: DateTimeType) -> None:
+        """更新结算日期
+
+        Arguments:
+            settle_date {DateTimeType} -- 结算日期
+        """
+        if settle_date is None:
+            settle_date = vxtime.today("23:59:59")
+        else:
+            settle_date = combine_datetime(settle_date, "23:59:59")
+
+        if settle_date <= self.settle_date:
+            logger.error(
+                f"新设置的结算日期: {to_timestring(settle_date,'%Y-%m-%d')}"
+                f"小于当前结算日期({to_timestring(self.settle_date,'%Y-%m-%d')})"
+            )
+            return
+
+        logger.info(
+            f"结算日期：{to_timestring(self.settle_date,'%Y-%m-%d')} ==>"
+            f" {to_timestring(settle_date,'%Y-%m-%d')} ..."
+        )
+        self.delete("positions", volume=0)
+        self.execute(
+            "UPDATE positions SET volume_today=0, volume_his=volume,  settle_date=? ;",
+            (settle_date,),
+        )
+
+        self._settle_date = settle_date
+        self.update_cash_position_frozens([])
+        self.update_symbol_position_frozens([])
+        self.update_accountinfos([])
+        self.execute(
+            """ UPDATE accounts 
+                SET today_profit=0,
+                    deposit=0,
+                    withdraw=0,
+                    asset_yd=asset,
+                    nav_yd=nav,
+                    fund_nav_yd=fund_nav, 
+                    settle_date=? ;
+            """,
+            (settle_date,),
+        )
```

### Comparing `vxquant-2023.4.1/src/vxquant/cli/__init__.py` & `vxquant-2023.5.13/src/vxquant/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/cli/base.py` & `vxquant-2023.5.13/src/vxquant/cli/base.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/config.py` & `vxquant-2023.5.13/src/vxquant/config.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,203 +1,188 @@
-"""配置文件"""
-import json
-from pathlib import Path
-from typing import Union
-from vxquant.apis import vxMdAPI, vxTdAPI, vxTeller
-from vxsched import vxContext, vxscheduler
-from vxutils import logger, vxWrapper
-
-
-__default_config__ = {
-    "custom_context": {},
-    "init_privoder_context": {
-        "class": "",
-        "params": {},
-    },
-    "mdapi": {},
-    "tdapi": {"channel": "default", "providers": {}},
-    "accountdb": {
-        "class": "vxquant.accountdb.sqlitedb.vxSQLiteAccountDB",
-        "params": {"db_uri": "data/vxquant.db"},
-        "accounts": [
-            {
-                "portfolio_id": "default",
-                "account_id": "default",
-                "init_balance": 1_000_000.00,
-                "if_exists": "ignore",
-                "channel": "default",
-            },
-        ],
-    },
-    "notify": {},
-    "preset_events": {
-        "before_trade": "09:15:00",
-        "on_trade": "09:30:00",
-        "noon_break_start": "11:30:00",
-        "noon_break_end": "13:00:00",
-        "before_close": "14:45:00",
-        "on_close": "14:55:00",
-        "after_close": "15:30:00",
-        "on_settle": "16:30:00",
-    },
-}
-
-
-class vxQuantConfig(vxContext):
-    """vxQuant配置文件"""
-
-    _default_config: dict = __default_config__
-
-    def __init__(self, **kwargs):
-        super().__init__(**kwargs)
-
-    def load_json(
-        self, config_file: Union[str, Path] = "etc/config.json", encoding="utf-8"
-    ) -> None:
-        """加载配置文件
-
-        Keyword Arguments:
-            config_file {Union[str,Path]} -- 配置文件路径 (default: {"etc/config.json"})
-
-        Example:
-
-            {
-                "custom_context":{
-                        "trader": "C:\\Program Files\\miniQMT\\",
-                        ...
-                },
-                "mdapi": {
-                    "current": {
-                        "class": "vxquant.providers.miniqmt.vxMiniQMTHQProvider",
-                        "params": {}
-                    },
-                    ...
-                },
-                "tdapi": {
-                    "channel" :"channel_name1",
-
-                    "providers":{
-                        "current": {
-                            "class": "vxquant.providers.miniqmt.vxMiniQMTHQProvider",
-                            "params": {}
-                        },
-                        "order_batch": {
-                            "class":"vxquant.providers.miniqmt.vxMiniQMTOrderBatchProvider",
-                            "params": {}
-                        },
-                        ...
-                    }
-                },
-                "accountdb": {
-                    "class": "vxquant.accountdb.sqlitedb.vxSQLiteAccountDB",
-                    "params": {"db_uri": "data/vxquant.db"},
-                    "accounts": [
-                        {
-                            "portfolio_id": "default",
-                            "account_id": "default",
-                            "init_balance": 4000000,
-                            "if_exists": "ignore",
-                            "channel": "default",
-                        },
-                    ],
-                },
-                "notify": {},
-                "cachedb": "~/.data/vxcache.db"
-            }
-
-        """
-        try:
-            with open(config_file, "r", encoding=encoding) as fp:
-                kwargs = json.load(fp)
-        except OSError:
-            kwargs = {}
-
-        self.update(kwargs)
-        logger.info(f"通过{config_file}初始化context完成.")
-
-    def create_context(self, **kwargs) -> vxContext:
-        """创建context"""
-
-        context = vxContext(kwargs)
-
-        if "accountdb" not in kwargs:
-            try:
-                context.accountdb = vxWrapper.init_by_config(self.accountdb.to_dict())
-                logger.info(f"初始化账户数据库: {context.accountdb}")
-            except Exception as e:
-                logger.error(f"初始化账户数据库失败: {e}")
-                context.accountdb = None
-
-        if "scheduler" not in kwargs:
-            context.scheduler = vxscheduler
-
-        for mod_name, mod_config in self.custom_context.items():
-            try:
-                context[mod_name] = vxWrapper.init_by_config(mod_config.to_dict())
-                logger.info(f"初始化{mod_name}: {kwargs[mod_name]}")
-            except Exception as e:
-                logger.error(f"初始化{mod_name}失败: {e}")
-
-        if "init_privoder_context" in self.keys():
-            init_func = vxWrapper.init_by_config(self.init_privoder_context.to_dict())
-            context = init_func(context=context, **self.init_privoder_context.params)
-
-        if "mdapi" in self.keys():
-            try:
-                context.mdapi = vxMdAPI(**self.mdapi.to_dict())
-                context.mdapi.set_context(context)
-                vxticks = context.mdapi.current("SHSE.000300")
-                logger.info(
-                    f"测试实时行情接口: {'SHSE.000300'} --"
-                    f" {vxticks['SHSE.000300'].lasttrade:,.2f}"
-                )
-                cal = context.mdapi.calender(start_date="2005-01-01")
-
-            except Exception as e:
-                logger.error(f"初始化行情接口失败: {e}")
-                context.mdapi = vxMdAPI()
-                logger.info(f"使用默认行情接口: {context.mdapi}")
-
-        if "tdapi" in self.keys():
-            try:
-                context.tdapi = vxTdAPI(**self.tdapi.providers.to_dict())
-                context.tdapi.set_context(context)
-                accountinfo = context.tdapi.get_account()
-                logger.info(
-                    f"测试交易接口:{accountinfo.account_id} 账户余额:"
-                    f" {accountinfo.nav:,.2f}元)"
-                )
-
-                context.teller = vxTeller(
-                    mdapi=context.mdapi, accountdb=context.accountdb
-                )
-                context.teller.register_scheduler(vxscheduler)
-                context.teller.add_channel(self.tdapi.channel, context.tdapi)
-            except Exception as e:
-                logger.error(f"初始化交易接口失败: {e}")
-                context.tdapi = None
-                context.teller = None
-
-        try:
-            if context.teller:
-                for account_config in self.accountdb.accounts:
-                    context.teller.create_account(**account_config.to_dict())
-                    logger.info(
-                        f"{account_config.portfolio_id} 创建账户:"
-                        f" {account_config.account_id} 通道: {account_config.channel}"
-                    )
-            else:
-                logger.warning(f"没有交易接口,不创建账户.")
-        except Exception as e:
-            logger.error(f"初始化账户失败: {e},账户配置: {self.accountdb.accounts}")
-
-        return context
-
-
-vxQCONFIG = vxQuantConfig()
-
-
-if __name__ == "__main__":
-    vxQCONFIG.load_json()
-    context = vxQCONFIG.create_context()
-    print(context.mdapi.current("SHSE.000300"))
-    print(context.mdapi.calendar(start_date="2020-01-01", end_date="2023-01-31"))
+"""配置文件"""
+import json
+from pathlib import Path
+from typing import Union
+from vxquant.apis import vxMdAPI, vxTdAPI, vxTeller, vxTellerAPI
+from vxsched import vxContext, vxscheduler, vxDailyTrigger
+from vxutils import logger, vxWrapper, vxtime
+
+
+__default_config__ = {
+    "custom_context": {},
+    "mdapi": {},
+    "tdapi": {"channel": "default", "providers": {}},
+    "tdapis": {},
+    "accountdb": {
+        "db_uri": "data/vxquant.db",
+        "accounts": [
+            {
+                "portfolio_id": "default",
+                "account_id": "default",
+                "init_balance": 1_000_000.00,
+                "if_exists": "ignore",
+                "channel": "default",
+            },
+        ],
+    },
+    "notify": {},
+    "preset_events": {
+        "before_trade": "09:15:00",
+        "on_trade": "09:30:00",
+        "noon_break_start": "11:30:00",
+        "noon_break_end": "13:00:00",
+        "before_close": "14:45:00",
+        "on_close": "14:55:00",
+        "after_close": "15:30:00",
+        "on_settle": "16:30:00",
+    },
+}
+
+
+class vxQuantConfig(vxContext):
+    """vxQuant配置文件"""
+
+    _default_config: dict = __default_config__
+
+    def __init__(self, **kwargs):
+        super().__init__(self._default_config, **kwargs)
+
+    def load_json(
+        self, config_file: Union[str, Path] = "etc/config.json", encoding="utf-8"
+    ) -> None:
+        """加载配置文件
+
+        Keyword Arguments:
+            config_file {Union[str,Path]} -- 配置文件路径 (default: {"etc/config.json"})
+
+        Example:
+
+            {
+                "custom_context": {},
+                "mdapi": {},
+                "tdapi": {"channel": "default", "providers": {}},
+                "tdapis": {},
+                "accountdb": {
+                    "db_uri": "data/vxquant.db",
+                    "accounts": [
+                        {
+                            "portfolio_id": "default",
+                            "account_id": "default",
+                            "init_balance": 1_000_000.00,
+                            "if_exists": "ignore",
+                            "channel": "default",
+                        },
+                    ],
+                },
+                "notify": {},
+                "preset_events": {
+                    "before_trade": "09:15:00",
+                    "on_trade": "09:30:00",
+                    "noon_break_start": "11:30:00",
+                    "noon_break_end": "13:00:00",
+                    "before_close": "14:45:00",
+                    "on_close": "14:55:00",
+                    "after_close": "15:30:00",
+                    "on_settle": "16:30:00",
+                },
+
+            }
+        """
+        try:
+            with open(config_file, "r", encoding=encoding) as fp:
+                kwargs = json.load(fp)
+        except OSError:
+            kwargs = {}
+
+        self.update(kwargs)
+        logger.info(f"通过{config_file}初始化context完成.")
+
+    def create_context(self, **kwargs) -> vxContext:
+        """创建context"""
+
+        context = vxContext(**kwargs)
+
+        if "sched" not in kwargs:
+            context.sched = vxscheduler
+            logger.info("初始化 sched 完成")
+            # context.scheduler = vxscheduler
+        context.sched.submit_event("day_begin", trigger=vxDailyTrigger("09:10:00"))
+        if vxtime.today("09:10:00") < vxtime.now() < vxtime.today("15:00:00"):
+            context.sched.submit_event("day_begin")
+
+        for mod_name, mod_config in self.custom_context.items():
+            try:
+                context[mod_name] = vxWrapper.init_by_config(mod_config.to_dict())
+                logger.info(f"初始化{mod_name}: {kwargs[mod_name]}")
+            except Exception as e:
+                logger.error(f"初始化{mod_name}失败: {e}")
+
+        if "mdapi" in self.keys():
+            try:
+                context.mdapi = vxMdAPI(**self.mdapi.to_dict())
+                context.mdapi.set_context(context)
+                vxticks = context.mdapi.current("SHSE.000300")
+                logger.info(
+                    f"测试实时行情接口: {'SHSE.000300'} --"
+                    f" {vxticks['SHSE.000300'].lasttrade:,.2f}"
+                )
+                # todo: 从配置文件中读取日历，并且更新到vxtime的holidays中
+                cal = context.mdapi.calendar(start_date="2005-01-01")
+                logger.info(f"获取交易日历: {len(cal)}天")
+                logger.warning("初始化mdapi 完成")
+
+            except Exception as e:
+                logger.error(f"初始化行情接口失败: {e}")
+                context.mdapi = vxMdAPI()
+                logger.info(f"使用默认行情接口: {context.mdapi}")
+
+        if "tdapis" in self.keys():
+            context.channels = {}
+
+            for channel_name, channel_config in self.tdapis.items():
+                try:
+                    tdapi = vxTdAPI(**channel_config.to_dict())
+                    tdapi.set_context(context)
+                    accountinfo = tdapi.get_account()
+                    context.channels[channel_name] = tdapi
+                    logger.info(
+                        f"下单通道 {channel_name}测试交易接口:"
+                        f" {accountinfo.account_id} 账户余额: {accountinfo.nav:,.2f}元)"
+                    )
+                    logger.warning("初始化tdapi 完成")
+                except Exception as e:
+                    logger.info(f"下单通道 {channel_name} 初始化交易接口失败: {e}", exc_info=True)
+                    context.channels.pop(channel_name)
+
+        try:
+            if "accountdb" in self.keys():
+                db_uri = self.accountdb.db_uri
+                context.teller = vxTellerAPI(db_uri=db_uri, mdapi=context.mdapi)
+                context.teller.register_scheduler(context.sched)
+                for channel_name, tdapi in context.channels.items():
+                    context.teller.add_channel(channel_name, tdapi)
+
+                for account_config in self.accountdb.accounts:
+                    context.teller.create_account(**account_config.to_dict())
+                    logger.info(
+                        f"{account_config.portfolio_id} 创建账户:"
+                        f" {account_config.account_id} 通道: {account_config.channel}"
+                    )
+                    context.sched.trigger_events()
+                # context.teller.register_scheduler(context.sched)
+
+            else:
+                logger.warning("没有交易接口,不创建账户.")
+        except Exception as e:
+            logger.error(f"初始化账户失败: {e},账户配置: {self.accountdb.accounts}", exc_info=True)
+
+        return context
+
+
+QCONFIG = vxQuantConfig()
+
+
+if __name__ == "__main__":
+    QCONFIG.load_json()
+    context = QCONFIG.create_context()
+    print(context.mdapi.current("SHSE.000300"))
+    print(context.mdapi.calendar(start_date="2020-01-01", end_date="2023-01-31"))
```

### Comparing `vxquant-2023.4.1/src/vxquant/exceptions.py` & `vxquant-2023.5.13/src/vxquant/exceptions.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/factor/builder.py` & `vxquant-2023.5.13/src/vxquant/factor/builder.py`

 * *Files 15% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 import polars as pl
 from tqdm import tqdm
 from typing import Dict, List, Union
 from vxquant.model.typehint import DateTimeType
 from vxquant.model.instruments import vxInstruments
 from vxquant.apis import vxMdAPI
 from vxquant.factor.expr.ops import *
-from vxquant.factor.loader import vxLocalDataLoader, vxDataLoader
-from vxutils import vxtime, to_datetime, logger
+from vxquant.factor.loader import vxLocalDataLoader
+from vxutils import vxtime, to_datetime, logger, vxWrapper
 
 
 def to_expr(name: str, feature: str = None, groupby: str = None) -> pl.Expr:
     """将字符串公式转化为pl的表达式格式
 
     Arguments:
         name {str} -- 名字
@@ -53,80 +53,102 @@
         else eval(feature).over(groupby).alias(name)
     )
 
 
 class vxFactorBuilder:
     def __init__(
         self,
-        loader: vxDataLoader,
-        instruments: Union[str, vxInstruments] = "cnstocks",
+        mdapi: vxMdAPI,
+        instruments: Union[str, vxInstruments, List] = "cnstocks",
         start_date: DateTimeType = None,
         end_date: DateTimeType = None,
-        period: str = "day",
-        sec_type: str = "STOCK",
+        freq: str = "day",
     ):
-        if isinstance(instruments, str):
-            instruments = loader.load_instruments(instruments)
-
         self.start_date = to_datetime(start_date or "2005-01-01")
         self.end_date = to_datetime(end_date or vxtime.today())
-        self._loader = loader
-        self._instruments = instruments
 
-        self._features = self._loader.load_features(period, sec_type).filter(
-            (pl.col("symbol").is_in(self._instruments.all_instruments()))
-            & (pl.col("trade_date").is_between(self.start_date, self.end_date))
+        if isinstance(instruments, str):
+            instruments = mdapi.instruments(instruments)
+        if isinstance(instruments, list):
+            instruments = vxInstruments("default").update_components(
+                instruments, start_date
+            )
+
+        self._mdapi = vxWrapper.init_by_config(mdapi) if mdapi else vxMdAPI()
+        self._instruments = instruments
+        self._instruments_filter = None
+        self._features = self._mdapi.features(
+            instruments=self._instruments,
+            start_date=self.start_date,
+            end_date=self.end_date,
+            freq=freq,
         )
-        logger.info(f"加载特征数据: {self._features.fetch(30)}")
+
+        logger.info(f"加载特征数据: {self._features.columns} ")
 
     def exclude_instruments(
         self, instruments: Union[str, vxInstruments]
     ) -> "vxFactorBuilder":
         """排除股票池中的股票
 
         Arguments:
             instruments {vxInstruments} -- 股票池
 
         Returns:
             vxFactorBuilder -- _description_
         """
         if isinstance(instruments, str):
-            instruments = self._loader.load_instruments(instruments)
+            instruments = self._mdapi.instruments(instruments)
 
         self._instruments.difference(instruments)
+        self._instruments_filter = None
         logger.info(f"剔除股票池: {instruments.name}")
         return self
 
     @property
-    def _instruments_filter(self) -> pl.DataFrame:
-        trade_dates = self._loader.load_calendar()
-        trade_dates = trade_dates.filter(
-            trade_dates.is_between(self.start_date, self.end_date)
-        )["trade_date"]
-        instruments_filters = []
-        instruments_rows = []
-        cnt = 0
-        for trade_date in tqdm(trade_dates, f"构建股票池过滤器{self._instruments.name}"):
-            available_symbols = self._instruments.list_instruments(trade_date)
-            instruments_rows.extend(
-                [
-                    {"trade_date": trade_date, "symbol": symbol, "mask": True}
-                    for symbol in available_symbols
-                ]
+    def instruments_filter(self) -> pl.DataFrame:
+        """股票池过滤器"""
+        if self._instruments_filter is None:
+            self._instruments_filter = self.build_instruments_filter()
+        return self._instruments_filter
+
+    def build_instruments_filter(self) -> pl.DataFrame:
+        """构建股票池过滤器
+
+        Returns:
+            pl.DataFrame -- _description_
+        """
+        trade_dates = self._mdapi.calendar(
+            start_date=self.start_date, end_date=self.end_date
+        )
+        instruments_filters = [
+            pl.DataFrame(
+                {"symbol": self._instruments.list_instruments(trade_date)}
+            ).select(
+                pl.lit(trade_date).alias("trade_date"),
+                pl.col("symbol"),
+                pl.lit(True).alias("mask"),
             )
-            cnt += len(available_symbols)
-            if cnt > 100_000:
-                instruments_filters.append(pl.DataFrame(instruments_rows))
-                instruments_rows = []
-                cnt = 0
-        if instruments_rows:
-            instruments_filters.append(pl.DataFrame(instruments_rows))
+            for trade_date in tqdm(
+                trade_dates, f"构建股票池过滤器{self._instruments.name}"
+            )
+        ]
 
         return pl.concat(instruments_filters)
 
+    def build_industry_factor_matrix(self) -> pl.DataFrame:
+        """生成行业因子矩阵
+
+        Returns:
+            pl.DataFrame -- industry_factor_matrix 行业因子矩阵
+        """
+        trade_dates = self._mdapi.calendar(
+            start_date=self.start_date, end_date=self.end_date
+        )
+
     def build_on_timeseries(self, **factor_exprs: Dict[str, str]) -> "vxFactorBuilder":
         """基于时序构建因子
 
         Arguments:
             factor_exprs {dict} -- 因子定义表达式如: MA20="Mean($close,20)",EMA20="EMA($close, 20)" ...
 
         Returns:
@@ -160,40 +182,75 @@
 
         return self
 
     def collect(self, *factor_names: List[str]) -> pl.DataFrame:
         if len(factor_names) == 1 and isinstance(factor_names[0], list):
             factor_names = factor_names[0]
 
+        # factor_names = set(factor_names)
+        if "trade_date" in factor_names:
+            factor_names.remove("trade_date")
+        if "symbol" in factor_names:
+            factor_names.remove("symbol")
+
         factor_cols = (
-            pl.col(set("trade_date", "symbol", *factor_names))
+            pl.col("trade_date", "symbol", *factor_names)
             if factor_names
             else pl.col("*")
         )
-        instruments_filter = self._instruments_filter
-        with vxtime.timeit("计算因子...", show_title=True):
-            features = self._features.collect()
-        logger.info(f"features: {features.tail(5)}")
+
+        # factor_cols = pl.col(factor_names) if factor_names else pl.col("*")
+
+        if isinstance(self._features, pl.LazyFrame):
+            with vxtime.timeit("计算因子...", show_title=True):
+                features = self._features.collect()
+            logger.debug(f"features: {features.tail(5)}")
+        else:
+            features = self._features
 
         with vxtime.timeit("过滤股票池..."):
-            return instruments_filter.join(
-                features, on=["trade_date", "symbol"], how="left"
-            ).select(factor_cols)
+            return (
+                self.instruments_filter.join(
+                    features, on=["trade_date", "symbol"], how="inner"
+                )
+                .filter("mask")
+                .select(factor_cols)
+            )
+
+    def normalize(self, factor_names: List[str]) -> "vxFactorBuilder":
+        """标准化"""
 
 
 if __name__ == "__main__":
-    loader = vxLocalDataLoader("/Volumes/work/quant/collector/data")
-    df = loader.load_calendar()
-    print(
-        df.filter(df.is_between(to_datetime("2023-01-04"), to_datetime("2023-03-01")))
-    )
+    import alphalens
+
+    mdapi = vxMdAPI()
+    cnstocks = mdapi.instruments("cnstocks")
+    f = mdapi.features(cnstocks, "2005-01-01", "2023-3-01")
+    print(f.groupby("is_trading").count())
+    vxtime.sleep(2)
+
+    fbuilder = vxFactorBuilder(mdapi, cnstocks, "2005-01-04", "2023-03-01")
 
-    cnstock = loader.load_instruments("cnstocks")
-    fbuilder = vxFactorBuilder(loader, "cnstocks", "2022-01-04", "2023-03-01")
+    # print(fbuilder._instruments_filter.filter(pl.col("mask")))
     # fbuilder.exclude_instruments("newstock")
-    # print(fbuilder._instruments_filter)
-    # fbuilder.build_on_timeseries(
-    #    vxAlpha001="EMA(($close/$yclose)/$amount,20)/Std(($close/$yclose)/$amount,20)"
-    # )
-    factor_data = fbuilder.collect()
-    # factor_data.write_parquet("./dist/factor.parquet")
+    # print(fbuilder._instruments_filter.filter(pl.col("mask")))
+    fbuilder.build_on_timeseries(
+        STO="1/MA($turnover_rate,21)+1/MA($turnover_rate,63)+1/MA($turnover_rate,63*4)",
+        VMOM="MA( $close / Ref($close,1) / $turnover_rate, 21)",
+        # MA20="EMA($close,20)",
+    )
+    factor_data = fbuilder.collect("is_trading", "STO", "VMOM")
+    factor_data.drop_nulls().write_csv("./dist/factor.csv")
+    factor_data = (
+        factor_data.drop_nulls().select(["trade_date", "symbol", "STO"]).to_pandas()
+    )
+    factor_data = factor_data.set_index(["trade_date", "symbol"])
     print(factor_data)
+    # print(factor_data.filter(pl.col("STO").is_not_null()))
+    prices = fbuilder.collect("open").to_pandas()
+    prices = prices.set_index(["trade_date"])
+    print(prices.unstack())
+    # data = alphalens.utils.get_clean_factor_and_forward_returns(
+    #    factor=factor_data, prices=prices, quantiles=5, periods=(1, 5, 20)
+    # )
+    # print(data)
```

### Comparing `vxquant-2023.4.1/src/vxquant/factor/expr/functions.py` & `vxquant-2023.5.13/src/vxquant/factor/expr/functions.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/factor/expr/ops.py` & `vxquant-2023.5.13/src/vxquant/factor/expr/ops.py`

 * *Files 5% similar despite different names*

```diff
@@ -173,14 +173,42 @@
     ----------
     Expression
         a feature instance with rolling average
     """
     return feature.rolling_mean(N)
 
 
+SMA = MA = Mean
+
+
+def EWM(feature: Feature, N: int, halflife: int = None) -> Feature:
+    """Exponential Weighted Mean (EWMA)
+
+    Parameters
+    ----------
+    feature : Expression
+        feature instance
+    N : int
+        rolling window size
+    halflife int
+        halflife (default: {None})
+
+    Returns
+    ----------
+    Expression
+        a feature instance with rolling average
+    """
+    if halflife is not None:
+        w = np.exp(np.log(0.5) / halflife * np.arange(N))[::-1]
+        w = w / w.sum()
+        return feature.rolling_mean(N, weights=w)
+
+    return feature.rolling_mean(N)
+
+
 def Sum(feature: Feature, N: int) -> Feature:
     """Rolling Sum
 
     Parameters
     ----------
     feature : Expression
         feature instance
```

### Comparing `vxquant-2023.4.1/src/vxquant/factor/loader.py` & `vxquant-2023.5.13/src/vxquant/factor/loader.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,194 +1,200 @@
-"""数据加载器"""
-
-from pathlib import Path
-from typing import Union, List
-import polars as pl
-from vxquant.model.contants import SecType
-from vxquant.model.typehint import DateTimeType
-from vxquant.model.instruments import vxInstruments
-from vxutils import to_datetime, to_timestring, to_enum, logger
-
-
-class vxDataLoader:
-    """本地数据加载器"""
-
-    def load_calendar(self) -> pl.Series:
-        """加载交易日历"""
-
-    def save_calendar(self, trade_dates: List[DateTimeType]) -> None:
-        """添加交易日历"""
-
-    def load_instruments(self, name: str = "cnstocks") -> vxInstruments:
-        """加载股票池"""
-
-    def save_instruments(self, instruments: vxInstruments) -> None:
-        """添加股票池"""
-
-    def load_features(
-        self, period: str = "day", sec_type: SecType = SecType.STOCK
-    ) -> pl.LazyFrame:
-        """加载特征数据
-
-        Keyword Arguments:
-            period {str} -- 周期，可选: day 或 min (default: {"day"})
-            sec_type {SecType} -- 证券类型 (default: {SecType.STOCK})
-
-        Returns:
-            pl.LazyFrame -- 返回特征数据LazyFrame格式
-        """
-
-    def save_features(
-        self, data: pl.DataFrame, period: str = "day", sec_type: SecType = SecType.STOCK
-    ) -> None:
-        """保存特征数据
-
-        Arguments:
-            data {pl.DataFrame} -- 特征数据
-
-        Keyword Arguments:
-            period {str} -- 周期，可选: day 或 min (default: {"day"})
-            sec_type {SecType} -- 证券类型 (default: {SecType.STOCK})
-        """
-
-    def load_factor(self, name: str) -> pl.LazyFrame:
-        """加载因子数据
-
-        Arguments:
-            name {str} -- 因子名称
-
-        Returns:
-            pl.LazyFrame -- 返回因子数据LazyFrame格式
-        """
-
-    def save_factor(self, factor_datas: pl.DataFrame) -> None:
-        """保存因子数据
-
-        Arguments:
-            factor_datas {pl.DataFrame} -- 因子数据
-        """
-
-
-class vxLocalDataLoader(vxDataLoader):
-    """本地数据加载器"""
-
-    def __init__(self, data_path: Union[str, Path] = None):
-        if data_path is None:
-            data_path = Path.home().joinpath(".data")
-        if isinstance(data_path, str):
-            data_path = Path(data_path)
-
-        self._data_path = data_path
-        self._data_path.joinpath("instruments").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("features").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("factors").mkdir(parents=True, exist_ok=True)
-        logger.info(f"{self.__class__.__name__} init with data_path: {self._data_path}")
-
-    def load_calendar(self) -> pl.Series:
-        if self._data_path.joinpath("calendar.csv").exists():
-            return (
-                pl.read_csv(self._data_path.joinpath("calendar.csv"))
-                .with_columns([pl.col("trade_date").apply(to_datetime)])
-                .sort(by="trade_date")
-            )
-        return None
-
-    def save_calendar(self, trade_dates: List[DateTimeType]) -> None:
-        calendar_csv = self._data_path.joinpath("calendar.csv")
-        calendar_df = pl.DataFrame({"trade_date": trade_dates})
-        if calendar_csv.exists():
-            save_trade_dates = pl.read_csv(calendar_csv)
-            calendar_df = save_trade_dates.extend(calendar_df)
-        calendar_df.select(
-            pl.col("trade_date").apply(lambda x: to_timestring(x, "%Y-%m-%d")).unique()
-        ).sort(by="trade_date").write_csv(calendar_csv)
-
-    def load_instruments(self, name: str = "cnstocks") -> vxInstruments:
-        instruments_csv = self._data_path.joinpath("instruments", f"{name}.csv")
-        registrations = None
-        if instruments_csv.exists():
-            registrations = pl.read_csv(instruments_csv)
-        return vxInstruments(name, registrations)
-
-    def save_instruments(self, instruments: vxInstruments) -> None:
-        instruments_csv = self._data_path.joinpath(
-            "instruments", f"{instruments.name}.csv"
-        )
-        instruments.registrations.write_csv(instruments_csv)
-
-    def load_features(
-        self, period: str = "day", sec_type: SecType = SecType.STOCK
-    ) -> pl.LazyFrame:
-        period = period.lower()
-        if period not in ["day", "min"]:
-            raise ValueError(f"period must be day or min, but got {period}")
-        sec_type = to_enum(sec_type, SecType)
-
-        features_parquet = self._data_path.joinpath(
-            "features", f"{period}_{sec_type.name.lower()}.parquet"
-        )
-        return pl.scan_parquet(features_parquet).with_columns(
-            [
-                pl.col("trade_date").str.strptime(pl.Datetime, "%Y-%m-%d"),
-                pl.col("*")
-                .exclude(["trade_date", "symbol"])
-                .cast(pl.Float64, strict=False),
-            ]
-        )
-
-    def save_features(
-        self,
-        data: pl.DataFrame,
-        period: str = "day",
-        sec_type: Union[str, SecType] = "STOCK",
-    ) -> None:
-        period = period.lower()
-
-        if period not in ["day", "min"]:
-            raise ValueError(f"period must be day or min, but got {period}")
-        sec_type = to_enum(sec_type, SecType)
-
-        features_parquet = self._data_path.joinpath(
-            "features", f"{period}_{sec_type.name.lower()}.parquet"
-        )
-        data = data.with_columns(
-            [
-                pl.col("trade_date").dt.strftime("%Y-%m-%d"),
-                pl.col("*")
-                .exclude(["trade_date", "symbol"])
-                .cast(pl.Float64, strict=False),
-            ]
-        ).sort(["trade_date", "symbol"])
-
-        if features_parquet.exists():
-            data = pl.read_parquet(features_parquet, use_pyarrow=True).extend(data)
-        data.write_parquet(features_parquet)
-
-    def load_factor(self, name: str) -> pl.LazyFrame:
-        factor_parquet = self._data_path.joinpath("factors", f"{name}.parquet")
-        return pl.scan_parquet(factor_parquet)
-
-    def save_factor(self, factor_datas: pl.DataFrame) -> None:
-        for name in factor_datas.columns:
-            if name in ["trade_date", "symbol"]:
-                continue
-
-            factor_parquet = self._data_path.joinpath("factors", f"{name}.parquet")
-            data = factor_datas.select(["trade_date", "symbol", name]).lazy()
-            if factor_parquet.exists():
-                data = pl.scan_parquet(factor_parquet).join(
-                    data,
-                    on=["trade_date", "symbol"],
-                    how="outer",
-                )
-            data.sink_parquet(factor_parquet)
-
-
-if __name__ == "__main__":
-    loader = vxLocalDataLoader("/Volumes/work/quant/collector/data")
-    print(loader.load_features("day", "STOCK").collect())
-    # print(loader.save_calendar(["2020-01-01 3:30:20", "2021-01-02", "2021-01-03"]))
-    # print(loader.load_calendar())
-    # from vxutils import vxtime
-
-    # vxtime.add_holidays(["2020-01-01 3:30:20", "2021-01-02", "2021-01-03"])
-    # print(vxtime.is_holiday("2020-01-01"))
+"""数据加载器"""
+
+from pathlib import Path
+from typing import Union, List
+import polars as pl
+from vxquant.model.contants import SecType
+from vxquant.model.typehint import DateTimeType
+from vxquant.model.instruments import vxInstruments
+from vxutils import to_datetime, to_timestring, to_enum, logger, vxAPIWrappers
+
+
+class vxDataLoader:
+    """本地数据加载器"""
+
+    def load_calendar(self) -> pl.Series:
+        """加载交易日历"""
+
+    def save_calendar(self, trade_dates: List[DateTimeType]) -> None:
+        """添加交易日历"""
+
+    def load_instruments(self, name: str = "cnstocks") -> vxInstruments:
+        """加载股票池"""
+
+    def save_instruments(self, instruments: vxInstruments) -> None:
+        """添加股票池"""
+
+    def load_features(
+        self, period: str = "day", sec_type: SecType = SecType.STOCK
+    ) -> pl.LazyFrame:
+        """加载特征数据
+
+        Keyword Arguments:
+            period {str} -- 周期，可选: day 或 min (default: {"day"})
+            sec_type {SecType} -- 证券类型 (default: {SecType.STOCK})
+
+        Returns:
+            pl.LazyFrame -- 返回特征数据LazyFrame格式
+        """
+
+    def save_features(
+        self, data: pl.DataFrame, period: str = "day", sec_type: SecType = SecType.STOCK
+    ) -> None:
+        """保存特征数据
+
+        Arguments:
+            data {pl.DataFrame} -- 特征数据
+
+        Keyword Arguments:
+            period {str} -- 周期，可选: day 或 min (default: {"day"})
+            sec_type {SecType} -- 证券类型 (default: {SecType.STOCK})
+        """
+
+    def load_factor(self, name: str) -> pl.LazyFrame:
+        """加载因子数据
+
+        Arguments:
+            name {str} -- 因子名称
+
+        Returns:
+            pl.LazyFrame -- 返回因子数据LazyFrame格式
+        """
+
+    def save_factor(self, factor_datas: pl.DataFrame) -> None:
+        """保存因子数据
+
+        Arguments:
+            factor_datas {pl.DataFrame} -- 因子数据
+        """
+
+
+class vxLocalDataLoader(vxDataLoader):
+    """本地数据加载器"""
+
+    def __init__(self, data_path: Union[str, Path] = None):
+        if data_path is None:
+            data_path = Path.home().joinpath(".data")
+        if isinstance(data_path, str):
+            data_path = Path(data_path)
+
+        self._data_path = data_path
+        self._data_path.joinpath("instruments").mkdir(parents=True, exist_ok=True)
+        self._data_path.joinpath("features").mkdir(parents=True, exist_ok=True)
+        self._data_path.joinpath("factors").mkdir(parents=True, exist_ok=True)
+        logger.info(f"{self.__class__.__name__} init with data_path: {self._data_path}")
+
+    def load_calendar(self) -> pl.Series:
+        if self._data_path.joinpath("calendar.csv").exists():
+            return (
+                pl.read_csv(self._data_path.joinpath("calendar.csv"))
+                .with_columns([pl.col("trade_date").apply(to_datetime)])
+                .sort(by="trade_date")
+            )
+        return None
+
+    def save_calendar(self, trade_dates: List[DateTimeType]) -> None:
+        calendar_csv = self._data_path.joinpath("calendar.csv")
+        calendar_df = pl.DataFrame({"trade_date": trade_dates})
+        if calendar_csv.exists():
+            save_trade_dates = pl.read_csv(calendar_csv)
+            calendar_df = save_trade_dates.extend(calendar_df)
+        calendar_df.select(
+            pl.col("trade_date").apply(lambda x: to_timestring(x, "%Y-%m-%d")).unique()
+        ).sort(by="trade_date").write_csv(calendar_csv)
+
+    def load_instruments(self, name: str = "cnstocks") -> vxInstruments:
+        instruments_csv = self._data_path.joinpath("instruments", f"{name}.csv")
+        registrations = None
+        if instruments_csv.exists():
+            registrations = pl.read_csv(instruments_csv)
+        return vxInstruments(name, registrations)
+
+    def save_instruments(self, instruments: vxInstruments) -> None:
+        instruments_csv = self._data_path.joinpath(
+            "instruments", f"{instruments.name}.csv"
+        )
+        instruments.registrations.write_csv(instruments_csv)
+
+    def load_industry_matrix(self, industry_classify):
+        pass
+
+    def save_industry_matrix(self, industry_matrix: pl.DataFrame) -> None:
+        pass
+
+    def load_features(
+        self, period: str = "day", sec_type: SecType = SecType.STOCK
+    ) -> pl.LazyFrame:
+        period = period.lower()
+        if period not in ["day", "min"]:
+            raise ValueError(f"period must be day or min, but got {period}")
+        sec_type = to_enum(sec_type, SecType)
+
+        features_parquet = self._data_path.joinpath(
+            "features", f"{period}_{sec_type.name.lower()}.parquet"
+        )
+        return pl.scan_parquet(features_parquet).with_columns(
+            [
+                pl.col("trade_date").str.strptime(pl.Datetime, "%Y-%m-%d"),
+                pl.col("*")
+                .exclude(["trade_date", "symbol"])
+                .cast(pl.Float64, strict=False),
+            ]
+        )
+
+    def save_features(
+        self,
+        data: pl.DataFrame,
+        period: str = "day",
+        sec_type: Union[str, SecType] = "STOCK",
+    ) -> None:
+        period = period.lower()
+
+        if period not in ["day", "min"]:
+            raise ValueError(f"period must be day or min, but got {period}")
+        sec_type = to_enum(sec_type, SecType)
+
+        features_parquet = self._data_path.joinpath(
+            "features", f"{period}_{sec_type.name.lower()}.parquet"
+        )
+        data = data.with_columns(
+            [
+                pl.col("trade_date").dt.strftime("%Y-%m-%d"),
+                pl.col("*")
+                .exclude(["trade_date", "symbol"])
+                .cast(pl.Float64, strict=False),
+            ]
+        ).sort(["trade_date", "symbol"])
+
+        if features_parquet.exists():
+            data = pl.read_parquet(features_parquet, use_pyarrow=True).extend(data)
+        data.write_parquet(features_parquet)
+
+    def load_factor(self, name: str) -> pl.LazyFrame:
+        factor_parquet = self._data_path.joinpath("factors", f"{name}.parquet")
+        return pl.scan_parquet(factor_parquet)
+
+    def save_factor(self, factor_datas: pl.DataFrame) -> None:
+        for name in factor_datas.columns:
+            if name in ["trade_date", "symbol", "mask"]:
+                continue
+
+            factor_parquet = self._data_path.joinpath("factors", f"{name}.parquet")
+            data = factor_datas.select(["trade_date", "symbol", name]).lazy()
+            if factor_parquet.exists():
+                data = pl.scan_parquet(factor_parquet).join(
+                    data,
+                    on=["trade_date", "symbol"],
+                    how="outer",
+                )
+            data.sink_parquet(factor_parquet)
+
+
+if __name__ == "__main__":
+    loader = vxLocalDataLoader("/Volumes/work/quant/collector/data")
+    print(loader.load_features("day", "STOCK").collect())
+    # print(loader.save_calendar(["2020-01-01 3:30:20", "2021-01-02", "2021-01-03"]))
+    # print(loader.load_calendar())
+    # from vxutils import vxtime
+
+    # vxtime.add_holidays(["2020-01-01 3:30:20", "2021-01-02", "2021-01-03"])
+    # print(vxtime.is_holiday("2020-01-01"))
```

### Comparing `vxquant-2023.4.1/src/vxquant/model/account.py` & `vxquant-2023.5.13/src/vxquant/model/account.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/contants.py` & `vxquant-2023.5.13/src/vxquant/model/contants.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/dbaccount.py` & `vxquant-2023.5.13/src/vxquant/model/dbaccount.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/exchange.py` & `vxquant-2023.5.13/src/vxquant/model/exchange.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/instruments.py` & `vxquant-2023.5.13/src/vxquant/model/instruments.py`

 * *Files 3% similar despite different names*

```diff
@@ -10,14 +10,16 @@
 
 def is_in_periods(dt, periods):
     dt = to_timestamp(dt) * 1_000_000
     return any(period[0] <= dt <= period[1] for period in periods)
 
 
 class vxInstruments:
+    """股票池类"""
+
     def __init__(self, name: str, registrations: pl.DataFrame = None):
         self._name = name
         self._registrations = (
             registrations.with_columns(
                 [
                     pl.col("start_date").apply(to_datetime),
                     pl.col("end_date").apply(to_datetime),
@@ -38,43 +40,70 @@
             to_datetime(vxtime.today())
             if self._registrations.height == 0
             else self._registrations["end_date"].max()
         )
 
     @property
     def name(self) -> str:
+        """股票池名称"""
         return self._name
 
     def __str__(self) -> str:
         return (
             f"< 证券池({self._name}) 最近更新日期"
             f":{self._last_updated_dt:%Y-%m-%d}"
             f" 最新证券:\n {self.list_instruments(self._last_updated_dt)} >"
         )
 
     @property
     def registrations(self) -> pl.DataFrame:
+        """股票池出入注册表
+
+        Returns:
+            pl.DataFrame -- 注册表
+        """
         return self._registrations
 
     @property
     def last_updated_dt(self) -> DateTimeType:
+        """最近更新日期
+
+        Returns:
+            DateTimeType -- 日期类型:datetime类型
+        """
         return self._last_updated_dt
 
     def list_instruments(self, trade_date: DateTimeType = None) -> List[InstrumentType]:
+        """列出股票池中的证券
+
+        Keyword Arguments:
+            trade_date {DateTimeType} -- 交易日，若为空，则为当前日期 (default: {None})
+
+        Returns:
+            List[InstrumentType] -- 股票列表
+        """
         trade_date = min(
             to_datetime(trade_date or vxtime.today()), self._last_updated_dt
         )
 
         inst = self._registrations.filter(
             ((pl.col("start_date") <= trade_date) & (pl.col("end_date") >= trade_date))
         )
 
         return inst["symbol"].to_list()
 
-    def get_weights(self, trade_date: DateTimeType = None) -> List[float]:
+    def get_weights(self, trade_date: DateTimeType = None) -> Dict[str, float]:
+        """获取权重信息
+
+        Keyword Arguments:
+            trade_date {DateTimeType} -- 交易日，若为空，则为当前日期 (default: {None})
+
+        Returns:
+            Dict[str,float] -- 权重信息
+        """
         trade_date = min(
             to_datetime(trade_date or vxtime.today()), self._last_updated_dt
         )
 
         inst = self._registrations.filter(
             ((pl.col("start_date") <= trade_date) & (pl.col("end_date") >= trade_date))
         )
@@ -107,25 +136,28 @@
                 ]
             ),
             in_place=True,
         )
         return self
 
     def update_components(
-        self, instruments: Dict[InstrumentType, float], updated_dt: DateTimeType = None
+        self,
+        instruments: Union[List[InstrumentType], Dict[InstrumentType, float]],
+        updated_dt: DateTimeType = None,
     ):
         """按增量更新股票池"""
 
         updated_dt = to_datetime(updated_dt or vxtime.today())
         if (not self._registrations.is_empty()) and self._last_updated_dt >= updated_dt:
             raise ValueError(
                 f"updated_dt( {updated_dt:%Y-%m-%d} ) 小于当前更新时间:"
                 f" {self._last_updated_dt:%Y-%m-%d}"
             )
-        if isinstance(instruments, list):
+
+        if isinstance(instruments, (list, tuple)):
             instruments = {inst: 1 for inst in instruments}
 
         new_instruments = pl.DataFrame(
             [
                 {"symbol": symbol, "end_date": self._last_updated_dt, "weight": weight}
                 for symbol, weight in instruments.items()
             ]
@@ -154,14 +186,15 @@
                     .alias("weight"),
                 ]
             )
             .select(["symbol", "start_date", "end_date", "weight"])
             .sort(by="end_date")
         )
         self._last_updated_dt = updated_dt
+        return self
 
     @classmethod
     def load(cls, name, instruments_parquet: Union[str, Path]) -> "vxInstruments":
         registrations = pl.read_parquet(instruments_parquet)
         return vxInstruments(name, registrations)
 
     def dump(self, instruments_parquet: Union[str, Path]) -> None:
@@ -264,16 +297,17 @@
                 .iter_rows(named=True)
             ):
                 if rows["start_date"] < other_rows["start_date"]:
                     new_registrations.append(
                         {
                             "symbol": rows["symbol"],
                             "start_date": rows["start_date"],
-                            "end_date": other_rows["start_date"]
-                            - datetime.timedelta(days=1),
+                            "end_date": other_rows["start_date"] - datetime.timedelta(
+                                days=1
+                            ),
                             "weight": rows["weight"],
                         }
                     )
 
                 rows["start_date"] = other_rows["end_date"] + datetime.timedelta(days=1)
 
                 if rows["start_date"] > rows["end_date"]:
```

### Comparing `vxquant-2023.4.1/src/vxquant/model/nomalize.py` & `vxquant-2023.5.13/src/vxquant/model/nomalize.py`

 * *Files 3% similar despite different names*

```diff
@@ -62,37 +62,42 @@
 
     if match_obj is None:
         raise ValueError(f"{symbol} format is not support.")
 
     code = match_obj[1]
     exchange = (
         symbol.replace("se", "").replace("SE", "").replace(".", "").replace(code, "")
-    )
-    if exchange.upper() in {"OF", "ETF", "LOF", ""}:
-        exchange = "SZSE" if code[0] in ["0", "1", "2", "3", "4"] else "SHSE"
+    ).upper()
+    if exchange in {"OF", "ETF", "LOF", "FUND", "OFUND", ""}:
+        if code[0] in ["0", "1", "2", "3", "4"]:
+            exchange = "SZSE"
+        elif code[0] in ["8"]:
+            exchange = "BJSE"
+        else:
+            exchange = "SHSE"
     else:
         exchange = exchange if len(exchange) > 2 else f"{exchange}SE"
 
-    return (exchange.upper(), code)
+    return (exchange, code)
 
 
 @lru_cache(200)
 def to_symbol(instrument: str):
     if instrument.upper() in {"CNY", "CACH"}:
         return "CNY"
 
-    match_obj = re.match(r"^(SHSE|SZSE).(\d{6})$", instrument)
+    match_obj = re.match(r"^(SHSE|SZSE|BJSE|HKSE).(\d{6})$", instrument)
 
     if match_obj:
         return instrument
 
     exchange, code = normalize_symbol(instrument)
     return f"{exchange}.{code}"
 
 
 if __name__ == "__main__":
     print(to_symbol("SHSE.600000"))
     print(to_symbol("SH600000"))
     print(to_symbol("sh600000"))
     print(to_symbol("600000.sh"))
     print(to_symbol("600000.SHSE"))
-    print(to_symbol("600000sh"))
+    print(to_symbol("600000bj"))
```

### Comparing `vxquant-2023.4.1/src/vxquant/model/portfolio.py` & `vxquant-2023.5.13/src/vxquant/model/portfolio.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/preset.py` & `vxquant-2023.5.13/src/vxquant/model/preset.py`

 * *Files 0% similar despite different names*

```diff
@@ -308,18 +308,24 @@
     "SZSE.159937",
     "SHSE.518680",
     "SHSE.518850",
     "SHSE.518600",
     "SHSE.518660",
     "SHSE.518890",
     "SZSE.159812",
+    "SZSE.159980",
+    "SZSE.159981",
     "SHSE.518860",
 ]
 # 现金管理产品
 _CASH_SECURITIES = [
+    "SHSE.511270",
+    "SHSE.511380",
+    "SHSE.511180",
+    "SZSE.159985",
     "SHSE.511990",
     "SHSE.511880",
     "SHSE.511660",
     "SHSE.511850",
     "SHSE.511810",
     "SZSE.159001",
     "SHSE.511690",
@@ -362,15 +368,14 @@
 class vxMarketPreset:
     """交易所预设"""
 
     def __init__(self, symbol) -> None:
         preset = _DEFAULT_RESET.copy()
         if symbol[:8] in _DEFULAT_SYMBOL_MAP:
             self.__dict__.update(**_DEFULAT_SYMBOL_MAP[symbol[:8]])
-
         elif symbol[:7] in _DEFULAT_SYMBOL_MAP:
             self.__dict__.update(**_DEFULAT_SYMBOL_MAP[symbol[:7]])
         else:
             self.__dict__.update(**preset)
 
         if symbol in _CASH_SECURITIES:
             self.allow_t0 = True
```

### Comparing `vxquant-2023.4.1/src/vxquant/model/tools/gmData.py` & `vxquant-2023.5.13/src/vxquant/model/tools/gmData.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/model/tools/qmtData.py` & `vxquant-2023.5.13/src/vxquant/model/tools/qmtData.py`

 * *Files 4% similar despite different names*

```diff
@@ -333,7 +333,59 @@
     # 最近结算日
     "settle_day": lambda: vxtime.today("23:59:59") - 24 * 60 * 60,
     # 下单channel
     "channel": lambda x: "",
 }
 
 qmtAccountInfoConvter = vxDataConvertor(vxAccountInfo, ACCOUNTINFO_CONVERTORS)
+
+
+CREDIT_ACCOUNTINFO_CONVERTORS = {
+    # 组合ID
+    "portfolio_id": lambda x: "",
+    # 账户id
+    "account_id": "m_strAccountID",
+    # 账户币种
+    "currency": lambda x: "CNY",
+    # 今日转入金额
+    "deposit": lambda x: 0.0,
+    # 今日转出金额
+    "withdraw": lambda x: 0.0,
+    # 总资产
+    "asset": "m_dBalance",
+    # 净资产
+    "nav": "m_dAssureAsset",
+    # 总负债
+    "debt": "m_dTotalDebt",
+    # 资金余额
+    "balance": lambda x: x.cash + x.frozen_cash,
+    # 冻结金额
+    "frozen": "m_dFrozenCash",
+    # 可用金额
+    "available": "m_dAvailable",
+    # 融资融券可用
+    "margin_available": "m_dEnableBailBalance",
+    # 总市值
+    "marketvalue": "m_dMarketValue",
+    # 今日盈利
+    "today_profit": lambda x: 0.0,
+    # 浮动盈亏
+    "fnl": "m_dPositionProfit",
+    # 基金份额
+    "fund_shares": "m_dBalance",
+    # 基金净值估算
+    "fund_nav": lambda x: 1.0,
+    # 昨日总资产
+    "asset_yd": "m_dBalance",
+    # 昨日净资产
+    "nav_yd": "m_dBalance",
+    # 昨日基金金额
+    "fund_nav_yd": lambda x: 1.0,
+    # 最近结算日
+    "settle_day": lambda: vxtime.today("23:59:59") - 24 * 60 * 60,
+    # 下单channel
+    "channel": lambda x: "",
+}
+
+qmtCreditAccountInfoConvter = vxDataConvertor(
+    vxAccountInfo, CREDIT_ACCOUNTINFO_CONVERTORS
+)
```

### Comparing `vxquant-2023.4.1/src/vxquant/model/tools/tdxData.py` & `vxquant-2023.5.13/src/vxquant/model/tools/tdxData.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/providers/baostock_api.py` & `vxquant-2023.5.13/src/vxquant/providers/baostock_api.py`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,144 +1,144 @@
-"""baostock数据接口"""
-
-import baostock as bs
-import polars as pl
-import pandas as pd
-from typing import List
-from vxquant.model.nomalize import to_symbol
-from vxquant.model.typehint import InstrumentType
-from vxquant.model.instruments import vxInstruments
-from vxquant.providers.base import vxCalendarProvider, vxDownloadInstrumentsProvider
-from vxutils import vxtime, to_timestring
-
-# 生成器
-
-
-def bs_gen(resultdata):
-    while (resultdata.error_code == "0") & resultdata.next():
-        yield resultdata.get_row_data()
-
-
-class vxBaoStockCalenderProvider(vxCalendarProvider):
-    """baostock 日历接口"""
-
-    def get_trade_dates(self, market: str = "cn") -> List[InstrumentType]:
-        try:
-            lg = bs.login()
-            if lg.error_code != "0":
-                raise ConnectionRefusedError(f"登录失败: {lg.error_msg}")
-
-            rs = bs.query_trade_dates(start_date="2005-01-01", end_date="2023-12-31")
-            if rs.error_code != "0":
-                raise ConnectionError(f"获取交易日历失败: {rs.error_msg}")
-
-            df = pl.DataFrame(list(bs_gen(rs))).transpose()
-            df.columns = rs.fields
-            return df.filter(pl.col("is_trading_day") == "1").select(
-                pl.col("calendar_date").alias("trade_date")
-            )["trade_date"]
-        finally:
-            bs.logout()
-
-
-class vxBaoStockDownloadInstrumentsProvider(vxDownloadInstrumentsProvider):
-    def __call__(self):
-        pass
-
-    def get_instruments(self) -> List[vxInstruments]:
-        with vxtime.timeit("query_stock_basic"):
-            rs = bs.query_stock_basic()
-            if rs.error_code != "0":
-                raise ConnectionError(f"获取股票基本信息失败: {rs.error_msg}")
-
-            datas = list(bs_gen(rs))
-            df = pl.DataFrame(datas).transpose()
-            df.columns = rs.fields
-        df = df.with_columns(
-            [
-                pl.col("code").apply(to_symbol).alias("symbol"),
-                pl.col("ipoDate").alias("start_date"),
-                pl.when(pl.col("outDate") == "")
-                .then(to_timestring(vxtime.today(), "%Y-%m-%d"))
-                .otherwise(pl.col("outDate"))
-                .alias("end_date"),
-                pl.lit(1).alias("weight"),
-            ]
-        ).select(["symbol", "start_date", "end_date", "weight", "type"])
-
-        cnstocks = vxInstruments(
-            "cnstocks",
-            df.filter(pl.col("type") == "1").select(
-                [
-                    "symbol",
-                    "start_date",
-                    "end_date",
-                    "weight",
-                ]
-            ),
-        )
-        cncbonds = vxInstruments(
-            "cncbonds",
-            df.filter(pl.col("type") == "4").select(
-                [
-                    "symbol",
-                    "start_date",
-                    "end_date",
-                    "weight",
-                ]
-            ),
-        )
-        cnindexes = vxInstruments(
-            "cnindexes",
-            df.filter(pl.col("type") == "2").select(
-                ["symbol", "start_date", "end_date", "weight"]
-            ),
-        )
-        cnetflofs = vxInstruments(
-            "cnetflofs",
-            df.filter(pl.col("type") == "5").select(
-                ["symbol", "start_date", "end_date", "weight"]
-            ),
-        )
-        return [cncbonds, cnstocks, cnindexes, cnetflofs]
-
-
-if __name__ == "__main__":
-    c = vxBaoStockCalenderProvider()
-
-    # with vxtime.timeit():
-    # d = c.get_trade_dates()
-    # print(d)
-    bs.login()
-    with vxtime.timeit():
-        rs = bs.query_stock_basic()
-    # rs = bs.query_all_stock(day="2021-01-04")
-    datas = list(bs_gen(rs))
-    df = pl.DataFrame(datas).transpose()
-    df.columns = rs.fields
-    df = df.with_columns(
-        [
-            pl.col("code").apply(to_symbol).alias("symbol"),
-            pl.col("ipoDate").alias("start_date"),
-            pl.when(pl.col("outDate") == "")
-            .then(to_timestring(vxtime.today(), "%Y-%m-%d"))
-            .otherwise(pl.col("outDate"))
-            .alias("end_date"),
-            pl.lit(1).alias("weights"),
-        ]
-    ).select(["symbol", "start_date", "end_date", "weights", "type"])
-    cnstocks = vxInstruments(
-        "cnstocks",
-        df.filter(pl.col("type") == "4").select(
-            [
-                "symbol",
-                "start_date",
-                "end_date",
-                "weights",
-            ]
-        ),
-    )
-    all_cnbonds = cnstocks.list_instruments()
-    print(len(all_cnbonds))
-    #
-
-    bs.logout()
+"""baostock数据接口"""
+
+import baostock as bs
+import polars as pl
+import pandas as pd
+from typing import List
+from vxquant.model.nomalize import to_symbol
+from vxquant.model.typehint import InstrumentType
+from vxquant.model.instruments import vxInstruments
+from vxquant.providers.base import vxCalendarProvider, vxDownloadInstrumentsProvider
+from vxutils import vxtime, to_timestring
+
+# 生成器
+
+
+def bs_gen(resultdata):
+    while (resultdata.error_code == "0") & resultdata.next():
+        yield resultdata.get_row_data()
+
+
+class vxBaoStockCalenderProvider(vxCalendarProvider):
+    """baostock 日历接口"""
+
+    def get_trade_dates(self, market: str = "cn") -> List[InstrumentType]:
+        try:
+            lg = bs.login()
+            if lg.error_code != "0":
+                raise ConnectionRefusedError(f"登录失败: {lg.error_msg}")
+
+            rs = bs.query_trade_dates(start_date="2005-01-01", end_date="2023-12-31")
+            if rs.error_code != "0":
+                raise ConnectionError(f"获取交易日历失败: {rs.error_msg}")
+
+            df = pl.DataFrame(list(bs_gen(rs))).transpose()
+            df.columns = rs.fields
+            return df.filter(pl.col("is_trading_day") == "1").select(
+                pl.col("calendar_date").alias("trade_date")
+            )["trade_date"]
+        finally:
+            bs.logout()
+
+
+class vxBaoStockDownloadInstrumentsProvider(vxDownloadInstrumentsProvider):
+    def __call__(self):
+        pass
+
+    def get_instruments(self) -> List[vxInstruments]:
+        with vxtime.timeit("query_stock_basic"):
+            rs = bs.query_stock_basic()
+            if rs.error_code != "0":
+                raise ConnectionError(f"获取股票基本信息失败: {rs.error_msg}")
+
+            datas = list(bs_gen(rs))
+            df = pl.DataFrame(datas).transpose()
+            df.columns = rs.fields
+        df = df.with_columns(
+            [
+                pl.col("code").apply(to_symbol).alias("symbol"),
+                pl.col("ipoDate").alias("start_date"),
+                pl.when(pl.col("outDate") == "")
+                .then(to_timestring(vxtime.today(), "%Y-%m-%d"))
+                .otherwise(pl.col("outDate"))
+                .alias("end_date"),
+                pl.lit(1).alias("weight"),
+            ]
+        ).select(["symbol", "start_date", "end_date", "weight", "type"])
+
+        cnstocks = vxInstruments(
+            "cnstocks",
+            df.filter(pl.col("type") == "1").select(
+                [
+                    "symbol",
+                    "start_date",
+                    "end_date",
+                    "weight",
+                ]
+            ),
+        )
+        cncbonds = vxInstruments(
+            "cncbonds",
+            df.filter(pl.col("type") == "4").select(
+                [
+                    "symbol",
+                    "start_date",
+                    "end_date",
+                    "weight",
+                ]
+            ),
+        )
+        cnindexes = vxInstruments(
+            "cnindexes",
+            df.filter(pl.col("type") == "2").select(
+                ["symbol", "start_date", "end_date", "weight"]
+            ),
+        )
+        cnetflofs = vxInstruments(
+            "cnetflofs",
+            df.filter(pl.col("type") == "5").select(
+                ["symbol", "start_date", "end_date", "weight"]
+            ),
+        )
+        return [cncbonds, cnstocks, cnindexes, cnetflofs]
+
+
+if __name__ == "__main__":
+    c = vxBaoStockCalenderProvider()
+
+    # with vxtime.timeit():
+    # d = c.get_trade_dates()
+    # print(d)
+    bs.login()
+    with vxtime.timeit():
+        rs = bs.query_stock_basic()
+    # rs = bs.query_all_stock(day="2021-01-04")
+    datas = list(bs_gen(rs))
+    df = pl.DataFrame(datas).transpose()
+    df.columns = rs.fields
+    df = df.with_columns(
+        [
+            pl.col("code").apply(to_symbol).alias("symbol"),
+            pl.col("ipoDate").alias("start_date"),
+            pl.when(pl.col("outDate") == "")
+            .then(to_timestring(vxtime.today(), "%Y-%m-%d"))
+            .otherwise(pl.col("outDate"))
+            .alias("end_date"),
+            pl.lit(1).alias("weights"),
+        ]
+    ).select(["symbol", "start_date", "end_date", "weights", "type"])
+    cnstocks = vxInstruments(
+        "cnstocks",
+        df.filter(pl.col("type") == "4").select(
+            [
+                "symbol",
+                "start_date",
+                "end_date",
+                "weights",
+            ]
+        ),
+    )
+    all_cnbonds = cnstocks.list_instruments()
+    print(len(all_cnbonds))
+    #
+
+    bs.logout()
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/base.py` & `vxquant-2023.5.13/src/vxquant/providers/base.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,17 @@
 """供应接口"""
 import datetime
 from abc import abstractmethod
-from typing import Dict, List, Union, Optional
+from typing import Dict, List, Union, Optional, Any
 import pandas as pd
 import polars as pl
-from pathlib import Path
 from vxutils import (
     vxtime,
-    vxLRUCache,
     to_datetime,
     diskcache,
-    to_timestamp,
-    logger,
-    vxSQLiteCache,
 )
 from vxsched import vxEvent, vxTrigger, vxContext
 from vxquant.model.exchange import (
     vxAccountInfo,
     vxPosition,
     vxCashPosition,
     vxOrder,
@@ -37,45 +32,65 @@
         self._context = None
 
     @property
     def context(self) -> vxContext:
         """上下文对象"""
         return self._context
 
-    def set_context(self, context: vxContext):
+    def set_context(self, context: vxContext, **kwargs):
+        """设置上下文对象
+
+        Arguments:
+            context {vxContext} -- 上下文对象
+        """
         self._context = context
+        self._context.update(kwargs)
+
+    def __call__(self, *args, **kwargs) -> Any:
+        raise NotImplementedError
+
+
+class vxInitProviderContext(vxProviderBase):
+    """初始化context接口"""
+
+    def set_context(self, context: vxContext, **kwargs):
+        return super().set_context(context, **kwargs)
 
 
 class vxHQProvider(vxProviderBase):
-    _tickcache = vxSQLiteCache()
+    """行情接口基类"""
+
+    _tickcache = diskcache
 
     def __call__(self, *symbols: List[InstrumentType]) -> Dict[InstrumentType, vxTick]:
         """实时行情接口
 
         Returns:
             Dict[InstrumentType, vxTick] -- _description_
         """
         if len(symbols) == 1 and isinstance(symbols[0], list):
             symbols = symbols[0]
 
         ticks = self._tickcache.get_many(symbols)
-        _missing_symbols = list(set(symbols) - set(ticks.keys()))
+        suspend_symbols = self._tickcache.get("__suspend_symbols__", [])
+        _missing_symbols = list(set(symbols) - set(ticks.keys()) - set(suspend_symbols))
 
         if _missing_symbols:
             hq_ticks = self._hq(*_missing_symbols)
-            now = vxtime.now()
-            if now < vxtime.today("09:25:00"):
-                expired_dt = vxtime.today("09:25:01")
-            elif now < vxtime.today("15:00:00"):
-                expired_dt = now + 3
-            else:
-                expired_dt = vxtime.today("09:25:01") + 24 * 60 * 60
+            if hq_ticks:
+                now = vxtime.now()
+                if now < vxtime.today("09:25:00"):
+                    expired_dt = vxtime.today("09:25:01")
+                elif now < vxtime.today("16:00:00"):
+                    expired_dt = now + 3
+                else:
+                    expired_dt = vxtime.today("09:25:01") + 24 * 60 * 60
 
-            self._tickcache.update(hq_ticks, expired_dt=expired_dt)
-            ticks.update(hq_ticks)
+                self._tickcache.update(hq_ticks, expired_dt=expired_dt)
+                ticks.update(hq_ticks)
         return ticks
 
     @abstractmethod
     def _hq(self, *symbols: List[InstrumentType]) -> Dict[InstrumentType, vxTick]:
         """实时数据接口
 
         Returns:
@@ -90,32 +105,34 @@
 
 class vxCalendarProvider(vxProviderBase):
     def __call__(
         self,
         start_date: DateTimeType = None,
         end_date: DateTimeType = None,
         market: str = "cn",
-    ):
+    ) -> pl.Series:
         start_date = to_datetime(start_date or "2010-01-01")
         end_date = to_datetime(end_date or vxtime.today())
 
         trade_days = []
+        this_year_begin = datetime.datetime.today().replace(
+            month=1, day=1, hour=0, minute=0, second=0
+        )
 
         for year in range(start_date.year, end_date.year + 1):
             key = f"calendar_{market}_{year}"
             if key not in diskcache:
                 dates = self.get_trade_dates(
                     market, start_date=f"{year}-01-01", end_date=f"{year}-12-31"
                 )
-                last_date = to_datetime(dates[-1])
-                expired_dt = (
-                    last_date if last_date > datetime.datetime.today() else None
-                )
-                diskcache.set(key, dates, expired_dt=expired_dt)
-                trade_days.extend(dates)
+                if dates:
+                    last_date = to_datetime(dates[-1])
+                    expired_dt = last_date if last_date > this_year_begin else None
+                    diskcache.set(key, dates, expired_dt=expired_dt)
+                    trade_days.extend(dates)
             else:
                 trade_days.extend(diskcache[key])
 
         return (
             pl.DataFrame({"trade_date": trade_days})
             .with_columns([pl.col("trade_date").apply(to_datetime)])
             .filter((pl.col("trade_date").is_between(start_date, end_date)))
@@ -149,14 +166,34 @@
 
         Returns:
             vxInstruments -- _description_
         """
         raise NotImplementedError
 
 
+class vxGetDividendProvider(vxProviderBase):
+    def __call__(
+        self,
+        symbol: InstrumentType,
+        start_date: DateTimeType = None,
+        end_date: DateTimeType = None,
+    ) -> pl.DataFrame:
+        """获取分红情况
+
+        Arguments:
+            symbol {InstrumentType} -- 需要下载的证券类型
+            start_date {DateTimeType} -- 开始时间
+            end_date {DateTimeType} -- 结束时间
+
+        Returns:
+            pl.DataFrame -- 返回： [trade_date, symbol, cash_div,allotment_ratio,allotment_price,share_div_ratio,share_trans_ratio,] 的列表
+        """
+        raise NotImplementedError
+
+
 class vxFeaturesProvider(vxProviderBase):
     def __call__(
         self,
         instruments: List[InstrumentType],
         start_date: DateTimeType = None,
         end_date: DateTimeType = None,
         freq: str = "1d",
@@ -216,143 +253,14 @@
             factor {pl.DataFrame} -- factor： "trade_date", "symbol", "factor1","factor2"...
         """
         if isinstance(factors, pl.DataFrame):
             factors = factors.lazy()
         self._db = self._db.join(factors, on=["trade_date", "symbol"])
 
 
-class vxDownloadAllProvider(vxProviderBase):
-    def __init__(self, data_path: Union[str, Path] = None) -> None:
-        if data_path is None:
-            data_path = Path.home().joinpath(".data")
-
-        if isinstance(data_path, str):
-            data_path = Path(data_path)
-
-        self._data_path = data_path
-        logger.info(f"Data Path: {self._data_path}")
-        self._data_path.joinpath("features").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("factors").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("instruments").mkdir(parents=True, exist_ok=True)
-        logger.info(f"初始化数据目录: {self._data_path} 完成")
-
-    def __call__(
-        self, start_date: DateTimeType = "2005-01-01", end_date: DateTimeType = None
-    ) -> None:
-        """下载全量数据
-
-        Keyword Arguments:
-            start_date {DateTimeType} -- 开始日期，默认：2005-01-01 (default: {"2005-01-01"})
-            end_date {DateTimeType} -- 结束日期，默认：None，即最近一个交易日 (default: {None})
-
-        """
-
-
-class vxDownloadDailyProvider(vxProviderBase):
-    """每日下载数据接口"""
-
-    def __init__(self, data_path: Union[str, Path] = None) -> None:
-        if data_path is None:
-            data_path = Path.home().joinpath(".data")
-
-        if isinstance(data_path, str):
-            data_path = Path(data_path)
-
-        self._data_path = data_path
-        logger.info(f"Data Path: {self._data_path}")
-        self._data_path.joinpath("features").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("factors").mkdir(parents=True, exist_ok=True)
-        self._data_path.joinpath("instruments").mkdir(parents=True, exist_ok=True)
-        logger.info(f"初始化数据目录: {self._data_path} 完成")
-
-    def __call__(self, context: vxContext, event: vxEvent) -> None:
-        """每日下载数据"""
-        logger.info("开始下载每日数据")
-        self.download_daily_features()
-        self.download_daily_factors()
-        self.download_daily_instruments()
-        logger.info("每日数据下载完成")
-
-
-class vxDownloadInstrumentsProvider(vxProviderBase):
-    """全量下载成分股接口"""
-
-    def __init__(self, instruments_path: Union[str, Path] = None) -> None:
-        self._instruments_path = Path(instruments_path or "~/.data/instruments")
-
-    def __call__(self) -> None:
-        """全量重新下载各个板块成分股票"""
-        logger.info("下载全量A股股票池")
-        instruments = []
-        instruments.extend(self.get_cnstocks())
-        instruments.extend(self.get_cbonds())
-        instruments.extend(self.get_indexs())
-        instruments.extend(self.get_industry())
-        instruments.extend(self.get_index_constituents())
-        for inst in instruments:
-            inst.registrations.write_csv(
-                self._instruments_path.joinpath(f"{inst._name}.csv"),
-                datetime_format="%Y-%m-%d",
-                date_format="%Y-%m-%d",
-            )
-
-    def get_cnstocks(self) -> List[vxInstruments]:
-        """下载全量A股股票数据,st股票池， 停牌股票池
-
-        Returns:
-            vxInstruments -- 'cnstocks'股票池
-        """
-
-    def get_cbonds(self) -> vxInstruments:
-        """下载全量可转债成分数据
-
-        Returns:
-            vxInstruments -- 'cbonds' 股票池
-        """
-
-    def get_indexs(self) -> vxInstruments:
-        """所有指数代码数据
-
-        Returns:
-            vxInstruments -- 'cnindexs' 股票池
-        """
-
-    def get_industry(self, industry_names: List[str] = None) -> List[vxInstruments]:
-        """获取申万行业成分股
-
-        Arguments:
-            industry_names {List[str]} -- 行业名称 {default: None} 当前为None时，全部行业成分股数据
-
-        Returns:
-            List[vxInstruments] -- 行业成分股
-        """
-
-    def get_index_constituents(
-        self, index_symbols: List[str] = None
-    ) -> List[vxInstruments]:
-        """获取指数的成分股
-
-        Keyword Arguments:
-            index_symbols {List[str]} -- 指数代码，若为None时，获取: ['SHSE.000300','SHSE.000905','SHSE.000852'] (default: {None})
-
-        Returns:
-            List[vxInstruments] -- 指数成分股
-        """
-
-
-class vxUpdateInstruments(vxProviderBase):
-    """增量更新成分股接口"""
-
-    def __init__(self, instruments_path: Union[str, Path] = None) -> None:
-        self._instruments_path = instruments_path or "~/.data/instruments"
-
-    def __call__(self, *instrument_names: List[str]) -> None:
-        """下载最新的成分股票"""
-
-
 class vxGetAccountProvider(vxProviderBase):
     def __call__(self, account_id: str = None) -> vxAccountInfo:
         """获取账户信息接口
 
         Keyword Arguments:
             account_id {str} -- 账号信息 (default: {None})
 
@@ -486,28 +394,7 @@
 
     def __str__(self) -> str:
         return f"< {self.__class__.__name__}({self.channel_name})"
 
     @abstractmethod
     def __call__(self, callback=None) -> List[vxEvent]:
         pass
-
-
-if __name__ == "__main__":
-    from vxquant.model.nomalize import to_symbol
-
-    with vxtime.timeit():
-        f = vxFactorsProvider(
-            "/Users/libao/src/开源代码/vxquant/.data/cn/day_stock_factors.parquet"
-        )
-        df = f.database.with_columns(
-            [
-                pl.col("ts_code").apply(to_symbol),
-                pl.col("total_mv").log().alias("market_cap"),
-                (1 / pl.col("pb")).alias("bm"),
-            ]
-        ).collect()
-
-        print(df)
-        df.select(pl.exclude("ts_code")).write_parquet(
-            "/Users/libao/src/开源代码/vxquant/.data/cn/day_stock_factors.parquet"
-        )
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/ftp.py` & `vxquant-2023.5.13/src/vxquant/providers/ftp.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/providers/local.py` & `vxquant-2023.5.13/src/vxquant/providers/local.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 """本地文件接口"""
 import polars as pl
 from pathlib import Path
 from typing import List, Union
 from vxquant.providers.base import vxInstrumentsProvider, vxFeaturesProvider
 from vxquant.model.instruments import vxInstruments
 from vxquant.model.typehint import InstrumentType, DateTimeType
+from vxquant.model.nomalize import normalize_freq, to_symbol
 from vxutils import logger, to_datetime, vxtime
 
 
 class vxLocalInstrumentsProvider(vxInstrumentsProvider):
     def __init__(self, data_dir: Union[str, Path] = None) -> None:
         self.instruments_dir = (
             Path(data_dir) if data_dir else Path.home().joinpath(".data")
@@ -50,28 +51,34 @@
         freq: str = "1d",
         fields: List[str] = None,
     ) -> pl.DataFrame:
         start_date = to_datetime(start_date or "2005-01-01")
         end_date = to_datetime(end_date or vxtime.today())
         if isinstance(instruments, vxInstruments):
             instruments = instruments.all_instruments()
-        freq = "day" if freq == "1d" else "min"
+        freq, period = normalize_freq(freq)
+
+        # freq = "day" if period == "1d" else "min"
 
         if fields is not None:
             fields = set(fields)
             fields.add(self._date_col)
             fields.add(self._symbol_col)
-            fields = pl.col(list(fields))
+            fields = pl.col(*fields)
         else:
             fields = pl.col("*")
 
-        data = pl.scan_parquet(Path(self._features_dir, f"features_{freq}.parquet"))
+        data = pl.scan_parquet(Path(self._features_dir, f"features_{period}.parquet"))
 
         return (
-            data.filter(
+            data.with_columns(
+                [pl.col(self._date_col).str.strptime(pl.Datetime, "%Y-%m-%d")]
+            )
+            .filter(
                 (pl.col(self._symbol_col).is_in(instruments))
                 & (pl.col(self._date_col).is_between(start_date, end_date))
             )
+            .drop_nulls()
             .sort([self._date_col, self._symbol_col])
             .collect()
             .select(fields)
         )
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/miniqmt.py` & `vxquant-2023.5.13/src/vxquant/providers/miniqmt.py`

 * *Files 25% similar despite different names*

```diff
@@ -18,40 +18,53 @@
 from vxquant.model.tools.qmtData import (
     qmtTickConvter,
     qmtOrderConvter,
     qmtPositionConvter,
     qmtTradeConvter,
     qmtCashPositionConvter,
     qmtAccountInfoConvter,
+    qmtCreditAccountInfoConvter,
 )
 from vxquant.model.preset import vxMarketPreset
 from vxquant.providers.base import (
+    vxInitProviderContext,
     vxHQProvider,
     vxCalendarProvider,
     vxFeaturesProvider,
     vxGetAccountProvider,
     vxGetPositionsProvider,
     vxOrderBatchProvider,
     vxOrderCancelProvider,
     vxGetExecutionReportsProvider,
     vxGetOrdersProvider,
     ProviderContext,
 )
 from vxsched import vxScheduler, vxContext, vxscheduler
-from vxutils import vxtime, logger, to_timestring
+from vxutils import vxtime, logger, to_timestring, to_text
 
 try:
     from xtquant import xtdata
     from xtquant.xttype import StockAccount
     from xtquant.xttrader import XtQuantTrader, XtQuantTraderCallback
     from xtquant import xtconstant
 except ImportError as e:
     raise ImportError("xtquant未安装，请将QMT安装目录")
 
 
+class QMTAccountType(Enum):
+    """QMT账户类型"""
+
+    NORMAL = xtconstant.SECURITY_ACCOUNT
+    CREDIT = xtconstant.CREDIT_ACCOUNT
+    FUTURE_OPTION = xtconstant.FUTURE_OPTION_ACCOUNT
+    STOCK_OPTION = xtconstant.STOCK_OPTION_ACCOUNT
+    HUGANGTONG = xtconstant.HUGANGTONG_ACCOUNT
+    SHENGANGTONG = xtconstant.SHENGANGTONG_ACCOUNT
+
+
 def to_qmt_symbol(symbol: InstrumentType):
     """将symbol(SHSE.600000) --> QMT的symbol格式(600000.SH)"""
     return f"{symbol[-6:]}.{symbol[:2]}"
 
 
 class vxMiniQMTHQProvider(vxHQProvider):
     """Mini QMT行情接口"""
@@ -64,67 +77,97 @@
         qmt_ticks = xtdata.get_full_tick(qmt_symbols)
         for k, v in qmt_ticks.items():
             v["symbol"] = k
         return dict(map(lambda x: qmtTickConvter(x, "symbol"), qmt_ticks.values()))
 
 
 class vxMiniQMTGetAccountProvider(vxGetAccountProvider):
-    """Mini QMT账户接口"""
+    """Mini QMT普通账户接口"""
 
     def __call__(self, account_id: str = None) -> vxAccountInfo:
-        acc_info = self.context.trader.query_stock_asset(self.context.account)
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+
+        acc_info = self.context.trader.query_stock_asset(account)
         if not acc_info:
             raise ConnectionError(f"无法获取账户信息，请检查连接. {acc_info}")
 
-        qmt_positions = self.context.trader.query_stock_positions(self.context.account)
+        qmt_positions = self.context.trader.query_stock_positions(account)
         fnl = sum(p.market_value - p.open_price * p.volume for p in qmt_positions)
         return qmtAccountInfoConvter(acc_info, fnl=fnl)
 
 
+class vxMiniQMTGetCreditAccountProvider(vxGetAccountProvider):
+    """Mini QMT信用账户接口"""
+
+    def __call__(self, account_id: str = None) -> vxAccountInfo:
+        account = self.context.qmt_accounts.get("CREDIT", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联信用账户. {account}")
+
+        acc_info = self.context.trader.query_credit_detail(account)
+        if not acc_info:
+            raise ConnectionError(f"无法获取账户信息，请检查连接. {acc_info}")
+        acc_info = acc_info[0]
+        return qmtCreditAccountInfoConvter(acc_info)
+
+
 class vxMiniQMTGetPositionsProvider(vxGetPositionsProvider):
     """Mini QMT持仓接口"""
 
     def __call__(
         self, symbol: InstrumentType = None, account_id: str = None
     ) -> Dict[InstrumentType, Union[vxPosition, vxCashPosition]]:
-        qmt_positions = self.context.trader.query_stock_positions(self.context.account)
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+        qmt_positions = self.context.trader.query_stock_positions(account)
         positions = dict(map(lambda x: qmtPositionConvter(x, "symbol"), qmt_positions))
         if symbol:
             return positions.pop(symbol, {})
 
-        acc_info = self.context.trader.query_stock_asset(self.context.account)
+        acc_info = self.context.trader.query_stock_asset(account)
         if not acc_info:
             raise ConnectionError(f"无法获取账户信息，请检查连接. {acc_info}")
         cash_position = qmtCashPositionConvter(acc_info)
         positions["CNY"] = cash_position
         return positions
 
 
 class vxMiniQMTGetOrdersProvider(vxGetOrdersProvider):
     def __call__(
         self, account_id: str = None, filter_finished: bool = False
     ) -> Dict[str, vxOrder]:
-        qmt_orders = self.context.trader.query_stock_orders(
-            self.context.account, filter_finished
-        )
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+        qmt_orders = self.context.trader.query_stock_orders(account, filter_finished)
         return dict(
             map(lambda order: qmtOrderConvter(order, "exchange_order_id"), qmt_orders)
         )
 
 
 class vxMiniQMTGetExecutionReportsProvider(vxGetExecutionReportsProvider):
     def __call__(
         self, account_id: str = None, order_id: str = None, trade_id: str = None
     ) -> Dict[str, vxTrade]:
-        qmt_trades = self.context.trader.query_stock_trades(self.context.account)
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+        qmt_trades = self.context.trader.query_stock_trades(account)
         return dict(map(lambda x: qmtTradeConvter(x, "trade_id"), qmt_trades))
 
 
 class vxMiniQMTOrderBatchProvider(vxOrderBatchProvider):
     def __call__(self, *vxorders) -> List[vxOrder]:
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+
         if len(vxorders) == 1 and isinstance(vxorders[0], (list, tuple, set)):
             vxorders = vxorders[0]
 
         for vxorder in vxorders:
             price_type = (
                 xtconstant.FIX_PRICE
                 if vxorder.order_type.name == "Limit"
@@ -138,15 +181,15 @@
             order_type = (
                 xtconstant.STOCK_BUY
                 if vxorder.order_direction.name == "Buy"
                 else xtconstant.STOCK_SELL
             )
 
             seq_no = self.context.trader.order_stock(
-                account=self.context.account,
+                account=account,
                 stock_code=to_qmt_symbol(vxorder.symbol),
                 order_type=order_type,
                 order_volume=vxorder.volume,
                 price_type=price_type,
                 price=vxorder.price,
                 strategy_name=vxorder.order_id[16:],
                 order_remark=vxorder.order_id[:16],
@@ -167,20 +210,24 @@
 
 
 class vxMiniQMTOrderCancelProvider(vxOrderCancelProvider):
     def __call__(self, *vxorders) -> None:
         if len(vxorders) == 1 and isinstance(vxorders[0], list):
             vxorders = vxorders[0]
 
+        account = self.context.qmt_accounts.get("NORMAL", None)
+        if not account:
+            raise ValueError(f"无法获取账户信息，请QMT是否已关联普通账户. {account}")
+
         for vxorder in vxorders:
             if not vxorder.exchange_order_id:
                 continue
 
             seq = self.context.trader.cancel_order_stock_async(
-                self.context.account, int(vxorder.exchange_order_id.replace("qmt_", ""))
+                account, int(vxorder.exchange_order_id.replace("qmt_", ""))
             )
             if seq <= 0:
                 logger.error(
                     f"委托订单:{vxorder.order_id} 撤单失败{vxorder.symbol} {vxorder.order_direction} {vxorder.volume}"
                 )
         return
 
@@ -188,16 +235,16 @@
 class vxMiniQMTCalendarProvider(vxCalendarProvider):
     def get_trade_dates(
         self,
         market: str = "cn",
         start_date: DateTimeType = None,
         end_date: DateTimeType = None,
     ):
-        start_date = to_timestring(start_date or "19900101", "%Y%m%d")
-        end_date = to_timestring(end_date or "20991231", "%Y%m%d")
+        start_date = to_timestring(start_date, "%Y%m%d") if start_date else "19900101"
+        end_date = to_timestring(end_date, "%Y%m%d") if end_date else "20991231"
         return xtdata.get_trading_calendar("SH", start_date, end_date)
 
 
 class QMTAccountStatus(Enum):
     INVALID = -1
     OK = 0
     WAITING_LOGIN = 1
@@ -215,30 +262,31 @@
     def __init__(
         self,
         context: vxContext,
     ) -> None:
         self._context = context
         if "sched" not in self._context:
             self._context.sched = vxscheduler
-        if "accountdb" not in self._context:
-            self._context.accountdb = vxSQLiteAccountDB()
+
+        # if "accountdb" not in self._context:
+        #    self._context.accountdb = vxSQLiteAccountDB()
 
     def on_connected(self):
         """
         连接成功推送
         """
-        logger.info("连接成功")
+        logger.info("QMT连接成功")
         self._context.sched.submit_events("on_connected")
 
     def on_disconnected(self):
         """
         连接状态回调
         :return:
         """
-        logger.warning("连接断开")
+        logger.warning("QMT连接断开")
         self._context.sched.submit_events("on_disconnected")
 
     def on_account_status(self, status):
         """
         账号状态信息推送
         :param response: XtAccountStatus 对象
         :return:
@@ -266,63 +314,55 @@
         """
         委托信息推送
         :param order: XtOrder对象
         :return:
         """
         broker_order = qmtOrderConvter(order)
         logger.info(
-            f"收到来自broker委托订单 {broker_order.exchange_order_id} 更新为:"
-            f" {broker_order}"
+            f"收到来自broker委托订单 {broker_order.exchange_order_id} 更新为: {broker_order}"
         )
-        with self._context.accountdb.start_session() as session:
-            order = session.update_order(broker_order)
-        if order:
-            self._context.sched.submit_event("on_order_status", order)
+        self._context.sched.submit_event("on_broker_order_status", broker_order)
 
     def on_stock_trade(self, trade):
         """
         成交信息推送
         :param trade: XtTrade对象
         :return:
         """
-        logger.info(
-            f"收到成交信息: {trade.account_id}, {trade.stock_code}, {trade.order_id}"
-        )
+        logger.info(f"收到成交信息: {trade.account_id}, {trade.stock_code}, {trade.order_id}")
 
-        vxtrade = qmtTradeConvter(trade)
+        broker_trade = qmtTradeConvter(trade)
 
-        if vxtrade.status != TradeStatus.Trade:
-            logger.warning(f"收到非成交的回报信息: {vxtrade}")
+        if broker_trade.status != TradeStatus.Trade:
+            logger.warning(f"收到非成交的回报信息: {broker_trade}")
             return
 
         # 调整当日手续费
-        if vxtrade.commission == 0:
-            _preset = vxMarketPreset(vxtrade.symbol)
-            vxtrade.commission = max(
+        if broker_trade.commission == 0:
+            _preset = vxMarketPreset(broker_trade.symbol)
+            broker_trade.commission = max(
                 (
-                    vxtrade.price
-                    * vxtrade.volume
+                    broker_trade.price
+                    * broker_trade.volume
                     * (
                         _preset.commission_coeff_peramount
-                        if vxtrade.order_direction.name == "Buy"
+                        if broker_trade.order_direction.name == "Buy"
                         else (
                             _preset.commission_coeff_peramount
                             + _preset.tax_coeff_peramount
                         )
                     )
                 ),
                 0.5,
             )
-        with self._context.accountdb.start_session() as session:
-            trade = session.update_trade(vxtrade)
-        if trade:
-            self._context.sched.submit_event("on_execution_report", vxtrade)
-        # logger.info(
-        #    f"收到来自broker成交回报信息 {vxtrade.exchange_order_id}: {vxtrade}"
-        # )
+
+        self._context.sched.submit_event("on_broker_execution_report", broker_trade)
+        logger.info(
+            f"收到来自broker成交回报信息 {broker_trade.exchange_order_id}: {broker_trade}"
+        )
 
     def on_stock_position(self, xtposition):
         """
         持仓信息推送
         :param position: XtPosition对象
         :return:
         """
@@ -339,34 +379,30 @@
         """
         # order_error.order_id = f"qmt_{order_error.order_id}"
         logger.warning(
             "收到委托订单错误反馈:"
             f" {order_error.order_id},"
             f" {order_error.error_id}, {order_error.error_msg}"
         )
-
         try:
-            with self._context.accountdb.start_session() as session:
-                vxorder = session.findone(
-                    "orders", exchange_order_id=f"qmt_{order_error.order_id}"
-                )
-                if not vxorder:
-                    logger.warning(
-                        f"收到来自broker委托订单 qmt_{order_error.order_id} 未找到"
-                    )
-                    return
-                vxorder.status = OrderStatus.Rejected
-                vxorder.reject_code = OrderRejectReason.UnknownOrder
-                vxorder.reject_reason = order_error.error_msg
-                order = self._context.accountdb.update_order(vxorder)
-                if order:
-                    self._context.sched.submit_event("on_order_status", order)
-
+            exchange_order_id = f"qmt_{order_error.order_id}"
+            orders = self._context.teller.get_orders(
+                exchange_order_id=exchange_order_id
+            )
+            if exchange_order_id not in orders:
+                logger.warning(f"收到来自broker委托订单 qmt_{order_error.order_id} 未找到")
+                return
+            vxorder = orders[exchange_order_id]
+            vxorder.status = OrderStatus.Rejected
+            vxorder.reject_code = OrderRejectReason.UnknownOrder
+            vxorder.reject_reason = f"{order_error.error_msg}"
+            self._context.sched.submit_event("on_broker_order_status", vxorder)
+            logger.debug(f"收到来自broker委托订单 {vxorder.exchange_order_id} 更新为: {vxorder}")
         except Exception as e:
-            logger.error(f"发生异常错误：{e}")
+            logger.error(e, exc_info=True)
 
     def on_order_stock_async_response(self, response):
         """
         :param response: XtOrderResponse 对象
         :return:
         """
         # with self.lock:
@@ -377,29 +413,39 @@
     def on_smt_appointment_async_response(self, response):
         """
         :param response: XtAppointmentResponse 对象
         :return:
         """
 
 
-def init_provider_context(
-    context: vxContext,
-    miniqmt_path: Union[str, Path],
-    account_id: str = None,
-    account_type: str = "STOCK",
-) -> None:
-    context.account = StockAccount(account_id, account_type)
-    context.trader = XtQuantTrader(miniqmt_path, int(vxtime.now()))
-    callback = vxQMTTraderCallback(context)
-
-    context.trader.start()
-    connect_result = context.trader.connect()
-    if connect_result != 0:
-        raise ConnectionError(f"连接失败: {connect_result}")
-    logger.info(f"trader 连接成功. {context.trader}")
-
-    context.trader.register_callback(callback)
-    subscribe_result = context.trader.subscribe(context.account)
-    if subscribe_result != 0:
-        raise ConnectionError(f"订阅失败: {subscribe_result}")
-    logger.info(f"订阅账号回调信息: {context.account}")
-    return context
+class vxInitMinitQMTProviderContext(vxInitProviderContext):
+    def __init__(self, miniqmt_path: Union[str, Path]):
+        self._miniqmt_path = str(miniqmt_path)
+        super().__init__()
+
+    def set_context(self, context: vxContext, **kwargs):
+        if (
+            self._context
+            and "trader" in self._context
+            and "qmt_accounts" in self._context
+        ):
+            return
+
+        context.trader = XtQuantTrader(self._miniqmt_path, int(vxtime.now()))
+        context.trader.start()
+        connect_result = context.trader.connect()
+        if connect_result != 0:
+            raise ConnectionError(f"连接失败: {connect_result}")
+        logger.info(f"trader 连接成功. {context.trader}")
+
+        callback = vxQMTTraderCallback(context)
+        context.trader.register_callback(callback)
+        accounts = context.trader.query_account_infos()
+        context.qmt_accounts = {}
+
+        for account in accounts:
+            subscribe_result = context.trader.subscribe(account)
+            if subscribe_result != 0:
+                raise ConnectionError(f"订阅失败: {subscribe_result}")
+            logger.info(f"订阅账号回调信息: {account}")
+            context.qmt_accounts[QMTAccountType(account.account_type).name] = account
+        return
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/mongo.py` & `vxquant-2023.5.13/src/vxquant/providers/mongo.py`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     vxAccountInfo,
     vxOrder,
     vxPosition,
     vxCashPosition,
     vxTrade,
 )
 from vxutils import logger
-from vxutils.dbproxy import vxMongoProxy
+from vxutils.database.dbproxy import vxMongoProxy
 
 _mongodb_lock = Lock()
 
 
 class vxMongoGetAccountProvider(vxGetAccountProvider):
     def __init__(self) -> None:
         if "dbconn" not in self.context.keys():
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/spiders/calendar_sse.py` & `vxquant-2023.5.13/src/vxquant/providers/spiders/calendar_sse.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/providers/spiders/hq_tencent.py` & `vxquant-2023.5.13/src/vxquant/providers/spiders/hq_tencent.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/providers/tdx.py` & `vxquant-2023.5.13/src/vxquant/providers/tdx.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,25 +1,22 @@
 """tdx行情"""
 
 import time
-import json
 from enum import Enum
-from contextlib import contextmanager, suppress
-from tqdm import tqdm
+from contextlib import suppress
+
 from typing import List, Dict
-from queue import PriorityQueue, Queue
-from heapq import heapify, heappop, heappush
+from queue import PriorityQueue
 from multiprocessing import Lock
 from functools import reduce
-from vxutils import logger, vxtime, singleton, diskcache, vxLRUCache
 from concurrent.futures import ThreadPoolExecutor, as_completed
+from tqdm import tqdm
+from vxutils import logger, vxtime, diskcache
 from vxquant.model.exchange import vxTick
 from vxquant.model.nomalize import to_symbol
-from vxquant.model.preset import vxMarketPreset
-from vxquant.model.contants import SecType
 from vxquant.model.typehint import InstrumentType
 from vxquant.model.tools.tdxData import tdxTickConvter
 from vxquant.providers.base import vxHQProvider
 
 try:
     from pytdx.hq import TdxHq_API, TDXParams
     from pytdx.config.hosts import hq_hosts
@@ -57,19 +54,19 @@
     return f"{TDXExchange(market).name}.{code}"
 
 
 class TdxHq_APIPool:
     """tdx行情接口池"""
 
     _hosts = PriorityQueue()
-    _apis = Queue()
+    _apis = PriorityQueue()
     _lock = Lock()
 
     def __init__(self):
-        self._cost = None
+        # self._cost = None
         self._api = None
         with self._lock:
             self.reflash_hosts()
 
     @classmethod
     def reflash_hosts(cls) -> None:
         if cls._hosts.qsize() >= 10:
@@ -89,60 +86,68 @@
                 with suppress(TimeoutError):
                     if tdxapi.connect(host, port, time_out=1):
                         cost = (time.perf_counter() - start) * 1000
                         tdxapi.disconnect()
                         data.append((cost, host, port))
 
             if data:
-                diskcache.set(__TDXHOSTS__, data, ttl=24 * 60 * 60)
+                diskcache.set(__TDXHOSTS__, data, expired_dt=vxtime.today("23:59:59"))
 
         [cls._hosts.put(item) for item in data]
 
     def __enter__(self):
         with self._lock:
             self.reflash_hosts()
 
         while self._apis.qsize() > 0:
-            self._api, lastconnect_dt = self._apis.get_nowait()
+            lastconnect_dt, self._api = self._apis.get_nowait()
             if (lastconnect_dt + 60 < vxtime.now()) or (self._api.do_heartbeat()):
                 return self._api
 
         while not self._hosts.empty():
-            self._cost, host, port = self._hosts.get_nowait()
+            cost, host, port = self._hosts.get_nowait()
             try:
-                start = time.perf_counter()
                 self._api = TdxHq_API()
-                self._api
                 if self._api.connect(host, port, time_out=0.7):
-                    self._cost = time.perf_counter() - start
                     return self._api
             except Exception as e:
                 logger.info(f"连接至:{host}:{port} 发生错误: {e}", exc_info=True)
 
     def __exit__(self, exc_type, exc_val, exc_tb):
         if exc_type is None or self._api.do_heartbeat():
-            self._apis.put_nowait((self._api, vxtime.now()))
+            self._apis.put_nowait((vxtime.now(), self._api))
 
 
 class TdxHQProvider(vxHQProvider):
     def _hq(self, *symbols: List[InstrumentType]) -> Dict[InstrumentType, vxTick]:
         if len(symbols) == 1 and isinstance(symbols[0], list):
             symbols = symbols[0]
 
         if not symbols:
             return {}
 
         tdxsymbols = [to_tdx_symbol(symbol) for symbol in symbols]
         results = {}
 
         with TdxHq_APIPool() as api:
+            missing_tdxsymbols = []
             for i in range(0, len(tdxsymbols), 80):
                 data = api.get_security_quotes(tdxsymbols[i : i + 80])
                 if data and len(data) == len(tdxsymbols[i : i + 80]):
                     results.update(map(lambda x: tdxTickConvter(x, key="symbol"), data))
+                else:
+                    missing_tdxsymbols.append(tdxsymbols[i : i + 80])
+            if missing_tdxsymbols:
+                vxtime.sleep(0.1)
+                for symbol in missing_tdxsymbols:
+                    data = api.get_security_quotes([symbol])
+                    if data:
+                        results.update(
+                            map(lambda x: tdxTickConvter(x, key="symbol"), data)
+                        )
         return results
 
 
 class MultiTdxHQProvider(vxHQProvider):
     def __init__(self) -> None:
         self._executor = ThreadPoolExecutor(5)
 
@@ -168,30 +173,46 @@
         return reduce(_r, as_completed(rets), {})
 
     def _tdx_get_security_quotes(
         self, symbols: List[InstrumentType]
     ) -> Dict[InstrumentType, vxTick]:
         tdxsymbols = [to_tdx_symbol(symbol) for symbol in symbols]
         results = {}
+        missing_tdxsymbols = []
 
         with TdxHq_APIPool() as api:
             for i in range(0, len(tdxsymbols), 80):
                 data = api.get_security_quotes(tdxsymbols[i : i + 80])
                 if data and len(data) == len(tdxsymbols[i : i + 80]):
                     results.update(map(lambda x: tdxTickConvter(x, key="symbol"), data))
+                else:
+                    missing_tdxsymbols.extend(tdxsymbols[i : i + 80])
+            if missing_tdxsymbols:
+                vxtime.sleep(0.1)
+                for symbol in missing_tdxsymbols:
+                    data = api.get_security_quotes([symbol])
+                    if data:
+                        results.update(
+                            map(lambda x: tdxTickConvter(x, key="symbol"), data)
+                        )
+
         return results
 
 
 if __name__ == "__main__":
+    from vxutils import to_datetime
+
     with TdxHq_APIPool() as tdxapi:
         print("hello world")
 
     with vxtime.timeit("create hqapi"):
         hq_api = MultiTdxHQProvider()
 
+    # print(diskcache.get("__suspend_symbols__"))
+
     symbols = [
         "SHSE.110043",
         "SHSE.110044",
         "SHSE.110045",
         "SHSE.110047",
         "SHSE.110048",
         "SHSE.110052",
@@ -695,8 +716,11 @@
 
     with vxtime.timeit():
         data = hq_api(symbols)
         print(len(set(symbols)), len(data))
 
     import polars as pl
 
-    print(pl.DataFrame([tick.message for tick in data.values()]))
+    df = pl.DataFrame([tick.message for tick in data.values()]).with_columns(
+        [pl.col(["created_dt", "updated_dt"]).apply(to_datetime)]
+    )
+    print(df)
```

### Comparing `vxquant-2023.4.1/src/vxquant/providers/zeromq.py` & `vxquant-2023.5.13/src/vxquant/providers/zeromq.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxquant/tdapi/base.py` & `vxquant-2023.5.13/src/vxutils/time.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,153 +1,149 @@
-"""交易接口"""
+"""量化交易时间计时器"""
 
-import pandas as pd
-from abc import ABC, abstractmethod
-from typing import Dict, List, Optional, Union
-from vxquant.model.preset import vxMarketPreset
-from vxutils import vxtime
-from vxquant.model.exchange import (
-    vxAccountInfo,
-    vxAlgoOrder,
-    vxCashPosition,
-    vxOrder,
-    vxPosition,
-    vxTick,
-    vxTrade,
-)
-from vxquant.model.contants import (
-    OrderDirection,
-    OrderOffset,
-    OrderStatus,
-    OrderType,
-    SecType,
+
+import time
+import contextlib
+from multiprocessing.dummy import Process, Condition
+from typing import Any, Callable, List
+from vxutils.convertors import (
+    combine_datetime,
+    to_timestring,
+    to_datetime,
+    to_timestamp,
 )
 
 
-class vxTdAPIBase(ABC):
-    """交易接口类"""
+__all__ = ["vxtime"]
+
+
+class _ShowProcessBar(Process):
+    def __init__(self, prefix: str, *args, **kwargs) -> None:
+        from tqdm import tqdm
+
+        self._is_started = False
+        self._prefix = prefix
+        self._start_dt = None
+        self._keep_waiting = Condition()
+        self._pbar = tqdm()
+        super().__init__(*args, **kwargs)
+
+    def run(self) -> None:
+        self._is_started = True
+        self._start_dt = time.perf_counter()
+        with self._keep_waiting:
+            while self._is_started:
+                self._pbar.set_description(
+                    f"计时器({self._prefix})  用时"
+                    f" {(time.perf_counter()-self._start_dt)*1000:,.2f}ms"
+                )
+                self._pbar.update()
+                self._keep_waiting.wait(1)
+
+    def stop(self) -> None:
+        with self._keep_waiting:
+            cost_time = (time.perf_counter() - self._start_dt) * 1000
+            self._is_started = False
+            self._keep_waiting.notify()
+            self._pbar.set_description(
+                f"计时器({self._prefix}) 用时 {cost_time:,.2f}ms"
+            )
+            self._pbar.close()
+        self.join()
+        return cost_time
+
+
+class vxtime:
+    """量化交易时间机器"""
+
+    _timefunc = time.time
+    _delayfunc = time.sleep
+    __holidays__ = set()
+    __businessdays__ = set()
+
+    @classmethod
+    def now(cls) -> float:
+        """当前时间"""
+        return cls._timefunc()
+
+    @classmethod
+    def sleep(cls, seconds: float) -> None:
+        """延时等待函数"""
+        cls._delayfunc(seconds)
+
+    @classmethod
+    @contextlib.contextmanager
+    def timeit(
+        cls, prefix: str = None, show_title: bool = False, show_pbar: bool = False
+    ) -> None:
+        """计时器"""
+        pbar = _ShowProcessBar(prefix or "default")
+        pbar.start()
+        try:
+            yield
+        finally:
+            pbar.stop()
+
+    @classmethod
+    def is_holiday(cls, date_: Any = None) -> bool:
+        """是否假日"""
+        date_ = date_ if date_ is not None else cls.now()
+        if to_datetime(date_).weekday in [0, 1]:
+            # 星期六日 均为休息日
+            return True
+
+        date_ = to_timestring(date_, "%Y-%m-%d")
+        return date_ in cls.__holidays__
+
+    @classmethod
+    def set_timefunc(cls, timefunc: Callable) -> None:
+        """设置timefunc函数"""
+        if not callable(timefunc):
+            raise ValueError(f"{timefunc} is not callable.")
+        cls._timefunc = timefunc
+
+    @classmethod
+    def set_delayfunc(cls, delayfunc: Callable) -> None:
+        """设置delayfunc函数"""
+        if not callable(delayfunc):
+            raise ValueError(f"{delayfunc} is not callable.")
+        cls._delayfunc = delayfunc
+
+    @classmethod
+    def today(cls, time_str: str = "00:00:00") -> float:
+        """今天 hh:mm:ss 对应的时间"""
+
+        date_str = to_timestring(cls.now(), "%Y-%m-%d")
+        return combine_datetime(date_str, time_str)
+
+    @classmethod
+    def add_holidays(cls, *holidays: List):
+        """增加假期时间"""
+        if len(holidays) == 1 and isinstance(holidays[0], list):
+            holidays = holidays[0]
+        cls.__holidays__.update(map(lambda d: to_timestring(d, "%Y-%m-%d"), holidays))
+
+    def get_next_business_day(self, date_: Any = None) -> float:
+        """获取下一个交易日"""
+
+        date_ = to_timestamp(date_ if date_ is not None else self.now())
+
+        while self.is_holiday(date_):
+            date_ += 24 * 60 * 60
+        return date_
+
+
+if __name__ == "__main__":
+    with vxtime.timeit("test2"):
+        print(11)
+        with vxtime.timeit("step 1"):
+            vxtime.sleep(1)
+        with vxtime.timeit("step 2"):
+            vxtime.sleep(2)
+
+        with vxtime.timeit("setp 3"):
+            vxtime.sleep(3)
+
+        with vxtime.timeit("step 4"):
+            vxtime.sleep(4)
 
-    def __init__(self):
-        self._cache = {}
-        self._cached_at = 0
-
-    @abstractmethod
-    def get_ticks(self, *symbols) -> Dict[str, vxTick]:
-        """获取最新的ticks 数据
-
-        Returns:
-            Dict[str,vxTick] -- 返回最新的tick数据
-        """
-
-    def current(self, *symbols: List[str]) -> Dict[str, vxTick]:
-        """实时行情信息
-
-        Arguments:
-            symbols {List[str]} -- 证券交易代码
-        """
-        if not symbols:
-            raise ValueError("symbols must not null.")
-
-        if isinstance(symbols[0], list):
-            symbols = symbols[0]
-
-        symbols = list(symbols)
-
-        now = vxtime.now()
-        if now > (self._cached_at + 3):
-            symbols.extend(self._cache.keys())
-            self._cache = {}
-            self._cached_at = now
-
-        target_symbols = set(symbols) - set(self._cache.keys())
-        vxticks = self.get_ticks(*target_symbols)
-        self._cache.update(vxticks)
-
-        return {
-            symbol: self._cache[symbol] for symbol in symbols if symbol in self._cache
-        }
-
-    @abstractmethod
-    def get_account(self) -> vxAccountInfo:
-        """获取账户基本信息"""
-
-    @abstractmethod
-    def get_positions(
-        self, symbol: str = None
-    ) -> Dict[str, Union[vxCashPosition, vxPosition]]:
-        """获取持仓信息
-
-        Keyword Arguments:
-            symbol {str} -- 对应的持仓信息 (default: {None})
-
-        Returns:
-            Dict[str, Union[vxCashPosition,vxPosition]] -- 返回持仓列表
-        """
-
-    @abstractmethod
-    def order_batch(self, *vxorders: List[vxOrder]) -> List[vxOrder]:
-        """提交委托订单
-
-        Arguments:
-            vxorders {List[vxOrder]} -- 待提交的委托订单
-        """
-
-    def order_volume(
-        self, symbol: str, volume: int, price: Optional[float] = 0
-    ) -> vxOrder:
-        """下单
-
-        Arguments:
-            account_id {str} -- _description_
-            symbol {str} -- _description_
-            volume {int} -- _description_
-            price {Optional[float]} -- _description_ (default: {None})
-
-        Returns:
-            vxorder {vxOrder} -- 下单委托订单号
-        """
-        if volume == 0:
-            raise ValueError("volume can't be 0.")
-
-        if (
-            not price
-            and vxMarketPreset(symbol).security_type == SecType.BOND_CONVERTIBLE
-        ):
-            ticks = self.current(symbol)
-            price = ticks[symbol].ask1_p if volume > 0 else ticks[symbol].bid1_p
-
-        vxorder = vxOrder(
-            symbol=symbol,
-            volume=abs(volume),
-            price=price,
-            order_offset=OrderOffset.Open if volume > 0 else OrderOffset.Close,
-            order_direction=OrderDirection.Buy if volume > 0 else OrderDirection.Sell,
-            order_type=OrderType.Market if price <= 0 else OrderType.Limit,
-            status=OrderStatus.PendingNew,
-        )
-
-        ret_orders = self.order_batch(vxorder)
-        return ret_orders[0]
-
-    @abstractmethod
-    def get_orders(self) -> List[vxOrder]:
-        """获取当日委托订单列表
-
-        Returns:
-            List[vxOrder] -- 当日委托订单列表
-        """
-
-    @abstractmethod
-    def get_execution_reports(self) -> List[vxTrade]:
-        """获取当日成交回报信息
-
-        Returns:
-            List[vxTrade] -- 当日成交回报列表
-        """
-
-    @abstractmethod
-    def order_cancel(self, *orders: List[vxOrder]) -> None:
-        """撤单
-
-        Arguments:
-            orders {List[vxOrder]} -- 待撤销订单
-        """
+        vxtime.sleep(0.3)
```

### Comparing `vxquant-2023.4.1/src/vxsched/__init__.py` & `vxquant-2023.5.13/src/vxsched/__init__.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxsched/__main__.py` & `vxquant-2023.5.13/src/vxsched/__main__.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,13 +1,20 @@
 """vxsched 主函数"""
 import argparse
+import sys
 from vxutils import logger
 from vxsched import vxscheduler
 
-if __name__ == "__main__":
+
+def main(args=None):
+    if args is None:
+        args = sys.argv[1:]
+    if len(args) == 0:
+        args = ["-h"]
+
     parser = argparse.ArgumentParser()
 
     parser.add_argument(
         "-c",
         "--config",
         help="config json file path: etc/config.json",
         default="config.json",
@@ -21,7 +28,11 @@
     )
     args = parser.parse_args()
 
     if args.verbose:
         logger.setLevel("DEBUG")
 
     vxscheduler.server_forever(config=args.config, mod=args.mod)
+
+
+if __name__ == "__main__":
+    main()
```

### Comparing `vxquant-2023.4.1/src/vxsched/context.py` & `vxquant-2023.5.13/src/vxsched/context.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxsched/core.py` & `vxquant-2023.5.13/src/vxsched/core.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,22 +1,22 @@
-import os
-import importlib
+"""vxsched调度器 """
+
 import contextlib
-from pathlib import Path
+import importlib
+import os
 import time
-from queue import Empty
-from itertools import chain
 
 from collections import defaultdict
-from typing import Any, Union, Callable
-from concurrent.futures import ThreadPoolExecutor as Executor
-from multiprocessing.dummy import Process, Lock
-from vxutils import logger, vxWrapper, vxtime
-from vxsched.event import vxEvent, vxTrigger, vxEventQueue
+from multiprocessing.dummy import Lock, Process
+from pathlib import Path
+from queue import Empty
+from typing import Any, List, Callable, Union
 from vxsched.context import vxContext
+from vxsched.event import vxEvent, vxEventQueue, vxTrigger
+from vxutils import logger, vxtime
 
 
 __all__ = ["vxScheduler", "vxscheduler"]
 
 _default_context = {
     "settings": {},
     "params": {},
@@ -24,44 +24,46 @@
         "class": "concurrent.futures.ThreadPoolExecutor",
         "params": {"thread_name_prefix": "vxSchedThread"},
     },
 }
 
 
 class vxTask:
+    """调度任务类"""
+
     def __init__(
         self, handler: Callable, time_limit: float = 1.0, lock: Lock = None
     ) -> None:
         self._handler = handler
         self.time_limit = time_limit
         self.lock = lock
         self.cost_time = 0
 
     def __call__(self, context: vxContext, event: vxEvent) -> Any:
+        start = time.perf_counter()
         try:
-            start = time.perf_counter()
             if self.lock:
                 with self.lock:
                     ret = self._handler(context, event)
             else:
                 ret = self._handler(context, event)
-        except KeyboardInterrupt:
+        except KeyboardInterrupt as user_abort:
             ret = None
-            logger.warning("用户提前终止... ")
+            logger.error(f"{self} 用户提前终止...")
+            raise KeyboardInterrupt("用户提前终止... ") from user_abort
 
         except Exception as err:
             ret = err
             logger.error(f"{self} run handler error: {err}", exc_info=True)
 
         finally:
             self.cost_time = time.perf_counter() - start
             if self.cost_time > self.time_limit:
                 logger.warning(
-                    f"{self._handler} 运行时间 {self.cost_time*1000:,.2f}ms.  触发消息:"
-                    f" {event}"
+                    f"{self._handler} 运行时间 {self.cost_time*1000:,.2f}ms.  触发消息: {event}"
                 )
 
         return ret
 
     def __eq__(self, _other: object) -> bool:
         if isinstance(_other, vxTask):
             return self._handler == _other._handler
@@ -76,89 +78,70 @@
 
     __repr__ = __str__
 
 
 class vxScheduler:
     def __init__(self):
         self._context = None
-        self._executor = None
-        self._map_func = map
         self._queue = vxEventQueue()
         self._handlers = defaultdict(set)
         self._active = False
         self._is_initialized = False
         self._worker_threads = []
 
     def __str__(self) -> str:
         return f"{self.__class__.__name__}(id-{id(self)})"
 
     __repr__ = __str__
 
     @property
     def context(self):
+        """上下文环境"""
         return self._context
 
-    def initialize(
-        self,
-        context: vxContext = None,
-        executor: Executor = None,
-    ) -> None:
+    def initialize(self, context: vxContext = None) -> None:
+        """初始化"""
         if self._is_initialized is True:
             logger.warning("已经初始化，请勿重复初始化")
             return
 
-        self._executor = executor
-        self._map_func = executor.map if hasattr(executor, "map") else map
-
-        # self._context = context or self._context or vxContext(_default_context)
-        if context is not None:
-            self._context = context
-            logger.debug(f"更新context内容: {self.context}")
-        elif self._context is None:
-            self._context = vxContext(_default_context)
-            logger.debug(f"创建缺省context内容: {self.context}")
-
+        self._context = context or self._context or vxContext(_default_context)
         self.submit_event("__init__")
         self.trigger_events()
         self._is_initialized = True
         logger.info(f"{self} 触发初始化完成 ... ")
 
     def is_alive(self):
         """是否运行中"""
         return self._active
 
-    def trigger_events(self, *trigger_events) -> None:
+    def trigger_events(self, *trigger_events) -> List:
         """同步触发已到期的消息"""
         if len(trigger_events) == 1 and isinstance(trigger_events[0], list):
             trigger_events = trigger_events[0]
 
-        events = defaultdict(list)
-        for t_event in trigger_events:
-            events[t_event.id].append(t_event)
+        events = {t_event.id: t_event for t_event in trigger_events}
 
         with contextlib.suppress(Empty):
             while not self._queue.empty():
-                event = self._queue.get_nowait()
-                events[event.id].append(event)
-
-        if not events:
-            return None
-
-        handlers = chain.from_iterable(
-            self._handlers[event.type]
-            for event in map(max, events.values())
-            if self._handlers[event.type]
-        )
-
-        return list(
-            self._map_func(
-                lambda handler: self._run_handler(event=event, handler=handler),
-                handlers,
+                q_event = self._queue.get_nowait()
+                if q_event.id not in events or q_event > events[q_event.id]:
+                    events[q_event.id] = q_event
+
+        return [
+            list(
+                map(
+                    lambda hdl: self._run_handler(hdl, event),
+                    self._handlers[event.type],
+                )
             )
-        )
+            for event in events.values()
+        ]
+
+        return
 
     def submit_event(
         self,
         event: Union[vxEvent, str],
         data: Any = None,
         trigger: vxTrigger = None,
         priority: float = 10,
@@ -179,29 +162,34 @@
             send_event = event
         else:
             raise ValueError(f"{self} event 类型{type(event)}错误，请检查: {event}")
 
         logger.debug(f"提交消息: {send_event}")
         self._queue.put_nowait(send_event)
 
-    def _run_handler(self, handler: Callable, event: vxEvent) -> None:
-        """单独运行一个handler"""
-
-        ret = handler(self.context, event)
+    def handle_reply(self, handler: vxTask, event: vxEvent, ret: Any):
+        """处理回复消息"""
         if (
             event.type != "__handle_timerecord__"
             and self._handlers["__handle_timerecord__"]
         ):
             self.submit_event(
                 "__handle_timerecord__", (str(handler), event, handler.cost_time)
             )
-
         if event.reply_to and self._handlers["__handle_reply__"]:
             self.submit_event("__handle_reply__", (event, ret))
 
+    def _run_handler(self, handler: Callable, event: vxEvent) -> None:
+        """单独运行一个handler"""
+
+        ret = None
+        try:
+            ret = handler(self.context, event)
+        finally:
+            self.handle_reply(handler, event, ret)
         return ret
 
     def register(
         self,
         event_type: str,
         time_limit: float = 1.0,
         lock: Lock = None,
@@ -240,96 +228,93 @@
             return handler
 
         return deco
 
     def run(
         self,
         context: vxContext = None,
-        executor: Executor = None,
     ) -> None:
         if self._is_initialized is False:
-            self.initialize(context, executor)
-
+            self.initialize(context)
         self._active = True
-
         self._run()
 
     def _run(self) -> None:
         """单个线程运行"""
         logger.info(f"{self} worker 开始运行...")
         try:
             while self._active:
                 with contextlib.suppress(Empty):
                     event = self._queue.get(timeout=1.0)
 
                     if self._handlers[event.type]:
                         list(
-                            self._map_func(
+                            map(
                                 lambda hdl: self._run_handler(hdl, event=event),
                                 self._handlers[event.type],
                             )
                         )
 
         finally:
             self._active = False
             logger.info(f"{self} worker 结束运行...")
 
     def start(
         self,
         context: vxContext = None,
-        executor: Executor = None,
         blocking: bool = False,
+        workers: int = 5,
     ) -> None:
         """启动调度器"""
         if self._active:
             logger.info(f"{self} 已经激活运行...")
             return
 
         if self._is_initialized is False:
-            self.initialize(context, executor)
+            self.initialize(context)
 
         self._active = True
         self._worker_threads = []
-        for i in range(5):
-            t = Process(target=self._run, name=f"vxSchedWorker{i}")
+        for i in range(workers):
+            t = Process(target=self._run, name=f"vxWorker{i}")
             t.daemon = True
             t.start()
             self._worker_threads.append(t)
 
         if blocking:
-            for t in self._worker_threads:
-                if t.is_alive():
-                    t.join()
+            try:
+                while self._active:
+                    vxtime.sleep(1.0)
+            except Exception:
+                self.stop()
+
         return
 
     def stop(self) -> None:
         """停止调度器"""
         self._active = False
         for t in self._worker_threads:
             if t.is_alive():
                 t.join()
 
     def server_forever(
         self, config: Union[str, Path] = None, mod: Union[str, Path] = "mod/"
     ):
         if isinstance(config, str):
             config = Path(config)
+        elif config is None:
+            config = Path("config.json")
 
         context = (
             vxContext.load_json(config.absolute(), _default_context)
             if config.exists()
             else vxContext(_default_context)
         )
-        executor_settings = context.get("executor", None)
-        if executor_settings is not None:
-            executor = vxWrapper.init_by_config(executor_settings)
-        else:
-            executor = Executor(thread_name_prefix="vxSchedThread")
         self.load_modules(mod)
-        self.start(context=context, executor=executor, blocking=True)
+        self.start(context=context, blocking=True)
 
     def load_modules(self, mod_path: Union[str, Path]) -> Any:
         """加载策略目录"""
         if isinstance(mod_path, Path):
             mod_path = mod_path.absolute()
 
         if not os.path.exists(mod_path):
@@ -352,7 +337,10 @@
                     logger.info("+" * 80)
                 except Exception as err:
                     logger.error(f"Load Module: {mod} Failed. {err}", exc_info=True)
                     logger.error("-" * 80)
 
 
 vxscheduler = vxScheduler()
+
+if __name__ == "__main__":
+    vxscheduler.server_forever()
```

### Comparing `vxquant-2023.4.1/src/vxsched/event.py` & `vxquant-2023.5.13/src/vxsched/event.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxsched/triggers/daily.py` & `vxquant-2023.5.13/src/vxsched/triggers/daily.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxsched/triggers/interval.py` & `vxquant-2023.5.13/src/vxsched/triggers/interval.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxsched/triggers/weekly.py` & `vxquant-2023.5.13/src/vxsched/triggers/weekly.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/__init__.py` & `vxquant-2023.5.13/src/vxutils/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -60,35 +60,32 @@
     vxBoolField,
     vxBytesField,
     vxDataMeta,
     vxDataClass,
     vxDataConvertor,
     vxDict,
 )
+from vxutils.dataorm import vxDataBase, vxDBSession
 from vxutils.debug import debug_log
 from vxutils.cache import (
     MissingCache,
-    CacheUnit,
-    DiskCacheUnit,
-    vxLRUCache,
+    vxCache,
     diskcache,
-    vxSQLiteCache,
 )
 
 setattr(builtins, "debug_log", debug_log)
 setattr(builtins, "logger", logger)
 setattr(builtins, "vxtime", vxtime)
 
 __all__ = [
     "diskcache",
     "MissingCache",
-    "CacheUnit",
-    "DiskCacheUnit",
-    "vxLRUCache",
-    "vxSQLiteCache",
+    "vxCache",
+    "vxDataBase",
+    "vxDBSession",
     "to_timestring",
     "to_datetime",
     "to_timestamp",
     "to_enum",
     "to_json",
     "combine_datetime",
     "vxJSONEncoder",
```

### Comparing `vxquant-2023.4.1/src/vxutils/cache.py` & `vxquant-2023.5.13/src/vxutils/dataclass.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,555 +1,671 @@
-"""缓存
+# encoding=utf-8
+""" 定制的数据类型
 
-支持
+vxDataClass
+vxDict
 
 """
 
+
+import zlib
+import math
+import uuid
 import pickle
-import inspect
-import hashlib
 from pathlib import Path
-from collections import OrderedDict
-from typing import Any, Dict, Type, Union, Callable, List
-from vxutils import vxtime, to_timestring, to_timestamp, to_json, logger
+from enum import Enum
+from functools import singledispatch
+from collections import UserDict
+from collections.abc import MutableMapping, Mapping, Sequence
+from typing import Any, Callable, Optional, List, Dict
+from operator import getitem
+from vxutils import (
+    vxtime,
+    vxJSONEncoder,
+    to_json,
+    to_enum,
+    to_timestamp,
+    to_timestring,
+    to_binary,
+)
 
+try:
+    import simplejson as json
+except ImportError:
+    import json
+
+
+__all__ = [
+    "vxField",
+    "vxUUIDField",
+    "vxEnumField",
+    "vxIntField",
+    "vxFloatField",
+    "vxPropertyField",
+    "vxDatetimeField",
+    "vxBoolField",
+    "vxDataMeta",
+    "vxDataClass",
+    "vxDataConvertor",
+    "vxDict",
+]
+
+
+class vxField:
+    """字段属性描述符
+
+    default_factory: 缺省值 或缺省值生成函数
+        ---> default_factory()
+
+    convertor_factory: 类型转换函数
+        ---> convertor_factory(input_value) -> value
+        ---> 例如: lambda x: to_timestring(x)
+
+    property_factory: 属性函数字段
+        ---> property_factory(obj)  -> value
+        ---> 例如: lambda obj: obj.x+obj.y
+
+    format_factory: 格式化输入函数
+        ---> fortmat_factory(value) ---> string
+        ---> 例如：lambda value: to_timestring(value, '%Y-%m-%d %H:%M:%S')
+
+
+    """
+
+    __slots__ = [
+        "_name",
+        "_fget",
+        "_fset",
+        "_property_factory",
+        "_default_factory",
+        "_convertor_factory",
+        "_format_factory",
+    ]
 
-__all__ = ["MissingCache", "CacheUnit", "DiskCacheUnit", "vxLRUCache", "vxSQLiteCache"]
-_ENDOFTIME = to_timestamp("2199-12-31 23:59:59")
+    def __init__(
+        self,
+        default_factory: Any = None,
+        convertor_factory: Callable = None,
+        property_factory: Callable = None,
+        format_factory: Callable = None,
+    ):
+        self._fget = None
+        self._fset = None
+        self._property_factory = property_factory
+        self._default_factory = (
+            default_factory if callable(default_factory) else lambda: default_factory
+        )
+        self._convertor_factory = convertor_factory
+        self._format_factory: Callable = format_factory
+        self._name = None
+
+    def __set_name__(self, owner, name):
+        """设置属性名称"""
+
+        self._name = f"_{name}"
+        # 设置获取attr的方法
+        if callable(self._property_factory):
+            self._fget = lambda obj, owner: self._property_factory(obj)
+            self._fset = None
+            return
 
+        self._fget = lambda obj, owner: getattr(obj, self._name, self.default)
 
-class MissingCache(Exception):
-    pass
+        if self._name == "_updated_dt":
 
+            def fset(obj, value):
+                setattr(obj, "_updated_dt", self._convertor_factory(value))
 
-class CacheUnit:
-    _key = None
-    _value = None
-    _expired_dt = _ENDOFTIME
+        elif callable(self._convertor_factory):
 
-    def __init__(self, key: str, value: Any, expired_dt: float = None) -> None:
-        self._key = key
-        self._value = value
-        self._expired_dt = to_timestamp(expired_dt or _ENDOFTIME)
+            def fset(obj, value):
+                setattr(obj, self._name, self._convertor_factory(value))
+                setattr(obj, "_updated_dt", vxtime.now())
 
-    @property
-    def key(self) -> str:
-        return self._key
+        else:
 
-    @property
-    def value(self) -> Any:
-        return self._value
+            def fset(obj, value):
+                setattr(obj, self._name, value)
+                setattr(obj, "_updated_dt", vxtime.now())
 
-    @property
-    def expired_dt(self) -> float:
-        return self._expired_dt
+        self._fset = fset
 
-    @property
-    def size(self) -> float:
-        return 1
+    def __get__(self, obj, owner):
+        try:
+            return self._fget(obj, owner)
+        except Exception:
+            return self.default
 
-    @property
-    def is_expired(self) -> float:
-        return self._expired_dt < vxtime.now()
+    def __set__(self, obj, value):
+        if self._fset is None:
+            return
+
+        try:
+            self._fset(obj, value)
+        except Exception:
+            setattr(obj, self._name, self.default)
 
     def __str__(self) -> str:
-        return (
-            f"< {self.__class__.__name__} key: {self._key} _value:"
-            f" {self._value} has expired >"
-            if self.is_expired
-            else (
-                f"< {self.__class__.__name__} key: {self._key} _value:"
-                f" {self._value} will expired at: {to_timestring(self.expired_dt)} > "
-            )
-        )
+        return f"{self.__class__.__name__} default: {self.default}"
 
     __repr__ = __str__
 
-    def __getstate__(self) -> Dict:
-        return {"key": self.key, "value": self.value, "expired_dt": self.expired_dt}
+    @property
+    def default(self):
+        """缺省值"""
 
-    def __setstate(self, state: Dict) -> None:
-        self.__init__(**state)
+        return self._default_factory()
 
-    @classmethod
-    def set_cache_params(cls, *args, **kwargs) -> None:
-        pass
-
-    @classmethod
-    def init_cache(cls) -> OrderedDict:
-        return OrderedDict()
 
-    def clear(self) -> None:
-        del self._value
+class vxUUIDField(vxField):
+    """uuid类型
 
-    def __lt__(self, other: "CacheUnit") -> bool:
-        return (self.expired_dt, self._value) > (other.expired_dt, other._value)
+    auto : auto 为True,则系统初始化自动创建一个uuid，为false则默认值为: ''
+    """
 
-    def __gt__(self, other: "CacheUnit") -> bool:
-        return (self.expired_dt, self._value) < (other.expired_dt, other._value)
+    def __init__(self, auto=True) -> None:
+        super().__init__(
+            default_factory=lambda: str(uuid.uuid4()) if auto else "",
+            convertor_factory=lambda value: value or "",
+        )
 
-    def __eq__(self, other: "CacheUnit") -> bool:
-        return (self.expired_dt, self._value) == (other.expired_dt, other._value)
 
-    def __hash__(self) -> int:
-        return hash((self._value, self._expired_dt))
+class vxEnumField(vxField):
+    """Enum类型字段"""
 
+    def __init__(self, default: Enum) -> None:
+        super().__init__(
+            default_factory=lambda: default,
+            convertor_factory=lambda x: to_enum(x, default.__class__, default),
+            format_factory=lambda value: value.name,
+        )
 
-class DiskCacheUnit(CacheUnit):
-    _path = Path.home().joinpath(".vxcache").absolute()
 
-    def __init__(self, key: str, value: Any, expired_dt: float = 0) -> None:
-        value_file = Path(self._path, f"{key}.dat")
-        super().__init__(key, value_file.absolute(), expired_dt)
-        self.value = value
+class vxIntField(vxField):
+    """整数类型字段"""
 
-    @property
-    def value(self) -> Any:
-        with open(self._value, "rb") as f:
-            cache_obj = pickle.load(f)
-            return cache_obj["value"]
-
-    @value.setter
-    def value(self, value: Any) -> None:
-        with open(self._value, "wb") as fp:
-            pickle.dump(
-                {"key": self.key, "value": value, "expired_dt": self._expired_dt}, fp
-            )
+    def __init__(
+        self, default: int, _min: Optional[float] = None, _max: Optional[float] = None
+    ):
+        if _min is None:
+            _min = -math.inf
 
-    @property
-    def size(self) -> float:
-        return self._value.stat().st_size
+        if _max is None:
+            _max = math.inf
 
-    @classmethod
-    def set_cache_params(cls, cache_dir: Union[str, Path]) -> None:
-        cls._path = Path(cache_dir)
-        cls._path.mkdir(parents=True, exist_ok=True)
-        logger.info(f"设置换成目录为: {cls._path}")
-
-    @classmethod
-    def init_cache(cls) -> OrderedDict:
-        if not Path(cls._path).exists():
-            Path(cls._path).mkdir(parents=True, exist_ok=True)
-            return OrderedDict()
-
-        cache_objs = []
-        for value_file in cls._path.glob("*.dat"):
-            with open(value_file, "rb") as fp:
-                cache_params = pickle.load(fp)
-
-            if (
-                isinstance(cache_params, dict)
-                and cache_params["expired_dt"] > vxtime.now()
-            ):
-                cache_objs.append(cls(**cache_params))
-            else:
-                logger.warning(f"cache_params error: {value_file} 删除")
-                Path(value_file).unlink()
+        def check_int(v: Any):
+            # 四舍五入
+            v = round(v)
+            if _min <= v <= _max:
+                return v
+            raise ValueError(f"赋值 {v} 超出取值范围: [{_min},{_max}]")
 
-        return OrderedDict(
-            {cache_obj.key: cache_obj for cache_obj in sorted(cache_objs)}
-        )
+        super().__init__(default_factory=default, convertor_factory=check_int)
 
-    def clear(self) -> None:
-        self._value.unlink(missing_ok=True)
 
-
-class vxLRUCache:
-    """Cache"""
+class vxFloatField(vxField):
+    """浮点类型字段"""
 
     def __init__(
         self,
-        size_limit: float = 0,
-        unit_factory: Type[CacheUnit] = None,
+        default: float,
+        ndigits: Optional[int] = None,
+        _min: Optional[float] = None,
+        _max: Optional[float] = None,
     ):
-        # self._lock = Lock()
-        self.size_limit = size_limit * 1000  # M
-        self._size = 0
-        self._unit_factory = unit_factory or CacheUnit
-        self._storage = OrderedDict()
+        if _min is None:
+            _min = -math.inf
 
-        for key, cache_obj in self._unit_factory.init_cache().items():
-            self.__setitem__(key, cache_obj)
+        if _max is None:
+            _max = math.inf
 
-    @property
-    def storage(self) -> Dict:
-        return {
-            key: cache_obj
-            for key, cache_obj in self._storage.items()
-            if not cache_obj.is_expired
-        }
+        def check_float(v: Any):
+            v = float(v)
+            if ndigits is not None:
+                v = round(v, ndigits)
+
+            if _min <= v <= _max:
+                return v
+            raise ValueError(f"赋值 {v} 超出取值范围: [{_min},{_max}]")
 
-    def keys(self) -> List[str]:
-        # with self._lock:
-        return [
-            key for key, cache_obj in self._storage.items() if not cache_obj.is_expired
-        ]
-
-    def set(self, key, value, ttl=0) -> None:
-        expired_dt = vxtime.now() + ttl if ttl > 0 else _ENDOFTIME
-        cache_obj = (
-            value
-            if isinstance(value, CacheUnit)
-            else self._unit_factory(key, value, expired_dt)
+        super().__init__(default_factory=default, convertor_factory=check_float)
+
+
+class vxPropertyField(vxField):
+    """函数属性类型字段"""
+
+    def __init__(
+        self, property_factory: Callable[[Any], Any], default_factory: Any = None
+    ):
+        super().__init__(
+            property_factory=property_factory, default_factory=default_factory
         )
 
-        # with self._lock:
-        self._adjust_size(key, cache_obj)
-        self._storage[key] = cache_obj
-        self._storage.move_to_end(key)
-
-        if self.limited:
-            # pop the oldest items beyond size limit
-            while self._size > self.size_limit:
-                self.popitem(last=False)
-
-    def get(self, key, default=None) -> Any:
-        cache_obj = self._storage.get(key, None)
-        if cache_obj is None or cache_obj.is_expired:
-            return default
-        self._storage.move_to_end(key)
-        return cache_obj.value
 
-    def __setitem__(self, key, value):
-        cache_obj = (
-            value
-            if isinstance(value, CacheUnit)
-            else self._unit_factory(key, value, _ENDOFTIME)
+class vxDatetimeField(vxField):
+    """时间类型字段"""
+
+    def __init__(
+        self,
+        default_factory=vxtime.now,
+        formatter_string="%F %H:%M:%S.%f",
+        convertor_factory=to_timestamp,
+    ):
+        super().__init__(
+            default_factory=default_factory,
+            convertor_factory=convertor_factory,
+            format_factory=lambda value: to_timestring(value, formatter_string),
         )
-        # precalculate the size after od.__setitem__
-        # with self._lock:
-        self._adjust_size(key, cache_obj)
-        self._storage[key] = cache_obj
-        self._storage.move_to_end(key)
-
-        if self.limited:
-            # pop the oldest items beyond size limit
-            while self._size > self.size_limit:
-                self.popitem(last=False)
 
-    def __getitem__(self, key):
-        # with self._lock:
-        cache_obj = self._storage.get(key, None)
-        if cache_obj is None or cache_obj.is_expired:
-            raise MissingCache(key)
-        self._storage.move_to_end(key)
-        return cache_obj.value
-
-    def __contains__(self, key):
-        # with self._lock:
-        return key in self._storage and self._storage[key].is_expired is False
+
+class vxBoolField(vxField):
+    """bool字段"""
+
+    def __init__(self, default):
+        super().__init__(default_factory=bool(default), convertor_factory=bool)
+
+
+class vxBytesField(vxField):
+    """bytes字段"""
+
+    def __init__(self, default: bytes = b""):
+        super().__init__(default_factory=lambda: default, convertor_factory=to_binary)
+
+
+class vxDataMeta(type):
+    """data 元类"""
+
+    def __new__(cls, name: str, bases: tuple, attrs: dict):
+        message_formater = {
+            name: var._format_factory
+            for name, var in attrs.items()
+            if isinstance(var, vxField)
+        }
+
+        for base_cls in bases:
+            message_formater.update(**base_cls.__vxfields__)
+
+        attrs["created_dt"]: float = vxDatetimeField()
+        attrs["updated_dt"]: float = vxDatetimeField()
+        message_formater["created_dt"] = attrs["created_dt"]._format_factory
+        message_formater["updated_dt"] = attrs["updated_dt"]._format_factory
+
+        if "__sortkeys__" in attrs:
+
+            def is_lower_than(self, other: "vxDataClass") -> bool:
+                """< 根据sortkeys的顺序一次对比"""
+                for k in self.__sortkeys__:
+                    if getattr(self, k) < getattr(other, k):
+                        return True
+                    elif getattr(self, k) > getattr(other, k):
+                        return False
+                return False
+
+            def is_greater_than(self, other: "vxDataClass") -> bool:
+                """> 根据sortkeys的顺序一次对比"""
+                for k in self.__sortkeys__:
+                    if getattr(self, k) < getattr(other, k):
+                        return False
+                    elif getattr(self, k) > getattr(other, k):
+                        return True
+                return False
+
+            attrs["__lt__"] = is_lower_than
+            attrs["__gt__"] = is_greater_than
+
+        attrs["__vxfields__"] = message_formater
+        attrs["__slots__"] = tuple(f"_{name}" for name in message_formater)
+
+        return type.__new__(cls, name, bases, attrs)
+
+    def __call__(cls, *args, **kwds) -> Any:
+        created_dt = kwds.pop("created_dt", None)
+        updated_dt = kwds.pop("updated_dt", None)
+        instance = super().__call__(*args, **kwds)
+        if created_dt:
+            instance.created_dt = created_dt
+            instance.updated_dt = updated_dt or created_dt
+
+        return instance
+
+
+class vxDataClass(metaclass=vxDataMeta):
+    """数据基类"""
+
+    __vxfields__: dict = {}
+    __sortkeys__: tuple = ()
+
+    def __init__(self, *args, **kwargs) -> None:
+        if args and isinstance(args[0], Mapping):
+            kwargs.update(args[0])
+        elif args:
+            kwargs.update(zip(self.__vxfields__, args))
+
+        for attr in self.keys():
+            value = kwargs.pop(attr, getattr(self, attr))
+            setattr(self, attr, value)
+
+    def __getitem__(self, key: str) -> Any:
+        return getattr(self, key)
+
+    def __setitem__(self, key: str, value: Any) -> None:
+        setattr(self, key, value)
 
     def __len__(self):
-        # with self._lock:
-        return len(self._storage)
+        return len(self.__vxfields__)
 
-    def __repr__(self):
-        storage_string = "".join(
-            f"\t== {cache_obj}\n" for cache_obj in list(self.storage.values())[-5:]
-        )
-        return (
-            f"{self.__class__.__name__}<size_limit:{self.size_limit if self.limited else 'no limit'} total_size:{self.total_size}>\n{storage_string}"
-        )
+    def __str__(self):
+        message = {}
+        try:
+            for attr, formatter in self.__vxfields__.items():
+                value = getattr(self, attr)
+                if isinstance(value, vxDataClass):
+                    value = value
+                elif formatter:
+                    value = formatter(value)
+
+                message[attr] = value
+            return f"< {self.__class__.__name__}(id-{id(self)}) : {to_json(message)} >"
+        except Exception:
+            message = {k: getattr(self, k) for k in self.keys()}
+            return f"< {self.__class__.__name__}(id-{id(self)}) : {message} >"
+
+    __repr__ = __str__
 
-    def set_limit_size(self, limit):
-        self.size_limit = limit
+    def __hash__(self):
+        return hash(self.__str__())
 
-    @property
-    def limited(self):
-        """whether memory cache is limited"""
-        return self.size_limit > 0
+    def __eq__(self, __o: "vxDataClass") -> bool:
+        return all(v == __o[k] for k, v in self.items())
+
+    def __contains__(self, item: str) -> bool:
+        return item in self.keys() if item else False
+
+    def __setstate__(self, state: dict):
+        self.__init__(**state)
+
+    def __getstate__(self):
+        return self.message
+
+    def __iter__(self):
+        return next(self)
+
+    def __next__(self):
+        yield from self.keys()
 
     @property
-    def total_size(self):
-        return self._size
+    def message(self) -> dict:
+        """展示数据"""
+        message = {}
+        for k, v in self.items():
+            if isinstance(v, Enum):
+                message[k] = v.name
+            elif isinstance(v, vxDataClass):
+                message[k] = v.message
+            else:
+                message[k] = v
 
-    def clear(self):
-        # with self._lock:
-        self._size = 0
-        for cache_obj in self._storage.values():
-            cache_obj.clear()
-        self._storage.clear()
+        return message
 
-    def popitem(self, last=False):
-        if len(self._storage) == 0:
-            return None, None
+    @staticmethod
+    def pack(obj):
+        """打包消息"""
+        pickled = pickle.dumps(obj)
+        return zlib.compress(pickled)
 
-        # with self._lock:
-        k, cache_obj = self._storage.popitem(last=last)
-        self._size -= cache_obj.size
-        value = cache_obj.value
-        cache_obj.clear()
+    @staticmethod
+    def unpack(packed_obj):
+        """解包消息"""
+        pickled = zlib.decompress(packed_obj)
+        return pickle.loads(pickled)
 
-        return k, value
+    def keys(self) -> Sequence:
+        """相关keys"""
+        yield from self.__vxfields__
 
-    def pop(self, key, default=None):
-        # with self._lock:
-        cache_obj = self._storage.pop(key, None)
-        if cache_obj is None:
-            return default
+    def update(self, **kwargs):
+        """更新数据"""
+        for k, v in kwargs.items():
+            setattr(self, k, v)
 
-        self._size -= cache_obj.size
-        cache_obj.clear()
-        return default if cache_obj.is_expired else cache_obj.value
+    def values(self) -> Sequence:
+        """获取内部数据"""
+        yield from [getattr(self, key) for key in self.keys()]
 
-    def _adjust_size(self, key, cache_obj):
-        if key in self._storage:
-            self._size -= self._storage[key].size
+    def items(self) -> Sequence:
+        """获取相关(key,value)对"""
+        yield from [(key, getattr(self, key)) for key in self.keys()]
 
-        self._size += cache_obj.size
+    def get(self, key, _default=None) -> Any:
+        """获取相关"""
+        return getattr(self, key, _default)
 
-    def __call__(self, func: Callable) -> Any:
-        def wapper(*args, **kwargs):
-            try:
-                ba = inspect.signature(func).bind(*args, **kwargs)
-                ba.apply_defaults()
-                string = to_json(ba.arguments, sort_keys=True, default=str)
-                key = hashlib.md5(string.encode()).hexdigest()
-                retval = self.__getitem__(key)
-            except MissingCache:
-                retval = func(*args, **kwargs)
-                self.__setitem__(key, retval)
 
-            return retval
+@vxJSONEncoder.register(vxDataClass)
+def _(obj):
+    message = {}
 
-        return wapper
+    for attr, formatter in obj.__vxfields__.items():
+        value = getattr(obj, attr)
+        if isinstance(value, vxDataClass):
+            value = value
+        elif formatter:
+            value = formatter(value)
 
-    def update(self, ttl=0, **kwargs):
-        for key, value in kwargs.items():
-            self.set(key, value, ttl)
+        message[attr] = value
 
+    return message
 
-# diskcache = vxLRUCache(size_limit=1000, unit_factory=DiskCacheUnit)
 
+class vxDataConvertor:
+    """数据转换器基础类"""
 
-SHARED_MEMORY_CACHE = "file:shm_cachedb?mode=memory&cache=shared"
+    def __init__(
+        self,
+        target_cls,
+        convertors_mapping: MutableMapping = None,
+        defaults: MutableMapping = None,
+    ) -> None:
+        self._target_cls = target_cls
+        self._convertors = {}
+        self._defaults_data = defaults or {}
 
-import pickle
-from functools import wraps
-from vxutils.database.sqlite import vxSQLiteDB
-from vxutils.dataclass import (
-    vxDataClass,
-    vxUUIDField,
-    vxDatetimeField,
-    vxBytesField,
-)
+        if convertors_mapping is None:
+            return
+
+        for target_col, convertor in convertors_mapping.items():
+            if callable(convertor):
+                self.add_convertors(target_col, convertor)
+            else:
+                self.rename_columns(convertor, target_col)
+
+    def add_convertors(self, target_col, conveter_func):
+        """设置col的转换函数
 
+        target_col : 待转换的字段名
+        convertor_func(other_data) ：转换函数 或者是缺省值，其中other_data 为待转换对象内容
+        """
+        if not callable(conveter_func):
+            raise ValueError(f"func({conveter_func.__name__} is not callable")
+        self._convertors[target_col] = conveter_func
+
+    def rename_columns(self, source_col, target_col):
+        """重命名字段"""
+
+        def _rename_func(other_data):
+            """重命名转换器"""
+            if hasattr(other_data, source_col):
+                return getattr(other_data, source_col)
+            return other_data[source_col]
+
+        self._convertors[target_col] = _rename_func
+
+    def set_defaults(self, target_col, default_value):
+        """设置默认值"""
+        self._defaults_data[target_col] = default_value
 
-class _CacheUnit(vxDataClass):
-    key: str = vxUUIDField(False)
-    value: Any = vxBytesField()
-    expired_dt: float = vxDatetimeField()
-
-
-class vxSQLiteCache:
-    def __init__(self, db_uri: Union[str, Path] = None) -> None:
-        if db_uri is None:
-            db_uri = SHARED_MEMORY_CACHE
-
-        self._conn = vxSQLiteDB.connect(db_uri)
-        self._conn.create_table("__cache__", ["key"], _CacheUnit)
-        self._last_remove_expired_dt = 0
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-
-    def __contains__(self, key) -> bool:
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            cache_unit = session.findone(
-                "__cache__", f"expired_dt> {vxtime.now()}", key=key
+    def _convert_col(self, col, other_data):
+        try:
+            col_value = self._defaults_data.get(col, None)
+            if col in self._convertors:
+                col_value = self._convertors[col](other_data)
+            elif hasattr(other_data, col):
+                col_value = getattr(other_data, col)
+            else:
+                col_value = getitem(other_data, col)
+        except Exception as err:
+            from vxutils import logger
+
+            logger.debug(
+                f"target class: {self._target_cls.__name__} Other_data load"
+                f" col:{col} err. {err}",
+                exc_info=True,
             )
-            return bool(cache_unit)
+            logger.debug(f"other_data={other_data}")
+
+        return col, col_value
+
+    def __call__(self, other_data, key="", **kwargs):
+        data = dict(
+            self._convert_col(col, other_data) for col in self._target_cls.__vxfields__
+        )
+        data.update(**kwargs)
+        instance = self._target_cls(data)
+        return (
+            (str(instance[key]), instance)
+            if len(key) > 0 and key in instance.keys()
+            else instance
+        )
+
+
+class vxDict(UserDict):
+    """引擎上下文context类"""
+
+    _default_config: Dict[str, Any] = {}
+
+    def __init__(self, *args, **kwargs):
+        default_config = dict(*args, **kwargs)
+        for k, v in default_config.items():
+            self.__dict__[k] = _to_vxdict(v)
+
+    def __getitem__(self, key):
+        return self.__dict__[key]
+
+    def __setitem__(self, key, value):
+        self.__dict__[key] = value
+
+    def __delitem__(self, key):
+        self.__dict__.__delitem__(key)
+
+    def __setattr__(self, attr: str, value: Any) -> Any:
+        self.__dict__[attr] = _to_vxdict(value)
 
     def __len__(self) -> int:
-        with self._conn.start_session() as session:
-            return len(session.distinct("__cache__", "key"))
+        return len(self.__dict__)
 
-    def __getitem__(self, key) -> Any:
-        if not key:
-            raise ValueError("key can't be empty")
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            cache_unit = session.findone(
-                "__cache__", f"""expired_dt > {vxtime.now()}""", key=key
-            )
-            if cache_unit is None:
-                raise MissingCache(key)
-            return pickle.loads(cache_unit.value)
+    def __eq__(self, __o: MutableMapping) -> bool:
+        if len(self) != len(__o):
+            return False
 
-    def get(self, key: str, default: Any = None) -> Any:
-        """获取缓存内容
+        try:
+            return all(v == __o[k] for k, v in self.items())
+        except Exception:
+            return False
 
-        Arguments:
-            key {str} -- 缓存key
-            default {Any} -- 默认值 {default=None}, 如果缓存不存在，返回默认值
+    def __hash__(self):
+        return hash(self.__str__())
 
-        Returns:
-            Any -- 缓存内容
-        """
-        if not key:
-            raise ValueError("key can't be empty")
+    def __setstate__(self, state) -> None:
+        self.__init__(**state)
 
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            cache_unit = session.findone(
-                "__cache__", f"""expired_dt > {vxtime.now()}""", key=key
-            )
-            return pickle.loads(cache_unit.value) if cache_unit else default
+    def __getstate__(self) -> dict:
+        return self.__dict__
 
-    def get_many(self, *keys: List[str]) -> Dict:
-        """获取缓存内容
+    def __str__(self):
+        try:
+            return f"< {self.__class__.__name__}(id-{id(self)}) : {to_json(self)} >"
+        except (TypeError, KeyError):
+            return f"< {self.__class__.__name__}(id-{id(self)}) : {self.__dict__} >"
 
-        Returns:
-            Dict -- 缓存内容
-        """
-        if not keys:
-            raise ValueError("keys can't be empty")
+    __repr__ = __str__
 
-        if len(keys) == 1 and isinstance(keys[0], (tuple, list)):
-            keys = keys[0]
+    def __iter__(self):
+        yield from self.__dict__
 
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            conditions = [
-                f"""key in ('{"', '".join(keys)}')""",
-                f"""expired_dt > {vxtime.now()}""",
-            ]
-            cur = session.find("__cache__", *conditions)
-            return {
-                cache_unit.key: pickle.loads(cache_unit.value) for cache_unit in cur
-            }
+    def keys(self):
+        yield from self.__dict__
 
-    def set(
-        self, key: str, value: Any, expired_dt: float = None, ttl: float = None
-    ) -> None:
-        """设置缓存内容
+    def values(self):
+        yield from self.__dict__.values()
+
+    def update(self, config: MutableMapping = None, **kwargs):
+        """批量更新字典"""
+        config = config or kwargs
+        for k, v in config.items():
+            self.__dict__[k] = _to_vxdict(v)
+
+    def items(self):
+        """(key,value) pairs"""
+        yield from self.__dict__.items()
+
+    def pop(self, key: str, default_: Any = None) -> Any:
+        """弹出key对应的value，若无此数据，则返回default_"""
+        return self.__dict__.pop(key, default_)
+
+    def clear(self) -> None:
+        """清空context"""
+        self.__dict__ = {}
+
+    @staticmethod
+    def load_json(json_file, default_config=None) -> None:
+        """加载json file
 
         Arguments:
-            key {str} -- 缓存key
-            value {Any} -- 缓存内容
-            expired_dt {float} -- 超时时间 (default: {None})
-            ttl {float} -- 生命周期，单位：s (default: {None})
+            json_file {_type_} -- 加载的json file
+
+        Raises:
+            OSError: 文件不存在
         """
-        if ttl:
-            expired_dt = vxtime.now() + ttl
 
-        if expired_dt is None:
-            expired_dt = _ENDOFTIME
+        json_file = Path(json_file)
+        if not json_file.exists():
+            raise OSError(f"json_file({json_file.as_posix()}) is not exists.")
+
+        with open(json_file.as_posix(), "r", encoding="utf-8") as fp:
+            config = json.load(fp)
 
-        _value = pickle.dumps(value)
-        cache_unit = _CacheUnit(key=key, value=_value, expired_dt=expired_dt)
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            session.save("__cache__", cache_unit)
+        return vxDict(default_config, **config)
 
-    def pop(self, key: str, default: Any = None) -> Any:
-        """弹出缓存内容
+    def save_json(self, json_file: str) -> None:
+        """保存json file
 
         Arguments:
-            key {str} -- 缓存key
-            default {Any} -- 缺省值 (default: {None})
+            json_file {str} -- 待保存的json file
 
-        Returns:
-            Any -- 缓存内容
         """
-        if not key:
-            raise ValueError("key can't be empty")
+        with open(json_file, "w", encoding="utf-8") as fp:
+            json.dump(self, fp, indent=4, cls=vxJSONEncoder)
 
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            cache_unit = session.findone(
-                "__cache__", f"""expired_dt > {vxtime.now()}""", key=key
-            )
-            if cache_unit:
-                session.delete("__cache__", key=key)
-                return pickle.loads(cache_unit.value)
-            return default
-
-    def _remove_expired(self, session: vxSQLiteDB) -> Any:
-        """删除超时内容"""
-        now = vxtime.now()
-        if self._last_remove_expired_dt + 60 > now:
-            return
-        self._last_remove_expired_dt = now
-        session.delete("__cache__", f"expired_dt < {self._last_remove_expired_dt}")
 
-    def update(
-        self, cacheobjs: Dict, expired_dt: float = None, ttl: float = None
-    ) -> None:
-        """批量更新
+@singledispatch
+def _to_vxdict(self: Any):
+    """转换为vxdict obj"""
+    return self
 
-        Keyword Arguments:
-            expired_dt {float} -- 超时时间 (default: {None})
-            cacheobjs {dict} -- 缓存内容
-        """
-        if ttl:
-            expired_dt = vxtime.now() + ttl
 
-        if expired_dt is None or expired_dt > _ENDOFTIME:
-            expired_dt = _ENDOFTIME
-        cache_units = [
-            _CacheUnit(key=key, value=pickle.dumps(value), expired_dt=expired_dt)
-            for key, value in cacheobjs.items()
-        ]
-        with self._conn.start_session() as session:
-            self._remove_expired(session)
-            session.save("__cache__", cache_units)
+@_to_vxdict.register(MutableMapping)
+def _(obj: MutableMapping) -> vxDict:
+    return vxDict(**obj)
 
-    def clear(self) -> None:
-        """清空所有缓存内容"""
-        with self._conn.start_session() as session:
-            session.truncate("__cache__")
-
-    def keys(self) -> List[str]:
-        """获取所有key"""
-        with self._conn.start_session() as session:
-            return session.distinct("__cache__", "key", f"expired_dt > {vxtime.now()}")
 
-    def hash_keys(self, obj: Any) -> str:
-        """将keys进行hash
+@_to_vxdict.register(Sequence)
+def _(obj: Sequence) -> List:
+    return obj if isinstance(obj, str) else [_to_vxdict(o_) for o_ in obj]
 
-        Arguments:
-            obj {Any} -- 需要hash的对象
 
-        Returns:
-            str -- hash后的keys
-        """
-        try:
-            return hash(obj)
-        except TypeError:
-            return hash(to_json(obj.__dict__, sort_keys=True, default=str))
-
-    def __call__(self, ttl: float = None) -> Any:
-        def deco(func: Callable) -> Callable:
-            @wraps(func)
-            def wapper(*args, **kwargs):
-                try:
-                    ba = inspect.signature(func).bind(*args, **kwargs)
-                    ba.apply_defaults()
-                    string = to_json(ba.arguments, sort_keys=True, default=str)
-                    key = hashlib.md5(string.encode()).hexdigest()
-                    retval = self[key]
-                except MissingCache:
-                    retval = func(*args, **kwargs)
-                    self.set(key, retval, ttl=ttl)
-
-                return retval
-
-            return wapper
-
-        return deco
-
-
-_cache_path = Path.home().joinpath(".cache")
-_cache_path.mkdir(parents=True, exist_ok=True)
-diskcache = vxSQLiteCache(str(_cache_path.joinpath("vxcache.dat").absolute()))
-
-if __name__ == "__main__":
-    # @c(ttl=10)
-    @diskcache(ttl=10)
-    def test(n):
-        if n < 2:
-            return n
-        return test(n - 1) + test(n - 2)
+@vxJSONEncoder.register(vxDict)
+def _(obj):
+    return dict(obj.items())
+
 
-    with vxtime.timeit():
-        print(test(20))
+MutableMapping.register(vxDict)
+Mapping.register(vxDataClass)
```

### Comparing `vxquant-2023.4.1/src/vxutils/convertors.py` & `vxquant-2023.5.13/src/vxutils/convertors.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/database/__init__.py` & `vxquant-2023.5.13/src/vxutils/database/__init__.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/database/mongodb.py` & `vxquant-2023.5.13/src/vxutils/database/mongodb.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/database/sqlite.py` & `vxquant-2023.5.13/src/vxutils/database/sqlite.py`

 * *Files 0% similar despite different names*

```diff
@@ -435,15 +435,15 @@
             vxTest(
                 id=i,
                 name=f"clear{i}",
                 is_check=False,
                 due_dt="2023-03-01",
                 created_dt="2023-03-01",
             )
-            for i in range(100)
+            for i in range(10000)
         ]
         # testdb.executemany(
         #    """UPDATE test
         #    SET
         #        name=:name
         #    WHERE id=:cnt
         #    """,
```

### Comparing `vxquant-2023.4.1/src/vxutils/dbproxy.py` & `vxquant-2023.5.13/src/vxutils/database/dbproxy.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/debug.py` & `vxquant-2023.5.13/src/vxutils/debug.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/decorators.py` & `vxquant-2023.5.13/src/vxutils/decorators.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/exceptions.py` & `vxquant-2023.5.13/src/vxutils/exceptions.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/log.py` & `vxquant-2023.5.13/src/vxutils/log.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/net.py` & `vxquant-2023.5.13/src/vxutils/net.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/src/vxutils/wrappers.py` & `vxquant-2023.5.13/src/vxutils/wrappers.py`

 * *Files 1% similar despite different names*

```diff
@@ -185,30 +185,31 @@
         params = provider.get("params", {})
         kwargs = {k: self._load_privoder(v, providers) for k, v in params.items()}
         return import_tools(provider["class"], kwargs)
 
     def register_providers(self, **providers):
         from vxutils import logger
 
-        for name, provider in providers.items():
-            if not provider:
+        for name, provider_config in providers.items():
+            if not provider_config:
                 continue
 
             if name in self.__dict__:
                 logger.warning(
                     "providers({name}) 已注册为: {self.__dict__[name]},忽略更新"
                 )
                 continue
 
             try:
-                self.__dict__[name] = self._load_privoder(provider, providers)
+                provider = self._load_privoder(provider_config, providers)
+                self.__dict__[name] = provider
                 logger.info(f"注册{name}接口成功 ")
             except Exception as err:
                 logger.error(
-                    f"加载provider: {name}({provider})出错: {err}", exc_info=True
+                    f"加载provider: {name}({provider_config})出错: {err}", exc_info=True
                 )
 
 
 if __name__ == "__main__":
     from vxutils import vxtime
 
     providers = {
```

### Comparing `vxquant-2023.4.1/src/vxutils/zmqsocket.py` & `vxquant-2023.5.13/src/vxutils/zmqsocket.py`

 * *Files identical despite different names*

### Comparing `vxquant-2023.4.1/PKG-INFO` & `vxquant-2023.5.13/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,24 +1,23 @@
 Metadata-Version: 2.1
 Name: vxquant
-Version: 2023.4.1
+Version: 2023.5.13
 Summary: 一个简单、易用、面向中国股市实盘的python量化交易框架
 Home-page: https://gitee.com/vxquant/vxquant
 License: MIT
 Keywords: quant,tools
 Author: vex1023
 Author-email: vex1023@qq.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: Implementation :: CPython
@@ -28,14 +27,15 @@
 Requires-Dist: polars[pyarrow]
 Requires-Dist: pymongo
 Requires-Dist: python-dateutil
 Requires-Dist: pyzmq
 Requires-Dist: requests
 Requires-Dist: scipy
 Requires-Dist: six
+Requires-Dist: sqlalchemy (>=2.0,<3.0)
 Requires-Dist: tqdm
 Description-Content-Type: text/markdown
 
 # vxquant
 
 #### 介绍
 一个简单、易用、面向中国股市实盘的python量化交易框架
```

