# Comparing `tmp/plone.app.standardtiles-3.1.0.tar.gz` & `tmp/plone.app.standardtiles-3.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "plone.app.standardtiles-3.1.0.tar", last modified: Thu May  4 10:08:12 2023, max compression
+gzip compressed data, was "plone.app.standardtiles-3.1.1.tar", last modified: Sat May 13 13:33:39 2023, max compression
```

## Comparing `plone.app.standardtiles-3.1.0.tar` & `plone.app.standardtiles-3.1.1.tar`

### file list

```diff
@@ -1,102 +1,102 @@
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.817982 plone.app.standardtiles-3.1.0/
--rw-r--r--   0 peterm     (501) staff       (20)    10911 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/CHANGES.rst
--rw-r--r--   0 peterm     (501) staff       (20)    12282 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/LICENSE.GPL
--rw-r--r--   0 peterm     (501) staff       (20)      750 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/LICENSE.txt
--rw-r--r--   0 peterm     (501) staff       (20)      178 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/MANIFEST.in
--rw-r--r--   0 peterm     (501) staff       (20)    13078 2023-05-04 10:08:12.818070 plone.app.standardtiles-3.1.0/PKG-INFO
--rw-r--r--   0 peterm     (501) staff       (20)     1061 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/README.rst
--rw-r--r--   0 peterm     (501) staff       (20)      289 2023-05-04 10:08:12.818306 plone.app.standardtiles-3.1.0/setup.cfg
--rw-r--r--   0 peterm     (501) staff       (20)     1992 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/setup.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.806775 plone.app.standardtiles-3.1.0/src/
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.808343 plone.app.standardtiles-3.1.0/src/plone/
--rw-r--r--   0 peterm     (501) staff       (20)       56 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/__init__.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.809442 plone.app.standardtiles-3.1.0/src/plone/app/
--rw-r--r--   0 peterm     (501) staff       (20)       56 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/__init__.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.812868 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/
--rw-r--r--   0 peterm     (501) staff       (20)      122 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/__init__.py
--rw-r--r--   0 peterm     (501) staff       (20)     3763 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/attachment.py
--rw-r--r--   0 peterm     (501) staff       (20)    11182 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/common.py
--rw-r--r--   0 peterm     (501) staff       (20)     4184 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/configure.zcml
--rw-r--r--   0 peterm     (501) staff       (20)     5249 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/content.zcml
--rw-r--r--   0 peterm     (501) staff       (20)    10594 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/contentlisting.py
--rw-r--r--   0 peterm     (501) staff       (20)     2330 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/discussion.py
--rw-r--r--   0 peterm     (501) staff       (20)      739 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/embed.py
--rw-r--r--   0 peterm     (501) staff       (20)     8462 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/existingcontent.py
--rw-r--r--   0 peterm     (501) staff       (20)     5774 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/field.py
--rw-r--r--   0 peterm     (501) staff       (20)     2182 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/head.py
--rw-r--r--   0 peterm     (501) staff       (20)     1909 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/head.zcml
--rw-r--r--   0 peterm     (501) staff       (20)     1425 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/html.py
--rw-r--r--   0 peterm     (501) staff       (20)      587 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/interfaces.py
--rw-r--r--   0 peterm     (501) staff       (20)     4359 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/layout.zcml
--rw-r--r--   0 peterm     (501) staff       (20)     1002 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/linkintegrity.py
--rw-r--r--   0 peterm     (501) staff       (20)     1688 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/media.zcml
--rw-r--r--   0 peterm     (501) staff       (20)     1361 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/metadata.py
--rw-r--r--   0 peterm     (501) staff       (20)    11827 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/navigation.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.814036 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/
--rw-r--r--   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/__init__.py
--rw-r--r--   0 peterm     (501) staff       (20)     3940 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/add.py
--rw-r--r--   0 peterm     (501) staff       (20)     1968 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/assignment.py
--rw-r--r--   0 peterm     (501) staff       (20)     2563 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/configure.zcml
--rw-r--r--   0 peterm     (501) staff       (20)      317 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/delete.py
--rw-r--r--   0 peterm     (501) staff       (20)     1185 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/edit.py
--rw-r--r--   0 peterm     (501) staff       (20)     2298 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/portlet.py
--rw-r--r--   0 peterm     (501) staff       (20)     1799 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/portletmanager.py
--rw-r--r--   0 peterm     (501) staff       (20)     1970 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/utils.py
--rw-r--r--   0 peterm     (501) staff       (20)     1720 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/vocabularies.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.807193 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.814388 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/default/
--rw-r--r--   0 peterm     (501) staff       (20)      184 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/default/metadata.xml
--rw-r--r--   0 peterm     (501) staff       (20)      207 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/default/portlets.xml
--rw-r--r--   0 peterm     (501) staff       (20)     4557 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/default/registry.xml
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.814626 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/uninstall/
--rw-r--r--   0 peterm     (501) staff       (20)      239 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/uninstall/portlets..xml
--rw-r--r--   0 peterm     (501) staff       (20)      146 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/uninstall/registry.xml
--rw-r--r--   0 peterm     (501) staff       (20)     1382 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/rawembed.py
--rw-r--r--   0 peterm     (501) staff       (20)     8427 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/rss.py
--rw-r--r--   0 peterm     (501) staff       (20)      780 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/setuphandlers.py
--rw-r--r--   0 peterm     (501) staff       (20)     1000 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/sitemap.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.816616 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/
--rw-r--r--   0 peterm     (501) staff       (20)     1761 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/attachment_listing.pt
--rw-r--r--   0 peterm     (501) staff       (20)     2251 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/configlets.pt
--rw-r--r--   0 peterm     (501) staff       (20)      728 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/contentlisting_view.pt
--rw-r--r--   0 peterm     (501) staff       (20)      457 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/description.pt
--rw-r--r--   0 peterm     (501) staff       (20)     3905 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/existingcontent_view.pt
--rw-r--r--   0 peterm     (501) staff       (20)      762 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/image.pt
--rw-r--r--   0 peterm     (501) staff       (20)     3686 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/listing_view.pt
--rw-r--r--   0 peterm     (501) staff       (20)     5767 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/login.pt
--rw-r--r--   0 peterm     (501) staff       (20)     1477 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/namedimage.pt
--rw-r--r--   0 peterm     (501) staff       (20)     1501 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigation.pt
--rw-r--r--   0 peterm     (501) staff       (20)     2143 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigation_recurse.pt
--rw-r--r--   0 peterm     (501) staff       (20)      681 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigationlink.pt
--rw-r--r--   0 peterm     (501) staff       (20)      767 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/rawembed.pt
--rw-r--r--   0 peterm     (501) staff       (20)     1689 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/rss.pt
--rw-r--r--   0 peterm     (501) staff       (20)     5453 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/summary_view.pt
--rw-r--r--   0 peterm     (501) staff       (20)     4940 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/tabular_view.pt
--rw-r--r--   0 peterm     (501) staff       (20)      368 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/title.pt
--rw-r--r--   0 peterm     (501) staff       (20)     9746 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/testing.py
--rw-r--r--   0 peterm     (501) staff       (20)      698 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/testing.zcml
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.817872 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/
--rw-r--r--   0 peterm     (501) staff       (20)     2921 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/RSS.xml
--rw-r--r--   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/__init__.py
--rw-r--r--   0 peterm     (501) staff       (20)      746 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/custom_existingcontent_layout.pt
--rw-r--r--   0 peterm     (501) staff       (20)      969 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/funky_display.pt
--rw-r--r--   0 peterm     (501) staff       (20)     7293 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_content.py
--rw-r--r--   0 peterm     (501) staff       (20)    14645 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_existing_content.py
--rw-r--r--   0 peterm     (501) staff       (20)    10897 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_field.py
--rw-r--r--   0 peterm     (501) staff       (20)     6241 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_head.py
--rw-r--r--   0 peterm     (501) staff       (20)    15107 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_layout.py
--rw-r--r--   0 peterm     (501) staff       (20)     7409 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_media.py
--rw-r--r--   0 peterm     (501) staff       (20)     1647 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_setup.py
--rw-r--r--   0 peterm     (501) staff       (20)      272 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/upgrades.py
--rw-r--r--   0 peterm     (501) staff       (20)      746 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/upgrades.zcml
--rw-r--r--   0 peterm     (501) staff       (20)     1854 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/utils.py
--rw-r--r--   0 peterm     (501) staff       (20)     2488 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/viewletmanager.py
-drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-04 10:08:12.809320 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/
--rw-r--r--   0 peterm     (501) staff       (20)    13078 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/PKG-INFO
--rw-r--r--   0 peterm     (501) staff       (20)     3964 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/SOURCES.txt
--rw-r--r--   0 peterm     (501) staff       (20)        1 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/dependency_links.txt
--rw-r--r--   0 peterm     (501) staff       (20)       40 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/entry_points.txt
--rw-r--r--   0 peterm     (501) staff       (20)       16 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/namespace_packages.txt
--rw-r--r--   0 peterm     (501) staff       (20)        1 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/not-zip-safe
--rw-r--r--   0 peterm     (501) staff       (20)      257 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/requires.txt
--rw-r--r--   0 peterm     (501) staff       (20)        6 2023-05-04 10:08:12.000000 plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/top_level.txt
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.926773 plone.app.standardtiles-3.1.1/
+-rw-r--r--   0 peterm     (501) staff       (20)    11029 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/CHANGES.rst
+-rw-r--r--   0 peterm     (501) staff       (20)    12282 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/LICENSE.GPL
+-rw-r--r--   0 peterm     (501) staff       (20)      750 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/LICENSE.txt
+-rw-r--r--   0 peterm     (501) staff       (20)    13196 2023-05-13 13:33:39.926446 plone.app.standardtiles-3.1.1/PKG-INFO
+-rw-r--r--   0 peterm     (501) staff       (20)     1061 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/README.rst
+-rw-r--r--   0 peterm     (501) staff       (20)     2858 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/pyproject.toml
+-rw-r--r--   0 peterm     (501) staff       (20)       38 2023-05-13 13:33:39.926844 plone.app.standardtiles-3.1.1/setup.cfg
+-rw-r--r--   0 peterm     (501) staff       (20)     1992 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/setup.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.896553 plone.app.standardtiles-3.1.1/src/
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.899836 plone.app.standardtiles-3.1.1/src/plone/
+-rw-r--r--   0 peterm     (501) staff       (20)       56 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/__init__.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.902686 plone.app.standardtiles-3.1.1/src/plone/app/
+-rw-r--r--   0 peterm     (501) staff       (20)       56 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/__init__.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.911808 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/
+-rw-r--r--   0 peterm     (501) staff       (20)      122 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/__init__.py
+-rw-r--r--   0 peterm     (501) staff       (20)     3763 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/attachment.py
+-rw-r--r--   0 peterm     (501) staff       (20)    11182 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/common.py
+-rw-r--r--   0 peterm     (501) staff       (20)     4184 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/configure.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)     5249 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/content.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)    10594 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/contentlisting.py
+-rw-r--r--   0 peterm     (501) staff       (20)     2330 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/discussion.py
+-rw-r--r--   0 peterm     (501) staff       (20)      739 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/embed.py
+-rw-r--r--   0 peterm     (501) staff       (20)     8603 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/existingcontent.py
+-rw-r--r--   0 peterm     (501) staff       (20)     5775 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/field.py
+-rw-r--r--   0 peterm     (501) staff       (20)     2182 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/head.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1909 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/head.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)     1425 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/html.py
+-rw-r--r--   0 peterm     (501) staff       (20)      587 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/interfaces.py
+-rw-r--r--   0 peterm     (501) staff       (20)     4359 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/layout.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)      981 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/linkintegrity.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1688 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/media.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)     1361 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/metadata.py
+-rw-r--r--   0 peterm     (501) staff       (20)    11827 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/navigation.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.914939 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/
+-rw-r--r--   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/__init__.py
+-rw-r--r--   0 peterm     (501) staff       (20)     3940 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/add.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1968 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/assignment.py
+-rw-r--r--   0 peterm     (501) staff       (20)     2563 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/configure.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)      317 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/delete.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1151 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/edit.py
+-rw-r--r--   0 peterm     (501) staff       (20)     2298 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/portlet.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1799 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/portletmanager.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1970 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/utils.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1720 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/vocabularies.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.897381 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.916026 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/default/
+-rw-r--r--   0 peterm     (501) staff       (20)      184 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/default/metadata.xml
+-rw-r--r--   0 peterm     (501) staff       (20)      207 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/default/portlets.xml
+-rw-r--r--   0 peterm     (501) staff       (20)     4557 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/default/registry.xml
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.916651 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/uninstall/
+-rw-r--r--   0 peterm     (501) staff       (20)      239 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/uninstall/portlets..xml
+-rw-r--r--   0 peterm     (501) staff       (20)      146 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/uninstall/registry.xml
+-rw-r--r--   0 peterm     (501) staff       (20)     1382 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/rawembed.py
+-rw-r--r--   0 peterm     (501) staff       (20)     8427 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/rss.py
+-rw-r--r--   0 peterm     (501) staff       (20)      780 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/setuphandlers.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1000 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/sitemap.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.922479 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/
+-rw-r--r--   0 peterm     (501) staff       (20)     1914 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/attachment_listing.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     2538 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/configlets.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      744 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/contentlisting_view.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      463 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/description.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     4337 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/existingcontent_view.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      771 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/image.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     3944 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/listing_view.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     6694 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/login.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     1254 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/namedimage.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     1675 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigation.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     2369 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigation_recurse.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      764 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigationlink.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      829 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/rawembed.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     1953 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/rss.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     6195 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/summary_view.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     4629 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/tabular_view.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      374 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/title.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     9746 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/testing.py
+-rw-r--r--   0 peterm     (501) staff       (20)      698 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/testing.zcml
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.926094 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/
+-rw-r--r--   0 peterm     (501) staff       (20)     2921 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/RSS.xml
+-rw-r--r--   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/__init__.py
+-rw-r--r--   0 peterm     (501) staff       (20)      819 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/custom_existingcontent_layout.pt
+-rw-r--r--   0 peterm     (501) staff       (20)      743 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/funky_display.pt
+-rw-r--r--   0 peterm     (501) staff       (20)     7293 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_content.py
+-rw-r--r--   0 peterm     (501) staff       (20)    14645 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_existing_content.py
+-rw-r--r--   0 peterm     (501) staff       (20)    10979 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_field.py
+-rw-r--r--   0 peterm     (501) staff       (20)     6241 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_head.py
+-rw-r--r--   0 peterm     (501) staff       (20)    15107 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_layout.py
+-rw-r--r--   0 peterm     (501) staff       (20)     7302 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_media.py
+-rw-r--r--   0 peterm     (501) staff       (20)     1625 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_setup.py
+-rw-r--r--   0 peterm     (501) staff       (20)      272 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/upgrades.py
+-rw-r--r--   0 peterm     (501) staff       (20)      746 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/upgrades.zcml
+-rw-r--r--   0 peterm     (501) staff       (20)     1854 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/utils.py
+-rw-r--r--   0 peterm     (501) staff       (20)     2488 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/viewletmanager.py
+drwxr-xr-x   0 peterm     (501) staff       (20)        0 2023-05-13 13:33:39.902356 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/
+-rw-r--r--   0 peterm     (501) staff       (20)    13196 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/PKG-INFO
+-rw-r--r--   0 peterm     (501) staff       (20)     3957 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/SOURCES.txt
+-rw-r--r--   0 peterm     (501) staff       (20)        1 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/dependency_links.txt
+-rw-r--r--   0 peterm     (501) staff       (20)       40 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/entry_points.txt
+-rw-r--r--   0 peterm     (501) staff       (20)       16 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/namespace_packages.txt
+-rw-r--r--   0 peterm     (501) staff       (20)        1 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/not-zip-safe
+-rw-r--r--   0 peterm     (501) staff       (20)      257 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/requires.txt
+-rw-r--r--   0 peterm     (501) staff       (20)        6 2023-05-13 13:33:39.000000 plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/top_level.txt
```

### Comparing `plone.app.standardtiles-3.1.0/CHANGES.rst` & `plone.app.standardtiles-3.1.1/CHANGES.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,17 @@
 Changelog
 =========
 
