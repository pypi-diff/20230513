# Comparing `tmp/zerocs-1.2.tar.gz` & `tmp/zerocs-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zerocs-1.2.tar", last modified: Fri May 12 01:14:21 2023, max compression
+gzip compressed data, was "zerocs-1.3.tar", last modified: Sat May 13 02:37:48 2023, max compression
```

## Comparing `zerocs-1.2.tar` & `zerocs-1.3.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.123458 zerocs-1.2/
--rw-r--r--   0 yanping   (1000) yanping   (1000)    18156 2023-05-12 01:14:21.123458 zerocs-1.2/PKG-INFO
--rw-r--r--   0 yanping   (1000) yanping   (1000)       38 2023-05-12 01:14:21.123458 zerocs-1.2/setup.cfg
--rw-r--r--   0 yanping   (1000) yanping   (1000)      867 2023-05-12 01:13:18.000000 zerocs-1.2/setup.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.099459 zerocs-1.2/zerocs/
--rw-r--r--   0 yanping   (1000) yanping   (1000)     4765 2023-04-26 13:53:23.000000 zerocs-1.2/zerocs/__init__.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.107458 zerocs-1.2/zerocs/base/
--rw-r--r--   0 yanping   (1000) yanping   (1000)      134 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/base/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1845 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/base/_base.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     7208 2023-05-12 01:13:18.000000 zerocs-1.2/zerocs/base/_default_func.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      496 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/base/_function.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     2674 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/base/base_.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      529 2023-04-26 13:20:00.000000 zerocs-1.2/zerocs/base/default_func_.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      670 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/base/function_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.111458 zerocs-1.2/zerocs/fork/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       35 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/fork/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1993 2023-04-22 03:18:59.000000 zerocs-1.2/zerocs/fork/_func.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1115 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/fork/fork_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.111458 zerocs-1.2/zerocs/logger/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       41 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/logger/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1860 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/logger/_logger.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      392 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/logger/logger_.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     7354 2023-04-26 13:20:00.000000 zerocs-1.2/zerocs/mate.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.115458 zerocs-1.2/zerocs/network/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       44 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/network/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      425 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/network/_network.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      508 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/network/network_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.115458 zerocs-1.2/zerocs/rabbitmq/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       47 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/rabbitmq/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1288 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/rabbitmq/_rabbitmq.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1293 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/rabbitmq/rabbitmq_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.119458 zerocs-1.2/zerocs/script/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       39 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/script/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1460 2023-04-26 13:20:00.000000 zerocs-1.2/zerocs/script/_queue.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      708 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/script/queue_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.119458 zerocs-1.2/zerocs/snowflakeId/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       55 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/snowflakeId/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     1918 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/snowflakeId/_snowflakeId.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)      469 2023-04-19 11:33:05.000000 zerocs-1.2/zerocs/snowflakeId/snowflakeId.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.123458 zerocs-1.2/zerocs/sqlite/
--rw-r--r--   0 yanping   (1000) yanping   (1000)       42 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/sqlite/__init__.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     5529 2023-04-20 04:53:25.000000 zerocs-1.2/zerocs/sqlite/_sqlite.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)     3577 2023-04-20 03:18:43.000000 zerocs-1.2/zerocs/sqlite/sqlite3_.py
--rw-r--r--   0 yanping   (1000) yanping   (1000)    11546 2023-05-06 12:04:57.000000 zerocs-1.2/zerocs/zerocs_.py
-drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-12 01:14:21.103459 zerocs-1.2/zerocs.egg-info/
--rw-r--r--   0 yanping   (1000) yanping   (1000)    18156 2023-05-12 01:14:20.000000 zerocs-1.2/zerocs.egg-info/PKG-INFO
--rw-r--r--   0 yanping   (1000) yanping   (1000)      943 2023-05-12 01:14:20.000000 zerocs-1.2/zerocs.egg-info/SOURCES.txt
--rw-r--r--   0 yanping   (1000) yanping   (1000)        1 2023-05-12 01:14:20.000000 zerocs-1.2/zerocs.egg-info/dependency_links.txt
--rw-r--r--   0 yanping   (1000) yanping   (1000)       12 2023-05-12 01:14:20.000000 zerocs-1.2/zerocs.egg-info/requires.txt
--rw-r--r--   0 yanping   (1000) yanping   (1000)        7 2023-05-12 01:14:20.000000 zerocs-1.2/zerocs.egg-info/top_level.txt
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.523276 zerocs-1.3/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)    18156 2023-05-13 02:37:48.523276 zerocs-1.3/PKG-INFO
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       38 2023-05-13 02:37:48.523276 zerocs-1.3/setup.cfg
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      867 2023-05-13 02:37:47.000000 zerocs-1.3/setup.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     4765 2023-04-26 13:53:23.000000 zerocs-1.3/zerocs/__init__.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/base/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      134 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/base/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1845 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/base/_base.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     7360 2023-05-13 02:17:44.000000 zerocs-1.3/zerocs/base/_default_func.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      496 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/base/_function.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     2674 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/base/base_.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      529 2023-04-26 13:20:00.000000 zerocs-1.3/zerocs/base/default_func_.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      670 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/base/function_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/fork/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       35 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/fork/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     2567 2023-05-13 02:24:50.000000 zerocs-1.3/zerocs/fork/_func.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1115 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/fork/fork_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/logger/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       41 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/logger/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1860 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/logger/_logger.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      392 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/logger/logger_.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     7545 2023-05-13 02:26:38.000000 zerocs-1.3/zerocs/mate.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/network/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       44 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/network/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      425 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/network/_network.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      508 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/network/network_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs/rabbitmq/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       47 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/rabbitmq/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1288 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/rabbitmq/_rabbitmq.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1293 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/rabbitmq/rabbitmq_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.523276 zerocs-1.3/zerocs/script/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       39 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/script/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1460 2023-04-26 13:20:00.000000 zerocs-1.3/zerocs/script/_queue.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      708 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/script/queue_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.523276 zerocs-1.3/zerocs/snowflakeId/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       55 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/snowflakeId/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     1918 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/snowflakeId/_snowflakeId.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      469 2023-04-19 11:33:05.000000 zerocs-1.3/zerocs/snowflakeId/snowflakeId.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.523276 zerocs-1.3/zerocs/sqlite/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       42 2023-04-20 04:53:25.000000 zerocs-1.3/zerocs/sqlite/__init__.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     5809 2023-05-13 02:31:17.000000 zerocs-1.3/zerocs/sqlite/_sqlite.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)     3834 2023-05-13 02:17:44.000000 zerocs-1.3/zerocs/sqlite/sqlite3_.py
+-rw-r--r--   0 yanping   (1000) yanping   (1000)    11546 2023-05-06 12:04:57.000000 zerocs-1.3/zerocs/zerocs_.py
+drwxr-xr-x   0 yanping   (1000) yanping   (1000)        0 2023-05-13 02:37:48.519276 zerocs-1.3/zerocs.egg-info/
+-rw-r--r--   0 yanping   (1000) yanping   (1000)    18156 2023-05-13 02:37:48.000000 zerocs-1.3/zerocs.egg-info/PKG-INFO
+-rw-r--r--   0 yanping   (1000) yanping   (1000)      943 2023-05-13 02:37:48.000000 zerocs-1.3/zerocs.egg-info/SOURCES.txt
+-rw-r--r--   0 yanping   (1000) yanping   (1000)        1 2023-05-13 02:37:48.000000 zerocs-1.3/zerocs.egg-info/dependency_links.txt
+-rw-r--r--   0 yanping   (1000) yanping   (1000)       12 2023-05-13 02:37:48.000000 zerocs-1.3/zerocs.egg-info/requires.txt
+-rw-r--r--   0 yanping   (1000) yanping   (1000)        7 2023-05-13 02:37:48.000000 zerocs-1.3/zerocs.egg-info/top_level.txt
```

### Comparing `zerocs-1.2/PKG-INFO` & `zerocs-1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zerocs
-Version: 1.2
+Version: 1.3
 Summary: zerocs
 Home-page: https://github.com/ZYPGITA/zerocs
 Author: YanPing
 Author-email: zyphhxx@foxmail.com
 Maintainer: YanPing
 Maintainer-email: zyphhxx@foxmail.com
 License: MIT License
