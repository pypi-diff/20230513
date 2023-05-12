# Comparing `tmp/hackerforms-0.8.0.tar.gz` & `tmp/hackerforms-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/hackerforms-0.8.0.tar", last modified: Mon Aug  1 19:27:37 2022, max compression
+gzip compressed data, was "dist/hackerforms-0.9.0.tar", last modified: Fri Sep  2 03:22:52 2022, max compression
```

## Comparing `hackerforms-0.8.0.tar` & `hackerforms-0.9.0.tar`

### file list

```diff
@@ -1,33 +1,33 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-01 19:27:37.000000 hackerforms-0.8.0/
--rw-r--r--   0 runner    (1001) docker     (121)      687 2022-08-01 19:27:37.000000 hackerforms-0.8.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      332 2022-08-01 19:27:24.000000 hackerforms-0.8.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms/
--rw-r--r--   0 runner    (1001) docker     (121)      459 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      679 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/auth.py
--rw-r--r--   0 runner    (1001) docker     (121)      561 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/exit_hook.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms/generated/
--rw-r--r--   0 runner    (1001) docker     (121)      320 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      536 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/actions.py
--rw-r--r--   0 runner    (1001) docker     (121)      943 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/apis.py
--rw-r--r--   0 runner    (1001) docker     (121)      721 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/file_utils.py
--rw-r--r--   0 runner    (1001) docker     (121)    37594 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/input_types.py
--rw-r--r--   0 runner    (1001) docker     (121)    16506 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)     8219 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/output_types.py
--rw-r--r--   0 runner    (1001) docker     (121)     4463 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    25722 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/page.py
--rw-r--r--   0 runner    (1001) docker     (121)     1141 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/generated/response_types.py
--rw-r--r--   0 runner    (1001) docker     (121)      131 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/input.py
--rw-r--r--   0 runner    (1001) docker     (121)      155 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/parameters.py
--rw-r--r--   0 runner    (1001) docker     (121)     1536 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/socket.py
--rw-r--r--   0 runner    (1001) docker     (121)      408 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/stdio.py
--rw-r--r--   0 runner    (1001) docker     (121)      186 2022-08-01 19:27:24.000000 hackerforms-0.8.0/hackerforms/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)      687 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      734 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       48 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-08-01 19:27:37.000000 hackerforms-0.8.0/hackerforms.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-01 19:27:37.000000 hackerforms-0.8.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      805 2022-08-01 19:27:24.000000 hackerforms-0.8.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-01 19:27:37.000000 hackerforms-0.8.0/test/
--rw-r--r--   0 runner    (1001) docker     (121)       87 2022-08-01 19:27:24.000000 hackerforms-0.8.0/test/test_dummy.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-02 03:22:52.000000 hackerforms-0.9.0/
+-rw-r--r--   0 runner    (1001) docker     (121)      687 2022-09-02 03:22:52.000000 hackerforms-0.9.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      332 2022-09-02 03:22:42.000000 hackerforms-0.9.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms/
+-rw-r--r--   0 runner    (1001) docker     (121)      597 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      679 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/auth.py
+-rw-r--r--   0 runner    (1001) docker     (121)      561 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/exit_hook.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms/generated/
+-rw-r--r--   0 runner    (1001) docker     (121)      320 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      891 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/actions.py
+-rw-r--r--   0 runner    (1001) docker     (121)      943 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/apis.py
+-rw-r--r--   0 runner    (1001) docker     (121)      721 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/file_utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)    43516 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/input_types.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21260 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8998 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/output_types.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5163 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    30691 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/page.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1141 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/generated/response_types.py
+-rw-r--r--   0 runner    (1001) docker     (121)      223 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/overloads.py
+-rw-r--r--   0 runner    (1001) docker     (121)      155 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/parameters.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1708 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/socket.py
+-rw-r--r--   0 runner    (1001) docker     (121)      408 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/stdio.py
+-rw-r--r--   0 runner    (1001) docker     (121)      203 2022-09-02 03:22:42.000000 hackerforms-0.9.0/hackerforms/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)      687 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      738 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       48 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       12 2022-09-02 03:22:52.000000 hackerforms-0.9.0/hackerforms.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-09-02 03:22:52.000000 hackerforms-0.9.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)      815 2022-09-02 03:22:42.000000 hackerforms-0.9.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-02 03:22:52.000000 hackerforms-0.9.0/test/
+-rw-r--r--   0 runner    (1001) docker     (121)       87 2022-09-02 03:22:42.000000 hackerforms-0.9.0/test/test_dummy.py
```

### Comparing `hackerforms-0.8.0/PKG-INFO` & `hackerforms-0.9.0/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hackerforms
-Version: 0.8.0
+Version: 0.9.0
 Summary: Hacker Forms
 Home-page: https://github.com/abstra-app/hackerforms-lib
 License: MIT
 Description: # Hackerforms
         Launch interactive Python scripts as beautiful form-like apps
         
         [Try it now on Abstra Cloud](https://www.abstracloud.com/forms)
```

### Comparing `hackerforms-0.8.0/hackerforms/auth.py` & `hackerforms-0.9.0/hackerforms/auth.py`

 * *Files identical despite different names*

### Comparing `hackerforms-0.8.0/hackerforms/exit_hook.py` & `hackerforms-0.9.0/hackerforms/exit_hook.py`

 * *Files identical despite different names*

### Comparing `hackerforms-0.8.0/hackerforms/generated/apis.py` & `hackerforms-0.9.0/hackerforms/generated/apis.py`

 * *Files identical despite different names*

### Comparing `hackerforms-0.8.0/hackerforms/generated/file_utils.py` & `hackerforms-0.9.0/hackerforms/generated/file_utils.py`

 * *Files identical despite different names*

### Comparing `hackerforms-0.8.0/hackerforms/generated/input_types.py` & `hackerforms-0.9.0/hackerforms/generated/input_types.py`

 * *Files 19% similar despite different names*

```diff
@@ -38,15 +38,16 @@
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
-
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.placeholder = kwargs.get("placeholder", "Your answer here")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
@@ -70,54 +71,33 @@
         """
         Returns:
             str: The value entered by the user
         """
         return answer
 
 
-class ExecuteJs(Input):
-    type = "execute-js"
-
-    def __init__(self, key: str, code: str, **kwargs):
-        super().__init__(key)
-        self.key = key
-        self.code = code
-        self.context = kwargs.get("context", {})
-
-    def json(self):
-        return {
-            "type": self.type,
-            "code": self.code,
-            "context": self.context,
-            "key": self.key,
-        }
-
-    def convert_answer(self, answer: str) -> str:
-        """
-        Returns:
-            string: Serialized return value of the executed JavaScript
-        """
-        return answer
-
-
 class TagInput(Input):
 
     type = "tag-input"
 
     def __init__(self, key: str, message: str, **kwargs):
         """Read a tag value from the user
 
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
-            initial_value (str or float): The initial value to display to the user
+            initial_value (list): The initial value to display to the user
+            placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
+
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", [])
         self.placeholder = kwargs.get("placeholder", "Your answer here")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.columns = kwargs.get("columns", 1)
@@ -137,15 +117,15 @@
         }
 
     def convert_answer(
         self, answer: typing.List[typing.Union[str, float]]
     ) -> typing.List[typing.Union[str, float]]:
         """
         Returns:
-            List[Union[str,float]]: The value entered by the user
+            list(str) or list(float): The value entered by the user
         """
 
         return answer
 
 
 class DateInput(Input):
     type = "date-input"
@@ -156,14 +136,16 @@
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (datetime.date or time.struct_time or str (YYYY-MM-DD)): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
 
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", None)
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
@@ -218,14 +200,17 @@
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            multiple (bool): Whether the user will be allowed to upload multiple files
 
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
@@ -245,15 +230,15 @@
             "multiple": self.multiple,
             "fullWidth": self.full_width,
         }
 
     def convert_answer(self, answer) -> typing.Optional[FileResponse]:
         """
         Returns:
-            FileResponse: The file uploaded by the user the user
+            FileResponse: A dict containing the file uploaded by the user ({"file": file, "url": str, "content": bytes})
         """
         if not answer:
             return None
 
         if not self.multiple:
             return FileResponse(answer)
 
@@ -269,14 +254,17 @@
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            multiple (bool): Whether the user will be allowed to upload multiple files
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.columns = kwargs.get("columns", 1)
@@ -295,15 +283,15 @@
             "multiple": self.multiple,
             "fullWidth": self.full_width,
         }
 
     def convert_answer(self, answer) -> typing.Optional[FileResponse]:
         """
         Returns:
-            FileResponse: The image file uploaded by the user the user
+            FileResponse: A dict containing the image file uploaded by the user ({"file": file, "url": str, "content": bytes})
         """
         if not answer:
             return None
 
         if not self.multiple:
             return FileResponse(answer)
 
@@ -319,14 +307,17 @@
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            multiple (bool): Whether the user will be allowed to upload multiple files
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.columns = kwargs.get("columns", 1)
@@ -345,15 +336,15 @@
             "multiple": self.multiple,
             "fullWidth": self.full_width,
         }
 
     def convert_answer(self, answer) -> typing.Optional[FileResponse]:
         """
         Returns:
-            FileResponse: The video file uploaded by the user the user
+            FileResponse: A dict containing the video uploaded by the user ({"file": file, "url": str, "content": bytes})
         """
         if not answer:
             return None
 
         if not self.multiple:
             return FileResponse(answer)
 
@@ -374,48 +365,56 @@
 
         Positional Args:
             message (str): The message to display to the user
             options (list): The options to display to the user, eg. ['Option 1', 'Option 2'] or [{'label': 'Option 1', 'value': '1'}, {'label': 'Option 2', 'value': '2'}]
 
         Keyword Args:
             multiple (bool): Whether the user can select multiple options
+            min (number): The minimal amount of options that should be selected
+            max (number): The maximum amount of options that should be selected
             button_text (str): The text to display on the button that will submit the value
             initial_value: The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.message = message
         self.options = options
         self.multiple = kwargs.get("multiple", False)
         self.initial_value = kwargs.get("initial_value", None)
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
+        self.min = kwargs.get("min", None)
+        self.max = kwargs.get("max", None)
 
     def json(self):
         return {
             "type": self.type,
             "key": self.key,
             "message": self.message,
             "options": self.options,
             "hint": self.hint,
             "multiple": self.multiple,
             "initialValue": self.initial_value,
             "required": self.required,
             "columns": self.columns,
             "fullWidth": self.full_width,
+            "min": self.min,
+            "max": self.max,
         }
 
     def convert_answer(
         self, answer: typing.Union[typing.List, typing.Any]
     ) -> typing.Union[typing.List, typing.Any]:
         """
         Returns:
-            list, any: The values/value selected by the user
+            list or any: The values/value selected by the user
         """
         return answer
 
 
 class CardsInput(Input):
     type = "cards-input"
 
@@ -429,14 +428,17 @@
                                 {'title': 'Option 2', 'image': 'https://image_2.png', 'description': 'option 2 description'}]
 
         Keyword Args:
             multiple (bool): Whether the user can select multiple options
             button_text (str): The text to display on the button that will submit the value
             initial_value (list): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            searchable (bool): Whether to show a search bar
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.label = label
         self.options = options
         self.multiple = kwargs.get("multiple", False)
         self.searchable = kwargs.get("searchable", False)
         self.initial_value = kwargs.get("initial_value", None)
@@ -490,14 +492,16 @@
 
         Keyword Args:
             multiple (bool): Whether the user can select multiple options
             button_text (str): The text to display on the button that will submit the value
             initial_value: The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.message = message
         self.options = options
         self.initial_value = kwargs.get("initial_value", None)
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
@@ -539,14 +543,16 @@
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
 
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.placeholder = kwargs.get("placeholder", "Your answer here")
@@ -585,14 +591,16 @@
             label (str): The label to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
             language (str): The programming language
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
 
         """
         super().__init__(key)
         self.label = label
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.language = kwargs.get("language", None)
@@ -627,28 +635,30 @@
     def __init__(self, key: str, label: str, **kwargs):
         """Gets NPS feedback from user
 
         Positional Args:
             label (str): The label to display to the user
 
         Keyword Args:
-            min (int): The text to display on the button that will submit the value
-            max (int): The initial value to display to the user
-            min_hint (str): Whether the input is required or not eg. "this field is required"
-            max_hint (str): The programming language
+            min (int): Min value accepted by the input
+            max (int): Max value accepted by the input
+            min_hint (str): Text to display next to the min value
+            max_hint (str): Text to display next to the max value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
 
         """
         super().__init__(key)
         self.label = label
         self.initial_value = kwargs.get("initial_value", None)
         self.required = kwargs.get("required", True)
         self.min = kwargs.get("min", 0)
-        self.max = kwargs.get("min", 10)
+        self.max = kwargs.get("max", 10)
         self.min_hint = kwargs.get("min_hint", "Not at all likely")
         self.max_hint = kwargs.get("max_hint", "Extremely likely")
         self.columns = kwargs.get("columns", 1)
         self.hint = kwargs.get("hint", None)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
@@ -663,38 +673,43 @@
             "initialValue": self.initial_value,
             "required": self.required,
             "columns": self.columns,
             "hint": self.hint,
             "fullWidth": self.full_width,
         }
 
