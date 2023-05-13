# Comparing `tmp/message-ix-models-2023.4.2.tar.gz` & `tmp/message-ix-models-2023.5.13.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "message-ix-models-2023.4.2.tar", last modified: Sun Apr  2 09:02:12 2023, max compression
+gzip compressed data, was "message-ix-models-2023.5.13.tar", last modified: Sat May 13 12:05:38 2023, max compression
```

## Comparing `message-ix-models-2023.4.2.tar` & `message-ix-models-2023.5.13.tar`

### file list

```diff
@@ -1,331 +1,330 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.gitattributes
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.424438 message-ix-models-2023.4.2/.github/
--rw-r--r--   0 runner    (1001) docker     (123)       50 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.github/codecov.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.github/pull_request_template.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.424438 message-ix-models-2023.4.2/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      779 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.github/workflows/lint.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.github/workflows/publish.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     3127 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.github/workflows/pytest.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1916 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      190 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/.readthedocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)      111 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/
--rw-r--r--   0 runner    (1001) docker     (123)      634 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/_static/
--rw-r--r--   0 runner    (1001) docker     (123)    56233 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/combined-logo-white.png
--rw-r--r--   0 runner    (1001) docker     (123)    49140 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/combined-logo-white.svg
--rw-r--r--   0 runner    (1001) docker     (123)     1709 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/custom.css
--rw-r--r--   0 runner    (1001) docker     (123)     6608 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/favicon.svg
--rw-r--r--   0 runner    (1001) docker     (123)    22635 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/logo-white.png
--rw-r--r--   0 runner    (1001) docker     (123)    13459 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_static/message-ix-models-logo-white.svg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/_template/
--rw-r--r--   0 runner    (1001) docker     (123)      665 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_template/autosummary-class.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1254 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/_template/autosummary-module.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/api/
--rw-r--r--   0 runner    (1001) docker     (123)     5785 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/disutility.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2082 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/model-bare.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/model-build.rst
--rw-r--r--   0 runner    (1001) docker     (123)      613 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/model-emissions.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2118 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/model.rst
--rw-r--r--   0 runner    (1001) docker     (123)      192 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/project.rst
--rw-r--r--   0 runner    (1001) docker     (123)      510 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/testing.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1477 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/tools.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4332 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/util.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/api/workflow.rst
--rw-r--r--   0 runner    (1001) docker     (123)       76 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/bibliography.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7952 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/cli.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)    11016 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/data.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/develop.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2544 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/distrib.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      297 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/install.rst
--rw-r--r--   0 runner    (1001) docker     (123)      485 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/main.bib
--rw-r--r--   0 runner    (1001) docker     (123)      760 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)     2861 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/migrate.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/pkg-data/
--rw-r--r--   0 runner    (1001) docker     (123)     1323 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/pkg-data/codelists.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/pkg-data/iiasa-se.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1861 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/pkg-data/node.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1273 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/pkg-data/relation.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/pkg-data/year.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2044 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/releasing.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3754 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/repro.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/doc/water/
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/water/files.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7308 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/water/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     8928 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/doc/whatsnew.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.428438 message-ix-models-2023.4.2/message_ix_models/
--rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4734 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/cd_links/
--rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/cd_links/unit.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6212 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/commodity.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/edits/
--rw-r--r--   0 runner    (1001) docker     (123)     2208 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/edits/messageix-transport-core.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     4763 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/edits/messageix-transport-input.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/iiasa-se/
--rw-r--r--   0 runner    (1001) docker     (123)      610 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/iiasa-se/def-regions.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/iiasa-se/mappings-R12.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      986 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/level.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/node/
--rw-r--r--   0 runner    (1001) docker     (123)     2014 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/ADVANCE.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    18288 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/B210-R11.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      168 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/ISR.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2835 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/R11.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2897 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/R12.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2840 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/R14.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     5440 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/R32.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2675 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/RCP.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      168 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/node/ZMB.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/relation/
--rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/relation/A.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6717 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/relation/B.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    55164 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/relation/CD-LINKS.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    72062 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/technology.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.416438 message-ix-models-2023.4.2/message_ix_models/data/test/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/test/advance/
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/test/advance/advance_compare_20171018-134445.csv.zip
--rw-r--r--   0 runner    (1001) docker     (123)       26 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/unit.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models/data/water/
--rw-r--r--   0 runner    (1001) docker     (123)      184 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/.gitattributes
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.436438 message-ix-models-2023.4.2/message_ix_models/data/water/availability/
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_2p6_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_2p6_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_5y_m_2p6_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_5y_m_7p0_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_5y_m_no_climate_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_6p0_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_7p0_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_no_climate_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/e-flow_no_climate_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/gw_energy_intensity_depth_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/gw_energy_intensity_depth_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/historical_new_cap_gw_sw_km3_year_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      128 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/historical_new_cap_gw_sw_km3_year_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_2p6_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_6p0_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_6p0_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_6p0_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_7p0_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_7p0_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_7p0_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_m_2p6_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_m_7p0_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_m_no_climate_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qr_5y_no_climate_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_2p6_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_6p0_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_6p0_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_6p0_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_7p0_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_7p0_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_7p0_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_m_2p6_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_m_7p0_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_m_no_climate_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_high_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_high_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_low_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_low_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_med_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/availability/qtot_5y_no_climate_med_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      249 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/config.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.436438 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/basins_by_region_simpl_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/basins_by_region_simpl_R12.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/basins_by_region_simpl_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/basins_country_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/delineation/basins_country_ZMB.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.436438 message-ix-models-2023.4.2/message_ix_models/data/water/demands/
--rw-r--r--   0 runner    (1001) docker     (123)      276 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/.gitattributes
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/country_region_map_key.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.440438 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.440438 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/
--rw-r--r--   0 runner    (1001) docker     (123)      132 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/all_rates_SSP2.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_manufacturing_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_manufacturing_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_recycling_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_return2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_withdrawal2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_withdrawal_baseline.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.440438 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_manufacturing_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_manufacturing_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_recycling_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_return2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_withdrawal2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)    72704 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/Thumbs.db
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.440438 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/all_rates_SSP2.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_m_water_demands.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_manufacturing_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_manufacturing_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_withdrawal_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_connection_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_recycling_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_return2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_return_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_treatment_rate_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_withdrawal2_baseline.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_withdrawal_baseline.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/
--rw-r--r--   0 runner    (1001) docker     (123)    14799 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/desalination.xlsx
--rw-r--r--   0 runner    (1001) docker     (123)    13915 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/extraction_techs.xlsx
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/historical_capacity_desalination_km3_year_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/historical_capacity_desalination_km3_year_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/projected_desalination_potential_km3_year_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/projected_desalination_potential_km3_year_ZMB.csv
--rw-r--r--   0 runner    (1001) docker     (123)    15469 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/water_distribution.xlsx
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/
--rw-r--r--   0 runner    (1001) docker     (123)      132 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/POWER_PLANTS_2016_Raptis.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cool_techs_country_share.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share_R12.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_country.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg_R11.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg_R12.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/enhanced_fsu_cool_techs_share.csv
--rw-r--r--   0 runner    (1001) docker     (123)    24537 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/power_plant_cooling_impact_MESSAGE.xlsx
--rw-r--r--   0 runner    (1001) docker     (123)      128 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/raptis_types_map_cooling_type.csv
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/raptis_types_map_unit_type.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/tech_names_ssp_msg.csv
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/tech_water_performance_ssp_msg.csv
--rw-r--r--   0 runner    (1001) docker     (123)    28513 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/set.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    42152 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/water/technology.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/data/year/
--rw-r--r--   0 runner    (1001) docker     (123)     1144 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/year/A.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/data/year/B.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/model/
--rw-r--r--   0 runner    (1001) docker     (123)      133 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4877 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/bare.py
--rw-r--r--   0 runner    (1001) docker     (123)     5577 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/build.py
--rw-r--r--   0 runner    (1001) docker     (123)      431 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      307 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/data.py
--rw-r--r--   0 runner    (1001) docker     (123)     7310 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/disutility.py
--rw-r--r--   0 runner    (1001) docker     (123)     2757 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)    10650 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/structure.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/model/water/
--rw-r--r--   0 runner    (1001) docker     (123)       58 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8335 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/build.py
--rw-r--r--   0 runner    (1001) docker     (123)     8322 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/model/water/data/
--rw-r--r--   0 runner    (1001) docker     (123)     1869 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    30512 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/demands.py
--rw-r--r--   0 runner    (1001) docker     (123)    28386 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/infrastructure.py
--rw-r--r--   0 runner    (1001) docker     (123)     6234 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/irrigation.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/
--rw-r--r--   0 runner    (1001) docker     (123)    12653 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/calculate_ppl_cooling_technology_shares.r
--rw-r--r--   0 runner    (1001) docker     (123)    38780 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/desalination.R
--rw-r--r--   0 runner    (1001) docker     (123)    38900 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/generate_water_constraints.R
--rw-r--r--   0 runner    (1001) docker     (123)    14302 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/generate_water_constraints_monthly.r
--rw-r--r--   0 runner    (1001) docker     (123)    12058 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/groundwater_harmonize.r
--rw-r--r--   0 runner    (1001) docker     (123)    11332 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_basin.py
--rw-r--r--   0 runner    (1001) docker     (123)    10839 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_raster.py
--rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_spatial.R
--rw-r--r--   0 runner    (1001) docker     (123)    29422 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/water_for_ppl.py
--rw-r--r--   0 runner    (1001) docker     (123)    27706 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/data/water_supply.py
--rw-r--r--   0 runner    (1001) docker     (123)    43611 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/reporting.py
--rw-r--r--   0 runner    (1001) docker     (123)     4560 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/model/water/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.444438 message-ix-models-2023.4.2/message_ix_models/project/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/project/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    12462 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/testing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/tests/model/
--rw-r--r--   0 runner    (1001) docker     (123)       62 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_bare.py
--rw-r--r--   0 runner    (1001) docker     (123)     2659 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_build.py
--rw-r--r--   0 runner    (1001) docker     (123)      279 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      735 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     8866 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_disutility.py
--rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_emissions.py
--rw-r--r--   0 runner    (1001) docker     (123)     8232 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/model/test_structure.py
--rw-r--r--   0 runner    (1001) docker     (123)     1758 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/test_cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      681 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/test_import.py
--rw-r--r--   0 runner    (1001) docker     (123)      940 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/test_testing.py
--rw-r--r--   0 runner    (1001) docker     (123)    12580 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/test_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4644 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/test_workflow.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/tests/tools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1630 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/tools/test_advance.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/tests/util/
--rw-r--r--   0 runner    (1001) docker     (123)       60 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3546 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_click.py
--rw-r--r--   0 runner    (1001) docker     (123)     3354 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     8090 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_context.py
--rw-r--r--   0 runner    (1001) docker     (123)      968 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     4561 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_node.py
--rw-r--r--   0 runner    (1001) docker     (123)     6522 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_scenarioinfo.py
--rw-r--r--   0 runner    (1001) docker     (123)      606 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tests/util/test_sdmx.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/tools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/tools/advance.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/message_ix_models/util/
--rw-r--r--   0 runner    (1001) docker     (123)    20956 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2777 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/_convert_units.py
--rw-r--r--   0 runner    (1001) docker     (123)     4917 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/_logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     2903 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     5823 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/click.py
--rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/common.py
--rw-r--r--   0 runner    (1001) docker     (123)     6142 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    12846 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/context.py
--rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/importlib.py
--rw-r--r--   0 runner    (1001) docker     (123)     3734 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/node.py
--rw-r--r--   0 runner    (1001) docker     (123)    10638 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/scenarioinfo.py
--rw-r--r--   0 runner    (1001) docker     (123)     3097 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/util/sdmx.py
--rw-r--r--   0 runner    (1001) docker     (123)     8186 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/message_ix_models/workflow.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-02 09:02:12.432438 message-ix-models-2023.4.2/message_ix_models.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    15804 2023-04-02 09:02:12.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       58 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      281 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-02 09:01:53.000000 message-ix-models-2023.4.2/message_ix_models.egg-info/zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      772 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1002 2023-04-02 09:02:12.448438 message-ix-models-2023.4.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       58 2023-04-02 09:01:41.000000 message-ix-models-2023.4.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.466146 message-ix-models-2023.5.13/
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.flake8
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.gitattributes
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.430146 message-ix-models-2023.5.13/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.github/codecov.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.github/pull_request_template.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.430146 message-ix-models-2023.5.13/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      928 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.github/workflows/lint.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      395 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.github/workflows/publish.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2492 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.github/workflows/pytest.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1916 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/.readthedocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2610 2023-05-13 12:05:38.466146 message-ix-models-2023.5.13/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      111 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.434146 message-ix-models-2023.5.13/doc/
+-rw-r--r--   0 runner    (1001) docker     (123)      634 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.434146 message-ix-models-2023.5.13/doc/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)    56233 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/combined-logo-white.png
+-rw-r--r--   0 runner    (1001) docker     (123)    49140 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/combined-logo-white.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     1709 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/custom.css
+-rw-r--r--   0 runner    (1001) docker     (123)     6608 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/favicon.svg
+-rw-r--r--   0 runner    (1001) docker     (123)    22635 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/logo-white.png
+-rw-r--r--   0 runner    (1001) docker     (123)    13459 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_static/message-ix-models-logo-white.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.434146 message-ix-models-2023.5.13/doc/_template/
+-rw-r--r--   0 runner    (1001) docker     (123)      665 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_template/autosummary-class.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1254 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/_template/autosummary-module.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.434146 message-ix-models-2023.5.13/doc/api/
+-rw-r--r--   0 runner    (1001) docker     (123)     5785 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/disutility.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2082 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/model-bare.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/model-build.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      613 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/model-emissions.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2118 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/model.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      192 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/project.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/testing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1477 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/tools.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4332 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/util.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/api/workflow.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       76 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/bibliography.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7952 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/cli.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11016 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/data.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/develop.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2544 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/distrib.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      182 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/install.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      485 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/main.bib
+-rw-r--r--   0 runner    (1001) docker     (123)      760 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)     2861 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/migrate.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/doc/pkg-data/
+-rw-r--r--   0 runner    (1001) docker     (123)     1323 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/pkg-data/codelists.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/pkg-data/iiasa-se.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1861 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/pkg-data/node.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1273 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/pkg-data/relation.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1658 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/pkg-data/year.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2044 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/releasing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3754 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/repro.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/doc/water/
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/water/files.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7308 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/water/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     9044 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/doc/whatsnew.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/
+-rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4734 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/data/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/data/cd_links/
+-rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/cd_links/unit.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     6212 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/commodity.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/data/edits/
+-rw-r--r--   0 runner    (1001) docker     (123)     2208 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/edits/messageix-transport-core.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     4763 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/edits/messageix-transport-input.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/data/iiasa-se/
+-rw-r--r--   0 runner    (1001) docker     (123)      610 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/iiasa-se/def-regions.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/iiasa-se/mappings-R12.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      986 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/level.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models/data/node/
+-rw-r--r--   0 runner    (1001) docker     (123)     2014 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/ADVANCE.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    18288 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/B210-R11.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/ISR.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2835 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/R11.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2897 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/R12.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2840 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/R14.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     5440 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/R32.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2675 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/RCP.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/node/ZMB.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.442146 message-ix-models-2023.5.13/message_ix_models/data/relation/
+-rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/relation/A.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     6717 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/relation/B.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    55164 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/relation/CD-LINKS.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    72062 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/technology.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.430146 message-ix-models-2023.5.13/message_ix_models/data/test/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.442146 message-ix-models-2023.5.13/message_ix_models/data/test/advance/
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/test/advance/advance_compare_20171018-134445.csv.zip
+-rw-r--r--   0 runner    (1001) docker     (123)       26 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/unit.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.442146 message-ix-models-2023.5.13/message_ix_models/data/water/
+-rw-r--r--   0 runner    (1001) docker     (123)      184 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/.gitattributes
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.446146 message-ix-models-2023.5.13/message_ix_models/data/water/availability/
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_2p6_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_2p6_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_5y_m_2p6_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_5y_m_7p0_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_5y_m_no_climate_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_6p0_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_7p0_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_no_climate_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/e-flow_no_climate_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/gw_energy_intensity_depth_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/gw_energy_intensity_depth_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/historical_new_cap_gw_sw_km3_year_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      128 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/historical_new_cap_gw_sw_km3_year_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_2p6_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_6p0_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_6p0_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_6p0_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_7p0_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_7p0_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_7p0_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_m_2p6_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_m_7p0_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_m_no_climate_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qr_5y_no_climate_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_2p6_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_6p0_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_6p0_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_6p0_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_7p0_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_7p0_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_7p0_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_m_2p6_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_m_7p0_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_m_no_climate_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_high_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_high_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_low_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_low_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_med_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/availability/qtot_5y_no_climate_med_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      249 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/config.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.446146 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/basins_by_region_simpl_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/basins_by_region_simpl_R12.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/basins_by_region_simpl_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/basins_country_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/delineation/basins_country_ZMB.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.446146 message-ix-models-2023.5.13/message_ix_models/data/water/demands/
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/.gitattributes
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/country_region_map_key.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.450146 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.450146 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/
+-rw-r--r--   0 runner    (1001) docker     (123)      132 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/all_rates_SSP2.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_manufacturing_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_manufacturing_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_rural_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_recycling_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_return2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_withdrawal2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R11/ssp2_regional_urban_withdrawal_baseline.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.450146 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_manufacturing_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_manufacturing_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_rural_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_recycling_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_return2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_withdrawal2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/R12/ssp2_regional_urban_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    72704 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/Thumbs.db
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.454146 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/all_rates_SSP2.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_m_water_demands.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_manufacturing_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_manufacturing_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_rural_withdrawal_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_connection_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_recycling_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_return2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_return_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_treatment_rate_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_withdrawal2_baseline.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/ZMB/ssp2_regional_urban_withdrawal_baseline.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.454146 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/
+-rw-r--r--   0 runner    (1001) docker     (123)    14799 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/desalination.xlsx
+-rw-r--r--   0 runner    (1001) docker     (123)    13915 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/extraction_techs.xlsx
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/historical_capacity_desalination_km3_year_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/historical_capacity_desalination_km3_year_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/projected_desalination_potential_km3_year_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/projected_desalination_potential_km3_year_ZMB.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    15469 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/water_distribution.xlsx
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.454146 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/
+-rw-r--r--   0 runner    (1001) docker     (123)      132 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/POWER_PLANTS_2016_Raptis.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cool_techs_country_share.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cool_techs_region_share_R12.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_country.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg_R11.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/cooltech_cost_and_shares_ssp_msg_R12.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/enhanced_fsu_cool_techs_share.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    24537 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/power_plant_cooling_impact_MESSAGE.xlsx
+-rw-r--r--   0 runner    (1001) docker     (123)      128 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/raptis_types_map_cooling_type.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/raptis_types_map_unit_type.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/tech_names_ssp_msg.csv
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/tech_water_performance_ssp_msg.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    28513 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/set.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    42152 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/water/technology.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/data/year/
+-rw-r--r--   0 runner    (1001) docker     (123)     1144 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/year/A.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/data/year/B.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/model/
+-rw-r--r--   0 runner    (1001) docker     (123)      133 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4877 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/bare.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5577 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/build.py
+-rw-r--r--   0 runner    (1001) docker     (123)      431 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7310 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/disutility.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2757 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10667 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/structure.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/model/water/
+-rw-r--r--   0 runner    (1001) docker     (123)       58 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8335 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/build.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8322 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/model/water/data/
+-rw-r--r--   0 runner    (1001) docker     (123)     1869 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30512 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/demands.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28386 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/infrastructure.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6234 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/irrigation.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/
+-rw-r--r--   0 runner    (1001) docker     (123)    12653 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/calculate_ppl_cooling_technology_shares.r
+-rw-r--r--   0 runner    (1001) docker     (123)    38780 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/desalination.R
+-rw-r--r--   0 runner    (1001) docker     (123)    38900 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/generate_water_constraints.R
+-rw-r--r--   0 runner    (1001) docker     (123)    14302 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/generate_water_constraints_monthly.r
+-rw-r--r--   0 runner    (1001) docker     (123)    12058 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/groundwater_harmonize.r
+-rw-r--r--   0 runner    (1001) docker     (123)    11332 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_basin.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10839 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_raster.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_spatial.R
+-rw-r--r--   0 runner    (1001) docker     (123)    29422 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/water_for_ppl.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27706 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/data/water_supply.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43611 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/reporting.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4560 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/model/water/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.458146 message-ix-models-2023.5.13/message_ix_models/project/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/project/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    12462 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/testing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.462146 message-ix-models-2023.5.13/message_ix_models/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.462146 message-ix-models-2023.5.13/message_ix_models/tests/model/
+-rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_bare.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2659 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_build.py
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      735 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8866 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_disutility.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_emissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8232 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/model/test_structure.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1758 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/test_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      681 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/test_import.py
+-rw-r--r--   0 runner    (1001) docker     (123)      940 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/test_testing.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12616 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/test_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4644 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/test_workflow.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.462146 message-ix-models-2023.5.13/message_ix_models/tests/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1630 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/tools/test_advance.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.462146 message-ix-models-2023.5.13/message_ix_models/tests/util/
+-rw-r--r--   0 runner    (1001) docker     (123)       60 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3546 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_click.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3354 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8090 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_context.py
+-rw-r--r--   0 runner    (1001) docker     (123)      968 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4561 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6522 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_scenarioinfo.py
+-rw-r--r--   0 runner    (1001) docker     (123)      606 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tests/util/test_sdmx.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.462146 message-ix-models-2023.5.13/message_ix_models/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/tools/advance.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.466146 message-ix-models-2023.5.13/message_ix_models/util/
+-rw-r--r--   0 runner    (1001) docker     (123)    20956 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2777 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/_convert_units.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4917 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/_logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2903 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5823 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/click.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6142 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12846 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/importlib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3734 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/node.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10638 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/scenarioinfo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3097 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/util/sdmx.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8186 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/message_ix_models/workflow.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:05:38.438146 message-ix-models-2023.5.13/message_ix_models.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2610 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    15757 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       58 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      234 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-05-13 12:05:38.000000 message-ix-models-2023.5.13/message_ix_models.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2875 2023-05-13 12:04:57.000000 message-ix-models-2023.5.13/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:05:38.466146 message-ix-models-2023.5.13/setup.cfg
```

### Comparing `message-ix-models-2023.4.2/.github/pull_request_template.md` & `message-ix-models-2023.5.13/.github/pull_request_template.md`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/.github/workflows/pytest.yaml` & `message-ix-models-2023.5.13/.github/workflows/pytest.yaml`

 * *Files 22% similar despite different names*

