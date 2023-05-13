# Comparing `tmp/ksconf-0.10.1.tar.gz` & `tmp/ksconf-0.10.2a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ksconf-0.10.1.tar", last modified: Tue Mar  7 20:38:56 2023, max compression
+gzip compressed data, was "ksconf-0.10.2a1.tar", last modified: Sat May 13 00:47:32 2023, max compression
```

## Comparing `ksconf-0.10.1.tar` & `ksconf-0.10.2a1.tar`

### file list

```diff
@@ -1,66 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/
--rw-r--r--   0 runner    (1001) docker     (123)    10752 2023-03-07 20:38:35.000000 ksconf-0.10.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-03-07 20:38:56.233385 ksconf-0.10.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-03-07 20:38:35.000000 ksconf-0.10.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.225385 ksconf-0.10.1/ksconf/
--rw-r--r--   0 runner    (1001) docker     (123)     4418 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      308 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)     2982 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/archive.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.229385 ksconf-0.10.1/ksconf/builder/
--rw-r--r--   0 runner    (1001) docker     (123)     5145 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/builder/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7625 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/builder/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)    10754 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/builder/core.py
--rw-r--r--   0 runner    (1001) docker     (123)     6780 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/builder/steps.py
--rw-r--r--   0 runner    (1001) docker     (123)    11430 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)    10405 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/combine.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/ksconf/commands/
--rw-r--r--   0 runner    (1001) docker     (123)    22197 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3716 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/check.py
--rw-r--r--   0 runner    (1001) docker     (123)    13705 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/combine.py
--rw-r--r--   0 runner    (1001) docker     (123)     3567 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/diff.py
--rw-r--r--   0 runner    (1001) docker     (123)    12040 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/merge.py
--rw-r--r--   0 runner    (1001) docker     (123)     8654 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/minimize.py
--rw-r--r--   0 runner    (1001) docker     (123)    11547 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/package.py
--rw-r--r--   0 runner    (1001) docker     (123)    22959 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/promote.py
--rw-r--r--   0 runner    (1001) docker     (123)    10977 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/restexport.py
--rw-r--r--   0 runner    (1001) docker     (123)    15603 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/restpublish.py
--rw-r--r--   0 runner    (1001) docker     (123)     6241 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/snapshot.py
--rw-r--r--   0 runner    (1001) docker     (123)     5567 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/sort.py
--rw-r--r--   0 runner    (1001) docker     (123)    22799 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/unarchive.py
--rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/commands/xmlformat.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/ksconf/conf/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/conf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18249 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/conf/delta.py
--rw-r--r--   0 runner    (1001) docker     (123)     6664 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/conf/merge.py
--rw-r--r--   0 runner    (1001) docker     (123)     5193 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/conf/meta.py
--rw-r--r--   0 runner    (1001) docker     (123)    18619 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/conf/parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1623 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/consts.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/ksconf/ext/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/ext/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6503 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/filter.py
--rw-r--r--   0 runner    (1001) docker     (123)    15185 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/layer.py
--rw-r--r--   0 runner    (1001) docker     (123)    13866 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/package.py
--rw-r--r--   0 runner    (1001) docker     (123)     2817 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/setup_entrypoints.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/ksconf/util/
--rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      799 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/compare.py
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/completers.py
--rw-r--r--   0 runner    (1001) docker     (123)     5609 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/file.py
--rw-r--r--   0 runner    (1001) docker     (123)      527 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/rest.py
--rw-r--r--   0 runner    (1001) docker     (123)     1121 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/util/terminal.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.233385 ksconf-0.10.1/ksconf/vc/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/vc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4194 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/vc/git.py
--rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-03-07 20:38:35.000000 ksconf-0.10.1/ksconf/xmlformat.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 20:38:56.229385 ksconf-0.10.1/ksconf.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      701 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-03-07 20:38:56.000000 ksconf-0.10.1/ksconf.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-07 20:38:43.000000 ksconf-0.10.1/ksconf.egg-info/zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      443 2023-03-07 20:38:56.233385 ksconf-0.10.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     7245 2023-03-07 20:38:35.000000 ksconf-0.10.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/
+-rw-r--r--   0 runner    (1001) docker     (123)    10752 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2379 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.912813 ksconf-0.10.2a1/ksconf/
+-rw-r--r--   0 runner    (1001) docker     (123)     4418 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      322 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.912813 ksconf-0.10.2a1/ksconf/app/
+-rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/app/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11231 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/app/deploy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5264 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/app/facts.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12268 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/app/manifest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3571 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/archive.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.912813 ksconf-0.10.2a1/ksconf/builder/
+-rw-r--r--   0 runner    (1001) docker     (123)     5147 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/builder/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7627 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/builder/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10752 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/builder/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6780 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/builder/steps.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11430 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10406 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/combine.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.912813 ksconf-0.10.2a1/ksconf/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)    22120 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3716 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/check.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13705 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/combine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3567 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/diff.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12040 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2935 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8654 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/minimize.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11547 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/package.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22959 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/promote.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10977 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/restexport.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15841 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/restpublish.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6241 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/snapshot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5567 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/sort.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21904 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/unarchive.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/commands/xmlformat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2159 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/compat.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/ksconf/conf/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/conf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17805 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/conf/delta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6686 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/conf/merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5193 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/conf/meta.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18619 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/conf/parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1726 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/consts.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/ksconf/ext/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/ext/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6503 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15084 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/layer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13850 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/package.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2817 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/setup_entrypoints.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/ksconf/util/
+-rw-r--r--   0 runner    (1001) docker     (123)      760 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      799 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/compare.py
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/completers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5634 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)      527 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/rest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1121 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/util/terminal.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/ksconf/vc/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/vc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4140 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/vc/git.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6021 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/ksconf/xmlformat.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:47:32.912813 ksconf-0.10.2a1/ksconf.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2379 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      701 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 00:47:32.000000 ksconf-0.10.2a1/ksconf.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:47:17.000000 ksconf-0.10.2a1/ksconf.egg-info/zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      443 2023-05-13 00:47:32.916813 ksconf-0.10.2a1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     7269 2023-05-13 00:47:02.000000 ksconf-0.10.2a1/setup.py
```

### Comparing `ksconf-0.10.1/LICENSE` & `ksconf-0.10.2a1/LICENSE`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/PKG-INFO` & `ksconf-0.10.2a1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ksconf
-Version: 0.10.1
+Version: 0.10.2a1
 Summary: KSCONF: Ksconf Splunk Configuration Tool
 Home-page: https://github.com/Kintyre/ksconf
 Author: Lowell Alleman
 Author-email: lowell@kintyre.co
 License: Apache Software License
 Project-URL: Documentation, https://ksconf.readthedocs.io/
 Project-URL: Splunk app, https://splunkbase.splunk.com/app/4383/
```

### Comparing `ksconf-0.10.1/README.md` & `ksconf-0.10.2a1/README.md`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/__init__.py` & `ksconf-0.10.2a1/ksconf/__init__.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/__main__.py` & `ksconf-0.10.2a1/ksconf/__main__.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/archive.py` & `ksconf-0.10.2a1/ksconf/archive.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,21 +1,27 @@
 from __future__ import absolute_import, unicode_literals
 
 import os
-from collections import namedtuple
 from fnmatch import fnmatch
+from typing import Iterable, NamedTuple, Sequence, Tuple, Union
 
 from ksconf.consts import RegexType
 
-GenArchFile = namedtuple("GenericArchiveEntry", ("path", "mode", "size", "payload"))
 
+class GenArchFile(NamedTuple):
+    path: str
+    mode: int
+    size: int
+    payload: Union[bytes, None]
 
-def extract_archive(archive_name, extract_filter=None):
+
+def extract_archive(archive_name, extract_filter: callable = None) -> Iterable[GenArchFile]:
     if extract_filter is not None and not callable(extract_filter):  # pragma: no cover
         raise ValueError("extract_filter must be a callable!")
+    archive_name = os.fspath(archive_name)
     if archive_name.lower().endswith(".zip"):
         return _extract_zip(archive_name, extract_filter)
     else:
         return _extract_tar(archive_name, extract_filter)
 
 
 def gaf_filter_name_like(pattern):
