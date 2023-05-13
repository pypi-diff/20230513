# Comparing `tmp/SummarizeGPT-1.0.tar.gz` & `tmp/SummarizeGPT-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SummarizeGPT-1.0.tar", last modified: Sat May 13 20:10:18 2023, max compression
+gzip compressed data, was "SummarizeGPT-1.1.tar", last modified: Sat May 13 20:18:19 2023, max compression
```

## Comparing `SummarizeGPT-1.0.tar` & `SummarizeGPT-1.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.650961 SummarizeGPT-1.0/
--rw-rw-rw-   0        0        0    35823 2023-05-13 17:55:48.000000 SummarizeGPT-1.0/LICENSE
--rw-rw-rw-   0        0        0     8151 2023-05-13 20:10:18.650436 SummarizeGPT-1.0/PKG-INFO
--rw-rw-rw-   0        0        0     7546 2023-05-13 20:09:03.000000 SummarizeGPT-1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.619351 SummarizeGPT-1.0/SummarizeGPT/
--rw-rw-rw-   0        0        0     5282 2023-05-13 20:07:51.000000 SummarizeGPT-1.0/SummarizeGPT/SummarizeGPT.py
--rw-rw-rw-   0        0        0        0 2023-05-13 16:38:58.000000 SummarizeGPT-1.0/SummarizeGPT/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.644032 SummarizeGPT-1.0/SummarizeGPT.egg-info/
--rw-rw-rw-   0        0        0     8151 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      386 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       65 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       17 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/requires.txt
--rw-rw-rw-   0        0        0       19 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.647756 SummarizeGPT-1.0/Tests/
--rw-rw-rw-   0        0        0     1123 2023-05-13 20:08:19.000000 SummarizeGPT-1.0/Tests/Test_SummarizeGPT.py
--rw-rw-rw-   0        0        0        0 2023-05-13 19:34:24.000000 SummarizeGPT-1.0/Tests/__init__.py
--rw-rw-rw-   0        0        0       42 2023-05-13 20:10:18.651619 SummarizeGPT-1.0/setup.cfg
--rw-rw-rw-   0        0        0      983 2023-05-13 20:10:12.000000 SummarizeGPT-1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:19.516163 SummarizeGPT-1.1/
+-rw-rw-rw-   0        0        0    35823 2023-05-13 17:55:48.000000 SummarizeGPT-1.1/LICENSE
+-rw-rw-rw-   0        0        0     8151 2023-05-13 20:18:19.515111 SummarizeGPT-1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     7546 2023-05-13 20:11:27.000000 SummarizeGPT-1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:19.481695 SummarizeGPT-1.1/SummarizeGPT/
+-rw-rw-rw-   0        0        0     5283 2023-05-13 20:16:01.000000 SummarizeGPT-1.1/SummarizeGPT/SummarizeGPT.py
+-rw-rw-rw-   0        0        0        0 2023-05-13 16:38:58.000000 SummarizeGPT-1.1/SummarizeGPT/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:19.508660 SummarizeGPT-1.1/SummarizeGPT.egg-info/
+-rw-rw-rw-   0        0        0     8151 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      416 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       65 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       17 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       19 2023-05-13 20:18:19.000000 SummarizeGPT-1.1/SummarizeGPT.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:19.512992 SummarizeGPT-1.1/Tests/
+-rw-rw-rw-   0        0        0        0 2023-05-13 19:34:24.000000 SummarizeGPT-1.1/Tests/__init__.py
+-rw-rw-rw-   0        0        0     1189 2023-05-13 20:17:57.000000 SummarizeGPT-1.1/Tests/test_summarize_gpt.py
+-rw-rw-rw-   0        0        0       42 2023-05-13 20:18:19.516163 SummarizeGPT-1.1/setup.cfg
+-rw-rw-rw-   0        0        0      983 2023-05-13 20:18:16.000000 SummarizeGPT-1.1/setup.py
```

### Comparing `SummarizeGPT-1.0/LICENSE` & `SummarizeGPT-1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `SummarizeGPT-1.0/PKG-INFO` & `SummarizeGPT-1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SummarizeGPT
-Version: 1.0
+Version: 1.1
 Summary: Tool to summarize directories of code for prompting with ChatGPT
 Home-page: https://github.com/Maralai/SummarizeGPT
 Author: Matt Harrison
 Author-email: matt@harrison.consulting
 License: GPLv3
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SummarizeGPT-1.0/README.md` & `SummarizeGPT-1.1/README.md`

 * *Files identical despite different names*

