# Comparing `tmp/commandsgpt-1.2.1.tar.gz` & `tmp/commandsgpt-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "commandsgpt-1.2.1.tar", last modified: Sat May 13 04:45:34 2023, max compression
+gzip compressed data, was "commandsgpt-1.2.2.tar", last modified: Sat May 13 18:51:29 2023, max compression
```

## Comparing `commandsgpt-1.2.1.tar` & `commandsgpt-1.2.2.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    12048 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9699 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:34.349952 commandsgpt-1.2.1/commands_gpt/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/commands_gpt/commands_gpt/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/chat.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3646 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/commands_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     7493 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/graphs.py
--rw-r--r--   0 runner    (1001) docker     (123)      564 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     9826 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/instruction_recognition.py
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/regex.py
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/commands_gpt/commands_gpt/static.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    12048 2023-05-13 04:45:34.000000 commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 04:45:34.000000 commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:45:34.000000 commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 04:45:34.000000 commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       84 2023-05-13 04:45:19.000000 commandsgpt-1.2.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-13 04:45:34.353952 commandsgpt-1.2.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:29.596086 commandsgpt-1.2.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    12048 2023-05-13 18:51:29.596086 commandsgpt-1.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9699 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:29.592086 commandsgpt-1.2.2/commands_gpt/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:29.592086 commandsgpt-1.2.2/commands_gpt/commands_gpt/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/chat.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:29.592086 commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3646 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/commands_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7493 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/graphs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10187 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/instruction_recognition.py
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/regex.py
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/commands_gpt/commands_gpt/static.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:29.596086 commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    12048 2023-05-13 18:51:29.000000 commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 18:51:29.000000 commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 18:51:29.000000 commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 18:51:29.000000 commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-05-13 18:51:16.000000 commandsgpt-1.2.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-13 18:51:29.596086 commandsgpt-1.2.2/setup.cfg
```

### Comparing `commandsgpt-1.2.1/LICENSE` & `commandsgpt-1.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/PKG-INFO` & `commandsgpt-1.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 2.1
 Name: commandsgpt
-Version: 1.2.1
+Version: 1.2.2
 Summary: An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 Home-page: https://github.com/AlexisAndradeDev/CommandsGPT
 Author: Martín Alexis Martínez Andrade
 Author-email: alexis.martinez.contacto@gmail.com
 Project-URL: Bug Tracker, https://github.com/AlexisAndradeDev/CommandsGPT/issues
 Project-URL: repository, https://github.com/AlexisAndradeDev/CommandsGPT
-Classifier: License :: OSI Approved :: MIT License
+Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # CommandsGPT
```

### Comparing `commandsgpt-1.2.1/README.md` & `commandsgpt-1.2.2/README.md`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/commands_funcs.py` & `commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/commands_funcs.py`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/commands_gpt/commands_gpt/commands/graphs.py` & `commandsgpt-1.2.2/commands_gpt/commands_gpt/commands/graphs.py`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/commands_gpt/commands_gpt/config.py` & `commandsgpt-1.2.2/commands_gpt/commands_gpt/config.py`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/commands_gpt/commands_gpt/instruction_recognition.py` & `commandsgpt-1.2.2/commands_gpt/commands_gpt/instruction_recognition.py`

 * *Files 2% similar despite different names*

```diff
@@ -22,25 +22,27 @@
     """
     messages = [
         {
         'role': 'system', 
         'content':
             """You are a tool that, based on the user's prompt, detects the series of commands that must be executed, arguments that each command will have, and the relationship between each command (for example, what data generated by a command will be used as an argument for another)."""
             """\n*IMPORTANT*: *WRITE in the LANGUAGE that the USER writes his/her prompt in*."""
