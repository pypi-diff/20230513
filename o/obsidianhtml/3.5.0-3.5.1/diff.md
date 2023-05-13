# Comparing `tmp/obsidianhtml-3.5.0.tar.gz` & `tmp/obsidianhtml-3.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "obsidianhtml-3.5.0.tar", last modified: Sun Mar 12 19:11:59 2023, max compression
+gzip compressed data, was "obsidianhtml-3.5.1.tar", last modified: Sat May 13 15:56:47 2023, max compression
```

## Comparing `obsidianhtml-3.5.0.tar` & `obsidianhtml-3.5.1.tar`

### file list

```diff
@@ -1,231 +1,231 @@
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.884013 obsidianhtml-3.5.0/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    35149 2022-02-06 13:26:34.000000 obsidianhtml-3.5.0/LICENSE
--rw-r--r--   0 dorus     (1000) dorus     (1000)       76 2022-02-06 13:26:34.000000 obsidianhtml-3.5.0/MANIFEST.in
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1558 2023-03-12 19:11:59.884013 obsidianhtml-3.5.0/PKG-INFO
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.814013 obsidianhtml-3.5.0/obsidianhtml/
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-02-06 13:26:34.000000 obsidianhtml-3.5.0/obsidianhtml/README.md
--rw-r--r--   0 dorus     (1000) dorus     (1000)      737 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/SharedResources.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1831 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)       38 2023-02-12 21:27:12.000000 obsidianhtml-3.5.0/obsidianhtml/__main__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.817346 obsidianhtml-3.5.0/obsidianhtml/compiler/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     8935 2023-03-12 19:06:42.000000 obsidianhtml-3.5.0/obsidianhtml/compiler/HTML.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    17089 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/compiler/Templating.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:04.000000 obsidianhtml-3.5.0/obsidianhtml/compiler/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:04.000000 obsidianhtml-3.5.0/obsidianhtml/compiler/__main__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.820680 obsidianhtml-3.5.0/obsidianhtml/controller/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    23942 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/controller/ConvertVault.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3011 2023-02-16 19:15:55.000000 obsidianhtml-3.5.0/obsidianhtml/controller/Export.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    12403 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/controller/Run.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2262 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/controller/Serve.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:08.000000 obsidianhtml-3.5.0/obsidianhtml/controller/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:08.000000 obsidianhtml-3.5.0/obsidianhtml/controller/__main__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.824013 obsidianhtml-3.5.0/obsidianhtml/core/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2227 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/core/Actor.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    16314 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/core/ConfigManager.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     8086 2023-03-05 15:15:57.000000 obsidianhtml-3.5.0/obsidianhtml/core/CopyVault.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3331 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/core/ErrorHandling.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     7250 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/core/FileFinder.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    12067 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/core/FileObject.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     6973 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/core/Index.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     6357 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/core/NetworkTree.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5894 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/core/PicknickBasket.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1175 2023-02-12 21:35:22.000000 obsidianhtml-3.5.0/obsidianhtml/core/Types.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-17 19:18:31.000000 obsidianhtml-3.5.0/obsidianhtml/core/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-17 19:18:31.000000 obsidianhtml-3.5.0/obsidianhtml/core/__main__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2652 2022-12-19 20:59:29.000000 obsidianhtml-3.5.0/obsidianhtml/core/readme.md
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.827346 obsidianhtml-3.5.0/obsidianhtml/features/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    14593 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/CreateIndexFromDirStructure.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    10973 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/CreateIndexFromTags.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     8580 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/EmbeddedSearch.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    14966 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/RssFeed.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1655 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/Search.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     4305 2023-03-12 19:06:42.000000 obsidianhtml-3.5.0/obsidianhtml/features/SidePane.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2023-02-12 12:08:54.000000 obsidianhtml-3.5.0/obsidianhtml/features/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2023-02-12 12:15:24.000000 obsidianhtml-3.5.0/obsidianhtml/features/__main__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1813 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/add_toc_when_missing.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2436 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/features/post_processing.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.827346 obsidianhtml-3.5.0/obsidianhtml/gui/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3425 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/Api.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)      849 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/ConfigChecker.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3166 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/Ledger.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3465 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/Templater.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1929 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/WindowManager.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)      508 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)      649 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/__main__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)      823 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/gui/lib.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)      351 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/gui/readme.md
--rw-r--r--   0 dorus     (1000) dorus     (1000)     7877 2023-03-12 19:06:42.000000 obsidianhtml-3.5.0/obsidianhtml/lib.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.834013 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2628 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/AdmonitionExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1321 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/BlockLinkExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     7309 2023-03-12 19:06:42.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CallOutExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1839 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CodeWrapperExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2511 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CustomTableExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    13444 2023-02-12 21:35:24.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CustomTocExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     4487 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/DataviewExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1986 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/EmbeddedSearchExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     4332 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/EraserExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    20430 2023-02-12 21:35:24.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/FootnoteExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1974 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/FormattingExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3366 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/MermaidExtension.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-07-29 10:39:28.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-07-30 10:57:29.000000 obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/__main__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.834013 obsidianhtml-3.5.0/obsidianhtml/md2html/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    21293 2023-02-12 21:35:24.000000 obsidianhtml-3.5.0/obsidianhtml/md2html/__init__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.834013 obsidianhtml-3.5.0/obsidianhtml/note2md/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1132 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/note2md/__init__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.837346 obsidianhtml-3.5.0/obsidianhtml/parser/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     8326 2023-02-12 21:35:24.000000 obsidianhtml-3.5.0/obsidianhtml/parser/HeaderTree.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3011 2023-02-12 21:35:23.000000 obsidianhtml-3.5.0/obsidianhtml/parser/MarkdownLink.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)    23606 2023-03-12 18:18:00.000000 obsidianhtml-3.5.0/obsidianhtml/parser/MarkdownPage.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:23.000000 obsidianhtml-3.5.0/obsidianhtml/parser/__init__.py
--rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:23.000000 obsidianhtml-3.5.0/obsidianhtml/parser/__main__.py
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.837346 obsidianhtml-3.5.0/obsidianhtml/src/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    15084 2023-03-12 18:24:10.000000 obsidianhtml-3.5.0/obsidianhtml/src/defaults_config.yml
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.840680 obsidianhtml-3.5.0/obsidianhtml/src/graph/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      399 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5545 2022-12-17 13:48:34.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_2d.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1866 2022-09-11 10:30:46.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_3d.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1055 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_node_graph.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1560 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)    11307 2022-11-13 16:19:09.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1152 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.svg
--rw-r--r--   0 dorus     (1000) dorus     (1000)     4959 2023-01-14 12:12:51.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/graph_full_page.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      871 2022-07-30 17:25:48.000000 obsidianhtml-3.5.0/obsidianhtml/src/graph/graph_template.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.840680 obsidianhtml-3.5.0/obsidianhtml/src/help_texts/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      601 2022-09-07 13:16:28.000000 obsidianhtml-3.5.0/obsidianhtml/src/help_texts/export_help_text
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2138 2022-09-09 07:59:22.000000 obsidianhtml-3.5.0/obsidianhtml/src/help_texts/help_text
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.840680 obsidianhtml-3.5.0/obsidianhtml/src/html/
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.844013 obsidianhtml-3.5.0/obsidianhtml/src/html/css/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3845 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/callouts.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5777 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/codehilite.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)    18035 2023-03-12 18:40:51.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/global_main.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      818 2022-08-26 16:39:36.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/global_overwrites.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)    39538 2022-09-19 12:16:07.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/master.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5429 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/mermaid.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)       36 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/css/taglist.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)    12014 2022-02-17 17:27:05.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/favicon.ico
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.844013 obsidianhtml-3.5.0/obsidianhtml/src/html/fonts/
--rw-r--r--   0 dorus     (1000) dorus     (1000)   168260 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/fonts/Roboto-Regular.ttf
--rw-r--r--   0 dorus     (1000) dorus     (1000)   192740 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/fonts/SourceCodePro-Regular.ttf
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.847346 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1878 2022-07-24 12:59:51.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_documentation.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      583 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_minimal.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5491 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_tabs.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)     7716 2023-01-14 12:12:43.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_documentation.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      769 2023-01-14 12:12:55.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_minimal.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3845 2023-02-10 12:09:14.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_tabs.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.847346 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      121 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/audio_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1148 2022-12-23 20:32:49.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/full_header.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      126 2023-02-12 13:25:42.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/image_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      230 2022-12-21 21:33:08.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/left_pane.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      993 2022-12-23 20:32:05.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/minimal_header.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      199 2022-09-03 16:06:56.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/not_created.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      236 2022-12-21 21:41:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/right_pane.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      107 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/templates/video_template.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.850679 obsidianhtml-3.5.0/obsidianhtml/src/html/themes/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      897 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/themes/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      339 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/themes/popup.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     6268 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/html/themes/theme-obsidian.css
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.854013 obsidianhtml-3.5.0/obsidianhtml/src/imported/
--rw-r--r--   0 dorus     (1000) dorus     (1000)   729969 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/imported/3d-force-graph.v1.70.10.min.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)    16183 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/imported/flexsearch.v0.7.2.bundle.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)   797631 2022-11-13 16:20:13.000000 obsidianhtml-3.5.0/obsidianhtml/src/imported/mathjax.v3.es5.tex-chtml.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)  1133121 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/imported/mermaid.9.0.1.min.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)  4257261 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/imported/mermaid.9.0.1.min.js.map
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.864013 obsidianhtml-3.5.0/obsidianhtml/src/index_from_dir_structure/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      298 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/index_from_dir_structure/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-09-03 19:36:31.000000 obsidianhtml-3.5.0/obsidianhtml/src/index_from_dir_structure/dirtree.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)      221 2022-02-20 16:31:45.000000 obsidianhtml-3.5.0/obsidianhtml/src/index_from_dir_structure/dirtree.svg
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.810680 obsidianhtml-3.5.0/obsidianhtml/src/installer/
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.867346 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/
--rw-r--r--   0 dorus     (1000) dorus     (1000)    14562 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/configurations.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    13783 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/gp_installer.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    11339 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/index.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    12338 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/init.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      110 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/readme.md
--rw-r--r--   0 dorus     (1000) dorus     (1000)    24152 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/setup_gitpages.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    13991 2022-04-30 21:45:32.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/test.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.810680 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.867346 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/components/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1977 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/components/select-entrypoint-path.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      889 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/components/select-vault-path.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.867346 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     6098 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/configurations_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     5319 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/gp_installer_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2875 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/index_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3874 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/init_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    15688 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/setup_gitpages_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      893 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/test_template.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.867346 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/js/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     4169 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/js/core.js
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.870679 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      828 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/action_components.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      448 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/error.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      625 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/flex.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      968 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/main.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)      655 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/response.css
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.870679 obsidianhtml-3.5.0/obsidianhtml/src/js/
--rw-r--r--   0 dorus     (1000) dorus     (1000)   108114 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/js/encoding.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2740 2022-12-21 21:59:01.000000 obsidianhtml-3.5.0/obsidianhtml/src/js/load_dirtree_footer.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)    18145 2023-02-12 21:57:56.000000 obsidianhtml-3.5.0/obsidianhtml/src/js/obsidian_core.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)    10057 2023-02-10 12:23:33.000000 obsidianhtml-3.5.0/obsidianhtml/src/js/obsidian_tabs_footer.js
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.870679 obsidianhtml-3.5.0/obsidianhtml/src/latex/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      297 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/latex/load_mathjax.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)      482 2022-09-04 19:38:03.000000 obsidianhtml-3.5.0/obsidianhtml/src/latex/load_mathjax_header_template.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.874013 obsidianhtml-3.5.0/obsidianhtml/src/rss/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      261 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/rss/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      530 2023-02-09 20:49:44.000000 obsidianhtml-3.5.0/obsidianhtml/src/rss/channel_template.xml
--rw-r--r--   0 dorus     (1000) dorus     (1000)      252 2022-02-17 17:26:47.000000 obsidianhtml-3.5.0/obsidianhtml/src/rss/item_template.xml
--rw-r--r--   0 dorus     (1000) dorus     (1000)      767 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/rss/rss.svg
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.874013 obsidianhtml-3.5.0/obsidianhtml/src/search/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1135 2023-01-28 17:50:13.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)   242525 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/pako.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)     3500 2023-03-02 13:48:12.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/search.css
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1782 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/search.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)    13950 2023-01-29 17:52:44.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/search.js
--rw-r--r--   0 dorus     (1000) dorus     (1000)      947 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/search/search.svg
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.884013 obsidianhtml-3.5.0/obsidianhtml/src/svgs/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/abstract.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/attention.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      479 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/bug.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/caution.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/check.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      535 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/cite.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/danger.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/done.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/error.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      474 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/example.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      534 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/external.svg
--rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/fail.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/failure.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/faq.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      247 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/fold.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      545 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/hashtag.svg
--rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/help.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      390 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/important.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      339 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/info.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/missing.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      303 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/note.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/question.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      535 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/quote.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/success.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/summary.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      390 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/tip.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/tldr.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      329 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/todo.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.0/obsidianhtml/src/svgs/warning.html
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.884013 obsidianhtml-3.5.0/obsidianhtml/src/tags_page/
--rw-r--r--   0 dorus     (1000) dorus     (1000)      252 2022-06-18 16:13:52.000000 obsidianhtml-3.5.0/obsidianhtml/src/tags_page/button_template.html
--rw-r--r--   0 dorus     (1000) dorus     (1000)        6 2023-03-12 19:11:56.000000 obsidianhtml-3.5.0/obsidianhtml/src/version
-drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-03-12 19:11:59.817346 obsidianhtml-3.5.0/obsidianhtml.egg-info/
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1558 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/PKG-INFO
--rw-r--r--   0 dorus     (1000) dorus     (1000)     7777 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/SOURCES.txt
--rw-r--r--   0 dorus     (1000) dorus     (1000)        1 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/dependency_links.txt
--rw-r--r--   0 dorus     (1000) dorus     (1000)     1061 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/entry_points.txt
--rw-r--r--   0 dorus     (1000) dorus     (1000)      132 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/requires.txt
--rw-r--r--   0 dorus     (1000) dorus     (1000)       13 2023-03-12 19:11:59.000000 obsidianhtml-3.5.0/obsidianhtml.egg-info/top_level.txt
--rw-r--r--   0 dorus     (1000) dorus     (1000)      807 2022-03-11 21:09:45.000000 obsidianhtml-3.5.0/pypi_readme.md
--rw-r--r--   0 dorus     (1000) dorus     (1000)      438 2023-02-12 21:35:19.000000 obsidianhtml-3.5.0/pyproject.toml
--rw-r--r--   0 dorus     (1000) dorus     (1000)     2149 2023-03-12 19:11:59.884013 obsidianhtml-3.5.0/setup.cfg
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.928703 obsidianhtml-3.5.1/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    35149 2022-02-06 13:26:34.000000 obsidianhtml-3.5.1/LICENSE
+-rw-r--r--   0 dorus     (1000) dorus     (1000)       76 2022-02-06 13:26:34.000000 obsidianhtml-3.5.1/MANIFEST.in
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1558 2023-05-13 15:56:47.928703 obsidianhtml-3.5.1/PKG-INFO
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.872036 obsidianhtml-3.5.1/obsidianhtml/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-02-06 13:26:34.000000 obsidianhtml-3.5.1/obsidianhtml/README.md
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      737 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/SharedResources.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1831 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)       38 2023-02-12 21:27:12.000000 obsidianhtml-3.5.1/obsidianhtml/__main__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.875370 obsidianhtml-3.5.1/obsidianhtml/compiler/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     8991 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/compiler/HTML.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    17089 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/compiler/Templating.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:04.000000 obsidianhtml-3.5.1/obsidianhtml/compiler/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:04.000000 obsidianhtml-3.5.1/obsidianhtml/compiler/__main__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.878703 obsidianhtml-3.5.1/obsidianhtml/controller/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    23942 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/controller/ConvertVault.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3011 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/controller/Export.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    12403 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/controller/Run.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2262 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/controller/Serve.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:08.000000 obsidianhtml-3.5.1/obsidianhtml/controller/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:08.000000 obsidianhtml-3.5.1/obsidianhtml/controller/__main__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.882036 obsidianhtml-3.5.1/obsidianhtml/core/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2227 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/Actor.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    16551 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/ConfigManager.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     8086 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/CopyVault.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3331 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/ErrorHandling.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     7250 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/core/FileFinder.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    12067 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/FileObject.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     6973 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/Index.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     6357 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/core/NetworkTree.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5894 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/core/PicknickBasket.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1175 2023-02-12 21:35:22.000000 obsidianhtml-3.5.1/obsidianhtml/core/Types.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-17 19:18:31.000000 obsidianhtml-3.5.1/obsidianhtml/core/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-17 19:18:31.000000 obsidianhtml-3.5.1/obsidianhtml/core/__main__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2652 2022-12-19 20:59:29.000000 obsidianhtml-3.5.1/obsidianhtml/core/readme.md
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.885370 obsidianhtml-3.5.1/obsidianhtml/features/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    14593 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/features/CreateIndexFromDirStructure.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    10973 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/features/CreateIndexFromTags.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     8580 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/features/EmbeddedSearch.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    14966 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/features/RssFeed.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1655 2023-04-09 20:17:12.000000 obsidianhtml-3.5.1/obsidianhtml/features/Search.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     4305 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/features/SidePane.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2023-02-12 12:08:54.000000 obsidianhtml-3.5.1/obsidianhtml/features/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2023-02-12 12:15:24.000000 obsidianhtml-3.5.1/obsidianhtml/features/__main__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1813 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/features/add_toc_when_missing.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2436 2023-02-12 21:35:23.000000 obsidianhtml-3.5.1/obsidianhtml/features/post_processing.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.885370 obsidianhtml-3.5.1/obsidianhtml/gui/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3425 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/Api.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      849 2023-04-09 20:17:12.000000 obsidianhtml-3.5.1/obsidianhtml/gui/ConfigChecker.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3166 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/Ledger.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3465 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/Templater.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1929 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/WindowManager.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      508 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      649 2023-02-12 21:35:23.000000 obsidianhtml-3.5.1/obsidianhtml/gui/__main__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      823 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/gui/lib.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      351 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/gui/readme.md
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     7877 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/lib.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.888703 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2628 2023-04-09 20:16:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/AdmonitionExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1321 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/BlockLinkExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     7309 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CallOutExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1839 2023-04-09 20:16:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CodeWrapperExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2511 2023-04-09 20:17:12.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CustomTableExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    13444 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CustomTocExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     4487 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/DataviewExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1986 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/EmbeddedSearchExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     4332 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/EraserExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    20430 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/FootnoteExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1974 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/FormattingExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3366 2023-04-09 20:16:25.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/MermaidExtension.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-07-29 10:39:28.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-07-30 10:57:29.000000 obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/__main__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.888703 obsidianhtml-3.5.1/obsidianhtml/md2html/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    20143 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/md2html/__init__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.888703 obsidianhtml-3.5.1/obsidianhtml/note2md/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1132 2023-04-09 20:21:25.000000 obsidianhtml-3.5.1/obsidianhtml/note2md/__init__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.892036 obsidianhtml-3.5.1/obsidianhtml/parser/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     8326 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/parser/HeaderTree.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3011 2023-02-12 21:35:23.000000 obsidianhtml-3.5.1/obsidianhtml/parser/MarkdownLink.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    23606 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/parser/MarkdownPage.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:23.000000 obsidianhtml-3.5.1/obsidianhtml/parser/__init__.py
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        0 2022-12-21 19:04:23.000000 obsidianhtml-3.5.1/obsidianhtml/parser/__main__.py
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.892036 obsidianhtml-3.5.1/obsidianhtml/src/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    15084 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/src/defaults_config.yml
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.895370 obsidianhtml-3.5.1/obsidianhtml/src/graph/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      399 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5545 2022-12-17 13:48:34.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_2d.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1866 2022-09-11 10:30:46.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_3d.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1055 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_node_graph.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1560 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    11307 2022-11-13 16:19:09.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1152 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.svg
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     4959 2023-01-14 12:12:51.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/graph_full_page.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      871 2022-07-30 17:25:48.000000 obsidianhtml-3.5.1/obsidianhtml/src/graph/graph_template.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.895370 obsidianhtml-3.5.1/obsidianhtml/src/help_texts/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      601 2022-09-07 13:16:28.000000 obsidianhtml-3.5.1/obsidianhtml/src/help_texts/export_help_text
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2138 2023-05-13 15:50:50.000000 obsidianhtml-3.5.1/obsidianhtml/src/help_texts/help_text
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.895370 obsidianhtml-3.5.1/obsidianhtml/src/html/
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.898703 obsidianhtml-3.5.1/obsidianhtml/src/html/css/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3845 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/callouts.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5777 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/codehilite.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    17987 2023-05-13 15:51:13.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/global_main.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      818 2022-08-26 16:39:36.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/global_overwrites.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    39538 2022-09-19 12:16:07.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/master.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5429 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/mermaid.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)       36 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/css/taglist.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    12014 2022-02-17 17:27:05.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/favicon.ico
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.898703 obsidianhtml-3.5.1/obsidianhtml/src/html/fonts/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   168260 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/fonts/Roboto-Regular.ttf
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   192740 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/fonts/SourceCodePro-Regular.ttf
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.898703 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1878 2022-07-24 12:59:51.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_documentation.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      583 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_minimal.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5491 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_tabs.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     7716 2023-01-14 12:12:43.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_documentation.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      769 2023-01-14 12:12:55.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_minimal.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3845 2023-02-10 12:09:14.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_tabs.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.902036 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      121 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/audio_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1148 2022-12-23 20:32:49.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/full_header.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      126 2023-02-12 13:25:42.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/image_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      230 2022-12-21 21:33:08.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/left_pane.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      993 2022-12-23 20:32:05.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/minimal_header.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      199 2022-09-03 16:06:56.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/not_created.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      236 2022-12-21 21:41:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/right_pane.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      107 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/templates/video_template.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.902036 obsidianhtml-3.5.1/obsidianhtml/src/html/themes/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      897 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/themes/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      339 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/themes/popup.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     6268 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/html/themes/theme-obsidian.css
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.905370 obsidianhtml-3.5.1/obsidianhtml/src/imported/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   729969 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/imported/3d-force-graph.v1.70.10.min.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    16183 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/imported/flexsearch.v0.7.2.bundle.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   797631 2022-11-13 16:20:13.000000 obsidianhtml-3.5.1/obsidianhtml/src/imported/mathjax.v3.es5.tex-chtml.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)  1133121 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/imported/mermaid.9.0.1.min.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)  4257261 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/imported/mermaid.9.0.1.min.js.map
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.915370 obsidianhtml-3.5.1/obsidianhtml/src/index_from_dir_structure/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      298 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/index_from_dir_structure/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-09-03 19:36:31.000000 obsidianhtml-3.5.1/obsidianhtml/src/index_from_dir_structure/dirtree.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      221 2022-02-20 16:31:45.000000 obsidianhtml-3.5.1/obsidianhtml/src/index_from_dir_structure/dirtree.svg
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.868703 obsidianhtml-3.5.1/obsidianhtml/src/installer/
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.915370 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    14562 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/configurations.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    13783 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/gp_installer.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    11339 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/index.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    12338 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/init.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      110 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/readme.md
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    24152 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/setup_gitpages.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    13991 2022-04-30 21:45:32.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/test.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.868703 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.915370 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/components/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1977 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/components/select-entrypoint-path.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      889 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/components/select-vault-path.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.918703 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     6098 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/configurations_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     5319 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/gp_installer_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2875 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/index_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3874 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/init_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    15688 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/setup_gitpages_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      893 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/test_template.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.918703 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/js/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     4169 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/js/core.js
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.918703 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      828 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/action_components.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      448 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/error.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      625 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/flex.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      968 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/main.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      655 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/response.css
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.918703 obsidianhtml-3.5.1/obsidianhtml/src/js/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   108114 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/js/encoding.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2740 2022-12-21 21:59:01.000000 obsidianhtml-3.5.1/obsidianhtml/src/js/load_dirtree_footer.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    18145 2023-02-12 21:57:56.000000 obsidianhtml-3.5.1/obsidianhtml/src/js/obsidian_core.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    10057 2023-02-10 12:23:33.000000 obsidianhtml-3.5.1/obsidianhtml/src/js/obsidian_tabs_footer.js
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.918703 obsidianhtml-3.5.1/obsidianhtml/src/latex/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      297 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/latex/load_mathjax.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      482 2022-09-04 19:38:03.000000 obsidianhtml-3.5.1/obsidianhtml/src/latex/load_mathjax_header_template.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.922036 obsidianhtml-3.5.1/obsidianhtml/src/rss/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      261 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/rss/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      530 2023-02-09 20:49:44.000000 obsidianhtml-3.5.1/obsidianhtml/src/rss/channel_template.xml
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      252 2022-02-17 17:26:47.000000 obsidianhtml-3.5.1/obsidianhtml/src/rss/item_template.xml
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      767 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/rss/rss.svg
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.922036 obsidianhtml-3.5.1/obsidianhtml/src/search/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1135 2023-01-28 17:50:13.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)   242525 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/pako.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     3500 2023-03-02 13:48:12.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/search.css
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1782 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/search.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)    13950 2023-01-29 17:52:44.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/search.js
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      947 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/search/search.svg
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.928703 obsidianhtml-3.5.1/obsidianhtml/src/svgs/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/abstract.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/attention.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      479 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/bug.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/caution.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/check.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      535 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/cite.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/danger.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/done.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      275 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/error.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      474 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/example.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      534 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/external.svg
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/fail.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/failure.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/faq.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      247 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/fold.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      545 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/hashtag.svg
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/help.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      390 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/important.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      339 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/info.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      294 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/missing.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      303 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/note.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      348 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/question.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      535 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/quote.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      253 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/success.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/summary.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      390 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/tip.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      480 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/tldr.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      329 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/todo.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      401 2022-04-27 21:48:26.000000 obsidianhtml-3.5.1/obsidianhtml/src/svgs/warning.html
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.928703 obsidianhtml-3.5.1/obsidianhtml/src/tags_page/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      252 2022-06-18 16:13:52.000000 obsidianhtml-3.5.1/obsidianhtml/src/tags_page/button_template.html
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        6 2023-05-13 15:56:41.000000 obsidianhtml-3.5.1/obsidianhtml/src/version
+drwxr-xr-x   0 dorus     (1000) dorus     (1000)        0 2023-05-13 15:56:47.875370 obsidianhtml-3.5.1/obsidianhtml.egg-info/
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1558 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/PKG-INFO
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     7777 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/SOURCES.txt
+-rw-r--r--   0 dorus     (1000) dorus     (1000)        1 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/dependency_links.txt
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     1061 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/entry_points.txt
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      132 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/requires.txt
+-rw-r--r--   0 dorus     (1000) dorus     (1000)       13 2023-05-13 15:56:47.000000 obsidianhtml-3.5.1/obsidianhtml.egg-info/top_level.txt
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      807 2022-03-11 21:09:45.000000 obsidianhtml-3.5.1/pypi_readme.md
+-rw-r--r--   0 dorus     (1000) dorus     (1000)      438 2023-02-12 21:35:19.000000 obsidianhtml-3.5.1/pyproject.toml
+-rw-r--r--   0 dorus     (1000) dorus     (1000)     2149 2023-05-13 15:56:47.932036 obsidianhtml-3.5.1/setup.cfg
```

### Comparing `obsidianhtml-3.5.0/LICENSE` & `obsidianhtml-3.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/PKG-INFO` & `obsidianhtml-3.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: obsidianhtml
-Version: 3.5.0
+Version: 3.5.1
 Summary: Converts Obsidian notes into proper markdown and HTML
 Home-page: https://github.com/obsidian-html/obsidian-html
 Author: https://github.com/dwrolvink
 Author-email: dwrolvink@protonmail.com
 License: GNU General Public License v3 or later (GPLv3+)
 Keywords: html,markdown,notes,markdown-to-html,note-taking,obsidian,html-css-javascript,notes-app,obsidian-md,obsidian-html,obsidianmd,obsidian-notes
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml/SharedResources.py` & `obsidianhtml-3.5.1/obsidianhtml/SharedResources.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/__init__.py` & `obsidianhtml-3.5.1/obsidianhtml/__init__.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/compiler/HTML.py` & `obsidianhtml-3.5.1/obsidianhtml/compiler/HTML.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,27 +14,29 @@
 
     html_url_prefix = pb.gc("html_url_prefix")
     navbar_links = pb.gc("navbar_links", cached=True)
     elements = []
 
     for l in navbar_links:
         link = l["link"]
