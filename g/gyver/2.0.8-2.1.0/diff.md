# Comparing `tmp/gyver-2.0.8.tar.gz` & `tmp/gyver-2.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gyver-2.0.8.tar", max compression
+gzip compressed data, was "gyver-2.1.0.tar", max compression
```

## Comparing `gyver-2.0.8.tar` & `gyver-2.1.0.tar`

### file list

```diff
@@ -1,85 +1,89 @@
--rw-r--r--   0        0        0     1079 2023-03-04 12:43:39.248229 gyver-2.0.8/LICENSE
--rw-r--r--   0        0        0      993 2023-03-04 12:43:39.248229 gyver-2.0.8/README.md
--rw-r--r--   0        0        0      158 2023-03-15 09:32:43.026509 gyver-2.0.8/gyver/__init__.py
--rw-r--r--   0        0        0      359 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/cache/__init__.py
--rw-r--r--   0        0        0     1224 2023-03-10 16:11:03.464198 gyver-2.0.8/gyver/cache/asyncio.py
--rw-r--r--   0        0        0      237 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/cache/config.py
--rw-r--r--   0        0        0     1776 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/cache/interface.py
--rw-r--r--   0        0        0     1395 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/cache/mapper.py
--rw-r--r--   0        0        0     6012 2023-03-10 16:27:14.550932 gyver-2.0.8/gyver/cache/mock.py
--rw-r--r--   0        0        0     4283 2023-03-07 05:23:55.941027 gyver-2.0.8/gyver/cache/redis.py
--rw-r--r--   0        0        0     1118 2023-03-10 16:15:35.399291 gyver-2.0.8/gyver/cache/sync.py
--rw-r--r--   0        0        0      559 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/cache/utils.py
--rw-r--r--   0        0        0      498 2023-03-04 12:43:39.249229 gyver-2.0.8/gyver/config/__init__.py
--rw-r--r--   0        0        0       78 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/config/adapter/__init__.py
--rw-r--r--   0        0        0     1327 2023-03-09 20:50:41.914917 gyver-2.0.8/gyver/config/adapter/attrs.py
--rw-r--r--   0        0        0     1054 2023-03-09 20:50:06.492341 gyver-2.0.8/gyver/config/adapter/dataclass.py
--rw-r--r--   0        0        0     5991 2023-03-10 16:32:43.024313 gyver-2.0.8/gyver/config/adapter/factory.py
--rw-r--r--   0        0        0     1032 2023-03-09 21:13:57.979600 gyver-2.0.8/gyver/config/adapter/gattrs.py
--rw-r--r--   0        0        0     2108 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/config/adapter/interface.py
--rw-r--r--   0        0        0     1702 2023-03-10 16:08:32.119795 gyver-2.0.8/gyver/config/adapter/mark.py
--rw-r--r--   0        0        0     1091 2023-03-10 16:09:18.518531 gyver-2.0.8/gyver/config/adapter/pydantic.py
--rw-r--r--   0        0        0     3502 2023-03-10 16:31:14.706865 gyver-2.0.8/gyver/config/config.py
--rw-r--r--   0        0        0     2061 2023-03-10 16:30:10.030804 gyver-2.0.8/gyver/config/envconfig.py
--rw-r--r--   0        0        0      587 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/config/typedef.py
--rw-r--r--   0        0        0      473 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/config/utils.py
--rw-r--r--   0        0        0      419 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/__init__.py
--rw-r--r--   0        0        0      288 2023-03-07 05:23:55.974028 gyver-2.0.8/gyver/context/atomic_/__init__.py
--rw-r--r--   0        0        0     2317 2023-03-10 16:36:51.294229 gyver-2.0.8/gyver/context/atomic_/bound.py
--rw-r--r--   0        0        0     2493 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/atomic_/core.py
--rw-r--r--   0        0        0     1332 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/atomic_/resolver.py
--rw-r--r--   0        0        0     5659 2023-03-10 16:36:46.100148 gyver-2.0.8/gyver/context/context.py
--rw-r--r--   0        0        0      102 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/interfaces/__init__.py
--rw-r--r--   0        0        0     1525 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/interfaces/adapter.py
--rw-r--r--   0        0        0       39 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/context/typedef.py
--rw-r--r--   0        0        0      253 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/crypto/__init__.py
--rw-r--r--   0        0        0      133 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/crypto/config.py
--rw-r--r--   0        0        0      909 2023-03-04 12:43:39.250229 gyver-2.0.8/gyver/crypto/fernet.py
--rw-r--r--   0        0        0     1833 2023-03-10 16:38:27.803733 gyver-2.0.8/gyver/crypto/rsa.py
--rw-r--r--   0        0        0      749 2023-03-07 05:23:55.993028 gyver-2.0.8/gyver/database/__init__.py
--rw-r--r--   0        0        0     2158 2023-03-10 16:38:46.159019 gyver-2.0.8/gyver/database/adapter.py
--rw-r--r--   0        0        0     1233 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/config.py
--rw-r--r--   0        0        0      360 2023-03-07 05:23:15.357387 gyver-2.0.8/gyver/database/context/__init__.py
--rw-r--r--   0        0        0     3592 2023-03-10 16:42:38.608634 gyver-2.0.8/gyver/database/context/asyncio.py
--rw-r--r--   0        0        0     3349 2023-03-09 20:52:47.347955 gyver-2.0.8/gyver/database/context/sync.py
--rw-r--r--   0        0        0      170 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/drivers/__init__.py
--rw-r--r--   0        0        0      229 2023-03-10 16:40:51.098960 gyver-2.0.8/gyver/database/drivers/dialect.py
--rw-r--r--   0        0        0      224 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/drivers/interface.py
--rw-r--r--   0        0        0     1493 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/drivers/utils.py
--rw-r--r--   0        0        0     1076 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/entity.py
--rw-r--r--   0        0        0      498 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/entity.pyi
--rw-r--r--   0        0        0       50 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/metadata.py
--rw-r--r--   0        0        0     1012 2023-03-07 05:24:54.748959 gyver-2.0.8/gyver/database/query/__init__.py
--rw-r--r--   0        0        0     1692 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/query/_helpers.py
--rw-r--r--   0        0        0     2936 2023-03-07 05:23:56.788040 gyver-2.0.8/gyver/database/query/comp.py
--rw-r--r--   0        0        0      294 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/query/exc.py
--rw-r--r--   0        0        0     1359 2023-03-10 16:41:06.755203 gyver-2.0.8/gyver/database/query/interface.py
--rw-r--r--   0        0        0      279 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/query/null.py
--rw-r--r--   0        0        0     1354 2023-03-10 16:41:36.292662 gyver-2.0.8/gyver/database/query/order_by.py
--rw-r--r--   0        0        0     1239 2023-03-10 16:42:11.055203 gyver-2.0.8/gyver/database/query/paginate.py
--rw-r--r--   0        0        0      697 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/query/utils.py
--rw-r--r--   0        0        0     4640 2023-03-10 16:43:18.701263 gyver-2.0.8/gyver/database/query/where.py
--rw-r--r--   0        0        0      327 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/database/typedef.py
--rw-r--r--   0        0        0     4289 2023-03-09 21:15:00.423614 gyver-2.0.8/gyver/database/utils.py
--rw-r--r--   0        0        0      927 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/exc.py
--rw-r--r--   0        0        0      857 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/model.py
--rw-r--r--   0        0        0        0 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/py.typed
--rw-r--r--   0        0        0      186 2023-03-04 12:43:39.251229 gyver-2.0.8/gyver/url/__init__.py
--rw-r--r--   0        0        0     3155 2023-03-09 20:56:43.056785 gyver-2.0.8/gyver/url/core.py
--rw-r--r--   0        0        0      423 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/encode.py
--rw-r--r--   0        0        0      589 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/fragment.py
--rw-r--r--   0        0        0     2687 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/netloc.py
--rw-r--r--   0        0        0     2729 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/path.py
--rw-r--r--   0        0        0     1652 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/query.py
--rw-r--r--   0        0        0      662 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/url/utils.py
--rw-r--r--   0        0        0      674 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/__init__.py
--rw-r--r--   0        0        0      156 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/exc.py
--rw-r--r--   0        0        0     7918 2023-03-10 16:44:11.897097 gyver-2.0.8/gyver/utils/finder.py
--rw-r--r--   0        0        0     1392 2023-03-09 20:53:46.480916 gyver-2.0.8/gyver/utils/helpers.py
--rw-r--r--   0        0        0      174 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/json.py
--rw-r--r--   0        0        0     2610 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/lazy.py
--rw-r--r--   0        0        0     1318 2023-03-09 20:53:36.426752 gyver-2.0.8/gyver/utils/singleton.py
--rw-r--r--   0        0        0     1718 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/strings.py
--rw-r--r--   0        0        0      134 2023-03-04 12:43:39.252229 gyver-2.0.8/gyver/utils/timezone.py
--rw-r--r--   0        0        0     2035 2023-03-15 09:32:43.023509 gyver-2.0.8/pyproject.toml
--rw-r--r--   0        0        0     2493 1970-01-01 00:00:00.000000 gyver-2.0.8/PKG-INFO
+-rw-r--r--   0        0        0     1079 2023-03-29 07:24:24.843143 gyver-2.1.0/LICENSE
+-rw-r--r--   0        0        0      993 2023-03-29 07:24:24.843143 gyver-2.1.0/README.md
+-rw-r--r--   0        0        0      158 2023-05-13 04:06:12.532636 gyver-2.1.0/gyver/__init__.py
+-rw-r--r--   0        0        0      359 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/__init__.py
+-rw-r--r--   0        0        0     1201 2023-04-14 08:44:43.823769 gyver-2.1.0/gyver/cache/asyncio.py
+-rw-r--r--   0        0        0      237 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/config.py
+-rw-r--r--   0        0        0     1776 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/interface.py
+-rw-r--r--   0        0        0     1395 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/mapper.py
+-rw-r--r--   0        0        0     5993 2023-04-14 08:44:43.832774 gyver-2.1.0/gyver/cache/mock.py
+-rw-r--r--   0        0        0     4283 2023-04-14 08:44:43.835775 gyver-2.1.0/gyver/cache/redis.py
+-rw-r--r--   0        0        0     1128 2023-04-14 08:44:43.837776 gyver-2.1.0/gyver/cache/sync.py
+-rw-r--r--   0        0        0      558 2023-03-29 07:33:58.431990 gyver-2.1.0/gyver/cache/utils.py
+-rw-r--r--   0        0        0      498 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/config/__init__.py
+-rw-r--r--   0        0        0       78 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/adapter/__init__.py
+-rw-r--r--   0        0        0     1320 2023-04-14 08:44:43.858786 gyver-2.1.0/gyver/config/adapter/attrs.py
+-rw-r--r--   0        0        0     1078 2023-04-14 08:44:43.860787 gyver-2.1.0/gyver/config/adapter/dataclass.py
+-rw-r--r--   0        0        0     5886 2023-04-14 08:44:43.866790 gyver-2.1.0/gyver/config/adapter/factory.py
+-rw-r--r--   0        0        0     1056 2023-04-14 08:44:43.871793 gyver-2.1.0/gyver/config/adapter/gattrs.py
+-rw-r--r--   0        0        0     2107 2023-04-14 08:44:43.875795 gyver-2.1.0/gyver/config/adapter/interface.py
+-rw-r--r--   0        0        0     1701 2023-04-14 08:44:43.878796 gyver-2.1.0/gyver/config/adapter/mark.py
+-rw-r--r--   0        0        0     1091 2023-04-14 08:44:43.881798 gyver-2.1.0/gyver/config/adapter/pydantic.py
+-rw-r--r--   0        0        0     3435 2023-04-14 08:44:43.847781 gyver-2.1.0/gyver/config/config.py
+-rw-r--r--   0        0        0     2126 2023-04-14 08:44:43.849782 gyver-2.1.0/gyver/config/envconfig.py
+-rw-r--r--   0        0        0      587 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/typedef.py
+-rw-r--r--   0        0        0      473 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/utils.py
+-rw-r--r--   0        0        0      419 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/__init__.py
+-rw-r--r--   0        0        0      288 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/__init__.py
+-rw-r--r--   0        0        0     2317 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/bound.py
+-rw-r--r--   0        0        0     2493 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/core.py
+-rw-r--r--   0        0        0     1332 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/resolver.py
+-rw-r--r--   0        0        0     5659 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/context.py
+-rw-r--r--   0        0        0      102 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/interfaces/__init__.py
+-rw-r--r--   0        0        0     1525 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/interfaces/adapter.py
+-rw-r--r--   0        0        0       39 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/typedef.py
+-rw-r--r--   0        0        0      253 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/__init__.py
+-rw-r--r--   0        0        0      133 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/config.py
+-rw-r--r--   0        0        0      909 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/fernet.py
+-rw-r--r--   0        0        0     1856 2023-04-14 08:44:43.914814 gyver-2.1.0/gyver/crypto/rsa.py
+-rw-r--r--   0        0        0      749 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/__init__.py
+-rw-r--r--   0        0        0     2136 2023-04-14 08:44:43.927820 gyver-2.1.0/gyver/database/adapter.py
+-rw-r--r--   0        0        0     1233 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/config.py
+-rw-r--r--   0        0        0      360 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/context/__init__.py
+-rw-r--r--   0        0        0     3542 2023-04-14 08:44:42.980359 gyver-2.1.0/gyver/database/context/asyncio.py
+-rw-r--r--   0        0        0     3349 2023-03-29 07:29:51.153084 gyver-2.1.0/gyver/database/context/sync.py
+-rw-r--r--   0        0        0      170 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/__init__.py
+-rw-r--r--   0        0        0      229 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/dialect.py
+-rw-r--r--   0        0        0      224 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/interface.py
+-rw-r--r--   0        0        0     1493 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/utils.py
+-rw-r--r--   0        0        0     1076 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/entity.py
+-rw-r--r--   0        0        0      498 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/entity.pyi
+-rw-r--r--   0        0        0       50 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/metadata.py
+-rw-r--r--   0        0        0     1012 2023-04-14 08:44:43.954833 gyver-2.1.0/gyver/database/query/__init__.py
+-rw-r--r--   0        0        0     1692 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/_helpers.py
+-rw-r--r--   0        0        0     2935 2023-04-14 08:44:43.960836 gyver-2.1.0/gyver/database/query/comp.py
+-rw-r--r--   0        0        0      294 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/exc.py
+-rw-r--r--   0        0        0     1353 2023-04-14 08:44:43.004370 gyver-2.1.0/gyver/database/query/interface.py
+-rw-r--r--   0        0        0      279 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/null.py
+-rw-r--r--   0        0        0     1270 2023-04-14 08:44:43.969841 gyver-2.1.0/gyver/database/query/order_by.py
+-rw-r--r--   0        0        0     1239 2023-04-14 08:44:43.971842 gyver-2.1.0/gyver/database/query/paginate.py
+-rw-r--r--   0        0        0      697 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/utils.py
+-rw-r--r--   0        0        0     4613 2023-04-14 08:44:43.975844 gyver-2.1.0/gyver/database/query/where.py
+-rw-r--r--   0        0        0      327 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/typedef.py
+-rw-r--r--   0        0        0     4243 2023-04-14 08:44:43.080407 gyver-2.1.0/gyver/database/utils.py
+-rw-r--r--   0        0        0     2030 2023-05-11 07:34:48.903992 gyver-2.1.0/gyver/exc.py
+-rw-r--r--   0        0        0      857 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/model.py
+-rw-r--r--   0        0        0      101 2023-05-08 11:52:12.095726 gyver-2.1.0/gyver/pools/__init__.py
+-rw-r--r--   0        0        0     5804 2023-05-11 07:47:54.886111 gyver-2.1.0/gyver/pools/asyncio.py
+-rw-r--r--   0        0        0     2200 2023-05-11 07:54:54.698462 gyver-2.1.0/gyver/pools/resource.py
+-rw-r--r--   0        0        0     3871 2023-05-11 07:48:16.387841 gyver-2.1.0/gyver/pools/thread.py
+-rw-r--r--   0        0        0        0 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/py.typed
+-rw-r--r--   0        0        0      186 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/url/__init__.py
+-rw-r--r--   0        0        0     3212 2023-05-13 03:47:35.995069 gyver-2.1.0/gyver/url/core.py
+-rw-r--r--   0        0        0      423 2023-05-13 03:47:04.475970 gyver-2.1.0/gyver/url/encode.py
+-rw-r--r--   0        0        0      679 2023-05-13 03:47:55.949791 gyver-2.1.0/gyver/url/fragment.py
+-rw-r--r--   0        0        0     2849 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/netloc.py
+-rw-r--r--   0        0        0     2863 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/path.py
+-rw-r--r--   0        0        0     1726 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/query.py
+-rw-r--r--   0        0        0      662 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/url/utils.py
+-rw-r--r--   0        0        0      674 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/utils/__init__.py
+-rw-r--r--   0        0        0      156 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/utils/exc.py
+-rw-r--r--   0        0        0     7836 2023-04-14 08:44:44.001856 gyver-2.1.0/gyver/utils/finder.py
+-rw-r--r--   0        0        0     1391 2023-04-14 08:44:44.003857 gyver-2.1.0/gyver/utils/helpers.py
+-rw-r--r--   0        0        0      174 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/json.py
+-rw-r--r--   0        0        0     2610 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/lazy.py
+-rw-r--r--   0        0        0     1319 2023-04-14 08:44:44.010861 gyver-2.1.0/gyver/utils/singleton.py
+-rw-r--r--   0        0        0     1718 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/strings.py
+-rw-r--r--   0        0        0      134 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/timezone.py
+-rw-r--r--   0        0        0     2418 2023-05-13 04:06:12.532636 gyver-2.1.0/pyproject.toml
+-rw-r--r--   0        0        0     2493 1970-01-01 00:00:00.000000 gyver-2.1.0/PKG-INFO
```

### Comparing `gyver-2.0.8/LICENSE` & `gyver-2.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/README.md` & `gyver-2.1.0/README.md`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/cache/asyncio.py` & `gyver-2.1.0/gyver/cache/asyncio.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,16 @@
 from typing import Literal
 from typing import Optional
 from typing import overload
 
+from gyver.attrs import call_init
+from gyver.attrs import define
+
 from gyver.utils import lazyfield
-from gyver.attrs import define, call_init
+
 from .config import CacheConfig
 from .interface import AsyncCacheInterface
 from .mapper import AsyncCacheMap
 from .mock import MockAsyncCache
 from .redis import AsyncRedisWrapper
 
 
@@ -31,19 +34,15 @@
 
     @staticmethod
     def _make_concrete(
         config: Optional[CacheConfig], test: bool
     ) -> AsyncCacheInterface:
         if test:
             return MockAsyncCache()
-        return (
-            AsyncRedisWrapper(config)
-            if config is not None
-            else AsyncRedisWrapper()
-        )
+        return AsyncRedisWrapper(config) if config is not None else AsyncRedisWrapper()
 
     @lazyfield
     def interface(self):
         return self._make_concrete(self.config, self.test)
 
     def mapper(self, name: str) -> AsyncCacheMap:
         return AsyncCacheMap(self.interface, name)
```

