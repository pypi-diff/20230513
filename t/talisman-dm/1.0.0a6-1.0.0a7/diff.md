# Comparing `tmp/talisman-dm-1.0.0a6.tar.gz` & `tmp/talisman-dm-1.0.0a7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/talisman-dm-1.0.0a6.tar", last modified: Mon Apr 24 13:34:20 2023, max compression
+gzip compressed data, was "dist/talisman-dm-1.0.0a7.tar", last modified: Wed May 10 12:47:08 2023, max compression
```

## Comparing `talisman-dm-1.0.0a6.tar` & `talisman-dm-1.0.0a7.tar`

### file list

```diff
@@ -1,117 +1,123 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/
--rw-r--r--   0 root         (0) root         (0)      778 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)       61 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/README.md
--rw-rw-rw-   0 root         (0) root         (0)        7 2023-04-24 13:21:39.000000 talisman-dm-1.0.0a6/VERSION
--rw-r--r--   0 root         (0) root         (0)       38 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)     1195 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/
--rw-r--r--   0 root         (0) root         (0)      778 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     2993 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       63 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        4 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/talisman_dm.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/
--rw-rw-rw-   0 root         (0) root         (0)      320 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/abstract/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-04-24 13:34:12.000000 talisman-dm-1.0.0a6/tdm/abstract/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/
--rw-rw-rw-   0 root         (0) root         (0)      908 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1095 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/base.py
--rw-rw-rw-   0 root         (0) root         (0)      247 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/directive.py
--rw-rw-rw-   0 root         (0) root         (0)     5052 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/document.py
--rw-rw-rw-   0 root         (0) root         (0)     3071 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/fact.py
--rw-rw-rw-   0 root         (0) root         (0)      604 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/fact_filter.py
--rw-rw-rw-   0 root         (0) root         (0)      940 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/link.py
--rw-rw-rw-   0 root         (0) root         (0)     1793 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/markup.py
--rw-rw-rw-   0 root         (0) root         (0)      258 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/mention.py
--rw-rw-rw-   0 root         (0) root         (0)     1626 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/node.py
--rw-rw-rw-   0 root         (0) root         (0)      996 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/datamodel/value.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/
--rw-rw-rw-   0 root         (0) root         (0)      278 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     4947 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/composite.py
--rw-rw-rw-   0 root         (0) root         (0)     1184 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/decorator.py
--rw-rw-rw-   0 root         (0) root         (0)     4507 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/model.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/
--rw-rw-rw-   0 root         (0) root         (0)      624 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1207 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/abstract.py
--rw-rw-rw-   0 root         (0) root         (0)      704 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/identifiable.py
--rw-rw-rw-   0 root         (0) root         (0)      590 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/markup.py
--rw-rw-rw-   0 root         (0) root         (0)      653 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/mention.py
--rw-rw-rw-   0 root         (0) root         (0)      641 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/metadata.py
--rw-rw-rw-   0 root         (0) root         (0)      732 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/serializers.py
--rw-rw-rw-   0 root         (0) root         (0)      632 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/value.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-04-24 13:34:12.000000 talisman-dm-1.0.0a6/tdm/datamodel/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/directives/
--rw-rw-rw-   0 root         (0) root         (0)      239 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/directives/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      436 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/directives/account.py
--rw-rw-rw-   0 root         (0) root         (0)      768 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/directives/concept.py
--rw-rw-rw-   0 root         (0) root         (0)      488 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/directives/platform.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/
--rw-rw-rw-   0 root         (0) root         (0)      155 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     6465 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_base.py
--rw-rw-rw-   0 root         (0) root         (0)     2455 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_container.py
--rw-rw-rw-   0 root         (0) root         (0)     1829 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_factory.py
--rw-rw-rw-   0 root         (0) root         (0)    13671 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_impl.py
--rw-rw-rw-   0 root         (0) root         (0)     7193 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_structure.py
--rw-rw-rw-   0 root         (0) root         (0)      768 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_types.py
--rw-rw-rw-   0 root         (0) root         (0)     5139 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/document/_view.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/
--rw-rw-rw-   0 root         (0) root         (0)      429 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     2424 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/concept.py
--rw-rw-rw-   0 root         (0) root         (0)      911 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/links.py
--rw-rw-rw-   0 root         (0) root         (0)     1106 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/mention.py
--rw-rw-rw-   0 root         (0) root         (0)     2473 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/facts/value.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/links/
--rw-rw-rw-   0 root         (0) root         (0)      155 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/links/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      962 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/links/reference.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/mentions/
--rw-rw-rw-   0 root         (0) root         (0)      180 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/mentions/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1121 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/mentions/image.py
--rw-rw-rw-   0 root         (0) root         (0)      233 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/mentions/node.py
--rw-rw-rw-   0 root         (0) root         (0)      759 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/mentions/text.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/
--rw-rw-rw-   0 root         (0) root         (0)      649 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      428 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/base64.py
--rw-rw-rw-   0 root         (0) root         (0)      705 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/file.py
--rw-rw-rw-   0 root         (0) root         (0)     1113 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/structure.py
--rw-rw-rw-   0 root         (0) root         (0)      938 2023-04-24 13:20:28.000000 talisman-dm-1.0.0a6/tdm/datamodel/nodes/text.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/
--rw-rw-rw-   0 root         (0) root         (0)      265 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      875 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/date.py
--rw-rw-rw-   0 root         (0) root         (0)      790 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/geo.py
--rw-rw-rw-   0 root         (0) root         (0)      333 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/link.py
--rw-rw-rw-   0 root         (0) root         (0)      717 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/datamodel/values/scalar.py
--rw-rw-rw-   0 root         (0) root         (0)     2747 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/helper.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/json_schema/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-04-24 13:34:12.000000 talisman-dm-1.0.0a6/tdm/json_schema/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      512 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/directives.py
--rw-rw-rw-   0 root         (0) root         (0)      514 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/facts.py
--rw-rw-rw-   0 root         (0) root         (0)      427 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/links.py
--rw-rw-rw-   0 root         (0) root         (0)      627 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/mentions.py
--rw-rw-rw-   0 root         (0) root         (0)     1789 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/nodes.py
--rw-rw-rw-   0 root         (0) root         (0)      513 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/json_schema/values.py
--rw-rw-rw-   0 root         (0) root         (0)     1033 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/legacy.py
--rw-rw-rw-   0 root         (0) root         (0)     2808 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/model.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/v0/
--rw-rw-rw-   0 root         (0) root         (0)       90 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/
--rw-rw-rw-   0 root         (0) root         (0)       87 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      905 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/content.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/
--rw-rw-rw-   0 root         (0) root         (0)      348 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     4731 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_facts.py
--rw-rw-rw-   0 root         (0) root         (0)     1630 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_metadata.py
--rw-rw-rw-   0 root         (0) root         (0)     4725 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_nodes.py
--rw-rw-rw-   0 root         (0) root         (0)     1481 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/directive.py
--rw-rw-rw-   0 root         (0) root         (0)     3689 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/document.py
--rw-rw-rw-   0 root         (0) root         (0)     1453 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/fact.py
--rw-rw-rw-   0 root         (0) root         (0)      445 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/v0/json_schema/metadata.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/wrapper/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-04-24 13:34:12.000000 talisman-dm-1.0.0a6/tdm/wrapper/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-24 13:34:20.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/
--rw-rw-rw-   0 root         (0) root         (0)      434 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     2633 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/_decorator.py
--rw-rw-rw-   0 root         (0) root         (0)      551 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/_delegate.py
--rw-rw-rw-   0 root         (0) root         (0)     1647 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/_impl.py
--rw-rw-rw-   0 root         (0) root         (0)      445 2023-04-24 10:06:58.000000 talisman-dm-1.0.0a6/tdm/wrapper/node/_interface.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/
+-rw-r--r--   0 root         (0) root         (0)      778 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)       61 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/README.md
+-rw-rw-rw-   0 root         (0) root         (0)        7 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/VERSION
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)     1195 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      778 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     3197 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       63 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        4 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/talisman_dm.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/
+-rw-rw-rw-   0 root         (0) root         (0)      320 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/abstract/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/
+-rw-rw-rw-   0 root         (0) root         (0)      908 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1095 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/base.py
+-rw-rw-rw-   0 root         (0) root         (0)      247 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/directive.py
+-rw-rw-rw-   0 root         (0) root         (0)     5072 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/document.py
+-rw-rw-rw-   0 root         (0) root         (0)     3071 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/fact.py
+-rw-rw-rw-   0 root         (0) root         (0)      604 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/fact_filter.py
+-rw-rw-rw-   0 root         (0) root         (0)      940 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/link.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/
+-rw-rw-rw-   0 root         (0) root         (0)      122 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      538 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/_helper.py
+-rw-rw-rw-   0 root         (0) root         (0)      653 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/abstract.py
+-rw-rw-rw-   0 root         (0) root         (0)      795 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/frozen.py
+-rw-rw-rw-   0 root         (0) root         (0)      300 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/markup/model.py
+-rw-rw-rw-   0 root         (0) root         (0)      258 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/mention.py
+-rw-rw-rw-   0 root         (0) root         (0)     1626 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/node.py
+-rw-rw-rw-   0 root         (0) root         (0)      996 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/datamodel/value.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/
+-rw-rw-rw-   0 root         (0) root         (0)      278 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     4947 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/composite.py
+-rw-rw-rw-   0 root         (0) root         (0)     1184 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/decorator.py
+-rw-rw-rw-   0 root         (0) root         (0)     4547 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/model.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/
+-rw-rw-rw-   0 root         (0) root         (0)      624 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1207 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/abstract.py
+-rw-rw-rw-   0 root         (0) root         (0)      704 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/identifiable.py
+-rw-rw-rw-   0 root         (0) root         (0)      590 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/markup.py
+-rw-rw-rw-   0 root         (0) root         (0)      653 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/mention.py
+-rw-rw-rw-   0 root         (0) root         (0)      641 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/metadata.py
+-rw-rw-rw-   0 root         (0) root         (0)      732 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/serializers.py
+-rw-rw-rw-   0 root         (0) root         (0)      632 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/value.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/directives/
+-rw-rw-rw-   0 root         (0) root         (0)      239 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/directives/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      436 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/directives/account.py
+-rw-rw-rw-   0 root         (0) root         (0)      768 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/directives/concept.py
+-rw-rw-rw-   0 root         (0) root         (0)      488 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/directives/platform.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/
+-rw-rw-rw-   0 root         (0) root         (0)      155 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     7372 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_base.py
+-rw-rw-rw-   0 root         (0) root         (0)     2455 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_container.py
+-rw-rw-rw-   0 root         (0) root         (0)     1829 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_factory.py
+-rw-rw-rw-   0 root         (0) root         (0)    13671 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_impl.py
+-rw-rw-rw-   0 root         (0) root         (0)      638 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_state.py
+-rw-rw-rw-   0 root         (0) root         (0)     7193 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_structure.py
+-rw-rw-rw-   0 root         (0) root         (0)      768 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_types.py
+-rw-rw-rw-   0 root         (0) root         (0)     5206 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/document/_view.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/
+-rw-rw-rw-   0 root         (0) root         (0)      429 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     2424 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/concept.py
+-rw-rw-rw-   0 root         (0) root         (0)      911 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/links.py
+-rw-rw-rw-   0 root         (0) root         (0)     1106 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/mention.py
+-rw-rw-rw-   0 root         (0) root         (0)     2473 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/facts/value.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/links/
+-rw-rw-rw-   0 root         (0) root         (0)      155 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/links/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      962 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/links/reference.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/mentions/
+-rw-rw-rw-   0 root         (0) root         (0)      180 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/mentions/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1121 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/mentions/image.py
+-rw-rw-rw-   0 root         (0) root         (0)      233 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/mentions/node.py
+-rw-rw-rw-   0 root         (0) root         (0)      759 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/mentions/text.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/
+-rw-rw-rw-   0 root         (0) root         (0)      649 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      428 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/base64.py
+-rw-rw-rw-   0 root         (0) root         (0)      705 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/file.py
+-rw-rw-rw-   0 root         (0) root         (0)     1113 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/structure.py
+-rw-rw-rw-   0 root         (0) root         (0)      938 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/nodes/text.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/
+-rw-rw-rw-   0 root         (0) root         (0)      265 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      875 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/date.py
+-rw-rw-rw-   0 root         (0) root         (0)      790 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/geo.py
+-rw-rw-rw-   0 root         (0) root         (0)      333 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/link.py
+-rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/datamodel/values/scalar.py
+-rw-rw-rw-   0 root         (0) root         (0)     3077 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/helper.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/json_schema/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      512 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/directives.py
+-rw-rw-rw-   0 root         (0) root         (0)      514 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/facts.py
+-rw-rw-rw-   0 root         (0) root         (0)      427 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/links.py
+-rw-rw-rw-   0 root         (0) root         (0)      627 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/mentions.py
+-rw-rw-rw-   0 root         (0) root         (0)     1829 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/nodes.py
+-rw-rw-rw-   0 root         (0) root         (0)      513 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/json_schema/values.py
+-rw-rw-rw-   0 root         (0) root         (0)     1033 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/legacy.py
+-rw-rw-rw-   0 root         (0) root         (0)     2808 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/model.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/v0/
+-rw-rw-rw-   0 root         (0) root         (0)       90 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/
+-rw-rw-rw-   0 root         (0) root         (0)       87 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      905 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/content.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/
+-rw-rw-rw-   0 root         (0) root         (0)      348 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     4731 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_facts.py
+-rw-rw-rw-   0 root         (0) root         (0)     1630 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_metadata.py
+-rw-rw-rw-   0 root         (0) root         (0)     4725 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_nodes.py
+-rw-rw-rw-   0 root         (0) root         (0)     1481 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/directive.py
+-rw-rw-rw-   0 root         (0) root         (0)     3689 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/document.py
+-rw-rw-rw-   0 root         (0) root         (0)     1453 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/fact.py
+-rw-rw-rw-   0 root         (0) root         (0)      445 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/v0/json_schema/metadata.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/wrapper/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-10 12:47:08.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/
+-rw-rw-rw-   0 root         (0) root         (0)      564 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     5509 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/_decorator.py
+-rw-rw-rw-   0 root         (0) root         (0)     1110 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/_delegate.py
+-rw-rw-rw-   0 root         (0) root         (0)     1647 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/_impl.py
+-rw-rw-rw-   0 root         (0) root         (0)      445 2023-05-10 12:46:47.000000 talisman-dm-1.0.0a7/tdm/wrapper/node/_interface.py
```

### Comparing `talisman-dm-1.0.0a6/PKG-INFO` & `talisman-dm-1.0.0a7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: talisman-dm
-Version: 1.0.0a6
+Version: 1.0.0a7
 Summary: Talisman Document Model python implementation
 Home-page: https://gitlab.at.ispras.ru/talisman/core/talisman-tdm
 Author: ISPRAS MODIS NLP team
 Author-email: modis@ispras.ru
 Maintainer: Vladimir Mayorov
 Maintainer-email: vmayorov@ispras.ru
 License: Apache Software License
