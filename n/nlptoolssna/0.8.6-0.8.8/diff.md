# Comparing `tmp/nlptoolssna-0.8.6.tar.gz` & `tmp/nlptoolssna-0.8.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nlptoolssna-0.8.6.tar", last modified: Thu May 11 20:52:33 2023, max compression
+gzip compressed data, was "nlptoolssna-0.8.8.tar", last modified: Sat May 13 13:46:27 2023, max compression
```

## Comparing `nlptoolssna-0.8.6.tar` & `nlptoolssna-0.8.8.tar`

### file list

```diff
@@ -1,84 +1,84 @@
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.868660 nlptoolssna-0.8.6/
--rw-rw-rw-   0        0        0      172 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/AUTHORS.rst
--rw-rw-rw-   0        0        0     3667 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/CONTRIBUTING.rst
--rw-rw-rw-   0        0        0       97 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/HISTORY.rst
--rw-rw-rw-   0        0        0     1091 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/LICENSE
--rw-rw-rw-   0        0        0      273 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/MANIFEST.in
--rw-rw-rw-   0        0        0     1924 2023-05-11 20:52:33.868660 nlptoolssna-0.8.6/PKG-INFO
--rw-rw-rw-   0        0        0      951 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/README.rst
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.785004 nlptoolssna-0.8.6/docs/
--rw-rw-rw-   0        0        0      676 2023-04-26 19:48:07.000000 nlptoolssna-0.8.6/docs/Makefile
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.759067 nlptoolssna-0.8.6/docs/build/
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.760070 nlptoolssna-0.8.6/docs/build/html/
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.786001 nlptoolssna-0.8.6/docs/build/html/_images/
--rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.6/docs/build/html/_images/download.png
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.791004 nlptoolssna-0.8.6/docs/build/html/_static/
--rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.6/docs/build/html/_static/download.png
--rw-rw-rw-   0        0        0      286 2023-04-11 21:34:54.000000 nlptoolssna-0.8.6/docs/build/html/_static/file.png
--rw-rw-rw-   0        0        0       90 2023-04-11 21:34:54.000000 nlptoolssna-0.8.6/docs/build/html/_static/minus.png
--rw-rw-rw-   0        0        0       90 2023-04-11 21:34:54.000000 nlptoolssna-0.8.6/docs/build/html/_static/plus.png
--rwxrwxrwx   0        0        0      791 2023-03-28 19:29:13.000000 nlptoolssna-0.8.6/docs/make.bat
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.802168 nlptoolssna-0.8.6/docs/source/
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.803165 nlptoolssna-0.8.6/docs/source/_static/
--rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.6/docs/source/_static/download.png
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.807202 nlptoolssna-0.8.6/docs/source/api/
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.808790 nlptoolssna-0.8.6/docs/source/api/DataDownload/
--rw-rw-rw-   0        0        0      138 2023-05-01 11:11:44.000000 nlptoolssna-0.8.6/docs/source/api/DataDownload/downloader.rst
--rw-rw-rw-   0        0        0      234 2023-05-01 11:08:11.000000 nlptoolssna-0.8.6/docs/source/api/DataDownload.rst
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.811812 nlptoolssna-0.8.6/docs/source/api/morphology/
--rw-rw-rw-   0        0        0      148 2023-05-02 18:17:06.000000 nlptoolssna-0.8.6/docs/source/api/morphology/morph_analyzer.rst
--rw-rw-rw-   0        0        0      230 2023-05-02 18:16:20.000000 nlptoolssna-0.8.6/docs/source/api/morphology.rst
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.818808 nlptoolssna-0.8.6/docs/source/api/utils/
--rw-rw-rw-   0        0        0      114 2023-05-04 19:55:13.000000 nlptoolssna-0.8.6/docs/source/api/utils/implication.rst
--rw-rw-rw-   0        0        0      102 2023-05-06 11:51:47.000000 nlptoolssna-0.8.6/docs/source/api/utils/jaccard.rst
--rw-rw-rw-   0        0        0       99 2023-05-04 19:26:52.000000 nlptoolssna-0.8.6/docs/source/api/utils/parser.rst
--rw-rw-rw-   0        0        0      141 2023-05-08 19:10:33.000000 nlptoolssna-0.8.6/docs/source/api/utils/text_transliteration.rst
--rw-rw-rw-   0        0        0      271 2023-05-08 19:09:40.000000 nlptoolssna-0.8.6/docs/source/api/utils.rst
--rw-rw-rw-   0        0        0      182 2023-05-06 11:52:28.000000 nlptoolssna-0.8.6/docs/source/api.rst
--rw-rw-rw-   0        0        0       32 2023-04-26 19:28:12.000000 nlptoolssna-0.8.6/docs/source/authors.rst
--rw-rw-rw-   0        0        0     6180 2023-04-27 12:10:35.000000 nlptoolssna-0.8.6/docs/source/conf.py
--rw-rw-rw-   0        0        0      314 2023-05-06 11:52:23.000000 nlptoolssna-0.8.6/docs/source/index.rst
--rw-rw-rw-   0        0        0     1177 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/docs/source/installation.rst
--rw-rw-rw-   0        0        0       31 2023-04-26 19:27:50.000000 nlptoolssna-0.8.6/docs/source/readme.rst
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.821808 nlptoolssna-0.8.6/nlptools/
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.825393 nlptoolssna-0.8.6/nlptools/DataDownload/
--rw-rw-rw-   0        0        0        0 2023-04-16 17:23:41.000000 nlptoolssna-0.8.6/nlptools/DataDownload/__init__.py
--rw-rw-rw-   0        0        0     5067 2023-05-11 20:27:50.000000 nlptoolssna-0.8.6/nlptools/DataDownload/downloader.py
--rw-rw-rw-   0        0        0      132 2023-05-06 12:05:24.000000 nlptoolssna-0.8.6/nlptools/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.834394 nlptoolssna-0.8.6/nlptools/arabiner/
--rw-rw-rw-   0        0        0        0 2023-02-26 06:10:53.000000 nlptoolssna-0.8.6/nlptools/arabiner/__init__.py
--rw-rw-rw-   0        0        0     4227 2023-04-30 06:31:38.000000 nlptoolssna-0.8.6/nlptools/arabiner/data.py
--rw-rw-rw-   0        0        0     5061 2023-04-30 06:31:27.000000 nlptoolssna-0.8.6/nlptools/arabiner/datasets.py
--rw-rw-rw-   0        0        0     3676 2023-03-29 20:23:29.000000 nlptoolssna-0.8.6/nlptools/arabiner/helpers.py
--rw-rw-rw-   0        0        0     1365 2023-04-30 06:28:09.000000 nlptoolssna-0.8.6/nlptools/arabiner/infer.py
--rw-rw-rw-   0        0        0     5092 2023-05-01 11:40:47.000000 nlptoolssna-0.8.6/nlptools/arabiner/transforms.py
--rw-rw-rw-   0        0        0      458 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/nlptools/cli.py
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.836393 nlptoolssna-0.8.6/nlptools/data/
--rw-rw-rw-   0        0        0    86011 2023-04-06 09:01:12.000000 nlptoolssna-0.8.6/nlptools/data/my_data.pickle
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.844621 nlptoolssna-0.8.6/nlptools/morphology/
--rw-rw-rw-   0        0        0      377 2023-05-02 18:19:19.000000 nlptoolssna-0.8.6/nlptools/morphology/__init__.py
--rw-rw-rw-   0        0        0     2784 2023-04-27 18:35:11.000000 nlptoolssna-0.8.6/nlptools/morphology/charsets.py
--rw-rw-rw-   0        0        0     6376 2023-05-08 18:11:31.000000 nlptoolssna-0.8.6/nlptools/morphology/morph_analyzer.py
--rw-rw-rw-   0        0        0       47 2023-04-01 20:02:46.000000 nlptoolssna-0.8.6/nlptools/morphology/settings.py
--rw-rw-rw-   0        0        0      602 2023-05-11 20:52:05.000000 nlptoolssna-0.8.6/nlptools/morphology/tokenizers_words.py
--rw-rw-rw-   0        0        0       20 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/nlptools/nlptools.py
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.853623 nlptoolssna-0.8.6/nlptools/utils/
--rw-rw-rw-   0        0        0        0 2023-05-06 10:33:56.000000 nlptoolssna-0.8.6/nlptools/utils/__init__.py
--rw-rw-rw-   0        0        0    26235 2023-05-11 20:51:14.000000 nlptoolssna-0.8.6/nlptools/utils/implication.py
--rw-rw-rw-   0        0        0    10287 2023-05-11 20:50:47.000000 nlptoolssna-0.8.6/nlptools/utils/jaccard.py
--rw-rw-rw-   0        0        0     7556 2023-05-11 20:46:42.000000 nlptoolssna-0.8.6/nlptools/utils/parser.py
--rw-rw-rw-   0        0        0     9283 2023-05-08 19:13:30.000000 nlptoolssna-0.8.6/nlptools/utils/text_transliteration.py
--rw-rw-rw-   0        0        0       32 2023-05-06 10:35:53.000000 nlptoolssna-0.8.6/nlptools/utils/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.864661 nlptoolssna-0.8.6/nlptoolssna.egg-info/
--rw-rw-rw-   0        0        0     1924 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1758 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       47 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0        2 2023-05-06 10:36:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       41 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-11 20:52:33.000000 nlptoolssna-0.8.6/nlptoolssna.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      586 2023-05-11 20:52:33.870733 nlptoolssna-0.8.6/setup.cfg
--rw-rw-rw-   0        0        0     2109 2023-05-06 10:49:14.000000 nlptoolssna-0.8.6/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-11 20:52:33.867658 nlptoolssna-0.8.6/tests/
--rw-rw-rw-   0        0        0       39 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/tests/__init__.py
--rw-rw-rw-   0        0        0      413 2023-04-15 18:20:16.000000 nlptoolssna-0.8.6/tests/test_nlptools.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.599743 nlptoolssna-0.8.8/
+-rw-rw-rw-   0        0        0      172 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/AUTHORS.rst
+-rw-rw-rw-   0        0        0     3667 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/CONTRIBUTING.rst
+-rw-rw-rw-   0        0        0       97 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/HISTORY.rst
+-rw-rw-rw-   0        0        0     1091 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/LICENSE
+-rw-rw-rw-   0        0        0      273 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/MANIFEST.in
+-rw-rw-rw-   0        0        0     1924 2023-05-13 13:46:27.599743 nlptoolssna-0.8.8/PKG-INFO
+-rw-rw-rw-   0        0        0      951 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/README.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.494364 nlptoolssna-0.8.8/docs/
+-rw-rw-rw-   0        0        0      676 2023-04-26 19:48:07.000000 nlptoolssna-0.8.8/docs/Makefile
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.466299 nlptoolssna-0.8.8/docs/build/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.469301 nlptoolssna-0.8.8/docs/build/html/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.495365 nlptoolssna-0.8.8/docs/build/html/_images/
+-rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.8/docs/build/html/_images/download.png
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.502366 nlptoolssna-0.8.8/docs/build/html/_static/
+-rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.8/docs/build/html/_static/download.png
+-rw-rw-rw-   0        0        0      286 2023-04-11 21:34:54.000000 nlptoolssna-0.8.8/docs/build/html/_static/file.png
+-rw-rw-rw-   0        0        0       90 2023-04-11 21:34:54.000000 nlptoolssna-0.8.8/docs/build/html/_static/minus.png
+-rw-rw-rw-   0        0        0       90 2023-04-11 21:34:54.000000 nlptoolssna-0.8.8/docs/build/html/_static/plus.png
+-rwxrwxrwx   0        0        0      791 2023-03-28 19:29:13.000000 nlptoolssna-0.8.8/docs/make.bat
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.510925 nlptoolssna-0.8.8/docs/source/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.511926 nlptoolssna-0.8.8/docs/source/_static/
+-rw-rw-rw-   0        0        0     9568 2023-04-26 20:26:03.000000 nlptoolssna-0.8.8/docs/source/_static/download.png
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.518925 nlptoolssna-0.8.8/docs/source/api/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.519925 nlptoolssna-0.8.8/docs/source/api/DataDownload/
+-rw-rw-rw-   0        0        0      138 2023-05-01 11:11:44.000000 nlptoolssna-0.8.8/docs/source/api/DataDownload/downloader.rst
+-rw-rw-rw-   0        0        0      234 2023-05-01 11:08:11.000000 nlptoolssna-0.8.8/docs/source/api/DataDownload.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.521926 nlptoolssna-0.8.8/docs/source/api/morphology/
+-rw-rw-rw-   0        0        0      148 2023-05-02 18:17:06.000000 nlptoolssna-0.8.8/docs/source/api/morphology/morph_analyzer.rst
+-rw-rw-rw-   0        0        0      230 2023-05-02 18:16:20.000000 nlptoolssna-0.8.8/docs/source/api/morphology.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.528643 nlptoolssna-0.8.8/docs/source/api/utils/
+-rw-rw-rw-   0        0        0      114 2023-05-04 19:55:13.000000 nlptoolssna-0.8.8/docs/source/api/utils/implication.rst
+-rw-rw-rw-   0        0        0      102 2023-05-06 11:51:47.000000 nlptoolssna-0.8.8/docs/source/api/utils/jaccard.rst
+-rw-rw-rw-   0        0        0       99 2023-05-04 19:26:52.000000 nlptoolssna-0.8.8/docs/source/api/utils/parser.rst
+-rw-rw-rw-   0        0        0      141 2023-05-08 19:10:33.000000 nlptoolssna-0.8.8/docs/source/api/utils/text_transliteration.rst
+-rw-rw-rw-   0        0        0      271 2023-05-08 19:09:40.000000 nlptoolssna-0.8.8/docs/source/api/utils.rst
+-rw-rw-rw-   0        0        0      182 2023-05-06 11:52:28.000000 nlptoolssna-0.8.8/docs/source/api.rst
+-rw-rw-rw-   0        0        0       32 2023-04-26 19:28:12.000000 nlptoolssna-0.8.8/docs/source/authors.rst
+-rw-rw-rw-   0        0        0     6180 2023-04-27 12:10:35.000000 nlptoolssna-0.8.8/docs/source/conf.py
+-rw-rw-rw-   0        0        0      314 2023-05-06 11:52:23.000000 nlptoolssna-0.8.8/docs/source/index.rst
+-rw-rw-rw-   0        0        0     1177 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/docs/source/installation.rst
+-rw-rw-rw-   0        0        0       31 2023-04-26 19:27:50.000000 nlptoolssna-0.8.8/docs/source/readme.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.535820 nlptoolssna-0.8.8/nlptools/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.540833 nlptoolssna-0.8.8/nlptools/DataDownload/
+-rw-rw-rw-   0        0        0        0 2023-04-16 17:23:41.000000 nlptoolssna-0.8.8/nlptools/DataDownload/__init__.py
+-rw-rw-rw-   0        0        0     5087 2023-05-11 20:56:17.000000 nlptoolssna-0.8.8/nlptools/DataDownload/downloader.py
+-rw-rw-rw-   0        0        0      132 2023-05-06 12:05:24.000000 nlptoolssna-0.8.8/nlptools/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.552821 nlptoolssna-0.8.8/nlptools/arabiner/
+-rw-rw-rw-   0        0        0        0 2023-02-26 06:10:53.000000 nlptoolssna-0.8.8/nlptools/arabiner/__init__.py
+-rw-rw-rw-   0        0        0     4142 2023-05-11 20:59:35.000000 nlptoolssna-0.8.8/nlptools/arabiner/data.py
+-rw-rw-rw-   0        0        0     5057 2023-05-11 20:57:32.000000 nlptoolssna-0.8.8/nlptools/arabiner/datasets.py
+-rw-rw-rw-   0        0        0     3676 2023-03-29 20:23:29.000000 nlptoolssna-0.8.8/nlptools/arabiner/helpers.py
+-rw-rw-rw-   0        0        0     1336 2023-05-11 21:00:06.000000 nlptoolssna-0.8.8/nlptools/arabiner/infer.py
+-rw-rw-rw-   0        0        0     5092 2023-05-11 20:58:53.000000 nlptoolssna-0.8.8/nlptools/arabiner/transforms.py
+-rw-rw-rw-   0        0        0      458 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/nlptools/cli.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.555823 nlptoolssna-0.8.8/nlptools/data/
+-rw-rw-rw-   0        0        0    86011 2023-04-06 09:01:12.000000 nlptoolssna-0.8.8/nlptools/data/my_data.pickle
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.566821 nlptoolssna-0.8.8/nlptools/morphology/
+-rw-rw-rw-   0        0        0      377 2023-05-02 18:19:19.000000 nlptoolssna-0.8.8/nlptools/morphology/__init__.py
+-rw-rw-rw-   0        0        0     2784 2023-04-27 18:35:11.000000 nlptoolssna-0.8.8/nlptools/morphology/charsets.py
+-rw-rw-rw-   0        0        0     6376 2023-05-08 18:11:31.000000 nlptoolssna-0.8.8/nlptools/morphology/morph_analyzer.py
+-rw-rw-rw-   0        0        0       47 2023-04-01 20:02:46.000000 nlptoolssna-0.8.8/nlptools/morphology/settings.py
+-rw-rw-rw-   0        0        0      602 2023-05-11 20:52:05.000000 nlptoolssna-0.8.8/nlptools/morphology/tokenizers_words.py
+-rw-rw-rw-   0        0        0       20 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/nlptools/nlptools.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.578199 nlptoolssna-0.8.8/nlptools/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-06 10:33:56.000000 nlptoolssna-0.8.8/nlptools/utils/__init__.py
+-rw-rw-rw-   0        0        0    27982 2023-05-13 13:44:33.000000 nlptoolssna-0.8.8/nlptools/utils/implication.py
+-rw-rw-rw-   0        0        0    10287 2023-05-11 20:50:47.000000 nlptoolssna-0.8.8/nlptools/utils/jaccard.py
+-rw-rw-rw-   0        0        0     7556 2023-05-11 20:46:42.000000 nlptoolssna-0.8.8/nlptools/utils/parser.py
+-rw-rw-rw-   0        0        0     9283 2023-05-08 19:13:30.000000 nlptoolssna-0.8.8/nlptools/utils/text_transliteration.py
+-rw-rw-rw-   0        0        0       32 2023-05-06 10:35:53.000000 nlptoolssna-0.8.8/nlptools/utils/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.593777 nlptoolssna-0.8.8/nlptoolssna.egg-info/
+-rw-rw-rw-   0        0        0     1924 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1758 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       47 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0        2 2023-05-06 10:36:33.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       41 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 13:46:27.000000 nlptoolssna-0.8.8/nlptoolssna.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      586 2023-05-13 13:46:27.602538 nlptoolssna-0.8.8/setup.cfg
+-rw-rw-rw-   0        0        0     2109 2023-05-11 21:37:10.000000 nlptoolssna-0.8.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:46:27.597753 nlptoolssna-0.8.8/tests/
+-rw-rw-rw-   0        0        0       39 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/tests/__init__.py
+-rw-rw-rw-   0        0        0      413 2023-04-15 18:20:16.000000 nlptoolssna-0.8.8/tests/test_nlptools.py
```

### Comparing `nlptoolssna-0.8.6/CONTRIBUTING.rst` & `nlptoolssna-0.8.8/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/LICENSE` & `nlptoolssna-0.8.8/LICENSE`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/PKG-INFO` & `nlptoolssna-0.8.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nlptoolssna
-Version: 0.8.6
+Version: 0.8.8
 Summary: Python Boilerplate contains all the boilerplate you need to create a Python package.
 Home-page: https://github.com/eng-aomar/nlptools
 Author: Alaa' Omar
 Author-email: alaa.omer2009@gmail.com
 License: MIT license
 Keywords: nlptools
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `nlptoolssna-0.8.6/README.rst` & `nlptoolssna-0.8.8/README.rst`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/Makefile` & `nlptoolssna-0.8.8/docs/Makefile`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/build/html/_images/download.png` & `nlptoolssna-0.8.8/docs/build/html/_images/download.png`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/build/html/_static/download.png` & `nlptoolssna-0.8.8/docs/build/html/_static/download.png`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/make.bat` & `nlptoolssna-0.8.8/docs/make.bat`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/source/_static/download.png` & `nlptoolssna-0.8.8/docs/source/_static/download.png`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/source/conf.py` & `nlptoolssna-0.8.8/docs/source/conf.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/docs/source/installation.rst` & `nlptoolssna-0.8.8/docs/source/installation.rst`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/DataDownload/downloader.py` & `nlptoolssna-0.8.8/nlptools/DataDownload/downloader.py`

 * *Files 4% similar despite different names*

