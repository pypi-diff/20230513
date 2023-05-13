# Comparing `tmp/EllipSect-3.0.1.tar.gz` & `tmp/EllipSect-3.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "EllipSect-3.0.1.tar", last modified: Tue Feb 14 00:46:54 2023, max compression
+gzip compressed data, was "EllipSect-3.2.1.tar", last modified: Sat May 13 17:31:03 2023, max compression
```

## Comparing `EllipSect-3.0.1.tar` & `EllipSect-3.2.1.tar`

### file list

```diff
@@ -1,88 +1,88 @@
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.194035 EllipSect-3.0.1/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      206 2022-05-19 20:23:00.000000 EllipSect-3.0.1/AUTHORS.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     1126 2022-08-31 20:39:25.000000 EllipSect-3.0.1/CHANGELOG.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    13841 2022-05-19 05:38:00.000000 EllipSect-3.0.1/CONTRIBUTING.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    35147 2020-07-24 13:17:31.000000 EllipSect-3.0.1/LICENSE.txt
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     6824 2023-02-14 00:46:54.194035 EllipSect-3.0.1/PKG-INFO
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     5879 2022-10-08 05:34:24.000000 EllipSect-3.0.1/README.rst
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.150035 EllipSect-3.0.1/docs/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     1154 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/Makefile
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.150035 EllipSect-3.0.1/docs/_static/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       18 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/_static/.gitignore
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     7461 2022-06-03 20:18:01.000000 EllipSect-3.0.1/docs/api.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       41 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/authors.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       43 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/changelog.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     9758 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/conf.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       33 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/contributing.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    17760 2022-09-07 23:14:29.000000 EllipSect-3.0.1/docs/howto.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     2321 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/index.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       67 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/license.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       39 2022-05-19 05:38:00.000000 EllipSect-3.0.1/docs/readme.rst
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      307 2022-05-27 21:03:59.000000 EllipSect-3.0.1/docs/requirements.txt
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.154035 EllipSect-3.0.1/example/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      341 2020-09-18 22:51:02.000000 EllipSect-3.0.1/example/README
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    69120 2020-08-14 03:16:26.000000 EllipSect-3.0.1/example/gal.fits
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     2646 2020-08-14 03:16:26.000000 EllipSect-3.0.1/example/galfit.feedme
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    25920 2020-08-14 03:16:26.000000 EllipSect-3.0.1/example/psf.fits
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.178035 EllipSect-3.0.1/img/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   251092 2021-05-21 15:14:44.000000 EllipSect-3.0.1/img/A2029.ring.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   149798 2021-10-21 21:59:56.000000 EllipSect-3.0.1/img/A85.comp.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   573061 2022-03-30 17:48:47.000000 EllipSect-3.0.1/img/A85.con-cub.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   670362 2022-03-30 17:49:48.000000 EllipSect-3.0.1/img/A85.cub.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    98164 2021-10-21 22:00:51.000000 EllipSect-3.0.1/img/A85.def.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   610346 2022-03-30 17:44:31.000000 EllipSect-3.0.1/img/A85.ell-cub.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   503397 2021-10-21 22:01:09.000000 EllipSect-3.0.1/img/A85.grid.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    95479 2021-10-21 22:01:39.000000 EllipSect-3.0.1/img/A85.log.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   102981 2021-10-21 22:02:04.000000 EllipSect-3.0.1/img/A85.pix.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   327227 2020-08-14 03:16:26.000000 EllipSect-3.0.1/img/A85.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    95328 2021-10-21 22:02:35.000000 EllipSect-3.0.1/img/A85.ranx1.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    89311 2021-10-21 22:03:30.000000 EllipSect-3.0.1/img/A85.ranx2.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    91257 2021-10-21 22:04:08.000000 EllipSect-3.0.1/img/A85.rany1.png
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      355 2022-05-19 05:38:00.000000 EllipSect-3.0.1/pyproject.toml
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     1760 2023-02-14 00:46:54.194035 EllipSect-3.0.1/setup.cfg
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      706 2022-05-19 05:38:00.000000 EllipSect-3.0.1/setup.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.142035 EllipSect-3.0.1/src/
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.178035 EllipSect-3.0.1/src/EllipSect.egg-info/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     6824 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/PKG-INFO
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     1610 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/SOURCES.txt
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        1 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/dependency_links.txt
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       57 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/entry_points.txt
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        1 2022-05-23 00:05:26.000000 EllipSect-3.0.1/src/EllipSect.egg-info/not-zip-safe
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      146 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/requires.txt
--rw-rw-r--   0 canorve   (1000) canorve   (1000)       10 2023-02-14 00:46:54.000000 EllipSect-3.0.1/src/EllipSect.egg-info/top_level.txt
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.178035 EllipSect-3.0.1/src/ellipsect/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      675 2022-05-29 17:51:45.000000 EllipSect-3.0.1/src/ellipsect/__init__.py
--rwxrwxr-x   0 canorve   (1000) canorve   (1000)     2080 2023-02-08 06:36:48.000000 EllipSect-3.0.1/src/ellipsect/ellipsectors.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.182035 EllipSect-3.0.1/src/ellipsect/inout/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:15:19.000000 EllipSect-3.0.1/src/ellipsect/inout/__init__.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    22279 2023-02-11 06:26:57.000000 EllipSect-3.0.1/src/ellipsect/inout/galfit.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     3380 2023-02-10 20:37:56.000000 EllipSect-3.0.1/src/ellipsect/inout/gfits.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    22020 2023-02-09 22:58:33.000000 EllipSect-3.0.1/src/ellipsect/inout/plots.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    20006 2023-02-11 06:45:03.000000 EllipSect-3.0.1/src/ellipsect/inout/prt.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    18581 2023-02-09 22:58:43.000000 EllipSect-3.0.1/src/ellipsect/inout/read.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.182035 EllipSect-3.0.1/src/ellipsect/lib/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 06:03:15.000000 EllipSect-3.0.1/src/ellipsect/lib/__init__.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     7937 2023-02-09 22:59:23.000000 EllipSect-3.0.1/src/ellipsect/lib/clas.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     1476 2023-02-09 22:59:28.000000 EllipSect-3.0.1/src/ellipsect/lib/libs.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.186035 EllipSect-3.0.1/src/ellipsect/phot/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:10:40.000000 EllipSect-3.0.1/src/ellipsect/phot/__init__.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     5474 2023-02-09 23:00:09.000000 EllipSect-3.0.1/src/ellipsect/phot/ned.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    15210 2023-02-11 06:28:51.000000 EllipSect-3.0.1/src/ellipsect/phot/phot.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    12271 2023-02-09 23:00:17.000000 EllipSect-3.0.1/src/ellipsect/phot/tidal.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.186035 EllipSect-3.0.1/src/ellipsect/sectors/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:15:40.000000 EllipSect-3.0.1/src/ellipsect/sectors/__init__.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     3065 2023-02-09 23:00:21.000000 EllipSect-3.0.1/src/ellipsect/sectors/comp.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     6814 2023-02-09 23:00:25.000000 EllipSect-3.0.1/src/ellipsect/sectors/ellip.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     2981 2023-02-09 23:00:28.000000 EllipSect-3.0.1/src/ellipsect/sectors/num.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    19198 2023-02-10 20:41:43.000000 EllipSect-3.0.1/src/ellipsect/sectors/sect.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.190035 EllipSect-3.0.1/src/ellipsect/sky/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 07:02:06.000000 EllipSect-3.0.1/src/ellipsect/sky/__init__.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    24185 2023-02-09 23:00:47.000000 EllipSect-3.0.1/src/ellipsect/sky/sky.py
-drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-02-14 00:46:54.194035 EllipSect-3.0.1/tests/
--rw-rw-r--   0 canorve   (1000) canorve   (1000)      277 2022-05-19 05:38:00.000000 EllipSect-3.0.1/tests/conftest.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    69120 2020-08-14 03:16:26.000000 EllipSect-3.0.1/tests/gal.fits
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     2879 2022-05-27 20:24:55.000000 EllipSect-3.0.1/tests/galfit.01
--rw-rw-r--   0 canorve   (1000) canorve   (1000)   192960 2023-02-11 06:53:51.000000 EllipSect-3.0.1/tests/imgblock.fits
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    25920 2020-08-14 03:16:26.000000 EllipSect-3.0.1/tests/psf.fits
--rw-rw-r--   0 canorve   (1000) canorve   (1000)    14696 2023-02-11 06:55:47.000000 EllipSect-3.0.1/tests/test_ellipsect.py
--rw-rw-r--   0 canorve   (1000) canorve   (1000)     2575 2022-05-19 05:38:00.000000 EllipSect-3.0.1/tox.ini
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.695956 EllipSect-3.2.1/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      206 2022-05-19 20:23:00.000000 EllipSect-3.2.1/AUTHORS.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     1126 2022-08-31 20:39:25.000000 EllipSect-3.2.1/CHANGELOG.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    13841 2022-05-19 05:38:00.000000 EllipSect-3.2.1/CONTRIBUTING.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    35147 2020-07-24 13:17:31.000000 EllipSect-3.2.1/LICENSE.txt
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     6819 2023-05-13 17:31:03.695956 EllipSect-3.2.1/PKG-INFO
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     5874 2023-03-17 05:15:08.000000 EllipSect-3.2.1/README.rst
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.667955 EllipSect-3.2.1/docs/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     1154 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/Makefile
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.667955 EllipSect-3.2.1/docs/_static/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       18 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/_static/.gitignore
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     7461 2022-06-03 20:18:01.000000 EllipSect-3.2.1/docs/api.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       41 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/authors.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       43 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/changelog.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     9758 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/conf.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       33 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/contributing.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    17760 2022-09-07 23:14:29.000000 EllipSect-3.2.1/docs/howto.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     2321 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/index.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       67 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/license.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       39 2022-05-19 05:38:00.000000 EllipSect-3.2.1/docs/readme.rst
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      307 2022-05-27 21:03:59.000000 EllipSect-3.2.1/docs/requirements.txt
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.671955 EllipSect-3.2.1/example/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      341 2020-09-18 22:51:02.000000 EllipSect-3.2.1/example/README
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    69120 2020-08-14 03:16:26.000000 EllipSect-3.2.1/example/gal.fits
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     2646 2020-08-14 03:16:26.000000 EllipSect-3.2.1/example/galfit.feedme
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    25920 2020-08-14 03:16:26.000000 EllipSect-3.2.1/example/psf.fits
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.679956 EllipSect-3.2.1/img/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   251092 2021-05-21 15:14:44.000000 EllipSect-3.2.1/img/A2029.ring.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   149798 2021-10-21 21:59:56.000000 EllipSect-3.2.1/img/A85.comp.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   573061 2022-03-30 17:48:47.000000 EllipSect-3.2.1/img/A85.con-cub.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   670362 2022-03-30 17:49:48.000000 EllipSect-3.2.1/img/A85.cub.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    98164 2021-10-21 22:00:51.000000 EllipSect-3.2.1/img/A85.def.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   610346 2022-03-30 17:44:31.000000 EllipSect-3.2.1/img/A85.ell-cub.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   503397 2021-10-21 22:01:09.000000 EllipSect-3.2.1/img/A85.grid.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    95479 2021-10-21 22:01:39.000000 EllipSect-3.2.1/img/A85.log.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   102981 2021-10-21 22:02:04.000000 EllipSect-3.2.1/img/A85.pix.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   327227 2020-08-14 03:16:26.000000 EllipSect-3.2.1/img/A85.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    95328 2021-10-21 22:02:35.000000 EllipSect-3.2.1/img/A85.ranx1.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    89311 2021-10-21 22:03:30.000000 EllipSect-3.2.1/img/A85.ranx2.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    91257 2021-10-21 22:04:08.000000 EllipSect-3.2.1/img/A85.rany1.png
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      355 2022-05-19 05:38:00.000000 EllipSect-3.2.1/pyproject.toml
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     1760 2023-05-13 17:31:03.699956 EllipSect-3.2.1/setup.cfg
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      706 2022-05-19 05:38:00.000000 EllipSect-3.2.1/setup.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.659955 EllipSect-3.2.1/src/
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.683956 EllipSect-3.2.1/src/EllipSect.egg-info/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     6819 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/PKG-INFO
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     1610 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/SOURCES.txt
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        1 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/dependency_links.txt
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       57 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/entry_points.txt
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        1 2022-05-23 00:05:26.000000 EllipSect-3.2.1/src/EllipSect.egg-info/not-zip-safe
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      146 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/requires.txt
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)       10 2023-05-13 17:31:03.000000 EllipSect-3.2.1/src/EllipSect.egg-info/top_level.txt
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.683956 EllipSect-3.2.1/src/ellipsect/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      675 2022-05-29 17:51:45.000000 EllipSect-3.2.1/src/ellipsect/__init__.py
+-rwxrwxr-x   0 canorve   (1000) canorve   (1000)     2080 2023-02-08 06:36:48.000000 EllipSect-3.2.1/src/ellipsect/ellipsectors.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.683956 EllipSect-3.2.1/src/ellipsect/inout/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:15:19.000000 EllipSect-3.2.1/src/ellipsect/inout/__init__.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    22988 2023-03-14 00:31:50.000000 EllipSect-3.2.1/src/ellipsect/inout/galfit.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     3380 2023-02-10 20:37:56.000000 EllipSect-3.2.1/src/ellipsect/inout/gfits.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    23201 2023-04-12 22:14:55.000000 EllipSect-3.2.1/src/ellipsect/inout/plots.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    20007 2023-04-19 15:30:49.000000 EllipSect-3.2.1/src/ellipsect/inout/prt.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    20009 2023-05-12 21:16:51.000000 EllipSect-3.2.1/src/ellipsect/inout/read.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.687956 EllipSect-3.2.1/src/ellipsect/lib/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 06:03:15.000000 EllipSect-3.2.1/src/ellipsect/lib/__init__.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     7905 2023-02-19 04:21:12.000000 EllipSect-3.2.1/src/ellipsect/lib/clas.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     1506 2023-03-14 03:32:46.000000 EllipSect-3.2.1/src/ellipsect/lib/libs.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.691956 EllipSect-3.2.1/src/ellipsect/phot/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:10:40.000000 EllipSect-3.2.1/src/ellipsect/phot/__init__.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     5474 2023-02-09 23:00:09.000000 EllipSect-3.2.1/src/ellipsect/phot/ned.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    15252 2023-03-14 00:35:39.000000 EllipSect-3.2.1/src/ellipsect/phot/phot.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    12271 2023-05-11 07:29:38.000000 EllipSect-3.2.1/src/ellipsect/phot/tidal.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.691956 EllipSect-3.2.1/src/ellipsect/sectors/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 02:15:40.000000 EllipSect-3.2.1/src/ellipsect/sectors/__init__.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     3065 2023-02-09 23:00:21.000000 EllipSect-3.2.1/src/ellipsect/sectors/comp.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     6814 2023-02-09 23:00:25.000000 EllipSect-3.2.1/src/ellipsect/sectors/ellip.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     2981 2023-02-09 23:00:28.000000 EllipSect-3.2.1/src/ellipsect/sectors/num.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    19192 2023-05-12 00:52:31.000000 EllipSect-3.2.1/src/ellipsect/sectors/sect.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.695956 EllipSect-3.2.1/src/ellipsect/sky/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)        0 2021-08-21 07:02:06.000000 EllipSect-3.2.1/src/ellipsect/sky/__init__.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    24185 2023-02-09 23:00:47.000000 EllipSect-3.2.1/src/ellipsect/sky/sky.py
+drwxrwxr-x   0 canorve   (1000) canorve   (1000)        0 2023-05-13 17:31:03.695956 EllipSect-3.2.1/tests/
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)      277 2022-05-19 05:38:00.000000 EllipSect-3.2.1/tests/conftest.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    69120 2020-08-14 03:16:26.000000 EllipSect-3.2.1/tests/gal.fits
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     2879 2022-05-27 20:24:55.000000 EllipSect-3.2.1/tests/galfit.01
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)   192960 2023-05-13 17:24:35.000000 EllipSect-3.2.1/tests/imgblock.fits
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    25920 2020-08-14 03:16:26.000000 EllipSect-3.2.1/tests/psf.fits
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)    14837 2023-05-13 17:24:07.000000 EllipSect-3.2.1/tests/test_ellipsect.py
+-rw-rw-r--   0 canorve   (1000) canorve   (1000)     2575 2022-05-19 05:38:00.000000 EllipSect-3.2.1/tox.ini
```

### Comparing `EllipSect-3.0.1/CHANGELOG.rst` & `EllipSect-3.2.1/CHANGELOG.rst`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/CONTRIBUTING.rst` & `EllipSect-3.2.1/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/LICENSE.txt` & `EllipSect-3.2.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/PKG-INFO` & `EllipSect-3.2.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: EllipSect
-Version: 3.0.1
+Version: 3.2.1
 Summary: A surface brightness analysis tool for GALFIT output.
 Home-page: https://github.com/canorve/EllipSect
 Author: Christopher Añorve
 Author-email: canorve@gmail.com
 License: GNU General Public License v3 (GPLv3)
 Project-URL: Documentation, https://github.com/canorve/EllipSect/blob/master/README.rst
 Project-URL: Source, https://github.com/canorve/EllipSect
@@ -32,21 +32,21 @@
 =============
 
 |DOI|
 
 EllipSect creates surface brightness profiles and extracts other
 photometric data from the GALFIT output peng et al. (2002).
 
-This code is “similar” (but not sustitute) to IRAF’s ellipse routine. It
+This code is “similar” (but not substitute) to IRAF’s ellipse routine. It
 creates a Surface brightness profile for the galaxy, model and
-(optionally) individual model components.
+, optionally, individual model components.
 
 In addition, *EllipSect* computes variables such as Absolute Magnitude,
 luminosity, Flux, total apparent magnitude, Bulge to Total Ratio, Tidal,
-Chinu in the sectors ellipse, Bumpiness, Signal to Noise Ratio, Akaike
+Chinu within a radius containing 90% of total light, Bumpiness, Signal to Noise Ratio, Akaike
 Information criterion, Bayesian information criterion, mean surface
 brightness at effective radius, percentage of total light per component,
 radius at 90% of light (for Sersic components only), effective radius in
 kpc, etc.
 
 --------------
 
@@ -88,21 +88,16 @@
 
 
 
 Run the automated tests:
 
 ::
 
-   python -m pytest 
+    tox 
 
-or
-
-::
-
-   pytest
 
 **Note**: *EllipSect* needs the GALFIT output files (GALFIT.XX) to work.
 Although *GALFIT* is not stricly required, it will required it to create
 the model components and sigma image. Make sure you can call GALFIT from
 the command line. Otherwise the automated tests will fail.
 
 --------------
```

