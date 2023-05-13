# Comparing `tmp/pii-extract-plg-regex-0.4.0.tar.gz` & `tmp/pii-extract-plg-regex-0.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pii-extract-plg-regex-0.4.0.tar", last modified: Wed May 10 18:09:59 2023, max compression
+gzip compressed data, was "pii-extract-plg-regex-0.4.1.tar", last modified: Fri May 12 20:58:49 2023, max compression
```

## Comparing `pii-extract-plg-regex-0.4.0.tar` & `pii-extract-plg-regex-0.4.1.tar`

### file list

```diff
@@ -1,94 +1,94 @@
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-plg-regex-0.4.0/LICENSE
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/MANIFEST.in
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2317 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2562 2023-05-10 16:13:12.000000 pii-extract-plg-regex-0.4.0/README.md
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      138 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/requirements.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/setup.cfg
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2668 2023-03-17 19:24:22.000000 pii-extract-plg-regex-0.4.0/setup.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      268 2023-03-20 21:11:54.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/defs.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1251 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/bitcoin_address.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2284 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/credit_card.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1511 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/email.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      492 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/ip_address.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/any/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/any/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      511 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/any/age.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1127 2023-03-17 19:24:22.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/any/international_phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1074 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/abn.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1616 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/phone_number.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      759 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/tfn.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1699 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/phone_number.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1152 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/social_insurance_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      744 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/aadhaar.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1911 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1515 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/phone_number.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      460 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/social_security_number.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1661 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/zipcode.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/any/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/any/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      762 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/any/international_phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1277 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/bank_account.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1859 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/govid.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2046 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1163 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/curp.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1705 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/ca/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/ca/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      391 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/ca/social_insurance_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2692 2023-02-20 12:24:29.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/govid.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1862 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/phone_number.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/br/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/br/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      707 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/br/cpf.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/pt/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/pt/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1778 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/pt/govid.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/ro/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/ro/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1052 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/ro/govid.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.189294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      928 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/govid.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1033 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/misc.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1557 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/plugin_loader.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:59.185294 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2317 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3220 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/SOURCES.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/dependency_links.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      105 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/entry_points.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      154 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/requires.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       22 2023-05-10 18:09:59.000000 pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/top_level.txt
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-plg-regex-0.4.1/LICENSE
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/MANIFEST.in
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2317 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2562 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/README.md
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      138 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/requirements.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/setup.cfg
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2668 2023-03-17 19:24:22.000000 pii-extract-plg-regex-0.4.1/setup.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      268 2023-03-20 21:11:54.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/defs.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1251 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/bitcoin_address.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2284 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/credit_card.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1511 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/email.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      492 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/ip_address.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/any/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/any/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      511 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/any/age.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1127 2023-03-17 19:24:22.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/any/international_phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1074 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/abn.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1616 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/phone_number.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      759 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/tfn.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1699 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/phone_number.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1152 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/social_insurance_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      744 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/aadhaar.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1903 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1515 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/phone_number.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      460 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/social_security_number.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1661 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/zipcode.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/any/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/any/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1065 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/any/international_phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1277 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/bank_account.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1859 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/govid.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2046 2023-05-11 11:56:25.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1163 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/curp.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1705 2023-05-10 16:13:30.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/ca/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/ca/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      391 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/ca/social_insurance_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2692 2023-02-20 12:24:29.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/govid.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1824 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/phone_number.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/br/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/br/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      685 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/br/cpf.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/pt/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/pt/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1778 2023-05-11 12:22:43.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/pt/govid.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/ro/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/ro/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1052 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/ro/govid.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.208941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      928 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/govid.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1033 2023-01-23 19:55:40.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/misc.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1897 2023-05-12 20:46:58.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/plugin_loader.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:49.204941 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2317 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3220 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/SOURCES.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/dependency_links.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      105 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/entry_points.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      154 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/requires.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       22 2023-05-12 20:58:49.000000 pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/top_level.txt
```

### Comparing `pii-extract-plg-regex-0.4.0/LICENSE` & `pii-extract-plg-regex-0.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/PKG-INFO` & `pii-extract-plg-regex-0.4.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-plg-regex
-Version: 0.4.0
+Version: 0.4.1
 Summary: Regex modules for the extraction of PII from text chunks
 Home-page: https://github.com/piisa/pii-extract-plg-regex
