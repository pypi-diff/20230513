# Comparing `tmp/pypreql-nlp-0.0.5.tar.gz` & `tmp/pypreql-nlp-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pypreql-nlp-0.0.5.tar", last modified: Mon May  8 13:51:30 2023, max compression
+gzip compressed data, was "pypreql-nlp-0.0.6.tar", last modified: Sat May 13 00:14:31 2023, max compression
```

## Comparing `pypreql-nlp-0.0.5.tar` & `pypreql-nlp-0.0.6.tar`

### file list

```diff
@@ -1,23 +1,29 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)     2004 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1566 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/preql_nlp/
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       83 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     7532 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/main.py
--rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/monkeypatch.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/preql_nlp/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/prompts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2357 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/prompts/final_selection.py
--rw-r--r--   0 runner    (1001) docker     (123)     4317 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/prompts/prompt_executor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1284 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/prompts/query_semantic_extraction.py
--rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/preql_nlp/prompts/semantic_to_tokens.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2004 2023-05-08 13:51:30.000000 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      486 2023-05-08 13:51:30.000000 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-08 13:51:30.000000 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-08 13:51:30.000000 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-08 13:51:30.000000 pypreql-nlp-0.0.5/pypreql_nlp.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      172 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-08 13:51:30.223676 pypreql-nlp-0.0.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-05-08 13:51:18.000000 pypreql-nlp-0.0.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     2004 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1566 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/preql_nlp/
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/preql_nlp/cache_providers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/cache_providers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      187 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/cache_providers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1355 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/cache_providers/local_sqlite.py
+-rw-r--r--   0 runner    (1001) docker     (123)       83 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1348 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9272 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/monkeypatch.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/preql_nlp/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/prompts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2356 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/prompts/final_selection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7317 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/prompts/prompt_executor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2063 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/prompts/query_semantic_extraction.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/preql_nlp/prompts/semantic_to_tokens.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2004 2023-05-13 00:14:31.000000 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      641 2023-05-13 00:14:31.000000 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:14:31.000000 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-13 00:14:31.000000 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 00:14:31.000000 pypreql-nlp-0.0.6/pypreql_nlp.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      172 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:14:31.230543 pypreql-nlp-0.0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-05-13 00:14:16.000000 pypreql-nlp-0.0.6/setup.py
```

### Comparing `pypreql-nlp-0.0.5/PKG-INFO` & `pypreql-nlp-0.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pypreql-nlp
-Version: 0.0.5
+Version: 0.0.6
 Summary: NLP interface for pypreql.
 Home-page: 
 Author: 
 Author-email: pypreql-community@gmail.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
```

### Comparing `pypreql-nlp-0.0.5/README.md` & `pypreql-nlp-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `pypreql-nlp-0.0.5/preql_nlp/main.py` & `pypreql-nlp-0.0.6/preql_nlp/main.py`

 * *Files 16% similar despite different names*

