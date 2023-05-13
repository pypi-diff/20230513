# Comparing `tmp/pyobjus-1.2.1.tar.gz` & `tmp/pyobjus-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyobjus-1.2.1.tar", last modified: Sat Mar 26 18:32:13 2022, max compression
+gzip compressed data, was "pyobjus-1.2.2.tar", last modified: Sat May 13 11:52:34 2023, max compression
```

## Comparing `pyobjus-1.2.1.tar` & `pyobjus-1.2.2.tar`

### file list

```diff
@@ -1,94 +1,94 @@
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.478280 pyobjus-1.2.1/
--rw-r--r--   0 runner     (501) staff       (20)     1081 2022-03-26 18:32:01.000000 pyobjus-1.2.1/LICENSE
--rw-r--r--   0 runner     (501) staff       (20)      174 2022-03-26 18:32:01.000000 pyobjus-1.2.1/MANIFEST.in
--rw-r--r--   0 runner     (501) staff       (20)      755 2022-03-26 18:32:01.000000 pyobjus-1.2.1/Makefile
--rw-r--r--   0 runner     (501) staff       (20)      651 2022-03-26 18:32:13.477875 pyobjus-1.2.1/PKG-INFO
--rw-r--r--   0 runner     (501) staff       (20)     3572 2022-03-26 18:32:01.000000 pyobjus-1.2.1/README.md
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.437760 pyobjus-1.2.1/docs/
--rw-r--r--   0 runner     (501) staff       (20)     5577 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/Makefile
--rw-r--r--   0 runner     (501) staff       (20)     5107 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/make.bat
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.443685 pyobjus-1.2.1/docs/source/
--rw-r--r--   0 runner     (501) staff       (20)    11291 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/api.rst
--rw-r--r--   0 runner     (501) staff       (20)     7788 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/conf.py
--rw-r--r--   0 runner     (501) staff       (20)    33692 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/core_tutorials.rst
--rw-r--r--   0 runner     (501) staff       (20)     6855 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/foundation_eg.rst
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.444941 pyobjus-1.2.1/docs/source/images/
--rw-r--r--   0 runner     (501) staff       (20)    70057 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/images/IMG_0322.PNG
--rw-r--r--   0 runner     (501) staff       (20)    47645 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/images/IMG_0330.PNG
--rw-r--r--   0 runner     (501) staff       (20)      809 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/index.rst
--rw-r--r--   0 runner     (501) staff       (20)      619 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/installation.rst
--rw-r--r--   0 runner     (501) staff       (20)     8076 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/pyobjus_internal.rst
--rw-r--r--   0 runner     (501) staff       (20)    15991 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/pyobjus_ios.rst
--rw-r--r--   0 runner     (501) staff       (20)     2247 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/quickstart.rst
--rw-r--r--   0 runner     (501) staff       (20)      267 2022-03-26 18:32:01.000000 pyobjus-1.2.1/docs/source/remarks.rst
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.454426 pyobjus-1.2.1/examples/
--rw-r--r--   0 runner     (501) staff       (20)     4770 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/background_transfer.py
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.455733 pyobjus-1.2.1/examples/ball-example/
--rw-r--r--   0 runner     (501) staff       (20)      116 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ball-example/README.md
--rw-r--r--   0 runner     (501) staff       (20)     2735 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ball-example/main.py
--rw-r--r--   0 runner     (501) staff       (20)      738 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ball-example/pyobjusball.kv
--rw-r--r--   0 runner     (501) staff       (20)     1011 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/classes_and_selectors.py
--rw-r--r--   0 runner     (501) staff       (20)     1459 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/delegate.py
--rw-r--r--   0 runner     (501) staff       (20)      513 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ns_alert.py
--rw-r--r--   0 runner     (501) staff       (20)      575 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ns_array.py
--rw-r--r--   0 runner     (501) staff       (20)      636 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ns_dictionary.py
--rw-r--r--   0 runner     (501) staff       (20)     1074 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ns_mutable_array.py
--rw-r--r--   0 runner     (501) staff       (20)     1007 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/ns_mutable_dictionary.py
--rw-r--r--   0 runner     (501) staff       (20)      301 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/objc_lib.m
--rw-r--r--   0 runner     (501) staff       (20)     1407 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/osx_ios_sysinfo.py
--rw-r--r--   0 runner     (501) staff       (20)     2527 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/pointer_to_type.py
--rw-r--r--   0 runner     (501) staff       (20)     1820 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/properties.py
--rw-r--r--   0 runner     (501) staff       (20)     1889 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/unions.py
--rw-r--r--   0 runner     (501) staff       (20)     4222 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/unknown_type.py
--rw-r--r--   0 runner     (501) staff       (20)     1468 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/using_autoclass.py
--rw-r--r--   0 runner     (501) staff       (20)    16011 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/using_carray.py
--rw-r--r--   0 runner     (501) staff       (20)      886 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/using_dylib_manager.py
--rw-r--r--   0 runner     (501) staff       (20)     1675 2022-03-26 18:32:01.000000 pyobjus-1.2.1/examples/using_literals.py
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.432536 pyobjus-1.2.1/objc_classes/
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.456924 pyobjus-1.2.1/objc_classes/aux/
--rw-r--r--   0 runner     (501) staff       (20)     1192 2022-03-26 18:32:01.000000 pyobjus-1.2.1/objc_classes/aux/bridge.h
--rw-r--r--   0 runner     (501) staff       (20)     3836 2022-03-26 18:32:01.000000 pyobjus-1.2.1/objc_classes/aux/bridge.m
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.458663 pyobjus-1.2.1/objc_classes/test/
--rw-r--r--   0 runner     (501) staff       (20)     2941 2022-03-26 18:32:01.000000 pyobjus-1.2.1/objc_classes/test/CArrayTestlib.h
--rw-r--r--   0 runner     (501) staff       (20)    14253 2022-03-26 18:32:01.000000 pyobjus-1.2.1/objc_classes/test/CArrayTestlib.m
--rw-r--r--   0 runner     (501) staff       (20)    11458 2022-03-26 18:32:01.000000 pyobjus-1.2.1/objc_classes/test/testlib.m
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.465709 pyobjus-1.2.1/pyobjus/
--rw-r--r--   0 runner     (501) staff       (20)       45 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/__init__.py
--rw-r--r--   0 runner     (501) staff       (20)     2396 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/_runtime.h
--rw-r--r--   0 runner     (501) staff       (20)     5221 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/common.pxi
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.468724 pyobjus-1.2.1/pyobjus/consts/
--rw-r--r--   0 runner     (501) staff       (20)     6322 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/consts/__init__.py
--rw-r--r--   0 runner     (501) staff       (20)      530 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/consts/corebluetooth.py
--rw-r--r--   0 runner     (501) staff       (20)      359 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/debug.pxi
--rw-r--r--   0 runner     (501) staff       (20)     9974 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/dylib_manager.py
--rw-r--r--   0 runner     (501) staff       (20)     8058 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/objc_py_types.py
--rw-r--r--   0 runner     (501) staff       (20)   142184 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/protocols.py
--rw-r--r--   0 runner     (501) staff       (20)    40132 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/pyobjus.pyx
--rw-r--r--   0 runner     (501) staff       (20)    27077 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/pyobjus_conversions.pxi
--rw-r--r--   0 runner     (501) staff       (20)    26696 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/pyobjus_types.pxi
--rw-r--r--   0 runner     (501) staff       (20)     5444 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyobjus/type_enc.pxi
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.467739 pyobjus-1.2.1/pyobjus.egg-info/
--rw-r--r--   0 runner     (501) staff       (20)      651 2022-03-26 18:32:13.000000 pyobjus-1.2.1/pyobjus.egg-info/PKG-INFO
--rw-r--r--   0 runner     (501) staff       (20)     1926 2022-03-26 18:32:13.000000 pyobjus-1.2.1/pyobjus.egg-info/SOURCES.txt
--rw-r--r--   0 runner     (501) staff       (20)        1 2022-03-26 18:32:13.000000 pyobjus-1.2.1/pyobjus.egg-info/dependency_links.txt
--rw-r--r--   0 runner     (501) staff       (20)        8 2022-03-26 18:32:13.000000 pyobjus-1.2.1/pyobjus.egg-info/top_level.txt
--rw-r--r--   0 runner     (501) staff       (20)       71 2022-03-26 18:32:01.000000 pyobjus-1.2.1/pyproject.toml
--rw-r--r--   0 runner     (501) staff       (20)       38 2022-03-26 18:32:13.478385 pyobjus-1.2.1/setup.cfg
--rw-r--r--   0 runner     (501) staff       (20)     4787 2022-03-26 18:32:01.000000 pyobjus-1.2.1/setup.py
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.476574 pyobjus-1.2.1/tests/
--rw-r--r--   0 runner     (501) staff       (20)    10796 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_carray.py
--rw-r--r--   0 runner     (501) staff       (20)     4203 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_delegate.py
--rw-r--r--   0 runner     (501) staff       (20)      754 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_dereference.py
--rw-r--r--   0 runner     (501) staff       (20)      941 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_literals.py
--rw-r--r--   0 runner     (501) staff       (20)     1578 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_ns_mutable_array.py
--rw-r--r--   0 runner     (501) staff       (20)     1132 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_nsarray.py
--rw-r--r--   0 runner     (501) staff       (20)     1549 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_nsobject.py
--rw-r--r--   0 runner     (501) staff       (20)     3397 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_nsstring.py
--rw-r--r--   0 runner     (501) staff       (20)     2739 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_nsvalue.py
--rw-r--r--   0 runner     (501) staff       (20)      506 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_partial_load.py
--rw-r--r--   0 runner     (501) staff       (20)     1561 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_properties.py
--rw-r--r--   0 runner     (501) staff       (20)      498 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_simple.py
--rw-r--r--   0 runner     (501) staff       (20)     1181 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_union.py
--rw-r--r--   0 runner     (501) staff       (20)     1371 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tests/test_unknown_types.py
-drwxr-xr-x   0 runner     (501) staff       (20)        0 2022-03-26 18:32:13.477099 pyobjus-1.2.1/tools/
--rw-r--r--   0 runner     (501) staff       (20)     6290 2022-03-26 18:32:01.000000 pyobjus-1.2.1/tools/buildprotocols.py
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.818585 pyobjus-1.2.2/
+-rw-r--r--   0 runner     (501) staff       (20)     1081 2023-05-13 11:52:21.000000 pyobjus-1.2.2/LICENSE
+-rw-r--r--   0 runner     (501) staff       (20)      174 2023-05-13 11:52:21.000000 pyobjus-1.2.2/MANIFEST.in
+-rw-r--r--   0 runner     (501) staff       (20)      755 2023-05-13 11:52:21.000000 pyobjus-1.2.2/Makefile
+-rw-r--r--   0 runner     (501) staff       (20)      622 2023-05-13 11:52:34.818163 pyobjus-1.2.2/PKG-INFO
+-rw-r--r--   0 runner     (501) staff       (20)     3542 2023-05-13 11:52:21.000000 pyobjus-1.2.2/README.md
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.782159 pyobjus-1.2.2/docs/
+-rw-r--r--   0 runner     (501) staff       (20)     5577 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/Makefile
+-rw-r--r--   0 runner     (501) staff       (20)     5107 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/make.bat
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.787179 pyobjus-1.2.2/docs/source/
+-rw-r--r--   0 runner     (501) staff       (20)    11291 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/api.rst
+-rw-r--r--   0 runner     (501) staff       (20)     7788 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/conf.py
+-rw-r--r--   0 runner     (501) staff       (20)    33692 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/core_tutorials.rst
+-rw-r--r--   0 runner     (501) staff       (20)     6855 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/foundation_eg.rst
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.788497 pyobjus-1.2.2/docs/source/images/
+-rw-r--r--   0 runner     (501) staff       (20)    70057 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/images/IMG_0322.PNG
+-rw-r--r--   0 runner     (501) staff       (20)    47645 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/images/IMG_0330.PNG
+-rw-r--r--   0 runner     (501) staff       (20)      809 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/index.rst
+-rw-r--r--   0 runner     (501) staff       (20)      619 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/installation.rst
+-rw-r--r--   0 runner     (501) staff       (20)     8076 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/pyobjus_internal.rst
+-rw-r--r--   0 runner     (501) staff       (20)    15991 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/pyobjus_ios.rst
+-rw-r--r--   0 runner     (501) staff       (20)     2247 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/quickstart.rst
+-rw-r--r--   0 runner     (501) staff       (20)      267 2023-05-13 11:52:21.000000 pyobjus-1.2.2/docs/source/remarks.rst
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.797410 pyobjus-1.2.2/examples/
+-rw-r--r--   0 runner     (501) staff       (20)     4770 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/background_transfer.py
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.798846 pyobjus-1.2.2/examples/ball-example/
+-rw-r--r--   0 runner     (501) staff       (20)      116 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ball-example/README.md
+-rw-r--r--   0 runner     (501) staff       (20)     2735 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ball-example/main.py
+-rw-r--r--   0 runner     (501) staff       (20)      738 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ball-example/pyobjusball.kv
+-rw-r--r--   0 runner     (501) staff       (20)     1011 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/classes_and_selectors.py
+-rw-r--r--   0 runner     (501) staff       (20)     1459 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/delegate.py
+-rw-r--r--   0 runner     (501) staff       (20)      513 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ns_alert.py
+-rw-r--r--   0 runner     (501) staff       (20)      575 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ns_array.py
+-rw-r--r--   0 runner     (501) staff       (20)      636 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ns_dictionary.py
+-rw-r--r--   0 runner     (501) staff       (20)     1074 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ns_mutable_array.py
+-rw-r--r--   0 runner     (501) staff       (20)     1007 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/ns_mutable_dictionary.py
+-rw-r--r--   0 runner     (501) staff       (20)      301 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/objc_lib.m
+-rw-r--r--   0 runner     (501) staff       (20)     1407 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/osx_ios_sysinfo.py
+-rw-r--r--   0 runner     (501) staff       (20)     2527 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/pointer_to_type.py
+-rw-r--r--   0 runner     (501) staff       (20)     1820 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/properties.py
+-rw-r--r--   0 runner     (501) staff       (20)     1889 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/unions.py
+-rw-r--r--   0 runner     (501) staff       (20)     4222 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/unknown_type.py
+-rw-r--r--   0 runner     (501) staff       (20)     1468 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/using_autoclass.py
+-rw-r--r--   0 runner     (501) staff       (20)    16011 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/using_carray.py
+-rw-r--r--   0 runner     (501) staff       (20)      886 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/using_dylib_manager.py
+-rw-r--r--   0 runner     (501) staff       (20)     1675 2023-05-13 11:52:21.000000 pyobjus-1.2.2/examples/using_literals.py
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.777306 pyobjus-1.2.2/objc_classes/
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.799744 pyobjus-1.2.2/objc_classes/aux/
+-rw-r--r--   0 runner     (501) staff       (20)     1192 2023-05-13 11:52:21.000000 pyobjus-1.2.2/objc_classes/aux/bridge.h
+-rw-r--r--   0 runner     (501) staff       (20)     3836 2023-05-13 11:52:21.000000 pyobjus-1.2.2/objc_classes/aux/bridge.m
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.801273 pyobjus-1.2.2/objc_classes/test/
+-rw-r--r--   0 runner     (501) staff       (20)     2941 2023-05-13 11:52:21.000000 pyobjus-1.2.2/objc_classes/test/CArrayTestlib.h
+-rw-r--r--   0 runner     (501) staff       (20)    14253 2023-05-13 11:52:21.000000 pyobjus-1.2.2/objc_classes/test/CArrayTestlib.m
+-rw-r--r--   0 runner     (501) staff       (20)    11458 2023-05-13 11:52:21.000000 pyobjus-1.2.2/objc_classes/test/testlib.m
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.807706 pyobjus-1.2.2/pyobjus/
+-rw-r--r--   0 runner     (501) staff       (20)       45 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/__init__.py
+-rw-r--r--   0 runner     (501) staff       (20)     2396 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/_runtime.h
+-rw-r--r--   0 runner     (501) staff       (20)     5221 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/common.pxi
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.810562 pyobjus-1.2.2/pyobjus/consts/
+-rw-r--r--   0 runner     (501) staff       (20)     6322 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/consts/__init__.py
+-rw-r--r--   0 runner     (501) staff       (20)      530 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/consts/corebluetooth.py
+-rw-r--r--   0 runner     (501) staff       (20)      359 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/debug.pxi
+-rw-r--r--   0 runner     (501) staff       (20)     9974 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/dylib_manager.py
+-rw-r--r--   0 runner     (501) staff       (20)     8058 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/objc_py_types.py
+-rw-r--r--   0 runner     (501) staff       (20)   142184 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/protocols.py
+-rw-r--r--   0 runner     (501) staff       (20)    40132 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/pyobjus.pyx
+-rw-r--r--   0 runner     (501) staff       (20)    27077 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/pyobjus_conversions.pxi
+-rw-r--r--   0 runner     (501) staff       (20)    26696 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/pyobjus_types.pxi
+-rw-r--r--   0 runner     (501) staff       (20)     5444 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyobjus/type_enc.pxi
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.809623 pyobjus-1.2.2/pyobjus.egg-info/
+-rw-r--r--   0 runner     (501) staff       (20)      622 2023-05-13 11:52:34.000000 pyobjus-1.2.2/pyobjus.egg-info/PKG-INFO
+-rw-r--r--   0 runner     (501) staff       (20)     1926 2023-05-13 11:52:34.000000 pyobjus-1.2.2/pyobjus.egg-info/SOURCES.txt
+-rw-r--r--   0 runner     (501) staff       (20)        1 2023-05-13 11:52:34.000000 pyobjus-1.2.2/pyobjus.egg-info/dependency_links.txt
+-rw-r--r--   0 runner     (501) staff       (20)        8 2023-05-13 11:52:34.000000 pyobjus-1.2.2/pyobjus.egg-info/top_level.txt
+-rw-r--r--   0 runner     (501) staff       (20)       71 2023-05-13 11:52:21.000000 pyobjus-1.2.2/pyproject.toml
+-rw-r--r--   0 runner     (501) staff       (20)       38 2023-05-13 11:52:34.818706 pyobjus-1.2.2/setup.cfg
+-rw-r--r--   0 runner     (501) staff       (20)     4838 2023-05-13 11:52:21.000000 pyobjus-1.2.2/setup.py
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.817104 pyobjus-1.2.2/tests/
+-rw-r--r--   0 runner     (501) staff       (20)    10796 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_carray.py
+-rw-r--r--   0 runner     (501) staff       (20)     4203 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_delegate.py
+-rw-r--r--   0 runner     (501) staff       (20)      754 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_dereference.py
+-rw-r--r--   0 runner     (501) staff       (20)      941 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_literals.py
+-rw-r--r--   0 runner     (501) staff       (20)     1578 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_ns_mutable_array.py
+-rw-r--r--   0 runner     (501) staff       (20)     1132 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_nsarray.py
+-rw-r--r--   0 runner     (501) staff       (20)     1549 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_nsobject.py
+-rw-r--r--   0 runner     (501) staff       (20)     3397 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_nsstring.py
+-rw-r--r--   0 runner     (501) staff       (20)     2739 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_nsvalue.py
+-rw-r--r--   0 runner     (501) staff       (20)      506 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_partial_load.py
+-rw-r--r--   0 runner     (501) staff       (20)     1561 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_properties.py
+-rw-r--r--   0 runner     (501) staff       (20)      498 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_simple.py
+-rw-r--r--   0 runner     (501) staff       (20)     1181 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_union.py
+-rw-r--r--   0 runner     (501) staff       (20)     1371 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tests/test_unknown_types.py
+drwxr-xr-x   0 runner     (501) staff       (20)        0 2023-05-13 11:52:34.817571 pyobjus-1.2.2/tools/
+-rw-r--r--   0 runner     (501) staff       (20)     6290 2023-05-13 11:52:21.000000 pyobjus-1.2.2/tools/buildprotocols.py
```

### Comparing `pyobjus-1.2.1/LICENSE` & `pyobjus-1.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/Makefile` & `pyobjus-1.2.2/Makefile`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/PKG-INFO` & `pyobjus-1.2.2/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,21 +1,15 @@
 Metadata-Version: 2.1
 Name: pyobjus
-Version: 1.2.1
-Summary: UNKNOWN
-Home-page: UNKNOWN
-License: UNKNOWN
-Platform: UNKNOWN
+Version: 1.2.2
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Operating System :: MacOS
-Classifier: Programming Language :: Python :: 2.7
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
 License-File: LICENSE
-
-UNKNOWN
-
```

