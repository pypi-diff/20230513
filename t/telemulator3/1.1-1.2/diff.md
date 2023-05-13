# Comparing `tmp/telemulator3-1.1.tar.gz` & `tmp/telemulator3-1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "telemulator3-1.1.tar", last modified: Sat Apr 29 09:58:59 2023, max compression
+gzip compressed data, was "telemulator3-1.2.tar", last modified: Sat May 13 07:15:43 2023, max compression
```

## Comparing `telemulator3-1.1.tar` & `telemulator3-1.2.tar`

### file list

```diff
@@ -1,52 +1,52 @@
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.395010 telemulator3-1.1/
--rw-rw-rw-   0        0        0     1094 2023-04-26 12:26:19.000000 telemulator3-1.1/LICENSE
--rw-rw-rw-   0        0        0       60 2023-04-28 10:27:40.000000 telemulator3-1.1/MANIFEST.in
--rw-rw-rw-   0        0        0     3536 2023-04-29 09:58:59.395511 telemulator3-1.1/PKG-INFO
--rw-rw-rw-   0        0        0     2948 2023-04-29 09:55:18.000000 telemulator3-1.1/README.md
--rw-rw-rw-   0        0        0      110 2023-04-26 12:26:19.000000 telemulator3-1.1/pyproject.toml
--rw-rw-rw-   0        0        0      715 2023-04-29 09:58:59.398013 telemulator3-1.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.278360 telemulator3-1.1/telemulator3/
--rw-rw-rw-   0        0        0     5140 2023-04-29 09:55:18.000000 telemulator3-1.1/telemulator3/__init__.py
--rw-rw-rw-   0        0        0     7140 2023-04-27 12:37:16.000000 telemulator3-1.1/telemulator3/api.py
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.316385 telemulator3-1.1/telemulator3/chat/
--rw-rw-rw-   0        0        0      403 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/__init__.py
--rw-rw-rw-   0        0        0     3117 2023-04-27 12:37:16.000000 telemulator3-1.1/telemulator3/chat/base.py
--rw-rw-rw-   0        0        0     2903 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/channel.py
--rw-rw-rw-   0        0        0     1890 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/group.py
--rw-rw-rw-   0        0        0     1330 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/history.py
--rw-rw-rw-   0        0        0     2551 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/keyboard.py
--rw-rw-rw-   0        0        0     3608 2023-04-27 12:37:16.000000 telemulator3-1.1/telemulator3/chat/member.py
--rw-rw-rw-   0        0        0     1268 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/chat/private.py
--rw-rw-rw-   0        0        0     1158 2023-04-27 12:37:16.000000 telemulator3-1.1/telemulator3/dictionaryable.py
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.380000 telemulator3-1.1/telemulator3/method/
--rw-rw-rw-   0        0        0     3755 2023-04-26 19:16:04.000000 telemulator3-1.1/telemulator3/method/__init__.py
--rw-rw-rw-   0        0        0      792 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/answerCallbackQuery.py
--rw-rw-rw-   0        0        0      395 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/deleteMessage.py
--rw-rw-rw-   0        0        0      638 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/editMessageCaption.py
--rw-rw-rw-   0        0        0      574 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/editMessageReplyMarkup.py
--rw-rw-rw-   0        0        0      742 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/editMessageText.py
--rw-rw-rw-   0        0        0      743 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/forwardMessage.py
--rw-rw-rw-   0        0        0      216 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getChat.py
--rw-rw-rw-   0        0        0      443 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getChatAdministrators.py
--rw-rw-rw-   0        0        0      574 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getChatMember.py
--rw-rw-rw-   0        0        0      249 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getChatMemberCount.py
--rw-rw-rw-   0        0        0      520 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getFile.py
--rw-rw-rw-   0        0        0      496 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/getMe.py
--rw-rw-rw-   0        0        0      292 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/leaveChat.py
--rw-rw-rw-   0        0        0      536 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/sendAudio.py
--rw-rw-rw-   0        0        0      431 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/sendChatAction.py
--rw-rw-rw-   0        0        0      566 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/sendDocument.py
--rw-rw-rw-   0        0        0      637 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/sendMessage.py
--rw-rw-rw-   0        0        0      575 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/sendPhoto.py
--rw-rw-rw-   0        0        0      346 2023-04-28 13:58:13.000000 telemulator3-1.1/telemulator3/method/setWebhook.py
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.392509 telemulator3-1.1/telemulator3/update/
--rw-rw-rw-   0        0        0       49 2023-04-26 12:26:19.000000 telemulator3-1.1/telemulator3/update/__init__.py
--rw-rw-rw-   0        0        0      699 2023-04-26 15:39:56.000000 telemulator3-1.1/telemulator3/update/callback_query.py
--rw-rw-rw-   0        0        0     4392 2023-04-27 10:54:49.000000 telemulator3-1.1/telemulator3/update/markup.py
--rw-rw-rw-   0        0        0     9346 2023-04-29 09:55:18.000000 telemulator3-1.1/telemulator3/update/message.py
--rw-rw-rw-   0        0        0     4353 2023-04-27 12:37:16.000000 telemulator3-1.1/telemulator3/user.py
-drwxrwxrwx   0        0        0        0 2023-04-29 09:58:59.293371 telemulator3-1.1/telemulator3.egg-info/
--rw-rw-rw-   0        0        0     3536 2023-04-29 09:58:59.000000 telemulator3-1.1/telemulator3.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1388 2023-04-29 09:58:59.000000 telemulator3-1.1/telemulator3.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-29 09:58:59.000000 telemulator3-1.1/telemulator3.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       13 2023-04-29 09:58:59.000000 telemulator3-1.1/telemulator3.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.356321 telemulator3-1.2/
+-rw-rw-rw-   0        0        0     1094 2023-04-26 12:26:19.000000 telemulator3-1.2/LICENSE
+-rw-rw-rw-   0        0        0       60 2023-04-28 10:27:40.000000 telemulator3-1.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     3528 2023-05-13 07:15:43.356321 telemulator3-1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     2940 2023-04-29 11:14:21.000000 telemulator3-1.2/README.md
+-rw-rw-rw-   0        0        0      110 2023-04-26 12:26:19.000000 telemulator3-1.2/pyproject.toml
+-rw-rw-rw-   0        0        0      715 2023-05-13 07:15:43.356321 telemulator3-1.2/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.246941 telemulator3-1.2/telemulator3/
+-rw-rw-rw-   0        0        0     5140 2023-04-29 09:55:18.000000 telemulator3-1.2/telemulator3/__init__.py
+-rw-rw-rw-   0        0        0     7140 2023-04-27 12:37:16.000000 telemulator3-1.2/telemulator3/api.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.278191 telemulator3-1.2/telemulator3/chat/
+-rw-rw-rw-   0        0        0      403 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/__init__.py
+-rw-rw-rw-   0        0        0     3117 2023-04-27 12:37:16.000000 telemulator3-1.2/telemulator3/chat/base.py
+-rw-rw-rw-   0        0        0     2903 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/channel.py
+-rw-rw-rw-   0        0        0     1890 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/group.py
+-rw-rw-rw-   0        0        0     1330 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/history.py
+-rw-rw-rw-   0        0        0     2551 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/keyboard.py
+-rw-rw-rw-   0        0        0     3608 2023-04-27 12:37:16.000000 telemulator3-1.2/telemulator3/chat/member.py
+-rw-rw-rw-   0        0        0     1268 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/chat/private.py
+-rw-rw-rw-   0        0        0     1158 2023-04-27 12:37:16.000000 telemulator3-1.2/telemulator3/dictionaryable.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.340695 telemulator3-1.2/telemulator3/method/
+-rw-rw-rw-   0        0        0     3755 2023-04-26 19:16:04.000000 telemulator3-1.2/telemulator3/method/__init__.py
+-rw-rw-rw-   0        0        0      792 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/answerCallbackQuery.py
+-rw-rw-rw-   0        0        0      395 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/deleteMessage.py
+-rw-rw-rw-   0        0        0      638 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/editMessageCaption.py
+-rw-rw-rw-   0        0        0      574 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/editMessageReplyMarkup.py
+-rw-rw-rw-   0        0        0      742 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/editMessageText.py
+-rw-rw-rw-   0        0        0      743 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/forwardMessage.py
+-rw-rw-rw-   0        0        0      216 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getChat.py
+-rw-rw-rw-   0        0        0      443 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getChatAdministrators.py
+-rw-rw-rw-   0        0        0      574 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getChatMember.py
+-rw-rw-rw-   0        0        0      249 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getChatMemberCount.py
+-rw-rw-rw-   0        0        0      520 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getFile.py
+-rw-rw-rw-   0        0        0      496 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/getMe.py
+-rw-rw-rw-   0        0        0      292 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/leaveChat.py
+-rw-rw-rw-   0        0        0      536 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/sendAudio.py
+-rw-rw-rw-   0        0        0      431 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/sendChatAction.py
+-rw-rw-rw-   0        0        0      566 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/sendDocument.py
+-rw-rw-rw-   0        0        0      637 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/sendMessage.py
+-rw-rw-rw-   0        0        0      575 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/sendPhoto.py
+-rw-rw-rw-   0        0        0      346 2023-04-28 13:58:13.000000 telemulator3-1.2/telemulator3/method/setWebhook.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.340695 telemulator3-1.2/telemulator3/update/
+-rw-rw-rw-   0        0        0       49 2023-04-26 12:26:19.000000 telemulator3-1.2/telemulator3/update/__init__.py
+-rw-rw-rw-   0        0        0      711 2023-05-13 07:10:16.000000 telemulator3-1.2/telemulator3/update/callback_query.py
+-rw-rw-rw-   0        0        0     4392 2023-04-27 10:54:49.000000 telemulator3-1.2/telemulator3/update/markup.py
+-rw-rw-rw-   0        0        0     9346 2023-04-29 09:55:18.000000 telemulator3-1.2/telemulator3/update/message.py
+-rw-rw-rw-   0        0        0     4353 2023-04-27 12:37:16.000000 telemulator3-1.2/telemulator3/user.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:15:43.262568 telemulator3-1.2/telemulator3.egg-info/
+-rw-rw-rw-   0        0        0     3528 2023-05-13 07:15:42.000000 telemulator3-1.2/telemulator3.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1388 2023-05-13 07:15:43.000000 telemulator3-1.2/telemulator3.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 07:15:42.000000 telemulator3-1.2/telemulator3.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       13 2023-05-13 07:15:42.000000 telemulator3-1.2/telemulator3.egg-info/top_level.txt
```

### Comparing `telemulator3-1.1/LICENSE` & `telemulator3-1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/PKG-INFO` & `telemulator3-1.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: telemulator3
-Version: 1.1
+Version: 1.2
 Summary: Mocked Telegram Bot API elements for unit tests of a bot based on the pyTelegramBotAPI library.
 Home-page: https://github.com/vb64/telemulator3
 Author: Vitaly Bogomolov
 Author-email: mail@vitaly-bogomolov.ru
 Project-URL: Bug Tracker, https://github.com/vb64/telemulator3/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -91,12 +91,12 @@
 assert group.history.contain('My Bot (ID 1) left chat')
 # group.history.dump()
 ```
 
 ## Development
 
 ```
