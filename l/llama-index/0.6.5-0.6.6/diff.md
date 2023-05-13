# Comparing `tmp/llama_index-0.6.5.tar.gz` & `tmp/llama_index-0.6.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "llama_index-0.6.5.tar", last modified: Thu May 11 00:33:02 2023, max compression
+gzip compressed data, was "llama_index-0.6.6.tar", last modified: Sat May 13 00:11:40 2023, max compression
```

## Comparing `llama_index-0.6.5.tar` & `llama_index-0.6.6.tar`

### file list

```diff
@@ -1,464 +1,472 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.292707 llama_index-0.6.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-11 00:32:40.000000 llama_index-0.6.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       72 2023-05-11 00:32:40.000000 llama_index-0.6.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-11 00:33:02.292707 llama_index-0.6.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4026 2023-05-11 00:32:40.000000 llama_index-0.6.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.236703 llama_index-0.6.5/llama_index/
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)     4719 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      322 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/async_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.236703 llama_index-0.6.5/llama_index/callbacks/
--rw-r--r--   0 runner    (1001) docker     (123)      196 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/callbacks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3066 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/callbacks/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5526 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/callbacks/llama_debug.py
--rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/callbacks/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.236703 llama_index-0.6.5/llama_index/composability/
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/composability/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      171 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/composability/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/composability/joint_qa_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)      313 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/constants.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/data_structs/
--rw-r--r--   0 runner    (1001) docker     (123)      400 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9458 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/data_structs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2292 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/document_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)     6221 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/node.py
--rw-r--r--   0 runner    (1001) docker     (123)      904 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/registry.py
--rw-r--r--   0 runner    (1001) docker     (123)     3638 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/struct_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/data_structs/table.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/embeddings/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8385 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1164 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/google.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/langchain.py
--rw-r--r--   0 runner    (1001) docker     (123)     9202 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/openai.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/embeddings/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/evaluation/
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/evaluation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12080 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/evaluation/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5341 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/evaluation/dataset_generation.py
--rw-r--r--   0 runner    (1001) docker     (123)      544 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/img_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/indices/
--rw-r--r--   0 runner    (1001) docker     (123)      542 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9102 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      856 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/base_retriever.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/indices/common/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/indices/common/struct_store/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common/struct_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8471 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common/struct_store/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common/struct_store/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     2676 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common/struct_store/sql.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/indices/common_tree/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common_tree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7971 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/common_tree/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.240703 llama_index-0.6.5/llama_index/indices/composability/
--rw-r--r--   0 runner    (1001) docker     (123)      180 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/composability/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3950 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/composability/graph.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/document_summary/
--rw-r--r--   0 runner    (1001) docker     (123)      382 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/document_summary/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6018 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/document_summary/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8686 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/document_summary/retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/empty/
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/empty/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2145 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/empty/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/empty/retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/keyword_table/
--rw-r--r--   0 runner    (1001) docker     (123)      656 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7676 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      650 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/rake_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/retrievers.py
--rw-r--r--   0 runner    (1001) docker     (123)      844 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/simple_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2264 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/keyword_table/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/knowledge_graph/
--rw-r--r--   0 runner    (1001) docker     (123)      254 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/knowledge_graph/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7796 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/knowledge_graph/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     9540 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/knowledge_graph/retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/list/
--rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/list/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3299 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/list/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/list/retrievers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3608 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/loading.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/postprocessor/
--rw-r--r--   0 runner    (1001) docker     (123)      888 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1749 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/cohere_rerank.py
--rw-r--r--   0 runner    (1001) docker     (123)    11715 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/node.py
--rw-r--r--   0 runner    (1001) docker     (123)     8830 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/node_recency.py
--rw-r--r--   0 runner    (1001) docker     (123)     5026 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/pii.py
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/postprocessor/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     8489 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/prompt_helper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/query/
--rw-r--r--   0 runner    (1001) docker     (123)      137 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3386 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/embedding_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.244703 llama_index-0.6.5/llama_index/indices/query/query_transform/
--rw-r--r--   0 runner    (1001) docker     (123)      281 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/query_transform/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8904 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/query_transform/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5920 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/query_transform/prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)     8012 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/response_synthesis.py
--rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/query/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/registry.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.248704 llama_index-0.6.5/llama_index/indices/response/
--rw-r--r--   0 runner    (1001) docker     (123)      419 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/response/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21926 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/response/response_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/response/type.py
--rw-r--r--   0 runner    (1001) docker     (123)     4083 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/service_context.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.248704 llama_index-0.6.5/llama_index/indices/struct_store/
--rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     5765 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/container_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2208 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/pandas.py
--rw-r--r--   0 runner    (1001) docker     (123)     4741 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/pandas_query.py
--rw-r--r--   0 runner    (1001) docker     (123)     6142 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/sql.py
--rw-r--r--   0 runner    (1001) docker     (123)     5950 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/struct_store/sql_query.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.248704 llama_index-0.6.5/llama_index/indices/tree/
--rw-r--r--   0 runner    (1001) docker     (123)      616 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/all_leaf_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)     5853 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     7188 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/inserter.py
--rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/select_leaf_embedding_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)    15309 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/select_leaf_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/tree/tree_root_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)     2002 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.248704 llama_index-0.6.5/llama_index/indices/vector_store/
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/vector_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7631 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/vector_store/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3980 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/indices/vector_store/retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.248704 llama_index-0.6.5/llama_index/langchain_helpers/
--rw-r--r--   0 runner    (1001) docker     (123)       39 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/langchain_helpers/agents/
--rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/agents/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2994 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/agents/agents.py
--rw-r--r--   0 runner    (1001) docker     (123)      837 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/agents/toolkits.py
--rw-r--r--   0 runner    (1001) docker     (123)     2211 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/agents/tools.py
--rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/chain_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     7675 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/memory_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     3287 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/sql_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     1224 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/streaming.py
--rw-r--r--   0 runner    (1001) docker     (123)    19719 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/langchain_helpers/text_splitter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/llm_predictor/
--rw-r--r--   0 runner    (1001) docker     (123)      359 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/llm_predictor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12281 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/llm_predictor/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     4282 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/llm_predictor/chatgpt.py
--rw-r--r--   0 runner    (1001) docker     (123)     8731 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/llm_predictor/huggingface.py
--rw-r--r--   0 runner    (1001) docker     (123)     2274 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/llm_predictor/structured.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/logger/
--rw-r--r--   0 runner    (1001) docker     (123)       95 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/logger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      995 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/logger/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/node_parser/
--rw-r--r--   0 runner    (1001) docker     (123)      184 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/node_parser/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      527 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/node_parser/interface.py
--rw-r--r--   0 runner    (1001) docker     (123)     3582 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/node_parser/node_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2396 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/node_parser/simple.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/optimization/
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/optimization/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4301 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/optimization/optimizer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/output_parsers/
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/output_parsers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      611 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/output_parsers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/output_parsers/guardrails.py
--rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/output_parsers/langchain.py
--rw-r--r--   0 runner    (1001) docker     (123)     1345 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/output_parsers/selection.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/playground/
--rw-r--r--   0 runner    (1001) docker     (123)      202 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/playground/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6471 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/playground/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.252704 llama_index-0.6.5/llama_index/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6633 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1969 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/chat_prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)     1134 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/default_prompt_selectors.py
--rw-r--r--   0 runner    (1001) docker     (123)    10843 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/default_prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)     1120 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/prompt_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     7685 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/prompts/prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.256704 llama_index-0.6.5/llama_index/query_engine/
--rw-r--r--   0 runner    (1001) docker     (123)      635 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3569 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/graph_query_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)     5811 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/multistep_query_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)     6984 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/retriever_query_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)     4587 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/router_query_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)     2964 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/query_engine/transform_query_engine.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.260705 llama_index-0.6.5/llama_index/readers/
--rw-r--r--   0 runner    (1001) docker     (123)     3043 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.260705 llama_index-0.6.5/llama_index/readers/chatgpt_plugin/
--rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/chatgpt_plugin/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2111 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/chatgpt_plugin/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3755 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/chroma.py
--rw-r--r--   0 runner    (1001) docker     (123)     3308 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/database.py
--rw-r--r--   0 runner    (1001) docker     (123)     3456 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/deeplake.py
--rw-r--r--   0 runner    (1001) docker     (123)     4981 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/discord_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     7769 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/elasticsearch.py
--rw-r--r--   0 runner    (1001) docker     (123)     2510 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/faiss.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.260705 llama_index-0.6.5/llama_index/readers/file/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8535 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/base_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/docs_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/epub_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3180 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/image_caption_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     4106 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/image_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3222 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/image_vision_llm_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/ipynb_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3616 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/markdown_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3162 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/mbox_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3945 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/slides_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3357 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/tabular_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1770 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/file/video_audio.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.260705 llama_index-0.6.5/llama_index/readers/github_readers/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/github_readers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11730 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/github_readers/github_api_client.py
--rw-r--r--   0 runner    (1001) docker     (123)    15889 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/github_readers/github_repository_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     5473 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/github_readers/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/google_readers/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/google_readers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/google_readers/gdocs.py
--rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/google_readers/gsheets.py
--rw-r--r--   0 runner    (1001) docker     (123)     3708 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/json.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/make_com/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/make_com/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/make_com/wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     1261 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/mbox.py
--rw-r--r--   0 runner    (1001) docker     (123)     2307 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/metal.py
--rw-r--r--   0 runner    (1001) docker     (123)     4588 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/milvus.py
--rw-r--r--   0 runner    (1001) docker     (123)     2608 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/mongo.py
--rw-r--r--   0 runner    (1001) docker     (123)     5541 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/myscale.py
--rw-r--r--   0 runner    (1001) docker     (123)     5679 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/notion.py
--rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/obsidian.py
--rw-r--r--   0 runner    (1001) docker     (123)     2766 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/pinecone.py
--rw-r--r--   0 runner    (1001) docker     (123)     6920 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/qdrant.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/redis/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/redis/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3492 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/redis/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/schema/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/schema/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1214 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/schema/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     7892 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/slack.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/steamship/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/steamship/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3498 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/steamship/file_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1042 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/string_iterable.py
--rw-r--r--   0 runner    (1001) docker     (123)     1918 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/twitter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/readers/weaviate/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/weaviate/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7760 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/weaviate/client.py
--rw-r--r--   0 runner    (1001) docker     (123)     3986 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/weaviate/reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1867 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/weaviate/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     7987 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/web.py
--rw-r--r--   0 runner    (1001) docker     (123)      981 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/wikipedia.py
--rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/readers/youtube_transcript.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/response/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/response/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2036 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/response/notebook_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/response/pprint_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3068 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/response/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/response/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.264705 llama_index-0.6.5/llama_index/retrievers/
--rw-r--r--   0 runner    (1001) docker     (123)     1258 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/retrievers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/retrievers/transform_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)     2792 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.268705 llama_index-0.6.5/llama_index/selectors/
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/selectors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7082 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/selectors/llm_selectors.py
--rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/selectors/prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)     2235 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/selectors/types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.268705 llama_index-0.6.5/llama_index/storage/
--rw-r--r--   0 runner    (1001) docker     (123)      124 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.268705 llama_index-0.6.5/llama_index/storage/docstore/
--rw-r--r--   0 runner    (1001) docker     (123)      536 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/keyval_docstore.py
--rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/mongo_docstore.py
--rw-r--r--   0 runner    (1001) docker     (123)      762 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/registry.py
--rw-r--r--   0 runner    (1001) docker     (123)     2658 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/simple_docstore.py
--rw-r--r--   0 runner    (1001) docker     (123)     2529 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/types.py
--rw-r--r--   0 runner    (1001) docker     (123)      915 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/docstore/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.268705 llama_index-0.6.5/llama_index/storage/index_store/
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/keyval_index_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/mongo_index_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/simple_index_store.py
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/types.py
--rw-r--r--   0 runner    (1001) docker     (123)      635 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/index_store/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.268705 llama_index-0.6.5/llama_index/storage/kvstore/
--rw-r--r--   0 runner    (1001) docker     (123)      187 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/kvstore/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4061 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/kvstore/mongodb_kvstore.py
--rw-r--r--   0 runner    (1001) docker     (123)     2580 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/kvstore/simple_kvstore.py
--rw-r--r--   0 runner    (1001) docker     (123)      973 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/kvstore/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     4460 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/storage/storage_context.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.272706 llama_index-0.6.5/llama_index/token_counter/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/token_counter/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4664 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/token_counter/mock_chain_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)      722 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/token_counter/mock_embed_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     2874 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/token_counter/token_counter.py
--rw-r--r--   0 runner    (1001) docker     (123)      908 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/token_counter/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.272706 llama_index-0.6.5/llama_index/tools/
--rw-r--r--   0 runner    (1001) docker     (123)      162 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1557 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tools/query_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tools/types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.272706 llama_index-0.6.5/llama_index/tts/
--rw-r--r--   0 runner    (1001) docker     (123)      154 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2589 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tts/bark.py
--rw-r--r--   0 runner    (1001) docker     (123)      631 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tts/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1282 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/tts/elevenlabs.py
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     5847 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.272706 llama_index-0.6.5/llama_index/vector_stores/
--rw-r--r--   0 runner    (1001) docker     (123)     1393 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5181 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/chatgpt_plugin.py
--rw-r--r--   0 runner    (1001) docker     (123)     3942 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/chroma.py
--rw-r--r--   0 runner    (1001) docker     (123)     8629 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/deeplake.py
--rw-r--r--   0 runner    (1001) docker     (123)     4451 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/faiss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3903 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/lancedb.py
--rw-r--r--   0 runner    (1001) docker     (123)     3523 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/metal.py
--rw-r--r--   0 runner    (1001) docker     (123)    15763 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/milvus.py
--rw-r--r--   0 runner    (1001) docker     (123)     8360 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/myscale.py
--rw-r--r--   0 runner    (1001) docker     (123)     7184 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/opensearch.py
--rw-r--r--   0 runner    (1001) docker     (123)    11372 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/pinecone.py
--rw-r--r--   0 runner    (1001) docker     (123)     6504 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/qdrant.py
--rw-r--r--   0 runner    (1001) docker     (123)    12763 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/redis.py
--rw-r--r--   0 runner    (1001) docker     (123)     2237 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/registry.py
--rw-r--r--   0 runner    (1001) docker     (123)     5370 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/simple.py
--rw-r--r--   0 runner    (1001) docker     (123)     2285 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     3379 2023-05-11 00:32:41.000000 llama_index-0.6.5/llama_index/vector_stores/weaviate.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.236703 llama_index-0.6.5/llama_index.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-11 00:33:02.000000 llama_index-0.6.5/llama_index.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    14219 2023-05-11 00:33:02.000000 llama_index-0.6.5/llama_index.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 00:33:02.000000 llama_index-0.6.5/llama_index.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-11 00:33:02.000000 llama_index-0.6.5/llama_index.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-11 00:33:02.000000 llama_index-0.6.5/llama_index.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      276 2023-05-11 00:32:41.000000 llama_index-0.6.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 00:33:02.292707 llama_index-0.6.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1192 2023-05-11 00:32:41.000000 llama_index-0.6.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/callbacks/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/callbacks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2975 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/callbacks/test_llama_debug.py
--rw-r--r--   0 runner    (1001) docker     (123)     1966 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/embeddings/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/embeddings/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3002 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/embeddings/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/composability/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/composability/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      993 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/composability/test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/document_summary/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/document_summary/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1340 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/document_summary/test_index.py
--rw-r--r--   0 runner    (1001) docker     (123)      367 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/document_summary/test_retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/empty/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/empty/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/empty/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/keyword_table/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/keyword_table/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6259 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/keyword_table/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1185 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/keyword_table/test_retrievers.py
--rw-r--r--   0 runner    (1001) docker     (123)     1010 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/keyword_table/test_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.276706 llama_index-0.6.5/tests/indices/knowledge_graph/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/knowledge_graph/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      381 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/knowledge_graph/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     6415 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/knowledge_graph/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3900 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/knowledge_graph/test_retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/list/
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/list/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6487 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/list/test_index.py
--rw-r--r--   0 runner    (1001) docker     (123)     1480 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/list/test_retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/postprocessor/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/postprocessor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13872 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/postprocessor/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/query/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1832 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/query/query_transform/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/query_transform/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      267 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/query_transform/mock_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      787 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/query_transform/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     6649 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/test_compose.py
--rw-r--r--   0 runner    (1001) docker     (123)    13016 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/test_compose_vector.py
--rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/query/test_query_bundle.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/struct_store/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/struct_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/struct_store/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)    11931 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/struct_store/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1234 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/struct_store/test_pandas.py
--rw-r--r--   0 runner    (1001) docker     (123)     3901 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/struct_store/test_sql_query.py
--rw-r--r--   0 runner    (1001) docker     (123)     5540 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/test_loading.py
--rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/test_loading_graph.py
--rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/test_node_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     7178 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/test_prompt_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/test_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.280706 llama_index-0.6.5/tests/indices/tree/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/tree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      992 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/tree/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     4444 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/tree/test_embedding_retriever.py
--rw-r--r--   0 runner    (1001) docker     (123)     7789 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/tree/test_index.py
--rw-r--r--   0 runner    (1001) docker     (123)     1332 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/tree/test_retrievers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/indices/vector_store/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      767 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     1153 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/mock_faiss.py
--rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/mock_services.py
--rw-r--r--   0 runner    (1001) docker     (123)     2960 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_faiss.py
--rw-r--r--   0 runner    (1001) docker     (123)     1630 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_lancedb.py
--rw-r--r--   0 runner    (1001) docker     (123)     1984 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_milvus.py
--rw-r--r--   0 runner    (1001) docker     (123)     4134 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_myscale.py
--rw-r--r--   0 runner    (1001) docker     (123)     1726 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_pinecone.py
--rw-r--r--   0 runner    (1001) docker     (123)     5027 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_retrievers.py
--rw-r--r--   0 runner    (1001) docker     (123)     6554 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_simple.py
--rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/test_weaviate.py
--rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/indices/vector_store/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/langchain_helpers/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/langchain_helpers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3426 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/langchain_helpers/test_text_splitter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/llm_predictor/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/llm_predictor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3174 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/llm_predictor/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/logger/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/logger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/logger/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/mock_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/mock_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8147 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/mock_utils/mock_predict.py
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/mock_utils/mock_prompts.py
--rw-r--r--   0 runner    (1001) docker     (123)     1141 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/mock_utils/mock_text_splitter.py
--rw-r--r--   0 runner    (1001) docker     (123)      739 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/mock_utils/mock_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/optimization/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/optimization/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2466 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/optimization/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/output_parsers/
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/output_parsers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/output_parsers/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)      972 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/output_parsers/test_selection.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.284706 llama_index-0.6.5/tests/playground/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/playground/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3494 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/playground/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.288707 llama_index-0.6.5/tests/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/prompts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4655 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/prompts/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.288707 llama_index-0.6.5/tests/readers/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/readers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11334 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/readers/test_file.py
--rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/readers/test_json.py
--rw-r--r--   0 runner    (1001) docker     (123)     1732 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/readers/test_mongo.py
--rw-r--r--   0 runner    (1001) docker     (123)      339 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/readers/test_string_iterable.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.288707 llama_index-0.6.5/tests/selectors/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/selectors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1261 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/selectors/test_llm_selectors.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.288707 llama_index-0.6.5/tests/storage/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.288707 llama_index-0.6.5/tests/storage/docstore/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/docstore/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2115 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/docstore/test_mongo_docstore.py
--rw-r--r--   0 runner    (1001) docker     (123)     2137 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/docstore/test_simple_docstore.py
--rw-r--r--   0 runner    (1001) docker     (123)      959 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/storage/test_storage_context.py
--rw-r--r--   0 runner    (1001) docker     (123)     3016 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/test_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.292707 llama_index-0.6.5/tests/token_predictor/
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/token_predictor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/token_predictor/test_base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 00:33:02.292707 llama_index-0.6.5/tests/vector_stores/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/vector_stores/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/vector_stores/test_qdrant.py
--rw-r--r--   0 runner    (1001) docker     (123)     1002 2023-05-11 00:32:41.000000 llama_index-0.6.5/tests/vector_stores/test_weaviate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 00:11:20.000000 llama_index-0.6.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-05-13 00:11:20.000000 llama_index-0.6.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-13 00:11:40.107422 llama_index-0.6.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4026 2023-05-13 00:11:20.000000 llama_index-0.6.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.059422 llama_index-0.6.6/llama_index/
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)     4719 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      322 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/async_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.063422 llama_index-0.6.6/llama_index/callbacks/
+-rw-r--r--   0 runner    (1001) docker     (123)      196 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/callbacks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3066 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/callbacks/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5526 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/callbacks/llama_debug.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/callbacks/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.063422 llama_index-0.6.6/llama_index/composability/
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/composability/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      171 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/composability/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/composability/joint_qa_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)      313 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/constants.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.063422 llama_index-0.6.6/llama_index/data_structs/
+-rw-r--r--   0 runner    (1001) docker     (123)      400 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9458 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/data_structs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2292 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/document_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6221 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/node.py
+-rw-r--r--   0 runner    (1001) docker     (123)      904 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/registry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3638 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/struct_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/data_structs/table.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.067422 llama_index-0.6.6/llama_index/embeddings/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8385 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1164 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/google.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/langchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9202 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/openai.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/embeddings/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.067422 llama_index-0.6.6/llama_index/evaluation/
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/evaluation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12080 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/evaluation/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5341 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/evaluation/dataset_generation.py
+-rw-r--r--   0 runner    (1001) docker     (123)      544 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/img_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.067422 llama_index-0.6.6/llama_index/indices/
+-rw-r--r--   0 runner    (1001) docker     (123)      542 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9102 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      856 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/base_retriever.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.067422 llama_index-0.6.6/llama_index/indices/common/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.067422 llama_index-0.6.6/llama_index/indices/common/struct_store/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common/struct_store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8471 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common/struct_store/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common/struct_store/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2676 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common/struct_store/sql.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/common_tree/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common_tree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7971 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/common_tree/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/composability/
+-rw-r--r--   0 runner    (1001) docker     (123)      180 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/composability/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3950 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/composability/graph.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/document_summary/
+-rw-r--r--   0 runner    (1001) docker     (123)      382 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/document_summary/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6018 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/document_summary/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8686 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/document_summary/retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/empty/
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/empty/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2145 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/empty/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/empty/retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/keyword_table/
+-rw-r--r--   0 runner    (1001) docker     (123)      656 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7676 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      650 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/rake_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/retrievers.py
+-rw-r--r--   0 runner    (1001) docker     (123)      844 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/simple_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2264 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/keyword_table/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/knowledge_graph/
+-rw-r--r--   0 runner    (1001) docker     (123)      254 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/knowledge_graph/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7796 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/knowledge_graph/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9540 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/knowledge_graph/retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/list/
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/list/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3299 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/list/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/list/retrievers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3608 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/loading.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/postprocessor/
+-rw-r--r--   0 runner    (1001) docker     (123)      888 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1749 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/cohere_rerank.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11715 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8830 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/node_recency.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5026 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/pii.py
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/postprocessor/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8489 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/prompt_helper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/query/
+-rw-r--r--   0 runner    (1001) docker     (123)      137 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3386 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/embedding_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.071422 llama_index-0.6.6/llama_index/indices/query/query_transform/
+-rw-r--r--   0 runner    (1001) docker     (123)      281 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/query_transform/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8904 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/query_transform/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5920 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/query_transform/prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8012 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/response_synthesis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/query/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/registry.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/response/
+-rw-r--r--   0 runner    (1001) docker     (123)      419 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/response/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21926 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/response/response_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/response/type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4083 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/service_context.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/struct_store/
+-rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5765 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/container_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2208 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/pandas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4741 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/pandas_query.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6142 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/sql.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5950 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/struct_store/sql_query.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/tree/
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/all_leaf_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5853 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7188 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/inserter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/select_leaf_embedding_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15309 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/select_leaf_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/tree/tree_root_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2002 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/vector_store/
+-rw-r--r--   0 runner    (1001) docker     (123)      331 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7702 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/
+-rw-r--r--   0 runner    (1001) docker     (123)      267 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/auto_retriever/
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/auto_retriever/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4476 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/auto_retriever/auto_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/auto_retriever/output_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2645 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/auto_retriever/prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4719 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/indices/vector_store/retrievers/retriever.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/langchain_helpers/
+-rw-r--r--   0 runner    (1001) docker     (123)       39 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.075422 llama_index-0.6.6/llama_index/langchain_helpers/agents/
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/agents/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2994 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/agents/agents.py
+-rw-r--r--   0 runner    (1001) docker     (123)      837 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/agents/toolkits.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2211 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/agents/tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/chain_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7675 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/memory_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3287 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/sql_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1224 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/streaming.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19719 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/langchain_helpers/text_splitter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/llm_predictor/
+-rw-r--r--   0 runner    (1001) docker     (123)      359 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/llm_predictor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12281 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/llm_predictor/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4282 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/llm_predictor/chatgpt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8731 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/llm_predictor/huggingface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2274 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/llm_predictor/structured.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/logger/
+-rw-r--r--   0 runner    (1001) docker     (123)       95 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/logger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      995 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/logger/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/node_parser/
+-rw-r--r--   0 runner    (1001) docker     (123)      184 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/node_parser/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      527 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/node_parser/interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3582 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/node_parser/node_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2396 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/node_parser/simple.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/optimization/
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/optimization/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4301 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/optimization/optimizer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/output_parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/output_parsers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      662 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/output_parsers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/output_parsers/guardrails.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/output_parsers/langchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1963 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/output_parsers/selection.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/playground/
+-rw-r--r--   0 runner    (1001) docker     (123)      202 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/playground/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6471 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/playground/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6633 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1969 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/chat_prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1134 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/default_prompt_selectors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10843 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/default_prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1167 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/prompt_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7685 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/prompts/prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.079422 llama_index-0.6.6/llama_index/query_engine/
+-rw-r--r--   0 runner    (1001) docker     (123)      635 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3569 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/graph_query_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5811 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/multistep_query_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6984 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/retriever_query_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4587 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/router_query_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2964 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/query_engine/transform_query_engine.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.083422 llama_index-0.6.6/llama_index/readers/
+-rw-r--r--   0 runner    (1001) docker     (123)     3043 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.083422 llama_index-0.6.6/llama_index/readers/chatgpt_plugin/
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/chatgpt_plugin/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2111 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/chatgpt_plugin/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3755 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/chroma.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3308 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3456 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/deeplake.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4981 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/discord_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7769 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/elasticsearch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2510 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/faiss.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/file/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8535 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/base_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/docs_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/epub_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3180 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/image_caption_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4106 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/image_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3222 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/image_vision_llm_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/ipynb_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3616 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/markdown_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3162 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/mbox_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3945 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/slides_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3357 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/tabular_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1770 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/file/video_audio.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/github_readers/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/github_readers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11730 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/github_readers/github_api_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15889 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/github_readers/github_repository_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5473 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/github_readers/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/google_readers/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/google_readers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/google_readers/gdocs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/google_readers/gsheets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3708 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/json.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/make_com/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/make_com/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/make_com/wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1261 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/mbox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2307 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/metal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4588 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/milvus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2608 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/mongo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5541 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/myscale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5679 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/notion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/obsidian.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2766 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/pinecone.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6920 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/qdrant.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/redis/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/redis/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3492 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/redis/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/schema/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/schema/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1214 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/schema/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7892 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/slack.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/steamship/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/steamship/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3498 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/steamship/file_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1042 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/string_iterable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1918 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/twitter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.087422 llama_index-0.6.6/llama_index/readers/weaviate/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/weaviate/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7105 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/weaviate/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3986 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/weaviate/reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1867 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/weaviate/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7987 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/web.py
+-rw-r--r--   0 runner    (1001) docker     (123)      981 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/wikipedia.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/readers/youtube_transcript.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/response/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/response/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2036 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/response/notebook_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/response/pprint_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3068 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/response/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/response/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/retrievers/
+-rw-r--r--   0 runner    (1001) docker     (123)     1329 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/retrievers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/retrievers/transform_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3542 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/selectors/
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/selectors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7082 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/selectors/llm_selectors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/selectors/prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2235 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/selectors/types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/storage/
+-rw-r--r--   0 runner    (1001) docker     (123)      124 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/storage/docstore/
+-rw-r--r--   0 runner    (1001) docker     (123)      536 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/keyval_docstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/mongo_docstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)      762 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/registry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2658 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/simple_docstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2529 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)      915 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/docstore/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/storage/index_store/
+-rw-r--r--   0 runner    (1001) docker     (123)      301 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/keyval_index_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/mongo_index_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/simple_index_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)      635 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/index_store/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.091422 llama_index-0.6.6/llama_index/storage/kvstore/
+-rw-r--r--   0 runner    (1001) docker     (123)      187 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/kvstore/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4061 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/kvstore/mongodb_kvstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2580 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/kvstore/simple_kvstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)      973 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/kvstore/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4460 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/storage/storage_context.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/llama_index/token_counter/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/token_counter/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4664 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/token_counter/mock_chain_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)      722 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/token_counter/mock_embed_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2874 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/token_counter/token_counter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/token_counter/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/llama_index/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)      162 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1557 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tools/query_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tools/types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/llama_index/tts/
+-rw-r--r--   0 runner    (1001) docker     (123)      154 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2589 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tts/bark.py
+-rw-r--r--   0 runner    (1001) docker     (123)      631 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tts/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1282 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/tts/elevenlabs.py
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5847 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/llama_index/vector_stores/
+-rw-r--r--   0 runner    (1001) docker     (123)     1393 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5332 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/chatgpt_plugin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5336 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/chroma.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8767 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/deeplake.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4593 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/faiss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4047 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/lancedb.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4882 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/metal.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15898 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/milvus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8535 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/myscale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7323 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/opensearch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10362 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/pinecone.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7363 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/qdrant.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14195 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/redis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2237 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/registry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5554 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/simple.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3450 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2286 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-05-13 00:11:20.000000 llama_index-0.6.6/llama_index/vector_stores/weaviate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.059422 llama_index-0.6.6/llama_index.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-13 00:11:40.000000 llama_index-0.6.6/llama_index.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    14603 2023-05-13 00:11:40.000000 llama_index-0.6.6/llama_index.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:11:40.000000 llama_index-0.6.6/llama_index.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 00:11:40.000000 llama_index-0.6.6/llama_index.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 00:11:40.000000 llama_index-0.6.6/llama_index.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-05-13 00:11:20.000000 llama_index-0.6.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:11:40.107422 llama_index-0.6.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1192 2023-05-13 00:11:20.000000 llama_index-0.6.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/tests/callbacks/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/callbacks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2975 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/callbacks/test_llama_debug.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1966 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.095422 llama_index-0.6.6/tests/embeddings/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/embeddings/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3002 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/embeddings/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/composability/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/composability/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1008 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/composability/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/document_summary/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/document_summary/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1340 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/document_summary/test_index.py
+-rw-r--r--   0 runner    (1001) docker     (123)      367 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/document_summary/test_retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/empty/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/empty/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/empty/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/keyword_table/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/keyword_table/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6259 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/keyword_table/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1185 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/keyword_table/test_retrievers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1010 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/keyword_table/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/knowledge_graph/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/knowledge_graph/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      381 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/knowledge_graph/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6415 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/knowledge_graph/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3900 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/knowledge_graph/test_retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/list/
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/list/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6487 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/list/test_index.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1480 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/list/test_retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/postprocessor/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/postprocessor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13872 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/postprocessor/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/query/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1832 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.099422 llama_index-0.6.6/tests/indices/query/query_transform/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/query_transform/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      267 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/query_transform/mock_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      787 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/query_transform/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6649 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/test_compose.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12483 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/test_compose_vector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/query/test_query_bundle.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/indices/struct_store/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/struct_store/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/struct_store/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11931 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/struct_store/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1234 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/struct_store/test_pandas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3901 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/struct_store/test_sql_query.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5540 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/test_loading.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/test_loading_graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/test_node_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7178 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/test_prompt_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/indices/tree/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/tree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      992 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/tree/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4444 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/tree/test_embedding_retriever.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7789 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/tree/test_index.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1332 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/tree/test_retrievers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/indices/vector_store/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/indices/vector_store/auto_retriever/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/auto_retriever/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/auto_retriever/test_output_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)      767 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1153 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/mock_faiss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1020 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/mock_services.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2960 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/test_faiss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4134 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/test_myscale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/test_pinecone.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5027 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/test_retrievers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6554 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/test_simple.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2125 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/indices/vector_store/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/langchain_helpers/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/langchain_helpers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3426 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/langchain_helpers/test_text_splitter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/llm_predictor/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/llm_predictor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3174 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/llm_predictor/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/logger/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/logger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/logger/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/mock_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/mock_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8147 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/mock_utils/mock_predict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/mock_utils/mock_prompts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1141 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/mock_utils/mock_text_splitter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      739 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/mock_utils/mock_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/optimization/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/optimization/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2466 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/optimization/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/output_parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/output_parsers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/output_parsers/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/output_parsers/test_selection.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.103422 llama_index-0.6.6/tests/playground/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/playground/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3494 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/playground/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/prompts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4655 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/prompts/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/readers/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/readers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11334 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/readers/test_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/readers/test_json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1732 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/readers/test_mongo.py
+-rw-r--r--   0 runner    (1001) docker     (123)      339 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/readers/test_string_iterable.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/selectors/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/selectors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1261 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/selectors/test_llm_selectors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/storage/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/storage/docstore/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/docstore/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2115 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/docstore/test_mongo_docstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2137 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/docstore/test_simple_docstore.py
+-rw-r--r--   0 runner    (1001) docker     (123)      959 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/storage/test_storage_context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3016 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/token_predictor/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/token_predictor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/token_predictor/test_base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:40.107422 llama_index-0.6.6/tests/vector_stores/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/vector_stores/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/vector_stores/test_qdrant.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1002 2023-05-13 00:11:20.000000 llama_index-0.6.6/tests/vector_stores/test_weaviate.py
```

### Comparing `llama_index-0.6.5/LICENSE` & `llama_index-0.6.6/LICENSE`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/PKG-INFO` & `llama_index-0.6.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: llama_index
-Version: 0.6.5
+Version: 0.6.6
 Summary: Interface between LLMs and your data
 Home-page: https://github.com/jerryjliu/llama_index
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # 🗂️ LlamaIndex 🦙
```