### Comparing `pyobjus-1.2.1/README.md` & `pyobjus-1.2.2/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -31,19 +31,17 @@
 ## Support
 
 If you need assistance, you can ask for help on our mailing list:
 
 * User Group : https://groups.google.com/group/kivy-users
 * Email      : kivy-users@googlegroups.com
 
-We also have an IRC channel:
+We also have a Discord server:
 
-* Server  : irc.freenode.net
-* Port    : 6667, 6697 (SSL only)
-* Channel : #kivy
+[https://chat.kivy.org/](https://chat.kivy.org/)
 
 
 ## Contributing
 
 We love pull requests and discussing novel ideas. Check out our
 [contribution guide](http://kivy.org/docs/contribute.html) and
 feel free to improve Pyobjus.
```

#### html2text {}

```diff
@@ -6,29 +6,28 @@
 sponsors/badge.svg)](#sponsors) ## Quick overview ```python from pyobjus import
 autoclass, objc_str from pyobjus.dylib_manager import load_framework, INCLUDE #
 load AppKit framework into pyojbus load_framework(INCLUDE.AppKit) # get nsalert
 class NSAlert = autoclass('NSAlert') # create an NSAlert object, and show it.
 alert = NSAlert.alloc().init() alert.setMessageText_(objc_str('Hello world!'))
 alert.runModal() ``` ## Support If you need assistance, you can ask for help on
 our mailing list: * User Group : https://groups.google.com/group/kivy-users *
-Email : kivy-users@googlegroups.com We also have an IRC channel: * Server :
-irc.freenode.net * Port : 6667, 6697 (SSL only) * Channel : #kivy ##
-Contributing We love pull requests and discussing novel ideas. Check out our
-[contribution guide](http://kivy.org/docs/contribute.html) and feel free to
-improve Pyobjus. The following mailing list and IRC channel are used
-exclusively for discussions about developing the Kivy framework and its sister
-projects: * Dev Group : https://groups.google.com/group/kivy-dev * Email :
-kivy-dev@googlegroups.com Discord channel: * Server : https://chat.kivy.org *
-Channel : #dev ## License Pyobjus is released under the terms of the MIT
-License. Please refer to the LICENSE file. ## Backers Thank you to all our
-backers! ð [[Become a backer](https://opencollective.com/kivy#backer)]
-[https://opencollective.com/kivy/backers.svg?width=890] ## Sponsors Support
-this project by becoming a sponsor. Your logo will show up here with a link to
-your website. [[Become a sponsor](https://opencollective.com/kivy#sponsor)]
-[https://opencollective.com/kivy/sponsor/0/avatar.svg] [https://
-opencollective.com/kivy/sponsor/1/avatar.svg] [https://opencollective.com/kivy/
-sponsor/2/avatar.svg] [https://opencollective.com/kivy/sponsor/3/avatar.svg]
-[https://opencollective.com/kivy/sponsor/4/avatar.svg] [https://
-opencollective.com/kivy/sponsor/5/avatar.svg] [https://opencollective.com/kivy/
-sponsor/6/avatar.svg] [https://opencollective.com/kivy/sponsor/7/avatar.svg]
-[https://opencollective.com/kivy/sponsor/8/avatar.svg] [https://
-opencollective.com/kivy/sponsor/9/avatar.svg]
+Email : kivy-users@googlegroups.com We also have a Discord server: [https://
+chat.kivy.org/](https://chat.kivy.org/) ## Contributing We love pull requests
+and discussing novel ideas. Check out our [contribution guide](http://kivy.org/
+docs/contribute.html) and feel free to improve Pyobjus. The following mailing
+list and IRC channel are used exclusively for discussions about developing the
+Kivy framework and its sister projects: * Dev Group : https://
+groups.google.com/group/kivy-dev * Email : kivy-dev@googlegroups.com Discord
+channel: * Server : https://chat.kivy.org * Channel : #dev ## License Pyobjus
+is released under the terms of the MIT License. Please refer to the LICENSE
+file. ## Backers Thank you to all our backers! ð [[Become a backer](https://
+opencollective.com/kivy#backer)] [https://opencollective.com/kivy/
+backers.svg?width=890] ## Sponsors Support this project by becoming a sponsor.
+Your logo will show up here with a link to your website. [[Become a sponsor]
+(https://opencollective.com/kivy#sponsor)] [https://opencollective.com/kivy/
+sponsor/0/avatar.svg] [https://opencollective.com/kivy/sponsor/1/avatar.svg]
+[https://opencollective.com/kivy/sponsor/2/avatar.svg] [https://
+opencollective.com/kivy/sponsor/3/avatar.svg] [https://opencollective.com/kivy/
+sponsor/4/avatar.svg] [https://opencollective.com/kivy/sponsor/5/avatar.svg]
+[https://opencollective.com/kivy/sponsor/6/avatar.svg] [https://
+opencollective.com/kivy/sponsor/7/avatar.svg] [https://opencollective.com/kivy/
+sponsor/8/avatar.svg] [https://opencollective.com/kivy/sponsor/9/avatar.svg]
```

### Comparing `pyobjus-1.2.1/docs/Makefile` & `pyobjus-1.2.2/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/make.bat` & `pyobjus-1.2.2/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/api.rst` & `pyobjus-1.2.2/docs/source/api.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/conf.py` & `pyobjus-1.2.2/docs/source/conf.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/core_tutorials.rst` & `pyobjus-1.2.2/docs/source/core_tutorials.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/foundation_eg.rst` & `pyobjus-1.2.2/docs/source/foundation_eg.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/images/IMG_0322.PNG` & `pyobjus-1.2.2/docs/source/images/IMG_0322.PNG`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/images/IMG_0330.PNG` & `pyobjus-1.2.2/docs/source/images/IMG_0330.PNG`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/index.rst` & `pyobjus-1.2.2/docs/source/index.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/installation.rst` & `pyobjus-1.2.2/docs/source/installation.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/pyobjus_internal.rst` & `pyobjus-1.2.2/docs/source/pyobjus_internal.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/pyobjus_ios.rst` & `pyobjus-1.2.2/docs/source/pyobjus_ios.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/docs/source/quickstart.rst` & `pyobjus-1.2.2/docs/source/quickstart.rst`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/background_transfer.py` & `pyobjus-1.2.2/examples/background_transfer.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ball-example/main.py` & `pyobjus-1.2.2/examples/ball-example/main.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ball-example/pyobjusball.kv` & `pyobjus-1.2.2/examples/ball-example/pyobjusball.kv`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/classes_and_selectors.py` & `pyobjus-1.2.2/examples/classes_and_selectors.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/delegate.py` & `pyobjus-1.2.2/examples/delegate.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ns_alert.py` & `pyobjus-1.2.2/examples/ns_alert.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ns_array.py` & `pyobjus-1.2.2/examples/ns_array.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ns_dictionary.py` & `pyobjus-1.2.2/examples/ns_dictionary.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ns_mutable_array.py` & `pyobjus-1.2.2/examples/ns_mutable_array.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/ns_mutable_dictionary.py` & `pyobjus-1.2.2/examples/ns_mutable_dictionary.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/osx_ios_sysinfo.py` & `pyobjus-1.2.2/examples/osx_ios_sysinfo.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/pointer_to_type.py` & `pyobjus-1.2.2/examples/pointer_to_type.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/properties.py` & `pyobjus-1.2.2/examples/properties.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/unions.py` & `pyobjus-1.2.2/examples/unions.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/unknown_type.py` & `pyobjus-1.2.2/examples/unknown_type.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/using_autoclass.py` & `pyobjus-1.2.2/examples/using_autoclass.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/using_carray.py` & `pyobjus-1.2.2/examples/using_carray.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/using_dylib_manager.py` & `pyobjus-1.2.2/examples/using_dylib_manager.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/examples/using_literals.py` & `pyobjus-1.2.2/examples/using_literals.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/objc_classes/aux/bridge.h` & `pyobjus-1.2.2/objc_classes/aux/bridge.h`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/objc_classes/aux/bridge.m` & `pyobjus-1.2.2/objc_classes/aux/bridge.m`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/objc_classes/test/CArrayTestlib.h` & `pyobjus-1.2.2/objc_classes/test/CArrayTestlib.h`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/objc_classes/test/CArrayTestlib.m` & `pyobjus-1.2.2/objc_classes/test/CArrayTestlib.m`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/objc_classes/test/testlib.m` & `pyobjus-1.2.2/objc_classes/test/testlib.m`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/_runtime.h` & `pyobjus-1.2.2/pyobjus/_runtime.h`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/common.pxi` & `pyobjus-1.2.2/pyobjus/common.pxi`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/consts/__init__.py` & `pyobjus-1.2.2/pyobjus/consts/__init__.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/consts/corebluetooth.py` & `pyobjus-1.2.2/pyobjus/consts/corebluetooth.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/dylib_manager.py` & `pyobjus-1.2.2/pyobjus/dylib_manager.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/objc_py_types.py` & `pyobjus-1.2.2/pyobjus/objc_py_types.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/protocols.py` & `pyobjus-1.2.2/pyobjus/protocols.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/pyobjus.pyx` & `pyobjus-1.2.2/pyobjus/pyobjus.pyx`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/pyobjus_conversions.pxi` & `pyobjus-1.2.2/pyobjus/pyobjus_conversions.pxi`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/pyobjus_types.pxi` & `pyobjus-1.2.2/pyobjus/pyobjus_types.pxi`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus/type_enc.pxi` & `pyobjus-1.2.2/pyobjus/type_enc.pxi`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/pyobjus.egg-info/PKG-INFO` & `pyobjus-1.2.2/pyobjus.egg-info/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,21 +1,15 @@
 Metadata-Version: 2.1
 Name: pyobjus
-Version: 1.2.1
-Summary: UNKNOWN
-Home-page: UNKNOWN
-License: UNKNOWN
-Platform: UNKNOWN
+Version: 1.2.2
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Operating System :: MacOS
-Classifier: Programming Language :: Python :: 2.7
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
 License-File: LICENSE
-
-UNKNOWN
-
```

### Comparing `pyobjus-1.2.1/pyobjus.egg-info/SOURCES.txt` & `pyobjus-1.2.2/pyobjus.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/setup.py` & `pyobjus-1.2.2/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -130,14 +130,15 @@
     ],
     classifiers=[
         'Development Status :: 4 - Beta',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Natural Language :: English',
         'Operating System :: MacOS',
-        'Programming Language :: Python :: 2.7',
-        'Programming Language :: Python :: 3.5',
-        'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
+        'Programming Language :: Python :: 3.8',
+        'Programming Language :: Python :: 3.9',
+        'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Topic :: Software Development :: Libraries :: Application Frameworks'
     ],
 )
```

### Comparing `pyobjus-1.2.1/tests/test_carray.py` & `pyobjus-1.2.2/tests/test_carray.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_delegate.py` & `pyobjus-1.2.2/tests/test_delegate.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_dereference.py` & `pyobjus-1.2.2/tests/test_dereference.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_literals.py` & `pyobjus-1.2.2/tests/test_literals.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_ns_mutable_array.py` & `pyobjus-1.2.2/tests/test_ns_mutable_array.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_nsarray.py` & `pyobjus-1.2.2/tests/test_nsarray.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_nsobject.py` & `pyobjus-1.2.2/tests/test_nsobject.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_nsstring.py` & `pyobjus-1.2.2/tests/test_nsstring.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_nsvalue.py` & `pyobjus-1.2.2/tests/test_nsvalue.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_properties.py` & `pyobjus-1.2.2/tests/test_properties.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_union.py` & `pyobjus-1.2.2/tests/test_union.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tests/test_unknown_types.py` & `pyobjus-1.2.2/tests/test_unknown_types.py`

 * *Files identical despite different names*

### Comparing `pyobjus-1.2.1/tools/buildprotocols.py` & `pyobjus-1.2.2/tools/buildprotocols.py`

 * *Files identical despite different names*

