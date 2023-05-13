# Comparing `tmp/giup-1.1.0.tar.gz` & `tmp/giup-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "giup-1.1.0.tar", max compression
+gzip compressed data, was "giup-1.1.1.tar", max compression
```

## Comparing `giup-1.1.0.tar` & `giup-1.1.1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.0/LICENSE
--rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.0/README.md
--rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.0/giup/__init__.py
--rwxr-xr-x   0        0        0     2500 2023-05-13 01:02:56.308225 giup-1.1.0/giup/cli.py
--rwxr-xr-x   0        0        0     5014 2023-05-13 01:02:56.310171 giup-1.1.0/giup/command.py
--rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.0/giup/git.py
--rwxr-xr-x   0        0        0     6505 2023-05-13 01:02:56.403719 giup-1.1.0/giup/project.py
--rwxr-xr-x   0        0        0     1875 2023-05-13 01:02:56.315382 giup-1.1.0/giup/util.py
--rwxr-xr-x   0        0        0     1105 2023-05-13 01:02:56.489062 giup-1.1.0/pyproject.toml
--rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.0/PKG-INFO
+-rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.1/LICENSE
+-rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.1/README.md
+-rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.1/giup/__init__.py
+-rwxr-xr-x   0        0        0     2500 2023-05-13 01:02:56.308225 giup-1.1.1/giup/cli.py
+-rwxr-xr-x   0        0        0     5440 2023-05-13 10:39:04.960359 giup-1.1.1/giup/command.py
+-rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.1/giup/git.py
+-rwxr-xr-x   0        0        0     6505 2023-05-13 01:02:56.403719 giup-1.1.1/giup/project.py
+-rwxr-xr-x   0        0        0     2078 2023-05-13 10:45:22.366835 giup-1.1.1/giup/util.py
+-rwxr-xr-x   0        0        0     1473 2023-05-13 11:15:51.023942 giup-1.1.1/pyproject.toml
+-rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.1/PKG-INFO
```

### Comparing `giup-1.1.0/LICENSE` & `giup-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `giup-1.1.0/README.md` & `giup-1.1.1/README.md`

 * *Files identical despite different names*

### Comparing `giup-1.1.0/giup/cli.py` & `giup-1.1.1/giup/cli.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.0/giup/command.py` & `giup-1.1.1/giup/command.py`

 * *Files 16% similar despite different names*

