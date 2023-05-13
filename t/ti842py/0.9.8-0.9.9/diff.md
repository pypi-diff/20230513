# Comparing `tmp/ti842py-0.9.8.tar.gz` & `tmp/ti842py-0.9.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ti842py-0.9.8.tar", last modified: Fri Sep 10 14:46:11 2021, max compression
+gzip compressed data, was "ti842py-0.9.9.tar", last modified: Sat Jan  1 02:36:36 2022, max compression
```

## Comparing `ti842py-0.9.8.tar` & `ti842py-0.9.9.tar`

### file list

```diff
@@ -1,33 +1,47 @@
-drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2021-09-10 14:46:11.454807 ti842py-0.9.8/
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)    35108 2021-08-17 11:26:30.000000 ti842py-0.9.8/LICENSE
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       48 2021-09-10 14:15:33.000000 ti842py-0.9.8/MANIFEST.in
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8531 2021-09-10 14:46:11.454807 ti842py-0.9.8/PKG-INFO
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     7817 2021-09-10 14:03:09.000000 ti842py-0.9.8/README.md
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       78 2021-09-10 14:03:09.000000 ti842py-0.9.8/requirements.txt
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       79 2021-09-10 14:46:11.454807 ti842py-0.9.8/setup.cfg
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1246 2021-09-10 14:45:40.000000 ti842py-0.9.8/setup.py
-drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2021-09-10 14:46:11.451475 ti842py-0.9.8/ti842py/
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      166 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/__init__.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      287 2021-09-10 14:45:58.000000 ti842py-0.9.8/ti842py/__version__.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     4628 2021-09-09 18:52:37.000000 ti842py-0.9.8/ti842py/main.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     6236 2021-09-09 20:35:45.000000 ti842py-0.9.8/ti842py/parsing_utils.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)    21770 2021-09-10 14:03:09.000000 ti842py-0.9.8/ti842py/tiParser.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)    14238 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/token_utils.py
-drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2021-09-10 14:46:11.454807 ti842py-0.9.8/ti842py/utils/
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      146 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/clear.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     6138 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/draw.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     2173 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/fix_floating_point.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      437 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/getDateTime.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1545 2021-09-03 18:34:30.000000 ti842py-0.9.8/ti842py/utils/getKey.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)    10889 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/goto.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8556 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/matrix.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       82 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/output.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1217 2021-09-10 14:03:09.000000 ti842py-0.9.8/ti842py/utils/prgm.py
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      138 2021-08-17 11:26:30.000000 ti842py-0.9.8/ti842py/utils/toNumber.py
-drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2021-09-10 14:46:11.451475 ti842py-0.9.8/ti842py.egg-info/
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8531 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/PKG-INFO
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)      632 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/SOURCES.txt
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)        1 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/dependency_links.txt
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       47 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/entry_points.txt
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)       79 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/requires.txt
--rw-r--r--   0 tabulate  (1000) tabulate  (1000)        8 2021-09-10 14:46:11.000000 ti842py-0.9.8/ti842py.egg-info/top_level.txt
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.192587 ti842py-0.9.9/
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.189253 ti842py-0.9.9/.github/
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.189253 ti842py-0.9.9/.github/workflows/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     2360 2021-03-12 02:53:04.000000 ti842py-0.9.9/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1004 2021-03-12 02:53:04.000000 ti842py-0.9.9/.github/workflows/main.yml
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1825 2021-08-16 22:10:28.000000 ti842py-0.9.9/.gitignore
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    35108 2021-03-12 02:53:04.000000 ti842py-0.9.9/LICENSE
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       23 2021-03-12 02:53:04.000000 ti842py-0.9.9/MANIFEST.in
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8455 2022-01-01 02:36:36.192587 ti842py-0.9.9/PKG-INFO
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     7823 2022-01-01 02:33:41.000000 ti842py-0.9.9/README.md
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    27003 2021-09-13 23:26:56.000000 ti842py-0.9.9/clc.py
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.189253 ti842py-0.9.9/imgs/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    20078 2021-07-12 21:29:33.000000 ti842py-0.9.9/imgs/ti842py-logo.svg
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      655 2021-03-12 02:53:04.000000 ti842py-0.9.9/power.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      703 2021-05-20 18:19:56.000000 ti842py-0.9.9/program.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       78 2021-09-08 21:18:17.000000 ti842py-0.9.9/requirements.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       79 2022-01-01 02:36:36.192587 ti842py-0.9.9/setup.cfg
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1137 2021-09-08 21:13:19.000000 ti842py-0.9.9/setup.py
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.189253 ti842py-0.9.9/tests/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      881 2021-08-16 22:10:04.000000 ti842py-0.9.9/tests/test.py
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.192587 ti842py-0.9.9/ti842py/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      166 2021-03-12 02:53:04.000000 ti842py-0.9.9/ti842py/__init__.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      287 2022-01-01 02:36:25.000000 ti842py-0.9.9/ti842py/__version__.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     5087 2021-09-13 22:26:29.000000 ti842py-0.9.9/ti842py/main.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     6236 2021-09-08 21:13:13.000000 ti842py-0.9.9/ti842py/parsing_utils.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    22008 2022-01-01 02:29:11.000000 ti842py-0.9.9/ti842py/tiParser.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    14238 2021-08-05 15:50:45.000000 ti842py-0.9.9/ti842py/token_utils.py
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.192587 ti842py-0.9.9/ti842py/utils/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      146 2021-05-15 22:32:01.000000 ti842py-0.9.9/ti842py/utils/clear.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     6138 2021-09-08 21:38:13.000000 ti842py-0.9.9/ti842py/utils/draw.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     2173 2021-07-02 01:44:02.000000 ti842py-0.9.9/ti842py/utils/fix_floating_point.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      437 2021-07-14 18:59:00.000000 ti842py-0.9.9/ti842py/utils/getDateTime.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1552 2022-01-01 02:33:41.000000 ti842py-0.9.9/ti842py/utils/getKey.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)    10889 2021-05-14 22:26:22.000000 ti842py-0.9.9/ti842py/utils/goto.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8785 2022-01-01 02:31:30.000000 ti842py-0.9.9/ti842py/utils/matrix.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       82 2021-07-15 18:21:01.000000 ti842py-0.9.9/ti842py/utils/output.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     2207 2021-09-13 23:18:30.000000 ti842py-0.9.9/ti842py/utils/persistant_data.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     1217 2021-09-11 21:55:41.000000 ti842py-0.9.9/ti842py/utils/prgm.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      150 2022-01-01 02:25:12.000000 ti842py-0.9.9/ti842py/utils/round.py
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      138 2021-05-15 22:34:08.000000 ti842py-0.9.9/ti842py/utils/toNumber.py
+drwxr-xr-x   0 tabulate  (1000) tabulate  (1000)        0 2022-01-01 02:36:36.192587 ti842py-0.9.9/ti842py.egg-info/
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)     8455 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/PKG-INFO
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)      829 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/SOURCES.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)        1 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/dependency_links.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       47 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/entry_points.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)       79 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/requires.txt
+-rw-r--r--   0 tabulate  (1000) tabulate  (1000)        8 2022-01-01 02:36:36.000000 ti842py-0.9.9/ti842py.egg-info/top_level.txt
```

### Comparing `ti842py-0.9.8/LICENSE` & `ti842py-0.9.9/LICENSE`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/PKG-INFO` & `ti842py-0.9.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,21 +1,19 @@
 Metadata-Version: 2.1
 Name: ti842py
-Version: 0.9.8
+Version: 0.9.9
 Summary: TI-BASIC to Python 3 Transpiler
 Home-page: https://github.com/TabulateJarl8/ti842py
 Author: Tabulate
 Author-email: tabulatejarl8@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
-Classifier: Operating System :: POSIX :: Linux
-Classifier: Environment :: Console
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Intended Audience :: Developers
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -62,17 +60,17 @@
  - `toString()`
  - `randInt()`/`rand`
  - Most drawing functions
  - List subscripting
  - Matrices
  - `Ans`
  - `prgm`
+ - `round()`
 
 ### Planned Features
- - `round()`
  - `Return`
  - `eval()`/`expr()`
 
 ### Known issues
 
 Issues can be found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/TabulateJarl8/ti842py/issues)
 
@@ -139,15 +137,15 @@
 Again, if the second argument is not supplied, the program will be written to `stdout`. The `transpile` command can be supplied with optional arguments. `decompileFile`, `multiplication`, and `floating_point` default to `True`, and `forceDecompile`, `run`, and `turbo_draw` default to `False`
 
 The last way that ti842py can be ran is by running the main python file. After cloning the repository, cd into the repository and run `python ti842py/main.py inputfile.txt`. You can supply any arguments that you would supply with the `ti842py` command.
 
 # Special functions
 ----
 
- - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the `X,T,θ,n` key is F10.
+ - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,θ,n` key is F9, and `clear` is backspace.
 
  - `If` - `If` blocks with `Then` after the `If` must be ended with `End`, they cannot be left open. `If` blocks on 2 lines without a `Then` cannot be closed with `End`
 
  - `prgm` - `prgm` will search the current directory for a file matching the provided name (case insensitive; extension of `.8xp`). If found, the file will be passed to the command `ti842py {filename} --run`, where `{filename}` is the name of the file. If a path is given that contains `.` or `~`, or if the path is not all uppercase, the transpiler will assume that the path has been manually provided by the user (this will be useful once I implement a TI-BASIC shell).
 
 # Libraries used
