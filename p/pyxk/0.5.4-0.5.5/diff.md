# Comparing `tmp/pyxk-0.5.4.tar.gz` & `tmp/pyxk-0.5.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyxk-0.5.4.tar", last modified: Tue May  9 09:35:36 2023, max compression
+gzip compressed data, was "pyxk-0.5.5.tar", last modified: Sat May 13 09:33:26 2023, max compression
```

## Comparing `pyxk-0.5.4.tar` & `pyxk-0.5.5.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.212000 pyxk-0.5.4/
--rw-rw----   0 root         (0) everybody  (9997)     1079 2022-09-01 11:31:05.000000 pyxk-0.5.4/LICENSE
--rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-09 09:35:36.212000 pyxk-0.5.4/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)        4 2023-03-31 15:33:16.000000 pyxk-0.5.4/README.md
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.192000 pyxk-0.5.4/pyxk/
--rw-rw----   0 root         (0) everybody  (9997)       53 2023-05-08 09:38:07.000000 pyxk-0.5.4/pyxk/__init__.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.202000 pyxk-0.5.4/pyxk/aclient/
--rw-rw----   0 root         (0) everybody  (9997)       90 2023-05-08 07:54:13.000000 pyxk-0.5.4/pyxk/aclient/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)    15040 2023-05-09 09:06:43.000000 pyxk-0.5.4/pyxk/aclient/client.py
--rw-rw----   0 root         (0) everybody  (9997)      699 2023-04-30 15:43:19.000000 pyxk-0.5.4/pyxk/aclient/typedef.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.202000 pyxk-0.5.4/pyxk/aes/
--rw-rw----   0 root         (0) everybody  (9997)       79 2023-04-10 03:10:37.000000 pyxk-0.5.4/pyxk/aes/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     3633 2023-05-08 07:57:14.000000 pyxk-0.5.4/pyxk/aes/_fmtdata.py
--rw-rw----   0 root         (0) everybody  (9997)     4695 2023-05-08 07:56:51.000000 pyxk-0.5.4/pyxk/aes/cryptor.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.202000 pyxk-0.5.4/pyxk/m3u8downloader/
--rw-rw----   0 root         (0) everybody  (9997)       66 2023-05-08 07:55:15.000000 pyxk-0.5.4/pyxk/m3u8downloader/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     2312 2023-05-09 08:54:39.000000 pyxk-0.5.4/pyxk/m3u8downloader/enter_point.py
--rw-rw----   0 root         (0) everybody  (9997)     4821 2023-05-08 07:56:03.000000 pyxk-0.5.4/pyxk/m3u8downloader/m3u8download.py
--rw-rw----   0 root         (0) everybody  (9997)     2968 2023-05-08 04:33:43.000000 pyxk-0.5.4/pyxk/m3u8downloader/m3u8parse.py
--rw-rw----   0 root         (0) everybody  (9997)    10951 2023-05-09 08:47:57.000000 pyxk-0.5.4/pyxk/m3u8downloader/main.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.212000 pyxk-0.5.4/pyxk/requests/
--rw-rw----   0 root         (0) everybody  (9997)      247 2023-05-08 07:57:36.000000 pyxk-0.5.4/pyxk/requests/__init__.py
--rw-rw----   0 root         (0) everybody  (9997)     7480 2023-05-08 07:58:19.000000 pyxk-0.5.4/pyxk/requests/api.py
--rw-rw----   0 root         (0) everybody  (9997)     3309 2023-05-09 03:19:15.000000 pyxk-0.5.4/pyxk/requests/entry_point.py
--rw-rw----   0 root         (0) everybody  (9997)    14682 2023-05-09 03:23:24.000000 pyxk-0.5.4/pyxk/requests/sessions.py
--rw-rw----   0 root         (0) everybody  (9997)    18965 2023-05-08 09:56:53.000000 pyxk-0.5.4/pyxk/utils.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-09 09:35:36.202000 pyxk-0.5.4/pyxk.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      627 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)       99 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/entry_points.txt
--rw-rw----   0 root         (0) everybody  (9997)       55 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/requires.txt
--rw-rw----   0 root         (0) everybody  (9997)        5 2023-05-09 09:35:36.000000 pyxk-0.5.4/pyxk.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)       38 2023-05-09 09:35:36.212000 pyxk-0.5.4/setup.cfg
--rw-rw----   0 root         (0) everybody  (9997)      927 2023-05-09 09:35:11.000000 pyxk-0.5.4/setup.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/
+-rw-rw----   0 root         (0) everybody  (9997)     1079 2022-09-01 11:31:05.000000 pyxk-0.5.5/LICENSE
+-rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:33:26.034000 pyxk-0.5.5/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)        4 2023-03-31 15:33:16.000000 pyxk-0.5.5/README.md
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk/
+-rw-rw----   0 root         (0) everybody  (9997)       53 2023-05-08 09:38:07.000000 pyxk-0.5.5/pyxk/__init__.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk/aclient/
+-rw-rw----   0 root         (0) everybody  (9997)       49 2023-05-13 08:37:44.000000 pyxk-0.5.5/pyxk/aclient/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)    17711 2023-05-13 08:47:34.000000 pyxk-0.5.5/pyxk/aclient/client.py
+-rw-rw----   0 root         (0) everybody  (9997)      615 2023-05-13 05:40:17.000000 pyxk-0.5.5/pyxk/aclient/typedef.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/aes/
+-rw-rw----   0 root         (0) everybody  (9997)       79 2023-04-10 03:10:37.000000 pyxk-0.5.5/pyxk/aes/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     3633 2023-05-08 07:57:14.000000 pyxk-0.5.5/pyxk/aes/_fmtdata.py
+-rw-rw----   0 root         (0) everybody  (9997)     4695 2023-05-08 07:56:51.000000 pyxk-0.5.5/pyxk/aes/cryptor.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/m3u8downloader/
+-rw-rw----   0 root         (0) everybody  (9997)       66 2023-05-08 07:55:15.000000 pyxk-0.5.5/pyxk/m3u8downloader/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     3484 2023-05-13 09:31:31.000000 pyxk-0.5.5/pyxk/m3u8downloader/enter_point.py
+-rw-rw----   0 root         (0) everybody  (9997)     4884 2023-05-13 09:28:48.000000 pyxk-0.5.5/pyxk/m3u8downloader/m3u8download.py
+-rw-rw----   0 root         (0) everybody  (9997)     2968 2023-05-08 04:33:43.000000 pyxk-0.5.5/pyxk/m3u8downloader/m3u8parse.py
+-rw-rw----   0 root         (0) everybody  (9997)    11732 2023-05-13 09:23:24.000000 pyxk-0.5.5/pyxk/m3u8downloader/main.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.034000 pyxk-0.5.5/pyxk/requests/
+-rw-rw----   0 root         (0) everybody  (9997)      247 2023-05-08 07:57:36.000000 pyxk-0.5.5/pyxk/requests/__init__.py
+-rw-rw----   0 root         (0) everybody  (9997)     7480 2023-05-08 07:58:19.000000 pyxk-0.5.5/pyxk/requests/api.py
+-rw-rw----   0 root         (0) everybody  (9997)     3309 2023-05-09 03:19:15.000000 pyxk-0.5.5/pyxk/requests/entry_point.py
+-rw-rw----   0 root         (0) everybody  (9997)    14682 2023-05-09 03:23:24.000000 pyxk-0.5.5/pyxk/requests/sessions.py
+-rw-rw----   0 root         (0) everybody  (9997)    19219 2023-05-13 07:41:11.000000 pyxk-0.5.5/pyxk/utils.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 09:33:26.024000 pyxk-0.5.5/pyxk.egg-info/
+-rw-rw----   0 root         (0) everybody  (9997)      345 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)      627 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/SOURCES.txt
+-rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/dependency_links.txt
+-rw-rw----   0 root         (0) everybody  (9997)       99 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/entry_points.txt
+-rw-rw----   0 root         (0) everybody  (9997)       55 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/requires.txt
+-rw-rw----   0 root         (0) everybody  (9997)        5 2023-05-13 09:33:25.000000 pyxk-0.5.5/pyxk.egg-info/top_level.txt
+-rw-rw----   0 root         (0) everybody  (9997)       38 2023-05-13 09:33:26.034000 pyxk-0.5.5/setup.cfg
+-rw-rw----   0 root         (0) everybody  (9997)      927 2023-05-13 09:33:13.000000 pyxk-0.5.5/setup.py
```

### Comparing `pyxk-0.5.4/LICENSE` & `pyxk-0.5.5/LICENSE`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/aclient/client.py` & `pyxk-0.5.5/pyxk/aclient/client.py`

 * *Files 26% similar despite different names*

