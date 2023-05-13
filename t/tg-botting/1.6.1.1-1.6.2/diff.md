# Comparing `tmp/tg-botting-1.6.1.1.tar.gz` & `tmp/tg-botting-1.6.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tg-botting-1.6.1.1.tar", last modified: Mon May  8 14:10:05 2023, max compression
+gzip compressed data, was "tg-botting-1.6.2.tar", last modified: Sat May 13 18:00:36 2023, max compression
```

## Comparing `tg-botting-1.6.1.1.tar` & `tg-botting-1.6.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-08 14:10:05.152740 tg-botting-1.6.1.1/
--rw-rw-rw-   0        0        0      920 2023-05-08 14:10:05.151767 tg-botting-1.6.1.1/PKG-INFO
--rw-rw-rw-   0        0        0      930 2022-12-06 14:18:03.000000 tg-botting-1.6.1.1/README.md
--rw-rw-rw-   0        0        0       42 2023-05-08 14:10:05.152740 tg-botting-1.6.1.1/setup.cfg
--rw-rw-rw-   0        0        0     1447 2023-05-08 14:05:42.000000 tg-botting-1.6.1.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-08 14:10:05.146755 tg-botting-1.6.1.1/tg_botting/
--rw-rw-rw-   0        0        0    27942 2023-04-11 17:05:02.000000 tg-botting-1.6.1.1/tg_botting/bot.py
--rw-rw-rw-   0        0        0      976 2023-01-11 17:39:26.000000 tg-botting-1.6.1.1/tg_botting/cog.py
--rw-rw-rw-   0        0        0      995 2022-12-13 21:08:58.000000 tg-botting-1.6.1.1/tg_botting/generals.py
--rw-rw-rw-   0        0        0    15716 2023-05-08 14:05:42.000000 tg-botting-1.6.1.1/tg_botting/objects.py
--rw-rw-rw-   0        0        0       38 2022-12-13 21:06:01.000000 tg-botting-1.6.1.1/tg_botting/user_utils.py
-drwxrwxrwx   0        0        0        0 2023-05-08 14:10:05.150770 tg-botting-1.6.1.1/tg_botting.egg-info/
--rw-rw-rw-   0        0        0      920 2023-05-08 14:10:05.000000 tg-botting-1.6.1.1/tg_botting.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      293 2023-05-08 14:10:05.000000 tg-botting-1.6.1.1/tg_botting.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-08 14:10:05.000000 tg-botting-1.6.1.1/tg_botting.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       44 2023-05-08 14:10:05.000000 tg-botting-1.6.1.1/tg_botting.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-05-08 14:10:05.000000 tg-botting-1.6.1.1/tg_botting.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 18:00:36.349670 tg-botting-1.6.2/
+-rw-rw-rw-   0        0        0      918 2023-05-13 18:00:36.349670 tg-botting-1.6.2/PKG-INFO
+-rw-rw-rw-   0        0        0      930 2022-12-06 14:18:03.000000 tg-botting-1.6.2/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 18:00:36.349670 tg-botting-1.6.2/setup.cfg
+-rw-rw-rw-   0        0        0     1445 2023-05-13 17:57:27.000000 tg-botting-1.6.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:00:36.343578 tg-botting-1.6.2/tg_botting/
+-rw-rw-rw-   0        0        0    29856 2023-05-13 17:56:33.000000 tg-botting-1.6.2/tg_botting/bot.py
+-rw-rw-rw-   0        0        0      976 2023-01-11 17:39:26.000000 tg-botting-1.6.2/tg_botting/cog.py
+-rw-rw-rw-   0        0        0      995 2022-12-13 21:08:58.000000 tg-botting-1.6.2/tg_botting/generals.py
+-rw-rw-rw-   0        0        0    15742 2023-05-13 17:48:07.000000 tg-botting-1.6.2/tg_botting/objects.py
+-rw-rw-rw-   0        0        0       38 2022-12-13 21:06:01.000000 tg-botting-1.6.2/tg_botting/user_utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:00:36.348563 tg-botting-1.6.2/tg_botting.egg-info/
+-rw-rw-rw-   0        0        0      918 2023-05-13 18:00:36.000000 tg-botting-1.6.2/tg_botting.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      293 2023-05-13 18:00:36.000000 tg-botting-1.6.2/tg_botting.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 18:00:36.000000 tg-botting-1.6.2/tg_botting.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       44 2023-05-13 18:00:36.000000 tg-botting-1.6.2/tg_botting.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 18:00:36.000000 tg-botting-1.6.2/tg_botting.egg-info/top_level.txt
```

### Comparing `tg-botting-1.6.1.1/PKG-INFO` & `tg-botting-1.6.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tg-botting
-Version: 1.6.1.1
+Version: 1.6.2
 Summary: python library for easy creation of a telegram bot.
 Home-page: https://github.com/2sweetheart2/tg_botting/tree/master
 Author: Sweetie (Roma Fomkin)
 Author-email: <2004sweetheart2004@gmail.com>
 Keywords: python,bot,tg,tg bot,telegram,telegram bot,botting
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
```

### Comparing `tg-botting-1.6.1.1/README.md` & `tg-botting-1.6.2/README.md`

 * *Files identical despite different names*

### Comparing `tg-botting-1.6.1.1/setup.py` & `tg-botting-1.6.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from setuptools import setup
 
 here = os.path.abspath(os.path.dirname(__file__))
 
 with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
     long_description = "\n" + fh.read()
 
