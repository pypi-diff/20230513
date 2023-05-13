# Comparing `tmp/torchility-0.6.6.tar.gz` & `tmp/torchility-0.6.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "torchility-0.6.6.tar", last modified: Fri May  5 13:47:18 2023, max compression
+gzip compressed data, was "torchility-0.6.7.tar", last modified: Sat May 13 05:21:56 2023, max compression
```

## Comparing `torchility-0.6.6.tar` & `torchility-0.6.7.tar`

### file list

```diff
@@ -1,37 +1,38 @@
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.445943 torchility-0.6.6/
--rw-r--r--   0 liuchen    (501) staff       (20)     1073 2020-01-28 04:19:18.000000 torchility-0.6.6/LICENSE
--rw-r--r--   0 liuchen    (501) staff       (20)     2074 2023-05-05 13:47:18.445508 torchility-0.6.6/PKG-INFO
--rw-r--r--   0 liuchen    (501) staff       (20)     1595 2023-03-20 06:35:45.000000 torchility-0.6.6/README.md
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.430550 torchility-0.6.6/examples/
--rw-r--r--   0 liuchen    (501) staff       (20)     1675 2023-03-27 12:31:34.000000 torchility-0.6.6/examples/1-mnist.py
--rw-r--r--   0 liuchen    (501) staff       (20)     2663 2023-03-28 13:54:47.000000 torchility-0.6.6/examples/2-mnist_callbacks.py
--rw-r--r--   0 liuchen    (501) staff       (20)     2223 2023-05-05 13:45:53.000000 torchility-0.6.6/examples/3-mnist_interpreter.py
--rw-r--r--   0 liuchen    (501) staff       (20)     1709 2022-03-31 07:25:03.000000 torchility-0.6.6/examples/4-mnist_model_analysis.py
--rw-r--r--   0 liuchen    (501) staff       (20)     1419 2022-05-28 01:44:42.000000 torchility-0.6.6/examples/5-mnist_lr_find.py
--rw-r--r--   0 liuchen    (501) staff       (20)     1962 2022-12-09 04:27:52.000000 torchility-0.6.6/examples/6-graph_node_clasification_DGL.py
--rw-r--r--   0 liuchen    (501) staff       (20)       38 2023-05-05 13:47:18.446202 torchility-0.6.6/setup.cfg
--rw-r--r--   0 liuchen    (501) staff       (20)     1117 2023-05-05 12:13:44.000000 torchility-0.6.6/setup.py
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.435544 torchility-0.6.6/torchility/
--rw-r--r--   0 liuchen    (501) staff       (20)      503 2023-05-05 13:44:59.000000 torchility-0.6.6/torchility/__init__.py
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.441932 torchility-0.6.6/torchility/callbacks/
--rw-r--r--   0 liuchen    (501) staff       (20)      101 2022-05-08 12:50:22.000000 torchility-0.6.6/torchility/callbacks/__init__.py
--rw-r--r--   0 liuchen    (501) staff       (20)     1153 2023-03-28 13:49:32.000000 torchility-0.6.6/torchility/callbacks/common.py
--rw-r--r--   0 liuchen    (501) staff       (20)     4840 2023-05-05 13:46:18.000000 torchility-0.6.6/torchility/callbacks/interpreters.py
--rw-r--r--   0 liuchen    (501) staff       (20)     3036 2023-03-19 07:43:59.000000 torchility-0.6.6/torchility/callbacks/performances.py
--rw-r--r--   0 liuchen    (501) staff       (20)    10012 2023-03-19 09:26:35.000000 torchility-0.6.6/torchility/callbacks/progress.py
--rw-r--r--   0 liuchen    (501) staff       (20)     2390 2021-06-09 14:49:55.000000 torchility-0.6.6/torchility/hooks.py
--rw-r--r--   0 liuchen    (501) staff       (20)      577 2021-06-10 07:05:35.000000 torchility-0.6.6/torchility/losses.py
--rw-r--r--   0 liuchen    (501) staff       (20)     4932 2023-03-28 13:36:07.000000 torchility-0.6.6/torchility/metrics.py
--rw-r--r--   0 liuchen    (501) staff       (20)     5971 2023-03-28 13:41:27.000000 torchility-0.6.6/torchility/tasks.py
--rw-r--r--   0 liuchen    (501) staff       (20)    11360 2023-03-28 13:33:59.000000 torchility-0.6.6/torchility/trainer.py
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.444491 torchility-0.6.6/torchility/utils/
--rw-r--r--   0 liuchen    (501) staff       (20)       68 2022-06-01 16:09:54.000000 torchility-0.6.6/torchility/utils/__init__.py
--rw-r--r--   0 liuchen    (501) staff       (20)     4222 2022-06-02 14:28:56.000000 torchility-0.6.6/torchility/utils/plots.py
--rw-r--r--   0 liuchen    (501) staff       (20)     6050 2023-05-05 01:14:22.000000 torchility-0.6.6/torchility/utils/utils.py
--rw-r--r--   0 liuchen    (501) staff       (20)     3014 2022-08-04 03:32:03.000000 torchility-0.6.6/torchility/utils/yaml_config.py
-drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-05 13:47:18.438630 torchility-0.6.6/torchility.egg-info/
--rw-r--r--   0 liuchen    (501) staff       (20)     2074 2023-05-05 13:47:18.000000 torchility-0.6.6/torchility.egg-info/PKG-INFO
--rw-r--r--   0 liuchen    (501) staff       (20)      795 2023-05-05 13:47:18.000000 torchility-0.6.6/torchility.egg-info/SOURCES.txt
--rw-r--r--   0 liuchen    (501) staff       (20)        1 2023-05-05 13:47:18.000000 torchility-0.6.6/torchility.egg-info/dependency_links.txt
--rw-r--r--   0 liuchen    (501) staff       (20)       83 2023-05-05 13:47:18.000000 torchility-0.6.6/torchility.egg-info/requires.txt
--rw-r--r--   0 liuchen    (501) staff       (20)       11 2023-05-05 13:47:18.000000 torchility-0.6.6/torchility.egg-info/top_level.txt
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.981634 torchility-0.6.7/
+-rw-r--r--   0 liuchen    (501) staff       (20)     1073 2020-01-28 04:19:18.000000 torchility-0.6.7/LICENSE
+-rw-r--r--   0 liuchen    (501) staff       (20)     2074 2023-05-13 05:21:56.979591 torchility-0.6.7/PKG-INFO
+-rw-r--r--   0 liuchen    (501) staff       (20)     1595 2023-03-20 06:35:45.000000 torchility-0.6.7/README.md
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.952404 torchility-0.6.7/examples/
+-rw-r--r--   0 liuchen    (501) staff       (20)     1740 2023-05-13 04:54:21.000000 torchility-0.6.7/examples/1-mnist.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     2663 2023-03-28 13:54:47.000000 torchility-0.6.7/examples/2-mnist_callbacks.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     2223 2023-05-05 13:48:59.000000 torchility-0.6.7/examples/3-mnist_interpreter.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     1709 2022-03-31 07:25:03.000000 torchility-0.6.7/examples/4-mnist_model_analysis.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     1419 2022-05-28 01:44:42.000000 torchility-0.6.7/examples/5-mnist_lr_find.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     1962 2022-12-09 04:27:52.000000 torchility-0.6.7/examples/6-graph_node_clasification_DGL.py
+-rw-r--r--   0 liuchen    (501) staff       (20)       38 2023-05-13 05:21:56.982057 torchility-0.6.7/setup.cfg
+-rw-r--r--   0 liuchen    (501) staff       (20)     1117 2023-05-05 12:13:44.000000 torchility-0.6.7/setup.py
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.961636 torchility-0.6.7/torchility/
+-rw-r--r--   0 liuchen    (501) staff       (20)      503 2023-05-13 05:20:50.000000 torchility-0.6.7/torchility/__init__.py
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.969753 torchility-0.6.7/torchility/callbacks/
+-rw-r--r--   0 liuchen    (501) staff       (20)      101 2022-05-08 12:50:22.000000 torchility-0.6.7/torchility/callbacks/__init__.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     1153 2023-03-28 13:49:32.000000 torchility-0.6.7/torchility/callbacks/common.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     4840 2023-05-05 13:46:18.000000 torchility-0.6.7/torchility/callbacks/interpreters.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     3036 2023-03-19 07:43:59.000000 torchility-0.6.7/torchility/callbacks/performances.py
+-rw-r--r--   0 liuchen    (501) staff       (20)    10012 2023-03-19 09:26:35.000000 torchility-0.6.7/torchility/callbacks/progress.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     1022 2023-05-13 05:20:20.000000 torchility-0.6.7/torchility/datamodule.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     2390 2021-06-09 14:49:55.000000 torchility-0.6.7/torchility/hooks.py
+-rw-r--r--   0 liuchen    (501) staff       (20)      577 2021-06-10 07:05:35.000000 torchility-0.6.7/torchility/losses.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     4932 2023-03-28 13:36:07.000000 torchility-0.6.7/torchility/metrics.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     5971 2023-03-28 13:41:27.000000 torchility-0.6.7/torchility/tasks.py
+-rw-r--r--   0 liuchen    (501) staff       (20)    12337 2023-05-13 05:03:46.000000 torchility-0.6.7/torchility/trainer.py
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.976960 torchility-0.6.7/torchility/utils/
+-rw-r--r--   0 liuchen    (501) staff       (20)       68 2022-06-01 16:09:54.000000 torchility-0.6.7/torchility/utils/__init__.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     4222 2022-06-02 14:28:56.000000 torchility-0.6.7/torchility/utils/plots.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     6050 2023-05-05 01:14:22.000000 torchility-0.6.7/torchility/utils/utils.py
+-rw-r--r--   0 liuchen    (501) staff       (20)     3014 2022-08-04 03:32:03.000000 torchility-0.6.7/torchility/utils/yaml_config.py
+drwxr-xr-x   0 liuchen    (501) staff       (20)        0 2023-05-13 05:21:56.965266 torchility-0.6.7/torchility.egg-info/
+-rw-r--r--   0 liuchen    (501) staff       (20)     2074 2023-05-13 05:21:56.000000 torchility-0.6.7/torchility.egg-info/PKG-INFO
+-rw-r--r--   0 liuchen    (501) staff       (20)      820 2023-05-13 05:21:56.000000 torchility-0.6.7/torchility.egg-info/SOURCES.txt
+-rw-r--r--   0 liuchen    (501) staff       (20)        1 2023-05-13 05:21:56.000000 torchility-0.6.7/torchility.egg-info/dependency_links.txt
+-rw-r--r--   0 liuchen    (501) staff       (20)       83 2023-05-13 05:21:56.000000 torchility-0.6.7/torchility.egg-info/requires.txt
+-rw-r--r--   0 liuchen    (501) staff       (20)       11 2023-05-13 05:21:56.000000 torchility-0.6.7/torchility.egg-info/top_level.txt
```

### Comparing `torchility-0.6.6/LICENSE` & `torchility-0.6.7/LICENSE`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/PKG-INFO` & `torchility-0.6.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchility
-Version: 0.6.6
+Version: 0.6.7
 Summary: UNKNOWN
 Home-page: https://github.com/hitlic/torchility
 Author: hitlic
 Author-email: liuchen.lic@gmail.com
 License: MIT
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `torchility-0.6.6/README.md` & `torchility-0.6.7/README.md`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/examples/1-mnist.py` & `torchility-0.6.7/examples/1-mnist.py`

 * *Files 3% similar despite different names*