```

### Comparing `talisman-dm-1.0.0a6/setup.py` & `talisman-dm-1.0.0a7/setup.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/talisman_dm.egg-info/PKG-INFO` & `talisman-dm-1.0.0a7/talisman_dm.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: talisman-dm
-Version: 1.0.0a6
+Version: 1.0.0a7
 Summary: Talisman Document Model python implementation
 Home-page: https://gitlab.at.ispras.ru/talisman/core/talisman-tdm
 Author: ISPRAS MODIS NLP team
 Author-email: modis@ispras.ru
 Maintainer: Vladimir Mayorov
 Maintainer-email: vmayorov@ispras.ru
 License: Apache Software License
```

### Comparing `talisman-dm-1.0.0a6/talisman_dm.egg-info/SOURCES.txt` & `talisman-dm-1.0.0a7/talisman_dm.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -14,18 +14,22 @@
 tdm/abstract/datamodel/__init__.py
 tdm/abstract/datamodel/base.py
 tdm/abstract/datamodel/directive.py
 tdm/abstract/datamodel/document.py
 tdm/abstract/datamodel/fact.py
 tdm/abstract/datamodel/fact_filter.py
 tdm/abstract/datamodel/link.py
-tdm/abstract/datamodel/markup.py
 tdm/abstract/datamodel/mention.py
 tdm/abstract/datamodel/node.py
 tdm/abstract/datamodel/value.py