```diff
@@ -133,28 +133,28 @@
     except requests.exceptions.HTTPError as e:
         if e.response.status_code == 403:
             print(f'Error 403: Forbidden. The requested file url {url} could not be downloaded due to insufficient permissions. Please check the URL and try again.')
         else:
             print('An error occurred while downloading the file:', e)
 
 
-def download_files():
+def download_files_from_urls():
     """
     Downloads multiple files from a dictionary of urls using the download_file() function.
 
     Args:
         None
 
     Returns:
         None
     """
     for url in urls.values():
         download_file(url)
 
-def download_files(key=None):
+def download_files_from_urls(key=None):
     """
     Downloads multiple files from a dictionary of urls using the download_file() function.
 
     Args:
         key (optional): The key of the dictionary to specify which URLs to download. If not provided, all URLs will be downloaded.
 
     Returns:
```

### Comparing `nlptoolssna-0.8.6/nlptools/arabiner/data.py` & `nlptoolssna-0.8.8/nlptools/arabiner/data.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,71 +1,71 @@
 from torch.utils.data import DataLoader
 from torchtext.vocab import vocab
 from collections import Counter, namedtuple
 import logging
 import re
-#import itertools
-from nlptools.arabiner.helpers import load_object
-from nlptools.arabiner.datasets import Token
+import itertools
+from arabiner.utils.helpers import load_object
+from arabiner.data.datasets import Token
 
 logger = logging.getLogger(__name__)
 
 