```

#### html2text {}

```diff
@@ -1,17 +1,16 @@
-Metadata-Version: 2.1 Name: ti842py Version: 0.9.8 Summary: TI-BASIC to Python
+Metadata-Version: 2.1 Name: ti842py Version: 0.9.9 Summary: TI-BASIC to Python
 3 Transpiler Home-page: https://github.com/TabulateJarl8/ti842py Author:
 Tabulate Author-email: tabulatejarl8@gmail.com License: UNKNOWN Platform:
 UNKNOWN Classifier: Programming Language :: Python :: 3 Classifier: License ::
 OSI Approved :: GNU General Public License v3 (GPLv3) Classifier: Operating
-System :: OS Independent Classifier: Operating System :: POSIX :: Linux
-Classifier: Environment :: Console Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: End Users/Desktop Classifier: Intended
-Audience :: Developers Requires-Python: >=3.6 Description-Content-Type: text/
-markdown License-File: LICENSE
+System :: OS Independent Classifier: Development Status :: 4 - Beta Classifier:
+Intended Audience :: End Users/Desktop Classifier: Intended Audience ::
+Developers Requires-Python: >=3.6 Description-Content-Type: text/markdown
+License-File: LICENSE
                                 [ti842py Logo]
     [PyPI] [Downloads] [PyPI_license] [Maintenance] [GitHub_Issues] [GitHub
                         followers] [GitHub_Repo_stars]
 ---- ti842py is a TI-BASIC to Python 3 transpiler. A transpiler is a piece of
 software that can convert code from one language to another. This program
 should be able to convert a lot of programs, but if you find something that it
 can't convert yet, start an issue. This transpiler also has the ability to
