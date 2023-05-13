# Comparing `tmp/infer-subc-0.0.4b0.tar.gz` & `tmp/infer-subc-0.0.post1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "infer-subc-0.0.4b0.tar", last modified: Sat May 13 07:30:29 2023, max compression
+gzip compressed data, was "infer-subc-0.0.post1.tar", last modified: Sat May 13 00:28:51 2023, max compression
```

## Comparing `infer-subc-0.0.4b0.tar` & `infer-subc-0.0.post1.tar`

### file list

```diff
@@ -1,185 +1,185 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.137157 infer-subc-0.0.4b0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.117157 infer-subc-0.0.4b0/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/.github/workflows/ci.yml.disable
--rw-r--r--   0 runner    (1001) docker     (123)     1618 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/.github/workflows/publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1919 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)    11501 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/20230221_MSI_3Dmeasurements.csv
--rw-r--r--   0 runner    (1001) docker     (123)    10428 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/202303063_MCZ-SR_3Dmeasurement-prioritylist.xlsx
--rw-r--r--   0 runner    (1001) docker     (123)     9102 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/ABOUT_THIS_TEMPLATE.md
--rw-r--r--   0 runner    (1001) docker     (123)     3636 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)       97 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/Containerfile
--rw-r--r--   0 runner    (1001) docker     (123)      229 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/HISTORY.md
--rw-r--r--   0 runner    (1001) docker     (123)     1485 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     7747 2023-05-13 07:30:29.137157 infer-subc-0.0.4b0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6497 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/
--rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/config.md
--rw-r--r--   0 runner    (1001) docker     (123)     5569 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/framework.md
--rw-r--r--   0 runner    (1001) docker     (123)     4540 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/index.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/infer_subc/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/infer_subc/core/
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/core/file_io.md
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/core/img.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/infer_subc/napari/
--rw-r--r--   0 runner    (1001) docker     (123)      225 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/napari/organelle_config.md
--rw-r--r--   0 runner    (1001) docker     (123)      236 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/napari/plugin.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/infer_subc/organelles/
--rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/cellmask.md
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/cytoplasm.md
--rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/er.md
--rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/golgi.md
--rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/lipid.md
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/lysosome.md
--rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/mitochondria.md
--rw-r--r--   0 runner    (1001) docker     (123)       65 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/nuclei.md
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles/peroxisome.md
--rw-r--r--   0 runner    (1001) docker     (123)      819 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/organelles.md
--rw-r--r--   0 runner    (1001) docker     (123)     1997 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/overview.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/infer_subc/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/utils/batch.md
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/utils/etc.md
--rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/utils/stats.md
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/utils/utils.md
--rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/infer_subc/workflow.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/docs/nbs/
--rw-r--r--   0 runner    (1001) docker     (123)     2632 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/nbs/overview.md
--rw-r--r--   0 runner    (1001) docker     (123)      730 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/docs/pipeline.md
--rw-r--r--   0 runner    (1001) docker     (123)      302 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/env_create.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.121157 infer-subc-0.0.4b0/infer_subc/
--rw-r--r--   0 runner    (1001) docker     (123)      793 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      162 2023-05-13 07:30:28.000000 infer-subc-0.0.4b0/infer_subc/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      749 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      397 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/constants.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.121157 infer-subc-0.0.4b0/infer_subc/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15488 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/core/file_io.py
--rw-r--r--   0 runner    (1001) docker     (123)    40110 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/core/img.py
--rw-r--r--   0 runner    (1001) docker     (123)     3062 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/core/zslice.py
--rw-r--r--   0 runner    (1001) docker     (123)      261 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/exceptions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.121157 infer-subc-0.0.4b0/infer_subc/organelles/
--rw-r--r--   0 runner    (1001) docker     (123)     1148 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8924 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/cellmask.py
--rw-r--r--   0 runner    (1001) docker     (123)     2847 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/cytoplasm.py
--rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/er.py
--rw-r--r--   0 runner    (1001) docker     (123)     5668 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/golgi.py
--rw-r--r--   0 runner    (1001) docker     (123)     4512 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/lipid.py
--rw-r--r--   0 runner    (1001) docker     (123)     5963 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/lysosome.py
--rw-r--r--   0 runner    (1001) docker     (123)     4084 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/mitochondria.py
--rw-r--r--   0 runner    (1001) docker     (123)     5553 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/nuclei.py
--rw-r--r--   0 runner    (1001) docker     (123)     4522 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/peroxisome.py
--rw-r--r--   0 runner    (1001) docker     (123)     1671 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles/qc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.129157 infer-subc-0.0.4b0/infer_subc/organelles_config/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    54029 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/all_functions.json
--rw-r--r--   0 runner    (1001) docker     (123)     2864 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.1.masks.json
--rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.1.masks_MCZ.json
--rw-r--r--   0 runner    (1001) docker     (123)     1863 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.2.lyso.json
--rw-r--r--   0 runner    (1001) docker     (123)     1266 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.3.mito.json
--rw-r--r--   0 runner    (1001) docker     (123)     2162 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.4.golgi.json
--rw-r--r--   0 runner    (1001) docker     (123)     1401 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.5.perox.json
--rw-r--r--   0 runner    (1001) docker     (123)     1280 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.6.ER.json
--rw-r--r--   0 runner    (1001) docker     (123)     1323 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.7.LD.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.129157 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/
--rw-r--r--   0 runner    (1001) docker     (123)     3389 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.1.soma_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     1867 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.2.nuclei_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)      627 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.3.cytosol_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     2374 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.4.lysosome_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.5.mitochondria_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     2487 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.6.golgi_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.7.peroxisome_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     1604 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.8.er_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     2175 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.9.lipid_stepbystep_from_raw.json
--rw-r--r--   0 runner    (1001) docker     (123)     3268 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_2.1.soma_stepbystep.json
--rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_2.2.nuclei_stepbystep.json
--rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch.json
--rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch2.json
--rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/infer_nuclei.json
--rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/infer_soma.json
--rw-r--r--   0 runner    (1001) docker     (123)    18307 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/og_all_functions.json
--rw-r--r--   0 runner    (1001) docker     (123)    18238 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/test_functions.json
--rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/function_guide.md
--rw-r--r--   0 runner    (1001) docker     (123)    17259 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/function_params.md
--rw-r--r--   0 runner    (1001) docker     (123)     1440 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/organelles_config/helper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.121157 infer-subc-0.0.4b0/infer_subc/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12599 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/_aicsimage_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     8166 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/batch.py
--rw-r--r--   0 runner    (1001) docker     (123)      589 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/directories.py
--rw-r--r--   0 runner    (1001) docker     (123)      345 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/filesystem.py
--rw-r--r--   0 runner    (1001) docker     (123)      374 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/lazy.py
--rw-r--r--   0 runner    (1001) docker     (123)    32061 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/stats.py
--rw-r--r--   0 runner    (1001) docker     (123)    24516 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/utils/stats_helpers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/infer_subc/workflow/
--rw-r--r--   0 runner    (1001) docker     (123)      312 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10350 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/batch_workflow.py
--rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/segmenter_function.py
--rw-r--r--   0 runner    (1001) docker     (123)     6394 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/workflow.py
--rw-r--r--   0 runner    (1001) docker     (123)     7950 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/workflow_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3505 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/workflow_definition.py
--rw-r--r--   0 runner    (1001) docker     (123)     8127 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/workflow_engine.py
--rw-r--r--   0 runner    (1001) docker     (123)     3519 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/infer_subc/workflow/workflow_step.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/infer_subc.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     7747 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     7449 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 07:30:29.000000 infer-subc-0.0.4b0/infer_subc.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/mkdocs.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.133157 infer-subc-0.0.4b0/notebooks/
--rw-r--r--   0 runner    (1001) docker     (123)     7692 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/00.0_framework_overview.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)     6770 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/00.1_pipeline_setup.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    52896 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/01_infer_nuclei-from-ERsignal_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    25936 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/01_infer_nuclei.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   113828 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/02_infer_cellmask.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)     8490 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/02a_cell_membrane.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    67191 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/02b_infer_neurites_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    47751 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/03_infer_cytoplasm.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    21870 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/04_infer_lysosome.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    56551 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/05_infer_mitochondria.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    42408 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/06_infer_golgi.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    40788 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/07_infer_peroxisome.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    51759 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/08_infer_ER.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    39618 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/09_infer_lipid_droplet.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    36588 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/10_regionprops.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    14696 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/11_batch_process.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    81922 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/12_fn_prototypes_json.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    89132 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/13_workflow_defs_json.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   213649 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/14_final_workflow.ipynb
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.137157 infer-subc-0.0.4b0/notebooks/todelete/
--rw-r--r--   0 runner    (1001) docker     (123)    16278 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/00.1_pipeline_setup_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    23658 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/00.2_extract_optimal_Z.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    53320 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/01_infer_nuclei_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    67064 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/02_infer_soma_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    66972 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/02a_infer_soma_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    67033 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/02b_infer_neurites_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    67027 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/02c_infer_wholecell_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    86025 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/03_infer_cytosol_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   121185 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/04_infer_lysosome_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   154818 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/05_infer_mitochondria_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    96854 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/06_infer_golgi_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    92224 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/07_infer_peroxisome_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   126036 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/08_infer_endoplasmic_reticulum_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   127295 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/09_infer_lipid_body_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   415241 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/10_batch_process_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   345416 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/10_batch_process_3Dv2.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    70614 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/999_fn_prototypes_json.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    19252 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/A_spectral_test.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)     9249 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/_centrosome_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     7543 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/_graveyard.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)    73532 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/new02a_infer_soma_3D.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)   478607 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/notebooks/todelete/test_soma_seg.ipynb
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-05-13 07:30:29.137157 infer-subc-0.0.4b0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/setup.py
--rw-r--r--   0 runner    (1001) docker     (123)      758 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/test.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:29.125157 infer-subc-0.0.4b0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/tests/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)      832 2023-05-13 07:30:20.000000 infer-subc-0.0.4b0/windows_notes.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.063383 infer-subc-0.0.post1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.027383 infer-subc-0.0.post1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.035383 infer-subc-0.0.post1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/.github/workflows/ci.yml.disable
+-rw-r--r--   0 runner    (1001) docker     (123)     1591 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/.github/workflows/publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1877 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)    11501 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/20230221_MSI_3Dmeasurements.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    10428 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/202303063_MCZ-SR_3Dmeasurement-prioritylist.xlsx
+-rw-r--r--   0 runner    (1001) docker     (123)     9102 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/ABOUT_THIS_TEMPLATE.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3636 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/Containerfile
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/HISTORY.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     6177 2023-05-13 00:28:51.063383 infer-subc-0.0.post1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4924 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/config.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5569 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/framework.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4540 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/index.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/infer_subc/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/infer_subc/core/
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/core/file_io.md
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/core/img.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/infer_subc/napari/
+-rw-r--r--   0 runner    (1001) docker     (123)      225 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/napari/organelle_config.md
+-rw-r--r--   0 runner    (1001) docker     (123)      236 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/napari/plugin.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/infer_subc/organelles/
+-rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/cellmask.md
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/cytoplasm.md
+-rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/er.md
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/golgi.md
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/lipid.md
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/lysosome.md
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/mitochondria.md
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/nuclei.md
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles/peroxisome.md
+-rw-r--r--   0 runner    (1001) docker     (123)      819 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/organelles.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1997 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/overview.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/infer_subc/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/utils/batch.md
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/utils/etc.md
+-rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/utils/stats.md
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/utils/utils.md
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/infer_subc/workflow.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.039383 infer-subc-0.0.post1/docs/nbs/
+-rw-r--r--   0 runner    (1001) docker     (123)     2632 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/nbs/overview.md
+-rw-r--r--   0 runner    (1001) docker     (123)      730 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/docs/pipeline.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4203 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/env_create.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.031383 infer-subc-0.0.post1/infer_subc/
+-rw-r--r--   0 runner    (1001) docker     (123)      793 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      161 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      749 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      397 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/constants.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.031383 infer-subc-0.0.post1/infer_subc/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15488 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/core/file_io.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40110 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/core/img.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3062 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/core/zslice.py
+-rw-r--r--   0 runner    (1001) docker     (123)      261 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.031383 infer-subc-0.0.post1/infer_subc/organelles/
+-rw-r--r--   0 runner    (1001) docker     (123)     1148 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8924 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/cellmask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2847 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/cytoplasm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/er.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5668 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/golgi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4512 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/lipid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5963 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/lysosome.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4084 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/mitochondria.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5553 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/nuclei.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4522 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/peroxisome.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1671 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles/qc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.043383 infer-subc-0.0.post1/infer_subc/organelles_config/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    54029 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/all_functions.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2864 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.1.masks.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.1.masks_MCZ.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1863 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.2.lyso.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1266 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.3.mito.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2162 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.4.golgi.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1401 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.5.perox.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1280 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.6.ER.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1323 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.7.LD.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.047383 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/
+-rw-r--r--   0 runner    (1001) docker     (123)     3389 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.1.soma_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1867 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.2.nuclei_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)      627 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.3.cytosol_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2374 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.4.lysosome_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.5.mitochondria_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2487 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.6.golgi_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.7.peroxisome_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1604 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.8.er_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2175 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.9.lipid_stepbystep_from_raw.json
+-rw-r--r--   0 runner    (1001) docker     (123)     3268 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_2.1.soma_stepbystep.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_2.2.nuclei_stepbystep.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch2.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/infer_nuclei.json
+-rw-r--r--   0 runner    (1001) docker     (123)     3089 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/infer_soma.json
+-rw-r--r--   0 runner    (1001) docker     (123)    18307 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/og_all_functions.json
+-rw-r--r--   0 runner    (1001) docker     (123)    18238 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/depricate/test_functions.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/function_guide.md
+-rw-r--r--   0 runner    (1001) docker     (123)    17259 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/function_params.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1440 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/organelles_config/helper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.035383 infer-subc-0.0.post1/infer_subc/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12599 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/_aicsimage_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8166 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/batch.py
+-rw-r--r--   0 runner    (1001) docker     (123)      589 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/directories.py
+-rw-r--r--   0 runner    (1001) docker     (123)      345 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/filesystem.py
+-rw-r--r--   0 runner    (1001) docker     (123)      374 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/lazy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32061 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24516 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/utils/stats_helpers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.035383 infer-subc-0.0.post1/infer_subc/workflow/
+-rw-r--r--   0 runner    (1001) docker     (123)      312 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10350 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/batch_workflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/segmenter_function.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6394 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/workflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7950 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/workflow_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3505 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/workflow_definition.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8127 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/workflow_engine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3519 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/infer_subc/workflow/workflow_step.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.043383 infer-subc-0.0.post1/infer_subc.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6177 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7449 2023-05-13 00:28:51.000000 infer-subc-0.0.post1/infer_subc.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:28:50.000000 infer-subc-0.0.post1/infer_subc.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/mkdocs.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.055383 infer-subc-0.0.post1/notebooks/
+-rw-r--r--   0 runner    (1001) docker     (123)     7692 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/00.0_framework_overview.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)     6770 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/00.1_pipeline_setup.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    52896 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/01_infer_nuclei-from-ERsignal_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    25936 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/01_infer_nuclei.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   113828 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/02_infer_cellmask.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)     8490 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/02a_cell_membrane.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    67191 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/02b_infer_neurites_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    47751 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/03_infer_cytoplasm.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    21870 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/04_infer_lysosome.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    56551 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/05_infer_mitochondria.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    42408 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/06_infer_golgi.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    40788 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/07_infer_peroxisome.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    51759 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/08_infer_ER.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    39618 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/09_infer_lipid_droplet.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    36588 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/10_regionprops.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    14696 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/11_batch_process.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    81922 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/12_fn_prototypes_json.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    89132 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/13_workflow_defs_json.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   213649 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/14_final_workflow.ipynb
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.059383 infer-subc-0.0.post1/notebooks/todelete/
+-rw-r--r--   0 runner    (1001) docker     (123)    16278 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/00.1_pipeline_setup_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    23658 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/00.2_extract_optimal_Z.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    53320 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/01_infer_nuclei_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    67064 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/02_infer_soma_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    66972 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/02a_infer_soma_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    67033 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/02b_infer_neurites_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    67027 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/02c_infer_wholecell_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    86025 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/03_infer_cytosol_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   121185 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/04_infer_lysosome_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   154818 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/05_infer_mitochondria_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    96854 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/06_infer_golgi_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    92224 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/07_infer_peroxisome_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   126036 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/08_infer_endoplasmic_reticulum_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   127295 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/09_infer_lipid_body_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   415241 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/10_batch_process_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   345416 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/10_batch_process_3Dv2.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    70614 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/999_fn_prototypes_json.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    19252 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/A_spectral_test.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)     9249 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/_centrosome_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7543 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/_graveyard.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)    73532 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/new02a_infer_soma_3D.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)   478607 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/notebooks/todelete/test_soma_seg.ipynb
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      289 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1644 2023-05-13 00:28:51.063383 infer-subc-0.0.post1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       97 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/setup.py
+-rw-r--r--   0 runner    (1001) docker     (123)      758 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/test.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:51.035383 infer-subc-0.0.post1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/tests/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      832 2023-05-13 00:28:32.000000 infer-subc-0.0.post1/windows_notes.md
```

### Comparing `infer-subc-0.0.4b0/.github/workflows/ci.yml.disable` & `infer-subc-0.0.post1/.github/workflows/ci.yml.disable`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/.github/workflows/publish.yml` & `infer-subc-0.0.post1/.github/workflows/publish.yml`

 * *Files 16% similar despite different names*

