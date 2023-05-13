# Comparing `tmp/hiyobot-0.1.5.tar.gz` & `tmp/hiyobot-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hiyobot-0.1.5.tar", last modified: Tue May  2 06:04:36 2023, max compression
+gzip compressed data, was "hiyobot-0.1.6.tar", last modified: Sat May 13 12:03:12 2023, max compression
```

## Comparing `hiyobot-0.1.5.tar` & `hiyobot-0.1.6.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 06:04:36.098813 hiyobot-0.1.5/
--rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-02 06:04:23.000000 hiyobot-0.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-02 06:04:36.098813 hiyobot-0.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2725 2023-05-02 06:04:23.000000 hiyobot-0.1.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 06:04:36.098813 hiyobot-0.1.5/hiyobot/
--rw-r--r--   0 runner    (1001) docker     (123)     7795 2023-05-02 06:04:23.000000 hiyobot-0.1.5/hiyobot/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 06:04:36.098813 hiyobot-0.1.5/hiyobot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-02 06:04:36.000000 hiyobot-0.1.5/hiyobot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      200 2023-05-02 06:04:36.000000 hiyobot-0.1.5/hiyobot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 06:04:36.000000 hiyobot-0.1.5/hiyobot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-02 06:04:36.000000 hiyobot-0.1.5/hiyobot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-02 06:04:36.000000 hiyobot-0.1.5/hiyobot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-02 06:04:36.098813 hiyobot-0.1.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-02 06:04:23.000000 hiyobot-0.1.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.873775 hiyobot-0.1.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 12:02:53.000000 hiyobot-0.1.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-13 12:03:12.873775 hiyobot-0.1.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2725 2023-05-13 12:02:53.000000 hiyobot-0.1.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.869775 hiyobot-0.1.6/hiyobot/
+-rw-r--r--   0 runner    (1001) docker     (123)     8662 2023-05-13 12:02:53.000000 hiyobot-0.1.6/hiyobot/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.873775 hiyobot-0.1.6/hiyobot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      200 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:03:12.873775 hiyobot-0.1.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:02:53.000000 hiyobot-0.1.6/setup.py
```

### Comparing `hiyobot-0.1.5/LICENSE` & `hiyobot-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `hiyobot-0.1.5/PKG-INFO` & `hiyobot-0.1.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.1.5
+Version: 0.1.6
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.1.5/README.md` & `hiyobot-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `hiyobot-0.1.5/hiyobot/__init__.py` & `hiyobot-0.1.6/hiyobot/__init__.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,25 +1,38 @@
 import websocket,ssl,json,threading,uuid,time,logging,re,traceback
 from functools import wraps
-HIYOBOT_VERSION=(0,1,4)
+HIYOBOT_VERSION=(0,1,6)
 MAX_RECV_LOG_LIMIT=100 #0 for no limit
 class Bot:
-    def __init__(self,channel,nick,password=None) -> None:
+    """
+    Simple Hack.chat bot class.
+    """
+    def __init__(self,channel,nick,password=None,joinoncreate=True) -> None:
+        """
+        Init the Bot.
+        """
         self.channel,self.nick,self.password=channel,nick,password
         self.events=[]
         self.checks=[]
         self.config={}
-        self.join()
+        if joinoncreate:
+            self.join()
     def join(self):
+        """
+        Send the request that joining into the channel.
+        """
         self.ws = websocket.create_connection("wss://hack.chat/chat-ws",sslopt={"cert_reqs":ssl.CERT_NONE})
         if self.password:
             self.ws.send(json.dumps({"cmd":"join","channel":self.channel,"nick":self.nick,"password":self.password}))
         else:
             self.ws.send(json.dumps({"cmd":"join","channel":self.channel,"nick":self.nick}))
     def on(self,matcher):
+        """
+        Add a new event.
+        """
         def decorate(func):
             @wraps(func)
             def wrapper(session, data,*args, **kwargs):
                 if matcher.match_all(data):
                     logging.debug(f"Matched! Function={func} Matcher={matcher}")
                     return func(session=session, data=data, *args, **kwargs)
                 else:
@@ -31,38 +44,50 @@
         while 1:
             self.ws.send('{"cmd":"ping"}')
             time.sleep(60)
     def _bindRaw(self,function):
         self.events.append(function)
         logging.debug(f"Restigered Event-Function {function} for bot {self}")
     def load_plugin(self,plugin_name):
+        """
+        Load a Hiyobot Plugin.
+        """
         #process the plugin name
         logging.debug("Ready for include module")
         plugin_name=plugin_name.replace("-","_")
         #import
         plugin=__import__(plugin_name)
         for command in plugin.exports:
             self._bindRaw(command)
         logging.debug(f"Included plugin {plugin_name}")
     def send(self,data):