@@ -21,17 +20,17 @@
 beta and may produce inaccurate results. # Features ---- - Converts string
 literals to comments - Attempts to interpret implicit multiplication - Attempts
 to fix floating point arithmetic errors - `Disp`/`Output()` - Variable
 assignment - `If/Then/Else` statements, including `Else If` - `ClrHome` -
 `Input`/`Prompt` - For, While, and Repeat loops - `Pause` - `Wait` - `Stop` -
 `DelVar` - `getKey` - `Goto`/`Lbl` - `getDate`, `getTime`, and `dayOfWk` - `IS>
 (`/`DS<(` - `Menu()` - `toString()` - `randInt()`/`rand` - Most drawing
-functions - List subscripting - Matrices - `Ans` - `prgm` ### Planned Features
-- `round()` - `Return` - `eval()`/`expr()` ### Known issues Issues can be found
-at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
+functions - List subscripting - Matrices - `Ans` - `prgm` - `round()` ###
+Planned Features - `Return` - `eval()`/`expr()` ### Known issues Issues can be
+found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
 TabulateJarl8/ti842py/issues) # Installation ---- ti842py can be installed via
 PyPI or by cloning the repository. To install it with PyPI, just run `pip3
 install ti842py` in a terminal. To install it locally, you can clone the
 repository and run `python setup.py install --user`. # Usage ---- Feel free to
 use the programs found at [https://github.com/TabulateJarl8/tiprograms](https:/
 /github.com/TabulateJarl8/tiprograms) to test this project out. ## CLI Usage
 ti842py can be used in 3 different ways. The first way is just running it from
@@ -72,26 +71,26 @@
 ti842py/main.py inputfile.txt`. You can supply any arguments that you would
 supply with the `ti842py` command. # Special functions ---- - `getKey` - The
 `getKey` function works just like it does in normal TI-BASIC, except with some
 special rules. Any key on the keyboard pressed will be converted to the
 corresponding key on the calculator. This works for letters, numbers, arrow
 keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top
 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha`
-is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the
-`X,T,Î¸,n` key is F10. - `If` - `If` blocks with `Then` after the `If` must be
-ended with `End`, they cannot be left open. `If` blocks on 2 lines without a
-`Then` cannot be closed with `End` - `prgm` - `prgm` will search the current
-directory for a file matching the provided name (case insensitive; extension of
-`.8xp`). If found, the file will be passed to the command `ti842py {filename} -
--run`, where `{filename}` is the name of the file. If a path is given that
-contains `.` or `~`, or if the path is not all uppercase, the transpiler will
-assume that the path has been manually provided by the user (this will be
-useful once I implement a TI-BASIC shell). # Libraries used ---- - [My fork of
-basically-ti-basic](https://github.com/TabulateJarl8/basically-ti-basic) - for
-decompiling `.8Xp` files - [graphics.py](https://anh.cs.luc.edu/
-handsonPythonTutorial/graphics.html) - for drawing features -
+is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,Î¸,n` key is
+F9, and `clear` is backspace. - `If` - `If` blocks with `Then` after the `If`
+must be ended with `End`, they cannot be left open. `If` blocks on 2 lines
+without a `Then` cannot be closed with `End` - `prgm` - `prgm` will search the
+current directory for a file matching the provided name (case insensitive;
+extension of `.8xp`). If found, the file will be passed to the command `ti842py
+{filename} --run`, where `{filename}` is the name of the file. If a path is
+given that contains `.` or `~`, or if the path is not all uppercase, the
+transpiler will assume that the path has been manually provided by the user
+(this will be useful once I implement a TI-BASIC shell). # Libraries used ---
+- - [My fork of basically-ti-basic](https://github.com/TabulateJarl8/basically-
+ti-basic) - for decompiling `.8Xp` files - [graphics.py](https://
+anh.cs.luc.edu/handsonPythonTutorial/graphics.html) - for drawing features -
 [insignification's fork of the goto module](https://github.com/insignification/
 python-goto/tree/fix2) - for `goto`/`lbl` support - [pynput](https://
 github.com/moses-palmer/pynput) - for non-blocking input support -
 [pythondialog](http://pythondialog.sourceforge.net/doc/) - Python wrapper
 around `dialog` for `Menu` support - [token_utils](https://github.com/aroberge/
 token-utils) - Support for fixing implicit multiplication
```

### Comparing `ti842py-0.9.8/README.md` & `ti842py-0.9.9/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -41,17 +41,17 @@
  - `toString()`
  - `randInt()`/`rand`
  - Most drawing functions
  - List subscripting
  - Matrices
  - `Ans`
  - `prgm`
+ - `round()`
 
 ### Planned Features
- - `round()`
  - `Return`
  - `eval()`/`expr()`
 
 ### Known issues
 
 Issues can be found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/TabulateJarl8/ti842py/issues)
 
