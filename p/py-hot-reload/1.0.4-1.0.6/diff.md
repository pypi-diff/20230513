# Comparing `tmp/py-hot-reload-1.0.4.tar.gz` & `tmp/py-hot-reload-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py-hot-reload-1.0.4.tar", last modified: Thu May 11 22:04:06 2023, max compression
+gzip compressed data, was "py-hot-reload-1.0.6.tar", last modified: Sat May 13 20:11:51 2023, max compression
```

## Comparing `py-hot-reload-1.0.4.tar` & `py-hot-reload-1.0.6.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3888 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1604 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 22:04:06.685377 py-hot-reload-1.0.4/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/src/py_hot_reload/
--rw-r--r--   0 runner    (1001) docker     (123)    13179 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/src/py_hot_reload/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2886 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/src/py_hot_reload/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3888 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-11 22:04:06.000000 py-hot-reload-1.0.4/src/py_hot_reload.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 22:04:06.689377 py-hot-reload-1.0.4/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/tests/test.py
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/tests/test2.py
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-11 22:03:55.000000 py-hot-reload-1.0.4/tests/testtt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:11:51.864651 py-hot-reload-1.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3888 2023-05-13 20:11:51.864651 py-hot-reload-1.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1604 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1594 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 20:11:51.864651 py-hot-reload-1.0.6/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:11:51.860651 py-hot-reload-1.0.6/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:11:51.860651 py-hot-reload-1.0.6/src/py_hot_reload/
+-rw-r--r--   0 runner    (1001) docker     (123)    13179 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/src/py_hot_reload/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3154 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/src/py_hot_reload/__main__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:11:51.864651 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3888 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-13 20:11:51.000000 py-hot-reload-1.0.6/src/py_hot_reload.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:11:51.864651 py-hot-reload-1.0.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/tests/test.py
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/tests/test2.py
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 20:11:36.000000 py-hot-reload-1.0.6/tests/testtt.py
```

### Comparing `py-hot-reload-1.0.4/LICENSE` & `py-hot-reload-1.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `py-hot-reload-1.0.4/PKG-INFO` & `py-hot-reload-1.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-hot-reload
-Version: 1.0.4
+Version: 1.0.6
 Summary: Python Hot Reload starts the given program and reloads it whenever any file changes in the current directory or imported modules.
 Author-email: Heppa Soft <heppasoft@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 heppasoft
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `py-hot-reload-1.0.4/README.md` & `py-hot-reload-1.0.6/README.md`

 * *Files identical despite different names*

### Comparing `py-hot-reload-1.0.4/pyproject.toml` & `py-hot-reload-1.0.6/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 [build-system]
 requires = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "py-hot-reload"
-version = "1.0.4"
+version = "1.0.6"
 description = "Python Hot Reload starts the given program and reloads it whenever any file changes in the current directory or imported modules."
 readme = "README.md"
 authors = [{ name = "Heppa Soft", email = "heppasoft@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "Development Status :: 5 - Production/Stable",
     "Topic :: Utilities",
@@ -35,19 +35,15 @@
 "Homepage" = "https://github.com/heppasoft/hot-reload"
 "Bug Tracker" = "https://github.com/heppasoft/hot-reload/issues"
 
 [project.scripts]
 py-hot-reload = "py_hot_reload.__main__:main"
 
 [tool.bumpver]
-current_version = "1.0.4"
+current_version = "1.0.6"
 version_pattern = "MAJOR.MINOR.PATCH"
-commit_message  = "{new_version}"
-commit          = true
-tag             = true
-push            = false
 
 [tool.bumpver.file_patterns]
 "pyproject.toml" = ['current_version = "{version}"', 'version = "{version}"']
 "src/py_hot_reload/__init__.py" = ['__version__ = "{version}"']
 "src/py_hot_reload/__main__.py" = ['__version__ = "{version}"']
```

### Comparing `py-hot-reload-1.0.4/src/py_hot_reload/__init__.py` & `py-hot-reload-1.0.6/src/py_hot_reload/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 
 __all__ = ["run_with_reloader", "file_run_with_reloader"]
 
 
 __author__ = "Heppa Soft"
 __copyright__ = "Copyright (C) 2023 Heppa Soft"
 __license__ = "MIT License"
-__version__ = "1.0.4"
+__version__ = "1.0.6"
 
 _ignore_always = tuple({sys.base_prefix, sys.base_exec_prefix})
 
 
 _ignore_common_dirs = {
     "__pycache__",
     ".git",
```

### Comparing `py-hot-reload-1.0.4/src/py_hot_reload/__main__.py` & `py-hot-reload-1.0.6/src/py_hot_reload/__main__.py`

 * *Files 9% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import click
 import subprocess
 
 
 __author__ = "Heppa Soft"
 __copyright__ = "Copyright (C) 2023 Heppa Soft"
 __license__ = "MIT License"
-__version__ = "1.0.4"
+__version__ = "1.0.6"
 
 
 def print_version(ctx, param, value):
     if not value or ctx.resilient_parsing:
         return
     click.echo("Version {}".format(__version__))
     ctx.exit()
@@ -57,14 +57,19 @@
         extra_patterns = extra_patterns.split(";")
     
     venv = os.getenv("VIRTUAL_ENV")
     executable = "python"
     if venv != None:
         executable = f"{venv}/bin/python" if os.name == "posix" else f"{venv}/Scripts/python.exe"
     
+    p = run_shell_command([executable, "-c", "import py_hot_reload"])
+    err = p[1].decode()
+    if err != "" and "ModuleNotFoundError: No module named 'py_hot_reload'" in err:
+        p = run_shell_command([executable, "-m", "pip", "install", "py_hot_reload"])
+    
     exit_code = subprocess.call([executable,"-c",f"import py_hot_reload;py_hot_reload.file_run_with_reloader('{python_file}', {args}, {extra_patterns}, {ignore_patterns}, {interval}, {verbose}, {add_current_folder_to_patterns}, {ignore_venv_and_python_lib})"], env=os.environ.copy(), close_fds=False)
     
     if exit_code != 3:
         return exit_code
 
 def main():
     hot_reload()
```

### Comparing `py-hot-reload-1.0.4/src/py_hot_reload.egg-info/PKG-INFO` & `py-hot-reload-1.0.6/src/py_hot_reload.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-hot-reload
-Version: 1.0.4
+Version: 1.0.6
 Summary: Python Hot Reload starts the given program and reloads it whenever any file changes in the current directory or imported modules.
 Author-email: Heppa Soft <heppasoft@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 heppasoft
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

