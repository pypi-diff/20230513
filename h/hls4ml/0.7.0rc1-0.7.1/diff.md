# Comparing `tmp/hls4ml-0.7.0rc1.tar.gz` & `tmp/hls4ml-0.7.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hls4ml-0.7.0rc1.tar", last modified: Sat Apr 15 01:45:10 2023, max compression
+gzip compressed data, was "hls4ml-0.7.1.tar", last modified: Sat May 13 15:56:55 2023, max compression
```

## Comparing `hls4ml-0.7.0rc1.tar` & `hls4ml-0.7.1.tar`

### file list

```diff
@@ -1,536 +1,537 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.091124 hls4ml-0.7.0rc1/
--rw-r--r--   0 runner    (1001) docker     (123)     5421 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.clang-format
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.031124 hls4ml-0.7.0rc1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.031124 hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (123)     1520 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0 runner    (1001) docker     (123)      378 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/config.yml
--rw-r--r--   0 runner    (1001) docker     (123)      990 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/PULL_REQUEST_TEMPLATE.md
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/dependabot.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.031124 hls4ml-0.7.0rc1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1246 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/workflows/build-sphinx.yml
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/workflows/pre-commit.yml
--rw-r--r--   0 runner    (1001) docker     (123)      693 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/workflows/pypi-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)      692 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/workflows/test-sphinx.yml
--rw-r--r--   0 runner    (1001) docker     (123)      775 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.github/workflows/update-branch-on-pr.yml
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1797 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/CITATION.cff
--rw-r--r--   0 runner    (1001) docker     (123)     2810 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)     2719 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/Jenkinsfile
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     6035 2023-04-15 01:45:10.091124 hls4ml-0.7.0rc1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5263 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.031124 hls4ml-0.7.0rc1/contrib/
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14507 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/garnet.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.031124 hls4ml-0.7.0rc1/contrib/kl_layer/
--rw-r--r--   0 runner    (1001) docker     (123)      537 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/kl_layer/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     3367 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/kl_layer/kl_layer.h
--rw-r--r--   0 runner    (1001) docker     (123)     6006 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/contrib/kl_layer/kl_layer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.035124 hls4ml-0.7.0rc1/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      678 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.035124 hls4ml-0.7.0rc1/docs/advanced/
--rw-r--r--   0 runner    (1001) docker     (123)     3922 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/advanced/accelerator.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6561 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/advanced/extension.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2985 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/advanced/fifo_depth.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.035124 hls4ml-0.7.0rc1/docs/api/
--rw-r--r--   0 runner    (1001) docker     (123)    10243 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/api/configuration.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2601 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/api/hls-model.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4666 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/api/profiling.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3832 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/command.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6176 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/concepts.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4090 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)     1587 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/details.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5608 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/flows.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.039124 hls4ml-0.7.0rc1/docs/img/
--rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/act_hls4ml.png
--rw-r--r--   0 runner    (1001) docker     (123)    10406 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/act_keras.png
--rw-r--r--   0 runner    (1001) docker     (123)    26453 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/hls4ml_logo.png
--rw-r--r--   0 runner    (1001) docker     (123)    21083 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/hls4ml_logo.svg
--rw-r--r--   0 runner    (1001) docker     (123)    25377 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/hls4ml_logo_lightgrey.png
--rw-r--r--   0 runner    (1001) docker     (123)    23796 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/hls4ml_logo_lightgrey.svg
--rw-r--r--   0 runner    (1001) docker     (123)     7506 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/hls4ml_logo_navbar.png
--rw-r--r--   0 runner    (1001) docker     (123)    64144 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/logo.jpg
--rw-r--r--   0 runner    (1001) docker     (123)    23360 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)    98357 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/nn_map_paper_fig_2.png
--rw-r--r--   0 runner    (1001) docker     (123)   202059 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/overview.jpg
--rw-r--r--   0 runner    (1001) docker     (123)   642072 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/overview.pdf
--rw-r--r--   0 runner    (1001) docker     (123)   335589 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/pynqframe.png
--rw-r--r--   0 runner    (1001) docker     (123)    82654 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/reuse_factor_paper_fig_8.png
--rw-r--r--   0 runner    (1001) docker     (123)    10231 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/weights_hls4ml.png
--rw-r--r--   0 runner    (1001) docker     (123)    10969 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/weights_keras.png
--rw-r--r--   0 runner    (1001) docker     (123)    76029 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/img/zynq_interfaces.png
--rw-r--r--   0 runner    (1001) docker     (123)     1639 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2858 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/reference.rst
--rw-r--r--   0 runner    (1001) docker     (123)      271 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/release_notes.rst
--rw-r--r--   0 runner    (1001) docker     (123)      188 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     6249 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/setup.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/docs/status.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.039124 hls4ml-0.7.0rc1/example-models/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.023124 hls4ml-0.7.0rc1/example-models/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.039124 hls4ml-0.7.0rc1/example-models/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      514 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/.github/workflows/update-model-list.yml
--rw-r--r--   0 runner    (1001) docker     (123)      159 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      435 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/available_data_config.json
--rw-r--r--   0 runner    (1001) docker     (123)      988 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/available_models.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.039124 hls4ml-0.7.0rc1/example-models/config-files/
--rw-r--r--   0 runner    (1001) docker     (123)      877 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/config-files/garnet_1layer_config.yml
--rw-r--r--   0 runner    (1001) docker     (123)      949 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/config-files/garnet_3layer_config.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/config-files/qkeras_3layer_config.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1361 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/config-files/qkeras_mnist_cnn_config.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/config-files/qkeras_mnist_dense_config.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.039124 hls4ml-0.7.0rc1/example-models/data/
--rw-r--r--   0 runner    (1001) docker     (123)  1188502 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/data/garnet_1layer_input.dat
--rw-r--r--   0 runner    (1001) docker     (123)     2304 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/data/garnet_1layer_output.dat
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.051124 hls4ml-0.7.0rc1/example-models/keras/
--rw-r--r--   0 runner    (1001) docker     (123)     4042 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_1layer.json
--rw-r--r--   0 runner    (1001) docker     (123)    13944 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_1layer_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     8084 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer.json
--rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_70pruned_retrained_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_95pruned_retrained_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    15426 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_batch_norm.json
--rw-r--r--   0 runner    (1001) docker     (123)    55224 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_batch_norm_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     9912 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binary_smaller.json
--rw-r--r--   0 runner    (1001) docker     (123)    52240 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binary_smaller_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    11160 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binarydense_relu_max.json
--rw-r--r--   0 runner    (1001) docker     (123)    52224 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binarydense_relu_max_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     9919 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_ternary_small.json
--rw-r--r--   0 runner    (1001) docker     (123)    52240 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_ternary_small_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    10545 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d.json
--rw-r--r--   0 runner    (1001) docker     (123)    11331 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_small.json
--rw-r--r--   0 runner    (1001) docker     (123)    23232 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_small_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)  1026808 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     3342 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv2d_model.json
--rw-r--r--   0 runner    (1001) docker     (123)    19904 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_conv2d_model_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    12760 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5.json
--rw-r--r--   0 runner    (1001) docker     (123)   197336 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    13774 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5.json
--rw-r--r--   0 runner    (1001) docker     (123)   690872 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    12760 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5.json
--rw-r--r--   0 runner    (1001) docker     (123)  4080168 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/garnet_1layer.json
--rw-r--r--   0 runner    (1001) docker     (123)    20144 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/garnet_1layer_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     3004 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/garnet_3layer.json
--rw-r--r--   0 runner    (1001) docker     (123)    42488 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/garnet_3layer_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     4950 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small.json
--rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm.json
--rw-r--r--   0 runner    (1001) docker     (123)    25392 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)    32528 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     5429 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/keras_bnn.json
--rw-r--r--   0 runner    (1001) docker     (123)    71320 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/keras_bnn_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     6981 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_3layer.json
--rw-r--r--   0 runner    (1001) docker     (123)    38344 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_3layer_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     6020 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_cnn.json
--rw-r--r--   0 runner    (1001) docker     (123)    47424 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_cnn_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)     8220 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_dense.json
--rw-r--r--   0 runner    (1001) docker     (123)    79416 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_dense_weights.h5
--rw-r--r--   0 runner    (1001) docker     (123)      513 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/keras-config.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.051124 hls4ml-0.7.0rc1/example-models/onnx/
--rw-r--r--   0 runner    (1001) docker     (123)     2931 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/conv1d_small_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)     6593 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/conv2d_small_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)     4757 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/conv2d_small_mp_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)   172539 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/dense_big_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)    23520 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/three_layer_bn_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)    42287 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/three_layer_bn_pytorch.onnx
--rw-r--r--   0 runner    (1001) docker     (123)    18824 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/three_layer_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)    32007 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/three_layer_pytorch.onnx
--rw-r--r--   0 runner    (1001) docker     (123)     2242 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/two_layer_keras.onnx
--rw-r--r--   0 runner    (1001) docker     (123)     8688 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx/two_layer_pytorch.onnx
--rw-r--r--   0 runner    (1001) docker     (123)      460 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/onnx-config.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/example-models/pytorch/
--rw-r--r--   0 runner    (1001) docker     (123)    26028 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/pytorch/three_layer_model.pt
--rw-r--r--   0 runner    (1001) docker     (123)     8356 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/pytorch/two_layer_model.pt
--rw-r--r--   0 runner    (1001) docker     (123)      465 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/pytorch-config.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/scan.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/example-models/tensorflow/
--rw-r--r--   0 runner    (1001) docker     (123)    19927 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/tensorflow/3layer.pb
--rw-r--r--   0 runner    (1001) docker     (123)      475 2023-04-15 01:44:59.000000 hls4ml-0.7.0rc1/example-models/tf-config.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml/
--rw-r--r--   0 runner    (1001) docker     (123)      611 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml/backends/
--rw-r--r--   0 runner    (1001) docker     (123)      794 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6207 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/backend.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml/backends/fpga/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    31806 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_backend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3311 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_layers.py
--rw-r--r--   0 runner    (1001) docker     (123)    15575 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7331 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/bn_quant.py
--rw-r--r--   0 runner    (1001) docker     (123)      633 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/bram_weights.py
--rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/clone.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/codegen.py
--rw-r--r--   0 runner    (1001) docker     (123)     1348 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/embedding.py
--rw-r--r--   0 runner    (1001) docker     (123)      952 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/final_reshape.py
--rw-r--r--   0 runner    (1001) docker     (123)      821 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/inplace_parallel_reshape.py
--rw-r--r--   0 runner    (1001) docker     (123)      957 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/inplace_stream_flatten.py
--rw-r--r--   0 runner    (1001) docker     (123)      412 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/remove_softmax.py
--rw-r--r--   0 runner    (1001) docker     (123)     2079 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/repack_stream.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml/backends/quartus/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7592 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/convolution_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     9303 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/convolution_winograd.py
--rw-r--r--   0 runner    (1001) docker     (123)     8717 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/core_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     4077 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/merge_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     3651 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/pointwise.py
--rw-r--r--   0 runner    (1001) docker     (123)     4533 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/pooling_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/quantization_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)    13910 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/recurrent_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     4962 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/reshaping_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     4005 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/resource_strategy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/transform_types.py
--rw-r--r--   0 runner    (1001) docker     (123)    16171 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/quartus/quartus_backend.py
--rw-r--r--   0 runner    (1001) docker     (123)     2553 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/template.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vitis/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vitis/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vitis/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vitis/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vitis/passes/feature_check.py
--rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vitis/vitis_backend.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vivado/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4554 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/broadcast_stream.py
--rw-r--r--   0 runner    (1001) docker     (123)     3997 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/conv_same_pad.py
--rw-r--r--   0 runner    (1001) docker     (123)     2405 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/conv_stream.py
--rw-r--r--   0 runner    (1001) docker     (123)    20889 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/convolution_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     8426 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/core_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     3740 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/fifo_depth_optimization.py
--rw-r--r--   0 runner    (1001) docker     (123)    11959 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/garnet_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     3855 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/merge_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     3450 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/pointwise.py
--rw-r--r--   0 runner    (1001) docker     (123)     4728 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/pooling_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     1320 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/quantization_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     8300 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/recurrent_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     4742 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/reshaping_templates.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/resource_strategy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/transform_types.py
--rw-r--r--   0 runner    (1001) docker     (123)    19054 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado/vivado_backend.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.059124 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2938 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/passes/fifo_depth_optimization.py
--rw-r--r--   0 runner    (1001) docker     (123)     1448 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/supported_boards.json
--rw-r--r--   0 runner    (1001) docker     (123)     6517 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/vivado_accelerator_backend.py
--rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/vivado_accelerator_config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/converters/
--rw-r--r--   0 runner    (1001) docker     (123)    14404 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/converters/keras/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2790 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/convolution.py
--rw-r--r--   0 runner    (1001) docker     (123)     4442 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/core.py
--rw-r--r--   0 runner    (1001) docker     (123)     2141 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/graph.py
--rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/merge.py
--rw-r--r--   0 runner    (1001) docker     (123)     4130 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/pooling.py
--rw-r--r--   0 runner    (1001) docker     (123)     6535 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/qkeras.py
--rw-r--r--   0 runner    (1001) docker     (123)     1475 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/recurrent.py
--rw-r--r--   0 runner    (1001) docker     (123)     3236 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/reshape.py
--rw-r--r--   0 runner    (1001) docker     (123)     3590 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras/reshaping.py
--rw-r--r--   0 runner    (1001) docker     (123)    11658 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/keras_to_hls.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/converters/onnx/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3012 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/convolution.py
--rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/core.py
--rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/merge.py
--rw-r--r--   0 runner    (1001) docker     (123)     4011 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/pooling.py
--rw-r--r--   0 runner    (1001) docker     (123)     1389 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx/reshape.py
--rw-r--r--   0 runner    (1001) docker     (123)    10799 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/onnx_to_hls.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/converters/pytorch/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/pytorch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3176 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/pytorch/convolution.py
--rw-r--r--   0 runner    (1001) docker     (123)     2388 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/pytorch/core.py
--rw-r--r--   0 runner    (1001) docker     (123)     6191 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/pytorch_to_hls.py
--rw-r--r--   0 runner    (1001) docker     (123)    14698 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/tf_to_hls.py
--rw-r--r--   0 runner    (1001) docker     (123)     5647 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/converters/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/model/
--rw-r--r--   0 runner    (1001) docker     (123)      214 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8366 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/attributes.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/model/flow/
--rw-r--r--   0 runner    (1001) docker     (123)      161 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/flow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4466 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/flow/flow.py
--rw-r--r--   0 runner    (1001) docker     (123)    33950 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/graph.py
--rw-r--r--   0 runner    (1001) docker     (123)    52343 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/layers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.063124 hls4ml-0.7.0rc1/hls4ml/model/optimizer/
--rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9492 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/optimizer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.067124 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1469 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/bn_fuse.py
--rw-r--r--   0 runner    (1001) docker     (123)      618 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/fuse_biasadd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2568 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/multi_dense.py
--rw-r--r--   0 runner    (1001) docker     (123)      528 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/nop.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/precision_merge.py
--rw-r--r--   0 runner    (1001) docker     (123)    11642 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/qkeras.py
--rw-r--r--   0 runner    (1001) docker     (123)      647 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/stamp.py
--rw-r--r--   0 runner    (1001) docker     (123)      815 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/transpose_opt.py
--rw-r--r--   0 runner    (1001) docker     (123)    24057 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/profiling.py
--rw-r--r--   0 runner    (1001) docker     (123)    22807 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/model/types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.067124 hls4ml-0.7.0rc1/hls4ml/report/
--rw-r--r--   0 runner    (1001) docker     (123)      372 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/report/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9341 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/report/quartus_report.py
--rw-r--r--   0 runner    (1001) docker     (123)    25795 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/report/vivado_report.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.027124 hls4ml-0.7.0rc1/hls4ml/templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.067124 hls4ml-0.7.0rc1/hls4ml/templates/quartus/
--rw-r--r--   0 runner    (1001) docker     (123)      798 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.067124 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/
--rw-r--r--   0 runner    (1001) docker     (123)    18367 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_channel.h
--rw-r--r--   0 runner    (1001) docker     (123)    16534 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_complex.h
--rw-r--r--   0 runner    (1001) docker     (123)    59595 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_fixed.h
--rw-r--r--   0 runner    (1001) docker     (123)    44867 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_float.h
--rw-r--r--   0 runner    (1001) docker     (123)   105429 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_int.h
--rw-r--r--   0 runner    (1001) docker     (123)    17449 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_sc.h
--rw-r--r--   0 runner    (1001) docker     (123)    84637 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_std_float.h
--rw-r--r--   0 runner    (1001) docker     (123)      791 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/stream.h
--rwxr-xr-x   0 runner    (1001) docker     (123)      551 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/build_lib.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.067124 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/
--rw-r--r--   0 runner    (1001) docker     (123)     1382 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/defines.h
--rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/myproject.cpp
--rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/myproject.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.071124 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/
--rw-r--r--   0 runner    (1001) docker     (123)    18055 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation.h
--rw-r--r--   0 runner    (1001) docker     (123)    23323 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     3184 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm.h
--rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1946 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_common.h
--rw-r--r--   0 runner    (1001) docker     (123)     2245 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d.h
--rw-r--r--   0 runner    (1001) docker     (123)    10544 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     7594 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     2731 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d.h
--rw-r--r--   0 runner    (1001) docker     (123)    14958 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)    10556 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     7012 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense.h
--rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_compressed.h
--rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1259 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed.h
--rw-r--r--   0 runner    (1001) docker     (123)      700 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     5023 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_helpers.h
--rw-r--r--   0 runner    (1001) docker     (123)    11047 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge.h
--rw-r--r--   0 runner    (1001) docker     (123)    11820 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     3941 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_mult.h
--rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding.h
--rw-r--r--   0 runner    (1001) docker     (123)     2186 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    12470 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling.h
--rw-r--r--   0 runner    (1001) docker     (123)    12279 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    25143 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent.h
--rw-r--r--   0 runner    (1001) docker     (123)     1805 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_activation.h
--rw-r--r--   0 runner    (1001) docker     (123)     2025 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1223 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize.h
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     3191 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose.h
--rw-r--r--   0 runner    (1001) docker     (123)      963 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_types.h
--rw-r--r--   0 runner    (1001) docker     (123)      207 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/parameters.h
--rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_bridge.cpp
--rw-r--r--   0 runner    (1001) docker     (123)     3611 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_test_parallel.cpp
--rw-r--r--   0 runner    (1001) docker     (123)     3914 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_test_stream.cpp
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.027124 hls4ml-0.7.0rc1/hls4ml/templates/vitis/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.071124 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/
--rw-r--r--   0 runner    (1001) docker     (123)     4040 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     4168 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     3572 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     9671 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_dense_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_dense_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    15306 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_pooling.h
--rw-r--r--   0 runner    (1001) docker     (123)    12369 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_pooling_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     4246 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv1d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     6188 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv2d_stream.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.075124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.075124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/
--rw-r--r--   0 runner    (1001) docker     (123)    10180 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_common.h
--rw-r--r--   0 runner    (1001) docker     (123)     6473 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_decl.h
--rw-r--r--   0 runner    (1001) docker     (123)    12185 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed.h
--rw-r--r--   0 runner    (1001) docker     (123)    85182 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_base.h
--rw-r--r--   0 runner    (1001) docker     (123)    27302 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_ref.h
--rw-r--r--   0 runner    (1001) docker     (123)     6985 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_special.h
--rw-r--r--   0 runner    (1001) docker     (123)    10012 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int.h
--rw-r--r--   0 runner    (1001) docker     (123)    71735 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_base.h
--rw-r--r--   0 runner    (1001) docker     (123)    55218 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_ref.h
--rw-r--r--   0 runner    (1001) docker     (123)     6301 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_special.h
--rw-r--r--   0 runner    (1001) docker     (123)     4894 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_shift_reg.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.075124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/etc/
--rw-r--r--   0 runner    (1001) docker     (123)   261465 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/etc/ap_private.h
--rw-r--r--   0 runner    (1001) docker     (123)      194 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/hls_math.h
--rw-r--r--   0 runner    (1001) docker     (123)     7480 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/hls_stream.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.075124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/utils/
--rw-r--r--   0 runner    (1001) docker     (123)     2227 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/utils/x_hls_utils.h
--rwxr-xr-x   0 runner    (1001) docker     (123)      530 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/build_lib.sh
--rw-r--r--   0 runner    (1001) docker     (123)     7812 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/build_prj.tcl
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.075124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/defines.h
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/myproject.cpp
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/myproject.h
--rw-r--r--   0 runner    (1001) docker     (123)      311 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/parameters.h
--rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/myproject_bridge.cpp
--rw-r--r--   0 runner    (1001) docker     (123)     2749 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/myproject_test.cpp
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.079124 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/
--rw-r--r--   0 runner    (1001) docker     (123)    28377 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_activation.h
--rw-r--r--   0 runner    (1001) docker     (123)    26176 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_activation_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1724 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_array.h
--rw-r--r--   0 runner    (1001) docker     (123)     4140 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm.h
--rw-r--r--   0 runner    (1001) docker     (123)     3772 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)      937 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_code_gen.h
--rw-r--r--   0 runner    (1001) docker     (123)     2058 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_common.h
--rw-r--r--   0 runner    (1001) docker     (123)     2416 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d.h
--rw-r--r--   0 runner    (1001) docker     (123)     2972 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_latency.h
--rw-r--r--   0 runner    (1001) docker     (123)     3879 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     3717 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     2755 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d.h
--rw-r--r--   0 runner    (1001) docker     (123)     3010 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_latency.h
--rw-r--r--   0 runner    (1001) docker     (123)     4007 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     5131 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    14664 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense.h
--rw-r--r--   0 runner    (1001) docker     (123)     2859 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_compressed.h
--rw-r--r--   0 runner    (1001) docker     (123)     2424 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_latency.h
--rw-r--r--   0 runner    (1001) docker     (123)     9970 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_resource.h
--rw-r--r--   0 runner    (1001) docker     (123)     2318 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_embed.h
--rw-r--r--   0 runner    (1001) docker     (123)      839 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_embed_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    30731 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_garnet.h
--rw-r--r--   0 runner    (1001) docker     (123)    12524 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_helpers.h
--rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_image.h
--rw-r--r--   0 runner    (1001) docker     (123)     1847 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_image_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    10964 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_merge.h
--rw-r--r--   0 runner    (1001) docker     (123)    11628 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_merge_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     3703 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_mult.h
--rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_padding.h
--rw-r--r--   0 runner    (1001) docker     (123)     2191 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_padding_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    15287 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_pooling.h
--rw-r--r--   0 runner    (1001) docker     (123)    23670 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_pooling_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     1889 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_recr_activations.h
--rw-r--r--   0 runner    (1001) docker     (123)    27031 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_recurrent.h
--rw-r--r--   0 runner    (1001) docker     (123)     5310 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv1d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     6697 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv2d_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)    11285 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)     6882 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_stream.h
--rw-r--r--   0 runner    (1001) docker     (123)      724 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_types.h
--rw-r--r--   0 runner    (1001) docker     (123)      217 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado/vivado_synth.tcl
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.027124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/
--rw-r--r--   0 runner    (1001) docker     (123)    11385 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_read_master.sv
--rw-r--r--   0 runner    (1001) docker     (123)     9883 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_write_master.sv
--rw-r--r--   0 runner    (1001) docker     (123)    12999 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_control_s_axi.v
--rw-r--r--   0 runner    (1001) docker     (123)     2414 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_counter.sv
--rw-r--r--   0 runner    (1001) docker     (123)    18061 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_int.sv
--rw-r--r--   0 runner    (1001) docker     (123)     8472 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/myproject_kernel.v
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/
--rw-r--r--   0 runner    (1001) docker     (123)     4866 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/axi_stream_driver.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)     9028 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/axi_stream_design.tcl
--rw-r--r--   0 runner    (1001) docker     (123)      617 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/build_lib.sh
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/myproject_axi.cpp
--rw-r--r--   0 runner    (1001) docker     (123)      239 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/myproject_axi.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.027124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/
--rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/axi_stream_driver.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)     1533 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_lite_design.tcl
--rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_stream_design.tcl
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.027124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/
--rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/axi_stream_driver.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/axi_stream_design.tcl
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      270 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13098 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5635 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/example_models.py
--rw-r--r--   0 runner    (1001) docker     (123)     3979 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/fixed_point_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     8204 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/plot.py
--rw-r--r--   0 runner    (1001) docker     (123)      534 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/utils/string_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/hls4ml/writer/
--rw-r--r--   0 runner    (1001) docker     (123)      502 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    58247 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/quartus_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)      892 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/vitis_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)    22595 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/vivado_accelerator_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)    30570 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/vivado_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)      354 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/hls4ml/writer/writers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.055124 hls4ml-0.7.0rc1/hls4ml.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6035 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    19488 2023-04-15 01:45:10.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      126 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-04-15 01:45:09.000000 hls4ml-0.7.0rc1/hls4ml.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      438 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.083124 hls4ml-0.7.0rc1/scripts/
--rwxr-xr-x   0 runner    (1001) docker     (123)    12340 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/scripts/hls4ml
--rw-r--r--   0 runner    (1001) docker     (123)     1199 2023-04-15 01:45:10.091124 hls4ml-0.7.0rc1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.087124 hls4ml-0.7.0rc1/test/
--rwxr-xr-x   0 runner    (1001) docker     (123)     3301 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/build-prj.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     1039 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/cleanup.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     2945 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/compare-reports.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     2582 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/convert-keras-models.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     2161 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/convert-onnx-models.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     2168 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/convert-pytorch-models.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.087124 hls4ml-0.7.0rc1/test/docker/
--rw-r--r--   0 runner    (1001) docker     (123)     2668 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/docker/Dockerfile
--rw-r--r--   0 runner    (1001) docker     (123)     2963 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/docker/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/docker/install_config-2017.2.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/docker/install_config.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     1519 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/gather-reports.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     1049 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/hls4ml-keras-test.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     1145 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/hls4ml-onnx-test.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     1169 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/hls4ml-pytorch-test.sh
--rw-r--r--   0 runner    (1001) docker     (123)     1707 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/keras-models.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     4075 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/keras-to-hls.sh
--rw-r--r--   0 runner    (1001) docker     (123)      778 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/onnx-models.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     2349 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/onnx-to-hls.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.091124 hls4ml-0.7.0rc1/test/pytest/
--rw-r--r--   0 runner    (1001) docker     (123)      749 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/ci-template.yml
--rw-r--r--   0 runner    (1001) docker     (123)      775 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/generate_ci_yaml.py
--rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_activations.py
--rw-r--r--   0 runner    (1001) docker     (123)     1579 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_batchnorm.py
--rw-r--r--   0 runner    (1001) docker     (123)     1816 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_bram_factor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1199 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_causalpadding.py
--rw-r--r--   0 runner    (1001) docker     (123)     1708 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_clone_flatten.py
--rw-r--r--   0 runner    (1001) docker     (123)     3587 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_cnn_mnist.py
--rw-r--r--   0 runner    (1001) docker     (123)     3664 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_cnn_mnist_qkeras.py
--rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_conv1d.py
--rw-r--r--   0 runner    (1001) docker     (123)     1618 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_conv1d_narrow.py
--rw-r--r--   0 runner    (1001) docker     (123)     1627 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_conv2d_narrow.py
--rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_embed.py
--rw-r--r--   0 runner    (1001) docker     (123)     5212 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_extensions.py
--rw-r--r--   0 runner    (1001) docker     (123)     5556 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_flows.py
--rw-r--r--   0 runner    (1001) docker     (123)     1750 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_garnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4121 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_globalpooling.py
--rw-r--r--   0 runner    (1001) docker     (123)     9627 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_graph.py
--rw-r--r--   0 runner    (1001) docker     (123)    20432 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_keras_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_keras_h5_loader.py
--rw-r--r--   0 runner    (1001) docker     (123)     6100 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_merge.py
--rw-r--r--   0 runner    (1001) docker     (123)     4473 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_pointwiseconv.py
--rw-r--r--   0 runner    (1001) docker     (123)     4018 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_pooling.py
--rw-r--r--   0 runner    (1001) docker     (123)      816 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_precision_parsing.py
--rw-r--r--   0 runner    (1001) docker     (123)    13097 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_qkeras.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-15 01:45:10.091124 hls4ml-0.7.0rc1/test/pytest/test_report/
--rw-r--r--   0 runner    (1001) docker     (123)    13881 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_report/myproject_csynth.rpt
--rw-r--r--   0 runner    (1001) docker     (123)    21009 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_report/myproject_csynth.xml
--rw-r--r--   0 runner    (1001) docker     (123)      943 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_report/vivado_hls.app
--rw-r--r--   0 runner    (1001) docker     (123)     7230 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_report/vivado_synth.rpt
--rw-r--r--   0 runner    (1001) docker     (123)     2906 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_report.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1366 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_reshape.py
--rw-r--r--   0 runner    (1001) docker     (123)     5149 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_rnn.py
--rw-r--r--   0 runner    (1001) docker     (123)     2255 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_sepconv2d.py
--rw-r--r--   0 runner    (1001) docker     (123)     3656 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_softmax.py
--rw-r--r--   0 runner    (1001) docker     (123)     1264 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_softsign.py
--rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_trace.py
--rw-r--r--   0 runner    (1001) docker     (123)     1839 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_transpose_concat.py
--rw-r--r--   0 runner    (1001) docker     (123)     1912 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_upsampling.py
--rw-r--r--   0 runner    (1001) docker     (123)     1986 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytest/test_zeropadding.py
--rw-r--r--   0 runner    (1001) docker     (123)      616 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytorch-models.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     2351 2023-04-15 01:44:58.000000 hls4ml-0.7.0rc1/test/pytorch-to-hls.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.839324 hls4ml-0.7.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     5421 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.clang-format
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.783325 hls4ml-0.7.1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.783325 hls4ml-0.7.1/.github/ISSUE_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (123)     1520 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0 runner    (1001) docker     (123)      378 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/ISSUE_TEMPLATE/config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      990 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/PULL_REQUEST_TEMPLATE.md
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/dependabot.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.783325 hls4ml-0.7.1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1246 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/workflows/build-sphinx.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/workflows/pre-commit.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      693 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/workflows/pypi-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      692 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/workflows/test-sphinx.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      775 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.github/workflows/update-branch-on-pr.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1797 2023-05-13 15:56:45.000000 hls4ml-0.7.1/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1514 2023-05-13 15:56:45.000000 hls4ml-0.7.1/CITATION.cff
+-rw-r--r--   0 runner    (1001) docker     (123)     2810 2023-05-13 15:56:45.000000 hls4ml-0.7.1/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2719 2023-05-13 15:56:45.000000 hls4ml-0.7.1/Jenkinsfile
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 15:56:45.000000 hls4ml-0.7.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 15:56:45.000000 hls4ml-0.7.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     6029 2023-05-13 15:56:55.839324 hls4ml-0.7.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5260 2023-05-13 15:56:45.000000 hls4ml-0.7.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.783325 hls4ml-0.7.1/contrib/
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14507 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/garnet.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.783325 hls4ml-0.7.1/contrib/kl_layer/
+-rw-r--r--   0 runner    (1001) docker     (123)      537 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/kl_layer/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3367 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/kl_layer/kl_layer.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6006 2023-05-13 15:56:45.000000 hls4ml-0.7.1/contrib/kl_layer/kl_layer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.787325 hls4ml-0.7.1/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      678 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.787325 hls4ml-0.7.1/docs/advanced/
+-rw-r--r--   0 runner    (1001) docker     (123)     3922 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/advanced/accelerator.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6561 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/advanced/extension.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2985 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/advanced/fifo_depth.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.787325 hls4ml-0.7.1/docs/api/
+-rw-r--r--   0 runner    (1001) docker     (123)    10243 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/api/configuration.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2601 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/api/hls-model.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4666 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/api/profiling.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3832 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/command.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6176 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/concepts.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4090 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/details.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5798 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/flows.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.791324 hls4ml-0.7.1/docs/img/
+-rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/act_hls4ml.png
+-rw-r--r--   0 runner    (1001) docker     (123)    10406 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/act_keras.png
+-rw-r--r--   0 runner    (1001) docker     (123)    26453 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/hls4ml_logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)    21083 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/hls4ml_logo.svg
+-rw-r--r--   0 runner    (1001) docker     (123)    25377 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/hls4ml_logo_lightgrey.png
+-rw-r--r--   0 runner    (1001) docker     (123)    23796 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/hls4ml_logo_lightgrey.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     7506 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/hls4ml_logo_navbar.png
+-rw-r--r--   0 runner    (1001) docker     (123)    64144 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/logo.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)    23360 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)    98357 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/nn_map_paper_fig_2.png
+-rw-r--r--   0 runner    (1001) docker     (123)   202059 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/overview.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)   642072 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/overview.pdf
+-rw-r--r--   0 runner    (1001) docker     (123)   335589 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/pynqframe.png
+-rw-r--r--   0 runner    (1001) docker     (123)    82654 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/reuse_factor_paper_fig_8.png
+-rw-r--r--   0 runner    (1001) docker     (123)    10231 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/weights_hls4ml.png
+-rw-r--r--   0 runner    (1001) docker     (123)    10969 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/weights_keras.png
+-rw-r--r--   0 runner    (1001) docker     (123)    76029 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/img/zynq_interfaces.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1639 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/reference.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      271 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/release_notes.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      188 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     6390 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/setup.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2179 2023-05-13 15:56:45.000000 hls4ml-0.7.1/docs/status.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.791324 hls4ml-0.7.1/example-models/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/example-models/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.791324 hls4ml-0.7.1/example-models/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/.github/workflows/update-model-list.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/available_data_config.json
+-rw-r--r--   0 runner    (1001) docker     (123)      988 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/available_models.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.791324 hls4ml-0.7.1/example-models/config-files/
+-rw-r--r--   0 runner    (1001) docker     (123)      877 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/config-files/garnet_1layer_config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      949 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/config-files/garnet_3layer_config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/config-files/qkeras_3layer_config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1361 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/config-files/qkeras_mnist_cnn_config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/config-files/qkeras_mnist_dense_config.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.791324 hls4ml-0.7.1/example-models/data/
+-rw-r--r--   0 runner    (1001) docker     (123)  1188502 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/data/garnet_1layer_input.dat
+-rw-r--r--   0 runner    (1001) docker     (123)     2304 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/data/garnet_1layer_output.dat
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.803324 hls4ml-0.7.1/example-models/keras/
+-rw-r--r--   0 runner    (1001) docker     (123)     4042 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_1layer.json
+-rw-r--r--   0 runner    (1001) docker     (123)    13944 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_1layer_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     8084 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer.json
+-rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_70pruned_retrained_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_95pruned_retrained_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    15426 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_batch_norm.json
+-rw-r--r--   0 runner    (1001) docker     (123)    55224 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_batch_norm_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     9912 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_binary_smaller.json
+-rw-r--r--   0 runner    (1001) docker     (123)    52240 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_binary_smaller_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    11160 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_binarydense_relu_max.json
+-rw-r--r--   0 runner    (1001) docker     (123)    52224 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_binarydense_relu_max_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     9919 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_ternary_small.json
+-rw-r--r--   0 runner    (1001) docker     (123)    52240 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_ternary_small_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    36096 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_3layer_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    10545 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv1d.json
+-rw-r--r--   0 runner    (1001) docker     (123)    11331 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv1d_small.json
+-rw-r--r--   0 runner    (1001) docker     (123)    23232 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv1d_small_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)  1026808 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv1d_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     3342 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv2d_model.json
+-rw-r--r--   0 runner    (1001) docker     (123)    19904 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_conv2d_model_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    12760 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5.json
+-rw-r--r--   0 runner    (1001) docker     (123)   197336 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    13774 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5.json
+-rw-r--r--   0 runner    (1001) docker     (123)   690872 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    12760 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5.json
+-rw-r--r--   0 runner    (1001) docker     (123)  4080168 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/garnet_1layer.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20144 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/garnet_1layer_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     3004 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/garnet_3layer.json
+-rw-r--r--   0 runner    (1001) docker     (123)    42488 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/garnet_3layer_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     4950 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small.json
+-rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm.json
+-rw-r--r--   0 runner    (1001) docker     (123)    25392 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)    32528 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     5429 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/keras_bnn.json
+-rw-r--r--   0 runner    (1001) docker     (123)    71320 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/keras_bnn_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     6981 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_3layer.json
+-rw-r--r--   0 runner    (1001) docker     (123)    38344 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_3layer_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     6020 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_mnist_cnn.json
+-rw-r--r--   0 runner    (1001) docker     (123)    47424 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_mnist_cnn_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)     8220 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_mnist_dense.json
+-rw-r--r--   0 runner    (1001) docker     (123)    79416 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras/qkeras_mnist_dense_weights.h5
+-rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/keras-config.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.803324 hls4ml-0.7.1/example-models/onnx/
+-rw-r--r--   0 runner    (1001) docker     (123)     2931 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/conv1d_small_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)     6593 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/conv2d_small_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)     4757 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/conv2d_small_mp_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)   172539 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/dense_big_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)    23520 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/three_layer_bn_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)    42287 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/three_layer_bn_pytorch.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)    18824 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/three_layer_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)    32007 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/three_layer_pytorch.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)     2242 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/two_layer_keras.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)     8688 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx/two_layer_pytorch.onnx
+-rw-r--r--   0 runner    (1001) docker     (123)      460 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/onnx-config.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.803324 hls4ml-0.7.1/example-models/pytorch/
+-rw-r--r--   0 runner    (1001) docker     (123)    26028 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/pytorch/three_layer_model.pt
+-rw-r--r--   0 runner    (1001) docker     (123)     8356 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/pytorch/two_layer_model.pt
+-rw-r--r--   0 runner    (1001) docker     (123)      465 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/pytorch-config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/scan.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.803324 hls4ml-0.7.1/example-models/tensorflow/
+-rw-r--r--   0 runner    (1001) docker     (123)    19927 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/tensorflow/3layer.pb
+-rw-r--r--   0 runner    (1001) docker     (123)      475 2023-05-13 15:56:46.000000 hls4ml-0.7.1/example-models/tf-config.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.803324 hls4ml-0.7.1/hls4ml/
+-rw-r--r--   0 runner    (1001) docker     (123)      611 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/
+-rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6207 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/backend.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/fpga/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31806 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/fpga_backend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3311 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/fpga_layers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15575 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/fpga_types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/fpga/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7404 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/bn_quant.py
+-rw-r--r--   0 runner    (1001) docker     (123)      633 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/bram_weights.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/clone.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/codegen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1348 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/embedding.py
+-rw-r--r--   0 runner    (1001) docker     (123)      952 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/final_reshape.py
+-rw-r--r--   0 runner    (1001) docker     (123)      821 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/inplace_parallel_reshape.py
+-rw-r--r--   0 runner    (1001) docker     (123)      957 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/inplace_stream_flatten.py
+-rw-r--r--   0 runner    (1001) docker     (123)      412 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/remove_softmax.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2079 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/fpga/passes/repack_stream.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/quartus/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/quartus/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7592 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/convolution_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9303 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/convolution_winograd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8717 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/core_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4077 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/merge_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3651 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/pointwise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4533 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/pooling_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/quantization_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13910 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/recurrent_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4962 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/reshaping_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4005 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/resource_strategy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/passes/transform_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15528 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/quartus/quartus_backend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2553 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/template.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/vitis/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vitis/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml/backends/vitis/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vitis/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vitis/passes/feature_check.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vitis/vitis_backend.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/backends/vivado/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/backends/vivado/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4554 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/broadcast_stream.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3997 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/conv_same_pad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2405 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/conv_stream.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20889 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/convolution_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8426 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/core_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3740 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/fifo_depth_optimization.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11959 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/garnet_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3855 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/merge_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/pointwise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4728 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/pooling_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1320 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/quantization_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8306 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/recurrent_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4742 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/reshaping_templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/resource_strategy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/passes/transform_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18429 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado/vivado_backend.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2938 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/passes/fifo_depth_optimization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1448 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/supported_boards.json
+-rw-r--r--   0 runner    (1001) docker     (123)     6624 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/vivado_accelerator_backend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/vivado_accelerator_config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/converters/
+-rw-r--r--   0 runner    (1001) docker     (123)    14004 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.811324 hls4ml-0.7.1/hls4ml/converters/keras/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2790 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/convolution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4442 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2141 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4130 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/pooling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6535 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/qkeras.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1475 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/recurrent.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3236 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/reshape.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3590 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras/reshaping.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11658 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/keras_to_hls.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/converters/onnx/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3012 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/convolution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4011 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/pooling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1389 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx/reshape.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10787 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/onnx_to_hls.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/converters/pytorch/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/pytorch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3176 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/pytorch/convolution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2388 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/pytorch/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6191 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/pytorch_to_hls.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14698 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/tf_to_hls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5647 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/converters/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/model/
+-rw-r--r--   0 runner    (1001) docker     (123)      214 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8366 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/attributes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/model/flow/
+-rw-r--r--   0 runner    (1001) docker     (123)      161 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/flow/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4466 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/flow/flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33950 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)    52349 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/layers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/model/optimizer/
+-rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9493 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/optimizer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/model/optimizer/passes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1469 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/bn_fuse.py
+-rw-r--r--   0 runner    (1001) docker     (123)      618 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/fuse_biasadd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2568 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/multi_dense.py
+-rw-r--r--   0 runner    (1001) docker     (123)      528 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/nop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/precision_merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11642 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/qkeras.py
+-rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/stamp.py
+-rw-r--r--   0 runner    (1001) docker     (123)      815 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/optimizer/passes/transpose_opt.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24047 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/profiling.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22808 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/model/types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/report/
+-rw-r--r--   0 runner    (1001) docker     (123)      372 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/report/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9341 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/report/quartus_report.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25795 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/report/vivado_report.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/hls4ml/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.815324 hls4ml-0.7.1/hls4ml/templates/quartus/
+-rw-r--r--   0 runner    (1001) docker     (123)      798 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.819324 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/
+-rw-r--r--   0 runner    (1001) docker     (123)    18367 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_channel.h
+-rw-r--r--   0 runner    (1001) docker     (123)    16534 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_complex.h
+-rw-r--r--   0 runner    (1001) docker     (123)    59595 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_fixed.h
+-rw-r--r--   0 runner    (1001) docker     (123)    44867 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_float.h
+-rw-r--r--   0 runner    (1001) docker     (123)   105429 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_int.h
+-rw-r--r--   0 runner    (1001) docker     (123)    17449 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_sc.h
+-rw-r--r--   0 runner    (1001) docker     (123)    84637 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_std_float.h
+-rw-r--r--   0 runner    (1001) docker     (123)      791 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/stream.h
+-rwxr-xr-x   0 runner    (1001) docker     (123)      551 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/build_lib.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.819324 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/
+-rw-r--r--   0 runner    (1001) docker     (123)     1382 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/defines.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/myproject.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/myproject.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.823324 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)    18055 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation.h
+-rw-r--r--   0 runner    (1001) docker     (123)    23323 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3487 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3464 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1946 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_common.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2245 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10544 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     7594 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2731 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d.h
+-rw-r--r--   0 runner    (1001) docker     (123)    14958 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10556 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     7012 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_compressed.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1259 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed.h
+-rw-r--r--   0 runner    (1001) docker     (123)      700 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5023 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_helpers.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11047 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11820 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4074 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_mult.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2186 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12470 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12279 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    25143 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1805 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_activation.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2025 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1223 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3191 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose.h
+-rw-r--r--   0 runner    (1001) docker     (123)      963 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_types.h
+-rw-r--r--   0 runner    (1001) docker     (123)      207 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/firmware/parameters.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/myproject_bridge.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3611 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/myproject_test_parallel.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3914 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/quartus/myproject_test_stream.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/hls4ml/templates/vitis/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.823324 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)     4040 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4168 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3572 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9671 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_dense_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_dense_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    15306 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_pooling.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12369 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_pooling_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4246 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv1d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6188 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv2d_stream.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.823324 hls4ml-0.7.1/hls4ml/templates/vivado/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.823324 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/
+-rw-r--r--   0 runner    (1001) docker     (123)    10180 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_common.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6473 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_decl.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12185 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed.h
+-rw-r--r--   0 runner    (1001) docker     (123)    85182 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_base.h
+-rw-r--r--   0 runner    (1001) docker     (123)    27302 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_ref.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6985 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_special.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10012 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int.h
+-rw-r--r--   0 runner    (1001) docker     (123)    71735 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_base.h
+-rw-r--r--   0 runner    (1001) docker     (123)    55218 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_ref.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6301 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_special.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4894 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_shift_reg.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.823324 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/etc/
+-rw-r--r--   0 runner    (1001) docker     (123)   261465 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/etc/ap_private.h
+-rw-r--r--   0 runner    (1001) docker     (123)      194 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/hls_math.h
+-rw-r--r--   0 runner    (1001) docker     (123)     7480 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/hls_stream.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.827324 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)     2227 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/utils/x_hls_utils.h
+-rwxr-xr-x   0 runner    (1001) docker     (123)      530 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/build_lib.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     7812 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/build_prj.tcl
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.827324 hls4ml-0.7.1/hls4ml/templates/vivado/firmware/
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/firmware/defines.h
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/firmware/myproject.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/firmware/myproject.h
+-rw-r--r--   0 runner    (1001) docker     (123)      311 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/firmware/parameters.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/myproject_bridge.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2749 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/myproject_test.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)    28377 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_activation.h
+-rw-r--r--   0 runner    (1001) docker     (123)    26176 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_activation_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1724 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_array.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4213 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3828 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)      937 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_code_gen.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2058 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_common.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2416 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3219 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_latency.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3879 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3717 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2755 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3257 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_latency.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4007 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5131 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    14664 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2859 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_compressed.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2424 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_latency.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9970 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_resource.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2318 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_embed.h
+-rw-r--r--   0 runner    (1001) docker     (123)      839 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_embed_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    30731 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_garnet.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12524 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_helpers.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_image.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1847 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_image_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10964 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_merge.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11628 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_merge_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3703 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_mult.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_padding.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2191 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_padding_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    15287 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_pooling.h
+-rw-r--r--   0 runner    (1001) docker     (123)    23670 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_pooling_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1889 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_recr_activations.h
+-rw-r--r--   0 runner    (1001) docker     (123)    27031 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_recurrent.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5310 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv1d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6697 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv2d_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11307 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6882 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_stream.h
+-rw-r--r--   0 runner    (1001) docker     (123)      724 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_types.h
+-rw-r--r--   0 runner    (1001) docker     (123)      217 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado/vivado_synth.tcl
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/
+-rw-r--r--   0 runner    (1001) docker     (123)    11385 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_read_master.sv
+-rw-r--r--   0 runner    (1001) docker     (123)     9883 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_write_master.sv
+-rw-r--r--   0 runner    (1001) docker     (123)    12999 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_control_s_axi.v
+-rw-r--r--   0 runner    (1001) docker     (123)     2414 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_counter.sv
+-rw-r--r--   0 runner    (1001) docker     (123)    18061 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_int.sv
+-rw-r--r--   0 runner    (1001) docker     (123)     8472 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/myproject_kernel.v
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/
+-rw-r--r--   0 runner    (1001) docker     (123)     4885 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/axi_stream_driver.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)     9028 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/axi_stream_design.tcl
+-rw-r--r--   0 runner    (1001) docker     (123)      617 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/build_lib.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/myproject_axi.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)      239 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/myproject_axi.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/
+-rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/axi_stream_driver.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)     1533 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_lite_design.tcl
+-rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_stream_design.tcl
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.779324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/
+-rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/axi_stream_driver.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/axi_stream_design.tcl
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      270 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13097 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5635 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/example_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3979 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/fixed_point_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8204 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/utils/string_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/hls4ml/writer/
+-rw-r--r--   0 runner    (1001) docker     (123)      502 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    58271 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/quartus_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      892 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/vitis_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22595 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/vivado_accelerator_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30570 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/vivado_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      354 2023-05-13 15:56:45.000000 hls4ml-0.7.1/hls4ml/writer/writers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.807325 hls4ml-0.7.1/hls4ml.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6029 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    19519 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      126 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-05-13 15:56:55.000000 hls4ml-0.7.1/hls4ml.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      438 2023-05-13 15:56:45.000000 hls4ml-0.7.1/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.831324 hls4ml-0.7.1/scripts/
+-rwxr-xr-x   0 runner    (1001) docker     (123)    12340 2023-05-13 15:56:45.000000 hls4ml-0.7.1/scripts/hls4ml
+-rw-r--r--   0 runner    (1001) docker     (123)     1199 2023-05-13 15:56:55.839324 hls4ml-0.7.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 15:56:45.000000 hls4ml-0.7.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.835324 hls4ml-0.7.1/test/
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3301 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/build-prj.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1039 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/cleanup.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2945 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/compare-reports.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2582 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/convert-keras-models.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2161 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/convert-onnx-models.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2168 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/convert-pytorch-models.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.835324 hls4ml-0.7.1/test/docker/
+-rw-r--r--   0 runner    (1001) docker     (123)     2668 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/docker/Dockerfile
+-rw-r--r--   0 runner    (1001) docker     (123)     2963 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/docker/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/docker/install_config-2017.2.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/docker/install_config.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1519 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/gather-reports.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1049 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/hls4ml-keras-test.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1145 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/hls4ml-onnx-test.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1169 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/hls4ml-pytorch-test.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     1707 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/keras-models.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4075 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/keras-to-hls.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      778 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/onnx-models.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2349 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/onnx-to-hls.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.839324 hls4ml-0.7.1/test/pytest/
+-rw-r--r--   0 runner    (1001) docker     (123)      749 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/ci-template.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      775 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/generate_ci_yaml.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_activations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1579 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_batchnorm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2875 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_binary_cnn.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1816 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_bram_factor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1199 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_causalpadding.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1708 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_clone_flatten.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3587 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_cnn_mnist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3664 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_cnn_mnist_qkeras.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_conv1d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1618 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_conv1d_narrow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1627 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_conv2d_narrow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_embed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5212 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_extensions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5556 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_flows.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1750 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_garnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4121 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_globalpooling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9627 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20432 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_keras_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_keras_h5_loader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6100 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_merge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5439 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_pointwiseconv.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4018 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_pooling.py
+-rw-r--r--   0 runner    (1001) docker     (123)      816 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_precision_parsing.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13097 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_qkeras.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:56:55.839324 hls4ml-0.7.1/test/pytest/test_report/
+-rw-r--r--   0 runner    (1001) docker     (123)    13881 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_report/myproject_csynth.rpt
+-rw-r--r--   0 runner    (1001) docker     (123)    21009 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_report/myproject_csynth.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      943 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_report/vivado_hls.app
+-rw-r--r--   0 runner    (1001) docker     (123)     7230 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_report/vivado_synth.rpt
+-rw-r--r--   0 runner    (1001) docker     (123)     2906 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_report.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1366 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_reshape.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5297 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_rnn.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2255 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_sepconv2d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3656 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_softmax.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1264 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_softsign.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1776 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_trace.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1839 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_transpose_concat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1912 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_upsampling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1986 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytest/test_zeropadding.py
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytorch-models.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2351 2023-05-13 15:56:45.000000 hls4ml-0.7.1/test/pytorch-to-hls.sh
```

### Comparing `hls4ml-0.7.0rc1/.clang-format` & `hls4ml-0.7.1/.clang-format`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/bug_report.md` & `hls4ml-0.7.1/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/ISSUE_TEMPLATE/feature_request.md` & `hls4ml-0.7.1/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/PULL_REQUEST_TEMPLATE.md` & `hls4ml-0.7.1/.github/PULL_REQUEST_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/workflows/build-sphinx.yml` & `hls4ml-0.7.1/.github/workflows/build-sphinx.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/workflows/pypi-publish.yml` & `hls4ml-0.7.1/.github/workflows/pypi-publish.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/workflows/test-sphinx.yml` & `hls4ml-0.7.1/.github/workflows/test-sphinx.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.github/workflows/update-branch-on-pr.yml` & `hls4ml-0.7.1/.github/workflows/update-branch-on-pr.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/.pre-commit-config.yaml` & `hls4ml-0.7.1/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/CITATION.cff` & `hls4ml-0.7.1/CITATION.cff`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 cff-version: 1.2.0
 message: "Please cite the following works when using this software."
 type: software
 authors:
 - given-names: "FastML Team"
 title: "hls4ml"
