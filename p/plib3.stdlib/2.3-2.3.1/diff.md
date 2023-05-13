# Comparing `tmp/plib3.stdlib-2.3.tar.gz` & `tmp/plib3.stdlib-2.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "plib3.stdlib-2.3.tar", last modified: Tue Jul 12 17:17:17 2022, max compression
+gzip compressed data, was "/home/pdonis/git/plib3-stdlib/dist/tmpciqxsh4d/plib3.stdlib-2.3.1.tar", last modified: Sat May 13 03:53:01 2023, max compression
```

## Comparing `plib3.stdlib-2.3.tar` & `plib3.stdlib-2.3.1.tar`

### file list

```diff
@@ -1,109 +1,109 @@
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.118144 plib3.stdlib-2.3/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    90557 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/CHANGES.rst
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    18010 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/LICENSE.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)       38 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/MANIFEST.in
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     7783 2022-07-12 17:17:17.118144 plib3.stdlib-2.3/PKG-INFO
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     6862 2022-03-07 06:51:40.000000 plib3.stdlib-2.3/README.rst
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      131 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/TODO.rst
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.102144 plib3.stdlib-2.3/examples/
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.102144 plib3.stdlib-2.3/examples/pyget/
--rwxr-x---   0 pdonis    (1002) pdonis    (1002)     3511 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/examples/pyget/pyget3.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.102144 plib3.stdlib-2.3/examples/pyidserver/
--rwxr-x---   0 pdonis    (1002) pdonis    (1002)     9934 2022-01-13 06:38:38.000000 plib3.stdlib-2.3/examples/pyidserver/pyidserver3.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.106144 plib3.stdlib-2.3/examples/scrips/
--rwxr-x---   0 pdonis    (1002) pdonis    (1002)     6239 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/examples/scrips/scrips3.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.106144 plib3.stdlib-2.3/examples/tzname/
--rwxr-x---   0 pdonis    (1002) pdonis    (1002)     3268 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/examples/tzname/tzname3.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.102144 plib3.stdlib-2.3/plib/
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.110144 plib3.stdlib-2.3/plib/stdlib/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      470 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/plib/stdlib/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3877 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/plib/stdlib/_extras.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1731 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/plib/stdlib/builtins.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5799 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/classtools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2695 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/cmdline.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.110144 plib3.stdlib-2.3/plib/stdlib/coll/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     8392 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    12098 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_abc.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     8327 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_bases.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    19554 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_mixins.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3534 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_names.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3062 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_seq.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2957 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_tests.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     8582 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_tuples.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5617 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/coll/_utils.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1475 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/copytools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2069 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/csvtools.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.110144 plib3.stdlib-2.3/plib/stdlib/decotools/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     6052 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/decotools/DelayedDecorator.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5064 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/decotools/IndexedGenerator.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     6174 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/decotools/MemoizedGenerator.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    42806 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/decotools/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      592 2022-03-07 06:51:40.000000 plib3.stdlib-2.3/plib/stdlib/examples.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      604 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/fdtools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1250 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/imp.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.114144 plib3.stdlib-2.3/plib/stdlib/ini/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3470 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/PIniFile.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2413 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/PIniFileBase.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1210 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/PIniFileOption.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1714 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/PIniFileSection.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5544 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/PIniInterface.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2464 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ini/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    28538 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/iters.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1317 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/jsontools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5303 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/localize.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     4341 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/mail.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      772 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/mathlib.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.114144 plib3.stdlib-2.3/plib/stdlib/net/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3509 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/net/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     6690 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/net/client.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2361 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/net/transport.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     8247 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/options.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     6036 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/ostools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     7367 2022-03-07 06:51:40.000000 plib3.stdlib-2.3/plib/stdlib/postinstall.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1956 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/proc.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      537 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/sigs.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3143 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/strings.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1471 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/systools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1782 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/timer.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5882 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/tztools.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.114144 plib3.stdlib-2.3/plib/stdlib/util/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     7156 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/util/ModuleProxy.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      369 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/stdlib/util/__init__.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.114144 plib3.stdlib-2.3/plib/test/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1046 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/__main__.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.118144 plib3.stdlib-2.3/plib/test/stdlib/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      721 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/ModuleProxy_testmod.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      282 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      729 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/plib/test/stdlib/__main__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    41450 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/abstract_testlib.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.118144 plib3.stdlib-2.3/plib/test/stdlib/doctests/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     4293 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1079 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_Singleton.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     4290 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_SortMixin.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1984 2022-07-12 17:15:26.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_abc.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2474 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_builtins.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1313 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_cached_property.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      790 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_coll.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3583 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_newlines.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     7596 2021-03-15 05:03:01.000000 plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_normalize_slice.txt
--rw-r-----   0 pdonis    (1002) pdonis    (1002)    22729 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/mapping_testlib.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     4228 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_ModuleProxy.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      938 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractcontainer.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1010 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractdict.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      870 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractkeyed.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1392 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractlist.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      961 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractmapping.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1859 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_abstractsequence.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      871 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_basecontainer.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1060 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_basedict.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      852 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_basekeyed.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1052 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_baselist.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      946 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_basemapping.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      946 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_basesequence.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     5612 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_ostools.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1302 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_sigs.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     2121 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/stdlib/test_stdlib.py
-drwxr-x---   0 pdonis    (1002) pdonis    (1002)        0 2022-07-12 17:17:17.118144 plib3.stdlib-2.3/plib/test/support/
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     3760 2022-01-09 02:45:11.000000 plib3.stdlib-2.3/plib/test/support/__init__.py
--rw-r-----   0 pdonis    (1002) pdonis    (1002)      117 2022-03-07 06:51:40.000000 plib3.stdlib-2.3/pyproject.toml
--rw-r-----   0 pdonis    (1002) pdonis    (1002)     1639 2022-07-12 17:17:17.122144 plib3.stdlib-2.3/setup.cfg
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1471 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/systools.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1782 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/timer.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     5799 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/classtools.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     5303 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/localize.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)      472 2023-05-13 03:47:26.000000 plib3.stdlib-2.3.1/plib/stdlib/__init__.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/util/
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      369 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/util/__init__.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     7156 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/util/ModuleProxy.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     3143 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/strings.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)      592 2022-01-20 06:02:56.000000 plib3.stdlib-2.3.1/plib/stdlib/examples.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1250 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/imp.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1317 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/jsontools.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)    28538 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/iters.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     7720 2023-05-13 03:48:48.000000 plib3.stdlib-2.3.1/plib/stdlib/postinstall.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     6036 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/ostools.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     1731 2022-07-29 23:10:48.000000 plib3.stdlib-2.3.1/plib/stdlib/builtins.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     3877 2022-07-29 23:10:48.000000 plib3.stdlib-2.3.1/plib/stdlib/_extras.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     4341 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/mail.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1475 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/copytools.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     2464 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/__init__.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     3470 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFile.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     1714 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileSection.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     5544 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/PIniInterface.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1210 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileOption.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     2413 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileBase.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     2695 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/cmdline.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     2069 2022-01-03 06:29:22.000000 plib3.stdlib-2.3.1/plib/stdlib/csvtools.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     8247 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/options.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1956 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/proc.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     8392 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/__init__.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     3534 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_names.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     2957 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_tests.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)    12098 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_abc.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     5617 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_utils.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     3062 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_seq.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     8582 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_tuples.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)    19554 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_mixins.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     8327 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/coll/_bases.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      772 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/mathlib.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/decotools/
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     5064 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/decotools/IndexedGenerator.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)    42806 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/decotools/__init__.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     6174 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/decotools/MemoizedGenerator.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     6052 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/decotools/DelayedDecorator.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/stdlib/net/
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     3509 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/net/__init__.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     6690 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/net/client.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     2361 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/plib/stdlib/net/transport.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      537 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/sigs.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     5882 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/tztools.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      604 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/stdlib/fdtools.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/test/
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/test/stdlib/
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1079 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_Singleton.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     3583 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_newlines.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     2474 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_builtins.txt
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     1984 2022-07-29 23:10:48.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_abc.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      790 2019-09-24 03:38:20.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_coll.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     7596 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_normalize_slice.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     4290 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_SortMixin.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1313 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_cached_property.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     4293 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib.txt
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1302 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_sigs.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1392 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractlist.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      282 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/__init__.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      938 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractcontainer.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      721 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/ModuleProxy_testmod.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      852 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_basekeyed.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      870 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractkeyed.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      961 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractmapping.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)    41450 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/abstract_testlib.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1060 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_basedict.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1052 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_baselist.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     2121 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_stdlib.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     4228 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_ModuleProxy.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1010 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractdict.py
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)      729 2022-07-29 23:10:48.000000 plib3.stdlib-2.3.1/plib/test/stdlib/__main__.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     5612 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_ostools.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      946 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_basemapping.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      871 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_basecontainer.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1859 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractsequence.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)    22729 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/mapping_testlib.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      946 2022-01-03 06:29:23.000000 plib3.stdlib-2.3.1/plib/test/stdlib/test_basesequence.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     1046 2022-01-05 02:22:10.000000 plib3.stdlib-2.3.1/plib/test/__main__.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/plib/test/support/
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)     3760 2022-01-04 20:34:28.000000 plib3.stdlib-2.3.1/plib/test/support/__init__.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/examples/
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/examples/pyidserver/
+-rwxrwx---   0 pdonis    (1002) pdonis    (1002)     9934 2022-01-09 05:08:44.000000 plib3.stdlib-2.3.1/examples/pyidserver/pyidserver3.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/examples/pyget/
+-rwxrwx---   0 pdonis    (1002) pdonis    (1002)     3511 2022-01-03 06:25:27.000000 plib3.stdlib-2.3.1/examples/pyget/pyget3.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/examples/scrips/
+-rwxrwx---   0 pdonis    (1002) pdonis    (1002)     6239 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/examples/scrips/scrips3.py
+drwxrwx---   0 pdonis    (1002) pdonis    (1002)        0 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/examples/tzname/
+-rwxrwx---   0 pdonis    (1002) pdonis    (1002)     3268 2022-01-03 06:29:49.000000 plib3.stdlib-2.3.1/examples/tzname/tzname3.py
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)    18010 2019-09-20 02:24:51.000000 plib3.stdlib-2.3.1/LICENSE.txt
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     6862 2022-01-22 04:03:34.000000 plib3.stdlib-2.3.1/README.rst
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)       38 2022-01-03 05:57:16.000000 plib3.stdlib-2.3.1/MANIFEST.in
+-rw-rw-r--   0 pdonis    (1002) pdonis    (1002)      131 2018-10-23 04:11:37.000000 plib3.stdlib-2.3.1/TODO.rst
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     7805 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/PKG-INFO
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)      117 2022-01-22 04:03:34.000000 plib3.stdlib-2.3.1/pyproject.toml
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)     1639 2023-05-13 03:53:01.000000 plib3.stdlib-2.3.1/setup.cfg
+-rw-rw----   0 pdonis    (1002) pdonis    (1002)    90727 2023-05-13 03:52:34.000000 plib3.stdlib-2.3.1/CHANGES.rst
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive
+POSIX tar archive (GNU)
```

### Comparing `plib3.stdlib-2.3/CHANGES.rst` & `plib3.stdlib-2.3.1/CHANGES.rst`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,17 @@
 plib3.stdlib Change Log
 =======================
 
+Version 2.3.1
+-------------
+
+- Speed up entry points generated by the ``make_entry_points``
+  function in the ``postinstall`` module by pre-computing the
+  script path.
+
 Version 2.3
 -----------
 
 - Add ``bbytes`` and ``bbytearray`` types to builtin extras, sane
   replacements for the built-in ``bytes`` and ``bytearray`` types
   that treat items at single indexes as objects of the same type,
   not integers.
```

