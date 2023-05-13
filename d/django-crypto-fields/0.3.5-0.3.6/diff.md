# Comparing `tmp/django-crypto-fields-0.3.5.tar.gz` & `tmp/django-crypto-fields-0.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-crypto-fields-0.3.5.tar", last modified: Fri Mar 31 13:33:59 2023, max compression
+gzip compressed data, was "django-crypto-fields-0.3.6.tar", last modified: Sat May 13 18:33:36 2023, max compression
```

## Comparing `django-crypto-fields-0.3.5.tar` & `django-crypto-fields-0.3.6.tar`

### file list

```diff
@@ -1,98 +1,98 @@
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.419132 django-crypto-fields-0.3.5/
--rw-r--r--   0 erikvw     (501) staff       (20)      119 2020-03-04 23:22:31.000000 django-crypto-fields-0.3.5/.coveragerc
--rw-r--r--   0 erikvw     (501) staff       (20)      436 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/.editorconfig
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.402270 django-crypto-fields-0.3.5/.github/
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.406662 django-crypto-fields-0.3.5/.github/workflows/
--rw-r--r--   0 erikvw     (501) staff       (20)     1921 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.5/.github/workflows/build.yml
--rw-r--r--   0 erikvw     (501) staff       (20)      989 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/.gitignore
--rw-r--r--   0 erikvw     (501) staff       (20)     1075 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.5/.pre-commit-config.yaml
--rw-r--r--   0 erikvw     (501) staff       (20)      291 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/.yamllint
--rw-r--r--   0 erikvw     (501) staff       (20)       76 2020-03-04 23:22:31.000000 django-crypto-fields-0.3.5/AUTHORS
--rw-r--r--   0 erikvw     (501) staff       (20)      434 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/CHANGES
--rw-r--r--   0 erikvw     (501) staff       (20)    35141 2020-03-04 23:21:45.000000 django-crypto-fields-0.3.5/LICENSE
--rw-r--r--   0 erikvw     (501) staff       (20)       74 2022-06-01 12:56:49.000000 django-crypto-fields-0.3.5/MANIFEST.in
--rw-r--r--   0 erikvw     (501) staff       (20)     6572 2023-03-31 13:33:59.419239 django-crypto-fields-0.3.5/PKG-INFO
--rw-r--r--   0 erikvw     (501) staff       (20)     5663 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/README.rst
--rw-r--r--   0 erikvw     (501) staff       (20)        6 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/VERSION
--rw-r--r--   0 erikvw     (501) staff       (20)      166 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/codecov.yml
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.409728 django-crypto-fields-0.3.5/django_crypto_fields/
--rw-r--r--   0 erikvw     (501) staff       (20)      857 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/__init__.py
--rw-r--r--   0 erikvw     (501) staff       (20)      571 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/admin.py
--rw-r--r--   0 erikvw     (501) staff       (20)      294 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/admin_site.py
--rw-r--r--   0 erikvw     (501) staff       (20)     4209 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/apps.py
--rw-r--r--   0 erikvw     (501) staff       (20)      288 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/constants.py
--rw-r--r--   0 erikvw     (501) staff       (20)     4425 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/cryptor.py
--rw-r--r--   0 erikvw     (501) staff       (20)      445 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/exceptions.py
--rw-r--r--   0 erikvw     (501) staff       (20)    15717 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/field_cryptor.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.412417 django-crypto-fields-0.3.5/django_crypto_fields/fields/
--rw-r--r--   0 erikvw     (501) staff       (20)      648 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/__init__.py
--rw-r--r--   0 erikvw     (501) staff       (20)      275 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/base_aes_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)     5916 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/base_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)      275 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/base_rsa_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)      140 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/encrypted_char_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2109 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/encrypted_decimal_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)      338 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/encrypted_integer_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)      338 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/encrypted_text_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2115 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/firstname_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)      244 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/identity_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)       87 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/fields/lastname_field.py
--rw-r--r--   0 erikvw     (501) staff       (20)     3799 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/key_creator.py
--rw-r--r--   0 erikvw     (501) staff       (20)     3433 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/key_files.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2714 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/key_path.py
--rw-r--r--   0 erikvw     (501) staff       (20)     4278 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/keys.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.412604 django-crypto-fields-0.3.5/django_crypto_fields/management/
--rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/management/__init__.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.412850 django-crypto-fields-0.3.5/django_crypto_fields/management/commands/
--rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/management/commands/__init__.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2782 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/management/commands/convert_aes_cfb2cbc.py
--rw-r--r--   0 erikvw     (501) staff       (20)      161 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/mask_encrypted.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.416028 django-crypto-fields-0.3.5/django_crypto_fields/migrations/
--rw-r--r--   0 erikvw     (501) staff       (20)     3618 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0001_initial.py
--rw-r--r--   0 erikvw     (501) staff       (20)     6261 2022-08-05 14:20:58.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0001_squashed_0011_delete_keyreference.py
--rw-r--r--   0 erikvw     (501) staff       (20)     1949 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0002_auto_20190303_2341.py
--rw-r--r--   0 erikvw     (501) staff       (20)      521 2022-08-05 14:20:58.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0002_crypt_cipher_mode.py
--rw-r--r--   0 erikvw     (501) staff       (20)      489 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0003_alter_crypt_cipher_mode.py
--rw-r--r--   0 erikvw     (501) staff       (20)      717 2021-04-23 11:43:39.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0003_auto_20161124_1835.py
--rw-r--r--   0 erikvw     (501) staff       (20)      700 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0004_auto_20161221_0018.py
--rw-r--r--   0 erikvw     (501) staff       (20)     1972 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0005_auto_20170106_1849.py
--rw-r--r--   0 erikvw     (501) staff       (20)      482 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0006_auto_20170328_0728.py
--rw-r--r--   0 erikvw     (501) staff       (20)     1021 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0007_auto_20170518_1233.py
--rw-r--r--   0 erikvw     (501) staff       (20)      845 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0008_auto_20170624_1905.py
--rw-r--r--   0 erikvw     (501) staff       (20)      645 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0009_auto_20170903_1532.py
--rw-r--r--   0 erikvw     (501) staff       (20)      936 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0010_keyreference.py
--rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/0011_delete_keyreference.py
--rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/migrations/__init__.py
--rw-r--r--   0 erikvw     (501) staff       (20)     1519 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/models.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2331 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/persist_key_path.py
--rw-r--r--   0 erikvw     (501) staff       (20)     2892 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/system_checks.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.416278 django-crypto-fields-0.3.5/django_crypto_fields/templatetags/
--rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/templatetags/__init__.py
--rw-r--r--   0 erikvw     (501) staff       (20)      349 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/templatetags/crypto_tags.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.417311 django-crypto-fields-0.3.5/django_crypto_fields/tests/
--rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/__init__.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.418917 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/
--rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-aes-local.key
--rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-aes-restricted.key
--rw-r--r--   0 erikvw     (501) staff       (20)     1674 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-local-private.pem
--rw-r--r--   0 erikvw     (501) staff       (20)      450 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-local-public.pem
--rw-r--r--   0 erikvw     (501) staff       (20)     1674 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-restricted-private.pem
--rw-r--r--   0 erikvw     (501) staff       (20)      450 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-restricted-public.pem
--rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-salt-local.key
--rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-salt-restricted.key
--rw-r--r--   0 erikvw     (501) staff       (20)      690 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/models.py
--rw-r--r--   0 erikvw     (501) staff       (20)     3919 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/test_cryptor.py
--rw-r--r--   0 erikvw     (501) staff       (20)    11313 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/test_field_cryptor.py
--rw-r--r--   0 erikvw     (501) staff       (20)     5851 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/test_key_creator.py
--rw-r--r--   0 erikvw     (501) staff       (20)     3435 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.5/django_crypto_fields/tests/test_models.py
--rw-r--r--   0 erikvw     (501) staff       (20)      291 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.5/django_crypto_fields/urls.py
--rw-r--r--   0 erikvw     (501) staff       (20)      161 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.5/django_crypto_fields/utils.py
-drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-03-31 13:33:59.410440 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/
--rw-r--r--   0 erikvw     (501) staff       (20)     6572 2023-03-31 13:33:59.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/PKG-INFO
--rw-r--r--   0 erikvw     (501) staff       (20)     3435 2023-03-31 13:33:59.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/SOURCES.txt
--rw-r--r--   0 erikvw     (501) staff       (20)        1 2023-03-31 13:33:59.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/dependency_links.txt
--rw-r--r--   0 erikvw     (501) staff       (20)        1 2020-03-04 23:21:45.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/not-zip-safe
--rw-r--r--   0 erikvw     (501) staff       (20)       94 2023-03-31 13:33:59.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/requires.txt
--rw-r--r--   0 erikvw     (501) staff       (20)       21 2023-03-31 13:33:59.000000 django-crypto-fields-0.3.5/django_crypto_fields.egg-info/top_level.txt
--rw-r--r--   0 erikvw     (501) staff       (20)     1680 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.5/pyproject.toml
--rw-r--r--   0 erikvw     (501) staff       (20)     1163 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.5/runtests.py
--rw-r--r--   0 erikvw     (501) staff       (20)     1325 2023-03-31 13:33:59.419597 django-crypto-fields-0.3.5/setup.cfg
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.929244 django-crypto-fields-0.3.6/
+-rw-r--r--   0 erikvw     (501) staff       (20)      119 2020-03-04 23:22:31.000000 django-crypto-fields-0.3.6/.coveragerc
+-rw-r--r--   0 erikvw     (501) staff       (20)      436 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/.editorconfig
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.910832 django-crypto-fields-0.3.6/.github/
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.915709 django-crypto-fields-0.3.6/.github/workflows/
+-rw-r--r--   0 erikvw     (501) staff       (20)     1921 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.6/.github/workflows/build.yml
+-rw-r--r--   0 erikvw     (501) staff       (20)      989 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/.gitignore
+-rw-r--r--   0 erikvw     (501) staff       (20)     1076 2023-05-13 18:33:29.000000 django-crypto-fields-0.3.6/.pre-commit-config.yaml
+-rw-r--r--   0 erikvw     (501) staff       (20)      291 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/.yamllint
+-rw-r--r--   0 erikvw     (501) staff       (20)       76 2020-03-04 23:22:31.000000 django-crypto-fields-0.3.6/AUTHORS
+-rw-r--r--   0 erikvw     (501) staff       (20)      434 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/CHANGES
+-rw-r--r--   0 erikvw     (501) staff       (20)    35141 2020-03-04 23:21:45.000000 django-crypto-fields-0.3.6/LICENSE
+-rw-r--r--   0 erikvw     (501) staff       (20)       74 2022-06-01 12:56:49.000000 django-crypto-fields-0.3.6/MANIFEST.in
+-rw-r--r--   0 erikvw     (501) staff       (20)     6572 2023-05-13 18:33:36.929359 django-crypto-fields-0.3.6/PKG-INFO
+-rw-r--r--   0 erikvw     (501) staff       (20)     5663 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/README.rst
+-rw-r--r--   0 erikvw     (501) staff       (20)        6 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/VERSION
+-rw-r--r--   0 erikvw     (501) staff       (20)      166 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/codecov.yml
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.919622 django-crypto-fields-0.3.6/django_crypto_fields/
+-rw-r--r--   0 erikvw     (501) staff       (20)      857 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/__init__.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      571 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/admin.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      294 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/admin_site.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     4209 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/apps.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      288 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/constants.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     4425 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/cryptor.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      445 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/exceptions.py
+-rw-r--r--   0 erikvw     (501) staff       (20)    15717 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/field_cryptor.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.922562 django-crypto-fields-0.3.6/django_crypto_fields/fields/
+-rw-r--r--   0 erikvw     (501) staff       (20)      648 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/__init__.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      275 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/base_aes_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     5916 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/base_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      275 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/base_rsa_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      140 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/encrypted_char_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2109 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/encrypted_decimal_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      338 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/encrypted_integer_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      338 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/encrypted_text_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2115 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/firstname_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      244 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/identity_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)       87 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/fields/lastname_field.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     3799 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/key_creator.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     3433 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/key_files.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2714 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/key_path.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     4278 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/keys.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.922727 django-crypto-fields-0.3.6/django_crypto_fields/management/
+-rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/management/__init__.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.922952 django-crypto-fields-0.3.6/django_crypto_fields/management/commands/
+-rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/management/commands/__init__.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2782 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/management/commands/convert_aes_cfb2cbc.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      161 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/mask_encrypted.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.925935 django-crypto-fields-0.3.6/django_crypto_fields/migrations/
+-rw-r--r--   0 erikvw     (501) staff       (20)     3618 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0001_initial.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     6261 2022-08-05 14:20:58.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0001_squashed_0011_delete_keyreference.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     1949 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0002_auto_20190303_2341.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      521 2022-08-05 14:20:58.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0002_crypt_cipher_mode.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      489 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0003_alter_crypt_cipher_mode.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      717 2021-04-23 11:43:39.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0003_auto_20161124_1835.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      700 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0004_auto_20161221_0018.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     1972 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0005_auto_20170106_1849.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      482 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0006_auto_20170328_0728.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     1021 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0007_auto_20170518_1233.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      845 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0008_auto_20170624_1905.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      645 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0009_auto_20170903_1532.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      936 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0010_keyreference.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/0011_delete_keyreference.py
+-rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/migrations/__init__.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     1519 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/models.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2331 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/persist_key_path.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     2892 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/system_checks.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.926267 django-crypto-fields-0.3.6/django_crypto_fields/templatetags/
+-rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/templatetags/__init__.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      349 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/templatetags/crypto_tags.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.927541 django-crypto-fields-0.3.6/django_crypto_fields/tests/
+-rw-r--r--   0 erikvw     (501) staff       (20)        0 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/__init__.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.929079 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/
+-rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-aes-local.key
+-rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-aes-restricted.key
+-rw-r--r--   0 erikvw     (501) staff       (20)     1674 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-local-private.pem
+-rw-r--r--   0 erikvw     (501) staff       (20)      450 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-local-public.pem
+-rw-r--r--   0 erikvw     (501) staff       (20)     1674 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-restricted-private.pem
+-rw-r--r--   0 erikvw     (501) staff       (20)      450 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-restricted-public.pem
+-rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-salt-local.key
+-rw-r--r--   0 erikvw     (501) staff       (20)      256 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-salt-restricted.key
+-rw-r--r--   0 erikvw     (501) staff       (20)      690 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/models.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     3919 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/test_cryptor.py
+-rw-r--r--   0 erikvw     (501) staff       (20)    11313 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/test_field_cryptor.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     5851 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/test_key_creator.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     3435 2022-08-10 01:05:08.000000 django-crypto-fields-0.3.6/django_crypto_fields/tests/test_models.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      291 2020-03-04 23:22:41.000000 django-crypto-fields-0.3.6/django_crypto_fields/urls.py
+-rw-r--r--   0 erikvw     (501) staff       (20)      161 2023-03-31 13:33:51.000000 django-crypto-fields-0.3.6/django_crypto_fields/utils.py
+drwxr-xr-x   0 erikvw     (501) staff       (20)        0 2023-05-13 18:33:36.920801 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/
+-rw-r--r--   0 erikvw     (501) staff       (20)     6572 2023-05-13 18:33:36.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/PKG-INFO
+-rw-r--r--   0 erikvw     (501) staff       (20)     3435 2023-05-13 18:33:36.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/SOURCES.txt
+-rw-r--r--   0 erikvw     (501) staff       (20)        1 2023-05-13 18:33:36.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/dependency_links.txt
+-rw-r--r--   0 erikvw     (501) staff       (20)        1 2020-03-04 23:21:45.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/not-zip-safe
+-rw-r--r--   0 erikvw     (501) staff       (20)       79 2023-05-13 18:33:36.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/requires.txt
+-rw-r--r--   0 erikvw     (501) staff       (20)       21 2023-05-13 18:33:36.000000 django-crypto-fields-0.3.6/django_crypto_fields.egg-info/top_level.txt
+-rw-r--r--   0 erikvw     (501) staff       (20)     1723 2023-05-13 18:33:29.000000 django-crypto-fields-0.3.6/pyproject.toml
+-rw-r--r--   0 erikvw     (501) staff       (20)     1163 2021-02-05 20:53:19.000000 django-crypto-fields-0.3.6/runtests.py
+-rw-r--r--   0 erikvw     (501) staff       (20)     1310 2023-05-13 18:33:36.929778 django-crypto-fields-0.3.6/setup.cfg
```

### Comparing `django-crypto-fields-0.3.5/.github/workflows/build.yml` & `django-crypto-fields-0.3.6/.github/workflows/build.yml`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/.gitignore` & `django-crypto-fields-0.3.6/.gitignore`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/.pre-commit-config.yaml` & `django-crypto-fields-0.3.6/.pre-commit-config.yaml`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 ---
 exclude: tests/etc/user-*
+
 repos:
   - repo: https://github.com/PyCQA/bandit
-    rev: 1.7.4
+    rev: 1.7.5
     hooks:
       - id: bandit
         args:
           - "-x *test*.py"
 
   - repo: https://github.com/psf/black
     rev: 23.1.0
@@ -37,12 +38,12 @@
       - id: check-docstring-first
       - id: check-executables-have-shebangs
       - id: check-merge-conflict
       - id: debug-statements
       - id: detect-private-key
 
   - repo: https://github.com/adrienverge/yamllint
-    rev: v1.29.0
+    rev: v1.30.0
     hooks:
       - id: yamllint
         args:
           - "--strict"
```