+3.1.1 (2023-05-13)
+------------------
+
+- Fix boolean fields title/description/text to not be required.
+  [petschki]
+
+
 3.1.0 (2023-05-04)
 ------------------
 
 - Add option to enable the Eventlisting view (this expands recurring events).
   NOTE: The listing will only show Event types.
   [petschki]
 
@@ -342,15 +349,15 @@
 
 - Simplify basic viewlet proxy tiles.
   [jensens]
 
 - Enable coveralls and code analysis.
   [gforcada]
 
-- Adapt travis to all other mosaic realted packages.
+- Adapt travis to all other mosaic related packages.
   [gforcada]
 
 - Remove unused function.
   [gforcada]
 
 
 1.0 (2016-04-11)
```

### Comparing `plone.app.standardtiles-3.1.0/LICENSE.GPL` & `plone.app.standardtiles-3.1.1/LICENSE.GPL`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/LICENSE.txt` & `plone.app.standardtiles-3.1.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/PKG-INFO` & `plone.app.standardtiles-3.1.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plone.app.standardtiles
-Version: 3.1.0
+Version: 3.1.1
 Summary: Tiles for plone.app.blocks page composition
 Home-page: https://github.com/plone/plone.app.standardtiles
 Author: Rob Gietema
 Author-email: rob@fourdigits.nl
 License: GPL
 Keywords: tiles content plone
 Classifier: Development Status :: 5 - Production/Stable
@@ -58,14 +58,21 @@
 -------
 
 The project is licensed under the GPLv2.
 
 Changelog
 =========
 
+3.1.1 (2023-05-13)
+------------------
+
+- Fix boolean fields title/description/text to not be required.
+  [petschki]
+
+
 3.1.0 (2023-05-04)
 ------------------
 
 - Add option to enable the Eventlisting view (this expands recurring events).
   NOTE: The listing will only show Event types.
   [petschki]
 
@@ -403,15 +410,15 @@
 
 - Simplify basic viewlet proxy tiles.
   [jensens]
 
 - Enable coveralls and code analysis.
   [gforcada]
 
-- Adapt travis to all other mosaic realted packages.
+- Adapt travis to all other mosaic related packages.
   [gforcada]
 
 - Remove unused function.
   [gforcada]
 
 
 1.0 (2016-04-11)
```

### Comparing `plone.app.standardtiles-3.1.0/README.rst` & `plone.app.standardtiles-3.1.1/README.rst`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/setup.py` & `plone.app.standardtiles-3.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import find_packages
 from setuptools import setup
 
 
-version = "3.1.0"
+version = "3.1.1"
 
 
 setup(
     name="plone.app.standardtiles",
     version=version,
     description="Tiles for plone.app.blocks page composition",
     long_description=(open("README.rst").read() + "\n" + open("CHANGES.rst").read()),
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/attachment.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/attachment.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/common.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/common.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/configure.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/configure.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/content.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/content.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/contentlisting.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/contentlisting.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/discussion.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/discussion.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/embed.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/embed.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/existingcontent.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/existingcontent.py`

 * *Files 2% similar despite different names*

```diff
@@ -72,19 +72,31 @@
     form.widget(
         "content_uid",
         RelatedItemsFieldWidget,
         vocabulary="plone.app.vocabularies.Catalog",
         pattern_options={"recentlyUsed": True},
     )
 
-    show_title = schema.Bool(title=_("Show content title"), default=True)
+    show_title = schema.Bool(
+        title=_("Show content title"),
+        default=True,
+        required=False,
+    )
 
-    show_description = schema.Bool(title=_("Show content description"), default=True)
+    show_description = schema.Bool(
+        title=_("Show content description"),
+        default=True,
+        required=False,
+    )
 
-    show_text = schema.Bool(title=_("Show content text"), default=True)
+    show_text = schema.Bool(
+        title=_("Show content text"),
+        default=True,
+        required=False,
+    )
 
     show_image = schema.Bool(
         title=_("Show content image (if available)"),
         default=False,
         required=False,
     )
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/field.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/field.py`

 * *Files 1% similar despite different names*

```diff
@@ -72,15 +72,15 @@
                         self.field
                     )
                     self._additionalSchemata = (schema,)
                     return
 
     @property
     def isVisible(self):
