# Comparing `tmp/openai_forward-0.1.8.tar.gz` & `tmp/openai_forward-0.1.9.tar.gz`

## Comparing `openai_forward-0.1.8.tar` & `openai_forward-0.1.9.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0       69 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/__init__.py
--rw-r--r--   0        0        0     1505 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/__main__.py
--rw-r--r--   0        0        0      675 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/app.py
--rw-r--r--   0        0        0     5204 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/base.py
--rw-r--r--   0        0        0     3135 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/config.py
--rw-r--r--   0        0        0      694 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/openai.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/content/__init__.py
--rw-r--r--   0        0        0     3418 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/content/chat.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/content/image.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/routers/__init__.py
--rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/routers/openai_v1.py
--rw-r--r--   0        0        0     2272 2020-02-02 00:00:00.000000 openai_forward-0.1.8/openai_forward/routers/schemas.py
--rw-r--r--   0        0        0     1897 2020-02-02 00:00:00.000000 openai_forward-0.1.8/.gitignore
--rw-r--r--   0        0        0     1064 2020-02-02 00:00:00.000000 openai_forward-0.1.8/LICENSE
--rw-r--r--   0        0        0     8655 2020-02-02 00:00:00.000000 openai_forward-0.1.8/README.md
--rw-r--r--   0        0        0     1646 2020-02-02 00:00:00.000000 openai_forward-0.1.8/pyproject.toml
--rw-r--r--   0        0        0     9945 2020-02-02 00:00:00.000000 openai_forward-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0       69 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/__init__.py
+-rw-r--r--   0        0        0     1586 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/__main__.py
+-rw-r--r--   0        0        0      802 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/app.py
+-rw-r--r--   0        0        0     5214 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/base.py
+-rw-r--r--   0        0        0     4203 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/config.py
+-rw-r--r--   0        0        0      694 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/openai.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/content/__init__.py
+-rw-r--r--   0        0        0     4169 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/content/chat.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/content/image.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/routers/__init__.py
+-rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/routers/openai_v1.py
+-rw-r--r--   0        0        0     2272 2020-02-02 00:00:00.000000 openai_forward-0.1.9/openai_forward/routers/schemas.py
+-rw-r--r--   0        0        0     1907 2020-02-02 00:00:00.000000 openai_forward-0.1.9/.gitignore
+-rw-r--r--   0        0        0     1064 2020-02-02 00:00:00.000000 openai_forward-0.1.9/LICENSE
+-rw-r--r--   0        0        0     8751 2020-02-02 00:00:00.000000 openai_forward-0.1.9/README.md
+-rw-r--r--   0        0        0     1662 2020-02-02 00:00:00.000000 openai_forward-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0    10064 2020-02-02 00:00:00.000000 openai_forward-0.1.9/PKG-INFO
```

### Comparing `openai_forward-0.1.8/openai_forward/__main__.py` & `openai_forward-0.1.9/openai_forward/__main__.py`

 * *Files 17% similar despite different names*

```diff
@@ -4,40 +4,44 @@
 
 
 class Cli:
     @staticmethod
     def run(port=8000,
             workers=1,
             api_key=None,
+            forward_key=None,
             base_url=None,
             log_chat=None,
             route_prefix=None,
             ip_whitelist=None,
             ip_blacklist=None,
             ):
         """ Run forwarding serve.
 
         Parameters
         ----------
 
         port: int, default 8000
-        workers: int, default 1
-        api_key: str, default None
-        base_url: str, default None
-        log_chat: str, default None
-        route_prefix: str, default None
-        ip_whitelist: str, default None
-        ip_blacklist: str, default None
+        workers: int, 1
+        api_key: str, None
+        forward_key: str, None
+        base_url: str, None
+        log_chat: str, None
+        route_prefix: str, None
+        ip_whitelist: str, None
+        ip_blacklist: str, None
         """
         if base_url:
             os.environ['OPENAI_BASE_URL'] = base_url
-        if log_chat:
-            os.environ['LOG_CHAT'] = log_chat
         if api_key:
             os.environ['OPENAI_API_KEY'] = api_key
+        if forward_key:
+            os.environ['FORWARD_KEY'] = forward_key
+        if log_chat:
+            os.environ['LOG_CHAT'] = log_chat
         if route_prefix:
             os.environ['ROUTE_PREFIX'] = route_prefix
         if ip_whitelist:
             os.environ['IP_WHITELIST'] = ip_whitelist
         if ip_blacklist:
             os.environ['IP_BLACKLIST'] = ip_blacklist
```

### Comparing `openai_forward-0.1.8/openai_forward/base.py` & `openai_forward-0.1.9/openai_forward/base.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from fastapi import Request, HTTPException, status
 from fastapi.responses import StreamingResponse
 from loguru import logger
 import httpx
 from starlette.background import BackgroundTask
 import os
 from itertools import cycle
-from .content.chat import parse_chat_completions, ChatSaver
-from .config import env2list
+from .content.chat import ChatSaver
+from .config import env2list, print_startup_info
 
 
 class OpenaiBase:
     BASE_URL = os.environ.get("OPENAI_BASE_URL", "https://api.openai.com").strip()
     ROUTE_PREFIX = os.environ.get("ROUTE_PREFIX", "").strip()
     _LOG_CHAT = os.environ.get("LOG_CHAT", "False").strip().lower() == "true"
     _openai_api_key_list = env2list("OPENAI_API_KEY", sep=" ")
@@ -23,36 +23,33 @@
     if ROUTE_PREFIX:
         if ROUTE_PREFIX.endswith('/'):
             ROUTE_PREFIX = ROUTE_PREFIX[:-1]
         if not ROUTE_PREFIX.startswith('/'):
             ROUTE_PREFIX = '/' + ROUTE_PREFIX
     timeout = 30
     chatsaver = ChatSaver(save_interval=10)
+    print_startup_info(BASE_URL, ROUTE_PREFIX, _openai_api_key_list, _FWD_KEYS, _LOG_CHAT)
 
     def validate_request_host(self, ip):
         if self.IP_WHITELIST and ip not in self.IP_WHITELIST:
             raise HTTPException(status_code=status.HTTP_403_FORBIDDEN,
                                 detail=f"Forbidden, ip={ip} not in whitelist!")
         if self.IP_BLACKLIST and ip in self.IP_BLACKLIST:
             raise HTTPException(status_code=status.HTTP_403_FORBIDDEN,
                                 detail=f"Forbidden, ip={ip} in blacklist!")
 
     @classmethod
-    def log_chat_completions(cls, bytes_: bytes):
-        target_info = parse_chat_completions(bytes_)
-        cls.chatsaver.add_chat({target_info['role']: target_info['content']})
-
-    @classmethod
-    async def aiter_bytes(cls, r: httpx.Response):
+    async def aiter_bytes(cls, r: httpx.Response, route_path: str):
         bytes_ = b''
         async for chunk in r.aiter_bytes():
             bytes_ += chunk
             yield chunk
         try:
-            cls.log_chat_completions(bytes_)
+            target_info = cls.chatsaver.parse_bytes_to_content(bytes_, route_path)
+            cls.chatsaver.add_chat({target_info['role']: target_info['content']})
         except Exception as e:
             logger.debug(f"log chat (not) error:\n{e=}")
 
     @classmethod
     async def _reverse_proxy(cls, request: Request):
         client: httpx.AsyncClient = request.app.state.client
         url_path = request.url.path
@@ -74,47 +71,43 @@
                     tmp_headers = {}
             else:
                 auth = "Bearer " + next(cls._cycle_api_key)
                 tmp_headers = {'Authorization': auth}
         else:
             tmp_headers = {}
 
-        if cls._LOG_CHAT:
+        log_chat_completions = False
+        if cls._LOG_CHAT and request.method == 'POST':
             try:
-                input_info = await request.json()
-                msgs = input_info['messages']
-                cls.chatsaver.add_chat({
-                    "host": request.client.host,
-                    "model": input_info['model'],
-                    "messages": [{msg['role']: msg['content']} for msg in msgs],
-                })
+                chat_info = await cls.chatsaver.parse_payload_to_content(request, route_path=url_path)
+                if chat_info:
+                    cls.chatsaver.add_chat(chat_info)
+                    log_chat_completions = True
             except Exception as e:
-                logger.debug(f"log chat (not) error:\n{request.client.host=}: {e}")
-
-        headers.pop("host", None)
-        headers.update(tmp_headers)
+                logger.debug(f"log chat error:\n{request.client.host=} {request.method=}: {e}")
 
+        tmp_headers.update({"Content-Type": "application/json"})
         req = client.build_request(
-            request.method, url, headers=headers,
+            request.method, url, headers=tmp_headers,
             content=request.stream(),
             timeout=cls.timeout,
         )
         try:
             r = await client.send(req, stream=True)
         except (httpx.ConnectError, httpx.ConnectTimeout) as e:
             error_info = f"{type(e)}: {e} | " \
-                         f"Please check if host={request.client.host} can access [{cls.BASE_URL}] successfully."
+                         f"Please check if host={request.client.host} can access [{cls.BASE_URL}] successfully?"
             logger.error(error_info)
             raise HTTPException(status_code=status.HTTP_504_GATEWAY_TIMEOUT, detail=error_info)
         except Exception as e:
             error_info = f"{type(e)}: {e}"
             logger.error(error_info)
             raise HTTPException(status_code=status.HTTP_500_INTERNAL_SERVER_ERROR, detail=error_info)
 
-        aiter_bytes = cls.aiter_bytes(r) if cls._LOG_CHAT else r.aiter_bytes()
+        aiter_bytes = cls.aiter_bytes(r, url_path) if log_chat_completions else r.aiter_bytes()
         return StreamingResponse(
             aiter_bytes,
             status_code=r.status_code,
             # headers=r.headers, # do not use r.headers, it will cause error
             media_type=r.headers.get("content-type"),
             background=BackgroundTask(r.aclose)
         )
```

### Comparing `openai_forward-0.1.8/openai_forward/config.py` & `openai_forward-0.1.9/openai_forward/config.py`

 * *Files 22% similar despite different names*

```diff
@@ -2,14 +2,37 @@
 import orjson
 from sparrow import relp
 from typing import Union, List, Dict
 import sys
 import logging
 import os
 import time
+from rich import print
+from rich.panel import Panel
+from rich.table import Table
+
+
+def print_startup_info(base_url, route_prefix, api_key, forward_key, log_chat):
+    try:
+        from dotenv import load_dotenv
+        load_dotenv('.env')
+    except Exception:
+        ...
+    route_prefix = route_prefix or "/"
+    api_key_info = True if len(api_key) else False
+    forward_key_info = True if len(forward_key) else False
+    table = Table(title="", box=None, width=100)
+    table.add_column("base-url", justify="left", style="#df412f")
+    table.add_column("route-prefix", justify="center", style="#df412f")
+    table.add_column("openai-api-key", justify="center", style="green")
+    table.add_column("forward-key", justify="center", style="green")
+    table.add_column("Log-chat", justify="center", style="green")
+    table.add_column("Log-dir", justify="center", style="#f5bb00")
+    table.add_row(base_url, route_prefix, str(api_key_info), str(forward_key_info), str(log_chat), "./Log/*.log")
+    print(Panel(table, title="🤗openai-forward is ready to serve!", expand=False))
 
 
 class InterceptHandler(logging.Handler):
     def emit(self, record):
         # Get corresponding Loguru level if it exists
         try:
             level = logger.level(record.levelname).name
@@ -25,15 +48,14 @@
 
 
 def setting_log(log_name, multi_process=True):
     # TODO 修复时区配置
     if os.environ.get("TZ") == "Asia/Shanghai":
         os.environ['TZ'] = "UTC-8"
         if hasattr(time, 'tzset'):
