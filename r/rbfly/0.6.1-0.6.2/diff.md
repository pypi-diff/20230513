# Comparing `tmp/rbfly-0.6.1.tar.gz` & `tmp/rbfly-0.6.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rbfly-0.6.1.tar", last modified: Sat Mar 18 23:54:46 2023, max compression
+gzip compressed data, was "rbfly-0.6.2.tar", last modified: Fri May 12 22:32:40 2023, max compression
```

## Comparing `rbfly-0.6.1.tar` & `rbfly-0.6.2.tar`

### file list

```diff
@@ -1,64 +1,64 @@
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.026779 rbfly-0.6.1/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    35147 2023-01-11 23:13:37.000000 rbfly-0.6.1/COPYING
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1417 2023-03-18 23:54:46.026779 rbfly-0.6.1/PKG-INFO
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      712 2023-01-11 23:13:37.000000 rbfly-0.6.1/README
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      174 2023-02-07 19:00:14.000000 rbfly-0.6.1/pyproject.toml
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.016779 rbfly-0.6.1/rbfly/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      935 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/__init__.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   143260 2023-02-24 21:26:03.000000 rbfly-0.6.1/rbfly/_buffer.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1435 2023-01-16 12:48:43.000000 rbfly-0.6.1/rbfly/_buffer.pxd
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1898 2023-01-30 12:32:49.000000 rbfly-0.6.1/rbfly/_buffer.pyx
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   126976 2023-02-24 21:26:03.000000 rbfly-0.6.1/rbfly/_codec.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1098 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/_codec.h
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1185 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/_codec.pxd
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2298 2023-01-12 14:54:58.000000 rbfly-0.6.1/rbfly/_codec.pyx
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.020112 rbfly-0.6.1/rbfly/amqp/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      956 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/amqp/__init__.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   495086 2023-02-24 21:26:04.000000 rbfly-0.6.1/rbfly/amqp/_message.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1412 2023-01-17 19:10:28.000000 rbfly-0.6.1/rbfly/amqp/_message.pxd
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1437 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/amqp/_message.pyi
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    19793 2023-01-30 23:02:18.000000 rbfly-0.6.1/rbfly/amqp/_message.pyx
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3894 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/cm.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1335 2023-01-30 14:42:53.000000 rbfly-0.6.1/rbfly/error.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)        0 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/py.typed
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.026779 rbfly-0.6.1/rbfly/streams/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1471 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/__init__.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   774231 2023-03-18 23:22:21.000000 rbfly-0.6.1/rbfly/streams/_client.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1697 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/_client.pyi
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    11251 2023-03-18 23:13:07.000000 rbfly-0.6.1/rbfly/streams/_client.pyx
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   498364 2023-03-18 23:36:28.000000 rbfly-0.6.1/rbfly/streams/_codec.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1600 2023-01-30 21:09:01.000000 rbfly-0.6.1/rbfly/streams/_codec.pyi
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    12624 2023-03-18 23:24:25.000000 rbfly-0.6.1/rbfly/streams/_codec.pyx
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)   309662 2023-02-24 21:26:04.000000 rbfly-0.6.1/rbfly/streams/_mqueue.c
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1244 2023-02-01 18:34:41.000000 rbfly-0.6.1/rbfly/streams/_mqueue.pyi
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3933 2023-02-21 20:27:20.000000 rbfly-0.6.1/rbfly/streams/_mqueue.pyx
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    17949 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/client.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     8690 2023-01-18 14:02:15.000000 rbfly-0.6.1/rbfly/streams/codec.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1894 2023-02-01 15:06:50.000000 rbfly-0.6.1/rbfly/streams/const.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1103 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/error.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     5229 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/offset.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    29310 2023-02-22 08:28:18.000000 rbfly-0.6.1/rbfly/streams/protocol.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1075 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/types.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     4004 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/streams/util.py
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.026779 rbfly-0.6.1/rbfly/tests/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/tests/__init__.py
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.026779 rbfly-0.6.1/rbfly/tests/amqp/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/tests/amqp/__init__.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     9581 2023-01-30 23:07:03.000000 rbfly-0.6.1/rbfly/tests/amqp/test_message.py
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.026779 rbfly-0.6.1/rbfly/tests/streams/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/tests/streams/__init__.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    11503 2023-03-18 23:14:09.000000 rbfly-0.6.1/rbfly/tests/streams/test_client.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)    13192 2023-03-18 23:21:44.000000 rbfly-0.6.1/rbfly/tests/streams/test_codec.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2271 2023-02-01 15:02:22.000000 rbfly-0.6.1/rbfly/tests/streams/test_mqueue.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1344 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/tests/streams/test_offset.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3228 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/tests/test_util.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1826 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/types.py
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2008 2023-01-11 23:13:37.000000 rbfly-0.6.1/rbfly/util.py
-drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-03-18 23:54:46.020112 rbfly-0.6.1/rbfly.egg-info/
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1417 2023-03-18 23:54:44.000000 rbfly-0.6.1/rbfly.egg-info/PKG-INFO
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1235 2023-03-18 23:54:46.000000 rbfly-0.6.1/rbfly.egg-info/SOURCES.txt
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)        1 2023-03-18 23:54:45.000000 rbfly-0.6.1/rbfly.egg-info/dependency_links.txt
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)      157 2023-03-18 23:54:45.000000 rbfly-0.6.1/rbfly.egg-info/requires.txt
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)        6 2023-03-18 23:54:45.000000 rbfly-0.6.1/rbfly.egg-info/top_level.txt
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1326 2023-03-18 23:54:46.026779 rbfly-0.6.1/setup.cfg
--rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1633 2023-01-14 12:57:42.000000 rbfly-0.6.1/setup.py
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.425956 rbfly-0.6.2/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    35147 2023-01-11 23:13:37.000000 rbfly-0.6.2/COPYING
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1417 2023-05-12 22:32:40.425956 rbfly-0.6.2/PKG-INFO
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      712 2023-01-11 23:13:37.000000 rbfly-0.6.2/README
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      174 2023-04-25 16:53:09.000000 rbfly-0.6.2/pyproject.toml
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.422623 rbfly-0.6.2/rbfly/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      935 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/__init__.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   143323 2023-05-12 15:51:35.000000 rbfly-0.6.2/rbfly/_buffer.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1435 2023-01-16 12:48:43.000000 rbfly-0.6.2/rbfly/_buffer.pxd
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1898 2023-01-30 12:32:49.000000 rbfly-0.6.2/rbfly/_buffer.pyx
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   127039 2023-05-12 15:51:35.000000 rbfly-0.6.2/rbfly/_codec.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1098 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/_codec.h
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1185 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/_codec.pxd
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2298 2023-01-12 14:54:58.000000 rbfly-0.6.2/rbfly/_codec.pyx
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.422623 rbfly-0.6.2/rbfly/amqp/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      956 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/amqp/__init__.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   496385 2023-05-12 15:51:36.000000 rbfly-0.6.2/rbfly/amqp/_message.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1412 2023-01-17 19:10:28.000000 rbfly-0.6.2/rbfly/amqp/_message.pxd
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1437 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/amqp/_message.pyi
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    19793 2023-01-30 23:02:18.000000 rbfly-0.6.2/rbfly/amqp/_message.pyx
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3894 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/cm.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1335 2023-01-30 14:42:53.000000 rbfly-0.6.2/rbfly/error.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)        0 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/py.typed
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.425956 rbfly-0.6.2/rbfly/streams/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1471 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/__init__.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   775470 2023-05-12 15:51:35.000000 rbfly-0.6.2/rbfly/streams/_client.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1697 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/_client.pyi
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    11251 2023-03-18 23:13:07.000000 rbfly-0.6.2/rbfly/streams/_client.pyx
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   499620 2023-05-12 15:51:36.000000 rbfly-0.6.2/rbfly/streams/_codec.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1600 2023-01-30 21:09:01.000000 rbfly-0.6.2/rbfly/streams/_codec.pyi
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    12624 2023-03-18 23:24:25.000000 rbfly-0.6.2/rbfly/streams/_codec.pyx
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)   309908 2023-05-12 15:51:35.000000 rbfly-0.6.2/rbfly/streams/_mqueue.c
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1244 2023-02-01 18:34:41.000000 rbfly-0.6.2/rbfly/streams/_mqueue.pyi
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3933 2023-02-21 20:27:20.000000 rbfly-0.6.2/rbfly/streams/_mqueue.pyx
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    18029 2023-05-12 16:31:57.000000 rbfly-0.6.2/rbfly/streams/client.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     8690 2023-01-18 14:02:15.000000 rbfly-0.6.2/rbfly/streams/codec.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1894 2023-02-01 15:06:50.000000 rbfly-0.6.2/rbfly/streams/const.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1103 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/error.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     5229 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/offset.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    29310 2023-02-22 08:28:18.000000 rbfly-0.6.2/rbfly/streams/protocol.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1075 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/types.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     4004 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/streams/util.py
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.425956 rbfly-0.6.2/rbfly/tests/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/tests/__init__.py
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.425956 rbfly-0.6.2/rbfly/tests/amqp/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/tests/amqp/__init__.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     9581 2023-01-30 23:07:03.000000 rbfly-0.6.2/rbfly/tests/amqp/test_message.py
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.425956 rbfly-0.6.2/rbfly/tests/streams/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      790 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/tests/streams/__init__.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    11617 2023-05-12 16:29:31.000000 rbfly-0.6.2/rbfly/tests/streams/test_client.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)    13192 2023-03-18 23:21:44.000000 rbfly-0.6.2/rbfly/tests/streams/test_codec.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2271 2023-02-01 15:02:22.000000 rbfly-0.6.2/rbfly/tests/streams/test_mqueue.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1344 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/tests/streams/test_offset.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     3228 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/tests/test_util.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1826 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/types.py
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     2008 2023-01-11 23:13:37.000000 rbfly-0.6.2/rbfly/util.py
+drwxr-xr-x   0 wrobell   (1000) wrobell   (1000)        0 2023-05-12 22:32:40.422623 rbfly-0.6.2/rbfly.egg-info/
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1417 2023-05-12 22:32:40.000000 rbfly-0.6.2/rbfly.egg-info/PKG-INFO
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1235 2023-05-12 22:32:40.000000 rbfly-0.6.2/rbfly.egg-info/SOURCES.txt
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)        1 2023-05-12 22:32:40.000000 rbfly-0.6.2/rbfly.egg-info/dependency_links.txt
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)      157 2023-05-12 22:32:40.000000 rbfly-0.6.2/rbfly.egg-info/requires.txt
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)        6 2023-05-12 22:32:40.000000 rbfly-0.6.2/rbfly.egg-info/top_level.txt
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1326 2023-05-12 22:32:40.429289 rbfly-0.6.2/setup.cfg
+-rw-r--r--   0 wrobell   (1000) wrobell   (1000)     1633 2023-01-14 12:57:42.000000 rbfly-0.6.2/setup.py
```

### Comparing `rbfly-0.6.1/COPYING` & `rbfly-0.6.2/COPYING`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/PKG-INFO` & `rbfly-0.6.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rbfly
-Version: 0.6.1
+Version: 0.6.2
 Summary: RbFly - a library for RabbitMQ Streams using Python asyncio
 Home-page: https://wrobell.dcmod.org/rbfly/
 Author: Artur Wroblewski
 Author-email: wrobell@riseup.net
 License: GPLv3+
 Project-URL: Source Code, https://gitlab.com/wrobell/rbfly
 Project-URL: Bug tracker, https://gitlab.com/wrobell/rbfly/issues
```

