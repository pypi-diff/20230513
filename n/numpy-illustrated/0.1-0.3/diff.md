# Comparing `tmp/numpy-illustrated-0.1.tar.gz` & `tmp/numpy-illustrated-0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "numpy-illustrated-0.1.tar", last modified: Fri Apr 14 05:03:03 2023, max compression
+gzip compressed data, was "numpy-illustrated-0.3.tar", last modified: Sat May 13 07:44:15 2023, max compression
```

## Comparing `numpy-illustrated-0.1.tar` & `numpy-illustrated-0.3.tar`

### file list

```diff
@@ -1,14 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-04-14 05:03:03.163244 numpy-illustrated-0.1/
--rw-rw-rw-   0        0        0     1822 2023-04-14 05:03:03.162253 numpy-illustrated-0.1/PKG-INFO
--rw-rw-rw-   0        0        0      995 2023-04-13 18:56:32.000000 numpy-illustrated-0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-04-14 05:03:03.131200 numpy-illustrated-0.1/npi/
--rw-rw-rw-   0        0        0     6009 2023-04-14 04:55:25.000000 numpy-illustrated-0.1/npi/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-14 05:03:03.160195 numpy-illustrated-0.1/numpy_illustrated.egg-info/
--rw-rw-rw-   0        0        0     1822 2023-04-14 05:03:03.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      278 2023-04-14 05:03:03.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-14 05:03:03.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-04-14 05:01:16.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0        6 2023-04-14 05:03:03.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/requires.txt
--rw-rw-rw-   0        0        0        4 2023-04-14 05:03:03.000000 numpy-illustrated-0.1/numpy_illustrated.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-14 05:03:03.163244 numpy-illustrated-0.1/setup.cfg
--rw-rw-rw-   0        0        0     1106 2023-04-14 05:01:47.000000 numpy-illustrated-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:44:15.514379 numpy-illustrated-0.3/
+-rw-rw-rw-   0        0        0     1087 2023-05-11 20:31:05.000000 numpy-illustrated-0.3/LICENSE.txt
+-rw-rw-rw-   0        0        0     8841 2023-05-13 07:44:15.512409 numpy-illustrated-0.3/PKG-INFO
+-rw-rw-rw-   0        0        0     7788 2023-05-11 21:17:33.000000 numpy-illustrated-0.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 07:44:15.466393 numpy-illustrated-0.3/npi/
+-rw-rw-rw-   0        0        0     6974 2023-05-13 07:39:48.000000 numpy-illustrated-0.3/npi/__init__.py
+-rw-rw-rw-   0        0        0     8347 2023-05-13 07:40:10.000000 numpy-illustrated-0.3/npi/pyfind.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:44:15.509378 numpy-illustrated-0.3/numpy_illustrated.egg-info/
+-rw-rw-rw-   0        0        0     8841 2023-05-13 07:44:15.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      304 2023-05-13 07:44:15.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 07:44:15.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-04-14 05:01:16.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0        6 2023-05-13 07:44:15.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        4 2023-05-13 07:44:15.000000 numpy-illustrated-0.3/numpy_illustrated.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 07:44:15.514379 numpy-illustrated-0.3/setup.cfg
+-rw-rw-rw-   0        0        0     1080 2023-05-13 07:41:01.000000 numpy-illustrated-0.3/setup.py
```

### Comparing `numpy-illustrated-0.1/setup.py` & `numpy-illustrated-0.3/setup.py`

 * *Files 18% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import setuptools
 
 with open('README.md', 'r') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name='numpy-illustrated',
-    version='0.1',
+    version='0.3',
     author='Lev Maximov',
     author_email='lev.maximov@gmail.com',
     url='https://github.com/axil/numpy-illustrated',
     description='Helper functions from the NumPy Illustrated guide',
     long_description=long_description,
     long_description_content_type='text/markdown',
     python_requires=">=3.7",
@@ -19,17 +19,16 @@
         'numpy',
     ],
     packages=['npi'],
     classifiers=[
         'Development Status :: 4 - Beta',
         'License :: OSI Approved :: MIT License',
         'Operating System :: OS Independent',
-        'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',    
         'Programming Language :: Python :: 3.10',    
         'Programming Language :: Python :: 3.11',    
     ],
     license='MIT License',
     zip_safe=False,
-    keywords=['find', 'argmin', 'argmax', 'sort', 'irange', 'savez', 'numpy'],
+    keywords=['find', 'argmin', 'argmax', 'sort', 'irange', 'numpy', 'first_above', 'first_nonzero'],
 )
```

