# Comparing `tmp/delfino-1.2.0.tar.gz` & `tmp/delfino-1.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "delfino-1.2.0.tar", max compression
+gzip compressed data, was "delfino-1.3.0.tar", max compression
```

## Comparing `delfino-1.2.0.tar` & `delfino-1.3.0.tar`

### file list

```diff
@@ -1,29 +1,29 @@
--rw-r--r--   0        0        0     1067 2023-05-06 20:40:51.841157 delfino-1.2.0/LICENSE
--rw-r--r--   0        0        0    17473 2023-05-06 20:40:51.841157 delfino-1.2.0/README.md
--rw-r--r--   0        0        0     3681 2023-05-06 20:40:51.841157 delfino-1.2.0/pyproject.toml
--rw-r--r--   0        0        0       34 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/__init__.py
--rw-r--r--   0        0        0      273 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/backports.py
--rw-r--r--   0        0        0       76 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/click_utils/__init__.py
--rw-r--r--   0        0        0    10340 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/click_utils/command.py
--rwxr-xr-x   0        0        0     2238 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/click_utils/command_groups.py
--rw-r--r--   0        0        0     3378 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/click_utils/set_from_config.py
--rw-r--r--   0        0        0     1343 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/config.py
--rw-r--r--   0        0        0      270 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/constants.py
--rw-r--r--   0        0        0      182 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/decorators/__init__.py
--rw-r--r--   0        0        0      545 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/decorators/files_folders.py
--rw-r--r--   0        0        0     1754 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/decorators/pass_app_context.py
--rw-r--r--   0        0        0     1545 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/decorators/pass_args.py
--rw-r--r--   0        0        0     4220 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/execution.py
--rw-r--r--   0        0        0        0 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/internal_parameters/__init__.py
--rw-r--r--   0        0        0     5402 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/internal_parameters/completion.py
--rw-r--r--   0        0        0      506 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/internal_parameters/help.py
--rw-r--r--   0        0        0      892 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/internal_parameters/verbosity.py
--rw-r--r--   0        0        0     4284 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/main.py
--rw-r--r--   0        0        0      143 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/models/__init__.py
--rw-r--r--   0        0        0      522 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/models/app_context.py
--rw-r--r--   0        0        0     1370 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/models/pyproject_toml.py
--rw-r--r--   0        0        0     1090 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/terminal_output.py
--rw-r--r--   0        0        0      618 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/utils.py
--rw-r--r--   0        0        0     1350 2023-05-06 20:40:51.841157 delfino-1.2.0/src/delfino/validation.py
--rw-r--r--   0        0        0    19083 1970-01-01 00:00:00.000000 delfino-1.2.0/setup.py
--rw-r--r--   0        0        0    18943 1970-01-01 00:00:00.000000 delfino-1.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-05-13 10:12:13.093087 delfino-1.3.0/LICENSE
+-rw-r--r--   0        0        0    18511 2023-05-13 10:12:13.093087 delfino-1.3.0/README.md
+-rw-r--r--   0        0        0     3681 2023-05-13 10:12:13.093087 delfino-1.3.0/pyproject.toml
+-rw-r--r--   0        0        0       34 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/__init__.py
+-rw-r--r--   0        0        0      273 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/backports.py
+-rw-r--r--   0        0        0       76 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/click_utils/__init__.py
+-rw-r--r--   0        0        0    10468 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/click_utils/command.py
+-rwxr-xr-x   0        0        0     2238 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/click_utils/command_groups.py
+-rw-r--r--   0        0        0     3378 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/click_utils/set_from_config.py
+-rw-r--r--   0        0        0     1343 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/config.py
+-rw-r--r--   0        0        0      270 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/constants.py
+-rw-r--r--   0        0        0      182 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/decorators/__init__.py
+-rw-r--r--   0        0        0      545 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/decorators/files_folders.py
+-rw-r--r--   0        0        0     1754 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/decorators/pass_app_context.py
+-rw-r--r--   0        0        0     1545 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/decorators/pass_args.py
+-rw-r--r--   0        0        0     4220 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/execution.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/internal_parameters/__init__.py
+-rw-r--r--   0        0        0     5402 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/internal_parameters/completion.py
+-rw-r--r--   0        0        0      506 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/internal_parameters/help.py
+-rw-r--r--   0        0        0      892 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/internal_parameters/verbosity.py
+-rw-r--r--   0        0        0     4278 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/main.py
+-rw-r--r--   0        0        0      143 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/models/__init__.py
+-rw-r--r--   0        0        0      522 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/models/app_context.py
+-rw-r--r--   0        0        0     1686 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/models/pyproject_toml.py
+-rw-r--r--   0        0        0     1090 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/terminal_output.py
+-rw-r--r--   0        0        0      618 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/utils.py
+-rw-r--r--   0        0        0     1350 2023-05-13 10:12:13.093087 delfino-1.3.0/src/delfino/validation.py
+-rw-r--r--   0        0        0    20131 1970-01-01 00:00:00.000000 delfino-1.3.0/setup.py
+-rw-r--r--   0        0        0    19981 1970-01-01 00:00:00.000000 delfino-1.3.0/PKG-INFO
```

### Comparing `delfino-1.2.0/LICENSE` & `delfino-1.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/README.md` & `delfino-1.3.0/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 <h1 align="center" style="border-bottom: none;">🧰&nbsp;&nbsp;Delfino&nbsp;&nbsp;🧰</h1>
-<h3 align="center">Plugable Click command finder/loader/executor.</h3>
+<h3 align="center">The Ultimate Command Line Companion for Your Projects</h3>
 
 <p align="center">
     <a href="https://app.circleci.com/pipelines/github/radeklat/delfino?branch=main">
         <img alt="CircleCI" src="https://img.shields.io/circleci/build/github/radeklat/delfino">
     </a>
     <a href="https://app.codecov.io/gh/radeklat/delfino/">
         <img alt="Codecov" src="https://img.shields.io/codecov/c/github/radeklat/delfino">
@@ -19,59 +19,52 @@
         <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/delfino">
     </a>
     <a href="https://pypistats.org/packages/delfino">
         <img alt="Downloads" src="https://img.shields.io/pypi/dm/delfino">
     </a>
 </p>
 
+Tired of managing scattered scripts? Say goodbye to complexity with Delfino!
+
+Delfino is a powerful wrapper around Click, the popular command line interface package. It automatically discovers and executes Click commands in your project. But Delfino doesn't stop there - it takes it a step further by allowing you to create plugins, making script distribution and installation a breeze.
+
+# Why choose Delfino?
+
+- **Streamline Scripts**: Consolidate all your helper scripts into a single, easy-to-use entry point. No more hunting for scripts or dealing with convoluted aliases. Simply use delfino followed by the script name and options.
+- **Reusable Plugins**: Package your helper scripts as plugins and install them with pip. Maintain consistency across projects and easily incorporate updates through a flexible configuration system.
+- **Simplify Tooling**: Delfino extends Click with advanced features like pass-through command-line options and seamless handling of file lists. Say goodbye to verbosity and hello to optimized workflows.
+
+Don't let scattered scripts and complex tooling slow you down. Embrace Delfino and revolutionize your command line experience. Try Delfino today and unlock simplicity in your projects!
+
 <!--
     How to generate TOC from PyCharm:
     https://github.com/vsch/idea-multimarkdown/wiki/Table-of-Contents-Extension
 -->
 [TOC levels=1,2 markdown formatted bullet hierarchy]: # "Table of content"
 
 # Table of content