### Comparing `rbfly-0.6.1/README` & `rbfly-0.6.2/README`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/__init__.py` & `rbfly-0.6.2/rbfly/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/_buffer.c` & `rbfly-0.6.2/rbfly/_buffer.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [],
         "name": "rbfly._buffer",
         "sources": [
@@ -18,16 +18,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -212,15 +212,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -251,15 +251,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
@@ -2505,28 +2505,28 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_COMPILING_IN_PYPY
-        PyObject *tmp_type, *tmp_value, *tmp_tb;
-        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
-        Py_INCREF(tb);
-        PyErr_Restore(tmp_type, tmp_value, tb);
-        Py_XDECREF(tmp_tb);
-#else
+#if CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
+#else
+        PyObject *tmp_type, *tmp_value, *tmp_tb;
+        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
+        Py_INCREF(tb);
+        PyErr_Restore(tmp_type, tmp_value, tb);
+        Py_XDECREF(tmp_tb);
 #endif
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
```

### Comparing `rbfly-0.6.1/rbfly/_buffer.pxd` & `rbfly-0.6.2/rbfly/_buffer.pxd`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/_buffer.pyx` & `rbfly-0.6.2/rbfly/_buffer.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/_codec.c` & `rbfly-0.6.2/rbfly/_codec.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [
             "rbfly/_codec.h"
         ],
@@ -23,16 +23,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -217,15 +217,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -256,15 +256,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
```

### Comparing `rbfly-0.6.1/rbfly/_codec.h` & `rbfly-0.6.2/rbfly/_codec.h`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/_codec.pxd` & `rbfly-0.6.2/rbfly/_codec.pxd`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/_codec.pyx` & `rbfly-0.6.2/rbfly/_codec.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/amqp/__init__.py` & `rbfly-0.6.2/rbfly/amqp/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/amqp/_message.c` & `rbfly-0.6.2/rbfly/amqp/_message.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [],
         "name": "rbfly.amqp._message",
         "sources": [
@@ -18,16 +18,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -212,15 +212,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -251,15 +251,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
@@ -966,17 +966,17 @@
 static const char *__pyx_filename;
 
 
 static const char *__pyx_f[] = {
   "stringsource",
   "rbfly/amqp/_message.pyx",
   "rbfly/amqp/_message.pxd",
-  "type.pxd",
-  "bool.pxd",
-  "complex.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/type.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/bool.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/complex.pxd",
 };
 
 /*--- Type declarations ---*/
 struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx;
 struct __pyx_t_5rbfly_7_buffer_Buffer;
 
 /* "_buffer.pxd":35
@@ -1396,20 +1396,28 @@
 
 /* SetupReduce.proto */
 static int __Pyx_setup_reduce(PyObject* type_obj);
 
 /* TypeImport.proto */
 #ifndef __PYX_HAVE_RT_ImportType_proto
 #define __PYX_HAVE_RT_ImportType_proto
+#if __STDC_VERSION__ >= 201112L
+#include <stdalign.h>
+#endif
+#if __STDC_VERSION__ >= 201112L || __cplusplus >= 201103L
+#define __PYX_GET_STRUCT_ALIGNMENT(s) alignof(s)
+#else
+#define __PYX_GET_STRUCT_ALIGNMENT(s) sizeof(void*)
+#endif
 enum __Pyx_ImportType_CheckSize {
    __Pyx_ImportType_CheckSize_Error = 0,
    __Pyx_ImportType_CheckSize_Warn = 1,
    __Pyx_ImportType_CheckSize_Ignore = 2
 };
-static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, enum __Pyx_ImportType_CheckSize check_size);
+static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size);
 #endif
 
 /* Import.proto */
 static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level);
 
 /* ImportFrom.proto */
 static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name);
