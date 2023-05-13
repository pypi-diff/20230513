# Comparing `tmp/cyberdrop-dl-4.2.19.tar.gz` & `tmp/cyberdrop-dl-4.2.21.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cyberdrop-dl-4.2.19.tar", last modified: Fri May 12 22:06:05 2023, max compression
+gzip compressed data, was "cyberdrop-dl-4.2.21.tar", last modified: Sat May 13 02:30:47 2023, max compression
```

## Comparing `cyberdrop-dl-4.2.19.tar` & `cyberdrop-dl-4.2.21.tar`

### file list

```diff
@@ -1,62 +1,62 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    17829 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    17394 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.004816 cyberdrop-dl-4.2.19/cyberdrop_dl/
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.004816 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3942 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/base_functions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4258 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/config_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3262 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/config_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     8468 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/data_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/error_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3450 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/sorting_functions.py
--rw-r--r--   0 runner    (1001) docker     (123)    12707 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/sql_helper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.004816 cyberdrop-dl-4.2.19/cyberdrop_dl/client/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10069 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/client/client.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/
--rw-r--r--   0 runner    (1001) docker     (123)     2095 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Anonfiles_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     7609 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Bunkr_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     7813 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Coomeno_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)    12738 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/CyberFile_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2920 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Cyberdrop_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2982 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/EHentai_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     4132 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Erome_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     4099 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Fapello_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Gfycat_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     4973 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/GoFile_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2762 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/HGameCG_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/ImgBox_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     3554 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/LoveFap_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     4282 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/NSFWXXX_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PimpAndHost_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     3240 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PixelDrain_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2886 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PostImg_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Saint_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     8745 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/ShareX_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)     2059 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/XBunkr_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)    13858 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Xenforo_Spider.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2922 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/downloader_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    17721 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/downloaders.py
--rw-r--r--   0 runner    (1001) docker     (123)    13146 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/old_downloaders.py
--rw-r--r--   0 runner    (1001) docker     (123)    17450 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/progress_definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)    19261 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/
--rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/JDownloader_Integration.py
--rw-r--r--   0 runner    (1001) docker     (123)    18907 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/Scraper.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:06:05.004816 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    17829 2023-05-12 22:06:04.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1933 2023-05-12 22:06:05.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:06:04.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-12 22:06:04.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      176 2023-05-12 22:06:04.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-12 22:06:04.000000 cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      860 2023-05-12 22:06:05.008817 cyberdrop-dl-4.2.19/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:05:48.000000 cyberdrop-dl-4.2.19/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.544670 cyberdrop-dl-4.2.21/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    17829 2023-05-13 02:30:47.544670 cyberdrop-dl-4.2.21/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    17394 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.536670 cyberdrop-dl-4.2.21/cyberdrop_dl/
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.540670 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3942 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/base_functions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4258 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/config_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3262 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/config_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8468 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/data_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/error_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3450 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/sorting_functions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12707 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/sql_helper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.540670 cyberdrop-dl-4.2.21/cyberdrop_dl/client/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10069 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/client/client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.540670 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/
+-rw-r--r--   0 runner    (1001) docker     (123)     2095 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Anonfiles_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7609 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Bunkr_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7813 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Coomeno_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12738 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/CyberFile_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2920 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Cyberdrop_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2982 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/EHentai_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4132 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Erome_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4099 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Fapello_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Gfycat_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4973 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/GoFile_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2762 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/HGameCG_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/ImgBox_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3554 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/LoveFap_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4282 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/NSFWXXX_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PimpAndHost_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3240 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PixelDrain_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2886 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PostImg_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Saint_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8745 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/ShareX_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2059 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/XBunkr_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13858 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Xenforo_Spider.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.544670 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2922 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/downloader_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17721 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/downloaders.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13146 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/old_downloaders.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17463 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/progress_definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19261 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.544670 cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/
+-rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/JDownloader_Integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18907 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/Scraper.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:30:47.536670 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    17829 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1933 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      176 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 02:30:47.000000 cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      860 2023-05-13 02:30:47.544670 cyberdrop-dl-4.2.21/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:30:38.000000 cyberdrop-dl-4.2.21/setup.py
```

### Comparing `cyberdrop-dl-4.2.19/LICENSE` & `cyberdrop-dl-4.2.21/LICENSE`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/PKG-INFO` & `cyberdrop-dl-4.2.21/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cyberdrop-dl
-Version: 4.2.19
+Version: 4.2.21
 Summary: Bulk downloader for multiple file hosts and forum sites
 Home-page: https://github.com/Jules-WinnfieldX/CyberDropDownloader
 Author: Jules-WinnfieldX
 Author-email: JulesWinnfieldII@protonmail.com
 Project-URL: Bug Tracker, https://github.com/Jules-WinnfieldX/CyberDropDownloader/issues
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: cyberdrop-dl Version: 4.2.19 Summary: Bulk
+Metadata-Version: 2.1 Name: cyberdrop-dl Version: 4.2.21 Summary: Bulk
 downloader for multiple file hosts and forum sites Home-page: https://
 github.com/Jules-WinnfieldX/CyberDropDownloader Author: Jules-WinnfieldX
 Author-email: JulesWinnfieldII@protonmail.com Project-URL: Bug Tracker, https:/
 /github.com/Jules-WinnfieldX/CyberDropDownloader/issues Requires-Python: >=3.7
 Description-Content-Type: text/markdown License-File: LICENSE # `cyberdrop-dl`
 **Bulk downloader for multiple file hosts** [![PyPI version](https://
 badge.fury.io/py/cyberdrop-dl.svg)](https://badge.fury.io/py/cyberdrop-dl) [!
```

