# Comparing `tmp/botlogging-1.0.1.tar.gz` & `tmp/botlogging-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "botlogging-1.0.1.tar", last modified: Mon Aug 15 23:38:06 2022, max compression
+gzip compressed data, was "botlogging-2.0.0.tar", last modified: Sat May 13 01:40:15 2023, max compression
```

## Comparing `botlogging-1.0.1.tar` & `botlogging-2.0.0.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2022-08-15 23:38:06.111037 botlogging-1.0.1/
--rw-r--r--   0 babybear  (1000) babybear  (1000)     3597 2022-08-15 23:38:06.111037 botlogging-1.0.1/PKG-INFO
--rw-r--r--   0 babybear  (1000) babybear  (1000)     2388 2022-08-15 23:32:01.000000 botlogging-1.0.1/README.md
--rw-r--r--   0 babybear  (1000) babybear  (1000)      103 2022-03-11 13:26:14.000000 botlogging-1.0.1/pyproject.toml
--rw-r--r--   0 babybear  (1000) babybear  (1000)      628 2022-08-15 23:38:06.111037 botlogging-1.0.1/setup.cfg
--rw-r--r--   0 babybear  (1000) babybear  (1000)       38 2022-08-15 22:35:14.000000 botlogging-1.0.1/setup.py
-drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2022-08-15 23:38:06.111037 botlogging-1.0.1/src/
-drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2022-08-15 23:38:06.111037 botlogging-1.0.1/src/botlogging/
--rw-r--r--   0 babybear  (1000) babybear  (1000)       90 2022-08-15 23:38:00.000000 botlogging-1.0.1/src/botlogging/__init__.py
--rw-r--r--   0 babybear  (1000) babybear  (1000)     1421 2022-08-15 23:38:00.000000 botlogging-1.0.1/src/botlogging/delayed.py
--rw-r--r--   0 babybear  (1000) babybear  (1000)     1366 2022-08-15 23:38:00.000000 botlogging-1.0.1/src/botlogging/embed.py
--rw-r--r--   0 babybear  (1000) babybear  (1000)     6703 2022-08-15 23:38:00.000000 botlogging-1.0.1/src/botlogging/logger.py
-drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2022-08-15 23:38:06.111037 botlogging-1.0.1/src/botlogging.egg-info/
--rw-r--r--   0 babybear  (1000) babybear  (1000)     3597 2022-08-15 23:38:06.000000 botlogging-1.0.1/src/botlogging.egg-info/PKG-INFO
--rw-r--r--   0 babybear  (1000) babybear  (1000)      297 2022-08-15 23:38:06.000000 botlogging-1.0.1/src/botlogging.egg-info/SOURCES.txt
--rw-r--r--   0 babybear  (1000) babybear  (1000)        1 2022-08-15 23:38:06.000000 botlogging-1.0.1/src/botlogging.egg-info/dependency_links.txt
--rw-r--r--   0 babybear  (1000) babybear  (1000)       11 2022-08-15 23:38:06.000000 botlogging-1.0.1/src/botlogging.egg-info/top_level.txt
+drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2023-05-13 01:40:15.952622 botlogging-2.0.0/
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     2939 2023-05-13 01:40:15.952622 botlogging-2.0.0/PKG-INFO
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     2457 2023-05-13 01:37:34.000000 botlogging-2.0.0/README.md
+-rw-r--r--   0 babybear  (1000) babybear  (1000)      103 2023-03-10 01:45:17.000000 botlogging-2.0.0/pyproject.toml
+-rw-r--r--   0 babybear  (1000) babybear  (1000)      628 2023-05-13 01:40:15.952622 botlogging-2.0.0/setup.cfg
+-rw-r--r--   0 babybear  (1000) babybear  (1000)       38 2023-03-10 01:45:17.000000 botlogging-2.0.0/setup.py
+drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2023-05-13 01:40:15.942622 botlogging-2.0.0/src/
+drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2023-05-13 01:40:15.952622 botlogging-2.0.0/src/botlogging/
+-rw-r--r--   0 babybear  (1000) babybear  (1000)       90 2023-03-10 01:45:17.000000 botlogging-2.0.0/src/botlogging/__init__.py
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     1506 2023-05-13 01:37:34.000000 botlogging-2.0.0/src/botlogging/delayed.py
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     1366 2023-03-10 01:45:17.000000 botlogging-2.0.0/src/botlogging/embed.py
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     6703 2023-03-10 01:45:17.000000 botlogging-2.0.0/src/botlogging/logger.py
+drwxr-xr-x   0 babybear  (1000) babybear  (1000)        0 2023-05-13 01:40:15.952622 botlogging-2.0.0/src/botlogging.egg-info/
+-rw-r--r--   0 babybear  (1000) babybear  (1000)     2939 2023-05-13 01:40:15.000000 botlogging-2.0.0/src/botlogging.egg-info/PKG-INFO
+-rw-r--r--   0 babybear  (1000) babybear  (1000)      297 2023-05-13 01:40:15.000000 botlogging-2.0.0/src/botlogging.egg-info/SOURCES.txt
+-rw-r--r--   0 babybear  (1000) babybear  (1000)        1 2023-05-13 01:40:15.000000 botlogging-2.0.0/src/botlogging.egg-info/dependency_links.txt
+-rw-r--r--   0 babybear  (1000) babybear  (1000)       11 2023-05-13 01:40:15.000000 botlogging-2.0.0/src/botlogging.egg-info/top_level.txt
```

### Comparing `botlogging-1.0.1/README.md` & `botlogging-2.0.0/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -67,14 +67,20 @@
 ```py
 from discord.ext import commands
 import botlogging
 
 logger = botlogging.DelayedLogger(bot=bot, name="mybot")
 ```
 
