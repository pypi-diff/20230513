# Comparing `tmp/dbterd-1.2.1.tar.gz` & `tmp/dbterd-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dbterd-1.2.1.tar", max compression
+gzip compressed data, was "dbterd-1.2.2.tar", max compression
```

## Comparing `dbterd-1.2.1.tar` & `dbterd-1.2.2.tar`

### file list

```diff
@@ -1,41 +1,41 @@
--rw-r--r--   0        0        0      203 2023-05-13 04:22:36.666970 dbterd-1.2.1/LICENSE
--rw-r--r--   0        0        0     3217 2023-05-13 04:22:36.666970 dbterd-1.2.1/README.md
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/__init__.py
--rw-r--r--   0        0        0       37 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/__main__.py
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/__init__.py
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/__init__.py
--rw-r--r--   0        0        0     4801 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/base.py
--rw-r--r--   0        0        0     3157 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/filter.py
--rw-r--r--   0        0        0      592 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/meta.py
--rw-r--r--   0        0        0     4558 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/test_relationship.py
--rw-r--r--   0        0        0     2575 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/base.py
--rw-r--r--   0        0        0      560 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/factory.py
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/__init__.py
--rw-r--r--   0        0        0      306 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/constants.py
--rw-r--r--   0        0        0      296 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/d2/__init__.py
--rw-r--r--   0        0        0     1591 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/d2/d2_test_relationship.py
--rw-r--r--   0        0        0      304 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/dbml/__init__.py
--rw-r--r--   0        0        0     2167 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/dbml/dbml_test_relationship.py
--rw-r--r--   0        0        0      168 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/default.py
--rw-r--r--   0        0        0      320 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/graphviz/__init__.py
--rw-r--r--   0        0        0     2778 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
--rw-r--r--   0        0        0      316 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/mermaid/__init__.py
--rw-r--r--   0        0        0     2162 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
--rw-r--r--   0        0        0      320 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/plantuml/__init__.py
--rw-r--r--   0        0        0     2012 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
--rw-r--r--   0        0        0      222 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/worker.py
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/__init__.py
--rw-r--r--   0        0        0     2026 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/main.py
--rw-r--r--   0        0        0     1928 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/params.py
--rw-r--r--   0        0        0      164 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/constants.py
--rw-r--r--   0        0        0      284 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/default.py
--rw-r--r--   0        0        0        0 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/__init__.py
--rw-r--r--   0        0        0      721 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/cli_messaging.py
--rw-r--r--   0        0        0      877 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/dict.py
--rw-r--r--   0        0        0     4494 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/file.py
--rw-r--r--   0        0        0     1022 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/jsonify.py
--rw-r--r--   0        0        0      976 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/log.py
--rw-r--r--   0        0        0     1605 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/yaml.py
--rw-r--r--   0        0        0       94 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/main.py
--rw-r--r--   0        0        0     2061 2023-05-13 04:22:52.348138 dbterd-1.2.1/pyproject.toml
--rw-r--r--   0        0        0     4230 1970-01-01 00:00:00.000000 dbterd-1.2.1/PKG-INFO
+-rw-r--r--   0        0        0      203 2023-05-13 06:09:43.232289 dbterd-1.2.2/LICENSE
+-rw-r--r--   0        0        0     3217 2023-05-13 06:09:43.232289 dbterd-1.2.2/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/__init__.py
+-rw-r--r--   0        0        0       37 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/__main__.py
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/__init__.py
+-rw-r--r--   0        0        0     4801 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/base.py
+-rw-r--r--   0        0        0     3157 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/filter.py
+-rw-r--r--   0        0        0      592 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/meta.py
+-rw-r--r--   0        0        0     5658 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/algos/test_relationship.py
+-rw-r--r--   0        0        0     2575 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/base.py
+-rw-r--r--   0        0        0      560 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/factory.py
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/__init__.py
+-rw-r--r--   0        0        0      306 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/constants.py
+-rw-r--r--   0        0        0      296 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/d2/__init__.py
+-rw-r--r--   0        0        0     1591 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/d2/d2_test_relationship.py
+-rw-r--r--   0        0        0      304 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/dbml/__init__.py
+-rw-r--r--   0        0        0     2167 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/dbml/dbml_test_relationship.py
+-rw-r--r--   0        0        0      168 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/default.py
+-rw-r--r--   0        0        0      320 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/graphviz/__init__.py
+-rw-r--r--   0        0        0     2778 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
+-rw-r--r--   0        0        0      316 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/mermaid/__init__.py
+-rw-r--r--   0        0        0     2162 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
+-rw-r--r--   0        0        0      320 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/plantuml/__init__.py
+-rw-r--r--   0        0        0     2012 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
+-rw-r--r--   0        0        0      222 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/adapters/worker.py
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/__init__.py
+-rw-r--r--   0        0        0     2026 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/main.py
+-rw-r--r--   0        0        0     1928 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/cli/params.py
+-rw-r--r--   0        0        0      164 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/constants.py
+-rw-r--r--   0        0        0      284 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/default.py
+-rw-r--r--   0        0        0        0 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/__init__.py
+-rw-r--r--   0        0        0      721 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/cli_messaging.py
+-rw-r--r--   0        0        0      877 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/dict.py
+-rw-r--r--   0        0        0     4494 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/file.py
+-rw-r--r--   0        0        0     1022 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/jsonify.py
+-rw-r--r--   0        0        0      976 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/log.py
+-rw-r--r--   0        0        0     1605 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/helpers/yaml.py
+-rw-r--r--   0        0        0       94 2023-05-13 06:09:43.236290 dbterd-1.2.2/dbterd/main.py
+-rw-r--r--   0        0        0     2061 2023-05-13 06:09:58.348375 dbterd-1.2.2/pyproject.toml
+-rw-r--r--   0        0        0     4230 1970-01-01 00:00:00.000000 dbterd-1.2.2/PKG-INFO
```

### Comparing `dbterd-1.2.1/README.md` & `dbterd-1.2.2/README.md`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/algos/base.py` & `dbterd-1.2.2/dbterd/adapters/algos/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/algos/filter.py` & `dbterd-1.2.2/dbterd/adapters/algos/filter.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/algos/meta.py` & `dbterd-1.2.2/dbterd/adapters/algos/meta.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/algos/test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/algos/test_relationship.py`

 * *Files 22% similar despite different names*