-        """Checks wheter the user has read permission of the field: if this is
+        """Checks whether the user has read permission of the field: if this is
         not the case, then the field is not displayed
         """
         try:
             schema = next(self.additionalSchemata)
         except StopIteration:
             schema = self.schema
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/head.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/head.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/head.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/head.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/html.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/html.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/interfaces.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/interfaces.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/layout.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/layout.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/linkintegrity.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/linkintegrity.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,29 +4,29 @@
 from plone.app.standardtiles import html
 from zope.component import adapter
 from zope.interface import implementer
 
 
 @implementer(IRetriever)
 @adapter(html.HTMLTile)
-class HTMLTile(object):
+class HTMLTile:
     def __init__(self, context):
         self.context = context
 
     def retrieveLinks(self):
         content = self.context.data["content"]
         # layout behavior tile storage hard codes 'utf-8' encoding
         # thus we do the same.
         links = set(extractLinks(content, "utf-8"))
         return links
 
 
 @implementer(IRetriever)
 @adapter(existingcontent.ExistingContentTile)
-class ExistingContentTile(object):
+class ExistingContentTile:
     def __init__(self, context):
         self.context = context
 
     def retrieveLinks(self):
         content_uid = self.context.data["content_uid"]
-        links = set(["../resolveuid/%s" % content_uid])
+        links = {"../resolveuid/%s" % content_uid}
         return links
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/media.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/media.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/metadata.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/metadata.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/navigation.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/navigation.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/add.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/add.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/assignment.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/assignment.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/configure.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/configure.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/edit.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/edit.py`

 * *Files 10% similar despite different names*

```diff
@@ -25,10 +25,8 @@
             tileId = self.tileId
 
         typeName = "plone.app.standardtiles.portlet"
         tile_url = "{}/@@{}/{}?portlet_hash={}".format(
             self.context.absolute_url(), typeName, tileId, portlet_hash
         )
         self.request.form["referer"] = tile_url
-        self.request.response.redirect(
-            "{0}?referer={1}".format(url, urllib.parse.quote(tile_url))
-        )
+        self.request.response.redirect(f"{url}?referer={urllib.parse.quote(tile_url)}")
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/portlet.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/portlet.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/portletmanager.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/portletmanager.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/utils.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/utils.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/portlets/vocabularies.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/portlets/vocabularies.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/profiles/default/registry.xml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/profiles/default/registry.xml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/rawembed.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/rawembed.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/rss.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/rss.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/setuphandlers.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/setuphandlers.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/sitemap.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/sitemap.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/attachment_listing.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/attachment_listing.pt`

 * *Files 7% similar despite different names*

```diff
@@ -1,51 +1,63 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
     <ul class="tileAttachment">
       <li tal:repeat="attachment view/data/files">
         <tal:file tal:condition="attachment">
           <a href="#"
-             tal:attributes="href string:${view/url}/@@download/${repeat/attachment/index}">
-            <img tal:condition="icon"
-                 class="icon"
-                 src="pdf.png"
+             tal:attributes="
+               href string:${view/url}/@@download/${repeat/attachment/index};
+             "
+          >
+            <img class="icon"
                  alt=""
-                 tal:define="icon python:view.get_icon_for(attachment)"
-                 tal:attributes="src string:${context/portal_url}/$icon"/>
+                 src="pdf.png"
+                 tal:define="
+                   icon python:view.get_icon_for(attachment);
+                 "
+                 tal:condition="icon"
+                 tal:attributes="
+                   src string:${context/portal_url}/$icon;
+                 "
+            />
             <tal:filename tal:replace="attachment/filename" />
           </a>
-          <span class="discreet byLine">
+          <span class="byLine">
             <span class="separator">
               -
             </span>
             <span class="contentType"
-                  tal:replace="python:view.lookupMime(attachment.contentType)">
+                  tal:replace="python:view.lookupMime(attachment.contentType)"
+            >
               PDF document
             </span>
             <span class="separator">
               -
             </span>
             <span class="fileSize"
-                  tal:replace="python:view.file_size(attachment)">
+                  tal:replace="python:view.file_size(attachment)"
+            >
               100
             </span>
             <span class="fileSizeUnit">
               KB
             </span>
           </span>
         </tal:file>
         <tal:no_file tal:condition="not:attachment">
-          <span class="discreet noFile"
-                i18n:translate="">
+          <span class="noFile"
+                i18n:translate=""
+          >
             No file
           </span>
         </tal:no_file>
       </li>
     </ul>
   </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/configlets.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/configlets.pt`

 * *Files 8% similar despite different names*

```diff
@@ -1,52 +1,71 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
-    <tal:controlpanel tal:define="controlPanel view/controlPanel;
-                                  groups python:controlPanel.getGroups('site');
-                                  portal_url context/portal_url;">
+    <tal:controlpanel tal:define="
+                        controlPanel view/controlPanel;
+                        groups python:controlPanel.getGroups('site');
+                        portal_url context/portal_url;
+                      ">
 
       <dl class="portlet"
-          id="portlet-prefs">
+          id="portlet-prefs"
+      >
         <dt class="portletHeader">
           <span class="portletTopLeft"></span>
           <a href=""
-             tal:attributes="href string:${portal_url}/plone_control_panel"
-             i18n:translate="">
+             tal:attributes="
+               href string:${portal_url}/plone_control_panel;
+             "
+             i18n:translate=""
+          >
             Site Setup
           </a>
           <span class="portletTopRight"></span>
         </dt>
 
         <dd class="portletItem"
-            tal:repeat="group groups">
-          <tal:block tal:define="configlets python:controlPanel.enumConfiglets(group=group['id'])"
-                     tal:condition="configlets">
+            tal:repeat="group groups"
+        >
+          <tal:block tal:define="
+                       configlets python:controlPanel.enumConfiglets(group=group['id']);
+                     "
+                     tal:condition="configlets"
+          >
             <strong tal:content="group/title"
-                    i18n:translate="">
+                    i18n:translate=""
+            >
               Plone Configlet Group Title
             </strong>
             <ul class="configlets">
               <tal:configlets tal:repeat="configlet configlets">
                 <li tal:condition="configlet/visible">
                   <a href=""
-                     tal:attributes="href configlet/url">
-                    <img src=""
-                         alt=""
-                         tal:attributes="src configlet/icon;
-                                         alt configlet/description"
+                     tal:attributes="
+                       href configlet/url;
+                     "
+                  >
+                    <img alt=""
+                         src=""
+                         tal:attributes="
+                           src configlet/icon;
+                           alt configlet/description;
+                         "
+                         tal:on-error="string:"
                          i18n:attributes="alt"
-                         tal:on-error="string:" />
+                    />
                     <tal:configletname tal:content="configlet/title"
-                                       i18n:translate=""></tal:configletname>
+                                       i18n:translate=""
+                    />
                   </a>
                 </li>
               </tal:configlets>
             </ul>
           </tal:block>
           <span class="portletBottomLeft"></span>
           <span class="portletBottomRight"></span>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/contentlisting_view.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/contentlisting_view.pt`

 * *Files 12% similar despite different names*

```diff
@@ -1,26 +1,30 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
 
     <h2 class="tileHeader"
         tal:condition="view/title"
-        tal:content="view/title">
+        tal:content="view/title"
+    >
       Title
     </h2>
 
     <div class="documentDescription"
          tal:condition="view/description"
-         tal:content="view/description">
+         tal:content="view/description"
+    >
       Description
     </div>
 
     <div class="${view/tile_class}"
-         tal:content="structure python:view.contents()">Listing</div>
+         tal:content="structure python:view.contents()"
+    >Listing</div>
 
   </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/existingcontent_view.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/existingcontent_view.pt`

 * *Files 10% similar despite different names*

```diff
@@ -1,87 +1,109 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
+      xmlns:metal="http://xml.zope.org/namespaces/metal"
       xmlns:tal="http://xml.zope.org/namespaces/tal"
-      xmlns:metal="http://xml.zope.org/namespaces/metal">
+      lang="en"
+      xml:lang="en"
+>
   <tal:block condition="nocall:view/content_context">
-  <tal:block condition="nocall:view/item_macros">
-  <body tal:define="context nocall:view/content_context;
-                    item_macro nocall:view/item_macros/content-core|nothing;
-                    data view/data;
-                    show_title python: data.get('show_title', True);
-                    show_description python: data.get('show_description', True);
-                    show_text python: data.get('show_text', True);
-                    show_image python: data.get('show_image', False);
-                    show_comments python: data.get('show_comments', False);">
+    <tal:block condition="nocall:view/item_macros">
+      <body tal:define="
+              context nocall:view/content_context;
+              item_macro nocall:view/item_macros/content-core|nothing;
+              data view/data;
+              show_title python: data.get('show_title', True);
+              show_description python: data.get('show_description', True);
+              show_text python: data.get('show_text', True);
+              show_image python: data.get('show_image', False);
+              show_comments python: data.get('show_comments', False);
+            ">
 
-    <section class="${view/tile_class}">
-      <h2 tal:define="title context/Title|nothing"
-          tal:condition="show_title"
-          tal:content="title">Title or id</h2>
+        <section class="${view/tile_class}">
+          <h2 tal:define="
+                title context/Title|nothing;
+              "
+              tal:condition="show_title"
+              tal:content="title"
+          >Title or id</h2>
 
-      <div class="documentDescription description"
-           tal:define="description context/Description|nothing"
-           tal:content="description"
-           tal:condition="show_description">
+          <div class="documentDescription description"
+               tal:define="
+                 description context/Description|nothing;
+               "
+               tal:condition="show_description"
+               tal:content="description"
+          >
           Description
-      </div>
-      <tal:image condition="show_image">
-        <div class="content-image"
-             tal:define="image_tag view/image_tag">
-          <figure><img tal:replace="structure image_tag" /></figure>
-        </div>
-      </tal:image>
-      <tal:text condition="show_text">
-        <tal:block condition="item_macro">
-          <div tal:define="view nocall:view/content_view;
-                           plone_view context/@@plone;
-                           portal_state context/@@plone_portal_state;
-                           context_state context/@@plone_context_state;
-                           plone_layout context/@@plone_layout;
-                           lang portal_state/language;
-                           dummy python: plone_layout.mark_view(view);
-                           portal_url portal_state/portal_url;
-                           checkPermission nocall: context/portal_membership/checkPermission;
-                           site_properties context/portal_properties/site_properties;
-                           fix python:request.set('ACTUAL_URL', context.absolute_url())">
-              <div metal:use-macro="item_macro">
+          </div>
+          <tal:image condition="show_image">
+            <div class="content-image"
+                 tal:define="
+                   image_tag view/image_tag;
+                 "
+            >
+              <figure><img tal:replace="structure image_tag" /></figure>
+            </div>
+          </tal:image>
+          <tal:text condition="show_text">
+            <tal:block condition="item_macro">
+              <div tal:define="
+                     view nocall:view/content_view;
+                     plone_view context/@@plone;
+                     portal_state context/@@plone_portal_state;
+                     context_state context/@@plone_context_state;
+                     plone_layout context/@@plone_layout;
+                     lang portal_state/language;
+                     dummy python: plone_layout.mark_view(view);
+                     portal_url portal_state/portal_url;
+                     checkPermission nocall: context/portal_membership/checkPermission;
+                     site_properties context/portal_properties/site_properties;
+                     fix python:request.set('ACTUAL_URL', context.absolute_url());
+                   ">
+                <div metal:use-macro="item_macro">
                   content
+                </div>
               </div>
-          </div>
-        </tal:block>
-        <tal:block tal:condition="not:item_macro">
-          <tal:comment tal:replace="nothing">
+            </tal:block>
+            <tal:block tal:condition="not:item_macro">
+              <tal:comment tal:replace="nothing">
             This is a fallback if your default_view has no "content-core"
             macro defined.
 
             Displays an error message for the developer.
-          </tal:comment>
-          <div>The template of the "<tal:view_name
-          replace="python:view.content_view_name" />" view of <tal:path
-          replace="python:context.absolute_url()" /> does not define a "content-core" macro.</div></tal:block>
-      </tal:text>
-      <div class="content-comments" tal:condition="show_comments"
-           tal:define="comments view/comments_count">
-        <a href="${context/absolute_url}#commenting">
-          <span class="icon-controlpanel-discussion"></span>
+              </tal:comment>
+              <div>The template of the "<tal:view_name replace="python:view.content_view_name" />" view of
+                <tal:path replace="python:context.absolute_url()" />
+                does not define a "content-core" macro.</div></tal:block>
+          </tal:text>
+          <div class="content-comments"
+               tal:define="
+                 comments view/comments_count;
+               "
+               tal:condition="show_comments"
+          >
+            <a href="${context/absolute_url}#commenting">
+              <span class="icon-controlpanel-discussion"></span>
           ${comments}
-        </a>
-      </div>
-    </section>
-  </body>
-  </tal:block>
-  <tal:block condition="not:nocall:view/item_macros">
-    <body>
-    <tal:panels define="panels python:view.item_panels">
-      <div tal:condition="panels"
-           tal:repeat="panel panels" tal:replace="structure panel">
+            </a>
+          </div>
+        </section>
+      </body>
+    </tal:block>
+    <tal:block condition="not:nocall:view/item_macros">
+      <body>
+        <tal:panels define="
+                      panels python:view.item_panels;
+                    ">
+          <div tal:condition="panels"
+               tal:repeat="panel panels"
+               tal:replace="structure panel"
+          >
           content
-      </div>
-      <p tal:condition="not:panels">Selected view is not available for the content.</p>
-    </tal:panels>
-    </body>
-  </tal:block>
+          </div>
+          <p tal:condition="not:panels">Selected view is not available for the content.</p>
+        </tal:panels>
+      </body>
+    </tal:block>
   </tal:block>
   <body tal:condition="not:nocall:view/content_context"></body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/image.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/image.pt`

 * *Files 19% similar despite different names*

```diff
@@ -1,18 +1,26 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
-  <body tal:define="scale view/data/scale;
-                    title view/data/title | nothing">
-    <img tal:define="scales view/@@images;
-                     thumbnail python: scales.scale('image', scale=scale)"
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
+  <body tal:define="
+          scale view/data/scale;
+          title view/data/title | nothing;
+        ">
+    <img tal:define="
+           scales view/@@images;
+           thumbnail python: scales.scale('image', scale=scale);
+         "
          tal:condition="thumbnail"
-         tal:attributes="alt title;
-                         title title;
-                         src thumbnail/url;
-                         width thumbnail/width;" />
+         tal:attributes="
+           alt title;
+           title title;
+           src thumbnail/url;
+           width thumbnail/width;
+         "
+    />
   </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/listing_view.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/listing_view.pt`

 * *Files 7% similar despite different names*

```diff
@@ -1,54 +1,71 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
-    <tal:defines define="batch context;
-                         original_context nocall:options/original_context|context;
-                         toLocalizedTime nocall:original_context/@@plone/toLocalizedTime;
-                         pas_member original_context/@@pas_member;
-                         show_about python:True;
-                         registry original_context/portal_registry;
-                         view_types python: registry.get('plone.types_use_view_action_in_listings', [])">
+    <tal:defines define="
+                   batch context;
+                   original_context nocall:options/original_context|context;
+                   toLocalizedTime nocall:original_context/@@plone/toLocalizedTime;
+                   pas_member original_context/@@pas_member;
+                   show_about python:True;
+                   registry original_context/portal_registry;
+                   view_types python: registry.get('plone.types_use_view_action_in_listings', []);
+                 ">
       <tal:listing condition="batch">
         <dl>
           <tal:entry repeat="item batch">
-            <dt tal:define="item_has_image python:item.getIcon;
-                            item_url item/getURL|item/absolute_url;
-                            item_type item/portal_type;
-                            item_creator item/Creator|item/creator;
-                            item_modified item/ModificationDate|item/modified;
-                            item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url">
+            <dt tal:define="
+                  item_has_image python:item.getIcon;
+                  item_url item/getURL|item/absolute_url;
+                  item_type item/portal_type;
+                  item_creator item/Creator|item/creator;
+                  item_modified item/ModificationDate|item/modified;
+                  item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url;
+                ">
               <span class="summary">
                 <img tal:condition="item_has_image"
-                             tal:attributes="src string:${item_url}/@@images/image/tile" />
+                     tal:attributes="
+                       src string:${item_url}/@@images/image/tile;
+                     "
+                />
                 <a href="#"
-                   tal:attributes="href item_view_url;
-                                   class string:${item/ContentTypeClass} ${item/review_state}"
-                   tal:content="item/Title|item/getId" />
+                   tal:content="item/Title|item/getId"
+                   tal:attributes="
+                     href item_view_url;
+                     class string:${item/ContentTypeClass} ${item/review_state};
+                   "
+                ></a>
               </span>
               <span class="documentByLine">
                 <tal:comment condition="python:item_type == 'Event'">
                   <!-- Removed special handling for Event type for now.-->
                 </tal:comment>
                 <tal:byline condition="show_about">
                   &mdash;
                   <span class="documentAuthor"
-                        tal:define="author python:pas_member.info(item_creator)"
-                        i18n:translate="label_by_author">
+                        tal:define="
+                          author python:pas_member.info(item_creator);
+                        "
+                        i18n:translate="label_by_author"
+                  >
                     by
                     <a href="#"
                        tal:content="author/name_or_id"
                        tal:omit-tag="not:author"
-                       tal:attributes="href string:${original_context/@@plone_portal_state/navigation_root_url}/author/${author/username}"
-                       i18n:name="author">
+                       tal:attributes="
+                         href string:${original_context/@@plone_portal_state/navigation_root_url}/author/${author/username};
+                       "
+                       i18n:name="author"
+                    >
                       Bob Dobalina
                     </a>
                   </span>
                   <tal:modified condition="python: item_type != 'Event'">
                     &mdash;
                     <tal:mod i18n:translate="">
                       last modified
@@ -63,17 +80,18 @@
             <dd>
               <span tal:replace="item/Description">
                 Cropped description
               </span>
             </dd>
           </tal:entry>
         </dl>
-        <div metal:use-macro="original_context/batch_macros/macros/navigation" />
+        <div metal:use-macro="original_context/batch_macros/macros/navigation"></div>
       </tal:listing>
-      <p class="discreet"
+      <p class="text-bg-secondary"
          tal:condition="not:batch"
-         i18n:translate="">
+         i18n:translate=""
+      >
         There are currently no items in this folder.
       </p>
     </tal:defines>
   </body>
 </html>
```

#### html2text {}

```diff
@@ -1,5 +1,5 @@
 
-   [Image] ______—__by_Bob_Dobalina___—__last_modified___August_16,_2001_at_23:
-  35:59____
+   [Image]        —  by Bob_Dobalina   —  last modified   August 16, 2001 at
+  23:35:59
        Cropped description
 There are currently no items in this folder.
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/namedimage.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/namedimage.pt`

 * *Files 22% similar despite different names*

```diff
@@ -1,32 +1,47 @@
-<span id="" class="" i18n:domain="plone.formwidget.namedfile"
-      tal:attributes="id view/id;
-                      class view/klass;
-                      style view/style;
-                      title view/title;
-                      lang view/lang;
-                      onclick view/onclick;
-                      ondblclick view/ondblclick;
-                      onmousedown view/onmousedown;
-                      onmouseup view/onmouseup;
-                      onmouseover view/onmouseover;
-                      onmousemove view/onmousemove;
-                      onmouseout view/onmouseout;
-                      onkeypress view/onkeypress;
-                      onkeydown view/onkeydown;
-                      onkeyup view/onkeyup"
-        tal:define="value view/value;
-                    exists python:value is not None;
-                    scales context/@@images;
-                    title context/title | nothing;
-                    fieldname view/field/__name__ | nothing;"
-        tal:condition="fieldname">
-        <img tal:define="thumbnail python:scales.scale(fieldname, width=320, direction='down')"
-             tal:condition="thumbnail"
-             tal:attributes="alt title;
-                             title title;
-                             src thumbnail/url;
-                             width thumbnail/width" />
-        <span tal:condition="not:exists" class="discreet" i18n:translate="no_image">
+<span class=""
+      id=""
+      tal:define="
+        value view/value;
+        exists python:value is not None;
+        scales context/@@images;
+        title context/title | nothing;
+        fieldname view/field/__name__ | nothing;
+      "
+      tal:condition="fieldname"
+      tal:attributes="
+        id view/id;
+        class view/klass;
+        style view/style;
+        title view/title;
+        lang view/lang;
+        onclick view/onclick;
+        ondblclick view/ondblclick;
+        onmousedown view/onmousedown;
+        onmouseup view/onmouseup;
+        onmouseover view/onmouseover;
+        onmousemove view/onmousemove;
+        onmouseout view/onmouseout;
+        onkeypress view/onkeypress;
+        onkeydown view/onkeydown;
+        onkeyup view/onkeyup;
+      "
+      i18n:domain="plone.formwidget.namedfile"
+>
+  <img tal:define="
+         thumbnail python:scales.scale(fieldname, width=320, direction='down');
+       "
+       tal:condition="thumbnail"
+       tal:attributes="
+         alt title;
+         title title;
+         src thumbnail/url;
+         width thumbnail/width;
+       "
+  />
+  <span class="text-bg-secondary"
+        tal:condition="not:exists"
+        i18n:translate="no_image"
+  >
             No image
-        </span>
-</span>
+  </span>
+</span>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigation.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigation.pt`

 * *Files 7% similar despite different names*

```diff
@@ -1,34 +1,50 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
     <div class="navigationTile"
-         tal:define="root view/navigation_root">
+         tal:define="
+           root view/navigation_root;
+         "
+    >
       <h2 class="tileHeader"
           tal:condition="view/title"
-          tal:content="view/title">
+          tal:content="view/title"
+      >
         Navigation
       </h2>
       <ul class="navTree navTreeLevel0">
-        <li tal:define="selectedClass view/root_item_class;
-                        li_class python:selectedClass and ' navTreeCurrentNode' or '';"
+        <li tal:define="
+              selectedClass view/root_item_class;
+              li_class python:selectedClass and ' navTreeCurrentNode' or '';
+            "
             tal:condition="view/include_top"
-            tal:attributes="class string:navTreeItem navTreeTopNode${li_class}">
-          <tal:block tal:define="rootIsPortal view/root_is_portal;">
-            <a tal:attributes="href root/absolute_url;
-                               title root/Description;
-                               class string:contenttype-plone-site $selectedClass;">
+            tal:attributes="
+              class string:navTreeItem navTreeTopNode${li_class};
+            "
+        >
+          <tal:block tal:define="
+                       rootIsPortal view/root_is_portal;
+                     ">
+            <a tal:attributes="
+                 href root/absolute_url;
+                 title root/Description;
+                 class string:contenttype-plone-site $selectedClass;
+               ">
               <span tal:condition="rootIsPortal"
-                    i18n:translate="">Home</span><span tal:condition="not:rootIsPortal"
-                    tal:content="root/Title">Root item title</span></a>
+                    i18n:translate=""
+              >Home</span><span tal:condition="not:rootIsPortal"
+                    tal:content="root/Title"
+              >Root item title</span></a>
           </tal:block>
         </li>
         <li tal:replace="structure view/createNavTree">
           SUBTREE
         </li>
       </ul>
     </div>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigation_recurse.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigation_recurse.pt`

 * *Files 25% similar despite different names*

```diff
@@ -1,40 +1,56 @@
-<tal:master define="level options/level|python:0;
-                    children options/children | nothing;
-                    bottomLevel options/bottomLevel | nothing;">
+<tal:master define="
+              level options/level|python:0;
+              children options/children | nothing;
+              bottomLevel options/bottomLevel | nothing;
+            ">
 
-<metal:main define-macro="nav_main">
-<tal:navitem repeat="node children">
-<li tal:define="show_children   node/show_children;
-                children        node/children;
-                item_url        node/getURL;
-                item_icon       nocall:node/item_icon|nothing;
-                item_type       node/portal_type;
-                is_current      node/currentItem;
-                is_in_path      node/currentParent;
-                li_class        python:is_current and ' navTreeCurrentNode' or '';
-                li_extr_class   python:is_in_path and ' navTreeItemInPath' or '';
-                li_folder_class python:show_children and ' navTreeFolderish' or '';
-                normalizeString nocall: context/plone_utils/normalizeString;"
-    tal:attributes="class string:navTreeItem visualNoMarker${li_class}${li_extr_class}${li_folder_class} section-${node/normalized_id}"
-    tal:condition="python:bottomLevel &lt;= 0 or level &lt;= bottomLevel">
+  <metal:main define-macro="nav_main">
+    <tal:navitem repeat="node children">
+      <li tal:define="
+            show_children   node/show_children;
+            children        node/children;
+            item_url        node/getURL;
+            item_icon       nocall:node/item_icon|nothing;
+            item_type       node/portal_type;
+            is_current      node/currentItem;
+            is_in_path      node/currentParent;
+            li_class        python:is_current and ' navTreeCurrentNode' or '';
+            li_extr_class   python:is_in_path and ' navTreeItemInPath' or '';
+            li_folder_class python:show_children and ' navTreeFolderish' or '';
+            normalizeString nocall: context/plone_utils/normalizeString;
+          "
+          tal:condition="python:bottomLevel &lt;= 0 or level &lt;= bottomLevel"
+          tal:attributes="
+            class string:navTreeItem visualNoMarker${li_class}${li_extr_class}${li_folder_class} section-${node/normalized_id};
+          "
+      >
 
-    <tal:level define="item_class string:state-${node/normalized_review_state};
-                       item_type_class python:'contenttype-' + normalizeString(item_type);
-                       item_class python:is_current and item_class + ' navTreeCurrentItem' or item_class;">
+        <tal:level define="
+                     item_class string:state-${node/normalized_review_state};
+                     item_type_class python:'contenttype-' + normalizeString(item_type);
+                     item_class python:is_current and item_class + ' navTreeCurrentItem' or item_class;
+                   ">
 
 
-        <a tal:attributes="href python:item_url;
-                           title node/Description;
-                           class string:$item_class${li_class}${li_extr_class}${li_folder_class} $item_type_class">
-            <img tal:condition="item_icon" tal:replace="structure item_icon/html_tag" />
+          <a tal:attributes="
+               href python:item_url;
+               title node/Description;
+               class string:$item_class${li_class}${li_extr_class}${li_folder_class} $item_type_class;
+             ">
+            <img tal:condition="item_icon"
+                 tal:replace="structure item_icon/html_tag"
+            />
             <span tal:content="node/Title">Selected Item Title</span></a>
 
-    <ul tal:attributes="class python:'navTree navTreeLevel'+str(level)"
-        tal:condition="python: len(children) > 0 and show_children">
-        <span tal:replace="structure python:view.recurse(children=children, level=level+1, bottomLevel=bottomLevel)" />
-    </ul>
-    </tal:level>
-</li>
-</tal:navitem>
-</metal:main>
+          <ul tal:condition="python: len(children) &gt; 0 and show_children"
+              tal:attributes="
+                class python:'navTree navTreeLevel'+str(level);
+              "
+          >
+            <span tal:replace="structure python:view.recurse(children=children, level=level+1, bottomLevel=bottomLevel)"></span>
+          </ul>
+        </tal:level>
+      </li>
+    </tal:navitem>
+  </metal:main>
 </tal:master>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/navigationlink.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/navigationlink.pt`

 * *Files 6% similar despite different names*

```diff
@@ -1,20 +1,27 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
-<head>
-  <link rel="home"
-        href=""
-        title="Front page"
-        i18n:attributes="title"
-        tal:attributes="href string:${view/navigation_root_url}" />
-  <link rel="contents"
-        href=""
-        title="Site Map"
-        i18n:attributes="title"
-        tal:attributes="href string:${view/navigation_root_url}/sitemap" />
-</head>
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
+  <head>
+    <link href=""
+          rel="home"
+          title="Front page"
+          tal:attributes="
+            href string:${view/navigation_root_url};
+          "
+          i18n:attributes="title"
+    />
+    <link href=""
+          rel="contents"
+          title="Site Map"
+          tal:attributes="
+            href string:${view/navigation_root_url}/sitemap;
+          "
+          i18n:attributes="title"
+    />
+  </head>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/rawembed.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/rawembed.pt`

 * *Files 6% similar despite different names*

```diff
@@ -1,21 +1,30 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
+      xmlns:metal="http://xml.zope.org/namespaces/metal"
       xmlns:tal="http://xml.zope.org/namespaces/tal"
-      xmlns:metal="http://xml.zope.org/namespaces/metal">
-  <body tal:define="title context/Title|nothing"
-                    i18n:domain="plone">
+      lang="en"
+      xml:lang="en"
+>
+  <body tal:define="
+          title context/Title|nothing;
+        "
+        i18n:domain="plone"
+  >
 
-  <div class="tileItem clearfix"
-       tal:attributes="class string:tileItem tile-id-${view/tile_id}">
-      <div class="tileHeading" tal:condition="view/show_title">
-          <h2 tal:content="view/tile_title">Title</h2>
+    <div class="tileItem clearfix"
+         tal:attributes="
+           class string:tileItem tile-id-${view/tile_id};
+         "
+    >
+      <div class="tileHeading"
+           tal:condition="view/show_title"
+      >
+        <h2 tal:content="view/tile_title">Title</h2>
       </div>
       <div class="tileBody">
         <div tal:replace="structure view/html_snippet">snippet</div>
       </div>
     </div>
 
   </body>
-</html>
+</html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/rss.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/rss.pt`

 * *Files 25% similar despite different names*

```diff
@@ -1,51 +1,73 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
-    <dl tal:condition="view/enabled"
-        class="rsstile">
+    <dl class="rsstile"
+        tal:condition="view/enabled"
+    >
       <dt class="header rss-title">
-        <a href=""
-           tal:attributes="href view/siteurl"
+        <a class="tile"
+           href=""
            tal:content="view/title"
-           class="tile">
+           tal:attributes="
+             href view/siteurl;
+           "
+        >
           Tags
         </a>
       </dt>
-      <tal:rss tal:condition="view/feedAvailable"
-               tal:define="toLocalizedTime nocall:context/@@plone/toLocalizedTime"
-               tal:repeat="item view/items">
+      <tal:rss tal:define="
+                 toLocalizedTime nocall:context/@@plone/toLocalizedTime;
+               "
+               tal:condition="view/feedAvailable"
+               tal:repeat="item view/items"
+      >
         <dd class="oddrow"
-            tal:define="oddrow repeat/item/odd"
-            tal:attributes="class python:oddrow and 'even' or 'odd'">
-          <a href="#"
-             tal:attributes="href string:${item/url}"
-             class="tile">
+            tal:define="
+              oddrow repeat/item/odd;
+            "
+            tal:attributes="
+              class python:oddrow and 'even' or 'odd';
+            "
+        >
+          <a class="tile"
+             href="#"
+             tal:attributes="
+               href string:${item/url};
+             "
+          >
             <span tal:replace="item/title">
               Title
             </span>
             <span class="itemDetails"
-                  tal:condition="exists:item/updated">
-              <span tal:omit-tag=""
-                    tal:content="python:toLocalizedTime(item['updated'])">
+                  tal:condition="exists:item/updated"
+            >
+              <span tal:content="python:toLocalizedTime(item['updated'])"
+                    tal:omit-tag=""
+              >
                 19.02.2007
               </span>
             </span>
           </a>
         </dd>
       </tal:rss>
       <dd class="footer rss-more"
-          tal:condition="view/feedAvailable">
+          tal:condition="view/feedAvailable"
+      >
         <a href=""
-           tal:attributes="href view/siteurl"
-           i18n:translate="box_morelink">
+           tal:attributes="
+             href view/siteurl;
+           "
+           i18n:translate="box_morelink"
+        >
           More&hellip;
         </a>
       </dd>
     </dl>
   </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/summary_view.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/summary_view.pt`

 * *Files 14% similar despite different names*

```diff
@@ -1,127 +1,164 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml"
-      xml:lang="en"
-      lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
-      xmlns:metal="http://xml.zope.org/namespaces/metal"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
-      i18n:domain="plone">
+      xmlns:metal="http://xml.zope.org/namespaces/metal"
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
+      lang="en"
+      xml:lang="en"
+      i18n:domain="plone"
+>
   <body>
-    <div tal:define="batch context;
-                     original_context nocall:options/original_context|context;
-                     registry original_context/portal_registry;
-                     view_types python: registry.get('plone.types_use_view_action_in_listings', [])">
+    <div tal:define="
+           batch context;
+           original_context nocall:options/original_context|context;
+           registry original_context/portal_registry;
+           view_types python: registry.get('plone.types_use_view_action_in_listings', []);
+         ">
       <tal:entry repeat="item batch">
-      <tal:block tal:define="item_url item/getURL|item/absolute_url;
-                             item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url;
-                             item_title_or_id item/Title|item/title_or_id;
-                             item_type item/portal_type;
-                             item_creator item/Creator|item/creator;
-                             item_description item/Description;
-                             item_modified item/ModificationDate|item/modified;
-                             item_start item/start;
-                             item_end item/end;">
-        <div class="tileItem visualIEFloatFix"
-             tal:define="item_has_image python:item.getIcon">
-          <a href="#"
-             class="summary-image"
-             tal:condition="item_has_image"
-             tal:attributes="href item_view_url">
-            <img tal:condition="item_has_image"
-                 tal:attributes="src string:${item_url}/@@images/image/thumb"
-                 alt=""/>
-          </a>
-          <h2 class="tileHeadline"
-              metal:define-macro="listitem">
-            <a href="#"
-               class="summary url"
-               tal:attributes="href item_view_url"
-               tal:content="item_title_or_id">
-              Item Title
+        <tal:block tal:define="
+                     item_url item/getURL|item/absolute_url;
+                     item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url;
+                     item_title_or_id item/Title|item/title_or_id;
+                     item_type item/portal_type;
+                     item_creator item/Creator|item/creator;
+                     item_description item/Description;
+                     item_modified item/ModificationDate|item/modified;
+                     item_start item/start;
+                     item_end item/end;
+                   ">
+          <div class="tileItem visualIEFloatFix"
+               tal:define="
+                 item_has_image python:item.getIcon;
+               "
+          >
+            <a class="summary-image"
+               href="#"
+               tal:condition="item_has_image"
+               tal:attributes="
+                 href item_view_url;
+               "
+            >
+              <img alt=""
+                   tal:condition="item_has_image"
+                   tal:attributes="
+                     src string:${item_url}/@@images/image/thumb;
+                   "
+              />
             </a>
-          </h2>
-          <div class="documentByLine">
-            <tal:event condition="python: item_start or item_end">
-              <span tal:condition="python: item.location"
-                    i18n:translate="">
-                (<span tal:content="string:${item/location}"
-                      class="location"
-                      i18n:name="location">
+            <h2 class="tileHeadline"
+                metal:define-macro="listitem"
+            >
+              <a class="summary url"
+                 href="#"
+                 tal:content="item_title_or_id"
+                 tal:attributes="
+                   href item_view_url;
+                 "
+              >
+              Item Title
+              </a>
+            </h2>
+            <div class="documentByLine">
+              <tal:event condition="python: item_start or item_end">
+                <span tal:condition="python: item.location"
+                      i18n:translate=""
+                >
+                  (<span class="location"
+                        tal:content="string:${item/location}"
+                        i18n:name="location"
+                  >
                   Oslo
-                </span>, from
-                <abbr class="dtstart pat-moment"
-                      title="${python:item_start.isoformat()}"
-                      data-pat-moment="format:MMMM Do, YYYY h:mm a;"
-                      data-date="${python: item_start.isoformat()}"
-                      i18n:name="start">
+                  </span>, from
+                  <abbr class="dtstart pat-moment"
+                        title="${python:item_start.isoformat()}"
+                        data-date="${python: item_start.isoformat()}"
+                        data-pat-moment="format:MMMM Do, YYYY h:mm a;"
+                        i18n:name="start"
+                  >
                   ${python: item_start.ctime()}
-                </abbr>
+                  </abbr>
                 to
-                <abbr class="dtend pat-moment"
-                      title="${python:item_end.isoformat()}"
-                      data-date="${python: item_end.isoformat()}"
-                      i18n:name="end">
+                  <abbr class="dtend pat-moment"
+                        title="${python:item_end.isoformat()}"
+                        data-date="${python: item_end.isoformat()}"
+                        i18n:name="end"
+                  >
                     ${python: item_end.ctime()}
-                </abbr>)
-              </span>
-              <span tal:condition="python: not item.location"
-                    i18n:translate="">
+                  </abbr>)
+                </span>
+                <span tal:condition="python: not item.location"
+                      i18n:translate=""
+                >
                 (from
-                <abbr class="dtstart pat-moment"
-                      title="${python:item_start.isoformat()}"
-                      data-pat-moment="format:MMMM Do, YYYY h:mm a;"
-                      data-date="${python: item_start.isoformat()}"
-                      i18n:name="start">
+                  <abbr class="dtstart pat-moment"
+                        title="${python:item_start.isoformat()}"
+                        data-date="${python: item_start.isoformat()}"
+                        data-pat-moment="format:MMMM Do, YYYY h:mm a;"
+                        i18n:name="start"
+                  >
                   ${python: item_start.ctime()}
-                </abbr>
+                  </abbr>
                 to
-                <abbr class="dtend pat-moment"
-                      title="${python:item_end.isoformat()}"
-                      data-date="${python: item_end.isoformat()}"
-                      i18n:name="end">
+                  <abbr class="dtend pat-moment"
+                        title="${python:item_end.isoformat()}"
+                        data-date="${python: item_end.isoformat()}"
+                        i18n:name="end"
+                  >
                   ${python: item_end.ctime()}
-                </abbr>)
-              </span>
-            </tal:event>
-            <tal:newsitem condition="python: item_type == 'News Item'">
-              <tal:name tal:condition="item_creator" tal:define="author item_creator">
-                <a href="#"
-                   tal:attributes="href string:author/${author/username|nothing}"
-                   tal:content="author/username|nothing"
-                   tal:omit-tag="not:author">
+                  </abbr>)
+                </span>
+              </tal:event>
+              <tal:newsitem condition="python: item_type == 'News Item'">
+                <tal:name tal:define="
+                            author item_creator;
+                          "
+                          tal:condition="item_creator"
+                >
+                  <a href="#"
+                     tal:content="author/username|nothing"
+                     tal:omit-tag="not:author"
+                     tal:attributes="
+                       href string:author/${author/username|nothing};
+                     "
+                  >
                   Bob Dobalina
-                </a>
-              </tal:name>
+                  </a>
+                </tal:name>
               &mdash;
-              <span class="documentModified">
-                <tal:mod i18n:translate="">
+                <span class="documentModified">
+                  <tal:mod i18n:translate="">
                   last modified
-                </tal:mod>
-                <span tal:content="item_modified">
+                  </tal:mod>
+                  <span tal:content="item_modified">
                   August 16, 2001 at 23:35:59
+                  </span>
                 </span>
-              </span>
-            </tal:newsitem>
-          </div>
-          <p class="tileBody"
-             tal:condition="item_description">
-            <span class="description"
-                  tal:content="item_description">
+              </tal:newsitem>
+            </div>
+            <p class="tileBody"
+               tal:condition="item_description"
+            >
+              <span class="description"
+                    tal:content="item_description"
+              >
               description
-            </span>
-          </p>
-          <p class="tileFooter">
-            <a href=""
-               tal:attributes="href python:item_url"
-               i18n:translate="read_more">
+              </span>
+            </p>
+            <p class="tileFooter">
+              <a href=""
+                 tal:attributes="
+                   href python:item_url;
+                 "
+                 i18n:translate="read_more"
+              >
               Read More&hellip;
-            </a>
-          </p>
-          <div class="visualClear"><!-- --></div>
-        </div>
-      </tal:block>
+              </a>
+            </p>
+            <div class="visualClear"><!-- --></div>
+          </div>
+        </tal:block>
       </tal:entry>
-      <div metal:use-macro="original_context/batch_macros/macros/navigation" />
+      <div metal:use-macro="original_context/batch_macros/macros/navigation"></div>
     </div>
   </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/templates/tabular_view.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/templates/tabular_view.pt`

 * *Files 6% similar despite different names*

```diff
@@ -1,92 +1,122 @@
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
-<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
-      xmlns:metal="http://xml.zope.org/namespaces/metal"
+<html xmlns="http://www.w3.org/1999/xhtml"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
+      xmlns:metal="http://xml.zope.org/namespaces/metal"
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
       lang="en"
-      i18n:domain="plone">
-    <body>
-        <div tal:define="batch context;
-                         original_context nocall:options/original_context|context;
-                         pas_member original_context/@@pas_member;
-                         registry original_context/portal_registry;
-                         view_types python: registry.get('plone.types_use_view_action_in_listings', []);
-                         view_about python: registry.get('plone.allow_anon_views_about', False)">
-            <div tal:condition="not: batch">
-                <p><strong>Nothing to list</strong></p>
-            </div>
+      xml:lang="en"
+      i18n:domain="plone"
+>
+  <body>
+    <div tal:define="
+           batch context;
+           original_context nocall:options/original_context|context;
+           pas_member original_context/@@pas_member;
+           registry original_context/portal_registry;
+           view_types python: registry.get('plone.types_use_view_action_in_listings', []);
+           view_about python: registry.get('plone.allow_anon_views_about', False);
+         ">
+      <div tal:condition="not: batch">
+        <p><strong>Nothing to list</strong></p>
+      </div>
 
-            <div tal:condition="batch">
+      <div tal:condition="batch">
 
-                    <table class="listing" summary="Content listing" i18n:attributes="summary">
-                    <thead>
-                        <tr>
-                            <th class="nosort">&nbsp;
-                                <tal:title i18n:translate="">
+        <table class="listing"
+               summary="Content listing"
+               i18n:attributes="summary"
+        >
+          <thead>
+            <tr>
+              <th class="nosort">&nbsp;
+                <tal:title i18n:translate="">
                                     Title
-                                </tal:title>&nbsp;
-                            </th>
-                            <th class="nosort" tal:condition="view_about">&nbsp;
-                                <tal:title i18n:translate="">
+                </tal:title>&nbsp;
+              </th>
+              <th class="nosort"
+                  tal:condition="view_about"
+              >&nbsp;
+                <tal:title i18n:translate="">
                                     Author
-                                </tal:title>
+                </tal:title>
                                 &nbsp;
-                            </th>
-                            <th class="nosort">
+              </th>
+              <th class="nosort">
                                 &nbsp;
-                                <tal:title i18n:translate="">
+                <tal:title i18n:translate="">
                                     Type
-                                </tal:title>
+                </tal:title>
                                 &nbsp;
-                            </th>
-                            <th class="nosort">
+              </th>
+              <th class="nosort">
                                 &nbsp;
-                                <tal:modified i18n:translate="">
+                <tal:modified i18n:translate="">
                                     Modified
-                                </tal:modified>&nbsp;
-                            </th>
-                        </tr>
-                    </thead>
-                    <tbody>
-                        <tal:results repeat="item batch">
-                            <tal:block tal:define="item_url item/getURL|item/absolute_url;
-                                                   item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url;
-                                                   item_title_or_id item/Title|item/title_or_id;
-                                                   item_type item/portal_type;
-                                                   item_description item/Description;
-                                                   item_creator item/Creator|item/creator;
-                                                   item_modified item/ModificationDate|item/modified">
+                </tal:modified>&nbsp;
+              </th>
+            </tr>
+          </thead>
+          <tbody>
+            <tal:results repeat="item batch">
+              <tal:block tal:define="
+                           item_url item/getURL|item/absolute_url;
+                           item_view_url python: item_url + '/view' if item.portal_type in view_types else item_url;
+                           item_title_or_id item/Title|item/title_or_id;
+                           item_type item/portal_type;
+                           item_description item/Description;
+                           item_creator item/Creator|item/creator;
+                           item_modified item/ModificationDate|item/modified;
+                         ">
 
-                            <tr tal:define="oddrow repeat/item/odd;"
-                                tal:attributes="class python:oddrow and 'even' or 'odd'" >
-                                <td>
-                                    <a href="#" tal:attributes="href item_view_url" tal:content="item_title_or_id">
+                <tr tal:define="
+                      oddrow repeat/item/odd;
+                    "
+                    tal:attributes="
+                      class python:oddrow and 'even' or 'odd';
+                    "
+                >
+                  <td>
+                    <a href="#"
+                       tal:content="item_title_or_id"
+                       tal:attributes="
+                         href item_view_url;
+                       "
+                    >
                                         Item Title
-                                    </a>
-                                </td>
-                                <td tal:condition="view_about">
-                                    <tal:name tal:condition="item_creator" tal:define="author python:pas_member.info(item_creator)">
-                                        <a href="#"
-                                           tal:attributes="href string:author/${author/username}"
-                                           tal:content="author/username"
-                                           tal:omit-tag="not:author">
+                    </a>
+                  </td>
+                  <td tal:condition="view_about">
+                    <tal:name tal:define="
+                                author python:pas_member.info(item_creator);
+                              "
+                              tal:condition="item_creator"
+                    >
+                      <a href="#"
+                         tal:content="author/username"
+                         tal:omit-tag="not:author"
+                         tal:attributes="
+                           href string:author/${author/username};
+                         "
+                      >
                                             Bob Dobalina
-                                        </a>
-                                    </tal:name>
-                                </td>
-                                <td tal:content="item_type">
+                      </a>
+                    </tal:name>
+                  </td>
+                  <td tal:content="item_type">
                                     Page
-                                </td>
-                                <td class="pat-moment" tal:content="python: item.modified.fCommon()"
-                                   data-pat-moment="format:MMMM Do, YYYY h:mm a;"
-                                   data-date="${python: item.modified.ISO8601()}" />
-                        </tal:block>
+                  </td>
+                  <td class="pat-moment"
+                      data-date="${python: item.modified.ISO8601()}"
+                      data-pat-moment="format:MMMM Do, YYYY h:mm a;"
+                      tal:content="python: item.modified.fCommon()"
+                  ></td>
+                </tr></tal:block>
 
-                        </tal:results>
-                    </tbody>
-                </table>
-                <div metal:use-macro="original_context/batch_macros/macros/navigation" />
-            </div>
-        </div>
-    </body>
+            </tal:results>
+          </tbody>
+        </table>
+        <div metal:use-macro="original_context/batch_macros/macros/navigation"></div>
+      </div>
+    </div>
+  </body>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/testing.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/testing.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/testing.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/testing.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/RSS.xml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/RSS.xml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/custom_existingcontent_layout.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/custom_existingcontent_layout.pt`

 * *Files 16% similar despite different names*

```diff
@@ -1,21 +1,25 @@
-<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en"
-      xmlns:tal="http://xml.zope.org/namespaces/tal"
-      xmlns:metal="http://xml.zope.org/namespaces/metal"
+<html xmlns="http://www.w3.org/1999/xhtml"
       xmlns:i18n="http://xml.zope.org/namespaces/i18n"
+      xmlns:metal="http://xml.zope.org/namespaces/metal"
+      xmlns:tal="http://xml.zope.org/namespaces/tal"
       lang="en"
       metal:use-macro="context/main_template/macros/master"
-      i18n:domain="plone">
-<body>
+      xml:lang="en"
+      i18n:domain="plone"
+>
+  <body>
 
-<metal:title fill-slot="content-title"><!--!empty--></metal:title>
-<metal:description fill-slot="content-description"><!--!empty--></metal:description>
+    <metal:title fill-slot="content-title"><!--!empty--></metal:title>
+    <metal:description fill-slot="content-description"><!--!empty--></metal:description>
 
-<metal:content-core fill-slot="content-core">
-  <metal:block define-macro="content-core">
-    <span>This is a custom layout</span>
-    <div tal:condition="context/text" tal:replace="context/text/output">
-  </metal:block>
-</metal:content-core>
+    <metal:content-core fill-slot="content-core">
+      <metal:block define-macro="content-core">
+        <span>This is a custom layout</span>
+        <div tal:condition="context/text"
+             tal:replace="context/text/output"
+        >
+        </div></metal:block>
+    </metal:content-core>
 
-</body>
+  </body>
 </html>
```

#### html2text {}

```diff
@@ -1,2 +1 @@
     This is a custom layout
-
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/funky_display.pt` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/funky_display.pt`

 * *Files 5% similar despite different names*

```diff
@@ -1,22 +1,27 @@
 <html xmlns="http://www.w3.org/1999/xhtml"
       xmlns:tal="http://xml.zope.org/namespaces/tal"
-      tal:omit-tag="">
-    <h1 id="" class=""
-          tal:attributes="id view/id;
-                          class view/klass;
-                          style view/style;
-                          title view/title;
-                          lang view/lang;
-                          onclick view/onclick;
-                          ondblclick view/ondblclick;
-                          onmousedown view/onmousedown;
-                          onmouseup view/onmouseup;
-                          onmouseover view/onmouseover;
-                          onmousemove view/onmousemove;
-                          onmouseout view/onmouseout;
-                          onkeypress view/onkeypress;
-                          onkeydown view/onkeydown;
-                          onkeyup view/onkeyup"><tal:block
-          condition="view/value" content="view/value"
+      tal:omit-tag=""
+>
+  <h1 class=""
+      id=""
+      tal:attributes="
+        id view/id;
+        class view/klass;
+        style view/style;
+        title view/title;
+        lang view/lang;
+        onclick view/onclick;
+        ondblclick view/ondblclick;
+        onmousedown view/onmousedown;
+        onmouseup view/onmouseup;
+        onmouseover view/onmouseover;
+        onmousemove view/onmousemove;
+        onmouseout view/onmouseout;
+        onkeypress view/onkeypress;
+        onkeydown view/onkeydown;
+        onkeyup view/onkeyup;
+      "
+  ><tal:block condition="view/value"
+               content="view/value"
     /></h1>
 </html>
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_content.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_content.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_existing_content.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_existing_content.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_field.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_field.py`

 * *Files 1% similar despite different names*

```diff
@@ -181,43 +181,43 @@
         # And then looking up the relative field tile:
         self.browser.open(
             "{}/@@plone.app.standardtiles.field?field={}".format(
                 self.content.absolute_url(),
                 "funky",
             )
         )
-        self.assertIn(
-            '<h1 id="form-widgets-funky" class="funky-widget', self.browser.contents
-        )
+        self.assertIn("<h1 ", self.browser.contents)
+        self.assertIn(' id="form-widgets-funky"', self.browser.contents)
+        self.assertIn(' class="funky-widget', self.browser.contents)
         self.assertIn(">Oh yeah, baby!</h1>", self.browser.contents)
 
         root = fromstring(self.browser.contents)
         nodes = root.xpath('//body//h1[@id="form-widgets-funky"]')
         self.assertEqual(len(nodes), 1)
         self.assertIn("funky-widget", nodes[0].attrib["class"].split())
         self.assertEqual("Oh yeah, baby!", nodes[0].text)
 
     def test_permissions(self):
         """Another thing that can be hinted in schemas is field-level
         permissions. That is, you might have a field within a schema that needs
         a special permission to be viewed, a pewrmission that might be stricter
