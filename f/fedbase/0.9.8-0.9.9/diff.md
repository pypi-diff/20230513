# Comparing `tmp/fedbase-0.9.8.tar.gz` & `tmp/fedbase-0.9.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fedbase-0.9.8.tar", last modified: Mon Apr 24 01:53:48 2023, max compression
+gzip compressed data, was "fedbase-0.9.9.tar", last modified: Mon Apr 24 02:28:33 2023, max compression
```

## Comparing `fedbase-0.9.8.tar` & `fedbase-0.9.9.tar`

### file list

```diff
@@ -1,48 +1,48 @@
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.435715 fedbase-0.9.8/
--rw-rw-rw-   0        0        0     1083 2021-11-25 09:10:20.000000 fedbase-0.9.8/LICENSE
--rw-rw-rw-   0        0        0     2297 2023-04-24 01:53:48.434716 fedbase-0.9.8/PKG-INFO
--rw-rw-rw-   0        0        0     1783 2022-04-16 12:00:00.000000 fedbase-0.9.8/README.md
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.375598 fedbase-0.9.8/fedbase/
--rw-rw-rw-   0        0        0       16 2021-11-25 09:27:32.000000 fedbase-0.9.8/fedbase/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.419722 fedbase-0.9.8/fedbase/baselines/
--rw-rw-rw-   0        0        0     1224 2023-04-24 00:48:42.000000 fedbase-0.9.8/fedbase/baselines/Central.py
--rw-rw-rw-   0        0        0     2475 2023-04-24 00:49:07.000000 fedbase-0.9.8/fedbase/baselines/Ditto.py
--rw-rw-rw-   0        0        0     2503 2023-04-24 00:47:54.000000 fedbase-0.9.8/fedbase/baselines/Fedavg.py
--rw-rw-rw-   0        0        0     2759 2023-04-24 00:48:16.000000 fedbase-0.9.8/fedbase/baselines/Fedavg_finetune.py
--rw-rw-rw-   0        0        0     2148 2023-04-24 00:42:15.000000 fedbase-0.9.8/fedbase/baselines/Local.py
--rw-rw-rw-   0        0        0      213 2023-02-07 09:23:33.000000 fedbase-0.9.8/fedbase/baselines/__init__.py
--rw-rw-rw-   0        0        0     2925 2023-04-24 00:50:07.000000 fedbase-0.9.8/fedbase/baselines/fedavg_ensemble.py
--rw-rw-rw-   0        0        0     2594 2023-04-24 00:45:57.000000 fedbase-0.9.8/fedbase/baselines/fedprox.py
--rw-rw-rw-   0        0        0     3015 2023-04-24 00:47:24.000000 fedbase-0.9.8/fedbase/baselines/fedprox_ensemble.py
--rw-rw-rw-   0        0        0     3188 2023-04-24 01:51:43.000000 fedbase-0.9.8/fedbase/baselines/fesem.py
--rw-rw-rw-   0        0        0     5189 2023-04-24 01:49:45.000000 fedbase-0.9.8/fedbase/baselines/fesem_con.py
--rw-rw-rw-   0        0        0     3838 2023-04-24 01:51:26.000000 fedbase-0.9.8/fedbase/baselines/ifca.py
--rw-rw-rw-   0        0        0     4601 2023-04-24 01:49:06.000000 fedbase-0.9.8/fedbase/baselines/ifca_con.py
--rw-rw-rw-   0        0        0     4606 2023-04-24 00:40:35.000000 fedbase-0.9.8/fedbase/baselines/ifca_res.py
--rw-rw-rw-   0        0        0     4359 2023-04-24 01:50:57.000000 fedbase-0.9.8/fedbase/baselines/wecfl.py
--rw-rw-rw-   0        0        0     5167 2023-04-24 01:50:15.000000 fedbase-0.9.8/fedbase/baselines/wecfl_con.py
--rw-rw-rw-   0        0        0     4543 2023-04-24 01:43:34.000000 fedbase-0.9.8/fedbase/baselines/wecfl_res.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.423720 fedbase-0.9.8/fedbase/model/
--rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.8/fedbase/model/__init__.py
--rw-rw-rw-   0        0        0     7655 2023-02-18 03:01:07.000000 fedbase-0.9.8/fedbase/model/model.py
--rw-rw-rw-   0        0        0     9298 2021-11-25 11:00:44.000000 fedbase-0.9.8/fedbase/model/resnet.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.425737 fedbase-0.9.8/fedbase/nodes/
--rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.8/fedbase/nodes/__init__.py
--rw-rw-rw-   0        0        0    14825 2023-04-23 01:06:53.000000 fedbase-0.9.8/fedbase/nodes/node.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.427715 fedbase-0.9.8/fedbase/server/
--rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.8/fedbase/server/__init__.py
--rw-rw-rw-   0        0        0     5838 2023-04-23 01:25:17.000000 fedbase-0.9.8/fedbase/server/server.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.433713 fedbase-0.9.8/fedbase/utils/
--rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.8/fedbase/utils/__init__.py
--rw-rw-rw-   0        0        0    14531 2023-04-23 01:05:04.000000 fedbase-0.9.8/fedbase/utils/data_loader.py
--rw-rw-rw-   0        0        0     6168 2021-11-25 11:00:44.000000 fedbase-0.9.8/fedbase/utils/femnist.py
--rw-rw-rw-   0        0        0      944 2021-12-15 01:18:16.000000 fedbase-0.9.8/fedbase/utils/model_utils.py
--rw-rw-rw-   0        0        0     1694 2023-04-23 01:03:36.000000 fedbase-0.9.8/fedbase/utils/tools.py
--rw-rw-rw-   0        0        0     1125 2022-12-08 06:10:12.000000 fedbase-0.9.8/fedbase/utils/visualize.py
-drwxrwxrwx   0        0        0        0 2023-04-24 01:53:48.390723 fedbase-0.9.8/fedbase.egg-info/
--rw-rw-rw-   0        0        0     2297 2023-04-24 01:53:48.000000 fedbase-0.9.8/fedbase.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1165 2023-04-24 01:53:48.000000 fedbase-0.9.8/fedbase.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-24 01:53:48.000000 fedbase-0.9.8/fedbase.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-04-24 01:53:48.000000 fedbase-0.9.8/fedbase.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-24 01:53:48.435715 fedbase-0.9.8/setup.cfg
--rw-rw-rw-   0        0        0      758 2023-04-24 01:53:35.000000 fedbase-0.9.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.900144 fedbase-0.9.9/
+-rw-rw-rw-   0        0        0     1083 2021-11-25 09:10:20.000000 fedbase-0.9.9/LICENSE
+-rw-rw-rw-   0        0        0     2297 2023-04-24 02:28:33.899145 fedbase-0.9.9/PKG-INFO
+-rw-rw-rw-   0        0        0     1783 2022-04-16 12:00:00.000000 fedbase-0.9.9/README.md
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.849144 fedbase-0.9.9/fedbase/
+-rw-rw-rw-   0        0        0       16 2021-11-25 09:27:32.000000 fedbase-0.9.9/fedbase/__init__.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.885144 fedbase-0.9.9/fedbase/baselines/
+-rw-rw-rw-   0        0        0     1224 2023-04-24 00:48:42.000000 fedbase-0.9.9/fedbase/baselines/Central.py
+-rw-rw-rw-   0        0        0     2475 2023-04-24 00:49:07.000000 fedbase-0.9.9/fedbase/baselines/Ditto.py
+-rw-rw-rw-   0        0        0     2503 2023-04-24 00:47:54.000000 fedbase-0.9.9/fedbase/baselines/Fedavg.py
+-rw-rw-rw-   0        0        0     2759 2023-04-24 00:48:16.000000 fedbase-0.9.9/fedbase/baselines/Fedavg_finetune.py
+-rw-rw-rw-   0        0        0     2148 2023-04-24 00:42:15.000000 fedbase-0.9.9/fedbase/baselines/Local.py
+-rw-rw-rw-   0        0        0      213 2023-02-07 09:23:33.000000 fedbase-0.9.9/fedbase/baselines/__init__.py
+-rw-rw-rw-   0        0        0     2925 2023-04-24 00:50:07.000000 fedbase-0.9.9/fedbase/baselines/fedavg_ensemble.py
+-rw-rw-rw-   0        0        0     2594 2023-04-24 00:45:57.000000 fedbase-0.9.9/fedbase/baselines/fedprox.py
+-rw-rw-rw-   0        0        0     3015 2023-04-24 00:47:24.000000 fedbase-0.9.9/fedbase/baselines/fedprox_ensemble.py
+-rw-rw-rw-   0        0        0     3188 2023-04-24 01:51:43.000000 fedbase-0.9.9/fedbase/baselines/fesem.py
+-rw-rw-rw-   0        0        0     5189 2023-04-24 01:49:45.000000 fedbase-0.9.9/fedbase/baselines/fesem_con.py
+-rw-rw-rw-   0        0        0     3842 2023-04-24 02:27:58.000000 fedbase-0.9.9/fedbase/baselines/ifca.py
+-rw-rw-rw-   0        0        0     4605 2023-04-24 02:17:01.000000 fedbase-0.9.9/fedbase/baselines/ifca_con.py
+-rw-rw-rw-   0        0        0     4606 2023-04-24 00:40:35.000000 fedbase-0.9.9/fedbase/baselines/ifca_res.py
+-rw-rw-rw-   0        0        0     4359 2023-04-24 01:50:57.000000 fedbase-0.9.9/fedbase/baselines/wecfl.py
+-rw-rw-rw-   0        0        0     5167 2023-04-24 01:50:15.000000 fedbase-0.9.9/fedbase/baselines/wecfl_con.py
+-rw-rw-rw-   0        0        0     4543 2023-04-24 01:43:34.000000 fedbase-0.9.9/fedbase/baselines/wecfl_res.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.888145 fedbase-0.9.9/fedbase/model/
+-rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.9/fedbase/model/__init__.py
+-rw-rw-rw-   0        0        0     7655 2023-02-18 03:01:07.000000 fedbase-0.9.9/fedbase/model/model.py
+-rw-rw-rw-   0        0        0     9298 2021-11-25 11:00:44.000000 fedbase-0.9.9/fedbase/model/resnet.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.891145 fedbase-0.9.9/fedbase/nodes/
+-rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.9/fedbase/nodes/__init__.py
+-rw-rw-rw-   0        0        0    14825 2023-04-23 01:06:53.000000 fedbase-0.9.9/fedbase/nodes/node.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.893144 fedbase-0.9.9/fedbase/server/
+-rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.9/fedbase/server/__init__.py
+-rw-rw-rw-   0        0        0     5854 2023-04-24 01:59:09.000000 fedbase-0.9.9/fedbase/server/server.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.898144 fedbase-0.9.9/fedbase/utils/
+-rw-rw-rw-   0        0        0        0 2021-11-25 11:37:24.000000 fedbase-0.9.9/fedbase/utils/__init__.py
+-rw-rw-rw-   0        0        0    14531 2023-04-23 01:05:04.000000 fedbase-0.9.9/fedbase/utils/data_loader.py
+-rw-rw-rw-   0        0        0     6168 2021-11-25 11:00:44.000000 fedbase-0.9.9/fedbase/utils/femnist.py
+-rw-rw-rw-   0        0        0      944 2021-12-15 01:18:16.000000 fedbase-0.9.9/fedbase/utils/model_utils.py
+-rw-rw-rw-   0        0        0     1694 2023-04-23 01:03:36.000000 fedbase-0.9.9/fedbase/utils/tools.py
+-rw-rw-rw-   0        0        0     1125 2022-12-08 06:10:12.000000 fedbase-0.9.9/fedbase/utils/visualize.py
+drwxrwxrwx   0        0        0        0 2023-04-24 02:28:33.864142 fedbase-0.9.9/fedbase.egg-info/
+-rw-rw-rw-   0        0        0     2297 2023-04-24 02:28:33.000000 fedbase-0.9.9/fedbase.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1165 2023-04-24 02:28:33.000000 fedbase-0.9.9/fedbase.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-04-24 02:28:33.000000 fedbase-0.9.9/fedbase.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-04-24 02:28:33.000000 fedbase-0.9.9/fedbase.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-04-24 02:28:33.900144 fedbase-0.9.9/setup.cfg
+-rw-rw-rw-   0        0        0      758 2023-04-24 02:28:25.000000 fedbase-0.9.9/setup.py
```

### Comparing `fedbase-0.9.8/LICENSE` & `fedbase-0.9.9/LICENSE`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/PKG-INFO` & `fedbase-0.9.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fedbase
-Version: 0.9.8
+Version: 0.9.9
 Summary: An easy, silly, DIY Federated Learning framework with many baselines for individual researchers.
 Home-page: https://github.com/jie-ma-ai/FedBase
 Author: Jie MA
 Author-email: ustcmj@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `fedbase-0.9.8/README.md` & `fedbase-0.9.9/README.md`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/Central.py` & `fedbase-0.9.9/fedbase/baselines/Central.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/Ditto.py` & `fedbase-0.9.9/fedbase/baselines/Ditto.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/Fedavg.py` & `fedbase-0.9.9/fedbase/baselines/Fedavg.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/Fedavg_finetune.py` & `fedbase-0.9.9/fedbase/baselines/Fedavg_finetune.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/Local.py` & `fedbase-0.9.9/fedbase/baselines/Local.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/fedavg_ensemble.py` & `fedbase-0.9.9/fedbase/baselines/fedavg_ensemble.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/fedprox.py` & `fedbase-0.9.9/fedbase/baselines/fedprox.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/fedprox_ensemble.py` & `fedbase-0.9.9/fedbase/baselines/fedprox_ensemble.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/fesem.py` & `fedbase-0.9.9/fedbase/baselines/fesem.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/fesem_con.py` & `fedbase-0.9.9/fedbase/baselines/fesem_con.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/ifca.py` & `fedbase-0.9.9/fedbase/baselines/ifca.py`

 * *Files 1% similar despite different names*

