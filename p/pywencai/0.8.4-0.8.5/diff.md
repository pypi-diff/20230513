# Comparing `tmp/pywencai-0.8.4.tar.gz` & `tmp/pywencai-0.8.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pywencai-0.8.4.tar", max compression
+gzip compressed data, was "pywencai-0.8.5.tar", max compression
```

## Comparing `pywencai-0.8.4.tar` & `pywencai-0.8.5.tar`

### file list

```diff
@@ -1,8 +1,9 @@
--rw-r--r--   0        0        0     1062 2023-05-11 04:59:27.411391 pywencai-0.8.4/LICENSE
--rw-r--r--   0        0        0     2446 2023-05-11 04:59:27.411391 pywencai-0.8.4/README.md
--rw-r--r--   0        0        0      612 2023-05-11 04:59:27.411391 pywencai-0.8.4/pyproject.toml
--rw-r--r--   0        0        0       23 2023-05-11 04:59:27.411391 pywencai-0.8.4/pywencai/__init__.py
--rw-r--r--   0        0        0     3559 2023-05-11 04:59:27.411391 pywencai-0.8.4/pywencai/convert.py
--rw-r--r--   0        0        0    39677 2023-05-11 04:59:27.411391 pywencai-0.8.4/pywencai/hexin-v.js
--rw-r--r--   0        0        0     4477 2023-05-11 04:59:27.415391 pywencai-0.8.4/pywencai/wencai.py
--rw-r--r--   0        0        0     3070 1970-01-01 00:00:00.000000 pywencai-0.8.4/PKG-INFO
+-rw-r--r--   0        0        0     1062 2023-05-13 06:17:17.135331 pywencai-0.8.5/LICENSE
+-rw-r--r--   0        0        0     2836 2023-05-13 06:17:17.135331 pywencai-0.8.5/README.md
+-rw-r--r--   0        0        0      612 2023-05-13 06:17:17.135331 pywencai-0.8.5/pyproject.toml
+-rw-r--r--   0        0        0       23 2023-05-13 06:17:17.135331 pywencai-0.8.5/pywencai/__init__.py
+-rw-r--r--   0        0        0     4746 2023-05-13 06:17:17.135331 pywencai-0.8.5/pywencai/convert.py
+-rw-r--r--   0        0        0      433 2023-05-13 06:17:17.135331 pywencai-0.8.5/pywencai/headers.py
+-rw-r--r--   0        0        0    39677 2023-05-13 06:17:17.135331 pywencai-0.8.5/pywencai/hexin-v.js
+-rw-r--r--   0        0        0     4083 2023-05-13 06:17:17.135331 pywencai-0.8.5/pywencai/wencai.py
+-rw-r--r--   0        0        0     3460 1970-01-01 00:00:00.000000 pywencai-0.8.5/PKG-INFO
```

### Comparing `pywencai-0.8.4/LICENSE` & `pywencai-0.8.5/LICENSE`

 * *Files identical despite different names*

### Comparing `pywencai-0.8.4/README.md` & `pywencai-0.8.5/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -93,14 +93,23 @@
 
 非必填，默认为Flase，是否在控制台打印日志。
 
 #### cookie
 
 非必填，默认为None，付费版可以尝试传入cookie，获取付费使用权限。
 
