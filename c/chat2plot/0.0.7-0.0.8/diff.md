# Comparing `tmp/chat2plot-0.0.7.tar.gz` & `tmp/chat2plot-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chat2plot-0.0.7.tar", last modified: Sat May 13 08:08:42 2023, max compression
+gzip compressed data, was "chat2plot-0.0.8.tar", last modified: Sat May 13 17:29:07 2023, max compression
```

## Comparing `chat2plot-0.0.7.tar` & `chat2plot-0.0.8.tar`

### file list

```diff
@@ -1,28 +1,28 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:08:42.642337 chat2plot-0.0.7/
--rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-05-13 08:08:21.000000 chat2plot-0.0.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 08:08:21.000000 chat2plot-0.0.7/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-13 08:08:42.642337 chat2plot-0.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1938 2023-05-13 08:08:21.000000 chat2plot-0.0.7/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:08:42.642337 chat2plot-0.0.7/chat2plot/
--rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8685 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/chat2plot.py
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/dataset_description.py
--rw-r--r--   0 runner    (1001) docker     (123)     1283 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/dictionary_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)     2561 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/prompt.py
--rw-r--r--   0 runner    (1001) docker     (123)     5217 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/render.py
--rw-r--r--   0 runner    (1001) docker     (123)     7783 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     1730 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/transform.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 08:08:21.000000 chat2plot-0.0.7/chat2plot/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:08:42.642337 chat2plot-0.0.7/chat2plot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-05-13 08:08:42.000000 chat2plot-0.0.7/chat2plot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-13 08:08:42.000000 chat2plot-0.0.7/chat2plot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:08:42.000000 chat2plot-0.0.7/chat2plot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:08:42.000000 chat2plot-0.0.7/chat2plot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 08:08:42.000000 chat2plot-0.0.7/chat2plot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-13 08:08:21.000000 chat2plot-0.0.7/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:08:21.000000 chat2plot-0.0.7/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      710 2023-05-13 08:08:42.646338 chat2plot-0.0.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1300 2023-05-13 08:08:21.000000 chat2plot-0.0.7/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:08:42.642337 chat2plot-0.0.7/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:08:21.000000 chat2plot-0.0.7/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 08:08:21.000000 chat2plot-0.0.7/tests/test_schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:29:07.494147 chat2plot-0.0.8/
+-rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-05-13 17:28:55.000000 chat2plot-0.0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 17:28:55.000000 chat2plot-0.0.8/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2417 2023-05-13 17:29:07.494147 chat2plot-0.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1961 2023-05-13 17:28:55.000000 chat2plot-0.0.8/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:29:07.494147 chat2plot-0.0.8/chat2plot/
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8737 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/chat2plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/dataset_description.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1283 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/dictionary_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2560 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/prompt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6062 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/render.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7850 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 17:28:55.000000 chat2plot-0.0.8/chat2plot/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:29:07.494147 chat2plot-0.0.8/chat2plot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2417 2023-05-13 17:29:07.000000 chat2plot-0.0.8/chat2plot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-13 17:29:07.000000 chat2plot-0.0.8/chat2plot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:29:07.000000 chat2plot-0.0.8/chat2plot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 17:29:07.000000 chat2plot-0.0.8/chat2plot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 17:29:07.000000 chat2plot-0.0.8/chat2plot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-13 17:28:55.000000 chat2plot-0.0.8/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 17:28:55.000000 chat2plot-0.0.8/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      710 2023-05-13 17:29:07.494147 chat2plot-0.0.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1300 2023-05-13 17:28:55.000000 chat2plot-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:29:07.494147 chat2plot-0.0.8/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:28:55.000000 chat2plot-0.0.8/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 17:28:55.000000 chat2plot-0.0.8/tests/test_schema.py
```

### Comparing `chat2plot-0.0.7/LICENSE` & `chat2plot-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.7/PKG-INFO` & `chat2plot-0.0.8/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chat2plot
-Version: 0.0.7
+Version: 0.0.8
 Summary: chat to visualization with LLM
 Home-page: https://github.com/nyanp/chat2plot
 Author: nyanp
 Author-email: Noumi.Taiga@gmail.com
 License: MIT
 Keywords: llm visualization chart gpt
 Classifier: License :: OSI Approved :: MIT License