```diff
@@ -15,40 +15,53 @@
 from preql_nlp.prompts import (
     run_prompt,
     SemanticToTokensPromptCase,
     SelectionPromptCase,
     SemanticExtractionPromptCase,
 )
 from preql_nlp.constants import logger, DEFAULT_LIMIT
+from preql_nlp.models import (
+    InitialParseResponse,
+    OrderResult,
+    FilterResult,
+    TokenInputs,
+    SemanticTokenResponse,
+    ConceptSelectionResponse,
+    IntermediateParseResults,
+)
+
+from preql.core.models import WhereClause, Conditional, Comparison
+from preql.core.enums import BooleanOperator
+
 
-from dataclasses import dataclass
 from typing import Any
 
 import re
 import uuid
 
+
 def split_to_tokens(input_text: str) -> list[str]:
     return list(set(re.split("\.|\_", input_text)))
 
 
-def build_token_list_by_purpose(concepts, purposes: Iterable[Purpose]):
+def build_token_list_by_purpose(concepts, purposes: Iterable[Purpose]) -> list[str]:
     concepts = {k: v for k, v in concepts.items() if v.purpose in purposes}
 
     unique = set(concepts.keys())
     final = set()
     # if a concept has another concept as a substring, remove
     # to help restrict the size of the search space
     for concept in unique:
         # matched = [comparison  for comparison in unique if comparison in concept]
         # filtered = [m for m in matched if m !=concept]
         # if not filtered:
         #     final.append(concept)
         for x in split_to_tokens(concept):
             final.add(x)
-    return ", ".join(list(final))
+    return list(final)
 
 
 def tokens_to_concept(
     tokens: list[str],
     concepts: List[str],
     limits: int = 5,
     universe: list[str] | None = None,
@@ -75,22 +88,14 @@
         stier = tier_list.pop(0)
         candidates = sorted(pickings[stier], key=lambda x: len(x))
         required = limits - len(found)
         found += candidates[:required]
     return found
 
 
-@dataclass
-class IntermediateParseResults:
-    select: List[str]
-    limit: int
-    order: List[str]
-    # filter: List[FilterItem]
-
-
 def coerce_list_dict(input: Any) -> List[dict]:
     if not isinstance(input, list):
         raise ValueError("Input must be a list")
     for x in input:
         if not isinstance(x, dict):
             raise ValueError("Input must be a list of dicts")
     return input
@@ -101,16 +106,33 @@
         raise ValueError("Input must be a list")
     for x in input:
         if not isinstance(x, str):
             raise ValueError("Input must be a list of dicts")
     return input
 
 
+def coerce_initial_result(input) -> InitialParseResponse:
+    return InitialParseResponse.parse_obj(input)
+
+
+def get_phrase_from_x(x):
+    if isinstance(x, str):
+        return x
+    elif isinstance(x, FilterResult):
+        return x.concept
+    elif isinstance(x, OrderResult):
+        return x.concept
+    raise ValueError
+
+
 def discover_inputs(
-    input_text: str, input_environment: Environment, debug: bool = False, log_info: bool = True
+    input_text: str,
+    input_environment: Environment,
+    debug: bool = False,
+    log_info: bool = True,
 ) -> IntermediateParseResults:
     # we work around prompt size issues and hallucination by doing a two phase discovery
     # first we parse the question into metrics/dimensions
     # then for each one, we match those to a token list
     # and then we deterministically map the tokens back to the most relevant concept
     # TODO: turn the third pass into a prompt
     concepts = input_environment.concepts
@@ -119,88 +141,94 @@
     metrics = build_token_list_by_purpose(concepts, (Purpose.METRIC,))
     dimensions = build_token_list_by_purpose(
         concepts, (Purpose.KEY, Purpose.PROPERTY, Purpose.CONSTANT)
     )
 
     session_uuid = uuid.uuid4()
 
-    parsed = coerce_list_dict(
-        run_prompt(SemanticExtractionPromptCase(input_text), debug=debug, log_info=log_info, session_uuid=session_uuid)
-    )[0]
-    order = parsed.get("order", [])
-    token_inputs = {"metrics": metrics, "dimensions": dimensions}
+    parsed: InitialParseResponse = run_prompt(
+        SemanticExtractionPromptCase(input_text),
+        debug=debug,
+        log_info=log_info,
+        session_uuid=session_uuid,
+    )
+    order = [x.concept for x in parsed.order]
+    filtering = [f.concept for f in parsed.filtering]
+    token_inputs = TokenInputs(
+        metrics=metrics, dimensions=dimensions, order=order, filtering=filtering
+    )
 
     output: List[str] = []
-    for field in [
-        "metrics",
-        "dimensions",
-    ]:
-        local_phrases = [x for x in parsed[field]]
-        phrase_tokens = coerce_list_dict(
-            run_prompt(
-                SemanticToTokensPromptCase(
-                    phrases=local_phrases, tokens=token_inputs[field]
-                ),
-                debug=True,
-                session_uuid=session_uuid,
-                log_info=log_info
-            )
+    for field in ["metrics", "dimensions", "filtering", "order"]:
+        local_phrases = [get_phrase_from_x(x) for x in getattr(parsed, field)]
+        phrase_tokens: SemanticTokenResponse = run_prompt( # type: ignore
+            SemanticToTokensPromptCase(
+                phrases=local_phrases, tokens=getattr(token_inputs, field)
+            ),
+            debug=True,
+            session_uuid=session_uuid,
+            log_info=log_info,
         )
         token_universe = []
         for mapping in phrase_tokens:
-            for k, v in mapping.items():
-                token_universe += v
+            token_universe += mapping.tokens
         for mapping in phrase_tokens:
-            for k, v in mapping.items():
-                concepts = tokens_to_concept(
-                    v,
-                    [c for c in final_concept_list],
-                    limits=5,
-                    universe=token_universe,
+            concepts = tokens_to_concept(
+                mapping.tokens,
+                [c for c in final_concept_list],
+                limits=5,
+                universe=token_universe,
+            )
+            logger.info(f"For phrase {mapping.phrase} got {concepts}")
+            if concepts:
+                output += concepts
+            else:
+                raise ValueError(
+                    f"Could not find concept for input {mapping.phrase} with tokens {mapping.tokens}"
                 )
-                logger.info(f"For phrase {k} got {concepts}")
-                if concepts:
-                    output += concepts
-                else:
-                    raise ValueError(
-                        f"Could not find concept for input {k} with tokens {v}"
-                    )
-    selections = coerce_list_dict(
-        run_prompt(SelectionPromptCase(concepts=output, question=input_text), debug=debug, session_uuid=session_uuid, log_info=log_info)
-    )[0]
-    final = list(set(selections.get("matches", [])))
+    selections: ConceptSelectionResponse = run_prompt( # type: ignore
+        SelectionPromptCase(concepts=output, question=input_text),
+        debug=debug,
+        session_uuid=session_uuid,
+        log_info=log_info,
+    )
+    final = list(set(selections.matches))
 
     return IntermediateParseResults(
-        select=final, limit=parsed.get("limit", 20), order=order
+        select=final,
+        limit=parsed.limit or 20,
+        order=parsed.order,
+        filtering=parsed.filtering,
     )
 
 
 def safe_limit(input: int | None) -> int:
     if not input:
         return DEFAULT_LIMIT
     if input in (-1, 0):
         return DEFAULT_LIMIT
     return input
 
 
 def safe_parse_order_item(
-    input: str, input_concepts: List[Concept]
+    input: OrderResult, input_concepts: List[Concept]
 ) -> OrderItem | None:
-    concept, direction = input.split(" ", 1)
-    matched = [c for c in input_concepts if concept in c.address]
+    matched = [c for c in input_concepts if input.concept in c.address]
     if not matched:
         return None
     try:
-        order = Ordering(direction)
+        order = input.order
     except Exception:
         return None
     return OrderItem(expr=matched[0], order=order)
 
 
-def parse_order(input_concepts: List[Concept], ordering: List[str] | None) -> OrderBy:
+def parse_order(
+    input_concepts: List[Concept], ordering: List[OrderResult] | None
+) -> OrderBy:
     default_order = [
         OrderItem(expr=c, order=Ordering.DESCENDING)
         for c in input_concepts
         if c.purpose == Purpose.METRIC
     ]
     if not ordering:
         return OrderBy(default_order)
@@ -208,33 +236,75 @@
     for order in ordering:
         parsed = safe_parse_order_item(order, input_concepts)
         if parsed:
             final.append(parsed)
     return OrderBy(items=final)
 
 
+
+
+def parse_filter(
+    input: FilterResult, input_concepts: List[Concept]
+) -> Comparison | None:
+    matched = [c for c in input_concepts if input.concept in c.address]
+    if not matched:
+        return None
+    return Comparison(
+        left=matched[0],
+        right=input.values[0] if len(input.values) == 1 else input.values,
+        operator=input.operator,
+    )
+
+
+def parse_filtering(
+    input_concepts: List[Concept], filtering: List[FilterResult]
+) -> WhereClause | None:
+    base = []
+    for item in filtering:
+        parsed = parse_filter(item, input_concepts)
+        if parsed:
+            base.append(parsed)
+    if not base:
+        return None
+    if len(base) == 1:
+        return WhereClause(conditional=base[0])
+    left: Conditional | Comparison = base.pop()
+    while base:
+        right = base.pop()
+        new = Conditional(left=left, right=right, operator=BooleanOperator.AND)
+        left = new
+    return WhereClause(conditional=left)
+
+
 def parse_query(
     input_text: str,
     input_environment: Environment,
     debug: bool = False,
-    log_info: bool=True
+    log_info: bool = True,
 ):
-    results = discover_inputs(input_text, input_environment, debug=debug, log_info=log_info)
+    results = discover_inputs(
+        input_text, input_environment, debug=debug, log_info=log_info
+    )
     concepts = [input_environment.concepts[x] for x in results.select]
     order = parse_order(concepts, results.order)
+    filtering = parse_filtering(concepts, results.filtering)
     if debug:
         print("Concepts found")
         for c in concepts:
             print(c.address)
-    query = Select(selection=concepts, limit=safe_limit(results.limit), order_by=order)
+    query = Select(
+        selection=concepts,
+        limit=safe_limit(results.limit),
+        order_by=order,
+        where_clause=filtering,
+    )
     return query
 
 
-
 def build_query(
     input_text: str,
     input_environment: Environment,
     debug: bool = False,
-    log_info: bool = True
+    log_info: bool = True,
 ) -> ProcessedQuery:
     query = parse_query(input_text, input_environment, debug=debug, log_info=log_info)
     return process_query_v2(statement=query, environment=input_environment)
```