```diff
@@ -51,63 +51,50 @@
 
 
 def get_relationships(manifest, **kwargs):
     """Extract relationships from dbt artifacts based on test relationship
 
     Args:
         manifest (dict): Manifest json
-        kwargs.algo (str): |
-            Algorithm name and optional rules.
-            Smaples:
-            - test_relationship
-            - test_relationship:(name:relationship|c_from:column_name|c_to:field)
-            - test_relationship:(name:foreign_key|c_from:fk_column_name|c_to:pk_column_name)
 
     Returns:
         List[Ref]: List of parsed relationship
     """
-    algo_parts = (kwargs.get("algo") or "").replace(" ", "").split(":", 1)
-    rules, _ = (
-        algo_parts[1] if len(algo_parts) > 1 else DEFAULT_ALGO_RULE,
-        algo_parts[0],
-    )
-    rules = rules[1:-1]  # remove brackets
-    rules = dict(arg.split(":") for arg in rules.split("|"))
-
+    rule = get_algo_rule(**kwargs)
     refs = [
         Ref(
             name=x,
-            table_map=manifest.parent_map[x],
+            table_map=get_table_map(test_node=manifest.nodes[x], **kwargs),
             column_map=[
                 str(
-                    manifest.nodes[x].test_metadata.kwargs.get(rules.get("c_to"))
+                    manifest.nodes[x].test_metadata.kwargs.get(rule.get("c_to"))
                     or "_and_".join(
                         manifest.nodes[x].test_metadata.kwargs.get(
-                            f'{rules.get("c_to")}s', "unknown"
+                            f'{rule.get("c_to")}s', "unknown"
                         )
                     )
                 ).lower(),
                 str(
                     manifest.nodes[x].test_metadata.kwargs.get("column_name")
-                    or manifest.nodes[x].test_metadata.kwargs.get(rules.get("c_from"))
+                    or manifest.nodes[x].test_metadata.kwargs.get(rule.get("c_from"))
                     or "_and_".join(
                         manifest.nodes[x].test_metadata.kwargs.get(
-                            f'{rules.get("c_from")}s', "unknown"
+                            f'{rule.get("c_from")}s', "unknown"
                         )
                     )
                 ).lower(),
             ],
             type=get_relationship_type(
                 manifest.nodes[x].meta.get(TEST_META_RELATIONSHIP_TYPE, "")
             ),
         )
         for x in manifest.nodes
         if (
             x.startswith("test")
-            and rules.get("name").lower() in x.lower()
+            and rule.get("name").lower() in x.lower()
             and manifest.nodes[x].meta.get(TEST_META_IGNORE_IN_ERD, "0") == "0"
         )
     ]
 
     # remove duplicates
     if refs:
         distinct_list = [refs[0]]
@@ -117,14 +104,67 @@
                 distinct_list.append(ref)
 
         return distinct_list
 
     return []
 
 
+def get_algo_rule(**kwargs):
+    """Extract rule from the --algo option
+
+    Args:
+        kwargs.algo (str): |
+            Algorithm name and optional rules.
+            Samples:
+            - test_relationship
+            - test_relationship:(name:relationship|c_from:column_name|c_to:field)
+            - test_relationship:(name:foreign_key|c_from:fk_column_name|c_to:pk_column_name)
+            - test_relationship:(
+                name:foreign_key|
+                c_from:fk_column_name|
+                c_to:pk_column_name|
+                t_to:pk_table_name
+            )
+
+    Returns:
+        dict: Rule object (
+            name [default 'relationship', use contains],
+            c_from [default 'column_name'],
+            c_to [default 'field'],
+            t_to [default 'to']
+        )
+    """
+    algo_parts = (kwargs.get("algo") or "").replace(" ", "").split(":", 1)
+    rules, _ = (
+        algo_parts[1] if len(algo_parts) > 1 else DEFAULT_ALGO_RULE,
+        algo_parts[0],
+    )
+    rules = rules[1:-1]  # remove brackets
+    rules = dict(arg.split(":") for arg in rules.split("|"))
+    return rules
+
+
+def get_table_map(test_node, **kwargs):
+    """Get the table map with order of [to, from] guaranteed
+
+    Args:
+        test_node (dict): Manifest Test node
+
+    Returns:
+        list: [to model, from model]
+    """
+    map = test_node.depends_on.get("nodes", [])
+    rule = get_algo_rule(**kwargs)
+    to_model = str(test_node.test_metadata.kwargs.get(rule.get("t_to", "to"), {}))
+    if f'("{map[1].split(".")[-1]}")'.lower() in to_model.replace("'", '"').lower():
+        return [map[1], map[0]]
+
+    return map
+
+
 def get_relationship_type(meta: str) -> str:
     """Get short form of the relationship type configured in test meta
 
     Args:
         meta (str): meta value
 
     Returns:
```

