# Comparing `tmp/pyxk-0.5.5.tar.gz` & `tmp/pyxk-0.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyxk-0.5.5.tar", last modified: Sat May 13 09:33:26 2023, max compression
+gzip compressed data, was "pyxk-0.5.6.tar", last modified: Sat May 13 09:36:54 2023, max compression
```

## Comparing `pyxk-0.5.5.tar` & `pyxk-0.5.6.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/
--rw-rw----   0 root         (0) everybody  (9997)     1079 2022-09-01 11:31:05.000000 pyxk-0.5.5/LICENSE
--rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:33:26.034000 pyxk-0.5.5/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)        4 2023-03-31 15:33:16.000000 pyxk-0.5.5/README.md
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk/
--rw-rw----   0 root         (0) everybody  (9997)       53 2023-05-08 09:38:07.000000 pyxk-0.5.5/pyxk/__init__.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk/aclient/
--rw-rw----   0 root         (0) everybody  (9997)       49 2023-05-13 08:37:44.000000 pyxk-0.5.5/pyxk/aclient/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)    17711 2023-05-13 08:47:34.000000 pyxk-0.5.5/pyxk/aclient/client.py
--rw-rw----   0 root         (0) everybody  (9997)      615 2023-05-13 05:40:17.000000 pyxk-0.5.5/pyxk/aclient/typedef.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/aes/
--rw-rw----   0 root         (0) everybody  (9997)       79 2023-04-10 03:10:37.000000 pyxk-0.5.5/pyxk/aes/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     3633 2023-05-08 07:57:14.000000 pyxk-0.5.5/pyxk/aes/_fmtdata.py
--rw-rw----   0 root         (0) everybody  (9997)     4695 2023-05-08 07:56:51.000000 pyxk-0.5.5/pyxk/aes/cryptor.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/m3u8downloader/
--rw-rw----   0 root         (0) everybody  (9997)       66 2023-05-08 07:55:15.000000 pyxk-0.5.5/pyxk/m3u8downloader/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     3484 2023-05-13 09:31:31.000000 pyxk-0.5.5/pyxk/m3u8downloader/enter_point.py
--rw-rw----   0 root         (0) everybody  (9997)     4884 2023-05-13 09:28:48.000000 pyxk-0.5.5/pyxk/m3u8downloader/m3u8download.py
--rw-rw----   0 root         (0) everybody  (9997)     2968 2023-05-08 04:33:43.000000 pyxk-0.5.5/pyxk/m3u8downloader/m3u8parse.py
--rw-rw----   0 root         (0) everybody  (9997)    11732 2023-05-13 09:23:24.000000 pyxk-0.5.5/pyxk/m3u8downloader/main.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/requests/
--rw-rw----   0 root         (0) everybody  (9997)      247 2023-05-08 07:57:36.000000 pyxk-0.5.5/pyxk/requests/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     7480 2023-05-08 07:58:19.000000 pyxk-0.5.5/pyxk/requests/api.py
--rw-rw----   0 root         (0) everybody  (9997)     3309 2023-05-09 03:19:15.000000 pyxk-0.5.5/pyxk/requests/entry_point.py
--rw-rw----   0 root         (0) everybody  (9997)    14682 2023-05-09 03:23:24.000000 pyxk-0.5.5/pyxk/requests/sessions.py
--rw-rw----   0 root         (0) everybody  (9997)    19219 2023-05-13 07:41:11.000000 pyxk-0.5.5/pyxk/utils.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      627 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)       99 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/entry_points.txt
--rw-rw----   0 root         (0) everybody  (9997)       55 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/requires.txt
--rw-rw----   0 root         (0) everybody  (9997)        5 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)       38 2023-05-13 09:33:26.034000 pyxk-0.5.5/setup.cfg
--rw-rw----   0 root         (0) everybody  (9997)      927 2023-05-13 09:33:13.000000 pyxk-0.5.5/setup.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/
+-rw-rw----   0 root         (0) everybody  (9997)     1079 2022-09-01 11:31:05.000000 pyxk-0.5.6/LICENSE
+-rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:36:54.033999 pyxk-0.5.6/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)        4 2023-03-31 15:33:16.000000 pyxk-0.5.6/README.md
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk/
+-rw-rw----   0 root         (0) everybody  (9997)       53 2023-05-08 09:38:07.000000 pyxk-0.5.6/pyxk/__init__.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk/aclient/
+-rw-rw----   0 root         (0) everybody  (9997)       49 2023-05-13 08:37:44.000000 pyxk-0.5.6/pyxk/aclient/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)    17711 2023-05-13 08:47:34.000000 pyxk-0.5.6/pyxk/aclient/client.py
+-rw-rw----   0 root         (0) everybody  (9997)      615 2023-05-13 05:40:17.000000 pyxk-0.5.6/pyxk/aclient/typedef.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk/aes/
+-rw-rw----   0 root         (0) everybody  (9997)       79 2023-04-10 03:10:37.000000 pyxk-0.5.6/pyxk/aes/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     3633 2023-05-08 07:57:14.000000 pyxk-0.5.6/pyxk/aes/_fmtdata.py
+-rw-rw----   0 root         (0) everybody  (9997)     4695 2023-05-08 07:56:51.000000 pyxk-0.5.6/pyxk/aes/cryptor.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk/m3u8downloader/
+-rw-rw----   0 root         (0) everybody  (9997)       66 2023-05-08 07:55:15.000000 pyxk-0.5.6/pyxk/m3u8downloader/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     3462 2023-05-13 09:36:19.000000 pyxk-0.5.6/pyxk/m3u8downloader/enter_point.py
+-rw-rw----   0 root         (0) everybody  (9997)     4884 2023-05-13 09:28:48.000000 pyxk-0.5.6/pyxk/m3u8downloader/m3u8download.py
+-rw-rw----   0 root         (0) everybody  (9997)     2968 2023-05-08 04:33:43.000000 pyxk-0.5.6/pyxk/m3u8downloader/m3u8parse.py
+-rw-rw----   0 root         (0) everybody  (9997)    11732 2023-05-13 09:23:24.000000 pyxk-0.5.6/pyxk/m3u8downloader/main.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk/requests/
+-rw-rw----   0 root         (0) everybody  (9997)      247 2023-05-08 07:57:36.000000 pyxk-0.5.6/pyxk/requests/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     7480 2023-05-08 07:58:19.000000 pyxk-0.5.6/pyxk/requests/api.py
+-rw-rw----   0 root         (0) everybody  (9997)     3309 2023-05-09 03:19:15.000000 pyxk-0.5.6/pyxk/requests/entry_point.py
+-rw-rw----   0 root         (0) everybody  (9997)    14682 2023-05-09 03:23:24.000000 pyxk-0.5.6/pyxk/requests/sessions.py
+-rw-rw----   0 root         (0) everybody  (9997)    19219 2023-05-13 07:41:11.000000 pyxk-0.5.6/pyxk/utils.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:36:54.033999 pyxk-0.5.6/pyxk.egg-info/
+-rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)      627 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/SOURCES.txt
+-rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/dependency_links.txt
+-rw-rw----   0 root         (0) everybody  (9997)       99 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/entry_points.txt
+-rw-rw----   0 root         (0) everybody  (9997)       55 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/requires.txt
+-rw-rw----   0 root         (0) everybody  (9997)        5 2023-05-13 09:36:53.000000 pyxk-0.5.6/pyxk.egg-info/top_level.txt
+-rw-rw----   0 root         (0) everybody  (9997)       38 2023-05-13 09:36:54.033999 pyxk-0.5.6/setup.cfg
+-rw-rw----   0 root         (0) everybody  (9997)      927 2023-05-13 09:36:32.000000 pyxk-0.5.6/setup.py
```

### Comparing `pyxk-0.5.5/LICENSE` & `pyxk-0.5.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/aclient/client.py` & `pyxk-0.5.6/pyxk/aclient/client.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/aclient/typedef.py` & `pyxk-0.5.6/pyxk/aclient/typedef.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/aes/_fmtdata.py` & `pyxk-0.5.6/pyxk/aes/_fmtdata.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/aes/cryptor.py` & `pyxk-0.5.6/pyxk/aes/cryptor.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/m3u8downloader/enter_point.py` & `pyxk-0.5.6/pyxk/m3u8downloader/enter_point.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,24 +10,24 @@
 @click.option("--reserve", is_flag=True, help="保留m3u8资源")
 @click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
 @click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
 @click.option("-l", "--limit", "limit", type=int, default=16, help="下载并发量")
 @click.option("-ua", "--user-agent", "user_agent", type=str, default=None, help="User-Agent")
 @click.pass_context
 def main(ctx, output, reload, reserve, headers, verify, limit, user_agent):
