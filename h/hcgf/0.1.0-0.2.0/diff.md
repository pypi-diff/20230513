# Comparing `tmp/hcgf-0.1.0.tar.gz` & `tmp/hcgf-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hcgf-0.1.0.tar", last modified: Tue Apr 11 16:14:49 2023, max compression
+gzip compressed data, was "hcgf-0.2.0.tar", last modified: Sat May 13 07:35:04 2023, max compression
```

## Comparing `hcgf-0.1.0.tar` & `hcgf-0.2.0.tar`

### file list

```diff
@@ -1,43 +1,48 @@
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.586121 hcgf-0.1.0/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)    11357 2023-03-25 10:33:36.000000 hcgf-0.1.0/LICENSE
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     5261 2023-04-11 16:14:49.586121 hcgf-0.1.0/PKG-INFO
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4854 2023-04-11 16:12:21.000000 hcgf-0.1.0/README.md
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.583121 hcgf-0.1.0/hcgf/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      154 2023-04-11 15:52:10.000000 hcgf-0.1.0/hcgf/__init__.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.584121 hcgf-0.1.0/hcgf/data_model/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      923 2023-04-03 08:46:08.000000 hcgf-0.1.0/hcgf/data_model/__init__.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.584121 hcgf-0.1.0/hcgf/dataloader/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      123 2023-03-25 10:33:36.000000 hcgf-0.1.0/hcgf/dataloader/__init__.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3916 2023-04-11 15:27:44.000000 hcgf-0.1.0/hcgf/dataloader/data_collector.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     2737 2023-03-27 01:17:21.000000 hcgf-0.1.0/hcgf/dataloader/data_loader.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1476 2023-04-03 09:05:55.000000 hcgf-0.1.0/hcgf/dataloader/dataset.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.584121 hcgf-0.1.0/hcgf/rm/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)        0 2023-04-02 15:08:12.000000 hcgf-0.1.0/hcgf/rm/__init__.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1375 2023-04-02 15:08:12.000000 hcgf-0.1.0/hcgf/rm/reward_model.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.584121 hcgf-0.1.0/hcgf/sft/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)       28 2023-03-25 10:33:36.000000 hcgf-0.1.0/hcgf/sft/__init__.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.585121 hcgf-0.1.0/hcgf/sft/chatglm/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      170 2023-04-03 07:50:12.000000 hcgf-0.1.0/hcgf/sft/chatglm/__init__.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4269 2023-04-10 02:05:09.000000 hcgf-0.1.0/hcgf/sft/chatglm/configuration_chatglm.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)    56527 2023-04-10 02:06:50.000000 hcgf-0.1.0/hcgf/sft/chatglm/modeling_chatglm.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)    15053 2023-04-10 02:09:24.000000 hcgf-0.1.0/hcgf/sft/chatglm/quantization.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)    16684 2023-04-10 02:10:14.000000 hcgf-0.1.0/hcgf/sft/chatglm/tokenization_chatglm.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     9221 2023-04-11 15:27:44.000000 hcgf-0.1.0/hcgf/sft/lora_ft.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.585121 hcgf-0.1.0/hcgf/trainer/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)       28 2023-03-25 10:33:36.000000 hcgf-0.1.0/hcgf/trainer/__init__.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     6066 2023-04-10 15:52:51.000000 hcgf-0.1.0/hcgf/trainer/trainer.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.586121 hcgf-0.1.0/hcgf/utils/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      128 2023-04-03 09:51:01.000000 hcgf-0.1.0/hcgf/utils/__init__.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     2048 2023-04-04 15:51:29.000000 hcgf-0.1.0/hcgf/utils/utils.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.584121 hcgf-0.1.0/hcgf.egg-info/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     5261 2023-04-11 16:14:49.000000 hcgf-0.1.0/hcgf.egg-info/PKG-INFO
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      751 2023-04-11 16:14:49.000000 hcgf-0.1.0/hcgf.egg-info/SOURCES.txt
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)        1 2023-04-11 16:14:49.000000 hcgf-0.1.0/hcgf.egg-info/dependency_links.txt
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)        5 2023-04-11 16:14:49.000000 hcgf-0.1.0/hcgf.egg-info/top_level.txt
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)       38 2023-04-11 16:14:49.586121 hcgf-0.1.0/setup.cfg
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      883 2023-04-11 15:51:53.000000 hcgf-0.1.0/setup.py
-drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-04-11 16:14:49.586121 hcgf-0.1.0/tests/
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4640 2023-04-11 15:33:54.000000 hcgf-0.1.0/tests/test_dataloader.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1451 2023-04-11 15:52:57.000000 hcgf-0.1.0/tests/test_lora_ft.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1419 2023-04-04 17:34:59.000000 hcgf-0.1.0/tests/test_trainer.py
--rw-rw-r--   0 wyd       (1013) anaconda  (1000)      453 2023-04-03 09:56:55.000000 hcgf-0.1.0/tests/test_utils.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.213953 hcgf-0.2.0/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)    11357 2023-03-25 10:33:36.000000 hcgf-0.2.0/LICENSE
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     7144 2023-05-13 07:35:04.213953 hcgf-0.2.0/PKG-INFO
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     6737 2023-05-13 07:34:32.000000 hcgf-0.2.0/README.md
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.210953 hcgf-0.2.0/hcgf/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      154 2023-04-11 15:52:10.000000 hcgf-0.2.0/hcgf/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4658 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/__main_infer__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3521 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/__main_tune__.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.211953 hcgf-0.2.0/hcgf/data_model/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      923 2023-04-03 08:46:08.000000 hcgf-0.2.0/hcgf/data_model/__init__.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.211953 hcgf-0.2.0/hcgf/dataloader/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      123 2023-03-25 10:33:36.000000 hcgf-0.2.0/hcgf/dataloader/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3685 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/dataloader/data_collector.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3636 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/dataloader/data_loader.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1475 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/dataloader/dataset.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.211953 hcgf-0.2.0/hcgf/rm/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)        0 2023-04-02 15:08:12.000000 hcgf-0.2.0/hcgf/rm/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1375 2023-04-02 15:08:12.000000 hcgf-0.2.0/hcgf/rm/reward_model.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.212953 hcgf-0.2.0/hcgf/sft/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       23 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)    15746 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/ft.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.212953 hcgf-0.2.0/hcgf/sft/lora/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       75 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/lora/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1360 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/lora/lora_config.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     8559 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/lora/lora_layer.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     5591 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/lora/lora_layer_8bit.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4973 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/sft/lora/lora_model.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.212953 hcgf-0.2.0/hcgf/trainer/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       28 2023-03-25 10:33:36.000000 hcgf-0.2.0/hcgf/trainer/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3220 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/trainer/fsdp.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)    10257 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/trainer/trainer.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.213953 hcgf-0.2.0/hcgf/utils/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      238 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/utils/__init__.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     3740 2023-05-13 07:34:32.000000 hcgf-0.2.0/hcgf/utils/utils.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.211953 hcgf-0.2.0/hcgf.egg-info/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     7144 2023-05-13 07:35:03.000000 hcgf-0.2.0/hcgf.egg-info/PKG-INFO
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      832 2023-05-13 07:35:04.000000 hcgf-0.2.0/hcgf.egg-info/SOURCES.txt
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)        1 2023-05-13 07:35:03.000000 hcgf-0.2.0/hcgf.egg-info/dependency_links.txt
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       92 2023-05-13 07:35:03.000000 hcgf-0.2.0/hcgf.egg-info/entry_points.txt
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       50 2023-05-13 07:35:03.000000 hcgf-0.2.0/hcgf.egg-info/requires.txt
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)        5 2023-05-13 07:35:03.000000 hcgf-0.2.0/hcgf.egg-info/top_level.txt
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)       38 2023-05-13 07:35:04.213953 hcgf-0.2.0/setup.cfg
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1158 2023-05-13 07:34:32.000000 hcgf-0.2.0/setup.py
+drwxrwsr-x   0 wyd       (1013) anaconda  (1000)        0 2023-05-13 07:35:04.213953 hcgf-0.2.0/tests/
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     4683 2023-05-13 07:34:32.000000 hcgf-0.2.0/tests/test_dataloader.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1552 2023-05-13 07:34:32.000000 hcgf-0.2.0/tests/test_lora_ft.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)     1432 2023-05-13 07:34:32.000000 hcgf-0.2.0/tests/test_trainer.py
+-rw-rw-r--   0 wyd       (1013) anaconda  (1000)      453 2023-04-03 09:56:55.000000 hcgf-0.2.0/tests/test_utils.py
```

### Comparing `hcgf-0.1.0/LICENSE` & `hcgf-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hcgf-0.1.0/PKG-INFO` & `hcgf-0.2.0/README.md`

 * *Files 21% similar despite different names*

```diff
@@ -1,48 +1,66 @@
-Metadata-Version: 2.1
-Name: hcgf
-Version: 0.1.0
-Summary: Humanable ChatGPT/GLM Fine-tuning.
-Home-page: https://github.com/hscspring/hcgf
-Author: Yam
-Author-email: haoshaochun@gmail.com
-Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: Apache Software License
-Classifier: Operating System :: OS Independent
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 先clone仓库或pip安装：
 
 ```bash
 pip install hcgf
 ```
 
 需要的依赖在`requirements.txt`中，通过下面命令安装：
 
 ```
 pip install -r requirements.txt
 ```
 
