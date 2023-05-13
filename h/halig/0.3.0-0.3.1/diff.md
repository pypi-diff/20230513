# Comparing `tmp/halig-0.3.0.tar.gz` & `tmp/halig-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "halig-0.3.0.tar", last modified: Tue May  9 18:30:22 2023, max compression
+gzip compressed data, was "halig-0.3.1.tar", last modified: Sat May 13 09:13:51 2023, max compression
```

## Comparing `halig-0.3.0.tar` & `halig-0.3.1.tar`

### file list

```diff
@@ -1,26 +1,26 @@
--rw-r--r--   0        0        0    34670 2023-04-12 19:46:50.194310 halig-0.3.0/LICENSE
--rw-r--r--   0        0        0     1633 2023-05-09 17:54:18.830294 halig-0.3.0/README.md
--rw-r--r--   0        0        0        0 2023-04-12 19:46:50.194310 halig-0.3.0/halig/__init__.py
--rw-r--r--   0        0        0       22 2023-05-09 18:28:41.005848 halig-0.3.0/halig/__version__.py
--rw-r--r--   0        0        0        0 2023-04-12 19:46:50.194310 halig-0.3.0/halig/commands/__init__.py
--rw-r--r--   0        0        0      292 2023-04-12 19:47:22.382591 halig-0.3.0/halig/commands/base.py
--rw-r--r--   0        0        0     2781 2023-05-09 06:48:39.717700 halig-0.3.0/halig/commands/edit.py
--rw-r--r--   0        0        0     1076 2023-04-12 19:47:22.382591 halig-0.3.0/halig/commands/notebooks.py
--rw-r--r--   0        0        0     1199 2023-04-12 19:47:22.382591 halig-0.3.0/halig/commands/show.py
--rw-r--r--   0        0        0     1418 2023-05-09 18:17:46.623174 halig-0.3.0/halig/encryption.py
--rw-r--r--   0        0        0     1354 2023-05-08 19:32:21.621775 halig-0.3.0/halig/literals.py
--rw-r--r--   0        0        0     2868 2023-05-08 20:59:47.779605 halig-0.3.0/halig/main.py
--rw-r--r--   0        0        0     3454 2023-05-09 18:26:48.286072 halig-0.3.0/halig/settings.py
--rw-r--r--   0        0        0      733 2023-05-08 21:12:42.122646 halig-0.3.0/halig/utils.py
--rw-r--r--   0        0        0     2656 2023-05-09 18:30:22.105654 halig-0.3.0/pyproject.toml
--rw-r--r--   0        0        0        0 2023-04-12 19:46:50.202310 halig-0.3.0/tests/__init__.py
--rw-r--r--   0        0        0        0 2023-04-12 19:47:22.382591 halig-0.3.0/tests/commands/__init__.py
--rw-r--r--   0        0        0     1645 2023-04-24 10:55:32.886664 halig-0.3.0/tests/commands/conftest.py
--rw-r--r--   0        0        0     1168 2023-05-09 17:58:32.738050 halig-0.3.0/tests/commands/test_edit.py
--rw-r--r--   0        0        0     1563 2023-04-24 10:55:32.886664 halig-0.3.0/tests/commands/test_notebooks.py
--rw-r--r--   0        0        0     1141 2023-04-24 10:55:32.886664 halig-0.3.0/tests/commands/test_show.py
--rw-r--r--   0        0        0     2820 2023-04-12 19:47:22.382591 halig-0.3.0/tests/conftest.py
--rw-r--r--   0        0        0     2276 2023-05-09 06:28:25.521779 halig-0.3.0/tests/test_encryption.py
--rw-r--r--   0        0        0     1541 2023-04-12 19:47:22.386591 halig-0.3.0/tests/test_settings.py
--rw-r--r--   0        0        0     1482 2023-04-24 10:55:32.886664 halig-0.3.0/tests/test_utils.py
--rw-r--r--   0        0        0     3763 1970-01-01 00:00:00.000000 halig-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0    34670 2023-04-12 19:46:50.194310 halig-0.3.1/LICENSE
+-rw-r--r--   0        0        0     1633 2023-05-13 08:52:41.111337 halig-0.3.1/README.md
+-rw-r--r--   0        0        0        0 2023-04-12 19:46:50.194310 halig-0.3.1/halig/__init__.py
+-rw-r--r--   0        0        0       22 2023-05-13 09:12:06.193606 halig-0.3.1/halig/__version__.py
+-rw-r--r--   0        0        0        0 2023-04-12 19:46:50.194310 halig-0.3.1/halig/commands/__init__.py
+-rw-r--r--   0        0        0      292 2023-04-12 19:47:22.382591 halig-0.3.1/halig/commands/base.py
+-rw-r--r--   0        0        0     2781 2023-05-09 06:48:39.717700 halig-0.3.1/halig/commands/edit.py
+-rw-r--r--   0        0        0     1076 2023-04-12 19:47:22.382591 halig-0.3.1/halig/commands/notebooks.py
+-rw-r--r--   0        0        0     1199 2023-04-12 19:47:22.382591 halig-0.3.1/halig/commands/show.py
+-rw-r--r--   0        0        0     1418 2023-05-09 18:17:46.623174 halig-0.3.1/halig/encryption.py
+-rw-r--r--   0        0        0     1354 2023-05-08 19:32:21.621775 halig-0.3.1/halig/literals.py
+-rw-r--r--   0        0        0     2868 2023-05-08 20:59:47.779605 halig-0.3.1/halig/main.py
+-rw-r--r--   0        0        0     3448 2023-05-13 09:05:36.698098 halig-0.3.1/halig/settings.py
+-rw-r--r--   0        0        0      733 2023-05-08 21:12:42.122646 halig-0.3.1/halig/utils.py
+-rw-r--r--   0        0        0     2728 2023-05-13 09:13:51.309472 halig-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-04-12 19:46:50.202310 halig-0.3.1/tests/__init__.py
+-rw-r--r--   0        0        0        0 2023-04-12 19:47:22.382591 halig-0.3.1/tests/commands/__init__.py
+-rw-r--r--   0        0        0     1645 2023-04-24 10:55:32.886664 halig-0.3.1/tests/commands/conftest.py
+-rw-r--r--   0        0        0     1168 2023-05-09 17:58:32.738050 halig-0.3.1/tests/commands/test_edit.py
+-rw-r--r--   0        0        0     1563 2023-04-24 10:55:32.886664 halig-0.3.1/tests/commands/test_notebooks.py
+-rw-r--r--   0        0        0     1141 2023-04-24 10:55:32.886664 halig-0.3.1/tests/commands/test_show.py
+-rw-r--r--   0        0        0     2820 2023-04-12 19:47:22.382591 halig-0.3.1/tests/conftest.py
+-rw-r--r--   0        0        0     2276 2023-05-09 06:28:25.521779 halig-0.3.1/tests/test_encryption.py
+-rw-r--r--   0        0        0     1320 2023-05-13 09:11:29.085662 halig-0.3.1/tests/test_settings.py
+-rw-r--r--   0        0        0     1482 2023-04-24 10:55:32.886664 halig-0.3.1/tests/test_utils.py
+-rw-r--r--   0        0        0     3832 1970-01-01 00:00:00.000000 halig-0.3.1/PKG-INFO
```

### Comparing `halig-0.3.0/LICENSE` & `halig-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/README.md` & `halig-0.3.1/README.md`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/commands/edit.py` & `halig-0.3.1/halig/commands/edit.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/commands/notebooks.py` & `halig-0.3.1/halig/commands/notebooks.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/commands/show.py` & `halig-0.3.1/halig/commands/show.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/encryption.py` & `halig-0.3.1/halig/encryption.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/literals.py` & `halig-0.3.1/halig/literals.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/main.py` & `halig-0.3.1/halig/main.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/halig/settings.py` & `halig-0.3.1/halig/settings.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,13 +1,14 @@
-import os
 from functools import lru_cache
 from pathlib import Path
 from typing import Any
 
 import httpx
+import httpx_cache
+import platformdirs
 import yaml
 from pydantic import BaseSettings, DirectoryPath, FilePath, HttpUrl, validator
 
 
 class Settings(BaseSettings):
     """Settings model. It mainly stores paths that are interesting to the project.
      All the path-attributes described below have a validity check upon instantiation,
@@ -58,15 +59,16 @@
                 keys.add(f.read())
         return keys
 
     def load_public_keys(self) -> set[str]:
         keys = set()
         for path in self.recipient_paths:
             if isinstance(path, HttpUrl):
-                response = httpx.get(str(path))
+                with httpx_cache.Client(cache=httpx_cache.FileCache()) as client:
+                    response = client.get(str(path))
                 if response.status_code == httpx.codes.OK:
                     for line in response.content.decode().split("\n"):
                         if line:
                             keys.add(line)
             elif isinstance(path, Path):
                 with path.open("r") as f:
                     keys.add(f.read())
@@ -75,20 +77,18 @@
     class Config:
         env_prefix = "halig_"
 
 
 @lru_cache
 def load_from_file(file_path: Path | None = None) -> Settings:
     if file_path is None:
-        xdg_config_home = Path(os.getenv("XDG_CONFIG_HOME", "~/.config")).expanduser()
-        if not xdg_config_home.exists():
-            err = f"File {xdg_config_home} does not exist"
-            raise FileNotFoundError(err)
-
-        file_path = xdg_config_home / "halig" / "halig.yml"
+        halig_config_home = Path(
+            platformdirs.user_config_dir("halig", ensure_exists=True),
+        )
+        file_path = halig_config_home / "halig.yml"
         file_path.touch(exist_ok=True)
     elif not file_path.exists():
         err = f"File {file_path} does not exist"
         raise FileNotFoundError(err)
 
     with file_path.open("r") as f:
         data = yaml.safe_load(f)
```

