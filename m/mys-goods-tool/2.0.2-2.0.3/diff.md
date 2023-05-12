# Comparing `tmp/mys_goods_tool-2.0.2.tar.gz` & `tmp/mys_goods_tool-2.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mys_goods_tool-2.0.2.tar", max compression
+gzip compressed data, was "mys_goods_tool-2.0.3.tar", max compression
```

## Comparing `mys_goods_tool-2.0.2.tar` & `mys_goods_tool-2.0.3.tar`

### file list

```diff
@@ -1,24 +1,24 @@
--rw-r--r--   0        0        0     1065 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/LICENSE
--rw-r--r--   0        0        0     4155 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/README.md
--rw-r--r--   0        0        0        0 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/__init__.py
--rw-r--r--   0        0        0     2226 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/__main__.py
--rw-r--r--   0        0        0    56880 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/api.py
--rw-r--r--   0        0        0     5536 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/custom_css.py
--rw-r--r--   0        0        0     7599 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/custom_widget.py
--rw-r--r--   0        0        0     9176 2023-05-10 19:31:45.275184 mys_goods_tool-2.0.2/mys_goods_tool/data_model.py
--rw-r--r--   0        0        0    13698 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/exchange_mode.py
--rw-r--r--   0        0        0    43340 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/exchange_plan_view.py
--rw-r--r--   0        0        0     6442 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/gt4-localized.html
--rw-r--r--   0        0        0     6501 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/gt4.html
--rw-r--r--   0        0        0     6840 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/index.html
--rw-r--r--   0        0        0    10861 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/gt.js
--rw-r--r--   0        0        0    14792 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/gt4.js
--rw-r--r--   0        0        0   366500 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/jquery.js
--rw-r--r--   0        0        0     6910 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/localized.html
--rw-r--r--   0        0        0     9157 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/geetest.py
--rw-r--r--   0        0        0    21679 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/login_view.py
--rw-r--r--   0        0        0    12750 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/tui.py
--rw-r--r--   0        0        0    17818 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/user_data.py
--rw-r--r--   0        0        0    11252 2023-05-10 19:31:45.279184 mys_goods_tool-2.0.2/mys_goods_tool/utils.py
--rw-r--r--   0        0        0     1535 2023-05-10 19:31:45.283184 mys_goods_tool-2.0.2/pyproject.toml
--rw-r--r--   0        0        0     5588 1970-01-01 00:00:00.000000 mys_goods_tool-2.0.2/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/LICENSE
+-rw-r--r--   0        0        0     4239 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/README.md
+-rw-r--r--   0        0        0        0 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/__init__.py
+-rw-r--r--   0        0        0     2226 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/__main__.py
+-rw-r--r--   0        0        0    56571 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/api.py
+-rw-r--r--   0        0        0     5536 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/custom_css.py
+-rw-r--r--   0        0        0     7599 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/custom_widget.py
+-rw-r--r--   0        0        0     9176 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/data_model.py
+-rw-r--r--   0        0        0    15247 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/exchange_mode.py
+-rw-r--r--   0        0        0    43505 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/exchange_plan_view.py
+-rw-r--r--   0        0        0     6442 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/gt4-localized.html
+-rw-r--r--   0        0        0     6501 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/gt4.html
+-rw-r--r--   0        0        0     6840 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/index.html
+-rw-r--r--   0        0        0    10861 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/gt.js
+-rw-r--r--   0        0        0    14792 2023-05-12 23:53:05.629523 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/gt4.js
+-rw-r--r--   0        0        0   366500 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/jquery.js
+-rw-r--r--   0        0        0     6910 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/localized.html
+-rw-r--r--   0        0        0     9157 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/geetest.py
+-rw-r--r--   0        0        0    21679 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/login_view.py
+-rw-r--r--   0        0        0    13119 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/tui.py
+-rw-r--r--   0        0        0    17830 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/user_data.py
+-rw-r--r--   0        0        0    11385 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/mys_goods_tool/utils.py
+-rw-r--r--   0        0        0     1639 2023-05-12 23:53:05.633524 mys_goods_tool-2.0.3/pyproject.toml
+-rw-r--r--   0        0        0     5672 1970-01-01 00:00:00.000000 mys_goods_tool-2.0.3/PKG-INFO
```

### Comparing `mys_goods_tool-2.0.2/LICENSE` & `mys_goods_tool-2.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/README.md` & `mys_goods_tool-2.0.3/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -12,18 +12,18 @@
   <img alt="代码行数" src="https://img.shields.io/tokei/lines/github/Ljzd-PRO/Mys_Goods_Tool?style=for-the-badge">
   <img alt="构建结果" src="https://img.shields.io/github/actions/workflow/status/Ljzd-PRO/Mys_Goods_Tool/build-v2.yml?event=pull_request&style=for-the-badge">
   <img alt="Python版本兼容性测试" src="https://img.shields.io/github/actions/workflow/status/Ljzd-PRO/Mys_Goods_Tool/python-package.yml?event=pull_request&label=Versions%20Test&style=for-the-badge">
 </div>
 
 ### 更新说明
 