```diff
@@ -10,461 +10,482 @@
     Pattern
 )
 from types import MethodType
 from itertools import zip_longest
 from multidict import CIMultiDict
 
 import aiohttp
-from yarl import URL
-from aiohttp import client_exceptions as aiohttp_client_exceptions
-try:
-    import chardet as _chardet
-except ImportError:
-    import charset_normalizer as _chardet
-from parsel.selector import Selector, LXML_SUPPORTS_HUGE_TREE
 
 from pyxk.aclient.typedef import (
     StrOrURL,
     Session,
     Response,
     EventLoop,
     CIMDict,
     Timeout,
-    ResponseSelector,
     RequestCallback
 )
-from pyxk.utils import get_user_agent
-
+from pyxk.utils import (
+    chardet,
+    LazyLoader,
+    get_user_agent,
+    default_headers,
+)
 
+_yarl = LazyLoader("_yarl", globals(), "yarl")
+_selector = LazyLoader("_selector", globals(), "parsel.selector")
+aiohttp_client_exceptions = LazyLoader("aiohttp_client_exceptions", globals(), "aiohttp.client_exceptions")
 
-__all__ = ["chardet", "Client"]
+__all__ = ["Client"]
 
-def chardet(byte: bytes):
-    """字符编码判断"""
-    return _chardet.detect(byte)
 
 
 class Client:
-    """
-    异步下载器 - 类变量
+    """异步下载器 - 类变量
 
-    :params: limit : 并发数量
-    :params: timeout : 请求超时时间
-    :params: headers : 请求头
-    :params: verify_ssl : ssl验证
-    :params: start_urls : 请求入口urls
-    :params: user_agnet : User-Agent
-    :params: aiohttp_kwargs : aiohttp.ClientSession 实例化参数
-    :params: retry_status_code : 请求状态码，包含在列表中的进行重新发送
+    :params: limit: aiohttp 并发控制
+    :params: timeout: 请求超时时间
+    :params: async_sleep: 异步休眠时间
+    :params: maximum_retry: 异步请求最大重试次数
+    :params: headers: 请求头
+    :params: semaphore: asyncio 并发控制
+    :params: verify: ssl验证
+    :params: start_urls: 请求入口urls
+    :params: user_agnet: User-Agent
+    :params: aiohttp_kwargs: aiohttp.ClientSession 实例化参数
+    :params: retry_status_code: 请求状态码，包含在列表中的进行重新发送
     :params: error_status_code: 请求状态码，包含在列表中直接抛出错误
+    :params: until_request_succeed: 请求状态码，知道请求成功为止
 
     __init__ parameters - 实例化参数
 
-    :params: loop : asyncio event loop
-    :params: session : aiohttp client_session
     :params: base_url : base_url
     """
-    limit: int = 16
-    timeout: Timeout = 7
+
+    limit: Optional[int] = None
+    timeout: Timeout = None
+    async_sleep: Optional[int] = None
+    maximum_retry: Optional[int] = None
     headers: Optional[Union[dict, CIMDict]] = None
-    verify_ssl: bool = True
+    semaphore: Optional[int] = None
+    verify: Optional[bool] = None
     start_urls: Union[List[str], List[Tuple[str, dict]]] = []
-    user_agent: str = get_user_agent("windows")
+    user_agent: Optional[str] = None
     aiohttp_kwargs: Optional[dict] = None
     retry_status_code: Optional[list] = None
     error_status_code: Optional[list] = None
+    until_request_succeed: Optional[Union[bool, List[int]]] = None
 
-    def __init__(
-        self,
-        *,
-        loop: EventLoop=None,
-        session: Session=None,
-        base_url: StrOrURL=None,
-    ) -> None:
-        self._loop = loop
-        self._session = session
-        self._base_url = self.set_base_url(base_url)
+    attr = (
+        ("limit", 100),
+        ("timeout", 7),
+        ("headers", CIMultiDict(default_headers())),
+        ("semaphore", 16),
+        ("verify", True),
+        ("async_sleep", 1),
+        ("maximum_retry", 20),
+        ("user_agent", get_user_agent()),
+        ("aiohttp_kwargs", {}),
+        ("until_request_succeed", False),
+    )
+
+    def __init__(self, *, base_url: StrOrURL=None):
+        # event loop
+        self._loop: EventLoop = None
+        # aiohttp session
+        self._session: Session = None
+        # base_url
+        self._base_url: StrOrURL = self.set_base_url(base_url)
 
     @classmethod
     def run(cls, **kwargs):
-        """
-        异步下载器 运行入口 - 应该从此方法运行
-
-        :params: **kwargs : 实例化参数
-        """
-        if not kwargs.__contains__("loop"):
-            loop = asyncio.new_event_loop()
-            asyncio.set_event_loop(loop)
-            kwargs.__setitem__("loop", loop)
         self = cls(**kwargs)
-        # run
-        self.loop.run_until_complete(self.async_start())
-        # close event loop
-        self.loop.close()
+        # 创建新的 event loop
+        self._loop = asyncio.new_event_loop()
+        asyncio.set_event_loop(self._loop)
+        # 运行
+        self._loop.run_until_complete(self.async_start())
+        # 关闭 event loop
+        self._loop.close()
         return self
 
-    async def async_start(self):
+    async def async_start(self) -> None:
         """开启异步下载器"""
-        # 创建 aiohttp session
         try:
-            # 创建 aiohttp session
-            await self.create_aiohttp_session()
+            # event loop
+            if (
+                not self._loop
+                or not isinstance(self._loop, asyncio.AbstractEventLoop)
+                or self._loop.is_closed()
+            ):
+                self._loop = asyncio.get_event_loop()
+                asyncio.set_event_loop(self._loop)
+            # semaphore
+            if not isinstance(self.semaphore, (int, float)) or self.semaphore < 0:
+                self.semaphore = dict(self.attr)["semaphore"]
+            self.semaphore = asyncio.Semaphore(self.semaphore)
+            # aiohttp kwargs
+            aiohttp_kwargs = self.aiohttp_kwargs \
+                if isinstance(self.aiohttp_kwargs, dict) else dict(self.attr)["aiohttp_kwargs"]
+            aiohttp_kwargs = aiohttp_kwargs.copy()
+            # timeout
+            if not aiohttp_kwargs.__contains__("timeout"):
+                if not isinstance(self.timeout, aiohttp.ClientTimeout):
+                    timeout = aiohttp.ClientTimeout(
+                        total = self.timeout \
+                            if isinstance(self.timeout, (int, float)) and self.timeout > 0 else dict(self.attr)["timeout"]
+                    )
+                else:
+                    timeout = self.timeout
+                aiohttp_kwargs["timeout"] = timeout
+            # connector
+            if not aiohttp_kwargs.__contains__("connector"):
+                aiohttp_kwargs["connector"] = aiohttp.TCPConnector(
+                    loop = self._loop,
+                    limit = self.limit \
+                        if isinstance(self.limit, int) and self.limit > 0 else dict(self.attr)["limit"],
+                    ssl = bool(self.verify) if self.verify is not None else dict(self.attr)["verify"],
+                )
+            # headers
+            if not aiohttp_kwargs.__contains__("headers"):
+                headers = CIMultiDict(self.headers) \
+                    if isinstance(self.headers, (dict, CIMultiDict)) else dict(self.attr)["headers"]
+                headers = headers.copy()
+                # User Agent
+                if self.user_agent and isinstance(self.user_agent, str):
+                    headers["User-Agent"] = self.user_agent
+                if not headers.__contains__("User-Agent"):
+                    headers["User-Agent"] = dict(self.attr)["user_agent"]
+                aiohttp_kwargs["headers"] = headers
+            # 创建 aiohttp client_session
+            self._session = aiohttp.ClientSession(loop=self._loop, **aiohttp_kwargs)
+            # 开始运行
             await self.start()
             result = await self.start_request()
-            # 运行结束返回值 传递给 completed
             await self.completed(result)
         finally:
             await self.async_close()
 
     async def async_close(self):
         """关闭异步下载器"""
         await self.close()
-        if self.session:
-            await self.session.close()
+        # 关闭 aiohttp client session
+        if isinstance(self._session, aiohttp.ClientSession) and self._session.closed is False:
+            await self._session.close()
 
     async def start_request(self) -> list:
         """发送 start_urls 链接"""
-        # 判断 start_urls 是否为空
-        if not self.start_urls:
-            raise NotImplementedError(f"{self.__class__.__name__}.start_urls is empty! (must be a 'list')")
-        cb_kwargs_list, start_urls = [], []
+        if not self.start_urls or not isinstance(self.start_urls, (list, tuple)):
+            raise NotImplementedError(f"{self.__class__.__name__}.start_urls is not available!")
+        tasks = []
         for item in self.start_urls:
-            if isinstance(item, (list, tuple)) and len(item) == 2:
-                url, cb_kwargs = item
-            else:
-                url, cb_kwargs = item, None
-            start_urls.append(url)
-            cb_kwargs_list.append(cb_kwargs)
+            url, cb_kwargs = item, None
+            if isinstance(item, (list, tuple)) and len(item) >= 2:
+                url, cb_kwargs = item[0], dict(item[1])
+            # base_url
             if not self._base_url:
-                self._base_url = self.set_base_url(url)
-        result = await self.gather(*start_urls, callback=self.parse, cb_kwargs_list=cb_kwargs_list)
+                self.base_url = url
+            task = self.request(url=url, callback=self.parse, cb_kwargs=cb_kwargs)
+            tasks.append(task)
+        result = await asyncio.gather(*tasks)
         return result
 
     async def request(
         self,
         url: StrOrURL,
+        callback: RequestCallback = None,
         *,
-        callback: RequestCallback=None,
-        method: str="GET",
-        cb_kwargs: Optional[dict]=None,
-        **kwargs
-    ) -> Any:
+        method: str = "GET",
+        cb_kwargs: Optional[dict] = None,
+        **req_kwargs
+    ) -> Union[Response, Any]:
+        """异步请求发送以及回调
+
+        :params: url: URL
+        :params: callback: 响应response 回调函数(函数是异步的)
+        :params: *
+        :params: method: 请求方法(default: GET)
+        :params: cb_kwargs: 回调函数 关键字参数
+        :params: **req_kwargs: 异步请求 request参数
         """
-        异步请求发送
-
-        :params: url : url地址
-        :params: callback : 响应response 回调函数(函数是异步的)
-        :params: method : 请求方法
-        :params: cb_kwargs : 回调函数 自定义参数
-        :params: **kwargs : 异步请求额外参数
+        async with self.semaphore:
+            url = self.build_url(url)
+            response = await self.send(method=method, url=url, **req_kwargs)
+            # 添加自定义方法
+            add_method_to_response(response)
+            # 开启回调函数
+            if callable(callback):
+                cb_kwargs = dict(cb_kwargs or {})
+                result = await callback(response, **cb_kwargs)
+                response.close()
+                return result
+            return response
+
+    async def send(
+        self, method: str, url: StrOrURL, **req_kwargs
+    ) -> Response:
+        """异步请求发送
+
+        :params: method: 请求方法
+        :params: url: URL
+        :params: **req_kwargs: 异步请求 request参数
         """
-        url = self.build_url(url)
-        exc_count, exc_max = 0, 30
-        response, is_close_response = None, False
-        cb_kwargs = cb_kwargs if isinstance(cb_kwargs, dict) else {}
+        retry, exc_count = 0, 0
+        maximum_retry = self.maximum_retry \
+            if isinstance(self.maximum_retry, int) and self.maximum_retry > 0 else dict(self.attr)["maximum_retry"]
         while True:
             try:
-                response = result = await self.session.request(method=method, url=url, **kwargs)
-                # 错误request状态码捕获
-                if (
-                    isinstance(self.error_status_code, (list, tuple))
-                    and response.status in self.error_status_code
-                ):
-                    raise aiohttp.InvalidURL(
-                        f"invalid url:{str(response.url)!r}, status_code: {response.status!r}"
-                    )
-                # request状态码捕获 并重试
-                if (
-                    isinstance(self.retry_status_code, (list, tuple))
-                    and response.status in self.retry_status_code
-                ):
-                    await asyncio.sleep(1)
+                response = await self._session.request(method=method, url=url, **req_kwargs)
+                # 抛出 error status_code
+                if isinstance(self.error_status_code, (list, tuple)) and response.status in self.error_status_code:
+                    raise aiohttp.InvalidURL(f"<Response[{response.status}] {url}>")
+                # 重试 retry status_code
+                if isinstance(self.retry_status_code, (list, tuple)) and response.status in self.retry_status_code:
+                    response.close()
+                    retry += 1
+                    if retry % 10 == 0:
+                        warnings.warn(f"<Response[{response.status}] {url}>, Retry: {retry}", stacklevel=4)
+                    await self.sleep()
+                    continue
+                # 直到请求状态码200才返回 until_request_succeed
+                as_succeed = self.until_request_succeed \
+                    if self.until_request_succeed is not None else dict(self.attr)["until_request_succeed"]
+                if not isinstance(as_succeed, (list, tuple)):
+                    as_succeed = [200] if as_succeed else []
+                if as_succeed and response.status not in as_succeed:
+                    response.close()
+                    retry += 1
+                    if retry % 10 == 0:
+                        warnings.warn(f"<Response[{response.status}] {url}>, Retry: {retry}", stacklevel=4)
+                    await self.sleep()
                     continue
-                # response 添加方法
-                add_method_to_response(response)
-                if callable(callback):
-                    result = await callback(response, **cb_kwargs)
-                    is_close_response = True
                 break
             # 请求超时 重试
             except asyncio.exceptions.TimeoutError:
                 exc_count += 1
-                if exc_count > exc_max:
+                if exc_count >= maximum_retry:
                     raise
-                await asyncio.sleep(1)
+                # warnings.warn(f"<{url}> Timeout", stacklevel=4)
+                await self.sleep()
             # 连接错误 重试
             except (
                 aiohttp_client_exceptions.ClientOSError,
                 aiohttp_client_exceptions.ClientPayloadError,
                 aiohttp_client_exceptions.ClientConnectorError,
             ):
                 exc_count += 1
-                if exc_count > exc_max:
+                if exc_count >= maximum_retry:
                     raise
-                # warnings.warn("Client Connector Error", stacklevel=4)
-                await asyncio.sleep(1)
+                # warnings.warn(f"<{url}> ConnectorError", stacklevel=4)
+                await self.sleep()
             # 服务器拒绝连接
             except aiohttp_client_exceptions.ServerDisconnectedError:
                 exc_count += 1
-                if exc_count > exc_max:
+                if exc_count >= maximum_retry:
                     raise
-                # warnings.warn("Server Disconnected Error", stacklevel=4)
-                await asyncio.sleep(1)
-            finally:
-                if response and is_close_response:
-                    response.close()
-        return result
+                # warnings.warn(f"<{url}> ServerDisconnectedError", stacklevel=4)
+                await self.sleep()
+        return response
+
+    async def sleep(self, delay: Optional[Union[int, float]]=None, result: Any=None):
+        """异步休眠"""
+        if not isinstance(delay, int) or delay <= 0:
+            delay = self.async_sleep \
+                if isinstance(self.async_sleep, int) and self.async_sleep > 0 else dict(self.attr)["async_sleep"]
+        return await asyncio.sleep(delay, result=result)
 
     async def gather(
         self,
-        *urls,
-        callback: RequestCallback=None,
-        method: str="GET",
-        cb_kwargs_list: List[dict]=None,
-        return_exceptions=False,
-        **kwargs
+        urls: List[StrOrURL],
+        callback: RequestCallback = None,
+        *,
+        method: str = "GET",
+        cb_kwargs_list: Optional[List[dict]] = None,
+        return_exceptions: bool = False,
+        **req_kwargs
     ) -> list:
-        """
-        收集 url列表，创建异步任务 并发发送
+        """发送url列表，创建异步任务 并发发送
 
-        :params: *urls : url 并发集合
-        :params: callback : 回调函数
-        :params: method : 请求方法
-        :params: cb_kwargs_list : 回调函数参数列表
-        :params: return_exceptions : 错误传递
-        :params: **kwargs : 请求参数
+        :params: urls: url list
+        :params: callback: 响应response 回调函数(函数是异步的)
+        :params: *
+        :params: method: 请求方法(default: GET)
+        :params: cb_kwargs_list: 回调函数关键字参数列表
+        :params: return_exceptions: 错误传递(default: False)
+        :params: **req_kwargs: 异步请求 request参数
         """
-        # cb_kwargs_list
+        # 初始化 cb_kwargs_list
         if isinstance(cb_kwargs_list, dict):
             cb_kwargs_list = [cb_kwargs_list for _ in enumerate(urls)]
-        elif not isinstance(cb_kwargs_list, (list, tuple)):
-            cb_kwargs_list = []
-
-        request_tasks = [
-            self.request(
-                url, callback=callback, method=method, cb_kwargs=cb_kwargs, **kwargs
+        elif isinstance(cb_kwargs_list, (list, tuple)):
+            cb_kwargs_list = cb_kwargs_list[:len(urls)]
+        else:
+            cb_kwargs_list = None
+        # 初始化urls
+        _urls, _cb_kw, = [], []
+        for item in urls:
+            url, cb_kwargs = item, None
+            if isinstance(item, (list, tuple)) and len(item) >= 2:
+                url, cb_kwargs = item[0], dict(item[1])
+            _urls.append(url)
+            _cb_kw.append(cb_kwargs)
+        urls = _urls
+        if not cb_kwargs_list:
+            cb_kwargs_list = _cb_kw
+        del _urls, _cb_kw
+        # 收集任务
+        tasks = []
+        for url, cb_kwargs in zip_longest(urls, cb_kwargs_list):
+            task = self.request(
+                url=url,
+                callback=callback,
+                method=method,
+                cb_kwargs=cb_kwargs,
+                **req_kwargs
             )
-            for url, cb_kwargs in zip_longest(urls, cb_kwargs_list, fillvalue={})
-        ]
-        result = await asyncio.gather(
-            *request_tasks,
-            return_exceptions=return_exceptions
-        )
+            tasks.append(task)
+        result = await asyncio.gather(*tasks, return_exceptions=return_exceptions)
         return result
 
-    async def create_aiohttp_session(self) -> None:
-        """创建 aiohttp session"""
-        headers = self.merge_headers()
-        aiohttp_kwargs = self.merge_aiohttp_kwargs()
-        self.session = aiohttp.ClientSession(
-            loop=self.loop, headers=headers, **aiohttp_kwargs
-        )
-
-    def merge_headers(self) -> CIMDict:
-        """合并 headers"""
-        headers = CIMultiDict(self.headers or {})
-        headers.setdefault("User-Agent", self.user_agent)
-        return headers
-
-    def merge_aiohttp_kwargs(self) -> dict:
-        """合并 aiohttp kwargs"""
-        aiohttp_kwargs = dict(self.aiohttp_kwargs or {})
-        # timeout 默认7秒
-        if isinstance(self.timeout, (int, float)) and self.timeout >= 0:
-            timeout = self.timeout
-        elif not isinstance(self.timeout, aiohttp.ClientTimeout):
-            timeout = 7
-        aiohttp_kwargs.setdefault("timeout", aiohttp.ClientTimeout(total=timeout))
-
-        # connector 默认 limit=16
-        if isinstance(self.limit, int) and self.limit >= 0:
-            limit = self.limit
-        else:
-            limit = 16
-        connector = aiohttp.TCPConnector(limit=limit, loop=self.loop, verify_ssl=self.verify_ssl)
-        aiohttp_kwargs.setdefault("connector", connector)
-        return aiohttp_kwargs
-
-
     def build_url(self, _url) -> StrOrURL:
         """构造完整url地址"""
-        if not isinstance(_url, (str, URL)):
+        if not isinstance(_url, (str, _yarl.URL)):
             return _url
-        _url = URL(_url)
+        _url = _yarl.URL(_url)
         if _url.is_absolute():
             return _url
-        if self.base_url and isinstance(self.base_url, URL):
-            return self.base_url.join(_url)
+        if self._base_url and isinstance(self._base_url, _yarl.URL):
+            return self._base_url.join(_url)
         return _url
 
     @staticmethod
-    def set_base_url(url: StrOrURL, /) -> StrOrURL:
+    def set_base_url(url: StrOrURL) -> StrOrURL:
         """设置 base_url"""
-        if url is None:
-            return None
-        if not isinstance(url, (str, URL)):
-            warnings.warn(f"{url!r} invalid base_url", stacklevel=4)
+        if not url or not isinstance(url, (str, _yarl.URL)):
             return None
-        url = URL(url)
+        url = _yarl.URL(url)
         if not url.is_absolute():
             # 不是绝对路径
-            warnings.warn(f"{url.human_repr()!r} not absolute", stacklevel=4)
             return None
         return url
 
     @property
     def loop(self) -> EventLoop:
-        """Event Loop"""
-        if not self._loop:
-            self._loop = asyncio.get_event_loop()
-            asyncio.set_event_loop(self._loop)
-        elif isinstance(self._loop, asyncio.AbstractEventLoop):
-            if self._loop.is_closed():
-                warnings.warn("Current EventLoop is closed", stacklevel=4)
+        """event loop"""
         return self._loop
 
-    @loop.setter
-    def loop(self, _loop: EventLoop) -> None:
-        if _loop is None:
-            self._loop = None
-            return
-        if not isinstance(_loop, asyncio.AbstractEventLoop):
-            warnings.warn(f"{_loop!r} invalid EventLoop", stacklevel=4)
-            self._loop = None
-            return
-        self._loop = _loop
-        asyncio.set_event_loop(_loop)
-
     @property
     def base_url(self) -> StrOrURL:
         """base_url"""
         return self._base_url
 
     @base_url.setter
     def base_url(self, _url: StrOrURL) -> None:
         self._base_url = self.set_base_url(_url)
 
-    @property
-    def session(self) -> Session:
-        """aiohttp session"""
-        return self._session
-
-    @session.setter
-    def session(self, _session: Session) -> None:
-        if not isinstance(_session, aiohttp.ClientSession):
-            warnings.warn(f"{_session!r} invalid aiohttp session", stacklevel=4)
-            return
-        self._session = _session
-
-    @staticmethod
-    async def sleep(delay: Union[int, float]=0, result: Any=None) -> Any:
-        """异步休眠"""
-        return await asyncio.sleep(delay, result=result)
-
-    @staticmethod
-    def apparent_encoding(byte: bytes):
-        return chardet(byte)["encoding"]
-
-    async def parse(self, response: Response):
+    async def parse(self, response: Response, **kwargs):
+        """默认解析函数"""
         raise NotImplementedError(f"'{self.__class__.__name__}.parse' not implemented!")
 
     async def completed(self, result: list) -> None:
         """运行完成结果回调函数"""
 
     async def start(self) -> None:
         """创建 aiohttp session 后调用"""
 
     async def close(self) -> None:
         """关闭 aiohttp session 前调用"""
 
-
 async def xpath(
     self,
     query: str,
     namespaces: Optional[Mapping[str, str]] = None,
     encoding: Optional[str] = None,
     type: Optional[str] = None,
     root: Optional[Any] = None,
     base_url: Optional[str] = None,
     _expr: Optional[str] = None,
-    huge_tree: bool = LXML_SUPPORTS_HUGE_TREE,
+    huge_tree: Optional[bool] = None,
     errors: str = "strict",
     **kwargs
-) -> ResponseSelector:
+):
     text = await self.text(encoding=encoding, errors=errors)
-    selector = Selector(
+    selector = _selector.Selector(
         text=text,
         type=type,
         _expr=_expr,
         namespaces=namespaces,
         root=root,
         base_url=base_url,
-        huge_tree=huge_tree,
+        huge_tree=_selector.LXML_SUPPORTS_HUGE_TREE if huge_tree is None else huge_tree,
     )
     return selector.xpath(query=query, **kwargs)
 
 async def css(
     self,
     query: str,
     namespaces: Optional[Mapping[str, str]] = None,
     encoding: Optional[str] = None,
     type: Optional[str] = None,
     root: Optional[Any] = None,
     base_url: Optional[str] = None,
     _expr: Optional[str] = None,
-    huge_tree: bool = LXML_SUPPORTS_HUGE_TREE,
+    huge_tree: Optional[bool] = None,
     errors: str = "strict"
-) -> ResponseSelector:
+):
     text = await self.text(encoding=encoding, errors=errors)
-    selector = Selector(
+    selector = _selector.Selector(
         text=text,
         type=type,
         _expr=_expr,
         namespaces=namespaces,
         root=root,
         base_url=base_url,
-        huge_tree=huge_tree,
+        huge_tree=_selector.LXML_SUPPORTS_HUGE_TREE if huge_tree is None else huge_tree,
     )
     return selector.css(query=query)
 
 async def re(
     self,
     regex: Union[str, Pattern[str]],
     replace_entities: bool = True,
     namespaces: Optional[Mapping[str, str]] = None,
     encoding: Optional[str] = None,
     type: Optional[str] = None,
     root: Optional[Any] = None,
     base_url: Optional[str] = None,
     _expr: Optional[str] = None,
-    huge_tree: bool = LXML_SUPPORTS_HUGE_TREE,
+    huge_tree: Optional[bool] = None,
     errors: str = "strict",
-) -> ResponseSelector:
+):
     text = await self.text(encoding=encoding, errors=errors)
-    selector = Selector(
+    selector = _selector.Selector(
         text=text,
         type=type,
         _expr=_expr,
         namespaces=namespaces,
         root=root,
         base_url=base_url,
-        huge_tree=huge_tree,
+        huge_tree=_selector.LXML_SUPPORTS_HUGE_TREE if huge_tree is None else huge_tree,
     )
     return selector.re(regex=regex, replace_entities=replace_entities)
 
-def urljoin(self, _url: Union[str, URL], /) -> StrOrURL:
+def urljoin(self, _url):
     if isinstance(_url, str):
-        _url = URL(_url)
-    elif not isinstance(_url, URL):
+        _url = _yarl.URL(_url)
+    elif not isinstance(_url, _yarl.URL):
         return _url
     if _url.is_absolute():
         return _url
     return self.url.join(_url)
 
-def add_method_to_response(response: Response) -> None:
-    """
-    为异步response添加实例方法
-    """
+async def apparent_encoding(self):
+    byte = await self.read()
+    return chardet(byte)["encoding"]
+
+def add_method_to_response(response):
+    """为异步response添加实例方法"""
     response.re = MethodType(re, response)
     response.css = MethodType(css, response)
     response.xpath = MethodType(xpath, response)
     response.urljoin = MethodType(urljoin, response)
+    response.apparent_encoding = MethodType(apparent_encoding, response)
```

