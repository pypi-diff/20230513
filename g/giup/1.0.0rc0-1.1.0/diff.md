# Comparing `tmp/GIUP-1.0.0rc0.tar.gz` & `tmp/giup-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\GIUP-1.0.0rc0.tar", last modified: Tue Jan 26 16:11:47 2021, max compression
+gzip compressed data, was "giup-1.1.0.tar", max compression
```

## Comparing `GIUP-1.0.0rc0.tar` & `giup-1.1.0.tar`

### file list

```diff
@@ -1,22 +1,10 @@
-drwxrwxrwx   0        0        0        0 2021-01-26 16:11:47.902627 GIUP-1.0.0rc0/
-drwxrwxrwx   0        0        0        0 2021-01-26 16:11:47.881658 GIUP-1.0.0rc0/GIUP.egg-info/
--rw-rw-rw-   0        0        0     3510 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      319 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       28 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/requires.txt
--rw-rw-rw-   0        0        0        5 2021-01-26 16:11:47.000000 GIUP-1.0.0rc0/GIUP.egg-info/top_level.txt
--rw-rw-rw-   0        0        0    11539 2021-01-25 13:09:55.000000 GIUP-1.0.0rc0/LICENSE
--rw-rw-rw-   0        0        0       27 2021-01-26 13:40:27.000000 GIUP-1.0.0rc0/MANIFEST.in
--rw-rw-rw-   0        0        0     3510 2021-01-26 16:11:47.901623 GIUP-1.0.0rc0/PKG-INFO
--rw-rw-rw-   0        0        0     2046 2021-01-25 11:51:59.000000 GIUP-1.0.0rc0/README.md
-drwxrwxrwx   0        0        0        0 2021-01-26 16:11:47.899631 GIUP-1.0.0rc0/giup/
--rw-rw-rw-   0        0        0        0 2021-01-26 14:30:02.000000 GIUP-1.0.0rc0/giup/__init__.py
--rw-rw-rw-   0        0        0     1950 2021-01-26 15:06:34.000000 GIUP-1.0.0rc0/giup/__main__.py
--rw-rw-rw-   0        0        0       26 2021-01-26 14:39:35.000000 GIUP-1.0.0rc0/giup/__version__.py
--rw-rw-rw-   0        0        0     4474 2021-01-26 14:29:26.000000 GIUP-1.0.0rc0/giup/command.py
--rw-rw-rw-   0        0        0     1801 2021-01-26 14:29:26.000000 GIUP-1.0.0rc0/giup/git.py
--rw-rw-rw-   0        0        0     6064 2021-01-26 14:29:26.000000 GIUP-1.0.0rc0/giup/project.py
--rw-rw-rw-   0        0        0     1652 2021-01-26 14:29:26.000000 GIUP-1.0.0rc0/giup/util.py
--rw-rw-rw-   0        0        0       42 2021-01-26 16:11:47.903621 GIUP-1.0.0rc0/setup.cfg
--rw-rw-rw-   0        0        0     3962 2021-01-26 15:27:14.000000 GIUP-1.0.0rc0/setup.py
+-rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.0/LICENSE
+-rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.0/README.md
+-rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.0/giup/__init__.py
+-rwxr-xr-x   0        0        0     2500 2023-05-13 01:02:56.308225 giup-1.1.0/giup/cli.py
+-rwxr-xr-x   0        0        0     5014 2023-05-13 01:02:56.310171 giup-1.1.0/giup/command.py
+-rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.0/giup/git.py
+-rwxr-xr-x   0        0        0     6505 2023-05-13 01:02:56.403719 giup-1.1.0/giup/project.py
+-rwxr-xr-x   0        0        0     1875 2023-05-13 01:02:56.315382 giup-1.1.0/giup/util.py
+-rwxr-xr-x   0        0        0     1105 2023-05-13 01:02:56.489062 giup-1.1.0/pyproject.toml
+-rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.0/PKG-INFO
```

### Comparing `GIUP-1.0.0rc0/GIUP.egg-info/PKG-INFO` & `giup-1.1.0/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,79 +1,97 @@
-Metadata-Version: 2.1
-Name: GIUP
-Version: 1.0.0rc0
-Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
-Home-page: https://github.com/Siphalor/giup
-Author: Siphalor
-Author-email: info@siphalor.de
-License: Apache-2.0
-Project-URL: Source, https://github.com/Siphalor/giup
-Project-URL: Issues, https://github.com/Siphalor/giup/issues
-Description: 
-        # GIUP - Git Interactive Update and Publish
-        Allows to interactively perform hierarchical merges and run publishing commands in between.
-        
-        When commands fail the user is given the chance to intervene by rerunning the current command, just continuing, running a custom shell command or stopping the project, or the current merge path.
-        
-        ## Example Workflow
-        Example workflow from one of my Minecraft modding projects:
-        
-        `.giup:`
-        ```json
-        {
-            "merge-paths": [
-                "1.16",
-                "1.16->1.15->1.14",
-                "1.16->1.17"
-            ],
-            "commands": [
-                {
-                    "title": "Cleanup build directories",
-                    "run": "rm -rf build .gradle",
-                    "nt": "rmdir /S /Q build & rmdir /S /Q .gradle"
-                },
-                {
-                    "title": "Build and publish",
-                    "run": "./gradlew publish",
-                    "nt": "gradlew publish"
-                },
-                "git push"
-            ]
-        }
-        ```
-        
-        This will consecutively merge:
-        
-        1. `1.16` to `1.15`
-        2. `1.15` to `1.14`
-        3. `1.16` to `1.17`
-        
-        After each merge GIUP will cleanup, build, publish and push the code
-        
-        ## Specification
-        By default, the project specification will be read from the `.giup` file in the working directory. The specification should be defined in JSON and uses the following keys:
-        
-        ### `merge-paths`
-        Here you can specify certain merge hierarchies. You can either specify a hierarchy as a string delimited by arrows (`->`) or as an array with all branches (`["1.16","1.15","1.14"]`).
-        
-        Specifying a single branch will just switch to that branch and run the commands.
-        
-        ### `commands`
-        In this array commands are specified.
-        Commands are specified as an object or a string, which is a short form for an object with the `run` key.
-        
-        The `run` entry should contain a string that will be run as a shell command. You can define overrides for Windows (`nt`) and POSIX (`posix`) shells.
-        
-        The `title`entry is a string that optionally gets displayed when the command is run. If not defined, the command itself will be displayed before execution.
-        
-Platform: UNKNOWN
-Classifier: License :: OSI Approved :: Apache Software License
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: Implementation :: CPython
-Classifier: Programming Language :: Python :: Implementation :: PyPy
-Classifier: Topic :: Software Development :: Build Tools
-Classifier: Topic :: Software Development :: Version Control :: Git
-Requires-Python: >=3.6.0
-Description-Content-Type: text/markdown
+Metadata-Version: 2.1
+Name: giup
+Version: 1.1.0
+Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
+Home-page: https://github.com/Siphalor/giup
+License: Apache-2.0
+Author: Siphalor
+Author-email: info@siphalor.de
+Requires-Python: >=3.8,<4.0
+Classifier: License :: OSI Approved :: Apache Software License
+Classifier: Natural Language :: English
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.6
+Classifier: Programming Language :: Python :: Implementation :: CPython
+Classifier: Programming Language :: Python :: Implementation :: PyPy
+Classifier: Topic :: Software Development :: Build Tools
+Classifier: Topic :: Software Development :: Version Control :: Git
+Requires-Dist: termcolor (>=2.3.0,<3.0.0)
+Project-URL: Repository, https://github.com/Siphalor/giup
+Description-Content-Type: text/markdown
+
+# GIUP - Git Interactive Update and Publish
+
+[![PyPI][pypi-image]][pypi-link]
+
+  [pypi-image]: https://img.shields.io/pypi/v/giup.svg
+  [pypi-link]: https://pypi.python.org/pypi/giup
+
+Allows to interactively perform hierarchical merges and run publishing commands in between.
+
+When commands fail the user is given the chance to intervene by rerunning the current command, just continuing, running a custom shell command or stopping the project, or the current merge path.
+
+## Example Workflow
+Example workflow from one of my Minecraft modding projects:
+
+`.giup:`
+```json
+{
+    "merge-paths": [
+        "1.16",
+        "1.16->1.15->1.14",
+        "1.16->1.17"
+    ],
+    "commands": [
+        {
+            "title": "Cleanup build directories",
+            "run": "rm -rf build .gradle",
+            "nt": "rmdir /S /Q build & rmdir /S /Q .gradle",
+            "ignore-errors": true
+        },
+        {
+            "title": "Build and publish",
+            "run": "./gradlew publish",
+            "nt": "gradlew publish"
+        },
+        "git push"
+    ]
+}
+```
+
+This consecutively merges:
+
+1. `1.16` to `1.15`
+2. `1.15` to `1.14`
+3. `1.16` to `1.17`
+
+After each merge GIUP cleans up, builds, publishes and pushes the code.
+
+## Getting Started
+To install this project run `pip install giup`. 
+
+To use this for your project create a `.giup` file (as described below) in your project root and run `giup`.
+
+## Project Specification
+By default, the project specification will be read from the `.giup` file in the working directory. The specification should be defined in JSON and uses the following keys:
+
+### `merge-paths`
+Here you can specify certain merge hierarchies. You can either specify a hierarchy as a string delimited by arrows (`->`) or as an array with all branches (`["1.16","1.15","1.14"]`).
+
+Specifying a single branch will just switch to that branch and run the commands.
+
+### `commands`
+In this array commands are specified.
+Commands are specified as an object or a string, which is a short form for an object with the `run` key.
+
+The `run` entry should contain a string that will be run as a shell command. You can define overrides for Windows (`nt`) and POSIX (`posix`) shells.
+
+The `title`entry is a string that optionally gets displayed when the command is run. If not defined, the command itself will be displayed before execution.
+
+The `ignore-errors` entry is an optional boolean telling GIUP whether unsuccessful runs of the command should be treated as errors (on by default). This is useful e.g. when trying to delete a file with `rmdir` which might not exist.
+
```

### Comparing `GIUP-1.0.0rc0/LICENSE` & `giup-1.1.0/LICENSE`

 * *Files 1% similar despite different names*

```diff
@@ -182,15 +182,15 @@
       replaced with your own identifying information. (Don't include
       the brackets!)  The text should be enclosed in the appropriate
       comment syntax for the file format. We also recommend that a
       file or class name and description of purpose be included on the
       same "printed page" as the copyright notice for easier
       identification within third-party archives.
 