-    def convert_answer(self, answer: int) -> str:
+    def convert_answer(self, answer: int) -> int:
         """
         Returns:
-            str: The value entered by the user
+            int: The value entered by the user
         """
         return answer
 
 
 class NumberInput(Input):
     type = "number-input"
 
     def __init__(self, key: str, message: str, **kwargs):
         """Read a number value from the user
 
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
-            message (str): The message to display to the user
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            min (float): Min value accepted by the input
+            max (float): Max value accepted by the input
+            step (float): The value to be incremented or decremented while using the input button
         """
+
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", 0)
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.placeholder = kwargs.get("placeholder", "Your answer here")
         self.columns = kwargs.get("columns", 1)
@@ -715,18 +730,18 @@
             "columns": self.columns,
             "fullWidth": self.full_width,
             "min": self.min,
             "max": self.max,
             "step": self.step,
         }
 
-    def convert_answer(self, answer: int) -> int:
+    def convert_answer(self, answer: float) -> float:
         """
         Returns:
-            int: The value entered by the user
+            float: The value entered by the user
         """
         return answer
 
 
 class EmailInput(Input):
     type = "email-input"
 
@@ -737,14 +752,16 @@
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.placeholder = kwargs.get("placeholder", "Your email here")
@@ -782,14 +799,16 @@
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.placeholder = kwargs.get("placeholder", "")
@@ -808,15 +827,15 @@
             "columns": self.columns,
             "fullWidth": self.full_width,
         }
 
     def convert_answer(self, answer) -> typing.Optional[PhoneResponse]:
         """
         Returns:
-            PhoneResponse: The value entered by the user
+            PhoneResponse: A dict containing the value entered by the user ({"raw": str, "masked": str})
         """
         return (
             PhoneResponse(raw=answer["raw"], masked=answer["masked"])
             if answer
             else None
         )
 