### Comparing `EllipSect-3.0.1/README.rst` & `EllipSect-3.2.1/README.rst`

 * *Files 6% similar despite different names*

```diff
@@ -8,21 +8,21 @@
 =============
 
 |DOI|
 
 EllipSect creates surface brightness profiles and extracts other
 photometric data from the GALFIT output peng et al. (2002).
 
-This code is “similar” (but not sustitute) to IRAF’s ellipse routine. It
+This code is “similar” (but not substitute) to IRAF’s ellipse routine. It
 creates a Surface brightness profile for the galaxy, model and
-(optionally) individual model components.
+, optionally, individual model components.
 
 In addition, *EllipSect* computes variables such as Absolute Magnitude,
 luminosity, Flux, total apparent magnitude, Bulge to Total Ratio, Tidal,
-Chinu in the sectors ellipse, Bumpiness, Signal to Noise Ratio, Akaike
+Chinu within a radius containing 90% of total light, Bumpiness, Signal to Noise Ratio, Akaike
 Information criterion, Bayesian information criterion, mean surface
 brightness at effective radius, percentage of total light per component,
 radius at 90% of light (for Sersic components only), effective radius in
 kpc, etc.
 
 --------------
 
@@ -64,21 +64,16 @@
 
 
 
 Run the automated tests:
 
 ::
 
-   python -m pytest 
+    tox 
 
-or
-
-::
-
-   pytest
 
 **Note**: *EllipSect* needs the GALFIT output files (GALFIT.XX) to work.
 Although *GALFIT* is not stricly required, it will required it to create
 the model components and sigma image. Make sure you can call GALFIT from
 the command line. Otherwise the automated tests will fail.
 
 --------------
```