### Comparing `llama_index-0.6.5/README.md` & `llama_index-0.6.6/README.md`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/__init__.py` & `llama_index-0.6.6/llama_index/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/callbacks/base.py` & `llama_index-0.6.6/llama_index/callbacks/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/callbacks/llama_debug.py` & `llama_index-0.6.6/llama_index/callbacks/llama_debug.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/callbacks/schema.py` & `llama_index-0.6.6/llama_index/callbacks/schema.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/composability/joint_qa_summary.py` & `llama_index-0.6.6/llama_index/composability/joint_qa_summary.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/data_structs.py` & `llama_index-0.6.6/llama_index/data_structs/data_structs.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/document_summary.py` & `llama_index-0.6.6/llama_index/data_structs/document_summary.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/node.py` & `llama_index-0.6.6/llama_index/data_structs/node.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/registry.py` & `llama_index-0.6.6/llama_index/data_structs/registry.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/struct_type.py` & `llama_index-0.6.6/llama_index/data_structs/struct_type.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/data_structs/table.py` & `llama_index-0.6.6/llama_index/data_structs/table.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/embeddings/base.py` & `llama_index-0.6.6/llama_index/embeddings/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/embeddings/google.py` & `llama_index-0.6.6/llama_index/embeddings/google.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/embeddings/langchain.py` & `llama_index-0.6.6/llama_index/embeddings/langchain.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/embeddings/openai.py` & `llama_index-0.6.6/llama_index/embeddings/openai.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/embeddings/utils.py` & `llama_index-0.6.6/llama_index/embeddings/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/evaluation/base.py` & `llama_index-0.6.6/llama_index/evaluation/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/evaluation/dataset_generation.py` & `llama_index-0.6.6/llama_index/evaluation/dataset_generation.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/img_utils.py` & `llama_index-0.6.6/llama_index/img_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/__init__.py` & `llama_index-0.6.6/llama_index/indices/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/base.py` & `llama_index-0.6.6/llama_index/indices/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/base_retriever.py` & `llama_index-0.6.6/llama_index/indices/base_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/common/struct_store/base.py` & `llama_index-0.6.6/llama_index/indices/common/struct_store/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/common/struct_store/schema.py` & `llama_index-0.6.6/llama_index/indices/common/struct_store/schema.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/common/struct_store/sql.py` & `llama_index-0.6.6/llama_index/indices/common/struct_store/sql.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/common_tree/base.py` & `llama_index-0.6.6/llama_index/indices/common_tree/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/composability/graph.py` & `llama_index-0.6.6/llama_index/indices/composability/graph.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/document_summary/base.py` & `llama_index-0.6.6/llama_index/indices/document_summary/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/document_summary/retrievers.py` & `llama_index-0.6.6/llama_index/indices/document_summary/retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/empty/base.py` & `llama_index-0.6.6/llama_index/indices/empty/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/empty/retrievers.py` & `llama_index-0.6.6/llama_index/indices/empty/retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/__init__.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/base.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/rake_base.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/rake_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/retrievers.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/simple_base.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/simple_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/keyword_table/utils.py` & `llama_index-0.6.6/llama_index/indices/keyword_table/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/knowledge_graph/base.py` & `llama_index-0.6.6/llama_index/indices/knowledge_graph/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/knowledge_graph/retrievers.py` & `llama_index-0.6.6/llama_index/indices/knowledge_graph/retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/list/base.py` & `llama_index-0.6.6/llama_index/indices/list/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/list/retrievers.py` & `llama_index-0.6.6/llama_index/indices/list/retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/loading.py` & `llama_index-0.6.6/llama_index/indices/loading.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/postprocessor/__init__.py` & `llama_index-0.6.6/llama_index/indices/postprocessor/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/postprocessor/cohere_rerank.py` & `llama_index-0.6.6/llama_index/indices/postprocessor/cohere_rerank.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/postprocessor/node.py` & `llama_index-0.6.6/llama_index/indices/postprocessor/node.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/postprocessor/node_recency.py` & `llama_index-0.6.6/llama_index/indices/postprocessor/node_recency.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/postprocessor/pii.py` & `llama_index-0.6.6/llama_index/indices/postprocessor/pii.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/prompt_helper.py` & `llama_index-0.6.6/llama_index/indices/prompt_helper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/base.py` & `llama_index-0.6.6/llama_index/indices/query/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/embedding_utils.py` & `llama_index-0.6.6/llama_index/indices/query/embedding_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/query_transform/base.py` & `llama_index-0.6.6/llama_index/indices/query/query_transform/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/query_transform/prompts.py` & `llama_index-0.6.6/llama_index/indices/query/query_transform/prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/response_synthesis.py` & `llama_index-0.6.6/llama_index/indices/query/response_synthesis.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/query/schema.py` & `llama_index-0.6.6/llama_index/indices/query/schema.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/registry.py` & `llama_index-0.6.6/llama_index/indices/registry.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/response/response_builder.py` & `llama_index-0.6.6/llama_index/indices/response/response_builder.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/service_context.py` & `llama_index-0.6.6/llama_index/indices/service_context.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/__init__.py` & `llama_index-0.6.6/llama_index/indices/struct_store/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/base.py` & `llama_index-0.6.6/llama_index/indices/struct_store/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/container_builder.py` & `llama_index-0.6.6/llama_index/indices/struct_store/container_builder.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/pandas.py` & `llama_index-0.6.6/llama_index/indices/struct_store/pandas.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/pandas_query.py` & `llama_index-0.6.6/llama_index/indices/struct_store/pandas_query.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/sql.py` & `llama_index-0.6.6/llama_index/indices/struct_store/sql.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/struct_store/sql_query.py` & `llama_index-0.6.6/llama_index/indices/struct_store/sql_query.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/__init__.py` & `llama_index-0.6.6/llama_index/indices/tree/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/all_leaf_retriever.py` & `llama_index-0.6.6/llama_index/indices/tree/all_leaf_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/base.py` & `llama_index-0.6.6/llama_index/indices/tree/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/inserter.py` & `llama_index-0.6.6/llama_index/indices/tree/inserter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/select_leaf_embedding_retriever.py` & `llama_index-0.6.6/llama_index/indices/tree/select_leaf_embedding_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/select_leaf_retriever.py` & `llama_index-0.6.6/llama_index/indices/tree/select_leaf_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/tree/tree_root_retriever.py` & `llama_index-0.6.6/llama_index/indices/tree/tree_root_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/utils.py` & `llama_index-0.6.6/llama_index/indices/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/indices/vector_store/base.py` & `llama_index-0.6.6/llama_index/indices/vector_store/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,18 +10,15 @@
 from llama_index.data_structs.data_structs import IndexDict
 from llama_index.data_structs.node import ImageNode, IndexNode, Node
 from llama_index.indices.base import BaseGPTIndex
 from llama_index.indices.base_retriever import BaseRetriever
 from llama_index.indices.service_context import ServiceContext
 from llama_index.storage.storage_context import StorageContext
 from llama_index.token_counter.token_counter import llm_token_counter
