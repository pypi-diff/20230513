# Comparing `tmp/sqllineage-1.4.2.tar.gz` & `tmp/sqllineage-1.4.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sqllineage-1.4.2.tar", last modified: Sat Apr 22 15:23:10 2023, max compression
+gzip compressed data, was "sqllineage-1.4.3.tar", last modified: Sat May 13 13:46:21 2023, max compression
```

## Comparing `sqllineage-1.4.2.tar` & `sqllineage-1.4.3.tar`

### file list

```diff
@@ -1,224 +1,224 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1057 2023-04-22 15:21:12.000000 sqllineage-1.4.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      137 2023-04-22 15:21:12.000000 sqllineage-1.4.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     7286 2023-04-22 15:23:10.091654 sqllineage-1.4.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6479 2023-04-22 15:21:12.000000 sqllineage-1.4.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-22 15:23:10.091654 sqllineage-1.4.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     3159 2023-04-22 15:21:12.000000 sqllineage-1.4.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineage/
--rw-r--r--   0 runner    (1001) docker     (123)      959 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineage/build/
--rw-r--r--   0 runner    (1001) docker     (123)      644 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/asset-manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)   146541 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/editor.worker.js
--rw-r--r--   0 runner    (1001) docker     (123)      149 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/editor.worker.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)   622794 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/editor.worker.js.map
--rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-04-22 15:21:46.000000 sqllineage-1.4.2/sqllineage/build/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (123)      736 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     5347 2023-04-22 15:21:46.000000 sqllineage-1.4.2/sqllineage/build/logo192.png
--rw-r--r--   0 runner    (1001) docker     (123)     9664 2023-04-22 15:21:46.000000 sqllineage-1.4.2/sqllineage/build/logo512.png
--rw-r--r--   0 runner    (1001) docker     (123)      494 2023-04-22 15:21:46.000000 sqllineage-1.4.2/sqllineage/build/manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-04-22 15:21:46.000000 sqllineage-1.4.2/sqllineage/build/robots.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.051654 sqllineage-1.4.2/sqllineage/build/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineage/build/static/css/
--rw-r--r--   0 runner    (1001) docker     (123)    69444 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/css/main.c1b86fee.css
--rw-r--r--   0 runner    (1001) docker     (123)   146886 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/css/main.c1b86fee.css.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.063654 sqllineage-1.4.2/sqllineage/build/static/js/
--rw-r--r--   0 runner    (1001) docker     (123)    18303 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/js/333.97bcedbd.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)    45386 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/js/333.97bcedbd.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)  3567447 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123) 12937379 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/build/static/media/
--rw-r--r--   0 runner    (1001) docker     (123)    62792 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage/build/static/media/codicon.4168b9c11e5075e9cfe6.ttf
--rw-r--r--   0 runner    (1001) docker     (123)     3448 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      493 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/analyzer.py
--rw-r--r--   0 runner    (1001) docker     (123)    11390 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/holders.py
--rw-r--r--   0 runner    (1001) docker     (123)     7062 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/parser/
--rw-r--r--   0 runner    (1001) docker     (123)     2386 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2818 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/analyzer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/
--rw-r--r--   0 runner    (1001) docker     (123)      245 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3319 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/cte_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/ddl_alter_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1299 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/ddl_drop_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     3562 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_insert_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_merge_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_select_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     4946 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/lineage_holder_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/noop_extractor.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)      349 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     6407 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/source.py
--rw-r--r--   0 runner    (1001) docker     (123)     1513 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/swap_partition.py
--rw-r--r--   0 runner    (1001) docker     (123)     4836 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/target.py
--rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/holder_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     7448 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/models.py
--rw-r--r--   0 runner    (1001) docker     (123)    15960 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.075654 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/
--rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11020 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/analyzer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.079654 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)      349 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1570 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1493 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/cte.py
--rw-r--r--   0 runner    (1001) docker     (123)     4332 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/source.py
--rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/swap_partition.py
--rw-r--r--   0 runner    (1001) docker     (123)     2737 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/target.py
--rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/holder_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     7344 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     7518 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/core/parser/sqlparse/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineage/data/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.087654 sqllineage-1.4.2/sqllineage/data/tpcds/
--rw-r--r--   0 runner    (1001) docker     (123)      828 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query01.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2556 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query02.sql
--rw-r--r--   0 runner    (1001) docker     (123)      479 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query03.sql
--rw-r--r--   0 runner    (1001) docker     (123)     6685 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query04.sql
--rw-r--r--   0 runner    (1001) docker     (123)     5211 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query05.sql
--rw-r--r--   0 runner    (1001) docker     (123)      688 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query06.sql
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query07.sql
--rw-r--r--   0 runner    (1001) docker     (123)     8175 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query08.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query09.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query10.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3407 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query11.sql
--rw-r--r--   0 runner    (1001) docker     (123)      737 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query12.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query13.sql
--rw-r--r--   0 runner    (1001) docker     (123)     9010 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query14.sql
--rw-r--r--   0 runner    (1001) docker     (123)      537 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query15.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query16.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1964 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query17.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query18.sql
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query19.sql
--rw-r--r--   0 runner    (1001) docker     (123)      741 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query20.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1097 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query21.sql
--rw-r--r--   0 runner    (1001) docker     (123)      428 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query22.sql
--rw-r--r--   0 runner    (1001) docker     (123)     4338 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query23.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3037 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query24.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1052 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query25.sql
--rw-r--r--   0 runner    (1001) docker     (123)      602 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query26.sql
--rw-r--r--   0 runner    (1001) docker     (123)      677 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query27.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2324 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query28.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query29.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query30.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1809 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query31.sql
--rw-r--r--   0 runner    (1001) docker     (123)      633 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query32.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2010 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query33.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1534 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query34.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1756 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query35.sql
--rw-r--r--   0 runner    (1001) docker     (123)      855 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query36.sql
--rw-r--r--   0 runner    (1001) docker     (123)      537 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query37.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query38.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3127 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query39.sql
--rw-r--r--   0 runner    (1001) docker     (123)      958 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query40.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query41.sql
--rw-r--r--   0 runner    (1001) docker     (123)      512 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query42.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query43.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1688 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query44.sql
--rw-r--r--   0 runner    (1001) docker     (123)      666 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query45.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1380 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query46.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query47.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query48.sql
--rw-r--r--   0 runner    (1001) docker     (123)     4775 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query49.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query50.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2161 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query51.sql
--rw-r--r--   0 runner    (1001) docker     (123)      503 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query52.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1450 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query53.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1784 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query54.sql
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query55.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1935 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query56.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query57.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2769 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query58.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query59.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1937 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query60.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query61.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query62.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query63.sql
--rw-r--r--   0 runner    (1001) docker     (123)     4418 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query64.sql
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query65.sql
--rw-r--r--   0 runner    (1001) docker     (123)    13194 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query66.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query67.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1427 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query68.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query69.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query70.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query71.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1330 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query72.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1295 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query73.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query74.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query75.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query76.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3844 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query77.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3067 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query78.sql
--rw-r--r--   0 runner    (1001) docker     (123)      924 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query79.sql
--rw-r--r--   0 runner    (1001) docker     (123)     3652 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query80.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1497 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query81.sql
--rw-r--r--   0 runner    (1001) docker     (123)      535 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query82.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2422 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query83.sql
--rw-r--r--   0 runner    (1001) docker     (123)      620 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query84.sql
--rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query85.sql
--rw-r--r--   0 runner    (1001) docker     (123)      671 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query86.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1006 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query87.sql
--rw-r--r--   0 runner    (1001) docker     (123)     5794 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query88.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query89.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1037 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query90.sql
--rw-r--r--   0 runner    (1001) docker     (123)      935 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query91.sql
--rw-r--r--   0 runner    (1001) docker     (123)      659 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query92.sql
--rw-r--r--   0 runner    (1001) docker     (123)      666 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query93.sql
--rw-r--r--   0 runner    (1001) docker     (123)      898 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query94.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1161 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query95.sql
--rw-r--r--   0 runner    (1001) docker     (123)      399 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query96.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1088 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query97.sql
--rw-r--r--   0 runner    (1001) docker     (123)      729 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query98.sql
--rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/data/tpcds/query99.sql
--rw-r--r--   0 runner    (1001) docker     (123)     7421 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/drawing.py
--rw-r--r--   0 runner    (1001) docker     (123)      328 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/io.py
--rw-r--r--   0 runner    (1001) docker     (123)     6066 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/runner.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.087654 sqllineage-1.4.2/sqllineage/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      373 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/utils/constant.py
--rw-r--r--   0 runner    (1001) docker     (123)      213 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/utils/entities.py
--rw-r--r--   0 runner    (1001) docker     (123)     1344 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineage/utils/helpers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineage.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     7286 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     7168 2023-04-22 15:23:10.000000 sqllineage-1.4.2/sqllineage.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      243 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-04-22 15:23:08.000000 sqllineage-1.4.2/sqllineage.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.087654 sqllineage-1.4.2/sqllineagejs/
--rw-r--r--   0 runner    (1001) docker     (123)      293 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/config-overrides.js
--rw-r--r--   0 runner    (1001) docker     (123)  1248521 2023-04-22 15:21:45.000000 sqllineage-1.4.2/sqllineagejs/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.087654 sqllineage-1.4.2/sqllineagejs/public/
--rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (123)     1813 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     5347 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/logo192.png
--rw-r--r--   0 runner    (1001) docker     (123)     9664 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/logo512.png
--rw-r--r--   0 runner    (1001) docker     (123)      494 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/public/robots.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.087654 sqllineage-1.4.2/sqllineagejs/src/
--rw-r--r--   0 runner    (1001) docker     (123)     9038 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/App.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/sqllineagejs/src/api/
--rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/api/client.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/sqllineagejs/src/app/
--rw-r--r--   0 runner    (1001) docker     (123)      293 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/app/store.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.055654 sqllineage-1.4.2/sqllineagejs/src/features/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/sqllineagejs/src/features/directory/
--rw-r--r--   0 runner    (1001) docker     (123)     1443 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/directory/Directory.js
--rw-r--r--   0 runner    (1001) docker     (123)     3300 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/directory/DirectoryTreeItem.js
--rw-r--r--   0 runner    (1001) docker     (123)     1197 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/directory/directorySlice.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/sqllineagejs/src/features/editor/
--rw-r--r--   0 runner    (1001) docker     (123)    12152 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/editor/DAG.js
--rw-r--r--   0 runner    (1001) docker     (123)      930 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/editor/DAGDesc.js
--rw-r--r--   0 runner    (1001) docker     (123)     2822 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/editor/Editor.js
--rw-r--r--   0 runner    (1001) docker     (123)     2245 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/editor/editorSlice.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 15:23:10.091654 sqllineage-1.4.2/sqllineagejs/src/features/widget/
--rw-r--r--   0 runner    (1001) docker     (123)      596 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/widget/LoadError.js
--rw-r--r--   0 runner    (1001) docker     (123)      525 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/features/widget/Loading.js
--rw-r--r--   0 runner    (1001) docker     (123)      641 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/index.css
--rw-r--r--   0 runner    (1001) docker     (123)      336 2023-04-22 15:21:12.000000 sqllineage-1.4.2/sqllineagejs/src/index.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.203902 sqllineage-1.4.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1057 2023-05-13 13:44:25.000000 sqllineage-1.4.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      137 2023-05-13 13:44:25.000000 sqllineage-1.4.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     7286 2023-05-13 13:46:21.199902 sqllineage-1.4.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6479 2023-05-13 13:44:25.000000 sqllineage-1.4.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:46:21.203902 sqllineage-1.4.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     3159 2023-05-13 13:44:25.000000 sqllineage-1.4.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineage/
+-rw-r--r--   0 runner    (1001) docker     (123)      959 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineage/build/
+-rw-r--r--   0 runner    (1001) docker     (123)      644 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/asset-manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)   146541 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/editor.worker.js
+-rw-r--r--   0 runner    (1001) docker     (123)      149 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/editor.worker.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)   622794 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/editor.worker.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-05-13 13:44:58.000000 sqllineage-1.4.3/sqllineage/build/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (123)      736 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     5347 2023-05-13 13:44:58.000000 sqllineage-1.4.3/sqllineage/build/logo192.png
+-rw-r--r--   0 runner    (1001) docker     (123)     9664 2023-05-13 13:44:58.000000 sqllineage-1.4.3/sqllineage/build/logo512.png
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-05-13 13:44:58.000000 sqllineage-1.4.3/sqllineage/build/manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 13:44:58.000000 sqllineage-1.4.3/sqllineage/build/robots.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.163902 sqllineage-1.4.3/sqllineage/build/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineage/build/static/css/
+-rw-r--r--   0 runner    (1001) docker     (123)    69444 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/css/main.c1b86fee.css
+-rw-r--r--   0 runner    (1001) docker     (123)   146886 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/css/main.c1b86fee.css.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.171902 sqllineage-1.4.3/sqllineage/build/static/js/
+-rw-r--r--   0 runner    (1001) docker     (123)    18303 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/js/333.97bcedbd.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)    45386 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/js/333.97bcedbd.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)  3567447 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123) 12937379 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/build/static/media/
+-rw-r--r--   0 runner    (1001) docker     (123)    62792 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage/build/static/media/codicon.4168b9c11e5075e9cfe6.ttf
+-rw-r--r--   0 runner    (1001) docker     (123)     3448 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/analyzer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11390 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/holders.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7062 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/
+-rw-r--r--   0 runner    (1001) docker     (123)     2386 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2818 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/analyzer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/
+-rw-r--r--   0 runner    (1001) docker     (123)      245 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3319 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/cte_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/ddl_alter_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1299 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/ddl_drop_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3876 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_insert_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_merge_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_select_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4946 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/lineage_holder_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/noop_extractor.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)      349 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6407 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/source.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1513 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/swap_partition.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4836 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/target.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/holder_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8434 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15960 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/
+-rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11020 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/analyzer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.187902 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)      349 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1570 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1493 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/cte.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4499 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/source.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/swap_partition.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2737 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/target.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/holder_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7344 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7518 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/core/parser/sqlparse/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineage/data/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.195902 sqllineage-1.4.3/sqllineage/data/tpcds/
+-rw-r--r--   0 runner    (1001) docker     (123)      828 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query01.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2556 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query02.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      479 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query03.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     6685 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query04.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     5211 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query05.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      688 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query06.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query07.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     8175 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query08.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query09.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query10.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3407 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query11.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      737 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query12.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query13.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     9010 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query14.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      537 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query15.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query16.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1964 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query17.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query18.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      750 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query19.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      741 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query20.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1097 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query21.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      428 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query22.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     4338 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query23.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3037 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query24.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1052 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query25.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      602 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query26.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      677 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query27.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2324 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query28.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query29.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query30.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1809 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query31.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      633 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query32.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2010 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query33.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1534 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query34.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1756 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query35.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      855 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query36.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      537 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query37.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query38.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3127 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query39.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      958 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query40.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query41.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      512 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query42.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query43.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1688 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query44.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      666 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query45.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1380 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query46.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query47.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query48.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     4775 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query49.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query50.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2161 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query51.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      503 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query52.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1450 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query53.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1784 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query54.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query55.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1935 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query56.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query57.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2769 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query58.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query59.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1937 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query60.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query61.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query62.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query63.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     4418 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query64.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query65.sql
+-rw-r--r--   0 runner    (1001) docker     (123)    13194 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query66.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query67.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1427 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query68.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query69.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query70.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query71.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1330 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query72.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1295 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query73.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query74.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query75.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query76.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3844 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query77.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3067 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query78.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      924 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query79.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     3652 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query80.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1497 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query81.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      535 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query82.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2422 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query83.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query84.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query85.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      671 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query86.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1006 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query87.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     5794 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query88.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query89.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1037 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query90.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query91.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query92.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      666 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query93.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      898 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query94.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1161 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query95.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query96.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1088 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query97.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      729 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query98.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/data/tpcds/query99.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     7421 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/drawing.py
+-rw-r--r--   0 runner    (1001) docker     (123)      328 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/io.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6066 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/runner.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineage/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      373 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/utils/constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)      213 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/utils/entities.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1344 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineage/utils/helpers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineage.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     7286 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7168 2023-05-13 13:46:21.000000 sqllineage-1.4.3/sqllineage.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      243 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 13:46:19.000000 sqllineage-1.4.3/sqllineage.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/
+-rw-r--r--   0 runner    (1001) docker     (123)      293 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/config-overrides.js
+-rw-r--r--   0 runner    (1001) docker     (123)  1248521 2023-05-13 13:44:56.000000 sqllineage-1.4.3/sqllineagejs/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/public/
+-rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (123)     1813 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     5347 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/logo192.png
+-rw-r--r--   0 runner    (1001) docker     (123)     9664 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/logo512.png
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/public/robots.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     9038 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/App.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/api/
+-rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/api/client.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/app/
+-rw-r--r--   0 runner    (1001) docker     (123)      293 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/app/store.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.167902 sqllineage-1.4.3/sqllineagejs/src/features/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/features/directory/
+-rw-r--r--   0 runner    (1001) docker     (123)     1443 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/directory/Directory.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3300 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/directory/DirectoryTreeItem.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1197 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/directory/directorySlice.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/features/editor/
+-rw-r--r--   0 runner    (1001) docker     (123)    12152 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/editor/DAG.js
+-rw-r--r--   0 runner    (1001) docker     (123)      930 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/editor/DAGDesc.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2822 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/editor/Editor.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2245 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/editor/editorSlice.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:46:21.199902 sqllineage-1.4.3/sqllineagejs/src/features/widget/
+-rw-r--r--   0 runner    (1001) docker     (123)      596 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/widget/LoadError.js
+-rw-r--r--   0 runner    (1001) docker     (123)      525 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/features/widget/Loading.js
+-rw-r--r--   0 runner    (1001) docker     (123)      641 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/index.css
+-rw-r--r--   0 runner    (1001) docker     (123)      336 2023-05-13 13:44:25.000000 sqllineage-1.4.3/sqllineagejs/src/index.js
```

### Comparing `sqllineage-1.4.2/LICENSE` & `sqllineage-1.4.3/LICENSE`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/PKG-INFO` & `sqllineage-1.4.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqllineage
-Version: 1.4.2
+Version: 1.4.3
 Summary: SQL Lineage Analysis Tool powered by Python
 Home-page: https://github.com/reata/sqllineage
 Author: Reata
 Author-email: reddevil.hjw@gmail.com
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `sqllineage-1.4.2/README.md` & `sqllineage-1.4.3/README.md`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/setup.py` & `sqllineage-1.4.3/setup.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/__init__.py` & `sqllineage-1.4.3/sqllineage/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import os
 
 
 NAME = "sqllineage"
-VERSION = "1.4.2"
+VERSION = "1.4.3"
 DEFAULT_LOGGING = {
     "version": 1,
     "disable_existing_loggers": False,
     "formatters": {"default": {"format": "%(levelname)s: %(message)s"}},
     "handlers": {
         "console": {
             "level": "WARNING",
```