### Comparing `halig-0.3.0/halig/utils.py` & `halig-0.3.1/halig/utils.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/pyproject.toml` & `halig-0.3.1/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -7,14 +7,16 @@
     "typer<1.0.0,>=0.6.1",
     "rich>=13.3.3",
     "pydantic>=1.10.7",
     "pyyaml>=6.0",
     "pyrage>=1.0.3",
     "pendulum>=2.1.2",
     "httpx>=0.24.0",
+    "platformdirs>=3.5.1",
+    "httpx-cache>=0.9.0",
 ]
 name = "halig"
 dynamic = []
 description = "age-encrypted, file-based, note-taking CLI app"
 readme = "README.md"
 keywords = [
     "cli",
@@ -32,15 +34,15 @@
     "Operating System :: POSIX :: Linux",
     "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11",
     "Topic :: Terminals",
     "Topic :: Utilities",
     "Typing :: Typed",
 ]
-version = "0.3.0"
+version = "0.3.1"
 
 [project.license]
 text = "GPL-3.0-or-later"
 
 [project.urls]
 Homepage = "https://git.roboces.dev/catalin/halig"
 Repository = "https://git.roboces.dev/catalin/halig"
@@ -133,14 +135,15 @@
 
 [[tool.mypy.overrides]]
 module = [
     "pyrage",
     "pyrage.ssh",
     "pyrage.x25519",
     "attr",
+    "httpx_cache",
 ]
 ignore_missing_imports = true
 
 [build-system]
 requires = [
     "pdm-backend",
 ]
