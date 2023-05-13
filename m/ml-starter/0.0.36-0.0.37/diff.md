# Comparing `tmp/ml-starter-0.0.36.tar.gz` & `tmp/ml-starter-0.0.37.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ml-starter-0.0.36.tar", last modified: Wed May 10 08:26:08 2023, max compression
+gzip compressed data, was "ml-starter-0.0.37.tar", last modified: Sat May 13 02:48:01 2023, max compression
```

## Comparing `ml-starter-0.0.36.tar` & `ml-starter-0.0.37.tar`

### file list

```diff
@@ -1,159 +1,164 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.388968 ml-starter-0.0.36/
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-05-10 08:25:54.000000 ml-starter-0.0.36/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-10 08:25:54.000000 ml-starter-0.0.36/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-10 08:26:08.388968 ml-starter-0.0.36/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1051 2023-05-10 08:25:54.000000 ml-starter-0.0.36/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7625 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/common_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     2534 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5043 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/env.py
--rw-r--r--   0 runner    (1001) docker     (123)    24979 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/registry.py
--rw-r--r--   0 runner    (1001) docker     (123)     2068 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/core/state.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/launchers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/launchers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      587 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/launchers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     4777 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/launchers/ddp.py
--rw-r--r--   0 runner    (1001) docker     (123)    10067 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/launchers/slurm.py
--rw-r--r--   0 runner    (1001) docker     (123)     4185 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/launchers/torchrun.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/loggers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6276 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2814 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/meter.py
--rw-r--r--   0 runner    (1001) docker     (123)    44298 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/multi.py
--rw-r--r--   0 runner    (1001) docker     (123)     4962 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/stdout.py
--rw-r--r--   0 runner    (1001) docker     (123)    13168 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/loggers/tensorboard.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/lr_schedulers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1892 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      474 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/constant.py
--rw-r--r--   0 runner    (1001) docker     (123)     1734 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/cosine.py
--rw-r--r--   0 runner    (1001) docker     (123)     2342 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/cosine_decay.py
--rw-r--r--   0 runner    (1001) docker     (123)     1639 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/linear.py
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/linear_no_decay.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.372968 ml-starter-0.0.36/ml/lr_schedulers/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1878 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/lr_schedulers/scripts/plot.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.376968 ml-starter-0.0.36/ml/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5409 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/activations.py
--rw-r--r--   0 runner    (1001) docker     (123)     3151 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8758 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/embeddings.py
--rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/init.py
--rw-r--r--   0 runner    (1001) docker     (123)    24040 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/lora.py
--rw-r--r--   0 runner    (1001) docker     (123)    12570 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/norms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.376968 ml-starter-0.0.36/ml/models/pretrained/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/pretrained/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    41234 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/pretrained/clip.py
--rw-r--r--   0 runner    (1001) docker     (123)    31736 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/pretrained/hubert.py
--rw-r--r--   0 runner    (1001) docker     (123)    60669 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/models/pretrained/sam.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.376968 ml-starter-0.0.36/ml/optimizers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1726 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/adam.py
--rw-r--r--   0 runner    (1001) docker     (123)     4935 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/adamw.py
--rw-r--r--   0 runner    (1001) docker     (123)     3382 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/adan.py
--rw-r--r--   0 runner    (1001) docker     (123)      879 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1120 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/sgd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6149 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/shampoo.py
--rw-r--r--   0 runner    (1001) docker     (123)      297 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/optimizers/types.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.376968 ml-starter-0.0.36/ml/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2703 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      392 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/launch.py
--rw-r--r--   0 runner    (1001) docker     (123)      251 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/resolve.py
--rw-r--r--   0 runner    (1001) docker     (123)      887 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/stage.py
--rw-r--r--   0 runner    (1001) docker     (123)     2031 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/scripts/train.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.376968 ml-starter-0.0.36/ml/tasks/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17884 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/tasks/datasets/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1569 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/async_iterable.py
--rw-r--r--   0 runner    (1001) docker     (123)     3778 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/clippify.py
--rw-r--r--   0 runner    (1001) docker     (123)     7256 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/collate.py
--rw-r--r--   0 runner    (1001) docker     (123)     9774 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/error_handling.py
--rw-r--r--   0 runner    (1001) docker     (123)     2345 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/multi_iter.py
--rw-r--r--   0 runner    (1001) docker     (123)     1552 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/samplers.py
--rw-r--r--   0 runner    (1001) docker     (123)     4615 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/streaming.py
--rw-r--r--   0 runner    (1001) docker     (123)     6692 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     1232 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1431 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/datasets/video_file.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/tasks/environments/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/environments/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/environments/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1611 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/environments/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    13450 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/environments/worker.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/tasks/losses/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/losses/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      931 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/losses/reduce.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/tasks/rl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/rl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17653 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/rl/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     3814 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/rl/replay.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/tasks/sl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/sl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1223 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/tasks/sl/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.380968 ml-starter-0.0.36/ml/trainers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20195 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/base.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.384968 ml-starter-0.0.36/ml/trainers/mixins/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8897 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/cpu_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     8654 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/gpu_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     3405 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/grad_clipping.py
--rw-r--r--   0 runner    (1001) docker     (123)     4419 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/heartbeat.py
--rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/mixed_precision.py
--rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/monitor_process.py
--rw-r--r--   0 runner    (1001) docker     (123)     5598 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/profiler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1262 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/mixins/step_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     7713 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/rl.py
--rw-r--r--   0 runner    (1001) docker     (123)     9857 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/sl.py
--rw-r--r--   0 runner    (1001) docker     (123)    11038 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/trainers/vanilla.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.388968 ml-starter-0.0.36/ml/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3709 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/argparse.py
--rw-r--r--   0 runner    (1001) docker     (123)     3295 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/atomic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/augmentation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4381 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/caching.py
--rw-r--r--   0 runner    (1001) docker     (123)      969 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/call_train.py
--rw-r--r--   0 runner    (1001) docker     (123)      162 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/checks.py
--rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/colors.py
--rw-r--r--   0 runner    (1001) docker     (123)     4886 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/data.py
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/datetime.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.388968 ml-starter-0.0.36/ml/utils/device/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1373 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/auto.py
--rw-r--r--   0 runner    (1001) docker     (123)     8348 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      524 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)     1572 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/gpu.py
--rw-r--r--   0 runner    (1001) docker     (123)      765 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/device/metal.py
--rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/distributed.py
--rw-r--r--   0 runner    (1001) docker     (123)     5127 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/image.py
--rw-r--r--   0 runner    (1001) docker     (123)     4856 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/io.py
--rw-r--r--   0 runner    (1001) docker     (123)     2388 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/large_models.py
--rw-r--r--   0 runner    (1001) docker     (123)     4585 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/meter.py
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/networking.py
--rw-r--r--   0 runner    (1001) docker     (123)      388 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/numpy.py
--rw-r--r--   0 runner    (1001) docker     (123)      317 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/random.py
--rw-r--r--   0 runner    (1001) docker     (123)     3042 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/staging.py
--rw-r--r--   0 runner    (1001) docker     (123)     4854 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/timer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1401 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/torch_distributed.py
--rw-r--r--   0 runner    (1001) docker     (123)    13201 2023-05-10 08:25:54.000000 ml-starter-0.0.36/ml/utils/video.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 08:26:08.388968 ml-starter-0.0.36/ml_starter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-10 08:26:08.000000 ml-starter-0.0.36/ml_starter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3250 2023-05-10 08:26:08.000000 ml-starter-0.0.36/ml_starter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 08:26:08.000000 ml-starter-0.0.36/ml_starter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      251 2023-05-10 08:26:08.000000 ml-starter-0.0.36/ml_starter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        3 2023-05-10 08:26:08.000000 ml-starter-0.0.36/ml_starter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-05-10 08:25:54.000000 ml-starter-0.0.36/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-10 08:25:54.000000 ml-starter-0.0.36/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-10 08:25:54.000000 ml-starter-0.0.36/requirements-docs.txt
--rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-10 08:25:54.000000 ml-starter-0.0.36/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-10 08:26:08.392968 ml-starter-0.0.36/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-05-10 08:25:54.000000 ml-starter-0.0.36/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.785941 ml-starter-0.0.37/
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-05-13 02:47:49.000000 ml-starter-0.0.37/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 02:47:49.000000 ml-starter-0.0.37/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 02:48:01.785941 ml-starter-0.0.37/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1051 2023-05-13 02:47:49.000000 ml-starter-0.0.37/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.745941 ml-starter-0.0.37/ml/
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8973 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.745941 ml-starter-0.0.37/ml/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/common_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2776 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5181 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/env.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25200 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/registry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2086 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/core/state.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.749941 ml-starter-0.0.37/ml/launchers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1728 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/mp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10045 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/slurm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4184 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/launchers/torchrun.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.749941 ml-starter-0.0.37/ml/loggers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6500 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2967 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/meter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44643 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/multi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5243 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/stdout.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13602 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/loggers/tensorboard.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.753941 ml-starter-0.0.37/ml/lr_schedulers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      644 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1783 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/cosine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/cosine_decay.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/linear.py
+-rw-r--r--   0 runner    (1001) docker     (123)      775 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/linear_no_decay.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.753941 ml-starter-0.0.37/ml/lr_schedulers/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/lr_schedulers/scripts/plot.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.757941 ml-starter-0.0.37/ml/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5408 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/activations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3277 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8754 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/embeddings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4600 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/init.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23911 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/lora.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12566 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/norms.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16207 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/parallel.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/models/pretrained/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41249 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/clip.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31800 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/hubert.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/llama.py
+-rw-r--r--   0 runner    (1001) docker     (123)    60772 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/models/pretrained/sam.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/optimizers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adam.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4985 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adamw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3432 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/adan.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/sgd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6320 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/shampoo.py
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/optimizers/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.761941 ml-starter-0.0.37/ml/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3592 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      454 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/launch.py
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/resolve.py
+-rw-r--r--   0 runner    (1001) docker     (123)      927 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/stage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2062 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/scripts/train.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.765941 ml-starter-0.0.37/ml/tasks/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18456 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.765941 ml-starter-0.0.37/ml/tasks/datasets/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2098 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/async_iterable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3841 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/clippify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7327 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/collate.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10047 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/error_handling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/multi_iter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/samplers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/streaming.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6998 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1509 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/datasets/video_file.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/environments/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13448 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/environments/worker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/losses/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/losses/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1245 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/losses/reduce.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/rl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18535 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3826 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/rl/replay.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/tasks/sl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/sl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/tasks/sl/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.769941 ml-starter-0.0.37/ml/trainers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20655 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.773941 ml-starter-0.0.37/ml/trainers/mixins/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2174 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/compile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9190 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/cpu_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4474 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/data_parallel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8827 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/gpu_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4445 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/grad_clipping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4591 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/heartbeat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3587 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/mixed_precision.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/monitor_process.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/profiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/mixins/step_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7701 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/rl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9838 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/sl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8798 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/trainers/vanilla.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.781941 ml-starter-0.0.37/ml/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3726 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/argparse.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3297 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/atomic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/augmentation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4361 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/caching.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5070 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/checkpoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1303 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/colors.py
+-rw-r--r--   0 runner    (1001) docker     (123)      698 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4941 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/datetime.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.781941 ml-starter-0.0.37/ml/utils/device/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/auto.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8885 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      548 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1753 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/gpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)      829 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/device/metal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4114 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/distributed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5222 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/large_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4831 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2588 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/meter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/networking.py
+-rw-r--r--   0 runner    (1001) docker     (123)      438 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/numpy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9981 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/parallel.py
+-rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/random.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/staging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4993 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7915 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/torch_distributed.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13637 2023-05-13 02:47:49.000000 ml-starter-0.0.37/ml/utils/video.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:48:01.785941 ml-starter-0.0.37/ml_starter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      251 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        3 2023-05-13 02:48:01.000000 ml-starter-0.0.37/ml_starter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-05-13 02:47:49.000000 ml-starter-0.0.37/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements-docs.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 02:47:49.000000 ml-starter-0.0.37/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 02:48:01.785941 ml-starter-0.0.37/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-05-13 02:47:49.000000 ml-starter-0.0.37/setup.py
```

### Comparing `ml-starter-0.0.36/LICENSE` & `ml-starter-0.0.37/LICENSE`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.36/PKG-INFO` & `ml-starter-0.0.37/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ml-starter
-Version: 0.0.36
+Version: 0.0.37
 Summary: ML project template repository
 Home-page: https://github.com/codekansas/ml-starter
 Author: Benjamin Bolte
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ml-starter-0.0.36/README.md` & `ml-starter-0.0.37/README.md`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.36/ml/api.py` & `ml-starter-0.0.37/ml/api.py`

 * *Files 6% similar despite different names*

```diff
@@ -43,31 +43,35 @@
     "ChunkSampler",
     "Clamp",
     "ClippifyDataset",
     "collate_non_null",
     "collate",
     "CollateMode",
     "colorize",
+    "ColumnParallelLinear",
     "conf_field",
     "configure_logging",
-    "DDPLauncher",
-    "DDPLauncherConfig",
     "DictIndex",
     "Environment",
     "format_timedelta",
     "from_args",
     "get_activation",
     "get_args",
     "get_cache_dir",
     "get_data_dir",
     "get_dataset_split_for_phase",
     "get_dataset_splits",
+    "get_distributed_backend",
     "get_eval_run_dir",
     "get_exp_name",
     "get_image_mask",
+    "get_local_rank_optional",
+    "get_local_rank",
+    "get_local_world_size_optional",
+    "get_local_world_size",
     "get_master_addr",
     "get_master_port",
     "get_model_dir",
     "get_norm_1d",
     "get_norm_2d",
     "get_norm_3d",
     "get_norm_linear",
@@ -77,53 +81,72 @@
     "get_rank",
     "get_run_dir",
     "get_type_from_string",
     "get_worker_info",
     "get_world_size_optional",
     "get_world_size",
     "init_",
+    "init_and_run",
+    "init_dist",
     "init_empty_weights",
+    "init_parallelism",
     "InitializationType",
     "instantiate_config",
     "is_debugging",
     "is_distributed",
     "is_master",
+    "launch_subprocesses",
     "LearnedPositionalEmbeddings",
     "load_model_and_task",
     "lora",
     "LoraConv1d",
     "LoraConv2d",
     "LoraEmbedding",
     "LoraLinear",
     "Loss",
     "meta_to_empty_func",
     "MultiIterDataset",
+    "MultiprocessConfig",
+    "MultiProcessLauncher",
+    "MultiProcessLauncherConfig",
     "NormType",
     "open_atomic",
     "Output",
     "pad_all",
     "pad_sequence",
+    "parallel_group_info",
+    "ParallelEmbedding",
+    "parallelism_is_initialized",
     "Phase",
     "pretrained_clip",
+    "pretrained_hubert",
+    "pretrained_llama",
     "pretrained_sam",
+    "PretrainedClipSize",
+    "PretrainedHubertSize",
+    "PretrainedLlamaKey",
+    "PretrainedSamSize",
     "project_dir_paths",
     "read_gif",
     "read_video",
     "reduce",
     "register_logger",
     "register_lr_scheduler",
     "register_model",
     "register_optimizer",
     "register_task",
     "register_trainer",
     "ReinforcementLearningTask",
     "ReinforcementLearningTaskConfig",
     "ReinforcementLearningTrainer",
     "ReinforcementLearningTrainerConfig",
+    "reset_parallelism",
     "RotaryEmbeddings",
+    "RowParallelLinear",
+    "set_distributed_backend",
     "set_random_seed",
     "set_slurm_master_addr",
     "set_slurm_rank_and_world_size",
     "SinusoidalEmbeddings",
     "SlurmLauncher",
     "SlurmLauncherConfig",
     "stage_environment",
@@ -166,31 +189,34 @@
     register_lr_scheduler,
     register_model,
     register_optimizer,
     register_task,
     register_trainer,
 )
 from ml.core.state import Phase, State
-from ml.launchers.ddp import DDPLauncher, DDPLauncherConfig
+from ml.launchers.mp import MultiProcessLauncher, MultiProcessLauncherConfig
 from ml.launchers.slurm import SlurmLauncher, SlurmLauncherConfig, set_slurm_master_addr, set_slurm_rank_and_world_size
 from ml.lr_schedulers.base import BaseLRScheduler, BaseLRSchedulerConfig
 from ml.models.activations import ActivationType, Clamp, cast_activation_type, get_activation
 from ml.models.base import BaseModel, BaseModelConfig
 from ml.models.embeddings import (
     LearnedPositionalEmbeddings,
     RotaryEmbeddings,
     SinusoidalEmbeddings,
     cast_embedding_kind,
     get_positional_embeddings,
 )
 from ml.models.init import InitializationType, cast_init_type, init_
 from ml.models.lora import LoraConv1d, LoraConv2d, LoraEmbedding, LoraLinear, lora
 from ml.models.norms import NormType, cast_norm_type, get_norm_1d, get_norm_2d, get_norm_3d, get_norm_linear
-from ml.models.pretrained.clip import pretrained_clip
-from ml.models.pretrained.sam import pretrained_sam
+from ml.models.parallel import ColumnParallelLinear, ParallelEmbedding, RowParallelLinear
+from ml.models.pretrained.clip import PretrainedClipSize, pretrained_clip
+from ml.models.pretrained.hubert import PretrainedHubertSize, pretrained_hubert
+from ml.models.pretrained.llama import PretrainedLlamaKey, pretrained_llama
+from ml.models.pretrained.sam import PretrainedSamSize, pretrained_sam
 from ml.optimizers.base import BaseOptimizer, BaseOptimizerConfig
 from ml.tasks.base import BaseTask, BaseTaskConfig
 from ml.tasks.datasets import transforms
 from ml.tasks.datasets.async_iterable import AsyncIterableDataset
 from ml.tasks.datasets.clippify import ClippifyDataset
 from ml.tasks.datasets.collate import CollateMode, collate, collate_non_null, pad_all, pad_sequence
 from ml.tasks.datasets.multi_iter import MultiIterDataset
@@ -221,26 +247,39 @@
 from ml.utils.checks import assert_no_nans
 from ml.utils.colors import colorize
 from ml.utils.data import check_md5, check_sha256, get_dataset_split_for_phase, get_dataset_splits, get_worker_info
 from ml.utils.datetime import format_timedelta
 from ml.utils.device.auto import AutoDevice
 from ml.utils.device.base import BaseDevice
 from ml.utils.distributed import (
+    get_local_rank,
+    get_local_rank_optional,
+    get_local_world_size,
+    get_local_world_size_optional,
     get_master_addr,
     get_master_port,
     get_random_port,
     get_rank,
     get_rank_optional,
     get_world_size,
     get_world_size_optional,
     is_distributed,
     is_master,
 )
 from ml.utils.image import read_gif, write_gif
-from ml.utils.io import instantiate_config, load_model_and_task
+from ml.utils.checkpoint import instantiate_config, load_model_and_task
 from ml.utils.large_models import init_empty_weights, meta_to_empty_func
 from ml.utils.logging import configure_logging
 from ml.utils.numpy import as_cpu_tensor, as_numpy_array
+from ml.utils.parallel import init_parallelism, parallel_group_info, parallelism_is_initialized, reset_parallelism
 from ml.utils.random import set_random_seed
 from ml.utils.staging import stage_environment
 from ml.utils.timer import Timer, timeout
+from ml.utils.torch_distributed import (
+    MultiprocessConfig,
+    get_distributed_backend,
+    init_and_run,
+    init_dist,
+    launch_subprocesses,
+    set_distributed_backend,
+)
 from ml.utils.video import read_video, write_video
```

### Comparing `ml-starter-0.0.36/ml/core/common_types.py` & `ml-starter-0.0.37/ml/core/common_types.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.36/ml/core/config.py` & `ml-starter-0.0.37/ml/core/config.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines the base config and object classes.
+
+The base configuration dataclass provides some small increments over what
+OmegaConf expects. The :func:``conf_field`` function exists to standardize
+the metadata that each field should have.
+"""
+
 from dataclasses import dataclass, field
 from typing import Any, Generic, TypeVar
 
 from omegaconf import MISSING, DictConfig
 
 FieldType = Any
 
@@ -20,15 +27,14 @@
             line argument in some CLIs
         short: An optional metadata field, which may be parsed to a command
             line argument in some CLIs
 
     Returns:
         The correctly constructed dataclass field
     """
-
     metadata: dict[str, Any] = {}
     if help is not None:
         metadata["help"] = help
     if short is not None:
         metadata["short"] = short
 
     if hasattr(value, "__call__"):
@@ -50,15 +56,14 @@
     @classmethod
     def get_defaults(cls: type[BaseConfigT]) -> dict[str, BaseConfigT]:
         """Returns default configurations.
 
         Returns:
             A dictionary of default configurations for the current config
         """
-
         return {}
 
     @classmethod
     def resolve(cls: type[BaseConfigT], config: BaseConfigT) -> None:
         """Runs post-construction config resolution.
 
         Args:
```

### Comparing `ml-starter-0.0.36/ml/core/env.py` & `ml-starter-0.0.37/ml/core/env.py`

 * *Files 2% similar despite different names*

```diff
@@ -145,14 +145,18 @@
 DisableMetal = _BoolEnvVar("DISABLE_METAL", default=False)
 is_metal_disabled = DisableMetal.get
 
 # Disables using the GPU.
 DisableGPU = _BoolEnvVar("DISABLE_GPU", default=False)
 is_gpu_disabled = DisableGPU.get
 
+# Disables colors in various parts.
+DisableColors = _BoolEnvVar("DISABLE_COLORS", default=False)
+are_colors_disabled = DisableColors.get
+
 # Disables Tensorboard subprocess.
 DisableTensorboard = _BoolEnvVar("DISABLE_TENSORBOARD", default=False)
 is_tensorboard_disabled = DisableTensorboard.get
 
 # Show full error message when trying to import a file.
 ShowFullImportError = _BoolEnvVar("SHOW_FULL_IMPORT_ERROR", default=False)
 should_show_full_import_error = ShowFullImportError.get
```

### Comparing `ml-starter-0.0.36/ml/core/registry.py` & `ml-starter-0.0.37/ml/core/registry.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,16 @@
+"""Defines the registry for all objects in the project.
+
+The registry is used to register all objects in the project, and to
+construct them from their configurations. This is done by using the
+`register` decorator, which registers the decorated class with an
+associated config dataclass in the registry. The registry can then be used to
+construct the object from its configuration.
+"""
+
 import functools
 import inspect
 import json
 import logging
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
 from pathlib import Path
@@ -98,15 +107,15 @@
         name = subconfig[NAME_KEY]
         if not isinstance(name, str):
             raise ValueError(f"Expected {key} name to be a string, got {name}")
         names.append(name)
     return names
 
 
-class register_base(ABC, Generic[Entry, Config]):  # pylint: disable=invalid-name
+class register_base(ABC, Generic[Entry, Config]):  # noqa: N801
     """Defines the base registry type."""
 
     REGISTRY: dict[str, tuple[type[Entry], type[Config]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     @abstractmethod
@@ -170,15 +179,14 @@
     @classmethod
     def populate_registry(cls, name: str) -> None:
         """Populates the registry until it has the requested name available.
 
         Args:
             name: The name of the registry item to get
         """
-
         lower_name = name.lower()
 
         # Check in the existing registry locations.
         if name in cls.REGISTRY_LOCATIONS:
             cls.manual_import(cls.REGISTRY_LOCATIONS[name])
         if name in cls.REGISTRY:
             return
@@ -339,15 +347,15 @@
         for key, default_cfg in self.config.get_defaults().items():
             self.REGISTRY[key] = cast(tuple[type[Entry], type[Config]], (entry, default_cfg))
             self.REGISTRY_LOCATIONS[key] = registry_location
 
         return entry
 
 
-class multi_register_base(register_base[Entry, Config], Generic[Entry, Config]):  # pylint: disable=invalid-name
+class multi_register_base(register_base[Entry, Config], Generic[Entry, Config]):  # noqa: N801
     """Defines a registry which produces multiple objects."""
 
     @classmethod
     def build_entry(cls, raw_config: DictConfig) -> Entry | None:
         raise NotImplementedError("`build_entry` not implemented; use `build_entries` instead")
 
     @classmethod
@@ -427,105 +435,105 @@
             for i, (reg_name, reg_cfg) in enumerate(zip(reg_names, reg_cfgs)):
                 _, reg_cfg_cls = cls.lookup(reg_name)
                 reg_cfg_cls.resolve(reg_cfg)
                 reg_cfgs[i] = reg_cfg
             raw_config[cls.config_key()] = reg_cfgs
 
 
-class register_model(register_base["BaseModel", "BaseModelConfig"]):  # pylint: disable=invalid-name
+class register_model(register_base["BaseModel", "BaseModelConfig"]):  # noqa: N801
     """Defines a registry for holding modules."""
 
     REGISTRY: dict[str, tuple[type["BaseModel"], type["BaseModelConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("models")
 
     @classmethod
     def config_key(cls) -> str:
         return "model"
 
 
-class register_task(register_base["BaseTask", "BaseTaskConfig"]):  # pylint: disable=invalid-name
+class register_task(register_base["BaseTask", "BaseTaskConfig"]):  # noqa: N801
     """Defines a registry for holding tasks."""
 
     REGISTRY: dict[str, tuple[type["BaseTask"], type["BaseTaskConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("tasks")
 
     @classmethod
     def config_key(cls) -> str:
         return "task"
 
 
-class register_trainer(register_base["BaseTrainer", "BaseTrainerConfig"]):  # pylint: disable=invalid-name
+class register_trainer(register_base["BaseTrainer", "BaseTrainerConfig"]):  # noqa: N801
     """Defines a registry for holding trainers."""
 
     REGISTRY: dict[str, tuple[type["BaseTrainer"], type["BaseTrainerConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("trainers")
 
     @classmethod
     def config_key(cls) -> str:
         return "trainer"
 
 
-class register_optimizer(register_base["BaseOptimizer", "BaseOptimizerConfig"]):  # pylint: disable=invalid-name
+class register_optimizer(register_base["BaseOptimizer", "BaseOptimizerConfig"]):  # noqa: N801
     """Defines a registry for holding optimizers."""
 
     REGISTRY: dict[str, tuple[type["BaseOptimizer"], type["BaseOptimizerConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("optimizers")
 
     @classmethod
     def config_key(cls) -> str:
         return "optimizer"
 
 
-class register_lr_scheduler(register_base["BaseLRScheduler", "BaseLRSchedulerConfig"]):  # pylint: disable=invalid-name
+class register_lr_scheduler(register_base["BaseLRScheduler", "BaseLRSchedulerConfig"]):  # noqa: N801
     """Defines a registry for holding learning rate schedulers."""
 
     REGISTRY: dict[str, tuple[type["BaseLRScheduler"], type["BaseLRSchedulerConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("lr_schedulers")
 
     @classmethod
     def config_key(cls) -> str:
         return "lr_scheduler"
 
 
-class register_logger(multi_register_base["BaseLogger", "BaseLoggerConfig"]):  # pylint: disable=invalid-name
+class register_logger(multi_register_base["BaseLogger", "BaseLoggerConfig"]):  # noqa: N801
     """Defines a registry for holding loggers."""
 
     REGISTRY: dict[str, tuple[type["BaseLogger"], type["BaseLoggerConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("loggers")
 
     @classmethod
     def config_key(cls) -> str:
         return "logger"
 
 
-class register_launcher(register_base["BaseLauncher", "BaseLauncherConfig"]):  # pylint: disable=invalid-name
+class register_launcher(register_base["BaseLauncher", "BaseLauncherConfig"]):  # noqa: N801
     REGISTRY: dict[str, tuple[type["BaseLauncher"], type["BaseLauncherConfig"]]] = {}
     REGISTRY_LOCATIONS: dict[str, Path] = {}
 
     @classmethod
     def search_directory(cls) -> Path:
         return Path("launchers")
 
@@ -590,15 +598,14 @@
     @classmethod
     def update_config(cls, config: DictConfig) -> None:
         """Updates the config in-place.
 
         Args:
             config: The config to update
         """
-
         # Pre-builds the config using the structured configs.
         register_model.update_config(config)
         register_task.update_config(config)
         register_trainer.update_config(config)
         register_optimizer.update_config(config)
         register_lr_scheduler.update_config(config)
         register_logger.update_configs(config)
@@ -607,15 +614,14 @@
     @classmethod
     def resolve_config(cls, config: DictConfig) -> None:
         """Resolves the config in-place.
 
         Args:
             config: The config to resolve
         """
-
         # Resolves the final config once all structured configs have been merged.
         OmegaConf.resolve(config)
 
         # Runs object-specific resolutions.
         register_model.resolve_config(config)
         register_task.resolve_config(config)
         register_trainer.resolve_config(config)
@@ -630,15 +636,14 @@
 
         Args:
             config: The raw DictConfig to parse
 
         Returns:
             The parsed Objects dataclass
         """
