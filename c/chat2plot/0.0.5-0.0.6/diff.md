# Comparing `tmp/chat2plot-0.0.5.tar.gz` & `tmp/chat2plot-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chat2plot-0.0.5.tar", last modified: Wed May 10 14:39:51 2023, max compression
+gzip compressed data, was "chat2plot-0.0.6.tar", last modified: Fri May 12 14:26:25 2023, max compression
```

## Comparing `chat2plot-0.0.5.tar` & `chat2plot-0.0.6.tar`

### file list

```diff
@@ -1,28 +1,28 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 14:39:51.077373 chat2plot-0.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-05-10 14:39:35.000000 chat2plot-0.0.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-10 14:39:35.000000 chat2plot-0.0.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-10 14:39:51.077373 chat2plot-0.0.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1938 2023-05-10 14:39:35.000000 chat2plot-0.0.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 14:39:51.073373 chat2plot-0.0.5/chat2plot/
--rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7992 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/chat2plot.py
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/dataset_description.py
--rw-r--r--   0 runner    (1001) docker     (123)     1294 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/dictionary_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/prompt.py
--rw-r--r--   0 runner    (1001) docker     (123)     4619 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/render.py
--rw-r--r--   0 runner    (1001) docker     (123)     6794 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     2368 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/transform.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-10 14:39:35.000000 chat2plot-0.0.5/chat2plot/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 14:39:51.077373 chat2plot-0.0.5/chat2plot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-10 14:39:51.000000 chat2plot-0.0.5/chat2plot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-10 14:39:51.000000 chat2plot-0.0.5/chat2plot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 14:39:51.000000 chat2plot-0.0.5/chat2plot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-10 14:39:51.000000 chat2plot-0.0.5/chat2plot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-10 14:39:51.000000 chat2plot-0.0.5/chat2plot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-10 14:39:35.000000 chat2plot-0.0.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-10 14:39:35.000000 chat2plot-0.0.5/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      710 2023-05-10 14:39:51.077373 chat2plot-0.0.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1300 2023-05-10 14:39:35.000000 chat2plot-0.0.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 14:39:51.077373 chat2plot-0.0.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 14:39:35.000000 chat2plot-0.0.5/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-10 14:39:35.000000 chat2plot-0.0.5/tests/test_schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 14:26:25.075667 chat2plot-0.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-05-12 14:26:10.000000 chat2plot-0.0.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-12 14:26:10.000000 chat2plot-0.0.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-12 14:26:25.075667 chat2plot-0.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1938 2023-05-12 14:26:10.000000 chat2plot-0.0.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 14:26:25.071667 chat2plot-0.0.6/chat2plot/
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8300 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/chat2plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/dataset_description.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1283 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/dictionary_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2576 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/prompt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5398 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/render.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6847 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1894 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-12 14:26:10.000000 chat2plot-0.0.6/chat2plot/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 14:26:25.071667 chat2plot-0.0.6/chat2plot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-12 14:26:25.000000 chat2plot-0.0.6/chat2plot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-12 14:26:25.000000 chat2plot-0.0.6/chat2plot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 14:26:25.000000 chat2plot-0.0.6/chat2plot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-12 14:26:25.000000 chat2plot-0.0.6/chat2plot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 14:26:25.000000 chat2plot-0.0.6/chat2plot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-12 14:26:10.000000 chat2plot-0.0.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-12 14:26:10.000000 chat2plot-0.0.6/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      710 2023-05-12 14:26:25.075667 chat2plot-0.0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1300 2023-05-12 14:26:10.000000 chat2plot-0.0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 14:26:25.075667 chat2plot-0.0.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 14:26:10.000000 chat2plot-0.0.6/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-12 14:26:10.000000 chat2plot-0.0.6/tests/test_schema.py
```

### Comparing `chat2plot-0.0.5/LICENSE` & `chat2plot-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.5/PKG-INFO` & `chat2plot-0.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chat2plot
-Version: 0.0.5
+Version: 0.0.6
 Summary: chat to visualization with LLM
 Home-page: https://github.com/nyanp/chat2plot
 Author: nyanp
 Author-email: Noumi.Taiga@gmail.com
 License: MIT
 Keywords: llm visualization chart gpt
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `chat2plot-0.0.5/README.md` & `chat2plot-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.5/chat2plot/chat2plot.py` & `chat2plot-0.0.6/chat2plot/chat2plot.py`

 * *Files 4% similar despite different names*