-    """下载m3u8资源 - m3u8 url"""
+    """m3u8下载器"""
     if not ctx.obj or not isinstance(ctx.obj, dict):
         ctx.obj = {}
     # 将参数传递给子命令
     if ctx.invoked_subcommand:
         ctx.obj.update(ctx.params)
 
 @main.command
 @click.pass_obj
-@click.argument("content", type=click.Path(exists=True), metavar="<FilePath>")
+@click.argument("content", type=click.Path(exists=True), metavar="<File>")
 @click.option("-u", "--url", "url", type=str, default=None, help="m3u8 url")
 @click.option("-o", "--output", "output", type=str, default=None, help="M3U8存储路径")
 @click.option("--reload", is_flag=True, help="重载m3u8资源")
 @click.option("--reserve", is_flag=True, help="保留m3u8资源")
 @click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
 @click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
 @click.option("-l", "--limit", "limit", type=int, default=None, help="下载并发量")
@@ -44,24 +44,24 @@
         verify=verify,
         limit=limit or obj["limit"],
         user_agent=get_user_agent(user_agent or obj["user_agent"])
     )
 
 @main.command
 @click.pass_obj
-@click.argument("_url", type=str, metavar="<URL>")
+@click.argument("_url", type=str, metavar="<Url>")
 @click.option("-o", "--output", "output", type=str, default=None, help="M3U8存储路径")
 @click.option("--reload", is_flag=True, help="重载m3u8资源")
 @click.option("--reserve", is_flag=True, help="保留m3u8资源")
 @click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
 @click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
 @click.option("-l", "--limit", "limit", type=int, default=None, help="下载并发量")
 @click.option("-ua", "--user-agent", "user_agent", type=str, default=None, help="User-Agent")
 def url(obj, _url, output, reload, reserve, headers, verify, limit, user_agent):