### Comparing `dbterd-1.2.1/dbterd/adapters/base.py` & `dbterd-1.2.2/dbterd/adapters/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/factory.py` & `dbterd-1.2.2/dbterd/adapters/factory.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/targets/d2/d2_test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/targets/d2/d2_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/targets/dbml/dbml_test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/targets/dbml/dbml_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py` & `dbterd-1.2.2/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/cli/main.py` & `dbterd-1.2.2/dbterd/cli/main.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/cli/params.py` & `dbterd-1.2.2/dbterd/cli/params.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/cli_messaging.py` & `dbterd-1.2.2/dbterd/helpers/cli_messaging.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/dict.py` & `dbterd-1.2.2/dbterd/helpers/dict.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/file.py` & `dbterd-1.2.2/dbterd/helpers/file.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/jsonify.py` & `dbterd-1.2.2/dbterd/helpers/jsonify.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/log.py` & `dbterd-1.2.2/dbterd/helpers/log.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/dbterd/helpers/yaml.py` & `dbterd-1.2.2/dbterd/helpers/yaml.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.1/pyproject.toml` & `dbterd-1.2.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dbterd"
-version = "1.2.1"
+version = "1.2.2"
 description = "CLI to generate ERD Diagram file from dbt artifact files"
 authors = ["Dat Nguyen <datnguyen.it09@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/datnguye/dbterd"
 repository = "https://github.com/datnguye/dbterd"
 keywords = ["flake8", "markdown", "lint"]
```

### Comparing `dbterd-1.2.1/PKG-INFO` & `dbterd-1.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dbterd
-Version: 1.2.1
+Version: 1.2.2
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
-Metadata-Version: 2.1 Name: dbterd Version: 1.2.1 Summary: CLI to generate ERD
+Metadata-Version: 2.1 Name: dbterd Version: 1.2.2 Summary: CLI to generate ERD
 Diagram file from dbt artifact files Home-page: https://github.com/datnguye/
 dbterd License: MIT Keywords: flake8,markdown,lint Author: Dat Nguyen Author-
 email: datnguyen.it09@gmail.com Requires-Python: >=3.9,<4.0 Classifier:
 Environment :: Console Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Classifier: Programming Language
 :: Python :: 3 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Programming Language ::
```

