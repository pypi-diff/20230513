# Comparing `tmp/gyver-2.1.0.tar.gz` & `tmp/gyver-2.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gyver-2.1.0.tar", max compression
+gzip compressed data, was "gyver-2.1.1.tar", max compression
```

## Comparing `gyver-2.1.0.tar` & `gyver-2.1.1.tar`

### file list

```diff
@@ -1,89 +1,89 @@
--rw-r--r--   0        0        0     1079 2023-03-29 07:24:24.843143 gyver-2.1.0/LICENSE
--rw-r--r--   0        0        0      993 2023-03-29 07:24:24.843143 gyver-2.1.0/README.md
--rw-r--r--   0        0        0      158 2023-05-13 04:06:12.532636 gyver-2.1.0/gyver/__init__.py
--rw-r--r--   0        0        0      359 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/__init__.py
--rw-r--r--   0        0        0     1201 2023-04-14 08:44:43.823769 gyver-2.1.0/gyver/cache/asyncio.py
--rw-r--r--   0        0        0      237 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/config.py
--rw-r--r--   0        0        0     1776 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/interface.py
--rw-r--r--   0        0        0     1395 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/cache/mapper.py
--rw-r--r--   0        0        0     5993 2023-04-14 08:44:43.832774 gyver-2.1.0/gyver/cache/mock.py
--rw-r--r--   0        0        0     4283 2023-04-14 08:44:43.835775 gyver-2.1.0/gyver/cache/redis.py
--rw-r--r--   0        0        0     1128 2023-04-14 08:44:43.837776 gyver-2.1.0/gyver/cache/sync.py
--rw-r--r--   0        0        0      558 2023-03-29 07:33:58.431990 gyver-2.1.0/gyver/cache/utils.py
--rw-r--r--   0        0        0      498 2023-03-29 07:24:24.843143 gyver-2.1.0/gyver/config/__init__.py
--rw-r--r--   0        0        0       78 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/adapter/__init__.py
--rw-r--r--   0        0        0     1320 2023-04-14 08:44:43.858786 gyver-2.1.0/gyver/config/adapter/attrs.py
--rw-r--r--   0        0        0     1078 2023-04-14 08:44:43.860787 gyver-2.1.0/gyver/config/adapter/dataclass.py
--rw-r--r--   0        0        0     5886 2023-04-14 08:44:43.866790 gyver-2.1.0/gyver/config/adapter/factory.py
--rw-r--r--   0        0        0     1056 2023-04-14 08:44:43.871793 gyver-2.1.0/gyver/config/adapter/gattrs.py
--rw-r--r--   0        0        0     2107 2023-04-14 08:44:43.875795 gyver-2.1.0/gyver/config/adapter/interface.py
--rw-r--r--   0        0        0     1701 2023-04-14 08:44:43.878796 gyver-2.1.0/gyver/config/adapter/mark.py
--rw-r--r--   0        0        0     1091 2023-04-14 08:44:43.881798 gyver-2.1.0/gyver/config/adapter/pydantic.py
--rw-r--r--   0        0        0     3435 2023-04-14 08:44:43.847781 gyver-2.1.0/gyver/config/config.py
--rw-r--r--   0        0        0     2126 2023-04-14 08:44:43.849782 gyver-2.1.0/gyver/config/envconfig.py
--rw-r--r--   0        0        0      587 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/typedef.py
--rw-r--r--   0        0        0      473 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/config/utils.py
--rw-r--r--   0        0        0      419 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/__init__.py
--rw-r--r--   0        0        0      288 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/__init__.py
--rw-r--r--   0        0        0     2317 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/bound.py
--rw-r--r--   0        0        0     2493 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/core.py
--rw-r--r--   0        0        0     1332 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/atomic_/resolver.py
--rw-r--r--   0        0        0     5659 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/context.py
--rw-r--r--   0        0        0      102 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/interfaces/__init__.py
--rw-r--r--   0        0        0     1525 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/interfaces/adapter.py
--rw-r--r--   0        0        0       39 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/context/typedef.py
--rw-r--r--   0        0        0      253 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/__init__.py
--rw-r--r--   0        0        0      133 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/config.py
--rw-r--r--   0        0        0      909 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/crypto/fernet.py
--rw-r--r--   0        0        0     1856 2023-04-14 08:44:43.914814 gyver-2.1.0/gyver/crypto/rsa.py
--rw-r--r--   0        0        0      749 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/__init__.py
--rw-r--r--   0        0        0     2136 2023-04-14 08:44:43.927820 gyver-2.1.0/gyver/database/adapter.py
--rw-r--r--   0        0        0     1233 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/config.py
--rw-r--r--   0        0        0      360 2023-03-29 07:24:24.844143 gyver-2.1.0/gyver/database/context/__init__.py
--rw-r--r--   0        0        0     3542 2023-04-14 08:44:42.980359 gyver-2.1.0/gyver/database/context/asyncio.py
--rw-r--r--   0        0        0     3349 2023-03-29 07:29:51.153084 gyver-2.1.0/gyver/database/context/sync.py
--rw-r--r--   0        0        0      170 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/__init__.py
--rw-r--r--   0        0        0      229 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/dialect.py
--rw-r--r--   0        0        0      224 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/interface.py
--rw-r--r--   0        0        0     1493 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/drivers/utils.py
--rw-r--r--   0        0        0     1076 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/entity.py
--rw-r--r--   0        0        0      498 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/entity.pyi
--rw-r--r--   0        0        0       50 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/metadata.py
--rw-r--r--   0        0        0     1012 2023-04-14 08:44:43.954833 gyver-2.1.0/gyver/database/query/__init__.py
--rw-r--r--   0        0        0     1692 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/_helpers.py
--rw-r--r--   0        0        0     2935 2023-04-14 08:44:43.960836 gyver-2.1.0/gyver/database/query/comp.py
--rw-r--r--   0        0        0      294 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/exc.py
--rw-r--r--   0        0        0     1353 2023-04-14 08:44:43.004370 gyver-2.1.0/gyver/database/query/interface.py
--rw-r--r--   0        0        0      279 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/null.py
--rw-r--r--   0        0        0     1270 2023-04-14 08:44:43.969841 gyver-2.1.0/gyver/database/query/order_by.py
--rw-r--r--   0        0        0     1239 2023-04-14 08:44:43.971842 gyver-2.1.0/gyver/database/query/paginate.py
--rw-r--r--   0        0        0      697 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/query/utils.py
--rw-r--r--   0        0        0     4613 2023-04-14 08:44:43.975844 gyver-2.1.0/gyver/database/query/where.py
--rw-r--r--   0        0        0      327 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/database/typedef.py
--rw-r--r--   0        0        0     4243 2023-04-14 08:44:43.080407 gyver-2.1.0/gyver/database/utils.py
--rw-r--r--   0        0        0     2030 2023-05-11 07:34:48.903992 gyver-2.1.0/gyver/exc.py
--rw-r--r--   0        0        0      857 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/model.py
--rw-r--r--   0        0        0      101 2023-05-08 11:52:12.095726 gyver-2.1.0/gyver/pools/__init__.py
--rw-r--r--   0        0        0     5804 2023-05-11 07:47:54.886111 gyver-2.1.0/gyver/pools/asyncio.py
--rw-r--r--   0        0        0     2200 2023-05-11 07:54:54.698462 gyver-2.1.0/gyver/pools/resource.py
--rw-r--r--   0        0        0     3871 2023-05-11 07:48:16.387841 gyver-2.1.0/gyver/pools/thread.py
--rw-r--r--   0        0        0        0 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/py.typed
--rw-r--r--   0        0        0      186 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/url/__init__.py
--rw-r--r--   0        0        0     3212 2023-05-13 03:47:35.995069 gyver-2.1.0/gyver/url/core.py
--rw-r--r--   0        0        0      423 2023-05-13 03:47:04.475970 gyver-2.1.0/gyver/url/encode.py
--rw-r--r--   0        0        0      679 2023-05-13 03:47:55.949791 gyver-2.1.0/gyver/url/fragment.py
--rw-r--r--   0        0        0     2849 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/netloc.py
--rw-r--r--   0        0        0     2863 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/path.py
--rw-r--r--   0        0        0     1726 2023-05-13 03:47:55.948790 gyver-2.1.0/gyver/url/query.py
--rw-r--r--   0        0        0      662 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/url/utils.py
--rw-r--r--   0        0        0      674 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/utils/__init__.py
--rw-r--r--   0        0        0      156 2023-03-29 07:24:24.845143 gyver-2.1.0/gyver/utils/exc.py
--rw-r--r--   0        0        0     7836 2023-04-14 08:44:44.001856 gyver-2.1.0/gyver/utils/finder.py
--rw-r--r--   0        0        0     1391 2023-04-14 08:44:44.003857 gyver-2.1.0/gyver/utils/helpers.py
--rw-r--r--   0        0        0      174 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/json.py
--rw-r--r--   0        0        0     2610 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/lazy.py
--rw-r--r--   0        0        0     1319 2023-04-14 08:44:44.010861 gyver-2.1.0/gyver/utils/singleton.py
--rw-r--r--   0        0        0     1718 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/strings.py
--rw-r--r--   0        0        0      134 2023-03-29 07:24:24.846143 gyver-2.1.0/gyver/utils/timezone.py
--rw-r--r--   0        0        0     2418 2023-05-13 04:06:12.532636 gyver-2.1.0/pyproject.toml
--rw-r--r--   0        0        0     2493 1970-01-01 00:00:00.000000 gyver-2.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1079 2023-03-29 07:24:24.843143 gyver-2.1.1/LICENSE
+-rw-r--r--   0        0        0      993 2023-03-29 07:24:24.843143 gyver-2.1.1/README.md
+-rw-r--r--   0        0        0      158 2023-05-13 16:49:41.026955 gyver-2.1.1/gyver/__init__.py
+-rw-r--r--   0        0        0      359 2023-03-29 07:24:24.843143 gyver-2.1.1/gyver/cache/__init__.py
+-rw-r--r--   0        0        0     1201 2023-04-14 08:44:43.823769 gyver-2.1.1/gyver/cache/asyncio.py
+-rw-r--r--   0        0        0      237 2023-03-29 07:24:24.843143 gyver-2.1.1/gyver/cache/config.py
+-rw-r--r--   0        0        0     1776 2023-03-29 07:24:24.843143 gyver-2.1.1/gyver/cache/interface.py
+-rw-r--r--   0        0        0     1395 2023-03-29 07:24:24.843143 gyver-2.1.1/gyver/cache/mapper.py
+-rw-r--r--   0        0        0     5993 2023-04-14 08:44:43.832774 gyver-2.1.1/gyver/cache/mock.py
+-rw-r--r--   0        0        0     4283 2023-04-14 08:44:43.835775 gyver-2.1.1/gyver/cache/redis.py
+-rw-r--r--   0        0        0     1128 2023-04-14 08:44:43.837776 gyver-2.1.1/gyver/cache/sync.py
+-rw-r--r--   0        0        0      558 2023-03-29 07:33:58.431990 gyver-2.1.1/gyver/cache/utils.py
+-rw-r--r--   0        0        0      498 2023-03-29 07:24:24.843143 gyver-2.1.1/gyver/config/__init__.py
+-rw-r--r--   0        0        0       78 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/config/adapter/__init__.py
+-rw-r--r--   0        0        0     1320 2023-04-14 08:44:43.858786 gyver-2.1.1/gyver/config/adapter/attrs.py
+-rw-r--r--   0        0        0     1078 2023-04-14 08:44:43.860787 gyver-2.1.1/gyver/config/adapter/dataclass.py
+-rw-r--r--   0        0        0     5886 2023-04-14 08:44:43.866790 gyver-2.1.1/gyver/config/adapter/factory.py
+-rw-r--r--   0        0        0     1056 2023-04-14 08:44:43.871793 gyver-2.1.1/gyver/config/adapter/gattrs.py
+-rw-r--r--   0        0        0     2107 2023-04-14 08:44:43.875795 gyver-2.1.1/gyver/config/adapter/interface.py
+-rw-r--r--   0        0        0     1701 2023-04-14 08:44:43.878796 gyver-2.1.1/gyver/config/adapter/mark.py
+-rw-r--r--   0        0        0     1091 2023-04-14 08:44:43.881798 gyver-2.1.1/gyver/config/adapter/pydantic.py
+-rw-r--r--   0        0        0     3435 2023-04-14 08:44:43.847781 gyver-2.1.1/gyver/config/config.py
+-rw-r--r--   0        0        0     2126 2023-04-14 08:44:43.849782 gyver-2.1.1/gyver/config/envconfig.py
+-rw-r--r--   0        0        0      587 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/config/typedef.py
+-rw-r--r--   0        0        0      473 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/config/utils.py
+-rw-r--r--   0        0        0      419 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/__init__.py
+-rw-r--r--   0        0        0      288 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/atomic_/__init__.py
+-rw-r--r--   0        0        0     2317 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/atomic_/bound.py
+-rw-r--r--   0        0        0     2493 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/atomic_/core.py
+-rw-r--r--   0        0        0     1332 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/atomic_/resolver.py
+-rw-r--r--   0        0        0     5659 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/context.py
+-rw-r--r--   0        0        0      102 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/interfaces/__init__.py
+-rw-r--r--   0        0        0     1525 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/interfaces/adapter.py
+-rw-r--r--   0        0        0       39 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/context/typedef.py
+-rw-r--r--   0        0        0      253 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/crypto/__init__.py
+-rw-r--r--   0        0        0      133 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/crypto/config.py
+-rw-r--r--   0        0        0      909 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/crypto/fernet.py
+-rw-r--r--   0        0        0     1856 2023-04-14 08:44:43.914814 gyver-2.1.1/gyver/crypto/rsa.py
+-rw-r--r--   0        0        0      749 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/database/__init__.py
+-rw-r--r--   0        0        0     2136 2023-04-14 08:44:43.927820 gyver-2.1.1/gyver/database/adapter.py
+-rw-r--r--   0        0        0     1233 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/database/config.py
+-rw-r--r--   0        0        0      360 2023-03-29 07:24:24.844143 gyver-2.1.1/gyver/database/context/__init__.py
+-rw-r--r--   0        0        0     3542 2023-04-14 08:44:42.980359 gyver-2.1.1/gyver/database/context/asyncio.py
+-rw-r--r--   0        0        0     3349 2023-03-29 07:29:51.153084 gyver-2.1.1/gyver/database/context/sync.py
+-rw-r--r--   0        0        0      170 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/drivers/__init__.py
+-rw-r--r--   0        0        0      229 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/drivers/dialect.py
+-rw-r--r--   0        0        0      224 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/drivers/interface.py
+-rw-r--r--   0        0        0     1493 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/drivers/utils.py
+-rw-r--r--   0        0        0     1076 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/entity.py
+-rw-r--r--   0        0        0      498 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/entity.pyi
+-rw-r--r--   0        0        0       50 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/metadata.py
+-rw-r--r--   0        0        0     1012 2023-04-14 08:44:43.954833 gyver-2.1.1/gyver/database/query/__init__.py
+-rw-r--r--   0        0        0     1692 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/query/_helpers.py
+-rw-r--r--   0        0        0     2935 2023-04-14 08:44:43.960836 gyver-2.1.1/gyver/database/query/comp.py
+-rw-r--r--   0        0        0      294 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/query/exc.py
+-rw-r--r--   0        0        0     1353 2023-04-14 08:44:43.004370 gyver-2.1.1/gyver/database/query/interface.py
+-rw-r--r--   0        0        0      279 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/query/null.py
+-rw-r--r--   0        0        0     1270 2023-04-14 08:44:43.969841 gyver-2.1.1/gyver/database/query/order_by.py
+-rw-r--r--   0        0        0     1239 2023-04-14 08:44:43.971842 gyver-2.1.1/gyver/database/query/paginate.py
+-rw-r--r--   0        0        0      697 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/query/utils.py
+-rw-r--r--   0        0        0     4613 2023-04-14 08:44:43.975844 gyver-2.1.1/gyver/database/query/where.py
+-rw-r--r--   0        0        0      327 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/database/typedef.py
+-rw-r--r--   0        0        0     4243 2023-04-14 08:44:43.080407 gyver-2.1.1/gyver/database/utils.py
+-rw-r--r--   0        0        0     2030 2023-05-11 07:34:48.903992 gyver-2.1.1/gyver/exc.py
+-rw-r--r--   0        0        0      857 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/model.py
+-rw-r--r--   0        0        0      101 2023-05-08 11:52:12.095726 gyver-2.1.1/gyver/pools/__init__.py
+-rw-r--r--   0        0        0     5764 2023-05-13 16:48:20.474968 gyver-2.1.1/gyver/pools/asyncio.py
+-rw-r--r--   0        0        0     2225 2023-05-13 16:48:21.238958 gyver-2.1.1/gyver/pools/resource.py
+-rw-r--r--   0        0        0     3855 2023-05-13 16:48:01.539206 gyver-2.1.1/gyver/pools/thread.py
+-rw-r--r--   0        0        0        0 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/py.typed
+-rw-r--r--   0        0        0      186 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/url/__init__.py
+-rw-r--r--   0        0        0     3166 2023-05-13 16:48:22.167946 gyver-2.1.1/gyver/url/core.py
+-rw-r--r--   0        0        0      423 2023-05-13 03:47:04.475970 gyver-2.1.1/gyver/url/encode.py
+-rw-r--r--   0        0        0      664 2023-05-13 16:48:21.208958 gyver-2.1.1/gyver/url/fragment.py
+-rw-r--r--   0        0        0     2834 2023-05-13 16:48:21.209958 gyver-2.1.1/gyver/url/netloc.py
+-rw-r--r--   0        0        0     2795 2023-05-13 16:48:21.212958 gyver-2.1.1/gyver/url/path.py
+-rw-r--r--   0        0        0     1711 2023-05-13 16:48:21.213958 gyver-2.1.1/gyver/url/query.py
+-rw-r--r--   0        0        0      662 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/url/utils.py
+-rw-r--r--   0        0        0      674 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/utils/__init__.py
+-rw-r--r--   0        0        0      156 2023-03-29 07:24:24.845143 gyver-2.1.1/gyver/utils/exc.py
+-rw-r--r--   0        0        0     7836 2023-04-14 08:44:44.001856 gyver-2.1.1/gyver/utils/finder.py
+-rw-r--r--   0        0        0     1391 2023-04-14 08:44:44.003857 gyver-2.1.1/gyver/utils/helpers.py
+-rw-r--r--   0        0        0      174 2023-03-29 07:24:24.846143 gyver-2.1.1/gyver/utils/json.py
+-rw-r--r--   0        0        0     2610 2023-03-29 07:24:24.846143 gyver-2.1.1/gyver/utils/lazy.py
+-rw-r--r--   0        0        0     1319 2023-04-14 08:44:44.010861 gyver-2.1.1/gyver/utils/singleton.py
+-rw-r--r--   0        0        0     1718 2023-03-29 07:24:24.846143 gyver-2.1.1/gyver/utils/strings.py
+-rw-r--r--   0        0        0      134 2023-03-29 07:24:24.846143 gyver-2.1.1/gyver/utils/timezone.py
+-rw-r--r--   0        0        0     2418 2023-05-13 16:49:41.023955 gyver-2.1.1/pyproject.toml
+-rw-r--r--   0        0        0     2493 1970-01-01 00:00:00.000000 gyver-2.1.1/PKG-INFO
```

### Comparing `gyver-2.1.0/LICENSE` & `gyver-2.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/README.md` & `gyver-2.1.1/README.md`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/asyncio.py` & `gyver-2.1.1/gyver/cache/asyncio.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/interface.py` & `gyver-2.1.1/gyver/cache/interface.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/mapper.py` & `gyver-2.1.1/gyver/cache/mapper.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/mock.py` & `gyver-2.1.1/gyver/cache/mock.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/redis.py` & `gyver-2.1.1/gyver/cache/redis.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/sync.py` & `gyver-2.1.1/gyver/cache/sync.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/cache/utils.py` & `gyver-2.1.1/gyver/cache/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/attrs.py` & `gyver-2.1.1/gyver/config/adapter/attrs.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/dataclass.py` & `gyver-2.1.1/gyver/config/adapter/dataclass.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/factory.py` & `gyver-2.1.1/gyver/config/adapter/factory.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/gattrs.py` & `gyver-2.1.1/gyver/config/adapter/gattrs.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/interface.py` & `gyver-2.1.1/gyver/config/adapter/interface.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/mark.py` & `gyver-2.1.1/gyver/config/adapter/mark.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/adapter/pydantic.py` & `gyver-2.1.1/gyver/config/adapter/pydantic.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/config.py` & `gyver-2.1.1/gyver/config/config.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/envconfig.py` & `gyver-2.1.1/gyver/config/envconfig.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/config/typedef.py` & `gyver-2.1.1/gyver/config/typedef.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/context/atomic_/bound.py` & `gyver-2.1.1/gyver/context/atomic_/bound.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/context/atomic_/core.py` & `gyver-2.1.1/gyver/context/atomic_/core.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/context/atomic_/resolver.py` & `gyver-2.1.1/gyver/context/atomic_/resolver.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/context/context.py` & `gyver-2.1.1/gyver/context/context.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/context/interfaces/adapter.py` & `gyver-2.1.1/gyver/context/interfaces/adapter.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/crypto/fernet.py` & `gyver-2.1.1/gyver/crypto/fernet.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/crypto/rsa.py` & `gyver-2.1.1/gyver/crypto/rsa.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/__init__.py` & `gyver-2.1.1/gyver/database/__init__.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/adapter.py` & `gyver-2.1.1/gyver/database/adapter.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/config.py` & `gyver-2.1.1/gyver/database/config.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/context/asyncio.py` & `gyver-2.1.1/gyver/database/context/asyncio.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/context/sync.py` & `gyver-2.1.1/gyver/database/context/sync.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/drivers/utils.py` & `gyver-2.1.1/gyver/database/drivers/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/entity.py` & `gyver-2.1.1/gyver/database/entity.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/__init__.py` & `gyver-2.1.1/gyver/database/query/__init__.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/_helpers.py` & `gyver-2.1.1/gyver/database/query/_helpers.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/comp.py` & `gyver-2.1.1/gyver/database/query/comp.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/interface.py` & `gyver-2.1.1/gyver/database/query/interface.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/order_by.py` & `gyver-2.1.1/gyver/database/query/order_by.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/paginate.py` & `gyver-2.1.1/gyver/database/query/paginate.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/utils.py` & `gyver-2.1.1/gyver/database/query/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/query/where.py` & `gyver-2.1.1/gyver/database/query/where.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/database/utils.py` & `gyver-2.1.1/gyver/database/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/exc.py` & `gyver-2.1.1/gyver/exc.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/model.py` & `gyver-2.1.1/gyver/model.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/pools/asyncio.py` & `gyver-2.1.1/gyver/pools/asyncio.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 T = TypeVar("T")
 
 
 FactoryType = Callable[[], Coroutine[Any, Any, T]]
 ReleaserType = Callable[[T], Coroutine[Any, Any, None]]
 
 
-@mutable(pydantic=False)
+@mutable
 class AsyncPool(Generic[T]):
     resources: asyncio.Queue[Resource[T]]
     factory: FactoryType[T]
     releaser: ReleaserType[T]
     _pool_recycle: float
     _pool_size: int
     _available: int
@@ -119,17 +119,15 @@
 
         :param count: The amount of resources to initialize, up to the
             `pool_size`. Defaults to the pool_size if None.
         """
         count = count or self._pool_size
         count = min(count, self._pool_size)
 
-        while (
-            self.resources.qsize() < count and await self._decrease_available()
-        ):
+        while self.resources.qsize() < count and await self._decrease_available():
             resource = await self._initialize_resource()
             self.resources.put_nowait(resource)
 
     async def dispose(self) -> None:
         """
         Remove and release all items of from the queue.
```

