# Comparing `tmp/devpytools-0.1.0.dev5.tar.gz` & `tmp/devpytools-0.1.0.dev6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\devpytools-0.1.0.dev5.tar", last modified: Fri May 12 19:53:06 2023, max compression
+gzip compressed data, was "dist\devpytools-0.1.0.dev6.tar", last modified: Sat May 13 11:08:25 2023, max compression
```

## Comparing `devpytools-0.1.0.dev5.tar` & `devpytools-0.1.0.dev6.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:06.062369 devpytools-0.1.0.dev5/
--rw-rw-rw-   0        0        0     1950 2022-10-05 19:38:35.000000 devpytools-0.1.0.dev5/.gitignore
--rw-rw-rw-   0        0        0     1085 2022-04-16 14:06:14.000000 devpytools-0.1.0.dev5/LICENSE
--rw-rw-rw-   0        0        0     3946 2023-05-12 19:53:06.060374 devpytools-0.1.0.dev5/PKG-INFO
--rw-rw-rw-   0        0        0     2140 2023-05-11 16:51:43.000000 devpytools-0.1.0.dev5/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:05.967623 devpytools-0.1.0.dev5/devpytools/
--rw-rw-rw-   0        0        0       45 2022-04-23 18:37:52.000000 devpytools-0.1.0.dev5/devpytools/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:06.043420 devpytools-0.1.0.dev5/devpytools/cacher/
--rw-rw-rw-   0        0        0      154 2022-10-09 09:16:26.000000 devpytools-0.1.0.dev5/devpytools/cacher/__init__.py
--rw-rw-rw-   0        0        0     2785 2022-10-10 18:41:26.000000 devpytools-0.1.0.dev5/devpytools/cacher/cache_provider.py
--rw-rw-rw-   0        0        0     8290 2023-05-12 19:49:43.000000 devpytools-0.1.0.dev5/devpytools/cacher/cacher.py
--rw-rw-rw-   0        0        0      654 2022-10-05 20:22:46.000000 devpytools-0.1.0.dev5/devpytools/cacher/extensions.py
--rw-rw-rw-   0        0        0      175 2023-05-12 19:42:30.000000 devpytools-0.1.0.dev5/devpytools/cacher/general.py
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:06.050409 devpytools-0.1.0.dev5/devpytools/other/
--rw-rw-rw-   0        0        0       34 2022-04-23 18:37:34.000000 devpytools-0.1.0.dev5/devpytools/other/__init__.py
--rw-rw-rw-   0        0        0     1408 2022-10-10 19:40:39.000000 devpytools-0.1.0.dev5/devpytools/other/replace.py
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:06.029460 devpytools-0.1.0.dev5/devpytools.egg-info/
--rw-rw-rw-   0        0        0     3946 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      541 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       11 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev5/devpytools.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 19:53:06.062369 devpytools-0.1.0.dev5/setup.cfg
--rw-rw-rw-   0        0        0     1426 2023-05-12 19:51:52.000000 devpytools-0.1.0.dev5/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-12 19:53:06.057382 devpytools-0.1.0.dev5/tests/
--rw-rw-rw-   0        0        0        0 2022-04-18 15:01:59.000000 devpytools-0.1.0.dev5/tests/__init__.py
--rw-rw-rw-   0        0        0     7546 2023-05-12 19:49:06.000000 devpytools-0.1.0.dev5/tests/test_cacher.py
--rw-rw-rw-   0        0        0      720 2022-10-10 19:39:51.000000 devpytools-0.1.0.dev5/tests/test_other.py
--rw-rw-rw-   0        0        0      183 2022-10-10 19:56:35.000000 devpytools-0.1.0.dev5/tox.ini
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.129708 devpytools-0.1.0.dev6/
+-rw-rw-rw-   0        0        0     1950 2022-10-05 19:38:35.000000 devpytools-0.1.0.dev6/.gitignore
+-rw-rw-rw-   0        0        0     1085 2022-04-16 14:06:14.000000 devpytools-0.1.0.dev6/LICENSE
+-rw-rw-rw-   0        0        0     3946 2023-05-13 11:08:25.128712 devpytools-0.1.0.dev6/PKG-INFO
+-rw-rw-rw-   0        0        0     2140 2023-05-11 16:51:43.000000 devpytools-0.1.0.dev6/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.069867 devpytools-0.1.0.dev6/devpytools/
+-rw-rw-rw-   0        0        0       45 2022-04-23 18:37:52.000000 devpytools-0.1.0.dev6/devpytools/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.118750 devpytools-0.1.0.dev6/devpytools/cacher/
+-rw-rw-rw-   0        0        0      154 2022-10-09 09:16:26.000000 devpytools-0.1.0.dev6/devpytools/cacher/__init__.py
+-rw-rw-rw-   0        0        0     2785 2022-10-10 18:41:26.000000 devpytools-0.1.0.dev6/devpytools/cacher/cache_provider.py
+-rw-rw-rw-   0        0        0     8566 2023-05-13 10:00:52.000000 devpytools-0.1.0.dev6/devpytools/cacher/cacher.py
+-rw-rw-rw-   0        0        0      654 2022-10-05 20:22:46.000000 devpytools-0.1.0.dev6/devpytools/cacher/extensions.py
+-rw-rw-rw-   0        0        0      175 2023-05-12 19:42:30.000000 devpytools-0.1.0.dev6/devpytools/cacher/general.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.121731 devpytools-0.1.0.dev6/devpytools/other/
+-rw-rw-rw-   0        0        0       34 2022-04-23 18:37:34.000000 devpytools-0.1.0.dev6/devpytools/other/__init__.py
+-rw-rw-rw-   0        0        0     1408 2022-10-10 19:40:39.000000 devpytools-0.1.0.dev6/devpytools/other/replace.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.108765 devpytools-0.1.0.dev6/devpytools.egg-info/
+-rw-rw-rw-   0        0        0     3946 2023-05-13 11:08:24.000000 devpytools-0.1.0.dev6/devpytools.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      541 2023-05-13 11:08:24.000000 devpytools-0.1.0.dev6/devpytools.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 11:08:24.000000 devpytools-0.1.0.dev6/devpytools.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-05-12 19:53:05.000000 devpytools-0.1.0.dev6/devpytools.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       11 2023-05-13 11:08:24.000000 devpytools-0.1.0.dev6/devpytools.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 11:08:24.000000 devpytools-0.1.0.dev6/devpytools.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 11:08:25.130705 devpytools-0.1.0.dev6/setup.cfg
+-rw-rw-rw-   0        0        0     1426 2023-05-13 11:07:36.000000 devpytools-0.1.0.dev6/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:08:25.126717 devpytools-0.1.0.dev6/tests/
+-rw-rw-rw-   0        0        0        0 2022-04-18 15:01:59.000000 devpytools-0.1.0.dev6/tests/__init__.py
+-rw-rw-rw-   0        0        0     7614 2023-05-13 09:57:52.000000 devpytools-0.1.0.dev6/tests/test_cacher.py
+-rw-rw-rw-   0        0        0      720 2022-10-10 19:39:51.000000 devpytools-0.1.0.dev6/tests/test_other.py
+-rw-rw-rw-   0        0        0      183 2022-10-10 19:56:35.000000 devpytools-0.1.0.dev6/tox.ini
```

### Comparing `devpytools-0.1.0.dev5/.gitignore` & `devpytools-0.1.0.dev6/.gitignore`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/LICENSE` & `devpytools-0.1.0.dev6/LICENSE`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/PKG-INFO` & `devpytools-0.1.0.dev6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: devpytools
-Version: 0.1.0.dev5
+Version: 0.1.0.dev6
 Summary: Various dev tools.
 Home-page: https://github.com/glowlex/devpytools
 Author: glowlex
 Author-email: antonioavocado777@gmail.com
 License: MIT
 Description: # devpytools
         Tools for development.