-注意：不支持PyTorch2.0，历史版本请参考下面链接安装：
-
-https://pytorch.org/get-started/previous-versions/
-
+建议使用PyTorch2.0
 
 
-## 微调
+## 微调训练
 
 ### 准备数据
 
 每一行一个dict的`.json`文件，必须包含`prompt`和`completion`两个字段。示例如下：
 
-```bash
+```python
 {"prompt": "你是谁？", "completion": "不告诉你。"}
 ```
 
+### 分布式微调
+
+使用PyTorch的FSDP训练，支持Zero3、Zero2和DDP模式，使用方法请参考帮助文档：
+
+```bash
+hcgf_tune -h
+```
+
+至少要指定`model`和`data_path`参数，如下：
+
+```bash
+hcgf_tune --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
+一共五种策略：
+
+- fsdp_zero3：命令行模式默认策略，FULL_SHARD，参数、梯度、优化器状态SHARD
+- fsdp_zero2：GRAD_OP_SHARD，梯度、优化器状态SHARD
+- mpdp(ddp)：NO_SHARD，类似DDP
+- mpds(8bit)：8bit模式（下面的《8bit微调》）
+- msds(single_gpu)：单卡模式（下面的《正常微调》）
+
+| 卡数 | 显存           | 训练数据 | 策略                  |
+| ---- | -------------- | -------- | --------------------- |
+| 多卡 | 单卡放不下模型 | 数据很多 | fsdp_zero3/fsdp_zero2 |
+|      | 单卡能放下模型 | 数据很多 | mpdp                  |
+|      | 单卡放不下模型 | 数据很少 | mpds                  |
+|      | 单卡能放下模型 | 数据很少 | msds                  |
+| 单卡 | 单卡放不下模型 | -        | mpds                  |
+|      | 单卡能放下模型 | -        | msds                  |
+
+
+注意，这里显存是在训练模式下的，和推理模式占用不同，可参考下面的《配置》。推理只支持后两种模式。
+
 
 ### 正常微调
 
 至少需要一张16G显存的卡。如果不指定显卡，默认为`cuda`。
 
 ```python
 #===== 微调 =====#
@@ -65,76 +83,105 @@
 gl.tune()
 # 如果有新的数据集，参考上面的写法，先加载数据
 gl.load_data("/path/to/new_data.json").tune()
 # 如果在原来的基础上用新数据继续微调，先加载之前的pt文件，再加载数据微调
 gl.load_pretrained("/path/to/lora_pt").load_data("/path/to/new_data.json").tune()
 ```
 
