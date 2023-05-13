# Comparing `tmp/pyjnius-1.4.2.tar.gz` & `tmp/pyjnius-1.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyjnius-1.4.2.tar", last modified: Sun Jul  3 19:16:55 2022, max compression
+gzip compressed data, was "pyjnius-1.5.0.tar", last modified: Sat May 13 08:38:56 2023, max compression
```

## Comparing `pyjnius-1.4.2.tar` & `pyjnius-1.5.0.tar`

### file list

```diff
@@ -1,42 +1,79 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.558696 pyjnius-1.4.2/
--rw-r--r--   0 runner    (1001) docker     (121)     1081 2022-07-03 19:16:50.000000 pyjnius-1.4.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       53 2022-07-03 19:16:50.000000 pyjnius-1.4.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)    10228 2022-07-03 19:16:55.558696 pyjnius-1.4.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     9146 2022-07-03 19:16:50.000000 pyjnius-1.4.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.558696 pyjnius-1.4.2/jnius/
--rw-r--r--   0 runner    (1001) docker     (121)     2447 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)       56 2022-07-03 19:16:54.000000 pyjnius-1.4.2/jnius/config.pxi
--rw-r--r--   0 runner    (1001) docker     (121)    10779 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/env.py
--rw-r--r--   0 runner    (1001) docker     (121)    22170 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jni.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     2608 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius.pyx
--rw-r--r--   0 runner    (1001) docker     (121)      967 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_compat.pxi
--rw-r--r--   0 runner    (1001) docker     (121)    31546 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_conversion.pxi
--rw-r--r--   0 runner    (1001) docker     (121)      616 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_env.pxi
--rw-r--r--   0 runner    (1001) docker     (121)    43873 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_export_class.pxi
--rw-r--r--   0 runner    (1001) docker     (121)      887 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_export_func.pxi
--rw-r--r--   0 runner    (1001) docker     (121)      181 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_jvm_android.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     2702 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_jvm_desktop.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     2922 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_jvm_dlopen.pxi
--rw-r--r--   0 runner    (1001) docker     (121)      666 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_localref.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     2387 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_nativetypes.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     2265 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_nativetypes3.pxi
--rw-r--r--   0 runner    (1001) docker     (121)     6796 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_proxy.pxi
--rw-r--r--   0 runner    (1001) docker     (121)    18968 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/jnius_utils.pxi
--rw-r--r--   0 runner    (1001) docker     (121)    18170 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/reflect.py
--rw-r--r--   0 runner    (1001) docker     (121)     2766 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/signatures.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.554696 pyjnius-1.4.2/jnius/src/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.554696 pyjnius-1.4.2/jnius/src/org/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.558696 pyjnius-1.4.2/jnius/src/org/jnius/
--rw-r--r--   0 runner    (1001) docker     (121)     1084 2022-07-03 19:16:54.000000 pyjnius-1.4.2/jnius/src/org/jnius/NativeInvocationHandler.class
--rw-r--r--   0 runner    (1001) docker     (121)     1134 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius/src/org/jnius/NativeInvocationHandler.java
--rw-r--r--   0 runner    (1001) docker     (121)     2470 2022-07-03 19:16:50.000000 pyjnius-1.4.2/jnius_config.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-07-03 19:16:55.558696 pyjnius-1.4.2/pyjnius.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)    10228 2022-07-03 19:16:54.000000 pyjnius-1.4.2/pyjnius.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      798 2022-07-03 19:16:55.000000 pyjnius-1.4.2/pyjnius.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-07-03 19:16:55.000000 pyjnius-1.4.2/pyjnius.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       85 2022-07-03 19:16:55.000000 pyjnius-1.4.2/pyjnius.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       31 2022-07-03 19:16:55.000000 pyjnius-1.4.2/pyjnius.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       90 2022-07-03 19:16:50.000000 pyjnius-1.4.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)      186 2022-07-03 19:16:55.558696 pyjnius-1.4.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     3058 2022-07-03 19:16:50.000000 pyjnius-1.4.2/setup.py
--rw-r--r--   0 runner    (1001) docker     (121)     2066 2022-07-03 19:16:50.000000 pyjnius-1.4.2/setup_sdist.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.808036 pyjnius-1.5.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-05-13 08:38:51.000000 pyjnius-1.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 08:38:51.000000 pyjnius-1.5.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    10229 2023-05-13 08:38:56.808036 pyjnius-1.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9146 2023-05-13 08:38:51.000000 pyjnius-1.5.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.800036 pyjnius-1.5.0/jnius/
+-rw-r--r--   0 runner    (1001) docker     (123)     2409 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-13 08:38:56.000000 pyjnius-1.5.0/jnius/config.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)    11453 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/env.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22170 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jni.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius.pyx
+-rw-r--r--   0 runner    (1001) docker     (123)      801 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_compat.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)    30439 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_conversion.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_env.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)    43401 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_export_class.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)      735 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_export_func.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_jvm_android.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_jvm_desktop.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)     2723 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_jvm_dlopen.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)      666 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_localref.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)     2265 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_nativetypes3.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)     6716 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_proxy.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)    18404 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/jnius_utils.pxi
+-rw-r--r--   0 runner    (1001) docker     (123)    17457 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/reflect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2766 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/signatures.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.796036 pyjnius-1.5.0/jnius/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.796036 pyjnius-1.5.0/jnius/src/org/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.800036 pyjnius-1.5.0/jnius/src/org/jnius/
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-13 08:38:56.000000 pyjnius-1.5.0/jnius/src/org/jnius/NativeInvocationHandler.class
+-rw-r--r--   0 runner    (1001) docker     (123)     1134 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius/src/org/jnius/NativeInvocationHandler.java
+-rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-05-13 08:38:51.000000 pyjnius-1.5.0/jnius_config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.804036 pyjnius-1.5.0/pyjnius.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    10229 2023-05-13 08:38:56.000000 pyjnius-1.5.0/pyjnius.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-05-13 08:38:56.000000 pyjnius-1.5.0/pyjnius.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:38:56.000000 pyjnius-1.5.0/pyjnius.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-05-13 08:38:56.000000 pyjnius-1.5.0/pyjnius.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-13 08:38:56.000000 pyjnius-1.5.0/pyjnius.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 08:38:51.000000 pyjnius-1.5.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-05-13 08:38:56.808036 pyjnius-1.5.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2955 2023-05-13 08:38:51.000000 pyjnius-1.5.0/setup.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2067 2023-05-13 08:38:51.000000 pyjnius-1.5.0/setup_sdist.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:38:56.808036 pyjnius-1.5.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_arraylist.py
+-rw-r--r--   0 runner    (1001) docker     (123)      664 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_assignable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2212 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_bad_declaration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6212 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_basics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1908 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_bytearray.py
+-rw-r--r--   0 runner    (1001) docker     (123)      774 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_cast.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5667 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_chars_and_strings.py
+-rw-r--r--   0 runner    (1001) docker     (123)      392 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_class_argument.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1438 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_closeable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1439 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_collections.py
+-rw-r--r--   0 runner    (1001) docker     (123)      745 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_comparable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2801 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_constructor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2774 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_dir.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1937 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2516 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_export_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)      951 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_implementation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2707 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_inheritance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_int_vs_long.py
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)      382 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_jnitable_overflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2537 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_jnius_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1188 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_jvm_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1690 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_lambdas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3160 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_method_multiple_signatures.py
+-rw-r--r--   0 runner    (1001) docker     (123)      546 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_multidimension.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2116 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_object_args.py
+-rw-r--r--   0 runner    (1001) docker     (123)      449 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_output_args.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8201 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_pass_by_reference_or_value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4058 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4074 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_reflect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4565 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_simple.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1083 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_static.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11198 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_visibility_all.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4873 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_visibility_package_protected.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6520 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_visibility_public_only.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8307 2023-05-13 08:38:51.000000 pyjnius-1.5.0/tests/test_visibility_public_protected.py
```

### Comparing `pyjnius-1.4.2/LICENSE` & `pyjnius-1.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/PKG-INFO` & `pyjnius-1.5.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 Metadata-Version: 2.1
 Name: pyjnius