### Comparing `SummarizeGPT-1.0/SummarizeGPT/SummarizeGPT.py` & `SummarizeGPT-1.1/SummarizeGPT/SummarizeGPT.py`

 * *Files 0% similar despite different names*

```diff
@@ -54,15 +54,15 @@
             _, ext = os.path.splitext(file)
             ext = ext.lower()  # Make the check case-insensitive
             if include_exts is not None and ext not in include_exts:
                 continue
             if exclude_exts is not None and ext in exclude_exts:
                 continue
             if not show_docker and not show_only_docker:
-                if file.lower().endswith(('.env', 'license', 'gitignore', 'setup.py', '__init__.py', 'test_summarizegpt.py')) or any(substring in file.lower() for substring in excluded_files):
+                if file.lower().endswith(('.env', 'license', 'gitignore', 'setup.py', '__init__.py', 'test_summarize_gpt.py')) or any(substring in file.lower() for substring in excluded_files):
                     continue
             elif show_only_docker:
                 if not any(substring in file.lower() for substring in ['docker', 'Dockerfile', 'requirements.txt']):
                     continue
 
             if file == output_file:
                 continue
```

### Comparing `SummarizeGPT-1.0/SummarizeGPT.egg-info/PKG-INFO` & `SummarizeGPT-1.1/SummarizeGPT.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SummarizeGPT
-Version: 1.0
+Version: 1.1
 Summary: Tool to summarize directories of code for prompting with ChatGPT
 Home-page: https://github.com/Maralai/SummarizeGPT
 Author: Matt Harrison
 Author-email: matt@harrison.consulting
 License: GPLv3
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SummarizeGPT-1.0/Tests/Test_SummarizeGPT.py` & `SummarizeGPT-1.1/Tests/test_summarize_gpt.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,27 +1,27 @@
 import os
 import unittest
-from SummarizeGPT.SummarizeGPT import summarize_directory
+from summarizeGPT.summarizeGPT import summarize_directory
 
-class TestSummarizeDirectory(unittest.TestCase):
+class TestSummarizeGPT(unittest.TestCase):
     def setUp(self):
         self.directory = os.path.dirname(os.path.dirname(os.path.realpath(__file__)))
         self.gitignore_file = os.path.join(self.directory, '.gitignore')
 
     def test_gitignore(self):
         # Test that .gitignore is working by checking that LICENSE is not in the summary
         summary = summarize_directory(self.directory, gitignore_file=self.gitignore_file)
         self.assertNotIn('build.README.md', summary)
 
     def test_include(self):
         # Test include and exclude arguments
-        summary = summarize_directory(self.directory, include_exts=['.md'])
+        summary = summarize_directory(self.directory, gitignore_file=self.gitignore_file, include_exts=['.md'])
         self.assertIn('python summarize_directory.py', summary)
             
     def test_exclude(self):
         # Test exclude argument        
-        summary = summarize_directory(self.directory, exclude_exts=['.md'])
+        summary = summarize_directory(self.directory, gitignore_file=self.gitignore_file, exclude_exts=['.md'])
         self.assertNotIn('python summarize_directory.py', summary)  # README.md should be excluded
 
 
 if __name__ == '__main__':
     unittest.main()
```

### Comparing `SummarizeGPT-1.0/setup.py` & `SummarizeGPT-1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     required = f.read().splitlines()
 
 setup(
     name='SummarizeGPT',
-    version='1.0',
+    version='1.1',
     packages=find_packages(),
     description='Tool to summarize directories of code for prompting with ChatGPT',
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     author='Matt Harrison',
     author_email='matt@harrison.consulting',
     license='GPLv3',
```