+tdm/abstract/datamodel/markup/__init__.py
+tdm/abstract/datamodel/markup/_helper.py
+tdm/abstract/datamodel/markup/abstract.py
+tdm/abstract/datamodel/markup/frozen.py
+tdm/abstract/datamodel/markup/model.py
 tdm/abstract/json_schema/__init__.py
 tdm/abstract/json_schema/composite.py
 tdm/abstract/json_schema/decorator.py
 tdm/abstract/json_schema/model.py
 tdm/abstract/json_schema/serializers/__init__.py
 tdm/abstract/json_schema/serializers/abstract.py
 tdm/abstract/json_schema/serializers/identifiable.py
@@ -40,14 +44,15 @@
 tdm/datamodel/directives/concept.py
 tdm/datamodel/directives/platform.py
 tdm/datamodel/document/__init__.py
 tdm/datamodel/document/_base.py
 tdm/datamodel/document/_container.py
 tdm/datamodel/document/_factory.py
 tdm/datamodel/document/_impl.py
+tdm/datamodel/document/_state.py
 tdm/datamodel/document/_structure.py
 tdm/datamodel/document/_types.py
 tdm/datamodel/document/_view.py
 tdm/datamodel/facts/__init__.py
 tdm/datamodel/facts/concept.py
 tdm/datamodel/facts/links.py
 tdm/datamodel/facts/mention.py