```

### Comparing `zerocs-1.2/setup.py` & `zerocs-1.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='zerocs',
-    version='1.2',
+    version='1.3',
     description="zerocs",
     long_description=open('zerocs/README.rst').read(),
     # long_description_content_type='text/plain',
     include_package_data=True,
     author='YanPing',
     author_email='zyphhxx@foxmail.com',
     maintainer='YanPing',
```

### Comparing `zerocs-1.2/zerocs/__init__.py` & `zerocs-1.3/zerocs/__init__.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/base/_base.py` & `zerocs-1.3/zerocs/base/_base.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/base/_default_func.py` & `zerocs-1.3/zerocs/base/_default_func.py`

 * *Files 2% similar despite different names*

```diff
@@ -84,14 +84,19 @@
         return {"code": 0, "msg": "update service status success"}
 
     @rpc
     def get_task_id(self, service_name, task_id):
         self.sqlite_init()
         return self._sqlite_get_task_id(service_name, task_id)
 
+    @rpc
+    def get_max_work(self, node_ip, service_name):
+        self.sqlite_init()
+        return self._sqlite_get_max_work(node_ip, service_name)
+
 
 class _DefaultFunc(Base, Function, Network):
 
     @rpc
     def update_max_work_num(self, work_num):
         service_name = self.__class__.__dict__['service_name']
         os.environ[f'{service_name}_MAX_WORK'] = f'{work_num}'