-from llama_index.vector_stores.types import (
-    NodeWithEmbedding,
-    VectorStore,
-)
+from llama_index.vector_stores.types import NodeWithEmbedding, VectorStore
 
 
 class GPTVectorStoreIndex(BaseGPTIndex[IndexDict]):
     """Base GPT Vector Store Index.
 
     Args:
         use_async (bool): Whether to use asynchronous calls. Defaults to False.
@@ -129,14 +126,17 @@
             results.append(result)
         return results
 
     async def _async_add_nodes_to_index(
         self, index_struct: IndexDict, nodes: Sequence[Node]
     ) -> None:
         """Asynchronously add nodes to index."""
+        if not nodes:
+            return
+
         embedding_results = await self._aget_node_embedding_results(nodes)
         new_ids = self._vector_store.add(embedding_results)
 
         # if the vector store doesn't store text, we need to add the nodes to the
         # index struct and document store
         if not self._vector_store.stores_text:
             for result, new_id in zip(embedding_results, new_ids):
@@ -145,14 +145,17 @@
 
     def _add_nodes_to_index(
         self,
         index_struct: IndexDict,
         nodes: Sequence[Node],
     ) -> None:
         """Add document to index."""
+        if not nodes:
+            return
+
         embedding_results = self._get_node_embedding_results(nodes)
         new_ids = self._vector_store.add(embedding_results)
 
         if not self._vector_store.stores_text:
             # NOTE: if the vector store doesn't store text,
             # we need to add the nodes to the index struct and document store
             for result, new_id in zip(embedding_results, new_ids):
```

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/agents/__init__.py` & `llama_index-0.6.6/llama_index/langchain_helpers/agents/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/agents/agents.py` & `llama_index-0.6.6/llama_index/langchain_helpers/agents/agents.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/agents/toolkits.py` & `llama_index-0.6.6/llama_index/langchain_helpers/agents/toolkits.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/agents/tools.py` & `llama_index-0.6.6/llama_index/langchain_helpers/agents/tools.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/memory_wrapper.py` & `llama_index-0.6.6/llama_index/langchain_helpers/memory_wrapper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/sql_wrapper.py` & `llama_index-0.6.6/llama_index/langchain_helpers/sql_wrapper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/streaming.py` & `llama_index-0.6.6/llama_index/langchain_helpers/streaming.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/langchain_helpers/text_splitter.py` & `llama_index-0.6.6/llama_index/langchain_helpers/text_splitter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/llm_predictor/base.py` & `llama_index-0.6.6/llama_index/llm_predictor/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -334,15 +334,15 @@
         Returns:
             Tuple[str, str]: Tuple of the predicted answer and the formatted prompt.
 
         """
         llm_payload = {**prompt_args}
         llm_payload["template"] = prompt
         event_id = self.callback_manager.on_event_start(
-            CBEventType.LLM, payload=prompt_args
+            CBEventType.LLM, payload=llm_payload
         )
         formatted_prompt = prompt.format(llm=self._llm, **prompt_args)
         llm_prediction = await self._apredict(prompt, **prompt_args)
         logger.debug(llm_prediction)
 
         # We assume that the value of formatted_prompt is exactly the thing
         # eventually sent to OpenAI, or whatever LLM downstream
```

### Comparing `llama_index-0.6.5/llama_index/llm_predictor/chatgpt.py` & `llama_index-0.6.6/llama_index/llm_predictor/chatgpt.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/llm_predictor/huggingface.py` & `llama_index-0.6.6/llama_index/llm_predictor/huggingface.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/llm_predictor/structured.py` & `llama_index-0.6.6/llama_index/llm_predictor/structured.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/logger/base.py` & `llama_index-0.6.6/llama_index/logger/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/node_parser/interface.py` & `llama_index-0.6.6/llama_index/node_parser/interface.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/node_parser/node_utils.py` & `llama_index-0.6.6/llama_index/node_parser/node_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/node_parser/simple.py` & `llama_index-0.6.6/llama_index/node_parser/simple.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/optimization/optimizer.py` & `llama_index-0.6.6/llama_index/optimization/optimizer.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/output_parsers/base.py` & `llama_index-0.6.6/llama_index/output_parsers/base.py`

 * *Files 11% similar despite different names*

```diff
@@ -19,7 +19,11 @@
     @abstractmethod
     def parse(self, output: str) -> Any:
         """Parse, validate, and correct errors programmatically."""
 
     @abstractmethod
     def format(self, output: str) -> str:
         """Format a query with structured output formatting instructions."""
+
+
+class OutputParserException(Exception):
+    pass
```

### Comparing `llama_index-0.6.5/llama_index/output_parsers/guardrails.py` & `llama_index-0.6.6/llama_index/output_parsers/guardrails.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/output_parsers/langchain.py` & `llama_index-0.6.6/llama_index/output_parsers/langchain.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/output_parsers/selection.py` & `llama_index-0.6.6/llama_index/output_parsers/selection.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,12 +1,13 @@
-from dataclasses import dataclass
 import json
+from dataclasses import dataclass
 from typing import Any
 
 from dataclasses_json import DataClassJsonMixin
+
 from llama_index.output_parsers.base import BaseOutputParser, StructuredOutput
 
 
 def _escape_curly_braces(input_string: str) -> str:
     # Replace '{' with '{{' and '}' with '}}' to escape curly braces
     escaped_string = input_string.replace("{", "{{").replace("}", "}}")
     return escaped_string
@@ -41,15 +42,34 @@
 @dataclass
 class Answer(DataClassJsonMixin):
     choice: int
     reason: str
 
 
 class SelectionOutputParser(BaseOutputParser):
+    def _marshal_llm_to_json(self, output: str) -> str:
+        """Extract a valid JSON array from a string.
+        Extracts a substring that represents a valid JSON array.
+
+        Args:
+            output: A string that may contain a valid JSON array surrounded by
+            extraneous characters or information.
+
+        Returns:
+            A string representing a valid JSON array.
+
+        """
+        output = output.strip()
+        left = output.find("[")
+        right = output.rfind("]")
+        output = output[left : right + 1]
+        return output
+
     def parse(self, output: str) -> Any:
+        output = self._marshal_llm_to_json(output)
         json_list = json.loads(output)
         answers = [Answer.from_dict(json_dict) for json_dict in json_list]
         return StructuredOutput(raw_output=output, parsed_output=answers)
 
     def format(self, prompt_template: str) -> str:
         fmt = prompt_template + "\n\n" + _escape_curly_braces(FORMAT_STR)
         return fmt
