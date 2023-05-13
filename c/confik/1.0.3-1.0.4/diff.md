# Comparing `tmp/confik-1.0.3.tar.gz` & `tmp/confik-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "confik-1.0.3.tar", last modified: Fri May 12 07:42:05 2023, max compression
+gzip compressed data, was "confik-1.0.4.tar", last modified: Sat May 13 04:29:56 2023, max compression
```

## Comparing `confik-1.0.3.tar` & `confik-1.0.4.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.628303 confik-1.0.3/
--rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 07:42:05.628192 confik-1.0.3/PKG-INFO
--rw-r--r--   0 leondaz    (501) staff       (20)      717 2023-05-12 07:24:54.000000 confik-1.0.3/README.md
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.626941 confik-1.0.3/confik/
--rw-r--r--   0 leondaz    (501) staff       (20)      827 2023-05-12 07:29:23.000000 confik-1.0.3/confik/__init__.py
--rw-r--r--   0 leondaz    (501) staff       (20)       78 2023-05-12 03:19:53.000000 confik-1.0.3/confik/exceptions.py
--rw-r--r--   0 leondaz    (501) staff       (20)     2806 2023-05-12 07:41:59.000000 confik-1.0.3/confik/parsers.py
--rw-r--r--   0 leondaz    (501) staff       (20)     1265 2023-05-12 06:56:06.000000 confik-1.0.3/confik/proxies.py
--rw-r--r--   0 leondaz    (501) staff       (20)      286 2023-05-12 05:54:36.000000 confik-1.0.3/confik/utils.py
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.627485 confik-1.0.3/confik.egg-info/
--rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/PKG-INFO
--rw-r--r--   0 leondaz    (501) staff       (20)      319 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/SOURCES.txt
--rw-r--r--   0 leondaz    (501) staff       (20)        1 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/dependency_links.txt
--rw-r--r--   0 leondaz    (501) staff       (20)        7 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/top_level.txt
--rw-r--r--   0 leondaz    (501) staff       (20)       38 2023-05-12 07:42:05.628337 confik-1.0.3/setup.cfg
--rw-r--r--   0 leondaz    (501) staff       (20)      277 2023-05-12 07:15:23.000000 confik-1.0.3/setup.py
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.627934 confik-1.0.3/tests/
--rw-r--r--   0 leondaz    (501) staff       (20)      308 2023-05-12 06:07:05.000000 confik-1.0.3/tests/test_confik_parser.py
--rw-r--r--   0 leondaz    (501) staff       (20)     2022 2023-05-12 07:41:59.000000 confik-1.0.3/tests/test_read_environment_variables.py
--rw-r--r--   0 leondaz    (501) staff       (20)      164 2023-05-12 05:54:17.000000 confik-1.0.3/tests/test_utils.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-13 04:29:56.962182 confik-1.0.4/
+-rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-13 04:29:56.962059 confik-1.0.4/PKG-INFO
+-rw-r--r--   0 leondaz    (501) staff       (20)      690 2023-05-12 07:45:30.000000 confik-1.0.4/README.md
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-13 04:29:56.960978 confik-1.0.4/confik/
+-rw-r--r--   0 leondaz    (501) staff       (20)      836 2023-05-13 04:28:55.000000 confik-1.0.4/confik/__init__.py
+-rw-r--r--   0 leondaz    (501) staff       (20)       78 2023-05-12 03:19:53.000000 confik-1.0.4/confik/exceptions.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     2491 2023-05-13 04:26:49.000000 confik-1.0.4/confik/parsers.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     1265 2023-05-12 06:56:06.000000 confik-1.0.4/confik/proxies.py
+-rw-r--r--   0 leondaz    (501) staff       (20)      619 2023-05-13 04:28:54.000000 confik-1.0.4/confik/utils.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-13 04:29:56.961413 confik-1.0.4/confik.egg-info/
+-rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-13 04:29:56.000000 confik-1.0.4/confik.egg-info/PKG-INFO
+-rw-r--r--   0 leondaz    (501) staff       (20)      319 2023-05-13 04:29:56.000000 confik-1.0.4/confik.egg-info/SOURCES.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)        1 2023-05-13 04:29:56.000000 confik-1.0.4/confik.egg-info/dependency_links.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)        7 2023-05-13 04:29:56.000000 confik-1.0.4/confik.egg-info/top_level.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)       38 2023-05-13 04:29:56.962231 confik-1.0.4/setup.cfg
+-rw-r--r--   0 leondaz    (501) staff       (20)      277 2023-05-13 04:29:42.000000 confik-1.0.4/setup.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-13 04:29:56.961832 confik-1.0.4/tests/
+-rw-r--r--   0 leondaz    (501) staff       (20)      308 2023-05-12 06:07:05.000000 confik-1.0.4/tests/test_confik_parser.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     2285 2023-05-13 04:28:54.000000 confik-1.0.4/tests/test_read_environment_variables.py
+-rw-r--r--   0 leondaz    (501) staff       (20)      149 2023-05-13 04:27:37.000000 confik-1.0.4/tests/test_utils.py
```

### Comparing `confik-1.0.3/README.md` & `confik-1.0.4/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -33,10 +33,10 @@
 
 
 admin_password = confik.get("ADMIN_PASSWORD", default_factory=factory)
 # $ very_confidential_pwd
 
 allowed_hosts = confik.get("ALLOWED_HOSTS", cast=confik.csv)
 