```diff
@@ -90,15 +90,15 @@
         return self.query(q, config_only, show_plot)
 
 
 class Chat2Plot(Chat2PlotBase):
     def __init__(
         self, df: pd.DataFrame, chat: BaseChatModel | None = None, verbose: bool = False
     ):
-        self._session = ChatSession(df, system_prompt("default"), "<{text}>", chat)
+        self._session = ChatSession(df, system_prompt("simple"), "<{text}>", chat)
         self._df = df
         self._verbose = verbose
 
     @property
     def session(self) -> ChatSession:
         return self._session
 
@@ -109,15 +109,15 @@
             return self._parse_response(raw_response, config_only, show_plot)
         except Exception as e:
             if self._verbose:
                 _logger.info(f"first response: {raw_response}")
                 _logger.warning(traceback.format_exc())
 
             msg = e.message if isinstance(e, jsonschema.ValidationError) else str(e)
-            error_correction = error_correction_prompt("default").format(
+            error_correction = error_correction_prompt("simple").format(
                 dataset=description(self._df),
                 question=q,
                 response=raw_response,
                 error_message=msg,
             )
             corrected_response = self._session.query_without_history(error_correction)
             if self._verbose:
@@ -202,30 +202,44 @@
         self, q: str, config_only: bool = False, show_plot: bool = False
     ) -> Plot:
         return self.query(q, config_only, show_plot)
 
 
 def chat2plot(
     df: pd.DataFrame,
-    model_type: str = "default",
+    model_type: str = "simple",
     chat: BaseChatModel | None = None,
     verbose: bool = False,
 ) -> Chat2PlotBase:
-    if model_type == "default":
+    if model_type == "simple":
         return Chat2Plot(df, chat, verbose)
     elif model_type == "vega":
         return Chat2Vega(df, chat, verbose)
     else:
         raise ValueError(
             f"model_type should be one of [default, vega] (given: {model_type})"
         )
 
 
-def parse_json(content: str) -> tuple[str, dict[str, Any]]:
-    ptn = r"```json(.*)```" if "```json" in content else r"```(.*)```"
-    s = re.search(ptn, content, re.MULTILINE | re.DOTALL)
-    if s:
-        json_part = json.loads(s.group(1))  # type: ignore
-        non_json_part = content.replace(s.group(0), "")
-        return non_json_part, delete_null_field(json_part)
+def _extract_tag_content(s: str, tag: str) -> str:
+    m = re.search(fr"<{tag}>(.*)</{tag}>", s, re.MULTILINE | re.DOTALL)
+    if m:
+        return m.group(1)
     else:
-        raise ValueError("failed to find start(```) and end(```) marker.")
+        m = re.search(fr"<{tag}>(.*)<{tag}>", s, re.MULTILINE | re.DOTALL)
+        if m:
+            return m.group(1)
+    return ""
+
+
+def parse_json(content: str) -> tuple[str, dict[str, Any]]:
+
+    json_part = _extract_tag_content(content, "json")  # type: ignore
+    if not json_part:
+        raise ValueError("failed to find <json> and </json> tags")
+
+    explanation_part = _extract_tag_content(content, "explain")
+    if not explanation_part:
+        explanation_part = _extract_tag_content(content, "explanation")
+
+    return explanation_part.strip(), delete_null_field(json.loads(json_part))
+
```

### Comparing `chat2plot-0.0.5/chat2plot/dictionary_helper.py` & `chat2plot-0.0.6/chat2plot/dictionary_helper.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,8 @@
-from typing import Any, Callable
-
+from typing import Any
 
 
 def remove_field_recursively(d: Any, field: str) -> Any:
     if isinstance(d, dict):
         if field in d:
             del d[field]
         for k in d.keys():