### Comparing `gyver-2.0.8/gyver/cache/interface.py` & `gyver-2.1.0/gyver/cache/interface.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/cache/mapper.py` & `gyver-2.1.0/gyver/cache/mapper.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/cache/mock.py` & `gyver-2.1.0/gyver/cache/mock.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,31 +3,30 @@
 from contextlib import asynccontextmanager
 from contextlib import contextmanager
 from contextlib import suppress
 from datetime import datetime
 from datetime import timezone
 from queue import Queue
 
+from gyver.attrs import define
+from gyver.attrs import info
+
 from gyver.exc import CacheMiss
 from gyver.utils import json
-from gyver.attrs import define, info
-
 from gyver.utils import lazyfield
 
 from .interface import AsyncCacheInterface
 from .interface import CacheInterface
 
 T = typing.TypeVar("T")
 
 
 @define
 class MockAsyncCache(AsyncCacheInterface):
-    key_map: typing.MutableMapping[str, typing.Any] = info(
-        default_factory=dict
-    )
+    key_map: typing.MutableMapping[str, typing.Any] = info(default_factory=dict)
 
     @lazyfield
     def _queue(self) -> asyncio.Queue[object]:
         size = 10
         queue = asyncio.Queue(size)
         for _ in range(size):
             queue.put_nowait(object())