-            """\n*IMPORTANT*: You can ONLY use the given commands. NEVER try to use OTHERS."""
+            """\n*IMPORTANT*: You can ONLY use the given commands. **NEVER try to use OTHERS**."""
 
             f"""\n\nCommands:\n{commands}"""
 
             """\n\nDepending on the prompt, you will use different commands and different arguments and relationships between commands. The only way you can see data generated by other commands from a command is by passing them as arguments."""
 
             """\n\n*Your response will have this format, ALWAYS stick to it*:"""
             """\n[[command_id, "COMMAND_NAME", {"arg1": value1, "arg2": value2, ...}, [[next_command_id, "dependent_on_data", required_value], [...], ...]], [...]]"""
+            """\nYou will replace EVERYTHING in the format with the correct data."""
             """\nTo reference data generated by a command, use __&i.data__. 'i' is the ID of the command; 'data' is the name of the generated data, and works like a Python value (if it's a list, you can use __&i.data[i]__, __&i.data[i:j]__, etc.; in a dictionary, __&i.data["key"]__, etc.)."""
             """\nYou can ONLY reference data in the arguments of the nodes."""
-            """\nThe structure will ultimately be like a graph. The next_command_id defines which command will be executed next, dependent_on_data is the name of the data generated by the current command which will be used as a condition (null if it won't be used), and required_value is what value the dependent_on_data must have to execute the next command (or null if it doesn't matter)."""
+            """\nThe structure will ultimately be like a graph. The next_command_id defines which command will be executed next; dependent_on_data is the name of the data generated by the current command which will be used as a condition (null if the next command will be executed no matter what the results of the current command where), and required_value is what value the dependent_on_data must have to execute the next command (null if dependent_on_data was also null)."""
+            """\nNote that dependent_on_data is NOT a data reference for the next command; it's just what will be used as a CONDITION to determine if the next command will be executed."""
             """\nA command can execute multiple next commands."""
             """\nBe concise but *solid* with the structure."""
             """\n*Consider that the user might write incorrectly and their inputs might be ambiguous*."""
             """\nThe only way to reference the data of other commands is by using the __&i.data__ referencing. Commands DO NOT KNOW each other's data."""
             """\nProvide all the relevant context in the arguments of the commands, so that you're not ambiguous."""
             """\nBe creative and logic when using the commands' arguments and data references."""
```

### Comparing `commandsgpt-1.2.1/commands_gpt/commands_gpt/regex.py` & `commandsgpt-1.2.2/commands_gpt/commands_gpt/regex.py`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/PKG-INFO` & `commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 2.1
 Name: commandsgpt
-Version: 1.2.1
+Version: 1.2.2
 Summary: An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 Home-page: https://github.com/AlexisAndradeDev/CommandsGPT
 Author: Martín Alexis Martínez Andrade
 Author-email: alexis.martinez.contacto@gmail.com
 Project-URL: Bug Tracker, https://github.com/AlexisAndradeDev/CommandsGPT/issues
 Project-URL: repository, https://github.com/AlexisAndradeDev/CommandsGPT
-Classifier: License :: OSI Approved :: MIT License
+Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # CommandsGPT
```

### Comparing `commandsgpt-1.2.1/commands_gpt/commandsgpt.egg-info/SOURCES.txt` & `commandsgpt-1.2.2/commands_gpt/commandsgpt.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.2.1/setup.cfg` & `commandsgpt-1.2.2/setup.cfg`

 * *Files 13% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 [metadata]
 name = commandsgpt
-version = 1.2.1
+version = 1.2.2
 author = Martín Alexis Martínez Andrade
 author_email = alexis.martinez.contacto@gmail.com
 description = An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 long_description = file: README.md, LICENSE
 long_description_content_type = text/markdown
 url = https://github.com/AlexisAndradeDev/CommandsGPT
 project_urls = 
 	Bug Tracker = https://github.com/AlexisAndradeDev/CommandsGPT/issues
 	repository = https://github.com/AlexisAndradeDev/CommandsGPT
 classifiers = 
-	License :: OSI Approved :: MIT License
+	License :: OSI Approved :: BSD License
 	Operating System :: OS Independent
 	Programming Language :: Python :: 3
 
 [options]
 package_dir = 
 	= commands_gpt
 packages = find:
```