### Comparing `sqllineage-1.4.2/sqllineage/build/asset-manifest.json` & `sqllineage-1.4.3/sqllineage/build/asset-manifest.json`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/editor.worker.js` & `sqllineage-1.4.3/sqllineage/build/editor.worker.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/editor.worker.js.map` & `sqllineage-1.4.3/sqllineage/build/editor.worker.js.map`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/favicon.ico` & `sqllineage-1.4.3/sqllineage/build/favicon.ico`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/index.html` & `sqllineage-1.4.3/sqllineage/build/index.html`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/logo192.png` & `sqllineage-1.4.3/sqllineage/build/logo192.png`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/logo512.png` & `sqllineage-1.4.3/sqllineage/build/logo512.png`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/css/main.c1b86fee.css` & `sqllineage-1.4.3/sqllineage/build/static/css/main.c1b86fee.css`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/css/main.c1b86fee.css.map` & `sqllineage-1.4.3/sqllineage/build/static/css/main.c1b86fee.css.map`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/js/333.97bcedbd.chunk.js` & `sqllineage-1.4.3/sqllineage/build/static/js/333.97bcedbd.chunk.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/js/333.97bcedbd.chunk.js.map` & `sqllineage-1.4.3/sqllineage/build/static/js/333.97bcedbd.chunk.js.map`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js` & `sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js.LICENSE.txt` & `sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/js/main.b4821123.js.map` & `sqllineage-1.4.3/sqllineage/build/static/js/main.b4821123.js.map`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/build/static/media/codicon.4168b9c11e5075e9cfe6.ttf` & `sqllineage-1.4.3/sqllineage/build/static/media/codicon.4168b9c11e5075e9cfe6.ttf`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/cli.py` & `sqllineage-1.4.3/sqllineage/cli.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/holders.py` & `sqllineage-1.4.3/sqllineage/core/holders.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/models.py` & `sqllineage-1.4.3/sqllineage/core/models.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/__init__.py` & `sqllineage-1.4.3/sqllineage/core/parser/__init__.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/analyzer.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/analyzer.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/cte_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/cte_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/ddl_alter_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/ddl_alter_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/ddl_drop_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/ddl_drop_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_insert_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_insert_extractor.py`

 * *Files 4% similar despite different names*