```

### Comparing `llama_index-0.6.5/llama_index/playground/base.py` & `llama_index-0.6.6/llama_index/playground/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/prompts/base.py` & `llama_index-0.6.6/llama_index/prompts/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/prompts/chat_prompts.py` & `llama_index-0.6.6/llama_index/prompts/chat_prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/prompts/default_prompt_selectors.py` & `llama_index-0.6.6/llama_index/prompts/default_prompt_selectors.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/prompts/default_prompts.py` & `llama_index-0.6.6/llama_index/prompts/default_prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/prompts/prompts.py` & `llama_index-0.6.6/llama_index/prompts/prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/__init__.py` & `llama_index-0.6.6/llama_index/query_engine/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/graph_query_engine.py` & `llama_index-0.6.6/llama_index/query_engine/graph_query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/multistep_query_engine.py` & `llama_index-0.6.6/llama_index/query_engine/multistep_query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/retriever_query_engine.py` & `llama_index-0.6.6/llama_index/query_engine/retriever_query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/router_query_engine.py` & `llama_index-0.6.6/llama_index/query_engine/router_query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/query_engine/transform_query_engine.py` & `llama_index-0.6.6/llama_index/query_engine/transform_query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/__init__.py` & `llama_index-0.6.6/llama_index/readers/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/base.py` & `llama_index-0.6.6/llama_index/readers/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/chatgpt_plugin/base.py` & `llama_index-0.6.6/llama_index/readers/chatgpt_plugin/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/chroma.py` & `llama_index-0.6.6/llama_index/readers/chroma.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/database.py` & `llama_index-0.6.6/llama_index/readers/database.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/deeplake.py` & `llama_index-0.6.6/llama_index/readers/deeplake.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/discord_reader.py` & `llama_index-0.6.6/llama_index/readers/discord_reader.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/download.py` & `llama_index-0.6.6/llama_index/readers/download.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/elasticsearch.py` & `llama_index-0.6.6/llama_index/readers/elasticsearch.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/faiss.py` & `llama_index-0.6.6/llama_index/readers/faiss.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/base.py` & `llama_index-0.6.6/llama_index/readers/file/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/base_parser.py` & `llama_index-0.6.6/llama_index/readers/file/base_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/docs_parser.py` & `llama_index-0.6.6/llama_index/readers/file/docs_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/epub_parser.py` & `llama_index-0.6.6/llama_index/readers/file/epub_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/image_caption_parser.py` & `llama_index-0.6.6/llama_index/readers/file/image_caption_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/image_parser.py` & `llama_index-0.6.6/llama_index/readers/file/image_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/image_vision_llm_parser.py` & `llama_index-0.6.6/llama_index/readers/file/image_vision_llm_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/ipynb_parser.py` & `llama_index-0.6.6/llama_index/readers/file/ipynb_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/markdown_parser.py` & `llama_index-0.6.6/llama_index/readers/file/markdown_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/mbox_parser.py` & `llama_index-0.6.6/llama_index/readers/file/mbox_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/slides_parser.py` & `llama_index-0.6.6/llama_index/readers/file/slides_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/tabular_parser.py` & `llama_index-0.6.6/llama_index/readers/file/tabular_parser.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/file/video_audio.py` & `llama_index-0.6.6/llama_index/readers/file/video_audio.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/github_readers/github_api_client.py` & `llama_index-0.6.6/llama_index/readers/github_readers/github_api_client.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/github_readers/github_repository_reader.py` & `llama_index-0.6.6/llama_index/readers/github_readers/github_repository_reader.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/github_readers/utils.py` & `llama_index-0.6.6/llama_index/readers/github_readers/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/google_readers/gdocs.py` & `llama_index-0.6.6/llama_index/readers/google_readers/gdocs.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/google_readers/gsheets.py` & `llama_index-0.6.6/llama_index/readers/google_readers/gsheets.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/json.py` & `llama_index-0.6.6/llama_index/readers/json.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/make_com/wrapper.py` & `llama_index-0.6.6/llama_index/readers/make_com/wrapper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/mbox.py` & `llama_index-0.6.6/llama_index/readers/mbox.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/metal.py` & `llama_index-0.6.6/llama_index/readers/metal.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/milvus.py` & `llama_index-0.6.6/llama_index/readers/milvus.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/mongo.py` & `llama_index-0.6.6/llama_index/readers/mongo.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/myscale.py` & `llama_index-0.6.6/llama_index/readers/myscale.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/notion.py` & `llama_index-0.6.6/llama_index/readers/notion.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/obsidian.py` & `llama_index-0.6.6/llama_index/readers/obsidian.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/pinecone.py` & `llama_index-0.6.6/llama_index/readers/pinecone.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/qdrant.py` & `llama_index-0.6.6/llama_index/readers/qdrant.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/redis/utils.py` & `llama_index-0.6.6/llama_index/readers/redis/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/schema/base.py` & `llama_index-0.6.6/llama_index/readers/schema/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/slack.py` & `llama_index-0.6.6/llama_index/readers/slack.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/steamship/file_reader.py` & `llama_index-0.6.6/llama_index/readers/steamship/file_reader.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/string_iterable.py` & `llama_index-0.6.6/llama_index/readers/string_iterable.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/twitter.py` & `llama_index-0.6.6/llama_index/readers/twitter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/weaviate/client.py` & `llama_index-0.6.6/llama_index/readers/weaviate/client.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,28 +1,23 @@
 """Weaviate-specific serializers for LlamaIndex data structures.
 
 Contain conversion to and from dataclasses that LlamaIndex uses.
 
 """
 
 import json
+import logging
 from dataclasses import field
-from typing import Any, Dict, List, Optional, cast
+from typing import Any, Dict, List, Optional, Tuple, cast
 
 from llama_index.data_structs.data_structs import Node
 from llama_index.data_structs.node import DocumentRelationship
-from llama_index.readers.weaviate.utils import (
-    get_by_id,
-    parse_get_response,
-    validate_client,
-)
-from llama_index.utils import get_new_id
+from llama_index.readers.weaviate.utils import parse_get_response, validate_client
 from llama_index.vector_stores.types import VectorStoreQuery, VectorStoreQueryMode