-Version: 1.4.2
+Version: 1.5.0
 Summary: A Python module to access Java classes as Python classes using JNI.
 Home-page: https://github.com/kivy/pyjnius
 Author: Kivy Team and other contributors
 Author-email: kivy-dev@googlegroups.com
 Keywords: Java JNI Android
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Operating System :: Android
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 Provides-Extra: ci
 License-File: LICENSE
 
 PyJNIus
```

### Comparing `pyjnius-1.4.2/README.md` & `pyjnius-1.5.0/README.md`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/__init__.py` & `pyjnius-1.5.0/jnius/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 =======
 
 Accessing Java classes from Python.
 
 All the documentation is available at: http://pyjnius.readthedocs.org
 '''
 
-__version__ = '1.4.2'
+__version__ = '1.5.0'
 
 from .env import get_java_setup
 
 import os
 import sys
 if sys.platform == 'win32' and sys.version_info >= (3, 8):
     path = os.path.dirname(__file__)
@@ -40,23 +40,21 @@
                     break
         else:
             raise Exception("Unable to create jni env, no jvm dll found.")
 else:
     from .jnius import *  # noqa
     from .reflect import *  # noqa
 
-from six import with_metaclass
-
 # XXX monkey patch methods that cannot be in cython.
 # Cython doesn't allow to set new attribute on methods it compiled
 
 HASHCODE_MAX = 2 ** 31 - 1
 
 
-class PythonJavaClass_(with_metaclass(MetaJavaBase, PythonJavaClass)):
+class PythonJavaClass_(PythonJavaClass, metaclass=MetaJavaBase):
 
     @java_method('()I', name='hashCode')
     def hashCode(self):
         return id(self) % HASHCODE_MAX
 
     @java_method('()Ljava/lang/String;', name='hashCode')
     def hashCode_(self):
```

### Comparing `pyjnius-1.4.2/jnius/env.py` & `pyjnius-1.5.0/jnius/env.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,25 +5,19 @@
 
 import sys
 from os.path import join, exists, dirname, realpath
 from os import getenv
 from platform import machine
 from subprocess import Popen, check_output, PIPE
 from shlex import split
-from logging import getLogger
+import logging
 from textwrap import dedent
+from shutil import which
 
