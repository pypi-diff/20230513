# Comparing `tmp/nonebot-plugin-starrail-calendar-1.0.3.tar.gz` & `tmp/nonebot_plugin_starrail_calendar-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot-plugin-starrail-calendar-1.0.3.tar", last modified: Tue May  2 04:23:59 2023, max compression
+gzip compressed data, was "nonebot_plugin_starrail_calendar-1.0.4.tar", max compression
```

## Comparing `nonebot-plugin-starrail-calendar-1.0.3.tar` & `nonebot_plugin_starrail_calendar-1.0.4.tar`

### file list

```diff
@@ -1,24 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-05-02 04:23:59.619198 nonebot-plugin-starrail-calendar-1.0.3/
--rw-rw-rw-   0        0        0    35823 2022-05-26 22:27:12.000000 nonebot-plugin-starrail-calendar-1.0.3/LICENSE
--rw-rw-rw-   0        0        0       83 2023-05-02 04:23:25.000000 nonebot-plugin-starrail-calendar-1.0.3/MANIFEST.in
--rw-rw-rw-   0        0        0      414 2023-05-02 04:23:59.618074 nonebot-plugin-starrail-calendar-1.0.3/PKG-INFO
--rw-rw-rw-   0        0        0      598 2023-05-02 01:45:54.000000 nonebot-plugin-starrail-calendar-1.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-02 04:23:59.597920 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/
--rw-rw-rw-   0        0        0     6265 2023-05-02 02:36:57.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/__init__.py
--rw-rw-rw-   0        0        0     2387 2022-10-25 13:40:10.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/browser.py
--rw-rw-rw-   0        0        0     4739 2023-05-02 02:09:58.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/data_source.py
--rw-rw-rw-   0        0        0     1901 2023-05-02 03:04:38.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/draw_calendar.py
-drwxrwxrwx   0        0        0        0 2023-05-02 04:23:59.616300 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/
--rw-rw-rw-   0        0        0     2371 2023-05-01 13:36:07.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/calendar.html
--rw-rw-rw-   0        0        0     6882 2022-06-26 03:57:47.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/index.css
--rw-rw-rw-   0        0        0   315626 2022-06-26 03:57:47.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/iview.css
--rw-rw-rw-   0        0        0     6346 2022-06-26 03:57:47.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/normalize.css
--rw-rw-rw-   0        0        0     2255 2023-04-29 01:27:19.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-02 04:23:59.610276 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/
--rw-rw-rw-   0        0        0      414 2023-05-02 04:23:59.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      762 2023-05-02 04:23:59.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-02 04:23:59.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      116 2023-05-02 04:23:59.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/requires.txt
--rw-rw-rw-   0        0        0       33 2023-05-02 04:23:59.000000 nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-02 04:23:59.619198 nonebot-plugin-starrail-calendar-1.0.3/setup.cfg
--rw-rw-rw-   0        0        0      847 2023-05-02 04:23:51.000000 nonebot-plugin-starrail-calendar-1.0.3/setup.py
+-rw-r--r--   0        0        0    35823 2022-05-26 22:27:12.688017 nonebot_plugin_starrail_calendar-1.0.4/LICENSE
+-rw-r--r--   0        0        0       50 2023-05-09 12:28:29.877145 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/.gitignore
+-rw-r--r--   0        0        0      273 2023-05-09 12:28:29.715697 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/misc.xml
+-rw-r--r--   0        0        0      323 2023-05-09 12:28:29.696706 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/modules.xml
+-rw-r--r--   0        0        0      344 2023-05-09 12:28:29.684758 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/nonebot_plugin_starrail_calendar.iml
+-rw-r--r--   0        0        0      188 2023-05-09 12:28:29.729563 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/vcs.xml
+-rw-r--r--   0        0        0     5550 2023-05-09 12:33:57.768042 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/__init__.py
+-rw-r--r--   0        0        0     2387 2022-10-25 13:40:10.642123 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/browser.py
+-rw-r--r--   0        0        0     4739 2023-05-02 02:09:58.604479 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/data_source.py
+-rw-r--r--   0        0        0     1901 2023-05-02 03:04:38.808483 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/draw_calendar.py
+-rw-r--r--   0        0        0     2371 2023-05-01 13:36:07.373205 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/calendar.html
+-rw-r--r--   0        0        0     6882 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/index.css
+-rw-r--r--   0        0        0   315626 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/iview.css
+-rw-r--r--   0        0        0     6346 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/normalize.css
+-rw-r--r--   0        0        0     2255 2023-04-29 01:27:19.441019 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/utils.py
+-rw-r--r--   0        0        0      546 2023-05-13 06:56:42.245245 nonebot_plugin_starrail_calendar-1.0.4/pyproject.toml
+-rw-r--r--   0        0        0      596 2023-05-09 12:37:06.326249 nonebot_plugin_starrail_calendar-1.0.4/README.md
+-rw-r--r--   0        0        0     1090 1970-01-01 00:00:00.000000 nonebot_plugin_starrail_calendar-1.0.4/PKG-INFO
```

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/LICENSE` & `nonebot_plugin_starrail_calendar-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/README.md` & `nonebot_plugin_starrail_calendar-1.0.4/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -5,21 +5,21 @@
 </div>
 
 
 ## 安装
 
 通过 `nb`或 `pip` 命令安装插件
 
-`pip install nonebot_plugin_star_rail_calendar`
+`pip install nonebot_plugin_starrail_calendar`
 <br>或<br>
-`nb plugin install nonebot_plugin_star_rail_calendar`
+`nb plugin install nonebot_plugin_starrail_calendar`
 
 ## 命令
 
 `<星穹/星琼>日历` 查看本群订阅服务器日历<br>
 `<星穹/星琼>日历 on/off` 订阅/取消指定服务器的日历推送<br>
-`<星穹/星琼>日历 time 时:分`  设置原神日历推送时间<br>
-`<星穹/星琼>日历 status`  查看原神日历推送设置
+`<星穹/星琼>日历 time 时:分`  设置星穹日历推送时间<br>
+`<星穹/星琼>日历 status`  查看星穹日历推送设置
 
 
 ### 功能演示
 ![calendar](preview.jpg)
```

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/__init__.py` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -77,19 +77,15 @@
     server = 'cn'
     fun = msg.extract_plain_text().strip()
     action = re.search(r'(?P<action>on|off|time|status|cardimage)', fun)
     if not fun:
         im = await generate_day_schedule(server, viewport={"width": 600, "height": 10})
 
         try:
-            if group_id not in group_data or 'cardimage' not in group_data[group_id] or not group_data[group_id][
-                'cardimage']:
-                await calendar.finish(MessageSegment.image(im))
-            else:
-                await calendar.finish(f'[CQ:cardimage,file={im}]')
+            await calendar.finish(f'[CQ:cardimage,file={im}]')
         except ActionFailed as e:
             logging.error(e)
 
     elif action:
 
         # 添加定时推送任务
         if action.group('action') == 'on':
@@ -147,28 +143,20 @@
                         at_sender=True)
 
             else:
                 await calendar.finish("请给出正确的时间，格式为12:00", at_sender=True)
 
         # 查询订阅推送状态
         elif action.group('action') == "status":
-            message = "订阅日历: {0}\n" \
-                      "推送时间: {1}:{2}".format(
-                group_data[group_id]['server_list'],
-                group_data[group_id]['hour'],
-                group_data[group_id]['minute']
-            )
-            await calendar.finish(message)
+            try:
+                message = "订阅日历: {0}\n" \
+                          "推送时间: {1}:{2}".format(
+                    group_data[group_id]['server_list'],
+                    group_data[group_id]['hour'],
+                    group_data[group_id]['minute']
+                )
+                await calendar.finish(message)
+            except KeyError as e:
+                await calendar.finish("当前Q群尚未开启日历推送，无法查看推送状态")
+
 
-        # 切换cardImage模式
-        elif action.group('action') == "cardimage":
-            if 'cardimage' not in group_data[group_id] or not group_data[group_id]['cardimage']:
-                group_data[group_id]['cardimage'] = True
-                save_data(group_data, 'data.json')
-                await calendar.finish('已切换为cardimage模式', at_sender=True)
-            else:
-                group_data[group_id]['cardimage'] = False
-                save_data(group_data, 'data.json')
-                await calendar.finish('已切换为标准image模式', at_sender=True)
-        else:
-            await calendar.finish('指令错误', at_sender=True)
```

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/browser.py` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/browser.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/data_source.py` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/data_source.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/draw_calendar.py` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/draw_calendar.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/calendar.html` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/calendar.html`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/index.css` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/index.css`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/iview.css` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/iview.css`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/template/normalize.css` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/normalize.css`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-starrail-calendar-1.0.3/nonebot_plugin_starrail_calendar/utils.py` & `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/utils.py`

 * *Files identical despite different names*