-
-import logging
+from llama_index.vector_stores.utils import metadata_dict_to_node, node_to_metadata_dict
 
 _logger = logging.getLogger(__name__)
 
 NODE_SCHEMA: List[Dict] = [
     {
         "dataType": ["string"],
         "description": "Text property",
@@ -31,50 +26,30 @@
     {
         "dataType": ["string"],
         "description": "Document id",
         "name": "doc_id",
     },
     {
         "dataType": ["string"],
-        "description": "extra_info (in JSON)",
-        "name": "extra_info",
-    },
-    {
-        "dataType": ["string"],
         "description": "The ref_doc_id of the Node",
         "name": "ref_doc_id",
     },
     {
         "dataType": ["string"],
         "description": "node_info (in JSON)",
         "name": "node_info",
     },
     {
         "dataType": ["string"],
-        "description": "The hash of the Document",
-        "name": "doc_hash",
-    },
-    {
-        "dataType": ["string"],
         "description": "The relationships of the node (in JSON)",
         "name": "relationships",
     },
 ]
 
 
-def _get_by_id(client: Any, object_id: str, class_prefix: str) -> Dict:
-    """Get entry by id."""
-    validate_client(client)
-    class_name = _class_name(class_prefix)
-    properties = NODE_SCHEMA
-    prop_names = [p["name"] for p in properties]
-    entry = get_by_id(client, object_id, class_name, prop_names)
-    return entry
-
-
 def create_schema(client: Any, class_prefix: str) -> None:
     """Create schema."""
     validate_client(client)
     # first check if schema exists
     schema = client.schema.get()
     classes = schema["classes"]
     existing_class_names = {c["class"] for c in classes}
@@ -135,94 +110,84 @@
 
 
 def _class_name(class_prefix: str) -> str:
     """Return class name."""
     return f"{class_prefix}_Node"
 
 
-def _to_node(entry: Dict) -> Node:
-    """Convert to Node."""
+def _legacy_metadata_dict_to_node(entry: Dict[str, Any]) -> Tuple[dict, dict, dict]:
+    """Legacy logic for converting metadata dict to node data.
+    Only for backwards compatibility.
+    """
     extra_info_str = entry["extra_info"]
     if extra_info_str == "":
-        extra_info = None
+        extra_info = {}
     else:
         extra_info = json.loads(extra_info_str)
 
     node_info_str = entry["node_info"]
     if node_info_str == "":
-        node_info = None
+        node_info = {}
     else:
         node_info = json.loads(node_info_str)
 
     relationships_str = entry["relationships"]
     relationships: Dict[DocumentRelationship, str]
     if relationships_str == "":
         relationships = field(default_factory=dict)
     else:
         relationships = {
             DocumentRelationship(k): v for k, v in json.loads(relationships_str).items()
         }
+    return extra_info, node_info, relationships
+
+
+def _to_node(entry: Dict) -> Node:
+    """Convert to Node."""
+    additional = entry.pop("_additional")
+    try:
+        extra_info, node_info, relationships = metadata_dict_to_node(entry)
+    except Exception as e:
+        _logger.debug("Failed to parse Node metadata, fallback to legacy logic.", e)
+        extra_info, node_info, relationships = _legacy_metadata_dict_to_node(entry)
 
     return Node(
         text=entry["text"],
+        embedding=additional["vector"],
         doc_id=entry["doc_id"],
-        embedding=entry["_additional"]["vector"],
         extra_info=extra_info,
         node_info=node_info,
         relationships=relationships,
     )
 
 
-def _node_to_dict(node: Node) -> dict:
-    node_dict = node.to_dict()
-    node_dict.pop("embedding")  # NOTE: stored outside of dict
-
-    # json-serialize the extra_info
-    extra_info = node_dict.pop("extra_info")
-    extra_info_str = ""
-    if extra_info is not None:
-        extra_info_str = json.dumps(extra_info)
-    node_dict["extra_info"] = extra_info_str
-
-    # json-serialize the node_info
-    node_info = node_dict.pop("node_info")
-    node_info_str = ""
-    if node_info is not None:
-        node_info_str = json.dumps(node_info)
-    node_dict["node_info"] = node_info_str
-
-    # json-serialize the relationships
-    relationships = node_dict.pop("relationships")
-    relationships_str = ""
-    if relationships is not None:
-        relationships_str = json.dumps(relationships)
-    node_dict["relationships"] = relationships_str
-
-    ref_doc_id = node.ref_doc_id
-    if ref_doc_id is not None:
-        node_dict["ref_doc_id"] = ref_doc_id
-    return node_dict
-
-
 def _add_node(
     client: Any, node: Node, class_prefix: str, batch: Optional[Any] = None
 ) -> str:
     """Add node."""
-    node_dict = _node_to_dict(node)
-    vector = node.embedding
+    metadata = {}
+    metadata["text"] = node.text or ""
 
-    # TODO: account for existing nodes that are stored
-    node_id = get_new_id(set())
+    additional_metadata = node_to_metadata_dict(node)
+    metadata.update(additional_metadata)
+
+    # NOTE: important to set this after additional_metadata to override.
+    #       be default, "doc_id" refers to source doc id, but for legacy reason
+    #       we use "doc_id" to refer to node id in weaviate.
+    metadata["doc_id"] = node.get_doc_id()
+
+    vector = node.embedding
+    node_id = node.get_doc_id()
     class_name = _class_name(class_prefix)
 
     # if batch object is provided (via a context manager), use that instead
     if batch is not None:
-        batch.add_data_object(node_dict, class_name, node_id, vector)
+        batch.add_data_object(metadata, class_name, node_id, vector)
     else:
-        client.batch.add_data_object(node_dict, class_name, node_id, vector)
+        client.batch.add_data_object(metadata, class_name, node_id, vector)
 
     return node_id
 
 
 def delete_document(client: Any, ref_doc_id: str, class_prefix: str) -> None:
     """Delete entry."""
     validate_client(client)
```

### Comparing `llama_index-0.6.5/llama_index/readers/weaviate/reader.py` & `llama_index-0.6.6/llama_index/readers/weaviate/reader.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/weaviate/utils.py` & `llama_index-0.6.6/llama_index/readers/weaviate/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/web.py` & `llama_index-0.6.6/llama_index/readers/web.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/wikipedia.py` & `llama_index-0.6.6/llama_index/readers/wikipedia.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/readers/youtube_transcript.py` & `llama_index-0.6.6/llama_index/readers/youtube_transcript.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/response/notebook_utils.py` & `llama_index-0.6.6/llama_index/response/notebook_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/response/pprint_utils.py` & `llama_index-0.6.6/llama_index/response/pprint_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/response/schema.py` & `llama_index-0.6.6/llama_index/response/schema.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/retrievers/__init__.py` & `llama_index-0.6.6/llama_index/retrievers/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,30 @@
-from llama_index.indices.vector_store.retrievers import VectorIndexRetriever
+from llama_index.indices.base_retriever import BaseRetriever
+from llama_index.indices.empty.retrievers import EmptyIndexRetriever
+from llama_index.indices.keyword_table.retrievers import KeywordTableSimpleRetriever
+from llama_index.indices.knowledge_graph.retrievers import KGTableRetriever
 from llama_index.indices.list.retrievers import (
     ListIndexEmbeddingRetriever,
     ListIndexRetriever,
 )
-from llama_index.indices.knowledge_graph.retrievers import KGTableRetriever
-from llama_index.indices.empty.retrievers import EmptyIndexRetriever
 from llama_index.indices.tree.all_leaf_retriever import TreeAllLeafRetriever
 from llama_index.indices.tree.select_leaf_embedding_retriever import (
     TreeSelectLeafEmbeddingRetriever,
 )
 from llama_index.indices.tree.select_leaf_retriever import TreeSelectLeafRetriever
 from llama_index.indices.tree.tree_root_retriever import TreeRootRetriever
+from llama_index.indices.vector_store.retrievers import (
+    VectorIndexAutoRetriever,
+    VectorIndexRetriever,
+)
 from llama_index.retrievers.transform_retriever import TransformRetriever
-from llama_index.indices.base_retriever import BaseRetriever
-from llama_index.indices.keyword_table.retrievers import KeywordTableSimpleRetriever
 
 __all__ = [
     "VectorIndexRetriever",
+    "VectorIndexAutoRetriever",
     "ListIndexEmbeddingRetriever",
     "ListIndexRetriever",
     "KGTableRetriever",
     "EmptyIndexRetriever",
     "TreeAllLeafRetriever",
     "TreeSelectLeafEmbeddingRetriever",
     "TreeSelectLeafRetriever",
```

### Comparing `llama_index-0.6.5/llama_index/retrievers/transform_retriever.py` & `llama_index-0.6.6/llama_index/retrievers/transform_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/schema.py` & `llama_index-0.6.6/llama_index/schema.py`

 * *Files 26% similar despite different names*

```diff
@@ -5,14 +5,26 @@
 from typing import Any, Dict, List, Optional
 
 from dataclasses_json import DataClassJsonMixin
 
 from llama_index.utils import get_new_id
 
 
+def _validate_is_flat_dict(metadata_dict: dict) -> None:
+    """
+    Validate that metadata dict is flat,
+    and key is str, and value is one of (str, int, float).
+    """
+    for key, val in metadata_dict.items():
+        if not isinstance(key, str):
+            raise ValueError("Metadata key must be str!")
+        if not isinstance(val, (str, int, float)):
+            raise ValueError("Value must be one of (str, int, float)")
+
+
 @dataclass
 class BaseDocument(DataClassJsonMixin):
     """Base document.
 
     Generic abstract interfaces that captures both index structs
     as well as documents.
 
@@ -20,25 +32,35 @@
 
     # TODO: consolidate fields from Document/IndexStruct into base class
     text: Optional[str] = None
     doc_id: Optional[str] = None
     embedding: Optional[List[float]] = None
     doc_hash: Optional[str] = None
 
-    # extra fields
+    """"
+    metadata fields
+    - injected as part of the text shown to LLMs as context
+    - used by vector DBs for metadata filtering
+
+    This must be a flat dictionary, 
+    and only uses str keys, and (str, int, float) values.
+    """
     extra_info: Optional[Dict[str, Any]] = None
 
     def __post_init__(self) -> None:
         """Post init."""
         # assign doc_id if not set
         if self.doc_id is None:
             self.doc_id = get_new_id(set())
         if self.doc_hash is None:
             self.doc_hash = self._generate_doc_hash()
 
+        if self.extra_info is not None:
+            _validate_is_flat_dict(self.extra_info)
+
     def _generate_doc_hash(self) -> str:
         """Generate a hash to represent the document."""
         doc_identity = str(self.text) + str(self.extra_info)
         return sha256(doc_identity.encode("utf-8", "surrogatepass")).hexdigest()
 
     @classmethod
     @abstractmethod
```

### Comparing `llama_index-0.6.5/llama_index/selectors/llm_selectors.py` & `llama_index-0.6.6/llama_index/selectors/llm_selectors.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/selectors/prompts.py` & `llama_index-0.6.6/llama_index/selectors/prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/selectors/types.py` & `llama_index-0.6.6/llama_index/selectors/types.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/__init__.py` & `llama_index-0.6.6/llama_index/storage/docstore/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/keyval_docstore.py` & `llama_index-0.6.6/llama_index/storage/docstore/keyval_docstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/mongo_docstore.py` & `llama_index-0.6.6/llama_index/storage/docstore/mongo_docstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/registry.py` & `llama_index-0.6.6/llama_index/storage/docstore/registry.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/simple_docstore.py` & `llama_index-0.6.6/llama_index/storage/docstore/simple_docstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/types.py` & `llama_index-0.6.6/llama_index/storage/docstore/types.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/docstore/utils.py` & `llama_index-0.6.6/llama_index/storage/docstore/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/index_store/keyval_index_store.py` & `llama_index-0.6.6/llama_index/storage/index_store/keyval_index_store.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/index_store/mongo_index_store.py` & `llama_index-0.6.6/llama_index/storage/index_store/mongo_index_store.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/index_store/simple_index_store.py` & `llama_index-0.6.6/llama_index/storage/index_store/simple_index_store.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/index_store/types.py` & `llama_index-0.6.6/llama_index/storage/index_store/types.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/index_store/utils.py` & `llama_index-0.6.6/llama_index/storage/index_store/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/kvstore/mongodb_kvstore.py` & `llama_index-0.6.6/llama_index/storage/kvstore/mongodb_kvstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/kvstore/simple_kvstore.py` & `llama_index-0.6.6/llama_index/storage/kvstore/simple_kvstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/kvstore/types.py` & `llama_index-0.6.6/llama_index/storage/kvstore/types.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/storage/storage_context.py` & `llama_index-0.6.6/llama_index/storage/storage_context.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/token_counter/mock_chain_wrapper.py` & `llama_index-0.6.6/llama_index/token_counter/mock_chain_wrapper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/token_counter/mock_embed_model.py` & `llama_index-0.6.6/llama_index/token_counter/mock_embed_model.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/token_counter/token_counter.py` & `llama_index-0.6.6/llama_index/token_counter/token_counter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/token_counter/utils.py` & `llama_index-0.6.6/llama_index/token_counter/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/tools/query_engine.py` & `llama_index-0.6.6/llama_index/tools/query_engine.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/tts/bark.py` & `llama_index-0.6.6/llama_index/tts/bark.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/tts/base.py` & `llama_index-0.6.6/llama_index/tts/base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/tts/elevenlabs.py` & `llama_index-0.6.6/llama_index/tts/elevenlabs.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/utils.py` & `llama_index-0.6.6/llama_index/utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/vector_stores/__init__.py` & `llama_index-0.6.6/llama_index/vector_stores/__init__.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/vector_stores/chatgpt_plugin.py` & `llama_index-0.6.6/llama_index/vector_stores/chatgpt_plugin.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,20 +3,20 @@
 import os
 from typing import Any, Dict, List, Optional
 
 import requests
 from requests.adapters import HTTPAdapter, Retry
 from tqdm.auto import tqdm
 
-from llama_index.data_structs.node import Node, DocumentRelationship
+from llama_index.data_structs.node import DocumentRelationship, Node
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
 
 
 def convert_docs_to_json(embedding_results: List[NodeWithEmbedding]) -> List[Dict]:
     """Convert docs to JSON."""
     docs = []
     for embedding_result in embedding_results:
@@ -112,16 +112,20 @@
             headers=headers,
             json={"ids": [doc_id]},
         )
 
     def query(
         self,
         query: VectorStoreQuery,
+        **kwargs: Any,
     ) -> VectorStoreQueryResult:
         """Get nodes for response."""
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for ChatGPT Plugin yet.")
+
         if query.query_str is None:
             raise ValueError("query_str must be provided")
         headers = {"Authorization": f"Bearer {self._bearer_token}"}
         # TODO: add metadata filter
         queries = [{"query": query.query_str, "top_k": query.similarity_top_k}]
         res = requests.post(
             f"{self._endpoint_url}/query", headers=headers, json={"queries": queries}
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/chroma.py` & `llama_index-0.6.6/llama_index/vector_stores/faiss.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,132 +1,166 @@
-"""Chroma vector store."""
+"""Faiss Vector store index.
+
+An index that that is built on top of an existing vector store.
+
+"""
+
 import logging
-import math
+import os
 from typing import Any, List, cast
 
-from llama_index.data_structs.node import DocumentRelationship, Node
-from llama_index.utils import truncate_text
+import numpy as np
+
 from llama_index.vector_stores.types import (
+    DEFAULT_PERSIST_DIR,
+    DEFAULT_PERSIST_FNAME,
     NodeWithEmbedding,
     VectorStore,
     VectorStoreQuery,
     VectorStoreQueryResult,
 )
 
-logger = logging.getLogger(__name__)
+logger = logging.getLogger()
 
 
-class ChromaVectorStore(VectorStore):
-    """Chroma vector store.
+class FaissVectorStore(VectorStore):
+    """Faiss Vector Store.
 
-    In this vector store, embeddings are stored within a ChromaDB collection.
+    Embeddings are stored within a Faiss index.
 
-    During query time, the index uses ChromaDB to query for the top
-    k most similar nodes.
+    During query time, the index uses Faiss to query for the top
+    k embeddings, and returns the corresponding indices.
 
     Args:
-        chroma_collection (chromadb.api.models.Collection.Collection):
-            ChromaDB collection instance
+        faiss_index (faiss.Index): Faiss index instance
 
     """
 
-    stores_text: bool = True
+    stores_text: bool = False
 
-    def __init__(self, chroma_collection: Any, **kwargs: Any) -> None:
-        """Init params."""
-        import_err_msg = (
-            "`chromadb` package not found, please run `pip install chromadb`"
-        )
+    def __init__(
+        self,
+        faiss_index: Any,
+    ) -> None:
+        """Initialize params."""
+        import_err_msg = """
+            `faiss` package not found. For instructions on
+            how to install `faiss` please visit
+            https://github.com/facebookresearch/faiss/wiki/Installing-Faiss
+        """
         try:
-            import chromadb  # noqa: F401
+            import faiss  # noqa: F401
         except ImportError:
             raise ImportError(import_err_msg)
-        from chromadb.api.models.Collection import Collection
 
-        self._collection = cast(Collection, chroma_collection)
+        self._faiss_index = cast(faiss.Index, faiss_index)
 
-    def add(self, embedding_results: List[NodeWithEmbedding]) -> List[str]:
+    @classmethod
+    def from_persist_dir(
+        cls,
+        persist_dir: str = DEFAULT_PERSIST_DIR,
+    ) -> "FaissVectorStore":
+        persist_path = os.path.join(persist_dir, DEFAULT_PERSIST_FNAME)
+        return cls.from_persist_path(persist_path=persist_path)
+
+    @classmethod
+    def from_persist_path(
+        cls,
+        persist_path: str,
+    ) -> "FaissVectorStore":
+        import faiss
+
+        if not os.path.exists(persist_path):
+            raise ValueError(f"No existing {__name__} found at {persist_path}.")
+
+        logger.info(f"Loading {__name__} from {persist_path}.")
+        faiss_index = faiss.read_index(persist_path)
+        return cls(faiss_index=faiss_index)
+
+    def add(
+        self,
+        embedding_results: List[NodeWithEmbedding],
+    ) -> List[str]:
         """Add embedding results to index.
 
+        NOTE: in the Faiss vector store, we do not store text in Faiss.
+
         Args
             embedding_results: List[NodeWithEmbedding]: list of embedding results
 
         """
-        if not self._collection:
-            raise ValueError("Collection not initialized")
-
-        embeddings = []
-        metadatas = []
-        ids = []
-        documents = []
+        new_ids = []
         for result in embedding_results:
-            embeddings.append(result.embedding)
-            extra_info = result.node.extra_info or {}
-            metadatas.append({**extra_info, **{"document_id": result.ref_doc_id}})
-            ids.append(result.id)
-            documents.append(result.node.get_text())
-
-        self._collection.add(
-            embeddings=embeddings,
-            ids=ids,
-            metadatas=metadatas,
-            documents=documents,
-        )
-        return ids
+            text_embedding = result.embedding
+            text_embedding_np = np.array(text_embedding, dtype="float32")[np.newaxis, :]
+            new_id = str(self._faiss_index.ntotal)
+            self._faiss_index.add(text_embedding_np)
+            new_ids.append(new_id)
+        return new_ids
+
+    @property
+    def client(self) -> Any:
+        """Return the faiss index."""
+        return self._faiss_index
+
+    def persist(
+        self,
+        persist_path: str = os.path.join(DEFAULT_PERSIST_DIR, DEFAULT_PERSIST_FNAME),
+    ) -> None:
+        """Save to file.
+
+        This method saves the vector store to disk.
 
-    def delete(self, doc_id: str, **delete_kwargs: Any) -> None:
+        Args:
+            persist_path (str): The save_path of the file.
+
+        """
+        import faiss
+
+        dirpath = os.path.dirname(persist_path)
+        if not os.path.exists(dirpath):
+            os.makedirs(dirpath)
+
+        faiss.write_index(self._faiss_index, persist_path)
+
+    def delete(
+        self,
+        doc_id: str,
+        **delete_kwargs: Any,
+    ) -> None:
         """Delete a document.
 
         Args:
             doc_id (str): document id
 
         """
-        self._collection.delete(where={"document_id": doc_id})
+        raise NotImplementedError("Delete not yet implemented for Faiss index.")
 
-    @property
-    def client(self) -> Any:
-        """Return client."""
-        return self._collection
-
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(
+        self,
+        query: VectorStoreQuery,
+        **kwargs: Any,
+    ) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query_embedding (List[float]): query embedding
             similarity_top_k (int): top k most similar nodes
 
         """
-        results = self._collection.query(
-            query_embeddings=query.query_embedding, n_results=query.similarity_top_k
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for Faiss yet.")
+
+        query_embedding = cast(List[float], query.query_embedding)
+        query_embedding_np = np.array(query_embedding, dtype="float32")[np.newaxis, :]
+        dists, indices = self._faiss_index.search(
+            query_embedding_np, query.similarity_top_k
         )
+        dists = [d for d in dists[0]]
+        # if empty, then return an empty response
+        if len(indices) == 0:
+            return VectorStoreQueryResult(similarities=[], ids=[])
 
-        logger.debug(f"> Top {len(results['documents'])} nodes:")
-        nodes = []
-        similarities = []
-        ids = []
-        for result in zip(
-            results["ids"][0],
-            results["documents"][0],
-            results["metadatas"][0],
-            results["distances"][0],
-        ):
-            node_id = result[0]
-            node = Node(
-                doc_id=node_id,
-                text=result[1],
-                extra_info=result[2],
-                relationships={
-                    DocumentRelationship.SOURCE: result[2]["document_id"],
-                },
-            )
-            nodes.append(node)
-
-            similarity_score = 1.0 - math.exp(-result[3])
-            similarities.append(similarity_score)
-
-            logger.debug(
-                f"> [Node {result[0]}] [Similarity score: {similarity_score}] "
-                f"{truncate_text(str(result[1]), 100)}"
-            )
-            ids.append(node_id)
+        # returned dimension is 1 x k
+        node_idxs = list([str(i) for i in indices[0]])
 
-        return VectorStoreQueryResult(nodes=nodes, similarities=similarities, ids=ids)
+        return VectorStoreQueryResult(similarities=dists, ids=node_idxs)
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/deeplake.py` & `llama_index-0.6.6/llama_index/vector_stores/deeplake.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 An index that is built within DeepLake.
 
 """
 import logging
 from typing import Any, Dict, List, Optional, cast
 
 import numpy as np
+
 from llama_index.indices.query.embedding_utils import get_top_k_embeddings
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
     VectorStoreQuery,
     VectorStoreQueryResult,
 )
@@ -213,21 +214,24 @@
         with self.ds:
             for id in sorted(ids)[::-1]:
                 self.ds.pop(id)
 
             self.ds.commit(f"deleted {len(ids)} samples", allow_empty=True)
             self.ds.summary()
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query_embedding (List[float]): query embedding
             similarity_top_k (int): top k most similar nodes
         """
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for DeepLake yet.")
+
         query_embedding = cast(List[float], query.query_embedding)
         embeddings = self.ds.embedding.numpy(fetch_chunks=True)
         embedding_ids = self.ds.ids.numpy(fetch_chunks=True)
         embedding_ids = [str(embedding_id[0]) for embedding_id in embedding_ids]
 
         top_similarities, top_ids = get_top_k_embeddings(
             query_embedding,
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/lancedb.py` & `llama_index-0.6.6/llama_index/vector_stores/lancedb.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 """LanceDB vector store."""
 from typing import Any, List, Optional
 
 from llama_index.data_structs.node import DocumentRelationship, Node
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
 
 
 class LanceDBVectorStore(VectorStore):
     """The LanceDB Vector Store.
 
     Stores text and embeddings in LanceDB. The vector store will open an existing
@@ -95,16 +95,20 @@
 
         """
         raise NotImplementedError("Delete not yet implemented for LanceDB.")
 
     def query(
         self,
         query: VectorStoreQuery,
+        **kwargs: Any,
     ) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes."""
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for LanceDB yet.")
+
         table = self.connection.open_table(self.table_name)
         lance_query = (
             table.search(query.query_embedding)
             .limit(query.similarity_top_k)
             .nprobes(self.nprobes)
         )
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/milvus.py` & `llama_index-0.6.6/llama_index/vector_stores/milvus.py`

 * *Files 2% similar despite different names*

```diff
@@ -363,15 +363,15 @@
             ids = ['"' + entry + '"' for entry in ids]
             self.collection.delete(f"id in [{','.join(ids)}]")
             logger.debug(f"Successfully deleted embedding with doc_id: {doc_ids}")
         except MilvusException as e:
             logger.debug(f"Unsuccessfully deleted embedding with doc_id: {doc_ids}")
             raise e
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query_embedding (List[float]): query embedding
             similarity_top_k (int): top k most similar nodes
             doc_ids (Optional[List[str]]): list of doc_ids to filter by
         """
@@ -379,14 +379,17 @@
 
         if self.collection is None:
             raise ValueError("Milvus instance not initialized.")
 
         if query.mode != VectorStoreQueryMode.DEFAULT:
             raise ValueError(f"Milvus does not support {query.mode} yet.")
 
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for Milvus yet.")
+
         expr: Optional[str] = None
         if query.doc_ids is not None and len(query.doc_ids) != 0:
             expr_list = ['"' + entry + '"' for entry in query.doc_ids]
             expr = f"doc_id in [{','.join(expr_list)}]"
 
         try:
             res = self.collection.search(
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/myscale.py` & `llama_index-0.6.6/llama_index/vector_stores/myscale.py`

 * *Files 2% similar despite different names*

```diff
@@ -98,15 +98,15 @@
 
         # schema column name, type, and construct format method
         self.column_config: Dict = {
             "id": {"type": "String", "extract_func": lambda x: x.id},
             "doc_id": {"type": "String", "extract_func": lambda x: x.ref_doc_id},
             "text": {
                 "type": "String",
-                "extract_func": lambda x: escape_str(x.node.get_text()),
+                "extract_func": lambda x: escape_str(x.node.text or ""),
             },
             "vector": {
                 "type": "Array(Float32)",
                 "extract_func": lambda x: format_list_to_string(x.embedding),
             },
             "node_info": {
                 "type": "JSON",
@@ -205,21 +205,25 @@
 
     def drop(self) -> None:
         """Drop MyScale Index and table"""
         self._client.command(
             f"DROP TABLE IF EXISTS {self.config.database}.{self.config.table}"
         )
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query (VectorStoreQuery): query
 
         """
+        if query.filters is not None:
+            raise ValueError(
+                "Metadata filters not implemented for SimpleVectorStore yet."
+            )
 
         query_embedding = cast(List[float], query.query_embedding)
         where_str = (
             f"doc_id in {format_list_to_string(query.doc_ids)}"
             if query.doc_ids
             else None
         )
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/opensearch.py` & `llama_index-0.6.6/llama_index/vector_stores/opensearch.py`

 * *Files 5% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 import json
 from typing import Any, Dict, List, Optional, cast
 
 from llama_index.data_structs import Node
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
 
 
 class OpensearchVectorClient:
     """Object encapsulating an Opensearch index that has vector search enabled.
 
     If the index does not yet exist, it is created during init.
@@ -196,17 +196,20 @@
 
         Args:
             doc_id (str): document id
 
         """
         self._client.delete_doc_id(doc_id)
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query_embedding (List[float]): query embedding
             similarity_top_k (int): top k most similar nodes
 
         """
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for OpenSearch yet.")
+
         query_embedding = cast(List[float], query.query_embedding)
         return self._client.do_approx_knn(query_embedding, query.similarity_top_k)
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/pinecone.py` & `llama_index-0.6.6/llama_index/vector_stores/pinecone.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,39 +4,31 @@
 
 """
 
 import logging
 import os
 from collections import Counter
 from functools import partial
-from typing import Any, Callable, Dict, List, Optional, cast
+from typing import Any, Callable, Dict, List, Optional, Tuple, cast
 
 from llama_index.data_structs.node import DocumentRelationship, Node
 from llama_index.vector_stores.types import (
+    MetadataFilters,
     NodeWithEmbedding,
     VectorStore,
     VectorStoreQuery,
     VectorStoreQueryMode,
     VectorStoreQueryResult,
 )
+from llama_index.vector_stores.utils import metadata_dict_to_node, node_to_metadata_dict
 
 _logger = logging.getLogger(__name__)
 
 
-def get_metadata_from_node_info(
-    node_info: Dict[str, Any], field_prefix: str
-) -> Dict[str, Any]:
-    """Get metadata from node extra info."""
-    metadata = {}
-    for key, value in node_info.items():
-        metadata[field_prefix + "_" + key] = value
-    return metadata
-
-
-def get_node_info_from_metadata(
+def _get_node_info_from_metadata(
     metadata: Dict[str, Any], field_prefix: str
 ) -> Dict[str, Any]:
     """Get node extra info from metadata."""
     node_extra_info = {}
     for key, value in metadata.items():
         if key.startswith(field_prefix + "_"):
             node_extra_info[key.replace(field_prefix + "_", "")] = value
@@ -95,49 +87,56 @@
         padding=True,
         truncation=True,
         max_length=512,
     )
     return tokenizer
 
 
+def _to_pinecone_filter(standard_filters: MetadataFilters) -> dict:
+    """Convert from standard dataclass to pinecone filter dict."""
+    filters = {}
+    for filter in standard_filters.filters:
+        filters[filter.key] = filter.value
+    return filters
+
+
+def _legacy_metadata_dict_to_node(metadata: Dict[str, Any]) -> Tuple[dict, dict, dict]:
+    extra_info = _get_node_info_from_metadata(metadata, "extra_info")
+    node_info = _get_node_info_from_metadata(metadata, "node_info")
+    doc_id = metadata["doc_id"]
+    relationships = {DocumentRelationship.SOURCE: doc_id}
+    return extra_info, node_info, relationships
+
+
 class PineconeVectorStore(VectorStore):
     """Pinecone Vector Store.
 
     In this vector store, embeddings and docs are stored within a
     Pinecone index.
 
     During query time, the index uses Pinecone to query for the top
     k most similar nodes.
 
     Args:
         pinecone_index (Optional[pinecone.Index]): Pinecone index instance
-        pinecone_kwargs (Optional[Dict]): kwargs to pass to Pinecone index.
-            NOTE: deprecated. If specified, then insert_kwargs, query_kwargs,
-            and delete_kwargs cannot be specified.
         insert_kwargs (Optional[Dict]): insert kwargs during `upsert` call.
-        query_kwargs (Optional[Dict]): query kwargs during `query` call.
-        delete_kwargs (Optional[Dict]): delete kwargs during `delete` call.
         add_sparse_vector (bool): whether to add sparse vector to index.
         tokenizer (Optional[Callable]): tokenizer to use to generate sparse
 
     """
 
     stores_text: bool = True
 
     def __init__(
         self,
         pinecone_index: Optional[Any] = None,
         index_name: Optional[str] = None,
         environment: Optional[str] = None,
         namespace: Optional[str] = None,
-        metadata_filters: Optional[Dict[str, Any]] = None,
-        pinecone_kwargs: Optional[Dict] = None,
         insert_kwargs: Optional[Dict] = None,
-        query_kwargs: Optional[Dict] = None,
-        delete_kwargs: Optional[Dict] = None,
         add_sparse_vector: bool = False,
         tokenizer: Optional[Callable] = None,
         **kwargs: Any,
     ) -> None:
         """Initialize params."""
         import_err_msg = (
             "`pinecone` package not found, please run `pip install pinecone-client`"
@@ -163,29 +162,15 @@
                     "Must specify index_name and environment "
                     "if not directly passing in client."
                 )
 
             pinecone.init(environment=environment)
             self._pinecone_index = pinecone.Index(index_name)
 
-        self._metadata_filters = metadata_filters or {}
-        self._pinecone_kwargs = pinecone_kwargs or {}
-        if pinecone_kwargs and (insert_kwargs or query_kwargs or delete_kwargs):
-            raise ValueError(
-                "pinecone_kwargs cannot be specified if insert_kwargs, "
-                "query_kwargs, or delete_kwargs are specified."
-            )
-        elif pinecone_kwargs:
-            self._insert_kwargs = pinecone_kwargs
-            self._query_kwargs = pinecone_kwargs
-            self._delete_kwargs = pinecone_kwargs
-        else:
-            self._insert_kwargs = insert_kwargs or {}
-            self._query_kwargs = query_kwargs or {}
-            self._delete_kwargs = delete_kwargs or {}
+        self._insert_kwargs = insert_kwargs or {}
 
         self._add_sparse_vector = add_sparse_vector
         if tokenizer is None:
             tokenizer = get_default_tokenizer()
         self._tokenizer = tokenizer
 
     def add(
@@ -200,75 +185,53 @@
         """
         ids = []
         for result in embedding_results:
             node_id = result.id
             node = result.node
 
             metadata = {
-                "text": node.get_text(),
-                # NOTE: this is the reference to source doc
-                "doc_id": node.ref_doc_id,
+                "text": node.text or "",
                 "id": node_id,
             }
-            if node.extra_info:
-                # TODO: check if overlap with default metadata keys
-                metadata.update(
-                    get_metadata_from_node_info(node.extra_info, "extra_info")
-                )
-            if node.node_info:
-                # TODO: check if overlap with default metadata keys
-                metadata.update(
-                    get_metadata_from_node_info(node.node_info, "node_info")
-                )
-            # if additional metadata keys overlap with the default keys,
-            # then throw an error
-            intersecting_keys = set(metadata.keys()).intersection(
-                self._metadata_filters.keys()
-            )
-            if intersecting_keys:
-                raise ValueError(
-                    "metadata_filters keys overlap with default "
-                    f"metadata keys: {intersecting_keys}"
-                )
-            metadata.update(self._metadata_filters)
+
+            additional_metadata = node_to_metadata_dict(node)
+            metadata.update(additional_metadata)
 
             entry = {
                 "id": node_id,
                 "values": result.embedding,
                 "metadata": metadata,
             }
             if self._add_sparse_vector:
                 sparse_vector = generate_sparse_vectors(
                     [node.get_text()], self._tokenizer
                 )[0]
                 entry.update({"sparse_values": sparse_vector})
             self._pinecone_index.upsert(
-                [entry], namespace=self._namespace, **self._pinecone_kwargs
+                [entry], namespace=self._namespace, **self._insert_kwargs
             )
             ids.append(node_id)
         return ids
 
     def delete(self, doc_id: str, **delete_kwargs: Any) -> None:
         """Delete a document.
 
         Args:
             doc_id (str): document id
 
         """
         # delete by filtering on the doc_id metadata
-        self._pinecone_index.delete(
-            filter={"doc_id": {"$eq": doc_id}}, **self._pinecone_kwargs
-        )
+        self._pinecone_index.delete(filter={"doc_id": {"$eq": doc_id}}, **delete_kwargs)
 
     @property
     def client(self) -> Any:
         """Return Pinecone client."""
         return self._pinecone_index
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query_embedding (List[float]): query embedding
             similarity_top_k (int): top k most similar nodes
 
         """
@@ -289,41 +252,61 @@
 
         query_embedding = None
         if query.mode in (VectorStoreQueryMode.DEFAULT, VectorStoreQueryMode.HYBRID):
             query_embedding = cast(List[float], query.query_embedding)
             if query.alpha is not None:
                 query_embedding = [v * query.alpha for v in query_embedding]
 
+        if query.filters is not None:
+            if "filter" in kwargs:
+                raise ValueError(
+                    "Cannot specify filter via both query and kwargs. "
+                    "Use kwargs only for pinecone specific items that are "
+                    "not supported via the generic query interface."
+                )
+            filter = _to_pinecone_filter(query.filters)
+        else:
+            filter = kwargs.pop("filter", {})
+
         response = self._pinecone_index.query(
             vector=query_embedding,
             sparse_vector=sparse_vector,
             top_k=query.similarity_top_k,
             include_values=True,
             include_metadata=True,
             namespace=self._namespace,
-            filter=self._metadata_filters,
-            **self._pinecone_kwargs,
+            filter=filter,
+            **kwargs,
         )
 
         top_k_nodes = []
         top_k_ids = []
         top_k_scores = []
         for match in response.matches:
             text = match.metadata["text"]
-            extra_info = get_node_info_from_metadata(match.metadata, "extra_info")
-            node_info = get_node_info_from_metadata(match.metadata, "node_info")
-            doc_id = match.metadata["doc_id"]
             id = match.metadata["id"]
+            try:
+                extra_info, node_info, relationships = metadata_dict_to_node(
+                    match.metadata
+                )
+            except Exception:
+                _logger.debug(
+                    "Failed to parse Node metadata, fallback to legacy logic."
+                )
+                # NOTE: deprecated legacy logic for backward compatibility
+                extra_info, node_info, relationships = _legacy_metadata_dict_to_node(
+                    match.metadata
+                )
 
             node = Node(
                 text=text,
+                doc_id=id,
                 extra_info=extra_info,
                 node_info=node_info,
-                doc_id=id,
-                relationships={DocumentRelationship.SOURCE: doc_id},
+                relationships=relationships,
             )
             top_k_ids.append(match.id)
             top_k_nodes.append(node)
             top_k_scores.append(match.score)
 
         return VectorStoreQueryResult(
             nodes=top_k_nodes, similarities=top_k_scores, ids=top_k_ids
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/qdrant.py` & `llama_index-0.6.6/llama_index/vector_stores/qdrant.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,27 +1,37 @@
 """Qdrant vector store index.
 
 An index that is built on top of an existing Qdrant collection.
 
 """
 import logging
-from typing import Any, List, Optional, cast
+from typing import Any, List, Optional, Tuple, cast
 
 from llama_index.data_structs.node import DocumentRelationship, Node
 from llama_index.utils import iter_batch
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
+from llama_index.vector_stores.utils import metadata_dict_to_node, node_to_metadata_dict
 
 logger = logging.getLogger(__name__)
 
 
+def _legacy_metadata_dict_to_node(payload: Any) -> Tuple[dict, dict, dict]:
+    extra_info = payload.get("extra_info", {})
+    relationships = {
+        DocumentRelationship.SOURCE: payload.get("doc_id", "None"),
+    }
+    node_info: dict = {}
+    return extra_info, node_info, relationships
+
+
 class QdrantVectorStore(VectorStore):
     """Qdrant Vector Store.
 
     In this vector store, embeddings and docs are stored within a
     Qdrant collection.
 
     During query time, the index uses Qdrant to query for the top
@@ -72,24 +82,25 @@
 
         ids = []
         for result_batch in iter_batch(embedding_results, self._batch_size):
             node_ids = []
             vectors = []
             payloads = []
             for result in result_batch:
+                assert isinstance(result, NodeWithEmbedding)
                 node_ids.append(result.id)
                 vectors.append(result.embedding)
                 node = result.node
-                payloads.append(
-                    {
-                        "doc_id": result.ref_doc_id,
-                        "text": node.get_text(),
-                        "extra_info": node.extra_info,
-                    }
-                )
+
+                metadata = {}
+                metadata["text"] = node.text or ""
+                additional_metadata = node_to_metadata_dict(node)
+                metadata.update(additional_metadata)
+
+                payloads.append(metadata)
 
             self._client.upsert(
                 collection_name=self._collection_name,
                 points=rest.Batch.construct(
                     ids=node_ids,
                     vectors=vectors,
                     payloads=payloads,
@@ -146,21 +157,22 @@
         except (RpcError, UnexpectedResponse, ValueError):
             return False
         return True
 
     def query(
         self,
         query: VectorStoreQuery,
+        **kwargs: Any,
     ) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes.
 
         Args:
             query (VectorStoreQuery): query
         """
-        from qdrant_client.http.models import Payload, Filter
+        from qdrant_client.http.models import Filter, Payload
 
         query_embedding = cast(List[float], query.query_embedding)
 
         response = self._client.search(
             collection_name=self._collection_name,
             query_vector=query_embedding,
             limit=cast(int, query.similarity_top_k),
@@ -170,41 +182,48 @@
         logger.debug(f"> Top {len(response)} nodes:")
 
         nodes = []
         similarities = []
         ids = []
         for point in response:
             payload = cast(Payload, point.payload)
+            try:
+                extra_info, node_info, relationships = metadata_dict_to_node(payload)
+            except Exception:
+                logger.debug("Failed to parse Node metadata, fallback to legacy logic.")
+                extra_info, node_info, relationships = _legacy_metadata_dict_to_node(
+                    payload
+                )
+
             node = Node(
                 doc_id=str(point.id),
                 text=payload.get("text"),
-                extra_info=payload.get("extra_info"),
-                relationships={
-                    DocumentRelationship.SOURCE: payload.get("doc_id", "None"),
-                },
+                extra_info=extra_info,
+                node_info=node_info,
+                relationships=relationships,
             )
             nodes.append(node)
             similarities.append(point.score)
             ids.append(str(point.id))
 
         return VectorStoreQueryResult(nodes=nodes, similarities=similarities, ids=ids)
 
     def _build_query_filter(self, query: VectorStoreQuery) -> Optional[Any]:
         if not query.doc_ids and not query.query_str:
             return None
 
-        from qdrant_client.http.models import (
-            FieldCondition,
-            Filter,
-            MatchAny,
-        )
+        from qdrant_client.http.models import FieldCondition, Filter, MatchAny
 
         must_conditions = []
 
         if query.doc_ids:
             must_conditions.append(
                 FieldCondition(
                     key="doc_id",
                     match=MatchAny(any=[doc_id for doc_id in query.doc_ids]),
                 )
             )
+        # TODO: implement this
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for Qdrant yet.")
+
         return Filter(must=must_conditions)
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/redis.py` & `llama_index-0.6.6/llama_index/vector_stores/redis.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 )
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
     VectorStoreQuery,
     VectorStoreQueryResult,
 )
+from llama_index.vector_stores.utils import node_to_metadata_dict
 
 _logger = logging.getLogger(__name__)
 
 
 if TYPE_CHECKING:
     from redis.client import Redis as RedisType
     from redis.commands.search.field import VectorField
@@ -116,44 +117,41 @@
 
         Returns:
             List[str]: List of ids of the documents added to the index.
 
         Raises:
             ValueError: If the index already exists and overwrite is False.
         """
-
-        # check index exists, call once to avoid calling multiple times
-        index_exists = self._index_exists()
-        if index_exists and self._overwrite:
-            self.delete_index()
-
-        elif index_exists and not self._overwrite:
-            raise ValueError("Index already exists and overwrite is False.")
-
-        else:  # index does not exist, create it
-            # get vector dim from embedding results if index does not exist
-            # as it will be created from the embedding result attributes.
-            self._index_args["dims"] = len(embedding_results[0].embedding)
+        # check to see if empty document list was passed
+        if len(embedding_results) == 0:
+            return []
+
+        # set vector dim for creation if index doesn't exist
+        self._index_args["dims"] = len(embedding_results[0].embedding)
+
+        if self._index_exists():
+            if self._overwrite:
+                self.delete_index()
+                self._create_index()
+            else:
+                logging.info(f"Adding document to existing index {self._index_name}")
+        else:
             self._create_index()
 
         ids = []
         for result in embedding_results:
-            # Add extra info and node info to the index
-            # cast types to satisfy mypy
-            node_info = cast_metadata_types(result.node.node_info)
-            extra_info = cast_metadata_types(result.node.extra_info)
-
             mapping = {
                 "id": result.id,
                 "doc_id": result.ref_doc_id,
                 "text": result.node.get_text(),
                 self._vector_key: array_to_buffer(result.embedding),
-                **node_info,
-                **extra_info,
             }
+            additional_metadata = node_to_metadata_dict(result.node)
+            mapping.update(additional_metadata)
+
             ids.append(result.id)
             key = "_".join([self._prefix, str(result.id)])
             self._redis_client.hset(key, mapping=mapping)  # type: ignore
 
         _logger.info(f"Added {len(ids)} documents to index {self._index_name}")
         return ids
 
@@ -165,36 +163,49 @@
             delete_kwargs (Any): Additional arguments to pass to the delete method.
 
         """
         # use tokenizer to escape dashes in query
         query_str = "@doc_id:{%s}" % self.tokenizer.escape(doc_id)
         # find all documents that match a doc_id
         results = self._redis_client.ft(self._index_name).search(query_str)
+        if len(results.docs) == 0:
+            # don't raise an error but warn the user that document wasn't found
+            # could be a result of eviction policy
+            _logger.warning(
+                f"Document with doc_id {doc_id} not found in index {self._index_name}"
+            )
+            return
 
         for doc in results.docs:
             self._redis_client.delete(doc.id)
         _logger.info(
             f"Deleted {len(results.docs)} documents from index {self._index_name}"
         )
 
     def delete_index(self) -> None:
         """Delete the index and all documents."""
         _logger.info(f"Deleting index {self._index_name}")
         self._redis_client.ft(self._index_name).dropindex(delete_documents=True)
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query the index.
 
         Args:
             query (VectorStoreQuery): query object
 
         Returns:
             VectorStoreQueryResult: query result
+
+        Raises:
+            ValueError: If query.query_embedding is None.
+            redis.exceptions.RedisError: If there is an error querying the index.
+            redis.exceptions.TimeoutError: If there is a timeout querying the index.
         """
-        from redis.exceptions import ResponseError as RedisResponseError
+        from redis.exceptions import RedisError
+        from redis.exceptions import TimeoutError as RedisTimeoutError
 
         return_fields = ["id", "doc_id", "text", self._vector_key, "vector_score"]
 
         redis_query = get_redis_query(
             return_fields=return_fields,
             top_k=query.similarity_top_k,
             vector_field=self._vector_field,
@@ -207,22 +218,26 @@
         }
         _logger.info(f"Querying index {self._index_name}")
 
         try:
             results = self._redis_client.ft(self._index_name).search(
                 redis_query, query_params=query_params  # type: ignore
             )
-        except RedisResponseError as e:
-            _logger.error(f"Error querying index {self._index_name}: {e}")
+        except RedisTimeoutError as e:
+            _logger.error(f"Query timed out on {self._index_name}: {e}")
+            raise e
+        except RedisError as e:
+            _logger.error(f"Error querying {self._index_name}: {e}")
             raise e
 
         ids = []
         nodes = []
         scores = []
         for doc in results.docs:
+            # TODO: properly retrieve metadata
             node = Node(
                 text=doc.text,
                 doc_id=doc.id,
                 embedding=None,
                 relationships={DocumentRelationship.SOURCE: doc.doc_id},
             )
             ids.append(doc.id)
@@ -234,21 +249,32 @@
 
     def persist(self, persist_path: str, in_background: bool = True) -> None:
         """Persist the vector store to disk.
 
         Args:
             persist_path (str): Path to persist the vector store to. (doesn't apply)
             in_background (bool, optional): Persist in background. Defaults to True.
+
+        Raises:
+            redis.exceptions.RedisError: If there is an error
+                                         persisting the index to disk.
         """
-        if in_background:
-            _logger.info("Saving index to disk in background")
-            self._redis_client.bgsave()
-        else:
-            _logger.info("Saving index to disk")
-            self._redis_client.save()
+        from redis.exceptions import RedisError
+
+        try:
+            if in_background:
+                _logger.info("Saving index to disk in background")
+                self._redis_client.bgsave()
+            else:
+                _logger.info("Saving index to disk")
+                self._redis_client.save()
+
+        except RedisError as e:
+            _logger.error(f"Error saving index to disk: {e}")
+            raise e
 
     def _create_index(self) -> None:
         # should never be called outside class and hence should not raise importerror
         from redis.commands.search.field import TagField, TextField
         from redis.commands.search.indexDefinition import IndexDefinition, IndexType
 
         # Create Index
@@ -307,44 +333,54 @@
                             during the graph building.
             ef_runtime (int): The umber of maximum top candidates to hold during the
                 KNN search
 
         returns:
             A RediSearch VectorField.
         """
+        from redis import DataError
         from redis.commands.search.field import VectorField
 
-        if algorithm.upper() == "HNSW":
-            return VectorField(
-                name,
-                "HNSW",
-                {
-                    "TYPE": datatype.upper(),
-                    "DIM": dims,
-                    "DISTANCE_METRIC": distance_metric.upper(),
-                    "INITIAL_CAP": initial_cap,
-                    "M": m,
-                    "EF_CONSTRUCTION": ef_construction,
-                    "EF_RUNTIME": ef_runtime,
-                    "EPSILON": epsilon,
-                },
-            )
-        else:
-            return VectorField(
-                name,
-                "FLAT",
-                {
-                    "TYPE": datatype.upper(),
-                    "DIM": dims,
-                    "DISTANCE_METRIC": distance_metric.upper(),
-                    "INITIAL_CAP": initial_cap,
-                    "BLOCK_SIZE": block_size,
-                },
+        try:
+            if algorithm.upper() == "HNSW":
+                return VectorField(
+                    name,
+                    "HNSW",
+                    {
+                        "TYPE": datatype.upper(),
+                        "DIM": dims,
+                        "DISTANCE_METRIC": distance_metric.upper(),
+                        "INITIAL_CAP": initial_cap,
+                        "M": m,
+                        "EF_CONSTRUCTION": ef_construction,
+                        "EF_RUNTIME": ef_runtime,
+                        "EPSILON": epsilon,
+                    },
+                )
+            else:
+                return VectorField(
+                    name,
+                    "FLAT",
+                    {
+                        "TYPE": datatype.upper(),
+                        "DIM": dims,
+                        "DISTANCE_METRIC": distance_metric.upper(),
+                        "INITIAL_CAP": initial_cap,
+                        "BLOCK_SIZE": block_size,
+                    },
+                )
+        except DataError as e:
+            raise ValueError(
+                f"Failed to create Redis index vector field with error: {e}"
             )
 
 
 def cast_metadata_types(mapping: Optional[Dict[str, Any]]) -> Dict[str, str]:
     metadata = {}
     if mapping:
         for key, value in mapping.items():
-            metadata[str(key)] = str(value)
+            try:
+                metadata[str(key)] = str(value)
+            except (TypeError, ValueError) as e:
+                # warn the user and continue
+                _logger.warning("Failed to cast metadata to string", e)
     return metadata
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/registry.py` & `llama_index-0.6.6/llama_index/vector_stores/registry.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/llama_index/vector_stores/simple.py` & `llama_index-0.6.6/llama_index/vector_stores/simple.py`

 * *Files 3% similar despite different names*

```diff
@@ -102,16 +102,22 @@
         for text_id in text_ids_to_delete:
             del self._data.embedding_dict[text_id]
             del self._data.text_id_to_doc_id[text_id]
 
     def query(
         self,
         query: VectorStoreQuery,
+        **kwargs: Any,
     ) -> VectorStoreQueryResult:
         """Get nodes for response."""
+        if query.filters is not None:
+            raise ValueError(
+                "Metadata filters not implemented for SimpleVectorStore yet."
+            )
+
         # TODO: consolidate with get_query_text_embedding_similarities
         items = self._data.embedding_dict.items()
         node_ids = [t[0] for t in items]
         embeddings = [t[1] for t in items]
 
         query_embedding = cast(List[float], query.query_embedding)
```

### Comparing `llama_index-0.6.5/llama_index/vector_stores/weaviate.py` & `llama_index-0.6.6/llama_index/vector_stores/weaviate.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,16 +12,16 @@
     delete_document,
     weaviate_query,
 )
 from llama_index.readers.weaviate.utils import get_default_class_prefix
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
 
 
 class WeaviateVectorStore(VectorStore):
     """Weaviate vector store.
 
     In this vector store, embeddings and docs are stored within a
@@ -97,16 +97,19 @@
 
         Args:
             doc_id (str): document id
 
         """
         delete_document(self._client, doc_id, self._class_prefix)
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query index for top k most similar nodes."""
+        if query.filters is not None:
+            raise ValueError("Metadata filters not implemented for Weaviate yet.")
+
         nodes = weaviate_query(
             self._client,
             self._class_prefix,
             query,
         )
         nodes = nodes[: query.similarity_top_k]
         node_idxs = [str(i) for i in range(len(nodes))]
```

### Comparing `llama_index-0.6.5/llama_index.egg-info/PKG-INFO` & `llama_index-0.6.6/llama_index.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: llama-index
-Version: 0.6.5
+Version: 0.6.6
 Summary: Interface between LLMs and your data
 Home-page: https://github.com/jerryjliu/llama_index
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # 🗂️ LlamaIndex 🦙
```

### Comparing `llama_index-0.6.5/llama_index.egg-info/SOURCES.txt` & `llama_index-0.6.6/llama_index.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -104,15 +104,20 @@
 llama_index/indices/tree/base.py
 llama_index/indices/tree/inserter.py
 llama_index/indices/tree/select_leaf_embedding_retriever.py
 llama_index/indices/tree/select_leaf_retriever.py
 llama_index/indices/tree/tree_root_retriever.py
 llama_index/indices/vector_store/__init__.py
 llama_index/indices/vector_store/base.py
-llama_index/indices/vector_store/retrievers.py
+llama_index/indices/vector_store/retrievers/__init__.py
+llama_index/indices/vector_store/retrievers/retriever.py
+llama_index/indices/vector_store/retrievers/auto_retriever/__init__.py
+llama_index/indices/vector_store/retrievers/auto_retriever/auto_retriever.py
+llama_index/indices/vector_store/retrievers/auto_retriever/output_parser.py
+llama_index/indices/vector_store/retrievers/auto_retriever/prompts.py
 llama_index/langchain_helpers/__init__.py
 llama_index/langchain_helpers/chain_wrapper.py
 llama_index/langchain_helpers/memory_wrapper.py
 llama_index/langchain_helpers/sql_wrapper.py
 llama_index/langchain_helpers/streaming.py
 llama_index/langchain_helpers/text_splitter.py
 llama_index/langchain_helpers/agents/__init__.py
@@ -266,14 +271,15 @@
 llama_index/vector_stores/opensearch.py
 llama_index/vector_stores/pinecone.py
 llama_index/vector_stores/qdrant.py
 llama_index/vector_stores/redis.py
 llama_index/vector_stores/registry.py
 llama_index/vector_stores/simple.py
 llama_index/vector_stores/types.py
+llama_index/vector_stores/utils.py
 llama_index/vector_stores/weaviate.py
 tests/__init__.py
 tests/conftest.py
 tests/test_utils.py
 tests/callbacks/__init__.py
 tests/callbacks/test_llama_debug.py
 tests/embeddings/__init__.py
@@ -324,22 +330,21 @@
 tests/indices/tree/test_index.py
 tests/indices/tree/test_retrievers.py
 tests/indices/vector_store/__init__.py
 tests/indices/vector_store/conftest.py
 tests/indices/vector_store/mock_faiss.py
 tests/indices/vector_store/mock_services.py
 tests/indices/vector_store/test_faiss.py
-tests/indices/vector_store/test_lancedb.py
-tests/indices/vector_store/test_milvus.py
 tests/indices/vector_store/test_myscale.py
 tests/indices/vector_store/test_pinecone.py
 tests/indices/vector_store/test_retrievers.py
 tests/indices/vector_store/test_simple.py
-tests/indices/vector_store/test_weaviate.py
 tests/indices/vector_store/utils.py
+tests/indices/vector_store/auto_retriever/__init__.py
+tests/indices/vector_store/auto_retriever/test_output_parser.py
 tests/langchain_helpers/__init__.py
 tests/langchain_helpers/test_text_splitter.py
 tests/llm_predictor/__init__.py
 tests/llm_predictor/test_base.py
 tests/logger/__init__.py
 tests/logger/test_base.py
 tests/mock_utils/__init__.py
```

### Comparing `llama_index-0.6.5/setup.py` & `llama_index-0.6.6/setup.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/callbacks/test_llama_debug.py` & `llama_index-0.6.6/tests/callbacks/test_llama_debug.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/conftest.py` & `llama_index-0.6.6/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/embeddings/test_base.py` & `llama_index-0.6.6/tests/embeddings/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/composability/test_utils.py` & `llama_index-0.6.6/tests/indices/composability/test_utils.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from typing import Any, Dict, List, Optional
 
 from llama_index.vector_stores.types import (
     NodeWithEmbedding,
     VectorStore,
-    VectorStoreQueryResult,
     VectorStoreQuery,
+    VectorStoreQueryResult,
 )
 
 
 class MockVectorStore(VectorStore):
     stores_text: bool = True
 
     def __init__(self, config_dict: Optional[Dict[str, Any]] = None) -> None:
@@ -29,10 +29,10 @@
         """Add embedding results to vector store."""
         raise NotImplementedError()
 
     def delete(self, doc_id: str, **delete_kwargs: Any) -> None:
         """Delete doc."""
         raise NotImplementedError()
 
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
+    def query(self, query: VectorStoreQuery, **kwargs: Any) -> VectorStoreQueryResult:
         """Query vector store."""
         raise NotImplementedError()
```

### Comparing `llama_index-0.6.5/tests/indices/conftest.py` & `llama_index-0.6.6/tests/indices/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/document_summary/test_index.py` & `llama_index-0.6.6/tests/indices/document_summary/test_index.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/empty/test_base.py` & `llama_index-0.6.6/tests/indices/empty/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/keyword_table/test_base.py` & `llama_index-0.6.6/tests/indices/keyword_table/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/keyword_table/test_retrievers.py` & `llama_index-0.6.6/tests/indices/keyword_table/test_retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/keyword_table/test_utils.py` & `llama_index-0.6.6/tests/indices/keyword_table/test_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/knowledge_graph/test_base.py` & `llama_index-0.6.6/tests/indices/knowledge_graph/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/knowledge_graph/test_retrievers.py` & `llama_index-0.6.6/tests/indices/knowledge_graph/test_retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/list/test_index.py` & `llama_index-0.6.6/tests/indices/list/test_index.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/list/test_retrievers.py` & `llama_index-0.6.6/tests/indices/list/test_retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/postprocessor/test_base.py` & `llama_index-0.6.6/tests/indices/postprocessor/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/query/conftest.py` & `llama_index-0.6.6/tests/indices/query/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/query/query_transform/test_base.py` & `llama_index-0.6.6/tests/indices/query/query_transform/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/query/test_compose.py` & `llama_index-0.6.6/tests/indices/query/test_compose.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/query/test_compose_vector.py` & `llama_index-0.6.6/tests/indices/query/test_compose_vector.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,30 +1,23 @@
 """Test recursive queries."""
 
 import asyncio
-import sys
 from typing import Any, Dict, List
-from unittest.mock import MagicMock
 
 import pytest
 
 from llama_index.data_structs.data_structs import IndexStruct
 from llama_index.embeddings.base import BaseEmbedding
 from llama_index.indices.composability.graph import ComposableGraph
 from llama_index.indices.keyword_table.simple_base import GPTSimpleKeywordTableIndex
 from llama_index.indices.service_context import ServiceContext
 from llama_index.indices.vector_store.base import GPTVectorStoreIndex
 from llama_index.readers.schema.base import Document
-from llama_index.storage.storage_context import StorageContext
-from llama_index.vector_stores.pinecone import PineconeVectorStore
-from tests.indices.vector_store.utils import MockPineconeIndex
-from tests.mock_utils.mock_prompts import (
-    MOCK_QUERY_KEYWORD_EXTRACT_PROMPT,
-)
-from tests.mock_utils.mock_utils import mock_tokenizer
+from tests.indices.vector_store.utils import get_pinecone_storage_context
+from tests.mock_utils.mock_prompts import MOCK_QUERY_KEYWORD_EXTRACT_PROMPT
 
 
 class MockEmbedding(BaseEmbedding):
     def _get_query_embedding(self, query: str) -> List[float]:
         """Mock get query embedding."""
         if query == "Foo?":
             return [0, 0, 1, 0, 0]
@@ -287,24 +280,14 @@
     response = query_engine.query(query_str)
     assert str(response) == ("Orange?:Orange?:This is a test.")
     query_str = "Cat?"
     response = query_engine.query(query_str)
     assert str(response) == ("Cat?:Cat?:This is a test v2.")
 
 
-def get_pinecone_storage_context() -> StorageContext:
-    # NOTE: mock pinecone import
-    sys.modules["pinecone"] = MagicMock()
-    return StorageContext.from_defaults(
-        vector_store=PineconeVectorStore(
-            pinecone_index=MockPineconeIndex(), tokenizer=mock_tokenizer
-        )
-    )
-
-
 def test_recursive_query_pinecone_pinecone(
     documents: List[Document],
     mock_service_context: ServiceContext,
     index_kwargs: Dict,
 ) -> None:
     """Test composing pinecone index on top of pinecone index."""
     pinecone_kwargs = index_kwargs["pinecone"]
```

### Comparing `llama_index-0.6.5/tests/indices/query/test_query_bundle.py` & `llama_index-0.6.6/tests/indices/query/test_query_bundle.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/struct_store/conftest.py` & `llama_index-0.6.6/tests/indices/struct_store/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/struct_store/test_base.py` & `llama_index-0.6.6/tests/indices/struct_store/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/struct_store/test_pandas.py` & `llama_index-0.6.6/tests/indices/struct_store/test_pandas.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/struct_store/test_sql_query.py` & `llama_index-0.6.6/tests/indices/struct_store/test_sql_query.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/test_loading.py` & `llama_index-0.6.6/tests/indices/test_loading.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/test_loading_graph.py` & `llama_index-0.6.6/tests/indices/test_loading_graph.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/test_node_utils.py` & `llama_index-0.6.6/tests/indices/test_node_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/test_prompt_helper.py` & `llama_index-0.6.6/tests/indices/test_prompt_helper.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/tree/conftest.py` & `llama_index-0.6.6/tests/indices/tree/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/tree/test_embedding_retriever.py` & `llama_index-0.6.6/tests/indices/tree/test_embedding_retriever.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/tree/test_index.py` & `llama_index-0.6.6/tests/indices/tree/test_index.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/tree/test_retrievers.py` & `llama_index-0.6.6/tests/indices/tree/test_retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/conftest.py` & `llama_index-0.6.6/tests/indices/vector_store/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/mock_faiss.py` & `llama_index-0.6.6/tests/indices/vector_store/mock_faiss.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/mock_services.py` & `llama_index-0.6.6/tests/indices/vector_store/mock_services.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 from typing import List
+
 from llama_index.embeddings.base import BaseEmbedding
 
 
 class MockEmbedding(BaseEmbedding):
     def _get_query_embedding(self, query: str) -> List[float]:
         del query  # Unused
         return [0, 0, 1, 0, 0]
@@ -22,8 +23,8 @@
             return [0, 0, 0, 0, 1]
         elif text == "This is bar test.":
             return [0, 0, 1, 0, 0]
         elif text == "Hello world backup.":
             # this is used when "Hello world." is deleted.
             return [1, 0, 0, 0, 0]
         else:
-            raise ValueError("Invalid text for `_get_text_embedding`.")
+            return [0, 0, 0, 0, 0]
```

### Comparing `llama_index-0.6.5/tests/indices/vector_store/test_faiss.py` & `llama_index-0.6.6/tests/indices/vector_store/test_faiss.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/test_lancedb.py` & `llama_index-0.6.6/tests/indices/vector_store/test_pinecone.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,59 +1,62 @@
-"""Test LanceDB index."""
-from typing import Any, List, Optional
+"""Test pinecone indexes."""
 
-from llama_index.indices.vector_store import GPTVectorStoreIndex
+from typing import List
+
+import pytest
+
+from llama_index.data_structs.node import Node
 from llama_index.indices.service_context import ServiceContext
-from llama_index.storage.storage_context import StorageContext
+from llama_index.indices.vector_store.base import GPTVectorStoreIndex
+from llama_index.readers.schema.base import Document
+from tests.indices.vector_store.utils import get_pinecone_storage_context
+from tests.mock_utils.mock_utils import mock_tokenizer
 
-from llama_index.vector_stores.types import (
-    NodeWithEmbedding,
-    VectorStore,
-    VectorStoreQuery,
-    VectorStoreQueryResult,
-)
-
-
-class MockLanceDBVectorStore(VectorStore):
-    stores_text: bool = True
-
-    def __init__(
-        self,
-        uri: str,
-        table_name: str = "vectors",
-        nprobes: int = 20,
-        refine_factor: Optional[int] = None,
-        **kwargs: Any,
-    ) -> None:
-        self.connection = None
-        self.uri = uri
-        self.table_name = table_name
-        self.nprobes = nprobes
-        self.refine_factor = refine_factor
-
-    @property
-    def client(self) -> None:
-        """Get client."""
-        return None
-
-    def add(
-        self,
-        embedding_results: List[NodeWithEmbedding],
-    ) -> List[str]:
-        return []
-
-    def delete(self, doc_id: str, **delete_kwargs: Any) -> None:
-        return None
-
-    def query(self, query: VectorStoreQuery) -> VectorStoreQueryResult:
-        return VectorStoreQueryResult()
-
-
-def test_save_load(mock_service_context: ServiceContext) -> None:
-    """Test we can save and load."""
-    vector_store = MockLanceDBVectorStore(uri=".")
-    storage_context = StorageContext.from_defaults(vector_store=vector_store)
-    GPTVectorStoreIndex.from_documents(
-        documents=[],
+
+@pytest.fixture
+def documents() -> List[Document]:
+    """Get documents."""
+    # NOTE: one document for now
+    doc_text = (
+        "Hello world.\n"
+        "This is a test.\n"
+        "This is another test.\n"
+        "This is a test v2."
+    )
+    return [Document(doc_text)]
+
+
+def test_build_pinecone(
+    documents: List[Document],
+    mock_service_context: ServiceContext,
+) -> None:
+    """Test build GPTVectorStoreIndex with PineconeVectorStore."""
+    storage_context = get_pinecone_storage_context()
+    index = GPTVectorStoreIndex.from_documents(
+        documents=documents,
+        storage_context=storage_context,
         service_context=mock_service_context,
+        tokenizer=mock_tokenizer,
+    )
+
+    retriever = index.as_retriever(similarity_top_k=1)
+    nodes = retriever.retrieve("What is?")
+    assert len(nodes) == 1
+    assert nodes[0].node.get_text() == "This is another test."
+
+
+def test_node_with_metadata(
+    mock_service_context: ServiceContext,
+) -> None:
+    storage_context = get_pinecone_storage_context()
+    input_nodes = [Node(text="test node text", extra_info={"key": "value"})]
+    index = GPTVectorStoreIndex(
+        input_nodes,
         storage_context=storage_context,
+        service_context=mock_service_context,
     )
+
+    retriever = index.as_retriever(similarity_top_k=1)
+    nodes = retriever.retrieve("What is?")
+    assert len(nodes) == 1
+    assert nodes[0].node.text == "test node text"
+    assert nodes[0].node.extra_info == {"key": "value"}
```

### Comparing `llama_index-0.6.5/tests/indices/vector_store/test_myscale.py` & `llama_index-0.6.6/tests/indices/vector_store/test_myscale.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/test_retrievers.py` & `llama_index-0.6.6/tests/indices/vector_store/test_retrievers.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/test_simple.py` & `llama_index-0.6.6/tests/indices/vector_store/test_simple.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/indices/vector_store/utils.py` & `llama_index-0.6.6/tests/indices/vector_store/utils.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,12 +1,17 @@
+import sys
 from typing import Any, Dict, List, Optional
 from unittest.mock import MagicMock
 
 import numpy as np
 
+from llama_index.storage.storage_context import StorageContext
+from llama_index.vector_stores.pinecone import PineconeVectorStore
+from tests.mock_utils.mock_utils import mock_tokenizer
+
 
 class MockPineconeIndex:
     def __init__(self) -> None:
         """Mock pinecone index."""
         self._tuples: List[Dict[str, Any]] = []
 
     def upsert(self, tuples: List[Dict[str, Any]], **kwargs: Any) -> None:
@@ -42,18 +47,23 @@
         indices = np.argsort(distances)[:top_k]
         # sorted_distances = distances[indices][:top_k]
 
         matches = []
         for index in indices:
             tup = self._tuples[index]
             match = MagicMock()
-            match.metadata = {
-                "text": tup["metadata"]["text"],
-                "doc_id": tup["metadata"]["doc_id"],
-                "id": tup["metadata"]["id"],
-            }
-
+            match.metadata = tup["metadata"]
             matches.append(match)
 
         response = MagicMock()
         response.matches = matches
         return response
+
+
+def get_pinecone_storage_context() -> StorageContext:
+    # NOTE: mock pinecone import
+    sys.modules["pinecone"] = MagicMock()
+    return StorageContext.from_defaults(
+        vector_store=PineconeVectorStore(
+            pinecone_index=MockPineconeIndex(), tokenizer=mock_tokenizer
+        )
+    )
```

### Comparing `llama_index-0.6.5/tests/langchain_helpers/test_text_splitter.py` & `llama_index-0.6.6/tests/langchain_helpers/test_text_splitter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/llm_predictor/test_base.py` & `llama_index-0.6.6/tests/llm_predictor/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/logger/test_base.py` & `llama_index-0.6.6/tests/logger/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/mock_utils/mock_predict.py` & `llama_index-0.6.6/tests/mock_utils/mock_predict.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/mock_utils/mock_prompts.py` & `llama_index-0.6.6/tests/mock_utils/mock_prompts.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/mock_utils/mock_text_splitter.py` & `llama_index-0.6.6/tests/mock_utils/mock_text_splitter.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/mock_utils/mock_utils.py` & `llama_index-0.6.6/tests/mock_utils/mock_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/optimization/test_base.py` & `llama_index-0.6.6/tests/optimization/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/output_parsers/test_base.py` & `llama_index-0.6.6/tests/output_parsers/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/output_parsers/test_selection.py` & `llama_index-0.6.6/tests/output_parsers/test_selection.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import pytest
+
 from llama_index.output_parsers.base import StructuredOutput
 from llama_index.output_parsers.selection import SelectionOutputParser
 
 
 @pytest.fixture()
 def output_parser() -> SelectionOutputParser:
     return SelectionOutputParser()
@@ -22,7 +23,28 @@
     """
     parsed = output_parser.parse(output=output)
     assert isinstance(parsed, StructuredOutput)
     assert isinstance(parsed.parsed_output, list)
     assert len(parsed.parsed_output) == 2
     assert parsed.parsed_output[0].choice == 1
     assert parsed.parsed_output[0].reason == "just because"
