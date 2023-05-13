# Comparing `tmp/jaseci_serv-1.4.0.8.tar.gz` & `tmp/jaseci_serv-1.4.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jaseci_serv-1.4.0.8.tar", last modified: Wed Feb  8 14:13:28 2023, max compression
+gzip compressed data, was "jaseci_serv-1.4.0.9.tar", last modified: Tue Feb 14 17:26:34 2023, max compression
```

## Comparing `jaseci_serv-1.4.0.8.tar` & `jaseci_serv-1.4.0.9.tar`

### file list

```diff
@@ -1,140 +1,128 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      178 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.377869 jaseci_serv-1.4.0.8/jaseci_serv/
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      394 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/asgi.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.377869 jaseci_serv-1.4.0.8/jaseci_serv/base/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/admin.py
--rw-r--r--   0 runner    (1001) docker     (123)       98 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)      462 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/jsorc.py
--rw-r--r--   0 runner    (1001) docker     (123)     9317 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/jsorc_loadtest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.377869 jaseci_serv-1.4.0.8/jaseci_serv/base/management/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/management/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.377869 jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      879 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/createdb.py
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/dropdb.py
--rw-r--r--   0 runner    (1001) docker     (123)      678 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/wait_for_db.py
--rw-r--r--   0 runner    (1001) docker     (123)     8040 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.381869 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3569 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/aitest_ai_models.py
--rw-r--r--   0 runner    (1001) docker     (123)      859 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/mock_redis.py
--rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_admin.py
--rw-r--r--   0 runner    (1001) docker     (123)     1034 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_commands.py
--rw-r--r--   0 runner    (1001) docker     (123)     3788 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_models.py
--rw-r--r--   0 runner    (1001) docker     (123)    11675 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_orm_hooks.py
--rw-r--r--   0 runner    (1001) docker     (123)     2685 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_orm_hooks_cfg.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.381869 jaseci_serv-1.4.0.8/jaseci_serv/hook/
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/hook/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5868 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/hook/orm.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.381869 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2747 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/api.py
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/apps.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.381869 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      266 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/general.jac
--rw-r--r--   0 runner    (1001) docker     (123)      900 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/infer.py
--rw-r--r--   0 runner    (1001) docker     (123)    14915 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/ll.jac
--rw-r--r--   0 runner    (1001) docker     (123)    21775 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/ll_wall.jac
--rw-r--r--   0 runner    (1001) docker     (123)      407 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/public.jac
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/public_updated.jac
--rw-r--r--   0 runner    (1001) docker     (123)     4955 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_admin_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    69705 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1741 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_general.py
--rw-r--r--   0 runner    (1001) docker     (123)    11101 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_ll.py
--rw-r--r--   0 runner    (1001) docker     (123)     4442 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_ll_wall.py
--rw-r--r--   0 runner    (1001) docker     (123)     6828 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_pub_walker.py
--rw-r--r--   0 runner    (1001) docker     (123)      808 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/try-syntax.jac
--rw-r--r--   0 runner    (1001) docker     (123)      630 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/various.jac
--rw-r--r--   0 runner    (1001) docker     (123)     6210 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/zsb.jac
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     8977 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jac_api/views.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/
--rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/admin.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      103 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)      882 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/config.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2286 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/models.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/permissions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4207 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/serializers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5269 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/tests/test_social_auth.py
--rw-r--r--   0 runner    (1001) docker     (123)     1020 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     6864 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3833 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/views.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/
--rw-r--r--   0 runner    (1001) docker     (123)       94 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/actions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/actions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11938 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/actions/stripe.py
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/admin.py
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     6076 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/stripe.jac
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2444 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/tests/test_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    14052 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/tests/test_stripe_jac.py
--rw-r--r--   0 runner    (1001) docker     (123)      161 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     1686 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3210 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/jsx_stripe/views.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/apps.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3977 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/tests/test_obj_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      313 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     2717 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/obj_api/views.py
--rw-r--r--   0 runner    (1001) docker     (123)     6085 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/settings.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/svc/
--rw-r--r--   0 runner    (1001) docker     (123)      412 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/svc/elastic/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/elastic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/elastic/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      540 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/elastic/elastic.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/
--rw-r--r--   0 runner    (1001) docker     (123)      122 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4062 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/mail.py
--rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/meta.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.385869 jaseci_serv-1.4.0.8/jaseci_serv/svc/prometheus/
--rwxr-xr-x   0 runner    (1001) docker     (123)       82 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/prometheus/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      169 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/prometheus/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      219 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/prometheus/prometheus.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/jaseci_serv/svc/redis/
--rw-r--r--   0 runner    (1001) docker     (123)       72 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/redis/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      204 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/redis/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      206 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/redis/redis.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/jaseci_serv/svc/task/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/task/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/task/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      365 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/svc/task/task.py
--rw-r--r--   0 runner    (1001) docker     (123)     1806 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/urls.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/jaseci_serv/user_api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       99 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)     3384 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/serializers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/jaseci_serv/user_api/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15768 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/tests/test_user_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      776 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     6511 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/user_api/views.py
--rw-r--r--   0 runner    (1001) docker     (123)      394 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jaseci_serv/wsgi.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:28.377869 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      178 2023-02-08 14:13:28.000000 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3797 2023-02-08 14:13:28.000000 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-08 14:13:28.000000 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      372 2023-02-08 14:13:28.000000 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-02-08 14:13:28.000000 jaseci_serv-1.4.0.8/jaseci_serv.egg-info/top_level.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)      628 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/jsserv
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-08 14:13:28.389869 jaseci_serv-1.4.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-02-08 14:13:11.000000 jaseci_serv-1.4.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.855676 jaseci_serv-1.4.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      178 2023-02-14 17:26:34.855676 jaseci_serv-1.4.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.835675 jaseci_serv-1.4.0.9/jaseci_serv/
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      394 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/asgi.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.839675 jaseci_serv-1.4.0.9/jaseci_serv/base/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)       98 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)      462 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/jsorc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9317 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/jsorc_loadtest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.839675 jaseci_serv-1.4.0.9/jaseci_serv/base/management/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/management/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.839675 jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      879 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/createdb.py
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/dropdb.py
+-rw-r--r--   0 runner    (1001) docker     (123)      678 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/wait_for_db.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8257 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.839675 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3569 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/aitest_ai_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      859 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/mock_redis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1034 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3788 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11675 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_orm_hooks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2685 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_orm_hooks_cfg.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.839675 jaseci_serv-1.4.0.9/jaseci_serv/hook/
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/hook/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5868 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/hook/orm.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.843675 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2747 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/apps.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.843675 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      266 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/general.jac
+-rw-r--r--   0 runner    (1001) docker     (123)      900 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/infer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14915 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/ll.jac
+-rw-r--r--   0 runner    (1001) docker     (123)    21775 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/ll_wall.jac
+-rw-r--r--   0 runner    (1001) docker     (123)      407 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/public.jac
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/public_updated.jac
+-rw-r--r--   0 runner    (1001) docker     (123)     4955 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_admin_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    70873 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1741 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_general.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11101 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_ll.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4442 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_ll_wall.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6828 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_pub_walker.py
+-rw-r--r--   0 runner    (1001) docker     (123)      808 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/try-syntax.jac
+-rw-r--r--   0 runner    (1001) docker     (123)      630 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/various.jac
+-rw-r--r--   0 runner    (1001) docker     (123)     6210 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/zsb.jac
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9104 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jac_api/views.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.847675 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/
+-rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/admin.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      103 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)      882 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/config.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2286 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/permissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4207 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/serializers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.847675 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5269 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/tests/test_social_auth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1020 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6864 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3833 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/views.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.847675 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/apps.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.847675 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3977 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/tests/test_obj_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      313 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2717 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/obj_api/views.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5988 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/settings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.847675 jaseci_serv-1.4.0.9/jaseci_serv/svc/
+-rw-r--r--   0 runner    (1001) docker     (123)      469 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/elastic/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/elastic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/elastic/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      540 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/elastic/elastic.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4062 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/mail.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1498 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/meta.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/prometheus/
+-rwxr-xr-x   0 runner    (1001) docker     (123)       82 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/prometheus/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/prometheus/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/prometheus/prometheus.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/redis/
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/redis/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      204 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/redis/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      206 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/redis/redis.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/stripe/
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/stripe/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/stripe/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      549 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/stripe/stripe.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.851675 jaseci_serv-1.4.0.9/jaseci_serv/svc/task/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/task/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/task/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      365 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/svc/task/task.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1736 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/urls.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.855676 jaseci_serv-1.4.0.9/jaseci_serv/user_api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       99 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3384 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/serializers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.855676 jaseci_serv-1.4.0.9/jaseci_serv/user_api/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15768 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/tests/test_user_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      776 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6511 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/user_api/views.py
+-rw-r--r--   0 runner    (1001) docker     (123)      394 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jaseci_serv/wsgi.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:34.835675 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      178 2023-02-14 17:26:34.000000 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-02-14 17:26:34.000000 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-14 17:26:34.000000 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      372 2023-02-14 17:26:34.000000 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-02-14 17:26:34.000000 jaseci_serv-1.4.0.9/jaseci_serv.egg-info/top_level.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)      628 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/jsserv
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-14 17:26:34.855676 jaseci_serv-1.4.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-02-14 17:25:59.000000 jaseci_serv-1.4.0.9/setup.py
```

### Comparing `jaseci_serv-1.4.0.8/LICENSE` & `jaseci_serv-1.4.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/admin.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/admin.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/jsorc_loadtest.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/jsorc_loadtest.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/createdb.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/createdb.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/dropdb.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/dropdb.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/management/commands/wait_for_db.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/management/commands/wait_for_db.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/models.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/models.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 from django.contrib.auth import get_user_model
 from django.contrib.auth.models import (
     AbstractBaseUser,
     BaseUserManager,
     PermissionsMixin,
 )
 from django.db import models
