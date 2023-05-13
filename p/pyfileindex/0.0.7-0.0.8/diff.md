# Comparing `tmp/pyfileindex-0.0.7.tar.gz` & `tmp/pyfileindex-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyfileindex-0.0.7.tar", last modified: Thu Oct 13 21:04:50 2022, max compression
+gzip compressed data, was "pyfileindex-0.0.8.tar", last modified: Sat May 13 00:14:10 2023, max compression
```

## Comparing `pyfileindex-0.0.7.tar` & `pyfileindex-0.0.8.tar`

### file list

```diff
@@ -1,18 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/
--rw-r--r--   0 runner    (1001) docker     (121)     1511 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       70 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)      802 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2704 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/pyfileindex/
--rw-r--r--   0 runner    (1001) docker     (121)      167 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/pyfileindex/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      496 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/pyfileindex/_version.py
--rw-r--r--   0 runner    (1001) docker     (121)     8436 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/pyfileindex/pyfileindex.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/pyfileindex.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)      802 2022-10-13 21:04:50.000000 pyfileindex-0.0.7/pyfileindex.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      311 2022-10-13 21:04:50.000000 pyfileindex-0.0.7/pyfileindex.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-13 21:04:50.000000 pyfileindex-0.0.7/pyfileindex.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       30 2022-10-13 21:04:50.000000 pyfileindex-0.0.7/pyfileindex.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-10-13 21:04:50.000000 pyfileindex-0.0.7/pyfileindex.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      183 2022-10-13 21:04:50.082669 pyfileindex-0.0.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1248 2022-10-13 21:04:49.000000 pyfileindex-0.0.7/setup.py
--rw-r--r--   0 runner    (1001) docker     (121)    68611 2022-10-13 21:04:41.000000 pyfileindex-0.0.7/versioneer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/
+-rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      853 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2762 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/pyfileindex/
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/pyfileindex/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/pyfileindex/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9582 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/pyfileindex/pyfileindex.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/pyfileindex.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      853 2023-05-13 00:14:10.000000 pyfileindex-0.0.8/pyfileindex.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      337 2023-05-13 00:14:10.000000 pyfileindex-0.0.8/pyfileindex.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:14:10.000000 pyfileindex-0.0.8/pyfileindex.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-13 00:14:10.000000 pyfileindex-0.0.8/pyfileindex.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 00:14:10.000000 pyfileindex-0.0.8/pyfileindex.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1307 2023-05-13 00:14:09.000000 pyfileindex-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:10.417634 pyfileindex-0.0.8/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)    15991 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/tests/test_pyfileindex.py
+-rw-r--r--   0 runner    (1001) docker     (123)    68611 2023-05-13 00:14:04.000000 pyfileindex-0.0.8/versioneer.py
```

### Comparing `pyfileindex-0.0.7/LICENSE` & `pyfileindex-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `pyfileindex-0.0.7/PKG-INFO` & `pyfileindex-0.0.8/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyfileindex
-Version: 0.0.7
+Version: 0.0.8
 Summary: pyfileindex - pythonic file system index
 Home-page: https://github.com/pyfileindex/pyfileindex
 Author: Jan Janssen
 Author-email: janssen@mpie.de
 License: BSD
 Keywords: pyfileindex
 Classifier: Development Status :: 5 - Production/Stable
@@ -12,10 +12,11 @@
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Science/Research
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 License-File: LICENSE
 
 pyfileindex creates a dynamic file system index inside a pandas DataFrame.
```