+
+
+def test_parse_non_json_friendly_llm_output(
+    output_parser: SelectionOutputParser,
+) -> None:
+    # https://github.com/jerryjliu/llama_index/issues/3135
+    output = """
+    Output:
+    [
+      {
+        "choice": 1,
+        "reason": "Useful for questions"
+      }
+    ]
+    """
+    parsed = output_parser.parse(output)
+    assert isinstance(parsed, StructuredOutput)
+    assert isinstance(parsed.parsed_output, list)
+    assert len(parsed.parsed_output) == 1
+    assert parsed.parsed_output[0].choice == 1
+    assert parsed.parsed_output[0].reason == "Useful for questions"
```

### Comparing `llama_index-0.6.5/tests/playground/test_base.py` & `llama_index-0.6.6/tests/playground/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/prompts/test_base.py` & `llama_index-0.6.6/tests/prompts/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/readers/test_file.py` & `llama_index-0.6.6/tests/readers/test_file.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/readers/test_json.py` & `llama_index-0.6.6/tests/readers/test_json.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/readers/test_mongo.py` & `llama_index-0.6.6/tests/readers/test_mongo.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/selectors/test_llm_selectors.py` & `llama_index-0.6.6/tests/selectors/test_llm_selectors.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/storage/conftest.py` & `llama_index-0.6.6/tests/storage/conftest.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/storage/docstore/test_mongo_docstore.py` & `llama_index-0.6.6/tests/storage/docstore/test_mongo_docstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/storage/docstore/test_simple_docstore.py` & `llama_index-0.6.6/tests/storage/docstore/test_simple_docstore.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/storage/test_storage_context.py` & `llama_index-0.6.6/tests/storage/test_storage_context.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/test_utils.py` & `llama_index-0.6.6/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/token_predictor/test_base.py` & `llama_index-0.6.6/tests/token_predictor/test_base.py`

 * *Files identical despite different names*

### Comparing `llama_index-0.6.5/tests/vector_stores/test_qdrant.py` & `llama_index-0.6.6/tests/vector_stores/test_qdrant.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import pytest
 
 try:
     import qdrant_client
 except ImportError:
     qdrant_client = None  # type: ignore
 