+from django.db.models import Q
 
 from jaseci.api.interface import Interface
 from jaseci.element.master import Master as CoreMaster
 from jaseci.element.super_master import SuperMaster as CoreSuper
 from jaseci_serv.settings import JASECI_CONFIGS
 from jaseci_serv.svc import MetaService
 from jaseci_serv.base.jsorc import JsOrcApi
@@ -75,26 +76,33 @@
             return True
         except Exception:
             return False
 
 
 class SuperMaster(Master, JsOrcApi, CoreSuper):
     @Interface.admin_api()
-    def master_allusers(self, limit: int = 10, offset: int = 0, asc: bool = False):
+    def master_allusers(
+        self, limit: int = 10, offset: int = 0, asc: bool = False, search: str = None
+    ):
         """
         Returns info on a set of users, limit specifies the number of users to
         return and offset specfies where to start
         """
 
         if (limit < 0) or (offset < 0):
             return {"response": "Error occured! Parameters must be `positive numbers`!"}
         users = get_user_model().objects.all()
 
         if not asc:
             users = users.order_by("-time_created")
+
+        if search:
+            condition = Q(email__icontains=search) | Q(name__icontains=search)
+            users = users.complex_filter(condition)
+
         total = users.count()
         end = offset + limit if limit else total
         filtered_users = []
 
         for i in users[offset:end]:
             filtered_users.append(
                 {
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/aitest_ai_models.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/aitest_ai_models.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/mock_redis.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/mock_redis.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_admin.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_admin.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_commands.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_commands.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_models.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_models.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_orm_hooks.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_orm_hooks.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/base/tests/test_orm_hooks_cfg.py` & `jaseci_serv-1.4.0.9/jaseci_serv/base/tests/test_orm_hooks_cfg.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/hook/orm.py` & `jaseci_serv-1.4.0.9/jaseci_serv/hook/orm.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/api.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/api.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/infer.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/infer.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/ll.jac` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/ll.jac`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/ll_wall.jac` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/ll_wall.jac`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_admin_api.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_admin_api.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_api.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import base64
+import json
 
 from django.contrib.auth import get_user_model
 from django.urls import reverse
 from jaseci_serv.utils.test_utils import skip_without_redis
 
 from rest_framework.test import APIClient
 from rest_framework import status
@@ -1266,14 +1267,44 @@
         """Test API for creating a graph"""
         payload = {}
         res = self.sclient.post(
             reverse("jac_api:master_allusers"), payload, format="json"
         )
         self.assertEqual(res.status_code, status.HTTP_200_OK)
 
+    def test_jac_admin_master_allusers_search(self):
+        """Test API for searching users"""
+        public_client = APIClient()
+        payload = {
+            "op": "user_create",
+            "name": "john.doe@gmail.com",
+            "global_init": "init",
+            "other_fields": {
+                "password": "yoyoyoyoyoyo",
+                "name": "John Doe",
+                "is_activated": True,
+            },
+        }
+
+        public_client.post(reverse(f'jac_api:{payload["op"]}'), payload, format="json")
+
+        res = self.sclient.post(reverse("jac_api:master_allusers"), {}, format="json")
+        res_obj = json.loads(res.content)
+
+        search_res = self.sclient.post(
+            reverse("jac_api:master_allusers"), {"search": "john.doe"}, format="json"
+        )
+        search_res_obj = json.loads(search_res.content)
+
+        self.assertEqual(res.status_code, status.HTTP_200_OK)
+        self.assertEqual(search_res.status_code, status.HTTP_200_OK)
+        self.assertEqual(res_obj["total"], 4)
+        self.assertEqual(search_res_obj["total"], 1)
+        self.assertEqual(search_res_obj["data"][0]["user"], payload["name"])
+
     def test_asim_bug_check(self):
         """Test public API for summoning walker"""
         zsb_file = open(os.path.dirname(__file__) + "/zsb.jac").read()
         payload = {"op": "sentinel_register", "name": "zsb", "code": zsb_file}
         res = self.client.post(
             reverse(f'jac_api:{payload["op"]}'), payload, format="json"
         )
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_jac_general.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_jac_general.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_ll.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_ll.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_ll_wall.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_ll_wall.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/test_pub_walker.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/test_pub_walker.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/try-syntax.jac` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/try-syntax.jac`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/various.jac` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/various.jac`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/tests/zsb.jac` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/tests/zsb.jac`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jac_api/views.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jac_api/views.py`

 * *Files 2% similar despite different names*

```diff
@@ -122,42 +122,44 @@
                         {
                             "name": file.name,
                             "base64": file_base64,
                             "content-type": file.content_type,
                         }
                     )
 
-    def proc_request_ctx(self, request, req_data):
+    def proc_request_ctx(self, request, req_data, raw_req_data):
         user_slzr.requests_for_emails = request
         req_query = request.GET.dict()
         req_data.update(
             {
                 "_req_ctx": {
                     "method": request.method,
                     "headers": dict(request.headers),
                     "query": req_query,
                     "body": req_data.copy(),
-                }
+                },
+                "_raw_req_ctx": raw_req_data.decode("utf-8"),
             }
         )
         req_data.update(req_query)
 
     def proc_request(self, request, **kwargs):
         """Parse request to field set"""