```

### Comparing `chat2plot-0.0.5/chat2plot/prompt.py` & `chat2plot-0.0.6/chat2plot/prompt.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,37 +1,35 @@
 import json
 from textwrap import dedent
 
 from chat2plot.schema import get_schema_of_chart_config
 
 
-def system_prompt(model_type: str = "default") -> str:
+def system_prompt(model_type: str = "simple") -> str:
     return _task_definition_part(model_type) + "\n" + _data_and_detailed_instruction_part()
 
 
-def error_correction_prompt(model_type: str = "default") -> str:
+def error_correction_prompt(model_type: str = "simple") -> str:
     return system_prompt(model_type) + dedent("""
         The user asked the following question:
         {question}
         
         Your response:
-        ```
         {response}
-        ```
         
         It fails with the following error:
         {error_message}
         
-        Correct the json and return a new json (do not import anything) that fixes the above mentioned error.
+        Correct the json and return a new explanation and json that fixes the above mentioned error.
         Do not generate the same json again.
     """)
 
 
 def _task_definition_part(model_type: str) -> str:
-    if model_type == "default":
+    if model_type == "simple":
         schema_json = json.dumps(get_schema_of_chart_config(inlining_refs=False, remove_title=True), indent=2)
 
         return dedent("""
             Your task is to generate chart configuration for the given dataset and user question delimited by <>.
             Responses should be in JSON format compliant to the following JSON Schema.
 
             """) + schema_json.replace("{", "{{").replace("}", "}}")
@@ -51,11 +49,12 @@
         This is the result of `print(df.head())`:
         
         {dataset}
         
         You should do the following step by step, and your response should include both 1 and 2:
         1. Explain whether filters should be applied to the data, which chart_type and columns should be used, and what transformations are necessary to fulfill the user's request.
            Answers should be in the same language as the user and be understandable to someone who does not know the JSON schema definition.
+           This text should be enclosed with <explain> and </explain> tag.
         2. Generate schema-compliant JSON that represents 1.