### Comparing `plib3.stdlib-2.3/LICENSE.txt` & `plib3.stdlib-2.3.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/PKG-INFO` & `plib3.stdlib-2.3.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 Metadata-Version: 2.1
 Name: plib3.stdlib
-Version: 2.3
+Version: 2.3.1
 Summary: Useful packages and modules to extend the Python 3 standard library.
 Home-page: http://pypi.org/project/plib3.stdlib
 Author: Peter A. Donis
 Author-email: peterdonis@alum.mit.edu
 License: GPLv2
+Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
 Classifier: Environment :: MacOS X
 Classifier: Environment :: Win32 (MS Windows)
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU General Public License v2 (GPLv2)
 Classifier: Operating System :: MacOS :: MacOS X
@@ -196,7 +197,9 @@
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with this program; if not, write to the Free Software
 Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
+
+
```

### Comparing `plib3.stdlib-2.3/README.rst` & `plib3.stdlib-2.3.1/README.rst`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/examples/pyget/pyget3.py` & `plib3.stdlib-2.3.1/examples/pyget/pyget3.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/examples/pyidserver/pyidserver3.py` & `plib3.stdlib-2.3.1/examples/pyidserver/pyidserver3.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/examples/scrips/scrips3.py` & `plib3.stdlib-2.3.1/examples/scrips/scrips3.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/examples/tzname/tzname3.py` & `plib3.stdlib-2.3.1/examples/tzname/tzname3.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/_extras.py` & `plib3.stdlib-2.3.1/plib/stdlib/_extras.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/builtins.py` & `plib3.stdlib-2.3.1/plib/stdlib/builtins.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/classtools.py` & `plib3.stdlib-2.3.1/plib/stdlib/classtools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/cmdline.py` & `plib3.stdlib-2.3.1/plib/stdlib/cmdline.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/__init__.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/__init__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_abc.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_abc.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_bases.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_bases.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_mixins.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_mixins.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_names.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_names.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_seq.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_seq.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_tests.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_tests.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_tuples.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_tuples.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/coll/_utils.py` & `plib3.stdlib-2.3.1/plib/stdlib/coll/_utils.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/copytools.py` & `plib3.stdlib-2.3.1/plib/stdlib/copytools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/csvtools.py` & `plib3.stdlib-2.3.1/plib/stdlib/csvtools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/decotools/DelayedDecorator.py` & `plib3.stdlib-2.3.1/plib/stdlib/decotools/DelayedDecorator.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/decotools/IndexedGenerator.py` & `plib3.stdlib-2.3.1/plib/stdlib/decotools/IndexedGenerator.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/decotools/MemoizedGenerator.py` & `plib3.stdlib-2.3.1/plib/stdlib/decotools/MemoizedGenerator.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/decotools/__init__.py` & `plib3.stdlib-2.3.1/plib/stdlib/decotools/__init__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/examples.py` & `plib3.stdlib-2.3.1/plib/stdlib/examples.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/fdtools.py` & `plib3.stdlib-2.3.1/plib/stdlib/fdtools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/imp.py` & `plib3.stdlib-2.3.1/plib/stdlib/imp.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/PIniFile.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFile.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/PIniFileBase.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileBase.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/PIniFileOption.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileOption.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/PIniFileSection.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/PIniFileSection.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/PIniInterface.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/PIniInterface.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ini/__init__.py` & `plib3.stdlib-2.3.1/plib/stdlib/ini/__init__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/iters.py` & `plib3.stdlib-2.3.1/plib/stdlib/iters.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/jsontools.py` & `plib3.stdlib-2.3.1/plib/stdlib/jsontools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/localize.py` & `plib3.stdlib-2.3.1/plib/stdlib/localize.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/mail.py` & `plib3.stdlib-2.3.1/plib/stdlib/mail.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/mathlib.py` & `plib3.stdlib-2.3.1/plib/stdlib/mathlib.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/net/__init__.py` & `plib3.stdlib-2.3.1/plib/stdlib/net/__init__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/net/client.py` & `plib3.stdlib-2.3.1/plib/stdlib/net/client.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/net/transport.py` & `plib3.stdlib-2.3.1/plib/stdlib/net/transport.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/options.py` & `plib3.stdlib-2.3.1/plib/stdlib/options.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/ostools.py` & `plib3.stdlib-2.3.1/plib/stdlib/ostools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/postinstall.py` & `plib3.stdlib-2.3.1/plib/stdlib/postinstall.py`

 * *Files 4% similar despite different names*