### Comparing `gyver-2.1.0/gyver/pools/resource.py` & `gyver-2.1.1/gyver/pools/resource.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 from time import time
-from typing import Any, Generic
+from typing import Any
+from typing import Generic
 from typing import TypeVar
 
-from gyver.attrs import define, mutable
+from gyver.attrs import define
+from gyver.attrs import mutable
 
 from gyver.exc import InvalidParamType
 
 T = TypeVar("T")
 
 
 STARTTIME_ATTR = "_gyver_starttime_"
 
 
-@mutable(pydantic=False)
+@mutable
 class ResourceProxy:
     _target: Any
     _gyver_starttime_: float
 
     def __init__(self, target: Any, starttime: float):
         object.__setattr__(self, "_target", target)
         object.__setattr__(self, "_gyver_starttime_", starttime)
```

### Comparing `gyver-2.1.0/gyver/pools/thread.py` & `gyver-2.1.1/gyver/pools/thread.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 T = TypeVar("T")
 
 
 FactoryType = Callable[[], T]
 ReleaserType = Callable[[T], None]
 
 
-@mutable(pydantic=False)
+@mutable
 class ThreadPool(Generic[T]):
     resources: Queue[Resource[T]]
     factory: FactoryType[T]
     releaser: ReleaserType[T]
     _pool_recycle: float
     _pool_size: int
     _available: int