+        raw_req_data = request.body
         pl_peek = str(dict(request.data))[:256]
         logger.info(str(f"Incoming call to {type(self).__name__} with {pl_peek}"))
         self.start_time = time()
 
         req_data = (
             request.data.dict() if type(request.data) is not dict else request.data
         )
 
         self.proc_prime_ctx(request, req_data)
         self.proc_file_ctx(request, req_data)
-        self.proc_request_ctx(request, req_data)
+        self.proc_request_ctx(request, req_data, raw_req_data)
 
         req_data.update(kwargs)
 
         self.cmd = req_data
         self.set_caller(request)
         self.res = "Not valid interaction!"
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/config.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/config.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/models.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/models.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/serializers.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/serializers.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/tests/test_social_auth.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/tests/test_social_auth.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/urls.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/urls.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/utils.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/utils.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/jsx_oauth/views.py` & `jaseci_serv-1.4.0.9/jaseci_serv/jsx_oauth/views.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/obj_api/tests/test_obj_api.py` & `jaseci_serv-1.4.0.9/jaseci_serv/obj_api/tests/test_obj_api.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/obj_api/views.py` & `jaseci_serv-1.4.0.9/jaseci_serv/obj_api/views.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/settings.py` & `jaseci_serv-1.4.0.9/jaseci_serv/settings.py`

 * *Files 1% similar despite different names*

```diff
@@ -47,15 +47,14 @@
     "jaseci_serv.base",
     "jaseci_serv.user_api",
     "jaseci_serv.obj_api",
     "jaseci_serv.jac_api",
     "corsheaders",
     "django_celery_results",
     "django_celery_beat",