@@ -828,14 +847,20 @@
         """Read a list value from the user
 
         Positional Args:
             item_schema (ListItemSchema): The schema for the items of the list
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
+            initial_value (str): The initial value to display to the user
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            min (float): Min value accepted by the input
+            max (float): Max value accepted by the input
+            add_button_text (str): Label to be displayed on the add button. The default is "+".
         """
         super().__init__(key)
         self.item_schema = item_schema
         self.initial_value = kwargs.get("initial_value", [{}])
         self.min = kwargs.get("min", None)
         self.max = kwargs.get("max", None)
         self.hint = kwargs.get("hint", None)
@@ -872,16 +897,18 @@
     def __init__(self, key: str, df: typing.Any, **kwargs):
         """Display a pandas dataframe as a table and allow the user to select rows
 
         Positional Args:
             df (pandas.DataFrame): The pandas dataframe to be displayed
 
         Keyword Args:
+            button_text (str): The text to display on the button that will submit the value
             required: Whether the input is required or not
-            button_text (string): The text to display on the next step button
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
 
         """
         super().__init__(key)
         self.df = df
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
         self.columns = kwargs.get("columns", 1)
@@ -897,37 +924,40 @@
             "columns": self.columns,
             "fullWidth": self.full_width,
         }
 
     def convert_answer(self, answer) -> typing.List:
         """
         Returns:
-            The list of selected rows
+            list: The list of selected rows
         """
         return answer
 
 
 class HTMLListInput(Input):
     type = "html-list-input"
 
     def __init__(self, key: str, label: str, options: typing.Any, **kwargs):
         """Read list of html values from the user
 
         Positional Args:
             label (str): The text related to this field
             options (list): The options to display to the user, eg. [
-                                {'html': '<div class="container"><p>Info 1A</><p>Info 1B</p></div>', 'value': 'info1'},
-                                {'html': '<div class="container"><p>Info 2A</><p>Info 2B</p></div>', 'value': 'info2'}]
+                                {'html': '<div class="container">Info 1A</div>', 'value': 'info1'},
+                                {'html': '<div class="container">Info 2B</div>', 'value': 'info2'}
+                            ]
 
         Keyword Args:
-            css (str): The css related to the html item in options
-            multiple (bool): Whether the user can select multiple options
             button_text (str): The text to display on the button that will submit the value
             initial_value (list): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            multiple (bool): Whether the user can select multiple options
+            css (str): The css related to the html item in options
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
         super().__init__(key)
         self.label = label
         self.options = options
         self.css = kwargs.get("css", None)
         self.multiple = kwargs.get("multiple", False)
         self.initial_value = kwargs.get("initial_value", None)
@@ -971,14 +1001,16 @@
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             initial_value (str): The initial value to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
             format (str): Whether the input is in the format 24hs or AM/PM. Default is 24hs.
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
         """
 
         super().__init__(key)
         self.message = message
         self.initial_value = kwargs.get("initial_value", "")
         self.required = kwargs.get("required", True)
         self.hint = kwargs.get("hint", None)