```diff
@@ -55,14 +55,22 @@
                 # Collecting subquery on the way, hold on parsing until last
                 # so that each handler don't have to worry about what's inside subquery
                 subqueries.append(sq)
 
             for current_handler in handlers:
                 current_handler.handle(segment, holder)
 
+            if segment.type == "with_compound_statement":
+                from .cte_extractor import DmlCteExtractor
+
+                holder |= DmlCteExtractor(self.dialect).extract(
+                    segment,
+                    AnalyzerContext(prev_cte=holder.cte, prev_write=holder.write),
+                )
+
             if segment.type == "select_statement":
                 holder |= DmlSelectExtractor(self.dialect).extract(
                     segment,
                     AnalyzerContext(
                         SqlFluffSubQuery.of(segment, None),
                         prev_cte=holder.cte,
                         prev_write=holder.write,
```

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_merge_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_merge_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/dml_select_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/dml_select_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/lineage_holder_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/lineage_holder_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/extractors/noop_extractor.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/extractors/noop_extractor.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/base.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/base.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/source.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/source.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/swap_partition.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/swap_partition.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/handlers/target.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/handlers/target.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/holder_utils.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/holder_utils.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/models.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/models.py`

 * *Files 8% similar despite different names*

```diff
@@ -20,14 +20,15 @@
     "partitionby_clause",
     "orderby_clause",
     "expression",
     "case_expression",
     "when_clause",
     "else_clause",
     "select_clause_element",