+#### request_params
+
+非必填，默认为`{}`，可以设置额外的request参数
+
+```python
+pywencai.get(question='昨日涨幅', sort_order='asc', loop=True, log=True, request_params={ 'proxies': proxies, 'timeout': (5, 10) })
+```
+> 具体参数参看：[https://requests.readthedocs.io/en/latest/api/#requests.request](https://requests.readthedocs.io/en/latest/api/#requests.request)
+
 ### 返回值
 
 当查询的是列表时，该方法返回一个`pandas`的`Dataframe`
 
 当查询的是详情是，该方法返回一个字典，字典中可能包含若干个文本和`Dataframe`
 
 ## 联系方式
```

### Comparing `pywencai-0.8.4/pyproject.toml` & `pywencai-0.8.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "pywencai"
-version = "0.8.4"
+version = "0.8.5"
 description = ""
 authors = ["pluto <mayuanchi1029@gmail.com>"]
 readme = "README.md"
 
 [[tool.poetry.source]]
 name = "tsinghua"
 url = "https://pypi.tuna.tsinghua.edu.cn/simple/"
```

### Comparing `pywencai-0.8.4/pywencai/hexin-v.js` & `pywencai-0.8.5/pywencai/hexin-v.js`

 * *Files identical despite different names*

### Comparing `pywencai-0.8.4/pywencai/wencai.py` & `pywencai-0.8.5/pywencai/wencai.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,55 +1,42 @@
-import os
-import execjs
 import json
 import requests as rq
 import pandas as pd
 import time
 import logging
-from fake_useragent import UserAgent
-from pywencai.convert import convert_params
 import pydash as _
-
-ua = UserAgent()
+from pywencai.convert import convert
+from pywencai.headers import headers
 
 logging.basicConfig(
     level=logging.INFO,
     format='[pywencai] %(asctime)s - %(levelname)s - %(message)s'
 )
 
-
-def get_token():
-    '''获取token'''
-    with open(os.path.join(os.path.dirname(__file__), 'hexin-v.js'), 'r') as f:
-        jscontent = f.read()
-    context = execjs.compile(jscontent)
-    return context.call("v")
-
-
 def while_do(do, retry=10, sleep=0, log=False):
     count = 0
     while count < retry:
         time.sleep(sleep)
         try:
             return do()
         except:
             log and logging.warning(f'{count+1}次尝试失败')
             count += 1
-    # log and logging.info(f'获取get_robot_data失败')
     return None
 
 
 def get_robot_data(**kwargs):
     '''获取condition'''
     retry = kwargs.get('retry', 10)
     sleep = kwargs.get('sleep', 0)
     question = kwargs.get('query')
     log = kwargs.get('log', False)
     query_type = kwargs.get('query_type', 'stock')
     cookie = kwargs.get('cookie', None)
+    request_params = kwargs.get('request_params', {})
     data = {
         'perpage': 10,
         'page': 1,
         'source': 'Ths_iwencai_Xuangu',
         'secondary_intent': query_type,
         'question': question
     }
@@ -58,21 +45,18 @@
     log and logging.info(f'获取condition开始')
 
     def do():
         res = rq.request(
             method='POST',
             url='http://www.iwencai.com/customized/chart/get-robot-data',
             json=data,
-            headers={
-                'hexin-v': get_token(),
-                'User-Agent': ua.random,
-                'cookie': cookie
-            }
+            headers=headers(cookie),
+            **request_params
         )
-        params = convert_params(res)
+        params = convert(res)
         log and logging.info(f'获取get_robot_data成功')
         return params
 
     result = while_do(do, retry, sleep, log)
 
     if result is None:
         log and logging.info(f'获取get_robot_data失败')
@@ -92,14 +76,15 @@
 
 def get_page(**kwargs):
     '''获取每页数据'''
     retry = kwargs.pop('retry', 10)
     sleep = kwargs.pop('sleep', 0)
     log = kwargs.pop('log', False)
     cookie = kwargs.pop('cookie', None)
+    request_params = kwargs.get('request_params', {})
 
     data = {
         'perpage': 100,
         'page': 1,
         'source': 'Ths_iwencai_Xuangu',
         **kwargs
     }
@@ -107,20 +92,17 @@
     log and logging.info(f'第{data.get("page")}页开始')
 
     def do():
         res = rq.request(
             method='POST',
             url='http://www.iwencai.com/gateway/urp/v7/landing/getDataList',
             data=data,
-            headers={
-                'hexin-v': get_token(),
-                'User-Agent': ua.random,
-                'cookie': cookie
-            },
-            timeout=(5, 10)
+            headers=headers(cookie),
+            timeout=(5, 10),
+            **request_params
         )
         result = json.loads(res.text)
         list = result['answer']['components'][0]['data']['datas']
         log and logging.info(f'第{data.get("page")}页成功')
         return pd.DataFrame.from_dict(list)
     
     result = while_do(do, retry, sleep, log)
```

### Comparing `pywencai-0.8.4/PKG-INFO` & `pywencai-0.8.5/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pywencai
-Version: 0.8.4
+Version: 0.8.5
 Summary: 
 Author: pluto
 Author-email: mayuanchi1029@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -112,14 +112,23 @@
 
 非必填，默认为Flase，是否在控制台打印日志。
 
 #### cookie
 
 非必填，默认为None，付费版可以尝试传入cookie，获取付费使用权限。
 
+#### request_params
+
+非必填，默认为`{}`，可以设置额外的request参数
+
+```python
+pywencai.get(question='昨日涨幅', sort_order='asc', loop=True, log=True, request_params={ 'proxies': proxies, 'timeout': (5, 10) })
+```
+> 具体参数参看：[https://requests.readthedocs.io/en/latest/api/#requests.request](https://requests.readthedocs.io/en/latest/api/#requests.request)
+
 ### 返回值
 
 当查询的是列表时，该方法返回一个`pandas`的`Dataframe`
 
 当查询的是详情是，该方法返回一个字典，字典中可能包含若干个文本和`Dataframe`
 
 ## 联系方式
```