@@ -995,18 +1027,77 @@
             "hint": self.hint,
             "initialValue": self.initial_value,
             "required": self.required,
             "columns": self.columns,
             "fullWidth": self.full_width,
         }
 
-    def convert_answer(self, answer: str) -> str:
+    def convert_answer(self, answer) -> datetime.time:
         """
         Returns:
-            str: The value selected by the user
+            datetime.time: A datetime.time object representing the value entered by the user
+        """
+        return datetime.time(answer["hour"], answer["minute"]) if answer else None
+
+
+class CurrencyInput(Input):
+    type = "currency-input"
+
+    def __init__(self, key: str, message: str, **kwargs):
+        """Read a number value from the user with a currency mask
+
+        Positional Args:
+            message (str): The message to display to the user
+
+        Keyword Args:
+            button_text (str): The text to display on the button that will submit the value
+            initial_value (str): The initial value to display to the user
+            required (bool or str): Whether the input is required or not, eg. "this field is required"
+            placeholder (str): The placeholder text to display to the user
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
+            min (float): The minimum value allowed, eg. "0"
+            max (float): The maximum value allowed, eg. "100"
+            step (float): The value to be incremented or decremented while using the input button
+            currency (str): The currency to display to the user, eg. "USD", "BRL, "EUR", "GBP" (default is USD)
+        """
+        super().__init__(key)
+        self.message = message
+        self.initial_value = kwargs.get("initial_value", 0)
+        self.required = kwargs.get("required", True)
+        self.hint = kwargs.get("hint", None)
+        self.placeholder = kwargs.get("placeholder", "Your answer here")
+        self.columns = kwargs.get("columns", 1)
+        self.full_width = kwargs.get("full_width", False)
+        self.min = kwargs.get("min")
+        self.max = kwargs.get("max")
+        self.step = kwargs.get("step")
+        self.currency = kwargs.get("currency", "USD")
+
+    def json(self):
+        return {
+            "type": self.type,
+            "key": self.key,
+            "message": self.message,
+            "initialValue": self.initial_value,
+            "placeholder": self.placeholder,
+            "required": self.required,
+            "hint": self.hint,
+            "columns": self.columns,
+            "fullWidth": self.full_width,
+            "min": self.min,
+            "max": self.max,
+            "step": self.step,
+            "currency": self.currency,
+        }
+
+    def convert_answer(self, answer) -> float:
+        """
+        Returns:
+            float: The value entered by the user
         """
         return answer
 
 
 class PasswordInput(Input):
     type = "password-input"
 
@@ -1016,23 +1107,27 @@
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will submit the value
             placeholder (str): The placeholder text to display to the user
             required (bool or str): Whether the input is required or not eg. "this field is required"
+            hint (str): A tooltip displayed to the user
+            full_width (bool): Whether the input should use full screen width
             lowercase_required (bool or str): Whether the input must have at least one lowercase character
             uppercase_required (bool or str): Whether the input must have at least one uppercase character
             special_required (bool or str): Whether the input must have at least one special character
             digit_required (bool or str): Whether the input must have at least one digit
             min_length (int): Minimum length of the password
             max_length (int): Maximum length of the password
             size (int): Size of the password
             pattern (str): A regex pattern for the accepted password
+            autocomplete (str): The autocomplete HTML attribute
         """
+
         super().__init__(key)
         self.message = message
         self.hint = kwargs.get("hint", None)
         self.required = kwargs.get("required", True)
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
         self.lowercase_required = kwargs.get("lowercase_required", True)
```

### Comparing `hackerforms-0.8.0/hackerforms/generated/inputs.py` & `hackerforms-0.9.0/hackerforms/generated/inputs.py`

 * *Files 20% similar despite different names*

```diff
@@ -30,14 +30,17 @@
       label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'title': 'Option 1', 'image': 'https://image_1.png', 'description': 'option 1 description'},{'title': 'Option 2', 'image': 'https://image_2.png', 'description': 'option 2 description'}]
 
     Keyword Args:
       multiple (bool): Whether the user can select multiple options
       button_text (str): The text to display on the button that will submit the value
       initial_value (list): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      searchable (bool): Whether to show a search bar
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           list, any: The options/option selected by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(
         Page().read_cards(label, options, **kwargs).run(button_text)
@@ -51,32 +54,61 @@
       label (str): The label to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
       language (str): The programming language
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           str: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_code(label, **kwargs).run(button_text))
 
 
+def read_currency(message: str, **kwargs):
+    """Read a number value from the user with a currency mask
+
+    Positional Args:
+      message (str): The message to display to the user
+
+    Keyword Args:
+      button_text (str): The text to display on the button that will submit the value
+      initial_value (str): The initial value to display to the user
+      required (bool or str): Whether the input is required or not, eg. "this field is required"
+      placeholder (str): The placeholder text to display to the user
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      min (float): The minimum value allowed, eg. "0"
+      max (float): The maximum value allowed, eg. "100"
+      step (float): The value to be incremented or decremented while using the input button
+      currency (str): The currency to display to the user, eg. "USD", "BRL, "EUR", "GBP" (default is USD)
+
+      Returns:
+          float: The value entered by the user
+    """
+    button_text = kwargs.get("button_text", "Next")
+    return get_single_value(Page().read_currency(message, **kwargs).run(button_text))
+
+
 def read_date(message: str, **kwargs):
     """Read a date value from the user
 
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (datetime.date or time.struct_time or str (YYYY-MM-DD)): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           datetime.date: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_date(message, **kwargs).run(button_text))
 
@@ -93,14 +125,16 @@
 
     Keyword Args:
       multiple (bool): Whether the user can select multiple options
       button_text (str): The text to display on the button that will submit the value
       initial_value: The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           str: The value selected by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(
         Page().read_dropdown(message, options, **kwargs).run(button_text)
@@ -114,14 +148,16 @@
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           str: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_email(message, **kwargs).run(button_text))
 