### Comparing `pypreql-nlp-0.0.5/preql_nlp/monkeypatch.py` & `pypreql-nlp-0.0.6/preql_nlp/monkeypatch.py`

 * *Files identical despite different names*

### Comparing `pypreql-nlp-0.0.5/preql_nlp/prompts/final_selection.py` & `pypreql-nlp-0.0.6/preql_nlp/prompts/final_selection.py`

 * *Files 5% similar despite different names*

```diff
@@ -19,11 +19,11 @@
 System:
 {"matches": ["order.state", "order.revenue.sum"],
 "reasoning": "order.state is the best match for state when looking at revenue, and order.revenue.sum would enable aggregating revenue." }
 User: concepts: ["product.color", "order.state", "order.year", "order.revenue.sum", "order.revenue.avg", "product.name", "order.month", "order.day", "product.manufacturer"]  question: "What are the average sales by state?"
 System:
 {"matches": ["order.state", "order.revenue.avg"],
 "reasoning": "order.state is the best match for state, and order.revenue.avg would capture average revenue." }{% endraw %}
-User: concepts:"[{{ concept_string }}]" question: "{{ question }}"
+User: concepts: [{{ concept_string }}] question: "{{ question }}"
 System:
 
 """
```

### Comparing `pypreql-nlp-0.0.5/preql_nlp/prompts/semantic_to_tokens.py` & `pypreql-nlp-0.0.6/preql_nlp/prompts/semantic_to_tokens.py`

 * *Files 22% similar despite different names*

