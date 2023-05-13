# Comparing `tmp/soca-0.0.1.tar.gz` & `tmp/soca-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "soca-0.0.1.tar", last modified: Wed Apr  5 20:01:54 2023, max compression
+gzip compressed data, was "soca-0.0.2.tar", last modified: Sat May 13 10:01:29 2023, max compression
```

## Comparing `soca-0.0.1.tar` & `soca-0.0.2.tar`

### file list

```diff
@@ -1,104 +1,105 @@
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    11357 2022-05-14 11:01:46.000000 soca-0.0.1/LICENSE
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       35 2022-10-18 09:05:27.000000 soca-0.0.1/MANIFEST.in
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    13432 2023-04-05 20:01:54.092735 soca-0.0.1/PKG-INFO
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    12812 2023-04-05 19:25:08.000000 soca-0.0.1/README.md
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      103 2022-05-14 11:01:46.000000 soca-0.0.1/pyproject.toml
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1077 2023-04-05 20:01:54.096735 soca-0.0.1/setup.cfg
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.084735 soca-0.0.1/src/
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.084735 soca-0.0.1/src/soca/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      534 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/__init__.py
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5371 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/__main__.py
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.088735 soca-0.0.1/src/soca/assets/
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     8956 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/assets/about.html
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    14093 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/app.js
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.088735 soca-0.0.1/src/soca/assets/img/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      460 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/back_arrow.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    54593 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/fi_logo.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1059 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/filter.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1866 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/github-default.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2561 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/help.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     8407 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/oeg_logo.gif
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    26590 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/soca-logo.ico
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    26590 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/soca-logo.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1777 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/sort.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    23522 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/img/upm_logo.png
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.088735 soca-0.0.1/src/soca/assets/language_icons/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2449 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/arduino.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1948 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/c++.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3517 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/c-sharp.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      588 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/c.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1936 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/clojure.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1317 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/coffeescript.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2507 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/css.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3140 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/go.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5933 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/groovy.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      288 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/haskell.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      415 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/html.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1477 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/java.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1101 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/javascript.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2621 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/lua.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1240 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/matlab.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1948 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/objectivec.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3095 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/perl.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1245 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/php.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1052 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/python.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1030 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/r.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2131 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/ruby.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      895 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/scala.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      473 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/shell.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1263 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/language_icons/swift.svg
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/src/soca/assets/repo_icons/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3613 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/acknowledgement.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1061 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/citation.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1656 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/copy.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2903 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/docker.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2913 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/documentation.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4113 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/doi.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      972 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/download.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2663 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/help.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1701 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/installation.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4390 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/license.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1357 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/notebook.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5241 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/ontology.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1356 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/owner.svg
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1133 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/paper.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      681 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/readme.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1428 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/releases.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1106 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/requirements.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2815 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/star.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3304 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/status.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2946 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/usage.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1307 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/watching.png
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     8756 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/repo_icons/web.png
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/src/soca/assets/scripts/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1001 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/scripts/copy_card.js
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5200 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/scripts/modals.js
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       79 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/scripts/tooltip.js
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4456 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/soca-card.css
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4710 2022-10-18 09:05:27.000000 soca-0.0.1/src/soca/assets/styles.css
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6539 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/assets/template.html
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/src/soca/commands/
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/__init__.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1910 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/create_config.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     7704 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/create_summary.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6559 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/extract_metadata.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     2713 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/fetch_repositories.py
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/src/soca/commands/portal/
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/__init__.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6034 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/card.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)    25462 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/metadata.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     4280 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/portal.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1256 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/scripts.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)      424 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/portal/styles.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1095 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/single_card.py
--rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6210 2023-04-05 19:25:08.000000 soca-0.0.1/src/soca/commands/upload_summary.py
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.084735 soca-0.0.1/src/soca.egg-info/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    13432 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/PKG-INFO
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3192 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/SOURCES.txt
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)        1 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/dependency_links.txt
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       43 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/entry_points.txt
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      172 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/requires.txt
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)        5 2023-04-05 20:01:54.000000 soca-0.0.1/src/soca.egg-info/top_level.txt
-drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 20:01:54.092735 soca-0.0.1/tests/
--rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    12492 2023-04-05 19:25:08.000000 soca-0.0.1/tests/test-scc.py
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.151864 soca-0.0.2/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    11357 2022-05-14 11:01:46.000000 soca-0.0.2/LICENSE
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       35 2022-10-18 09:05:27.000000 soca-0.0.2/MANIFEST.in
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    13565 2023-05-13 10:01:29.151864 soca-0.0.2/PKG-INFO
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    12983 2023-04-05 20:24:25.000000 soca-0.0.2/README.md
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      103 2022-05-14 11:01:46.000000 soca-0.0.2/pyproject.toml
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1051 2023-05-13 10:01:29.151864 soca-0.0.2/setup.cfg
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.123864 soca-0.0.2/src/
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.123864 soca-0.0.2/src/soca/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      534 2023-04-05 20:09:21.000000 soca-0.0.2/src/soca/__init__.py
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5374 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/__main__.py
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.127864 soca-0.0.2/src/soca/assets/
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     8961 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/assets/about.html
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    14095 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/assets/app.js
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.131864 soca-0.0.2/src/soca/assets/img/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      460 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/back_arrow.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    54593 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/fi_logo.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1059 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/filter.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1866 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/github-default.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2561 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/help.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     8407 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/oeg_logo.gif
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    26590 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/soca-logo.ico
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    26590 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/soca-logo.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1777 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/sort.svg
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)      462 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/assets/img/statIcon.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    23522 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/img/upm_logo.png
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.139864 soca-0.0.2/src/soca/assets/language_icons/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2449 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/arduino.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1948 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/c++.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3517 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/c-sharp.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      588 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/c.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1936 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/clojure.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1317 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/coffeescript.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2507 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/css.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3140 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/go.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5933 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/groovy.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      288 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/haskell.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      415 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/html.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1477 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/java.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1101 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/javascript.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2621 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/lua.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1240 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/matlab.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1948 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/objectivec.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3095 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/perl.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1245 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/php.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1052 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/python.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1030 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/r.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2131 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/ruby.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      895 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/scala.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      473 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/shell.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1263 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/language_icons/swift.svg
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.147864 soca-0.0.2/src/soca/assets/repo_icons/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3613 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/acknowledgement.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1061 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/citation.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1656 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/copy.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2903 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/docker.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2913 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/documentation.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4113 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/doi.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      972 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/download.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2663 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/help.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1701 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/installation.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4390 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/license.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1357 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/notebook.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5241 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/ontology.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1356 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/owner.svg
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1133 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/paper.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      681 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/readme.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1428 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/releases.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1106 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/requirements.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2815 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/star.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3304 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/status.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     2946 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/usage.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1307 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/watching.png
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     8756 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/repo_icons/web.png
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.147864 soca-0.0.2/src/soca/assets/scripts/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     1001 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/scripts/copy_card.js
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     5200 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/scripts/modals.js
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       79 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/scripts/tooltip.js
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4473 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/assets/soca-card.css
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     4710 2022-10-18 09:05:27.000000 soca-0.0.2/src/soca/assets/styles.css
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6633 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/assets/template.html
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.147864 soca-0.0.2/src/soca/commands/
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/__init__.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1910 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/create_config.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     8224 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/create_summary.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     7436 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/extract_metadata.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     2713 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/fetch_repositories.py
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.151864 soca-0.0.2/src/soca/commands/portal/
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/portal/__init__.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6033 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/portal/card.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)    28062 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/portal/metadata.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     4902 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/portal/portal.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1256 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/portal/scripts.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)      424 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/portal/styles.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     1095 2023-04-05 19:25:08.000000 soca-0.0.2/src/soca/commands/single_card.py
+-rwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)     6394 2023-05-13 09:59:50.000000 soca-0.0.2/src/soca/commands/upload_summary.py
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.127864 soca-0.0.2/src/soca.egg-info/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    13565 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/PKG-INFO
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)     3225 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/SOURCES.txt
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)        1 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/dependency_links.txt
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)       43 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/entry_points.txt
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)      183 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/requires.txt
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)        5 2023-05-13 10:01:29.000000 soca-0.0.2/src/soca.egg-info/top_level.txt
+drwxrwxr-x   0 dgarijo   (1000) dgarijo   (1000)        0 2023-05-13 10:01:29.151864 soca-0.0.2/tests/
+-rw-rw-r--   0 dgarijo   (1000) dgarijo   (1000)    16720 2023-05-13 09:59:50.000000 soca-0.0.2/tests/test-scc.py
```

### Comparing `soca-0.0.1/LICENSE` & `soca-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/PKG-INFO` & `soca-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: soca
-Version: 0.0.1
+Version: 0.0.2
 Summary: A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 Home-page: https://github.com/oeg-upm/soca
