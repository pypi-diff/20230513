# Comparing `tmp/gpt_hero_core-0.0.3.tar.gz` & `tmp/gpt_hero_core-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gpt_hero_core-0.0.3.tar", max compression
+gzip compressed data, was "gpt_hero_core-0.0.4.tar", max compression
```

## Comparing `gpt_hero_core-0.0.3.tar` & `gpt_hero_core-0.0.4.tar`

### file list

```diff
@@ -1,41 +1,46 @@
--rw-r--r--   0        0        0        0 2023-05-05 04:58:13.565597 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/_pytest/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966070 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/asttokens/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:34.975250 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/click/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:34.999316 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/devtools/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966143 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/executing/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:11.870342 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/filelock/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:54.055649 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/git/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:13.705589 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/identify/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:11.870215 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/iniconfig/py.typed
--rw-r--r--   0        0        0       26 2023-05-05 04:59:00.766396 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/isort/_vendored/tomli/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:59:00.769093 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/isort/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:35.009270 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/jinja2/py.typed
--rw-r--r--   0        0        0       26 2023-05-05 04:58:53.867609 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/markdown_it/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966525 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/markupsafe/py.typed
--rw-r--r--   0        0        0       26 2023-05-05 04:58:53.836928 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/mdurl/py.typed
--rw-r--r--   0        0        0       64 2023-05-05 04:58:49.288550 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/mypy/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:11.877313 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/packaging/py.typed
--rw-r--r--   0        0        0      286 2023-05-05 04:57:54.382759 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/pip/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:11.872215 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/platformdirs/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:35.119978 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/pydantic/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:13.608395 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/pytest/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:53.948491 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/rich/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:59:00.670140 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/semver/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:58:14.237899 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/syrupy/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 04:59:00.624640 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/tomlkit/py.typed
--rw-r--r--   0        0        0        0 2023-05-05 05:15:35.139446 gpt_hero_core-0.0.3/.venv/lib/python3.11/site-packages/typer/py.typed
--rw-r--r--   0        0        0     1066 2023-05-05 04:07:10.259156 gpt_hero_core-0.0.3/LICENSE
--rw-r--r--   0        0        0       16 2023-05-05 05:14:52.371760 gpt_hero_core-0.0.3/README.md
--rw-r--r--   0        0        0      897 2023-05-05 05:44:14.335059 gpt_hero_core-0.0.3/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-05 05:14:52.372307 gpt_hero_core-0.0.3/src/gpt_hero_core/__init__.py
--rw-r--r--   0        0        0        0 2023-05-05 05:14:52.372584 gpt_hero_core-0.0.3/src/gpt_hero_core/heros/__init__.py
--rw-r--r--   0        0        0      294 2023-05-05 05:14:52.372862 gpt_hero_core-0.0.3/src/gpt_hero_core/heros/base.py
--rw-r--r--   0        0        0      178 2023-05-05 05:14:52.373181 gpt_hero_core-0.0.3/src/gpt_hero_core/heros/manager.py
--rw-r--r--   0        0        0     4755 2023-05-05 05:20:05.173676 gpt_hero_core-0.0.3/src/gpt_hero_core/main.py
--rw-r--r--   0        0        0        0 2023-05-05 05:14:52.373280 gpt_hero_core-0.0.3/src/gpt_hero_core/plugins/__init__.py
--rw-r--r--   0        0        0      423 2023-05-05 05:14:52.373540 gpt_hero_core-0.0.3/src/gpt_hero_core/plugins/base.py
--rw-r--r--   0        0        0     1675 2023-05-05 05:14:52.373756 gpt_hero_core-0.0.3/src/gpt_hero_core/plugins/manager.py
--rw-r--r--   0        0        0        0 2023-05-05 05:14:52.373860 gpt_hero_core-0.0.3/src/gpt_hero_core/skills/__init__.py
--rw-r--r--   0        0        0      667 2023-05-05 05:14:52.374179 gpt_hero_core-0.0.3/src/gpt_hero_core/skills/base.py
--rw-r--r--   0        0        0      183 2023-05-05 05:14:52.374366 gpt_hero_core-0.0.3/src/gpt_hero_core/skills/manager.py
--rw-r--r--   0        0        0      512 1970-01-01 00:00:00.000000 gpt_hero_core-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:13.565597 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/_pytest/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966070 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/asttokens/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:34.975250 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/click/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:34.999316 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/devtools/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966143 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/executing/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:11.870342 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/filelock/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:54.055649 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/git/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:13.705589 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/identify/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:11.870215 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/iniconfig/py.typed
+-rw-r--r--   0        0        0       26 2023-05-05 04:59:00.766396 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/isort/_vendored/tomli/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:59:00.769093 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/isort/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:35.009270 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/jinja2/py.typed
+-rw-r--r--   0        0        0       26 2023-05-05 04:58:53.867609 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/markdown_it/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:34.966525 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/markupsafe/py.typed
+-rw-r--r--   0        0        0       26 2023-05-05 04:58:53.836928 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/mdurl/py.typed
+-rw-r--r--   0        0        0       64 2023-05-05 04:58:49.288550 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/mypy/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:11.877313 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/packaging/py.typed
+-rw-r--r--   0        0        0      286 2023-05-05 04:57:54.382759 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/pip/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:11.872215 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/platformdirs/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:35.119978 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/pydantic/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:13.608395 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/pytest/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:53.948491 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/rich/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:59:00.670140 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/semver/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:58:14.237899 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/syrupy/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 04:59:00.624640 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/tomlkit/py.typed
+-rw-r--r--   0        0        0        0 2023-05-05 05:15:35.139446 gpt_hero_core-0.0.4/.venv/lib/python3.11/site-packages/typer/py.typed
+-rw-r--r--   0        0        0     1066 2023-05-05 04:07:10.259156 gpt_hero_core-0.0.4/LICENSE
+-rw-r--r--   0        0        0       16 2023-05-05 05:14:52.371760 gpt_hero_core-0.0.4/README.md
+-rw-r--r--   0        0        0      897 2023-05-13 05:46:23.294093 gpt_hero_core-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-05 05:14:52.372307 gpt_hero_core-0.0.4/src/gpt_hero_core/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-05 05:14:52.372584 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/__init__.py
+-rw-r--r--   0        0        0      727 2023-05-13 05:45:45.777784 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/base.py
+-rw-r--r--   0        0        0      472 2023-05-13 05:45:45.778201 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/biography.py
+-rw-r--r--   0        0        0      529 2023-05-13 05:45:45.778973 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/chest.py
+-rw-r--r--   0        0        0      178 2023-05-05 05:14:52.373181 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/manager.py
+-rw-r--r--   0        0        0     1265 2023-05-13 05:45:45.779473 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/mission.py
+-rw-r--r--   0        0        0      774 2023-05-13 05:45:45.780022 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/notebook.py
+-rw-r--r--   0        0        0      560 2023-05-13 05:45:45.780332 gpt_hero_core-0.0.4/src/gpt_hero_core/heros/schema.py
+-rw-r--r--   0        0        0     4755 2023-05-05 05:20:05.173676 gpt_hero_core-0.0.4/src/gpt_hero_core/main.py
+-rw-r--r--   0        0        0        0 2023-05-05 05:14:52.373280 gpt_hero_core-0.0.4/src/gpt_hero_core/plugins/__init__.py
+-rw-r--r--   0        0        0      423 2023-05-05 05:14:52.373540 gpt_hero_core-0.0.4/src/gpt_hero_core/plugins/base.py
+-rw-r--r--   0        0        0     1675 2023-05-05 05:14:52.373756 gpt_hero_core-0.0.4/src/gpt_hero_core/plugins/manager.py
+-rw-r--r--   0        0        0        0 2023-05-05 05:14:52.373860 gpt_hero_core-0.0.4/src/gpt_hero_core/skills/__init__.py
+-rw-r--r--   0        0        0      667 2023-05-05 05:14:52.374179 gpt_hero_core-0.0.4/src/gpt_hero_core/skills/base.py
+-rw-r--r--   0        0        0      183 2023-05-05 05:14:52.374366 gpt_hero_core-0.0.4/src/gpt_hero_core/skills/manager.py
+-rw-r--r--   0        0        0      512 1970-01-01 00:00:00.000000 gpt_hero_core-0.0.4/PKG-INFO
```

### Comparing `gpt_hero_core-0.0.3/LICENSE` & `gpt_hero_core-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `gpt_hero_core-0.0.3/pyproject.toml` & `gpt_hero_core-0.0.4/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gpt-hero-core"
-version = "0.0.3"
+version = "0.0.4"
 description = "A Multi-Agent System for Auto-GPT-like Task Completion"
 authors = ["lucemia <lucemia@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{ include = "gpt_hero_core", from = "src" }]
 include = ["**/py.typed"]
 exclude = ["**/tests"]
```

### Comparing `gpt_hero_core-0.0.3/src/gpt_hero_core/main.py` & `gpt_hero_core-0.0.4/src/gpt_hero_core/main.py`

 * *Files identical despite different names*

### Comparing `gpt_hero_core-0.0.3/src/gpt_hero_core/plugins/manager.py` & `gpt_hero_core-0.0.4/src/gpt_hero_core/plugins/manager.py`

 * *Files identical despite different names*

### Comparing `gpt_hero_core-0.0.3/src/gpt_hero_core/skills/base.py` & `gpt_hero_core-0.0.4/src/gpt_hero_core/skills/base.py`

 * *Files identical despite different names*

### Comparing `gpt_hero_core-0.0.3/PKG-INFO` & `gpt_hero_core-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gpt-hero-core
-Version: 0.0.3
+Version: 0.0.4
 Summary: A Multi-Agent System for Auto-GPT-like Task Completion
 License: MIT
 Author: lucemia
 Author-email: lucemia@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

