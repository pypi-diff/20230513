# Comparing `tmp/linkml_runtime-1.5.2.tar.gz` & `tmp/linkml_runtime-1.5.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "linkml_runtime-1.5.2.tar", max compression
+gzip compressed data, was "linkml_runtime-1.5.3.tar", max compression
```

## Comparing `linkml_runtime-1.5.2.tar` & `linkml_runtime-1.5.3.tar`

### file list

```diff
@@ -1,142 +1,142 @@
--rw-r--r--   0        0        0     7048 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/LICENSE
--rw-r--r--   0        0        0     1996 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/README.md
--rw-r--r--   0        0        0     1179 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/__init__.py
--rw-r--r--   0        0        0      426 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/__init__.py
--rw-r--r--   0        0        0     1225 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/csv_dumper.py
--rw-r--r--   0        0        0      863 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/dumper_root.py
--rw-r--r--   0        0        0     3950 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/json_dumper.py
--rw-r--r--   0        0        0     3771 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/rdf_dumper.py
--rw-r--r--   0        0        0     7077 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/rdflib_dumper.py
--rw-r--r--   0        0        0      751 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/dumpers/yaml_dumper.py
--rw-r--r--   0        0        0        0 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/index/__init__.py
--rw-r--r--   0        0        0     8875 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/index/object_index.py
--rw-r--r--   0        0        0      119 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/README.md
--rw-r--r--   0        0        0      738 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/__init__.py
--rw-r--r--   0        0        0     3240 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/annotations.py
--rw-r--r--   0        0        0     3333 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/extensions.py
--rw-r--r--   0        0        0      114 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/graphql/README.md
--rw-r--r--   0        0        0    30306 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/graphql/meta.graphql
--rw-r--r--   0        0        0      111 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/README.md
--rw-r--r--   0        0        0    11169 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/annotations.json
--rw-r--r--   0        0        0     9306 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/extensions.json
--rw-r--r--   0        0        0    12109 2023-05-02 19:04:18.262419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/mappings.json
--rw-r--r--   0        0        0   222072 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/meta.json
--rw-r--r--   0        0        0     6442 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/types.json
--rw-r--r--   0        0        0    22401 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/units.json
--rw-r--r--   0        0        0    14834 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/validation.json
--rw-r--r--   0        0        0      113 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/README.md
--rw-r--r--   0        0        0      648 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/annotations.context.jsonld
--rw-r--r--   0        0        0      648 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/annotations.model.context.jsonld
--rw-r--r--   0        0        0     7019 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/context.jsonld
--rw-r--r--   0        0        0      587 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/extensions.context.jsonld
--rw-r--r--   0        0        0      587 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/extensions.model.context.jsonld
--rw-r--r--   0        0        0     1615 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/mappings.context.jsonld
--rw-r--r--   0        0        0     1615 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/mappings.model.context.jsonld
--rw-r--r--   0        0        0    13814 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/meta.context.jsonld
--rw-r--r--   0        0        0    14266 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/meta.model.context.jsonld
--rw-r--r--   0        0        0      610 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/types.context.jsonld
--rw-r--r--   0        0        0      610 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/types.model.context.jsonld
--rw-r--r--   0        0        0     2065 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/units.context.jsonld
--rw-r--r--   0        0        0     2065 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/units.model.context.jsonld
--rw-r--r--   0        0        0     1910 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/validation.context.jsonld
--rw-r--r--   0        0        0     1910 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/validation.model.context.jsonld
--rw-r--r--   0        0        0      117 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/README.md
--rw-r--r--   0        0        0     4196 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/annotations.schema.json
--rw-r--r--   0        0        0     1984 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/extensions.schema.json
--rw-r--r--   0        0        0      297 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/mappings.schema.json
--rw-r--r--   0        0        0   353208 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/meta.schema.json
--rw-r--r--   0        0        0      291 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/types.schema.json
--rw-r--r--   0        0        0     5621 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/units.schema.json
--rw-r--r--   0        0        0     2291 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/validation.schema.json
--rw-r--r--   0        0        0     7126 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/linkml_files.py
--rw-r--r--   0        0        0     1821 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/mappings.py
--rw-r--r--   0        0        0   249036 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/meta.py
--rw-r--r--   0        0        0      112 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/README.md
--rw-r--r--   0        0        0      118 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/docs/credits.md
--rw-r--r--   0        0        0      141 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/docs/home.md
--rw-r--r--   0        0        0        5 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/import_map.json
--rw-r--r--   0        0        0      119 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/README.md
--rw-r--r--   0        0        0      833 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/annotations.yaml
--rw-r--r--   0        0        0     1057 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/extensions.yaml
--rw-r--r--   0        0        0     2755 2023-05-02 19:04:18.266419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/mappings.yaml
--rw-r--r--   0        0        0    89120 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/meta.yaml
--rw-r--r--   0        0        0     3880 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/types.yaml
--rw-r--r--   0        0        0     2776 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/units.yaml
--rw-r--r--   0        0        0     2953 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/validation.yaml
--rw-r--r--   0        0        0      110 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/owl/README.md
--rw-r--r--   0        0        0   192274 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/owl/meta.owl.ttl
--rw-r--r--   0        0        0      110 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/README.md
--rw-r--r--   0        0        0    13054 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/annotations.model.ttl
--rw-r--r--   0        0        0    13054 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/annotations.ttl
--rw-r--r--   0        0        0    10932 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/extensions.model.ttl
--rw-r--r--   0        0        0    10932 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/extensions.ttl
--rw-r--r--   0        0        0    13825 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/mappings.model.ttl
--rw-r--r--   0        0        0    13825 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/mappings.ttl
--rw-r--r--   0        0        0   207795 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/meta.model.ttl
--rw-r--r--   0        0        0   207795 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/meta.ttl
--rw-r--r--   0        0        0     7565 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/types.model.ttl
--rw-r--r--   0        0        0     7565 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/types.ttl
--rw-r--r--   0        0        0    25276 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/units.model.ttl
--rw-r--r--   0        0        0    25276 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/units.ttl
--rw-r--r--   0        0        0    16810 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/validation.model.ttl
--rw-r--r--   0        0        0    16810 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/validation.ttl
--rw-r--r--   0        0        0      113 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/README.md
--rw-r--r--   0        0        0     1261 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/annotations.shex
--rw-r--r--   0        0        0     8918 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/annotations.shexj
--rw-r--r--   0        0        0      821 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/extensions.shex
--rw-r--r--   0        0        0     5303 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/extensions.shexj
--rw-r--r--   0        0        0      424 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/mappings.shex
--rw-r--r--   0        0        0     2568 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/mappings.shexj
--rw-r--r--   0        0        0    37441 2023-05-02 19:04:18.270419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/meta.shex
--rw-r--r--   0        0        0   254576 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/meta.shexj
--rw-r--r--   0        0        0      459 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/types.shex
--rw-r--r--   0        0        0     2568 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/types.shexj
--rw-r--r--   0        0        0     1682 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/units.shex
--rw-r--r--   0        0        0    11643 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/units.shexj
--rw-r--r--   0        0        0     1519 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/validation.shex
--rw-r--r--   0        0        0     7343 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/validation.shexj
--rw-r--r--   0        0        0     4599 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/types.py
--rw-r--r--   0        0        0     3332 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/units.py
--rw-r--r--   0        0        0     6897 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/linkml_model/validation.py
--rw-r--r--   0        0        0      426 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/__init__.py
--rw-r--r--   0        0        0     1533 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/context_flattener.py
--rw-r--r--   0        0        0     1933 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/csv_loader.py
--rw-r--r--   0        0        0     1318 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/json_loader.py
--rw-r--r--   0        0        0     5199 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/loader_root.py
--rw-r--r--   0        0        0     4735 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/rdf_loader.py
--rw-r--r--   0        0        0    14065 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/rdflib_loader.py
--rw-r--r--   0        0        0     1358 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/requests_ssl_patch.py
--rw-r--r--   0        0        0     1821 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/loaders/yaml_loader.py
--rw-r--r--   0        0        0    42276 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/processing/referencevalidator.py
--rw-r--r--   0        0        0    26951 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/processing/validation_datamodel.py
--rw-r--r--   0        0        0    10253 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/processing/validation_datamodel.yaml
--rw-r--r--   0        0        0        0 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/__init__.py
--rw-r--r--   0        0        0      850 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/comparefiles.py
--rw-r--r--   0        0        0     1972 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/compile_python.py
--rw-r--r--   0        0        0     4034 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/context_utils.py
--rw-r--r--   0        0        0     2389 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/csvutils.py
--rw-r--r--   0        0        0      486 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/curienamespace.py
--rw-r--r--   0        0        0     1325 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/dataclass_extensions_376.py
--rw-r--r--   0        0        0      433 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/dictutils.py
--rw-r--r--   0        0        0     2554 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/distroutils.py
--rw-r--r--   0        0        0     3683 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/enumerations.py
--rw-r--r--   0        0        0     6755 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/eval_utils.py
--rw-r--r--   0        0        0     6594 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/formatutils.py
--rw-r--r--   0        0        0     5672 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/inference_utils.py
--rw-r--r--   0        0        0     1976 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/introspection.py
--rw-r--r--   0        0        0    11553 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/metamodelcore.py
--rw-r--r--   0        0        0    10580 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/namespaces.py
--rw-r--r--   0        0        0     2870 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/pattern.py
--rw-r--r--   0        0        0     6697 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/permissiblevalueimpl.py
--rw-r--r--   0        0        0     4720 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/ruleutils.py
--rw-r--r--   0        0        0     2287 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/schema_as_dict.py
--rw-r--r--   0        0        0     9312 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/schema_builder.py
--rw-r--r--   0        0        0     2815 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/schemaops.py
--rw-r--r--   0        0        0    66900 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/schemaview.py
--rw-r--r--   0        0        0     4327 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/schemaview_cli.py
--rw-r--r--   0        0        0      368 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/slot.py
--rw-r--r--   0        0        0      641 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/strictness.py
--rw-r--r--   0        0        0     1405 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/walker_utils.py
--rw-r--r--   0        0        0    19743 2023-05-02 19:04:18.274419 linkml_runtime-1.5.2/linkml_runtime/utils/yamlutils.py
--rw-r--r--   0        0        0     1826 2023-05-02 19:04:38.202384 linkml_runtime-1.5.2/pyproject.toml
--rw-r--r--   0        0        0     3680 1970-01-01 00:00:00.000000 linkml_runtime-1.5.2/PKG-INFO
+-rw-r--r--   0        0        0     7048 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/LICENSE
+-rw-r--r--   0        0        0     1996 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/README.md
+-rw-r--r--   0        0        0     1179 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/__init__.py
+-rw-r--r--   0        0        0      426 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/__init__.py
+-rw-r--r--   0        0        0     1264 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/csv_dumper.py
+-rw-r--r--   0        0        0      973 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/dumper_root.py
+-rw-r--r--   0        0        0     4377 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/json_dumper.py
+-rw-r--r--   0        0        0     4023 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/rdf_dumper.py
+-rw-r--r--   0        0        0     7169 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/rdflib_dumper.py
+-rw-r--r--   0        0        0      901 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/dumpers/yaml_dumper.py
+-rw-r--r--   0        0        0        0 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/index/__init__.py
+-rw-r--r--   0        0        0     8875 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/index/object_index.py
+-rw-r--r--   0        0        0      119 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/README.md
+-rw-r--r--   0        0        0      738 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/__init__.py
+-rw-r--r--   0        0        0     3240 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/annotations.py
+-rw-r--r--   0        0        0     3333 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/extensions.py
+-rw-r--r--   0        0        0      114 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/graphql/README.md
+-rw-r--r--   0        0        0    30306 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/graphql/meta.graphql
+-rw-r--r--   0        0        0      111 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/README.md
+-rw-r--r--   0        0        0    11169 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/annotations.json
+-rw-r--r--   0        0        0     9306 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/extensions.json
+-rw-r--r--   0        0        0    12109 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/mappings.json
+-rw-r--r--   0        0        0   222072 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/meta.json
+-rw-r--r--   0        0        0     6442 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/types.json
+-rw-r--r--   0        0        0    22401 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/units.json
+-rw-r--r--   0        0        0    14834 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/validation.json
+-rw-r--r--   0        0        0      113 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/README.md
+-rw-r--r--   0        0        0      648 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/annotations.context.jsonld
+-rw-r--r--   0        0        0      648 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/annotations.model.context.jsonld
+-rw-r--r--   0        0        0     7019 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/context.jsonld
+-rw-r--r--   0        0        0      587 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/extensions.context.jsonld
+-rw-r--r--   0        0        0      587 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/extensions.model.context.jsonld
+-rw-r--r--   0        0        0     1615 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/mappings.context.jsonld
+-rw-r--r--   0        0        0     1615 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/mappings.model.context.jsonld
+-rw-r--r--   0        0        0    13814 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/meta.context.jsonld
+-rw-r--r--   0        0        0    14266 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/meta.model.context.jsonld
+-rw-r--r--   0        0        0      610 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/types.context.jsonld
+-rw-r--r--   0        0        0      610 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/types.model.context.jsonld
+-rw-r--r--   0        0        0     2065 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/units.context.jsonld
+-rw-r--r--   0        0        0     2065 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/units.model.context.jsonld
+-rw-r--r--   0        0        0     1910 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/validation.context.jsonld
+-rw-r--r--   0        0        0     1910 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/validation.model.context.jsonld
+-rw-r--r--   0        0        0      117 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/README.md
+-rw-r--r--   0        0        0     4196 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/annotations.schema.json
+-rw-r--r--   0        0        0     1984 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/extensions.schema.json
+-rw-r--r--   0        0        0      297 2023-05-13 02:39:28.116564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/mappings.schema.json
+-rw-r--r--   0        0        0   353208 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/meta.schema.json
+-rw-r--r--   0        0        0      291 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/types.schema.json
+-rw-r--r--   0        0        0     5621 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/units.schema.json
+-rw-r--r--   0        0        0     2291 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/validation.schema.json
+-rw-r--r--   0        0        0     7126 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/linkml_files.py
+-rw-r--r--   0        0        0     1821 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/mappings.py
+-rw-r--r--   0        0        0   249036 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/meta.py
+-rw-r--r--   0        0        0      112 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/README.md
+-rw-r--r--   0        0        0      118 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/docs/credits.md
+-rw-r--r--   0        0        0      141 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/docs/home.md
+-rw-r--r--   0        0        0        5 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/import_map.json
+-rw-r--r--   0        0        0      119 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/README.md
+-rw-r--r--   0        0        0      833 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/annotations.yaml
+-rw-r--r--   0        0        0     1057 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/extensions.yaml
+-rw-r--r--   0        0        0     2755 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/mappings.yaml
+-rw-r--r--   0        0        0    89120 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/meta.yaml
+-rw-r--r--   0        0        0     3880 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/types.yaml
+-rw-r--r--   0        0        0     2776 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/units.yaml
+-rw-r--r--   0        0        0     2953 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/validation.yaml
+-rw-r--r--   0        0        0      110 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/owl/README.md
+-rw-r--r--   0        0        0   192274 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/owl/meta.owl.ttl
+-rw-r--r--   0        0        0      110 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/README.md
+-rw-r--r--   0        0        0    13054 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/annotations.model.ttl
+-rw-r--r--   0        0        0    13054 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/annotations.ttl
+-rw-r--r--   0        0        0    10932 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/extensions.model.ttl
+-rw-r--r--   0        0        0    10932 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/extensions.ttl
+-rw-r--r--   0        0        0    13825 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/mappings.model.ttl
+-rw-r--r--   0        0        0    13825 2023-05-13 02:39:28.120564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/mappings.ttl
+-rw-r--r--   0        0        0   207795 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/meta.model.ttl
+-rw-r--r--   0        0        0   207795 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/meta.ttl
+-rw-r--r--   0        0        0     7565 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/types.model.ttl
+-rw-r--r--   0        0        0     7565 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/types.ttl
+-rw-r--r--   0        0        0    25276 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/units.model.ttl
+-rw-r--r--   0        0        0    25276 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/units.ttl
+-rw-r--r--   0        0        0    16810 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/validation.model.ttl
+-rw-r--r--   0        0        0    16810 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/validation.ttl
+-rw-r--r--   0        0        0      113 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/README.md
+-rw-r--r--   0        0        0     1261 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/annotations.shex
+-rw-r--r--   0        0        0     8918 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/annotations.shexj
+-rw-r--r--   0        0        0      821 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/extensions.shex
+-rw-r--r--   0        0        0     5303 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/extensions.shexj
+-rw-r--r--   0        0        0      424 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/mappings.shex
+-rw-r--r--   0        0        0     2568 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/mappings.shexj
+-rw-r--r--   0        0        0    37441 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/meta.shex
+-rw-r--r--   0        0        0   254576 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/meta.shexj
+-rw-r--r--   0        0        0      459 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/types.shex
+-rw-r--r--   0        0        0     2568 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/types.shexj
+-rw-r--r--   0        0        0     1682 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/units.shex
+-rw-r--r--   0        0        0    11643 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/units.shexj
+-rw-r--r--   0        0        0     1519 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/validation.shex
+-rw-r--r--   0        0        0     7343 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/validation.shexj
+-rw-r--r--   0        0        0     4599 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/types.py
+-rw-r--r--   0        0        0     3332 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/units.py
+-rw-r--r--   0        0        0     6897 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/linkml_model/validation.py
+-rw-r--r--   0        0        0      426 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/__init__.py
+-rw-r--r--   0        0        0     1533 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/context_flattener.py
+-rw-r--r--   0        0        0     2000 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/csv_loader.py
+-rw-r--r--   0        0        0     1394 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/json_loader.py
+-rw-r--r--   0        0        0     5919 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/loader_root.py
+-rw-r--r--   0        0        0     4831 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/rdf_loader.py
+-rw-r--r--   0        0        0    14214 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/rdflib_loader.py
+-rw-r--r--   0        0        0     1358 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/requests_ssl_patch.py
+-rw-r--r--   0        0        0     1971 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/loaders/yaml_loader.py
+-rw-r--r--   0        0        0    42276 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/processing/referencevalidator.py
+-rw-r--r--   0        0        0    26951 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/processing/validation_datamodel.py
+-rw-r--r--   0        0        0    10253 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/processing/validation_datamodel.yaml
+-rw-r--r--   0        0        0        0 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/__init__.py
+-rw-r--r--   0        0        0      850 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/comparefiles.py
+-rw-r--r--   0        0        0     1972 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/compile_python.py
+-rw-r--r--   0        0        0     4034 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/context_utils.py
+-rw-r--r--   0        0        0     2389 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/csvutils.py
+-rw-r--r--   0        0        0      486 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/curienamespace.py
+-rw-r--r--   0        0        0     1325 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/dataclass_extensions_376.py
+-rw-r--r--   0        0        0      433 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/dictutils.py
+-rw-r--r--   0        0        0     2554 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/distroutils.py
+-rw-r--r--   0        0        0     3683 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/enumerations.py
+-rw-r--r--   0        0        0     6755 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/eval_utils.py
+-rw-r--r--   0        0        0     6594 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/formatutils.py
+-rw-r--r--   0        0        0     5672 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/inference_utils.py
+-rw-r--r--   0        0        0     1976 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/introspection.py
+-rw-r--r--   0        0        0    11553 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/metamodelcore.py
+-rw-r--r--   0        0        0    10580 2023-05-13 02:39:28.124564 linkml_runtime-1.5.3/linkml_runtime/utils/namespaces.py
+-rw-r--r--   0        0        0     2870 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/pattern.py
+-rw-r--r--   0        0        0     6697 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/permissiblevalueimpl.py
+-rw-r--r--   0        0        0     4720 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/ruleutils.py
+-rw-r--r--   0        0        0     2287 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/schema_as_dict.py
+-rw-r--r--   0        0        0     9312 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/schema_builder.py
+-rw-r--r--   0        0        0     2815 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/schemaops.py
+-rw-r--r--   0        0        0    66900 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/schemaview.py
+-rw-r--r--   0        0        0     4327 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/schemaview_cli.py
+-rw-r--r--   0        0        0      368 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/slot.py
+-rw-r--r--   0        0        0      641 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/strictness.py
+-rw-r--r--   0        0        0     1405 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/walker_utils.py
+-rw-r--r--   0        0        0    19743 2023-05-13 02:39:28.128564 linkml_runtime-1.5.3/linkml_runtime/utils/yamlutils.py
+-rw-r--r--   0        0        0     1848 2023-05-13 02:39:44.068446 linkml_runtime-1.5.3/pyproject.toml
+-rw-r--r--   0        0        0     3715 1970-01-01 00:00:00.000000 linkml_runtime-1.5.3/PKG-INFO
```

### Comparing `linkml_runtime-1.5.2/LICENSE` & `linkml_runtime-1.5.3/LICENSE`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/README.md` & `linkml_runtime-1.5.3/README.md`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/__init__.py` & `linkml_runtime-1.5.3/linkml_runtime/__init__.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/dumpers/csv_dumper.py` & `linkml_runtime-1.5.3/linkml_runtime/dumpers/csv_dumper.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 import io
 import yaml
 import json