-log = getLogger(__name__)
-
-PY2 = sys.version_info.major < 3
-
-if PY2:
-    from distutils.spawn import find_executable as which
-else:
-    from shutil import which
+log = logging.getLogger('kivy').getChild(__name__)
 
 machine = machine()  # not expected to change at runtime
 
 # This dictionary converts values from platform.machine()
 # to a "cpu" string. It is needed to set the correct lib path,
 # found in the JRE_HOME, e.g.: <JRE_HOME>/lib/<cpu>/.
 MACHINE2CPU = {
@@ -82,14 +76,16 @@
 
     if platform == "android":
         return AndroidJavaLocation(platform, JAVA_HOME)
     if platform == "win32": #only this?
         return WindowsJavaLocation(platform, JAVA_HOME)
     if platform == "darwin": #only this?
         return MacOsXJavaLocation(platform, JAVA_HOME)    
+    if 'bsd' in platform:
+        return BSDJavaLocation(platform, JAVA_HOME)
     if platform in ('linux', 'linux2', 'sunos5'): #only this?
         return UnixJavaLocation(platform, JAVA_HOME)
     log.warning("warning: unknown platform %s assuming linux or sunOS" % platform)
     return UnixJavaLocation(platform, JAVA_HOME)
 
 
 class JavaLocation:
@@ -232,14 +228,37 @@
         return [
             'lib/server/libjvm.so',
             'jre/lib/{}/default/libjvm.so'.format(cpu),
             'jre/lib/{}/server/libjvm.so'.format(cpu),
         ]
 
 
+# NOTE: Build works on FreeBSD. Other BSD flavors may need tuning!
+class BSDJavaLocation(JavaLocation):
+    def _get_platform_include_dir(self):
+        os = self.platform.translate({ord(n): None for n in '0123456789'})
+        return join(self.home, 'include', os)
+
+    def _possible_lib_locations(self):
+        root = self.home
+        if root.endswith('jre'):
+            root = root[:-3]
+
+        cpu = get_cpu()
+        log.debug(
+            f"Platform {self.platform} may need cpu in path to find libjvm, which is: {cpu}"
+        )
+
+        return [
+            'lib/server/libjvm.so',
+            'jre/lib/{}/default/libjvm.so'.format(cpu),
+            'jre/lib/{}/server/libjvm.so'.format(cpu),
+        ]
+
+
 class MacOsXJavaLocation(UnixJavaLocation):
     def _get_platform_include_dir(self):
         return join(self.home, 'include', 'darwin')
 
     def _possible_lib_locations(self):
         if '1.6' in self.home:
             return ['../Libraries/libjvm.dylib'] # TODO what should this be resolved to?
@@ -339,17 +358,15 @@
 
 def get_osx_framework():
     framework = Popen(
         '/usr/libexec/java_home',
         stdout=PIPE, shell=True
     ).communicate()[0]
 
-    if not PY2:
-        framework = framework.decode('utf-8')
-
+    framework = framework.decode('utf-8')
     return framework.strip()
 
 
 def get_cpu():
     try:
         return MACHINE2CPU[machine]
     except KeyError:
```

### Comparing `pyjnius-1.4.2/jnius/jni.pxi` & `pyjnius-1.5.0/jnius/jni.pxi`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/jnius.pyx` & `pyjnius-1.5.0/jnius/jnius.pyx`

 * *Files 6% similar despite different names*

```diff
@@ -106,16 +106,14 @@
 ELSE:
     include "jnius_jvm_dlopen.pxi"
 
 include "jnius_env.pxi"
 include "jnius_utils.pxi"
 include "jnius_conversion.pxi"
 include "jnius_localref.pxi"
-IF JNIUS_PYTHON3:
-    include "jnius_nativetypes3.pxi"
-ELSE:
-    include "jnius_nativetypes.pxi"
+
+include "jnius_nativetypes3.pxi"
 
 include "jnius_export_func.pxi"
 include "jnius_export_class.pxi"
 
 include "jnius_proxy.pxi"
```

### Comparing `pyjnius-1.4.2/jnius/jnius_compat.pxi` & `pyjnius-1.5.0/jnius/jnius_compat.pxi`

 * *Files 20% similar despite different names*

```diff
@@ -1,24 +1,16 @@
 '''
 Handle Python 2 vs 3 differences here.
 '''
 
-from cpython.version cimport PY_MAJOR_VERSION
-
-cdef int PY2 = PY_MAJOR_VERSION < 3
-
 # because Cython's basestring doesn't work with isinstance() properly
 # and has differences between Python 2 and Python 3 runtime behavior
 # so it's not really usable unless some bug in the upstream is fixed
 # (tested with Cython==0.29.2)
-cdef tuple base_string
-if PY_MAJOR_VERSION < 3:
-    base_string = (bytes, unicode)
-else:
-    base_string = (bytes, str)
+cdef tuple base_string = (bytes, str)
 
 
 cdef unicode to_unicode(object arg):
     '''
     Accept full object as a type to prevent py2/py3 differences
     and throw an exception in case of misusing this function.
     '''
```

### Comparing `pyjnius-1.4.2/jnius/jnius_conversion.pxi` & `pyjnius-1.5.0/jnius/jnius_conversion.pxi`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-from cpython.version cimport PY_MAJOR_VERSION
-
 activeLambdaJavaProxies = set()
 
 cdef jstringy_arg(argtype):
     return argtype in ('Ljava/lang/String;',
                        'Ljava/lang/CharSequence;',
                        'Ljava/lang/Object;')
 
@@ -138,20 +136,15 @@
                         'argument. Want {0!r}, got {1!r}'.format(
                             argtype[1:-1], py_arg))
 
         elif argtype[0] == '[':
             if py_arg is None:
                 j_args[index].l = NULL
                 continue
-            if isinstance(py_arg, basestring) and PY_MAJOR_VERSION < 3:
-                if argtype == '[B':
-                    py_arg = map(ord, py_arg)
-                elif argtype == '[C':
-                    py_arg = list(py_arg)
-            if isinstance(py_arg, str) and PY_MAJOR_VERSION >= 3 and argtype == '[C':
+            if isinstance(py_arg, str) and argtype == '[C':
                 py_arg = list(py_arg)
             if isinstance(py_arg, ByteArray) and argtype != '[B':
                 raise JavaException(
                     'Cannot use ByteArray for signature {}'.format(argtype))
             if not isinstance(py_arg, (list, tuple, ByteArray, bytes, bytearray)):
                 raise JavaException('Expecting a python list/tuple, got '
                         '{0!r}'.format(py_arg))