```diff
@@ -14,15 +14,14 @@
 mnist_full = MNIST(data_dir, train=True, transform=transform, download=True)
 train_ds, val_ds = random_split(mnist_full, [55000, 5000])
 test_ds = MNIST(data_dir, train=False, transform=transform, download=True)
 train_dl = DataLoader(train_ds, batch_size=32)
 val_dl = DataLoader(val_ds, batch_size=32)
 test_dl = DataLoader(test_ds, batch_size=32)
 
-
 # 2. --- 模型
 channels, width, height = (1, 28, 28)
 model = nn.Sequential(
     nn.Flatten(),
     nn.Linear(channels * width * height, 64),
     nn.ReLU(),
     nn.Dropout(0.1),
@@ -34,18 +33,18 @@
 
 
 # 3. --- 优化器
 opt = torch.optim.Adam(model.parameters(), lr=2e-4)
 
 
 # 4. --- 训练
-trainer = Trainer(model, F.cross_entropy, opt, epochs=2)            # 训练器
+trainer = Trainer(model, F.cross_entropy, opt, epochs=2, logger=False, reset_dl=1)            # 训练器
 trainer.fit(train_dl, val_dl)                                       # 训练、验证
 trainer.test(test_dl)                                               # 测试
-
+trainer.predict(test_dl, has_label=True)
 
 """ 使用GPU
 # 默认情况下自动选择可用的GPU，如下两种形式相同
 trainer = Trainer()
 trainer = Trainer(accelerator="auto", devices="auto", strategy="auto") 
 
 # 使用一个GPU
```