```

### Comparing `devpytools-0.1.0.dev5/README.md` & `devpytools-0.1.0.dev6/README.md`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/devpytools/cacher/cache_provider.py` & `devpytools-0.1.0.dev6/devpytools/cacher/cache_provider.py`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/devpytools/cacher/cacher.py` & `devpytools-0.1.0.dev6/devpytools/cacher/cacher.py`

 * *Files 3% similar despite different names*

```diff
@@ -38,40 +38,42 @@
         @param tmpDirPath:
             folder where pickled files will be stored, if None inmemory store will be used
         @param isExpired:
             function to determine if cached result is expired
             args is (resultCreationTime, result)
             has pre-prepeared functions in devpytools.cacher.extensions
         @param isLocal:
-            if True then Cacher not added to global store and cannot be obtained by getCacher func call
+            if True then the Cacher not added to the global store and cannot be obtained by getCacher func call
         @param uniqueKey:
             list of args to use for unique key creation or
             should return string that represents the result uniqueness by the function args
             used as part of cache filename
             by default picks args of (str, int, float) types and return a hash of their tuple
         @param isEnable:
             is cache functionality is enabled
         @param cacheProvider:
             use given cacheProvider
         @param isSavable:
             function to determine if the result of wrapped function should be cached
             by default only positive results cached
         @param version:
             added to names of cached results and can be used for fast switching