-$ git clone git@github.com:vb64/telemulator3
-$ cd telemulator3
-$ make setup PYTHON_BIN=/path/to/python3
-$ make tests
+git clone git@github.com:vb64/telemulator3
+cd telemulator3
+make setup PYTHON_BIN=/path/to/python3
+make tests
 ```
```

### Comparing `telemulator3-1.1/README.md` & `telemulator3-1.2/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -76,12 +76,12 @@
 assert group.history.contain('My Bot (ID 1) left chat')
 # group.history.dump()
 ```
 
 ## Development
 
 ```
-$ git clone git@github.com:vb64/telemulator3
-$ cd telemulator3
-$ make setup PYTHON_BIN=/path/to/python3
-$ make tests
+git clone git@github.com:vb64/telemulator3
+cd telemulator3
+make setup PYTHON_BIN=/path/to/python3
+make tests
 ```
```

### Comparing `telemulator3-1.1/setup.cfg` & `telemulator3-1.2/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2074 656c 656d 756c 6174 6f72 330d   = telemulator3.
-00000020: 0a76 6572 7369 6f6e 203d 2031 2e31 0d0a  .version = 1.1..
+00000020: 0a76 6572 7369 6f6e 203d 2031 2e32 0d0a  .version = 1.2..
 00000030: 6175 7468 6f72 203d 2056 6974 616c 7920  author = Vitaly 
 00000040: 426f 676f 6d6f 6c6f 760d 0a61 7574 686f  Bogomolov..autho
 00000050: 725f 656d 6169 6c20 3d20 6d61 696c 4076  r_email = mail@v
 00000060: 6974 616c 792d 626f 676f 6d6f 6c6f 762e  italy-bogomolov.
 00000070: 7275 0d0a 6465 7363 7269 7074 696f 6e20  ru..description 
 00000080: 3d20 4d6f 636b 6564 2054 656c 6567 7261  = Mocked Telegra
 00000090: 6d20 426f 7420 4150 4920 656c 656d 656e  m Bot API elemen