```diff
@@ -1,14 +1,12 @@
 name: Publish
 on:
   push:
-    tags:
-      - "v*"
-    # branches:
-    #   - main
+    branches:
+      - main
 jobs:
   pypi:
     name: Upload release to PyPI
     runs-on: ubuntu-latest
     # environment:
     #   name: pypi
     #   url: https://pypi.org/p/<your-pypi-project-name>
```

### Comparing `infer-subc-0.0.4b0/.gitignore` & `infer-subc-0.0.post1/.gitignore`

 * *Files 3% similar despite different names*

```diff
@@ -134,10 +134,7 @@
 .github/templates/*
 
 #osx crud
 .DS_Store
 
 # mkdocs
 site
-
-# written by setuptools_scm
-*/_version.py
```

### Comparing `infer-subc-0.0.4b0/20230221_MSI_3Dmeasurements.csv` & `infer-subc-0.0.post1/20230221_MSI_3Dmeasurements.csv`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/202303063_MCZ-SR_3Dmeasurement-prioritylist.xlsx` & `infer-subc-0.0.post1/202303063_MCZ-SR_3Dmeasurement-prioritylist.xlsx`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/ABOUT_THIS_TEMPLATE.md` & `infer-subc-0.0.post1/ABOUT_THIS_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/CONTRIBUTING.md` & `infer-subc-0.0.post1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/Makefile` & `infer-subc-0.0.post1/Makefile`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/PKG-INFO` & `infer-subc-0.0.post1/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: infer-subc
-Version: 0.0.4b0
+Version: 0.0.post1
 Summary: A plugin that enables organelle segmentation
 Home-page: https://github.com/ndcn/infer-subc
 Author: Andy Henrie
 Author-email: ergonyc@gmail.com
 License: BSD-3
 Project-URL: Bug Tracker, https://github.com/ndcn/infer-subc/issues
 Project-URL: Documentation, https://github.com/ndcn/infer-subc#README.md