+当然，也可以使用`hcgf_tune`:
+
+```bash
+hcgf_tune strategy msds --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
 
 ### 8bit微调
 
 至少需要一张12G显存的卡。不指定device。只需要初始化时改一下即可，其他操作和上面正常微调一样。
 
 需要安装依赖: `bitsandbytes`
 
 ```python
 gl = hcgf.GlmLora("THUDM/chatglm-6b", load_in_8bit=True)
 ```
 
+
+当然，也可以使用`hcgf_tune`:
+
+```bash
+hcgf_tune strategy mpds --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
 ### 继续微调
 
 先加载之前的`pt`文件，然后加载数据微调。
 
 ```python
 gl.load_pretrained("/path/to/lora_pt").load_data("/path/to/new_data.json").tune()
 ```
 
+### 演示Demo/推理
+
+请执行`hcgf_infer -h`查看帮助。
+
+
 ### 参数说明
 
 主要有三个方法的参数，有值的表示默认值。
 
 ```python
 load_data(
     data_path: str, 
     max_seq_len: int = 512, # 句子最大长度，超过会截断
 )
 tune(
-    batch_size: int = 1,
+    batch_size: int = 8,
     lr: float = 2e-4,
-    num_epochs: int = 10,
-    warmup_steps: Optional[int] = None,     # 为None时会用第一个Epoch进行warmup
-    accumulate_steps: Optional[int] = 32,
+    num_epochs: int = 3,
+    warmup_steps: Optional[int] = None,     # 为None时会用1/3个Epoch进行warmup
+    accumulate_steps: Optional[int] = None, # 为None时等价于1
     out_dir: str = "./output/",
-    print_every: int = 10,                  # 每隔多少个Step打印一次输出（Step、Loss、LearningRate）
+    print_every: Optional[int] = None,      # 为None时每1/10Epoch个Steps打印一次输出（Step、Loss、LearningRate）
 )
 chat(
     inp: str, 
     history: List[Tuple[str, str]] = None,  # (问，答)Pair对
-    max_len: int = 512,                     # 上下文的最大长度，超过就不生成了
-    temperature: float = 0.95,              # 越小越确定，越大越随机，比如你微调后可以把它改成0.2
+    max_new_tokens: int = 512,              # 生成的文本最大长度，Prompt的长度=支持的最大长度-max_new_tokens，Prompt长度超过会被截断
+    do_sample: bool = True,                 # 采样
+    num_beams: int = 1,                     # Beam Search 的 beam 数量
+    temperature: float = 0.95,              # 越小越确定，越大越随机，比如你微调后可以把它改成0.1
     top_p: float = 0.7,                     # 同上，两者不要同时调
+    repetition_penalty: float = 1.02,       # 生成内容重复惩罚，越大越不容易重复
     stop: List[str] = []                    # 停止文本，可以是标点、特定词或句子等，输出不包含停止文本
 )
-
 ```
 