-        than the permission neede to view the object.
+        than the permission needed to view the object.
 
         The ``topsecret`` field is an example, as you need to have the
         ``cmf.ModifyPortalContent`` permission to be able to see it.
 
         """
         # Let's first insert some value into it:
-        self.content.topsecret = "Santa Claus does not exist!"
+        self.content.topsecret = "Santa Clause does not exist!"
         transaction.commit()
 
         # And then let's try to invoke the tile via our browser. Let's keep
         # in mind we are logged out, so we should see an empty tile, because no
         # value should be made visible to normal user (which can be kids and
-        # really should not be spoiled about Santa Claus' identity).
+        # really should not be spoiled about Santa Clause' identity).
 
         self.browser.open(
             "{}/@@plone.app.standardtiles.field?field={}".format(
                 self.content.absolute_url(),
                 "topsecret",
             )
         )
@@ -240,20 +240,20 @@
         self.browser.open(
             "{}/@@plone.app.standardtiles.field?field={}".format(
                 self.content.absolute_url(),
                 "topsecret",
             )
         )
         self.assertIn('<span id="form-widgets-topsecret"', self.browser.contents)
-        self.assertIn(">Santa Claus does not exist!</span>", self.browser.contents)
+        self.assertIn(">Santa Clause does not exist!</span>", self.browser.contents)
 
         root = fromstring(self.browser.contents)
         nodes = root.xpath('//body//*[@id="form-widgets-topsecret"]')
         self.assertEqual(len(nodes), 1)
-        self.assertEqual("Santa Claus does not exist!", nodes[0].text)
+        self.assertEqual("Santa Clause does not exist!", nodes[0].text)
 
     def test_behavior_field(self):
         """Right now, we have always operated on fields that were, in Dexterity
         terms, onto the "main schema". But what about fields that are in
         behavior fields associated to the content type?
 
         The field tile can handle them as well, although the name's prefixed
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_head.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_head.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_layout.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_layout.py`

 * *Files 1% similar despite different names*

```diff
@@ -217,15 +217,15 @@
         lt.settings.always_show_selector = True
         transaction.commit()
 
         self.unprivileged_browser.open(
             self.portalURL + "/@@plone.app.standardtiles.languageselector"
         )
 