-
         model = register_model.build_entry(config)
         task = register_task.build_entry(config)
         trainer = register_trainer.build_entry(config)
         optimizer = register_optimizer.build_entry(config)
         lr_scheduler = register_lr_scheduler.build_entry(config)
         loggers = register_logger.build_entries(config)
         launcher = register_launcher.build_entry(config)
```

### Comparing `ml-starter-0.0.36/ml/core/state.py` & `ml-starter-0.0.37/ml/core/state.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a dataclass for keeping track of the current training state."""
+
 from dataclasses import dataclass
 from typing import Literal, TypeVar, cast, get_args
 
 from omegaconf import MISSING
 from torch import nn
 
 from ml.core.config import conf_field
@@ -26,16 +28,14 @@
     args = get_args(Phase)
     assert raw_phase in args, f"Invalid phase: '{raw_phase}' Valid options are {args}"
     return cast(Phase, raw_phase)
 
 
 @dataclass
 class State:
-    """Defines the state variables to track training."""
-
     num_epochs: int = conf_field(MISSING, help="Number of epochs so far")
     num_steps: int = conf_field(MISSING, help="Number of steps so far")
     num_epoch_steps: int = conf_field(MISSING, help="Number of steps in the current epoch")
     num_samples: int = conf_field(MISSING, help="Number of sample so far")
     num_epoch_samples: int = conf_field(MISSING, help="Number of samples in the current epoch")
     num_valid_steps: int = conf_field(MISSING, help="Number of validation steps so far")
     num_test_steps: int = conf_field(MISSING, help="Number of test steps so far")
```

### Comparing `ml-starter-0.0.36/ml/launchers/base.py` & `ml-starter-0.0.37/ml/launchers/base.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Base launcher class and config."""
+
 from dataclasses import dataclass
 from typing import Generic, TypeVar
 
 from ml.core.config import BaseConfig, BaseObject
 
 T = TypeVar("T", bound="BaseLauncher")
 
@@ -12,14 +14,9 @@
 
 
 LauncherConfigT = TypeVar("LauncherConfigT", bound=BaseLauncherConfig)
 
 
 class BaseLauncher(BaseObject[LauncherConfigT], Generic[LauncherConfigT]):
     def launch(self) -> None:
-        """Launches the training process.
-
-        Raises:
-            NotImplementedError: If the subclass does not implement this method
-        """
-
+        """Launches the training process."""
         raise NotImplementedError
```

### Comparing `ml-starter-0.0.36/ml/launchers/ddp.py` & `ml-starter-0.0.37/ml/launchers/torchrun.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,136 +1,121 @@
-"""Defines a Distributed Data Parallel launcher.
+"""Defines a launcher which uses `torchrun` to launch a job.
 
-This is a light-weight wrapper around PyTorch's built-in Distributed Data
-Parallel class.
-
-For multiple devices, data is split along the batch dimension, passed to each
-device, which computes losses independently. The loss tensors are gathered to
-the master device to compute a single loss. In other words, each device
-belongs to exactly one process.
+This is a light-weight werapper around PyTorch's `torch.distributed.launch`
+script. It is used to launch a job on a single node with multiple processes,
+each with multiple devices.
 """
 
-import functools
 import logging
-import os
-import sys
-import traceback
+import shutil
+import subprocess
 from dataclasses import dataclass
-from typing import Callable
 
 import torch
-import torch.multiprocessing as mp
-from omegaconf import MISSING, DictConfig, OmegaConf
+from omegaconf import MISSING, OmegaConf
 
 from ml.core.config import conf_field
-from ml.core.registry import Objects, register_launcher
+from ml.core.registry import project_dirs, register_launcher, register_trainer
 from ml.launchers.base import BaseLauncher, BaseLauncherConfig
-from ml.scripts.train import train_main_with_objects
-from ml.utils.distributed import (
-    set_init_method,
-    set_master_addr,
-    set_master_port,
-    set_rank,
-    set_world_size,
-)
-from ml.utils.logging import configure_logging
 from ml.utils.networking import get_unused_port
-from ml.utils.torch_distributed import get_distributed_backend, init_process_group
 
 logger: logging.Logger = logging.getLogger(__name__)
 
+TORCHRUN_TEMPLATE: str = """
+#!/usr/bin/env python
 
-@dataclass
-class MultiprocessConfig:
-    rank: int = conf_field(-1, help="The rank of the process")
-    world_size: int = conf_field(MISSING, help="The total number of processes")
-    devices_per_rank: int = conf_field(1, help="The number of devices per rank")
-    master_addr: str = conf_field("localhost", help="The address of the master process")
-    master_port: int = conf_field(MISSING, help="The port of the master process")
-
-
-def process_main(cfg: MultiprocessConfig, raw_config: DictConfig) -> None:
-    set_master_addr(cfg.master_addr)
-    set_master_port(cfg.master_port)
-    set_rank(cfg.rank)
-    set_world_size(cfg.world_size)
-    set_init_method("env://")
-    configure_logging(rank=cfg.rank, world_size=cfg.world_size)
-    logger.info("Initializing process group")
-    init_process_group(backend=get_distributed_backend())
-
-    objs = Objects.parse_raw_config(raw_config)
-    train_main_with_objects(objs)
-
-
-def func_wrapped(
-    func: Callable[[MultiprocessConfig], None],
-    cfg: MultiprocessConfig,
-    error_queue: "mp.Queue[str]",
-) -> None:
-    try:
-        func(cfg)
-    except KeyboardInterrupt:
-        pass
-    except Exception:
-        error_queue.put(traceback.format_exc())
-        sys.exit(1)
+from pathlib import Path
+
+from omegaconf import OmegaConf
+
+from ml.core.registry import project_dirs as registry_project_dirs
+from ml.scripts.train import train_main
+
+PROJECT_DIRS = {project_root}
+CONFIG_PATH = '{config_path}'
+
+
+def main() -> None:
+    for p in PROJECT_DIRS:
+        registry_project_dirs.add(Path(p))
+    config = OmegaConf.load(CONFIG_PATH)
+    train_main(config)
+
+
+if __name__ == "__main__":
+    main()
+"""
 
 
 @dataclass
-class DDPLauncherConfig(BaseLauncherConfig):
-    multiprocess: MultiprocessConfig = conf_field(MultiprocessConfig())
+class TorchRunLauncherConfig(BaseLauncherConfig):
+    nproc_per_node: int = conf_field(MISSING, help="The number of processes per node")
+    master_addr: str = conf_field("127.0.0.1", help="The address of the master")
+    master_port: int = conf_field(MISSING, help="The port of the master")
+    backend: str = conf_field("nccl", help="The backend to use for distributed training")
+    start_method: str = conf_field("spawn", help="The method to use to start processes")
+    torchrun_path: str = conf_field(MISSING, help="The path to the TorchRun script")
 
     @classmethod
-    def resolve(cls: type["DDPLauncherConfig"], config: "DDPLauncherConfig") -> None:
+    def resolve(cls: type["TorchRunLauncherConfig"], config: "TorchRunLauncherConfig") -> None:
         super().resolve(config)
 
-        device_count = torch.cuda.device_count()
-        if config.multiprocess.devices_per_rank > device_count:
-            raise ValueError(
-                f"Requested {config.multiprocess.devices_per_rank} devices per rank, "
-                f"but only {device_count} are available"
-            )
-        if OmegaConf.is_missing(config.multiprocess, "world_size"):
-            config.multiprocess.world_size = device_count // config.multiprocess.devices_per_rank
-        if OmegaConf.is_missing(config.multiprocess, "master_port"):
-            config.multiprocess.master_port = get_unused_port()
+        if OmegaConf.is_missing(config, "nproc_per_node"):
+            config.nproc_per_node = torch.cuda.device_count()
+        if OmegaConf.is_missing(config, "master_port"):
+            config.master_port = get_unused_port()
+        if OmegaConf.is_missing(config, "torchrun_path"):
+            torchrun_path = shutil.which("torchrun")
+            if torchrun_path is None:
+                raise ValueError("Could not find torchrun in PATH")
+            config.torchrun_path = torchrun_path
 
 
-@register_launcher("ddp", DDPLauncherConfig)
-class DDPLauncher(BaseLauncher[DDPLauncherConfig]):
+@register_launcher("torchrun", TorchRunLauncherConfig)
+class TorchRunLauncher(BaseLauncher[TorchRunLauncherConfig]):
     def launch(self) -> None:
-        if not torch.cuda.is_available():
-            raise RuntimeError("DDPLauncher requires CUDA")
-
-        func = functools.partial(process_main, raw_config=self.raw_config)
-
-        # Config should have valid values at this point, post-resolution.
-        cfg = self.config.multiprocess
-
-        if cfg.world_size <= 1:
-            logger.warning("Multi-process DDPTrainer expects more than one device")
-            cfg.rank = 0
-            func(cfg)
-            return
-
-        def set_env(rank: int) -> None:
-            os.environ["CUDA_VISIBLE_DEVICES"] = str(rank)
-
-        # This is essentially the same as `mp.spawn` but with specific control
-        # over CUDA_VISIBLE_DEVICES.
-        logger.info("Launching %d training workers", cfg.world_size)
-        ctx = mp.get_context("spawn")
-        error_queues = []
-        procs = []
-        for rank in range(cfg.world_size):
-            error_queue = ctx.SimpleQueue()
-            cfg.rank = rank
-            set_env(rank)
-            proc = ctx.Process(target=func_wrapped, args=(func, cfg, error_queue), daemon=False)
-            logger.debug("Started process %d", rank)
-            proc.start()
-            error_queues.append(error_queue)
-            procs.append(proc)
-        pctx = mp.ProcessContext(procs, error_queues)
-        while not pctx.join():
-            pass
+        """Launches the job by calling the TorchRun CLI in a subprocess."""
+        trainer = register_trainer.build_entry_non_null(self.raw_config)
+        trainer.save_config()
+
+        # Builds the run file.
+        torchrun_file = TORCHRUN_TEMPLATE.format(
+            project_root=[str(p) for p in project_dirs.paths],
+            config_path=trainer.config_path,
+        ).strip()
+
+        torchrun_fpath = trainer.exp_dir / "torchrun.py"
+        with open(torchrun_fpath, "w", encoding="utf-8") as f:
+            f.write(torchrun_file)
+        logger.info("Wrote torchrun file to %s", torchrun_fpath)
+
+        # Makes a specific log directory for TorchRun logs.
+        (log_dir := trainer.log_dir / "torchrun").mkdir(parents=True, exist_ok=True)
+
+        # This launcher expects to run on only one node. A multi-node TorchRun
+        # launcher would require a way to launch TorchRun processes across
+        # multiple target nodes.
+        node_rank, num_nodes = 0, 1
+
+        cmd = [
+            self.config.torchrun_path,
+            "--nproc-per-node",
+            str(self.config.nproc_per_node),
+            "--node-rank",
+            str(node_rank),
+            "--nnodes",
+            str(num_nodes),
+            "--master-addr",
+            self.config.master_addr,
+            "--master-port",
+            str(self.config.master_port),
+            "--start-method",
+            self.config.start_method,
+            "--log-dir",
+            str(log_dir),
+            "--run-path",
+            str(torchrun_fpath),
+        ]
+
+        # Launch the job
+        logger.info("Launching job with command: %s", " ".join(cmd))
+        subprocess.run(cmd, check=True)
```

### Comparing `ml-starter-0.0.36/ml/launchers/slurm.py` & `ml-starter-0.0.37/ml/launchers/slurm.py`

 * *Files 2% similar despite different names*

```diff
@@ -41,15 +41,15 @@
     set_init_method,
     set_master_addr,
     set_rank,
     set_world_size,
 )
 from ml.utils.logging import configure_logging
 from ml.utils.staging import stage_environment
-from ml.utils.torch_distributed import get_distributed_backend, init_process_group
+from ml.utils.torch_distributed import init_process_group_from_backend
 
 logger: logging.Logger = logging.getLogger(__name__)
 
 T = TypeVar("T", bound="SlurmLauncher")
 
 SBATCH_TEMPLATE: str = """
 #!/bin/bash
@@ -263,17 +263,17 @@
     # Sets environment variables from Clurm environment variables.
     set_slurm_master_addr()
     rank, world_size = set_slurm_rank_and_world_size()
 
     # Sets the initialization method and configures per-rank logging.
     set_init_method(f"tcp://{get_master_addr()}:{get_master_port()}")
     configure_logging(rank=rank, world_size=world_size)
-    init_process_group(backend=get_distributed_backend())
+    init_process_group_from_backend()
 
-    objs = Objects.parse_raw_config(raw_config)  # type: ignore
+    objs = Objects.parse_raw_config(raw_config)  # type: ignore[arg-type]
 
     assert (trainer := objs.trainer) is not None
     trainer.add_lock_file("running", exists_ok=True)
     trainer.remove_lock_file("scheduled", missing_ok=True)
 
     signal.signal(signal.SIGTERM, ignore_signal)
     trainer.add_signal_handler(signal.SIGUSR1, requeue_job)
```

### Comparing `ml-starter-0.0.36/ml/loggers/base.py` & `ml-starter-0.0.37/ml/loggers/base.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines the base logger.
+
+New loggers should implement whichever `log_` functions they need to.
+Unimplemented functions are simply ignored. The framework will handle logging
+rate limiting and munging the logged values to a common format.
+"""
+
 import datetime
 import functools
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
 from pathlib import Path
 from typing import Callable, Generic, TypeVar, Union
 
@@ -126,15 +133,14 @@
 
         Args:
             state: The state to check
 
         Returns:
             If the logger should write values for the current state
         """
-
         current_time = datetime.datetime.now()
         min_write_time_diff = datetime.timedelta(seconds=self.write_every_n_seconds(state.phase))
 
         if state.phase not in self.last_write_time:
             self.last_write_time[state.phase] = current_time
             return True
         elif current_time - self.last_write_time[state.phase] < min_write_time_diff:
@@ -176,19 +182,17 @@
 
         Args:
             phase: The phase to get the write interval for
 
         Returns:
             The write interval, in seconds
         """
-
         if phase == "train":
             if self.config.write_train_every_n_seconds is not None:
                 return self.config.write_train_every_n_seconds
-        else:
-            if self.config.write_val_every_n_seconds is not None:
-                return self.config.write_val_every_n_seconds
+        elif self.config.write_val_every_n_seconds is not None:
+            return self.config.write_val_every_n_seconds
 
         if self.config.write_every_n_seconds is not None:
             return self.config.write_every_n_seconds
 
         return self.default_write_every_n_seconds(phase)
```

### Comparing `ml-starter-0.0.36/ml/loggers/meter.py` & `ml-starter-0.0.37/ml/loggers/meter.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""Defines a metered logger.
+
+This logger keeps track of statistics of logged values. It is useful for
+getting global statistics during evaluation.
+"""
+
 from dataclasses import dataclass
 from typing import Any, Callable, Iterable
 
 from torch import Tensor
 
 from ml.core.registry import register_logger
 from ml.core.state import Phase, State
```

### Comparing `ml-starter-0.0.36/ml/loggers/multi.py` & `ml-starter-0.0.37/ml/loggers/multi.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines a general logger for munging logged values to an expected format.
+
+This logger handles munging, rate limiting, and multiplexing logged values
+to each of the implemented child loggers. It is the logging interface that
+is exposed to the task and model.
+"""
+
 import functools
 import logging
 import math
 import re
 from collections import defaultdict
 from typing import Any, Callable, Iterator, Literal, Sequence, TypeVar
 
@@ -47,15 +54,14 @@
         text: The text to standardize
         max_line_length: If set, truncate lines to this length
         remove_non_ascii: Remove non-ASCII characters if present
 
     Returns:
         The standardized text lines
     """
-
     if remove_non_ascii:
         text = "".join(char for char in text if ord(char) < 128)
     lines = [re.sub(r"\s+", " ", line) for line in re.split(r"[\n\r]+", text.strip())]
     if max_line_length is not None:
         lines = [subline for line in lines for subline in _chunk_lines(line, max_line_length)]
     return lines
 
@@ -69,15 +75,14 @@
 
     Returns:
         The selected audio channel
 
     Raises:
         ValueError: If the audio shape is invalid
     """
-
     if audio.shape[-2] not in VALID_AUDIO_CHANNEL_COUNTS:
         raise ValueError(f"Invalid audio channel count: {audio.shape[0]}")
     if channel_select_mode == "first":
         return audio[..., 0, :]
     if channel_select_mode == "last":
         return audio[..., -1, :]
     if channel_select_mode == "mean":
@@ -97,15 +102,14 @@
         interpolation: Interpolation mode to use for image resizing
         trg_res: The target image resolution; the image will be reshaped to
             have approximately the same area as an image with this resolution
 
     Returns:
         The resized image
     """
-
     width, height = V.get_image_size(image)
     trg_height, trg_width = trg_res
     factor = math.sqrt((trg_height * trg_width) / (height * width))
     new_height, new_width = int(height * factor), int(width * factor)
     return V.resize(image, [new_height, new_width], interpolation)
 
 
@@ -127,15 +131,14 @@
 
     Returns:
         The normalized image, with shape (C, H, W)
 
     Raises:
         ValueError: If the image shape is invalid
     """
-
     if normalize and image.is_floating_point():
         minv, maxv = _aminmax(image)
         maxv.clamp_min_(1.0)
         minv.clamp_max_(0.0)
         image = torch.clamp((image.detach() - minv) / (maxv - minv), 0.0, 1.0)
 
     if image.ndim == 2:
@@ -175,15 +178,14 @@
 
     Returns:
         The normalized image, with shape (B, C, H, W)
 
     Raises:
         ValueError: If the image shape is invalid
     """
-
     if normalize and images.is_floating_point():
         minv, maxv = _aminmax(images)
         maxv.clamp_min_(1.0)
         minv.clamp_max_(0.0)
         images = torch.clamp((images.detach() - minv) / (maxv - minv), 0.0, 1.0)
 
     if images.ndim == 3:
@@ -219,15 +221,14 @@
 
     Returns:
         The standardized audio tensor, with shape (C, T)
 
     Raises:
         ValueError: If the audio shape is invalid
     """
-
     if audio.ndim == 1:
         audio = audio.unsqueeze(0)
     elif audio.ndim == 2:
         if audio.shape[0] in VALID_AUDIO_CHANNEL_COUNTS:
             pass
         elif audio.shape[1] in VALID_AUDIO_CHANNEL_COUNTS:
             audio = audio.permute(1, 0)
@@ -253,15 +254,14 @@
 
     Returns:
         The standardized audio tensor, with shape (B, C, T)
 
     Raises:
         ValueError: If the audio shape is invalid
     """
-
     if audios.ndim == 2:
         audios = audios.unsqueeze(1)
     elif audios.ndim == 3:
         if audios.shape[1] in VALID_AUDIO_CHANNEL_COUNTS:
             pass
         elif audios.shape[2] in VALID_AUDIO_CHANNEL_COUNTS:
             audios = audios.permute(2, 1)
@@ -289,15 +289,14 @@
 
     Returns:
         The separated audio tensor
 
     Raises:
         ValueError: If the audio shape is invalid
     """
-
     if sep_frames == 0:
         return audio.transpose(0, 1).flatten(1)
 
     if audio.ndim != 3:
         raise ValueError(f"Invalid audio shape: {audio.shape}")
     bsz, chans, tsz = audio.shape
     audio_samples = audio.unbind(0)  # B * (C, T)
@@ -317,15 +316,14 @@
 
     Returns:
         The normalized video, with shape (T, C, H, W)
 
     Raises:
         ValueError: If the video shape is invalid
     """
-
     if normalize and video.is_floating_point():
         minv, maxv = _aminmax(video[-1])
         maxv.clamp_min_(1.0)
         minv.clamp_max_(0.0)
         video = torch.clamp((video.detach() - minv) / (maxv - minv), 0.0, 1.0)
 
     if video.ndim == 3:
@@ -355,15 +353,14 @@
 
     Returns:
         The normalized video, with shape (B, T, C, H, W)
 
     Raises:
         ValueError: If the video shape is invalid
     """
-
     if normalize and videos.is_floating_point():
         minv, maxv = _aminmax(videos[:, -1])
         maxv.clamp_min_(1.0)
         minv.clamp_max_(0.0)
         videos = torch.clamp((videos.detach() - minv) / (maxv - minv), 0.0, 1.0)
 
     if videos.ndim == 4:
@@ -393,15 +390,14 @@
             of the image
         line_spacing: The spacing between adjacent lines
         centered: If set, center the text labels, otherwise align to the left
 
     Returns:
         The image with a text label
     """
-
     if not text:
         return image
     if max_num_lines is None:
         max_num_lines = len(text)
     else:
         text = text[:max_num_lines]
     pil_image = V.to_pil_image(image)
@@ -438,15 +434,14 @@
         length: The desired video length, in seconds, at the target FPS
         target_fps: The target frames per second for the logger
         stack_dim: Which dimension to stack along, for lists
 
     Returns:
         The normalized video
     """
-
     if fps is None and length is None:
         return torch.stack(video, dim=stack_dim) if isinstance(video, list) else video
 
     pre_frames = len(video) if isinstance(video, list) else video.size(0)
     if fps is None:
         assert length is not None  # Not used, just for type checker
         fps = int(pre_frames / length)
@@ -497,15 +492,14 @@
         sep: Some optional padding around the images
         squareness_weight: Weight for number of non-square pixels in penalty
         emptiness_weight: Weight for number of empty pixels in penalty
 
     Returns:
         The square image, with shape (C, H', W') or (T, C, H', W')
     """
-
     assert images_or_videos.dim() in (4, 5)
 
     def ternary_search_optimal_side_counts(height: int, width: int, count: int) -> tuple[int, int]:
         lo, hi = 1, count
 
         def squareness_penalty(val: int) -> float:
             h, w = val * height, ((count + val - 1) // val) * width
@@ -575,15 +569,14 @@
         """Logs a scalar value.
 
         Args:
             key: The key being logged
             value: The scalar value being logged
             namespace: An optional logging namespace
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def scalar_future() -> Number:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, (int, float, Tensor))
             value_concrete = cast_fp32(value_concrete)
@@ -595,15 +588,14 @@
         """Logs a string value.
 
         Args:
             key: The key being logged
             value: The string value being logged
             namespace: An optional logging namespace
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def value_future() -> str:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, str)
             return value_concrete
@@ -625,15 +617,14 @@
             value: The image being logged; can be (C, H, W), (H, W, C) or (H, W)
                 as an RGB (3 channel) or grayscale (1 channel) image
             namespace: An optional logging namespace
             keep_resolution: If set, keep the image resolution the same,
                 otherwise upscale or downscale the image to a standard
                 resolution
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def image_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             value_concrete = cast_fp32(value_concrete)
@@ -662,15 +653,14 @@
             max_line_length: Labels longer than this length are wrapped around
             keep_resolution: If set, keep the image resolution the same,
                 otherwise upscale or downscale the image to a standard
                 resolution
             centered: If set, center the text labels, otherwise align to the
                 left
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def labeled_image_future() -> Tensor:
             image, text = value() if callable(value) else value
             assert isinstance(image, Tensor)
             assert isinstance(text, str)
