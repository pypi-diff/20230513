# Comparing `tmp/commandsgpt-1.1.3.tar.gz` & `tmp/commandsgpt-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "commandsgpt-1.1.3.tar", last modified: Sat May  6 15:21:18 2023, max compression
+gzip compressed data, was "commandsgpt-1.2.0.tar", last modified: Sat May 13 04:31:56 2023, max compression
```

## Comparing `commandsgpt-1.1.3.tar` & `commandsgpt-1.2.0.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:18.635806 commandsgpt-1.1.3/
--rw-r--r--   0 runner    (1001) docker     (123)     1093 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    11342 2023-05-06 15:21:18.635806 commandsgpt-1.1.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9412 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:18.627806 commandsgpt-1.1.3/commands_gpt/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:18.631806 commandsgpt-1.1.3/commands_gpt/commands_gpt/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/chat.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:18.635806 commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3580 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/commands_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     6461 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/graphs.py
--rw-r--r--   0 runner    (1001) docker     (123)      405 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5148 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/instruction_recognition.py
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/regex.py
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/commands_gpt/commands_gpt/static.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 15:21:18.635806 commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    11342 2023-05-06 15:21:18.000000 commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-06 15:21:18.000000 commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-06 15:21:18.000000 commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-06 15:21:18.000000 commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       84 2023-05-06 15:21:07.000000 commandsgpt-1.1.3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-06 15:21:18.635806 commandsgpt-1.1.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:56.229193 commandsgpt-1.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1093 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    11629 2023-05-13 04:31:56.233193 commandsgpt-1.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9699 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:56.229193 commandsgpt-1.2.0/commands_gpt/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:56.229193 commandsgpt-1.2.0/commands_gpt/commands_gpt/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/chat.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:56.229193 commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3646 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/commands_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7493 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/graphs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9826 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/instruction_recognition.py
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/regex.py
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/commands_gpt/commands_gpt/static.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:31:56.229193 commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    11629 2023-05-13 04:31:56.000000 commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 04:31:56.000000 commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:31:56.000000 commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 04:31:56.000000 commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-05-13 04:31:45.000000 commandsgpt-1.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-13 04:31:56.233193 commandsgpt-1.2.0/setup.cfg
```

### Comparing `commandsgpt-1.1.3/LICENSE` & `commandsgpt-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.1.3/PKG-INFO` & `commandsgpt-1.2.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: commandsgpt
-Version: 1.1.3
+Version: 1.2.0
 Summary: An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 Home-page: https://github.com/AlexisAndradeDev/CommandsGPT
 Author: Martín Alexis Martínez Andrade
 Author-email: alexis.martinez.contacto@gmail.com
 Project-URL: Bug Tracker, https://github.com/AlexisAndradeDev/CommandsGPT/issues
 Project-URL: repository, https://github.com/AlexisAndradeDev/CommandsGPT
 Classifier: License :: OSI Approved :: MIT License
@@ -29,20 +29,32 @@
 ```
 
 If you're using a virtual environment:
 ```
 pipenv install commandsgpt
 ```
 
+You also have to install the OpenAI package:
+
+```
+pip install openai
+```
+
+or
+
+```
+pipenv install openai
+```
+
 # Basic usage
 
 Create a `commands` dictionary that will store the commands described in natural language. Create the functions that will be called when the commands are executed (they must match the arguments and return values of the `commands` dict; the first parameter of these functions must be a Config object). Create a `command_name_to_func` dictionary that will take the name of a command and return the corresponding function.
 
 *Example of commands dictionary*
-```
+```python
 commands = {
     "REQUEST_USER_INPUT": {
         "description": "Asks the user to input data through the interface.",
         "arguments": {
             "message": {"description": "Message displayed to the user related to the data that will be requested (example: 'Enter your age').", "type": "string"},
         },
         "generates_data": {
@@ -50,68 +62,70 @@
         },
     },
     ...
 }
 ```
 
 *Example of a command function*
-```
+```python
 def request_user_input_command(config: Config, graph: Graph, message: str) -> dict[str, Any]:
     input_ = input(f"{message}\n*: ")
     results = {
         "input": input_,
     }
     return results
 ```
 
 *Example of command_name_to_func dictionary*
-```
+```python
 command_name_to_func = {
     "REQUEST_USER_INPUT": request_user_input_command,
     ...
 }
 ```
 
 Add the ***essential commands*** to your commands dictionaries.
 * These are the default commands that implement core logic to the model's thinking, like an IF command.
 * If you already defined your own core logic commands (IF command, THINK command, etc.), then you are free not to use them.
 