### Comparing `torchility-0.6.6/examples/2-mnist_callbacks.py` & `torchility-0.6.7/examples/2-mnist_callbacks.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/examples/3-mnist_interpreter.py` & `torchility-0.6.7/examples/3-mnist_interpreter.py`

 * *Files 0% similar despite different names*

```diff
@@ -43,15 +43,15 @@
 # 4. --- 训练
 
 # 要计算每个样本的指标，因此不能reduction（即求和、平均等操作）
 metric = nn.CrossEntropyLoss(reduction='none')
 
 interpreter = ClassifierInterpreter(metric=metric, k=15, class_num=10, stage='test')          # 针对分类模型测试数据的解释器
 trainer = Trainer(model, F.cross_entropy, opt,                           # 训练器
-                  epochs=1, callbacks=[interpreter])
+                  epochs=5, callbacks=[interpreter])
 trainer.fit(train_dl, val_dl)                                            # 训练、验证
 trainer.test(test_dl)                                                    # 测试
 
 
 # 5. --- 解释
 
 # 返回测试集中损失最大的k个样本的信息
```

### Comparing `torchility-0.6.6/examples/4-mnist_model_analysis.py` & `torchility-0.6.7/examples/4-mnist_model_analysis.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/examples/5-mnist_lr_find.py` & `torchility-0.6.7/examples/5-mnist_lr_find.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/examples/6-graph_node_clasification_DGL.py` & `torchility-0.6.7/examples/6-graph_node_clasification_DGL.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/setup.py` & `torchility-0.6.7/setup.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/callbacks/common.py` & `torchility-0.6.7/torchility/callbacks/common.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/callbacks/interpreters.py` & `torchility-0.6.7/torchility/callbacks/interpreters.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/callbacks/performances.py` & `torchility-0.6.7/torchility/callbacks/performances.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/callbacks/progress.py` & `torchility-0.6.7/torchility/callbacks/progress.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/hooks.py` & `torchility-0.6.7/torchility/hooks.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/losses.py` & `torchility-0.6.7/torchility/losses.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/metrics.py` & `torchility-0.6.7/torchility/metrics.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/tasks.py` & `torchility-0.6.7/torchility/tasks.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/trainer.py` & `torchility-0.6.7/torchility/trainer.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,46 +11,49 @@
 from torchmetrics import Metric
 
 from .callbacks import ResetMetrics, SimpleBar
 from .metrics import MetricBase
 from .tasks import GeneralTaskModule
 from .callbacks import Progress
 from .utils import batches
