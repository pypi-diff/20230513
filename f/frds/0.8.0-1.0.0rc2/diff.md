# Comparing `tmp/frds-0.8.0.tar.gz` & `tmp/frds-1.0.0rc2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "frds-0.8.0.tar", last modified: Tue Apr 19 06:39:42 2022, max compression
+gzip compressed data, last modified: Sun Feb  2 00:00:00 2020, max compression
```

## Comparing `frds-0.8.0.tar` & `frds-1.0.0rc2.tar`

### file list

```diff
@@ -1,90 +1,38 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.200750 frds-0.8.0/
--rw-r--r--   0 runner    (1001) docker     (121)     1066 2022-04-19 06:39:25.000000 frds-0.8.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)     8560 2022-04-19 06:39:42.200750 frds-0.8.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     6649 2022-04-19 06:39:25.000000 frds-0.8.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.188750 frds-0.8.0/frds/
--rw-r--r--   0 runner    (1001) docker     (121)      372 2022-04-19 06:39:25.000000 frds-0.8.0/frds/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/algorithms/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/algorithms/bunching/
--rw-r--r--   0 runner    (1001) docker     (121)    13044 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/bunching/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/algorithms/isolation_forest/
--rw-r--r--   0 runner    (1001) docker     (121)     1770 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/isolation_forest/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/algorithms/isolation_forest/src/
--rw-r--r--   0 runner    (1001) docker     (121)     8196 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/isolation_forest/src/IsolationForest.cpp
--rw-r--r--   0 runner    (1001) docker     (121)     2354 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/isolation_forest/src/IsolationForest.hpp
--rw-r--r--   0 runner    (1001) docker     (121)     2571 2022-04-19 06:39:25.000000 frds-0.8.0/frds/algorithms/isolation_forest/src/iforest_module.cpp
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/data/
--rw-r--r--   0 runner    (1001) docker     (121)      252 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/data/wrds/
--rw-r--r--   0 runner    (1001) docker     (121)      601 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/data/wrds/comp/
--rw-r--r--   0 runner    (1001) docker     (121)       91 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/comp/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)   153366 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/comp/funda.py
--rw-r--r--   0 runner    (1001) docker     (121)   110577 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/comp/fundq.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/data/wrds/execucomp/
--rw-r--r--   0 runner    (1001) docker     (121)       29 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/execucomp/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    19318 2022-04-19 06:39:25.000000 frds-0.8.0/frds/data/wrds/execucomp/anncomp.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.188750 frds-0.8.0/frds/io/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/io/fred/
--rw-r--r--   0 runner    (1001) docker     (121)      886 2022-04-19 06:39:25.000000 frds-0.8.0/frds/io/fred/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds/io/wrds/
--rw-r--r--   0 runner    (1001) docker     (121)     2049 2022-04-19 06:39:25.000000 frds-0.8.0/frds/io/wrds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    13920 2022-04-19 06:39:25.000000 frds-0.8.0/frds/io/wrds/connection.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.196750 frds-0.8.0/frds/measures/
--rw-r--r--   0 runner    (1001) docker     (121)      128 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      265 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/bank.py
--rw-r--r--   0 runner    (1001) docker     (121)     9006 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/corporate.py
--rw-r--r--   0 runner    (1001) docker     (121)     3501 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_absorption_ratio.py
--rw-r--r--   0 runner    (1001) docker     (121)     3165 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_anomaly_score.py
--rw-r--r--   0 runner    (1001) docker     (121)     2578 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_bank_z_score.py
--rw-r--r--   0 runner    (1001) docker     (121)     4194 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_cca.py
--rw-r--r--   0 runner    (1001) docker     (121)     6513 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_dip.py
--rw-r--r--   0 runner    (1001) docker     (121)     1709 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_hhi_index.py
--rw-r--r--   0 runner    (1001) docker     (121)     4106 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_kyle_lambda.py
--rw-r--r--   0 runner    (1001) docker     (121)     2489 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_mes.py
--rw-r--r--   0 runner    (1001) docker     (121)     5395 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/func_ses.py
--rw-r--r--   0 runner    (1001) docker     (121)      125 2022-04-19 06:39:25.000000 frds-0.8.0/frds/measures/general.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.196750 frds-0.8.0/frds/mktstructure/
--rw-r--r--   0 runner    (1001) docker     (121)      267 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1190 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/cmd_classify.py
--rw-r--r--   0 runner    (1001) docker     (121)     1242 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/cmd_clean.py
--rw-r--r--   0 runner    (1001) docker     (121)     1954 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/cmd_compute.py
--rw-r--r--   0 runner    (1001) docker     (121)     1193 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/cmd_download.py
--rw-r--r--   0 runner    (1001) docker     (121)     6923 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/main.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.196750 frds-0.8.0/frds/mktstructure/measures/
--rw-r--r--   0 runner    (1001) docker     (121)       77 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      557 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/bidask_spread.py
--rw-r--r--   0 runner    (1001) docker     (121)     1170 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/effective_spread.py
--rw-r--r--   0 runner    (1001) docker     (121)      287 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (121)     2097 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/permanent_price_impact.py
--rw-r--r--   0 runner    (1001) docker     (121)     1533 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/price_impact.py
--rw-r--r--   0 runner    (1001) docker     (121)     1598 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/measures/realized_spread.py
--rw-r--r--   0 runner    (1001) docker     (121)     2234 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/request_templates.py
--rw-r--r--   0 runner    (1001) docker     (121)     4998 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/trth.py
--rw-r--r--   0 runner    (1001) docker     (121)    13556 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/trth_parser.c
--rw-r--r--   0 runner    (1001) docker     (121)     6041 2022-04-19 06:39:25.000000 frds-0.8.0/frds/mktstructure/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.192751 frds-0.8.0/frds.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     8560 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2125 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       67 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)       48 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       33 2022-04-19 06:39:42.000000 frds-0.8.0/frds.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-04-19 06:39:42.200750 frds-0.8.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     2406 2022-04-19 06:39:25.000000 frds-0.8.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.196750 frds-0.8.0/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:25.000000 frds-0.8.0/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.196750 frds-0.8.0/tests/algorithms/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:25.000000 frds-0.8.0/tests/algorithms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1720 2022-04-19 06:39:25.000000 frds-0.8.0/tests/algorithms/test_isolation_forest.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.200750 frds-0.8.0/tests/data/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:25.000000 frds-0.8.0/tests/data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      917 2022-04-19 06:39:25.000000 frds-0.8.0/tests/data/test_wrds_comp_anncomp.py
--rw-r--r--   0 runner    (1001) docker     (121)      884 2022-04-19 06:39:25.000000 frds-0.8.0/tests/data/test_wrds_comp_funda.py
--rw-r--r--   0 runner    (1001) docker     (121)      884 2022-04-19 06:39:25.000000 frds-0.8.0/tests/data/test_wrds_comp_fundq.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:42.200750 frds-0.8.0/tests/measures/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-04-19 06:39:25.000000 frds-0.8.0/tests/measures/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     6786 2022-04-19 06:39:25.000000 frds-0.8.0/tests/measures/test_bank.py
--rw-r--r--   0 runner    (1001) docker     (121)     2414 2022-04-19 06:39:25.000000 frds-0.8.0/tests/measures/test_corporate.py
--rw-r--r--   0 runner    (1001) docker     (121)     1059 2022-04-19 06:39:25.000000 frds-0.8.0/tests/measures/test_general.py
+-rw-r--r--   0        0        0      310 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.pylintrc
+-rw-r--r--   0        0        0     3399 2020-02-02 00:00:00.000000 frds-1.0.0rc2/mkdocs.yml
+-rw-r--r--   0        0        0       64 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/FUNDING.yml
+-rw-r--r--   0        0        0      594 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      857 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/build-and-deploy-docs.yml
+-rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/publish-to-test-pypi.yml
+-rw-r--r--   0        0        0      606 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/test.yml
+-rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/CNAME
+-rw-r--r--   0        0        0     3952 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/index.md
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures.md
+-rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_icon.png
+-rw-r--r--   0        0        0    58143 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_icon_white.png
+-rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_logo.png
+-rw-r--r--   0        0        0     2310 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/absorption_ratio.md
+-rw-r--r--   0        0        0     1280 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/contingent_claim_analysis.md
+-rw-r--r--   0        0        0     2166 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/distress_insurance_premium.md
+-rw-r--r--   0        0        0     1521 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/marginal_expected_shortfall.md
+-rw-r--r--   0        0        0     3743 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/systemic_expected_shortfall.md
+-rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.0rc2/images/frds_icon.png
+-rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.0rc2/images/frds_logo.png
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/__init__.py
+-rw-r--r--   0        0        0     1412 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/absorption_ratio.py
+-rw-r--r--   0        0        0     3102 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/contingent_claims_analysis.py
+-rw-r--r--   0        0        0     4538 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/distress_insurance_premium.py
+-rw-r--r--   0        0        0     1231 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/marginal_expected_shortfall.py
+-rw-r--r--   0        0        0     1809 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/systemic_expected_shortfall.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/__init__.py
+-rw-r--r--   0        0        0     2367 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_absorption_ratio.py
+-rw-r--r--   0        0        0     1036 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_distress_insurance_premium.py
+-rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_marginal_expected_shortfall.py
+-rw-r--r--   0        0        0      789 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_systemic_expected_shortfall.py
+-rw-r--r--   0        0        0     1819 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.gitignore
+-rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 frds-1.0.0rc2/LICENSE
+-rw-r--r--   0        0        0     2958 2020-02-02 00:00:00.000000 frds-1.0.0rc2/README.md
+-rw-r--r--   0        0        0      916 2020-02-02 00:00:00.000000 frds-1.0.0rc2/pyproject.toml
+-rw-r--r--   0        0        0     3846 2020-02-02 00:00:00.000000 frds-1.0.0rc2/PKG-INFO
```

### Comparing `frds-0.8.0/LICENSE` & `frds-1.0.0rc2/LICENSE`

 * *Files identical despite different names*