@@ -256,18 +249,15 @@
         j_strlen = j_env[0].GetStringLength(j_env, j_string);
 
         buffsize = j_strlen * sizeof(jchar)
         py_uni = (<char *>j_chars)[:buffsize].decode('utf-16')
     finally:
         j_env[0].ReleaseStringChars(j_env, j_string, j_chars)
 
-    if PY_MAJOR_VERSION < 3:
-        return py_uni.encode('utf-8')
-    else:
-        return py_uni
+    return py_uni
 
 cdef convert_jarray_to_python(JNIEnv *j_env, definition, jobject j_object):
     cdef jboolean iscopy
     cdef jboolean *j_booleans
     cdef jbyte *j_bytes
     cdef jchar *j_chars
     cdef jshort *j_shorts
@@ -307,18 +297,15 @@
         ret_as_bytearray.set_buffer(j_env, j_object, array_size, j_bytes)
         return ret_as_bytearray
 
     elif r == 'C':
         j_chars = j_env[0].GetCharArrayElements(
                 j_env, j_object, &iscopy)
 
-        if PY_MAJOR_VERSION < 3:
-            ret = [chr(<char>j_chars[i]) for i in range(array_size)]
-        else:
-            ret = [chr(j_chars[i]) for i in range(array_size)]
+        ret = [chr(j_chars[i]) for i in range(array_size)]
         j_env[0].ReleaseCharArrayElements(
                 j_env, j_object, j_chars, 0)
 
     elif r == 'S':
         j_shorts = j_env[0].GetShortArrayElements(
                 j_env, j_object, &iscopy)
         ret = [(<short>j_shorts[i]) for i in range(array_size)]
@@ -547,32 +534,22 @@
 
         else:
             raise JavaException('Invalid python object for this '
                     'argument. Want {0!r}, got {1!r}'.format(
                         definition[1:-1], obj))
 
     elif definition[0] == '[':
