# Comparing `tmp/pyproject-generator-0.2.5.tar.gz` & `tmp/pyproject-generator-0.2.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyproject-generator-0.2.5.tar", last modified: Fri May 12 20:43:54 2023, max compression
+gzip compressed data, was "pyproject-generator-0.2.6.tar", last modified: Fri May 12 21:19:24 2023, max compression
```

## Comparing `pyproject-generator-0.2.5.tar` & `pyproject-generator-0.2.6.tar`

### file list

```diff
@@ -1,46 +1,46 @@
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.798529 pyproject-generator-0.2.5/
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1078 2023-05-04 01:48:13.000000 pyproject-generator-0.2.5/LICENSE
--rw-r--r--   0 cangyuanli   (501) staff       (20)     4200 2023-05-12 20:43:54.798839 pyproject-generator-0.2.5/PKG-INFO
--rw-r--r--   0 cangyuanli   (501) staff       (20)     3659 2023-05-09 02:31:28.000000 pyproject-generator-0.2.5/README.md
--rw-r--r--   0 cangyuanli   (501) staff       (20)      264 2023-05-08 15:13:51.000000 pyproject-generator-0.2.5/pyproject.toml
--rw-r--r--   0 cangyuanli   (501) staff       (20)      874 2023-05-12 20:43:54.800349 pyproject-generator-0.2.5/setup.cfg
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.744119 pyproject-generator-0.2.5/src/
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.757728 pyproject-generator-0.2.5/src/pyproject/
--rw-r--r--   0 cangyuanli   (501) staff       (20)       51 2023-05-05 02:42:30.000000 pyproject-generator-0.2.5/src/pyproject/__init__.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)       22 2023-05-12 20:43:48.000000 pyproject-generator-0.2.5/src/pyproject/__version__.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)     4781 2023-05-12 20:27:46.000000 pyproject-generator-0.2.5/src/pyproject/cli.py
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.759290 pyproject-generator-0.2.5/src/pyproject/config/
--rw-r--r--   0 cangyuanli   (501) staff       (20)      337 2023-05-05 15:13:27.000000 pyproject-generator-0.2.5/src/pyproject/config/default_config.json
--rw-r--r--   0 cangyuanli   (501) staff       (20)     2246 2023-05-09 13:28:26.000000 pyproject-generator-0.2.5/src/pyproject/licenses.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1727 2023-05-05 12:40:42.000000 pyproject-generator-0.2.5/src/pyproject/logger.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)    16322 2023-05-12 20:27:23.000000 pyproject-generator-0.2.5/src/pyproject/project_builder.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)     2905 2023-05-08 19:42:00.000000 pyproject-generator-0.2.5/src/pyproject/spinner.py
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.790106 pyproject-generator-0.2.5/src/pyproject/templates/
--rw-r--r--   0 cangyuanli   (501) staff       (20)      863 2023-05-12 20:20:29.000000 pyproject-generator-0.2.5/src/pyproject/templates/gh_actions_status_update.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      643 2023-05-12 20:21:48.000000 pyproject-generator-0.2.5/src/pyproject/templates/gh_actions_tests.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1498 2023-05-03 19:23:49.000000 pyproject-generator-0.2.5/src/pyproject/templates/gitignore.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)    34503 2023-05-09 13:30:26.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_agpl_v3.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      549 2023-05-09 02:32:18.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_apache_v2.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1292 2023-05-09 00:48:28.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_bsd2.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1457 2023-05-04 13:35:45.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_bsd3.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)    18092 2023-05-09 00:34:37.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_gpl_v2.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)    35149 2023-05-09 00:33:45.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_gpl_v3.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     7633 2023-05-09 13:30:26.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_lgpl_v3.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1074 2023-04-30 01:18:24.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_mit.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)    16726 2023-05-09 00:40:15.000000 pyproject-generator-0.2.5/src/pyproject/templates/license_mozilla_v2.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      905 2023-05-03 23:48:11.000000 pyproject-generator-0.2.5/src/pyproject/templates/pre_commit_config.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      263 2023-05-04 02:15:39.000000 pyproject-generator-0.2.5/src/pyproject/templates/pyproject.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1040 2023-05-04 20:10:03.000000 pyproject-generator-0.2.5/src/pyproject/templates/readme.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      603 2023-05-05 12:52:13.000000 pyproject-generator-0.2.5/src/pyproject/templates/setup.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      402 2023-04-12 23:45:24.000000 pyproject-generator-0.2.5/src/pyproject/templates/tox.template
--rw-r--r--   0 cangyuanli   (501) staff       (20)      220 2023-05-07 23:06:58.000000 pyproject-generator-0.2.5/src/pyproject/utils.py
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.794996 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/
--rw-r--r--   0 cangyuanli   (501) staff       (20)     4200 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/PKG-INFO
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1411 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/SOURCES.txt
--rw-r--r--   0 cangyuanli   (501) staff       (20)        1 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/dependency_links.txt
--rw-r--r--   0 cangyuanli   (501) staff       (20)       49 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/entry_points.txt
--rw-r--r--   0 cangyuanli   (501) staff       (20)       18 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/requires.txt
--rw-r--r--   0 cangyuanli   (501) staff       (20)       10 2023-05-12 20:43:54.000000 pyproject-generator-0.2.5/src/pyproject_generator.egg-info/top_level.txt
-drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 20:43:54.797085 pyproject-generator-0.2.5/tests/
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1001 2023-05-09 02:01:59.000000 pyproject-generator-0.2.5/tests/test_cli.py
--rw-r--r--   0 cangyuanli   (501) staff       (20)     1808 2023-05-09 06:04:34.000000 pyproject-generator-0.2.5/tests/test_pyproject.py
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.778491 pyproject-generator-0.2.6/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1078 2023-05-04 01:48:13.000000 pyproject-generator-0.2.6/LICENSE
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     4200 2023-05-12 21:19:24.778841 pyproject-generator-0.2.6/PKG-INFO
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     3659 2023-05-09 02:31:28.000000 pyproject-generator-0.2.6/README.md
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      264 2023-05-08 15:13:51.000000 pyproject-generator-0.2.6/pyproject.toml
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      874 2023-05-12 21:19:24.781011 pyproject-generator-0.2.6/setup.cfg
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.723706 pyproject-generator-0.2.6/src/
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.737506 pyproject-generator-0.2.6/src/pyproject/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)       51 2023-05-05 02:42:30.000000 pyproject-generator-0.2.6/src/pyproject/__init__.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)       22 2023-05-12 21:18:20.000000 pyproject-generator-0.2.6/src/pyproject/__version__.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     4781 2023-05-12 20:27:46.000000 pyproject-generator-0.2.6/src/pyproject/cli.py
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.738638 pyproject-generator-0.2.6/src/pyproject/config/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      337 2023-05-05 15:13:27.000000 pyproject-generator-0.2.6/src/pyproject/config/default_config.json
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     2246 2023-05-09 13:28:26.000000 pyproject-generator-0.2.6/src/pyproject/licenses.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1727 2023-05-05 12:40:42.000000 pyproject-generator-0.2.6/src/pyproject/logger.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)    16353 2023-05-12 21:13:14.000000 pyproject-generator-0.2.6/src/pyproject/project_builder.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     2905 2023-05-08 19:42:00.000000 pyproject-generator-0.2.6/src/pyproject/spinner.py
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.768904 pyproject-generator-0.2.6/src/pyproject/templates/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      863 2023-05-12 20:20:29.000000 pyproject-generator-0.2.6/src/pyproject/templates/gh_actions_status_update.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      643 2023-05-12 20:21:48.000000 pyproject-generator-0.2.6/src/pyproject/templates/gh_actions_tests.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1498 2023-05-03 19:23:49.000000 pyproject-generator-0.2.6/src/pyproject/templates/gitignore.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)    34503 2023-05-09 13:30:26.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_agpl_v3.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      549 2023-05-09 02:32:18.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_apache_v2.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1292 2023-05-09 00:48:28.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_bsd2.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1457 2023-05-04 13:35:45.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_bsd3.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)    18092 2023-05-09 00:34:37.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_gpl_v2.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)    35149 2023-05-09 00:33:45.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_gpl_v3.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     7633 2023-05-09 13:30:26.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_lgpl_v3.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1074 2023-04-30 01:18:24.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_mit.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)    16726 2023-05-09 00:40:15.000000 pyproject-generator-0.2.6/src/pyproject/templates/license_mozilla_v2.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      905 2023-05-03 23:48:11.000000 pyproject-generator-0.2.6/src/pyproject/templates/pre_commit_config.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      263 2023-05-04 02:15:39.000000 pyproject-generator-0.2.6/src/pyproject/templates/pyproject.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1040 2023-05-04 20:10:03.000000 pyproject-generator-0.2.6/src/pyproject/templates/readme.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      603 2023-05-05 12:52:13.000000 pyproject-generator-0.2.6/src/pyproject/templates/setup.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      402 2023-04-12 23:45:24.000000 pyproject-generator-0.2.6/src/pyproject/templates/tox.template
+-rw-r--r--   0 cangyuanli   (501) staff       (20)      220 2023-05-07 23:06:58.000000 pyproject-generator-0.2.6/src/pyproject/utils.py
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.774312 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     4200 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/PKG-INFO
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1411 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/SOURCES.txt
+-rw-r--r--   0 cangyuanli   (501) staff       (20)        1 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/dependency_links.txt
+-rw-r--r--   0 cangyuanli   (501) staff       (20)       49 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/entry_points.txt
+-rw-r--r--   0 cangyuanli   (501) staff       (20)       18 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/requires.txt
+-rw-r--r--   0 cangyuanli   (501) staff       (20)       10 2023-05-12 21:19:24.000000 pyproject-generator-0.2.6/src/pyproject_generator.egg-info/top_level.txt
+drwxr-xr-x   0 cangyuanli   (501) staff       (20)        0 2023-05-12 21:19:24.776649 pyproject-generator-0.2.6/tests/
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1001 2023-05-09 02:01:59.000000 pyproject-generator-0.2.6/tests/test_cli.py
+-rw-r--r--   0 cangyuanli   (501) staff       (20)     1808 2023-05-09 06:04:34.000000 pyproject-generator-0.2.6/tests/test_pyproject.py
```

### Comparing `pyproject-generator-0.2.5/LICENSE` & `pyproject-generator-0.2.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/PKG-INFO` & `pyproject-generator-0.2.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyproject-generator
-Version: 0.2.5
+Version: 0.2.6
 Summary: A command line tool to setup Python packages
 Home-page: https://github.com/CangyuanLi/pyproject
 Author: Cangyuan Li
 Author-email: everest229@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/CangyuanLi/pyproject/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `pyproject-generator-0.2.5/README.md` & `pyproject-generator-0.2.6/README.md`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/setup.cfg` & `pyproject-generator-0.2.6/setup.cfg`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/cli.py` & `pyproject-generator-0.2.6/src/pyproject/cli.py`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/licenses.py` & `pyproject-generator-0.2.6/src/pyproject/licenses.py`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/logger.py` & `pyproject-generator-0.2.6/src/pyproject/logger.py`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/project_builder.py` & `pyproject-generator-0.2.6/src/pyproject/project_builder.py`

 * *Files 1% similar despite different names*

```diff
@@ -158,15 +158,15 @@
         self._config = self._set_config(config)
 
     def _create_config_dir(self) -> None:
         """Create the user config directory if it does not exist. Since the default
         configuration may add keys, merge the two, preferring the
         existing config so we don't overwrite user changes.
         """