### Comparing `cyberdrop-dl-4.2.19/README.md` & `cyberdrop-dl-4.2.21/README.md`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/base_functions.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/base_functions.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/config_manager.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/config_manager.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/config_schema.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/config_schema.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/data_classes.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/data_classes.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/error_classes.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/error_classes.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/sorting_functions.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/sorting_functions.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/base_functions/sql_helper.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/base_functions/sql_helper.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/client/client.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/client/client.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Anonfiles_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Anonfiles_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Bunkr_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Bunkr_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Coomeno_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Coomeno_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/CyberFile_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/CyberFile_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Cyberdrop_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Cyberdrop_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/EHentai_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/EHentai_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Erome_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Erome_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Fapello_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Fapello_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Gfycat_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Gfycat_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/GoFile_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/GoFile_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/HGameCG_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/HGameCG_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/ImgBox_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/ImgBox_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/LoveFap_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/LoveFap_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/NSFWXXX_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/NSFWXXX_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PimpAndHost_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PimpAndHost_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PixelDrain_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PixelDrain_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/PostImg_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/PostImg_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Saint_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Saint_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/ShareX_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/ShareX_Spider.py`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,15 @@
 
 
 class ShareXCrawler:
     def __init__(self, *, include_id=False, quiet: bool, SQL_Helper: SQLHelper):
         self.include_id = include_id
         self.quiet = quiet
         self.SQL_Helper = SQL_Helper
-        self.limiter = AsyncLimiter(15, 1)
+        self.limiter = AsyncLimiter(10, 1)
 
     async def fetch(self, session: ScrapeSession, url: URL) -> DomainItem:
         """Director for ShareX scraper"""
         assert url.host is not None
         domain_obj = DomainItem(url.host.lower(), {})
 
         log(f"Starting: {url}", quiet=self.quiet, style="green")
```

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/XBunkr_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/XBunkr_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/crawlers/Xenforo_Spider.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/crawlers/Xenforo_Spider.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/downloader_utils.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/downloader_utils.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/downloaders.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/downloaders.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/old_downloaders.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/old_downloaders.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/downloader/progress_definitions.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/downloader/progress_definitions.py`

 * *Files 0% similar despite different names*

```diff
@@ -184,15 +184,15 @@
         self.completed_tasks.append(task_id)
 
     def advance_task(self, task_id: TaskID, amount: int) -> None:
         self.progress.advance(task_id, amount)
 
     def update_total(self, task_id: TaskID, total: int) -> None:
         if task_id in self.invisible_tasks:
-            self.progress.update(task_id, visible=False)
+            self.progress.update(task_id, total=total, visible=False)
         elif task_id in self.visible_tasks:
             self.progress.update(task_id, total=total, visible=True)
         elif task_id in self.uninitiated_tasks:
             self.progress.update(task_id, total=total, visible=False)
             self.uninitiated_tasks.remove(task_id)
             self.invisible_tasks.append(task_id)
             self.redraw()
```

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/main.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/main.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/JDownloader_Integration.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/JDownloader_Integration.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl/scraper/Scraper.py` & `cyberdrop-dl-4.2.21/cyberdrop_dl/scraper/Scraper.py`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/PKG-INFO` & `cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cyberdrop-dl
-Version: 4.2.19
+Version: 4.2.21
 Summary: Bulk downloader for multiple file hosts and forum sites
 Home-page: https://github.com/Jules-WinnfieldX/CyberDropDownloader
 Author: Jules-WinnfieldX
 Author-email: JulesWinnfieldII@protonmail.com
 Project-URL: Bug Tracker, https://github.com/Jules-WinnfieldX/CyberDropDownloader/issues
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: cyberdrop-dl Version: 4.2.19 Summary: Bulk
+Metadata-Version: 2.1 Name: cyberdrop-dl Version: 4.2.21 Summary: Bulk
 downloader for multiple file hosts and forum sites Home-page: https://
 github.com/Jules-WinnfieldX/CyberDropDownloader Author: Jules-WinnfieldX
 Author-email: JulesWinnfieldII@protonmail.com Project-URL: Bug Tracker, https:/
 /github.com/Jules-WinnfieldX/CyberDropDownloader/issues Requires-Python: >=3.7
 Description-Content-Type: text/markdown License-File: LICENSE # `cyberdrop-dl`
 **Bulk downloader for multiple file hosts** [![PyPI version](https://
 badge.fury.io/py/cyberdrop-dl.svg)](https://badge.fury.io/py/cyberdrop-dl) [!
```

### Comparing `cyberdrop-dl-4.2.19/cyberdrop_dl.egg-info/SOURCES.txt` & `cyberdrop-dl-4.2.21/cyberdrop_dl.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `cyberdrop-dl-4.2.19/setup.cfg` & `cyberdrop-dl-4.2.21/setup.cfg`

 * *Files identical despite different names*