-        if pb.gc("toggles/slugify_html_links"):
-            link = slugify_path(link)
-
-        # default
-        el = f'<a class="navbar-link" href="{html_url_prefix}/{link}" title="{l["name"]}">{l["name"]}</a>'
+        el = None
 
         # external links
         if "type" in l.keys():
             if l["type"] == "external":
                 el = f'<a class="navbar-link" href="{link}" title="{l["name"]}">{l["name"]}</a>'
             else:
                 raise Exception(f"navbar_link type of {l['type']} is unknown. Known types: external (for internal links just remove the type keyvalue pair)")
 
+        # internal links
+        if not el:
+            if pb.gc("toggles/slugify_html_links"):
+                link = slugify_path(link)
+            el = f'<a class="navbar-link" href="{html_url_prefix}/{link}" title="{l["name"]}">{l["name"]}</a>'
+
         elements.append(el)
 
     pb.navbar_links = elements
     return elements
 
 
 def create_folder_navigation_view(pb) -> T.WriteExportFile:
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml/compiler/Templating.py` & `obsidianhtml-3.5.1/obsidianhtml/compiler/Templating.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/controller/ConvertVault.py` & `obsidianhtml-3.5.1/obsidianhtml/controller/ConvertVault.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/controller/Export.py` & `obsidianhtml-3.5.1/obsidianhtml/controller/Export.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/controller/Run.py` & `obsidianhtml-3.5.1/obsidianhtml/controller/Run.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/controller/Serve.py` & `obsidianhtml-3.5.1/obsidianhtml/controller/Serve.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/Actor.py` & `obsidianhtml-3.5.1/obsidianhtml/core/Actor.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/ConfigManager.py` & `obsidianhtml-3.5.1/obsidianhtml/core/ConfigManager.py`

 * *Files 1% similar despite different names*

```diff
@@ -293,27 +293,33 @@
             )
             return False
         return True
 
     for k, v in update_dict.items():
         key_path = "/".join(x for x in (path, k) if x != "")
 
