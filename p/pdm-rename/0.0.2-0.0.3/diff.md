# Comparing `tmp/pdm-rename-0.0.2.tar.gz` & `tmp/pdm-rename-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pdm-rename-0.0.2.tar", last modified: Mon Nov 21 15:25:39 2022, max compression
+gzip compressed data, was "pdm-rename-0.0.3.tar", last modified: Fri May 12 22:55:34 2023, max compression
```

## Comparing `pdm-rename-0.0.2.tar` & `pdm-rename-0.0.3.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0 runner    (1001) docker     (121)     1064 2022-11-21 15:25:21.729576 pdm-rename-0.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)      401 2022-11-21 15:25:21.729576 pdm-rename-0.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (121)     3884 2022-11-21 15:25:21.729576 pdm-rename-0.0.2/plugin.py
--rw-r--r--   0 runner    (1001) docker     (121)      972 2022-11-21 15:25:21.729576 pdm-rename-0.0.2/pyproject.toml
--rw-------   0 runner    (1001) docker     (121)      657 2022-11-21 15:25:39.853739 pdm-rename-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-05-12 22:55:13.503456 pdm-rename-0.0.3/LICENSE
+-rw-r--r--   0        0        0      401 2023-05-12 22:55:13.503456 pdm-rename-0.0.3/README.md
+-rw-r--r--   0        0        0     3755 2023-05-12 22:55:13.503456 pdm-rename-0.0.3/plugin.py
+-rw-r--r--   0        0        0      972 2023-05-12 22:55:13.503456 pdm-rename-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0      657 1970-01-01 00:00:00.000000 pdm-rename-0.0.3/PKG-INFO
```

### Comparing `pdm-rename-0.0.2/LICENSE` & `pdm-rename-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `pdm-rename-0.0.2/plugin.py` & `pdm-rename-0.0.3/plugin.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,23 +5,18 @@
 from pdm.core import Core
 from pdm.project import Project
 from pdm.signals import post_build, pre_build
 
 
 def parse_config(project: Project) -> Optional[Dict[str, str]]:
     pyproject = project.pyproject
-    if (
-        pyproject is None
-        or "tool" not in pyproject
-        or "pdm" not in pyproject["tool"]
-        or "rename" not in pyproject["tool"]["pdm"]
-    ):
+    if "rename" not in pyproject.settings:
         return None
 
-    rename_config: Dict[str, str] = pyproject["tool"]["pdm"]["rename"]
+    rename_config: Dict[str, str] = pyproject.settings["rename"].value
 
     if (
         not isinstance(rename_config, Dict)
         or not all(isinstance(i, str) for i in rename_config.keys())
         or not all(isinstance(i, str) for i in rename_config.values())
     ):
         project.core.ui.echo("tool.pdm.rename must be a dictionary of strings.", err=True)
@@ -34,15 +29,14 @@
     project: Project,
     rename_config: Dict[str, str],
     rename_back: bool = False,
 ) -> Dict[Path, Path]:
     result: Dict[Path, Path] = {}
 
     for initial_name, rename_to in rename_config.items():
-
         initial_path = project.root.joinpath(Path(initial_name))
         rename_to_path = project.root.joinpath(Path(rename_to))
 
         if not rename_back and not initial_path.exists():
             project.core.ui.echo(
                 f"Directory '{initial_name}' doesn't exist, no renaming.", err=True
             )
```

### Comparing `pdm-rename-0.0.2/pyproject.toml` & `pdm-rename-0.0.3/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 [project]
 name = "pdm-rename"
 description = "Plugin, that allows to dynamically rename folders during the build stage."
 authors = [
     { name = "aleksul", email = "me@aleksul.space" },
 ]
 dependencies = [
-    "pdm>=2.2.1,<3.0",
+    "pdm>=2.3.0,<3.0",
 ]
 requires-python = ">=3.7"
 readme = "README.md"
-version = "0.0.2"
+version = "0.0.3"
 
 [project.license]
 text = "MIT"
 
 [project.entry-points.pdm]
 rename = "plugin:rename_plugin"
```

### Comparing `pdm-rename-0.0.2/PKG-INFO` & `pdm-rename-0.0.3/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pdm-rename
-Version: 0.0.2
+Version: 0.0.3
 Summary: Plugin, that allows to dynamically rename folders during the build stage.
 License: MIT
 Author-email: aleksul <me@aleksul.space>
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
 # pdm-rename
```