-# def conll_to_segments(filename):
-#     """
-#     Convert CoNLL files to segments. This return list of segments and each segment is
-#     a list of tuples (token, tag)
-#     :param filename: Path
-#     :return: list[[tuple]] - [[(token, tag), (token, tag), ...], [(token, tag), ...]]
-#     """
-#     segments, segment = list(), list()
-
-#     with open(filename, "r") as fh:
-#         for token in fh.read().splitlines():
-#             if not token.strip():
-#                 segments.append(segment)
-#                 segment = list()
-#             else:
-#                 parts = token.split()
-#                 token = Token(text=parts[0], gold_tag=parts[1:])
-#                 segment.append(token)
-
-#         segments.append(segment)
-
-#     return segments
-
-
-# def parse_conll_files(data_paths):
-#     """
-#     Parse CoNLL formatted files and return list of segments for each file and index
-#     the vocabs and tags across all data_paths
-#     :param data_paths: tuple(Path) - tuple of filenames
-#     :return: tuple( [[(token, tag), ...], [(token, tag), ...]], -> segments for data_paths[i]
-#                     [[(token, tag), ...], [(token, tag), ...]], -> segments for data_paths[i+1],
-#                     ...
-#                   )
-#              List of segments for each dataset and each segment has list of (tokens, tags)
-#     """
-#     vocabs = namedtuple("Vocab", ["tags", "tokens"])
-#     datasets, tags, tokens = list(), list(), list()
-
-#     for data_path in data_paths:
-#         dataset = conll_to_segments(data_path)
-#         datasets.append(dataset)
-#         tokens += [token.text for segment in dataset for token in segment]
-#         tags += [token.gold_tag for segment in dataset for token in segment]
-
-#     # Flatten list of tags
-#     tags = list(itertools.chain(*tags))
-
-#     # Generate vocabs for tags and tokens
-#     tag_vocabs = tag_vocab_by_type(tags)
-#     tag_vocabs.insert(0, vocab(Counter(tags)))
-#     vocabs = vocabs(tokens=vocab(Counter(tokens), specials=["UNK"]), tags=tag_vocabs)
-#     return tuple(datasets), vocabs
+def conll_to_segments(filename):
+    """
+    Convert CoNLL files to segments. This return list of segments and each segment is
+    a list of tuples (token, tag)
+    :param filename: Path
+    :return: list[[tuple]] - [[(token, tag), (token, tag), ...], [(token, tag), ...]]
+    """
+    segments, segment = list(), list()
+
+    with open(filename, "r") as fh:
+        for token in fh.read().splitlines():
+            if not token.strip():
+                segments.append(segment)
+                segment = list()
+            else:
+                parts = token.split()
+                token = Token(text=parts[0], gold_tag=parts[1:])
+                segment.append(token)
+
+        segments.append(segment)
+
+    return segments
+
+
+def parse_conll_files(data_paths):
+    """
+    Parse CoNLL formatted files and return list of segments for each file and index
+    the vocabs and tags across all data_paths
+    :param data_paths: tuple(Path) - tuple of filenames
+    :return: tuple( [[(token, tag), ...], [(token, tag), ...]], -> segments for data_paths[i]
+                    [[(token, tag), ...], [(token, tag), ...]], -> segments for data_paths[i+1],
+                    ...
+                  )
+             List of segments for each dataset and each segment has list of (tokens, tags)
+    """
+    vocabs = namedtuple("Vocab", ["tags", "tokens"])
+    datasets, tags, tokens = list(), list(), list()
+
+    for data_path in data_paths:
+        dataset = conll_to_segments(data_path)
+        datasets.append(dataset)
+        tokens += [token.text for segment in dataset for token in segment]
+        tags += [token.gold_tag for segment in dataset for token in segment]
+
+    # Flatten list of tags
+    tags = list(itertools.chain(*tags))
+
+    # Generate vocabs for tags and tokens
+    tag_vocabs = tag_vocab_by_type(tags)
+    tag_vocabs.insert(0, vocab(Counter(tags)))
+    vocabs = vocabs(tokens=vocab(Counter(tokens), specials=["UNK"]), tags=tag_vocabs)
+    return tuple(datasets), vocabs
 
 
 def tag_vocab_by_type(tags):
     vocabs = list()
     c = Counter(tags)
     tag_names = c.keys()
     tag_types = sorted(list(set([tag.split("-", 1)[1] for tag in tag_names if "-" in tag])))