@@ -132,34 +168,39 @@
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      multiple (bool): Whether the user will be allowed to upload multiple files
 
       Returns:
-          FileResponse: The file uploaded by the user the user
+          FileResponse: A dict containing the file uploaded by the user ({"file": file, "url": str, "content": bytes})
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_file(message, **kwargs).run(button_text))
 
 
 def read_html_list(label: str, options: typing.Any, **kwargs):
     """Read list of html values from the user
 
     Positional Args:
-      label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'html': '<div class="container"><p>Info 1A</><p>Info 1B</p></div>', 'value': 'info1'},{'html': '<div class="container"><p>Info 2A</><p>Info 2B</p></div>', 'value': 'info2'}]
+      label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'html': '<div class="container">Info 1A</div>', 'value': 'info1'},{'html': '<div class="container">Info 2B</div>', 'value': 'info2'}]
 
     Keyword Args:
-      css (str): The css related to the html item in options
-      multiple (bool): Whether the user can select multiple options
       button_text (str): The text to display on the button that will submit the value
       initial_value (list): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      multiple (bool): Whether the user can select multiple options
+      css (str): The css related to the html item in options
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           list, any: The options/option selected by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(
         Page().read_html_list(label, options, **kwargs).run(button_text)
@@ -172,30 +213,39 @@
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      multiple (bool): Whether the user will be allowed to upload multiple files
 
       Returns:
-          FileResponse: The image file uploaded by the user the user
+          FileResponse: A dict containing the image file uploaded by the user ({"file": file, "url": str, "content": bytes})
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_image(message, **kwargs).run(button_text))
 
 
 def read_list(item_schema: typing.Any, **kwargs):
     """Read a list value from the user
 
     Positional Args:
       item_schema (ListItemSchema): The schema for the items of the list
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
+      initial_value (str): The initial value to display to the user
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      min (float): Min value accepted by the input
+      max (float): Max value accepted by the input
+      add_button_text (str): Label to be displayed on the add button. The default is "+".
 
       Returns:
           list: The values entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_list(item_schema, **kwargs).run(button_text))
 
@@ -208,80 +258,92 @@
     """Read a multiple choice value from the user
 
     Positional Args:
       message (str): The message to display to the useroptions (list): The options to display to the user, eg. ['Option 1', 'Option 2'] or [{'label': 'Option 1', 'value': '1'}, {'label': 'Option 2', 'value': '2'}]
 
     Keyword Args:
       multiple (bool): Whether the user can select multiple options
+      min (number): The minimal amount of options that should be selected
+      max (number): The maximum amount of options that should be selected
       button_text (str): The text to display on the button that will submit the value
       initial_value: The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          list, any: The values/value selected by the user
+          list or any: The values/value selected by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(
         Page().read_multiple_choice(message, options, **kwargs).run(button_text)
     )
 
 
 def read_nps(label: str, **kwargs):
     """Gets NPS feedback from user
 
     Positional Args:
       label (str): The label to display to the user
 
     Keyword Args:
-      min (int): The text to display on the button that will submit the value
-      max (int): The initial value to display to the user
-      min_hint (str): Whether the input is required or not eg. "this field is required"
-      max_hint (str): The programming language
+      min (int): Min value accepted by the input
+      max (int): Max value accepted by the input
+      min_hint (str): Text to display next to the min value
+      max_hint (str): Text to display next to the max value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          str: The value entered by the user
+          int: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_nps(label, **kwargs).run(button_text))
 
 
 def read_number(message: str, **kwargs):
     """Read a number value from the user
 
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
-      message (str): The message to display to the user
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      min (float): Min value accepted by the input
+      max (float): Max value accepted by the input
+      step (float): The value to be incremented or decremented while using the input button
 
       Returns:
-          int: The value entered by the user
+          float: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_number(message, **kwargs).run(button_text))
 
 
 def read_pandas_row_selection(df: typing.Any, **kwargs):
     """Display a pandas dataframe as a table and allow the user to select rows
 
     Positional Args:
       df (pandas.DataFrame): The pandas dataframe to be displayed
 
     Keyword Args:
+      button_text (str): The text to display on the button that will submit the value
       required: Whether the input is required or not
-      button_text (string): The text to display on the next step button
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          The list of selected rows
+          list: The list of selected rows
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(
         Page().read_pandas_row_selection(df, **kwargs).run(button_text)
     )
 
 
@@ -291,22 +353,25 @@
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
       lowercase_required (bool or str): Whether the input must have at least one lowercase character
       uppercase_required (bool or str): Whether the input must have at least one uppercase character
       special_required (bool or str): Whether the input must have at least one special character
       digit_required (bool or str): Whether the input must have at least one digit
       min_length (int): Minimum length of the password
       max_length (int): Maximum length of the password
       size (int): Size of the password
       pattern (str): A regex pattern for the accepted password
+      autocomplete (str): The autocomplete HTML attribute
 
       Returns:
           str: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_password(message, **kwargs).run(button_text))
 
@@ -318,35 +383,40 @@
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          PhoneResponse: The value entered by the user
+          PhoneResponse: A dict containing the value entered by the user ({"raw": str, "masked": str})
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_phone(message, **kwargs).run(button_text))
 
 
 def read_tag(message: str, **kwargs):
     """Read a tag value from the user
 
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
-      initial_value (str or float): The initial value to display to the user
+      initial_value (list): The initial value to display to the user
+      placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          List[Union[str,float]]: The value entered by the user
+          list(str) or list(float): The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_tag(message, **kwargs).run(button_text))
 
 
 def read(message: str, **kwargs):
     """Read a text value from the user simple text input
@@ -355,14 +425,16 @@
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           str: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read(message, **kwargs).run(button_text))
 
@@ -374,14 +446,16 @@
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       placeholder (str): The placeholder text to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
           str: The value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_textarea(message, **kwargs).run(button_text))
 
@@ -393,17 +467,19 @@
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
       format (str): Whether the input is in the format 24hs or AM/PM. Default is 24hs.
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
 
       Returns:
-          str: The value selected by the user
+          datetime.time: A datetime.time object representing the value entered by the user
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_time(message, **kwargs).run(button_text))
 
 
 def read_video(message: str, **kwargs):
     """Read a video file value from the user
@@ -411,17 +487,20 @@
     Positional Args:
       message (str): The message to display to the user
 
     Keyword Args:
       button_text (str): The text to display on the button that will submit the value
       initial_value (str): The initial value to display to the user
       required (bool or str): Whether the input is required or not eg. "this field is required"
+      hint (str): A tooltip displayed to the user
+      full_width (bool): Whether the input should use full screen width
+      multiple (bool): Whether the user will be allowed to upload multiple files
 
       Returns:
-          FileResponse: The video file uploaded by the user the user
+          FileResponse: A dict containing the video uploaded by the user ({"file": file, "url": str, "content": bytes})
     """
     button_text = kwargs.get("button_text", "Next")
     return get_single_value(Page().read_video(message, **kwargs).run(button_text))
 
 
 def get_single_value(answer: typing.Dict):
     return list(answer.values())[0]
```

### Comparing `hackerforms-0.8.0/hackerforms/generated/output_types.py` & `hackerforms-0.9.0/hackerforms/generated/output_types.py`

 * *Files 7% similar despite different names*

```diff
@@ -27,16 +27,17 @@
         """Display a message to the user
 
         Positional Args:
             message (str): The message to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
         """
-        self.message = message
+        self.message = str(message)
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
         return {
             "type": self.type,
             "message": self.message,
@@ -52,14 +53,15 @@
         """Display a formatted text to the user
 
         Positional Args:
             text (str): The formatted text to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
         """
         self.text = text
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
         return {
@@ -76,16 +78,18 @@
     def __init__(self, image: typing.Union[str, io.IOBase], **kwargs):
         """Display an image to the user
 
         Positional Args:
             image (file-like or str (path, url, base64)): The image to display to the user
 
         Keyword Args:
-            subtitle (str): The subtitle of the image
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+            subtitle (str): The subtitle of the image
+
         """
         self.image = image
         self.subtitle = kwargs.get("subtitle", "")
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
@@ -104,17 +108,19 @@
     def __init__(self, link_url: str, **kwargs):
         """Display a link to the user
 
         Positional Args:
             link_url (str): The url of the link to display to the user
 
         Keyword Args:
-            link_text (str): The text to display on the link
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+            link_text (str): The text to display on the link
             same_tab (bool): Whether to open the link in the same tab or not
+
         """
         self.link_url = link_url
         self.link_text = kwargs.get("link_text", "Click here")
         self.same_tab = kwargs.get("same_tab", False)
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
@@ -137,14 +143,16 @@
 
         Positional Args:
             file (file-like or str (path, url, base64)): The file to download
 
         Keyword Args:
             download_text (str): The text to display on the button that will download the file
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+
         """
         self.file = file
         self.download_text = kwargs.get("download_text", "Download here")
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
@@ -161,14 +169,15 @@
     type = "html-output"
 
     def __init__(self, html: str, **kwargs):
         """Display a html snippet to the user
 
         Positional Args:
             html (str): The html snippet to display to the user
+            full_width (bool): Whether the input should use full screen width
 
         Keyword Args:
             button_text (str): The text to display on the button that will continue the form
         """
         self.html = html
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
@@ -189,14 +198,17 @@
         """Display a pandas dataframe to the user
 
         Positional Args:
             df (pandas.DataFrame): The dataframe to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+            display_index (bool): Whether to show a index column
+
         """
         self.df = df
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
         self.display_index = kwargs.get("display_index", False)
 
     def json(self):
@@ -216,14 +228,16 @@
         """Display a plotly figure to the user
 
         Positional Args:
             fig (plotly.Figure): The figure to display to the user
 
         Keyword Args:
             button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+
         """
         self.fig = fig
         self.columns = kwargs.get("columns", 1)
         self.full_width = kwargs.get("full_width", False)
 
     def json(self):
         return {
@@ -240,18 +254,21 @@
     def __init__(self, url_or_html: str, **kwargs):
         """Display an inline iframe to the user
 
         Positional Args:
             url_or_html (str): The link to the document or the own document to display to the user
 
         Keyword Args:
+            button_text (str): The text to display on the button that will continue the form
             width (int): The width of the iframe
             height (int): The height of the iframe
-            button_text (str): The text to display on the button that will continue the form
+            full_width (bool): Whether the input should use full screen width
+
         """
+
         if url(url_or_html):
             self.url = url_or_html
         else:
             self.url = f"data:text/html,{quote(url_or_html)}"
 
         self.width = kwargs.get("width", 800)
         self.height = kwargs.get("height", 600)
```

### Comparing `hackerforms-0.8.0/hackerforms/generated/page.py` & `hackerforms-0.9.0/hackerforms/generated/page.py`

 * *Files 12% similar despite different names*

```diff
@@ -31,41 +31,27 @@
     def json(self):
         """Get the json representation of the form
         Returns:
             The json representation of the form
         """
         return [widget.json() for widget in self.widgets]
 
-    def execute_js(self, code: str, **kwargs):
-        """Execute JavaScript on the page
-
-        Args:
-            code: The JS code to be executed
-        Keyword Arg:
-            context (dict): variables to be passed to the JS code
-            key (string): The key of the return value on the form result. Defaults to empty string
-
-        Returns:
-            string: Serialized return value of the executed JavaScript
-        """
-
-        key = kwargs.pop("key", "js_result")
-        self.widgets.append(ExecuteJs(key, code, **kwargs))
-        return self
-
     def read_cards(self, label: str, options: typing.Any, **kwargs):
         """Read cards from the user
 
         Positional Args:
           label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'title': 'Option 1', 'image': 'https://image_1.png', 'description': 'option 1 description'},{'title': 'Option 2', 'image': 'https://image_2.png', 'description': 'option 2 description'}]
 
         Keyword Args:
           multiple (bool): Whether the user can select multiple options
           initial_value (list): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          searchable (bool): Whether to show a search bar
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the label arg
 
 
         Returns:
           The form object
         """
@@ -79,34 +65,65 @@
         Positional Args:
           label (str): The label to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
           language (str): The programming language
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the label arg
 
 
         Returns:
           The form object
         """
         key = kwargs.pop("key", label)
         self.widgets.append(CodeInput(key, label, **kwargs))
         return self
 