### Comparing `django-crypto-fields-0.3.5/LICENSE` & `django-crypto-fields-0.3.6/LICENSE`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/PKG-INFO` & `django-crypto-fields-0.3.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-crypto-fields
-Version: 0.3.5
+Version: 0.3.6
 Summary: Add encrypted field classes and more to your Django models.
 Home-page: http://github.com/erikvw/django-crypto-fields
 Author: Erik van Widenfelt
 Author-email: ew2789@gmail.com
 License: GPL license, see LICENSE
 Keywords: django Edc fields encryption security
 Classifier: Environment :: Web Environment
```

### Comparing `django-crypto-fields-0.3.5/README.rst` & `django-crypto-fields-0.3.6/README.rst`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/__init__.py` & `django-crypto-fields-0.3.6/django_crypto_fields/__init__.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/admin.py` & `django-crypto-fields-0.3.6/django_crypto_fields/admin.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/apps.py` & `django-crypto-fields-0.3.6/django_crypto_fields/apps.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/cryptor.py` & `django-crypto-fields-0.3.6/django_crypto_fields/cryptor.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/field_cryptor.py` & `django-crypto-fields-0.3.6/django_crypto_fields/field_cryptor.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/fields/__init__.py` & `django-crypto-fields-0.3.6/django_crypto_fields/fields/__init__.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/fields/base_field.py` & `django-crypto-fields-0.3.6/django_crypto_fields/fields/base_field.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/fields/encrypted_decimal_field.py` & `django-crypto-fields-0.3.6/django_crypto_fields/fields/encrypted_decimal_field.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/fields/firstname_field.py` & `django-crypto-fields-0.3.6/django_crypto_fields/fields/firstname_field.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/key_creator.py` & `django-crypto-fields-0.3.6/django_crypto_fields/key_creator.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/key_files.py` & `django-crypto-fields-0.3.6/django_crypto_fields/key_files.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/key_path.py` & `django-crypto-fields-0.3.6/django_crypto_fields/key_path.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/keys.py` & `django-crypto-fields-0.3.6/django_crypto_fields/keys.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/management/commands/convert_aes_cfb2cbc.py` & `django-crypto-fields-0.3.6/django_crypto_fields/management/commands/convert_aes_cfb2cbc.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0001_initial.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0001_squashed_0011_delete_keyreference.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0001_squashed_0011_delete_keyreference.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0002_auto_20190303_2341.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0002_auto_20190303_2341.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0002_crypt_cipher_mode.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0002_crypt_cipher_mode.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0003_auto_20161124_1835.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0003_auto_20161124_1835.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0004_auto_20161221_0018.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0004_auto_20161221_0018.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0005_auto_20170106_1849.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0005_auto_20170106_1849.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0007_auto_20170518_1233.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0007_auto_20170518_1233.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0008_auto_20170624_1905.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0008_auto_20170624_1905.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0009_auto_20170903_1532.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0009_auto_20170903_1532.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/migrations/0010_keyreference.py` & `django-crypto-fields-0.3.6/django_crypto_fields/migrations/0010_keyreference.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/models.py` & `django-crypto-fields-0.3.6/django_crypto_fields/models.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/persist_key_path.py` & `django-crypto-fields-0.3.6/django_crypto_fields/persist_key_path.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/system_checks.py` & `django-crypto-fields-0.3.6/django_crypto_fields/system_checks.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-local-private.pem` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-local-private.pem`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/etc/user-rsa-restricted-private.pem` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/etc/user-rsa-restricted-private.pem`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/models.py` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/models.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/test_cryptor.py` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/test_cryptor.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/test_field_cryptor.py` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/test_field_cryptor.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/test_key_creator.py` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/test_key_creator.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields/tests/test_models.py` & `django-crypto-fields-0.3.6/django_crypto_fields/tests/test_models.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields.egg-info/PKG-INFO` & `django-crypto-fields-0.3.6/django_crypto_fields.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-crypto-fields
-Version: 0.3.5
+Version: 0.3.6
 Summary: Add encrypted field classes and more to your Django models.
 Home-page: http://github.com/erikvw/django-crypto-fields
 Author: Erik van Widenfelt
 Author-email: ew2789@gmail.com
 License: GPL license, see LICENSE
 Keywords: django Edc fields encryption security
 Classifier: Environment :: Web Environment
```

