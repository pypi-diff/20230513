# Comparing `tmp/gsheet-player-0.0.16.tar.gz` & `tmp/gsheet-player-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gsheet-player-0.0.16.tar", last modified: Fri May 12 20:30:09 2023, max compression
+gzip compressed data, was "gsheet-player-0.2.0.tar", last modified: Fri May 12 22:34:10 2023, max compression
```

## Comparing `gsheet-player-0.0.16.tar` & `gsheet-player-0.2.0.tar`

### file list

```diff
@@ -1,22 +1,21 @@
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 20:30:09.598143 gsheet-player-0.0.16/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1488 2023-05-12 20:30:09.597999 gsheet-player-0.0.16/PKG-INFO
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1065 2023-05-12 20:29:10.000000 gsheet-player-0.0.16/README.md
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1694 2023-05-12 20:29:39.000000 gsheet-player-0.0.16/pyproject.toml
--rw-r--r--   0 gregshepherd   (501) staff       (20)       38 2023-05-12 20:30:09.598187 gsheet-player-0.0.16/setup.cfg
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 20:30:09.596070 gsheet-player-0.0.16/src/
--rw-r--r--   0 gregshepherd   (501) staff       (20)        0 2023-05-07 17:09:23.000000 gsheet-player-0.0.16/src/__init__.py
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 20:30:09.596666 gsheet-player-0.0.16/src/gsheet_player/
--rw-r--r--   0 gregshepherd   (501) staff       (20)       23 2023-05-12 20:29:39.000000 gsheet-player-0.0.16/src/gsheet_player/__init__.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     2327 2023-05-12 20:21:15.000000 gsheet-player-0.0.16/src/gsheet_player/file_ops.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     8445 2023-05-12 20:21:15.000000 gsheet-player-0.0.16/src/gsheet_player/gsheetPlayer.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     6913 2023-05-12 20:21:15.000000 gsheet-player-0.0.16/src/gsheet_player/gsheet_ops.py
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 20:30:09.597534 gsheet-player-0.0.16/src/gsheet_player.egg-info/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1488 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/PKG-INFO
--rw-r--r--   0 gregshepherd   (501) staff       (20)      464 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/SOURCES.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)        1 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/dependency_links.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)       55 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/entry_points.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)       65 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/requires.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)       23 2023-05-12 20:30:09.000000 gsheet-player-0.0.16/src/gsheet_player.egg-info/top_level.txt
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 20:30:09.597820 gsheet-player-0.0.16/tests/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     2029 2023-05-12 20:23:17.000000 gsheet-player-0.0.16/tests/test_file_ops.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1481 2023-05-12 19:51:25.000000 gsheet-player-0.0.16/tests/test_gsheetPlayer.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.816333 gsheet-player-0.2.0/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-12 22:34:10.816134 gsheet-player-0.2.0/PKG-INFO
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1065 2023-05-12 20:29:10.000000 gsheet-player-0.2.0/README.md
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1561 2023-05-12 22:34:06.000000 gsheet-player-0.2.0/pyproject.toml
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       38 2023-05-12 22:34:10.816404 gsheet-player-0.2.0/setup.cfg
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.813164 gsheet-player-0.2.0/src/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)        0 2023-05-07 17:09:23.000000 gsheet-player-0.2.0/src/__init__.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.814287 gsheet-player-0.2.0/src/gsheet_player/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       22 2023-05-12 22:34:06.000000 gsheet-player-0.2.0/src/gsheet_player/__init__.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     2327 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/file_ops.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     8445 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/gsheetPlayer.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     6913 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/gsheet_ops.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.815311 gsheet-player-0.2.0/src/gsheet_player.egg-info/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/PKG-INFO
+-rw-r--r--   0 gregshepherd   (501) staff       (20)      420 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/SOURCES.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)        1 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/dependency_links.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       65 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/requires.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       23 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/top_level.txt
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.815666 gsheet-player-0.2.0/tests/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     2029 2023-05-12 20:23:17.000000 gsheet-player-0.2.0/tests/test_file_ops.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1481 2023-05-12 19:51:25.000000 gsheet-player-0.2.0/tests/test_gsheetPlayer.py
```

### Comparing `gsheet-player-0.0.16/PKG-INFO` & `gsheet-player-0.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gsheet-player
-Version: 0.0.16
+Version: 0.2.0
 Summary: Data class to hold a player information from a spreadsheet row
 Author-email: shepworld <info@shepworld.com>
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
```

### Comparing `gsheet-player-0.0.16/README.md` & `gsheet-player-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.0.16/pyproject.toml` & `gsheet-player-0.2.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -4,53 +4,49 @@
 
 [project]
 name = "gsheet-player"
 description = "Data class to hold a player information from a spreadsheet row"
 authors = [{ name = "shepworld", email = "info@shepworld.com" }]
 license = { file = "LICENSE" }
 readme = "README.md"
-version = "0.0.16"
+version = "0.2.0"
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3",
 ]
 dependencies = []
 requires-python = ">=3.9"
 
     [project.optional-dependencies]
     build   = ["build", "twine"]
     dev     = ["black", "bumpver", "isort", "mypy", "pytest", "ruff"]
 
-    [project.scripts]
-    gsheet = "gsheet_player.__main__:main"
-
 [bumpver]
 current_version = "2023.1001-alpha"
 version_pattern = "YYYY.BUILD[-TAG]"
 commit_message = "bump version {old_version} -> {new_version}"
 commit = true
 tag = true
 push = true
 
 [tool.bumpver]
-current_version = "0.0.16"
+current_version = "0.2.0"
 version_pattern = "MAJOR.MINOR.PATCH"
 commit_message  = "bump version {old_version} -> {new_version}"
 commit          = true
 tag             = true
 push            = false
 
 [tool.bumpver.file_patterns]
 "pyproject.toml" = [
     'current_version = "{version}"',
     'version = "{version}"',
 ]
 "src/gsheet_player/__init__.py" = ["{version}"]
-"src/gsheet_player/__main__.py" = ["- gsheet_player v{version}"]
 
 [tool.isort]
 profile                   = "black"
 import_heading_stdlib     = "Standard library imports"
 import_heading_thirdparty = "Third party imports"
 import_heading_firstparty = "gsheet_player imports"
```

### Comparing `gsheet-player-0.0.16/src/gsheet_player/file_ops.py` & `gsheet-player-0.2.0/src/gsheet_player/file_ops.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.0.16/src/gsheet_player/gsheetPlayer.py` & `gsheet-player-0.2.0/src/gsheet_player/gsheetPlayer.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.0.16/src/gsheet_player/gsheet_ops.py` & `gsheet-player-0.2.0/src/gsheet_player/gsheet_ops.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.0.16/src/gsheet_player.egg-info/PKG-INFO` & `gsheet-player-0.2.0/src/gsheet_player.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gsheet-player
-Version: 0.0.16
+Version: 0.2.0
 Summary: Data class to hold a player information from a spreadsheet row
 Author-email: shepworld <info@shepworld.com>
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
```

### Comparing `gsheet-player-0.0.16/tests/test_file_ops.py` & `gsheet-player-0.2.0/tests/test_file_ops.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.0.16/tests/test_gsheetPlayer.py` & `gsheet-player-0.2.0/tests/test_gsheetPlayer.py`

 * *Files identical despite different names*