+Best Practice:
+
+- `tune`: 如果内存不够可以调小batch_size，同时增加accumulate_steps，一般是batch_size的整数倍；
+- `chat`: 一般只需调整`temerature`；
+
+
 ### 配置
 
 有几个影响显存的参数可以配置：`max_seq_len`，`batch_size`。
 
 
 ```python
 (
 gl
 .load_data("./data/chatgpt_finetune_faq.json", max_seq_len=128)
 .tune(batch_size=1)
 )
 
 ```
 
+以下配置针对`ChatGLM-6B`。
+
+
 不同配置 `8bit` 资源占用：
 
 | max_seq_len | batch_size | memory |
 | ----------- | ---------- | ------ |
 | `64`        | 1          | 11G    |
 | `128`       | 1          | 12G    |
 | `512`       | 1          | 22G    |
@@ -160,42 +207,39 @@
 
 ### 准备数据
 
 需要pair对数据，计算logits过程和普通预训练模型一样（一个Batch多个pair对）；计算loss时属于同一个pair对的logits放一块算。
 
 推理时直接用logits就行。
 
-### 推理
 
 
 ## 测试
 
 ```bash
 # 全部测试
 python -m pytest
 # 测试训练和推理，比较慢
 python -m pytest -s -m slow
 # 测试其他的
 python -m pytest -m "not slow"
 ```
 
 
-## 版本说明
-
-如果你用的是旧版本的ChatGLM（icetk tokenizer），可以安装`hcgf==0.0.7`版本，同时，需要手动指定`model_id`参数为模型文件实际路径。
+## 其他说明
 
-即将`"THUDM/chatglm-6b"`替换为`transformers` `cache`的对应snapshots下的id。或者，建议手动clone仓库：
+如果遇到加载超时，可以直接load本地cache下的模型：
 
-```bash
-git lfs install
-git clone https://huggingface.co/THUDM/chatglm-6b
+```Python
+GlmLora("/path/to/huggingface/models--THUDM--chatglm-6b/snapshots/<id>/")
 ```
 
-然后切换到早期使用icetk的commit。这时候要替换的就是这个仓库的路径了。
-
 
 ## 更新日志
 
+- **v0.2.0** `20230513`
+  - 支持分布式微调
+  - 调整推理模式，支持Batch
 - **v0.1.0** `20230412`
   - 支持ChatGLM新版Tokenizer
   - 使用官方调整后的MASK方式
-- **v0.0.7** `20230405`
+- **v0.0.7** `20230405`
```

### Comparing `hcgf-0.1.0/README.md` & `hcgf-0.2.0/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,35 +1,79 @@
+Metadata-Version: 2.1
+Name: hcgf
+Version: 0.2.0
+Summary: Humanable ChatGPT/GLM Fine-tuning.
+Home-page: https://github.com/hscspring/hcgf
+Author: Yam
+Author-email: haoshaochun@gmail.com
+Classifier: Programming Language :: Python :: 3
+Classifier: License :: OSI Approved :: Apache Software License
+Classifier: Operating System :: OS Independent
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 先clone仓库或pip安装：
 
 ```bash
 pip install hcgf
 ```
 
 需要的依赖在`requirements.txt`中，通过下面命令安装：
 
 ```
 pip install -r requirements.txt
 ```
 
-注意：不支持PyTorch2.0，历史版本请参考下面链接安装：
-
-https://pytorch.org/get-started/previous-versions/
-
+建议使用PyTorch2.0
 
 
-## 微调
+## 微调训练
 
 ### 准备数据
 
 每一行一个dict的`.json`文件，必须包含`prompt`和`completion`两个字段。示例如下：
 
-```bash
+```python
 {"prompt": "你是谁？", "completion": "不告诉你。"}
 ```
 
+### 分布式微调
+
+使用PyTorch的FSDP训练，支持Zero3、Zero2和DDP模式，使用方法请参考帮助文档：
+
+```bash
+hcgf_tune -h
+```
+
+至少要指定`model`和`data_path`参数，如下：
+
+```bash
+hcgf_tune --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
+一共五种策略：
+
+- fsdp_zero3：命令行模式默认策略，FULL_SHARD，参数、梯度、优化器状态SHARD
+- fsdp_zero2：GRAD_OP_SHARD，梯度、优化器状态SHARD
+- mpdp(ddp)：NO_SHARD，类似DDP
+- mpds(8bit)：8bit模式（下面的《8bit微调》）
+- msds(single_gpu)：单卡模式（下面的《正常微调》）
+
+| 卡数 | 显存           | 训练数据 | 策略                  |
+| ---- | -------------- | -------- | --------------------- |
+| 多卡 | 单卡放不下模型 | 数据很多 | fsdp_zero3/fsdp_zero2 |
+|      | 单卡能放下模型 | 数据很多 | mpdp                  |
+|      | 单卡放不下模型 | 数据很少 | mpds                  |
+|      | 单卡能放下模型 | 数据很少 | msds                  |
+| 单卡 | 单卡放不下模型 | -        | mpds                  |
+|      | 单卡能放下模型 | -        | msds                  |
+
+
+注意，这里显存是在训练模式下的，和推理模式占用不同，可参考下面的《配置》。推理只支持后两种模式。
+
 
 ### 正常微调
 
 至少需要一张16G显存的卡。如果不指定显卡，默认为`cuda`。
 
 ```python
 #===== 微调 =====#
@@ -52,76 +96,105 @@
 gl.tune()
 # 如果有新的数据集，参考上面的写法，先加载数据
 gl.load_data("/path/to/new_data.json").tune()
 # 如果在原来的基础上用新数据继续微调，先加载之前的pt文件，再加载数据微调
 gl.load_pretrained("/path/to/lora_pt").load_data("/path/to/new_data.json").tune()
 ```
 