@@ -89,17 +88,15 @@
         dumps: typing.Callable[[typing.Any], str] = json.dumps,
     ) -> None:
         async with self._in_queue():
             if map_name not in self.key_map:
                 self.key_map[map_name] = {}
             self.key_map[map_name][name] = dumps(value)
 
-    async def delete(
-        self, name: str, map_name: typing.Optional[str] = None
-    ) -> None:
+    async def delete(self, name: str, map_name: typing.Optional[str] = None) -> None:
         async with self._in_queue():
             used_map = self.key_map
             if map_name is not None:
                 if map_name not in self.key_map:
                     return
                 used_map = self.key_map[map_name]
 
@@ -132,17 +129,15 @@
     def _in_queue(self):
         try:
             self._queue.get()
             yield
         finally:
             self._queue.put(object())
 
-    def get(
-        self, name: str, cast: typing.Callable[[typing.Any], T] = json.loads
-    ) -> T:
+    def get(self, name: str, cast: typing.Callable[[typing.Any], T] = json.loads) -> T:
         with self._in_queue():
             try:
                 val = self.key_map[name]
                 if isinstance(val, dict):
                     raise CacheMiss
                 response, exp = val
             except KeyError:
```

### Comparing `gyver-2.0.8/gyver/cache/redis.py` & `gyver-2.1.0/gyver/cache/redis.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -4,18 +4,18 @@
 from typing import Callable
 from typing import Literal
 from typing import Optional
 from typing import TypeVar
 from typing import Union
 
 import redis
-from redis import asyncio as aioredis
-
 from gyver.attrs import define
 from gyver.attrs import info
+from redis import asyncio as aioredis
+
 from gyver.config import AdapterConfigFactory
 from gyver.exc import CacheMiss
 from gyver.utils import json
 from gyver.utils import lazyfield
 
 from .config import CacheConfig
 from .interface import AsyncCacheInterface
```

### Comparing `gyver-2.0.8/gyver/cache/sync.py` & `gyver-2.1.0/gyver/cache/sync.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 from typing import Literal
 from typing import Optional
 from typing import overload
 
+from gyver.attrs import call_init
+from gyver.attrs import define
+
 from gyver.utils import lazyfield
-from gyver.attrs import define, call_init
 
 from .config import CacheConfig
 from .interface import CacheInterface
 from .mapper import CacheMap
 from .mock import MockCache
 from .redis import RedisWrapper
 
@@ -27,17 +29,15 @@
 
     def __init__(
         self, *, config: Optional[CacheConfig] = None, test: bool = False
     ) -> None:
         call_init(self, config, test)
 
     @staticmethod
-    def _make_concrete(
-        config: Optional[CacheConfig], test: bool
-    ) -> CacheInterface:
+    def _make_concrete(config: Optional[CacheConfig], test: bool) -> CacheInterface:
         if test:
             return MockCache()
         return RedisWrapper() if config is None else RedisWrapper(config)
 
     @lazyfield
     def interface(self):
         return self._make_concrete(self.config, self.test)