@@ -15,14 +15,16 @@
 
 # 📈 Chat2Plot - interactive text-to-visualization with LLM
 
 Chat2plot is a project that provides visualizations based on chat instructions for given data.
 
 demo: https://chat2plot-sample.streamlit.app/
 
+![sample](sample.png)
+
 ## Usage
 
 ```Python
 import os
 import pandas as pd
 from chat2plot import chat2plot
```

### Comparing `chat2plot-0.0.7/README.md` & `chat2plot-0.0.8/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 # 📈 Chat2Plot - interactive text-to-visualization with LLM
 
 Chat2plot is a project that provides visualizations based on chat instructions for given data.
 
 demo: https://chat2plot-sample.streamlit.app/
 
+![sample](sample.png)
+
 ## Usage
 
 ```Python
 import os
 import pandas as pd
 from chat2plot import chat2plot
```

### Comparing `chat2plot-0.0.7/chat2plot/chat2plot.py` & `chat2plot-0.0.8/chat2plot/chat2plot.py`

 * *Files 2% similar despite different names*

```diff
@@ -147,14 +147,15 @@
 
     def _parse_response(self, content: str, config_only: bool, show_plot: bool) -> Plot:
         explanation, json_data = parse_json(content)
 
         try:
             config = PlotConfig.from_json(json_data)
         except Exception:
+            _logger.warning(traceback.format_exc())
             # To reduce the number of failure cases as much as possible,
             # only check against the json schema when instantiation fails.
             jsonschema.validate(json_data, PlotConfig.schema())
             raise
 
         if self._verbose:
             _logger.info(config)
```

### Comparing `chat2plot-0.0.7/chat2plot/dictionary_helper.py` & `chat2plot-0.0.8/chat2plot/dictionary_helper.py`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.7/chat2plot/prompt.py` & `chat2plot-0.0.8/chat2plot/prompt.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
     """
     )
 
 
 def _task_definition_part(model_type: str) -> str:
     if model_type == "simple":
         schema_json = json.dumps(
-            get_schema_of_chart_config(inlining_refs=False, remove_title=True), indent=2
+            get_schema_of_chart_config(inlining_refs=True, remove_title=True), indent=2
         )
 
         return (
             dedent(
                 """
             Your task is to generate chart configuration for the given dataset and user question delimited by <>.
             Responses should be in JSON format compliant to the following JSON Schema.
```

### Comparing `chat2plot-0.0.7/chat2plot/render.py` & `chat2plot-0.0.8/chat2plot/render.py`

 * *Files 19% similar despite different names*

```diff
@@ -2,14 +2,16 @@
 from typing import Any
 
 import altair as alt
 import pandas as pd
 import plotly.express as px
 import vegafusion as vf
 from altair.utils.data import to_values