```

### Comparing `zerocs-1.2/zerocs/base/base_.py` & `zerocs-1.3/zerocs/base/base_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/base/default_func_.py` & `zerocs-1.3/zerocs/base/default_func_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/base/function_.py` & `zerocs-1.3/zerocs/base/function_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/fork/_func.py` & `zerocs-1.3/zerocs/fork/_func.py`

 * *Files 8% similar despite different names*

```diff
@@ -8,42 +8,53 @@
 import multiprocessing
 from multiprocessing import Process
 
 from nameko.standalone.rpc import ClusterRpcProxy
 
 from zerocs.mate import _Mate
 from zerocs.rabbitmq import RabbitMq
+from zerocs.network import Network
+from zerocs.logger import Logger
 
 
 def run_task(json_data, service, config, res):
     res.append(1)
     service_path = os.getenv('ZERO_FW_SERVICE_PATH')
     module = __import__(f"{service_path}.{service}.{service}",
                         globals=globals(), locals=locals(), fromlist=['WorkFunction'])
     func = module.WorkFunction
     func(service, config, json_data)
     res.pop(0)
 
 
-class _Func(RabbitMq, _Mate):
+class _Func(RabbitMq, Network, Logger, _Mate):
 
     @staticmethod
     def rpc_proxy():
         _config = os.getenv('ZERO_FW_RABBITMQ_CONFIG')
         rpc_obj = ClusterRpcProxy({'AMQP_URI': _config}).start()
         return rpc_obj.zerocs_service
 
+    def _log(self, msg):
+        _path = os.getenv('ZERO_PROJECT_PATH')
+        _file = os.getenv('ZERO_FW_LOGS_PATH')
+        log_path = os.path.join(_path, _file)
+        logger_ = self._logger(self._get_snowflake_id(datacenter_id=0, worker_id=0, did_wid=-1),
+                               log_path, self.service_name)
+        logger_.error(msg)
+
     def _container_start(self, container):
         container.start()
         container.wait()
 
     def _mq_callback(self, ch, method, properties, body):
         ch.basic_ack(delivery_tag=method.delivery_tag)
-        max_work = os.getenv(f'{self.service_name}_MAX_WORK')
+        max_work = self.rpc_proxy().get_max_work(self._node_ip, self.service_name)
         _max_work = int(max_work) if max_work is not None else 1
+        self._log(f'max_work == {_max_work}, res.len == {len(self._res)}')
         task_data = json.loads(body.decode())
         task_id = task_data['task_id']
         all_task_id = self.rpc_proxy().get_task_id(self.service_name, task_id)
         if task_id in all_task_id:
             logging.error(f'task is stop: {task_id}')
         else:
             if len(self._res) < _max_work:
@@ -51,11 +62,12 @@
                 p = Process(target=run_task, args=(task_data, self.service_name, self._config, self._res,))
                 p.start()
             else:
                 ch.basic_publish(body=body, exchange='', routing_key=self.service_name)
 
     def _start_work(self, service_name, config):
         self._config = config
+        self._node_ip = self._get_ipaddr()
         self.service_name = service_name
         self._res = multiprocessing.Manager().list()
         self._rabbitmq_init(config)
         self._get_message(service_name, self._mq_callback)
```

### Comparing `zerocs-1.2/zerocs/fork/fork_.py` & `zerocs-1.3/zerocs/fork/fork_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/logger/_logger.py` & `zerocs-1.3/zerocs/logger/_logger.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/mate.py` & `zerocs-1.3/zerocs/mate.py`

 * *Files 2% similar despite different names*

```diff
@@ -284,20 +284,28 @@
         """
         get Task ID stopped
         :param service_name:
         :param task_id: task id
         :return:
         """
 