+    def read_currency(self, message: str, **kwargs):
+        """Read a number value from the user with a currency mask
+
+        Positional Args:
+          message (str): The message to display to the user
+
+        Keyword Args:
+          initial_value (str): The initial value to display to the user
+          required (bool or str): Whether the input is required or not, eg. "this field is required"
+          placeholder (str): The placeholder text to display to the user
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          min (float): The minimum value allowed, eg. "0"
+          max (float): The maximum value allowed, eg. "100"
+          step (float): The value to be incremented or decremented while using the input button
+          currency (str): The currency to display to the user, eg. "USD", "BRL, "EUR", "GBP" (default is USD)
+          columns: The number of columns of the input
+          key: The key of the input's value on the form result. Defaults to the message arg
+
+
+        Returns:
+          The form object
+        """
+        key = kwargs.pop("key", message)
+        self.widgets.append(CurrencyInput(key, message, **kwargs))
+        return self
+
     def read_date(self, message: str, **kwargs):
         """Read a date value from the user
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (datetime.date or time.struct_time or str (YYYY-MM-DD)): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -126,14 +143,16 @@
           message (str): The message to display to the useroptions (list): The options to display to the user, eg. ['Option 1', 'Option 2'] or [{'label': 'Option 1', 'value': '1'}, {'label': 'Option 2', 'value': '2'}]
 
         Keyword Args:
           multiple (bool): Whether the user can select multiple options
           initial_value: The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -147,14 +166,16 @@
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -167,14 +188,17 @@
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          multiple (bool): Whether the user will be allowed to upload multiple files
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -182,21 +206,23 @@
         self.widgets.append(FileInput(key, message, **kwargs))
         return self
 
     def read_html_list(self, label: str, options: typing.Any, **kwargs):
         """Read list of html values from the user
 
         Positional Args:
-          label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'html': '<div class="container"><p>Info 1A</><p>Info 1B</p></div>', 'value': 'info1'},{'html': '<div class="container"><p>Info 2A</><p>Info 2B</p></div>', 'value': 'info2'}]
+          label (str): The text related to this fieldoptions (list): The options to display to the user, eg. [{'html': '<div class="container">Info 1A</div>', 'value': 'info1'},{'html': '<div class="container">Info 2B</div>', 'value': 'info2'}]
 
         Keyword Args:
-          css (str): The css related to the html item in options
-          multiple (bool): Whether the user can select multiple options
           initial_value (list): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          multiple (bool): Whether the user can select multiple options
+          css (str): The css related to the html item in options
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the label arg
 
 
         Returns:
           The form object
         """
@@ -209,14 +235,17 @@
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          multiple (bool): Whether the user will be allowed to upload multiple files
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -227,14 +256,20 @@
     def read_list(self, item_schema: typing.Any, **kwargs):
         """Read a list value from the user
 
         Positional Args:
           item_schema (ListItemSchema): The schema for the items of the list
 
         Keyword Args:
+          initial_value (str): The initial value to display to the user
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          min (float): Min value accepted by the input
+          max (float): Max value accepted by the input
+          add_button_text (str): Label to be displayed on the add button. The default is "+".
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the "result" arg
 
 
         Returns:
           The form object
         """
@@ -251,16 +286,20 @@
         """Read a multiple choice value from the user
 
         Positional Args:
           message (str): The message to display to the useroptions (list): The options to display to the user, eg. ['Option 1', 'Option 2'] or [{'label': 'Option 1', 'value': '1'}, {'label': 'Option 2', 'value': '2'}]
 
         Keyword Args:
           multiple (bool): Whether the user can select multiple options
+          min (number): The minimal amount of options that should be selected
+          max (number): The maximum amount of options that should be selected
           initial_value: The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -271,20 +310,22 @@
     def read_nps(self, label: str, **kwargs):
         """Gets NPS feedback from user
 
         Positional Args:
           label (str): The label to display to the user
 
         Keyword Args:
-          min (int): The text to display on the button that will submit the value
-          max (int): The initial value to display to the user
-          min_hint (str): Whether the input is required or not eg. "this field is required"
-          max_hint (str): The programming language
+          min (int): Min value accepted by the input
+          max (int): Max value accepted by the input
+          min_hint (str): Text to display next to the min value
+          max_hint (str): Text to display next to the max value
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the label arg
 
 
         Returns:
           The form object
         """
@@ -295,18 +336,22 @@
     def read_number(self, message: str, **kwargs):
         """Read a number value from the user
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
-          message (str): The message to display to the user
           initial_value (str): The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          min (float): Min value accepted by the input
+          max (float): Max value accepted by the input
+          step (float): The value to be incremented or decremented while using the input button
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -318,14 +363,16 @@
         """Display a pandas dataframe as a table and allow the user to select rows
 
         Positional Args:
           df (pandas.DataFrame): The pandas dataframe to be displayed
 
         Keyword Args:
           required: Whether the input is required or not
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the "result" arg
 
 
         Returns:
           The form object
         """
@@ -338,22 +385,25 @@
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           lowercase_required (bool or str): Whether the input must have at least one lowercase character
           uppercase_required (bool or str): Whether the input must have at least one uppercase character
           special_required (bool or str): Whether the input must have at least one special character
           digit_required (bool or str): Whether the input must have at least one digit
           min_length (int): Minimum length of the password
           max_length (int): Maximum length of the password
           size (int): Size of the password
           pattern (str): A regex pattern for the accepted password
+          autocomplete (str): The autocomplete HTML attribute
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -367,14 +417,16 @@
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -385,16 +437,19 @@
     def read_tag(self, message: str, **kwargs):
         """Read a tag value from the user
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
-          initial_value (str or float): The initial value to display to the user
+          initial_value (list): The initial value to display to the user
+          placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -408,14 +463,16 @@
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -430,14 +487,16 @@
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           placeholder (str): The placeholder text to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -451,14 +510,16 @@
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
           format (str): Whether the input is in the format 24hs or AM/PM. Default is 24hs.
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -471,14 +532,17 @@
 
         Positional Args:
           message (str): The message to display to the user
 
         Keyword Args:
           initial_value (str): The initial value to display to the user
           required (bool or str): Whether the input is required or not eg. "this field is required"