@@ -118,15 +118,15 @@
 Again, if the second argument is not supplied, the program will be written to `stdout`. The `transpile` command can be supplied with optional arguments. `decompileFile`, `multiplication`, and `floating_point` default to `True`, and `forceDecompile`, `run`, and `turbo_draw` default to `False`
 
 The last way that ti842py can be ran is by running the main python file. After cloning the repository, cd into the repository and run `python ti842py/main.py inputfile.txt`. You can supply any arguments that you would supply with the `ti842py` command.
 
 # Special functions
 ----
 
- - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the `X,T,θ,n` key is F10.
+ - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,θ,n` key is F9, and `clear` is backspace.
 
  - `If` - `If` blocks with `Then` after the `If` must be ended with `End`, they cannot be left open. `If` blocks on 2 lines without a `Then` cannot be closed with `End`
 
  - `prgm` - `prgm` will search the current directory for a file matching the provided name (case insensitive; extension of `.8xp`). If found, the file will be passed to the command `ti842py {filename} --run`, where `{filename}` is the name of the file. If a path is given that contains `.` or `~`, or if the path is not all uppercase, the transpiler will assume that the path has been manually provided by the user (this will be useful once I implement a TI-BASIC shell).
 
 # Libraries used
```

#### html2text {}

```diff
@@ -11,17 +11,17 @@
 beta and may produce inaccurate results. # Features ---- - Converts string
 literals to comments - Attempts to interpret implicit multiplication - Attempts
 to fix floating point arithmetic errors - `Disp`/`Output()` - Variable
 assignment - `If/Then/Else` statements, including `Else If` - `ClrHome` -
 `Input`/`Prompt` - For, While, and Repeat loops - `Pause` - `Wait` - `Stop` -
 `DelVar` - `getKey` - `Goto`/`Lbl` - `getDate`, `getTime`, and `dayOfWk` - `IS>
 (`/`DS<(` - `Menu()` - `toString()` - `randInt()`/`rand` - Most drawing
-functions - List subscripting - Matrices - `Ans` - `prgm` ### Planned Features
-- `round()` - `Return` - `eval()`/`expr()` ### Known issues Issues can be found
-at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
+functions - List subscripting - Matrices - `Ans` - `prgm` - `round()` ###
+Planned Features - `Return` - `eval()`/`expr()` ### Known issues Issues can be
+found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
 TabulateJarl8/ti842py/issues) # Installation ---- ti842py can be installed via
 PyPI or by cloning the repository. To install it with PyPI, just run `pip3
 install ti842py` in a terminal. To install it locally, you can clone the
 repository and run `python setup.py install --user`. # Usage ---- Feel free to
 use the programs found at [https://github.com/TabulateJarl8/tiprograms](https:/
 /github.com/TabulateJarl8/tiprograms) to test this project out. ## CLI Usage
 ti842py can be used in 3 different ways. The first way is just running it from
@@ -62,26 +62,26 @@
 ti842py/main.py inputfile.txt`. You can supply any arguments that you would
 supply with the `ti842py` command. # Special functions ---- - `getKey` - The
 `getKey` function works just like it does in normal TI-BASIC, except with some
 special rules. Any key on the keyboard pressed will be converted to the
 corresponding key on the calculator. This works for letters, numbers, arrow
 keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top
 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha`
-is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the
-`X,T,Î¸,n` key is F10. - `If` - `If` blocks with `Then` after the `If` must be
-ended with `End`, they cannot be left open. `If` blocks on 2 lines without a
-`Then` cannot be closed with `End` - `prgm` - `prgm` will search the current
-directory for a file matching the provided name (case insensitive; extension of
-`.8xp`). If found, the file will be passed to the command `ti842py {filename} -
--run`, where `{filename}` is the name of the file. If a path is given that
-contains `.` or `~`, or if the path is not all uppercase, the transpiler will
-assume that the path has been manually provided by the user (this will be
-useful once I implement a TI-BASIC shell). # Libraries used ---- - [My fork of
-basically-ti-basic](https://github.com/TabulateJarl8/basically-ti-basic) - for
-decompiling `.8Xp` files - [graphics.py](https://anh.cs.luc.edu/
-handsonPythonTutorial/graphics.html) - for drawing features -
+is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,Î¸,n` key is
+F9, and `clear` is backspace. - `If` - `If` blocks with `Then` after the `If`
+must be ended with `End`, they cannot be left open. `If` blocks on 2 lines
+without a `Then` cannot be closed with `End` - `prgm` - `prgm` will search the
+current directory for a file matching the provided name (case insensitive;
+extension of `.8xp`). If found, the file will be passed to the command `ti842py
+{filename} --run`, where `{filename}` is the name of the file. If a path is
+given that contains `.` or `~`, or if the path is not all uppercase, the
+transpiler will assume that the path has been manually provided by the user
+(this will be useful once I implement a TI-BASIC shell). # Libraries used ---
+- - [My fork of basically-ti-basic](https://github.com/TabulateJarl8/basically-
+ti-basic) - for decompiling `.8Xp` files - [graphics.py](https://
+anh.cs.luc.edu/handsonPythonTutorial/graphics.html) - for drawing features -
 [insignification's fork of the goto module](https://github.com/insignification/
 python-goto/tree/fix2) - for `goto`/`lbl` support - [pynput](https://
 github.com/moses-palmer/pynput) - for non-blocking input support -
 [pythondialog](http://pythondialog.sourceforge.net/doc/) - Python wrapper
 around `dialog` for `Menu` support - [token_utils](https://github.com/aroberge/
 token-utils) - Support for fixing implicit multiplication
```

### Comparing `ti842py-0.9.8/setup.py` & `ti842py-0.9.9/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 import setuptools
 import os
 
-here = os.path.abspath(os.path.dirname(__file__))
-
-with open(os.path.join(here, "README.md"), "r") as fh:
+with open("README.md", "r") as fh:
 	long_description = fh.read()
 
-with open(os.path.join(here, 'requirements.txt')) as fh:
+with open('requirements.txt') as fh:
 	install_requires = [line.rstrip() for line in fh.readlines()]
 
+here = os.path.abspath(os.path.dirname(__file__))
 about = {}
 with open(os.path.join(here, "ti842py", "__version__.py"), "r") as f:
 	exec(f.read(), about)
 
 setuptools.setup(
 	name=about["__title__"],
 	version=about["__version__"],
@@ -29,16 +28,14 @@
 		]
 	},
 	packages=setuptools.find_packages(),
 	classifiers=[
 		"Programming Language :: Python :: 3",
 		"License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
 		"Operating System :: OS Independent",
-		"Operating System :: POSIX :: Linux",
-		"Environment :: Console",
 		"Development Status :: 4 - Beta",
 		"Intended Audience :: End Users/Desktop",
 		"Intended Audience :: Developers"
 	],
 	python_requires='>=3.6',
 	include_package_data=True
 )
```

### Comparing `ti842py-0.9.8/ti842py/main.py` & `ti842py-0.9.9/ti842py/main.py`

 * *Files 8% similar despite different names*

```diff
@@ -145,36 +145,54 @@
 	parser.add_argument(
 		'--turbo-draw',
 		action='store_true',
 		help='Remove the 0.1 second delay between drawing actions'
 	)
 
 	parser.add_argument(
+		'--reset-persistant-data',
+		action='store_true',
+		help='Reset the ti842py persistant data (variables, matrices, etc)',
+		dest='reset_data'
+	)
+
+	parser.add_argument(
 		'-r',
 		'--run',
 		action="store_true",
 		help="Runs the program after it\'s done transpiling. Will not print to stdout",
 		dest='run'
 	)
 
 	parser.add_argument(
 		'-V',
 		'--version',
 		action='version',
-		version='ti842py {version}'.format(version=__version__)
+		version=f'ti842py {__version__}'
 	)
 
 	args = parser.parse_args()
 
+	if args.reset_data:
+		user_confirm = ''
+		while user_confirm not in {'y', 'n'}:
+			user_confirm = input('Are you sure you would like to remove the persistant data? [y/n] ').lower()
+		if user_confirm == 'y':
+			os.remove(os.path.expanduser('~/.ti842py-persistant'))
+			print('Removed persistant data')
+		else:
+			print('Cancelled removal of persistant data')
+
 	if hasattr(args.infile, '__getitem__'):
 		infile = args.infile[0]
 	else:
 		infile = args.infile
 
 	if infile is None:
-		raise argparse.ArgumentError(infile_argument, 'the infile argument is required')
+		parser.print_help()
+		sys.exit(1)
 
 	transpile(infile, args.outfile, args.n, args.d, args.multiplication, args.floating_point, args.turbo_draw, args.run)
 
 
 if __name__ == "__main__":
 	main()
```

### Comparing `ti842py-0.9.8/ti842py/parsing_utils.py` & `ti842py-0.9.9/ti842py/parsing_utils.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py/tiParser.py` & `ti842py-0.9.9/ti842py/tiParser.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,14 +38,16 @@
 
 		if self.floating_point:
 			self.UTILS['fix_floating_point']['enabled'] = True
 
 		if self.turbo_draw:
 			self.UTILS['draw']['code'] = [line for line in self.UTILS['draw']['code'] if '@_slow' not in line]
 
+		self.UTILS['persistant_data']['enabled'] = True
+
 		self.drawLock = False
 
 	def convertLine(self, index, line):
 		# TODO: possible curses interface instead of just printing and outputting
 
 		statement = ""
 
@@ -324,19 +326,20 @@
 			# Things that can be alone on a line
 			if line.startswith("getKey") or \
 				line.startswith("abs") or \
 				line.startswith("sqrt") or \
 				line.startswith("toString(") or \
 				line.startswith('randInt(') or \
 				line.startswith('rand') or \
+				line.startswith('round(') or \
 				re.search(r'^\[[A-J]\]', line):
 				statement = line
 			else:
-				statement = "# UNKNOWN INDENTIFIER: {}".format(line)
-				logger.warning("Unknown indentifier on line %s", index + 1)
+				statement = f"# UNKNOWN INDENTIFIER: {line}"
+				logger.warning(f"Unknown indentifier on line {index + 1}")
 
 		if isinstance(statement, str):
 			statement = [statement]
 
 		statement = parsing_utils.noStringReplace(r'{', '[', statement)
 		statement = parsing_utils.noStringReplace(r'}', ']', statement)
 		statement = parsing_utils.noStringReplace('≠', '!=', statement)
@@ -380,14 +383,18 @@
 			self.UTILS['getDateTime']['enabled'] = True
 		if 'remainder(' in ' '.join(statement):
 			statement = parsing_utils.noStringReplace(r'remainder\(([^\)]+)\)', lambda m: m.group(1).replace(' ', '').split(',')[0] + ' % ' + m.group(1).replace(' ', '').split(',')[1], statement)
 
 		if 'dim(' in ' '.join(statement):
 			statement = parsing_utils.noStringReplace(r'dim\(', 'len(', statement)
 
+		if 'round(' in ' '.join(statement):
+			statement = parsing_utils.noStringReplace(r'round\(', 'ti_round(', statement)
+			self.UTILS['round']['enabled'] = True
+
 		if re.search(r'l[1-6]\([0-9A-Za-z]+\)', ' '.join(statement)):
 			# List subscription
 			try:
 				statement = parsing_utils.noStringReplace(r'(l[1-6])\(([0-9A-Z]+)\)', lambda m: m.group(1) + '[' + str(int(m.group(2)) - 1) + ']', statement)
 			except ValueError:
 				statement = parsing_utils.noStringReplace(r'(l[1-6])\(([0-9A-Z]+)\)', lambda m: m.group(1) + '[' + m.group(2) + ']', statement)
```

### Comparing `ti842py-0.9.8/ti842py/token_utils.py` & `ti842py-0.9.9/ti842py/token_utils.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py/utils/draw.py` & `ti842py-0.9.9/ti842py/utils/draw.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py/utils/fix_floating_point.py` & `ti842py-0.9.9/ti842py/utils/fix_floating_point.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py/utils/getKey.py` & `ti842py-0.9.9/ti842py/utils/getKey.py`

 * *Files 4% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 			pynput.keyboard.Key.f10: 32,
 			pynput.keyboard.Key.f7: 33,
 			pynput.keyboard.Key.down: 34,
 			"a": 41,
 			"b": 42,
 			"c": 43,
 			pynput.keyboard.Key.f8: 44,
-			pynput.keyboard.Key.f9: 45,
+			pynput.keyboard.Key.backspace: 45,
 			"d": 51,
 			"e": 52,
 			"f": 53,
 			"g": 54,
 			"h": 55,
 			"^": 55,
 			"i": 61,
```

### Comparing `ti842py-0.9.8/ti842py/utils/goto.py` & `ti842py-0.9.9/ti842py/utils/goto.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py/utils/matrix.py` & `ti842py-0.9.9/ti842py/utils/matrix.py`

 * *Files 0% similar despite different names*

```diff
@@ -285,21 +285,28 @@
 	def __neg__(self):
 		new_matrix = copy.deepcopy(self.matrix)
 		for i in range(len(new_matrix)):
 			for j in range(len(new_matrix[i])):
 				new_matrix[i][j] = -new_matrix[i][j]
 		return Matrix(new_matrix)
 
+	def __round__(self, digits):
+		new_matrix = copy.deepcopy(self.matrix)
+		for i in range(len(new_matrix)):
+			for j in range(len(new_matrix[i])):
+				new_matrix[i][j] = round(new_matrix[i][j], digits)
+		return Matrix(new_matrix)
+
 	def __eq__(self, other):
 		return 1 if self.matrix == other.matrix else 0
 
 	def __ne__(self, other):
 		return not self.__eq__(other)
 
-	def __repr__(self):
+	def __str__(self):
 		return '\n'.join(['[' + ' '.join([str(num) for num in sublist]) + ']' for sublist in self.matrix])
 
 	def __getitem__(self, index):
 		# We do not need __setitem__ because the user should not be messing
 		# with the parent lists directly. __getitem__ is enough to interface
 		# with the child lists contained within self.matrix
 		return self.matrix[index] # indexes start at 1 in TI-BASIC
```

### Comparing `ti842py-0.9.8/ti842py/utils/prgm.py` & `ti842py-0.9.9/ti842py/utils/prgm.py`

 * *Files identical despite different names*

### Comparing `ti842py-0.9.8/ti842py.egg-info/PKG-INFO` & `ti842py-0.9.9/ti842py.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,21 +1,19 @@
 Metadata-Version: 2.1
 Name: ti842py
-Version: 0.9.8
+Version: 0.9.9
 Summary: TI-BASIC to Python 3 Transpiler
 Home-page: https://github.com/TabulateJarl8/ti842py
 Author: Tabulate
 Author-email: tabulatejarl8@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
-Classifier: Operating System :: POSIX :: Linux
-Classifier: Environment :: Console
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Intended Audience :: Developers
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -62,17 +60,17 @@
  - `toString()`
  - `randInt()`/`rand`
  - Most drawing functions
  - List subscripting
  - Matrices
  - `Ans`
  - `prgm`
+ - `round()`
 
 ### Planned Features
- - `round()`
  - `Return`
  - `eval()`/`expr()`
 
 ### Known issues
 
 Issues can be found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/TabulateJarl8/ti842py/issues)
 