-    "jaseci_serv.jsx_stripe",
     "jaseci_serv.jsx_oauth",
 ]
 
 MIDDLEWARE = [
     "corsheaders.middleware.CorsMiddleware",
     "django.middleware.security.SecurityMiddleware",
     "django.contrib.sessions.middleware.SessionMiddleware",
@@ -206,16 +205,14 @@
     "EMAIL_RESETPASS_HTML_BODY",
     "LOGIN_TOKEN_TTL_HOURS",
 ]
 
 DJANGO_CELERY_BEAT_TZ_AWARE = False
 DEFAULT_AUTO_FIELD = "django.db.models.AutoField"
 
-JSX_STRIPE_DIR = os.path.join(BASE_DIR, "jaseci_serv/jsx_stripe")
-
 
 #################################################
 #                    ADDONS                     #
 #################################################
 
 # ------------------- OAUTH ------------------- #
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/svc/elastic/elastic.py` & `jaseci_serv-1.4.0.9/jaseci_serv/svc/elastic/elastic.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/config.py` & `jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/config.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/svc/mail/mail.py` & `jaseci_serv-1.4.0.9/jaseci_serv/svc/mail/mail.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/svc/meta.py` & `jaseci_serv-1.4.0.9/jaseci_serv/svc/meta.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 from jaseci.svc import MetaService as Ms
 from jaseci_serv.svc import (
     MailService,
     RedisService,
     TaskService,
     PromotheusService,
     ElasticService,
+    StripeService,
+    PromotheusService,
 )
 from .config import RUN_SVCS
 
 
 class MetaService(Ms):
     ###################################################
     #                   OVERRIDEN                     #