-debug = confik.get('DEBUG', cast=bool, choices=['True', 'False'])
+debug = confik.get('DEBUG', cast=bool)
 
 ```
```

### Comparing `confik-1.0.3/confik/__init__.py` & `confik-1.0.4/confik/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from .exceptions import ConfikError
 from .parsers import ConfikParser
-from .utils import csv
+from .utils import boolean, csv
 
 confik = ConfikParser()
 
 
 def get(
     key,
     default=None,
```

### Comparing `confik-1.0.3/confik/parsers.py` & `confik-1.0.4/confik/parsers.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from collections.abc import Callable, Iterable
 
 from confik.exceptions import ConfikError
 from confik.proxies import EnvMappingProxy
+from confik.utils import boolean
 
 
 class ConfikParser:
     proxy_class = EnvMappingProxy
 
     def __init__(self, path=".", *args, **kwargs):
         self.source = self.proxy_class(*args, path=path, **kwargs)
@@ -68,23 +69,15 @@
                 value=env,
                 choices=", ".join(choices),
             )
 
         if cast:
             try:
                 if cast is bool:
-                    truthy_values = ("True", "true", "1")
-                    falsy_values = ("False", "false", "0")
-                    allowed_values = (*truthy_values, *falsy_values)
-
-                    assert env in allowed_values, "{} not in [{}]".format(
-                        env, ", ".join(allowed_values)
-                    )
-                    return env in truthy_values
-
+                    return boolean(env)
                 return cast(env)
             except ValueError:
                 raise ConfikError(
                     "value {v} can't be casted into {c}".format(v=env, c=cast.__name__)
                 )
 
         return env
```

### Comparing `confik-1.0.3/confik/proxies.py` & `confik-1.0.4/confik/proxies.py`

 * *Files identical despite different names*

### Comparing `confik-1.0.3/tests/test_read_environment_variables.py` & `confik-1.0.4/tests/test_read_environment_variables.py`

 * *Files 7% similar despite different names*

```diff
@@ -73,7 +73,17 @@
         env = confik.get("VARIABLE_WITH_FALSE_VALUE_{i}".format(i=i), cast=bool)
         assert env is False, "Expected False, got {}".format(env)
 
 
 def test_read_integer():
     env = confik.get("VARIABLE_WITH_INTEGER", cast=int)
     assert isinstance(env, int)
+
+
+def test_read_not_bool_as_bool():
+    with pytest.raises(AssertionError):
+        env = confik.get("PATH", cast=bool)
+
+
+def test_confik_boolean_same_as_python_bool():
+    with pytest.raises(AssertionError):
+        env = confik.get("PATH", cast=confik.boolean)
```