### Comparing `EllipSect-3.0.1/docs/Makefile` & `EllipSect-3.2.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/docs/api.rst` & `EllipSect-3.2.1/docs/api.rst`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/docs/conf.py` & `EllipSect-3.2.1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/docs/howto.rst` & `EllipSect-3.2.1/docs/howto.rst`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/docs/index.rst` & `EllipSect-3.2.1/docs/index.rst`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/example/gal.fits` & `EllipSect-3.2.1/example/gal.fits`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/example/galfit.feedme` & `EllipSect-3.2.1/example/galfit.feedme`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/example/psf.fits` & `EllipSect-3.2.1/example/psf.fits`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A2029.ring.png` & `EllipSect-3.2.1/img/A2029.ring.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.comp.png` & `EllipSect-3.2.1/img/A85.comp.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.con-cub.png` & `EllipSect-3.2.1/img/A85.con-cub.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.cub.png` & `EllipSect-3.2.1/img/A85.cub.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.def.png` & `EllipSect-3.2.1/img/A85.def.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.ell-cub.png` & `EllipSect-3.2.1/img/A85.ell-cub.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.grid.png` & `EllipSect-3.2.1/img/A85.grid.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.log.png` & `EllipSect-3.2.1/img/A85.log.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.pix.png` & `EllipSect-3.2.1/img/A85.pix.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.png` & `EllipSect-3.2.1/img/A85.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.ranx1.png` & `EllipSect-3.2.1/img/A85.ranx1.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.ranx2.png` & `EllipSect-3.2.1/img/A85.ranx2.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/img/A85.rany1.png` & `EllipSect-3.2.1/img/A85.rany1.png`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/setup.cfg` & `EllipSect-3.2.1/setup.cfg`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/setup.py` & `EllipSect-3.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/EllipSect.egg-info/PKG-INFO` & `EllipSect-3.2.1/src/EllipSect.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: EllipSect
-Version: 3.0.1
+Version: 3.2.1
 Summary: A surface brightness analysis tool for GALFIT output.
 Home-page: https://github.com/canorve/EllipSect
 Author: Christopher Añorve
 Author-email: canorve@gmail.com
 License: GNU General Public License v3 (GPLv3)
 Project-URL: Documentation, https://github.com/canorve/EllipSect/blob/master/README.rst
 Project-URL: Source, https://github.com/canorve/EllipSect
