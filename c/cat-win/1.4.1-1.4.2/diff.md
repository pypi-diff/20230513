# Comparing `tmp/cat_win-1.4.1.tar.gz` & `tmp/cat_win-1.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cat_win-1.4.1.tar", last modified: Thu May  4 09:55:21 2023, max compression
+gzip compressed data, was "cat_win-1.4.2.tar", last modified: Thu May 11 09:26:07 2023, max compression
```

## Comparing `cat_win-1.4.1.tar` & `cat_win-1.4.2.tar`

### file list

```diff
@@ -1,60 +1,61 @@
--rw-r--r--   0        0        0     1090 2023-02-19 10:54:41.226281 cat_win-1.4.1/LICENSE
--rw-r--r--   0        0        0    13844 2023-05-03 09:54:22.285343 cat_win-1.4.1/README.md
--rw-r--r--   0        0        0       39 2023-02-26 11:57:46.261532 cat_win-1.4.1/cat_win/.pytest_cache/.gitignore
--rw-r--r--   0        0        0      191 2023-02-26 11:57:46.261532 cat_win-1.4.1/cat_win/.pytest_cache/CACHEDIR.TAG
--rw-r--r--   0        0        0      310 2023-02-26 11:57:46.261532 cat_win-1.4.1/cat_win/.pytest_cache/README.md
--rw-r--r--   0        0        0     5653 2023-02-26 11:57:52.638849 cat_win-1.4.1/cat_win/.pytest_cache/v/cache/nodeids
--rw-r--r--   0        0        0        2 2023-02-26 11:57:52.639848 cat_win-1.4.1/cat_win/.pytest_cache/v/cache/stepwise
--rw-r--r--   0        0        0      289 2023-05-03 09:25:07.971212 cat_win-1.4.1/cat_win/__init__.py
--rw-r--r--   0        0        0      363 2023-05-01 18:46:04.882782 cat_win-1.4.1/cat_win/__main__.py
--rw-r--r--   0        0        0    34673 2023-05-03 14:39:37.447115 cat_win-1.4.1/cat_win/cat.py
--rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.1/cat_win/const/__init__.py
--rw-r--r--   0        0        0     4717 2023-05-03 09:19:54.039073 cat_win-1.4.1/cat_win/const/argconstants.py
--rw-r--r--   0        0        0     2492 2023-05-01 16:13:49.121661 cat_win-1.4.1/cat_win/const/colorconstants.py
--rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.1/cat_win/persistence/__init__.py
--rw-r--r--   0        0        0     8208 2023-05-01 16:14:23.265362 cat_win-1.4.1/cat_win/persistence/config.py
--rw-r--r--   0        0        0      319 2023-05-01 18:46:08.801676 cat_win-1.4.1/cat_win/shell.py
--rw-r--r--   0        0        0        0 2023-02-19 10:54:41.304282 cat_win-1.4.1/cat_win/tests/__init__.py
--rw-r--r--   0        0        0        0 2023-04-29 10:00:24.210446 cat_win-1.4.1/cat_win/tests/mocks/__init__.py
--rw-r--r--   0        0        0     1347 2023-05-02 09:52:28.939216 cat_win-1.4.1/cat_win/tests/mocks/std.py
--rw-r--r--   0        0        0     1170 2023-05-01 15:49:21.685058 cat_win-1.4.1/cat_win/tests/test_argconstants.py
--rw-r--r--   0        0        0     8294 2023-05-02 08:59:10.289918 cat_win-1.4.1/cat_win/tests/test_argparser.py
--rw-r--r--   0        0        0     7392 2023-05-03 09:05:55.317568 cat_win-1.4.1/cat_win/tests/test_cat.py
--rw-r--r--   0        0        0     1131 2023-05-02 19:37:40.487184 cat_win-1.4.1/cat_win/tests/test_cbase64.py
--rw-r--r--   0        0        0     1569 2023-05-02 19:37:45.944459 cat_win-1.4.1/cat_win/tests/test_checksum.py
--rw-r--r--   0        0        0     3613 2023-05-02 19:37:53.765103 cat_win-1.4.1/cat_win/tests/test_converter.py
--rw-r--r--   0        0        0      823 2023-05-02 19:38:00.930937 cat_win-1.4.1/cat_win/tests/test_file.py
--rw-r--r--   0        0        0     2021 2023-05-01 15:57:01.266856 cat_win-1.4.1/cat_win/tests/test_fileattributes.py
--rw-r--r--   0        0        0     6186 2023-05-02 19:38:14.571569 cat_win-1.4.1/cat_win/tests/test_full.py
--rw-r--r--   0        0        0     6086 2023-05-01 18:44:11.062879 cat_win-1.4.1/cat_win/tests/test_holder.py
--rw-r--r--   0        0        0     7408 2023-05-01 16:03:35.076827 cat_win-1.4.1/cat_win/tests/test_rawviewer.py
--rw-r--r--   0        0        0     4277 2023-05-02 10:37:50.918683 cat_win-1.4.1/cat_win/tests/test_shell.py
--rw-r--r--   0        0        0     1270 2023-05-01 16:04:47.934927 cat_win-1.4.1/cat_win/tests/test_stdinhelper.py
--rw-r--r--   0        0        0     3117 2023-05-02 09:42:04.478371 cat_win-1.4.1/cat_win/tests/test_stringfinder.py
--rw-r--r--   0        0        0     3951 2023-05-02 19:38:32.100152 cat_win-1.4.1/cat_win/tests/test_updatechecker.py
--rw-r--r--   0        0        0      170 2023-02-19 10:54:41.307281 cat_win-1.4.1/cat_win/tests/texts/full_test_result_B.txt
--rw-r--r--   0        0        0      196 2023-02-19 10:54:41.307281 cat_win-1.4.1/cat_win/tests/texts/full_test_result_C.txt
--rw-r--r--   0        0        0      139 2023-02-19 10:54:41.308281 cat_win-1.4.1/cat_win/tests/texts/full_test_result_D.txt
--rw-r--r--   0        0        0      189 2023-02-19 10:54:41.308281 cat_win-1.4.1/cat_win/tests/texts/test.txt
--rw-r--r--   0        0        0        0 2023-03-26 11:37:07.806578 cat_win-1.4.1/cat_win/tests/texts/test_empty.txt
--rw-r--r--   0        0        0       19 2023-02-19 10:54:41.308281 cat_win-1.4.1/cat_win/tests/texts/test_holderEdgeCase_1.txt
--rw-r--r--   0        0        0       21 2023-02-19 10:54:41.308281 cat_win-1.4.1/cat_win/tests/texts/test_holderEdgeCase_2.txt
--rw-r--r--   0        0        0       28 2023-03-26 12:18:11.309629 cat_win-1.4.1/cat_win/tests/texts/test_holderEdgeCase_3.txt
--rw-r--r--   0        0        0       10 2023-02-22 11:49:01.641263 cat_win-1.4.1/cat_win/tests/texts/test_holderEdgeCase_4.txt
--rw-r--r--   0        0        0       62 2023-03-26 12:18:56.747176 cat_win-1.4.1/cat_win/tests/texts/test_peek.txt
--rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.1/cat_win/util/__init__.py
--rw-r--r--   0        0        0     5959 2023-05-02 19:36:46.470436 cat_win-1.4.1/cat_win/util/argparser.py
--rw-r--r--   0        0        0     2765 2023-05-01 13:47:22.633145 cat_win-1.4.1/cat_win/util/cbase64.py
--rw-r--r--   0        0        0     1621 2023-05-01 16:15:32.374189 cat_win-1.4.1/cat_win/util/checksum.py
--rw-r--r--   0        0        0     3221 2023-05-01 14:51:45.585464 cat_win-1.4.1/cat_win/util/converter.py
--rw-r--r--   0        0        0      365 2023-05-01 15:43:43.676935 cat_win-1.4.1/cat_win/util/file.py
--rw-r--r--   0        0        0     3885 2023-05-01 13:59:25.760074 cat_win-1.4.1/cat_win/util/fileattributes.py
--rw-r--r--   0        0        0     6329 2023-05-01 16:17:00.047671 cat_win-1.4.1/cat_win/util/holder.py
--rw-r--r--   0        0        0     2736 2023-05-01 14:12:52.471228 cat_win-1.4.1/cat_win/util/rawviewer.py
--rw-r--r--   0        0        0     6620 2023-05-01 16:17:59.443693 cat_win-1.4.1/cat_win/util/stdinhelper.py
--rw-r--r--   0        0        0     3762 2023-05-01 16:20:02.002989 cat_win-1.4.1/cat_win/util/stringfinder.py
--rw-r--r--   0        0        0      386 2023-05-01 18:45:26.688828 cat_win-1.4.1/cat_win/util/tmpfilehelper.py
--rw-r--r--   0        0        0        0 2023-02-23 20:58:12.051941 cat_win-1.4.1/cat_win/web/__init__.py
--rw-r--r--   0        0        0     5682 2023-05-01 18:45:36.714361 cat_win-1.4.1/cat_win/web/updatechecker.py
--rw-r--r--   0        0        0     1552 2023-04-14 15:23:59.559474 cat_win-1.4.1/pyproject.toml
--rw-r--r--   0        0        0    14828 1970-01-01 00:00:00.000000 cat_win-1.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1090 2023-02-19 10:54:41.226281 cat_win-1.4.2/LICENSE
+-rw-r--r--   0        0        0    13860 2023-05-05 17:29:17.289986 cat_win-1.4.2/README.md
+-rw-r--r--   0        0        0       39 2023-02-26 11:57:46.261532 cat_win-1.4.2/cat_win/.pytest_cache/.gitignore
+-rw-r--r--   0        0        0      191 2023-02-26 11:57:46.261532 cat_win-1.4.2/cat_win/.pytest_cache/CACHEDIR.TAG
+-rw-r--r--   0        0        0      310 2023-02-26 11:57:46.261532 cat_win-1.4.2/cat_win/.pytest_cache/README.md
+-rw-r--r--   0        0        0     5653 2023-02-26 11:57:52.638849 cat_win-1.4.2/cat_win/.pytest_cache/v/cache/nodeids
+-rw-r--r--   0        0        0        2 2023-02-26 11:57:52.639848 cat_win-1.4.2/cat_win/.pytest_cache/v/cache/stepwise
+-rw-r--r--   0        0        0      289 2023-05-11 09:25:47.008420 cat_win-1.4.2/cat_win/__init__.py
+-rw-r--r--   0        0        0      363 2023-05-01 18:46:04.882782 cat_win-1.4.2/cat_win/__main__.py
+-rw-r--r--   0        0        0    35374 2023-05-10 15:30:06.562028 cat_win-1.4.2/cat_win/cat.py
+-rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.2/cat_win/const/__init__.py
+-rw-r--r--   0        0        0     4717 2023-05-03 09:19:54.039073 cat_win-1.4.2/cat_win/const/argconstants.py
+-rw-r--r--   0        0        0     2492 2023-05-01 16:13:49.121661 cat_win-1.4.2/cat_win/const/colorconstants.py
+-rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.2/cat_win/persistence/__init__.py
+-rw-r--r--   0        0        0     8208 2023-05-04 20:42:15.378650 cat_win-1.4.2/cat_win/persistence/config.py
+-rw-r--r--   0        0        0      319 2023-05-01 18:46:08.801676 cat_win-1.4.2/cat_win/shell.py
+-rw-r--r--   0        0        0        0 2023-02-19 10:54:41.304282 cat_win-1.4.2/cat_win/tests/__init__.py
+-rw-r--r--   0        0        0        0 2023-04-29 10:00:24.210446 cat_win-1.4.2/cat_win/tests/mocks/__init__.py
+-rw-r--r--   0        0        0     1443 2023-05-04 13:28:17.759035 cat_win-1.4.2/cat_win/tests/mocks/std.py
+-rw-r--r--   0        0        0     1170 2023-05-01 15:49:21.685058 cat_win-1.4.2/cat_win/tests/test_argconstants.py
+-rw-r--r--   0        0        0     8294 2023-05-02 08:59:10.289918 cat_win-1.4.2/cat_win/tests/test_argparser.py
+-rw-r--r--   0        0        0     7492 2023-05-07 10:04:21.634459 cat_win-1.4.2/cat_win/tests/test_cat.py
+-rw-r--r--   0        0        0     1131 2023-05-02 19:37:40.487184 cat_win-1.4.2/cat_win/tests/test_cbase64.py
+-rw-r--r--   0        0        0     1569 2023-05-02 19:37:45.944459 cat_win-1.4.2/cat_win/tests/test_checksum.py
+-rw-r--r--   0        0        0     1533 2023-05-04 13:57:20.651422 cat_win-1.4.2/cat_win/tests/test_config.py
+-rw-r--r--   0        0        0     3613 2023-05-02 19:37:53.765103 cat_win-1.4.2/cat_win/tests/test_converter.py
+-rw-r--r--   0        0        0      823 2023-05-02 19:38:00.930937 cat_win-1.4.2/cat_win/tests/test_file.py
+-rw-r--r--   0        0        0     2021 2023-05-01 15:57:01.266856 cat_win-1.4.2/cat_win/tests/test_fileattributes.py
+-rw-r--r--   0        0        0     6164 2023-05-07 09:54:17.443534 cat_win-1.4.2/cat_win/tests/test_full.py
+-rw-r--r--   0        0        0     6922 2023-05-08 12:29:13.706678 cat_win-1.4.2/cat_win/tests/test_holder.py
+-rw-r--r--   0        0        0     7408 2023-05-01 16:03:35.076827 cat_win-1.4.2/cat_win/tests/test_rawviewer.py
+-rw-r--r--   0        0        0     4190 2023-05-07 09:56:25.443429 cat_win-1.4.2/cat_win/tests/test_shell.py
+-rw-r--r--   0        0        0     1254 2023-05-04 13:29:46.034492 cat_win-1.4.2/cat_win/tests/test_stdinhelper.py
+-rw-r--r--   0        0        0     3117 2023-05-02 09:42:04.478371 cat_win-1.4.2/cat_win/tests/test_stringfinder.py
+-rw-r--r--   0        0        0     3951 2023-05-02 19:38:32.100152 cat_win-1.4.2/cat_win/tests/test_updatechecker.py
+-rw-r--r--   0        0        0      170 2023-02-19 10:54:41.307281 cat_win-1.4.2/cat_win/tests/texts/full_test_result_B.txt
+-rw-r--r--   0        0        0      196 2023-02-19 10:54:41.307281 cat_win-1.4.2/cat_win/tests/texts/full_test_result_C.txt
+-rw-r--r--   0        0        0      139 2023-02-19 10:54:41.308281 cat_win-1.4.2/cat_win/tests/texts/full_test_result_D.txt
+-rw-r--r--   0        0        0      189 2023-02-19 10:54:41.308281 cat_win-1.4.2/cat_win/tests/texts/test.txt
+-rw-r--r--   0        0        0        0 2023-03-26 11:37:07.806578 cat_win-1.4.2/cat_win/tests/texts/test_empty.txt
+-rw-r--r--   0        0        0       19 2023-02-19 10:54:41.308281 cat_win-1.4.2/cat_win/tests/texts/test_holderEdgeCase_1.txt
+-rw-r--r--   0        0        0       21 2023-02-19 10:54:41.308281 cat_win-1.4.2/cat_win/tests/texts/test_holderEdgeCase_2.txt
+-rw-r--r--   0        0        0       28 2023-03-26 12:18:11.309629 cat_win-1.4.2/cat_win/tests/texts/test_holderEdgeCase_3.txt
+-rw-r--r--   0        0        0       10 2023-02-22 11:49:01.641263 cat_win-1.4.2/cat_win/tests/texts/test_holderEdgeCase_4.txt
+-rw-r--r--   0        0        0       62 2023-03-26 12:18:56.747176 cat_win-1.4.2/cat_win/tests/texts/test_peek.txt
+-rw-r--r--   0        0        0        0 2023-02-23 20:58:12.050939 cat_win-1.4.2/cat_win/util/__init__.py
+-rw-r--r--   0        0        0     5959 2023-05-02 19:36:46.470436 cat_win-1.4.2/cat_win/util/argparser.py
+-rw-r--r--   0        0        0     2765 2023-05-01 13:47:22.633145 cat_win-1.4.2/cat_win/util/cbase64.py
+-rw-r--r--   0        0        0     1621 2023-05-01 16:15:32.374189 cat_win-1.4.2/cat_win/util/checksum.py
+-rw-r--r--   0        0        0     3221 2023-05-01 14:51:45.585464 cat_win-1.4.2/cat_win/util/converter.py
+-rw-r--r--   0        0        0      498 2023-05-05 19:13:34.870700 cat_win-1.4.2/cat_win/util/file.py
+-rw-r--r--   0        0        0     3885 2023-05-08 17:38:04.295791 cat_win-1.4.2/cat_win/util/fileattributes.py
+-rw-r--r--   0        0        0     7006 2023-05-07 19:58:27.528617 cat_win-1.4.2/cat_win/util/holder.py
+-rw-r--r--   0        0        0     2793 2023-05-04 20:39:22.680079 cat_win-1.4.2/cat_win/util/rawviewer.py
+-rw-r--r--   0        0        0     6620 2023-05-08 17:37:42.297614 cat_win-1.4.2/cat_win/util/stdinhelper.py
+-rw-r--r--   0        0        0     3762 2023-05-01 16:20:02.002989 cat_win-1.4.2/cat_win/util/stringfinder.py
+-rw-r--r--   0        0        0      386 2023-05-01 18:45:26.688828 cat_win-1.4.2/cat_win/util/tmpfilehelper.py
+-rw-r--r--   0        0        0        0 2023-02-23 20:58:12.051941 cat_win-1.4.2/cat_win/web/__init__.py
+-rw-r--r--   0        0        0     5851 2023-05-08 17:41:30.393772 cat_win-1.4.2/cat_win/web/updatechecker.py
+-rw-r--r--   0        0        0     1552 2023-04-14 15:23:59.559474 cat_win-1.4.2/pyproject.toml
+-rw-r--r--   0        0        0    14844 1970-01-01 00:00:00.000000 cat_win-1.4.2/PKG-INFO
```

### Comparing `cat_win-1.4.1/LICENSE` & `cat_win-1.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/README.md` & `cat_win-1.4.2/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -82,15 +82,15 @@
 <p align="right">(<a href="#top">back to top</a>)</p>
 
 ## Getting Started
 
 ### Prerequisites
 
 - Using cat_win as a Python-Package demands a Python-Interpreter (>= 3.7).