```diff
@@ -10,83 +10,71 @@
   - cron: "0 5 * * *"
 
 # Cancel previous runs that have not completed
 concurrency:
   group: ${{ github.workflow }}-${{ github.head_ref || github.run_id }}
   cancel-in-progress: true
 
-env:
-  # For setuptools-scm. With fetch --tags below, this ensures that enough
-  # history is fetched to contain the latest tag, so that setuptools-scm can
-  # generate the version number. Update:
-  # - See https://github.com/iiasa/message-ix-models/releases, at "NN commits to
-  #   main since this release". The value should be at least equal to NN + the
-  #   number of commits on any PR branch.
-  # - Reset to a lower value, e.g. 100, after a new release.
-  depth: 100
-
 jobs:
   pytest:
     strategy:
       matrix:
         # One job per OS; latest python version testable on GitHub actions.
         # These should match the versions used in the "pytest" workflows of both
         # ixmp and message_ix.
         version:
         - { os: macos-latest, python: "3.10" }
         - { os: ubuntu-latest, python: "3.10" }
         - { os: windows-latest, python: "3.10" }
         # Versions of both ixmp and message_ix to use
         upstream-version:
-        - v3.4.0  # Minimum version given in setup.cfg
-        - v3.5.0
-        - v3.6.0  # Latest released version
+        # Temporarily disabled (iiasa/ixmp#477)
+        # - v3.4.0  # Minimum version given in setup.cfg
+        # - v3.5.0
+        # - v3.6.0  # Latest released version
         - main    # Development version
 
       fail-fast: false
 
     runs-on: ${{ matrix.version.os }}
     name: ${{ matrix.version.os }}-py${{ matrix.version.python }}-upstream-${{ matrix.upstream-version }}
 
     steps:
     - name: Check out message-ix-models
       uses: actions/checkout@v3
       with:
         lfs: true
-        path: message-ix-models
         fetch-depth: ${{ env.depth }}
 
-    - name: Fetch tags (for setuptools-scm)
-      run: (cd message-ix-models; git fetch --tags --depth=${{ env.depth }})
-      shell: bash
-
     - uses: actions/setup-python@v4
       with:
         python-version: ${{ matrix.version.python }}
         cache: pip
-        cache-dependency-path: "**/setup.cfg"
+        cache-dependency-path: "**/pyproject.toml"
 
     - uses: iiasa/actions/setup-gams@main
       with:
         version: 25.1.1
         license: ${{ secrets.GAMS_LICENSE }}
 
     - name: Install packages and dependencies
       run: |
         pip install --upgrade "ixmp @ git+https://github.com/iiasa/ixmp.git@${{ matrix.upstream-version }}"
         pip install --upgrade "message-ix @ git+https://github.com/iiasa/message_ix.git@${{ matrix.upstream-version }}"
-        pip install ./message-ix-models[tests]
+        pip install .[tests]
 
     - name: Run test suite using pytest
-      working-directory: message-ix-models
-      run: pytest message_ix_models -rA --verbose --color=yes --cov-report=xml --cov-report=term-missing --numprocesses=auto
+      run: |
+        pytest message_ix_models \
+          -rA --verbose --color=yes --durations=20 \
+          --cov-report=term-missing --cov-report=xml \
+          --numprocesses=auto
+      shell: bash
 
     - name: Test documentation build using Sphinx
       if: startsWith(matrix.os, 'ubuntu')
       env:
         RTD_TOKEN_MESSAGE_DATA: ${{ secrets.RTD_TOKEN_MESSAGE_DATA }}
-      run: make --directory=message-ix-models/doc html
+      run: make --directory=doc html
 
     - name: Upload test coverage to Codecov.io
       uses: codecov/codecov-action@v3
-      with:
-        root_dir: message-ix-models
```

