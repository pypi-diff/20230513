# Comparing `tmp/SummarizeGPT-0.1.tar.gz` & `tmp/SummarizeGPT-1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SummarizeGPT-0.1.tar", last modified: Sat May 13 19:56:12 2023, max compression
+gzip compressed data, was "SummarizeGPT-1.0.tar", last modified: Sat May 13 20:10:18 2023, max compression
```

## Comparing `SummarizeGPT-0.1.tar` & `SummarizeGPT-1.0.tar`

### file list

```diff
@@ -1,18 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 19:56:12.107801 SummarizeGPT-0.1/
--rw-rw-rw-   0        0        0    35823 2023-05-13 17:55:48.000000 SummarizeGPT-0.1/LICENSE
--rw-rw-rw-   0        0        0     8086 2023-05-13 19:56:12.106726 SummarizeGPT-0.1/PKG-INFO
--rw-rw-rw-   0        0        0     7481 2023-05-13 19:54:32.000000 SummarizeGPT-0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 19:56:12.097600 SummarizeGPT-0.1/SummarizeGPT.egg-info/
--rw-rw-rw-   0        0        0     8086 2023-05-13 19:56:11.000000 SummarizeGPT-0.1/SummarizeGPT.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      318 2023-05-13 19:56:11.000000 SummarizeGPT-0.1/SummarizeGPT.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 19:56:11.000000 SummarizeGPT-0.1/SummarizeGPT.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       17 2023-05-13 19:56:11.000000 SummarizeGPT-0.1/SummarizeGPT.egg-info/requires.txt
--rw-rw-rw-   0        0        0       19 2023-05-13 19:56:11.000000 SummarizeGPT-0.1/SummarizeGPT.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 19:56:12.107801 SummarizeGPT-0.1/setup.cfg
--rw-rw-rw-   0        0        0      853 2023-05-13 16:49:21.000000 SummarizeGPT-0.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:56:12.100835 SummarizeGPT-0.1/summarizeGPT/
--rw-rw-rw-   0        0        0        0 2023-05-13 16:38:58.000000 SummarizeGPT-0.1/summarizeGPT/__init__.py
--rw-rw-rw-   0        0        0     5289 2023-05-13 19:54:04.000000 SummarizeGPT-0.1/summarizeGPT/summarize_directory.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:56:12.105135 SummarizeGPT-0.1/tests/
--rw-rw-rw-   0        0        0        0 2023-05-13 19:34:24.000000 SummarizeGPT-0.1/tests/__init__.py
--rw-rw-rw-   0        0        0     1130 2023-05-13 19:54:01.000000 SummarizeGPT-0.1/tests/test_summarize_directory.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.650961 SummarizeGPT-1.0/
+-rw-rw-rw-   0        0        0    35823 2023-05-13 17:55:48.000000 SummarizeGPT-1.0/LICENSE
+-rw-rw-rw-   0        0        0     8151 2023-05-13 20:10:18.650436 SummarizeGPT-1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     7546 2023-05-13 20:09:03.000000 SummarizeGPT-1.0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.619351 SummarizeGPT-1.0/SummarizeGPT/
+-rw-rw-rw-   0        0        0     5282 2023-05-13 20:07:51.000000 SummarizeGPT-1.0/SummarizeGPT/SummarizeGPT.py
+-rw-rw-rw-   0        0        0        0 2023-05-13 16:38:58.000000 SummarizeGPT-1.0/SummarizeGPT/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.644032 SummarizeGPT-1.0/SummarizeGPT.egg-info/
+-rw-rw-rw-   0        0        0     8151 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      386 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       65 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       17 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       19 2023-05-13 20:10:18.000000 SummarizeGPT-1.0/SummarizeGPT.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:18.647756 SummarizeGPT-1.0/Tests/
+-rw-rw-rw-   0        0        0     1123 2023-05-13 20:08:19.000000 SummarizeGPT-1.0/Tests/Test_SummarizeGPT.py
+-rw-rw-rw-   0        0        0        0 2023-05-13 19:34:24.000000 SummarizeGPT-1.0/Tests/__init__.py
+-rw-rw-rw-   0        0        0       42 2023-05-13 20:10:18.651619 SummarizeGPT-1.0/setup.cfg
+-rw-rw-rw-   0        0        0      983 2023-05-13 20:10:12.000000 SummarizeGPT-1.0/setup.py
```

### Comparing `SummarizeGPT-0.1/LICENSE` & `SummarizeGPT-1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `SummarizeGPT-0.1/PKG-INFO` & `SummarizeGPT-1.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: SummarizeGPT
-Version: 0.1
+Version: 1.0
 Summary: Tool to summarize directories of code for prompting with ChatGPT
 Home-page: https://github.com/Maralai/SummarizeGPT
 Author: Matt Harrison
 Author-email: matt@harrison.consulting
 License: GPLv3
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![GitHub Workflow Status](https://img.shields.io/github/workflow/status/Maralai/SummarizeGPT/Test%20Summarize%20GPT)
+[![Test Summarize GPT](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml/badge.svg)](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml)
 
 # Code Summarization Tool
 
 This tool generates a summary of a directory's contents, including a tree view of its subdirectories and files, and the contents of each file. It can optionally exclude files listed in a .gitignore file, exclude or include Docker files, or filter files based on their extensions.
 
 ## Installation
```