+    "cast_expression",
 ]
 
 SOURCE_COLUMN_SEGMENT_TYPE = NON_IDENTIFIER_OR_COLUMN_SEGMENT_TYPE + [
     "identifier",
     "column_reference",
 ]
 
@@ -109,15 +110,30 @@
                 )
             if source_columns:
                 sub_segments = retrieve_segments(column)
                 column_name = None
                 for sub_segment in sub_segments:
                     if sub_segment.type == "column_reference":
                         column_name = get_identifier(sub_segment)
-
+                    elif sub_segment.type == "expression":
+                        # special handling for postgres style type cast, col as target column name instead of col::type
+                        if len(sub2_segments := retrieve_segments(sub_segment)) == 1:
+                            if (
+                                sub2_segment := sub2_segments[0]
+                            ).type == "cast_expression":
+                                if (
+                                    len(
+                                        sub3_segments := retrieve_segments(sub2_segment)
+                                    )
+                                    == 2
+                                ):
+                                    if (
+                                        sub3_segment := sub3_segments[0]
+                                    ).type == "column_reference":
+                                        column_name = get_identifier(sub3_segment)
                 return Column(
                     column.raw if column_name is None else column_name,
                     source_columns=source_columns,
                 )
 
         # Wildcard, Case, Function without alias (thus not recognized as an Identifier)
         source_columns = SqlFluffColumn._extract_source_columns(column)
