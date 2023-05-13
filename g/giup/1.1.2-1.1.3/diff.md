# Comparing `tmp/giup-1.1.2.tar.gz` & `tmp/giup-1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "giup-1.1.2.tar", max compression
+gzip compressed data, was "giup-1.1.3.tar", max compression
```

## Comparing `giup-1.1.2.tar` & `giup-1.1.3.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.2/LICENSE
--rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.2/README.md
--rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.2/giup/__init__.py
--rwxr-xr-x   0        0        0     2500 2023-05-13 01:02:56.308225 giup-1.1.2/giup/cli.py
--rwxr-xr-x   0        0        0     5421 2023-05-13 11:24:49.589816 giup-1.1.2/giup/command.py
--rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.2/giup/git.py
--rwxr-xr-x   0        0        0     6527 2023-05-13 11:22:48.153931 giup-1.1.2/giup/project.py
--rwxr-xr-x   0        0        0     2078 2023-05-13 10:45:22.366835 giup-1.1.2/giup/util.py
--rwxr-xr-x   0        0        0     1473 2023-05-13 11:29:09.702714 giup-1.1.2/pyproject.toml
--rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.2/PKG-INFO
+-rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.3/LICENSE
+-rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.3/README.md
+-rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.3/giup/__init__.py
+-rwxr-xr-x   0        0        0     2610 2023-05-13 12:01:19.763092 giup-1.1.3/giup/cli.py
+-rwxr-xr-x   0        0        0     5368 2023-05-13 12:00:22.923550 giup-1.1.3/giup/command.py
+-rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.3/giup/git.py
+-rwxr-xr-x   0        0        0     6599 2023-05-13 11:54:43.712272 giup-1.1.3/giup/project.py
+-rwxr-xr-x   0        0        0     2078 2023-05-13 10:45:22.366835 giup-1.1.3/giup/util.py
+-rwxr-xr-x   0        0        0     1473 2023-05-13 12:02:21.156302 giup-1.1.3/pyproject.toml
+-rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.3/PKG-INFO
```

### Comparing `giup-1.1.2/LICENSE` & `giup-1.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `giup-1.1.2/README.md` & `giup-1.1.3/README.md`

 * *Files identical despite different names*

### Comparing `giup-1.1.2/giup/cli.py` & `giup-1.1.3/giup/cli.py`

 * *Files 7% similar despite different names*

```diff
@@ -13,14 +13,17 @@
 # limitations under the License.
 #
 # -*- coding: utf-8 -*-
 import argparse
 import asyncio
 import importlib.metadata
 import sys
+# Importing the readline module enables input() history
+# noinspection PyUnresolvedReferences
+import readline
 
 from termcolor import cprint
 
 from giup import util
 from giup.project import Project
 from giup.command import Command
```

### Comparing `giup-1.1.2/giup/command.py` & `giup-1.1.3/giup/command.py`

 * *Files 5% similar despite different names*

```diff
@@ -55,16 +55,15 @@
                 return await self.execute()
             except BaseException:
                 cprint("Failed to complete command!", color="red", attrs=["bold"], file=sys.stderr)
                 if fail_on_error:
                     raise CommandFailError()
                 cprint("Specify action (" + _CONTINUATION_TEXT + ")", file=sys.stderr)
                 while True:
-                    print("?> ", end="", file=sys.stderr)
-                    inp = input()
+                    inp = input("?> ")
                     inp_parts = inp.split(None, 1)
                     inp_action = inp_parts[0]
                     inp_args = None if len(inp_parts) < 2 else inp_parts[1]
 
                     actions = util.fuzzy_match(inp_action, _CONTINUATION_ACTIONS)
                     if len(actions) == 0:
                         cprint(f"Unknown action! (Available actions: {_CONTINUATION_TEXT})", file=sys.stderr)
@@ -97,15 +96,15 @@
 
                     elif action == "quit":
                         raise util.GiupStop()
 
                     elif action == "rerun":
                         rerun = True
                         cprint("> Rerunning last command" if self.title is None else f"> Rerunning: {self.title}",
-                               attrs="blue", file=sys.stderr)
+                               color="blue", file=sys.stderr)
                         break
 
     @property
     def title(self) -> Optional[str]:
         return self._title
 
     @staticmethod
```

### Comparing `giup-1.1.2/giup/git.py` & `giup-1.1.3/giup/git.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.2/giup/project.py` & `giup-1.1.3/giup/project.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,14 +12,15 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 #
 # -*- coding: utf-8 -*-
 import asyncio
 import json
 import sys
+import traceback
 from typing import List, Any, Optional
 
 from termcolor import cprint
 
 from . import git
 from . import util
 from .command import Command
@@ -39,14 +40,15 @@
 
     async def run(self):
         original_branch = await git.get_current_branch()
         i = 0
         for merge_path in self.merge_paths:
             cprint(f"> Following merge path #{i}: {' -> '.join(merge_path)}", color="blue")
             i += 1
+            # noinspection PyBroadException
             try:
                 if not merge_path:
                     cprint("> Merge path is empty, skipping", color="yellow", file=sys.stderr)
                     continue
 
                 elif len(merge_path) == 1:  # singleton path
                     await Command(git.switch, merge_path[0], title="Switching to branch \"" + merge_path[0] + "\"")\
@@ -65,16 +67,16 @@
                         await self.run_commands()
 
             except util.GiupPathAbort:
                 cprint("Aborting current path!", attrs=["bold"], file=sys.stderr)
             except util.GiupStop:
                 cprint("Quitting giup (cancelling all further paths)", attrs=["bold"], file=sys.stderr)
                 break
-            except BaseException as e:
-                cprint("Failed to follow merge path!\n" + str(e), color="red", file=sys.stderr)
+            except BaseException:
+                cprint(f"Failed to follow merge path!\n{traceback.format_exc()}", color="red", file=sys.stderr)
                 if self.fail_on_error:
                     return
 
         cprint("> Returning to original branch \"" + original_branch + "\"", color="blue")
         await git.switch(original_branch)
 
     @staticmethod
```

### Comparing `giup-1.1.2/giup/util.py` & `giup-1.1.3/giup/util.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.2/pyproject.toml` & `giup-1.1.3/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "GIUP"
-version = "1.1.2"
+version = "1.1.3"
 description = "Interactively and hierarchically perform git merges across branches and run commands in between."
 authors = ["Siphalor <info@siphalor.de>"]
 license = "Apache-2.0"
 readme = "README.md"
 repository = "https://github.com/Siphalor/giup"
 classifiers = [
     "License :: OSI Approved :: Apache Software License",
```

### Comparing `giup-1.1.2/PKG-INFO` & `giup-1.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: giup
-Version: 1.1.2
+Version: 1.1.3
 Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
 Home-page: https://github.com/Siphalor/giup
 License: Apache-2.0
 Author: Siphalor
 Author-email: info@siphalor.de
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
```