-   Copyright 2021 Siphalor
+   Copyright [yyyy] [name of copyright owner]
 
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
 
        http://www.apache.org/licenses/LICENSE-2.0
```

### Comparing `GIUP-1.0.0rc0/PKG-INFO` & `giup-1.1.0/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -1,79 +1,69 @@
-Metadata-Version: 2.1
-Name: GIUP
-Version: 1.0.0rc0
-Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
-Home-page: https://github.com/Siphalor/giup
-Author: Siphalor
-Author-email: info@siphalor.de
-License: Apache-2.0
-Project-URL: Source, https://github.com/Siphalor/giup
-Project-URL: Issues, https://github.com/Siphalor/giup/issues
-Description: 
-        # GIUP - Git Interactive Update and Publish
-        Allows to interactively perform hierarchical merges and run publishing commands in between.
-        
-        When commands fail the user is given the chance to intervene by rerunning the current command, just continuing, running a custom shell command or stopping the project, or the current merge path.
-        
-        ## Example Workflow
-        Example workflow from one of my Minecraft modding projects:
-        
-        `.giup:`
-        ```json
+# GIUP - Git Interactive Update and Publish
+
+[![PyPI][pypi-image]][pypi-link]
+
+  [pypi-image]: https://img.shields.io/pypi/v/giup.svg
+  [pypi-link]: https://pypi.python.org/pypi/giup
+
+Allows to interactively perform hierarchical merges and run publishing commands in between.
+
+When commands fail the user is given the chance to intervene by rerunning the current command, just continuing, running a custom shell command or stopping the project, or the current merge path.
+
+## Example Workflow
+Example workflow from one of my Minecraft modding projects:
+
+`.giup:`
+```json
+{
+    "merge-paths": [
+        "1.16",
+        "1.16->1.15->1.14",
+        "1.16->1.17"
+    ],
+    "commands": [
         {
-            "merge-paths": [
-                "1.16",
-                "1.16->1.15->1.14",
-                "1.16->1.17"
-            ],
-            "commands": [
-                {
-                    "title": "Cleanup build directories",
-                    "run": "rm -rf build .gradle",
-                    "nt": "rmdir /S /Q build & rmdir /S /Q .gradle"
-                },
-                {
-                    "title": "Build and publish",
-                    "run": "./gradlew publish",
-                    "nt": "gradlew publish"
-                },
-                "git push"
-            ]
-        }
-        ```
-        
-        This will consecutively merge:
-        
-        1. `1.16` to `1.15`
-        2. `1.15` to `1.14`
-        3. `1.16` to `1.17`
-        
-        After each merge GIUP will cleanup, build, publish and push the code
-        
-        ## Specification
-        By default, the project specification will be read from the `.giup` file in the working directory. The specification should be defined in JSON and uses the following keys:
-        
-        ### `merge-paths`
-        Here you can specify certain merge hierarchies. You can either specify a hierarchy as a string delimited by arrows (`->`) or as an array with all branches (`["1.16","1.15","1.14"]`).
-        
-        Specifying a single branch will just switch to that branch and run the commands.
-        
-        ### `commands`
-        In this array commands are specified.
-        Commands are specified as an object or a string, which is a short form for an object with the `run` key.
-        
-        The `run` entry should contain a string that will be run as a shell command. You can define overrides for Windows (`nt`) and POSIX (`posix`) shells.
-        
-        The `title`entry is a string that optionally gets displayed when the command is run. If not defined, the command itself will be displayed before execution.
-        
-Platform: UNKNOWN
-Classifier: License :: OSI Approved :: Apache Software License
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: Implementation :: CPython
-Classifier: Programming Language :: Python :: Implementation :: PyPy
-Classifier: Topic :: Software Development :: Build Tools
-Classifier: Topic :: Software Development :: Version Control :: Git
-Requires-Python: >=3.6.0
-Description-Content-Type: text/markdown
+            "title": "Cleanup build directories",
+            "run": "rm -rf build .gradle",
+            "nt": "rmdir /S /Q build & rmdir /S /Q .gradle",
+            "ignore-errors": true
+        },
+        {
+            "title": "Build and publish",
+            "run": "./gradlew publish",
+            "nt": "gradlew publish"
+        },
+        "git push"
+    ]
+}
+```
+
+This consecutively merges:
+
+1. `1.16` to `1.15`
+2. `1.15` to `1.14`
+3. `1.16` to `1.17`
+
+After each merge GIUP cleans up, builds, publishes and pushes the code.
+
+## Getting Started
+To install this project run `pip install giup`. 
+
+To use this for your project create a `.giup` file (as described below) in your project root and run `giup`.
+
+## Project Specification
+By default, the project specification will be read from the `.giup` file in the working directory. The specification should be defined in JSON and uses the following keys:
+
+### `merge-paths`
+Here you can specify certain merge hierarchies. You can either specify a hierarchy as a string delimited by arrows (`->`) or as an array with all branches (`["1.16","1.15","1.14"]`).
+
+Specifying a single branch will just switch to that branch and run the commands.
+
+### `commands`
+In this array commands are specified.
+Commands are specified as an object or a string, which is a short form for an object with the `run` key.
+
+The `run` entry should contain a string that will be run as a shell command. You can define overrides for Windows (`nt`) and POSIX (`posix`) shells.
+
+The `title`entry is a string that optionally gets displayed when the command is run. If not defined, the command itself will be displayed before execution.
+
+The `ignore-errors` entry is an optional boolean telling GIUP whether unsuccessful runs of the command should be treated as errors (on by default). This is useful e.g. when trying to delete a file with `rmdir` which might not exist.
```

### Comparing `GIUP-1.0.0rc0/giup/command.py` & `giup-1.1.0/giup/command.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,120 +1,136 @@
-# Copyright 2021 Siphalor
-#
-# Licensed under the Apache License, Version 2.0 (the "License");
-# you may not use this file except in compliance with the License.
-# You may obtain a copy of the License at
-#
-# http://www.apache.org/licenses/LICENSE-2.0
-#
-# Unless required by applicable law or agreed to in writing, software
-# distributed under the License is distributed on an "AS IS" BASIS,
-# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
-# See the License for the specific language governing permissions and
-# limitations under the License.
-#
-# -*- coding: utf-8 -*-
-import json
-import os
-import sys
-from types import coroutine
-from typing import Any, Tuple, Optional
-
-from termcolor import cprint
-
-from . import util
-
-
-class Command:
-    _CONTINUATION_TEXT = "a = abort path, c = continue, m = run command, q = quit, r = rerun"
-
-    _fun: coroutine
-    _args: Tuple[Any]
-    _kwargs: dict
-    _title: Optional[str]
-
-    def __init__(self, fun: coroutine, *args: Any, title: Optional[str] = None, **kwargs: Any):
-        self._fun = fun
-        self._args = args
-        self._kwargs = kwargs
-        self._title = title
-
-    async def execute(self):
-        await self._fun(*self._args, **self._kwargs)
-
-    async def run(self, fail_on_error: bool = False):
-        if self.title is not None:
-            cprint("> " + self.title, color="blue")
-
-        rerun = True
-        while rerun:
-            rerun = False
-            # noinspection PyBroadException
-            try:
-                return await self.execute()
-            except BaseException:
-                cprint("Failed to complete command!", color="red", attrs=["bold"], file=sys.stderr)
-                if fail_on_error:
-                    raise CommandFailError()
-                cprint("Specify action (" + Command._CONTINUATION_TEXT + ")", file=sys.stderr)
-                while True:
-                    print("?> ", end="", file=sys.stderr)
-                    inp = input()
-                    inp = inp[0]
-                    if inp == "a":
-                        raise util.GiupPathAbort()
-                    elif inp == "c":
-                        cprint("Skipping current command" if self.title is None else "Skipping " + self.title,
-                               attrs=["bold"], file=sys.stderr)
-                        return
-                    elif inp == "m":
-                        line = input("$ ")
-                        await util.async_run_command_result(line)
-                        cprint("Choose next action: " + Command._CONTINUATION_TEXT, file=sys.stderr)
-                        continue
-                    elif inp == "q":
-                        raise util.GiupStop()
-                    elif inp == "r":
-                        rerun = True
-                        cprint("Rerunning current command" if self.title is None else "Rerunning: " + self.title,
-                               attrs=["bold"], file=sys.stderr)
-                        break
-                    else:
-                        cprint("Unknown option! (Available actions: " + Command._CONTINUATION_TEXT + ")",
-                               file=sys.stderr)
-                        continue
-                continue
-
-    @property
-    def title(self) -> Optional[str]:
-        return self._title
-
-    @staticmethod
-    def read(src: Any):
-        if type(src) == str:
-            return Command(util.async_run_command_result, src, title="Running command \"" + src + "\"")
-        elif type(src) == dict:
-            if os.name in src:
-                cmd = src[os.name]
-            else:
-                if "run" not in src:
-                    raise CommandParseError("No run command found in command definition:\n" +
-                                            json.dumps(src, indent="\t"))
-                cmd = src["run"]
-
-            return Command(
-                util.async_run_command_result,
-                cmd,
-                stdout=bool(src.get("stdout", True)),
-                stderr=bool(src.get("stderr", True)),
-                title=(src["title"] if "title" in src else "Running command \"" + cmd + "\"")
-            )
-        else:
-            raise CommandParseError("Invalid command json:\n" + json.dumps(src, indent="\t"))
-
-
-class CommandParseError(util.ParseError):
-    pass
-
-
-class CommandFailError(BaseException):
-    pass
+# Copyright 2023 Siphalor
+#
+# Licensed under the Apache License, Version 2.0 (the "License");
+# you may not use this file except in compliance with the License.
+# You may obtain a copy of the License at
+#
+# http://www.apache.org/licenses/LICENSE-2.0
+#
+# Unless required by applicable law or agreed to in writing, software
+# distributed under the License is distributed on an "AS IS" BASIS,
+# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
+# See the License for the specific language governing permissions and
+# limitations under the License.
+#
+# -*- coding: utf-8 -*-
+import json
+import os
+import sys
+from types import coroutine
+from typing import Any, Tuple, Optional
+
+from termcolor import cprint
+
+from . import util
+
+
+class Command:
+    _CONTINUATION_TEXT = "a = abort path, c = continue, m = run command, q = quit, r = rerun"
+
+    _fun: coroutine
+    _args: Tuple[Any]
+    _kwargs: dict
+    _title: Optional[str]
+
+    def __init__(self, fun: coroutine, *args: Any, title: Optional[str] = None, **kwargs: Any):
+        self._fun = fun
+        self._args = args
+        self._kwargs = kwargs
+        self._title = title
+
+    async def execute(self):
+        await self._fun(*self._args, **self._kwargs)
+
+    async def run(self, fail_on_error: bool = False):
+        if self.title is not None:
+            cprint("> " + self.title, color="blue")
+
+        rerun = True
+        while rerun:
+            rerun = False
+            # noinspection PyBroadException
+            try:
+                return await self.execute()
+            except BaseException:
+                cprint("Failed to complete command!", color="red", attrs=["bold"], file=sys.stderr)
+                if fail_on_error:
+                    raise CommandFailError()
+                cprint("Specify action (" + Command._CONTINUATION_TEXT + ")", file=sys.stderr)
+                while True:
+                    print("?> ", end="", file=sys.stderr)
+                    inp = input()
+                    inp = inp[0]
+                    if inp == "a":
+                        raise util.GiupPathAbort()
+                    elif inp == "c":
+                        cprint("> Skipping current command" if self.title is None else f"> Skipping {self.title}",
+                               color="blue", file=sys.stderr)
+                        return
+                    elif inp == "m":
+                        line = input("$ ")
+                        await util.async_run_command_result(line)
+                        cprint("Choose next action: " + Command._CONTINUATION_TEXT, file=sys.stderr)
+                        continue
+                    elif inp.startswith("m "):
+                        _, cmd = inp.split(" ", maxsplit=1)
+                        await util.async_run_command_result(cmd)
+                        cprint("Choose next action: " + Command._CONTINUATION_TEXT, file=sys.stderr)
+                        continue
+                    elif inp == "q":
+                        raise util.GiupStop()
+                    elif inp == "r":
+                        rerun = True
+                        cprint("> Rerunning last command" if self.title is None else f"> Rerunning: {self.title}",
+                               attrs="blue", file=sys.stderr)
+                        break
+                    else:
+                        cprint("Unknown option! (Available actions: " + Command._CONTINUATION_TEXT + ")",
+                               file=sys.stderr)
+                        continue
+                continue
+
+    @property
+    def title(self) -> Optional[str]:
+        return self._title
+
+    @staticmethod
+    def read(src: Any):
+        if type(src) == str:
+            return Command.create_run(None, src)
+
+        elif type(src) == dict:
+            if os.name in src:
+                cmd = src[os.name]
+            else:
+                if "run" not in src:
+                    raise CommandParseError("No run command found in command definition:\n" +
+                                            json.dumps(src, indent="\t"))
+                cmd = src["run"]
+
+            return Command.create_run(
+                src.get("title", None), cmd,
+                ignore_errors=bool(src.get("ignore-errors", False)),
+                stdout=bool(src.get("stdout")),
+                stderr=bool(src.get("stderr"))
+            )
+        else:
+            raise CommandParseError("Invalid command json:\n" + json.dumps(src, indent="\t"))
+
+    @staticmethod
+    def create_run(title: Optional[str], cmd: str,
+                   ignore_errors: bool = False,
+                   stdout: bool = True, stderr: bool = True):
+        return Command(
+            util.async_run_command_result if ignore_errors else util.async_run_command_expect_success,
+            cmd,
+            stdout=stdout, stderr=stderr,
+            title=(title if title is not None else f"Running command \"{cmd}\"")
+        )
+
+
+class CommandParseError(util.ParseError):
+    pass
+
+
+class CommandFailError(BaseException):
+    pass
```