```diff
@@ -68,15 +68,15 @@
             else:
                 nodes[j].local_update_steps(local_steps, partial(nodes[j].train_single_step_fedprox, reg_model = server.aggregate(nodes, list(range(num_nodes))), lam= reg))
 
         # server aggregation and distribution by cluster
         for k in range(K):
             if len(assignment[k])>0:
                 weight_ls = [nodes[i].data_size/sum([nodes[i].data_size for i in assignment[k]]) for i in assignment[k]]
-                model_k = server.aggregate([nodes[i].model for i in assign_ls], weight_ls)
+                model_k = server.aggregate([nodes[i].model for i in assignment[k]], weight_ls)
                 server.distribute([nodes[i].model for i in assignment[k]], model_k)
                 cluster_models[k].load_state_dict(model_k)
 
         # test accuracy
         for i in range(num_nodes):
             nodes[i].local_test()
         server.acc(nodes, weight_list)
```

### Comparing `fedbase-0.9.8/fedbase/baselines/ifca_con.py` & `fedbase-0.9.9/fedbase/baselines/ifca_con.py`

 * *Files 1% similar despite different names*

```diff
@@ -77,15 +77,15 @@
                     model_sim = cluster_models[nodes[j].label], model_all = cluster_models, tmp = tmp, mu = mu, base = base\
                         , reg_lam = reg_lam, reg_model = server.model))
 
         # server aggregation and distribution by cluster
         for k in range(K):
             if len(assignment[k])>0:
                 weight_ls = [nodes[i].data_size/sum([nodes[i].data_size for i in assignment[k]]) for i in assignment[k]]
-                model_k = server.aggregate([nodes[i].model for i in assign_ls], weight_ls)
+                model_k = server.aggregate([nodes[i].model for i in assignment[k]], weight_ls)
                 server.distribute([nodes[i].model for i in assignment[k]], model_k)
                 cluster_models[k].load_state_dict(model_k)
 
         # test accuracy
         for i in range(num_nodes):
             nodes[i].local_test()
         server.acc(nodes, weight_list)
```