### Comparing `pyxk-0.5.4/pyxk/aclient/typedef.py` & `pyxk-0.5.5/pyxk/aclient/typedef.py`

 * *Files 23% similar despite different names*

```diff
@@ -4,22 +4,19 @@
     Optional,
     Callable,
 )
 from multidict import CIMultiDict
 from asyncio import AbstractEventLoop
 
 from yarl import URL
-from parsel import SelectorList
 from aiohttp import ClientSession, ClientResponse, ClientTimeout
 
 
-
-__all__ = ["Session", "EventLoop", "Response", "CIMDict", "StrOrURL", "Timeout", "RequestCallback", "ResponseSelector"]
+__all__ = ["Session", "EventLoop", "Response", "CIMDict", "StrOrURL", "Timeout", "RequestCallback"]
 
 EventLoop = Optional[AbstractEventLoop]
 Session = Optional[ClientSession]
 Response = Optional[ClientResponse]
 CIMDict = Optional[CIMultiDict]
-StrOrURL =Optional[Union[str, URL]]
-Timeout = Union[int, float, ClientTimeout]
+StrOrURL = Optional[Union[str, URL]]
+Timeout = Optional[Union[int, float, ClientTimeout]]
 RequestCallback = Callable[[ClientResponse], Any]
-ResponseSelector = Optional[SelectorList]
```