-        self._user_config_dir.mkdir(exist_ok=True)
+        self._user_config_dir.mkdir(parents=True, exist_ok=True)
         config_file = self._user_config_dir / "config.json"
 
         if not config_file.exists() or config_file.stat().st_size == 0:
             shutil.copy(
                 BASE_PATH / "config/default_config.json",
                 config_file,
             )
@@ -200,15 +200,15 @@
             "LICENSE": config.license.proper_name,
             "LICENSE_BADGE": config.license.badge_url,
             "LICENSE_LINK": config.license.link,
         }
 
         filled_in_templates = {}
         for file in self._template_path.glob("*.template"):
-            with open(file, "r") as f:
+            with open(file, "r", encoding="utf8") as f:
                 src = string.Template(f.read())
                 result = src.substitute(d)
 
                 filled_in_templates[file.stem] = result
 
         return filled_in_templates
```

### Comparing `pyproject-generator-0.2.5/src/pyproject/spinner.py` & `pyproject-generator-0.2.6/src/pyproject/spinner.py`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/gh_actions_status_update.template` & `pyproject-generator-0.2.6/src/pyproject/templates/gh_actions_status_update.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/gh_actions_tests.template` & `pyproject-generator-0.2.6/src/pyproject/templates/gh_actions_tests.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/gitignore.template` & `pyproject-generator-0.2.6/src/pyproject/templates/gitignore.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_agpl_v3.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_agpl_v3.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_apache_v2.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_apache_v2.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_bsd2.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_bsd2.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_bsd3.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_bsd3.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_gpl_v2.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_gpl_v2.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_gpl_v3.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_gpl_v3.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_lgpl_v3.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_lgpl_v3.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_mit.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_mit.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/license_mozilla_v2.template` & `pyproject-generator-0.2.6/src/pyproject/templates/license_mozilla_v2.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/pre_commit_config.template` & `pyproject-generator-0.2.6/src/pyproject/templates/pre_commit_config.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/readme.template` & `pyproject-generator-0.2.6/src/pyproject/templates/readme.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject/templates/setup.template` & `pyproject-generator-0.2.6/src/pyproject/templates/setup.template`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/src/pyproject_generator.egg-info/PKG-INFO` & `pyproject-generator-0.2.6/src/pyproject_generator.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyproject-generator
-Version: 0.2.5
+Version: 0.2.6
 Summary: A command line tool to setup Python packages
 Home-page: https://github.com/CangyuanLi/pyproject
 Author: Cangyuan Li
 Author-email: everest229@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/CangyuanLi/pyproject/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `pyproject-generator-0.2.5/src/pyproject_generator.egg-info/SOURCES.txt` & `pyproject-generator-0.2.6/src/pyproject_generator.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/tests/test_cli.py` & `pyproject-generator-0.2.6/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `pyproject-generator-0.2.5/tests/test_pyproject.py` & `pyproject-generator-0.2.6/tests/test_pyproject.py`

 * *Files identical despite different names*