```

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/__init__.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/__init__.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/base.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/base.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/document.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/document.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,14 +12,16 @@
 _NodeLink = TypeVar('_NodeLink', bound=AbstractNodeLink)
 _Node = TypeVar('_Node', bound=AbstractNode)
 
 NodeOrId = Union[str, AbstractNode]
 
 
 class TalismanDocument(metaclass=ABCMeta):
+    __slots__ = ()
+
     @property
     @abstractmethod
     def id(self) -> str:
         pass
 
     @property
     @abstractmethod
```

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/fact.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/fact.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/fact_filter.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/fact_filter.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/link.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/link.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/node.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/node.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/datamodel/value.py` & `talisman-dm-1.0.0a7/tdm/abstract/datamodel/value.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/composite.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/composite.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/decorator.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/decorator.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/model.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/model.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from collections import defaultdict
 from dataclasses import fields
 from typing import Any, Dict, Generic, List, Optional, Sequence, Type, TypeVar, Union
 
 from pydantic import BaseModel, Extra, create_model, root_validator
 from typing_extensions import Literal, Self
 
-from tdm.helper import cache_result, generics_mapping, unfold_union, uniform_collection
+from tdm.helper import cache_result, generics_mapping, register_in_module, unfold_union, uniform_collection
 from .serializers import AbstractElementModel, AbstractElementSerializer, BaseSerializers
 
 _Element = TypeVar('_Element')
 
 
 # hackish root validator solution as normal validators are not called for skipped required fields
 def set_type_if_none(cls, values):