```

### Comparing `halig-0.3.0/tests/commands/conftest.py` & `halig-0.3.1/tests/commands/conftest.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/commands/test_edit.py` & `halig-0.3.1/tests/commands/test_edit.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/commands/test_notebooks.py` & `halig-0.3.1/tests/commands/test_notebooks.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/commands/test_show.py` & `halig-0.3.1/tests/commands/test_show.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/conftest.py` & `halig-0.3.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/test_encryption.py` & `halig-0.3.1/tests/test_encryption.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/tests/test_settings.py` & `halig-0.3.1/tests/test_settings.py`

 * *Files 17% similar despite different names*

```diff
@@ -16,20 +16,14 @@
 
 
 def test_load_from_file(notebooks_path: Path, settings_file_path: Path):
     settings = load_from_file(settings_file_path)
     assert settings.notebooks_root_path == notebooks_path
 
 
-def test_load_from_non_xdg_home_config_raises_file_not_found_error(fs):
-    path = Path("~/.config").expanduser()
-    with pytest.raises(FileNotFoundError, match=f"File {path} does not exist"):
-        load_from_file()
-
-
 def test_load_from_existing_standard_file(settings_file_path: Path, settings: Settings):
     standard_settings = load_from_file()
     assert standard_settings.notebooks_root_path == settings.notebooks_root_path
 
 
 def test_load_from_empty_file_raises_value_error(empty_file_path: Path):
     with pytest.raises(ValueError, match=f"File {empty_file_path} is empty"):
```

### Comparing `halig-0.3.0/tests/test_utils.py` & `halig-0.3.1/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `halig-0.3.0/PKG-INFO` & `halig-0.3.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: halig
-Version: 0.3.0
+Version: 0.3.1
 Summary: age-encrypted, file-based, note-taking CLI app
 Keywords: cli notes age rage encryption notebook
 Author-Email: cătălin <185504a9@duck.com>
 License: GPL-3.0-or-later
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Console
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
@@ -23,14 +23,16 @@
 Requires-Dist: typer<1.0.0,>=0.6.1
 Requires-Dist: rich>=13.3.3
 Requires-Dist: pydantic>=1.10.7
 Requires-Dist: pyyaml>=6.0
 Requires-Dist: pyrage>=1.0.3
 Requires-Dist: pendulum>=2.1.2
 Requires-Dist: httpx>=0.24.0
+Requires-Dist: platformdirs>=3.5.1
+Requires-Dist: httpx-cache>=0.9.0
 Requires-Dist: pytest>=7.2.2; extra == "testing"
 Requires-Dist: pytest-cov>=4.0.0; extra == "testing"
 Requires-Dist: pyfakefs>=5.1.0; extra == "testing"
 Requires-Dist: pytest-clarity>=1.0.1; extra == "testing"
 Requires-Dist: pytest-reportlog>=0.2.1; extra == "testing"
 Requires-Dist: pytest-duration-insights>=0.1.1; extra == "testing"
 Requires-Dist: pytest-pretty>=1.1.1; extra == "testing"
```