+then within your event loop, run
+
+```py
+logger.register_queue()
+```
+
 ## Custom embeds
 
 You can override the embeds sent to Discord by passing in your own embeds.
 
 ```py
 # create a custom embed
 embed = discord.Embed(description="Custom embed!")
```

### Comparing `botlogging-1.0.1/setup.cfg` & `botlogging-2.0.0/setup.cfg`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = botlogging
-version = 1.0.1
+version = 2.0.0
 author = effprime
 author_email = effprime@github.com
 description = A logging package for Discord bots
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/effprime/BotLogging
 project_urls =
```

### Comparing `botlogging-1.0.1/src/botlogging/delayed.py` & `botlogging-2.0.0/src/botlogging/delayed.py`

 * *Files 12% similar despite different names*

```diff
@@ -14,30 +14,32 @@
         name (str): the name of the logging channel
         wait_time (float): the time to wait between log sends
         queue_size (int): the max number of queue events
     """
 
     def __init__(self, *args, **kwargs):
         self.wait_time = kwargs.pop("wait_time", 1)
-        self.__send_queue = asyncio.Queue(maxsize=kwargs.pop("queue_size", 1000))
+        self.queue_size = kwargs.pop("queue_size", 1000)
+        self.__send_queue = None
         super().__init__(*args, **kwargs)
 
-        self.bot.loop.create_task(self.__run())
-
     async def info(self, message, *args, **kwargs):
         await self.__send_queue.put(super().info(message, *args, **kwargs))
 
     async def debug(self, message, *args, **kwargs):
         await self.__send_queue.put(super().debug(message, *args, **kwargs))
 
     async def warning(self, message, *args, **kwargs):
         await self.__send_queue.put(super().warning(message, *args, **kwargs))
 
     async def error(self, message, *args, **kwargs):
         await self.__send_queue.put(super().error(message, *args, **kwargs))
 
-    async def __run(self):
+    def register_queue(self):
+        self.__send_queue = asyncio.Queue(loop=asyncio.get_event_loop(), maxsize=self.queue_size)
+
+    async def run(self):
         while True:
             coro = await self.__send_queue.get()
             if coro:
                 await coro
-            await asyncio.sleep(self.wait_time)
+            await asyncio.sleep(self.wait_time)
```

### Comparing `botlogging-1.0.1/src/botlogging/embed.py` & `botlogging-2.0.0/src/botlogging/embed.py`

 * *Files identical despite different names*

### Comparing `botlogging-1.0.1/src/botlogging/logger.py` & `botlogging-2.0.0/src/botlogging/logger.py`

 * *Files identical despite different names*