```

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlfluff/utils.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlfluff/utils.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/__init__.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/__init__.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/analyzer.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/analyzer.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/base.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/base.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/cte.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/cte.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/source.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/source.py`

 * *Files 3% similar despite different names*

```diff
@@ -43,14 +43,18 @@
         self.union_barriers = []
         super().__init__()
 
     def _indicate(self, token: Token) -> bool:
         if token.normalized in ("UNION", "UNION ALL"):
             self.union_barriers.append((len(self.columns), len(self.tables)))
 
+        if self.column_flag is True and bool(token.normalized == "DISTINCT"):
+            # special handling for SELECT DISTINCT
+            return True
+
         if any(re.match(regex, token.normalized) for regex in self.SOURCE_TABLE_TOKENS):
             self.column_flag = False
             return True
         elif bool(token.normalized == "SELECT"):
             self.column_flag = True
             return True
         else:
@@ -88,15 +92,15 @@
         else:
             raise SQLLineageException(
                 "An Identifier is expected, got %s[value: %s] instead."
                 % (type(token).__name__, token)
             )
 
     def _handle_column(self, token: Token) -> None:
-        column_token_types = (Identifier, Function, Operation, Case)
+        column_token_types = (Identifier, Function, Operation, Case, Parenthesis)
         if isinstance(token, column_token_types) or token.ttype is Wildcard:
             column_tokens = [token]
         elif isinstance(token, IdentifierList):
             column_tokens = [
                 sub_token
                 for sub_token in token.tokens
                 if isinstance(sub_token, column_token_types)
```

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/swap_partition.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/swap_partition.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/handlers/target.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/handlers/target.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/holder_utils.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/holder_utils.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/models.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/models.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/core/parser/sqlparse/utils.py` & `sqllineage-1.4.3/sqllineage/core/parser/sqlparse/utils.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query01.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query01.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query02.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query02.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query04.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query04.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query05.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query05.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query06.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query06.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query07.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query07.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query08.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query08.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query09.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query09.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query10.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query10.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query11.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query11.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query12.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query12.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query13.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query13.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query14.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query14.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query15.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query15.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query16.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query16.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query17.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query17.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query18.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query18.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query19.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query19.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query20.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query20.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query21.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query21.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query23.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query23.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query24.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query24.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query25.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query25.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query26.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query26.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query27.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query27.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query28.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query28.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query29.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query29.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query30.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query30.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query31.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query31.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query32.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query32.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query33.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query33.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query34.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query34.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query35.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query35.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query36.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query36.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query37.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query37.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query38.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query38.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query39.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query39.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query40.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query40.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query41.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query41.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query42.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query42.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query43.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query43.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query44.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query44.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query45.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query45.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query46.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query46.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query47.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query47.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query48.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query48.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query49.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query49.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query50.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query50.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query51.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query51.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query53.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query53.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query54.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query54.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query56.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query56.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query57.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query57.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query58.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query58.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query59.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query59.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query60.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query60.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query61.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query61.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query62.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query62.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query63.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query63.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query64.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query64.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query65.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query65.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query66.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query66.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query67.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query67.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query68.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query68.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query69.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query69.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query70.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query70.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query71.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query71.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query72.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query72.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query73.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query73.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query74.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query74.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query75.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query75.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query76.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query76.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query77.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query77.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query78.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query78.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query79.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query79.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query80.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query80.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query81.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query81.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query82.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query82.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query83.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query83.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query84.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query84.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query85.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query85.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query86.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query86.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query87.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query87.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query88.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query88.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query89.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query89.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query90.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query90.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query91.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query91.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query92.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query92.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query93.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query93.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query94.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query94.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query95.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query95.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query97.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query97.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query98.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query98.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/data/tpcds/query99.sql` & `sqllineage-1.4.3/sqllineage/data/tpcds/query99.sql`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/drawing.py` & `sqllineage-1.4.3/sqllineage/drawing.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/io.py` & `sqllineage-1.4.3/sqllineage/io.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/runner.py` & `sqllineage-1.4.3/sqllineage/runner.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage/utils/helpers.py` & `sqllineage-1.4.3/sqllineage/utils/helpers.py`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineage.egg-info/PKG-INFO` & `sqllineage-1.4.3/sqllineage.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqllineage
-Version: 1.4.2
+Version: 1.4.3
 Summary: SQL Lineage Analysis Tool powered by Python
 Home-page: https://github.com/reata/sqllineage
 Author: Reata
 Author-email: reddevil.hjw@gmail.com
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `sqllineage-1.4.2/sqllineage.egg-info/SOURCES.txt` & `sqllineage-1.4.3/sqllineage.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/package-lock.json` & `sqllineage-1.4.3/sqllineagejs/package-lock.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9166631874860833%*

 * *Differences: {"'packages'": "{'': {'version': '1.4.3'}}", "'version'": "'1.4.3'"}*

```diff
@@ -13625,15 +13625,15 @@
             },
             "devDependencies": {
                 "gh-pages": "^4.0.0",
                 "react-app-rewired": "^2.1.8",
                 "react-scripts": "^5.0.0"
             },
             "name": "sqllineagejs",