@@ -92,15 +92,15 @@
             field_type = Union[tuple(f_t)]
 
         model_fields[name] = (field_type, default_value)
     if label:
         model_fields['type'] = (Literal[label], ...)
         validators['set_if_none'] = root_validator(pre=True, allow_reuse=True)(set_type_if_none)
 
-    model = create_model(f"{type_.__name__}Model", __base__=ElementModel, __validators__=validators, **model_fields)
+    model = register_in_module(create_model(f"{type_.__name__}Model", __base__=ElementModel, __validators__=validators, **model_fields))
 
     def deserialize(self: model, typed_id2element: Dict[type, Dict[str, Any]]) -> type_:
         kwargs = {}
         for f in set(type_.__dataclass_fields__).intersection(self.__dict__):
             kwargs[f] = getattr(self, f)
             if f in special_fields:
                 for deserializer in special_fields[f]:
```

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/__init__.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/__init__.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/abstract.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/abstract.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/identifiable.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/identifiable.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/markup.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/markup.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/mention.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/mention.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/metadata.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/metadata.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/serializers.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/serializers.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/abstract/json_schema/serializers/value.py` & `talisman-dm-1.0.0a7/tdm/abstract/json_schema/serializers/value.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/directives/concept.py` & `talisman-dm-1.0.0a7/tdm/datamodel/directives/concept.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_base.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_base.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,40 @@
 from collections import defaultdict
+from itertools import chain
 from typing import Dict, Iterable, Set, Tuple, Type, TypeVar, Union
 
 from tdm.abstract.datamodel import EnsureIdentifiable
 from ._container import TypedIdsContainer
+from ._state import pack_view_state, unpack_view_state
 from ._types import get_base_type
 from ._view import AbstractView, object_view
 
 _TD = TypeVar('_TD', bound='BaseImpl')
 
 
 class BaseImpl(object):
     __slots__ = (
         '_id2view', '_dependencies', '_containers'
     )
 
+    def __setstate__(self, state):
+        d, s = state
+        if d is not None:
+            self.__dict__.update(d)
+        s['_id2view'] = unpack_view_state(s['_id2view'])
+        for slot in chain.from_iterable(getattr(cls, '__slots__', ()) for cls in type(self).mro()):
+            setattr(self, slot, s.get(slot, None))
+
+    def __getstate__(self):
+        result = {slot: getattr(self, slot, None) for slot in
+                  chain.from_iterable(getattr(cls, '__slots__', ()) for cls in type(self).mro())}
+        result['_id2view'] = pack_view_state(result.get('_id2view', {}))
+        d = self.__dict__ if hasattr(self, '__dict__') else None
+        return d, result
+
     def __init__(
             self,
             id2view: Dict[str, Union[EnsureIdentifiable, AbstractView]],
             dependencies: Dict[str, Set[Tuple[str, Type[EnsureIdentifiable]]]],
             containers: Dict[Type[EnsureIdentifiable], TypedIdsContainer],
     ):
         self._id2view = id2view
@@ -78,20 +95,24 @@
                     if dep not in ids:
                         raise ValueError(f"Couldn't remove element {id_} as it depends on element {dep}")
         remove_from_containers = defaultdict(set)
         id2view = dict(self._id2view)
         dependencies = dict(self._dependencies)
         updated = set()
         remove = defaultdict(set)
+        removed_ids = set()
         for id_ in ids:
             remove[get_base_type(id2view[id_].orig_type())].add(id_)
         while remove:
             to_remove = defaultdict(set)
             for base_type, ids in remove.items():
                 for id_ in ids:
+                    if id_ in removed_ids:
+                        continue
+                    removed_ids.add(id_)
                     for dep_id, dep_type in dependencies.get(id_, ()):
                         to_remove[dep_type].add(dep_id)
                     view = id2view.pop(id_)
                     dependencies.pop(id_, None)
                     remove_from_containers[base_type].add(id_)
                     if not isinstance(view, AbstractView):
                         continue
```

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_container.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_container.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_factory.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_factory.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_impl.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_impl.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_structure.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_structure.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_types.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_types.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/document/_view.py` & `talisman-dm-1.0.0a7/tdm/datamodel/document/_view.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from abc import abstractmethod
 from dataclasses import dataclass, fields, is_dataclass, make_dataclass
 from typing import Callable, Dict, Generic, Set, Tuple, Type, TypeVar, Union
 
 from tdm.abstract.datamodel import EnsureIdentifiable
