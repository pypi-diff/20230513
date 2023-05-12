# Comparing `tmp/handycsv-4.3.0.tar.gz` & `tmp/handycsv-4.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "handycsv-4.3.0.tar", last modified: Thu May  4 02:59:26 2023, max compression
+gzip compressed data, was "handycsv-4.4.0.tar", last modified: Fri May 12 22:01:18 2023, max compression
```

## Comparing `handycsv-4.3.0.tar` & `handycsv-4.4.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-04 02:59:26.061685 handycsv-4.3.0/
--rw-r-----   0 nic       (1000) nic       (1000)     1525 2023-05-02 02:28:44.000000 handycsv-4.3.0/LICENSE
--rw-r-----   0 nic       (1000) nic       (1000)      131 2023-05-02 02:28:44.000000 handycsv-4.3.0/NOTICE
--rw-r-----   0 nic       (1000) nic       (1000)      238 2023-05-04 02:59:26.061685 handycsv-4.3.0/PKG-INFO
--rw-r-----   0 nic       (1000) nic       (1000)       79 2023-05-02 02:28:44.000000 handycsv-4.3.0/README.md
-drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-04 02:59:26.057685 handycsv-4.3.0/handycsv/
--rw-r-----   0 nic       (1000) nic       (1000)     1719 2023-05-04 02:57:07.000000 handycsv-4.3.0/handycsv/__init__.py
--rw-r-----   0 nic       (1000) nic       (1000)     7418 2023-05-03 17:02:59.000000 handycsv-4.3.0/handycsv/column_stats.py
--rw-r-----   0 nic       (1000) nic       (1000)    11803 2023-05-03 17:01:12.000000 handycsv-4.3.0/handycsv/csv.py
--rw-r-----   0 nic       (1000) nic       (1000)    10480 2023-05-03 17:02:56.000000 handycsv-4.3.0/handycsv/grid_stats.py
-drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-04 02:59:26.061685 handycsv-4.3.0/handycsv.egg-info/
--rw-r-----   0 nic       (1000) nic       (1000)      238 2023-05-04 02:59:26.000000 handycsv-4.3.0/handycsv.egg-info/PKG-INFO
--rw-r-----   0 nic       (1000) nic       (1000)      326 2023-05-04 02:59:26.000000 handycsv-4.3.0/handycsv.egg-info/SOURCES.txt
--rw-r-----   0 nic       (1000) nic       (1000)        1 2023-05-04 02:59:26.000000 handycsv-4.3.0/handycsv.egg-info/dependency_links.txt
--rw-r-----   0 nic       (1000) nic       (1000)        9 2023-05-04 02:59:26.000000 handycsv-4.3.0/handycsv.egg-info/top_level.txt
--rw-r-----   0 nic       (1000) nic       (1000)      104 2023-05-04 02:58:40.000000 handycsv-4.3.0/pyproject.toml
--rw-r-----   0 nic       (1000) nic       (1000)       38 2023-05-04 02:59:26.061685 handycsv-4.3.0/setup.cfg
--rw-r-----   0 nic       (1000) nic       (1000)     2473 2023-05-02 02:28:44.000000 handycsv-4.3.0/setup.py
-drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-04 02:59:26.061685 handycsv-4.3.0/test/
--rw-r-----   0 nic       (1000) nic       (1000)     5096 2023-05-03 17:10:43.000000 handycsv-4.3.0/test/test_columnstats.py
--rw-r-----   0 nic       (1000) nic       (1000)    15248 2023-05-04 02:56:41.000000 handycsv-4.3.0/test/test_csv.py
--rw-r-----   0 nic       (1000) nic       (1000)     8794 2023-05-03 17:10:01.000000 handycsv-4.3.0/test/test_gridstats.py
+drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-12 22:01:18.451229 handycsv-4.4.0/
+-rw-r-----   0 nic       (1000) nic       (1000)     1525 2023-05-02 02:28:44.000000 handycsv-4.4.0/LICENSE
+-rw-r-----   0 nic       (1000) nic       (1000)      131 2023-05-02 02:28:44.000000 handycsv-4.4.0/NOTICE
+-rw-r-----   0 nic       (1000) nic       (1000)      238 2023-05-12 22:01:18.451229 handycsv-4.4.0/PKG-INFO
+-rw-r-----   0 nic       (1000) nic       (1000)       79 2023-05-02 02:28:44.000000 handycsv-4.4.0/README.md
+drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-12 22:01:18.451229 handycsv-4.4.0/handycsv/
+-rw-r-----   0 nic       (1000) nic       (1000)     1719 2023-05-12 21:58:55.000000 handycsv-4.4.0/handycsv/__init__.py
+-rw-r-----   0 nic       (1000) nic       (1000)     7454 2023-05-12 22:00:25.000000 handycsv-4.4.0/handycsv/column_stats.py
+-rw-r-----   0 nic       (1000) nic       (1000)    11839 2023-05-12 21:58:03.000000 handycsv-4.4.0/handycsv/csv.py
+-rw-r-----   0 nic       (1000) nic       (1000)    10516 2023-05-12 21:58:28.000000 handycsv-4.4.0/handycsv/grid_stats.py
+drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-12 22:01:18.451229 handycsv-4.4.0/handycsv.egg-info/
+-rw-r-----   0 nic       (1000) nic       (1000)      238 2023-05-12 22:01:18.000000 handycsv-4.4.0/handycsv.egg-info/PKG-INFO
+-rw-r-----   0 nic       (1000) nic       (1000)      326 2023-05-12 22:01:18.000000 handycsv-4.4.0/handycsv.egg-info/SOURCES.txt
+-rw-r-----   0 nic       (1000) nic       (1000)        1 2023-05-12 22:01:18.000000 handycsv-4.4.0/handycsv.egg-info/dependency_links.txt
+-rw-r-----   0 nic       (1000) nic       (1000)        9 2023-05-12 22:01:18.000000 handycsv-4.4.0/handycsv.egg-info/top_level.txt
+-rw-r-----   0 nic       (1000) nic       (1000)      104 2023-05-04 02:58:40.000000 handycsv-4.4.0/pyproject.toml
+-rw-r-----   0 nic       (1000) nic       (1000)       38 2023-05-12 22:01:18.451229 handycsv-4.4.0/setup.cfg
+-rw-r-----   0 nic       (1000) nic       (1000)     2473 2023-05-02 02:28:44.000000 handycsv-4.4.0/setup.py
+drwxr-x---   0 nic       (1000) nic       (1000)        0 2023-05-12 22:01:18.451229 handycsv-4.4.0/test/
+-rw-r-----   0 nic       (1000) nic       (1000)     5096 2023-05-03 17:10:43.000000 handycsv-4.4.0/test/test_columnstats.py
+-rw-r-----   0 nic       (1000) nic       (1000)    15248 2023-05-04 02:56:41.000000 handycsv-4.4.0/test/test_csv.py
+-rw-r-----   0 nic       (1000) nic       (1000)     8794 2023-05-03 17:10:01.000000 handycsv-4.4.0/test/test_gridstats.py
```

### Comparing `handycsv-4.3.0/LICENSE` & `handycsv-4.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `handycsv-4.3.0/handycsv/__init__.py` & `handycsv-4.4.0/handycsv/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -29,8 +29,8 @@
  * POSSIBILITY OF SUCH DAMAGE.
 """
 
 from .column_stats import ColumnStats
 from .csv import Csv
 from .grid_stats import GridStats
 
-__version__ = '4.3.0'
+__version__ = '4.4.0'
```

