# Comparing `tmp/gsheet-player-0.2.0.tar.gz` & `tmp/gsheet-player-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gsheet-player-0.2.0.tar", last modified: Fri May 12 22:34:10 2023, max compression
+gzip compressed data, was "gsheet-player-0.2.1.tar", last modified: Sat May 13 02:42:51 2023, max compression
```

## Comparing `gsheet-player-0.2.0.tar` & `gsheet-player-0.2.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.816333 gsheet-player-0.2.0/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-12 22:34:10.816134 gsheet-player-0.2.0/PKG-INFO
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1065 2023-05-12 20:29:10.000000 gsheet-player-0.2.0/README.md
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1561 2023-05-12 22:34:06.000000 gsheet-player-0.2.0/pyproject.toml
--rw-r--r--   0 gregshepherd   (501) staff       (20)       38 2023-05-12 22:34:10.816404 gsheet-player-0.2.0/setup.cfg
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.813164 gsheet-player-0.2.0/src/
--rw-r--r--   0 gregshepherd   (501) staff       (20)        0 2023-05-07 17:09:23.000000 gsheet-player-0.2.0/src/__init__.py
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.814287 gsheet-player-0.2.0/src/gsheet_player/
--rw-r--r--   0 gregshepherd   (501) staff       (20)       22 2023-05-12 22:34:06.000000 gsheet-player-0.2.0/src/gsheet_player/__init__.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     2327 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/file_ops.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     8445 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/gsheetPlayer.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     6913 2023-05-12 20:21:15.000000 gsheet-player-0.2.0/src/gsheet_player/gsheet_ops.py
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.815311 gsheet-player-0.2.0/src/gsheet_player.egg-info/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/PKG-INFO
--rw-r--r--   0 gregshepherd   (501) staff       (20)      420 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/SOURCES.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)        1 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/dependency_links.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)       65 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/requires.txt
--rw-r--r--   0 gregshepherd   (501) staff       (20)       23 2023-05-12 22:34:10.000000 gsheet-player-0.2.0/src/gsheet_player.egg-info/top_level.txt
-drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-12 22:34:10.815666 gsheet-player-0.2.0/tests/
--rw-r--r--   0 gregshepherd   (501) staff       (20)     2029 2023-05-12 20:23:17.000000 gsheet-player-0.2.0/tests/test_file_ops.py
--rw-r--r--   0 gregshepherd   (501) staff       (20)     1481 2023-05-12 19:51:25.000000 gsheet-player-0.2.0/tests/test_gsheetPlayer.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-13 02:42:51.571352 gsheet-player-0.2.1/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-13 02:42:51.571220 gsheet-player-0.2.1/PKG-INFO
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1065 2023-05-12 20:29:10.000000 gsheet-player-0.2.1/README.md
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1561 2023-05-13 02:42:47.000000 gsheet-player-0.2.1/pyproject.toml
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       38 2023-05-13 02:42:51.571395 gsheet-player-0.2.1/setup.cfg
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-13 02:42:51.569542 gsheet-player-0.2.1/src/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)        0 2023-05-07 17:09:23.000000 gsheet-player-0.2.1/src/__init__.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-13 02:42:51.570078 gsheet-player-0.2.1/src/gsheet_player/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       22 2023-05-13 02:42:47.000000 gsheet-player-0.2.1/src/gsheet_player/__init__.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     2415 2023-05-13 02:38:29.000000 gsheet-player-0.2.1/src/gsheet_player/file_ops.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     8445 2023-05-12 20:21:15.000000 gsheet-player-0.2.1/src/gsheet_player/gsheetPlayer.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     6913 2023-05-12 20:21:15.000000 gsheet-player-0.2.1/src/gsheet_player/gsheet_ops.py
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-13 02:42:51.570759 gsheet-player-0.2.1/src/gsheet_player.egg-info/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1487 2023-05-13 02:42:51.000000 gsheet-player-0.2.1/src/gsheet_player.egg-info/PKG-INFO
+-rw-r--r--   0 gregshepherd   (501) staff       (20)      420 2023-05-13 02:42:51.000000 gsheet-player-0.2.1/src/gsheet_player.egg-info/SOURCES.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)        1 2023-05-13 02:42:51.000000 gsheet-player-0.2.1/src/gsheet_player.egg-info/dependency_links.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       65 2023-05-13 02:42:51.000000 gsheet-player-0.2.1/src/gsheet_player.egg-info/requires.txt
+-rw-r--r--   0 gregshepherd   (501) staff       (20)       23 2023-05-13 02:42:51.000000 gsheet-player-0.2.1/src/gsheet_player.egg-info/top_level.txt
+drwxr-xr-x   0 gregshepherd   (501) staff       (20)        0 2023-05-13 02:42:51.571030 gsheet-player-0.2.1/tests/
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     2029 2023-05-12 20:23:17.000000 gsheet-player-0.2.1/tests/test_file_ops.py
+-rw-r--r--   0 gregshepherd   (501) staff       (20)     1481 2023-05-12 19:51:25.000000 gsheet-player-0.2.1/tests/test_gsheetPlayer.py
```

### Comparing `gsheet-player-0.2.0/PKG-INFO` & `gsheet-player-0.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gsheet-player
-Version: 0.2.0
+Version: 0.2.1
 Summary: Data class to hold a player information from a spreadsheet row
 Author-email: shepworld <info@shepworld.com>
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
```

### Comparing `gsheet-player-0.2.0/README.md` & `gsheet-player-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.2.0/pyproject.toml` & `gsheet-player-0.2.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 
 [project]
 name = "gsheet-player"
 description = "Data class to hold a player information from a spreadsheet row"
 authors = [{ name = "shepworld", email = "info@shepworld.com" }]
 license = { file = "LICENSE" }
 readme = "README.md"
