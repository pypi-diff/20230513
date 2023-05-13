# Comparing `tmp/hangman-package-1.0.0.tar.gz` & `tmp/hangman-package-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hangman-package-1.0.0.tar", last modified: Sat May 13 19:36:10 2023, max compression
+gzip compressed data, was "hangman-package-1.0.1.tar", last modified: Sat May 13 19:52:09 2023, max compression
```

## Comparing `hangman-package-1.0.0.tar` & `hangman-package-1.0.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:10.105235 hangman-package-1.0.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-05-13 19:35:57.000000 hangman-package-1.0.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-05-13 19:36:10.105235 hangman-package-1.0.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1113 2023-05-13 19:35:57.000000 hangman-package-1.0.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:10.105235 hangman-package-1.0.0/hangman/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 19:35:57.000000 hangman-package-1.0.0/hangman/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 19:35:57.000000 hangman-package-1.0.0/hangman/drawings.py
--rw-r--r--   0 runner    (1001) docker     (123)     2146 2023-05-13 19:35:57.000000 hangman-package-1.0.0/hangman/hangman.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:10.105235 hangman-package-1.0.0/hangman_package.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-05-13 19:36:10.000000 hangman-package-1.0.0/hangman_package.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      269 2023-05-13 19:36:10.000000 hangman-package-1.0.0/hangman_package.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 19:36:10.000000 hangman-package-1.0.0/hangman_package.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 19:36:10.000000 hangman-package-1.0.0/hangman_package.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 19:35:57.000000 hangman-package-1.0.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 19:36:10.105235 hangman-package-1.0.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:10.105235 hangman-package-1.0.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      848 2023-05-13 19:35:57.000000 hangman-package-1.0.0/tests/test_hangman.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:52:09.028981 hangman-package-1.0.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-05-13 19:51:55.000000 hangman-package-1.0.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-05-13 19:52:09.028981 hangman-package-1.0.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1129 2023-05-13 19:51:55.000000 hangman-package-1.0.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:52:09.028981 hangman-package-1.0.1/hangman/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 19:51:55.000000 hangman-package-1.0.1/hangman/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 19:51:55.000000 hangman-package-1.0.1/hangman/drawings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2146 2023-05-13 19:51:55.000000 hangman-package-1.0.1/hangman/hangman.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:52:09.028981 hangman-package-1.0.1/hangman_package.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-05-13 19:52:09.000000 hangman-package-1.0.1/hangman_package.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      269 2023-05-13 19:52:09.000000 hangman-package-1.0.1/hangman_package.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 19:52:09.000000 hangman-package-1.0.1/hangman_package.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 19:52:09.000000 hangman-package-1.0.1/hangman_package.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 19:51:55.000000 hangman-package-1.0.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 19:52:09.028981 hangman-package-1.0.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:52:09.028981 hangman-package-1.0.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      848 2023-05-13 19:51:55.000000 hangman-package-1.0.1/tests/test_hangman.py
```

### Comparing `hangman-package-1.0.0/LICENSE` & `hangman-package-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `hangman-package-1.0.0/PKG-INFO` & `hangman-package-1.0.1/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hangman-package
-Version: 1.0.0
+Version: 1.0.1
 Summary: A package to play a custom hangman game
 Author-email: Vinicius Koji Enari <viniciusenari@gmail.com>
 Project-URL: Homepage, https://github.com/viniciusenari/hangman-package
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
@@ -16,15 +16,15 @@
 The Hangman package is a Python implementation of the classic game, Hangman. It allows users to play the game by guessing letters to complete a hidden word.
 
 ## Installation
 
 The package can be installed using pip:
 
 ```bash
-pip install hangman
+pip install hangman-package
 ```
 
 ## Usage
 
 The package can be used in the following way:
 
 ```python
@@ -37,14 +37,14 @@
 hangman.play()
 ```
 
 When `play()` is called, the game will begin and the user will be prompted to guess letters to complete the hidden word. The game ends when the user either completes the word or runs out of guesses.
 
 ## Contributing
 
-Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/your-username/hangman).
+Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/viniciusenari/hangman-package).
 
 If you would like to contribute to the package, please fork the repository and submit a pull request with your changes.
 
 ## License
 
 The Hangman package is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
```

### Comparing `hangman-package-1.0.0/README.md` & `hangman-package-1.0.1/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 The Hangman package is a Python implementation of the classic game, Hangman. It allows users to play the game by guessing letters to complete a hidden word.
 
 ## Installation
 
 The package can be installed using pip:
 
 ```bash
-pip install hangman
+pip install hangman-package
 ```
 
 ## Usage
 
 The package can be used in the following way:
 
 ```python
@@ -24,14 +24,14 @@
 hangman.play()
 ```
 
 When `play()` is called, the game will begin and the user will be prompted to guess letters to complete the hidden word. The game ends when the user either completes the word or runs out of guesses.
 
 ## Contributing
 
-Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/your-username/hangman).
+Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/viniciusenari/hangman-package).
 
 If you would like to contribute to the package, please fork the repository and submit a pull request with your changes.
 
 ## License
 
 The Hangman package is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
```

### Comparing `hangman-package-1.0.0/hangman/drawings.py` & `hangman-package-1.0.1/hangman/drawings.py`

 * *Files identical despite different names*

### Comparing `hangman-package-1.0.0/hangman/hangman.py` & `hangman-package-1.0.1/hangman/hangman.py`

 * *Files identical despite different names*

### Comparing `hangman-package-1.0.0/hangman_package.egg-info/PKG-INFO` & `hangman-package-1.0.1/hangman_package.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hangman-package
-Version: 1.0.0
+Version: 1.0.1
 Summary: A package to play a custom hangman game
 Author-email: Vinicius Koji Enari <viniciusenari@gmail.com>
 Project-URL: Homepage, https://github.com/viniciusenari/hangman-package
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
@@ -16,15 +16,15 @@
 The Hangman package is a Python implementation of the classic game, Hangman. It allows users to play the game by guessing letters to complete a hidden word.
 
 ## Installation
 
 The package can be installed using pip:
 
 ```bash
-pip install hangman
+pip install hangman-package
 ```
 
 ## Usage
 
 The package can be used in the following way:
 
 ```python
@@ -37,14 +37,14 @@
 hangman.play()
 ```
 
 When `play()` is called, the game will begin and the user will be prompted to guess letters to complete the hidden word. The game ends when the user either completes the word or runs out of guesses.
 
 ## Contributing
 
-Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/your-username/hangman).
+Contributions to the Hangman package are welcome! If you encounter a bug or have a feature request, please open an issue on the [GitHub repository](https://github.com/viniciusenari/hangman-package).
 
 If you would like to contribute to the package, please fork the repository and submit a pull request with your changes.
 
 ## License
 
 The Hangman package is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
```

### Comparing `hangman-package-1.0.0/pyproject.toml` & `hangman-package-1.0.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "hangman-package"
-version = "1.0.0"
+version = "1.0.1"
 authors = [
   { name="Vinicius Koji Enari", email="viniciusenari@gmail.com" },
 ]
 description = "A package to play a custom hangman game"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `hangman-package-1.0.0/tests/test_hangman.py` & `hangman-package-1.0.1/tests/test_hangman.py`

 * *Files identical despite different names*