+        # these dicts are freeform, and thus should not be checked
+        excluded_key_paths = ["module_config"]
+
         # every configured key should be known in base config, otherwise this might suggest a typo/other error
         if k not in base_dict.keys():
             raise Exception(f'\n\tThe configured key "{key_path}" is unknown. Check for typos/indentation. {helptext}')
 
         # don't overwrite a dict in the base config with a string, or something else
         # in general, we don't expect types to change
         if type(base_dict[k]) != type(v):
             if check_leaf(key_path, base_dict[k]):
                 raise Exception(f'\n\tThe value of key "{key_path}" is expected to be of type {type(base_dict[k])}, but is of type {type(v)}. {helptext}')
 
         # dict match -> recurse
         if isinstance(base_dict[k], dict) and isinstance(v, dict):
-            base_dict[k] = MergeDictRecurse(base_dict[k], update_dict[k], path=key_path)
+            if key_path in excluded_key_paths:
+                base_dict[k] = update_dict[k].copy()
+            else:
+                base_dict[k] = MergeDictRecurse(base_dict[k], update_dict[k], path=key_path)
             continue
 
         # other cases -> copy over
         if isinstance(update_dict[k], list):
             base_dict[k] = v.copy()
         else:
             check_leaf(key_path, base_dict[k])
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/CopyVault.py` & `obsidianhtml-3.5.1/obsidianhtml/core/CopyVault.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/ErrorHandling.py` & `obsidianhtml-3.5.1/obsidianhtml/core/ErrorHandling.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/FileFinder.py` & `obsidianhtml-3.5.1/obsidianhtml/core/FileFinder.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/FileObject.py` & `obsidianhtml-3.5.1/obsidianhtml/core/FileObject.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/Index.py` & `obsidianhtml-3.5.1/obsidianhtml/core/Index.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/NetworkTree.py` & `obsidianhtml-3.5.1/obsidianhtml/core/NetworkTree.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/PicknickBasket.py` & `obsidianhtml-3.5.1/obsidianhtml/core/PicknickBasket.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/Types.py` & `obsidianhtml-3.5.1/obsidianhtml/core/Types.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/core/readme.md` & `obsidianhtml-3.5.1/obsidianhtml/core/readme.md`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/CreateIndexFromDirStructure.py` & `obsidianhtml-3.5.1/obsidianhtml/features/CreateIndexFromDirStructure.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/CreateIndexFromTags.py` & `obsidianhtml-3.5.1/obsidianhtml/features/CreateIndexFromTags.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/EmbeddedSearch.py` & `obsidianhtml-3.5.1/obsidianhtml/features/EmbeddedSearch.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/RssFeed.py` & `obsidianhtml-3.5.1/obsidianhtml/features/RssFeed.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/Search.py` & `obsidianhtml-3.5.1/obsidianhtml/features/Search.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/SidePane.py` & `obsidianhtml-3.5.1/obsidianhtml/features/SidePane.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/add_toc_when_missing.py` & `obsidianhtml-3.5.1/obsidianhtml/features/add_toc_when_missing.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/features/post_processing.py` & `obsidianhtml-3.5.1/obsidianhtml/features/post_processing.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/Api.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/Api.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/ConfigChecker.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/ConfigChecker.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/Ledger.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/Ledger.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/Templater.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/Templater.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/WindowManager.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/WindowManager.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/__main__.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/__main__.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/gui/lib.py` & `obsidianhtml-3.5.1/obsidianhtml/gui/lib.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/lib.py` & `obsidianhtml-3.5.1/obsidianhtml/lib.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/AdmonitionExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/AdmonitionExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/BlockLinkExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/BlockLinkExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CallOutExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CallOutExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CodeWrapperExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CodeWrapperExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CustomTableExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CustomTableExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/CustomTocExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/CustomTocExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/DataviewExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/DataviewExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/EmbeddedSearchExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/EmbeddedSearchExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/EraserExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/EraserExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/FootnoteExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/FootnoteExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/FormattingExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/FormattingExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/markdown_extensions/MermaidExtension.py` & `obsidianhtml-3.5.1/obsidianhtml/markdown_extensions/MermaidExtension.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/md2html/__init__.py` & `obsidianhtml-3.5.1/obsidianhtml/md2html/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -125,39 +125,14 @@
                 query_part = link.query_delimiter + link.query
             new_link = f']({urllib.parse.quote(link.fo.get_link("html", origin=fo))}{query_part})'
 
         # Update link
         safe_link = re.escape("](" + ol + ")")
         md.page = re.sub(safe_link, new_link, md.page)
 
-    # [4] Handle local image links (copy them over to output)
-    # ------------------------------------------------------------------
-    for link in re.findall(r"\!\[.*?\]\((.*?)\)", md.page):
-        if link.strip() == "":
-            continue
-
-        l = urllib.parse.unquote(link)
-        if l[0] == "/":
-            l = l.replace("/", "", 1)
-
-        # Only handle local image files (images located in the root folder)
-        # Doublecheck, who knows what some weird '../../folder/..' does...
-        rel_path_str, link_fo = pb.FileFinder.FindFile(l, pb)
-        if rel_path_str is False:
-            if pb.gc("toggles/warn_on_skipped_image", cached=True):
-                warnings.warn(f"Image {l} treated as external and not imported in html")
-            continue
-
-        # Copy src to dst
-        link_fo.copy_file("mth")
-
-        # [11.2] Adjust image link in page to new dst folder (when the link is to a file in our root folder)
-        new_link = "![](" + urllib.parse.quote(link_fo.get_link("html", origin=fo)) + ")"
-        safe_link = r"\!\[.*\]\(" + re.escape(link) + r"\)"
-        md.page = re.sub(safe_link, new_link, md.page)
 
     # [?] Handle local source tag-links (copy them over to output)
     # ------------------------------------------------------------------
     for link in re.findall(r'(?<=<source src=")([^"]*)', md.page):
         l = urllib.parse.unquote(link)
         if "://" in l:
             continue
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml/note2md/__init__.py` & `obsidianhtml-3.5.1/obsidianhtml/note2md/__init__.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/parser/HeaderTree.py` & `obsidianhtml-3.5.1/obsidianhtml/parser/HeaderTree.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/parser/MarkdownLink.py` & `obsidianhtml-3.5.1/obsidianhtml/parser/MarkdownLink.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/parser/MarkdownPage.py` & `obsidianhtml-3.5.1/obsidianhtml/parser/MarkdownPage.py`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/defaults_config.yml` & `obsidianhtml-3.5.1/obsidianhtml/src/defaults_config.yml`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_2d.js` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_2d.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_3d.js` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_3d.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/default_grapher_node_graph.html` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/default_grapher_node_graph.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.css` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.js` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/graph.svg` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/graph.svg`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/graph_full_page.html` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/graph_full_page.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/graph/graph_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/graph/graph_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/help_texts/export_help_text` & `obsidianhtml-3.5.1/obsidianhtml/src/help_texts/export_help_text`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/help_texts/help_text` & `obsidianhtml-3.5.1/obsidianhtml/src/help_texts/help_text`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/callouts.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/callouts.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/codehilite.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/codehilite.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/global_main.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/global_main.css`

 * *Files 0% similar despite different names*

