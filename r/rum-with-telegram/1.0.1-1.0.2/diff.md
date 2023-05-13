# Comparing `tmp/rum_with_telegram-1.0.1.tar.gz` & `tmp/rum_with_telegram-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rum_with_telegram-1.0.1.tar", last modified: Fri May 12 03:21:25 2023, max compression
+gzip compressed data, was "rum_with_telegram-1.0.2.tar", last modified: Sat May 13 14:00:11 2023, max compression
```

## Comparing `rum_with_telegram-1.0.1.tar` & `rum_with_telegram-1.0.2.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 03:21:25.241110 rum_with_telegram-1.0.1/
--rw-rw-rw-   0        0        0     1087 2023-03-22 04:17:54.000000 rum_with_telegram-1.0.1/LICENSE
--rw-rw-rw-   0        0        0     1032 2023-05-12 03:21:25.240092 rum_with_telegram-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0       19 2023-03-22 04:17:54.000000 rum_with_telegram-1.0.1/README.md
--rw-rw-rw-   0        0        0      163 2023-04-25 07:27:09.000000 rum_with_telegram-1.0.1/pyproject.toml
-drwxrwxrwx   0        0        0        0 2023-05-12 03:21:25.229067 rum_with_telegram-1.0.1/rum_with_telegram/
--rw-rw-rw-   0        0        0      215 2023-05-12 03:06:02.000000 rum_with_telegram-1.0.1/rum_with_telegram/__init__.py
--rw-rw-rw-   0        0        0     1955 2023-05-04 04:53:43.000000 rum_with_telegram-1.0.1/rum_with_telegram/config.py
--rw-rw-rw-   0        0        0    26110 2023-05-12 03:21:02.000000 rum_with_telegram-1.0.1/rum_with_telegram/data_exchanger.py
--rw-rw-rw-   0        0        0     3872 2023-05-12 03:14:44.000000 rum_with_telegram-1.0.1/rum_with_telegram/db_handle.py
--rw-rw-rw-   0        0        0     1820 2023-05-12 03:02:22.000000 rum_with_telegram-1.0.1/rum_with_telegram/module.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:21:25.238097 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/
--rw-rw-rw-   0        0        0     1032 2023-05-12 03:21:25.000000 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      398 2023-05-12 03:21:25.000000 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 03:21:25.000000 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       78 2023-05-12 03:21:25.000000 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/requires.txt
--rw-rw-rw-   0        0        0       18 2023-05-12 03:21:25.000000 rum_with_telegram-1.0.1/rum_with_telegram.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 03:21:25.241110 rum_with_telegram-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1430 2023-05-12 03:06:02.000000 rum_with_telegram-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:00:11.130677 rum_with_telegram-1.0.2/
+-rw-rw-rw-   0        0        0     1087 2023-03-22 04:17:54.000000 rum_with_telegram-1.0.2/LICENSE
+-rw-rw-rw-   0        0        0     1032 2023-05-13 14:00:11.129679 rum_with_telegram-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0       19 2023-03-22 04:17:54.000000 rum_with_telegram-1.0.2/README.md
+-rw-rw-rw-   0        0        0      163 2023-04-25 07:27:09.000000 rum_with_telegram-1.0.2/pyproject.toml
+drwxrwxrwx   0        0        0        0 2023-05-13 14:00:11.116714 rum_with_telegram-1.0.2/rum_with_telegram/
+-rw-rw-rw-   0        0        0      215 2023-05-13 13:58:38.000000 rum_with_telegram-1.0.2/rum_with_telegram/__init__.py
+-rw-rw-rw-   0        0        0     2092 2023-05-13 13:53:34.000000 rum_with_telegram-1.0.2/rum_with_telegram/config.py
+-rw-rw-rw-   0        0        0    26650 2023-05-13 13:58:57.000000 rum_with_telegram-1.0.2/rum_with_telegram/data_exchanger.py
+-rw-rw-rw-   0        0        0     3872 2023-05-12 03:14:44.000000 rum_with_telegram-1.0.2/rum_with_telegram/db_handle.py
+-rw-rw-rw-   0        0        0     1820 2023-05-12 03:02:22.000000 rum_with_telegram-1.0.2/rum_with_telegram/module.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:00:11.127694 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/
+-rw-rw-rw-   0        0        0     1032 2023-05-13 14:00:11.000000 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      398 2023-05-13 14:00:11.000000 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:00:11.000000 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       78 2023-05-13 14:00:11.000000 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       18 2023-05-13 14:00:11.000000 rum_with_telegram-1.0.2/rum_with_telegram.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:00:11.130677 rum_with_telegram-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1430 2023-05-13 13:58:38.000000 rum_with_telegram-1.0.2/setup.py
```

### Comparing `rum_with_telegram-1.0.1/LICENSE` & `rum_with_telegram-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `rum_with_telegram-1.0.1/PKG-INFO` & `rum_with_telegram-1.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rum_with_telegram
-Version: 1.0.1
+Version: 1.0.2
 Summary: A bot, send telegram update to rum group as trx, and get new trx from rum group to channel.
 Home-page: https://github.com/liujuanjuan1984/rum_with_telegram
 Author: liujuanjuan1984
 Author-email: qiaoanlu@163.com
 Project-URL: Github Repo, https://github.com/liujuanjuan1984/rum_with_telegram
 Project-URL: Bug Tracker, https://github.com/liujuanjuan1984/rum_with_telegram/issues
 Project-URL: About Quorum, https://github.com/rumsystem/quorum
```