### Comparing `pyxk-0.5.4/pyxk/aes/_fmtdata.py` & `pyxk-0.5.5/pyxk/aes/_fmtdata.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/aes/cryptor.py` & `pyxk-0.5.5/pyxk/aes/cryptor.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/m3u8downloader/enter_point.py` & `pyxk-0.5.5/pyxk/m3u8downloader/enter_point.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,49 +1,70 @@
 import click
-from pyxk.m3u8downloader import load_url, load_content
+from pyxk import LazyLoader, get_user_agent
 
+m3u8downloader = LazyLoader("m3u8downloader", globals(), "pyxk.m3u8downloader")
 
 
-@click.group(invoke_without_command=True)
-@click.option("-u", "--url", "url", type=str, default=None, help="m3u8 url")
+@click.group(invoke_without_command=False, chain=False)
 @click.option("-o", "--output", "output", type=str, default=None, help="M3U8存储路径")
 @click.option("--reload", is_flag=True, help="重载m3u8资源")
 @click.option("--reserve", is_flag=True, help="保留m3u8资源")
 @click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
 @click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
 @click.option("-l", "--limit", "limit", type=int, default=16, help="下载并发量")
+@click.option("-ua", "--user-agent", "user_agent", type=str, default=None, help="User-Agent")
 @click.pass_context