+          hint (str): A tooltip displayed to the user
+          full_width (bool): Whether the input should use full screen width
+          multiple (bool): Whether the user will be allowed to upload multiple files
           columns: The number of columns of the input
           key: The key of the input's value on the form result. Defaults to the message arg
 
 
         Returns:
           The form object
         """
@@ -492,14 +556,15 @@
 
         Positional Args:
           file (file-like or str (path, url, base64)): The file to download
 
 
         Keyword Args:
           download_text (str): The text to display on the button that will download the file
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(FileOutput(file, **kwargs))
@@ -507,14 +572,15 @@
 
     def display_html(self, html: str, **kwargs):
         """Display a html snippet to the user
 
 
         Positional Args:
           html (str): The html snippet to display to the user
+          full_width (bool): Whether the input should use full screen width
 
 
         Keyword Args:
           columns: The number of columns of the input
 
 
         Returns:
@@ -530,14 +596,15 @@
         Positional Args:
           url_or_html (str): The link to the document or the own document to display to the user
 
 
         Keyword Args:
           width (int): The width of the iframe
           height (int): The height of the iframe
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(IFrameOutput(url_or_html, **kwargs))
@@ -548,14 +615,15 @@
 
 
         Positional Args:
           image (file-like or str (path, url, base64)): The image to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
           subtitle (str): The subtitle of the image
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
@@ -567,14 +635,15 @@
 
 
         Positional Args:
           link_url (str): The url of the link to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
           link_text (str): The text to display on the link
           same_tab (bool): Whether to open the link in the same tab or not
           columns: The number of columns of the input
 
 
         Returns:
           The form object
@@ -587,14 +656,15 @@
 
 
         Positional Args:
           text (str): The formatted text to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(MarkdownOutput(text, **kwargs))
@@ -605,14 +675,16 @@
 
 
         Positional Args:
           df (pandas.DataFrame): The dataframe to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
+          display_index (bool): Whether to show a index column
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(PandasOutput(df, **kwargs))
@@ -623,14 +695,15 @@
 
 
         Positional Args:
           fig (plotly.Figure): The figure to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(PlotlyOutput(fig, **kwargs))
@@ -641,14 +714,15 @@
 
 
         Positional Args:
           message (str): The message to display to the user
 
 
         Keyword Args:
+          full_width (bool): Whether the input should use full screen width
           columns: The number of columns of the input
 
 
         Returns:
           The form object
         """
         self.widgets.append(TextOutput(message, **kwargs))
```

### Comparing `hackerforms-0.8.0/hackerforms/generated/response_types.py` & `hackerforms-0.9.0/hackerforms/generated/response_types.py`

 * *Files identical despite different names*

### Comparing `hackerforms-0.8.0/hackerforms/socket.py` & `hackerforms-0.9.0/hackerforms/socket.py`

 * *Files 10% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 from .utils import serialize, deserialize
 from .parameters import set_params
 import os
 
 initialized = False
 
 
+# TODO: create_connection should have retry logic
 def initialize():
     global ws, initialized
     initialized = True
     session_id = os.environ.get("SESSION_ID")
     # ws_host = os.environ.get('WS_HOST', 'ws://localhost:8080')
     ws_host = os.environ.get("WS_HOST", "wss://hackerforms-broker.abstra.cloud")
 
@@ -40,24 +41,28 @@
         return
     ws.send(serialize(data))
 
 
 def receive(path: str = ""):
     if not initialized:
         return
-    data = deserialize(ws.recv())
+
+    recvd = ws.recv()
+    if not recvd:
+        raise Exception("Websocket not connected")
+    data = deserialize(recvd)
 
     if not path:
         return data
     return data.get(path, None)
 
 
 @atexit.register
 def close():
-    if not initialized:
+    if not initialized or ws is None or not ws.connected:
         return
     send(
         {
             "type": "program:end",
             "exitCode": hooks.exit_code,
             "exception": hooks.exception,
         }
```

### Comparing `hackerforms-0.8.0/hackerforms.egg-info/PKG-INFO` & `hackerforms-0.9.0/hackerforms.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hackerforms
-Version: 0.8.0
+Version: 0.9.0
 Summary: Hacker Forms
 Home-page: https://github.com/abstra-app/hackerforms-lib
 License: MIT
 Description: # Hackerforms
         Launch interactive Python scripts as beautiful form-like apps
         
         [Try it now on Abstra Cloud](https://www.abstracloud.com/forms)
```

### Comparing `hackerforms-0.8.0/hackerforms.egg-info/SOURCES.txt` & `hackerforms-0.9.0/hackerforms.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 README.md
 setup.py
 hackerforms/__init__.py
 hackerforms/auth.py
 hackerforms/exit_hook.py
-hackerforms/input.py
+hackerforms/overloads.py
 hackerforms/parameters.py
 hackerforms/socket.py
 hackerforms/stdio.py
 hackerforms/utils.py
 hackerforms.egg-info/PKG-INFO
 hackerforms.egg-info/SOURCES.txt
 hackerforms.egg-info/dependency_links.txt
```

### Comparing `hackerforms-0.8.0/setup.py` & `hackerforms-0.9.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 import re
 import pathlib
 from setuptools import setup
 
 regex = "^v(\d+\.\d+\.\d+)$"
-TAG = os.getenv("TAG")
+TAG = os.getenv("TAG", "v0.0.0")
 if not TAG or not re.search(regex, TAG):
     raise ValueError("TAG enviroment variable must be in the format v1.2.3")
 version = re.search(regex, TAG).group(1)
 
 # The directory containing this file
 HERE = pathlib.Path(__file__).parent
```

