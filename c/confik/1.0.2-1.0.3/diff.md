# Comparing `tmp/confik-1.0.2.tar.gz` & `tmp/confik-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "confik-1.0.2.tar", last modified: Fri May 12 06:58:34 2023, max compression
+gzip compressed data, was "confik-1.0.3.tar", last modified: Fri May 12 07:42:05 2023, max compression
```

## Comparing `confik-1.0.2.tar` & `confik-1.0.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 06:58:34.685003 confik-1.0.2/
--rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 06:58:34.684871 confik-1.0.2/PKG-INFO
--rw-r--r--   0 leondaz    (501) staff       (20)      133 2023-05-12 06:07:05.000000 confik-1.0.2/README.md
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 06:58:34.683304 confik-1.0.2/confik/
--rw-r--r--   0 leondaz    (501) staff       (20)      828 2023-05-12 06:34:12.000000 confik-1.0.2/confik/__init__.py
--rw-r--r--   0 leondaz    (501) staff       (20)       78 2023-05-12 03:19:53.000000 confik-1.0.2/confik/exceptions.py
--rw-r--r--   0 leondaz    (501) staff       (20)     2213 2023-05-12 06:45:46.000000 confik-1.0.2/confik/parsers.py
--rw-r--r--   0 leondaz    (501) staff       (20)     1265 2023-05-12 06:56:06.000000 confik-1.0.2/confik/proxies.py
--rw-r--r--   0 leondaz    (501) staff       (20)      286 2023-05-12 05:54:36.000000 confik-1.0.2/confik/utils.py
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 06:58:34.683979 confik-1.0.2/confik.egg-info/
--rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 06:58:34.000000 confik-1.0.2/confik.egg-info/PKG-INFO
--rw-r--r--   0 leondaz    (501) staff       (20)      319 2023-05-12 06:58:34.000000 confik-1.0.2/confik.egg-info/SOURCES.txt
--rw-r--r--   0 leondaz    (501) staff       (20)        1 2023-05-12 06:58:34.000000 confik-1.0.2/confik.egg-info/dependency_links.txt
--rw-r--r--   0 leondaz    (501) staff       (20)        7 2023-05-12 06:58:34.000000 confik-1.0.2/confik.egg-info/top_level.txt
--rw-r--r--   0 leondaz    (501) staff       (20)       38 2023-05-12 06:58:34.685043 confik-1.0.2/setup.cfg
--rw-r--r--   0 leondaz    (501) staff       (20)      277 2023-05-12 06:58:33.000000 confik-1.0.2/setup.py
-drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 06:58:34.684583 confik-1.0.2/tests/
--rw-r--r--   0 leondaz    (501) staff       (20)      308 2023-05-12 06:07:05.000000 confik-1.0.2/tests/test_confik_parser.py
--rw-r--r--   0 leondaz    (501) staff       (20)     1482 2023-05-12 06:07:05.000000 confik-1.0.2/tests/test_read_environment_variables.py
--rw-r--r--   0 leondaz    (501) staff       (20)      164 2023-05-12 05:54:17.000000 confik-1.0.2/tests/test_utils.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.628303 confik-1.0.3/
+-rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 07:42:05.628192 confik-1.0.3/PKG-INFO
+-rw-r--r--   0 leondaz    (501) staff       (20)      717 2023-05-12 07:24:54.000000 confik-1.0.3/README.md
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.626941 confik-1.0.3/confik/
+-rw-r--r--   0 leondaz    (501) staff       (20)      827 2023-05-12 07:29:23.000000 confik-1.0.3/confik/__init__.py
+-rw-r--r--   0 leondaz    (501) staff       (20)       78 2023-05-12 03:19:53.000000 confik-1.0.3/confik/exceptions.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     2806 2023-05-12 07:41:59.000000 confik-1.0.3/confik/parsers.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     1265 2023-05-12 06:56:06.000000 confik-1.0.3/confik/proxies.py
+-rw-r--r--   0 leondaz    (501) staff       (20)      286 2023-05-12 05:54:36.000000 confik-1.0.3/confik/utils.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.627485 confik-1.0.3/confik.egg-info/
+-rw-r--r--   0 leondaz    (501) staff       (20)      197 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/PKG-INFO
+-rw-r--r--   0 leondaz    (501) staff       (20)      319 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/SOURCES.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)        1 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/dependency_links.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)        7 2023-05-12 07:42:05.000000 confik-1.0.3/confik.egg-info/top_level.txt
+-rw-r--r--   0 leondaz    (501) staff       (20)       38 2023-05-12 07:42:05.628337 confik-1.0.3/setup.cfg
+-rw-r--r--   0 leondaz    (501) staff       (20)      277 2023-05-12 07:15:23.000000 confik-1.0.3/setup.py
+drwxr-xr-x   0 leondaz    (501) staff       (20)        0 2023-05-12 07:42:05.627934 confik-1.0.3/tests/
+-rw-r--r--   0 leondaz    (501) staff       (20)      308 2023-05-12 06:07:05.000000 confik-1.0.3/tests/test_confik_parser.py
+-rw-r--r--   0 leondaz    (501) staff       (20)     2022 2023-05-12 07:41:59.000000 confik-1.0.3/tests/test_read_environment_variables.py
+-rw-r--r--   0 leondaz    (501) staff       (20)      164 2023-05-12 05:54:17.000000 confik-1.0.3/tests/test_utils.py
```

### Comparing `confik-1.0.2/confik/__init__.py` & `confik-1.0.3/confik/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 
 def get(
     key,
     default=None,
     cast=None,
     default_factory=None,
     choices=tuple(),
-    raise_exception=False,
+    raise_exception=True,
 ):
     """An interface to confik.get(...)
 
     :param key: The key name to get from environment
     :param default: The value to return if the key was not found
     :param cast: A function to call on the value after it's found
     :param default_factory: A function to call with the key to return a value if the value was not found
```

### Comparing `confik-1.0.2/confik/parsers.py` & `confik-1.0.3/confik/parsers.py`

 * *Files 17% similar despite different names*

```diff
@@ -30,14 +30,19 @@
         assert not all(
             [default, default_factory]
         ), "default and default_factory parameters are mutually exclusive, must only provide one of them."
 
         assert isinstance(choices, Iterable), "choices must be an iterable"
         assert isinstance(raise_exception, bool), "raise_exception must be a boolean"
 
+        if default and choices:
+            assert (
+                default in choices
+            ), "default value is not in the list of provided choices"
+
     def get(
         self,
         key,
         default=None,
         cast=None,
         default_factory=None,
         choices=tuple(),
@@ -47,29 +52,39 @@
             key, cast, default, default_factory, choices, raise_exception
         )
 
         env = self.source.get(key, default)
 
         if env is None:
             if default_factory:
-                env = default_factory(key)
+                return default_factory(key)
             elif raise_exception:
                 raise ConfikError(
                     "{key} variable can't be of type None".format(key=key)
                 )
 
         if choices:
             assert env in choices, "{key}={value} is not in choices={choices}".format(
                 key=key,
                 value=env,
                 choices=", ".join(choices),
             )
 
-        try:
-            if cast:
+        if cast:
+            try:
+                if cast is bool:
+                    truthy_values = ("True", "true", "1")
+                    falsy_values = ("False", "false", "0")
+                    allowed_values = (*truthy_values, *falsy_values)
+
+                    assert env in allowed_values, "{} not in [{}]".format(
+                        env, ", ".join(allowed_values)
+                    )
+                    return env in truthy_values
+
                 return cast(env)
+            except ValueError:
+                raise ConfikError(
+                    "value {v} can't be casted into {c}".format(v=env, c=cast.__name__)
+                )
 
-            return env
-        except ValueError:
-            raise ConfikError(
-                "value {v} can't be casted into {c}".format(v=env, c=cast.__name__)
-            )
+        return env
```

### Comparing `confik-1.0.2/confik/proxies.py` & `confik-1.0.3/confik/proxies.py`

 * *Files identical despite different names*

### Comparing `confik-1.0.2/tests/test_read_environment_variables.py` & `confik-1.0.3/tests/test_read_environment_variables.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,14 @@
 import random
 import string
 
+import pytest
+
 import confik
+from confik import ConfikError
 
 
 def get_random_key():
     return "".join(random.choice(string.ascii_uppercase) for _ in range(20))
 
 
 def test_read_variable_from_env():
@@ -16,16 +19,17 @@
 def test_read_variable_from_os():
     env = confik.get("PATH")
     assert env, "env is {v}".format(v=env)
 
 
 def test_get_non_existent_key():
     random_key = get_random_key()
-    env = confik.get(random_key)
-    assert env is None, "env has a value of {v}".format(v=env)
+
+    with pytest.raises(ConfikError):
+        confik.get(random_key)
 
 
 def test_default_value():
     random_key = get_random_key()
 
     env = confik.get(random_key, "DEFAULT_VALUE")
     assert (
@@ -52,7 +56,24 @@
     for i, element in enumerate(env):
         assert bool(
             element.find(" ")
         ), "element at index {i} has space {element}".format(
             i=i,
             element=element,
         )
+
+
+def test_read_truthy_bools():
+    for i in range(1, 4):
+        env = confik.get("VARIABLE_WITH_TRUE_VALUE_{i}".format(i=i), cast=bool)
+        assert env is True, "Expected True, got {}".format(env)
+
+
+def test_read_falsy_bools():
+    for i in range(1, 4):
+        env = confik.get("VARIABLE_WITH_FALSE_VALUE_{i}".format(i=i), cast=bool)
+        assert env is False, "Expected False, got {}".format(env)
+
+
+def test_read_integer():
+    env = confik.get("VARIABLE_WITH_INTEGER", cast=int)
+    assert isinstance(env, int)
```