### Comparing `pyfileindex-0.0.7/README.md` & `pyfileindex-0.0.8/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # pyfileindex
 PyFileIndex - pythonic file system index 
 
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/61d50c2f9f5f404f879a02650ff3da35)](https://www.codacy.com/app/jan-janssen/pyfileindex?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=pyfileindex/pyfileindex&amp;utm_campaign=Badge_Grade)
 [![Python package](https://github.com/pyiron/pyfileindex/workflows/Python%20package/badge.svg)](https://github.com/pyiron/pyfileindex/actions)
-[![Coverage Status](https://coveralls.io/repos/github/pyiron/pyfileindex/badge.svg?branch=master)](https://coveralls.io/github/pyiron/pyfileindex?branch=master)
-[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pyiron/pyfileindex/master?filepath=notebooks%2Fdemo.ipynb)
+[![Coverage Status](https://coveralls.io/repos/github/pyiron/pyfileindex/badge.svg?branch=main)](https://coveralls.io/github/pyiron/pyfileindex?branch=main)
+[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pyiron/pyfileindex/main?filepath=notebooks%2Fdemo.ipynb)
 
 The pyfileindex helps to keep track of files in a specific directory, to monitor added files, modified files and deleted files. The module is compatible with Python 3.7 or later but restricted to Unix-like system - Windows is not supported. 
 
 ![Preview](pyfileindex.gif)
 
 # Installation
 The pyfileindex can either be installed via pip using:
@@ -37,19 +37,23 @@
 
     pfi.dataframe 
 
 Update file system index: 
 
     pfi.update()
 
-For more details, take a look at the example notebook: https://github.com/pyiron/pyfileindex/blob/master/notebooks/demo.ipynb
+And open a subdirectory using: 
+
+    pfi.open(path='subdirectory')
+
+For more details, take a look at the example notebook: https://github.com/pyiron/pyfileindex/blob/main/notebooks/demo.ipynb
 
 
 # License
-The pyfileindex is released under the BSD license https://github.com/pyiron/pyfileindex/blob/master/LICENSE . It is a spin-off of the pyiron project https://github.com/pyiron/pyiron therefore if you use the pyfileindex for your publication, please cite: 
+The pyfileindex is released under the BSD license https://github.com/pyiron/pyfileindex/blob/main/LICENSE . It is a spin-off of the pyiron project https://github.com/pyiron/pyiron therefore if you use the pyfileindex for your publication, please cite: 
 
     @article{pyiron-paper,
       title = {pyiron: An integrated development environment for computational materials science},
       journal = {Computational Materials Science},
       volume = {163},
       pages = {24 - 36},
       year = {2019},
```

### Comparing `pyfileindex-0.0.7/pyfileindex/pyfileindex.py` & `pyfileindex-0.0.8/pyfileindex/pyfileindex.py`

 * *Files 13% similar despite different names*

```diff
@@ -10,35 +10,90 @@
 
 class PyFileIndex(object):
     """
     The PyFileIndex maintains a pandas Dataframe to track changes in the file system.
 
     Args:
         path (str): file system path
-        filter_function (function): function to filter for specific files
-        debug (bool): enable debug print statements
+        filter_function (function): function to filter for specific files (optional)
+        debug (bool): enable debug print statements (optional)
+        df (pandas.DataFrame): DataFrame of a previous PyFileIndex object (optional)
     """
 
-    def __init__(self, path=".", filter_function=None, debug=False):
+    def __init__(self, path=".", filter_function=None, debug=False, df=None):
         self._debug = debug
         self._filter_function = filter_function
-        path = os.path.abspath(path)
-        self._df = self._create_df_from_lst(
-            list([self._get_lst_entry_from_path(entry=path)])
-            + list(self._scandir(path=path, df=None, recursive=True))
-        )
+        self._path = os.path.abspath(os.path.expanduser(path))
+        if df is None:
+            self._df = self._create_df_from_lst(
+                list([self._get_lst_entry_from_path(entry=self._path)])
+                + list(self._scandir(path=self._path, df=None, recursive=True))
+            )
+        else:
+            self._df = df
 
     @property
     def df(self):
         return self._df
 
     @property
     def dataframe(self):
         return self.df
 
+    def open(self, path):
+        """
+        Open PyFileIndex in the subdirectory path
+
+        Args:
+             path (str): subdirectory to open
+
+        Returns:
+            PyFileIndex: PyFileIndex for subdirectory
+        """
+        abs_path = os.path.abspath(os.path.expanduser(os.path.join(self._path, path)))
+        if abs_path == self._path:
+            return self
+        elif os.path.commonpath([abs_path, self._path]) == self._path:
+            return PyFileIndex(
+                path=abs_path,
+                filter_function=self._filter_function,
+                debug=self._debug,
+                df=self._df[self._df["path"].str.contains(abs_path)],
+            )
+        else:
+            return PyFileIndex(
+                path=abs_path, filter_function=self._filter_function, debug=self._debug
+            )
+
+    def update(self):
+        """
+        Update file index
+        """
+        df_new, files_changed_lst, path_deleted_lst = self._get_changes_quick()
+        if self._debug:
+            print("Changes: ", df_new.path.values, files_changed_lst, path_deleted_lst)
+        if len(path_deleted_lst) != 0:
+            self._df = self._df[~self._df.path.isin(path_deleted_lst)]
+        if len(files_changed_lst) != 0:
+            df_updated = self._create_df_from_lst(
+                [self._get_lst_entry_from_path(entry=f) for f in files_changed_lst]
+            )
+            self._df = self._df[~self._df.path.isin(df_updated.path)]
+            self._df = (
+                pandas.concat([self._df, df_updated])
+                .drop_duplicates()
+                .reset_index(drop=True)
+            )
+        if len(df_new) != 0:
+            self._df = (
+                pandas.concat([self._df, df_new])
+                .drop_duplicates()
+                .reset_index(drop=True)
+            )
+
     def _init_df_lst(self, path_lst, df=None, include_root=True):
         """
         Internal function to build the pandas file index from a list of directories
 
         Args:
             path_lst (list): list of directories to scan
             df (pandas.DataFrame/ None): existing file index table
@@ -114,40 +169,14 @@
         else:
             files_changed_lst, dir_changed_lst = [], []
         df_new = self._init_df_lst(
             path_lst=dir_changed_lst, df=df_exists, include_root=False
         )
         return df_new, files_changed_lst, path_deleted_lst
 
-    def update(self):
-        """
-        Update file index
-        """
-        df_new, files_changed_lst, path_deleted_lst = self._get_changes_quick()
-        if self._debug:
-            print("Changes: ", df_new.path.values, files_changed_lst, path_deleted_lst)
-        if len(path_deleted_lst) != 0:
-            self._df = self._df[~self._df.path.isin(path_deleted_lst)]
-        if len(files_changed_lst) != 0:
-            df_updated = self._create_df_from_lst(
-                [self._get_lst_entry_from_path(entry=f) for f in files_changed_lst]
-            )
-            self._df = self._df[~self._df.path.isin(df_updated.path)]
-            self._df = (
-                pandas.concat([self._df, df_updated])
-                .drop_duplicates()
-                .reset_index(drop=True)
-            )
-        if len(df_new) != 0:
-            self._df = (
-                pandas.concat([self._df, df_new])
-                .drop_duplicates()
-                .reset_index(drop=True)
-            )
-
     def _get_lst_entry_from_path(self, entry):
         """
         Internal function to generate file index entry from file system path
 
         Args:
             entry (str): file system path
 
@@ -246,7 +275,10 @@
                 "path": path_lst,
                 "dirname": dirname_lst,
                 "is_directory": dir_lst,
                 "mtime": mtime_lst,
                 "nlink": nlink_lst,
             }
         )
+
+    def __len__(self):
+        return len(self._df[~self._df.is_directory])
```

### Comparing `pyfileindex-0.0.7/pyfileindex.egg-info/PKG-INFO` & `pyfileindex-0.0.8/pyfileindex.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyfileindex
-Version: 0.0.7
+Version: 0.0.8
 Summary: pyfileindex - pythonic file system index
 Home-page: https://github.com/pyfileindex/pyfileindex
 Author: Jan Janssen
 Author-email: janssen@mpie.de
 License: BSD
 Keywords: pyfileindex
 Classifier: Development Status :: 5 - Production/Stable
@@ -12,10 +12,11 @@
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Science/Research
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 License-File: LICENSE
 
 pyfileindex creates a dynamic file system index inside a pandas DataFrame.
```

### Comparing `pyfileindex-0.0.7/setup.py` & `pyfileindex-0.0.8/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -19,18 +19,19 @@
                  'Topic :: Scientific/Engineering :: Physics',
                  'License :: OSI Approved :: BSD License',
                  'Intended Audience :: Science/Research',
                  'Operating System :: OS Independent',
                  'Programming Language :: Python :: 3.7',
                  'Programming Language :: Python :: 3.8',
                  'Programming Language :: Python :: 3.9',
-                 'Programming Language :: Python :: 3.10'
+                 'Programming Language :: Python :: 3.10',
+                 'Programming Language :: Python :: 3.11'
                 ],
 
     keywords='pyfileindex',
     packages=find_packages(exclude=["*tests*", "*binder*", "*notebooks*"]),
     install_requires=[
-        'pandas>=1.5.0',
+        'pandas>=2.0.1',
         'scandir>=1.10.0'
     ],
     cmdclass=versioneer.get_cmdclass(),
     )
```

### Comparing `pyfileindex-0.0.7/versioneer.py` & `pyfileindex-0.0.8/versioneer.py`

 * *Files identical despite different names*