```diff
@@ -102,14 +102,27 @@
         if os.path.isdir(fullname):
             for filename in os.listdir(fullname):
                 if filename.endswith(".py"):
                     names.append((name, filename))
     return names
 
 
+def _get_script_path(dirname, package_name, import_name=None, share_root=None, script_basename=None):
+    script_dir = _get_share_script_dir(package_name, import_name, share_root=share_root)
+    script_dir = os.path.join(script_dir, dirname)
+    script_basename = script_basename or first(f for f in os.listdir(script_dir) if f.endswith('.py'))
+    if not script_basename:
+        raise RuntimeError("Script not found for {} in {}".format(dirname, script_dir))
+    return os.path.join(script_dir, script_basename)
+
+
+def _run_script(script_path):
+    runpy.run_path(script_path, run_name='__main__')
+
+
 def run_share_script(dirname, package_name, import_name=None, share_root=None, script_basename=None):
     """Run script located in ``share`` directory ``dirname``.
     
     A common use case for this is running example programs distributed with a library
     (like those distributed with this library). If the programs are in a subdirectory
     of ``share/<dirname>`` (e.g., "examples" for example programs), pass the name of
     the subdirectory in ``share_root``.
@@ -120,26 +133,23 @@
     This function will normally run the first Python script it finds in the chosen
     directory; to tell it to run a specific script, pass the base name of the
     script (i.e., without any directory name, but with the ``.py`` extension if it
     has it) in ``script_basename``. (Note that this option can point to a script
     that does not have the ``.py`` extension.)
     """
     
-    script_dir = _get_share_script_dir(package_name, import_name, share_root=share_root)
-    script_dir = os.path.join(script_dir, dirname)
-    script_basename = script_basename or first(f for f in os.listdir(script_dir) if f.endswith('.py'))
-    if not script_basename:
-        raise RuntimeError("Script not found for {} in {}".format(dirname, script_dir))
-    script_path = os.path.join(script_dir, script_basename)
-    runpy.run_path(script_path, run_name='__main__')
+    script_path = _get_script_path(dirname, package_name, import_name, share_root, script_basename)
+    _run_script(script_path)
 
 
 def _make_entry_point(name, dirname, package_name, import_name=None, share_root=None, script_basename=None):
+    # Compute this in advance since it won't change
+    script_path = _get_script_path(dirname, package_name, import_name, share_root=share_root, script_basename=script_basename)
     def _f():
-        run_share_script(dirname, package_name, import_name, share_root=share_root, script_basename=script_basename)
+        _run_script(script_path)
     _f.__name__ = name
     return _f
 
 
 def make_entry_points(modname, package_name, import_name=None, share_root=None):
     """Add entry point functions to ``mod`` for share scripts shipped with ``package_name``.
     """
```