-from tdm.helper import generics_mapping, is_subclass
+from tdm.helper import generics_mapping, is_subclass, register_in_module
 
 _T = TypeVar('_T', bound=EnsureIdentifiable)
 
 
 @dataclass(frozen=True)
 class AbstractView(Generic[_T]):
     __depends_on__: Set[str]
@@ -123,14 +123,16 @@
             'orig_type': lambda _: type_,
             'get_dependencies': get_dependencies,
             '__eq__': eq
         },
         frozen=True
     )
 
+    view_type = register_in_module(view_type)
+
     __depends_on__ = generate_depends_on(id_fields, restore_fields)
 
     def constructor(obj: _ST) -> _TT:
         view = {name: fc(getattr(obj, name)) for name, fc in constructor_fields.items()}
         return view_type(__depends_on__=__depends_on__(view), **view)
 
     _CACHE[type_] = view_type, constructor
```

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/facts/concept.py` & `talisman-dm-1.0.0a7/tdm/datamodel/facts/concept.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/facts/links.py` & `talisman-dm-1.0.0a7/tdm/datamodel/facts/links.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/facts/mention.py` & `talisman-dm-1.0.0a7/tdm/datamodel/facts/mention.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/facts/value.py` & `talisman-dm-1.0.0a7/tdm/datamodel/facts/value.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/links/reference.py` & `talisman-dm-1.0.0a7/tdm/datamodel/links/reference.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/mentions/image.py` & `talisman-dm-1.0.0a7/tdm/datamodel/mentions/image.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/mentions/text.py` & `talisman-dm-1.0.0a7/tdm/datamodel/mentions/text.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/nodes/__init__.py` & `talisman-dm-1.0.0a7/tdm/datamodel/nodes/__init__.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/nodes/file.py` & `talisman-dm-1.0.0a7/tdm/datamodel/nodes/file.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/nodes/structure.py` & `talisman-dm-1.0.0a7/tdm/datamodel/nodes/structure.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/nodes/text.py` & `talisman-dm-1.0.0a7/tdm/datamodel/nodes/text.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/values/date.py` & `talisman-dm-1.0.0a7/tdm/datamodel/values/date.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/values/geo.py` & `talisman-dm-1.0.0a7/tdm/datamodel/values/geo.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/datamodel/values/scalar.py` & `talisman-dm-1.0.0a7/tdm/datamodel/values/scalar.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/helper.py` & `talisman-dm-1.0.0a7/tdm/helper.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+import sys
 from typing import Any, Callable, Collection, Dict, Generic, List, Optional, Set, Tuple, TypeVar, Union
 
 
 def unfold_union(type_: type) -> Tuple[type, ...]:
     # check if it is union
     if hasattr(type_, '__origin__') and type_.__origin__ is Union:
         return type_.__args__
@@ -79,7 +80,21 @@
         # assume type vars are not intersect
         result = {}
         for orig_base in type_.__orig_bases__:
             if '__origin__' in orig_base.__dict__ and '__args__' in orig_base.__dict__:
                 result.update(dict(zip(orig_base.__origin__.__parameters__, orig_base.__args__)))
         return result
     return {}
+
+
+_T = TypeVar('_T', bound=type)
+
+
+def register_in_module(t: _T) -> _T:
+    module = t.__module__
+    name = t.__name__
+    if hasattr(sys.modules[module], name):
+        if getattr(sys.modules[module], name) is not t:
+            raise RuntimeError
+    else:
+        setattr(sys.modules[module], name, t)
+    return t
```

