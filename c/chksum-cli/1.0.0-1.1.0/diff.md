# Comparing `tmp/chksum-cli-1.0.0.tar.gz` & `tmp/chksum-cli-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chksum-cli-1.0.0.tar", last modified: Thu Dec 15 04:32:26 2022, max compression
+gzip compressed data, was "chksum-cli-1.1.0.tar", last modified: Sat May 13 20:08:56 2023, max compression
```

## Comparing `chksum-cli-1.0.0.tar` & `chksum-cli-1.1.0.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxrwxrwx   0        0        0        0 2022-12-15 04:32:26.854526 chksum-cli-1.0.0/
--rw-rw-rw-   0        0        0    35823 2022-11-27 23:39:31.000000 chksum-cli-1.0.0/LICENSE
--rw-rw-rw-   0        0        0     3136 2022-12-15 04:32:26.854026 chksum-cli-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0     2487 2022-12-15 04:16:18.000000 chksum-cli-1.0.0/README.md
--rw-rw-rw-   0        0        0      834 2022-12-15 03:58:03.000000 chksum-cli-1.0.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2022-12-15 04:32:26.854526 chksum-cli-1.0.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2022-12-15 04:32:26.824528 chksum-cli-1.0.0/src/
-drwxrwxrwx   0        0        0        0 2022-12-15 04:32:26.832526 chksum-cli-1.0.0/src/chksum_cli/
--rw-rw-rw-   0        0        0       83 2022-12-14 16:07:58.000000 chksum-cli-1.0.0/src/chksum_cli/__init__.py
--rw-rw-rw-   0        0        0      252 2022-12-14 16:08:04.000000 chksum-cli-1.0.0/src/chksum_cli/__main__.py
--rw-rw-rw-   0        0        0    15217 2022-12-15 04:30:49.000000 chksum-cli-1.0.0/src/chksum_cli/chksum.py
--rw-rw-rw-   0        0        0      225 2022-12-14 16:08:13.000000 chksum-cli-1.0.0/src/chksum_cli/launcher.py
-drwxrwxrwx   0        0        0        0 2022-12-15 04:32:26.851526 chksum-cli-1.0.0/src/chksum_cli.egg-info/
--rw-rw-rw-   0        0        0     3136 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      381 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       49 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       32 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2022-12-15 04:32:26.000000 chksum-cli-1.0.0/src/chksum_cli.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2022-12-15 04:32:26.852526 chksum-cli-1.0.0/test/
--rw-rw-rw-   0        0        0     2856 2022-12-13 19:51:32.000000 chksum-cli-1.0.0/test/test.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:08:56.881754 chksum-cli-1.1.0/
+-rw-rw-rw-   0        0        0    35823 2022-11-27 23:39:31.000000 chksum-cli-1.1.0/LICENSE
+-rw-rw-rw-   0        0        0     3440 2023-05-13 20:08:56.880754 chksum-cli-1.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     2791 2023-05-05 21:40:18.000000 chksum-cli-1.1.0/README.md
+-rw-rw-rw-   0        0        0      834 2023-05-05 21:41:05.000000 chksum-cli-1.1.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 20:08:56.881754 chksum-cli-1.1.0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 20:08:56.834758 chksum-cli-1.1.0/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 20:08:56.851755 chksum-cli-1.1.0/src/chksum_cli/
+-rw-rw-rw-   0        0        0       83 2022-12-14 16:07:58.000000 chksum-cli-1.1.0/src/chksum_cli/__init__.py
+-rw-rw-rw-   0        0        0      252 2022-12-14 16:08:04.000000 chksum-cli-1.1.0/src/chksum_cli/__main__.py
+-rw-rw-rw-   0        0        0    16581 2023-05-05 21:39:11.000000 chksum-cli-1.1.0/src/chksum_cli/chksum.py
+-rw-rw-rw-   0        0        0      225 2022-12-14 16:08:13.000000 chksum-cli-1.1.0/src/chksum_cli/launcher.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:08:56.878254 chksum-cli-1.1.0/src/chksum_cli.egg-info/
+-rw-rw-rw-   0        0        0     3440 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      381 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       49 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       32 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 20:08:56.000000 chksum-cli-1.1.0/src/chksum_cli.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 20:08:56.879755 chksum-cli-1.1.0/test/
+-rw-rw-rw-   0        0        0     2856 2022-12-13 19:51:32.000000 chksum-cli-1.1.0/test/test.py
```

### Comparing `chksum-cli-1.0.0/LICENSE` & `chksum-cli-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `chksum-cli-1.0.0/PKG-INFO` & `chksum-cli-1.1.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chksum-cli
-Version: 1.0.0
+Version: 1.1.0
 Summary: Compare checksums from the command line
 Author: espehon
 Project-URL: Homepage, https://github.com/espehon/chksum-cli
 Project-URL: Bug Tracker, https://github.com/espehon/chksum-cli/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
@@ -28,14 +28,24 @@
 # Install
 Requires Python >= 3.10
 ```
 pip install chksum-cli
 ```
 
 
+# Features
+- User friendly non-specific argument order
+- Visual feedback comparing hashes
+- Exit code matches hash results
+- Can ignore dot files
+- Interactive mode
+- Hash only function
+- Can use md5, sha1, sha256, and sha512
+
+
 # Usage
 ```
 CHKSUM [-?] [-i] [-d] position1 position2 [position3]
 
 Calculate and compare the checksums of files or directories.
 Can also compare against pasted strings.
 ALGORITHMS = ['md5', 'sha1', 'sha256', 'sha512']