### Comparing `handycsv-4.3.0/handycsv/column_stats.py` & `handycsv-4.4.0/handycsv/column_stats.py`

 * *Files 2% similar despite different names*

```diff
@@ -150,23 +150,23 @@
 
   def pretty(self, precision=None, right_align=False):
     """
     Returns a pretty string.
     """
     return self.csv.pretty(precision=precision, right_align=right_align)
 
-  def write(self, filename, transpose=False):
+  def write(self, filename, transpose=False, delimiter=','):
     """
     Write the ColumnStats to a CSV file
 
     Args:
       filename (str)   : name of file to write (auto .gz if given)
       transpose (bool) : transpose the ColumnStats before writing
     """
-    self.csv.write(filename, transpose=transpose)
+    self.csv.write(filename, transpose=transpose, delimiter=delimiter)
 
   def get(self, row, default=None):
     """
     Gets a value by reference of row
 
     Args:
       row     : row specifier
```

### Comparing `handycsv-4.3.0/handycsv/csv.py` & `handycsv-4.4.0/handycsv/csv.py`

 * *Files 4% similar despite different names*

```diff
@@ -222,15 +222,15 @@
 
     # Creates the final string
     pcsv = ''
     for row in raw:
       pcsv += (' '.join(row)).rstrip() + '\n'
     return pcsv
 
-  def write(self, filename, transpose=False):
+  def write(self, filename, transpose=False, delimiter=','):
     """
     Write the CSV to a file.
 
     Args:
       filename (str)   : name of file to write (auto .gz if given)
       transpose (bool) : transpose before writing
     """
@@ -238,15 +238,15 @@
 
     if not csv.raw:
       raise ValueError('unintialized CSV can not be written to a file')
 
     # open file to write
     opener = gzip.open if filename.endswith('.gz') else open
     with opener(filename, 'wb') as fd:
-      fd.write(bytes(csv.__str__(), 'utf-8'))
+      fd.write(bytes(csv.to_string(delimiter=delimiter), 'utf-8'))
 
   def get_row(self, row):
     """
     Returns a whole row.
 
     Args:
       row (int) : row index
```

### Comparing `handycsv-4.3.0/handycsv/grid_stats.py` & `handycsv-4.4.0/handycsv/grid_stats.py`

 * *Files 0% similar despite different names*

```diff
@@ -177,23 +177,23 @@
 
   def pretty(self, precision=None, right_align=False):
     """
     Returns a pretty string.
     """
     return self.csv.pretty(precision=precision, right_align=right_align)
 
-  def write(self, filename, transpose=False):
+  def write(self, filename, transpose=False, delimiter=','):
     """
     Write the GridStats to a CSV file
 
     Args:
       filename (str)   : name of file to write (auto .gz if given)
       transpose (bool) : transpose the ColumnStats before writing
     """
-    self.csv.write(filename, transpose=transpose)
+    self.csv.write(filename, transpose=transpose, delimiter=delimiter)
 
   def get(self, row, column, default=None):
     """
     Gets a value by reference of row and column
 
     Args:
       row     : row specifier
```

### Comparing `handycsv-4.3.0/setup.py` & `handycsv-4.4.0/setup.py`

 * *Files identical despite different names*

### Comparing `handycsv-4.3.0/test/test_columnstats.py` & `handycsv-4.4.0/test/test_columnstats.py`

 * *Files identical despite different names*

### Comparing `handycsv-4.3.0/test/test_csv.py` & `handycsv-4.4.0/test/test_csv.py`

 * *Files identical despite different names*

### Comparing `handycsv-4.3.0/test/test_gridstats.py` & `handycsv-4.4.0/test/test_gridstats.py`

 * *Files identical despite different names*

