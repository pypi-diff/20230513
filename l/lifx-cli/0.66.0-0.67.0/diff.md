# Comparing `tmp/lifx_cli-0.66.0.tar.gz` & `tmp/lifx_cli-0.67.0.tar.gz`

## Comparing `lifx_cli-0.66.0.tar` & `lifx_cli-0.67.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/requirements.txt
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/__init__.py
--rwxr-xr-x   0        0        0     1847 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/auth.py
--rwxr-xr-x   0        0        0     1773 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/colors.py
--rwxr-xr-x   0        0        0     1026 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/devices.py
--rwxr-xr-x   0        0        0    10047 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/lifx.py
--rwxr-xr-x   0        0        0     3499 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/lights.py
--rwxr-xr-x   0        0        0      946 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/src/lifx/scenes.py
--rw-r--r--   0        0        0     3085 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/.gitignore
--rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/LICENSE
--rw-r--r--   0        0        0     1734 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/README.md
--rw-r--r--   0        0        0      582 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/pyproject.toml
--rw-r--r--   0        0        0     2224 2020-02-02 00:00:00.000000 lifx_cli-0.66.0/PKG-INFO
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/requirements.txt
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/__init__.py
+-rwxr-xr-x   0        0        0     1847 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/auth.py
+-rwxr-xr-x   0        0        0     1773 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/colors.py
+-rwxr-xr-x   0        0        0     1026 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/devices.py
+-rwxr-xr-x   0        0        0    10047 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/lifx.py
+-rwxr-xr-x   0        0        0     3499 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/lights.py
+-rwxr-xr-x   0        0        0      946 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/src/lifx/scenes.py
+-rw-r--r--   0        0        0     3085 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/.gitignore
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/LICENSE
+-rw-r--r--   0        0        0     1734 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/README.md
+-rw-r--r--   0        0        0      591 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/pyproject.toml
+-rw-r--r--   0        0        0     2224 2020-02-02 00:00:00.000000 lifx_cli-0.67.0/PKG-INFO
```

### Comparing `lifx_cli-0.66.0/src/lifx/auth.py` & `lifx_cli-0.67.0/src/lifx/auth.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/src/lifx/colors.py` & `lifx_cli-0.67.0/src/lifx/colors.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/src/lifx/devices.py` & `lifx_cli-0.67.0/src/lifx/devices.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/src/lifx/lifx.py` & `lifx_cli-0.67.0/src/lifx/lifx.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/src/lifx/lights.py` & `lifx_cli-0.67.0/src/lifx/lights.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/src/lifx/scenes.py` & `lifx_cli-0.67.0/src/lifx/scenes.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/.gitignore` & `lifx_cli-0.67.0/.gitignore`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/LICENSE` & `lifx_cli-0.67.0/LICENSE`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/README.md` & `lifx_cli-0.67.0/README.md`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.66.0/pyproject.toml` & `lifx_cli-0.67.0/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "lifx-cli"
-version = "0.66.0"
+version = "0.67.0"
 authors = [{name="Wes Henderson", email="info@necrux.com"}]
 description = "The Unofficial LIFX CLI"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
@@ -16,8 +16,8 @@
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/necrux/lifx-cli"
 "Bug Tracker" = "https://github.com/necrux/lifx-cli/issues"
 
 [project.scripts]
-lifx = 'lifx:main'
+lifx = 'src.lifx.lifx:main'
```

### Comparing `lifx_cli-0.66.0/PKG-INFO` & `lifx_cli-0.67.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lifx-cli
-Version: 0.66.0
+Version: 0.67.0
 Summary: The Unofficial LIFX CLI
 Project-URL: Homepage, https://github.com/necrux/lifx-cli
 Project-URL: Bug Tracker, https://github.com/necrux/lifx-cli/issues
 Author-email: Wes Henderson <info@necrux.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