-```
+```python
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 ```
 
-Your `config` object: 
-```
-config = Config("gpt-4-0314", verbosity=1) # verbosity is optional
+Your `config` object:
+```python
+# keyword arguments are optional
+config = Config("gpt-4-0314", verbosity=1, explain_graph=True)
 ```
 
 Create an instruction:
 
-```
+```python
 instruction = input("Enter your instruction: ")
 ```
 
 Pass your instruction to the recognizer model:
 
-```
+```python
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 ```
 
 Finally, execute the graph of commands:
 
-```
+```python
 graph.execute_commands(config)
 ```
 
 # Basic example
 
-```
+```python
 from typing import Any
 from pathlib import Path
 from commands_gpt.instruction_recognition import recognize_instruction_and_create_graph
 from commands_gpt.commands.graphs import execute_commands
 from commands_gpt.config import Config
 
 # Commands Natural Language Dict
@@ -175,19 +189,20 @@
 }
 
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 
 chat_model = "gpt-4-0314"
 
-config = Config(chat_model, verbosity=1)
+config = Config(chat_model, verbosity=1, explain_graph=True)
 
 instruction = input("Enter your prompt: ")
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 graph.execute_commands(config)
 ```
 
 # Adding custom commands
 
 You can add and modify your own custom commands by creating two dictionaries:
@@ -211,15 +226,15 @@
         * The nested dictionaries have keys *description* and *type*.
 
         * **description**: Description of the data field in natural language.
 
         * **type**: Data type. E.g.: "string", "boolean", "int".
 
 ***Example***