-        # langauge selector is empty by default in Plone 5
+        # language selector is empty by default in Plone 5
         self.assertNotIn("portal-languageselector", self.unprivileged_browser.contents)
 
         root = fromstring(self.unprivileged_browser.contents)
         nodes = root.xpath('//body//*[@id="portal-languageselector"]')
         self.assertEqual(len(nodes), 0)
 
         nodes = root.xpath('//body//*[@class="language-ca"]')
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_media.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_media.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,16 +6,14 @@
 from plone.app.standardtiles.html import HTMLTile
 from plone.app.standardtiles.testing import PASTANDARDTILES_FUNCTIONAL_TESTING
 from plone.app.testing import setRoles
 from plone.app.testing import TEST_USER_ID
 from plone.app.testing import TEST_USER_NAME
 from plone.app.testing import TEST_USER_PASSWORD
 from plone.namedfile import NamedFile
-from plone.namedfile import NamedImage
-from plone.protect.authenticator import createToken
 from plone.testing.zope import Browser
 from unittest import TestCase
 from urllib.parse import quote
 from zope.annotation import IAnnotations
 
 import io
 import os
@@ -198,15 +196,15 @@
             + quote(path)
             + "&portlet_title=TEST_RSS_TILE"
         )
 
         self.assertIn("TEST_RSS_TILE", self.unprivileged_browser.contents)
 
         self.assertIn(
-            '<a href="http://localhost:55440/plone/doc-one" class="tile">',
+            ' href="http://localhost:55440/plone/doc-one"',
             self.unprivileged_browser.contents,
         )
 
     def test_html_tile_unicode(self):
         tile = HTMLTile(self.portal, self.layer["request"])
         tile.__name__ = "test.html.tile"
         tile.data["content"] = "<p>Hello Wörld!</p>"
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/tests/test_setup.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/tests/test_setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-from plone import api
 from plone.app.standardtiles.testing import PASTANDARDTILES_INTEGRATION_TESTING
 from plone.registry.interfaces import IRegistry
 from Products.CMFPlone.utils import get_installer
 from zope.component import getUtility
 
 import unittest
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/upgrades.zcml` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/upgrades.zcml`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/utils.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/utils.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone/app/standardtiles/viewletmanager.py` & `plone.app.standardtiles-3.1.1/src/plone/app/standardtiles/viewletmanager.py`

 * *Files identical despite different names*

### Comparing `plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/PKG-INFO` & `plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plone.app.standardtiles
-Version: 3.1.0
+Version: 3.1.1
 Summary: Tiles for plone.app.blocks page composition
 Home-page: https://github.com/plone/plone.app.standardtiles
 Author: Rob Gietema
 Author-email: rob@fourdigits.nl
 License: GPL
 Keywords: tiles content plone
 Classifier: Development Status :: 5 - Production/Stable