-def main(ctx, url, output, reload, reserve, headers, verify, limit):
+def main(ctx, output, reload, reserve, headers, verify, limit, user_agent):
     """下载m3u8资源 - m3u8 url"""
     if not ctx.obj or not isinstance(ctx.obj, dict):
         ctx.obj = {}
     # 将参数传递给子命令
     if ctx.invoked_subcommand:
         ctx.obj.update(ctx.params)
-        return
-    # 没有调用子命令
-    if not url:
-        url = click.prompt("请输入 m3u8 url", type=str)
-    load_url(url, output=output, reload=reload, reserve=reserve, headers=dict(headers), verify=verify, limit=limit)
 
 @main.command
 @click.pass_obj
-@click.argument("content", type=click.Path(exists=True), metavar="<m3u8 file path>")
+@click.argument("content", type=click.Path(exists=True), metavar="<FilePath>")
 @click.option("-u", "--url", "url", type=str, default=None, help="m3u8 url")
 @click.option("-o", "--output", "output", type=str, default=None, help="M3U8存储路径")
 @click.option("--reload", is_flag=True, help="重载m3u8资源")
 @click.option("--reserve", is_flag=True, help="保留m3u8资源")
 @click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
 @click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
 @click.option("-l", "--limit", "limit", type=int, default=None, help="下载并发量")