-version = "0.2.0"
+version = "0.2.1"
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3",
 ]
 dependencies = []
 requires-python = ">=3.9"
@@ -26,15 +26,15 @@
 version_pattern = "YYYY.BUILD[-TAG]"
 commit_message = "bump version {old_version} -> {new_version}"
 commit = true
 tag = true
 push = true
 
 [tool.bumpver]
-current_version = "0.2.0"
+current_version = "0.2.1"
 version_pattern = "MAJOR.MINOR.PATCH"
 commit_message  = "bump version {old_version} -> {new_version}"
 commit          = true
 tag             = true
 push            = false
 
 [tool.bumpver.file_patterns]
```

### Comparing `gsheet-player-0.2.0/src/gsheet_player/file_ops.py` & `gsheet-player-0.2.1/src/gsheet_player/file_ops.py`

 * *Files 3% similar despite different names*

```diff
@@ -60,14 +60,16 @@
     # Iterate on first row for header values to name fields
     Person = namedtuple("Person", next(reader), rename=True, defaults=["", 0, [], ""])
     for i, row in enumerate(reader, start=2):
         person = Person(*row)
         curr = gsheetPlayer(person, i, gsheet)
         if curr.cid in players and "FREE" not in curr.cid:
             log.warning(f"DUPLICATE ENTRY: {curr} {curr.cid} row={i}, ignoring...")
+        elif "FREE" in curr.cid:
+            players[f"{curr.cid}_{curr.email}"] = curr
         else:
             players[curr.cid] = curr
             if by_email:
                 emails[curr.email] = curr
 
     if by_email:
         return players, emails
```

### Comparing `gsheet-player-0.2.0/src/gsheet_player/gsheetPlayer.py` & `gsheet-player-0.2.1/src/gsheet_player/gsheetPlayer.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.2.0/src/gsheet_player/gsheet_ops.py` & `gsheet-player-0.2.1/src/gsheet_player/gsheet_ops.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.2.0/src/gsheet_player.egg-info/PKG-INFO` & `gsheet-player-0.2.1/src/gsheet_player.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gsheet-player
-Version: 0.2.0
+Version: 0.2.1
 Summary: Data class to hold a player information from a spreadsheet row
 Author-email: shepworld <info@shepworld.com>
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
```

### Comparing `gsheet-player-0.2.0/tests/test_file_ops.py` & `gsheet-player-0.2.1/tests/test_file_ops.py`

 * *Files identical despite different names*

### Comparing `gsheet-player-0.2.0/tests/test_gsheetPlayer.py` & `gsheet-player-0.2.1/tests/test_gsheetPlayer.py`

 * *Files identical despite different names*