```

### Comparing `telemulator3-1.1/telemulator3/__init__.py` & `telemulator3-1.2/telemulator3/__init__.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/api.py` & `telemulator3-1.2/telemulator3/api.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/base.py` & `telemulator3-1.2/telemulator3/chat/base.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/channel.py` & `telemulator3-1.2/telemulator3/chat/channel.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/group.py` & `telemulator3-1.2/telemulator3/chat/group.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/history.py` & `telemulator3-1.2/telemulator3/chat/history.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/keyboard.py` & `telemulator3-1.2/telemulator3/chat/keyboard.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/member.py` & `telemulator3-1.2/telemulator3/chat/member.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/chat/private.py` & `telemulator3-1.2/telemulator3/chat/private.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/dictionaryable.py` & `telemulator3-1.2/telemulator3/dictionaryable.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/__init__.py` & `telemulator3-1.2/telemulator3/method/__init__.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/answerCallbackQuery.py` & `telemulator3-1.2/telemulator3/method/answerCallbackQuery.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/editMessageCaption.py` & `telemulator3-1.2/telemulator3/method/editMessageCaption.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/editMessageReplyMarkup.py` & `telemulator3-1.2/telemulator3/method/editMessageReplyMarkup.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/editMessageText.py` & `telemulator3-1.2/telemulator3/method/editMessageText.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/forwardMessage.py` & `telemulator3-1.2/telemulator3/method/forwardMessage.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/getChatMember.py` & `telemulator3-1.2/telemulator3/method/getChatMember.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/getFile.py` & `telemulator3-1.2/telemulator3/method/getFile.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/sendAudio.py` & `telemulator3-1.2/telemulator3/method/sendAudio.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/sendDocument.py` & `telemulator3-1.2/telemulator3/method/sendDocument.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/sendMessage.py` & `telemulator3-1.2/telemulator3/method/sendMessage.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/method/sendPhoto.py` & `telemulator3-1.2/telemulator3/method/sendPhoto.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/update/callback_query.py` & `telemulator3-1.2/telemulator3/update/callback_query.py`

 * *Files 14% similar despite different names*

```diff
@@ -5,13 +5,13 @@
 class CallbackQuery(CallbackQueryBase):
     """Construct and return CallbackQuery."""
 
     def __init__(self, from_user, callback_data, chat_instance, message):
         """Create callback from user."""
         api = from_user.api
         callback_id = api.new_id(api.EntityCallback)