-- 修复米游社（大别野）等商品分区无商品的问题
-- 修复图形界面兑换模式下不会执行兑换的问题
-- 删除多余的 `pyperclip` 依赖
-- 解决部分商品兑换时间错误的问题
+- 修复定时兑换无效的问题
+- 修复失去网络连接的情况下会导致程序退出的Bug
+- 对于 Linux 使用 Ubuntu 20.04 进行构建，防止出现缺少 GNU libc 对应版本的问题
+- 非 Windows 系统增加 [uvloop](https://github.com/MagicStack/uvloop) 支持，提高性能
 
 ## 功能和特性
 
 - [x] 使用 [Textual](https://github.com/Textualize/textual) 终端图形界面库，支持 Windows / Linux / macOS 甚至可能是移动端SSH客户端
 - [x] 短信验证码登录（只需接收一次验证码）
 - [x] 内置人机验证页面，无需前往官网验证
 - [x] 多账号支持
```

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/__main__.py` & `mys_goods_tool-2.0.3/mys_goods_tool/__main__.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/api.py` & `mys_goods_tool-2.0.3/mys_goods_tool/api.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,16 +7,16 @@
 from pydantic import ValidationError, BaseModel
 from requests.utils import dict_from_cookiejar
 
 from mys_goods_tool.data_model import GameRecord, GameInfo, Good, Address, BaseApiStatus, MmtData, GeetestResult, \
     GetCookieStatus, \
     CreateMobileCaptchaStatus, GetGoodDetailStatus, ExchangeStatus
 from mys_goods_tool.user_data import config as conf, UserAccount, BBSCookies, ExchangePlan, ExchangeResult
-from mys_goods_tool.utils import generate_device_id, logger, custom_attempt_times, generate_ds, Subscribe, \
-    NtpTime
+from mys_goods_tool.utils import generate_device_id, logger, generate_ds, Subscribe, \
+    NtpTime, get_async_retry
 
 URL_LOGIN_TICKET_BY_CAPTCHA = "https://webapi.account.mihoyo.com/Api/login_by_mobilecaptcha"
 URL_LOGIN_TICKET_BY_PASSWORD = "https://webapi.account.mihoyo.com/Api/login_by_password"
 URL_MULTI_TOKEN_BY_LOGIN_TICKET = "https://api-takumi.mihoyo.com/auth/api/getMultiTokenByLoginTicket?login_ticket={0}&token_types=3&uid={1}"
 URL_COOKIE_TOKEN_BY_CAPTCHA = "https://api-takumi.mihoyo.com/account/auth/api/webLoginByMobile"
 URL_COOKIE_TOKEN_BY_STOKEN = "https://passport-api.mihoyo.com/account/auth/api/getCookieAccountInfoBySToken"
 URL_LTOKEN_BY_STOKEN = "https://passport-api.mihoyo.com/account/auth/api/getLTokenBySToken"
@@ -289,15 +289,15 @@
         return self.retcode == -201 or self.message in ["验证码错误", "Captcha not match Err"]
 
     @property
     def login_expired(self):
         """
         是否返回登录失效
         """
-        return self.retcode == -100 or self.message in ["登录失效，请重新登录"]
+        return self.retcode in [-100, 10001] or self.message in ["登录失效，请重新登录"]
 
     @property
     def invalid_ds(self):
         """
         Headers里的DS是否无效
         """
         # TODO 2023/4/13: 待补充状态码
@@ -309,16 +309,15 @@
     """
     获取用户绑定的游戏账户信息，返回一个GameRecord对象的列表
 
     :param account: 用户账户数据
     :param retry: 是否允许重试
     """
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_GAME_RECORD.format(account.bbs_uid), headers=HEADERS_GAME_RECORD,
                                            cookies=account.cookies.dict(), timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 if api_result.login_expired:
                     logger.info(
@@ -342,16 +341,15 @@
     获取米哈游游戏的详细信息，若返回`None`说明获取失败
 
     :param retry: 是否允许重试
     """
     headers = HEADERS_GAME_LIST.copy()
     try:
         subscribe = Subscribe()
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 headers["DS"] = generate_ds()
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_GAME_LIST, headers=headers, timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 if api_result.invalid_ds:
                     logger.info(
@@ -375,16 +373,15 @@
     """
     获取用户当前米游币数量
 
     :param account: 用户账户数据
     :param retry: 是否允许重试
     """
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_MYB, headers=HEADERS_MYB, cookies=account.cookies.dict(),
                                            timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 if api_result.login_expired:
                     logger.info(
@@ -417,16 +414,15 @@
         "platform": "Android",
         "registration_id": "1a0018970a5c00e814d"
     }
     headers = HEADERS_DEVICE.copy()
     headers["x-rpc-device_id"] = account.device_id_android
     try:
         subscribe = Subscribe()
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 headers["DS"] = generate_ds(data)
                 async with httpx.AsyncClient() as client:
                     res = await client.post(URL_DEVICE_LOGIN, headers=headers, json=data,
                                             cookies=account.cookies.dict(),
                                             timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
@@ -469,16 +465,15 @@
         "platform": "Android",
         "registration_id": "1a0018970a5c00e814d"
     }
     headers = HEADERS_DEVICE.copy()
     headers["x-rpc-device_id"] = account.device_id_android
     try:
         subscribe = Subscribe()
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 headers["DS"] = generate_ds(data)
                 async with httpx.AsyncClient() as client:
                     res = await client.post(URL_DEVICE_SAVE, headers=headers, json=data, cookies=account.cookies.dict(),
                                             timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 if api_result.login_expired:
@@ -510,16 +505,15 @@
 
     :param good: 商品对象 / 商品ID，如果指定为商品对象，则会更新商品对象的数据并返回其引用
     :param retry: 是否允许重试
     :return: 商品数据
     """
     good_id = good.goods_id if isinstance(good, Good) else good
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_CHECK_GOOD.format(good_id), timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 # TODO 2023/4/13: 待改成对象方法判断
                 if api_result.message == '商品不存在' or api_result.message == '商品已下架':
                     return GetGoodDetailStatus(good_not_existed=True), None
@@ -527,30 +521,29 @@
                     return GetGoodDetailStatus(success=True), good.update(api_result.data)
                 else:
                     return GetGoodDetailStatus(success=True), Good.parse_obj(api_result.data)
     except tenacity.RetryError as e:
         if is_incorrect_return(e):
             logger.exception(f"米游币商品兑换 - 获取商品详细信息: 服务器没有正确返回")
             logger.debug(f"网络请求返回: {res.text}")
-            GetGoodDetailStatus(incorrect_return=True), None
+            return GetGoodDetailStatus(incorrect_return=True), None
         else:
             logger.exception(f"米游币商品兑换 - 获取商品详细信息: 网络请求失败")
-            GetGoodDetailStatus(network_error=True), None
+            return GetGoodDetailStatus(network_error=True), None
 
 
 async def get_good_games(retry: bool = True) -> Tuple[BaseApiStatus, Optional[List[Tuple[str, str]]]]:
     """
     获取商品分区列表
 
     :param retry: 是否允许重试
     :return: (商品分区全名, 字母简称) 的列表
     """
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_GOOD_LIST.format(page=1,
                                                                 game=""),
                                            headers=HEADERS_GOOD_LIST,
                                            timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
@@ -574,16 +567,15 @@
     :param retry: 是否允许重试
     :return: 商品信息列表
     """
     good_list = []
     page = 1
 
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_GOOD_LIST.format(page=page,
                                                                 game=game), headers=HEADERS_GOOD_LIST,
                                            timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
                 goods = map(Good.parse_obj, api_result.data["list"])
@@ -611,16 +603,15 @@
 
     :param account: 用户账户数据
     :param retry: 是否允许重试
     """
     headers = HEADERS_ADDRESS.copy()
     headers["x-rpc-device_id"] = account.device_id_ios
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_ADDRESS.format(
                         round(NtpTime.time() * 1000)), headers=headers, cookies=account.cookies.dict(),
                         timeout=conf.preference.timeout)
                     api_result = ApiResultHandler(res.json())
                     if api_result.login_expired:
@@ -646,16 +637,15 @@
 
     :param phone_number: 手机号
     :param retry: 是否允许重试
     """
     headers = HEADERS_WEBAPI.copy()
     headers["x-rpc-device_id"] = generate_device_id()
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_REGISTRABLE.format(mobile=phone_number, t=round(NtpTime.time() * 1000)),
                                            headers=headers, timeout=conf.preference.timeout)
                     api_result = ApiResultHandler(res.json())
                 return BaseApiStatus(success=True), bool(api_result.data["is_registable"])
     except tenacity.RetryError as e:
@@ -686,16 +676,15 @@
         time_now = round(NtpTime.time() * 1000)
         await client.options(URL_CREATE_MMT.format(now=time_now, t=time_now),
                              headers=headers, timeout=conf.preference.timeout)
         return await client.get(URL_CREATE_MMT.format(now=time_now, t=time_now),
                                 headers=headers, timeout=conf.preference.timeout)
 
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 if keep_client:
                     client = httpx.AsyncClient()
                     res = await request()
                 else:
                     async with httpx.AsyncClient() as client:
                         res = await request()
@@ -752,16 +741,15 @@
         """
         return await client.post(URL_CREATE_MOBILE_CAPTCHA,
                                  content=encoded_params,
                                  headers=headers,
                                  timeout=conf.preference.timeout)
 
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 # FIXME 2023/4/13: 似乎会导致卡在连接状态，暂时弃用
                 #   res = await client.options(URL_CREATE_MOBILE_CAPTCHA,
                 #                            headers=headers,
                 #                            timeout=conf.preference.timeout)
                 #   cookies.update(res.cookies)
                 if client is not None:
@@ -829,16 +817,15 @@
                                  headers=headers,
                                  content=encoded_params,
                                  cookies=_cookies,
                                  timeout=conf.preference.timeout
                                  )
 
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry),
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 if client is not None:
                     res = await request()
                 else:
                     async with httpx.AsyncClient() as client:
                         res = await request()
                 api_result = ApiResultHandler(res.json())
@@ -876,16 +863,15 @@
     :param retry: 是否允许重试
     """
     if not cookies.login_ticket:
         return GetCookieStatus(missing_login_ticket=True), None
     elif not cookies.bbs_uid:
         return GetCookieStatus(missing_bbs_uid=True), None
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(
                         URL_MULTI_TOKEN_BY_LOGIN_TICKET.format(cookies.login_ticket, cookies.bbs_uid),
                         headers=HEADERS_API_TAKUMI_PC,
                         timeout=conf.preference.timeout)
                 api_result = ApiResultHandler(res.json())
@@ -918,16 +904,15 @@
     :param retry: 是否允许重试
 
     >>> import asyncio
     >>> coroutine = get_cookie_token_by_captcha("12345678910", 123456)
     >>> assert asyncio.new_event_loop().run_until_complete(coroutine)[0].incorrect_captcha is True
     """
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry),
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.post(URL_COOKIE_TOKEN_BY_CAPTCHA,
                                             headers=HEADERS_API_TAKUMI_PC,
                                             json={
                                                 "is_bh2": False,
                                                 "mobile": phone_number,
@@ -981,16 +966,15 @@
         "geetest_validate": geetest_result.validate,
         "geetest_seccode": geetest_result.seccode,
         "source": "user.mihoyo.com",
         "t": round(NtpTime.time() * 1000)
     }
     encoded_params = urlencode(params)
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.post(
                         URL_LOGIN_TICKET_BY_PASSWORD,
                         content=encoded_params,
                         headers=headers,
                         timeout=conf.preference.timeout
@@ -1026,16 +1010,15 @@
     >>> assert asyncio.new_event_loop().run_until_complete(coroutine)[0].success is False
     """
     headers = HEADERS_PASSPORT_API.copy()
     headers["x-rpc-device_id"] = device_id if device_id else generate_device_id()
     if not cookies.stoken_v2:
         return GetCookieStatus(missing_stoken_v2=True), None
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(
                         URL_COOKIE_TOKEN_BY_STOKEN,
                         cookies=cookies.dict(v2_stoken=True, cookie_type=True),
                         headers=headers,
                         timeout=conf.preference.timeout
@@ -1079,16 +1062,15 @@
     headers["x-rpc-device_id"] = device_id if device_id else generate_device_id()
     headers.setdefault("x-rpc-aigis", "")
     headers.setdefault("x-rpc-app_id", "bll8iq97cem8")
 
     if not cookies.stoken_v1:
         return GetCookieStatus(missing_stoken_v1=True), None
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     headers.setdefault("DS", generate_ds(salt=conf.salt_config.SALT_PROD))
                     res = await client.post(
                         URL_STOKEN_V2_BY_V1,
                         cookies={"stoken": cookies.stoken_v1, "stuid": cookies.bbs_uid},
                         headers=headers,
@@ -1133,16 +1115,15 @@
     headers = HEADERS_PASSPORT_API.copy()
     headers["x-rpc-device_id"] = device_id if device_id else generate_device_id()
     if not cookies.stoken_v2:
         return GetCookieStatus(missing_stoken_v2=True), None
     if not cookies.mid:
         return GetCookieStatus(missing_mid=True), None
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry), reraise=True,
-                                                    wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(
                         URL_LTOKEN_BY_STOKEN,
                         cookies=cookies.dict(v2_stoken=True, cookie_type=True),
                         headers=headers,
                         timeout=conf.preference.timeout
@@ -1206,15 +1187,70 @@
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=True, return_data=res.json(), plan=plan)
         else:
             logger.info(
                 f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认。")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=False, return_data=res.json(), plan=plan)
-    except tenacity.RetryError as e:
+    except Exception as e:
+        if is_incorrect_return(e):
+            logger.error(
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回")
+            logger.debug(f"网络请求返回: {res.text}")
+            return ExchangeStatus(incorrect_return=True), None
+        else:
+            logger.exception(
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 请求失败")
+            return ExchangeStatus(network_error=True), None
+
+
+def good_exchange_sync(plan: ExchangePlan) -> Tuple[ExchangeStatus, Optional[ExchangeResult]]:
+    """
+    执行米游币商品兑换
+
+    :param plan: 兑换计划
+    """
+    headers = HEADERS_EXCHANGE
+    headers["x-rpc-device_id"] = plan.account.device_id_ios
+    content = {
+        "app_id": 1,
+        "point_sn": "myb",
+        "goods_id": plan.good.goods_id,
+        "exchange_num": 1,
+    }
+    if plan.address is not None:
+        content.setdefault("address_id", plan.address.id)
+    if plan.game_record is not None:
+        content.setdefault("uid", plan.game_record.game_role_id)
+        # 例: cn_gf01
+        content.setdefault("region", plan.game_record.region)
+        # 例: hk4e_cn
+        content.setdefault("game_biz", plan.good.game_biz)
+    try:
+        with httpx.Client() as client:
+            res = client.post(
+                URL_EXCHANGE, headers=headers, json=content, cookies=plan.account.cookies.dict(),
+                timeout=conf.preference.timeout)
+        api_result = ApiResultHandler(res.json())
+        if api_result.login_expired:
+            logger.info(
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 登录失效")
+            logger.debug(f"网络请求返回: {res.text}")
+            return ExchangeStatus(login_expired=True), None
+        if api_result.success:
+            logger.info(
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换成功！可以自行确认。")
+            logger.debug(f"网络请求返回: {res.text}")
+            return ExchangeStatus(success=True), ExchangeResult(result=True, return_data=res.json(), plan=plan)
+        else:
+            logger.info(
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认。")
+            logger.debug(f"网络请求返回: {res.text}")
+            return ExchangeStatus(success=True), ExchangeResult(result=False, return_data=res.json(), plan=plan)
+    except Exception as e:
         if is_incorrect_return(e):
             logger.error(
                 f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(incorrect_return=True), None
         else:
             logger.exception(
```

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/custom_css.py` & `mys_goods_tool-2.0.3/mys_goods_tool/custom_css.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/custom_widget.py` & `mys_goods_tool-2.0.3/mys_goods_tool/custom_widget.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/data_model.py` & `mys_goods_tool-2.0.3/mys_goods_tool/data_model.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/exchange_plan_view.py` & `mys_goods_tool-2.0.3/mys_goods_tool/exchange_plan_view.py`

 * *Files 0% similar despite different names*

```diff
@@ -330,34 +330,37 @@
     async def _on_mount(self, _: events.Mount):
         # 进度条、刷新按钮
         self.button_refresh.disable()
         self.loading.show()
 
         # 更新商品频道列表
         partition_status, partition_all = await get_good_games()
-        # 过滤掉 "全部" 分区
-        partitions = filter(lambda x: x[1] != "all", partition_all)
+
+        # 刷新按钮、进度条
+        self.button_refresh.enable()
+        self.loading.hide()
+
         if partition_status:
+            # 过滤掉 "全部" 分区
+            partitions = filter(lambda x: x[1] != "all", partition_all)
             for name, abbr in partitions:
                 if abbr not in self.good_dict:
                     # 如果没有商品频道对应值，则进行创建
                     goods_data = self.GoodsDictValue((name, abbr))
                     self.good_dict.setdefault(abbr, goods_data)
                     await self.tabbed_content.append(goods_data.tap_pane)
 
             # 更新每个频道的商品数据
             await self.update_data()
+            return True
         else:
             self.text_view.update("[bold red]⚠ 获取商品频道列表失败，可尝试刷新[/]")
             self.app.notice("[bold red]获取商品频道列表失败！[/]")
             # TODO 待补充各种错误情况
-
-        # 进度条、刷新按钮
-        self.button_refresh.enable()
-        self.loading.hide()
+            return False
 
     def reset_selected(self):
         """
         重置商品选择
         """
         # 刷新选项列表后检查是否为空
         for value in self.good_dict.values():
@@ -393,15 +396,15 @@
                 return
 
             good = good_dict_value.good_list[selected_index]
             GoodsContent.selected_tuple = name, abbr, selected_index
 
             # 获取商品详情
             self.loading.show()
-            good_detail_status, good_detail = await get_good_detail(good)
+            good_detail_status, _ = await get_good_detail(good)
             self.loading.hide()
             if not good_detail_status:
                 # TODO 待补充各种错误情况
                 self.app.notice("[bold red]获取商品详情(game_biz)失败，但你仍然可以尝试进行兑换[/]")
             self.selected = good
 
             # 启用重置按钮
@@ -432,16 +435,19 @@
                 await ExchangePlanView.game_record_content.update_data()
 
         elif event.button.id == "button-goods-refresh":
             # 按下“刷新”按钮时触发的事件
 
             # 在初次加载时，如果获取商品频道信息失败，则此时重新获取
             if not self.good_dict:
-                await self._on_mount(events.Mount())
-            await self.update_data()
+                good_games_result = await self._on_mount(events.Mount())
+            else:
+                good_games_result = True
+            if good_games_result:
+                await self.update_data()
 
         elif event.button.id == "button-goods-reset":
             # 按下“重置”按钮时触发的事件
 
             self.reset_selected()
             self.app.notice("已重置商品选择")
```

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/gt4-localized.html` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/gt4-localized.html`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/gt4.html` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/gt4.html`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/index.html` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/index.html`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/gt.js` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/gt.js`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/gt4.js` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/gt4.js`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/libs/jquery.js` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/libs/jquery.js`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest-webui/localized.html` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest-webui/localized.html`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/geetest.py` & `mys_goods_tool-2.0.3/mys_goods_tool/geetest.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/login_view.py` & `mys_goods_tool-2.0.3/mys_goods_tool/login_view.py`

 * *Files identical despite different names*

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/tui.py` & `mys_goods_tool-2.0.3/mys_goods_tool/tui.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from __future__ import annotations
 
+import sys
 from io import StringIO
 
 from rich.console import RenderableType
 from rich.markdown import Markdown
 from rich.text import Text
 from textual import events
 from textual.app import App, ComposeResult, DEFAULT_COLORS
@@ -400,14 +401,21 @@
             super().write(text)
             TuiApp.text_log.write(text)
 
     def _on_mount(self, _: events.Mount) -> None:
         TuiApp.app = self
         TuiApp.text_log_writer = TuiApp.TextLogWriter()
         logger.add(self.text_log_writer, diagnose=False, level="DEBUG", format=LOG_FORMAT)
+        if sys.platform not in ('win32', 'cygwin', 'cli'):
+            if "uvloop" not in sys.modules.copy():
+                import uvloop
+                import asyncio
+                asyncio.set_event_loop_policy(uvloop.EventLoopPolicy())
+            else:
+                logger.info("在非 Windows 环境下，你可以安装 uvloop 以提高性能")
         self.query_one("Welcome Button", Button).focus()
 
     def action_screenshot(self, filename: str | None = None, path: str = str(ROOT_PATH)) -> None:
         """Save an SVG "screenshot". This action will save an SVG file containing the current contents of the screen.
 
         Args:
             filename: Filename of screenshot, or None to auto-generate. Defaults to None.
```

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/user_data.py` & `mys_goods_tool-2.0.3/mys_goods_tool/user_data.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 
 ROOT_PATH = Path("./")
 """程序所在目录"""
 
 CONFIG_PATH = ROOT_PATH / "user_data.json"
 """用户数据文件默认路径"""
 
-VERSION = "2.0.2"
+VERSION = "2.0.3"
 """程序当前版本"""
 
 if TYPE_CHECKING:
     IntStr = Union[int, str]
     DictStrAny = Dict[str, Any]
     AbstractSetIntStr = AbstractSet[IntStr]
     MappingIntStrAny = Mapping[IntStr, Any]
@@ -408,15 +408,15 @@
 
 
 class UserData(BaseModel):
     """
     用户数据类
     """
     version: str = VERSION
-    """创建用户数据的程序版本号"""
+    """本次修改用户数据文件的程序版本号"""
     exchange_plans: Union[Set[ExchangePlan], List[ExchangePlan]] = set()
     """兑换计划列表"""
     preference: Preference = Preference()
     """偏好设置"""
     salt_config: SaltConfig = SaltConfig()
     """生成Headers - DS所用salt值"""
     device_config: DeviceConfig = DeviceConfig()
```

### Comparing `mys_goods_tool-2.0.2/mys_goods_tool/utils.py` & `mys_goods_tool-2.0.3/mys_goods_tool/utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -33,23 +33,36 @@
 
 
 def custom_attempt_times(retry: bool):
     """
     自定义的重试机制停止条件\n
     根据是否要重试的bool值，给出相应的`tenacity.stop_after_attempt`对象
 
-    :param retry: True - 重试次数达到配置中 MAX_RETRY_TIMES 时停止; False - 执行次数达到1时停止，即不进行重试
+    :param retry: True - 重试次数达到偏好设置中 max_retry_times 时停止; False - 执行次数达到1时停止，即不进行重试
     """
     if retry:
         return tenacity.stop_after_attempt(
             conf.preference.max_retry_times + 1) if conf.preference.max_retry_times else tenacity.stop_after_attempt(1)
     else:
         return tenacity.stop_after_attempt(1)
 
 
+def get_async_retry(retry: bool):
+    """
+    获取异步重试装饰器
+
+    :param retry: True - 重试次数达到偏好设置中 max_retry_times 时停止; False - 执行次数达到1时停止，即不进行重试
+    """
+    return tenacity.AsyncRetrying(
+        stop=custom_attempt_times(retry),
+        retry=tenacity.retry_if_exception_type(BaseException),
+        wait=tenacity.wait_fixed(conf.preference.retry_interval),
+    )
+
+
 class NtpTime:
     """
     NTP时间校准相关
     """
     time_offset = 0
     """本地时间与互联网时间的偏差"""
 
@@ -59,16 +72,15 @@
         校准时间
         """
         if conf.preference.enable_ntp_sync:
             if not conf.preference.ntp_server:
                 logger.error("开启了互联网时间校对，但未配置NTP服务器 preference.ntp_server，放弃时间同步")
                 return False
             try:
-                for attempt in tenacity.Retrying(stop=custom_attempt_times(True), reraise=True,
-                                                 wait=tenacity.wait_fixed(conf.preference.retry_interval)):
+                for attempt in get_async_retry(True):
                     with attempt:
                         cls.time_offset = ntplib.NTPClient().request(
                             conf.preference.ntp_server).tx_time - time.time()
             except tenacity.RetryError:
                 logger.error("校对互联网时间失败，改为使用本地时间")
                 logger.debug(traceback.format_exc())
                 return False
@@ -218,16 +230,15 @@
     下载文件
 
     :param url: 文件URL
     :param retry: 是否允许重试
     :return: 文件数据
     """
     try:
-        async for attempt in tenacity.AsyncRetrying(stop=custom_attempt_times(retry),
-                                                    wait=tenacity.wait_fixed(conf.SLEEP_TIME_RETRY)):
+        async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(url, timeout=conf.preference.timeout, follow_redirects=True)
                 return res.content
     except tenacity.RetryError:
         logger.error(f"下载文件 - {url} 失败")
         logger.debug(f"{traceback.format_exc()}")
@@ -274,15 +285,15 @@
     @classmethod
     async def download(cls) -> bool:
         """
         读取在线配置资源
         :return: 是否成功
         """
         try:
-            for attempt in tenacity.Retrying(stop=custom_attempt_times(True)):
+            for attempt in get_async_retry(True):
                 with attempt:
                     file = await get_file(cls.CONFIG_URL)
                     file = json.loads(file.decode())
                     if not file:
                         return False
                     cls.conf_list = list(
                         filter(lambda co: ..., file))
```

### Comparing `mys_goods_tool-2.0.2/pyproject.toml` & `mys_goods_tool-2.0.3/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "mys-goods-tool"
-version = "2.0.2"
+version = "2.0.3"
 description = "米游社商品兑换工具|短信验证登录|终端TUI界面"
 authors = ["Ljzd-PRO <ljzd@office.ljzd-pro.ml>"]
 readme = "README.md"
 homepage = "https://github.com/Ljzd-PRO/Mys_Goods_Tool"
 repository = "https://github.com/Ljzd-PRO/Mys_Goods_Tool"
 documentation = "https://github.com/Ljzd-PRO/Mys_Goods_Tool/wiki"
 keywords = ["mihoyo", "mihoyobbs", "genshin impact", "textual", "tui"]
@@ -30,26 +30,32 @@
 loguru = "^0.7.0"
 httpx = "^0.24.0"
 rich = "^13.3.5"
 textual = "^0.24.1"
 socksio = "^1.0.0"
 apscheduler = "^3.10.1"
 
+[tool.poetry.group.uvloop.dependencies]
+uvloop = "^0.17.0"
+
 [tool.poetry.group.pyinstaller.dependencies]
 pyinstaller = "==5.10.1"
 
 [tool.poetry.group.test.dependencies]
 pytest = "^7.3.1"
 pytest-html = "^3.2.0"
 pytest-asyncio = "^0.21.0"
 flake8 = "^6.0.0"
 
 [tool.poetry.group.dev.dependencies]
 pydevd-pycharm = "231.8109.197"
 
+[tool.poetry.group.uvloop]
+optional = true
+
 [tool.poetry.group.pyinstaller]
 optional = true
 
 [tool.poetry.group.test]
 optional = true
 
 [tool.poetry.group.dev]
```

### Comparing `mys_goods_tool-2.0.2/PKG-INFO` & `mys_goods_tool-2.0.3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mys-goods-tool
-Version: 2.0.2
+Version: 2.0.3
 Summary: 米游社商品兑换工具|短信验证登录|终端TUI界面
 Home-page: https://github.com/Ljzd-PRO/Mys_Goods_Tool
 Keywords: mihoyo,mihoyobbs,genshin impact,textual,tui
 Author: Ljzd-PRO
 Author-email: ljzd@office.ljzd-pro.ml
 Requires-Python: >=3.9,<3.12
 Classifier: Development Status :: 5 - Production/Stable
@@ -45,18 +45,18 @@
   <img alt="代码行数" src="https://img.shields.io/tokei/lines/github/Ljzd-PRO/Mys_Goods_Tool?style=for-the-badge">
   <img alt="构建结果" src="https://img.shields.io/github/actions/workflow/status/Ljzd-PRO/Mys_Goods_Tool/build-v2.yml?event=pull_request&style=for-the-badge">
   <img alt="Python版本兼容性测试" src="https://img.shields.io/github/actions/workflow/status/Ljzd-PRO/Mys_Goods_Tool/python-package.yml?event=pull_request&label=Versions%20Test&style=for-the-badge">
 </div>
 
 ### 更新说明
 
-- 修复米游社（大别野）等商品分区无商品的问题
-- 修复图形界面兑换模式下不会执行兑换的问题
-- 删除多余的 `pyperclip` 依赖
-- 解决部分商品兑换时间错误的问题
+- 修复定时兑换无效的问题
+- 修复失去网络连接的情况下会导致程序退出的Bug
+- 对于 Linux 使用 Ubuntu 20.04 进行构建，防止出现缺少 GNU libc 对应版本的问题
+- 非 Windows 系统增加 [uvloop](https://github.com/MagicStack/uvloop) 支持，提高性能
 
 ## 功能和特性
 
 - [x] 使用 [Textual](https://github.com/Textualize/textual) 终端图形界面库，支持 Windows / Linux / macOS 甚至可能是移动端SSH客户端
 - [x] 短信验证码登录（只需接收一次验证码）
 - [x] 内置人机验证页面，无需前往官网验证
 - [x] 多账号支持
```