+from pandas.api.types import is_integer_dtype
+from pandas.core.groupby.generic import DataFrameGroupBy
 from plotly.graph_objs import Figure
 
 from chat2plot.schema import (
     AggregationType,
     BarMode,
     ChartType,
     Filter,
@@ -71,15 +73,17 @@
         fig = px.pie(agg, names=agg.columns[0], values=agg.columns[-1])
     elif chart_type in [ChartType.LINE, ChartType.AREA]:
         func_table = {ChartType.LINE: px.line, ChartType.AREA: px.area}
 
         if is_aggregation(config):
             agg = groupby_agg(df_filtered, config)
             fig = func_table[chart_type](
-                agg, **_ax_config(config, agg.columns[0], y=agg.columns[-1])
+                agg,
+                color=config.color or None,
+                **_ax_config(config, agg.columns[0], y=agg.columns[-1]),
             )
         else:
             assert config.x is not None
             fig = func_table[chart_type](
                 df_filtered,
                 color=config.color or None,
                 **_ax_config(config, config.x.column, config.y.column),
@@ -106,14 +110,28 @@
     chart = alt.Chart.from_dict(spec)
     if show:
         chart.show()
 
     return chart
 
 
+def _is_datetime_like_column(s: pd.Series) -> bool:
+    if is_integer_dtype(s):
+        return False
+    try:
+        pd.to_datetime(s)
+        return True
+    except Exception:
+        try:
+            pd.to_datetime(s, dayfirst=True)
+            return True
+        except Exception:
+            return False
+
+
 def groupby_agg(df: pd.DataFrame, config: PlotConfig) -> pd.DataFrame:
     group_by = [config.x.column] if config.x is not None else []
 
     if config.color and (not config.x or (config.color != config.x.column)):
         group_by.append(config.color)
 
     agg_method = {
@@ -124,30 +142,36 @@
         AggregationType.MIN: "min",
         AggregationType.MAX: "max",
     }
 
     y = config.y
     aggregation = y.aggregation or AggregationType.AVG
 
+    if config.x and config.x.column and _is_datetime_like_column(df[config.x.column]):
+        df = df.copy()
+        df[config.x.column] = pd.to_datetime(df[config.x.column])
+
+    def _apply_agg(
+        aggregation: AggregationType, df: pd.DataFrame | DataFrameGroupBy
+    ) -> Any:
+        if aggregation == AggregationType.COUNTROWS:
+            return len(df) if isinstance(df, pd.DataFrame) else df.size()
+        else:
+            return df[y.column].agg(agg_method[aggregation])
+
     if not group_by:
-        return pd.DataFrame(
-            {y.transformed_name(): [df[y.column].agg(agg_method[aggregation])]}
-        )
+        return pd.DataFrame({y.transformed_name(): [_apply_agg(aggregation, df)]})
     else:
-        agg = (
-            df.groupby(group_by, dropna=False)[y.column]
-            .agg(agg_method[aggregation])
-            .rename(y.transformed_name())
-        )
+        agg = _apply_agg(aggregation, df.groupby(group_by, dropna=False)).rename(y.transformed_name())  # type: ignore
         ascending = config.sort_order == SortOrder.ASC
 
-        if config.sort_criteria == SortingCriteria.NAME:
-            agg = agg.sort_index(ascending=ascending)
-        elif config.sort_criteria == SortingCriteria.VALUE:
+        if config.sort_criteria == SortingCriteria.VALUE:
             agg = agg.sort_values(ascending=ascending)
+        else:
+            agg = agg.sort_index(ascending=ascending, level=0)
 
         return agg.reset_index()
 
 
 def is_aggregation(config: PlotConfig) -> bool:
     return config.y.aggregation is not None
```

### Comparing `chat2plot-0.0.7/chat2plot/schema.py` & `chat2plot-0.0.8/chat2plot/schema.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-import copy
 import re
 from enum import Enum
 from typing import Any
 
 import jsonref
 import pydantic
 
@@ -22,14 +21,15 @@
 
 class AggregationType(str, Enum):
     SUM = "SUM"
     AVG = "AVG"
     MIN = "MIN"
     MAX = "MAX"
     COUNT = "COUNT"
+    COUNTROWS = "COUNTROWS"
     DISTINCT_COUNT = "DISTINCT_COUNT"
 
 
 class ResponseType(str, Enum):
     SUCCESS = "success"
     UNKNOWN = "unknown"
     FAILED_TO_RENDER = "failed to render"
@@ -117,15 +117,15 @@
         )
 
 
 class YAxis(pydantic.BaseModel):
     column: str = pydantic.Field(description="column in datasets used for the y-axis")
     aggregation: AggregationType | None = pydantic.Field(
         None,
-        description=f"Type of aggregation. It will be ignored when it is scatter plot",
+        description="Type of aggregation. Required for all chart types but scatter plots.",
     )
     min_value: float | None
     max_value: float | None
     label: str | None
 
     def transformed_name(self) -> str:
         dst = self.column
@@ -137,29 +137,36 @@
     def parse_from_llm(
         cls, d: dict[str, str | float | dict[str, str]], needs_aggregation: bool = False
     ) -> "YAxis":
         agg = d.get("aggregation")
         if needs_aggregation and not agg:
             agg = "AVG"
 
+        if not d.get("column") and needs_aggregation:
+            agg = "COUNTROWS"
+        elif agg == "COUNTROWS":
+            agg = "COUNT"
+
         return YAxis(
-            column=d.get("column") or None,  # type: ignore
+            column=d.get("column") or "",  # type: ignore
             aggregation=AggregationType(agg) if agg else None,
-            transform=Transform.parse_from_llm(d["transform"]) if "transform" in d else None,  # type: ignore
             min_value=d.get("min_value"),  # type: ignore
             max_value=d.get("max_value"),  # type: ignore
             label=d.get("label") or None,  # type: ignore
         )
 
 
 class PlotConfig(pydantic.BaseModel):
-    chart_type: ChartType = pydantic.Field(description="the type of the chart")
+    chart_type: ChartType = pydantic.Field(
+        description="The type of the chart. Use scatter plots as little as possible unless explicitly specified by the user."
+    )
     filters: list[str] = pydantic.Field(
         description="List of filter conditions, where each filter must be a legal string that can be passed to df.query(),"
-        ' such as "x >= 0". Filters will be calculated before transforming axis.',
+        ' such as "x >= 0". Filters are calculated before transforming axes.　'
+        "When using AVG on the y-axis, do not filter the same column to a specific single value.",
     )
     x: XAxis | None = pydantic.Field(
         None, description="X-axis for the chart, or label column for pie chart"
     )
     y: YAxis = pydantic.Field(
         description="Y-axis or measure value for the chart, or the wedge sizes for pie chart.",
     )
@@ -177,21 +184,14 @@
     sort_order: SortOrder | None = pydantic.Field(
         None, description="Sorting order for x-axis"
     )
     horizontal: bool | None = pydantic.Field(
         None, description="If true, the chart is drawn in a horizontal orientation"
     )
 
-    @property
-    def required_columns(self) -> list[str]:
-        columns = [self.y.column]
-        if self.x:
-            columns.append(self.x.column)
-        return columns
-
     @classmethod
     def from_json(cls, json_data: dict[str, Any]) -> "PlotConfig":
         assert "chart_type" in json_data
         assert "y" in json_data
 
         def wrap_if_not_list(value: str | list[str]) -> list[str]:
             if not isinstance(value, list):
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `chat2plot-0.0.7/chat2plot/transform.py` & `chat2plot-0.0.8/chat2plot/transform.py`

 * *Files 3% similar despite different names*

```diff
@@ -44,15 +44,18 @@
 
 
 def round_datetime(series: pd.Series, period: TimeUnit) -> pd.Series:
     if is_integer_dtype(series) and period == TimeUnit.YEAR:
         # assuming that it is year column, so no transform is needed
         return series
 
-    series = pd.to_datetime(series)
+    try:
+        series = pd.to_datetime(series)
+    except Exception:
+        series = pd.to_datetime(series, dayfirst=True)
 
     period_map = {
         TimeUnit.DAY: "D",
         TimeUnit.WEEK: "W",
         TimeUnit.MONTH: "M",
         TimeUnit.QUARTER: "Q",
         TimeUnit.YEAR: "Y",
```

### Comparing `chat2plot-0.0.7/chat2plot.egg-info/PKG-INFO` & `chat2plot-0.0.8/chat2plot.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chat2plot
-Version: 0.0.7
+Version: 0.0.8
 Summary: chat to visualization with LLM
 Home-page: https://github.com/nyanp/chat2plot
 Author: nyanp
 Author-email: Noumi.Taiga@gmail.com
 License: MIT
 Keywords: llm visualization chart gpt
 Classifier: License :: OSI Approved :: MIT License
@@ -15,14 +15,16 @@
 
 # 📈 Chat2Plot - interactive text-to-visualization with LLM
 
 Chat2plot is a project that provides visualizations based on chat instructions for given data.
 
 demo: https://chat2plot-sample.streamlit.app/
 
+![sample](sample.png)
+
 ## Usage
 
 ```Python
 import os
 import pandas as pd
 from chat2plot import chat2plot
```

### Comparing `chat2plot-0.0.7/setup.cfg` & `chat2plot-0.0.8/setup.cfg`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.7/setup.py` & `chat2plot-0.0.8/setup.py`

 * *Files identical despite different names*

### Comparing `chat2plot-0.0.7/tests/test_schema.py` & `chat2plot-0.0.8/tests/test_schema.py`

 * *Files identical despite different names*