```

### Comparing `gyver-2.0.8/gyver/cache/utils.py` & `gyver-2.1.0/gyver/cache/utils.py`

 * *Files 18% similar despite different names*

```diff
@@ -10,12 +10,12 @@
 
     :param config: CacheConfig: Pass the configuration to the function
     :return: A string that is a valid uri for connecting to redis
     """
     url = URL("")
     url.scheme = "redis"
     url.add(
-        netloc_args=Netloc("").set(
+        netloc_obj=Netloc("").set(
             config.host, config.user, config.password, config.port
         )
     )
     return url.encode()
```

### Comparing `gyver-2.0.8/gyver/config/adapter/attrs.py` & `gyver-2.1.0/gyver/config/adapter/attrs.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 from typing import Any
 from typing import Generator
 from typing import Sequence
 from typing import Union
 
 from attr._make import Factory
 from attrs import NOTHING
-from attrs import Attribute, fields
-
+from attrs import Attribute
+from attrs import fields
 from gyver.attrs import define
+
 from gyver.config.adapter.interface import FieldResolverStrategy
 from gyver.config.config import MISSING
 from gyver.exc import InvalidCast
 from gyver.utils import panic
 
 
 @define
@@ -21,17 +22,15 @@
     def cast(self) -> type:
         if field_type := self.field.type:
             return field_type
         raise panic(InvalidCast, f"Field {self.field.name} has no valid type")
 
     def names(self) -> Sequence[str]:
         return tuple(
-            item
-            for item in (self.field.name, self.field.alias)
-            if item is not None
+            item for item in (self.field.name, self.field.alias) if item is not None
         )
 
     def init_name(self) -> str:
         return self.field.alias or self.field.name
 
     def default(self) -> Union[Any, type[MISSING]]:
         default = self.field.default
```

### Comparing `gyver-2.0.8/gyver/config/adapter/dataclass.py` & `gyver-2.1.0/gyver/config/adapter/dataclass.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 from dataclasses import MISSING as dc_MISSING
-from dataclasses import Field, fields
+from dataclasses import Field
+from dataclasses import fields
 from typing import Any
 from typing import Generator
 from typing import Sequence
 from typing import Union
 
 from gyver.attrs import define
+
 from gyver.config.adapter.interface import FieldResolverStrategy
 from gyver.config.config import MISSING
 
 
 @define
 class DataclassResolverStrategy(FieldResolverStrategy[Field]):
     field: Field
```

### Comparing `gyver-2.0.8/gyver/config/adapter/factory.py` & `gyver-2.1.0/gyver/config/adapter/factory.py`

 * *Files 3% similar despite different names*

```diff
@@ -7,17 +7,18 @@
 from typing import Optional
 from typing import Sequence
 from typing import TypeVar
 from typing import cast
 from typing import get_args
 from typing import get_origin
 
+from gyver.attrs import define
+from gyver.attrs import mark_factory
 from pydantic import BaseModel
 
-from gyver.attrs import mark_factory, define
 from gyver.config.config import MISSING
 from gyver.config.config import Config
 from gyver.config.utils import boolean_cast
 from gyver.exc import MissingName
 from gyver.utils import finder
 from gyver.utils import json
 from gyver.utils import panic
@@ -36,29 +37,25 @@
 
 def _try_each(*names: str, default: Any, cast: Any, config: Config):
     for name in names:
         with suppress(MissingName):
             return config(name, cast)
     if default is not MISSING:
         return default
-    raise panic(
-        MissingName, f"{', '.join(names)} not found and no default was given"
-    )
+    raise panic(MissingName, f"{', '.join(names)} not found and no default was given")
 
 
 def _resolve_cast(outer_type: type):
     _sequences = (list, tuple, set)
     origin = get_origin(outer_type)
     if outer_type is bool:
         return boolean_cast
     if origin is None:
         return (
-            make_lex_separator(outer_type)
-            if outer_type in _sequences
-            else outer_type
+            make_lex_separator(outer_type) if outer_type in _sequences else outer_type
         )
     if (origin := get_origin(outer_type)) in _sequences:
         assert origin is not None
         args = get_args(outer_type)
         cast = args[0] if args else str
         return make_lex_separator(origin, cast)
     return _loads if dict in (origin, outer_type) else origin
@@ -68,17 +65,15 @@
     return json.loads(val) if isinstance(val, str) else val
 
 
 @define
 class AdapterConfigFactory:
     config: Config = _default_config
 
-    def get_strategy_class(
-        self, config_class: type
-    ) -> type[FieldResolverStrategy]:
+    def get_strategy_class(self, config_class: type) -> type[FieldResolverStrategy]:
         if hasattr(config_class, "__gyver_attrs__"):
             return GyverAttrsResolverStrategy
         elif is_dataclass(config_class):
             return DataclassResolverStrategy
         elif issubclass(config_class, BaseModel):
             return PydanticResolverStrategy
         elif hasattr(config_class, "__attrs_attrs__"):
@@ -116,17 +111,15 @@
         __prefix__: str = "",
         *,
         presets: Optional[Mapping[str, Any]] = None,
         **defaults: Any,
     ) -> Callable[[], T]:
         @mark_factory
         def load():
-            return self.load(
-                model_cls, __prefix__, presets=presets, **defaults
-            )
+            return self.load(model_cls, __prefix__, presets=presets, **defaults)
 
         return load
 
     def _get_value(
         self,
         model_cls: type,
         resolver: FieldResolverStrategy,
@@ -135,17 +128,15 @@
     ):
         names = self.resolve_names(model_cls, resolver, prefix)
         default = next(
             (result for name in names if (result := defaults.get(name))),
             resolver.default(),
         )
         cast = _resolve_cast(resolver.cast())
-        return _try_each(
-            *names, default=default, cast=cast, config=self.config
-        )
+        return _try_each(*names, default=default, cast=cast, config=self.config)
 
     def resolve_names(
         self, model_cls: type, resolver: FieldResolverStrategy, prefix: str
     ) -> Sequence[str]:
         names = resolver.names()
         prefix = prefix or getattr(model_cls, "__prefix__", "")
         prefix = prefix.removesuffix("_")
@@ -174,17 +165,15 @@
         It returns them in a dict of {class: (configs)}.
 
         :param cls: Call the class_validator function, which is used to validate that a
         class has all of the required attributes
         :param root: Path: Specify the root directory of the project
         :return: A dictionary of {class: (configs)}
         """