-        if PY_MAJOR_VERSION < 3:
-            conversions = {
-                int: 'I',
-                bool: 'Z',
-                long: 'J',
-                float: 'F',
-                unicode: 'Ljava/lang/String;',
-                bytes: 'Ljava/lang/String;'
-            }
-        else:
-            conversions = {
-                int: 'I',
-                bool: 'Z',
-                long: 'J',
-                float: 'F',
-                unicode: 'Ljava/lang/String;',
-                bytes: 'B'
-            }
+        conversions = {
+            int: 'I',
+            bool: 'Z',
+            long: 'J',
+            float: 'F',
+            unicode: 'Ljava/lang/String;',
+            bytes: 'B'
+        }
         retclass = j_env[0].FindClass(j_env, 'java/lang/Object')
         retobject = j_env[0].NewObjectArray(j_env, len(obj), retclass, NULL)
         for index, item in enumerate(obj):
             item_definition = conversions.get(type(item), definition[1:])
             retsubobject = convert_python_to_jobject(
                     j_env, item_definition, item)
             j_env[0].SetObjectArrayElement(j_env, retobject, index,
@@ -657,31 +634,22 @@
     cdef JavaClass jc
 
     cdef ByteArray a_bytes
 
     if definition == 'Ljava/lang/Object;' and len(pyarray) > 0:
         # then the method will accept any array type as param
         # let's be as precise as we can
-        if PY_MAJOR_VERSION < 3:
-            conversions = {
-                int: 'I',
-                bool: 'Z',
-                long: 'J',
-                float: 'F',
-                basestring: 'Ljava/lang/String;',
-            }
-        else:
-            conversions = {
-                int: 'I',
-                bool: 'Z',
-                long: 'J',
-                float: 'F',
-                bytes: 'B',
-                str: 'Ljava/lang/String;',
-            }
+        conversions = {
+            int: 'I',
+            bool: 'Z',
+            long: 'J',
+            float: 'F',
+            bytes: 'B',
+            str: 'Ljava/lang/String;',
+        }
         for _type, override in conversions.iteritems():
             if isinstance(pyarray[0], _type):
                 definition = override
                 break
 
     if definition == 'Z':
         ret = j_env[0].NewBooleanArray(j_env, array_size)
```

### Comparing `pyjnius-1.4.2/jnius/jnius_env.pxi` & `pyjnius-1.5.0/jnius/jnius_env.pxi`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/jnius_export_class.pxi` & `pyjnius-1.5.0/jnius/jnius_export_class.pxi`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 from cpython cimport PyObject
-from cpython.version cimport PY_MAJOR_VERSION
 from warnings import warn
 
 
 class JavaException(Exception):
     '''Can be a real java exception, or just an exception from the wrapper.
     '''
     classname = None     # The classname of the exception
@@ -221,29 +220,29 @@
 
         classDict['__cls_storage'] = jcs
 
         # search all the static JavaMethod within our class, and resolve them
         cdef JavaMethod jm
         cdef JavaMultipleMethod jmm
         cdef jboolean resolve_static = True
-        for name, value in items_compat(classDict):
+        for name, value in classDict.items():
             if isinstance(value, JavaMethod):
                 jm = value
                 if not jm.is_static:
                     continue
                 jm.set_resolve_info(j_env, jcs.j_cls,
                     str_for_c(name), str_for_c(__javaclass__))
             elif isinstance(value, JavaMultipleMethod):
                 jmm = value
                 jmm.set_resolve_info(j_env, jcs.j_cls, resolve_static,
                     str_for_c(name), str_for_c(__javaclass__))
 
         # search all the static JavaField within our class, and resolve them
         cdef JavaField jf
-        for name, value in items_compat(classDict):
+        for name, value in classDict.items():
             if not isinstance(value, JavaField):
                 continue
             jf = value
             if not jf.is_static:
                 continue
             jf.set_resolve_info(j_env, jcs.j_cls,
                 str_for_c(name), str_for_c(__javaclass__))
@@ -399,15 +398,15 @@
 
     cdef void resolve_methods(self) except *:
         # search all the JavaMethod within our class, and resolve them
         cdef JavaMethod jm
         cdef JavaMultipleMethod jmm
         cdef JNIEnv *j_env = get_jnienv()
         cdef jboolean resolve_static = False
-        for name, value in items_compat(self.__class__.__dict__):
+        for name, value in self.__class__.__dict__.items():
             if isinstance(value, JavaMethod):
                 jm = value
                 if jm.is_static:
                     continue
                 jm.set_resolve_info(j_env, self.j_cls,
                     str_for_c(name), str_for_c(self.__javaclass__))
             elif isinstance(value, JavaMultipleMethod):
@@ -415,15 +414,15 @@
                 jmm.set_resolve_info(j_env, self.j_cls, resolve_static,
                     str_for_c(name), str_for_c(self.__javaclass__))
 
     cdef void resolve_fields(self) except *:
         # search all the JavaField within our class, and resolve them
         cdef JavaField jf
         cdef JNIEnv *j_env = get_jnienv()
-        for name, value in items_compat(self.__class__.__dict__):
+        for name, value in self.__class__.__dict__.items():
             if not isinstance(value, JavaField):
                 continue
             jf = value
             if jf.is_static:
                 continue
             jf.set_resolve_info(j_env, self.j_cls,
                 name, self.__javaclass__)
@@ -582,18 +581,15 @@
         elif r == 'B':
             j_byte = j_env[0].GetByteField(
                     j_env, j_self, self.j_field)
             ret = <char>j_byte
         elif r == 'C':
             j_char = j_env[0].GetCharField(
                     j_env, j_self, self.j_field)
-            if PY_MAJOR_VERSION < 3:
-                ret = chr(<char>j_char)
-            else:
-                ret = chr(j_char)
+            ret = chr(j_char)
         elif r == 'S':
             j_short = j_env[0].GetShortField(
                     j_env, j_self, self.j_field)
             ret = <short>j_short
         elif r == 'I':
             j_int = j_env[0].GetIntField(
                     j_env, j_self, self.j_field)
@@ -709,18 +705,15 @@
         elif r == 'B':
             j_byte = j_env[0].GetStaticByteField(
                     j_env, self.j_cls, self.j_field)
             ret = <char>j_byte
         elif r == 'C':
             j_char = j_env[0].GetStaticCharField(
                     j_env, self.j_cls, self.j_field)
-            if PY_MAJOR_VERSION < 3:
-                ret = chr(<char>j_char)
-            else:
-                ret = chr(j_char)
+            ret = chr(j_char)
         elif r == 'S':
             j_short = j_env[0].GetStaticShortField(
                     j_env, self.j_cls, self.j_field)
             ret = <short>j_short
         elif r == 'I':
             j_int = j_env[0].GetStaticIntField(
                     j_env, self.j_cls, self.j_field)
@@ -925,18 +918,15 @@
                 j_byte = j_env[0].CallByteMethodA(
                         j_env, j_self, self.j_method, j_args)
             ret = <char>j_byte
         elif r == 'C':
             with nogil:
                 j_char = j_env[0].CallCharMethodA(
                         j_env, j_self, self.j_method, j_args)
-            if PY_MAJOR_VERSION < 3:
-                ret = chr(<char>j_char)
-            else:
-                ret = chr(j_char)
+            ret = chr(j_char)
         elif r == 'S':
             with nogil:
                 j_short = j_env[0].CallShortMethodA(
                         j_env, j_self, self.j_method, j_args)
             ret = <short>j_short
         elif r == 'I':
             with nogil:
@@ -1016,18 +1006,15 @@
                 j_byte = j_env[0].CallStaticByteMethodA(
                         j_env, self.j_cls, self.j_method, j_args)
             ret = <char>j_byte
         elif r == 'C':
             with nogil:
                 j_char = j_env[0].CallStaticCharMethodA(
                         j_env, self.j_cls, self.j_method, j_args)
-            if PY_MAJOR_VERSION < 3:
-                ret = chr(<char>j_char)
-            else:
-                ret = chr(j_char)
+            ret = chr(j_char)
         elif r == 'S':
             with nogil:
                 j_short = j_env[0].CallStaticShortMethodA(
                         j_env, self.j_cls, self.j_method, j_args)
             ret = <short>j_short
         elif r == 'I':
             with nogil:
@@ -1138,15 +1125,15 @@
         cdef list found_signatures = []
 
         if self.j_self:
             methods = self.instance_methods
         else:
             methods = self.static_methods
 
-        for signature, jm in items_compat(methods):
+        for signature, jm in methods.items():
             # store signatures for the exception
             found_signatures.append(signature)
 
             sign_ret, sign_args = jm.definition_return, jm.definition_args
             if jm.is_varargs:
                 max_sign_args = len(sign_args) - 1
                 args_ = args[:max_sign_args] + (args[max_sign_args:],)
```

### Comparing `pyjnius-1.4.2/jnius/jnius_jvm_desktop.pxi` & `pyjnius-1.5.0/jnius/jnius_jvm_desktop.pxi`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 import sys
 import os
 from os.path import join
 from jnius.env import get_java_setup
-from cpython.version cimport PY_MAJOR_VERSION
 
 # on desktop, we need to create an env :)
 # example taken from http://www.inonit.com/cygwin/jni/invocationApi/c.html
 
 cdef extern jint __stdcall JNI_CreateJavaVM(JavaVM **pvm, void **penv, void *args)
 cdef extern from "jni.h":
     int JNI_VERSION_1_4
```

### Comparing `pyjnius-1.4.2/jnius/jnius_jvm_dlopen.pxi` & `pyjnius-1.5.0/jnius/jnius_jvm_dlopen.pxi`

 * *Files 4% similar despite different names*

```diff
@@ -50,22 +50,15 @@
     cdef bytes py_bytes
     cdef void *handle
     import jnius_config
 
     JAVA_LOCATION = get_java_setup()
     cdef str java_lib = JAVA_LOCATION.get_jnius_lib_location()
 
-    IF JNIUS_PYTHON3:
-        try:
-            java_lib = java_lib.decode("utf-8")
-        except AttributeError:
-            java_lib = java_lib
-        lib_path = str_for_c(java_lib)
-    ELSE:
-        lib_path = str_for_c(java_lib)
+    lib_path = str_for_c(java_lib)
 
     handle = dlopen(lib_path, RTLD_NOW | RTLD_GLOBAL)
 
     if handle == NULL:
         raise SystemError("Error calling dlopen({0}): {1}".format(lib_path, dlerror()))
 
     cdef void *jniCreateJVM = dlsym(handle, b"JNI_CreateJavaVM")
```

### Comparing `pyjnius-1.4.2/jnius/jnius_localref.pxi` & `pyjnius-1.5.0/jnius/jnius_localref.pxi`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/jnius_nativetypes.pxi` & `pyjnius-1.5.0/jnius/jnius_nativetypes3.pxi`

 * *Files 5% similar despite different names*

```diff
@@ -1,35 +1,33 @@
+
 cdef python_op(int op, object a, object b):
     if op == 0:
         return a < b
     elif op == 1:
         return a <= b
     elif op == 2:
         return a == b
     elif op == 3:
         return a >= b
     elif op == 4:
         return a > b
     elif op == 5:
         return a != b
 
-
 cdef class ByteArray:
     cdef LocalRef _jobject
     cdef long _size
     cdef unsigned char *_buf
     cdef unsigned char[:] _arr
 
     def __cinit__(self):
         self._size = 0
         self._buf = NULL
         self._arr = None
 
-
-
     def __dealloc__(self):
         cdef JNIEnv *j_env
         if self._buf != NULL:
             j_env = get_jnienv()
             j_env[0].ReleaseByteArrayElements(
                 j_env, self._jobject.obj, <jbyte *>self._buf, 0)
             self._buf = NULL
@@ -62,19 +60,14 @@
                     xx = x
                     val.append(self._arr[xx])
             return val
         else:
             xx = index
             return self._arr[xx]
 
-    def __getslice__(self, long i, long j):
-        if self._size:
-            return self._arr[i:j]
-        return []
-
     def __richcmp__(self, other, op):
         cdef ByteArray b_other
         if isinstance(other, (list, tuple)):
             return python_op(op, self.tolist(), other)
         elif isinstance(other, ByteArray):
             b_other = other
             return python_op(op, self.tostring(), other.tostring())
```

### Comparing `pyjnius-1.4.2/jnius/jnius_proxy.pxi` & `pyjnius-1.5.0/jnius/jnius_proxy.pxi`

 * *Files 1% similar despite different names*

```diff
@@ -129,17 +129,15 @@
 
     # did python returned a "native" type ?
     jtype = None
 
     if ret_signature == 'Ljava/lang/Object;':
         # generic object, try to manually convert it
         tp = type(ret)
-        if PY2 and tp == int:
-            jtype = 'I'
-        elif (PY2 and tp == long) or tp == int:
+        if tp == int:
             jtype = 'J'
         elif tp == float:
             jtype = 'D'
         elif tp == bool:
             jtype = 'Z'
     elif len(ret_signature) == 1:
         jtype = ret_signature
```

### Comparing `pyjnius-1.4.2/jnius/jnius_utils.pxi` & `pyjnius-1.5.0/jnius/jnius_utils.pxi`

 * *Files 5% similar despite different names*

```diff
@@ -1,21 +1,9 @@
 cdef str_for_c(s):
-     if PY2:
-        if isinstance(s, unicode):
-            return s.encode('utf-8')
-        else:
-            return s
-     else:
-        return s.encode('utf-8')
-
-cdef items_compat(d):
-     if not PY2:
-         return d.items()
-     else:
-        return d.iteritems()                
+    return s.encode('utf-8')
 
 cdef parse_definition(definition):
     # not a function, just a field
     if definition[0] != '(':
         return definition, None
 
     # it's a function!
@@ -366,19 +354,15 @@
             r = r[1:-1]
 
             if arg is None:
                 score += 10
                 continue
 
             # if it's a string, accept any python string
-            if r == 'java/lang/String' and isinstance(arg, base_string) and PY2:
-                score += 10
-                continue
-
-            if r == 'java/lang/String' and isinstance(arg, str) and not PY2:
+            if r == 'java/lang/String' and isinstance(arg, str):
                 score += 10
                 continue
 
             # if it's a generic object, accept python string, or any java
             # class/object
             if r == 'java/lang/Object':
                 if isinstance(arg, (PythonJavaClass, JavaClass, JavaObject)):
@@ -436,23 +420,19 @@
 
         if r[0] == '[':
 
             if arg is None:
                 score += 10
                 continue
 
-            if (r == '[B' or r == '[C') and isinstance(arg, base_string) and PY2:
-                score += 10
-                continue
-
-            if (r == '[B') and isinstance(arg, bytes) and not PY2:
+            if (r == '[B') and isinstance(arg, bytes):
                 score += 10
                 continue
 
-            if (r == '[C') and isinstance(arg, str) and not PY2:
+            if (r == '[C') and isinstance(arg, str):
                 score += 10
                 continue
 
             if r == '[B' and isinstance(arg, (bytearray, ByteArray)):
                 score += 10
                 continue
```

### Comparing `pyjnius-1.4.2/jnius/reflect.py` & `pyjnius-1.5.0/jnius/reflect.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,27 +1,26 @@
 from __future__ import absolute_import
 from __future__ import unicode_literals
 from __future__ import division
 from collections import defaultdict
-from logging import getLogger, DEBUG
+import logging
 
-from six import with_metaclass, PY2
 
 from .jnius import (
     JavaClass, MetaJavaClass, JavaMethod, JavaStaticMethod,
     JavaField, JavaStaticField, JavaMultipleMethod, find_javaclass,
     JavaException, get_signature
 )
 
 __all__ = ('autoclass', 'ensureclass', 'protocol_map')
 
-log = getLogger(__name__)
+log = logging.getLogger('kivy').getChild(__name__)
 
 
-class Class(with_metaclass(MetaJavaClass, JavaClass)):
+class Class(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/Class'
 
     desiredAssertionStatus = JavaMethod('()Z')
     forName = JavaMultipleMethod([
         ('(Ljava/lang/String,Z,Ljava/lang/ClassLoader;)Ljava/langClass;', True, False),
         ('(Ljava/lang/String;)Ljava/lang/Class;', True, False), ])
     getClassLoader = JavaMethod('()Ljava/lang/ClassLoader;')
@@ -68,22 +67,22 @@
             self.getName()
         )
 
     def __repr__(self):
         return '<%s at 0x%x>' % (self, id(self))
 
 
-class Object(with_metaclass(MetaJavaClass, JavaClass)):
+class Object(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/Object'
 
     getClass = JavaMethod('()Ljava/lang/Class;')
     hashCode = JavaMethod('()I')
 
 
-class Modifier(with_metaclass(MetaJavaClass, JavaClass)):
+class Modifier(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/reflect/Modifier'
 
     isAbstract = JavaStaticMethod('(I)Z')
     isFinal = JavaStaticMethod('(I)Z')
     isInterface = JavaStaticMethod('(I)Z')
     isNative = JavaStaticMethod('(I)Z')
     isPrivate = JavaStaticMethod('(I)Z')
@@ -91,37 +90,36 @@
     isPublic = JavaStaticMethod('(I)Z')
     isStatic = JavaStaticMethod('(I)Z')
     isStrict = JavaStaticMethod('(I)Z')
     isSynchronized = JavaStaticMethod('(I)Z')
     isTransient = JavaStaticMethod('(I)Z')
     isVolatile = JavaStaticMethod('(I)Z')
 
-class Method(with_metaclass(MetaJavaClass, JavaClass)):
+class Method(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/reflect/Method'
 
     getName = JavaMethod('()Ljava/lang/String;')
     toString = JavaMethod('()Ljava/lang/String;')
     getParameterTypes = JavaMethod('()[Ljava/lang/Class;')
     getReturnType = JavaMethod('()Ljava/lang/Class;')
     getModifiers = JavaMethod('()I')
     isVarArgs = JavaMethod('()Z')
     isDefault = JavaMethod('()Z')
-    
 
 
-class Field(with_metaclass(MetaJavaClass, JavaClass)):
+class Field(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/reflect/Field'
 
     getName = JavaMethod('()Ljava/lang/String;')
     toString = JavaMethod('()Ljava/lang/String;')
     getType = JavaMethod('()Ljava/lang/Class;')
     getModifiers = JavaMethod('()I')
 
 
-class Constructor(with_metaclass(MetaJavaClass, JavaClass)):
+class Constructor(JavaClass, metaclass=MetaJavaClass):
     __javaclass__ = 'java/lang/reflect/Constructor'
 
     toString = JavaMethod('()Ljava/lang/String;')
     getParameterTypes = JavaMethod('()[Ljava/lang/Class;')
     getModifiers = JavaMethod('()I')
     isVarArgs = JavaMethod('()Z')
 
@@ -296,15 +294,15 @@
             # uniquely named method
             owningCls, method, level = cls_methods[name][0]
             static = Modifier.isStatic(method.getModifiers())
             varargs = method.isVarArgs()
             sig = '({0}){1}'.format(
                 ''.join([get_signature(x) for x in method.getParameterTypes()]),
                 get_signature(method.getReturnType()))
-            if log.isEnabledFor(DEBUG):
+            if log.isEnabledFor(logging.DEBUG):
                 log_method(method, name, sig)
             classDict[name] = (JavaStaticMethod if static else JavaMethod)(sig, varargs=varargs)
             # methods that fit the characteristics of a JavaBean's methods get turned into properties.
             # these added properties should not supercede any other methods or fields.
             if name != 'getClass' and bean_getter(name) and len(method.getParameterTypes()) == 0:
                 lowername = lower_name(name[2 if name.startswith('is') else 3:])
                 if lowername in classDict:
@@ -331,15 +329,15 @@
                 if level > paramsig_to_level[param_sig]:
                     log.debug("discarding %s name from %s at level %d" % (name, str(owningCls), level))
                     continue
 
                 return_sig = get_signature(method.getReturnType())
                 sig = '({0}){1}'.format(param_sig, return_sig)
 
-                if log.isEnabledFor(DEBUG):
+                if log.isEnabledFor(logging.DEBUG):
                     log_method(method, name, sig)
                 signatures.append((sig, Modifier.isStatic(method.getModifiers()), method.isVarArgs()))
 
             log.debug("method selected %d multiple signatures of %s" % (len(signatures), str(signatures)))
             classDict[name] = JavaMultipleMethod(signatures)
 
     # check whether any classes in the hierarchy appear in the protocol_map
@@ -376,39 +374,14 @@
     ''' dunder method for java.util.Map '''
     rtr = self.get(k)
     if rtr is None:
         raise KeyError()
     return rtr
 
 
-class Py2Iterator(object):
-    '''
-    In py2 the next() is called on the iterator, not __next__
-    so we need to wrap the java call to check hasNext to conform to
-    python's api
-    '''
-    def __init__(self, java_iterator):
-        self.java_iterator = java_iterator
-
-    def __iter__(self):
-        return self
-
-    def next(self):
-        log.debug("monkey patched next() called")
-        if not self.java_iterator.hasNext():
-            raise StopIteration()
-        return self.java_iterator.next()
-
-
-def safe_iterator(iterator):
-    if PY2:
-        return Py2Iterator(iterator)
-    return iterator
-
-
 def _iterator_next(self):
     ''' dunder method for java.util.Iterator'''
     if not self.hasNext():
         raise StopIteration()
 
     return self.next()
 
@@ -425,22 +398,22 @@
     },
     'java.util.Map' : {
         '__setitem__' : lambda self, k, v : self.put(k,v),
         '__getitem__' : _map_getitem,
         '__delitem__' : lambda self, item: self.remove(item),
         '__len__' : lambda self: self.size(),
         '__contains__' : lambda self, item: self.containsKey(item),
-        '__iter__' : lambda self: safe_iterator(self.keySet().iterator())
+        '__iter__' : lambda self: self.keySet().iterator()
     },
     'java.util.Iterator' : {
-        '__iter__' : lambda self: safe_iterator(self),
+        '__iter__' : lambda self: self,
         '__next__' : _iterator_next,
     },
     'java.lang.Iterable' : {
-        '__iter__' : lambda self: safe_iterator(self.iterator()),
+        '__iter__' : lambda self: self.iterator(),
     },
     # this also addresses java.io.Closeable
     'java.lang.AutoCloseable' : {
         '__enter__' : lambda self: self,
         '__exit__' : lambda self, type, value, traceback: self.close()
     },
     'java.lang.Comparable' : {
```

### Comparing `pyjnius-1.4.2/jnius/signatures.py` & `pyjnius-1.5.0/jnius/signatures.py`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/src/org/jnius/NativeInvocationHandler.class` & `pyjnius-1.5.0/jnius/src/org/jnius/NativeInvocationHandler.class`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius/src/org/jnius/NativeInvocationHandler.java` & `pyjnius-1.5.0/jnius/src/org/jnius/NativeInvocationHandler.java`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/jnius_config.py` & `pyjnius-1.5.0/jnius_config.py`

 * *Files identical despite different names*

### Comparing `pyjnius-1.4.2/pyjnius.egg-info/PKG-INFO` & `pyjnius-1.5.0/pyjnius.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 Metadata-Version: 2.1
 Name: pyjnius
-Version: 1.4.2
+Version: 1.5.0
 Summary: A Python module to access Java classes as Python classes using JNI.
 Home-page: https://github.com/kivy/pyjnius
 Author: Kivy Team and other contributors
 Author-email: kivy-dev@googlegroups.com
 Keywords: Java JNI Android
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Operating System :: Android
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 Provides-Extra: ci
 License-File: LICENSE
 
 PyJNIus
```

### Comparing `pyjnius-1.4.2/setup.py` & `pyjnius-1.5.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -15,24 +15,21 @@
 import sys
 from setup_sdist import SETUP_KWARGS
 
 # XXX hack to be able to import jnius.env withough having build
 # jnius.jnius yet, better solution welcome
 syspath = sys.path[:]
 sys.path.insert(0, 'jnius')
-from env import (
-    get_java_setup,
-    PY2
-)
+from env import get_java_setup
 sys.path = syspath
 
 def getenv(key):
     '''Get value from environment and decode it.'''
     val = environ.get(key)
-    if val is not None and not PY2:
+    if val is not None:
         try:
             return val.decode()
         except AttributeError:
             return val
     return val
 
 
@@ -42,15 +39,14 @@
     'jnius_conversion.pxi',
     'jnius_export_class.pxi',
     'jnius_export_func.pxi',
     'jnius_jvm_android.pxi',
     'jnius_jvm_desktop.pxi',
     'jnius_jvm_dlopen.pxi',
     'jnius_localref.pxi',
-    'jnius_nativetypes.pxi',
     'jnius_nativetypes3.pxi',
     'jnius_proxy.pxi',
     'jnius.pyx',
     'jnius_utils.pxi',
 ]
 
 EXTRA_LINK_ARGS = []
@@ -86,15 +82,14 @@
 
 compile_native_invocation_handler(JAVA)
 
 
 # generate the config.pxi
 with open(join(dirname(__file__), 'jnius', 'config.pxi'), 'w') as fd:
     fd.write('DEF JNIUS_PLATFORM = {0!r}\n\n'.format(PLATFORM))
-    fd.write('DEF JNIUS_PYTHON3 = True\n\n')
 
 # pop setup.py from included files in the installed package
 SETUP_KWARGS['py_modules'].remove('setup')
 
 ext_modules = [
     Extension(
         'jnius', [join('jnius', x) for x in FILES],
```

### Comparing `pyjnius-1.4.2/setup_sdist.py` & `pyjnius-1.5.0/setup_sdist.py`

 * *Files 1% similar despite different names*

```diff
@@ -44,18 +44,18 @@
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Natural Language :: English',
         'Operating System :: MacOS',
         'Operating System :: Microsoft :: Windows',
         'Operating System :: POSIX :: Linux',
         'Operating System :: Android',
-        'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Topic :: Software Development :: Libraries :: Application Frameworks'
     ]
 }
 
 if __name__ == '__main__':
     setup(**SETUP_KWARGS)
```