@@ -59,22 +65,28 @@
                     extract_filter(GenArchFile(zi.filename, mode, zi.file_size, None)):
                 payload = zipf.read(zi)
             else:
                 payload = None
             yield GenArchFile(zi.filename, mode, zi.file_size, payload)
 
 
-def sanity_checker(iterable):
+def sanity_checker(iterable: Iterable[GenArchFile]) -> Iterable[GenArchFile]:
+    # Keep this here for a few versions because some of the cdillc.splunk code references this.
+    from warnings import warn
+    warn("Please use AppManifest.check_paths() instead.  The sanity_checker() "
+         "function will be removed in 1.0 or sooner.", DeprecationWarning)
     for gaf in iterable:
         if gaf.path.startswith("/") or ".." in gaf.path:
             raise ValueError(f"Bad path found in archive:  {gaf.path}")
         yield gaf
 
 
-def gen_arch_file_remapper(iterable, mapping):
+def gen_arch_file_remapper(iterable: Iterable[GenArchFile],
+                           mapping: Sequence[Tuple[str, str]]
+                           ) -> Iterable[GenArchFile]:
     # Mapping is assumed to be a sequence of (find,replace) strings; find can be compiled regex
     for gaf in iterable:
         path = gaf.path
         for (find, replace) in mapping:
             if isinstance(find, RegexType):
                 path = find.sub(replace, path)
             else:
```

### Comparing `ksconf-0.10.1/ksconf/builder/__init__.py` & `ksconf-0.10.2a1/ksconf/builder/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 import inspect
 import os
 import re
 import sys
 from subprocess import Popen
 from typing import Callable, List
 
+from ksconf.compat import handle_py3_kw_only_args
 from ksconf.consts import EXIT_CODE_INTERNAL_ERROR, KSCONF_DEBUG
-from ksconf.util import handle_py3_kw_only_args
 
 QUIET = -1
 NORMAL = 0
 VERBOSE = 1
 
 
 class BuildExternalException(Exception):
```

### Comparing `ksconf-0.10.1/ksconf/builder/cache.py` & `ksconf-0.10.2a1/ksconf/builder/cache.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,17 +10,17 @@
 
 
 class FileSet:
     """ A collection of fingerprinted files.
 
     Currently the fingerprint is only a SHA256 hash.
 
-    Two constructore are provided for building an instance from either file that
+    Two constructors are provided for building an instance from either file that
     live on the filesystem, via :py:meth:`from_filesystem` or from a persisted
-    cached record aviable from the :py:meth:`from_cache`.
+    cached record available from the :py:meth:`from_cache`.
     The filesystem version actively reads all inputs files at object creation
     time, so this can be costly, especially if repeated.
     """
     # XXX: Do we need both files (set), and file_meta (dict)?  Try to make this work with just files_meta
     __slots__ = ["files", "files_meta"]
 
     def __init__(self):
```

### Comparing `ksconf-0.10.1/ksconf/builder/core.py` & `ksconf-0.10.2a1/ksconf/builder/core.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 # -*- coding: utf-8 -*-
 """
 
 
 Cache build requirements:
 
-    * Caching mechanism should inspet 'inputs' (collect file hashes) to determine if any content has
+    * Caching mechanism should inspect 'inputs' (collect file hashes) to determine if any content has
       changed.  If input varies, then command should be re-run.
     * Command (decorated function) should be generally unaware of all other details of build process,
       and it should *ONLY* be able to see files listed in "inputs"
-    * Allow caching to be fully disabled (run in-place with no dir proxying) for CI/CD
+    * Allow caching to be fully disabled (run in-place with no dir proxy) for CI/CD
     * Cache should have allow a timeout parameter
 
 
 decorator used to implement caching:
     * decorator args:
         * inputs:       list or glob
         * outputs       (do we need this, can we just detect this??)
```

### Comparing `ksconf-0.10.1/ksconf/builder/steps.py` & `ksconf-0.10.2a1/ksconf/builder/steps.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/cli.py` & `ksconf-0.10.2a1/ksconf/cli.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/combine.py` & `ksconf-0.10.2a1/ksconf/combine.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,33 +23,35 @@
 
 class LayerCombinerException(Exception):
     pass
 
 
 class LayerCombiner:
     """
-    Class to rescursively combine layers (directories) into a single rendered output target directory.
+    Class to recursively combine layers (directories) into a single rendered output target directory.
     This is heavily used by the ``ksconf combine`` command as well as by the ``package`` command.
 
 
     Typical class use case:
 
     ::
         lc = LayerCombiner()
 
         # Setup source, either
             (1) lc.set_source_dirs()  OR
             (2) lc.set_layer_root()
 
-        Call hierarch:
+    Call hierarch:
+
+    ::
 
         lc.combine()                    Entry point
             -> prepare()                Directory, layer prep
                 -> prepare_target_dir() Make dir; subclass handles marker here (combine CLI)
-            -> pre_combine_inventory()  Hook for pre-processing (or alterting) the set of files to combine
+            -> pre_combine_inventory()  Hook for pre-processing (or alerting) the set of files to combine
             -> combine_files()          Main worker function
             -> post_combine()           Optional, cleanup leftover files
     """
 
     # Note this is case sensitive.  Don't be lazy, name your files correctly  :-)
     conf_file_re = re.compile(r"([a-z_-]+\.conf|(default|local)\.meta)$")
     spec_file_re = re.compile(r"\.conf\.spec$")
@@ -68,15 +70,15 @@
 
         self.config.follow_symlink = follow_symlink
 
         # Internal tracking variables
         self.layer_names_all = set()
         self.layer_names_used = set()
 
-        # Not a great long-term design, but good enough for initial converstion from command-based desgin
+        # Not a great long-term design, but good enough for initial conversion from command-based design
         self.stdout = sys.stdout
         self.stderr = sys.stderr
 
     def set_source_dirs(self, sources: list):
         self.layer_root = DirectLayerRoot(config=self.config)
         for src in sources:
             self.layer_root.add_layer(src)
```

### Comparing `ksconf-0.10.1/ksconf/commands/__init__.py` & `ksconf-0.10.2a1/ksconf/commands/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,19 +9,20 @@
 from argparse import ArgumentParser, ArgumentTypeError
 from collections import namedtuple
 from io import open
 from textwrap import dedent
 from warnings import warn
 
 from ksconf import KsconfPluginWarning
+from ksconf.compat import cache
 from ksconf.conf.parser import (ConfParserException, ParserConfig,
                                 detect_by_bom, parse_conf, smart_write_conf,
                                 write_conf)
 from ksconf.consts import EXIT_CODE_BAD_CONF_FILE, EXIT_CODE_NO_SUCH_FILE, SMART_CREATE, SmartEnum
-from ksconf.util import debug_traceback, memoize
+from ksconf.util import debug_traceback
 
 __all__ = [
     "KsconfCmd",
     "ConfDirProxy",
     "ConfFileProxy",
     "ConfFileType",
     "dedent",
@@ -518,15 +519,15 @@
 if "ksconf_cmd" in os.environ.get("KSCONF_DISABLE_PLUGINS", ""):    # pragma: no cover
     # Only use the fallback built in mechanism.  This is helpful when unittesting and building docs
     # as we don't want to accidentally document/test code from other packages.
     __get_entity_resolvers = [_get_fallback]
 
 
 # This caching is *mostly* beneficial for unittest CLI testing
-@memoize
+@cache
 def get_entrypoints(group, name=None):
 
     for resolver in list(__get_entity_resolvers):
         results = None
         try:
             results = resolver(group, name=name)
         except ImportError:    # pragma: no cover
@@ -562,18 +563,15 @@
                 yield KsconfCmdEntryPoint(name, entry, cmd_cls, msg)
             else:
                 raise RuntimeError(msg)
             continue
         try:
             cmd_cls._handle_imports()
         except ImportError as e:
-            if hasattr(e, "name"):         # PY3
-                module = e.name
-            else:
-                module = e
+            module = e.name
             if on_error == "warn":
                 warn(f"Unable to load external modules for {name}.  Disabling.  "
                      f"{module}.", KsconfPluginWarning)
             elif on_error == "return":
                 error = f"Missing 3rd party module:  {module}"
                 yield KsconfCmdEntryPoint(name, entry, cmd_cls, error)
             else:
```

### Comparing `ksconf-0.10.1/ksconf/commands/check.py` & `ksconf-0.10.2a1/ksconf/commands/check.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/combine.py` & `ksconf-0.10.2a1/ksconf/commands/combine.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/diff.py` & `ksconf-0.10.2a1/ksconf/commands/diff.py`

 * *Files 4% similar despite different names*

```diff
@@ -46,15 +46,15 @@
                             help="Control the highest level for which 'replace' events may occur.")
         parser.add_argument("--comments", "-C",
                             action="store_true", default=False,
                             help="Enable comparison of comments.  (Unlikely to work consistently)")
         parser.add_argument("--format", "-f",
                             choices=["diff", "json"], default="diff",
                             help="Output file format to produce.  'diff' the the classic format used by default. "
-                            "'json' is helpful when trying to review changes programatically .")
+                            "'json' is helpful when trying to review changes programmatically.")
 
     def run(self, args):
         ''' Compare two configuration files. '''
         args.conf1.set_parser_option(keep_comments=args.comments)
         args.conf2.set_parser_option(keep_comments=args.comments)
 
         cfg1 = args.conf1.data
```

### Comparing `ksconf-0.10.1/ksconf/commands/filter.py` & `ksconf-0.10.2a1/ksconf/commands/filter.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/merge.py` & `ksconf-0.10.2a1/ksconf/commands/merge.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/minimize.py` & `ksconf-0.10.2a1/ksconf/commands/minimize.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/package.py` & `ksconf-0.10.2a1/ksconf/commands/package.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/promote.py` & `ksconf-0.10.2a1/ksconf/commands/promote.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/restexport.py` & `ksconf-0.10.2a1/ksconf/commands/restexport.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/restpublish.py` & `ksconf-0.10.2a1/ksconf/commands/restpublish.py`

 * *Files 2% similar despite different names*

```diff
@@ -10,23 +10,23 @@
 
 
 """
 from __future__ import absolute_import, unicode_literals
 
 import os
 import sys