@@ -139,15 +137,15 @@
 Again, if the second argument is not supplied, the program will be written to `stdout`. The `transpile` command can be supplied with optional arguments. `decompileFile`, `multiplication`, and `floating_point` default to `True`, and `forceDecompile`, `run`, and `turbo_draw` default to `False`
 
 The last way that ti842py can be ran is by running the main python file. After cloning the repository, cd into the repository and run `python ti842py/main.py inputfile.txt`. You can supply any arguments that you would supply with the `ti842py` command.
 
 # Special functions
 ----
 
- - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the `X,T,θ,n` key is F10.
+ - `getKey` - The `getKey` function works just like it does in normal TI-BASIC, except with some special rules. Any key on the keyboard pressed will be converted to the corresponding key on the calculator. This works for letters, numbers, arrow keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha` is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,θ,n` key is F9, and `clear` is backspace.
 
  - `If` - `If` blocks with `Then` after the `If` must be ended with `End`, they cannot be left open. `If` blocks on 2 lines without a `Then` cannot be closed with `End`
 
  - `prgm` - `prgm` will search the current directory for a file matching the provided name (case insensitive; extension of `.8xp`). If found, the file will be passed to the command `ti842py {filename} --run`, where `{filename}` is the name of the file. If a path is given that contains `.` or `~`, or if the path is not all uppercase, the transpiler will assume that the path has been manually provided by the user (this will be useful once I implement a TI-BASIC shell).
 
 # Libraries used