### Comparing `message-ix-models-2023.4.2/.gitignore` & `message-ix-models-2023.5.13/.gitignore`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/LICENSE` & `message-ix-models-2023.5.13/LICENSE`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/PKG-INFO` & `message-ix-models-2023.5.13/README.rst`

 * *Files 6% similar despite different names*

```diff
@@ -1,21 +1,7 @@
-Metadata-Version: 2.1
-Name: message-ix-models
-Version: 2023.4.2
-Summary: Tools for the MESSAGEix-GLOBIOM family of models
-Home-page: https://github.com/iiasa/message-ix-models
-Author: IIASA Energy, Climate, and Environment (ECE) Program
-Author-email: message_ix@iiasa.ac.at
-License: Apache 2.0
-Requires-Python: >=3.7
-Description-Content-Type: text/x-rst
-Provides-Extra: tests
-Provides-Extra: docs
-License-File: LICENSE
-
 Tools for MESSAGEix-GLOBIOM models
 **********************************
 
 .. image:: https://img.shields.io/pypi/v/message-ix-models.svg
    :alt: PyPI version
    :target: https://pypi.python.org/pypi/message-ix-models/
```

### Comparing `message-ix-models-2023.4.2/doc/Makefile` & `message-ix-models-2023.5.13/doc/Makefile`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/combined-logo-white.png` & `message-ix-models-2023.5.13/doc/_static/combined-logo-white.png`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/combined-logo-white.svg` & `message-ix-models-2023.5.13/doc/_static/combined-logo-white.svg`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/custom.css` & `message-ix-models-2023.5.13/doc/_static/custom.css`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/favicon.svg` & `message-ix-models-2023.5.13/doc/_static/favicon.svg`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/logo-white.png` & `message-ix-models-2023.5.13/doc/_static/logo-white.png`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_static/message-ix-models-logo-white.svg` & `message-ix-models-2023.5.13/doc/_static/message-ix-models-logo-white.svg`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_template/autosummary-class.rst` & `message-ix-models-2023.5.13/doc/_template/autosummary-class.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/_template/autosummary-module.rst` & `message-ix-models-2023.5.13/doc/_template/autosummary-module.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/disutility.rst` & `message-ix-models-2023.5.13/doc/api/disutility.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/model-bare.rst` & `message-ix-models-2023.5.13/doc/api/model-bare.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/model-build.rst` & `message-ix-models-2023.5.13/doc/api/model-build.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/model-emissions.rst` & `message-ix-models-2023.5.13/doc/api/model-emissions.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/model.rst` & `message-ix-models-2023.5.13/doc/api/model.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/tools.rst` & `message-ix-models-2023.5.13/doc/api/tools.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/util.rst` & `message-ix-models-2023.5.13/doc/api/util.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/api/workflow.rst` & `message-ix-models-2023.5.13/doc/api/workflow.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/cli.rst` & `message-ix-models-2023.5.13/doc/cli.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/conf.py` & `message-ix-models-2023.5.13/doc/conf.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/data.rst` & `message-ix-models-2023.5.13/doc/data.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/develop.rst` & `message-ix-models-2023.5.13/doc/develop.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/distrib.rst` & `message-ix-models-2023.5.13/doc/distrib.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/index.rst` & `message-ix-models-2023.5.13/doc/index.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/make.bat` & `message-ix-models-2023.5.13/doc/make.bat`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/migrate.rst` & `message-ix-models-2023.5.13/doc/migrate.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/pkg-data/codelists.rst` & `message-ix-models-2023.5.13/doc/pkg-data/codelists.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/pkg-data/iiasa-se.rst` & `message-ix-models-2023.5.13/doc/pkg-data/iiasa-se.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/pkg-data/node.rst` & `message-ix-models-2023.5.13/doc/pkg-data/node.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/pkg-data/relation.rst` & `message-ix-models-2023.5.13/doc/pkg-data/relation.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/pkg-data/year.rst` & `message-ix-models-2023.5.13/doc/pkg-data/year.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/releasing.rst` & `message-ix-models-2023.5.13/doc/releasing.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/repro.rst` & `message-ix-models-2023.5.13/doc/repro.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/water/files.rst` & `message-ix-models-2023.5.13/doc/water/files.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/water/index.rst` & `message-ix-models-2023.5.13/doc/water/index.rst`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/doc/whatsnew.rst` & `message-ix-models-2023.5.13/doc/whatsnew.rst`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,18 @@
 What's new
 **********
 
 .. Next release
 .. ============
 