-VERSION = '1.6.1.1'
+VERSION = '1.6.2'
 DESCRIPTION = 'python library for easy creation of a telegram bot.'
 LONG_DESCRIPTION = 'A package that allows you to create bots for telegram using its entire API.'
 
 setup(
     name="tg-botting",
     version=VERSION,
     url='https://github.com/2sweetheart2/tg_botting/tree/master',
```

### Comparing `tg-botting-1.6.1.1/tg_botting/bot.py` & `tg-botting-1.6.2/tg_botting/bot.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 import asyncio
 import datetime
+import inspect
 import json
 import sys
 import time
 import traceback
+from inspect import signature
 
 import aiohttp
 import requests
 from pyrogram import Client
 
 from . import generals
 from .cog import Cog
 from .objects import Message, ChatActions, UserProfilePicture, CallbackQuery, Command, ChatPermission, \
-    PromotePermission, PreCheckOutQuery, Chat
+    PromotePermission, PreCheckOutQuery, Chat, User
 
 
 class CallbackError(Exception):
     def __init__(self, message=None, *args):
         if message is not None:
             self.message = message
             super().__init__(message, *args)
@@ -49,14 +51,15 @@
             self.pyrogram = Client('me', user_id, user_hash).start()
         else:
             self.pyrogram = None
         self.random_cog = None
         self.url = ''
         self.token = ''
         self.offset = None
+        self.type_error_message = 'Вы не правильно указали одно значение. Вместо \'{}\' нужна {}'
         self.bot = self
         self.prefix = prefixs
         self.__cogs = {}
         self.group_photos = []
         self.actions_from_cog = {}
         self.command_roles = {}
         self.ignore_listener_filter = []
@@ -456,26 +459,26 @@
             for _m in self.listeners_handle.get('on_message_new'):
                 if _m in self.ignore_listener_filter or message.chat.id in self.chat_filter:
                     if _m in self.actions_from_cog:
                         await _m(self.actions_from_cog.get(_m), message)
                     else:
                         await _m(message)
 
-    async def dispatch_command(self, message, command):
+    async def dispatch_command(self, message, command,args):
         if 'on_pre_command' in self.listeners_handle:
             for _m in self.listeners_handle.get('on_pre_command'):
                 if _m in self.actions_from_cog:
                     await _m(self.actions_from_cog.get(_m), command, message)
                 else:
                     await _m(command, message)
 
         if command in self.actions_from_cog:
-            await command.func(self.actions_from_cog.get(command), message)
+            await command.func(self.actions_from_cog.get(command), message,*args)
         else:
-            await command.func(message)
+            await command.func(message,*args)
 
     async def dispatch_uknow_command(self, message):
         if self.listeners_handle.get("on_unknow_command"):
             for _m in self.listeners_handle.get('on_unknow_command'):
                 if _m in self.ignore_listener_filter or message.chat.id in self.chat_filter:
                     if _m in self.actions_from_cog:
                         await _m(self.actions_from_cog.get(_m), message)
@@ -606,29 +609,74 @@
                 self.all_commands.update({cls.__class__.__name__: values})
             elif '__listener__' in dir(v):
                 self.add_listener(v.__listener__, v)
                 self.actions_from_cog.update({v: cls})
                 if v.__ignore_filter__:
                     self.ignore_listener_filter.append(v)
 
+    async def get_args(self,args):
+        data = []
+        for arg in args:
+            try:
+                data.append(int(arg))
+                continue
+            except:
+                pass
+            if arg[0] == '@':
+                data.append(await User.load(arg,self))
+                continue
+            data.append(arg)
+        return data
+
+    async def tupe_error(self,message, arg,need_type):
+        type = need_type
+        if need_type==int:
+            type = 'число'
+        elif need_type==str:
+            type = 'строка'
+        elif need_type==User:
+            type = 'пользователь'
+        await message.reply(self.type_error_message.format(arg,type))
+
+
     async def dispatch(self, message):
         if self.has_prefix(message):
-            ms = message.text.split(' ')
+            ms = message.text.split()
             ms.pop(0)
             rs, c, from_aliases = self.search(' '.join(ms))
             if rs:
                 for i in range(c):
                     ms.pop(0)
+                args = await self.get_args(ms)
+                need_args = signature(rs.func)
+                put_args = []
+                first = False
+                for i in range(0,len(need_args.parameters)):
+                    if list(need_args.parameters)[i]=='self':
+                        continue
+                    if not first:
+                        first = True
+                        continue
+                    val = list(need_args.parameters.values())[i]
+                    try:
+                        if val.annotation != inspect.Parameter.empty:
+                            if not isinstance(args[i-1],val.annotation):
+                                return await self.tupe_error(message,args[i-1],val.annotation)
+                    except IndexError as e:
+                        put_args.append(None)
+                        continue
+                    put_args.append(args[i-1])
+                    ms.pop(0)
                 message.text = ' '.join(ms)
                 setattr(message, 'texts', ms)
                 if len(self.chat_filter) > 0:
                     if message.chat.id not in self.chat_filter and rs not in self.ignore_filter:
                         return await self.dispatch_chat_filter_error(message)
                 try:
-                    await self.dispatch_command(message, rs)
+                    await self.dispatch_command(message, rs,put_args)
                 except CallbackError as e:
                     await message.reply(e.message)
                     return await self.dispatch_error_command_invoke(message, rs, e)
                 except Exception as e:
                     await self.dispatch_error_command_invoke(message, rs, e)
                     traceback.print_exc()
             else:
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `tg-botting-1.6.1.1/tg_botting/cog.py` & `tg-botting-1.6.2/tg_botting/cog.py`

 * *Files identical despite different names*

### Comparing `tg-botting-1.6.1.1/tg_botting/generals.py` & `tg-botting-1.6.2/tg_botting/generals.py`

 * *Files identical despite different names*

### Comparing `tg-botting-1.6.1.1/tg_botting/objects.py` & `tg-botting-1.6.2/tg_botting/objects.py`

 * *Files 1% similar despite different names*

```diff
@@ -270,14 +270,15 @@
             data['parse_mode'] = parse_mode
         if reply_markup:
             data['reply_markup'] = json.dumps(reply_markup.to_dict())
         if photo:
             data['caption'] = text
             data.pop('chat_id')
             return await self.send_photo(photo, **data)
+        text = str(text)
         if text is not None:
             if len(text) > 4096:
                 datas = []
                 for i in range(0,(len(text)//4094)+1):
                     data['text'] = text[i*4096:(i+1)*4094]
                     rs = await self.bot.tg_request('sendMessage', True, **data)
                     datas.append(rs)
```

### Comparing `tg-botting-1.6.1.1/tg_botting.egg-info/PKG-INFO` & `tg-botting-1.6.2/tg_botting.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tg-botting
-Version: 1.6.1.1
+Version: 1.6.2
 Summary: python library for easy creation of a telegram bot.
 Home-page: https://github.com/2sweetheart2/tg_botting/tree/master
 Author: Sweetie (Roma Fomkin)
 Author-email: <2004sweetheart2004@gmail.com>
 Keywords: python,bot,tg,tg bot,telegram,telegram bot,botting
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
```