-```
+```python
 commands = {
     "WRITE_TO_USER": {
         "description": "Writes something to the interface to communicate with the user.",
         "arguments": {
             "content": {"description": "Content to write.", "type": "string"},
         },
         "generates_data": {},
@@ -253,15 +268,15 @@
     * The arguments must match the arguments from the commands dictionary.
 
     * The return value must be a dictionary which keys must match the "generates_data" key.
 
     * The data types must match the ones declared in the commands dictionary.
 
 ***Example***
-```
+```python
 def write_to_user_command(config: Config, graph: Graph, content: str) -> dict[str, Any]:
     # add newlines because regex data injection replaces newline characters
     # by \\n substrings.
     content_with_newlines = "\n".join(content.split("\\n"))
     print(f">>> {content_with_newlines}")
     return {}
```

### Comparing `commandsgpt-1.1.3/README.md` & `commandsgpt-1.2.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -13,20 +13,32 @@
 ```
 
 If you're using a virtual environment:
 ```
 pipenv install commandsgpt
 ```
 
+You also have to install the OpenAI package:
+
+```
+pip install openai
+```
+
+or
+
+```
+pipenv install openai
+```
+
 # Basic usage
 
 Create a `commands` dictionary that will store the commands described in natural language. Create the functions that will be called when the commands are executed (they must match the arguments and return values of the `commands` dict; the first parameter of these functions must be a Config object). Create a `command_name_to_func` dictionary that will take the name of a command and return the corresponding function.
 
 *Example of commands dictionary*
-```
+```python
 commands = {
     "REQUEST_USER_INPUT": {
         "description": "Asks the user to input data through the interface.",
         "arguments": {
             "message": {"description": "Message displayed to the user related to the data that will be requested (example: 'Enter your age').", "type": "string"},
         },
         "generates_data": {
@@ -34,68 +46,70 @@
         },
     },
     ...
 }
 ```
 
 *Example of a command function*
-```
+```python
 def request_user_input_command(config: Config, graph: Graph, message: str) -> dict[str, Any]:
     input_ = input(f"{message}\n*: ")
     results = {
         "input": input_,
     }
     return results
 ```
 
 *Example of command_name_to_func dictionary*
-```
+```python
 command_name_to_func = {
     "REQUEST_USER_INPUT": request_user_input_command,
     ...
 }
 ```
 
 Add the ***essential commands*** to your commands dictionaries.
 * These are the default commands that implement core logic to the model's thinking, like an IF command.
 * If you already defined your own core logic commands (IF command, THINK command, etc.), then you are free not to use them.
 
-```
+```python
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 ```
 
-Your `config` object: 
-```
-config = Config("gpt-4-0314", verbosity=1) # verbosity is optional
+Your `config` object:
+```python
+# keyword arguments are optional
+config = Config("gpt-4-0314", verbosity=1, explain_graph=True)
 ```
 
 Create an instruction:
 
-```
+```python
 instruction = input("Enter your instruction: ")
 ```
 
 Pass your instruction to the recognizer model:
 
-```
+```python
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 ```
 
 Finally, execute the graph of commands:
 
-```
+```python
 graph.execute_commands(config)
 ```
 
 # Basic example
 
-```
+```python
 from typing import Any
 from pathlib import Path
 from commands_gpt.instruction_recognition import recognize_instruction_and_create_graph
 from commands_gpt.commands.graphs import execute_commands
 from commands_gpt.config import Config
 
 # Commands Natural Language Dict
@@ -159,19 +173,20 @@
 }
 
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 
 chat_model = "gpt-4-0314"
 
-config = Config(chat_model, verbosity=1)
+config = Config(chat_model, verbosity=1, explain_graph=True)
 
 instruction = input("Enter your prompt: ")
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 graph.execute_commands(config)
 ```
 
 # Adding custom commands
 
 You can add and modify your own custom commands by creating two dictionaries:
@@ -195,15 +210,15 @@
         * The nested dictionaries have keys *description* and *type*.
 
         * **description**: Description of the data field in natural language.
 
         * **type**: Data type. E.g.: "string", "boolean", "int".
 
 ***Example***
-```
+```python
 commands = {
     "WRITE_TO_USER": {
         "description": "Writes something to the interface to communicate with the user.",
         "arguments": {
             "content": {"description": "Content to write.", "type": "string"},
         },
         "generates_data": {},
@@ -237,15 +252,15 @@
     * The arguments must match the arguments from the commands dictionary.
 
     * The return value must be a dictionary which keys must match the "generates_data" key.
 
     * The data types must match the ones declared in the commands dictionary.
 
 ***Example***
-```
+```python
 def write_to_user_command(config: Config, graph: Graph, content: str) -> dict[str, Any]:
     # add newlines because regex data injection replaces newline characters
     # by \\n substrings.
     content_with_newlines = "\n".join(content.split("\\n"))
     print(f">>> {content_with_newlines}")
     return {}
```

### Comparing `commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/commands_funcs.py` & `commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/commands_funcs.py`

 * *Files 2% similar despite different names*

```diff
@@ -18,15 +18,16 @@
         "description": "Returns the Boolean value of a condition.",
         "arguments": {
             "condition": {"description": "Condition. Can be in natural language.", "type": "string"},
         },
         "generates_data": {
             "result": {"description": "Result of the condition: 0 or 1.", "type": "boolean"},
         },
-    }
+    },
+    # TODO: Create a FOR command to increment a counter variable
 }
 
 # Commands functions
 # Must be named 'LowercaseCommandName_command'
 # The first argument must be the Config object, followed by the Graph object
 # The arguments must match the arguments from the ESSENTIAL_COMMANDS dictionary
 # The return value must be a dictionary which keys must match the "generates_data" keys
```

### Comparing `commandsgpt-1.1.3/commands_gpt/commands_gpt/commands/graphs.py` & `commandsgpt-1.2.0/commands_gpt/commands_gpt/commands/graphs.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,56 +1,76 @@
 import functools
 import json
 from typing import Any, Callable
 
 from .. import regex
+from .. import instruction_recognition
 from ..static import StaticVar
 from ..config import Config
 
-# status codes
-NOT_REACHED = 0
-NOT_EXECUTED = 1
-EXECUTED = 2
+# next commands field indexes
+NEXT_COMMAND_ID = 0
+DEPENDENT_ON_DATA = 1
+REQUIRED_VALUE = 2
 
 @functools.total_ordering
 class CommandNode:
-    def __init__(self, data: list, commands: dict[str, dict], command_name_to_func: dict[str, Callable]):
+    def __init__(self, data: list, commands: dict[str, dict], 
+            command_name_to_func: dict[str, Callable]):
         self.id = data[0]
-        self.previous_command_id = data[1][0] if data[1] else None
-        self.dependent_on_data = data[1][1] if data[1] else None
-        self.required_value = data[1][2] if data[1] else None
-        self.command_name = data[2]
+        self.command_name = data[1]
 
         assert self.command_name in commands, f"Command '{self.command_name}' does not exist."
         assert self.command_name in command_name_to_func, f"Command '{self.command_name}' does not have a function declaration."
 
         self.command = command_name_to_func[self.command_name]
-        self.arguments = data[3] if len(data) > 3 else None
+        self.arguments = data[2]
+
+        self.next_commands: list[list[int | str | Any]] = data[3]
+        assert all(
+            map(
+                lambda next_command:
+                    (type(next_command[0]) is int and 
+                     type(next_command[1]) in [str, type(None)]),
+                self.next_commands,
+            )
+        ), f"Next commands field must match data types: list[list[int, str, Any]].\n{self.next_commands}"
 
-        self.status = NOT_REACHED
         self.data_generated = None
 
     def __eq__(self, other):
         return self.id == other.id
 
     def __lt__(self, other):
         return self.id < other.id
 
     def __str__(self):
-        return f"CommandNode(id={self.id}, previous_command_id={self.previous_command_id}, dependent_on_data={self.dependent_on_data}, required_value={self.required_value}, command={self.command})"
+        return f"CommandNode(id={self.id}, command={self.command})"
 
     def execute_command(self, config: Config, graph, arguments: dict[str, Any]):
         print(f"\n\nRunning '{self.command_name}' command with id {self.id}...")
         if config.verbosity >= 2:
             print(f"Using arguments: {arguments}")
         self.data_generated = self.command(config, graph, **arguments)
+    
+    def get_next_commands_to_execute(self) -> list[int]:
+        next_commands_to_execute = []
+        for next_command in self.next_commands:
+            next_command_id = next_command[NEXT_COMMAND_ID]
+            dependent_on_data = next_command[DEPENDENT_ON_DATA]
+            required_value = next_command[REQUIRED_VALUE]
+
+            if dependent_on_data is None: # doesn't matter the result of current node
+                next_commands_to_execute.append(next_command_id)
+            else: # next command execution depends on the result of current node
+                if self.data_generated[dependent_on_data] == required_value:
+                    next_commands_to_execute.append(next_command_id)
+        return next_commands_to_execute
 
 class Graph:
-    # TODO: Do not call twice set_start_data when initializing a graph (__init__ -> initialize -> build_graph)
-
     def __init__(self, raw_commands_data: StaticVar, commands: dict[str, dict], 
             command_name_to_func: dict[str, Callable]):
         self.set_start_data(raw_commands_data, commands, command_name_to_func)
         self.initialize()
 
     def set_start_data(self, raw_commands_data: StaticVar, commands: dict[str, dict], 
             command_name_to_func: dict[str, Callable]):
@@ -66,15 +86,14 @@
 
     def build_nodes(self):
         for command_data in self.commands_data:
             node = CommandNode(command_data, self.commands, self.command_name_to_func)
             if node.id in self.reached_nodes_ids:
                 # recover results of the node
                 reached_node = self.nodes[node.id]
-                node.status = reached_node.status
                 node.data_generated = reached_node.data_generated
             self.nodes[node.id] = node
 
     def initialize(self):
         self.reached_nodes_ids: list[int] = []
         self.nodes: dict[str, CommandNode] = {}
         self.build_graph(self.raw_commands_data, self.commands, self.command_name_to_func)
@@ -83,60 +102,65 @@
         # inject data generated by the node to the data string
         new_raw_commands_data = StaticVar(regex.inject_node_data(
             self.raw_commands_data.val, node_id, data_generated_by_node,
         ))
 
         # rebuild graph
         self.build_graph(new_raw_commands_data, self.commands, self.command_name_to_func)
-    
-    def execute_node(self, node_id: int, config: Config):
+        
+    def execute_node(self, node_id: int, config: Config) -> list[int]:
         node = self.nodes[node_id]
-
-        if node.status == EXECUTED:
-            return
-
-        if node.previous_command_id is not None:
-            previous_node = self.nodes[node.previous_command_id]
-            if previous_node.status == NOT_EXECUTED:
-                # the previous node was not executed, so this node will not
-                # activate
-                return
-
-            if previous_node.status == NOT_REACHED:
-                self.execute_node(previous_node.id, config)
-
-            if node.dependent_on_data:
-                if previous_node.data_generated[node.dependent_on_data] != node.required_value:
-                    node.status = NOT_EXECUTED
-                    return
-
+    
         node.execute_command(config, self, node.arguments)
         self.reached_nodes_ids.append(node.id)
-        node.status = EXECUTED
 
         if node.id in self.data_references:
             self.inject_node_data(node.id, node.data_generated)
+        
+        next_commands_to_execute = node.get_next_commands_to_execute()
+        return next_commands_to_execute
 
-    def print_graph(self):
+    def print_graph(self, explain_graph: bool):
         print("\n\n--- Commands graph ---")
+
+        print("\n~~ Graph ~~")
         for node in self.nodes.values():
             print(f"\n{node.id}. {node.command_name}")
-            if node.previous_command_id:
-                print(f"\n\tExecuted after node «{node.previous_command_id}».")
-            if node.dependent_on_data:
-                print(f"\n\t\tResult field '{node.dependent_on_data}' of node «{node.previous_command_id}» must have value «{node.required_value}» in order to execute this node.")
+            
+            if node.next_commands:
+                print(f"\tCommands executed by this node:")
+                for next_command_id, dependent_on_data, required_value in node.next_commands:
+                    next_node = self.nodes[next_command_id]
+                    print(f"\t{next_node.id}. {next_node.command_name}")
+                    if dependent_on_data is not None:
+                        print(f"\t\tIf '{dependent_on_data}' generated data has value: {required_value}.")
+
+        if explain_graph:
+            print("\n~~ Explanation ~~")
+            explanation = instruction_recognition.explain_graph_in_natural_language(self.raw_commands_data.val, self.commands)
+            print(explanation)
+
         print("\n--- -------------- ---\n")
 
     def execute_commands(self, config: Config):
         self.initialize()
         if config.verbosity >= 1:
-            self.print_graph()
+            self.print_graph(config.explain_graph)
+
+        first_node_id = sorted(self.nodes.keys())[0]
+        next_commands_to_execute = self.execute_node(first_node_id, config)
+        new_next_commands_to_execute = []
+        while True:
+            new_next_commands_to_execute.clear()
+            for next_command_id in next_commands_to_execute:
+                new_next_commands_to_execute.extend(self.execute_node(next_command_id, config))
+            next_commands_to_execute = new_next_commands_to_execute.copy()
 
-        for node_id in sorted(self.nodes.keys()):
-            self.execute_node(node_id, config)
+            if not next_commands_to_execute:
+                break
 
 def generate_graph_build_data(raw_commands_data):
     """
     Parses a commands data string to a JSON to create the graph data
 
     Args:
         raw_commands_data (str): A string containing raw commands data that has not yet been converted to a JSON.
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `commandsgpt-1.1.3/commands_gpt/commands_gpt/regex.py` & `commandsgpt-1.2.0/commands_gpt/commands_gpt/regex.py`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/PKG-INFO` & `commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: commandsgpt
-Version: 1.1.3
+Version: 1.2.0
 Summary: An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 Home-page: https://github.com/AlexisAndradeDev/CommandsGPT
 Author: Martín Alexis Martínez Andrade
 Author-email: alexis.martinez.contacto@gmail.com
 Project-URL: Bug Tracker, https://github.com/AlexisAndradeDev/CommandsGPT/issues
 Project-URL: repository, https://github.com/AlexisAndradeDev/CommandsGPT
 Classifier: License :: OSI Approved :: MIT License
@@ -29,20 +29,32 @@
 ```
 
 If you're using a virtual environment:
 ```
 pipenv install commandsgpt
 ```
 
+You also have to install the OpenAI package:
+
+```
+pip install openai
+```
+
+or
+
+```
+pipenv install openai
+```
+
 # Basic usage
 
 Create a `commands` dictionary that will store the commands described in natural language. Create the functions that will be called when the commands are executed (they must match the arguments and return values of the `commands` dict; the first parameter of these functions must be a Config object). Create a `command_name_to_func` dictionary that will take the name of a command and return the corresponding function.
 
 *Example of commands dictionary*
-```
+```python
 commands = {
     "REQUEST_USER_INPUT": {
         "description": "Asks the user to input data through the interface.",
         "arguments": {
             "message": {"description": "Message displayed to the user related to the data that will be requested (example: 'Enter your age').", "type": "string"},
         },
         "generates_data": {
@@ -50,68 +62,70 @@
         },
     },
     ...
 }
 ```
 
 *Example of a command function*
-```
+```python
 def request_user_input_command(config: Config, graph: Graph, message: str) -> dict[str, Any]:
     input_ = input(f"{message}\n*: ")
     results = {
         "input": input_,
     }
     return results
 ```
 
 *Example of command_name_to_func dictionary*
-```
+```python
 command_name_to_func = {
     "REQUEST_USER_INPUT": request_user_input_command,
     ...
 }
 ```
 
 Add the ***essential commands*** to your commands dictionaries.
 * These are the default commands that implement core logic to the model's thinking, like an IF command.
 * If you already defined your own core logic commands (IF command, THINK command, etc.), then you are free not to use them.
 
-```
+```python
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 ```
 
-Your `config` object: 
-```
-config = Config("gpt-4-0314", verbosity=1) # verbosity is optional
+Your `config` object:
+```python
+# keyword arguments are optional
+config = Config("gpt-4-0314", verbosity=1, explain_graph=True)
 ```
 
 Create an instruction:
 
-```
+```python
 instruction = input("Enter your instruction: ")
 ```
 
 Pass your instruction to the recognizer model:
 
-```
+```python
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 ```
 
 Finally, execute the graph of commands:
 
-```
+```python
 graph.execute_commands(config)
 ```
 
 # Basic example
 
-```
+```python
 from typing import Any
 from pathlib import Path
 from commands_gpt.instruction_recognition import recognize_instruction_and_create_graph
 from commands_gpt.commands.graphs import execute_commands
 from commands_gpt.config import Config
 
 # Commands Natural Language Dict
@@ -175,19 +189,20 @@
 }
 
 from commands_gpt.commands.commands_funcs import add_essential_commands
 add_essential_commands(commands, command_name_to_func)
 
 chat_model = "gpt-4-0314"
 
-config = Config(chat_model, verbosity=1)
+config = Config(chat_model, verbosity=1, explain_graph=True)
 
 instruction = input("Enter your prompt: ")
 graph = recognize_instruction_and_create_graph(
     instruction, config.chat_model, commands, command_name_to_func,
+    verbosity=config.verbosity,
 )
 graph.execute_commands(config)
 ```
 
 # Adding custom commands
 
 You can add and modify your own custom commands by creating two dictionaries:
@@ -211,15 +226,15 @@
         * The nested dictionaries have keys *description* and *type*.
 
         * **description**: Description of the data field in natural language.
 
         * **type**: Data type. E.g.: "string", "boolean", "int".
 
 ***Example***
-```
+```python
 commands = {
     "WRITE_TO_USER": {
         "description": "Writes something to the interface to communicate with the user.",
         "arguments": {
             "content": {"description": "Content to write.", "type": "string"},
         },
         "generates_data": {},
@@ -253,15 +268,15 @@
     * The arguments must match the arguments from the commands dictionary.
 
     * The return value must be a dictionary which keys must match the "generates_data" key.
 
     * The data types must match the ones declared in the commands dictionary.
 
 ***Example***
-```
+```python
 def write_to_user_command(config: Config, graph: Graph, content: str) -> dict[str, Any]:
     # add newlines because regex data injection replaces newline characters
     # by \\n substrings.
     content_with_newlines = "\n".join(content.split("\\n"))
     print(f">>> {content_with_newlines}")
     return {}
```

### Comparing `commandsgpt-1.1.3/commands_gpt/commandsgpt.egg-info/SOURCES.txt` & `commandsgpt-1.2.0/commands_gpt/commandsgpt.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `commandsgpt-1.1.3/setup.cfg` & `commandsgpt-1.2.0/setup.cfg`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = commandsgpt
-version = 1.1.3
+version = 1.2.0
 author = Martín Alexis Martínez Andrade
 author_email = alexis.martinez.contacto@gmail.com
 description = An implementation of GPT-4 that recognizes which commands it must run to fulfill an instruction, using a graph. Create new commands easily by describing them using natural language and coding the functions corresponding to the commands.
 long_description = file: README.md, LICENSE
 long_description_content_type = text/markdown
 url = https://github.com/AlexisAndradeDev/CommandsGPT
 project_urls =
```