@@ -114,8 +114,8 @@
             num_workers=num_workers,
             collate_fn=dataset.collate_fn,
         )
 
         logger.info("%s batches found", len(dataloader))
         dataloaders.append(dataloader)
 
-    return 
+    return dataloaders
```

### Comparing `nlptoolssna-0.8.6/nlptools/arabiner/datasets.py` & `nlptoolssna-0.8.8/nlptools/arabiner/datasets.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import logging
 import torch
 from torch.utils.data import Dataset
 from torch.nn.utils.rnn import pad_sequence
-from nlptools.arabiner.transforms import (
+from arabiner.data.transforms import (
     BertSeqTransform,
     NestedTagsTransform
 )
 
 logger = logging.getLogger(__name__)
```

### Comparing `nlptoolssna-0.8.6/nlptools/arabiner/helpers.py` & `nlptoolssna-0.8.8/nlptools/arabiner/helpers.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/arabiner/infer.py` & `nlptoolssna-0.8.8/nlptools/arabiner/infer.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 import os
 logger = logging.getLogger(__name__)
 
 
 
 def ner(text, model_path, batch_size=32):
     # Load tagger
-    filename = 'Wj27012000/867530901NED20230418modelv28'
+    filename = 'Wj27012000'
     path =downloader.get_appdatadir()
     model_path = os.path.join(path, filename)
     tagger, tag_vocab, train_config = load_checkpoint(model_path)
 
     # Convert text to a tagger dataset and index the tokens in args.text
     dataset, token_vocab = text2segments(text)
```

### Comparing `nlptoolssna-0.8.6/nlptools/arabiner/transforms.py` & `nlptoolssna-0.8.8/nlptools/arabiner/transforms.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import torch
 from transformers import BertTokenizer
 from functools import partial
 import logging
 import re
 import itertools
-from nlptools.arabiner.data import datasets
+import arabiner
 
 logger = logging.getLogger(__name__)
 
 
 class BertSeqTransform:
     def __init__(self, bert_model, vocab, max_seq_len=512):
         self.tokenizer = BertTokenizer.from_pretrained(bert_model)
@@ -18,15 +18,15 @@
             truncation=True,
         )
         self.max_seq_len = max_seq_len
         self.vocab = vocab
 
     def __call__(self, segment):
         subwords, tags, tokens = list(), list(), list()
