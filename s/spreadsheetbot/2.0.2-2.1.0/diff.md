# Comparing `tmp/spreadsheetbot-2.0.2.tar.gz` & `tmp/spreadsheetbot-2.1.0.tar.gz`

## Comparing `spreadsheetbot-2.0.2.tar` & `spreadsheetbot-2.1.0.tar`

### file list

```diff
@@ -1,24 +1,24 @@
--rw-r--r--   0        0        0       94 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/Makefile
--rw-r--r--   0        0        0     7097 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/__init__.py
--rw-r--r--   0        0        0       91 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/basic/__init__.py
--rw-r--r--   0        0        0     1292 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/basic/drive.py
--rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/basic/errors.py
--rw-r--r--   0        0        0     3015 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/basic/handlers.py
--rw-r--r--   0        0        0     1042 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/basic/log.py
--rw-r--r--   0        0        0     1776 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/__init__.py
--rw-r--r--   0        0        0     8952 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/abstract.py
--rw-r--r--   0        0        0     3333 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/groups.py
--rw-r--r--   0        0        0      714 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/i18n.py
--rw-r--r--   0        0        0     1421 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/keyboard.py
--rw-r--r--   0        0        0     1182 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/log.py
--rw-r--r--   0        0        0     3980 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/notifications.py
--rw-r--r--   0        0        0     2474 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/registration.py
--rw-r--r--   0        0        0     1184 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/report.py
--rw-r--r--   0        0        0     1130 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/settings.py
--rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/switch.py
--rw-r--r--   0        0        0    20774 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/users.py
--rw-r--r--   0        0        0     2038 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/.gitignore
--rw-r--r--   0        0        0     1107 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/LICENSE.txt
--rw-r--r--   0        0        0     7061 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/README.md
--rw-r--r--   0        0        0      742 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/pyproject.toml
--rw-r--r--   0        0        0     7789 2020-02-02 00:00:00.000000 spreadsheetbot-2.0.2/PKG-INFO
+-rw-r--r--   0        0        0      128 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/Makefile
+-rw-r--r--   0        0        0     6933 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/__init__.py
+-rw-r--r--   0        0        0       91 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/basic/__init__.py
+-rw-r--r--   0        0        0     1292 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/basic/drive.py
+-rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/basic/errors.py
+-rw-r--r--   0        0        0     3061 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/basic/handlers.py
+-rw-r--r--   0        0        0     1042 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/basic/log.py
+-rw-r--r--   0        0        0     1923 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/__init__.py
+-rw-r--r--   0        0        0     9520 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/abstract.py
+-rw-r--r--   0        0        0     3329 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/groups.py
+-rw-r--r--   0        0        0      714 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/i18n.py
+-rw-r--r--   0        0        0     1421 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/keyboard.py
+-rw-r--r--   0        0        0     1182 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/log.py
+-rw-r--r--   0        0        0     3980 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/notifications.py
+-rw-r--r--   0        0        0     2474 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/registration.py
+-rw-r--r--   0        0        0     1184 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/report.py
+-rw-r--r--   0        0        0     1130 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/settings.py
+-rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/switch.py
+-rw-r--r--   0        0        0    20960 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/users.py
+-rw-r--r--   0        0        0     2038 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/.gitignore
+-rw-r--r--   0        0        0     1107 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/LICENSE.txt
+-rw-r--r--   0        0        0     7061 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/README.md
+-rw-r--r--   0        0        0      742 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/pyproject.toml
+-rw-r--r--   0        0        0     7789 2020-02-02 00:00:00.000000 spreadsheetbot-2.1.0/PKG-INFO
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/__init__.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-import sys
-
 from telegram import Bot
 from telegram.ext import (
     Application,
     ApplicationBuilder,
     ChatMemberHandler,
     CommandHandler,
     MessageHandler,
@@ -17,15 +15,15 @@
     Settings,
     Groups,
     Users,
     Registration,
     Report,
     Keyboard,
     Notifications,
-    PerfomNotification
+    PerfomNotifications
 )
 
 from spreadsheetbot.basic import Log, INFO, DEBUG
 from spreadsheetbot.basic.handlers import ErrorHandlerFun, ChatMemberHandlerFun
 
 UPDATE_GROUP_USER_REQUEST  = 0
 UPDATE_GROUP_GROUP_REQUEST = 2
@@ -59,24 +57,23 @@
         await Notifications.async_init(self.sheets_secret, self.sheets_link)
 
         bot: Bot = app.bot
         await bot.set_my_commands([(HELP_COMMAND, Settings.help_command_description)])
 
         await LogSheet.write(None, "Started an application")
 
-        app.create_task(Switch.update(app))
-        app.create_task(Settings.update(app))
-        app.create_task(Groups.update(app))
-        app.create_task(Users.update(app))
-        app.create_task(Registration.update(app))
-        app.create_task(Report.update(app))
-        app.create_task(Keyboard.update(app))
-        app.create_task(Notifications.update(app))
-
-        app.create_task(PerfomNotification(app))
+        Switch.update(app)
+        Settings.update(app)
+        Groups.update(app)
+        Users.update(app)
+        Registration.update(app)
+        Report.update(app)
+        Keyboard.update(app)
+        Notifications.update(app)
+        PerfomNotifications(app)
 
     async def post_shutdown(self, app: Application) -> None:
         await LogSheet.write(None, "Stopped an application")
 
     def run_polling(self):
         Log.info("Starting...")
         app = ApplicationBuilder() \
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/basic/drive.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/basic/drive.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/basic/handlers.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/basic/handlers.py`

 * *Files 12% similar despite different names*