```diff
@@ -2,27 +2,69 @@
 STRUCTURED_PROMPT_V1 = """\
 System: you are an AI that helps a user map phrases to tokens by associating a phrase with tokens related to the words
 in the phrase.
 Guidelines:
 * you can assume the user will always provide a list of phrases
 * you can assume the user will always provide a list of tokens
 * only return tokens provided by the user
-The output should be a VALID JSON blob with the phrases as keys and arrays of tokens as values:
 * If a phrase has no matches, return an empty array
+The output should be a VALID JSON list with each entry having the following keys
+* phrase, the input phrase
+* tokens, a list of matching token strings
+
+
 User: given the tokens ["color", "product", "year", "revenue"], match tokens to the phrases ["product revenue", "product color", "product revenue by year", "yearly revenue"]
 System:
-{% raw %}{
-    "product revenue": ["product", "revenue"],
-    "product color": ["product", "color"],
-    "product revenue by year": ["product", "revenue", "year"],
-    "yearly revenue": ["year", "revenue"]
-}
+{% raw %}
+[
+   {
+      "phrase":"product revenue",
+      "tokens":[
+         "product",
+         "revenue"
+      ]
+   },
+   {
+      "phrase":"product color",
+      "tokens":[
+         "product",
+         "color"
+      ]
+    },
+    {
+      "phrase":"product revenue by year",
+      "tokens":[
+         "product",
+         "revenue",
+         "year"
+      ]
+   },
+    {
+      "phrase":"yearly revenue",
+      "tokens":[
+         "revenue",
+         "year"
+      ]
+   }   
+]
 User: given the tokens ["product", "count", "order", "year"], match tokens to the phrases ["products sold", "orders"]
 System:
-{
-    "products sold": ["product", "count"],
-    "orders": ["order", "count"]
-}{% endraw %}
-User: Given the tokens {{ tokens }}, match tokens to the phrases {{ phrase_str }}
+[
+   {
+      "phrase":"products_sold",
+      "tokens":[
+         "product",
+         "count"
+      ]
+   },
+   {
+      "phrase":"orders",
+      "tokens":[
+         "order",
+         "count"
+      ]
+   }
+]{% endraw %}
+User: Given the tokens {{ tokens }}, match tokens to the phrases [{{ phrase_str }}]
 System:
 """
```

### Comparing `pypreql-nlp-0.0.5/pypreql_nlp.egg-info/PKG-INFO` & `pypreql-nlp-0.0.6/pypreql_nlp.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pypreql-nlp
-Version: 0.0.5
+Version: 0.0.6
 Summary: NLP interface for pypreql.
 Home-page: 
 Author: 
 Author-email: pypreql-community@gmail.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
```

### Comparing `pypreql-nlp-0.0.5/setup.py` & `pypreql-nlp-0.0.6/setup.py`

 * *Files identical despite different names*

