# Comparing `tmp/irails-1.3.5.tar.gz` & `tmp/irails-1.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "irails-1.3.5.tar", last modified: Fri May 12 06:08:16 2023, max compression
+gzip compressed data, was "irails-1.3.6.tar", last modified: Sat May 13 06:11:24 2023, max compression
```

## Comparing `irails-1.3.5.tar` & `irails-1.3.6.tar`

### file list

```diff
@@ -1,88 +1,88 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.273355 irails-1.3.5/
--rw-rw-rw-   0        0        0       83 2023-05-04 04:10:30.000000 irails-1.3.5/MANIFEST.in
--rw-rw-rw-   0        0        0     5079 2023-05-12 06:08:16.272357 irails-1.3.5/PKG-INFO
--rw-rw-rw-   0        0        0     4296 2023-05-09 11:36:53.000000 irails-1.3.5/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.198590 irails-1.3.5/irails/
--rw-rw-rw-   0        0        0      306 2023-05-12 06:08:00.000000 irails-1.3.5/irails/__init__.py
--rw-rw-rw-   0        0        0     3402 2023-05-07 08:38:04.000000 irails-1.3.5/irails/_i18n.py
--rw-rw-rw-   0        0        0     2445 2023-05-11 15:39:57.000000 irails-1.3.5/irails/_loader.py
--rw-rw-rw-   0        0        0     2390 2023-04-27 14:23:55.000000 irails-1.3.5/irails/_utils.py
--rw-rw-rw-   0        0        0    11722 2023-05-11 15:21:25.000000 irails-1.3.5/irails/auth.py
--rw-rw-rw-   0        0        0    12332 2023-05-12 05:53:59.000000 irails-1.3.5/irails/base_controller.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.207568 irails-1.3.5/irails/casbin_adapters/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.209562 irails-1.3.5/irails/casbin_adapters/__pycache__/
--rw-rw-rw-   0        0        0    17834 2023-04-30 14:29:09.000000 irails-1.3.5/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc
--rw-rw-rw-   0        0        0    10407 2023-04-30 14:28:38.000000 irails-1.3.5/irails/casbin_adapters/sqlalchemy_adapter.py
--rw-rw-rw-   0        0        0     4381 2023-02-25 09:43:32.000000 irails-1.3.5/irails/cbv.py
--rw-rw-rw-   0        0        0     6065 2023-05-11 15:19:41.000000 irails-1.3.5/irails/config.py
--rw-rw-rw-   0        0        0    12478 2023-05-12 05:56:24.000000 irails-1.3.5/irails/controller_utils.py
--rw-rw-rw-   0        0        0    32319 2023-05-12 06:03:46.000000 irails-1.3.5/irails/core.py
--rw-rw-rw-   0        0        0     6409 2023-05-11 15:21:34.000000 irails-1.3.5/irails/database.py
--rw-rw-rw-   0        0        0     1459 2023-05-11 15:27:11.000000 irails-1.3.5/irails/log.py
--rw-rw-rw-   0        0        0     8673 2023-05-11 15:20:30.000000 irails-1.3.5/irails/midware.py
--rw-rw-rw-   0        0        0     2141 2023-04-03 14:30:15.000000 irails-1.3.5/irails/midware_casbin.py
--rw-rw-rw-   0        0        0     9341 2023-05-11 15:20:39.000000 irails-1.3.5/irails/midware_session.py
--rw-rw-rw-   0        0        0     4200 2023-04-27 11:53:07.000000 irails-1.3.5/irails/mvc_router.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.216542 irails-1.3.5/irails/scripts/
--rw-rw-rw-   0        0        0        0 2023-04-26 07:44:41.000000 irails-1.3.5/irails/scripts/__init__.py
--rw-rw-rw-   0        0        0     7811 2023-05-11 15:34:41.000000 irails-1.3.5/irails/scripts/_app.py
--rw-rw-rw-   0        0        0     7690 2023-05-09 06:52:08.000000 irails-1.3.5/irails/scripts/_controller.py
--rw-rw-rw-   0        0        0     6934 2023-05-11 05:34:35.000000 irails-1.3.5/irails/scripts/_i18n.py
--rw-rw-rw-   0        0        0     2301 2023-05-03 14:35:33.000000 irails-1.3.5/irails/scripts/_project.py
--rw-rw-rw-   0        0        0     1600 2023-05-11 15:45:21.000000 irails-1.3.5/irails/scripts/_run.py
--rw-rw-rw-   0        0        0     2288 2023-05-11 14:15:32.000000 irails-1.3.5/irails/scripts/_shell.py
--rw-rw-rw-   0        0        0     1855 2023-05-11 12:33:17.000000 irails-1.3.5/irails/scripts/main.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.163913 irails-1.3.5/irails/scripts/tpls/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.228511 irails-1.3.5/irails/scripts/tpls/app/
--rw-rw-rw-   0        0        0      223 2023-05-09 15:18:47.000000 irails-1.3.5/irails/scripts/tpls/app/controller.tpl
--rw-rw-rw-   0        0        0        0 2023-04-28 06:03:05.000000 irails-1.3.5/irails/scripts/tpls/app/css.tpl
--rw-rw-rw-   0        0        0      791 2023-04-25 10:42:10.000000 irails-1.3.5/irails/scripts/tpls/app/home.css.tpl
--rw-rw-rw-   0        0        0     1293 2023-05-05 10:16:42.000000 irails-1.3.5/irails/scripts/tpls/app/home.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 11:52:26.000000 irails-1.3.5/irails/scripts/tpls/app/model.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 11:52:38.000000 irails-1.3.5/irails/scripts/tpls/app/service.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 12:03:35.000000 irails-1.3.5/irails/scripts/tpls/app/test.tpl
--rw-rw-rw-   0        0        0       18 2023-05-02 08:56:04.000000 irails-1.3.5/irails/scripts/tpls/app/view.tpl
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.230506 irails-1.3.5/irails/scripts/tpls/project/
--rw-rw-rw-   0        0        0      139 2023-04-23 09:46:24.000000 irails-1.3.5/irails/scripts/tpls/project/.gitignore
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.231507 irails-1.3.5/irails/scripts/tpls/project/apps/
--rw-rw-rw-   0        0        0        0 2023-04-26 09:58:51.000000 irails-1.3.5/irails/scripts/tpls/project/apps/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.243471 irails-1.3.5/irails/scripts/tpls/project/configs/
--rw-rw-rw-   0        0        0      746 2023-05-09 06:45:34.000000 irails-1.3.5/irails/scripts/tpls/project/configs/alembic.ini
--rw-rw-rw-   0        0        0      198 2023-05-09 06:44:21.000000 irails-1.3.5/irails/scripts/tpls/project/configs/authencation.yaml
--rw-rw-rw-   0        0        0        0 2023-03-06 08:27:07.000000 irails-1.3.5/irails/scripts/tpls/project/configs/cache.yaml
--rw-rw-rw-   0        0        0      104 2023-05-04 05:06:32.000000 irails-1.3.5/irails/scripts/tpls/project/configs/casbin-adapter.csv
--rw-rw-rw-   0        0        0      302 2023-05-04 05:24:51.000000 irails-1.3.5/irails/scripts/tpls/project/configs/casbin-model.conf
--rw-rw-rw-   0        0        0      817 2023-05-10 10:45:36.000000 irails-1.3.5/irails/scripts/tpls/project/configs/database.yaml
--rw-rw-rw-   0        0        0      748 2023-05-11 05:35:06.000000 irails-1.3.5/irails/scripts/tpls/project/configs/general.yaml
--rw-rw-rw-   0        0        0      337 2023-04-22 10:54:12.000000 irails-1.3.5/irails/scripts/tpls/project/configs/session.yaml
--rw-rw-rw-   0        0        0      272 2023-05-09 06:44:59.000000 irails-1.3.5/irails/scripts/tpls/project/configs/upload.yaml
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.168132 irails-1.3.5/irails/scripts/tpls/project/data/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.246463 irails-1.3.5/irails/scripts/tpls/project/data/alembic/
--rw-rw-rw-   0        0        0       38 2023-04-09 12:01:20.000000 irails-1.3.5/irails/scripts/tpls/project/data/alembic/README
--rw-rw-rw-   0        0        0     2144 2023-04-30 09:03:04.000000 irails-1.3.5/irails/scripts/tpls/project/data/alembic/env.py
--rw-rw-rw-   0        0        0      510 2023-04-09 12:01:20.000000 irails-1.3.5/irails/scripts/tpls/project/data/alembic/script.py.mako
--rw-rw-rw-   0        0        0      231 2023-05-11 15:42:13.000000 irails-1.3.5/irails/scripts/tpls/project/main.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.248458 irails-1.3.5/irails/scripts/tpls/project/public/
--rw-rw-rw-   0        0        0     1233 2023-05-02 08:46:22.000000 irails-1.3.5/irails/scripts/tpls/project/public/error_404.html
--rw-rw-rw-   0        0        0     1083 2023-05-02 08:46:46.000000 irails-1.3.5/irails/scripts/tpls/project/public/error_500.html
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.250452 irails-1.3.5/irails/scripts/tpls/project/public/libs/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.172122 irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.254422 irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/
--rw-rw-rw-   0        0        0  1970121 2023-04-23 08:02:36.000000 irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.265375 irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/
--rw-rw-rw-   0        0        0   323666 2023-04-23 08:04:13.000000 irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css
--rw-rw-rw-   0        0        0      725 2023-04-21 12:39:53.000000 irails-1.3.5/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js
--rw-rw-rw-   0        0        0  1441055 2023-04-21 07:36:37.000000 irails-1.3.5/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.173119 irails-1.3.5/irails/scripts/tpls/project/public/vue@3.2.36/
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.267370 irails-1.3.5/irails/scripts/tpls/project/public/vue@3.2.36/dist/
--rw-rw-rw-   0        0        0   640610 2023-04-21 07:36:07.000000 irails-1.3.5/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js
--rw-rw-rw-   0        0        0     2887 2023-05-12 05:35:40.000000 irails-1.3.5/irails/view.py
-drwxrwxrwx   0        0        0        0 2023-05-12 06:08:16.204576 irails-1.3.5/irails.egg-info/
--rw-rw-rw-   0        0        0     5079 2023-05-12 06:08:15.000000 irails-1.3.5/irails.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2326 2023-05-12 06:08:16.000000 irails-1.3.5/irails.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 06:08:15.000000 irails-1.3.5/irails.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-12 06:08:15.000000 irails-1.3.5/irails.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      766 2023-05-12 06:08:15.000000 irails-1.3.5/irails.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-05-12 06:08:15.000000 irails-1.3.5/irails.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 06:08:16.273355 irails-1.3.5/setup.cfg
--rw-rw-rw-   0        0        0     2551 2023-05-09 11:27:27.000000 irails-1.3.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.763029 irails-1.3.6/
+-rw-rw-rw-   0        0        0       83 2023-05-04 04:10:30.000000 irails-1.3.6/MANIFEST.in
+-rw-rw-rw-   0        0        0     5315 2023-05-13 06:11:24.752058 irails-1.3.6/PKG-INFO
+-rw-rw-rw-   0        0        0     4532 2023-05-13 06:11:01.000000 irails-1.3.6/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.671378 irails-1.3.6/irails/
+-rw-rw-rw-   0        0        0      306 2023-05-13 05:44:35.000000 irails-1.3.6/irails/__init__.py
+-rw-rw-rw-   0        0        0     3409 2023-05-13 06:08:26.000000 irails-1.3.6/irails/_i18n.py
+-rw-rw-rw-   0        0        0     2445 2023-05-11 15:39:57.000000 irails-1.3.6/irails/_loader.py
+-rw-rw-rw-   0        0        0     2390 2023-04-27 14:23:55.000000 irails-1.3.6/irails/_utils.py
+-rw-rw-rw-   0        0        0    11722 2023-05-11 15:21:25.000000 irails-1.3.6/irails/auth.py
+-rw-rw-rw-   0        0        0    12426 2023-05-13 05:30:29.000000 irails-1.3.6/irails/base_controller.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.683900 irails-1.3.6/irails/casbin_adapters/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.685894 irails-1.3.6/irails/casbin_adapters/__pycache__/
+-rw-rw-rw-   0        0        0    17834 2023-04-30 14:29:09.000000 irails-1.3.6/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc
+-rw-rw-rw-   0        0        0    10589 2023-05-13 05:03:07.000000 irails-1.3.6/irails/casbin_adapters/sqlalchemy_adapter.py
+-rw-rw-rw-   0        0        0     4381 2023-02-25 09:43:32.000000 irails-1.3.6/irails/cbv.py
+-rw-rw-rw-   0        0        0     6065 2023-05-11 15:19:41.000000 irails-1.3.6/irails/config.py
+-rw-rw-rw-   0        0        0    12478 2023-05-12 05:56:24.000000 irails-1.3.6/irails/controller_utils.py
+-rw-rw-rw-   0        0        0    32319 2023-05-12 06:03:46.000000 irails-1.3.6/irails/core.py
+-rw-rw-rw-   0        0        0     6409 2023-05-11 15:21:34.000000 irails-1.3.6/irails/database.py
+-rw-rw-rw-   0        0        0     1459 2023-05-11 15:27:11.000000 irails-1.3.6/irails/log.py
+-rw-rw-rw-   0        0        0     8673 2023-05-11 15:20:30.000000 irails-1.3.6/irails/midware.py
+-rw-rw-rw-   0        0        0     2141 2023-04-03 14:30:15.000000 irails-1.3.6/irails/midware_casbin.py
+-rw-rw-rw-   0        0        0     9341 2023-05-11 15:20:39.000000 irails-1.3.6/irails/midware_session.py
+-rw-rw-rw-   0        0        0     4200 2023-04-27 11:53:07.000000 irails-1.3.6/irails/mvc_router.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.694213 irails-1.3.6/irails/scripts/
+-rw-rw-rw-   0        0        0        0 2023-04-26 07:44:41.000000 irails-1.3.6/irails/scripts/__init__.py
+-rw-rw-rw-   0        0        0     7811 2023-05-11 15:34:41.000000 irails-1.3.6/irails/scripts/_app.py
+-rw-rw-rw-   0        0        0     7690 2023-05-09 06:52:08.000000 irails-1.3.6/irails/scripts/_controller.py
+-rw-rw-rw-   0        0        0     7755 2023-05-13 05:57:18.000000 irails-1.3.6/irails/scripts/_i18n.py
+-rw-rw-rw-   0        0        0     2301 2023-05-03 14:35:33.000000 irails-1.3.6/irails/scripts/_project.py
+-rw-rw-rw-   0        0        0     1600 2023-05-11 15:45:21.000000 irails-1.3.6/irails/scripts/_run.py
+-rw-rw-rw-   0        0        0     2288 2023-05-11 14:15:32.000000 irails-1.3.6/irails/scripts/_shell.py
+-rw-rw-rw-   0        0        0     1855 2023-05-11 12:33:17.000000 irails-1.3.6/irails/scripts/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.635352 irails-1.3.6/irails/scripts/tpls/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.705184 irails-1.3.6/irails/scripts/tpls/app/
+-rw-rw-rw-   0        0        0      223 2023-05-09 15:18:47.000000 irails-1.3.6/irails/scripts/tpls/app/controller.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-28 06:03:05.000000 irails-1.3.6/irails/scripts/tpls/app/css.tpl
+-rw-rw-rw-   0        0        0      791 2023-04-25 10:42:10.000000 irails-1.3.6/irails/scripts/tpls/app/home.css.tpl
+-rw-rw-rw-   0        0        0     1293 2023-05-05 10:16:42.000000 irails-1.3.6/irails/scripts/tpls/app/home.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 11:52:26.000000 irails-1.3.6/irails/scripts/tpls/app/model.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 11:52:38.000000 irails-1.3.6/irails/scripts/tpls/app/service.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 12:03:35.000000 irails-1.3.6/irails/scripts/tpls/app/test.tpl
+-rw-rw-rw-   0        0        0       18 2023-05-02 08:56:04.000000 irails-1.3.6/irails/scripts/tpls/app/view.tpl
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.708175 irails-1.3.6/irails/scripts/tpls/project/
+-rw-rw-rw-   0        0        0      139 2023-04-23 09:46:24.000000 irails-1.3.6/irails/scripts/tpls/project/.gitignore
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.709173 irails-1.3.6/irails/scripts/tpls/project/apps/
+-rw-rw-rw-   0        0        0        0 2023-04-26 09:58:51.000000 irails-1.3.6/irails/scripts/tpls/project/apps/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.721141 irails-1.3.6/irails/scripts/tpls/project/configs/
+-rw-rw-rw-   0        0        0      746 2023-05-09 06:45:34.000000 irails-1.3.6/irails/scripts/tpls/project/configs/alembic.ini
+-rw-rw-rw-   0        0        0      198 2023-05-09 06:44:21.000000 irails-1.3.6/irails/scripts/tpls/project/configs/authencation.yaml
+-rw-rw-rw-   0        0        0        0 2023-03-06 08:27:07.000000 irails-1.3.6/irails/scripts/tpls/project/configs/cache.yaml
+-rw-rw-rw-   0        0        0      104 2023-05-04 05:06:32.000000 irails-1.3.6/irails/scripts/tpls/project/configs/casbin-adapter.csv
+-rw-rw-rw-   0        0        0      302 2023-05-04 05:24:51.000000 irails-1.3.6/irails/scripts/tpls/project/configs/casbin-model.conf
+-rw-rw-rw-   0        0        0      817 2023-05-10 10:45:36.000000 irails-1.3.6/irails/scripts/tpls/project/configs/database.yaml
+-rw-rw-rw-   0        0        0      748 2023-05-11 05:35:06.000000 irails-1.3.6/irails/scripts/tpls/project/configs/general.yaml
+-rw-rw-rw-   0        0        0      337 2023-04-22 10:54:12.000000 irails-1.3.6/irails/scripts/tpls/project/configs/session.yaml
+-rw-rw-rw-   0        0        0      272 2023-05-09 06:44:59.000000 irails-1.3.6/irails/scripts/tpls/project/configs/upload.yaml
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.638904 irails-1.3.6/irails/scripts/tpls/project/data/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.725130 irails-1.3.6/irails/scripts/tpls/project/data/alembic/
+-rw-rw-rw-   0        0        0       38 2023-04-09 12:01:20.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/README
+-rw-rw-rw-   0        0        0     2144 2023-04-30 09:03:04.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/env.py
+-rw-rw-rw-   0        0        0      510 2023-04-09 12:01:20.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/script.py.mako
+-rw-rw-rw-   0        0        0      231 2023-05-11 15:42:13.000000 irails-1.3.6/irails/scripts/tpls/project/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.727124 irails-1.3.6/irails/scripts/tpls/project/public/
+-rw-rw-rw-   0        0        0     1233 2023-05-02 08:46:22.000000 irails-1.3.6/irails/scripts/tpls/project/public/error_404.html
+-rw-rw-rw-   0        0        0     1083 2023-05-02 08:46:46.000000 irails-1.3.6/irails/scripts/tpls/project/public/error_500.html
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.731145 irails-1.3.6/irails/scripts/tpls/project/public/libs/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.642117 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.736107 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/
+-rw-rw-rw-   0        0        0  1970121 2023-04-23 08:02:36.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.742084 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/
+-rw-rw-rw-   0        0        0   323666 2023-04-23 08:04:13.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css
+-rw-rw-rw-   0        0        0      725 2023-04-21 12:39:53.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js
+-rw-rw-rw-   0        0        0  1441055 2023-04-21 07:36:37.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.644117 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.748069 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/
+-rw-rw-rw-   0        0        0   640610 2023-04-21 07:36:07.000000 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js
+-rw-rw-rw-   0        0        0     2887 2023-05-12 05:35:40.000000 irails-1.3.6/irails/view.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.681358 irails-1.3.6/irails.egg-info/
+-rw-rw-rw-   0        0        0     5315 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2326 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      778 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 06:11:24.763029 irails-1.3.6/setup.cfg
+-rw-rw-rw-   0        0        0     2551 2023-05-09 11:27:27.000000 irails-1.3.6/setup.py
```

### Comparing `irails-1.3.5/PKG-INFO` & `irails-1.3.6/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,318 +1,284 @@
-00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
-00000010: 3a20 322e 310d 0a4e 616d 653a 2069 7261  : 2.1..Name: ira
-00000020: 696c 730d 0a56 6572 7369 6f6e 3a20 312e  ils..Version: 1.
-00000030: 332e 350d 0a53 756d 6d61 7279 3a20 5369  3.5..Summary: Si
-00000040: 6d70 6c65 2061 6e64 2065 6c65 6761 6e74  mple and elegant
-00000050: 2075 7365 206f 6620 4661 7374 4170 6920   use of FastApi 
-00000060: 696e 204d 5643 206d 6f64 650d 0a48 6f6d  in MVC mode..Hom
-00000070: 652d 7061 6765 3a20 6874 7470 733a 2f2f  e-page: https://
-00000080: 6769 7468 7562 2e63 6f6d 2f73 6d6a 6b7a  github.com/smjkz
-00000090: 736c 2f69 7261 696c 730d 0a41 7574 686f  sl/irails..Autho
-000000a0: 723a 2042 7275 6365 2063 686f 750d 0a41  r: Bruce chou..A
-000000b0: 7574 686f 722d 656d 6169 6c3a 2073 6d6a  uthor-email: smj
-000000c0: 6b7a 736c 4067 6d61 696c 2e63 6f6d 0d0a  kzsl@gmail.com..
-000000d0: 4c69 6365 6e73 653a 2041 7061 6368 6520  License: Apache 
-000000e0: 4c69 6365 6e73 6520 322e 300d 0a4b 6579  License 2.0..Key
-000000f0: 776f 7264 733a 2077 6562 2066 7261 6d65  words: web frame
-00000100: 776f 726b 2c6d 7663 2066 7261 6d65 776f  work,mvc framewo
-00000110: 726b 2c66 6173 7461 7069 2066 7261 6d65  rk,fastapi frame
-00000120: 776f 726b 0d0a 436c 6173 7369 6669 6572  work..Classifier
-00000130: 3a20 4c69 6365 6e73 6520 3a3a 204f 5349  : License :: OSI
-00000140: 2041 7070 726f 7665 6420 3a3a 2041 7061   Approved :: Apa
-00000150: 6368 6520 536f 6674 7761 7265 204c 6963  che Software Lic
-00000160: 656e 7365 0d0a 436c 6173 7369 6669 6572  ense..Classifier
-00000170: 3a20 4f70 6572 6174 696e 6720 5379 7374  : Operating Syst
-00000180: 656d 203a 3a20 4f53 2049 6e64 6570 656e  em :: OS Indepen
-00000190: 6465 6e74 0d0a 436c 6173 7369 6669 6572  dent..Classifier
-000001a0: 3a20 5072 6f67 7261 6d6d 696e 6720 4c61  : Programming La
-000001b0: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
-000001c0: 203a 3a20 332e 360d 0a43 6c61 7373 6966   :: 3.6..Classif
-000001d0: 6965 723a 2050 726f 6772 616d 6d69 6e67  ier: Programming
-000001e0: 204c 616e 6775 6167 6520 3a3a 2050 7974   Language :: Pyt
-000001f0: 686f 6e20 3a3a 2033 2e37 0d0a 436c 6173  hon :: 3.7..Clas
-00000200: 7369 6669 6572 3a20 5072 6f67 7261 6d6d  sifier: Programm
-00000210: 696e 6720 4c61 6e67 7561 6765 203a 3a20  ing Language :: 
-00000220: 5079 7468 6f6e 203a 3a20 332e 380d 0a43  Python :: 3.8..C
-00000230: 6c61 7373 6966 6965 723a 2050 726f 6772  lassifier: Progr
-00000240: 616d 6d69 6e67 204c 616e 6775 6167 6520  amming Language 
-00000250: 3a3a 2050 7974 686f 6e20 3a3a 2033 2e39  :: Python :: 3.9
-00000260: 0d0a 436c 6173 7369 6669 6572 3a20 5072  ..Classifier: Pr
-00000270: 6f67 7261 6d6d 696e 6720 4c61 6e67 7561  ogramming Langua
-00000280: 6765 203a 3a20 5079 7468 6f6e 203a 3a20  ge :: Python :: 
-00000290: 332e 3130 0d0a 436c 6173 7369 6669 6572  3.10..Classifier
-000002a0: 3a20 5072 6f67 7261 6d6d 696e 6720 4c61  : Programming La
-000002b0: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
-000002c0: 203a 3a20 332e 3131 0d0a 5265 7175 6972   :: 3.11..Requir
-000002d0: 6573 2d50 7974 686f 6e3a 203e 3d33 2e36  es-Python: >=3.6
-000002e0: 0d0a 4465 7363 7269 7074 696f 6e2d 436f  ..Description-Co
-000002f0: 6e74 656e 742d 5479 7065 3a20 7465 7874  ntent-Type: text
-00000300: 2f6d 6172 6b64 6f77 6e0d 0a0d 0a23 2069  /markdown....# i
-00000310: 7261 696c 730d 0a41 206d 7663 2066 7261  rails..A mvc fra
-00000320: 6d65 776f 726b 2075 7365 6420 4661 7374  mework used Fast
-00000330: 4170 690d 0a53 696d 706c 6520 616e 6420  Api..Simple and 
-00000340: 656c 6567 616e 7420 7573 6520 6f66 2046  elegant use of F
-00000350: 6173 7441 7069 2069 6e20 4d56 4320 6d6f  astApi in MVC mo
-00000360: 6465 0d0a 0d0a 5b44 656d 6f5d 2868 7474  de....[Demo](htt
-00000370: 7073 3a2f 2f69 7261 696c 732e 3272 6169  ps://irails.2rai
-00000380: 6c73 2e63 6e2f 2920 0d0a 2320 5765 6c63  ls.cn/) ..# Welc
-00000390: 6f6d 6520 746f 2049 5241 494c 5328 7079  ome to IRAILS(py
-000003a0: 7468 6f6e 206f 6e20 7261 696c 7329 0d0a  thon on rails)..
-000003b0: 0d0a 200d 0a0d 0a23 2320 496e 7374 616c  .. ....## Instal
-000003c0: 6c61 7469 6f6e 2020 0d0a 0d0a 2a20 6070  lation  ....* `p
-000003d0: 6970 2069 6e73 7461 6c6c 2069 7261 696c  ip install irail
-000003e0: 7360 202d 2069 6e73 7461 6c6c 2069 7261  s` - install ira
-000003f0: 696c 730d 0a0d 0a23 2320 436f 6d6d 616e  ils....## Comman
-00000400: 6473 0d0a 0d0a 2a20 6069 7261 696c 7320  ds....* `irails 
-00000410: 7072 6f6a 6563 7420 5b70 726f 6a65 6374  project [project
-00000420: 2d6e 616d 6528 6469 722d 6e61 6d65 295d  -name(dir-name)]
-00000430: 6020 2d20 4372 6561 7465 2061 206e 6577  ` - Create a new
-00000440: 2069 7261 696c 7320 7072 6f6a 6563 742e   irails project.
-00000450: 0d0a 2a20 6069 7261 696c 7320 6170 7020  ..* `irails app 
-00000460: 5b61 7070 2d6e 616d 6528 6368 6f6f 7365  [app-name(choose
-00000470: 206f 7220 696e 7075 7420 6170 7073 2064   or input apps d
-00000480: 6972 295d 6020 2d20 4578 616d 706c 653a  ir)]` - Example:
-00000490: 2060 6972 6169 6c73 2061 7070 2061 646d   `irails app adm
-000004a0: 6973 7369 6f6e 7360 2043 7265 6174 6520  issions` Create 
-000004b0: 6120 6e65 7720 6972 6169 6c73 2061 7070  a new irails app
-000004c0: 2e0d 0a2a 2060 6972 6169 6c73 2072 756e  ...* `irails run
-000004d0: 205b 2d2d 706f 7274 2070 6f72 745d 6020   [--port port]` 
-000004e0: 2d20 5275 6e20 7072 6f6a 6563 7420 7669  - Run project vi
-000004f0: 7369 7420 6f6e 203c 6120 6872 6566 3d22  sit on <a href="
-00000500: 6874 7470 3a2f 2f31 3237 2e30 2e30 2e31  http://127.0.0.1
-00000510: 3a38 3030 3022 3e68 7474 703a 2f2f 3132  :8000">http://12
-00000520: 372e 302e 302e 313a 3830 3030 3c2f 613e  7.0.0.1:8000</a>
-00000530: 2e20 0d0a 200d 0a0d 0a23 2320 5072 6f6a  . .. ....## Proj
-00000540: 6563 7420 6c61 796f 7574 0d0a 6060 600d  ect layout..```.
-00000550: 0a20 0d0a 2020 2020 7c20 2020 6d61 696e  . ..    |   main
-00000560: 2e70 790d 0a20 2020 202b 2d2d 2d61 7070  .py..    +---app
-00000570: 7320 2020 2020 2020 2020 2020 2020 2020  s               
-00000580: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000590: 2023 2320 4170 7073 2063 6f6e 7461 696e   ## Apps contain
-000005a0: 6572 2028 4120 7072 6f6a 6563 7420 6361  er (A project ca
-000005b0: 6e20 6861 7665 206d 756c 7469 706c 6520  n have multiple 
-000005c0: 636f 6e74 6169 6e65 7273 290d 0a20 2020  containers)..   
-000005d0: 207c 2020 202b 2d2d 2d61 646d 6973 7369   |   +---admissi
-000005e0: 6f6e 7320 2020 2020 2020 2020 2020 2020  ons             
-000005f0: 2020 2020 2020 2020 2023 2320 4170 7020           ## App 
-00000600: 6469 7220 2841 6e20 6170 706c 6963 6174  dir (An applicat
-00000610: 696f 6e20 636f 6e74 6169 6e65 7220 6361  ion container ca
-00000620: 6e20 6861 7665 206d 756c 7469 706c 6520  n have multiple 
-00000630: 6170 706c 6963 6174 696f 6e73 290d 0a20  applications).. 
-00000640: 2020 207c 2020 207c 2020 207c 2020 205f     |   |   |   _
-00000650: 5f69 6e69 745f 5f2e 7079 2020 2020 2020  _init__.py      
-00000660: 2020 2020 2020 2020 2020 200d 0a20 2020             ..   
-00000670: 207c 2020 207c 2020 202b 2d2d 2d63 6f6e   |   |   +---con
-00000680: 7472 6f6c 6c65 7273 2020 2020 2020 2020  trollers        
-00000690: 2020 2020 2020 2020 2023 2320 436f 6e74           ## Cont
-000006a0: 726f 6c6c 6572 2066 696c 6573 0d0a 2020  roller files..  
-000006b0: 2020 7c20 2020 7c20 2020 7c20 2020 7c20    |   |   |   | 
-000006c0: 2020 686f 6d65 5f63 6f6e 7472 6f6c 6c65    home_controlle
-000006d0: 722e 7079 2020 2020 2020 2323 2043 6f6e  r.py      ## Con
-000006e0: 7472 6f6c 6c65 7220 636c 6173 7320 6669  troller class fi
-000006f0: 6c65 2c69 7427 7320 6c6f 6f6b 206c 696b  le,it's look lik
-00000700: 6520 6063 6c61 7373 2048 6f6d 6543 6f6e  e `class HomeCon
-00000710: 7472 6f6c 6c65 7260 0d0a 2020 2020 7c20  troller`..    | 
-00000720: 2020 7c20 2020 7c20 2020 7c20 2020 5f5f    |   |   |   __
-00000730: 696e 6974 5f5f 2e70 790d 0a20 2020 207c  init__.py..    |
-00000740: 2020 207c 2020 202b 2d2d 2d6c 6f63 616c     |   +---local
-00000750: 6573 2020 2020 2020 2020 2020 2020 2020  es              
-00000760: 2020 2020 2020 2023 2320 4931 386e 206c         ## I18n l
-00000770: 6f63 616c 6573 2064 6972 2c75 7365 2063  ocales dir,use c
-00000780: 6f6d 6d61 6e64 2060 6170 7073 2f61 7070  ommand `apps/app
-00000790: 3a24 2069 7261 6c69 7320 6931 386e 2067  :$ iralis i18n g
-000007a0: 6574 7465 7874 6020 7769 6c6c 2061 7574  ettext` will aut
-000007b0: 6f20 6765 6e65 7261 7465 2069 7465 6d73  o generate items
-000007c0: 0d0a 2020 2020 7c20 2020 7c20 2020 2b2d  ..    |   |   +-
-000007d0: 2d2d 6d6f 6465 6c73 2020 2020 2020 2020  --models        
-000007e0: 2020 2020 2020 2020 2020 2020 2020 2323                ##
-000007f0: 2044 6174 6162 6173 6520 6d6f 6465 6c73   Database models
-00000800: 2066 696c 6573 2869 6620 796f 7520 7573   files(if you us
-00000810: 6520 736f 6d65 2064 6174 6162 6173 6520  e some database 
-00000820: 7375 7070 6f72 7429 0d0a 2020 2020 7c20  support)..    | 
-00000830: 2020 7c20 2020 7c20 2020 2020 2020 5f5f    |   |       __
-00000840: 696e 6974 5f5f 2e70 790d 0a20 2020 207c  init__.py..    |
-00000850: 2020 207c 2020 202b 2d2d 2d73 6572 7669     |   +---servi
-00000860: 6365 7320 2020 2020 2020 2020 2020 2020  ces             
-00000870: 2020 2020 2020 2023 2320 4d6f 6475 6c65         ## Module
-00000880: 2066 6f72 2062 7573 696e 6573 7320 6c6f   for business lo
-00000890: 6769 6320 7072 6f63 6573 7369 6e67 0d0a  gic processing..
-000008a0: 2020 2020 7c20 2020 7c20 2020 2b2d 2d2d      |   |   +---
-000008b0: 7465 7374 7320 2020 2020 2020 2020 2020  tests           
-000008c0: 2020 2020 2020 2020 2020 2020 2323 2055              ## U
-000008d0: 6e69 7420 7465 7374 7469 6e67 0d0a 2020  nit testting..  
-000008e0: 2020 7c20 2020 7c20 2020 2b2d 2d2d 7669    |   |   +---vi
-000008f0: 6577 7320 2020 2020 2020 2020 2020 2020  ews             
-00000900: 2020 2020 2020 2020 2020 2323 2053 7461            ## Sta
-00000910: 7469 6320 7669 6577 2066 696c 6573 2028  tic view files (
-00000920: 7573 6520 604a 696e 6a61 3260 2054 656d  use `Jinja2` Tem
-00000930: 706c 6174 6529 0d0a 2020 2020 7c20 2020  plate)..    |   
-00000940: 7c20 2020 7c20 2020 7c20 2020 6c61 796f  |   |   |   layo
-00000950: 7574 2e68 746d 6c0d 0a20 2020 207c 2020  ut.html..    |  
-00000960: 207c 2020 207c 2020 207c 0d0a 2020 2020   |   |   |..    
-00000970: 7c20 2020 7c20 2020 7c20 2020 2b2d 2d2d  |   |   |   +---
-00000980: 686f 6d65 2020 2020 2020 2020 2020 2020  home            
-00000990: 2020 2020 2020 2020 2323 2054 6865 2063          ## The c
-000009a0: 6f6e 7472 6f6c 6c65 7220 6163 7469 6f6e  ontroller action
-000009b0: 2773 2073 7461 7469 6320 6669 6c65 286e  's static file(n
-000009c0: 616d 6520 6973 2073 616d 6520 746f 2074  ame is same to t
-000009d0: 6865 2063 6f6e 7472 6f6c 6c65 7227 7320  he controller's 
-000009e0: 636c 6173 7320 6e61 6d65 290d 0a20 2020  class name)..   
-000009f0: 207c 2020 207c 2020 207c 2020 207c 2020   |   |   |   |  
-00000a00: 2020 2020 2068 6f6d 652e 6373 7320 2020       home.css   
-00000a10: 2020 2020 2020 2020 200d 0a20 2020 207c           ..    |
-00000a20: 2020 207c 2020 207c 2020 207c 2020 2020     |   |   |    
-00000a30: 2020 2068 6f6d 652e 6874 6d6c 2020 2020     home.html    
-00000a40: 2020 2020 2020 2023 2320 5374 6174 6963         ## Static
-00000a50: 2066 696c 6520 636f 7272 6573 706f 6e64   file correspond
-00000a60: 696e 6720 746f 2061 6374 696f 6e28 6e61  ing to action(na
-00000a70: 6d65 2069 7320 7361 6d65 2074 6f20 7468  me is same to th
-00000a80: 6520 636f 6e74 726f 6c6c 6572 2773 206d  e controller's m
-00000a90: 6574 686f 6420 6e61 6d65 290d 0a20 2020  ethod name)..   
-00000aa0: 202b 2d2d 2d63 6f6e 6669 6773 2020 2020   +---configs    
-00000ab0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000ac0: 2020 2020 2020 2020 2023 2320 5072 6f6a           ## Proj
-00000ad0: 6563 7420 636f 6e66 6967 7572 6520 6469  ect configure di
-00000ae0: 720d 0a20 2020 207c 2020 2020 2020 2061  r..    |       a
-00000af0: 6c65 6d62 6963 2e69 6e69 2020 2020 2020  lembic.ini      
-00000b00: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000b10: 2320 416c 656d 6269 6320 636f 6e66 6967  # Alembic config
-00000b20: 7572 6520 6669 6c65 2028 4765 6e65 7261  ure file (Genera
-00000b30: 6c6c 792c 2074 6865 7265 2069 7320 6e6f  lly, there is no
-00000b40: 206e 6565 6420 746f 2063 6861 6e67 652c   need to change,
-00000b50: 2075 7365 6420 7468 6520 6461 7461 6261   used the databa
-00000b60: 7365 206d 6967 7261 7469 6f6e 290d 0a20  se migration).. 
-00000b70: 2020 207c 2020 2020 2020 2063 6173 6269     |       casbi
-00000b80: 6e2d 6164 6170 7465 722e 6373 7620 2020  n-adapter.csv   
-00000b90: 2020 2020 2020 2020 2020 2023 2320 4361             ## Ca
-00000ba0: 7362 696e 2061 7574 6820 6d6f 6475 6c65  sbin auth module
-00000bb0: 2063 6f6e 6669 6720 6164 6170 7465 7220   config adapter 
-00000bc0: 6669 6c65 2829 0d0a 2020 2020 7c20 2020  file()..    |   
-00000bd0: 2020 2020 6361 7362 696e 2d6d 6f64 656c      casbin-model
-00000be0: 2e63 6f6e 6620 2020 2020 2020 2020 2020  .conf           
-00000bf0: 2020 2020 2323 2043 6173 6269 6e20 6175      ## Casbin au
-00000c00: 7468 2063 6f6e 6669 6720 6d6f 6465 6c0d  th config model.
-00000c10: 0a20 2020 207c 2020 2020 2020 2064 6174  .    |       dat
-00000c20: 6162 6173 652e 7961 6d6c 2020 2020 2020  abase.yaml      
-00000c30: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
-00000c40: 436f 6e66 6967 7572 6520 666f 7220 6461  Configure for da
-00000c50: 7461 6261 7365 2073 7570 706f 7274 0d0a  tabase support..
-00000c60: 2020 2020 7c20 2020 2020 2020 6765 6e65      |       gene
-00000c70: 7261 6c2e 7961 6d6c 2020 2020 2020 2020  ral.yaml        
-00000c80: 2020 2020 2020 2020 2020 2020 2323 2047              ## G
-00000c90: 656e 6572 616c 2063 6f6e 6669 6775 7265  eneral configure
-00000ca0: 730d 0a20 2020 207c 2020 2020 2020 2073  s..    |       s
-00000cb0: 6573 7369 6f6e 2e79 616d 6c20 2020 2020  ession.yaml     
-00000cc0: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000cd0: 2320 5365 7373 696f 6e20 636f 6e66 6967  # Session config
-00000ce0: 7572 6573 0d0a 2020 2020 7c0d 0a20 2020  ures..    |..   
-00000cf0: 202b 2d2d 2d64 6174 610d 0a20 2020 207c   +---data..    |
-00000d00: 2020 202b 2d2d 2d61 6c65 6d62 6963 0d0a     +---alembic..
-00000d10: 2020 2020 7c20 2020 7c20 2020 5c2d 2d2d      |   |   \---
-00000d20: 7665 7273 696f 6e73 0d0a 2020 2020 7c20  versions..    | 
-00000d30: 2020 5c2d 2d2d 6462 0d0a 2020 2020 7c0d    \---db..    |.
-00000d40: 0a20 2020 202b 2d2d 2d70 7562 6c69 6320  .    +---public 
-00000d50: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000d60: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
-00000d70: 5075 626c 6963 2064 6972 2028 7769 6c6c  Public dir (will
-00000d80: 206d 6f75 6e74 6564 2074 6f20 7468 6520   mounted to the 
-00000d90: 272f 7075 626c 6963 2720 7572 6c29 0d0a  '/public' url)..
-00000da0: 2020 2020 7c20 2020 7c20 2020 6572 726f      |   |   erro
-00000db0: 725f 3430 342e 6874 6d6c 2020 2020 2020  r_404.html      
-00000dc0: 2020 2020 2020 2020 2020 2020 2323 2045              ## E
-00000dd0: 7272 6f72 2070 6167 6520 2e2e 2e0d 0a20  rror page ..... 
-00000de0: 2020 207c 2020 207c 2020 2065 7272 6f72     |   |   error
-00000df0: 5f35 3030 2e68 746d 6c0d 0a20 2020 207c  _500.html..    |
-00000e00: 0d0a 2020 2020 2b2d 2d2d 7570 6c6f 6164  ..    +---upload
-00000e10: 7320 2020 2020 2020 2020 2020 2020 2020  s               
-00000e20: 2020 2020 2020 2020 2020 2020 2020 2323                ##
-00000e30: 204f 7468 6572 7320 6469 7228 6966 2079   Others dir(if y
-00000e40: 6f75 7220 6e65 6564 206f 7220 6e6f 7429  our need or not)
-00000e50: 0d0a 6060 600d 0a23 2320 4578 7472 6173  ..```..## Extras
-00000e60: 2063 6f6d 6d61 6e64 730d 0a2a 2060 6972   commands..* `ir
-00000e70: 6169 6c73 2069 3138 6e20 6765 7474 6578  ails i18n gettex
-00000e80: 7460 202d 2d67 656e 6572 6174 6520 6931  t` --generate i1
-00000e90: 386e 2069 6e20 6972 6169 6c73 2061 7070  8n in irails app
-00000ea0: 2064 6972 0d0a 0d0a 2323 2054 616b 6520   dir....## Take 
-00000eb0: 6120 6c6f 6f6b 2063 6f6e 6669 6775 7265  a look configure
-00000ec0: 2066 696c 6520 6067 656e 6572 616c 2e79   file `general.y
-00000ed0: 616d 6c60 0d0a 200d 0a60 6060 200d 0a20  aml`.. ..``` .. 
-00000ee0: 2020 2061 7070 3a0d 0a20 2020 2020 2020     app:..       
-00000ef0: 2061 7070 6469 723a 0d0a 2020 2020 2020   appdir:..      
-00000f00: 2020 2d20 6170 7073 0d0a 2020 2020 2020    - apps..      
-00000f10: 2020 656e 6162 6c65 643a 206e 756c 6c0d    enabled: null.
-00000f20: 0a20 2020 2072 6f6f 743a 2061 7070 732e  .    root: apps.
-00000f30: 726f 6f74 0d0a 0d0a 2020 2020 636f 7273  root....    cors
-00000f40: 3a0d 0a20 2020 2020 2020 2061 6c6c 6f77  :..        allow
-00000f50: 5f63 7265 6465 6e74 6961 6c73 3a20 7472  _credentials: tr
-00000f60: 7565 0d0a 2020 2020 2020 2020 616c 6c6f  ue..        allo
-00000f70: 775f 6865 6164 6572 733a 0d0a 2020 2020  w_headers:..    
-00000f80: 2020 2020 2020 2020 2d20 272a 270d 0a20          - '*'.. 
-00000f90: 2020 2020 2020 2061 6c6c 6f77 5f6d 6574         allow_met
-00000fa0: 686f 6473 3a0d 0a20 2020 2020 2020 2020  hods:..         
-00000fb0: 2020 202d 2027 2a27 0d0a 2020 2020 2020     - '*'..      
-00000fc0: 2020 616c 6c6f 775f 6f72 6967 696e 733a    allow_origins:
-00000fd0: 0d0a 2020 2020 2020 2020 2020 2020 2d20  ..            - 
-00000fe0: 272a 270d 0a20 2020 2064 6562 7567 3a20  '*'..    debug: 
-00000ff0: 7472 7565 0d0a 2020 2020 6572 726f 7273  true..    errors
-00001000: 3a0d 0a20 2020 2020 2020 2065 7272 6f72  :..        error
-00001010: 5f34 3034 5f70 6167 653a 2027 7b52 4f4f  _404_page: '{ROO
-00001020: 542e 7075 626c 6963 5f64 6972 7d2f 6572  T.public_dir}/er
-00001030: 726f 725f 3430 342e 6874 6d6c 270d 0a20  ror_404.html'.. 
-00001040: 2020 2020 2020 2065 7272 6f72 5f35 3030         error_500
-00001050: 5f70 6167 653a 2027 7b52 4f4f 542e 7075  _page: '{ROOT.pu
-00001060: 626c 6963 5f64 6972 7d2f 6572 726f 725f  blic_dir}/error_
-00001070: 3530 302e 6874 6d6c 270d 0a20 2020 206c  500.html'..    l
-00001080: 6f67 3a0d 0a20 2020 2020 2020 2066 696c  og:..        fil
-00001090: 653a 2027 270d 0a20 2020 2020 2020 206c  e: ''..        l
-000010a0: 6576 656c 3a20 4445 4255 470d 0a20 2020  evel: DEBUG..   
-000010b0: 2020 2020 206e 616d 653a 2069 5261 696c       name: iRail
-000010c0: 730d 0a20 2020 2070 7562 6c69 635f 6469  s..    public_di
-000010d0: 723a 202e 2f70 7562 6c69 630d 0a0d 0a20  r: ./public.... 
-000010e0: 2020 2076 6965 773a 0d0a 2020 2020 2020     view:..      
-000010f0: 2020 6a69 6e6a 6132 3a0d 0a20 2020 2020    jinja2:..     
-00001100: 2020 2020 2020 2062 6c6f 636b 5f65 6e64         block_end
-00001110: 5f73 7472 696e 673a 2027 257d 270d 0a20  _string: '%}'.. 
-00001120: 2020 2020 2020 2020 2020 2062 6c6f 636b             block
-00001130: 5f73 7461 7274 5f73 7472 696e 673a 2027  _start_string: '
-00001140: 7b25 270d 0a20 2020 2020 2020 2020 2020  {%'..           
-00001150: 2063 6f6d 6d65 6e74 5f65 6e64 5f73 7472   comment_end_str
-00001160: 696e 673a 2027 237d 270d 0a20 2020 2020  ing: '#}'..     
-00001170: 2020 2020 2020 2063 6f6d 6d65 6e74 5f73         comment_s
-00001180: 7461 7274 5f73 7472 696e 673a 2027 7b23  tart_string: '{#
-00001190: 270d 0a20 2020 2020 2020 2020 2020 2076  '..            v
-000011a0: 6172 6961 626c 655f 656e 645f 7374 7269  ariable_end_stri
-000011b0: 6e67 3a20 277d 270d 0a20 2020 2020 2020  ng: '}'..       
-000011c0: 2020 2020 2076 6172 6961 626c 655f 7374       variable_st
-000011d0: 6172 745f 7374 7269 6e67 3a20 247b 0d0a  art_string: ${..
-000011e0: 2020 2020 2020 2020 7374 6174 6963 5f66          static_f
-000011f0: 6f72 6d61 743a 0d0a 2020 2020 2020 2020  ormat:..        
-00001200: 2d20 7675 650d 0a20 2020 2020 2020 202d  - vue..        -
-00001210: 2068 746d 6c0d 0a20 2020 2069 3138 6e3a   html..    i18n:
-00001220: 0d0a 2020 2020 2020 2020 6c61 6e67 3a20  ..        lang: 
-00001230: 5b27 7a68 275d 0d0a 2020 2020 2020 2020  ['zh']..        
-00001240: 7572 6c5f 6c61 6e67 5f6b 6579 3a20 276c  url_lang_key: 'l
-00001250: 616e 6727 0d0a 6060 600d 0a23 2320 5461  ang'..```..## Ta
-00001260: 6b65 2061 206c 6f6f 6b20 636f 6e74 726f  ke a look contro
-00001270: 6c6c 6572 2066 696c 6520 0d0a 200d 0a60  ller file .. ..`
-00001280: 6060 7079 7468 6f6e 0d0a 2020 2020 6672  ``python..    fr
-00001290: 6f6d 2069 7261 696c 7320 696d 706f 7274  om irails import
-000012a0: 2061 7069 5f72 6f75 7465 722c 6170 692c   api_router,api,
-000012b0: 5265 7175 6573 742c 5265 7370 6f6e 7365  Request,Response
-000012c0: 2c42 6173 6543 6f6e 7472 6f6c 6c65 722c  ,BaseController,
-000012d0: 6170 706c 6963 6174 696f 6e0d 0a20 0d0a  application.. ..
-000012e0: 2020 2020 4061 7069 5f72 6f75 7465 7228      @api_router(
-000012f0: 7061 7468 3d27 2f7b 636f 6e74 726f 6c6c  path='/{controll
-00001300: 6572 7d27 2c61 7574 683d 276e 6f6e 6527  er}',auth='none'
-00001310: 290d 0a20 2020 2063 6c61 7373 2041 646d  )..    class Adm
-00001320: 696e 436f 6e74 726f 6c6c 6572 2842 6173  inController(Bas
-00001330: 6543 6f6e 7472 6f6c 6c65 7229 3a20 0d0a  eController): ..
-00001340: 2020 2020 2020 2020 4061 7069 2e67 6574          @api.get
-00001350: 2822 2f69 6e64 6578 2229 0d0a 2020 2020  ("/index")..    
-00001360: 2020 2020 6465 6620 696e 6465 7828 7365      def index(se
-00001370: 6c66 293a 0d0a 2020 2020 2020 2020 2020  lf):..          
-00001380: 2020 2222 220d 0a20 2020 2020 2020 2020    """..         
-00001390: 2020 203a 7469 746c 6520 4164 6d69 6e0d     :title Admin.
-000013a0: 0a20 2020 2020 2020 2020 2020 2022 2222  .            """
-000013b0: 0d0a 2020 2020 2020 2020 2020 2020 7265  ..            re
-000013c0: 7475 726e 2073 656c 662e 7669 6577 2829  turn self.view()
-000013d0: 0d0a 6060 600d 0a                        ..```..
+00000000: 2320 6972 6169 6c73 0d0a 4120 6d76 6320  # irails..A mvc 
+00000010: 6672 616d 6577 6f72 6b20 7573 6564 2046  framework used F
+00000020: 6173 7441 7069 0d0a 5369 6d70 6c65 2061  astApi..Simple a
+00000030: 6e64 2065 6c65 6761 6e74 2075 7365 206f  nd elegant use o
+00000040: 6620 4661 7374 4170 6920 696e 204d 5643  f FastApi in MVC
+00000050: 206d 6f64 650d 0a0d 0a5b 446f 6373 5d28   mode....[Docs](
+00000060: 6874 7470 733a 2f2f 6972 6169 6c73 2e32  https://irails.2
+00000070: 7261 696c 732e 636e 2f29 200d 0a23 2057  rails.cn/) ..# W
+00000080: 656c 636f 6d65 2074 6f20 4952 4149 4c53  elcome to IRAILS
+00000090: 2870 7974 686f 6e20 6f6e 2072 6169 6c73  (python on rails
+000000a0: 290d 0a0d 0a20 0d0a 0d0a 2323 2049 6e73  ).... ....## Ins
+000000b0: 7461 6c6c 6174 696f 6e20 200d 0a0d 0a2a  tallation  ....*
+000000c0: 2060 7069 7020 696e 7374 616c 6c20 6972   `pip install ir
+000000d0: 6169 6c73 6020 2d20 696e 7374 616c 6c20  ails` - install 
+000000e0: 6972 6169 6c73 0d0a 0d0a 2323 2043 6f6d  irails....## Com
+000000f0: 6d61 6e64 730d 0a0d 0a2a 2060 6972 6169  mands....* `irai
+00000100: 6c73 2070 726f 6a65 6374 205b 7072 6f6a  ls project [proj
+00000110: 6563 742d 6e61 6d65 2864 6972 2d6e 616d  ect-name(dir-nam
+00000120: 6529 5d60 2020 2020 2020 2020 202d 2043  e)]`         - C
+00000130: 7265 6174 6520 6120 6e65 7720 6972 6169  reate a new irai
+00000140: 6c73 2070 726f 6a65 6374 2e0d 0a2a 2060  ls project...* `
+00000150: 6972 6169 6c73 2061 7070 205b 6170 702d  irails app [app-
+00000160: 6e61 6d65 2863 686f 6f73 6520 6f72 2069  name(choose or i
+00000170: 6e70 7574 2061 7070 7320 6469 7229 5d60  nput apps dir)]`
+00000180: 202d 2045 7861 6d70 6c65 3a20 6069 7261   - Example: `ira
+00000190: 696c 7320 6170 7020 6164 6d69 7373 696f  ils app admissio
+000001a0: 6e73 6020 4372 6561 7465 2061 206e 6577  ns` Create a new
+000001b0: 2069 7261 696c 7320 6170 702e 0d0a 2a20   irails app...* 
+000001c0: 6069 7261 696c 7320 7275 6e20 5b2d 2d68  `irails run [--h
+000001d0: 6f73 7420 686f 7374 5d20 5b2d 2d70 6f72  ost host] [--por
+000001e0: 7420 706f 7274 5d60 2020 2020 2020 2020  t port]`        
+000001f0: 2020 2d20 5275 6e20 7072 6f6a 6563 7420    - Run project 
+00000200: 7669 7369 7420 6f6e 205b 6874 7470 3a2f  visit on [http:/
+00000210: 2f31 3237 2e30 2e30 2e31 3a38 3030 303e  /127.0.0.1:8000>
+00000220: 5d28 6874 7470 3a2f 2f31 3237 2e30 2e30  ](http://127.0.0
+00000230: 2e31 3a38 3030 3029 2e20 0d0a 2a20 6069  .1:8000). ..* `i
+00000240: 7261 696c 7320 636f 6e74 726f 6c6c 6572  rails controller
+00000250: 205b 6163 7469 6f6e 732e 2e2e 5d60 2020   [actions...]`  
+00000260: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000270: 2d20 6765 6e65 7261 7465 2061 2063 6f6e  - generate a con
+00000280: 7472 6f6c 6c65 7220 7769 7468 2067 6976  troller with giv
+00000290: 656e 2061 6374 696f 6e73 2869 6620 6e6f  en actions(if no
+000002a0: 2067 6976 656e 2c64 6566 616c 7574 2069   given,defalut i
+000002b0: 7320 2a2a 696e 6465 782a 2a29 2e20 0d0a  s **index**). ..
+000002c0: 200d 0a0d 0a23 2320 5072 6f6a 6563 7420   ....## Project 
+000002d0: 6c61 796f 7574 0d0a 6060 600d 0a20 0d0a  layout..```.. ..
+000002e0: 2020 2020 7c20 2020 6d61 696e 2e70 790d      |   main.py.
+000002f0: 0a20 2020 202b 2d2d 2d61 7070 7320 2020  .    +---apps   
+00000300: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000310: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
+00000320: 4170 7073 2063 6f6e 7461 696e 6572 2028  Apps container (
+00000330: 4120 7072 6f6a 6563 7420 6361 6e20 6861  A project can ha
+00000340: 7665 206d 756c 7469 706c 6520 636f 6e74  ve multiple cont
+00000350: 6169 6e65 7273 290d 0a20 2020 207c 2020  ainers)..    |  
+00000360: 202b 2d2d 2d61 646d 6973 7369 6f6e 7320   +---admissions 
+00000370: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000380: 2020 2020 2023 2320 4170 7020 6469 7220       ## App dir 
+00000390: 2841 6e20 6170 706c 6963 6174 696f 6e20  (An application 
+000003a0: 636f 6e74 6169 6e65 7220 6361 6e20 6861  container can ha
+000003b0: 7665 206d 756c 7469 706c 6520 6170 706c  ve multiple appl
+000003c0: 6963 6174 696f 6e73 290d 0a20 2020 207c  ications)..    |
+000003d0: 2020 207c 2020 207c 2020 205f 5f69 6e69     |   |   __ini
+000003e0: 745f 5f2e 7079 2020 2020 2020 2020 2020  t__.py          
+000003f0: 2020 2020 2020 200d 0a20 2020 207c 2020         ..    |  
+00000400: 207c 2020 202b 2d2d 2d63 6f6e 7472 6f6c   |   +---control
+00000410: 6c65 7273 2020 2020 2020 2020 2020 2020  lers            
+00000420: 2020 2020 2023 2320 436f 6e74 726f 6c6c       ## Controll
+00000430: 6572 2066 696c 6573 0d0a 2020 2020 7c20  er files..    | 
+00000440: 2020 7c20 2020 7c20 2020 7c20 2020 686f    |   |   |   ho
+00000450: 6d65 5f63 6f6e 7472 6f6c 6c65 722e 7079  me_controller.py
+00000460: 2020 2020 2020 2323 2043 6f6e 7472 6f6c        ## Control
+00000470: 6c65 7220 636c 6173 7320 6669 6c65 2c69  ler class file,i
+00000480: 7427 7320 6c6f 6f6b 206c 696b 6520 6063  t's look like `c
+00000490: 6c61 7373 2048 6f6d 6543 6f6e 7472 6f6c  lass HomeControl
+000004a0: 6c65 7260 0d0a 2020 2020 7c20 2020 7c20  ler`..    |   | 
+000004b0: 2020 7c20 2020 7c20 2020 5f5f 696e 6974    |   |   __init
+000004c0: 5f5f 2e70 790d 0a20 2020 207c 2020 207c  __.py..    |   |
+000004d0: 2020 202b 2d2d 2d6c 6f63 616c 6573 2020     +---locales  
+000004e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000004f0: 2020 2023 2320 4931 386e 206c 6f63 616c     ## I18n local
+00000500: 6573 2064 6972 2c75 7365 2063 6f6d 6d61  es dir,use comma
+00000510: 6e64 2060 6170 7073 2f61 7070 3a24 2069  nd `apps/app:$ i
+00000520: 7261 6c69 7320 6931 386e 2067 6574 7465  ralis i18n gette
+00000530: 7874 6020 7769 6c6c 2061 7574 6f20 6765  xt` will auto ge
+00000540: 6e65 7261 7465 2069 7465 6d73 0d0a 2020  nerate items..  
+00000550: 2020 7c20 2020 7c20 2020 2b2d 2d2d 6d6f    |   |   +---mo
+00000560: 6465 6c73 2020 2020 2020 2020 2020 2020  dels            
+00000570: 2020 2020 2020 2020 2020 2323 2044 6174            ## Dat
+00000580: 6162 6173 6520 6d6f 6465 6c73 2066 696c  abase models fil
+00000590: 6573 2869 6620 796f 7520 7573 6520 736f  es(if you use so
+000005a0: 6d65 2064 6174 6162 6173 6520 7375 7070  me database supp
+000005b0: 6f72 7429 0d0a 2020 2020 7c20 2020 7c20  ort)..    |   | 
+000005c0: 2020 7c20 2020 2020 2020 5f5f 696e 6974    |       __init
+000005d0: 5f5f 2e70 790d 0a20 2020 207c 2020 207c  __.py..    |   |
+000005e0: 2020 202b 2d2d 2d73 6572 7669 6365 7320     +---services 
+000005f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000600: 2020 2023 2320 4d6f 6475 6c65 2066 6f72     ## Module for
+00000610: 2062 7573 696e 6573 7320 6c6f 6769 6320   business logic 
+00000620: 7072 6f63 6573 7369 6e67 0d0a 2020 2020  processing..    
+00000630: 7c20 2020 7c20 2020 2b2d 2d2d 7465 7374  |   |   +---test
+00000640: 7320 2020 2020 2020 2020 2020 2020 2020  s               
+00000650: 2020 2020 2020 2020 2323 2055 6e69 7420          ## Unit 
+00000660: 7465 7374 7469 6e67 0d0a 2020 2020 7c20  testting..    | 
+00000670: 2020 7c20 2020 2b2d 2d2d 7669 6577 7320    |   +---views 
+00000680: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000690: 2020 2020 2020 2323 2053 7461 7469 6320        ## Static 
+000006a0: 7669 6577 2066 696c 6573 2028 7573 6520  view files (use 
+000006b0: 604a 696e 6a61 3260 2054 656d 706c 6174  `Jinja2` Templat
+000006c0: 6529 0d0a 2020 2020 7c20 2020 7c20 2020  e)..    |   |   
+000006d0: 7c20 2020 7c20 2020 6c61 796f 7574 2e68  |   |   layout.h
+000006e0: 746d 6c0d 0a20 2020 207c 2020 207c 2020  tml..    |   |  
+000006f0: 207c 2020 207c 0d0a 2020 2020 7c20 2020   |   |..    |   
+00000700: 7c20 2020 7c20 2020 2b2d 2d2d 686f 6d65  |   |   +---home
+00000710: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000720: 2020 2020 2323 2054 6865 2063 6f6e 7472      ## The contr
+00000730: 6f6c 6c65 7220 6163 7469 6f6e 2773 2073  oller action's s
+00000740: 7461 7469 6320 6669 6c65 286e 616d 6520  tatic file(name 
+00000750: 6973 2073 616d 6520 746f 2074 6865 2063  is same to the c
+00000760: 6f6e 7472 6f6c 6c65 7227 7320 636c 6173  ontroller's clas
+00000770: 7320 6e61 6d65 290d 0a20 2020 207c 2020  s name)..    |  
+00000780: 207c 2020 207c 2020 207c 2020 2020 2020   |   |   |      
+00000790: 2068 6f6d 652e 6373 7320 2020 2020 2020   home.css       
+000007a0: 2020 2020 200d 0a20 2020 207c 2020 207c       ..    |   |
+000007b0: 2020 207c 2020 207c 2020 2020 2020 2068     |   |       h
+000007c0: 6f6d 652e 6874 6d6c 2020 2020 2020 2020  ome.html        
+000007d0: 2020 2023 2320 5374 6174 6963 2066 696c     ## Static fil
+000007e0: 6520 636f 7272 6573 706f 6e64 696e 6720  e corresponding 
+000007f0: 746f 2061 6374 696f 6e28 6e61 6d65 2069  to action(name i
+00000800: 7320 7361 6d65 2074 6f20 7468 6520 636f  s same to the co
+00000810: 6e74 726f 6c6c 6572 2773 206d 6574 686f  ntroller's metho
+00000820: 6420 6e61 6d65 290d 0a20 2020 202b 2d2d  d name)..    +--
+00000830: 2d63 6f6e 6669 6773 2020 2020 2020 2020  -configs        
+00000840: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000850: 2020 2020 2023 2320 5072 6f6a 6563 7420       ## Project 
+00000860: 636f 6e66 6967 7572 6520 6469 720d 0a20  configure dir.. 
+00000870: 2020 207c 2020 2020 2020 2061 6c65 6d62     |       alemb
+00000880: 6963 2e69 6e69 2020 2020 2020 2020 2020  ic.ini          
+00000890: 2020 2020 2020 2020 2020 2023 2320 416c             ## Al
+000008a0: 656d 6269 6320 636f 6e66 6967 7572 6520  embic configure 
+000008b0: 6669 6c65 2028 4765 6e65 7261 6c6c 792c  file (Generally,
+000008c0: 2074 6865 7265 2069 7320 6e6f 206e 6565   there is no nee
+000008d0: 6420 746f 2063 6861 6e67 652c 2075 7365  d to change, use
+000008e0: 6420 7468 6520 6461 7461 6261 7365 206d  d the database m
+000008f0: 6967 7261 7469 6f6e 290d 0a20 2020 207c  igration)..    |
+00000900: 2020 2020 2020 2063 6173 6269 6e2d 6164         casbin-ad
+00000910: 6170 7465 722e 6373 7620 2020 2020 2020  apter.csv       
+00000920: 2020 2020 2020 2023 2320 4361 7362 696e         ## Casbin
+00000930: 2061 7574 6820 6d6f 6475 6c65 2063 6f6e   auth module con
+00000940: 6669 6720 6164 6170 7465 7220 6669 6c65  fig adapter file
+00000950: 2829 0d0a 2020 2020 7c20 2020 2020 2020  ()..    |       
+00000960: 6361 7362 696e 2d6d 6f64 656c 2e63 6f6e  casbin-model.con
+00000970: 6620 2020 2020 2020 2020 2020 2020 2020  f               
+00000980: 2323 2043 6173 6269 6e20 6175 7468 2063  ## Casbin auth c
+00000990: 6f6e 6669 6720 6d6f 6465 6c0d 0a20 2020  onfig model..   
+000009a0: 207c 2020 2020 2020 2064 6174 6162 6173   |       databas
+000009b0: 652e 7961 6d6c 2020 2020 2020 2020 2020  e.yaml          
+000009c0: 2020 2020 2020 2020 2023 2320 436f 6e66           ## Conf
+000009d0: 6967 7572 6520 666f 7220 6461 7461 6261  igure for databa
+000009e0: 7365 2073 7570 706f 7274 0d0a 2020 2020  se support..    
+000009f0: 7c20 2020 2020 2020 6765 6e65 7261 6c2e  |       general.
+00000a00: 7961 6d6c 2020 2020 2020 2020 2020 2020  yaml            
+00000a10: 2020 2020 2020 2020 2323 2047 656e 6572          ## Gener
+00000a20: 616c 2063 6f6e 6669 6775 7265 730d 0a20  al configures.. 
+00000a30: 2020 207c 2020 2020 2020 2073 6573 7369     |       sessi
+00000a40: 6f6e 2e79 616d 6c20 2020 2020 2020 2020  on.yaml         
+00000a50: 2020 2020 2020 2020 2020 2023 2320 5365             ## Se
+00000a60: 7373 696f 6e20 636f 6e66 6967 7572 6573  ssion configures
+00000a70: 0d0a 2020 2020 7c0d 0a20 2020 202b 2d2d  ..    |..    +--
+00000a80: 2d64 6174 610d 0a20 2020 207c 2020 202b  -data..    |   +
+00000a90: 2d2d 2d61 6c65 6d62 6963 0d0a 2020 2020  ---alembic..    
+00000aa0: 7c20 2020 7c20 2020 5c2d 2d2d 7665 7273  |   |   \---vers
+00000ab0: 696f 6e73 0d0a 2020 2020 7c20 2020 5c2d  ions..    |   \-
+00000ac0: 2d2d 6462 0d0a 2020 2020 7c0d 0a20 2020  --db..    |..   
+00000ad0: 202b 2d2d 2d70 7562 6c69 6320 2020 2020   +---public     
+00000ae0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000af0: 2020 2020 2020 2020 2023 2320 5075 626c           ## Publ
+00000b00: 6963 2064 6972 2028 7769 6c6c 206d 6f75  ic dir (will mou
+00000b10: 6e74 6564 2074 6f20 7468 6520 272f 7075  nted to the '/pu
+00000b20: 626c 6963 2720 7572 6c29 0d0a 2020 2020  blic' url)..    
+00000b30: 7c20 2020 7c20 2020 6572 726f 725f 3430  |   |   error_40
+00000b40: 342e 6874 6d6c 2020 2020 2020 2020 2020  4.html          
+00000b50: 2020 2020 2020 2020 2323 2045 7272 6f72          ## Error
+00000b60: 2070 6167 6520 2e2e 2e0d 0a20 2020 207c   page .....    |
+00000b70: 2020 207c 2020 2065 7272 6f72 5f35 3030     |   error_500
+00000b80: 2e68 746d 6c0d 0a20 2020 207c 0d0a 2020  .html..    |..  
+00000b90: 2020 2b2d 2d2d 7570 6c6f 6164 7320 2020    +---uploads   
+00000ba0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000bb0: 2020 2020 2020 2020 2020 2323 204f 7468            ## Oth
+00000bc0: 6572 7320 6469 7228 6966 2079 6f75 7220  ers dir(if your 
+00000bd0: 6e65 6564 206f 7220 6e6f 7429 0d0a 6060  need or not)..``
+00000be0: 600d 0a23 2320 4578 7472 6173 2063 6f6d  `..## Extras com
+00000bf0: 6d61 6e64 730d 0a2a 2060 6972 6169 6c73  mands..* `irails
+00000c00: 2069 3138 6e20 6765 7474 6578 7460 2020   i18n gettext`  
+00000c10: 2d2d 6765 6e65 7261 7465 2069 3138 6e20  --generate i18n 
+00000c20: 696e 2069 7261 696c 7320 6170 7020 6469  in irails app di
+00000c30: 720d 0a2a 2060 6972 6169 6c73 2073 6865  r..* `irails she
+00000c40: 6c6c 6020 2020 2020 2020 2020 2d2d 7275  ll`         --ru
+00000c50: 6e20 7079 7468 6f6e 2069 6e74 6572 7072  n python interpr
+00000c60: 6574 6572 2077 6974 6820 6275 696c 6469  eter with buildi
+00000c70: 6e20 7375 7070 6f72 7420 636f 6e74 6578  n support contex
+00000c80: 7473 200d 0a0d 0a23 2320 5461 6b65 2061  ts ....## Take a
+00000c90: 206c 6f6f 6b20 636f 6e66 6967 7572 6520   look configure 
+00000ca0: 6669 6c65 2060 6765 6e65 7261 6c2e 7961  file `general.ya
+00000cb0: 6d6c 600d 0a20 0d0a 6060 6020 0d0a 2020  ml`.. ..``` ..  
+00000cc0: 2020 6170 703a 0d0a 2020 2020 2020 2020    app:..        
+00000cd0: 6170 7064 6972 3a0d 0a20 2020 2020 2020  appdir:..       
+00000ce0: 202d 2061 7070 730d 0a20 2020 2020 2020   - apps..       
+00000cf0: 2065 6e61 626c 6564 3a20 6e75 6c6c 0d0a   enabled: null..
+00000d00: 2020 2020 726f 6f74 3a20 6170 7073 2e72      root: apps.r
+00000d10: 6f6f 740d 0a0d 0a20 2020 2063 6f72 733a  oot....    cors:
+00000d20: 0d0a 2020 2020 2020 2020 616c 6c6f 775f  ..        allow_
+00000d30: 6372 6564 656e 7469 616c 733a 2074 7275  credentials: tru
+00000d40: 650d 0a20 2020 2020 2020 2061 6c6c 6f77  e..        allow
+00000d50: 5f68 6561 6465 7273 3a0d 0a20 2020 2020  _headers:..     
+00000d60: 2020 2020 2020 202d 2027 2a27 0d0a 2020         - '*'..  
+00000d70: 2020 2020 2020 616c 6c6f 775f 6d65 7468        allow_meth
+00000d80: 6f64 733a 0d0a 2020 2020 2020 2020 2020  ods:..          
+00000d90: 2020 2d20 272a 270d 0a20 2020 2020 2020    - '*'..       
+00000da0: 2061 6c6c 6f77 5f6f 7269 6769 6e73 3a0d   allow_origins:.
+00000db0: 0a20 2020 2020 2020 2020 2020 202d 2027  .            - '
+00000dc0: 2a27 0d0a 2020 2020 6465 6275 673a 2074  *'..    debug: t
+00000dd0: 7275 650d 0a20 2020 2065 7272 6f72 733a  rue..    errors:
+00000de0: 0d0a 2020 2020 2020 2020 6572 726f 725f  ..        error_
+00000df0: 3430 345f 7061 6765 3a20 277b 524f 4f54  404_page: '{ROOT
+00000e00: 2e70 7562 6c69 635f 6469 727d 2f65 7272  .public_dir}/err
+00000e10: 6f72 5f34 3034 2e68 746d 6c27 0d0a 2020  or_404.html'..  
+00000e20: 2020 2020 2020 6572 726f 725f 3530 305f        error_500_
+00000e30: 7061 6765 3a20 277b 524f 4f54 2e70 7562  page: '{ROOT.pub
+00000e40: 6c69 635f 6469 727d 2f65 7272 6f72 5f35  lic_dir}/error_5
+00000e50: 3030 2e68 746d 6c27 0d0a 2020 2020 6c6f  00.html'..    lo
+00000e60: 673a 0d0a 2020 2020 2020 2020 6669 6c65  g:..        file
+00000e70: 3a20 2727 0d0a 2020 2020 2020 2020 6c65  : ''..        le
+00000e80: 7665 6c3a 2044 4542 5547 0d0a 2020 2020  vel: DEBUG..    
+00000e90: 2020 2020 6e61 6d65 3a20 6952 6169 6c73      name: iRails
+00000ea0: 0d0a 2020 2020 7075 626c 6963 5f64 6972  ..    public_dir
+00000eb0: 3a20 2e2f 7075 626c 6963 0d0a 0d0a 2020  : ./public....  
+00000ec0: 2020 7669 6577 3a0d 0a20 2020 2020 2020    view:..       
+00000ed0: 206a 696e 6a61 323a 0d0a 2020 2020 2020   jinja2:..      
+00000ee0: 2020 2020 2020 626c 6f63 6b5f 656e 645f        block_end_
+00000ef0: 7374 7269 6e67 3a20 2725 7d27 0d0a 2020  string: '%}'..  
+00000f00: 2020 2020 2020 2020 2020 626c 6f63 6b5f            block_
+00000f10: 7374 6172 745f 7374 7269 6e67 3a20 277b  start_string: '{
+00000f20: 2527 0d0a 2020 2020 2020 2020 2020 2020  %'..            
+00000f30: 636f 6d6d 656e 745f 656e 645f 7374 7269  comment_end_stri
+00000f40: 6e67 3a20 2723 7d27 0d0a 2020 2020 2020  ng: '#}'..      
+00000f50: 2020 2020 2020 636f 6d6d 656e 745f 7374        comment_st
+00000f60: 6172 745f 7374 7269 6e67 3a20 277b 2327  art_string: '{#'
+00000f70: 0d0a 2020 2020 2020 2020 2020 2020 7661  ..            va
+00000f80: 7269 6162 6c65 5f65 6e64 5f73 7472 696e  riable_end_strin
+00000f90: 673a 2027 7d27 0d0a 2020 2020 2020 2020  g: '}'..        
+00000fa0: 2020 2020 7661 7269 6162 6c65 5f73 7461      variable_sta
+00000fb0: 7274 5f73 7472 696e 673a 2024 7b0d 0a20  rt_string: ${.. 
+00000fc0: 2020 2020 2020 2073 7461 7469 635f 666f         static_fo
+00000fd0: 726d 6174 3a0d 0a20 2020 2020 2020 202d  rmat:..        -
+00000fe0: 2076 7565 0d0a 2020 2020 2020 2020 2d20   vue..        - 
+00000ff0: 6874 6d6c 0d0a 2020 2020 6931 386e 3a0d  html..    i18n:.
+00001000: 0a20 2020 2020 2020 206c 616e 673a 205b  .        lang: [
+00001010: 277a 6827 5d0d 0a20 2020 2020 2020 2075  'zh']..        u
+00001020: 726c 5f6c 616e 675f 6b65 793a 2027 6c61  rl_lang_key: 'la
+00001030: 6e67 270d 0a60 6060 0d0a 2323 2054 616b  ng'..```..## Tak
+00001040: 6520 6120 6c6f 6f6b 2063 6f6e 7472 6f6c  e a look control
+00001050: 6c65 7220 6669 6c65 200d 0a20 0d0a 6060  ler file .. ..``
+00001060: 6070 7974 686f 6e0d 0a20 2020 2066 726f  `python..    fro
+00001070: 6d20 6972 6169 6c73 2069 6d70 6f72 7420  m irails import 
+00001080: 6170 695f 726f 7574 6572 2c61 7069 2c52  api_router,api,R
+00001090: 6571 7565 7374 2c52 6573 706f 6e73 652c  equest,Response,
+000010a0: 4261 7365 436f 6e74 726f 6c6c 6572 2c61  BaseController,a
+000010b0: 7070 6c69 6361 7469 6f6e 0d0a 200d 0a20  pplication.. .. 
+000010c0: 2020 2040 6170 695f 726f 7574 6572 2870     @api_router(p
+000010d0: 6174 683d 272f 7b63 6f6e 7472 6f6c 6c65  ath='/{controlle
+000010e0: 727d 272c 6175 7468 3d27 6e6f 6e65 2729  r}',auth='none')
+000010f0: 0d0a 2020 2020 636c 6173 7320 4164 6d69  ..    class Admi
+00001100: 6e43 6f6e 7472 6f6c 6c65 7228 4261 7365  nController(Base
+00001110: 436f 6e74 726f 6c6c 6572 293a 200d 0a20  Controller): .. 
+00001120: 2020 2020 2020 2040 6170 692e 6765 7428         @api.get(
+00001130: 222f 696e 6465 7822 290d 0a20 2020 2020  "/index")..     
+00001140: 2020 2064 6566 2069 6e64 6578 2873 656c     def index(sel
+00001150: 6629 3a0d 0a20 2020 2020 2020 2020 2020  f):..           
+00001160: 2022 2222 0d0a 2020 2020 2020 2020 2020   """..          
+00001170: 2020 3a74 6974 6c65 2041 646d 696e 0d0a    :title Admin..
+00001180: 2020 2020 2020 2020 2020 2020 2222 220d              """.
+00001190: 0a20 2020 2020 2020 2020 2020 2072 6574  .            ret
+000011a0: 7572 6e20 7365 6c66 2e76 6965 7728 290d  urn self.view().
+000011b0: 0a60 6060                                .```
```

### Comparing `irails-1.3.5/README.md` & `irails-1.3.6/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,269 +1,333 @@
-00000000: 2320 6972 6169 6c73 0d0a 4120 6d76 6320  # irails..A mvc 
-00000010: 6672 616d 6577 6f72 6b20 7573 6564 2046  framework used F
-00000020: 6173 7441 7069 0d0a 5369 6d70 6c65 2061  astApi..Simple a
-00000030: 6e64 2065 6c65 6761 6e74 2075 7365 206f  nd elegant use o
-00000040: 6620 4661 7374 4170 6920 696e 204d 5643  f FastApi in MVC
-00000050: 206d 6f64 650d 0a0d 0a5b 4465 6d6f 5d28   mode....[Demo](
-00000060: 6874 7470 733a 2f2f 6972 6169 6c73 2e32  https://irails.2
-00000070: 7261 696c 732e 636e 2f29 200d 0a23 2057  rails.cn/) ..# W
-00000080: 656c 636f 6d65 2074 6f20 4952 4149 4c53  elcome to IRAILS
-00000090: 2870 7974 686f 6e20 6f6e 2072 6169 6c73  (python on rails
-000000a0: 290d 0a0d 0a20 0d0a 0d0a 2323 2049 6e73  ).... ....## Ins
-000000b0: 7461 6c6c 6174 696f 6e20 200d 0a0d 0a2a  tallation  ....*
-000000c0: 2060 7069 7020 696e 7374 616c 6c20 6972   `pip install ir
-000000d0: 6169 6c73 6020 2d20 696e 7374 616c 6c20  ails` - install 
-000000e0: 6972 6169 6c73 0d0a 0d0a 2323 2043 6f6d  irails....## Com
-000000f0: 6d61 6e64 730d 0a0d 0a2a 2060 6972 6169  mands....* `irai
-00000100: 6c73 2070 726f 6a65 6374 205b 7072 6f6a  ls project [proj
-00000110: 6563 742d 6e61 6d65 2864 6972 2d6e 616d  ect-name(dir-nam
-00000120: 6529 5d60 202d 2043 7265 6174 6520 6120  e)]` - Create a 
-00000130: 6e65 7720 6972 6169 6c73 2070 726f 6a65  new irails proje
-00000140: 6374 2e0d 0a2a 2060 6972 6169 6c73 2061  ct...* `irails a
-00000150: 7070 205b 6170 702d 6e61 6d65 2863 686f  pp [app-name(cho
-00000160: 6f73 6520 6f72 2069 6e70 7574 2061 7070  ose or input app
-00000170: 7320 6469 7229 5d60 202d 2045 7861 6d70  s dir)]` - Examp
-00000180: 6c65 3a20 6069 7261 696c 7320 6170 7020  le: `irails app 
-00000190: 6164 6d69 7373 696f 6e73 6020 4372 6561  admissions` Crea
-000001a0: 7465 2061 206e 6577 2069 7261 696c 7320  te a new irails 
-000001b0: 6170 702e 0d0a 2a20 6069 7261 696c 7320  app...* `irails 
-000001c0: 7275 6e20 5b2d 2d70 6f72 7420 706f 7274  run [--port port
-000001d0: 5d60 202d 2052 756e 2070 726f 6a65 6374  ]` - Run project
-000001e0: 2076 6973 6974 206f 6e20 3c61 2068 7265   visit on <a hre
-000001f0: 663d 2268 7474 703a 2f2f 3132 372e 302e  f="http://127.0.
-00000200: 302e 313a 3830 3030 223e 6874 7470 3a2f  0.1:8000">http:/
-00000210: 2f31 3237 2e30 2e30 2e31 3a38 3030 303c  /127.0.0.1:8000<
-00000220: 2f61 3e2e 200d 0a20 0d0a 0d0a 2323 2050  /a>. .. ....## P
-00000230: 726f 6a65 6374 206c 6179 6f75 740d 0a60  roject layout..`
-00000240: 6060 0d0a 200d 0a20 2020 207c 2020 206d  ``.. ..    |   m
-00000250: 6169 6e2e 7079 0d0a 2020 2020 2b2d 2d2d  ain.py..    +---
-00000260: 6170 7073 2020 2020 2020 2020 2020 2020  apps            
-00000270: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000280: 2020 2020 2323 2041 7070 7320 636f 6e74      ## Apps cont
-00000290: 6169 6e65 7220 2841 2070 726f 6a65 6374  ainer (A project
-000002a0: 2063 616e 2068 6176 6520 6d75 6c74 6970   can have multip
-000002b0: 6c65 2063 6f6e 7461 696e 6572 7329 0d0a  le containers)..
-000002c0: 2020 2020 7c20 2020 2b2d 2d2d 6164 6d69      |   +---admi
-000002d0: 7373 696f 6e73 2020 2020 2020 2020 2020  ssions          
-000002e0: 2020 2020 2020 2020 2020 2020 2323 2041              ## A
-000002f0: 7070 2064 6972 2028 416e 2061 7070 6c69  pp dir (An appli
-00000300: 6361 7469 6f6e 2063 6f6e 7461 696e 6572  cation container
-00000310: 2063 616e 2068 6176 6520 6d75 6c74 6970   can have multip
-00000320: 6c65 2061 7070 6c69 6361 7469 6f6e 7329  le applications)
-00000330: 0d0a 2020 2020 7c20 2020 7c20 2020 7c20  ..    |   |   | 
-00000340: 2020 5f5f 696e 6974 5f5f 2e70 7920 2020    __init__.py   
-00000350: 2020 2020 2020 2020 2020 2020 2020 0d0a                ..
-00000360: 2020 2020 7c20 2020 7c20 2020 2b2d 2d2d      |   |   +---
-00000370: 636f 6e74 726f 6c6c 6572 7320 2020 2020  controllers     
-00000380: 2020 2020 2020 2020 2020 2020 2323 2043              ## C
-00000390: 6f6e 7472 6f6c 6c65 7220 6669 6c65 730d  ontroller files.
-000003a0: 0a20 2020 207c 2020 207c 2020 207c 2020  .    |   |   |  
-000003b0: 207c 2020 2068 6f6d 655f 636f 6e74 726f   |   home_contro
-000003c0: 6c6c 6572 2e70 7920 2020 2020 2023 2320  ller.py      ## 
-000003d0: 436f 6e74 726f 6c6c 6572 2063 6c61 7373  Controller class
-000003e0: 2066 696c 652c 6974 2773 206c 6f6f 6b20   file,it's look 
-000003f0: 6c69 6b65 2060 636c 6173 7320 486f 6d65  like `class Home
-00000400: 436f 6e74 726f 6c6c 6572 600d 0a20 2020  Controller`..   
-00000410: 207c 2020 207c 2020 207c 2020 207c 2020   |   |   |   |  
-00000420: 205f 5f69 6e69 745f 5f2e 7079 0d0a 2020   __init__.py..  
-00000430: 2020 7c20 2020 7c20 2020 2b2d 2d2d 6c6f    |   |   +---lo
-00000440: 6361 6c65 7320 2020 2020 2020 2020 2020  cales           
-00000450: 2020 2020 2020 2020 2020 2323 2049 3138            ## I18
-00000460: 6e20 6c6f 6361 6c65 7320 6469 722c 7573  n locales dir,us
-00000470: 6520 636f 6d6d 616e 6420 6061 7070 732f  e command `apps/
-00000480: 6170 703a 2420 6972 616c 6973 2069 3138  app:$ iralis i18
-00000490: 6e20 6765 7474 6578 7460 2077 696c 6c20  n gettext` will 
-000004a0: 6175 746f 2067 656e 6572 6174 6520 6974  auto generate it
-000004b0: 656d 730d 0a20 2020 207c 2020 207c 2020  ems..    |   |  
-000004c0: 202b 2d2d 2d6d 6f64 656c 7320 2020 2020   +---models     
-000004d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000004e0: 2023 2320 4461 7461 6261 7365 206d 6f64   ## Database mod
-000004f0: 656c 7320 6669 6c65 7328 6966 2079 6f75  els files(if you
-00000500: 2075 7365 2073 6f6d 6520 6461 7461 6261   use some databa
-00000510: 7365 2073 7570 706f 7274 290d 0a20 2020  se support)..   
-00000520: 207c 2020 207c 2020 207c 2020 2020 2020   |   |   |      
-00000530: 205f 5f69 6e69 745f 5f2e 7079 0d0a 2020   __init__.py..  
-00000540: 2020 7c20 2020 7c20 2020 2b2d 2d2d 7365    |   |   +---se
-00000550: 7276 6963 6573 2020 2020 2020 2020 2020  rvices          
-00000560: 2020 2020 2020 2020 2020 2323 204d 6f64            ## Mod
-00000570: 756c 6520 666f 7220 6275 7369 6e65 7373  ule for business
-00000580: 206c 6f67 6963 2070 726f 6365 7373 696e   logic processin
-00000590: 670d 0a20 2020 207c 2020 207c 2020 202b  g..    |   |   +
-000005a0: 2d2d 2d74 6573 7473 2020 2020 2020 2020  ---tests        
-000005b0: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-000005c0: 2320 556e 6974 2074 6573 7474 696e 670d  # Unit testting.
-000005d0: 0a20 2020 207c 2020 207c 2020 202b 2d2d  .    |   |   +--
-000005e0: 2d76 6965 7773 2020 2020 2020 2020 2020  -views          
-000005f0: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
-00000600: 5374 6174 6963 2076 6965 7720 6669 6c65  Static view file
-00000610: 7320 2875 7365 2060 4a69 6e6a 6132 6020  s (use `Jinja2` 
-00000620: 5465 6d70 6c61 7465 290d 0a20 2020 207c  Template)..    |
-00000630: 2020 207c 2020 207c 2020 207c 2020 206c     |   |   |   l
-00000640: 6179 6f75 742e 6874 6d6c 0d0a 2020 2020  ayout.html..    
-00000650: 7c20 2020 7c20 2020 7c20 2020 7c0d 0a20  |   |   |   |.. 
-00000660: 2020 207c 2020 207c 2020 207c 2020 202b     |   |   |   +
-00000670: 2d2d 2d68 6f6d 6520 2020 2020 2020 2020  ---home         
-00000680: 2020 2020 2020 2020 2020 2023 2320 5468             ## Th
-00000690: 6520 636f 6e74 726f 6c6c 6572 2061 6374  e controller act
-000006a0: 696f 6e27 7320 7374 6174 6963 2066 696c  ion's static fil
-000006b0: 6528 6e61 6d65 2069 7320 7361 6d65 2074  e(name is same t
-000006c0: 6f20 7468 6520 636f 6e74 726f 6c6c 6572  o the controller
-000006d0: 2773 2063 6c61 7373 206e 616d 6529 0d0a  's class name)..
-000006e0: 2020 2020 7c20 2020 7c20 2020 7c20 2020      |   |   |   
-000006f0: 7c20 2020 2020 2020 686f 6d65 2e63 7373  |       home.css
-00000700: 2020 2020 2020 2020 2020 2020 0d0a 2020              ..  
-00000710: 2020 7c20 2020 7c20 2020 7c20 2020 7c20    |   |   |   | 
-00000720: 2020 2020 2020 686f 6d65 2e68 746d 6c20        home.html 
-00000730: 2020 2020 2020 2020 2020 2323 2053 7461            ## Sta
-00000740: 7469 6320 6669 6c65 2063 6f72 7265 7370  tic file corresp
-00000750: 6f6e 6469 6e67 2074 6f20 6163 7469 6f6e  onding to action
-00000760: 286e 616d 6520 6973 2073 616d 6520 746f  (name is same to
-00000770: 2074 6865 2063 6f6e 7472 6f6c 6c65 7227   the controller'
-00000780: 7320 6d65 7468 6f64 206e 616d 6529 0d0a  s method name)..
-00000790: 2020 2020 2b2d 2d2d 636f 6e66 6967 7320      +---configs 
-000007a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000007b0: 2020 2020 2020 2020 2020 2020 2323 2050              ## P
-000007c0: 726f 6a65 6374 2063 6f6e 6669 6775 7265  roject configure
-000007d0: 2064 6972 0d0a 2020 2020 7c20 2020 2020   dir..    |     
-000007e0: 2020 616c 656d 6269 632e 696e 6920 2020    alembic.ini   
+00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
+00000010: 3a20 322e 310d 0a4e 616d 653a 2069 7261  : 2.1..Name: ira
+00000020: 696c 730d 0a56 6572 7369 6f6e 3a20 312e  ils..Version: 1.
+00000030: 332e 360d 0a53 756d 6d61 7279 3a20 5369  3.6..Summary: Si
+00000040: 6d70 6c65 2061 6e64 2065 6c65 6761 6e74  mple and elegant
+00000050: 2075 7365 206f 6620 4661 7374 4170 6920   use of FastApi 
+00000060: 696e 204d 5643 206d 6f64 650d 0a48 6f6d  in MVC mode..Hom
+00000070: 652d 7061 6765 3a20 6874 7470 733a 2f2f  e-page: https://
+00000080: 6769 7468 7562 2e63 6f6d 2f73 6d6a 6b7a  github.com/smjkz
+00000090: 736c 2f69 7261 696c 730d 0a41 7574 686f  sl/irails..Autho
+000000a0: 723a 2042 7275 6365 2063 686f 750d 0a41  r: Bruce chou..A
+000000b0: 7574 686f 722d 656d 6169 6c3a 2073 6d6a  uthor-email: smj
+000000c0: 6b7a 736c 4067 6d61 696c 2e63 6f6d 0d0a  kzsl@gmail.com..
+000000d0: 4c69 6365 6e73 653a 2041 7061 6368 6520  License: Apache 
+000000e0: 4c69 6365 6e73 6520 322e 300d 0a4b 6579  License 2.0..Key
+000000f0: 776f 7264 733a 2077 6562 2066 7261 6d65  words: web frame
+00000100: 776f 726b 2c6d 7663 2066 7261 6d65 776f  work,mvc framewo
+00000110: 726b 2c66 6173 7461 7069 2066 7261 6d65  rk,fastapi frame
+00000120: 776f 726b 0d0a 436c 6173 7369 6669 6572  work..Classifier
+00000130: 3a20 4c69 6365 6e73 6520 3a3a 204f 5349  : License :: OSI
+00000140: 2041 7070 726f 7665 6420 3a3a 2041 7061   Approved :: Apa
+00000150: 6368 6520 536f 6674 7761 7265 204c 6963  che Software Lic
+00000160: 656e 7365 0d0a 436c 6173 7369 6669 6572  ense..Classifier
+00000170: 3a20 4f70 6572 6174 696e 6720 5379 7374  : Operating Syst
+00000180: 656d 203a 3a20 4f53 2049 6e64 6570 656e  em :: OS Indepen
+00000190: 6465 6e74 0d0a 436c 6173 7369 6669 6572  dent..Classifier
+000001a0: 3a20 5072 6f67 7261 6d6d 696e 6720 4c61  : Programming La
+000001b0: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
+000001c0: 203a 3a20 332e 360d 0a43 6c61 7373 6966   :: 3.6..Classif
+000001d0: 6965 723a 2050 726f 6772 616d 6d69 6e67  ier: Programming
+000001e0: 204c 616e 6775 6167 6520 3a3a 2050 7974   Language :: Pyt
+000001f0: 686f 6e20 3a3a 2033 2e37 0d0a 436c 6173  hon :: 3.7..Clas
+00000200: 7369 6669 6572 3a20 5072 6f67 7261 6d6d  sifier: Programm
+00000210: 696e 6720 4c61 6e67 7561 6765 203a 3a20  ing Language :: 
+00000220: 5079 7468 6f6e 203a 3a20 332e 380d 0a43  Python :: 3.8..C
+00000230: 6c61 7373 6966 6965 723a 2050 726f 6772  lassifier: Progr
+00000240: 616d 6d69 6e67 204c 616e 6775 6167 6520  amming Language 
+00000250: 3a3a 2050 7974 686f 6e20 3a3a 2033 2e39  :: Python :: 3.9
+00000260: 0d0a 436c 6173 7369 6669 6572 3a20 5072  ..Classifier: Pr
+00000270: 6f67 7261 6d6d 696e 6720 4c61 6e67 7561  ogramming Langua
+00000280: 6765 203a 3a20 5079 7468 6f6e 203a 3a20  ge :: Python :: 
+00000290: 332e 3130 0d0a 436c 6173 7369 6669 6572  3.10..Classifier
+000002a0: 3a20 5072 6f67 7261 6d6d 696e 6720 4c61  : Programming La
+000002b0: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
+000002c0: 203a 3a20 332e 3131 0d0a 5265 7175 6972   :: 3.11..Requir
+000002d0: 6573 2d50 7974 686f 6e3a 203e 3d33 2e36  es-Python: >=3.6
+000002e0: 0d0a 4465 7363 7269 7074 696f 6e2d 436f  ..Description-Co
+000002f0: 6e74 656e 742d 5479 7065 3a20 7465 7874  ntent-Type: text
+00000300: 2f6d 6172 6b64 6f77 6e0d 0a0d 0a23 2069  /markdown....# i
+00000310: 7261 696c 730d 0a41 206d 7663 2066 7261  rails..A mvc fra
+00000320: 6d65 776f 726b 2075 7365 6420 4661 7374  mework used Fast
+00000330: 4170 690d 0a53 696d 706c 6520 616e 6420  Api..Simple and 
+00000340: 656c 6567 616e 7420 7573 6520 6f66 2046  elegant use of F
+00000350: 6173 7441 7069 2069 6e20 4d56 4320 6d6f  astApi in MVC mo
+00000360: 6465 0d0a 0d0a 5b44 6f63 735d 2868 7474  de....[Docs](htt
+00000370: 7073 3a2f 2f69 7261 696c 732e 3272 6169  ps://irails.2rai
+00000380: 6c73 2e63 6e2f 2920 0d0a 2320 5765 6c63  ls.cn/) ..# Welc
+00000390: 6f6d 6520 746f 2049 5241 494c 5328 7079  ome to IRAILS(py
+000003a0: 7468 6f6e 206f 6e20 7261 696c 7329 0d0a  thon on rails)..
+000003b0: 0d0a 200d 0a0d 0a23 2320 496e 7374 616c  .. ....## Instal
+000003c0: 6c61 7469 6f6e 2020 0d0a 0d0a 2a20 6070  lation  ....* `p
+000003d0: 6970 2069 6e73 7461 6c6c 2069 7261 696c  ip install irail
+000003e0: 7360 202d 2069 6e73 7461 6c6c 2069 7261  s` - install ira
+000003f0: 696c 730d 0a0d 0a23 2320 436f 6d6d 616e  ils....## Comman
+00000400: 6473 0d0a 0d0a 2a20 6069 7261 696c 7320  ds....* `irails 
+00000410: 7072 6f6a 6563 7420 5b70 726f 6a65 6374  project [project
+00000420: 2d6e 616d 6528 6469 722d 6e61 6d65 295d  -name(dir-name)]
+00000430: 6020 2020 2020 2020 2020 2d20 4372 6561  `         - Crea
+00000440: 7465 2061 206e 6577 2069 7261 696c 7320  te a new irails 
+00000450: 7072 6f6a 6563 742e 0d0a 2a20 6069 7261  project...* `ira
+00000460: 696c 7320 6170 7020 5b61 7070 2d6e 616d  ils app [app-nam
+00000470: 6528 6368 6f6f 7365 206f 7220 696e 7075  e(choose or inpu
+00000480: 7420 6170 7073 2064 6972 295d 6020 2d20  t apps dir)]` - 
+00000490: 4578 616d 706c 653a 2060 6972 6169 6c73  Example: `irails
+000004a0: 2061 7070 2061 646d 6973 7369 6f6e 7360   app admissions`
+000004b0: 2043 7265 6174 6520 6120 6e65 7720 6972   Create a new ir
+000004c0: 6169 6c73 2061 7070 2e0d 0a2a 2060 6972  ails app...* `ir
+000004d0: 6169 6c73 2072 756e 205b 2d2d 686f 7374  ails run [--host
+000004e0: 2068 6f73 745d 205b 2d2d 706f 7274 2070   host] [--port p
+000004f0: 6f72 745d 6020 2020 2020 2020 2020 202d  ort]`          -
+00000500: 2052 756e 2070 726f 6a65 6374 2076 6973   Run project vis
+00000510: 6974 206f 6e20 5b68 7474 703a 2f2f 3132  it on [http://12
+00000520: 372e 302e 302e 313a 3830 3030 3e5d 2868  7.0.0.1:8000>](h
+00000530: 7474 703a 2f2f 3132 372e 302e 302e 313a  ttp://127.0.0.1:
+00000540: 3830 3030 292e 200d 0a2a 2060 6972 6169  8000). ..* `irai
+00000550: 6c73 2063 6f6e 7472 6f6c 6c65 7220 5b61  ls controller [a
+00000560: 6374 696f 6e73 2e2e 2e5d 6020 2020 2020  ctions...]`     
+00000570: 2020 2020 2020 2020 2020 2020 202d 2067               - g
+00000580: 656e 6572 6174 6520 6120 636f 6e74 726f  enerate a contro
+00000590: 6c6c 6572 2077 6974 6820 6769 7665 6e20  ller with given 
+000005a0: 6163 7469 6f6e 7328 6966 206e 6f20 6769  actions(if no gi
+000005b0: 7665 6e2c 6465 6661 6c75 7420 6973 202a  ven,defalut is *
+000005c0: 2a69 6e64 6578 2a2a 292e 200d 0a20 0d0a  *index**). .. ..
+000005d0: 0d0a 2323 2050 726f 6a65 6374 206c 6179  ..## Project lay
+000005e0: 6f75 740d 0a60 6060 0d0a 200d 0a20 2020  out..```.. ..   
+000005f0: 207c 2020 206d 6169 6e2e 7079 0d0a 2020   |   main.py..  
+00000600: 2020 2b2d 2d2d 6170 7073 2020 2020 2020    +---apps      
+00000610: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000620: 2020 2020 2020 2020 2020 2323 2041 7070            ## App
+00000630: 7320 636f 6e74 6169 6e65 7220 2841 2070  s container (A p
+00000640: 726f 6a65 6374 2063 616e 2068 6176 6520  roject can have 
+00000650: 6d75 6c74 6970 6c65 2063 6f6e 7461 696e  multiple contain
+00000660: 6572 7329 0d0a 2020 2020 7c20 2020 2b2d  ers)..    |   +-
+00000670: 2d2d 6164 6d69 7373 696f 6e73 2020 2020  --admissions    
+00000680: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000690: 2020 2323 2041 7070 2064 6972 2028 416e    ## App dir (An
+000006a0: 2061 7070 6c69 6361 7469 6f6e 2063 6f6e   application con
+000006b0: 7461 696e 6572 2063 616e 2068 6176 6520  tainer can have 
+000006c0: 6d75 6c74 6970 6c65 2061 7070 6c69 6361  multiple applica
+000006d0: 7469 6f6e 7329 0d0a 2020 2020 7c20 2020  tions)..    |   
+000006e0: 7c20 2020 7c20 2020 5f5f 696e 6974 5f5f  |   |   __init__
+000006f0: 2e70 7920 2020 2020 2020 2020 2020 2020  .py             
+00000700: 2020 2020 0d0a 2020 2020 7c20 2020 7c20      ..    |   | 
+00000710: 2020 2b2d 2d2d 636f 6e74 726f 6c6c 6572    +---controller
+00000720: 7320 2020 2020 2020 2020 2020 2020 2020  s               
+00000730: 2020 2323 2043 6f6e 7472 6f6c 6c65 7220    ## Controller 
+00000740: 6669 6c65 730d 0a20 2020 207c 2020 207c  files..    |   |
+00000750: 2020 207c 2020 207c 2020 2068 6f6d 655f     |   |   home_
+00000760: 636f 6e74 726f 6c6c 6572 2e70 7920 2020  controller.py   
+00000770: 2020 2023 2320 436f 6e74 726f 6c6c 6572     ## Controller
+00000780: 2063 6c61 7373 2066 696c 652c 6974 2773   class file,it's
+00000790: 206c 6f6f 6b20 6c69 6b65 2060 636c 6173   look like `clas
+000007a0: 7320 486f 6d65 436f 6e74 726f 6c6c 6572  s HomeController
+000007b0: 600d 0a20 2020 207c 2020 207c 2020 207c  `..    |   |   |
+000007c0: 2020 207c 2020 205f 5f69 6e69 745f 5f2e     |   __init__.
+000007d0: 7079 0d0a 2020 2020 7c20 2020 7c20 2020  py..    |   |   
+000007e0: 2b2d 2d2d 6c6f 6361 6c65 7320 2020 2020  +---locales     
 000007f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000800: 2020 2323 2041 6c65 6d62 6963 2063 6f6e    ## Alembic con