+当然，也可以使用`hcgf_tune`:
+
+```bash
+hcgf_tune strategy msds --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
 
 ### 8bit微调
 
 至少需要一张12G显存的卡。不指定device。只需要初始化时改一下即可，其他操作和上面正常微调一样。
 
 需要安装依赖: `bitsandbytes`
 
 ```python
 gl = hcgf.GlmLora("THUDM/chatglm-6b", load_in_8bit=True)
 ```
 
+
+当然，也可以使用`hcgf_tune`:
+
+```bash
+hcgf_tune strategy mpds --model THUDM/chatglm-6b --data_path path/to/train_data.json
+```
+
 ### 继续微调
 
 先加载之前的`pt`文件，然后加载数据微调。
 
 ```python
 gl.load_pretrained("/path/to/lora_pt").load_data("/path/to/new_data.json").tune()
 ```
 
+### 演示Demo/推理
+
+请执行`hcgf_infer -h`查看帮助。
+
+
 ### 参数说明
 
 主要有三个方法的参数，有值的表示默认值。
 
 ```python
 load_data(
     data_path: str, 
     max_seq_len: int = 512, # 句子最大长度，超过会截断
 )
 tune(
-    batch_size: int = 1,
+    batch_size: int = 8,
     lr: float = 2e-4,
-    num_epochs: int = 10,
-    warmup_steps: Optional[int] = None,     # 为None时会用第一个Epoch进行warmup
-    accumulate_steps: Optional[int] = 32,
+    num_epochs: int = 3,
+    warmup_steps: Optional[int] = None,     # 为None时会用1/3个Epoch进行warmup
+    accumulate_steps: Optional[int] = None, # 为None时等价于1
     out_dir: str = "./output/",
-    print_every: int = 10,                  # 每隔多少个Step打印一次输出（Step、Loss、LearningRate）
+    print_every: Optional[int] = None,      # 为None时每1/10Epoch个Steps打印一次输出（Step、Loss、LearningRate）
 )
 chat(
     inp: str, 
     history: List[Tuple[str, str]] = None,  # (问，答)Pair对
-    max_len: int = 512,                     # 上下文的最大长度，超过就不生成了
-    temperature: float = 0.95,              # 越小越确定，越大越随机，比如你微调后可以把它改成0.2
+    max_new_tokens: int = 512,              # 生成的文本最大长度，Prompt的长度=支持的最大长度-max_new_tokens，Prompt长度超过会被截断
+    do_sample: bool = True,                 # 采样
+    num_beams: int = 1,                     # Beam Search 的 beam 数量
+    temperature: float = 0.95,              # 越小越确定，越大越随机，比如你微调后可以把它改成0.1
     top_p: float = 0.7,                     # 同上，两者不要同时调
+    repetition_penalty: float = 1.02,       # 生成内容重复惩罚，越大越不容易重复
     stop: List[str] = []                    # 停止文本，可以是标点、特定词或句子等，输出不包含停止文本
 )
-
 ```
 
+Best Practice:
+
+- `tune`: 如果内存不够可以调小batch_size，同时增加accumulate_steps，一般是batch_size的整数倍；
+- `chat`: 一般只需调整`temerature`；
+
+
 ### 配置
 
 有几个影响显存的参数可以配置：`max_seq_len`，`batch_size`。
 
 
 ```python
 (
 gl
 .load_data("./data/chatgpt_finetune_faq.json", max_seq_len=128)
 .tune(batch_size=1)
 )
 
 ```
 
+以下配置针对`ChatGLM-6B`。
+
+
 不同配置 `8bit` 资源占用：
 
 | max_seq_len | batch_size | memory |
 | ----------- | ---------- | ------ |
 | `64`        | 1          | 11G    |
 | `128`       | 1          | 12G    |
 | `512`       | 1          | 22G    |
@@ -147,42 +220,39 @@
 
 ### 准备数据
 
 需要pair对数据，计算logits过程和普通预训练模型一样（一个Batch多个pair对）；计算loss时属于同一个pair对的logits放一块算。
 
 推理时直接用logits就行。
 
-### 推理
 
 
 ## 测试
 
 ```bash
 # 全部测试
 python -m pytest
 # 测试训练和推理，比较慢
 python -m pytest -s -m slow
 # 测试其他的
 python -m pytest -m "not slow"
 ```
 
 
-## 版本说明
-
-如果你用的是旧版本的ChatGLM（icetk tokenizer），可以安装`hcgf==0.0.7`版本，同时，需要手动指定`model_id`参数为模型文件实际路径。
+## 其他说明
 
-即将`"THUDM/chatglm-6b"`替换为`transformers` `cache`的对应snapshots下的id。或者，建议手动clone仓库：
+如果遇到加载超时，可以直接load本地cache下的模型：
 
-```bash
-git lfs install
-git clone https://huggingface.co/THUDM/chatglm-6b
+```Python
+GlmLora("/path/to/huggingface/models--THUDM--chatglm-6b/snapshots/<id>/")
 ```
 
