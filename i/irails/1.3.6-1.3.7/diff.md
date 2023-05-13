# Comparing `tmp/irails-1.3.6.tar.gz` & `tmp/irails-1.3.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "irails-1.3.6.tar", last modified: Sat May 13 06:11:24 2023, max compression
+gzip compressed data, was "irails-1.3.7.tar", last modified: Sat May 13 06:16:05 2023, max compression
```

## Comparing `irails-1.3.6.tar` & `irails-1.3.7.tar`

### file list

```diff
@@ -1,88 +1,88 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.763029 irails-1.3.6/
--rw-rw-rw-   0        0        0       83 2023-05-04 04:10:30.000000 irails-1.3.6/MANIFEST.in
--rw-rw-rw-   0        0        0     5315 2023-05-13 06:11:24.752058 irails-1.3.6/PKG-INFO
--rw-rw-rw-   0        0        0     4532 2023-05-13 06:11:01.000000 irails-1.3.6/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.671378 irails-1.3.6/irails/
--rw-rw-rw-   0        0        0      306 2023-05-13 05:44:35.000000 irails-1.3.6/irails/__init__.py
--rw-rw-rw-   0        0        0     3409 2023-05-13 06:08:26.000000 irails-1.3.6/irails/_i18n.py
--rw-rw-rw-   0        0        0     2445 2023-05-11 15:39:57.000000 irails-1.3.6/irails/_loader.py
--rw-rw-rw-   0        0        0     2390 2023-04-27 14:23:55.000000 irails-1.3.6/irails/_utils.py
--rw-rw-rw-   0        0        0    11722 2023-05-11 15:21:25.000000 irails-1.3.6/irails/auth.py
--rw-rw-rw-   0        0        0    12426 2023-05-13 05:30:29.000000 irails-1.3.6/irails/base_controller.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.683900 irails-1.3.6/irails/casbin_adapters/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.685894 irails-1.3.6/irails/casbin_adapters/__pycache__/
--rw-rw-rw-   0        0        0    17834 2023-04-30 14:29:09.000000 irails-1.3.6/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc
--rw-rw-rw-   0        0        0    10589 2023-05-13 05:03:07.000000 irails-1.3.6/irails/casbin_adapters/sqlalchemy_adapter.py
--rw-rw-rw-   0        0        0     4381 2023-02-25 09:43:32.000000 irails-1.3.6/irails/cbv.py
--rw-rw-rw-   0        0        0     6065 2023-05-11 15:19:41.000000 irails-1.3.6/irails/config.py
--rw-rw-rw-   0        0        0    12478 2023-05-12 05:56:24.000000 irails-1.3.6/irails/controller_utils.py
--rw-rw-rw-   0        0        0    32319 2023-05-12 06:03:46.000000 irails-1.3.6/irails/core.py
--rw-rw-rw-   0        0        0     6409 2023-05-11 15:21:34.000000 irails-1.3.6/irails/database.py
--rw-rw-rw-   0        0        0     1459 2023-05-11 15:27:11.000000 irails-1.3.6/irails/log.py
--rw-rw-rw-   0        0        0     8673 2023-05-11 15:20:30.000000 irails-1.3.6/irails/midware.py
--rw-rw-rw-   0        0        0     2141 2023-04-03 14:30:15.000000 irails-1.3.6/irails/midware_casbin.py
--rw-rw-rw-   0        0        0     9341 2023-05-11 15:20:39.000000 irails-1.3.6/irails/midware_session.py
--rw-rw-rw-   0        0        0     4200 2023-04-27 11:53:07.000000 irails-1.3.6/irails/mvc_router.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.694213 irails-1.3.6/irails/scripts/
--rw-rw-rw-   0        0        0        0 2023-04-26 07:44:41.000000 irails-1.3.6/irails/scripts/__init__.py
--rw-rw-rw-   0        0        0     7811 2023-05-11 15:34:41.000000 irails-1.3.6/irails/scripts/_app.py
--rw-rw-rw-   0        0        0     7690 2023-05-09 06:52:08.000000 irails-1.3.6/irails/scripts/_controller.py
--rw-rw-rw-   0        0        0     7755 2023-05-13 05:57:18.000000 irails-1.3.6/irails/scripts/_i18n.py
--rw-rw-rw-   0        0        0     2301 2023-05-03 14:35:33.000000 irails-1.3.6/irails/scripts/_project.py
--rw-rw-rw-   0        0        0     1600 2023-05-11 15:45:21.000000 irails-1.3.6/irails/scripts/_run.py
--rw-rw-rw-   0        0        0     2288 2023-05-11 14:15:32.000000 irails-1.3.6/irails/scripts/_shell.py
--rw-rw-rw-   0        0        0     1855 2023-05-11 12:33:17.000000 irails-1.3.6/irails/scripts/main.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.635352 irails-1.3.6/irails/scripts/tpls/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.705184 irails-1.3.6/irails/scripts/tpls/app/
--rw-rw-rw-   0        0        0      223 2023-05-09 15:18:47.000000 irails-1.3.6/irails/scripts/tpls/app/controller.tpl
--rw-rw-rw-   0        0        0        0 2023-04-28 06:03:05.000000 irails-1.3.6/irails/scripts/tpls/app/css.tpl
--rw-rw-rw-   0        0        0      791 2023-04-25 10:42:10.000000 irails-1.3.6/irails/scripts/tpls/app/home.css.tpl
--rw-rw-rw-   0        0        0     1293 2023-05-05 10:16:42.000000 irails-1.3.6/irails/scripts/tpls/app/home.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 11:52:26.000000 irails-1.3.6/irails/scripts/tpls/app/model.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 11:52:38.000000 irails-1.3.6/irails/scripts/tpls/app/service.tpl
--rw-rw-rw-   0        0        0        0 2023-04-25 12:03:35.000000 irails-1.3.6/irails/scripts/tpls/app/test.tpl
--rw-rw-rw-   0        0        0       18 2023-05-02 08:56:04.000000 irails-1.3.6/irails/scripts/tpls/app/view.tpl
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.708175 irails-1.3.6/irails/scripts/tpls/project/
--rw-rw-rw-   0        0        0      139 2023-04-23 09:46:24.000000 irails-1.3.6/irails/scripts/tpls/project/.gitignore
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.709173 irails-1.3.6/irails/scripts/tpls/project/apps/
--rw-rw-rw-   0        0        0        0 2023-04-26 09:58:51.000000 irails-1.3.6/irails/scripts/tpls/project/apps/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.721141 irails-1.3.6/irails/scripts/tpls/project/configs/
--rw-rw-rw-   0        0        0      746 2023-05-09 06:45:34.000000 irails-1.3.6/irails/scripts/tpls/project/configs/alembic.ini
--rw-rw-rw-   0        0        0      198 2023-05-09 06:44:21.000000 irails-1.3.6/irails/scripts/tpls/project/configs/authencation.yaml
--rw-rw-rw-   0        0        0        0 2023-03-06 08:27:07.000000 irails-1.3.6/irails/scripts/tpls/project/configs/cache.yaml
--rw-rw-rw-   0        0        0      104 2023-05-04 05:06:32.000000 irails-1.3.6/irails/scripts/tpls/project/configs/casbin-adapter.csv
--rw-rw-rw-   0        0        0      302 2023-05-04 05:24:51.000000 irails-1.3.6/irails/scripts/tpls/project/configs/casbin-model.conf
--rw-rw-rw-   0        0        0      817 2023-05-10 10:45:36.000000 irails-1.3.6/irails/scripts/tpls/project/configs/database.yaml
--rw-rw-rw-   0        0        0      748 2023-05-11 05:35:06.000000 irails-1.3.6/irails/scripts/tpls/project/configs/general.yaml
--rw-rw-rw-   0        0        0      337 2023-04-22 10:54:12.000000 irails-1.3.6/irails/scripts/tpls/project/configs/session.yaml
--rw-rw-rw-   0        0        0      272 2023-05-09 06:44:59.000000 irails-1.3.6/irails/scripts/tpls/project/configs/upload.yaml
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.638904 irails-1.3.6/irails/scripts/tpls/project/data/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.725130 irails-1.3.6/irails/scripts/tpls/project/data/alembic/
--rw-rw-rw-   0        0        0       38 2023-04-09 12:01:20.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/README
--rw-rw-rw-   0        0        0     2144 2023-04-30 09:03:04.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/env.py
--rw-rw-rw-   0        0        0      510 2023-04-09 12:01:20.000000 irails-1.3.6/irails/scripts/tpls/project/data/alembic/script.py.mako
--rw-rw-rw-   0        0        0      231 2023-05-11 15:42:13.000000 irails-1.3.6/irails/scripts/tpls/project/main.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.727124 irails-1.3.6/irails/scripts/tpls/project/public/
--rw-rw-rw-   0        0        0     1233 2023-05-02 08:46:22.000000 irails-1.3.6/irails/scripts/tpls/project/public/error_404.html
--rw-rw-rw-   0        0        0     1083 2023-05-02 08:46:46.000000 irails-1.3.6/irails/scripts/tpls/project/public/error_500.html
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.731145 irails-1.3.6/irails/scripts/tpls/project/public/libs/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.642117 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.736107 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/
--rw-rw-rw-   0        0        0  1970121 2023-04-23 08:02:36.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.742084 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/
--rw-rw-rw-   0        0        0   323666 2023-04-23 08:04:13.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css
--rw-rw-rw-   0        0        0      725 2023-04-21 12:39:53.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js
--rw-rw-rw-   0        0        0  1441055 2023-04-21 07:36:37.000000 irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.644117 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.748069 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/
--rw-rw-rw-   0        0        0   640610 2023-04-21 07:36:07.000000 irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js
--rw-rw-rw-   0        0        0     2887 2023-05-12 05:35:40.000000 irails-1.3.6/irails/view.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:11:24.681358 irails-1.3.6/irails.egg-info/
--rw-rw-rw-   0        0        0     5315 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2326 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      778 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 06:11:24.000000 irails-1.3.6/irails.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 06:11:24.763029 irails-1.3.6/setup.cfg
--rw-rw-rw-   0        0        0     2551 2023-05-09 11:27:27.000000 irails-1.3.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.129498 irails-1.3.7/
+-rw-rw-rw-   0        0        0       83 2023-05-04 04:10:30.000000 irails-1.3.7/MANIFEST.in
+-rw-rw-rw-   0        0        0     5315 2023-05-13 06:16:05.128492 irails-1.3.7/PKG-INFO
+-rw-rw-rw-   0        0        0     4532 2023-05-13 06:11:01.000000 irails-1.3.7/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.061883 irails-1.3.7/irails/
+-rw-rw-rw-   0        0        0      306 2023-05-13 06:15:56.000000 irails-1.3.7/irails/__init__.py
+-rw-rw-rw-   0        0        0     3409 2023-05-13 06:08:26.000000 irails-1.3.7/irails/_i18n.py
+-rw-rw-rw-   0        0        0     2445 2023-05-11 15:39:57.000000 irails-1.3.7/irails/_loader.py
+-rw-rw-rw-   0        0        0     2390 2023-04-27 14:23:55.000000 irails-1.3.7/irails/_utils.py
+-rw-rw-rw-   0        0        0    11722 2023-05-11 15:21:25.000000 irails-1.3.7/irails/auth.py
+-rw-rw-rw-   0        0        0    12426 2023-05-13 05:30:29.000000 irails-1.3.7/irails/base_controller.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.069863 irails-1.3.7/irails/casbin_adapters/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.070859 irails-1.3.7/irails/casbin_adapters/__pycache__/
+-rw-rw-rw-   0        0        0    17834 2023-04-30 14:29:09.000000 irails-1.3.7/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc
+-rw-rw-rw-   0        0        0    10589 2023-05-13 05:03:07.000000 irails-1.3.7/irails/casbin_adapters/sqlalchemy_adapter.py
+-rw-rw-rw-   0        0        0     4381 2023-02-25 09:43:32.000000 irails-1.3.7/irails/cbv.py
+-rw-rw-rw-   0        0        0     6065 2023-05-11 15:19:41.000000 irails-1.3.7/irails/config.py
+-rw-rw-rw-   0        0        0    12478 2023-05-12 05:56:24.000000 irails-1.3.7/irails/controller_utils.py
+-rw-rw-rw-   0        0        0    32319 2023-05-12 06:03:46.000000 irails-1.3.7/irails/core.py
+-rw-rw-rw-   0        0        0     6409 2023-05-11 15:21:34.000000 irails-1.3.7/irails/database.py
+-rw-rw-rw-   0        0        0     1459 2023-05-11 15:27:11.000000 irails-1.3.7/irails/log.py
+-rw-rw-rw-   0        0        0     8673 2023-05-11 15:20:30.000000 irails-1.3.7/irails/midware.py
+-rw-rw-rw-   0        0        0     2141 2023-04-03 14:30:15.000000 irails-1.3.7/irails/midware_casbin.py
+-rw-rw-rw-   0        0        0     9341 2023-05-11 15:20:39.000000 irails-1.3.7/irails/midware_session.py
+-rw-rw-rw-   0        0        0     4200 2023-04-27 11:53:07.000000 irails-1.3.7/irails/mvc_router.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.080806 irails-1.3.7/irails/scripts/
+-rw-rw-rw-   0        0        0        0 2023-04-26 07:44:41.000000 irails-1.3.7/irails/scripts/__init__.py
+-rw-rw-rw-   0        0        0     7811 2023-05-11 15:34:41.000000 irails-1.3.7/irails/scripts/_app.py
+-rw-rw-rw-   0        0        0     7690 2023-05-09 06:52:08.000000 irails-1.3.7/irails/scripts/_controller.py
+-rw-rw-rw-   0        0        0     7755 2023-05-13 05:57:18.000000 irails-1.3.7/irails/scripts/_i18n.py
+-rw-rw-rw-   0        0        0     2301 2023-05-03 14:35:33.000000 irails-1.3.7/irails/scripts/_project.py
+-rw-rw-rw-   0        0        0     1600 2023-05-11 15:45:21.000000 irails-1.3.7/irails/scripts/_run.py
+-rw-rw-rw-   0        0        0     2288 2023-05-11 14:15:32.000000 irails-1.3.7/irails/scripts/_shell.py
+-rw-rw-rw-   0        0        0     1855 2023-05-11 12:33:17.000000 irails-1.3.7/irails/scripts/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.030050 irails-1.3.7/irails/scripts/tpls/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.089781 irails-1.3.7/irails/scripts/tpls/app/
+-rw-rw-rw-   0        0        0      223 2023-05-09 15:18:47.000000 irails-1.3.7/irails/scripts/tpls/app/controller.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-28 06:03:05.000000 irails-1.3.7/irails/scripts/tpls/app/css.tpl
+-rw-rw-rw-   0        0        0      791 2023-04-25 10:42:10.000000 irails-1.3.7/irails/scripts/tpls/app/home.css.tpl
+-rw-rw-rw-   0        0        0     1293 2023-05-05 10:16:42.000000 irails-1.3.7/irails/scripts/tpls/app/home.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 11:52:26.000000 irails-1.3.7/irails/scripts/tpls/app/model.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 11:52:38.000000 irails-1.3.7/irails/scripts/tpls/app/service.tpl
+-rw-rw-rw-   0        0        0        0 2023-04-25 12:03:35.000000 irails-1.3.7/irails/scripts/tpls/app/test.tpl
+-rw-rw-rw-   0        0        0       18 2023-05-02 08:56:04.000000 irails-1.3.7/irails/scripts/tpls/app/view.tpl
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.093772 irails-1.3.7/irails/scripts/tpls/project/
+-rw-rw-rw-   0        0        0      139 2023-04-23 09:46:24.000000 irails-1.3.7/irails/scripts/tpls/project/.gitignore
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.094769 irails-1.3.7/irails/scripts/tpls/project/apps/
+-rw-rw-rw-   0        0        0        0 2023-04-26 09:58:51.000000 irails-1.3.7/irails/scripts/tpls/project/apps/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.104742 irails-1.3.7/irails/scripts/tpls/project/configs/
+-rw-rw-rw-   0        0        0      746 2023-05-09 06:45:34.000000 irails-1.3.7/irails/scripts/tpls/project/configs/alembic.ini
+-rw-rw-rw-   0        0        0      198 2023-05-09 06:44:21.000000 irails-1.3.7/irails/scripts/tpls/project/configs/authencation.yaml
+-rw-rw-rw-   0        0        0        0 2023-03-06 08:27:07.000000 irails-1.3.7/irails/scripts/tpls/project/configs/cache.yaml
+-rw-rw-rw-   0        0        0      104 2023-05-04 05:06:32.000000 irails-1.3.7/irails/scripts/tpls/project/configs/casbin-adapter.csv
+-rw-rw-rw-   0        0        0      302 2023-05-04 05:24:51.000000 irails-1.3.7/irails/scripts/tpls/project/configs/casbin-model.conf
+-rw-rw-rw-   0        0        0      817 2023-05-10 10:45:36.000000 irails-1.3.7/irails/scripts/tpls/project/configs/database.yaml
+-rw-rw-rw-   0        0        0      748 2023-05-11 05:35:06.000000 irails-1.3.7/irails/scripts/tpls/project/configs/general.yaml
+-rw-rw-rw-   0        0        0      337 2023-04-22 10:54:12.000000 irails-1.3.7/irails/scripts/tpls/project/configs/session.yaml
+-rw-rw-rw-   0        0        0      272 2023-05-09 06:44:59.000000 irails-1.3.7/irails/scripts/tpls/project/configs/upload.yaml
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.033045 irails-1.3.7/irails/scripts/tpls/project/data/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.110726 irails-1.3.7/irails/scripts/tpls/project/data/alembic/
+-rw-rw-rw-   0        0        0       38 2023-04-09 12:01:20.000000 irails-1.3.7/irails/scripts/tpls/project/data/alembic/README
+-rw-rw-rw-   0        0        0     2144 2023-04-30 09:03:04.000000 irails-1.3.7/irails/scripts/tpls/project/data/alembic/env.py
+-rw-rw-rw-   0        0        0      510 2023-04-09 12:01:20.000000 irails-1.3.7/irails/scripts/tpls/project/data/alembic/script.py.mako
+-rw-rw-rw-   0        0        0      231 2023-05-11 15:42:13.000000 irails-1.3.7/irails/scripts/tpls/project/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.113736 irails-1.3.7/irails/scripts/tpls/project/public/
+-rw-rw-rw-   0        0        0     1233 2023-05-02 08:46:22.000000 irails-1.3.7/irails/scripts/tpls/project/public/error_404.html
+-rw-rw-rw-   0        0        0     1083 2023-05-02 08:46:46.000000 irails-1.3.7/irails/scripts/tpls/project/public/error_500.html
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.116709 irails-1.3.7/irails/scripts/tpls/project/public/libs/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.036038 irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.119512 irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/
+-rw-rw-rw-   0        0        0  1970121 2023-04-23 08:02:36.000000 irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.123505 irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/
+-rw-rw-rw-   0        0        0   323666 2023-04-23 08:04:13.000000 irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css
+-rw-rw-rw-   0        0        0      725 2023-04-21 12:39:53.000000 irails-1.3.7/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js
+-rw-rw-rw-   0        0        0  1441055 2023-04-21 07:36:37.000000 irails-1.3.7/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.037035 irails-1.3.7/irails/scripts/tpls/project/public/vue@3.2.36/
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.126500 irails-1.3.7/irails/scripts/tpls/project/public/vue@3.2.36/dist/
+-rw-rw-rw-   0        0        0   640610 2023-04-21 07:36:07.000000 irails-1.3.7/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js
+-rw-rw-rw-   0        0        0     2887 2023-05-12 05:35:40.000000 irails-1.3.7/irails/view.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:16:05.067868 irails-1.3.7/irails.egg-info/
+-rw-rw-rw-   0        0        0     5315 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2326 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      777 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 06:16:04.000000 irails-1.3.7/irails.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 06:16:05.129498 irails-1.3.7/setup.cfg
+-rw-rw-rw-   0        0        0     2551 2023-05-09 11:27:27.000000 irails-1.3.7/setup.py
```

### Comparing `irails-1.3.6/PKG-INFO` & `irails-1.3.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: irails
-Version: 1.3.6
+Version: 1.3.7
 Summary: Simple and elegant use of FastApi in MVC mode
 Home-page: https://github.com/smjkzsl/irails
 Author: Bruce chou
 Author-email: smjkzsl@gmail.com
 License: Apache License 2.0
 Keywords: web framework,mvc framework,fastapi framework
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `irails-1.3.6/README.md` & `irails-1.3.7/README.md`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/_i18n.py` & `irails-1.3.7/irails/_i18n.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/_loader.py` & `irails-1.3.7/irails/_loader.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/_utils.py` & `irails-1.3.7/irails/_utils.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/auth.py` & `irails-1.3.7/irails/auth.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/base_controller.py` & `irails-1.3.7/irails/base_controller.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc` & `irails-1.3.7/irails/casbin_adapters/__pycache__/sqlalchemy_adapter.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/casbin_adapters/sqlalchemy_adapter.py` & `irails-1.3.7/irails/casbin_adapters/sqlalchemy_adapter.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/cbv.py` & `irails-1.3.7/irails/cbv.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/config.py` & `irails-1.3.7/irails/config.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/controller_utils.py` & `irails-1.3.7/irails/controller_utils.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/core.py` & `irails-1.3.7/irails/core.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/database.py` & `irails-1.3.7/irails/database.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/log.py` & `irails-1.3.7/irails/log.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/midware.py` & `irails-1.3.7/irails/midware.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/midware_casbin.py` & `irails-1.3.7/irails/midware_casbin.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/midware_session.py` & `irails-1.3.7/irails/midware_session.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/mvc_router.py` & `irails-1.3.7/irails/mvc_router.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_app.py` & `irails-1.3.7/irails/scripts/_app.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_controller.py` & `irails-1.3.7/irails/scripts/_controller.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_i18n.py` & `irails-1.3.7/irails/scripts/_i18n.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_project.py` & `irails-1.3.7/irails/scripts/_project.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_run.py` & `irails-1.3.7/irails/scripts/_run.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/_shell.py` & `irails-1.3.7/irails/scripts/_shell.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/main.py` & `irails-1.3.7/irails/scripts/main.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/app/home.css.tpl` & `irails-1.3.7/irails/scripts/tpls/app/home.css.tpl`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/app/home.tpl` & `irails-1.3.7/irails/scripts/tpls/app/home.tpl`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/configs/alembic.ini` & `irails-1.3.7/irails/scripts/tpls/project/configs/alembic.ini`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/configs/database.yaml` & `irails-1.3.7/irails/scripts/tpls/project/configs/database.yaml`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/configs/general.yaml` & `irails-1.3.7/irails/scripts/tpls/project/configs/general.yaml`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/data/alembic/env.py` & `irails-1.3.7/irails/scripts/tpls/project/data/alembic/env.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/error_404.html` & `irails-1.3.7/irails/scripts/tpls/project/public/error_404.html`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/error_500.html` & `irails-1.3.7/irails/scripts/tpls/project/public/error_500.html`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js` & `irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/dist/index.full.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css` & `irails-1.3.7/irails/scripts/tpls/project/public/libs/element-plus@2.3.3/theme-chalk/index.css`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js` & `irails-1.3.7/irails/scripts/tpls/project/public/libs/vue3-sfc-loader-config.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js` & `irails-1.3.7/irails/scripts/tpls/project/public/libs/vue3-sfc-loader.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js` & `irails-1.3.7/irails/scripts/tpls/project/public/vue@3.2.36/dist/vue.global.js`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails/view.py` & `irails-1.3.7/irails/view.py`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails.egg-info/PKG-INFO` & `irails-1.3.7/irails.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: irails
-Version: 1.3.6
+Version: 1.3.7
 Summary: Simple and elegant use of FastApi in MVC mode
 Home-page: https://github.com/smjkzsl/irails
 Author: Bruce chou
 Author-email: smjkzsl@gmail.com
 License: Apache License 2.0
 Keywords: web framework,mvc framework,fastapi framework
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `irails-1.3.6/irails.egg-info/SOURCES.txt` & `irails-1.3.7/irails.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `irails-1.3.6/irails.egg-info/requires.txt` & `irails-1.3.7/irails.egg-info/requires.txt`

 * *Files 2% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 simpleeval==0.9.13
 sniffio==1.3.0
 SQLAlchemy==2.0.9
 starlette==0.26.1
 typing-extensions==4.5.0
 typing-inspect==0.8.0
 ujson==5.5.0
-urllib3==2.0.2
+urllib3==1.26
 uvicorn==0.21.1
 watchfiles==0.19.0
 websockets==11.0.2
 yarg==0.1.9
 chardet==5.1.0
 polib==1.2.0
 httpx==0.24.0
```

### Comparing `irails-1.3.6/setup.py` & `irails-1.3.7/setup.py`

 * *Files identical despite different names*