```

### Comparing `gyver-2.1.0/gyver/url/core.py` & `gyver-2.1.1/gyver/url/core.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 from collections import defaultdict
-from typing import Mapping, Union
+from typing import Mapping
 from typing import Optional
 from urllib.parse import urlparse
 from urllib.parse import urlunsplit
 
+from gyver.attrs import mutable
+
 from gyver.url.encode import Encodable
 from gyver.url.fragment import Fragment
 from gyver.url.netloc import Netloc
 from gyver.url.path import Path
 from gyver.url.query import Query
-from gyver.attrs import mutable
 
 
-@mutable(pydantic=False, eq=False)
+@mutable(eq=False)
 class URL(Encodable):
     scheme: str
     netloc: Netloc
     path: Path
     query: Query
     fragment: Fragment
 
@@ -36,17 +37,15 @@
         self.query = Query(query)
         self.path = Path(path)
         self.fragment = Fragment(fragment)
         self.netloc = Netloc(netloc)
 
     def encode(self, omit_empty_equal: bool = True):
         resolved_query = (
-            self.query.encode()
-            if omit_empty_equal
-            else self.query.omit_empty_equal()
+            self.query.encode() if omit_empty_equal else self.query.omit_empty_equal()
         )
         return urlunsplit(
             (
                 self.scheme,
                 self.netloc.encode(),
                 self.path.encode(),
                 resolved_query,
```

### Comparing `gyver-2.1.0/gyver/url/fragment.py` & `gyver-2.1.1/gyver/url/fragment.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 from urllib.parse import quote
 
+from gyver.attrs import mutable
+
 from gyver.url.encode import Encodable
 from gyver.url.utils import is_valid_encoded_path
 from gyver.url.utils import utf8
-from gyver.attrs import mutable
 
 
-@mutable(pydantic=False, eq=False)
+@mutable(eq=False)
 class Fragment(Encodable):
     fragment_str: str
 
     def __init__(self, fragment_str: str) -> None:
         self.set(fragment_str)
 
     def encode(self):
```

### Comparing `gyver-2.1.0/gyver/url/netloc.py` & `gyver-2.1.1/gyver/url/netloc.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 from typing import Optional
 from urllib.parse import quote
 
+from gyver.attrs import mutable
+
 from gyver.url.encode import Encodable
 from gyver.url.utils import utf8
-from gyver.attrs import mutable
 
 
-@mutable(pydantic=False, eq=False)
+@mutable(eq=False)
 class Netloc(Encodable):
     username: Optional[str]
     password: Optional[str]
     host: str
     port: Optional[int]
 
     def __init__(self, netloc: str) -> None:
```

### Comparing `gyver-2.1.0/gyver/url/path.py` & `gyver-2.1.1/gyver/url/path.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 import re
 from typing import Union
 from urllib.parse import quote
 from urllib.parse import unquote
 
+from gyver.attrs import mutable
+
 from gyver.url.encode import Encodable
 from gyver.url.utils import is_valid_encoded_path
 from gyver.url.utils import utf8
 
-from gyver.attrs import mutable
-
 PERCENT_REGEX = r"\%[a-fA-F\d][a-fA-F\d]"
 
 SAFE_SEGMENT_CHARS = ":@-._~!$&'()*+,;="
 
 
-@mutable(pydantic=False, eq=False)
+@mutable(eq=False)
 class Path(Encodable):
     segments: list[str]
 
     def __init__(self, pathstr: str) -> None:
         self.segments = self._load(pathstr)
 
     def _load(self, pathstr: str):
@@ -37,24 +37,20 @@
             segments.append(seg)
         return [
             unquote(item.decode("utf-8") if isinstance(item, bytes) else item)
             for item in segments
         ]
 
     def encode(self):
-        return "/".join(
-            quote(utf8(item), SAFE_SEGMENT_CHARS) for item in self.segments
-        )
+        return "/".join(quote(utf8(item), SAFE_SEGMENT_CHARS) for item in self.segments)
 
     def add(self, path: Union[str, "Path"]):
         segments = []
         if isinstance(path, str):
-            segments.extend(
-                self._process_segments([], path.lstrip("/").split("/"))
-            )
+            segments.extend(self._process_segments([], path.lstrip("/").split("/")))
         else:
             segments.extend(path.segments)
         self.segments = self._process_segments(self.segments, segments)
         return self
 
     def set(self, path: Union[str, "Path"]):
         segments = []
```

### Comparing `gyver-2.1.0/gyver/url/query.py` & `gyver-2.1.1/gyver/url/query.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 from collections import defaultdict
 from typing import Mapping
 from typing import Optional
 from urllib.parse import parse_qs
 from urllib.parse import quote
 
 from gyver.attrs import mutable
+
 from gyver.url.encode import Encodable
 
 
-@mutable(pydantic=False, eq=False)
+@mutable(eq=False)
 class Query(Encodable):
     params: defaultdict[str, list[str]]
 
     def __init__(self, querystr: str) -> None:
         self.params = defaultdict(list)
         self.params |= parse_qs(querystr, keep_blank_values=True)
```

### Comparing `gyver-2.1.0/gyver/url/utils.py` & `gyver-2.1.1/gyver/url/utils.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/__init__.py` & `gyver-2.1.1/gyver/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/finder.py` & `gyver-2.1.1/gyver/utils/finder.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/helpers.py` & `gyver-2.1.1/gyver/utils/helpers.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/lazy.py` & `gyver-2.1.1/gyver/utils/lazy.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/singleton.py` & `gyver-2.1.1/gyver/utils/singleton.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/gyver/utils/strings.py` & `gyver-2.1.1/gyver/utils/strings.py`

 * *Files identical despite different names*

### Comparing `gyver-2.1.0/pyproject.toml` & `gyver-2.1.1/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gyver"
-version = "2.1.0"
+version = "2.1.1"
 description = "Toolbox for web development"
 authors = ["Gustavo Correa <self.gustavocorrea@gmail.com>"]
 readme = "README.md"
 repository = "https://github.com/guscardvs/gyver"
 
 [tool.poetry.dependencies]
 python = "^3.9"
@@ -16,15 +16,15 @@
 aiomysql = { version = "^0.1.1", optional = true }
 pymysql = { version = "^1.0.2", optional = true }
 aiosqlite = { version = "^0.18.0", optional = true }
 tzdata = { markers = "sys_platform != \"linux\"", version = "^2022.6" }
 sqlalchemy = { version = "^2.0.4", optional = true }
 cryptography = "^40.0.2"
 redis = { version = "^4.5.5", optional = true }
-gyver-attrs = "^0.5.1"
+gyver-attrs = "^0.5.2"
 
 [tool.poetry.group.lint.dependencies]
 black = "^22.10.0"
 isort = "^5.10.1"
 flake8 = "^5.0.4"
 autoflake = "^1.7.7"
```

### Comparing `gyver-2.1.0/PKG-INFO` & `gyver-2.1.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gyver
-Version: 2.1.0
+Version: 2.1.1
 Summary: Toolbox for web development
 Home-page: https://github.com/guscardvs/gyver
 Author: Gustavo Correa
 Author-email: self.gustavocorrea@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
@@ -15,15 +15,15 @@
 Provides-Extra: db-mysql
 Provides-Extra: db-pg
 Provides-Extra: db-sqlite
 Requires-Dist: aiomysql (>=0.1.1,<0.2.0) ; extra == "db-mysql" or extra == "db-mariadb"
 Requires-Dist: aiosqlite (>=0.18.0,<0.19.0) ; extra == "db-sqlite"
 Requires-Dist: asyncpg (>=0.27.0,<0.28.0) ; extra == "db-pg"
 Requires-Dist: cryptography (>=40.0.2,<41.0.0)
-Requires-Dist: gyver-attrs (>=0.5.1,<0.6.0)
+Requires-Dist: gyver-attrs (>=0.5.2,<0.6.0)
 Requires-Dist: orjson (>=3.8.1,<4.0.0)
 Requires-Dist: psycopg2 (>=2.9.5,<3.0.0) ; extra == "db-pg"
 Requires-Dist: pydantic[email] (>=1.10.2,<2.0.0)
 Requires-Dist: pymysql (>=1.0.2,<2.0.0) ; extra == "db-mysql" or extra == "db-mariadb"
 Requires-Dist: redis (>=4.5.5,<5.0.0) ; extra == "cache"
 Requires-Dist: sqlalchemy (>=2.0.4,<3.0.0) ; extra == "db-mysql" or extra == "db-mariadb" or extra == "db-pg" or extra == "db-sqlite"
 Requires-Dist: typing-extensions (>=4.4.0,<5.0.0)
```

