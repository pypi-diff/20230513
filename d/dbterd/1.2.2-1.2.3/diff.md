# Comparing `tmp/dbterd-1.2.2.tar.gz` & `tmp/dbterd-1.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dbterd-1.2.2.tar", max compression
+gzip compressed data, was "dbterd-1.2.3.tar", max compression
```

## Comparing `dbterd-1.2.2.tar` & `dbterd-1.2.3.tar`

### file list

```diff
@@ -1,41 +1,41 @@
--rw-r--r--   0        0        0      203 2023-05-13 06:09:43.232289 dbterd-1.2.2/LICENSE
--rw-r--r--   0        0        0     3217 2023-05-13 06:09:43.232289 dbterd-1.2.2/README.md
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/__init__.py
--rw-r--r--   0        0        0       37 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/__main__.py
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/__init__.py
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/__init__.py
--rw-r--r--   0        0        0     4801 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/base.py
--rw-r--r--   0        0        0     3157 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/filter.py
--rw-r--r--   0        0        0      592 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/meta.py
--rw-r--r--   0        0        0     5658 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/test_relationship.py
--rw-r--r--   0        0        0     2575 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/base.py
--rw-r--r--   0        0        0      560 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/factory.py
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/__init__.py
--rw-r--r--   0        0        0      306 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/constants.py
--rw-r--r--   0        0        0      296 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/d2/__init__.py
--rw-r--r--   0        0        0     1591 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/d2/d2_test_relationship.py
--rw-r--r--   0        0        0      304 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/dbml/__init__.py
--rw-r--r--   0        0        0     2167 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/dbml/dbml_test_relationship.py
--rw-r--r--   0        0        0      168 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/default.py
--rw-r--r--   0        0        0      320 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/graphviz/__init__.py
--rw-r--r--   0        0        0     2778 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
--rw-r--r--   0        0        0      316 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/mermaid/__init__.py
--rw-r--r--   0        0        0     2162 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
--rw-r--r--   0        0        0      320 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/plantuml/__init__.py
--rw-r--r--   0        0        0     2012 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
--rw-r--r--   0        0        0      222 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/worker.py
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/__init__.py
--rw-r--r--   0        0        0     2026 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/main.py
--rw-r--r--   0        0        0     1928 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/params.py
--rw-r--r--   0        0        0      164 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/constants.py
--rw-r--r--   0        0        0      284 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/default.py
--rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/__init__.py
--rw-r--r--   0        0        0      721 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/cli_messaging.py
--rw-r--r--   0        0        0      877 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/dict.py
--rw-r--r--   0        0        0     4494 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/file.py
--rw-r--r--   0        0        0     1022 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/jsonify.py
--rw-r--r--   0        0        0      976 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/log.py
--rw-r--r--   0        0        0     1605 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/yaml.py
--rw-r--r--   0        0        0       94 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/main.py
--rw-r--r--   0        0        0     2061 2023-05-13 06:09:58.348375 dbterd-1.2.2/pyproject.toml
--rw-r--r--   0        0        0     4230 1970-01-01 00:00:00.000000 dbterd-1.2.2/PKG-INFO
+-rw-r--r--   0        0        0      203 2023-05-13 08:24:42.046913 dbterd-1.2.3/LICENSE
+-rw-r--r--   0        0        0     3217 2023-05-13 08:24:42.050913 dbterd-1.2.3/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/__init__.py
+-rw-r--r--   0        0        0       37 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/__main__.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/algos/__init__.py
+-rw-r--r--   0        0        0     4801 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/algos/base.py
+-rw-r--r--   0        0        0     3157 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/algos/filter.py
+-rw-r--r--   0        0        0      592 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/algos/meta.py
+-rw-r--r--   0        0        0     5653 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/algos/test_relationship.py
+-rw-r--r--   0        0        0     2575 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/base.py
+-rw-r--r--   0        0        0      560 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/factory.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/__init__.py
+-rw-r--r--   0        0        0      306 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/constants.py
+-rw-r--r--   0        0        0      296 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/d2/__init__.py
+-rw-r--r--   0        0        0     1591 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/d2/d2_test_relationship.py
+-rw-r--r--   0        0        0      304 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/dbml/__init__.py
+-rw-r--r--   0        0        0     2179 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/dbml/dbml_test_relationship.py
+-rw-r--r--   0        0        0      168 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/default.py
+-rw-r--r--   0        0        0      320 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/graphviz/__init__.py
+-rw-r--r--   0        0        0     2778 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
+-rw-r--r--   0        0        0      316 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/mermaid/__init__.py
+-rw-r--r--   0        0        0     2162 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
+-rw-r--r--   0        0        0      320 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/plantuml/__init__.py
+-rw-r--r--   0        0        0     2012 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
+-rw-r--r--   0        0        0      222 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/adapters/worker.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/cli/__init__.py
+-rw-r--r--   0        0        0     2026 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/cli/main.py
+-rw-r--r--   0        0        0     1928 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/cli/params.py
+-rw-r--r--   0        0        0      164 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/constants.py
+-rw-r--r--   0        0        0      284 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/default.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/__init__.py
+-rw-r--r--   0        0        0      721 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/cli_messaging.py
+-rw-r--r--   0        0        0      877 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/dict.py
+-rw-r--r--   0        0        0     4494 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/file.py
+-rw-r--r--   0        0        0     1022 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/jsonify.py
+-rw-r--r--   0        0        0      976 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/log.py
+-rw-r--r--   0        0        0     1605 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/helpers/yaml.py
+-rw-r--r--   0        0        0       94 2023-05-13 08:24:42.054913 dbterd-1.2.3/dbterd/main.py
+-rw-r--r--   0        0        0     2061 2023-05-13 08:24:55.278685 dbterd-1.2.3/pyproject.toml
+-rw-r--r--   0        0        0     4230 1970-01-01 00:00:00.000000 dbterd-1.2.3/PKG-INFO
```

### Comparing `dbterd-1.2.2/README.md` & `dbterd-1.2.3/README.md`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/algos/base.py` & `dbterd-1.2.3/dbterd/adapters/algos/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/algos/filter.py` & `dbterd-1.2.3/dbterd/adapters/algos/filter.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/algos/meta.py` & `dbterd-1.2.3/dbterd/adapters/algos/meta.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/algos/test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/algos/test_relationship.py`

 * *Files 2% similar despite different names*