@@ -703,15 +693,14 @@
             keep_resolution: If set, keep the image resolution the same,
                 otherwise upscale or downscale the image to a standard
                 resolution
             max_images: The maximum number of images to show; extra images
                 are clipped
             sep: An optional separation amount between adjacent images
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def images_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             value_concrete = standardize_images(
@@ -753,15 +742,14 @@
                 resolution
             max_images: The maximum number of images to show; extra images
                 are clipped
             sep: An optional separation amount between adjacent images
             centered: If set, center the text labels, otherwise align to the
                 left
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def labeled_images_future() -> Tensor:
             images, texts = value() if callable(value) else value
             assert isinstance(images, Tensor)
             assert images.shape[0] == len(texts)
@@ -811,15 +799,14 @@
             hop_length_ms: The FFT hop length, in milliseconds
             channel_select_mode: How to select the channel if the audio is
                 stereo; can be "first", "last", or "mean"; this is only used
                 for the spectrogram
             keep_resolution: If set, keep the resolution of the
                 spectrogram; otherwise, make human-viewable
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def raw_audio_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             return value_concrete
@@ -881,29 +868,31 @@
                 stereo; can be "first", "last", or "mean"; this is only used
                 for the spectrogram
             spec_sep: An optional separation amount between adjacent
                 spectrograms
             keep_resolution: If set, keep the resolution of the
                 spectrogram; otherwise, make human-viewable
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def raw_audio_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             return value_concrete
 
         @functools.lru_cache
         def audio_future() -> tuple[Tensor, int]:
             value_concrete = raw_audio_future()
             audio = standardize_audios(value_concrete, log_key=f"{namespace}/{key}", max_audios=max_audios)
             audio = cast_fp32(audio)
-            to_frames = lambda ms: 0 if ms == 0.0 else 2 ** round(math.log2(ms * sample_rate / 1000))
+
+            def to_frames(ms: float) -> int:
+                return 0 if ms == 0.0 else 2 ** round(math.log2(ms * sample_rate / 1000))
+
             audio = separate_with_padding(audio, to_frames(sep_ms))
             return audio, sample_rate
 
         self.audio[namespace][key] = audio_future
 
         if log_spec:
             # Using a unique key for the spectrogram is very important because
@@ -945,23 +934,25 @@
             hop_length_ms: The FFT hop length, in milliseconds
             channel_select_mode: How to select the channel if the audio is
                 stereo; can be "first", "last", or "mean"; this is only used
                 for the spectrogram
             keep_resolution: If set, keep the resolution of the
                 spectrogram; otherwise, make human-viewable
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def spec_future() -> Tensor:
             audio = value() if callable(value) else value
             audio = standardize_audio(audio, log_key=f"{namespace}/{key}")
             audio = get_audio_channel(audio, channel_select_mode)
-            to_frames = lambda ms: 2 ** round(math.log2(ms * sample_rate / 1000))
+
+            def to_frames(ms: float) -> int:
+                return 2 ** round(math.log2(ms * sample_rate / 1000))
+
             n_fft = to_frames(n_fft_ms)
             hop_length = None if hop_length_ms is None else to_frames(hop_length_ms)
             audio_spec = torch.stft(audio, n_fft, hop_length=hop_length, normalized=True, return_complex=True)
             audio_spec = torch.log10(torch.abs(audio_spec) + 1e-6)
             return standardize_image(
                 audio_spec,
                 log_key=f"{namespace}/{key}",
@@ -1000,23 +991,25 @@
                 stereo; can be "first", "last", or "mean"; this is only used
                 for the spectrogram
             spec_sep: An optional separation amount between adjacent
                 spectrograms
             keep_resolution: If set, keep the resolution of the
                 spectrogram; otherwise, make human-viewable
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def spec_future() -> Tensor:
             audio = value() if callable(value) else value
             audio = standardize_audios(audio, log_key=f"{namespace}/{key}", max_audios=max_audios)
             audio = get_audio_channel(audio, channel_select_mode)
-            to_frames = lambda ms: 2 ** round(math.log2(ms * sample_rate / 1000))
+
+            def to_frames(ms: float) -> int:
+                return 2 ** round(math.log2(ms * sample_rate / 1000))
+
             n_fft = to_frames(n_fft_ms)
             hop_length = None if hop_length_ms is None else to_frames(hop_length_ms)
             audio_spec = torch.stft(audio, n_fft, hop_length=hop_length, normalized=True, return_complex=True)
             audio_spec = torch.log10(torch.abs(audio_spec) + 1e-6)
             audio_spec = standardize_images(
                 audio_spec,
                 log_key=f"{namespace}/{key}",
@@ -1043,15 +1036,14 @@
             value: The video being logged; the video can be (T, C, H, W),
                 (T, H, W, C) or (T, H, W) as an RGB (3 channel) or grayscale
                 (1 channel) video
             namespace: An optional logging namespace
             fps: The video frames per second
             length: The desired video length, in seconds, at the target FPS
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def video_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             video = standardize_video(value_concrete, log_key=f"{namespace}/{key}")
@@ -1081,15 +1073,14 @@
             namespace: An optional logging namespace
             max_videos: The maximum number of videos to show; extra images
                 are clipped
             sep: An optional separation amount between adjacent videos
             fps: The video frames per second
             length: The desired video length, in seconds, at the target FPS
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def videos_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, (Tensor, list))
             video = normalize_video_fps(value_concrete, fps, length, stack_dim=1)
@@ -1103,15 +1094,14 @@
         """Logs a histogram.
 
         Args:
             key: The key being logged
             value: The values to create a histogram from, with arbitrary shape
             namespace: An optional logging namespace
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def histogram_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             value_concrete = cast_fp32(value_concrete)
@@ -1133,15 +1123,14 @@
             key: The key being logged
             value: The point cloud values, with shape (N, 3) or (B, ..., 3);
                 can pass multiple batches in order to show multiple point
                 clouds
             namespace: An optional logging namespace
             max_points: An optional maximum number of points in the point cloud
         """
-
         namespace = self.resolve_namespace(namespace)
 
         @functools.lru_cache
         def point_cloud_future() -> Tensor:
             value_concrete = value() if callable(value) else value
             assert isinstance(value_concrete, Tensor)
             value_concrete = cast_fp32(value_concrete)
```

### Comparing `ml-starter-0.0.36/ml/loggers/stdout.py` & `ml-starter-0.0.37/ml/loggers/stdout.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines a simple logger that writes to stdout.
+
+I put a bunch of colors in here to make it easier to quickly find logged
+values of interest, but the colors can be disabled by setting the
+environment variable ``DISABLE_COLORS=1``
+"""
+
 import datetime
 import itertools
 import logging
 from dataclasses import dataclass
 from pathlib import Path
 from typing import Any, Callable
 
@@ -86,15 +93,17 @@
                 if len(ks) == 2:
                     kk, rest = ks
                     if kk not in sub_sections:
                         sub_sections[kk] = {}
                     sub_sections[kk][rest] = section[k]
                     section.pop(k)
 
-            get_line = lambda kv: f'"{kv[0]}": {as_str(kv[1](), self.config.precision)}'
+            def get_line(kv: tuple[str, Any]) -> str:
+                return f'"{kv[0]}": {as_str(kv[1](), self.config.precision)}'
+
             inner_str = ", ".join(
                 itertools.chain(
                     map(get_line, sorted(section.items())),
                     (get_section_string(k, v, level + 1) for k, v in sorted(sub_sections.items())),
                 )
             )
             level_color = LEVEL_COLORS[min(level, len(LEVEL_COLORS) - 1)]
```

### Comparing `ml-starter-0.0.36/ml/loggers/tensorboard.py` & `ml-starter-0.0.37/ml/loggers/tensorboard.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+"""Defines a Tensorboard logging interface.
+
+This is a pretty vanilla Tensorboard setup. Each phase gets its own
+SummaryWriter, and scalars are logged to the writer for the current phase.
+Additionally, when developing locally, we also start a Tensorboard server
+in a subprocess. This can be disabled by setting ``DISABLE_TENSORBOARD=1``.
+Also, a specific Tensorboard port can be specified by setting
+``TENSORBOARD_PORT=<port>``.
+"""
+
 import atexit
 import datetime
 import functools
 import logging
 import os
 import re
 import subprocess
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/base.py` & `ml-starter-0.0.37/ml/lr_schedulers/base.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+"""Defines the base class and config for all learning rate schedulers.
+
+Learning rate schedulers can be plotted using the tool in
+:mod:`ml.tools.plot_lr_schedulers`. For example:
+
+.. code-block:: bash
+
+    python -m ml.lr_schedulers.scripts.plot linear /path/to/save.png
+"""
+
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
 from typing import Any, Generic, TypeVar
 
 from torch.optim.optimizer import Optimizer
 
 from ml.core.config import BaseConfig, BaseObject
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/cosine.py` & `ml-starter-0.0.37/ml/lr_schedulers/cosine.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a cosine learning rate scheduler."""
+
 import math
 from dataclasses import dataclass
 
 from omegaconf import MISSING, OmegaConf
 
 from ml.core.config import conf_field
 from ml.core.registry import register_lr_scheduler
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/cosine_decay.py` & `ml-starter-0.0.37/ml/lr_schedulers/cosine_decay.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a cosine learning rate scheduler with decay."""
+
 import math
 from dataclasses import dataclass
 
 from omegaconf import II, MISSING, OmegaConf
 
 from ml.core.config import conf_field
 from ml.core.registry import register_lr_scheduler
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/linear.py` & `ml-starter-0.0.37/ml/lr_schedulers/linear.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""Defines a linear warmup and decay learning rate scheduler.
+
+This scheduler first warms up some number of steps, then smoothly decays
+until the end of training.
+"""
+
 from dataclasses import dataclass
 
 from omegaconf import II, MISSING, OmegaConf
 
 from ml.core.config import conf_field
 from ml.core.registry import register_lr_scheduler
 from ml.core.state import State
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/linear_no_decay.py` & `ml-starter-0.0.37/ml/lr_schedulers/linear_no_decay.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a linear warmup scheduler without decay."""
+
 from dataclasses import dataclass
 
 from ml.core.config import conf_field
 from ml.core.registry import register_lr_scheduler
 from ml.core.state import State
 from ml.lr_schedulers.base import BaseLRScheduler, BaseLRSchedulerConfig
```

### Comparing `ml-starter-0.0.36/ml/lr_schedulers/scripts/plot.py` & `ml-starter-0.0.37/ml/lr_schedulers/scripts/plot.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,20 +1,28 @@
+"""A simple script for plotting learning rate schedules with various parameters.
+
+This script can be used as follows:
+
+.. code-block:: bash
+
+    python -m ml.lr_schedulers.scripts.plot linear /path/to/save.png
+"""
+
 import argparse
 from pathlib import Path
 
 import matplotlib.pyplot as plt
 
 from ml.core.registry import register_lr_scheduler
 from ml.core.state import State
 from ml.utils.argparse import add_args, from_args
 
 
 def main() -> None:
     """Plots a learning rate schedule."""
-
     # Gets the plotting-specific arguments.
     parser = argparse.ArgumentParser(description="Plots a learning rate schedule")
     parser.add_argument("lr_scheduler", help="Which scheduler to plot")
     parser.add_argument("save_path", help="Where to save the plot")
     parser.add_argument("-n", "--num-iters", type=int, default=100_000, help="Number of iterations")
     parser.add_argument("-s", "--stride", type=int, default=100, help="Stride between iterations")
     args, cli_args = parser.parse_known_args()
```

### Comparing `ml-starter-0.0.36/ml/models/activations.py` & `ml-starter-0.0.37/ml/models/activations.py`

 * *Files 0% similar despite different names*

```diff
@@ -145,15 +145,14 @@
 
     Returns:
         The activation function as a module
 
     Raises:
         NotImplementedError: If the activation function is invalid
     """
-
     match act:
         case "no_act":
             return nn.Identity()
         case "relu":
             return nn.ReLU(inplace=inplace)
         case "relu2":
             return nn.ReLU(inplace=inplace)
```

### Comparing `ml-starter-0.0.36/ml/models/base.py` & `ml-starter-0.0.37/ml/models/base.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,12 @@
+"""The base object and config for all models.
+
+This is essentially just a small wrapper around a vanilla PyTorch module.
+"""
+
 import logging
 from dataclasses import dataclass
 from typing import Generic, TypeVar
 
 import torch
 from torch import Tensor, nn
```

### Comparing `ml-starter-0.0.36/ml/models/embeddings.py` & `ml-starter-0.0.37/ml/models/embeddings.py`

 * *Files 0% similar despite different names*

```diff
@@ -69,15 +69,14 @@
 
         Args:
             max_tsz: The maximum sequence length.
             embed_dim: The embedding dimension.
             weight_init: The initialization type for the embedding weight.
             learnable: Whether the embeddings are learnable.
         """
-
         super().__init__()
 
         self.max_tsz = max_tsz
         self.embed_dim = embed_dim
         self.weight_init = weight_init
 
         self.embeddings = nn.Parameter(torch.empty(max_tsz, embed_dim), requires_grad=learnable)
@@ -102,15 +101,14 @@
 
         Args:
             max_tsz: The maximum sequence length.
             embed_dim: The embedding dimension.
             learnable: Whether the embeddings are learnable.
             base: The base for the sinusoidal embeddings.
         """
-
         self.learnable = learnable
         self.base = base
 
         super().__init__(max_tsz, embed_dim, learnable=learnable)
 
     def reset_parameters(self) -> None:
         self.embeddings.data.copy_(self.get_embeddings(self.max_tsz))
@@ -137,15 +135,14 @@
 
         Args:
             max_tsz: The maximum sequence length.
             embed_dim: The embedding dimension.
             learnable: Whether the embeddings are learnable.
             base: The base for the sinusoidal embeddings.
         """
-
         super().__init__()
 
         assert embed_dim % 4 == 0, "Embedding dimension must be divisible by 4."
 
         self.embed_dim = embed_dim
         self.learnable = learnable
         self.base = base
@@ -254,15 +251,14 @@
 
     Returns:
         The positional embeddings module.
 
     Raises:
         ValueError: If an invalid embedding kind is supplied.
     """
-
     match kind:
         case "identity":
             return IdentityPositionalEmbeddings()
 
         case "learned":
             return LearnedPositionalEmbeddings(
                 max_tsz=max_tsz,
```

### Comparing `ml-starter-0.0.36/ml/models/init.py` & `ml-starter-0.0.37/ml/models/init.py`

 * *Files 0% similar despite different names*

```diff
@@ -83,15 +83,14 @@
     Returns:
         The initialized weight and bias (which can be discarded, since the
         initialization happens in-place).
 
     Raises:
         NotImplementedError: If the initialization mode isn't implemented
     """
-
     # Don't do anything for meta tensors.
     if weight.is_meta:
         return weight, bias
     if isinstance(weight, nn.Parameter):
         weight = weight.data
     if isinstance(bias, nn.Parameter):
         bias = bias.data
```

### Comparing `ml-starter-0.0.36/ml/models/lora.py` & `ml-starter-0.0.37/ml/models/lora.py`

 * *Files 1% similar despite different names*

```diff
@@ -116,20 +116,19 @@
 
         if mode:
             if self.merge and self.merged:
                 # Make sure that the weights are not merged
                 if self.lora_a is not None and self.lora_b is not None:
                     self.weight.data -= (self.lora_b @ self.lora_a).transpose(0, 1) * self.scaling
                 self.merged = False
-        else:
-            if self.merge and not self.merged:
-                # Merge the weights and mark it
-                if self.lora_a is not None and self.lora_b is not None:
-                    self.weight.data += (self.lora_b @ self.lora_a).transpose(0, 1) * self.scaling
-                self.merged = True
+        elif self.merge and not self.merged:
+            # Merge the weights and mark it
+            if self.lora_a is not None and self.lora_b is not None:
+                self.weight.data += (self.lora_b @ self.lora_a).transpose(0, 1) * self.scaling
+            self.merged = True
 
         return self
 
     def forward(self, x: Tensor) -> Tensor:
         if self.lora_a is not None and self.lora_b is not None and not self.merged:
             result = super().forward(x)
             after_a = F.embedding(
@@ -203,20 +202,19 @@
         if mode:
             if self.merge and self.merged:
                 # Make sure that the weights are not merged
                 if self.lora_a is not None and self.lora_b is not None:
                     self.weight.data -= self._t(self.lora_b @ self.lora_a) * self.scaling
                 self.merged = False
 
-        else:
-            if self.merge and not self.merged:
-                # Merge the weights and mark it
-                if self.lora_a is not None and self.lora_b is not None:
-                    self.weight.data += self._t(self.lora_b @ self.lora_a) * self.scaling
-                self.merged = True
+        elif self.merge and not self.merged:
+            # Merge the weights and mark it
+            if self.lora_a is not None and self.lora_b is not None:
+                self.weight.data += self._t(self.lora_b @ self.lora_a) * self.scaling
+            self.merged = True
 
         return self
 
     def forward(self, x: Tensor) -> Tensor:
         if self.lora_a is not None and self.lora_b is not None and not self.merged:
             result = F.linear(x, self._t(self.weight), bias=self.bias)
             mm = self.dropout(x) @ self.lora_a.transpose(0, 1) @ self.lora_b.transpose(0, 1)
@@ -284,20 +282,19 @@
         if mode:
             if self.merge and self.merged:
                 # Make sure that the weights are not merged
                 if self.lora_a is not None and self.lora_b is not None:
                     self.weight.data -= self.lora_b @ self.lora_a * self.scaling
                 self.merged = False
 
-        else:
-            if self.merge and not self.merged:
-                # Merge the weights and mark it
-                if self.lora_a is not None and self.lora_b is not None:
-                    self.weight.data += self.lora_b @ self.lora_a * self.scaling
-                self.merged = True
+        elif self.merge and not self.merged:
+            # Merge the weights and mark it
+            if self.lora_a is not None and self.lora_b is not None:
+                self.weight.data += self.lora_b @ self.lora_a * self.scaling
+            self.merged = True
 
         return self
 
     def forward(self, x: Tensor) -> Tensor:
         if self.lora_a is not None and self.lora_b is not None and not self.merged:
             result = F.conv1d(x, self.weight, self.bias, self.stride, self.padding, self.dilation, self.groups)
             mm_a = F.conv1d(self.dropout(x), self.lora_a, None, self.stride, self.padding, self.dilation, self.groups)
@@ -366,20 +363,19 @@
         if mode:
             if self.merge and self.merged:
                 # Make sure that the weights are not merged
                 if self.lora_a is not None and self.lora_b is not None:
                     self.weight.data -= self.lora_b @ self.lora_a * self.scaling
                 self.merged = False
 
-        else:
-            if self.merge and not self.merged:
-                # Merge the weights and mark it
-                if self.lora_a is not None and self.lora_b is not None:
-                    self.weight.data += self.lora_b @ self.lora_a * self.scaling
-                self.merged = True
+        elif self.merge and not self.merged:
+            # Merge the weights and mark it
+            if self.lora_a is not None and self.lora_b is not None:
+                self.weight.data += self.lora_b @ self.lora_a * self.scaling
+            self.merged = True
 
         return self
 
     def forward(self, x: Tensor) -> Tensor:
         if self.lora_a is not None and self.lora_b is not None and not self.merged:
             result = F.conv2d(x, self.weight, self.bias, self.stride, self.padding, self.dilation, self.groups)
             mm_a = F.conv2d(self.dropout(x), self.lora_a, None, self.stride, self.padding, self.dilation, self.groups)
@@ -607,15 +603,14 @@
 
     Returns:
         The LoRA version of the module.
 
     Raises:
         ValueError: If the module is not supported.
     """
-
     if isinstance(module, nn.Embedding):
         return LoraEmbedding(
             module.num_embeddings,
             module.embedding_dim,
             r=r,
             lora_alpha=alpha,
             merge=merge,
```

### Comparing `ml-starter-0.0.36/ml/models/norms.py` & `ml-starter-0.0.37/ml/models/norms.py`

 * *Files 0% similar despite different names*

```diff
@@ -184,15 +184,14 @@
 
     Returns:
         A normalization layer
 
     Raises:
         NotImplementedError: If `norm` is not a valid 1D norm type
     """
-
     match norm:
         case "no_norm":
             return nn.Identity()
         case "batch" | "batch_affine":
             if dim is None:
                 return nn.LazyBatchNorm1d(affine=norm == "batch_affine", device=device, dtype=dtype)
             return nn.BatchNorm1d(dim, affine=norm == "batch_affine", device=device, dtype=dtype)
@@ -230,15 +229,14 @@
 
     Returns:
         A normalization layer
 
     Raises:
         NotImplementedError: If `norm` is not a valid 2D norm type
     """
-
     match norm:
         case "no_norm":
             return nn.Identity()
         case "batch" | "batch_affine":
             if dim is None:
                 return nn.LazyBatchNorm2d(affine=norm == "batch_affine", device=device, dtype=dtype)
             return nn.BatchNorm2d(dim, affine=norm == "batch_affine", device=device, dtype=dtype)
@@ -276,15 +274,14 @@
 
     Returns:
         A normalization layer
 
     Raises:
         NotImplementedError: If `norm` is not a valid 3D norm type
     """
-
     match norm:
         case "no_norm":
             return nn.Identity()
         case "batch" | "batch_affine":
             if dim is None:
                 return nn.LazyBatchNorm3d(affine=norm == "batch_affine", device=device, dtype=dtype)
             return nn.BatchNorm3d(dim, affine=norm == "batch_affine", device=device, dtype=dtype)
@@ -320,15 +317,14 @@
 
     Returns:
         A normalization layer
 
     Raises:
         NotImplementedError: If `norm` is not a valid linear norm type
     """
-
     match norm:
         case "no_norm":
             return nn.Identity()
         case "batch" | "batch_affine":
             assert dim is not None, "`dim` is required for batch norm"
             return LastBatchNorm(dim, affine=norm == "batch_affine", device=device, dtype=dtype)
         case "layer" | "layer_affine":
```

### Comparing `ml-starter-0.0.36/ml/models/pretrained/clip.py` & `ml-starter-0.0.37/ml/models/pretrained/clip.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-# pylint: disable=too-many-lines
 """Defines a simple API for using OpenAI's pretrained CLIP model.
 
 .. highlight:: python
 .. code-block:: python
 
     from ml.models.pretrained.clip import pretrained_clip
 
@@ -57,34 +56,34 @@
 from ml.utils.device.base import BaseDevice
 from ml.utils.logging import configure_logging
 
 logger = logging.getLogger(__name__)
 
 URL_PREFIX = "https://openaipublic.azureedge.net/clip/models"
 
-PretrainedModel = Literal[
+PretrainedClipSize = Literal[
     "RN50",
     "RN101",
     "RN50x4",
     "RN50x16",
     "RN50x64",
     "ViT_B_32",
     "ViT_B_16",
     "ViT_L_14",
     "ViT_L_14_336px",
 ]
 
 
-def cast_pretrained_model_key(s: str) -> PretrainedModel:
-    args = get_args(PretrainedModel)
+def cast_pretrained_model_key(s: str) -> PretrainedClipSize:
+    args = get_args(PretrainedClipSize)
     assert s in args, f"Invalid pretraiend model key: '{s}' Valid options are {args}"
-    return cast(PretrainedModel, s)
+    return cast(PretrainedClipSize, s)
 
 
-PRETRAINED_MODELS: dict[PretrainedModel, str] = {
+PRETRAINED_MODELS: dict[PretrainedClipSize, str] = {
     "RN50": f"{URL_PREFIX}/afeb0e10f9e5a86da6080e35cf09123aca3b358a0c3e3b6c78a7b63bc04b6762/RN50.pt",
     "RN101": f"{URL_PREFIX}/8fa8567bab74a42d41c5915025a8e4538c3bdbe8804a470a72f30b0d94fab599/RN101.pt",
     "RN50x4": f"{URL_PREFIX}/7e526bd135e493cef0776de27d5f42653e6b4c8bf9e0f653bb11773263205fdd/RN50x4.pt",
     "RN50x16": f"{URL_PREFIX}/52378b407f34354e150460fe41077663dd5b39c54cd0bfd2b27167a4a06ec9aa/RN50x16.pt",
     "RN50x64": f"{URL_PREFIX}/be1cfb55d75a9666199fb2206c106743da0f6468c9d327f3e0d0a543a9919d9c/RN50x64.pt",
     "ViT_B_32": f"{URL_PREFIX}/40d365715913c9da98579312b702a82c18be219cc2a73407c4526f58eba950af/ViT-B-32.pt",
     "ViT_B_16": f"{URL_PREFIX}/5806e77cd80f8b59890b7e101eabd078d9fb84e6937f9e85e4ecb61988df416f/ViT-B-16.pt",
@@ -139,15 +138,14 @@
     say, 32K bpe vocab. To avoid that, we want lookup tables between utf-8
     bytes and unicode strings. And avoids mapping to whitespace/control
     characters the BPE code barfs on.
 
     Returns:
         Mapping from UTF-8 byte to unicode string.
     """
-
     bs = list(range(ord("!"), ord("~") + 1))
     bs += list(range(ord("¡"), ord("¬") + 1))
     bs += list(range(ord("®"), ord("ÿ") + 1))
     cs = bs[:]
     n = 0
     for b in range(2**8):
         if b not in bs:
@@ -166,15 +164,15 @@
         prev_char = char
     return pairs
 
 
 @functools.lru_cache()
 def test_clean_func(lower: bool = True) -> Callable[[str], str]:
     try:
-        import ftfy  # type: ignore
+        import ftfy  # type: ignore[import]
 
     except ImportError:
         logger.warning("Please install ftfy: pip install ftfy")
         ftfy = None
 
     def _clean(text: str) -> str:
         if ftfy is not None:
@@ -427,15 +425,14 @@
             output_dim: Number of final output dimensions
             heads: Number of attention heads
             input_resolution: Number of pixels in width and height directions
             width: Hidden channel count
             device: Default PyTorch device to use
             dtype: Default PyTorch dtype to use
         """
-
         super().__init__()
 
         self.output_dim = output_dim
         self.input_resolution = input_resolution
 
         # The 3-layer stem
         self.conv1 = nn.Conv2d(
@@ -571,15 +568,15 @@
         width: int,
         layers: int,
         heads: int,
         attn_mask: Tensor | None = None,
         *,
         device: torch.device | None = None,
         dtype: torch.dtype | None = None,
-    ):
+    ) -> None:
         super().__init__()
         self.width = width
         self.layers = layers
         blocks = [ResidualAttentionBlock(width, heads, attn_mask, device=device, dtype=dtype) for _ in range(layers)]
         self.resblocks = nn.Sequential(*blocks)
 
     def forward(self, x: Tensor) -> Tensor:
@@ -865,15 +862,14 @@
         module without worrying about storing all the weights on accident.
 
         Args:
             clip_model: The CLIP model to use for predictions
             device: The device to use for predictions. If None, will use the
                 device returned by AutoDevice.detect_device().
         """
-
         super().__init__()
 
         self.device = AutoDevice.detect_device() if device is None else device
         self.model = clip_model.eval()
         self.device.module_to(self.model)
         self.tokenizer = self.model.linguistic.get_tokenizer()
         self.pil_preprocess = self.model.get_pil_preprocess()
@@ -921,47 +917,47 @@
                     attr.data = attr.data.half()
 
     model.apply(_convert_weights_to_fp16)
 
 
 @overload
 def pretrained_clip(
-    key: PretrainedModel | nn.Module,
+    key: PretrainedClipSize | nn.Module,
     mode: Literal["visual"],
     *,
     device: torch.device | None = None,
     dtype: torch.dtype | None = None,
 ) -> ModifiedResNet | VisionTransformer:
     ...
 
 
 @overload
 def pretrained_clip(
-    key: PretrainedModel | nn.Module,
+    key: PretrainedClipSize | nn.Module,
     mode: Literal["linguistic"],
     *,
     device: torch.device | None = None,
     dtype: torch.dtype | None = None,
 ) -> TextModel:
     ...
 
 
 @overload
 def pretrained_clip(
-    key: PretrainedModel | nn.Module,
+    key: PretrainedClipSize | nn.Module,
     mode: Literal["all"],
     *,
     device: torch.device | None = None,
     dtype: torch.dtype | None = None,
 ) -> Clip:
     ...
 
 
 def pretrained_clip(
-    key: PretrainedModel | nn.Module,
+    key: PretrainedClipSize | nn.Module,
     mode: str,
     *,
     device: torch.device | None = None,
     dtype: torch.dtype | None = None,
 ) -> Clip | ModifiedResNet | VisionTransformer | TextModel:
     """Builds the CLIP model from a state dictionary.
 
@@ -971,15 +967,14 @@
             the visual or linguistic part of the model
         device: The device for the model
         dtype: The dtype for the model
 
     Returns:
         The constructed clip model, or just the visual or text branch
     """
-
     assert mode in ("all", "visual", "linguistic")
 
     if isinstance(key, nn.Module):
         ckpt = key.state_dict()
     else:
         filepath = get_pretrained_path(key)
         ckpt = torch.jit.load(filepath, map_location="cpu").state_dict()
@@ -1049,29 +1044,29 @@
         model.linguistic.load_state_dict(get_ckpt_part(ckpt, "linguistic."))
         return model.linguistic
     else:
         model.load_state_dict(ckpt)
         return model
 
 
-def get_pretrained_path(key: PretrainedModel) -> Path:
+def get_pretrained_path(key: PretrainedClipSize) -> Path:
     if key not in PRETRAINED_MODELS:
         raise KeyError(f"Invalid CLIP model key {key}; choices are {list(PRETRAINED_MODELS.keys())}")
     model_url = PRETRAINED_MODELS[key]
     save_path = (get_model_dir() / f"CLIP_{key}").resolve()
     filename = "ckpt.pt"
     filepath = save_path / filename
     if not filepath.exists():
         download_url(model_url, str(save_path), filename=filename)
     return filepath
 
 
 def test_pretrained_model() -> None:
     parser = argparse.ArgumentParser(description="Tests a pretraiend CLIP model")
-    parser.add_argument("key", type=str, choices=get_args(PretrainedModel))
+    parser.add_argument("key", type=str, choices=get_args(PretrainedClipSize))
     args = parser.parse_args()
 
     configure_logging()
 
     # Gets an image of a peach from Wikipedia.
     peach_url = "https://upload.wikimedia.org/wikipedia/commons/9/9e/Autumn_Red_peaches.jpg"
     url_path = Path("/tmp/peach.jpg")
@@ -1080,15 +1075,15 @@
 
     peach_img = PIL.Image.open(url_path)
     pos_desc = "A picture of an Autumn Red peach"
     neg_desc = "An Instagram photo of a cute puppy"
 
     # Loads the JIT'd model and the regular model.
     auto_device = AutoDevice.detect_device()
-    jit_model = cast(Clip, torch.jit.load(get_pretrained_path(cast(PretrainedModel, args.key)), map_location="cpu"))
+    jit_model = cast(Clip, torch.jit.load(get_pretrained_path(cast(PretrainedClipSize, args.key)), map_location="cpu"))
     model = pretrained_clip(jit_model, "all")
 
     # Moves to the correct device.
     auto_device.module_to(jit_model)
     auto_device.module_to(model)
 
     # Puts in eval mode.
```

### Comparing `ml-starter-0.0.36/ml/models/pretrained/hubert.py` & `ml-starter-0.0.37/ml/models/pretrained/hubert.py`

 * *Files 0% similar despite different names*

```diff
@@ -34,15 +34,15 @@
 from ml.core.env import get_model_dir
 from ml.models.activations import ActivationType, get_activation
 from ml.utils.data import check_sha256
 from ml.utils.device.auto import AutoDevice
 from ml.utils.device.base import BaseDevice
 from ml.utils.logging import configure_logging
 
-HubertSize = Literal["base", "large", "extra_large"]
+PretrainedHubertSize = Literal["base", "large", "extra_large"]
 
 
 @dataclass
 class HubertConfig:
     vocab_size: int
     hidden_size: int
     num_hidden_layers: int
@@ -122,15 +122,15 @@
         hidden_states = self.activation(hidden_states)
 
         hidden_states = hidden_states.transpose(1, 2)
         return hidden_states
 
 
 class HubertAttention(nn.Module):
-    """Multi-headed attention from 'Attention Is All You Need' paper"""
+    """Multi-headed attention from 'Attention Is All You Need' paper."""
 
     def __init__(
         self,
         embed_dim: int,
         num_heads: int,
         dropout: float = 0.0,
         is_decoder: bool = False,
@@ -181,15 +181,14 @@
             updated past key and value states (if `past_key_value` is provided).
 
         Raises:
             ValueError: If `past_key_value` is not `None` and `key_value_states`
                 is either `None` or has a different sequence length than the
                 `past_key_value` tuple.
         """
-
         bsz, tgt_len, _ = hidden_states.size()
 
         query_states = self.q_proj(hidden_states) * self.scaling
 
         if (
             key_value_states is not None
             and past_key_value is not None
@@ -473,18 +472,18 @@
             is_decoder=False,
         )
         self.dropout = nn.Dropout(config.hidden_dropout)
         self.layer_norm = nn.LayerNorm(config.hidden_size, eps=config.layer_norm_eps)
         self.feed_forward = HubertFeedForward(config)
         self.final_layer_norm = nn.LayerNorm(config.hidden_size, eps=config.layer_norm_eps)
 
-    def forward(self, hidden_states: Tensor, attention_mask: Tensor | None = None) -> Tensor:
+    def forward(self, hidden_states: Tensor, attn_mask: Tensor | None = None) -> Tensor:
         attn_residual = hidden_states
         hidden_states = self.layer_norm(hidden_states)
-        hidden_states, _, _ = self.attention(hidden_states, attention_mask=attention_mask)
+        hidden_states, _ = self.attention(hidden_states, attn_mask=attn_mask)
         hidden_states = self.dropout(hidden_states)
         hidden_states = attn_residual + hidden_states
         hidden_states = hidden_states + self.feed_forward(self.final_layer_norm(hidden_states))
         return hidden_states
 
 
 class HubertEncoderStableLayerNorm(nn.Module):
@@ -516,15 +515,15 @@
         hidden_states = self.layer_norm(hidden_states)
         return hidden_states
 
 
 class Hubert(nn.Module):
     __constants__ = ["conv_kernel", "conv_stride"]
 
-    def __init__(self, config: HubertConfig):
+    def __init__(self, config: HubertConfig) -> None:
         super().__init__()
 
         self.conv_kernel = config.conv_kernel
         self.conv_stride = config.conv_stride
         self.pre_normalize = config.pre_normalize
 
         self.feature_extractor = HubertFeatureEncoder(config)
@@ -577,15 +576,14 @@
         module without worrying about storing all the weights on accident.
 
         Args:
             hubert_model: The HuBERT model to use for predictions.
             device: The device to use for predictions. If `None`, will use the
                 device returned by AutoDevice.detect_device().
         """
-
         super().__init__()
 
         self.device = AutoDevice.detect_device() if device is None else device
         self.model = hubert_model.eval()
         self.device.module_to(self.model)
 
     def predict(self, waveform: np.ndarray | Tensor, output_layer: int | None = None) -> Tensor:
@@ -595,15 +593,14 @@
             waveform: The waveform to get hidden states for, with shape (B, T)
             output_layer: The layer to get hidden states from. If `None`, will
                 return the hidden states from the last layer.
 
         Returns:
             The hidden states for the given waveform, with shape (B, T, D)
         """
-
         waveform = self.device.tensor_to(waveform)
         return self.model.forward(waveform, attn_mask=None, output_layer=output_layer)
 
     def predict_in_chunks(
         self,
         waveform: Tensor | np.ndarray,
         chunk_size: int,
@@ -620,36 +617,35 @@
             chunk_size: The size of each chunk to process.
             output_layer: The layer to get hidden states from. If `None`, will
                 return the hidden states from the last layer.
 
         Returns:
             The hidden states for the given waveform, with shape (B, T, D)
         """
-
         with torch.inference_mode():
             x = self.device.tensor_to(waveform)  # Loads entire waveform into device memory.
 
             if self.model.pre_normalize:
                 x = F.layer_norm(x, x.shape)
             x = x.view(1, -1)
 
             feat = []
             for start in range(0, x.size(1), chunk_size):
                 x_chunk = x[:, start : start + chunk_size]
-                feat_chunk, _ = self.model(x_chunk, output_layer=output_layer)
+                feat_chunk = self.model.forward(x_chunk, output_layer=output_layer)
                 feat.append(feat_chunk)
 
         return torch.cat(feat, 1).squeeze(0)
 
 
 EXCLUDE_KEYS = {"masked_spec_embed", ".weight", ".bias"}
 
 
 def _load_pretrained_hubert(
-    size: HubertSize,
+    size: PretrainedHubertSize,
     ckpt_url: str,
     sha256: str,
     config: HubertConfig,
     remove_prefix: str | None = None,
 ) -> Hubert:
     model = Hubert(config)
 
@@ -668,15 +664,15 @@
         ckpt = {k[len(remove_prefix) :]: v for k, v in ckpt.items()}
     ckpt = {k: v for k, v in ckpt.items() if k not in EXCLUDE_KEYS}
     model.load_state_dict(ckpt)
 
     return model
 
 
-def hubert(size: HubertSize) -> Hubert:
+def pretrained_hubert(size: PretrainedHubertSize) -> Hubert:
     match size:
         case "base":
             return _load_pretrained_hubert(
                 size,
                 ckpt_url="https://huggingface.co/facebook/hubert-base-ls960/resolve/main/pytorch_model.bin",
                 sha256="062249fffb353eab67547a2fbc129f7c31a2f459faf641b19e8fb007cc5c48ad",
                 config=HubertConfig(
@@ -770,22 +766,22 @@
                     pre_normalize=True,
                 ),
             )
 
 
 def test_hubert_adhoc() -> None:
     parser = argparse.ArgumentParser()
-    parser.add_argument("size", type=str, choices=get_args(HubertSize))
+    parser.add_argument("size", type=str, choices=get_args(PretrainedHubertSize))
     parser.add_argument("-t", "--tsz", type=int, default=22400)
     args = parser.parse_args()
 
     configure_logging()
 
     # Loads the model and moves to the right device.
-    model = hubert(size=cast(HubertSize, args.size))
+    model = pretrained_hubert(size=cast(PretrainedHubertSize, args.size))
     predictor = model.predictor()
 
     # Test the model on a random waveform.
     y = predictor.predict(torch.randn(1, args.tsz))
     assert (args.tsz // 320) == y.shape[1] + 1
```

### Comparing `ml-starter-0.0.36/ml/models/pretrained/sam.py` & `ml-starter-0.0.37/ml/models/pretrained/sam.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,15 +38,16 @@
 from torchvision.transforms.functional import resize, to_pil_image
 
 from ml.core.env import get_model_dir
 from ml.utils.device.auto import AutoDevice
 from ml.utils.device.base import BaseDevice
 from ml.utils.logging import configure_logging
 
-PretrainedModel = Literal["ViT-H", "ViT-L", "ViT-B"]
+PretrainedSamSize = Literal["ViT-H", "ViT-L", "ViT-B"]
+
 ImageFormat = Literal["RGB", "BGR"]
 
 DEFAULT_PIXEL_MEAN = (123.675, 116.28, 103.53)
 DEFAULT_PIXEL_STD = (58.395, 57.12, 57.375)
 
 
 @dataclass
@@ -54,15 +55,15 @@
     url: str
     encoder_embed_dim: int
     encoder_depth: int
     encoder_num_heads: int
     encoder_global_attn_indices: tuple[int, int, int, int]
 
 
-PRETRAINED_MODELS: dict[PretrainedModel, PretrainedModelConfig] = {
+PRETRAINED_MODELS: dict[PretrainedSamSize, PretrainedModelConfig] = {
     "ViT-H": PretrainedModelConfig(
         url="https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth",
         encoder_embed_dim=1280,
         encoder_depth=32,
         encoder_num_heads=16,
         encoder_global_attn_indices=(7, 15, 23, 31),
     ),
@@ -151,15 +152,14 @@
             norm_layer: Normalization layer.
             act_layer: Activation layer.
             use_abs_pos: If True, use absolute positional embeddings.
             use_rel_pos: If True, add relative positional embeddings to the attention map.
             window_size: Window size for window attention blocks.
             global_attn_indexes: Indexes for blocks using global attention.
         """
-
         super().__init__()
 
         self.img_size = img_size
 
         self.patch_embed = PatchEmbed(
             kernel_size=(patch_size, patch_size),
             stride=(patch_size, patch_size),
@@ -241,15 +241,14 @@
             use_rel_pos: If True, add relative positional embeddings to the
                 attention map.
             window_size: Window size for window attention blocks. If it equals
                 0, then use global attention.
             input_size: Input resolution for calculating the relative positional
                 parameter size.
         """
-
         super().__init__()
 
         self.norm1 = norm_layer(dim)
         self.attn = Attention(
             dim,
             num_heads=num_heads,
             qkv_bias=qkv_bias,
@@ -264,22 +263,22 @@
 
     def forward(self, x: Tensor) -> Tensor:
         shortcut = x
         x = self.norm1(x)
 
         # Window partition
         if self.window_size > 0:
-            H, W = x.shape[1], x.shape[2]
+            hei, wid = x.shape[1], x.shape[2]
             x, pad_hw = window_partition(x, self.window_size)
 
         x = self.attn(x)
 
         # Reverse window partition
         if self.window_size > 0:
-            x = window_unpartition(x, self.window_size, pad_hw, (H, W))
+            x = window_unpartition(x, self.window_size, pad_hw, (hei, wid))
 
         x = shortcut + x
         x = x + self.mlp(self.norm2(x))
 
         return x
 
 
@@ -299,15 +298,14 @@
             num_heads: Number of attention heads.
             qkv_bias:  If True, add a learnable bias to query, key, value.
             use_rel_pos: If True, add relative positional embeddings to the
                 attention map.
             input_size: Input resolution for calculating the relative positional
                 parameter size.
         """
-
         super().__init__()
 
         self.num_heads = num_heads
         head_dim = dim // num_heads
         self.scale = head_dim**-0.5
 
         self.qkv = nn.Linear(dim, dim * 3, bias=qkv_bias)
@@ -345,64 +343,61 @@
         x: Input tokens with shape (B, H, W, C).
         window_size: Window size.
 
     Returns:
         Windows after partition with shape (B * n_win, win_size, win_size, C),
         and the shape.
     """
+    bsz, hei, wid, chans = x.shape
 
-    B, H, W, C = x.shape
-
-    pad_h = (window_size - H % window_size) % window_size
-    pad_w = (window_size - W % window_size) % window_size
+    pad_h = (window_size - hei % window_size) % window_size
+    pad_w = (window_size - wid % window_size) % window_size
     if pad_h > 0 or pad_w > 0:
         x = F.pad(x, (0, 0, 0, pad_w, 0, pad_h))
-    Hp, Wp = H + pad_h, W + pad_w
+    hei_p, wid_p = hei + pad_h, wid + pad_w
 
-    x = x.view(B, Hp // window_size, window_size, Wp // window_size, window_size, C)
-    windows = x.permute(0, 1, 3, 2, 4, 5).contiguous().view(-1, window_size, window_size, C)
-    return windows, (Hp, Wp)
+    x = x.view(bsz, hei_p // window_size, window_size, wid_p // window_size, window_size, chans)
+    windows = x.permute(0, 1, 3, 2, 4, 5).contiguous().view(-1, window_size, window_size, chans)
+    return windows, (hei_p, wid_p)
 
 
 def window_unpartition(windows: Tensor, window_size: int, pad_hw: tuple[int, int], hw: tuple[int, int]) -> Tensor:
     """Window unpartition into original sequences and removing padding.
 
     Args:
         windows: Input tokens with (B * n_win, win_size, win_size, C).
         window_size: Window size.
         pad_hw: Padded height and width (Hp, Wp).
         hw: Original height and width (H, W) before padding.
 
     Returns:
         The unpartitioned sequences with shape (B, H, W, C).
     """
+    hei_p, wid_p = pad_hw
+    hei, wid = hw
+    bsz = windows.shape[0] // (hei_p * wid_p // window_size // window_size)
+    x = windows.view(bsz, hei_p // window_size, wid_p // window_size, window_size, window_size, -1)
+    x = x.permute(0, 1, 3, 2, 4, 5).contiguous().view(bsz, hei_p, wid_p, -1)
 
-    Hp, Wp = pad_hw
-    H, W = hw
-    B = windows.shape[0] // (Hp * Wp // window_size // window_size)
-    x = windows.view(B, Hp // window_size, Wp // window_size, window_size, window_size, -1)
-    x = x.permute(0, 1, 3, 2, 4, 5).contiguous().view(B, Hp, Wp, -1)
-
-    if Hp > H or Wp > W:
-        x = x[:, :H, :W, :].contiguous()
+    if hei_p > hei or wid_p > wid:
+        x = x[:, :hei, :wid, :].contiguous()
     return x
 
 
 def get_rel_pos(q_size: int, k_size: int, rel_pos: Tensor) -> Tensor:
     """Get relative positional embeddings.
 
     Args:
         q_size: Size of query q.
         k_size: Size of key k.
         rel_pos: Relative position embeddings (L, C).
 
     Returns:
         Extracted positional embeddings according to relative positions.
     """
-
     max_rel_dist = int(2 * max(q_size, k_size) - 1)
 
     # Interpolate rel pos if needed.
     if rel_pos.shape[0] != max_rel_dist:
         rel_pos_resized = F.interpolate(
             rel_pos.reshape(1, rel_pos.shape[0], -1).permute(0, 2, 1),
             size=max_rel_dist,
@@ -439,27 +434,26 @@
         rel_pos_w: Relative position embeddings (Lw, C) for width axis.
         q_size: Spatial sequence size of query q with (q_h, q_w).
         k_size: Spatial sequence size of key k with (k_h, k_w).
 
     Returns:
         Attention map with added relative positional embeddings.
     """
-
     q_h, q_w = q_size
     k_h, k_w = k_size
-    Rh = get_rel_pos(q_h, k_h, rel_pos_h)
-    Rw = get_rel_pos(q_w, k_w, rel_pos_w)
+    rel_h = get_rel_pos(q_h, k_h, rel_pos_h)
+    rel_w = get_rel_pos(q_w, k_w, rel_pos_w)
 
-    B, _, dim = q.shape
-    r_q = q.reshape(B, q_h, q_w, dim)
-    rel_h = torch.einsum("bhwc,hkc->bhwk", r_q, Rh)
-    rel_w = torch.einsum("bhwc,wkc->bhwk", r_q, Rw)
+    bsz, _, dim = q.shape
+    r_q = q.reshape(bsz, q_h, q_w, dim)
+    rel_h = torch.einsum("bhwc,hkc->bhwk", r_q, rel_h)
+    rel_w = torch.einsum("bhwc,wkc->bhwk", r_q, rel_w)
 
-    attn = attn.view(B, q_h, q_w, k_h, k_w) + rel_h[:, :, :, :, None] + rel_w[:, :, :, None, :]
-    attn = attn.view(B, q_h * q_w, k_h * k_w)
+    attn = attn.view(bsz, q_h, q_w, k_h, k_w) + rel_h[:, :, :, :, None] + rel_w[:, :, :, None, :]
+    attn = attn.view(bsz, q_h * q_w, k_h * k_w)
 
     return attn
 
 
 class PatchEmbed(nn.Module):
     def __init__(
         self,
@@ -474,15 +468,14 @@
         Args:
             kernel_size: Kernel size of the projection layer.
             stride: Stride of the projection layer.
             padding: Padding size of the projection layer.
             in_chans: Number of input image channels.
             embed_dim: Patch embedding dimension.
         """
-
         super().__init__()
 
         self.proj = nn.Conv2d(in_chans, embed_dim, kernel_size=kernel_size, stride=stride, padding=padding)
 
     def forward(self, x: Tensor) -> Tensor:
         x = self.proj(x)
         x = x.permute(0, 2, 3, 1)  # (B, C, H, W) -> (B, H, W, C)
@@ -508,15 +501,14 @@
             num_multimask_outputs: The number of masks to predict when
                 disambiguating masks
             activation: The type of activation to use when upscaling masks
             iou_head_depth: The depth of the MLP used to predict mask quality
             iou_head_hidden_dim: The hidden dimension of the MLP used to
                 predict mask quality
         """
-
         super().__init__()
         self.transformer_dim = transformer_dim
         self.transformer = transformer
 
         self.num_multimask_outputs = num_multimask_outputs
 
         self.iou_token = nn.Embedding(1, transformer_dim)
@@ -647,28 +639,26 @@
         self,
         embed_dim: int,
         image_embedding_size: tuple[int, int],
         input_image_size: tuple[int, int],
         mask_in_chans: int,
         activation: Type[nn.Module] = nn.GELU,
     ) -> None:
-        """
-        Encodes prompts for input to SAM's mask decoder.
+        """Encodes prompts for input to SAM's mask decoder.
 
         Args:
             embed_dim: The prompts' embedding dimension
             image_embedding_size: The spatial size of the image embedding,
                 as (H, W).
             input_image_size: The padded size of the image as input to the
                 image encoder, as (H, W).
             mask_in_chans: The number of hidden channels used for encoding
                 input masks.
             activation: The activation to use when encoding input masks.
         """
-
         super().__init__()
 
         self.embed_dim = embed_dim
         self.input_image_size = input_image_size
         self.image_embedding_size = image_embedding_size
         self.pe_layer = PositionEmbeddingRandom(embed_dim // 2)
 
@@ -694,15 +684,14 @@
 
         The embedding is applied to a dense set of points the shape of the
         image encoding.
 
         Returns:
             Positional encoding with shape (1, emb_dim, emb_h, emb_w)
         """
-
         return self.pe_layer(self.image_embedding_size).unsqueeze(0)
 
     def _embed_points(
         self,
         points: Tensor,
         labels: Tensor,
         pad: bool,
@@ -767,15 +756,14 @@
 
         Returns:
             Sparse embeddings for the points and boxes, with shape
             (B, N, embed_dim), where N is determined by the number of
             input points and boxes, and the dense embeddings for the masks,
             with shape (B, emb_dim, emb_h, emb_w)
         """
-
         bs = self._get_batch_size(points, boxes, masks)
         sparse_embeddings = torch.empty((bs, 0, self.embed_dim), device=self._get_device())
         if points is not None:
             coords, labels = points
             point_embeddings = self._embed_points(coords, labels, pad=(boxes is None))
             sparse_embeddings = torch.cat([sparse_embeddings, point_embeddings], dim=1)
         if boxes is not None:
@@ -849,15 +837,14 @@
                 divide embedding_dim
             mlp_dim: The channel dimension internal to the MLP block
             activation: The activation to use in the MLP block
             attention_downsample_rate: The downsample rate for the attention
                 blocks. The attention blocks will downsample the input image
                 by this factor.
         """
-
         super().__init__()
 
         self.depth = depth
         self.embedding_dim = embedding_dim
         self.num_heads = num_heads
         self.mlp_dim = mlp_dim
         self.layers = nn.ModuleList()
@@ -896,15 +883,14 @@
                 have the same shape as image_embedding.
             point_embedding: The embedding to add to the query points. Must
                 have shape (B, N_points, embedding_dim).
 
         Returns:
             The processed point and image embeddings.
         """
-
         image_embedding = image_embedding.flatten(2).permute(0, 2, 1)
         image_pe = image_pe.flatten(2).permute(0, 2, 1)
 
         # Prepare queries
         queries = point_embedding
         keys = image_embedding
 
@@ -950,15 +936,14 @@
             mlp_dim: The hidden dimension of the mlp block
             activation: The activation of the mlp block
             attention_downsample_rate: The downsample rate for the attention
                 blocks. The attention blocks will downsample the input image
                 by this factor.
             skip_first_layer_pe: Skip the PE on the first layer
         """
-
         super().__init__()
         self.self_attn = TwoWayAttentionFunction(embedding_dim, num_heads)
         self.norm1 = nn.LayerNorm(embedding_dim)
 
         self.cross_attn_token_to_image = TwoWayAttentionFunction(
             embedding_dim,
             num_heads,
@@ -1079,15 +1064,14 @@
             image_encoder: The backbone used to encode the image.
             prompt_encoder: Encodes various types of input prompts.
             mask_decoder: Predicts masks from the image embeddings
                 and encoded prompts.
             pixel_mean: Mean values for normalizing pixels in the input image.
             pixel_std: Std values for normalizing pixels in the input image.
         """
-
         super().__init__()
 
         self.image_encoder = image_encoder
         self.prompt_encoder = prompt_encoder
         self.mask_decoder = mask_decoder
         self.register_buffer("pixel_mean", Tensor(pixel_mean).view(-1, 1, 1), False)
         self.register_buffer("pixel_std", Tensor(pixel_std).view(-1, 1, 1), False)
@@ -1130,15 +1114,14 @@
             prompts, C is determined by multimask_output, and (H, W) is the
             original size of the image. The 'iou_predictions' key is the
             model's predictions of mask quality, with shape (B, C). The
             'low_res_logits' key is the low resolution logits with shape
             (B, C, 256, 256). This can be passed as mask input to subsequent
             iterations of prediction.
         """
-
         input_images = torch.stack([self.preprocess(x["image"]) for x in batched_input], dim=0)
         image_embeddings = self.image_encoder(input_images)
 
         outputs = []
         for image_record, curr_embedding in zip(batched_input, image_embeddings):
             if "point_coords" in image_record:
                 points = (image_record["point_coords"], image_record["point_labels"])
@@ -1186,15 +1169,14 @@
             original_size: The original size of the image before resizing for
                 input to the model, in (H, W) format.
 
         Returns:
             Batched masks with shape (B, C, H, W), where (H, W) matches
             the original size.
         """
-
         masks = F.interpolate(
             masks,
             (self.image_encoder.img_size, self.image_encoder.img_size),
             mode="bilinear",
             align_corners=False,
         )
         masks = masks[..., : input_size[0], : input_size[1]]
@@ -1262,23 +1244,22 @@
         return (newh, neww)
 
 
 class SamPredictor:
     def __init__(self, sam_model: Sam, *, device: BaseDevice | None = None) -> None:
         """Provides an API to do repeated mask predictions on an image.
 
-        This predictor tses SAM to calculate the image embedding for an image,
+        This predictor uses SAM to calculate the image embedding for an image,
         and then allow repeated, efficient mask prediction given prompts.
 
         Args:
             sam_model: The model to use for mask prediction.
             device: The device to use for prediction. If None, will use the
                 device returned by AutoDevice.detect_device().
         """
-
         super().__init__()
 
         self.device = AutoDevice.detect_device() if device is None else device
         self.model = sam_model.eval()
         self.device.module_to(self.model)
         self.transform = ResizeLongestSide(sam_model.image_encoder.img_size)
         self.reset_image()
@@ -1290,15 +1271,14 @@
         masks to be predicted with the 'predict' method.
 
         Args:
             image: The image for calculating masks. Expects an image in HWC
                 uint8 format, with pixel values in [0, 255].
             image_format: The color format of the image, in ['RGB', 'BGR'].
         """
-
         assert image_format in get_args(ImageFormat)
 
         if image_format != self.model.image_format:
             image = image[..., ::-1]
 
         # Transform the image to the form expected by the model
         input_image = self.transform.apply_image(image)
@@ -1321,15 +1301,14 @@
 
         Args:
             transformed_image: The input image, with shape (1, 3, H, W), which
                 has been transformed with ResizeLongestSide.
             original_image_size: The size of the image before transformation,
                 in (H, W) format.
         """
-
         assert (
             len(transformed_image.shape) == 4
             and transformed_image.shape[1] == 3
             and max(*transformed_image.shape[2:]) == self.model.image_encoder.img_size
         ), f"set_torch_image input must be BCHW with long side {self.model.image_encoder.img_size}."
         self.reset_image()
 
@@ -1377,15 +1356,14 @@
             and an array of shape (C, H, W), where C is the number of masks and
             H=W=256. These low resolution logits can be passed to a subsequent
             iteration as mask input.
 
         Raises:
             RuntimeError: If an image has not been set yet.
         """
-
         if not self.is_image_set:
             raise RuntimeError("An image must be set with .set_image(...) before mask prediction.")
 
         # Transform input prompts
         coords_torch, labels_torch, box_torch, mask_input_torch = None, None, None, None
         if point_coords is not None:
             assert point_labels is not None, "point_labels must be supplied if point_coords is supplied."
@@ -1461,15 +1439,14 @@
             and an array of shape (C, H, W), where C is the number of masks and
             H=W=256. These low resolution logits can be passed to a subsequent
             iteration as mask input.
 
         Raises:
             RuntimeError: If an image has not been set yet.
         """
-
         if not self.is_image_set:
             raise RuntimeError("An image must be set with .set_image(...) before mask prediction.")
 
         if point_coords is not None:
             points = (point_coords, point_labels)
         else:
             points = None
@@ -1509,27 +1486,27 @@
         self.features = None
         self.orig_h = None
         self.orig_w = None
         self.input_h = None
         self.input_w = None
 
 
-def get_pretrained_path(key: PretrainedModel) -> Path:
+def get_pretrained_path(key: PretrainedSamSize) -> Path:
     if key not in PRETRAINED_MODELS:
         raise KeyError(f"Invalid CLIP model key {key}; choices are {list(PRETRAINED_MODELS.keys())}")
     model_url = PRETRAINED_MODELS[key].url
     save_path = (get_model_dir() / f"SAM_{key}").resolve()
     filename = "ckpt.pt"
     filepath = save_path / filename
     if not filepath.exists():
         download_url(model_url, str(save_path), filename=filename)
     return filepath
 
 
-def pretrained_sam(key: PretrainedModel, *, skip_weights: bool = False) -> Sam:
+def pretrained_sam(key: PretrainedSamSize, *, skip_weights: bool = False) -> Sam:
     config = PRETRAINED_MODELS[key]
 
     prompt_embed_dim = 256
     image_size = 1024
     vit_patch_size = 16
     image_embedding_size = image_size // vit_patch_size
 
@@ -1576,26 +1553,26 @@
         model.load_state_dict(state_dict)
 
     return model
 
 
 def test_pretrained_model() -> None:
     parser = argparse.ArgumentParser(description="Tests a pretrained SAM model")
-    parser.add_argument("key", type=str, choices=get_args(PretrainedModel))
+    parser.add_argument("key", type=str, choices=get_args(PretrainedSamSize))
     args = parser.parse_args()
 
     configure_logging()
 
     # Gets an image of a peach from Wikipedia.
     peach_url = "https://upload.wikimedia.org/wikipedia/commons/9/9e/Autumn_Red_peaches.jpg"
     url_path = Path("/tmp/peach.jpg")
     if not url_path.exists():
         download_url(peach_url, "/tmp", filename="peach.jpg")
 
-    model = pretrained_sam(cast(PretrainedModel, args.key))
+    model = pretrained_sam(cast(PretrainedSamSize, args.key))
     predictor = model.predictor()
 
     peach_img = PIL.Image.open(url_path)
     predictor.set_image(np.array(peach_img))
 
     predictions, _, _ = predictor.predict()
     single_mask = predictions[0]
```

### Comparing `ml-starter-0.0.36/ml/optimizers/adam.py` & `ml-starter-0.0.37/ml/optimizers/adam.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Wrapper around the PyTorch Adam optimizer."""
+
 from dataclasses import dataclass
 
 from torch import nn
 from torch.optim.adam import Adam
 
 from ml.core.config import conf_field
 from ml.core.registry import register_optimizer
```

### Comparing `ml-starter-0.0.36/ml/optimizers/adamw.py` & `ml-starter-0.0.37/ml/optimizers/adamw.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Wrapper around the PyTorch Adamw optimizer."""
+
 from dataclasses import dataclass
 from typing import Any, Iterable
 
 from torch import nn
 from torch.optim.adamw import AdamW
 
 from ml.core.config import conf_field
@@ -19,15 +21,14 @@
         default_decay: Whether to decay by default (for modules which aren't
             explicitly specified)
         weight_decay: The weight decay to use
 
     Returns:
         The dictionary to pass to the optimizer
     """
-
     wd_params: set[str] = set()
     no_wd_params: set[str] = set()
     seen: set[str] = set()
 
     always_decay = (
         nn.Linear,
         nn.Conv1d,
```

### Comparing `ml-starter-0.0.36/ml/optimizers/adan.py` & `ml-starter-0.0.37/ml/optimizers/adan.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Wrapper around the PyTorch Adan optimizer."""
+
 from dataclasses import dataclass
 from typing import Callable, Iterable
 
 import torch
 from torch import nn
 from torch.optim import Optimizer
```

### Comparing `ml-starter-0.0.36/ml/optimizers/base.py` & `ml-starter-0.0.37/ml/optimizers/base.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""Defines the base optimizer adapter.
+
+This class usually just wraps PyTorch optimizers, providing some common
+hyperparameter configurations.
+"""
+
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
 from typing import Any, Generic, TypeVar
 
 from torch import nn
 from torch.optim.optimizer import Optimizer
```

### Comparing `ml-starter-0.0.36/ml/optimizers/sgd.py` & `ml-starter-0.0.37/ml/optimizers/sgd.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a simple SGD optimizer."""
+
 from dataclasses import dataclass
 
 from torch import nn
 from torch.optim.sgd import SGD
 
 from ml.core.config import conf_field
 from ml.core.registry import register_optimizer
```

### Comparing `ml-starter-0.0.36/ml/optimizers/shampoo.py` & `ml-starter-0.0.37/ml/optimizers/shampoo.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""Wrapper around the Shampoo optimizer.
+
+This optimizer was proposed in `Shampoo: Preconditioned Stochastic Tensor
+Optimization <https://arxiv.org/abs/1802.09568>`_.
+"""
+
 from dataclasses import dataclass
 
 import torch
 from torch import Tensor, nn
 from torch.optim.optimizer import Optimizer
 
 from ml.core.config import conf_field
@@ -85,15 +91,14 @@
 
         Args:
             closure: A closure that reevaluates the model and returns the loss.
 
         Returns:
             The total loss
         """
-
         loss = None
         if closure is not None:
             loss = closure()
 
         for group in self.param_groups:
             for p in group["params"]:
                 if p.grad is None:
```

### Comparing `ml-starter-0.0.36/ml/scripts/cli.py` & `ml-starter-0.0.37/ml/scripts/cli.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,7 +1,49 @@
+"""Main entry point for the CLI.
+
+Whichever package you are using should probably have some sort of CLI entry
+point which calls this function, for example:
+
+.. code-block:: python
+
+    from pathlib import Path
+
+    from ml.scripts.cli import cli_main as ml_cli_main
+
+    PROJECT_ROOT = Path(__file__).parent.parent  # Root relative to CLI file
+
+    def cli_main() -> None:
+        ml_cli_main(PROJECT_ROOT)
+
+    if __name__ == "__main__":
+        cli_main()
+
+You can add this to your ``setup.py`` file as follows:
+
+.. code-block:: python
+
+    setup(
+        ...,
+        entry_points={
+            "console_scripts": [
+                "runml = my_package.cli:cli_main",
+            ],
+        },
+    )
+
+Alternatively, you can add it to your ``setup.cfg`` file as follows:
+
+.. code-block:: ini
+
+    [options.entry_points]
+
+    console_scripts =
+        runml = my_package.cli:cli_main
+"""
+
 import logging
 import shlex
 import sys
 from pathlib import Path
 from typing import TYPE_CHECKING, Callable
 
 from ml.utils.distributed import get_rank_optional, get_world_size_optional
```

### Comparing `ml-starter-0.0.36/ml/scripts/stage.py` & `ml-starter-0.0.37/ml/scripts/stage.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Stages the current configuration."""
+
 import logging
 
 from omegaconf import DictConfig, OmegaConf
 
 from ml.core.env import get_stage_dir
 from ml.core.registry import project_dirs
 from ml.utils.staging import stage_environment
@@ -11,15 +13,14 @@
 
 def stage_main(config: DictConfig) -> None:
     """Stages the current configuration.
 
     Args:
         config: The configuration object.
     """
-
     # Stages the currently-imported files.
     out_dir = stage_environment(project_dirs.paths[1:], get_stage_dir())
     logger.info("Staged environment to %s", out_dir)
 
     # Stages the raw config.
     config_dir = out_dir / "configs"
     config_dir.mkdir(exist_ok=True, parents=True)
```

### Comparing `ml-starter-0.0.36/ml/scripts/train.py` & `ml-starter-0.0.37/ml/scripts/train.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Runs the training script."""
+
 import datetime
 import logging
 from contextlib import contextmanager
 from typing import Iterator
 
 from omegaconf import DictConfig
 
@@ -15,15 +17,14 @@
 
 def train_main(config: DictConfig) -> None:
     """Runs the training loop.
 
     Args:
         config: The configuration object.
     """
-
     with Timer("setting random seed", spinner=True):
         from ml.utils.random import set_random_seed
 
         set_random_seed()
 
     objs = Objects.parse_raw_config(config)
 
@@ -32,15 +33,14 @@
 
 def train_main_with_objects(objs: Objects) -> None:
     """Runs the training loop.
 
     Args:
         objs: The objects to use for training.
     """
-
     # Checks that the config has the right keys for training.
     assert (model := objs.model) is not None
     assert (task := objs.task) is not None
     assert (optimizer := objs.optimizer) is not None
     assert (lr_scheduler := objs.lr_scheduler) is not None
     assert (trainer := objs.trainer) is not None
```

### Comparing `ml-starter-0.0.36/ml/tasks/base.py` & `ml-starter-0.0.37/ml/tasks/base.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,19 @@
 # pylint: disable=too-many-public-methods
+"""Defines the base class and config for all tasks.
+
+Tasks are the main unit of work in the ML framework. They are responsible for
+defining the training, validation, and testing loops, as well as data loading,
+logging, and model evaluation. They also do a lot of timing and logging of
+performance metrics, with some hooks for calling custom code snippets at
+various points. Typically, you should use either the
+:class:`ml.tasks.sl.SupervisedLearningTask` or
+:class:`ml.tasks.rl.ReinforcementLearningTask` classes instead of this base
+class.
+"""
 
 import functools
 import logging
 import time
 from abc import ABC, abstractmethod
 from dataclasses import dataclass, is_dataclass
 from pathlib import Path
@@ -272,15 +283,14 @@
                 tensors. If a dictionary, all loss tensors need to have the
                 same shape.
 
         Returns:
             The single loss with shape (N), where N is the number of losses,
             and the loss names, a list of length N.
         """
-
         if isinstance(loss, Tensor):
             if loss.ndim == 0:
                 return loss.unsqueeze(0), ["loss"]
             if loss.ndim == 1:
                 return loss, ["loss"]
             return reduce(loss, self.__final_loss_reduce_type).unsqueeze(0), ["loss"]
         assert isinstance(loss, dict), f"Loss should be a scalar or dictionary, not {type(loss)}"
@@ -359,15 +369,14 @@
             dataset: The dataset to sample from
             cfg: The associated dataloader config
             phase: The dataset's phase
 
         Raises:
             NotImplementedError: If this method is not overridden
         """
-
         raise NotImplementedError("`get_sampler` should be implemented for the specific task")
 
     def get_batch_sampler(self, sampler: Sampler, cfg: DataLoaderConfig, phase: Phase) -> Sampler[list[int]]:
         """Returns a dataset batch sampler to use instead fo sequential sampling.
 
         The batch sampler should yield lists of integer indices, which
         are the samples that are passed to the dataset.
@@ -376,15 +385,14 @@
             sampler: The underlying sampler
             cfg: The associated dataloader config
             phase: The dataset's phase
 
         Raises:
             NotImplementedError: If this method is not overridden
         """
-
         raise NotImplementedError("`get_sampler` should be implemented for the specific task")
 
     def get_dataloader(self, dataset: Dataset, phase: Phase) -> DataLoader:
         if phase not in self.dataloader_configs:
             raise KeyError(f"Missing {phase=} in dataloader configs")
         cfg = self.dataloader_configs[phase]
 
@@ -413,32 +421,32 @@
             sampler = self.get_sampler(dataset, cfg, phase)
         except NotImplementedError:
             return DataLoader(
                 dataset=dataset,
                 batch_size=cfg.batch_size,
                 drop_last=cfg.drop_last,
                 shuffle=cfg.shuffle if isinstance(dataset, Sized) else False,
-                **common_kwargs,  # type: ignore
+                **common_kwargs,  # type: ignore[arg-type]
             )
 
         try:
             batch_sampler = self.get_batch_sampler(sampler, cfg, phase)
         except NotImplementedError:
             return DataLoader(
                 dataset=dataset,
                 sampler=sampler,
                 batch_size=cfg.batch_size,
                 drop_last=cfg.drop_last,
-                **common_kwargs,  # type: ignore
+                **common_kwargs,  # type: ignore[arg-type]
             )
 
         return DataLoader(
             dataset=dataset,
             batch_sampler=batch_sampler,
-            **common_kwargs,  # type: ignore
+            **common_kwargs,  # type: ignore[arg-type]
         )
 
     @classmethod
     def worker_init_fn(cls, worker_id: int) -> None:
         set_random_seed(offset=worker_id)
 
     @classmethod
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/async_iterable.py` & `ml-starter-0.0.37/ml/tasks/datasets/async_iterable.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,7 +1,25 @@
+"""Defines a dataset for asynchronous iteration.
+
+This dataclass is useful when you are trying to use Python's ``async`` /
+``await`` syntax to iterate over a dataset. This just starts a separate thread
+that runs the async iterator and puts the results into a queue, which is then
+used to iterate over the dataset.
+
+Example::
+
+    class MyDataset(AsyncIterableDataset):
+        async def __aiter__(self) -> AsyncIterator[T]:
+            for i in range(10):
+                yield i
+
+    for i in MyDataset():
+        print(i)
+"""
+
 import asyncio
 import logging
 import queue
 import threading
 from typing import AsyncIterator, Iterator, TypeVar
 
 from torch.utils.data.dataset import IterableDataset
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/clippify.py` & `ml-starter-0.0.37/ml/tasks/datasets/clippify.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a dataset for converting frame streams to clips."""
+
 import logging
 import random
 from collections import deque
 from typing import Deque, Generic, Iterator, TypeVar
 
 import torch
 from torch import Tensor
@@ -40,15 +42,14 @@
             num_images: The number of images in each clip
             stride: The stride between adjacent images
             jump_size: How many frames to jump in the future
             sample_first: If set, don't always start on the first item; instead,
                 sample the first item within `jump_size`
             use_last: If set, always use the last item in the dataset
         """
-
         super().__init__()
 
         self.image_dataset = image_dataset
         self.num_images = num_images
         self.stride = stride
         self.jump_size = jump_size
         self.sample_first = sample_first
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/collate.py` & `ml-starter-0.0.37/ml/tasks/datasets/collate.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines custom collation functions for PyTorch datasets."""
+
 from dataclasses import is_dataclass
 from typing import Any, Callable, Literal
 
 import numpy as np
 import torch
 import torchvision.transforms.functional as V
 from PIL.Image import Image as PILImage
@@ -36,15 +38,14 @@
 
     Returns:
         The padded or truncated tensors
 
     Raises:
         ValueError: If the tensor dimensions are invalid
     """
-
     if not tensors:
         return tensors
 
     num_dims = tensors[0].dim()
     if num_dims == 0:
         raise ValueError("Tensor dimensions must be greater than zero")
     if not all(t.dim() == num_dims for t in tensors):
@@ -86,15 +87,14 @@
         left_truncate: If set, truncate on the left side, otherwise truncate
             on the right side
         pad_value: The padding value to use
 
     Returns:
         The padded tensors
     """
-
     if not tensors:
         return tensors
 
     # Gets the tensor dimension.
     all_dims = set(t.dim() for t in tensors)
     assert len(all_dims) == 1, f"Got different numbers of tensor dimensions: {all_dims}"
     dims = list(all_dims)[0]
@@ -131,15 +131,14 @@
 
     Returns:
         The collated item, or None if the item list was empty
 
     Raises:
         NotImplementedError: If the mode is invalid
     """
-
     if len(items) == 0:
         return None
     item = items[0]
 
     # Any None items should be filtered out.
     if item is None:
         return None
@@ -186,15 +185,15 @@
 
     # Collate lists and tuples if they have the same lengths.
     if isinstance(item, (list, tuple)) and all(len(i) == len(item) for i in items):
         output_list = []
         for j in range(len(item)):
             output_list.append(collate([i[j] for i in items], mode=mode, pad=pad))
         if is_named_tuple(item):
-            return type(item)(*output_list)  # type: ignore
+            return type(item)(*output_list)  # type: ignore[arg-type]
         if isinstance(item, tuple):
             return tuple(output_list)
         return output_list
 
     # Handles dataclasses.
     if is_dataclass(item):
         output_dict = {}
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/error_handling.py` & `ml-starter-0.0.37/ml/tasks/datasets/error_handling.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines error handling wrappers for datasets.
+
+The worst feeling in the world is when you're training a model and it crashes
+after 10 hours of training. This module defines some error handling wrappers
+for datasets which will catch errors and log them (in batches).
+"""
+
 import bdb
 import logging
 import random
 import sys
 import time
 from collections import Counter
 from dataclasses import dataclass
@@ -235,13 +242,12 @@
 
     Returns:
         The wrapped dataset, which catches some errors
 
     Raises:
         NotImplementedError: If the dataset type is not supported
     """
-
     if isinstance(dataset, IterableDataset):
         return ErrorHandlingIterableDataset(dataset, config)
     elif isinstance(dataset, Dataset):
         return ErrorHandlingDataset(dataset, config)
     raise NotImplementedError(f"Unexpected type: {dataset}")
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/multi_iter.py` & `ml-starter-0.0.37/ml/tasks/datasets/multi_iter.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,7 +1,16 @@
+"""Defines a dataset for iterating from multiple sub-datasets.
+
+It's often the case that you want to write a dataset for iterating from a
+single sample, then combine all those datasets into one mega-dataset for
+iterating from all the samples. This dataset serves that purpose by, at each
+iteration, randomly choosing a dataset and getting it's next sample, until
+all samples in all datasets have been exhausted.
+"""
+
 import random
 from dataclasses import dataclass
 from typing import Generic, Iterable, Iterator, TypeVar
 
 import numpy as np
 from torch.utils.data.dataset import IterableDataset
 
@@ -22,15 +31,16 @@
         until_all_empty: bool = False,
         iterate_forever: bool = False,
     ) -> None:
         """Defines a dataset for iterating from multiple iterable datasets.
 
         Args:
             datasets: The information about the datasets to iterate from and
-                how to iterate them; specifically,
+                how to iterate them; specifically, the sampling rate of each
+                dataset.
             until_all_empty: If set, iterates until all datasets are empty,
                 otherwise only iterate until any dataset is empty
             iterate_forever: If set, iterate child dataset forever
         """
         super().__init__()
 
         self.datasets = list(datasets)
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/samplers.py` & `ml-starter-0.0.37/ml/tasks/datasets/samplers.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Custom samplers for datasets."""
+
 import random
 from typing import Iterator, Sized
 
 from torch.utils.data.sampler import Sampler
 
 
 class ChunkSampler(Sampler[int]):
@@ -16,15 +18,14 @@
         yields the desired behavior.
 
         Args:
             dataset: The dataset to sample from
             batch_size: The size of each chunk
             shuffle: Yield chunks in random order or from first to last
         """
-
         super().__init__(dataset)
 
         self.dataset = dataset
         self.batch_size = batch_size
         self.shuffle = shuffle
         self.num_samples = len(dataset)
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/streaming.py` & `ml-starter-0.0.37/ml/tasks/datasets/streaming.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,45 +1,54 @@
+"""Defines a dataset which combines many streaming datasets.
+
+This dataset takes a set of child iterable datasets and iterates from
+them infinitely. When a child dataset is exhausted, it is returned to
+the reservoir and restarted, while another dataset is chosen.
+"""
+
 import logging
 import random
 from typing import Collection, Generic, Iterator, TypeVar
 
 from torch.utils.data.dataset import IterableDataset
 
 from ml.utils.data import get_worker_info
 
 logger: logging.Logger = logging.getLogger(__name__)
 
 Batch = TypeVar("Batch")
 
 
 class StreamingDataset(IterableDataset[tuple[int, Batch]], Generic[Batch]):
-    def __init__(self, datasets: Collection[IterableDataset[Batch]], max_simultaneous: int) -> None:
-        """Defines a dataset which combines many streaming datasets.
+    """Defines a dataset which combines many streaming datasets.
+
+    This dataset takes a set of child iterable datasets and iterates from
+    them infinitely. When a child dataset is exhausted, it is returned to
+    the reservoir and restarted, while another dataset is chosen.
+
+    An example usage for this dataset is to get samples from many videos,
+    where each sub-dataset yields video samples. This way the child dataset
+    can be used to run inference on a single video, while the parent
+    streaming dataset can be used to train on a mixture of videos. The
+    child dataset can then be optimized to make video loading times fast.
+    """
 
-        This dataset takes a set of child iterable datasets and iterates from
-        them infinitely. When a child dataset is exhausted, it is returned to
-        the reservoir and restarted, while another dataset is chosen.
-
-        An example usage for this dataset is to get samples from many videos,
-        where each sub-dataset yields video samples. This way the child dataset
-        can be used to run inference on a single video, while the parent
-        streaming dataset can be used to train on a mixture of videos. The
-        child dataset can then be optimized to make video loading times fast.
+    def __init__(self, datasets: Collection[IterableDataset[Batch]], max_simultaneous: int) -> None:
+        """Initializes a new streaming dataset.
 
         Args:
             datasets: The sub-datasets to iterate from
             max_simultaneous: The maximum number of simultaneous datasets to
                 iterate from. Increasing this number increases the dataset
                 diversity but also increases memory usage as samples need to be
                 stored in memory
 
         Raises:
             ValueError: If no datasets are provided
         """
-
         super().__init__()
 
         if len(datasets) == 0:
             raise ValueError("Must provide at least one dataset")
 
         self.datasets = list(datasets)
         self.max_simultaneous = max_simultaneous
@@ -104,9 +113,15 @@
             except StopIteration:
                 logger.debug("Finished one iteration for dataset %d", dataset_id)
                 self.return_dataset(reservoir_id)
         return dataset_id, sample
 
 
 class StreamingDatasetNoIndex(StreamingDataset[Batch], IterableDataset[tuple[int, Batch]], Generic[Batch]):
+    """Defines a streaming dataset which only yields the batch.
+
+    This dataset is identical to the StreamingDataset, except that it
+    cuts off the dataset index and only yields the batch.
+    """
+
     def __next__(self) -> Batch:  # type: ignore[override]
         return super().__next__()[1]
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/transforms.py` & `ml-starter-0.0.37/ml/tasks/datasets/transforms.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a bunch of dataset transforms."""
+
 import random
 from typing import TypeVar
 
 import torch
 import torchvision.transforms.functional as V
 from PIL.Image import Image as PILImage
 from torch import Tensor, nn
@@ -13,75 +15,123 @@
 
 # Default image normalization parameters.
 MEAN: NormParams = 0.48145466, 0.4578275, 0.40821073
 STD: NormParams = 0.26862954, 0.26130258, 0.27577711
 
 
 def square_crop(img: Image) -> Image:
+    """Crops an image to a square.
+
+    Args:
+        img: The input image
+
+    Returns:
+        The cropped image, with height and width equal.
+    """
     img_width, img_height = V.get_image_size(img)
     height = width = min(img_height, img_width)
     top, left = (img_height - height) // 2, (img_width - width) // 2
     return V.crop(img, top, left, height, width)
 
 
 def square_resize_crop(img: Image, size: int, interpolation: InterpolationMode = InterpolationMode.NEAREST) -> Image:
+    """Resizes an image to a square and then crops it.
+
+    Args:
+        img: The input image
+        size: The size of the square
+        interpolation: The interpolation mode to use
+
+    Returns:
+        The cropped image
+    """
     img_width, img_height = V.get_image_size(img)
     min_dim = min(img_width, img_height)
     height, width = int((img_width / min_dim) * size), int((img_height / min_dim) * size)
     img = V.resize(img, [height, width], interpolation)
     top, left = (height - size) // 2, (width - size) // 2
     return V.crop(img, top, left, size, size)
 
 
 def upper_left_crop(img: Image, height: int, width: int) -> Image:
-    return V.crop(img, 0, 0, height, width)
+    """Crops an image from the upper left corner.
 
+    This is useful because it preserves camera intrinsics for an image.
 
-def rescale(x: Image, scale: float, min_val: float, do_checks: bool = False) -> Image:
-    assert isinstance(x, Tensor), "Rescale must operate on a tensor"
-    assert x.dtype.is_floating_point, "Rescale got non-floating point input tensor"
-    if do_checks:
-        min_val, max_val = x.min().item(), x.max().item()
-        assert min_val >= 0 and max_val <= 1, "Rescale input has values outside [0, 1]"
-    return x * scale + min_val
-
+    Args:
+        img: The input image
+        height: The height of the crop
+        width: The width of the crop
 
-def convert_image_to_rgb(image: PILImage) -> PILImage:
-    return image.convert("RGB")
+    Returns:
+        The cropped image
+    """
+    return V.crop(img, 0, 0, height, width)
 
 
 def normalize(t: Tensor, *, mean: NormParams = MEAN, std: NormParams = STD) -> Tensor:
+    """Normalizes an image tensor (by default, using ImageNet parameters).
+
+    This can be paired with :func:`denormalize` to convert an image tensor
+    to a normalized tensor for processing by a model.
+
+    Args:
+        t: The input tensor
+        mean: The mean to subtract
+        std: The standard deviation to divide by
+
+    Returns:
+        The normalized tensor
+    """
     return V.normalize(t, mean, std)
 
 
 def denormalize(t: Tensor, *, mean: NormParams = MEAN, std: NormParams = STD) -> Tensor:
+    """Denormalizes a tensor.
+
+    This can be paired with :func:`normalize` to convert a normalized tensor
+    back to the original image for viewing by humans.
+
+    Args:
+        t: The input tensor
+        mean: The mean to subtract
+        std: The standard deviation to divide by
+
+    Returns:
+        The denormalized tensor
+    """
     mean_tensor = torch.tensor(mean, device=t.device, dtype=t.dtype)
     std_tensor = torch.tensor(std, device=t.device, dtype=t.dtype)
     return (t * std_tensor[None, :, None, None]) + mean_tensor[None, :, None, None]
 
 
-def normalize_shape(t: Tensor) -> Tensor:
-    dims = t.shape[0]
-    if dims == 3:
-        return t
-    if dims == 1:
-        return t.repeat_interleave(3, dim=0)
-    if dims > 3:
-        return t[:3]
-    raise NotImplementedError(dims)
+def random_square_crop(img: Image) -> Image:
+    """Randomly crops an image to a square.
 
+    Args:
+        img: The input image
 
-def random_square_crop(img: Image) -> Image:
+    Returns:
+        The cropped image
+    """
     img_width, img_height = V.get_image_size(img)
     height = width = min(img_height, img_width)
     top, left = random.randint(0, img_height - height), random.randint(0, img_width - width)
     return V.crop(img, top, left, height, width)
 
 
 def random_square_crop_multi(imgs: list[Image]) -> list[Image]:
+    """Randomly crops a list of images to the same size.
+
+    Args:
+        imgs: The list of images to crop
+
+    Returns:
+        The cropped images
+    """
     img_dims = V.get_image_size(imgs[0])
     assert all(V.get_image_size(i) == img_dims for i in imgs[1:])
     img_width, img_height = img_dims
     height = width = min(img_width, img_height)
     top, left = random.randint(0, img_height - height), random.randint(0, img_width - width)
     return [V.crop(i, top, left, height, width) for i in imgs]
 
@@ -92,15 +142,14 @@
     Args:
         img: The input image
         ref_size: The reference size, as (width, height)
 
     Returns:
         The resized image
     """
-
     img_c, (img_w, img_h), (ref_w, ref_h) = V.get_image_num_channels(img), V.get_image_size(img), ref_size
     if img_h / img_w < ref_h / ref_w:  # Pad width
         new_h, new_w = (img_h * ref_w) // img_w, ref_w
     else:
         new_h, new_w = ref_h, (img_w * ref_h) // img_h
     img = V.resize(img, [new_h, new_w], InterpolationMode.BILINEAR)
     new_img = img.new_zeros(img_c, ref_h, ref_w)
@@ -116,75 +165,56 @@
         img: The input image
         ref_img: The reference image
 
     Returns:
         The input image resized to the same size as the reference image,
             zero-padding dimensions which are too small
     """
-
     ref_w, ref_h = V.get_image_size(ref_img)
     return make_size(img, (ref_w, ref_h))
 
 
 class SquareResizeCrop(nn.Module):
+    """Resizes and crops an image to a square with the target shape.
+
+    Generally SquareCrop followed by a resize should be preferred when using
+    bilinear resize, as it is faster to do the interpolation on the smaller
+    image. However, nearest neighbor resize on the larger image followed by
+    a crop on the smaller image can sometimes be faster.
+    """
+
     __constants__ = ["size", "interpolation"]
 
     def __init__(self, size: int, interpolation: InterpolationMode = InterpolationMode.NEAREST) -> None:
-        """Resizes and crops an image to a square with the target shape.
-
-        Generally SquareCrop followed by a resize should be preferred when using
-        bilinear resize, as it is faster to do the interpolation on the smaller
-        image. However, nearest neighbor resize on the larger image followed by
-        a crop on the smaller image can sometimes be faster.
+        """Initializes the square resize crop.
 
         Args:
             size: The square height and width to resize to
             interpolation: The interpolation type to use when resizing
         """
-
         super().__init__()
 
         self.size = int(size)
         self.interpolation = InterpolationMode(interpolation)
 
     def forward(self, img: Image) -> Image:
         return square_resize_crop(img, self.size, self.interpolation)
 
 
 class UpperLeftCrop(nn.Module):
+    """Crops image from upper left corner, to preserve image intrinsics."""
+
     __constants__ = ["height", "width"]
 
     def __init__(self, height: int, width: int) -> None:
-        """Crops image from upper left corner, to preserve image intrinsics.
+        """Initializes the upper left crop.
 
         Args:
             height: The max height of the cropped image
             width: The max width of the cropped image
         """
-
         super().__init__()
 
         self.height, self.width = height, width
 
     def forward(self, img: Image) -> Image:
         return upper_left_crop(img, self.height, self.width)
-
-
-class RescaleImage(nn.Module):
-    __constants__ = ["min_val", "scale", "do_checks"]
-
-    def __init__(self, min_val: float, max_val: float, do_checks: bool = True) -> None:
-        """Rescales an image from (0, 1) to some other scale.
-
-        Args:
-            min_val: The scale if `max_val` is None, otherwise the min value
-            max_val: The maximum value
-            do_checks: If set, check the input tensor ranges (can disable for
-                more efficient image loading)
-        """
-
-        super().__init__()
-
-        self.min_val, self.scale, self.do_checks = min_val, max_val - min_val, do_checks
-
-    def forward(self, x: Image) -> Image:
-        return rescale(x, self.min_val, self.scale, self.do_checks)
```

### Comparing `ml-starter-0.0.36/ml/tasks/datasets/video_file.py` & `ml-starter-0.0.37/ml/tasks/datasets/video_file.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a dataset which iterates through frames in a video file."""
+
 from pathlib import Path
 from typing import Callable, Iterator
 
 import numpy as np
 from torch import Tensor
 from torch.utils.data.dataset import IterableDataset
 
@@ -19,27 +21,26 @@
         """Defines a dataset which iterates through frames in a video file.
 
         Args:
             file_path: The path to the video file to iterate through
             reader: The video reader to use
             transform: An optional transform to apply to each frame
         """
-
         super().__init__()
 
         self.file_path = str(file_path)
         self.reader = reader
         self.transform = transform
 
     video_props: VideoProps
     video_stream: Iterator[np.ndarray | Tensor]
 
     def __iter__(self) -> Iterator[Tensor]:
         self.video_props = VideoProps.from_file_ffmpeg(self.file_path)
-        self.video_stream = read_video(self.reader, self.file_path)
+        self.video_stream = read_video(self.file_path, reader=self.reader)
         return self
 
     def __next__(self) -> Tensor:
         buffer = next(self.video_stream)
         image = as_cpu_tensor(buffer).permute(2, 0, 1)  # HWC -> CHW
         if self.transform is not None:
             image = self.transform(image)
```

### Comparing `ml-starter-0.0.36/ml/tasks/environments/base.py` & `ml-starter-0.0.37/ml/tasks/environments/base.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.36/ml/tasks/environments/worker.py` & `ml-starter-0.0.37/ml/tasks/environments/worker.py`

 * *Files 0% similar despite different names*

```diff
@@ -85,15 +85,14 @@
     def __init__(self, env: "Environment[RLState, RLAction]", seed: int = 1337) -> None:
         """Defines a synchronous environment worker.
 
         Args:
             env: The environment to wrap.
             seed: The random seed to use.
         """
-
         super().__init__()
 
         self.env = env
         self.seed = seed
 
         self.state: RLState | SpecialState | None = None
 
@@ -151,15 +150,14 @@
             cleanup_time: The time to wait for the worker to finish before killing it.
             mode: The mode to use for the worker.
             daemon: Whether to run the worker as a daemon.
 
         Raises:
             ValueError: If the mode is invalid.
         """
-
         super().__init__()
 
         self.cleanup_time = cleanup_time
         self.rank = 0 if rank is None else rank
         self.world_size = 1 if world_size is None else world_size
 
         self.action_queue: "Queue[RLAction | SpecialAction]" = manager.Queue(maxsize=1)
```

### Comparing `ml-starter-0.0.36/ml/tasks/rl/base.py` & `ml-starter-0.0.37/ml/tasks/rl/base.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,30 @@
+"""The base task and config for reinforcement learning tasks.
+
+This class expects you to implement the following functions:
+
+.. code-block:: python
+
+    class MyReinforcementLearningTask(ml.ReinforcementLearning[Config, Model, State, Action, Output, Loss]):
+        def get_actions(self, model: Model, states: list[State], optimal: bool) -> list[Action]:
+            ...
+
+        def get_environment(self) -> Environment:
+            ...
+
+        def run_model(self, model: Model, batch: tuple[State, Action], state: ml.State) -> Output:
+            ...
+
+        def compute_loss(self, model: Model, batch: tuple[State, Action], state: ml.State, output: Output) -> Loss:
+            ...
+
+Additionally, you can implement :meth:`postprocess_trajectory` and :meth:`postprocess_trajectories` to apply some
+postprocessing to collected batches, such as computing the discounted rewards.
+"""
+
 import functools
 import logging
 import multiprocessing as mp
 import time
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
 from pathlib import Path
@@ -132,30 +155,28 @@
 
         Args:
             samples: The trajectory to postprocess.
 
         Returns:
             The postprocessed trajectory.
         """
-
         return samples
 
     def postprocess_trajectories(
         self,
         trajectories: list[list[tuple[RLState, RLAction]]],
     ) -> list[list[tuple[RLState, RLAction]]]:
         """Performs any global postprocessing on all of the trajectories.
 
         Args:
             trajectories: The trajectories to postprocess.
 
         Returns:
             The postprocessed trajectories.
         """
-
         return trajectories
 
     def iter_samples(
         self,
         model: ModelT,
         worker_pool: WorkerPool[RLState, RLAction],
         *,
@@ -188,15 +209,14 @@
 
         Yields:
             Lists of samples from the environment.
 
         Raises:
             ValueError: If `min_batch_size` is greater than `max_batch_size`.
         """
-
         min_trajectory_length = max(min_trajectory_length, self.config.dataset.num_samples, 1)
         num_samples, num_trajectories = 0, 0
 
         worker_pool.reset()
         trajectories: list[list[tuple[RLState, RLAction]]] = [[] for _ in range(len(worker_pool))]
         max_batch_size = len(worker_pool) if max_batch_size is None else min(max_batch_size, len(worker_pool))
 
@@ -390,15 +410,14 @@
         Returns:
             The sampled clip, if `save_path` is not provided, otherwise `None`
             (the clip is saved to `save_path`).
 
         Raises:
             ValueError: If `save_path` is provided and `return_states` is `True`
         """
-
         env_cfg = self.config.environment
 
         if not return_states and not return_images:
             raise ValueError("Must return states, images or both")
 
         environment = self.get_environment_cached()
```

### Comparing `ml-starter-0.0.36/ml/tasks/rl/replay.py` & `ml-starter-0.0.37/ml/tasks/rl/replay.py`

 * *Files 1% similar despite different names*

```diff
@@ -71,15 +71,15 @@
 
 class ReplayDataset(IterableDataset[T], Generic[T]):
     def __init__(
         self,
         buffer: MultiReplaySamples[T],
         clip_size: int,
         stride: int = 1,
-        collate_fn: Callable[[list[T]], T] = collate,  # type: ignore
+        collate_fn: Callable[[list[T]], T] = collate,  # type: ignore[assignment]
     ) -> None:
         super().__init__()
 
         self.buffer = buffer
         self._buffer_partitioned: MultiReplaySamples[T] | None = None
         self.clip_size = clip_size
         self.stride = stride
```

### Comparing `ml-starter-0.0.36/ml/tasks/sl/base.py` & `ml-starter-0.0.37/ml/tasks/sl/base.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,23 @@
-# pylint: disable=too-many-public-methods
+"""Defines the base supervised learning task type.
+
+This class expects you to implement the following functions:
+
+.. code-block:: python
+
+    class MySupervisedLearningTask(ml.ReinforcementLearning[Config, Model, Batch, Output, Loss]):
+        def run_model(self, model: Model, batch: Batch, state: ml.State) -> Output:
+            ...
+
+        def compute_loss(self, model: Model, batch: Batch, state: ml.State, output: Output) -> Loss:
+            ...
+
+        def get_dataset(self, phase: ml.Phase) -> Dataset:
+            ...
+"""
 
 import logging
 from abc import ABC
 from dataclasses import dataclass
 from typing import Generic, TypeVar
 
 from torch.utils.data.dataset import Dataset
@@ -32,13 +47,9 @@
     """Defines the base task type."""
 
     def get_dataset(self, phase: Phase) -> Dataset:
         """Returns the dataset for a given phase.
 
         Args:
             phase: The dataset phase to get
-
-        Raises:
-            NotImplementedError: If this method is not overridden
         """
-
         raise NotImplementedError("`get_dataset` should be implemented by the task")
```

### Comparing `ml-starter-0.0.36/ml/trainers/base.py` & `ml-starter-0.0.37/ml/trainers/base.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+"""Defines the base trainer class and config.
+
+The trainer is the thing that actually runs the training loop. There are
+separate trainers for supervised and reinforcement learning since the latter
+requires interacting with an environment, so you use the appropriate trainer
+for your task (they are defined in :mod:`ml.trainers.sl` and
+:mod:`ml.trainers.rl` respectively). The base trainer handles things like
+setting up the experiment directory, saving checkpoints, and logging.
+"""
+
 import enum
 import functools
 import logging
 import os
 import signal
 from dataclasses import asdict, dataclass
 from pathlib import Path
@@ -58,17 +68,16 @@
 
 
 def remove_lock_file(exp_dir: Path, lock_type: LockType, *, missing_ok: bool = False) -> None:
     if is_master():
         if (lock_file := exp_dir / f".lock_{lock_type}").exists():
             lock_file.unlink()
             logger.debug("Removed %s lock file from experiment directory %s", lock_type, exp_dir)
-        else:
-            if not missing_ok:
-                raise RuntimeError(f"Lock file not found at {lock_file}")
+        elif not missing_ok:
+            raise RuntimeError(f"Lock file not found at {lock_file}")
 
 
 def has_lock_file(exp_dir: Path, lock_type: LockType | None = None) -> bool:
     if lock_type is not None:
         return (exp_dir / f".lock_{lock_type}").exists()
     return any((exp_dir / f".lock_{lock_type_arg}").exists() for lock_type_arg in get_args(LockType))
 
@@ -79,15 +88,14 @@
     Args:
         exp_dir: The experiment directory
         state: The current trainer state
 
     Returns:
         The path to the PyTorch checkpoint to save or load
     """
-
     if state is None:
         return exp_dir / "checkpoints" / "ckpt.pt"
     return exp_dir / "checkpoints" / f"ckpt.{state.num_steps}.pt"
 
 
 def get_exp_dir(base_run_dir: Path, exp_name: str, run_id: int) -> Path:
     return (base_run_dir / exp_name / f"run_{run_id}").resolve()
@@ -99,15 +107,14 @@
     Args:
         base_run_dir: The base run directory for the entire experiment
         exp_name: The name of the experiment
 
     Returns:
         A run ID for an experiment directory without a lockfile
     """
-
     # If the run ID isn't specified, look at all run IDs until there is one
     # which either doesn't exist or doesn't have a checkpoint directory.
     run_id = 0
     while (exp_dir := get_exp_dir(base_run_dir, exp_name, run_id)).is_dir() and has_lock_file(exp_dir):
         run_id += 1
 
     return run_id
@@ -326,15 +333,14 @@
 
         Returns:
             The state loaded from the checkpoint.
 
         Raises:
             UnpicklingError: If there is some issue unpickling the checkpoint.
         """
-
         with Timer("loading checkpoint", spinner=True):
             if isinstance(ckpt, (str, Path)):
                 try:
                     ckpt = cast(dict, torch.load(ckpt, weights_only=weights_only))
                 except UnpicklingError:
                     if weights_only:
                         logger.warning("Failed to load checkpoint using `weights_only` flag, retrying without it")
@@ -413,15 +419,14 @@
             task: The current task
             optimizer: The current optimizer
             lr_scheduler: The current learning rate scheduler
 
         Raises:
             NotImplementedError: If the subclass does not implement this method
         """
-
         raise NotImplementedError
 
     def write_logs(self, task: TaskT, model: ModelT, state: State) -> None:
         model.logger.write(self.loggers, state)
         task.logger.write(self.loggers, state)
         self.logger.write(self.loggers, state)
         for value_logger in self.loggers:
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/cpu_stats.py` & `ml-starter-0.0.37/ml/trainers/mixins/cpu_stats.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""A trainer mixin for logging CPU statistics.
+
+This logs memory and CPU utilization in a background process, sending it to
+the logging process every now and then. This is useful for detecting memory
+leaks in your dataloader, among other issues.
+"""
+
 import logging
 import multiprocessing as mp
 import os
 import time
 from ctypes import Structure, c_double, c_uint16, c_uint64
 from dataclasses import dataclass
 from multiprocessing.managers import SyncManager, ValueProxy
@@ -81,15 +88,17 @@
     pid: int,
 ) -> None:
     start_event.set()
 
     proc, cur_pid = psutil.Process(pid), os.getpid()
     logger.debug("Starting CPU stats monitor for PID %d with PID %d", pid, cur_pid)
 
-    get_children = lambda: {p.pid: p for p in proc.children(recursive=True) if p.pid != cur_pid}
+    def get_children() -> dict[int, psutil.Process]:
+        return {p.pid: p for p in proc.children(recursive=True) if p.pid != cur_pid}
+
     child_procs = get_children()
 
     while True:
         try:
             # Updates child processes, preserving the previous child process
             # object. Otherwise the CPU percentage will be zero.
             new_procs = get_children()
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/gpu_stats.py` & `ml-starter-0.0.37/ml/trainers/mixins/gpu_stats.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""A trainer mixin for logging GPU statistics.
+
+This logs GPU memory and utilization in a background process using
+``nvidia-smi``, if a GPU is available in the system.
+"""
+
 import functools
 import logging
 import multiprocessing as mp
 import os
 import re
 import shutil
 import subprocess
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/heartbeat.py` & `ml-starter-0.0.37/ml/trainers/mixins/heartbeat.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""A simple mixin for monitoring if the main training job is still alive.
+
+If this mixin detects that the training job has died then it will kill the
+current process.
+"""
+
 import logging
 import multiprocessing as mp
 import os
 import time
 from dataclasses import dataclass
 from multiprocessing.managers import SyncManager
 from multiprocessing.synchronize import Event
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/mixed_precision.py` & `ml-starter-0.0.37/ml/trainers/mixins/mixed_precision.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,7 +1,16 @@
+"""Defines a mixin for doing FP16 scaling.
+
+FP16 scaling is a technique for training with FP16 precision while maintaining
+FP32 precision for the model weights. This is done by scaling the loss by a
+large factor (e.g. 2^16) and then scaling the gradients by the inverse of that
+factor. So if the scale factor starts to decrease, it means that the loss is
+overflowing and training is diverging.
+"""
+
 from dataclasses import dataclass
 from typing import Any, ContextManager, TypeVar
 
 import torch
 from torch import Tensor
 from torch.optim import Optimizer
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/monitor_process.py` & `ml-starter-0.0.37/ml/trainers/mixins/monitor_process.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a base trainer mixin for handling subprocess monitoring jobs."""
+
 import logging
 import multiprocessing as mp
 from dataclasses import dataclass
 from typing import Generic, TypeVar
 
 from torch.optim.optimizer import Optimizer
 
@@ -20,15 +22,15 @@
 MonitorProcessConfigT = TypeVar("MonitorProcessConfigT", bound=MonitorProcessConfig)
 
 
 class MonitorProcessMixin(
     BaseTrainer[MonitorProcessConfigT, ModelT, TaskT],
     Generic[MonitorProcessConfigT, ModelT, TaskT],
 ):
-    """Defines a trainer mixin for getting CPU statistics."""
+    """Defines a base trainer mixin for handling monitoring processes."""
 
     def __init__(self, config: MonitorProcessConfigT) -> None:
         super().__init__(config)
 
         self._mp_manager = mp.Manager()
 
     def on_training_end(
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/profiler.py` & `ml-starter-0.0.37/ml/trainers/mixins/profiler.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines a trainer mixin for profiling PyTorch models.
+
+This can be enabled by setting ``trainer.profiler.enabled=true`` in your
+configuration file. It will run the first few steps of training with the
+profiler enabled, and then log a report of the results to the log directory.
+"""
+
 import contextlib
 import datetime
 import logging
 import time
 from dataclasses import dataclass
 from typing import Any, ContextManager, Iterator, TypeVar
```

### Comparing `ml-starter-0.0.36/ml/trainers/mixins/step_wrapper.py` & `ml-starter-0.0.37/ml/trainers/mixins/step_wrapper.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+"""Defines a mixin to wrap some steps in a context manager.
+
+This is used by other components which want to know when a step is being
+run, such as when doing profiling.
+"""
+
 from abc import ABC
 from types import TracebackType
 from typing import ContextManager, Literal, TypeVar
 
 from ml.trainers.base import BaseTrainer, BaseTrainerConfig, ModelT, TaskT
 
 StepType = Literal[
```

### Comparing `ml-starter-0.0.36/ml/trainers/rl.py` & `ml-starter-0.0.37/ml/trainers/rl.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 
 from ml.core.config import conf_field
 from ml.core.registry import register_trainer
 from ml.lr_schedulers.base import BaseLRScheduler
 from ml.optimizers.base import BaseOptimizer
 from ml.tasks.rl.base import ReinforcementLearningTask
 from ml.trainers.base import ModelT
-from ml.trainers.vanilla import TrainingFinishedException, VanillaTrainer, VanillaTrainerConfig
+from ml.trainers.vanilla import TrainingFinishedError, VanillaTrainer, VanillaTrainerConfig
 from ml.utils.timer import Timer
 
 logger = logging.getLogger(__name__)
 
 
 @dataclass
 class SamplingConfig:
@@ -70,31 +70,30 @@
             task: The current task
             optimizer: The current optimizer
             lr_scheduler: The current learning rate scheduler
 
         Raises:
             ValueError: If the task is not a reinforcement learning task
         """
-
         if not isinstance(task, ReinforcementLearningTask):
             raise ValueError(f"Expected task to be a ReinforcementLearningTask, got {type(task)}")
 
         self._init_environment()
         model = self._compile_model(model)
-        task_model = self.get_task_model(task, model)
+        task_model = self._get_task_model(task, model)
         optim, lr_sched = self._get_optim_and_lr_sched(model, optimizer, lr_scheduler)
         state = self._get_state(task, model, optim, lr_sched)
 
         def on_exit(signum: int, _: FrameType | None) -> None:
             sig = signal.Signals(signum)
             self.on_exit(sig, state, task, model, optim, lr_sched)
 
         def on_finish_training() -> None:
             self.save_checkpoint(state, task, model, optim, lr_sched)
-            raise TrainingFinishedException
+            raise TrainingFinishedError
 
         # Handle user-defined interrupts.
         signal.signal(signal.SIGUSR1, on_exit)
 
         # Gets the environment workers.
         worker_pool = task.get_worker_pool(force_sync=self.config.sampling.force_sync)
 
@@ -166,15 +165,15 @@
                             break
 
                     with self.step_context("on_epoch_end"):
                         self.on_epoch_end(state, task, model, optim, lr_sched)
 
                     state.num_epochs += 1
 
-        except TrainingFinishedException:
+        except TrainingFinishedError:
             logger.info(
                 "Finished training after %d epochs, %d steps, %d samples",
                 state.num_epochs,
                 state.num_steps,
                 state.num_samples,
             )
```

### Comparing `ml-starter-0.0.36/ml/trainers/sl.py` & `ml-starter-0.0.37/ml/trainers/sl.py`

 * *Files 3% similar despite different names*

```diff
@@ -21,22 +21,22 @@
 from ml.core.config import conf_field
 from ml.core.registry import register_trainer
 from ml.core.state import State
 from ml.lr_schedulers.base import BaseLRScheduler
 from ml.optimizers.base import BaseOptimizer
 from ml.tasks.sl.base import SupervisedLearningTask
 from ml.trainers.base import ModelT
-from ml.trainers.vanilla import TrainingFinishedException, VanillaTrainer, VanillaTrainerConfig
+from ml.trainers.vanilla import TrainingFinishedError, VanillaTrainer, VanillaTrainerConfig
 from ml.utils.device.base import InfinitePrefetcher
 from ml.utils.timer import Timer
 
 logger: logging.Logger = logging.getLogger(__name__)
 
 
-class EpochDoneException(Exception):
+class EpochDoneError(Exception):
     """Raised when an epoch is done."""
 
 
 @dataclass
 class ValidationConfig:
     valid_every_n_steps: int | None = conf_field(100, help="Number of training steps to run per test step")
     num_init_valid_steps: int | None = conf_field(1, help="Number of initial validation steps")
@@ -98,35 +98,34 @@
             task: The current task
             optimizer: The current optimizer
             lr_scheduler: The current learning rate scheduler
 
         Raises:
             ValueError: If the task is not a supervised learning task
         """
-
         if not isinstance(task, SupervisedLearningTask):
             raise ValueError(f"Expected task to be a SupervisedLearningTask, got {type(task)}")
 
         self._init_environment()
         model = self._compile_model(model)
 
         with Timer("building task model", spinner=True):
-            task_model = self.get_task_model(task, model)
+            task_model = self._get_task_model(task, model)
             self.maybe_add_grad_clipping(task_model)
 
-        optim, lr_sched = self._get_optim_and_lr_sched(model, optimizer, lr_scheduler)
+        optim, lr_sched = self._get_optim_and_lr_sched(task_model, optimizer, lr_scheduler)
         state = self._get_state(task, model, optim, lr_sched)
 
         def on_exit(signum: int, _: FrameType | None) -> None:
             sig = signal.Signals(signum)
             self.on_exit(sig, state, task, model, optim, lr_sched)
 
         def on_finish_training() -> None:
             self.save_checkpoint(state, task, model, optim, lr_sched)
-            raise TrainingFinishedException
+            raise TrainingFinishedError
 
         # Handle user-defined interrupts.
         signal.signal(signal.SIGUSR1, on_exit)
 
         # Gets the datasets.
         with Timer("getting datasets", 0.1, spinner=True):
             train_ds = task.get_dataset("train")
@@ -182,15 +181,15 @@
 
                         try:
 
                             def batch_iterator() -> Iterator[Batch]:
                                 try:
                                     yield next(train_pf_iter)
                                 except StopIteration:
-                                    raise EpochDoneException
+                                    raise EpochDoneError
 
                                 for _ in range(self.get_batches_per_step(state) - 1):
                                     try:
                                         yield next(train_pf_iter)
                                     except StopIteration:
                                         pass
 
@@ -200,15 +199,15 @@
                                 state=state,
                                 task=task,
                                 model=model,
                                 optim=optim,
                                 lr_sched=lr_sched,
                             )
 
-                        except EpochDoneException:
+                        except EpochDoneError:
                             break
 
                         valid_every_n_steps = self.config.validation.valid_every_n_steps
                         if valid_every_n_steps is not None and state.num_steps % valid_every_n_steps == 0:
                             self._log_prefetcher_stats(valid_pf)
 
                             self.val_step(
@@ -229,15 +228,15 @@
                             self.on_step_end(state, loss_dict, task, model, optim, lr_sched)
 
                     with self.step_context("on_epoch_end"):
                         self.on_epoch_end(state, task, model, optim, lr_sched)
 
                     state.num_epochs += 1
 
-        except TrainingFinishedException:
+        except TrainingFinishedError:
             logger.info(
                 "Finished training after %d epochs, %d steps, %d samples",
                 state.num_epochs,
                 state.num_steps,
                 state.num_samples,
             )
```

### Comparing `ml-starter-0.0.36/ml/trainers/vanilla.py` & `ml-starter-0.0.37/ml/trainers/vanilla.py`

 * *Files 26% similar despite different names*

```diff
@@ -3,111 +3,80 @@
 This trainer expects the task to handle all the relevant movement of data and
 models to their associated devices.
 """
 
 import logging
 from dataclasses import dataclass
 from pathlib import Path
-from typing import Callable, Generic, Iterator, TypeVar, cast
+from typing import Generic, Iterator, TypeVar
 
 import torch
-from omegaconf import II
 from torch import Tensor, nn
 from torch.optim import Optimizer
 
-from ml.core.common_types import Batch, Loss
+from ml.core.common_types import Batch
 from ml.core.config import conf_field
 from ml.core.state import State, set_phase
 from ml.lr_schedulers.base import BaseLRScheduler, SchedulerAdapter
 from ml.optimizers.base import BaseOptimizer
 from ml.trainers.base import BaseTrainer, BaseTrainerConfig, ModelT, TaskT
+from ml.trainers.mixins.compile import CompileConfig, CompileMixin
 from ml.trainers.mixins.cpu_stats import CPUStatsConfig, CPUStatsMixin
+from ml.trainers.mixins.data_parallel import ParallelMixin, TrainerParallelConfig
 from ml.trainers.mixins.gpu_stats import GPUStatsConfig, GPUStatsMixin
 from ml.trainers.mixins.grad_clipping import (
     GradientClippingConfig,
     GradientClippingTrainerMixin,
 )
 from ml.trainers.mixins.mixed_precision import (
     MixedPrecisionTrainerConfig,
     MixedPrecisionTrainerMixin,
 )
 from ml.trainers.mixins.profiler import ProfilerTrainerConfig, ProfilerTrainerMixin
-from ml.utils.distributed import get_world_size
 from ml.utils.timer import Timer
 
 logger: logging.Logger = logging.getLogger(__name__)
 
 
-class TrainingFinishedException(Exception):
+class TrainingFinishedError(Exception):
     pass
 
 
-class TaskModel(nn.Module, Generic[ModelT, TaskT, Batch, Loss]):
-    def __init__(self, task: TaskT, model: ModelT) -> None:
-        super().__init__()
-
-        self.task = task
-        self.model = model
-
-    def forward(self, batch: Batch, state: State) -> Loss:
-        self.task.on_before_forward_step(self.model, batch, state)
-        output = self.task.run_model(self.model, batch, state)
-        self.task.on_after_forward_step(self.model, batch, output, state)
-        loss: Loss = self.task.compute_loss(self.model, batch, state, output)
-        self.task.on_after_compute_loss(self.model, batch, output, loss, state)
-        return loss
-
-
-@dataclass
-class TorchCompileConfig:
-    enabled: bool = conf_field(II("oc.env:TORCH_COMPILE,0"), help="Enable Torch compilation")
-    fullgraph: bool = conf_field(False, help="Whether it is OK to break the model into subgraphs")
-    dynamic: bool = conf_field(False, help="Whether to use dynamic shape tracing")
-    backend: str = conf_field("auto", help="The backend to use")
-    mode: str | None = conf_field("max-autotune", help="Can be either 'default', 'reduce-overhead' or 'max-autotune'")
-
-
 @dataclass
 class VanillaTrainerConfig(
     ProfilerTrainerConfig,
     GradientClippingConfig,
     MixedPrecisionTrainerConfig,
     GPUStatsConfig,
     CPUStatsConfig,
+    CompileConfig,
+    TrainerParallelConfig,
     BaseTrainerConfig,
 ):
     set_to_none: bool = conf_field(True, help="Mode for clearing optimizer gradients")
     deterministic: bool = conf_field(False, help="If set, use determinstic algorithms")
     use_tf32: bool = conf_field(True, help="If set, use TensorFloat32")
-    torch_compile: TorchCompileConfig = conf_field(TorchCompileConfig(), help="Torch compile config")
     detect_anomaly: bool = conf_field(False, help="Whether to detect anomalies")
     detect_anomaly_check_nan: bool = conf_field(False, help="Whether to check for NaNs when detecting anomalies")
 
 
 VanillaTrainerConfigT = TypeVar("VanillaTrainerConfigT", bound=VanillaTrainerConfig)
 
 
 class VanillaTrainer(
     ProfilerTrainerMixin[VanillaTrainerConfigT, ModelT, TaskT],
     GradientClippingTrainerMixin[VanillaTrainerConfigT, ModelT, TaskT],
     MixedPrecisionTrainerMixin[VanillaTrainerConfigT, ModelT, TaskT],
     GPUStatsMixin[VanillaTrainerConfigT, ModelT, TaskT],
     CPUStatsMixin[VanillaTrainerConfigT, ModelT, TaskT],
+    CompileMixin[VanillaTrainerConfigT, ModelT, TaskT],
+    ParallelMixin[VanillaTrainerConfigT, ModelT, TaskT],
     BaseTrainer[VanillaTrainerConfigT, ModelT, TaskT],
     Generic[VanillaTrainerConfigT, ModelT, TaskT],
 ):
-    def get_task_model(self, task: TaskT, model: ModelT) -> nn.Module:
-        device, dtype = self._device.get_device(), self._weight_precision
-        model.init(device, dtype)
-        task.to(device, dtype)
-        task_model: nn.Module = TaskModel(task=task, model=model)
-        if get_world_size() > 1:
-            task_model = nn.parallel.DistributedDataParallel(task_model)
-        return task_model
-
     def train_step(
         self,
         *,
         task_model: nn.Module,
         batches: Iterator[Batch],
         state: State,
         task: TaskT,
@@ -222,43 +191,22 @@
             self.save_config()
             self.log_run_config()
 
         # Enables anomaly detection.
         if self.config.detect_anomaly:
             torch.autograd.set_detect_anomaly(True, check_nan=self.config.detect_anomaly_check_nan)
 
-    def _compile_model(self, model: ModelT) -> ModelT:
-        if self.config.torch_compile.enabled:
-            backend: str | Callable = self.config.torch_compile.backend
-            if backend == "auto":
-                backend = self._device.get_torch_compile_backend()
-                logger.info("Using torch-compile backend [%s]", backend)
-
-            model = cast(
-                ModelT,
-                torch.compile(
-                    model,
-                    fullgraph=self.config.torch_compile.fullgraph,
-                    dynamic=self.config.torch_compile.dynamic,
-                    backend=backend,
-                    mode=self.config.torch_compile.mode,
-                    disable=not self.config.torch_compile.enabled,
-                ),
-            )
-
-        return model
-
     def _get_optim_and_lr_sched(
         self,
-        model: ModelT,
+        task_model: nn.Module,
         optimizer: BaseOptimizer,
         lr_scheduler: BaseLRScheduler,
     ) -> tuple[Optimizer, SchedulerAdapter]:
         with Timer("building optimizer", 0.1, spinner=True):
-            optim = optimizer.get(model)
+            optim = optimizer.get(task_model)
         with Timer("building learning rate scheduler", 0.1, spinner=True):
             lr_sched = lr_scheduler.get(optim)
         return optim, lr_sched
 
     def _get_state(
         self,
         task: TaskT,
```

### Comparing `ml-starter-0.0.36/ml/utils/argparse.py` & `ml-starter-0.0.37/ml/utils/argparse.py`

 * *Files 5% similar despite different names*

```diff
@@ -19,15 +19,14 @@
 
     Returns:
         The type corresponding to the type name.
 
     Raises:
         ValueError: If the type name is not supported.
     """
-
     if type_name == "str":
         return str
     if type_name == "float":
         return float
     if type_name == "int":
         return int
     raise ValueError(type_name)
@@ -39,15 +38,14 @@
     Args:
         parser: The argument parser to add arguments to.
         dc: The dataclass to add arguments from.
 
     Raises:
         NotImplementedError: If the dataclass has a field with an unsupported type.
     """
-
     for field in fields(dc):
         args: list[str] = []
         if field.metadata.get("short") is not None:
             args.append(f"-{field.metadata['short']}")
         args.append(f"--{field.name.replace('_', '-')}")
         kwargs: dict[str, Any] = {}
         if field.default != MISSING:
@@ -59,15 +57,15 @@
         if field.type in (str, float, int):
             assert "default" in kwargs, f"Field {field.name} requires default"
             kwargs["type"] = field.type
         elif field.type is bool:
             assert "default" in kwargs, f"Field {field.name} requires default"
             default_val = cast(bool, kwargs["default"])
             kwargs["action"] = "store_false" if default_val else "store_true"
-        elif field.type in ("str", "float", "int"):  # type: ignore
+        elif field.type in ("str", "float", "int"):  # type: ignore[comparison-overlap]
             kwargs["type"] = get_type_from_string(cast(str, field.type))
             if "default" in kwargs and not isinstance(kwargs["default"], kwargs["type"]):
                 kwargs.pop("default")
                 kwargs["required"] = True
             elif "default" not in kwargs:
                 kwargs["required"] = True
         elif get_origin(field.type) is Union:
@@ -91,14 +89,13 @@
     Args:
         args: The argument parser namespace to create the dataclass from.
         dc: The dataclass to create.
 
     Returns:
         The dataclass created from the argument parser namespace.
     """
-
     values: dict[str, Any] = {}
     for field in fields(dc):
         values[field.name] = getattr(args, field.name)
     cfg = OmegaConf.structured(dc(**values))
     dc.resolve(cfg)
     return cfg
```

### Comparing `ml-starter-0.0.36/ml/utils/atomic.py` & `ml-starter-0.0.37/ml/utils/atomic.py`

 * *Files 2% similar despite different names*

```diff
@@ -22,15 +22,14 @@
 
 def fsync_directory(path: Path) -> None:
     """Performs an fsync on a directory.
 
     Args:
         path: The path to fsync.
     """
-
     fid = os.open(str(path), os.O_RDONLY)
     try:
         os.fsync(fid)
     finally:
         if fid >= 0:
             os.close(fid)
 
@@ -43,15 +42,14 @@
     """Performs an atomic save using a temporary file.
 
     Args:
         save_func: The function to call, that saves the file
         save_path: Where to save the file
         durable: If set, make the write durable
     """
-
     save_path = Path(save_path)
     tmp_file = save_path.parent / f".tmp_{save_path.name}"
     renamed = False
     try:
         save_func(tmp_file)
         tmp_file.rename(save_path)
         renamed = True
@@ -72,15 +70,14 @@
 
     Yields:
         The path to the temporary file
 
     Raises:
         OSError: If the temporary file could not be created
     """
-
     tf = tmp.NamedTemporaryFile(delete=False, suffix=suffix, dir=dir)
     tf.file.close()
     try:
         yield tf.name
     finally:
         try:
             os.remove(tf.name)
@@ -111,15 +108,15 @@
     *,
     encoding: str = "utf-8",
     fsync: bool = False,
 ) -> ContextManager[TextIO]:
     ...
 
 
-@contextmanager  # type: ignore
+@contextmanager  # type: ignore[misc]
 def open_atomic(
     filepath: str | Path,
     mode: str,
     *,
     encoding: str = "utf-8",
     fsync: bool = False,
 ) -> Iterator[IO[Any]]:
@@ -130,15 +127,14 @@
         mode: The mode to open the file in
         encoding: The encoding to use
         fsync: If set, make the write durable
 
     Yields:
         A context manager that yields the opened file
     """
-
     with tempfile(dir=os.path.dirname(os.path.abspath(filepath))) as tmppath:
         with open(tmppath, mode=mode, encoding=encoding) as file:
             try:
                 yield cast(Union[TextIO, BinaryIO], file)
             finally:
                 if fsync:
                     file.flush()
```

### Comparing `ml-starter-0.0.36/ml/utils/augmentation.py` & `ml-starter-0.0.37/ml/utils/augmentation.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,14 @@
         image: The image to mask, with shape (..., H, W)
         min_prct: Minimum percent of image to mask in either dimension
         max_prct: Maximum percent of image to mask in either dimension
 
     Returns:
         An image mask, with shape (..., H, W) matching the original image shape
     """
-
     device, bsz, (height, width) = image.device, image.shape[:-2], image.shape[-2:]
     mask_dims = bsz + (1, 1)
 
     min_height, max_height = int(height * min_prct), int(height * max_prct)
     min_width, max_width = int(width * min_prct), int(width * max_prct)
 
     mask_height = torch.floor(torch.rand(*mask_dims, device=device) * (max_height - min_height) + min_height).long()
```

### Comparing `ml-starter-0.0.36/ml/utils/caching.py` & `ml-starter-0.0.37/ml/utils/caching.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,29 +15,28 @@
 Object = TypeVar("Object", bound=Any)
 Tk = TypeVar("Tk")
 Tv = TypeVar("Tv")
 
 CacheType = Literal["pkl", "json"]
 
 
-class cached_object:  # pylint: disable=invalid-name
+class cached_object:  # noqa: N801
     def __init__(self, cache_key: str, ext: CacheType = "pkl", ignore: bool = False, cache_obj: bool = True) -> None:
         """Defines a wrapper for caching function calls to a file location.
 
         This is just a convenient way of caching heavy operations to disk,
         using a specific key.
 
         Args:
             cache_key: The key to use for caching the file
             ext: The caching type to use (JSON or pickling)
             ignore: Should the cache be ignored?
             cache_obj: If set, keep the object around to avoid deserializing it
                 when it is accessed again
         """
-
         self.cache_key = cache_key
         self.ext = ext
         self.obj = None
         self.ignore = ignore
         self.cache_obj = cache_obj
 
         assert ext in get_args(CacheType), f"Unexpected extension: {ext}"
@@ -102,15 +101,14 @@
         This lazily indexes all the values in the provided dictionary, flattens
         them out and allows them to be looked up by a specific index. This is
         analogous to PyTorch's ConcatDataset.
 
         Args:
             items: The dictionary to index
         """
-
         self.items = items
 
     @functools.cached_property
     def _item_list(self) -> list[tuple[Tk, list[Tv]]]:
         return [(k, list(v)) for k, v in self.items.items()]
 
     @functools.cached_property
```

### Comparing `ml-starter-0.0.36/ml/utils/cli.py` & `ml-starter-0.0.37/ml/utils/cli.py`

 * *Files identical despite different names*

### Comparing `ml-starter-0.0.36/ml/utils/data.py` & `ml-starter-0.0.37/ml/utils/data.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Some common utilities for datasets and data loaders."""
+
 import hashlib
 from dataclasses import dataclass
 from pathlib import Path
 from typing import Sequence, TypeVar
 
 import tqdm
 from torch.utils.data.dataloader import get_worker_info as _get_worker_info_base
@@ -20,15 +22,14 @@
 
 def get_worker_info() -> WorkerInfo:
     """Gets a typed worker info object which always returns a value.
 
     Returns:
         The typed worker info object
     """
-
     if (worker_info := _get_worker_info_base()) is None:
         return WorkerInfo(
             worker_id=0,
             num_workers=1,
             in_worker=False,
         )
 
@@ -57,15 +58,14 @@
 
     Returns:
         A tuple of three lists, one for each phase.
 
     Raises:
         ValueError: If the split sizes would be invalid.
     """
-
     num_items = len(items)
 
     # Converts a fraction to an integer number of items.
     if isinstance(valid, float):
         if 0 > valid or valid > 1:
             raise ValueError(f"Valid fraction must be between 0 and 1, got {valid}")
         valid = int(num_items * valid)
@@ -104,15 +104,14 @@
 
     Returns:
         The items for the given phase.
 
     Raises:
         ValueError: If the phase is not valid.
     """
-
     train_items, valid_items, test_items = get_dataset_splits(items, valid, test)
 
     match phase:
         case "train":
             return train_items
         case "valid":
             return valid_items
@@ -130,15 +129,14 @@
         hash_str: Expected MD5 of the file.
         chunk_size: Size of the chunks to read from the file.
         use_tqdm: Whether to use tqdm to show progress.
 
     Returns:
         True if the MD5 matches, False otherwise.
     """
-
     md5 = hashlib.md5()
 
     with open(file_path, "rb") as f:
         for chunk in tqdm.tqdm(iter(lambda: f.read(chunk_size), b""), disable=not use_tqdm, delay=1.0):
             md5.update(chunk)
 
     return md5.hexdigest() == hash_str
@@ -152,15 +150,14 @@
         hash_str: Expected SHA256 of the file.
         chunk_size: Size of the chunks to read from the file.
         use_tqdm: Whether to use tqdm to show progress.
 
     Returns:
         True if the SHA256 matches, False otherwise.
     """
-
     sha256 = hashlib.sha256()
 
     with open(file_path, "rb") as f:
         for chunk in tqdm.tqdm(iter(lambda: f.read(chunk_size), b""), disable=not use_tqdm, delay=1.0):
             sha256.update(chunk)
 
     return sha256.hexdigest() == hash_str
```

### Comparing `ml-starter-0.0.36/ml/utils/datetime.py` & `ml-starter-0.0.37/ml/utils/datetime.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Utilities for working with datetimes."""
+
 import datetime
 
 
 def format_timedelta(delta: datetime.timedelta) -> str:
     """Formats a time delta to human-readable format.
 
     Args:
@@ -34,9 +36,8 @@
 
     Args:
         dt: The datetime to format
 
     Returns:
         The human-readable datetime
     """
-
     return dt.strftime("%Y-%m-%d %H:%M:%S")
```

### Comparing `ml-starter-0.0.36/ml/utils/device/auto.py` & `ml-starter-0.0.37/ml/utils/device/auto.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,16 +1,28 @@
+"""Defines a utility class for automatically detecting the device to use.
+
+This function just goes through a list of devices in order of priority and
+finds whichever one is available. To disable some device, you can set the
+associated environment variable, for example:
+
+.. code-block:: bash
+
+    export DISABLE_METAL=1
+    export DISABLE_GPU=1
+"""
+
 import functools
 import logging
 from typing import Type
 
 from ml.utils.device.base import BaseDevice
 from ml.utils.device.cpu import CPUDevice
 from ml.utils.device.gpu import GPUDevice
 from ml.utils.device.metal import MetalDevice
-from ml.utils.logging import INFOALL
+from ml.utils.logging import DEBUGALL
 
 logger: logging.Logger = logging.getLogger(__name__)
 
 # These devices are ordered by priority, so an earlier device in the list
 # is preferred to a later device in the list.
 ALL_DEVICES: list[Type[BaseDevice]] = [
     MetalDevice,
@@ -23,15 +35,15 @@
     """Mixin to automatically detect the device type to use."""
 
     @classmethod
     @functools.lru_cache(None)
     def detect_device(cls) -> Type[BaseDevice]:
         for device_type in ALL_DEVICES:
             if device_type.has_device():
-                logger.log(INFOALL, "Device: [%s]", device_type.get_device())
+                logger.log(DEBUGALL, "Device: [%s]", device_type.get_device())
                 return device_type
         raise RuntimeError("Could not automatically detect the device to use")
 
     @classmethod
     def get_device_from_key(cls, key: str) -> Type[BaseDevice]:
         if key == "auto":
             return AutoDevice.detect_device()
```

### Comparing `ml-starter-0.0.36/ml/utils/device/base.py` & `ml-starter-0.0.37/ml/utils/device/base.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,26 @@
+"""Utilities for working with devices.
+
+This module contains utilities for working with devices, such as moving tensors
+and modules to devices, and getting prefetchers for non-blocking host-to-device
+transfers.
+
+The typical flow for using this module is:
+
+.. code-block:: python
+
+    from ml.utils.device.auto import AutoDevice
+
+    device = AutoDevice.detect_device()
+    device.module_to(some_module)
+    device.tensor_to(some_tensor)
+    device.get_prefetcher(some_dataloader)
+    device.recursive_apply(some_container, some_func)
+"""
+
 import contextlib
 import functools
 import threading
 from abc import ABC, abstractmethod
 from dataclasses import is_dataclass
 from typing import Any, Callable, ContextManager, Iterable, Iterator, Mapping, Sequence
 
@@ -24,15 +43,14 @@
     Args:
         item: The item to apply the function to
         func: The function to apply (for the tensor)
 
     Returns:
         The same item, with the function applied
     """
-
     if isinstance(item, (str, int, float)):
         return item
     if isinstance(item, np.ndarray):
         item = torch.from_numpy(item)
     if isinstance(item, Tensor):
         return func(item)
     if is_dataclass(item):
@@ -97,15 +115,14 @@
         Args:
             item: The item to apply the function to
             chunks: The number of output chunks
 
         Returns:
             The item, split into the requested number of chunks
         """
-
         if isinstance(item, (str, int, float)):
             return [item] * chunks
         if isinstance(item, np.ndarray):
             item = torch.from_numpy(item)
         if isinstance(item, Tensor):
             item_chunk_list = list(item.chunk(chunks, dim=0))
             assert len(item_chunk_list) == chunks, f"{len(item_chunk_list)=} != {chunks=}"
```

### Comparing `ml-starter-0.0.36/ml/utils/device/cpu.py` & `ml-starter-0.0.37/ml/utils/device/cpu.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""CPU device type."""
+
 from typing import Callable
 
 import torch
 
 from ml.utils.device.base import BaseDevice
```

### Comparing `ml-starter-0.0.36/ml/utils/device/gpu.py` & `ml-starter-0.0.37/ml/utils/device/gpu.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+"""GPU device type.
+
+The default floating point type can be configured with the environment
+variables:
+
+- ``USE_FP64``: Use FP64
+- ``USE_FP32``: Use FP32
+- ``USE_BF16``: Use BF16
+"""
+
 import logging
 import os
 from typing import Callable
 
 import torch
 
 from ml.core.env import is_gpu_disabled
@@ -21,15 +31,15 @@
 
     @classmethod
     def has_device(cls) -> bool:
         return torch.cuda.is_available() and torch.cuda.device_count() > 0 and not is_gpu_disabled()
 
     @classmethod
     def get_device(cls) -> torch.device:
-        return torch.device("cuda", 0)
+        return torch.device("cuda")
 
     @classmethod
     def get_floating_point_type(cls) -> torch.dtype:
         use_bf16 = get_env_bool("USE_BF16")
         use_fp32 = get_env_bool("USE_FP32")
         use_fp64 = get_env_bool("USE_FP64")
         if use_fp64:
```

### Comparing `ml-starter-0.0.36/ml/utils/image.py` & `ml-starter-0.0.37/ml/utils/image.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines utilities for dealing with images."""
+
 import itertools
 import math
 from fractions import Fraction
 from pathlib import Path
 from typing import Iterator
 
 import numpy as np
@@ -34,15 +36,14 @@
         interpolation: Interpolation mode to use for image resizing
         trg_res: The target image resolution; the image will be reshaped to
             have approximately the same area as an image with this resolution
 
     Returns:
         The resized image
     """
-
     width, height = V.get_image_size(image)
     trg_height, trg_width = trg_res
     factor = math.sqrt((trg_height * trg_width) / (height * width))
     new_height, new_width = int(height * factor), int(width * factor)
     return V.resize(image, [new_height, new_width], interpolation)
 
 
@@ -70,15 +71,14 @@
 
     Returns:
         The normalized image, with shape (H, W, C)
 
     Raises:
         ValueError: If the image shape is invalid
     """
-
     if isinstance(image, np.ndarray):
         image = torch.from_numpy(image)
 
     if normalize and image.is_floating_point():
         minv, maxv = _aminmax(image)
         maxv.clamp_min_(1.0)
         minv.clamp_max_(0.0)
@@ -108,15 +108,14 @@
     Args:
         in_file: The path to the input file.
         skip_first_frame: If set, skip the first frame.
 
     Yields:
         A stream of Numpy arrays with shape (H, W, C).
     """
-
     gif = Image.open(str(in_file))
     iterator = ImageSequence.Iterator(gif)
     if skip_first_frame:
         next(iterator)
     for frame in iterator:
         yield np.array(frame)
 
@@ -138,15 +137,17 @@
         keep_resolution: If set, preserve original image resolution, otherwise
             change image resolution to human-viewable.
         fps: Frames per second for the GIF.
         loop: If set, loop the GIF.
         first_frame_zeros: If set, the first frame will be all zeros.
     """
 
-    to_image = lambda t: Image.fromarray(standardize_image(t, keep_resolution=keep_resolution))
+    def to_image(t: np.ndarray | Tensor) -> Image.Image:
+        return Image.fromarray(standardize_image(t, keep_resolution=keep_resolution))
+
     first_frame = standardize_image(next(itr), keep_resolution=keep_resolution)
     first_img = Image.fromarray(np.zeros_like(first_frame) if first_frame_zeros else first_frame)
     first_img.save(
         str(out_file),
         save_all=True,
         append_images=itertools.chain((Image.fromarray(i) for i in (first_frame,)), (to_image(t) for t in itr)),
         duration=int(1000 / fps),  # Number of milliseconds per frame.
```

### Comparing `ml-starter-0.0.36/ml/utils/io.py` & `ml-starter-0.0.37/ml/utils/checkpoint.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,14 @@
+"""Defines checkpoint utility functions.
+
+These functions can be used to load a model from an arbitrary config file
+and checkpoint. Note that there might be some issues if you move the checkpoint
+around places.
+"""
+
 import logging
 from pathlib import Path
 from typing import TypeVar, cast
 
 import torch
 from omegaconf import DictConfig, OmegaConf
 
@@ -23,15 +30,14 @@
     Args:
         config: The config to use. If a string or a Path, it is expected to
             be a path to a YAML file.
 
     Returns:
         The instantiated objects.
     """
-
     if isinstance(config, (str, Path)):
         config = cast(DictConfig, OmegaConf.load(config))
     elif isinstance(config, dict):
         config = OmegaConf.create(config)
     Objects.resolve_config(config)
     return Objects.parse_raw_config(config)
 
@@ -92,15 +98,14 @@
         The model and task loaded from the checkpoint
 
     Raises:
         ValueError: If both `config_path` and `ckpt_path` are None.
         RuntimeError: If the checkpoint is missing and `missing_ckpt_okay` is
             False.
     """
-
     with Timer("loading checkpoint"):
         ckpt: str | Path | dict | None = None
 
         trainer: BaseTrainer
 
         if config_path is None:
             if ckpt_path is None:
```

### Comparing `ml-starter-0.0.36/ml/utils/large_models.py` & `ml-starter-0.0.37/ml/utils/large_models.py`

 * *Files 10% similar despite different names*

```diff
@@ -18,44 +18,43 @@
     Args:
         include_buffers: Whether or not to also put all buffers on the meta
             device while initializing.
 
     Yields:
         An empty context manager
     """
-
     old_register_parameter = nn.Module.register_parameter
     if include_buffers:
         old_register_buffer = nn.Module.register_buffer
 
     def register_empty_parameter(module: nn.Module, name: str, param: nn.Parameter | None) -> None:
         old_register_parameter(module, name, param)
         if param is not None:
             param_cls = type(module._parameters[name])
             kwargs = module._parameters[name].__dict__
-            meta_param = module._parameters[name].to(torch.device("meta"))  # type: ignore
-            module._parameters[name] = param_cls(meta_param, **kwargs)  # type: ignore
+            meta_param = module._parameters[name].to(torch.device("meta"))  # type: ignore[union-attr]
+            module._parameters[name] = param_cls(meta_param, **kwargs)  # type: ignore[misc]
 
     def register_empty_buffer(module: nn.Module, name: str, buffer: Tensor | None) -> None:
         old_register_buffer(module, name, buffer)
         if buffer is not None:
-            module._buffers[name] = module._buffers[name].to(torch.device("meta"))  # type: ignore
+            module._buffers[name] = module._buffers[name].to(torch.device("meta"))  # type: ignore[union-attr]
 
     try:
-        nn.Module.register_parameter = register_empty_parameter  # type: ignore
+        nn.Module.register_parameter = register_empty_parameter  # type: ignore[assignment]
         if include_buffers:
-            nn.Module.register_buffer = register_empty_buffer  # type: ignore
+            nn.Module.register_buffer = register_empty_buffer  # type: ignore[assignment]
         yield
     finally:
-        nn.Module.register_parameter = old_register_parameter  # type: ignore
+        nn.Module.register_parameter = old_register_parameter  # type: ignore[method-assign]
         if include_buffers:
-            nn.Module.register_buffer = old_register_buffer  # type: ignore
+            nn.Module.register_buffer = old_register_buffer  # type: ignore[method-assign]
 
 
-def meta_to_empty_func(device: torch.device, dtype: torch.dtype | None) -> Callable[[Tensor], Tensor]:
+def meta_to_empty_func(device: torch.device | str, dtype: torch.dtype | None = None) -> Callable[[Tensor], Tensor]:
     def _func(t: Tensor) -> Tensor:
         if not t.is_meta:
             return t
         if t.is_floating_point() and dtype is not None:
             return torch.empty(t.shape, device=device, dtype=dtype)
         return torch.empty(t.shape, device=device)
```

### Comparing `ml-starter-0.0.36/ml/utils/logging.py` & `ml-starter-0.0.37/ml/utils/logging.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,34 +1,41 @@
+"""Logging utilities.
+
+This extends the basic Python logger to log across all ranks, and to colorize
+the logs to make them easier to parse.
+"""
+
 import logging
 import math
 import sys
 import time
 
 from ml.core.env import is_debugging
 from ml.utils.colors import Color, colorize, get_colorize_parts
 
 # Logging level to show on all ranks.
 INFOALL: int = logging.INFO + 1
+DEBUGALL: int = logging.DEBUG + 1
 
 
 class RankFilter(logging.Filter):
     def __init__(self, *, rank: int | None = None) -> None:
         """Logging filter which filters out INFO logs on non-zero ranks.
 
         Args:
             rank: The current rank
         """
-
         super().__init__()
 
         self.rank = rank
 
         # Log using INFOALL to show on all ranks.
         logging.addLevelName(INFOALL, "INFOALL")
-        levels_to_log_all_ranks = (INFOALL, logging.CRITICAL, logging.ERROR, logging.WARNING)
+        logging.addLevelName(DEBUGALL, "DEBUGALL")
+        levels_to_log_all_ranks = (DEBUGALL, INFOALL, logging.CRITICAL, logging.ERROR, logging.WARNING)
         self.log_all_ranks = {logging.getLevelName(level) for level in levels_to_log_all_ranks}
 
     def filter(self, record: logging.LogRecord) -> bool:
         if self.rank is None or self.rank == 0:
             return True
         if record.levelname in self.log_all_ranks:
             return True
@@ -42,14 +49,15 @@
     COLOR_SEQ = "\033[1;%dm"
     BOLD_SEQ = "\033[1m"
 
     COLORS: dict[str, Color] = {
         "WARNING": "yellow",
         "INFOALL": "magenta",
         "INFO": "cyan",
+        "DEBUGALL": "grey",
         "DEBUG": "grey",
         "CRITICAL": "yellow",
         "FATAL": "red",
         "ERROR": "red",
     }
 
     def __init__(
@@ -74,17 +82,16 @@
         self.use_color = use_color
 
     def format(self, record: logging.LogRecord) -> str:
         levelname = record.levelname
 
         if levelname == "DEBUG":
             record.levelname = ""
-        else:
-            if self.use_color and levelname in self.COLORS:
-                record.levelname = colorize(levelname, self.COLORS[levelname], bold=True)
+        elif self.use_color and levelname in self.COLORS:
+            record.levelname = colorize(levelname, self.COLORS[levelname], bold=True)
         return logging.Formatter.format(self, record)
 
 
 class TqdmHandler(logging.Handler):
     def emit(self, record: logging.LogRecord) -> None:
         import tqdm
 
@@ -107,15 +114,14 @@
 
     Args:
         prefix: An optional prefix to add to the logger
         rank: The current rank, or None if not using multiprocessing
         world_size: The total world size, or None if not using multiprocessing
         use_tqdm: Write using TQDM instead of sys.stdout
     """
-
     if rank is not None or world_size is not None:
         assert rank is not None and world_size is not None
     root_logger = logging.getLogger()
     while root_logger.hasHandlers():
         root_logger.removeHandler(root_logger.handlers[0])
     handler = TqdmHandler() if use_tqdm else logging.StreamHandler(sys.stdout)
     handler.setFormatter(ColoredFormatter(prefix=prefix, rank=rank, world_size=world_size))
```

### Comparing `ml-starter-0.0.36/ml/utils/meter.py` & `ml-starter-0.0.37/ml/utils/meter.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+"""Defines a meter for computing statistics over a stream of values."""
+
 import functools
 from typing import Any, cast
 
 import torch
 import torch.distributed as dist
 from torch import Tensor
```

### Comparing `ml-starter-0.0.36/ml/utils/staging.py` & `ml-starter-0.0.37/ml/utils/staging.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+"""Functions for staging environments.
+
+Staged environments freeze a copy of the current Python codebase that can be
+run in a separate process without worrying that changes to the current codebase
+will affect the staged environment.
+
+To save space, it basically copies over whatever modules are in the current
+environment (which are a subset of the codebase) to a new directory.
+"""
+
 import datetime
 import hashlib
 import logging
 import os
 import shutil
 import sys
 from pathlib import Path
@@ -30,15 +40,14 @@
 
     Returns:
         The stage environment path
 
     Raises:
         ValueError: If no project root is found.
     """
-
     if isinstance(project_roots, (str, Path)):
         project_roots = [Path(project_roots)]
 
     if not project_roots:
         raise ValueError("No project root directories")
 
     with Timer("getting files to stage", spinner=True):
```

### Comparing `ml-starter-0.0.36/ml/utils/timer.py` & `ml-starter-0.0.37/ml/utils/timer.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,12 @@
+"""Defines a timer context manager for timing code blocks.
+
+This also provides a simple spinner for long-running tasks.
+"""
+
 import errno
 import functools
 import logging
 import os
 import signal
 import sys
 import threading
@@ -147,10 +152,10 @@
             signal.alarm(seconds)
             try:
                 result = func(*args, **kwargs)
             finally:
                 signal.alarm(0)
             return result
 
-        return wrapper  # type: ignore
+        return wrapper  # type: ignore[return-value]
 
     return decorator
```

### Comparing `ml-starter-0.0.36/ml/utils/video.py` & `ml-starter-0.0.37/ml/utils/video.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,24 @@
+"""Defines utilites for saving and loading video streams.
+
+The main API for using this module is:
+
+.. code-block:: python
+
+    from ml.utils.video import read_video, write_video
+
+    def frame_iterator() -> Iterator[Tensor]:
+        for frame in read_video("/path/to/video.mp4"):
+            yield frame
+
+    write_video(frame_iterator(), "/path/to/other/video.mp4")
+
+This just uses FFMPEG so it should be reasonably quick.
+"""
+
 import asyncio
 import re
 import shutil
 import warnings
 from dataclasses import dataclass
 from fractions import Fraction
 from pathlib import Path
@@ -65,15 +82,14 @@
         in_file: The input video to read
         output_fmt: The output image format
         channels: Number of output channels for each video frame
 
     Yields:
         Frames from the video as numpy arrays with shape (H, W, C)
     """
-
     props = VideoProps.from_file_ffmpeg(in_file)
 
     stream = ffmpeg.input(str(in_file))
     stream = ffmpeg.output(stream, "pipe:", format="rawvideo", pix_fmt=output_fmt, r=float(props.fps))
     stream = ffmpeg.run_async(stream, pipe_stdout=True)
 
     while True:
@@ -102,15 +118,14 @@
         target_dims: (width, height) dimensions for images being loaded, with
             None meaning that the aspect ratio should be kept the same
 
     Yields:
         Frames from the video as numpy arrays with shape (H, W, C), along with
         the frame timestamps
     """
-
     props = VideoProps.from_file_ffmpeg(in_file)
 
     def aspect_ratio(x: int, a: int, b: int) -> int:
         return (x * a + b - 1) // b
 
     vf: list[str] = []
     if target_dims is not None:
@@ -170,15 +185,14 @@
 
     Args:
         in_file: The input video to read
 
     Yields:
         Frames from the video as numpy arrays with shape (H, W, C)
     """
-
     cap = cv2.VideoCapture(str(in_file))
 
     while True:
         ret, buffer = cap.read()
         if not ret:
             cap.release()
             return
@@ -200,15 +214,14 @@
         out_file: The path to the output file.
         keep_resolution: If set, don't change the image resolution, otherwise
             resize to a human-friendly resolution.
         fps: Frames per second for the video.
         codec: FourCC code specifying OpenCV video codec type. Examples are
             MPEG, MP4V, DIVX, AVC1, H236.
     """
-
     Path(out_file).parent.mkdir(exist_ok=True, parents=True)
 
     first_img = standardize_image(next(itr), keep_resolution=keep_resolution)
     height, width, _ = first_img.shape
 
     fourcc = cv2.VideoWriter_fourcc(*codec)
     stream = cv2.VideoWriter(str(out_file), fourcc, fps if isinstance(fps, int) else round(fps), (width, height))
@@ -244,15 +257,14 @@
             resize to a human-friendly resolution.
         fps: Frames per second for the video.
         out_fps: Frames per second for the saved video.
         vcodec: The video codec to use for the output video
         input_fmt: The input image format
         output_fmt: The output image format
     """
-
     Path(out_file).parent.mkdir(exist_ok=True, parents=True)
 
     first_img = standardize_image(next(itr), keep_resolution=keep_resolution)
     height, width, _ = first_img.shape
 
     stream = ffmpeg.input("pipe:", format="rawvideo", pix_fmt=input_fmt, s=f"{width}x{height}", r=float(fps))
     stream = ffmpeg.output(stream, str(out_file), pix_fmt=output_fmt, vcodec=vcodec, r=float(out_fps))
@@ -293,15 +305,14 @@
         fps: Frames per second for the video.
         title: Title for the video metadata.
         comment: Comment for the video metadata.
         writer: The Matplotlib video writer to use (if you use the
             default one, make sure you have `ffmpeg` installed on your
             system).
     """
-
     Path(out_file).parent.mkdir(exist_ok=True, parents=True)
 
     first_img = standardize_image(next(itr), keep_resolution=keep_resolution)
     height, width, _ = first_img.shape
     fig, ax = plt.subplots(figsize=(width / dpi, height / dpi))
 
     # Ensures that there's no extra space around the image.
@@ -335,15 +346,15 @@
             mpl_writer.grab_frame()
 
 
 Reader = Literal["ffmpeg", "opencv"]
 Writer = Literal["ffmpeg", "matplotlib", "opencv"]
 
 
-def read_video(reader: Reader, in_file: str | Path) -> Iterator[np.ndarray]:
+def read_video(in_file: str | Path, *, reader: Reader = "ffmpeg") -> Iterator[np.ndarray]:
     if reader == "ffmpeg":
         if not shutil.which("ffmpeg"):
             warnings.warn("FFMPEG is not available in the system. Falling back to OpenCV.")
             reader = "opencv"
         else:
             return read_video_ffmpeg(in_file)
 
@@ -370,15 +381,14 @@
         keep_resolution: If set, don't change the image resolution, otherwise
             resize to a human-friendly resolution.
         writer: The video writer to use.
 
     Raises:
         ValueError: If the writer is invalid.
     """
-
     if writer == "ffmpeg":
         if not shutil.which("ffmpeg"):
             warnings.warn("FFMPEG is not available in the system. Falling back to OpenCV.")
             writer = "opencv"
         else:
             write_video_ffmpeg(itr, out_file, fps=fps, keep_resolution=keep_resolution)
             return
```

### Comparing `ml-starter-0.0.36/ml_starter.egg-info/PKG-INFO` & `ml-starter-0.0.37/ml_starter.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ml-starter
-Version: 0.0.36
+Version: 0.0.37
 Summary: ML project template repository
 Home-page: https://github.com/codekansas/ml-starter
 Author: Benjamin Bolte
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ml-starter-0.0.36/ml_starter.egg-info/SOURCES.txt` & `ml-starter-0.0.37/ml_starter.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 ml/core/common_types.py
 ml/core/config.py
 ml/core/env.py
 ml/core/registry.py
 ml/core/state.py
 ml/launchers/__init__.py
 ml/launchers/base.py
-ml/launchers/ddp.py
+ml/launchers/mp.py
 ml/launchers/slurm.py
 ml/launchers/torchrun.py
 ml/loggers/__init__.py
 ml/loggers/base.py
 ml/loggers/meter.py
 ml/loggers/multi.py
 ml/loggers/stdout.py
@@ -39,17 +39,19 @@
 ml/models/__init__.py
 ml/models/activations.py
 ml/models/base.py
 ml/models/embeddings.py
 ml/models/init.py
 ml/models/lora.py
 ml/models/norms.py
+ml/models/parallel.py
 ml/models/pretrained/__init__.py
 ml/models/pretrained/clip.py
 ml/models/pretrained/hubert.py
+ml/models/pretrained/llama.py
 ml/models/pretrained/sam.py
 ml/optimizers/__init__.py
 ml/optimizers/adam.py
 ml/optimizers/adamw.py
 ml/optimizers/adan.py
 ml/optimizers/base.py
 ml/optimizers/sgd.py
@@ -87,41 +89,44 @@
 ml/tasks/sl/base.py
 ml/trainers/__init__.py
 ml/trainers/base.py
 ml/trainers/rl.py
 ml/trainers/sl.py
 ml/trainers/vanilla.py
 ml/trainers/mixins/__init__.py
+ml/trainers/mixins/compile.py
 ml/trainers/mixins/cpu_stats.py
+ml/trainers/mixins/data_parallel.py
 ml/trainers/mixins/gpu_stats.py
 ml/trainers/mixins/grad_clipping.py
 ml/trainers/mixins/heartbeat.py
 ml/trainers/mixins/mixed_precision.py
 ml/trainers/mixins/monitor_process.py
 ml/trainers/mixins/profiler.py
 ml/trainers/mixins/step_wrapper.py
 ml/utils/__init__.py
 ml/utils/argparse.py
 ml/utils/atomic.py
 ml/utils/augmentation.py
 ml/utils/caching.py
-ml/utils/call_train.py
+ml/utils/checkpoint.py
 ml/utils/checks.py
 ml/utils/cli.py
 ml/utils/colors.py
+ml/utils/config.py
 ml/utils/data.py
 ml/utils/datetime.py
 ml/utils/distributed.py
 ml/utils/image.py
-ml/utils/io.py
 ml/utils/large_models.py
 ml/utils/logging.py
 ml/utils/meter.py
 ml/utils/networking.py
 ml/utils/numpy.py
+ml/utils/parallel.py
 ml/utils/random.py
 ml/utils/staging.py
 ml/utils/timer.py
 ml/utils/torch_distributed.py
 ml/utils/video.py
 ml/utils/device/__init__.py
 ml/utils/device/auto.py
```

### Comparing `ml-starter-0.0.36/pyproject.toml` & `ml-starter-0.0.37/pyproject.toml`

 * *Files 17% similar despite different names*

```diff
@@ -9,14 +9,15 @@
 timeout = 60
 addopts = "-rx -rf -x -q --full-trace"
 testpaths = ["tests"]
 
 markers = [
     "slow: Marks test as being slow",
     "has_gpu: Marks test as requiring a GPU to run",
+    "multi_gpu: Marks tests as requiring multiple GPUs to run",
     "has_mps: Marks test as requiring an MPS device to run",
 ]
 
 [tool.mypy]
 
 pretty = true
 show_column_numbers = true
@@ -29,14 +30,16 @@
 
 warn_unused_ignores = true
 warn_redundant_casts = true
 
 incremental = true
 namespace_packages = false
 
+exclude = ["^ml/api.py$"]
+
 # For TorchScript stuff.
 disable_error_code = ["attr-defined"]
 
 [[tool.mypy.overrides]]
 
 module = [
     "cv2.*",
@@ -49,25 +52,33 @@
 
 [tool.isort]
 
 profile = "black"
 
 [tool.ruff]
 
-select = ["E", "F", "I", "W"]
-ignore = ["E712", "E731"]
+select = ["ANN", "D", "E", "F", "I", "N", "PGH", "PLC", "PLE", "PLR", "PLW", "W"]
+
+ignore = [
+    "ANN101", "ANN102", "ANN401",
+    "D101", "D102", "D103", "D104", "D105", "D106", "D107",
+    "N812", "N817",
+    "PLR0911", "PLR0912", "PLR0913", "PLR0915", "PLR2004",
+    "PLW0603", "PLW2901",
+]
+
 line-length = 120
 dummy-variable-rgx = "^(_+|(_+[a-zA-Z0-9_]*[a-zA-Z0-9]+?))$"
 target-version = "py310"
 
 [tool.ruff.per-file-ignores]
 
 "__init__.py" = ["E402", "F401", "F403", "F811"]
 
-[tool.ruff.mccabe]
-
-max-complexity = 10
-
 [tool.ruff.isort]
 
 known-first-party = ["ml", "tests"]
 combine-as-imports = true
+
+[tool.ruff.pydocstyle]
+
+convention = "google"
```

### Comparing `ml-starter-0.0.36/setup.py` & `ml-starter-0.0.37/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 #!/usr/bin/env python
+"""Setup script for the ml-starter project."""
 
 import re
 
 from setuptools import setup
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description: str = f.read()
```