-Author: Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzaled, Daniel Garijo
-Author-email: miguel.arroyo.marquez@alumnos.upm.es, daniel.garijo@upm.es
+Author: Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzalez, Daniel Garijo
+Author-email: daniel.garijo@upm.es
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 
 # Software Catalog Creator (soca)
 
-[![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
+[![DOI](https://zenodo.org/badge/402041422.svg)](https://zenodo.org/badge/latestdoi/402041422) [![PyPI](https://badge.fury.io/py/soca.svg)](https://badge.fury.io/py/soca) [![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
 
 <img src="doc/images/soca-logo.png" alt="logo" width="150"/>
 
 A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 
 ## Sample result
```

### Comparing `soca-0.0.1/README.md` & `soca-0.0.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 
 # Software Catalog Creator (soca)
 
-[![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
+[![DOI](https://zenodo.org/badge/402041422.svg)](https://zenodo.org/badge/latestdoi/402041422) [![PyPI](https://badge.fury.io/py/soca.svg)](https://badge.fury.io/py/soca) [![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
 
 <img src="doc/images/soca-logo.png" alt="logo" width="150"/>
 
 A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 
 ## Sample result
```

### Comparing `soca-0.0.1/setup.cfg` & `soca-0.0.2/setup.cfg`

 * *Files 16% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 [metadata]
 name = soca
 version = attr: soca.__version__
-author = Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzaled, Daniel Garijo
-author_email = miguel.arroyo.marquez@alumnos.upm.es, daniel.garijo@upm.es
+author = Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzalez, Daniel Garijo
+author_email = daniel.garijo@upm.es
 description = A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/oeg-upm/soca
 classifiers = 
 	Programming Language :: Python :: 3
 	Operating System :: OS Independent
@@ -31,14 +31,15 @@
 	influxdb-client
 	configparser
 	DateTime
 	pathlib
 	nltk
 	configparser
 	influxdb_client
+	validators
 
 [options.packages.find]
 where = src
 
 [options.entry_points]
 console_scripts = 
 	soca = soca.__main__:cli
```

### Comparing `soca-0.0.1/src/soca/__init__.py` & `soca-0.0.2/src/soca/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import pathlib, sys, os
 
-__version__ = "0.0.1"
+__version__ = "0.0.2"
 
 # Project base path
 base_dir = str(pathlib.Path(__file__).parent.resolve())
 
 class HiddenPrints:
     def __enter__(self):
         self._original_stdout = sys.stdout
```

### Comparing `soca-0.0.1/src/soca/__main__.py` & `soca-0.0.2/src/soca/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -25,15 +25,15 @@
 #TODO
 @cli.command()
 def configure():
     """This creates a ~/.soca/configure.ini file"""
     #TODO defaults check
     url = click.prompt("URL to database",default = "http://localhost:8086")
     bucket = click.prompt("Bucket", default = "my-bucket")
-    org = click.prompt("Organisation",default = "test1")
+    org = click.prompt("Organisation",default = "org_name")
     token = click.prompt("Token", default = "")
     if len(token) == 0:
         click.echo("No token given, please enter token or press enter")
         token = click.prompt("Token", default = "")
     try:
         from soca.commands import create_config
```

### Comparing `soca-0.0.1/src/soca/assets/about.html` & `soca-0.0.2/src/soca/assets/about.html`

 * *Files 1% similar despite different names*

```diff
@@ -55,15 +55,15 @@
 			and <a href="https://github.com/SoftwareUnderstanding/inspect4py">inspect4py</a>,
 			enabling end-users to filter and sort all the repositories in multiple ways.
 
 		</p>
 		<h3 style="margin-bottom: 1rem;">Team</h3>
 		<p style="text-align: justify;">
 			<ul>
-				<li><strong>Daniel Rodríguez Mariblanca</strong>: Developer and designer of the portal and soca.
+				<li><strong>Daniel Rodr&iacuteguez Mariblanca</strong>: Developer and designer of the portal and SOCA.
 					<i>Universidad Polit&eacute;cnica de Madrid, ETSIINF</i> (Computer Engineering, Business Administration and Management).</li>
 				<li><strong>Miguel Arroyo M&aacute;rquez</strong> Developer and Designer for SOCA and SOCA-Dash. 
 					<i>Universidad Polit&eacute;cnica de Madrid, ETSIINF</i></li>
 				<li><strong>Daniel Garijo</strong>: mentor. Distinguished researcher at <i>Universidad Polit&eacute;cnica de Madrid, ETSIINF</i></li>
 				<li><strong>Esteban Gonz&aacute;lez</strong>: mentor. PhD student at <i>Universidad Polit&eacute;cnica de Madrid, ETSIINF</i></li>
 				<li><strong>Oscar Corcho</strong>: mentor. Full professor at <i>Universidad Polit&eacute;cnica de Madrid, ETSIINF</i></li>
 		</p>
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

#### html2text {}

```diff
@@ -54,17 +54,17 @@
 GitHub. The main objective of this web is to give visibility to researchers by
 showcasing their work in a minimalistic portal.
 
 Scc extracts most of the displayed metadata with the help of somef and
 inspect4py, enabling end-users to filter and sort all the repositories in
 multiple ways.
 **** Team ****
-    * Daniel RodrÃ­guez Mariblanca: Developer and designer of the portal and
-      soca. Universidad Politécnica de Madrid, ETSIINF (Computer Engineering,
-      Business Administration and Management).
+    * Daniel Rodr&iacuteguez Mariblanca: Developer and designer of the portal
+      and SOCA. Universidad Politécnica de Madrid, ETSIINF (Computer
+      Engineering, Business Administration and Management).
     * Miguel Arroyo Márquez Developer and Designer for SOCA and SOCA-Dash.
       Universidad Politécnica de Madrid, ETSIINF
     * Daniel Garijo: mentor. Distinguished researcher at Universidad
       Politécnica de Madrid, ETSIINF
     * Esteban González: mentor. PhD student at Universidad Politécnica de
       Madrid, ETSIINF
     * Oscar Corcho: mentor. Full professor at Universidad Politécnica de
```

### Comparing `soca-0.0.1/src/soca/assets/app.js` & `soca-0.0.2/src/soca/assets/app.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -293,15 +293,15 @@
     const filteredCards = cards.filter(card => {
         return (card.name.toLowerCase().includes(usr_query) || card.description.toLowerCase().includes(usr_query)) &&
             (
                 ((state_acknowledgement) ? card.acknowledgement : true) &&
                 ((state_citation) ? card.citation : true) &&
                 ((state_docker) ? card.hasBuildFile : true) &&
                 ((state_documentation) ? card.hasDocumentation : true) &&
-                ((state_identifier) ? card.identifier : true) &&
+                ((state_identifier) ? card.hasIdentifier : true) &&
                 ((state_status) ? card.repoStatus : true) &&
                 ((state_download) ? card.downloadUrl : true) &&
                 ((state_license) ? card.license : true) &&
                 ((state_notebook) ? card.hasExecutableNotebook : true) &&
                 ((state_paper) ? card.paper : true) &&
                 ((state_ontology) ? card.isOntology : true) &&
                 ((state_web) ? card.isWeb : true) &&
```

### Comparing `soca-0.0.1/src/soca/assets/img/fi_logo.png` & `soca-0.0.2/src/soca/assets/img/fi_logo.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/filter.svg` & `soca-0.0.2/src/soca/assets/img/filter.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/github-default.svg` & `soca-0.0.2/src/soca/assets/img/github-default.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/help.png` & `soca-0.0.2/src/soca/assets/img/help.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/oeg_logo.gif` & `soca-0.0.2/src/soca/assets/img/oeg_logo.gif`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/soca-logo.ico` & `soca-0.0.2/src/soca/assets/img/soca-logo.ico`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/soca-logo.png` & `soca-0.0.2/src/soca/assets/img/soca-logo.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/sort.svg` & `soca-0.0.2/src/soca/assets/img/sort.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/img/upm_logo.png` & `soca-0.0.2/src/soca/assets/img/upm_logo.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/arduino.svg` & `soca-0.0.2/src/soca/assets/language_icons/arduino.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/c++.svg` & `soca-0.0.2/src/soca/assets/language_icons/c++.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/c-sharp.svg` & `soca-0.0.2/src/soca/assets/language_icons/c-sharp.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/c.svg` & `soca-0.0.2/src/soca/assets/language_icons/c.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/clojure.svg` & `soca-0.0.2/src/soca/assets/language_icons/clojure.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/coffeescript.svg` & `soca-0.0.2/src/soca/assets/language_icons/coffeescript.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/css.svg` & `soca-0.0.2/src/soca/assets/language_icons/css.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/go.svg` & `soca-0.0.2/src/soca/assets/language_icons/go.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/groovy.svg` & `soca-0.0.2/src/soca/assets/language_icons/groovy.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/java.svg` & `soca-0.0.2/src/soca/assets/language_icons/java.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/javascript.svg` & `soca-0.0.2/src/soca/assets/language_icons/javascript.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/lua.svg` & `soca-0.0.2/src/soca/assets/language_icons/lua.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/matlab.svg` & `soca-0.0.2/src/soca/assets/language_icons/matlab.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/objectivec.svg` & `soca-0.0.2/src/soca/assets/language_icons/objectivec.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/perl.svg` & `soca-0.0.2/src/soca/assets/language_icons/perl.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/php.svg` & `soca-0.0.2/src/soca/assets/language_icons/php.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/python.svg` & `soca-0.0.2/src/soca/assets/language_icons/python.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/r.svg` & `soca-0.0.2/src/soca/assets/language_icons/r.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/ruby.svg` & `soca-0.0.2/src/soca/assets/language_icons/ruby.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/scala.svg` & `soca-0.0.2/src/soca/assets/language_icons/scala.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/language_icons/swift.svg` & `soca-0.0.2/src/soca/assets/language_icons/swift.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/acknowledgement.png` & `soca-0.0.2/src/soca/assets/repo_icons/acknowledgement.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/citation.png` & `soca-0.0.2/src/soca/assets/repo_icons/citation.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/copy.svg` & `soca-0.0.2/src/soca/assets/repo_icons/copy.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/docker.png` & `soca-0.0.2/src/soca/assets/repo_icons/docker.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/documentation.png` & `soca-0.0.2/src/soca/assets/repo_icons/documentation.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/doi.png` & `soca-0.0.2/src/soca/assets/repo_icons/doi.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/download.png` & `soca-0.0.2/src/soca/assets/repo_icons/download.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/help.png` & `soca-0.0.2/src/soca/assets/repo_icons/help.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/installation.png` & `soca-0.0.2/src/soca/assets/repo_icons/installation.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/license.png` & `soca-0.0.2/src/soca/assets/repo_icons/license.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/notebook.png` & `soca-0.0.2/src/soca/assets/repo_icons/notebook.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/ontology.png` & `soca-0.0.2/src/soca/assets/repo_icons/ontology.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/owner.svg` & `soca-0.0.2/src/soca/assets/repo_icons/owner.svg`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/paper.png` & `soca-0.0.2/src/soca/assets/repo_icons/paper.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/readme.png` & `soca-0.0.2/src/soca/assets/repo_icons/readme.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/releases.png` & `soca-0.0.2/src/soca/assets/repo_icons/releases.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/requirements.png` & `soca-0.0.2/src/soca/assets/repo_icons/requirements.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/star.png` & `soca-0.0.2/src/soca/assets/repo_icons/star.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/status.png` & `soca-0.0.2/src/soca/assets/repo_icons/status.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/usage.png` & `soca-0.0.2/src/soca/assets/repo_icons/usage.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/watching.png` & `soca-0.0.2/src/soca/assets/repo_icons/watching.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/repo_icons/web.png` & `soca-0.0.2/src/soca/assets/repo_icons/web.png`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/scripts/copy_card.js` & `soca-0.0.2/src/soca/assets/scripts/copy_card.js`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/scripts/modals.js` & `soca-0.0.2/src/soca/assets/scripts/modals.js`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/soca-card.css` & `soca-0.0.2/src/soca/assets/soca-card.css`

 * *Files 1% similar despite different names*

```diff
@@ -29,13 +29,13 @@
 .soca-card .flex-horizontal{display: flex; align-items: center; flex-direction: row;}
 .soca-card .float-right{justify-content: flex-end;}
 .soca-card .grey-color-svg{filter: brightness(0) saturate(100%) invert(26%) sepia(0%) saturate(9%) hue-rotate(190deg) brightness(93%) contrast(100%);}
 .soca-card .title:hover{text-decoration: underline;}
 .soca-card .ref-repo-icons{flex-wrap: wrap;}
 .soca-card .icon-wrapper {cursor: pointer; width: 2rem; display: flex; align-items: center; justify-content: center;}
 .highlight *{font-family: monospace; font-size: large;}
-.modal {display: none;position: fixed;z-index: 1;padding-top: 20vh;left: 0;top: 0;width: 100%;height: 100%;overflow: auto;background-color: rgb(0,0,0);background-color: rgba(0,0,0,0.4);}
+.modal {display: none;position: fixed;z-index: 1;padding-top: 20vh;left: 0;top: 0;width: 100%;height: 100%;overflow: auto;background-color: rgb(0,0,0);background-color: rgba(0,0,0,0.4); cursor: default;}
 .modal-content {background-color: #e0e0e0;margin: auto;padding: 20px;border: 0px;width: 90%;max-width: 40rem;border-radius: 1rem;}
 .modal-on{display: block;}
 .close {color: #3e3e3e;float: right;font-size: 28px;font-weight: bold;position: relative;bottom: 0.8rem;}
 .close:hover, .close:focus {  color: #000;  text-decoration: none; cursor: pointer;}
 .soca-card .repo-type{height: 1.4rem; margin-left: 0.2rem; margin-right: 0.2rem; cursor: pointer;}
```

### Comparing `soca-0.0.1/src/soca/assets/styles.css` & `soca-0.0.2/src/soca/assets/styles.css`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/assets/template.html` & `soca-0.0.2/src/soca/assets/template.html`

 * *Files 2% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 </head>
 <body>
 <nav class="navbar">
 	<div class="navbar-inside">
 		<h2 id="nav-title">Software Catalog</h2>
 		<input id="searchBar" placeholder="Search for repositories..." title="Type in a repository" type="text"/>
 		<div data-toggle="tooltip" data-placement="right" title="About page"><a href="about.html"><img src="img/help.png" class="grey-color-svg" style="height: 2rem; margin-left: 1rem;"></a></div>
-		<div data-toggle="tooltip" data-placement="right" title="SOCA Dashboard Analytics"><a href="https://dashboards-software.oeg.fi.upm.es/d/FX3TNka4k/prototype?orgId=1&from=now-7d&to=now"><img src="img/statIcon.svg" class="grey-color-svg" style="height: 2rem; margin-left: 1rem;"></a></div>
+		<div data-toggle="tooltip" data-placement="right" title="SOCA Dashboard Analytics"><a href="https://dashboards-software.oeg.fi.upm.es/d/FX3TNka4k/prototype?orgId=1&from=now-6M&to=now&var-organisation=oeg-upm&var-SOCA_Version=0.0.2&var-SOMEF_Version=0.9.3&kiosk" target="_blank"><img src="img/statIcon.svg" class="grey-color-svg" style="height: 2rem; margin-left: 1rem;"></a></div>
 	</div>
 	
 	<div class="filters-wrapper">
 		<div class="filters">
 			<div data-toggle="tooltip" data-placement="bottom" title="Sort"><img src="img/sort.svg" class="sort-filter-icon"/></div>
 			<div class="sort">
 				<div data-toggle="tooltip" data-placement="bottom" title="Sort by title" class="sort-box" id="title"><p>Title</p></div>
```

### Comparing `soca-0.0.1/src/soca/commands/create_config.py` & `soca-0.0.2/src/soca/commands/create_config.py`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/commands/create_summary.py` & `soca-0.0.2/src/soca/commands/create_summary.py`

 * *Files 8% similar despite different names*

```diff
@@ -37,14 +37,15 @@
     output['CFF_file'] = 0
     output['no_citation'] = 0
     output['released'] = {'<2 MONTHS': 0, 'LONGER': 0}
     output['_soca_version'] = soca_ver
     output['_somef_version'] = somef_ver
     output['_timestamp'] = __json_serial(datetime.now())
     output['num_repos'] = 0
+    output['num_ontologies']= 0
     output['language_count'] = {}
 
 
 
 #functions below to identify good practices
 #TODO look into correct identifiers
 def __findId(json_obj):
@@ -132,15 +133,15 @@
     if not json_obj['readmeUrl']:
         output['num_no_readme'] += 1
     else:
         output['num_with_readme'] +=1
         if json_obj['installation']:
             output['num_with_installation'] +=1
         if json_obj['acknowledgement']:
-            output['num_with_acknowledgment'] +=1
+            output['num_with_acknowledgement'] +=1
         if json_obj['requirement']:
             output['num_with_requirement'] +=1
         if json_obj['description']:
             output['num_with_description'] +=1
 
 
 def __findCitation(json_obj):
@@ -191,30 +192,40 @@
     #updates the list of organisations
     try:
 
         json_array = __open_Json(directory_org_data)
         if not os.path.exists(outFile):
             os.makedirs(outFile)
         for item in json_array:
+            is_ontology = safe_dic(item, 'isOntology')
+            ontologies_dict = safe_dic(item, 'ontologies')
+            if is_ontology or (ontologies_dict is not None and len(ontologies_dict) > 0):
+                languages = safe_dic(item,'languages')
+                if not languages:
+                    output['num_ontologies'] += 1
+                    continue
+                elif any(lang.lower() in ['html', 'turtle', 'owl', 'rdf', 'rml'] for lang in languages):
+                    output['num_ontologies'] += 1
+                    continue
             if item['hasDocumentation']:
                 output['has_documentation'] = output['has_documentation'] + 1
             #citation
             __findCitation(item)
             # finds licenses
-            output['licenses'][__findLicense(item)] = output['licenses'][__findLicense(item)] + 1
+            output['licenses'][__findLicense(item)] += 1
             # finds identifiers
             __findId(item)
             # gives readme evaluation
             __readme_analysis(item)
             # release time
-            output['released'][__last_update(item)] = output['released'][__last_update(item)] + 1
+            output['released'][__last_update(item)] += 1
             # adds org_name
             output['_org_name'] = item['owner']
             output['num_repos'] += 1
-            #licenses
+            #Counts Languages used
             __languages(item)
 
         # saves dictionary to json file
         with open(outFile + "/" + item['owner'] + "_summary.json", 'w+') as out_file:
             json.dump(output, out_file, sort_keys=True, indent=4,
                       ensure_ascii=False)
             #console outputs
```

### Comparing `soca-0.0.1/src/soca/commands/extract_metadata.py` & `soca-0.0.2/src/soca/commands/extract_metadata.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 import csv
 import json
 import os
+from os import path
 from progressbar import progressbar
 from somef.somef_cli import cli_get_data
-
-
-import os
-from os import path
 from soca import HiddenPrints
 import subprocess
 import shutil
 import traceback
+import datetime
+
+import requests
+import pprint
 
 
 def extract(repos_csv, output, use_inspect4py, verbose):
     """
     @Param repos_csv: input file from the fetch command, A list of github urls
     @Param output: defined output file
     @Param use_inspect4py: Bool to indicate desire to use inspect4py
@@ -47,38 +48,43 @@
         ##################################################################
         # somef
 
         try:
             print(f"Extracting metadata from {repo_url}")
             if not verbose:
                 with HiddenPrints():
-                    #metadata = cli_get_data(0.9, False, repo_url, keep_tmp=git_clone_dir)
-                    metadata = cli_get_data(0.9, False, repo_url, None, False, False, False, keep_tmp=git_clone_dir)
+                    metadata = cli_get_data(0.9, False, repo_url, keep_tmp=git_clone_dir)
+                    #metadata = cli_get_data(0.9, False, repo_url, None, False, False, False, keep_tmp=git_clone_dir)
+                    
             else:
-                #metadata = cli_get_data(0.9, False, repo_url, keep_tmp=git_clone_dir)
-                metadata = cli_get_data(0.9, False, repo_url, None, False, False, False, keep_tmp=git_clone_dir)
+                metadata = cli_get_data(0.9, False, repo_url, keep_tmp=git_clone_dir)
+                #metadata = cli_get_data(0.9, False, repo_url, None, False, False, False, keep_tmp=git_clone_dir)
             if not metadata:
-                print(f'ERROR: {repo_url} is down, skipping it...')
+                #print(f'ERROR: {repo_url} is down, skipping it...')
+                print(f'ERROR: unable to extract from {repo_url}, skipping it...')
                 failed_repos.append(repo_url)
                 continue
         except KeyboardInterrupt:
             exit()
         except Exception as e:
             # traceback.print_exc()
-            print(f"ERROR: Could not extract metadata from {repo_url}")
+            try:
+                continue
+            except:
+                print(f"ERROR: Could not extract metadata from {repo_url}")
+                continue
             print(str(e))
             failed_repos.append(repo_url)
             continue
 
         ##################################################################
         # inspect4py
 
         if use_inspect4py and 'programming_languages' in metadata.results\
                 and any(lang['result']['value'] == "Python" for lang in metadata.results['programming_languages']):
-            print("hello")
             try:
                 metadata.results["inspect4py"] = {}
 
                 if verbose:
                     subprocess.call(
                         f'inspect4py -i {git_clone_dir} -o {output}/inspect4py_tmp -si',
                         shell=True
@@ -147,23 +153,38 @@
         #       traceback.print_exc()
         #       print(f"ERROR: Could not run XX tool for {repo_url}")
         #       failed_repos.append(repo_url)
         #       continue
         #
 
         # Save metadata
+        # repo_full_name = (repo_url[19:]).replace("/", "_").replace(".", "-")
+        # with open(f"{output}/{repo_full_name}.json", 'w') as repo_metadata:
+        #     json.dump(metadata.results, repo_metadata, indent=4)
         repo_full_name = (repo_url[19:]).replace("/", "_").replace(".", "-")
-        with open(f"{output}/{repo_full_name}.json", 'w') as repo_metadata:
+        today = datetime.date.today().strftime("%Y-%m-%d")
+        with open(f"{output}/{repo_full_name}_{today}.json", 'w') as repo_metadata:
             json.dump(metadata.results, repo_metadata, indent=4)
 
     if len(failed_repos_i4p) > 0:
         print("ERROR: inspect4py could not be ran in the following repo/s:")
         for fr in failed_repos_i4p:
             print(fr)
 
     if len(failed_repos) > 0:
         print("ERROR: metadata could not be extracted from the following repo/s:")
         for fr in failed_repos:
             print(fr)
 
     print(
         f"\n✅ Successfully extracted metadata from ({len(repos_url) - len(failed_repos)}/{len(repos_url)}) repositories.")
+
+#This function is to enable the extraction of sufficient information for the creation of a card of a repository without
+#readme
+#This is due to somef not generating any json if the repository does not have a readme
+#This may be fixed in future as there is an issue open. Hence TODO
+
+# def _no_readme():
+#     try:
+#         next
+#     except Exception as e:
+#         print(str(e))
```

### Comparing `soca-0.0.1/src/soca/commands/fetch_repositories.py` & `soca-0.0.2/src/soca/commands/fetch_repositories.py`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/commands/portal/card.py` & `soca-0.0.2/src/soca/commands/portal/card.py`

 * *Files 1% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 def cards_data_dump(repo_metadata_dir):
 
     cards_data = []
 #TODO change
     #add possible "final release"
     for file in os.listdir(os.fsencode(repo_metadata_dir)):
         filename = os.fsdecode(file)
-        if filename.endswith(".json"): 
+        if filename.endswith(".json"):
             with open(f"{repo_metadata_dir}/{filename}") as json_metadata:
                 print(f"Creating card for '{filename}'")
                 repo_metadata = json.load(json_metadata)
                 md = metadata.metadata(repo_metadata_dir, repo_metadata)
                 citations = md.citations()
                 print(md.identifier())
                 cards_data.append({
```

### Comparing `soca-0.0.1/src/soca/commands/portal/metadata.py` & `soca-0.0.2/src/soca/commands/portal/metadata.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 import re
 import sys
 from pygments import highlight
 from pygments.lexers.scdoc import ScdocLexer
 from pygments.formatters import HtmlFormatter
 import mistune
 import os
+#from cffconvert import Citation
 #from cffconvert.cli import cli as cff2bibcli
 
 class metadata(object):
 
     def __init__(self, repo_metadata_dir, repo_metadata, embedded = False):
         self.repo_metadata_dir = os.path.abspath(repo_metadata_dir)
         self.md = repo_metadata
@@ -123,18 +124,19 @@
                             <img src="{self.base}repo_icons/readme.png" 
                             class="repo-icon" 
                             {self.add_tooltip('bottom','Readme')}>
                         </a>""")
 
         license = self.license()
         if license:
+
             html += self.icon_wrapper(
                 icon_html = f"""<img src="{self.base}repo_icons/license.png" 
                             class="repo-icon"
-                            {self.add_tooltip('bottom',f'License: {license["name"]}')}>
+                            {self.add_tooltip('bottom',f'License: {safe_dic(license,"name")}')}>
                             """,
                 modal_html= self.modal(
                     title = 'License',
                     body = self.html_license(license),
                     markdown_translation=False),
                 other_field = f'data-url="{safe_dic(license,"url")}"',
                 extra_class = 'ref-license' 
@@ -173,24 +175,29 @@
                                 <img src="{self.base}repo_icons/paper.png" 
                                 class="repo-icon" 
                                 {self.add_tooltip('bottom',paper.title_paper)}>
                         </a>""")
         #TODO check ScdocLexer
         citations = self.citations()
         if citations:
+            citation = "No Citation Indicated"
             formatter = HtmlFormatter(linenos=False, full=True, style='friendly')
             #TODO once fixed turn to if, elif, else  so that it prioritises CFF (converted to bibtex format)
             if 'cff' in citations:
-                #TODO
+                # try:
+                #     cite = Citation(cffstr=safe_dic(citations,"cff"))
+                #     citation = cite.as_bibtex()
+                # except:
                 pass
             if 'bibtex' in citations:
-                citation = citations['bibtex']
+                citation = safe_dic(citations,"bibtex")
             else:
                 try:
                     citation = citations['citation'][0]
+                    #citation = safe_list(safe_dic(citations,citation),0)
                 except Exception as e:
                     print(str(e))
             html += self.icon_wrapper(
                 icon_html = f"""<img src="{self.base}repo_icons/citation.png" 
                             class="repo-icon" 
                             {self.add_tooltip('bottom',f"Citation")}>""",
                 modal_html = self.modal(
@@ -275,36 +282,48 @@
                     title = 'Help',
                     body = help))
 
         hasDocumentation = self.hasDocumentation()
         if hasDocumentation:
             if len(hasDocumentation) > 1:
                 #mk_list = "\n".join([f'* <{d}>' if ('http' in d and not ' ' in d) else f'* {d}' for d in hasDocumentation])
+
                 mk_list = "\n".join([
                     f'* <{safe_dic(safe_dic(d, "result"), "value")}>' if (
-                                'http' in safe_dic(safe_dic(d, "result"), "value") and ' ' not in safe_dic(
-                            safe_dic(d, "result"), "value"))
+                                 self._is_valid_url(safe_dic(safe_dic(d, "result"), "value")))
                     else f'* {safe_dic(safe_dic(d, "result"), "value")}' for d in hasDocumentation
                 ])
 
                 html += self.icon_wrapper(
                     icon_html = f"""<img src="{self.base}repo_icons/documentation.png" 
                             class="repo-icon" 
                             {self.add_tooltip('bottom',"Documentation")}>""",
 
                     modal_html = self.modal(
                         title = 'Documentation',
                         body = mk_list))
             else:
-                html += self.icon_wrapper(
-                        icon_html = f"""<a href="{hasDocumentation[0]}" target="_blank" class="repo-icon">
-                                <img src="{self.base}repo_icons/documentation.png" 
+                doc = safe_dic(safe_dic(safe_list(hasDocumentation,0),'result'),'value')
+                if self._is_valid_url(doc):
+                    html += self.icon_wrapper(
+                        icon_html=f"""<a href="{doc}" target="_blank" class="repo-icon">
+                                                    <img src="{self.base}repo_icons/documentation.png" 
+                                                    class="repo-icon" 
+                                                    {self.add_tooltip('bottom', 'Documentation')}>
+                                                </a>""")
+                else:
+                    html += self.icon_wrapper(
+                        icon_html=f"""<img src="{self.base}repo_icons/documentation.png" 
                                 class="repo-icon" 
-                                {self.add_tooltip('bottom','Documentation')}>
-                            </a>""")
+                                {self.add_tooltip('bottom', 'Documentation')}>""",
+
+                        modal_html=self.modal(
+                            title='Documentation',
+                            body=f'{doc}'))
+
 
         acknowledgement =  self.acknowledgement()
         if acknowledgement:
             html += self.icon_wrapper(
 
                 icon_html = f"""<img src="{self.base}repo_icons/acknowledgement.png" 
                         class="repo-icon" 
@@ -324,14 +343,24 @@
                             class="repo-icon" 
                             {self.add_tooltip('bottom','Download')}>
                         </a>"""
                 )
 
         return html
 
+    def _is_valid_url(self,url):
+        """Private function to check if a string is a valid URL."""
+        import re
+
+        # Regular expression to match a valid URL
+        url_regex = re.compile(r"^https?://[^\s/$.?#].[^\s]*$")
+
+        # Check if the input string matches the URL regex
+        return bool(url_regex.match(url))
+
     # HTML helper ##################################################
 
     
     def add_tooltip(self, placement, tooltip_text):
         """Supported placements: ['bottom', 'up', 'right', 'left']"""
         return f'''data-toggle="tooltip" data-placement="{placement}" title="{tooltip_text}" alt="{tooltip_text}"'''
     
@@ -356,15 +385,24 @@
                             <div style="margin-bottom: 1rem; overflow: auto;">{body}</div>
                         </div>
                     </div>"""
 
 
     # Metadata ##################################################
     def last_release(self):
-        return safe_dic(safe_dic(self.releases()[0],'result'),'name') if self.n_releases() !=0 else ''
+        if self.n_releases() != 0:
+            if not safe_dic(safe_dic(safe_list(self.releases(),0),'result'),'name'):
+                if (tag:=safe_dic(safe_dic(safe_list(self.releases(),0),'result'),'tag')):
+                    return tag
+                else:
+                    return "Missing Descriptors"
+            return safe_dic(safe_dic(safe_list(self.releases(),0),'result'),'name')
+        else:
+            return ''
+        #return safe_dic(safe_dic(safe_list(self.releases(),0),'result'),'name') if self.n_releases() != 0 else ''
 
     #TODO
     def repo_type(self):
 
         # inspect4py
         ######################
 
@@ -449,22 +487,21 @@
     def identifier(self):
         return safe_dic(safe_dic(safe_list(safe_dic(self.md,'identifier'),0),'result'),'value')
     def status(self):
         return safe_dic(self.md,'repository_status')
 
 
     def acknowledgement(self):
-        return safe_dic(safe_list(safe_dic(self.md,'acknowlegement'),0),'value')
+        return safe_dic(safe_dic(safe_list(safe_dic(self.md,'acknowledgement'),0),'result'),'value')
 
     def hasDocumentation(self):
         docList = safe_dic(self.md, 'documentation')
         return docList if docList else None
 
     def requirements(self):
-
         reqs = safe_dic(self.md,'requirements')
         if not reqs:
             return None
         return "\n".join([safe_dic(safe_dic(d,'result'),'value') for d in reqs])
 
     def installation(self):
         inst = safe_dic(self.md,'installation')
@@ -520,18 +557,37 @@
 
         if not description:
             description = safe_dic(safe_dic(safe_list(all_descriptions,0),'result'),'value')
             if not description:
                 description = 'No description available yet.'
 
         return description
-    
 
     def license(self):
-        return safe_dic(safe_list(safe_dic(self.md,'license'),0),'result')
+        license = safe_dic(safe_list(safe_dic(self.md, 'license'), 0), 'result')
+        if (typ := safe_dic(license, "type")) and ((typ == "File_dump") or (typ == "Text_excerpt")):
+            self._find_license_name(license)
+            return license
+        else:
+            return license
+
+
+    def _find_license_name(self, license):
+        find_name = safe_dic(license, "value")
+        if 'Apache' in find_name:
+            license['name'] = 'Apache License 2.0'
+            license['url'] = 'https://api.github.com/licenses/apache-2.0'
+        elif 'MIT' in find_name:
+            license['name'] = 'MIT License'
+            license['url'] = 'https://api.github.com/licenses/MIT'
+        elif 'GPL' in find_name:
+            license['name'] = 'GNU General Public License v3.0'
+            license['url'] = 'https://api.github.com/licenses/gpl-3.0'
+        else:
+            license['name'] = 'Other'
 
     def last_update(self):
         result = safe_dic(safe_list(safe_dic(self.md,'date_updated'),0),'result')
         date_modified_str = of_correctType(result,'Date')[:-1]
         date_modified = datetime.strptime(date_modified_str, '%Y-%m-%dT%H:%M:%S')
         return date_modified
 
@@ -585,15 +641,17 @@
             match type:
                 case 'cff':
                     citations['cff'] = c['result']['value']
                 case 'bibtex':
                     citations['bibtex'] = c['result']['value']
                 case _:
                     continue
-        return citations if len(citations) > 0 else None
+        #return citations if len(citations) > 0 else None
+        test = len(citations)
+        return citations if bool(citations) else None
 
     # Originally citations Took the ver8 somef "regular expression" output and would create a list of excerpts
 
     def paper(self):
         citations = safe_dic(self.citations(),'citation')
         p = []
         if citations:
@@ -620,15 +678,15 @@
         return list[i]
     except:
         return None
 def of_correctType(result, ofType):
     if safe_dic(result, 'type') == ofType:
         return safe_dic(result, 'value')
     else:
-        raise Exception("not of correct %s type" % ofType)
+        raise Exception("not of correct %s type" %ofType)
 
 class citation_parser(object):
 
     def __init__(self, citation) -> None:
         self.link_paper = re.search('url[ ]*=[ ]*{(.*)}', citation)
         if self.link_paper:
             self.link_paper = self.link_paper.group(1)
```

### Comparing `soca-0.0.1/src/soca/commands/portal/portal.py` & `soca-0.0.2/src/soca/commands/portal/portal.py`

 * *Files 6% similar despite different names*

```diff
@@ -112,18 +112,31 @@
 
 def list_owners(repo_metadata_dir):
 
     owners = []
 
     for file in os.listdir(os.fsencode(repo_metadata_dir)):
         filename = os.fsdecode(file)
-        if filename.endswith(".json"): 
+        if filename.endswith(".json"):
             with open(f"{repo_metadata_dir}/{filename}") as json_metadata:
                 repo_metadata = json.load(json_metadata)
                 md = metadata.metadata(repo_metadata_dir, repo_metadata)
                 owner = md.owner()
                 if owner not in owners:
                     owners.append(owner)
 
     return owners
 
+    # repo_full_name = (repo_url[19:]).replace("/", "_").replace(".", "-")
+    # today = datetime.date.today().strftime("%Y-%m-%d")
+    #
+    # for file in os.listdir(os.fsencode(repo_metadata_dir)):
+    #     filename = os.fsdecode(file)
+    #     if filename.endswith(f"_{today}.json"):
+    #         with open(f"{repo_metadata_dir}/{filename}") as json_metadata:
+    #             repo_metadata = json.load(json_metadata)
+    #             md = metadata.metadata(repo_metadata_dir, repo_metadata)
+    #             owner = md.owner()
+    #             if owner not in owners:
+    #                 owners.append(owner)
+
```

### Comparing `soca-0.0.1/src/soca/commands/portal/scripts.py` & `soca-0.0.2/src/soca/commands/portal/scripts.py`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/commands/single_card.py` & `soca-0.0.2/src/soca/commands/single_card.py`

 * *Files identical despite different names*

### Comparing `soca-0.0.1/src/soca/commands/upload_summary.py` & `soca-0.0.2/src/soca/commands/upload_summary.py`

 * *Files 2% similar despite different names*

```diff
@@ -61,14 +61,15 @@
     database['fields']['release_more_twoMon'] = 0
     database['fields']['release_less_twoMon'] = 0
     database['fields']['readme_score_0'] = 0
     database['fields']['readme_score_1'] = 0
     database['fields']['readme_score_2'] = 0
     database['fields']['readme_score_3'] = 0
     database['fields']['num_repos'] = 0
+    database['fields']['num_ontologies'] = 0
     database['fields']['num_CFF'] = 0
 
 
 def summaryToDatabase(summary_output):
     """Function that takes the "output" dictionary from create_summary.py and equates it to influxdb
         database dictionary
     Returns
@@ -92,25 +93,26 @@
         'num_withoutId': summary_output['identifiers']['num_without_identifier'],
         'num_withId': summary_output['identifiers']['num_pid'] +summary_output['identifiers']['num_pid'],
         'num_Apache': summary_output['licenses']['APACHE'],
         'num_GPL': summary_output['licenses']['GPL'],
         'num_MIT': summary_output['licenses']['MIT'],
         'num_Other': summary_output['licenses']['OTHER'],
         'num_Missing': summary_output['licenses']['MISSING'],
-        'sum_licenses': summary_output['num_repos'] - summary_output['licenses']['MISSING'],
+        'sum_licenses': summary_output['licenses']['APACHE'] + summary_output['licenses']['GPL'] + summary_output['licenses']['MIT'] + summary_output['licenses']['OTHER'],
         'num_with_citation': summary_output['has_citation'],
         'num_no_citation': summary_output['no_citation'],
         'release_more_twoMon': summary_output['released']['LONGER'],
         'release_less_twoMon': summary_output['released']['<2 MONTHS'],
         'readme_score_0': summary_output['readme']['Level 0'],
         'readme_score_1': summary_output['readme']['Level 1'],
         'readme_score_2': summary_output['readme']['Level 2'],
         'readme_score_3': summary_output['readme']['Level 3'],
         'sum_readme': summary_output['num_repos'] - summary_output['readme']['Level 0'],
         'num_repos': summary_output['num_repos'],
+        'num_ontologies': summary_output['num_ontologies'],
         'num_no_readme': summary_output['num_no_readme'],
         'num_with_readme': summary_output['num_with_readme'],
         'num_with_description': summary_output['num_with_description'],
         'num_with_acknowledgement': summary_output['num_with_acknowledgement'],
         'num_with_installation': summary_output['num_with_installation'],
         'num_with_requirement': summary_output['num_with_requirement']
     })
```

### Comparing `soca-0.0.1/src/soca.egg-info/PKG-INFO` & `soca-0.0.2/src/soca.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: soca
-Version: 0.0.1
+Version: 0.0.2
 Summary: A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 Home-page: https://github.com/oeg-upm/soca
-Author: Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzaled, Daniel Garijo
-Author-email: miguel.arroyo.marquez@alumnos.upm.es, daniel.garijo@upm.es
+Author: Daniel Rodríguez Mariblanca, Miguel Arroyo Márquez, Esteban Gonzalez, Daniel Garijo
+Author-email: daniel.garijo@upm.es
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 
 # Software Catalog Creator (soca)
 
-[![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
+[![DOI](https://zenodo.org/badge/402041422.svg)](https://zenodo.org/badge/latestdoi/402041422) [![PyPI](https://badge.fury.io/py/soca.svg)](https://badge.fury.io/py/soca) [![Project Status: Active: The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
 
 <img src="doc/images/soca-logo.png" alt="logo" width="150"/>
 
 A python package that given an organization/user name, it will create a software catalog for browsing all repositories or just a single repository in a minimalist card.
 
 ## Sample result
```

### Comparing `soca-0.0.1/src/soca.egg-info/SOURCES.txt` & `soca-0.0.2/src/soca.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -21,14 +21,15 @@
 src/soca/assets/img/filter.svg
 src/soca/assets/img/github-default.svg
 src/soca/assets/img/help.png
 src/soca/assets/img/oeg_logo.gif
 src/soca/assets/img/soca-logo.ico
 src/soca/assets/img/soca-logo.png
 src/soca/assets/img/sort.svg
+src/soca/assets/img/statIcon.svg
 src/soca/assets/img/upm_logo.png
 src/soca/assets/language_icons/arduino.svg
 src/soca/assets/language_icons/c++.svg
 src/soca/assets/language_icons/c-sharp.svg
 src/soca/assets/language_icons/c.svg
 src/soca/assets/language_icons/clojure.svg
 src/soca/assets/language_icons/coffeescript.svg
```

### Comparing `soca-0.0.1/tests/test-scc.py` & `soca-0.0.2/tests/test-scc.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,50 +1,71 @@
+import os
 import unittest
 from unittest import TestCase, mock
 import json
 from pathlib import Path
 from datetime import datetime
 
 import soca.commands.portal.metadata as md
+import soca.commands.portal.portal as portal
+import soca.commands.create_summary as summary
 #from ..src.soca.commands.portal.metadata import metadata as m
 import soca.commands.extract_metadata as ex
 
 
-
-
-
-
-path4 = Path(__file__).parent / "json_files"  / "ver8.json"
-with path4.open() as f:
-    ver8 = json.load(f)
-f.close()
-ver8 = md.metadata(path4, ver8)
-######
-
-
-
-
-
 class test_soca(TestCase):
     pass
 
-class test_extract_metadata_py(TestCase):
-
-    def test_general(self):
-        csv = Path(__file__).parent / "csv_files" / "repos.csv"
-        ex.extract(str(csv),"repos-metadata", True, False)
+class test_pipeline_metadata_py(TestCase):
+    pass
+        #TODO create a full pipeline for testing extract -> portal -> summary and test the summary numbers
+#    def test_general(self):
+        #csv = Path(__file__).parent / "csv_files" / "repos.csv"
+        #ex.extract(str(csv),"repos-metadata", True, False)
+        #portal.generate("repos-metadata", "portal", "Software Catalog", "soca-logo.ico")
+        #summary.create_summary("portal/cards_data.json")
+
+    # def delete_directory(path):
+    #     """Deletes a directory and all files within it.
+    #
+    #     Args:
+    #         path (str): The path of the directory to be deleted.
+    #     """
+    #     # Check if the path exists and is a directory
+    #     if os.path.exists(path) and os.path.isdir(path):
+    #         # Iterate through all files in the directory and delete them
+    #         for file in os.listdir(path):
+    #             file_path = os.path.join(path, file)
+    #             if os.path.isfile(file_path):
+    #                 os.remove(file_path)
+    #             elif os.path.isdir(file_path):
+    #                 # Recursively delete any subdirectories
+    #                 delete_directory(file_path)
+    #         # Remove the directory itself
+    #         os.rmdir(path)
+    #     else:
+    #         print(f"The directory {path} does not exist or is not a directory.")
 class test_metadata_py(TestCase):
     def test_License(self):
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
-        pass
-    #TODO
+        lic = meta.license()
+        self.assertEqual(lic['value'],'https://api.github.com/licenses/apache-2.0')
+    def test_License_fileExploration(self):
+        path = Path(__file__).parent / "json_files"  / "epw2rdf-contents.json"
+        with path.open() as f:
+            data = json.load(f)
+        f.close()
+        meta = md.metadata(path, data)
+        lic = meta.license()
+        self.assertEqual(lic['name'], 'MIT License')
+
     def test_noLicense(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.license())
         pass
     def test_lastUpdate_type(self):
@@ -89,19 +110,20 @@
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         rel =  data['releases']
         self.assertEqual(meta.n_releases(),len(rel))
-    #TODO
-    def no_releases(self):
+
+    def test_no_releases(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
+        self.assertEqual(0, empty.n_releases())
         pass
     def test_downloadUrl(self):
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
@@ -111,25 +133,34 @@
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         url = data['readme_url'][0]['result']['value']
         self.assertEqual(meta.readme(),url)
-    #TODO
+
     def test_no_readme(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.readme())
-        pass
 
     def test_last_release(self):
+        path = Path(__file__).parent / "json_files" / "widoco_9_test.json"
+        with path.open() as f:
+            data = json.load(f)
+        f.close()
+        meta = md.metadata(path, data)
+        self.assertEqual(meta.last_release(), 'WIDOCO 1.4.17: Update OOPS! Web service. GitHub actions')
+    def test_no_last_release(self):
+        mT = json.loads('{"emtpy":"mT"}')
+        path = Path("doesntExist")
+        empty = md.metadata(path, mT)
+        self.assertEquals('',empty.last_release())
 
-        pass
     def test_logo(self):
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         logo = data['logo'][0]['result']['value']
@@ -153,56 +184,58 @@
         self.assertEqual(meta.hasDocumentation(),data['documentation'])
     def test_noDocumenation(self):
         # This JSON represents a github with only a readme(containing an image)
         path2 = Path(__file__).parent / "json_files" / "testLogo.json"
         with path2.open() as f:
             logo = json.load(f)
         f.close()
-
         plain = md.metadata(path2, logo)
         self.assertIsNone(plain.hasDocumentation())
-    #TODO
+
     def test_citations(self):
         path = Path(__file__).parent / "json_files"  / "somef9.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
-        pen = meta.citations()
-        print(pen['citation'])
+        cite = meta.citations()
+        if len(cite) > 0:
+            pass
 
-        pass
     def test_noCitation(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.citations())
     def test_paper(self):
-        path = Path(__file__).parent / "json_files"  / "somef9.json"
+        path = Path(__file__).parent / "json_files" / "somef9.json"
+        #path = Path(__file__).parent / "json_files" / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         self.assertIn("doi.org", meta.paper()[0].link_paper)
     def test_noPaper(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.paper())
     def test_title(self):
-        path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
+        path = Path(__file__).parent / "json_files"  / "oeg-upm_r4r.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         title = data['name'][0]['result']['value']
         self.assertEquals(title,meta.title())
-    #TODO
     def test_noTitle(self):
-        pass
+        mT = json.loads('{"emtpy":"mT"}')
+        path = Path("doesntExist")
+        empty = md.metadata(path, mT)
+        self.assertIsNone(empty.title())
     def test_owner(self):
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
         owner = data['owner'][0]['result']['value']
@@ -251,34 +284,50 @@
         self.assertEqual(meta.identifier(),id)
     def test_noId(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.identifier())
 
-    #TODO
     def test_requirements(self):
-        pass
+        path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
+        with path.open() as f:
+            data = json.load(f)
+        f.close()
+        meta = md.metadata(path, data)
+        self.assertIsNotNone(meta.requirements())
+
     def test_noRequirements(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.requirements())
-    #TODO
     def test_docker(self):
-        pass
+        path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
+        with path.open() as f:
+            data = json.load(f)
+        f.close()
+        meta = md.metadata(path, data)
+        dock = meta.docker()
+        self.assertGreater(len(meta.docker()),0)
     def test_noDocker(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.docker())
 
-    #TODO
     def test_installation(self):
-        pass
+        path = Path(__file__).parent / "json_files"  / "somef9.json"
+        with path.open() as f:
+            data = json.load(f)
+        f.close()
+        meta = md.metadata(path, data)
+        install = meta.installation()
+        self.assertIsNotNone(install)
+
 
     def test_noInstallation(self):
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
@@ -294,15 +343,15 @@
             if lang == "python":
                 self.assertTrue()
     def test_noLanguage(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.languages())
-    #TODO
+
     def test_copy_btn(self):
         #print(meta.copy_btn())
         path = Path(__file__).parent / "json_files"  / "widoco_9_test.json"
         with path.open() as f:
             data = json.load(f)
         f.close()
         meta = md.metadata(path, data)
@@ -319,21 +368,21 @@
         self.assertEqual(meta.status(),status)
     def test_noStatus(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.status())
 
-    #TODO
     def test_usage(self):
         path5 = Path(__file__).parent / "json_files" / "somef9.json"
         with path5.open() as f:
             somef9jayson = json.load(f)
         f.close()
         somef9 = md.metadata(path5, somef9jayson)
+        self.assertIsNotNone(somef9.usage())
         #print(somef9.usage())
         pass
     def test_noUsage(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.usage())
@@ -347,20 +396,58 @@
         #print(somef9.notebook())
         pass
     def test_noNotebook(self):
         mT = json.loads('{"emtpy":"mT"}')
         path = Path("doesntExist")
         empty = md.metadata(path, mT)
         self.assertIsNone(empty.notebook())
-    #TODO
+        
+    def test_repo_type(self):
+        path5 = Path(__file__).parent / "json_files" / "somef9.json"
+        with path5.open() as f:
+            somef9jayson = json.load(f)
+        f.close()
+        somef9 = md.metadata(path5, somef9jayson)
+        #print(somef9.repo_type())
+        pass
+    def test_repo_type(self):
+        path5 = Path(__file__).parent / "json_files" / "somef9.json"
+        with path5.open() as f:
+            somef9jayson = json.load(f)
+        f.close()
+        somef9 = md.metadata(path5, somef9jayson)
+        kek = somef9.html_repo_type()
+        print(kek)
+
     def test_html_repo_icons(self):
-#        path = Path(__file__).parent / "json_files" / "somef9.json"
-#        with path.open() as f:
-#            somef9jayson = json.load(f)
-#        f.close()
-#        somef9 = md.metadata(path, somef9jayson)
-#        somef9.html_repo_icons()
+        path = Path(__file__).parent / "json_files" / "oeg-upm_soca.json"
+        with path.open() as f:
+            somef9jayson = json.load(f)
+        f.close()
+        somef9 = md.metadata(path, somef9jayson)
+        somef9.html_repo_icons()
+        pass
+    def test_r4r(self):
+        path = Path(__file__).parent / "json_files" / "oeg-upm_r4r.json"
+        with path.open() as f:
+            r4rjayson = json.load(f)
+        f.close()
+        r4r = md.metadata(path, r4rjayson)
+        r4r.html_repo_icons()
         pass
 
+    def test_ontology(self):
+        path = Path(__file__).parent / "json_files" / "ontologytest.json"
+        with path.open() as f:
+            ontojayson = json.load(f)
+        f.close()
+        summary.create_summary(path,"summary",False)
+        path2 = Path(__file__).parent/ "summary"
+        dir = os.listdir(path2)
+        if len(dir) == 0:
+            os.rmdir(path2)
+            pass
+
+
 if __name__ == '__main__':
     unittest.main()
```

