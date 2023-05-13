# Comparing `tmp/ml-starter-0.0.37.tar.gz` & `tmp/ml-starter-0.0.38.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ml-starter-0.0.37.tar", last modified: Sat May 13 02:48:01 2023, max compression
+gzip compressed data, was "ml-starter-0.0.38.tar", last modified: Sat May 13 07:01:19 2023, max compression
```

## Comparing `ml-starter-0.0.37.tar` & `ml-starter-0.0.38.tar`

### file list

```diff
@@ -1,164 +1,164 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.785941 ml-starter-0.0.37/
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-05-13 02:47:49.000000 ml-starter-0.0.37/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 02:47:49.000000 ml-starter-0.0.37/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 02:48:01.785941 ml-starter-0.0.37/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1051 2023-05-13 02:47:49.000000 ml-starter-0.0.37/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.745941 ml-starter-0.0.37/ml/
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8973 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.745941 ml-starter-0.0.37/ml/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/common_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     2776 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5181 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/env.py
--rw-r--r--   0 runner    (1001) docker     (123)    25200 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/registry.py
--rw-r--r--   0 runner    (1001) docker     (123)     2086 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/state.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.749941 ml-starter-0.0.37/ml/launchers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1728 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/mp.py
--rw-r--r--   0 runner    (1001) docker     (123)    10045 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/slurm.py
--rw-r--r--   0 runner    (1001) docker     (123)     4184 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/torchrun.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.749941 ml-starter-0.0.37/ml/loggers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6500 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2967 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/meter.py
--rw-r--r--   0 runner    (1001) docker     (123)    44643 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/multi.py
--rw-r--r--   0 runner    (1001) docker     (123)     5243 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/stdout.py
--rw-r--r--   0 runner    (1001) docker     (123)    13602 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/tensorboard.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.753941 ml-starter-0.0.37/ml/lr_schedulers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      644 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/constant.py
--rw-r--r--   0 runner    (1001) docker     (123)     1783 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/cosine.py
--rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/cosine_decay.py
--rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/linear.py
--rw-r--r--   0 runner    (1001) docker     (123)      775 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/linear_no_decay.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.753941 ml-starter-0.0.37/ml/lr_schedulers/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/scripts/plot.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.757941 ml-starter-0.0.37/ml/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5408 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/activations.py
--rw-r--r--   0 runner    (1001) docker     (123)     3277 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8754 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/embeddings.py
--rw-r--r--   0 runner    (1001) docker     (123)     4600 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/init.py
--rw-r--r--   0 runner    (1001) docker     (123)    23911 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/lora.py
--rw-r--r--   0 runner    (1001) docker     (123)    12566 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/norms.py
--rw-r--r--   0 runner    (1001) docker     (123)    16207 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/parallel.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/models/pretrained/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    41249 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/clip.py
--rw-r--r--   0 runner    (1001) docker     (123)    31800 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/hubert.py
--rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/llama.py
--rw-r--r--   0 runner    (1001) docker     (123)    60772 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/sam.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/optimizers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adam.py
--rw-r--r--   0 runner    (1001) docker     (123)     4985 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adamw.py
--rw-r--r--   0 runner    (1001) docker     (123)     3432 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adan.py
--rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/sgd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6320 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/shampoo.py
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/types.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3592 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      454 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/launch.py
--rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/resolve.py
--rw-r--r--   0 runner    (1001) docker     (123)      927 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/stage.py
--rw-r--r--   0 runner    (1001) docker     (123)     2062 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/train.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.765941 ml-starter-0.0.37/ml/tasks/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18456 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.765941 ml-starter-0.0.37/ml/tasks/datasets/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2098 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/async_iterable.py
--rw-r--r--   0 runner    (1001) docker     (123)     3841 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/clippify.py
--rw-r--r--   0 runner    (1001) docker     (123)     7327 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/collate.py
--rw-r--r--   0 runner    (1001) docker     (123)    10047 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/error_handling.py
--rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/multi_iter.py
--rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/samplers.py
--rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/streaming.py
--rw-r--r--   0 runner    (1001) docker     (123)     6998 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1509 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/video_file.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/environments/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    13448 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/worker.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/losses/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/losses/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1245 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/losses/reduce.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/rl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18535 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3826 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/replay.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/sl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/sl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/sl/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/trainers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20655 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.773941 ml-starter-0.0.37/ml/trainers/mixins/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2174 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/compile.py
--rw-r--r--   0 runner    (1001) docker     (123)     9190 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/cpu_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     4474 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/data_parallel.py
--rw-r--r--   0 runner    (1001) docker     (123)     8827 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/gpu_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     4445 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/grad_clipping.py
--rw-r--r--   0 runner    (1001) docker     (123)     4591 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/heartbeat.py
--rw-r--r--   0 runner    (1001) docker     (123)     3587 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/mixed_precision.py
--rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/monitor_process.py
--rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/profiler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/step_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     7701 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/rl.py
--rw-r--r--   0 runner    (1001) docker     (123)     9838 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/sl.py
--rw-r--r--   0 runner    (1001) docker     (123)     8798 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/vanilla.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.781941 ml-starter-0.0.37/ml/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3726 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/argparse.py
--rw-r--r--   0 runner    (1001) docker     (123)     3297 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/atomic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/augmentation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4361 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/caching.py
--rw-r--r--   0 runner    (1001) docker     (123)     5070 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/checkpoint.py
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/checks.py
--rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     1303 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/colors.py
--rw-r--r--   0 runner    (1001) docker     (123)      698 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4941 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/data.py
--rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/datetime.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.781941 ml-starter-0.0.37/ml/utils/device/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/auto.py
--rw-r--r--   0 runner    (1001) docker     (123)     8885 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)     1753 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/gpu.py
--rw-r--r--   0 runner    (1001) docker     (123)      829 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/metal.py
--rw-r--r--   0 runner    (1001) docker     (123)     4114 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/distributed.py
--rw-r--r--   0 runner    (1001) docker     (123)     5222 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/image.py
--rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/large_models.py
--rw-r--r--   0 runner    (1001) docker     (123)     4831 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     2588 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/meter.py
--rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/networking.py
--rw-r--r--   0 runner    (1001) docker     (123)      438 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/numpy.py
--rw-r--r--   0 runner    (1001) docker     (123)     9981 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/parallel.py
--rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/random.py
--rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/staging.py
--rw-r--r--   0 runner    (1001) docker     (123)     4993 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/timer.py
--rw-r--r--   0 runner    (1001) docker     (123)     7915 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/torch_distributed.py
--rw-r--r--   0 runner    (1001) docker     (123)    13637 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/video.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.785941 ml-starter-0.0.37/ml_starter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      251 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        3 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-05-13 02:47:49.000000 ml-starter-0.0.37/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements-docs.txt
--rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 02:48:01.785941 ml-starter-0.0.37/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-05-13 02:47:49.000000 ml-starter-0.0.37/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.927616 ml-starter-0.0.38/
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-05-13 07:01:02.000000 ml-starter-0.0.38/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 07:01:02.000000 ml-starter-0.0.38/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 07:01:19.927616 ml-starter-0.0.38/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1051 2023-05-13 07:01:02.000000 ml-starter-0.0.38/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.895616 ml-starter-0.0.38/ml/
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9054 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.895616 ml-starter-0.0.38/ml/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/common_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2776 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5181 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/env.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25200 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/registry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2086 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/core/state.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.899616 ml-starter-0.0.38/ml/launchers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/launchers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/launchers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1823 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/launchers/mp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10045 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/launchers/slurm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4184 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/launchers/torchrun.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.899616 ml-starter-0.0.38/ml/loggers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6500 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2967 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/meter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44643 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/multi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5243 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/stdout.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13602 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/loggers/tensorboard.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.899616 ml-starter-0.0.38/ml/lr_schedulers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      644 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1783 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/cosine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/cosine_decay.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/linear.py
+-rw-r--r--   0 runner    (1001) docker     (123)      775 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/linear_no_decay.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.899616 ml-starter-0.0.38/ml/lr_schedulers/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/lr_schedulers/scripts/plot.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.903616 ml-starter-0.0.38/ml/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5408 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/activations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3297 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8754 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/embeddings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4600 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/init.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23911 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/lora.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12566 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/norms.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16201 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/parallel.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.903616 ml-starter-0.0.38/ml/models/pretrained/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/pretrained/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41249 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/pretrained/clip.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31800 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/pretrained/hubert.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22211 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/pretrained/llama.py
+-rw-r--r--   0 runner    (1001) docker     (123)    60772 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/models/pretrained/sam.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.907616 ml-starter-0.0.38/ml/optimizers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/adam.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4985 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/adamw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3432 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/adan.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/sgd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6320 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/shampoo.py
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/optimizers/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.907616 ml-starter-0.0.38/ml/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3592 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      454 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/launch.py
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/resolve.py
+-rw-r--r--   0 runner    (1001) docker     (123)      927 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/stage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2062 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/scripts/train.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.907616 ml-starter-0.0.38/ml/tasks/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18456 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.911616 ml-starter-0.0.38/ml/tasks/datasets/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2098 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/async_iterable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3841 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/clippify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7327 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/collate.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10047 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/error_handling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/multi_iter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/samplers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/streaming.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6998 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1509 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/datasets/video_file.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.911616 ml-starter-0.0.38/ml/tasks/environments/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/environments/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/environments/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/environments/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13448 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/environments/worker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.911616 ml-starter-0.0.38/ml/tasks/losses/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/losses/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1245 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/losses/reduce.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.911616 ml-starter-0.0.38/ml/tasks/rl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/rl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18535 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/rl/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3826 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/rl/replay.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.911616 ml-starter-0.0.38/ml/tasks/sl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/sl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/tasks/sl/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.915616 ml-starter-0.0.38/ml/trainers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20655 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.915616 ml-starter-0.0.38/ml/trainers/mixins/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2174 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/compile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9190 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/cpu_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4478 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/data_parallel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8827 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/gpu_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4445 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/grad_clipping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4591 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/heartbeat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3587 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/mixed_precision.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/monitor_process.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/profiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/mixins/step_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7701 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/rl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9838 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/sl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8798 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/trainers/vanilla.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.923616 ml-starter-0.0.38/ml/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3726 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/argparse.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3297 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/atomic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/augmentation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4361 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/caching.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5070 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/checkpoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1303 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/colors.py
+-rw-r--r--   0 runner    (1001) docker     (123)      698 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4941 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/datetime.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.923616 ml-starter-0.0.38/ml/utils/device/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/auto.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8885 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1753 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/gpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)      829 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/device/metal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4114 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/distributed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5222 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/large_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4831 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2588 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/meter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/networking.py
+-rw-r--r--   0 runner    (1001) docker     (123)      438 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/numpy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9981 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/parallel.py
+-rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/random.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/staging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4993 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7917 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/torch_distributed.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13637 2023-05-13 07:01:02.000000 ml-starter-0.0.38/ml/utils/video.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:01:19.927616 ml-starter-0.0.38/ml_starter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 07:01:19.000000 ml-starter-0.0.38/ml_starter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-05-13 07:01:19.000000 ml-starter-0.0.38/ml_starter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 07:01:19.000000 ml-starter-0.0.38/ml_starter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      251 2023-05-13 07:01:19.000000 ml-starter-0.0.38/ml_starter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        3 2023-05-13 07:01:19.000000 ml-starter-0.0.38/ml_starter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-05-13 07:01:02.000000 ml-starter-0.0.38/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 07:01:02.000000 ml-starter-0.0.38/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 07:01:02.000000 ml-starter-0.0.38/requirements-docs.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 07:01:02.000000 ml-starter-0.0.38/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 07:01:19.927616 ml-starter-0.0.38/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-05-13 07:01:02.000000 ml-starter-0.0.38/setup.py
```

### Comparing `ml-starter-0.0.37/LICENSE` & `ml-starter-0.0.38/LICENSE`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/PKG-INFO` & `ml-starter-0.0.38/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ml-starter
-Version: 0.0.37
+Version: 0.0.38
 Summary: ML project template repository
 Home-page: https://github.com/codekansas/ml-starter
 Author: Benjamin Bolte
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ml-starter-0.0.37/README.md` & `ml-starter-0.0.38/README.md`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/api.py` & `ml-starter-0.0.38/ml/api.py`

 * *Files 2% similar despite different names*

```diff
@@ -156,14 +156,15 @@
     "SupervisedLearningTask",
     "SupervisedLearningTaskConfig",
     "SupervisedLearningTrainer",
     "SupervisedLearningTrainerConfig",
     "SyncEnvironmentWorker",
     "SyncWorkerPool",
     "test_dataset",