@@ -32,21 +32,21 @@
 =============
 
 |DOI|
 
 EllipSect creates surface brightness profiles and extracts other
 photometric data from the GALFIT output peng et al. (2002).
 
-This code is “similar” (but not sustitute) to IRAF’s ellipse routine. It
+This code is “similar” (but not substitute) to IRAF’s ellipse routine. It
 creates a Surface brightness profile for the galaxy, model and
-(optionally) individual model components.
+, optionally, individual model components.
 
 In addition, *EllipSect* computes variables such as Absolute Magnitude,
 luminosity, Flux, total apparent magnitude, Bulge to Total Ratio, Tidal,
-Chinu in the sectors ellipse, Bumpiness, Signal to Noise Ratio, Akaike
+Chinu within a radius containing 90% of total light, Bumpiness, Signal to Noise Ratio, Akaike
 Information criterion, Bayesian information criterion, mean surface
 brightness at effective radius, percentage of total light per component,
 radius at 90% of light (for Sersic components only), effective radius in
 kpc, etc.
 
 --------------
 
@@ -88,21 +88,16 @@
 
 
 
 Run the automated tests:
 
 ::
 
-   python -m pytest 
+    tox 
 
-or
-
-::
-
-   pytest
 
 **Note**: *EllipSect* needs the GALFIT output files (GALFIT.XX) to work.
 Although *GALFIT* is not stricly required, it will required it to create
 the model components and sigma image. Make sure you can call GALFIT from
 the command line. Otherwise the automated tests will fail.
 
 --------------
```

### Comparing `EllipSect-3.0.1/src/EllipSect.egg-info/SOURCES.txt` & `EllipSect-3.2.1/src/EllipSect.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/__init__.py` & `EllipSect-3.2.1/src/ellipsect/__init__.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/ellipsectors.py` & `EllipSect-3.2.1/src/ellipsect/ellipsectors.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/inout/galfit.py` & `EllipSect-3.2.1/src/ellipsect/inout/galfit.py`

 * *Files 9% similar despite different names*

```diff
@@ -650,108 +650,140 @@
 
     galcomps.Active[maskdist] = True
 
     return galcomps
 
 
 
-
 ### Sersic components 
 class GetReff:
     '''class to obtain the effective radius for the whole galaxy'''
 
-    def GetReSer(self, galhead: GalHead, galcomps: GalComps, eff: float) -> float:
+    def GetReSer(self, galhead: GalHead, comps: GalComps, eff: float, theta: float) -> float:
 
-        comps = self.conver2Sersic(galcomps)
 
         maskgal = (comps.Active == True) 
 
         comps.Flux = 10**((galhead.mgzpt - comps.Mag)/2.5)
 
-        
         totFlux = comps.Flux[maskgal].sum()
 
         totmag = -2.5*np.log10(totFlux) + galhead.mgzpt
 
         a = 0.1
         b = comps.Rad[maskgal][-1] * 1000  # hope it doesn't crash
-        
+
         Reff = self.solveSerRe(a, b, comps.Flux[maskgal], comps.Rad[maskgal], 
-                comps.Exp[maskgal], totFlux, eff)
+                comps.Exp[maskgal], comps.AxRat[maskgal], comps.PosAng[maskgal], totFlux, eff, theta)
 
 
         return Reff, totmag
 
 
-    def conver2Sersic(self, galcomps: GalComps) -> GalComps:
-        ''' function to convert exponential, gaussian params to Sersic params'''
-
-        comps =  copy.deepcopy(galcomps)
 
-        maskdev = (comps.Active == True) & (comps.NameComp == "devauc")
-        maskexp = (comps.Active == True) & (comps.NameComp == "expdisk")
-        maskgas = (comps.Active == True) & (comps.NameComp == "gaussian")
+    def solveSerRe(self, a: float, b: float, flux: list, rad: list, n: list, q: list, pa: list, totFlux: float, eff: float, theta: float) -> float:
+        "return the Re of a set of Sersic functions. It uses Bisection"
 
 
-        K_GAUSS = 0.6931471805599455 #constant k for gaussian
-        K_EXP = 1.6783469900166612 # constant k for expdisk
-        SQ2 = np.sqrt(2) 
+        Re = bisect(self.funReSer, a, b, args=(flux, rad, n, q, pa, totFlux, eff, theta))
 
-        #for gaussian functions
-        if maskgas.any():
-            comps.Exp[maskgas] = 0.5 
-            comps.Rad[maskgas] = comps.Rad[maskgas]/2.354 #converting to sigma 
-            comps.Rad[maskgas] = SQ2*(K_GAUSS**0.5)*comps.Rad[maskgas] #converting to Re 
+        return Re
 
 
-        #for de vaucouleurs
-        if maskdev.any():
-            comps.Exp[maskdev] = 4
+    def funReSer(self, R: float, flux: list, rad: list, n: list, q: list, pa: list, totFlux: float, eff: float, theta: float) -> float:
+        
 
-        #for exponential disks
-        if maskexp.any():
-            comps.Exp[maskexp] = 1
-            comps.Rad[maskexp] = K_EXP*comps.Rad[maskexp] #converting to Re
+        fun = self.Ftotser(R, flux, rad, n, q, pa, theta) - totFlux*eff
 
-        return comps
+        return fun
+     
+    def Ftotser(self, R: float, flux: list, rad: list, n: list, q: list, pa: list, theta: float) -> float:
 
+        ftotR = self.Fser(R, flux, rad, n, q, pa, theta) 
 
+        return ftotR.sum()
 
 
-    def solveSerRe(self, a: float, b: float, flux: list, rad: list, n: list, totFlux: float, eff: float) -> float:
-        "return the Re of a set of Sersic functions. It uses Bisection"
 
-        Re = bisect(self.funReSer, a, b, args=(flux, rad, n, totFlux, eff))
+    def Fser(self, R: float, Flux: list, Re: list, n: list, q: list, pa: list, theta: float) -> float:
+        '''sersic flux to a determined R'''
+        
+        k = gammaincinv(2*n, 0.5)
 
-        return Re
+        Rcor = GetRadAng(R, q, pa, theta) 
 
+        X = k*(Rcor/Re)**(1/n) 
 
-    def funReSer(self, R: float, flux: list, rad: list, n: list, totFlux: float, eff: float) -> float:
+        Fr = Flux*gammainc(2*n, X) ##esta funcion esta mal 
         