### Comparing `plib3.stdlib-2.3/plib/stdlib/proc.py` & `plib3.stdlib-2.3.1/plib/stdlib/proc.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/sigs.py` & `plib3.stdlib-2.3.1/plib/stdlib/sigs.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/strings.py` & `plib3.stdlib-2.3.1/plib/stdlib/strings.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/systools.py` & `plib3.stdlib-2.3.1/plib/stdlib/systools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/timer.py` & `plib3.stdlib-2.3.1/plib/stdlib/timer.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/tztools.py` & `plib3.stdlib-2.3.1/plib/stdlib/tztools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/stdlib/util/ModuleProxy.py` & `plib3.stdlib-2.3.1/plib/stdlib/util/ModuleProxy.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/__main__.py` & `plib3.stdlib-2.3.1/plib/test/__main__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/ModuleProxy_testmod.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/ModuleProxy_testmod.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/__main__.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/__main__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/abstract_testlib.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/abstract_testlib.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_Singleton.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_Singleton.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_SortMixin.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_SortMixin.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_abc.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_abc.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_builtins.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_builtins.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_cached_property.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_cached_property.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_coll.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_coll.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_newlines.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_newlines.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/doctests/test_stdlib_normalize_slice.txt` & `plib3.stdlib-2.3.1/plib/test/stdlib/doctests/test_stdlib_normalize_slice.txt`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/mapping_testlib.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/mapping_testlib.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_ModuleProxy.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_ModuleProxy.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractcontainer.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractcontainer.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractdict.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractdict.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractkeyed.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractkeyed.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractlist.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractlist.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractmapping.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractmapping.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_abstractsequence.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_abstractsequence.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_basecontainer.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_basecontainer.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_basedict.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_basedict.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_basekeyed.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_basekeyed.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_baselist.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_baselist.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_basemapping.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_basemapping.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_basesequence.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_basesequence.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_ostools.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_ostools.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_sigs.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_sigs.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/stdlib/test_stdlib.py` & `plib3.stdlib-2.3.1/plib/test/stdlib/test_stdlib.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/plib/test/support/__init__.py` & `plib3.stdlib-2.3.1/plib/test/support/__init__.py`

 * *Files identical despite different names*

### Comparing `plib3.stdlib-2.3/setup.cfg` & `plib3.stdlib-2.3.1/setup.cfg`

 * *Files identical despite different names*

