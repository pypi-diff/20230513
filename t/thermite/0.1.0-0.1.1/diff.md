# Comparing `tmp/thermite-0.1.0.tar.gz` & `tmp/thermite-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "thermite-0.1.0.tar", last modified: Sat May 13 13:02:18 2023, max compression
+gzip compressed data, was "thermite-0.1.1.tar", last modified: Sat May 13 13:05:52 2023, max compression
```

## Comparing `thermite-0.1.0.tar` & `thermite-0.1.1.tar`

### file list

```diff
@@ -1,85 +1,85 @@
--rw-r--r--   0        0        0       28 2023-05-12 04:49:43.079330 thermite-0.1.0/.gitignore
--rw-r--r--   0        0        0     1082 2023-04-10 14:31:39.097142 thermite-0.1.0/LICENSE
--rw-r--r--   0        0        0     2528 2023-05-11 04:53:09.442923 thermite-0.1.0/Makefile
--rw-r--r--   0        0        0     1469 2023-05-12 05:20:20.459670 thermite-0.1.0/README.md
--rw-r--r--   0        0        0      150 2023-04-10 14:31:39.097142 thermite-0.1.0/conda_env.yaml
--rw-r--r--   0        0        0     2720 2023-05-12 05:11:41.844680 thermite-0.1.0/docs/classes_events.md
--rw-r--r--   0        0        0      938 2023-05-12 05:16:16.617480 thermite-0.1.0/docs/cli_callbacks.md
--rw-r--r--   0        0        0      895 2023-05-12 04:18:22.635421 thermite-0.1.0/docs/css/mkdocstrings.css
--rw-r--r--   0        0        0     1287 2023-05-12 18:40:39.670464 thermite-0.1.0/docs/examples/advanced.md
--rw-r--r--   0        0        0      670 2023-05-12 18:50:10.971243 thermite-0.1.0/docs/examples/basic.md
--rw-r--r--   0        0        0      827 2023-05-12 18:48:45.450048 thermite-0.1.0/docs/examples/dataclasses.md
--rw-r--r--   0        0        0     2200 2023-05-12 18:49:45.658896 thermite-0.1.0/docs/examples/lists.md
--rw-r--r--   0        0        0     2774 2023-05-13 07:00:30.810653 thermite-0.1.0/docs/index.md
--rw-r--r--   0        0        0       44 2023-05-12 03:49:33.471411 thermite-0.1.0/docs/references.md
--rw-r--r--   0        0        0      485 2023-05-11 04:48:46.773541 thermite-0.1.0/examples/adv/config_file.py
--rw-r--r--   0        0        0      194 2023-05-11 04:51:06.318280 thermite-0.1.0/examples/adv/config_file.yml
--rw-r--r--   0        0        0     1933 2023-05-12 18:42:20.727526 thermite-0.1.0/examples/adv/config_file_help.out
--rw-r--r--   0        0        0      865 2023-05-11 04:09:31.484073 thermite-0.1.0/examples/adv/param_transfer.py
--rw-r--r--   0        0        0     1348 2023-05-12 18:42:20.455521 thermite-0.1.0/examples/adv/param_transfer_help.out
--rw-r--r--   0        0        0      138 2023-05-12 18:42:20.579523 thermite-0.1.0/examples/adv/param_transfer_output.out
--rw-r--r--   0        0        0     2404 2023-05-13 07:10:26.493921 thermite-0.1.0/examples/adv/simclr.py
--rw-r--r--   0        0        0     1344 2023-05-12 18:42:18.771487 thermite-0.1.0/examples/basics/adjust_help.out
--rw-r--r--   0        0        0      713 2023-05-07 20:48:38.579351 thermite-0.1.0/examples/basics/adjust_help.py
--rw-r--r--   0        0        0     1811 2023-05-12 18:42:18.899489 thermite-0.1.0/examples/basics/opts_to_args.out
--rw-r--r--   0        0        0      787 2023-05-07 20:48:22.407157 thermite-0.1.0/examples/basics/opts_to_args.py
--rw-r--r--   0        0        0     1816 2023-05-12 18:42:19.031492 thermite-0.1.0/examples/dataclasses/basic.out
--rw-r--r--   0        0        0      269 2023-05-07 18:16:17.299206 thermite-0.1.0/examples/dataclasses/basic.py
--rw-r--r--   0        0        0     1198 2023-05-12 18:42:19.287497 thermite-0.1.0/examples/dataclasses/custom_converter.out
--rw-r--r--   0        0        0      643 2023-05-07 20:23:22.406254 thermite-0.1.0/examples/dataclasses/custom_converter.py
--rw-r--r--   0        0        0     1265 2023-05-12 18:42:19.155494 thermite-0.1.0/examples/dataclasses/with_arguments.out
--rw-r--r--   0        0        0      602 2023-05-07 18:59:28.785876 thermite-0.1.0/examples/dataclasses/with_arguments.py
--rw-r--r--   0        0        0      238 2023-05-08 20:07:43.401327 thermite-0.1.0/examples/lists/default.py
--rw-r--r--   0        0        0     1168 2023-05-12 18:42:19.423500 thermite-0.1.0/examples/lists/default_help.out
--rw-r--r--   0        0        0       57 2023-05-12 18:42:19.571503 thermite-0.1.0/examples/lists/default_output.out
--rw-r--r--   0        0        0      661 2023-05-10 04:26:34.637079 thermite-0.1.0/examples/lists/empty_list.py
--rw-r--r--   0        0        0     1344 2023-05-12 18:42:20.323518 thermite-0.1.0/examples/lists/empty_list_help.out
--rw-r--r--   0        0        0       76 2023-05-12 18:42:20.199515 thermite-0.1.0/examples/lists/empty_list_output.out
--rw-r--r--   0        0        0      653 2023-05-09 03:49:23.733171 thermite-0.1.0/examples/lists/multiple_args.py
--rw-r--r--   0        0        0     1341 2023-05-12 18:42:20.075513 thermite-0.1.0/examples/lists/multiple_args_help.out
--rw-r--r--   0        0        0       78 2023-05-12 18:42:19.943510 thermite-0.1.0/examples/lists/multiple_args_output.out
--rw-r--r--   0        0        0      536 2023-05-08 20:48:32.673845 thermite-0.1.0/examples/lists/var_length_list_opt.py
--rw-r--r--   0        0        0     1192 2023-05-12 18:42:19.819508 thermite-0.1.0/examples/lists/var_length_list_opt_help.out
--rw-r--r--   0        0        0       70 2023-05-12 18:42:19.695505 thermite-0.1.0/examples/lists/var_length_list_opt_output.out
--rw-r--r--   0        0        0      611 2023-05-07 16:09:47.181972 thermite-0.1.0/examples/nested.py
--rw-r--r--   0        0        0      357 2023-05-07 20:46:01.217468 thermite-0.1.0/examples/simple.py
--rw-r--r--   0        0        0      128 2023-05-07 16:09:18.165639 thermite-0.1.0/examples/simple_defaults.yml
--rw-r--r--   0        0        0     1271 2023-05-12 18:35:44.052234 thermite-0.1.0/mkdocs.yml
--rw-r--r--   0        0        0     1073 2023-05-11 06:02:48.928771 thermite-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      398 2023-04-10 14:31:39.097142 thermite-0.1.0/tests/__init__.py
--rw-r--r--   0        0        0      154 2023-05-07 12:30:51.915611 thermite-0.1.0/tests/conftest.py
--rw-r--r--   0        0        0     3099 2023-04-10 14:31:39.097142 thermite-0.1.0/tests/examples/__init__.py
--rw-r--r--   0        0        0      611 2023-05-02 19:02:57.368574 thermite-0.1.0/tests/examples/nested.py
--rw-r--r--   0        0        0      518 2023-05-04 20:25:09.408460 thermite-0.1.0/tests/examples/simple.py
--rw-r--r--   0        0        0      128 2023-05-04 21:14:52.684365 thermite-0.1.0/tests/examples/simple_defaults.yml
--rw-r--r--   0        0        0      713 2023-05-04 21:50:41.025438 thermite-0.1.0/tests/examples/subcommands.py
--rw-r--r--   0        0        0      150 2023-05-04 21:36:15.783211 thermite-0.1.0/tests/examples/subcommands_defaults.yml
--rw-r--r--   0        0        0      971 2023-05-09 19:54:00.605930 thermite-0.1.0/tests/plugins/test_default_defs.py
--rw-r--r--   0        0        0      235 2023-05-02 19:02:57.368574 thermite-0.1.0/tests/plugins/test_help.py
--rw-r--r--   0        0        0     3586 2023-05-04 05:08:57.205250 thermite-0.1.0/tests/test_command.py
--rw-r--r--   0        0        0     3311 2023-05-09 19:54:00.605930 thermite-0.1.0/tests/test_default_defs.py
--rw-r--r--   0        0        0    11212 2023-05-09 19:54:00.605930 thermite-0.1.0/tests/test_parameters.py
--rw-r--r--   0        0        0      250 2023-04-10 14:31:39.101142 thermite-0.1.0/tests/test_preprocessing.py
--rw-r--r--   0        0        0     1928 2023-04-30 10:24:03.003364 thermite-0.1.0/tests/test_type_converters.py
--rw-r--r--   0        0        0      528 2023-05-02 19:02:57.368574 thermite-0.1.0/tests/test_utils.py
--rw-r--r--   0        0        0     1011 2023-05-11 03:55:14.868858 thermite-0.1.0/thermite/__init__.py
--rw-r--r--   0        0        0      546 2023-05-07 14:23:49.597794 thermite-0.1.0/thermite/callbacks.py
--rw-r--r--   0        0        0     1221 2023-05-09 19:47:15.920754 thermite-0.1.0/thermite/cli_args_splitter.py
--rw-r--r--   0        0        0     8997 2023-05-09 19:54:00.605930 thermite-0.1.0/thermite/command.py
--rw-r--r--   0        0        0     2929 2023-05-09 20:02:40.956589 thermite-0.1.0/thermite/config.py
--rw-r--r--   0        0        0     2602 2023-04-10 17:18:39.948715 thermite-0.1.0/thermite/exceptions.py
--rw-r--r--   0        0        0      792 2023-05-08 21:09:45.226730 thermite-0.1.0/thermite/parameters/__init__.py
--rw-r--r--   0        0        0     4884 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/parameters/base.py
--rw-r--r--   0        0        0     8756 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/parameters/create.py
--rw-r--r--   0        0        0     9289 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/parameters/group.py
--rw-r--r--   0        0        0     3542 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/parameters/processors.py
--rw-r--r--   0        0        0     8153 2023-05-07 14:28:24.881055 thermite-0.1.0/thermite/plugins/default_defs.py
--rw-r--r--   0        0        0     9508 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/plugins/help.py
--rw-r--r--   0        0        0     1354 2023-04-10 14:31:39.101142 thermite-0.1.0/thermite/preprocessing.py
--rw-r--r--   0        0        0     3120 2023-04-26 18:37:03.026404 thermite-0.1.0/thermite/preset_config.py
--rw-r--r--   0        0        0       54 2023-04-10 14:31:39.101142 thermite-0.1.0/thermite/rich.py
--rw-r--r--   0        0        0     4840 2023-05-09 20:03:22.097025 thermite-0.1.0/thermite/run.py
--rw-r--r--   0        0        0     4839 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/signatures.py
--rw-r--r--   0        0        0    13351 2023-05-09 19:54:00.609930 thermite-0.1.0/thermite/type_converters.py
--rw-r--r--   0        0        0     1197 2023-05-02 19:02:57.372576 thermite-0.1.0/thermite/utils.py
--rw-r--r--   0        0        0      937 1970-01-01 00:00:00.000000 thermite-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0       33 2023-05-13 13:05:32.639618 thermite-0.1.1/.gitignore
+-rw-r--r--   0        0        0     1082 2023-04-10 14:31:39.097142 thermite-0.1.1/LICENSE
+-rw-r--r--   0        0        0     2528 2023-05-11 04:53:09.442923 thermite-0.1.1/Makefile
+-rw-r--r--   0        0        0     1469 2023-05-12 05:20:20.459670 thermite-0.1.1/README.md
+-rw-r--r--   0        0        0      150 2023-04-10 14:31:39.097142 thermite-0.1.1/conda_env.yaml
+-rw-r--r--   0        0        0     2720 2023-05-12 05:11:41.844680 thermite-0.1.1/docs/classes_events.md
+-rw-r--r--   0        0        0      938 2023-05-12 05:16:16.617480 thermite-0.1.1/docs/cli_callbacks.md
+-rw-r--r--   0        0        0      895 2023-05-12 04:18:22.635421 thermite-0.1.1/docs/css/mkdocstrings.css
+-rw-r--r--   0        0        0     1287 2023-05-12 18:40:39.670464 thermite-0.1.1/docs/examples/advanced.md
+-rw-r--r--   0        0        0      670 2023-05-12 18:50:10.971243 thermite-0.1.1/docs/examples/basic.md
+-rw-r--r--   0        0        0      827 2023-05-12 18:48:45.450048 thermite-0.1.1/docs/examples/dataclasses.md
+-rw-r--r--   0        0        0     2200 2023-05-12 18:49:45.658896 thermite-0.1.1/docs/examples/lists.md
+-rw-r--r--   0        0        0     2774 2023-05-13 07:00:30.810653 thermite-0.1.1/docs/index.md
+-rw-r--r--   0        0        0       44 2023-05-12 03:49:33.471411 thermite-0.1.1/docs/references.md
+-rw-r--r--   0        0        0      485 2023-05-11 04:48:46.773541 thermite-0.1.1/examples/adv/config_file.py
+-rw-r--r--   0        0        0      194 2023-05-11 04:51:06.318280 thermite-0.1.1/examples/adv/config_file.yml
+-rw-r--r--   0        0        0     1933 2023-05-12 18:42:20.727526 thermite-0.1.1/examples/adv/config_file_help.out
+-rw-r--r--   0        0        0      865 2023-05-11 04:09:31.484073 thermite-0.1.1/examples/adv/param_transfer.py
+-rw-r--r--   0        0        0     1348 2023-05-12 18:42:20.455521 thermite-0.1.1/examples/adv/param_transfer_help.out
+-rw-r--r--   0        0        0      138 2023-05-12 18:42:20.579523 thermite-0.1.1/examples/adv/param_transfer_output.out
+-rw-r--r--   0        0        0     2404 2023-05-13 07:10:26.493921 thermite-0.1.1/examples/adv/simclr.py
+-rw-r--r--   0        0        0     1344 2023-05-12 18:42:18.771487 thermite-0.1.1/examples/basics/adjust_help.out
+-rw-r--r--   0        0        0      713 2023-05-07 20:48:38.579351 thermite-0.1.1/examples/basics/adjust_help.py
+-rw-r--r--   0        0        0     1811 2023-05-12 18:42:18.899489 thermite-0.1.1/examples/basics/opts_to_args.out
+-rw-r--r--   0        0        0      787 2023-05-07 20:48:22.407157 thermite-0.1.1/examples/basics/opts_to_args.py
+-rw-r--r--   0        0        0     1816 2023-05-12 18:42:19.031492 thermite-0.1.1/examples/dataclasses/basic.out
+-rw-r--r--   0        0        0      269 2023-05-07 18:16:17.299206 thermite-0.1.1/examples/dataclasses/basic.py
+-rw-r--r--   0        0        0     1198 2023-05-12 18:42:19.287497 thermite-0.1.1/examples/dataclasses/custom_converter.out
+-rw-r--r--   0        0        0      643 2023-05-07 20:23:22.406254 thermite-0.1.1/examples/dataclasses/custom_converter.py
+-rw-r--r--   0        0        0     1265 2023-05-12 18:42:19.155494 thermite-0.1.1/examples/dataclasses/with_arguments.out
+-rw-r--r--   0        0        0      602 2023-05-07 18:59:28.785876 thermite-0.1.1/examples/dataclasses/with_arguments.py
+-rw-r--r--   0        0        0      238 2023-05-08 20:07:43.401327 thermite-0.1.1/examples/lists/default.py
+-rw-r--r--   0        0        0     1168 2023-05-12 18:42:19.423500 thermite-0.1.1/examples/lists/default_help.out
+-rw-r--r--   0        0        0       57 2023-05-12 18:42:19.571503 thermite-0.1.1/examples/lists/default_output.out
+-rw-r--r--   0        0        0      661 2023-05-10 04:26:34.637079 thermite-0.1.1/examples/lists/empty_list.py
+-rw-r--r--   0        0        0     1344 2023-05-12 18:42:20.323518 thermite-0.1.1/examples/lists/empty_list_help.out
+-rw-r--r--   0        0        0       76 2023-05-12 18:42:20.199515 thermite-0.1.1/examples/lists/empty_list_output.out
+-rw-r--r--   0        0        0      653 2023-05-09 03:49:23.733171 thermite-0.1.1/examples/lists/multiple_args.py
+-rw-r--r--   0        0        0     1341 2023-05-12 18:42:20.075513 thermite-0.1.1/examples/lists/multiple_args_help.out
+-rw-r--r--   0        0        0       78 2023-05-12 18:42:19.943510 thermite-0.1.1/examples/lists/multiple_args_output.out
+-rw-r--r--   0        0        0      536 2023-05-08 20:48:32.673845 thermite-0.1.1/examples/lists/var_length_list_opt.py
+-rw-r--r--   0        0        0     1192 2023-05-12 18:42:19.819508 thermite-0.1.1/examples/lists/var_length_list_opt_help.out
+-rw-r--r--   0        0        0       70 2023-05-12 18:42:19.695505 thermite-0.1.1/examples/lists/var_length_list_opt_output.out
+-rw-r--r--   0        0        0      611 2023-05-07 16:09:47.181972 thermite-0.1.1/examples/nested.py
+-rw-r--r--   0        0        0      357 2023-05-07 20:46:01.217468 thermite-0.1.1/examples/simple.py
+-rw-r--r--   0        0        0      128 2023-05-07 16:09:18.165639 thermite-0.1.1/examples/simple_defaults.yml
+-rw-r--r--   0        0        0     1271 2023-05-12 18:35:44.052234 thermite-0.1.1/mkdocs.yml
+-rw-r--r--   0        0        0     1094 2023-05-13 13:04:36.063147 thermite-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0      398 2023-04-10 14:31:39.097142 thermite-0.1.1/tests/__init__.py
+-rw-r--r--   0        0        0      154 2023-05-07 12:30:51.915611 thermite-0.1.1/tests/conftest.py
+-rw-r--r--   0        0        0     3099 2023-04-10 14:31:39.097142 thermite-0.1.1/tests/examples/__init__.py
+-rw-r--r--   0        0        0      611 2023-05-02 19:02:57.368574 thermite-0.1.1/tests/examples/nested.py
+-rw-r--r--   0        0        0      518 2023-05-04 20:25:09.408460 thermite-0.1.1/tests/examples/simple.py
+-rw-r--r--   0        0        0      128 2023-05-04 21:14:52.684365 thermite-0.1.1/tests/examples/simple_defaults.yml
+-rw-r--r--   0        0        0      713 2023-05-04 21:50:41.025438 thermite-0.1.1/tests/examples/subcommands.py
+-rw-r--r--   0        0        0      150 2023-05-04 21:36:15.783211 thermite-0.1.1/tests/examples/subcommands_defaults.yml
+-rw-r--r--   0        0        0      971 2023-05-09 19:54:00.605930 thermite-0.1.1/tests/plugins/test_default_defs.py
+-rw-r--r--   0        0        0      235 2023-05-02 19:02:57.368574 thermite-0.1.1/tests/plugins/test_help.py
+-rw-r--r--   0        0        0     3586 2023-05-04 05:08:57.205250 thermite-0.1.1/tests/test_command.py
+-rw-r--r--   0        0        0     3311 2023-05-09 19:54:00.605930 thermite-0.1.1/tests/test_default_defs.py
+-rw-r--r--   0        0        0    11212 2023-05-09 19:54:00.605930 thermite-0.1.1/tests/test_parameters.py
+-rw-r--r--   0        0        0      250 2023-04-10 14:31:39.101142 thermite-0.1.1/tests/test_preprocessing.py
+-rw-r--r--   0        0        0     1928 2023-04-30 10:24:03.003364 thermite-0.1.1/tests/test_type_converters.py
+-rw-r--r--   0        0        0      528 2023-05-02 19:02:57.368574 thermite-0.1.1/tests/test_utils.py
+-rw-r--r--   0        0        0     1011 2023-05-13 13:05:16.455483 thermite-0.1.1/thermite/__init__.py
+-rw-r--r--   0        0        0      546 2023-05-07 14:23:49.597794 thermite-0.1.1/thermite/callbacks.py
+-rw-r--r--   0        0        0     1221 2023-05-09 19:47:15.920754 thermite-0.1.1/thermite/cli_args_splitter.py
+-rw-r--r--   0        0        0     8997 2023-05-09 19:54:00.605930 thermite-0.1.1/thermite/command.py
+-rw-r--r--   0        0        0     2929 2023-05-09 20:02:40.956589 thermite-0.1.1/thermite/config.py
+-rw-r--r--   0        0        0     2602 2023-04-10 17:18:39.948715 thermite-0.1.1/thermite/exceptions.py
+-rw-r--r--   0        0        0      792 2023-05-08 21:09:45.226730 thermite-0.1.1/thermite/parameters/__init__.py
+-rw-r--r--   0        0        0     4884 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/parameters/base.py
+-rw-r--r--   0        0        0     8756 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/parameters/create.py
+-rw-r--r--   0        0        0     9289 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/parameters/group.py
+-rw-r--r--   0        0        0     3542 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/parameters/processors.py
+-rw-r--r--   0        0        0     8153 2023-05-07 14:28:24.881055 thermite-0.1.1/thermite/plugins/default_defs.py
+-rw-r--r--   0        0        0     9508 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/plugins/help.py
+-rw-r--r--   0        0        0     1354 2023-04-10 14:31:39.101142 thermite-0.1.1/thermite/preprocessing.py
+-rw-r--r--   0        0        0     3120 2023-04-26 18:37:03.026404 thermite-0.1.1/thermite/preset_config.py
+-rw-r--r--   0        0        0       54 2023-04-10 14:31:39.101142 thermite-0.1.1/thermite/rich.py
+-rw-r--r--   0        0        0     4840 2023-05-09 20:03:22.097025 thermite-0.1.1/thermite/run.py
+-rw-r--r--   0        0        0     4839 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/signatures.py
+-rw-r--r--   0        0        0    13351 2023-05-09 19:54:00.609930 thermite-0.1.1/thermite/type_converters.py
+-rw-r--r--   0        0        0     1197 2023-05-02 19:02:57.372576 thermite-0.1.1/thermite/utils.py
+-rw-r--r--   0        0        0     2448 1970-01-01 00:00:00.000000 thermite-0.1.1/PKG-INFO
```

### Comparing `thermite-0.1.0/LICENSE` & `thermite-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/Makefile` & `thermite-0.1.1/Makefile`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/README.md` & `thermite-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/classes_events.md` & `thermite-0.1.1/docs/classes_events.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/cli_callbacks.md` & `thermite-0.1.1/docs/cli_callbacks.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/css/mkdocstrings.css` & `thermite-0.1.1/docs/css/mkdocstrings.css`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/examples/advanced.md` & `thermite-0.1.1/docs/examples/advanced.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/examples/basic.md` & `thermite-0.1.1/docs/examples/basic.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/examples/dataclasses.md` & `thermite-0.1.1/docs/examples/dataclasses.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/examples/lists.md` & `thermite-0.1.1/docs/examples/lists.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/docs/index.md` & `thermite-0.1.1/docs/index.md`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/adv/config_file_help.out` & `thermite-0.1.1/examples/adv/config_file_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/adv/param_transfer.py` & `thermite-0.1.1/examples/adv/param_transfer.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/adv/param_transfer_help.out` & `thermite-0.1.1/examples/adv/param_transfer_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/adv/simclr.py` & `thermite-0.1.1/examples/adv/simclr.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/basics/adjust_help.out` & `thermite-0.1.1/examples/basics/adjust_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/basics/adjust_help.py` & `thermite-0.1.1/examples/basics/adjust_help.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/basics/opts_to_args.out` & `thermite-0.1.1/examples/basics/opts_to_args.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/basics/opts_to_args.py` & `thermite-0.1.1/examples/basics/opts_to_args.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/dataclasses/basic.out` & `thermite-0.1.1/examples/dataclasses/basic.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/dataclasses/custom_converter.out` & `thermite-0.1.1/examples/dataclasses/custom_converter.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/dataclasses/custom_converter.py` & `thermite-0.1.1/examples/dataclasses/custom_converter.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/dataclasses/with_arguments.out` & `thermite-0.1.1/examples/dataclasses/with_arguments.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/dataclasses/with_arguments.py` & `thermite-0.1.1/examples/dataclasses/with_arguments.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/default_help.out` & `thermite-0.1.1/examples/lists/default_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/empty_list.py` & `thermite-0.1.1/examples/lists/empty_list.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/empty_list_help.out` & `thermite-0.1.1/examples/lists/empty_list_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/multiple_args.py` & `thermite-0.1.1/examples/lists/multiple_args.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/multiple_args_help.out` & `thermite-0.1.1/examples/lists/multiple_args_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/var_length_list_opt.py` & `thermite-0.1.1/examples/lists/var_length_list_opt.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/lists/var_length_list_opt_help.out` & `thermite-0.1.1/examples/lists/var_length_list_opt_help.out`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/examples/nested.py` & `thermite-0.1.1/examples/nested.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/mkdocs.yml` & `thermite-0.1.1/mkdocs.yml`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/pyproject.toml` & `thermite-0.1.1/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 [build-system]
 requires = ["flit_core >=3.2,<4"]
 build-backend = "flit_core.buildapi"
 
 [project]
 name = "thermite"
 authors = [{name = "Holger Hoefling", email = "hhoeflin@gmail.com"}]
+readme = "README.md"
 license = {file = "LICENSE"}
 classifiers = ["License :: OSI Approved :: MIT License"]
 dynamic = ["version", "description"]
 requires-python = ">=3.10"
 dependencies = [
     "rich",
     "more_itertools",
```