```

#### html2text {}

```diff
@@ -1,17 +1,16 @@
-Metadata-Version: 2.1 Name: ti842py Version: 0.9.8 Summary: TI-BASIC to Python
+Metadata-Version: 2.1 Name: ti842py Version: 0.9.9 Summary: TI-BASIC to Python
 3 Transpiler Home-page: https://github.com/TabulateJarl8/ti842py Author:
 Tabulate Author-email: tabulatejarl8@gmail.com License: UNKNOWN Platform:
 UNKNOWN Classifier: Programming Language :: Python :: 3 Classifier: License ::
 OSI Approved :: GNU General Public License v3 (GPLv3) Classifier: Operating
-System :: OS Independent Classifier: Operating System :: POSIX :: Linux
-Classifier: Environment :: Console Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: End Users/Desktop Classifier: Intended
-Audience :: Developers Requires-Python: >=3.6 Description-Content-Type: text/
-markdown License-File: LICENSE
+System :: OS Independent Classifier: Development Status :: 4 - Beta Classifier:
+Intended Audience :: End Users/Desktop Classifier: Intended Audience ::
+Developers Requires-Python: >=3.6 Description-Content-Type: text/markdown
+License-File: LICENSE
                                 [ti842py Logo]
     [PyPI] [Downloads] [PyPI_license] [Maintenance] [GitHub_Issues] [GitHub
                         followers] [GitHub_Repo_stars]
 ---- ti842py is a TI-BASIC to Python 3 transpiler. A transpiler is a piece of
 software that can convert code from one language to another. This program
 should be able to convert a lot of programs, but if you find something that it
 can't convert yet, start an issue. This transpiler also has the ability to