-        fun = self.Ftotser(R, flux, rad, n) - totFlux*eff
+        return Fr
 
-        return fun
 
 
-    def Ftotser(self, R: float, flux: list, rad: list, n: list) -> float:
+def conver2Sersic(galcomps: GalComps) -> GalComps:
+    ''' function to convert exponential, gaussian params to Sersic params'''
 
-        ftotR = self.Fser(R, flux, rad, n) 
+    comps =  copy.deepcopy(galcomps)
 
-        return ftotR.sum()
+    maskdev = comps.NameComp == "devauc"
+    maskexp = comps.NameComp == "expdisk"
+    maskgas = comps.NameComp == "gaussian"
 
 
-    def Fser(self, R: float, Flux: list, Re: list, n: list) -> float:
-        '''sersic flux to a determined R'''
-        
-        k = gammaincinv(2*n, 0.5)
+    K_GAUSS = 0.6931471805599455 #constant k for gaussian
+    K_EXP = 1.6783469900166612 # constant k for expdisk
+    SQ2 = np.sqrt(2) 
+
+    #for gaussian functions
+    if maskgas.any():
+        comps.Exp[maskgas] = 0.5 
+        comps.Rad[maskgas] = comps.Rad[maskgas]/2.354 #converting to sigma 
+        comps.Rad[maskgas] = SQ2*(K_GAUSS**0.5)*comps.Rad[maskgas] #converting to Re 
+
+
+    #for de vaucouleurs
+    if maskdev.any():
+        comps.Exp[maskdev] = 4
+
+    #for exponential disks
+    if maskexp.any():
+        comps.Exp[maskexp] = 1
+        comps.Rad[maskexp] = K_EXP*comps.Rad[maskexp] #converting to Re
+
+
+    return comps
+
+
+
+def GetRadAng(R: float, q: list, pa: list, theta: float) -> float:
+    '''Given an ellipse and an angle it returns the radius in angle direction. 
+    Theta are the values for the galaxy and the others for every component'''
+
+
+
+    #changing measured angle from y-axis to x-axis
+    # and changing to rads:
+    newpa = (pa + 90)*np.pi/180 #angle of every component
+    theta = (theta + 90)*np.pi/180 #angle of direction of R 
+
+    #bim = q * R
+
+    ecc = np.sqrt(1 - q**2)
+
+    alpha = theta - newpa #this is the direction 
+
+
+    bell =  R*np.sqrt(1 - (ecc*np.cos(alpha))**2)
+
+
+    aell = bell/q  #rad to evalue for every component
+
+
+
+    return aell 
 
-        X = k*(R/Re)**(1/n) 
 
-        Fr = Flux*gammainc(2*n, X) ##esta funcion esta mal 
-        
-        return Fr
 
-
```

### Comparing `EllipSect-3.0.1/src/ellipsect/inout/gfits.py` & `EllipSect-3.2.1/src/ellipsect/inout/gfits.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/inout/plots.py` & `EllipSect-3.2.1/src/ellipsect/inout/plots.py`

 * *Files 14% similar despite different names*

```diff
@@ -16,14 +16,15 @@
 
 
 from ellipsect.lib.libs import *
 
 from ellipsect import *
 
 from ellipsect.sectors.num import Interpol
+from ellipsect.inout.prt import  PrintFilesGax
 
 
 def PlotSB(xradq,ysbq,ysberrq,xradm,ysbm,ysberrm,ellconf,scale):
     """  Produces final best-fitting plot  """
 
     # subplot for arc sec axis
     plt.close('all')
@@ -241,16 +242,15 @@
         ell = Comp2Ellip(galhead, galcomps, ellconf.tot, linewidth)
     else:
         ell=[]
 
 
     ShowCube(galhead.outimage, namepng = ellconf.namecube, dpival 
              = ellconf.dpival, bri = ellconf.brightness, con = ellconf.contrast, 
-             frac = ellconf.frac, fracmax = ellconf.fracmax,  cmap = ellconf.cmap, 
-             ellipse = ell)
+              cmap = ellconf.cmap, ellipse = ell, plate = galhead.scale)
 
 
     if ellconf.dplot:
         plt.pause(1.5)
  
     plt.close()
 
@@ -302,84 +302,128 @@
 
 
 
 
 class ShowCube:
 
     def __init__(self, cubeimg: str, namepng="cubeout.png", dpival=100, 
-                bri = 33, con = 0.98, frac = 1, fracmax = 1, cmap='viridis', ellipse=[]):
+                bri = 0, con = 1, cmap='viridis', ellipse=[], plate = 1):
         """
         This routine shows the GALFIT output cube image: galaxy, model and residual    
         """
 
         
         hdu = fits.open(cubeimg)
         data = (hdu[1].data.copy()).astype(float)
         model = (hdu[2].data.copy()).astype(float)
         residual = (hdu[3].data.copy()).astype(float)
         hdu.close()
 
-        flatmodimg=model.flatten()  
-        flatresimg=residual.flatten()  
+        flatmodimg = model.flatten()  
+        flatresimg = residual.flatten()  
 
         flatmodimg.sort()
         flatresimg.sort()
 
-        restot=len(flatresimg)
+        restot = len(flatresimg)
 
-        restop=round(.9*restot)
-        resbot=round(.1*restot)
+        restop = round(.9*restot)
+        resbot = round(.1*restot)
+
+        modtot = len(flatmodimg)
+
+        modtop = round(.9*modtot)
+        modbot = round(.1*modtot)
+
+
+
+        modimgpatch = flatmodimg#[modbot:modtop]
+        resimgpatch = flatresimg[resbot:restop]
+
+        resmin = np.min(resimgpatch)
+        resmax = np.max(resimgpatch)
 
-        modimgpatch=flatmodimg
-        resimgpatch=flatresimg[resbot:restop]
 
         modmin = np.min(modimgpatch)
         modmax = np.max(modimgpatch)
 
 
-        modmin = frac*modmin 
-        modmax = fracmax*modmax
+        data = data.clip(modmax/1e4,modmax)
+        model = model.clip(modmax/1e4)
 
+        modmin = modmax/1e4
 
 
+        middle = (modmax - modmin)/2
 
-        if (modmin > modmax):
-            modmin, modmax = modmax, modmin
 
+        #brightness auto-adjust according to the contrast value 
+
+        Autobri = middle*(con -1) + modmin*(1-con) 
+
+
+        #user can re-adjust brightness in addition to Autobri
+        newdata = con*(data - middle) + middle + Autobri + bri*(modmax-middle)
+        newmodel = con*(model - middle) + middle + Autobri + bri*(modmax-middle)
 
-        resmin = np.min(resimgpatch)
-        resmax = np.max(resimgpatch)
 
 
         mask=data < 0 
         data[mask] = 1 # avoids problems in log
      
         fig, (ax1, ax2, ax3) = plt.subplots(figsize=(14, 5), nrows = 1, ncols = 3)
         fig.subplots_adjust(left=0.04, right=0.98, bottom=0.02, top=0.98)
 