-        unk_token = datasets.Token(text="UNK")
+        unk_token = arabiner.data.datasets.Token(text="UNK")
 
         for token in segment:
             token_subwords = self.encoder(token.text)[1:-1]
             subwords += token_subwords
             tags += [self.vocab.tags[0].get_stoi()[token.gold_tag[0]]] + [self.vocab.tags[0].get_stoi()["O"]] * (len(token_subwords) - 1)
             tokens += [token] + [unk_token] * (len(token_subwords) - 1)
 
@@ -59,15 +59,15 @@
             truncation=True,
         )
         self.max_seq_len = max_seq_len
         self.vocab = vocab
 
     def __call__(self, segment):
         tags, tokens, subwords = list(), list(), list()
-        unk_token = datasets.Token(text="UNK")
+        unk_token = arabiner.data.datasets.Token(text="UNK")
 
         # Encode each token and get its subwords and IDs
         for token in segment:
             token.subwords = self.encoder(token.text)[1:-1]
             subwords += token.subwords
             tokens += [token] + [unk_token] * (len(token.subwords ) - 1)
```

### Comparing `nlptoolssna-0.8.6/nlptools/data/my_data.pickle` & `nlptoolssna-0.8.8/nlptools/data/my_data.pickle`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/morphology/charsets.py` & `nlptoolssna-0.8.8/nlptools/morphology/charsets.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/morphology/morph_analyzer.py` & `nlptoolssna-0.8.8/nlptools/morphology/morph_analyzer.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/morphology/tokenizers_words.py` & `nlptoolssna-0.8.8/nlptools/morphology/tokenizers_words.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/utils/implication.py` & `nlptoolssna-0.8.8/nlptools/utils/implication.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,20 +1,22 @@
 # Created: 16/03/2021 , By Mohammad A'bed
 # Trello task: https://trello.com/c/nHnmnFAe/19-re-implement-implication-function-in-python
 
 #  The Imply algorithm takes two words as input and produces the matching tuple defined by (Words Matching).
 #  The matching between two words is defined as a tuple:
 #  <w1, w2, implication direction, distance, conflicts, verdict, preferredWord> .
-from nlptools.utils.parser import arStrip
 
+from nlptools.utils.parser import arStrip
 class Implication:
     """
-    The Imply algorithm takes two words as input and produces the matching tuple defined by (Words Matching).
-    he matching between two words is defined as a tuple:
-    <w1, w2, implication direction, distance, conflicts, verdict, preferredWord> .
+    The implication class computes whether the two Arabic words are the same or not, regardless of how they are diacritized. The output also contains implication direction, distance, number of conflicts, and other outputs. 
+    Argd:
+        :obj:`str' word1: input string
+        :obj:`str' word2: input string
+
     """
     # Diacritic Pair Distance Map
     distanceTable = [
     [0, 0, 1, 1, 1, 1, 1, 1, 15, 16, 16, 16, 0, 0, 0, 0 ],
     [0, 0, 101, 101, 101, 101, 101, 101, 101, 101, 101, 101, 0, 0, 0, 0],
     [1, 101, 0, 101, 101, 101, 101, 101, 101, 101, 101, 101, 0, 0, 0, 0],
     [1, 101, 101, 0, 101, 101, 101, 101, 101, 101, 101, 101, 0, 0, 0, 0],
@@ -84,33 +86,33 @@
             self.distance = 0
             self.conflicts = 0
             return
         else: # If w1 and w2 are noot exact match
             try:
                 self.lettersDirection = []
                 # build diacritics array for each word 
-                self.word1Diacritics = Implication.calculate_direction(self.word1)
-                self.word2Diacritics = Implication.calculate_direction(self.word2)
+                self.word1Diacritics = Implication.get_diacritics_array(self.word1)
+                self.word2Diacritics = Implication.get_diacritics_array(self.word2)
 
                  # defined lettersDirection array with size of word1Diacritics and fill it by zeros
                 for x in range(0 , len(self.word1Diacritics) + 1): 
                     self.lettersDirection.append(0)
             except :
                 # In case of errors returns the values below 
                 self.verdict = "Incompatible"
                 self.direction = -3 # the two words have different letters
                 self.distance = 3000
                 self.conflicts = 0
                 return
 
             # check if diacritics in both words for some of syntax errors then return Incompatible
-            if (Implication.diacriticsSyntaxErrorIn(self.word1Diacritics) == False and  Implication.diacriticsSyntaxErrorIn(self.word2Diacritics) == False) : 
+            if (  Implication.diacritics_syntax_error_in(self.word1Diacritics) == False and  Implication.diacritics_syntax_error_in(self.word2Diacritics) == False) : 
                 # If no syntax error found:
-                self.word1Undiac = Implication.removeDiacritics(self.word1)
-                self.word2Undiac = Implication.removeDiacritics(self.word2)
+                self.word1Undiac = arStrip(self.word1, diacs=False, shaddah=False)
+                self.word2Undiac = arStrip(self.word2, diacs=False, shaddah=False)
                 # return compatible if each word is one and same letter regardless of diacritics on this letter
                 if (len(self.word1Undiac) == 1 and len(self.word2Undiac) == 1 and self.word1Undiac == self.word2Undiac): 
                         self.verdict = "Compatible"
                         self.direction = 3  #  Both letters have exactly the same diacritics 
                         self.distance = 0
                         self.conflicts = 0
                 else : # If words are more than letter or deffirent letter then calculate the impication
@@ -119,61 +121,91 @@
                 
             else : # If found syntax error in diacitics in word1 or word2 then return these:
                 self.verdict = "Incompatible"
                 self.direction = -3 # the two words have different letters
                 self.distance = 3000
                 self.conflicts = 0
             
-    def get_non_preferred_word( self , word1,  word2) :
+    def get_non_preferred_word(self, word1, word2):
+        """
+        Returns the non-preferred word from two given words.
+
+        Args:
+            :obj:`str' word1: The first word.
+            :obj:`str' word2: The second word.
+
+        Returns:
+            :obj:`str': The non-preferred word.
+
+        Raises:
+            None
+        """
         # this function talkes 2-words and retuen preferredWord 
         word1 = word1.strip()
         word2 = word2.strip()
-        if (word1 != "null" and  word1.strip() ) :
-            if (word2 != "null" and word2.strip()) :
+        if (word1 != None and  word1 ) :
+            if (word2 != None and word2) :
                 preferredWord = ""
-                preferredWord = Implication.get_preferred_word(word1, word2)
+                preferredWord = Implication.getPreferredWord(word1, word2)
                 if word1== preferredWord:
                     return word2
                 else:
                     return word1
             else :
                 return word1
         
         else :
-            if word2 != "null" and word2.strip():
+            if word2 != None and word2:
                 return word2 
             else:
-                return "null"
+                return None
+    
+
+
     def get_preferred_word( self , word1,   word2) :
+        """
+        Returns the preferred word from two given words.
+
+        Args:
+            :obj:`str' word1: The first word.
+            :obj:`str' word2: The second word.
+
+        Returns:
+            :obj:`str': The preferred word.
+
+        Raises:
+            None
+        """        
         word1 = word1.strip()
         word2 = word2.strip()
-        if ( word1 != "null" and word1.strip()) :
-            if (word2 != "null" and word2.strip()) :
+        if ( word1 != None and word1) :
+            if (word2 != None and word2) :
                 implication =  Implication(word1, word2) 
-                if (implication.get_distance() < 15) :
-                    if ( ( implication.get_direction() == 0 ) or
-                       (implication.get_direction() == 2 ) ):
+                direction = implication.get_distance()
+                if (direction < 15) :
+                    if ( ( direction == 0 ) or
+                       (direction == 2 ) ):
                         return word1
-                    elif implication.get_direction() == 1 :
+                    elif direction == 1 :
                         return word2
-                    elif implication.get_direction() == 3 :
+                    elif direction == 3 :
                         if ( ( not word1.endswith("َ") ) and ( not word1.endswith("ُ") ) ) : 
                             return word2
                         return word1
 
                 return ""
             else :
                 return word1
         
         else :
-            if word2 != "null" and ( not word2.strip() ):
+            if word2 != None and (not word2):
                 return  word2
             else:
-                return "null"
-
+                return None
+            
     def normalize_alef(word):
         """
         Normalize the alif (ألف) character in the given word according to certain rules.
 
         Args:
             word (:obj:`str`): The input word to be normalized.
 
@@ -197,20 +229,18 @@
             word = word[:len(word) - 2] + "ىً"
 
         if word.endswith("ًا"):
             word = word[:len(word) - 2] + "اً"
         # Replace Alif-dhamma with Alif
         if word.startswith("ٱ"):
             word = "ا" + word[1:]
-
         return word
 
 
-
-    def diacritics_syntax_error_in(diacritics_array):
+    def diacritics_syntax_error_in( diacriticsArray ) :
         """
         Check if the diacritics in the given array are incorrect.
 
         Args:
             diacritics_array (:obj:`list`): A list of diacritics to be checked.
 
         Returns:
@@ -225,57 +255,67 @@
 
             diacritics = ["َ", "ُ", "ِ", "ّ"]
             has_error = Implication.diacritics_syntax_error_in(diacritics)  # Returns False
 
             diacritics = ["َ", "ُ", "ِ", "ٓ"]
             has_error = Implication.diacritics_syntax_error_in(diacritics)  # Returns True
         """
+        # This funcion return True when the diacritics is incorreclty 
         try:
-            # Check last letter diacritic
-            if Implication.wrong_end_diacritic(diacritics_array[-1]):
+            # check last letter diacritic
+            if ( Implication.wrong_end_diacritic(diacriticsArray[ len(diacriticsArray) - 1]) ) : 
                 return True
-            else:
-                # Check all letters diacritic except the last letter diacritic
-                for i in range(len(diacritics_array) - 1):
-                    if Implication.wrong_middle_diacritic(diacritics_array[i]):
-                        return True
+            else :
+                # check All letters diacritic except the last letter diacritic
+                for i in range(0 , len(diacriticsArray) - 1 ) :
+                    if (Implication.wrong_middle_iacritic(diacriticsArray[i])) :
+                        return True 
                 return False
-        except:
-            return False
             
+        except :
+            return False
+        
 
     def wrong_end_diacritic(diac):
         """
         Check if the given diacritic is a wrong end diacritic.
 
         Args:
             diac (:obj:`int`): The diacritic value to be checked.
 
         Returns:
-            :obj:`bool`: True if the diacritic is a wrong end diacritic, False otherwise.
+            :obj:`bool`: True if the diacritic is one of the follwoing number (85:SHADDAH WITH FATHATAN, 86:SHADDAH WITH KASRTA, 87:SHADDAH WITH DHAMTAN), False if diacritic is greator than or equal0 and diacritic is less than or equal 11.
 
         **Example:**
 
         .. highlight:: python
         .. code-block:: python
 
             from nlptools.utils.implication import Implication 
 
             diacritic = 0
             is_wrong_end = Implication.wrong_end_diacritic(diacritic)  # Returns False
 
             diacritic = 85
             is_wrong_end = Implication.wrong_end_diacritic(diacritic)  # Returns True
         """
-        if diac >= 0 and diac <= 11:
+        # 0 > No Diacritics , 1 > SUKUN, 2 > FATHA, 3 > KASRA, 4 > DAMMA, 5 > FATHATAN, 6 > KASRATAN,
+        #  7 > DAMMATAN, 8 > SHADDA, 9 > SHADDA with FATHA, 10 > SHADDA with KASRA, 11 > SHADDA with DAMMA
+        if (diac >= 0 and diac <= 11) :
             return False
-        else:
-            # 85 - 86 - 87: SHADDAH WITH FATHATAN, SHADDAH WITH KASRTA, SHADDAH WITH DHAMTAN
+        else :
+            # 85 - 86 - 87: SHADDAH WITH FATHATAN,SHADDAH WITH KASRTA, SHADDAH WITH DHAMTAN
             return diac < 85 or diac > 87
+        
+    def wrong_middle_iacritic( diac) :
 
+        if (diac >= 0 and diac <= 4) :
+            return False
+        else :
+            return diac < 8 or diac > 15
             
     
     def calculate_words_implication(self):
         """
         Calculate the implication between two words.
 
         This method updates the verdict, direction, distance, and conflicts attributes of the object based on the implication between the words.
@@ -294,44 +334,46 @@
             implication.calculate_words_implication()
             # Access the updated attributes
             verdict = implication.verdict
             direction = implication.direction
             distance = implication.distance
             conflicts = implication.conflicts
         """
+
         self.verdict = "Incompatible"
-        self.direction = -2
+        self.direction = -2 
         self.distance = 1000
-
-        if Implication.equal_words(self) is False:
-            if len(self.word1Undiac) == 0 and len(self.word2Undiac) == 0:
-                if self.word1 == self.word2:
+        if (Implication.equal_words(self) == False): # If both words are not thge same return these values 
+            if ((len(self.word1Undiac) == 0 and len(self.word2Undiac) == 0)):
+                if (self.word1 == self.word2): 
                     self.conflicts = 0
                     self.distance = 0
-                    self.direction = 3
+                    self.direction = 3 
                 else:
                     self.conflicts = 1
                     self.distance = 1000
-                    self.direction = -2
+                    self.direction = -2 
+                
             else:
                 self.conflicts = max(len(self.word1Undiac), len(self.word2Undiac))
+            
         else:
-            if Implication.calculate_letters_implication(self):
+            if (Implication.calculate_letters_implication(self)):
                 self.direction = Implication.calculate_direction(self)
-                if self.direction == -1:
+                if (self.direction == -1) :
                     self.distance = 101
                 else:
                     self.verdict = "Compatible"
+                
             else:
-                self.direction = -3
+                self.direction = -3 # the two words have different letters
                 self.distance = 3000
                 self.conflicts = 0
 
-
-    def equal_words(self):
+    def equal_words( self ) :
         """
         Check if the two words are equal, taking into account the alif as the first letter.
 
         This method updates the word1Undiac and word2Undiac attributes by removing the first letter, and returns True if the words are equal, False otherwise.
 
         Returns:
             :obj:`bool`: True if the words are equal, False otherwise.
@@ -346,122 +388,125 @@
             implication = Implication(word1, word2)
             result = implication.equal_words()
             if result:
                 print("The words are equal")
             else:
                 print("The words are not equal")
         """
-        word1_first_letter = self.word1Undiac[0:1]  # First letter in word1
-        word2_first_letter = self.word2Undiac[0:1]  # First letter in word2
-        self.word1Undiac = self.word1Undiac[1:]  # All word1 letters without diacritics except first letter
-        self.word2Undiac = self.word2Undiac[1:]  # All word2 letters without diacritics except first letter
-
-        if self.word1Undiac != self.word2Undiac:
+       # check if the tow words are the same taking into account the alif as the first letter 
+        word1FirstLetter = self.word1Undiac[0 : 1] # First letter in word1 
+        word2FirstLetter = self.word2Undiac[0 : 1] # First letter in word2 
+        self.word1Undiac =  self.word1Undiac[1 : ] # all word1 letters without diacritics except first letter 
+        self.word2Undiac =  self.word2Undiac[1 : ] # all word2 letters without diacritics except first letter 
+        
+        # If both words withot first letter are not equal return false, otherwise continue 
+        if ( self.word1Undiac != self.word2Undiac):
             return False
 
-        if word1_first_letter == word2_first_letter:
+        # If the first letter in both words the same and (the other letters are the same) then return true, otherwise continue  
+        if word1FirstLetter == word2FirstLetter :
             return True
 
-        if word1_first_letter != "ا" or (word2_first_letter not in ["آ", "أ", "إ"]):
-            if (word1_first_letter in ["آ", "أ", "إ"]) and word2_first_letter == "ا":
-                self.lettersDirection[0] = 2  # w2 implies w1
+        # check if first letter is any alif (the other letters are the same) then return below values 
+        if (word1FirstLetter != "ا" or word2FirstLetter != "آ" and word2FirstLetter != "أ" and word2FirstLetter != "إ") :
+            if ((word1FirstLetter == "آ" or word1FirstLetter == "أ" or word1FirstLetter == "إ") and word2FirstLetter == "ا") :
+                self.lettersDirection[0] = 2 # w2 implies w1
                 self.conflictFlags[3] = True
                 return True
             else:
                 return False
         else:
-            self.lettersDirection[0] = 1  # w1 implies w2
+            self.lettersDirection[0] = 1 # w1 implies w2
             self.conflictFlags[2] = True
             return True
-
+        
         return False
 
-    def calculate_letters_implication(self):
+       
+    def calculate_letters_implication(self) :
         """
-        Calculate the implication between each pair of diacritics in the words.
-
         This method updates the lettersDirection, conflictFlags, and distance attributes based on the directionTable and distanceTable values for each pair of diacritics. It returns True after the calculation is completed.
 
         Returns:
-            bool: True indicating the calculation is completed.
+            :obj:`bool`: True indicating the calculation is completed.
 
         **Example:**
 
         .. highlight:: python
         .. code-block:: python
 
             from nlptools.utils.implication import Implication
 
             implication = Implication(word1, word2)
             result = implication.calculate_letters_implication()
             if result:
                 print("Letters implication calculation completed")
         """
         self.distance = 0
-        word1_diac = 0
-        word2_diac = 0
-
-        for i in range(0, len(self.word1Diacritics) - 1):
-            word1_diac = self.word1Diacritics[i]
-            word2_diac = self.word2Diacritics[i]
-
-            self.lettersDirection[i + 1] = self.directionTable[word1_diac][word2_diac]
-            self.conflictFlags[self.lettersDirection[i + 1] + 1] = True
-            self.distance = self.distance + self.distanceTable[word1_diac][word2_diac]
-
-        word1_diac = int(self.word1Diacritics[len(self.word1Diacritics) - 1])  # last letter diacritics for word1
-        word2_diac = int(self.word2Diacritics[len(self.word1Diacritics) - 1])  # last letter diacritics for word2
+        word1Diac = 0
+        word2Diac = 0
+  
+        for i in range ( 0 , len(self.word1Diacritics) - 1) :
+            word1Diac = self.word1Diacritics[i];
+            word2Diac = self.word2Diacritics[i];
+
+            self.lettersDirection[i + 1] = self.directionTable[word1Diac][word2Diac];
+            self.conflictFlags[self.lettersDirection[i + 1] + 1] = True;
+            self.distance = self.distance + self.distanceTable[word1Diac][word2Diac];
+
+               
+        word1Diac = int( self.word1Diacritics[len(self.word1Diacritics) - 1] ) # last letter diacritics to word1
+        word2Diac = int( self.word2Diacritics[len(self.word1Diacritics) - 1] ) # last letter diacritics to word2
         # 8: expresses the presence of shaddah
-        if word1_diac == 8 or word2_diac == 8:
-            self.lettersDirection[len(self.lettersDirection) - 1] = self.directionTable[word1_diac][word2_diac]
+        if (word1Diac == 8 or word2Diac == 8) :
+            self.lettersDirection[len(self.lettersDirection) - 1] = self.directionTable[word1Diac][word2Diac]
             self.conflictFlags[self.lettersDirection[len(self.lettersDirection) - 1] + 1] = True
-            self.distance = self.distance + self.distanceTable[word1_diac][word2_diac]
-        
+            self.distance = self.distance + self.distanceTable[word1Diac][word2Diac]
         return True
 
         
-    def calculate_direction(self):
+    def calculate_direction(self ): 
         """
         Calculates the direction of compatibility based on conflict flags.
 
         Returns:
             :obj:`int`: The direction of compatibility:
                 -1: Incompatible-diacritics
                 0: Compatible-imply each other
                 1: Compatible-w1 implies w2
                 2: Compatible-w2 implies w1
                 3: Compatible-exactly equal
                 -2147483648: Default value for an invalid direction
         """
         self.conflicts = 0
-
-        if self.conflictFlags[0] is True:
-            return -1  # Incompatible-diacritics
-
-        if self.conflictFlags[2] is True and self.conflictFlags[3] is True:
-            return 0  # Compatible-imply each other
-
-        if self.conflictFlags[2] is True and self.conflictFlags[3] is False:
-            return 1  # Compatible-w1 implies w2
-
-        if self.conflictFlags[2] is False and self.conflictFlags[3] is True:
-            return 2  # Compatible-w2 implies w1
-
-        if self.conflictFlags[4]:
-            return 3  # Compatible-exactly equal
-
+        if (self.conflictFlags[0] == True): 
+            return -1 # Incompatible-diacritics
+        
+        if (self.conflictFlags[2] == True and self.conflictFlags[3] == True ):
+            return 0 # Compatible-imply each other
+        
+        if (self.conflictFlags[2] == True and self.conflictFlags[3] == False ):
+            return 1 # Compatible-w1 implies w2
+        
+        if (self.conflictFlags[2] == False and self.conflictFlags[3] == True ):
+            return 2 # Compatible-w2 implies w1
+        
+        if (self.conflictFlags[4]):
+            return 3 # Compatible-exactly equal
+        
         return -2147483648
 
 
-    def calculate_direction( word ):
+
+    def get_diacritics_array(word): 
         """
         Converts diacritics in a word to digits and returns the array of diacritics.
 
         Args:
-            word (:obj:`str`): The word containing diacritics.
+            word (:obj:`str`): The word with diacritics.
 
         Returns:
             :obj:`list`: The array of diacritics converted to digits.
 
         Raises:
             Exception: If the first character of the word is a digit.
 
@@ -532,30 +577,28 @@
         
         # Convert string array digits to integer digits array 
         for x in range(0 , len(strDiacritics) ):
             diacritics[x] = int(strDiacritics[x])
         return diacritics
     
     # def removeDiacritics( word ): # remove all diacritics from Arabic word
-    #     # word = word.replace(" ", "")
-    #     # word = word.replace("ْ", "") #SUKUN
-    #     # word = word.replace("َ", "") #FATHA
-    #     # word = word.replace("ِ", "") #KASRA
-    #     # word = word.replace("ُ", "") #DAMMA
-    #     # word = word.replace("ً", "") #FATHATAN
-    #     # word = word.replace("ٍ", "") #KASRATAN
-    #     # word = word.replace("ٌ", "") #DAMMATAN
-    #     # word = word.replace("ّ", "") #SHADD
-    #     #word = word.sub(r'[\u064B-\u0650]+', '',word) # Remove all Arabic diacretics [ ًٌٍَُِْ]A
-    #     word = arStrip(word,diacs=False , shaddah=False)
+    #     word = word.replace(" ", "")
+    #     word = word.replace("ْ", "") #SUKUN
+    #     word = word.replace("َ", "") #FATHA
+    #     word = word.replace("ِ", "") #KASRA
+    #     word = word.replace("ُ", "") #DAMMA
+    #     word = word.replace("ً", "") #FATHATAN
+    #     word = word.replace("ٍ", "") #KASRATAN
+    #     word = word.replace("ٌ", "") #DAMMATAN
+    #     word = word.replace("ّ", "") #SHADDA
     #     return word
 
     def get_letters_array(word):
         """
-        Retrieves the array of letters from a given word.
+        Returns the array of letters from a given word.
 
         Args:
             word (:obj:`str`): The word from which to extract the letters.
 
         Returns:
             obj:`list`: The array of letters.
 
@@ -569,15 +612,14 @@
             letters = get_letters_array(word)
             print(letters)
             Output: ['م', 'ر', 'ح', 'ب', 'ا']
         """
         word = arStrip(word, diacs=False, shaddah=False)
         return list(word)
 
-
     def get_verdict(self ): 
         return self.verdict
 
 
     def get_direction(self): 
         return self.direction
 
@@ -595,18 +637,18 @@
 
 
     def get_word2(self) :
         return self.word2 
 
     def get_result(self):
         """
-        Retrieves the result of the comparison between two words.
+        Returns the result of the comparison between two words.
 
         Returns:
-            :obj:`str`: The result of the comparison. Can be "Same" or "Different".
+            :obj:`str`: The result of the comparison. Can be *Same* or *Different*.
 
         **Example:**
 
         .. highlight:: python
         .. code-block:: python
 
             from nlptools.utils.implication import Implication
@@ -619,11 +661,10 @@
         """
         if Implication.get_direction(self) >= 0 and Implication.get_distance(self) < 15:
             self.result = "Same"
         else:
             self.result = "Different"
         return self.result
 
-
     def toString(self) :
         return self.word1 + "\t" + self.word2 + "\t" + str(self.verdict) + "\t" + str(self.direction) + "\t" + str(self.distance) + "\t"+ str(self.conflicts)
```