```diff
@@ -19,17 +19,19 @@
 from types import coroutine
 from typing import Any, Tuple, Optional
 
 from termcolor import cprint
 
 from . import util
 
+_CONTINUATION_TEXT = "a = abort path, c = continue, e = execute command, q = quit, r = rerun"
+_CONTINUATION_ACTIONS = ["abort", "continue", "execute", "quit", "rerun"]
+
 
 class Command:
-    _CONTINUATION_TEXT = "a = abort path, c = continue, m = run command, q = quit, r = rerun"
 
     _fun: coroutine
     _args: Tuple[Any]
     _kwargs: dict
     _title: Optional[str]
 
     def __init__(self, fun: coroutine, *args: Any, title: Optional[str] = None, **kwargs: Any):
@@ -51,46 +53,60 @@
             # noinspection PyBroadException
             try:
                 return await self.execute()
             except BaseException:
                 cprint("Failed to complete command!", color="red", attrs=["bold"], file=sys.stderr)
                 if fail_on_error:
                     raise CommandFailError()
-                cprint("Specify action (" + Command._CONTINUATION_TEXT + ")", file=sys.stderr)
+                cprint("Specify action (" + _CONTINUATION_TEXT + ")", file=sys.stderr)
                 while True:
                     print("?> ", end="", file=sys.stderr)
                     inp = input()
-                    inp = inp[0]
-                    if inp == "a":
+                    inp_parts = inp.split(None, 1)
+                    inp_action = inp_parts[0]
+                    inp_args = None if len(inp_parts) < 2 else inp_parts[1]
+
+                    actions = util.fuzzy_match(inp_action, _CONTINUATION_ACTIONS)
+                    if len(actions) == 0:
+                        cprint(f"Unknown action! (Available actions: {_CONTINUATION_TEXT})", file=sys.stderr)
+                        continue
+                    elif len(actions) > 1:
+                        cprint(f"Multiple actions match the input: {', '.join(actions)}", file=sys.stderr)
+                        continue
+
+                    action = actions[0]
+
+                    if action == "abort":
                         raise util.GiupPathAbort()
-                    elif inp == "c":
+
+                    elif action == "continue":
                         cprint("> Skipping current command" if self.title is None else f"> Skipping {self.title}",
                                color="blue", file=sys.stderr)
                         return
-                    elif inp == "m":
-                        line = input("$ ")
-                        await util.async_run_command_result(line)
-                        cprint("Choose next action: " + Command._CONTINUATION_TEXT, file=sys.stderr)
-                        continue
-                    elif inp.startswith("m "):
-                        _, cmd = inp.split(" ", maxsplit=1)
+
+                    elif action == "execute":
+                        if inp_args is not None:
+                            cmd = inp_args
+                        else:
+                            cmd = input("$ ")
+                        if cmd.isspace():
+                            continue
+
                         await util.async_run_command_result(cmd)
-                        cprint("Choose next action: " + Command._CONTINUATION_TEXT, file=sys.stderr)
+                        cprint(f"Choose next action: {_CONTINUATION_TEXT}", file=sys.stderr)
                         continue
-                    elif inp == "q":
+
+                    elif inp == "quit":
                         raise util.GiupStop()
-                    elif inp == "r":
+
+                    elif inp == "rerun":
                         rerun = True
                         cprint("> Rerunning last command" if self.title is None else f"> Rerunning: {self.title}",
                                attrs="blue", file=sys.stderr)
                         break
-                    else:
-                        cprint("Unknown option! (Available actions: " + Command._CONTINUATION_TEXT + ")",
-                               file=sys.stderr)
-                        continue
                 continue
 
     @property
     def title(self) -> Optional[str]:
         return self._title
 
     @staticmethod
@@ -106,16 +122,16 @@
                     raise CommandParseError("No run command found in command definition:\n" +
                                             json.dumps(src, indent="\t"))
                 cmd = src["run"]
 
             return Command.create_run(
                 src.get("title", None), cmd,
                 ignore_errors=bool(src.get("ignore-errors", False)),
-                stdout=bool(src.get("stdout")),
-                stderr=bool(src.get("stderr"))
+                stdout=bool(src.get("stdout", True)),
+                stderr=bool(src.get("stderr", True))
             )
         else:
             raise CommandParseError("Invalid command json:\n" + json.dumps(src, indent="\t"))
 
     @staticmethod
     def create_run(title: Optional[str], cmd: str,
                    ignore_errors: bool = False,
```

### Comparing `giup-1.1.0/giup/git.py` & `giup-1.1.1/giup/git.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.0/giup/project.py` & `giup-1.1.1/giup/project.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.0/giup/util.py` & `giup-1.1.1/giup/util.py`

 * *Files 12% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 #
 # -*- coding: utf-8 -*-
 import asyncio
-from typing import Tuple
+from typing import Tuple, List
 
 
 async def async_run_command_result(cmd: str, stdout: bool = True, stderr: bool = True) -> int:
     res = await asyncio.create_subprocess_shell(
         cmd,
         stdout=(None if stdout else asyncio.subprocess.DEVNULL),
         stderr=(None if stderr else asyncio.subprocess.DEVNULL)
@@ -37,14 +37,21 @@
         cmd,
         stdout=(asyncio.subprocess.PIPE if stdout else None),
         stderr=(asyncio.subprocess.PIPE if stderr else None)
     )
     return res.returncode, await res.communicate()
 
 
+def fuzzy_match(user_input: str, cases: List[str]) -> List[str]:
+    if user_input in cases:
+        return [user_input]
+
+    return list(filter(lambda case: case.startswith(user_input), cases))
+
+
 class ParseError(BaseException):
     _message: str
 
     def __init__(self, message: str):
         self._message = message
 
     def __str__(self):
```

### Comparing `giup-1.1.0/PKG-INFO` & `giup-1.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: giup
-Version: 1.1.0
+Version: 1.1.1
 Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
 Home-page: https://github.com/Siphalor/giup
 License: Apache-2.0
 Author: Siphalor
 Author-email: info@siphalor.de
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
```