+    "test_environment",
     "timeout",
     "Timer",
     "transforms",
     "VanillaTrainer",
     "VanillaTrainerConfig",
     "VideoFileDataset",
     "WorkerPool",
@@ -221,14 +222,15 @@
 from ml.tasks.datasets.collate import CollateMode, collate, collate_non_null, pad_all, pad_sequence
 from ml.tasks.datasets.multi_iter import MultiIterDataset
 from ml.tasks.datasets.samplers import ChunkSampler
 from ml.tasks.datasets.streaming import StreamingDataset, StreamingDatasetNoIndex
 from ml.tasks.datasets.utils import test_dataset
 from ml.tasks.datasets.video_file import VideoFileDataset
 from ml.tasks.environments.base import Environment
+from ml.tasks.environments.utils import test_environment
 from ml.tasks.environments.worker import (
     AsyncEnvironmentWorker,
     AsyncWorkerPool,
     BaseEnvironmentWorker,
     SyncEnvironmentWorker,
     SyncWorkerPool,
     WorkerPool,
@@ -240,14 +242,15 @@
 from ml.trainers.rl import ReinforcementLearningTrainer, ReinforcementLearningTrainerConfig
 from ml.trainers.sl import SupervisedLearningTrainer, SupervisedLearningTrainerConfig
 from ml.trainers.vanilla import VanillaTrainer, VanillaTrainerConfig
 from ml.utils.argparse import from_args, get_args, get_type_from_string
 from ml.utils.atomic import atomic_save, open_atomic
 from ml.utils.augmentation import get_image_mask
 from ml.utils.caching import DictIndex, cached_object
+from ml.utils.checkpoint import instantiate_config, load_model_and_task
 from ml.utils.checks import assert_no_nans
 from ml.utils.colors import colorize
 from ml.utils.data import check_md5, check_sha256, get_dataset_split_for_phase, get_dataset_splits, get_worker_info
 from ml.utils.datetime import format_timedelta
 from ml.utils.device.auto import AutoDevice
 from ml.utils.device.base import BaseDevice
 from ml.utils.distributed import (
@@ -262,15 +265,14 @@
     get_rank_optional,
     get_world_size,
     get_world_size_optional,
     is_distributed,
     is_master,
 )
 from ml.utils.image import read_gif, write_gif
-from ml.utils.checkpoint import instantiate_config, load_model_and_task
 from ml.utils.large_models import init_empty_weights, meta_to_empty_func
 from ml.utils.logging import configure_logging
 from ml.utils.numpy import as_cpu_tensor, as_numpy_array
 from ml.utils.parallel import init_parallelism, parallel_group_info, parallelism_is_initialized, reset_parallelism
 from ml.utils.random import set_random_seed
 from ml.utils.staging import stage_environment
 from ml.utils.timer import Timer, timeout
```

### Comparing `ml-starter-0.0.37/ml/core/common_types.py` & `ml-starter-0.0.38/ml/core/common_types.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/core/config.py` & `ml-starter-0.0.38/ml/core/config.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/core/env.py` & `ml-starter-0.0.38/ml/core/env.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/core/registry.py` & `ml-starter-0.0.38/ml/core/registry.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/core/state.py` & `ml-starter-0.0.38/ml/core/state.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/launchers/base.py` & `ml-starter-0.0.38/ml/launchers/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/launchers/mp.py` & `ml-starter-0.0.38/ml/launchers/mp.py`

 * *Files 13% similar despite different names*

```diff
@@ -33,18 +33,22 @@
     multiprocess: MultiprocessConfig = conf_field(MultiprocessConfig())
 
     @classmethod
     def resolve(cls: type["MultiProcessLauncherConfig"], config: "MultiProcessLauncherConfig") -> None:
         super().resolve(config)
 
         # Resolve multiprocess config.
-        config.multiprocess.resolve()
+        MultiprocessConfig.resolve(config.multiprocess)
 
 
 @register_launcher("mp", MultiProcessLauncherConfig)
 class MultiProcessLauncher(BaseLauncher[MultiProcessLauncherConfig]):
     def launch(self) -> None:
         if not torch.cuda.is_available():
             raise RuntimeError("MultiProcessLauncher requires CUDA")
 
-        func = functools.partial(process_main, raw_config=self.raw_config)
+        func = functools.partial(
+            process_main,
+            cfg=self.config.multiprocess,
+            raw_config=self.raw_config,
+        )
         launch_subprocesses(func, self.config.multiprocess)
```

### Comparing `ml-starter-0.0.37/ml/launchers/slurm.py` & `ml-starter-0.0.38/ml/launchers/slurm.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/launchers/torchrun.py` & `ml-starter-0.0.38/ml/launchers/torchrun.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/loggers/base.py` & `ml-starter-0.0.38/ml/loggers/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/loggers/meter.py` & `ml-starter-0.0.38/ml/loggers/meter.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/loggers/multi.py` & `ml-starter-0.0.38/ml/loggers/multi.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/loggers/stdout.py` & `ml-starter-0.0.38/ml/loggers/stdout.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/loggers/tensorboard.py` & `ml-starter-0.0.38/ml/loggers/tensorboard.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/base.py` & `ml-starter-0.0.38/ml/lr_schedulers/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/constant.py` & `ml-starter-0.0.38/ml/lr_schedulers/constant.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/cosine.py` & `ml-starter-0.0.38/ml/lr_schedulers/cosine.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/cosine_decay.py` & `ml-starter-0.0.38/ml/lr_schedulers/cosine_decay.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/linear.py` & `ml-starter-0.0.38/ml/lr_schedulers/linear.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/linear_no_decay.py` & `ml-starter-0.0.38/ml/lr_schedulers/linear_no_decay.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/lr_schedulers/scripts/plot.py` & `ml-starter-0.0.38/ml/lr_schedulers/scripts/plot.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/activations.py` & `ml-starter-0.0.38/ml/models/activations.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/base.py` & `ml-starter-0.0.38/ml/models/base.py`

 * *Files 4% similar despite different names*

```diff
@@ -47,26 +47,26 @@
                 return t
             if t.is_floating_point():
                 return t.to(device=device, dtype=dtype, non_blocking=allow_nonblocking(device, t.device))
             return t.to(device=device, non_blocking=allow_nonblocking(device, t.device))
 
         self._apply(move_to_device)
 
-        bad_params = {(name, p.device) for name, p in self.named_parameters() if p.device != device}
+        bad_params = {(name, p.device) for name, p in self.named_parameters() if p.device.type != device.type}
         if bad_params:
             bad_param_names = sorted(list(bad_params))[:5]
             logger.warning(
                 "Got %d params which are on a different device from %s. First %d:%s",
                 len(bad_params),
                 device,
                 len(bad_param_names),
                 summarize(bad_param_names),
             )
 
-        bad_buffers = {(name, b.device) for name, b in self.named_buffers() if b.device != device}
+        bad_buffers = {(name, b.device) for name, b in self.named_buffers() if b.device.type != device.type}
         if bad_buffers:
             bad_buffer_names = sorted(list(bad_buffers))[:5]
             logger.warning(
                 "Got %d buffers which are on a different device from %s. First %d:\n%s",
                 len(bad_buffers),
                 device,
                 len(bad_buffer_names),
```

### Comparing `ml-starter-0.0.37/ml/models/embeddings.py` & `ml-starter-0.0.38/ml/models/embeddings.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/init.py` & `ml-starter-0.0.38/ml/models/init.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/lora.py` & `ml-starter-0.0.38/ml/models/lora.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/norms.py` & `ml-starter-0.0.38/ml/models/norms.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/parallel.py` & `ml-starter-0.0.38/ml/models/parallel.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 """Defines primitive model parallel layers.
 
 Before using this module, you should initialize the parallel process groups
-using :func:`ml.utils.parallel.initialize_parallelism`. This will create
+using :func:`ml.utils.parallel.init_parallelism`. This will create
 three process group for model parallelism, pipeline parallelism, and data
 parallelism. The process group information can be accessed using
 :func:`ml.utils.parallel.parallel_group_info`.
 
 The following layers are defined:
 
 - :class:`ParallelEmbedding`: A model-parallel embedding layer.
```

### Comparing `ml-starter-0.0.37/ml/models/pretrained/clip.py` & `ml-starter-0.0.38/ml/models/pretrained/clip.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/pretrained/hubert.py` & `ml-starter-0.0.38/ml/models/pretrained/hubert.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/models/pretrained/llama.py` & `ml-starter-0.0.38/ml/models/pretrained/llama.py`

 * *Files 0% similar despite different names*

```diff
@@ -568,17 +568,17 @@
     )
 
     logger.info("Generated: %s", generated)
 
 
 def setup() -> None:
     # Hides some nuisance logs.
-    # logging.getLogger("torch.distributed").setLevel(logging.ERROR)
-    # logging.getLogger("torch.nn.parallel.distributed").setLevel(logging.ERROR)
-    # logging.getLogger("ml.utils.torch_distributed").setLevel(logging.ERROR)
+    logging.getLogger("torch.distributed").setLevel(logging.ERROR)
+    logging.getLogger("torch.nn.parallel.distributed").setLevel(logging.ERROR)
+    logging.getLogger("ml.utils.torch_distributed").setLevel(logging.ERROR)
 
     # Setting the seed across all processes to make sure that the weights
     # initialize to the same values (needed to make the test pass).
     torch.manual_seed(1337)
 
 
 def test_pretrained_model() -> None:
```

### Comparing `ml-starter-0.0.37/ml/models/pretrained/sam.py` & `ml-starter-0.0.38/ml/models/pretrained/sam.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/adam.py` & `ml-starter-0.0.38/ml/optimizers/adam.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/adamw.py` & `ml-starter-0.0.38/ml/optimizers/adamw.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/adan.py` & `ml-starter-0.0.38/ml/optimizers/adan.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/base.py` & `ml-starter-0.0.38/ml/optimizers/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/sgd.py` & `ml-starter-0.0.38/ml/optimizers/sgd.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/optimizers/shampoo.py` & `ml-starter-0.0.38/ml/optimizers/shampoo.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/scripts/cli.py` & `ml-starter-0.0.38/ml/scripts/cli.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/scripts/stage.py` & `ml-starter-0.0.38/ml/scripts/stage.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/scripts/train.py` & `ml-starter-0.0.38/ml/scripts/train.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/base.py` & `ml-starter-0.0.38/ml/tasks/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/async_iterable.py` & `ml-starter-0.0.38/ml/tasks/datasets/async_iterable.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/clippify.py` & `ml-starter-0.0.38/ml/tasks/datasets/clippify.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/collate.py` & `ml-starter-0.0.38/ml/tasks/datasets/collate.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/error_handling.py` & `ml-starter-0.0.38/ml/tasks/datasets/error_handling.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/multi_iter.py` & `ml-starter-0.0.38/ml/tasks/datasets/multi_iter.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/samplers.py` & `ml-starter-0.0.38/ml/tasks/datasets/samplers.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/streaming.py` & `ml-starter-0.0.38/ml/tasks/datasets/streaming.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/transforms.py` & `ml-starter-0.0.38/ml/tasks/datasets/transforms.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/utils.py` & `ml-starter-0.0.38/ml/tasks/datasets/utils.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/datasets/video_file.py` & `ml-starter-0.0.38/ml/tasks/datasets/video_file.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/environments/base.py` & `ml-starter-0.0.38/ml/tasks/environments/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/environments/utils.py` & `ml-starter-0.0.38/ml/tasks/environments/utils.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/environments/worker.py` & `ml-starter-0.0.38/ml/tasks/environments/worker.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/losses/reduce.py` & `ml-starter-0.0.38/ml/tasks/losses/reduce.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/rl/base.py` & `ml-starter-0.0.38/ml/tasks/rl/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/rl/replay.py` & `ml-starter-0.0.38/ml/tasks/rl/replay.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/tasks/sl/base.py` & `ml-starter-0.0.38/ml/tasks/sl/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/base.py` & `ml-starter-0.0.38/ml/trainers/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/compile.py` & `ml-starter-0.0.38/ml/trainers/mixins/compile.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/cpu_stats.py` & `ml-starter-0.0.38/ml/trainers/mixins/cpu_stats.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/data_parallel.py` & `ml-starter-0.0.38/ml/trainers/mixins/data_parallel.py`

 * *Files 0% similar despite different names*

```diff
@@ -119,9 +119,9 @@
     """Defines a trainer mixin for fully sharded data parallel models."""
 
     def _get_task_model(self, task: TaskT, model: ModelT) -> nn.Module:
         device, dtype = self._device.get_device(), self._weight_precision
         model.init(device, dtype)
         task.to(device, dtype)
         task_model: nn.Module = TaskModel(task=task, model=model)
-        task_model = dp(task_model, self.config.fsdp)
+        task_model = dp(task_model, self.config.parallel)
         return task_model
```

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/gpu_stats.py` & `ml-starter-0.0.38/ml/trainers/mixins/gpu_stats.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/grad_clipping.py` & `ml-starter-0.0.38/ml/trainers/mixins/grad_clipping.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/heartbeat.py` & `ml-starter-0.0.38/ml/trainers/mixins/heartbeat.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/mixed_precision.py` & `ml-starter-0.0.38/ml/trainers/mixins/mixed_precision.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/monitor_process.py` & `ml-starter-0.0.38/ml/trainers/mixins/monitor_process.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/profiler.py` & `ml-starter-0.0.38/ml/trainers/mixins/profiler.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/mixins/step_wrapper.py` & `ml-starter-0.0.38/ml/trainers/mixins/step_wrapper.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/rl.py` & `ml-starter-0.0.38/ml/trainers/rl.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/sl.py` & `ml-starter-0.0.38/ml/trainers/sl.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/trainers/vanilla.py` & `ml-starter-0.0.38/ml/trainers/vanilla.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/argparse.py` & `ml-starter-0.0.38/ml/utils/argparse.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/atomic.py` & `ml-starter-0.0.38/ml/utils/atomic.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/augmentation.py` & `ml-starter-0.0.38/ml/utils/augmentation.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/caching.py` & `ml-starter-0.0.38/ml/utils/caching.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/checkpoint.py` & `ml-starter-0.0.38/ml/utils/checkpoint.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/cli.py` & `ml-starter-0.0.38/ml/utils/cli.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/colors.py` & `ml-starter-0.0.38/ml/utils/colors.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/config.py` & `ml-starter-0.0.38/ml/utils/config.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/data.py` & `ml-starter-0.0.38/ml/utils/data.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/datetime.py` & `ml-starter-0.0.38/ml/utils/datetime.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/device/auto.py` & `ml-starter-0.0.38/ml/utils/device/auto.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/device/base.py` & `ml-starter-0.0.38/ml/utils/device/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/device/cpu.py` & `ml-starter-0.0.38/ml/utils/device/cpu.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/device/gpu.py` & `ml-starter-0.0.38/ml/utils/device/gpu.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/device/metal.py` & `ml-starter-0.0.38/ml/utils/device/metal.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/distributed.py` & `ml-starter-0.0.38/ml/utils/distributed.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/image.py` & `ml-starter-0.0.38/ml/utils/image.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/large_models.py` & `ml-starter-0.0.38/ml/utils/large_models.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/logging.py` & `ml-starter-0.0.38/ml/utils/logging.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/meter.py` & `ml-starter-0.0.38/ml/utils/meter.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/parallel.py` & `ml-starter-0.0.38/ml/utils/parallel.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/staging.py` & `ml-starter-0.0.38/ml/utils/staging.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/timer.py` & `ml-starter-0.0.38/ml/utils/timer.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml/utils/torch_distributed.py` & `ml-starter-0.0.38/ml/utils/torch_distributed.py`

 * *Files 6% similar despite different names*

```diff
@@ -42,36 +42,36 @@
     pipeline_parallelism: int = conf_field(1, help="The number of pipeline parallel processes")
     backend: str | None = conf_field(None, help="The distributed backend")
     model_parallel_backend: str | None = conf_field(None, help="The model parallel backend")
     pipeline_parallel_backend: str | None = conf_field(None, help="The pipeline parallel backend")
     data_parallel_backend: str | None = conf_field(None, help="The data parallel backend")
     launch_method: str = conf_field("forkserver", help="The launch method for multiprocessing")
 
-    def resolve(self) -> None:
+    @classmethod
+    def resolve(cls, config: "MultiprocessConfig") -> None:
         device_count = torch.cuda.device_count() if torch.cuda.is_available() else 1
-        if is_missing(self, "world_size"):
-            self.world_size = device_count
-        if is_missing(self, "local_world_size"):
-            self.local_world_size = min(device_count, self.world_size)
-        if is_missing(self, "master_port"):
-            self.master_port = get_unused_port()
+        if is_missing(config, "world_size"):
+            config.world_size = device_count
+        if is_missing(config, "local_world_size"):
+            config.local_world_size = min(device_count, config.world_size)
+        if is_missing(config, "master_port"):
+            config.master_port = get_unused_port()
 
 
 def init_process_group_from_backend(backend: str | dist.Backend | None = None) -> None:
     if backend is None:
         backend = get_distributed_backend()
     init_method, world_size, rank = get_init_method(), get_world_size(), get_rank()
 
     logger.log(INFOALL, "Initializing %d / %d using %s - %s", rank, world_size, init_method, backend)
     dist.init_process_group(backend=backend, init_method=init_method, world_size=world_size, rank=rank)
 
     if torch.cuda.is_available():
         device_count = torch.cuda.device_count()
         torch.cuda.set_device(rank % device_count)
-        torch.set_default_device(torch.device("cuda", rank % device_count))
 
     logger.info("Initialized process group; running dummy all-reduce")
     dist.all_reduce(torch.zeros(1, device="cuda" if torch.cuda.is_available() else "cpu"))
     logger.info("Dummy all-reduce succeeded")
 
 
 def init_dist(
@@ -176,15 +176,15 @@
         func: The function to launch.
         cfg: The configuration for the function.
         setup: A function to run before launching the subprocesses.
 
     Raises:
         RuntimeError: If the function fails in any subprocess.
     """
-    cfg.resolve()
+    MultiprocessConfig.resolve(cfg)
 
     if cfg.world_size <= 1:
         logger.warning("Multi-process trainer expects more than one device; running single-process")
         cfg.rank = 0
         init_and_run(func, cfg)
         return
```

### Comparing `ml-starter-0.0.37/ml/utils/video.py` & `ml-starter-0.0.38/ml/utils/video.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/ml_starter.egg-info/PKG-INFO` & `ml-starter-0.0.38/ml_starter.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ml-starter
-Version: 0.0.37
+Version: 0.0.38
 Summary: ML project template repository
 Home-page: https://github.com/codekansas/ml-starter
 Author: Benjamin Bolte
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ml-starter-0.0.37/ml_starter.egg-info/SOURCES.txt` & `ml-starter-0.0.38/ml_starter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/pyproject.toml` & `ml-starter-0.0.38/pyproject.toml`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.37/setup.py` & `ml-starter-0.0.38/setup.py`

 * *Files identical despite different names*