-def file(obj, content, url, output, reload, reserve, headers, verify, limit):
+@click.option("-ua", "--user-agent", "user_agent", type=str, default=None, help="User-Agent")
+def file(obj, content, url, output, reload, reserve, headers, verify, limit, user_agent):
     """下载m3u8资源 - m3u8 content"""
-    load_content(
+    m3u8downloader.load_content(
         content=content,
         url=url or obj["url"],
         output=output or obj["output"],
         reload=reload,
         reserve=reserve,
         headers=dict(headers or obj["headers"]),
         verify=verify,
-        limit=limit or obj["limit"]
+        limit=limit or obj["limit"],
+        user_agent=get_user_agent(user_agent or obj["user_agent"])
+    )
+
+@main.command
+@click.pass_obj
+@click.argument("_url", type=str, metavar="<URL>")
+@click.option("-o", "--output", "output", type=str, default=None, help="M3U8存储路径")
+@click.option("--reload", is_flag=True, help="重载m3u8资源")
+@click.option("--reserve", is_flag=True, help="保留m3u8资源")
+@click.option("-h", "--headers", "headers", type=(str, str), multiple=True, help="Request Headers")
+@click.option("--no-verify", "verify", is_flag=True, default=True, help="Request Verify")
+@click.option("-l", "--limit", "limit", type=int, default=None, help="下载并发量")
+@click.option("-ua", "--user-agent", "user_agent", type=str, default=None, help="User-Agent")
+def url(obj, _url, output, reload, reserve, headers, verify, limit, user_agent):
+    """下载m3u8资源 - m3u8 content"""
+    m3u8downloader.load_url(
+        url=_url,
+        output=output or obj["output"],
+        reload=reload,
+        reserve=reserve,
+        headers=dict(headers or obj["headers"]),
+        verify=verify,
+        limit=limit or obj["limit"],
+        user_agent=get_user_agent(user_agent or obj["user_agent"])
     )
```

### Comparing `pyxk-0.5.4/pyxk/m3u8downloader/m3u8download.py` & `pyxk-0.5.5/pyxk/m3u8downloader/m3u8download.py`

 * *Files 5% similar despite different names*

```diff
@@ -17,37 +17,39 @@
     """m3u8 - segments 下载器
 
     :params: m3u8keys: m3u8资源加密密钥
     :params: segments: m3u8 segments
     :params: progress: rich.progress.Progress
     :params: download: rich.progress.Progress
     """
-    timeout = 120
+    timeout = 30
     error_status_code = list(range(403, 411))
-    retry_status_code = list(range(201, 601))
+    until_request_succeed = True
 
     def __init__(
         self,
         *,
         m3obj,
         m3u8keys: Optional[dict] = None,
         segments: Optional[dict] = None,
         progress: Optional[object] = None,
         download: Optional[object] = None,
         **kwargs
     ):
         super().__init__(**kwargs)
         self.m3obj = m3obj
-        self.limit = self.m3obj._limit
+        self.limit = m3obj._limit
         self.cipher = {index: Cryptor(**cipher) for index, cipher in m3u8keys.items()} if m3u8keys else {}
         self.tempfiles = os.path.join(self.m3obj._tempfiles, "segments") if self.m3obj._tempfiles else None
+        self.semaphore = m3obj._limit
         self.start_urls = segments
         self.task = None
         self.progress = progress
         self.download = download
+        self.user_agent = m3obj._user_agent
 
     async def start_request(self):
         # 数据不齐全 不下载
         if (
             not self.start_urls
             or not self.tempfiles
             or not self.m3obj.output
```

### Comparing `pyxk-0.5.4/pyxk/m3u8downloader/m3u8parse.py` & `pyxk-0.5.5/pyxk/m3u8downloader/m3u8parse.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/m3u8downloader/main.py` & `pyxk-0.5.5/pyxk/m3u8downloader/main.py`

 * *Files 10% similar despite different names*

```diff
@@ -7,24 +7,23 @@
     hash256,
     make_open,
     LazyLoader,
     progress_column,
     download_column,
     human_playtime
 )
-from pyxk.requests import Session
 from pyxk.m3u8downloader.m3u8parse import M3U8Parae
 from pyxk.m3u8downloader.m3u8download import Downloader
 
 _rich_box = LazyLoader("_rich_box", globals(), "rich.box")
 _rich_live = LazyLoader("_rich_live", globals(), "rich.live")
 _rich_table = LazyLoader("_rich_table", globals(), "rich.table")
 _rich_panel = LazyLoader("_rich_panel", globals(), "rich.panel")
 _rich_console = LazyLoader("_rich_console", globals(), "rich.console")
-
+_requests = LazyLoader("_requests", globals(), "pyxk.requests")
 
 
 class M3U8:
     """m3u8资源下载器"""
     def __init__(self):
         # m3u8文件输出
         self._output = None
@@ -36,15 +35,17 @@
         self._reserve = False
         # request - verify
         self._verify = True
         # request - headers
         self._headers = None
         # limit
         self._limit = 16
-        self._session = Session()
+        # user agent
+        self._user_agent = None
+        self._session = None
         self._console = _rich_console.Console()
 
     @property
     def output(self):
         """output"""
         return self._output
 
@@ -65,28 +66,32 @@
         *,
         output: Optional[str] = None,
         reload: bool = False,
         reserve: bool = False,
         headers: Optional[dict] = None,
         verify: bool = True,
         limit: int = 16,
+        user_agent: Optional[str] = None,
     ):
         """下载m3u8资源 - m3u8 url
 
         :params: url: m3u8 url
         :params: output: m3u8资源输出到文件
         :params: reload: 重新从网络加载m3u8文件
         :params: reserve: 下载完成后保留m3u8文件
         :params: headers: request 请求头
         :params: verify: request verify
         :params: limit: 异步下载并发量
+        :params: user_agent: User-Agent
         """
         self.output, self._limit = output, limit if isinstance(limit, int) and limit > 0 else 16
         self._reload, self._reserve = bool(reload), bool(reserve)
         self._headers, self._verify = headers, bool(verify)