+        """
+        Send JSON pack/text.
+        """
         if type(data) == str:
             #auto-detect&convert type
             data=Message.Text(data)
         self.ws.send(json.dumps(data))
         dumped=json.dumps(data)
         if MAX_RECV_LOG_LIMIT != 0:
             if len(dumped) >= MAX_RECV_LOG_LIMIT:
                 logging.debug(f"Sent: {dumped[:MAX_RECV_LOG_LIMIT]}...")
             else:
                 logging.debug(f"Sent: {dumped}")
         else:
             logging.debug(f"Sent: {dumped}")
     def _run(self,async_run=False):
         while True:
-            data = json.loads(self.ws.recv())
+            try:
+                data = json.loads(self.ws.recv())
+                
+            except:
+                logging.warning("Recv Data Failed, call re-join")
+                self.join()
+                continue
             def process(data):
                 dumped=json.dumps(data)
                 if MAX_RECV_LOG_LIMIT != 0:
                     if len(dumped) >= MAX_RECV_LOG_LIMIT:
                         logging.debug(f"Recv: {dumped[:MAX_RECV_LOG_LIMIT]}...")
                     else:
                         logging.debug(f"Recv: {dumped}")
@@ -85,72 +110,89 @@
                         logging.warn(f"Error when processing Event {event}")
                         traceback.print_exc()
             if async_run:
                 threading.Thread(target=process,args=(data,)).start()
             else:
                 process(data)
     def run(self,async_mission=True,in_new_thread=False,ping_thread=True):
+        """
+        Enter the bot mainloop.
+        """
         if in_new_thread:
             self.thread=threading.Thread(target=self._run,args=(async_mission,))
             self.thread.start()
         else:
             self._run(async_mission)
         if ping_thread:
             self.ping_thread=threading.Thread(target=self._pingThread)
             self.ping_thread.start()
 class Matcher:
+    """
+    A class, to check "should this event run"
+    """
     def __init__(self,rule):
         self.rules=[]
         
         if rule == list:
             self.rules=list
         else:
             self.rules.append(rule)
     def add_rule(self,rule):
+        """
+        Add a Checking function.
+        """
         self.rules.append(rule)
     def match(self,data):
+        """
+        Match. if one is successed, then True
+        """
         matched=False
         for rule in self.rules:
             matched_=rule(data)
             if matched_:
                 matched=True
     def match_all(self,data):
+        """
+        Match. only return true when all function returns true
+        """
         if type(data) == Data:
             data=data.__dict__
         for rule in self.rules:
             matched=rule(data)
             if matched == False:
                 return False
         return matched
 class Data:
+    """
+    Base Data Class
+    """
     def __init__(self,jsondata):
         self.__dict__=jsondata
 class Message:
+    """
+    Function-to-JSON class
+    """
     def Text(string):
         return {"cmd":"chat","text":string}
     def Image(URL):
         return {"cmd":"chat","text":f"![]({URL})"}
 class Matchers:
-    def message(data):
-        return data["cmd"] == "chat"
-    def join(data):
-        return data["cmd"] == "onlineAdd"
-    def startswith(text):
-        def _startswith(data):
-            return data.get("text","").startswith(text)
-        return _startswith
-    def regex(text):
-        def _regex(data):
-            return bool(re.match(text,data.get("text","")))
-        return _regex
-    def nick(text):
-        def _nick(data):
-            return data.get("nick") == text
-        return _nick
+    """
+    Preset Matchers.
+    """
+    message=lambda x:x["cmd"] == "chat"
+    join=lambda x:x["cmd"] == "onlineAdd"
+    startswith=lambda x:lambda y:y.get("text","").startswith(x)
+    regex=lambda x:lambda y:bool(re.match(x,y.get("text","")))
+    nick=lambda x:lambda y:y.get("nick")==x
+    nicknameTaken=lambda x:x["cmd"] == "warn" and x["text"] == "Nickname Taken"
 class Utils:
+    """
+    Some tools.
+    """
     def in_new_thread(func):
         return lambda:threading.Thread(target=func).start()
     def run_in_new_thread(func):
         return threading.Thread(target=func).start()
 class Session:
     def __init__(self,bot,data):
         logging.debug(f"Built session(bot={bot})")
```

### Comparing `hiyobot-0.1.5/hiyobot.egg-info/PKG-INFO` & `hiyobot-0.1.6/hiyobot.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.1.5
+Version: 0.1.6
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.1.5/setup.py` & `hiyobot-0.1.6/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='hiyobot', # 你的项目名称
-    version='0.1.5', # 你的项目版本
+    version="0.1.6", # 你的项目版本
     description='A simple bot framework for Hack.chat.', # 你的项目简介
     long_description=open('README.md').read(), # 你的项目详细介绍，一般从README.md文件中读取
     long_description_content_type='text/markdown', # 你的项目详细介绍的格式，一般为markdown格式
     url='https://github.com/Hiyoteam/hiyobot', # 你的项目主页，一般为github仓库地址
     author='MaggieLOL', # 你的姓名或者团队名称
     author_email='tanhanzesnd@gmail.com', # 你的邮箱或者团队邮箱
     license='GPL-2.0', # 你的项目使用的许可证，一般为MIT或者其他开源许可证
```