```diff
@@ -9,35 +9,34 @@
 from spreadsheetbot.sheets.log import LogSheet
 from spreadsheetbot.sheets.groups import Groups
 from spreadsheetbot.sheets.users import Users
 
 from spreadsheetbot.basic.log import Log
 from spreadsheetbot.basic.errors import BotShouldBeInactive
 
-async def ErrorHandlerFun(update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
+async def ErrorHandlerFun(update: Update|dict, context: ContextTypes.DEFAULT_TYPE) -> None:
     if type(context.error) == BotShouldBeInactive:
         Log.error(msg="Exception Bot should be inactive", exc_info=context.error)
         exit(1)
 
     Log.error(msg="Exception while handling an update:", exc_info=context.error)
 
     tb_list = traceback.format_exception(None, context.error, context.error.__traceback__)
     tb_string = "".join(tb_list)
 
-    update_str = update.to_dict() if isinstance(update, Update) else str(update)
+    update_str = update.to_dict() if isinstance(update, Update) else update if isinstance(update, dict) else str(update)
     message = (
         f"An exception was raised while handling an update\n"
         f"<pre>update = {html.escape(json.dumps(update_str, indent=2, ensure_ascii=False))}"
         "</pre>\n\n"
         f"<pre>context.chat_data = {html.escape(str(context.chat_data))}</pre>\n\n"
         f"<pre>context.user_data = {html.escape(str(context.user_data))}</pre>\n\n"
         f"<pre>{html.escape(tb_string)}</pre>"
     )
-
-    await Groups.send_to_all_superadmin_groups(context.bot, message, ParseMode.HTML)
+    Groups.send_to_all_superadmin_groups(context.application, message, ParseMode.HTML)
 
 async def ChatMemberHandlerFun(update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
     Log.debug(f"Chat member event \n{update.my_chat_member}\n")
     if update.effective_chat.type in [Chat.GROUP, Chat.SUPERGROUP, Chat.CHANNEL]:
         Log.info((
             f"{update.my_chat_member.new_chat_member['status'].title()} event in "
             f"{update.effective_chat.type} with title {update.effective_chat.title} id {update.effective_chat.id}"
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/basic/log.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/basic/log.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/__init__.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -11,28 +11,36 @@
 
 import asyncio
 from telegram.ext import Application
 from telegram.constants import ParseMode
 
 from spreadsheetbot.basic.log import Log
 
-async def PerfomNotification(app: Application):
+def PerfomNotifications(app: Application):
+    app.create_task(
+        _perform_notification(app),
+        {
+            'action': 'Perform notification'
+        }
+    )
+
+async def _perform_notification(app: Application):
     Log.info("Start performing notification")
     for idx,row in Notifications.as_df.loc[Notifications.selector_to_notify()].iterrows():
         await Users.send_notification_to_all_users(
-            app.bot, row.text_markdown, ParseMode.MARKDOWN, row.send_picture, row.state, row.condition
+            app, row.text_markdown, ParseMode.MARKDOWN, row.send_picture, row.state, row.condition
         )
         if row.state == "":
-            await Groups.send_to_all_normal_groups(app.bot, row.text_markdown, ParseMode.MARKDOWN, row.send_picture)
+            await Groups.send_to_all_normal_groups(app, row.text_markdown, ParseMode.MARKDOWN, row.send_picture)
         admin_group_text = \
             Settings.notification_admin_groups_template.format(message=row.text_markdown) if row.condition == None \
             else Settings.notification_admin_groups_condition_template.format(message=row.text_markdown, condition=row.condition)
         await Groups.send_to_all_admin_groups(
-            app.bot, 
+            app, 
             admin_group_text,
             ParseMode.MARKDOWN,
             row.send_picture
         )
         await Notifications.set_done(idx)
     Log.info("Done performing notification")
     await asyncio.sleep(Settings.notifications_update_time)
-    app.create_task(PerfomNotification(app))
+    PerfomNotifications(app)
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/abstract.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/abstract.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 from telegram.ext import Application
 import asyncio
 import gspread_asyncio
 from gspread import utils
 import pandas as pd
 
 from telegram import (
-    Bot,
     InlineKeyboardMarkup,
     Document
 )
 from telegram.ext.filters import MessageFilter
 
 from google.oauth2.service_account import Credentials 
 
@@ -75,24 +74,33 @@
         pass
     
     async def _post_async_init(self):
         await self._process_df_update()
 
     async def _get_df(self) -> pd.DataFrame:
         pass
+
+    def _create_update_context(self, action, **kwargs) -> dict:
+        return {
+            'action': action,
+            'name': self.name,
+        } | kwargs
+    
+    def update(self, app: Application) -> None:
+        app.create_task(self._update(app), self._create_update_context('Whole df update'))
     
-    async def update(self, app: Application) -> None:
+    async def _update(self, app: Application) -> None:
         await self._pre_update()
         await asyncio.sleep(self.update_sleep_time)
         
         Log.info(f"Prepared to update whole df {self.name}")
         while len(self.mutex) > 0:
             Log.info(f"Halted whole df update at {self.name} with mutex {self.mutex}")
             await asyncio.sleep(self.retry_sleep_time)
-        app.create_task(self.update(app))
+        self.update(app)
         self.whole_mutex = True
         
         await self._connect()
         self.as_df = await self._get_df()
         self.whole_mutex = False
 
         Log.info(f"Updated whole df {self.name}")
@@ -177,39 +185,49 @@
         wks_update = self._prepare_batch_update([
             (wks_row, self.wks_col(key), value)
             for key, value in record_params.items()
         ])
         
         await self.wks.batch_update(wks_update)
         if get_file != None and save_to != None and save_as != None and app != None:
-            app.create_task(SaveToDrive(self.agc.gc.auth.token, save_to, save_as, get_file))
+            app.create_task(
+                SaveToDrive(self.agc.gc.auth.token, save_to, save_as, get_file),
+                self._create_update_context('Save to drive', save_to=save_to, save_as=save_as)
+            )
         
         del self.mutex[self.mutex.index(uid)]
         Log.info(f"Done batch update {record_action} record in {self.name} with {self.uid_col} {uid} and {collumns} collumns")
         Log.debug(f"Current mutext at {self.name} is {self.mutex}")
     
     def _get(self, selector, iloc = 0) -> pd.Series:
         row = self.as_df.loc[selector]
         if row.empty:
             return None
         return row.iloc[iloc]
 
-    async def _send_to_all_uids(self, selector, bot: Bot, message: str, parse_mode: str, 
+    def _send_to_all_uids(self, selector, app: Application, message: str, parse_mode: str, 
         send_photo: str = None, reply_markup: InlineKeyboardMarkup = None
     ):
-        if send_photo == None or send_photo == '':
+        update = self._create_update_context(
+            'Send to all uids',
+            message=message,
+            parse_mode=parse_mode,
+            send_photo=send_photo,
+            reply_markup=reply_markup.to_dict() if reply_markup else reply_markup
+        )
+        if send_photo not in [None, '']:
             for uid in self.as_df.loc[selector][self.uid_col].to_list():
-                try:
-                    await bot.send_message(chat_id=uid, text=message, parse_mode=parse_mode, reply_markup=reply_markup)
-                except Exception:
-                    Log.info(f"Error while sending message to id {uid}")
+                app.create_task(
+                    app.bot.send_photo(chat_id=uid, photo=send_photo, caption=message, parse_mode=parse_mode, reply_markup=reply_markup),
+                    update
+                )
             return
         for uid in self.as_df.loc[selector][self.uid_col].to_list():
-            try:
-                await bot.send_photo(chat_id=uid, photo=send_photo, caption=message, parse_mode=parse_mode, reply_markup=reply_markup)
-            except Exception:
-                Log.info(f"Error while sending photo to id {uid}")
+            app.create_task(
+                app.bot.send_message(chat_id=uid, text=message, parse_mode=parse_mode, reply_markup=reply_markup),
+                update
+            )
     
     class AbstractFilter(MessageFilter):
         def __init__(self, name: str = None, data_filter: bool = False, outer_obj = None):
             super().__init__(name, data_filter)
             self.outer_obj = outer_obj
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/groups.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/groups.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import pandas as pd
 from spreadsheetbot.sheets.abstract import AbstractSheetAdapter
 
-from telegram import Message, Update, Chat, Bot
-from telegram.ext import ContextTypes
+from telegram import Message, Update, Chat
+from telegram.ext import Application, ContextTypes
 
 from spreadsheetbot.sheets.i18n import I18n
 from spreadsheetbot.sheets.settings import Settings
 from spreadsheetbot.sheets.report import Report
 
 class GroupsAdapterClass(AbstractSheetAdapter):
     def __init__(self) -> None:
@@ -29,30 +29,30 @@
             (df.chat_id != "") &
             (df.is_admin.isin(I18n.yes_no_super)) &
             (df.is_active == I18n.yes)
         ]
         df.chat_id = df.chat_id.apply(str)
         return df
     
-    async def send_to_all_normal_groups(self, bot: Bot, message: str, parse_mode: str, send_photo: str = None):
-        await self._send_to_all_uids(
+    def send_to_all_normal_groups(self, app: Application, message: str, parse_mode: str, send_photo: str = None):
+        self._send_to_all_uids(
             self.as_df.is_admin == I18n.no,
-            bot, message, parse_mode, send_photo
+            app, message, parse_mode, send_photo
         )
     
-    async def send_to_all_admin_groups(self, bot: Bot, message: str, parse_mode: str, send_photo: str = None):
-        await self._send_to_all_uids(
+    def send_to_all_admin_groups(self, app: Application, message: str, parse_mode: str, send_photo: str = None):
+        self._send_to_all_uids(
             self.as_df.is_admin.isin(I18n.yes_super),
-            bot, message, parse_mode, send_photo
+            app, message, parse_mode, send_photo
         )
     
-    async def send_to_all_superadmin_groups(self, bot: Bot, message: str, parse_mode: str, send_photo: str = None):
-        await self._send_to_all_uids(
+    def send_to_all_superadmin_groups(self, app: Application, message: str, parse_mode: str, send_photo: str = None):
+        self._send_to_all_uids(
             self.as_df.is_admin == I18n.super,
-            bot, message, parse_mode, send_photo
+            app, message, parse_mode, send_photo
         )
     
     class GroupChatClass(AbstractSheetAdapter.AbstractFilter):
         def filter(self, message: Message) -> bool:
             return message.chat.type in [Chat.GROUP, Chat.SUPERGROUP, Chat.CHANNEL]
     
     class IsRegisteredClass(AbstractSheetAdapter.AbstractFilter):
```

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/i18n.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/i18n.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/keyboard.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/keyboard.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/log.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/log.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/notifications.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/notifications.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/registration.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/registration.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/report.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/report.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/settings.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/settings.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/switch.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/switch.py`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/src/spreadsheetbot/sheets/users.py` & `spreadsheetbot-2.1.0/src/spreadsheetbot/sheets/users.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 import pandas as pd
 from spreadsheetbot.sheets.abstract import AbstractSheetAdapter
 
 from telegram import (
-    Bot,
     Message,
     Update,
     Chat,
     ReplyKeyboardRemove,
     InlineKeyboardMarkup,
     InlineKeyboardButton,
     TelegramObject
 )
 from telegram.constants import ParseMode
-from telegram.ext import ContextTypes
+from telegram.ext import Application, ContextTypes
 from telegram.ext.filters import (
     UpdateType
 )
 
 from spreadsheetbot.sheets.i18n import I18n
 from spreadsheetbot.sheets.switch import Switch
 from spreadsheetbot.sheets.settings import Settings
@@ -73,22 +72,23 @@
 
         self.get   = lambda uid: self._get(self.selector(uid))
         self.state = lambda uid: self.get(uid).state
         self.active_user_count  = lambda: self.as_df.loc[self.as_df.is_active == I18n.yes].shape[0]
         self.should_send_report = lambda count: count % Report.send_every_x_active_users == 0
 
         self.is_active = lambda user: user.is_active == I18n.yes
+        self.get_state_string = lambda user, state: user[state] if user[state] != '' else I18n.data_empty if not Registration.is_document_state(state) else state
         self.user_data_markdown = lambda user: "\n".join([
-            f"{state}: *{user[state] if not Registration.is_document_state(state) else state}*"
+            f"{state}: *{self.get_state_string(user, state)}*"
             for state in Registration.main_states
         ]) + f"\n*{I18n.is_active if self.is_active(user) else I18n.is_inactive}*"
         self.user_data_inline_keyboard = lambda user: InlineKeyboardMarkup([
             [
                 InlineKeyboardButton(
-                    user[state] if not Registration.is_document_state(state) else state,
+                    self.get_state_string(user, state),
                     callback_data=self.CALLBACK_USER_CHANGE_STATE_TEMPLATE.format(state=state))
             ]
             for state in Registration.main_states
         ] + [[
             InlineKeyboardButton(
                 I18n.set_inactive if self.is_active(user) else I18n.set_active,
                 callback_data=self.CALLBACK_USER_SET_INACTIVE if self.is_active(user) else self.CALLBACK_USER_SET_ACTIVE
@@ -111,44 +111,42 @@
     
     async def banned(self, chat_id: int|str):
         await self._update_record(chat_id, 'is_bot_banned', I18n.yes)
     
     async def unbanned(self, chat_id: int|str):
         await self._update_record(chat_id, 'is_bot_banned', I18n.no)
     
-    async def _change_message_after_callback(self, chat_id: int|str, message_id: int|str, bot: Bot) -> None:
-        try:
-            user = self._get(self.selector(chat_id))
-            keyboard_row = Keyboard.registration_keyboard_row
-            await bot.edit_message_text(
-                keyboard_row.text_markdown.format(user=self.user_data_markdown(user)),
-                chat_id=chat_id,
-                message_id=message_id,
-                reply_markup=self.user_data_inline_keyboard(user),
-                parse_mode=ParseMode.MARKDOWN
-            )
-        except Exception:
-            Log.debug(f"Was not able to edit a message for chat id {chat_id}")
+    async def _change_message_after_callback(self, chat_id: int|str, message_id: int|str, app: Application) -> None:
+        user = self._get(self.selector(chat_id))
+        keyboard_row = Keyboard.registration_keyboard_row
+        message = keyboard_row.text_markdown.format(user=self.user_data_markdown(user))
+        reply_markup = self.user_data_inline_keyboard(user)
+        app.create_task(
+            app.bot.edit_message_text(
+                message, chat_id=chat_id, message_id=message_id, reply_markup=reply_markup, parse_mode=ParseMode.MARKDOWN
+            ),
+            self._create_update_context('Message change', chat_id=chat_id, message_id=message_id, reply_markup=reply_markup)
+        )
 
     def _prepare_state_to_save(self, message: Message, document_link: str) -> tuple[str|TelegramObject|None, str|None]:
         if document_link in ["", None]:
             return(message.text, None)
         elif len(message.photo) != 0:
             return(message.photo, document_link)
         elif message.document != None:
             return(message.document, document_link)
         return (None, None)
     
-    async def send_notification_to_all_users(self, bot: Bot, message: str, parse_mode: str,
+    async def send_notification_to_all_users(self, app: Application, message: str, parse_mode: str,
                                              send_photo: str = None, state: str = None,
                                              condition: str = None):
         condition_column = 'is_active' if condition in [None, ''] else condition
-        await self._send_to_all_uids(
+        self._send_to_all_uids(
             self.selector_condition(condition_column),
-            bot, message, parse_mode,
+            app, message, parse_mode,
             send_photo,
             reply_markup=Notifications.get_keyboard(state)
         )
     
     class PrivateChatClass(AbstractSheetAdapter.AbstractFilter):
         def filter(self, message: Message) -> bool:
             return message.chat.type == Chat.PRIVATE
@@ -252,20 +250,18 @@
         await self._batch_update_or_create_record(update.effective_chat.id, save_to=save_to, save_as=save_as, app=context.application,
             state = '' if last_state else registration_next.state,
             **update_vals
         )
 
         count = self.active_user_count()
         if last_main_state and self.should_send_report(count):
-            context.application.create_task(
-                Groups.send_to_all_admin_groups(
-                    context.bot,
-                    Report.currently_active_users_template.format(count=count),
-                    ParseMode.MARKDOWN
-                )
+            Groups.send_to_all_admin_groups(
+                context.application,
+                Report.currently_active_users_template.format(count=count),
+                ParseMode.MARKDOWN
             )
     
     async def restart_help_on_registration_complete_handler(self, update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
         template = Settings.user_template_from_update(update)
         await update.message.reply_markdown(
             template.format(template = Settings.restart_on_registration_complete),
             reply_markup=Keyboard.reply_keyboard
@@ -307,15 +303,15 @@
             I18n.has_been_set_inactive if update.callback_query.data == self.CALLBACK_USER_SET_INACTIVE else I18n.has_been_set_active,
             reply_markup=Keyboard.reply_keyboard,
             parse_mode=ParseMode.MARKDOWN
         )
         await self._update_record(update.effective_chat.id, 'is_active',
             I18n.no if update.callback_query.data == self.CALLBACK_USER_SET_INACTIVE else I18n.yes
         )
-        await self._change_message_after_callback(update.effective_chat.id, update.callback_query.message.message_id, context.bot)
+        await self._change_message_after_callback(update.effective_chat.id, update.callback_query.message.message_id, context.application)
     
     async def change_state_callback_handler(self, update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
         await update.callback_query.answer()
         state = update.callback_query.data.removeprefix(self.CALLBACK_USER_CHANGE_STATE_PREFIX)
         registration = Registration.get(state)
         await context.bot.send_message(
             update.effective_chat.id,
@@ -358,15 +354,15 @@
         )
         await self._batch_update_or_create_record(update.effective_chat.id, save_to=save_to, save_as=save_as, app=context.application,
             state = '',
             **{
                 state: state_val
             }
         )
-        await self._change_message_after_callback(update.effective_chat.id, message_id, context.bot)
+        await self._change_message_after_callback(update.effective_chat.id, message_id, context.application)
     
     async def restart_help_notification_handler(self, update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
         template = Settings.user_template_from_update(update)
         state = self.state(update.effective_chat.id)
         await update.message.reply_markdown(
             template.format(template = Notifications.get_text_markdown(state)),
             reply_markup=Notifications.get_keyboard(state)
@@ -412,24 +408,25 @@
         await self._batch_update_or_create_record(update.effective_chat.id, save_to=save_to, save_as=save_as, app=context.application,
             state = '',
             **{state: state_val}
         )
     
     async def strange_error_handler(self, update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
         await update.message.reply_markdown(Settings.strange_user_error, reply_markup=ReplyKeyboardRemove())
+        chat_id = update.effective_chat.id
         message = (
-            f"Strange error on user with id `{update.effective_chat.id}` "
+            f"Strange error on user with id `{chat_id}` "
             f"and username `{update.effective_chat.username}` "
             f"- user is not registered, but the bot is active"
         )
         Log.info(message)
-        context.application.create_task(
-            LogSheet.write(update.effective_chat.id, (
-                f"Strange error, user {update.effective_chat.username} "
-                f"is not registered, but the bot is active"
-            ))
+        log_sheet_message = (
+            f"Strange error, user {update.effective_chat.username} "
+            f"is not registered, but the bot is active"
         )
         context.application.create_task(
-            Groups.send_to_all_superadmin_groups(context.bot, message, ParseMode.MARKDOWN)
+            LogSheet.write(chat_id, log_sheet_message),
+            self._create_update_context('Log sheet write', message=log_sheet_message, user_id=chat_id)
         )
+        Groups.send_to_all_superadmin_groups(context.application, message, ParseMode.MARKDOWN)
 
 Users = UsersAdapterClass()
```