+        self._user_agent = user_agent if user_agent and isinstance(user_agent, str) else None
+        self._session = _requests.Session(user_agent=self._user_agent)
         # 关闭requests警告
         if self._verify is False:
             import urllib3
             urllib3.disable_warnings()
         content = self.get_m3u8_content(url)
         # 无效m3u8内容
         if not self._is_m3u8_content(content):
@@ -102,29 +107,33 @@
         *,
         output: Optional[str] = None,
         reload: bool = False,
         reserve: bool = False,
         headers: Optional[dict] = None,
         verify: bool = True,
         limit: int = 16,
+        user_agent: Optional[str] = None,
     ):
         """下载m3u8资源 - m3u8 content
 
         :params: content: m3u8 content 或 m3u8本地文件路径
         :params: url: m3u8 url
         :params: output: m3u8资源输出到文件
         :params: reload: 重新从网络加载m3u8文件
         :params: reserve: 下载完成后保留m3u8文件
         :params: headers: request 请求头
         :params: verify: request verify
         :params: limit: 异步下载并发量
+        :params: user_agent: User-Agent
         """
         self.output, self._limit = output, limit if isinstance(limit, int) and limit > 0 else 16
         self._reload, self._reserve = bool(reload), bool(reserve)
         self._headers, self._verify = headers, bool(verify)