```diff
@@ -321,18 +321,14 @@
 }
 
 td:nth-child(2n) {
     border-left: 1px dotted rgb(var(--table-border-color-rgb), 0.3);
     border-right: 1px dotted rgb(var(--table-border-color-rgb), 0.3);
 }
 
-td:first-child {
-    min-width: max-content;
-}
-
 th:first-child,
 td:first-child {
     padding-left: 0rem;
 }
 
 tr:last-child td {
     border-bottom: 0px;
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/global_overwrites.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/global_overwrites.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/master.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/master.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/css/mermaid.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/css/mermaid.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/favicon.ico` & `obsidianhtml-3.5.1/obsidianhtml/src/html/favicon.ico`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/fonts/Roboto-Regular.ttf` & `obsidianhtml-3.5.1/obsidianhtml/src/html/fonts/Roboto-Regular.ttf`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/fonts/SourceCodePro-Regular.ttf` & `obsidianhtml-3.5.1/obsidianhtml/src/html/fonts/SourceCodePro-Regular.ttf`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_documentation.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_documentation.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_minimal.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_minimal.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/main_tabs.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/main_tabs.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_documentation.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_documentation.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_minimal.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_minimal.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/layouts/template_tabs.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/layouts/template_tabs.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/templates/full_header.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/templates/full_header.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/templates/minimal_header.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/templates/minimal_header.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/themes/button_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/html/themes/button_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/html/themes/theme-obsidian.css` & `obsidianhtml-3.5.1/obsidianhtml/src/html/themes/theme-obsidian.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/imported/3d-force-graph.v1.70.10.min.js` & `obsidianhtml-3.5.1/obsidianhtml/src/imported/3d-force-graph.v1.70.10.min.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/imported/flexsearch.v0.7.2.bundle.js` & `obsidianhtml-3.5.1/obsidianhtml/src/imported/flexsearch.v0.7.2.bundle.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/imported/mathjax.v3.es5.tex-chtml.js` & `obsidianhtml-3.5.1/obsidianhtml/src/imported/mathjax.v3.es5.tex-chtml.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/imported/mermaid.9.0.1.min.js` & `obsidianhtml-3.5.1/obsidianhtml/src/imported/mermaid.9.0.1.min.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/imported/mermaid.9.0.1.min.js.map` & `obsidianhtml-3.5.1/obsidianhtml/src/imported/mermaid.9.0.1.min.js.map`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/configurations.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/configurations.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/gp_installer.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/gp_installer.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/index.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/index.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/init.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/init.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/setup_gitpages.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/setup_gitpages.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/dist/test.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/dist/test.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/components/select-entrypoint-path.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/components/select-entrypoint-path.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/components/select-vault-path.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/components/select-vault-path.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/configurations_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/configurations_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/gp_installer_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/gp_installer_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/index_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/index_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/init_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/init_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/setup_gitpages_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/setup_gitpages_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/html/test_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/html/test_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/js/core.js` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/js/core.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/action_components.css` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/action_components.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/flex.css` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/flex.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/main.css` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/main.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/installer/units/style/response.css` & `obsidianhtml-3.5.1/obsidianhtml/src/installer/units/style/response.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/js/encoding.js` & `obsidianhtml-3.5.1/obsidianhtml/src/js/encoding.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/js/load_dirtree_footer.js` & `obsidianhtml-3.5.1/obsidianhtml/src/js/load_dirtree_footer.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/js/obsidian_core.js` & `obsidianhtml-3.5.1/obsidianhtml/src/js/obsidian_core.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/js/obsidian_tabs_footer.js` & `obsidianhtml-3.5.1/obsidianhtml/src/js/obsidian_tabs_footer.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/rss/channel_template.xml` & `obsidianhtml-3.5.1/obsidianhtml/src/rss/channel_template.xml`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/rss/rss.svg` & `obsidianhtml-3.5.1/obsidianhtml/src/rss/rss.svg`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/button_template.html` & `obsidianhtml-3.5.1/obsidianhtml/src/search/button_template.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/pako.js` & `obsidianhtml-3.5.1/obsidianhtml/src/search/pako.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/search.css` & `obsidianhtml-3.5.1/obsidianhtml/src/search/search.css`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/search.html` & `obsidianhtml-3.5.1/obsidianhtml/src/search/search.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/search.js` & `obsidianhtml-3.5.1/obsidianhtml/src/search/search.js`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/search/search.svg` & `obsidianhtml-3.5.1/obsidianhtml/src/search/search.svg`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/svgs/cite.html` & `obsidianhtml-3.5.1/obsidianhtml/src/svgs/cite.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/svgs/external.svg` & `obsidianhtml-3.5.1/obsidianhtml/src/svgs/external.svg`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/svgs/hashtag.svg` & `obsidianhtml-3.5.1/obsidianhtml/src/svgs/hashtag.svg`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml/src/svgs/quote.html` & `obsidianhtml-3.5.1/obsidianhtml/src/svgs/quote.html`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml.egg-info/PKG-INFO` & `obsidianhtml-3.5.1/obsidianhtml.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: obsidianhtml
-Version: 3.5.0
+Version: 3.5.1
 Summary: Converts Obsidian notes into proper markdown and HTML
 Home-page: https://github.com/obsidian-html/obsidian-html
 Author: https://github.com/dwrolvink
 Author-email: dwrolvink@protonmail.com
 License: GNU General Public License v3 or later (GPLv3+)
 Keywords: html,markdown,notes,markdown-to-html,note-taking,obsidian,html-css-javascript,notes-app,obsidian-md,obsidian-html,obsidianmd,obsidian-notes
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `obsidianhtml-3.5.0/obsidianhtml.egg-info/SOURCES.txt` & `obsidianhtml-3.5.1/obsidianhtml.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/obsidianhtml.egg-info/entry_points.txt` & `obsidianhtml-3.5.1/obsidianhtml.egg-info/entry_points.txt`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/pypi_readme.md` & `obsidianhtml-3.5.1/pypi_readme.md`

 * *Files identical despite different names*

### Comparing `obsidianhtml-3.5.0/setup.cfg` & `obsidianhtml-3.5.1/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = obsidianhtml
-version = 3.5.0
+version = 3.5.1
 summary = Converts Obsidian notes into proper markdown and HTML
 long_description = file: pypi_readme.md
 home_page = https://github.com/obsidian-html/obsidian-html
 author = https://github.com/dwrolvink
 author_email = dwrolvink@protonmail.com
 license = GNU General Public License v3 or later (GPLv3+)
 classifiers =
```