@@ -47,16 +57,17 @@
 
 options:
   -?, --help         Show this help message and exit.
   -i, --interactive  Run in interactive mode.
   -d, --dots         Ignore '.' (dot) files from directories.
 
 If the first 2 positional arguments are strings, the algorithm is not needed. Default is md5.
+Likewise, passing only a single path will simply out the digest.
 ```
-Arguments can be passed in any order. [[note](#issues)]\
+Arguments can be passed in any order. [Note: [This issue](#issues)]\
 E.g. the following are equivalent:\
 `chksum <PathToFile> <PathToDir> sha256 -d`\
 `chksum -d <PathToDir> sha256 <PathToFile>`
 
 
 # Interactive mode
 Use `-i` to enter the interactive mode where arguments can be passed one at a time.\
@@ -92,15 +103,15 @@
 59198d6aad1674a0b372027ce275a9b6
 59198d6aad1674a0b372027ce275a9b6
 √ Hashes Match
 ```
 
 
 # <a name="issues"></a>Issues
-Using `-d` in between second and third positional causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Using `-d` in between positionals can causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
 Example:\
         `$ chksum ./file ./file -d sha1`
 
 
 # Author
 
 - [@espehon](https://www.github.com/espehon)
```

#### html2text {}

```diff
@@ -1,38 +1,42 @@
-Metadata-Version: 2.1 Name: chksum-cli Version: 1.0.0 Summary: Compare
+Metadata-Version: 2.1 Name: chksum-cli Version: 1.1.0 Summary: Compare
 checksums from the command line Author: espehon Project-URL: Homepage, https://
 github.com/espehon/chksum-cli Project-URL: Bug Tracker, https://github.com/
 espehon/chksum-cli/issues Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 5 - Production/Stable Classifier: Environment
 :: Console Classifier: License :: OSI Approved :: GNU General Public License v3
 (GPLv3) Classifier: Operating System :: OS Independent Classifier: Topic ::
 Utilities Requires-Python: >=3.10 Description-Content-Type: text/markdown
 License-File: LICENSE
     [https://raw.githubusercontent.com/espehon/chksum-cli/main/docs/images/
                                    Demo.png]
 # chksum CLI for comparing two checksums # Install Requires Python >= 3.10 ```
-pip install chksum-cli ``` # Usage ``` CHKSUM [-?] [-i] [-d] position1
-position2 [position3] Calculate and compare the checksums of files or
-directories. Can also compare against pasted strings. ALGORITHMS = ['md5',
-'sha1', 'sha256', 'sha512'] positional arguments: position1 Checksum, file, or
-algorithm position2 Checksum, file, or algorithm position3 Checksum, file, or
-algorithm options: -?, --help Show this help message and exit. -i, --
-interactive Run in interactive mode. -d, --dots Ignore '.' (dot) files from
-directories. If the first 2 positional arguments are strings, the algorithm is
-not needed. Default is md5. ``` Arguments can be passed in any order. [[note]
-(#issues)]\ E.g. the following are equivalent:\ `chksum   sha256 -d`\ `chksum -
-d  sha256 ` # Interactive mode Use `-i` to enter the interactive mode where
-arguments can be passed one at a time.\ Note that `-i` is mutually exclusive.
-``` $ chksum -i _ _ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ /
-__| | | | '_ ` _ \ | (__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/
-\__,_|_| |_| |_| Copyright (c) 2022, espehon All rights reserved. ALGORITHMS =
-['md5', 'sha1', 'sha256', 'sha512'] Enter Algorithm or path to File or
-Directory > ``` Inputs are checked after each entry and the prompt is updated
-accordingly ``` Enter Algorithm or path to File or Directory > ./ Directory
-entered. Enter Algorithm or path to File or Directory > ./ Directory entered.
-Enter Algorithm > md5 Algorithm entered. Do you want to include '.' (dot)
-files? [Y/n] > n include_dots = False -------------[MD5]-------------
+pip install chksum-cli ``` # Features - User friendly non-specific argument
+order - Visual feedback comparing hashes - Exit code matches hash results - Can
+ignore dot files - Interactive mode - Hash only function - Can use md5, sha1,
+sha256, and sha512 # Usage ``` CHKSUM [-?] [-i] [-d] position1 position2
+[position3] Calculate and compare the checksums of files or directories. Can
+also compare against pasted strings. ALGORITHMS = ['md5', 'sha1', 'sha256',
+'sha512'] positional arguments: position1 Checksum, file, or algorithm
+position2 Checksum, file, or algorithm position3 Checksum, file, or algorithm
+options: -?, --help Show this help message and exit. -i, --interactive Run in
+interactive mode. -d, --dots Ignore '.' (dot) files from directories. If the
+first 2 positional arguments are strings, the algorithm is not needed. Default
+is md5. Likewise, passing only a single path will simply out the digest. ```
+Arguments can be passed in any order. [Note: [This issue](#issues)]\ E.g. the
+following are equivalent:\ `chksum   sha256 -d`\ `chksum -d  sha256 ` #
+Interactive mode Use `-i` to enter the interactive mode where arguments can be
+passed one at a time.\ Note that `-i` is mutually exclusive. ``` $ chksum -i _
+_ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ / __| | | | '_ ` _ \ |
+(__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/\__,_|_| |_| |_|
+Copyright (c) 2022, espehon All rights reserved. ALGORITHMS = ['md5', 'sha1',
+'sha256', 'sha512'] Enter Algorithm or path to File or Directory > ``` Inputs
+are checked after each entry and the prompt is updated accordingly ``` Enter
+Algorithm or path to File or Directory > ./ Directory entered. Enter Algorithm
+or path to File or Directory > ./ Directory entered. Enter Algorithm > md5
+Algorithm entered. Do you want to include '.' (dot) files? [Y/n] > n
+include_dots = False -------------[MD5]-------------
 - 59198d6aad1674a0b372027ce275a9b6 59198d6aad1674a0b372027ce275a9b6 â Hashes
-Match ``` # Issues Using `-d` in between second and third positional causes an
-argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/
-11))\ Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
+Match ``` # Issues Using `-d` in between positionals can causes an argparse
+error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
 www.github.com/espehon)
```

### Comparing `chksum-cli-1.0.0/README.md` & `chksum-cli-1.1.0/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -11,14 +11,24 @@
 # Install
 Requires Python >= 3.10
 ```
 pip install chksum-cli
 ```
 
 
+# Features
+- User friendly non-specific argument order
+- Visual feedback comparing hashes
+- Exit code matches hash results
+- Can ignore dot files
+- Interactive mode
+- Hash only function
+- Can use md5, sha1, sha256, and sha512
+
+
 # Usage
 ```
 CHKSUM [-?] [-i] [-d] position1 position2 [position3]
 
 Calculate and compare the checksums of files or directories.
 Can also compare against pasted strings.
 ALGORITHMS = ['md5', 'sha1', 'sha256', 'sha512']
@@ -30,16 +40,17 @@
 
 options:
   -?, --help         Show this help message and exit.
   -i, --interactive  Run in interactive mode.
   -d, --dots         Ignore '.' (dot) files from directories.
 
 If the first 2 positional arguments are strings, the algorithm is not needed. Default is md5.
+Likewise, passing only a single path will simply out the digest.
 ```
-Arguments can be passed in any order. [[note](#issues)]\
+Arguments can be passed in any order. [Note: [This issue](#issues)]\
 E.g. the following are equivalent:\
 `chksum <PathToFile> <PathToDir> sha256 -d`\
 `chksum -d <PathToDir> sha256 <PathToFile>`
 
 
 # Interactive mode
 Use `-i` to enter the interactive mode where arguments can be passed one at a time.\
@@ -75,15 +86,15 @@
 59198d6aad1674a0b372027ce275a9b6
 59198d6aad1674a0b372027ce275a9b6
 √ Hashes Match
 ```
 
 
 # <a name="issues"></a>Issues
-Using `-d` in between second and third positional causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Using `-d` in between positionals can causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
 Example:\
         `$ chksum ./file ./file -d sha1`
 
 
 # Author
 
 - [@espehon](https://www.github.com/espehon)
```

#### html2text {}

```diff
@@ -1,29 +1,33 @@
     [https://raw.githubusercontent.com/espehon/chksum-cli/main/docs/images/
                                    Demo.png]
 # chksum CLI for comparing two checksums # Install Requires Python >= 3.10 ```
-pip install chksum-cli ``` # Usage ``` CHKSUM [-?] [-i] [-d] position1
-position2 [position3] Calculate and compare the checksums of files or
-directories. Can also compare against pasted strings. ALGORITHMS = ['md5',
-'sha1', 'sha256', 'sha512'] positional arguments: position1 Checksum, file, or
-algorithm position2 Checksum, file, or algorithm position3 Checksum, file, or
-algorithm options: -?, --help Show this help message and exit. -i, --
-interactive Run in interactive mode. -d, --dots Ignore '.' (dot) files from
-directories. If the first 2 positional arguments are strings, the algorithm is
-not needed. Default is md5. ``` Arguments can be passed in any order. [[note]
-(#issues)]\ E.g. the following are equivalent:\ `chksum   sha256 -d`\ `chksum -
-d  sha256 ` # Interactive mode Use `-i` to enter the interactive mode where
-arguments can be passed one at a time.\ Note that `-i` is mutually exclusive.
-``` $ chksum -i _ _ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ /
-__| | | | '_ ` _ \ | (__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/
-\__,_|_| |_| |_| Copyright (c) 2022, espehon All rights reserved. ALGORITHMS =
-['md5', 'sha1', 'sha256', 'sha512'] Enter Algorithm or path to File or
-Directory > ``` Inputs are checked after each entry and the prompt is updated
-accordingly ``` Enter Algorithm or path to File or Directory > ./ Directory
-entered. Enter Algorithm or path to File or Directory > ./ Directory entered.
-Enter Algorithm > md5 Algorithm entered. Do you want to include '.' (dot)
-files? [Y/n] > n include_dots = False -------------[MD5]-------------
+pip install chksum-cli ``` # Features - User friendly non-specific argument
+order - Visual feedback comparing hashes - Exit code matches hash results - Can
+ignore dot files - Interactive mode - Hash only function - Can use md5, sha1,
+sha256, and sha512 # Usage ``` CHKSUM [-?] [-i] [-d] position1 position2
+[position3] Calculate and compare the checksums of files or directories. Can
+also compare against pasted strings. ALGORITHMS = ['md5', 'sha1', 'sha256',
+'sha512'] positional arguments: position1 Checksum, file, or algorithm
+position2 Checksum, file, or algorithm position3 Checksum, file, or algorithm
+options: -?, --help Show this help message and exit. -i, --interactive Run in
+interactive mode. -d, --dots Ignore '.' (dot) files from directories. If the
+first 2 positional arguments are strings, the algorithm is not needed. Default
+is md5. Likewise, passing only a single path will simply out the digest. ```
+Arguments can be passed in any order. [Note: [This issue](#issues)]\ E.g. the
+following are equivalent:\ `chksum   sha256 -d`\ `chksum -d  sha256 ` #
+Interactive mode Use `-i` to enter the interactive mode where arguments can be
+passed one at a time.\ Note that `-i` is mutually exclusive. ``` $ chksum -i _
+_ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ / __| | | | '_ ` _ \ |
+(__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/\__,_|_| |_| |_|
+Copyright (c) 2022, espehon All rights reserved. ALGORITHMS = ['md5', 'sha1',
+'sha256', 'sha512'] Enter Algorithm or path to File or Directory > ``` Inputs
+are checked after each entry and the prompt is updated accordingly ``` Enter
+Algorithm or path to File or Directory > ./ Directory entered. Enter Algorithm
+or path to File or Directory > ./ Directory entered. Enter Algorithm > md5
+Algorithm entered. Do you want to include '.' (dot) files? [Y/n] > n
+include_dots = False -------------[MD5]-------------
 - 59198d6aad1674a0b372027ce275a9b6 59198d6aad1674a0b372027ce275a9b6 â Hashes
-Match ``` # Issues Using `-d` in between second and third positional causes an
-argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/
-11))\ Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
+Match ``` # Issues Using `-d` in between positionals can causes an argparse
+error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
 www.github.com/espehon)
```

### Comparing `chksum-cli-1.0.0/pyproject.toml` & `chksum-cli-1.1.0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "chksum-cli"
-version = "1.0.0"
+version = "1.1.0"
 authors = [
     { name="espehon"},
 ]
 description = "Compare checksums from the command line"
 readme = "README.md"
 requires-python = ">=3.10"
 dependencies = [
```

### Comparing `chksum-cli-1.0.0/src/chksum_cli/chksum.py` & `chksum-cli-1.1.0/src/chksum_cli/chksum.py`

 * *Files 14% similar despite different names*

```diff
@@ -29,19 +29,26 @@
 CHKSUM_LICENSE = """  Copyright (c) 2022, espehon\n  License: https://www.gnu.org/licenses/gpl-3.0.html"""
 
 ALGORITHMS = ['md5', 'sha1', 'sha256', 'sha512']
 
 positionals = {}    # for storing positionals their type
 method = 'md5'      # algorithm to be used. Currently set as default (not a constant)
 
+interactive_colors = {      # colors used in the interactive mode
+                'prompt': Fore.LIGHTBLUE_EX,
+                'output': Fore.BLUE,
+                'input': Fore.LIGHTWHITE_EX,
+                'warn': Fore.LIGHTYELLOW_EX
+            }
+
 parser = argparse.ArgumentParser(
     prog="CHKSUM",
     description = (f"Calculate and compare the checksums of files or directories.\nCan also compare against pasted strings. \n{ALGORITHMS = }"),
     formatter_class=argparse.RawDescriptionHelpFormatter,
-    epilog = (f"If the first 2 positional arguments are strings, the algorithm is not needed. Default is {method}.\n\tExample 1: chksum ./file1 ./file2 sha512\n\tExample 2: chksum 123456789ABCDEF 123456789ABCDEF\n\tExample 3: chksum ./dir 123456789ABCDEF"),
+    epilog = (f"If the first 2 positional arguments are strings, the algorithm is not needed. Default is {method}.\n\tExample 1: chksum ./file1 ./file2 sha512\n\tExample 2: chksum 123456789ABCDEF 123456789ABCDEF\n\tExample 3: chksum ./dir 123456789ABCDEF\nLikewise, passing only a single path will simply out the digest."),
     add_help = False # free -h from help (-? will be used as help flag)
 )
 parser.add_argument('-?',
                     '--help',
                     action='help',
                     help="Show this help message and exit."     # make -? help
 )
@@ -64,14 +71,15 @@
 )
 parser.add_argument('position1',
                     type=str,
                     help="Checksum, file, or algorithm"
 )
 parser.add_argument('position2',
                     type=str,
+                    nargs='?',
                     help="Checksum, file, or algorithm"
 )
 parser.add_argument('position3',
                     type=str,
                     nargs='?',
                     help="Checksum, file, or algorithm"
 )
@@ -180,30 +188,45 @@
     if hash_1 == hash_2:    # output the final result
         print(Fore.LIGHTGREEN_EX + "√ Hashes Match\n")
         return True
     else:
         print(Fore.LIGHTRED_EX + "X Hashes Do Not Match\n")
         return False
 
+def output_single_hash(path: str, is_directory: bool=False):
+    hash = get_hash(path, is_directory)
+    title = str.upper("[" + method + "]").center(len(hash), '-')
+    print(title)
+    print(hash)
+
 
 def cli(argv=None):
-    """Processes the command line arguments and outputs accordingly.
-    This is the main logic for the program when ran as one line (not in interactive mode)"""
+    """
+    Processes the command line arguments and outputs accordingly.
+    This is the main logic for the program when ran as one line (not in interactive mode)
+    """
+    
     global method
     global args
     args = parser.parse_args(argv)              # get args from input
 
     process_positional(args.position1, 1)   # store positional accordingly
-    process_positional(args.position2, 2)   # store positional accordingly
+
     try:
+        process_positional(args.position2, 2)    # store positional accordingly (optional if user wants to know a hash)
         process_positional(args.position3, 3)    # store optional 3rd positional
     except TypeError:
-        # There was no third positional
+        # There was no third positional and maybe no 2nd
         pass
-    if len(positionals) < 2:    # must have at least 2 positionals
+
+    if len(positionals) < 2:    # check if single hash mode or possible missing args
+        for position in positionals:
+            if positionals[position]['type'] == 'file' or positionals[position]['type'] == 'dir':
+                output_single_hash(positionals[position]['value'], positionals[position]['type'] == 'dir')
+                return 0
         return "Missing positional argument..."
 
     hashes = []                 # stores the final hashes for output
     iteration = 1               # tracks iteration and doubles as a dictionary key
     hashes_were_prepared = True   # is set to False if this script runs the hash.
     try:
         while len(hashes) < 2 and iteration <= 3:
@@ -229,15 +252,16 @@
         method = 'Strings'
     if compare_hashes(hashes[0], hashes[1], method): # test, format, and output hashes
         return 0
     return 1
     
 
 def stand_alone(single_run=False):
-    """ Interactive mode
+    """ 
+    Interactive mode
     This is the standalone version.
     Logic works as follows:
         1. Get 1 of 3 options from user
         2. Determine which option was given
         3. Ask for 1 of 2 remaining options
         4. Determine which option was given
         5. Ask for final option
@@ -256,77 +280,78 @@
   ___| |__ | | _____ _   _ _ __ ___  
  / __| '_ \| |/ / __| | | | '_ ` _ \ 
 | (__| | | |   <\__ \ |_| | | | | | |
  \___|_| |_|_|\_\___/\__,_|_| |_| |_|"""
 
     while program_is_running:
         try:
-            print(f"{Fore.LIGHTBLUE_EX}{TITLE}")
-            print(f"{Fore.LIGHTBLUE_EX}{next(license_generator)}")
-            print(f"{Fore.LIGHTBLUE_EX}\n{ALGORITHMS = }")
-            print(f"{Fore.LIGHTBLUE_EX}Called at " + CWD + "\n")
+            print(f"{interactive_colors['output']}{TITLE}")
+            print(f"{interactive_colors['output']}{next(license_generator)}")
+            print(f"{interactive_colors['output']}\n{ALGORITHMS = }")
+            print(f"{interactive_colors['output']}Called at " + CWD + "\n")
 
             method = None
             hash_1 = None
             hash_2 = None
 
             include_dots = None
             tries = 3
             hash_strings = 0
+            
 
             while method is None or hash_1 is None or hash_2 is None:
                 match [method, hash_1, hash_2]:
                     case [a, b, c] if a is None and (b is None or c is None):
-                        user = input(Fore.LIGHTBLUE_EX + "Enter Algorithm or Path to File or Directory > " + Fore.RESET)
+                        user = input(interactive_colors['prompt'] + "Enter Algorithm or Path to File or Directory > " + interactive_colors['input'])
                     case [a, b, c] if a is not None and (b is None or c is None):
-                        user = input(Fore.LIGHTBLUE_EX + "Enter Path to File or Directory > " + Fore.RESET)
+                        user = input(interactive_colors['prompt'] + "Enter Path to File or Directory > " + interactive_colors['input'])
                     case [a, b, c] if a is None and not (b is None or c is None):
-                        user = input(Fore.LIGHTBLUE_EX + "Enter Algorithm > " + Fore.RESET)
+                        user = input(interactive_colors['prompt'] + "Enter Algorithm > " + interactive_colors['input'])
 
                 if user.strip() == "":
                     tries -= 1
-                    print(f"\t{Fore.BLUE}Nothing was entered; please try again. ({Fore.LIGHTYELLOW_EX}{tries}{Fore.BLUE} tries remain)")
+                    print(f"\t{interactive_colors['output']}Nothing was entered; please try again. ({interactive_colors['warn']}{tries}{Fore.BLUE} tries remain)")
                 elif str.lower(user) in ALGORITHMS:
                     method = str.lower(user)
-                    print(Fore.BLUE + "\tAlgorithm entered.")
+                    print(interactive_colors['output'] + "\tAlgorithm entered.")
                 else:
                     if '~' in user:
                         user = get_full_path(user)
                     if os.path.isfile(user):
-                        print(Fore.BLUE + "\tFile entered.")
+                        print(interactive_colors['output'] + "\tFile entered.")
                     elif os.path.exists(user):
-                        print(Fore.BLUE + "\tDirectory entered.")
+                        print(interactive_colors['output'] + "\tDirectory entered.")
                     else:
-                        print(Fore.BLUE + "\tHash string entered.")
+                        print(interactive_colors['output'] + "\tHash string entered.")
                         if hash_1 is None or hash_2 is None:
                             hash_strings += 1
                     if hash_1 is None:
                         hash_1 = user
                     elif hash_2 is None:
                         hash_2 = user
                     else:
                         tries -= 1
-                        print(Fore.BLUE + f"\tYou've already supplied two hash objects. ({Fore.LIGHTYELLOW_EX}{tries}{Fore.BLUE} tries remain)")
+                        print(interactive_colors['output'] + f"\tYou've already supplied two hash objects. ({interactive_colors['warn']}{tries}{interactive_colors['output']} tries remain)")
                 if hash_strings >= 2:
                     method = "STRINGS" # no need for algorithm
                     break
                 if tries <= 0:
-                    print(Fore.LIGHTYELLOW_EX + "\tNumber of tries exceeded!")
+                    print(interactive_colors['warn'] + "\tNumber of tries exceeded!")
                     raise UserWarning
 
             for index, thing in enumerate([hash_1, hash_2]):
                 if os.path.isfile(thing):
                     if index == 0:
                         hash_1 = checksum.get_for_file(thing, hash_mode=method)
                     else:
                         hash_2 = checksum.get_for_file(thing, hash_mode=method)
                 elif os.path.exists(thing):
                     if include_dots is None:
-                        include_dots = str.lower(input(Fore.LIGHTBLUE_EX + "Do you want to include '.' (dot) files? [Y/n] > " + Fore.RESET)).strip() != 'n'
-                        print(Fore.BLUE + f"\t{include_dots = }")
+                        include_dots = str.lower(input(interactive_colors['prompt'] + "Do you want to include '.' (dot) files? [Y/n] > " + interactive_colors['input'])).strip() != 'n'
+                        print(interactive_colors['output'] + f"\t{include_dots = }")
                     if index == 0:
                         hash_1 = checksum.get_for_directory(thing, hash_mode=method,
                         filter_dots= not include_dots)
                     else:
                         hash_2 = checksum.get_for_directory(thing, hash_mode=method,
                         filter_dots= not include_dots)
                 else:
@@ -339,22 +364,22 @@
             if compare_hashes(hash_1, hash_2, method) and single_run: # test, format, and output
                 return 0    # if in single run mode, exit program with code 0
             elif single_run:
                 return 1    # if in single run mode, exit program with code 1
             # else (if not in single mode) continue though loop
 
         except KeyboardInterrupt:
-            print(Fore.LIGHTYELLOW_EX + "Keyboard Interrupt!")
+            print(interactive_colors['warn'] + "Keyboard Interrupt!")
         except UserWarning:
-            print(f"{Fore.BLUE}\tProgress stopped...")
+            print(interactive_colors['output'] + "\tProgress stopped...")
         except PermissionError:
-            print(Fore.LIGHTRED_EX + "Permission Denied.")
+            print(Fore.LIGHTRED_EX + "Permission Denied.")  # this should always be light red
 
         program_is_running = False
         if single_run is False:
             try:    # Incase the user mashes keyboard interrupt
-                user = str.lower(input(f"{Fore.LIGHTBLUE_EX}\nEnter R to rerun. Anything else will exit. > "))
+                user = str.lower(input(f"{interactive_colors['prompt']}\nEnter R to rerun. Anything else will exit. > "))
                 if user == 'r':
                     program_is_running = True
                     print('\n' * 3)
             except KeyboardInterrupt:
-                print(Fore.LIGHTYELLOW_EX + "Exiting program...")
+                print(interactive_colors['warn'] + "Exiting program...")
```

### Comparing `chksum-cli-1.0.0/src/chksum_cli.egg-info/PKG-INFO` & `chksum-cli-1.1.0/src/chksum_cli.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chksum-cli
-Version: 1.0.0
+Version: 1.1.0
 Summary: Compare checksums from the command line
 Author: espehon
 Project-URL: Homepage, https://github.com/espehon/chksum-cli
 Project-URL: Bug Tracker, https://github.com/espehon/chksum-cli/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
@@ -28,14 +28,24 @@
 # Install
 Requires Python >= 3.10
 ```
 pip install chksum-cli
 ```
 
 
+# Features
+- User friendly non-specific argument order
+- Visual feedback comparing hashes
+- Exit code matches hash results
+- Can ignore dot files
+- Interactive mode
+- Hash only function
+- Can use md5, sha1, sha256, and sha512
+
+
 # Usage
 ```
 CHKSUM [-?] [-i] [-d] position1 position2 [position3]
 
 Calculate and compare the checksums of files or directories.
 Can also compare against pasted strings.
 ALGORITHMS = ['md5', 'sha1', 'sha256', 'sha512']
@@ -47,16 +57,17 @@
 
 options:
   -?, --help         Show this help message and exit.
   -i, --interactive  Run in interactive mode.
   -d, --dots         Ignore '.' (dot) files from directories.
 
 If the first 2 positional arguments are strings, the algorithm is not needed. Default is md5.
+Likewise, passing only a single path will simply out the digest.
 ```
-Arguments can be passed in any order. [[note](#issues)]\
+Arguments can be passed in any order. [Note: [This issue](#issues)]\
 E.g. the following are equivalent:\
 `chksum <PathToFile> <PathToDir> sha256 -d`\
 `chksum -d <PathToDir> sha256 <PathToFile>`
 
 
 # Interactive mode
 Use `-i` to enter the interactive mode where arguments can be passed one at a time.\
@@ -92,15 +103,15 @@
 59198d6aad1674a0b372027ce275a9b6
 59198d6aad1674a0b372027ce275a9b6
 √ Hashes Match
 ```
 
 
 # <a name="issues"></a>Issues
-Using `-d` in between second and third positional causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Using `-d` in between positionals can causes an argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
 Example:\
         `$ chksum ./file ./file -d sha1`
 
 
 # Author
 
 - [@espehon](https://www.github.com/espehon)
```

#### html2text {}

```diff
@@ -1,38 +1,42 @@
-Metadata-Version: 2.1 Name: chksum-cli Version: 1.0.0 Summary: Compare
+Metadata-Version: 2.1 Name: chksum-cli Version: 1.1.0 Summary: Compare
 checksums from the command line Author: espehon Project-URL: Homepage, https://
 github.com/espehon/chksum-cli Project-URL: Bug Tracker, https://github.com/
 espehon/chksum-cli/issues Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 5 - Production/Stable Classifier: Environment
 :: Console Classifier: License :: OSI Approved :: GNU General Public License v3
 (GPLv3) Classifier: Operating System :: OS Independent Classifier: Topic ::
 Utilities Requires-Python: >=3.10 Description-Content-Type: text/markdown
 License-File: LICENSE
     [https://raw.githubusercontent.com/espehon/chksum-cli/main/docs/images/
                                    Demo.png]
 # chksum CLI for comparing two checksums # Install Requires Python >= 3.10 ```
-pip install chksum-cli ``` # Usage ``` CHKSUM [-?] [-i] [-d] position1
-position2 [position3] Calculate and compare the checksums of files or
-directories. Can also compare against pasted strings. ALGORITHMS = ['md5',
-'sha1', 'sha256', 'sha512'] positional arguments: position1 Checksum, file, or
-algorithm position2 Checksum, file, or algorithm position3 Checksum, file, or
-algorithm options: -?, --help Show this help message and exit. -i, --
-interactive Run in interactive mode. -d, --dots Ignore '.' (dot) files from
-directories. If the first 2 positional arguments are strings, the algorithm is
-not needed. Default is md5. ``` Arguments can be passed in any order. [[note]
-(#issues)]\ E.g. the following are equivalent:\ `chksum   sha256 -d`\ `chksum -
-d  sha256 ` # Interactive mode Use `-i` to enter the interactive mode where
-arguments can be passed one at a time.\ Note that `-i` is mutually exclusive.
-``` $ chksum -i _ _ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ /
-__| | | | '_ ` _ \ | (__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/
-\__,_|_| |_| |_| Copyright (c) 2022, espehon All rights reserved. ALGORITHMS =
-['md5', 'sha1', 'sha256', 'sha512'] Enter Algorithm or path to File or
-Directory > ``` Inputs are checked after each entry and the prompt is updated
-accordingly ``` Enter Algorithm or path to File or Directory > ./ Directory
-entered. Enter Algorithm or path to File or Directory > ./ Directory entered.
-Enter Algorithm > md5 Algorithm entered. Do you want to include '.' (dot)
-files? [Y/n] > n include_dots = False -------------[MD5]-------------
+pip install chksum-cli ``` # Features - User friendly non-specific argument
+order - Visual feedback comparing hashes - Exit code matches hash results - Can
+ignore dot files - Interactive mode - Hash only function - Can use md5, sha1,
+sha256, and sha512 # Usage ``` CHKSUM [-?] [-i] [-d] position1 position2
+[position3] Calculate and compare the checksums of files or directories. Can
+also compare against pasted strings. ALGORITHMS = ['md5', 'sha1', 'sha256',
+'sha512'] positional arguments: position1 Checksum, file, or algorithm
+position2 Checksum, file, or algorithm position3 Checksum, file, or algorithm
+options: -?, --help Show this help message and exit. -i, --interactive Run in
+interactive mode. -d, --dots Ignore '.' (dot) files from directories. If the
+first 2 positional arguments are strings, the algorithm is not needed. Default
+is md5. Likewise, passing only a single path will simply out the digest. ```
+Arguments can be passed in any order. [Note: [This issue](#issues)]\ E.g. the
+following are equivalent:\ `chksum   sha256 -d`\ `chksum -d  sha256 ` #
+Interactive mode Use `-i` to enter the interactive mode where arguments can be
+passed one at a time.\ Note that `-i` is mutually exclusive. ``` $ chksum -i _
+_ | | | | ___| |__ | | _____ _ _ _ __ ___ / __| '_ \| |/ / __| | | | '_ ` _ \ |
+(__| | | | <\__ \ |_| | | | | | | \___|_| |_|_|\_\___/\__,_|_| |_| |_|
+Copyright (c) 2022, espehon All rights reserved. ALGORITHMS = ['md5', 'sha1',
+'sha256', 'sha512'] Enter Algorithm or path to File or Directory > ``` Inputs
+are checked after each entry and the prompt is updated accordingly ``` Enter
+Algorithm or path to File or Directory > ./ Directory entered. Enter Algorithm
+or path to File or Directory > ./ Directory entered. Enter Algorithm > md5
+Algorithm entered. Do you want to include '.' (dot) files? [Y/n] > n
+include_dots = False -------------[MD5]-------------
 - 59198d6aad1674a0b372027ce275a9b6 59198d6aad1674a0b372027ce275a9b6 â Hashes
-Match ``` # Issues Using `-d` in between second and third positional causes an
-argparse error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/
-11))\ Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
+Match ``` # Issues Using `-d` in between positionals can causes an argparse
+error. (See Issue: [#11](https://github.com/espehon/chksum-cli/issues/11))\
+Example:\ `$ chksum ./file ./file -d sha1` # Author - [@espehon](https://
 www.github.com/espehon)
```

### Comparing `chksum-cli-1.0.0/test/test.py` & `chksum-cli-1.1.0/test/test.py`

 * *Files identical despite different names*