-00000810: 6669 6775 7265 2066 696c 6520 2847 656e  figure file (Gen
-00000820: 6572 616c 6c79 2c20 7468 6572 6520 6973  erally, there is
-00000830: 206e 6f20 6e65 6564 2074 6f20 6368 616e   no need to chan
-00000840: 6765 2c20 7573 6564 2074 6865 2064 6174  ge, used the dat
-00000850: 6162 6173 6520 6d69 6772 6174 696f 6e29  abase migration)
-00000860: 0d0a 2020 2020 7c20 2020 2020 2020 6361  ..    |       ca
-00000870: 7362 696e 2d61 6461 7074 6572 2e63 7376  sbin-adapter.csv
-00000880: 2020 2020 2020 2020 2020 2020 2020 2323                ##
-00000890: 2043 6173 6269 6e20 6175 7468 206d 6f64   Casbin auth mod
-000008a0: 756c 6520 636f 6e66 6967 2061 6461 7074  ule config adapt
-000008b0: 6572 2066 696c 6528 290d 0a20 2020 207c  er file()..    |
-000008c0: 2020 2020 2020 2063 6173 6269 6e2d 6d6f         casbin-mo
-000008d0: 6465 6c2e 636f 6e66 2020 2020 2020 2020  del.conf        
-000008e0: 2020 2020 2020 2023 2320 4361 7362 696e         ## Casbin
-000008f0: 2061 7574 6820 636f 6e66 6967 206d 6f64   auth config mod
-00000900: 656c 0d0a 2020 2020 7c20 2020 2020 2020  el..    |       
-00000910: 6461 7461 6261 7365 2e79 616d 6c20 2020  database.yaml   
-00000920: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000930: 2323 2043 6f6e 6669 6775 7265 2066 6f72  ## Configure for
-00000940: 2064 6174 6162 6173 6520 7375 7070 6f72   database suppor
-00000950: 740d 0a20 2020 207c 2020 2020 2020 2067  t..    |       g
-00000960: 656e 6572 616c 2e79 616d 6c20 2020 2020  eneral.yaml     
-00000970: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000980: 2320 4765 6e65 7261 6c20 636f 6e66 6967  # General config
-00000990: 7572 6573 0d0a 2020 2020 7c20 2020 2020  ures..    |     
-000009a0: 2020 7365 7373 696f 6e2e 7961 6d6c 2020    session.yaml  
-000009b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-000009c0: 2020 2323 2053 6573 7369 6f6e 2063 6f6e    ## Session con
-000009d0: 6669 6775 7265 730d 0a20 2020 207c 0d0a  figures..    |..
-000009e0: 2020 2020 2b2d 2d2d 6461 7461 0d0a 2020      +---data..  
-000009f0: 2020 7c20 2020 2b2d 2d2d 616c 656d 6269    |   +---alembi
-00000a00: 630d 0a20 2020 207c 2020 207c 2020 205c  c..    |   |   \
-00000a10: 2d2d 2d76 6572 7369 6f6e 730d 0a20 2020  ---versions..   
-00000a20: 207c 2020 205c 2d2d 2d64 620d 0a20 2020   |   \---db..   
-00000a30: 207c 0d0a 2020 2020 2b2d 2d2d 7075 626c   |..    +---publ
-00000a40: 6963 2020 2020 2020 2020 2020 2020 2020  ic              
-00000a50: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000a60: 2323 2050 7562 6c69 6320 6469 7220 2877  ## Public dir (w
-00000a70: 696c 6c20 6d6f 756e 7465 6420 746f 2074  ill mounted to t
-00000a80: 6865 2027 2f70 7562 6c69 6327 2075 726c  he '/public' url
-00000a90: 290d 0a20 2020 207c 2020 207c 2020 2065  )..    |   |   e
-00000aa0: 7272 6f72 5f34 3034 2e68 746d 6c20 2020  rror_404.html   
-00000ab0: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000ac0: 2320 4572 726f 7220 7061 6765 202e 2e2e  # Error page ...
-00000ad0: 0d0a 2020 2020 7c20 2020 7c20 2020 6572  ..    |   |   er
-00000ae0: 726f 725f 3530 302e 6874 6d6c 0d0a 2020  ror_500.html..  
-00000af0: 2020 7c0d 0a20 2020 202b 2d2d 2d75 706c    |..    +---upl
-00000b00: 6f61 6473 2020 2020 2020 2020 2020 2020  oads            
-00000b10: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000b20: 2023 2320 4f74 6865 7273 2064 6972 2869   ## Others dir(i
-00000b30: 6620 796f 7572 206e 6565 6420 6f72 206e  f your need or n
-00000b40: 6f74 290d 0a60 6060 0d0a 2323 2045 7874  ot)..```..## Ext
-00000b50: 7261 7320 636f 6d6d 616e 6473 0d0a 2a20  ras commands..* 
-00000b60: 6069 7261 696c 7320 6931 386e 2067 6574  `irails i18n get
-00000b70: 7465 7874 6020 2d2d 6765 6e65 7261 7465  text` --generate
-00000b80: 2069 3138 6e20 696e 2069 7261 696c 7320   i18n in irails 
-00000b90: 6170 7020 6469 720d 0a0d 0a23 2320 5461  app dir....## Ta
-00000ba0: 6b65 2061 206c 6f6f 6b20 636f 6e66 6967  ke a look config
-00000bb0: 7572 6520 6669 6c65 2060 6765 6e65 7261  ure file `genera
-00000bc0: 6c2e 7961 6d6c 600d 0a20 0d0a 6060 6020  l.yaml`.. ..``` 
-00000bd0: 0d0a 2020 2020 6170 703a 0d0a 2020 2020  ..    app:..    
-00000be0: 2020 2020 6170 7064 6972 3a0d 0a20 2020      appdir:..   
-00000bf0: 2020 2020 202d 2061 7070 730d 0a20 2020       - apps..   
-00000c00: 2020 2020 2065 6e61 626c 6564 3a20 6e75       enabled: nu
-00000c10: 6c6c 0d0a 2020 2020 726f 6f74 3a20 6170  ll..    root: ap
-00000c20: 7073 2e72 6f6f 740d 0a0d 0a20 2020 2063  ps.root....    c
-00000c30: 6f72 733a 0d0a 2020 2020 2020 2020 616c  ors:..        al
-00000c40: 6c6f 775f 6372 6564 656e 7469 616c 733a  low_credentials:
-00000c50: 2074 7275 650d 0a20 2020 2020 2020 2061   true..        a
-00000c60: 6c6c 6f77 5f68 6561 6465 7273 3a0d 0a20  llow_headers:.. 
-00000c70: 2020 2020 2020 2020 2020 202d 2027 2a27             - '*'
-00000c80: 0d0a 2020 2020 2020 2020 616c 6c6f 775f  ..        allow_
-00000c90: 6d65 7468 6f64 733a 0d0a 2020 2020 2020  methods:..      
-00000ca0: 2020 2020 2020 2d20 272a 270d 0a20 2020        - '*'..   
-00000cb0: 2020 2020 2061 6c6c 6f77 5f6f 7269 6769       allow_origi
-00000cc0: 6e73 3a0d 0a20 2020 2020 2020 2020 2020  ns:..           
-00000cd0: 202d 2027 2a27 0d0a 2020 2020 6465 6275   - '*'..    debu
-00000ce0: 673a 2074 7275 650d 0a20 2020 2065 7272  g: true..    err
-00000cf0: 6f72 733a 0d0a 2020 2020 2020 2020 6572  ors:..        er
-00000d00: 726f 725f 3430 345f 7061 6765 3a20 277b  ror_404_page: '{
-00000d10: 524f 4f54 2e70 7562 6c69 635f 6469 727d  ROOT.public_dir}
-00000d20: 2f65 7272 6f72 5f34 3034 2e68 746d 6c27  /error_404.html'
-00000d30: 0d0a 2020 2020 2020 2020 6572 726f 725f  ..        error_
-00000d40: 3530 305f 7061 6765 3a20 277b 524f 4f54  500_page: '{ROOT
-00000d50: 2e70 7562 6c69 635f 6469 727d 2f65 7272  .public_dir}/err
-00000d60: 6f72 5f35 3030 2e68 746d 6c27 0d0a 2020  or_500.html'..  
-00000d70: 2020 6c6f 673a 0d0a 2020 2020 2020 2020    log:..        
-00000d80: 6669 6c65 3a20 2727 0d0a 2020 2020 2020  file: ''..      
-00000d90: 2020 6c65 7665 6c3a 2044 4542 5547 0d0a    level: DEBUG..
-00000da0: 2020 2020 2020 2020 6e61 6d65 3a20 6952          name: iR
-00000db0: 6169 6c73 0d0a 2020 2020 7075 626c 6963  ails..    public
-00000dc0: 5f64 6972 3a20 2e2f 7075 626c 6963 0d0a  _dir: ./public..
-00000dd0: 0d0a 2020 2020 7669 6577 3a0d 0a20 2020  ..    view:..   
-00000de0: 2020 2020 206a 696e 6a61 323a 0d0a 2020       jinja2:..  
-00000df0: 2020 2020 2020 2020 2020 626c 6f63 6b5f            block_
-00000e00: 656e 645f 7374 7269 6e67 3a20 2725 7d27  end_string: '%}'
-00000e10: 0d0a 2020 2020 2020 2020 2020 2020 626c  ..            bl
-00000e20: 6f63 6b5f 7374 6172 745f 7374 7269 6e67  ock_start_string
-00000e30: 3a20 277b 2527 0d0a 2020 2020 2020 2020  : '{%'..        
-00000e40: 2020 2020 636f 6d6d 656e 745f 656e 645f      comment_end_
-00000e50: 7374 7269 6e67 3a20 2723 7d27 0d0a 2020  string: '#}'..  
-00000e60: 2020 2020 2020 2020 2020 636f 6d6d 656e            commen
-00000e70: 745f 7374 6172 745f 7374 7269 6e67 3a20  t_start_string: 
-00000e80: 277b 2327 0d0a 2020 2020 2020 2020 2020  '{#'..          
-00000e90: 2020 7661 7269 6162 6c65 5f65 6e64 5f73    variable_end_s
-00000ea0: 7472 696e 673a 2027 7d27 0d0a 2020 2020  tring: '}'..    
-00000eb0: 2020 2020 2020 2020 7661 7269 6162 6c65          variable
-00000ec0: 5f73 7461 7274 5f73 7472 696e 673a 2024  _start_string: $
-00000ed0: 7b0d 0a20 2020 2020 2020 2073 7461 7469  {..        stati
-00000ee0: 635f 666f 726d 6174 3a0d 0a20 2020 2020  c_format:..     
-00000ef0: 2020 202d 2076 7565 0d0a 2020 2020 2020     - vue..      
-00000f00: 2020 2d20 6874 6d6c 0d0a 2020 2020 6931    - html..    i1
-00000f10: 386e 3a0d 0a20 2020 2020 2020 206c 616e  8n:..        lan
-00000f20: 673a 205b 277a 6827 5d0d 0a20 2020 2020  g: ['zh']..     
-00000f30: 2020 2075 726c 5f6c 616e 675f 6b65 793a     url_lang_key:
-00000f40: 2027 6c61 6e67 270d 0a60 6060 0d0a 2323   'lang'..```..##
-00000f50: 2054 616b 6520 6120 6c6f 6f6b 2063 6f6e   Take a look con
-00000f60: 7472 6f6c 6c65 7220 6669 6c65 200d 0a20  troller file .. 
-00000f70: 0d0a 6060 6070 7974 686f 6e0d 0a20 2020  ..```python..   
-00000f80: 2066 726f 6d20 6972 6169 6c73 2069 6d70   from irails imp
-00000f90: 6f72 7420 6170 695f 726f 7574 6572 2c61  ort api_router,a
-00000fa0: 7069 2c52 6571 7565 7374 2c52 6573 706f  pi,Request,Respo
-00000fb0: 6e73 652c 4261 7365 436f 6e74 726f 6c6c  nse,BaseControll
-00000fc0: 6572 2c61 7070 6c69 6361 7469 6f6e 0d0a  er,application..
-00000fd0: 200d 0a20 2020 2040 6170 695f 726f 7574   ..    @api_rout
-00000fe0: 6572 2870 6174 683d 272f 7b63 6f6e 7472  er(path='/{contr
-00000ff0: 6f6c 6c65 727d 272c 6175 7468 3d27 6e6f  oller}',auth='no
-00001000: 6e65 2729 0d0a 2020 2020 636c 6173 7320  ne')..    class 
-00001010: 4164 6d69 6e43 6f6e 7472 6f6c 6c65 7228  AdminController(
-00001020: 4261 7365 436f 6e74 726f 6c6c 6572 293a  BaseController):
-00001030: 200d 0a20 2020 2020 2020 2040 6170 692e   ..        @api.
-00001040: 6765 7428 222f 696e 6465 7822 290d 0a20  get("/index").. 
-00001050: 2020 2020 2020 2064 6566 2069 6e64 6578         def index
-00001060: 2873 656c 6629 3a0d 0a20 2020 2020 2020  (self):..       
-00001070: 2020 2020 2022 2222 0d0a 2020 2020 2020       """..      
-00001080: 2020 2020 2020 3a74 6974 6c65 2041 646d        :title Adm
-00001090: 696e 0d0a 2020 2020 2020 2020 2020 2020  in..            
-000010a0: 2222 220d 0a20 2020 2020 2020 2020 2020  """..           
-000010b0: 2072 6574 7572 6e20 7365 6c66 2e76 6965   return self.vie
-000010c0: 7728 290d 0a60 6060                      w()..```
+00000800: 2323 2049 3138 6e20 6c6f 6361 6c65 7320  ## I18n locales 
+00000810: 6469 722c 7573 6520 636f 6d6d 616e 6420  dir,use command 
+00000820: 6061 7070 732f 6170 703a 2420 6972 616c  `apps/app:$ iral
+00000830: 6973 2069 3138 6e20 6765 7474 6578 7460  is i18n gettext`
+00000840: 2077 696c 6c20 6175 746f 2067 656e 6572   will auto gener
+00000850: 6174 6520 6974 656d 730d 0a20 2020 207c  ate items..    |
+00000860: 2020 207c 2020 202b 2d2d 2d6d 6f64 656c     |   +---model
+00000870: 7320 2020 2020 2020 2020 2020 2020 2020  s               
+00000880: 2020 2020 2020 2023 2320 4461 7461 6261         ## Databa
+00000890: 7365 206d 6f64 656c 7320 6669 6c65 7328  se models files(
+000008a0: 6966 2079 6f75 2075 7365 2073 6f6d 6520  if you use some 
+000008b0: 6461 7461 6261 7365 2073 7570 706f 7274  database support
+000008c0: 290d 0a20 2020 207c 2020 207c 2020 207c  )..    |   |   |
+000008d0: 2020 2020 2020 205f 5f69 6e69 745f 5f2e         __init__.
+000008e0: 7079 0d0a 2020 2020 7c20 2020 7c20 2020  py..    |   |   
+000008f0: 2b2d 2d2d 7365 7276 6963 6573 2020 2020  +---services    
+00000900: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000910: 2323 204d 6f64 756c 6520 666f 7220 6275  ## Module for bu
+00000920: 7369 6e65 7373 206c 6f67 6963 2070 726f  siness logic pro
+00000930: 6365 7373 696e 670d 0a20 2020 207c 2020  cessing..    |  
+00000940: 207c 2020 202b 2d2d 2d74 6573 7473 2020   |   +---tests  
+00000950: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000960: 2020 2020 2023 2320 556e 6974 2074 6573       ## Unit tes
+00000970: 7474 696e 670d 0a20 2020 207c 2020 207c  tting..    |   |
+00000980: 2020 202b 2d2d 2d76 6965 7773 2020 2020     +---views    
+00000990: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000009a0: 2020 2023 2320 5374 6174 6963 2076 6965     ## Static vie
+000009b0: 7720 6669 6c65 7320 2875 7365 2060 4a69  w files (use `Ji
+000009c0: 6e6a 6132 6020 5465 6d70 6c61 7465 290d  nja2` Template).
+000009d0: 0a20 2020 207c 2020 207c 2020 207c 2020  .    |   |   |  
+000009e0: 207c 2020 206c 6179 6f75 742e 6874 6d6c   |   layout.html
+000009f0: 0d0a 2020 2020 7c20 2020 7c20 2020 7c20  ..    |   |   | 
+00000a00: 2020 7c0d 0a20 2020 207c 2020 207c 2020    |..    |   |  
+00000a10: 207c 2020 202b 2d2d 2d68 6f6d 6520 2020   |   +---home   
+00000a20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a30: 2023 2320 5468 6520 636f 6e74 726f 6c6c   ## The controll
+00000a40: 6572 2061 6374 696f 6e27 7320 7374 6174  er action's stat
+00000a50: 6963 2066 696c 6528 6e61 6d65 2069 7320  ic file(name is 
+00000a60: 7361 6d65 2074 6f20 7468 6520 636f 6e74  same to the cont
+00000a70: 726f 6c6c 6572 2773 2063 6c61 7373 206e  roller's class n
+00000a80: 616d 6529 0d0a 2020 2020 7c20 2020 7c20  ame)..    |   | 
+00000a90: 2020 7c20 2020 7c20 2020 2020 2020 686f    |   |       ho
+00000aa0: 6d65 2e63 7373 2020 2020 2020 2020 2020  me.css          
+00000ab0: 2020 0d0a 2020 2020 7c20 2020 7c20 2020    ..    |   |   
+00000ac0: 7c20 2020 7c20 2020 2020 2020 686f 6d65  |   |       home
+00000ad0: 2e68 746d 6c20 2020 2020 2020 2020 2020  .html           
+00000ae0: 2323 2053 7461 7469 6320 6669 6c65 2063  ## Static file c
+00000af0: 6f72 7265 7370 6f6e 6469 6e67 2074 6f20  orresponding to 
+00000b00: 6163 7469 6f6e 286e 616d 6520 6973 2073  action(name is s
+00000b10: 616d 6520 746f 2074 6865 2063 6f6e 7472  ame to the contr
+00000b20: 6f6c 6c65 7227 7320 6d65 7468 6f64 206e  oller's method n
+00000b30: 616d 6529 0d0a 2020 2020 2b2d 2d2d 636f  ame)..    +---co
+00000b40: 6e66 6967 7320 2020 2020 2020 2020 2020  nfigs           
+00000b50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000b60: 2020 2323 2050 726f 6a65 6374 2063 6f6e    ## Project con
+00000b70: 6669 6775 7265 2064 6972 0d0a 2020 2020  figure dir..    
+00000b80: 7c20 2020 2020 2020 616c 656d 6269 632e  |       alembic.
+00000b90: 696e 6920 2020 2020 2020 2020 2020 2020  ini             
+00000ba0: 2020 2020 2020 2020 2323 2041 6c65 6d62          ## Alemb
+00000bb0: 6963 2063 6f6e 6669 6775 7265 2066 696c  ic configure fil
+00000bc0: 6520 2847 656e 6572 616c 6c79 2c20 7468  e (Generally, th
+00000bd0: 6572 6520 6973 206e 6f20 6e65 6564 2074  ere is no need t
+00000be0: 6f20 6368 616e 6765 2c20 7573 6564 2074  o change, used t
+00000bf0: 6865 2064 6174 6162 6173 6520 6d69 6772  he database migr
+00000c00: 6174 696f 6e29 0d0a 2020 2020 7c20 2020  ation)..    |   
+00000c10: 2020 2020 6361 7362 696e 2d61 6461 7074      casbin-adapt
+00000c20: 6572 2e63 7376 2020 2020 2020 2020 2020  er.csv          
+00000c30: 2020 2020 2323 2043 6173 6269 6e20 6175      ## Casbin au
+00000c40: 7468 206d 6f64 756c 6520 636f 6e66 6967  th module config
+00000c50: 2061 6461 7074 6572 2066 696c 6528 290d   adapter file().
+00000c60: 0a20 2020 207c 2020 2020 2020 2063 6173  .    |       cas
+00000c70: 6269 6e2d 6d6f 6465 6c2e 636f 6e66 2020  bin-model.conf  
+00000c80: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
+00000c90: 4361 7362 696e 2061 7574 6820 636f 6e66  Casbin auth conf
+00000ca0: 6967 206d 6f64 656c 0d0a 2020 2020 7c20  ig model..    | 
+00000cb0: 2020 2020 2020 6461 7461 6261 7365 2e79        database.y
+00000cc0: 616d 6c20 2020 2020 2020 2020 2020 2020  aml             
+00000cd0: 2020 2020 2020 2323 2043 6f6e 6669 6775        ## Configu
+00000ce0: 7265 2066 6f72 2064 6174 6162 6173 6520  re for database 
+00000cf0: 7375 7070 6f72 740d 0a20 2020 207c 2020  support..    |  
+00000d00: 2020 2020 2067 656e 6572 616c 2e79 616d       general.yam
+00000d10: 6c20 2020 2020 2020 2020 2020 2020 2020  l               
+00000d20: 2020 2020 2023 2320 4765 6e65 7261 6c20       ## General 
+00000d30: 636f 6e66 6967 7572 6573 0d0a 2020 2020  configures..    
+00000d40: 7c20 2020 2020 2020 7365 7373 696f 6e2e  |       session.
+00000d50: 7961 6d6c 2020 2020 2020 2020 2020 2020  yaml            
+00000d60: 2020 2020 2020 2020 2323 2053 6573 7369          ## Sessi
+00000d70: 6f6e 2063 6f6e 6669 6775 7265 730d 0a20  on configures.. 
+00000d80: 2020 207c 0d0a 2020 2020 2b2d 2d2d 6461     |..    +---da
+00000d90: 7461 0d0a 2020 2020 7c20 2020 2b2d 2d2d  ta..    |   +---
+00000da0: 616c 656d 6269 630d 0a20 2020 207c 2020  alembic..    |  
+00000db0: 207c 2020 205c 2d2d 2d76 6572 7369 6f6e   |   \---version
+00000dc0: 730d 0a20 2020 207c 2020 205c 2d2d 2d64  s..    |   \---d
+00000dd0: 620d 0a20 2020 207c 0d0a 2020 2020 2b2d  b..    |..    +-
+00000de0: 2d2d 7075 626c 6963 2020 2020 2020 2020  --public        
+00000df0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000e00: 2020 2020 2020 2323 2050 7562 6c69 6320        ## Public 
+00000e10: 6469 7220 2877 696c 6c20 6d6f 756e 7465  dir (will mounte
+00000e20: 6420 746f 2074 6865 2027 2f70 7562 6c69  d to the '/publi
+00000e30: 6327 2075 726c 290d 0a20 2020 207c 2020  c' url)..    |  
+00000e40: 207c 2020 2065 7272 6f72 5f34 3034 2e68   |   error_404.h
+00000e50: 746d 6c20 2020 2020 2020 2020 2020 2020  tml             
+00000e60: 2020 2020 2023 2320 4572 726f 7220 7061       ## Error pa
+00000e70: 6765 202e 2e2e 0d0a 2020 2020 7c20 2020  ge .....    |   
+00000e80: 7c20 2020 6572 726f 725f 3530 302e 6874  |   error_500.ht
+00000e90: 6d6c 0d0a 2020 2020 7c0d 0a20 2020 202b  ml..    |..    +
+00000ea0: 2d2d 2d75 706c 6f61 6473 2020 2020 2020  ---uploads      
+00000eb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000ec0: 2020 2020 2020 2023 2320 4f74 6865 7273         ## Others
+00000ed0: 2064 6972 2869 6620 796f 7572 206e 6565   dir(if your nee
+00000ee0: 6420 6f72 206e 6f74 290d 0a60 6060 0d0a  d or not)..```..
+00000ef0: 2323 2045 7874 7261 7320 636f 6d6d 616e  ## Extras comman
+00000f00: 6473 0d0a 2a20 6069 7261 696c 7320 6931  ds..* `irails i1
+00000f10: 386e 2067 6574 7465 7874 6020 202d 2d67  8n gettext`  --g
+00000f20: 656e 6572 6174 6520 6931 386e 2069 6e20  enerate i18n in 
+00000f30: 6972 6169 6c73 2061 7070 2064 6972 0d0a  irails app dir..
+00000f40: 2a20 6069 7261 696c 7320 7368 656c 6c60  * `irails shell`
+00000f50: 2020 2020 2020 2020 202d 2d72 756e 2070           --run p
+00000f60: 7974 686f 6e20 696e 7465 7270 7265 7465  ython interprete
+00000f70: 7220 7769 7468 2062 7569 6c64 696e 2073  r with buildin s
+00000f80: 7570 706f 7274 2063 6f6e 7465 7874 7320  upport contexts 
+00000f90: 0d0a 0d0a 2323 2054 616b 6520 6120 6c6f  ....## Take a lo
+00000fa0: 6f6b 2063 6f6e 6669 6775 7265 2066 696c  ok configure fil
+00000fb0: 6520 6067 656e 6572 616c 2e79 616d 6c60  e `general.yaml`
+00000fc0: 0d0a 200d 0a60 6060 200d 0a20 2020 2061  .. ..``` ..    a
+00000fd0: 7070 3a0d 0a20 2020 2020 2020 2061 7070  pp:..        app
+00000fe0: 6469 723a 0d0a 2020 2020 2020 2020 2d20  dir:..        - 
+00000ff0: 6170 7073 0d0a 2020 2020 2020 2020 656e  apps..        en
+00001000: 6162 6c65 643a 206e 756c 6c0d 0a20 2020  abled: null..   
+00001010: 2072 6f6f 743a 2061 7070 732e 726f 6f74   root: apps.root
+00001020: 0d0a 0d0a 2020 2020 636f 7273 3a0d 0a20  ....    cors:.. 
+00001030: 2020 2020 2020 2061 6c6c 6f77 5f63 7265         allow_cre
+00001040: 6465 6e74 6961 6c73 3a20 7472 7565 0d0a  dentials: true..
+00001050: 2020 2020 2020 2020 616c 6c6f 775f 6865          allow_he
+00001060: 6164 6572 733a 0d0a 2020 2020 2020 2020  aders:..        
+00001070: 2020 2020 2d20 272a 270d 0a20 2020 2020      - '*'..     
+00001080: 2020 2061 6c6c 6f77 5f6d 6574 686f 6473     allow_methods
+00001090: 3a0d 0a20 2020 2020 2020 2020 2020 202d  :..            -
+000010a0: 2027 2a27 0d0a 2020 2020 2020 2020 616c   '*'..        al
+000010b0: 6c6f 775f 6f72 6967 696e 733a 0d0a 2020  low_origins:..  
+000010c0: 2020 2020 2020 2020 2020 2d20 272a 270d            - '*'.
+000010d0: 0a20 2020 2064 6562 7567 3a20 7472 7565  .    debug: true
+000010e0: 0d0a 2020 2020 6572 726f 7273 3a0d 0a20  ..    errors:.. 
+000010f0: 2020 2020 2020 2065 7272 6f72 5f34 3034         error_404
+00001100: 5f70 6167 653a 2027 7b52 4f4f 542e 7075  _page: '{ROOT.pu
+00001110: 626c 6963 5f64 6972 7d2f 6572 726f 725f  blic_dir}/error_
+00001120: 3430 342e 6874 6d6c 270d 0a20 2020 2020  404.html'..     
+00001130: 2020 2065 7272 6f72 5f35 3030 5f70 6167     error_500_pag
+00001140: 653a 2027 7b52 4f4f 542e 7075 626c 6963  e: '{ROOT.public
+00001150: 5f64 6972 7d2f 6572 726f 725f 3530 302e  _dir}/error_500.
+00001160: 6874 6d6c 270d 0a20 2020 206c 6f67 3a0d  html'..    log:.
+00001170: 0a20 2020 2020 2020 2066 696c 653a 2027  .        file: '
+00001180: 270d 0a20 2020 2020 2020 206c 6576 656c  '..        level
+00001190: 3a20 4445 4255 470d 0a20 2020 2020 2020  : DEBUG..       
+000011a0: 206e 616d 653a 2069 5261 696c 730d 0a20   name: iRails.. 
+000011b0: 2020 2070 7562 6c69 635f 6469 723a 202e     public_dir: .
+000011c0: 2f70 7562 6c69 630d 0a0d 0a20 2020 2076  /public....    v
+000011d0: 6965 773a 0d0a 2020 2020 2020 2020 6a69  iew:..        ji
+000011e0: 6e6a 6132 3a0d 0a20 2020 2020 2020 2020  nja2:..         
+000011f0: 2020 2062 6c6f 636b 5f65 6e64 5f73 7472     block_end_str
+00001200: 696e 673a 2027 257d 270d 0a20 2020 2020  ing: '%}'..     
+00001210: 2020 2020 2020 2062 6c6f 636b 5f73 7461         block_sta
+00001220: 7274 5f73 7472 696e 673a 2027 7b25 270d  rt_string: '{%'.
+00001230: 0a20 2020 2020 2020 2020 2020 2063 6f6d  .            com
+00001240: 6d65 6e74 5f65 6e64 5f73 7472 696e 673a  ment_end_string:
+00001250: 2027 237d 270d 0a20 2020 2020 2020 2020   '#}'..         
+00001260: 2020 2063 6f6d 6d65 6e74 5f73 7461 7274     comment_start
+00001270: 5f73 7472 696e 673a 2027 7b23 270d 0a20  _string: '{#'.. 
+00001280: 2020 2020 2020 2020 2020 2076 6172 6961             varia
+00001290: 626c 655f 656e 645f 7374 7269 6e67 3a20  ble_end_string: 
+000012a0: 277d 270d 0a20 2020 2020 2020 2020 2020  '}'..           
+000012b0: 2076 6172 6961 626c 655f 7374 6172 745f   variable_start_
+000012c0: 7374 7269 6e67 3a20 247b 0d0a 2020 2020  string: ${..    
+000012d0: 2020 2020 7374 6174 6963 5f66 6f72 6d61      static_forma
+000012e0: 743a 0d0a 2020 2020 2020 2020 2d20 7675  t:..        - vu
+000012f0: 650d 0a20 2020 2020 2020 202d 2068 746d  e..        - htm
+00001300: 6c0d 0a20 2020 2069 3138 6e3a 0d0a 2020  l..    i18n:..  
+00001310: 2020 2020 2020 6c61 6e67 3a20 5b27 7a68        lang: ['zh
+00001320: 275d 0d0a 2020 2020 2020 2020 7572 6c5f  ']..        url_
+00001330: 6c61 6e67 5f6b 6579 3a20 276c 616e 6727  lang_key: 'lang'
+00001340: 0d0a 6060 600d 0a23 2320 5461 6b65 2061  ..```..## Take a
+00001350: 206c 6f6f 6b20 636f 6e74 726f 6c6c 6572   look controller
+00001360: 2066 696c 6520 0d0a 200d 0a60 6060 7079   file .. ..```py
+00001370: 7468 6f6e 0d0a 2020 2020 6672 6f6d 2069  thon..    from i
+00001380: 7261 696c 7320 696d 706f 7274 2061 7069  rails import api
+00001390: 5f72 6f75 7465 722c 6170 692c 5265 7175  _router,api,Requ
+000013a0: 6573 742c 5265 7370 6f6e 7365 2c42 6173  est,Response,Bas
+000013b0: 6543 6f6e 7472 6f6c 6c65 722c 6170 706c  eController,appl
+000013c0: 6963 6174 696f 6e0d 0a20 0d0a 2020 2020  ication.. ..    
+000013d0: 4061 7069 5f72 6f75 7465 7228 7061 7468  @api_router(path
+000013e0: 3d27 2f7b 636f 6e74 726f 6c6c 6572 7d27  ='/{controller}'
+000013f0: 2c61 7574 683d 276e 6f6e 6527 290d 0a20  ,auth='none').. 
+00001400: 2020 2063 6c61 7373 2041 646d 696e 436f     class AdminCo
+00001410: 6e74 726f 6c6c 6572 2842 6173 6543 6f6e  ntroller(BaseCon
+00001420: 7472 6f6c 6c65 7229 3a20 0d0a 2020 2020  troller): ..    
+00001430: 2020 2020 4061 7069 2e67 6574 2822 2f69      @api.get("/i
+00001440: 6e64 6578 2229 0d0a 2020 2020 2020 2020  ndex")..        
+00001450: 6465 6620 696e 6465 7828 7365 6c66 293a  def index(self):
+00001460: 0d0a 2020 2020 2020 2020 2020 2020 2222  ..            ""
+00001470: 220d 0a20 2020 2020 2020 2020 2020 203a  "..            :
+00001480: 7469 746c 6520 4164 6d69 6e0d 0a20 2020  title Admin..   
+00001490: 2020 2020 2020 2020 2022 2222 0d0a 2020           """..  
+000014a0: 2020 2020 2020 2020 2020 7265 7475 726e            return
+000014b0: 2073 656c 662e 7669 6577 2829 0d0a 6060   self.view()..``
+000014c0: 600d 0a                                  `..
```

### Comparing `irails-1.3.5/irails/_i18n.py` & `irails-1.3.6/irails/_i18n.py`

 * *Files 3% similar despite different names*

```diff
@@ -57,15 +57,15 @@
     def do_command():
         from ._loader import load_module
         _tools_file = os.path.join(sys.prefix,'Tools','i18n',f"msgfmt.py")
         module = load_module('mfgmft',_tools_file)
         if module:
             module.make(po_file,mo_file)
         else:
-            print(f"not found tools file : mfgmft")
+            print(f"not found tools file : {_tools_file}")
     # 判断po文件是否存在
     if os.path.exists(po_file): 
         if os.path.exists(mo_file):
             mod_time =  (os.stat(mo_file).st_mtime)
         else:
             mod_time = 0
         pod_time =  (os.stat(po_file).st_mtime)
```

### Comparing `irails-1.3.5/irails/_loader.py` & `irails-1.3.6/irails/_loader.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/_utils.py` & `irails-1.3.6/irails/_utils.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/auth.py` & `irails-1.3.6/irails/auth.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/base_controller.py` & `irails-1.3.6/irails/base_controller.py`

 * *Files 2% similar despite different names*

```diff
@@ -143,19 +143,21 @@
         pass
 
     def _verity_error(self,msg="User authentication failed!"):
         """return Response for show Verity failed infomation"""
         pass
      
     # @property
-    def view(self,content:str="",view_path:str="", format:str="html", context: dict={},local2context:bool=True,**kwargs): 
+    def view(self,content:str="",view_path:str="", format:str="html", context: dict=None,local2context:bool=True,**kwargs): 
         """
         return a Response by template file
         if :view_path is empty ,it's will look for current method in the view directory(offen is app dir views\controller's name)
         """
+        if not context:
+            context={}
         if not isinstance(context,dict):
             if hasattr(context,'__dict__'):
                 context = getattr(context,'__dict__')
             else:
                 context = {}
                 
             
@@ -208,15 +210,16 @@
         
         if not 'flash' in context:
             context['flash'] = self._request.session['flash']
         template_path = os.path.join(self.__appdir__,"views")
         viewobj = _View(self._request,self._response, tmpl_path=template_path) 
         viewobj._templates.env.globals["url_for"] = url_for 
         viewobj._templates.env.globals["_"] = self._ 
-        return viewobj(view_path,context,**kwargs)
+        response_result = viewobj(view_path,context,**kwargs)
+        return response_result
     
     async def _save_upload_file(self,file:File):  
         """return the file to saved path and http URL"""
         file.file.seek(0, 2)  # 将指针移动到文件末尾
 
         if MAX_UPLOAD_LEN>=0 and file.file.tell() > MAX_UPLOAD_LEN:
             mb = MAX_UPLOAD_LEN/1024/1024
```

### Comparing `irails-1.3.5/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc` & `irails-1.3.6/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/casbin_adapters/sqlalchemy_adapter.py` & `irails-1.3.6/irails/casbin_adapters/sqlalchemy_adapter.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,17 +5,22 @@
 from sqlalchemy import Column, Integer, String
 from sqlalchemy import create_engine, or_
 from sqlalchemy.ext.declarative import declarative_base
 from sqlalchemy.orm import sessionmaker
 #copied from:https://github.com/pycasbin/sqlalchemy-adapter/blob/master/casbin_sqlalchemy_adapter/adapter.py
 #Base = declarative_base()
 from irails import database
-
+from irails.config import config
+rule_table = 'casbin_rule'
+cfg = config.get("auth")
+if cfg and 'adapter_table' in cfg:
+    rule_table = cfg.get('adapter_table','casbin_rule')
+    
 class CasbinRule(database.Base):
-    __tablename__ = "casbin_rule"
+    __tablename__ = rule_table
 
     id = Column(Integer, primary_key=True)
     ptype = Column(String(255))
     v0 = Column(String(255))
     v1 = Column(String(255))
     v2 = Column(String(255))
     v3 = Column(String(255))
```

### Comparing `irails-1.3.5/irails/cbv.py` & `irails-1.3.6/irails/cbv.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/config.py` & `irails-1.3.6/irails/config.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/controller_utils.py` & `irails-1.3.6/irails/controller_utils.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/core.py` & `irails-1.3.6/irails/core.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/database.py` & `irails-1.3.6/irails/database.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/log.py` & `irails-1.3.6/irails/log.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/midware.py` & `irails-1.3.6/irails/midware.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/midware_casbin.py` & `irails-1.3.6/irails/midware_casbin.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/midware_session.py` & `irails-1.3.6/irails/midware_session.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/mvc_router.py` & `irails-1.3.6/irails/mvc_router.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/_app.py` & `irails-1.3.6/irails/scripts/_app.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/_controller.py` & `irails-1.3.6/irails/scripts/_controller.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/_i18n.py` & `irails-1.3.6/irails/scripts/_i18n.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,15 @@
-import sys,os,importlib
+import sys,os,importlib,datetime
 from irails import __version__
 from irails.config import is_in_app, is_in_irails,YamlConfig
 cur_dir = os.path.abspath(os.curdir)
 root_path = os.path.abspath(os.path.join(cur_dir,"../.."))
 config = YamlConfig(os.path.join(root_path,"configs"))
 locales_path = os.path.abspath('locales') 
-
+dev_mode = True
 import glob
 
 def get_html_vue_files(_root_path):
     html_vue_files = []
     for root, dirs, files in os.walk(_root_path):
         for file in files:
             file_path = os.path.join(root, file)
@@ -145,41 +145,54 @@
         with open(_pot_file,'r') as f:
             _pot_content = f.read()
         _pot_content = split_pot(_pot_content)
         
     else:
         print("messages.pot des'nt exists!")
         return
-    import datetime
+    
     d1 = datetime.datetime.now().strftime('%Y-%m-%d %H:%M%z')
     year = datetime.datetime.now().strftime('%Y')
      
      
     d2 = d1
     for lang in nelangs:
         if len(lang)!=5: #ensure like zh-CN ,en-US
             continue
         header = po_header.replace("{d1}",d1).replace("{d2}",d2).replace("{lang}",lang).replace("{YEAR}",year).replace("{version}",__version__)
         path = os.path.join(locales_path,f"{lang}.po")
+        #backup 
+        if os.path.exists(path):
+            timestamp = datetime.datetime.now().strftime("%Y%m%d%H%M%S") 
+            backup_filename = os.path.join(locales_path,f"{lang}_{timestamp}_bak.po")
+            #  
+            with open(path, "rb") as src_file:
+                with open(backup_filename, "wb") as backup_file:
+                    backup_file.write(src_file.read())
+
         with open(path,'w') as f:
             f.write(header+"\n"+_pot_content)
             
             print(f"generated {path}")
         #gen html files
 
 def do_command(i18n_tool_file:str):
+    global dev_mode
     if i18n_tool_file.lower()=='gettext':
         i18n_tool_file='pygettext'
     if i18n_tool_file=='pygettext':
         
         if not os.path.exists(locales_path):
             os.makedirs(locales_path,exist_ok=True)
         if len(sys.argv)<2:
-            for d in ['controllers','services','models']:
-                sys.argv.append(d)
+            if dev_mode:
+                sys.argv.append(cur_dir)
+            else:
+                for d in ['controllers','services','models']:
+                    sys.argv.append(d)
 
         if not '-o' in sys.argv:
             sys.argv.insert(1,'-o') 
             sys.argv.insert(2,f'{locales_path}{os.sep}messages.pot') 
          
             
     _tools_file = os.path.join(sys.prefix,'Tools','i18n',f"{i18n_tool_file}.py")
@@ -192,19 +205,25 @@
             print(f"Done!")
         except Exception as e:
             print(e)
     else:
         print(f"not found tools file:{i18n_tool_file}")
 def main(): 
     #irails pygettext  -a -o messages.pot /path/to/your/dir/*.py
-    
+    global dev_mode
+    irails_srcs = ['__init__.py','_i18n.py','_loader.py','_utils.py','auth.py','base_controller.py','cbv.py']
+    for src in irails_srcs:
+        p = os.path.join(cur_dir,src)
+        if not os.path.exists(p):
+            dev_mode = False
     if os.path.exists(root_path) and  os.path.isdir(root_path): 
         if not is_in_irails(root_path) or not is_in_app(cur_dir):
             print(f"Please exec in irails project's app dir ,like `apps/app`")
-            exit()
+            if not dev_mode:
+                exit()
     if len(sys.argv)>=2:
          
         cmd = sys.argv.pop(1)
         do_command(cmd)
     else:
         self_file = os.path.basename(__file__).lstrip("_").replace(".py",'')
         print(f"Usage: irails {self_file} [args...]")
```

### Comparing `irails-1.3.5/irails/scripts/_project.py` & `irails-1.3.6/irails/scripts/_project.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/_run.py` & `irails-1.3.6/irails/scripts/_run.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/_shell.py` & `irails-1.3.6/irails/scripts/_shell.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/main.py` & `irails-1.3.6/irails/scripts/main.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/app/home.css.tpl` & `irails-1.3.6/irails/scripts/tpls/app/home.css.tpl`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/app/home.tpl` & `irails-1.3.6/irails/scripts/tpls/app/home.tpl`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/configs/alembic.ini` & `irails-1.3.6/irails/scripts/tpls/project/configs/alembic.ini`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/configs/database.yaml` & `irails-1.3.6/irails/scripts/tpls/project/configs/database.yaml`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/configs/general.yaml` & `irails-1.3.6/irails/scripts/tpls/project/configs/general.yaml`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/data/alembic/env.py` & `irails-1.3.6/irails/scripts/tpls/project/data/alembic/env.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/error_404.html` & `irails-1.3.6/irails/scripts/tpls/project/public/error_404.html`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/error_500.html` & `irails-1.3.6/irails/scripts/tpls/project/public/error_500.html`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js` & `irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css` & `irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js` & `irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js` & `irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js` & `irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails/view.py` & `irails-1.3.6/irails/view.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails.egg-info/PKG-INFO` & `irails-1.3.6/irails.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310d 0a4e 616d 653a 2069 7261  : 2.1..Name: ira
 00000020: 696c 730d 0a56 6572 7369 6f6e 3a20 312e  ils..Version: 1.
-00000030: 332e 350d 0a53 756d 6d61 7279 3a20 5369  3.5..Summary: Si
+00000030: 332e 360d 0a53 756d 6d61 7279 3a20 5369  3.6..Summary: Si
 00000040: 6d70 6c65 2061 6e64 2065 6c65 6761 6e74  mple and elegant
 00000050: 2075 7365 206f 6620 4661 7374 4170 6920   use of FastApi 
 00000060: 696e 204d 5643 206d 6f64 650d 0a48 6f6d  in MVC mode..Hom
 00000070: 652d 7061 6765 3a20 6874 7470 733a 2f2f  e-page: https://
 00000080: 6769 7468 7562 2e63 6f6d 2f73 6d6a 6b7a  github.com/smjkz
 00000090: 736c 2f69 7261 696c 730d 0a41 7574 686f  sl/irails..Autho
 000000a0: 723a 2042 7275 6365 2063 686f 750d 0a41  r: Bruce chou..A
@@ -48,271 +48,286 @@
 000002f0: 6e74 656e 742d 5479 7065 3a20 7465 7874  ntent-Type: text
 00000300: 2f6d 6172 6b64 6f77 6e0d 0a0d 0a23 2069  /markdown....# i
 00000310: 7261 696c 730d 0a41 206d 7663 2066 7261  rails..A mvc fra
 00000320: 6d65 776f 726b 2075 7365 6420 4661 7374  mework used Fast
 00000330: 4170 690d 0a53 696d 706c 6520 616e 6420  Api..Simple and 
 00000340: 656c 6567 616e 7420 7573 6520 6f66 2046  elegant use of F
 00000350: 6173 7441 7069 2069 6e20 4d56 4320 6d6f  astApi in MVC mo
-00000360: 6465 0d0a 0d0a 5b44 656d 6f5d 2868 7474  de....[Demo](htt
+00000360: 6465 0d0a 0d0a 5b44 6f63 735d 2868 7474  de....[Docs](htt
 00000370: 7073 3a2f 2f69 7261 696c 732e 3272 6169  ps://irails.2rai
 00000380: 6c73 2e63 6e2f 2920 0d0a 2320 5765 6c63  ls.cn/) ..# Welc
 00000390: 6f6d 6520 746f 2049 5241 494c 5328 7079  ome to IRAILS(py
 000003a0: 7468 6f6e 206f 6e20 7261 696c 7329 0d0a  thon on rails)..
 000003b0: 0d0a 200d 0a0d 0a23 2320 496e 7374 616c  .. ....## Instal
 000003c0: 6c61 7469 6f6e 2020 0d0a 0d0a 2a20 6070  lation  ....* `p
 000003d0: 6970 2069 6e73 7461 6c6c 2069 7261 696c  ip install irail
 000003e0: 7360 202d 2069 6e73 7461 6c6c 2069 7261  s` - install ira
 000003f0: 696c 730d 0a0d 0a23 2320 436f 6d6d 616e  ils....## Comman
 00000400: 6473 0d0a 0d0a 2a20 6069 7261 696c 7320  ds....* `irails 
 00000410: 7072 6f6a 6563 7420 5b70 726f 6a65 6374  project [project
 00000420: 2d6e 616d 6528 6469 722d 6e61 6d65 295d  -name(dir-name)]
-00000430: 6020 2d20 4372 6561 7465 2061 206e 6577  ` - Create a new
-00000440: 2069 7261 696c 7320 7072 6f6a 6563 742e   irails project.
-00000450: 0d0a 2a20 6069 7261 696c 7320 6170 7020  ..* `irails app 
-00000460: 5b61 7070 2d6e 616d 6528 6368 6f6f 7365  [app-name(choose
-00000470: 206f 7220 696e 7075 7420 6170 7073 2064   or input apps d
-00000480: 6972 295d 6020 2d20 4578 616d 706c 653a  ir)]` - Example:
-00000490: 2060 6972 6169 6c73 2061 7070 2061 646d   `irails app adm
-000004a0: 6973 7369 6f6e 7360 2043 7265 6174 6520  issions` Create 
-000004b0: 6120 6e65 7720 6972 6169 6c73 2061 7070  a new irails app
-000004c0: 2e0d 0a2a 2060 6972 6169 6c73 2072 756e  ...* `irails run
-000004d0: 205b 2d2d 706f 7274 2070 6f72 745d 6020   [--port port]` 
-000004e0: 2d20 5275 6e20 7072 6f6a 6563 7420 7669  - Run project vi
-000004f0: 7369 7420 6f6e 203c 6120 6872 6566 3d22  sit on <a href="
-00000500: 6874 7470 3a2f 2f31 3237 2e30 2e30 2e31  http://127.0.0.1
-00000510: 3a38 3030 3022 3e68 7474 703a 2f2f 3132  :8000">http://12
-00000520: 372e 302e 302e 313a 3830 3030 3c2f 613e  7.0.0.1:8000</a>
-00000530: 2e20 0d0a 200d 0a0d 0a23 2320 5072 6f6a  . .. ....## Proj
-00000540: 6563 7420 6c61 796f 7574 0d0a 6060 600d  ect layout..```.
-00000550: 0a20 0d0a 2020 2020 7c20 2020 6d61 696e  . ..    |   main
-00000560: 2e70 790d 0a20 2020 202b 2d2d 2d61 7070  .py..    +---app
-00000570: 7320 2020 2020 2020 2020 2020 2020 2020  s               
-00000580: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000590: 2023 2320 4170 7073 2063 6f6e 7461 696e   ## Apps contain
-000005a0: 6572 2028 4120 7072 6f6a 6563 7420 6361  er (A project ca
-000005b0: 6e20 6861 7665 206d 756c 7469 706c 6520  n have multiple 
-000005c0: 636f 6e74 6169 6e65 7273 290d 0a20 2020  containers)..   
-000005d0: 207c 2020 202b 2d2d 2d61 646d 6973 7369   |   +---admissi
-000005e0: 6f6e 7320 2020 2020 2020 2020 2020 2020  ons             
-000005f0: 2020 2020 2020 2020 2023 2320 4170 7020           ## App 
-00000600: 6469 7220 2841 6e20 6170 706c 6963 6174  dir (An applicat
-00000610: 696f 6e20 636f 6e74 6169 6e65 7220 6361  ion container ca
-00000620: 6e20 6861 7665 206d 756c 7469 706c 6520  n have multiple 
-00000630: 6170 706c 6963 6174 696f 6e73 290d 0a20  applications).. 
-00000640: 2020 207c 2020 207c 2020 207c 2020 205f     |   |   |   _
-00000650: 5f69 6e69 745f 5f2e 7079 2020 2020 2020  _init__.py      
-00000660: 2020 2020 2020 2020 2020 200d 0a20 2020             ..   
-00000670: 207c 2020 207c 2020 202b 2d2d 2d63 6f6e   |   |   +---con
-00000680: 7472 6f6c 6c65 7273 2020 2020 2020 2020  trollers        
-00000690: 2020 2020 2020 2020 2023 2320 436f 6e74           ## Cont
-000006a0: 726f 6c6c 6572 2066 696c 6573 0d0a 2020  roller files..  
-000006b0: 2020 7c20 2020 7c20 2020 7c20 2020 7c20    |   |   |   | 
-000006c0: 2020 686f 6d65 5f63 6f6e 7472 6f6c 6c65    home_controlle
-000006d0: 722e 7079 2020 2020 2020 2323 2043 6f6e  r.py      ## Con
-000006e0: 7472 6f6c 6c65 7220 636c 6173 7320 6669  troller class fi
-000006f0: 6c65 2c69 7427 7320 6c6f 6f6b 206c 696b  le,it's look lik
-00000700: 6520 6063 6c61 7373 2048 6f6d 6543 6f6e  e `class HomeCon
-00000710: 7472 6f6c 6c65 7260 0d0a 2020 2020 7c20  troller`..    | 
-00000720: 2020 7c20 2020 7c20 2020 7c20 2020 5f5f    |   |   |   __
-00000730: 696e 6974 5f5f 2e70 790d 0a20 2020 207c  init__.py..    |
-00000740: 2020 207c 2020 202b 2d2d 2d6c 6f63 616c     |   +---local
-00000750: 6573 2020 2020 2020 2020 2020 2020 2020  es              
-00000760: 2020 2020 2020 2023 2320 4931 386e 206c         ## I18n l
-00000770: 6f63 616c 6573 2064 6972 2c75 7365 2063  ocales dir,use c
-00000780: 6f6d 6d61 6e64 2060 6170 7073 2f61 7070  ommand `apps/app
-00000790: 3a24 2069 7261 6c69 7320 6931 386e 2067  :$ iralis i18n g
-000007a0: 6574 7465 7874 6020 7769 6c6c 2061 7574  ettext` will aut
-000007b0: 6f20 6765 6e65 7261 7465 2069 7465 6d73  o generate items
-000007c0: 0d0a 2020 2020 7c20 2020 7c20 2020 2b2d  ..    |   |   +-
-000007d0: 2d2d 6d6f 6465 6c73 2020 2020 2020 2020  --models        
-000007e0: 2020 2020 2020 2020 2020 2020 2020 2323                ##
-000007f0: 2044 6174 6162 6173 6520 6d6f 6465 6c73   Database models
-00000800: 2066 696c 6573 2869 6620 796f 7520 7573   files(if you us
-00000810: 6520 736f 6d65 2064 6174 6162 6173 6520  e some database 
-00000820: 7375 7070 6f72 7429 0d0a 2020 2020 7c20  support)..    | 
-00000830: 2020 7c20 2020 7c20 2020 2020 2020 5f5f    |   |       __
-00000840: 696e 6974 5f5f 2e70 790d 0a20 2020 207c  init__.py..    |
-00000850: 2020 207c 2020 202b 2d2d 2d73 6572 7669     |   +---servi
-00000860: 6365 7320 2020 2020 2020 2020 2020 2020  ces             
-00000870: 2020 2020 2020 2023 2320 4d6f 6475 6c65         ## Module
-00000880: 2066 6f72 2062 7573 696e 6573 7320 6c6f   for business lo
-00000890: 6769 6320 7072 6f63 6573 7369 6e67 0d0a  gic processing..
-000008a0: 2020 2020 7c20 2020 7c20 2020 2b2d 2d2d      |   |   +---
-000008b0: 7465 7374 7320 2020 2020 2020 2020 2020  tests           
-000008c0: 2020 2020 2020 2020 2020 2020 2323 2055              ## U
-000008d0: 6e69 7420 7465 7374 7469 6e67 0d0a 2020  nit testting..  
-000008e0: 2020 7c20 2020 7c20 2020 2b2d 2d2d 7669    |   |   +---vi
-000008f0: 6577 7320 2020 2020 2020 2020 2020 2020  ews             
-00000900: 2020 2020 2020 2020 2020 2323 2053 7461            ## Sta
-00000910: 7469 6320 7669 6577 2066 696c 6573 2028  tic view files (
-00000920: 7573 6520 604a 696e 6a61 3260 2054 656d  use `Jinja2` Tem
-00000930: 706c 6174 6529 0d0a 2020 2020 7c20 2020  plate)..    |   
-00000940: 7c20 2020 7c20 2020 7c20 2020 6c61 796f  |   |   |   layo
-00000950: 7574 2e68 746d 6c0d 0a20 2020 207c 2020  ut.html..    |  
-00000960: 207c 2020 207c 2020 207c 0d0a 2020 2020   |   |   |..    
-00000970: 7c20 2020 7c20 2020 7c20 2020 2b2d 2d2d  |   |   |   +---
-00000980: 686f 6d65 2020 2020 2020 2020 2020 2020  home            
-00000990: 2020 2020 2020 2020 2323 2054 6865 2063          ## The c
-000009a0: 6f6e 7472 6f6c 6c65 7220 6163 7469 6f6e  ontroller action
-000009b0: 2773 2073 7461 7469 6320 6669 6c65 286e  's static file(n
-000009c0: 616d 6520 6973 2073 616d 6520 746f 2074  ame is same to t
-000009d0: 6865 2063 6f6e 7472 6f6c 6c65 7227 7320  he controller's 
-000009e0: 636c 6173 7320 6e61 6d65 290d 0a20 2020  class name)..   
-000009f0: 207c 2020 207c 2020 207c 2020 207c 2020   |   |   |   |  
-00000a00: 2020 2020 2068 6f6d 652e 6373 7320 2020       home.css   
-00000a10: 2020 2020 2020 2020 200d 0a20 2020 207c           ..    |
-00000a20: 2020 207c 2020 207c 2020 207c 2020 2020     |   |   |    
-00000a30: 2020 2068 6f6d 652e 6874 6d6c 2020 2020     home.html    
-00000a40: 2020 2020 2020 2023 2320 5374 6174 6963         ## Static
-00000a50: 2066 696c 6520 636f 7272 6573 706f 6e64   file correspond
-00000a60: 696e 6720 746f 2061 6374 696f 6e28 6e61  ing to action(na
-00000a70: 6d65 2069 7320 7361 6d65 2074 6f20 7468  me is same to th
-00000a80: 6520 636f 6e74 726f 6c6c 6572 2773 206d  e controller's m
-00000a90: 6574 686f 6420 6e61 6d65 290d 0a20 2020  ethod name)..   
-00000aa0: 202b 2d2d 2d63 6f6e 6669 6773 2020 2020   +---configs    
-00000ab0: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000ac0: 2020 2020 2020 2020 2023 2320 5072 6f6a           ## Proj
-00000ad0: 6563 7420 636f 6e66 6967 7572 6520 6469  ect configure di
-00000ae0: 720d 0a20 2020 207c 2020 2020 2020 2061  r..    |       a
-00000af0: 6c65 6d62 6963 2e69 6e69 2020 2020 2020  lembic.ini      
-00000b00: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000b10: 2320 416c 656d 6269 6320 636f 6e66 6967  # Alembic config
-00000b20: 7572 6520 6669 6c65 2028 4765 6e65 7261  ure file (Genera
-00000b30: 6c6c 792c 2074 6865 7265 2069 7320 6e6f  lly, there is no
-00000b40: 206e 6565 6420 746f 2063 6861 6e67 652c   need to change,
-00000b50: 2075 7365 6420 7468 6520 6461 7461 6261   used the databa
-00000b60: 7365 206d 6967 7261 7469 6f6e 290d 0a20  se migration).. 
-00000b70: 2020 207c 2020 2020 2020 2063 6173 6269     |       casbi
-00000b80: 6e2d 6164 6170 7465 722e 6373 7620 2020  n-adapter.csv   
-00000b90: 2020 2020 2020 2020 2020 2023 2320 4361             ## Ca
-00000ba0: 7362 696e 2061 7574 6820 6d6f 6475 6c65  sbin auth module
-00000bb0: 2063 6f6e 6669 6720 6164 6170 7465 7220   config adapter 
-00000bc0: 6669 6c65 2829 0d0a 2020 2020 7c20 2020  file()..    |   
-00000bd0: 2020 2020 6361 7362 696e 2d6d 6f64 656c      casbin-model
-00000be0: 2e63 6f6e 6620 2020 2020 2020 2020 2020  .conf           
-00000bf0: 2020 2020 2323 2043 6173 6269 6e20 6175      ## Casbin au
-00000c00: 7468 2063 6f6e 6669 6720 6d6f 6465 6c0d  th config model.
-00000c10: 0a20 2020 207c 2020 2020 2020 2064 6174  .    |       dat
-00000c20: 6162 6173 652e 7961 6d6c 2020 2020 2020  abase.yaml      
-00000c30: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
-00000c40: 436f 6e66 6967 7572 6520 666f 7220 6461  Configure for da
-00000c50: 7461 6261 7365 2073 7570 706f 7274 0d0a  tabase support..
-00000c60: 2020 2020 7c20 2020 2020 2020 6765 6e65      |       gene
-00000c70: 7261 6c2e 7961 6d6c 2020 2020 2020 2020  ral.yaml        
-00000c80: 2020 2020 2020 2020 2020 2020 2323 2047              ## G
-00000c90: 656e 6572 616c 2063 6f6e 6669 6775 7265  eneral configure
-00000ca0: 730d 0a20 2020 207c 2020 2020 2020 2073  s..    |       s
-00000cb0: 6573 7369 6f6e 2e79 616d 6c20 2020 2020  ession.yaml     
-00000cc0: 2020 2020 2020 2020 2020 2020 2020 2023                 #
-00000cd0: 2320 5365 7373 696f 6e20 636f 6e66 6967  # Session config
-00000ce0: 7572 6573 0d0a 2020 2020 7c0d 0a20 2020  ures..    |..   
-00000cf0: 202b 2d2d 2d64 6174 610d 0a20 2020 207c   +---data..    |
-00000d00: 2020 202b 2d2d 2d61 6c65 6d62 6963 0d0a     +---alembic..
-00000d10: 2020 2020 7c20 2020 7c20 2020 5c2d 2d2d      |   |   \---
-00000d20: 7665 7273 696f 6e73 0d0a 2020 2020 7c20  versions..    | 
-00000d30: 2020 5c2d 2d2d 6462 0d0a 2020 2020 7c0d    \---db..    |.
-00000d40: 0a20 2020 202b 2d2d 2d70 7562 6c69 6320  .    +---public 
-00000d50: 2020 2020 2020 2020 2020 2020 2020 2020                  
-00000d60: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
-00000d70: 5075 626c 6963 2064 6972 2028 7769 6c6c  Public dir (will
-00000d80: 206d 6f75 6e74 6564 2074 6f20 7468 6520   mounted to the 
-00000d90: 272f 7075 626c 6963 2720 7572 6c29 0d0a  '/public' url)..
-00000da0: 2020 2020 7c20 2020 7c20 2020 6572 726f      |   |   erro
-00000db0: 725f 3430 342e 6874 6d6c 2020 2020 2020  r_404.html      
-00000dc0: 2020 2020 2020 2020 2020 2020 2323 2045              ## E
-00000dd0: 7272 6f72 2070 6167 6520 2e2e 2e0d 0a20  rror page ..... 
-00000de0: 2020 207c 2020 207c 2020 2065 7272 6f72     |   |   error
-00000df0: 5f35 3030 2e68 746d 6c0d 0a20 2020 207c  _500.html..    |
-00000e00: 0d0a 2020 2020 2b2d 2d2d 7570 6c6f 6164  ..    +---upload
-00000e10: 7320 2020 2020 2020 2020 2020 2020 2020  s               
-00000e20: 2020 2020 2020 2020 2020 2020 2020 2323                ##
-00000e30: 204f 7468 6572 7320 6469 7228 6966 2079   Others dir(if y
-00000e40: 6f75 7220 6e65 6564 206f 7220 6e6f 7429  our need or not)
-00000e50: 0d0a 6060 600d 0a23 2320 4578 7472 6173  ..```..## Extras
-00000e60: 2063 6f6d 6d61 6e64 730d 0a2a 2060 6972   commands..* `ir
-00000e70: 6169 6c73 2069 3138 6e20 6765 7474 6578  ails i18n gettex
-00000e80: 7460 202d 2d67 656e 6572 6174 6520 6931  t` --generate i1
-00000e90: 386e 2069 6e20 6972 6169 6c73 2061 7070  8n in irails app
-00000ea0: 2064 6972 0d0a 0d0a 2323 2054 616b 6520   dir....## Take 
-00000eb0: 6120 6c6f 6f6b 2063 6f6e 6669 6775 7265  a look configure
-00000ec0: 2066 696c 6520 6067 656e 6572 616c 2e79   file `general.y
-00000ed0: 616d 6c60 0d0a 200d 0a60 6060 200d 0a20  aml`.. ..``` .. 
-00000ee0: 2020 2061 7070 3a0d 0a20 2020 2020 2020     app:..       
-00000ef0: 2061 7070 6469 723a 0d0a 2020 2020 2020   appdir:..      
-00000f00: 2020 2d20 6170 7073 0d0a 2020 2020 2020    - apps..      
-00000f10: 2020 656e 6162 6c65 643a 206e 756c 6c0d    enabled: null.
-00000f20: 0a20 2020 2072 6f6f 743a 2061 7070 732e  .    root: apps.
-00000f30: 726f 6f74 0d0a 0d0a 2020 2020 636f 7273  root....    cors
-00000f40: 3a0d 0a20 2020 2020 2020 2061 6c6c 6f77  :..        allow
-00000f50: 5f63 7265 6465 6e74 6961 6c73 3a20 7472  _credentials: tr
-00000f60: 7565 0d0a 2020 2020 2020 2020 616c 6c6f  ue..        allo
-00000f70: 775f 6865 6164 6572 733a 0d0a 2020 2020  w_headers:..    
-00000f80: 2020 2020 2020 2020 2d20 272a 270d 0a20          - '*'.. 
-00000f90: 2020 2020 2020 2061 6c6c 6f77 5f6d 6574         allow_met
-00000fa0: 686f 6473 3a0d 0a20 2020 2020 2020 2020  hods:..         
-00000fb0: 2020 202d 2027 2a27 0d0a 2020 2020 2020     - '*'..      
-00000fc0: 2020 616c 6c6f 775f 6f72 6967 696e 733a    allow_origins:
-00000fd0: 0d0a 2020 2020 2020 2020 2020 2020 2d20  ..            - 
-00000fe0: 272a 270d 0a20 2020 2064 6562 7567 3a20  '*'..    debug: 
-00000ff0: 7472 7565 0d0a 2020 2020 6572 726f 7273  true..    errors
-00001000: 3a0d 0a20 2020 2020 2020 2065 7272 6f72  :..        error
-00001010: 5f34 3034 5f70 6167 653a 2027 7b52 4f4f  _404_page: '{ROO
-00001020: 542e 7075 626c 6963 5f64 6972 7d2f 6572  T.public_dir}/er
-00001030: 726f 725f 3430 342e 6874 6d6c 270d 0a20  ror_404.html'.. 
-00001040: 2020 2020 2020 2065 7272 6f72 5f35 3030         error_500
-00001050: 5f70 6167 653a 2027 7b52 4f4f 542e 7075  _page: '{ROOT.pu
-00001060: 626c 6963 5f64 6972 7d2f 6572 726f 725f  blic_dir}/error_
-00001070: 3530 302e 6874 6d6c 270d 0a20 2020 206c  500.html'..    l
-00001080: 6f67 3a0d 0a20 2020 2020 2020 2066 696c  og:..        fil
-00001090: 653a 2027 270d 0a20 2020 2020 2020 206c  e: ''..        l
-000010a0: 6576 656c 3a20 4445 4255 470d 0a20 2020  evel: DEBUG..   
-000010b0: 2020 2020 206e 616d 653a 2069 5261 696c       name: iRail
-000010c0: 730d 0a20 2020 2070 7562 6c69 635f 6469  s..    public_di
-000010d0: 723a 202e 2f70 7562 6c69 630d 0a0d 0a20  r: ./public.... 
-000010e0: 2020 2076 6965 773a 0d0a 2020 2020 2020     view:..      
-000010f0: 2020 6a69 6e6a 6132 3a0d 0a20 2020 2020    jinja2:..     
-00001100: 2020 2020 2020 2062 6c6f 636b 5f65 6e64         block_end
-00001110: 5f73 7472 696e 673a 2027 257d 270d 0a20  _string: '%}'.. 
-00001120: 2020 2020 2020 2020 2020 2062 6c6f 636b             block
-00001130: 5f73 7461 7274 5f73 7472 696e 673a 2027  _start_string: '
-00001140: 7b25 270d 0a20 2020 2020 2020 2020 2020  {%'..           
-00001150: 2063 6f6d 6d65 6e74 5f65 6e64 5f73 7472   comment_end_str
-00001160: 696e 673a 2027 237d 270d 0a20 2020 2020  ing: '#}'..     
-00001170: 2020 2020 2020 2063 6f6d 6d65 6e74 5f73         comment_s
-00001180: 7461 7274 5f73 7472 696e 673a 2027 7b23  tart_string: '{#
-00001190: 270d 0a20 2020 2020 2020 2020 2020 2076  '..            v
-000011a0: 6172 6961 626c 655f 656e 645f 7374 7269  ariable_end_stri
-000011b0: 6e67 3a20 277d 270d 0a20 2020 2020 2020  ng: '}'..       
-000011c0: 2020 2020 2076 6172 6961 626c 655f 7374       variable_st
-000011d0: 6172 745f 7374 7269 6e67 3a20 247b 0d0a  art_string: ${..
-000011e0: 2020 2020 2020 2020 7374 6174 6963 5f66          static_f
-000011f0: 6f72 6d61 743a 0d0a 2020 2020 2020 2020  ormat:..        
-00001200: 2d20 7675 650d 0a20 2020 2020 2020 202d  - vue..        -
-00001210: 2068 746d 6c0d 0a20 2020 2069 3138 6e3a   html..    i18n:
-00001220: 0d0a 2020 2020 2020 2020 6c61 6e67 3a20  ..        lang: 
-00001230: 5b27 7a68 275d 0d0a 2020 2020 2020 2020  ['zh']..        
-00001240: 7572 6c5f 6c61 6e67 5f6b 6579 3a20 276c  url_lang_key: 'l
-00001250: 616e 6727 0d0a 6060 600d 0a23 2320 5461  ang'..```..## Ta
-00001260: 6b65 2061 206c 6f6f 6b20 636f 6e74 726f  ke a look contro
-00001270: 6c6c 6572 2066 696c 6520 0d0a 200d 0a60  ller file .. ..`
-00001280: 6060 7079 7468 6f6e 0d0a 2020 2020 6672  ``python..    fr
-00001290: 6f6d 2069 7261 696c 7320 696d 706f 7274  om irails import
-000012a0: 2061 7069 5f72 6f75 7465 722c 6170 692c   api_router,api,
-000012b0: 5265 7175 6573 742c 5265 7370 6f6e 7365  Request,Response
-000012c0: 2c42 6173 6543 6f6e 7472 6f6c 6c65 722c  ,BaseController,
-000012d0: 6170 706c 6963 6174 696f 6e0d 0a20 0d0a  application.. ..
-000012e0: 2020 2020 4061 7069 5f72 6f75 7465 7228      @api_router(
-000012f0: 7061 7468 3d27 2f7b 636f 6e74 726f 6c6c  path='/{controll
-00001300: 6572 7d27 2c61 7574 683d 276e 6f6e 6527  er}',auth='none'
-00001310: 290d 0a20 2020 2063 6c61 7373 2041 646d  )..    class Adm
-00001320: 696e 436f 6e74 726f 6c6c 6572 2842 6173  inController(Bas
-00001330: 6543 6f6e 7472 6f6c 6c65 7229 3a20 0d0a  eController): ..
-00001340: 2020 2020 2020 2020 4061 7069 2e67 6574          @api.get
-00001350: 2822 2f69 6e64 6578 2229 0d0a 2020 2020  ("/index")..    
-00001360: 2020 2020 6465 6620 696e 6465 7828 7365      def index(se
-00001370: 6c66 293a 0d0a 2020 2020 2020 2020 2020  lf):..          
-00001380: 2020 2222 220d 0a20 2020 2020 2020 2020    """..         
-00001390: 2020 203a 7469 746c 6520 4164 6d69 6e0d     :title Admin.
-000013a0: 0a20 2020 2020 2020 2020 2020 2022 2222  .            """
-000013b0: 0d0a 2020 2020 2020 2020 2020 2020 7265  ..            re
-000013c0: 7475 726e 2073 656c 662e 7669 6577 2829  turn self.view()
-000013d0: 0d0a 6060 600d 0a                        ..```..
+00000430: 6020 2020 2020 2020 2020 2d20 4372 6561  `         - Crea
+00000440: 7465 2061 206e 6577 2069 7261 696c 7320  te a new irails 
+00000450: 7072 6f6a 6563 742e 0d0a 2a20 6069 7261  project...* `ira
+00000460: 696c 7320 6170 7020 5b61 7070 2d6e 616d  ils app [app-nam
+00000470: 6528 6368 6f6f 7365 206f 7220 696e 7075  e(choose or inpu
+00000480: 7420 6170 7073 2064 6972 295d 6020 2d20  t apps dir)]` - 
+00000490: 4578 616d 706c 653a 2060 6972 6169 6c73  Example: `irails
+000004a0: 2061 7070 2061 646d 6973 7369 6f6e 7360   app admissions`
+000004b0: 2043 7265 6174 6520 6120 6e65 7720 6972   Create a new ir
+000004c0: 6169 6c73 2061 7070 2e0d 0a2a 2060 6972  ails app...* `ir
+000004d0: 6169 6c73 2072 756e 205b 2d2d 686f 7374  ails run [--host
+000004e0: 2068 6f73 745d 205b 2d2d 706f 7274 2070   host] [--port p
+000004f0: 6f72 745d 6020 2020 2020 2020 2020 202d  ort]`          -
+00000500: 2052 756e 2070 726f 6a65 6374 2076 6973   Run project vis
+00000510: 6974 206f 6e20 5b68 7474 703a 2f2f 3132  it on [http://12
+00000520: 372e 302e 302e 313a 3830 3030 3e5d 2868  7.0.0.1:8000>](h
+00000530: 7474 703a 2f2f 3132 372e 302e 302e 313a  ttp://127.0.0.1:
+00000540: 3830 3030 292e 200d 0a2a 2060 6972 6169  8000). ..* `irai
+00000550: 6c73 2063 6f6e 7472 6f6c 6c65 7220 5b61  ls controller [a
+00000560: 6374 696f 6e73 2e2e 2e5d 6020 2020 2020  ctions...]`     
+00000570: 2020 2020 2020 2020 2020 2020 202d 2067               - g
+00000580: 656e 6572 6174 6520 6120 636f 6e74 726f  enerate a contro
+00000590: 6c6c 6572 2077 6974 6820 6769 7665 6e20  ller with given 
+000005a0: 6163 7469 6f6e 7328 6966 206e 6f20 6769  actions(if no gi
+000005b0: 7665 6e2c 6465 6661 6c75 7420 6973 202a  ven,defalut is *
+000005c0: 2a69 6e64 6578 2a2a 292e 200d 0a20 0d0a  *index**). .. ..
+000005d0: 0d0a 2323 2050 726f 6a65 6374 206c 6179  ..## Project lay
+000005e0: 6f75 740d 0a60 6060 0d0a 200d 0a20 2020  out..```.. ..   
+000005f0: 207c 2020 206d 6169 6e2e 7079 0d0a 2020   |   main.py..  
+00000600: 2020 2b2d 2d2d 6170 7073 2020 2020 2020    +---apps      
+00000610: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000620: 2020 2020 2020 2020 2020 2323 2041 7070            ## App
+00000630: 7320 636f 6e74 6169 6e65 7220 2841 2070  s container (A p
+00000640: 726f 6a65 6374 2063 616e 2068 6176 6520  roject can have 
+00000650: 6d75 6c74 6970 6c65 2063 6f6e 7461 696e  multiple contain
+00000660: 6572 7329 0d0a 2020 2020 7c20 2020 2b2d  ers)..    |   +-
+00000670: 2d2d 6164 6d69 7373 696f 6e73 2020 2020  --admissions    
+00000680: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000690: 2020 2323 2041 7070 2064 6972 2028 416e    ## App dir (An
+000006a0: 2061 7070 6c69 6361 7469 6f6e 2063 6f6e   application con
+000006b0: 7461 696e 6572 2063 616e 2068 6176 6520  tainer can have 
+000006c0: 6d75 6c74 6970 6c65 2061 7070 6c69 6361  multiple applica
+000006d0: 7469 6f6e 7329 0d0a 2020 2020 7c20 2020  tions)..    |   
+000006e0: 7c20 2020 7c20 2020 5f5f 696e 6974 5f5f  |   |   __init__
+000006f0: 2e70 7920 2020 2020 2020 2020 2020 2020  .py             
+00000700: 2020 2020 0d0a 2020 2020 7c20 2020 7c20      ..    |   | 
+00000710: 2020 2b2d 2d2d 636f 6e74 726f 6c6c 6572    +---controller
+00000720: 7320 2020 2020 2020 2020 2020 2020 2020  s               
+00000730: 2020 2323 2043 6f6e 7472 6f6c 6c65 7220    ## Controller 
+00000740: 6669 6c65 730d 0a20 2020 207c 2020 207c  files..    |   |
+00000750: 2020 207c 2020 207c 2020 2068 6f6d 655f     |   |   home_
+00000760: 636f 6e74 726f 6c6c 6572 2e70 7920 2020  controller.py   
+00000770: 2020 2023 2320 436f 6e74 726f 6c6c 6572     ## Controller
+00000780: 2063 6c61 7373 2066 696c 652c 6974 2773   class file,it's
+00000790: 206c 6f6f 6b20 6c69 6b65 2060 636c 6173   look like `clas
+000007a0: 7320 486f 6d65 436f 6e74 726f 6c6c 6572  s HomeController
+000007b0: 600d 0a20 2020 207c 2020 207c 2020 207c  `..    |   |   |
+000007c0: 2020 207c 2020 205f 5f69 6e69 745f 5f2e     |   __init__.
+000007d0: 7079 0d0a 2020 2020 7c20 2020 7c20 2020  py..    |   |   
+000007e0: 2b2d 2d2d 6c6f 6361 6c65 7320 2020 2020  +---locales     
+000007f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000800: 2323 2049 3138 6e20 6c6f 6361 6c65 7320  ## I18n locales 
+00000810: 6469 722c 7573 6520 636f 6d6d 616e 6420  dir,use command 
+00000820: 6061 7070 732f 6170 703a 2420 6972 616c  `apps/app:$ iral
+00000830: 6973 2069 3138 6e20 6765 7474 6578 7460  is i18n gettext`
+00000840: 2077 696c 6c20 6175 746f 2067 656e 6572   will auto gener
+00000850: 6174 6520 6974 656d 730d 0a20 2020 207c  ate items..    |
+00000860: 2020 207c 2020 202b 2d2d 2d6d 6f64 656c     |   +---model
+00000870: 7320 2020 2020 2020 2020 2020 2020 2020  s               
+00000880: 2020 2020 2020 2023 2320 4461 7461 6261         ## Databa
+00000890: 7365 206d 6f64 656c 7320 6669 6c65 7328  se models files(
+000008a0: 6966 2079 6f75 2075 7365 2073 6f6d 6520  if you use some 
+000008b0: 6461 7461 6261 7365 2073 7570 706f 7274  database support
+000008c0: 290d 0a20 2020 207c 2020 207c 2020 207c  )..    |   |   |
+000008d0: 2020 2020 2020 205f 5f69 6e69 745f 5f2e         __init__.
+000008e0: 7079 0d0a 2020 2020 7c20 2020 7c20 2020  py..    |   |   
+000008f0: 2b2d 2d2d 7365 7276 6963 6573 2020 2020  +---services    
+00000900: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000910: 2323 204d 6f64 756c 6520 666f 7220 6275  ## Module for bu
+00000920: 7369 6e65 7373 206c 6f67 6963 2070 726f  siness logic pro
+00000930: 6365 7373 696e 670d 0a20 2020 207c 2020  cessing..    |  
+00000940: 207c 2020 202b 2d2d 2d74 6573 7473 2020   |   +---tests  
+00000950: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000960: 2020 2020 2023 2320 556e 6974 2074 6573       ## Unit tes
+00000970: 7474 696e 670d 0a20 2020 207c 2020 207c  tting..    |   |
+00000980: 2020 202b 2d2d 2d76 6965 7773 2020 2020     +---views    
+00000990: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000009a0: 2020 2023 2320 5374 6174 6963 2076 6965     ## Static vie
+000009b0: 7720 6669 6c65 7320 2875 7365 2060 4a69  w files (use `Ji
+000009c0: 6e6a 6132 6020 5465 6d70 6c61 7465 290d  nja2` Template).
+000009d0: 0a20 2020 207c 2020 207c 2020 207c 2020  .    |   |   |  
+000009e0: 207c 2020 206c 6179 6f75 742e 6874 6d6c   |   layout.html
+000009f0: 0d0a 2020 2020 7c20 2020 7c20 2020 7c20  ..    |   |   | 
+00000a00: 2020 7c0d 0a20 2020 207c 2020 207c 2020    |..    |   |  
+00000a10: 207c 2020 202b 2d2d 2d68 6f6d 6520 2020   |   +---home   
+00000a20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a30: 2023 2320 5468 6520 636f 6e74 726f 6c6c   ## The controll
+00000a40: 6572 2061 6374 696f 6e27 7320 7374 6174  er action's stat
+00000a50: 6963 2066 696c 6528 6e61 6d65 2069 7320  ic file(name is 
+00000a60: 7361 6d65 2074 6f20 7468 6520 636f 6e74  same to the cont
+00000a70: 726f 6c6c 6572 2773 2063 6c61 7373 206e  roller's class n
+00000a80: 616d 6529 0d0a 2020 2020 7c20 2020 7c20  ame)..    |   | 
+00000a90: 2020 7c20 2020 7c20 2020 2020 2020 686f    |   |       ho
+00000aa0: 6d65 2e63 7373 2020 2020 2020 2020 2020  me.css          
+00000ab0: 2020 0d0a 2020 2020 7c20 2020 7c20 2020    ..    |   |   
+00000ac0: 7c20 2020 7c20 2020 2020 2020 686f 6d65  |   |       home
+00000ad0: 2e68 746d 6c20 2020 2020 2020 2020 2020  .html           
+00000ae0: 2323 2053 7461 7469 6320 6669 6c65 2063  ## Static file c
+00000af0: 6f72 7265 7370 6f6e 6469 6e67 2074 6f20  orresponding to 
+00000b00: 6163 7469 6f6e 286e 616d 6520 6973 2073  action(name is s
+00000b10: 616d 6520 746f 2074 6865 2063 6f6e 7472  ame to the contr
+00000b20: 6f6c 6c65 7227 7320 6d65 7468 6f64 206e  oller's method n
+00000b30: 616d 6529 0d0a 2020 2020 2b2d 2d2d 636f  ame)..    +---co
+00000b40: 6e66 6967 7320 2020 2020 2020 2020 2020  nfigs           
+00000b50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000b60: 2020 2323 2050 726f 6a65 6374 2063 6f6e    ## Project con
+00000b70: 6669 6775 7265 2064 6972 0d0a 2020 2020  figure dir..    
+00000b80: 7c20 2020 2020 2020 616c 656d 6269 632e  |       alembic.
+00000b90: 696e 6920 2020 2020 2020 2020 2020 2020  ini             
+00000ba0: 2020 2020 2020 2020 2323 2041 6c65 6d62          ## Alemb
+00000bb0: 6963 2063 6f6e 6669 6775 7265 2066 696c  ic configure fil
+00000bc0: 6520 2847 656e 6572 616c 6c79 2c20 7468  e (Generally, th
+00000bd0: 6572 6520 6973 206e 6f20 6e65 6564 2074  ere is no need t
+00000be0: 6f20 6368 616e 6765 2c20 7573 6564 2074  o change, used t
+00000bf0: 6865 2064 6174 6162 6173 6520 6d69 6772  he database migr
+00000c00: 6174 696f 6e29 0d0a 2020 2020 7c20 2020  ation)..    |   
+00000c10: 2020 2020 6361 7362 696e 2d61 6461 7074      casbin-adapt
+00000c20: 6572 2e63 7376 2020 2020 2020 2020 2020  er.csv          
+00000c30: 2020 2020 2323 2043 6173 6269 6e20 6175      ## Casbin au
+00000c40: 7468 206d 6f64 756c 6520 636f 6e66 6967  th module config
+00000c50: 2061 6461 7074 6572 2066 696c 6528 290d   adapter file().
+00000c60: 0a20 2020 207c 2020 2020 2020 2063 6173  .    |       cas
+00000c70: 6269 6e2d 6d6f 6465 6c2e 636f 6e66 2020  bin-model.conf  
+00000c80: 2020 2020 2020 2020 2020 2020 2023 2320               ## 
+00000c90: 4361 7362 696e 2061 7574 6820 636f 6e66  Casbin auth conf
+00000ca0: 6967 206d 6f64 656c 0d0a 2020 2020 7c20  ig model..    | 
+00000cb0: 2020 2020 2020 6461 7461 6261 7365 2e79        database.y
+00000cc0: 616d 6c20 2020 2020 2020 2020 2020 2020  aml             
+00000cd0: 2020 2020 2020 2323 2043 6f6e 6669 6775        ## Configu
+00000ce0: 7265 2066 6f72 2064 6174 6162 6173 6520  re for database 
+00000cf0: 7375 7070 6f72 740d 0a20 2020 207c 2020  support..    |  
+00000d00: 2020 2020 2067 656e 6572 616c 2e79 616d       general.yam
+00000d10: 6c20 2020 2020 2020 2020 2020 2020 2020  l               
+00000d20: 2020 2020 2023 2320 4765 6e65 7261 6c20       ## General 
+00000d30: 636f 6e66 6967 7572 6573 0d0a 2020 2020  configures..    
+00000d40: 7c20 2020 2020 2020 7365 7373 696f 6e2e  |       session.
+00000d50: 7961 6d6c 2020 2020 2020 2020 2020 2020  yaml            
+00000d60: 2020 2020 2020 2020 2323 2053 6573 7369          ## Sessi
+00000d70: 6f6e 2063 6f6e 6669 6775 7265 730d 0a20  on configures.. 
+00000d80: 2020 207c 0d0a 2020 2020 2b2d 2d2d 6461     |..    +---da
+00000d90: 7461 0d0a 2020 2020 7c20 2020 2b2d 2d2d  ta..    |   +---
+00000da0: 616c 656d 6269 630d 0a20 2020 207c 2020  alembic..    |  
+00000db0: 207c 2020 205c 2d2d 2d76 6572 7369 6f6e   |   \---version
+00000dc0: 730d 0a20 2020 207c 2020 205c 2d2d 2d64  s..    |   \---d
+00000dd0: 620d 0a20 2020 207c 0d0a 2020 2020 2b2d  b..    |..    +-
+00000de0: 2d2d 7075 626c 6963 2020 2020 2020 2020  --public        
+00000df0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000e00: 2020 2020 2020 2323 2050 7562 6c69 6320        ## Public 
+00000e10: 6469 7220 2877 696c 6c20 6d6f 756e 7465  dir (will mounte
+00000e20: 6420 746f 2074 6865 2027 2f70 7562 6c69  d to the '/publi
+00000e30: 6327 2075 726c 290d 0a20 2020 207c 2020  c' url)..    |  
+00000e40: 207c 2020 2065 7272 6f72 5f34 3034 2e68   |   error_404.h
+00000e50: 746d 6c20 2020 2020 2020 2020 2020 2020  tml             
+00000e60: 2020 2020 2023 2320 4572 726f 7220 7061       ## Error pa
+00000e70: 6765 202e 2e2e 0d0a 2020 2020 7c20 2020  ge .....    |   
+00000e80: 7c20 2020 6572 726f 725f 3530 302e 6874  |   error_500.ht
+00000e90: 6d6c 0d0a 2020 2020 7c0d 0a20 2020 202b  ml..    |..    +
+00000ea0: 2d2d 2d75 706c 6f61 6473 2020 2020 2020  ---uploads      
+00000eb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000ec0: 2020 2020 2020 2023 2320 4f74 6865 7273         ## Others
+00000ed0: 2064 6972 2869 6620 796f 7572 206e 6565   dir(if your nee
+00000ee0: 6420 6f72 206e 6f74 290d 0a60 6060 0d0a  d or not)..```..
+00000ef0: 2323 2045 7874 7261 7320 636f 6d6d 616e  ## Extras comman
+00000f00: 6473 0d0a 2a20 6069 7261 696c 7320 6931  ds..* `irails i1
+00000f10: 386e 2067 6574 7465 7874 6020 202d 2d67  8n gettext`  --g
+00000f20: 656e 6572 6174 6520 6931 386e 2069 6e20  enerate i18n in 
+00000f30: 6972 6169 6c73 2061 7070 2064 6972 0d0a  irails app dir..
+00000f40: 2a20 6069 7261 696c 7320 7368 656c 6c60  * `irails shell`
+00000f50: 2020 2020 2020 2020 202d 2d72 756e 2070           --run p
+00000f60: 7974 686f 6e20 696e 7465 7270 7265 7465  ython interprete
+00000f70: 7220 7769 7468 2062 7569 6c64 696e 2073  r with buildin s
+00000f80: 7570 706f 7274 2063 6f6e 7465 7874 7320  upport contexts 
+00000f90: 0d0a 0d0a 2323 2054 616b 6520 6120 6c6f  ....## Take a lo
+00000fa0: 6f6b 2063 6f6e 6669 6775 7265 2066 696c  ok configure fil
+00000fb0: 6520 6067 656e 6572 616c 2e79 616d 6c60  e `general.yaml`
+00000fc0: 0d0a 200d 0a60 6060 200d 0a20 2020 2061  .. ..``` ..    a
+00000fd0: 7070 3a0d 0a20 2020 2020 2020 2061 7070  pp:..        app
+00000fe0: 6469 723a 0d0a 2020 2020 2020 2020 2d20  dir:..        - 
+00000ff0: 6170 7073 0d0a 2020 2020 2020 2020 656e  apps..        en
+00001000: 6162 6c65 643a 206e 756c 6c0d 0a20 2020  abled: null..   
+00001010: 2072 6f6f 743a 2061 7070 732e 726f 6f74   root: apps.root
+00001020: 0d0a 0d0a 2020 2020 636f 7273 3a0d 0a20  ....    cors:.. 
+00001030: 2020 2020 2020 2061 6c6c 6f77 5f63 7265         allow_cre
+00001040: 6465 6e74 6961 6c73 3a20 7472 7565 0d0a  dentials: true..
+00001050: 2020 2020 2020 2020 616c 6c6f 775f 6865          allow_he
+00001060: 6164 6572 733a 0d0a 2020 2020 2020 2020  aders:..        
+00001070: 2020 2020 2d20 272a 270d 0a20 2020 2020      - '*'..     
+00001080: 2020 2061 6c6c 6f77 5f6d 6574 686f 6473     allow_methods
+00001090: 3a0d 0a20 2020 2020 2020 2020 2020 202d  :..            -
+000010a0: 2027 2a27 0d0a 2020 2020 2020 2020 616c   '*'..        al
+000010b0: 6c6f 775f 6f72 6967 696e 733a 0d0a 2020  low_origins:..  
+000010c0: 2020 2020 2020 2020 2020 2d20 272a 270d            - '*'.
+000010d0: 0a20 2020 2064 6562 7567 3a20 7472 7565  .    debug: true
+000010e0: 0d0a 2020 2020 6572 726f 7273 3a0d 0a20  ..    errors:.. 
+000010f0: 2020 2020 2020 2065 7272 6f72 5f34 3034         error_404
+00001100: 5f70 6167 653a 2027 7b52 4f4f 542e 7075  _page: '{ROOT.pu
+00001110: 626c 6963 5f64 6972 7d2f 6572 726f 725f  blic_dir}/error_
+00001120: 3430 342e 6874 6d6c 270d 0a20 2020 2020  404.html'..     
+00001130: 2020 2065 7272 6f72 5f35 3030 5f70 6167     error_500_pag
+00001140: 653a 2027 7b52 4f4f 542e 7075 626c 6963  e: '{ROOT.public
+00001150: 5f64 6972 7d2f 6572 726f 725f 3530 302e  _dir}/error_500.
+00001160: 6874 6d6c 270d 0a20 2020 206c 6f67 3a0d  html'..    log:.
+00001170: 0a20 2020 2020 2020 2066 696c 653a 2027  .        file: '
+00001180: 270d 0a20 2020 2020 2020 206c 6576 656c  '..        level
+00001190: 3a20 4445 4255 470d 0a20 2020 2020 2020  : DEBUG..       
+000011a0: 206e 616d 653a 2069 5261 696c 730d 0a20   name: iRails.. 
+000011b0: 2020 2070 7562 6c69 635f 6469 723a 202e     public_dir: .
+000011c0: 2f70 7562 6c69 630d 0a0d 0a20 2020 2076  /public....    v
+000011d0: 6965 773a 0d0a 2020 2020 2020 2020 6a69  iew:..        ji
+000011e0: 6e6a 6132 3a0d 0a20 2020 2020 2020 2020  nja2:..         
+000011f0: 2020 2062 6c6f 636b 5f65 6e64 5f73 7472     block_end_str
+00001200: 696e 673a 2027 257d 270d 0a20 2020 2020  ing: '%}'..     
+00001210: 2020 2020 2020 2062 6c6f 636b 5f73 7461         block_sta
+00001220: 7274 5f73 7472 696e 673a 2027 7b25 270d  rt_string: '{%'.
+00001230: 0a20 2020 2020 2020 2020 2020 2063 6f6d  .            com
+00001240: 6d65 6e74 5f65 6e64 5f73 7472 696e 673a  ment_end_string:
+00001250: 2027 237d 270d 0a20 2020 2020 2020 2020   '#}'..         
+00001260: 2020 2063 6f6d 6d65 6e74 5f73 7461 7274     comment_start
+00001270: 5f73 7472 696e 673a 2027 7b23 270d 0a20  _string: '{#'.. 
+00001280: 2020 2020 2020 2020 2020 2076 6172 6961             varia
+00001290: 626c 655f 656e 645f 7374 7269 6e67 3a20  ble_end_string: 
+000012a0: 277d 270d 0a20 2020 2020 2020 2020 2020  '}'..           
+000012b0: 2076 6172 6961 626c 655f 7374 6172 745f   variable_start_
+000012c0: 7374 7269 6e67 3a20 247b 0d0a 2020 2020  string: ${..    
+000012d0: 2020 2020 7374 6174 6963 5f66 6f72 6d61      static_forma
+000012e0: 743a 0d0a 2020 2020 2020 2020 2d20 7675  t:..        - vu
+000012f0: 650d 0a20 2020 2020 2020 202d 2068 746d  e..        - htm
+00001300: 6c0d 0a20 2020 2069 3138 6e3a 0d0a 2020  l..    i18n:..  
+00001310: 2020 2020 2020 6c61 6e67 3a20 5b27 7a68        lang: ['zh
+00001320: 275d 0d0a 2020 2020 2020 2020 7572 6c5f  ']..        url_
+00001330: 6c61 6e67 5f6b 6579 3a20 276c 616e 6727  lang_key: 'lang'
+00001340: 0d0a 6060 600d 0a23 2320 5461 6b65 2061  ..```..## Take a
+00001350: 206c 6f6f 6b20 636f 6e74 726f 6c6c 6572   look controller
+00001360: 2066 696c 6520 0d0a 200d 0a60 6060 7079   file .. ..```py
+00001370: 7468 6f6e 0d0a 2020 2020 6672 6f6d 2069  thon..    from i
+00001380: 7261 696c 7320 696d 706f 7274 2061 7069  rails import api
+00001390: 5f72 6f75 7465 722c 6170 692c 5265 7175  _router,api,Requ
+000013a0: 6573 742c 5265 7370 6f6e 7365 2c42 6173  est,Response,Bas
+000013b0: 6543 6f6e 7472 6f6c 6c65 722c 6170 706c  eController,appl
+000013c0: 6963 6174 696f 6e0d 0a20 0d0a 2020 2020  ication.. ..    
+000013d0: 4061 7069 5f72 6f75 7465 7228 7061 7468  @api_router(path
+000013e0: 3d27 2f7b 636f 6e74 726f 6c6c 6572 7d27  ='/{controller}'
+000013f0: 2c61 7574 683d 276e 6f6e 6527 290d 0a20  ,auth='none').. 
+00001400: 2020 2063 6c61 7373 2041 646d 696e 436f     class AdminCo
+00001410: 6e74 726f 6c6c 6572 2842 6173 6543 6f6e  ntroller(BaseCon
+00001420: 7472 6f6c 6c65 7229 3a20 0d0a 2020 2020  troller): ..    
+00001430: 2020 2020 4061 7069 2e67 6574 2822 2f69      @api.get("/i
+00001440: 6e64 6578 2229 0d0a 2020 2020 2020 2020  ndex")..        
+00001450: 6465 6620 696e 6465 7828 7365 6c66 293a  def index(self):
+00001460: 0d0a 2020 2020 2020 2020 2020 2020 2222  ..            ""
+00001470: 220d 0a20 2020 2020 2020 2020 2020 203a  "..            :
+00001480: 7469 746c 6520 4164 6d69 6e0d 0a20 2020  title Admin..   
+00001490: 2020 2020 2020 2020 2022 2222 0d0a 2020           """..  
+000014a0: 2020 2020 2020 2020 2020 7265 7475 726e            return
+000014b0: 2073 656c 662e 7669 6577 2829 0d0a 6060   self.view()..``
+000014c0: 600d 0a                                  `..
```

### Comparing `irails-1.3.5/irails.egg-info/SOURCES.txt` & `irails-1.3.6/irails.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `irails-1.3.5/irails.egg-info/requires.txt` & `irails-1.3.6/irails.egg-info/requires.txt`

 * *Files 14% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 simpleeval==0.9.13
 sniffio==1.3.0
 SQLAlchemy==2.0.9
 starlette==0.26.1
 typing-extensions==4.5.0
 typing-inspect==0.8.0
 ujson==5.5.0
-urllib3==1.26.15
+urllib3==2.0.2
 uvicorn==0.21.1
 watchfiles==0.19.0
 websockets==11.0.2
 yarg==0.1.9
 chardet==5.1.0
-polib
-mkdocs
+polib==1.2.0
+httpx==0.24.0
```

### Comparing `irails-1.3.5/setup.py` & `irails-1.3.6/setup.py`

 * *Files identical despite different names*