### Comparing `thermite-0.1.0/tests/examples/__init__.py` & `thermite-0.1.1/tests/examples/__init__.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/examples/nested.py` & `thermite-0.1.1/tests/examples/nested.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/examples/simple.py` & `thermite-0.1.1/tests/examples/simple.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/examples/subcommands.py` & `thermite-0.1.1/tests/examples/subcommands.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/plugins/test_default_defs.py` & `thermite-0.1.1/tests/plugins/test_default_defs.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/test_command.py` & `thermite-0.1.1/tests/test_command.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/test_default_defs.py` & `thermite-0.1.1/tests/test_default_defs.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/test_parameters.py` & `thermite-0.1.1/tests/test_parameters.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/test_type_converters.py` & `thermite-0.1.1/tests/test_type_converters.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/tests/test_utils.py` & `thermite-0.1.1/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/__init__.py` & `thermite-0.1.1/thermite/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 """A package for easily creating CLIs."""
-__version__ = "0.1.0"
+__version__ = "0.1.1"
 
 from .command import CliCallback
 from .config import Config, Event
 from .parameters import (
     ConstantTriggerProcessor,
     ConvertTriggerProcessor,
     MultiConvertTriggerProcessor,
```

### Comparing `thermite-0.1.0/thermite/callbacks.py` & `thermite-0.1.1/thermite/callbacks.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/cli_args_splitter.py` & `thermite-0.1.1/thermite/cli_args_splitter.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/command.py` & `thermite-0.1.1/thermite/command.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/config.py` & `thermite-0.1.1/thermite/config.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/exceptions.py` & `thermite-0.1.1/thermite/exceptions.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/parameters/__init__.py` & `thermite-0.1.1/thermite/parameters/__init__.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/parameters/base.py` & `thermite-0.1.1/thermite/parameters/base.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/parameters/create.py` & `thermite-0.1.1/thermite/parameters/create.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/parameters/group.py` & `thermite-0.1.1/thermite/parameters/group.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/parameters/processors.py` & `thermite-0.1.1/thermite/parameters/processors.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/plugins/default_defs.py` & `thermite-0.1.1/thermite/plugins/default_defs.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/plugins/help.py` & `thermite-0.1.1/thermite/plugins/help.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/preprocessing.py` & `thermite-0.1.1/thermite/preprocessing.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/preset_config.py` & `thermite-0.1.1/thermite/preset_config.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/run.py` & `thermite-0.1.1/thermite/run.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/signatures.py` & `thermite-0.1.1/thermite/signatures.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/type_converters.py` & `thermite-0.1.1/thermite/type_converters.py`

 * *Files identical despite different names*

### Comparing `thermite-0.1.0/thermite/utils.py` & `thermite-0.1.1/thermite/utils.py`

 * *Files identical despite different names*