-        ax1.imshow(con*data + bri, origin ='lower', norm 
+        im = ax1.imshow(newdata, origin ='lower', interpolation='nearest', norm 
                     = colors.LogNorm(vmin=modmin, vmax=modmax), cmap = cmap)
 
+
         ax1.set_title('Data')
 
+        y,x = data.shape
+
+        xt = .02*x
+        yt = .02*y
+
+        lxline = round(.1*x)
+        lyline = round(.1*y)
+        x1 = [xt, xt+lxline]
+        y1 = [lyline, lyline]
+
+        arcsec = lxline*plate*U.arcsec 
+
+
+        if arcsec.value >= 60:
+            lxlinearc = arcsec.to("arcmin").value
+            s = "{}\'".format(round(lxlinearc))
+        else:
+            lxlinearc = arcsec.value
+            s = "{}\'\'".format(round(lxlinearc))
+ 
+        ax1.plot(x1, y1, color="white", linewidth=3)
+
+        ax1.text(xt+round(lxline/5),lyline+yt,s,color='white',fontsize=14)
+    
+        #ax1.set_xlabel(r'$\circ$')
+        #ax2.set_ylabel('23\"')
 
         for ell in ellipse:
             ax1.add_patch(ell)
 
 
-        ax2.imshow(con*model + bri, origin='lower', norm 
+        ax2.imshow(newmodel, origin='lower', interpolation='nearest', norm 
                     = colors.LogNorm(vmin = modmin, vmax = modmax), cmap = cmap)
+
+
         ax2.set_title('GALFIT Model')
 
         ax3.imshow(residual, origin='lower', vmin = resmin, vmax = resmax, cmap = cmap)
         ax3.set_title('Residual')
 
 
-
-
         plt.savefig(namepng, dpi = dpival)
     
 
         #plt.show()
 
 
 def PlotMul(ellconf, galhead, galcomps, mgegal, mgemod, mgecom):
@@ -418,15 +462,15 @@
 
 
     if ellconf.flagpix:
         axpix = axsec[0,0].twiny()
         axpix2 = axsec[0,1].twiny()
 
     fig.text(0.04, 0.5, "Surface Brightness (mag/'')", va='center', rotation='vertical')
-    fig.text(0.96, 0.5, 'error (%)', va='center', rotation='vertical')
+    fig.text(0.96, 0.5, 'error ', va='center', rotation='vertical')
 
     axsec[-1, 0].set_xlabel("radius ('')")
     axsec[-1, 1].set_xlabel("radius ('')")
 
     if ellconf.flaglogx == True:
         axsec[-1, 0].xaxis.set_major_locator(LogLocator(base=10.0, numticks=15))
         if ellconf.flagpix:
```

### Comparing `EllipSect-3.0.1/src/ellipsect/inout/prt.py` & `EllipSect-3.2.1/src/ellipsect/inout/prt.py`

 * *Files 0% similar despite different names*

```diff
@@ -345,15 +345,15 @@
     print(str)
     ##
 
     print("grey angle at lower-bottom in multi-plot is measured from the galaxy's major axis ")
     print("red angle at upper-right in multi-plot is measured from the Y-axis (same as GALFIT)\n")
 
 
-    print("In multi-plot, each color represents the same as the ones in the single-plot's legend")
+    print("In multi-plot, every color represents the same as the ones in the single-plot's legend")
 
 
 
 
 def printPhot(ellconf, galhead, galcomps, dataned, datatidal, sectgalax):
```

### Comparing `EllipSect-3.0.1/src/ellipsect/inout/read.py` & `EllipSect-3.2.1/src/ellipsect/inout/read.py`

 * *Files 10% similar despite different names*

```diff
@@ -103,23 +103,23 @@
     parser.add_argument("-skb","--skybox", type=int, help="pixel size of the box for randsky. Default = 20",default=20)
     parser.add_argument("-skn","--skynum", type=int, help="Number of boxes used in randsky. Default = 20",default=20)
     parser.add_argument("-skw","--skywidth", type=int, help="width of the ring for gradsky. Default = 20 ",default=20)
     parser.add_argument("-distm","--distmax", type=float, help="maximum distance among model centers to be considered to be part of the same galaxy ")
     parser.add_argument("-fw","--fwhm", type=float, help="It is used to compute Area_psf for BICres. It also draws a vertical line at the given value. Default = 2 pixels ")
 
 
-    parser.add_argument("-fr","--frac", type=float, help="fraction of the minimum model count to be used as vmin of imshow for the cube image ",default=1)
+    #parser.add_argument("-fr","--frac", type=float, help="fraction of the minimum model count to be used as vmin of imshow for the cube image ",default=1)
 
-    parser.add_argument("-frm","--fracmax", type=float, help="fraction of the maximum model count to be used as vmax of imshow for the cube image ",default=1)
+    #parser.add_argument("-frm","--fracmax", type=float, help="fraction of the maximum model count to be used as vmax of imshow for the cube image ",default=1)
 
 
     parser.add_argument("-br","--brightness", type=float, 
-                        help="brightness of the image. Only for galaxy and model. Default = 33", default=33)
+                        help="brightness of the image. Only for galaxy and model. Default = 0. Preferible range goes from -1 to 1", default=0)
     parser.add_argument("-co","--contrast", type=float, 
-                        help="contrast of the image. Only for galaxy and model. Default = 0.98",default=0.98)
+                        help="contrast of the image. Only for galaxy and model. Default = 1. Preferible range goes from 0 to 1",default=1)
 
 
 
     parser.add_argument("-cm","--cmap", type=str, help="cmap to be used for the cube image ",default="viridis")
 
 
     parser.add_argument("-nc","--numcomp", type=int, help="component number to" 
@@ -479,44 +479,67 @@
 
 
 def prefixNames(ellconf, outimage):
     '''names of the output files based on prefix of galfit output'''
 
     #note: make one function to save all the names: 
     root_ext = os.path.splitext(outimage)
-
     ellconf.namefile = root_ext[0]
-
-    # names for the different png
-    ellconf.namepng = ellconf.namefile + ".png"
-    ellconf.namesec = ellconf.namefile + "-gal.png"
-    ellconf.namemod = ellconf.namefile + "-mod.png"
-    ellconf.namemul = ellconf.namefile + "-mul.png"
-    ellconf.namesub = ellconf.namefile + "-comp.fits"
-
-    ellconf.namesig = ellconf.namefile + "-sig.fits"
-
-
-    ellconf.sboutput = ellconf.namefile + "-sbout"
-    ellconf.output = ellconf.namefile + "-out.txt"
-
-    ellconf.namened = ellconf.namefile + "-ned.xml"
-
-
-
-    ellconf.namesnr = ellconf.namefile + "-snr.fits"
-
-    ellconf.namecheck = ellconf.namefile + "-check.fits"
-    
-    ellconf.namering = ellconf.namefile + "-ring.fits"
     
-    ellconf.nameringmask = ellconf.namefile + "-ringmask.fits"
+    #adding numbers of galfit file for output
+    gal_ext = os.path.splitext(ellconf.galfile)
+    numstr = gal_ext[1] 
+    numstr = numstr[1:]
+
+    if numstr.isnumeric():
+
+        # names for the different png
+        ellconf.namepng = ellconf.namefile + '-' + numstr + ".png"
+        ellconf.namesec = ellconf.namefile + '-' + numstr + "-gal.png"
+        ellconf.namemod = ellconf.namefile + '-' + numstr + "-mod.png"
+        ellconf.namemul = ellconf.namefile + '-' + numstr + "-mul.png"
+        ellconf.namesub = ellconf.namefile + '-' + numstr + "-comp.fits"
+
+        ellconf.namesig = ellconf.namefile + '-' + numstr + "-sig.fits"
+
+
+        ellconf.sboutput = ellconf.namefile + '-' + numstr + "-sbout"
+        ellconf.output = ellconf.namefile + '-' + numstr + "-out.txt"
+
+        ellconf.namened = ellconf.namefile + '-' + numstr + "-ned.xml"
+
+        ellconf.namesnr = ellconf.namefile + '-' + numstr + "-snr.fits"
+        ellconf.namecheck = ellconf.namefile + '-' + numstr + "-check.fits"
+        ellconf.namering = ellconf.namefile + '-' + numstr + "-ring.fits"
+        ellconf.nameringmask = ellconf.namefile + '-' + numstr + "-ringmask.fits"
+        ellconf.namecube = ellconf.namefile + '-' + numstr + "-cub.png"
+        ellconf.namechi = ellconf.namefile + '-' + numstr + "-chi.fits"
 
-    ellconf.namecube = ellconf.namefile + "-cub.png"
+    else:
 
+        # names for the different png
+        ellconf.namepng = ellconf.namefile + ".png"
+        ellconf.namesec = ellconf.namefile + "-gal.png"
+        ellconf.namemod = ellconf.namefile + "-mod.png"
+        ellconf.namemul = ellconf.namefile + "-mul.png"
+        ellconf.namesub = ellconf.namefile + "-comp.fits"
+
+        ellconf.namesig = ellconf.namefile + "-sig.fits"
+
+
+        ellconf.sboutput = ellconf.namefile + "-sbout"
+        ellconf.output = ellconf.namefile + "-out.txt"
+
+        ellconf.namened = ellconf.namefile + "-ned.xml"
+
+        ellconf.namesnr = ellconf.namefile + "-snr.fits"
+        ellconf.namecheck = ellconf.namefile + "-check.fits"
+        ellconf.namering = ellconf.namefile + "-ring.fits"
+        ellconf.nameringmask = ellconf.namefile + "-ringmask.fits"
+        ellconf.namecube = ellconf.namefile + "-cub.png"
+        ellconf.namechi = ellconf.namefile + "-chi.fits"
 
-    ellconf.namechi = ellconf.namefile + "-chi.fits"
 
 
 
     return True
```

### Comparing `EllipSect-3.0.1/src/ellipsect/lib/clas.py` & `EllipSect-3.2.1/src/ellipsect/lib/clas.py`

 * *Files 2% similar despite different names*

```diff
@@ -151,21 +151,19 @@
     skynum = 20
     skywidth = 20
 
     fwhm = 2
 
     distmax = 10
 
-    brightness = 33 
-    contrast = 0.98
+    brightness = 0 
+    contrast = 1 
 
     cmap="viridis"
 
-    frac = 1
-    fracmax = 1
 
     numcomp = 1
     tot = 0 # total number of components
 
 
     # for computed gradsky
     gradskymean = 0
```

### Comparing `EllipSect-3.0.1/src/ellipsect/lib/libs.py` & `EllipSect-3.2.1/src/ellipsect/lib/libs.py`

 * *Files 12% similar despite different names*

```diff
@@ -41,11 +41,11 @@
 from astropy.io.votable import parse
 from mgefit.sectors_photometry import sectors_photometry
 
 from matplotlib.ticker import (MultipleLocator, FormatStrFormatter,NullFormatter,
                                AutoMinorLocator,LogLocator,LinearLocator,AutoLocator)
 
 
-
+from astropy import units as U
```

### Comparing `EllipSect-3.0.1/src/ellipsect/phot/ned.py` & `EllipSect-3.2.1/src/ellipsect/phot/ned.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/phot/phot.py` & `EllipSect-3.2.1/src/ellipsect/phot/phot.py`

 * *Files 1% similar despite different names*

```diff
@@ -211,21 +211,21 @@
         warnings.simplefilter("ignore")
 
 
     ################################################################
     ################################################################
     print('computing the effective radius for the whole galaxy')
     eff = 0.5
-    EffRad, tempmag = GetReff().GetReSer(galhead, galcomps, eff)
+    EffRad, tempmag = GetReff().GetReSer(galhead, galcomps, eff, ellconf.parg)
 
     eff = 0.9
-    EffRad9, tempmag = GetReff().GetReSer(galhead, galcomps, eff)
+    EffRad9, tempmag = GetReff().GetReSer(galhead, galcomps, eff, ellconf.parg)
 
     eff = 0.3
-    EffRad3, tempmag = GetReff().GetReSer(galhead, galcomps, eff)
+    EffRad3, tempmag = GetReff().GetReSer(galhead, galcomps, eff, ellconf.parg)
 
     datatidal.EffRad = EffRad
     datatidal.EffRad9 = EffRad9
     datatidal.EffRad3 = EffRad3
     ################################################################
     ################################################################
```

### Comparing `EllipSect-3.0.1/src/ellipsect/phot/tidal.py` & `EllipSect-3.2.1/src/ellipsect/phot/tidal.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/sectors/comp.py` & `EllipSect-3.2.1/src/ellipsect/sectors/comp.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/sectors/ellip.py` & `EllipSect-3.2.1/src/ellipsect/sectors/ellip.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/sectors/num.py` & `EllipSect-3.2.1/src/ellipsect/sectors/num.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/src/ellipsect/sectors/sect.py` & `EllipSect-3.2.1/src/ellipsect/sectors/sect.py`

 * *Files 2% similar despite different names*

```diff
@@ -43,15 +43,14 @@
 
 
 from ellipsect.lib.clas import PhotAPI 
 
 
 def SectorsGalfit(args):
 
-
     ellconf = PassArgs(args) # from now on, ellconf is used instead of args
 
 
     ######################################
     ####### Read Galfit File #############
 
 
@@ -77,14 +76,18 @@
     print("Number of components = ",N)
 
     ellconf.tot = N
 
     #creates names of the output files based on prefix of galfit output
     prefixNames(ellconf, galhead.outimage)
 
+    if os.path.isfile(galhead.sigimage):
+        ellconf.namesig = galhead.sigimage #using existing sigma file
+
+
 
 
     if ellconf.flagsbout == True: 
 
         if not os.path.exists("sbfiles"):
             print("Creating directory for output photometry ... ")
             os.makedirs("sbfiles")
@@ -100,15 +103,14 @@
 
     dataimg = readDataImg(ellconf, galhead)
 
     # removing background from galaxy and model images 
     dataimg.img = dataimg.img - ellconf.skylevel
     dataimg.model = dataimg.model - ellconf.skylevel
 
-
     plotCube(ellconf, galhead, galcomps) #plots the cube image
 
 
     #   numsectors=19 default
     numsectors = ellconf.sectors
 
     minlevel = ellconf.minlevel  # minimun value for sky
@@ -708,28 +710,18 @@
     if args.fwhm:
         ellconf.flagfwhm= True
         ellconf.fwhm= args.fwhm
 
     if args.brightness:
         ellconf.brightness = args.brightness
 
-
     if args.contrast:
         ellconf.contrast = args.contrast
 
 
-    if args.frac:
-        ellconf.frac = args.frac
-
-    if args.fracmax:
-        ellconf.fracmax = args.fracmax
-
-
-
-
     if args.cmap:
         ellconf.cmap = args.cmap
 
     if args.numcomp:
         ellconf.numcomp = args.numcomp
 
     if args.aext:
```

### Comparing `EllipSect-3.0.1/src/ellipsect/sky/sky.py` & `EllipSect-3.2.1/src/ellipsect/sky/sky.py`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/tests/gal.fits` & `EllipSect-3.2.1/tests/gal.fits`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/tests/galfit.01` & `EllipSect-3.2.1/tests/galfit.01`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/tests/imgblock.fits` & `EllipSect-3.2.1/tests/imgblock.fits`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/tests/psf.fits` & `EllipSect-3.2.1/tests/psf.fits`

 * *Files identical despite different names*

### Comparing `EllipSect-3.0.1/tests/test_ellipsect.py` & `EllipSect-3.2.1/tests/test_ellipsect.py`

 * *Files 3% similar despite different names*

```diff
@@ -35,16 +35,16 @@
 # checking the creation of files
 def test_files():
 
     arg=['tests/galfit.01', '-np']
 
     path="tests/"
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock-01.png"
+    filemulpng = "imgblock-01-mul.png"
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
     if os.path.isfile(filepng):
         os.remove(filepng)
     if os.path.isfile(filemulpng):
@@ -74,23 +74,23 @@
 # checking the creation of the components file
 def test_comp():
 
     arg=['tests/galfit.01','--comp', '--noplot']
 
     path="tests/"
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock-01.png"
+    filemulpng = "imgblock-01-mul.png"
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
 
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
 
     filecomp= path+filecomp
 
     if os.path.isfile(filecomp):
         os.remove(filecomp)
 
 
@@ -124,30 +124,30 @@
 def test_phot():
 
 
     arg=['tests/galfit.01','--phot', '--noned', '--noplot']
 
     path="tests/"
 
-    filephot = "imgblock-out.txt"
+    filephot = "imgblock-01-out.txt"
     filephot= path+filephot
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
     filecomp= path+filecomp
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock-01.png"
+    filemulpng = "imgblock-01-mul.png"
 
-    filesig = "imgblock-sig.fits"
+    filesig = "imgblock-01-sig.fits"
     filesig= path+filesig
 
-    filecheck = "imgblock-check.fits"
+    filecheck = "imgblock-01-check.fits"
     filecheck= path+filecheck
 
-    filecube = "imgblock-cub.png"
+    filecube = "imgblock-01-cub.png"
     filecube = path+filecube
 
 
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
@@ -255,36 +255,36 @@
 def test_gsky():
 
 
     arg=['tests/galfit.01','-gsky', '-ri','2', '-skw','3','--noplot']
 
     path="tests/"
 
-    filephot = "imgblock-out.txt"
+    filephot = "imgblock-01-out.txt"
     filephot= path+filephot
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
     filecomp= path+filecomp
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock-01.png"
+    filemulpng = "imgblock-01-mul.png"
 
-    filesig = "imgblock-sig.fits"
+    filesig = "imgblock-01-sig.fits"
     filesig= path+filesig
 
-    filecheck = "imgblock-check.fits"
+    filecheck = "imgblock-01-check.fits"
     filecheck= path+filecheck
 
-    filecube = "imgblock-cub.png"
+    filecube = "imgblock-01-cub.png"
     filecube = path+filecube
 
-    filersky = "imgblock-ring.fits"
+    filersky = "imgblock-01-ring.fits"
     filersky = path + filersky
 
-    filermsky = "imgblock-ringmask.fits"
+    filermsky = "imgblock-01-ringmask.fits"
     filermsky = path + filermsky
 
 
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
@@ -370,36 +370,36 @@
 def test_rsky():
 
 
     arg=['tests/galfit.01','-rsky','--noplot']
 
     path="tests/"
 
-    filephot = "imgblock-out.txt"
+    filephot = "imgblock-01-out.txt"
     filephot= path+filephot
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
     filecomp= path+filecomp
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock.01-png"
+    filemulpng = "imgblock-01-mul.png"
 
-    filesig = "imgblock-sig.fits"
+    filesig = "imgblock-01-sig.fits"
     filesig= path+filesig
 
-    filecheck = "imgblock-check.fits"
+    filecheck = "imgblock-01-check.fits"
     filecheck= path+filecheck
 
-    filecube = "imgblock-cub.png"
+    filecube = "imgblock-01-cub.png"
     filecube = path+filecube
 
-    filersky = "imgblock-ring.fits"
+    filersky = "imgblock-01-ring.fits"
     filersky = path + filersky
 
-    filermsky = "imgblock-ringmask.fits"
+    filermsky = "imgblock-01-ringmask.fits"
     filermsky = path + filermsky
 
 
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
@@ -487,36 +487,36 @@
 def test_freepar():
 
 
     arg=['tests/galfit.01','--noplot']
 
     path="tests/"
 
-    filephot = "imgblock-out.txt"
+    filephot = "imgblock-01-out.txt"
     filephot= path+filephot
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
     filecomp= path+filecomp
 
-    filepng = "imgblock.png"
+    filepng = "imgblock-01.png"
     filemulpng = "imgblock-mul.png"
 
-    filesig = "imgblock-sig.fits"
+    filesig = "imgblock-01-sig.fits"
     filesig= path+filesig
 
-    filecheck = "imgblock-check.fits"
+    filecheck = "imgblock-01-check.fits"
     filecheck= path+filecheck
 
-    filecube = "imgblock-cub.png"
+    filecube = "imgblock-01-cub.png"
     filecube = path+filecube
 
-    filersky = "imgblock-ring.fits"
+    filersky = "imgblock-01-ring.fits"
     filersky = path + filersky
 
-    filermsky = "imgblock-ringmask.fits"
+    filermsky = "imgblock-01-ringmask.fits"
     filermsky = path + filermsky
 
 
 
     filepng = path+filepng
     filemulpng = path+filemulpng
 
@@ -620,36 +620,36 @@
 def test_img_size():
 
 
     arg=['tests/galfit.01','--noplot']
 
     path="tests/"
 
-    filephot = "imgblock-out.txt"
+    filephot = "imgblock-01-out.txt"
     filephot= path+filephot
 
-    filecomp = "imgblock-comp.fits"
+    filecomp = "imgblock-01-comp.fits"
     filecomp= path+filecomp
 
-    filepng = "imgblock.png"
-    filemulpng = "imgblock-mul.png"
+    filepng = "imgblock-01.png"
+    filemulpng = "imgblock-01-mul.png"
 
-    filesig = "imgblock-sig.fits"
+    filesig = "imgblock-01-sig.fits"
     filesig= path+filesig
 
-    filecheck = "imgblock-check.fits"
+    filecheck = "imgblock-01-check.fits"
     filecheck= path+filecheck
 
-    filecube = "imgblock-cub.png"
+    filecube = "imgblock-01-cub.png"
     filecube = path+filecube
 
-    filersky = "imgblock-ring.fits"
+    filersky = "imgblock-01-ring.fits"
     filersky = path + filersky
 
-    filermsky = "imgblock-ringmask.fits"
+    filermsky = "imgblock-01-ringmask.fits"
     filermsky = path + filermsky
 
 
     tempmask="tempmask.fits"
     filetempmask = tempmask 
 
     filepng = path+filepng
```

### Comparing `EllipSect-3.0.1/tox.ini` & `EllipSect-3.2.1/tox.ini`

 * *Files identical despite different names*