-from argparse import ArgumentParser
+from argparse import ArgumentParser, Namespace
 from urllib.parse import urlparse
 
 from ksconf.commands import (ConfFileProxy, ConfFileType, KsconfCmd,
                              add_splunkd_access_args, add_splunkd_namespace,
                              dedent)
 from ksconf.conf.delta import DiffHeader, compare_stanzas, is_equal, reduce_stanza, show_diff
 from ksconf.conf.meta import MetaData
-from ksconf.conf.parser import GLOBAL_STANZA, PARSECONF_LOOSE, conf_attr_boolean
+from ksconf.conf.parser import GLOBAL_STANZA, PARSECONF_LOOSE, ConfType, conf_attr_boolean
 from ksconf.consts import EXIT_CODE_SUCCESS
 from ksconf.util.completers import conf_files_completer
 
 # Lazy loaded by _handle_imports()
 splunklib = None
 
 
@@ -102,19 +102,19 @@
                             help=dedent("""\
             Remove existing REST entities.  This is a destructive operation.
             In this mode, stanza attributes are unnecessary.
             NOTE:  This works for 'local' entities only; the default folder cannot be updated.
             """))
 
     @staticmethod
-    def make_boolean(stanza, attr="disabled"):
+    def make_boolean(stanza: ConfType, attr: str = "disabled"):
         if attr in stanza:
             stanza[attr] = "1" if conf_attr_boolean(stanza[attr]) else "0"
 
-    def connect_splunkd(self, args):
+    def connect_splunkd(self, args: Namespace):
         up = urlparse(args.url)
         # Take username/password form URL, if encoded there; otherwise use defaults from argparse
         if args.session_key:
             auth_args = {
                 "token": args.session_key
             }
             login_fail_info = f"session={args.session_key[:10]}..."
@@ -136,21 +136,20 @@
             #   (2) confirm that that the given namespace (app) is legit.
             self._service.apps.list()
         except Exception as e:
             sys.stderr.write(f"Connect issue url=https://{up.hostname}:{up.port} "
                              f"{login_fail_info}:  {e}\n")
             raise e
 
-    def handle_conf_file(self, args, conf_proxy):
+    def handle_conf_file(self, args: Namespace, conf_proxy: ConfFileProxy):
         if args.conf_type:
             conf_type = args.conf_type
         else:
             conf_type = os.path.basename(conf_proxy.name).replace(".conf", "")
 
-
         try:
             config_file = self._service.confs[conf_type]
         except KeyError:
             self.stderr.write(f"Invalid conf type named '{conf_type}'.\n")
             return
         conf = conf_proxy.data
 
@@ -187,15 +186,18 @@
 
             if "meta" in info:
                 print(info["meta"])
 
             if "acl_delta" in info:
                 show_diff(self.stdout, info["acl_delta"])
 
-    def publish_conf(self, stanza_name, stanza_data, config_file):
+    def publish_conf(self,
+                     stanza_name: str,
+                     stanza_data: ConfType,
+                     config_file):
         if self.meta:
             metadata = self.meta.get(config_file.name, stanza_name)
             owner = metadata.get("owner", None)
             app = config_file.service.namespace.app
             if metadata.get("export", None) == "system":
                 sharing = "global"
             else:
@@ -320,15 +322,18 @@
             print(f"Failed hitting:  {resource}  ARGS={final_meta}")
             import traceback
             traceback.print_exc()
             # XXX:  Do better
 
         return (action, res)
 
-    def delete_conf(self, stanza_name, stanza_data, config_file):
+    def delete_conf(self,
+                    stanza_name: str,
+                    stanza_data: ConfType,
+                    config_file):
         res = {}
         if stanza_name in config_file:
             stz = config_file[stanza_name]
             stz_data = stz.content
             res["path"] = stz.path
             try:
                 res["updated"] = stz.state["updated"]
@@ -342,15 +347,15 @@
             config_file.delete(stanza_name)
             res["delta"] = compare_stanzas(data, {}, stanza_name)
             return ("deleted", res)
         else:
             res["delta"] = []
             return ("nochange", res)
 
-    def run(self, args):
+    def run(self, args: Namespace):
         if args.insecure:
             raise NotImplementedError("Need to implement -k feature")
 
         if args.meta:
             self.meta = MetaData()
             for meta_file in args.meta:
                 print(f"Loading metadata from {meta_file}")