-    """下载m3u8资源 - m3u8 content"""
+    """下载m3u8资源 - m3u8 url"""
     m3u8downloader.load_url(
         url=_url,
         output=output or obj["output"],
         reload=reload,
         reserve=reserve,
         headers=dict(headers or obj["headers"]),
         verify=verify,
```

### Comparing `pyxk-0.5.5/pyxk/m3u8downloader/m3u8download.py` & `pyxk-0.5.6/pyxk/m3u8downloader/m3u8download.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/m3u8downloader/m3u8parse.py` & `pyxk-0.5.6/pyxk/m3u8downloader/m3u8parse.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/m3u8downloader/main.py` & `pyxk-0.5.6/pyxk/m3u8downloader/main.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/requests/api.py` & `pyxk-0.5.6/pyxk/requests/api.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/requests/entry_point.py` & `pyxk-0.5.6/pyxk/requests/entry_point.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/requests/sessions.py` & `pyxk-0.5.6/pyxk/requests/sessions.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk/utils.py` & `pyxk-0.5.6/pyxk/utils.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/pyxk.egg-info/SOURCES.txt` & `pyxk-0.5.6/pyxk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.5/setup.py` & `pyxk-0.5.6/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pyxk",
-    version="0.5.5",
+    version="0.5.6",
     author="pengke",
     install_requires=[
         "requests",
         "pycryptodome",
         "rich",
         "m3u8",
         "aiohttp",
```