@@ -7993,29 +8001,31 @@
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__Pyx_modinit_type_import_code", 0);
   /*--- Type import code ---*/
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(3, 9, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   __pyx_ptype_7cpython_4type_type = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "type", 
   #if defined(PYPY_VERSION_NUM) && PYPY_VERSION_NUM < 0x050B0000
-  sizeof(PyTypeObject),
+  sizeof(PyTypeObject), __PYX_GET_STRUCT_ALIGNMENT(PyTypeObject),
   #else
-  sizeof(PyHeapTypeObject),
+  sizeof(PyHeapTypeObject), __PYX_GET_STRUCT_ALIGNMENT(PyHeapTypeObject),
   #endif
   __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_4type_type) __PYX_ERR(3, 9, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(4, 8, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_7cpython_4bool_bool = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "bool", sizeof(PyBoolObject), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_7cpython_4bool_bool = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "bool", sizeof(PyBoolObject), __PYX_GET_STRUCT_ALIGNMENT(PyBoolObject),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_4bool_bool) __PYX_ERR(4, 8, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(5, 15, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_7cpython_7complex_complex = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "complex", sizeof(PyComplexObject), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_7cpython_7complex_complex = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "complex", sizeof(PyComplexObject), __PYX_GET_STRUCT_ALIGNMENT(PyComplexObject),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_7complex_complex) __PYX_ERR(5, 15, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __Pyx_RefNannyFinishContext();
   return 0;
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
   __Pyx_RefNannyFinishContext();
@@ -9139,28 +9149,28 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_COMPILING_IN_PYPY
-        PyObject *tmp_type, *tmp_value, *tmp_tb;
-        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
-        Py_INCREF(tb);
-        PyErr_Restore(tmp_type, tmp_value, tb);
-        Py_XDECREF(tmp_tb);
-#else
+#if CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
+#else
+        PyObject *tmp_type, *tmp_value, *tmp_tb;
+        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
+        Py_INCREF(tb);
+        PyErr_Restore(tmp_type, tmp_value, tb);
+        Py_XDECREF(tmp_tb);
 #endif
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
@@ -9972,44 +9982,62 @@
     return ret;
 }
 
 /* TypeImport */
 #ifndef __PYX_HAVE_RT_ImportType
 #define __PYX_HAVE_RT_ImportType
 static PyTypeObject *__Pyx_ImportType(PyObject *module, const char *module_name, const char *class_name,
-    size_t size, enum __Pyx_ImportType_CheckSize check_size)
+    size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size)
 {
     PyObject *result = 0;
     char warning[200];
     Py_ssize_t basicsize;
+    Py_ssize_t itemsize;
 #ifdef Py_LIMITED_API
     PyObject *py_basicsize;
+    PyObject *py_itemsize;
 #endif
     result = PyObject_GetAttrString(module, class_name);
     if (!result)
         goto bad;
     if (!PyType_Check(result)) {
         PyErr_Format(PyExc_TypeError,
             "%.200s.%.200s is not a type object",
             module_name, class_name);
         goto bad;
     }
 #ifndef Py_LIMITED_API
     basicsize = ((PyTypeObject *)result)->tp_basicsize;
+    itemsize = ((PyTypeObject *)result)->tp_itemsize;
 #else
     py_basicsize = PyObject_GetAttrString(result, "__basicsize__");
     if (!py_basicsize)
         goto bad;
     basicsize = PyLong_AsSsize_t(py_basicsize);
     Py_DECREF(py_basicsize);
     py_basicsize = 0;
     if (basicsize == (Py_ssize_t)-1 && PyErr_Occurred())
         goto bad;
+    py_itemsize = PyObject_GetAttrString(result, "__itemsize__");
+    if (!py_itemsize)
+        goto bad;
+    itemsize = PyLong_AsSsize_t(py_itemsize);
+    Py_DECREF(py_itemsize);
+    py_itemsize = 0;
+    if (itemsize == (Py_ssize_t)-1 && PyErr_Occurred())
+        goto bad;
 #endif
-    if ((size_t)basicsize < size) {
+    if (itemsize) {
+        if (size % alignment) {
+            alignment = size % alignment;
+        }
+        if (itemsize < (Py_ssize_t)alignment)
+            itemsize = (Py_ssize_t)alignment;
+    }
+    if ((size_t)(basicsize + itemsize) < size) {
         PyErr_Format(PyExc_ValueError,
             "%.200s.%.200s size changed, may indicate binary incompatibility. "
             "Expected %zd from C header, got %zd from PyObject",
             module_name, class_name, size, basicsize);
         goto bad;
     }
     if (check_size == __Pyx_ImportType_CheckSize_Error && (size_t)basicsize != size) {
```

### Comparing `rbfly-0.6.1/rbfly/amqp/_message.pxd` & `rbfly-0.6.2/rbfly/amqp/_message.pxd`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/amqp/_message.pyi` & `rbfly-0.6.2/rbfly/amqp/_message.pyi`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/amqp/_message.pyx` & `rbfly-0.6.2/rbfly/amqp/_message.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/cm.py` & `rbfly-0.6.2/rbfly/cm.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/error.py` & `rbfly-0.6.2/rbfly/error.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/__init__.py` & `rbfly-0.6.2/rbfly/streams/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_client.c` & `rbfly-0.6.2/rbfly/streams/_client.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [],
         "name": "rbfly.streams._client",
         "sources": [
@@ -18,16 +18,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -212,15 +212,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -251,15 +251,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
@@ -1902,20 +1902,28 @@
 
 /* SetupReduce.proto */
 static int __Pyx_setup_reduce(PyObject* type_obj);
 
 /* TypeImport.proto */
 #ifndef __PYX_HAVE_RT_ImportType_proto
 #define __PYX_HAVE_RT_ImportType_proto
+#if __STDC_VERSION__ >= 201112L
+#include <stdalign.h>
+#endif
+#if __STDC_VERSION__ >= 201112L || __cplusplus >= 201103L
+#define __PYX_GET_STRUCT_ALIGNMENT(s) alignof(s)
+#else
+#define __PYX_GET_STRUCT_ALIGNMENT(s) sizeof(void*)
+#endif
 enum __Pyx_ImportType_CheckSize {
    __Pyx_ImportType_CheckSize_Error = 0,
    __Pyx_ImportType_CheckSize_Warn = 1,
    __Pyx_ImportType_CheckSize_Ignore = 2
 };
-static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, enum __Pyx_ImportType_CheckSize check_size);
+static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size);
 #endif
 
 /* PatchInspect.proto */
 static PyObject* __Pyx_patch_inspect(PyObject* module);
 
 /* PatchAsyncIO.proto */
 static PyObject* __Pyx_patch_asyncio(PyObject* module);
@@ -11424,15 +11432,16 @@
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__Pyx_modinit_type_import_code", 0);
   /*--- Type import code ---*/
   __pyx_t_1 = PyImport_ImportModule("rbfly.amqp._message"); if (unlikely(!__pyx_t_1)) __PYX_ERR(2, 22, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_5rbfly_4amqp_8_message_MessageCtx = __Pyx_ImportType(__pyx_t_1, "rbfly.amqp._message", "MessageCtx", sizeof(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_5rbfly_4amqp_8_message_MessageCtx = __Pyx_ImportType(__pyx_t_1, "rbfly.amqp._message", "MessageCtx", sizeof(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx), __PYX_GET_STRUCT_ALIGNMENT(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_5rbfly_4amqp_8_message_MessageCtx) __PYX_ERR(2, 22, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __Pyx_RefNannyFinishContext();
   return 0;
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
   __Pyx_RefNannyFinishContext();
@@ -13007,28 +13016,28 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_COMPILING_IN_PYPY
-        PyObject *tmp_type, *tmp_value, *tmp_tb;
-        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
-        Py_INCREF(tb);
-        PyErr_Restore(tmp_type, tmp_value, tb);
-        Py_XDECREF(tmp_tb);
-#else
+#if CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
+#else
+        PyObject *tmp_type, *tmp_value, *tmp_tb;
+        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
+        Py_INCREF(tb);
+        PyErr_Restore(tmp_type, tmp_value, tb);
+        Py_XDECREF(tmp_tb);
 #endif
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
@@ -14498,15 +14507,19 @@
 #endif
 #if PY_VERSION_HEX >= 0x030500B2 || defined(PyCoro_CheckExact)
     if (PyCoro_CheckExact(obj)) {
         return __Pyx_NewRef(obj);
     } else
 #endif
 #if CYTHON_COMPILING_IN_CPYTHON && defined(CO_ITERABLE_COROUTINE)
+#if PY_VERSION_HEX >= 0x030C00A6
+    if (PyGen_CheckExact(obj) && (PyGen_GetCode(obj)->co_flags & CO_ITERABLE_COROUTINE)) {
+#else
     if (PyGen_CheckExact(obj) && ((PyGenObject*)obj)->gi_code && ((PyCodeObject *)((PyGenObject*)obj)->gi_code)->co_flags & CO_ITERABLE_COROUTINE) {
+#endif
         return __Pyx_NewRef(obj);
     } else
 #endif
     {
         PyObject *method = NULL;
         int is_method = __Pyx_PyObject_GetMethod(obj, __pyx_n_s_await, &method);
         if (likely(is_method)) {
@@ -14548,15 +14561,15 @@
                  "object %.100s can't be used in 'await' expression",
                  Py_TYPE(obj)->tp_name);
 bad:
     return NULL;
 }
 
 /* CoroutineYieldFrom */
-static PyObject* __Pyx__Coroutine_Yield_From_Generic(__pyx_CoroutineObject *gen, PyObject *source) {
+  static PyObject* __Pyx__Coroutine_Yield_From_Generic(__pyx_CoroutineObject *gen, PyObject *source) {
     PyObject *retval;
     PyObject *source_gen = __Pyx__Coroutine_GetAwaitableIter(source);
     if (unlikely(!source_gen)) {
         return NULL;
     }
     if (__Pyx_Coroutine_Check(source_gen)) {
         retval = __Pyx_Generator_Next(source_gen);
@@ -14595,15 +14608,15 @@
         Py_INCREF(source);
         gen->yieldfrom = source;
     }
     return retval;
 }
 
 /* GetException */
-#if CYTHON_FAST_THREAD_STATE
+  #if CYTHON_FAST_THREAD_STATE
 static int __Pyx__GetException(PyThreadState *tstate, PyObject **type, PyObject **value, PyObject **tb)
 #else
 static int __Pyx_GetException(PyObject **type, PyObject **value, PyObject **tb)
 #endif
 {
     PyObject *local_type, *local_value, *local_tb;
 #if CYTHON_FAST_THREAD_STATE
@@ -14669,15 +14682,15 @@
     Py_XDECREF(local_type);
     Py_XDECREF(local_value);
     Py_XDECREF(local_tb);
     return -1;
 }
 
 /* FastTypeChecks */
-#if CYTHON_COMPILING_IN_CPYTHON
+  #if CYTHON_COMPILING_IN_CPYTHON
 static int __Pyx_InBases(PyTypeObject *a, PyTypeObject *b) {
     while (a) {
         a = a->tp_base;
         if (a == b)
             return 1;
     }
     return b == &PyBaseObject_Type;
@@ -14769,15 +14782,15 @@
         return __Pyx_inner_PyErr_GivenExceptionMatches2(err, exc_type1, exc_type2);
     }
     return (PyErr_GivenExceptionMatches(err, exc_type1) || PyErr_GivenExceptionMatches(err, exc_type2));
 }
 #endif
 
 /* ReturnWithStopIteration */
-static void __Pyx__ReturnWithStopIteration(PyObject* value) {
+  static void __Pyx__ReturnWithStopIteration(PyObject* value) {
     PyObject *exc, *args;
 #if CYTHON_COMPILING_IN_CPYTHON || CYTHON_COMPILING_IN_PYSTON
     __Pyx_PyThreadState_declare
     if ((PY_VERSION_HEX >= 0x03030000 && PY_VERSION_HEX < 0x030500B1)
             || unlikely(PyTuple_Check(value) || PyExceptionInstance_Check(value))) {
         args = PyTuple_New(1);
         if (unlikely(!args)) return;
@@ -14811,29 +14824,29 @@
     if (unlikely(!exc)) return;
 #endif
     PyErr_SetObject(PyExc_StopIteration, exc);
     Py_DECREF(exc);
 }
 
 /* PyObjectSetAttrStr */
-#if CYTHON_USE_TYPE_SLOTS
+  #if CYTHON_USE_TYPE_SLOTS
 static CYTHON_INLINE int __Pyx_PyObject_SetAttrStr(PyObject* obj, PyObject* attr_name, PyObject* value) {
     PyTypeObject* tp = Py_TYPE(obj);
     if (likely(tp->tp_setattro))
         return tp->tp_setattro(obj, attr_name, value);
 #if PY_MAJOR_VERSION < 3
     if (likely(tp->tp_setattr))
         return tp->tp_setattr(obj, PyString_AS_STRING(attr_name), value);
 #endif
     return PyObject_SetAttr(obj, attr_name, value);
 }
 #endif
 
 /* PyErrExceptionMatches */
-#if CYTHON_FAST_THREAD_STATE
+  #if CYTHON_FAST_THREAD_STATE
 static int __Pyx_PyErr_ExceptionMatchesTuple(PyObject *exc_type, PyObject *tuple) {
     Py_ssize_t i, n;
     n = PyTuple_GET_SIZE(tuple);
 #if PY_MAJOR_VERSION >= 3
     for (i=0; i<n; i++) {
         if (exc_type == PyTuple_GET_ITEM(tuple, i)) return 1;
     }
@@ -14850,61 +14863,61 @@
     if (unlikely(PyTuple_Check(err)))
         return __Pyx_PyErr_ExceptionMatchesTuple(exc_type, err);
     return __Pyx_PyErr_GivenExceptionMatches(exc_type, err);
 }
 #endif
 
 /* GetAttr */
-static CYTHON_INLINE PyObject *__Pyx_GetAttr(PyObject *o, PyObject *n) {
+  static CYTHON_INLINE PyObject *__Pyx_GetAttr(PyObject *o, PyObject *n) {
 #if CYTHON_USE_TYPE_SLOTS
 #if PY_MAJOR_VERSION >= 3
     if (likely(PyUnicode_Check(n)))
 #else
     if (likely(PyString_Check(n)))
 #endif
         return __Pyx_PyObject_GetAttrStr(o, n);
 #endif
     return PyObject_GetAttr(o, n);
 }
 
 /* GetAttr3 */
-static PyObject *__Pyx_GetAttr3Default(PyObject *d) {
+  static PyObject *__Pyx_GetAttr3Default(PyObject *d) {
     __Pyx_PyThreadState_declare
     __Pyx_PyThreadState_assign
     if (unlikely(!__Pyx_PyErr_ExceptionMatches(PyExc_AttributeError)))
         return NULL;
     __Pyx_PyErr_Clear();
     Py_INCREF(d);
     return d;
 }
 static CYTHON_INLINE PyObject *__Pyx_GetAttr3(PyObject *o, PyObject *n, PyObject *d) {
     PyObject *r = __Pyx_GetAttr(o, n);
     return (likely(r)) ? r : __Pyx_GetAttr3Default(d);
 }
 
 /* append */
-static CYTHON_INLINE int __Pyx_PyObject_Append(PyObject* L, PyObject* x) {
+  static CYTHON_INLINE int __Pyx_PyObject_Append(PyObject* L, PyObject* x) {
     if (likely(PyList_CheckExact(L))) {
         if (unlikely(__Pyx_PyList_Append(L, x) < 0)) return -1;
     } else {
         PyObject* retval = __Pyx_PyObject_CallMethod1(L, __pyx_n_s_append, x);
         if (unlikely(!retval))
             return -1;
         Py_DECREF(retval);
     }
     return 0;
 }
 
 /* None */
-static CYTHON_INLINE void __Pyx_RaiseClosureNameError(const char *varname) {
+  static CYTHON_INLINE void __Pyx_RaiseClosureNameError(const char *varname) {
     PyErr_Format(PyExc_NameError, "free variable '%s' referenced before assignment in enclosing scope", varname);
 }
 
 /* SliceObject */
-static CYTHON_INLINE int __Pyx_PyObject_SetSlice(PyObject* obj, PyObject* value,
+  static CYTHON_INLINE int __Pyx_PyObject_SetSlice(PyObject* obj, PyObject* value,
         Py_ssize_t cstart, Py_ssize_t cstop,
         PyObject** _py_start, PyObject** _py_stop, PyObject** _py_slice,
         int has_cstart, int has_cstop, CYTHON_UNUSED int wraparound) {
 #if CYTHON_USE_TYPE_SLOTS
     PyMappingMethods* mp;
 #if PY_MAJOR_VERSION < 3
     PySequenceMethods* ms = Py_TYPE(obj)->tp_as_sequence;
@@ -14994,26 +15007,26 @@
         "'%.200s' object does not support slice %.10s",
         Py_TYPE(obj)->tp_name, value ? "assignment" : "deletion");
 bad:
     return -1;
 }
 
 /* RaiseKeywordRequired */
-static void __Pyx_RaiseKeywordRequired(const char* func_name, PyObject* kw_name) {
+  static void __Pyx_RaiseKeywordRequired(const char* func_name, PyObject* kw_name) {
     PyErr_Format(PyExc_TypeError,
         #if PY_MAJOR_VERSION >= 3
         "%s() needs keyword-only argument %U", func_name, kw_name);
         #else
         "%s() needs keyword-only argument %s", func_name,
         PyString_AS_STRING(kw_name));
         #endif
 }
 
 /* CythonFunctionShared */
-#include <structmember.h>
+  #include <structmember.h>
 static PyObject *
 __Pyx_CyFunction_get_doc(__pyx_CyFunctionObject *op, CYTHON_UNUSED void *closure)
 {
     if (unlikely(op->func_doc == NULL)) {
         if (op->func.m_ml->ml_doc) {
 #if PY_MAJOR_VERSION >= 3
             op->func_doc = PyUnicode_FromString(op->func.m_ml->ml_doc);
@@ -15621,28 +15634,28 @@
 static CYTHON_INLINE void __Pyx_CyFunction_SetAnnotationsDict(PyObject *func, PyObject *dict) {
     __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *) func;
     m->func_annotations = dict;
     Py_INCREF(dict);
 }
 
 /* CythonFunction */
-static PyObject *__Pyx_CyFunction_New(PyMethodDef *ml, int flags, PyObject* qualname,
+  static PyObject *__Pyx_CyFunction_New(PyMethodDef *ml, int flags, PyObject* qualname,
                                       PyObject *closure, PyObject *module, PyObject* globals, PyObject* code) {
     PyObject *op = __Pyx_CyFunction_Init(
         PyObject_GC_New(__pyx_CyFunctionObject, __pyx_CyFunctionType),
         ml, flags, qualname, closure, module, globals, code
     );
     if (likely(op)) {
         PyObject_GC_Track(op);
     }
     return op;
 }
 
 /* StopAsyncIteration */
-#if PY_VERSION_HEX < 0x030500B1
+  #if PY_VERSION_HEX < 0x030500B1
 static PyTypeObject __Pyx__PyExc_StopAsyncIteration_type = {
     PyVarObject_HEAD_INIT(0, 0)
     "StopAsyncIteration",
     sizeof(PyBaseExceptionObject),
     0,
     0,
     0,
@@ -15718,15 +15731,15 @@
     if (builtins && unlikely(PyMapping_SetItemString(builtins, (char*) "StopAsyncIteration", __Pyx_PyExc_StopAsyncIteration) < 0))
         return -1;
 #endif
     return 0;
 }
 
 /* Import */
-static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level) {
+  static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level) {
     PyObject *empty_list = 0;
     PyObject *module = 0;
     PyObject *global_dict = 0;
     PyObject *empty_dict = 0;
     PyObject *list;
     #if PY_MAJOR_VERSION < 3
     PyObject *py_import;
@@ -15783,29 +15796,29 @@
     #endif
     Py_XDECREF(empty_list);
     Py_XDECREF(empty_dict);
     return module;
 }
 
 /* ImportFrom */
-static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name) {
+  static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name) {
     PyObject* value = __Pyx_PyObject_GetAttrStr(module, name);
     if (unlikely(!value) && PyErr_ExceptionMatches(PyExc_AttributeError)) {
         PyErr_Format(PyExc_ImportError,
         #if PY_MAJOR_VERSION < 3
             "cannot import name %.230s", PyString_AS_STRING(name));
         #else
             "cannot import name %S", name);
         #endif
     }
     return value;
 }
 
 /* HasAttr */
-static CYTHON_INLINE int __Pyx_HasAttr(PyObject *o, PyObject *n) {
+  static CYTHON_INLINE int __Pyx_HasAttr(PyObject *o, PyObject *n) {
     PyObject *r;
     if (unlikely(!__Pyx_PyBaseString_Check(n))) {
         PyErr_SetString(PyExc_TypeError,
                         "hasattr(): attribute name must be string");
         return -1;
     }
     r = __Pyx_GetAttr(o, n);
@@ -15815,25 +15828,25 @@
     } else {
         Py_DECREF(r);
         return 1;
     }
 }
 
 /* PyObject_GenericGetAttr */
-#if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
+  #if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
 static PyObject* __Pyx_PyObject_GenericGetAttr(PyObject* obj, PyObject* attr_name) {
     if (unlikely(Py_TYPE(obj)->tp_dictoffset)) {
         return PyObject_GenericGetAttr(obj, attr_name);
     }
     return __Pyx_PyObject_GenericGetAttrNoDict(obj, attr_name);
 }
 #endif
 
 /* SetVTable */
-static int __Pyx_SetVtable(PyObject *dict, void *vtable) {
+  static int __Pyx_SetVtable(PyObject *dict, void *vtable) {
 #if PY_VERSION_HEX >= 0x02070000
     PyObject *ob = PyCapsule_New(vtable, 0, 0);
 #else
     PyObject *ob = PyCObject_FromVoidPtr(vtable, 0);
 #endif
     if (!ob)
         goto bad;
@@ -15843,15 +15856,15 @@
     return 0;
 bad:
     Py_XDECREF(ob);
     return -1;
 }
 
 /* PyObjectGetAttrStrNoError */
-static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
+  static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
     __Pyx_PyThreadState_declare
     __Pyx_PyThreadState_assign
     if (likely(__Pyx_PyErr_ExceptionMatches(PyExc_AttributeError)))
         __Pyx_PyErr_Clear();
 }
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name) {
     PyObject *result;
@@ -15865,15 +15878,15 @@
     if (unlikely(!result)) {
         __Pyx_PyObject_GetAttrStr_ClearAttributeError();
     }
     return result;
 }
 
 /* SetupReduce */
-static int __Pyx_setup_reduce_is_named(PyObject* meth, PyObject* name) {
+  static int __Pyx_setup_reduce_is_named(PyObject* meth, PyObject* name) {
   int ret;
   PyObject *name_attr;
   name_attr = __Pyx_PyObject_GetAttrStr(meth, __pyx_n_s_name_2);
   if (likely(name_attr)) {
       ret = PyObject_RichCompareBool(name_attr, name, Py_EQ);
   } else {
       ret = -1;
@@ -15969,47 +15982,65 @@
     Py_XDECREF(reduce_cython);
     Py_XDECREF(setstate);
     Py_XDECREF(setstate_cython);
     return ret;
 }
 
 /* TypeImport */
-#ifndef __PYX_HAVE_RT_ImportType
+  #ifndef __PYX_HAVE_RT_ImportType
 #define __PYX_HAVE_RT_ImportType
 static PyTypeObject *__Pyx_ImportType(PyObject *module, const char *module_name, const char *class_name,
-    size_t size, enum __Pyx_ImportType_CheckSize check_size)
+    size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size)
 {
     PyObject *result = 0;
     char warning[200];
     Py_ssize_t basicsize;
+    Py_ssize_t itemsize;
 #ifdef Py_LIMITED_API
     PyObject *py_basicsize;
+    PyObject *py_itemsize;
 #endif
     result = PyObject_GetAttrString(module, class_name);
     if (!result)
         goto bad;
     if (!PyType_Check(result)) {
         PyErr_Format(PyExc_TypeError,
             "%.200s.%.200s is not a type object",
             module_name, class_name);
         goto bad;
     }
 #ifndef Py_LIMITED_API
     basicsize = ((PyTypeObject *)result)->tp_basicsize;
+    itemsize = ((PyTypeObject *)result)->tp_itemsize;
 #else
     py_basicsize = PyObject_GetAttrString(result, "__basicsize__");
     if (!py_basicsize)
         goto bad;
     basicsize = PyLong_AsSsize_t(py_basicsize);
     Py_DECREF(py_basicsize);
     py_basicsize = 0;
     if (basicsize == (Py_ssize_t)-1 && PyErr_Occurred())
         goto bad;
+    py_itemsize = PyObject_GetAttrString(result, "__itemsize__");
+    if (!py_itemsize)
+        goto bad;
+    itemsize = PyLong_AsSsize_t(py_itemsize);
+    Py_DECREF(py_itemsize);
+    py_itemsize = 0;
+    if (itemsize == (Py_ssize_t)-1 && PyErr_Occurred())
+        goto bad;
 #endif
-    if ((size_t)basicsize < size) {
+    if (itemsize) {
+        if (size % alignment) {
+            alignment = size % alignment;
+        }
+        if (itemsize < (Py_ssize_t)alignment)
+            itemsize = (Py_ssize_t)alignment;
+    }
+    if ((size_t)(basicsize + itemsize) < size) {
         PyErr_Format(PyExc_ValueError,
             "%.200s.%.200s size changed, may indicate binary incompatibility. "
             "Expected %zd from C header, got %zd from PyObject",
             module_name, class_name, size, basicsize);
         goto bad;
     }
     if (check_size == __Pyx_ImportType_CheckSize_Error && (size_t)basicsize != size) {
@@ -16030,15 +16061,15 @@
 bad:
     Py_XDECREF(result);
     return NULL;
 }
 #endif
 
 /* PatchInspect */
-static PyObject* __Pyx_patch_inspect(PyObject* module) {
+  static PyObject* __Pyx_patch_inspect(PyObject* module) {
 #if defined(__Pyx_Generator_USED) && (!defined(CYTHON_PATCH_INSPECT) || CYTHON_PATCH_INSPECT)
     static int inspect_patched = 0;
     if (unlikely((!inspect_patched) && module)) {
         module = __Pyx_Coroutine_patch_module(
             module, ""
 "old_types = getattr(_module.isgenerator, '_cython_generator_types', None)\n"
 "if old_types is None or not isinstance(old_types, set):\n"
@@ -16055,15 +16086,15 @@
 #else
     if ((0)) return __Pyx_Coroutine_patch_module(module, NULL);
 #endif
     return module;
 }
 
 /* PatchAsyncIO */
-static PyObject* __Pyx_patch_asyncio(PyObject* module) {
+  static PyObject* __Pyx_patch_asyncio(PyObject* module) {
 #if PY_VERSION_HEX < 0x030500B2 &&\
         (defined(__Pyx_Coroutine_USED) || defined(__Pyx_Generator_USED)) &&\
         (!defined(CYTHON_PATCH_ASYNCIO) || CYTHON_PATCH_ASYNCIO)
     PyObject *patch_module = NULL;
     static int asyncio_patched = 0;
     if (unlikely((!asyncio_patched) && module)) {
         PyObject *package;
@@ -16138,15 +16169,15 @@
 #else
     if ((0)) return __Pyx_patch_inspect(__Pyx_Coroutine_patch_module(module, NULL));
 #endif
     return module;
 }
 
 /* CalculateMetaclass */
-static PyObject *__Pyx_CalculateMetaclass(PyTypeObject *metaclass, PyObject *bases) {
+  static PyObject *__Pyx_CalculateMetaclass(PyTypeObject *metaclass, PyObject *bases) {
     Py_ssize_t i, nbases = PyTuple_GET_SIZE(bases);
     for (i=0; i < nbases; i++) {
         PyTypeObject *tmptype;
         PyObject *tmp = PyTuple_GET_ITEM(bases, i);
         tmptype = Py_TYPE(tmp);
 #if PY_MAJOR_VERSION < 3
         if (tmptype == &PyClass_Type)
@@ -16177,15 +16208,15 @@
 #endif
     }
     Py_INCREF((PyObject*) metaclass);
     return (PyObject*) metaclass;
 }
 
 /* Py3ClassCreate */
-static PyObject *__Pyx_Py3MetaclassPrepare(PyObject *metaclass, PyObject *bases, PyObject *name,
+  static PyObject *__Pyx_Py3MetaclassPrepare(PyObject *metaclass, PyObject *bases, PyObject *name,
                                            PyObject *qualname, PyObject *mkw, PyObject *modname, PyObject *doc) {
     PyObject *ns;
     if (metaclass) {
         PyObject *prep = __Pyx_PyObject_GetAttrStr(metaclass, __pyx_n_s_prepare);
         if (prep) {
             PyObject *pargs = PyTuple_Pack(2, name, bases);
             if (unlikely(!pargs)) {
@@ -16244,15 +16275,15 @@
         Py_DECREF(margs);
     }
     Py_XDECREF(owned_metaclass);
     return result;
 }
 
 /* CyFunctionClassCell */
-static int __Pyx_CyFunction_InitClassCell(PyObject *cyfunctions, PyObject *classobj) {
+  static int __Pyx_CyFunction_InitClassCell(PyObject *cyfunctions, PyObject *classobj) {
     Py_ssize_t i, count = PyList_GET_SIZE(cyfunctions);
     for (i = 0; i < count; i++) {
         __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *)
 #if CYTHON_ASSUME_SAFE_MACROS && !CYTHON_AVOID_BORROWED_REFS
             PyList_GET_ITEM(cyfunctions, i);
 #else
             PySequence_ITEM(cyfunctions, i);
@@ -16265,15 +16296,15 @@
         Py_DECREF((PyObject*)m);
 #endif
     }
     return 0;
 }
 
 /* GetItemInt */
-static PyObject *__Pyx_GetItemInt_Generic(PyObject *o, PyObject* j) {
+  static PyObject *__Pyx_GetItemInt_Generic(PyObject *o, PyObject* j) {
     PyObject *r;
     if (!j) return NULL;
     r = PyObject_GetItem(o, j);
     Py_DECREF(j);
     return r;
 }
 static CYTHON_INLINE PyObject *__Pyx_GetItemInt_List_Fast(PyObject *o, Py_ssize_t i,
@@ -16352,15 +16383,15 @@
         return PySequence_GetItem(o, i);
     }
 #endif
     return __Pyx_GetItemInt_Generic(o, PyInt_FromSsize_t(i));
 }
 
 /* ObjectGetItem */
-#if CYTHON_USE_TYPE_SLOTS
+  #if CYTHON_USE_TYPE_SLOTS
 static PyObject *__Pyx_PyObject_GetIndex(PyObject *obj, PyObject* index) {
     PyObject *runerr = NULL;
     Py_ssize_t key_value;
     PySequenceMethods *m = Py_TYPE(obj)->tp_as_sequence;
     if (unlikely(!(m && m->sq_item))) {
         PyErr_Format(PyExc_TypeError, "'%.200s' object is not subscriptable", Py_TYPE(obj)->tp_name);
         return NULL;
@@ -16381,15 +16412,15 @@
         return m->mp_subscript(obj, key);
     }
     return __Pyx_PyObject_GetIndex(obj, key);
 }
 #endif
 
 /* CLineInTraceback */
-#ifndef CYTHON_CLINE_IN_TRACEBACK
+  #ifndef CYTHON_CLINE_IN_TRACEBACK
 static int __Pyx_CLineForTraceback(CYTHON_UNUSED PyThreadState *tstate, int c_line) {
     PyObject *use_cline;
     PyObject *ptype, *pvalue, *ptraceback;
 #if CYTHON_COMPILING_IN_CPYTHON
     PyObject **cython_runtime_dict;
 #endif
     if (unlikely(!__pyx_cython_runtime)) {
@@ -16423,15 +16454,15 @@
     }
     __Pyx_ErrRestoreInState(tstate, ptype, pvalue, ptraceback);
     return c_line;
 }
 #endif
 
 /* CodeObjectCache */
-static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line) {
+  static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line) {
     int start = 0, mid = 0, end = count - 1;
     if (end >= 0 && code_line > entries[end].code_line) {
         return count;
     }
     while (start < end) {
         mid = start + (end - start) / 2;
         if (code_line < entries[mid].code_line) {
@@ -16503,15 +16534,15 @@
     entries[pos].code_line = code_line;
     entries[pos].code_object = code_object;
     __pyx_code_cache.count++;
     Py_INCREF(code_object);
 }
 
 /* AddTraceback */
-#include "compile.h"
+  #include "compile.h"
 #include "frameobject.h"
 #include "traceback.h"
 #if PY_VERSION_HEX >= 0x030b00a6
   #ifndef Py_BUILD_CORE
     #define Py_BUILD_CORE 1
   #endif
   #include "internal/pycore_frame.h"
@@ -16610,15 +16641,15 @@
     PyTraceBack_Here(py_frame);
 bad:
     Py_XDECREF(py_code);
     Py_XDECREF(py_frame);
 }
 
 /* CIntFromPyVerify */
-#define __PYX_VERIFY_RETURN_INT(target_type, func_type, func_value)\
+  #define __PYX_VERIFY_RETURN_INT(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 0)
 #define __PYX_VERIFY_RETURN_INT_EXC(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 1)
 #define __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, exc)\
     {\
         func_type value = func_value;\
         if (sizeof(target_type) < sizeof(func_type)) {\
@@ -16632,15 +16663,15 @@
                     goto raise_overflow;\
             }\
         }\
         return (target_type) value;\
     }
 
 /* CIntFromPy */
-static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *x) {
+  static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const int neg_one = (int) -1, const_zero = (int) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -16828,15 +16859,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to int");
     return (int) -1;
 }
 
 /* CIntFromPy */
-static CYTHON_INLINE uint64_t __Pyx_PyInt_As_uint64_t(PyObject *x) {
+  static CYTHON_INLINE uint64_t __Pyx_PyInt_As_uint64_t(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const uint64_t neg_one = (uint64_t) -1, const_zero = (uint64_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -17024,15 +17055,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to uint64_t");
     return (uint64_t) -1;
 }
 
 /* CIntFromPy */
-static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *x) {
+  static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const long neg_one = (long) -1, const_zero = (long) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -17220,15 +17251,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to long");
     return (long) -1;
 }
 
 /* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_uint64_t(uint64_t value) {
+  static CYTHON_INLINE PyObject* __Pyx_PyInt_From_uint64_t(uint64_t value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const uint64_t neg_one = (uint64_t) -1, const_zero = (uint64_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -17258,15 +17289,15 @@
         unsigned char *bytes = (unsigned char *)&value;
         return _PyLong_FromByteArray(bytes, sizeof(uint64_t),
                                      little, !is_unsigned);
     }
 }
 
 /* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_int(int value) {
+  static CYTHON_INLINE PyObject* __Pyx_PyInt_From_int(int value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const int neg_one = (int) -1, const_zero = (int) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -17296,15 +17327,15 @@
         unsigned char *bytes = (unsigned char *)&value;
         return _PyLong_FromByteArray(bytes, sizeof(int),
                                      little, !is_unsigned);
     }
 }
 
 /* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
+  static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const long neg_one = (long) -1, const_zero = (long) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -17334,15 +17365,15 @@
         unsigned char *bytes = (unsigned char *)&value;
         return _PyLong_FromByteArray(bytes, sizeof(long),
                                      little, !is_unsigned);
     }
 }
 
 /* Generator */
-static PyMethodDef __pyx_Generator_methods[] = {
+  static PyMethodDef __pyx_Generator_methods[] = {
     {"send", (PyCFunction) __Pyx_Coroutine_Send, METH_O,
      (char*) PyDoc_STR("send(arg) -> send 'arg' into generator,\nreturn next yielded value or raise StopIteration.")},
     {"throw", (PyCFunction) __Pyx_Coroutine_Throw, METH_VARARGS,
      (char*) PyDoc_STR("throw(typ[,val[,tb]]) -> raise exception in generator,\nreturn next yielded value or raise StopIteration.")},
     {"close", (PyCFunction) __Pyx_Coroutine_Close_Method, METH_NOARGS,
      (char*) PyDoc_STR("close() -> raise GeneratorExit inside generator.")},
     {0, 0, 0, 0}
@@ -17437,15 +17468,15 @@
     if (unlikely(!__pyx_GeneratorType)) {
         return -1;
     }
     return 0;
 }
 
 /* AsyncGeneratorInitFinalizer */
-#if PY_VERSION_HEX < 0x030600B0
+  #if PY_VERSION_HEX < 0x030600B0
 static int __Pyx_async_gen_init_hooks(__pyx_PyAsyncGenObject *o) {
 #if 0
     PyThreadState *tstate;
     PyObject *finalizer;
     PyObject *firstiter;
 #endif
     if (likely(o->ag_hooks_inited)) {
@@ -17472,15 +17503,15 @@
     }
 #endif
     return 0;
 }
 #endif
 
 /* AsyncGenerator */
-PyDoc_STRVAR(__Pyx_async_gen_send_doc,
+  PyDoc_STRVAR(__Pyx_async_gen_send_doc,
 "send(arg) -> send 'arg' into generator,\n\
 return next yielded value or raise StopIteration.");
 PyDoc_STRVAR(__Pyx_async_gen_close_doc,
 "close() -> raise GeneratorExit inside generator.");
 PyDoc_STRVAR(__Pyx_async_gen_throw_doc,
 "throw(typ[,val[,tb]]) -> raise exception in generator,\n\
 return next yielded value or raise StopIteration.");
@@ -18304,18 +18335,18 @@
     __pyx__PyAsyncGenASendType = __Pyx_FetchCommonType(&__pyx__PyAsyncGenASendType_type);
     if (unlikely(!__pyx__PyAsyncGenASendType))
         return -1;
     return 0;
 }
 
 /* AsyncGen */
-
+  
 
 /* CheckBinaryVersion */
-static int __Pyx_check_binary_version(void) {
+  static int __Pyx_check_binary_version(void) {
     char ctversion[5];
     int same=1, i, found_dot;
     const char* rt_from_call = Py_GetVersion();
     PyOS_snprintf(ctversion, 5, "%d.%d", PY_MAJOR_VERSION, PY_MINOR_VERSION);
     found_dot = 0;
     for (i = 0; i < 4; i++) {
         if (!ctversion[i]) {
@@ -18345,15 +18376,15 @@
                       ctversion, __Pyx_MODULE_NAME, rtversion);
         return PyErr_WarnEx(NULL, message, 1);
     }
     return 0;
 }
 
 /* InitStrings */
-static int __Pyx_InitStrings(__Pyx_StringTabEntry *t) {
+  static int __Pyx_InitStrings(__Pyx_StringTabEntry *t) {
     while (t->p) {
         #if PY_MAJOR_VERSION < 3
         if (t->is_unicode) {
             *t->p = PyUnicode_DecodeUTF8(t->s, t->n - 1, NULL);
         } else if (t->intern) {
             *t->p = PyString_InternFromString(t->s);
         } else {
```

### Comparing `rbfly-0.6.1/rbfly/streams/_client.pyi` & `rbfly-0.6.2/rbfly/streams/_client.pyi`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_client.pyx` & `rbfly-0.6.2/rbfly/streams/_client.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_codec.c` & `rbfly-0.6.2/rbfly/streams/_codec.c`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [],
         "name": "rbfly.streams._codec",
         "sources": [
@@ -18,16 +18,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -212,15 +212,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -251,15 +251,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
@@ -965,18 +965,18 @@
 static const char * __pyx_cfilenm= __FILE__;
 static const char *__pyx_filename;
 
 
 static const char *__pyx_f[] = {
   "stringsource",
   "rbfly/streams/_codec.pyx",
-  "venv/lib/python3.10/site-packages/Cython/Includes/cpython/array.pxd",
-  "venv/lib/python3.10/site-packages/Cython/Includes/cpython/type.pxd",
-  "venv/lib/python3.10/site-packages/Cython/Includes/cpython/bool.pxd",
-  "venv/lib/python3.10/site-packages/Cython/Includes/cpython/complex.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/array.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/type.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/bool.pxd",
+  ".venv-3.11/lib/python3.11/site-packages/Cython/Includes/cpython/complex.pxd",
   "rbfly/amqp/_message.pxd",
 };
 
 /*--- Type declarations ---*/
 #ifndef _ARRAYARRAY_H
 struct arrayobject;
 typedef struct arrayobject arrayobject;
@@ -1438,20 +1438,28 @@
 
 /* SetupReduce.proto */
 static int __Pyx_setup_reduce(PyObject* type_obj);
 
 /* TypeImport.proto */
 #ifndef __PYX_HAVE_RT_ImportType_proto
 #define __PYX_HAVE_RT_ImportType_proto
+#if __STDC_VERSION__ >= 201112L
+#include <stdalign.h>
+#endif
+#if __STDC_VERSION__ >= 201112L || __cplusplus >= 201103L
+#define __PYX_GET_STRUCT_ALIGNMENT(s) alignof(s)
+#else
+#define __PYX_GET_STRUCT_ALIGNMENT(s) sizeof(void*)
+#endif
 enum __Pyx_ImportType_CheckSize {
    __Pyx_ImportType_CheckSize_Error = 0,
    __Pyx_ImportType_CheckSize_Warn = 1,
    __Pyx_ImportType_CheckSize_Ignore = 2
 };
-static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, enum __Pyx_ImportType_CheckSize check_size);
+static PyTypeObject *__Pyx_ImportType(PyObject* module, const char *module_name, const char *class_name, size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size);
 #endif
 
 /* Import.proto */
 static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level);
 
 /* ImportFrom.proto */
 static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name);
@@ -7154,39 +7162,43 @@
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__Pyx_modinit_type_import_code", 0);
   /*--- Type import code ---*/
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(3, 9, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   __pyx_ptype_7cpython_4type_type = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "type", 
   #if defined(PYPY_VERSION_NUM) && PYPY_VERSION_NUM < 0x050B0000
-  sizeof(PyTypeObject),
+  sizeof(PyTypeObject), __PYX_GET_STRUCT_ALIGNMENT(PyTypeObject),
   #else
-  sizeof(PyHeapTypeObject),
+  sizeof(PyHeapTypeObject), __PYX_GET_STRUCT_ALIGNMENT(PyHeapTypeObject),
   #endif
   __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_4type_type) __PYX_ERR(3, 9, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(4, 8, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_7cpython_4bool_bool = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "bool", sizeof(PyBoolObject), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_7cpython_4bool_bool = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "bool", sizeof(PyBoolObject), __PYX_GET_STRUCT_ALIGNMENT(PyBoolObject),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_4bool_bool) __PYX_ERR(4, 8, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_t_1)) __PYX_ERR(5, 15, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_7cpython_7complex_complex = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "complex", sizeof(PyComplexObject), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_7cpython_7complex_complex = __Pyx_ImportType(__pyx_t_1, __Pyx_BUILTIN_MODULE_NAME, "complex", sizeof(PyComplexObject), __PYX_GET_STRUCT_ALIGNMENT(PyComplexObject),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_7complex_complex) __PYX_ERR(5, 15, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule("array"); if (unlikely(!__pyx_t_1)) __PYX_ERR(2, 58, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_7cpython_5array_array = __Pyx_ImportType(__pyx_t_1, "array", "array", sizeof(arrayobject), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_7cpython_5array_array = __Pyx_ImportType(__pyx_t_1, "array", "array", sizeof(arrayobject), __PYX_GET_STRUCT_ALIGNMENT(arrayobject),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_7cpython_5array_array) __PYX_ERR(2, 58, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __pyx_t_1 = PyImport_ImportModule("rbfly.amqp._message"); if (unlikely(!__pyx_t_1)) __PYX_ERR(6, 22, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
-  __pyx_ptype_5rbfly_4amqp_8_message_MessageCtx = __Pyx_ImportType(__pyx_t_1, "rbfly.amqp._message", "MessageCtx", sizeof(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx), __Pyx_ImportType_CheckSize_Warn);
+  __pyx_ptype_5rbfly_4amqp_8_message_MessageCtx = __Pyx_ImportType(__pyx_t_1, "rbfly.amqp._message", "MessageCtx", sizeof(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx), __PYX_GET_STRUCT_ALIGNMENT(struct __pyx_obj_5rbfly_4amqp_8_message_MessageCtx),
+  __Pyx_ImportType_CheckSize_Warn);
    if (!__pyx_ptype_5rbfly_4amqp_8_message_MessageCtx) __PYX_ERR(6, 22, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
   __Pyx_RefNannyFinishContext();
   return 0;
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
   __Pyx_RefNannyFinishContext();
@@ -8300,28 +8312,28 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_COMPILING_IN_PYPY
-        PyObject *tmp_type, *tmp_value, *tmp_tb;
-        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
-        Py_INCREF(tb);
-        PyErr_Restore(tmp_type, tmp_value, tb);
-        Py_XDECREF(tmp_tb);
-#else
+#if CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
+#else
+        PyObject *tmp_type, *tmp_value, *tmp_tb;
+        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
+        Py_INCREF(tb);
+        PyErr_Restore(tmp_type, tmp_value, tb);
+        Py_XDECREF(tmp_tb);
 #endif
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
@@ -8995,44 +9007,62 @@
     return ret;
 }
 
 /* TypeImport */
 #ifndef __PYX_HAVE_RT_ImportType
 #define __PYX_HAVE_RT_ImportType
 static PyTypeObject *__Pyx_ImportType(PyObject *module, const char *module_name, const char *class_name,
-    size_t size, enum __Pyx_ImportType_CheckSize check_size)
+    size_t size, size_t alignment, enum __Pyx_ImportType_CheckSize check_size)
 {
     PyObject *result = 0;
     char warning[200];
     Py_ssize_t basicsize;
+    Py_ssize_t itemsize;
 #ifdef Py_LIMITED_API
     PyObject *py_basicsize;
+    PyObject *py_itemsize;
 #endif
     result = PyObject_GetAttrString(module, class_name);
     if (!result)
         goto bad;
     if (!PyType_Check(result)) {
         PyErr_Format(PyExc_TypeError,
             "%.200s.%.200s is not a type object",
             module_name, class_name);
         goto bad;
     }
 #ifndef Py_LIMITED_API
     basicsize = ((PyTypeObject *)result)->tp_basicsize;
+    itemsize = ((PyTypeObject *)result)->tp_itemsize;
 #else
     py_basicsize = PyObject_GetAttrString(result, "__basicsize__");
     if (!py_basicsize)
         goto bad;
     basicsize = PyLong_AsSsize_t(py_basicsize);
     Py_DECREF(py_basicsize);
     py_basicsize = 0;
     if (basicsize == (Py_ssize_t)-1 && PyErr_Occurred())
         goto bad;
+    py_itemsize = PyObject_GetAttrString(result, "__itemsize__");
+    if (!py_itemsize)
+        goto bad;
+    itemsize = PyLong_AsSsize_t(py_itemsize);
+    Py_DECREF(py_itemsize);
+    py_itemsize = 0;
+    if (itemsize == (Py_ssize_t)-1 && PyErr_Occurred())
+        goto bad;
 #endif
-    if ((size_t)basicsize < size) {
+    if (itemsize) {
+        if (size % alignment) {
+            alignment = size % alignment;
+        }
+        if (itemsize < (Py_ssize_t)alignment)
+            itemsize = (Py_ssize_t)alignment;
+    }
+    if ((size_t)(basicsize + itemsize) < size) {
         PyErr_Format(PyExc_ValueError,
             "%.200s.%.200s size changed, may indicate binary incompatibility. "
             "Expected %zd from C header, got %zd from PyObject",
             module_name, class_name, size, basicsize);
         goto bad;
     }
     if (check_size == __Pyx_ImportType_CheckSize_Error && (size_t)basicsize != size) {
```

### Comparing `rbfly-0.6.1/rbfly/streams/_codec.pyi` & `rbfly-0.6.2/rbfly/streams/_codec.pyi`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_codec.pyx` & `rbfly-0.6.2/rbfly/streams/_codec.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_mqueue.c` & `rbfly-0.6.2/rbfly/streams/_mqueue.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.33 */
+/* Generated by Cython 0.29.34 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [],
         "name": "rbfly.streams._mqueue",
         "sources": [
@@ -18,16 +18,16 @@
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_33"
-#define CYTHON_HEX_VERSION 0x001D21F0
+#define CYTHON_ABI "0_29_34"
+#define CYTHON_HEX_VERSION 0x001D22F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -212,15 +212,15 @@
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
   #if PY_VERSION_HEX < 0x02070000
     #undef CYTHON_USE_PYLONG_INTERNALS
     #define CYTHON_USE_PYLONG_INTERNALS 0
   #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS 1
+    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -251,15 +251,15 @@
   #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
   #endif
   #ifndef CYTHON_USE_TP_FINALIZE
     #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
   #endif
   #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS (PY_VERSION_HEX >= 0x030600B1)
+    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
   #endif
   #if PY_VERSION_HEX >= 0x030B00A4
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
     #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
   #endif
@@ -4586,28 +4586,28 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_COMPILING_IN_PYPY
-        PyObject *tmp_type, *tmp_value, *tmp_tb;
-        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
-        Py_INCREF(tb);
-        PyErr_Restore(tmp_type, tmp_value, tb);
-        Py_XDECREF(tmp_tb);
-#else
+#if CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
+#else
+        PyObject *tmp_type, *tmp_value, *tmp_tb;
+        PyErr_Fetch(&tmp_type, &tmp_value, &tmp_tb);
+        Py_INCREF(tb);
+        PyErr_Restore(tmp_type, tmp_value, tb);
+        Py_XDECREF(tmp_tb);
 #endif
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
@@ -5963,15 +5963,19 @@
 #endif
 #if PY_VERSION_HEX >= 0x030500B2 || defined(PyCoro_CheckExact)
     if (PyCoro_CheckExact(obj)) {
         return __Pyx_NewRef(obj);
     } else
 #endif
 #if CYTHON_COMPILING_IN_CPYTHON && defined(CO_ITERABLE_COROUTINE)
+#if PY_VERSION_HEX >= 0x030C00A6
+    if (PyGen_CheckExact(obj) && (PyGen_GetCode(obj)->co_flags & CO_ITERABLE_COROUTINE)) {
+#else
     if (PyGen_CheckExact(obj) && ((PyGenObject*)obj)->gi_code && ((PyCodeObject *)((PyGenObject*)obj)->gi_code)->co_flags & CO_ITERABLE_COROUTINE) {
+#endif
         return __Pyx_NewRef(obj);
     } else
 #endif
     {
         PyObject *method = NULL;
         int is_method = __Pyx_PyObject_GetMethod(obj, __pyx_n_s_await, &method);
         if (likely(is_method)) {
@@ -6013,15 +6017,15 @@
                  "object %.100s can't be used in 'await' expression",
                  Py_TYPE(obj)->tp_name);
 bad:
     return NULL;
 }
 
 /* CoroutineYieldFrom */
-static PyObject* __Pyx__Coroutine_Yield_From_Generic(__pyx_CoroutineObject *gen, PyObject *source) {
+  static PyObject* __Pyx__Coroutine_Yield_From_Generic(__pyx_CoroutineObject *gen, PyObject *source) {
     PyObject *retval;
     PyObject *source_gen = __Pyx__Coroutine_GetAwaitableIter(source);
     if (unlikely(!source_gen)) {
         return NULL;
     }
     if (__Pyx_Coroutine_Check(source_gen)) {
         retval = __Pyx_Generator_Next(source_gen);
@@ -6060,25 +6064,25 @@
         Py_INCREF(source);
         gen->yieldfrom = source;
     }
     return retval;
 }
 
 /* PyObject_GenericGetAttr */
-#if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
+  #if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
 static PyObject* __Pyx_PyObject_GenericGetAttr(PyObject* obj, PyObject* attr_name) {
     if (unlikely(Py_TYPE(obj)->tp_dictoffset)) {
         return PyObject_GenericGetAttr(obj, attr_name);
     }
     return __Pyx_PyObject_GenericGetAttrNoDict(obj, attr_name);
 }
 #endif
 
 /* SetVTable */
-static int __Pyx_SetVtable(PyObject *dict, void *vtable) {
+  static int __Pyx_SetVtable(PyObject *dict, void *vtable) {
 #if PY_VERSION_HEX >= 0x02070000
     PyObject *ob = PyCapsule_New(vtable, 0, 0);
 #else
     PyObject *ob = PyCObject_FromVoidPtr(vtable, 0);
 #endif
     if (!ob)
         goto bad;
@@ -6088,15 +6092,15 @@
     return 0;
 bad:
     Py_XDECREF(ob);
     return -1;
 }
 
 /* PyErrExceptionMatches */
-#if CYTHON_FAST_THREAD_STATE
+  #if CYTHON_FAST_THREAD_STATE
 static int __Pyx_PyErr_ExceptionMatchesTuple(PyObject *exc_type, PyObject *tuple) {
     Py_ssize_t i, n;
     n = PyTuple_GET_SIZE(tuple);
 #if PY_MAJOR_VERSION >= 3
     for (i=0; i<n; i++) {
         if (exc_type == PyTuple_GET_ITEM(tuple, i)) return 1;
     }
@@ -6113,15 +6117,15 @@
     if (unlikely(PyTuple_Check(err)))
         return __Pyx_PyErr_ExceptionMatchesTuple(exc_type, err);
     return __Pyx_PyErr_GivenExceptionMatches(exc_type, err);
 }
 #endif
 
 /* PyObjectGetAttrStrNoError */
-static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
+  static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
     __Pyx_PyThreadState_declare
     __Pyx_PyThreadState_assign
     if (likely(__Pyx_PyErr_ExceptionMatches(PyExc_AttributeError)))
         __Pyx_PyErr_Clear();
 }
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name) {
     PyObject *result;
@@ -6135,15 +6139,15 @@
     if (unlikely(!result)) {
         __Pyx_PyObject_GetAttrStr_ClearAttributeError();
     }
     return result;
 }
 
 /* SetupReduce */
-static int __Pyx_setup_reduce_is_named(PyObject* meth, PyObject* name) {
+  static int __Pyx_setup_reduce_is_named(PyObject* meth, PyObject* name) {
   int ret;
   PyObject *name_attr;
   name_attr = __Pyx_PyObject_GetAttrStr(meth, __pyx_n_s_name);
   if (likely(name_attr)) {
       ret = PyObject_RichCompareBool(name_attr, name, Py_EQ);
   } else {
       ret = -1;
@@ -6239,15 +6243,15 @@
     Py_XDECREF(reduce_cython);
     Py_XDECREF(setstate);
     Py_XDECREF(setstate_cython);
     return ret;
 }
 
 /* Import */
-static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level) {
+  static PyObject *__Pyx_Import(PyObject *name, PyObject *from_list, int level) {
     PyObject *empty_list = 0;
     PyObject *module = 0;
     PyObject *global_dict = 0;
     PyObject *empty_dict = 0;
     PyObject *list;
     #if PY_MAJOR_VERSION < 3
     PyObject *py_import;
@@ -6304,15 +6308,15 @@
     #endif
     Py_XDECREF(empty_list);
     Py_XDECREF(empty_dict);
     return module;
 }
 
 /* PatchInspect */
-static PyObject* __Pyx_patch_inspect(PyObject* module) {
+  static PyObject* __Pyx_patch_inspect(PyObject* module) {
 #if defined(__Pyx_Generator_USED) && (!defined(CYTHON_PATCH_INSPECT) || CYTHON_PATCH_INSPECT)
     static int inspect_patched = 0;
     if (unlikely((!inspect_patched) && module)) {
         module = __Pyx_Coroutine_patch_module(
             module, ""
 "old_types = getattr(_module.isgenerator, '_cython_generator_types', None)\n"
 "if old_types is None or not isinstance(old_types, set):\n"
@@ -6329,15 +6333,15 @@
 #else
     if ((0)) return __Pyx_Coroutine_patch_module(module, NULL);
 #endif
     return module;
 }
 
 /* PatchAsyncIO */
-static PyObject* __Pyx_patch_asyncio(PyObject* module) {
+  static PyObject* __Pyx_patch_asyncio(PyObject* module) {
 #if PY_VERSION_HEX < 0x030500B2 &&\
         (defined(__Pyx_Coroutine_USED) || defined(__Pyx_Generator_USED)) &&\
         (!defined(CYTHON_PATCH_ASYNCIO) || CYTHON_PATCH_ASYNCIO)
     PyObject *patch_module = NULL;
     static int asyncio_patched = 0;
     if (unlikely((!asyncio_patched) && module)) {
         PyObject *package;
@@ -6412,29 +6416,29 @@
 #else
     if ((0)) return __Pyx_patch_inspect(__Pyx_Coroutine_patch_module(module, NULL));
 #endif
     return module;
 }
 
 /* ImportFrom */
-static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name) {
+  static PyObject* __Pyx_ImportFrom(PyObject* module, PyObject* name) {
     PyObject* value = __Pyx_PyObject_GetAttrStr(module, name);
     if (unlikely(!value) && PyErr_ExceptionMatches(PyExc_AttributeError)) {
         PyErr_Format(PyExc_ImportError,
         #if PY_MAJOR_VERSION < 3
             "cannot import name %.230s", PyString_AS_STRING(name));
         #else
             "cannot import name %S", name);
         #endif
     }
     return value;
 }
 
 /* CLineInTraceback */
-#ifndef CYTHON_CLINE_IN_TRACEBACK
+  #ifndef CYTHON_CLINE_IN_TRACEBACK
 static int __Pyx_CLineForTraceback(CYTHON_UNUSED PyThreadState *tstate, int c_line) {
     PyObject *use_cline;
     PyObject *ptype, *pvalue, *ptraceback;
 #if CYTHON_COMPILING_IN_CPYTHON
     PyObject **cython_runtime_dict;
 #endif
     if (unlikely(!__pyx_cython_runtime)) {
@@ -6468,15 +6472,15 @@
     }
     __Pyx_ErrRestoreInState(tstate, ptype, pvalue, ptraceback);
     return c_line;
 }
 #endif
 
 /* CodeObjectCache */
-static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line) {
+  static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line) {
     int start = 0, mid = 0, end = count - 1;
     if (end >= 0 && code_line > entries[end].code_line) {
         return count;
     }
     while (start < end) {
         mid = start + (end - start) / 2;
         if (code_line < entries[mid].code_line) {
@@ -6548,15 +6552,15 @@
     entries[pos].code_line = code_line;
     entries[pos].code_object = code_object;
     __pyx_code_cache.count++;
     Py_INCREF(code_object);
 }
 
 /* AddTraceback */
-#include "compile.h"
+  #include "compile.h"
 #include "frameobject.h"
 #include "traceback.h"
 #if PY_VERSION_HEX >= 0x030b00a6
   #ifndef Py_BUILD_CORE
     #define Py_BUILD_CORE 1
   #endif
   #include "internal/pycore_frame.h"
@@ -6655,15 +6659,15 @@
     PyTraceBack_Here(py_frame);
 bad:
     Py_XDECREF(py_code);
     Py_XDECREF(py_frame);
 }
 
 /* CIntFromPyVerify */
-#define __PYX_VERIFY_RETURN_INT(target_type, func_type, func_value)\
+  #define __PYX_VERIFY_RETURN_INT(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 0)
 #define __PYX_VERIFY_RETURN_INT_EXC(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 1)
 #define __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, exc)\
     {\
         func_type value = func_value;\
         if (sizeof(target_type) < sizeof(func_type)) {\
@@ -6677,15 +6681,15 @@
                     goto raise_overflow;\
             }\
         }\
         return (target_type) value;\
     }
 
 /* CIntFromPy */
-static CYTHON_INLINE int32_t __Pyx_PyInt_As_int32_t(PyObject *x) {
+  static CYTHON_INLINE int32_t __Pyx_PyInt_As_int32_t(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const int32_t neg_one = (int32_t) -1, const_zero = (int32_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -6873,15 +6877,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to int32_t");
     return (int32_t) -1;
 }
 
 /* CIntFromPy */
-static CYTHON_INLINE uint16_t __Pyx_PyInt_As_uint16_t(PyObject *x) {
+  static CYTHON_INLINE uint16_t __Pyx_PyInt_As_uint16_t(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const uint16_t neg_one = (uint16_t) -1, const_zero = (uint16_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -7069,15 +7073,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to uint16_t");
     return (uint16_t) -1;
 }
 
 /* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_int32_t(int32_t value) {
+  static CYTHON_INLINE PyObject* __Pyx_PyInt_From_int32_t(int32_t value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const int32_t neg_one = (int32_t) -1, const_zero = (int32_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -7107,15 +7111,15 @@
         unsigned char *bytes = (unsigned char *)&value;
         return _PyLong_FromByteArray(bytes, sizeof(int32_t),
                                      little, !is_unsigned);
     }
 }
 
 /* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
+  static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const long neg_one = (long) -1, const_zero = (long) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -7145,15 +7149,15 @@
         unsigned char *bytes = (unsigned char *)&value;
         return _PyLong_FromByteArray(bytes, sizeof(long),
                                      little, !is_unsigned);
     }
 }
 
 /* CIntFromPy */
-static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *x) {
+  static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const long neg_one = (long) -1, const_zero = (long) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -7341,15 +7345,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to long");
     return (long) -1;
 }
 
 /* CIntFromPy */
-static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *x) {
+  static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *x) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const int neg_one = (int) -1, const_zero = (int) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
@@ -7537,15 +7541,15 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to int");
     return (int) -1;
 }
 
 /* FastTypeChecks */
-#if CYTHON_COMPILING_IN_CPYTHON
+  #if CYTHON_COMPILING_IN_CPYTHON
 static int __Pyx_InBases(PyTypeObject *a, PyTypeObject *b) {
     while (a) {
         a = a->tp_base;
         if (a == b)
             return 1;
     }
     return b == &PyBaseObject_Type;
@@ -7637,15 +7641,15 @@
         return __Pyx_inner_PyErr_GivenExceptionMatches2(err, exc_type1, exc_type2);
     }
     return (PyErr_GivenExceptionMatches(err, exc_type1) || PyErr_GivenExceptionMatches(err, exc_type2));
 }
 #endif
 
 /* CheckBinaryVersion */
-static int __Pyx_check_binary_version(void) {
+  static int __Pyx_check_binary_version(void) {
     char ctversion[5];
     int same=1, i, found_dot;
     const char* rt_from_call = Py_GetVersion();
     PyOS_snprintf(ctversion, 5, "%d.%d", PY_MAJOR_VERSION, PY_MINOR_VERSION);
     found_dot = 0;
     for (i = 0; i < 4; i++) {
         if (!ctversion[i]) {
@@ -7675,15 +7679,15 @@
                       ctversion, __Pyx_MODULE_NAME, rtversion);
         return PyErr_WarnEx(NULL, message, 1);
     }
     return 0;
 }
 
 /* InitStrings */
-static int __Pyx_InitStrings(__Pyx_StringTabEntry *t) {
+  static int __Pyx_InitStrings(__Pyx_StringTabEntry *t) {
     while (t->p) {
         #if PY_MAJOR_VERSION < 3
         if (t->is_unicode) {
             *t->p = PyUnicode_DecodeUTF8(t->s, t->n - 1, NULL);
         } else if (t->intern) {
             *t->p = PyString_InternFromString(t->s);
         } else {
```

### Comparing `rbfly-0.6.1/rbfly/streams/_mqueue.pyi` & `rbfly-0.6.2/rbfly/streams/_mqueue.pyi`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/_mqueue.pyx` & `rbfly-0.6.2/rbfly/streams/_mqueue.pyx`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/client.py` & `rbfly-0.6.2/rbfly/streams/client.py`

 * *Files 1% similar despite different names*

```diff
@@ -455,15 +455,20 @@
     :param uri: Connection URI.
     """
     p = urlparse(uri)
     port = p.port
 
     scheme = Scheme(p.scheme)
     host = p.hostname if p.hostname else 'localhost'
-    vhost = p.path if p.path else '/'
+
+    # '/' -> '/'
+    # '//' -> '/'
+    # '/vhost' -> 'vhost'
+    path = p.path[1:]
+    vhost = path if path else '/'
 
     if port is None and scheme == Scheme.RABBITMQ_STREAM:
         port = 5552
     elif port is None and scheme == Scheme.RABBITMQ_STREAM_TLS:
         port = 5551
     elif port is None:
         port = 5552
```

### Comparing `rbfly-0.6.1/rbfly/streams/codec.py` & `rbfly-0.6.2/rbfly/streams/codec.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/const.py` & `rbfly-0.6.2/rbfly/streams/const.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/error.py` & `rbfly-0.6.2/rbfly/streams/error.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/offset.py` & `rbfly-0.6.2/rbfly/streams/offset.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/protocol.py` & `rbfly-0.6.2/rbfly/streams/protocol.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/types.py` & `rbfly-0.6.2/rbfly/streams/types.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/streams/util.py` & `rbfly-0.6.2/rbfly/streams/util.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/__init__.py` & `rbfly-0.6.2/rbfly/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/amqp/__init__.py` & `rbfly-0.6.2/rbfly/tests/amqp/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/amqp/test_message.py` & `rbfly-0.6.2/rbfly/tests/amqp/test_message.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/streams/__init__.py` & `rbfly-0.6.2/rbfly/tests/streams/__init__.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/streams/test_client.py` & `rbfly-0.6.2/rbfly/tests/streams/test_client.py`

 * *Files 1% similar despite different names*

```diff
@@ -45,28 +45,32 @@
         Scheme.RABBITMQ_STREAM, 'localhost', 5552, '/', None, None
     ),
     (
         'rabbitmq-stream://localhost',
         Scheme.RABBITMQ_STREAM, 'localhost', 5552, '/', None, None
     ),
     (
+        'rabbitmq-stream://localhost/',
+        Scheme.RABBITMQ_STREAM, 'localhost', 5552, '/', None, None
+    ),
+    (
         'rabbitmq-stream://some-server:1002/a-vhost',
-        Scheme.RABBITMQ_STREAM, 'some-server', 1002, '/a-vhost', None, None
+        Scheme.RABBITMQ_STREAM, 'some-server', 1002, 'a-vhost', None, None
     ),
     (
         'rabbitmq-stream+tls://some-server',
         Scheme.RABBITMQ_STREAM_TLS, 'some-server', 5551, '/', None, None
     ),
     (
         'rabbitmq-stream://user@some-server',
         Scheme.RABBITMQ_STREAM, 'some-server', 5552, '/', 'user', None
     ),
     (
         'rabbitmq-stream://user:passta@some-server/tsohvvhost',
-        Scheme.RABBITMQ_STREAM, 'some-server', 5552, '/tsohvvhost', 'user', 'passta'
+        Scheme.RABBITMQ_STREAM, 'some-server', 5552, 'tsohvvhost', 'user', 'passta'
     ),
 ]
 
 TEST_MESSAGE_ID = [
     (2 ** 31 - 1, 2 ** 31),
     (2 ** 32 - 1, 2 ** 32),
     (2 ** 63 - 1, 2 ** 63),
@@ -80,15 +84,15 @@
         uri: str,
         scheme: Scheme,
         host: str,
         port: int,
         vhost: str,
         user: tp.Optional[str],
         password: tp.Optional[str],
-    ) -> None:
+) -> None:
     """
     Test creating RabbitMQ Streams client from URI.
     """
     # pylint: disable=protected-access
 
     client = streams_client(uri)
     assert client._cinfo.scheme == scheme
```

### Comparing `rbfly-0.6.1/rbfly/tests/streams/test_codec.py` & `rbfly-0.6.2/rbfly/tests/streams/test_codec.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/streams/test_mqueue.py` & `rbfly-0.6.2/rbfly/tests/streams/test_mqueue.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/streams/test_offset.py` & `rbfly-0.6.2/rbfly/tests/streams/test_offset.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/tests/test_util.py` & `rbfly-0.6.2/rbfly/tests/test_util.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/types.py` & `rbfly-0.6.2/rbfly/types.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly/util.py` & `rbfly-0.6.2/rbfly/util.py`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/rbfly.egg-info/PKG-INFO` & `rbfly-0.6.2/rbfly.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rbfly
-Version: 0.6.1
+Version: 0.6.2
 Summary: RbFly - a library for RabbitMQ Streams using Python asyncio
 Home-page: https://wrobell.dcmod.org/rbfly/
 Author: Artur Wroblewski
 Author-email: wrobell@riseup.net
 License: GPLv3+
 Project-URL: Source Code, https://gitlab.com/wrobell/rbfly
 Project-URL: Bug tracker, https://gitlab.com/wrobell/rbfly/issues
```

### Comparing `rbfly-0.6.1/rbfly.egg-info/SOURCES.txt` & `rbfly-0.6.2/rbfly.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `rbfly-0.6.1/setup.cfg` & `rbfly-0.6.2/setup.cfg`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = rbfly
-version = 0.6.1
+version = 0.6.2
 author = Artur Wroblewski
 author_email = wrobell@riseup.net
 license = GPLv3+
 description = RbFly - a library for RabbitMQ Streams using Python asyncio
 long_description = file: README
 long_description_content_type = text/x-rst
 url = https://wrobell.dcmod.org/rbfly/
@@ -29,15 +29,15 @@
 	*.pyx
 	*.pxd
 	*.h
 
 [options.extras_require]
 tests = 
 	cython-lint
-	mypy == 1.1.1
+	mypy == 1.3.0
 	bandit
 	toml  # required by bandit, not needed when using Python 3.11?
 	pylint
 	pytest-cov
 	pytest-timeout
 	pytest-asyncio
 	pytest-lazy-fixture
```

### Comparing `rbfly-0.6.1/setup.py` & `rbfly-0.6.2/setup.py`

 * *Files identical despite different names*