-            print(os.environ['TZ'])
             time.tzset()
 
     logging.root.handlers = [InterceptHandler()]
     for name in logging.root.manager.loggerDict.keys():
         logging.getLogger(name).handlers = []
         logging.getLogger(name).propagate = True
     logger_config = {
```

### Comparing `openai_forward-0.1.8/openai_forward/openai.py` & `openai_forward-0.1.9/openai_forward/openai.py`

 * *Files identical despite different names*

### Comparing `openai_forward-0.1.8/openai_forward/content/chat.py` & `openai_forward-0.1.9/openai_forward/content/chat.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import orjson
 from orjson import JSONDecodeError
 from loguru import logger
 from httpx._decoders import LineDecoder
+from fastapi import Request
 from pathlib import Path
 from sparrow import relp
 from typing import List, Dict
 import os
 
 decoder = LineDecoder()
 
@@ -62,14 +63,35 @@
     def chat_file(self):
         return os.path.join(self._log_dir, f"chat_{self._file_idx}.txt")
 
     def _init_chat_file(self):
         while Path(self.chat_file).exists():
             self._file_idx += 1
 
+    @staticmethod
+    async def parse_payload_to_content(request: Request, route_path: str):
+        payload = await request.json()
+        if route_path == "/v1/chat/completions":
+            msgs = payload['messages']
+            model = payload['model']
+            return {
+                "host": request.client.host,
+                "model": model,
+                "messages": [{msg['role']: msg['content']} for msg in msgs],
+            }
+        else:
+            return {}
+
+    @staticmethod
+    def parse_bytes_to_content(bytes_: bytes, route_path: str):
+        if route_path == "/v1/chat/completions":
+            return parse_chat_completions(bytes_)
+        else:
+            return {}
+
     def add_chat(self, chat_info: dict):
         logger.info(str(chat_info))
         self._chat_list.append(chat_info)
         self._cur_chat_file_size += 1
         self._save_chat()
 
     def _save_chat(self):
```

### Comparing `openai_forward-0.1.8/openai_forward/routers/schemas.py` & `openai_forward-0.1.9/openai_forward/routers/schemas.py`

 * *Files identical despite different names*

### Comparing `openai_forward-0.1.8/.gitignore` & `openai_forward-0.1.9/.gitignore`

 * *Files 9% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 .idea/
 .vscode/
+.DS_Store
 third-party/
 run.sh
 ssl/
 chat.yaml
 chat_*.yaml
 
 .env.example
```

### Comparing `openai_forward-0.1.8/LICENSE` & `openai_forward-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `openai_forward-0.1.8/README.md` & `openai_forward-0.1.9/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -35,37 +35,45 @@
     </a>
 </p>
 
 
 
 本项目用于解决一些地区无法直接访问OpenAI的问题，将该服务部署在可以正常访问openai
 api的服务器上，通过该服务转发OpenAI的请求。即搭建反向代理服务  
-测试访问：https://caloi.top/openai/v1/chat/completions 将等价于 https://api.openai.com/v1/chat/completions  
+
+---
+
+测试访问：https://caloi.top/openai/v1/chat/completions  
 或者说 https://caloi.top/openai 等价于 https://api.openai.com
 
-# Table of Contents
+---
 
-- [Features](#Features)
+# 目录
+
+- [功能](#功能)
 - [应用](#应用)
 - [安装部署](#安装部署)
 - [服务调用](#服务调用)
 - [配置选项](#配置选项)
 - [聊天日志](#聊天日志)
 - [高级配置](#高级配置)
 
-# Features
-
+# 功能
+**基础功能**  
 - [x] 支持转发OpenAI所有接口
 - [x] 支持流式响应
+- [x] 支持指定转发路由前缀
+- [x] docker部署
+- [x] pip 安装部署
+
+**高级功能**  
 - [x] 实时记录聊天记录(包括流式响应的聊天内容)
 - [x] 支持默认openai api key(多api key 循环调用)
-- [x] 转发api key (在已设置默认openai api key情况下使用)
-- [x] docker部署
-- [x] 支持指定转发路由前缀
-- [x] 支持请求IP验证
+- [x] 自定义forward api key 代替 openai api key (见高级配置)
+- [x] 支持请求IP验证(IP白名单与黑名单)
 
 # 应用
 
 > 这里以个人使用该项目搭建好的代理服务 https://caloi.top/openai 为例
 
 ### [caloi.top](https://caloi.top)
 
@@ -115,65 +123,65 @@
     "n": 1,
     "size": "512x512"
 }'
 ```
 
 # 安装部署
 
-提供3种服务部署方式,选择一种即可
+选择一种即可
 
 ## pip
-pip的安装方式目前在使用nginx反向代理时存在Bug, 建议使用Docker方式部署。  
+
 **安装**
 
 ```bash
 pip install openai-forward
 ```
 
 **运行转发服务**  
-可通过`--port`指定端口号，默认为`8000`，可通过`--workers`指定工作进程数，默认为`1`
+可通过`--port`指定端口号，默认为`8000`
 
 ```bash
-openai_forward run --port=9999 --workers=1
+openai_forward run --port=9999 
 ```
 
 服务就搭建完成了，使用方式只需将`https://api.openai.com` 替换为服务所在端口`http://{ip}:{port}` 即可。
 
-当然也可以将 OPENAI_API_KEY 作为环境变量传入作为默认api key， 这样客户端在请求相关路由时可以无需在Header中传入Authorization。
+当然也可以将 OPENAI_API_KEY 作为环境变量或`--api_key`参数传入作为默认api key， 这样客户端在请求相关路由时可以无需在Header中传入Authorization。
 带默认api key的启动方式：
 
 ```bash
-OPENAI_API_KEY="sk-xxx" openai_forward run --port=9999 --workers=1
+openai_forward run --port=9999 --api_key="sk-******"
 ```
 
 注: 如果既存在默认api key又在请求头中传入了api key，则以请求头中的api key会覆盖默认api key.
 
 ## Docker (推荐)
 
 ```bash
-docker run --name="openai-forward" -d -p 9999:8000 beidongjiedeguang/openai-forward:latest 
+docker run -d -p 9999:8000 beidongjiedeguang/openai-forward:latest 
 ```
 
 将映射宿主机的9999端口，通过`http://{ip}:9999`访问服务。  
 注：同样可以在启动命令中通过-e传入环境变量OPENAI_API_KEY=sk-xxx作为默认api key
 
 ## 源码部署
 
 ```bash
 git clone https://github.com/beidongjiedeguang/openai-forward.git --depth=1
 cd openai-forward
 ```
 
-**使用 docker**
+**Docker**
 
 ```bash
 docker-compose up
 ```
 
-**或使用pip**
+**pip**
 
 ```bash
 pip install -e .
 openai-forward run 
 ```
 
 # 服务调用
@@ -196,15 +204,15 @@
 
 | 配置项       | 说明 | 默认值 |
 |-----------| --- | :---: |
 | --port    | 服务端口号 | 8000 |
 | --workers | 工作进程数 | 1 |
 
 **环境变量配置项**  
-参考项目根目录下`.env`文件
+支持从运行目录下的`.env`文件中读取: 
 
 | 环境变量            | 说明                                                              |           默认值            |
 |-----------------|-----------------------------------------------------------------|:------------------------:|
 | OPENAI_API_KEY  | 默认openai api key，支持多个默认api key, 以 `sk-` 开头， 以空格分割      |            无             |
 | FORWARD_KEY     | 允许调用方使用该key代替openai api key，支持多个forward key, 以`fk-` 开头, 以空格分割 |      无             |
 | OPENAI_BASE_URL | 转发base url                                                      | `https://api.openai.com` |
 | LOG_CHAT        | 是否记录聊天内容                                                        |          `true`          |
@@ -240,15 +248,15 @@
 这里我们配置了FORWARD_KEY为`fk-******`, 那么后面客户端在调用时只需设置OPENAI_API_KEY为我们自定义的`fk-******` 即可。  
 这样的好处是在使用一些需要输入OPENAI_API_KEY的第三方应用时，我们可以使用`fk-******`搭配proxy使用（如下面的例子） 而无需担心OPENAI_API_KEY被泄露。
 
 **用例:**
 ```bash
 curl https://caloi.top/openai/v1/chat/completions \
   -H "Content-Type: application/json" \
-  -H "Authorization: Bearer fk-******" \
+  -H "Authorization: Bearer fk-mytoken-abcd" \
   -d '{
     "model": "gpt-3.5-turbo",
     "messages": [{"role": "user", "content": "Hello!"}]
   }'
 ```
 **Python**
 ```diff
@@ -261,8 +269,18 @@
 ```bash 
 docker run -d \
     -p 3000:3000 \
     -e OPENAI_API_KEY="fk-******" \
     -e BASE_URL="caloi.top/openai" \
     -e CODE="<your password>" \
     yidadaa/chatgpt-next-web 
-``` 
+``` 
+
+# Backer and Sponsor
+
+<a href="https://www.jetbrains.com/?from=beidongjiedeguang/openai-forward" target="_blank">
+<img src="./img/jetbrains.svg" width="100px" height="100px">
+</a>
+
+# License
+
+Openai-forward is licensed under the [MIT](https://opensource.org/license/mit/) license.
```

#### html2text {}

```diff
@@ -4,91 +4,89 @@
                                      ******
                         OpenAI API æ¥å£è½¬åæå¡
                 The fastest way to deploy openai api forwarding
  [PyPI_version] [License] [Release_(latest_by_date)] [GitHub_repo_size] [docer
                 image_size] [tests] [pypi_downloads] [codecov]
 æ¬é¡¹ç®ç¨äºè§£å³ä¸äºå°åºæ æ³ç´æ¥è®¿é®OpenAIçé®é¢ï¼å°è¯¥æå¡é¨ç½²å¨å¯ä»¥æ­£å¸¸è®¿é®openai
 apiçæå¡å¨ä¸ï¼éè¿è¯¥æå¡è½¬åOpenAIçè¯·æ±ãå³æ­å»ºååä»£çæå¡
-æµè¯è®¿é®ï¼https://caloi.top/openai/v1/chat/completions å°ç­ä»·äº https:
-//api.openai.com/v1/chat/completions æèè¯´ https://caloi.top/openai
-ç­ä»·äº https://api.openai.com # Table of Contents - [Features](#Features) -
-[åºç¨](#åºç¨) - [å®è£é¨ç½²](#å®è£é¨ç½²) - [æå¡è°ç¨]
-(#æå¡è°ç¨) - [éç½®éé¡¹](#éç½®éé¡¹) - [èå¤©æ¥å¿](#èå¤©æ¥å¿)
-- [é«çº§éç½®](#é«çº§éç½®) # Features - [x] æ¯æè½¬åOpenAIæææ¥å£
-- [x] æ¯ææµå¼ååº - [x] å®æ¶è®°å½èå¤©è®°å½
+--- æµè¯è®¿é®ï¼https://caloi.top/openai/v1/chat/completions æèè¯´
+https://caloi.top/openai ç­ä»·äº https://api.openai.com --- # ç®å½ -
+[åè½](#åè½) - [åºç¨](#åºç¨) - [å®è£é¨ç½²](#å®è£é¨ç½²) -
+[æå¡è°ç¨](#æå¡è°ç¨) - [éç½®éé¡¹](#éç½®éé¡¹) - [èå¤©æ¥å¿]
+(#èå¤©æ¥å¿) - [é«çº§éç½®](#é«çº§éç½®) # åè½ **åºç¡åè½** - [x]
+æ¯æè½¬åOpenAIæææ¥å£ - [x] æ¯ææµå¼ååº - [x]
+æ¯ææå®è½¬åè·¯ç±åç¼ - [x] dockeré¨ç½² - [x] pip å®è£é¨ç½²
+**é«çº§åè½** - [x] å®æ¶è®°å½èå¤©è®°å½
 (åæ¬æµå¼ååºçèå¤©åå®¹) - [x] æ¯æé»è®¤openai api key(å¤api key
-å¾ªç¯è°ç¨) - [x] è½¬åapi key (å¨å·²è®¾ç½®é»è®¤openai api
-keyæåµä¸ä½¿ç¨) - [x] dockeré¨ç½² - [x] æ¯ææå®è½¬åè·¯ç±åç¼ -
-[x] æ¯æè¯·æ±IPéªè¯ # åºç¨ >
-è¿éä»¥ä¸ªäººä½¿ç¨è¯¥é¡¹ç®æ­å»ºå¥½çä»£çæå¡ https://caloi.top/openai
-ä¸ºä¾ ### [caloi.top](https://caloi.top) åºäºå¼æºé¡¹ç®[ChatGPT-Next-Web]
-(https://github.com/Yidadaa/ChatGPT-Next-Web)æ­å»ºèªå·±çchatgptæå¡
-æ¿æ¢dockerå¯å¨å½ä»¤ä¸­ç
+å¾ªç¯è°ç¨) - [x] èªå®ä¹forward api key ä»£æ¿ openai api key
+(è§é«çº§éç½®) - [x] æ¯æè¯·æ±IPéªè¯(IPç½ååä¸é»åå) # åºç¨
+> è¿éä»¥ä¸ªäººä½¿ç¨è¯¥é¡¹ç®æ­å»ºå¥½çä»£çæå¡ https://caloi.top/
+openai ä¸ºä¾ ### [caloi.top](https://caloi.top) åºäºå¼æºé¡¹ç®[ChatGPT-
+Next-Web](https://github.com/Yidadaa/ChatGPT-Next-
+Web)æ­å»ºèªå·±çchatgptæå¡ æ¿æ¢dockerå¯å¨å½ä»¤ä¸­ç
 `BASE_URL`ä¸ºæä»¬èªå·±æ­å»ºçä»£çæå¡å°å ```bash docker run -d \ -
 p 3000:3000 \ -e OPENAI_API_KEY="sk-******" \ -e BASE_URL="caloi.top/openai" \
 -e CODE="" \ yidadaa/chatgpt-next-web ``` è®¿é® https://caloi.top
 ãè®¿é®å¯ç ä¸º `beidongjiedeguang` ### å¨æ¨¡åä¸­ä½¿ç¨ **JS/TS** ```diff
 import { Configuration } from "openai"; const configuration = new Configuration
 ({ + basePath: "https://caloi.top/openai/v1", apiKey: "sk-******", }); ```
 **Python** ```diff import openai + openai.api_base = "https://caloi.top/openai/
 v1" openai.api_key = "sk-******" ``` ### Image Generation (DALL-E): ```bash
 curl --location 'https://caloi.top/openai/v1/images/generations' \ --header
 'Authorization: Bearer sk-******' \ --header 'Content-Type: application/json' \
 --data '{ "prompt": "A photo of a cat", "n": 1, "size": "512x512" }' ``` #
-å®è£é¨ç½² æä¾3ç§æå¡é¨ç½²æ¹å¼,éæ©ä¸ç§å³å¯ ## pip
-pipçå®è£æ¹å¼ç®åå¨ä½¿ç¨nginxååä»£çæ¶å­å¨Bug,
-å»ºè®®ä½¿ç¨Dockeræ¹å¼é¨ç½²ã **å®è£** ```bash pip install openai-forward
-``` **è¿è¡è½¬åæå¡** å¯éè¿`--
-port`æå®ç«¯å£å·ï¼é»è®¤ä¸º`8000`ï¼å¯éè¿`--
-workers`æå®å·¥ä½è¿ç¨æ°ï¼é»è®¤ä¸º`1` ```bash openai_forward run --
-port=9999 --workers=1 ```
-æå¡å°±æ­å»ºå®æäºï¼ä½¿ç¨æ¹å¼åªéå°`https://api.openai.com`
+å®è£é¨ç½² éæ©ä¸ç§å³å¯ ## pip **å®è£** ```bash pip install openai-
+forward ``` **è¿è¡è½¬åæå¡** å¯éè¿`--
+port`æå®ç«¯å£å·ï¼é»è®¤ä¸º`8000` ```bash openai_forward run --port=9999
+``` æå¡å°±æ­å»ºå®æäºï¼ä½¿ç¨æ¹å¼åªéå°`https://api.openai.com`
 æ¿æ¢ä¸ºæå¡æå¨ç«¯å£`http://{ip}:{port}` å³å¯ã å½ç¶ä¹å¯ä»¥å°
-OPENAI_API_KEY ä½ä¸ºç¯å¢åéä¼ å¥ä½ä¸ºé»è®¤api keyï¼
+OPENAI_API_KEY ä½ä¸ºç¯å¢åéæ`--api_key`åæ°ä¼ å¥ä½ä¸ºé»è®¤api
+keyï¼
 è¿æ ·å®¢æ·ç«¯å¨è¯·æ±ç¸å³è·¯ç±æ¶å¯ä»¥æ éå¨Headerä¸­ä¼ å¥Authorizationã
-å¸¦é»è®¤api keyçå¯å¨æ¹å¼ï¼ ```bash OPENAI_API_KEY="sk-xxx"
-openai_forward run --port=9999 --workers=1 ``` æ³¨: å¦ææ¢å­å¨é»è®¤api
+å¸¦é»è®¤api keyçå¯å¨æ¹å¼ï¼ ```bash openai_forward run --port=9999 --
+api_key="sk-******" ``` æ³¨: å¦ææ¢å­å¨é»è®¤api
 keyåå¨è¯·æ±å¤´ä¸­ä¼ å¥äºapi keyï¼åä»¥è¯·æ±å¤´ä¸­çapi
-keyä¼è¦çé»è®¤api key. ## Docker (æ¨è) ```bash docker run --
-name="openai-forward" -d -p 9999:8000 beidongjiedeguang/openai-forward:latest
-``` å°æ å°å®¿ä¸»æºç9999ç«¯å£ï¼éè¿`http://{ip}:9999`è®¿é®æå¡ã
+keyä¼è¦çé»è®¤api key. ## Docker (æ¨è) ```bash docker run -d -p 9999:
+8000 beidongjiedeguang/openai-forward:latest ```
+å°æ å°å®¿ä¸»æºç9999ç«¯å£ï¼éè¿`http://{ip}:9999`è®¿é®æå¡ã
 æ³¨ï¼åæ ·å¯ä»¥å¨å¯å¨å½ä»¤ä¸­éè¿-
 eä¼ å¥ç¯å¢åéOPENAI_API_KEY=sk-xxxä½ä¸ºé»è®¤api key ## æºç é¨ç½²
 ```bash git clone https://github.com/beidongjiedeguang/openai-forward.git --
-depth=1 cd openai-forward ``` **ä½¿ç¨ docker** ```bash docker-compose up ```
-**æä½¿ç¨pip** ```bash pip install -e . openai-forward run ``` # æå¡è°ç¨
+depth=1 cd openai-forward ``` **Docker** ```bash docker-compose up ``` **pip**
+```bash pip install -e . openai-forward run ``` # æå¡è°ç¨
 æ¿æ¢openaiçapiå°åä¸ºè¯¥æå¡çå°åå³å¯ï¼å¦ï¼ ```bash https://
 api.openai.com/v1/chat/completions ``` æ¿æ¢ä¸º ```bash http://{ip}:{port}/v1/
 chat/completions ``` # éç½®éé¡¹ **`openai-forward run`åæ°éç½®é¡¹** |
 éç½®é¡¹ | è¯´æ | é»è®¤å¼ | |-----------| --- | :---: | | --port |
 æå¡ç«¯å£å· | 8000 | | --workers | å·¥ä½è¿ç¨æ° | 1 |
-**ç¯å¢åééç½®é¡¹** åèé¡¹ç®æ ¹ç®å½ä¸`.env`æä»¶ | ç¯å¢åé |
-è¯´æ | é»è®¤å¼ | |-----------------|---------------------------------------
---------------------------|:------------------------:| | OPENAI_API_KEY |
-é»è®¤openai api keyï¼æ¯æå¤ä¸ªé»è®¤api key, ä»¥ `sk-` å¼å¤´ï¼
-ä»¥ç©ºæ ¼åå² | æ  | | FORWARD_KEY | åè®¸è°ç¨æ¹ä½¿ç¨è¯¥keyä»£æ¿openai
-api keyï¼æ¯æå¤ä¸ªforward key, ä»¥`fk-` å¼å¤´, ä»¥ç©ºæ ¼åå² | æ  | |
-OPENAI_BASE_URL | è½¬åbase url | `https://api.openai.com` | | LOG_CHAT |
-æ¯å¦è®°å½èå¤©åå®¹ | `true` | | ROUTE_PREFIX | è·¯ç±åç¼ | æ  | |
-IP_WHITELIST | ipç½åå, ç©ºæ ¼åå¼ | æ  | | IP_BLACKLIST | ipé»åå,
-ç©ºæ ¼åå¼ | æ  | # èå¤©æ¥å¿ ä¿å­è·¯å¾å¨å½åç®å½ä¸ç`Log/
-`è·¯å¾ä¸­ã èå¤©æ¥å¿ä»¥ `chat_`å¼å¤´,
-é»è®¤æ¯5è½®å¯¹è¯åå¥ä¸æ¬¡æä»¶ è®°å½æ ¼å¼ä¸º ```text {'host': xxx,
-'model': xxx, 'message': [{'user': xxx}, {'assistant': xxx}]} {'assistant':
-xxx} {'host': ...} {'assistant': ...} ... ``` # é«çº§éç½®
+**ç¯å¢åééç½®é¡¹** æ¯æä»è¿è¡ç®å½ä¸ç`.env`æä»¶ä¸­è¯»å: |
+ç¯å¢åé | è¯´æ | é»è®¤å¼ | |-----------------|------------------------
+-----------------------------------------|:------------------------:| |
+OPENAI_API_KEY | é»è®¤openai api keyï¼æ¯æå¤ä¸ªé»è®¤api key, ä»¥ `sk-
+` å¼å¤´ï¼ ä»¥ç©ºæ ¼åå² | æ  | | FORWARD_KEY |
+åè®¸è°ç¨æ¹ä½¿ç¨è¯¥keyä»£æ¿openai api keyï¼æ¯æå¤ä¸ªforward key,
+ä»¥`fk-` å¼å¤´, ä»¥ç©ºæ ¼åå² | æ  | | OPENAI_BASE_URL | è½¬åbase url |
+`https://api.openai.com` | | LOG_CHAT | æ¯å¦è®°å½èå¤©åå®¹ | `true` | |
+ROUTE_PREFIX | è·¯ç±åç¼ | æ  | | IP_WHITELIST | ipç½åå, ç©ºæ ¼åå¼
+| æ  | | IP_BLACKLIST | ipé»åå, ç©ºæ ¼åå¼ | æ  | # èå¤©æ¥å¿
+ä¿å­è·¯å¾å¨å½åç®å½ä¸ç`Log/`è·¯å¾ä¸­ã èå¤©æ¥å¿ä»¥
+`chat_`å¼å¤´, é»è®¤æ¯5è½®å¯¹è¯åå¥ä¸æ¬¡æä»¶ è®°å½æ ¼å¼ä¸º ```text
+{'host': xxx, 'model': xxx, 'message': [{'user': xxx}, {'assistant': xxx}]}
+{'assistant': xxx} {'host': ...} {'assistant': ...} ... ``` # é«çº§éç½®
 **è®¾ç½®api_keyä¸ºèªå·±è®¾ç½®çforward key** éè¦éç½® OPENAI_API_KEY å
 FORWARD_KEY, ä¾å¦ ```bash OPENAI_API_KEY=sk-******* FORWARD_KEY=fk-****** #
 è¿éfk-tokenç±æä»¬èªå·±å®ä¹ ``` è¿éæä»¬éç½®äºFORWARD_KEYä¸º`fk-
 ******`,
 é£ä¹åé¢å®¢æ·ç«¯å¨è°ç¨æ¶åªéè®¾ç½®OPENAI_API_KEYä¸ºæä»¬èªå®ä¹ç`fk-
 ******` å³å¯ã
 è¿æ ·çå¥½å¤æ¯å¨ä½¿ç¨ä¸äºéè¦è¾å¥OPENAI_API_KEYçç¬¬ä¸æ¹åºç¨æ¶ï¼æä»¬å¯ä»¥ä½¿ç¨`fk-
 ******`æ­éproxyä½¿ç¨ï¼å¦ä¸é¢çä¾å­ï¼
 èæ éæå¿OPENAI_API_KEYè¢«æ³é²ã **ç¨ä¾:** ```bash curl https://
 caloi.top/openai/v1/chat/completions \ -H "Content-Type: application/json" \ -
-H "Authorization: Bearer fk-******" \ -d '{ "model": "gpt-3.5-turbo",
+H "Authorization: Bearer fk-mytoken-abcd" \ -d '{ "model": "gpt-3.5-turbo",
 "messages": [{"role": "user", "content": "Hello!"}] }' ``` **Python** ```diff
 import openai + openai.api_base = "https://caloi.top/openai/v1" -
 openai.api_key = "sk-******" + openai.api_key = "fk-******" ``` **Web
 application** ```bash docker run -d \ -p 3000:3000 \ -e OPENAI_API_KEY="fk-
 ******" \ -e BASE_URL="caloi.top/openai" \ -e CODE="" \ yidadaa/chatgpt-next-
-web ```
+web ``` # Backer and Sponsor [./img/jetbrains.svg] # License Openai-forward is
+licensed under the [MIT](https://opensource.org/license/mit/) license.
```

### Comparing `openai_forward-0.1.8/pyproject.toml` & `openai_forward-0.1.9/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -15,21 +15,22 @@
     "Development Status :: 5 - Production/Stable",
     "Operating System :: OS Independent",
     "Programming Language :: Python :: 3"
 ]
 
 dependencies = [
     "loguru",
-    "sparrow-python>=0.1.2",
+    "sparrow-python>=0.1.3",
     "fastapi",
     "uvicorn",
     "orjson",
     "python-dotenv",
     "httpx",
-    "pytz"
+    "pytz",
+    "chardet",
 ]
 
 dynamic = ["version"]
 
 [project.urls]
 Homepage = "https://github.com/beidongjiedeguang/openai-forward"
 Documentation = "https://github.com/beidongjiedeguang/openai-forward#openai-forward"
```

### Comparing `openai_forward-0.1.8/PKG-INFO` & `openai_forward-0.1.9/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,29 +1,30 @@
 Metadata-Version: 2.1
 Name: openai_forward
-Version: 0.1.8
+Version: 0.1.9
 Summary: 🚀 Openai api forward · OpenAI 接口转发服务 · stream forwarding
 Project-URL: Homepage, https://github.com/beidongjiedeguang/openai-forward
 Project-URL: Documentation, https://github.com/beidongjiedeguang/openai-forward#openai-forward
 Project-URL: Issues, https://github.com/beidongjiedeguang/openai-forward/issues
 Project-URL: Source, https://github.com/beidongjiedeguang/openai-forward
 Author-email: kunyuan <beidongjiedeguang@gmail.com>
 License-File: LICENSE
 Keywords: chatgpt,fastapi,forward,openai,openai-api,openai-proxy,python,streaming-api
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.6
+Requires-Dist: chardet
 Requires-Dist: fastapi
 Requires-Dist: httpx
 Requires-Dist: loguru
 Requires-Dist: orjson
 Requires-Dist: python-dotenv
 Requires-Dist: pytz
-Requires-Dist: sparrow-python>=0.1.2
+Requires-Dist: sparrow-python>=0.1.3
 Requires-Dist: uvicorn
 Provides-Extra: bard
 Requires-Dist: googlebard; extra == 'bard'
 Provides-Extra: chatgpt
 Requires-Dist: revchatgpt; extra == 'chatgpt'
 Provides-Extra: edge
 Requires-Dist: edgegpt; extra == 'edge'
@@ -68,37 +69,45 @@
     </a>
 </p>
 
 
 
 本项目用于解决一些地区无法直接访问OpenAI的问题，将该服务部署在可以正常访问openai
 api的服务器上，通过该服务转发OpenAI的请求。即搭建反向代理服务  
-测试访问：https://caloi.top/openai/v1/chat/completions 将等价于 https://api.openai.com/v1/chat/completions  
+
+---
+
+测试访问：https://caloi.top/openai/v1/chat/completions  
 或者说 https://caloi.top/openai 等价于 https://api.openai.com
 
-# Table of Contents
+---
 
-- [Features](#Features)
+# 目录
+
+- [功能](#功能)
 - [应用](#应用)
 - [安装部署](#安装部署)
 - [服务调用](#服务调用)
 - [配置选项](#配置选项)
 - [聊天日志](#聊天日志)
 - [高级配置](#高级配置)
 
-# Features
-
+# 功能
+**基础功能**  
 - [x] 支持转发OpenAI所有接口
 - [x] 支持流式响应
+- [x] 支持指定转发路由前缀
+- [x] docker部署
+- [x] pip 安装部署
+
+**高级功能**  
 - [x] 实时记录聊天记录(包括流式响应的聊天内容)
 - [x] 支持默认openai api key(多api key 循环调用)
-- [x] 转发api key (在已设置默认openai api key情况下使用)
-- [x] docker部署
-- [x] 支持指定转发路由前缀
-- [x] 支持请求IP验证
+- [x] 自定义forward api key 代替 openai api key (见高级配置)
+- [x] 支持请求IP验证(IP白名单与黑名单)
 
 # 应用
 
 > 这里以个人使用该项目搭建好的代理服务 https://caloi.top/openai 为例
 
 ### [caloi.top](https://caloi.top)
 
@@ -148,65 +157,65 @@
     "n": 1,
     "size": "512x512"
 }'
 ```
 
 # 安装部署
 
-提供3种服务部署方式,选择一种即可
+选择一种即可
 
 ## pip
-pip的安装方式目前在使用nginx反向代理时存在Bug, 建议使用Docker方式部署。  
+
 **安装**
 
 ```bash
 pip install openai-forward
 ```
 
 **运行转发服务**  
-可通过`--port`指定端口号，默认为`8000`，可通过`--workers`指定工作进程数，默认为`1`
+可通过`--port`指定端口号，默认为`8000`
 
 ```bash
-openai_forward run --port=9999 --workers=1
+openai_forward run --port=9999 
 ```
 
 服务就搭建完成了，使用方式只需将`https://api.openai.com` 替换为服务所在端口`http://{ip}:{port}` 即可。
 
-当然也可以将 OPENAI_API_KEY 作为环境变量传入作为默认api key， 这样客户端在请求相关路由时可以无需在Header中传入Authorization。
+当然也可以将 OPENAI_API_KEY 作为环境变量或`--api_key`参数传入作为默认api key， 这样客户端在请求相关路由时可以无需在Header中传入Authorization。
 带默认api key的启动方式：
 
 ```bash
-OPENAI_API_KEY="sk-xxx" openai_forward run --port=9999 --workers=1
+openai_forward run --port=9999 --api_key="sk-******"
 ```
 
 注: 如果既存在默认api key又在请求头中传入了api key，则以请求头中的api key会覆盖默认api key.
 
 ## Docker (推荐)
 
 ```bash
-docker run --name="openai-forward" -d -p 9999:8000 beidongjiedeguang/openai-forward:latest 
+docker run -d -p 9999:8000 beidongjiedeguang/openai-forward:latest 
 ```
 
 将映射宿主机的9999端口，通过`http://{ip}:9999`访问服务。  
 注：同样可以在启动命令中通过-e传入环境变量OPENAI_API_KEY=sk-xxx作为默认api key
 
 ## 源码部署
 
 ```bash
 git clone https://github.com/beidongjiedeguang/openai-forward.git --depth=1
 cd openai-forward
 ```
 
-**使用 docker**
+**Docker**
 
 ```bash
 docker-compose up
 ```
 
-**或使用pip**
+**pip**
 
 ```bash
 pip install -e .
 openai-forward run 
 ```
 
 # 服务调用
@@ -229,15 +238,15 @@
 
 | 配置项       | 说明 | 默认值 |
 |-----------| --- | :---: |
 | --port    | 服务端口号 | 8000 |
 | --workers | 工作进程数 | 1 |
 
 **环境变量配置项**  
-参考项目根目录下`.env`文件
+支持从运行目录下的`.env`文件中读取: 
 
 | 环境变量            | 说明                                                              |           默认值            |
 |-----------------|-----------------------------------------------------------------|:------------------------:|
 | OPENAI_API_KEY  | 默认openai api key，支持多个默认api key, 以 `sk-` 开头， 以空格分割      |            无             |
 | FORWARD_KEY     | 允许调用方使用该key代替openai api key，支持多个forward key, 以`fk-` 开头, 以空格分割 |      无             |
 | OPENAI_BASE_URL | 转发base url                                                      | `https://api.openai.com` |
 | LOG_CHAT        | 是否记录聊天内容                                                        |          `true`          |
@@ -273,15 +282,15 @@
 这里我们配置了FORWARD_KEY为`fk-******`, 那么后面客户端在调用时只需设置OPENAI_API_KEY为我们自定义的`fk-******` 即可。  
 这样的好处是在使用一些需要输入OPENAI_API_KEY的第三方应用时，我们可以使用`fk-******`搭配proxy使用（如下面的例子） 而无需担心OPENAI_API_KEY被泄露。
 
 **用例:**
 ```bash
 curl https://caloi.top/openai/v1/chat/completions \
   -H "Content-Type: application/json" \
-  -H "Authorization: Bearer fk-******" \
+  -H "Authorization: Bearer fk-mytoken-abcd" \
   -d '{
     "model": "gpt-3.5-turbo",
     "messages": [{"role": "user", "content": "Hello!"}]
   }'
 ```
 **Python**
 ```diff
@@ -294,8 +303,18 @@
 ```bash 
 docker run -d \
     -p 3000:3000 \
     -e OPENAI_API_KEY="fk-******" \
     -e BASE_URL="caloi.top/openai" \
     -e CODE="<your password>" \
     yidadaa/chatgpt-next-web 
-``` 
+``` 
+
+# Backer and Sponsor
+
+<a href="https://www.jetbrains.com/?from=beidongjiedeguang/openai-forward" target="_blank">
+<img src="./img/jetbrains.svg" width="100px" height="100px">
+</a>
+
+# License
+
+Openai-forward is licensed under the [MIT](https://opensource.org/license/mit/) license.
```

#### html2text {}

```diff
@@ -1,112 +1,110 @@
-Metadata-Version: 2.1 Name: openai_forward Version: 0.1.8 Summary: ð Openai
+Metadata-Version: 2.1 Name: openai_forward Version: 0.1.9 Summary: ð Openai
 api forward Â· OpenAI æ¥å£è½¬åæå¡ Â· stream forwarding Project-URL:
 Homepage, https://github.com/beidongjiedeguang/openai-forward Project-URL:
 Documentation, https://github.com/beidongjiedeguang/openai-forward#openai-
 forward Project-URL: Issues, https://github.com/beidongjiedeguang/openai-
 forward/issues Project-URL: Source, https://github.com/beidongjiedeguang/
 openai-forward Author-email: kunyuan
 gmail.com> License-File: LICENSE Keywords:
 chatgpt,fastapi,forward,openai,openai-api,openai-proxy,python,streaming-api
 Classifier: Development Status :: 5 - Production/Stable Classifier: Operating
 System :: OS Independent Classifier: Programming Language :: Python :: 3
-Requires-Python: >=3.6 Requires-Dist: fastapi Requires-Dist: httpx Requires-
-Dist: loguru Requires-Dist: orjson Requires-Dist: python-dotenv Requires-Dist:
-pytz Requires-Dist: sparrow-python>=0.1.2 Requires-Dist: uvicorn Provides-
-Extra: bard Requires-Dist: googlebard; extra == 'bard' Provides-Extra: chatgpt
-Requires-Dist: revchatgpt; extra == 'chatgpt' Provides-Extra: edge Requires-
-Dist: edgegpt; extra == 'edge' Provides-Extra: ssl Requires-Dist: certbot;
-extra == 'ssl' Description-Content-Type: text/markdown **ä¸­æ** |
-[**English**](./README_EN.md)
+Requires-Python: >=3.6 Requires-Dist: chardet Requires-Dist: fastapi Requires-
+Dist: httpx Requires-Dist: loguru Requires-Dist: orjson Requires-Dist: python-
+dotenv Requires-Dist: pytz Requires-Dist: sparrow-python>=0.1.3 Requires-Dist:
+uvicorn Provides-Extra: bard Requires-Dist: googlebard; extra == 'bard'
+Provides-Extra: chatgpt Requires-Dist: revchatgpt; extra == 'chatgpt' Provides-
+Extra: edge Requires-Dist: edgegpt; extra == 'edge' Provides-Extra: ssl
+Requires-Dist: certbot; extra == 'ssl' Description-Content-Type: text/markdown
+**ä¸­æ** | [**English**](./README_EN.md)
                                     ******
                                 OpenAI Forward
                                      ******
                         OpenAI API æ¥å£è½¬åæå¡
                 The fastest way to deploy openai api forwarding
  [PyPI_version] [License] [Release_(latest_by_date)] [GitHub_repo_size] [docer
                 image_size] [tests] [pypi_downloads] [codecov]
 æ¬é¡¹ç®ç¨äºè§£å³ä¸äºå°åºæ æ³ç´æ¥è®¿é®OpenAIçé®é¢ï¼å°è¯¥æå¡é¨ç½²å¨å¯ä»¥æ­£å¸¸è®¿é®openai
 apiçæå¡å¨ä¸ï¼éè¿è¯¥æå¡è½¬åOpenAIçè¯·æ±ãå³æ­å»ºååä»£çæå¡
-æµè¯è®¿é®ï¼https://caloi.top/openai/v1/chat/completions å°ç­ä»·äº https:
-//api.openai.com/v1/chat/completions æèè¯´ https://caloi.top/openai
-ç­ä»·äº https://api.openai.com # Table of Contents - [Features](#Features) -
-[åºç¨](#åºç¨) - [å®è£é¨ç½²](#å®è£é¨ç½²) - [æå¡è°ç¨]
-(#æå¡è°ç¨) - [éç½®éé¡¹](#éç½®éé¡¹) - [èå¤©æ¥å¿](#èå¤©æ¥å¿)
-- [é«çº§éç½®](#é«çº§éç½®) # Features - [x] æ¯æè½¬åOpenAIæææ¥å£
-- [x] æ¯ææµå¼ååº - [x] å®æ¶è®°å½èå¤©è®°å½
+--- æµè¯è®¿é®ï¼https://caloi.top/openai/v1/chat/completions æèè¯´
+https://caloi.top/openai ç­ä»·äº https://api.openai.com --- # ç®å½ -
+[åè½](#åè½) - [åºç¨](#åºç¨) - [å®è£é¨ç½²](#å®è£é¨ç½²) -
+[æå¡è°ç¨](#æå¡è°ç¨) - [éç½®éé¡¹](#éç½®éé¡¹) - [èå¤©æ¥å¿]
+(#èå¤©æ¥å¿) - [é«çº§éç½®](#é«çº§éç½®) # åè½ **åºç¡åè½** - [x]
+æ¯æè½¬åOpenAIæææ¥å£ - [x] æ¯ææµå¼ååº - [x]
+æ¯ææå®è½¬åè·¯ç±åç¼ - [x] dockeré¨ç½² - [x] pip å®è£é¨ç½²
+**é«çº§åè½** - [x] å®æ¶è®°å½èå¤©è®°å½
 (åæ¬æµå¼ååºçèå¤©åå®¹) - [x] æ¯æé»è®¤openai api key(å¤api key
-å¾ªç¯è°ç¨) - [x] è½¬åapi key (å¨å·²è®¾ç½®é»è®¤openai api
-keyæåµä¸ä½¿ç¨) - [x] dockeré¨ç½² - [x] æ¯ææå®è½¬åè·¯ç±åç¼ -
-[x] æ¯æè¯·æ±IPéªè¯ # åºç¨ >
-è¿éä»¥ä¸ªäººä½¿ç¨è¯¥é¡¹ç®æ­å»ºå¥½çä»£çæå¡ https://caloi.top/openai
-ä¸ºä¾ ### [caloi.top](https://caloi.top) åºäºå¼æºé¡¹ç®[ChatGPT-Next-Web]
-(https://github.com/Yidadaa/ChatGPT-Next-Web)æ­å»ºèªå·±çchatgptæå¡
-æ¿æ¢dockerå¯å¨å½ä»¤ä¸­ç
+å¾ªç¯è°ç¨) - [x] èªå®ä¹forward api key ä»£æ¿ openai api key
+(è§é«çº§éç½®) - [x] æ¯æè¯·æ±IPéªè¯(IPç½ååä¸é»åå) # åºç¨
+> è¿éä»¥ä¸ªäººä½¿ç¨è¯¥é¡¹ç®æ­å»ºå¥½çä»£çæå¡ https://caloi.top/
+openai ä¸ºä¾ ### [caloi.top](https://caloi.top) åºäºå¼æºé¡¹ç®[ChatGPT-
+Next-Web](https://github.com/Yidadaa/ChatGPT-Next-
+Web)æ­å»ºèªå·±çchatgptæå¡ æ¿æ¢dockerå¯å¨å½ä»¤ä¸­ç
 `BASE_URL`ä¸ºæä»¬èªå·±æ­å»ºçä»£çæå¡å°å ```bash docker run -d \ -
 p 3000:3000 \ -e OPENAI_API_KEY="sk-******" \ -e BASE_URL="caloi.top/openai" \
 -e CODE="" \ yidadaa/chatgpt-next-web ``` è®¿é® https://caloi.top
 ãè®¿é®å¯ç ä¸º `beidongjiedeguang` ### å¨æ¨¡åä¸­ä½¿ç¨ **JS/TS** ```diff
 import { Configuration } from "openai"; const configuration = new Configuration
 ({ + basePath: "https://caloi.top/openai/v1", apiKey: "sk-******", }); ```
 **Python** ```diff import openai + openai.api_base = "https://caloi.top/openai/
 v1" openai.api_key = "sk-******" ``` ### Image Generation (DALL-E): ```bash
 curl --location 'https://caloi.top/openai/v1/images/generations' \ --header
 'Authorization: Bearer sk-******' \ --header 'Content-Type: application/json' \
 --data '{ "prompt": "A photo of a cat", "n": 1, "size": "512x512" }' ``` #
-å®è£é¨ç½² æä¾3ç§æå¡é¨ç½²æ¹å¼,éæ©ä¸ç§å³å¯ ## pip
-pipçå®è£æ¹å¼ç®åå¨ä½¿ç¨nginxååä»£çæ¶å­å¨Bug,
-å»ºè®®ä½¿ç¨Dockeræ¹å¼é¨ç½²ã **å®è£** ```bash pip install openai-forward
-``` **è¿è¡è½¬åæå¡** å¯éè¿`--
-port`æå®ç«¯å£å·ï¼é»è®¤ä¸º`8000`ï¼å¯éè¿`--
-workers`æå®å·¥ä½è¿ç¨æ°ï¼é»è®¤ä¸º`1` ```bash openai_forward run --
-port=9999 --workers=1 ```
-æå¡å°±æ­å»ºå®æäºï¼ä½¿ç¨æ¹å¼åªéå°`https://api.openai.com`
+å®è£é¨ç½² éæ©ä¸ç§å³å¯ ## pip **å®è£** ```bash pip install openai-
+forward ``` **è¿è¡è½¬åæå¡** å¯éè¿`--
+port`æå®ç«¯å£å·ï¼é»è®¤ä¸º`8000` ```bash openai_forward run --port=9999
+``` æå¡å°±æ­å»ºå®æäºï¼ä½¿ç¨æ¹å¼åªéå°`https://api.openai.com`
 æ¿æ¢ä¸ºæå¡æå¨ç«¯å£`http://{ip}:{port}` å³å¯ã å½ç¶ä¹å¯ä»¥å°
-OPENAI_API_KEY ä½ä¸ºç¯å¢åéä¼ å¥ä½ä¸ºé»è®¤api keyï¼
+OPENAI_API_KEY ä½ä¸ºç¯å¢åéæ`--api_key`åæ°ä¼ å¥ä½ä¸ºé»è®¤api
+keyï¼
 è¿æ ·å®¢æ·ç«¯å¨è¯·æ±ç¸å³è·¯ç±æ¶å¯ä»¥æ éå¨Headerä¸­ä¼ å¥Authorizationã
-å¸¦é»è®¤api keyçå¯å¨æ¹å¼ï¼ ```bash OPENAI_API_KEY="sk-xxx"
-openai_forward run --port=9999 --workers=1 ``` æ³¨: å¦ææ¢å­å¨é»è®¤api
+å¸¦é»è®¤api keyçå¯å¨æ¹å¼ï¼ ```bash openai_forward run --port=9999 --
+api_key="sk-******" ``` æ³¨: å¦ææ¢å­å¨é»è®¤api
 keyåå¨è¯·æ±å¤´ä¸­ä¼ å¥äºapi keyï¼åä»¥è¯·æ±å¤´ä¸­çapi
-keyä¼è¦çé»è®¤api key. ## Docker (æ¨è) ```bash docker run --
-name="openai-forward" -d -p 9999:8000 beidongjiedeguang/openai-forward:latest
-``` å°æ å°å®¿ä¸»æºç9999ç«¯å£ï¼éè¿`http://{ip}:9999`è®¿é®æå¡ã
+keyä¼è¦çé»è®¤api key. ## Docker (æ¨è) ```bash docker run -d -p 9999:
+8000 beidongjiedeguang/openai-forward:latest ```
+å°æ å°å®¿ä¸»æºç9999ç«¯å£ï¼éè¿`http://{ip}:9999`è®¿é®æå¡ã
 æ³¨ï¼åæ ·å¯ä»¥å¨å¯å¨å½ä»¤ä¸­éè¿-
 eä¼ å¥ç¯å¢åéOPENAI_API_KEY=sk-xxxä½ä¸ºé»è®¤api key ## æºç é¨ç½²
 ```bash git clone https://github.com/beidongjiedeguang/openai-forward.git --
-depth=1 cd openai-forward ``` **ä½¿ç¨ docker** ```bash docker-compose up ```
-**æä½¿ç¨pip** ```bash pip install -e . openai-forward run ``` # æå¡è°ç¨
+depth=1 cd openai-forward ``` **Docker** ```bash docker-compose up ``` **pip**
+```bash pip install -e . openai-forward run ``` # æå¡è°ç¨
 æ¿æ¢openaiçapiå°åä¸ºè¯¥æå¡çå°åå³å¯ï¼å¦ï¼ ```bash https://
 api.openai.com/v1/chat/completions ``` æ¿æ¢ä¸º ```bash http://{ip}:{port}/v1/
 chat/completions ``` # éç½®éé¡¹ **`openai-forward run`åæ°éç½®é¡¹** |
 éç½®é¡¹ | è¯´æ | é»è®¤å¼ | |-----------| --- | :---: | | --port |
 æå¡ç«¯å£å· | 8000 | | --workers | å·¥ä½è¿ç¨æ° | 1 |
-**ç¯å¢åééç½®é¡¹** åèé¡¹ç®æ ¹ç®å½ä¸`.env`æä»¶ | ç¯å¢åé |
-è¯´æ | é»è®¤å¼ | |-----------------|---------------------------------------
---------------------------|:------------------------:| | OPENAI_API_KEY |
-é»è®¤openai api keyï¼æ¯æå¤ä¸ªé»è®¤api key, ä»¥ `sk-` å¼å¤´ï¼
-ä»¥ç©ºæ ¼åå² | æ  | | FORWARD_KEY | åè®¸è°ç¨æ¹ä½¿ç¨è¯¥keyä»£æ¿openai
-api keyï¼æ¯æå¤ä¸ªforward key, ä»¥`fk-` å¼å¤´, ä»¥ç©ºæ ¼åå² | æ  | |
-OPENAI_BASE_URL | è½¬åbase url | `https://api.openai.com` | | LOG_CHAT |
-æ¯å¦è®°å½èå¤©åå®¹ | `true` | | ROUTE_PREFIX | è·¯ç±åç¼ | æ  | |
-IP_WHITELIST | ipç½åå, ç©ºæ ¼åå¼ | æ  | | IP_BLACKLIST | ipé»åå,
-ç©ºæ ¼åå¼ | æ  | # èå¤©æ¥å¿ ä¿å­è·¯å¾å¨å½åç®å½ä¸ç`Log/
-`è·¯å¾ä¸­ã èå¤©æ¥å¿ä»¥ `chat_`å¼å¤´,
-é»è®¤æ¯5è½®å¯¹è¯åå¥ä¸æ¬¡æä»¶ è®°å½æ ¼å¼ä¸º ```text {'host': xxx,
-'model': xxx, 'message': [{'user': xxx}, {'assistant': xxx}]} {'assistant':
-xxx} {'host': ...} {'assistant': ...} ... ``` # é«çº§éç½®
+**ç¯å¢åééç½®é¡¹** æ¯æä»è¿è¡ç®å½ä¸ç`.env`æä»¶ä¸­è¯»å: |
+ç¯å¢åé | è¯´æ | é»è®¤å¼ | |-----------------|------------------------
+-----------------------------------------|:------------------------:| |
+OPENAI_API_KEY | é»è®¤openai api keyï¼æ¯æå¤ä¸ªé»è®¤api key, ä»¥ `sk-
+` å¼å¤´ï¼ ä»¥ç©ºæ ¼åå² | æ  | | FORWARD_KEY |
+åè®¸è°ç¨æ¹ä½¿ç¨è¯¥keyä»£æ¿openai api keyï¼æ¯æå¤ä¸ªforward key,
+ä»¥`fk-` å¼å¤´, ä»¥ç©ºæ ¼åå² | æ  | | OPENAI_BASE_URL | è½¬åbase url |
+`https://api.openai.com` | | LOG_CHAT | æ¯å¦è®°å½èå¤©åå®¹ | `true` | |
+ROUTE_PREFIX | è·¯ç±åç¼ | æ  | | IP_WHITELIST | ipç½åå, ç©ºæ ¼åå¼
+| æ  | | IP_BLACKLIST | ipé»åå, ç©ºæ ¼åå¼ | æ  | # èå¤©æ¥å¿
+ä¿å­è·¯å¾å¨å½åç®å½ä¸ç`Log/`è·¯å¾ä¸­ã èå¤©æ¥å¿ä»¥
+`chat_`å¼å¤´, é»è®¤æ¯5è½®å¯¹è¯åå¥ä¸æ¬¡æä»¶ è®°å½æ ¼å¼ä¸º ```text
+{'host': xxx, 'model': xxx, 'message': [{'user': xxx}, {'assistant': xxx}]}
+{'assistant': xxx} {'host': ...} {'assistant': ...} ... ``` # é«çº§éç½®
 **è®¾ç½®api_keyä¸ºèªå·±è®¾ç½®çforward key** éè¦éç½® OPENAI_API_KEY å
 FORWARD_KEY, ä¾å¦ ```bash OPENAI_API_KEY=sk-******* FORWARD_KEY=fk-****** #
 è¿éfk-tokenç±æä»¬èªå·±å®ä¹ ``` è¿éæä»¬éç½®äºFORWARD_KEYä¸º`fk-
 ******`,
 é£ä¹åé¢å®¢æ·ç«¯å¨è°ç¨æ¶åªéè®¾ç½®OPENAI_API_KEYä¸ºæä»¬èªå®ä¹ç`fk-
 ******` å³å¯ã
 è¿æ ·çå¥½å¤æ¯å¨ä½¿ç¨ä¸äºéè¦è¾å¥OPENAI_API_KEYçç¬¬ä¸æ¹åºç¨æ¶ï¼æä»¬å¯ä»¥ä½¿ç¨`fk-
 ******`æ­éproxyä½¿ç¨ï¼å¦ä¸é¢çä¾å­ï¼
 èæ éæå¿OPENAI_API_KEYè¢«æ³é²ã **ç¨ä¾:** ```bash curl https://
 caloi.top/openai/v1/chat/completions \ -H "Content-Type: application/json" \ -
-H "Authorization: Bearer fk-******" \ -d '{ "model": "gpt-3.5-turbo",
+H "Authorization: Bearer fk-mytoken-abcd" \ -d '{ "model": "gpt-3.5-turbo",
 "messages": [{"role": "user", "content": "Hello!"}] }' ``` **Python** ```diff
 import openai + openai.api_base = "https://caloi.top/openai/v1" -
 openai.api_key = "sk-******" + openai.api_key = "fk-******" ``` **Web
 application** ```bash docker run -d \ -p 3000:3000 \ -e OPENAI_API_KEY="fk-
 ******" \ -e BASE_URL="caloi.top/openai" \ -e CODE="" \ yidadaa/chatgpt-next-
-web ```
+web ``` # Backer and Sponsor [./img/jetbrains.svg] # License Openai-forward is
+licensed under the [MIT](https://opensource.org/license/mit/) license.
```