```diff
@@ -148,15 +148,15 @@
 
     Args:
         test_node (dict): Manifest Test node
 
     Returns:
         list: [to model, from model]
     """
-    map = test_node.depends_on.get("nodes", [])
+    map = test_node.depends_on.nodes or []
     rule = get_algo_rule(**kwargs)
     to_model = str(test_node.test_metadata.kwargs.get(rule.get("t_to", "to"), {}))
     if f'("{map[1].split(".")[-1]}")'.lower() in to_model.replace("'", '"').lower():
         return [map[1], map[0]]
 
     return map
```

### Comparing `dbterd-1.2.2/dbterd/adapters/base.py` & `dbterd-1.2.3/dbterd/adapters/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/factory.py` & `dbterd-1.2.3/dbterd/adapters/factory.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/targets/d2/d2_test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/targets/d2/d2_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/targets/dbml/dbml_test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/targets/dbml/dbml_test_relationship.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+import json
+
 from dbterd.adapters.algos import test_relationship
 
 
 def run(manifest, catalog, **kwargs):
     """Parse dbt artifacts and export DBML file
 
     Args:
@@ -33,18 +35,18 @@
     for table in tables:
         dbml += f"//--configured at schema: {table.database}.{table.schema}\n"
         dbml += 'Table "{table}" {{\n{columns}\n}}\n'.format(
             table=table.name,
             columns="\n".join(
                 [
                     str.format(
-                        '"{0}" "{1}"{2}',
+                        '  "{0}" "{1}"{2}',
                         x.name,
                         x.data_type,
-                        str.format(" [note: {1}{0}{1}]", x.description, chr(34))
+                        str.format(" [note: {0}]", json.dumps(x.description))
                         if x.description
                         else "",
                     )
                     for x in table.columns
                 ]
             ),
         )
```

### Comparing `dbterd-1.2.2/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py` & `dbterd-1.2.3/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/cli/main.py` & `dbterd-1.2.3/dbterd/cli/main.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/cli/params.py` & `dbterd-1.2.3/dbterd/cli/params.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/cli_messaging.py` & `dbterd-1.2.3/dbterd/helpers/cli_messaging.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/dict.py` & `dbterd-1.2.3/dbterd/helpers/dict.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/file.py` & `dbterd-1.2.3/dbterd/helpers/file.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/jsonify.py` & `dbterd-1.2.3/dbterd/helpers/jsonify.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/log.py` & `dbterd-1.2.3/dbterd/helpers/log.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/dbterd/helpers/yaml.py` & `dbterd-1.2.3/dbterd/helpers/yaml.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.2/pyproject.toml` & `dbterd-1.2.3/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dbterd"
-version = "1.2.2"
+version = "1.2.3"
 description = "CLI to generate ERD Diagram file from dbt artifact files"
 authors = ["Dat Nguyen <datnguyen.it09@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/datnguye/dbterd"
 repository = "https://github.com/datnguye/dbterd"
 keywords = ["flake8", "markdown", "lint"]
```

### Comparing `dbterd-1.2.2/PKG-INFO` & `dbterd-1.2.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dbterd
-Version: 1.2.2
+Version: 1.2.3
 Summary: CLI to generate ERD Diagram file from dbt artifact files
 Home-page: https://github.com/datnguye/dbterd
 License: MIT
 Keywords: flake8,markdown,lint
 Author: Dat Nguyen
 Author-email: datnguyen.it09@gmail.com
 Requires-Python: >=3.9,<4.0
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: dbterd Version: 1.2.2 Summary: CLI to generate ERD
+Metadata-Version: 2.1 Name: dbterd Version: 1.2.3 Summary: CLI to generate ERD
 Diagram file from dbt artifact files Home-page: https://github.com/datnguye/
 dbterd License: MIT Keywords: flake8,markdown,lint Author: Dat Nguyen Author-
 email: datnguyen.it09@gmail.com Requires-Python: >=3.9,<4.0 Classifier:
 Environment :: Console Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Classifier: Programming Language
 :: Python :: 3 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Programming Language ::
```