-version: "v0.7.0rc1"
+version: "v0.7.1"
 doi: 10.5281/zenodo.1201549
 repository-code: "https://github.com/fastmachinelearning/hls4ml"
 url: "https://fastmachinelearning.org/hls4ml"
 keywords:
   - python
   - machine-learning
   - FPGA
```

### Comparing `hls4ml-0.7.0rc1/CONTRIBUTING.md` & `hls4ml-0.7.1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/Jenkinsfile` & `hls4ml-0.7.1/Jenkinsfile`

 * *Files 0% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 pipeline {
   agent {
     docker {
-      image 'vivado-el7:2'
+      image 'vivado-el7:3'
       args  '-v /data/Xilinx:/data/Xilinx'
     }
   }
   options {
     timeout(time: 6, unit: 'HOURS')
   }
 
   stages {
     stage('Keras to HLS') {
       steps {
         dir(path: 'test') {
           sh '''#!/bin/bash --login
-              conda activate hls4ml-py37
+              conda activate hls4ml-py38
               pip install tensorflow pyparsing
               pip install -U ../ --user
               ./convert-keras-models.sh -x -f keras-models.txt
               pip uninstall hls4ml -y'''
         }
       }
     }
```

### Comparing `hls4ml-0.7.0rc1/LICENSE` & `hls4ml-0.7.1/LICENSE`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/PKG-INFO` & `hls4ml-0.7.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hls4ml
-Version: 0.7.0rc1
+Version: 0.7.1
 Summary: Machine learning in FPGAs using HLS
 Home-page: https://fastmachinelearning.org/hls4ml
 Author: hls4ml Team
 License: Apache-2.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