-            "version": "1.4.2"
+            "version": "1.4.3"
         },
         "node_modules/@babel/code-frame": {
             "dependencies": {
                 "@babel/highlight": "^7.18.6"
             },
             "dev": true,
             "engines": {
@@ -32068,9 +32068,9 @@
             },
             "integrity": "sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q==",
             "resolved": "https://registry.npmjs.org/yocto-queue/-/yocto-queue-0.1.0.tgz",
             "version": "0.1.0"
         }
     },
     "requires": true,
-    "version": "1.4.2"
+    "version": "1.4.3"
 }
```

### Comparing `sqllineage-1.4.2/sqllineagejs/package.json` & `sqllineage-1.4.3/sqllineagejs/package.json`

 * *Files 17% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9375%*

 * *Differences: {"'version'": "'1.4.3'"}*

```diff
@@ -42,9 +42,9 @@
     "private": true,
     "scripts": {
         "build": "react-app-rewired build",
         "deploy": "gh-pages -d build",
         "eject": "react-scripts eject",
         "start": "react-app-rewired start"
     },
-    "version": "1.4.2"
+    "version": "1.4.3"
 }
```

### Comparing `sqllineage-1.4.2/sqllineagejs/public/favicon.ico` & `sqllineage-1.4.3/sqllineagejs/public/favicon.ico`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/public/index.html` & `sqllineage-1.4.3/sqllineagejs/public/index.html`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/public/logo192.png` & `sqllineage-1.4.3/sqllineagejs/public/logo192.png`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/public/logo512.png` & `sqllineage-1.4.3/sqllineagejs/public/logo512.png`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/App.js` & `sqllineage-1.4.3/sqllineagejs/src/App.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/api/client.js` & `sqllineage-1.4.3/sqllineagejs/src/api/client.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/directory/Directory.js` & `sqllineage-1.4.3/sqllineagejs/src/features/directory/Directory.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/directory/DirectoryTreeItem.js` & `sqllineage-1.4.3/sqllineagejs/src/features/directory/DirectoryTreeItem.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/directory/directorySlice.js` & `sqllineage-1.4.3/sqllineagejs/src/features/directory/directorySlice.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/editor/DAG.js` & `sqllineage-1.4.3/sqllineagejs/src/features/editor/DAG.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/editor/DAGDesc.js` & `sqllineage-1.4.3/sqllineagejs/src/features/editor/DAGDesc.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/editor/Editor.js` & `sqllineage-1.4.3/sqllineagejs/src/features/editor/Editor.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/editor/editorSlice.js` & `sqllineage-1.4.3/sqllineagejs/src/features/editor/editorSlice.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/widget/LoadError.js` & `sqllineage-1.4.3/sqllineagejs/src/features/widget/LoadError.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/features/widget/Loading.js` & `sqllineage-1.4.3/sqllineagejs/src/features/widget/Loading.js`

 * *Files identical despite different names*

### Comparing `sqllineage-1.4.2/sqllineagejs/src/index.css` & `sqllineage-1.4.3/sqllineagejs/src/index.css`

 * *Files identical despite different names*

