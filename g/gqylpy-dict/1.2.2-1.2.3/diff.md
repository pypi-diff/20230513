# Comparing `tmp/gqylpy_dict-1.2.2.tar.gz` & `tmp/gqylpy_dict-1.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gqylpy_dict-1.2.2.tar", last modified: Sun May  7 08:22:57 2023, max compression
+gzip compressed data, was "gqylpy_dict-1.2.3.tar", last modified: Sat May 13 03:08:00 2023, max compression
```

## Comparing `gqylpy_dict-1.2.2.tar` & `gqylpy_dict-1.2.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 08:22:57.212764 gqylpy_dict-1.2.2/
--rw-r--r--   0 runner    (1001) docker     (123)    12343 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2039 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/NOTICE
--rw-r--r--   0 runner    (1001) docker     (123)     1975 2023-05-07 08:22:57.212764 gqylpy_dict-1.2.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      985 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 08:22:57.208764 gqylpy_dict-1.2.2/gqylpy_dict/
--rw-r--r--   0 runner    (1001) docker     (123)     7324 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/gqylpy_dict/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10014 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/gqylpy_dict/g dict.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 08:22:57.208764 gqylpy_dict-1.2.2/gqylpy_dict.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1975 2023-05-07 08:22:57.000000 gqylpy_dict-1.2.2/gqylpy_dict.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      219 2023-05-07 08:22:57.000000 gqylpy_dict-1.2.2/gqylpy_dict.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-07 08:22:57.000000 gqylpy_dict-1.2.2/gqylpy_dict.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-07 08:22:57.000000 gqylpy_dict-1.2.2/gqylpy_dict.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-07 08:22:57.212764 gqylpy_dict-1.2.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-05-07 08:22:46.000000 gqylpy_dict-1.2.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:08:00.791307 gqylpy_dict-1.2.3/
+-rw-r--r--   0 runner    (1001) docker     (123)    12343 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2039 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/NOTICE
+-rw-r--r--   0 runner    (1001) docker     (123)     3954 2023-05-13 03:08:00.791307 gqylpy_dict-1.2.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2870 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:08:00.787307 gqylpy_dict-1.2.3/gqylpy_dict/
+-rw-r--r--   0 runner    (1001) docker     (123)    10919 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/gqylpy_dict/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10140 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/gqylpy_dict/g dict.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:08:00.791307 gqylpy_dict-1.2.3/gqylpy_dict.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3954 2023-05-13 03:08:00.000000 gqylpy_dict-1.2.3/gqylpy_dict.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-05-13 03:08:00.000000 gqylpy_dict-1.2.3/gqylpy_dict.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:08:00.000000 gqylpy_dict-1.2.3/gqylpy_dict.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 03:08:00.000000 gqylpy_dict-1.2.3/gqylpy_dict.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 03:08:00.791307 gqylpy_dict-1.2.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-05-13 03:07:45.000000 gqylpy_dict-1.2.3/setup.py
```

### Comparing `gqylpy_dict-1.2.2/LICENSE` & `gqylpy_dict-1.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `gqylpy_dict-1.2.2/NOTICE` & `gqylpy_dict-1.2.3/NOTICE`

 * *Files identical despite different names*

### Comparing `gqylpy_dict-1.2.2/gqylpy_dict/g dict.py` & `gqylpy_dict-1.2.3/gqylpy_dict/g dict.py`

 * *Files 2% similar despite different names*

```diff
@@ -108,15 +108,15 @@
     def __init__(self, __data__=None, /, **data):
         if __data__ is None:
             __data__ = data
         else:
             __data__.update(data)
 
         for name, value in __data__.items():
-            self[name] = value
+            dict.__setitem__(self, name, GqylpyDict(value))
 
     def __new__(cls, __data__={}, /, **data):
         if isinstance(__data__, dict):
             return dict.__new__(cls)
 
         if isinstance(__data__, (list, tuple)):
             return __data__.__class__(cls(v) for v in __data__)
@@ -129,28 +129,32 @@
     def __setattr__(self, name: str, value: Any, /) -> None:
         self[name] = value
 
     def __delattr__(self, name: str, /) -> None:
         del self[name]
 
     def __setitem__(self, name: Hashable, value: Any, /) -> None:
-        dict.__setitem__(self, name, GqylpyDict(value))
+        if not isinstance(value, GqylpyDict):
+            value = GqylpyDict(value)
+        dict.__setitem__(self, name, value)
 
     def __hash__(self) -> int:
         return -2
 
     def __reduce__(self) -> Tuple[Type['GqylpyDict'], Tuple[dict]]:
         return GqylpyDict, (dict(self),)
 
-    def copy(self) -> 'GqylpyDict':
+    def __copy__(self) -> 'GqylpyDict':
         copied = GqylpyDict()
         for name, value in self.items():
             dict.__setitem__(copied, name, value)
         return copied
 
+    copy = __copy__
+
     def deepcopy(self) -> 'GqylpyDict':
         return GqylpyDict(self)
 
     def update(self, __data__: Optional[dict] = None, /, **data) -> None:
         try:
             dict.update(self, GqylpyDict(
                 *() if __data__ is None else (__data__,), **data
```

### Comparing `gqylpy_dict-1.2.2/setup.py` & `gqylpy_dict-1.2.3/setup.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 import setuptools
 import gqylpy_dict as g
 
-with open(g.__file__, encoding='utf8') as f:
-    for line in f:
-        if line.startswith('@version: ', 4):
-            version = line.split()[-1]
-            break
-    author, email = f.readline().split(maxsplit=1)[-1].rstrip().split()
-    source = f.readline().split()[-1]
+gdoc: list = g.__doc__.split('\n')
+
+for index, line in enumerate(gdoc):
+    if line.startswith('@version: ', 4):
+        version = line.split()[-1]
+        break
+_, author, email = gdoc[index + 1].split()
+source = gdoc[index + 2].split()[-1]
 
 setuptools.setup(
     name=g.__package__,
     version=version,
     author=author,
     author_email=email,
     license='WTFPL,Apache-2.0',
@@ -20,20 +21,21 @@
     description='基于内置 dict，它是对内置 dict 的增强。内置 dict 能做的它都能做，内置'
                 ' dict 不能做的它更能做。',
     long_description=open('README.md', encoding='utf8').read(),
     long_description_content_type='text/markdown',
     packages=[g.__package__],
     python_requires='>=3.8, <4',
     classifiers=[
-        'Environment :: Web Environment',
+        'Development Status :: 5 - Production/Stable',
         'Intended Audience :: Developers',
+        'Natural Language :: Chinese (Simplified)',
+        'Natural Language :: English',
         'Operating System :: OS Independent',
-        'Topic :: Text Processing :: Indexing',
-        'Topic :: Utilities',
-        'Topic :: Internet',
         'Topic :: Software Development :: Libraries :: Python Modules',
+        'Topic :: Artistic Software',
+        'Topic :: Scientific/Engineering :: Mathematics',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
         'Programming Language :: Python :: 3.11'
     ]
 )
```