-然后切换到早期使用icetk的commit。这时候要替换的就是这个仓库的路径了。
-
 
 ## 更新日志
 
+- **v0.2.0** `20230513`
+  - 支持分布式微调
+  - 调整推理模式，支持Batch
 - **v0.1.0** `20230412`
   - 支持ChatGLM新版Tokenizer
   - 使用官方调整后的MASK方式
-- **v0.0.7** `20230405`
+- **v0.0.7** `20230405`
```

### Comparing `hcgf-0.1.0/hcgf/data_model/__init__.py` & `hcgf-0.2.0/hcgf/data_model/__init__.py`

 * *Files identical despite different names*

### Comparing `hcgf-0.1.0/hcgf/dataloader/data_collector.py` & `hcgf-0.2.0/hcgf/dataloader/data_collector.py`

 * *Files 7% similar despite different names*

```diff
@@ -20,19 +20,17 @@
     150001 [gMASK]
     150002 [sMASK]
 
     # new version
     130000 [MASK]  # mask
     130001 [gMASK] # gmask
     130004 <sop>   # bos
-    130005 <eop>   # eop
-    2      </s>    # eos
+    130005 <eop>   # eos
     3      <pad>   # pad
     0      <unk>   # unk
-    130002 [sMASK] # smask
     """
 
     @classmethod
     def get_masks(cls, longest_seq_len: int, cxt_len: int, dtype=torch.int32):
         """
         Referenced from ChatGLMModel.get_masks
         """
@@ -47,19 +45,19 @@
     def get_position_ids(
         cls,
         longest_seq_len: int,
         cxt_len: int,
         mask_position: int,
         use_gmask: bool,
         position_encoding_2d: bool = True,
-        dtype=torch.int64,
     ):
         """
         Referenced from ChatGLMMModel.get_position_ids
         """
+        dtype=torch.int64
         position_ids = torch.arange(longest_seq_len, dtype=dtype)
         if position_encoding_2d:
             # NOTE: if position_encoding_2d, use_gmask is not used
             # https://github.com/THUDM/ChatGLM-6B/issues/498#event-8971243132
             position_ids[cxt_len:] = mask_position
             block_position_ids = torch.cat((
                 torch.zeros(cxt_len, dtype=dtype),
@@ -72,15 +70,14 @@
                 position_ids[longest_seq_len - 1:] = mask_position
         return position_ids
 
     @classmethod
     def collate_fn(
         cls,
         data_items: List[DataItem],
-        input_dtype: torch.Type = torch.int64
     ) -> GlmBatchInput:
         len_ids = [len(v.input_ids) for v in data_items]
         longest_seq_len = max(len_ids)
         id_list = []
         mask_list = []
         pid_list = []
         label_list = []
@@ -96,31 +93,27 @@
             use_gmask = False if MASK in ids else True
 
             _masks = cls.get_masks(longest_seq_len, cxt_len)
             # equal to cxt_len - 1
             cxt_idx = ids.index(130004)
             _pids = cls.get_position_ids(
                 longest_seq_len, cxt_idx, mask_position, use_gmask,
-                position_encoding_2d=True, dtype=input_dtype
+                position_encoding_2d=True
             )
 
             padding_len = longest_seq_len - seq_len
             _labels = [-100] * (cxt_len - 1) + \
                 ids[(cxt_len - 1):] + [-100] * padding_len
-            _ids = ids + [2] * padding_len
+            # pad_id: 3
+            _ids = ids + [3] * padding_len
 
-            if input_dtype == torch.int32:
-                TensorIns = torch.IntTensor
-            else:
-                TensorIns = torch.LongTensor
-
-            id_list.append(TensorIns(_ids))
+            id_list.append(torch.LongTensor(_ids))
             pid_list.append(_pids)
             mask_list.append(_masks)
-            label_list.append(TensorIns(_labels))
+            label_list.append(torch.LongTensor(_labels))
         input_ids = torch.stack(id_list)
         position_ids = torch.stack(pid_list)
         attention_mask = torch.stack(mask_list)
         labels = torch.stack(label_list)
         return {
             "input_ids": input_ids,
             "position_ids": position_ids,
```

### Comparing `hcgf-0.1.0/hcgf/dataloader/dataset.py` & `hcgf-0.2.0/hcgf/dataloader/dataset.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -40,8 +40,8 @@
         return DataItem(input_ids, cxt_len)
 
     def __len__(self) -> int:
         return len(self.data)
 
     def __iter__(self):
         for i in range(len(self.data)):
-            yield self[i]
+            yield self[i]
```

### Comparing `hcgf-0.1.0/hcgf/rm/reward_model.py` & `hcgf-0.2.0/hcgf/rm/reward_model.py`

 * *Files identical despite different names*

### Comparing `hcgf-0.1.0/hcgf.egg-info/SOURCES.txt` & `hcgf-0.2.0/hcgf.egg-info/SOURCES.txt`

 * *Files 24% similar despite different names*

```diff
@@ -1,30 +1,35 @@
 LICENSE
 README.md
 setup.py
 hcgf/__init__.py
+hcgf/__main_infer__.py
+hcgf/__main_tune__.py
 hcgf.egg-info/PKG-INFO
 hcgf.egg-info/SOURCES.txt
 hcgf.egg-info/dependency_links.txt
+hcgf.egg-info/entry_points.txt
+hcgf.egg-info/requires.txt
 hcgf.egg-info/top_level.txt
 hcgf/data_model/__init__.py
 hcgf/dataloader/__init__.py
 hcgf/dataloader/data_collector.py
 hcgf/dataloader/data_loader.py
 hcgf/dataloader/dataset.py
 hcgf/rm/__init__.py
 hcgf/rm/reward_model.py
 hcgf/sft/__init__.py
-hcgf/sft/lora_ft.py
-hcgf/sft/chatglm/__init__.py
-hcgf/sft/chatglm/configuration_chatglm.py
-hcgf/sft/chatglm/modeling_chatglm.py
-hcgf/sft/chatglm/quantization.py
-hcgf/sft/chatglm/tokenization_chatglm.py
+hcgf/sft/ft.py
+hcgf/sft/lora/__init__.py
+hcgf/sft/lora/lora_config.py
+hcgf/sft/lora/lora_layer.py
+hcgf/sft/lora/lora_layer_8bit.py
+hcgf/sft/lora/lora_model.py
 hcgf/trainer/__init__.py
+hcgf/trainer/fsdp.py
 hcgf/trainer/trainer.py
 hcgf/utils/__init__.py
 hcgf/utils/utils.py
 tests/test_dataloader.py
 tests/test_lora_ft.py
 tests/test_trainer.py
 tests/test_utils.py
```

### Comparing `hcgf-0.1.0/setup.py` & `hcgf-0.2.0/setup.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,27 +1,36 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
+with open('requirements.txt', 'r', encoding='utf-8') as f:
+    requirements = f.read().split('\n')
+
+
 setuptools.setup(
     name="hcgf",
-    version="0.1.0",
+    version="0.2.0",
     author="Yam",
     author_email="haoshaochun@gmail.com",
     description="Humanable ChatGPT/GLM Fine-tuning.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/hscspring/hcgf",
     include_package_data=True,
     # default is `setup.py` path, so do not need a `package_dir` attr
     # if another dir, should be declared by `package_dir`
     packages=setuptools.find_packages(exclude=["*.tests", "*.tests.*", "tests.*", "tests"]),
-    install_requires=[
-    ],
+    install_requires=requirements,
+    entry_points={
+        "console_scripts": [
+            "hcgf_tune = hcgf.__main_tune__:main",
+            "hcgf_infer = hcgf.__main_infer__:main",
+        ]
+    },
     package_data={
     },
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: Apache Software License",
         "Operating System :: OS Independent",
     ],
```

### Comparing `hcgf-0.1.0/tests/test_dataloader.py` & `hcgf-0.2.0/tests/test_dataloader.py`

 * *Files 4% similar despite different names*

```diff
@@ -33,24 +33,24 @@
     assert len(v.input_ids) == expected
 
 
 arr_dtype = np.int64
 
 input_ids = np.array(
     [
-        [5, 94874, 94874, 94874, 130001, 130004, 5, 88443, 2],
-        [5, 94874, 130001, 130004, 5, 84480, 2, 2, 2],
+        [5, 94874, 94874, 94874, 130001, 130004, 5, 88443, 130005],
+        [5, 94874, 130001, 130004, 5, 84480, 130005, 3, 3],
     ],
     dtype=arr_dtype
 )
 
 labels = np.array(
     [
-        [-100, -100, -100, -100, -100, 130004, 5, 88443, 2],
-        [-100, -100, -100, 130004, 5, 84480, 2, -100, -100],
+        [-100, -100, -100, -100, -100, 130004, 5, 88443, 130005],
+        [-100, -100, -100, 130004, 5, 84480, 130005, -100, -100],
     ],
     dtype=arr_dtype
 )
 
 position_ids = np.array(
     [
         [[0, 1, 2, 3, 4, 4, 4, 4, 4],
@@ -93,14 +93,15 @@
     ("labels", (2, 9), labels),
 ])
 def test_data_collector(mocked_dataset, inp_key, shape, expected):
     binp = GlmDataCollector.collate_fn(mocked_dataset)
     assert type(binp) == dict
     val = binp[inp_key]
     assert tuple(val.shape) == shape
+    print(val.numpy())
     assert np.alltrue(val.numpy() == expected)
 
 
 @pytest.mark.parametrize("func,expected", [
     ("train_dev_split", Tuple),
     ("load", DataLoader),
 ])
```

### Comparing `hcgf-0.1.0/tests/test_lora_ft.py` & `hcgf-0.2.0/tests/test_lora_ft.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,51 +1,61 @@
 import os
 import shutil
 from pathlib import Path
 import pytest
 
-from hcgf.sft.lora_ft import GlmLora
+from hcgf.sft.ft import GlmLora
 
 
-@pytest.mark.slow
-@pytest.mark.parametrize("mode", ["8bit", "normal"])
-def test_lora_ft(glm_data_file, glm_tune_param, mode):
-    params = glm_tune_param
-    model_id = "THUDM/chatglm-6b"
+def run_ft(gl: GlmLora, glm_data_file: str, params: dict):
     p1 = "./test_output1/"
     p2 = "./test_output2/"
+    params["out_dir"] = p1
+    print("tuning...")
+    (gl
+    .load_data(glm_data_file, max_seq_len=32)
+    .tune(**params))
+    gl.eval()
+    q = "你是谁？"
+    response, history = gl.chat(q, temperature=0.2)
+    print(q, response)
+    params["out_dir"] = p2
+    print("\n\ntuning again...")
+    gl.tune(**params)
+    print("\n\ninference...")
+    out_dir = Path(os.path.join(params["out_dir"], "ckpt"))
+    best_ckpt = sorted(
+        out_dir.glob("*best*"), 
+        key=lambda x: int(x.stem.split("best-")[-1])
+    )[-1]
+    gl.load_pretrained(best_ckpt).eval()
+    response, history = gl.chat("你是谁？", temperature=0.2)
+    print(response)
+    assert 1, "should pass"
+
+    for path in [p1, p2]:
+        if os.path.exists(path):
+            shutil.rmtree(path)
+
+
+@pytest.mark.slow
+def test_lora_signle_gpu_ft(glm_data_file, glm_tune_param):
+    model_id = "THUDM/chatglm-6b"
+    gl = GlmLora(model_id, device="cuda:0")
+    run_ft(gl, glm_data_file, glm_tune_param)
+
+
+@pytest.mark.slow
+def test_lora_8bit_ft(glm_data_file, glm_tune_param):
+    model_id = "THUDM/chatglm-6b"
     no_bnb = False
-    if mode == "8bit":
-        try:
-            import bitsandbytes as bnb
-        except Exception:
-            no_bnb = True
-        if not no_bnb:
-            gl = GlmLora(model_id, load_in_8bit=True)
-    elif mode == "normal":
-        gl = GlmLora(model_id, device="cuda:0")
-    
+    try:
+        import bitsandbytes as bnb
+    except Exception:
+        no_bnb = True
     if no_bnb:
         pass
     else:
-        params["out_dir"] = p1
-        print("tuning...")
-        (gl
-        .load_data(glm_data_file, max_seq_len=32)
-        .tune(**params))
-        gl.eval()
-        response, history = gl.chat("你是谁？", temperature=0.2)
-        print(response)
-        params["out_dir"] = p2
-        print("\n\ntuning again...")
-        gl.tune(**params)
-        print("\n\ninference...")
-        out_dir = Path(os.path.join(params["out_dir"], "ckpt"))
-        last_ckpt = list(out_dir.glob("*last*"))[0]
-        gl.load_pretrained(last_ckpt).eval()
-        response, history = gl.chat("你是谁？", temperature=0.2)
-        print(response)
-        assert 1, "should pass"
+        gl = GlmLora(model_id, load_in_8bit=True)
+        run_ft(gl, glm_data_file, glm_tune_param)
     
-    for path in [p1, p2]:
-        if os.path.exists(path):
-            shutil.rmtree(path)
+
```

### Comparing `hcgf-0.1.0/tests/test_trainer.py` & `hcgf-0.2.0/tests/test_trainer.py`

 * *Files 10% similar despite different names*

```diff
@@ -48,16 +48,16 @@
 ]
 
 model = Model()
 
 
 @pytest.mark.parametrize("lr", [1e-1])
 @pytest.mark.parametrize("num_epochs", [1, 2])
-@pytest.mark.parametrize("warmup_steps", [None, 10])
-@pytest.mark.parametrize("accumulate_steps", [1, 8])
+@pytest.mark.parametrize("warmup_steps", [0, None, 0.5, 1])
+@pytest.mark.parametrize("accumulate_steps", [None, 1, 8])
 def test_trainer(lr, num_epochs, warmup_steps, accumulate_steps):
     out_path = "./test_output/"
     trainer = Trainer(
         lr,
         num_epochs,
         warmup_steps,
         accumulate_steps,
```