@@ -69,68 +69,87 @@
 - [`napari`](https://napari.org/stable/) -- Used as the visualization framework, a fast, interactive, multi-domensional image viewer for Python.
 - [`scipy`](https://scipy.org/install/) -- Image analysis
 - [`scikit-image`](https://scikit-image.org/) -- Image analysis
 - [`itk`](https://itkpythonpackage.readthedocs.io/en/master/Quick_start_guide.html) -- Image analysis
 - [`numpy`](https://numpy.org/) -- Under the hood computation
 - [`Alzheimer's Disease AD Workbench`](https://www.alzheimersdata.org/ad-workbench) -- We initially wanted to use the ADDI's ADWB as a method of data sharing and to serve as a computational resource.
 
+## ADWB hints
+
+Given that the github repos are not yet whitelisted, the source directory needs to be zipped and uploaded in order to make an "editable" pip install.
+
+[uploading guide ](https://knowledgebase.aridhia.io/article/guidance-for-uploading-files/)
+[uploading files via the workspace article](https://knowledgebase.aridhia.io/article/uploading-files-via-the-workspace/).
+[Using BLOB storage](https://knowledgebase.aridhia.io/article/using-blob-storage/)
 
 ## Getting Started
 
 ### Prerequisites
 
+The following are prerequisites and should be installed prior to using the workflow.
 
+- `napari` 
+  ```
+  pip install "napari[all]"
+  ```
+
+- `scipy`
+  ```
+  python -m pip install scipy
+  ```
+
+- `scikit-image`
+  ```
+  pip install scikit-image
+  ```
+
+- `itk`
+  ```
+  pip install itk
+  ```
+- `numpy`
+  ```
+  pip install numpy
+  ```
 
 ### Installation
-`infer_subc` is  available on `PyPI` via: 
 
+`infer_subc` is not yet available on `PyPI` so must be  be `pip` ionstalled from source
 ```
-pip install infer_subc
+pip install git+https://github.com/ndcn/infer-subc.git
 ```
 
-If there are issues more details can be fouund in the [documentation](https://ndcn.github.io/infer-subc/config/)
-
+## Usage
 
-## Usage - quick start
-Its recommended that you use this repo along with the [`organelle-segmenter-plugin`](https://github.com/ndcn/organelle-segmenter-plugin) as in [Option A](#option-a-napari-organelle-segmenter-plugin) below.  Alternatively using the module functions directly as in [Option B](#option-b-python-script-or-notebook) would work just fine.
+```py
+from infer_subc.organelles import infer_lyso
+from infer_subc.core.file_io import read_czi_image
 
+img_data,meta_dict = read_czi_image("path/to/image.czi")
+lyso_obj =  infer_lyso(img_data) 
 
-### Option A: Napari `organelle-segmenter-plugin`
-
-1. Open a file in napari by dragging multi-channel .czi file onto napari which will import a multi-channel, multi-Z 'layer'. (Using the menu's defaults to `aicsIMAGEIO` reader which automatically splits mutliple channels into individual layers.  The plugin is able to support multi-dimensional data in .tiff, .tif. ome.tif, .ome.tiff, .czi)
-2. Start the plugin (open napari, go to "Plugins" --> "organelle-segmenter-plugin" --> "workflow editor")
-3. Select the image and channel to work on
-4. Select a workflow based on the example image and target segmentation based on user's data. Ideally, it is recommend to start with the example with very similar morphology as user's data.
-5. Click "Run All" to execute the whole workflow on the sample data.
-6. Adjust the parameters of steps, based on the intermediate results.  A complete list of all functions can be found [here](https://github.com/ndcn/infer-subc/blob/main/infer_subc/organelles_config/function_params.md)🚧 WIP 🚧
-7. Click "Run All" again after adjusting the parameters and repeat step 6 and 7 until the result is satisfactory.
-8. Save the workflow
-9. Close the plugin and open the **batch processing** part by (go to "Plugins" --> "organelle-segmenter-plugin" --> "batch processing")
-10. Load the customized workflow saved above 
-11. Load the folder with all the images to process
-12. Click "Run"
-13. Follow the [examples](https://github.com/ndcn/infer-subc/blob/main/notebooks/14_final_workflow.ipynb) in the `infer_subc` [repo](https://github.com/ndcn/infer-subc/) for postprocessing of the saved segmentations and generating the statistics.  
+```
 
-### Option B: python script or notebook 
+ 🚧 WIP 🚧 (🚨🚨🚨🚨 )
+> NOTE: command line capabilities not implimented
+```bash
+$ python -m infer_subc
+#or
+$ infer_subc
+```
 
-A variety of example [notebooks](https://github.com/ndcn/infer-subc/blob/main/notebooks/) demonstrating how to use the are available in the repo.  Additional information can be found at https://ndcn.github.io/infer-subc/nbs/overview/.  
+## Roadmap
 
+ - [ ] Create `PyPI` package
+ - [ ] Update installation instructions to reflect optimal use of `conda` environments
 
 ## Development
 
 Read the [CONTRIBUTING.md](CONTRIBUTING.md) file.
 
 ## License
-Distributed under the terms of the [BSD-3] license,
-"organelle-segmenter-plugin" is free and open source software
+
+Distributed under the Unlicense license. See `LICENSE` for more information.  
 
 ## Issues
 
 If you encounter any problems, please file an issue with a detailed description.
-
-## ADWB hints
-
-Given that the github repos are not yet whitelisted, the source directory needs to be zipped and uploaded in order to make an "editable" pip install.
-
-[uploading guide ](https://knowledgebase.aridhia.io/article/guidance-for-uploading-files/)
-[uploading files via the workspace article](https://knowledgebase.aridhia.io/article/uploading-files-via-the-workspace/).
-[Using BLOB storage](https://knowledgebase.aridhia.io/article/using-blob-storage/)
```

### Comparing `infer-subc-0.0.4b0/docs/framework.md` & `infer-subc-0.0.post1/docs/framework.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/index.md` & `infer-subc-0.0.post1/docs/index.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/infer_subc/organelles.md` & `infer-subc-0.0.post1/docs/infer_subc/organelles.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/infer_subc/overview.md` & `infer-subc-0.0.post1/docs/infer_subc/overview.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/infer_subc/workflow.md` & `infer-subc-0.0.post1/docs/infer_subc/workflow.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/nbs/overview.md` & `infer-subc-0.0.post1/docs/nbs/overview.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/docs/pipeline.md` & `infer-subc-0.0.post1/docs/pipeline.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/__init__.py` & `infer-subc-0.0.post1/infer_subc/__init__.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/cli.py` & `infer-subc-0.0.post1/infer_subc/cli.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/core/file_io.py` & `infer-subc-0.0.post1/infer_subc/core/file_io.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/core/img.py` & `infer-subc-0.0.post1/infer_subc/core/img.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/core/zslice.py` & `infer-subc-0.0.post1/infer_subc/core/zslice.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/__init__.py` & `infer-subc-0.0.post1/infer_subc/organelles/__init__.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/cellmask.py` & `infer-subc-0.0.post1/infer_subc/organelles/cellmask.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/cytoplasm.py` & `infer-subc-0.0.post1/infer_subc/organelles/cytoplasm.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/er.py` & `infer-subc-0.0.post1/infer_subc/organelles/er.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/golgi.py` & `infer-subc-0.0.post1/infer_subc/organelles/golgi.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/lipid.py` & `infer-subc-0.0.post1/infer_subc/organelles/lipid.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/lysosome.py` & `infer-subc-0.0.post1/infer_subc/organelles/lysosome.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/mitochondria.py` & `infer-subc-0.0.post1/infer_subc/organelles/mitochondria.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/nuclei.py` & `infer-subc-0.0.post1/infer_subc/organelles/nuclei.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/peroxisome.py` & `infer-subc-0.0.post1/infer_subc/organelles/peroxisome.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles/qc.py` & `infer-subc-0.0.post1/infer_subc/organelles/qc.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/all_functions.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/all_functions.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.1.masks.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.1.masks.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.1.masks_MCZ.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.1.masks_MCZ.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.2.lyso.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.2.lyso.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.3.mito.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.3.mito.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.4.golgi.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.4.golgi.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.5.perox.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.5.perox.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.6.ER.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.6.ER.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/conf_0.7.LD.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/conf_0.7.LD.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.1.soma_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.1.soma_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.2.nuclei_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.2.nuclei_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.3.cytosol_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.3.cytosol_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.4.lysosome_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.4.lysosome_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.5.mitochondria_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.5.mitochondria_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.6.golgi_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.6.golgi_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.7.peroxisome_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.7.peroxisome_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.8.er_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.8.er_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_1.9.lipid_stepbystep_from_raw.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_1.9.lipid_stepbystep_from_raw.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_2.1.soma_stepbystep.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_2.1.soma_stepbystep.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_2.2.nuclei_stepbystep.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_2.2.nuclei_stepbystep.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch2.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/conf_infer_fixed_infer_organelles_batch2.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/infer_nuclei.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/infer_nuclei.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/infer_soma.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/infer_soma.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/og_all_functions.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/og_all_functions.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/depricate/test_functions.json` & `infer-subc-0.0.post1/infer_subc/organelles_config/depricate/test_functions.json`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/function_guide.md` & `infer-subc-0.0.post1/infer_subc/organelles_config/function_guide.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/function_params.md` & `infer-subc-0.0.post1/infer_subc/organelles_config/function_params.md`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/organelles_config/helper.py` & `infer-subc-0.0.post1/infer_subc/organelles_config/helper.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/utils/_aicsimage_reader.py` & `infer-subc-0.0.post1/infer_subc/utils/_aicsimage_reader.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/utils/batch.py` & `infer-subc-0.0.post1/infer_subc/utils/batch.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/utils/directories.py` & `infer-subc-0.0.post1/infer_subc/utils/directories.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/utils/stats.py` & `infer-subc-0.0.post1/infer_subc/utils/stats.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/utils/stats_helpers.py` & `infer-subc-0.0.post1/infer_subc/utils/stats_helpers.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/batch_workflow.py` & `infer-subc-0.0.post1/infer_subc/workflow/batch_workflow.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/segmenter_function.py` & `infer-subc-0.0.post1/infer_subc/workflow/segmenter_function.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/workflow.py` & `infer-subc-0.0.post1/infer_subc/workflow/workflow.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/workflow_config.py` & `infer-subc-0.0.post1/infer_subc/workflow/workflow_config.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/workflow_definition.py` & `infer-subc-0.0.post1/infer_subc/workflow/workflow_definition.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/workflow_engine.py` & `infer-subc-0.0.post1/infer_subc/workflow/workflow_engine.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc/workflow/workflow_step.py` & `infer-subc-0.0.post1/infer_subc/workflow/workflow_step.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/infer_subc.egg-info/PKG-INFO` & `infer-subc-0.0.post1/infer_subc.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: infer-subc
-Version: 0.0.4b0
+Version: 0.0.post1
 Summary: A plugin that enables organelle segmentation
 Home-page: https://github.com/ndcn/infer-subc
 Author: Andy Henrie
 Author-email: ergonyc@gmail.com
 License: BSD-3
 Project-URL: Bug Tracker, https://github.com/ndcn/infer-subc/issues
 Project-URL: Documentation, https://github.com/ndcn/infer-subc#README.md
@@ -69,68 +69,87 @@
 - [`napari`](https://napari.org/stable/) -- Used as the visualization framework, a fast, interactive, multi-domensional image viewer for Python.
 - [`scipy`](https://scipy.org/install/) -- Image analysis
 - [`scikit-image`](https://scikit-image.org/) -- Image analysis
 - [`itk`](https://itkpythonpackage.readthedocs.io/en/master/Quick_start_guide.html) -- Image analysis
 - [`numpy`](https://numpy.org/) -- Under the hood computation
 - [`Alzheimer's Disease AD Workbench`](https://www.alzheimersdata.org/ad-workbench) -- We initially wanted to use the ADDI's ADWB as a method of data sharing and to serve as a computational resource.
 
+## ADWB hints
+
+Given that the github repos are not yet whitelisted, the source directory needs to be zipped and uploaded in order to make an "editable" pip install.
+
+[uploading guide ](https://knowledgebase.aridhia.io/article/guidance-for-uploading-files/)
+[uploading files via the workspace article](https://knowledgebase.aridhia.io/article/uploading-files-via-the-workspace/).
+[Using BLOB storage](https://knowledgebase.aridhia.io/article/using-blob-storage/)
 
 ## Getting Started
 
 ### Prerequisites
 
+The following are prerequisites and should be installed prior to using the workflow.
 
+- `napari` 
+  ```
+  pip install "napari[all]"
+  ```
+
+- `scipy`
+  ```
+  python -m pip install scipy
+  ```
+
+- `scikit-image`
+  ```
+  pip install scikit-image
+  ```
+
+- `itk`
+  ```
+  pip install itk
+  ```
+- `numpy`
+  ```
+  pip install numpy
+  ```
 
 ### Installation
-`infer_subc` is  available on `PyPI` via: 
 
+`infer_subc` is not yet available on `PyPI` so must be  be `pip` ionstalled from source
 ```
-pip install infer_subc
+pip install git+https://github.com/ndcn/infer-subc.git
 ```
 
-If there are issues more details can be fouund in the [documentation](https://ndcn.github.io/infer-subc/config/)
-
+## Usage
 
-## Usage - quick start
-Its recommended that you use this repo along with the [`organelle-segmenter-plugin`](https://github.com/ndcn/organelle-segmenter-plugin) as in [Option A](#option-a-napari-organelle-segmenter-plugin) below.  Alternatively using the module functions directly as in [Option B](#option-b-python-script-or-notebook) would work just fine.
+```py
+from infer_subc.organelles import infer_lyso
+from infer_subc.core.file_io import read_czi_image
 
+img_data,meta_dict = read_czi_image("path/to/image.czi")
+lyso_obj =  infer_lyso(img_data) 
 
-### Option A: Napari `organelle-segmenter-plugin`
-
-1. Open a file in napari by dragging multi-channel .czi file onto napari which will import a multi-channel, multi-Z 'layer'. (Using the menu's defaults to `aicsIMAGEIO` reader which automatically splits mutliple channels into individual layers.  The plugin is able to support multi-dimensional data in .tiff, .tif. ome.tif, .ome.tiff, .czi)
-2. Start the plugin (open napari, go to "Plugins" --> "organelle-segmenter-plugin" --> "workflow editor")
-3. Select the image and channel to work on
-4. Select a workflow based on the example image and target segmentation based on user's data. Ideally, it is recommend to start with the example with very similar morphology as user's data.
-5. Click "Run All" to execute the whole workflow on the sample data.
-6. Adjust the parameters of steps, based on the intermediate results.  A complete list of all functions can be found [here](https://github.com/ndcn/infer-subc/blob/main/infer_subc/organelles_config/function_params.md)🚧 WIP 🚧
-7. Click "Run All" again after adjusting the parameters and repeat step 6 and 7 until the result is satisfactory.
-8. Save the workflow
-9. Close the plugin and open the **batch processing** part by (go to "Plugins" --> "organelle-segmenter-plugin" --> "batch processing")
-10. Load the customized workflow saved above 
-11. Load the folder with all the images to process
-12. Click "Run"
-13. Follow the [examples](https://github.com/ndcn/infer-subc/blob/main/notebooks/14_final_workflow.ipynb) in the `infer_subc` [repo](https://github.com/ndcn/infer-subc/) for postprocessing of the saved segmentations and generating the statistics.  
+```
 
-### Option B: python script or notebook 
+ 🚧 WIP 🚧 (🚨🚨🚨🚨 )
+> NOTE: command line capabilities not implimented
+```bash
+$ python -m infer_subc
+#or
+$ infer_subc
+```
 
-A variety of example [notebooks](https://github.com/ndcn/infer-subc/blob/main/notebooks/) demonstrating how to use the are available in the repo.  Additional information can be found at https://ndcn.github.io/infer-subc/nbs/overview/.  
+## Roadmap
 
+ - [ ] Create `PyPI` package
+ - [ ] Update installation instructions to reflect optimal use of `conda` environments
 
 ## Development
 
 Read the [CONTRIBUTING.md](CONTRIBUTING.md) file.
 
 ## License
-Distributed under the terms of the [BSD-3] license,
-"organelle-segmenter-plugin" is free and open source software
+
+Distributed under the Unlicense license. See `LICENSE` for more information.  
 
 ## Issues
 
 If you encounter any problems, please file an issue with a detailed description.
-
-## ADWB hints
-
-Given that the github repos are not yet whitelisted, the source directory needs to be zipped and uploaded in order to make an "editable" pip install.
-
-[uploading guide ](https://knowledgebase.aridhia.io/article/guidance-for-uploading-files/)
-[uploading files via the workspace article](https://knowledgebase.aridhia.io/article/uploading-files-via-the-workspace/).
-[Using BLOB storage](https://knowledgebase.aridhia.io/article/using-blob-storage/)
```

### Comparing `infer-subc-0.0.4b0/infer_subc.egg-info/SOURCES.txt` & `infer-subc-0.0.post1/infer_subc.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/mkdocs.yml` & `infer-subc-0.0.post1/mkdocs.yml`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/00.0_framework_overview.ipynb` & `infer-subc-0.0.post1/notebooks/00.0_framework_overview.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/00.1_pipeline_setup.ipynb` & `infer-subc-0.0.post1/notebooks/00.1_pipeline_setup.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/01_infer_nuclei-from-ERsignal_3D.ipynb` & `infer-subc-0.0.post1/notebooks/01_infer_nuclei-from-ERsignal_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/01_infer_nuclei.ipynb` & `infer-subc-0.0.post1/notebooks/01_infer_nuclei.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/02_infer_cellmask.ipynb` & `infer-subc-0.0.post1/notebooks/02_infer_cellmask.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/02a_cell_membrane.ipynb` & `infer-subc-0.0.post1/notebooks/02a_cell_membrane.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/02b_infer_neurites_3D.ipynb` & `infer-subc-0.0.post1/notebooks/02b_infer_neurites_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/03_infer_cytoplasm.ipynb` & `infer-subc-0.0.post1/notebooks/03_infer_cytoplasm.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/04_infer_lysosome.ipynb` & `infer-subc-0.0.post1/notebooks/04_infer_lysosome.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/05_infer_mitochondria.ipynb` & `infer-subc-0.0.post1/notebooks/05_infer_mitochondria.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/06_infer_golgi.ipynb` & `infer-subc-0.0.post1/notebooks/06_infer_golgi.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/07_infer_peroxisome.ipynb` & `infer-subc-0.0.post1/notebooks/07_infer_peroxisome.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/08_infer_ER.ipynb` & `infer-subc-0.0.post1/notebooks/08_infer_ER.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/09_infer_lipid_droplet.ipynb` & `infer-subc-0.0.post1/notebooks/09_infer_lipid_droplet.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/10_regionprops.ipynb` & `infer-subc-0.0.post1/notebooks/10_regionprops.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/11_batch_process.ipynb` & `infer-subc-0.0.post1/notebooks/11_batch_process.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/12_fn_prototypes_json.ipynb` & `infer-subc-0.0.post1/notebooks/12_fn_prototypes_json.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/13_workflow_defs_json.ipynb` & `infer-subc-0.0.post1/notebooks/13_workflow_defs_json.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/14_final_workflow.ipynb` & `infer-subc-0.0.post1/notebooks/14_final_workflow.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/00.1_pipeline_setup_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/00.1_pipeline_setup_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/00.2_extract_optimal_Z.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/00.2_extract_optimal_Z.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/01_infer_nuclei_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/01_infer_nuclei_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/02_infer_soma_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/02_infer_soma_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/02a_infer_soma_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/02a_infer_soma_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/02b_infer_neurites_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/02b_infer_neurites_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/02c_infer_wholecell_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/02c_infer_wholecell_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/03_infer_cytosol_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/03_infer_cytosol_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/04_infer_lysosome_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/04_infer_lysosome_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/05_infer_mitochondria_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/05_infer_mitochondria_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/06_infer_golgi_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/06_infer_golgi_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/07_infer_peroxisome_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/07_infer_peroxisome_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/08_infer_endoplasmic_reticulum_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/08_infer_endoplasmic_reticulum_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/09_infer_lipid_body_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/09_infer_lipid_body_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/10_batch_process_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/10_batch_process_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/10_batch_process_3Dv2.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/10_batch_process_3Dv2.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/999_fn_prototypes_json.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/999_fn_prototypes_json.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/A_spectral_test.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/A_spectral_test.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/_centrosome_routines.py` & `infer-subc-0.0.post1/notebooks/todelete/_centrosome_routines.py`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/_graveyard.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/_graveyard.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/new02a_infer_soma_3D.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/new02a_infer_soma_3D.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/notebooks/todelete/test_soma_seg.ipynb` & `infer-subc-0.0.post1/notebooks/todelete/test_soma_seg.ipynb`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/setup.cfg` & `infer-subc-0.0.post1/setup.cfg`

 * *Files 6% similar despite different names*

```diff
@@ -37,15 +37,14 @@
 	numpy
 	aicsimageio >= 4.7.0
 	scipy    #>=1.1.0
 	numpy    #>=1.15.1
 	scikit-image #>=0.18.0,<0.19.0
 	pandas   #>=0.23.4
 	jupyter
-	centrosome
 platforms = any
 python_requires = >=3.8
 include_package_data = True
 package_dir = 
 	= .
 setup_requires = setuptools_scm
```

### Comparing `infer-subc-0.0.4b0/test.yaml` & `infer-subc-0.0.post1/test.yaml`

 * *Files identical despite different names*

### Comparing `infer-subc-0.0.4b0/windows_notes.md` & `infer-subc-0.0.post1/windows_notes.md`

 * *Files identical despite different names*