-- [What is Delfino](#what-is-delfino)
-  - [Plugins](#plugins)
 - [Installation](#installation)
 - [Configuration](#configuration)
-  - [Enabling a plugin](#enabling-a-plugin)
-  - [Enabling/disabling commands](#enablingdisabling-commands)
 - [Usage](#usage)
 - [Development](#development)
   - [Commands discovery](#commands-discovery)
   - [Minimal command](#minimal-command)
   - [Minimal plugin](#minimal-plugin)
+- [Existing plugins](#existing-plugins)
+  - [Enabling a plugin](#enabling-a-plugin)
+  - [Enabling/disabling commands](#enablingdisabling-commands)
 - [Advanced usage](#advanced-usage)
   - [Auto-completion](#auto-completion)
   - [Running external programs](#running-external-programs)
   - [Optional dependencies](#optional-dependencies)
   - [Project settings](#project-settings)
   - [Plugin settings](#plugin-settings)
   - [Project specific overrides](#project-specific-overrides)
   - [Grouping commands](#grouping-commands)
 
-# What is Delfino
-
-Delfino is a wrapper around [Click](https://click.palletsprojects.com) command line scripts. It automatically discovers instances of [Click commands](https://click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command) and offers them for execution. However, the biggest power comes from the possibility of creating [plugins](#plugins), which can be distributed as standard Python packages.
-
-## Plugins
-
-Plugins can greatly reduce code duplication and/or promote your own standards in multiple places. For example, you can create a plugin wrapping common linting tools that you use on your projects, including their default configuration. Keeping the rules and creating new projects with the same style suddenly becomes a matter of installing one Python library.
-
-Each plugin can contain one or more Click commands that are automatically discovered and exposed by Delfino. See [`delfino-demo`](https://github.com/radeklat/delfino-demo) for a minimal plugin, which provide a `demo` command printing out a message.
-
-Existing plugins:
-
-| Plugin name                                                  | Description                                                                                        |
-|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
-| [delfino-demo](https://github.com/radeklat/delfino-demo)     | A minimal plugin example for Delfino. Contains one command printing a message.                     |
-| [delfino-core](https://github.com/radeklat/delfino-core)     | Commands wrapping tools used during every day development (linting, testing, dependencies update). |
-| [delfino-docker](https://github.com/radeklat/delfino-docker) | Docker build helper script.                                                                        |
-
 # Installation
 
 - pip: `pip install delfino`
 - Poetry: `poetry add --group=dev delfino`
 - Pipenv: `pipenv install -d delfino`
 
 or 
@@ -83,63 +76,42 @@
 to enable [auto-completion](#auto-completion).
 
 # Configuration
 
 All configuration is expected to live in one of the following files:
 
 - `pyproject.toml` in the project root
-- `.pylintrc` in the project root - to allow dev specific config, not source controlled or for non-Python projects
-- `.pylintrc` in the user home directory - for user tools available in the system
+- `.delfinorc` in the project root - to allow dev specific config, not source controlled or for non-Python projects
+- `.delfinorc` in the user home directory - for user tools available in the system
 
 If multiple files are discovered, only the highest one in the list will be used.
 
-The format for `.pylintrc` is the same as for `pyproject.toml`.
-
-## Enabling a plugin
-
-For security reasons, plugins are disabled by default. To enable a plugin, you have to include it in the `pyproject.toml` file:
-
-```toml
-[tool.delfino.plugins.<PLUGIN_NAME>]
-```
-
-## Enabling/disabling commands
-
-By default, all commands are enabled. Use `enable_commands` or `disable_commands`  to show only a subset of commands. If both used, disabled commands are subtracted from the set of enabled commands.
-
-```toml
-# [tool.delfino.plugins.<PLUGIN_NAME_A>]
-# enable_commands = [<COMMAND_NAME>]
-# disable_commands = [<COMMAND_NAME>]
-
-# [tool.delfino.plugins.<PLUGIN_NAME_B>]
-# enable_commands = [<COMMAND_NAME>]
-# disable_commands = [<COMMAND_NAME>]
-```
+The format for `.delfinorc` is the same as for `pyproject.toml`.
 
 # Usage
 
 Run `delfino --help` to see all available commands and their usage.
 
 # Development
 
 Delfino is a simple wrapper around [Click commands](https://click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command). Any Click command will be accepted by Delfino.
 
 ## Commands discovery
 
 Delfino looks for any [`click.Command`](https://click.palletsprojects.com/en/8.0.x/api/#click.Command) sub-class in the following locations:
 
-- `commands` folder in the root of the project (next to the `pyproject.toml` file). This location is useful for commands that don't need to be replicated in multiple locations/projects.
+- `commands` folder in the root of the project (next to the `pyproject.toml` file). This location is useful for commands that don't need to be replicated in multiple locations/projects. To change the default location, use the `tool.delfino.local_command_folders` config option. It allows specifying more than one folder.
 - python module import path (`<IMPORT_PATH>`) specified by `entry_point` of [a plugin](#minimal-plugin):
   ```toml
   [tool.poetry.plugins] # Optional super table
 
   [tool.poetry.plugins."delfino.plugin"]
   "delfino-<PLUGIN_NAME>" = "<IMPORT_PATH>"
   ```
+- Folder specified in the [config file](#configuration) under `tool.delfino.local_commands_directory`.
 
 Any files starting with an underscore, except for `__init__.py`, will be ignored.
 
 > **Warning**
 > Folders are NOT inspected recursively. If you place any commands into nested folders, they will not be loaded by Delfino.
 
 
@@ -179,14 +151,50 @@
 
 If you'd like to use one or more commands in multiple places, you can create a plugin. A plugin is just a regular Python package with specific entry point telling Delfino it should use it. It can also be distributed as any other Python packages, for example via Pypi.
 
 The quickest way to create one is to use a [Delfino plugin cookiecutter template](https://github.com/radeklat/delfino-plugin-cookiecutter-template), which asks you several questions and sets up the whole project.
 
 Alternatively, you can get inspired by [the demo plugin](https://github.com/radeklat/delfino-demo) or any of the other [existing plugins](#plugins).
 
+# Existing plugins
+
+Plugins can greatly reduce code duplication and/or promote your own standards in multiple places. For example, you can create a plugin wrapping common linting tools that you use on your projects, including their default configuration. Keeping the rules and creating new projects with the same style suddenly becomes a matter of installing one Python library.
+
+Each plugin can contain one or more Click commands that are automatically discovered and exposed by Delfino. See [`delfino-demo`](https://github.com/radeklat/delfino-demo) for a minimal plugin, which provide a `demo` command printing out a message.
+
+Existing plugins:
+
+| Plugin name                                                  | Description                                                                                        |
+|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
+| [delfino-demo](https://github.com/radeklat/delfino-demo)     | A minimal plugin example for Delfino. Contains one command printing a message.                     |
+| [delfino-core](https://github.com/radeklat/delfino-core)     | Commands wrapping tools used during every day development (linting, testing, dependencies update). |
+| [delfino-docker](https://github.com/radeklat/delfino-docker) | Docker build helper script.                                                                        |
+
+## Enabling a plugin
+
+For security reasons, plugins are disabled by default. To enable a plugin, you have to include it in the `pyproject.toml` file:
+
+```toml
+[tool.delfino.plugins.<PLUGIN_NAME>]
+```
+
+## Enabling/disabling commands
+
+By default, all commands are enabled. Use `enable_commands` or `disable_commands`  to show only a subset of commands. If both used, disabled commands are subtracted from the set of enabled commands.
+
+```toml
+# [tool.delfino.plugins.<PLUGIN_NAME_A>]
+# enable_commands = [<COMMAND_NAME>]
+# disable_commands = [<COMMAND_NAME>]
+
+# [tool.delfino.plugins.<PLUGIN_NAME_B>]
+# enable_commands = [<COMMAND_NAME>]
+# disable_commands = [<COMMAND_NAME>]
+```
+
 # Advanced usage
 
 <!--
 ## Advanced Command
 
 Delfino adds optional bits of functionality on top of Click. The following example demonstrates some of those:
```

### Comparing `delfino-1.2.0/pyproject.toml` & `delfino-1.3.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "delfino"
-version = "1.2.0"
+version = "1.3.0"
 description = "A collection of command line helper scripts wrapping tools used during Python development."
 authors = ["Radek Lát <radek.lat@gmail.com>"]
 license = "MIT License"
 readme = "README.md"
 homepage = "https://github.com/radeklat/delfino"
 classifiers = [
     "Development Status :: 4 - Beta",
```

### Comparing `delfino-1.2.0/src/delfino/click_utils/command.py` & `delfino-1.3.0/src/delfino/click_utils/command.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 import logging
 import sys
 from dataclasses import dataclass
 from functools import partial
 from importlib import import_module, resources
 from importlib.resources import Package
 from pathlib import Path
-from typing import Dict, Iterator, List, Mapping, Optional, Set, cast
+from typing import Dict, Iterable, Iterator, List, Mapping, Optional, Set, cast
 
 import click
 from pydantic import BaseModel, Field, validator
 
-from delfino.constants import DEFAULT_LOCAL_COMMANDS_DIRECTORY, PYPROJECT_TOML_FILENAME
+from delfino.constants import DEFAULT_LOCAL_COMMAND_FOLDERS, PYPROJECT_TOML_FILENAME
 from delfino.models.pyproject_toml import PluginConfig
 
 if sys.version_info < (3, 10):
     # `importlib.metadata` available since 3.8 but `distribution.entry_points.select` only since 3.10
     from importlib_metadata import distributions
 else:
     from importlib.metadata import distributions
@@ -125,18 +125,18 @@
     TYPE_OF_PLUGIN = "delfino.plugin"
     LOCAL_PLUGIN_NAME = "local"
 
     def __init__(
         self,
         plugins_configs: Dict[str, PluginConfig],
         command_packages: Optional[List[_CommandPackage]] = None,
-        local_commands_directory: Path = DEFAULT_LOCAL_COMMANDS_DIRECTORY,
+        local_command_folders: Iterable[Path] = DEFAULT_LOCAL_COMMAND_FOLDERS,
     ):
         if command_packages is None:
-            self._command_packages = self._default_command_packages(plugins_configs, local_commands_directory)
+            self._command_packages = self._default_command_packages(plugins_configs, local_command_folders)
         else:
             self._command_packages = command_packages
         self._visible_commands: Dict[str, _Command] = {}
         self._hidden_commands: Dict[str, _Command] = {}
         self._register_packages()
 
     def __len__(self) -> int:
@@ -154,25 +154,28 @@
 
     @property
     def hidden_commands(self) -> List[_Command]:
         return list(self._hidden_commands.values())
 
     @classmethod
     def _default_command_packages(
-        cls, plugins_configs: Dict[str, PluginConfig], local_commands_directory: Path
+        cls, plugins_configs: Dict[str, PluginConfig], local_command_folders: Iterable[Path]
     ) -> List[_CommandPackage]:
         # This is a function to lazy load packages in tests. They may not exist on import of the code.
         return [
             # Lower priority - discovered installed packages
             *cls._discover_command_packages(plugins_configs),
             # Higher priority - locally available packages
-            _CommandPackage(
-                plugin_name=cls.LOCAL_PLUGIN_NAME,
-                package=str(local_commands_directory),
-                plugin_config=plugins_configs.get(cls.LOCAL_PLUGIN_NAME, PluginConfig.empty()),
+            *(
+                _CommandPackage(
+                    plugin_name=cls.LOCAL_PLUGIN_NAME,
+                    package=str(local_commands_folder),
+                    plugin_config=plugins_configs.get(cls.LOCAL_PLUGIN_NAME, PluginConfig.empty()),
+                )
+                for local_commands_folder in local_command_folders
             ),
         ]
 
     @classmethod
     def _discover_command_packages(cls, plugins_configs: Dict[str, PluginConfig]) -> List[_CommandPackage]:
         """Discover packages from plugin. It is using package metadata as plugin discovering solution.
```

### Comparing `delfino-1.2.0/src/delfino/click_utils/command_groups.py` & `delfino-1.3.0/src/delfino/click_utils/command_groups.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/click_utils/set_from_config.py` & `delfino-1.3.0/src/delfino/click_utils/set_from_config.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/config.py` & `delfino-1.3.0/src/delfino/config.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/decorators/files_folders.py` & `delfino-1.3.0/src/delfino/decorators/files_folders.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/decorators/pass_app_context.py` & `delfino-1.3.0/src/delfino/decorators/pass_app_context.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/decorators/pass_args.py` & `delfino-1.3.0/src/delfino/decorators/pass_args.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/execution.py` & `delfino-1.3.0/src/delfino/execution.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/internal_parameters/completion.py` & `delfino-1.3.0/src/delfino/internal_parameters/completion.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/internal_parameters/verbosity.py` & `delfino-1.3.0/src/delfino/internal_parameters/verbosity.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/main.py` & `delfino-1.3.0/src/delfino/main.py`

 * *Files 2% similar despite different names*

```diff
@@ -33,15 +33,15 @@
             self._pyproject_toml = load_config(self._project_root)
         except ConfigValidationError as exc:
             self._pyproject_toml = PyprojectToml()
             self._pyproject_toml_validation_error = exc
 
         self._command_registry = CommandRegistry(
             plugins_configs=self._pyproject_toml.tool.delfino.plugins,
-            local_commands_directory=self._pyproject_toml.tool.delfino.local_commands_directory,
+            local_command_folders=self._pyproject_toml.tool.delfino.local_command_folders,
         )
 
     def list_commands(self, ctx: click.Context) -> List[str]:
         """Override as MultiCommand always returns []."""
         del ctx
         return sorted(command.name for command in self._command_registry.visible_commands)
```

### Comparing `delfino-1.2.0/src/delfino/models/app_context.py` & `delfino-1.3.0/src/delfino/models/app_context.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/models/pyproject_toml.py` & `delfino-1.3.0/src/delfino/models/pyproject_toml.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from pathlib import Path
-from typing import Any, Dict, List, Optional, Set
+from typing import Any, Dict, List, Optional, Set, Tuple
+from warnings import warn
 
 from pydantic import BaseModel, Extra, Field
 
-from delfino.constants import DEFAULT_LOCAL_COMMANDS_DIRECTORY
+from delfino.constants import DEFAULT_LOCAL_COMMAND_FOLDERS
 
 
 class PluginConfig(BaseModel):
     enable_commands: Set[str] = Field(default_factory=set)
     disable_commands: Set[str] = Field(default_factory=set)
     command_groups: Dict[str, List[str]] = Field(default_factory=dict)
 
@@ -16,18 +17,26 @@
         return cls()
 
     class Config:
         extra = Extra.allow  # Allows arbitrary plugin-specific keys
 
 
 class Delfino(BaseModel):
-    local_commands_directory: Path = DEFAULT_LOCAL_COMMANDS_DIRECTORY
+    local_command_folders: Tuple[Path, ...] = DEFAULT_LOCAL_COMMAND_FOLDERS
     plugins: Dict[str, PluginConfig] = Field(default_factory=dict)
     command_groups: Dict[str, List[str]] = Field(default_factory=dict)
 
+    @property
+    def local_commands_directory(self) -> Path:
+        warn(
+            "tool.delfino.local_commands_directory is deprecated. Use tool.delfino.local_command_folders instead.",
+            DeprecationWarning,
+        )
+        return self.local_command_folders[0]
+
     class Config:
         extra = Extra.allow
 
 
 class Poetry(BaseModel):
     name: str
     version: str
```

### Comparing `delfino-1.2.0/src/delfino/terminal_output.py` & `delfino-1.3.0/src/delfino/terminal_output.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/utils.py` & `delfino-1.3.0/src/delfino/utils.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/src/delfino/validation.py` & `delfino-1.3.0/src/delfino/validation.py`

 * *Files identical despite different names*

### Comparing `delfino-1.2.0/setup.py` & `delfino-1.3.0/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -24,17 +24,17 @@
 {':python_version < "3.10"': ['importlib-metadata']}
 
 entry_points = \
 {'console_scripts': ['delfino = delfino.main:main', 'mike = delfino.main:main']}
 
 setup_kwargs = {
     'name': 'delfino',
-    'version': '1.2.0',
+    'version': '1.3.0',
     'description': 'A collection of command line helper scripts wrapping tools used during Python development.',
-    'long_description': '<h1 align="center" style="border-bottom: none;">🧰&nbsp;&nbsp;Delfino&nbsp;&nbsp;🧰</h1>\n<h3 align="center">Plugable Click command finder/loader/executor.</h3>\n\n<p align="center">\n    <a href="https://app.circleci.com/pipelines/github/radeklat/delfino?branch=main">\n        <img alt="CircleCI" src="https://img.shields.io/circleci/build/github/radeklat/delfino">\n    </a>\n    <a href="https://app.codecov.io/gh/radeklat/delfino/">\n        <img alt="Codecov" src="https://img.shields.io/codecov/c/github/radeklat/delfino">\n    </a>\n    <a href="https://github.com/radeklat/delfino/tags">\n        <img alt="GitHub tag (latest SemVer)" src="https://img.shields.io/github/tag/radeklat/delfino">\n    </a>\n    <img alt="Maintenance" src="https://img.shields.io/maintenance/yes/2023">\n    <a href="https://github.com/radeklat/delfino/commits/main">\n        <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/radeklat/delfino">\n    </a>\n    <a href="https://www.python.org/doc/versions/">\n        <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/delfino">\n    </a>\n    <a href="https://pypistats.org/packages/delfino">\n        <img alt="Downloads" src="https://img.shields.io/pypi/dm/delfino">\n    </a>\n</p>\n\n<!--\n    How to generate TOC from PyCharm:\n    https://github.com/vsch/idea-multimarkdown/wiki/Table-of-Contents-Extension\n-->\n[TOC levels=1,2 markdown formatted bullet hierarchy]: # "Table of content"\n\n# Table of content\n- [What is Delfino](#what-is-delfino)\n  - [Plugins](#plugins)\n- [Installation](#installation)\n- [Configuration](#configuration)\n  - [Enabling a plugin](#enabling-a-plugin)\n  - [Enabling/disabling commands](#enablingdisabling-commands)\n- [Usage](#usage)\n- [Development](#development)\n  - [Commands discovery](#commands-discovery)\n  - [Minimal command](#minimal-command)\n  - [Minimal plugin](#minimal-plugin)\n- [Advanced usage](#advanced-usage)\n  - [Auto-completion](#auto-completion)\n  - [Running external programs](#running-external-programs)\n  - [Optional dependencies](#optional-dependencies)\n  - [Project settings](#project-settings)\n  - [Plugin settings](#plugin-settings)\n  - [Project specific overrides](#project-specific-overrides)\n  - [Grouping commands](#grouping-commands)\n\n# What is Delfino\n\nDelfino is a wrapper around [Click](https://click.palletsprojects.com) command line scripts. It automatically discovers instances of [Click commands](https://click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command) and offers them for execution. However, the biggest power comes from the possibility of creating [plugins](#plugins), which can be distributed as standard Python packages.\n\n## Plugins\n\nPlugins can greatly reduce code duplication and/or promote your own standards in multiple places. For example, you can create a plugin wrapping common linting tools that you use on your projects, including their default configuration. Keeping the rules and creating new projects with the same style suddenly becomes a matter of installing one Python library.\n\nEach plugin can contain one or more Click commands that are automatically discovered and exposed by Delfino. See [`delfino-demo`](https://github.com/radeklat/delfino-demo) for a minimal plugin, which provide a `demo` command printing out a message.\n\nExisting plugins:\n\n| Plugin name                                                  | Description                                                                                        |\n|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|\n| [delfino-demo](https://github.com/radeklat/delfino-demo)     | A minimal plugin example for Delfino. Contains one command printing a message.                     |\n| [delfino-core](https://github.com/radeklat/delfino-core)     | Commands wrapping tools used during every day development (linting, testing, dependencies update). |\n| [delfino-docker](https://github.com/radeklat/delfino-docker) | Docker build helper script.                                                                        |\n\n# Installation\n\n- pip: `pip install delfino`\n- Poetry: `poetry add --group=dev delfino`\n- Pipenv: `pipenv install -d delfino`\n\nor \n\n- pip: `pip install delfino[completion]`\n- Poetry: `poetry add --group=dev delfino[completion]`\n- Pipenv: `pipenv install -d delfino[completion]`\n\nto enable [auto-completion](#auto-completion).\n\n# Configuration\n\nAll configuration is expected to live in one of the following files:\n\n- `pyproject.toml` in the project root\n- `.pylintrc` in the project root - to allow dev specific config, not source controlled or for non-Python projects\n- `.pylintrc` in the user home directory - for user tools available in the system\n\nIf multiple files are discovered, only the highest one in the list will be used.\n\nThe format for `.pylintrc` is the same as for `pyproject.toml`.\n\n## Enabling a plugin\n\nFor security reasons, plugins are disabled by default. To enable a plugin, you have to include it in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN_NAME>]\n```\n\n## Enabling/disabling commands\n\nBy default, all commands are enabled. Use `enable_commands` or `disable_commands`  to show only a subset of commands. If both used, disabled commands are subtracted from the set of enabled commands.\n\n```toml\n# [tool.delfino.plugins.<PLUGIN_NAME_A>]\n# enable_commands = [<COMMAND_NAME>]\n# disable_commands = [<COMMAND_NAME>]\n\n# [tool.delfino.plugins.<PLUGIN_NAME_B>]\n# enable_commands = [<COMMAND_NAME>]\n# disable_commands = [<COMMAND_NAME>]\n```\n\n# Usage\n\nRun `delfino --help` to see all available commands and their usage.\n\n# Development\n\nDelfino is a simple wrapper around [Click commands](https://click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command). Any Click command will be accepted by Delfino.\n\n## Commands discovery\n\nDelfino looks for any [`click.Command`](https://click.palletsprojects.com/en/8.0.x/api/#click.Command) sub-class in the following locations:\n\n- `commands` folder in the root of the project (next to the `pyproject.toml` file). This location is useful for commands that don\'t need to be replicated in multiple locations/projects.\n- python module import path (`<IMPORT_PATH>`) specified by `entry_point` of [a plugin](#minimal-plugin):\n  ```toml\n  [tool.poetry.plugins] # Optional super table\n\n  [tool.poetry.plugins."delfino.plugin"]\n  "delfino-<PLUGIN_NAME>" = "<IMPORT_PATH>"\n  ```\n\nAny files starting with an underscore, except for `__init__.py`, will be ignored.\n\n> **Warning**\n> Folders are NOT inspected recursively. If you place any commands into nested folders, they will not be loaded by Delfino.\n\n\n## Minimal command\n\n<!-- TODO(Radek): Delfino expects `pyproject.toml` configured. -->\n<!-- TODO(Radek): Delfino expects Poetry or Pipenv to be available. -->\n\n1. Create a `commands` folder:\n   ```shell script\n   mkdir commands\n   ```\n2. Create a `commands/__init__.py` file, with the following content:\n   ```python\n   import click\n   \n   @click.command()\n   def command_test():\n       """Tests commands placed in the `commands` folder are loaded."""\n       print("✨ This command works! ✨")\n   ```\n3. See if Delfino loads the command. Open a terminal and in the root of the project, call: `delfino --help`. You should see something like this:\n   ```text\n   Usage: delfino [OPTIONS] COMMAND [ARGS]...\n   \n   Options:\n     --help  Show this message and exit.\n   \n   Commands:\n     ...\n     command-test            Tests commands placed in the `commands` folder...\n     ...\n   ```\n4. Run the command with `delfino command-test`\n\n## Minimal plugin\n\nIf you\'d like to use one or more commands in multiple places, you can create a plugin. A plugin is just a regular Python package with specific entry point telling Delfino it should use it. It can also be distributed as any other Python packages, for example via Pypi.\n\nThe quickest way to create one is to use a [Delfino plugin cookiecutter template](https://github.com/radeklat/delfino-plugin-cookiecutter-template), which asks you several questions and sets up the whole project.\n\nAlternatively, you can get inspired by [the demo plugin](https://github.com/radeklat/delfino-demo) or any of the other [existing plugins](#plugins).\n\n# Advanced usage\n\n<!--\n## Advanced Command\n\nDelfino adds optional bits of functionality on top of Click. The following example demonstrates some of those:\n\n```python\n# commands/__init__.py\n\nimport click\n\nfrom delfino.contexts import pass_app_context, AppContext\nfrom delfino.validation import assert_pip_package_installed, pyproject_toml_key_missing\n\n@click.command()\n# The `pass_app_context` decorator adds `AppContext` as the first parameter.\n@pass_app_context\ndef command_test(app_context: AppContext):\n   """Tests commands placed in the `commands` folder are loaded."""\n   # Test optional dependencies. Any failing assertion will be printed as:\n   # Command \'<NAME>\' is misconfigured. <ASSERTION ERROR MESSAGE>\n   assert_pip_package_installed("delfino")\n\n   # AppContext contain a parsed `pyproject.toml` file.\n   # Commands can add their config under `[tool.delfino.commands.<COMMAND_NAME>]`.\n   assert "command_test" in app_context.pyproject_toml.tool.delfino.commands, \\\n       pyproject_toml_key_missing("tool.delfino.commands.command_test")\n\n   print(app_context.pyproject_toml.tool.delfino.commands["command-test"])\n```\n-->\n\n## Auto-completion\n\nYou can either attempt to install completions automatically with:\n\n```shell script\ndelfino --install-completion\n```\n\nor generate it with:\n\n```shell script\ndelfino --show-completion\n```\n\nand manually put it in the relevant RC file.\n\nThe auto-completion implementation is dynamic so that every time it is invoked, it uses the current project. Each project can have different commands or disable certain commands it doesn\'t use. And dynamic auto-completion makes sure only the currently available commands will be suggested.\n\nThe downside of this approach is that evaluating what is available each time is slower than a static list of commands.\n\n## Running external programs\n\nIt is up to you how you want to execute external processes as part of commands (if you need to at all). A common way in Python is to use `subprocess.run`. Delfino comes with its own [`run` implementation](https://github.com/radeklat/delfino/blob/main/src/delfino/execution.py#L94), which wraps and simplifies `subprocess.run` for the most common use cases:\n\n- Normalizing `subprocess.run` arguments - you can pass in either a string or a list. Either way, `subprocess.run` will be executed correctly.\n- Handling errors from the execution via the `on_error` argument. Giving the option to either ignore the errors and continue (`PASS`), not continue and clean exit (`EXIT`) or not continue and abort with error code (`ABORT`).\n- Setting environment variables.\n- Logging what is being executed in the debug level.\n\nExample:\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.execution import run, OnError\n\n@click.command()\ndef test():\n    run("pytest tests", on_error=OnError.ABORT)\n```\n\n## Optional dependencies\n\nIf you put several commands into one [plugin](#plugins), you can make some dependencies of some commands [optional](https://python-poetry.org/docs/pyproject#extras). This is useful when a command is not always used, and you don\'t want to install unnecessary dependencies. Instead, you can check if a dependency is installed only when the command is executed with `delfino.validation.assert_pip_package_installed`:\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.validation import assert_pip_package_installed\n\ntry:\n    from git import Repo\nexcept ImportError:\n    pass\n\n@click.command()\ndef git_active_branch():\n    assert_pip_package_installed("gitpython")\n    print(Repo(".").active_branch)\n```\n\nIn the example above, if `gitpython` is not installed, delfino will show the command but will fail with suggestion to install `gitpython` only when the command is executed. You can also add `git_active_branch` into [`disable_commands` config](#enablingdisabling-commands) in places where you don\'t intend to use it.\n\nThis way you can greatly reduce the number of dependencies a plugin brings into a project without a need to have many small plugins.\n\n## Project settings\n\nYou can store an arbitrary object in the Click context as [`click.Context.obj`](https://click.palletsprojects.com/api/#click.Context.obj). Delfino utilizes this object to store an instance of [`AppContext`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/app_context.py), which provides access to project related information. If you need to, you can still attach arbitrary attributes to this object later.\n\nYou can pass this object to your commands by decorating them with [`click.pass_obj`](https://click.palletsprojects.com/api/#click.pass_obj):\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.models.app_context import AppContext\n\n@click.command()\n@click.pass_obj\ndef print_app_version(obj: AppContext):\n    print(obj.pyproject_toml.tool.poetry.version)\n```\n\n## Plugin settings\n\nPlugin settings are expected to live in the `pyproject.toml` file. To prevent naming conflicts, each plugin must put its settings under `tool.delfino.plugins.<PLUGIN_NAME>`. It also allows Delfino to pass these settings directly to commands from these plugins.\n\nDelfino loads, parses, validates and stores plugin settings in [`AppContext.plugin_config`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/app_context.py). If not specified otherwise (see below), it will be an instance of [`PluginConfig`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/pyproject_toml.py), with any extra keys unvalidated and in JSON-like Python objects.\n\nYou can add additional validation to your plugin settings by sub-classing the `PluginConfig` , defining expected keys, default values and/or validation. Delfino utilizes [`pydantic`](https://docs.pydantic.dev/) to create data classes.\n\nDelfino also needs to know, which class to use for the validation. To do that, switch to `delfino.decorators.pass_app_context` instead of [`click.pass_obj`](https://click.palletsprojects.com/api/#click.pass_obj):\n\n```toml\n# pyproject.toml\n\n[tool.delfino.plugins.delfino_login_plugin]\nusername = "user"\n```\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.models.pyproject_toml import PluginConfig\nfrom delfino.models.app_context import AppContext\nfrom delfino.decorators import pass_app_context\n\n\nclass LoginPluginConfig(PluginConfig):\n    login: str\n\n\n@click.command()\n@pass_app_context(LoginPluginConfig)\ndef login(app_context: AppContext[LoginPluginConfig]):\n    print(app_context.plugin_config.login)\n```\n\nThe `AppContext` class is generic. Defining the `PluginConfigType` (such as `AppContext[LoginPluginConfig]` in the example above) enables introspection and type checks.\n\n## Project specific overrides\n\nIt is likely your projects will require slight divergence to the defaults you encode in your scripts. The following sections cover the most common use cases.\n\n### Pass-through arguments\n\nYou can pass additional arguments to downstream tools by decorating commands with the [`decorators.pass_args`](https://github.com/radeklat/delfino/blob/main/src/delfino/decorators/pass_args.py) decorator:\n\n```python\n# commands/__init__.py\n\nfrom typing import Tuple\n\nimport click\nfrom delfino.decorators import pass_args\nfrom delfino.execution import run, OnError\n\n@click.command()\n@pass_args\ndef test(passed_args: Tuple[str, ...]):\n    run(["pytest", "tests", *passed_args], on_error=OnError.ABORT)\n```\n\nThen additional arguments can be passed either via command line after `--`:\n\n```shell script\ndelfino test -- --capture=no\n```\n\nOr via configuration in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN>.test]\npass_args = [\'--capture=no\']\n```\n\nEither way, both will result in executing `pytest tests --capture=no`.\n\n### Files override\n\nYou can override files passed to downstream tools by decorating commands with the [`decorators.files_folders_option`](https://github.com/radeklat/delfino/blob/main/src/delfino/decorators/files_folders.py) decorator:\n\n```python\n# commands/__init__.py\n\nfrom typing import Tuple\n\nimport click\nfrom delfino.decorators import files_folders_option\nfrom delfino.execution import run, OnError\n\n@click.command()\n@files_folders_option\ndef test(files_folders: Tuple[str, ...]):\n    if not files_folders:\n        files_folders = ("tests/unit", "tests/integration")\n    run(["pytest", *files_folders], on_error=OnError.ABORT)\n```\n\nThen the default `"tests/unit", "tests/integration"` folders can be overridden either via command line options `-f`/`--file`/`--folder`:\n\n```shell script\ndelfino test -f tests/other\n```\n\nOr via configuration in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN>.test]\nfiles_folders = [\'tests/other\']\n```\n\nEither way, both will result in executing `pytest tests/other`.\n\n## Grouping commands\n\nOften it is useful to run several commands as a group with a different command name. Click supports calling other commands with [`click.Context.forward`](https://click.palletsprojects.com/api/#click.Context.forward) or [`click.Context.invoke`](https://click.palletsprojects.com/api/#click.Context.invoke).\n\n<!-- TODO(Radek): Add description of `execute_commands_group` once migrated from `delfino-core`. -->\n',
+    'long_description': '<h1 align="center" style="border-bottom: none;">🧰&nbsp;&nbsp;Delfino&nbsp;&nbsp;🧰</h1>\n<h3 align="center">The Ultimate Command Line Companion for Your Projects</h3>\n\n<p align="center">\n    <a href="https://app.circleci.com/pipelines/github/radeklat/delfino?branch=main">\n        <img alt="CircleCI" src="https://img.shields.io/circleci/build/github/radeklat/delfino">\n    </a>\n    <a href="https://app.codecov.io/gh/radeklat/delfino/">\n        <img alt="Codecov" src="https://img.shields.io/codecov/c/github/radeklat/delfino">\n    </a>\n    <a href="https://github.com/radeklat/delfino/tags">\n        <img alt="GitHub tag (latest SemVer)" src="https://img.shields.io/github/tag/radeklat/delfino">\n    </a>\n    <img alt="Maintenance" src="https://img.shields.io/maintenance/yes/2023">\n    <a href="https://github.com/radeklat/delfino/commits/main">\n        <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/radeklat/delfino">\n    </a>\n    <a href="https://www.python.org/doc/versions/">\n        <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/delfino">\n    </a>\n    <a href="https://pypistats.org/packages/delfino">\n        <img alt="Downloads" src="https://img.shields.io/pypi/dm/delfino">\n    </a>\n</p>\n\nTired of managing scattered scripts? Say goodbye to complexity with Delfino!\n\nDelfino is a powerful wrapper around Click, the popular command line interface package. It automatically discovers and executes Click commands in your project. But Delfino doesn\'t stop there - it takes it a step further by allowing you to create plugins, making script distribution and installation a breeze.\n\n# Why choose Delfino?\n\n- **Streamline Scripts**: Consolidate all your helper scripts into a single, easy-to-use entry point. No more hunting for scripts or dealing with convoluted aliases. Simply use delfino followed by the script name and options.\n- **Reusable Plugins**: Package your helper scripts as plugins and install them with pip. Maintain consistency across projects and easily incorporate updates through a flexible configuration system.\n- **Simplify Tooling**: Delfino extends Click with advanced features like pass-through command-line options and seamless handling of file lists. Say goodbye to verbosity and hello to optimized workflows.\n\nDon\'t let scattered scripts and complex tooling slow you down. Embrace Delfino and revolutionize your command line experience. Try Delfino today and unlock simplicity in your projects!\n\n<!--\n    How to generate TOC from PyCharm:\n    https://github.com/vsch/idea-multimarkdown/wiki/Table-of-Contents-Extension\n-->\n[TOC levels=1,2 markdown formatted bullet hierarchy]: # "Table of content"\n\n# Table of content\n- [Installation](#installation)\n- [Configuration](#configuration)\n- [Usage](#usage)\n- [Development](#development)\n  - [Commands discovery](#commands-discovery)\n  - [Minimal command](#minimal-command)\n  - [Minimal plugin](#minimal-plugin)\n- [Existing plugins](#existing-plugins)\n  - [Enabling a plugin](#enabling-a-plugin)\n  - [Enabling/disabling commands](#enablingdisabling-commands)\n- [Advanced usage](#advanced-usage)\n  - [Auto-completion](#auto-completion)\n  - [Running external programs](#running-external-programs)\n  - [Optional dependencies](#optional-dependencies)\n  - [Project settings](#project-settings)\n  - [Plugin settings](#plugin-settings)\n  - [Project specific overrides](#project-specific-overrides)\n  - [Grouping commands](#grouping-commands)\n\n# Installation\n\n- pip: `pip install delfino`\n- Poetry: `poetry add --group=dev delfino`\n- Pipenv: `pipenv install -d delfino`\n\nor \n\n- pip: `pip install delfino[completion]`\n- Poetry: `poetry add --group=dev delfino[completion]`\n- Pipenv: `pipenv install -d delfino[completion]`\n\nto enable [auto-completion](#auto-completion).\n\n# Configuration\n\nAll configuration is expected to live in one of the following files:\n\n- `pyproject.toml` in the project root\n- `.delfinorc` in the project root - to allow dev specific config, not source controlled or for non-Python projects\n- `.delfinorc` in the user home directory - for user tools available in the system\n\nIf multiple files are discovered, only the highest one in the list will be used.\n\nThe format for `.delfinorc` is the same as for `pyproject.toml`.\n\n# Usage\n\nRun `delfino --help` to see all available commands and their usage.\n\n# Development\n\nDelfino is a simple wrapper around [Click commands](https://click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command). Any Click command will be accepted by Delfino.\n\n## Commands discovery\n\nDelfino looks for any [`click.Command`](https://click.palletsprojects.com/en/8.0.x/api/#click.Command) sub-class in the following locations:\n\n- `commands` folder in the root of the project (next to the `pyproject.toml` file). This location is useful for commands that don\'t need to be replicated in multiple locations/projects. To change the default location, use the `tool.delfino.local_command_folders` config option. It allows specifying more than one folder.\n- python module import path (`<IMPORT_PATH>`) specified by `entry_point` of [a plugin](#minimal-plugin):\n  ```toml\n  [tool.poetry.plugins] # Optional super table\n\n  [tool.poetry.plugins."delfino.plugin"]\n  "delfino-<PLUGIN_NAME>" = "<IMPORT_PATH>"\n  ```\n- Folder specified in the [config file](#configuration) under `tool.delfino.local_commands_directory`.\n\nAny files starting with an underscore, except for `__init__.py`, will be ignored.\n\n> **Warning**\n> Folders are NOT inspected recursively. If you place any commands into nested folders, they will not be loaded by Delfino.\n\n\n## Minimal command\n\n<!-- TODO(Radek): Delfino expects `pyproject.toml` configured. -->\n<!-- TODO(Radek): Delfino expects Poetry or Pipenv to be available. -->\n\n1. Create a `commands` folder:\n   ```shell script\n   mkdir commands\n   ```\n2. Create a `commands/__init__.py` file, with the following content:\n   ```python\n   import click\n   \n   @click.command()\n   def command_test():\n       """Tests commands placed in the `commands` folder are loaded."""\n       print("✨ This command works! ✨")\n   ```\n3. See if Delfino loads the command. Open a terminal and in the root of the project, call: `delfino --help`. You should see something like this:\n   ```text\n   Usage: delfino [OPTIONS] COMMAND [ARGS]...\n   \n   Options:\n     --help  Show this message and exit.\n   \n   Commands:\n     ...\n     command-test            Tests commands placed in the `commands` folder...\n     ...\n   ```\n4. Run the command with `delfino command-test`\n\n## Minimal plugin\n\nIf you\'d like to use one or more commands in multiple places, you can create a plugin. A plugin is just a regular Python package with specific entry point telling Delfino it should use it. It can also be distributed as any other Python packages, for example via Pypi.\n\nThe quickest way to create one is to use a [Delfino plugin cookiecutter template](https://github.com/radeklat/delfino-plugin-cookiecutter-template), which asks you several questions and sets up the whole project.\n\nAlternatively, you can get inspired by [the demo plugin](https://github.com/radeklat/delfino-demo) or any of the other [existing plugins](#plugins).\n\n# Existing plugins\n\nPlugins can greatly reduce code duplication and/or promote your own standards in multiple places. For example, you can create a plugin wrapping common linting tools that you use on your projects, including their default configuration. Keeping the rules and creating new projects with the same style suddenly becomes a matter of installing one Python library.\n\nEach plugin can contain one or more Click commands that are automatically discovered and exposed by Delfino. See [`delfino-demo`](https://github.com/radeklat/delfino-demo) for a minimal plugin, which provide a `demo` command printing out a message.\n\nExisting plugins:\n\n| Plugin name                                                  | Description                                                                                        |\n|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|\n| [delfino-demo](https://github.com/radeklat/delfino-demo)     | A minimal plugin example for Delfino. Contains one command printing a message.                     |\n| [delfino-core](https://github.com/radeklat/delfino-core)     | Commands wrapping tools used during every day development (linting, testing, dependencies update). |\n| [delfino-docker](https://github.com/radeklat/delfino-docker) | Docker build helper script.                                                                        |\n\n## Enabling a plugin\n\nFor security reasons, plugins are disabled by default. To enable a plugin, you have to include it in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN_NAME>]\n```\n\n## Enabling/disabling commands\n\nBy default, all commands are enabled. Use `enable_commands` or `disable_commands`  to show only a subset of commands. If both used, disabled commands are subtracted from the set of enabled commands.\n\n```toml\n# [tool.delfino.plugins.<PLUGIN_NAME_A>]\n# enable_commands = [<COMMAND_NAME>]\n# disable_commands = [<COMMAND_NAME>]\n\n# [tool.delfino.plugins.<PLUGIN_NAME_B>]\n# enable_commands = [<COMMAND_NAME>]\n# disable_commands = [<COMMAND_NAME>]\n```\n\n# Advanced usage\n\n<!--\n## Advanced Command\n\nDelfino adds optional bits of functionality on top of Click. The following example demonstrates some of those:\n\n```python\n# commands/__init__.py\n\nimport click\n\nfrom delfino.contexts import pass_app_context, AppContext\nfrom delfino.validation import assert_pip_package_installed, pyproject_toml_key_missing\n\n@click.command()\n# The `pass_app_context` decorator adds `AppContext` as the first parameter.\n@pass_app_context\ndef command_test(app_context: AppContext):\n   """Tests commands placed in the `commands` folder are loaded."""\n   # Test optional dependencies. Any failing assertion will be printed as:\n   # Command \'<NAME>\' is misconfigured. <ASSERTION ERROR MESSAGE>\n   assert_pip_package_installed("delfino")\n\n   # AppContext contain a parsed `pyproject.toml` file.\n   # Commands can add their config under `[tool.delfino.commands.<COMMAND_NAME>]`.\n   assert "command_test" in app_context.pyproject_toml.tool.delfino.commands, \\\n       pyproject_toml_key_missing("tool.delfino.commands.command_test")\n\n   print(app_context.pyproject_toml.tool.delfino.commands["command-test"])\n```\n-->\n\n## Auto-completion\n\nYou can either attempt to install completions automatically with:\n\n```shell script\ndelfino --install-completion\n```\n\nor generate it with:\n\n```shell script\ndelfino --show-completion\n```\n\nand manually put it in the relevant RC file.\n\nThe auto-completion implementation is dynamic so that every time it is invoked, it uses the current project. Each project can have different commands or disable certain commands it doesn\'t use. And dynamic auto-completion makes sure only the currently available commands will be suggested.\n\nThe downside of this approach is that evaluating what is available each time is slower than a static list of commands.\n\n## Running external programs\n\nIt is up to you how you want to execute external processes as part of commands (if you need to at all). A common way in Python is to use `subprocess.run`. Delfino comes with its own [`run` implementation](https://github.com/radeklat/delfino/blob/main/src/delfino/execution.py#L94), which wraps and simplifies `subprocess.run` for the most common use cases:\n\n- Normalizing `subprocess.run` arguments - you can pass in either a string or a list. Either way, `subprocess.run` will be executed correctly.\n- Handling errors from the execution via the `on_error` argument. Giving the option to either ignore the errors and continue (`PASS`), not continue and clean exit (`EXIT`) or not continue and abort with error code (`ABORT`).\n- Setting environment variables.\n- Logging what is being executed in the debug level.\n\nExample:\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.execution import run, OnError\n\n@click.command()\ndef test():\n    run("pytest tests", on_error=OnError.ABORT)\n```\n\n## Optional dependencies\n\nIf you put several commands into one [plugin](#plugins), you can make some dependencies of some commands [optional](https://python-poetry.org/docs/pyproject#extras). This is useful when a command is not always used, and you don\'t want to install unnecessary dependencies. Instead, you can check if a dependency is installed only when the command is executed with `delfino.validation.assert_pip_package_installed`:\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.validation import assert_pip_package_installed\n\ntry:\n    from git import Repo\nexcept ImportError:\n    pass\n\n@click.command()\ndef git_active_branch():\n    assert_pip_package_installed("gitpython")\n    print(Repo(".").active_branch)\n```\n\nIn the example above, if `gitpython` is not installed, delfino will show the command but will fail with suggestion to install `gitpython` only when the command is executed. You can also add `git_active_branch` into [`disable_commands` config](#enablingdisabling-commands) in places where you don\'t intend to use it.\n\nThis way you can greatly reduce the number of dependencies a plugin brings into a project without a need to have many small plugins.\n\n## Project settings\n\nYou can store an arbitrary object in the Click context as [`click.Context.obj`](https://click.palletsprojects.com/api/#click.Context.obj). Delfino utilizes this object to store an instance of [`AppContext`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/app_context.py), which provides access to project related information. If you need to, you can still attach arbitrary attributes to this object later.\n\nYou can pass this object to your commands by decorating them with [`click.pass_obj`](https://click.palletsprojects.com/api/#click.pass_obj):\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.models.app_context import AppContext\n\n@click.command()\n@click.pass_obj\ndef print_app_version(obj: AppContext):\n    print(obj.pyproject_toml.tool.poetry.version)\n```\n\n## Plugin settings\n\nPlugin settings are expected to live in the `pyproject.toml` file. To prevent naming conflicts, each plugin must put its settings under `tool.delfino.plugins.<PLUGIN_NAME>`. It also allows Delfino to pass these settings directly to commands from these plugins.\n\nDelfino loads, parses, validates and stores plugin settings in [`AppContext.plugin_config`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/app_context.py). If not specified otherwise (see below), it will be an instance of [`PluginConfig`](https://github.com/radeklat/delfino/blob/main/src/delfino/models/pyproject_toml.py), with any extra keys unvalidated and in JSON-like Python objects.\n\nYou can add additional validation to your plugin settings by sub-classing the `PluginConfig` , defining expected keys, default values and/or validation. Delfino utilizes [`pydantic`](https://docs.pydantic.dev/) to create data classes.\n\nDelfino also needs to know, which class to use for the validation. To do that, switch to `delfino.decorators.pass_app_context` instead of [`click.pass_obj`](https://click.palletsprojects.com/api/#click.pass_obj):\n\n```toml\n# pyproject.toml\n\n[tool.delfino.plugins.delfino_login_plugin]\nusername = "user"\n```\n\n```python\n# commands/__init__.py\n\nimport click\nfrom delfino.models.pyproject_toml import PluginConfig\nfrom delfino.models.app_context import AppContext\nfrom delfino.decorators import pass_app_context\n\n\nclass LoginPluginConfig(PluginConfig):\n    login: str\n\n\n@click.command()\n@pass_app_context(LoginPluginConfig)\ndef login(app_context: AppContext[LoginPluginConfig]):\n    print(app_context.plugin_config.login)\n```\n\nThe `AppContext` class is generic. Defining the `PluginConfigType` (such as `AppContext[LoginPluginConfig]` in the example above) enables introspection and type checks.\n\n## Project specific overrides\n\nIt is likely your projects will require slight divergence to the defaults you encode in your scripts. The following sections cover the most common use cases.\n\n### Pass-through arguments\n\nYou can pass additional arguments to downstream tools by decorating commands with the [`decorators.pass_args`](https://github.com/radeklat/delfino/blob/main/src/delfino/decorators/pass_args.py) decorator:\n\n```python\n# commands/__init__.py\n\nfrom typing import Tuple\n\nimport click\nfrom delfino.decorators import pass_args\nfrom delfino.execution import run, OnError\n\n@click.command()\n@pass_args\ndef test(passed_args: Tuple[str, ...]):\n    run(["pytest", "tests", *passed_args], on_error=OnError.ABORT)\n```\n\nThen additional arguments can be passed either via command line after `--`:\n\n```shell script\ndelfino test -- --capture=no\n```\n\nOr via configuration in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN>.test]\npass_args = [\'--capture=no\']\n```\n\nEither way, both will result in executing `pytest tests --capture=no`.\n\n### Files override\n\nYou can override files passed to downstream tools by decorating commands with the [`decorators.files_folders_option`](https://github.com/radeklat/delfino/blob/main/src/delfino/decorators/files_folders.py) decorator:\n\n```python\n# commands/__init__.py\n\nfrom typing import Tuple\n\nimport click\nfrom delfino.decorators import files_folders_option\nfrom delfino.execution import run, OnError\n\n@click.command()\n@files_folders_option\ndef test(files_folders: Tuple[str, ...]):\n    if not files_folders:\n        files_folders = ("tests/unit", "tests/integration")\n    run(["pytest", *files_folders], on_error=OnError.ABORT)\n```\n\nThen the default `"tests/unit", "tests/integration"` folders can be overridden either via command line options `-f`/`--file`/`--folder`:\n\n```shell script\ndelfino test -f tests/other\n```\n\nOr via configuration in the `pyproject.toml` file:\n\n```toml\n[tool.delfino.plugins.<PLUGIN>.test]\nfiles_folders = [\'tests/other\']\n```\n\nEither way, both will result in executing `pytest tests/other`.\n\n## Grouping commands\n\nOften it is useful to run several commands as a group with a different command name. Click supports calling other commands with [`click.Context.forward`](https://click.palletsprojects.com/api/#click.Context.forward) or [`click.Context.invoke`](https://click.palletsprojects.com/api/#click.Context.invoke).\n\n<!-- TODO(Radek): Add description of `execute_commands_group` once migrated from `delfino-core`. -->\n',
     'author': 'Radek Lát',
     'author_email': 'radek.lat@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/radeklat/delfino',
     'package_dir': package_dir,
     'packages': packages,
```

#### html2text {}

```diff
@@ -1,116 +1,130 @@
 # -*- coding: utf-8 -*- from setuptools import setup package_dir = \ {'':
 'src'} packages = \ ['delfino', 'delfino.click_utils', 'delfino.decorators',
 'delfino.internal_parameters', 'delfino.models'] package_data = \ {'': ['*']}
 install_requires = \ ['click>=8.0,<9.0', 'deprecation>=2.1,<3.0',
 'pydantic>=1.8,<2.0', 'toml>=0.10,<0.11'] extras_require = \ {':python_version
 < "3.10"': ['importlib-metadata']} entry_points = \ {'console_scripts':
 ['delfino = delfino.main:main', 'mike = delfino.main:main']} setup_kwargs =
-{ 'name': 'delfino', 'version': '1.2.0', 'description': 'A collection of
+{ 'name': 'delfino', 'version': '1.3.0', 'description': 'A collection of
 command line helper scripts wrapping tools used during Python development.',
 'long_description': '
                        ****** ð§°  Delfino  ð§° ******
 \n
-           **** Plugable Click command finder/loader/executor. ****
+        **** The Ultimate Command Line Companion for Your Projects ****
 \n\n
   \n \n_[CircleCI]\n\n \n_[Codecov]\n\n \n_[GitHub_tag_(latest_SemVer)]\n\n
 [Maintenance]\n \n_[GitHub_last_commit]\n\n \n_[PyPI_-_Python_Version]\n\n \n_
                                 [Downloads]\n\n
-\n\n\n[TOC levels=1,2 markdown formatted bullet hierarchy]: # "Table of
-content"\n\n# Table of content\n- [What is Delfino](#what-is-delfino)\n -
-[Plugins](#plugins)\n- [Installation](#installation)\n- [Configuration]
-(#configuration)\n - [Enabling a plugin](#enabling-a-plugin)\n - [Enabling/
-disabling commands](#enablingdisabling-commands)\n- [Usage](#usage)\n-
-[Development](#development)\n - [Commands discovery](#commands-discovery)\n -
-[Minimal command](#minimal-command)\n - [Minimal plugin](#minimal-plugin)\n-
-[Advanced usage](#advanced-usage)\n - [Auto-completion](#auto-completion)\n -
-[Running external programs](#running-external-programs)\n - [Optional
-dependencies](#optional-dependencies)\n - [Project settings](#project-
-settings)\n - [Plugin settings](#plugin-settings)\n - [Project specific
-overrides](#project-specific-overrides)\n - [Grouping commands](#grouping-
-commands)\n\n# What is Delfino\n\nDelfino is a wrapper around [Click](https://
-click.palletsprojects.com) command line scripts. It automatically discovers
-instances of [Click commands](https://click.palletsprojects.com/quickstart/
-#basic-concepts-creating-a-command) and offers them for execution. However, the
-biggest power comes from the possibility of creating [plugins](#plugins), which
-can be distributed as standard Python packages.\n\n## Plugins\n\nPlugins can
-greatly reduce code duplication and/or promote your own standards in multiple
-places. For example, you can create a plugin wrapping common linting tools that
-you use on your projects, including their default configuration. Keeping the
-rules and creating new projects with the same style suddenly becomes a matter
-of installing one Python library.\n\nEach plugin can contain one or more Click
-commands that are automatically discovered and exposed by Delfino. See
-[`delfino-demo`](https://github.com/radeklat/delfino-demo) for a minimal
-plugin, which provide a `demo` command printing out a message.\n\nExisting
-plugins:\n\n| Plugin name | Description |\n|:----------------------------------
----------------------------|:--------------------------------------------------
--------------------------------------------------|\n| [delfino-demo](https://
-github.com/radeklat/delfino-demo) | A minimal plugin example for Delfino.
-Contains one command printing a message. |\n| [delfino-core](https://
-github.com/radeklat/delfino-core) | Commands wrapping tools used during every
-day development (linting, testing, dependencies update). |\n| [delfino-docker]
-(https://github.com/radeklat/delfino-docker) | Docker build helper script.
-|\n\n# Installation\n\n- pip: `pip install delfino`\n- Poetry: `poetry add --
-group=dev delfino`\n- Pipenv: `pipenv install -d delfino`\n\nor \n\n- pip: `pip
-install delfino[completion]`\n- Poetry: `poetry add --group=dev delfino
-[completion]`\n- Pipenv: `pipenv install -d delfino[completion]`\n\nto enable
-[auto-completion](#auto-completion).\n\n# Configuration\n\nAll configuration is
-expected to live in one of the following files:\n\n- `pyproject.toml` in the
-project root\n- `.pylintrc` in the project root - to allow dev specific config,
-not source controlled or for non-Python projects\n- `.pylintrc` in the user
-home directory - for user tools available in the system\n\nIf multiple files
-are discovered, only the highest one in the list will be used.\n\nThe format
-for `.pylintrc` is the same as for `pyproject.toml`.\n\n## Enabling a
-plugin\n\nFor security reasons, plugins are disabled by default. To enable a
-plugin, you have to include it in the `pyproject.toml` file:\n\n```toml\n
-[tool.delfino.plugins.]\n```\n\n## Enabling/disabling commands\n\nBy default,
-all commands are enabled. Use `enable_commands` or `disable_commands` to show
-only a subset of commands. If both used, disabled commands are subtracted from
-the set of enabled commands.\n\n```toml\n# [tool.delfino.plugins.]\n#
-enable_commands = []\n# disable_commands = []\n\n# [tool.delfino.plugins.]\n#
-enable_commands = []\n# disable_commands = []\n```\n\n# Usage\n\nRun `delfino -
--help` to see all available commands and their usage.\n\n#
+\n\nTired of managing scattered scripts? Say goodbye to complexity with
+Delfino!\n\nDelfino is a powerful wrapper around Click, the popular command
+line interface package. It automatically discovers and executes Click commands
+in your project. But Delfino doesn\'t stop there - it takes it a step further
+by allowing you to create plugins, making script distribution and installation
+a breeze.\n\n# Why choose Delfino?\n\n- **Streamline Scripts**: Consolidate all
+your helper scripts into a single, easy-to-use entry point. No more hunting for
+scripts or dealing with convoluted aliases. Simply use delfino followed by the
+script name and options.\n- **Reusable Plugins**: Package your helper scripts
+as plugins and install them with pip. Maintain consistency across projects and
+easily incorporate updates through a flexible configuration system.\n-
+**Simplify Tooling**: Delfino extends Click with advanced features like pass-
+through command-line options and seamless handling of file lists. Say goodbye
+to verbosity and hello to optimized workflows.\n\nDon\'t let scattered scripts
+and complex tooling slow you down. Embrace Delfino and revolutionize your
+command line experience. Try Delfino today and unlock simplicity in your
+projects!\n\n\n[TOC levels=1,2 markdown formatted bullet hierarchy]: # "Table
+of content"\n\n# Table of content\n- [Installation](#installation)\n-
+[Configuration](#configuration)\n- [Usage](#usage)\n- [Development]
+(#development)\n - [Commands discovery](#commands-discovery)\n - [Minimal
+command](#minimal-command)\n - [Minimal plugin](#minimal-plugin)\n- [Existing
+plugins](#existing-plugins)\n - [Enabling a plugin](#enabling-a-plugin)\n -
+[Enabling/disabling commands](#enablingdisabling-commands)\n- [Advanced usage]
+(#advanced-usage)\n - [Auto-completion](#auto-completion)\n - [Running external
+programs](#running-external-programs)\n - [Optional dependencies](#optional-
+dependencies)\n - [Project settings](#project-settings)\n - [Plugin settings]
+(#plugin-settings)\n - [Project specific overrides](#project-specific-
+overrides)\n - [Grouping commands](#grouping-commands)\n\n# Installation\n\n-
+pip: `pip install delfino`\n- Poetry: `poetry add --group=dev delfino`\n-
+Pipenv: `pipenv install -d delfino`\n\nor \n\n- pip: `pip install delfino
+[completion]`\n- Poetry: `poetry add --group=dev delfino[completion]`\n-
+Pipenv: `pipenv install -d delfino[completion]`\n\nto enable [auto-completion]
+(#auto-completion).\n\n# Configuration\n\nAll configuration is expected to live
+in one of the following files:\n\n- `pyproject.toml` in the project root\n-
+`.delfinorc` in the project root - to allow dev specific config, not source
+controlled or for non-Python projects\n- `.delfinorc` in the user home
+directory - for user tools available in the system\n\nIf multiple files are
+discovered, only the highest one in the list will be used.\n\nThe format for
+`.delfinorc` is the same as for `pyproject.toml`.\n\n# Usage\n\nRun `delfino --
+help` to see all available commands and their usage.\n\n#
 Development\n\nDelfino is a simple wrapper around [Click commands](https://
 click.palletsprojects.com/quickstart/#basic-concepts-creating-a-command). Any
 Click command will be accepted by Delfino.\n\n## Commands discovery\n\nDelfino
 looks for any [`click.Command`](https://click.palletsprojects.com/en/8.0.x/api/
 #click.Command) sub-class in the following locations:\n\n- `commands` folder in
 the root of the project (next to the `pyproject.toml` file). This location is
 useful for commands that don\'t need to be replicated in multiple locations/
-projects.\n- python module import path (``) specified by `entry_point` of [a
-plugin](#minimal-plugin):\n ```toml\n [tool.poetry.plugins] # Optional super
-table\n\n [tool.poetry.plugins."delfino.plugin"]\n "delfino-" = ""\n ```\n\nAny
-files starting with an underscore, except for `__init__.py`, will be
-ignored.\n\n> **Warning**\n> Folders are NOT inspected recursively. If you
-place any commands into nested folders, they will not be loaded by
-Delfino.\n\n\n## Minimal command\n\n\n\n\n1. Create a `commands` folder:\n
-```shell script\n mkdir commands\n ```\n2. Create a `commands/__init__.py`
-file, with the following content:\n ```python\n import click\n \n
-@click.command()\n def command_test():\n """Tests commands placed in the
-`commands` folder are loaded."""\n print("â¨ This command works! â¨")\n
-```\n3. See if Delfino loads the command. Open a terminal and in the root of
-the project, call: `delfino --help`. You should see something like this:\n
-```text\n Usage: delfino [OPTIONS] COMMAND [ARGS]...\n \n Options:\n --help
-Show this message and exit.\n \n Commands:\n ...\n command-test Tests commands
-placed in the `commands` folder...\n ...\n ```\n4. Run the command with
-`delfino command-test`\n\n## Minimal plugin\n\nIf you\'d like to use one or
-more commands in multiple places, you can create a plugin. A plugin is just a
-regular Python package with specific entry point telling Delfino it should use
-it. It can also be distributed as any other Python packages, for example via
-Pypi.\n\nThe quickest way to create one is to use a [Delfino plugin
-cookiecutter template](https://github.com/radeklat/delfino-plugin-cookiecutter-
-template), which asks you several questions and sets up the whole
-project.\n\nAlternatively, you can get inspired by [the demo plugin](https://
-github.com/radeklat/delfino-demo) or any of the other [existing plugins]
-(#plugins).\n\n# Advanced usage\n\n\n\n## Auto-completion\n\nYou can either
-attempt to install completions automatically with:\n\n```shell script\ndelfino
---install-completion\n```\n\nor generate it with:\n\n```shell script\ndelfino -
--show-completion\n```\n\nand manually put it in the relevant RC file.\n\nThe
-auto-completion implementation is dynamic so that every time it is invoked, it
-uses the current project. Each project can have different commands or disable
+projects. To change the default location, use the
+`tool.delfino.local_command_folders` config option. It allows specifying more
+than one folder.\n- python module import path (``) specified by `entry_point`
+of [a plugin](#minimal-plugin):\n ```toml\n [tool.poetry.plugins] # Optional
+super table\n\n [tool.poetry.plugins."delfino.plugin"]\n "delfino-" = ""\n
+```\n- Folder specified in the [config file](#configuration) under
+`tool.delfino.local_commands_directory`.\n\nAny files starting with an
+underscore, except for `__init__.py`, will be ignored.\n\n> **Warning**\n>
+Folders are NOT inspected recursively. If you place any commands into nested
+folders, they will not be loaded by Delfino.\n\n\n## Minimal
+command\n\n\n\n\n1. Create a `commands` folder:\n ```shell script\n mkdir
+commands\n ```\n2. Create a `commands/__init__.py` file, with the following
+content:\n ```python\n import click\n \n @click.command()\n def command_test():
+\n """Tests commands placed in the `commands` folder are loaded."""\n print
+("â¨ This command works! â¨")\n ```\n3. See if Delfino loads the command.
+Open a terminal and in the root of the project, call: `delfino --help`. You
+should see something like this:\n ```text\n Usage: delfino [OPTIONS] COMMAND
+[ARGS]...\n \n Options:\n --help Show this message and exit.\n \n Commands:\n
+...\n command-test Tests commands placed in the `commands` folder...\n ...\n
+```\n4. Run the command with `delfino command-test`\n\n## Minimal plugin\n\nIf
+you\'d like to use one or more commands in multiple places, you can create a
+plugin. A plugin is just a regular Python package with specific entry point
+telling Delfino it should use it. It can also be distributed as any other
+Python packages, for example via Pypi.\n\nThe quickest way to create one is to
+use a [Delfino plugin cookiecutter template](https://github.com/radeklat/
+delfino-plugin-cookiecutter-template), which asks you several questions and
+sets up the whole project.\n\nAlternatively, you can get inspired by [the demo
+plugin](https://github.com/radeklat/delfino-demo) or any of the other [existing
+plugins](#plugins).\n\n# Existing plugins\n\nPlugins can greatly reduce code
+duplication and/or promote your own standards in multiple places. For example,
+you can create a plugin wrapping common linting tools that you use on your
+projects, including their default configuration. Keeping the rules and creating
+new projects with the same style suddenly becomes a matter of installing one
+Python library.\n\nEach plugin can contain one or more Click commands that are
+automatically discovered and exposed by Delfino. See [`delfino-demo`](https://
+github.com/radeklat/delfino-demo) for a minimal plugin, which provide a `demo`
+command printing out a message.\n\nExisting plugins:\n\n| Plugin name |
+Description |\n|:-------------------------------------------------------------
+|:-----------------------------------------------------------------------------
+----------------------|\n| [delfino-demo](https://github.com/radeklat/delfino-
+demo) | A minimal plugin example for Delfino. Contains one command printing a
+message. |\n| [delfino-core](https://github.com/radeklat/delfino-core) |
+Commands wrapping tools used during every day development (linting, testing,
+dependencies update). |\n| [delfino-docker](https://github.com/radeklat/
+delfino-docker) | Docker build helper script. |\n\n## Enabling a plugin\n\nFor
+security reasons, plugins are disabled by default. To enable a plugin, you have
+to include it in the `pyproject.toml` file:\n\n```toml\n
+[tool.delfino.plugins.]\n```\n\n## Enabling/disabling commands\n\nBy default,
+all commands are enabled. Use `enable_commands` or `disable_commands` to show
+only a subset of commands. If both used, disabled commands are subtracted from
+the set of enabled commands.\n\n```toml\n# [tool.delfino.plugins.]\n#
+enable_commands = []\n# disable_commands = []\n\n# [tool.delfino.plugins.]\n#
+enable_commands = []\n# disable_commands = []\n```\n\n# Advanced
+usage\n\n\n\n## Auto-completion\n\nYou can either attempt to install
+completions automatically with:\n\n```shell script\ndelfino --install-
+completion\n```\n\nor generate it with:\n\n```shell script\ndelfino --show-
+completion\n```\n\nand manually put it in the relevant RC file.\n\nThe auto-
+completion implementation is dynamic so that every time it is invoked, it uses
+the current project. Each project can have different commands or disable
 certain commands it doesn\'t use. And dynamic auto-completion makes sure only
 the currently available commands will be suggested.\n\nThe downside of this
 approach is that evaluating what is available each time is slower than a static
 list of commands.\n\n## Running external programs\n\nIt is up to you how you
 want to execute external processes as part of commands (if you need to at all).
 A common way in Python is to use `subprocess.run`. Delfino comes with its own
 [`run` implementation](https://github.com/radeklat/delfino/blob/main/src/
```

### Comparing `delfino-1.2.0/PKG-INFO` & `delfino-1.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310a 4e61 6d65 3a20 6465 6c66  : 2.1.Name: delf
-00000020: 696e 6f0a 5665 7273 696f 6e3a 2031 2e32  ino.Version: 1.2
+00000020: 696e 6f0a 5665 7273 696f 6e3a 2031 2e33  ino.Version: 1.3
 00000030: 2e30 0a53 756d 6d61 7279 3a20 4120 636f  .0.Summary: A co
 00000040: 6c6c 6563 7469 6f6e 206f 6620 636f 6d6d  llection of comm
 00000050: 616e 6420 6c69 6e65 2068 656c 7065 7220  and line helper 
 00000060: 7363 7269 7074 7320 7772 6170 7069 6e67  scripts wrapping
 00000070: 2074 6f6f 6c73 2075 7365 6420 6475 7269   tools used duri
 00000080: 6e67 2050 7974 686f 6e20 6465 7665 6c6f  ng Python develo
 00000090: 706d 656e 742e 0a48 6f6d 652d 7061 6765  pment..Home-page
@@ -92,1093 +92,1158 @@
 000005b0: 7874 2f6d 6172 6b64 6f77 6e0a 0a3c 6831  xt/markdown..<h1
 000005c0: 2061 6c69 676e 3d22 6365 6e74 6572 2220   align="center" 
 000005d0: 7374 796c 653d 2262 6f72 6465 722d 626f  style="border-bo
 000005e0: 7474 6f6d 3a20 6e6f 6e65 3b22 3ef0 9fa7  ttom: none;">...
 000005f0: b026 6e62 7370 3b26 6e62 7370 3b44 656c  .&nbsp;&nbsp;Del
 00000600: 6669 6e6f 266e 6273 703b 266e 6273 703b  fino&nbsp;&nbsp;
 00000610: f09f a7b0 3c2f 6831 3e0a 3c68 3320 616c  ....</h1>.<h3 al
-00000620: 6967 6e3d 2263 656e 7465 7222 3e50 6c75  ign="center">Plu
-00000630: 6761 626c 6520 436c 6963 6b20 636f 6d6d  gable Click comm
-00000640: 616e 6420 6669 6e64 6572 2f6c 6f61 6465  and finder/loade
-00000650: 722f 6578 6563 7574 6f72 2e3c 2f68 333e  r/executor.</h3>
-00000660: 0a0a 3c70 2061 6c69 676e 3d22 6365 6e74  ..<p align="cent
-00000670: 6572 223e 0a20 2020 203c 6120 6872 6566  er">.    <a href
-00000680: 3d22 6874 7470 733a 2f2f 6170 702e 6369  ="https://app.ci
-00000690: 7263 6c65 6369 2e63 6f6d 2f70 6970 656c  rcleci.com/pipel
-000006a0: 696e 6573 2f67 6974 6875 622f 7261 6465  ines/github/rade
-000006b0: 6b6c 6174 2f64 656c 6669 6e6f 3f62 7261  klat/delfino?bra
-000006c0: 6e63 683d 6d61 696e 223e 0a20 2020 2020  nch=main">.     
-000006d0: 2020 203c 696d 6720 616c 743d 2243 6972     <img alt="Cir
-000006e0: 636c 6543 4922 2073 7263 3d22 6874 7470  cleCI" src="http
-000006f0: 733a 2f2f 696d 672e 7368 6965 6c64 732e  s://img.shields.
-00000700: 696f 2f63 6972 636c 6563 692f 6275 696c  io/circleci/buil
-00000710: 642f 6769 7468 7562 2f72 6164 656b 6c61  d/github/radekla
-00000720: 742f 6465 6c66 696e 6f22 3e0a 2020 2020  t/delfino">.    
-00000730: 3c2f 613e 0a20 2020 203c 6120 6872 6566  </a>.    <a href
-00000740: 3d22 6874 7470 733a 2f2f 6170 702e 636f  ="https://app.co
-00000750: 6465 636f 762e 696f 2f67 682f 7261 6465  decov.io/gh/rade
-00000760: 6b6c 6174 2f64 656c 6669 6e6f 2f22 3e0a  klat/delfino/">.
-00000770: 2020 2020 2020 2020 3c69 6d67 2061 6c74          <img alt
-00000780: 3d22 436f 6465 636f 7622 2073 7263 3d22  ="Codecov" src="
-00000790: 6874 7470 733a 2f2f 696d 672e 7368 6965  https://img.shie
-000007a0: 6c64 732e 696f 2f63 6f64 6563 6f76 2f63  lds.io/codecov/c
-000007b0: 2f67 6974 6875 622f 7261 6465 6b6c 6174  /github/radeklat
-000007c0: 2f64 656c 6669 6e6f 223e 0a20 2020 203c  /delfino">.    <
-000007d0: 2f61 3e0a 2020 2020 3c61 2068 7265 663d  /a>.    <a href=
-000007e0: 2268 7474 7073 3a2f 2f67 6974 6875 622e  "https://github.
-000007f0: 636f 6d2f 7261 6465 6b6c 6174 2f64 656c  com/radeklat/del
-00000800: 6669 6e6f 2f74 6167 7322 3e0a 2020 2020  fino/tags">.    
-00000810: 2020 2020 3c69 6d67 2061 6c74 3d22 4769      <img alt="Gi
-00000820: 7448 7562 2074 6167 2028 6c61 7465 7374  tHub tag (latest
-00000830: 2053 656d 5665 7229 2220 7372 633d 2268   SemVer)" src="h
-00000840: 7474 7073 3a2f 2f69 6d67 2e73 6869 656c  ttps://img.shiel
-00000850: 6473 2e69 6f2f 6769 7468 7562 2f74 6167  ds.io/github/tag
-00000860: 2f72 6164 656b 6c61 742f 6465 6c66 696e  /radeklat/delfin
-00000870: 6f22 3e0a 2020 2020 3c2f 613e 0a20 2020  o">.    </a>.   
-00000880: 203c 696d 6720 616c 743d 224d 6169 6e74   <img alt="Maint
-00000890: 656e 616e 6365 2220 7372 633d 2268 7474  enance" src="htt
-000008a0: 7073 3a2f 2f69 6d67 2e73 6869 656c 6473  ps://img.shields
-000008b0: 2e69 6f2f 6d61 696e 7465 6e61 6e63 652f  .io/maintenance/
-000008c0: 7965 732f 3230 3233 223e 0a20 2020 203c  yes/2023">.    <
-000008d0: 6120 6872 6566 3d22 6874 7470 733a 2f2f  a href="https://
-000008e0: 6769 7468 7562 2e63 6f6d 2f72 6164 656b  github.com/radek
-000008f0: 6c61 742f 6465 6c66 696e 6f2f 636f 6d6d  lat/delfino/comm
-00000900: 6974 732f 6d61 696e 223e 0a20 2020 2020  its/main">.     
-00000910: 2020 203c 696d 6720 616c 743d 2247 6974     <img alt="Git
-00000920: 4875 6220 6c61 7374 2063 6f6d 6d69 7422  Hub last commit"
-00000930: 2073 7263 3d22 6874 7470 733a 2f2f 696d   src="https://im
-00000940: 672e 7368 6965 6c64 732e 696f 2f67 6974  g.shields.io/git
-00000950: 6875 622f 6c61 7374 2d63 6f6d 6d69 742f  hub/last-commit/
-00000960: 7261 6465 6b6c 6174 2f64 656c 6669 6e6f  radeklat/delfino
-00000970: 223e 0a20 2020 203c 2f61 3e0a 2020 2020  ">.    </a>.    
-00000980: 3c61 2068 7265 663d 2268 7474 7073 3a2f  <a href="https:/
-00000990: 2f77 7777 2e70 7974 686f 6e2e 6f72 672f  /www.python.org/
-000009a0: 646f 632f 7665 7273 696f 6e73 2f22 3e0a  doc/versions/">.
-000009b0: 2020 2020 2020 2020 3c69 6d67 2061 6c74          <img alt
-000009c0: 3d22 5079 5049 202d 2050 7974 686f 6e20  ="PyPI - Python 
-000009d0: 5665 7273 696f 6e22 2073 7263 3d22 6874  Version" src="ht
-000009e0: 7470 733a 2f2f 696d 672e 7368 6965 6c64  tps://img.shield
-000009f0: 732e 696f 2f70 7970 692f 7079 7665 7273  s.io/pypi/pyvers
-00000a00: 696f 6e73 2f64 656c 6669 6e6f 223e 0a20  ions/delfino">. 
-00000a10: 2020 203c 2f61 3e0a 2020 2020 3c61 2068     </a>.    <a h
-00000a20: 7265 663d 2268 7474 7073 3a2f 2f70 7970  ref="https://pyp
-00000a30: 6973 7461 7473 2e6f 7267 2f70 6163 6b61  istats.org/packa
-00000a40: 6765 732f 6465 6c66 696e 6f22 3e0a 2020  ges/delfino">.  
-00000a50: 2020 2020 2020 3c69 6d67 2061 6c74 3d22        <img alt="
-00000a60: 446f 776e 6c6f 6164 7322 2073 7263 3d22  Downloads" src="
-00000a70: 6874 7470 733a 2f2f 696d 672e 7368 6965  https://img.shie
-00000a80: 6c64 732e 696f 2f70 7970 692f 646d 2f64  lds.io/pypi/dm/d
-00000a90: 656c 6669 6e6f 223e 0a20 2020 203c 2f61  elfino">.    </a
-00000aa0: 3e0a 3c2f 703e 0a0a 3c21 2d2d 0a20 2020  >.</p>..<!--.   
-00000ab0: 2048 6f77 2074 6f20 6765 6e65 7261 7465   How to generate
-00000ac0: 2054 4f43 2066 726f 6d20 5079 4368 6172   TOC from PyChar
-00000ad0: 6d3a 0a20 2020 2068 7474 7073 3a2f 2f67  m:.    https://g
-00000ae0: 6974 6875 622e 636f 6d2f 7673 6368 2f69  ithub.com/vsch/i
-00000af0: 6465 612d 6d75 6c74 696d 6172 6b64 6f77  dea-multimarkdow
-00000b00: 6e2f 7769 6b69 2f54 6162 6c65 2d6f 662d  n/wiki/Table-of-
-00000b10: 436f 6e74 656e 7473 2d45 7874 656e 7369  Contents-Extensi
-00000b20: 6f6e 0a2d 2d3e 0a5b 544f 4320 6c65 7665  on.-->.[TOC leve
-00000b30: 6c73 3d31 2c32 206d 6172 6b64 6f77 6e20  ls=1,2 markdown 
-00000b40: 666f 726d 6174 7465 6420 6275 6c6c 6574  formatted bullet
-00000b50: 2068 6965 7261 7263 6879 5d3a 2023 2022   hierarchy]: # "
-00000b60: 5461 626c 6520 6f66 2063 6f6e 7465 6e74  Table of content
-00000b70: 220a 0a23 2054 6162 6c65 206f 6620 636f  "..# Table of co
-00000b80: 6e74 656e 740a 2d20 5b57 6861 7420 6973  ntent.- [What is
-00000b90: 2044 656c 6669 6e6f 5d28 2377 6861 742d   Delfino](#what-
-00000ba0: 6973 2d64 656c 6669 6e6f 290a 2020 2d20  is-delfino).  - 
-00000bb0: 5b50 6c75 6769 6e73 5d28 2370 6c75 6769  [Plugins](#plugi
-00000bc0: 6e73 290a 2d20 5b49 6e73 7461 6c6c 6174  ns).- [Installat
-00000bd0: 696f 6e5d 2823 696e 7374 616c 6c61 7469  ion](#installati
-00000be0: 6f6e 290a 2d20 5b43 6f6e 6669 6775 7261  on).- [Configura
-00000bf0: 7469 6f6e 5d28 2363 6f6e 6669 6775 7261  tion](#configura
-00000c00: 7469 6f6e 290a 2020 2d20 5b45 6e61 626c  tion).  - [Enabl
-00000c10: 696e 6720 6120 706c 7567 696e 5d28 2365  ing a plugin](#e
-00000c20: 6e61 626c 696e 672d 612d 706c 7567 696e  nabling-a-plugin
-00000c30: 290a 2020 2d20 5b45 6e61 626c 696e 672f  ).  - [Enabling/
-00000c40: 6469 7361 626c 696e 6720 636f 6d6d 616e  disabling comman
-00000c50: 6473 5d28 2365 6e61 626c 696e 6764 6973  ds](#enablingdis
-00000c60: 6162 6c69 6e67 2d63 6f6d 6d61 6e64 7329  abling-commands)
-00000c70: 0a2d 205b 5573 6167 655d 2823 7573 6167  .- [Usage](#usag
-00000c80: 6529 0a2d 205b 4465 7665 6c6f 706d 656e  e).- [Developmen
-00000c90: 745d 2823 6465 7665 6c6f 706d 656e 7429  t](#development)
-00000ca0: 0a20 202d 205b 436f 6d6d 616e 6473 2064  .  - [Commands d
-00000cb0: 6973 636f 7665 7279 5d28 2363 6f6d 6d61  iscovery](#comma
-00000cc0: 6e64 732d 6469 7363 6f76 6572 7929 0a20  nds-discovery). 
-00000cd0: 202d 205b 4d69 6e69 6d61 6c20 636f 6d6d   - [Minimal comm
-00000ce0: 616e 645d 2823 6d69 6e69 6d61 6c2d 636f  and](#minimal-co
-00000cf0: 6d6d 616e 6429 0a20 202d 205b 4d69 6e69  mmand).  - [Mini
-00000d00: 6d61 6c20 706c 7567 696e 5d28 236d 696e  mal plugin](#min
-00000d10: 696d 616c 2d70 6c75 6769 6e29 0a2d 205b  imal-plugin).- [
-00000d20: 4164 7661 6e63 6564 2075 7361 6765 5d28  Advanced usage](
-00000d30: 2361 6476 616e 6365 642d 7573 6167 6529  #advanced-usage)
-00000d40: 0a20 202d 205b 4175 746f 2d63 6f6d 706c  .  - [Auto-compl
-00000d50: 6574 696f 6e5d 2823 6175 746f 2d63 6f6d  etion](#auto-com
-00000d60: 706c 6574 696f 6e29 0a20 202d 205b 5275  pletion).  - [Ru
-00000d70: 6e6e 696e 6720 6578 7465 726e 616c 2070  nning external p
-00000d80: 726f 6772 616d 735d 2823 7275 6e6e 696e  rograms](#runnin
-00000d90: 672d 6578 7465 726e 616c 2d70 726f 6772  g-external-progr
-00000da0: 616d 7329 0a20 202d 205b 4f70 7469 6f6e  ams).  - [Option
-00000db0: 616c 2064 6570 656e 6465 6e63 6965 735d  al dependencies]
-00000dc0: 2823 6f70 7469 6f6e 616c 2d64 6570 656e  (#optional-depen
-00000dd0: 6465 6e63 6965 7329 0a20 202d 205b 5072  dencies).  - [Pr
-00000de0: 6f6a 6563 7420 7365 7474 696e 6773 5d28  oject settings](
-00000df0: 2370 726f 6a65 6374 2d73 6574 7469 6e67  #project-setting
-00000e00: 7329 0a20 202d 205b 506c 7567 696e 2073  s).  - [Plugin s
-00000e10: 6574 7469 6e67 735d 2823 706c 7567 696e  ettings](#plugin
-00000e20: 2d73 6574 7469 6e67 7329 0a20 202d 205b  -settings).  - [
-00000e30: 5072 6f6a 6563 7420 7370 6563 6966 6963  Project specific
-00000e40: 206f 7665 7272 6964 6573 5d28 2370 726f   overrides](#pro
-00000e50: 6a65 6374 2d73 7065 6369 6669 632d 6f76  ject-specific-ov
-00000e60: 6572 7269 6465 7329 0a20 202d 205b 4772  errides).  - [Gr
-00000e70: 6f75 7069 6e67 2063 6f6d 6d61 6e64 735d  ouping commands]
-00000e80: 2823 6772 6f75 7069 6e67 2d63 6f6d 6d61  (#grouping-comma
-00000e90: 6e64 7329 0a0a 2320 5768 6174 2069 7320  nds)..# What is 
-00000ea0: 4465 6c66 696e 6f0a 0a44 656c 6669 6e6f  Delfino..Delfino
-00000eb0: 2069 7320 6120 7772 6170 7065 7220 6172   is a wrapper ar
-00000ec0: 6f75 6e64 205b 436c 6963 6b5d 2868 7474  ound [Click](htt
-00000ed0: 7073 3a2f 2f63 6c69 636b 2e70 616c 6c65  ps://click.palle
-00000ee0: 7473 7072 6f6a 6563 7473 2e63 6f6d 2920  tsprojects.com) 
-00000ef0: 636f 6d6d 616e 6420 6c69 6e65 2073 6372  command line scr
-00000f00: 6970 7473 2e20 4974 2061 7574 6f6d 6174  ipts. It automat
-00000f10: 6963 616c 6c79 2064 6973 636f 7665 7273  ically discovers
-00000f20: 2069 6e73 7461 6e63 6573 206f 6620 5b43   instances of [C
-00000f30: 6c69 636b 2063 6f6d 6d61 6e64 735d 2868  lick commands](h
-00000f40: 7474 7073 3a2f 2f63 6c69 636b 2e70 616c  ttps://click.pal
-00000f50: 6c65 7473 7072 6f6a 6563 7473 2e63 6f6d  letsprojects.com
-00000f60: 2f71 7569 636b 7374 6172 742f 2362 6173  /quickstart/#bas
-00000f70: 6963 2d63 6f6e 6365 7074 732d 6372 6561  ic-concepts-crea
-00000f80: 7469 6e67 2d61 2d63 6f6d 6d61 6e64 2920  ting-a-command) 
-00000f90: 616e 6420 6f66 6665 7273 2074 6865 6d20  and offers them 
-00000fa0: 666f 7220 6578 6563 7574 696f 6e2e 2048  for execution. H
-00000fb0: 6f77 6576 6572 2c20 7468 6520 6269 6767  owever, the bigg
-00000fc0: 6573 7420 706f 7765 7220 636f 6d65 7320  est power comes 
-00000fd0: 6672 6f6d 2074 6865 2070 6f73 7369 6269  from the possibi
-00000fe0: 6c69 7479 206f 6620 6372 6561 7469 6e67  lity of creating
-00000ff0: 205b 706c 7567 696e 735d 2823 706c 7567   [plugins](#plug
-00001000: 696e 7329 2c20 7768 6963 6820 6361 6e20  ins), which can 
-00001010: 6265 2064 6973 7472 6962 7574 6564 2061  be distributed a
-00001020: 7320 7374 616e 6461 7264 2050 7974 686f  s standard Pytho
-00001030: 6e20 7061 636b 6167 6573 2e0a 0a23 2320  n packages...## 
-00001040: 506c 7567 696e 730a 0a50 6c75 6769 6e73  Plugins..Plugins
-00001050: 2063 616e 2067 7265 6174 6c79 2072 6564   can greatly red
-00001060: 7563 6520 636f 6465 2064 7570 6c69 6361  uce code duplica
-00001070: 7469 6f6e 2061 6e64 2f6f 7220 7072 6f6d  tion and/or prom
-00001080: 6f74 6520 796f 7572 206f 776e 2073 7461  ote your own sta
-00001090: 6e64 6172 6473 2069 6e20 6d75 6c74 6970  ndards in multip
-000010a0: 6c65 2070 6c61 6365 732e 2046 6f72 2065  le places. For e
-000010b0: 7861 6d70 6c65 2c20 796f 7520 6361 6e20  xample, you can 
-000010c0: 6372 6561 7465 2061 2070 6c75 6769 6e20  create a plugin 
-000010d0: 7772 6170 7069 6e67 2063 6f6d 6d6f 6e20  wrapping common 
-000010e0: 6c69 6e74 696e 6720 746f 6f6c 7320 7468  linting tools th
-000010f0: 6174 2079 6f75 2075 7365 206f 6e20 796f  at you use on yo
-00001100: 7572 2070 726f 6a65 6374 732c 2069 6e63  ur projects, inc
-00001110: 6c75 6469 6e67 2074 6865 6972 2064 6566  luding their def
-00001120: 6175 6c74 2063 6f6e 6669 6775 7261 7469  ault configurati
-00001130: 6f6e 2e20 4b65 6570 696e 6720 7468 6520  on. Keeping the 
-00001140: 7275 6c65 7320 616e 6420 6372 6561 7469  rules and creati
-00001150: 6e67 206e 6577 2070 726f 6a65 6374 7320  ng new projects 
-00001160: 7769 7468 2074 6865 2073 616d 6520 7374  with the same st
-00001170: 796c 6520 7375 6464 656e 6c79 2062 6563  yle suddenly bec
-00001180: 6f6d 6573 2061 206d 6174 7465 7220 6f66  omes a matter of
-00001190: 2069 6e73 7461 6c6c 696e 6720 6f6e 6520   installing one 
-000011a0: 5079 7468 6f6e 206c 6962 7261 7279 2e0a  Python library..
-000011b0: 0a45 6163 6820 706c 7567 696e 2063 616e  .Each plugin can
-000011c0: 2063 6f6e 7461 696e 206f 6e65 206f 7220   contain one or 
-000011d0: 6d6f 7265 2043 6c69 636b 2063 6f6d 6d61  more Click comma
-000011e0: 6e64 7320 7468 6174 2061 7265 2061 7574  nds that are aut
-000011f0: 6f6d 6174 6963 616c 6c79 2064 6973 636f  omatically disco
-00001200: 7665 7265 6420 616e 6420 6578 706f 7365  vered and expose
-00001210: 6420 6279 2044 656c 6669 6e6f 2e20 5365  d by Delfino. Se
-00001220: 6520 5b60 6465 6c66 696e 6f2d 6465 6d6f  e [`delfino-demo
-00001230: 605d 2868 7474 7073 3a2f 2f67 6974 6875  `](https://githu
-00001240: 622e 636f 6d2f 7261 6465 6b6c 6174 2f64  b.com/radeklat/d
-00001250: 656c 6669 6e6f 2d64 656d 6f29 2066 6f72  elfino-demo) for
-00001260: 2061 206d 696e 696d 616c 2070 6c75 6769   a minimal plugi
-00001270: 6e2c 2077 6869 6368 2070 726f 7669 6465  n, which provide
-00001280: 2061 2060 6465 6d6f 6020 636f 6d6d 616e   a `demo` comman
-00001290: 6420 7072 696e 7469 6e67 206f 7574 2061  d printing out a
-000012a0: 206d 6573 7361 6765 2e0a 0a45 7869 7374   message...Exist
-000012b0: 696e 6720 706c 7567 696e 733a 0a0a 7c20  ing plugins:..| 
-000012c0: 506c 7567 696e 206e 616d 6520 2020 2020  Plugin name     
-000012d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000012e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000012f0: 2020 2020 2020 2020 2020 2020 207c 2044               | D
-00001300: 6573 6372 6970 7469 6f6e 2020 2020 2020  escription      
-00001310: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00001320: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00001330: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00001340: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00001350: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00001360: 2020 7c0a 7c3a 2d2d 2d2d 2d2d 2d2d 2d2d    |.|:----------
-00001370: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-00001380: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-00001390: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-000013a0: 2d2d 2d7c 3a2d 2d2d 2d2d 2d2d 2d2d 2d2d  ---|:-----------
-000013b0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-000013c0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-000013d0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-000013e0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-000013f0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-00001400: 2d2d 2d2d 2d2d 2d2d 7c0a 7c20 5b64 656c  --------|.| [del
-00001410: 6669 6e6f 2d64 656d 6f5d 2868 7474 7073  fino-demo](https
-00001420: 3a2f 2f67 6974 6875 622e 636f 6d2f 7261  ://github.com/ra
-00001430: 6465 6b6c 6174 2f64 656c 6669 6e6f 2d64  deklat/delfino-d
-00001440: 656d 6f29 2020 2020 207c 2041 206d 696e  emo)     | A min
-00001450: 696d 616c 2070 6c75 6769 6e20 6578 616d  imal plugin exam
-00001460: 706c 6520 666f 7220 4465 6c66 696e 6f2e  ple for Delfino.
-00001470: 2043 6f6e 7461 696e 7320 6f6e 6520 636f   Contains one co
-00001480: 6d6d 616e 6420 7072 696e 7469 6e67 2061  mmand printing a
-00001490: 206d 6573 7361 6765 2e20 2020 2020 2020   message.       
-000014a0: 2020 2020 2020 2020 2020 2020 2020 7c0a                |.
-000014b0: 7c20 5b64 656c 6669 6e6f 2d63 6f72 655d  | [delfino-core]
-000014c0: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
-000014d0: 636f 6d2f 7261 6465 6b6c 6174 2f64 656c  com/radeklat/del
-000014e0: 6669 6e6f 2d63 6f72 6529 2020 2020 207c  fino-core)     |
-000014f0: 2043 6f6d 6d61 6e64 7320 7772 6170 7069   Commands wrappi
-00001500: 6e67 2074 6f6f 6c73 2075 7365 6420 6475  ng tools used du
-00001510: 7269 6e67 2065 7665 7279 2064 6179 2064  ring every day d
-00001520: 6576 656c 6f70 6d65 6e74 2028 6c69 6e74  evelopment (lint
-00001530: 696e 672c 2074 6573 7469 6e67 2c20 6465  ing, testing, de
-00001540: 7065 6e64 656e 6369 6573 2075 7064 6174  pendencies updat
-00001550: 6529 2e20 7c0a 7c20 5b64 656c 6669 6e6f  e). |.| [delfino
-00001560: 2d64 6f63 6b65 725d 2868 7474 7073 3a2f  -docker](https:/
-00001570: 2f67 6974 6875 622e 636f 6d2f 7261 6465  /github.com/rade
-00001580: 6b6c 6174 2f64 656c 6669 6e6f 2d64 6f63  klat/delfino-doc
-00001590: 6b65 7229 207c 2044 6f63 6b65 7220 6275  ker) | Docker bu
-000015a0: 696c 6420 6865 6c70 6572 2073 6372 6970  ild helper scrip
-000015b0: 742e 2020 2020 2020 2020 2020 2020 2020  t.              
-000015c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000015d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000015e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000015f0: 2020 2020 2020 2020 2020 7c0a 0a23 2049            |..# I
-00001600: 6e73 7461 6c6c 6174 696f 6e0a 0a2d 2070  nstallation..- p
-00001610: 6970 3a20 6070 6970 2069 6e73 7461 6c6c  ip: `pip install
-00001620: 2064 656c 6669 6e6f 600a 2d20 506f 6574   delfino`.- Poet
-00001630: 7279 3a20 6070 6f65 7472 7920 6164 6420  ry: `poetry add 
-00001640: 2d2d 6772 6f75 703d 6465 7620 6465 6c66  --group=dev delf
-00001650: 696e 6f60 0a2d 2050 6970 656e 763a 2060  ino`.- Pipenv: `
-00001660: 7069 7065 6e76 2069 6e73 7461 6c6c 202d  pipenv install -
-00001670: 6420 6465 6c66 696e 6f60 0a0a 6f72 200a  d delfino`..or .
-00001680: 0a2d 2070 6970 3a20 6070 6970 2069 6e73  .- pip: `pip ins
-00001690: 7461 6c6c 2064 656c 6669 6e6f 5b63 6f6d  tall delfino[com
-000016a0: 706c 6574 696f 6e5d 600a 2d20 506f 6574  pletion]`.- Poet
-000016b0: 7279 3a20 6070 6f65 7472 7920 6164 6420  ry: `poetry add 
-000016c0: 2d2d 6772 6f75 703d 6465 7620 6465 6c66  --group=dev delf
-000016d0: 696e 6f5b 636f 6d70 6c65 7469 6f6e 5d60  ino[completion]`
-000016e0: 0a2d 2050 6970 656e 763a 2060 7069 7065  .- Pipenv: `pipe
-000016f0: 6e76 2069 6e73 7461 6c6c 202d 6420 6465  nv install -d de
-00001700: 6c66 696e 6f5b 636f 6d70 6c65 7469 6f6e  lfino[completion
-00001710: 5d60 0a0a 746f 2065 6e61 626c 6520 5b61  ]`..to enable [a
-00001720: 7574 6f2d 636f 6d70 6c65 7469 6f6e 5d28  uto-completion](
-00001730: 2361 7574 6f2d 636f 6d70 6c65 7469 6f6e  #auto-completion
-00001740: 292e 0a0a 2320 436f 6e66 6967 7572 6174  )...# Configurat
-00001750: 696f 6e0a 0a41 6c6c 2063 6f6e 6669 6775  ion..All configu
-00001760: 7261 7469 6f6e 2069 7320 6578 7065 6374  ration is expect
-00001770: 6564 2074 6f20 6c69 7665 2069 6e20 6f6e  ed to live in on
-00001780: 6520 6f66 2074 6865 2066 6f6c 6c6f 7769  e of the followi
-00001790: 6e67 2066 696c 6573 3a0a 0a2d 2060 7079  ng files:..- `py
-000017a0: 7072 6f6a 6563 742e 746f 6d6c 6020 696e  project.toml` in
-000017b0: 2074 6865 2070 726f 6a65 6374 2072 6f6f   the project roo
-000017c0: 740a 2d20 602e 7079 6c69 6e74 7263 6020  t.- `.pylintrc` 
-000017d0: 696e 2074 6865 2070 726f 6a65 6374 2072  in the project r
-000017e0: 6f6f 7420 2d20 746f 2061 6c6c 6f77 2064  oot - to allow d
-000017f0: 6576 2073 7065 6369 6669 6320 636f 6e66  ev specific conf
-00001800: 6967 2c20 6e6f 7420 736f 7572 6365 2063  ig, not source c
-00001810: 6f6e 7472 6f6c 6c65 6420 6f72 2066 6f72  ontrolled or for
-00001820: 206e 6f6e 2d50 7974 686f 6e20 7072 6f6a   non-Python proj
-00001830: 6563 7473 0a2d 2060 2e70 796c 696e 7472  ects.- `.pylintr
-00001840: 6360 2069 6e20 7468 6520 7573 6572 2068  c` in the user h
-00001850: 6f6d 6520 6469 7265 6374 6f72 7920 2d20  ome directory - 
-00001860: 666f 7220 7573 6572 2074 6f6f 6c73 2061  for user tools a
-00001870: 7661 696c 6162 6c65 2069 6e20 7468 6520  vailable in the 
-00001880: 7379 7374 656d 0a0a 4966 206d 756c 7469  system..If multi
-00001890: 706c 6520 6669 6c65 7320 6172 6520 6469  ple files are di
-000018a0: 7363 6f76 6572 6564 2c20 6f6e 6c79 2074  scovered, only t
-000018b0: 6865 2068 6967 6865 7374 206f 6e65 2069  he highest one i
-000018c0: 6e20 7468 6520 6c69 7374 2077 696c 6c20  n the list will 
-000018d0: 6265 2075 7365 642e 0a0a 5468 6520 666f  be used...The fo
-000018e0: 726d 6174 2066 6f72 2060 2e70 796c 696e  rmat for `.pylin
-000018f0: 7472 6360 2069 7320 7468 6520 7361 6d65  trc` is the same
-00001900: 2061 7320 666f 7220 6070 7970 726f 6a65   as for `pyproje
-00001910: 6374 2e74 6f6d 6c60 2e0a 0a23 2320 456e  ct.toml`...## En
-00001920: 6162 6c69 6e67 2061 2070 6c75 6769 6e0a  abling a plugin.
-00001930: 0a46 6f72 2073 6563 7572 6974 7920 7265  .For security re
-00001940: 6173 6f6e 732c 2070 6c75 6769 6e73 2061  asons, plugins a
-00001950: 7265 2064 6973 6162 6c65 6420 6279 2064  re disabled by d
-00001960: 6566 6175 6c74 2e20 546f 2065 6e61 626c  efault. To enabl
-00001970: 6520 6120 706c 7567 696e 2c20 796f 7520  e a plugin, you 
-00001980: 6861 7665 2074 6f20 696e 636c 7564 6520  have to include 
-00001990: 6974 2069 6e20 7468 6520 6070 7970 726f  it in the `pypro
-000019a0: 6a65 6374 2e74 6f6d 6c60 2066 696c 653a  ject.toml` file:
-000019b0: 0a0a 6060 6074 6f6d 6c0a 5b74 6f6f 6c2e  ..```toml.[tool.
-000019c0: 6465 6c66 696e 6f2e 706c 7567 696e 732e  delfino.plugins.
-000019d0: 3c50 4c55 4749 4e5f 4e41 4d45 3e5d 0a60  <PLUGIN_NAME>].`
-000019e0: 6060 0a0a 2323 2045 6e61 626c 696e 672f  ``..## Enabling/
-000019f0: 6469 7361 626c 696e 6720 636f 6d6d 616e  disabling comman
-00001a00: 6473 0a0a 4279 2064 6566 6175 6c74 2c20  ds..By default, 
-00001a10: 616c 6c20 636f 6d6d 616e 6473 2061 7265  all commands are
-00001a20: 2065 6e61 626c 6564 2e20 5573 6520 6065   enabled. Use `e
-00001a30: 6e61 626c 655f 636f 6d6d 616e 6473 6020  nable_commands` 
-00001a40: 6f72 2060 6469 7361 626c 655f 636f 6d6d  or `disable_comm
-00001a50: 616e 6473 6020 2074 6f20 7368 6f77 206f  ands`  to show o
-00001a60: 6e6c 7920 6120 7375 6273 6574 206f 6620  nly a subset of 
-00001a70: 636f 6d6d 616e 6473 2e20 4966 2062 6f74  commands. If bot
-00001a80: 6820 7573 6564 2c20 6469 7361 626c 6564  h used, disabled
-00001a90: 2063 6f6d 6d61 6e64 7320 6172 6520 7375   commands are su
-00001aa0: 6274 7261 6374 6564 2066 726f 6d20 7468  btracted from th
-00001ab0: 6520 7365 7420 6f66 2065 6e61 626c 6564  e set of enabled
-00001ac0: 2063 6f6d 6d61 6e64 732e 0a0a 6060 6074   commands...```t
-00001ad0: 6f6d 6c0a 2320 5b74 6f6f 6c2e 6465 6c66  oml.# [tool.delf
-00001ae0: 696e 6f2e 706c 7567 696e 732e 3c50 4c55  ino.plugins.<PLU
-00001af0: 4749 4e5f 4e41 4d45 5f41 3e5d 0a23 2065  GIN_NAME_A>].# e
-00001b00: 6e61 626c 655f 636f 6d6d 616e 6473 203d  nable_commands =
-00001b10: 205b 3c43 4f4d 4d41 4e44 5f4e 414d 453e   [<COMMAND_NAME>
-00001b20: 5d0a 2320 6469 7361 626c 655f 636f 6d6d  ].# disable_comm
-00001b30: 616e 6473 203d 205b 3c43 4f4d 4d41 4e44  ands = [<COMMAND
-00001b40: 5f4e 414d 453e 5d0a 0a23 205b 746f 6f6c  _NAME>]..# [tool
-00001b50: 2e64 656c 6669 6e6f 2e70 6c75 6769 6e73  .delfino.plugins
-00001b60: 2e3c 504c 5547 494e 5f4e 414d 455f 423e  .<PLUGIN_NAME_B>
-00001b70: 5d0a 2320 656e 6162 6c65 5f63 6f6d 6d61  ].# enable_comma
-00001b80: 6e64 7320 3d20 5b3c 434f 4d4d 414e 445f  nds = [<COMMAND_
-00001b90: 4e41 4d45 3e5d 0a23 2064 6973 6162 6c65  NAME>].# disable
-00001ba0: 5f63 6f6d 6d61 6e64 7320 3d20 5b3c 434f  _commands = [<CO
-00001bb0: 4d4d 414e 445f 4e41 4d45 3e5d 0a60 6060  MMAND_NAME>].```
-00001bc0: 0a0a 2320 5573 6167 650a 0a52 756e 2060  ..# Usage..Run `
-00001bd0: 6465 6c66 696e 6f20 2d2d 6865 6c70 6020  delfino --help` 
-00001be0: 746f 2073 6565 2061 6c6c 2061 7661 696c  to see all avail
-00001bf0: 6162 6c65 2063 6f6d 6d61 6e64 7320 616e  able commands an
-00001c00: 6420 7468 6569 7220 7573 6167 652e 0a0a  d their usage...
-00001c10: 2320 4465 7665 6c6f 706d 656e 740a 0a44  # Development..D
-00001c20: 656c 6669 6e6f 2069 7320 6120 7369 6d70  elfino is a simp
-00001c30: 6c65 2077 7261 7070 6572 2061 726f 756e  le wrapper aroun
-00001c40: 6420 5b43 6c69 636b 2063 6f6d 6d61 6e64  d [Click command
-00001c50: 735d 2868 7474 7073 3a2f 2f63 6c69 636b  s](https://click
-00001c60: 2e70 616c 6c65 7473 7072 6f6a 6563 7473  .palletsprojects
-00001c70: 2e63 6f6d 2f71 7569 636b 7374 6172 742f  .com/quickstart/
-00001c80: 2362 6173 6963 2d63 6f6e 6365 7074 732d  #basic-concepts-
-00001c90: 6372 6561 7469 6e67 2d61 2d63 6f6d 6d61  creating-a-comma
-00001ca0: 6e64 292e 2041 6e79 2043 6c69 636b 2063  nd). Any Click c
-00001cb0: 6f6d 6d61 6e64 2077 696c 6c20 6265 2061  ommand will be a
-00001cc0: 6363 6570 7465 6420 6279 2044 656c 6669  ccepted by Delfi
-00001cd0: 6e6f 2e0a 0a23 2320 436f 6d6d 616e 6473  no...## Commands
-00001ce0: 2064 6973 636f 7665 7279 0a0a 4465 6c66   discovery..Delf
-00001cf0: 696e 6f20 6c6f 6f6b 7320 666f 7220 616e  ino looks for an
-00001d00: 7920 5b60 636c 6963 6b2e 436f 6d6d 616e  y [`click.Comman
-00001d10: 6460 5d28 6874 7470 733a 2f2f 636c 6963  d`](https://clic
-00001d20: 6b2e 7061 6c6c 6574 7370 726f 6a65 6374  k.palletsproject
-00001d30: 732e 636f 6d2f 656e 2f38 2e30 2e78 2f61  s.com/en/8.0.x/a
-00001d40: 7069 2f23 636c 6963 6b2e 436f 6d6d 616e  pi/#click.Comman
-00001d50: 6429 2073 7562 2d63 6c61 7373 2069 6e20  d) sub-class in 
-00001d60: 7468 6520 666f 6c6c 6f77 696e 6720 6c6f  the following lo
-00001d70: 6361 7469 6f6e 733a 0a0a 2d20 6063 6f6d  cations:..- `com
-00001d80: 6d61 6e64 7360 2066 6f6c 6465 7220 696e  mands` folder in
-00001d90: 2074 6865 2072 6f6f 7420 6f66 2074 6865   the root of the
-00001da0: 2070 726f 6a65 6374 2028 6e65 7874 2074   project (next t
-00001db0: 6f20 7468 6520 6070 7970 726f 6a65 6374  o the `pyproject
-00001dc0: 2e74 6f6d 6c60 2066 696c 6529 2e20 5468  .toml` file). Th
-00001dd0: 6973 206c 6f63 6174 696f 6e20 6973 2075  is location is u
-00001de0: 7365 6675 6c20 666f 7220 636f 6d6d 616e  seful for comman
-00001df0: 6473 2074 6861 7420 646f 6e27 7420 6e65  ds that don't ne
-00001e00: 6564 2074 6f20 6265 2072 6570 6c69 6361  ed to be replica
-00001e10: 7465 6420 696e 206d 756c 7469 706c 6520  ted in multiple 
-00001e20: 6c6f 6361 7469 6f6e 732f 7072 6f6a 6563  locations/projec
-00001e30: 7473 2e0a 2d20 7079 7468 6f6e 206d 6f64  ts..- python mod
-00001e40: 756c 6520 696d 706f 7274 2070 6174 6820  ule import path 
-00001e50: 2860 3c49 4d50 4f52 545f 5041 5448 3e60  (`<IMPORT_PATH>`
-00001e60: 2920 7370 6563 6966 6965 6420 6279 2060  ) specified by `
-00001e70: 656e 7472 795f 706f 696e 7460 206f 6620  entry_point` of 
-00001e80: 5b61 2070 6c75 6769 6e5d 2823 6d69 6e69  [a plugin](#mini
-00001e90: 6d61 6c2d 706c 7567 696e 293a 0a20 2060  mal-plugin):.  `
-00001ea0: 6060 746f 6d6c 0a20 205b 746f 6f6c 2e70  ``toml.  [tool.p
-00001eb0: 6f65 7472 792e 706c 7567 696e 735d 2023  oetry.plugins] #
-00001ec0: 204f 7074 696f 6e61 6c20 7375 7065 7220   Optional super 
-00001ed0: 7461 626c 650a 0a20 205b 746f 6f6c 2e70  table..  [tool.p
-00001ee0: 6f65 7472 792e 706c 7567 696e 732e 2264  oetry.plugins."d
-00001ef0: 656c 6669 6e6f 2e70 6c75 6769 6e22 5d0a  elfino.plugin"].
-00001f00: 2020 2264 656c 6669 6e6f 2d3c 504c 5547    "delfino-<PLUG
-00001f10: 494e 5f4e 414d 453e 2220 3d20 223c 494d  IN_NAME>" = "<IM
-00001f20: 504f 5254 5f50 4154 483e 220a 2020 6060  PORT_PATH>".  ``
-00001f30: 600a 0a41 6e79 2066 696c 6573 2073 7461  `..Any files sta
-00001f40: 7274 696e 6720 7769 7468 2061 6e20 756e  rting with an un
-00001f50: 6465 7273 636f 7265 2c20 6578 6365 7074  derscore, except
-00001f60: 2066 6f72 2060 5f5f 696e 6974 5f5f 2e70   for `__init__.p
-00001f70: 7960 2c20 7769 6c6c 2062 6520 6967 6e6f  y`, will be igno
-00001f80: 7265 642e 0a0a 3e20 2a2a 5761 726e 696e  red...> **Warnin
-00001f90: 672a 2a0a 3e20 466f 6c64 6572 7320 6172  g**.> Folders ar
-00001fa0: 6520 4e4f 5420 696e 7370 6563 7465 6420  e NOT inspected 
-00001fb0: 7265 6375 7273 6976 656c 792e 2049 6620  recursively. If 
-00001fc0: 796f 7520 706c 6163 6520 616e 7920 636f  you place any co
-00001fd0: 6d6d 616e 6473 2069 6e74 6f20 6e65 7374  mmands into nest
-00001fe0: 6564 2066 6f6c 6465 7273 2c20 7468 6579  ed folders, they
-00001ff0: 2077 696c 6c20 6e6f 7420 6265 206c 6f61   will not be loa
-00002000: 6465 6420 6279 2044 656c 6669 6e6f 2e0a  ded by Delfino..
-00002010: 0a0a 2323 204d 696e 696d 616c 2063 6f6d  ..## Minimal com
-00002020: 6d61 6e64 0a0a 3c21 2d2d 2054 4f44 4f28  mand..<!-- TODO(
-00002030: 5261 6465 6b29 3a20 4465 6c66 696e 6f20  Radek): Delfino 
-00002040: 6578 7065 6374 7320 6070 7970 726f 6a65  expects `pyproje
-00002050: 6374 2e74 6f6d 6c60 2063 6f6e 6669 6775  ct.toml` configu
-00002060: 7265 642e 202d 2d3e 0a3c 212d 2d20 544f  red. -->.<!-- TO
-00002070: 444f 2852 6164 656b 293a 2044 656c 6669  DO(Radek): Delfi
-00002080: 6e6f 2065 7870 6563 7473 2050 6f65 7472  no expects Poetr
-00002090: 7920 6f72 2050 6970 656e 7620 746f 2062  y or Pipenv to b
-000020a0: 6520 6176 6169 6c61 626c 652e 202d 2d3e  e available. -->
-000020b0: 0a0a 312e 2043 7265 6174 6520 6120 6063  ..1. Create a `c
-000020c0: 6f6d 6d61 6e64 7360 2066 6f6c 6465 723a  ommands` folder:
-000020d0: 0a20 2020 6060 6073 6865 6c6c 2073 6372  .   ```shell scr
-000020e0: 6970 740a 2020 206d 6b64 6972 2063 6f6d  ipt.   mkdir com
-000020f0: 6d61 6e64 730a 2020 2060 6060 0a32 2e20  mands.   ```.2. 
-00002100: 4372 6561 7465 2061 2060 636f 6d6d 616e  Create a `comman
-00002110: 6473 2f5f 5f69 6e69 745f 5f2e 7079 6020  ds/__init__.py` 
-00002120: 6669 6c65 2c20 7769 7468 2074 6865 2066  file, with the f
-00002130: 6f6c 6c6f 7769 6e67 2063 6f6e 7465 6e74  ollowing content
-00002140: 3a0a 2020 2060 6060 7079 7468 6f6e 0a20  :.   ```python. 
-00002150: 2020 696d 706f 7274 2063 6c69 636b 0a20    import click. 
-00002160: 2020 0a20 2020 4063 6c69 636b 2e63 6f6d    .   @click.com
-00002170: 6d61 6e64 2829 0a20 2020 6465 6620 636f  mand().   def co
-00002180: 6d6d 616e 645f 7465 7374 2829 3a0a 2020  mmand_test():.  
-00002190: 2020 2020 2022 2222 5465 7374 7320 636f       """Tests co
-000021a0: 6d6d 616e 6473 2070 6c61 6365 6420 696e  mmands placed in
-000021b0: 2074 6865 2060 636f 6d6d 616e 6473 6020   the `commands` 
-000021c0: 666f 6c64 6572 2061 7265 206c 6f61 6465  folder are loade
-000021d0: 642e 2222 220a 2020 2020 2020 2070 7269  d.""".       pri
-000021e0: 6e74 2822 e29c a820 5468 6973 2063 6f6d  nt("... This com
-000021f0: 6d61 6e64 2077 6f72 6b73 2120 e29c a822  mand works! ..."
-00002200: 290a 2020 2060 6060 0a33 2e20 5365 6520  ).   ```.3. See 
-00002210: 6966 2044 656c 6669 6e6f 206c 6f61 6473  if Delfino loads
-00002220: 2074 6865 2063 6f6d 6d61 6e64 2e20 4f70   the command. Op
-00002230: 656e 2061 2074 6572 6d69 6e61 6c20 616e  en a terminal an
-00002240: 6420 696e 2074 6865 2072 6f6f 7420 6f66  d in the root of
-00002250: 2074 6865 2070 726f 6a65 6374 2c20 6361   the project, ca
-00002260: 6c6c 3a20 6064 656c 6669 6e6f 202d 2d68  ll: `delfino --h
-00002270: 656c 7060 2e20 596f 7520 7368 6f75 6c64  elp`. You should
-00002280: 2073 6565 2073 6f6d 6574 6869 6e67 206c   see something l
-00002290: 696b 6520 7468 6973 3a0a 2020 2060 6060  ike this:.   ```
-000022a0: 7465 7874 0a20 2020 5573 6167 653a 2064  text.   Usage: d
-000022b0: 656c 6669 6e6f 205b 4f50 5449 4f4e 535d  elfino [OPTIONS]
-000022c0: 2043 4f4d 4d41 4e44 205b 4152 4753 5d2e   COMMAND [ARGS].
-000022d0: 2e2e 0a20 2020 0a20 2020 4f70 7469 6f6e  ...   .   Option
-000022e0: 733a 0a20 2020 2020 2d2d 6865 6c70 2020  s:.     --help  
-000022f0: 5368 6f77 2074 6869 7320 6d65 7373 6167  Show this messag
-00002300: 6520 616e 6420 6578 6974 2e0a 2020 200a  e and exit..   .
-00002310: 2020 2043 6f6d 6d61 6e64 733a 0a20 2020     Commands:.   
-00002320: 2020 2e2e 2e0a 2020 2020 2063 6f6d 6d61    ....     comma
-00002330: 6e64 2d74 6573 7420 2020 2020 2020 2020  nd-test         
-00002340: 2020 2054 6573 7473 2063 6f6d 6d61 6e64     Tests command
-00002350: 7320 706c 6163 6564 2069 6e20 7468 6520  s placed in the 
-00002360: 6063 6f6d 6d61 6e64 7360 2066 6f6c 6465  `commands` folde
-00002370: 722e 2e2e 0a20 2020 2020 2e2e 2e0a 2020  r....     ....  
-00002380: 2060 6060 0a34 2e20 5275 6e20 7468 6520   ```.4. Run the 
-00002390: 636f 6d6d 616e 6420 7769 7468 2060 6465  command with `de
-000023a0: 6c66 696e 6f20 636f 6d6d 616e 642d 7465  lfino command-te
-000023b0: 7374 600a 0a23 2320 4d69 6e69 6d61 6c20  st`..## Minimal 
-000023c0: 706c 7567 696e 0a0a 4966 2079 6f75 2764  plugin..If you'd
-000023d0: 206c 696b 6520 746f 2075 7365 206f 6e65   like to use one
-000023e0: 206f 7220 6d6f 7265 2063 6f6d 6d61 6e64   or more command
-000023f0: 7320 696e 206d 756c 7469 706c 6520 706c  s in multiple pl
-00002400: 6163 6573 2c20 796f 7520 6361 6e20 6372  aces, you can cr
-00002410: 6561 7465 2061 2070 6c75 6769 6e2e 2041  eate a plugin. A
-00002420: 2070 6c75 6769 6e20 6973 206a 7573 7420   plugin is just 
-00002430: 6120 7265 6775 6c61 7220 5079 7468 6f6e  a regular Python
-00002440: 2070 6163 6b61 6765 2077 6974 6820 7370   package with sp
-00002450: 6563 6966 6963 2065 6e74 7279 2070 6f69  ecific entry poi
-00002460: 6e74 2074 656c 6c69 6e67 2044 656c 6669  nt telling Delfi
-00002470: 6e6f 2069 7420 7368 6f75 6c64 2075 7365  no it should use
-00002480: 2069 742e 2049 7420 6361 6e20 616c 736f   it. It can also
-00002490: 2062 6520 6469 7374 7269 6275 7465 6420   be distributed 
-000024a0: 6173 2061 6e79 206f 7468 6572 2050 7974  as any other Pyt
-000024b0: 686f 6e20 7061 636b 6167 6573 2c20 666f  hon packages, fo
-000024c0: 7220 6578 616d 706c 6520 7669 6120 5079  r example via Py
-000024d0: 7069 2e0a 0a54 6865 2071 7569 636b 6573  pi...The quickes
-000024e0: 7420 7761 7920 746f 2063 7265 6174 6520  t way to create 
-000024f0: 6f6e 6520 6973 2074 6f20 7573 6520 6120  one is to use a 
-00002500: 5b44 656c 6669 6e6f 2070 6c75 6769 6e20  [Delfino plugin 
-00002510: 636f 6f6b 6965 6375 7474 6572 2074 656d  cookiecutter tem
-00002520: 706c 6174 655d 2868 7474 7073 3a2f 2f67  plate](https://g
-00002530: 6974 6875 622e 636f 6d2f 7261 6465 6b6c  ithub.com/radekl
-00002540: 6174 2f64 656c 6669 6e6f 2d70 6c75 6769  at/delfino-plugi
-00002550: 6e2d 636f 6f6b 6965 6375 7474 6572 2d74  n-cookiecutter-t
-00002560: 656d 706c 6174 6529 2c20 7768 6963 6820  emplate), which 
-00002570: 6173 6b73 2079 6f75 2073 6576 6572 616c  asks you several
-00002580: 2071 7565 7374 696f 6e73 2061 6e64 2073   questions and s
-00002590: 6574 7320 7570 2074 6865 2077 686f 6c65  ets up the whole
-000025a0: 2070 726f 6a65 6374 2e0a 0a41 6c74 6572   project...Alter
-000025b0: 6e61 7469 7665 6c79 2c20 796f 7520 6361  natively, you ca
-000025c0: 6e20 6765 7420 696e 7370 6972 6564 2062  n get inspired b
-000025d0: 7920 5b74 6865 2064 656d 6f20 706c 7567  y [the demo plug
-000025e0: 696e 5d28 6874 7470 733a 2f2f 6769 7468  in](https://gith
-000025f0: 7562 2e63 6f6d 2f72 6164 656b 6c61 742f  ub.com/radeklat/
-00002600: 6465 6c66 696e 6f2d 6465 6d6f 2920 6f72  delfino-demo) or
-00002610: 2061 6e79 206f 6620 7468 6520 6f74 6865   any of the othe
-00002620: 7220 5b65 7869 7374 696e 6720 706c 7567  r [existing plug
-00002630: 696e 735d 2823 706c 7567 696e 7329 2e0a  ins](#plugins)..
-00002640: 0a23 2041 6476 616e 6365 6420 7573 6167  .# Advanced usag
-00002650: 650a 0a3c 212d 2d0a 2323 2041 6476 616e  e..<!--.## Advan
-00002660: 6365 6420 436f 6d6d 616e 640a 0a44 656c  ced Command..Del
-00002670: 6669 6e6f 2061 6464 7320 6f70 7469 6f6e  fino adds option
-00002680: 616c 2062 6974 7320 6f66 2066 756e 6374  al bits of funct
-00002690: 696f 6e61 6c69 7479 206f 6e20 746f 7020  ionality on top 
-000026a0: 6f66 2043 6c69 636b 2e20 5468 6520 666f  of Click. The fo
-000026b0: 6c6c 6f77 696e 6720 6578 616d 706c 6520  llowing example 
-000026c0: 6465 6d6f 6e73 7472 6174 6573 2073 6f6d  demonstrates som
-000026d0: 6520 6f66 2074 686f 7365 3a0a 0a60 6060  e of those:..```
-000026e0: 7079 7468 6f6e 0a23 2063 6f6d 6d61 6e64  python.# command
-000026f0: 732f 5f5f 696e 6974 5f5f 2e70 790a 0a69  s/__init__.py..i
-00002700: 6d70 6f72 7420 636c 6963 6b0a 0a66 726f  mport click..fro
-00002710: 6d20 6465 6c66 696e 6f2e 636f 6e74 6578  m delfino.contex
-00002720: 7473 2069 6d70 6f72 7420 7061 7373 5f61  ts import pass_a
-00002730: 7070 5f63 6f6e 7465 7874 2c20 4170 7043  pp_context, AppC
-00002740: 6f6e 7465 7874 0a66 726f 6d20 6465 6c66  ontext.from delf
-00002750: 696e 6f2e 7661 6c69 6461 7469 6f6e 2069  ino.validation i
-00002760: 6d70 6f72 7420 6173 7365 7274 5f70 6970  mport assert_pip
-00002770: 5f70 6163 6b61 6765 5f69 6e73 7461 6c6c  _package_install
-00002780: 6564 2c20 7079 7072 6f6a 6563 745f 746f  ed, pyproject_to
-00002790: 6d6c 5f6b 6579 5f6d 6973 7369 6e67 0a0a  ml_key_missing..
-000027a0: 4063 6c69 636b 2e63 6f6d 6d61 6e64 2829  @click.command()
-000027b0: 0a23 2054 6865 2060 7061 7373 5f61 7070  .# The `pass_app
-000027c0: 5f63 6f6e 7465 7874 6020 6465 636f 7261  _context` decora
-000027d0: 746f 7220 6164 6473 2060 4170 7043 6f6e  tor adds `AppCon
-000027e0: 7465 7874 6020 6173 2074 6865 2066 6972  text` as the fir
-000027f0: 7374 2070 6172 616d 6574 6572 2e0a 4070  st parameter..@p
-00002800: 6173 735f 6170 705f 636f 6e74 6578 740a  ass_app_context.
-00002810: 6465 6620 636f 6d6d 616e 645f 7465 7374  def command_test
-00002820: 2861 7070 5f63 6f6e 7465 7874 3a20 4170  (app_context: Ap
-00002830: 7043 6f6e 7465 7874 293a 0a20 2020 2222  pContext):.   ""
-00002840: 2254 6573 7473 2063 6f6d 6d61 6e64 7320  "Tests commands 
-00002850: 706c 6163 6564 2069 6e20 7468 6520 6063  placed in the `c
-00002860: 6f6d 6d61 6e64 7360 2066 6f6c 6465 7220  ommands` folder 
-00002870: 6172 6520 6c6f 6164 6564 2e22 2222 0a20  are loaded.""". 
-00002880: 2020 2320 5465 7374 206f 7074 696f 6e61    # Test optiona
-00002890: 6c20 6465 7065 6e64 656e 6369 6573 2e20  l dependencies. 
-000028a0: 416e 7920 6661 696c 696e 6720 6173 7365  Any failing asse
-000028b0: 7274 696f 6e20 7769 6c6c 2062 6520 7072  rtion will be pr
-000028c0: 696e 7465 6420 6173 3a0a 2020 2023 2043  inted as:.   # C
-000028d0: 6f6d 6d61 6e64 2027 3c4e 414d 453e 2720  ommand '<NAME>' 
-000028e0: 6973 206d 6973 636f 6e66 6967 7572 6564  is misconfigured
-000028f0: 2e20 3c41 5353 4552 5449 4f4e 2045 5252  . <ASSERTION ERR
-00002900: 4f52 204d 4553 5341 4745 3e0a 2020 2061  OR MESSAGE>.   a
-00002910: 7373 6572 745f 7069 705f 7061 636b 6167  ssert_pip_packag
-00002920: 655f 696e 7374 616c 6c65 6428 2264 656c  e_installed("del
-00002930: 6669 6e6f 2229 0a0a 2020 2023 2041 7070  fino")..   # App
-00002940: 436f 6e74 6578 7420 636f 6e74 6169 6e20  Context contain 
-00002950: 6120 7061 7273 6564 2060 7079 7072 6f6a  a parsed `pyproj
-00002960: 6563 742e 746f 6d6c 6020 6669 6c65 2e0a  ect.toml` file..
-00002970: 2020 2023 2043 6f6d 6d61 6e64 7320 6361     # Commands ca
-00002980: 6e20 6164 6420 7468 6569 7220 636f 6e66  n add their conf
-00002990: 6967 2075 6e64 6572 2060 5b74 6f6f 6c2e  ig under `[tool.
-000029a0: 6465 6c66 696e 6f2e 636f 6d6d 616e 6473  delfino.commands
-000029b0: 2e3c 434f 4d4d 414e 445f 4e41 4d45 3e5d  .<COMMAND_NAME>]
-000029c0: 602e 0a20 2020 6173 7365 7274 2022 636f  `..   assert "co
-000029d0: 6d6d 616e 645f 7465 7374 2220 696e 2061  mmand_test" in a
-000029e0: 7070 5f63 6f6e 7465 7874 2e70 7970 726f  pp_context.pypro
-000029f0: 6a65 6374 5f74 6f6d 6c2e 746f 6f6c 2e64  ject_toml.tool.d
-00002a00: 656c 6669 6e6f 2e63 6f6d 6d61 6e64 732c  elfino.commands,
-00002a10: 205c 0a20 2020 2020 2020 7079 7072 6f6a   \.       pyproj
-00002a20: 6563 745f 746f 6d6c 5f6b 6579 5f6d 6973  ect_toml_key_mis
-00002a30: 7369 6e67 2822 746f 6f6c 2e64 656c 6669  sing("tool.delfi
-00002a40: 6e6f 2e63 6f6d 6d61 6e64 732e 636f 6d6d  no.commands.comm
-00002a50: 616e 645f 7465 7374 2229 0a0a 2020 2070  and_test")..   p
-00002a60: 7269 6e74 2861 7070 5f63 6f6e 7465 7874  rint(app_context
-00002a70: 2e70 7970 726f 6a65 6374 5f74 6f6d 6c2e  .pyproject_toml.
-00002a80: 746f 6f6c 2e64 656c 6669 6e6f 2e63 6f6d  tool.delfino.com
-00002a90: 6d61 6e64 735b 2263 6f6d 6d61 6e64 2d74  mands["command-t
-00002aa0: 6573 7422 5d29 0a60 6060 0a2d 2d3e 0a0a  est"]).```.-->..
-00002ab0: 2323 2041 7574 6f2d 636f 6d70 6c65 7469  ## Auto-completi
-00002ac0: 6f6e 0a0a 596f 7520 6361 6e20 6569 7468  on..You can eith
-00002ad0: 6572 2061 7474 656d 7074 2074 6f20 696e  er attempt to in
-00002ae0: 7374 616c 6c20 636f 6d70 6c65 7469 6f6e  stall completion
-00002af0: 7320 6175 746f 6d61 7469 6361 6c6c 7920  s automatically 
-00002b00: 7769 7468 3a0a 0a60 6060 7368 656c 6c20  with:..```shell 
-00002b10: 7363 7269 7074 0a64 656c 6669 6e6f 202d  script.delfino -
-00002b20: 2d69 6e73 7461 6c6c 2d63 6f6d 706c 6574  -install-complet
-00002b30: 696f 6e0a 6060 600a 0a6f 7220 6765 6e65  ion.```..or gene
-00002b40: 7261 7465 2069 7420 7769 7468 3a0a 0a60  rate it with:..`
-00002b50: 6060 7368 656c 6c20 7363 7269 7074 0a64  ``shell script.d
-00002b60: 656c 6669 6e6f 202d 2d73 686f 772d 636f  elfino --show-co
-00002b70: 6d70 6c65 7469 6f6e 0a60 6060 0a0a 616e  mpletion.```..an
-00002b80: 6420 6d61 6e75 616c 6c79 2070 7574 2069  d manually put i
-00002b90: 7420 696e 2074 6865 2072 656c 6576 616e  t in the relevan
-00002ba0: 7420 5243 2066 696c 652e 0a0a 5468 6520  t RC file...The 
-00002bb0: 6175 746f 2d63 6f6d 706c 6574 696f 6e20  auto-completion 
-00002bc0: 696d 706c 656d 656e 7461 7469 6f6e 2069  implementation i
-00002bd0: 7320 6479 6e61 6d69 6320 736f 2074 6861  s dynamic so tha
-00002be0: 7420 6576 6572 7920 7469 6d65 2069 7420  t every time it 
-00002bf0: 6973 2069 6e76 6f6b 6564 2c20 6974 2075  is invoked, it u
-00002c00: 7365 7320 7468 6520 6375 7272 656e 7420  ses the current 
-00002c10: 7072 6f6a 6563 742e 2045 6163 6820 7072  project. Each pr
-00002c20: 6f6a 6563 7420 6361 6e20 6861 7665 2064  oject can have d
-00002c30: 6966 6665 7265 6e74 2063 6f6d 6d61 6e64  ifferent command
-00002c40: 7320 6f72 2064 6973 6162 6c65 2063 6572  s or disable cer
-00002c50: 7461 696e 2063 6f6d 6d61 6e64 7320 6974  tain commands it
-00002c60: 2064 6f65 736e 2774 2075 7365 2e20 416e   doesn't use. An
-00002c70: 6420 6479 6e61 6d69 6320 6175 746f 2d63  d dynamic auto-c
-00002c80: 6f6d 706c 6574 696f 6e20 6d61 6b65 7320  ompletion makes 
-00002c90: 7375 7265 206f 6e6c 7920 7468 6520 6375  sure only the cu
-00002ca0: 7272 656e 746c 7920 6176 6169 6c61 626c  rrently availabl
-00002cb0: 6520 636f 6d6d 616e 6473 2077 696c 6c20  e commands will 
-00002cc0: 6265 2073 7567 6765 7374 6564 2e0a 0a54  be suggested...T
-00002cd0: 6865 2064 6f77 6e73 6964 6520 6f66 2074  he downside of t
-00002ce0: 6869 7320 6170 7072 6f61 6368 2069 7320  his approach is 
-00002cf0: 7468 6174 2065 7661 6c75 6174 696e 6720  that evaluating 
-00002d00: 7768 6174 2069 7320 6176 6169 6c61 626c  what is availabl
-00002d10: 6520 6561 6368 2074 696d 6520 6973 2073  e each time is s
-00002d20: 6c6f 7765 7220 7468 616e 2061 2073 7461  lower than a sta
-00002d30: 7469 6320 6c69 7374 206f 6620 636f 6d6d  tic list of comm
-00002d40: 616e 6473 2e0a 0a23 2320 5275 6e6e 696e  ands...## Runnin
-00002d50: 6720 6578 7465 726e 616c 2070 726f 6772  g external progr
-00002d60: 616d 730a 0a49 7420 6973 2075 7020 746f  ams..It is up to
-00002d70: 2079 6f75 2068 6f77 2079 6f75 2077 616e   you how you wan
-00002d80: 7420 746f 2065 7865 6375 7465 2065 7874  t to execute ext
-00002d90: 6572 6e61 6c20 7072 6f63 6573 7365 7320  ernal processes 
-00002da0: 6173 2070 6172 7420 6f66 2063 6f6d 6d61  as part of comma
-00002db0: 6e64 7320 2869 6620 796f 7520 6e65 6564  nds (if you need
-00002dc0: 2074 6f20 6174 2061 6c6c 292e 2041 2063   to at all). A c
-00002dd0: 6f6d 6d6f 6e20 7761 7920 696e 2050 7974  ommon way in Pyt
-00002de0: 686f 6e20 6973 2074 6f20 7573 6520 6073  hon is to use `s
-00002df0: 7562 7072 6f63 6573 732e 7275 6e60 2e20  ubprocess.run`. 
-00002e00: 4465 6c66 696e 6f20 636f 6d65 7320 7769  Delfino comes wi
-00002e10: 7468 2069 7473 206f 776e 205b 6072 756e  th its own [`run
-00002e20: 6020 696d 706c 656d 656e 7461 7469 6f6e  ` implementation
-00002e30: 5d28 6874 7470 733a 2f2f 6769 7468 7562  ](https://github
-00002e40: 2e63 6f6d 2f72 6164 656b 6c61 742f 6465  .com/radeklat/de
-00002e50: 6c66 696e 6f2f 626c 6f62 2f6d 6169 6e2f  lfino/blob/main/
-00002e60: 7372 632f 6465 6c66 696e 6f2f 6578 6563  src/delfino/exec
-00002e70: 7574 696f 6e2e 7079 234c 3934 292c 2077  ution.py#L94), w
-00002e80: 6869 6368 2077 7261 7073 2061 6e64 2073  hich wraps and s
-00002e90: 696d 706c 6966 6965 7320 6073 7562 7072  implifies `subpr
-00002ea0: 6f63 6573 732e 7275 6e60 2066 6f72 2074  ocess.run` for t
-00002eb0: 6865 206d 6f73 7420 636f 6d6d 6f6e 2075  he most common u
-00002ec0: 7365 2063 6173 6573 3a0a 0a2d 204e 6f72  se cases:..- Nor
-00002ed0: 6d61 6c69 7a69 6e67 2060 7375 6270 726f  malizing `subpro
-00002ee0: 6365 7373 2e72 756e 6020 6172 6775 6d65  cess.run` argume
-00002ef0: 6e74 7320 2d20 796f 7520 6361 6e20 7061  nts - you can pa
-00002f00: 7373 2069 6e20 6569 7468 6572 2061 2073  ss in either a s
-00002f10: 7472 696e 6720 6f72 2061 206c 6973 742e  tring or a list.
-00002f20: 2045 6974 6865 7220 7761 792c 2060 7375   Either way, `su
-00002f30: 6270 726f 6365 7373 2e72 756e 6020 7769  bprocess.run` wi
-00002f40: 6c6c 2062 6520 6578 6563 7574 6564 2063  ll be executed c
-00002f50: 6f72 7265 6374 6c79 2e0a 2d20 4861 6e64  orrectly..- Hand
-00002f60: 6c69 6e67 2065 7272 6f72 7320 6672 6f6d  ling errors from
-00002f70: 2074 6865 2065 7865 6375 7469 6f6e 2076   the execution v
-00002f80: 6961 2074 6865 2060 6f6e 5f65 7272 6f72  ia the `on_error
-00002f90: 6020 6172 6775 6d65 6e74 2e20 4769 7669  ` argument. Givi
-00002fa0: 6e67 2074 6865 206f 7074 696f 6e20 746f  ng the option to
-00002fb0: 2065 6974 6865 7220 6967 6e6f 7265 2074   either ignore t
-00002fc0: 6865 2065 7272 6f72 7320 616e 6420 636f  he errors and co
-00002fd0: 6e74 696e 7565 2028 6050 4153 5360 292c  ntinue (`PASS`),
-00002fe0: 206e 6f74 2063 6f6e 7469 6e75 6520 616e   not continue an
-00002ff0: 6420 636c 6561 6e20 6578 6974 2028 6045  d clean exit (`E
-00003000: 5849 5460 2920 6f72 206e 6f74 2063 6f6e  XIT`) or not con
-00003010: 7469 6e75 6520 616e 6420 6162 6f72 7420  tinue and abort 
-00003020: 7769 7468 2065 7272 6f72 2063 6f64 6520  with error code 
-00003030: 2860 4142 4f52 5460 292e 0a2d 2053 6574  (`ABORT`)..- Set
-00003040: 7469 6e67 2065 6e76 6972 6f6e 6d65 6e74  ting environment
-00003050: 2076 6172 6961 626c 6573 2e0a 2d20 4c6f   variables..- Lo
-00003060: 6767 696e 6720 7768 6174 2069 7320 6265  gging what is be
-00003070: 696e 6720 6578 6563 7574 6564 2069 6e20  ing executed in 
-00003080: 7468 6520 6465 6275 6720 6c65 7665 6c2e  the debug level.
-00003090: 0a0a 4578 616d 706c 653a 0a0a 6060 6070  ..Example:..```p
-000030a0: 7974 686f 6e0a 2320 636f 6d6d 616e 6473  ython.# commands
-000030b0: 2f5f 5f69 6e69 745f 5f2e 7079 0a0a 696d  /__init__.py..im
-000030c0: 706f 7274 2063 6c69 636b 0a66 726f 6d20  port click.from 
-000030d0: 6465 6c66 696e 6f2e 6578 6563 7574 696f  delfino.executio
-000030e0: 6e20 696d 706f 7274 2072 756e 2c20 4f6e  n import run, On
-000030f0: 4572 726f 720a 0a40 636c 6963 6b2e 636f  Error..@click.co
-00003100: 6d6d 616e 6428 290a 6465 6620 7465 7374  mmand().def test
-00003110: 2829 3a0a 2020 2020 7275 6e28 2270 7974  ():.    run("pyt
-00003120: 6573 7420 7465 7374 7322 2c20 6f6e 5f65  est tests", on_e
-00003130: 7272 6f72 3d4f 6e45 7272 6f72 2e41 424f  rror=OnError.ABO
-00003140: 5254 290a 6060 600a 0a23 2320 4f70 7469  RT).```..## Opti
-00003150: 6f6e 616c 2064 6570 656e 6465 6e63 6965  onal dependencie
-00003160: 730a 0a49 6620 796f 7520 7075 7420 7365  s..If you put se
-00003170: 7665 7261 6c20 636f 6d6d 616e 6473 2069  veral commands i
-00003180: 6e74 6f20 6f6e 6520 5b70 6c75 6769 6e5d  nto one [plugin]
-00003190: 2823 706c 7567 696e 7329 2c20 796f 7520  (#plugins), you 
-000031a0: 6361 6e20 6d61 6b65 2073 6f6d 6520 6465  can make some de
-000031b0: 7065 6e64 656e 6369 6573 206f 6620 736f  pendencies of so
-000031c0: 6d65 2063 6f6d 6d61 6e64 7320 5b6f 7074  me commands [opt
-000031d0: 696f 6e61 6c5d 2868 7474 7073 3a2f 2f70  ional](https://p
-000031e0: 7974 686f 6e2d 706f 6574 7279 2e6f 7267  ython-poetry.org
-000031f0: 2f64 6f63 732f 7079 7072 6f6a 6563 7423  /docs/pyproject#
-00003200: 6578 7472 6173 292e 2054 6869 7320 6973  extras). This is
-00003210: 2075 7365 6675 6c20 7768 656e 2061 2063   useful when a c
-00003220: 6f6d 6d61 6e64 2069 7320 6e6f 7420 616c  ommand is not al
-00003230: 7761 7973 2075 7365 642c 2061 6e64 2079  ways used, and y
-00003240: 6f75 2064 6f6e 2774 2077 616e 7420 746f  ou don't want to
-00003250: 2069 6e73 7461 6c6c 2075 6e6e 6563 6573   install unneces
-00003260: 7361 7279 2064 6570 656e 6465 6e63 6965  sary dependencie
-00003270: 732e 2049 6e73 7465 6164 2c20 796f 7520  s. Instead, you 
-00003280: 6361 6e20 6368 6563 6b20 6966 2061 2064  can check if a d
-00003290: 6570 656e 6465 6e63 7920 6973 2069 6e73  ependency is ins
-000032a0: 7461 6c6c 6564 206f 6e6c 7920 7768 656e  talled only when
-000032b0: 2074 6865 2063 6f6d 6d61 6e64 2069 7320   the command is 
-000032c0: 6578 6563 7574 6564 2077 6974 6820 6064  executed with `d
-000032d0: 656c 6669 6e6f 2e76 616c 6964 6174 696f  elfino.validatio
-000032e0: 6e2e 6173 7365 7274 5f70 6970 5f70 6163  n.assert_pip_pac
-000032f0: 6b61 6765 5f69 6e73 7461 6c6c 6564 603a  kage_installed`:
-00003300: 0a0a 6060 6070 7974 686f 6e0a 2320 636f  ..```python.# co
-00003310: 6d6d 616e 6473 2f5f 5f69 6e69 745f 5f2e  mmands/__init__.
-00003320: 7079 0a0a 696d 706f 7274 2063 6c69 636b  py..import click
-00003330: 0a66 726f 6d20 6465 6c66 696e 6f2e 7661  .from delfino.va
-00003340: 6c69 6461 7469 6f6e 2069 6d70 6f72 7420  lidation import 
-00003350: 6173 7365 7274 5f70 6970 5f70 6163 6b61  assert_pip_packa
-00003360: 6765 5f69 6e73 7461 6c6c 6564 0a0a 7472  ge_installed..tr
-00003370: 793a 0a20 2020 2066 726f 6d20 6769 7420  y:.    from git 
-00003380: 696d 706f 7274 2052 6570 6f0a 6578 6365  import Repo.exce
-00003390: 7074 2049 6d70 6f72 7445 7272 6f72 3a0a  pt ImportError:.
-000033a0: 2020 2020 7061 7373 0a0a 4063 6c69 636b      pass..@click
-000033b0: 2e63 6f6d 6d61 6e64 2829 0a64 6566 2067  .command().def g
-000033c0: 6974 5f61 6374 6976 655f 6272 616e 6368  it_active_branch
-000033d0: 2829 3a0a 2020 2020 6173 7365 7274 5f70  ():.    assert_p
-000033e0: 6970 5f70 6163 6b61 6765 5f69 6e73 7461  ip_package_insta
-000033f0: 6c6c 6564 2822 6769 7470 7974 686f 6e22  lled("gitpython"
-00003400: 290a 2020 2020 7072 696e 7428 5265 706f  ).    print(Repo
-00003410: 2822 2e22 292e 6163 7469 7665 5f62 7261  (".").active_bra
-00003420: 6e63 6829 0a60 6060 0a0a 496e 2074 6865  nch).```..In the
-00003430: 2065 7861 6d70 6c65 2061 626f 7665 2c20   example above, 
-00003440: 6966 2060 6769 7470 7974 686f 6e60 2069  if `gitpython` i
-00003450: 7320 6e6f 7420 696e 7374 616c 6c65 642c  s not installed,
-00003460: 2064 656c 6669 6e6f 2077 696c 6c20 7368   delfino will sh
-00003470: 6f77 2074 6865 2063 6f6d 6d61 6e64 2062  ow the command b
-00003480: 7574 2077 696c 6c20 6661 696c 2077 6974  ut will fail wit
-00003490: 6820 7375 6767 6573 7469 6f6e 2074 6f20  h suggestion to 
-000034a0: 696e 7374 616c 6c20 6067 6974 7079 7468  install `gitpyth
-000034b0: 6f6e 6020 6f6e 6c79 2077 6865 6e20 7468  on` only when th
-000034c0: 6520 636f 6d6d 616e 6420 6973 2065 7865  e command is exe
-000034d0: 6375 7465 642e 2059 6f75 2063 616e 2061  cuted. You can a
-000034e0: 6c73 6f20 6164 6420 6067 6974 5f61 6374  lso add `git_act
-000034f0: 6976 655f 6272 616e 6368 6020 696e 746f  ive_branch` into
-00003500: 205b 6064 6973 6162 6c65 5f63 6f6d 6d61   [`disable_comma
-00003510: 6e64 7360 2063 6f6e 6669 675d 2823 656e  nds` config](#en
-00003520: 6162 6c69 6e67 6469 7361 626c 696e 672d  ablingdisabling-
-00003530: 636f 6d6d 616e 6473 2920 696e 2070 6c61  commands) in pla
-00003540: 6365 7320 7768 6572 6520 796f 7520 646f  ces where you do
-00003550: 6e27 7420 696e 7465 6e64 2074 6f20 7573  n't intend to us
-00003560: 6520 6974 2e0a 0a54 6869 7320 7761 7920  e it...This way 
-00003570: 796f 7520 6361 6e20 6772 6561 746c 7920  you can greatly 
-00003580: 7265 6475 6365 2074 6865 206e 756d 6265  reduce the numbe
-00003590: 7220 6f66 2064 6570 656e 6465 6e63 6965  r of dependencie
-000035a0: 7320 6120 706c 7567 696e 2062 7269 6e67  s a plugin bring
-000035b0: 7320 696e 746f 2061 2070 726f 6a65 6374  s into a project
-000035c0: 2077 6974 686f 7574 2061 206e 6565 6420   without a need 
-000035d0: 746f 2068 6176 6520 6d61 6e79 2073 6d61  to have many sma
-000035e0: 6c6c 2070 6c75 6769 6e73 2e0a 0a23 2320  ll plugins...## 
-000035f0: 5072 6f6a 6563 7420 7365 7474 696e 6773  Project settings
-00003600: 0a0a 596f 7520 6361 6e20 7374 6f72 6520  ..You can store 
-00003610: 616e 2061 7262 6974 7261 7279 206f 626a  an arbitrary obj
-00003620: 6563 7420 696e 2074 6865 2043 6c69 636b  ect in the Click
-00003630: 2063 6f6e 7465 7874 2061 7320 5b60 636c   context as [`cl
-00003640: 6963 6b2e 436f 6e74 6578 742e 6f62 6a60  ick.Context.obj`
-00003650: 5d28 6874 7470 733a 2f2f 636c 6963 6b2e  ](https://click.
-00003660: 7061 6c6c 6574 7370 726f 6a65 6374 732e  palletsprojects.
-00003670: 636f 6d2f 6170 692f 2363 6c69 636b 2e43  com/api/#click.C
-00003680: 6f6e 7465 7874 2e6f 626a 292e 2044 656c  ontext.obj). Del
-00003690: 6669 6e6f 2075 7469 6c69 7a65 7320 7468  fino utilizes th
-000036a0: 6973 206f 626a 6563 7420 746f 2073 746f  is object to sto
-000036b0: 7265 2061 6e20 696e 7374 616e 6365 206f  re an instance o
-000036c0: 6620 5b60 4170 7043 6f6e 7465 7874 605d  f [`AppContext`]
-000036d0: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
-000036e0: 636f 6d2f 7261 6465 6b6c 6174 2f64 656c  com/radeklat/del
-000036f0: 6669 6e6f 2f62 6c6f 622f 6d61 696e 2f73  fino/blob/main/s
-00003700: 7263 2f64 656c 6669 6e6f 2f6d 6f64 656c  rc/delfino/model
-00003710: 732f 6170 705f 636f 6e74 6578 742e 7079  s/app_context.py
-00003720: 292c 2077 6869 6368 2070 726f 7669 6465  ), which provide
-00003730: 7320 6163 6365 7373 2074 6f20 7072 6f6a  s access to proj
-00003740: 6563 7420 7265 6c61 7465 6420 696e 666f  ect related info
-00003750: 726d 6174 696f 6e2e 2049 6620 796f 7520  rmation. If you 
-00003760: 6e65 6564 2074 6f2c 2079 6f75 2063 616e  need to, you can
-00003770: 2073 7469 6c6c 2061 7474 6163 6820 6172   still attach ar
-00003780: 6269 7472 6172 7920 6174 7472 6962 7574  bitrary attribut
-00003790: 6573 2074 6f20 7468 6973 206f 626a 6563  es to this objec
-000037a0: 7420 6c61 7465 722e 0a0a 596f 7520 6361  t later...You ca
-000037b0: 6e20 7061 7373 2074 6869 7320 6f62 6a65  n pass this obje
-000037c0: 6374 2074 6f20 796f 7572 2063 6f6d 6d61  ct to your comma
-000037d0: 6e64 7320 6279 2064 6563 6f72 6174 696e  nds by decoratin
-000037e0: 6720 7468 656d 2077 6974 6820 5b60 636c  g them with [`cl
-000037f0: 6963 6b2e 7061 7373 5f6f 626a 605d 2868  ick.pass_obj`](h
-00003800: 7474 7073 3a2f 2f63 6c69 636b 2e70 616c  ttps://click.pal
-00003810: 6c65 7473 7072 6f6a 6563 7473 2e63 6f6d  letsprojects.com
-00003820: 2f61 7069 2f23 636c 6963 6b2e 7061 7373  /api/#click.pass
-00003830: 5f6f 626a 293a 0a0a 6060 6070 7974 686f  _obj):..```pytho
-00003840: 6e0a 2320 636f 6d6d 616e 6473 2f5f 5f69  n.# commands/__i
-00003850: 6e69 745f 5f2e 7079 0a0a 696d 706f 7274  nit__.py..import
-00003860: 2063 6c69 636b 0a66 726f 6d20 6465 6c66   click.from delf
-00003870: 696e 6f2e 6d6f 6465 6c73 2e61 7070 5f63  ino.models.app_c
-00003880: 6f6e 7465 7874 2069 6d70 6f72 7420 4170  ontext import Ap
-00003890: 7043 6f6e 7465 7874 0a0a 4063 6c69 636b  pContext..@click
-000038a0: 2e63 6f6d 6d61 6e64 2829 0a40 636c 6963  .command().@clic
-000038b0: 6b2e 7061 7373 5f6f 626a 0a64 6566 2070  k.pass_obj.def p
-000038c0: 7269 6e74 5f61 7070 5f76 6572 7369 6f6e  rint_app_version
-000038d0: 286f 626a 3a20 4170 7043 6f6e 7465 7874  (obj: AppContext
-000038e0: 293a 0a20 2020 2070 7269 6e74 286f 626a  ):.    print(obj
-000038f0: 2e70 7970 726f 6a65 6374 5f74 6f6d 6c2e  .pyproject_toml.
-00003900: 746f 6f6c 2e70 6f65 7472 792e 7665 7273  tool.poetry.vers
-00003910: 696f 6e29 0a60 6060 0a0a 2323 2050 6c75  ion).```..## Plu
-00003920: 6769 6e20 7365 7474 696e 6773 0a0a 506c  gin settings..Pl
-00003930: 7567 696e 2073 6574 7469 6e67 7320 6172  ugin settings ar
-00003940: 6520 6578 7065 6374 6564 2074 6f20 6c69  e expected to li
-00003950: 7665 2069 6e20 7468 6520 6070 7970 726f  ve in the `pypro
-00003960: 6a65 6374 2e74 6f6d 6c60 2066 696c 652e  ject.toml` file.
-00003970: 2054 6f20 7072 6576 656e 7420 6e61 6d69   To prevent nami
-00003980: 6e67 2063 6f6e 666c 6963 7473 2c20 6561  ng conflicts, ea
-00003990: 6368 2070 6c75 6769 6e20 6d75 7374 2070  ch plugin must p
-000039a0: 7574 2069 7473 2073 6574 7469 6e67 7320  ut its settings 
-000039b0: 756e 6465 7220 6074 6f6f 6c2e 6465 6c66  under `tool.delf
-000039c0: 696e 6f2e 706c 7567 696e 732e 3c50 4c55  ino.plugins.<PLU
-000039d0: 4749 4e5f 4e41 4d45 3e60 2e20 4974 2061  GIN_NAME>`. It a
-000039e0: 6c73 6f20 616c 6c6f 7773 2044 656c 6669  lso allows Delfi
-000039f0: 6e6f 2074 6f20 7061 7373 2074 6865 7365  no to pass these
-00003a00: 2073 6574 7469 6e67 7320 6469 7265 6374   settings direct
-00003a10: 6c79 2074 6f20 636f 6d6d 616e 6473 2066  ly to commands f
-00003a20: 726f 6d20 7468 6573 6520 706c 7567 696e  rom these plugin
-00003a30: 732e 0a0a 4465 6c66 696e 6f20 6c6f 6164  s...Delfino load
-00003a40: 732c 2070 6172 7365 732c 2076 616c 6964  s, parses, valid
-00003a50: 6174 6573 2061 6e64 2073 746f 7265 7320  ates and stores 
-00003a60: 706c 7567 696e 2073 6574 7469 6e67 7320  plugin settings 
-00003a70: 696e 205b 6041 7070 436f 6e74 6578 742e  in [`AppContext.
-00003a80: 706c 7567 696e 5f63 6f6e 6669 6760 5d28  plugin_config`](
-00003a90: 6874 7470 733a 2f2f 6769 7468 7562 2e63  https://github.c
-00003aa0: 6f6d 2f72 6164 656b 6c61 742f 6465 6c66  om/radeklat/delf
-00003ab0: 696e 6f2f 626c 6f62 2f6d 6169 6e2f 7372  ino/blob/main/sr
-00003ac0: 632f 6465 6c66 696e 6f2f 6d6f 6465 6c73  c/delfino/models
-00003ad0: 2f61 7070 5f63 6f6e 7465 7874 2e70 7929  /app_context.py)
-00003ae0: 2e20 4966 206e 6f74 2073 7065 6369 6669  . If not specifi
-00003af0: 6564 206f 7468 6572 7769 7365 2028 7365  ed otherwise (se
-00003b00: 6520 6265 6c6f 7729 2c20 6974 2077 696c  e below), it wil
-00003b10: 6c20 6265 2061 6e20 696e 7374 616e 6365  l be an instance
-00003b20: 206f 6620 5b60 506c 7567 696e 436f 6e66   of [`PluginConf
-00003b30: 6967 605d 2868 7474 7073 3a2f 2f67 6974  ig`](https://git
-00003b40: 6875 622e 636f 6d2f 7261 6465 6b6c 6174  hub.com/radeklat
-00003b50: 2f64 656c 6669 6e6f 2f62 6c6f 622f 6d61  /delfino/blob/ma
-00003b60: 696e 2f73 7263 2f64 656c 6669 6e6f 2f6d  in/src/delfino/m
-00003b70: 6f64 656c 732f 7079 7072 6f6a 6563 745f  odels/pyproject_
-00003b80: 746f 6d6c 2e70 7929 2c20 7769 7468 2061  toml.py), with a
-00003b90: 6e79 2065 7874 7261 206b 6579 7320 756e  ny extra keys un
-00003ba0: 7661 6c69 6461 7465 6420 616e 6420 696e  validated and in
-00003bb0: 204a 534f 4e2d 6c69 6b65 2050 7974 686f   JSON-like Pytho
-00003bc0: 6e20 6f62 6a65 6374 732e 0a0a 596f 7520  n objects...You 
-00003bd0: 6361 6e20 6164 6420 6164 6469 7469 6f6e  can add addition
-00003be0: 616c 2076 616c 6964 6174 696f 6e20 746f  al validation to
-00003bf0: 2079 6f75 7220 706c 7567 696e 2073 6574   your plugin set
-00003c00: 7469 6e67 7320 6279 2073 7562 2d63 6c61  tings by sub-cla
-00003c10: 7373 696e 6720 7468 6520 6050 6c75 6769  ssing the `Plugi
-00003c20: 6e43 6f6e 6669 6760 202c 2064 6566 696e  nConfig` , defin
-00003c30: 696e 6720 6578 7065 6374 6564 206b 6579  ing expected key
-00003c40: 732c 2064 6566 6175 6c74 2076 616c 7565  s, default value
-00003c50: 7320 616e 642f 6f72 2076 616c 6964 6174  s and/or validat
-00003c60: 696f 6e2e 2044 656c 6669 6e6f 2075 7469  ion. Delfino uti
-00003c70: 6c69 7a65 7320 5b60 7079 6461 6e74 6963  lizes [`pydantic
-00003c80: 605d 2868 7474 7073 3a2f 2f64 6f63 732e  `](https://docs.
-00003c90: 7079 6461 6e74 6963 2e64 6576 2f29 2074  pydantic.dev/) t
-00003ca0: 6f20 6372 6561 7465 2064 6174 6120 636c  o create data cl
-00003cb0: 6173 7365 732e 0a0a 4465 6c66 696e 6f20  asses...Delfino 
-00003cc0: 616c 736f 206e 6565 6473 2074 6f20 6b6e  also needs to kn
-00003cd0: 6f77 2c20 7768 6963 6820 636c 6173 7320  ow, which class 
-00003ce0: 746f 2075 7365 2066 6f72 2074 6865 2076  to use for the v
-00003cf0: 616c 6964 6174 696f 6e2e 2054 6f20 646f  alidation. To do
-00003d00: 2074 6861 742c 2073 7769 7463 6820 746f   that, switch to
-00003d10: 2060 6465 6c66 696e 6f2e 6465 636f 7261   `delfino.decora
-00003d20: 746f 7273 2e70 6173 735f 6170 705f 636f  tors.pass_app_co
-00003d30: 6e74 6578 7460 2069 6e73 7465 6164 206f  ntext` instead o
-00003d40: 6620 5b60 636c 6963 6b2e 7061 7373 5f6f  f [`click.pass_o
-00003d50: 626a 605d 2868 7474 7073 3a2f 2f63 6c69  bj`](https://cli
-00003d60: 636b 2e70 616c 6c65 7473 7072 6f6a 6563  ck.palletsprojec
-00003d70: 7473 2e63 6f6d 2f61 7069 2f23 636c 6963  ts.com/api/#clic
-00003d80: 6b2e 7061 7373 5f6f 626a 293a 0a0a 6060  k.pass_obj):..``
-00003d90: 6074 6f6d 6c0a 2320 7079 7072 6f6a 6563  `toml.# pyprojec
-00003da0: 742e 746f 6d6c 0a0a 5b74 6f6f 6c2e 6465  t.toml..[tool.de
-00003db0: 6c66 696e 6f2e 706c 7567 696e 732e 6465  lfino.plugins.de
-00003dc0: 6c66 696e 6f5f 6c6f 6769 6e5f 706c 7567  lfino_login_plug
-00003dd0: 696e 5d0a 7573 6572 6e61 6d65 203d 2022  in].username = "
-00003de0: 7573 6572 220a 6060 600a 0a60 6060 7079  user".```..```py
-00003df0: 7468 6f6e 0a23 2063 6f6d 6d61 6e64 732f  thon.# commands/
-00003e00: 5f5f 696e 6974 5f5f 2e70 790a 0a69 6d70  __init__.py..imp
-00003e10: 6f72 7420 636c 6963 6b0a 6672 6f6d 2064  ort click.from d
-00003e20: 656c 6669 6e6f 2e6d 6f64 656c 732e 7079  elfino.models.py
-00003e30: 7072 6f6a 6563 745f 746f 6d6c 2069 6d70  project_toml imp
-00003e40: 6f72 7420 506c 7567 696e 436f 6e66 6967  ort PluginConfig
-00003e50: 0a66 726f 6d20 6465 6c66 696e 6f2e 6d6f  .from delfino.mo
-00003e60: 6465 6c73 2e61 7070 5f63 6f6e 7465 7874  dels.app_context
-00003e70: 2069 6d70 6f72 7420 4170 7043 6f6e 7465   import AppConte
-00003e80: 7874 0a66 726f 6d20 6465 6c66 696e 6f2e  xt.from delfino.
-00003e90: 6465 636f 7261 746f 7273 2069 6d70 6f72  decorators impor
-00003ea0: 7420 7061 7373 5f61 7070 5f63 6f6e 7465  t pass_app_conte
-00003eb0: 7874 0a0a 0a63 6c61 7373 204c 6f67 696e  xt...class Login
-00003ec0: 506c 7567 696e 436f 6e66 6967 2850 6c75  PluginConfig(Plu
-00003ed0: 6769 6e43 6f6e 6669 6729 3a0a 2020 2020  ginConfig):.    
-00003ee0: 6c6f 6769 6e3a 2073 7472 0a0a 0a40 636c  login: str...@cl
-00003ef0: 6963 6b2e 636f 6d6d 616e 6428 290a 4070  ick.command().@p
-00003f00: 6173 735f 6170 705f 636f 6e74 6578 7428  ass_app_context(
-00003f10: 4c6f 6769 6e50 6c75 6769 6e43 6f6e 6669  LoginPluginConfi
-00003f20: 6729 0a64 6566 206c 6f67 696e 2861 7070  g).def login(app
-00003f30: 5f63 6f6e 7465 7874 3a20 4170 7043 6f6e  _context: AppCon
-00003f40: 7465 7874 5b4c 6f67 696e 506c 7567 696e  text[LoginPlugin
-00003f50: 436f 6e66 6967 5d29 3a0a 2020 2020 7072  Config]):.    pr
-00003f60: 696e 7428 6170 705f 636f 6e74 6578 742e  int(app_context.
-00003f70: 706c 7567 696e 5f63 6f6e 6669 672e 6c6f  plugin_config.lo
-00003f80: 6769 6e29 0a60 6060 0a0a 5468 6520 6041  gin).```..The `A
-00003f90: 7070 436f 6e74 6578 7460 2063 6c61 7373  ppContext` class
-00003fa0: 2069 7320 6765 6e65 7269 632e 2044 6566   is generic. Def
-00003fb0: 696e 696e 6720 7468 6520 6050 6c75 6769  ining the `Plugi
-00003fc0: 6e43 6f6e 6669 6754 7970 6560 2028 7375  nConfigType` (su
-00003fd0: 6368 2061 7320 6041 7070 436f 6e74 6578  ch as `AppContex
-00003fe0: 745b 4c6f 6769 6e50 6c75 6769 6e43 6f6e  t[LoginPluginCon
-00003ff0: 6669 675d 6020 696e 2074 6865 2065 7861  fig]` in the exa
-00004000: 6d70 6c65 2061 626f 7665 2920 656e 6162  mple above) enab
-00004010: 6c65 7320 696e 7472 6f73 7065 6374 696f  les introspectio
-00004020: 6e20 616e 6420 7479 7065 2063 6865 636b  n and type check
-00004030: 732e 0a0a 2323 2050 726f 6a65 6374 2073  s...## Project s
-00004040: 7065 6369 6669 6320 6f76 6572 7269 6465  pecific override
-00004050: 730a 0a49 7420 6973 206c 696b 656c 7920  s..It is likely 
-00004060: 796f 7572 2070 726f 6a65 6374 7320 7769  your projects wi
-00004070: 6c6c 2072 6571 7569 7265 2073 6c69 6768  ll require sligh
-00004080: 7420 6469 7665 7267 656e 6365 2074 6f20  t divergence to 
-00004090: 7468 6520 6465 6661 756c 7473 2079 6f75  the defaults you
-000040a0: 2065 6e63 6f64 6520 696e 2079 6f75 7220   encode in your 
-000040b0: 7363 7269 7074 732e 2054 6865 2066 6f6c  scripts. The fol
-000040c0: 6c6f 7769 6e67 2073 6563 7469 6f6e 7320  lowing sections 
-000040d0: 636f 7665 7220 7468 6520 6d6f 7374 2063  cover the most c
-000040e0: 6f6d 6d6f 6e20 7573 6520 6361 7365 732e  ommon use cases.
-000040f0: 0a0a 2323 2320 5061 7373 2d74 6872 6f75  ..### Pass-throu
-00004100: 6768 2061 7267 756d 656e 7473 0a0a 596f  gh arguments..Yo
-00004110: 7520 6361 6e20 7061 7373 2061 6464 6974  u can pass addit
-00004120: 696f 6e61 6c20 6172 6775 6d65 6e74 7320  ional arguments 
-00004130: 746f 2064 6f77 6e73 7472 6561 6d20 746f  to downstream to
-00004140: 6f6c 7320 6279 2064 6563 6f72 6174 696e  ols by decoratin
-00004150: 6720 636f 6d6d 616e 6473 2077 6974 6820  g commands with 
-00004160: 7468 6520 5b60 6465 636f 7261 746f 7273  the [`decorators
-00004170: 2e70 6173 735f 6172 6773 605d 2868 7474  .pass_args`](htt
-00004180: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00004190: 7261 6465 6b6c 6174 2f64 656c 6669 6e6f  radeklat/delfino
-000041a0: 2f62 6c6f 622f 6d61 696e 2f73 7263 2f64  /blob/main/src/d
-000041b0: 656c 6669 6e6f 2f64 6563 6f72 6174 6f72  elfino/decorator
-000041c0: 732f 7061 7373 5f61 7267 732e 7079 2920  s/pass_args.py) 
-000041d0: 6465 636f 7261 746f 723a 0a0a 6060 6070  decorator:..```p
-000041e0: 7974 686f 6e0a 2320 636f 6d6d 616e 6473  ython.# commands
-000041f0: 2f5f 5f69 6e69 745f 5f2e 7079 0a0a 6672  /__init__.py..fr
-00004200: 6f6d 2074 7970 696e 6720 696d 706f 7274  om typing import
-00004210: 2054 7570 6c65 0a0a 696d 706f 7274 2063   Tuple..import c
-00004220: 6c69 636b 0a66 726f 6d20 6465 6c66 696e  lick.from delfin
-00004230: 6f2e 6465 636f 7261 746f 7273 2069 6d70  o.decorators imp
-00004240: 6f72 7420 7061 7373 5f61 7267 730a 6672  ort pass_args.fr
-00004250: 6f6d 2064 656c 6669 6e6f 2e65 7865 6375  om delfino.execu
-00004260: 7469 6f6e 2069 6d70 6f72 7420 7275 6e2c  tion import run,
-00004270: 204f 6e45 7272 6f72 0a0a 4063 6c69 636b   OnError..@click
-00004280: 2e63 6f6d 6d61 6e64 2829 0a40 7061 7373  .command().@pass
-00004290: 5f61 7267 730a 6465 6620 7465 7374 2870  _args.def test(p
-000042a0: 6173 7365 645f 6172 6773 3a20 5475 706c  assed_args: Tupl
-000042b0: 655b 7374 722c 202e 2e2e 5d29 3a0a 2020  e[str, ...]):.  
-000042c0: 2020 7275 6e28 5b22 7079 7465 7374 222c    run(["pytest",
-000042d0: 2022 7465 7374 7322 2c20 2a70 6173 7365   "tests", *passe
-000042e0: 645f 6172 6773 5d2c 206f 6e5f 6572 726f  d_args], on_erro
-000042f0: 723d 4f6e 4572 726f 722e 4142 4f52 5429  r=OnError.ABORT)
-00004300: 0a60 6060 0a0a 5468 656e 2061 6464 6974  .```..Then addit
-00004310: 696f 6e61 6c20 6172 6775 6d65 6e74 7320  ional arguments 
-00004320: 6361 6e20 6265 2070 6173 7365 6420 6569  can be passed ei
-00004330: 7468 6572 2076 6961 2063 6f6d 6d61 6e64  ther via command
-00004340: 206c 696e 6520 6166 7465 7220 602d 2d60   line after `--`
-00004350: 3a0a 0a60 6060 7368 656c 6c20 7363 7269  :..```shell scri
-00004360: 7074 0a64 656c 6669 6e6f 2074 6573 7420  pt.delfino test 
-00004370: 2d2d 202d 2d63 6170 7475 7265 3d6e 6f0a  -- --capture=no.
-00004380: 6060 600a 0a4f 7220 7669 6120 636f 6e66  ```..Or via conf
-00004390: 6967 7572 6174 696f 6e20 696e 2074 6865  iguration in the
-000043a0: 2060 7079 7072 6f6a 6563 742e 746f 6d6c   `pyproject.toml
-000043b0: 6020 6669 6c65 3a0a 0a60 6060 746f 6d6c  ` file:..```toml
-000043c0: 0a5b 746f 6f6c 2e64 656c 6669 6e6f 2e70  .[tool.delfino.p
-000043d0: 6c75 6769 6e73 2e3c 504c 5547 494e 3e2e  lugins.<PLUGIN>.
-000043e0: 7465 7374 5d0a 7061 7373 5f61 7267 7320  test].pass_args 
-000043f0: 3d20 5b27 2d2d 6361 7074 7572 653d 6e6f  = ['--capture=no
-00004400: 275d 0a60 6060 0a0a 4569 7468 6572 2077  '].```..Either w
-00004410: 6179 2c20 626f 7468 2077 696c 6c20 7265  ay, both will re
-00004420: 7375 6c74 2069 6e20 6578 6563 7574 696e  sult in executin
-00004430: 6720 6070 7974 6573 7420 7465 7374 7320  g `pytest tests 
-00004440: 2d2d 6361 7074 7572 653d 6e6f 602e 0a0a  --capture=no`...
-00004450: 2323 2320 4669 6c65 7320 6f76 6572 7269  ### Files overri
-00004460: 6465 0a0a 596f 7520 6361 6e20 6f76 6572  de..You can over
-00004470: 7269 6465 2066 696c 6573 2070 6173 7365  ride files passe
-00004480: 6420 746f 2064 6f77 6e73 7472 6561 6d20  d to downstream 
-00004490: 746f 6f6c 7320 6279 2064 6563 6f72 6174  tools by decorat
-000044a0: 696e 6720 636f 6d6d 616e 6473 2077 6974  ing commands wit
-000044b0: 6820 7468 6520 5b60 6465 636f 7261 746f  h the [`decorato
-000044c0: 7273 2e66 696c 6573 5f66 6f6c 6465 7273  rs.files_folders
-000044d0: 5f6f 7074 696f 6e60 5d28 6874 7470 733a  _option`](https:
-000044e0: 2f2f 6769 7468 7562 2e63 6f6d 2f72 6164  //github.com/rad
-000044f0: 656b 6c61 742f 6465 6c66 696e 6f2f 626c  eklat/delfino/bl
-00004500: 6f62 2f6d 6169 6e2f 7372 632f 6465 6c66  ob/main/src/delf
-00004510: 696e 6f2f 6465 636f 7261 746f 7273 2f66  ino/decorators/f
-00004520: 696c 6573 5f66 6f6c 6465 7273 2e70 7929  iles_folders.py)
-00004530: 2064 6563 6f72 6174 6f72 3a0a 0a60 6060   decorator:..```
-00004540: 7079 7468 6f6e 0a23 2063 6f6d 6d61 6e64  python.# command
-00004550: 732f 5f5f 696e 6974 5f5f 2e70 790a 0a66  s/__init__.py..f
-00004560: 726f 6d20 7479 7069 6e67 2069 6d70 6f72  rom typing impor
-00004570: 7420 5475 706c 650a 0a69 6d70 6f72 7420  t Tuple..import 
-00004580: 636c 6963 6b0a 6672 6f6d 2064 656c 6669  click.from delfi
-00004590: 6e6f 2e64 6563 6f72 6174 6f72 7320 696d  no.decorators im
-000045a0: 706f 7274 2066 696c 6573 5f66 6f6c 6465  port files_folde
-000045b0: 7273 5f6f 7074 696f 6e0a 6672 6f6d 2064  rs_option.from d
-000045c0: 656c 6669 6e6f 2e65 7865 6375 7469 6f6e  elfino.execution
-000045d0: 2069 6d70 6f72 7420 7275 6e2c 204f 6e45   import run, OnE
-000045e0: 7272 6f72 0a0a 4063 6c69 636b 2e63 6f6d  rror..@click.com
-000045f0: 6d61 6e64 2829 0a40 6669 6c65 735f 666f  mand().@files_fo
-00004600: 6c64 6572 735f 6f70 7469 6f6e 0a64 6566  lders_option.def
-00004610: 2074 6573 7428 6669 6c65 735f 666f 6c64   test(files_fold
-00004620: 6572 733a 2054 7570 6c65 5b73 7472 2c20  ers: Tuple[str, 
-00004630: 2e2e 2e5d 293a 0a20 2020 2069 6620 6e6f  ...]):.    if no
-00004640: 7420 6669 6c65 735f 666f 6c64 6572 733a  t files_folders:
-00004650: 0a20 2020 2020 2020 2066 696c 6573 5f66  .        files_f
-00004660: 6f6c 6465 7273 203d 2028 2274 6573 7473  olders = ("tests
-00004670: 2f75 6e69 7422 2c20 2274 6573 7473 2f69  /unit", "tests/i
-00004680: 6e74 6567 7261 7469 6f6e 2229 0a20 2020  ntegration").   
-00004690: 2072 756e 285b 2270 7974 6573 7422 2c20   run(["pytest", 
-000046a0: 2a66 696c 6573 5f66 6f6c 6465 7273 5d2c  *files_folders],
-000046b0: 206f 6e5f 6572 726f 723d 4f6e 4572 726f   on_error=OnErro
-000046c0: 722e 4142 4f52 5429 0a60 6060 0a0a 5468  r.ABORT).```..Th
-000046d0: 656e 2074 6865 2064 6566 6175 6c74 2060  en the default `
-000046e0: 2274 6573 7473 2f75 6e69 7422 2c20 2274  "tests/unit", "t
-000046f0: 6573 7473 2f69 6e74 6567 7261 7469 6f6e  ests/integration
-00004700: 2260 2066 6f6c 6465 7273 2063 616e 2062  "` folders can b
-00004710: 6520 6f76 6572 7269 6464 656e 2065 6974  e overridden eit
-00004720: 6865 7220 7669 6120 636f 6d6d 616e 6420  her via command 
-00004730: 6c69 6e65 206f 7074 696f 6e73 2060 2d66  line options `-f
-00004740: 602f 602d 2d66 696c 6560 2f60 2d2d 666f  `/`--file`/`--fo
-00004750: 6c64 6572 603a 0a0a 6060 6073 6865 6c6c  lder`:..```shell
-00004760: 2073 6372 6970 740a 6465 6c66 696e 6f20   script.delfino 
-00004770: 7465 7374 202d 6620 7465 7374 732f 6f74  test -f tests/ot
-00004780: 6865 720a 6060 600a 0a4f 7220 7669 6120  her.```..Or via 
-00004790: 636f 6e66 6967 7572 6174 696f 6e20 696e  configuration in
-000047a0: 2074 6865 2060 7079 7072 6f6a 6563 742e   the `pyproject.
-000047b0: 746f 6d6c 6020 6669 6c65 3a0a 0a60 6060  toml` file:..```
-000047c0: 746f 6d6c 0a5b 746f 6f6c 2e64 656c 6669  toml.[tool.delfi
-000047d0: 6e6f 2e70 6c75 6769 6e73 2e3c 504c 5547  no.plugins.<PLUG
-000047e0: 494e 3e2e 7465 7374 5d0a 6669 6c65 735f  IN>.test].files_
-000047f0: 666f 6c64 6572 7320 3d20 5b27 7465 7374  folders = ['test
-00004800: 732f 6f74 6865 7227 5d0a 6060 600a 0a45  s/other'].```..E
-00004810: 6974 6865 7220 7761 792c 2062 6f74 6820  ither way, both 
-00004820: 7769 6c6c 2072 6573 756c 7420 696e 2065  will result in e
-00004830: 7865 6375 7469 6e67 2060 7079 7465 7374  xecuting `pytest
-00004840: 2074 6573 7473 2f6f 7468 6572 602e 0a0a   tests/other`...
-00004850: 2323 2047 726f 7570 696e 6720 636f 6d6d  ## Grouping comm
-00004860: 616e 6473 0a0a 4f66 7465 6e20 6974 2069  ands..Often it i
-00004870: 7320 7573 6566 756c 2074 6f20 7275 6e20  s useful to run 
-00004880: 7365 7665 7261 6c20 636f 6d6d 616e 6473  several commands
-00004890: 2061 7320 6120 6772 6f75 7020 7769 7468   as a group with
-000048a0: 2061 2064 6966 6665 7265 6e74 2063 6f6d   a different com
-000048b0: 6d61 6e64 206e 616d 652e 2043 6c69 636b  mand name. Click
-000048c0: 2073 7570 706f 7274 7320 6361 6c6c 696e   supports callin
-000048d0: 6720 6f74 6865 7220 636f 6d6d 616e 6473  g other commands
-000048e0: 2077 6974 6820 5b60 636c 6963 6b2e 436f   with [`click.Co
-000048f0: 6e74 6578 742e 666f 7277 6172 6460 5d28  ntext.forward`](
-00004900: 6874 7470 733a 2f2f 636c 6963 6b2e 7061  https://click.pa
-00004910: 6c6c 6574 7370 726f 6a65 6374 732e 636f  lletsprojects.co
-00004920: 6d2f 6170 692f 2363 6c69 636b 2e43 6f6e  m/api/#click.Con
-00004930: 7465 7874 2e66 6f72 7761 7264 2920 6f72  text.forward) or
-00004940: 205b 6063 6c69 636b 2e43 6f6e 7465 7874   [`click.Context
-00004950: 2e69 6e76 6f6b 6560 5d28 6874 7470 733a  .invoke`](https:
-00004960: 2f2f 636c 6963 6b2e 7061 6c6c 6574 7370  //click.palletsp
-00004970: 726f 6a65 6374 732e 636f 6d2f 6170 692f  rojects.com/api/
-00004980: 2363 6c69 636b 2e43 6f6e 7465 7874 2e69  #click.Context.i
-00004990: 6e76 6f6b 6529 2e0a 0a3c 212d 2d20 544f  nvoke)...<!-- TO
-000049a0: 444f 2852 6164 656b 293a 2041 6464 2064  DO(Radek): Add d
-000049b0: 6573 6372 6970 7469 6f6e 206f 6620 6065  escription of `e
-000049c0: 7865 6375 7465 5f63 6f6d 6d61 6e64 735f  xecute_commands_
-000049d0: 6772 6f75 7060 206f 6e63 6520 6d69 6772  group` once migr
-000049e0: 6174 6564 2066 726f 6d20 6064 656c 6669  ated from `delfi
-000049f0: 6e6f 2d63 6f72 6560 2e20 2d2d 3e0a 0a    no-core`. -->..
+00000620: 6967 6e3d 2263 656e 7465 7222 3e54 6865  ign="center">The
+00000630: 2055 6c74 696d 6174 6520 436f 6d6d 616e   Ultimate Comman
+00000640: 6420 4c69 6e65 2043 6f6d 7061 6e69 6f6e  d Line Companion
+00000650: 2066 6f72 2059 6f75 7220 5072 6f6a 6563   for Your Projec
+00000660: 7473 3c2f 6833 3e0a 0a3c 7020 616c 6967  ts</h3>..<p alig
+00000670: 6e3d 2263 656e 7465 7222 3e0a 2020 2020  n="center">.    
+00000680: 3c61 2068 7265 663d 2268 7474 7073 3a2f  <a href="https:/
+00000690: 2f61 7070 2e63 6972 636c 6563 692e 636f  /app.circleci.co
+000006a0: 6d2f 7069 7065 6c69 6e65 732f 6769 7468  m/pipelines/gith
+000006b0: 7562 2f72 6164 656b 6c61 742f 6465 6c66  ub/radeklat/delf
+000006c0: 696e 6f3f 6272 616e 6368 3d6d 6169 6e22  ino?branch=main"
+000006d0: 3e0a 2020 2020 2020 2020 3c69 6d67 2061  >.        <img a
+000006e0: 6c74 3d22 4369 7263 6c65 4349 2220 7372  lt="CircleCI" sr
+000006f0: 633d 2268 7474 7073 3a2f 2f69 6d67 2e73  c="https://img.s
+00000700: 6869 656c 6473 2e69 6f2f 6369 7263 6c65  hields.io/circle
+00000710: 6369 2f62 7569 6c64 2f67 6974 6875 622f  ci/build/github/
+00000720: 7261 6465 6b6c 6174 2f64 656c 6669 6e6f  radeklat/delfino
+00000730: 223e 0a20 2020 203c 2f61 3e0a 2020 2020  ">.    </a>.    
+00000740: 3c61 2068 7265 663d 2268 7474 7073 3a2f  <a href="https:/
+00000750: 2f61 7070 2e63 6f64 6563 6f76 2e69 6f2f  /app.codecov.io/
+00000760: 6768 2f72 6164 656b 6c61 742f 6465 6c66  gh/radeklat/delf
+00000770: 696e 6f2f 223e 0a20 2020 2020 2020 203c  ino/">.        <
+00000780: 696d 6720 616c 743d 2243 6f64 6563 6f76  img alt="Codecov
+00000790: 2220 7372 633d 2268 7474 7073 3a2f 2f69  " src="https://i
+000007a0: 6d67 2e73 6869 656c 6473 2e69 6f2f 636f  mg.shields.io/co
+000007b0: 6465 636f 762f 632f 6769 7468 7562 2f72  decov/c/github/r
+000007c0: 6164 656b 6c61 742f 6465 6c66 696e 6f22  adeklat/delfino"
+000007d0: 3e0a 2020 2020 3c2f 613e 0a20 2020 203c  >.    </a>.    <
+000007e0: 6120 6872 6566 3d22 6874 7470 733a 2f2f  a href="https://
+000007f0: 6769 7468 7562 2e63 6f6d 2f72 6164 656b  github.com/radek
+00000800: 6c61 742f 6465 6c66 696e 6f2f 7461 6773  lat/delfino/tags
+00000810: 223e 0a20 2020 2020 2020 203c 696d 6720  ">.        <img 
+00000820: 616c 743d 2247 6974 4875 6220 7461 6720  alt="GitHub tag 
+00000830: 286c 6174 6573 7420 5365 6d56 6572 2922  (latest SemVer)"
+00000840: 2073 7263 3d22 6874 7470 733a 2f2f 696d   src="https://im
+00000850: 672e 7368 6965 6c64 732e 696f 2f67 6974  g.shields.io/git
+00000860: 6875 622f 7461 672f 7261 6465 6b6c 6174  hub/tag/radeklat
+00000870: 2f64 656c 6669 6e6f 223e 0a20 2020 203c  /delfino">.    <
+00000880: 2f61 3e0a 2020 2020 3c69 6d67 2061 6c74  /a>.    <img alt
+00000890: 3d22 4d61 696e 7465 6e61 6e63 6522 2073  ="Maintenance" s
+000008a0: 7263 3d22 6874 7470 733a 2f2f 696d 672e  rc="https://img.
+000008b0: 7368 6965 6c64 732e 696f 2f6d 6169 6e74  shields.io/maint
+000008c0: 656e 616e 6365 2f79 6573 2f32 3032 3322  enance/yes/2023"
+000008d0: 3e0a 2020 2020 3c61 2068 7265 663d 2268  >.    <a href="h
+000008e0: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
+000008f0: 6d2f 7261 6465 6b6c 6174 2f64 656c 6669  m/radeklat/delfi
+00000900: 6e6f 2f63 6f6d 6d69 7473 2f6d 6169 6e22  no/commits/main"
+00000910: 3e0a 2020 2020 2020 2020 3c69 6d67 2061  >.        <img a
+00000920: 6c74 3d22 4769 7448 7562 206c 6173 7420  lt="GitHub last 
+00000930: 636f 6d6d 6974 2220 7372 633d 2268 7474  commit" src="htt
+00000940: 7073 3a2f 2f69 6d67 2e73 6869 656c 6473  ps://img.shields
+00000950: 2e69 6f2f 6769 7468 7562 2f6c 6173 742d  .io/github/last-
+00000960: 636f 6d6d 6974 2f72 6164 656b 6c61 742f  commit/radeklat/
+00000970: 6465 6c66 696e 6f22 3e0a 2020 2020 3c2f  delfino">.    </
+00000980: 613e 0a20 2020 203c 6120 6872 6566 3d22  a>.    <a href="
+00000990: 6874 7470 733a 2f2f 7777 772e 7079 7468  https://www.pyth
+000009a0: 6f6e 2e6f 7267 2f64 6f63 2f76 6572 7369  on.org/doc/versi
+000009b0: 6f6e 732f 223e 0a20 2020 2020 2020 203c  ons/">.        <
+000009c0: 696d 6720 616c 743d 2250 7950 4920 2d20  img alt="PyPI - 
+000009d0: 5079 7468 6f6e 2056 6572 7369 6f6e 2220  Python Version" 
+000009e0: 7372 633d 2268 7474 7073 3a2f 2f69 6d67  src="https://img
+000009f0: 2e73 6869 656c 6473 2e69 6f2f 7079 7069  .shields.io/pypi
+00000a00: 2f70 7976 6572 7369 6f6e 732f 6465 6c66  /pyversions/delf
+00000a10: 696e 6f22 3e0a 2020 2020 3c2f 613e 0a20  ino">.    </a>. 
+00000a20: 2020 203c 6120 6872 6566 3d22 6874 7470     <a href="http
+00000a30: 733a 2f2f 7079 7069 7374 6174 732e 6f72  s://pypistats.or
+00000a40: 672f 7061 636b 6167 6573 2f64 656c 6669  g/packages/delfi
+00000a50: 6e6f 223e 0a20 2020 2020 2020 203c 696d  no">.        <im
+00000a60: 6720 616c 743d 2244 6f77 6e6c 6f61 6473  g alt="Downloads
+00000a70: 2220 7372 633d 2268 7474 7073 3a2f 2f69  " src="https://i
+00000a80: 6d67 2e73 6869 656c 6473 2e69 6f2f 7079  mg.shields.io/py
+00000a90: 7069 2f64 6d2f 6465 6c66 696e 6f22 3e0a  pi/dm/delfino">.
+00000aa0: 2020 2020 3c2f 613e 0a3c 2f70 3e0a 0a54      </a>.</p>..T
+00000ab0: 6972 6564 206f 6620 6d61 6e61 6769 6e67  ired of managing
+00000ac0: 2073 6361 7474 6572 6564 2073 6372 6970   scattered scrip
+00000ad0: 7473 3f20 5361 7920 676f 6f64 6279 6520  ts? Say goodbye 
+00000ae0: 746f 2063 6f6d 706c 6578 6974 7920 7769  to complexity wi
+00000af0: 7468 2044 656c 6669 6e6f 210a 0a44 656c  th Delfino!..Del
+00000b00: 6669 6e6f 2069 7320 6120 706f 7765 7266  fino is a powerf
+00000b10: 756c 2077 7261 7070 6572 2061 726f 756e  ul wrapper aroun
+00000b20: 6420 436c 6963 6b2c 2074 6865 2070 6f70  d Click, the pop
+00000b30: 756c 6172 2063 6f6d 6d61 6e64 206c 696e  ular command lin
+00000b40: 6520 696e 7465 7266 6163 6520 7061 636b  e interface pack
+00000b50: 6167 652e 2049 7420 6175 746f 6d61 7469  age. It automati
+00000b60: 6361 6c6c 7920 6469 7363 6f76 6572 7320  cally discovers 
+00000b70: 616e 6420 6578 6563 7574 6573 2043 6c69  and executes Cli
+00000b80: 636b 2063 6f6d 6d61 6e64 7320 696e 2079  ck commands in y
+00000b90: 6f75 7220 7072 6f6a 6563 742e 2042 7574  our project. But
+00000ba0: 2044 656c 6669 6e6f 2064 6f65 736e 2774   Delfino doesn't
+00000bb0: 2073 746f 7020 7468 6572 6520 2d20 6974   stop there - it
+00000bc0: 2074 616b 6573 2069 7420 6120 7374 6570   takes it a step
+00000bd0: 2066 7572 7468 6572 2062 7920 616c 6c6f   further by allo
+00000be0: 7769 6e67 2079 6f75 2074 6f20 6372 6561  wing you to crea
+00000bf0: 7465 2070 6c75 6769 6e73 2c20 6d61 6b69  te plugins, maki
+00000c00: 6e67 2073 6372 6970 7420 6469 7374 7269  ng script distri
+00000c10: 6275 7469 6f6e 2061 6e64 2069 6e73 7461  bution and insta
+00000c20: 6c6c 6174 696f 6e20 6120 6272 6565 7a65  llation a breeze
+00000c30: 2e0a 0a23 2057 6879 2063 686f 6f73 6520  ...# Why choose 
+00000c40: 4465 6c66 696e 6f3f 0a0a 2d20 2a2a 5374  Delfino?..- **St
+00000c50: 7265 616d 6c69 6e65 2053 6372 6970 7473  reamline Scripts
+00000c60: 2a2a 3a20 436f 6e73 6f6c 6964 6174 6520  **: Consolidate 
+00000c70: 616c 6c20 796f 7572 2068 656c 7065 7220  all your helper 
+00000c80: 7363 7269 7074 7320 696e 746f 2061 2073  scripts into a s
+00000c90: 696e 676c 652c 2065 6173 792d 746f 2d75  ingle, easy-to-u
+00000ca0: 7365 2065 6e74 7279 2070 6f69 6e74 2e20  se entry point. 
+00000cb0: 4e6f 206d 6f72 6520 6875 6e74 696e 6720  No more hunting 
+00000cc0: 666f 7220 7363 7269 7074 7320 6f72 2064  for scripts or d
+00000cd0: 6561 6c69 6e67 2077 6974 6820 636f 6e76  ealing with conv
+00000ce0: 6f6c 7574 6564 2061 6c69 6173 6573 2e20  oluted aliases. 
+00000cf0: 5369 6d70 6c79 2075 7365 2064 656c 6669  Simply use delfi
+00000d00: 6e6f 2066 6f6c 6c6f 7765 6420 6279 2074  no followed by t
+00000d10: 6865 2073 6372 6970 7420 6e61 6d65 2061  he script name a
+00000d20: 6e64 206f 7074 696f 6e73 2e0a 2d20 2a2a  nd options..- **
+00000d30: 5265 7573 6162 6c65 2050 6c75 6769 6e73  Reusable Plugins
+00000d40: 2a2a 3a20 5061 636b 6167 6520 796f 7572  **: Package your
+00000d50: 2068 656c 7065 7220 7363 7269 7074 7320   helper scripts 
+00000d60: 6173 2070 6c75 6769 6e73 2061 6e64 2069  as plugins and i
+00000d70: 6e73 7461 6c6c 2074 6865 6d20 7769 7468  nstall them with
+00000d80: 2070 6970 2e20 4d61 696e 7461 696e 2063   pip. Maintain c
+00000d90: 6f6e 7369 7374 656e 6379 2061 6372 6f73  onsistency acros
+00000da0: 7320 7072 6f6a 6563 7473 2061 6e64 2065  s projects and e
+00000db0: 6173 696c 7920 696e 636f 7270 6f72 6174  asily incorporat
+00000dc0: 6520 7570 6461 7465 7320 7468 726f 7567  e updates throug
+00000dd0: 6820 6120 666c 6578 6962 6c65 2063 6f6e  h a flexible con
+00000de0: 6669 6775 7261 7469 6f6e 2073 7973 7465  figuration syste
+00000df0: 6d2e 0a2d 202a 2a53 696d 706c 6966 7920  m..- **Simplify 
+00000e00: 546f 6f6c 696e 672a 2a3a 2044 656c 6669  Tooling**: Delfi
+00000e10: 6e6f 2065 7874 656e 6473 2043 6c69 636b  no extends Click
+00000e20: 2077 6974 6820 6164 7661 6e63 6564 2066   with advanced f
+00000e30: 6561 7475 7265 7320 6c69 6b65 2070 6173  eatures like pas
+00000e40: 732d 7468 726f 7567 6820 636f 6d6d 616e  s-through comman
+00000e50: 642d 6c69 6e65 206f 7074 696f 6e73 2061  d-line options a
+00000e60: 6e64 2073 6561 6d6c 6573 7320 6861 6e64  nd seamless hand
+00000e70: 6c69 6e67 206f 6620 6669 6c65 206c 6973  ling of file lis
+00000e80: 7473 2e20 5361 7920 676f 6f64 6279 6520  ts. Say goodbye 
+00000e90: 746f 2076 6572 626f 7369 7479 2061 6e64  to verbosity and
+00000ea0: 2068 656c 6c6f 2074 6f20 6f70 7469 6d69   hello to optimi
+00000eb0: 7a65 6420 776f 726b 666c 6f77 732e 0a0a  zed workflows...
+00000ec0: 446f 6e27 7420 6c65 7420 7363 6174 7465  Don't let scatte
+00000ed0: 7265 6420 7363 7269 7074 7320 616e 6420  red scripts and 
+00000ee0: 636f 6d70 6c65 7820 746f 6f6c 696e 6720  complex tooling 
+00000ef0: 736c 6f77 2079 6f75 2064 6f77 6e2e 2045  slow you down. E
+00000f00: 6d62 7261 6365 2044 656c 6669 6e6f 2061  mbrace Delfino a
+00000f10: 6e64 2072 6576 6f6c 7574 696f 6e69 7a65  nd revolutionize
+00000f20: 2079 6f75 7220 636f 6d6d 616e 6420 6c69   your command li
+00000f30: 6e65 2065 7870 6572 6965 6e63 652e 2054  ne experience. T
+00000f40: 7279 2044 656c 6669 6e6f 2074 6f64 6179  ry Delfino today
+00000f50: 2061 6e64 2075 6e6c 6f63 6b20 7369 6d70   and unlock simp
+00000f60: 6c69 6369 7479 2069 6e20 796f 7572 2070  licity in your p
+00000f70: 726f 6a65 6374 7321 0a0a 3c21 2d2d 0a20  rojects!..<!--. 
+00000f80: 2020 2048 6f77 2074 6f20 6765 6e65 7261     How to genera
+00000f90: 7465 2054 4f43 2066 726f 6d20 5079 4368  te TOC from PyCh
+00000fa0: 6172 6d3a 0a20 2020 2068 7474 7073 3a2f  arm:.    https:/
+00000fb0: 2f67 6974 6875 622e 636f 6d2f 7673 6368  /github.com/vsch
+00000fc0: 2f69 6465 612d 6d75 6c74 696d 6172 6b64  /idea-multimarkd
+00000fd0: 6f77 6e2f 7769 6b69 2f54 6162 6c65 2d6f  own/wiki/Table-o
+00000fe0: 662d 436f 6e74 656e 7473 2d45 7874 656e  f-Contents-Exten
+00000ff0: 7369 6f6e 0a2d 2d3e 0a5b 544f 4320 6c65  sion.-->.[TOC le
+00001000: 7665 6c73 3d31 2c32 206d 6172 6b64 6f77  vels=1,2 markdow
+00001010: 6e20 666f 726d 6174 7465 6420 6275 6c6c  n formatted bull
+00001020: 6574 2068 6965 7261 7263 6879 5d3a 2023  et hierarchy]: #
+00001030: 2022 5461 626c 6520 6f66 2063 6f6e 7465   "Table of conte
+00001040: 6e74 220a 0a23 2054 6162 6c65 206f 6620  nt"..# Table of 
+00001050: 636f 6e74 656e 740a 2d20 5b49 6e73 7461  content.- [Insta
+00001060: 6c6c 6174 696f 6e5d 2823 696e 7374 616c  llation](#instal
+00001070: 6c61 7469 6f6e 290a 2d20 5b43 6f6e 6669  lation).- [Confi
+00001080: 6775 7261 7469 6f6e 5d28 2363 6f6e 6669  guration](#confi
+00001090: 6775 7261 7469 6f6e 290a 2d20 5b55 7361  guration).- [Usa
+000010a0: 6765 5d28 2375 7361 6765 290a 2d20 5b44  ge](#usage).- [D
+000010b0: 6576 656c 6f70 6d65 6e74 5d28 2364 6576  evelopment](#dev
+000010c0: 656c 6f70 6d65 6e74 290a 2020 2d20 5b43  elopment).  - [C
+000010d0: 6f6d 6d61 6e64 7320 6469 7363 6f76 6572  ommands discover
+000010e0: 795d 2823 636f 6d6d 616e 6473 2d64 6973  y](#commands-dis
+000010f0: 636f 7665 7279 290a 2020 2d20 5b4d 696e  covery).  - [Min
+00001100: 696d 616c 2063 6f6d 6d61 6e64 5d28 236d  imal command](#m
+00001110: 696e 696d 616c 2d63 6f6d 6d61 6e64 290a  inimal-command).
+00001120: 2020 2d20 5b4d 696e 696d 616c 2070 6c75    - [Minimal plu
+00001130: 6769 6e5d 2823 6d69 6e69 6d61 6c2d 706c  gin](#minimal-pl
+00001140: 7567 696e 290a 2d20 5b45 7869 7374 696e  ugin).- [Existin
+00001150: 6720 706c 7567 696e 735d 2823 6578 6973  g plugins](#exis
+00001160: 7469 6e67 2d70 6c75 6769 6e73 290a 2020  ting-plugins).  
+00001170: 2d20 5b45 6e61 626c 696e 6720 6120 706c  - [Enabling a pl
+00001180: 7567 696e 5d28 2365 6e61 626c 696e 672d  ugin](#enabling-
+00001190: 612d 706c 7567 696e 290a 2020 2d20 5b45  a-plugin).  - [E
+000011a0: 6e61 626c 696e 672f 6469 7361 626c 696e  nabling/disablin
+000011b0: 6720 636f 6d6d 616e 6473 5d28 2365 6e61  g commands](#ena
+000011c0: 626c 696e 6764 6973 6162 6c69 6e67 2d63  blingdisabling-c
+000011d0: 6f6d 6d61 6e64 7329 0a2d 205b 4164 7661  ommands).- [Adva
+000011e0: 6e63 6564 2075 7361 6765 5d28 2361 6476  nced usage](#adv
+000011f0: 616e 6365 642d 7573 6167 6529 0a20 202d  anced-usage).  -
+00001200: 205b 4175 746f 2d63 6f6d 706c 6574 696f   [Auto-completio
+00001210: 6e5d 2823 6175 746f 2d63 6f6d 706c 6574  n](#auto-complet
+00001220: 696f 6e29 0a20 202d 205b 5275 6e6e 696e  ion).  - [Runnin
+00001230: 6720 6578 7465 726e 616c 2070 726f 6772  g external progr
+00001240: 616d 735d 2823 7275 6e6e 696e 672d 6578  ams](#running-ex
+00001250: 7465 726e 616c 2d70 726f 6772 616d 7329  ternal-programs)
+00001260: 0a20 202d 205b 4f70 7469 6f6e 616c 2064  .  - [Optional d
+00001270: 6570 656e 6465 6e63 6965 735d 2823 6f70  ependencies](#op
+00001280: 7469 6f6e 616c 2d64 6570 656e 6465 6e63  tional-dependenc
+00001290: 6965 7329 0a20 202d 205b 5072 6f6a 6563  ies).  - [Projec
+000012a0: 7420 7365 7474 696e 6773 5d28 2370 726f  t settings](#pro
+000012b0: 6a65 6374 2d73 6574 7469 6e67 7329 0a20  ject-settings). 
+000012c0: 202d 205b 506c 7567 696e 2073 6574 7469   - [Plugin setti
+000012d0: 6e67 735d 2823 706c 7567 696e 2d73 6574  ngs](#plugin-set
+000012e0: 7469 6e67 7329 0a20 202d 205b 5072 6f6a  tings).  - [Proj
+000012f0: 6563 7420 7370 6563 6966 6963 206f 7665  ect specific ove
+00001300: 7272 6964 6573 5d28 2370 726f 6a65 6374  rrides](#project
+00001310: 2d73 7065 6369 6669 632d 6f76 6572 7269  -specific-overri
+00001320: 6465 7329 0a20 202d 205b 4772 6f75 7069  des).  - [Groupi
+00001330: 6e67 2063 6f6d 6d61 6e64 735d 2823 6772  ng commands](#gr
+00001340: 6f75 7069 6e67 2d63 6f6d 6d61 6e64 7329  ouping-commands)
+00001350: 0a0a 2320 496e 7374 616c 6c61 7469 6f6e  ..# Installation
+00001360: 0a0a 2d20 7069 703a 2060 7069 7020 696e  ..- pip: `pip in
+00001370: 7374 616c 6c20 6465 6c66 696e 6f60 0a2d  stall delfino`.-
+00001380: 2050 6f65 7472 793a 2060 706f 6574 7279   Poetry: `poetry
+00001390: 2061 6464 202d 2d67 726f 7570 3d64 6576   add --group=dev
+000013a0: 2064 656c 6669 6e6f 600a 2d20 5069 7065   delfino`.- Pipe
+000013b0: 6e76 3a20 6070 6970 656e 7620 696e 7374  nv: `pipenv inst
+000013c0: 616c 6c20 2d64 2064 656c 6669 6e6f 600a  all -d delfino`.
+000013d0: 0a6f 7220 0a0a 2d20 7069 703a 2060 7069  .or ..- pip: `pi
+000013e0: 7020 696e 7374 616c 6c20 6465 6c66 696e  p install delfin
+000013f0: 6f5b 636f 6d70 6c65 7469 6f6e 5d60 0a2d  o[completion]`.-
+00001400: 2050 6f65 7472 793a 2060 706f 6574 7279   Poetry: `poetry
+00001410: 2061 6464 202d 2d67 726f 7570 3d64 6576   add --group=dev
+00001420: 2064 656c 6669 6e6f 5b63 6f6d 706c 6574   delfino[complet
+00001430: 696f 6e5d 600a 2d20 5069 7065 6e76 3a20  ion]`.- Pipenv: 
+00001440: 6070 6970 656e 7620 696e 7374 616c 6c20  `pipenv install 
+00001450: 2d64 2064 656c 6669 6e6f 5b63 6f6d 706c  -d delfino[compl
+00001460: 6574 696f 6e5d 600a 0a74 6f20 656e 6162  etion]`..to enab
+00001470: 6c65 205b 6175 746f 2d63 6f6d 706c 6574  le [auto-complet
+00001480: 696f 6e5d 2823 6175 746f 2d63 6f6d 706c  ion](#auto-compl
+00001490: 6574 696f 6e29 2e0a 0a23 2043 6f6e 6669  etion)...# Confi
+000014a0: 6775 7261 7469 6f6e 0a0a 416c 6c20 636f  guration..All co
+000014b0: 6e66 6967 7572 6174 696f 6e20 6973 2065  nfiguration is e
+000014c0: 7870 6563 7465 6420 746f 206c 6976 6520  xpected to live 
+000014d0: 696e 206f 6e65 206f 6620 7468 6520 666f  in one of the fo
+000014e0: 6c6c 6f77 696e 6720 6669 6c65 733a 0a0a  llowing files:..
+000014f0: 2d20 6070 7970 726f 6a65 6374 2e74 6f6d  - `pyproject.tom
+00001500: 6c60 2069 6e20 7468 6520 7072 6f6a 6563  l` in the projec
+00001510: 7420 726f 6f74 0a2d 2060 2e64 656c 6669  t root.- `.delfi
+00001520: 6e6f 7263 6020 696e 2074 6865 2070 726f  norc` in the pro
+00001530: 6a65 6374 2072 6f6f 7420 2d20 746f 2061  ject root - to a
+00001540: 6c6c 6f77 2064 6576 2073 7065 6369 6669  llow dev specifi
+00001550: 6320 636f 6e66 6967 2c20 6e6f 7420 736f  c config, not so
+00001560: 7572 6365 2063 6f6e 7472 6f6c 6c65 6420  urce controlled 
+00001570: 6f72 2066 6f72 206e 6f6e 2d50 7974 686f  or for non-Pytho
+00001580: 6e20 7072 6f6a 6563 7473 0a2d 2060 2e64  n projects.- `.d
+00001590: 656c 6669 6e6f 7263 6020 696e 2074 6865  elfinorc` in the
+000015a0: 2075 7365 7220 686f 6d65 2064 6972 6563   user home direc
+000015b0: 746f 7279 202d 2066 6f72 2075 7365 7220  tory - for user 
+000015c0: 746f 6f6c 7320 6176 6169 6c61 626c 6520  tools available 
+000015d0: 696e 2074 6865 2073 7973 7465 6d0a 0a49  in the system..I
+000015e0: 6620 6d75 6c74 6970 6c65 2066 696c 6573  f multiple files
+000015f0: 2061 7265 2064 6973 636f 7665 7265 642c   are discovered,
+00001600: 206f 6e6c 7920 7468 6520 6869 6768 6573   only the highes
+00001610: 7420 6f6e 6520 696e 2074 6865 206c 6973  t one in the lis
+00001620: 7420 7769 6c6c 2062 6520 7573 6564 2e0a  t will be used..
+00001630: 0a54 6865 2066 6f72 6d61 7420 666f 7220  .The format for 
+00001640: 602e 6465 6c66 696e 6f72 6360 2069 7320  `.delfinorc` is 
+00001650: 7468 6520 7361 6d65 2061 7320 666f 7220  the same as for 
+00001660: 6070 7970 726f 6a65 6374 2e74 6f6d 6c60  `pyproject.toml`
+00001670: 2e0a 0a23 2055 7361 6765 0a0a 5275 6e20  ...# Usage..Run 
+00001680: 6064 656c 6669 6e6f 202d 2d68 656c 7060  `delfino --help`
+00001690: 2074 6f20 7365 6520 616c 6c20 6176 6169   to see all avai
+000016a0: 6c61 626c 6520 636f 6d6d 616e 6473 2061  lable commands a
+000016b0: 6e64 2074 6865 6972 2075 7361 6765 2e0a  nd their usage..
+000016c0: 0a23 2044 6576 656c 6f70 6d65 6e74 0a0a  .# Development..
+000016d0: 4465 6c66 696e 6f20 6973 2061 2073 696d  Delfino is a sim
+000016e0: 706c 6520 7772 6170 7065 7220 6172 6f75  ple wrapper arou
+000016f0: 6e64 205b 436c 6963 6b20 636f 6d6d 616e  nd [Click comman
+00001700: 6473 5d28 6874 7470 733a 2f2f 636c 6963  ds](https://clic
+00001710: 6b2e 7061 6c6c 6574 7370 726f 6a65 6374  k.palletsproject
+00001720: 732e 636f 6d2f 7175 6963 6b73 7461 7274  s.com/quickstart
+00001730: 2f23 6261 7369 632d 636f 6e63 6570 7473  /#basic-concepts
+00001740: 2d63 7265 6174 696e 672d 612d 636f 6d6d  -creating-a-comm
+00001750: 616e 6429 2e20 416e 7920 436c 6963 6b20  and). Any Click 
+00001760: 636f 6d6d 616e 6420 7769 6c6c 2062 6520  command will be 
+00001770: 6163 6365 7074 6564 2062 7920 4465 6c66  accepted by Delf
+00001780: 696e 6f2e 0a0a 2323 2043 6f6d 6d61 6e64  ino...## Command
+00001790: 7320 6469 7363 6f76 6572 790a 0a44 656c  s discovery..Del
+000017a0: 6669 6e6f 206c 6f6f 6b73 2066 6f72 2061  fino looks for a
+000017b0: 6e79 205b 6063 6c69 636b 2e43 6f6d 6d61  ny [`click.Comma
+000017c0: 6e64 605d 2868 7474 7073 3a2f 2f63 6c69  nd`](https://cli
+000017d0: 636b 2e70 616c 6c65 7473 7072 6f6a 6563  ck.palletsprojec
+000017e0: 7473 2e63 6f6d 2f65 6e2f 382e 302e 782f  ts.com/en/8.0.x/
+000017f0: 6170 692f 2363 6c69 636b 2e43 6f6d 6d61  api/#click.Comma
+00001800: 6e64 2920 7375 622d 636c 6173 7320 696e  nd) sub-class in
+00001810: 2074 6865 2066 6f6c 6c6f 7769 6e67 206c   the following l
+00001820: 6f63 6174 696f 6e73 3a0a 0a2d 2060 636f  ocations:..- `co
+00001830: 6d6d 616e 6473 6020 666f 6c64 6572 2069  mmands` folder i
+00001840: 6e20 7468 6520 726f 6f74 206f 6620 7468  n the root of th
+00001850: 6520 7072 6f6a 6563 7420 286e 6578 7420  e project (next 
+00001860: 746f 2074 6865 2060 7079 7072 6f6a 6563  to the `pyprojec
+00001870: 742e 746f 6d6c 6020 6669 6c65 292e 2054  t.toml` file). T
+00001880: 6869 7320 6c6f 6361 7469 6f6e 2069 7320  his location is 
+00001890: 7573 6566 756c 2066 6f72 2063 6f6d 6d61  useful for comma
+000018a0: 6e64 7320 7468 6174 2064 6f6e 2774 206e  nds that don't n
+000018b0: 6565 6420 746f 2062 6520 7265 706c 6963  eed to be replic
+000018c0: 6174 6564 2069 6e20 6d75 6c74 6970 6c65  ated in multiple
+000018d0: 206c 6f63 6174 696f 6e73 2f70 726f 6a65   locations/proje
+000018e0: 6374 732e 2054 6f20 6368 616e 6765 2074  cts. To change t
+000018f0: 6865 2064 6566 6175 6c74 206c 6f63 6174  he default locat
+00001900: 696f 6e2c 2075 7365 2074 6865 2060 746f  ion, use the `to
+00001910: 6f6c 2e64 656c 6669 6e6f 2e6c 6f63 616c  ol.delfino.local
+00001920: 5f63 6f6d 6d61 6e64 5f66 6f6c 6465 7273  _command_folders
+00001930: 6020 636f 6e66 6967 206f 7074 696f 6e2e  ` config option.
+00001940: 2049 7420 616c 6c6f 7773 2073 7065 6369   It allows speci
+00001950: 6679 696e 6720 6d6f 7265 2074 6861 6e20  fying more than 
+00001960: 6f6e 6520 666f 6c64 6572 2e0a 2d20 7079  one folder..- py
+00001970: 7468 6f6e 206d 6f64 756c 6520 696d 706f  thon module impo
+00001980: 7274 2070 6174 6820 2860 3c49 4d50 4f52  rt path (`<IMPOR
+00001990: 545f 5041 5448 3e60 2920 7370 6563 6966  T_PATH>`) specif
+000019a0: 6965 6420 6279 2060 656e 7472 795f 706f  ied by `entry_po
+000019b0: 696e 7460 206f 6620 5b61 2070 6c75 6769  int` of [a plugi
+000019c0: 6e5d 2823 6d69 6e69 6d61 6c2d 706c 7567  n](#minimal-plug
+000019d0: 696e 293a 0a20 2060 6060 746f 6d6c 0a20  in):.  ```toml. 
+000019e0: 205b 746f 6f6c 2e70 6f65 7472 792e 706c   [tool.poetry.pl
+000019f0: 7567 696e 735d 2023 204f 7074 696f 6e61  ugins] # Optiona
+00001a00: 6c20 7375 7065 7220 7461 626c 650a 0a20  l super table.. 
+00001a10: 205b 746f 6f6c 2e70 6f65 7472 792e 706c   [tool.poetry.pl
+00001a20: 7567 696e 732e 2264 656c 6669 6e6f 2e70  ugins."delfino.p
+00001a30: 6c75 6769 6e22 5d0a 2020 2264 656c 6669  lugin"].  "delfi
+00001a40: 6e6f 2d3c 504c 5547 494e 5f4e 414d 453e  no-<PLUGIN_NAME>
+00001a50: 2220 3d20 223c 494d 504f 5254 5f50 4154  " = "<IMPORT_PAT
+00001a60: 483e 220a 2020 6060 600a 2d20 466f 6c64  H>".  ```.- Fold
+00001a70: 6572 2073 7065 6369 6669 6564 2069 6e20  er specified in 
+00001a80: 7468 6520 5b63 6f6e 6669 6720 6669 6c65  the [config file
+00001a90: 5d28 2363 6f6e 6669 6775 7261 7469 6f6e  ](#configuration
+00001aa0: 2920 756e 6465 7220 6074 6f6f 6c2e 6465  ) under `tool.de
+00001ab0: 6c66 696e 6f2e 6c6f 6361 6c5f 636f 6d6d  lfino.local_comm
+00001ac0: 616e 6473 5f64 6972 6563 746f 7279 602e  ands_directory`.
+00001ad0: 0a0a 416e 7920 6669 6c65 7320 7374 6172  ..Any files star
+00001ae0: 7469 6e67 2077 6974 6820 616e 2075 6e64  ting with an und
+00001af0: 6572 7363 6f72 652c 2065 7863 6570 7420  erscore, except 
+00001b00: 666f 7220 605f 5f69 6e69 745f 5f2e 7079  for `__init__.py
+00001b10: 602c 2077 696c 6c20 6265 2069 676e 6f72  `, will be ignor
+00001b20: 6564 2e0a 0a3e 202a 2a57 6172 6e69 6e67  ed...> **Warning
+00001b30: 2a2a 0a3e 2046 6f6c 6465 7273 2061 7265  **.> Folders are
+00001b40: 204e 4f54 2069 6e73 7065 6374 6564 2072   NOT inspected r
+00001b50: 6563 7572 7369 7665 6c79 2e20 4966 2079  ecursively. If y
+00001b60: 6f75 2070 6c61 6365 2061 6e79 2063 6f6d  ou place any com
+00001b70: 6d61 6e64 7320 696e 746f 206e 6573 7465  mands into neste
+00001b80: 6420 666f 6c64 6572 732c 2074 6865 7920  d folders, they 
+00001b90: 7769 6c6c 206e 6f74 2062 6520 6c6f 6164  will not be load
+00001ba0: 6564 2062 7920 4465 6c66 696e 6f2e 0a0a  ed by Delfino...
+00001bb0: 0a23 2320 4d69 6e69 6d61 6c20 636f 6d6d  .## Minimal comm
+00001bc0: 616e 640a 0a3c 212d 2d20 544f 444f 2852  and..<!-- TODO(R
+00001bd0: 6164 656b 293a 2044 656c 6669 6e6f 2065  adek): Delfino e
+00001be0: 7870 6563 7473 2060 7079 7072 6f6a 6563  xpects `pyprojec
+00001bf0: 742e 746f 6d6c 6020 636f 6e66 6967 7572  t.toml` configur
+00001c00: 6564 2e20 2d2d 3e0a 3c21 2d2d 2054 4f44  ed. -->.<!-- TOD
+00001c10: 4f28 5261 6465 6b29 3a20 4465 6c66 696e  O(Radek): Delfin
+00001c20: 6f20 6578 7065 6374 7320 506f 6574 7279  o expects Poetry
+00001c30: 206f 7220 5069 7065 6e76 2074 6f20 6265   or Pipenv to be
+00001c40: 2061 7661 696c 6162 6c65 2e20 2d2d 3e0a   available. -->.
+00001c50: 0a31 2e20 4372 6561 7465 2061 2060 636f  .1. Create a `co
+00001c60: 6d6d 616e 6473 6020 666f 6c64 6572 3a0a  mmands` folder:.
+00001c70: 2020 2060 6060 7368 656c 6c20 7363 7269     ```shell scri
+00001c80: 7074 0a20 2020 6d6b 6469 7220 636f 6d6d  pt.   mkdir comm
+00001c90: 616e 6473 0a20 2020 6060 600a 322e 2043  ands.   ```.2. C
+00001ca0: 7265 6174 6520 6120 6063 6f6d 6d61 6e64  reate a `command
+00001cb0: 732f 5f5f 696e 6974 5f5f 2e70 7960 2066  s/__init__.py` f
+00001cc0: 696c 652c 2077 6974 6820 7468 6520 666f  ile, with the fo
+00001cd0: 6c6c 6f77 696e 6720 636f 6e74 656e 743a  llowing content:
+00001ce0: 0a20 2020 6060 6070 7974 686f 6e0a 2020  .   ```python.  
+00001cf0: 2069 6d70 6f72 7420 636c 6963 6b0a 2020   import click.  
+00001d00: 200a 2020 2040 636c 6963 6b2e 636f 6d6d   .   @click.comm
+00001d10: 616e 6428 290a 2020 2064 6566 2063 6f6d  and().   def com
+00001d20: 6d61 6e64 5f74 6573 7428 293a 0a20 2020  mand_test():.   
+00001d30: 2020 2020 2222 2254 6573 7473 2063 6f6d      """Tests com
+00001d40: 6d61 6e64 7320 706c 6163 6564 2069 6e20  mands placed in 
+00001d50: 7468 6520 6063 6f6d 6d61 6e64 7360 2066  the `commands` f
+00001d60: 6f6c 6465 7220 6172 6520 6c6f 6164 6564  older are loaded
+00001d70: 2e22 2222 0a20 2020 2020 2020 7072 696e  .""".       prin
+00001d80: 7428 22e2 9ca8 2054 6869 7320 636f 6d6d  t("... This comm
+00001d90: 616e 6420 776f 726b 7321 20e2 9ca8 2229  and works! ...")
+00001da0: 0a20 2020 6060 600a 332e 2053 6565 2069  .   ```.3. See i
+00001db0: 6620 4465 6c66 696e 6f20 6c6f 6164 7320  f Delfino loads 
+00001dc0: 7468 6520 636f 6d6d 616e 642e 204f 7065  the command. Ope
+00001dd0: 6e20 6120 7465 726d 696e 616c 2061 6e64  n a terminal and
+00001de0: 2069 6e20 7468 6520 726f 6f74 206f 6620   in the root of 
+00001df0: 7468 6520 7072 6f6a 6563 742c 2063 616c  the project, cal
+00001e00: 6c3a 2060 6465 6c66 696e 6f20 2d2d 6865  l: `delfino --he
+00001e10: 6c70 602e 2059 6f75 2073 686f 756c 6420  lp`. You should 
+00001e20: 7365 6520 736f 6d65 7468 696e 6720 6c69  see something li
+00001e30: 6b65 2074 6869 733a 0a20 2020 6060 6074  ke this:.   ```t
+00001e40: 6578 740a 2020 2055 7361 6765 3a20 6465  ext.   Usage: de
+00001e50: 6c66 696e 6f20 5b4f 5054 494f 4e53 5d20  lfino [OPTIONS] 
+00001e60: 434f 4d4d 414e 4420 5b41 5247 535d 2e2e  COMMAND [ARGS]..
+00001e70: 2e0a 2020 200a 2020 204f 7074 696f 6e73  ..   .   Options
+00001e80: 3a0a 2020 2020 202d 2d68 656c 7020 2053  :.     --help  S
+00001e90: 686f 7720 7468 6973 206d 6573 7361 6765  how this message
+00001ea0: 2061 6e64 2065 7869 742e 0a20 2020 0a20   and exit..   . 
+00001eb0: 2020 436f 6d6d 616e 6473 3a0a 2020 2020    Commands:.    
+00001ec0: 202e 2e2e 0a20 2020 2020 636f 6d6d 616e   ....     comman
+00001ed0: 642d 7465 7374 2020 2020 2020 2020 2020  d-test          
+00001ee0: 2020 5465 7374 7320 636f 6d6d 616e 6473    Tests commands
+00001ef0: 2070 6c61 6365 6420 696e 2074 6865 2060   placed in the `
+00001f00: 636f 6d6d 616e 6473 6020 666f 6c64 6572  commands` folder
+00001f10: 2e2e 2e0a 2020 2020 202e 2e2e 0a20 2020  ....     ....   
+00001f20: 6060 600a 342e 2052 756e 2074 6865 2063  ```.4. Run the c
+00001f30: 6f6d 6d61 6e64 2077 6974 6820 6064 656c  ommand with `del
+00001f40: 6669 6e6f 2063 6f6d 6d61 6e64 2d74 6573  fino command-tes
+00001f50: 7460 0a0a 2323 204d 696e 696d 616c 2070  t`..## Minimal p
+00001f60: 6c75 6769 6e0a 0a49 6620 796f 7527 6420  lugin..If you'd 
+00001f70: 6c69 6b65 2074 6f20 7573 6520 6f6e 6520  like to use one 
+00001f80: 6f72 206d 6f72 6520 636f 6d6d 616e 6473  or more commands
+00001f90: 2069 6e20 6d75 6c74 6970 6c65 2070 6c61   in multiple pla
+00001fa0: 6365 732c 2079 6f75 2063 616e 2063 7265  ces, you can cre
+00001fb0: 6174 6520 6120 706c 7567 696e 2e20 4120  ate a plugin. A 
+00001fc0: 706c 7567 696e 2069 7320 6a75 7374 2061  plugin is just a
+00001fd0: 2072 6567 756c 6172 2050 7974 686f 6e20   regular Python 
+00001fe0: 7061 636b 6167 6520 7769 7468 2073 7065  package with spe
+00001ff0: 6369 6669 6320 656e 7472 7920 706f 696e  cific entry poin
+00002000: 7420 7465 6c6c 696e 6720 4465 6c66 696e  t telling Delfin
+00002010: 6f20 6974 2073 686f 756c 6420 7573 6520  o it should use 
+00002020: 6974 2e20 4974 2063 616e 2061 6c73 6f20  it. It can also 
+00002030: 6265 2064 6973 7472 6962 7574 6564 2061  be distributed a
+00002040: 7320 616e 7920 6f74 6865 7220 5079 7468  s any other Pyth
+00002050: 6f6e 2070 6163 6b61 6765 732c 2066 6f72  on packages, for
+00002060: 2065 7861 6d70 6c65 2076 6961 2050 7970   example via Pyp
+00002070: 692e 0a0a 5468 6520 7175 6963 6b65 7374  i...The quickest
+00002080: 2077 6179 2074 6f20 6372 6561 7465 206f   way to create o
+00002090: 6e65 2069 7320 746f 2075 7365 2061 205b  ne is to use a [
+000020a0: 4465 6c66 696e 6f20 706c 7567 696e 2063  Delfino plugin c
+000020b0: 6f6f 6b69 6563 7574 7465 7220 7465 6d70  ookiecutter temp
+000020c0: 6c61 7465 5d28 6874 7470 733a 2f2f 6769  late](https://gi
+000020d0: 7468 7562 2e63 6f6d 2f72 6164 656b 6c61  thub.com/radekla
+000020e0: 742f 6465 6c66 696e 6f2d 706c 7567 696e  t/delfino-plugin
+000020f0: 2d63 6f6f 6b69 6563 7574 7465 722d 7465  -cookiecutter-te
+00002100: 6d70 6c61 7465 292c 2077 6869 6368 2061  mplate), which a
+00002110: 736b 7320 796f 7520 7365 7665 7261 6c20  sks you several 
+00002120: 7175 6573 7469 6f6e 7320 616e 6420 7365  questions and se
+00002130: 7473 2075 7020 7468 6520 7768 6f6c 6520  ts up the whole 
+00002140: 7072 6f6a 6563 742e 0a0a 416c 7465 726e  project...Altern
+00002150: 6174 6976 656c 792c 2079 6f75 2063 616e  atively, you can
+00002160: 2067 6574 2069 6e73 7069 7265 6420 6279   get inspired by
+00002170: 205b 7468 6520 6465 6d6f 2070 6c75 6769   [the demo plugi
+00002180: 6e5d 2868 7474 7073 3a2f 2f67 6974 6875  n](https://githu
+00002190: 622e 636f 6d2f 7261 6465 6b6c 6174 2f64  b.com/radeklat/d
+000021a0: 656c 6669 6e6f 2d64 656d 6f29 206f 7220  elfino-demo) or 
+000021b0: 616e 7920 6f66 2074 6865 206f 7468 6572  any of the other
+000021c0: 205b 6578 6973 7469 6e67 2070 6c75 6769   [existing plugi
+000021d0: 6e73 5d28 2370 6c75 6769 6e73 292e 0a0a  ns](#plugins)...
+000021e0: 2320 4578 6973 7469 6e67 2070 6c75 6769  # Existing plugi
+000021f0: 6e73 0a0a 506c 7567 696e 7320 6361 6e20  ns..Plugins can 
+00002200: 6772 6561 746c 7920 7265 6475 6365 2063  greatly reduce c
+00002210: 6f64 6520 6475 706c 6963 6174 696f 6e20  ode duplication 
+00002220: 616e 642f 6f72 2070 726f 6d6f 7465 2079  and/or promote y
+00002230: 6f75 7220 6f77 6e20 7374 616e 6461 7264  our own standard
+00002240: 7320 696e 206d 756c 7469 706c 6520 706c  s in multiple pl
+00002250: 6163 6573 2e20 466f 7220 6578 616d 706c  aces. For exampl
+00002260: 652c 2079 6f75 2063 616e 2063 7265 6174  e, you can creat
+00002270: 6520 6120 706c 7567 696e 2077 7261 7070  e a plugin wrapp
+00002280: 696e 6720 636f 6d6d 6f6e 206c 696e 7469  ing common linti
+00002290: 6e67 2074 6f6f 6c73 2074 6861 7420 796f  ng tools that yo
+000022a0: 7520 7573 6520 6f6e 2079 6f75 7220 7072  u use on your pr
+000022b0: 6f6a 6563 7473 2c20 696e 636c 7564 696e  ojects, includin
+000022c0: 6720 7468 6569 7220 6465 6661 756c 7420  g their default 
+000022d0: 636f 6e66 6967 7572 6174 696f 6e2e 204b  configuration. K
+000022e0: 6565 7069 6e67 2074 6865 2072 756c 6573  eeping the rules
+000022f0: 2061 6e64 2063 7265 6174 696e 6720 6e65   and creating ne
+00002300: 7720 7072 6f6a 6563 7473 2077 6974 6820  w projects with 
+00002310: 7468 6520 7361 6d65 2073 7479 6c65 2073  the same style s
+00002320: 7564 6465 6e6c 7920 6265 636f 6d65 7320  uddenly becomes 
+00002330: 6120 6d61 7474 6572 206f 6620 696e 7374  a matter of inst
+00002340: 616c 6c69 6e67 206f 6e65 2050 7974 686f  alling one Pytho
+00002350: 6e20 6c69 6272 6172 792e 0a0a 4561 6368  n library...Each
+00002360: 2070 6c75 6769 6e20 6361 6e20 636f 6e74   plugin can cont
+00002370: 6169 6e20 6f6e 6520 6f72 206d 6f72 6520  ain one or more 
+00002380: 436c 6963 6b20 636f 6d6d 616e 6473 2074  Click commands t
+00002390: 6861 7420 6172 6520 6175 746f 6d61 7469  hat are automati
+000023a0: 6361 6c6c 7920 6469 7363 6f76 6572 6564  cally discovered
+000023b0: 2061 6e64 2065 7870 6f73 6564 2062 7920   and exposed by 
+000023c0: 4465 6c66 696e 6f2e 2053 6565 205b 6064  Delfino. See [`d
+000023d0: 656c 6669 6e6f 2d64 656d 6f60 5d28 6874  elfino-demo`](ht
+000023e0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
+000023f0: 2f72 6164 656b 6c61 742f 6465 6c66 696e  /radeklat/delfin
+00002400: 6f2d 6465 6d6f 2920 666f 7220 6120 6d69  o-demo) for a mi
+00002410: 6e69 6d61 6c20 706c 7567 696e 2c20 7768  nimal plugin, wh
+00002420: 6963 6820 7072 6f76 6964 6520 6120 6064  ich provide a `d
+00002430: 656d 6f60 2063 6f6d 6d61 6e64 2070 7269  emo` command pri
+00002440: 6e74 696e 6720 6f75 7420 6120 6d65 7373  nting out a mess
+00002450: 6167 652e 0a0a 4578 6973 7469 6e67 2070  age...Existing p
+00002460: 6c75 6769 6e73 3a0a 0a7c 2050 6c75 6769  lugins:..| Plugi
+00002470: 6e20 6e61 6d65 2020 2020 2020 2020 2020  n name          
+00002480: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002490: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000024a0: 2020 2020 2020 2020 7c20 4465 7363 7269          | Descri
+000024b0: 7074 696f 6e20 2020 2020 2020 2020 2020  ption           
+000024c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000024d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000024e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000024f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002500: 2020 2020 2020 2020 2020 2020 207c 0a7c               |.|
+00002510: 3a2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  :---------------
+00002520: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002530: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002540: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 7c3a  --------------|:
+00002550: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002560: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002570: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002580: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00002590: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+000025a0: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+000025b0: 2d2d 2d7c 0a7c 205b 6465 6c66 696e 6f2d  ---|.| [delfino-
+000025c0: 6465 6d6f 5d28 6874 7470 733a 2f2f 6769  demo](https://gi
+000025d0: 7468 7562 2e63 6f6d 2f72 6164 656b 6c61  thub.com/radekla
+000025e0: 742f 6465 6c66 696e 6f2d 6465 6d6f 2920  t/delfino-demo) 
+000025f0: 2020 2020 7c20 4120 6d69 6e69 6d61 6c20      | A minimal 
+00002600: 706c 7567 696e 2065 7861 6d70 6c65 2066  plugin example f
+00002610: 6f72 2044 656c 6669 6e6f 2e20 436f 6e74  or Delfino. Cont
+00002620: 6169 6e73 206f 6e65 2063 6f6d 6d61 6e64  ains one command
+00002630: 2070 7269 6e74 696e 6720 6120 6d65 7373   printing a mess
+00002640: 6167 652e 2020 2020 2020 2020 2020 2020  age.            
+00002650: 2020 2020 2020 2020 207c 0a7c 205b 6465           |.| [de
+00002660: 6c66 696e 6f2d 636f 7265 5d28 6874 7470  lfino-core](http
+00002670: 733a 2f2f 6769 7468 7562 2e63 6f6d 2f72  s://github.com/r
+00002680: 6164 656b 6c61 742f 6465 6c66 696e 6f2d  adeklat/delfino-
+00002690: 636f 7265 2920 2020 2020 7c20 436f 6d6d  core)     | Comm
+000026a0: 616e 6473 2077 7261 7070 696e 6720 746f  ands wrapping to
+000026b0: 6f6c 7320 7573 6564 2064 7572 696e 6720  ols used during 
+000026c0: 6576 6572 7920 6461 7920 6465 7665 6c6f  every day develo
+000026d0: 706d 656e 7420 286c 696e 7469 6e67 2c20  pment (linting, 
+000026e0: 7465 7374 696e 672c 2064 6570 656e 6465  testing, depende
+000026f0: 6e63 6965 7320 7570 6461 7465 292e 207c  ncies update). |
+00002700: 0a7c 205b 6465 6c66 696e 6f2d 646f 636b  .| [delfino-dock
+00002710: 6572 5d28 6874 7470 733a 2f2f 6769 7468  er](https://gith
+00002720: 7562 2e63 6f6d 2f72 6164 656b 6c61 742f  ub.com/radeklat/
+00002730: 6465 6c66 696e 6f2d 646f 636b 6572 2920  delfino-docker) 
+00002740: 7c20 446f 636b 6572 2062 7569 6c64 2068  | Docker build h
+00002750: 656c 7065 7220 7363 7269 7074 2e20 2020  elper script.   
+00002760: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002770: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002780: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002790: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000027a0: 2020 2020 207c 0a0a 2323 2045 6e61 626c       |..## Enabl
+000027b0: 696e 6720 6120 706c 7567 696e 0a0a 466f  ing a plugin..Fo
+000027c0: 7220 7365 6375 7269 7479 2072 6561 736f  r security reaso
+000027d0: 6e73 2c20 706c 7567 696e 7320 6172 6520  ns, plugins are 
+000027e0: 6469 7361 626c 6564 2062 7920 6465 6661  disabled by defa
+000027f0: 756c 742e 2054 6f20 656e 6162 6c65 2061  ult. To enable a
+00002800: 2070 6c75 6769 6e2c 2079 6f75 2068 6176   plugin, you hav
+00002810: 6520 746f 2069 6e63 6c75 6465 2069 7420  e to include it 
+00002820: 696e 2074 6865 2060 7079 7072 6f6a 6563  in the `pyprojec
+00002830: 742e 746f 6d6c 6020 6669 6c65 3a0a 0a60  t.toml` file:..`
+00002840: 6060 746f 6d6c 0a5b 746f 6f6c 2e64 656c  ``toml.[tool.del
+00002850: 6669 6e6f 2e70 6c75 6769 6e73 2e3c 504c  fino.plugins.<PL
+00002860: 5547 494e 5f4e 414d 453e 5d0a 6060 600a  UGIN_NAME>].```.
+00002870: 0a23 2320 456e 6162 6c69 6e67 2f64 6973  .## Enabling/dis
+00002880: 6162 6c69 6e67 2063 6f6d 6d61 6e64 730a  abling commands.
+00002890: 0a42 7920 6465 6661 756c 742c 2061 6c6c  .By default, all
+000028a0: 2063 6f6d 6d61 6e64 7320 6172 6520 656e   commands are en
+000028b0: 6162 6c65 642e 2055 7365 2060 656e 6162  abled. Use `enab
+000028c0: 6c65 5f63 6f6d 6d61 6e64 7360 206f 7220  le_commands` or 
+000028d0: 6064 6973 6162 6c65 5f63 6f6d 6d61 6e64  `disable_command
+000028e0: 7360 2020 746f 2073 686f 7720 6f6e 6c79  s`  to show only
+000028f0: 2061 2073 7562 7365 7420 6f66 2063 6f6d   a subset of com
+00002900: 6d61 6e64 732e 2049 6620 626f 7468 2075  mands. If both u
+00002910: 7365 642c 2064 6973 6162 6c65 6420 636f  sed, disabled co
+00002920: 6d6d 616e 6473 2061 7265 2073 7562 7472  mmands are subtr
+00002930: 6163 7465 6420 6672 6f6d 2074 6865 2073  acted from the s
+00002940: 6574 206f 6620 656e 6162 6c65 6420 636f  et of enabled co
+00002950: 6d6d 616e 6473 2e0a 0a60 6060 746f 6d6c  mmands...```toml
+00002960: 0a23 205b 746f 6f6c 2e64 656c 6669 6e6f  .# [tool.delfino
+00002970: 2e70 6c75 6769 6e73 2e3c 504c 5547 494e  .plugins.<PLUGIN
+00002980: 5f4e 414d 455f 413e 5d0a 2320 656e 6162  _NAME_A>].# enab
+00002990: 6c65 5f63 6f6d 6d61 6e64 7320 3d20 5b3c  le_commands = [<
+000029a0: 434f 4d4d 414e 445f 4e41 4d45 3e5d 0a23  COMMAND_NAME>].#
+000029b0: 2064 6973 6162 6c65 5f63 6f6d 6d61 6e64   disable_command
+000029c0: 7320 3d20 5b3c 434f 4d4d 414e 445f 4e41  s = [<COMMAND_NA
+000029d0: 4d45 3e5d 0a0a 2320 5b74 6f6f 6c2e 6465  ME>]..# [tool.de
+000029e0: 6c66 696e 6f2e 706c 7567 696e 732e 3c50  lfino.plugins.<P
+000029f0: 4c55 4749 4e5f 4e41 4d45 5f42 3e5d 0a23  LUGIN_NAME_B>].#
+00002a00: 2065 6e61 626c 655f 636f 6d6d 616e 6473   enable_commands
+00002a10: 203d 205b 3c43 4f4d 4d41 4e44 5f4e 414d   = [<COMMAND_NAM
+00002a20: 453e 5d0a 2320 6469 7361 626c 655f 636f  E>].# disable_co
+00002a30: 6d6d 616e 6473 203d 205b 3c43 4f4d 4d41  mmands = [<COMMA
+00002a40: 4e44 5f4e 414d 453e 5d0a 6060 600a 0a23  ND_NAME>].```..#
+00002a50: 2041 6476 616e 6365 6420 7573 6167 650a   Advanced usage.
+00002a60: 0a3c 212d 2d0a 2323 2041 6476 616e 6365  .<!--.## Advance
+00002a70: 6420 436f 6d6d 616e 640a 0a44 656c 6669  d Command..Delfi
+00002a80: 6e6f 2061 6464 7320 6f70 7469 6f6e 616c  no adds optional
+00002a90: 2062 6974 7320 6f66 2066 756e 6374 696f   bits of functio
+00002aa0: 6e61 6c69 7479 206f 6e20 746f 7020 6f66  nality on top of
+00002ab0: 2043 6c69 636b 2e20 5468 6520 666f 6c6c   Click. The foll
+00002ac0: 6f77 696e 6720 6578 616d 706c 6520 6465  owing example de
+00002ad0: 6d6f 6e73 7472 6174 6573 2073 6f6d 6520  monstrates some 
+00002ae0: 6f66 2074 686f 7365 3a0a 0a60 6060 7079  of those:..```py
+00002af0: 7468 6f6e 0a23 2063 6f6d 6d61 6e64 732f  thon.# commands/
+00002b00: 5f5f 696e 6974 5f5f 2e70 790a 0a69 6d70  __init__.py..imp
+00002b10: 6f72 7420 636c 6963 6b0a 0a66 726f 6d20  ort click..from 
+00002b20: 6465 6c66 696e 6f2e 636f 6e74 6578 7473  delfino.contexts
+00002b30: 2069 6d70 6f72 7420 7061 7373 5f61 7070   import pass_app
+00002b40: 5f63 6f6e 7465 7874 2c20 4170 7043 6f6e  _context, AppCon
+00002b50: 7465 7874 0a66 726f 6d20 6465 6c66 696e  text.from delfin
+00002b60: 6f2e 7661 6c69 6461 7469 6f6e 2069 6d70  o.validation imp
+00002b70: 6f72 7420 6173 7365 7274 5f70 6970 5f70  ort assert_pip_p
+00002b80: 6163 6b61 6765 5f69 6e73 7461 6c6c 6564  ackage_installed
+00002b90: 2c20 7079 7072 6f6a 6563 745f 746f 6d6c  , pyproject_toml
+00002ba0: 5f6b 6579 5f6d 6973 7369 6e67 0a0a 4063  _key_missing..@c
+00002bb0: 6c69 636b 2e63 6f6d 6d61 6e64 2829 0a23  lick.command().#
+00002bc0: 2054 6865 2060 7061 7373 5f61 7070 5f63   The `pass_app_c
+00002bd0: 6f6e 7465 7874 6020 6465 636f 7261 746f  ontext` decorato
+00002be0: 7220 6164 6473 2060 4170 7043 6f6e 7465  r adds `AppConte
+00002bf0: 7874 6020 6173 2074 6865 2066 6972 7374  xt` as the first
+00002c00: 2070 6172 616d 6574 6572 2e0a 4070 6173   parameter..@pas
+00002c10: 735f 6170 705f 636f 6e74 6578 740a 6465  s_app_context.de
+00002c20: 6620 636f 6d6d 616e 645f 7465 7374 2861  f command_test(a
+00002c30: 7070 5f63 6f6e 7465 7874 3a20 4170 7043  pp_context: AppC
+00002c40: 6f6e 7465 7874 293a 0a20 2020 2222 2254  ontext):.   """T
+00002c50: 6573 7473 2063 6f6d 6d61 6e64 7320 706c  ests commands pl
+00002c60: 6163 6564 2069 6e20 7468 6520 6063 6f6d  aced in the `com
+00002c70: 6d61 6e64 7360 2066 6f6c 6465 7220 6172  mands` folder ar
+00002c80: 6520 6c6f 6164 6564 2e22 2222 0a20 2020  e loaded.""".   
+00002c90: 2320 5465 7374 206f 7074 696f 6e61 6c20  # Test optional 
+00002ca0: 6465 7065 6e64 656e 6369 6573 2e20 416e  dependencies. An
+00002cb0: 7920 6661 696c 696e 6720 6173 7365 7274  y failing assert
+00002cc0: 696f 6e20 7769 6c6c 2062 6520 7072 696e  ion will be prin
+00002cd0: 7465 6420 6173 3a0a 2020 2023 2043 6f6d  ted as:.   # Com
+00002ce0: 6d61 6e64 2027 3c4e 414d 453e 2720 6973  mand '<NAME>' is
+00002cf0: 206d 6973 636f 6e66 6967 7572 6564 2e20   misconfigured. 
+00002d00: 3c41 5353 4552 5449 4f4e 2045 5252 4f52  <ASSERTION ERROR
+00002d10: 204d 4553 5341 4745 3e0a 2020 2061 7373   MESSAGE>.   ass
+00002d20: 6572 745f 7069 705f 7061 636b 6167 655f  ert_pip_package_
+00002d30: 696e 7374 616c 6c65 6428 2264 656c 6669  installed("delfi
+00002d40: 6e6f 2229 0a0a 2020 2023 2041 7070 436f  no")..   # AppCo
+00002d50: 6e74 6578 7420 636f 6e74 6169 6e20 6120  ntext contain a 
+00002d60: 7061 7273 6564 2060 7079 7072 6f6a 6563  parsed `pyprojec
+00002d70: 742e 746f 6d6c 6020 6669 6c65 2e0a 2020  t.toml` file..  
+00002d80: 2023 2043 6f6d 6d61 6e64 7320 6361 6e20   # Commands can 
+00002d90: 6164 6420 7468 6569 7220 636f 6e66 6967  add their config
+00002da0: 2075 6e64 6572 2060 5b74 6f6f 6c2e 6465   under `[tool.de
+00002db0: 6c66 696e 6f2e 636f 6d6d 616e 6473 2e3c  lfino.commands.<
+00002dc0: 434f 4d4d 414e 445f 4e41 4d45 3e5d 602e  COMMAND_NAME>]`.
+00002dd0: 0a20 2020 6173 7365 7274 2022 636f 6d6d  .   assert "comm
+00002de0: 616e 645f 7465 7374 2220 696e 2061 7070  and_test" in app
+00002df0: 5f63 6f6e 7465 7874 2e70 7970 726f 6a65  _context.pyproje
+00002e00: 6374 5f74 6f6d 6c2e 746f 6f6c 2e64 656c  ct_toml.tool.del
+00002e10: 6669 6e6f 2e63 6f6d 6d61 6e64 732c 205c  fino.commands, \
+00002e20: 0a20 2020 2020 2020 7079 7072 6f6a 6563  .       pyprojec
+00002e30: 745f 746f 6d6c 5f6b 6579 5f6d 6973 7369  t_toml_key_missi
+00002e40: 6e67 2822 746f 6f6c 2e64 656c 6669 6e6f  ng("tool.delfino
+00002e50: 2e63 6f6d 6d61 6e64 732e 636f 6d6d 616e  .commands.comman
+00002e60: 645f 7465 7374 2229 0a0a 2020 2070 7269  d_test")..   pri
+00002e70: 6e74 2861 7070 5f63 6f6e 7465 7874 2e70  nt(app_context.p
+00002e80: 7970 726f 6a65 6374 5f74 6f6d 6c2e 746f  yproject_toml.to
+00002e90: 6f6c 2e64 656c 6669 6e6f 2e63 6f6d 6d61  ol.delfino.comma
+00002ea0: 6e64 735b 2263 6f6d 6d61 6e64 2d74 6573  nds["command-tes
+00002eb0: 7422 5d29 0a60 6060 0a2d 2d3e 0a0a 2323  t"]).```.-->..##
+00002ec0: 2041 7574 6f2d 636f 6d70 6c65 7469 6f6e   Auto-completion
+00002ed0: 0a0a 596f 7520 6361 6e20 6569 7468 6572  ..You can either
+00002ee0: 2061 7474 656d 7074 2074 6f20 696e 7374   attempt to inst
+00002ef0: 616c 6c20 636f 6d70 6c65 7469 6f6e 7320  all completions 
+00002f00: 6175 746f 6d61 7469 6361 6c6c 7920 7769  automatically wi
+00002f10: 7468 3a0a 0a60 6060 7368 656c 6c20 7363  th:..```shell sc
+00002f20: 7269 7074 0a64 656c 6669 6e6f 202d 2d69  ript.delfino --i
+00002f30: 6e73 7461 6c6c 2d63 6f6d 706c 6574 696f  nstall-completio
+00002f40: 6e0a 6060 600a 0a6f 7220 6765 6e65 7261  n.```..or genera
+00002f50: 7465 2069 7420 7769 7468 3a0a 0a60 6060  te it with:..```
+00002f60: 7368 656c 6c20 7363 7269 7074 0a64 656c  shell script.del
+00002f70: 6669 6e6f 202d 2d73 686f 772d 636f 6d70  fino --show-comp
+00002f80: 6c65 7469 6f6e 0a60 6060 0a0a 616e 6420  letion.```..and 
+00002f90: 6d61 6e75 616c 6c79 2070 7574 2069 7420  manually put it 
+00002fa0: 696e 2074 6865 2072 656c 6576 616e 7420  in the relevant 
+00002fb0: 5243 2066 696c 652e 0a0a 5468 6520 6175  RC file...The au
+00002fc0: 746f 2d63 6f6d 706c 6574 696f 6e20 696d  to-completion im
+00002fd0: 706c 656d 656e 7461 7469 6f6e 2069 7320  plementation is 
+00002fe0: 6479 6e61 6d69 6320 736f 2074 6861 7420  dynamic so that 
+00002ff0: 6576 6572 7920 7469 6d65 2069 7420 6973  every time it is
+00003000: 2069 6e76 6f6b 6564 2c20 6974 2075 7365   invoked, it use
+00003010: 7320 7468 6520 6375 7272 656e 7420 7072  s the current pr
+00003020: 6f6a 6563 742e 2045 6163 6820 7072 6f6a  oject. Each proj
+00003030: 6563 7420 6361 6e20 6861 7665 2064 6966  ect can have dif
+00003040: 6665 7265 6e74 2063 6f6d 6d61 6e64 7320  ferent commands 
+00003050: 6f72 2064 6973 6162 6c65 2063 6572 7461  or disable certa
+00003060: 696e 2063 6f6d 6d61 6e64 7320 6974 2064  in commands it d
+00003070: 6f65 736e 2774 2075 7365 2e20 416e 6420  oesn't use. And 
+00003080: 6479 6e61 6d69 6320 6175 746f 2d63 6f6d  dynamic auto-com
+00003090: 706c 6574 696f 6e20 6d61 6b65 7320 7375  pletion makes su
+000030a0: 7265 206f 6e6c 7920 7468 6520 6375 7272  re only the curr
+000030b0: 656e 746c 7920 6176 6169 6c61 626c 6520  ently available 
+000030c0: 636f 6d6d 616e 6473 2077 696c 6c20 6265  commands will be
+000030d0: 2073 7567 6765 7374 6564 2e0a 0a54 6865   suggested...The
+000030e0: 2064 6f77 6e73 6964 6520 6f66 2074 6869   downside of thi
+000030f0: 7320 6170 7072 6f61 6368 2069 7320 7468  s approach is th
+00003100: 6174 2065 7661 6c75 6174 696e 6720 7768  at evaluating wh
+00003110: 6174 2069 7320 6176 6169 6c61 626c 6520  at is available 
+00003120: 6561 6368 2074 696d 6520 6973 2073 6c6f  each time is slo
+00003130: 7765 7220 7468 616e 2061 2073 7461 7469  wer than a stati
+00003140: 6320 6c69 7374 206f 6620 636f 6d6d 616e  c list of comman
+00003150: 6473 2e0a 0a23 2320 5275 6e6e 696e 6720  ds...## Running 
+00003160: 6578 7465 726e 616c 2070 726f 6772 616d  external program
+00003170: 730a 0a49 7420 6973 2075 7020 746f 2079  s..It is up to y
+00003180: 6f75 2068 6f77 2079 6f75 2077 616e 7420  ou how you want 
+00003190: 746f 2065 7865 6375 7465 2065 7874 6572  to execute exter
+000031a0: 6e61 6c20 7072 6f63 6573 7365 7320 6173  nal processes as
+000031b0: 2070 6172 7420 6f66 2063 6f6d 6d61 6e64   part of command
+000031c0: 7320 2869 6620 796f 7520 6e65 6564 2074  s (if you need t
+000031d0: 6f20 6174 2061 6c6c 292e 2041 2063 6f6d  o at all). A com
+000031e0: 6d6f 6e20 7761 7920 696e 2050 7974 686f  mon way in Pytho
+000031f0: 6e20 6973 2074 6f20 7573 6520 6073 7562  n is to use `sub
+00003200: 7072 6f63 6573 732e 7275 6e60 2e20 4465  process.run`. De
+00003210: 6c66 696e 6f20 636f 6d65 7320 7769 7468  lfino comes with
+00003220: 2069 7473 206f 776e 205b 6072 756e 6020   its own [`run` 
+00003230: 696d 706c 656d 656e 7461 7469 6f6e 5d28  implementation](
+00003240: 6874 7470 733a 2f2f 6769 7468 7562 2e63  https://github.c
+00003250: 6f6d 2f72 6164 656b 6c61 742f 6465 6c66  om/radeklat/delf
+00003260: 696e 6f2f 626c 6f62 2f6d 6169 6e2f 7372  ino/blob/main/sr
+00003270: 632f 6465 6c66 696e 6f2f 6578 6563 7574  c/delfino/execut
+00003280: 696f 6e2e 7079 234c 3934 292c 2077 6869  ion.py#L94), whi
+00003290: 6368 2077 7261 7073 2061 6e64 2073 696d  ch wraps and sim
+000032a0: 706c 6966 6965 7320 6073 7562 7072 6f63  plifies `subproc
+000032b0: 6573 732e 7275 6e60 2066 6f72 2074 6865  ess.run` for the
+000032c0: 206d 6f73 7420 636f 6d6d 6f6e 2075 7365   most common use
+000032d0: 2063 6173 6573 3a0a 0a2d 204e 6f72 6d61   cases:..- Norma
+000032e0: 6c69 7a69 6e67 2060 7375 6270 726f 6365  lizing `subproce
+000032f0: 7373 2e72 756e 6020 6172 6775 6d65 6e74  ss.run` argument
+00003300: 7320 2d20 796f 7520 6361 6e20 7061 7373  s - you can pass
+00003310: 2069 6e20 6569 7468 6572 2061 2073 7472   in either a str
+00003320: 696e 6720 6f72 2061 206c 6973 742e 2045  ing or a list. E
+00003330: 6974 6865 7220 7761 792c 2060 7375 6270  ither way, `subp
+00003340: 726f 6365 7373 2e72 756e 6020 7769 6c6c  rocess.run` will
+00003350: 2062 6520 6578 6563 7574 6564 2063 6f72   be executed cor
+00003360: 7265 6374 6c79 2e0a 2d20 4861 6e64 6c69  rectly..- Handli
+00003370: 6e67 2065 7272 6f72 7320 6672 6f6d 2074  ng errors from t
+00003380: 6865 2065 7865 6375 7469 6f6e 2076 6961  he execution via
+00003390: 2074 6865 2060 6f6e 5f65 7272 6f72 6020   the `on_error` 
+000033a0: 6172 6775 6d65 6e74 2e20 4769 7669 6e67  argument. Giving
+000033b0: 2074 6865 206f 7074 696f 6e20 746f 2065   the option to e
+000033c0: 6974 6865 7220 6967 6e6f 7265 2074 6865  ither ignore the
+000033d0: 2065 7272 6f72 7320 616e 6420 636f 6e74   errors and cont
+000033e0: 696e 7565 2028 6050 4153 5360 292c 206e  inue (`PASS`), n
+000033f0: 6f74 2063 6f6e 7469 6e75 6520 616e 6420  ot continue and 
+00003400: 636c 6561 6e20 6578 6974 2028 6045 5849  clean exit (`EXI
+00003410: 5460 2920 6f72 206e 6f74 2063 6f6e 7469  T`) or not conti
+00003420: 6e75 6520 616e 6420 6162 6f72 7420 7769  nue and abort wi
+00003430: 7468 2065 7272 6f72 2063 6f64 6520 2860  th error code (`
+00003440: 4142 4f52 5460 292e 0a2d 2053 6574 7469  ABORT`)..- Setti
+00003450: 6e67 2065 6e76 6972 6f6e 6d65 6e74 2076  ng environment v
+00003460: 6172 6961 626c 6573 2e0a 2d20 4c6f 6767  ariables..- Logg
+00003470: 696e 6720 7768 6174 2069 7320 6265 696e  ing what is bein
+00003480: 6720 6578 6563 7574 6564 2069 6e20 7468  g executed in th
+00003490: 6520 6465 6275 6720 6c65 7665 6c2e 0a0a  e debug level...
+000034a0: 4578 616d 706c 653a 0a0a 6060 6070 7974  Example:..```pyt
+000034b0: 686f 6e0a 2320 636f 6d6d 616e 6473 2f5f  hon.# commands/_
+000034c0: 5f69 6e69 745f 5f2e 7079 0a0a 696d 706f  _init__.py..impo
+000034d0: 7274 2063 6c69 636b 0a66 726f 6d20 6465  rt click.from de
+000034e0: 6c66 696e 6f2e 6578 6563 7574 696f 6e20  lfino.execution 
+000034f0: 696d 706f 7274 2072 756e 2c20 4f6e 4572  import run, OnEr
+00003500: 726f 720a 0a40 636c 6963 6b2e 636f 6d6d  ror..@click.comm
+00003510: 616e 6428 290a 6465 6620 7465 7374 2829  and().def test()
+00003520: 3a0a 2020 2020 7275 6e28 2270 7974 6573  :.    run("pytes
+00003530: 7420 7465 7374 7322 2c20 6f6e 5f65 7272  t tests", on_err
+00003540: 6f72 3d4f 6e45 7272 6f72 2e41 424f 5254  or=OnError.ABORT
+00003550: 290a 6060 600a 0a23 2320 4f70 7469 6f6e  ).```..## Option
+00003560: 616c 2064 6570 656e 6465 6e63 6965 730a  al dependencies.
+00003570: 0a49 6620 796f 7520 7075 7420 7365 7665  .If you put seve
+00003580: 7261 6c20 636f 6d6d 616e 6473 2069 6e74  ral commands int
+00003590: 6f20 6f6e 6520 5b70 6c75 6769 6e5d 2823  o one [plugin](#
+000035a0: 706c 7567 696e 7329 2c20 796f 7520 6361  plugins), you ca
+000035b0: 6e20 6d61 6b65 2073 6f6d 6520 6465 7065  n make some depe
+000035c0: 6e64 656e 6369 6573 206f 6620 736f 6d65  ndencies of some
+000035d0: 2063 6f6d 6d61 6e64 7320 5b6f 7074 696f   commands [optio
+000035e0: 6e61 6c5d 2868 7474 7073 3a2f 2f70 7974  nal](https://pyt
+000035f0: 686f 6e2d 706f 6574 7279 2e6f 7267 2f64  hon-poetry.org/d
+00003600: 6f63 732f 7079 7072 6f6a 6563 7423 6578  ocs/pyproject#ex
+00003610: 7472 6173 292e 2054 6869 7320 6973 2075  tras). This is u
+00003620: 7365 6675 6c20 7768 656e 2061 2063 6f6d  seful when a com
+00003630: 6d61 6e64 2069 7320 6e6f 7420 616c 7761  mand is not alwa
+00003640: 7973 2075 7365 642c 2061 6e64 2079 6f75  ys used, and you
+00003650: 2064 6f6e 2774 2077 616e 7420 746f 2069   don't want to i
+00003660: 6e73 7461 6c6c 2075 6e6e 6563 6573 7361  nstall unnecessa
+00003670: 7279 2064 6570 656e 6465 6e63 6965 732e  ry dependencies.
+00003680: 2049 6e73 7465 6164 2c20 796f 7520 6361   Instead, you ca
+00003690: 6e20 6368 6563 6b20 6966 2061 2064 6570  n check if a dep
+000036a0: 656e 6465 6e63 7920 6973 2069 6e73 7461  endency is insta
+000036b0: 6c6c 6564 206f 6e6c 7920 7768 656e 2074  lled only when t
+000036c0: 6865 2063 6f6d 6d61 6e64 2069 7320 6578  he command is ex
+000036d0: 6563 7574 6564 2077 6974 6820 6064 656c  ecuted with `del
+000036e0: 6669 6e6f 2e76 616c 6964 6174 696f 6e2e  fino.validation.
+000036f0: 6173 7365 7274 5f70 6970 5f70 6163 6b61  assert_pip_packa
+00003700: 6765 5f69 6e73 7461 6c6c 6564 603a 0a0a  ge_installed`:..
+00003710: 6060 6070 7974 686f 6e0a 2320 636f 6d6d  ```python.# comm
+00003720: 616e 6473 2f5f 5f69 6e69 745f 5f2e 7079  ands/__init__.py
+00003730: 0a0a 696d 706f 7274 2063 6c69 636b 0a66  ..import click.f
+00003740: 726f 6d20 6465 6c66 696e 6f2e 7661 6c69  rom delfino.vali
+00003750: 6461 7469 6f6e 2069 6d70 6f72 7420 6173  dation import as
+00003760: 7365 7274 5f70 6970 5f70 6163 6b61 6765  sert_pip_package
+00003770: 5f69 6e73 7461 6c6c 6564 0a0a 7472 793a  _installed..try:
+00003780: 0a20 2020 2066 726f 6d20 6769 7420 696d  .    from git im
+00003790: 706f 7274 2052 6570 6f0a 6578 6365 7074  port Repo.except
+000037a0: 2049 6d70 6f72 7445 7272 6f72 3a0a 2020   ImportError:.  
+000037b0: 2020 7061 7373 0a0a 4063 6c69 636b 2e63    pass..@click.c
+000037c0: 6f6d 6d61 6e64 2829 0a64 6566 2067 6974  ommand().def git
+000037d0: 5f61 6374 6976 655f 6272 616e 6368 2829  _active_branch()
+000037e0: 3a0a 2020 2020 6173 7365 7274 5f70 6970  :.    assert_pip
+000037f0: 5f70 6163 6b61 6765 5f69 6e73 7461 6c6c  _package_install
+00003800: 6564 2822 6769 7470 7974 686f 6e22 290a  ed("gitpython").
+00003810: 2020 2020 7072 696e 7428 5265 706f 2822      print(Repo("
+00003820: 2e22 292e 6163 7469 7665 5f62 7261 6e63  .").active_branc
+00003830: 6829 0a60 6060 0a0a 496e 2074 6865 2065  h).```..In the e
+00003840: 7861 6d70 6c65 2061 626f 7665 2c20 6966  xample above, if
+00003850: 2060 6769 7470 7974 686f 6e60 2069 7320   `gitpython` is 
+00003860: 6e6f 7420 696e 7374 616c 6c65 642c 2064  not installed, d
+00003870: 656c 6669 6e6f 2077 696c 6c20 7368 6f77  elfino will show
+00003880: 2074 6865 2063 6f6d 6d61 6e64 2062 7574   the command but
+00003890: 2077 696c 6c20 6661 696c 2077 6974 6820   will fail with 
+000038a0: 7375 6767 6573 7469 6f6e 2074 6f20 696e  suggestion to in
+000038b0: 7374 616c 6c20 6067 6974 7079 7468 6f6e  stall `gitpython
+000038c0: 6020 6f6e 6c79 2077 6865 6e20 7468 6520  ` only when the 
+000038d0: 636f 6d6d 616e 6420 6973 2065 7865 6375  command is execu
+000038e0: 7465 642e 2059 6f75 2063 616e 2061 6c73  ted. You can als
+000038f0: 6f20 6164 6420 6067 6974 5f61 6374 6976  o add `git_activ
+00003900: 655f 6272 616e 6368 6020 696e 746f 205b  e_branch` into [
+00003910: 6064 6973 6162 6c65 5f63 6f6d 6d61 6e64  `disable_command
+00003920: 7360 2063 6f6e 6669 675d 2823 656e 6162  s` config](#enab
+00003930: 6c69 6e67 6469 7361 626c 696e 672d 636f  lingdisabling-co
+00003940: 6d6d 616e 6473 2920 696e 2070 6c61 6365  mmands) in place
+00003950: 7320 7768 6572 6520 796f 7520 646f 6e27  s where you don'
+00003960: 7420 696e 7465 6e64 2074 6f20 7573 6520  t intend to use 
+00003970: 6974 2e0a 0a54 6869 7320 7761 7920 796f  it...This way yo
+00003980: 7520 6361 6e20 6772 6561 746c 7920 7265  u can greatly re
+00003990: 6475 6365 2074 6865 206e 756d 6265 7220  duce the number 
+000039a0: 6f66 2064 6570 656e 6465 6e63 6965 7320  of dependencies 
+000039b0: 6120 706c 7567 696e 2062 7269 6e67 7320  a plugin brings 
+000039c0: 696e 746f 2061 2070 726f 6a65 6374 2077  into a project w
+000039d0: 6974 686f 7574 2061 206e 6565 6420 746f  ithout a need to
+000039e0: 2068 6176 6520 6d61 6e79 2073 6d61 6c6c   have many small
+000039f0: 2070 6c75 6769 6e73 2e0a 0a23 2320 5072   plugins...## Pr
+00003a00: 6f6a 6563 7420 7365 7474 696e 6773 0a0a  oject settings..
+00003a10: 596f 7520 6361 6e20 7374 6f72 6520 616e  You can store an
+00003a20: 2061 7262 6974 7261 7279 206f 626a 6563   arbitrary objec
+00003a30: 7420 696e 2074 6865 2043 6c69 636b 2063  t in the Click c
+00003a40: 6f6e 7465 7874 2061 7320 5b60 636c 6963  ontext as [`clic
+00003a50: 6b2e 436f 6e74 6578 742e 6f62 6a60 5d28  k.Context.obj`](
+00003a60: 6874 7470 733a 2f2f 636c 6963 6b2e 7061  https://click.pa
+00003a70: 6c6c 6574 7370 726f 6a65 6374 732e 636f  lletsprojects.co
+00003a80: 6d2f 6170 692f 2363 6c69 636b 2e43 6f6e  m/api/#click.Con
+00003a90: 7465 7874 2e6f 626a 292e 2044 656c 6669  text.obj). Delfi
+00003aa0: 6e6f 2075 7469 6c69 7a65 7320 7468 6973  no utilizes this
+00003ab0: 206f 626a 6563 7420 746f 2073 746f 7265   object to store
+00003ac0: 2061 6e20 696e 7374 616e 6365 206f 6620   an instance of 
+00003ad0: 5b60 4170 7043 6f6e 7465 7874 605d 2868  [`AppContext`](h
+00003ae0: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
+00003af0: 6d2f 7261 6465 6b6c 6174 2f64 656c 6669  m/radeklat/delfi
+00003b00: 6e6f 2f62 6c6f 622f 6d61 696e 2f73 7263  no/blob/main/src
+00003b10: 2f64 656c 6669 6e6f 2f6d 6f64 656c 732f  /delfino/models/
+00003b20: 6170 705f 636f 6e74 6578 742e 7079 292c  app_context.py),
+00003b30: 2077 6869 6368 2070 726f 7669 6465 7320   which provides 
+00003b40: 6163 6365 7373 2074 6f20 7072 6f6a 6563  access to projec
+00003b50: 7420 7265 6c61 7465 6420 696e 666f 726d  t related inform
+00003b60: 6174 696f 6e2e 2049 6620 796f 7520 6e65  ation. If you ne
+00003b70: 6564 2074 6f2c 2079 6f75 2063 616e 2073  ed to, you can s
+00003b80: 7469 6c6c 2061 7474 6163 6820 6172 6269  till attach arbi
+00003b90: 7472 6172 7920 6174 7472 6962 7574 6573  trary attributes
+00003ba0: 2074 6f20 7468 6973 206f 626a 6563 7420   to this object 
+00003bb0: 6c61 7465 722e 0a0a 596f 7520 6361 6e20  later...You can 
+00003bc0: 7061 7373 2074 6869 7320 6f62 6a65 6374  pass this object
+00003bd0: 2074 6f20 796f 7572 2063 6f6d 6d61 6e64   to your command
+00003be0: 7320 6279 2064 6563 6f72 6174 696e 6720  s by decorating 
+00003bf0: 7468 656d 2077 6974 6820 5b60 636c 6963  them with [`clic
+00003c00: 6b2e 7061 7373 5f6f 626a 605d 2868 7474  k.pass_obj`](htt
+00003c10: 7073 3a2f 2f63 6c69 636b 2e70 616c 6c65  ps://click.palle
+00003c20: 7473 7072 6f6a 6563 7473 2e63 6f6d 2f61  tsprojects.com/a
+00003c30: 7069 2f23 636c 6963 6b2e 7061 7373 5f6f  pi/#click.pass_o
+00003c40: 626a 293a 0a0a 6060 6070 7974 686f 6e0a  bj):..```python.
+00003c50: 2320 636f 6d6d 616e 6473 2f5f 5f69 6e69  # commands/__ini
+00003c60: 745f 5f2e 7079 0a0a 696d 706f 7274 2063  t__.py..import c
+00003c70: 6c69 636b 0a66 726f 6d20 6465 6c66 696e  lick.from delfin
+00003c80: 6f2e 6d6f 6465 6c73 2e61 7070 5f63 6f6e  o.models.app_con
+00003c90: 7465 7874 2069 6d70 6f72 7420 4170 7043  text import AppC
+00003ca0: 6f6e 7465 7874 0a0a 4063 6c69 636b 2e63  ontext..@click.c
+00003cb0: 6f6d 6d61 6e64 2829 0a40 636c 6963 6b2e  ommand().@click.
+00003cc0: 7061 7373 5f6f 626a 0a64 6566 2070 7269  pass_obj.def pri
+00003cd0: 6e74 5f61 7070 5f76 6572 7369 6f6e 286f  nt_app_version(o
+00003ce0: 626a 3a20 4170 7043 6f6e 7465 7874 293a  bj: AppContext):
+00003cf0: 0a20 2020 2070 7269 6e74 286f 626a 2e70  .    print(obj.p
+00003d00: 7970 726f 6a65 6374 5f74 6f6d 6c2e 746f  yproject_toml.to
+00003d10: 6f6c 2e70 6f65 7472 792e 7665 7273 696f  ol.poetry.versio
+00003d20: 6e29 0a60 6060 0a0a 2323 2050 6c75 6769  n).```..## Plugi
+00003d30: 6e20 7365 7474 696e 6773 0a0a 506c 7567  n settings..Plug
+00003d40: 696e 2073 6574 7469 6e67 7320 6172 6520  in settings are 
+00003d50: 6578 7065 6374 6564 2074 6f20 6c69 7665  expected to live
+00003d60: 2069 6e20 7468 6520 6070 7970 726f 6a65   in the `pyproje
+00003d70: 6374 2e74 6f6d 6c60 2066 696c 652e 2054  ct.toml` file. T
+00003d80: 6f20 7072 6576 656e 7420 6e61 6d69 6e67  o prevent naming
+00003d90: 2063 6f6e 666c 6963 7473 2c20 6561 6368   conflicts, each
+00003da0: 2070 6c75 6769 6e20 6d75 7374 2070 7574   plugin must put
+00003db0: 2069 7473 2073 6574 7469 6e67 7320 756e   its settings un
+00003dc0: 6465 7220 6074 6f6f 6c2e 6465 6c66 696e  der `tool.delfin
+00003dd0: 6f2e 706c 7567 696e 732e 3c50 4c55 4749  o.plugins.<PLUGI
+00003de0: 4e5f 4e41 4d45 3e60 2e20 4974 2061 6c73  N_NAME>`. It als
+00003df0: 6f20 616c 6c6f 7773 2044 656c 6669 6e6f  o allows Delfino
+00003e00: 2074 6f20 7061 7373 2074 6865 7365 2073   to pass these s
+00003e10: 6574 7469 6e67 7320 6469 7265 6374 6c79  ettings directly
+00003e20: 2074 6f20 636f 6d6d 616e 6473 2066 726f   to commands fro
+00003e30: 6d20 7468 6573 6520 706c 7567 696e 732e  m these plugins.
+00003e40: 0a0a 4465 6c66 696e 6f20 6c6f 6164 732c  ..Delfino loads,
+00003e50: 2070 6172 7365 732c 2076 616c 6964 6174   parses, validat
+00003e60: 6573 2061 6e64 2073 746f 7265 7320 706c  es and stores pl
+00003e70: 7567 696e 2073 6574 7469 6e67 7320 696e  ugin settings in
+00003e80: 205b 6041 7070 436f 6e74 6578 742e 706c   [`AppContext.pl
+00003e90: 7567 696e 5f63 6f6e 6669 6760 5d28 6874  ugin_config`](ht
+00003ea0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
+00003eb0: 2f72 6164 656b 6c61 742f 6465 6c66 696e  /radeklat/delfin
+00003ec0: 6f2f 626c 6f62 2f6d 6169 6e2f 7372 632f  o/blob/main/src/
+00003ed0: 6465 6c66 696e 6f2f 6d6f 6465 6c73 2f61  delfino/models/a
+00003ee0: 7070 5f63 6f6e 7465 7874 2e70 7929 2e20  pp_context.py). 
+00003ef0: 4966 206e 6f74 2073 7065 6369 6669 6564  If not specified
+00003f00: 206f 7468 6572 7769 7365 2028 7365 6520   otherwise (see 
+00003f10: 6265 6c6f 7729 2c20 6974 2077 696c 6c20  below), it will 
+00003f20: 6265 2061 6e20 696e 7374 616e 6365 206f  be an instance o
+00003f30: 6620 5b60 506c 7567 696e 436f 6e66 6967  f [`PluginConfig
+00003f40: 605d 2868 7474 7073 3a2f 2f67 6974 6875  `](https://githu
+00003f50: 622e 636f 6d2f 7261 6465 6b6c 6174 2f64  b.com/radeklat/d
+00003f60: 656c 6669 6e6f 2f62 6c6f 622f 6d61 696e  elfino/blob/main
+00003f70: 2f73 7263 2f64 656c 6669 6e6f 2f6d 6f64  /src/delfino/mod
+00003f80: 656c 732f 7079 7072 6f6a 6563 745f 746f  els/pyproject_to
+00003f90: 6d6c 2e70 7929 2c20 7769 7468 2061 6e79  ml.py), with any
+00003fa0: 2065 7874 7261 206b 6579 7320 756e 7661   extra keys unva
+00003fb0: 6c69 6461 7465 6420 616e 6420 696e 204a  lidated and in J
+00003fc0: 534f 4e2d 6c69 6b65 2050 7974 686f 6e20  SON-like Python 
+00003fd0: 6f62 6a65 6374 732e 0a0a 596f 7520 6361  objects...You ca
+00003fe0: 6e20 6164 6420 6164 6469 7469 6f6e 616c  n add additional
+00003ff0: 2076 616c 6964 6174 696f 6e20 746f 2079   validation to y
+00004000: 6f75 7220 706c 7567 696e 2073 6574 7469  our plugin setti
+00004010: 6e67 7320 6279 2073 7562 2d63 6c61 7373  ngs by sub-class
+00004020: 696e 6720 7468 6520 6050 6c75 6769 6e43  ing the `PluginC
+00004030: 6f6e 6669 6760 202c 2064 6566 696e 696e  onfig` , definin
+00004040: 6720 6578 7065 6374 6564 206b 6579 732c  g expected keys,
+00004050: 2064 6566 6175 6c74 2076 616c 7565 7320   default values 
+00004060: 616e 642f 6f72 2076 616c 6964 6174 696f  and/or validatio
+00004070: 6e2e 2044 656c 6669 6e6f 2075 7469 6c69  n. Delfino utili
+00004080: 7a65 7320 5b60 7079 6461 6e74 6963 605d  zes [`pydantic`]
+00004090: 2868 7474 7073 3a2f 2f64 6f63 732e 7079  (https://docs.py
+000040a0: 6461 6e74 6963 2e64 6576 2f29 2074 6f20  dantic.dev/) to 
+000040b0: 6372 6561 7465 2064 6174 6120 636c 6173  create data clas
+000040c0: 7365 732e 0a0a 4465 6c66 696e 6f20 616c  ses...Delfino al
+000040d0: 736f 206e 6565 6473 2074 6f20 6b6e 6f77  so needs to know
+000040e0: 2c20 7768 6963 6820 636c 6173 7320 746f  , which class to
+000040f0: 2075 7365 2066 6f72 2074 6865 2076 616c   use for the val
+00004100: 6964 6174 696f 6e2e 2054 6f20 646f 2074  idation. To do t
+00004110: 6861 742c 2073 7769 7463 6820 746f 2060  hat, switch to `
+00004120: 6465 6c66 696e 6f2e 6465 636f 7261 746f  delfino.decorato
+00004130: 7273 2e70 6173 735f 6170 705f 636f 6e74  rs.pass_app_cont
+00004140: 6578 7460 2069 6e73 7465 6164 206f 6620  ext` instead of 
+00004150: 5b60 636c 6963 6b2e 7061 7373 5f6f 626a  [`click.pass_obj
+00004160: 605d 2868 7474 7073 3a2f 2f63 6c69 636b  `](https://click
+00004170: 2e70 616c 6c65 7473 7072 6f6a 6563 7473  .palletsprojects
+00004180: 2e63 6f6d 2f61 7069 2f23 636c 6963 6b2e  .com/api/#click.
+00004190: 7061 7373 5f6f 626a 293a 0a0a 6060 6074  pass_obj):..```t
+000041a0: 6f6d 6c0a 2320 7079 7072 6f6a 6563 742e  oml.# pyproject.
+000041b0: 746f 6d6c 0a0a 5b74 6f6f 6c2e 6465 6c66  toml..[tool.delf
+000041c0: 696e 6f2e 706c 7567 696e 732e 6465 6c66  ino.plugins.delf
+000041d0: 696e 6f5f 6c6f 6769 6e5f 706c 7567 696e  ino_login_plugin
+000041e0: 5d0a 7573 6572 6e61 6d65 203d 2022 7573  ].username = "us
+000041f0: 6572 220a 6060 600a 0a60 6060 7079 7468  er".```..```pyth
+00004200: 6f6e 0a23 2063 6f6d 6d61 6e64 732f 5f5f  on.# commands/__
+00004210: 696e 6974 5f5f 2e70 790a 0a69 6d70 6f72  init__.py..impor
+00004220: 7420 636c 6963 6b0a 6672 6f6d 2064 656c  t click.from del
+00004230: 6669 6e6f 2e6d 6f64 656c 732e 7079 7072  fino.models.pypr
+00004240: 6f6a 6563 745f 746f 6d6c 2069 6d70 6f72  oject_toml impor
+00004250: 7420 506c 7567 696e 436f 6e66 6967 0a66  t PluginConfig.f
+00004260: 726f 6d20 6465 6c66 696e 6f2e 6d6f 6465  rom delfino.mode
+00004270: 6c73 2e61 7070 5f63 6f6e 7465 7874 2069  ls.app_context i
+00004280: 6d70 6f72 7420 4170 7043 6f6e 7465 7874  mport AppContext
+00004290: 0a66 726f 6d20 6465 6c66 696e 6f2e 6465  .from delfino.de
+000042a0: 636f 7261 746f 7273 2069 6d70 6f72 7420  corators import 
+000042b0: 7061 7373 5f61 7070 5f63 6f6e 7465 7874  pass_app_context
+000042c0: 0a0a 0a63 6c61 7373 204c 6f67 696e 506c  ...class LoginPl
+000042d0: 7567 696e 436f 6e66 6967 2850 6c75 6769  uginConfig(Plugi
+000042e0: 6e43 6f6e 6669 6729 3a0a 2020 2020 6c6f  nConfig):.    lo
+000042f0: 6769 6e3a 2073 7472 0a0a 0a40 636c 6963  gin: str...@clic
+00004300: 6b2e 636f 6d6d 616e 6428 290a 4070 6173  k.command().@pas
+00004310: 735f 6170 705f 636f 6e74 6578 7428 4c6f  s_app_context(Lo
+00004320: 6769 6e50 6c75 6769 6e43 6f6e 6669 6729  ginPluginConfig)
+00004330: 0a64 6566 206c 6f67 696e 2861 7070 5f63  .def login(app_c
+00004340: 6f6e 7465 7874 3a20 4170 7043 6f6e 7465  ontext: AppConte
+00004350: 7874 5b4c 6f67 696e 506c 7567 696e 436f  xt[LoginPluginCo
+00004360: 6e66 6967 5d29 3a0a 2020 2020 7072 696e  nfig]):.    prin
+00004370: 7428 6170 705f 636f 6e74 6578 742e 706c  t(app_context.pl
+00004380: 7567 696e 5f63 6f6e 6669 672e 6c6f 6769  ugin_config.logi
+00004390: 6e29 0a60 6060 0a0a 5468 6520 6041 7070  n).```..The `App
+000043a0: 436f 6e74 6578 7460 2063 6c61 7373 2069  Context` class i
+000043b0: 7320 6765 6e65 7269 632e 2044 6566 696e  s generic. Defin
+000043c0: 696e 6720 7468 6520 6050 6c75 6769 6e43  ing the `PluginC
+000043d0: 6f6e 6669 6754 7970 6560 2028 7375 6368  onfigType` (such
+000043e0: 2061 7320 6041 7070 436f 6e74 6578 745b   as `AppContext[
+000043f0: 4c6f 6769 6e50 6c75 6769 6e43 6f6e 6669  LoginPluginConfi
+00004400: 675d 6020 696e 2074 6865 2065 7861 6d70  g]` in the examp
+00004410: 6c65 2061 626f 7665 2920 656e 6162 6c65  le above) enable
+00004420: 7320 696e 7472 6f73 7065 6374 696f 6e20  s introspection 
+00004430: 616e 6420 7479 7065 2063 6865 636b 732e  and type checks.
+00004440: 0a0a 2323 2050 726f 6a65 6374 2073 7065  ..## Project spe
+00004450: 6369 6669 6320 6f76 6572 7269 6465 730a  cific overrides.
+00004460: 0a49 7420 6973 206c 696b 656c 7920 796f  .It is likely yo
+00004470: 7572 2070 726f 6a65 6374 7320 7769 6c6c  ur projects will
+00004480: 2072 6571 7569 7265 2073 6c69 6768 7420   require slight 
+00004490: 6469 7665 7267 656e 6365 2074 6f20 7468  divergence to th
+000044a0: 6520 6465 6661 756c 7473 2079 6f75 2065  e defaults you e
+000044b0: 6e63 6f64 6520 696e 2079 6f75 7220 7363  ncode in your sc
+000044c0: 7269 7074 732e 2054 6865 2066 6f6c 6c6f  ripts. The follo
+000044d0: 7769 6e67 2073 6563 7469 6f6e 7320 636f  wing sections co
+000044e0: 7665 7220 7468 6520 6d6f 7374 2063 6f6d  ver the most com
+000044f0: 6d6f 6e20 7573 6520 6361 7365 732e 0a0a  mon use cases...
+00004500: 2323 2320 5061 7373 2d74 6872 6f75 6768  ### Pass-through
+00004510: 2061 7267 756d 656e 7473 0a0a 596f 7520   arguments..You 
+00004520: 6361 6e20 7061 7373 2061 6464 6974 696f  can pass additio
+00004530: 6e61 6c20 6172 6775 6d65 6e74 7320 746f  nal arguments to
+00004540: 2064 6f77 6e73 7472 6561 6d20 746f 6f6c   downstream tool
+00004550: 7320 6279 2064 6563 6f72 6174 696e 6720  s by decorating 
+00004560: 636f 6d6d 616e 6473 2077 6974 6820 7468  commands with th
+00004570: 6520 5b60 6465 636f 7261 746f 7273 2e70  e [`decorators.p
+00004580: 6173 735f 6172 6773 605d 2868 7474 7073  ass_args`](https
+00004590: 3a2f 2f67 6974 6875 622e 636f 6d2f 7261  ://github.com/ra
+000045a0: 6465 6b6c 6174 2f64 656c 6669 6e6f 2f62  deklat/delfino/b
+000045b0: 6c6f 622f 6d61 696e 2f73 7263 2f64 656c  lob/main/src/del
+000045c0: 6669 6e6f 2f64 6563 6f72 6174 6f72 732f  fino/decorators/
+000045d0: 7061 7373 5f61 7267 732e 7079 2920 6465  pass_args.py) de
+000045e0: 636f 7261 746f 723a 0a0a 6060 6070 7974  corator:..```pyt
+000045f0: 686f 6e0a 2320 636f 6d6d 616e 6473 2f5f  hon.# commands/_
+00004600: 5f69 6e69 745f 5f2e 7079 0a0a 6672 6f6d  _init__.py..from
+00004610: 2074 7970 696e 6720 696d 706f 7274 2054   typing import T
+00004620: 7570 6c65 0a0a 696d 706f 7274 2063 6c69  uple..import cli
+00004630: 636b 0a66 726f 6d20 6465 6c66 696e 6f2e  ck.from delfino.
+00004640: 6465 636f 7261 746f 7273 2069 6d70 6f72  decorators impor
+00004650: 7420 7061 7373 5f61 7267 730a 6672 6f6d  t pass_args.from
+00004660: 2064 656c 6669 6e6f 2e65 7865 6375 7469   delfino.executi
+00004670: 6f6e 2069 6d70 6f72 7420 7275 6e2c 204f  on import run, O
+00004680: 6e45 7272 6f72 0a0a 4063 6c69 636b 2e63  nError..@click.c
+00004690: 6f6d 6d61 6e64 2829 0a40 7061 7373 5f61  ommand().@pass_a
+000046a0: 7267 730a 6465 6620 7465 7374 2870 6173  rgs.def test(pas
+000046b0: 7365 645f 6172 6773 3a20 5475 706c 655b  sed_args: Tuple[
+000046c0: 7374 722c 202e 2e2e 5d29 3a0a 2020 2020  str, ...]):.    
+000046d0: 7275 6e28 5b22 7079 7465 7374 222c 2022  run(["pytest", "
+000046e0: 7465 7374 7322 2c20 2a70 6173 7365 645f  tests", *passed_
+000046f0: 6172 6773 5d2c 206f 6e5f 6572 726f 723d  args], on_error=
+00004700: 4f6e 4572 726f 722e 4142 4f52 5429 0a60  OnError.ABORT).`
+00004710: 6060 0a0a 5468 656e 2061 6464 6974 696f  ``..Then additio
+00004720: 6e61 6c20 6172 6775 6d65 6e74 7320 6361  nal arguments ca
+00004730: 6e20 6265 2070 6173 7365 6420 6569 7468  n be passed eith
+00004740: 6572 2076 6961 2063 6f6d 6d61 6e64 206c  er via command l
+00004750: 696e 6520 6166 7465 7220 602d 2d60 3a0a  ine after `--`:.
+00004760: 0a60 6060 7368 656c 6c20 7363 7269 7074  .```shell script
+00004770: 0a64 656c 6669 6e6f 2074 6573 7420 2d2d  .delfino test --
+00004780: 202d 2d63 6170 7475 7265 3d6e 6f0a 6060   --capture=no.``
+00004790: 600a 0a4f 7220 7669 6120 636f 6e66 6967  `..Or via config
+000047a0: 7572 6174 696f 6e20 696e 2074 6865 2060  uration in the `
+000047b0: 7079 7072 6f6a 6563 742e 746f 6d6c 6020  pyproject.toml` 
+000047c0: 6669 6c65 3a0a 0a60 6060 746f 6d6c 0a5b  file:..```toml.[
+000047d0: 746f 6f6c 2e64 656c 6669 6e6f 2e70 6c75  tool.delfino.plu
+000047e0: 6769 6e73 2e3c 504c 5547 494e 3e2e 7465  gins.<PLUGIN>.te
+000047f0: 7374 5d0a 7061 7373 5f61 7267 7320 3d20  st].pass_args = 
+00004800: 5b27 2d2d 6361 7074 7572 653d 6e6f 275d  ['--capture=no']
+00004810: 0a60 6060 0a0a 4569 7468 6572 2077 6179  .```..Either way
+00004820: 2c20 626f 7468 2077 696c 6c20 7265 7375  , both will resu
+00004830: 6c74 2069 6e20 6578 6563 7574 696e 6720  lt in executing 
+00004840: 6070 7974 6573 7420 7465 7374 7320 2d2d  `pytest tests --
+00004850: 6361 7074 7572 653d 6e6f 602e 0a0a 2323  capture=no`...##
+00004860: 2320 4669 6c65 7320 6f76 6572 7269 6465  # Files override
+00004870: 0a0a 596f 7520 6361 6e20 6f76 6572 7269  ..You can overri
+00004880: 6465 2066 696c 6573 2070 6173 7365 6420  de files passed 
+00004890: 746f 2064 6f77 6e73 7472 6561 6d20 746f  to downstream to
+000048a0: 6f6c 7320 6279 2064 6563 6f72 6174 696e  ols by decoratin
+000048b0: 6720 636f 6d6d 616e 6473 2077 6974 6820  g commands with 
+000048c0: 7468 6520 5b60 6465 636f 7261 746f 7273  the [`decorators
+000048d0: 2e66 696c 6573 5f66 6f6c 6465 7273 5f6f  .files_folders_o
+000048e0: 7074 696f 6e60 5d28 6874 7470 733a 2f2f  ption`](https://
+000048f0: 6769 7468 7562 2e63 6f6d 2f72 6164 656b  github.com/radek
+00004900: 6c61 742f 6465 6c66 696e 6f2f 626c 6f62  lat/delfino/blob
+00004910: 2f6d 6169 6e2f 7372 632f 6465 6c66 696e  /main/src/delfin
+00004920: 6f2f 6465 636f 7261 746f 7273 2f66 696c  o/decorators/fil
+00004930: 6573 5f66 6f6c 6465 7273 2e70 7929 2064  es_folders.py) d
+00004940: 6563 6f72 6174 6f72 3a0a 0a60 6060 7079  ecorator:..```py
+00004950: 7468 6f6e 0a23 2063 6f6d 6d61 6e64 732f  thon.# commands/
+00004960: 5f5f 696e 6974 5f5f 2e70 790a 0a66 726f  __init__.py..fro
+00004970: 6d20 7479 7069 6e67 2069 6d70 6f72 7420  m typing import 
+00004980: 5475 706c 650a 0a69 6d70 6f72 7420 636c  Tuple..import cl
+00004990: 6963 6b0a 6672 6f6d 2064 656c 6669 6e6f  ick.from delfino
+000049a0: 2e64 6563 6f72 6174 6f72 7320 696d 706f  .decorators impo
+000049b0: 7274 2066 696c 6573 5f66 6f6c 6465 7273  rt files_folders
+000049c0: 5f6f 7074 696f 6e0a 6672 6f6d 2064 656c  _option.from del
+000049d0: 6669 6e6f 2e65 7865 6375 7469 6f6e 2069  fino.execution i
+000049e0: 6d70 6f72 7420 7275 6e2c 204f 6e45 7272  mport run, OnErr
+000049f0: 6f72 0a0a 4063 6c69 636b 2e63 6f6d 6d61  or..@click.comma
+00004a00: 6e64 2829 0a40 6669 6c65 735f 666f 6c64  nd().@files_fold
+00004a10: 6572 735f 6f70 7469 6f6e 0a64 6566 2074  ers_option.def t
+00004a20: 6573 7428 6669 6c65 735f 666f 6c64 6572  est(files_folder
+00004a30: 733a 2054 7570 6c65 5b73 7472 2c20 2e2e  s: Tuple[str, ..
+00004a40: 2e5d 293a 0a20 2020 2069 6620 6e6f 7420  .]):.    if not 
+00004a50: 6669 6c65 735f 666f 6c64 6572 733a 0a20  files_folders:. 
+00004a60: 2020 2020 2020 2066 696c 6573 5f66 6f6c         files_fol
+00004a70: 6465 7273 203d 2028 2274 6573 7473 2f75  ders = ("tests/u
+00004a80: 6e69 7422 2c20 2274 6573 7473 2f69 6e74  nit", "tests/int
+00004a90: 6567 7261 7469 6f6e 2229 0a20 2020 2072  egration").    r
+00004aa0: 756e 285b 2270 7974 6573 7422 2c20 2a66  un(["pytest", *f
+00004ab0: 696c 6573 5f66 6f6c 6465 7273 5d2c 206f  iles_folders], o
+00004ac0: 6e5f 6572 726f 723d 4f6e 4572 726f 722e  n_error=OnError.
+00004ad0: 4142 4f52 5429 0a60 6060 0a0a 5468 656e  ABORT).```..Then
+00004ae0: 2074 6865 2064 6566 6175 6c74 2060 2274   the default `"t
+00004af0: 6573 7473 2f75 6e69 7422 2c20 2274 6573  ests/unit", "tes
+00004b00: 7473 2f69 6e74 6567 7261 7469 6f6e 2260  ts/integration"`
+00004b10: 2066 6f6c 6465 7273 2063 616e 2062 6520   folders can be 
+00004b20: 6f76 6572 7269 6464 656e 2065 6974 6865  overridden eithe
+00004b30: 7220 7669 6120 636f 6d6d 616e 6420 6c69  r via command li
+00004b40: 6e65 206f 7074 696f 6e73 2060 2d66 602f  ne options `-f`/
+00004b50: 602d 2d66 696c 6560 2f60 2d2d 666f 6c64  `--file`/`--fold
+00004b60: 6572 603a 0a0a 6060 6073 6865 6c6c 2073  er`:..```shell s
+00004b70: 6372 6970 740a 6465 6c66 696e 6f20 7465  cript.delfino te
+00004b80: 7374 202d 6620 7465 7374 732f 6f74 6865  st -f tests/othe
+00004b90: 720a 6060 600a 0a4f 7220 7669 6120 636f  r.```..Or via co
+00004ba0: 6e66 6967 7572 6174 696f 6e20 696e 2074  nfiguration in t
+00004bb0: 6865 2060 7079 7072 6f6a 6563 742e 746f  he `pyproject.to
+00004bc0: 6d6c 6020 6669 6c65 3a0a 0a60 6060 746f  ml` file:..```to
+00004bd0: 6d6c 0a5b 746f 6f6c 2e64 656c 6669 6e6f  ml.[tool.delfino
+00004be0: 2e70 6c75 6769 6e73 2e3c 504c 5547 494e  .plugins.<PLUGIN
+00004bf0: 3e2e 7465 7374 5d0a 6669 6c65 735f 666f  >.test].files_fo
+00004c00: 6c64 6572 7320 3d20 5b27 7465 7374 732f  lders = ['tests/
+00004c10: 6f74 6865 7227 5d0a 6060 600a 0a45 6974  other'].```..Eit
+00004c20: 6865 7220 7761 792c 2062 6f74 6820 7769  her way, both wi
+00004c30: 6c6c 2072 6573 756c 7420 696e 2065 7865  ll result in exe
+00004c40: 6375 7469 6e67 2060 7079 7465 7374 2074  cuting `pytest t
+00004c50: 6573 7473 2f6f 7468 6572 602e 0a0a 2323  ests/other`...##
+00004c60: 2047 726f 7570 696e 6720 636f 6d6d 616e   Grouping comman
+00004c70: 6473 0a0a 4f66 7465 6e20 6974 2069 7320  ds..Often it is 
+00004c80: 7573 6566 756c 2074 6f20 7275 6e20 7365  useful to run se
+00004c90: 7665 7261 6c20 636f 6d6d 616e 6473 2061  veral commands a
+00004ca0: 7320 6120 6772 6f75 7020 7769 7468 2061  s a group with a
+00004cb0: 2064 6966 6665 7265 6e74 2063 6f6d 6d61   different comma
+00004cc0: 6e64 206e 616d 652e 2043 6c69 636b 2073  nd name. Click s
+00004cd0: 7570 706f 7274 7320 6361 6c6c 696e 6720  upports calling 
+00004ce0: 6f74 6865 7220 636f 6d6d 616e 6473 2077  other commands w
+00004cf0: 6974 6820 5b60 636c 6963 6b2e 436f 6e74  ith [`click.Cont
+00004d00: 6578 742e 666f 7277 6172 6460 5d28 6874  ext.forward`](ht
+00004d10: 7470 733a 2f2f 636c 6963 6b2e 7061 6c6c  tps://click.pall
+00004d20: 6574 7370 726f 6a65 6374 732e 636f 6d2f  etsprojects.com/
+00004d30: 6170 692f 2363 6c69 636b 2e43 6f6e 7465  api/#click.Conte
+00004d40: 7874 2e66 6f72 7761 7264 2920 6f72 205b  xt.forward) or [
+00004d50: 6063 6c69 636b 2e43 6f6e 7465 7874 2e69  `click.Context.i
+00004d60: 6e76 6f6b 6560 5d28 6874 7470 733a 2f2f  nvoke`](https://
+00004d70: 636c 6963 6b2e 7061 6c6c 6574 7370 726f  click.palletspro
+00004d80: 6a65 6374 732e 636f 6d2f 6170 692f 2363  jects.com/api/#c
+00004d90: 6c69 636b 2e43 6f6e 7465 7874 2e69 6e76  lick.Context.inv
+00004da0: 6f6b 6529 2e0a 0a3c 212d 2d20 544f 444f  oke)...<!-- TODO
+00004db0: 2852 6164 656b 293a 2041 6464 2064 6573  (Radek): Add des
+00004dc0: 6372 6970 7469 6f6e 206f 6620 6065 7865  cription of `exe
+00004dd0: 6375 7465 5f63 6f6d 6d61 6e64 735f 6772  cute_commands_gr
+00004de0: 6f75 7060 206f 6e63 6520 6d69 6772 6174  oup` once migrat
+00004df0: 6564 2066 726f 6d20 6064 656c 6669 6e6f  ed from `delfino
+00004e00: 2d63 6f72 6560 2e20 2d2d 3e0a 0a         -core`. -->..
```

