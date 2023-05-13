# Comparing `tmp/py-Ayra-8.7.4.tar.gz` & `tmp/py-Ayra-8.7.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py-Ayra-8.7.4.tar", last modified: Sat May  6 19:01:17 2023, max compression
+gzip compressed data, was "py-Ayra-8.7.5.tar", last modified: Sat May 13 17:26:51 2023, max compression
```

## Comparing `py-Ayra-8.7.4.tar` & `py-Ayra-8.7.5.tar`

### file list

```diff
@@ -1,77 +1,77 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.150447 py-Ayra-8.7.4/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.142446 py-Ayra-8.7.4/Ayra/
--rw-r--r--   0 root         (0) root         (0)     3004 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/__init__.py
--rw-r--r--   0 root         (0) root         (0)     2736 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/__main__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.142446 py-Ayra-8.7.4/Ayra/_misc/
--rw-r--r--   0 root         (0) root         (0)     1866 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/_misc/__init__.py
--rw-r--r--   0 root         (0) root         (0)     4805 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/_misc/_assistant.py
--rw-r--r--   0 root         (0) root         (0)    12369 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/_misc/_decorators.py
--rw-r--r--   0 root         (0) root         (0)     4157 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/_misc/_supporter.py
--rw-r--r--   0 root         (0) root         (0)     1912 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/_misc/_wrappers.py
--rw-r--r--   0 root         (0) root         (0)     1964 2023-05-06 06:05:13.000000 py-Ayra-8.7.4/Ayra/configs.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.146446 py-Ayra-8.7.4/Ayra/dB/
--rw-r--r--   0 root         (0) root         (0)     1962 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/dB/__init__.py
--rw-r--r--   0 root         (0) root         (0)      304 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/_core.py
--rw-r--r--   0 root         (0) root         (0)      808 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/afk_db.py
--rw-r--r--   0 root         (0) root         (0)      704 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/antiflood_db.py
--rw-r--r--   0 root         (0) root         (0)      827 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/asst_fns.py
--rw-r--r--   0 root         (0) root         (0)      852 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/asstcmd_db.py
--rw-r--r--   0 root         (0) root         (0)     1943 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/autoban_db.py
--rw-r--r--   0 root         (0) root         (0)      391 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/blacklist_chat_db.py
--rw-r--r--   0 root         (0) root         (0)     1010 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/blacklist_db.py
--rw-r--r--   0 root         (0) root         (0)      893 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/botchat_db.py
--rw-r--r--   0 root         (0) root         (0)      752 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/broadcast_db.py
--rw-r--r--   0 root         (0) root         (0)     1727 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/ch_db.py
--rw-r--r--   0 root         (0) root         (0)      618 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/dnd_db.py
--rw-r--r--   0 root         (0) root         (0)      956 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/echo_db.py
--rw-r--r--   0 root         (0) root         (0)      729 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/filestore_db.py
--rw-r--r--   0 root         (0) root         (0)     1105 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/filter_db.py
--rw-r--r--   0 root         (0) root         (0)      789 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/forcesub_db.py
--rw-r--r--   0 root         (0) root         (0)     1042 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/gban_mute_db.py
--rw-r--r--   0 root         (0) root         (0)      812 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/gcast_blacklist_db.py
--rw-r--r--   0 root         (0) root         (0)     1490 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/greetings_db.py
--rw-r--r--   0 root         (0) root         (0)      595 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/logusers_db.py
--rw-r--r--   0 root         (0) root         (0)      757 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/mute_db.py
--rw-r--r--   0 root         (0) root         (0)      624 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/night_db.py
--rw-r--r--   0 root         (0) root         (0)     1195 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/notes_db.py
--rw-r--r--   0 root         (0) root         (0)     1002 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/nsfw_db.py
--rw-r--r--   0 root         (0) root         (0)      646 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/pmpermit_db.py
--rw-r--r--   0 root         (0) root         (0)      788 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/snips_db.py
--rw-r--r--   0 root         (0) root         (0)      623 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/vc_sudos.py
--rw-r--r--   0 root         (0) root         (0)      897 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/dB/warn_db.py
--rw-r--r--   0 root         (0) root         (0)      485 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/exceptions.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.146446 py-Ayra-8.7.4/Ayra/fns/
--rw-r--r--   0 root         (0) root         (0)    12365 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/FastTelethon.py
--rw-r--r--   0 root         (0) root         (0)     1143 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/__init__.py
--rw-r--r--   0 root         (0) root         (0)     5308 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/admins.py
--rw-r--r--   0 root         (0) root         (0)     2195 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/executor.py
--rw-r--r--   0 root         (0) root         (0)     9150 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/gDrive.py
--rw-r--r--   0 root         (0) root         (0)    43096 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/google_image.py
--rw-r--r--   0 root         (0) root         (0)    19988 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/fns/helper.py
--rw-r--r--   0 root         (0) root         (0)     7427 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/info.py
--rw-r--r--   0 root         (0) root         (0)    17343 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/misc.py
--rw-r--r--   0 root         (0) root         (0)    28822 2023-05-03 20:26:34.000000 py-Ayra-8.7.4/Ayra/fns/tools.py
--rw-r--r--   0 root         (0) root         (0)     8262 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/fns/ytdl.py
--rw-r--r--   0 root         (0) root         (0)     9174 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/kynan.py
--rw-r--r--   0 root         (0) root         (0)     2787 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/loader.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.150447 py-Ayra-8.7.4/Ayra/startup/
--rw-r--r--   0 root         (0) root         (0)     8452 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/BaseClient.py
--rw-r--r--   0 root         (0) root         (0)     2573 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/startup/__init__.py
--rw-r--r--   0 root         (0) root         (0)     9774 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/_database.py
--rw-r--r--   0 root         (0) root         (0)      820 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/_extra.py
--rw-r--r--   0 root         (0) root         (0)     2933 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/connections.py
--rw-r--r--   0 root         (0) root         (0)    18378 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/startup/funcs.py
--rw-r--r--   0 root         (0) root         (0)     2289 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/loader.py
--rw-r--r--   0 root         (0) root         (0)     2836 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/Ayra/startup/utils.py
--rw-r--r--   0 root         (0) root         (0)       45 2023-05-06 19:00:55.000000 py-Ayra-8.7.4/Ayra/version.py
--rw-r--r--   0 root         (0) root         (0)    35182 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/LICENSE
--rw-r--r--   0 root         (0) root         (0)     3387 2023-05-06 19:01:17.150447 py-Ayra-8.7.4/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     2570 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-06 19:01:17.150447 py-Ayra-8.7.4/py_Ayra.egg-info/
--rw-r--r--   0 root         (0) root         (0)     3387 2023-05-06 19:01:17.000000 py-Ayra-8.7.4/py_Ayra.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     1466 2023-05-06 19:01:17.000000 py-Ayra-8.7.4/py_Ayra.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-06 19:01:17.000000 py-Ayra-8.7.4/py_Ayra.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-06 19:01:17.000000 py-Ayra-8.7.4/py_Ayra.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        5 2023-05-06 19:01:17.000000 py-Ayra-8.7.4/py_Ayra.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-06 19:01:17.150447 py-Ayra-8.7.4/setup.cfg
--rw-r--r--   0 root         (0) root         (0)     1496 2023-05-03 16:58:28.000000 py-Ayra-8.7.4/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.394356 py-Ayra-8.7.5/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.386355 py-Ayra-8.7.5/Ayra/
+-rw-r--r--   0 root         (0) root         (0)     3004 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     2736 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/__main__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.386355 py-Ayra-8.7.5/Ayra/_misc/
+-rw-r--r--   0 root         (0) root         (0)     1866 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/_misc/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     4805 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/_misc/_assistant.py
+-rw-r--r--   0 root         (0) root         (0)    12369 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/_misc/_decorators.py
+-rw-r--r--   0 root         (0) root         (0)     4157 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/_misc/_supporter.py
+-rw-r--r--   0 root         (0) root         (0)     1912 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/_misc/_wrappers.py
+-rw-r--r--   0 root         (0) root         (0)     1964 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/configs.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.390356 py-Ayra-8.7.5/Ayra/dB/
+-rw-r--r--   0 root         (0) root         (0)     1962 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      304 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/_core.py
+-rw-r--r--   0 root         (0) root         (0)      808 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/afk_db.py
+-rw-r--r--   0 root         (0) root         (0)      704 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/antiflood_db.py
+-rw-r--r--   0 root         (0) root         (0)      827 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/asst_fns.py
+-rw-r--r--   0 root         (0) root         (0)      852 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/asstcmd_db.py
+-rw-r--r--   0 root         (0) root         (0)     1943 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/autoban_db.py
+-rw-r--r--   0 root         (0) root         (0)      391 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/blacklist_chat_db.py
+-rw-r--r--   0 root         (0) root         (0)     1010 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/blacklist_db.py
+-rw-r--r--   0 root         (0) root         (0)      893 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/botchat_db.py
+-rw-r--r--   0 root         (0) root         (0)      752 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/broadcast_db.py
+-rw-r--r--   0 root         (0) root         (0)     1727 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/ch_db.py
+-rw-r--r--   0 root         (0) root         (0)      618 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/dnd_db.py
+-rw-r--r--   0 root         (0) root         (0)      956 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/echo_db.py
+-rw-r--r--   0 root         (0) root         (0)      729 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/filestore_db.py
+-rw-r--r--   0 root         (0) root         (0)     1105 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/filter_db.py
+-rw-r--r--   0 root         (0) root         (0)      789 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/forcesub_db.py
+-rw-r--r--   0 root         (0) root         (0)     1042 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/gban_mute_db.py
+-rw-r--r--   0 root         (0) root         (0)      812 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/gcast_blacklist_db.py
+-rw-r--r--   0 root         (0) root         (0)     1490 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/greetings_db.py
+-rw-r--r--   0 root         (0) root         (0)      595 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/logusers_db.py
+-rw-r--r--   0 root         (0) root         (0)      757 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/mute_db.py
+-rw-r--r--   0 root         (0) root         (0)      624 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/night_db.py
+-rw-r--r--   0 root         (0) root         (0)     1195 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/notes_db.py
+-rw-r--r--   0 root         (0) root         (0)     1002 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/nsfw_db.py
+-rw-r--r--   0 root         (0) root         (0)      646 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/pmpermit_db.py
+-rw-r--r--   0 root         (0) root         (0)      788 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/snips_db.py
+-rw-r--r--   0 root         (0) root         (0)      623 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/vc_sudos.py
+-rw-r--r--   0 root         (0) root         (0)      897 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/dB/warn_db.py
+-rw-r--r--   0 root         (0) root         (0)      485 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/exceptions.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.390356 py-Ayra-8.7.5/Ayra/fns/
+-rw-r--r--   0 root         (0) root         (0)    12365 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/FastTelethon.py
+-rw-r--r--   0 root         (0) root         (0)     1143 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     5308 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/admins.py
+-rw-r--r--   0 root         (0) root         (0)     2195 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/executor.py
+-rw-r--r--   0 root         (0) root         (0)     9150 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/gDrive.py
+-rw-r--r--   0 root         (0) root         (0)    43096 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/google_image.py
+-rw-r--r--   0 root         (0) root         (0)    20173 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/helper.py
+-rw-r--r--   0 root         (0) root         (0)     7427 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/info.py
+-rw-r--r--   0 root         (0) root         (0)    17343 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/misc.py
+-rw-r--r--   0 root         (0) root         (0)    28822 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/tools.py
+-rw-r--r--   0 root         (0) root         (0)     8262 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/fns/ytdl.py
+-rw-r--r--   0 root         (0) root         (0)     9174 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/kynan.py
+-rw-r--r--   0 root         (0) root         (0)     2787 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/loader.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.390356 py-Ayra-8.7.5/Ayra/startup/
+-rw-r--r--   0 root         (0) root         (0)     8452 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/BaseClient.py
+-rw-r--r--   0 root         (0) root         (0)     2573 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     9774 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/_database.py
+-rw-r--r--   0 root         (0) root         (0)      820 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/_extra.py
+-rw-r--r--   0 root         (0) root         (0)     2933 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/connections.py
+-rw-r--r--   0 root         (0) root         (0)    18384 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/funcs.py
+-rw-r--r--   0 root         (0) root         (0)     2289 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/loader.py
+-rw-r--r--   0 root         (0) root         (0)     2836 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/startup/utils.py
+-rw-r--r--   0 root         (0) root         (0)       45 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/Ayra/version.py
+-rw-r--r--   0 root         (0) root         (0)    35182 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     3387 2023-05-13 17:26:51.394356 py-Ayra-8.7.5/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     2570 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:26:51.394356 py-Ayra-8.7.5/py_Ayra.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     3387 2023-05-13 17:26:51.000000 py-Ayra-8.7.5/py_Ayra.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     1466 2023-05-13 17:26:51.000000 py-Ayra-8.7.5/py_Ayra.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:26:51.000000 py-Ayra-8.7.5/py_Ayra.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:26:51.000000 py-Ayra-8.7.5/py_Ayra.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        5 2023-05-13 17:26:51.000000 py-Ayra-8.7.5/py_Ayra.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:26:51.394356 py-Ayra-8.7.5/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)     1496 2023-05-13 17:26:33.000000 py-Ayra-8.7.5/setup.py
```

### Comparing `py-Ayra-8.7.4/Ayra/__init__.py` & `py-Ayra-8.7.5/Ayra/__init__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/__main__.py` & `py-Ayra-8.7.5/Ayra/__main__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/_misc/__init__.py` & `py-Ayra-8.7.5/Ayra/_misc/__init__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/_misc/_assistant.py` & `py-Ayra-8.7.5/Ayra/_misc/_assistant.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/_misc/_decorators.py` & `py-Ayra-8.7.5/Ayra/_misc/_decorators.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/_misc/_supporter.py` & `py-Ayra-8.7.5/Ayra/_misc/_supporter.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/_misc/_wrappers.py` & `py-Ayra-8.7.5/Ayra/_misc/_wrappers.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/configs.py` & `py-Ayra-8.7.5/Ayra/configs.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/__init__.py` & `py-Ayra-8.7.5/Ayra/dB/__init__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/afk_db.py` & `py-Ayra-8.7.5/Ayra/dB/afk_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/antiflood_db.py` & `py-Ayra-8.7.5/Ayra/dB/antiflood_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/asst_fns.py` & `py-Ayra-8.7.5/Ayra/dB/asst_fns.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/asstcmd_db.py` & `py-Ayra-8.7.5/Ayra/dB/asstcmd_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/autoban_db.py` & `py-Ayra-8.7.5/Ayra/dB/autoban_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/blacklist_db.py` & `py-Ayra-8.7.5/Ayra/dB/blacklist_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/botchat_db.py` & `py-Ayra-8.7.5/Ayra/dB/botchat_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/broadcast_db.py` & `py-Ayra-8.7.5/Ayra/dB/broadcast_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/ch_db.py` & `py-Ayra-8.7.5/Ayra/dB/ch_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/dnd_db.py` & `py-Ayra-8.7.5/Ayra/dB/dnd_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/echo_db.py` & `py-Ayra-8.7.5/Ayra/dB/echo_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/filestore_db.py` & `py-Ayra-8.7.5/Ayra/dB/filestore_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/filter_db.py` & `py-Ayra-8.7.5/Ayra/dB/filter_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/forcesub_db.py` & `py-Ayra-8.7.5/Ayra/dB/forcesub_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/gban_mute_db.py` & `py-Ayra-8.7.5/Ayra/dB/gban_mute_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/gcast_blacklist_db.py` & `py-Ayra-8.7.5/Ayra/dB/gcast_blacklist_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/greetings_db.py` & `py-Ayra-8.7.5/Ayra/dB/greetings_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/logusers_db.py` & `py-Ayra-8.7.5/Ayra/dB/logusers_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/mute_db.py` & `py-Ayra-8.7.5/Ayra/dB/mute_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/night_db.py` & `py-Ayra-8.7.5/Ayra/dB/night_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/notes_db.py` & `py-Ayra-8.7.5/Ayra/dB/notes_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/nsfw_db.py` & `py-Ayra-8.7.5/Ayra/dB/nsfw_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/pmpermit_db.py` & `py-Ayra-8.7.5/Ayra/dB/pmpermit_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/snips_db.py` & `py-Ayra-8.7.5/Ayra/dB/snips_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/vc_sudos.py` & `py-Ayra-8.7.5/Ayra/dB/vc_sudos.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/dB/warn_db.py` & `py-Ayra-8.7.5/Ayra/dB/warn_db.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/FastTelethon.py` & `py-Ayra-8.7.5/Ayra/fns/FastTelethon.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/__init__.py` & `py-Ayra-8.7.5/Ayra/fns/__init__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/admins.py` & `py-Ayra-8.7.5/Ayra/fns/admins.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/executor.py` & `py-Ayra-8.7.5/Ayra/fns/executor.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/gDrive.py` & `py-Ayra-8.7.5/Ayra/fns/gDrive.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/google_image.py` & `py-Ayra-8.7.5/Ayra/fns/google_image.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/helper.py` & `py-Ayra-8.7.5/Ayra/fns/helper.py`

 * *Files 1% similar despite different names*

```diff
@@ -35,15 +35,15 @@
 except ImportError:
     heroku3 = None
 
 try:
     from git import Repo
     from git.exc import GitCommandError, InvalidGitRepositoryError, NoSuchPathError
 except ImportError:
-    Repo = None
+    Repo = "https://github.com/naya1503/Naya-Userbot"
 
 
 import asyncio
 import multiprocessing
 from concurrent.futures import ThreadPoolExecutor
 from functools import partial, wraps
 
@@ -550,14 +550,19 @@
                 "Ayra",
                 sys.argv[1],
                 sys.argv[2],
                 sys.argv[3],
                 sys.argv[4],
                 sys.argv[5],
                 sys.argv[6],
+                sys.argv[7],
+                sys.argv[8],
+                sys.argv[9],
+                sys.argv[10],
+                sys.argv[11],
             )
 
 
 async def shutdown(ay):
     from .. import HOSTED_ON, LOGS
 
     ay = await eor(ay, "Mematikan")
```

### Comparing `py-Ayra-8.7.4/Ayra/fns/info.py` & `py-Ayra-8.7.5/Ayra/fns/info.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/misc.py` & `py-Ayra-8.7.5/Ayra/fns/misc.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/tools.py` & `py-Ayra-8.7.5/Ayra/fns/tools.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/fns/ytdl.py` & `py-Ayra-8.7.5/Ayra/fns/ytdl.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/kynan.py` & `py-Ayra-8.7.5/Ayra/kynan.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/loader.py` & `py-Ayra-8.7.5/Ayra/loader.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/BaseClient.py` & `py-Ayra-8.7.5/Ayra/startup/BaseClient.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/__init__.py` & `py-Ayra-8.7.5/Ayra/startup/__init__.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/_database.py` & `py-Ayra-8.7.5/Ayra/startup/_database.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/_extra.py` & `py-Ayra-8.7.5/Ayra/startup/_extra.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/connections.py` & `py-Ayra-8.7.5/Ayra/startup/connections.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/funcs.py` & `py-Ayra-8.7.5/Ayra/startup/funcs.py`

 * *Files 0% similar despite different names*

```diff
@@ -152,15 +152,15 @@
     from .. import udB, ayra_bot
 
     if udB.get_key("BOT_TOKEN"):
         return
     await ayra_bot.start()
     LOGS.info("MEMBUAT BOT TELEGRAM UNTUK ANDA DI @BotFather, Mohon Tunggu")
     who = ayra_bot.me