### Comparing `fedbase-0.9.8/fedbase/baselines/ifca_res.py` & `fedbase-0.9.9/fedbase/baselines/ifca_res.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/wecfl.py` & `fedbase-0.9.9/fedbase/baselines/wecfl.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/wecfl_con.py` & `fedbase-0.9.9/fedbase/baselines/wecfl_con.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/baselines/wecfl_res.py` & `fedbase-0.9.9/fedbase/baselines/wecfl_res.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/model/model.py` & `fedbase-0.9.9/fedbase/model/model.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/model/resnet.py` & `fedbase-0.9.9/fedbase/model/resnet.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/nodes/node.py` & `fedbase-0.9.9/fedbase/nodes/node.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/server/server.py` & `fedbase-0.9.9/fedbase/server/server.py`

 * *Files 1% similar despite different names*

```diff
@@ -37,19 +37,19 @@
             aggregated_weights[j] = torch.zeros(aggregated_weights[j].shape).to(self.device)
         # sum_size = sum([nodes[i].data_size for i in idlist])
         for i in range(len(model_list)):
             for j in model_list[i].state_dict().keys():
                 aggregated_weights[j] += model_list[i].state_dict()[j]*weight_list[i]
         return aggregated_weights
     
-    def distribute(self, model_in_list, model_dis = None):
-        if model_dis is None:
-            model_dis = self.model
+    def distribute(self, model_in_list, model_dis_dict = None):
+        if not model_dis_dict:
+            model_dis_dict = self.model.state_dict()
         for i in model_in_list:
-            i.load_state_dict(model_dis.state_dict())
+            i.load_state_dict(model_dis_dict)
 
     def acc(self, nodes, weight_list):
         global_test_metrics = [0]*2
         for i in range(len(weight_list)):
             for j in range(len(global_test_metrics)):
                 global_test_metrics[j] += weight_list[i]*nodes[i].test_metrics[-1][j]
         print('GLOBAL Accuracy, Macro F1 is %.2f %%, %.2f %%' % (100*global_test_metrics[0], 100*global_test_metrics[1]))
```