-- Using cat_win as an Executable (Windows only!) demands no prerequisites, hereby the stand-alone executable `catw.exe`  is sufficient.
+- Using cat_win as an Executable (Windows only!) demands no prerequisites, hereby the stand-alone executables `catw.exe` (& `cats.exe`) are sufficient.
 
 ### Installation
 [![Version][CurrentVersion]](https://pypi.org/project/cat-win/)
 
 Simply install the python package (via [PyPI-cat_win](https://pypi.org/project/cat-win/)):
 ```console
 python -m pip install --upgrade cat_win[clip]
@@ -129,15 +129,15 @@
 cats --help
 ```
 
 | Argument / Option      | Description                                               | works in shell |
 |------------------------|-----------------------------------------------------------|----------------|
 | *-h, --help*           | show help message and exit                                | ✔              |
 | *-v, --version*        | output version information                                | ✔              |
-| *-d, --debug*          | show debug information                                    | ✔              |
+| *--debug, --debug*     | show debug information                                    | ✔              |
 |                        |                                                           |                |
 | *-n, --number*         | number all output lines                                   | ✔              |
 | *-l, --linelength*     | display the length of each line                           | ✔              |
 | *-e, --ends*           | display $ at the end of each line                         | ✔              |
 | *-t, --tabs*           | display TAB characters as ^I                              | ✔              |
 | *--eof, --eof*         | display EOF characters as ^EOF                            | ✔              |
 | *-u, --unique*         | suppress repeated output lines                            | ❌             |
```

#### html2text {}

```diff
@@ -35,70 +35,71 @@
 binary numbers within any text, and much more ... Contrary to the name of the
 project it is of course possible to use cat_win on Linux or MacOS! ### Made
 With [![MadeWith-Python]](https://www.python.org/) [![Python][Python-Version]]
 (https://www.python.org/)
                                                                   (back_to_top)
 ## Getting Started ### Prerequisites - Using cat_win as a Python-Package
 demands a Python-Interpreter (>= 3.7). - Using cat_win as an Executable
-(Windows only!) demands no prerequisites, hereby the stand-alone executable
-`catw.exe` is sufficient. ### Installation [![Version][CurrentVersion]](https:/
-/pypi.org/project/cat-win/) Simply install the python package (via [PyPI-
-cat_win](https://pypi.org/project/cat-win/)): ```console python -m pip install
---upgrade cat_win[clip] ``` cat_win uses the [pyperclip](https://pypi.org/
-project/pyperclip/) module by default. Should any problems occur, you can also
-use the [pyperclip3](https://pypi.org/project/pyperclip3/) or [pyclip](https://
-pypi.org/project/pyclip/) module. In this case simply run: ```console python -
-m pip install --upgrade cat_win ``` and manually install the desired module
-yourself. **OR alternatively** you can use the compiled version (*`Windows
-only`*): 1. Simply download the [catw.exe](https://raw.githubusercontent.com/
-SilenZcience/cat_win/main/bin/catw.exe) file to handle filecontents. 2.
-Download the [cats.exe](https://raw.githubusercontent.com/SilenZcience/cat_win/
-main/bin/cats.exe) file to use the cat-shell (optional). 3. Add the file path
-to your system-environment `PATH`-variables. > â ï¸ **You should never trust
-any executable file!** Feel free to compile the package yourself (e.g. using
-[PyInstaller](https://pyinstaller.org/en/stable/)). > You can verify the
-creation of catw.exe yourself by reading the [source code](https://github.com/
-SilenZcience/cat_win/blob/main/cat_win/cat.py), checking the [origin](https://
-github.com/SilenZcience/cat_win/tree/main/bin) of the file and validating the
+(Windows only!) demands no prerequisites, hereby the stand-alone executables
+`catw.exe` (& `cats.exe`) are sufficient. ### Installation [![Version]
+[CurrentVersion]](https://pypi.org/project/cat-win/) Simply install the python
+package (via [PyPI-cat_win](https://pypi.org/project/cat-win/)): ```console
+python -m pip install --upgrade cat_win[clip] ``` cat_win uses the [pyperclip]
+(https://pypi.org/project/pyperclip/) module by default. Should any problems
+occur, you can also use the [pyperclip3](https://pypi.org/project/pyperclip3/
+) or [pyclip](https://pypi.org/project/pyclip/) module. In this case simply
+run: ```console python -m pip install --upgrade cat_win ``` and manually
+install the desired module yourself. **OR alternatively** you can use the
+compiled version (*`Windows only`*): 1. Simply download the [catw.exe](https://
+raw.githubusercontent.com/SilenZcience/cat_win/main/bin/catw.exe) file to
+handle filecontents. 2. Download the [cats.exe](https://
+raw.githubusercontent.com/SilenZcience/cat_win/main/bin/cats.exe) file to use
+the cat-shell (optional). 3. Add the file path to your system-environment
+`PATH`-variables. > â ï¸ **You should never trust any executable file!** Feel
+free to compile the package yourself (e.g. using [PyInstaller](https://
+pyinstaller.org/en/stable/)). > You can verify the creation of catw.exe
+yourself by reading the [source code](https://github.com/SilenZcience/cat_win/
+blob/main/cat_win/cat.py), checking the [origin](https://github.com/
+SilenZcience/cat_win/tree/main/bin) of the file and validating the
 corresponding [workflow](https://github.com/SilenZcience/cat_win/blob/
 main/.github/workflows/build_executable.yml) used.
                                                                   (back_to_top)
 ## Usage ```console catw [FILE]... [OPTION]... catw --help ``` > â ï¸ *from
 v1.0.33 to v1.1.0 the entrypoint changes from `cat` to `catw`. If you wish to
 keep the old command, you will have to define an alias yourself.* ```console
 cats [OPTION]... cats --help ``` | Argument / Option | Description | works in
 shell | |------------------------|---------------------------------------------
 --------------|----------------| | *-h, --help* | show help message and exit |
-â | | *-v, --version* | output version information | â | | *-d, --debug* |
-show debug information | â | | | | | | *-n, --number* | number all output
-lines | â | | *-l, --linelength* | display the length of each line | â | |
-*-e, --ends* | display $ at the end of each line | â | | *-t, --tabs* |
-display TAB characters as ^I | â | | *--eof, --eof* | display EOF characters
-as ^EOF | â | | *-u, --unique* | suppress repeated output lines | â | | *-
-b, --blank* | hide empty lines | â | | *-r, --reverse* | reverse output | â
-| | *-p, --peek* | only print the first and last lines | â | | *-s, --sum* |
-show sum of lines | â | | *-S, --SUM* | ONLY show sum of lines | â | | *-f,
---files* | list applied files | â | | *-F, --FILES* | ONLY list applied files
-and file sizes | â | | *-g, --grep* | only show lines containing queried
-keywords | â | | *-i, --interactive* | use stdin | â | | *-o, --oneline* |
-take only the first stdin-line | â | | *-E, --ECHO* | handle every following
-parameter as stdin | â | | *-c, --clip* | copy output to clipboard | â | |
-*-m, --checksum* | show the checksums of all files | â | | *-a, --attributes*
-| show meta-information about the files | â | | | | | | *--dec, --DEC* |
-convert decimal numbers to hexadecimal and binary | â | | *--hex, --HEX* |
-convert hexadecimal numbers to decimal and binary | â | | *--bin, --BIN* |
-convert binary numbers to decimal and hexadecimal | â | | *--b64e, --b64e* |
-encode the input to base64 | â | | *--b64d, --b64d* | decode the input from
-base64 | â | | | | | | *--hexview, --HEXVIEW* | display the raw byte
-representation in hexadecimal | â | | *--binview, --binview* | display the
-raw byte representation in binary | â | | | | | | *--nc, --nocolor* | disable
-colored output | â | | *--nb, --nobreak* | do not interrupt the output on
-queried keywords | â | | *--nk, --nokeyword* | inverse the grep output | â
-| | *--config, --config* | change color configuration | â | | | | | | *-R, --
-R\
+â | | *-v, --version* | output version information | â | | *--debug, --
+debug* | show debug information | â | | | | | | *-n, --number* | number all
+output lines | â | | *-l, --linelength* | display the length of each line |
+â | | *-e, --ends* | display $ at the end of each line | â | | *-t, --tabs*
+| display TAB characters as ^I | â | | *--eof, --eof* | display EOF
+characters as ^EOF | â | | *-u, --unique* | suppress repeated output lines |
+â | | *-b, --blank* | hide empty lines | â | | *-r, --reverse* | reverse
+output | â | | *-p, --peek* | only print the first and last lines | â | |
+*-s, --sum* | show sum of lines | â | | *-S, --SUM* | ONLY show sum of lines
+| â | | *-f, --files* | list applied files | â | | *-F, --FILES* | ONLY
+list applied files and file sizes | â | | *-g, --grep* | only show lines
+containing queried keywords | â | | *-i, --interactive* | use stdin | â | |
+*-o, --oneline* | take only the first stdin-line | â | | *-E, --ECHO* |
+handle every following parameter as stdin | â | | *-c, --clip* | copy output
+to clipboard | â | | *-m, --checksum* | show the checksums of all files | â
+| | *-a, --attributes* | show meta-information about the files | â | | | | |
+| *--dec, --DEC* | convert decimal numbers to hexadecimal and binary | â | |
+*--hex, --HEX* | convert hexadecimal numbers to decimal and binary | â | | *-
+-bin, --BIN* | convert binary numbers to decimal and hexadecimal | â | | *--
+b64e, --b64e* | encode the input to base64 | â | | *--b64d, --b64d* | decode
+the input from base64 | â | | | | | | *--hexview, --HEXVIEW* | display the
+raw byte representation in hexadecimal | â | | *--binview, --binview* |
+display the raw byte representation in binary | â | | | | | | *--nc, --
+nocolor* | disable colored output | â | | *--nb, --nobreak* | do not
+interrupt the output on queried keywords | â | | *--nk, --nokeyword* |
+inverse the grep output | â | | *--config, --config* | change color
+configuration | â | | | | | | *-R, --R\
 >* | reconfigure the std-stream(s) with the parsed encoding  \
 > = 'in'/'out'/'err' (default is stdin & stdout)| â | | | | | | *enc=X* | set
 file enconding to X (default is utf-8) | â | | *find=X* | find/query a
 substring X in the given files | â | | *match=X* | find/query a pattern X in
 the given files | â | | *trunc=X:Y* | truncate file to lines X and Y (python-
 like) | â | | | | | | *[a,b]* | replace a with b in every line | â | | *[a:
 âb:c]* | python-like string indexing syntax (line by line) | â | ###
```

### Comparing `cat_win-1.4.1/cat_win/.pytest_cache/v/cache/nodeids` & `cat_win-1.4.2/cat_win/.pytest_cache/v/cache/nodeids`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/cat.py` & `cat_win-1.4.2/cat_win/cat.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,14 +38,17 @@
 arg_parser = ArgParser()
 converter = Converter()
 holder = Holder()
 tmp_file_helper = TmpFileHelper()
 
 on_windows_os = system() == 'Windows'
 
+LARGE_FILE_SIZE = 1024 * 1024 * 100  # 100 Megabytes
+
+
 def exception_handler(exception_type: type, exception, traceback, debug_hook=sys.excepthook) -> None:
     try:
         print(color_dic[CKW.RESET_ALL])
         if holder.args_id[ARGS_DEBUG]:
             debug_hook(exception_type, exception, traceback)
             return
         print(f"\n{exception_type.__name__}{':' * bool(str(exception))} {exception}")
@@ -93,15 +96,15 @@
         help_message += '\t> >>> !help\n'
         help_message += '\t> ...\n'
     else:
         help_message += f"\t{'catw f g -r' : <25}Output g's contents in reverse order, then f's content in reverse order\n"
         help_message += f"\t{'catw f g -ne': <25}Output f's, then g's content, while numerating and showing the end of lines\n"
         help_message += f"\t{'catw f trunc=a:b:c': <25}Output f's content starting at line a, ending at line b, stepping c\n"
     print(help_message)
-    print_update_information(__project__, __version__, color_dic)
+    print_update_information(__project__, __version__, color_dic, on_windows_os)
 
 
 def _show_version() -> None:
     """
     Show the Version message and exit.
     """
     cat_version = f"Catw {__version__} - from {working_dir}\n"
@@ -113,15 +116,15 @@
     version_message += f"Built with: \tPython {__sysversion__}\n"  # sys.version
     try:
         version_message += f"Install time: \t{datetime.fromtimestamp(os.path.getctime(os.path.realpath(__file__)))}\n"
     except OSError: # fails on pyinstaller executable
         version_message += 'Install time: \t-\n'
     version_message += f"Author: \t{__author__}\n"
     print(version_message)
-    print_update_information(__project__, __version__, color_dic)
+    print_update_information(__project__, __version__, color_dic, on_windows_os)
 
 
 def _show_debug(args: list, unknown_args: list, known_files: list, unknown_files: list,
                 echo_args: list) -> None:
     """
     Print all neccassary debug information
     """
@@ -170,17 +173,18 @@
         return
     file_sizes = []
     msg = 'found' if holder.args_id[ARGS_FFILES] else 'applied'
     print(color_dic[CKW.COUNT_AND_FILES], end='')
     print(f"{msg} FILE(s):", end='')
     print(color_dic[CKW.RESET_ALL])
     for file in holder.files:
-        size = get_file_size(file.path)
-        file_sizes.append(size)
-        print(f"\t{color_dic[CKW.COUNT_AND_FILES]}{_convert_size(size): <10}", end='')
+        if file.file_size == -1:
+            file.set_file_size(get_file_size(file.path))
+        file_sizes.append(file.file_size)
+        print(f"\t{color_dic[CKW.COUNT_AND_FILES]}{_convert_size(file.file_size): <10}", end='')
         print(f"{'*' if file.contains_queried else ' '}{file.displayname}{color_dic[CKW.RESET_ALL]}")
     print(color_dic[CKW.COUNT_AND_FILES], end='')
     print(f"Sum:\t{_convert_size(sum(file_sizes))}", end='')
     print(color_dic[CKW.RESET_ALL])
     print(color_dic[CKW.COUNT_AND_FILES], end='')
     print(f"Amount:\t{len(holder.files)}", end='')
     print(color_dic[CKW.RESET_ALL])
@@ -545,15 +549,15 @@
             try:
                 if len(enter_char.encode(arg_parser.file_encoding)) != 3:
                     raise UnicodeEncodeError('', '', -1, -1, '') from exc
             except UnicodeEncodeError:
                 enter_char = 'ENTER'
             print(f"Do you want to open the file as a binary, without parameters? [Y/{enter_char}]:", end='')
             inp = input()
-            if not 'Y' in inp.upper() and inp:
+            if inp and 'Y' not in inp.upper():
                 print('Aborting...')
                 return
         except EOFError:
             pass
         except UnicodeError:
             print(f"Input is not recognized in the given encoding: {arg_parser.file_encoding}")
             print('Aborting...')
@@ -645,15 +649,15 @@
     start = len(holder.files)-1 if holder.reversed else 0
     end = -1 if holder.reversed else len(holder.files)
 
     raw_view_mode = None
     if holder.args_id[ARGS_HEXVIEW] or holder.args_id[ARGS_BINVIEW]:
         for arg, param in holder.args:
             if arg == ARGS_HEXVIEW:
-                raw_view_mode = 'X' if param == param.upper() else 'x'
+                raw_view_mode = 'X' if param.isupper() else 'x'
                 break
             if arg == ARGS_BINVIEW:
                 raw_view_mode = 'b'
                 break
 
     for i in range(start, end, -1 if holder.reversed else 1):
         if raw_view_mode:
@@ -757,14 +761,25 @@
     if holder.args_id[ARGS_FFILES]:
         _show_files()
         return
     if holder.args_id[ARGS_DATA] or holder.args_id[ARGS_CHECKSUM]:
         _print_meta_and_checksum(holder.args_id[ARGS_DATA], holder.args_id[ARGS_CHECKSUM])
         return
 
+    file_size_sum = 0
+    for file in holder.files:
+        file.set_file_size(get_file_size(file.path))
+        file_size_sum += file.file_size
+        if file_size_sum >= LARGE_FILE_SIZE:
+            if (sys.stdout.isatty() and not sys.stdout.closed):
+                print(color_dic[CKW.MESSAGE_IMPORTANT], end='')
+                print('Some files are exceedingly large and may require a lot of time and resources.', end='')
+                print(color_dic[CKW.RESET_ALL])
+            break
+
     if holder.args_id[ARGS_B64D]:
         holder.set_decoding_temp_files([tmp_file_helper.generate_temp_file_name() for _ in holder.files])
     holder.generate_values(arg_parser.file_encoding)
 
     if holder.args_id[ARGS_CCOUNT]:
         _show_count()
         return
@@ -786,14 +801,15 @@
             if holder.args_id[ARGS_DEBUG]:
                 print('FileNotFoundError', tmp_file)
 
 
 def shell_main():
     init(True)
 
+    command_prefix = '!'
     shell_prefix = '>>> '
     eof_control_char = 'Z' if on_windows_os else 'D'
     oneline = holder.args_id[ARGS_ONELINE]
 
     class CmdExec:
         exit_shell = False
 
@@ -812,24 +828,24 @@
                 the line entered in the cat shell
                 
             Returns:
             (bool):
                 indicates if a valid command has been found
                 and executed
             """
-            if cmd[:1] != '!':
+            if cmd[:1] != command_prefix:
                 return False
             line_split = cmd[1:].split(' ')
             method = getattr(self, '_command_' + line_split[0], lambda _: False)
             method(line_split[1:])
             return True
 
         def _command_cat(self, _) -> None:
-            cat = " ,_     _\n |\\\\_,-~/\n / _  _ |    ,--.\n(  @  @ )   / ,-'\n \  _T_/"
-            cat += "-._( (\n /         `. \\\n|         _  \ |\n \ \ ,  /      |\n  || |-_\__   /\n ((_/`(____,-'\n"
+            cat = " ,_     _\n |\\\\_,-~/\n / _  _ |    ,--.\n(  @  @ )   / ,-'\n \\  _T_/"
+            cat += "-._( (\n /         `. \\\n|         _  \\ |\n \\ \\ ,  /      |\n  || |-_\\__   /\n ((_/`(____,-'\n"
             print('\n'.join(['\t\t\t' + c for c in cat.split('\n')]))
 
         def _command_help(self, _) -> None:
             print(f"Type ^{eof_control_char} (Ctrl + {eof_control_char}) or '!exit' to exit.")
             print("Type '!add <OPTION>', '!del <OPTION>', '!see' to change/see the active parameters.")
 
         def _command_add(self, cmd: list) -> None:
```

### Comparing `cat_win-1.4.1/cat_win/const/argconstants.py` & `cat_win-1.4.2/cat_win/const/argconstants.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/const/colorconstants.py` & `cat_win-1.4.2/cat_win/const/colorconstants.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/persistence/config.py` & `cat_win-1.4.2/cat_win/persistence/config.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/mocks/std.py` & `cat_win-1.4.2/cat_win/tests/mocks/std.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,17 @@
         raise StopIteration
 
 
 class StdInMock:
     def __init__(self, input_value: str = '') -> None:
         self.input_value = input_value
 
+    def set_content(self, input_value: str) -> None:
+        self.input_value = input_value
+
     # def reconfigure(self, encoding = None) -> None:
     #     return
 
     def readline(self) -> str:
         return self.input_value.split('\n')[0] + '\n'
 
     def __iter__(self) -> StdInMockIter:
```

### Comparing `cat_win-1.4.1/cat_win/tests/test_argconstants.py` & `cat_win-1.4.2/cat_win/tests/test_argconstants.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_argparser.py` & `cat_win-1.4.2/cat_win/tests/test_argparser.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_cat.py` & `cat_win-1.4.2/cat_win/tests/test_cat.py`

 * *Files 5% similar despite different names*

```diff
@@ -12,126 +12,124 @@
 
 test_file_path = os.path.join(os.path.dirname(__file__), 'texts', 'test.txt')
 test_file_content = []
 with open(test_file_path, 'r', encoding='utf-8') as f:
     test_file_content = f.read().split('\n')
 
 
-holder = Holder()
-
-@patch('cat_win.cat.holder', holder)
 @patch('cat_win.cat.color_dic', dict.fromkeys(cat.color_dic, ''))
 class TestCat(TestCase):
     maxDiff = None
 
     def tearDown(self):
         cat._calculate_line_prefix_spacing.cache_clear()
         cat._calculate_line_length_prefix_spacing.cache_clear()
+        cat.holder = Holder()
 
     def test_cat_output_default_file(self):
-        holder.set_files([test_file_path])
-        holder.set_args([])
+        cat.holder.set_files([test_file_path])
+        cat.holder.set_args([])
 
         check_against = '\n'.join(test_file_content) + '\n'
 
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.edit_files()
             self.assertEqual(fake_out.getvalue(), check_against)
 
     def test_cat_output_multiple_files(self):
-        holder.set_files([test_file_path, test_file_path, test_file_path])
-        holder.set_args([])
+        cat.holder.set_files([test_file_path, test_file_path, test_file_path])
+        cat.holder.set_args([])
 
         check_against = '\n'.join(test_file_content * 3) + '\n'
 
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.edit_files()
             self.assertEqual(fake_out.getvalue(), check_against)
 
     def test_cat_output_reverse(self):
-        holder.set_files([test_file_path])
-        holder.set_args([(5, '')]) #reverse
+        cat.holder.set_files([test_file_path])
+        cat.holder.set_args([(5, '')]) #reverse
 
         check_against = test_file_content
         check_against.reverse()
         check_against = '\n'.join(check_against) + '\n'
 
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.edit_files()
             self.assertEqual(fake_out.getvalue(), check_against)
 
     def test_cat_output_ends_and_tabs(self):
-        holder.set_files([test_file_path])
-        holder.set_args([(2, ''), (3, '')]) #ends & tabs
+        cat.holder.set_files([test_file_path])
+        cat.holder.set_args([(2, ''), (3, '')]) #ends & tabs
 
         check_against = ('\n'.join([c.replace('\t', '^I') + '$' for c in test_file_content]) +
                          '\n')
 
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.edit_files()
             self.assertEqual(fake_out.getvalue(), check_against)
 
     def test_cat__get_line_prefix_file_excess(self):
-        holder.all_line_number_place_holder = 5
+        cat.holder.all_line_number_place_holder = 5
         self.assertEqual(cat._get_line_prefix(9, 1), '    9) ')
 
     def test_cat__get_line_prefix_file_occupied(self):
-        holder.all_line_number_place_holder = 2
+        cat.holder.all_line_number_place_holder = 2
         self.assertEqual(cat._get_line_prefix(10, 1), '10) ')
 
     def test_cat__get_line_prefix_file_excess_long(self):
-        holder.all_line_number_place_holder = 12
+        cat.holder.all_line_number_place_holder = 12
         self.assertEqual(cat._get_line_prefix(34719, 1), '       34719) ')
 
     def test_cat__get_line_prefix_file_occupied_long(self):
-        holder.all_line_number_place_holder = 5
+        cat.holder.all_line_number_place_holder = 5
         self.assertEqual(cat._get_line_prefix(34718, 1), '34718) ')
 
     def test_cat__get_line_prefix_files_excess(self):
-        holder.all_line_number_place_holder = 5
-        holder.file_number_place_holder = 4
-        holder.files = [1,2]
+        cat.holder.all_line_number_place_holder = 5
+        cat.holder.file_number_place_holder = 4
+        cat.holder.files = [1,2]
         self.assertEqual(cat._get_line_prefix(9, 1), '   1.    9) ')
 
     def test_cat__get_line_prefix_files_occupied(self):
-        holder.all_line_number_place_holder = 3
-        holder.file_number_place_holder = 2
-        holder.files = [1,2]
+        cat.holder.all_line_number_place_holder = 3
+        cat.holder.file_number_place_holder = 2
+        cat.holder.files = [1,2]
         self.assertEqual(cat._get_line_prefix(987, 10), '10.987) ')
 
     def test_cat__get_line_prefix_files_excess_long(self):
-        holder.all_line_number_place_holder = 12
-        holder.file_number_place_holder = 10
-        holder.files = [1,2]
+        cat.holder.all_line_number_place_holder = 12
+        cat.holder.file_number_place_holder = 10
+        cat.holder.files = [1,2]
         self.assertEqual(cat._get_line_prefix(101, 404), '       404.         101) ')
 
     def test_cat__get_line_prefix_files_occupied_long(self):
-        holder.all_line_number_place_holder = 11
-        holder.file_number_place_holder = 9
-        holder.files = [1,2]
+        cat.holder.all_line_number_place_holder = 11
+        cat.holder.file_number_place_holder = 9
+        cat.holder.files = [1,2]
         self.assertEqual(cat._get_line_prefix(12345123451, 123456789), '123456789.12345123451) ')
 
     def test_cat__get_line_length_prefix_string_excess(self):
-        holder.file_line_length_place_holder = 5
-        holder.set_args([])
+        cat.holder.file_line_length_place_holder = 5
+        cat.holder.set_args([])
         self.assertEqual(cat._get_line_length_prefix('testtest', 'abcdefghi'), 'testtest[    9] ')
 
     def test_cat__get_line_length_prefix_string_occupied(self):
-        holder.file_line_length_place_holder = 2
-        holder.set_args([])
+        cat.holder.file_line_length_place_holder = 2
+        cat.holder.set_args([])
         self.assertEqual(cat._get_line_length_prefix('prefix', 'abcdefghij'), 'prefix[10] ')
 
     def test_cat__get_line_length_prefix_bytes_excess(self):
-        holder.file_line_length_place_holder = 5
-        holder.set_args([])
+        cat.holder.file_line_length_place_holder = 5
+        cat.holder.set_args([])
         self.assertEqual(cat._get_line_length_prefix('testtest', b'abcdefghi'), 'testtest[    9] ')
 
     def test_cat__get_line_length_prefix_bytes_occupied(self):
-        holder.file_line_length_place_holder = 2
-        holder.set_args([])
+        cat.holder.file_line_length_place_holder = 2
+        cat.holder.set_args([])
         self.assertEqual(cat._get_line_length_prefix('prefix', b'abcdefghij'), 'prefix[10] ')
 
     def test_remove_ansi_codes_from_line(self):
         red = '\x1b[31m'
         reset = '\x1b[0m'
         random_string = f"abc{red}defghij{reset}klmnopq{red}r{reset}"
         expected_output = 'abcdefghijklmnopqr'
```

### Comparing `cat_win-1.4.1/cat_win/tests/test_cbase64.py` & `cat_win-1.4.2/cat_win/tests/test_cbase64.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_checksum.py` & `cat_win-1.4.2/cat_win/tests/test_checksum.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_converter.py` & `cat_win-1.4.2/cat_win/tests/test_converter.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_file.py` & `cat_win-1.4.2/cat_win/tests/test_file.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_fileattributes.py` & `cat_win-1.4.2/cat_win/tests/test_fileattributes.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_full.py` & `cat_win-1.4.2/cat_win/tests/test_full.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 from unittest.mock import patch
 from unittest import TestCase
 import os
 
 from cat_win import cat
 from cat_win.tests.mocks.std import StdInMock, StdOutMock
 from cat_win.util.argparser import ArgParser
+from cat_win.util.holder import Holder
 # import sys
 # sys.path.append('../cat_win')
 
 
 test_file_dir = os.path.join(os.path.dirname(__file__), 'texts')
 test_file_path  = os.path.join(test_file_dir, 'test.txt')
 test_empty_path = os.path.join(test_file_dir, 'test_empty.txt')
@@ -22,16 +23,15 @@
 class TestCatFull(TestCase):
     maxDiff = None
 
     def tearDown(self):
         cat._calculate_line_prefix_spacing.cache_clear()
         cat._calculate_line_length_prefix_spacing.cache_clear()
         cat.arg_parser = ArgParser()
-        for i in range(len(cat.holder.args_id)):
-            cat.holder.args_id[i] = False
+        cat.holder = Holder()
 
     # no files parsed
     @patch('cat_win.cat.sys.argv', ['<CAT>', '-ln', '--nc', '[::-2]', 'enc=utf8'])
     def test_cat_output_full_a(self):
         expected_output = ''
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.main()
```

### Comparing `cat_win-1.4.1/cat_win/tests/test_rawviewer.py` & `cat_win-1.4.2/cat_win/tests/test_rawviewer.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_shell.py` & `cat_win-1.4.2/cat_win/tests/test_shell.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,36 +1,34 @@
 from unittest.mock import patch
 from unittest import TestCase
 
 from cat_win import cat
 from cat_win.tests.mocks.std import StdInHelperMock, StdOutMock
-from cat_win.util.argparser import ArgParser
 from cat_win.util.holder import Holder
 # import sys
 # sys.path.append('../cat_win')
 stdinhelpermock = StdInHelperMock()
 
 
 @patch('cat_win.cat.sys.argv', ['<CAT>'])
 @patch('cat_win.cat.stdinhelper.get_stdin_content', stdinhelpermock.get_stdin_content)
 class TestShell(TestCase):
     maxDiff = None
 
     def tearDown(self):
         cat._calculate_line_prefix_spacing.cache_clear()
         cat._calculate_line_length_prefix_spacing.cache_clear()
-        cat.arg_parser = ArgParser()
         cat.holder = Holder()
 
     def test_cat_shell_output_unchanged(self):
         stdinhelpermock.set_content('abc\nxyz')
         expected_output = ['abc', 'xyz']
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.shell_main()
-            fake_output = [line.lstrip('>>> ')for line in fake_out.getvalue().splitlines()[2:-1]]
+            fake_output = [line.lstrip('>>> ') for line in fake_out.getvalue().splitlines()[2:-1]]
             self.assertListEqual(fake_output, expected_output)
 
     def test_cat_shell_line_count(self):
         stdinhelpermock.set_content('test1\n!add -n\n!help\ntest2')
         expected_output = ['2) test2']
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.shell_main()
@@ -65,15 +63,15 @@
     def test_cat_shell_exit(self):
         stdinhelpermock.set_content('abc\n!exit\nabc')
         expected_output = ['abc']
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.shell_main()
             fake_output = [line.lstrip('>>> ') for line in fake_out.getvalue().splitlines()[2:-1]]
             self.assertListEqual(fake_output, expected_output)
-    
+
     def test_cat_shell_cmd_escape(self):
         stdinhelpermock.set_content('\\!exit\ntest')
         expected_output = ['!exit', 'test']
         with patch('cat_win.cat.sys.stdout', new=StdOutMock()) as fake_out:
             cat.shell_main()
             fake_output = [line.lstrip('>>> ') for line in fake_out.getvalue().splitlines()[2:-1]]
             self.assertListEqual(fake_output, expected_output)
```

### Comparing `cat_win-1.4.1/cat_win/tests/test_stringfinder.py` & `cat_win-1.4.2/cat_win/tests/test_stringfinder.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/tests/test_updatechecker.py` & `cat_win-1.4.2/cat_win/tests/test_updatechecker.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/util/argparser.py` & `cat_win-1.4.2/cat_win/util/argparser.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/util/cbase64.py` & `cat_win-1.4.2/cat_win/util/cbase64.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/util/checksum.py` & `cat_win-1.4.2/cat_win/util/checksum.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/util/converter.py` & `cat_win-1.4.2/cat_win/util/converter.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/util/fileattributes.py` & `cat_win-1.4.2/cat_win/util/fileattributes.py`

 * *Files 0% similar despite different names*

```diff
@@ -83,15 +83,15 @@
     """
     calculate file metadata information.
     
     Parameters:
     file (str):
         a string representation of a file (-path)
     on_windows_os (bool):
-        indicates if the user is on windows os using
+        indicates if the user is on windows OS using
         platform.system() == 'Windows'
     colors (list):
         a list containing the ANSI-Colorcodes to display
         the attributes like [RESET_ALL, ATTRIB, +ATTRIB, -ATTRIB]
     
     Returns:
     meta_data (str):
```

### Comparing `cat_win-1.4.1/cat_win/util/holder.py` & `cat_win-1.4.2/cat_win/util/holder.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,16 +1,40 @@
-from functools import lru_cache, reduce
+from functools import lru_cache
 from heapq import nlargest
 
 from cat_win.const.argconstants import HIGHEST_ARG_ID, ARGS_NOCOL, ARGS_LLENGTH, ARGS_NUMBER, \
-    ARGS_REVERSE, ARGS_B64D, ARGS_B64E
+    ARGS_REVERSE, ARGS_B64D, ARGS_B64E, ARGS_COUNT, ARGS_CCOUNT
 from cat_win.util.cbase64 import _decode_base64
 from cat_win.util.file import File
 
 
+def reduce_list(args: list) -> list:
+    """
+    remove duplicate args regardless if shortform or
+    longform has been used.
+    
+    Parameters:
+    args (list):
+        the entire list of args, containing possible duplicates
+        
+    Returns:
+    new_args (list):
+        the args-list without duplicates
+    """
+    new_args = []
+    temp_args_id = []
+    
+    for arg in args:
+        id, _ = arg
+        if id not in temp_args_id:
+            temp_args_id.append(id)
+            new_args.append(arg)
+    return new_args
+
+
 class Holder():
     def __init__(self) -> None:
         self.files: list = []  # all files, including tmp-file from stdin
         self._inner_files: list = []
         self.args: list = []  # list of all used parameters: format [[id, param]]
         self.args_id: list = [False] * (HIGHEST_ARG_ID + 1)
         self.temp_file_stdin = None  # if stdin is used, this temp_file will contain the stdin-input
@@ -51,15 +75,15 @@
         return file
 
     def set_files(self, files: list) -> None:
         self.files = [File(path, self._get_file_display_name(path)) for path in files]
         self._inner_files = files[:]
 
     def set_args(self, args: list) -> None:
-        self.args = reduce(lambda l, x: l + [x] if x not in l else l, args, [])
+        self.args = reduce_list(args)
         for arg_id, _ in self.args:
             self.args_id[arg_id] = True
         if self.args_id[ARGS_B64E]:
             self.args_id[ARGS_NOCOL] = True
             # prefix will be deleted anyway
             self.args_id[ARGS_LLENGTH] = False
             self.args_id[ARGS_NUMBER] = False
@@ -67,15 +91,15 @@
 
     def add_args(self, args: list) -> None:
         self.args_id = [False] * (HIGHEST_ARG_ID + 1)
         self.set_args(self.args + args)
 
     def delete_args(self, args: list) -> None:
         self.args_id = [False] * (HIGHEST_ARG_ID + 1)
-        self.set_args([arg for arg in self.args if not arg in args])
+        self.set_args([arg for arg in self.args if arg not in args])
 
     def set_temp_file_stdin(self, file: str) -> None:
         self.temp_file_stdin = file
 
     def set_temp_file_echo(self, file: str) -> None:
         self.temp_file_echo = file
 
@@ -85,15 +109,15 @@
     def __count_generator__(self, reader):
         """
         Parameters:
         reader (method):
             the method to read from
         
         Yields:
-        b (bytes):
+        byt (bytes):
             the bytes in chunks read from the reader
         """
         byt = reader(1024 * 1024)
         while byt:
             yield byt
             byt = reader(1024 * 1024)
 
@@ -152,9 +176,11 @@
     def generate_values(self, encoding: str) -> None:
         self.__calc_file_number_place_holder__()
         if self.args_id[ARGS_B64D]:
             for i, file in enumerate(self.files):
                 with open(file.path, 'rb') as raw_f_read:
                     with open(self._inner_files[i], 'wb') as raw_f_write:
                         raw_f_write.write(_decode_base64(raw_f_read.read().decode(encoding)))
-        self.__calc_place_holder__()
-        self.__calc_file_line_length_place_holder__()
+        if self.args_id[ARGS_COUNT] or self.args_id[ARGS_CCOUNT] or self.args_id[ARGS_NUMBER]:
+            self.__calc_place_holder__()
+        if self.args_id[ARGS_LLENGTH]:
+            self.__calc_file_line_length_place_holder__()
```

### Comparing `cat_win-1.4.1/cat_win/util/rawviewer.py` & `cat_win-1.4.2/cat_win/util/rawviewer.py`

 * *Files 5% similar despite different names*

```diff
@@ -21,14 +21,16 @@
     current_line (str):
         a string representation that, when put together, forms the hexviewer
         output containing the header and line information aswell
         as the bytes themselves
     """
     if colors is None or len(colors) < 2:
         colors = ['', '']
+    if mode not in ['x', 'X', 'b']:
+        mode = 'X'
 
     CRLF = {10: '␤', 13: '␍'}
 
     try:
         if len(CRLF[10].encode(file_encoding)) != 3:
             raise UnicodeEncodeError('', '', -1, -1, '')
     except UnicodeEncodeError:
```

### Comparing `cat_win-1.4.1/cat_win/util/stdinhelper.py` & `cat_win-1.4.2/cat_win/util/stdinhelper.py`

 * *Files 1% similar despite different names*

```diff
@@ -182,15 +182,15 @@
     
     Parameters:
     file_list (list):
         all files that should be written
     file_encoding (str):
         the encoding to use for writing the files
     on_windows_os (bool):
-        indicates if the user is on windows os using
+        indicates if the user is on windows OS using
         platform.system() == 'Windows'
     one_line (bool):
         determines if only the first stdin line should be read
         
     Returns:
     (list):
         containing all files, that could succesfully be written.
```

### Comparing `cat_win-1.4.1/cat_win/util/stringfinder.py` & `cat_win-1.4.2/cat_win/util/stringfinder.py`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/cat_win/web/updatechecker.py` & `cat_win-1.4.2/cat_win/web/updatechecker.py`

 * *Files 2% similar despite different names*

```diff
@@ -116,40 +116,43 @@
             status = STATUS_PRE_RELEASE_AVAILABLE
             break
     if i < len(current):
         status *= -1
     return status
 
 
-def print_update_information(package: str, current_version: str, color_dic: dict) -> None:
+def print_update_information(package: str, current_version: str, color_dic: dict, on_windows_os: bool) -> None:
     """
     prints update information if there are any.
     
     Parameters:
     package (str):
         the package name to check
     current_version (str):
         a version representation as string of the current version
     color_dic (dict):
         a dictionary translating the color-keywords to ANSI-Colorcodes
+    on_windows_os (bool):
+        indicates if the user is on windows OS using
+        platform.system() == 'Windows'
     """
     latest_version = get_latest_package_version(package)
     status = new_version_available(current_version, latest_version)
     if status == STATUS_UP_TO_DATE:
         return
     message = ''
     warning = ''
     info    = ''
     if abs(status) == STATUS_STABLE_RELEASE_AVAILABLE:
         message += f"{color_dic[CKW.MESSAGE_IMPORTANT]}"
         message += f"A new stable release of {package} is available: v{latest_version}"
         message += f"{color_dic[CKW.RESET_ALL]}\n{color_dic[CKW.MESSAGE_IMPORTANT]}"
         message += 'To update, run:'
         message += f"{color_dic[CKW.RESET_ALL]}\n{color_dic[CKW.MESSAGE_IMPORTANT]}"
-        message += f"python -m pip install --upgrade {package}"
+        message += f"python{'3' * (not on_windows_os)} -m pip install --upgrade {package}"
     elif abs(status) == STATUS_PRE_RELEASE_AVAILABLE:
         message += f"{color_dic[CKW.MESSAGE_INFORMATION]}"
         message += f"A new pre-release of {package} is available: v{latest_version}"
     message += f"{color_dic[CKW.RESET_ALL]}"
     if status < STATUS_UP_TO_DATE:
         warning += f"{color_dic[CKW.MESSAGE_WARNING]}"
         warning += 'Warning: Due to the drastic version increase, backwards compatibility is no longer guaranteed!'
```

### Comparing `cat_win-1.4.1/pyproject.toml` & `cat_win-1.4.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `cat_win-1.4.1/PKG-INFO` & `cat_win-1.4.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cat_win
-Version: 1.4.1
+Version: 1.4.2
 Summary: Simple OS Independent 'cat' Command-line Tool made in Python.
 Keywords: cat,cli,console,crossplatform,python,terminal
 Author-email: "Silas A. Kraume" <silas.kraume1552@gmail.com>
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
@@ -110,15 +110,15 @@
 <p align="right">(<a href="#top">back to top</a>)</p>
 
 ## Getting Started
 
 ### Prerequisites
 
 - Using cat_win as a Python-Package demands a Python-Interpreter (>= 3.7).
-- Using cat_win as an Executable (Windows only!) demands no prerequisites, hereby the stand-alone executable `catw.exe`  is sufficient.
+- Using cat_win as an Executable (Windows only!) demands no prerequisites, hereby the stand-alone executables `catw.exe` (& `cats.exe`) are sufficient.
 
 ### Installation
 [![Version][CurrentVersion]](https://pypi.org/project/cat-win/)
 
 Simply install the python package (via [PyPI-cat_win](https://pypi.org/project/cat-win/)):
 ```console
 python -m pip install --upgrade cat_win[clip]
@@ -157,15 +157,15 @@
 cats --help
 ```
 
 | Argument / Option      | Description                                               | works in shell |
 |------------------------|-----------------------------------------------------------|----------------|
 | *-h, --help*           | show help message and exit                                | ✔              |
 | *-v, --version*        | output version information                                | ✔              |
-| *-d, --debug*          | show debug information                                    | ✔              |
+| *--debug, --debug*     | show debug information                                    | ✔              |
 |                        |                                                           |                |
 | *-n, --number*         | number all output lines                                   | ✔              |
 | *-l, --linelength*     | display the length of each line                           | ✔              |
 | *-e, --ends*           | display $ at the end of each line                         | ✔              |
 | *-t, --tabs*           | display TAB characters as ^I                              | ✔              |
 | *--eof, --eof*         | display EOF characters as ^EOF                            | ✔              |
 | *-u, --unique*         | suppress repeated output lines                            | ❌             |
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: cat_win Version: 1.4.1 Summary: Simple OS
+Metadata-Version: 2.1 Name: cat_win Version: 1.4.2 Summary: Simple OS
 Independent 'cat' Command-line Tool made in Python. Keywords:
 cat,cli,console,crossplatform,python,terminal Author-email: "Silas A. Kraume"
 kraume1552@gmail.com> Requires-Python: >=3.7 Description-Content-Type: text/
 markdown Classifier: License :: OSI Approved :: MIT License Classifier:
 Programming Language :: Python Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
@@ -52,70 +52,71 @@
 binary numbers within any text, and much more ... Contrary to the name of the
 project it is of course possible to use cat_win on Linux or MacOS! ### Made
 With [![MadeWith-Python]](https://www.python.org/) [![Python][Python-Version]]
 (https://www.python.org/)
                                                                   (back_to_top)
 ## Getting Started ### Prerequisites - Using cat_win as a Python-Package
 demands a Python-Interpreter (>= 3.7). - Using cat_win as an Executable
-(Windows only!) demands no prerequisites, hereby the stand-alone executable
-`catw.exe` is sufficient. ### Installation [![Version][CurrentVersion]](https:/
-/pypi.org/project/cat-win/) Simply install the python package (via [PyPI-
-cat_win](https://pypi.org/project/cat-win/)): ```console python -m pip install
---upgrade cat_win[clip] ``` cat_win uses the [pyperclip](https://pypi.org/
-project/pyperclip/) module by default. Should any problems occur, you can also
-use the [pyperclip3](https://pypi.org/project/pyperclip3/) or [pyclip](https://
-pypi.org/project/pyclip/) module. In this case simply run: ```console python -
-m pip install --upgrade cat_win ``` and manually install the desired module
-yourself. **OR alternatively** you can use the compiled version (*`Windows
-only`*): 1. Simply download the [catw.exe](https://raw.githubusercontent.com/
-SilenZcience/cat_win/main/bin/catw.exe) file to handle filecontents. 2.
-Download the [cats.exe](https://raw.githubusercontent.com/SilenZcience/cat_win/
-main/bin/cats.exe) file to use the cat-shell (optional). 3. Add the file path
-to your system-environment `PATH`-variables. > â ï¸ **You should never trust
-any executable file!** Feel free to compile the package yourself (e.g. using
-[PyInstaller](https://pyinstaller.org/en/stable/)). > You can verify the
-creation of catw.exe yourself by reading the [source code](https://github.com/
-SilenZcience/cat_win/blob/main/cat_win/cat.py), checking the [origin](https://
-github.com/SilenZcience/cat_win/tree/main/bin) of the file and validating the
+(Windows only!) demands no prerequisites, hereby the stand-alone executables
+`catw.exe` (& `cats.exe`) are sufficient. ### Installation [![Version]
+[CurrentVersion]](https://pypi.org/project/cat-win/) Simply install the python
+package (via [PyPI-cat_win](https://pypi.org/project/cat-win/)): ```console
+python -m pip install --upgrade cat_win[clip] ``` cat_win uses the [pyperclip]
+(https://pypi.org/project/pyperclip/) module by default. Should any problems
+occur, you can also use the [pyperclip3](https://pypi.org/project/pyperclip3/
+) or [pyclip](https://pypi.org/project/pyclip/) module. In this case simply
+run: ```console python -m pip install --upgrade cat_win ``` and manually
+install the desired module yourself. **OR alternatively** you can use the
+compiled version (*`Windows only`*): 1. Simply download the [catw.exe](https://
+raw.githubusercontent.com/SilenZcience/cat_win/main/bin/catw.exe) file to
+handle filecontents. 2. Download the [cats.exe](https://
+raw.githubusercontent.com/SilenZcience/cat_win/main/bin/cats.exe) file to use
+the cat-shell (optional). 3. Add the file path to your system-environment
+`PATH`-variables. > â ï¸ **You should never trust any executable file!** Feel
+free to compile the package yourself (e.g. using [PyInstaller](https://
+pyinstaller.org/en/stable/)). > You can verify the creation of catw.exe
+yourself by reading the [source code](https://github.com/SilenZcience/cat_win/
+blob/main/cat_win/cat.py), checking the [origin](https://github.com/
+SilenZcience/cat_win/tree/main/bin) of the file and validating the
 corresponding [workflow](https://github.com/SilenZcience/cat_win/blob/
 main/.github/workflows/build_executable.yml) used.
                                                                   (back_to_top)
 ## Usage ```console catw [FILE]... [OPTION]... catw --help ``` > â ï¸ *from
 v1.0.33 to v1.1.0 the entrypoint changes from `cat` to `catw`. If you wish to
 keep the old command, you will have to define an alias yourself.* ```console
 cats [OPTION]... cats --help ``` | Argument / Option | Description | works in
 shell | |------------------------|---------------------------------------------
 --------------|----------------| | *-h, --help* | show help message and exit |
-â | | *-v, --version* | output version information | â | | *-d, --debug* |
-show debug information | â | | | | | | *-n, --number* | number all output
-lines | â | | *-l, --linelength* | display the length of each line | â | |
-*-e, --ends* | display $ at the end of each line | â | | *-t, --tabs* |
-display TAB characters as ^I | â | | *--eof, --eof* | display EOF characters
-as ^EOF | â | | *-u, --unique* | suppress repeated output lines | â | | *-
-b, --blank* | hide empty lines | â | | *-r, --reverse* | reverse output | â
-| | *-p, --peek* | only print the first and last lines | â | | *-s, --sum* |
-show sum of lines | â | | *-S, --SUM* | ONLY show sum of lines | â | | *-f,
---files* | list applied files | â | | *-F, --FILES* | ONLY list applied files
-and file sizes | â | | *-g, --grep* | only show lines containing queried
-keywords | â | | *-i, --interactive* | use stdin | â | | *-o, --oneline* |
-take only the first stdin-line | â | | *-E, --ECHO* | handle every following
-parameter as stdin | â | | *-c, --clip* | copy output to clipboard | â | |
-*-m, --checksum* | show the checksums of all files | â | | *-a, --attributes*
-| show meta-information about the files | â | | | | | | *--dec, --DEC* |
-convert decimal numbers to hexadecimal and binary | â | | *--hex, --HEX* |
-convert hexadecimal numbers to decimal and binary | â | | *--bin, --BIN* |
-convert binary numbers to decimal and hexadecimal | â | | *--b64e, --b64e* |
-encode the input to base64 | â | | *--b64d, --b64d* | decode the input from
-base64 | â | | | | | | *--hexview, --HEXVIEW* | display the raw byte
-representation in hexadecimal | â | | *--binview, --binview* | display the
-raw byte representation in binary | â | | | | | | *--nc, --nocolor* | disable
-colored output | â | | *--nb, --nobreak* | do not interrupt the output on
-queried keywords | â | | *--nk, --nokeyword* | inverse the grep output | â
-| | *--config, --config* | change color configuration | â | | | | | | *-R, --
-R\
+â | | *-v, --version* | output version information | â | | *--debug, --
+debug* | show debug information | â | | | | | | *-n, --number* | number all
+output lines | â | | *-l, --linelength* | display the length of each line |
+â | | *-e, --ends* | display $ at the end of each line | â | | *-t, --tabs*
+| display TAB characters as ^I | â | | *--eof, --eof* | display EOF
+characters as ^EOF | â | | *-u, --unique* | suppress repeated output lines |
+â | | *-b, --blank* | hide empty lines | â | | *-r, --reverse* | reverse
+output | â | | *-p, --peek* | only print the first and last lines | â | |
+*-s, --sum* | show sum of lines | â | | *-S, --SUM* | ONLY show sum of lines
+| â | | *-f, --files* | list applied files | â | | *-F, --FILES* | ONLY
+list applied files and file sizes | â | | *-g, --grep* | only show lines
+containing queried keywords | â | | *-i, --interactive* | use stdin | â | |
+*-o, --oneline* | take only the first stdin-line | â | | *-E, --ECHO* |
+handle every following parameter as stdin | â | | *-c, --clip* | copy output
+to clipboard | â | | *-m, --checksum* | show the checksums of all files | â
+| | *-a, --attributes* | show meta-information about the files | â | | | | |
+| *--dec, --DEC* | convert decimal numbers to hexadecimal and binary | â | |
+*--hex, --HEX* | convert hexadecimal numbers to decimal and binary | â | | *-
+-bin, --BIN* | convert binary numbers to decimal and hexadecimal | â | | *--
+b64e, --b64e* | encode the input to base64 | â | | *--b64d, --b64d* | decode
+the input from base64 | â | | | | | | *--hexview, --HEXVIEW* | display the
+raw byte representation in hexadecimal | â | | *--binview, --binview* |
+display the raw byte representation in binary | â | | | | | | *--nc, --
+nocolor* | disable colored output | â | | *--nb, --nobreak* | do not
+interrupt the output on queried keywords | â | | *--nk, --nokeyword* |
+inverse the grep output | â | | *--config, --config* | change color
+configuration | â | | | | | | *-R, --R\
 >* | reconfigure the std-stream(s) with the parsed encoding  \
 > = 'in'/'out'/'err' (default is stdin & stdout)| â | | | | | | *enc=X* | set
 file enconding to X (default is utf-8) | â | | *find=X* | find/query a
 substring X in the given files | â | | *match=X* | find/query a pattern X in
 the given files | â | | *trunc=X:Y* | truncate file to lines X and Y (python-
 like) | â | | | | | | *[a,b]* | replace a with b in every line | â | | *[a:
 âb:c]* | python-like string indexing syntax (line by line) | â | ###
```