@@ -21,17 +20,17 @@
 beta and may produce inaccurate results. # Features ---- - Converts string
 literals to comments - Attempts to interpret implicit multiplication - Attempts
 to fix floating point arithmetic errors - `Disp`/`Output()` - Variable
 assignment - `If/Then/Else` statements, including `Else If` - `ClrHome` -
 `Input`/`Prompt` - For, While, and Repeat loops - `Pause` - `Wait` - `Stop` -
 `DelVar` - `getKey` - `Goto`/`Lbl` - `getDate`, `getTime`, and `dayOfWk` - `IS>
 (`/`DS<(` - `Menu()` - `toString()` - `randInt()`/`rand` - Most drawing
-functions - List subscripting - Matrices - `Ans` - `prgm` ### Planned Features
-- `round()` - `Return` - `eval()`/`expr()` ### Known issues Issues can be found
-at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
+functions - List subscripting - Matrices - `Ans` - `prgm` - `round()` ###
+Planned Features - `Return` - `eval()`/`expr()` ### Known issues Issues can be
+found at [https://github.com/TabulateJarl8/ti842py/issues](https://github.com/
 TabulateJarl8/ti842py/issues) # Installation ---- ti842py can be installed via
 PyPI or by cloning the repository. To install it with PyPI, just run `pip3
 install ti842py` in a terminal. To install it locally, you can clone the
 repository and run `python setup.py install --user`. # Usage ---- Feel free to
 use the programs found at [https://github.com/TabulateJarl8/tiprograms](https:/
 /github.com/TabulateJarl8/tiprograms) to test this project out. ## CLI Usage
 ti842py can be used in 3 different ways. The first way is just running it from