-        
-        Make sure to prefix the requested json string with triple backticks exactly and suffix the json with triple backticks exactly.
+           This text should be enclosed with <json> and </json> tag.
+
         """)
```

### Comparing `chat2plot-0.0.5/chat2plot/schema.py` & `chat2plot-0.0.6/chat2plot/schema.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,18 @@
+import copy
 import re
 from enum import Enum
-from typing import Any, Type
+from typing import Any
 
 import jsonref
 import pydantic
 
 from chat2plot.dictionary_helper import remove_field_recursively, flatten_single_element_allof
 
 
-class SchemaWithoutTitle:
-    @staticmethod
-    def schema_extra(schema: dict[str, Any], _: Type[Any]) -> None:
-        for prop in schema.get("properties", {}).values():
-            prop.pop("title", None)
-
-
 class ChartType(str, Enum):
     PIE = "pie"
     SCATTER = "scatter"
     LINE = "line"
     BAR = "bar"
     AREA = "area"
     HORIZONTAL_BAR = "horizontal-bar"
@@ -54,14 +48,20 @@
     YEAR= "year"
     MONTH = "month"
     WEEK = "week"
     QUARTER = "quarter"
     DAY = "day"
 
 
+class BarMode(str, Enum):
+    STACK = "stacked"
+    GROUP = "group"
+
+
+
 class Transform(pydantic.BaseModel):
     aggregation: AggregationType | None = pydantic.Field(
         None,
         description=f"Type of aggregation. It will be ignored when it is scatter plot",
     )
     bin_size: int | None = pydantic.Field(
         None,
@@ -88,26 +88,20 @@
             aggregation=AggregationType(d["aggregation"].upper())
             if d.get("aggregation")
             else None,
             bin_size=d.get("bin_size") or None,
             time_unit=d.get("time_unit") or None
         )
 
-    class Config(SchemaWithoutTitle):
-        pass
-
 
 class Filter(pydantic.BaseModel):
     lhs: str
     rhs: str
     op: str
 
-    class Config(SchemaWithoutTitle):
-        pass
-
     def escaped(self) -> str:
         lhs = f"`{self.lhs}`" if self.lhs[0] != "`" else self.lhs
         return f"{lhs} {self.op} {self.rhs}"
 
     @classmethod
     def parse_from_llm(cls, f: str) -> "Filter":
         f = f.strip()
@@ -122,64 +116,66 @@
                 rhs = m.group(2).strip()
                 return Filter(lhs=lhs, rhs=rhs, op=op)
 
         raise ValueError(f"Unsupported op or failed to parse: {f}")
 
 
 class Axis(pydantic.BaseModel):
-    column: str = pydantic.Field(None, description="column in datasets used for the axis")
-    transform: Transform | None = pydantic.Field(None, description="transformation applied to column")
+    column: str = pydantic.Field(description="column in datasets used for the axis")
+    transform: Transform = pydantic.Field(None, description="transformation applied to column")
     min_value: float | None
     max_value: float | None
     label: str | None
 
     def transformed_name(self):
         return self.transform.transformed_name(self.column) if self.transform else self.column
 
-    class Config(SchemaWithoutTitle):
-        pass
-
     @classmethod
     def parse_from_llm(cls, d: dict[str, str | float | dict[str, str]]) -> "Axis":
         return Axis(
             column=d.get("column") or None,
             transform=Transform.parse_from_llm(d["transform"]) if "transform" in d else None,  # type: ignore
             min_value=d.get("min_value"),  # type: ignore
             max_value=d.get("max_value"),  # type: ignore
             label=d.get("label") or None,  # type: ignore
         )
 
 
 class PlotConfig(pydantic.BaseModel):
-    chart_type: ChartType = pydantic.Field(None, description="the type of the chart")
+    chart_type: ChartType = pydantic.Field(description="the type of the chart")
     filters: list[str] = pydantic.Field(
-        None,
         description="List of filter conditions, where each filter must be a legal string that can be passed to df.query(),"
         ' such as "x >= 0". Filters will be calculated before transforming axis.',
     )
     x: Axis | None = pydantic.Field(
         None, description="X-axis for the chart, or label column for pie chart"
     )
     y: Axis = pydantic.Field(
-        None,
         description="Y-axis or measure value for the chart, or the wedge sizes for pie chart.",
     )
-    hue: str | None = pydantic.Field(
+    color: str | None = pydantic.Field(
         None,
         description="Column name used as grouping variables that will produce different colors.",
     )
+    bar_mode: BarMode | None = pydantic.Field(
+        None,
+        description="If 'stacked', bars are stacked. In 'group' mode, bars are placed beside each other."
+    )
     sort_criteria: SortingCriteria | None = pydantic.Field(
         None, description="The sorting criteria for x-axis"
     )
     sort_order: SortOrder | None = pydantic.Field(
         None, description="Sorting order for x-axis"
     )
 
-    class Config(SchemaWithoutTitle):
-        pass
+    def transpose(self) -> "PlotConfig":
+        transposed = copy.deepcopy(self)
+        transposed.y = self.x
+        transposed.x = self.y
+        return transposed
 
     @property
     def required_columns(self) -> list[str]:
         columns = [self.y.column]
         if self.x:
             columns.append(self.x.column)
         return columns
@@ -198,15 +194,16 @@
         chart_type = ChartType(json_data["chart_type"])
 
         return cls(
             chart_type=chart_type,
             x=Axis.parse_from_llm(json_data["x"]) if json_data.get("x") else None,
             y=Axis.parse_from_llm(json_data["y"]),
             filters=wrap_if_not_list(json_data.get("filters", [])),
-            hue=json_data.get("hue") or None,
+            color=json_data.get("color") or None,
+            bar_mode=BarMode(json_data["bar_mode"]) if json_data.get("bar_mode") else None,
             sort_criteria=SortingCriteria(json_data["sort_criteria"])
             if json_data.get("sort_criteria")
             else None,
             sort_order=SortOrder(json_data["sort_order"])
             if json_data.get("sort_order")
             else None,
         )
```

### Comparing `chat2plot-0.0.5/chat2plot/transform.py` & `chat2plot-0.0.6/chat2plot/transform.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,25 +1,19 @@
 import copy
-import re
-
 
 import numpy as np
 import pandas as pd
 from pandas.api.types import is_integer_dtype
 
 from chat2plot.schema import PlotConfig, Axis, TimeUnit
 
 
 def transform(df: pd.DataFrame, config: PlotConfig) -> tuple[pd.DataFrame, PlotConfig]:
     config = copy.deepcopy(config)
 
-    for col in config.required_columns:
-        if col not in df:
-            df[col] = transform_one(df, col, config)
-
     if config.x and config.x.transform:
         x_trans = _transform(df, config.x)
         df[x_trans.name] = x_trans
         config.x.column = x_trans.name
 
     if config.y.transform:
         y_trans = _transform(df, config.y)
@@ -40,41 +34,29 @@
 
     if ax.transform.time_unit:
         dst = round_datetime(dst, ax.transform.time_unit)
 
     return pd.Series(dst.values, name=ax.transformed_name())
 
 
-def transform_one(df: pd.DataFrame, col: str, config: PlotConfig) -> pd.Series:
-    m = re.match(r"BINNING\((.*),(.*)\)", col)
-    if m:
-        col = m.group(1).strip()
-        interval = int(m.group(2).strip())
-        return binning(df[col], interval)
-
-    m = re.match(r"ROUND_DATETIME\((.*),(.*)\)", col)
-    if m:
-        col = m.group(1).strip()
-        period = m.group(2).strip()
-        return round_datetime(df[col], period)
-
-    raise ValueError(f"Unknown column transform: {col}")
-
-
 def binning(series: pd.Series, interval: int) -> pd.Series:
     start_point = np.floor(series.min() / interval) * interval
     end_point = np.ceil((series.max() + 1) / interval) * interval
     bins = pd.interval_range(
         start=start_point,
         end=end_point,
         freq=interval,
         closed="both" if is_integer_dtype(series) else "left",
     )
     binned_series = pd.cut(series, bins=bins)
     return binned_series.astype(str)
 
 
 def round_datetime(series: pd.Series, period: TimeUnit) -> pd.Series:
+    if is_integer_dtype(series) and period == TimeUnit.YEAR:
+        # assuming that it is year column, so no transform is needed
+        return series
+
     series = pd.to_datetime(series)
 
     period_map = {TimeUnit.DAY: "D", TimeUnit.WEEK: "W", TimeUnit.MONTH: "M", TimeUnit.QUARTER: "Q", TimeUnit.YEAR: "Y"}
     return series.dt.to_period(period_map.get(period, period)).dt.to_timestamp()
```

### Comparing `chat2plot-0.0.5/chat2plot.egg-info/PKG-INFO` & `chat2plot-0.0.6/chat2plot.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chat2plot
-Version: 0.0.5
+Version: 0.0.6
 Summary: chat to visualization with LLM
 Home-page: https://github.com/nyanp/chat2plot
 Author: nyanp
 Author-email: Noumi.Taiga@gmail.com
 License: MIT
 Keywords: llm visualization chart gpt
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `chat2plot-0.0.5/setup.cfg` & `chat2plot-0.0.6/setup.cfg`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.5/setup.py` & `chat2plot-0.0.6/setup.py`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.5/tests/test_schema.py` & `chat2plot-0.0.6/tests/test_schema.py`

 * *Files identical despite different names*