@@ -58,14 +58,21 @@
 -------
 
 The project is licensed under the GPLv2.
 
 Changelog
 =========
 
+3.1.1 (2023-05-13)
+------------------
+
+- Fix boolean fields title/description/text to not be required.
+  [petschki]
+
+
 3.1.0 (2023-05-04)
 ------------------
 
 - Add option to enable the Eventlisting view (this expands recurring events).
   NOTE: The listing will only show Event types.
   [petschki]
 
@@ -403,15 +410,15 @@
 
 - Simplify basic viewlet proxy tiles.
   [jensens]
 
 - Enable coveralls and code analysis.
   [gforcada]
 
-- Adapt travis to all other mosaic realted packages.
+- Adapt travis to all other mosaic related packages.
   [gforcada]
 
 - Remove unused function.
   [gforcada]
 
 
 1.0 (2016-04-11)
```

### Comparing `plone.app.standardtiles-3.1.0/src/plone.app.standardtiles.egg-info/SOURCES.txt` & `plone.app.standardtiles-3.1.1/src/plone.app.standardtiles.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 CHANGES.rst
 LICENSE.GPL
 LICENSE.txt
-MANIFEST.in
 README.rst
-setup.cfg
+pyproject.toml
 setup.py
 src/plone/__init__.py
 src/plone.app.standardtiles.egg-info/PKG-INFO
 src/plone.app.standardtiles.egg-info/SOURCES.txt
 src/plone.app.standardtiles.egg-info/dependency_links.txt
 src/plone.app.standardtiles.egg-info/entry_points.txt
 src/plone.app.standardtiles.egg-info/namespace_packages.txt
```