@@ -86,15 +86,15 @@
 If you use this software in a publication, please cite the software
 ```bibtex
 @software{fastml_hls4ml,
   author       = {{FastML Team}},
   title        = {fastmachinelearning/hls4ml},
   year         = 2023,
   publisher    = {Zenodo},
-  version      = {v0.7.0rc1},
+  version      = {v0.7.1},
   doi          = {10.5281/zenodo.1201549},
   url          = {https://github.com/fastmachinelearning/hls4ml}
 }
 ```
 and first publication:
 ```bibtex
 @article{Duarte:2018ite,
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
-Metadata-Version: 2.1 Name: hls4ml Version: 0.7.0rc1 Summary: Machine learning
-in FPGAs using HLS Home-page: https://fastmachinelearning.org/hls4ml Author:
+Metadata-Version: 2.1 Name: hls4ml Version: 0.7.1 Summary: Machine learning in
+FPGAs using HLS Home-page: https://fastmachinelearning.org/hls4ml Author:
 hls4ml Team License: Apache-2.0 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers Classifier: Intended Audience ::
 Science/Research Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: C++ Classifier: Programming Language ::
 Python :: 3 Classifier: Programming Language :: Python :: 3 :: Only Classifier:
 Topic :: Software Development :: Libraries Classifier: Topic :: Software
 Development :: Libraries :: Python Modules Requires-Python: >=3.7 Description-
@@ -42,15 +42,15 @@
 products/design-tools/vivado/integration/esl-design.html)) Note: Vitis HLS is
 not yet supported. Vivado HLS versions between 2018.2 and 2020.1 are
 recommended. ```Python # Use Vivado HLS to synthesize the model # This might
 take several minutes hls_model.build() # Print out the report if you want
 hls4ml.report.read_vivado_report('my-hls-test') ``` # Citation If you use this
 software in a publication, please cite the software ```bibtex @software
 {fastml_hls4ml, author = {{FastML Team}}, title = {fastmachinelearning/hls4ml},
-year = 2023, publisher = {Zenodo}, version = {v0.7.0rc1}, doi = {10.5281/
+year = 2023, publisher = {Zenodo}, version = {v0.7.1}, doi = {10.5281/
 zenodo.1201549}, url = {https://github.com/fastmachinelearning/hls4ml} } ```
 and first publication: ```bibtex @article{Duarte:2018ite, author = "Duarte,
 Javier and others", title = "{Fast inference of deep neural networks in FPGAs
 for particle physics}", eprint = "1804.06913", archivePrefix = "arXiv",
 primaryClass = "physics.ins-det", reportNumber = "FERMILAB-PUB-18-089-E", doi =
 "10.1088/1748-0221/13/07/P07027", journal = "JINST", volume = "13", number =
 "07", pages = "P07027", year = "2018" } ``` Additionally, if you use specific
```

### Comparing `hls4ml-0.7.0rc1/README.md` & `hls4ml-0.7.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -65,15 +65,15 @@
 If you use this software in a publication, please cite the software
 ```bibtex
 @software{fastml_hls4ml,
   author       = {{FastML Team}},
   title        = {fastmachinelearning/hls4ml},
   year         = 2023,
   publisher    = {Zenodo},
-  version      = {v0.7.0rc1},
+  version      = {v0.7.1},
   doi          = {10.5281/zenodo.1201549},
   url          = {https://github.com/fastmachinelearning/hls4ml}
 }
 ```
 and first publication:
 ```bibtex
 @article{Duarte:2018ite,
```

#### html2text {}

```diff
@@ -32,15 +32,15 @@
 products/design-tools/vivado/integration/esl-design.html)) Note: Vitis HLS is
 not yet supported. Vivado HLS versions between 2018.2 and 2020.1 are
 recommended. ```Python # Use Vivado HLS to synthesize the model # This might
 take several minutes hls_model.build() # Print out the report if you want
 hls4ml.report.read_vivado_report('my-hls-test') ``` # Citation If you use this
 software in a publication, please cite the software ```bibtex @software
 {fastml_hls4ml, author = {{FastML Team}}, title = {fastmachinelearning/hls4ml},
-year = 2023, publisher = {Zenodo}, version = {v0.7.0rc1}, doi = {10.5281/
+year = 2023, publisher = {Zenodo}, version = {v0.7.1}, doi = {10.5281/
 zenodo.1201549}, url = {https://github.com/fastmachinelearning/hls4ml} } ```
 and first publication: ```bibtex @article{Duarte:2018ite, author = "Duarte,
 Javier and others", title = "{Fast inference of deep neural networks in FPGAs
 for particle physics}", eprint = "1804.06913", archivePrefix = "arXiv",
 primaryClass = "physics.ins-det", reportNumber = "FERMILAB-PUB-18-089-E", doi =
 "10.1088/1748-0221/13/07/P07027", journal = "JINST", volume = "13", number =
 "07", pages = "P07027", year = "2018" } ``` Additionally, if you use specific
```

### Comparing `hls4ml-0.7.0rc1/contrib/README.md` & `hls4ml-0.7.1/contrib/README.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/contrib/garnet.py` & `hls4ml-0.7.1/contrib/garnet.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/contrib/kl_layer/README.md` & `hls4ml-0.7.1/contrib/kl_layer/README.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/contrib/kl_layer/kl_layer.h` & `hls4ml-0.7.1/contrib/kl_layer/kl_layer.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/contrib/kl_layer/kl_layer.py` & `hls4ml-0.7.1/contrib/kl_layer/kl_layer.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/Makefile` & `hls4ml-0.7.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/advanced/accelerator.rst` & `hls4ml-0.7.1/docs/advanced/accelerator.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/advanced/extension.rst` & `hls4ml-0.7.1/docs/advanced/extension.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/advanced/fifo_depth.rst` & `hls4ml-0.7.1/docs/advanced/fifo_depth.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/api/configuration.rst` & `hls4ml-0.7.1/docs/api/configuration.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/api/hls-model.rst` & `hls4ml-0.7.1/docs/api/hls-model.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/api/profiling.rst` & `hls4ml-0.7.1/docs/api/profiling.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/command.rst` & `hls4ml-0.7.1/docs/command.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/concepts.rst` & `hls4ml-0.7.1/docs/concepts.rst`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/conf.py` & `hls4ml-0.7.1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/details.rst` & `hls4ml-0.7.1/docs/details.rst`

 * *Files 11% similar despite different names*

```diff
@@ -1,16 +1,18 @@
-======================
-Backends and I/O Types
-======================
+================
+Software Details
+================
 
-Backends
---------
+Frontends and Backends
+----------------------
 
-``hls4ml`` supports the concept of a *backend* that determines the target HLS language.
-Currently, Vivado HLS, Intel HLS, and Vitis HLS (experimental) are supported.
+In ``hls4ml`` there is a a concept of a *frontend* to parse the input NN into an internal model graph, and a *backend* that controls
+what type of output is produced from the graph. Frontends and backends can be independently chosen. Examples of frontends are the
+parsers for Keras or ONNX, and examples of backends are Vivado HLS, Intel HLS, and Vitis HLS. See :ref:`Status and Features` for the
+currently supported frontends and backends.
 
 I/O Types
 ---------
 
 ``hls4ml`` supports multiple styles for handling data between layers, known as the ``io_type``.
 
 io_parallel
```

### Comparing `hls4ml-0.7.0rc1/docs/flows.rst` & `hls4ml-0.7.1/docs/flows.rst`

 * *Files 10% similar despite different names*

```diff
@@ -1,31 +1,36 @@
 ==========================
 Optimizer Passes and Flows
 ==========================
 
+Internal Structure
+------------------
+
 The ``hls4ml`` library will parse models from Keras, PyTorch or ONNX into an internal execution graph. This model graph is represented with the
 :py:class:`~hls4ml.model.graph.ModelGraph` class. The nodes in this graph, corresponding to the layer and operations of the input model are represented
 by classes derived from the :py:class:`~hls4ml.model.layers.Layer` base class.
 
 Layers are required to have defined inputs and outputs that define how they are connected in the graph and what is the shape of their output. All information
 about the layer's state and configuration is stored in its attributes. All weights, variables and data types are attributes and there are mapping views to sort through them.
 Layers can define expected attributes and can be verified for correctness, or to produce a list of configurable attributes that user can tweak.
 
 Optimizer passes
 ----------------
 
-To reach a state from which the code can be generated, internal model graph will undergo a series of optimizations (transformations), dubbed *optimization passes*.
-All transformations of the model and any modification to any layer's attributes must be implemented through an optimization pass. All optimizer passes derive from
-the :py:class:`~hls4ml.model.optimizer.optimizer.OptimizerPass` class. Optimizer passes are applied at the level of nodes/layers, however a special class
-:py:class:`~hls4ml.model.optimizer.optimizer.ModelOptimizerPass` exists that is applied on the full model. Subclasses of
-:py:class:`~hls4ml.model.optimizer.optimizer.OptimizerPass` must provide a criteria in ``match`` function that, if satisfied, will perform the transformation from
-``transform`` function. The boolean return value of ``transform`` indicates if the optimizer pass made changes to the model graph, requiring running the optimizers again.
-Example of an optimizer pass that runs on the full model, is :py:class:`~hls4ml.model.optimizer.passes.stamp.MakeStamp`, while an example of the layer optimizer is
-:py:class:`~hls4ml.model.optimizer.passes.fuse_biasadd` class that adds a bias to a :py:class:`~hls4ml.model.layers.Dense`,
-:py:class:`~hls4ml.model.layers.Conv1D`, or :py:class:`~hls4ml.model.layers.Conv2D` layer.
+To reach a state from which the code can be generated, the internal model graph undergoes a series of optimizations (transformations), dubbed
+*optimization passes*. All transformations of the model and any modification to any layer's attributes must be implemented through an optimization
+pass. All optimizer passes derive from the :py:class:`~hls4ml.model.optimizer.optimizer.OptimizerPass` class. Optimizer passes are usually applied to
+nodes/layers; however, a special class :py:class:`~hls4ml.model.optimizer.optimizer.ModelOptimizerPass` exists that is applied on the full model. An
+example of a layer optimizer is :py:class:`~hls4ml.model.optimizer.passes.fuse_biasadd`, which adds a bias to a
+:py:class:`~hls4ml.model.layers.Dense`, :py:class:`~hls4ml.model.layers.Conv1D`, or :py:class:`~hls4ml.model.layers.Conv2D` layer, while an example of
+an optimizer pass that runs on the full model is :py:class:`~hls4ml.model.optimizer.passes.stamp.MakeStamp`, which creates a unique number (stamp).
+
+Subclasses of :py:class:`~hls4ml.model.optimizer.optimizer.OptimizerPass` must provide a criteria in ``match`` function that, if satisfied, will
+perform the transformation from ``transform`` function. The boolean return value of ``transform`` indicates if the optimizer pass made changes to the
+model graph that may require running the optimizers again. In that case, optimizers in a flow are run again.
 
 Optimizers can be general, independent of the backend, in which case they are located in :py:mod:`hls4ml.model.optimizer.passes`, or they may be backend-specific,
 in which case they are located in a folder dependent on the backend, e.g., :py:mod:`hls4ml.backends.vivado.passes` or
 :py:mod:`hls4ml.backends.quartus.passes`. A common set of optimizers that are used by FPGA backends are located in :py:mod:`hls4ml.backends.fpga.passes`.
 
 Certain optimizers are used frequently enough that it makes sense to define special classes, which inherit from :py:class:`~hls4ml.model.optimizer.optimizer.OptimizerPass`
 
@@ -40,18 +45,19 @@
 Note that :py:class:`~hls4ml.model.optimizer.optimizer.LayerOptimizerPass` and :py:class:`~hls4ml.model.optimizer.optimizer.ModelOptimizerPass`
 also exist as decorators that wrap a function.
 
 New optimizers can be registered with the :py:func:`~hls4ml.model.optimizer.optimizer.register_pass`. Optimizers should be assigned to a flow (see below).
 
 Flows
 -----
-A :py:class:`~hls4ml.model.flow.flow.Flow` is an ordered set of optimizers that represent a single stage in the conversion process. The optimizers from a flow are applied
-until they no longer make changes to the model graph after which the next flow (stage) can start. Flows may depend on other flows being applied before them,
-ensuring the model graph is in a desired state before a flow starts. The function :py:func:`~hls4ml.model.flow.flow.register_flow` is used to register a new flow. Flows
-are applied on a model graph with :py:func:`~hls4ml.model.graph.ModelGraph.apply_flow`.
+A :py:class:`~hls4ml.model.flow.flow.Flow` is an ordered set of optimizers that represents a single stage in the conversion process. The optimizers
+from a flow are applied in sequence until they no longer make changes to the model graph (controlled by the ``transform`` return value), after which
+the next flow (stage) can start. Flows may require that other flows are applied before them, ensuring the model graph is in a desired state before a
+flow starts. The function :py:func:`~hls4ml.model.flow.flow.register_flow` is used to register a new flow. Flows are applied on a model graph with
+:py:func:`~hls4ml.model.graph.ModelGraph.apply_flow`.
 
 There are common model-level flows that can run regardless of the backend, and there are backend-specific flows.
 The `convert and optimize <https://github.com/fastmachinelearning/hls4ml/blob/7c0a065935904f50bd7e4c547f85354b36276092/hls4ml/model/optimizer/__init__.py#L14-L20>`_
 flows do not depend on a backend.
 
 Each backend provides provides a default flow that defines the default target for that backend. For example, the Vivado backend defaults to an
 `IP flow <https://github.com/fastmachinelearning/hls4ml/blob/7c0a065935904f50bd7e4c547f85354b36276092/hls4ml/backends/vivado/vivado_backend.py#L148-L160>`_
```

### Comparing `hls4ml-0.7.0rc1/docs/img/act_hls4ml.png` & `hls4ml-0.7.1/docs/img/act_hls4ml.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/act_keras.png` & `hls4ml-0.7.1/docs/img/act_keras.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/hls4ml_logo.png` & `hls4ml-0.7.1/docs/img/hls4ml_logo.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/hls4ml_logo.svg` & `hls4ml-0.7.1/docs/img/hls4ml_logo.svg`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/hls4ml_logo_lightgrey.png` & `hls4ml-0.7.1/docs/img/hls4ml_logo_lightgrey.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/hls4ml_logo_lightgrey.svg` & `hls4ml-0.7.1/docs/img/hls4ml_logo_lightgrey.svg`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/hls4ml_logo_navbar.png` & `hls4ml-0.7.1/docs/img/hls4ml_logo_navbar.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/logo.jpg` & `hls4ml-0.7.1/docs/img/logo.jpg`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/logo.png` & `hls4ml-0.7.1/docs/img/logo.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/nn_map_paper_fig_2.png` & `hls4ml-0.7.1/docs/img/nn_map_paper_fig_2.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/overview.jpg` & `hls4ml-0.7.1/docs/img/overview.jpg`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/overview.pdf` & `hls4ml-0.7.1/docs/img/overview.pdf`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/pynqframe.png` & `hls4ml-0.7.1/docs/img/pynqframe.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/reuse_factor_paper_fig_8.png` & `hls4ml-0.7.1/docs/img/reuse_factor_paper_fig_8.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/weights_hls4ml.png` & `hls4ml-0.7.1/docs/img/weights_hls4ml.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/weights_keras.png` & `hls4ml-0.7.1/docs/img/weights_keras.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/img/zynq_interfaces.png` & `hls4ml-0.7.1/docs/img/zynq_interfaces.png`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/docs/index.rst` & `hls4ml-0.7.1/docs/index.rst`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -2,17 +2,17 @@
     :hidden:
     :caption: Introduction
 
     concepts
     status
     setup
     release_notes
-    command
     details
     flows
+    command
     reference
 
 .. toctree::
     :hidden:
     :glob:
     :caption: Quick API Reference
```

### Comparing `hls4ml-0.7.0rc1/docs/reference.rst` & `hls4ml-0.7.1/docs/reference.rst`

 * *Files 0% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 ..  code-block:: bibtex
 
     @software{fastml_hls4ml,
     author       = {{FastML Team}},
     title        = {fastmachinelearning/hls4ml},
     year         = 2023,
     publisher    = {Zenodo},
-    version      = {v0.7.0rc1},
+    version      = {v0.7.1},
     doi          = {10.5281/zenodo.1201549},
     url          = {https://github.com/fastmachinelearning/hls4ml}
     }
 
 and first publication:
 
 ..  code-block:: bibtex
```

### Comparing `hls4ml-0.7.0rc1/docs/setup.rst` & `hls4ml-0.7.1/docs/setup.rst`

 * *Files 2% similar despite different names*

```diff
@@ -18,14 +18,17 @@
 
 .. code-block::
 
    pip install hls4ml[profiling]
 
 ``hls4ml`` is also available as a ``conda`` package in the ``conda-forge`` repository. To install, run:
 
+.. warning::
+   Version of hls4ml available on ``conda-forge`` is outdated, we recommend installing with ``pip`` to get the latest version.
+
 .. code-block::
 
    conda install -c conda-forge hls4ml
 
 Development version
 -------------------
```

### Comparing `hls4ml-0.7.0rc1/docs/status.rst` & `hls4ml-0.7.1/docs/status.rst`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 ===================
 Status and Features
 ===================
 
 Status
-========
+======
 
 The latest version (built from ``main``) is |version|.
 The stable version (released on PyPI) is |release|.
 See the :ref:`Release Notes` section for a changelog.
 
 
 Features
@@ -45,22 +45,22 @@
      - (Q)ONNX
      - Vivado HLS
      - Intel HLS
      - Vitis HLS
    * - MLP
      - ``supported``
      - ``limited``
-     - ``supported``
+     - ``in development``
      - ``supported``
      - ``supported``
      - ``experimental``
    * - CNN
      - ``supported``
      - ``limited``
-     - ``supported``
+     - ``in development``
      - ``supported``
      - ``supported``
      - ``experimental``
    * - RNN (LSTM)
      - ``supported``
      - ``N/A``
      - ``in development``
```

### Comparing `hls4ml-0.7.0rc1/example-models/.github/workflows/update-model-list.yml` & `hls4ml-0.7.1/example-models/.github/workflows/update-model-list.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/available_data_config.json` & `hls4ml-0.7.1/example-models/available_data_config.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/available_models.json` & `hls4ml-0.7.1/example-models/available_models.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/config-files/garnet_1layer_config.yml` & `hls4ml-0.7.1/example-models/config-files/garnet_1layer_config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/config-files/garnet_3layer_config.yml` & `hls4ml-0.7.1/example-models/config-files/garnet_3layer_config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/config-files/qkeras_3layer_config.yml` & `hls4ml-0.7.1/example-models/config-files/qkeras_3layer_config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/config-files/qkeras_mnist_cnn_config.yml` & `hls4ml-0.7.1/example-models/config-files/qkeras_mnist_cnn_config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/config-files/qkeras_mnist_dense_config.yml` & `hls4ml-0.7.1/example-models/config-files/qkeras_mnist_dense_config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/data/garnet_1layer_input.dat` & `hls4ml-0.7.1/example-models/data/garnet_1layer_input.dat`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/data/garnet_1layer_output.dat` & `hls4ml-0.7.1/example-models/data/garnet_1layer_output.dat`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_1layer.json` & `hls4ml-0.7.1/example-models/keras/KERAS_1layer.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_1layer_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_1layer_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer.json` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_70pruned_retrained_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_70pruned_retrained_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_95pruned_retrained_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_95pruned_retrained_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_batch_norm.json` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_batch_norm.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_batch_norm_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_batch_norm_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binary_smaller.json` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_binary_smaller.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binary_smaller_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_binary_smaller_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binarydense_relu_max.json` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_binarydense_relu_max.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_binarydense_relu_max_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_binarydense_relu_max_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_ternary_small.json` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_ternary_small.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_ternary_small_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_ternary_small_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_3layer_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_3layer_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d.json` & `hls4ml-0.7.1/example-models/keras/KERAS_conv1d.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_small.json` & `hls4ml-0.7.1/example-models/keras/KERAS_conv1d_small.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_small_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_conv1d_small_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv1d_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_conv1d_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv2d_model.json` & `hls4ml-0.7.1/example-models/keras/KERAS_conv2d_model.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_conv2d_model_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_conv2d_model_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5.json` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x100x100x100x100x100x5_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5.json` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x200x200x200x200x200x5_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5.json` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5_weights.h5` & `hls4ml-0.7.1/example-models/keras/KERAS_dense_16x500x500x500x500x500x5_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/garnet_1layer.json` & `hls4ml-0.7.1/example-models/keras/garnet_1layer.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/garnet_1layer_weights.h5` & `hls4ml-0.7.1/example-models/keras/garnet_1layer_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/garnet_3layer.json` & `hls4ml-0.7.1/example-models/keras/garnet_3layer.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/garnet_3layer_weights.h5` & `hls4ml-0.7.1/example-models/keras/garnet_3layer_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small.json` & `hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm.json` & `hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm_weights.h5` & `hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_NoBatchNorm_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/jetTagger_Conv2D_Small_weights.h5` & `hls4ml-0.7.1/example-models/keras/jetTagger_Conv2D_Small_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/keras_bnn.json` & `hls4ml-0.7.1/example-models/keras/keras_bnn.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/keras_bnn_weights.h5` & `hls4ml-0.7.1/example-models/keras/keras_bnn_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_3layer.json` & `hls4ml-0.7.1/example-models/keras/qkeras_3layer.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_3layer_weights.h5` & `hls4ml-0.7.1/example-models/keras/qkeras_3layer_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_cnn.json` & `hls4ml-0.7.1/example-models/keras/qkeras_mnist_cnn.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_cnn_weights.h5` & `hls4ml-0.7.1/example-models/keras/qkeras_mnist_cnn_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_dense.json` & `hls4ml-0.7.1/example-models/keras/qkeras_mnist_dense.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras/qkeras_mnist_dense_weights.h5` & `hls4ml-0.7.1/example-models/keras/qkeras_mnist_dense_weights.h5`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/keras-config.yml` & `hls4ml-0.7.1/example-models/keras-config.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/conv1d_small_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/conv1d_small_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/conv2d_small_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/conv2d_small_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/conv2d_small_mp_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/conv2d_small_mp_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/dense_big_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/dense_big_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/three_layer_bn_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/three_layer_bn_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/three_layer_bn_pytorch.onnx` & `hls4ml-0.7.1/example-models/onnx/three_layer_bn_pytorch.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/three_layer_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/three_layer_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/three_layer_pytorch.onnx` & `hls4ml-0.7.1/example-models/onnx/three_layer_pytorch.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/two_layer_keras.onnx` & `hls4ml-0.7.1/example-models/onnx/two_layer_keras.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/onnx/two_layer_pytorch.onnx` & `hls4ml-0.7.1/example-models/onnx/two_layer_pytorch.onnx`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/pytorch/three_layer_model.pt` & `hls4ml-0.7.1/example-models/pytorch/three_layer_model.pt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/pytorch/two_layer_model.pt` & `hls4ml-0.7.1/example-models/pytorch/two_layer_model.pt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/scan.py` & `hls4ml-0.7.1/example-models/scan.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/example-models/tensorflow/3layer.pb` & `hls4ml-0.7.1/example-models/tensorflow/3layer.pb`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/__init__.py` & `hls4ml-0.7.1/hls4ml/__init__.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/__init__.py` & `hls4ml-0.7.1/hls4ml/backends/__init__.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/backend.py` & `hls4ml-0.7.1/hls4ml/backends/backend.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_backend.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/fpga_backend.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_layers.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/fpga_layers.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/fpga_types.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/fpga_types.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/bn_quant.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/bn_quant.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 from hls4ml.model.layers import BatchNormalization, register_layer
 from hls4ml.model.optimizer import OptimizerPass
 from hls4ml.model.types import IntegerPrecisionType, NamedType, XnorPrecisionType
 
 batchnorm_quantized_tanh_config_template = """struct config{index} : nnet::batchnorm_quantized_tanh_config {{
     static const unsigned n_in = {n_in};
     static const unsigned n_filt = {n_filt};
+    static const unsigned n_scale_bias = (n_filt == -1) ? n_in : n_filt;
     static const unsigned io_type = nnet::{iotype};
     static const unsigned reuse_factor = {reuse};
 }};\n"""
 
 batchnorm_quantized_tanh_function_template = (
     'nnet::normalize_{quantize}_tanh<{input_t}, {config}>({input}, {output}, {threshold});'
 )
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/bram_weights.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/bram_weights.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/clone.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/clone.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/codegen.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/codegen.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/embedding.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/embedding.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/final_reshape.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/final_reshape.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/inplace_parallel_reshape.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/inplace_parallel_reshape.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/inplace_stream_flatten.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/inplace_stream_flatten.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/fpga/passes/repack_stream.py` & `hls4ml-0.7.1/hls4ml/backends/fpga/passes/repack_stream.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/convolution_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/convolution_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/convolution_winograd.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/convolution_winograd.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/core_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/core_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/merge_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/merge_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/pointwise.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/pointwise.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/pooling_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/pooling_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/quantization_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/quantization_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/recurrent_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/recurrent_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/reshaping_templates.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/reshaping_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/resource_strategy.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/resource_strategy.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/passes/transform_types.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/passes/transform_types.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/quartus/quartus_backend.py` & `hls4ml-0.7.1/hls4ml/backends/quartus/quartus_backend.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 from contextlib import contextmanager
 
 import numpy as np
 
 from hls4ml.backends import FPGABackend
-from hls4ml.model.attributes import ConfigurableAttribute
+from hls4ml.model.attributes import ConfigurableAttribute, TypeAttribute
 from hls4ml.model.flow import register_flow
 from hls4ml.model.layers import GRU, LSTM, Activation, Conv1D, Conv2D, Dense, Embedding, Layer, SimpleRNN, Softmax
 from hls4ml.model.optimizer import get_backend_passes, layer_optimizer
 from hls4ml.model.types import FixedPrecisionType, IntegerPrecisionType, NamedType
 from hls4ml.report import parse_quartus_report
 
 
@@ -35,14 +35,16 @@
             LSTM,
             GRU,
         ]
 
         for layer in rnn_layers:
             attrs = self.attribute_map.get(layer, [])
             attrs.append(ConfigurableAttribute('recurrent_reuse_factor', default=1))
+            attrs.append(ConfigurableAttribute('table_size', default=1024))
+            attrs.append(TypeAttribute('table', default=FixedPrecisionType(18, 8)))
             self.attribute_map[layer] = attrs
 
     def _register_flows(self):
         initializers = self._get_layer_initializers()
         init_flow = register_flow('init_layers', initializers, requires=['optimize'], backend=self.name)
 
         streaming_passes = ['quartus:reshape_stream', 'quartus:clone_output']
@@ -308,24 +310,14 @@
         )  # TODO Not used yet as there is no codegen implementation of CNNs for Quartus backend
 
     @layer_optimizer(LSTM)
     def init_lstm(self, layer):
         reuse_factor = layer.model.config.get_reuse_factor(layer)
         layer.set_attr('recurrent_reuse_factor', reuse_factor)
 
-        index_t = IntegerPrecisionType(width=1, signed=False)
-        layer.set_attr('index_t', index_t)
-
-        if 'table_t' not in layer.attributes:
-            layer.set_attr(
-                'table_t', NamedType(name=layer.name + '_table_t', precision=FixedPrecisionType(width=18, integer=8))
-            )
-        if 'table_size' not in layer.attributes:
-            layer.set_attr('table_size', 1024)
-
         # We don't use RF yet
         if True:  # layer.model.config.is_resource_strategy(layer): ... Quartus only supports Dense resource multiplication
             n_in, n_out, n_in_recr, n_out_recr = self.get_layer_mult_size(layer)
             self.set_closest_reuse_factor(layer, n_in, n_out)
             self.set_closest_reuse_factor(layer, n_in_recr, n_out_recr, attribute='recurrent_reuse_factor')
             layer.set_attr('strategy', 'resource')
 
@@ -363,18 +355,8 @@
             )
 
     @layer_optimizer(SimpleRNN)
     def init_simple_rnn(self, layer):
         reuse_factor = layer.model.config.get_reuse_factor(layer)
         layer.set_attr('recurrent_reuse_factor', reuse_factor)
 
-        index_t = IntegerPrecisionType(width=1, signed=False)
-        layer.set_attr('index_t', index_t)
-
-        if 'table_t' not in layer.attributes:
-            layer.set_attr(
-                'table_t', NamedType(name=layer.name + '_table_t', precision=FixedPrecisionType(width=18, integer=8))
-            )
-        if 'table_size' not in layer.attributes:
-            layer.set_attr('table_size', 1024)
-
         # TODO - Consider setting and using RF
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/template.py` & `hls4ml-0.7.1/hls4ml/backends/template.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vitis/passes/feature_check.py` & `hls4ml-0.7.1/hls4ml/backends/vitis/passes/feature_check.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vitis/vitis_backend.py` & `hls4ml-0.7.1/hls4ml/backends/vitis/vitis_backend.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/broadcast_stream.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/broadcast_stream.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/conv_same_pad.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/conv_same_pad.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/conv_stream.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/conv_stream.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/convolution_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/convolution_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/core_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/core_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/fifo_depth_optimization.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/fifo_depth_optimization.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/garnet_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/garnet_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/merge_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/merge_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/pointwise.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/pointwise.py`

 * *Files 4% similar despite different names*

```diff
@@ -78,10 +78,15 @@
     def transform(self, model, node):
         dim = node.__class__.__name__[-2:]  # '1D' or '2D'
         pw_node = model.make_node('PointwiseConv' + dim, node.name, copy(node.attributes), node.inputs.copy())
         if len(node.weights['weight'].data.shape) == 2:  # This can happen if we assign weights of Dense layer to 1x1 Conv2D
             expand_axis = tuple(range(int(dim[0])))
             pw_node.weights['weight'].data = np.expand_dims(node.weights['weight'].data, axis=expand_axis)
         pw_node.weights['bias'].data = node.weights['bias'].data
+        # Set strategy to ensure lowercase string is passed to the template
+        if model.config.is_resource_strategy(pw_node):
+            pw_node.set_attr('strategy', 'resource')
+        else:
+            pw_node.set_attr('strategy', 'latency')
         model.replace_node(node, pw_node)
 
         return True
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/pooling_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/pooling_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/quantization_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/quantization_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/recurrent_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/recurrent_templates.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,35 +12,35 @@
     static const unsigned n_zeros = {nzeros};
     static const unsigned n_nonzeros = {nonzeros};
     static const unsigned multiplier_limit = DIV_ROUNDUP(n_in * n_out, reuse_factor) - n_zeros / reuse_factor;
     static const bool store_weights_in_bram = false;
     typedef {accum_t.name} accum_t;
     typedef {bias_t.name} bias_t;
     typedef {weight_t.name} weight_t;
-    typedef ap_{index_t} index_t;
+    typedef {index_t.name} index_t;
     template<class x_T, class y_T>
     using product = nnet::product::{product_type}<x_T, y_T>;
 }};\n"""
 
 # activation templates
 
 activ_config_template = """struct {type}_config{index} : nnet::activ_config {{
     static const unsigned n_in = {n_in};
     static const unsigned table_size = {table_size};
     static const unsigned io_type = nnet::{iotype};
     static const unsigned reuse_factor = {reuse};
-    typedef ap_{table_t} table_t;
+    typedef {table_t.name} table_t;
 }};\n"""
 
 recr_activ_config_template = """struct {type}_config{index}_recr : nnet::activ_config {{
     static const unsigned n_in = {n_in};
     static const unsigned table_size = {table_size};
     static const unsigned io_type = nnet::{iotype};
     static const unsigned reuse_factor = {reuse};
-    typedef ap_{table_t} table_t;
+    typedef {table_t.name} table_t;
 }};\n"""
 
 # LSTM + GRU templates
 
 recr_config_template = """struct config{index} : nnet::{recr_type}_config {{
     typedef {accum_t.name} accum_t;
     typedef {weight_t.name} weight_t;  // Matrix
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/reshaping_templates.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/reshaping_templates.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/resource_strategy.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/resource_strategy.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/passes/transform_types.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/passes/transform_types.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado/vivado_backend.py` & `hls4ml-0.7.1/hls4ml/backends/vivado/vivado_backend.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import os
 import sys
 
 import numpy as np
 
 from hls4ml.backends import FPGABackend
 from hls4ml.backends.fpga.fpga_types import APTypeConverter, HLSTypeConverter, VivadoArrayVariableConverter
-from hls4ml.model.attributes import ChoiceAttribute, ConfigurableAttribute
+from hls4ml.model.attributes import ChoiceAttribute, ConfigurableAttribute, TypeAttribute
 from hls4ml.model.flow import register_flow
 from hls4ml.model.layers import (
     GRU,
     LSTM,
     Conv1D,
     Conv2D,
     Dense,
@@ -47,14 +47,16 @@
             GRU,
         ]
 
         for layer in rnn_layers:
             attrs = self.attribute_map.get(layer, [])
             attrs.append(ConfigurableAttribute('recurrent_reuse_factor', default=1))
             attrs.append(ConfigurableAttribute('static', value_type=bool, default=True))
+            attrs.append(ConfigurableAttribute('table_size', default=1024))
+            attrs.append(TypeAttribute('table', default=FixedPrecisionType(18, 8)))
             self.attribute_map[layer] = attrs
 
         # Add ParallelizationFactor to Conv1D/2D
         pf_layers = [
             Conv1D,
             Conv2D,
         ]
@@ -389,54 +391,38 @@
 
     @layer_optimizer(LSTM)
     def init_lstm(self, layer):
         # TODO Allow getting recurrent reuse factor from the config
         reuse_factor = layer.model.config.get_reuse_factor(layer)
         layer.set_attr('recurrent_reuse_factor', reuse_factor)
 
-        index_t = IntegerPrecisionType(width=1, signed=False)
-
-        if 'table_t' not in layer.attributes:
-            layer.set_attr('table_t', FixedPrecisionType(width=18, integer=8))
-        if 'table_size' not in layer.attributes:
-            layer.set_attr('table_size', 1024)
         if layer.model.config.is_resource_strategy(layer):
             n_in, n_out, n_in_recr, n_out_recr = self.get_layer_mult_size(layer)
             self.set_closest_reuse_factor(layer, n_in, n_out)
             self.set_closest_reuse_factor(layer, n_in_recr, n_out_recr, attribute='recurrent_reuse_factor')
-            layer.weights['weight'].data = np.transpose(layer.weights['weight'].data)
-            layer.weights['recurrent_weight'].data = np.transpose(layer.weights['recurrent_weight'].data)
             layer.set_attr('strategy', 'resource')
         else:
             layer.set_attr('strategy', 'latency')
 
-        layer.set_attr('index_t', index_t)
+        layer.set_attr('index_t', NamedType(f'layer{layer.index}_index', IntegerPrecisionType(width=1, signed=False)))
 
     @layer_optimizer(GRU)
     def init_gru(self, layer):
         reuse_factor = layer.model.config.get_reuse_factor(layer)
         layer.set_attr('recurrent_reuse_factor', reuse_factor)
 
-        index_t = IntegerPrecisionType(width=1, signed=False)
-
-        if 'table_t' not in layer.attributes:
-            layer.set_attr('table_t', FixedPrecisionType(width=18, integer=8))
-        if 'table_size' not in layer.attributes:
-            layer.set_attr('table_size', 1024)
         if layer.model.config.is_resource_strategy(layer):
             n_in, n_out, n_in_recr, n_out_recr = self.get_layer_mult_size(layer)
             self.set_closest_reuse_factor(layer, n_in, n_out)
             self.set_closest_reuse_factor(layer, n_in_recr, n_out_recr, attribute='recurrent_reuse_factor')
-            layer.weights['weight'].data = np.transpose(layer.weights['weight'].data)
-            layer.weights['recurrent_weight'].data = np.transpose(layer.weights['recurrent_weight'].data)
             layer.set_attr('strategy', 'resource')
         else:
             layer.set_attr('strategy', 'latency')
 
-        layer.set_attr('index_t', index_t)
+        layer.set_attr('index_t', NamedType(f'layer{layer.index}_index', IntegerPrecisionType(width=1, signed=False)))
 
     @layer_optimizer(GarNet)
     def init_garnet(self, layer):
         reuse_factor = layer.attributes['reuse_factor']
 
         var_converter = VivadoArrayVariableConverter(type_converter=HLSTypeConverter(precision_converter=APTypeConverter()))
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/passes/fifo_depth_optimization.py` & `hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/passes/fifo_depth_optimization.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/supported_boards.json` & `hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/supported_boards.json`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/vivado_accelerator_backend.py` & `hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/vivado_accelerator_backend.py`

 * *Files 4% similar despite different names*

```diff
@@ -54,21 +54,21 @@
                 except Exception:
                     print("Something went wrong, check the Vivado logs")
                 os.chdir(curr_dir)
 
         return parse_vivado_report(model.config.get_output_dir())
 
     def make_xclbin(self, model, platform='xilinx_u250_xdma_201830_2'):
-        """
+        """Create the xclbin for the given model and target platform.
 
-        Parameters
-        ----------
-        - model : compiled and built hls_model.
-        - platform : development Target Platform, must be installed first. On the host machine is required only the
-                     deployment target platform, both can be found on the Getting Started section of the Alveo card.
+        Args:
+            model (ModelGraph): Compiled and build model.
+            platform (str, optional): Development/Deployment target platform, must be installed first.
+                The host machine only requires the deployment target platform. Refer to the Getting Started section of
+                the Alveo guide. Defaults to 'xilinx_u250_xdma_201830_2'.
         """
         curr_dir = os.getcwd()
         abs_path_dir = os.path.abspath(model.config.get_output_dir())
         os.chdir(abs_path_dir)
         os.makedirs('xo_files', exist_ok=True)
         try:
             os.system('vivado -mode batch -source design.tcl')
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/backends/vivado_accelerator/vivado_accelerator_config.py` & `hls4ml-0.7.1/hls4ml/backends/vivado_accelerator/vivado_accelerator_config.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/__init__.py` & `hls4ml-0.7.1/hls4ml/converters/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -190,15 +190,15 @@
     project_name='myproject',
     input_data_tb=None,
     output_data_tb=None,
     backend='Vivado',
     hls_config=None,
     **kwargs,
 ):
-    """Convert to hls4ml model based on the provided configuration.
+    """Convert Keras model to hls4ml model based on the provided configuration.
 
     Args:
         model: Keras model to convert
         output_dir (str, optional): Output directory of the generated HLS
             project. Defaults to 'my-hls-test'.
         project_name (str, optional): Name of the HLS project.
             Defaults to 'myproject'.
@@ -217,15 +217,15 @@
             Defaults to 5.
         io_type (str, optional): Type of implementation used. One of
             'io_parallel' or 'io_stream'. Defaults to 'io_parallel'.
         hls_config (dict, optional): The HLS config.
         kwargs** (dict, optional): Additional parameters that will be used to create the config of the specified backend
 
     Raises:
-        Exception: If precision and reuse factor are not present in 'hls_config'
+        Exception: If precision and reuse factor are not present in 'hls_config'.
 
     Returns:
         ModelGraph: hls4ml model.
     """
 
     config = create_config(output_dir=output_dir, project_name=project_name, backend=backend, **kwargs)
 
@@ -252,62 +252,43 @@
     project_name='myproject',
     input_data_tb=None,
     output_data_tb=None,
     backend='Vivado',
     hls_config=None,
     **kwargs,
 ):
-    """
+    """Convert PyTorch model to hls4ml model based on the provided configuration.
 
-    Convert a Pytorch model to a hls model.
+    Args:
+        model: PyTorch model to conert.
+        input_shape (list): The shape of the input tensor.
+        output_dir (str, optional): Output directory of the generated HLS project. Defaults to 'my-hls-test'.
+        project_name (str, optional): Name of the HLS project. Defaults to 'myproject'.
+        input_data_tb (str, optional): String representing the path of input data in .npy or .dat format that will be
+            used during csim and cosim. Defaults to None.
+        output_data_tb (str, optional): String representing the path of output data in .npy or .dat format that will be
+            used during csim and cosim. Defaults to None.
+        backend (str, optional): Name of the backend to use, e.g., 'Vivado' or 'Quartus'. Defaults to 'Vivado'.
+        board (str, optional): One of target boards specified in `supported_board.json` file. If set to `None` a default
+            device of a backend will be used. See documentation of the backend used.
+        part (str, optional): The FPGA part. If set to `None` a default part of a backend will be used.
+            See documentation of the backend used. Note that if `board` is specified, the part associated to that board
+            will overwrite any part passed as a parameter.
+        clock_period (int, optional): Clock period of the design.
+            Defaults to 5.
+        io_type (str, optional): Type of implementation used. One of
+            'io_parallel' or 'io_stream'. Defaults to 'io_parallel'.
+        hls_config (dict, optional): The HLS config.
+        kwargs** (dict, optional): Additional parameters that will be used to create the config of the specified backend.
+
+    Raises:
+        Exception: If precision and reuse factor are not present in 'hls_config'.
 
-    Parameters
-    ----------
-    model : Pytorch model object.
-        Model to be converted to hls model object.
-    input_shape : @todo: to be filled
-    output_dir (str, optional): Output directory of the generated HLS
-        project. Defaults to 'my-hls-test'.
-    project_name (str, optional): Name of the HLS project.
-        Defaults to 'myproject'.
-    input_data_tb (str, optional): String representing the path of input data in .npy or .dat format that will be
-        used during csim and cosim.
-    output_data_tb (str, optional): String representing the path of output data in .npy or .dat format that will be
-        used during csim and cosim.
-    backend (str, optional): Name of the backend to use, e.g., 'Vivado'
-        or 'Quartus'.
-    board (str, optional): One of target boards specified in `supported_board.json` file. If set to `None` a default
-        device of a backend will be used. See documentation of the backend used.
-    part (str, optional): The FPGA part. If set to `None` a default part of a backend will be used.
-        See documentation of the backend used. Note that if `board` is specified, the part associated to that board
-        will overwrite any part passed as a parameter.
-    clock_period (int, optional): Clock period of the design.
-        Defaults to 5.
-    io_type (str, optional): Type of implementation used. One of
-        'io_parallel' or 'io_stream'. Defaults to 'io_parallel'.
-    hls_config (dict, optional): The HLS config.
-    kwargs** (dict, optional): Additional parameters that will be used to create the config of the specified backend
-
-    Returns
-    -------
-    ModelGraph : hls4ml model object.
-
-    See Also
-    --------
-    hls4ml.convert_from_keras_model, hls4ml.convert_from_onnx_model
-
-    Examples
-    --------
-    >>> import hls4ml
-    >>> config = hls4ml.utils.config_from_pytorch_model(model, granularity='model')
-    >>> hls_model = hls4ml.converters.convert_from_pytorch_model(model, hls_config=config)
-
-    Notes
-    -----
-    Only sequential Pytorch models are supported for now.
+    Returns:
+        ModelGraph: hls4ml model.
     """
 
     config = create_config(output_dir=output_dir, project_name=project_name, backend=backend, **kwargs)
 
     config['PytorchModel'] = model
     config['InputShape'] = input_shape
     config['InputData'] = input_data_tb
@@ -331,57 +312,45 @@
     project_name='myproject',
     input_data_tb=None,
     output_data_tb=None,
     backend='Vivado',
     hls_config=None,
     **kwargs,
 ):
-    """
+    """Convert Keras model to hls4ml model based on the provided configuration.
 
-    Convert an ONNX model to a hls model.
+    Args:
+        model: ONNX model to convert.
+        output_dir (str, optional): Output directory of the generated HLS
+            project. Defaults to 'my-hls-test'.
+        project_name (str, optional): Name of the HLS project.
+            Defaults to 'myproject'.
+        input_data_tb (str, optional): String representing the path of input data in .npy or .dat format that will be
+            used during csim and cosim.
+        output_data_tb (str, optional): String representing the path of output data in .npy or .dat format that will be
+            used during csim and cosim.
+        backend (str, optional): Name of the backend to use, e.g., 'Vivado'
+            or 'Quartus'.
+        board (str, optional): One of target boards specified in `supported_board.json` file. If set to `None` a default
+            device of a backend will be used. See documentation of the backend used.
+        part (str, optional): The FPGA part. If set to `None` a default part of a backend will be used.
+            See documentation of the backend used. Note that if `board` is specified, the part associated to that board
+            will overwrite any part passed as a parameter.
+        clock_period (int, optional): Clock period of the design.
+            Defaults to 5.
+        io_type (str, optional): Type of implementation used. One of
+            'io_parallel' or 'io_stream'. Defaults to 'io_parallel'.
+        hls_config (dict, optional): The HLS config.
+        kwargs** (dict, optional): Additional parameters that will be used to create the config of the specified backend
+
+    Raises:
+        Exception: If precision and reuse factor are not present in 'hls_config'.
 
-    Parameters
-    ----------
-    model : ONNX model object.
-        Model to be converted to hls model object.
-    output_dir (str, optional): Output directory of the generated HLS
-        project. Defaults to 'my-hls-test'.
-    project_name (str, optional): Name of the HLS project.
-        Defaults to 'myproject'.
-    input_data_tb (str, optional): String representing the path of input data in .npy or .dat format that will be
-        used during csim and cosim.
-    output_data_tb (str, optional): String representing the path of output data in .npy or .dat format that will be
-        used during csim and cosim.
-    backend (str, optional): Name of the backend to use, e.g., 'Vivado'
-        or 'Quartus'.
-    board (str, optional): One of target boards specified in `supported_board.json` file. If set to `None` a default
-        device of a backend will be used. See documentation of the backend used.
-    part (str, optional): The FPGA part. If set to `None` a default part of a backend will be used.
-        See documentation of the backend used. Note that if `board` is specified, the part associated to that board
-        will overwrite any part passed as a parameter.
-    clock_period (int, optional): Clock period of the design.
-        Defaults to 5.
-    io_type (str, optional): Type of implementation used. One of
-        'io_parallel' or 'io_stream'. Defaults to 'io_parallel'.
-    hls_config (dict, optional): The HLS config.
-    kwargs** (dict, optional): Additional parameters that will be used to create the config of the specified backend
-
-    Returns
-    -------
-    ModelGraph : hls4ml model object.
-
-    See Also
-    --------
-    hls4ml.convert_from_keras_model, hls4ml.convert_from_pytorch_model
-
-    Examples
-    --------
-    >>> import hls4ml
-    >>> config = hls4ml.utils.config_from_onnx_model(model, granularity='model')
-    >>> hls_model = hls4ml.converters.convert_from_onnx_model(model, hls_config=config)
+    Returns:
+        ModelGraph: hls4ml model.
     """
 
     config = create_config(output_dir=output_dir, project_name=project_name, backend=backend, **kwargs)
 
     config['OnnxModel'] = model
     config['InputData'] = input_data_tb
     config['OutputPredictions'] = output_data_tb
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/convolution.py` & `hls4ml-0.7.1/hls4ml/converters/keras/convolution.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/core.py` & `hls4ml-0.7.1/hls4ml/converters/keras/core.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/graph.py` & `hls4ml-0.7.1/hls4ml/converters/keras/graph.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/merge.py` & `hls4ml-0.7.1/hls4ml/converters/keras/merge.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/pooling.py` & `hls4ml-0.7.1/hls4ml/converters/keras/pooling.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/qkeras.py` & `hls4ml-0.7.1/hls4ml/converters/keras/qkeras.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/recurrent.py` & `hls4ml-0.7.1/hls4ml/converters/keras/recurrent.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/reshape.py` & `hls4ml-0.7.1/hls4ml/converters/keras/reshape.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras/reshaping.py` & `hls4ml-0.7.1/hls4ml/converters/keras/reshaping.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/keras_to_hls.py` & `hls4ml-0.7.1/hls4ml/converters/keras_to_hls.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx/convolution.py` & `hls4ml-0.7.1/hls4ml/converters/onnx/convolution.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx/core.py` & `hls4ml-0.7.1/hls4ml/converters/onnx/core.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx/merge.py` & `hls4ml-0.7.1/hls4ml/converters/onnx/merge.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx/pooling.py` & `hls4ml-0.7.1/hls4ml/converters/onnx/pooling.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx/reshape.py` & `hls4ml-0.7.1/hls4ml/converters/onnx/reshape.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/onnx_to_hls.py` & `hls4ml-0.7.1/hls4ml/converters/onnx_to_hls.py`

 * *Files 2% similar despite different names*

```diff
@@ -25,26 +25,20 @@
             'moving_mean': 3,
             'moving_variance': 4,
         }
 
     def get_weights_data(self, layer_name, var_name):
         """Extract weights data from ONNX model.
 
-        Parameters
-        ----------
-        layer_name : string
-            layer's name in the ONNX model
-        var_name : string
-            variable to be extracted
-
-        Returns
-        -------
-        data : numpy array
-            extracted weights data
+        Args:
+            layer_name (str): Layer's name in the ONNX model.
+            var_name (str): Variable to be extracted.
 
+        Returns:
+            ndarray: Extracted weights data.
         """
         # Get the node associated with the layer name
         node = next(node for node in self.model.graph.node if node.name == layer_name)
 
         inputs = self.input_map[layer_name]
         inp_idx = self.index_map[var_name]
 
@@ -214,25 +208,23 @@
     output_index_list = [x.name for x in graph.output]
     return [node.name for node in graph.node if node.output[0] in output_index_list]
 
 
 def onnx_to_hls(config):
     """Convert onnx model to hls model from configuration.
 
-    Parameters
-    ----------
-    config: dict
-        onnx configuration from yaml file or passed through API.
-
-    Returns
-    -------
-    ModelGraph : hls4ml model object
+    Args:
+        config (dict): ONNX configuration from yaml file or passed through API.
 
-    """
+    Raises:
+        Exception: Raised if an unsupported operation is found in the ONNX model.
 
+    Returns:
+        ModelGraph: hls4ml model object
+    """
     # This is a list of dictionaries to hold all the layer info we need to generate HLS
     layer_list = []
 
     # Extract model architecture
     print('Interpreting Model ...')
 
     model = onnx.load(config['OnnxModel']) if isinstance(config['OnnxModel'], str) else config['OnnxModel']
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/pytorch/convolution.py` & `hls4ml-0.7.1/hls4ml/converters/pytorch/convolution.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/pytorch/core.py` & `hls4ml-0.7.1/hls4ml/converters/pytorch/core.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/pytorch_to_hls.py` & `hls4ml-0.7.1/hls4ml/converters/pytorch_to_hls.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/tf_to_hls.py` & `hls4ml-0.7.1/hls4ml/converters/tf_to_hls.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/converters/utils.py` & `hls4ml-0.7.1/hls4ml/converters/utils.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/attributes.py` & `hls4ml-0.7.1/hls4ml/model/attributes.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/flow/flow.py` & `hls4ml-0.7.1/hls4ml/model/flow/flow.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/graph.py` & `hls4ml-0.7.1/hls4ml/model/graph.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/layers.py` & `hls4ml-0.7.1/hls4ml/model/layers.py`

 * *Files 0% similar despite different names*

```diff
@@ -108,15 +108,15 @@
                         config_key, self.name, self.class_name
                     )
                 )
             if config_key.endswith('_t') and isinstance(
                 config_value, str
             ):  # TODO maybe move this to __setitem__ of AttributeDict?
                 precision = self.model.config.backend.convert_precision_string(config_value)
-                config_value = NamedType(self.name + config_key, precision)
+                config_value = NamedType(self.name + '_' + config_key, precision)
             self.attributes[config_key] = config_value
 
         self.initialize()
         self._validate_attributes()
 
     @property
     def class_name(self, include_wrapped=False):
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/__init__.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/__init__.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/optimizer.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/optimizer.py`

 * *Files 1% similar despite different names*

```diff
@@ -297,15 +297,15 @@
     The passes are attempted until all passes no longer match or no changes to the model graph occur.
 
     Args:
         model (ModelGraph): The model to optimize.
         passes (list): List of passes to apply.
 
     Returns:
-        set: The set of applied passes (the pases that matched the predicate).
+        set: The set of applied passes (the passes that matched the predicate).
     """
     optimizers = {opt_pass: get_optimizer(opt_pass) for opt_pass in passes}
     applied_passes = set()
     optimization_done = False
     while not optimization_done:
         for opt_name, opt in optimizers.items():
             if isinstance(opt, ModelOptimizerPass) and opt_name not in applied_passes:
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/bn_fuse.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/bn_fuse.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/fuse_biasadd.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/fuse_biasadd.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/multi_dense.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/multi_dense.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/nop.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/nop.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/precision_merge.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/precision_merge.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/qkeras.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/qkeras.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/stamp.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/stamp.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/optimizer/passes/transpose_opt.py` & `hls4ml-0.7.1/hls4ml/model/optimizer/passes/transpose_opt.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/profiling.py` & `hls4ml-0.7.1/hls4ml/model/profiling.py`

 * *Files 4% similar despite different names*

```diff
@@ -418,39 +418,30 @@
 
     if fmt == 'longform':
         data = pandas.DataFrame(data)
     return data
 
 
 def numerical(model=None, hls_model=None, X=None, plot='boxplot'):
-    """
-    Perform numerical profiling of a model
+    """Perform numerical profiling of a model.
 
-    Parameters
-    ----------
-    model : keras or pytorch model
-        The model to profile
-    hls_model : ModelGraph
-        The ModelGraph to profile
-    X : array-like, optional
-        Test data on which to evaluate the model to profile activations
-        Must be formatted suitably for the ``model.predict(X)`` method
-    plot : str, optional
-        The type of plot to produce.
-        Options are: 'boxplot' (default), 'violinplot', 'histogram',
-        'FacetGrid'
-
-    Returns
-    -------
-    tuple
-        The quadruple of produced figures. First weights and biases
-        for the pre- and post-optimization models respectively,
-        then activations for the pre- and post-optimization models
-        respectively. (Optimizations are applied to an ModelGraph by hls4ml,
-        a post-optimization ModelGraph is a final model)
+    Args:
+        model (optional): Keras of PyTorch model. Defaults to None.
+        hls_model (ModelGraph, optional): The ModelGraph to profile. Defaults to None.
+        X (ndarray, optional): Test data on which to evaluate the model to profile activations.
+            Must be formatted suitably for the ``model.predict(X)``. Defaults to None.
+        plot (str, optional): The type of plot to produce. Options are: 'boxplot' (default), 'violinplot', 'histogram',
+            'FacetGrid'. Defaults to 'boxplot'.
+
+    Returns:
+        tuple: The quadruple of produced figures. First weights and biases
+            for the pre- and post-optimization models respectively,
+            then activations for the pre- and post-optimization models
+            respectively. (Optimizations are applied to an ModelGraph by hls4ml,
+            a post-optimization ModelGraph is a final model).
     """
     wp, wph, ap, aph = None, None, None, None
 
     hls_model_present = hls_model is not None and isinstance(hls_model, ModelGraph)
     model_present = model is not None
 
     if hls_model_present:
@@ -550,29 +541,23 @@
     """Get output of partial model"""
     partial_model = keras.models.Model(inputs=model_input, outputs=layer.output)
     y = partial_model.predict(X)
     return y
 
 
 def get_ymodel_keras(keras_model, X):
-    """
-    Calculate each layer's ouput and put them into a dictionary
+    """Calculate each layer's ouput and put them into a dictionary.
+
+    Args:
+        keras_model (_type_): A keras Model
+        X (ndarray): Test data on which to evaluate the model to profile activations.
+            Must be formatted suitably for the ``model.predict(X)``.
 
-    Parameters
-    ----------
-    keras_model :
-        a keras model
-    X : array-like
-        Test data on which to evaluate the model to profile activations.
-        Must be formatted suitably for the ``model.predict(X)`` method.
-
-    Returns
-    -------
-    dictionary
-        A dictionary in the form {"layer_name": ouput array of layer}
+    Returns:
+        dict: A dictionary in the form {"layer_name": ouput array of layer}.
     """
 
     ymodel = {}
 
     for layer in keras_model.layers:
         print(f"Processing {layer.name} in Keras model...")
         if not _is_ignored_layer(layer):
@@ -664,38 +649,28 @@
     plt.xticks(rotation=90)
     plt.tight_layout()
 
     return f
 
 
 def compare(keras_model, hls_model, X, plot_type="dist_diff"):
-    """
-    Compare each layer's output in keras and hls model. Note that the hls_model should not be compiled before using this.
+    """Compare each layer's output in keras and hls model. Note that the hls_model should not be compiled before using this.
+
+    Args:
+        keras_model: Original keras model.
+        hls_model (ModelGraph): Converted ModelGraph, with "Trace:True" in the configuration file.
+        X (ndarray): Input tensor for the model.
+        plot_type (str, optional): Different methods to visualize the y_model and y_sim differences.
+            Possible options include:
+            - 'norm_diff':: square root of the sum of the squares of the differences between each output vectors.
+            - 'dist_diff':: The normalized distribution of the differences of the elements between two output vectors.
+            Defaults to "dist_diff".
 
-    Parameters
-    ----------
-    keras_model :
-        original keras model
-    hls_model :
-        converted ModelGraph, with "Trace:True" in the configuration file.
-    X : array-like
-        Input for the model.
-    plot_type : string
-        different methods to visualize the y_model and y_sim differences.
-        Possible options include:
-
-        - 'norm_diff' : square root of the sum of the squares of the differences
-          between each output vectors
-        - 'dist_diff' : The normalized distribution of the differences of the elements
-          between two output vectors
-
-    Returns
-    -------
-    matplotlib figure
-        plot object of the histogram depicting the difference in each layer's output
+    Returns:
+        matplotlib figure: Plot object of the histogram depicting the difference in each layer's output.
     """
 
     # Take in output from both models
     # Note that each y is a dictionary with structure {"layer_name": flattened ouput array}
     ymodel = get_ymodel_keras(keras_model, X)
     _, ysim = hls_model.trace(X)
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/model/types.py` & `hls4ml-0.7.1/hls4ml/model/types.py`

 * *Files 0% similar despite different names*

```diff
@@ -366,14 +366,15 @@
 
 
 class NamedType:
     """Class representing a named type.
 
     For convenience, hls4ml gives names to data types used in the generated HLS. This is equivalent to defining types
     in C/C++ like::
+
         typedef precision name;
 
     Args:
         name (str): Name given to the type (used in generated C++/HLS).
         precision (PrecisionType): Precision data type.
     """
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/report/quartus_report.py` & `hls4ml-0.7.1/hls4ml/report/quartus_report.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/report/vivado_report.py` & `hls4ml-0.7.1/hls4ml/report/vivado_report.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/Makefile` & `hls4ml-0.7.1/hls4ml/templates/quartus/Makefile`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_channel.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_channel.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_complex.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_complex.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_fixed.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_fixed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_float.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_float.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_int.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_int.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_sc.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_sc.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/ac_std_float.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/ac_std_float.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/ac_types/stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/ac_types/stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/build_lib.sh` & `hls4ml-0.7.1/hls4ml/templates/quartus/build_lib.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/defines.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/defines.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/myproject.cpp` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/myproject.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/myproject.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/myproject.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_activation_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm.h`

 * *Files 8% similar despite different names*

```diff
@@ -11,30 +11,31 @@
     // Internal data type definitions
     typedef float bias_t;
     typedef float scale_t;
 
     // Layer Sizes
     static const unsigned n_in = 10;
     static const unsigned n_filt = -1;
+    static const unsigned n_scale_bias = 10;
 
     // Resource reuse info
     static const unsigned io_type = io_parallel;
     static const unsigned reuse_factor = 1;
     static const bool store_weights_in_bram = false;
     static const unsigned n_zeros = 0;
     // partitioning arrays cyclically to go with roll factors?
 
     // Default multiplication
     template <class x_T, class y_T> using product = nnet::product::mult<x_T, y_T>;
 };
 
 template <class data_T, class res_T, typename CONFIG_T>
 void normalize(data_T data[CONFIG_T::n_in], res_T res[CONFIG_T::n_in],
-               const typename CONFIG_T::scale_t scale[CONFIG_T::n_in],
-               const typename CONFIG_T::bias_t bias[CONFIG_T::n_in]) {
+               const typename CONFIG_T::scale_t scale[CONFIG_T::n_scale_bias],
+               const typename CONFIG_T::bias_t bias[CONFIG_T::n_scale_bias]) {
 // Calcuate result
 Result:
     #pragma unroll
     for (int ires = 0; ires < CONFIG_T::n_in; ires++) {
         if (CONFIG_T::n_filt == -1) {
             res[ires] = CONFIG_T::template product<data_T, typename CONFIG_T::scale_t>::product(data[ires], scale[ires]) +
                         bias[ires];
@@ -50,50 +51,54 @@
 // ****************************************************
 //       Merged Batch Normalization and Quantized Tanh
 // ****************************************************
 struct batchnorm_quantized_tanh_config {
     // Layer Sizes
     static const unsigned n_in = 10;
     static const unsigned n_filt = -1;
+    static const unsigned n_scale_bias = 10;
 
     // Resource reuse info
     static const unsigned io_type = io_parallel;
     static const unsigned reuse_factor = 1;
     static const unsigned n_zeros = 0;
 };
 
 template <class data_T, typename CONFIG_T>
 void normalize_binary_tanh(data_T data[CONFIG_T::n_in], ac_int<1, false> res[CONFIG_T::n_in],
-                           const data_T threshold[CONFIG_T::n_in]) {
+                           const data_T threshold[CONFIG_T::n_scale_bias]) {
     #pragma unroll
     for (int ii = 0; ii < CONFIG_T::n_in; ii++) {
         ac_int<1, false> cache;
         data_T datareg = data[ii];
-        if (datareg > threshold[ii])
+        int norm_index = CONFIG_T::n_filt == -1 ? ii : ii % CONFIG_T::n_filt;
+        if (datareg > threshold[norm_index])
             cache = 1;
         else
             cache = 0;
 
-        res[ii] = (ac_int<1, false>)cache;
+        res[ii] = cache;
     }
 }
 
 template <class data_T, typename CONFIG_T>
 void normalize_ternary_tanh(data_T data[CONFIG_T::n_in], ac_int<2, true> res[CONFIG_T::n_in],
-                            const data_T threshold_hi[CONFIG_T::n_in], const data_T threshold_lo[CONFIG_T::n_in]) {
+                            const data_T threshold_hi[CONFIG_T::n_scale_bias],
+                            const data_T threshold_lo[CONFIG_T::n_scale_bias]) {
     #pragma unroll
     for (int ii = 0; ii < CONFIG_T::n_in; ii++) {
         ac_int<2, true> cache;
         data_T datareg = data[ii];
-        if (datareg > threshold_hi[ii])
+        int norm_index = CONFIG_T::n_filt == -1 ? ii : ii % CONFIG_T::n_filt;
+        if (datareg > threshold_hi[norm_index])
             cache = 1;
-        else if (datareg <= threshold_lo[ii])
+        else if (datareg <= threshold_lo[norm_index])
             cache = -1;
         else
             cache = 0;
-        res[ii] = (ac_int<2, true>)cache;
+        res[ii] = cache;
     }
 }
 
 } // namespace nnet
 
 #endif
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_batchnorm_stream.h`

 * *Files 8% similar despite different names*

```diff
@@ -8,16 +8,16 @@
 
 namespace nnet {
 
 // ****************************************************
 //       Streaming Batch Normalization
 // ****************************************************
 template <class data_T, class res_T, typename CONFIG_T>
-void normalize(stream<data_T> &data, stream<res_T> &res, const typename CONFIG_T::scale_t scale[CONFIG_T::n_in],
-               const typename CONFIG_T::bias_t bias[CONFIG_T::n_in]) {
+void normalize(stream<data_T> &data, stream<res_T> &res, const typename CONFIG_T::scale_t scale[CONFIG_T::n_scale_bias],
+               const typename CONFIG_T::bias_t bias[CONFIG_T::n_scale_bias]) {
 
     constexpr unsigned multiplier_limit = DIV_ROUNDUP(CONFIG_T::n_in, CONFIG_T::reuse_factor);
     constexpr unsigned pipeline = CONFIG_T::n_in / multiplier_limit;
     CONFIG_T::template product<typename data_T::value_type, typename CONFIG_T::scale_t>::limit(multiplier_limit);
 
 BatchNormLoop:
     #pragma ii pipeline
@@ -42,43 +42,43 @@
     }
 }
 
 // ****************************************************
 //       Merged Batch Normalization and Quantized Tanh
 // ****************************************************
 template <class data_T, typename CONFIG_T>
-void normalize_binary_tanh(stream<data_T> &data, stream<nnet::array<ac_int<1, false>, CONFIG_T::n_in>> &res,
-                           const typename data_T::value_type threshold[CONFIG_T::n_in]) {
+void normalize_binary_tanh(stream<data_T> &data, stream<nnet::array<ac_int<1, false>, CONFIG_T::n_scale_bias>> &res,
+                           const typename data_T::value_type threshold[CONFIG_T::n_scale_bias]) {
 
 BinaryNormLoop:
     #pragma ii 1
     for (int i = 0; i < CONFIG_T::n_in / data_T::size; i++) {
         data_T in_data = data.read();
-        nnet::array<ac_int<1, false>, CONFIG_T::n_in> out_data;
+        nnet::array<ac_int<1, false>, CONFIG_T::n_scale_bias> out_data;
 
     BatchNormPack:
         #pragma unroll
         for (int j = 0; j < data_T::size; j++) {
             out_data[j] = (in_data[j] > threshold[i * data_T::size + j]) ? 1 : 0;
         }
 
         res.write(out_data);
     }
 }
 
 template <class data_T, typename CONFIG_T>
-void normalize_ternary_tanh(stream<data_T> &data, stream<nnet::array<ac_int<2, true>, CONFIG_T::n_in>> &res,
-                            const typename data_T::value_type threshold_hi[CONFIG_T::n_in],
-                            const typename data_T::value_type threshold_lo[CONFIG_T::n_in]) {
+void normalize_ternary_tanh(stream<data_T> &data, stream<nnet::array<ac_int<2, true>, CONFIG_T::n_scale_bias>> &res,
+                            const typename data_T::value_type threshold_hi[CONFIG_T::n_scale_bias],
+                            const typename data_T::value_type threshold_lo[CONFIG_T::n_scale_bias]) {
 
 TernaryNormLoop:
     #pragma ii 1
     for (int i = 0; i < CONFIG_T::n_in / data_T::size; i++) {
         data_T in_data = data.read();
-        nnet::array<ac_int<2, true>, CONFIG_T::n_in> out_data;
+        nnet::array<ac_int<2, true>, CONFIG_T::n_scale_bias> out_data;
 
     BatchNormPack:
         #pragma unroll
         for (int j = 0; j < data_T::size; j++) {
             int norm_index = i * data_T::size + j;
             if (in_data[j] > threshold_hi[norm_index])
                 out_data[j] = 1;
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_common.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_common.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv1d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_conv2d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_compressed.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_compressed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_dense_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_embed_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_helpers.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_helpers.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_merge_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_mult.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_mult.h`

 * *Files 4% similar despite different names*

```diff
@@ -85,32 +85,33 @@
         r_T y = static_cast<r_T>(a) << w.weight;
         // negate or not depending on weight sign
         return w.sign == 1 ? y : static_cast<r_T>(-y);
     }
 };
 } // namespace product
 
+// TO-DO: These may need extra variants if ac_int types are used in more places
 template <class data_T, class res_T, typename CONFIG_T>
 inline typename std::enable_if<std::is_same<data_T, ac_int<1, false>>::value &&
                                    std::is_same<typename CONFIG_T::weight_t, ac_int<1, false>>::value,
                                ac_int<nnet::ceillog2(CONFIG_T::n_in) + 2, true>>::type
 cast(typename CONFIG_T::accum_t x) {
-    return (ac_int<nnet::ceillog2(CONFIG_T::n_in) + 2, true>)(x - CONFIG_T::n_in / 2) * 2;
+    return static_cast<ac_int<nnet::ceillog2(CONFIG_T::n_in) + 2, true>>(((x - CONFIG_T::n_in / 2) * 2).to_ac_int());
 }
 
 template <class data_T, class res_T, typename CONFIG_T>
 inline typename std::enable_if<std::is_same<data_T, ac_int<1, false>>::value &&
                                    !std::is_same<typename CONFIG_T::weight_t, ac_int<1, false>>::value,
                                res_T>::type
 cast(typename CONFIG_T::accum_t x) {
-    return (res_T)x;
+    return static_cast<res_T>(x);
 }
 
 template <class data_T, class res_T, typename CONFIG_T>
 inline typename std::enable_if<(!std::is_same<data_T, ac_int<1, false>>::value), res_T>::type
 cast(typename CONFIG_T::accum_t x) {
-    return (res_T)x;
+    return static_cast<res_T>(x);
 }
 
 } // namespace nnet
 
 #endif
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_padding_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_pooling_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_activation.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_activation.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_recurrent_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_resize_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose_stream.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_transpose_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_types.h` & `hls4ml-0.7.1/hls4ml/templates/quartus/firmware/nnet_utils/nnet_types.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_bridge.cpp` & `hls4ml-0.7.1/hls4ml/templates/quartus/myproject_bridge.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_test_parallel.cpp` & `hls4ml-0.7.1/hls4ml/templates/quartus/myproject_test_parallel.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/quartus/myproject_test_stream.cpp` & `hls4ml-0.7.1/hls4ml/templates/quartus/myproject_test_stream.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv1d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_conv2d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_dense_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_dense_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_dense_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_dense_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_pooling.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_pooling.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_pooling_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_pooling_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv1d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv1d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv2d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vitis/nnet_utils/nnet_sepconv2d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_common.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_common.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_decl.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_decl.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_base.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_base.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_ref.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_ref.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_fixed_special.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_fixed_special.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_base.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_base.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_ref.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_ref.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_int_special.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_int_special.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/ap_shift_reg.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/ap_shift_reg.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/etc/ap_private.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/etc/ap_private.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/hls_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/hls_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/ap_types/utils/x_hls_utils.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/ap_types/utils/x_hls_utils.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/build_lib.sh` & `hls4ml-0.7.1/hls4ml/templates/vivado/build_lib.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/build_prj.tcl` & `hls4ml-0.7.1/hls4ml/templates/vivado/build_prj.tcl`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/firmware/myproject.cpp` & `hls4ml-0.7.1/hls4ml/templates/vivado/firmware/myproject.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/myproject_bridge.cpp` & `hls4ml-0.7.1/hls4ml/templates/vivado/myproject_bridge.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/myproject_test.cpp` & `hls4ml-0.7.1/hls4ml/templates/vivado/myproject_test.cpp`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_activation.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_activation.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_activation_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_activation_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_array.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_array.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm.h`

 * *Files 3% similar despite different names*

```diff
@@ -65,43 +65,45 @@
 // ****************************************************
 //       Merged Batch Normalization and Quantized Tanh
 // ****************************************************
 struct batchnorm_quantized_tanh_config {
     // Layer Sizes
     static const unsigned n_in = 10;
     static const unsigned n_filt = -1;
+    static const unsigned n_scale_bias = 10;
 
     // Resource reuse info
     static const unsigned io_type = io_parallel;
     static const unsigned reuse_factor = 1;
     static const unsigned n_zeros = 0;
 };
 
 template <class data_T, typename CONFIG_T>
-void normalize_binary_tanh(data_T data[CONFIG_T::n_in], ap_uint<1> res[CONFIG_T::n_in], data_T threshold[CONFIG_T::n_in]) {
+void normalize_binary_tanh(data_T data[CONFIG_T::n_in], ap_uint<1> res[CONFIG_T::n_in],
+                           data_T threshold[CONFIG_T::n_scale_bias]) {
     #pragma HLS PIPELINE
     #pragma HLS ARRAY_PARTITION variable=res complete
 
     data_T datareg;
     ap_uint<1> cache;
     for (int ii = 0; ii < CONFIG_T::n_in; ii++) {
         datareg = data[ii];
         int norm_index = CONFIG_T::n_filt == -1 ? ii : ii % CONFIG_T::n_filt;
         if (datareg > threshold[norm_index])
             cache = 1;
         else
             cache = 0;
 
-        res[ii] = (ap_uint<1>)cache;
+        res[ii] = cache;
     }
 }
 
 template <class data_T, typename CONFIG_T>
-void normalize_ternary_tanh(data_T data[CONFIG_T::n_in], ap_int<2> res[CONFIG_T::n_in], data_T threshold_hi[CONFIG_T::n_in],
-                            data_T threshold_lo[CONFIG_T::n_in]) {
+void normalize_ternary_tanh(data_T data[CONFIG_T::n_in], ap_int<2> res[CONFIG_T::n_in],
+                            data_T threshold_hi[CONFIG_T::n_scale_bias], data_T threshold_lo[CONFIG_T::n_scale_bias]) {
     #pragma HLS PIPELINE
     #pragma HLS ARRAY_PARTITION variable=res complete
 
     data_T datareg;
     ap_int<2> cache;
     for (int ii = 0; ii < CONFIG_T::n_in; ii++) {
         datareg = data[ii];
@@ -109,14 +111,14 @@
         if (datareg > threshold_hi[norm_index])
             cache = 1;
         else if (datareg <= threshold_lo[norm_index])
             cache = -1;
         else
             cache = 0;
 
-        res[ii] = (ap_int<2>)cache;
+        res[ii] = cache;
     }
 }
 
 } // namespace nnet
 
 #endif
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_batchnorm_stream.h`

 * *Files 7% similar despite different names*

```diff
@@ -47,49 +47,49 @@
     }
 }
 
 // ****************************************************
 //       Merged Batch Normalization and Quantized Tanh
 // ****************************************************
 template <class data_T, typename CONFIG_T>
-void normalize_binary_tanh(hls::stream<data_T> &data, hls::stream<nnet::array<ap_uint<1>, CONFIG_T::n_in>> &res,
-                           typename data_T::value_type threshold[CONFIG_T::n_in]) {
+void normalize_binary_tanh(hls::stream<data_T> &data, hls::stream<nnet::array<ap_uint<1>, CONFIG_T::n_scale_bias>> &res,
+                           typename data_T::value_type threshold[CONFIG_T::n_scale_bias]) {
     #pragma HLS ARRAY_PARTITION variable=threshold complete
 
 BinaryNormLoop:
     for (int i = 0; i < CONFIG_T::n_in / data_T::size; i++) {
         #pragma HLS PIPELINE
 
         data_T in_data = data.read();
-        nnet::array<ap_uint<1>, CONFIG_T::n_in> out_data;
+        nnet::array<ap_uint<1>, CONFIG_T::n_scale_bias> out_data;
         PRAGMA_DATA_PACK(out_data)
 
     BatchNormPack:
         for (int j = 0; j < data_T::size; j++) {
             #pragma HLS UNROLL
             out_data[j] = (in_data[j] > threshold[i * data_T::size + j]) ? 1 : 0;
         }
 
         res.write(out_data);
     }
 }
 
 template <class data_T, typename CONFIG_T>
-void normalize_ternary_tanh(hls::stream<data_T> &data, hls::stream<nnet::array<ap_int<2>, CONFIG_T::n_in>> &res,
-                            typename data_T::value_type threshold_hi[CONFIG_T::n_in],
-                            typename data_T::value_type threshold_lo[CONFIG_T::n_in]) {
+void normalize_ternary_tanh(hls::stream<data_T> &data, hls::stream<nnet::array<ap_int<2>, CONFIG_T::n_scale_bias>> &res,
+                            typename data_T::value_type threshold_hi[CONFIG_T::n_scale_bias],
+                            typename data_T::value_type threshold_lo[CONFIG_T::n_scale_bias]) {
     #pragma HLS ARRAY_PARTITION variable=threshold_hi complete
     #pragma HLS ARRAY_PARTITION variable=threshold_lo complete
 
 TernaryNormLoop:
     for (int i = 0; i < CONFIG_T::n_in / data_T::size; i++) {
         #pragma HLS PIPELINE
 
         data_T in_data = data.read();
-        nnet::array<ap_int<2>, CONFIG_T::n_in> out_data;
+        nnet::array<ap_int<2>, CONFIG_T::n_scale_bias> out_data;
         PRAGMA_DATA_PACK(out_data)
 
     BatchNormPack:
         for (int j = 0; j < data_T::size; j++) {
             #pragma HLS UNROLL
 
             int norm_index = i * data_T::size + j;
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_code_gen.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_code_gen.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_common.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_common.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_latency.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_latency.h`

 * *Files 16% similar despite different names*

```diff
@@ -28,55 +28,61 @@
     #pragma HLS ARRAY_PARTITION variable=biases complete
 
     // Limit multipliers to control parallelization
     #pragma HLS ALLOCATION operation instances=mul limit=CONFIG_T::mult_config::multiplier_limit
 
 PartitionLoop:
     for (int i_part = 0; i_part < CONFIG_T::n_partitions; i_part++) {
-        #pragma HLS PIPELINE II=CONFIG_T::reuse_factor
+        #pragma HLS PIPELINE II=CONFIG_T::reuse_factor rewind
 
         CONFIG_T::template fill_buffer<data_T, CONFIG_T>::fill_buffer(data, data_buf, i_part);
 
     PixelLoop:
         for (unsigned i_pxl = 0; i_pxl < CONFIG_T::n_pixels; i_pxl++) {
             #pragma HLS UNROLL
 
             data_T cache;
 
         // Do the matrix-multiply
         Product1:
             for (int i_in = 0; i_in < mult_n_in; i_in++) {
+                #pragma HLS UNROLL
                 cache = data_buf[i_pxl][i_in];
             Product2:
                 for (int i_out = 0; i_out < mult_n_out; i_out++) {
+                    #pragma HLS UNROLL
                     mult[i_in * mult_n_out + i_out] =
                         CONFIG_T::mult_config::template product<data_T, typename CONFIG_T::mult_config::weight_t>::product(
                             cache, weights[i_in * mult_n_out + i_out]);
                 }
             }
 
         // Initialize accumulator with input biases
         ResetAccum:
             for (int i_acc = 0; i_acc < mult_n_out; i_acc++) {
+                #pragma HLS UNROLL
                 acc[i_acc] = (typename CONFIG_T::accum_t)biases[i_acc];
             }
 
         // Accumulate multiplication result
         Accum1:
             for (int i_in = 0; i_in < mult_n_in; i_in++) {
+                #pragma HLS UNROLL
             Accum2:
                 for (int i_out = 0; i_out < mult_n_out; i_out++) {
+                    #pragma HLS UNROLL
                     acc[i_out] += mult[i_in * mult_n_out + i_out];
                 }
             }
 
         // Cast to "res_t" type
         Result:
             for (int i_res = 0; i_res < mult_n_out; i_res++) {
-                *(res++) = cast<data_T, res_T, CONFIG_T>(acc[i_res]);
+                #pragma HLS UNROLL
+                *(res++) = cast<data_T, res_T, typename CONFIG_T::mult_config>(acc[i_res]);
             }
         }
     }
 }
 
 } // namespace nnet
 #endif
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv1d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_latency.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_latency.h`

 * *Files 25% similar despite different names*

```diff
@@ -29,55 +29,61 @@
     #pragma HLS ARRAY_PARTITION variable=biases complete
 
     // Limit multipliers to control parallelization
     #pragma HLS ALLOCATION operation instances=mul limit=CONFIG_T::mult_config::multiplier_limit
 
 PartitionLoop:
     for (int i_part = 0; i_part < CONFIG_T::n_partitions; i_part++) {
-        #pragma HLS PIPELINE II=CONFIG_T::reuse_factor
+        #pragma HLS PIPELINE II=CONFIG_T::reuse_factor rewind
 
         CONFIG_T::template fill_buffer<data_T, CONFIG_T>::fill_buffer(data, data_buf, i_part);
 
     PixelLoop:
         for (unsigned i_pxl = 0; i_pxl < CONFIG_T::n_pixels; i_pxl++) {
             #pragma HLS UNROLL
 
             data_T cache;
 
         // Do the matrix-multiply
         Product1:
             for (int i_in = 0; i_in < mult_n_in; i_in++) {
+                #pragma HLS UNROLL
                 cache = data_buf[i_pxl][i_in];
             Product2:
                 for (int i_out = 0; i_out < mult_n_out; i_out++) {
+                    #pragma HLS UNROLL
                     mult[i_in * mult_n_out + i_out] =
                         CONFIG_T::mult_config::template product<data_T, typename CONFIG_T::mult_config::weight_t>::product(
                             cache, weights[i_in * mult_n_out + i_out]);
                 }
             }
 
         // Initialize accumulator with input biases
         ResetAccum:
             for (int i_acc = 0; i_acc < mult_n_out; i_acc++) {
+                #pragma HLS UNROLL
                 acc[i_acc] = (typename CONFIG_T::accum_t)biases[i_acc];
             }
 
         // Accumulate multiplication result
         Accum1:
             for (int i_in = 0; i_in < mult_n_in; i_in++) {
+                #pragma HLS UNROLL
             Accum2:
                 for (int i_out = 0; i_out < mult_n_out; i_out++) {
+                    #pragma HLS UNROLL
                     acc[i_out] += mult[i_in * mult_n_out + i_out];
                 }
             }
 
         // Cast to "res_t" type
         Result:
             for (int i_res = 0; i_res < mult_n_out; i_res++) {
-                *(res++) = cast<data_T, res_T, CONFIG_T>(acc[i_res]);
+                #pragma HLS UNROLL
+                *(res++) = cast<data_T, res_T, typename CONFIG_T::mult_config>(acc[i_res]);
             }
         }
     }
 }
 
 } // namespace nnet
 #endif
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv2d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_conv_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_conv_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_compressed.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_compressed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_latency.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_latency.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_resource.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_resource.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_dense_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_dense_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_embed.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_embed.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_embed_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_embed_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_garnet.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_garnet.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_helpers.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_helpers.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_image.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_image.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_image_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_image_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_merge.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_merge.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_merge_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_merge_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_mult.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_mult.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_padding.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_padding.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_padding_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_padding_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_pooling.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_pooling.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_pooling_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_pooling_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_recr_activations.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_recr_activations.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_recurrent.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_recurrent.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv1d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv1d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv2d_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv2d_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_sepconv_stream.h`

 * *Files 0% similar despite different names*

```diff
@@ -50,15 +50,15 @@
         }
     }
 
 // Cast to "res_t" type
 Result:
     for (int ires = 0; ires < CONFIG_T::n_chan; ires++) {
         #pragma HLS UNROLL
-        res[ires] = cast<data_T, res_T, CONFIG_T>(acc[ires]);
+        res[ires] = cast<data_T, res_T, typename CONFIG_T::mult_config>(acc[ires]);
     }
 }
 
 template <class data_T, class res_T, typename CONFIG_T>
 void depthwise_mult_buffer(hls::stream<typename data_T::value_type> data_window[CONFIG_T::kernel_size * CONFIG_T::n_chan],
                            res_T &res_pack, hls::stream<res_T> &res_stream, unsigned &outputs_ready,
                            typename CONFIG_T::weight_t weights[CONFIG_T::kernel_size * CONFIG_T::n_chan],
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_stream.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_stream.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado/nnet_utils/nnet_types.h` & `hls4ml-0.7.1/hls4ml/templates/vivado/nnet_utils/nnet_types.h`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_read_master.sv` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_read_master.sv`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_write_master.sv` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_axi_write_master.sv`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_control_s_axi.v` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_control_s_axi.v`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_counter.sv` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_counter.sv`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_int.sv` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/krnl_rtl_int.sv`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/myproject_kernel.v` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/krnl_rtl_src/myproject_kernel.v`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/axi_stream_driver.py` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/python_drivers/axi_stream_driver.py`

 * *Files 13% similar despite different names*

```diff
@@ -8,65 +8,62 @@
     def __init__(self, xclbin_name, dtbo=None, download=True, ignore_version=False, device=None):
 
         super().__init__(xclbin_name, dtbo=dtbo, download=download, ignore_version=ignore_version, device=device)
         self.input_buffer = None
         self.output_buffer = None
 
     def allocate_mem(self, X_shape, y_shape, dtype=np.float32, trg_in=None, trg_out=None):
-        """
-        Buffer allocation in the card memory
-        Parameters
-        ----------
-        X_shape : input buffer shape.
-        y_shape : output buffer shape.
-        dtype   : the data type of the elements of the input/output vectors.
-                  Note: it should be set depending on the interface of the accelerator; if it uses 'float'
-                  types for the 'data' AXI-Stream field, 'np.float32' dtype is the correct one to use.
-                  Instead if it uses 'ap_fixed<A,B>', 'np.intA' is the correct one to use (note that A cannot
-                  any integer value, but it can assume {..., 8, 16, 32, ...} values. Check `numpy`
-                  doc for more info).
-                  In this case the encoding/decoding has to be computed by the host machine. For example for
-                  'ap_fixed<16,6>' type the following 2 functions are the correct one to use for encode/decode
-                  'float' -> 'ap_fixed<16,6>':
-                  ```
+        """Buffer allocation in the accelerator's memory.
+
+        Args:
+            X_shape (list): Input buffer shape.
+            y_shape (list): Output buffer shape.
+            dtype (dtype, optional): The data type of the elements of the input/output tensors. Must be an instance of
+                numpy dtype. Defaults to np.float32.
+
+                It should be set depending on the interface of the accelerator; if it uses 'float'
+                data type for the 'data' AXI-Stream field, 'np.float32' dtype must be used. Instead if it uses
+                'ap_fixed<A,B>', 'np.intA' is the correct dtype to use. Note that A cannot any integer value, but it can
+                assume power of 2 values, i.e., {..., 8, 16, 32, ...}. Check `numpy` documentation for more information.
+                In this case the encoding/decoding has to be computed by the host machine. For example for
+                'ap_fixed<16,6>' type the following 2 functions are the correct one to use for encode/decode
+                'float' -> 'ap_fixed<16,6>'::
+
                     def encode(xi):
                         return np.int16(round(xi * 2**10)) # note 2**10 = 2**(A-B)
                     def decode(yi):
                         return yi * 2**-10
                     encode_v = np.vectorize(encode) # to apply them element-wise
                     decode_v = np.vectorize(decode)
-                  ```
-        trg_in  : input buffer target memory. By default the v++ command
-                  set it to HBM[0] for alveo-u50.
-        trg_out : output buffer target memory.By default the v++ command
-                  set it to HBM[0] for alveo-u50.
-
-        Assigns
-        -------
-        input_buffer : input PYNQ buffer, must be allocated first and just once.
-        output_buffer : output PYNQ buffer, must be allocated first and just once.
-        input_buffer, output_buffer : input and output PYNQ buffers
 
+            trg_in (optional): Input buffer target memory. By default the v++ command set it to HBM[0] for
+                alveo-u50. Defaults to None.
+            trg_out (optional): Output buffer target memory. By default the v++ command set it to HBM[0] for
+                alveo-u50. Defaults to None.
         """
         self.input_buffer = allocate(shape=X_shape, dtype=dtype, target=trg_in)
         self.output_buffer = allocate(shape=y_shape, dtype=dtype, target=trg_out)
 
-    def predict(self, X, y_shape, dtype=np.float32, debug=None, profile=False, encode=None, decode=None):
-        """
-        Obtain the predictions of the NN implemented in the FPGA.
-        Parameters:
-        - X : the input vector. Should be numpy ndarray.
-        - y_shape : the shape of the output vector. Needed to the accelerator to set the TLAST bit properly and
-                    for sizing the output vector shape.
-        - dtype   : the data type of the elements of the input/output vectors.
-        - debug : boolean, if set the function will print information about the data transfers status.
-        - profile : boolean. Set it to `True` to print the performance of the algorithm in term of `inference/s`.
-        - encode/decode: function pointers. See `dtype` section for more information.
-        - return: an output array based on `np.ndarray` with a shape equal to `y_shape` and a `dtype` equal to
-                  the namesake parameter.
+    def predict(self, X, y_shape, dtype=np.float32, debug=False, profile=False, encode=None, decode=None):
+        """Obtain the predictions of the NN implemented in the FPGA.
+
+        Args:
+            X (ndarray): The input tensor.
+            y_shape (list): The shape of the output tensor, needed by the accelerator to set the TLAST bit properly.
+            dtype (dtype, optional): The data type of the elements of the input/output tensors. Must be an instance of
+                numpy dtype. Defaults to np.float32.
+            debug (bool, optional): If set, the function will print information about the data transfers status.
+                Defaults to False.
+            profile (bool, optional): If set, the function will print the performance of the algorithm in terms of
+                inference/s. Defaults to False.
+            encode (Callable, optional): Function to transform the input tensor. Defaults to None.
+            decode (Callable, optional): Function to transform the output tensor. Defaults to None.
+
+        Returns:
+            _type_: A ``np.ndarray`` with a shape equal of ``y_shape`` and ``dtype`` data type.
         """
         self.allocate_mem(X_shape=X.shape, y_shape=y_shape, dtype=dtype)
         if profile:
             timea = datetime.now()
         if encode is not None:
             X = encode(X)
         in_size = np.prod(X.shape)
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/axi_stream_design.tcl` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/alveo/tcl_scripts/axi_stream_design.tcl`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/build_lib.sh` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/build_lib.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/axi_stream_driver.py` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/python_drivers/axi_stream_driver.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_lite_design.tcl` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_lite_design.tcl`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_stream_design.tcl` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/pynq-z2/tcl_scripts/axi_stream_design.tcl`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/axi_stream_driver.py` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/python_drivers/axi_stream_driver.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/axi_stream_design.tcl` & `hls4ml-0.7.1/hls4ml/templates/vivado_accelerator/zcu102/tcl_scripts/axi_stream_design.tcl`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/utils/config.py` & `hls4ml-0.7.1/hls4ml/utils/config.py`

 * *Files 0% similar despite different names*

```diff
@@ -95,15 +95,15 @@
     This function serves as the initial step in creating the custom conversion configuration.
     Users are advised to inspect the returned object to tweak the conversion configuration.
     The return object can be passed as `hls_config` parameter to `convert_from_keras_model`.
 
     Args:
         model: Keras model
         granularity (str, optional): Granularity of the created config. Defaults to 'model'.
-            Can be set to 'model', 'type' and 'layer'.
+            Can be set to 'model', 'type' and 'name'.
 
             Granularity can be used to generate a more verbose config that can be fine-tuned.
             The default granularity ('model') will generate config keys that apply to the whole
             model, so changes to the keys will affect the entire model. 'type' granularity will
             generate config keys that affect all layers of a given type, while the 'name' granularity
             will generate config keys for every layer separately, allowing for highly specific
             configuration tweaks.
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/utils/example_models.py` & `hls4ml-0.7.1/hls4ml/utils/example_models.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/utils/fixed_point_utils.py` & `hls4ml-0.7.1/hls4ml/utils/fixed_point_utils.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/utils/plot.py` & `hls4ml-0.7.1/hls4ml/utils/plot.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/utils/string_utils.py` & `hls4ml-0.7.1/hls4ml/utils/string_utils.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/writer/quartus_writer.py` & `hls4ml-0.7.1/hls4ml/writer/quartus_writer.py`

 * *Files 0% similar despite different names*

```diff
@@ -73,14 +73,15 @@
         h_file.write(f"#ifndef {var.name.upper()}_H_\n")
         h_file.write(f"#define {var.name.upper()}_H_\n")
         h_file.write("\n")
 
         rf = int(layer.get_attr('reuse_factor', 1))
         weight_header = '#ifdef __INTELFPGA_COMPILER__\n'
 
+        weight_size = 0
         if isinstance(layer, (Conv2D, Conv2DBatchnorm)):
             weight_size = (
                 layer.get_attr('impl_filt_height')
                 * layer.get_attr('impl_filt_width')
                 * layer.get_attr('n_filt')
                 * layer.get_attr('n_chan')
             )
```

### Comparing `hls4ml-0.7.0rc1/hls4ml/writer/vitis_writer.py` & `hls4ml-0.7.1/hls4ml/writer/vitis_writer.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/writer/vivado_accelerator_writer.py` & `hls4ml-0.7.1/hls4ml/writer/vivado_accelerator_writer.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml/writer/vivado_writer.py` & `hls4ml-0.7.1/hls4ml/writer/vivado_writer.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/hls4ml.egg-info/PKG-INFO` & `hls4ml-0.7.1/hls4ml.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hls4ml
-Version: 0.7.0rc1
+Version: 0.7.1
 Summary: Machine learning in FPGAs using HLS
 Home-page: https://fastmachinelearning.org/hls4ml
 Author: hls4ml Team
 License: Apache-2.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
@@ -86,15 +86,15 @@
 If you use this software in a publication, please cite the software
 ```bibtex
 @software{fastml_hls4ml,
   author       = {{FastML Team}},
   title        = {fastmachinelearning/hls4ml},
   year         = 2023,
   publisher    = {Zenodo},
-  version      = {v0.7.0rc1},
+  version      = {v0.7.1},
   doi          = {10.5281/zenodo.1201549},
   url          = {https://github.com/fastmachinelearning/hls4ml}
 }
 ```
 and first publication:
 ```bibtex
 @article{Duarte:2018ite,
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
-Metadata-Version: 2.1 Name: hls4ml Version: 0.7.0rc1 Summary: Machine learning
-in FPGAs using HLS Home-page: https://fastmachinelearning.org/hls4ml Author:
+Metadata-Version: 2.1 Name: hls4ml Version: 0.7.1 Summary: Machine learning in
+FPGAs using HLS Home-page: https://fastmachinelearning.org/hls4ml Author:
 hls4ml Team License: Apache-2.0 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers Classifier: Intended Audience ::
 Science/Research Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: C++ Classifier: Programming Language ::
 Python :: 3 Classifier: Programming Language :: Python :: 3 :: Only Classifier:
 Topic :: Software Development :: Libraries Classifier: Topic :: Software
 Development :: Libraries :: Python Modules Requires-Python: >=3.7 Description-
@@ -42,15 +42,15 @@
 products/design-tools/vivado/integration/esl-design.html)) Note: Vitis HLS is
 not yet supported. Vivado HLS versions between 2018.2 and 2020.1 are
 recommended. ```Python # Use Vivado HLS to synthesize the model # This might
 take several minutes hls_model.build() # Print out the report if you want
 hls4ml.report.read_vivado_report('my-hls-test') ``` # Citation If you use this
 software in a publication, please cite the software ```bibtex @software
 {fastml_hls4ml, author = {{FastML Team}}, title = {fastmachinelearning/hls4ml},
-year = 2023, publisher = {Zenodo}, version = {v0.7.0rc1}, doi = {10.5281/
+year = 2023, publisher = {Zenodo}, version = {v0.7.1}, doi = {10.5281/
 zenodo.1201549}, url = {https://github.com/fastmachinelearning/hls4ml} } ```
 and first publication: ```bibtex @article{Duarte:2018ite, author = "Duarte,
 Javier and others", title = "{Fast inference of deep neural networks in FPGAs
 for particle physics}", eprint = "1804.06913", archivePrefix = "arXiv",
 primaryClass = "physics.ins-det", reportNumber = "FERMILAB-PUB-18-089-E", doi =
 "10.1088/1748-0221/13/07/P07027", journal = "JINST", volume = "13", number =
 "07", pages = "P07027", year = "2018" } ``` Additionally, if you use specific
```

### Comparing `hls4ml-0.7.0rc1/hls4ml.egg-info/SOURCES.txt` & `hls4ml-0.7.1/hls4ml.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -422,14 +422,15 @@
 test/docker/README.md
 test/docker/install_config-2017.2.txt
 test/docker/install_config.txt
 test/pytest/ci-template.yml
 test/pytest/generate_ci_yaml.py
 test/pytest/test_activations.py
 test/pytest/test_batchnorm.py
+test/pytest/test_binary_cnn.py
 test/pytest/test_bram_factor.py
 test/pytest/test_causalpadding.py
 test/pytest/test_clone_flatten.py
 test/pytest/test_cnn_mnist.py
 test/pytest/test_cnn_mnist_qkeras.py
 test/pytest/test_conv1d.py
 test/pytest/test_conv1d_narrow.py
```

### Comparing `hls4ml-0.7.0rc1/scripts/hls4ml` & `hls4ml-0.7.1/scripts/hls4ml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/setup.cfg` & `hls4ml-0.7.1/setup.cfg`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/build-prj.sh` & `hls4ml-0.7.1/test/build-prj.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/cleanup.sh` & `hls4ml-0.7.1/test/cleanup.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/compare-reports.sh` & `hls4ml-0.7.1/test/compare-reports.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/convert-keras-models.sh` & `hls4ml-0.7.1/test/convert-keras-models.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/convert-onnx-models.sh` & `hls4ml-0.7.1/test/convert-onnx-models.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/convert-pytorch-models.sh` & `hls4ml-0.7.1/test/convert-pytorch-models.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/docker/Dockerfile` & `hls4ml-0.7.1/test/docker/Dockerfile`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/docker/README.md` & `hls4ml-0.7.1/test/docker/README.md`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/docker/install_config-2017.2.txt` & `hls4ml-0.7.1/test/docker/install_config-2017.2.txt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/docker/install_config.txt` & `hls4ml-0.7.1/test/docker/install_config.txt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/gather-reports.sh` & `hls4ml-0.7.1/test/gather-reports.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/hls4ml-keras-test.sh` & `hls4ml-0.7.1/test/hls4ml-keras-test.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/hls4ml-onnx-test.sh` & `hls4ml-0.7.1/test/hls4ml-onnx-test.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/hls4ml-pytorch-test.sh` & `hls4ml-0.7.1/test/hls4ml-pytorch-test.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/keras-models.txt` & `hls4ml-0.7.1/test/keras-models.txt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/keras-to-hls.sh` & `hls4ml-0.7.1/test/keras-to-hls.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/onnx-models.txt` & `hls4ml-0.7.1/test/onnx-models.txt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/onnx-to-hls.sh` & `hls4ml-0.7.1/test/onnx-to-hls.sh`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/ci-template.yml` & `hls4ml-0.7.1/test/pytest/ci-template.yml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/generate_ci_yaml.py` & `hls4ml-0.7.1/test/pytest/generate_ci_yaml.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_activations.py` & `hls4ml-0.7.1/test/pytest/test_activations.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_batchnorm.py` & `hls4ml-0.7.1/test/pytest/test_batchnorm.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_bram_factor.py` & `hls4ml-0.7.1/test/pytest/test_bram_factor.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_causalpadding.py` & `hls4ml-0.7.1/test/pytest/test_causalpadding.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_clone_flatten.py` & `hls4ml-0.7.1/test/pytest/test_clone_flatten.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_cnn_mnist.py` & `hls4ml-0.7.1/test/pytest/test_cnn_mnist.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_cnn_mnist_qkeras.py` & `hls4ml-0.7.1/test/pytest/test_cnn_mnist_qkeras.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_conv1d.py` & `hls4ml-0.7.1/test/pytest/test_conv1d.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_conv1d_narrow.py` & `hls4ml-0.7.1/test/pytest/test_conv1d_narrow.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_conv2d_narrow.py` & `hls4ml-0.7.1/test/pytest/test_conv2d_narrow.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_embed.py` & `hls4ml-0.7.1/test/pytest/test_embed.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_extensions.py` & `hls4ml-0.7.1/test/pytest/test_extensions.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_flows.py` & `hls4ml-0.7.1/test/pytest/test_flows.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_garnet.py` & `hls4ml-0.7.1/test/pytest/test_garnet.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_globalpooling.py` & `hls4ml-0.7.1/test/pytest/test_globalpooling.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_graph.py` & `hls4ml-0.7.1/test/pytest/test_graph.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_keras_api.py` & `hls4ml-0.7.1/test/pytest/test_keras_api.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_keras_h5_loader.py` & `hls4ml-0.7.1/test/pytest/test_keras_h5_loader.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_merge.py` & `hls4ml-0.7.1/test/pytest/test_merge.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_pointwiseconv.py` & `hls4ml-0.7.1/test/pytest/test_pointwiseconv.py`

 * *Files 24% similar despite different names*

```diff
@@ -123,7 +123,34 @@
         model, hls_config=config, output_dir=output_dir, io_type=io_type, backend=backend
     )
     hls_model.compile()
     hls_prediction = hls_model.predict(X_input).reshape(keras_prediction.shape)
 
     assert 'Pointwise' in list(hls_model.graph.values())[1].class_name
     np.testing.assert_allclose(hls_prediction, keras_prediction, rtol=0, atol=0.001)
+
+
+@pytest.mark.parametrize('strategy', ['Latency', 'Resource'])
+def test_pointwise_config(strategy):
+    model = tf.keras.models.Sequential()
+    input_shape = (8, 8, 3)
+    model.add(
+        Conv2D(
+            filters=8,
+            kernel_size=(1, 1),
+            input_shape=input_shape,
+            kernel_initializer='normal',
+            use_bias=False,
+            name='conv2d_1x1',
+        )
+    )
+
+    model.compile(optimizer='adam', loss='mse')
+
+    config = hls4ml.utils.config_from_keras_model(model, granularity='name')
+    config['Model']['Strategy'] = strategy
+    config['LayerName']['conv2d_1x1']['Strategy'] = strategy  # Will fail if the strategy is not lowercase
+    output_dir = str(test_root_path / f'hls4mlprj_pointwise2d_config_{strategy}')
+
+    hls_model = hls4ml.converters.convert_from_keras_model(model, hls_config=config, output_dir=output_dir)
+    # Model will fail to compile if strategy was set incorrectly
+    hls_model.compile()
```

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_pooling.py` & `hls4ml-0.7.1/test/pytest/test_pooling.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_precision_parsing.py` & `hls4ml-0.7.1/test/pytest/test_precision_parsing.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_qkeras.py` & `hls4ml-0.7.1/test/pytest/test_qkeras.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_report/myproject_csynth.rpt` & `hls4ml-0.7.1/test/pytest/test_report/myproject_csynth.rpt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_report/myproject_csynth.xml` & `hls4ml-0.7.1/test/pytest/test_report/myproject_csynth.xml`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_report/vivado_hls.app` & `hls4ml-0.7.1/test/pytest/test_report/vivado_hls.app`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_report/vivado_synth.rpt` & `hls4ml-0.7.1/test/pytest/test_report/vivado_synth.rpt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_report.py` & `hls4ml-0.7.1/test/pytest/test_report.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_reshape.py` & `hls4ml-0.7.1/test/pytest/test_reshape.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_rnn.py` & `hls4ml-0.7.1/test/pytest/test_rnn.py`

 * *Files 10% similar despite different names*

```diff
@@ -80,15 +80,16 @@
         (GRU, 'Vitis', 'io_stream'),
         (GRU, 'Quartus', 'io_parallel'),
         (GRU, 'Quartus', 'io_stream'),
     ],
 )
 @pytest.mark.parametrize('return_sequences', [True, False])
 @pytest.mark.parametrize('static', [True, False])
-def test_rnn_accuracy(rnn_layer, return_sequences, backend, io_type, static):
+@pytest.mark.parametrize('strategy', ['latency', 'resource'])
+def test_rnn_accuracy(rnn_layer, return_sequences, backend, io_type, strategy, static):
     # Subtract 0.5 to include negative values
     input_shape = (12, 8)
     X = np.random.rand(50, *input_shape) - 0.5
 
     layer_name = rnn_layer.__class__.__name__.lower()
     keras_model = Sequential()
     keras_model.add(
@@ -105,16 +106,17 @@
     keras_model.compile()
 
     default_precision = 'ap_fixed<32, 16>' if backend in ['Vivado', 'Vitis'] else 'ac_fixed<32, 16, true>'
     hls_config = hls4ml.utils.config_from_keras_model(
         keras_model, granularity='name', default_precision=default_precision, backend=backend
     )
     hls_config['LayerName'][layer_name]['static'] = static
-    prj_name = 'hls4mlprj_rnn_accuracy_{}_static_{}_ret_seq_{}_{}_{}'.format(
-        rnn_layer.__class__.__name__.lower(), int(static), int(return_sequences), backend, io_type
+    hls_config['LayerName'][layer_name]['Strategy'] = strategy
+    prj_name = 'hls4mlprj_rnn_accuracy_{}_static_{}_ret_seq_{}_{}_{}_{}'.format(
+        rnn_layer.__class__.__name__.lower(), int(static), int(return_sequences), backend, io_type, strategy
     )
     output_dir = str(test_root_path / prj_name)
 
     hls_model = hls4ml.converters.convert_from_keras_model(
         keras_model, hls_config=hls_config, output_dir=output_dir, backend=backend, io_type=io_type
     )
     hls_model.compile()
```

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_sepconv2d.py` & `hls4ml-0.7.1/test/pytest/test_sepconv2d.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_softmax.py` & `hls4ml-0.7.1/test/pytest/test_softmax.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_softsign.py` & `hls4ml-0.7.1/test/pytest/test_softsign.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_trace.py` & `hls4ml-0.7.1/test/pytest/test_trace.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_transpose_concat.py` & `hls4ml-0.7.1/test/pytest/test_transpose_concat.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_upsampling.py` & `hls4ml-0.7.1/test/pytest/test_upsampling.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytest/test_zeropadding.py` & `hls4ml-0.7.1/test/pytest/test_zeropadding.py`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytorch-models.txt` & `hls4ml-0.7.1/test/pytorch-models.txt`

 * *Files identical despite different names*

### Comparing `hls4ml-0.7.0rc1/test/pytorch-to-hls.sh` & `hls4ml-0.7.1/test/pytorch-to-hls.sh`

 * *Files identical despite different names*