+v2023.5.13 (2023-05-13)
+=======================
+
+- Adjust :func:`.generate_product` for pandas 2.0.0 (:pull:`98`).
+
 2023.4.2
 ========
 
 - Add :doc:`/water/index` (:pull:`88`, :pull:`91`).
 - New utility function :func:`.replace_par_data` (:pull:`90`).
 - :func:`.disutility.get_spec` preserves all :class:`Annotations <~.sdmx.model.v21.Annotation>` attached to the :class:`~.sdmx.model.v21.Code` object used as a template for usage technologies (:pull:`90`).
 - Add ``CO2_Emission_Global_Total`` to the :ref:`“A” relation codelist <relation-yaml>` (:pull:`90`).
```

### Comparing `message-ix-models-2023.4.2/message_ix_models/__init__.py` & `message-ix-models-2023.5.13/message_ix_models/__init__.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/cli.py` & `message-ix-models-2023.5.13/message_ix_models/cli.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/cd_links/unit.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/cd_links/unit.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/commodity.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/commodity.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/edits/messageix-transport-core.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/edits/messageix-transport-core.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/edits/messageix-transport-input.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/edits/messageix-transport-input.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/iiasa-se/def-regions.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/iiasa-se/def-regions.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/iiasa-se/mappings-R12.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/iiasa-se/mappings-R12.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/level.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/level.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/ADVANCE.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/ADVANCE.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/B210-R11.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/B210-R11.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/R11.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/R11.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/R12.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/R12.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/R14.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/R14.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/R32.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/R32.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/node/RCP.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/node/RCP.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/relation/A.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/relation/A.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/relation/B.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/relation/B.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/relation/CD-LINKS.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/relation/CD-LINKS.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/technology.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/technology.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/demands/harmonized/Thumbs.db` & `message-ix-models-2023.5.13/message_ix_models/data/water/demands/harmonized/Thumbs.db`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/desalination.xlsx` & `message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/desalination.xlsx`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/extraction_techs.xlsx` & `message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/extraction_techs.xlsx`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/infrastructure/water_distribution.xlsx` & `message-ix-models-2023.5.13/message_ix_models/data/water/infrastructure/water_distribution.xlsx`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/ppl_cooling_tech/power_plant_cooling_impact_MESSAGE.xlsx` & `message-ix-models-2023.5.13/message_ix_models/data/water/ppl_cooling_tech/power_plant_cooling_impact_MESSAGE.xlsx`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/set.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/water/set.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/water/technology.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/water/technology.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/year/A.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/year/A.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/data/year/B.yaml` & `message-ix-models-2023.5.13/message_ix_models/data/year/B.yaml`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/bare.py` & `message-ix-models-2023.5.13/message_ix_models/model/bare.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/build.py` & `message-ix-models-2023.5.13/message_ix_models/model/build.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/config.py` & `message-ix-models-2023.5.13/message_ix_models/model/config.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/disutility.py` & `message-ix-models-2023.5.13/message_ix_models/model/disutility.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/emissions.py` & `message-ix-models-2023.5.13/message_ix_models/model/emissions.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/structure.py` & `message-ix-models-2023.5.13/message_ix_models/model/structure.py`

 * *Files 0% similar despite different names*

```diff
@@ -145,15 +145,15 @@
         result = template.copy()  # Duplicate the template
 
         fmt = dict(zip(dims.keys(), item))  # Format the ID and name
         result.id = result.id.format(**fmt)
         result.name = str(result.name).format(**fmt)  # type: ignore [assignment]
 
         codes.append(result)  # Store code and indices
