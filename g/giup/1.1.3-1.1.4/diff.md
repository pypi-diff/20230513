# Comparing `tmp/giup-1.1.3.tar.gz` & `tmp/giup-1.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "giup-1.1.3.tar", max compression
+gzip compressed data, was "giup-1.1.4.tar", max compression
```

## Comparing `giup-1.1.3.tar` & `giup-1.1.4.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.3/LICENSE
--rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.3/README.md
--rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.3/giup/__init__.py
--rwxr-xr-x   0        0        0     2610 2023-05-13 12:01:19.763092 giup-1.1.3/giup/cli.py
--rwxr-xr-x   0        0        0     5368 2023-05-13 12:00:22.923550 giup-1.1.3/giup/command.py
--rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.3/giup/git.py
--rwxr-xr-x   0        0        0     6599 2023-05-13 11:54:43.712272 giup-1.1.3/giup/project.py
--rwxr-xr-x   0        0        0     2078 2023-05-13 10:45:22.366835 giup-1.1.3/giup/util.py
--rwxr-xr-x   0        0        0     1473 2023-05-13 12:02:21.156302 giup-1.1.3/pyproject.toml
--rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.3/PKG-INFO
+-rwxr-xr-x   0        0        0    11558 2021-01-31 22:52:26.563141 giup-1.1.4/LICENSE
+-rwxr-xr-x   0        0        0     2655 2021-01-31 23:04:48.331614 giup-1.1.4/README.md
+-rwxr-xr-x   0        0        0        0 2023-05-13 00:41:43.507705 giup-1.1.4/giup/__init__.py
+-rwxr-xr-x   0        0        0     2805 2023-05-13 15:10:47.846943 giup-1.1.4/giup/cli.py
+-rwxr-xr-x   0        0        0     5368 2023-05-13 12:00:22.923550 giup-1.1.4/giup/command.py
+-rwxr-xr-x   0        0        0     1745 2023-05-13 01:02:56.311788 giup-1.1.4/giup/git.py
+-rwxr-xr-x   0        0        0     6633 2023-05-13 15:11:32.223538 giup-1.1.4/giup/project.py
+-rwxr-xr-x   0        0        0     2078 2023-05-13 10:45:22.366835 giup-1.1.4/giup/util.py
+-rwxr-xr-x   0        0        0     1473 2023-05-13 15:12:32.568229 giup-1.1.4/pyproject.toml
+-rw-r--r--   0        0        0     3782 1970-01-01 00:00:00.000000 giup-1.1.4/PKG-INFO
```

### Comparing `giup-1.1.3/LICENSE` & `giup-1.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `giup-1.1.3/README.md` & `giup-1.1.4/README.md`

 * *Files identical despite different names*

### Comparing `giup-1.1.3/giup/cli.py` & `giup-1.1.4/giup/cli.py`

 * *Files 11% similar despite different names*

```diff
@@ -62,27 +62,34 @@
         "-P", "--merge-path",
         type=str,
         action="append",
         default=[],
         help="Overwrite the config and follow these merge paths instead",
     )
     parser.add_argument(
+        "--no-commands",
+        action="store_true",
+        default=False,
+        help="Don't run any commands",
+    )
+    parser.add_argument(
         "-v", "--version",
         action="version",
         version=importlib.metadata.version("giup"),
     )
 
     args = parser.parse_args()
 
     try:
         project: Project = await Project.read(
             args.project,
-            fail_on_error=args.fail,
             override_commands=list(map(lambda cmd: Command.create_run(None, cmd), args.run_command)),
-            override_merge_paths=list(map(lambda path: path.split("->"), args.merge_path))
+            override_merge_paths=list(map(lambda path: path.split("->"), args.merge_path)),
+            disable_commands=args.no_commands,
+            fail_on_error=args.fail,
         )
 
         await project.run()
 
     except util.ParseError as error:
         cprint("Failed to parse project configuration file:\n" + str(error), color="red", file=sys.stderr)
```

### Comparing `giup-1.1.3/giup/command.py` & `giup-1.1.4/giup/command.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.3/giup/git.py` & `giup-1.1.4/giup/git.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.3/giup/project.py` & `giup-1.1.4/giup/project.py`

 * *Files 4% similar despite different names*

```diff
@@ -104,25 +104,26 @@
                 cprint("Invalid branch name \"" + result.branch_name + "\"", color="red", file=sys.stderr)
         return branches
 
     @staticmethod
     async def read(file_name: str = ".giup",
                    override_commands: Optional[List[str]] = None,
                    override_merge_paths: Optional[List[List[str]]] = None,
+                   disable_commands: bool = False,
                    fail_on_error: bool = False):
         project: Project = Project()
         project._fail_on_error = fail_on_error
 
         try:
             config_file = open(file_name)
             config_json = json.load(config_file)
         except OSError as e:
             msg = f"Couldn't load configuration file \"{file_name}\": {e}"
 
-            if override_commands and override_commands:
+            if override_commands and (override_commands or disable_commands):
                 # both mandatory fields are overriden, so we can proceed anyway
                 cprint(msg, color="yellow")
             else:
                 raise ProjectParseError(msg)
 
         if override_merge_paths:
             project._merge_paths = override_merge_paths
@@ -137,29 +138,28 @@
                 else:
                     raise ProjectParseError("Invalid json for merge paths specified:\n" +
                                             json.dumps(merge_paths_json, indent="\t"))
 
         if len(project._merge_paths) == 0:
             raise ProjectParseError("No valid merge paths found!")
 
-        if override_commands:
+        if disable_commands:
+            project._commands = []
+        elif override_commands:
             project._commands = override_commands
         else:
             if "commands" in config_json:
                 commands_json = config_json["commands"]
                 if type(commands_json) == list:
                     project._commands = []
                     for command_json in commands_json:
                         project._commands.append(Command.read(command_json))
                 else:
                     project._commands = [Command.read(commands_json)]
 
-        if len(project._commands) == 0:
-            raise ProjectParseError("No valid commands found!")
-
         return project
 
     @property
     def merge_paths(self):
         return self._merge_paths
 
     @property
```

### Comparing `giup-1.1.3/giup/util.py` & `giup-1.1.4/giup/util.py`

 * *Files identical despite different names*

### Comparing `giup-1.1.3/pyproject.toml` & `giup-1.1.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "GIUP"
-version = "1.1.3"
+version = "1.1.4"
 description = "Interactively and hierarchically perform git merges across branches and run commands in between."
 authors = ["Siphalor <info@siphalor.de>"]
 license = "Apache-2.0"
 readme = "README.md"
 repository = "https://github.com/Siphalor/giup"
 classifiers = [
     "License :: OSI Approved :: Apache Software License",
```

### Comparing `giup-1.1.3/PKG-INFO` & `giup-1.1.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: giup
-Version: 1.1.3
+Version: 1.1.4
 Summary: Interactively and hierarchically perform git merges across branches and run commands in between.
 Home-page: https://github.com/Siphalor/giup
 License: Apache-2.0
 Author: Siphalor
 Author-email: info@siphalor.de
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
```