-    name = who.first_name + "Bot"
+    name = who.first_name + "Asisstant"
     if who.username:
         username = who.username + "_bot"
     else:
         username = "nay_" + (str(who.id))[5:] + "_bot"
     bf = "@BotFather"
     await ayra_bot(UnblockRequest(bf))
     await ayra_bot.send_message(bf, "/cancel")
```

### Comparing `py-Ayra-8.7.4/Ayra/startup/loader.py` & `py-Ayra-8.7.5/Ayra/startup/loader.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/Ayra/startup/utils.py` & `py-Ayra-8.7.5/Ayra/startup/utils.py`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/LICENSE` & `py-Ayra-8.7.5/LICENSE`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/PKG-INFO` & `py-Ayra-8.7.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-Ayra
-Version: 8.7.4
+Version: 8.7.5
 Summary: A Secure and Powerful Python-Telethon Based Library For Ayra Userbot.
 Home-page: https://github.com/naya1503/pyAyra
 Author: naya1503
 Author-email: cosmospanas70@gmail.com
 License: GNU AFFERO GENERAL PUBLIC LICENSE (v3)
 Project-URL: Bug Tracker, https://github.com/naya1503/pyAyra/issues
 Project-URL: Documentation, https://ultroid.tech
```

### Comparing `py-Ayra-8.7.4/README.md` & `py-Ayra-8.7.5/README.md`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/py_Ayra.egg-info/PKG-INFO` & `py-Ayra-8.7.5/py_Ayra.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-Ayra
-Version: 8.7.4
+Version: 8.7.5
 Summary: A Secure and Powerful Python-Telethon Based Library For Ayra Userbot.
 Home-page: https://github.com/naya1503/pyAyra
 Author: naya1503
 Author-email: cosmospanas70@gmail.com
 License: GNU AFFERO GENERAL PUBLIC LICENSE (v3)
 Project-URL: Bug Tracker, https://github.com/naya1503/pyAyra/issues
 Project-URL: Documentation, https://ultroid.tech
```

### Comparing `py-Ayra-8.7.4/py_Ayra.egg-info/SOURCES.txt` & `py-Ayra-8.7.5/py_Ayra.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `py-Ayra-8.7.4/setup.py` & `py-Ayra-8.7.5/setup.py`

 * *Files identical despite different names*