-from typing import Dict, List, Any
+from typing import Union
+from pydantic import BaseModel
 
 from linkml_runtime.dumpers.dumper_root import Dumper
 from linkml_runtime.dumpers.json_dumper import JSONDumper
 from linkml_runtime.utils.yamlutils import YAMLRoot
 from linkml_runtime.linkml_model.meta import SlotDefinitionName, SchemaDefinition
 from linkml_runtime.utils.schemaview import SchemaView
 
 from linkml_runtime.utils.csvutils import GlobalConfig, get_configmap
 from json_flattener import flatten_to_csv
 
 
 class CSVDumper(Dumper):
 
-    def dumps(self, element: YAMLRoot,
+    def dumps(self, element: Union[BaseModel, YAMLRoot],
               index_slot: SlotDefinitionName = None,
               schema: SchemaDefinition = None,
               schemaview: SchemaView = None,
               **kwargs) -> str:
         """ Return element formatted as CSV lines """
         json_dumper = JSONDumper()
         element_j = json.loads(json_dumper.dumps(element))
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/dumpers/json_dumper.py` & `linkml_runtime-1.5.3/linkml_runtime/dumpers/json_dumper.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,76 +1,86 @@
 import json
 from decimal import Decimal
-from typing import Dict
+from typing import Dict, Union
+from pydantic import BaseModel
 
 from deprecated.classic import deprecated
 
 from linkml_runtime.dumpers.dumper_root import Dumper
 from linkml_runtime.utils import formatutils
 from linkml_runtime.utils.context_utils import CONTEXTS_PARAM_TYPE
 from linkml_runtime.utils.formatutils import remove_empty_items
 from linkml_runtime.utils.yamlutils import YAMLRoot, as_json_object
 from jsonasobj2 import JsonObj
 
+
 class JSONDumper(Dumper):
 
-    def dump(self, element: YAMLRoot, to_file: str, contexts: CONTEXTS_PARAM_TYPE = None, **kwargs) -> None:
+    def dump(self, element: Union[BaseModel, YAMLRoot], to_file: str, contexts: CONTEXTS_PARAM_TYPE = None,
+             **kwargs) -> None:
         """
         Write element as json to to_file
         :param element: LinkML object to be serialized as YAML
         :param to_file: file to write to
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
             * JSON String
             * dict
             * JSON Object
             * A list containing elements of any type named above
         """
+        if isinstance(element, BaseModel):
+            element = element.dict()
         super().dump(element, to_file, contexts=contexts, **kwargs)
 
-    def dumps(self, element: YAMLRoot, contexts: CONTEXTS_PARAM_TYPE = None, inject_type=True) -> str:
+    def dumps(self, element: Union[BaseModel, YAMLRoot], contexts: CONTEXTS_PARAM_TYPE = None, inject_type=True) -> str:
         """
         Return element as a JSON or a JSON-LD string
         :param element: LinkML object to be emitted
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
             * JSON String
             * dict
             * JSON Object
             * A list containing elements of any type named above
         :param inject_type: if True (default), add a @type at the top level
         :return: JSON Object representing the element
         """
+
         def default(o):
+            if isinstance(o, BaseModel):
+                return remove_empty_items(o.dict(), hide_protected_keys=True)
             if isinstance(o, YAMLRoot):
                 return remove_empty_items(o, hide_protected_keys=True)
             elif isinstance(o, Decimal):
                 # https://stackoverflow.com/questions/1960516/python-json-serialize-a-decimal-object
                 return str(o)
             else:
                 return json.JSONDecoder().decode(o)
+        if isinstance(element, BaseModel):
+            element = element.dict()
         return json.dumps(as_json_object(element, contexts, inject_type=inject_type),
                           default=default,
                           ensure_ascii=False,
                           indent='  ')
 
-
     @staticmethod
     @deprecated("Use `utils/formatutils/remove_empty_items` instead")
     def remove_empty_items(obj: Dict) -> Dict:
         """
         Remove empty items from obj
         :param obj:
         :return: copy of dictionary with empty lists/dicts and Nones removed
         """
         return formatutils.remove_empty_items(obj, hide_protected_keys=True)
 
-    def to_json_object(self, element: YAMLRoot, contexts: CONTEXTS_PARAM_TYPE = None, inject_type=True) -> JsonObj:
+    def to_json_object(self, element: Union[BaseModel, YAMLRoot], contexts: CONTEXTS_PARAM_TYPE = None,
+                       inject_type=True) -> JsonObj:
         """
         As dumps(), except returns a JsonObj, not a string
 
         :param element: LinkML object to be emitted
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
@@ -79,23 +89,23 @@
             * JSON Object
             * A list containing elements of any type named above
         :param inject_type: if True (default), add a @type at the top level
         :return: JSON Object representing the element
         """
         return as_json_object(element, contexts, inject_type=inject_type)
 
-    def to_dict(self, element: YAMLRoot, **kwargs) -> JsonObj:
+    def to_dict(self, element: Union[BaseModel, YAMLRoot], **kwargs) -> JsonObj:
         """
         As dumps(), except returns a JsonObj, not a string
 
         :param element: LinkML object to be emitted
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
             * JSON String
             * dict
             * JSON Object
             * A list containing elements of any type named above
         :param inject_type: if True (default), add a @type at the top level
         :return: JSON Object representing the element
         """
-        return json.loads(self.dumps(element, inject_type=False, **kwargs))
+        return json.loads(self.dumps(element, inject_type=False, **kwargs))
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/dumpers/rdf_dumper.py` & `linkml_runtime-1.5.3/linkml_runtime/dumpers/rdf_dumper.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 import json
-from typing import Optional
+from typing import Optional, Union
+from pydantic import BaseModel
 
 from hbreader import hbread
 from rdflib import Graph
 
 
 from linkml_runtime.dumpers.dumper_root import Dumper
 from linkml_runtime.utils.context_utils import CONTEXTS_PARAM_TYPE, CONTEXT_TYPE
 from linkml_runtime.utils.formatutils import remove_empty_items
 from linkml_runtime.utils.yamlutils import YAMLRoot
 
 
 class RDFDumper(Dumper):
-    def as_rdf_graph(self, element: YAMLRoot, contexts: CONTEXTS_PARAM_TYPE, namespaces: CONTEXT_TYPE = None) -> Graph:
+    def as_rdf_graph(self, element: Union[BaseModel, YAMLRoot], contexts: CONTEXTS_PARAM_TYPE, namespaces: CONTEXT_TYPE = None) -> Graph:
         """
         Convert element into an RDF graph guided by the context(s) in contexts
         :param element: element to represent in RDF
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
             * JSON String
@@ -59,33 +60,37 @@
                             else:
                                 continue
                         if not pfx.startswith('@'):
                             g.bind(pfx, ns)
 
         return g
 
-    def dump(self, element: YAMLRoot, to_file: str, contexts: CONTEXTS_PARAM_TYPE = None, fmt: str = 'turtle') -> None:
+    def dump(self, element: Union[BaseModel, YAMLRoot], to_file: str, contexts: CONTEXTS_PARAM_TYPE = None, fmt: str = 'turtle') -> None:
         """
         Write element as rdf to to_file
         :param element: LinkML object to be emitted
         :param to_file: file to write to
         :param contexts: JSON-LD context(s) in the form of:
             * file name
             * URL
             * JSON String
             * dict
             * JSON Object
             * A list containing elements of any type named above
         :param fmt: RDF format
         """
+        if isinstance(element, BaseModel):
+            element = element.dict()
         super().dump(element, to_file, contexts=contexts, fmt=fmt)
 
-    def dumps(self, element: YAMLRoot, contexts: CONTEXTS_PARAM_TYPE = None, fmt: Optional[str] = 'turtle') -> str:
+    def dumps(self, element: Union[BaseModel, YAMLRoot], contexts: CONTEXTS_PARAM_TYPE = None, fmt: Optional[str] = 'turtle') -> str:
         """
         Convert element into an RDF graph guided by the context(s) in contexts
         :param element: element to represent in RDF
         :param contexts: JSON-LD context(s) in the form of a file or URL, a json string or a json obj
         :param fmt: rdf format
         :return: rdflib Graph containing element
         """
+        if isinstance(element, BaseModel):
+            element = element.dict()
         return self.as_rdf_graph(remove_empty_items(element, hide_protected_keys=True), contexts).\
             serialize(format=fmt)
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/dumpers/rdflib_dumper.py` & `linkml_runtime-1.5.3/linkml_runtime/dumpers/rdflib_dumper.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import logging
 import urllib
 from abc import abstractmethod
-from typing import Optional, Any, Dict
+from typing import Optional, Any, Dict, Union
+from pydantic import BaseModel
 
 from rdflib import Graph, URIRef, XSD
 from rdflib.term import Node, BNode, Literal
 from rdflib.namespace import RDF
 
 
 from linkml_runtime.dumpers.dumper_root import Dumper
@@ -19,15 +20,15 @@
     Dumps from elements (instances of a LinkML model) to an rdflib Graph
 
     Note: this should be used in place of rdf_loader for now
 
     This requires a SchemaView object
 
     """
-    def as_rdf_graph(self, element: YAMLRoot, schemaview: SchemaView, prefix_map: Dict[str, str] = None) -> Graph:
+    def as_rdf_graph(self, element: Union[BaseModel, YAMLRoot], schemaview: SchemaView, prefix_map: Dict[str, str] = None) -> Graph:
         """
         Dumps from element to an rdflib Graph,
         following a schema
 
         :param element: element to represent in RDF
         :param schemaview:
         :param prefix_map:
@@ -132,15 +133,15 @@
                     graph.add((element_uri, slot_uri, v_node))
                     if slot.designates_type:
                         type_added = True
         if not type_added:
             graph.add((element_uri, RDF.type, URIRef(schemaview.get_uri(cn, expand=True))))
         return element_uri
 
-    def dump(self, element: YAMLRoot,
+    def dump(self, element: Union[BaseModel, YAMLRoot],
              to_file: str,
              schemaview: SchemaView = None,
              fmt: str = 'turtle', prefix_map: Dict[str, str] = None, **args) -> None:
         """
         Write element as rdf to to_file
 
         :param element: element to represent in RDF
@@ -148,15 +149,15 @@
         :param schemaview:
         :param fmt:
         :param prefix_map:
         :return:
         """
         super().dump(element, to_file, schemaview=schemaview, fmt=fmt, prefix_map=prefix_map)
 
-    def dumps(self, element: YAMLRoot, schemaview: SchemaView = None,
+    def dumps(self, element: Union[BaseModel, YAMLRoot], schemaview: SchemaView = None,
               fmt: Optional[str] = 'turtle', prefix_map: Dict[str, str] = None) -> str:
         """
         Convert element into an RDF graph guided by the schema
 
         :param element:
         :param schemaview:
         :param fmt:
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/index/object_index.py` & `linkml_runtime-1.5.3/linkml_runtime/index/object_index.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/__init__.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/__init__.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/annotations.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/annotations.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/extensions.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/extensions.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/graphql/meta.graphql` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/graphql/meta.graphql`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/annotations.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/annotations.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/extensions.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/extensions.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/mappings.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/mappings.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/meta.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/meta.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/types.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/types.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/units.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/units.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/json/validation.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/json/validation.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/annotations.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/annotations.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/annotations.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/annotations.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/extensions.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/extensions.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/extensions.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/extensions.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/mappings.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/mappings.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/mappings.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/mappings.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/meta.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/meta.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/meta.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/meta.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/types.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/types.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/types.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/types.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/units.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/units.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/units.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/units.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/validation.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/validation.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonld/validation.model.context.jsonld` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonld/validation.model.context.jsonld`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/annotations.schema.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/annotations.schema.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/extensions.schema.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/extensions.schema.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/meta.schema.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/meta.schema.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/units.schema.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/units.schema.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/jsonschema/validation.schema.json` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/jsonschema/validation.schema.json`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/linkml_files.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/linkml_files.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/mappings.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/mappings.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/meta.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/meta.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/annotations.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/annotations.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/extensions.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/extensions.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/mappings.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/mappings.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/meta.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/meta.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/types.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/types.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/units.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/units.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/model/schema/validation.yaml` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/model/schema/validation.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/owl/meta.owl.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/owl/meta.owl.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/annotations.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/annotations.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/annotations.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/annotations.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/extensions.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/extensions.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/extensions.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/extensions.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/mappings.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/mappings.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/mappings.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/mappings.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/meta.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/meta.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/meta.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/meta.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/types.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/types.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/types.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/types.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/units.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/units.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/units.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/units.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/validation.model.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/validation.model.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/rdf/validation.ttl` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/rdf/validation.ttl`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/annotations.shex` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/annotations.shex`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/annotations.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/annotations.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/extensions.shex` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/extensions.shex`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/extensions.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/extensions.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/mappings.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/mappings.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/meta.shex` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/meta.shex`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/meta.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/meta.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/types.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/types.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/units.shex` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/units.shex`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/units.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/units.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/validation.shex` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/validation.shex`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/shex/validation.shexj` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/shex/validation.shexj`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/types.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/types.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/units.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/units.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/linkml_model/validation.py` & `linkml_runtime-1.5.3/linkml_runtime/linkml_model/validation.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/context_flattener.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/context_flattener.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/csv_loader.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/csv_loader.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from json_flattener import unflatten_from_csv, KeyConfig, GlobalConfig, Serializer
 import json
 from typing import Type, Union, List
 from linkml_runtime.utils.yamlutils import YAMLRoot
+from pydantic import BaseModel
 
 from linkml_runtime.loaders.loader_root import Loader
 from linkml_runtime.loaders.json_loader import JSONLoader
 from linkml_runtime.linkml_model.meta import SlotDefinitionName, SchemaDefinition, ClassDefinition
 from linkml_runtime.utils.yamlutils import YAMLRoot
 from linkml_runtime.utils.schemaview import SchemaView
 from linkml_runtime.utils.csvutils import get_configmap
@@ -13,28 +14,28 @@
 class CSVLoader(Loader):
 
     def load_any(self, *args, **kwargs) -> Union[YAMLRoot, List[YAMLRoot]]:
         return self.load(*args, **kwargs)
 
 
     def loads(self, input,
-              target_class: Type[YAMLRoot],
+              target_class: Type[Union[BaseModel, YAMLRoot]],
               index_slot: SlotDefinitionName = None,
               schema: SchemaDefinition = None,
               schemaview: SchemaView = None,
               **kwargs) -> str:
         if schemaview is None:
             schemaview = SchemaView(schema)
         configmap = get_configmap(schemaview, index_slot)
         config = GlobalConfig(key_configs=configmap)
         objs = unflatten_from_csv(input, config=config, **kwargs)
         return JSONLoader().loads(json.dumps({index_slot: objs}), target_class=target_class)
 
     def load(self, source: str,
-             target_class: Type[YAMLRoot],
+             target_class: Type[Union[BaseModel, YAMLRoot]],
              index_slot: SlotDefinitionName = None,
              schema: SchemaDefinition = None,
              schemaview: SchemaView = None,
              **kwargs) -> str:
         if schemaview is None:
             schemaview = SchemaView(schema)
         configmap = get_configmap(schemaview, index_slot)
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/json_loader.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/json_loader.py`

 * *Files 16% similar despite different names*

```diff
@@ -2,20 +2,20 @@
 import logging
 from typing import Union, TextIO, Optional, Dict, Type, List
 
 from hbreader import FileInfo
 
 from linkml_runtime.loaders.loader_root import Loader
 from linkml_runtime.utils.yamlutils import YAMLRoot
-
+from pydantic import BaseModel
 
 class JSONLoader(Loader):
 
-    def load_any(self, source: Union[str, dict, TextIO], target_class: Type[YAMLRoot], *, base_dir: Optional[str] = None,
-             metadata: Optional[FileInfo] = None, **_) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def load_any(self, source: Union[str, dict, TextIO], target_class: Type[Union[BaseModel, YAMLRoot]], *, base_dir: Optional[str] = None,
+             metadata: Optional[FileInfo] = None, **_) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         def loader(data: Union[str, dict], _: FileInfo) -> Optional[Dict]:
             data_as_dict = json.loads(data) if isinstance(data, str) else data
             if isinstance(data_as_dict, list):
                 return self.json_clean(data_as_dict)
             typ = data_as_dict.pop('@type', None)
             if typ and typ != target_class.__name__:
                 logging.warning(f"Warning: input type mismatch. Expected: {target_class.__name__}, Actual: {typ}")
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/loader_root.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/loader_root.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from abc import ABC, abstractmethod
 from typing import TextIO, Union, Optional, Callable, Dict, Type, Any, List
 
+from pydantic import BaseModel
 from hbreader import FileInfo, hbread
 from jsonasobj2 import as_dict, JsonObj
 
 from linkml_runtime.utils.yamlutils import YAMLRoot
 
 
 class Loader(ABC):
@@ -32,17 +33,17 @@
                 else:
                     Loader.json_clean(v)
         return inp
 
     def load_source(self,
                     source: Union[str, dict, TextIO],
                     loader: Callable[[Union[str, Dict], FileInfo], Optional[Union[Dict, List]]],
-                    target_class: Type[YAMLRoot],
+                    target_class: Union[Type[YAMLRoot], Type[BaseModel]],
                     accept_header: Optional[str] = "text/plain, application/yaml;q=0.9",
-                    metadata: Optional[FileInfo] = None) -> Optional[Union[YAMLRoot, List[YAMLRoot]]]:
+                    metadata: Optional[FileInfo] = None) -> Optional[Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]]:
         """ Base loader - convert a file, url, string, open file handle or dictionary into an instance
         of target_class
 
         :param source: URL, file name, block of text, Existing Object or open file handle
         :param loader: Take a stringified image or a dictionary and return a loadable dictionary
         :param target_class: Destination class
         :param accept_header: Accept header to use if doing a request
@@ -55,70 +56,79 @@
         if metadata is None:
             metadata = FileInfo()
         if not isinstance(source, dict):
             data = hbread(source, metadata, metadata.base_path, accept_header)
         else:
             data = source
         data_as_dict = loader(data, metadata)
+
         if data_as_dict:
             if isinstance(data_as_dict, list):
-                return [target_class(**as_dict(x)) for x in data_as_dict]
+               if issubclass(target_class, YAMLRoot):
+                   return [target_class(**as_dict(x)) for x in data_as_dict]
+               elif issubclass(target_class, BaseModel):
+                   return [target_class.parse_obj(**as_dict(x)) for x in data_as_dict]
+               else:
+                   raise ValueError(f'Cannot load list of {target_class}')
             elif isinstance(data_as_dict, dict):
-                return target_class(**data_as_dict)
+                if issubclass(target_class, BaseModel):
+                    return target_class.parse_obj(data_as_dict)
+                else:
+                    return target_class(**data_as_dict)
             elif isinstance(data_as_dict, JsonObj):
                 return [target_class(**as_dict(x)) for x in data_as_dict]
             else:
                 raise ValueError(f'Unexpected type {data_as_dict}')
         else:
             return None
 
-    def load(self, *args, **kwargs) -> YAMLRoot:
+    def load(self, *args, **kwargs) -> Union[BaseModel, YAMLRoot]:
         """
         Load source as an instance of target_class
 
         :param source: source file/text/url to load
         :param target_class: destination class
         :param base_dir: scoping directory for source if it is a file or url
         :param metadata: metadata about the source
         :param _: extensions
         :return: instance of target_class
         """
         results = self.load_any(*args, **kwargs)
-        if isinstance(results, YAMLRoot):
+        if isinstance(results, BaseModel) or isinstance(results, YAMLRoot):
             return results
         else:
-            raise ValueError(f'Result is not an instance of YAMLRoot: {type(results)}')
+            raise ValueError(f'Result is not an instance of BaseModel or YAMLRoot: {type(results)}')
 
     @abstractmethod
-    def load_any(self, source: Union[str, dict, TextIO], target_class: Type[YAMLRoot], *, base_dir: Optional[str] = None,
-             metadata: Optional[FileInfo] = None, **_) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def load_any(self, source: Union[str, dict, TextIO], target_class: Type[Union[BaseModel, YAMLRoot]], *, base_dir: Optional[str] = None,
+             metadata: Optional[FileInfo] = None, **_) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         """
         Load source as an instance of target_class, or list of instances of target_class
 
         @param source: source file/text/url to load
         @param target_class: destination class
         @param base_dir: scoping directory for source if it is a file or url
         @param metadata: metadata about the source
         @param _: extensions
         @return: instance of target_class
         """
         raise NotImplementedError()
 
-    def loads_any(self, source: str, target_class: Type[YAMLRoot], *, metadata: Optional[FileInfo] = None, **_) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def loads_any(self, source: str, target_class: Type[Union[BaseModel, YAMLRoot]], *, metadata: Optional[FileInfo] = None, **_) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         """
         Load source as a string as an instance of target_class, or list of instances of target_class
         @param source: source
         @param target_class: destination class
         @param metadata: metadata about the source
         @param _: extensions
         @return: instance of taarget_class
         """
         return self.load_any(source, target_class, metadata=metadata)
 
-    def loads(self, source: str, target_class: Type[YAMLRoot], *, metadata: Optional[FileInfo] = None, **_) -> YAMLRoot:
+    def loads(self, source: str, target_class: Type[Union[BaseModel, YAMLRoot]], *, metadata: Optional[FileInfo] = None, **_) -> Union[BaseModel, YAMLRoot]:
         """
         Load source as a string
         :param source: source
         :param target_class: destination class
         :param metadata: metadata about the source
         :param _: extensions
         :return: instance of taarget_class
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/rdf_loader.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/rdf_loader.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,30 +1,32 @@
 from typing import Union, TextIO, Optional, Type, List
 
 from hbreader import FileInfo
 
 from linkml_runtime.loaders.loader_root import Loader
 from linkml_runtime.utils.context_utils import CONTEXTS_PARAM_TYPE
 from linkml_runtime.utils.yamlutils import YAMLRoot
+from pydantic import BaseModel
 from rdflib import Graph
 
 from linkml_runtime.loaders.requests_ssl_patch import no_ssl_verification
 
 # TODO: figure out what mime types go here.  I think we can find the complete set in rdflib
 RDF_MIME_TYPES = "application/x-turtle;q=0.9, application/rdf+n3;q=0.8, application/rdf+xml;q=0.5, text/plain;q=0.1"
 
 
 class RDFLoader(Loader):
 
-    def load_any(self, *args, **kwargs) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def load_any(self, *args, **kwargs) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         return self.load(*args, **kwargs)
 
-    def load(self, source: Union[str, TextIO, Graph], target_class: Type[YAMLRoot], *, base_dir: Optional[str] = None,
+
+    def load(self, source: Union[str, TextIO, Graph], target_class: Type[Union[BaseModel, YAMLRoot]], *, base_dir: Optional[str] = None,
              contexts: CONTEXTS_PARAM_TYPE = None, fmt: Optional[str] = 'turtle',
-             metadata: Optional[FileInfo] = None) -> YAMLRoot:
+             metadata: Optional[FileInfo] = None) -> Union[BaseModel, YAMLRoot]:
         """
         Load the RDF in source into the python target_class structure
         :param source: RDF data source. Can be a URL, a file name, an RDF string, an open handle or an existing graph
         :param base_dir: Base directory that can be used if file name or URL.  This is copied into metadata if present
         :param target_class: LinkML class to load the RDF into
         :param contexts: JSON-LD context(s) to use to generate the JSON that will be loaded into target_class.  This is
         optional because, if source is in JSON-LD format, it is possible that the contexts are already there
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/rdflib_loader.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/rdflib_loader.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,33 +11,34 @@
 
 from linkml_runtime import MappingError, DataNotFoundError
 from linkml_runtime.linkml_model import ClassDefinitionName, TypeDefinition, EnumDefinition, ClassDefinition
 from linkml_runtime.loaders.loader_root import Loader
 from linkml_runtime.utils.formatutils import underscore
 from linkml_runtime.utils.schemaview import SchemaView, SlotDefinition
 from linkml_runtime.utils.yamlutils import YAMLRoot
+from pydantic import BaseModel
 
 VALID_SUBJECT = Union[URIRef, BNode]
 ANYDICT = Dict[str, Any]
 
 @dataclass
 class Pointer:
     obj: str
 
 class RDFLibLoader(Loader):
     """
     Loads objects from rdflib Graphs into the python target_class structure
 
     Note: this is a more complete replacement for rdf_loader
     """
-    def from_rdf_graph(self, graph: Graph, schemaview: SchemaView, target_class: Type[YAMLRoot],
+    def from_rdf_graph(self, graph: Graph, schemaview: SchemaView, target_class: Type[Union[BaseModel, YAMLRoot]],
                        prefix_map: Dict[str, str] = None,
                        cast_literals: bool = True,
                        allow_unprocessed_triples: bool = True,
-                       ignore_unmapped_predicates: bool = False) -> List[YAMLRoot]:
+                       ignore_unmapped_predicates: bool = False) -> List[Union[BaseModel, YAMLRoot]]:
         """
         Loads objects from graph into lists of the python target_class structure,
         recursively walking RDF graph from instances of target_class.
 
         :param graph: rdflib Graph that holds instances of target_class
         :param schemaview: schema to which graph conforms
         :param target_class: class which root nodes should instantiate
@@ -219,20 +220,20 @@
     def _uri_to_id(self, node: VALID_SUBJECT, id_slot: SlotDefinition, schemaview: SchemaView) -> str:
         if schemaview.is_slot_percent_encoded(id_slot):
             return urllib.parse.unquote(node).replace(schemaview.namespaces()._base, "")
         else:
             return schemaview.namespaces().curie_for(node)
 
 
-    def load(self, source: Union[str, TextIO, Graph], target_class: Type[YAMLRoot], *,
+    def load(self, source: Union[str, TextIO, Graph], target_class: Type[Union[BaseModel, YAMLRoot]], *,
              schemaview: SchemaView = None,
              prefix_map: Dict[str, str] = None,
              fmt: Optional[str] = 'turtle',
              metadata: Optional[FileInfo] = None,
-             **kwargs) -> YAMLRoot:
+             **kwargs) -> Union[BaseModel, YAMLRoot]:
         """
         Load the RDF in source into the python target_class structure
 
         The assumption of all loaders is that the source contains exactly one instance of the
         target class. To load from graphs with multiple instances, use from_rdf_graph
 
         :param source: RDF data source. Can be a file name, an open handle or an existing graph
@@ -253,14 +254,14 @@
             else:
                 g.parse(source, format=fmt)
         objs = self.from_rdf_graph(g, schemaview=schemaview, target_class=target_class, prefix_map=prefix_map, **kwargs)
         if len(objs) != 1:
             raise DataNotFoundError(f'Got {len(objs)} of type {target_class} from source, expected exactly 1')
         return objs[0]
 
-    def loads(self, source: str, **kwargs) -> YAMLRoot:
+    def loads(self, source: str, **kwargs) -> Union[BaseModel, YAMLRoot]:
         return self.load(source, **kwargs)
 
-    def load_any(self, source: str, **kwargs) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def load_any(self, source: str, **kwargs) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         return self.load(source, **kwargs)
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/requests_ssl_patch.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/requests_ssl_patch.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/loaders/yaml_loader.py` & `linkml_runtime-1.5.3/linkml_runtime/loaders/yaml_loader.py`

 * *Files 18% similar despite different names*

```diff
@@ -3,22 +3,25 @@
 from typing import Union, TextIO, Optional, Dict, Type, List
 
 import yaml
 from hbreader import FileInfo
 
 from linkml_runtime.loaders.loader_root import Loader
 from linkml_runtime.utils.yamlutils import YAMLRoot, DupCheckYamlLoader
-
+from pydantic import BaseModel
 
 class YAMLLoader(Loader):
     """
     A Loader that is capable of instantiating LinkML data objects from a YAML file
     """
 
-    def load_any(self, source: Union[str, dict, TextIO], target_class: Type[YAMLRoot], *, base_dir: Optional[str] = None,
+    def load_any(self,
+                 source: Union[str, dict, TextIO],
+                 target_class: Union[Type[YAMLRoot],Type[BaseModel]],
+                 *, base_dir: Optional[str] = None,
                  metadata: Optional[FileInfo] = None, **_) -> Union[YAMLRoot, List[YAMLRoot]]:
         def loader(data: Union[str, dict], source_file: FileInfo) -> Optional[Dict]:
             if isinstance(data, str):
                 data = StringIO(data)
                 if source_file and source_file.source_file:
                     data.name = os.path.relpath(source_file.source_file, source_file.base_path)
                 return yaml.load(data, DupCheckYamlLoader)
@@ -28,15 +31,15 @@
         if not metadata:
             metadata = FileInfo()
         if base_dir and not metadata.base_path:
             metadata.base_path = base_dir
         return self.load_source(source, loader, target_class, accept_header="text/yaml, application/yaml;q=0.9",
                                 metadata=metadata)
 
-    def loads_any(self, source: str, target_class: Type[YAMLRoot], *, metadata: Optional[FileInfo] = None, **_) -> Union[YAMLRoot, List[YAMLRoot]]:
+    def loads_any(self, source: str, target_class: Type[Union[BaseModel, YAMLRoot]], *, metadata: Optional[FileInfo] = None, **_) -> Union[BaseModel, YAMLRoot, List[BaseModel], List[YAMLRoot]]:
         """
         Load source as a string
         @param source: source
         @param target_class: destination class
         @param metadata: metadata about the source
         @param _: extensions
         @return: instance of taarget_class
```

### Comparing `linkml_runtime-1.5.2/linkml_runtime/processing/referencevalidator.py` & `linkml_runtime-1.5.3/linkml_runtime/processing/referencevalidator.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/processing/validation_datamodel.py` & `linkml_runtime-1.5.3/linkml_runtime/processing/validation_datamodel.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/processing/validation_datamodel.yaml` & `linkml_runtime-1.5.3/linkml_runtime/processing/validation_datamodel.yaml`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/comparefiles.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/comparefiles.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/compile_python.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/compile_python.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/context_utils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/context_utils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/csvutils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/csvutils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/dataclass_extensions_376.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/dataclass_extensions_376.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/distroutils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/distroutils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/enumerations.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/enumerations.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/eval_utils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/eval_utils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/formatutils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/formatutils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/inference_utils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/inference_utils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/introspection.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/introspection.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/metamodelcore.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/metamodelcore.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/namespaces.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/namespaces.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/pattern.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/pattern.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/permissiblevalueimpl.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/permissiblevalueimpl.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/ruleutils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/ruleutils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/schema_as_dict.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/schema_as_dict.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/schema_builder.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/schema_builder.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/schemaops.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/schemaops.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/schemaview.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/schemaview.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/schemaview_cli.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/schemaview_cli.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/strictness.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/strictness.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/walker_utils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/walker_utils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/linkml_runtime/utils/yamlutils.py` & `linkml_runtime-1.5.3/linkml_runtime/utils/yamlutils.py`

 * *Files identical despite different names*

### Comparing `linkml_runtime-1.5.2/pyproject.toml` & `linkml_runtime-1.5.3/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "linkml-runtime"
-version = "v1.5.2"
+version = "v1.5.3"
 description = "Runtime environment for LinkML, the Linked open data modeling language"
 authors = [
     "Chris Mungall <cjmungall@lbl.gov>",
     "Harold Solbrig <solbrig@jhu.edu>",
     "Sierra Moxon <smoxon@lbl.gov>",
     "Bill Duncan <wdduncan@gmail.com>",
     "Harshad Hegde <hhegde@lbl.gov>"
@@ -49,15 +49,16 @@
 jsonasobj2 = "==1.*,>=1.0.0,>=1.0.4"
 jsonschema = ">=3.2.0"
 prefixcommons = ">=0.1.12"
 pyyaml = "*"
 rdflib = ">=6.0.0"
 requests = "*"
 prefixmaps = ">=0.1.4"
-curies = "^0.4.0"
+curies = ">=0.5.4"
+pydantic = "^1.10.2"
 
 [tool.poetry.dev-dependencies]
 coverage = "^6.2"
 importlib-metadata = {version = "^4.12.0", python = "<3.8"}
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
```

### Comparing `linkml_runtime-1.5.2/PKG-INFO` & `linkml_runtime-1.5.3/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: linkml-runtime
-Version: 1.5.2
+Version: 1.5.3
 Summary: Runtime environment for LinkML, the Linked open data modeling language
 Home-page: https://github.com/linkml/linkml-runtime
 Keywords: linkml,metamodel,schema visualization,rdf,owl,yaml
 Author: Chris Mungall
 Author-email: cjmungall@lbl.gov
 Requires-Python: >=3.7.6,<4.0.0
 Classifier: Development Status :: 5 - Production/Stable
@@ -19,22 +19,23 @@
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Dist: click
-Requires-Dist: curies (>=0.4.0,<0.5.0)
+Requires-Dist: curies (>=0.5.4)
 Requires-Dist: deprecated
 Requires-Dist: hbreader
 Requires-Dist: json-flattener (>=0.1.9)
 Requires-Dist: jsonasobj2 (>=1.0.4,<2.0.0)
 Requires-Dist: jsonschema (>=3.2.0)
 Requires-Dist: prefixcommons (>=0.1.12)
 Requires-Dist: prefixmaps (>=0.1.4)
+Requires-Dist: pydantic (>=1.10.2,<2.0.0)
 Requires-Dist: pyyaml
 Requires-Dist: rdflib (>=6.0.0)
 Requires-Dist: requests
 Project-URL: Documentation, https://github.com/linkml/linkml-runtime
 Project-URL: Repository, https://github.com/linkml/linkml-runtime
 Description-Content-Type: text/markdown
```