```

### Comparing `ksconf-0.10.1/ksconf/commands/snapshot.py` & `ksconf-0.10.2a1/ksconf/commands/snapshot.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/sort.py` & `ksconf-0.10.2a1/ksconf/commands/sort.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/commands/unarchive.py` & `ksconf-0.10.2a1/ksconf/commands/unarchive.py`

 * *Files 10% similar despite different names*

```diff
@@ -8,31 +8,35 @@
 
 """
 
 from __future__ import absolute_import, print_function, unicode_literals
 
 import os
 import re
-from io import StringIO
+from pathlib import Path
 from subprocess import list2cmdline
 
-from ksconf.archive import (extract_archive, gaf_filter_name_like,
-                            gen_arch_file_remapper, sanity_checker)
+from ksconf.app import get_facts_manifest_from_archive
+from ksconf.app.facts import AppFacts
+from ksconf.app.manifest import AppArchiveContentError, AppArchiveError
+from ksconf.archive import extract_archive, gen_arch_file_remapper
 from ksconf.commands import KsconfCmd, dedent
-from ksconf.conf.parser import PARSECONF_LOOSE, ConfParserException, default_encoding, parse_conf
-from ksconf.consts import EXIT_CODE_FAILED_SAFETY_CHECK, EXIT_CODE_GIT_FAILURE, KSCONF_DEBUG
+from ksconf.conf.parser import PARSECONF_LOOSE, ConfParserException, parse_conf
+from ksconf.consts import (EXIT_CODE_BAD_ARCHIVE_FILE, EXIT_CODE_BAD_ARGS,
+                           EXIT_CODE_FAILED_SAFETY_CHECK, EXIT_CODE_GIT_FAILURE,
+                           KSCONF_DEBUG)
 from ksconf.filter import create_filtered_list
-from ksconf.util.compare import _cmp_sets
+from ksconf.util.compare import cmp_sets
 from ksconf.util.completers import DirectoriesCompleter, FilesCompleter
 from ksconf.util.file import dir_exists, file_hash, relwalk
 from ksconf.vc.git import (git_cmd, git_cmd_iterable, git_is_clean,
                            git_is_working_tree, git_ls_files, git_status_ui,
                            git_version)
 
-allowed_extentions = ("*.tgz", "*.tar.gz", "*.spl", "*.zip")
+allowed_extensions = ("*.tgz", "*.tar.gz", "*.spl", "*.zip")
 
 
 # XXX:  Add a git status --ignored --porcelain APPNAME check to list out files/dirs that are excluded...
 
 # XXX:  Update code base to use ksconf.layer, as was done for the 'ksconf combine' command.
 
 
@@ -50,15 +54,15 @@
     """)
     format = "manual"
     maturity = "beta"
 
     def register_args(self, parser):
         parser.add_argument("tarball", metavar="SPL",
                             help="The path to the archive to install."
-                            ).completer = FilesCompleter(allowednames=allowed_extentions)
+                            ).completer = FilesCompleter(allowednames=allowed_extensions)
         parser.add_argument("--dest", metavar="DIR", default=".", help=dedent("""\
             Set the destination path where the archive will be extracted.
             By default, the current directory is used.  Sane values include: etc/apps,
             etc/deployment-apps, and so on.""")
                             ).completer = DirectoriesCompleter()
         parser.add_argument("--app-name", metavar="NAME", default=None, help=dedent("""\
             The app name to use when expanding the archive.
@@ -113,135 +117,134 @@
         parser.add_argument("--git-commit-args", "-G", default=[], action="append",
                             help="Extra arguments to pass to 'git'")
 
     def run(self, args):
         """ Install / upgrade a Splunk app from an archive file """
         # Handle ignored files by preserving them as much as possible.
         # Add --dry-run mode?  j/k - that's what git is for!
-
         DEBUG = KSCONF_DEBUG in os.environ
 
-        if not os.path.isfile(args.tarball):
-            self.stderr.write("No such file or directory {}\n".format(args.tarball))
+        tarball = Path(args.tarball)
+        if not tarball.is_file():
+            self.stderr.write(f"No such file or directory {tarball}\n")
             return EXIT_CODE_FAILED_SAFETY_CHECK
 
-        if not os.path.isdir(args.dest):
-            self.stderr.write("Destination directory does not exist: {}\n".format(args.dest))
+        dest = Path(args.dest)
+        if not dest.is_dir():
+            self.stderr.write(f"Destination directory does not exist: {dest}\n")
             return EXIT_CODE_FAILED_SAFETY_CHECK
 
-        f_hash = file_hash(args.tarball)
-        self.stdout.write("Inspecting archive:               {}\n".format(args.tarball))
+        f_hash = file_hash(tarball)
+        self.stdout.write(f"Inspecting archive:               {tarball}\n")
 
-        # TODO: Grab and share wit ksconf_shared.py in https://github.com/Kintyre/ansible-collection-splunk
         new_app_name = args.app_name
+
+        if new_app_name and "/" in new_app_name:
+            if new_app_name.endswith("/"):
+                new_app_name = new_app_name.rstrip("/")
+            else:
+                self.stderr.write(f"Invalid app name.  Please remove '/' from app name {new_app_name}")
+                return EXIT_CODE_BAD_ARGS
+
         # ARCHIVE PRE-CHECKS:  Archive must contain only one app, no weird paths, ...
-        app_name = set()
-        app_conf = {}
-        files = 0
-        local_files = set()
-        a = extract_archive(args.tarball, extract_filter=gaf_filter_name_like("app.conf"))
-        for gaf in sanity_checker(a):
-            gaf_app, gaf_relpath = gaf.path.split("/", 1)
-            files += 1
-            if gaf.path.endswith("app.conf") and gaf.payload:
-                conffile = StringIO(gaf.payload.decode(default_encoding))
-                conffile.name = os.path.join(args.tarball, gaf.path)
-                app_conf = parse_conf(conffile, profile=PARSECONF_LOOSE)
-                del conffile
-            elif gaf_relpath.startswith("local" + os.path.sep) or \
-                    gaf_relpath.endswith("local.meta"):
-                local_files.add(gaf_relpath)
-            app_name.add(gaf.path.split("/", 1)[0])
-            del gaf_app, gaf_relpath
-        if len(app_name) > 1:
-            self.stderr.write("The 'unarchive' command only supports extracting a single splunk"
-                              " app at a time.\nHowever the archive {} contains {} apps:  {}\n"
-                              "".format(args.tarball, len(app_name), ", ".join(app_name)))
+        try:
+            app_facts, app_manifest = get_facts_manifest_from_archive(
+                tarball, calculate_hash=False, check_paths=True)
+        except AppArchiveError as e:
+            self.stderr.write(f"Failed to extract content from {tarball}\n{e}")
+            return EXIT_CODE_BAD_ARCHIVE_FILE
+        except AppArchiveContentError as e:
+            self.stderr.write(f"The 'unarchive' command does not support the {tarball} archive.\n{e}")
             return EXIT_CODE_FAILED_SAFETY_CHECK
-        else:
-            app_name = app_name.pop()
-        del a
+
+        local_files = set(app_manifest.find_local())
+        app_name = app_facts.name
+
         if local_files:
-            self.stderr.write("Local {} files found in the archive.  ".format(len(local_files)))
+            self.stderr.write(f"Local {len(local_files)} files found in the archive.  ")
             if args.allow_local:
                 self.stderr.write("Keeping these due to the '--allow-local' flag\n")
             else:
                 self.stderr.write("Excluding local files by default.  "
                                   "Use '--allow-local' to override.")
 
         if not new_app_name and True:  # if not --no-app-name-fixes
             if app_name.endswith("-master"):
                 self.stdout.write("Automatically dropping '-master' from the app name.  "
                                   "This is often the result of a github export.\n")
-                # Trick, but it works...
                 new_app_name = app_name[:-7]
             mo = re.search(r"(.*)-\d+\.[\d.-]+$", app_name)
             if mo:
-                self.stdout.write("Automatically removing the version suffix from the app name.  "
-                                  "'{}' will be extracted as '{}'\n".format(app_name, mo.group(1)))
                 new_app_name = mo.group(1)
+                self.stdout.write("Automatically removing the version suffix from the app name.  "
+                                  f"'{app_name}' will be extracted as '{new_app_name}'\n")
 
         app_basename = new_app_name or app_name
-        dest_app = os.path.join(args.dest, app_basename)
-        self.stdout.write("Inspecting destination folder:    {}\n".format(os.path.abspath(dest_app)))
+        dest_app: Path = dest / app_basename
+        self.stdout.write(f"Inspecting destination folder:    {dest_app.absolute()}\n")
 
         # FEEDBACK TO THE USER:   UPGRADE VS INSTALL, GIT?, APP RENAME, ...
         app_name_msg = app_name
 
         git_ver = git_version()
         if git_ver is None:
             vc_msg = "without version control support (git not present)"
             is_git = False
         else:
             vc_msg = "without version control support"
 
-        old_app_conf = {}
+        existing_app = None
 
-        if os.path.isdir(dest_app):
+        if dest_app.is_dir():
             mode = "upgrade"
             if git_ver:
                 is_git = git_is_working_tree(dest_app)
             try:
                 # Ignoring the 'local' entries since distributed apps shouldn't contain local
                 old_app_conf_file = os.path.join(dest_app, args.default_dir, "app.conf")
                 old_app_conf = parse_conf(old_app_conf_file, profile=PARSECONF_LOOSE)
+                existing_app = AppFacts.from_conf(app_basename, old_app_conf)
+                del old_app_conf
             except (ConfParserException, FileNotFoundError):
                 self.stderr.write("Unable to read app.conf from existing install.\n")
                 # Assume upgrade form unknown version
         else:
             mode = "install"
             if git_ver:
                 is_git = git_is_working_tree(args.dest)
         if is_git:
             vc_msg = "with git support"
-        if new_app_name and new_app_name != app_name:
-            app_name_msg = "{} (renamed from {})".format(new_app_name, app_name)
 
-        def show_pkg_info(conf, label):
-            self.stdout.write("{} packaging info:    '{}' by {} (version {})\n".format(
-                label,
-                conf.get("ui", {}).get("label", "Unknown"),
-                conf.get("launcher", {}).get("author", "Unknown"),
-                conf.get("launcher", {}).get("version", "Unknown")))
-
-        if old_app_conf:
-            show_pkg_info(old_app_conf, " Installed app")
-        if app_conf:
-            show_pkg_info(app_conf, "   Tarball app")
+        if new_app_name:
+            if new_app_name == app_name:
+                # No rename detected (user provided 'app_name' matches the default app name)
+                new_app_name = None
+            else:
+                app_name_msg = f"{new_app_name} (renamed from {app_name})"
+
+        def show_pkg_info(facts: AppFacts, label):
+            self.stdout.write(f"{label} packaging info:    "
+                              f"'{facts.label or 'Unknown'}' by "
+                              f"{facts.author or 'Unknown'} "
+                              f"(version {facts.author or 'Unknown'})\n")
+
+        if existing_app:
+            show_pkg_info(existing_app, " Installed app")
+        if app_facts:
+            show_pkg_info(app_facts, "   Tarball app")
 
-        self.stdout.write("About to {} the {} app {}.\n".format(mode, app_name_msg, vc_msg))
+        self.stdout.write(f"About to {mode} the {app_name_msg} app {vc_msg}.\n")
 
         existing_files = set()
         if mode == "upgrade":
             if is_git:
                 existing_files.update(git_ls_files(dest_app))
                 if not existing_files:
                     self.stderr.write("App is in a git repository but no files have been staged "
-                                      "or committed.  Either commit or remove '{}' and try again."
-                                      "\n".format(dest_app))
+                                      f"or committed.  Either commit or remove '{dest_app}' and try again.")
                     return EXIT_CODE_FAILED_SAFETY_CHECK
                 if args.git_sanity_check == "off":
                     self.stdout.write("The 'git status' safety checks have been disabled via CLI"
                                       "argument.  Skipping.\n")
                 else:
                     d = {
                         #        untracked, ignored
@@ -263,18 +266,18 @@
                             git_status_ui(dest_app, "--untracked-files=no")
                         elif args.git_sanity_check == "ignored":
                             git_status_ui(dest_app, "--ignored")
                         else:
                             git_status_ui(dest_app)
                         return EXIT_CODE_FAILED_SAFETY_CHECK
             else:
-                for (root, dirs, filenames) in relwalk(dest_app):
+                for (root, _, filenames) in relwalk(dest_app):
                     for fn in filenames:
                         existing_files.add(os.path.join(root, fn))
-            self.stdout.write("Before upgrade.  App has {} files\n".format(len(existing_files)))
+            self.stdout.write(f"Before upgrade.  App has {len(existing_files)} files\n")
         elif is_git:
             self.stdout.write("Git clean check skipped.  Not needed for a fresh app install.\n")
 
         def fixup_pattern_bw(patterns, prefix=None):
             modified = []
             for pattern in patterns:
                 if pattern.startswith("./"):
@@ -300,144 +303,137 @@
         self.stderr.write("Extraction exclude patterns:  {!r}\n".format(excludes))
         exclude_filter = create_filtered_list("splunk", default=False)
         exclude_filter.feedall(excludes)
 
         # Calculate path rewrite operations
         path_rewrites = []
         files_iter = extract_archive(args.tarball)
-        if True:
-            files_iter = sanity_checker(files_iter)
         if args.default_dir != DEFAULT_DIR:
             rep = r"\1/{}/".format(args.default_dir.strip("/"))
             path_rewrites.append((re.compile(r"^(/?[^/]+)/{}/".format(DEFAULT_DIR)), rep))
             del rep
         if new_app_name:
-            # We do have the "app_name" extracted from our first pass above, but
             regex = re.compile(r'^([^/]+)(?=/)')
             path_rewrites.append((regex, new_app_name))
+            del regex
         if path_rewrites:
             files_iter = gen_arch_file_remapper(files_iter, path_rewrites)
+        del path_rewrites
 
         # Filer out "removed" files; and let us keep some based on a keep-allowlist
         self.stdout.write("Extracting app now...\n")
         for gaf in files_iter:
             if exclude_filter.match(gaf.path):
                 self.stdout.write("Skipping [blocklist] {}\n".format(gaf.path))
                 continue
             if not is_git or args.git_mode in ("nochange", "stage"):
-                self.stdout.write("{0:60s} {2:o} {1:-6d}\n".format(gaf.path, gaf.size, gaf.mode))
+                self.stdout.write(f"{gaf.path:60s} {gaf.mode:o} {gaf.size:-6d}\n")
             installed_files.add(gaf.path.split("/", 1)[1])
             full_path = os.path.join(args.dest, gaf.path)
             dir_exists(os.path.dirname(full_path))
             with open(full_path, "wb") as fp:
                 fp.write(gaf.payload)
             os.chmod(full_path, gaf.mode)
             del fp, full_path
 
-        files_new, files_upd, files_del = _cmp_sets(installed_files, existing_files)
+        files_new, files_upd, files_del = cmp_sets(installed_files, existing_files)
 
         if DEBUG:
             print("New: \n\t{}".format("\n\t".join(sorted(files_new))))
             print("Existing: \n\t{}".format("\n\t".join(sorted(files_upd))))
             print("Removed:  \n\t{}".format("\n\t".join(sorted(files_del))))
 
-        self.stdout.write("Extracted {} files:  {} new, {} existing, and {} removed\n".format(
-            len(installed_files), len(files_new), len(files_upd), len(files_del)))
+        self.stdout.write(f"Extracted {len(installed_files)} files:  "
+                          f"{len(files_new)} new, {len(files_upd)} existing, "
+                          f"and {len(files_del)} removed\n")
 
         # Filer out "removed" files; and let us keep some based on a keep-allowlist:  This should
         # include things like local, ".gitignore", ".gitattributes" and so on
 
         keep_list = [".git*"]
         keep_list.extend(args.keep)
         if not args.allow_local:
             keep_list += ["local/...", "local.meta"]
         keep_list = fixup_pattern_bw(keep_list)
-        self.stderr.write("Keep file patterns:  {!r}\n".format(keep_list))
+        self.stderr.write(f"Keep file patterns:  {keep_list!r}\n")
 
         keep_filter = create_filtered_list("splunk", default=False)
         keep_filter.feedall(keep_list)
 
         files_to_delete = []
         files_to_keep = []
         for fn in files_del:
             if keep_filter.match(fn):
                 # How to handle a keep of "default.d/..." when we DO want to cleanup the default
                 # redirect folder of "default.d/10-upstream"?
                 # This may be an academic question since most apps will continue to send
                 # an ever increasing list of default files (to mask out old/unused ones)
-                self.stdout.write("Keeping {}\n".format(fn))
+                self.stdout.write(f"Keeping {fn}\n")
                 files_to_keep.append(fn)
             else:
                 files_to_delete.append(fn)
         if files_to_keep:
-            self.stdout.write("Keeping {} of {} files marked for deletion due to allow list.\n"
-                              .format(len(files_to_keep), len(files_del)))
+            self.stdout.write(f"Keeping {len(files_to_keep)} of {len(files_del)} "
+                              "files marked for deletion due to allow list.\n")
         git_rm_queue = []
 
         if files_to_delete:
             self.stdout.write("Removing files not present in the upgraded version of the app.\n")
         for fn in files_to_delete:
             path = os.path.join(dest_app, fn)
             if is_git and args.git_mode in ("stage", "commit"):
-                self.stdout.write("git rm -f {}\n".format(path))
+                self.stdout.write(f"git rm -f {path}\n")
                 git_rm_queue.append(fn)
             else:
-                self.stdout.write("rm -f {}\n".format(path))
+                self.stdout.write(f"rm -f {path}\n")
                 os.unlink(path)
 
         if git_rm_queue:
             # Run 'git rm file1 file2 file3 ..." (using an xargs like mechanism)
             git_cmd_iterable(["rm"], git_rm_queue, cwd=dest_app)
         del git_rm_queue
 
         if is_git:
             if args.git_mode in ("stage", "commit"):
-                git_cmd(["add", "--all", os.path.basename(dest_app)], cwd=os.path.dirname(dest_app))
+                git_cmd(["add", "--all", dest_app.name], cwd=dest_app.parent)
                 # self.stdout.write("git add {}\n".format(os.path.basename(dest_app)))
             '''
             else:
                 self.stdout.write("git add {}\n".format(dest_app))
             '''
 
             # Is there anything to stage/commit?
-            if git_is_clean(os.path.dirname(dest_app), check_untracked=False):
-                self.stderr.write("No changes detected.  Nothing to {}\n".format(args.git_mode))
+            if git_is_clean(dest_app.parent, check_untracked=False):
+                self.stderr.write(f"No changes detected.  Nothing to {args.git_mode}\n")
                 return
 
-            git_commit_app_name = app_conf.get("ui", {}).get("label", os.path.basename(dest_app))
-            git_commit_new_version = app_conf.get("launcher", {}).get("version", None)
+            git_commit_app_name = app_facts.label or dest_app.name
             if mode == "install":
-                git_commit_message = "Install {}".format(git_commit_app_name)
-
-                if git_commit_new_version:
-                    git_commit_message += " version {}".format(git_commit_new_version)
+                git_commit_message = f"Install {git_commit_app_name}"
+                if app_facts.version:
+                    git_commit_message += f" version {app_facts.version}"
             else:
                 # Todo:  Specify Upgrade/Downgrade/Refresh
-                git_commit_message = "Upgrade {}".format(
-                    git_commit_app_name)
-                git_commit_old_version = old_app_conf.get("launcher", {}).get("version", None)
-                if git_commit_old_version and git_commit_new_version:
-                    git_commit_message += " version {} (was {})".format(git_commit_new_version,
-                                                                        git_commit_old_version)
-                elif git_commit_new_version:
-                    git_commit_message += " to version {}".format(git_commit_new_version)
+                git_commit_message = f"Upgrade {git_commit_app_name}"
+                if existing_app.version and app_facts.version:
+                    git_commit_message += f" version {app_facts.version} (was {existing_app.version})"
+                elif app_facts.version:
+                    git_commit_message += f" to version {app_facts.version}"
             # Could possibly include some CLI arg details, like what file patterns were excluded
-            git_commit_message += "\n\nSHA256 {} {}\n\nSplunk-App-managed-by: ksconf" \
-                .format(f_hash, os.path.basename(args.tarball))
-            git_commit_cmd = ["commit", os.path.basename(dest_app), "-m", git_commit_message]
+            git_commit_message += f"\n\nSHA256 {f_hash} {tarball.name}\n\nSplunk-App-managed-by: ksconf"
+            git_commit_cmd = ["commit", dest_app.name, "-m", git_commit_message]
 
             if not args.no_edit:
                 git_commit_cmd.append("--edit")
 
             git_commit_cmd.extend(args.git_commit_args)
 
             if args.git_mode == "commit":
                 capture_std = True if args.no_edit else False
-                proc = git_cmd(git_commit_cmd, cwd=os.path.dirname(dest_app),
-                               capture_std=capture_std)
+                proc = git_cmd(git_commit_cmd, cwd=dest_app.parent, capture_std=capture_std)
                 if proc.returncode == 0:
                     self.stderr.write(dedent("""\
                     Your changes have been committed.  Please review before pushing.  If you
                     find any issues, here are some possible solutions:
 
 
                     To fix issues in the last commit, edit and add the files to be fixed, then run:
@@ -451,15 +447,15 @@
                     To roll back the last commit and REVERT the app upgrade, run:
 
                         git reset --hard HEAD^1
 
                     NOTE:  Make sure you have *no* other uncommitted changes before running 'reset'.
                     """))
                 else:
-                    self.stderr.write("Git commit failed.  Return code {}.  Git args:  git {}\n"
-                                      .format(proc.returncode, list2cmdline(git_commit_cmd)))
+                    self.stderr.write(f"Git commit failed.  Return code {proc.returncode}.  "
+                                      f"Git args:  git {list2cmdline(git_commit_cmd)}\n")
                     return EXIT_CODE_GIT_FAILURE
             elif args.git_mode == "stage":
                 self.stdout.write("To commit later, use the following\n")
-                self.stdout.write(
-                    "\tgit {}\n".format(list2cmdline(git_commit_cmd).replace("\n", "\\n")))
+                self.stdout.write("\tgit {}\n".format(
+                    list2cmdline(git_commit_cmd).replace("\n", "\\n")))
             # When in 'nochange' mode, no point in even noting these options to the user.
```

### Comparing `ksconf-0.10.1/ksconf/commands/xmlformat.py` & `ksconf-0.10.2a1/ksconf/commands/xmlformat.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/conf/delta.py` & `ksconf-0.10.2a1/ksconf/conf/delta.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from enum import Enum
 from io import open
 from os import PathLike
 from typing import List, NamedTuple, Sequence, TextIO, Union
 
 from ksconf.conf.parser import GLOBAL_STANZA, ConfType, StanzaType, _format_stanza, default_encoding
 from ksconf.consts import EXIT_CODE_DIFF_CHANGE, EXIT_CODE_DIFF_EQUAL, EXIT_CODE_DIFF_NO_COMMON
-from ksconf.util.compare import _cmp_sets
+from ksconf.util.compare import cmp_sets
 from ksconf.util.terminal import ANSI_BOLD, ANSI_GREEN, ANSI_RED, ANSI_RESET, ANSI_YELLOW, TermColor
 
 ####################################################################################################
 # DiffVerb logic
 
 
 class DiffVerb(Enum):
@@ -34,23 +34,14 @@
 # Legacy names
 DIFF_OP_INSERT = DiffVerb.INSERT
 DIFF_OP_DELETE = DiffVerb.DELETE
 DIFF_OP_REPLACE = DiffVerb.REPLACE
 DIFF_OP_EQUAL = DiffVerb.EQUAL
 
 
-'''
-from typing import NamedTuple
-DiffOp = NamedTuple("DiffOp", (["tag", DiffVerb], ["location", Union[DiffGlobal, DiffStanza, DiffStzKey]], ["a", Union[ConfType, StanzaType, str]], ["b", Union[ConfType, StanzaType, str]]))
-DiffGlobal = NamedTuple("DiffGlobal", (["type", str],))
-DiffStanza = NamedTuple("DiffStanza", (["type", str], ["stanza", str]))
-DiffStzKey = NamedTuple("DiffStzKey", (["type", str], ["stanza", str], ["key", str]))
-'''
-
-
 class DiffLevel(Enum):
     GLOBAL = "global"
     STANZA = "stanza"
     KEY = "key"
 
 
 class DiffGlobal(NamedTuple):
@@ -121,15 +112,15 @@
     else:
         return list(_compare_stanzas(a, b, stanza_name, replace_level))
 
 
 def _compare_stanzas(a: StanzaType, b: StanzaType,
                      stanza_name: str,
                      replace_level: DiffLevel) -> List[DiffOp]:
-    kv_a, kv_common, kv_b = _cmp_sets(list(a.keys()), list(b.keys()))
+    kv_a, kv_common, kv_b = cmp_sets(list(a.keys()), list(b.keys()))
 
     if replace_level in (DiffLevel.GLOBAL, DiffLevel.STANZA) and not kv_common:
         # No keys in common, just swap
         yield DiffOp(DiffVerb.REPLACE, DiffStanza(DiffLevel.STANZA, stanza_name), a, b)
         return
 
     # Level 2 - Key comparisons
@@ -170,15 +161,15 @@
     :rtype: [DiffOp]
 
     .. note:: The :py:class:`DiffOp` output idea was borrowed from
               :class:`SequenceMatcher` class in the :mod:`difflib`
               in the standard Python module.
 
     This function returns a sequence of 5 element tuples describing the
-    transformation based on the detail level specified in `replace_level`.
+    transformation based on the detail level specified in ``replace_level``.
 
     Each :py:class:`DiffOp` (named tuple) takes the form:
 
         (tag, location, a, b)
 
     *tag:*
 
@@ -198,15 +189,15 @@
     ====================== ========== ==============================================================
     `("global")`           DiffGlobal Global file level context (e.g., both files are the same)
     `("stanza", stanza)`   DiffStanza Stanzas are the same, or completely different (no shared keys)
     `("key", stanza, key)` DiffStzKey Key level change
     ====================== ========== ==============================================================
 
     .. versionchanged:: v0.8.8
-        The ``preserve_empty`` argument was origionally introduced to preserve backwards
+        The ``preserve_empty`` argument was originally introduced to preserve backwards
         compatibility, but it ended up introducing new bugs.
         Additionally, no use cases were found where better to automatically discarding empty stanzas.
 
     .. versionchanged:: v0.8.8
         The ``allow_level0`` argument was replaced with ``replace_level``.
         Instead of using ``allow_level0=False`` use ``replace_level="stanza"``.
         At the same time a new feature was added to support ``replace_level="key"``.
@@ -223,15 +214,15 @@
             raise TypeError(f"Invalid value '{replace_level}' given for "
                             f"replace_level.  Choose 'global', 'stanza', or 'key'")
 
     delta = []
 
     # Level 0 - Compare entire file
     if replace_level == DiffLevel.GLOBAL:
-        stanza_a, stanza_common, stanza_b = _cmp_sets(list(a.keys()), list(b.keys()))
+        stanza_a, stanza_common, stanza_b = cmp_sets(list(a.keys()), list(b.keys()))
         if a == b:
             return [DiffOp(DiffVerb.EQUAL, DiffGlobal(DiffLevel.GLOBAL), a, b)]
         if not stanza_common:
             # Q:  Does this specific output make the consumer's job more difficult?
             # Nothing in common between these two files
             # Note:  Stanza renames are not detected and are out of scope.
             return [DiffOp(DiffVerb.REPLACE, DiffGlobal(DiffLevel.GLOBAL), a, b)]
@@ -248,15 +239,15 @@
     all_stanzas = sorted(all_stanzas)
     for stanza in all_stanzas:
         delta.extend(compare_stanzas(a.get(stanza), b.get(stanza), stanza, replace_level))
     return delta
 
 
 def summarize_cfg_diffs(delta: List[DiffOp], stream: TextIO):
-    """ Summarize a delta into a human-readable format.   The input `delta` is in the format
+    """ Summarize a delta into a human-readable format.   The input ``delta`` is in the format
     produced by the compare_cfgs() function.
     """
     stanza_stats = defaultdict(set)
     key_stats = defaultdict(lambda: defaultdict(lambda: defaultdict(set)))
     c = Counter()
     for op in delta:
         c[op.tag] += 1
```

### Comparing `ksconf-0.10.1/ksconf/conf/merge.py` & `ksconf-0.10.2a1/ksconf/conf/merge.py`

 * *Files 1% similar despite different names*

```diff
@@ -42,15 +42,15 @@
             base[section].update(items)
         else:
             # TODO:  Support other magic here too..., though with no parent info
             base[section] = items
     # Nothing to return, base is updated in-place
 
 
-def merge_conf_dicts(*dicts):
+def merge_conf_dicts(*dicts: ConfType) -> ConfType:
     result = {}
     for d in dicts:
         d = deepcopy(d)
         if not result:
             result = d
         else:
             # Merge each subsequent layer on one at a time
```

### Comparing `ksconf-0.10.1/ksconf/conf/meta.py` & `ksconf-0.10.2a1/ksconf/conf/meta.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/conf/parser.py` & `ksconf-0.10.2a1/ksconf/conf/parser.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/consts.py` & `ksconf-0.10.2a1/ksconf/consts.py`

 * *Files 16% similar despite different names*

```diff
@@ -10,14 +10,24 @@
     UPDATE = "updated"
     NOCHANGE = "unchanged"
 
     def __str__(self):
         return self.value
 
 
+class _UNSET:
+    pass
+
+
+UNSET = _UNSET()
+
+
+MANIFEST_HASH = "sha256"
+
+
 # Legacy names
 SMART_CREATE = SmartEnum.CREATE
 SMART_UPDATE = SmartEnum.UPDATE
 SMART_NOCHANGE = SmartEnum.NOCHANGE
 
 
 # EXIT_CODE_* constants:  Use consistent exit codes for scriptability
@@ -41,14 +51,15 @@
 EXIT_CODE_FORMAT_APPLIED = 8
 EXIT_CODE_SORT_APPLIED = 9
 
 EXIT_CODE_CLI_ARG_DEPRECATED = 10
 
 # Errors caused by users
 EXIT_CODE_BAD_CONF_FILE = 20
+EXIT_CODE_BAD_ARCHIVE_FILE = 21
 EXIT_CODE_FAILED_SAFETY_CHECK = 22
 EXIT_CODE_COMBINE_MARKER_MISSING = 30
 
 # Errors caused by GIT interactions
 EXIT_CODE_GIT_FAILURE = 40
 
 # Retry or temporary failure
```

### Comparing `ksconf-0.10.1/ksconf/filter.py` & `ksconf-0.10.2a1/ksconf/filter.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/layer.py` & `ksconf-0.10.2a1/ksconf/layer.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,23 +1,18 @@
 from __future__ import annotations
 
 import os
 import re
 from collections import defaultdict
 from fnmatch import fnmatch
+from os import PathLike
 from typing import Type
 
 from ksconf.util.file import relwalk
 
-try:
-    # PY3 with no-op fallback for older versions
-    from os import PathLike
-except ImportError:
-    PathLike = object
-
 """
 
 LayerRootBase has one or more 'Layer', each layer has one or more 'File's.
 
 
 LayerRoot methods:
```

### Comparing `ksconf-0.10.1/ksconf/package.py` & `ksconf-0.10.2a1/ksconf/package.py`

 * *Files 1% similar despite different names*

```diff
@@ -73,15 +73,15 @@
         :rtype: str
         """
         return self._var_magic.expand(value)
 
     def expand_new_only(self, value):
         """ Expand a variable but return False if no substitution occurred
 
-        :param str value:  String that main contain ``{{variable}}`` substitution.
+        :param str value:  String that may contain ``{{variable}}`` substitution.
         :return:  Expanded value if variables were expanded, else False
         :rtype: str
         """
         new_value = self._var_magic.expand(value)
         return new_value if new_value != value else False
 
     def combine(self, src, filters, layer_method="dir.d", allow_symlink=False):
@@ -227,15 +227,15 @@
         with tarfile.open(filename, mode="w:gz") as spl:
             spl.add(self.app_dir, arcname=self.app_name)
         return filename
 
     def __enter__(self):
         self.build_dir = tempfile.mkdtemp("-ksconf-package-build")
         if self.app_name == "." or "{{" in self.app_name:
-            # Use a placehold app name, specifically as "." causes build_dir == app_dir
+            # Use a placeholder app name, otherwise build_dir == app_dir
             self.app_dir = os.path.join(self.build_dir, "app")
         else:
             self.app_dir = os.path.join(self.build_dir, self.app_name)
         self._var_magic = AppVarMagic(self.src_path, self.app_dir)
         return self
 
     def __exit__(self, exc_type, exc_val, exc_tb):
```

### Comparing `ksconf-0.10.1/ksconf/setup_entrypoints.py` & `ksconf-0.10.2a1/ksconf/setup_entrypoints.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/util/__init__.py` & `ksconf-0.10.2a1/ksconf/compat.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,43 +1,29 @@
-from __future__ import unicode_literals
-
-from functools import lru_cache
-
-from ksconf.consts import KSCONF_DEBUG
-
-
-def _xargs(iterable, cmd_len=1024):
-    fn_len = 0
-    buf = []
-    iterable = list(iterable)
-    while iterable:
-        s = iterable.pop(0)
-        l = len(s) + 1
-        if fn_len + l >= cmd_len:
-            yield buf
-            buf = []
-            fn_len = 0
-        buf.append(s)
-        fn_len += l
-    if buf:
-        yield buf
-
-
-# the LRU functionality is not really needed
-memoize = lru_cache(maxsize=None)
-
-
-def debug_traceback():  # pragma: no cover
-    """ If the 'KSCONF_DEBUG' environmental variable is set, then show a stack trace. """
-    level = 10
-    from os import environ
-    if KSCONF_DEBUG in environ:
-        # TODO:  Pop one off the top of the stack to hide THIS function
-        import traceback
-        traceback.print_exc(level)
+"""
+Silly simple Python version compatibility items
+"""
+
+import sys
+
+# Since 'list' in Python 3.7 doesn't support __class_getitem__ (See PEP 560)
+# We could just always import from typing, but that appears to cause some issues
+# with type hinting, and this appears to work correctly.
+if sys.version_info < (3, 8):
+    from typing import List, Tuple
+else:
+    List = list
+    Tuple = tuple
+
+
+try:
+    # Python 3.9 and later
+    from functools import cache
+except ImportError:
+    from functools import lru_cache
+    cache = lru_cache(maxsize=None)
 
 
 def handle_py3_kw_only_args(kw, *default_args):
     """ Fake support for Python 3.8+ style keyword-only style arguments, or ``*`` arg syntax.
 
     Example Python 3.8+ syntax:
 
@@ -71,7 +57,17 @@
     if kw:
         import inspect
         caller = inspect.currentframe().f_back.f_code.co_name
         # Should all unexpected args be reported?  feels like this good enough
         raise TypeError("{} got an unexpected keyword argument '{}'"
                         .format(caller, list(kw)[0]))
     return out
+
+
+del sys
+
+__all__ = [
+    "List",
+    "Tuple",
+    "cache",
+    "handle_py3_kw_only_args",
+]
```

### Comparing `ksconf-0.10.1/ksconf/util/compare.py` & `ksconf-0.10.2a1/ksconf/util/compare.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/util/completers.py` & `ksconf-0.10.2a1/ksconf/util/completers.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/util/file.py` & `ksconf-0.10.2a1/ksconf/util/file.py`

 * *Files 1% similar despite different names*

```diff
@@ -106,14 +106,15 @@
     return pattern
 
 
 def relwalk(top, topdown=True, onerror=None, followlinks=False):
     """ Relative path walker
     Like os.walk() except that it doesn't include the "top" prefix in the resulting 'dirpath'.
     """
+    top = os.fspath(top)
     if not top.endswith(os.path.sep):
         top += os.path.sep
     prefix = len(top)
     for (dirpath, dirnames, filenames) in os.walk(top, topdown, onerror, followlinks):
         dirpath = dirpath[prefix:]
         yield (dirpath, dirnames, filenames)
```

### Comparing `ksconf-0.10.1/ksconf/util/rest.py` & `ksconf-0.10.2a1/ksconf/util/rest.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/util/terminal.py` & `ksconf-0.10.2a1/ksconf/util/terminal.py`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/ksconf/vc/git.py` & `ksconf-0.10.2a1/ksconf/vc/git.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,19 +1,15 @@
 from __future__ import absolute_import, unicode_literals
 
 from collections import Counter, namedtuple
+from shutil import which
 from subprocess import PIPE, Popen, call, list2cmdline
 
-from ksconf.util import _xargs, memoize
-
-try:
-    from shutil import which
-except ImportError:
-    from backports.shutil_which import which
-
+from ksconf.compat import cache
+from ksconf.util import _xargs
 
 GIT_BIN = "git"
 GitCmdOutput = namedtuple("GitCmdOutput", ["cmd", "returncode", "stdout", "stderr", "lines"])
 
 unitesting = False
 
 
@@ -41,16 +37,16 @@
     for chunk in _xargs(iterable, cmd_len - base_len):
         p = git_cmd(args + chunk, cwd=cwd)
         if p.returncode != 0:  # pragma: no cover
             raise RuntimeError("git exited with code {}.  Command: {}".format(
                 p.returncode, list2cmdline(args + chunk)))
 
 
-# Shave time off of unit testing; or anyting that does CLI calls from the API
-@memoize
+# Shave time off of unit testing; or anything that does CLI calls from the API
+@cache
 def git_version():
     git_path = which(GIT_BIN)
     if not git_path:
         return None
     try:
         cmd = git_cmd(["--version"])
     except GitNotAvailable:
```

### Comparing `ksconf-0.10.1/ksconf/xmlformat.py` & `ksconf-0.10.2a1/ksconf/xmlformat.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
     # Lazy loaded etree; This prevents crashing at module import if not installed
     g = globals()
     from lxml import etree
     g["etree"] = etree
 
 
 class FileReadlinesCache:
-    """ Silly class as a hacky workaround for CDATA detection... """
+    """ Silly workaround for CDATA detection... """
 
     def __init__(self):
         self.cache = {}
 
     @staticmethod
     def convert_filename(filename):
         if filename.startswith("file:"):
```

### Comparing `ksconf-0.10.1/ksconf.egg-info/PKG-INFO` & `ksconf-0.10.2a1/ksconf.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ksconf
-Version: 0.10.1
+Version: 0.10.2a1
 Summary: KSCONF: Ksconf Splunk Configuration Tool
 Home-page: https://github.com/Kintyre/ksconf
 Author: Lowell Alleman
 Author-email: lowell@kintyre.co
 License: Apache Software License
 Project-URL: Documentation, https://ksconf.readthedocs.io/
 Project-URL: Splunk app, https://splunkbase.splunk.com/app/4383/
```

### Comparing `ksconf-0.10.1/ksconf.egg-info/SOURCES.txt` & `ksconf-0.10.2a1/ksconf.egg-info/SOURCES.txt`

 * *Files 15% similar despite different names*

```diff
@@ -4,27 +4,32 @@
 setup.py
 ksconf/__init__.py
 ksconf/__main__.py
 ksconf/_version.py
 ksconf/archive.py
 ksconf/cli.py
 ksconf/combine.py
+ksconf/compat.py
 ksconf/consts.py
 ksconf/filter.py
 ksconf/layer.py
 ksconf/package.py
 ksconf/setup_entrypoints.py
 ksconf/xmlformat.py
 ksconf.egg-info/PKG-INFO
 ksconf.egg-info/SOURCES.txt
 ksconf.egg-info/dependency_links.txt
 ksconf.egg-info/entry_points.txt
 ksconf.egg-info/requires.txt
 ksconf.egg-info/top_level.txt
 ksconf.egg-info/zip-safe
+ksconf/app/__init__.py
+ksconf/app/deploy.py
+ksconf/app/facts.py
+ksconf/app/manifest.py
 ksconf/builder/__init__.py
 ksconf/builder/cache.py
 ksconf/builder/core.py
 ksconf/builder/steps.py
 ksconf/commands/__init__.py
 ksconf/commands/check.py
 ksconf/commands/combine.py
```

### Comparing `ksconf-0.10.1/ksconf.egg-info/entry_points.txt` & `ksconf-0.10.2a1/ksconf.egg-info/entry_points.txt`

 * *Files identical despite different names*

### Comparing `ksconf-0.10.1/setup.py` & `ksconf-0.10.2a1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -160,14 +160,15 @@
       url="https://github.com/Kintyre/ksconf",
       project_urls={
           "Documentation": "https://ksconf.readthedocs.io/",
           "Splunk app": "https://splunkbase.splunk.com/app/4383/",
       },
       packages=[
           "ksconf",
+          "ksconf.app",
           "ksconf.builder",
           "ksconf.commands",
           "ksconf.conf",
           "ksconf.util",
           "ksconf.vc",
           "ksconf.ext",    # Third-party modules shipping with ksconf
       ],
```

