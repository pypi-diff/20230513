# Comparing `tmp/pybluemonday-0.0.8.tar.gz` & `tmp/pybluemonday-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/pybluemonday-0.0.8.tar", last modified: Mon Oct 18 16:56:10 2021, max compression
+gzip compressed data, was "dist/pybluemonday-0.0.9.tar", last modified: Sun Feb  6 07:24:28 2022, max compression
```

## Comparing `pybluemonday-0.0.8.tar` & `pybluemonday-0.0.9.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     4452 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3442 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/README.md
--rw-r--r--   0 runner    (1001) docker     (121)     4340 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/bluemonday.go
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday/
--rw-r--r--   0 runner    (1001) docker     (121)     3721 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/pybluemonday/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4452 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      449 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       43 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/pybluemonday.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     2306 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/tests/bluemonday/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/bluemonday/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4536 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/bluemonday/test_policies.py
--rw-r--r--   0 runner    (1001) docker     (121)     5197 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/bluemonday/test_sanitize.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-18 16:56:10.000000 pybluemonday-0.0.8/tests/html_sanitizer/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/html_sanitizer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1043 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/html_sanitizer/test_sanitize.py
--rw-r--r--   0 runner    (1001) docker     (121)     1233 2021-10-18 16:55:38.000000 pybluemonday-0.0.8/tests/test_memory_leaks.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     4452 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     3442 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (121)     4902 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/bluemonday.go
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/pybluemonday/
+-rw-r--r--   0 runner    (1001) docker     (121)     4720 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/pybluemonday/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/pybluemonday.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     4452 2022-02-06 07:24:27.000000 pybluemonday-0.0.9/pybluemonday.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      449 2022-02-06 07:24:27.000000 pybluemonday-0.0.9/pybluemonday.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-02-06 07:24:27.000000 pybluemonday-0.0.9/pybluemonday.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       10 2022-02-06 07:24:27.000000 pybluemonday-0.0.9/pybluemonday.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       43 2022-02-06 07:24:27.000000 pybluemonday-0.0.9/pybluemonday.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     2306 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/tests/bluemonday/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/bluemonday/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4536 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/bluemonday/test_policies.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6679 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/bluemonday/test_sanitize.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-06 07:24:28.000000 pybluemonday-0.0.9/tests/html_sanitizer/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/html_sanitizer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1043 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/html_sanitizer/test_sanitize.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1233 2022-02-06 07:23:41.000000 pybluemonday-0.0.9/tests/test_memory_leaks.py
```

### Comparing `pybluemonday-0.0.8/PKG-INFO` & `pybluemonday-0.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybluemonday
-Version: 0.0.8
+Version: 0.0.9
 Summary: Python bindings for the bluemonday HTML sanitizer
 Home-page: https://github.com/ColdHeat/pybluemonday
 Author: Kevin Chung
 Author-email: kchung@nyu.edu
 License: UNKNOWN
 Description: # pybluemonday
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: pybluemonday Version: 0.0.8 Summary: Python
+Metadata-Version: 2.1 Name: pybluemonday Version: 0.0.9 Summary: Python
 bindings for the bluemonday HTML sanitizer Home-page: https://github.com/
 ColdHeat/pybluemonday Author: Kevin Chung Author-email: kchung@nyu.edu License:
 UNKNOWN Description: # pybluemonday [![PyPI](https://img.shields.io/pypi/v/
 pybluemonday)](https://pypi.org/project/pybluemonday/) pybluemonday is a
 library for sanitizing HTML very quickly via [bluemonday](https://github.com/
 microcosm-cc/bluemonday). pybluemonday takes untrusted user generated content
 as an input, and will return HTML that has been sanitised against a whitelist
```

### Comparing `pybluemonday-0.0.8/README.md` & `pybluemonday-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `pybluemonday-0.0.8/bluemonday.go` & `pybluemonday-0.0.9/bluemonday.go`

 * *Files 7% similar despite different names*

```diff
@@ -152,14 +152,33 @@
 
 	policy := POLICIES[goPolicyId]
 	args := []reflect.Value{reflect.ValueOf(goArgument)}
 	meth := reflect.ValueOf(policy).MethodByName(goMethod)
 	meth.Call(args)
 }
 
+//export CallPolicyFunctionWithInt
+func CallPolicyFunctionWithInt(policyId C.ulong, method *C.char, argtype *C.char, argument C.uint) {
+	goPolicyId := uint32(policyId)
+	goMethod := C.GoString(method)
+	goArgType := C.GoString(argtype)
+	goArgument := int(argument)
+	policy := POLICIES[goPolicyId]
+
+	switch goArgType {
+	case "SandboxValue":
+		sv := bluemonday.SandboxValue(goArgument)
+		args := []reflect.Value{reflect.ValueOf(sv)}
+		meth := reflect.ValueOf(policy).MethodByName(goMethod)
+		meth.Call(args)
+	default:
+		panic("Unknown argument type function")
+	}
+}
+
 //export SanitizeWithPolicy
 func SanitizeWithPolicy(policyId C.ulong, document *C.char) *C.char {
 	goPolicyId := uint32(policyId)
 	goDocument := C.GoString(document)
 
 	policy := POLICIES[goPolicyId]
 	output := policy.Sanitize(goDocument)
```

### Comparing `pybluemonday-0.0.8/pybluemonday.egg-info/PKG-INFO` & `pybluemonday-0.0.9/pybluemonday.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybluemonday
-Version: 0.0.8
+Version: 0.0.9
 Summary: Python bindings for the bluemonday HTML sanitizer
 Home-page: https://github.com/ColdHeat/pybluemonday
 Author: Kevin Chung
 Author-email: kchung@nyu.edu
 License: UNKNOWN
 Description: # pybluemonday
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: pybluemonday Version: 0.0.8 Summary: Python
+Metadata-Version: 2.1 Name: pybluemonday Version: 0.0.9 Summary: Python
 bindings for the bluemonday HTML sanitizer Home-page: https://github.com/
 ColdHeat/pybluemonday Author: Kevin Chung Author-email: kchung@nyu.edu License:
 UNKNOWN Description: # pybluemonday [![PyPI](https://img.shields.io/pypi/v/
 pybluemonday)](https://pypi.org/project/pybluemonday/) pybluemonday is a
 library for sanitizing HTML very quickly via [bluemonday](https://github.com/
 microcosm-cc/bluemonday). pybluemonday takes untrusted user generated content
 as an input, and will return HTML that has been sanitised against a whitelist
```

### Comparing `pybluemonday-0.0.8/setup.py` & `pybluemonday-0.0.9/setup.py`

 * *Files identical despite different names*

### Comparing `pybluemonday-0.0.8/tests/bluemonday/test_policies.py` & `pybluemonday-0.0.9/tests/bluemonday/test_policies.py`

 * *Files identical despite different names*

### Comparing `pybluemonday-0.0.8/tests/html_sanitizer/test_sanitize.py` & `pybluemonday-0.0.9/tests/html_sanitizer/test_sanitize.py`

 * *Files identical despite different names*

### Comparing `pybluemonday-0.0.8/tests/test_memory_leaks.py` & `pybluemonday-0.0.9/tests/test_memory_leaks.py`

 * *Files identical despite different names*