+    def _sqlite_get_max_work(self, node_ip, service_name):
+        """
+        get Task ID stopped
+        :param service_name:
+        :param node_ip: node_ip
+        :return:
+        """
+
     def _sqlite_insert_task_id(self, service_name, task_id):
         """
         insert Task ID stopped
         :param service_name:
         :param task_id:
         :return:
         """
 
     def _sqlite_get_all_task_id(self):
         """
         Get All stop task
         :return:
-        """
+        """
```

### Comparing `zerocs-1.2/zerocs/rabbitmq/_rabbitmq.py` & `zerocs-1.3/zerocs/rabbitmq/_rabbitmq.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/rabbitmq/rabbitmq_.py` & `zerocs-1.3/zerocs/rabbitmq/rabbitmq_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/script/_queue.py` & `zerocs-1.3/zerocs/script/_queue.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/script/queue_.py` & `zerocs-1.3/zerocs/script/queue_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/snowflakeId/_snowflakeId.py` & `zerocs-1.3/zerocs/snowflakeId/_snowflakeId.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs/sqlite/_sqlite.py` & `zerocs-1.3/zerocs/sqlite/_sqlite.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,17 +11,17 @@
 class _SqlIte(_Mate):
 
     def _connect_db(self, db_file):
         self._conn = sqlite3.connect(db_file)
         self._cursor = self._conn.cursor()
 
     def _execute(self, _sql):
-        ZERO_PROJECT_PATH = os.getenv('ZERO_PROJECT_PATH')
-        ZERO_FW_DB_FILE = os.getenv('ZERO_FW_DB_FILE')
-        db_file = os.path.join(ZERO_PROJECT_PATH, ZERO_FW_DB_FILE)
+        _path = os.getenv('ZERO_PROJECT_PATH')
+        _file = os.getenv('ZERO_FW_DB_FILE')
+        db_file = os.path.join(_path, _file)
         self._connect_db(db_file)
         return self._cursor.execute(_sql)
 
     def _is_table(self, table_name):
         _sql = f"SELECT count(*) FROM sqlite_master WHERE type='table' AND name='{table_name}';"
         cursor = self._execute(_sql)
         for i in cursor:
@@ -132,14 +132,23 @@
         cursor = self._execute(_sql)
 
         task_ids = []
         for i in list(cursor):
             task_ids.append(i[1])
         return task_ids
 
+    def _sqlite_get_max_work(self, node_ip, service_name):
+        _sql = f"""SELECT * FROM SYSTEMINFO WHERE SERVICE_NAME="{service_name}" AND NODE_IP="{node_ip}"; """
+        cursor = self._execute(_sql)
+
+        _max_work = []
+        for i in list(cursor):
+            _max_work.append(i[1])
+        return _max_work[0]
+
     def _sqlite_insert_task_id(self, service_name, task_id):
         if len(self._sqlite_get_task_id(service_name, task_id)) < 1:
             _sql = f"""INSERT INTO TASKID (SERVICE_NAME,TASK_ID) VALUES ("{service_name}", "{task_id}")"""
         else:
             _sql = f""""""
 
         self._execute(_sql)
```

### Comparing `zerocs-1.2/zerocs/sqlite/sqlite3_.py` & `zerocs-1.3/zerocs/sqlite/sqlite3_.py`

 * *Files 2% similar despite different names*

```diff
@@ -104,14 +104,23 @@
         get Task ID stopped
         :param service_name:
         :param task_id: task id
         :return:
         """
         return super()._sqlite_get_task_id(service_name, task_id)
 
+    def _sqlite_get_max_work(self, node_ip, service_name):
+        """
+        get Task ID stopped
+        :param service_name:
+        :param node_ip: node_ip
+        :return:
+        """
+        return super()._sqlite_get_max_work(node_ip, service_name)
+
     def _sqlite_insert_task_id(self, service_name, task_id):
         """
         insert Task ID stopped
         :param service_name:
         :param task_id:
         :return:
         """
```

### Comparing `zerocs-1.2/zerocs/zerocs_.py` & `zerocs-1.3/zerocs/zerocs_.py`

 * *Files identical despite different names*

### Comparing `zerocs-1.2/zerocs.egg-info/PKG-INFO` & `zerocs-1.3/zerocs.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zerocs
-Version: 1.2
+Version: 1.3
 Summary: zerocs
 Home-page: https://github.com/ZYPGITA/zerocs
 Author: YanPing
 Author-email: zyphhxx@foxmail.com
 Maintainer: YanPing
 Maintainer-email: zyphhxx@foxmail.com
 License: MIT License
```

### Comparing `zerocs-1.2/zerocs.egg-info/SOURCES.txt` & `zerocs-1.3/zerocs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

