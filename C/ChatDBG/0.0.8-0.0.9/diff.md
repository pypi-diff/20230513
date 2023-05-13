# Comparing `tmp/ChatDBG-0.0.8.tar.gz` & `tmp/ChatDBG-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ChatDBG-0.0.8.tar", last modified: Sat Mar 25 23:25:08 2023, max compression
+gzip compressed data, was "ChatDBG-0.0.9.tar", last modified: Tue Mar 28 23:23:15 2023, max compression
```

## Comparing `ChatDBG-0.0.8.tar` & `ChatDBG-0.0.9.tar`

### file list

```diff
@@ -1,32 +1,30 @@
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.703418 ChatDBG-0.0.8/
--rw-r--r--   0 emery      (504) staff       (20)    11357 2023-03-20 19:54:38.000000 ChatDBG-0.0.8/LICENSE
--rw-r--r--   0 emery      (504) staff       (20)     5830 2023-03-25 23:25:08.703270 ChatDBG-0.0.8/PKG-INFO
--rw-r--r--   0 emery      (504) staff       (20)     5348 2023-03-25 23:23:48.000000 ChatDBG-0.0.8/README.md
--rw-r--r--   0 emery      (504) staff       (20)      665 2023-03-25 23:24:36.000000 ChatDBG-0.0.8/pyproject.toml
--rw-r--r--   0 emery      (504) staff       (20)       38 2023-03-25 23:25:08.703456 ChatDBG-0.0.8/setup.cfg
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.696667 ChatDBG-0.0.8/src/
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.698162 ChatDBG-0.0.8/src/ChatDBG.egg-info/
--rw-r--r--   0 emery      (504) staff       (20)     5830 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/PKG-INFO
--rw-r--r--   0 emery      (504) staff       (20)      621 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/SOURCES.txt
--rw-r--r--   0 emery      (504) staff       (20)        1 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/dependency_links.txt
--rw-r--r--   0 emery      (504) staff       (20)       50 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/entry_points.txt
--rw-r--r--   0 emery      (504) staff       (20)       35 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/requires.txt
--rw-r--r--   0 emery      (504) staff       (20)        8 2023-03-25 23:25:08.000000 ChatDBG-0.0.8/src/ChatDBG.egg-info/top_level.txt
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.701631 ChatDBG-0.0.8/src/chatdbg/
--rw-r--r--   0 emery      (504) staff       (20)        0 2023-03-20 22:43:04.000000 ChatDBG-0.0.8/src/chatdbg/__init__.py
--rw-r--r--   0 emery      (504) staff       (20)       73 2023-03-24 01:39:19.000000 ChatDBG-0.0.8/src/chatdbg/__main__.py
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.702257 ChatDBG-0.0.8/src/chatdbg/backup/
--rw-r--r--   0 emery      (504) staff       (20)     8131 2023-03-24 01:42:24.000000 ChatDBG-0.0.8/src/chatdbg/backup/chatdbg_lldb.py
--rw-r--r--   0 emery      (504) staff       (20)     3892 2023-03-22 15:09:26.000000 ChatDBG-0.0.8/src/chatdbg/backup/chatdbg_why.py
--rw-r--r--   0 emery      (504) staff       (20)    64306 2023-03-22 23:38:35.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg-bak.py
--rw-r--r--   0 emery      (504) staff       (20)     3317 2023-03-24 02:28:55.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg.py
--rw-r--r--   0 emery      (504) staff       (20)     7369 2023-03-25 23:21:17.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg_gdb.py
--rw-r--r--   0 emery      (504) staff       (20)     3577 2023-03-23 12:17:58.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg_ipdb.py
--rw-r--r--   0 emery      (504) staff       (20)     9814 2023-03-25 23:19:26.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg_lldb.py
--rw-r--r--   0 emery      (504) staff       (20)     4922 2023-03-24 02:48:53.000000 ChatDBG-0.0.8/src/chatdbg/chatdbg_why.py
--rw-r--r--   0 emery      (504) staff       (20)    63581 2023-03-24 02:16:23.000000 ChatDBG-0.0.8/src/chatdbg/pdb.py
--rw-r--r--   0 emery      (504) staff       (20)     3142 2023-03-22 23:38:34.000000 ChatDBG-0.0.8/src/chatdbg/prompter.py
--rw-r--r--   0 emery      (504) staff       (20)      225 2023-03-23 12:21:24.000000 ChatDBG-0.0.8/src/chatdbg/testme.py
-drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-25 23:25:08.702909 ChatDBG-0.0.8/test/
--rw-r--r--   0 emery      (504) staff       (20)       13 2023-03-22 22:43:17.000000 ChatDBG-0.0.8/test/test-issue1.py
--rw-r--r--   0 emery      (504) staff       (20)      184 2023-03-20 22:41:39.000000 ChatDBG-0.0.8/test/testme.py
+drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-28 23:23:15.382860 ChatDBG-0.0.9/
+-rw-r--r--   0 emery      (504) staff       (20)    11357 2023-03-20 19:54:38.000000 ChatDBG-0.0.9/LICENSE
+-rw-r--r--   0 emery      (504) staff       (20)     5900 2023-03-28 23:23:15.382750 ChatDBG-0.0.9/PKG-INFO
+-rw-r--r--   0 emery      (504) staff       (20)     5418 2023-03-27 06:22:39.000000 ChatDBG-0.0.9/README.md
+-rw-r--r--   0 emery      (504) staff       (20)      665 2023-03-28 23:18:08.000000 ChatDBG-0.0.9/pyproject.toml
+-rw-r--r--   0 emery      (504) staff       (20)       38 2023-03-28 23:23:15.382893 ChatDBG-0.0.9/setup.cfg
+drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-28 23:23:15.380016 ChatDBG-0.0.9/src/
+drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-28 23:23:15.380972 ChatDBG-0.0.9/src/ChatDBG.egg-info/
+-rw-r--r--   0 emery      (504) staff       (20)     5900 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/PKG-INFO
+-rw-r--r--   0 emery      (504) staff       (20)      607 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/SOURCES.txt
+-rw-r--r--   0 emery      (504) staff       (20)        1 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/dependency_links.txt
+-rw-r--r--   0 emery      (504) staff       (20)       50 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/entry_points.txt
+-rw-r--r--   0 emery      (504) staff       (20)       35 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/requires.txt
+-rw-r--r--   0 emery      (504) staff       (20)        8 2023-03-28 23:23:15.000000 ChatDBG-0.0.9/src/ChatDBG.egg-info/top_level.txt
+drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-28 23:23:15.382366 ChatDBG-0.0.9/src/chatdbg/
+-rw-r--r--   0 emery      (504) staff       (20)        0 2023-03-20 22:43:04.000000 ChatDBG-0.0.9/src/chatdbg/__init__.py
+-rw-r--r--   0 emery      (504) staff       (20)       73 2023-03-24 01:39:19.000000 ChatDBG-0.0.9/src/chatdbg/__main__.py
+drwxr-xr-x   0 emery      (504) staff       (20)        0 2023-03-28 23:23:15.382603 ChatDBG-0.0.9/src/chatdbg/backup/
+-rw-r--r--   0 emery      (504) staff       (20)     8131 2023-03-24 01:42:24.000000 ChatDBG-0.0.9/src/chatdbg/backup/chatdbg_lldb.py
+-rw-r--r--   0 emery      (504) staff       (20)     3892 2023-03-22 15:09:26.000000 ChatDBG-0.0.9/src/chatdbg/backup/chatdbg_why.py
+-rw-r--r--   0 emery      (504) staff       (20)    64306 2023-03-22 23:38:35.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg-bak.py
+-rw-r--r--   0 emery      (504) staff       (20)     3317 2023-03-24 02:28:55.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg.py
+-rw-r--r--   0 emery      (504) staff       (20)     7593 2023-03-26 18:06:56.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg_gdb.py
+-rw-r--r--   0 emery      (504) staff       (20)     3577 2023-03-23 12:17:58.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg_ipdb.py
+-rw-r--r--   0 emery      (504) staff       (20)     5933 2023-03-26 18:08:02.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg_lldb.py
+-rw-r--r--   0 emery      (504) staff       (20)     4922 2023-03-24 02:48:53.000000 ChatDBG-0.0.9/src/chatdbg/chatdbg_why.py
+-rw-r--r--   0 emery      (504) staff       (20)    63589 2023-03-27 06:18:33.000000 ChatDBG-0.0.9/src/chatdbg/pdb.py
+-rw-r--r--   0 emery      (504) staff       (20)     3142 2023-03-22 23:38:34.000000 ChatDBG-0.0.9/src/chatdbg/prompter.py
+-rw-r--r--   0 emery      (504) staff       (20)      225 2023-03-23 12:21:24.000000 ChatDBG-0.0.9/src/chatdbg/testme.py
+-rw-r--r--   0 emery      (504) staff       (20)     4368 2023-03-26 18:09:03.000000 ChatDBG-0.0.9/src/chatdbg/utils.py
```

### Comparing `ChatDBG-0.0.8/LICENSE` & `ChatDBG-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/PKG-INFO` & `ChatDBG-0.0.9/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ChatDBG
-Version: 0.0.8
+Version: 0.0.9
 Summary: ChatDBG.
 Author-email: Emery Berger <emery.berger@gmail.com>
 Project-URL: Homepage, https://github.com/plasma-umass/ChatDBG
 Project-URL: Bug Tracker, https://github.com/plasma-umass/ChatDBG
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,17 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # ChatDBG
 
 by [Emery Berger](https://emeryberger.com)
 
-ChatDBG is an experimental debugger (for Python *and* (new) native code) that integrates large language models to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix. As far as we are aware, ChatDBG is the first debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
+ChatDBG is an experimental debugger for Python *and* native code that integrates large language models into a standard debugger (`pdb`, `lldb`, and `gdb`) to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix.
+
+As far as we are aware, ChatDBG is the *first* debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
 
 [![PyPI Latest Release](https://img.shields.io/pypi/v/chatdbg.svg)](https://pypi.org/project/chatdbg/)[![Downloads](https://pepy.tech/badge/chatdbg)](https://pepy.tech/project/chatdbg) [![Downloads](https://pepy.tech/badge/chatdbg/month)](https://pepy.tech/project/chatdbg) ![Python versions](https://img.shields.io/pypi/pyversions/chatdbg.svg?style=flat-square)
 
 
 ## Installation
 
 Install ChatDBG using `pip`:
@@ -46,28 +48,28 @@
 ChatDBG is an extension of the standard Python debugger `pdb`. Like
 `pdb`, when your script encounters an uncaught exception, ChatDBG will
 enter post mortem debugging mode.
 
 Unlike other debuggers, you can then use the `why` command to ask
 ChatDBG why your program failed and get a suggested fix.
 
-For example:
+### Example
 
 ```
 Traceback (most recent call last):
   File "yourscript.py", line 9, in <module>
     print(tryme(100))
   File "yourscript.py", line 4, in tryme
     if x / i > 2:
 ZeroDivisionError: division by zero
 Uncaught exception. Entering post mortem debugging
 Running 'cont' or 'step' will restart the program
 > yourscript.py(4)tryme()
 -> if x / i > 2:
-(Pdb) why
+(ChatDBG Pdb) why
 ```
 
 
 ChatDBG will then provide a helpful explanation of why your program failed and a suggested fix:
 
 ```
 The root cause of the error is that the code is attempting to
@@ -117,15 +119,15 @@
 
 <details>
 <summary>
 <B>Example of using `why` in LLDB</B>
 </summary>
 
 ```
-(lldb) run
+(ChatDBG lldb) run
 Process 91113 launched: '/Users/emery/git/chatdbg/test/a.out' (arm64)
 TEST 1
 TEST -422761288
 TEST 0
 TEST 0
 TEST 0
 TEST 0
@@ -143,15 +145,15 @@
    10    int main()
 Target 0: (a.out) stopped.
 ```
 
 Now you can ask `why`:
 
 ```
-(lldb) why
+(ChatDBG lldb) why
 The root cause of this error is an out-of-bounds memory access. The
 program is trying to access an element of the `x` array that is beyond
 its allocated size. Specifically, when `n` is large enough (greater
 than or equal to 1), the expression `n * 10000` causes the program to
 access memory beyond the end of the `x` array.
 
 To fix this error, we can check that the index is within bounds before
```

### Comparing `ChatDBG-0.0.8/README.md` & `ChatDBG-0.0.9/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 # ChatDBG
 
 by [Emery Berger](https://emeryberger.com)
 
-ChatDBG is an experimental debugger (for Python *and* (new) native code) that integrates large language models to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix. As far as we are aware, ChatDBG is the first debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
+ChatDBG is an experimental debugger for Python *and* native code that integrates large language models into a standard debugger (`pdb`, `lldb`, and `gdb`) to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix.
+
+As far as we are aware, ChatDBG is the *first* debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
 
 [![PyPI Latest Release](https://img.shields.io/pypi/v/chatdbg.svg)](https://pypi.org/project/chatdbg/)[![Downloads](https://pepy.tech/badge/chatdbg)](https://pepy.tech/project/chatdbg) [![Downloads](https://pepy.tech/badge/chatdbg/month)](https://pepy.tech/project/chatdbg) ![Python versions](https://img.shields.io/pypi/pyversions/chatdbg.svg?style=flat-square)
 
 
 ## Installation
 
 Install ChatDBG using `pip`:
@@ -32,28 +34,28 @@
 ChatDBG is an extension of the standard Python debugger `pdb`. Like
 `pdb`, when your script encounters an uncaught exception, ChatDBG will
 enter post mortem debugging mode.
 
 Unlike other debuggers, you can then use the `why` command to ask
 ChatDBG why your program failed and get a suggested fix.
 
-For example:
+### Example
 
 ```
 Traceback (most recent call last):
   File "yourscript.py", line 9, in <module>
     print(tryme(100))
   File "yourscript.py", line 4, in tryme
     if x / i > 2:
 ZeroDivisionError: division by zero
 Uncaught exception. Entering post mortem debugging
 Running 'cont' or 'step' will restart the program
 > yourscript.py(4)tryme()
 -> if x / i > 2:
-(Pdb) why
+(ChatDBG Pdb) why
 ```
 
 
 ChatDBG will then provide a helpful explanation of why your program failed and a suggested fix:
 
 ```
 The root cause of the error is that the code is attempting to
@@ -103,15 +105,15 @@
 
 <details>
 <summary>
 <B>Example of using `why` in LLDB</B>
 </summary>
 
 ```
-(lldb) run
+(ChatDBG lldb) run
 Process 91113 launched: '/Users/emery/git/chatdbg/test/a.out' (arm64)
 TEST 1
 TEST -422761288
 TEST 0
 TEST 0
 TEST 0
 TEST 0
@@ -129,15 +131,15 @@
    10    int main()
 Target 0: (a.out) stopped.
 ```
 
 Now you can ask `why`:
 
 ```
-(lldb) why
+(ChatDBG lldb) why
 The root cause of this error is an out-of-bounds memory access. The
 program is trying to access an element of the `x` array that is beyond
 its allocated size. Specifically, when `n` is large enough (greater
 than or equal to 1), the expression `n * 10000` causes the program to
 access memory beyond the end of the `x` array.
 
 To fix this error, we can check that the index is within bounds before
```

### Comparing `ChatDBG-0.0.8/pyproject.toml` & `ChatDBG-0.0.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ChatDBG"
-version = "0.0.8"
+version = "0.0.9"
 authors = [
   { name="Emery Berger", email="emery.berger@gmail.com" },
 ]
 dependencies = ["openai>=0.27.0", "openai_async>=0.0.3"]
 description = "ChatDBG."
 readme = "README.md"
 requires-python = ">=3.7"
```

### Comparing `ChatDBG-0.0.8/src/ChatDBG.egg-info/PKG-INFO` & `ChatDBG-0.0.9/src/ChatDBG.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ChatDBG
-Version: 0.0.8
+Version: 0.0.9
 Summary: ChatDBG.
 Author-email: Emery Berger <emery.berger@gmail.com>
 Project-URL: Homepage, https://github.com/plasma-umass/ChatDBG
 Project-URL: Bug Tracker, https://github.com/plasma-umass/ChatDBG
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,17 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # ChatDBG
 
 by [Emery Berger](https://emeryberger.com)
 
-ChatDBG is an experimental debugger (for Python *and* (new) native code) that integrates large language models to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix. As far as we are aware, ChatDBG is the first debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
+ChatDBG is an experimental debugger for Python *and* native code that integrates large language models into a standard debugger (`pdb`, `lldb`, and `gdb`) to help debug your code. With ChatDBG, you can ask your debugger "why" your program failed, and it will provide a suggested fix.
+
+As far as we are aware, ChatDBG is the *first* debugger to automatically perform root cause analysis and to provide suggested fixes. This is an alpha release; we greatly welcome feedback and suggestions!
 
 [![PyPI Latest Release](https://img.shields.io/pypi/v/chatdbg.svg)](https://pypi.org/project/chatdbg/)[![Downloads](https://pepy.tech/badge/chatdbg)](https://pepy.tech/project/chatdbg) [![Downloads](https://pepy.tech/badge/chatdbg/month)](https://pepy.tech/project/chatdbg) ![Python versions](https://img.shields.io/pypi/pyversions/chatdbg.svg?style=flat-square)
 
 
 ## Installation
 
 Install ChatDBG using `pip`:
@@ -46,28 +48,28 @@
 ChatDBG is an extension of the standard Python debugger `pdb`. Like
 `pdb`, when your script encounters an uncaught exception, ChatDBG will
 enter post mortem debugging mode.
 
 Unlike other debuggers, you can then use the `why` command to ask
 ChatDBG why your program failed and get a suggested fix.
 
-For example:
+### Example
 
 ```
 Traceback (most recent call last):
   File "yourscript.py", line 9, in <module>
     print(tryme(100))
   File "yourscript.py", line 4, in tryme
     if x / i > 2:
 ZeroDivisionError: division by zero
 Uncaught exception. Entering post mortem debugging
 Running 'cont' or 'step' will restart the program
 > yourscript.py(4)tryme()
 -> if x / i > 2:
-(Pdb) why
+(ChatDBG Pdb) why
 ```
 
 
 ChatDBG will then provide a helpful explanation of why your program failed and a suggested fix:
 
 ```
 The root cause of the error is that the code is attempting to
@@ -117,15 +119,15 @@
 
 <details>
 <summary>
 <B>Example of using `why` in LLDB</B>
 </summary>
 
 ```
-(lldb) run
+(ChatDBG lldb) run
 Process 91113 launched: '/Users/emery/git/chatdbg/test/a.out' (arm64)
 TEST 1
 TEST -422761288
 TEST 0
 TEST 0
 TEST 0
 TEST 0
@@ -143,15 +145,15 @@
    10    int main()
 Target 0: (a.out) stopped.
 ```
 
 Now you can ask `why`:
 
 ```
-(lldb) why
+(ChatDBG lldb) why
 The root cause of this error is an out-of-bounds memory access. The
 program is trying to access an element of the `x` array that is beyond
 its allocated size. Specifically, when `n` is large enough (greater
 than or equal to 1), the expression `n * 10000` causes the program to
 access memory beyond the end of the `x` array.
 
 To fix this error, we can check that the index is within bounds before
```

### Comparing `ChatDBG-0.0.8/src/ChatDBG.egg-info/SOURCES.txt` & `ChatDBG-0.0.9/src/ChatDBG.egg-info/SOURCES.txt`

 * *Files 20% similar despite different names*

```diff
@@ -14,11 +14,10 @@
 src/chatdbg/chatdbg_gdb.py
 src/chatdbg/chatdbg_ipdb.py
 src/chatdbg/chatdbg_lldb.py
 src/chatdbg/chatdbg_why.py
 src/chatdbg/pdb.py
 src/chatdbg/prompter.py
 src/chatdbg/testme.py
+src/chatdbg/utils.py
 src/chatdbg/backup/chatdbg_lldb.py
-src/chatdbg/backup/chatdbg_why.py
-test/test-issue1.py
-test/testme.py
+src/chatdbg/backup/chatdbg_why.py
```

### Comparing `ChatDBG-0.0.8/src/chatdbg/backup/chatdbg_lldb.py` & `ChatDBG-0.0.9/src/chatdbg/backup/chatdbg_lldb.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/backup/chatdbg_why.py` & `ChatDBG-0.0.9/src/chatdbg/backup/chatdbg_why.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/chatdbg-bak.py` & `ChatDBG-0.0.9/src/chatdbg/chatdbg-bak.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/chatdbg.py` & `ChatDBG-0.0.9/src/chatdbg/chatdbg.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/chatdbg_gdb.py` & `ChatDBG-0.0.9/src/chatdbg/chatdbg_gdb.py`

 * *Files 6% similar despite different names*

```diff
@@ -158,17 +158,21 @@
         return ''
 
     stack_trace = ""
     source_code = ""
 
     frames = []
     frame = gdb.selected_frame()
+
+    # magic number - don't bother walking up more than this many frames.
+    # This is just to prevent overwhelming OpenAI (or to cope with a stack overflow!).
+    max_frames = 10
     
     # Walk the stack and build up the frames list.
-    while frame is not None:
+    while frame is not None and max_frames > 0:
         func_name = frame.name()
         symtab_and_line = frame.find_sal()
         if symtab_and_line.symtab is not None:
             filename = symtab_and_line.symtab.filename
         else:
             filename = None
         if symtab_and_line.line is not None:
@@ -183,14 +187,15 @@
         for symbol in block:
             if symbol.is_argument:
                 name = symbol.name
                 value = frame.read_var(name)
                 args.append((name, value))
         frames.append((filename, func_name, args, lineno, colno))
         frame = frame.older()
+        max_frames -= 1
 
     # Now build the stack trace and source code strings.
     for i, frame_info in enumerate(frames):
         file_name = frame_info[0]
         func_name = frame_info[1]
         line_num = frame_info[3]
         arg_list = []
```

### Comparing `ChatDBG-0.0.8/src/chatdbg/chatdbg_ipdb.py` & `ChatDBG-0.0.9/src/chatdbg/chatdbg_ipdb.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/chatdbg_why.py` & `ChatDBG-0.0.9/src/chatdbg/chatdbg_why.py`

 * *Files identical despite different names*

### Comparing `ChatDBG-0.0.8/src/chatdbg/pdb.py` & `ChatDBG-0.0.9/src/chatdbg/pdb.py`

 * *Files 1% similar despite different names*

```diff
@@ -211,15 +211,15 @@
     def __init__(self, completekey='tab', stdin=None, stdout=None, skip=None,
                  nosigint=False, readrc=True):
         bdb.Bdb.__init__(self, skip=skip)
         cmd.Cmd.__init__(self, completekey, stdin, stdout)
         sys.audit("pdb.Pdb")
         if stdout:
             self.use_rawinput = 0
-        self.prompt = '(Pdb) '
+        self.prompt = '(ChatDBG Pdb) '
         self.aliases = {}
         self.displaying = {}
         self.mainpyfile = ''
         self._wait_for_mainpyfile = False
         self.tb_lineno = {}
         # Try to load readline if it exists
         try:
```

### Comparing `ChatDBG-0.0.8/src/chatdbg/prompter.py` & `ChatDBG-0.0.9/src/chatdbg/prompter.py`

 * *Files identical despite different names*