+from .datamodule import GeneralDataModule
 
 def default_args(func):
     signature = inspect.signature(func)
     return {
         k: v.default
         for k, v in signature.parameters.items()
         if v.default is not inspect.Parameter.empty
     }
 
 class Trainer(PLTrainer):
     def __init__(self, model:torch.nn.Module=None,  # pytorch Module
         loss:Callable=None,                         # loss function
         optimizer:torch.optim.Optimizer=None,       # pytorch optimizer
-        epochs=None,                                # max epochs
+        epochs:int=None,                            # max epochs
         metrics:Union[Callable, Metric]=(),         # instance of torchmetrics.Metric or other callable instance
         task_module: LightningModule=None,          # task_model
         datamodule: LightningDataModule = None,     # PL data module
-        default_bar=False,  # 是否使用默认进度条
-        task_kwargs=dict(),                         # parameters of the task_module
+        default_bar=False,                          # 是否使用默认进度条
+        reset_dl:int=0,                             # 每隔多个少epoch重置一次训练DataLoader，与reload_dataloaders_every_n_epochs相似
+        task_kwargs:dict=None,                      # parameters dict of the task_module
         **pltrainer_kwargs                          # keyword arguments of pytorch_lightning Trainer
         ):
 
         self.init_params = default_args(PLTrainer)
         self.progress = None
         self.best_model = None   # 训练中最好的torch模型
 
         #   *************************************
         #   *    Task Configuration    --- LIC  *
         #   *************************************
 
         metrics = self._prepare_metrics(metrics)
         if task_module is None:
+            task_kwargs = task_kwargs if task_kwargs is not None else {}
             self.task_module = GeneralTaskModule(model, loss, optimizer, metrics, **task_kwargs)
         else:
             self.task_module = task_module
         self.datamodule = datamodule
 
         #   *************************************
         #   *    Trainer Parameters    --- LIC  *
@@ -72,19 +75,24 @@
             if not any([isinstance(cbk, ProgressBar) for cbk in cbks]):
                 cbks.append(SimpleBar())  # ResetMetrics must stay before SimpleBar
         self.init_params['callbacks'] = cbks
 
         # === default logger
         if self.init_params['logger'] is None or self.init_params['logger'] == True:
             if self.init_params['default_root_dir'] is None:
-                log_dir = 'logs'
+                log_dir = 'torchility_logs'
             else:
                 log_dir = self.init_params['default_root_dir']
             self.init_params['logger'] = TensorBoardLogger(log_dir, name=None, log_graph=True, default_hp_metric=False)
 
+        # === reset dataloader
+        self.reset_dl = reset_dl
+        if reset_dl > 0:
+            self.init_params['reload_dataloaders_every_n_epochs'] = reset_dl
+
         super().__init__(**self.init_params)
 
     def _prepare_metrics(self, metrics, just_for_test=False):
         metrics_ready = {'train': [], 'val':[], 'test':[]}
         for m in metrics:
             if isinstance(m, (tuple, list)):  # when m is (metric_name, metric)
                 assert len(m) == 2, '`metric` should be a tuple of (metric_name, metric_callable)'
@@ -112,41 +120,47 @@
                     metrics_ready['test'].append(MetricBase(m, name))
         return metrics_ready if not just_for_test else metrics_ready['test']
 
     def fit(self, train_dl=None, val_dl=None, epochs=None, ckpt_path=None):
         if self.datamodule:
             super().fit(self.task_module, datamodule=self.datamodule, ckpt_path=ckpt_path)
         else:
-            super().fit(self.task_module, train_dataloaders=train_dl, val_dataloaders=val_dl, ckpt_path=ckpt_path)
+            dm = GeneralDataModule(train_dl=train_dl, val_dl=val_dl, reset=self.reset_dl)
+            # super().fit(self.task_module, train_dataloaders=train_dl, val_dataloaders=val_dl, ckpt_path=ckpt_path)
+            super().fit(self.task_module, datamodule=dm, ckpt_path=ckpt_path)
         return self.progress
 
     def test(self, test_dl=None, ckpt_path='best', verbose=True, metrics=None, do_loss=True):  # pylint: disable=arguments-renamed
         """
         Args:
             metrics: 一旦提供了test的metrics，则会将trainer中用于test的metrics覆盖，也就是说可以指定仅用于test的metrics
             do_loss: 在测试时是否计算损失函数，当测试任务和训练任务数据不一致无法计算损失函数时，可设do_loss=False
         """
         self.task_module.do_test_loss = do_loss
         if metrics is not None:  # 如果提供了仅用于test的metrics
             test_metrics = self._prepare_metrics(metrics, just_for_test=True)
             self.task_module.metrics['test'] = test_metrics
 
         if test_dl is not None:
-            return super().test(self.task_module, dataloaders=test_dl, ckpt_path=ckpt_path, verbose=verbose)
+            dm = GeneralDataModule(test_dl=test_dl)
+            return super().test(self.task_module, datamodule=dm, ckpt_path=ckpt_path, verbose=verbose)
+            # return super().test(self.task_module, dataloaders=test_dl, ckpt_path=ckpt_path, verbose=verbose)
         elif self.datamodule and self.datamodule.test_dataloader():
             return super().test(self.task_module, datamodule=self.datamodule, ckpt_path=ckpt_path, verbose=verbose)
         else:
             raise Exception("Dataloader or DataModule is needed!")  # pylint: disable=broad-exception-raised
 
     def predict(self, pred_dl=None, has_label=False, ckpt_path='best', concat=True):  # pylint: disable=arguments-renamed
         self.task_module.pred_dataloader_has_label = has_label
         if pred_dl is not None:
-            preds = super().predict(self.task_module, pred_dl, None, return_predictions=True, ckpt_path=ckpt_path)
+            dm = GeneralDataModule(pred_dl=pred_dl)
+            preds = super().predict(self.task_module, datamodule=dm, return_predictions=True, ckpt_path=ckpt_path)
+            # preds = super().predict(self.task_module, pred_dl, None, return_predictions=True, ckpt_path=ckpt_path)
         elif self.datamodule and self.datamodule.test_dataloader():
-            preds = super().predict(self.task_module, None, self.datamodule, return_predictions=True, ckpt_path=ckpt_path)
+            preds = super().predict(self.task_module, None, datamodule=self.datamodule, return_predictions=True, ckpt_path=ckpt_path)
         else:
             raise Exception("Dataloader or DataModule is needed!")  # pylint: disable=broad-exception-raised
         if concat:
             return torch.cat(preds, dim=0)
         else:
             return preds
```

### Comparing `torchility-0.6.6/torchility/utils/plots.py` & `torchility-0.6.7/torchility/utils/plots.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/utils/utils.py` & `torchility-0.6.7/torchility/utils/utils.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility/utils/yaml_config.py` & `torchility-0.6.7/torchility/utils/yaml_config.py`

 * *Files identical despite different names*

### Comparing `torchility-0.6.6/torchility.egg-info/PKG-INFO` & `torchility-0.6.7/torchility.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchility
-Version: 0.6.6
+Version: 0.6.7
 Summary: UNKNOWN
 Home-page: https://github.com/hitlic/torchility
 Author: hitlic
 Author-email: liuchen.lic@gmail.com
 License: MIT
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `torchility-0.6.6/torchility.egg-info/SOURCES.txt` & `torchility-0.6.7/torchility.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 examples/1-mnist.py
 examples/2-mnist_callbacks.py
 examples/3-mnist_interpreter.py
 examples/4-mnist_model_analysis.py
 examples/5-mnist_lr_find.py
 examples/6-graph_node_clasification_DGL.py
 torchility/__init__.py
+torchility/datamodule.py
 torchility/hooks.py
 torchility/losses.py
 torchility/metrics.py
 torchility/tasks.py
 torchility/trainer.py
 torchility.egg-info/PKG-INFO
 torchility.egg-info/SOURCES.txt
```