+        self._user_agent = user_agent if user_agent and isinstance(user_agent, str) else None
+        self._session = _requests.Session(user_agent=self._user_agent)
         # 关闭requests警告
         if self._verify is False:
             import urllib3
             urllib3.disable_warnings()
         # 无效m3u8内容
         if not self._is_m3u8_content(content):
             m3u8file = os.path.normpath(os.path.abspath(content)) if isinstance(content, str) else None
@@ -261,63 +270,69 @@
     *,
     output: Optional[str] = None,
     reload: bool = False,
     reserve: bool = False,
     headers: Optional[dict] = None,
     verify: bool = True,
     limit: int = 16,
+    user_agent: Optional[str] = None,
 ):
     """下载m3u8资源 - m3u8 url
 
     :params: url: m3u8 url
     :params: output: m3u8资源输出到文件
     :params: reload: 重新从网络加载m3u8文件
     :params: reserve: 下载完成后保留m3u8文件
     :params: headers: request 请求头
     :params: verify: request verify
     :params: limit: 异步下载并发量
+    :params: user_agent: User-Agent
     """
     m3u8obj = M3U8()
     return m3u8obj.load_url(
         url,
         output=output,
         reload=reload,
         reserve=reserve,
         headers=headers,
         verify=verify,
-        limit=limit
+        limit=limit,
+        user_agent=user_agent
     )
 
 
 def load_content(
     content: str,
     url: Optional[str] = None,
     *,
     output: Optional[str] = None,
     reload: bool = False,
     reserve: bool = False,
     headers: Optional[dict] = None,
     verify: bool = True,
     limit: int = 16,
+    user_agent: Optional[str] = None,
 ):
     """下载m3u8资源 - m3u8 content
 
     :params: content: m3u8 content 或 m3u8本地文件路径
     :params: url: m3u8 url
     :params: output: m3u8资源输出到文件
     :params: reload: 重新从网络加载m3u8文件
     :params: reserve: 下载完成后保留m3u8文件
     :params: headers: request 请求头
     :params: verify: request verify
     :params: limit: 异步下载并发量
+    :params: user_agent: User-Agent
     """
     m3u8obj = M3U8()
     return m3u8obj.load_content(
         content,
         url,
         output=output,
         reload=reload,
         reserve=reserve,
         headers=headers,
         verify=verify,
-        limit=limit
+        limit=limit,
+        user_agent=user_agent
     )
```

### Comparing `pyxk-0.5.4/pyxk/requests/api.py` & `pyxk-0.5.5/pyxk/requests/api.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/requests/entry_point.py` & `pyxk-0.5.5/pyxk/requests/entry_point.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/requests/sessions.py` & `pyxk-0.5.5/pyxk/requests/sessions.py`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/pyxk/utils.py` & `pyxk-0.5.5/pyxk/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,15 @@
     "string_conversion_digits",
     "human_playtime",
     "pycode_conversion_lazyloader",
     "pyfile_conversion_lazyloader",
     "units_conversion_from_byte",
     "download_column",
     "progress_column",
+    "chardet"
 ]
 
 
 
 class LazyLoader(ModuleType):
     """
     模块 延迟加载
@@ -145,14 +146,15 @@
 
 
 # User Agent
 def get_user_agent(ua: Optional[str]=None, overwrite: bool=False) -> str:
     """获取 UserAgent，默认 Android
 
     :params: ua: 模糊查找内置字典UserAgent
+        (android, windows, mac, iphone, ipad, symbian, apad)
     :params: overwrite: 若为True, 直接返回UserAgent
 
     :return `str`
     """
     # 重写 UserAgent
     if overwrite:
         return ua
@@ -448,28 +450,28 @@
     progress: Optional[object] = None,
     completed: Optional[float] = None,
     transient: bool = False,
     description: Optional[str] = None,
     show_transfer_speed: bool = True,
 ):
     """下载进度条
-    
+
     :params: start: 立即启动任务，如果为 False 则需要手动启动
     :params: total: 进度总步数
     :params: console: rich.console.Console
     :params: add_task: 是否添加进度任务 默认True
     :params: progress: rich.progress.Progress类 默认自动创建
     :params: completed: task 已完成步数 默认为0
     :params: transient: 转瞬即逝
     :params: description: 任务描述
     :params: show_transfer_speed: 显示任务速度
-    
+
     `add_task` is `True`
         return progress, task
-    
+
     `add_task` is `False`
         return progress
     """
     import rich.progress as rich_progress
     if not isinstance(progress, rich_progress.Progress):
         column = [
             rich_progress.TextColumn("[progress.description]{task.description}"),
@@ -503,28 +505,28 @@
     progress: Optional[object] = None,
     completed: Optional[float] = None,
     transient: bool = False,
     description: Optional[str] = None,
     show_transfer_speed: bool = False,
 ):
     """任务进度条
-    
+
     :params: start: 立即启动任务，如果为 False 则需要手动启动
     :params: total: 进度总步数
     :params: console: rich.console.Console
     :params: add_task: 是否添加进度任务 默认True
     :params: progress: rich.progress.Progress类 默认自动创建
     :params: completed: task 已完成步数 默认为0
     :params: transient: 转瞬即逝
     :params: description: 任务描述
     :params: show_transfer_speed: 显示任务速度
-    
+
     `add_task` is `True`
         return progress, task
-    
+
     `add_task` is `False`
         return progress
     """
     import rich.progress as rich_progress
     if not isinstance(progress, rich_progress.Progress):
         column = [
             rich_progress.TextColumn("[progress.description]{task.description}"),
@@ -542,7 +544,15 @@
             total=total,
             start=start,
             description=description or "",
             completed=completed or 0
         )
         return progress, task
     return progress
+
+def chardet(byte: bytes):
+    """字符编码判断"""
+    try:
+        import chardet as _chardet
+    except ImportError:
+        import charset_normalizer as _chardet
+    return _chardet.detect(byte)
```

### Comparing `pyxk-0.5.4/pyxk.egg-info/SOURCES.txt` & `pyxk-0.5.5/pyxk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyxk-0.5.4/setup.py` & `pyxk-0.5.5/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pyxk",
-    version="0.5.4",
+    version="0.5.5",
     author="pengke",
     install_requires=[
         "requests",
         "pycryptodome",
         "rich",
         "m3u8",
         "aiohttp",
```