@@ -37,7 +39,8 @@
 
     def populate_services(self):
         self.add_service_builder("redis", RedisService)
         self.add_service_builder("task", TaskService)
         self.add_service_builder("mail", MailService)
         self.add_service_builder("promon", PromotheusService)
         self.add_service_builder("elastic", ElasticService)
+        self.add_service_builder("stripe", StripeService)
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/svc/task/config.py` & `jaseci_serv-1.4.0.9/jaseci_serv/svc/task/config.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/urls.py` & `jaseci_serv-1.4.0.9/jaseci_serv/urls.py`

 * *Files 4% similar despite different names*

```diff
@@ -40,10 +40,9 @@
         name="schema-swagger-ui",
     ),
     path("redocs/", schema_view.with_ui("redoc", cache_timeout=0), name="schema-redoc"),
     path("admin/", admin.site.urls),
     path("user/", include("jaseci_serv.user_api.urls")),
     path("", include("jaseci_serv.jac_api.urls")),
     path("", include("jaseci_serv.obj_api.urls")),
-    path("js_admin/stripe/", include("jaseci_serv.jsx_stripe.urls")),
     path("", include("jaseci_serv.jsx_oauth.urls")),
 ]
```

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/user_api/serializers.py` & `jaseci_serv-1.4.0.9/jaseci_serv/user_api/serializers.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/user_api/tests/test_user_api.py` & `jaseci_serv-1.4.0.9/jaseci_serv/user_api/tests/test_user_api.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/user_api/urls.py` & `jaseci_serv-1.4.0.9/jaseci_serv/user_api/urls.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv/user_api/views.py` & `jaseci_serv-1.4.0.9/jaseci_serv/user_api/views.py`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/jaseci_serv.egg-info/SOURCES.txt` & `jaseci_serv-1.4.0.9/jaseci_serv.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -63,27 +63,14 @@
 jaseci_serv/jsx_oauth/permissions.py
 jaseci_serv/jsx_oauth/serializers.py
 jaseci_serv/jsx_oauth/urls.py
 jaseci_serv/jsx_oauth/utils.py
 jaseci_serv/jsx_oauth/views.py
 jaseci_serv/jsx_oauth/tests/__init__.py
 jaseci_serv/jsx_oauth/tests/test_social_auth.py