### Comparing `spreadsheetbot-2.0.2/.gitignore` & `spreadsheetbot-2.1.0/.gitignore`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/LICENSE.txt` & `spreadsheetbot-2.1.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/README.md` & `spreadsheetbot-2.1.0/README.md`

 * *Files identical despite different names*

### Comparing `spreadsheetbot-2.0.2/pyproject.toml` & `spreadsheetbot-2.1.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "spreadsheetbot"
-version = "2.0.2"
+version = "2.1.0"
 authors = [
   { name="Egor Dubrovin", email="dubrovin.en@ya.ru" },
 ]
 description = "Google Spreadsheet-based Telegram Bot Package"
 readme = "README.md"
 requires-python = ">=3.11"
 classifiers = [
```

### Comparing `spreadsheetbot-2.0.2/PKG-INFO` & `spreadsheetbot-2.1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spreadsheetbot
-Version: 2.0.2
+Version: 2.1.0
 Summary: Google Spreadsheet-based Telegram Bot Package
 Project-URL: Homepage, https://github.com/twobrowin-study/spreadsheetbot-lib
 Project-URL: Bug Tracker, https://github.com/twobrowin-study/spreadsheetbot-lib/issues
 Author-email: Egor Dubrovin <dubrovin.en@ya.ru>
 License-File: LICENSE.txt
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