### Comparing `talisman-dm-1.0.0a6/tdm/json_schema/directives.py` & `talisman-dm-1.0.0a7/tdm/json_schema/directives.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/json_schema/facts.py` & `talisman-dm-1.0.0a7/tdm/json_schema/facts.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/json_schema/mentions.py` & `talisman-dm-1.0.0a7/tdm/json_schema/mentions.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/json_schema/nodes.py` & `talisman-dm-1.0.0a7/tdm/json_schema/nodes.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import Callable, Iterable, Tuple, Type, Union
 
 from pydantic import Field, create_model
 from typing_extensions import Annotated
 
 from tdm.abstract.datamodel import AbstractNode, TalismanDocument
 from tdm.abstract.json_schema import ElementModel, get_model_generator
-from tdm.helper import unfold_union
+from tdm.helper import register_in_module, unfold_union
 
 
 def register_node_models() -> Tuple[Type[ElementModel[AbstractNode]], Callable[[AbstractNode], ElementModel[AbstractNode]]]:
     import tdm.datamodel.nodes as nodes  # we need this import for serializers registration
     nodes
 
     # TODO: here plugin for extra document nodes could be added
@@ -21,15 +21,15 @@
         'children': (Tuple[str, ...], ...)
     }
 
     model_mapping = {}
     tree_models = []
 
     for model in unfold_union(models[AbstractNode]):
-        tree_model = create_model(f"Tree{model.__name__}", __base__=model, **kwargs)
+        tree_model = register_in_module(create_model(f"Tree{model.__name__}", __base__=model, **kwargs))
         model_mapping[model] = tree_model
         tree_models.append(tree_model)
 
     NodeModel_ = Annotated[Union[tuple(tree_models)], Field(discriminator='type')]  # noqa N806
 
     # wrap serialize to generate tree node instead of node
     def serialize_node(node: AbstractNode) -> ElementModel[AbstractNode]:
```

### Comparing `talisman-dm-1.0.0a6/tdm/json_schema/values.py` & `talisman-dm-1.0.0a7/tdm/json_schema/values.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/legacy.py` & `talisman-dm-1.0.0a7/tdm/legacy.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/model.py` & `talisman-dm-1.0.0a7/tdm/model.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/content.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/content.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_facts.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_facts.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_metadata.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_metadata.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/convert/_nodes.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/convert/_nodes.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/directive.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/directive.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/document.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/document.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/v0/json_schema/fact.py` & `talisman-dm-1.0.0a7/tdm/v0/json_schema/fact.py`

 * *Files identical despite different names*

### Comparing `talisman-dm-1.0.0a6/tdm/wrapper/node/_impl.py` & `talisman-dm-1.0.0a7/tdm/wrapper/node/_impl.py`

 * *Files identical despite different names*