-        builder = (
-            finder.FinderBuilder().add_validator(is_config).from_path(root)
-        )
+        builder = finder.FinderBuilder().add_validator(is_config).from_path(root)
         output = builder.find()
         tempself = cls()
         return {
             cfg: tuple(
                 tempself.resolve_names(cfg, field, "")
                 for field in cfg.__fields__.values()
             )
```

### Comparing `gyver-2.0.8/gyver/config/adapter/gattrs.py` & `gyver-2.1.0/gyver/config/adapter/gattrs.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 from typing import Any
 from typing import Generator
 from typing import Sequence
 from typing import Union
 
-from gyver.attrs import define, fields
+from gyver.attrs import define
+from gyver.attrs import fields
 from gyver.attrs.field import Field
 from gyver.attrs.utils.typedef import MISSING as NOTHING
+
 from gyver.config.adapter.interface import FieldResolverStrategy
 from gyver.config.config import MISSING
 
 
 @define
 class GyverAttrsResolverStrategy(FieldResolverStrategy[Field]):
     field: Field
```

### Comparing `gyver-2.0.8/gyver/config/adapter/interface.py` & `gyver-2.1.0/gyver/config/adapter/interface.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,17 +8,16 @@
 
 from gyver.config.config import MISSING
 
 if TYPE_CHECKING:
     from dataclasses import Field
 
     from attrs import Attribute
-    from pydantic.fields import ModelField
-
     from gyver.attrs.field import Field as GField
+    from pydantic.fields import ModelField
 
 T = TypeVar("T", "ModelField", "Attribute", "Field", "GField")
 
 
 class FieldResolverStrategy(Protocol[T]):
     """
     A protocol for resolving the properties of a field, regardless of
```

### Comparing `gyver-2.0.8/gyver/config/adapter/mark.py` & `gyver-2.1.0/gyver/config/adapter/mark.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from typing import Any
 from typing import TypeVar
 
 import typing_extensions
-
 from gyver.attrs import define
 from gyver.attrs.field import FieldInfo
 from gyver.attrs.field import info
 
 # Sentinel object used to check if the __config_class__ attribute
 # has been set on the class
 SENTINEL = object()
```

### Comparing `gyver-2.0.8/gyver/config/adapter/pydantic.py` & `gyver-2.1.0/gyver/config/adapter/pydantic.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Any
 from typing import Generator
 from typing import Sequence
 from typing import Union
 
+from gyver.attrs import define
 from pydantic import BaseModel
 from pydantic.fields import ModelField
 
-from gyver.attrs import define
 from gyver.config.adapter.interface import FieldResolverStrategy
 from gyver.config.config import MISSING
 
 
 @define
 class PydanticResolverStrategy(FieldResolverStrategy[ModelField]):
     field: ModelField
```

### Comparing `gyver-2.0.8/gyver/config/config.py` & `gyver-2.1.0/gyver/config/config.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,19 +5,20 @@
 from typing import Callable
 from typing import Iterator
 from typing import MutableMapping
 from typing import TypeVar
 from typing import Union
 from typing import overload
 
+from gyver.attrs import define
+from gyver.attrs import info
+
 from gyver.exc import InvalidCast
 from gyver.exc import MissingName
 from gyver.utils.exc import panic
-from gyver.attrs import define, info
-
 from gyver.utils.lazy import lazyfield
 
 T = TypeVar("T")
 
 
 @define
 class EnvMapping(MutableMapping[str, str]):
@@ -27,17 +28,15 @@
     def __getitem__(self, name: str):
         val = self.mapping[name]
         self.already_read.add(name)
         return val
 
     def __setitem__(self, name: str, value: str):
         if name in self.already_read:
-            raise panic(
-                KeyError, f"{name} already read, cannot change its value"
-            )
+            raise panic(KeyError, f"{name} already read, cannot change its value")
         self.mapping[name] = value
 
     def __delitem__(self, name: str) -> None:
         if name in self.already_read:
             raise panic(KeyError, f"{name} already read, cannot delete")
         del self.mapping[name]
 
@@ -80,17 +79,15 @@
                 name, value = line.split("=", 1)
                 yield name.strip(), value.strip()
 
     def _cast(self, name: str, val: Any, cast: Callable) -> Any:
         try:
             val = cast(val)
         except Exception as e:
-            raise panic(
-                InvalidCast, f"{name} received an invalid value {val}"
-            ) from e
+            raise panic(InvalidCast, f"{name} received an invalid value {val}") from e
         else:
             return val
 
     def _get_val(
         self, name: str, default: Union[Any, type[MISSING]] = MISSING
     ) -> Union[Any, type[MISSING]]:
         return self.mapping.get(name, self.file_values.get(name, default))
@@ -99,17 +96,15 @@
         self,
         name: str,
         cast: Callable = _default_cast,
         default: Union[Any, type[MISSING]] = MISSING,
     ) -> Any:
         val = self._get_val(name, default)
         if val is MISSING:
-            raise panic(
-                MissingName, f"{name} not found and no default was given"
-            )
+            raise panic(MissingName, f"{name} not found and no default was given")
         return self._cast(name, val, cast)
 
     @overload
     def __call__(
         self,
         name: str,
         cast: Union[Callable[[Any], T], type[T]] = _default_cast,
```

### Comparing `gyver-2.0.8/gyver/config/envconfig.py` & `gyver-2.1.0/gyver/config/envconfig.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,17 @@
 import os
 from pathlib import Path
-from typing import Sequence, Union
+from typing import Sequence
+from typing import Union
+
+from gyver.attrs import call_init
+from gyver.attrs import define
+from gyver.attrs import info
 
 from gyver import utils
-from gyver.attrs import define, info, call_init
 
 from .config import Config
 from .config import EnvMapping
 from .config import default_mapping
 from .typedef import Env
```

### Comparing `gyver-2.0.8/gyver/config/typedef.py` & `gyver-2.1.0/gyver/config/typedef.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/context/atomic_/bound.py` & `gyver-2.1.0/gyver/context/atomic_/bound.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/context/atomic_/core.py` & `gyver-2.1.0/gyver/context/atomic_/core.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/context/atomic_/resolver.py` & `gyver-2.1.0/gyver/context/atomic_/resolver.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/context/context.py` & `gyver-2.1.0/gyver/context/context.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/context/interfaces/adapter.py` & `gyver-2.1.0/gyver/context/interfaces/adapter.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/crypto/fernet.py` & `gyver-2.1.0/gyver/crypto/fernet.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/crypto/rsa.py` & `gyver-2.1.0/gyver/crypto/rsa.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 from cryptography.hazmat.backends import default_backend
 from cryptography.hazmat.primitives import hashes
 from cryptography.hazmat.primitives import serialization
 from cryptography.hazmat.primitives.asymmetric import padding
 from cryptography.hazmat.primitives.asymmetric import rsa
+from gyver.attrs import define
+from gyver.attrs import info
 
 from gyver.config import AdapterConfigFactory
 from gyver.config import as_config
 from gyver.utils import lazyfield
-from gyver.attrs import define, info
 
 
 @as_config
 class RSACryptoConfig:
     __prefix__ = "crypto"
 
     private_key: str
```

### Comparing `gyver-2.0.8/gyver/database/__init__.py` & `gyver-2.1.0/gyver/database/__init__.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/adapter.py` & `gyver-2.1.0/gyver/database/adapter.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import typing
 
 import sqlalchemy as sa
-from sqlalchemy.ext.asyncio import create_async_engine
-
 from gyver.attrs import define
 from gyver.attrs import info
+from sqlalchemy.ext.asyncio import create_async_engine
+
 from gyver.config import AdapterConfigFactory
 from gyver.context import atomic
 from gyver.database.context.asyncio import AsyncSessionAdapter
 from gyver.database.context.sync import SessionAdapter
 from gyver.database.typedef import Driver
 from gyver.utils.lazy import lazyfield
 
@@ -37,17 +37,15 @@
 
     @lazyfield
     def async_engine(self):
         return create_async_engine(make_uri(self.config), **self.db_kwargs)
 
     @lazyfield
     def engine(self):
-        return sa.create_engine(
-            make_uri(self.config, sync=True), **self.db_kwargs
-        )
+        return sa.create_engine(make_uri(self.config, sync=True), **self.db_kwargs)
 
     def context(self):
         context = SaAdapter(engine=self.engine).context()
         return atomic(context) if self.config.autotransaction else context
 
     def async_context(self):
         context = AsyncConnectionAdapter(engine=self.async_engine).context()
```

### Comparing `gyver-2.0.8/gyver/database/config.py` & `gyver-2.1.0/gyver/database/config.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/context/asyncio.py` & `gyver-2.1.0/gyver/database/context/asyncio.py`

 * *Files 8% similar despite different names*

```diff
@@ -6,17 +6,15 @@
 from gyver.utils import lazyfield
 
 AsyncSaContext = context.AsyncContext[sa_asyncio.AsyncConnection]
 
 AsyncSessionContext = context.AsyncContext[sa_asyncio.AsyncSession]
 
 
-class AsyncConnectionAdapter(
-    context.AtomicAsyncAdapter[sa_asyncio.AsyncConnection]
-):
+class AsyncConnectionAdapter(context.AtomicAsyncAdapter[sa_asyncio.AsyncConnection]):
     @typing.overload
     def __init__(
         self,
         *,
         uri: str,
         engine: None = None,
     ) -> None:
@@ -62,23 +60,19 @@
     async def begin(self, client: sa_asyncio.AsyncConnection) -> None:
         if client.in_transaction():
             await client.begin_nested()
         else:
             await client.begin()
 
     async def commit(self, client: sa_asyncio.AsyncConnection) -> None:
-        if trx := (
-            client.get_nested_transaction() or client.get_transaction()
-        ):
+        if trx := (client.get_nested_transaction() or client.get_transaction()):
             await trx.commit()
 
     async def rollback(self, client: sa_asyncio.AsyncConnection) -> None:
-        if trx := (
-            client.get_nested_transaction() or client.get_transaction()
-        ):
+        if trx := (client.get_nested_transaction() or client.get_transaction()):
             await trx.rollback()
 
     async def in_atomic(self, client: sa_asyncio.AsyncConnection) -> bool:
         return client.in_transaction()
 
     def context(
         self,
```

### Comparing `gyver-2.0.8/gyver/database/context/sync.py` & `gyver-2.1.0/gyver/database/context/sync.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/drivers/utils.py` & `gyver-2.1.0/gyver/database/drivers/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/entity.py` & `gyver-2.1.0/gyver/database/entity.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/query/__init__.py` & `gyver-2.1.0/gyver/database/query/__init__.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -10,17 +10,17 @@
 from .paginate import FieldPaginate
 from .paginate import LimitOffsetPaginate
 from .paginate import Paginate
 from .utils import as_date
 from .utils import as_lower
 from .utils import as_time
 from .utils import as_upper
+from .where import ApplyWhere
 from .where import FieldResolver
 from .where import Where
-from .where import ApplyWhere
 from .where import and_
 from .where import or_
 
 __all__ = [
     "Where",
     "ApplyWhere",
     "FieldResolver",
```

### Comparing `gyver-2.0.8/gyver/database/query/_helpers.py` & `gyver-2.1.0/gyver/database/query/_helpers.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/query/comp.py` & `gyver-2.1.0/gyver/database/query/comp.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 import typing
 
 import sqlalchemy as sa
 
-
 from .interface import BindClause
 from .interface import Comparator
 from .interface import Comparison
 from .interface import FieldType
 from .interface import Sortable
```

### Comparing `gyver-2.0.8/gyver/database/query/interface.py` & `gyver-2.1.0/gyver/database/query/interface.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,17 +12,15 @@
 
 from gyver.database.entity import AbstractEntity
 from gyver.database.typedef import ClauseType
 
 ExecutableType = typing.Union[Select, Update, Delete]
 ExecutableT = typing.TypeVar("ExecutableT", bound=ExecutableType)
 Sortable = typing.Union[int, float, date, time]
-Comparison = typing.Union[
-    ColumnElement[sa.Boolean], BooleanClauseList, Function
-]
+Comparison = typing.Union[ColumnElement[sa.Boolean], BooleanClauseList, Function]
 FieldType = typing.Union[ColumnElement, sa.Column]
 T = typing.TypeVar("T", contravariant=True)
 Mapper = typing.Union[sa.Table, type[AbstractEntity]]
 
 
 class Comparator(typing.Protocol[T]):
     def __call__(self, field: FieldType, target: T) -> typing.Any:
```

### Comparing `gyver-2.0.8/gyver/database/query/order_by.py` & `gyver-2.1.0/gyver/database/query/order_by.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import enum
 import typing
-from gyver.attrs import define
 
+from gyver.attrs import define
 from sqlalchemy.sql import ColumnElement
 from sqlalchemy.sql import Select
 
 
 class OrderDirection(enum.Enum):
     ASC = "asc"
     DESC = "desc"
@@ -37,19 +37,13 @@
             query.order_by(self._apply_order(self._find_column(query)))
             if self._should_apply
             else query
         )
 
     def _find_column(self, query: Select) -> ColumnElement:
         try:
-            return next(
-                col for col in query.selected_columns if col.key == self.field
-            )
+            return next(col for col in query.selected_columns if col.key == self.field)
         except StopIteration:
-            raise ValueError(
-                f"Field {self.field} does not exist in query"
-            ) from None
+            raise ValueError(f"Field {self.field} does not exist in query") from None
 
     def _apply_order(self, col: ColumnElement):
-        return (
-            col.asc() if self.direction is OrderDirection.ASC else col.desc()
-        )
+        return col.asc() if self.direction is OrderDirection.ASC else col.desc()
```

### Comparing `gyver-2.0.8/gyver/database/query/paginate.py` & `gyver-2.1.0/gyver/database/query/paginate.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from abc import ABC
 from abc import abstractmethod
 
+from gyver.attrs import define
 from sqlalchemy.sql import Select
 
-from gyver.attrs import define
 from gyver.database.typedef import ClauseType
 
 from . import comp as cp
 from .interface import ApplyClause
 from .interface import Comparator
 from .where import Where
```

### Comparing `gyver-2.0.8/gyver/database/query/utils.py` & `gyver-2.1.0/gyver/database/query/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/database/query/where.py` & `gyver-2.1.0/gyver/database/query/where.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 import contextlib
 import typing
 
 import sqlalchemy as sa
+from gyver.attrs import call_init
+from gyver.attrs import define
 
-from gyver.attrs import define, call_init
 from gyver.database.typedef import ClauseType
 
 from . import _helpers
 from . import comp as cp
 from . import interface
 
 T = typing.TypeVar("T")
@@ -16,17 +17,15 @@
 
 
 class _BindCache:
     def __init__(self) -> None:
         self._cached: dict[typing.Hashable, interface.Comparison] = {}
         self.maxlen = CACHE_MAXLEN
 
-    def get(
-        self, key: typing.Hashable
-    ) -> typing.Optional[interface.Comparison]:
+    def get(self, key: typing.Hashable) -> typing.Optional[interface.Comparison]:
         try:
             return self._cached.get(key)
         except TypeError:
             return None
 
     def set(
         self, key: typing.Hashable, value: interface.Comparison
@@ -99,17 +98,15 @@
             return AlwaysTrue().bind(mapper)
         resolved = self.expected.resolve(mapper)
         if not isinstance(mapper, typing.Hashable):
             return self._get_comparison(
                 _helpers.retrieve_attr(mapper, self.field),
                 resolved,
             )
-        if (
-            value := _cache.get((mapper, self.field, resolved, self.comp))
-        ) is not None:
+        if (value := _cache.get((mapper, self.field, resolved, self.comp))) is not None:
             return value
         attr = _helpers.retrieve_attr(mapper, self.field)
 
         return _cache.set(
             (mapper, self.field, resolved, self.comp),
             self._get_comparison(attr, resolved),
         )
@@ -168,14 +165,12 @@
         del mapper
         return self._cmp
 
 
 class ApplyWhere(interface.ApplyClause):
     type_ = ClauseType.APPLY
 
-    def __init__(
-        self, mapper: interface.Mapper, *where: interface.BindClause
-    ) -> None:
+    def __init__(self, mapper: interface.Mapper, *where: interface.BindClause) -> None:
         self.where = and_(*where).bind(mapper)
 
     def apply(self, query: interface.ExecutableT) -> interface.ExecutableT:
         return query.where(self.where)
```

### Comparing `gyver-2.0.8/gyver/database/utils.py` & `gyver-2.1.0/gyver/database/utils.py`

 * *Files 10% similar despite different names*

```diff
@@ -25,23 +25,23 @@
 
     Returns:
         str: database URI in the format
         'dialect_name(+driver)?://username:password@host:port/dbname'
         if not only host else 'dialect_name(+driver)?://host'
     """
 
-    url = URL("").set(netloc_args=Netloc("").set(host=config.host))
+    url = URL("").set(netloc_obj=Netloc("").set(host=config.host))
     url.scheme = f"{drivers.build_dialect_scheme(config.dialect, sync)}"
 
     if config.dialect.only_host:
         return url.encode()
 
     return url.add(
         path=config.name,
-        netloc_args=Netloc("").set(
+        netloc_obj=Netloc("").set(
             username=config.user,
             password=config.password,
             port=config.effective_port,
         ),
     ).encode()
 
 
@@ -102,17 +102,15 @@
     lazy: str = "selectin",
     use_list: typing.Literal[True],  # pylint: disable=unused-argument
 ) -> list[EntityT]:
     ...
 
 
 def make_relation(
-    relation: typing.Union[
-        str, type[EntityT], typing.Callable[[], type[EntityT]]
-    ],
+    relation: typing.Union[str, type[EntityT], typing.Callable[[], type[EntityT]]],
     *,
     relation_name: str = "",
     back_populates: typing.Optional[str] = None,
     secondary: typing.Union[sa.Table, type, None] = None,
     foreign_keys: typing.Optional[list[typing.Any]] = None,
     lazy: str = "selectin",
     use_list: bool = False,  # noqa
@@ -133,13 +131,11 @@
 
 def create_relation_table(table_name: str, *entities: str):
     return sa.Table(
         table_name,
         default_metadata,
         sa.Column("id", sa.Integer, primary_key=True),
         *[
-            sa.Column(
-                f"{entity}_id", sa.Integer, sa.ForeignKey(f"{entity}.id")
-            )
+            sa.Column(f"{entity}_id", sa.Integer, sa.ForeignKey(f"{entity}.id"))
             for entity in entities
         ],
     )
```

### Comparing `gyver-2.0.8/gyver/model.py` & `gyver-2.1.0/gyver/model.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/url/core.py` & `gyver-2.1.0/gyver/url/core.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,21 +1,29 @@
 from collections import defaultdict
-from typing import Mapping
+from typing import Mapping, Union
 from typing import Optional
 from urllib.parse import urlparse
 from urllib.parse import urlunsplit
 
 from gyver.url.encode import Encodable
 from gyver.url.fragment import Fragment
 from gyver.url.netloc import Netloc
 from gyver.url.path import Path
 from gyver.url.query import Query
+from gyver.attrs import mutable
 
 
+@mutable(pydantic=False, eq=False)
 class URL(Encodable):
+    scheme: str
+    netloc: Netloc
+    path: Path
+    query: Query
+    fragment: Fragment
+
     def __init__(self, val: str) -> None:
         self.load(val)
 
     def load(self, val: str):
         parsed = urlparse(val)
         (
             self.scheme,
@@ -23,15 +31,14 @@
             path,
             _,
             query,
             fragment,
         ) = parsed
         self.query = Query(query)
         self.path = Path(path)
-        self.port = parsed.port
         self.fragment = Fragment(fragment)
         self.netloc = Netloc(netloc)
 
     def encode(self, omit_empty_equal: bool = True):
         resolved_query = (
             self.query.encode()
             if omit_empty_equal
@@ -43,69 +50,66 @@
                 self.netloc.encode(),
                 self.path.encode(),
                 resolved_query,
                 self.fragment.encode(),
             )
         )
 
-    def __repr__(self) -> str:
-        return object.__repr__(self)
-
     def add(
         self,
         queryasdict: Optional[Mapping[str, str]] = None,
         /,
         path: Optional[str] = None,
         query: Optional[Mapping[str, str]] = None,
         fragment: Optional[str] = None,
         netloc: Optional[str] = None,
-        netloc_args: Optional[Netloc] = None,
+        netloc_obj: Optional[Netloc] = None,
     ):
         if queryasdict:
             self.query.add(queryasdict)
         if path:
             self.path.add(path)
         if query:
             self.query.add(query)
         if fragment:
             self.fragment.set(fragment)
         if netloc:
             self.netloc = self.netloc.merge(Netloc(netloc))
-        if netloc_args:
-            self.netloc = self.netloc.merge(netloc_args)
+        if netloc_obj:
+            self.netloc = self.netloc.merge(netloc_obj)
         return self
 
     def set(
         self,
         queryasdict: Optional[Mapping[str, str]] = None,
         /,
         path: Optional[str] = None,
         query: Optional[Mapping[str, str]] = None,
         fragment: Optional[str] = None,
         netloc: Optional[str] = None,
-        netloc_args: Optional[Netloc] = None,
+        netloc_obj: Optional[Netloc] = None,
     ):
         if queryasdict:
             self.query.set(queryasdict)
         if path:
             self.path.set(path)
         if query:
             self.query.set(query)
         if fragment:
             self.fragment.set(fragment)
         if netloc:
             self.netloc.load(netloc)
-        if netloc_args:
-            self.netloc = netloc_args
+        if netloc_obj:
+            self.netloc = netloc_obj
         return self
 
     def copy(self):
         new_url = URL("")
         new_url.scheme = self.scheme
         new_url.fragment.fragment_str = self.fragment.fragment_str
         new_url.path.segments = self.path.segments.copy()
         new_url.query.params = defaultdict(
             list,
             ((key, list(value)) for key, value in self.query.params.items()),
         )
-        new_url.add(netloc_args=self.netloc)
+        new_url.add(netloc_obj=self.netloc)
         return new_url
```

### Comparing `gyver-2.0.8/gyver/url/netloc.py` & `gyver-2.1.0/gyver/url/netloc.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,22 @@
 from typing import Optional
 from urllib.parse import quote
 
 from gyver.url.encode import Encodable
 from gyver.url.utils import utf8
+from gyver.attrs import mutable
 
 
+@mutable(pydantic=False, eq=False)
 class Netloc(Encodable):
+    username: Optional[str]
+    password: Optional[str]
+    host: str
+    port: Optional[int]
+
     def __init__(self, netloc: str) -> None:
         self.username: Optional[str] = None
         self.password: Optional[str] = None
         self.load(netloc)
 
     def load(self, netloc: str):
         userinfo, _, host = netloc.partition("@")
```

### Comparing `gyver-2.0.8/gyver/url/path.py` & `gyver-2.1.0/gyver/url/path.py`

 * *Files 15% similar despite different names*

```diff
@@ -3,22 +3,27 @@
 from urllib.parse import quote
 from urllib.parse import unquote
 
 from gyver.url.encode import Encodable
 from gyver.url.utils import is_valid_encoded_path
 from gyver.url.utils import utf8
 
+from gyver.attrs import mutable
+
 PERCENT_REGEX = r"\%[a-fA-F\d][a-fA-F\d]"
 
 SAFE_SEGMENT_CHARS = ":@-._~!$&'()*+,;="
 
 
+@mutable(pydantic=False, eq=False)
 class Path(Encodable):
+    segments: list[str]
+
     def __init__(self, pathstr: str) -> None:
-        self.segments: list[str] = self._load(pathstr)
+        self.segments = self._load(pathstr)
 
     def _load(self, pathstr: str):
         path_segments = pathstr.split("/")
         return self._process_segments([], path_segments)
 
     def _process_segments(
         self,
@@ -32,20 +37,24 @@
             segments.append(seg)
         return [
             unquote(item.decode("utf-8") if isinstance(item, bytes) else item)
             for item in segments
         ]
 
     def encode(self):
-        return "/".join(quote(utf8(item), SAFE_SEGMENT_CHARS) for item in self.segments)
+        return "/".join(
+            quote(utf8(item), SAFE_SEGMENT_CHARS) for item in self.segments
+        )
 
     def add(self, path: Union[str, "Path"]):
         segments = []
         if isinstance(path, str):
-            segments.extend(self._process_segments([], path.lstrip("/").split("/")))
+            segments.extend(
+                self._process_segments([], path.lstrip("/").split("/"))
+            )
         else:
             segments.extend(path.segments)
         self.segments = self._process_segments(self.segments, segments)
         return self
 
     def set(self, path: Union[str, "Path"]):
         segments = []
```

### Comparing `gyver-2.0.8/gyver/url/query.py` & `gyver-2.1.0/gyver/url/query.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,20 +1,24 @@
 from collections import defaultdict
 from typing import Mapping
 from typing import Optional
 from urllib.parse import parse_qs
 from urllib.parse import quote
 
+from gyver.attrs import mutable
 from gyver.url.encode import Encodable
 
 
+@mutable(pydantic=False, eq=False)
 class Query(Encodable):
+    params: defaultdict[str, list[str]]
+
     def __init__(self, querystr: str) -> None:
-        self.params: defaultdict[str, list[str]] = defaultdict(list)
-        self.params.update(parse_qs(querystr, keep_blank_values=True))
+        self.params = defaultdict(list)
+        self.params |= parse_qs(querystr, keep_blank_values=True)
 
     def encode(self):
         return "&".join(
             "=".join((quote(key, safe=""), quote(item or "", safe="")))
             for key, value in self.params.items()
             for item in value
         )
```

### Comparing `gyver-2.0.8/gyver/url/utils.py` & `gyver-2.1.0/gyver/url/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/utils/__init__.py` & `gyver-2.1.0/gyver/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/utils/finder.py` & `gyver-2.1.0/gyver/utils/finder.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 import os
 import pathlib
 import sys
 import threading
 import typing
 
 from gyver.attrs import define
+
 from gyver.exc import InvalidPath
 from gyver.exc import MissingParams
 from gyver.utils.lazy import lazyfield
 
 PathConverter = typing.Callable[[pathlib.Path], str]
 StrOrPath = typing.Union[str, pathlib.Path]
 T = typing.TypeVar("T")
@@ -53,22 +54,18 @@
 
     @lazyfield
     def output(self):
         return dict(self)
 
     def __attrs_post_init__(self):
         if not self.root.exists():
-            raise InvalidPath(
-                f"root must be a valid path, received {self.root}"
-            )
+            raise InvalidPath(f"root must be a valid path, received {self.root}")
 
     def _should_look(self, path: pathlib.Path):
-        str_exclude = tuple(
-            item for item in self.exclude if isinstance(item, str)
-        )
+        str_exclude = tuple(item for item in self.exclude if isinstance(item, str))
         path_exclude = tuple(
             item for item in self.exclude if isinstance(item, pathlib.Path)
         )
         return (
             path.name not in str_exclude
             and path not in path_exclude
             and (not path.is_file() or path.name.endswith(".py"))
@@ -164,15 +161,14 @@
         if frame_info.filename == __file__:
             frame_info = next(
                 frame for frame in frame_stack if frame.filename != __file__
             )
 
         caller_path: str = frame_info.filename
         caller_absolute_path: str = os.path.abspath(caller_path)
-
         caller_root_path = next(
             iter(
                 sorted(
                     (p for p in sys.path if p in caller_absolute_path),
                     key=lambda p: len(p),
                 )
             )
@@ -180,17 +176,15 @@
 
         if not os.path.isabs(caller_path):
             caller_module_name: str = pathlib.Path(caller_path).name
             project_related_folders: str = caller_path.replace(
                 os.sep + caller_module_name, ""
             )
 
-            caller_root_path = caller_root_path.replace(
-                project_related_folders, ""
-            )
+            caller_root_path = caller_root_path.replace(project_related_folders, "")
 
         return self.from_path(pathlib.Path(caller_root_path))
 
     def from_package(self, stack_position: int = 1):
         """
         Finds the root path of the package that called the method and sets it as the
         base path for the finder.
```

### Comparing `gyver-2.0.8/gyver/utils/helpers.py` & `gyver-2.1.0/gyver/utils/helpers.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 import functools
 import warnings
 from typing import Callable
 from typing import TypeVar
 from typing import cast
 
-from typing_extensions import ParamSpec
-
 from gyver.attrs import define
+from typing_extensions import ParamSpec
 
 from .exc import panic
 
 
 def _not_implemented(msg: str):
     def inner(*_, **__kwds__):
         raise panic(NotImplementedError, msg)
```

### Comparing `gyver-2.0.8/gyver/utils/lazy.py` & `gyver-2.1.0/gyver/utils/lazy.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/gyver/utils/singleton.py` & `gyver-2.1.0/gyver/utils/singleton.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import typing
+
 from .helpers import deprecated
 
 T = typing.TypeVar("T")
 
 
 @deprecated
 def make_singleton(cls: type[T]) -> type[T]:
```

### Comparing `gyver-2.0.8/gyver/utils/strings.py` & `gyver-2.1.0/gyver/utils/strings.py`

 * *Files identical despite different names*

### Comparing `gyver-2.0.8/pyproject.toml` & `gyver-2.1.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gyver"
-version = "2.0.8"
+version = "2.1.0"
 description = "Toolbox for web development"
 authors = ["Gustavo Correa <self.gustavocorrea@gmail.com>"]
 readme = "README.md"
 repository = "https://github.com/guscardvs/gyver"
 
 [tool.poetry.dependencies]
 python = "^3.9"
@@ -14,17 +14,17 @@
 psycopg2 = { version = "^2.9.5", optional = true }
 asyncpg = { version = "^0.27.0", optional = true }
 aiomysql = { version = "^0.1.1", optional = true }
 pymysql = { version = "^1.0.2", optional = true }
 aiosqlite = { version = "^0.18.0", optional = true }
 tzdata = { markers = "sys_platform != \"linux\"", version = "^2022.6" }
 sqlalchemy = { version = "^2.0.4", optional = true }
-cryptography = "^38.0.4"
-redis = { version = "^4.4.0", optional = true }
-gyver-attrs = "^0.4.0"
+cryptography = "^40.0.2"
+redis = { version = "^4.5.5", optional = true }
+gyver-attrs = "^0.5.1"
 
 [tool.poetry.group.lint.dependencies]
 black = "^22.10.0"
 isort = "^5.10.1"
 flake8 = "^5.0.4"
 autoflake = "^1.7.7"
 
@@ -32,14 +32,15 @@
 pytest = "^7.2.0"
 pytest-cov = "^4.0.0"
 coverage = "^6.5.0"
 pytest-asyncio = "^0.20.1"
 hypothesis = "^6.56.4"
 fakeredis = "^2.4.0"
 moto = { extras = ["sqs", "s3"], version = "^4.0.12" }
+pytest-xdist = "^3.2.1"
 
 [tool.poetry.group.types.dependencies]
 sqlalchemy2-stubs = "^0.0.2a29"
 
 
 [tool.poetry.group.asgi.dependencies]
 starlette = "^0.21.0"
@@ -71,10 +72,25 @@
 line_length = 88
 
 [tool.isort]
 profile = 'black'
 line_length = 88
 force_single_line = true
 
+[tool.pytest.ini_options]
+asyncio_mode = "auto"
+addopts = [
+    "-n",
+    "4",
+    "--cov=gyver/",
+    "--cov-report=html",
+    "--cov-config=.coveragerc",
+    "--no-cov-on-fail",
+    "--cov-fail-under=80",
+]
+filterwarnings = [
+    "error",
+    "ignore:The --rsyncdir command line argument and rsyncdirs config variable are deprecated.:DeprecationWarning",
+]
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `gyver-2.0.8/PKG-INFO` & `gyver-2.1.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gyver
-Version: 2.0.8
+Version: 2.1.0
 Summary: Toolbox for web development
 Home-page: https://github.com/guscardvs/gyver
 Author: Gustavo Correa
 Author-email: self.gustavocorrea@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
@@ -14,21 +14,21 @@
 Provides-Extra: db-mariadb
 Provides-Extra: db-mysql
 Provides-Extra: db-pg
 Provides-Extra: db-sqlite
 Requires-Dist: aiomysql (>=0.1.1,<0.2.0) ; extra == "db-mysql" or extra == "db-mariadb"
 Requires-Dist: aiosqlite (>=0.18.0,<0.19.0) ; extra == "db-sqlite"
 Requires-Dist: asyncpg (>=0.27.0,<0.28.0) ; extra == "db-pg"
-Requires-Dist: cryptography (>=38.0.4,<39.0.0)
-Requires-Dist: gyver-attrs (>=0.4.0,<0.5.0)
+Requires-Dist: cryptography (>=40.0.2,<41.0.0)
+Requires-Dist: gyver-attrs (>=0.5.1,<0.6.0)
 Requires-Dist: orjson (>=3.8.1,<4.0.0)
 Requires-Dist: psycopg2 (>=2.9.5,<3.0.0) ; extra == "db-pg"
 Requires-Dist: pydantic[email] (>=1.10.2,<2.0.0)
 Requires-Dist: pymysql (>=1.0.2,<2.0.0) ; extra == "db-mysql" or extra == "db-mariadb"
-Requires-Dist: redis (>=4.4.0,<5.0.0) ; extra == "cache"
+Requires-Dist: redis (>=4.5.5,<5.0.0) ; extra == "cache"
 Requires-Dist: sqlalchemy (>=2.0.4,<3.0.0) ; extra == "db-mysql" or extra == "db-mariadb" or extra == "db-pg" or extra == "db-sqlite"
 Requires-Dist: typing-extensions (>=4.4.0,<5.0.0)
 Requires-Dist: tzdata (>=2022.6,<2023.0) ; sys_platform != "linux"
 Project-URL: Repository, https://github.com/guscardvs/gyver
 Description-Content-Type: text/markdown
 
 # Gyver
```