-jaseci_serv/jsx_stripe/__init__.py
-jaseci_serv/jsx_stripe/admin.py
-jaseci_serv/jsx_stripe/apps.py
-jaseci_serv/jsx_stripe/models.py
-jaseci_serv/jsx_stripe/stripe.jac
-jaseci_serv/jsx_stripe/urls.py
-jaseci_serv/jsx_stripe/utils.py
-jaseci_serv/jsx_stripe/views.py
-jaseci_serv/jsx_stripe/actions/__init__.py
-jaseci_serv/jsx_stripe/actions/stripe.py
-jaseci_serv/jsx_stripe/tests/__init__.py
-jaseci_serv/jsx_stripe/tests/test_api.py
-jaseci_serv/jsx_stripe/tests/test_stripe_jac.py
 jaseci_serv/obj_api/__init__.py
 jaseci_serv/obj_api/apps.py
 jaseci_serv/obj_api/urls.py
 jaseci_serv/obj_api/views.py
 jaseci_serv/obj_api/tests/__init__.py
 jaseci_serv/obj_api/tests/test_obj_api.py
 jaseci_serv/svc/__init__.py
@@ -97,14 +84,17 @@
 jaseci_serv/svc/mail/mail.py
 jaseci_serv/svc/prometheus/__init__.py
 jaseci_serv/svc/prometheus/config.py
 jaseci_serv/svc/prometheus/prometheus.py
 jaseci_serv/svc/redis/__init__.py
 jaseci_serv/svc/redis/config.py
 jaseci_serv/svc/redis/redis.py
+jaseci_serv/svc/stripe/__init__.py
+jaseci_serv/svc/stripe/config.py
+jaseci_serv/svc/stripe/stripe.py
 jaseci_serv/svc/task/__init__.py
 jaseci_serv/svc/task/config.py
 jaseci_serv/svc/task/task.py
 jaseci_serv/user_api/__init__.py
 jaseci_serv/user_api/apps.py
 jaseci_serv/user_api/serializers.py
 jaseci_serv/user_api/urls.py
```

### Comparing `jaseci_serv-1.4.0.8/jsserv` & `jaseci_serv-1.4.0.9/jsserv`

 * *Files identical despite different names*

### Comparing `jaseci_serv-1.4.0.8/setup.py` & `jaseci_serv-1.4.0.9/setup.py`

 * *Files identical despite different names*