### Comparing `SummarizeGPT-0.1/README.md` & `SummarizeGPT-1.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-![GitHub Workflow Status](https://img.shields.io/github/workflow/status/Maralai/SummarizeGPT/Test%20Summarize%20GPT)
+[![Test Summarize GPT](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml/badge.svg)](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml)
 
 # Code Summarization Tool
 
 This tool generates a summary of a directory's contents, including a tree view of its subdirectories and files, and the contents of each file. It can optionally exclude files listed in a .gitignore file, exclude or include Docker files, or filter files based on their extensions.
 
 ## Installation
```

### Comparing `SummarizeGPT-0.1/SummarizeGPT.egg-info/PKG-INFO` & `SummarizeGPT-1.0/SummarizeGPT.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: SummarizeGPT
-Version: 0.1
+Version: 1.0
 Summary: Tool to summarize directories of code for prompting with ChatGPT
 Home-page: https://github.com/Maralai/SummarizeGPT
 Author: Matt Harrison
 Author-email: matt@harrison.consulting
 License: GPLv3
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![GitHub Workflow Status](https://img.shields.io/github/workflow/status/Maralai/SummarizeGPT/Test%20Summarize%20GPT)
+[![Test Summarize GPT](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml/badge.svg)](https://github.com/Maralai/SummarizeGPT/actions/workflows/python-app.yml)
 
 # Code Summarization Tool
 
 This tool generates a summary of a directory's contents, including a tree view of its subdirectories and files, and the contents of each file. It can optionally exclude files listed in a .gitignore file, exclude or include Docker files, or filter files based on their extensions.
 
 ## Installation
```

### Comparing `SummarizeGPT-0.1/setup.py` & `SummarizeGPT-1.0/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     required = f.read().splitlines()
 
 setup(
     name='SummarizeGPT',
-    version='0.1',
+    version='1.0',
     packages=find_packages(),
     description='Tool to summarize directories of code for prompting with ChatGPT',
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     author='Matt Harrison',
     author_email='matt@harrison.consulting',
     license='GPLv3',
@@ -18,8 +18,13 @@
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
     ],
     install_requires=required,
+    entry_points={
+        'console_scripts': [
+            'SummarizeGPT=summarizeGPT.summarizeGPT:main',
+        ],
+    },
 )
```

### Comparing `SummarizeGPT-0.1/summarizeGPT/summarize_directory.py` & `SummarizeGPT-1.0/SummarizeGPT/SummarizeGPT.py`

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
-                if file.lower().endswith(('.env', 'license', 'gitignore', 'setup.py', '__init__.py', 'test_summarize_directory.py')) or any(substring in file.lower() for substring in excluded_files):
+                if file.lower().endswith(('.env', 'license', 'gitignore', 'setup.py', '__init__.py', 'test_summarizegpt.py')) or any(substring in file.lower() for substring in excluded_files):
                     continue
             elif show_only_docker:
                 if not any(substring in file.lower() for substring in ['docker', 'Dockerfile', 'requirements.txt']):
                     continue
 
             if file == output_file:
                 continue
```

### Comparing `SummarizeGPT-0.1/tests/test_summarize_directory.py` & `SummarizeGPT-1.0/Tests/Test_SummarizeGPT.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import os
 import unittest
-from summarizeGPT.summarize_directory import summarize_directory
+from SummarizeGPT.SummarizeGPT import summarize_directory
 
 class TestSummarizeDirectory(unittest.TestCase):
     def setUp(self):
         self.directory = os.path.dirname(os.path.dirname(os.path.realpath(__file__)))
         self.gitignore_file = os.path.join(self.directory, '.gitignore')
 
     def test_gitignore(self):
```