### Comparing `django-crypto-fields-0.3.5/django_crypto_fields.egg-info/SOURCES.txt` & `django-crypto-fields-0.3.6/django_crypto_fields.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/pyproject.toml` & `django-crypto-fields-0.3.6/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -23,47 +23,49 @@
 [tool.coverage.paths]
 source = ["django_crypto_fields"]
 
 [tool.coverage.report]
 show_missing = true
 skip_covered = true
 omit = ["requirements.txt"]
+exclude_lines = [
+  "pragma: no cover",
+  "if TYPE_CHECKING:",
+]
 
 [tool.tox]
 legacy_tox_ini = """
 [tox]
 envlist =
-    py{310,311}-dj{40,41,dev},
+    py{310,311}-dj{41,dev},
     lint
 
 isolated_build = true
 
 [gh-actions]
 python =
     3.10: py310
-    3.11: py311
+    3.11: py311, lint
 
 [gh-actions:env]
 DJANGO =
-    4.0: dj40 lint
-    4.1: dj41
+    4.1: dj41, lint
     dev: djdev
 
 [testenv]
 deps =
     -r https://raw.githubusercontent.com/clinicedc/edc/develop/requirements.tests/tox.txt
     -r https://raw.githubusercontent.com/clinicedc/edc/develop/requirements.tests/test_utils.txt
     -r https://raw.githubusercontent.com/clinicedc/edc/develop/requirements.tests/edc.txt
     -r https://raw.githubusercontent.com/clinicedc/edc/develop/requirements.tests/third_party_dev.txt
-    dj40: Django>=4.0,<4.1
     dj41: Django>=4.1,<4.2
     djdev: https://github.com/django/django/tarball/main
 
 commands =
-    pip install -U pip
+    pip install -U pip coverage[toml]
     pip --version
     pip freeze
     coverage run -a runtests.py
     coverage report
 
 [testenv:lint]
 deps = -r https://raw.githubusercontent.com/clinicedc/edc/develop/requirements.tests/lint.txt
```

### Comparing `django-crypto-fields-0.3.5/runtests.py` & `django-crypto-fields-0.3.6/runtests.py`

 * *Files identical despite different names*

### Comparing `django-crypto-fields-0.3.5/setup.cfg` & `django-crypto-fields-0.3.6/setup.cfg`

 * *Files 6% similar despite different names*

```diff
@@ -25,16 +25,16 @@
 python_requires = >=3.10
 zip_safe = False
 include_package_data = True
 packages = find:
 install_requires = 
 	pycryptodomex
 	django-audit-fields
-	edc-utils>=0.3.19
-	edc-model-fields>=0.3.6
+	edc-utils
+	edc-model-fields
 	django-extensions
 
 [options.packages.find]
 exclude = 
 	examples*
 	tools*
 	docs*
```