-        >>> c = Cacher(name="dev")
-        >>> c.cache()
+        >>> c = Cacher(tmpDirPath="./tmp")
+        >>> c.cache
         >>> def a(b):
         >>>     ...
         # or
         >>> c = Cacher(name="dev", tmpDirPath="./tmp", isEnable=os.getenv("IS_DEV", "")=="true",\
         >>>            isExpired=extensions.expireAfterHours(1), version=1)
         >>> c.cache()
         >>> def a(b):
         >>>     ...
         '''
+        if name is None:
+            isLocal = True
         if not isLocal:
             if CACHER_MAP.get(name):
                 raise ValueError('name should be unique across process')
             CACHER_MAP[name] = self
         self.name = name
         self.tmpDirPath = tmpDirPath
         self.isExpired = isExpired
@@ -174,25 +176,30 @@
             res = func(*args, **kwargs)
             if not self.isSavable or self.isSavable(res):
                 self.cacheProvider.setData(hsh, self.version, func, res, kw.arguments)
             return res
         return cast(FuncType, decorated)
 
 
-
-CACHER_MAP[None] = Cacher()
-
-
 def getCacher(name: Optional[str] = None):
     '''
-    returns previously initiated cacher by name or returns a default if none is found
+    returns previously initiated cacher by name or raise KeyError
     >>> cacher = getCacher()
+    # or
+    >>> Cacher('dev', tmpDirPath="./tmp")
+    ...
+    >>> cacher = getCacher('dev')
 
-    >>> @cacher.cache()
+    >>> @cacher.cache
     >>> def a(b):
     >>>     ...
     # or
-    >>> @cacher.cache(tmpDirPath='./tmp')
+    >>> @cacher.cache(tmpDirPath='../tmp2')
     >>> def a(b):
     >>>     ...
     >>> '''
-    return CACHER_MAP.get(name, CACHER_MAP[None])
+    if name is None and not CACHER_MAP.get(name):
+        CACHER_MAP[None] = Cacher(tmpDirPath="./tmp")
+    r = CACHER_MAP.get(name)
+    if not r:
+        raise KeyError(f'cacher {name} not found')
+    return r
```

### Comparing `devpytools-0.1.0.dev5/devpytools/cacher/extensions.py` & `devpytools-0.1.0.dev6/devpytools/cacher/extensions.py`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/devpytools/other/replace.py` & `devpytools-0.1.0.dev6/devpytools/other/replace.py`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/devpytools.egg-info/PKG-INFO` & `devpytools-0.1.0.dev6/devpytools.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: devpytools
-Version: 0.1.0.dev5
+Version: 0.1.0.dev6
 Summary: Various dev tools.
 Home-page: https://github.com/glowlex/devpytools
 Author: glowlex
 Author-email: antonioavocado777@gmail.com
 License: MIT
 Description: # devpytools
         Tools for development.
```

### Comparing `devpytools-0.1.0.dev5/devpytools.egg-info/SOURCES.txt` & `devpytools-0.1.0.dev6/devpytools.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `devpytools-0.1.0.dev5/setup.py` & `devpytools-0.1.0.dev6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='devpytools',
-    version='0.1.0.dev5',
+    version='0.1.0.dev6',
     description='Various dev tools.',
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url='https://github.com/glowlex/devpytools',
     author='glowlex',
     author_email='antonioavocado777@gmail.com',
     license='MIT',
```

### Comparing `devpytools-0.1.0.dev5/tests/test_cacher.py` & `devpytools-0.1.0.dev6/tests/test_cacher.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 
 @pytest.fixture()
 def inmemResourceSetup(request):
     os.mkdir(TMP_DIR_PATH)
 
     def resource_teardown():
-        c = CACHER_MAP[None]
+        c = getCacher(None)
         CACHER_MAP.clear()
         CACHER_MAP[None] = c
         shutil.rmtree(TMP_DIR_PATH)
     request.addfinalizer(resource_teardown)
 
 
 @pytest.fixture()
@@ -79,35 +79,37 @@
     var = 7
     assert a(1) == 4
     assert countFiles(path) != 0
 
 
 def test_getCacher(inmemResourceSetup):
     c = getCacher()
-    c1 = getCacher('test')
+    try:
+        getCacher('test')
+    except KeyError:
+        pass
+    else:
+        raise Exception('KeyError is not raised')
+    Cacher(name='test')
     c2 = getCacher('test')
     var = 4
 
     @c.cache
     def a(a):
         return var
 
-    @c1.cache
-    def a1(a):
-        return var
-
     @c2.cache
     def a2(a):
         return var
     assert a(1) == 4
-    assert a2(1) == 4
+    var = 5
+    assert a2(1) == 5
     var = 7
     assert a(1) == 4
-    assert a1(2) == 7
-    assert a2(1) == 4
+    assert a2(1) == 5
 
 
 def test_globalCachers(inmemResourceSetup):
     c = Cacher(name='test')
     with pytest.raises(ValueError):
         c = Cacher(name='test')
```

### Comparing `devpytools-0.1.0.dev5/tests/test_other.py` & `devpytools-0.1.0.dev6/tests/test_other.py`

 * *Files identical despite different names*