-        indices.append(item)
+        indices.append(tuple(map(str, item)))
 
     # - Convert length-N sequence of D-tuples to D iterables each of length N.
     # - Convert to D × 1-dimensional xr.DataArrays, each of length N.
     tmp = zip(*indices)
     indexers = {d: xr.DataArray(list(i), dims=name) for d, i in zip(dims.keys(), tmp)}
     # Corresponding indexer with the full code IDs
     indexers[name] = xr.DataArray([c.id for c in codes], dims=name)
```

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/build.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/build.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/cli.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/cli.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/__init__.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/__init__.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/demands.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/demands.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/infrastructure.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/infrastructure.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/irrigation.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/irrigation.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/calculate_ppl_cooling_technology_shares.r` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/calculate_ppl_cooling_technology_shares.r`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/desalination.R` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/desalination.R`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/generate_water_constraints.R` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/generate_water_constraints.R`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/generate_water_constraints_monthly.r` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/generate_water_constraints_monthly.r`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/groundwater_harmonize.r` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/groundwater_harmonize.r`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_basin.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_basin.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_raster.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_raster.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/pre_processing/hydro_agg_spatial.R` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/pre_processing/hydro_agg_spatial.R`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/water_for_ppl.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/water_for_ppl.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/data/water_supply.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/data/water_supply.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/reporting.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/reporting.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/model/water/utils.py` & `message-ix-models-2023.5.13/message_ix_models/model/water/utils.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/testing.py` & `message-ix-models-2023.5.13/message_ix_models/testing.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_bare.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_bare.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_build.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_build.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_config.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_config.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_disutility.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_disutility.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_emissions.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_emissions.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/model/test_structure.py` & `message-ix-models-2023.5.13/message_ix_models/tests/model/test_structure.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/test_cli.py` & `message-ix-models-2023.5.13/message_ix_models/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/test_import.py` & `message-ix-models-2023.5.13/message_ix_models/tests/test_import.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/test_testing.py` & `message-ix-models-2023.5.13/message_ix_models/tests/test_testing.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/test_util.py` & `message-ix-models-2023.5.13/message_ix_models/tests/test_util.py`

 * *Files 1% similar despite different names*