-Download-URL: https://github.com/piisa/pii-extract-plg-regex/tarball/v0.4.0
+Download-URL: https://github.com/piisa/pii-extract-plg-regex/tarball/v0.4.1
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-extract-plg-regex-0.4.0/README.md` & `pii-extract-plg-regex-0.4.1/README.md`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/setup.py` & `pii-extract-plg-regex-0.4.1/setup.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/bitcoin_address.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/bitcoin_address.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/credit_card.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/credit_card.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/any/email.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/any/email.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/any/international_phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/any/international_phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/abn.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/abn.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/au/tfn.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/au/tfn.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/ca/social_insurance_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/ca/social_insurance_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/aadhaar.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/aadhaar.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/in_/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/in_/phone_number.py`

 * *Files 2% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 
 # ----------------------------------------------------------------------------
 
 # compiled regex
 _REGEX = None
 
 
-def Indian_phone_number(text: str) -> Iterable[Tuple[str, int]]:
+def IN_phone_number(text: str) -> Iterable[Tuple[str, int]]:
     """
     Indian Phone Numbers
     """
     # Compile regex if needed
     global _REGEX
     if _REGEX is None:
         _REGEX = re.compile(PHONE_REGEX, flags=re.X)
@@ -61,15 +61,15 @@
             yield item_value, match.start()
 
 # ---------------------------------------------------------------------
 
 
 PII_TASKS = {
     "class": "callable",
-    "task": Indian_phone_number,
+    "task": IN_phone_number,
     "pii": {
         "type": PiiEnum.PHONE_NUMBER,
         "method": "soft-regex,context",
         "context": {
             "type": "regex",
             "value": CONTEXT_REGEX,
             "width": [64, 64]
```

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/en/us/zipcode.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/en/us/zipcode.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/bank_account.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/bank_account.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/govid.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/govid.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/es/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/es/phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/curp.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/curp.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/es/mx/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/es/mx/phone_number.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/govid.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/govid.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/fr/fr/phone_number.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/fr/fr/phone_number.py`

 * *Files 5% similar despite different names*

```diff
@@ -55,12 +55,11 @@
 # ---------------------------------------------------------------------
 
 PII_TASKS = {
     "class": "callable",
     "task": FR_phone_number,
     "pii": {
         "type": PiiEnum.PHONE_NUMBER,
-        "subtype": "FR phone number",
         "method": "soft-regex,context",
         "context": {"type": "regex", "value": CONTEXT_REGEX, "width": [64, 64]},
     },
 }
```

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/br/cpf.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/br/cpf.py`

 * *Files 15% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 
 
 _CPF_REGEX = re.compile(r"\b \d{3} \. \d{3} \. \d{3} - \d{2} \b", flags=re.X)
 
 
 def cadastro_pessoa_fisica(doc: str) -> Iterable[str]:
     """
-    Brazilian número de inscrição no Cadastro de Pessoas Físicas (detect and validate)
+    Brazilian número de inscrição no Cadastro de Pessoas Físicas
     """
     for candidate in _CPF_REGEX.findall(doc):
         if cpf.is_valid(candidate):
             yield candidate
 
 
 PII_TASKS = [(PiiEnum.GOV_ID, cadastro_pessoa_fisica,
```

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/pt/pt/govid.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/pt/pt/govid.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/ro/ro/govid.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/ro/ro/govid.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/govid.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/govid.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex/modules/zh/cn/misc.py` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex/modules/zh/cn/misc.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/PKG-INFO` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-plg-regex
-Version: 0.4.0
+Version: 0.4.1
 Summary: Regex modules for the extraction of PII from text chunks
 Home-page: https://github.com/piisa/pii-extract-plg-regex
-Download-URL: https://github.com/piisa/pii-extract-plg-regex/tarball/v0.4.0
+Download-URL: https://github.com/piisa/pii-extract-plg-regex/tarball/v0.4.1
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-extract-plg-regex-0.4.0/src/pii_extract_plg_regex.egg-info/SOURCES.txt` & `pii-extract-plg-regex-0.4.1/src/pii_extract_plg_regex.egg-info/SOURCES.txt`

 * *Files identical despite different names*