### Comparing `fedbase-0.9.8/fedbase/utils/data_loader.py` & `fedbase-0.9.9/fedbase/utils/data_loader.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/utils/femnist.py` & `fedbase-0.9.9/fedbase/utils/femnist.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/utils/model_utils.py` & `fedbase-0.9.9/fedbase/utils/model_utils.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/utils/tools.py` & `fedbase-0.9.9/fedbase/utils/tools.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase/utils/visualize.py` & `fedbase-0.9.9/fedbase/utils/visualize.py`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/fedbase.egg-info/PKG-INFO` & `fedbase-0.9.9/fedbase.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fedbase
-Version: 0.9.8
+Version: 0.9.9
 Summary: An easy, silly, DIY Federated Learning framework with many baselines for individual researchers.
 Home-page: https://github.com/jie-ma-ai/FedBase
 Author: Jie MA
 Author-email: ustcmj@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `fedbase-0.9.8/fedbase.egg-info/SOURCES.txt` & `fedbase-0.9.9/fedbase.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `fedbase-0.9.8/setup.py` & `fedbase-0.9.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="fedbase",
-    version="0.9.8",
+    version="0.9.9",
     author="Jie MA",
     # author_email="ustcmj@gmail.com, jie.ma-5@student.uts.edu.au",
     author_email="ustcmj@gmail.com",
     description="An easy, silly, DIY Federated Learning framework with many baselines for individual researchers.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/jie-ma-ai/FedBase",
```