```diff
@@ -150,15 +150,18 @@
 
     exp = series_of_pint_quantity(
         [registry("4.9895 kg"), registry("46.2664 kg"), registry("454.9531 kg")],
     )
 
     # With store="quantity", a series of pint.Quantity is returned
     result = convert_units(*args, store="quantity")
-    assert all(np.isclose(a, b, atol=1e-4) for a, b in zip(exp.values, result.values))
+    assert all(
+        np.isclose(a, b, atol=1e-4 * registry.kg)
+        for a, b in zip(exp.values, result.values)
+    )
 
     # With store="magnitude", a series of floats
     exp = pd.Series([q.magnitude for q in exp.values], name="bar")
     assert_series_equal(exp, convert_units(*args, store="magnitude"), check_dtype=False)
 
     # Other values for store= are errors
     with pytest.raises(ValueError, match="store = 'foo'"):
```

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/test_workflow.py` & `message-ix-models-2023.5.13/message_ix_models/tests/test_workflow.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/tools/test_advance.py` & `message-ix-models-2023.5.13/message_ix_models/tests/tools/test_advance.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_cache.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_cache.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_click.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_click.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_config.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_config.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_context.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_context.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_logging.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_logging.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_node.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_node.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_scenarioinfo.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_scenarioinfo.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tests/util/test_sdmx.py` & `message-ix-models-2023.5.13/message_ix_models/tests/util/test_sdmx.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/tools/advance.py` & `message-ix-models-2023.5.13/message_ix_models/tools/advance.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/__init__.py` & `message-ix-models-2023.5.13/message_ix_models/util/__init__.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/_convert_units.py` & `message-ix-models-2023.5.13/message_ix_models/util/_convert_units.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/_logging.py` & `message-ix-models-2023.5.13/message_ix_models/util/_logging.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/cache.py` & `message-ix-models-2023.5.13/message_ix_models/util/cache.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/click.py` & `message-ix-models-2023.5.13/message_ix_models/util/click.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/common.py` & `message-ix-models-2023.5.13/message_ix_models/util/common.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/config.py` & `message-ix-models-2023.5.13/message_ix_models/util/config.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/context.py` & `message-ix-models-2023.5.13/message_ix_models/util/context.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/importlib.py` & `message-ix-models-2023.5.13/message_ix_models/util/importlib.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/node.py` & `message-ix-models-2023.5.13/message_ix_models/util/node.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/scenarioinfo.py` & `message-ix-models-2023.5.13/message_ix_models/util/scenarioinfo.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/util/sdmx.py` & `message-ix-models-2023.5.13/message_ix_models/util/sdmx.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models/workflow.py` & `message-ix-models-2023.5.13/message_ix_models/workflow.py`

 * *Files identical despite different names*

### Comparing `message-ix-models-2023.4.2/message_ix_models.egg-info/SOURCES.txt` & `message-ix-models-2023.5.13/message_ix_models.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,15 @@
+.flake8
 .gitattributes
 .gitignore
 .readthedocs.yml
 LICENSE
 README.rst
 conftest.py
 pyproject.toml
-setup.cfg
-setup.py
 .github/codecov.yml
 .github/pull_request_template.md
 .github/workflows/lint.yaml
 .github/workflows/publish.yaml
 .github/workflows/pytest.yaml
 doc/Makefile
 doc/bibliography.rst
@@ -59,15 +58,14 @@
 message_ix_models/workflow.py
 message_ix_models.egg-info/PKG-INFO
 message_ix_models.egg-info/SOURCES.txt
 message_ix_models.egg-info/dependency_links.txt
 message_ix_models.egg-info/entry_points.txt
 message_ix_models.egg-info/requires.txt
 message_ix_models.egg-info/top_level.txt
-message_ix_models.egg-info/zip-safe
 message_ix_models/data/commodity.yaml
 message_ix_models/data/level.yaml
 message_ix_models/data/technology.yaml
 message_ix_models/data/unit.yaml
 message_ix_models/data/cd_links/unit.yaml
 message_ix_models/data/edits/messageix-transport-core.yaml
 message_ix_models/data/edits/messageix-transport-input.yaml
```