### Comparing `nlptoolssna-0.8.6/nlptools/utils/jaccard.py` & `nlptoolssna-0.8.8/nlptools/utils/jaccard.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/utils/parser.py` & `nlptoolssna-0.8.8/nlptools/utils/parser.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptools/utils/text_transliteration.py` & `nlptoolssna-0.8.8/nlptools/utils/text_transliteration.py`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/nlptoolssna.egg-info/PKG-INFO` & `nlptoolssna-0.8.8/nlptoolssna.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nlptoolssna
-Version: 0.8.6
+Version: 0.8.8
 Summary: Python Boilerplate contains all the boilerplate you need to create a Python package.
 Home-page: https://github.com/eng-aomar/nlptools
 Author: Alaa' Omar
 Author-email: alaa.omer2009@gmail.com
 License: MIT license
 Keywords: nlptools
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `nlptoolssna-0.8.6/nlptoolssna.egg-info/SOURCES.txt` & `nlptoolssna-0.8.8/nlptoolssna.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/setup.cfg` & `nlptoolssna-0.8.8/setup.cfg`

 * *Files identical despite different names*

### Comparing `nlptoolssna-0.8.6/setup.py` & `nlptoolssna-0.8.8/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 requirements = [
     'six',
     'farasapy',
     'tqdm',
     'requests',
     'regex',
     'pathlib',
-    # 'torch==1.13.0',
+    # 'torch==1.13.1',
     # 'transformers==4.24.0',
     # 'torchtext==0.14.0',
     # 'torchvision==0.14.0',
     # 'torchdata==0.5.1',
     # 'seqeval==1.2.2'
 ]
```