@@ -72,26 +71,26 @@
 ti842py/main.py inputfile.txt`. You can supply any arguments that you would
 supply with the `ti842py` command. # Special functions ---- - `getKey` - The
 `getKey` function works just like it does in normal TI-BASIC, except with some
 special rules. Any key on the keyboard pressed will be converted to the
 corresponding key on the calculator. This works for letters, numbers, arrow
 keys, enter, delete, and symbols. As for the buttons not on a keyboard, the top
 5 keys are the F1-F5 keys on the keyboard, `2nd` is grave `` ` ``, and `alpha`
-is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, `clear` is F9, and the
-`X,T,Î¸,n` key is F10. - `If` - `If` blocks with `Then` after the `If` must be
-ended with `End`, they cannot be left open. `If` blocks on 2 lines without a
-`Then` cannot be closed with `End` - `prgm` - `prgm` will search the current
-directory for a file matching the provided name (case insensitive; extension of
-`.8xp`). If found, the file will be passed to the command `ti842py {filename} -
--run`, where `{filename}` is the name of the file. If a path is given that
-contains `.` or `~`, or if the path is not all uppercase, the transpiler will
-assume that the path has been manually provided by the user (this will be
-useful once I implement a TI-BASIC shell). # Libraries used ---- - [My fork of
-basically-ti-basic](https://github.com/TabulateJarl8/basically-ti-basic) - for
-decompiling `.8Xp` files - [graphics.py](https://anh.cs.luc.edu/
-handsonPythonTutorial/graphics.html) - for drawing features -
+is tilda `~`. `mode` is F6, `stat` is f7, `vars` is F8, the `X,T,Î¸,n` key is
+F9, and `clear` is backspace. - `If` - `If` blocks with `Then` after the `If`
+must be ended with `End`, they cannot be left open. `If` blocks on 2 lines
+without a `Then` cannot be closed with `End` - `prgm` - `prgm` will search the
+current directory for a file matching the provided name (case insensitive;
+extension of `.8xp`). If found, the file will be passed to the command `ti842py
+{filename} --run`, where `{filename}` is the name of the file. If a path is
+given that contains `.` or `~`, or if the path is not all uppercase, the
+transpiler will assume that the path has been manually provided by the user
+(this will be useful once I implement a TI-BASIC shell). # Libraries used ---
+- - [My fork of basically-ti-basic](https://github.com/TabulateJarl8/basically-
+ti-basic) - for decompiling `.8Xp` files - [graphics.py](https://
+anh.cs.luc.edu/handsonPythonTutorial/graphics.html) - for drawing features -
 [insignification's fork of the goto module](https://github.com/insignification/
 python-goto/tree/fix2) - for `goto`/`lbl` support - [pynput](https://
 github.com/moses-palmer/pynput) - for non-blocking input support -
 [pythondialog](http://pythondialog.sourceforge.net/doc/) - Python wrapper
 around `dialog` for `Menu` support - [token_utils](https://github.com/aroberge/
 token-utils) - Support for fixing implicit multiplication
```