### Comparing `rum_with_telegram-1.0.1/rum_with_telegram/config.py` & `rum_with_telegram-1.0.2/rum_with_telegram/config.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,14 +12,16 @@
     # the title of feed
     FEED_TITLE: str
     RUM_SEED: str
     TG_BOT_TOKEN: str
     TG_BOT_NAME: str
     TG_CHANNEL_NAME: str
     TG_GROUP_NAME: str
+    POST_AUTH_TYPE: str = "blacklist"  # whitelist or blacklist
+    WHITELIST: list = None
     # list of telegram userid who is admin for this service
     ADMIN_USERIDS: list = None
     # blacklist of public keys of rum group, whos trxs cannot be packed to block
     BLACK_LIST_PUBKEYS: list = None
     # blacklist of telegram userids who cannot use this service
     BLACK_LIST_TGIDS: list = None
     # whether to print sql statements
@@ -39,14 +41,15 @@
     def __post_init__(self):
         if self.TG_CHANNEL_URL is None:
             name = self.TG_CHANNEL_NAME.replace("@", "")
             self.TG_CHANNEL_URL = f"https://t.me/{name}"
         self.ADMIN_USERIDS = self.ADMIN_USERIDS or []
         self.BLACK_LIST_PUBKEYS = self.BLACK_LIST_PUBKEYS or []
         self.BLACK_LIST_TGIDS = self.BLACK_LIST_TGIDS or []
+        self.WHITELIST = self.WHITELIST or []
 
 
 def read_json(json_file: str):
     with open(json_file, "r", encoding="utf-8") as f:
         data = json.load(f)
     return data
```

### Comparing `rum_with_telegram-1.0.1/rum_with_telegram/data_exchanger.py` & `rum_with_telegram-1.0.2/rum_with_telegram/data_exchanger.py`

 * *Files 1% similar despite different names*

```diff
@@ -136,14 +136,17 @@
                 await asyncio.sleep(5)
             self.start_trx = start_trx
 
     async def _handle_rum(self, start_trx):
         trxs = self.rum.api.get_content(num=20, start_trx=start_trx)
         for trx in trxs:
             start_trx = trx["TrxId"]
+            if self.config.POST_AUTH_TYPE == "whitelist":
+                if trx["SenderPubkey"] not in self.config.WHITELIST:
+                    continue
             if trx["SenderPubkey"] in self.config.BLACK_LIST_PUBKEYS:
                 continue
             if get_trx_type(trx) != "post":
                 continue
             _tag = self.config.RUM_TO_TG_TAG
             if _tag and _tag not in trx["Data"]["object"]["content"]:
                 continue
@@ -207,14 +210,20 @@
         """send message to rum group and telegram channel"""
         message_id = update.message.message_id
         logger.info("handle_private_chat %s", message_id)
         userid = update.message.from_user.id
         if userid in self.config.BLACK_LIST_TGIDS:
             await update.message.reply_text("You are in the blacklist.")
             return
+        if self.config.POST_AUTH_TYPE == "whitelist":
+            if userid not in self.config.WHITELIST:
+                await update.message.reply_text(
+                    f"You are not in the whitelist. Your content will not be post to channel.\n You can leave a comment to any post of the channel.@{self.config.TG_CHANNEL_NAME}"
+                )
+                return
         _first_name = update.message.from_user.first_name
         _last_name = update.message.from_user.last_name
         _fullname = f"{_first_name} {_last_name}" if _last_name else _first_name
         _text = update.message.text or update.message.caption or ""
         if _text.startswith("/profile"):
             await self.command_profile(update, context)
             return
```

### Comparing `rum_with_telegram-1.0.1/rum_with_telegram/db_handle.py` & `rum_with_telegram-1.0.2/rum_with_telegram/db_handle.py`

 * *Files identical despite different names*

### Comparing `rum_with_telegram-1.0.1/rum_with_telegram/module.py` & `rum_with_telegram-1.0.2/rum_with_telegram/module.py`

 * *Files identical despite different names*

### Comparing `rum_with_telegram-1.0.1/rum_with_telegram.egg-info/PKG-INFO` & `rum_with_telegram-1.0.2/rum_with_telegram.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rum-with-telegram
-Version: 1.0.1
+Version: 1.0.2
 Summary: A bot, send telegram update to rum group as trx, and get new trx from rum group to channel.
 Home-page: https://github.com/liujuanjuan1984/rum_with_telegram
 Author: liujuanjuan1984
 Author-email: qiaoanlu@163.com
 Project-URL: Github Repo, https://github.com/liujuanjuan1984/rum_with_telegram
 Project-URL: Bug Tracker, https://github.com/liujuanjuan1984/rum_with_telegram/issues
 Project-URL: About Quorum, https://github.com/rumsystem/quorum
```

### Comparing `rum_with_telegram-1.0.1/setup.py` & `rum_with_telegram-1.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="rum_with_telegram",
-    version="1.0.1",
+    version="1.0.2",
     author="liujuanjuan1984",
     author_email="qiaoanlu@163.com",
     description="A bot, send telegram update to rum group as trx, and get new trx from rum group to channel.",
     keywords=["python-telegram-bot", "rumsystem", "quorum"],
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/liujuanjuan1984/rum_with_telegram",
```