-        CallbackQueryBase.__init__(self, callback_id, from_user, callback_data, chat_instance, message)
+        CallbackQueryBase.__init__(self, callback_id, from_user, callback_data, chat_instance, '', message=message)
         from_user.api.callback_queries[callback_id] = self
 
     def __str__(self):
         """As text."""
         return '{} >> tap inline button with callback_data: {}'.format(self.from_user, self.data)
```

### Comparing `telemulator3-1.1/telemulator3/update/markup.py` & `telemulator3-1.2/telemulator3/update/markup.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/update/message.py` & `telemulator3-1.2/telemulator3/update/message.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3/user.py` & `telemulator3-1.2/telemulator3/user.py`

 * *Files identical despite different names*

### Comparing `telemulator3-1.1/telemulator3.egg-info/PKG-INFO` & `telemulator3-1.2/telemulator3.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: telemulator3
-Version: 1.1
+Version: 1.2
 Summary: Mocked Telegram Bot API elements for unit tests of a bot based on the pyTelegramBotAPI library.
 Home-page: https://github.com/vb64/telemulator3
 Author: Vitaly Bogomolov
 Author-email: mail@vitaly-bogomolov.ru
 Project-URL: Bug Tracker, https://github.com/vb64/telemulator3/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -91,12 +91,12 @@
 assert group.history.contain('My Bot (ID 1) left chat')
 # group.history.dump()
 ```
 
 ## Development
 
 ```
-$ git clone git@github.com:vb64/telemulator3
-$ cd telemulator3
-$ make setup PYTHON_BIN=/path/to/python3
-$ make tests
+git clone git@github.com:vb64/telemulator3
+cd telemulator3
+make setup PYTHON_BIN=/path/to/python3
+make tests
 ```
```

### Comparing `telemulator3-1.1/telemulator3.egg-info/SOURCES.txt` & `telemulator3-1.2/telemulator3.egg-info/SOURCES.txt`

 * *Files identical despite different names*