-from llama_index.data_structs.node import Node, DocumentRelationship
+from llama_index.data_structs.node import DocumentRelationship, Node
 from llama_index.vector_stores import QdrantVectorStore
 from llama_index.vector_stores.types import NodeWithEmbedding, VectorStoreQuery
 
 
 @pytest.fixture
 def node_embeddings() -> List[NodeWithEmbedding]:
     return [
@@ -56,15 +56,15 @@
     query_filter = qdrant_vector_store._build_query_filter(query)
 
     assert query_filter is None
 
 
 @pytest.mark.skipif(qdrant_client is None, reason="qdrant-client not installed")
 def test_build_query_filter_returns_match_any() -> None:
-    from qdrant_client.http.models import Filter, FieldCondition, MatchAny
+    from qdrant_client.http.models import FieldCondition, Filter, MatchAny
 
     client = qdrant_client.QdrantClient(":memory:")
     qdrant_vector_store = QdrantVectorStore(collection_name="test", client=client)
 
     query = VectorStoreQuery(doc_ids=["1", "2", "3"])
     query_filter = cast(Filter, qdrant_vector_store._build_query_filter(query))
 
@@ -74,15 +74,15 @@
     assert query_filter.must[0].key == "doc_id"  # type: ignore[index]
     assert isinstance(query_filter.must[0].match, MatchAny)  # type: ignore[index]
     assert query_filter.must[0].match.any == ["1", "2", "3"]  # type: ignore[index]
 
 
 @pytest.mark.skipif(qdrant_client is None, reason="qdrant-client not installed")
 def test_build_query_filter_returns_text_filter() -> None:
-    from qdrant_client.http.models import Filter, FieldCondition, MatchText
+    from qdrant_client.http.models import FieldCondition, Filter, MatchText
 
     client = qdrant_client.QdrantClient(":memory:")
     qdrant_vector_store = QdrantVectorStore(collection_name="test", client=client)
 
     query = VectorStoreQuery(query_str="lorem")
     query_filter = cast(Filter, qdrant_vector_store._build_query_filter(query))
 
@@ -92,15 +92,15 @@
     assert query_filter.must[0].key == "text"  # type: ignore[index]
     assert isinstance(query_filter.must[0].match, MatchText)  # type: ignore[index]
     assert query_filter.must[0].match.text == "lorem"  # type: ignore[index]
 
 
 @pytest.mark.skipif(qdrant_client is None, reason="qdrant-client not installed")
 def test_build_query_filter_returns_combined_filter() -> None:
-    from qdrant_client.http.models import Filter, FieldCondition, MatchText, MatchAny
+    from qdrant_client.http.models import FieldCondition, Filter, MatchAny, MatchText
 
     client = qdrant_client.QdrantClient(":memory:")
     qdrant_vector_store = QdrantVectorStore(collection_name="test", client=client)
 
     query = VectorStoreQuery(query_str="lorem", doc_ids=["1", "2", "3"])
     query_filter = cast(Filter, qdrant_vector_store._build_query_filter(query))
```

### Comparing `llama_index-0.6.5/tests/vector_stores/test_weaviate.py` & `llama_index-0.6.6/tests/vector_stores/test_weaviate.py`

 * *Files identical despite different names*

