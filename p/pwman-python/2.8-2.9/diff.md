# Comparing `tmp/pwman-python-2.8.tar.gz` & `tmp/pwman-python-2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pwman-python-2.8.tar", last modified: Mon Apr 10 19:37:51 2023, max compression
+gzip compressed data, was "pwman-python-2.9.tar", last modified: Mon Apr 17 19:58:12 2023, max compression
```

## Comparing `pwman-python-2.8.tar` & `pwman-python-2.9.tar`

### file list

```diff
@@ -1,70 +1,70 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/
--rw-r--r--   0 root         (0) root         (0)    18092 2023-04-10 19:37:49.000000 pwman-python-2.8/COPYING
--rw-r--r--   0 root         (0) root         (0)      212 2023-04-10 19:37:49.000000 pwman-python-2.8/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)     4374 2023-04-10 19:37:51.594332 pwman-python-2.8/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     4831 2023-04-10 19:37:50.000000 pwman-python-2.8/README.html
--rw-r--r--   0 root         (0) root         (0)     3589 2023-04-10 19:37:49.000000 pwman-python-2.8/README.rst
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.590332 pwman-python-2.8/doc/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.590332 pwman-python-2.8/doc/api/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/doc/api/libpwman/
--rw-r--r--   0 root         (0) root         (0)     4007 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/aes.html
--rw-r--r--   0 root         (0) root         (0)    12876 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/cryptsql.html
--rw-r--r--   0 root         (0) root         (0)    39835 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/database.html
--rw-r--r--   0 root         (0) root         (0)     3868 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/dbdiff.html
--rw-r--r--   0 root         (0) root         (0)     5888 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/exception.html
--rw-r--r--   0 root         (0) root         (0)    10554 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/fileobj.html
--rw-r--r--   0 root         (0) root         (0)     4218 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/mlock.html
--rw-r--r--   0 root         (0) root         (0)     8077 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/otp.html
--rw-r--r--   0 root         (0) root         (0)    43114 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/ui.html
--rw-r--r--   0 root         (0) root         (0)     6301 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/ui_escape.html
--rw-r--r--   0 root         (0) root         (0)     2673 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/util.html
--rw-r--r--   0 root         (0) root         (0)     1345 2023-04-10 19:37:50.000000 pwman-python-2.8/doc/api/libpwman/version.html
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/doc/foreign-licenses/
--rw-r--r--   0 root         (0) root         (0)    12769 2023-04-10 19:37:49.000000 pwman-python-2.8/doc/foreign-licenses/PYTHON-LICENSE.txt
--rw-r--r--   0 root         (0) root         (0)      269 2023-04-10 19:37:49.000000 pwman-python-2.8/doc/foreign-licenses/README
--rw-r--r--   0 root         (0) root         (0)      863 2023-04-10 19:37:49.000000 pwman-python-2.8/examplescript.py
--rwxr-xr-x   0 root         (0) root         (0)      404 2023-04-10 19:37:49.000000 pwman-python-2.8/gitconfig.sh
--rwxr-xr-x   0 root         (0) root         (0)      853 2023-04-10 19:37:49.000000 pwman-python-2.8/install_to_venv.sh
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/libpwman/
--rw-r--r--   0 root         (0) root         (0)      326 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/__init__.py
--rw-r--r--   0 root         (0) root         (0)     7279 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/__main__.py
--rw-r--r--   0 root         (0) root         (0)     3239 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/aes.py
--rw-r--r--   0 root         (0) root         (0)    12852 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/cryptsql.py
--rw-r--r--   0 root         (0) root         (0)    24849 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/database.py
--rw-r--r--   0 root         (0) root         (0)     1681 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/dbdiff.py
--rw-r--r--   0 root         (0) root         (0)      251 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/exception.py
--rw-r--r--   0 root         (0) root         (0)     3523 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/fileobj.py
--rw-r--r--   0 root         (0) root         (0)     1916 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/mlock.py
--rw-r--r--   0 root         (0) root         (0)     2348 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/otp.py
--rw-r--r--   0 root         (0) root         (0)    52799 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/ui.py
--rw-r--r--   0 root         (0) root         (0)     1210 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/ui_escape.py
--rw-r--r--   0 root         (0) root         (0)     1776 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/util.py
--rw-r--r--   0 root         (0) root         (0)      380 2023-04-10 19:37:49.000000 pwman-python-2.8/libpwman/version.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/maintenance/
--rwxr-xr-x   0 root         (0) root         (0)      453 2023-04-10 19:37:49.000000 pwman-python-2.8/maintenance/cleantree.sh
--rwxr-xr-x   0 root         (0) root         (0)      103 2023-04-10 19:37:49.000000 pwman-python-2.8/maintenance/deb-dependencies-install.sh
--rwxr-xr-x   0 root         (0) root         (0)     1519 2023-04-10 19:37:49.000000 pwman-python-2.8/maintenance/gen-doc.sh
--rw-r--r--   0 root         (0) root         (0)      900 2023-04-10 19:37:49.000000 pwman-python-2.8/maintenance/win-install-dependencies.cmd
--rw-r--r--   0 root         (0) root         (0)     3674 2023-04-10 19:37:49.000000 pwman-python-2.8/maintenance/win-standalone-build.cmd
--rwxr-xr-x   0 root         (0) root         (0)      276 2023-04-10 19:37:49.000000 pwman-python-2.8/pwman
--rw-r--r--   0 root         (0) root         (0)      849 2023-04-10 19:37:49.000000 pwman-python-2.8/pwman.cmd
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/pwman_python.egg-info/
--rw-r--r--   0 root         (0) root         (0)     4374 2023-04-10 19:37:51.000000 pwman-python-2.8/pwman_python.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     1375 2023-04-10 19:37:51.000000 pwman-python-2.8/pwman_python.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-10 19:37:51.000000 pwman-python-2.8/pwman_python.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       14 2023-04-10 19:37:51.000000 pwman-python-2.8/pwman_python.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        9 2023-04-10 19:37:51.000000 pwman-python-2.8/pwman_python.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       19 2023-04-10 19:37:49.000000 pwman-python-2.8/requirements.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-04-10 19:37:51.594332 pwman-python-2.8/setup.cfg
--rwxr-xr-x   0 root         (0) root         (0)     1728 2023-04-10 19:37:49.000000 pwman-python-2.8/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-10 19:37:51.594332 pwman-python-2.8/tests/
--rw-r--r--   0 root         (0) root         (0)      133 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/__init__.py
--rw-r--r--   0 root         (0) root         (0)      186 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/pwman_tstlib.py
--rwxr-xr-x   0 root         (0) root         (0)     1325 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/run.sh
--rw-r--r--   0 root         (0) root         (0)      520 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_database_v0.db
--rw-r--r--   0 root         (0) root         (0)     1680 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_database_v0.py
--rw-r--r--   0 root         (0) root         (0)     2621 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_database_v1.db
--rw-r--r--   0 root         (0) root         (0)     3441 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_database_v1.py
--rw-r--r--   0 root         (0) root         (0)      427 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_escape.py
--rw-r--r--   0 root         (0) root         (0)     2399 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_otp.py
--rw-r--r--   0 root         (0) root         (0)     3647 2023-04-10 19:37:49.000000 pwman-python-2.8/tests/test_ui.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.101115 pwman-python-2.9/
+-rw-r--r--   0 root         (0) root         (0)    18092 2023-04-17 19:58:09.000000 pwman-python-2.9/COPYING
+-rw-r--r--   0 root         (0) root         (0)      212 2023-04-17 19:58:09.000000 pwman-python-2.9/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)     4374 2023-04-17 19:58:12.101115 pwman-python-2.9/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     4831 2023-04-17 19:58:10.000000 pwman-python-2.9/README.html
+-rw-r--r--   0 root         (0) root         (0)     3589 2023-04-17 19:58:09.000000 pwman-python-2.9/README.rst
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.097114 pwman-python-2.9/doc/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.097114 pwman-python-2.9/doc/api/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.097114 pwman-python-2.9/doc/api/libpwman/
+-rw-r--r--   0 root         (0) root         (0)     4007 2023-04-17 19:58:11.000000 pwman-python-2.9/doc/api/libpwman/aes.html
+-rw-r--r--   0 root         (0) root         (0)    12876 2023-04-17 19:58:11.000000 pwman-python-2.9/doc/api/libpwman/cryptsql.html
+-rw-r--r--   0 root         (0) root         (0)    40268 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/database.html
+-rw-r--r--   0 root         (0) root         (0)     3868 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/dbdiff.html
+-rw-r--r--   0 root         (0) root         (0)     5888 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/exception.html
+-rw-r--r--   0 root         (0) root         (0)     9734 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/fileobj.html
+-rw-r--r--   0 root         (0) root         (0)     4218 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/mlock.html
+-rw-r--r--   0 root         (0) root         (0)     8077 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/otp.html
+-rw-r--r--   0 root         (0) root         (0)    42993 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/ui.html
+-rw-r--r--   0 root         (0) root         (0)     6301 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/ui_escape.html
+-rw-r--r--   0 root         (0) root         (0)     2590 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/util.html
+-rw-r--r--   0 root         (0) root         (0)     1345 2023-04-17 19:58:10.000000 pwman-python-2.9/doc/api/libpwman/version.html
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.097114 pwman-python-2.9/doc/foreign-licenses/
+-rw-r--r--   0 root         (0) root         (0)    13936 2023-04-17 19:58:09.000000 pwman-python-2.9/doc/foreign-licenses/PYTHON-LICENSE.txt
+-rw-r--r--   0 root         (0) root         (0)      269 2023-04-17 19:58:09.000000 pwman-python-2.9/doc/foreign-licenses/README
+-rw-r--r--   0 root         (0) root         (0)      863 2023-04-17 19:58:09.000000 pwman-python-2.9/examplescript.py
+-rwxr-xr-x   0 root         (0) root         (0)      404 2023-04-17 19:58:09.000000 pwman-python-2.9/gitconfig.sh
+-rwxr-xr-x   0 root         (0) root         (0)      853 2023-04-17 19:58:09.000000 pwman-python-2.9/install_to_venv.sh
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.101115 pwman-python-2.9/libpwman/
+-rw-r--r--   0 root         (0) root         (0)      429 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     7279 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/__main__.py
+-rw-r--r--   0 root         (0) root         (0)     3239 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/aes.py
+-rw-r--r--   0 root         (0) root         (0)    12815 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/cryptsql.py
+-rw-r--r--   0 root         (0) root         (0)    27175 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/database.py
+-rw-r--r--   0 root         (0) root         (0)     1681 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/dbdiff.py
+-rw-r--r--   0 root         (0) root         (0)      251 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/exception.py
+-rw-r--r--   0 root         (0) root         (0)     3848 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/fileobj.py
+-rw-r--r--   0 root         (0) root         (0)     1916 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/mlock.py
+-rw-r--r--   0 root         (0) root         (0)     2133 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/otp.py
+-rw-r--r--   0 root         (0) root         (0)    49977 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/ui.py
+-rw-r--r--   0 root         (0) root         (0)     1210 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/ui_escape.py
+-rw-r--r--   0 root         (0) root         (0)     1693 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/util.py
+-rw-r--r--   0 root         (0) root         (0)      380 2023-04-17 19:58:09.000000 pwman-python-2.9/libpwman/version.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.101115 pwman-python-2.9/maintenance/
+-rwxr-xr-x   0 root         (0) root         (0)      453 2023-04-17 19:58:09.000000 pwman-python-2.9/maintenance/cleantree.sh
+-rwxr-xr-x   0 root         (0) root         (0)      103 2023-04-17 19:58:09.000000 pwman-python-2.9/maintenance/deb-dependencies-install.sh
+-rwxr-xr-x   0 root         (0) root         (0)     1519 2023-04-17 19:58:09.000000 pwman-python-2.9/maintenance/gen-doc.sh
+-rw-r--r--   0 root         (0) root         (0)      900 2023-04-17 19:58:09.000000 pwman-python-2.9/maintenance/win-install-dependencies.cmd
+-rw-r--r--   0 root         (0) root         (0)     3674 2023-04-17 19:58:09.000000 pwman-python-2.9/maintenance/win-standalone-build.cmd
+-rwxr-xr-x   0 root         (0) root         (0)      276 2023-04-17 19:58:09.000000 pwman-python-2.9/pwman
+-rw-r--r--   0 root         (0) root         (0)      849 2023-04-17 19:58:09.000000 pwman-python-2.9/pwman.cmd
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.101115 pwman-python-2.9/pwman_python.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     4374 2023-04-17 19:58:12.000000 pwman-python-2.9/pwman_python.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     1375 2023-04-17 19:58:12.000000 pwman-python-2.9/pwman_python.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-04-17 19:58:12.000000 pwman-python-2.9/pwman_python.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       14 2023-04-17 19:58:12.000000 pwman-python-2.9/pwman_python.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        9 2023-04-17 19:58:12.000000 pwman-python-2.9/pwman_python.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       19 2023-04-17 19:58:09.000000 pwman-python-2.9/requirements.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-04-17 19:58:12.101115 pwman-python-2.9/setup.cfg
+-rwxr-xr-x   0 root         (0) root         (0)     1682 2023-04-17 19:58:09.000000 pwman-python-2.9/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-17 19:58:12.101115 pwman-python-2.9/tests/
+-rw-r--r--   0 root         (0) root         (0)      133 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      186 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/pwman_tstlib.py
+-rwxr-xr-x   0 root         (0) root         (0)     1325 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/run.sh
+-rw-r--r--   0 root         (0) root         (0)      520 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_database_v0.db
+-rw-r--r--   0 root         (0) root         (0)     1680 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_database_v0.py
+-rw-r--r--   0 root         (0) root         (0)     2621 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_database_v1.db
+-rw-r--r--   0 root         (0) root         (0)     3441 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_database_v1.py
+-rw-r--r--   0 root         (0) root         (0)      427 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_escape.py
+-rw-r--r--   0 root         (0) root         (0)     2399 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_otp.py
+-rw-r--r--   0 root         (0) root         (0)     8554 2023-04-17 19:58:09.000000 pwman-python-2.9/tests/test_ui.py
```

### Comparing `pwman-python-2.8/COPYING` & `pwman-python-2.9/COPYING`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/PKG-INFO` & `pwman-python-2.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pwman-python
-Version: 2.8
+Version: 2.9
 Summary: Commandline password manager
 Home-page: https://bues.ch/h/pwman
 Author: Michael Büsch
 Author-email: m@bues.ch
 Keywords: password manager command line TOTP 2FA
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `pwman-python-2.8/README.html` & `pwman-python-2.9/README.html`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/README.rst` & `pwman-python-2.9/README.rst`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/doc/api/libpwman/aes.html` & `pwman-python-2.9/doc/api/libpwman/aes.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module aes</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">aes</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/aes.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/aes.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/aes.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/aes.py</a></td></tr></table>
     <p><span class="code">#&nbsp;<a href="#AES">AES</a>&nbsp;wrapper<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
    index
-aes /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/aes.py
+aes /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/aes.py
 # AES wrapper
 # Copyright (c) 2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � os�
```

### Comparing `pwman-python-2.8/doc/api/libpwman/cryptsql.html` & `pwman-python-2.9/doc/api/libpwman/cryptsql.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module cryptsql</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">cryptsql</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/cryptsql.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/cryptsql.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/cryptsql.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/cryptsql.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Crypto&nbsp;SQL<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
         index
-cryptsql /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+cryptsql /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
          cryptsql.py
 # Crypto SQL
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � functools re      sqlite3
```

### Comparing `pwman-python-2.8/doc/api/libpwman/database.html` & `pwman-python-2.9/doc/api/libpwman/database.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module database</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">database</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/database.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/database.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/database.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/database.py</a></td></tr></table>
     <p><span class="code">#<br>
 #&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Encrypted&nbsp;database<br>
 #<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.<br>
 #</span></p>
@@ -231,22 +231,26 @@
 
 <dl><dt><a name="PWManDatabase-importSqlScript"><strong>importSqlScript</strong></a>(self, *args, **kwargs)</dt><dd><span class="code">Imports&nbsp;a&nbsp;plain&nbsp;text&nbsp;dump&nbsp;into&nbsp;the&nbsp;database.<br>
 script:&nbsp;The&nbsp;script&nbsp;string&nbsp;to&nbsp;import.<br>
 clear:&nbsp;If&nbsp;True,&nbsp;drop&nbsp;all&nbsp;tables&nbsp;from&nbsp;the&nbsp;database&nbsp;before&nbsp;importing.</span></dd></dl>
 
 <dl><dt><a name="PWManDatabase-isDirty"><strong>isDirty</strong></a>(self)</dt><dd><span class="code">Returns&nbsp;True,&nbsp;if&nbsp;the&nbsp;database&nbsp;contains&nbsp;uncommitted&nbsp;data.</span></dd></dl>
 
-<dl><dt><a name="PWManDatabase-moveEntries"><strong>moveEntries</strong></a>(self, fromCategory, toCategory)</dt><dd><span class="code">Move&nbsp;all&nbsp;entries&nbsp;from&nbsp;one&nbsp;category&nbsp;to&nbsp;another&nbsp;category.<br>
+<dl><dt><a name="PWManDatabase-moveEntries"><strong>moveEntries</strong></a>(self, fromCategory, toCategory, toDb=None, copy=False)</dt><dd><span class="code">Move&nbsp;or&nbsp;copy&nbsp;all&nbsp;entries&nbsp;from&nbsp;one&nbsp;category&nbsp;to&nbsp;another&nbsp;category.<br>
 fromCategory:&nbsp;The&nbsp;category&nbsp;to&nbsp;move&nbsp;all&nbsp;entries&nbsp;from.<br>
-toCategory:&nbsp;The&nbsp;(new)&nbsp;category&nbsp;to&nbsp;move&nbsp;all&nbsp;entries&nbsp;to.</span></dd></dl>
-
-<dl><dt><a name="PWManDatabase-moveEntry"><strong>moveEntry</strong></a>(self, entry, newCategory, newTitle)</dt><dd><span class="code">Move&nbsp;an&nbsp;existing&nbsp;entry&nbsp;to&nbsp;a&nbsp;new&nbsp;category&nbsp;and/or&nbsp;set&nbsp;a&nbsp;new&nbsp;entry&nbsp;title.<br>
-entry:&nbsp;The&nbsp;<a href="#PWManEntry">PWManEntry</a>()&nbsp;instance&nbsp;to&nbsp;move.<br>
-newCategory:&nbsp;The&nbsp;new&nbsp;category&nbsp;name&nbsp;string.<br>
-newTitle:&nbsp;The&nbsp;new&nbsp;title&nbsp;string.</span></dd></dl>
+toCategory:&nbsp;The&nbsp;(new)&nbsp;category&nbsp;to&nbsp;move&nbsp;all&nbsp;entries&nbsp;to.<br>
+toDb:&nbsp;The&nbsp;target&nbsp;database.&nbsp;Defaults&nbsp;to&nbsp;self.<br>
+copy:&nbsp;If&nbsp;False,&nbsp;then&nbsp;move.&nbsp;If&nbsp;True,&nbsp;then&nbsp;copy.</span></dd></dl>
+
+<dl><dt><a name="PWManDatabase-moveEntry"><strong>moveEntry</strong></a>(self, entry, newCategory, newTitle, toDb=None, copy=False)</dt><dd><span class="code">Move&nbsp;or&nbsp;copy&nbsp;an&nbsp;existing&nbsp;entry&nbsp;to&nbsp;a&nbsp;new&nbsp;category&nbsp;and/or&nbsp;set&nbsp;a&nbsp;new&nbsp;entry&nbsp;title.<br>
+entry:&nbsp;The&nbsp;<a href="#PWManEntry">PWManEntry</a>()&nbsp;instance&nbsp;to&nbsp;move/copy.<br>
+newCategory:&nbsp;The&nbsp;target&nbsp;category&nbsp;name&nbsp;string.<br>
+newTitle:&nbsp;The&nbsp;target&nbsp;title&nbsp;string.<br>
+toDb:&nbsp;The&nbsp;target&nbsp;database.&nbsp;Defaults&nbsp;to&nbsp;self.<br>
+copy:&nbsp;If&nbsp;False,&nbsp;then&nbsp;move.&nbsp;If&nbsp;True,&nbsp;then&nbsp;copy.</span></dd></dl>
 
 <dl><dt><a name="PWManDatabase-setEntryAttr"><strong>setEntryAttr</strong></a>(self, entryAttr)</dt><dd><span class="code">Set&nbsp;an&nbsp;attribute&nbsp;associated&nbsp;with&nbsp;an&nbsp;entry.<br>
 entryAttr:&nbsp;The&nbsp;new&nbsp;<a href="#PWManEntryAttr">PWManEntryAttr</a>()&nbsp;instance&nbsp;to&nbsp;write&nbsp;to&nbsp;the&nbsp;database.<br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If&nbsp;entryAttr.data&nbsp;is&nbsp;None,&nbsp;then&nbsp;the&nbsp;attribute&nbsp;is&nbsp;deleted.</span></dd></dl>
 
 <dl><dt><a name="PWManDatabase-setEntryBulk"><strong>setEntryBulk</strong></a>(self, entryBulk)</dt><dd><span class="code">Set&nbsp;the&nbsp;bulk&nbsp;data&nbsp;associated&nbsp;with&nbsp;an&nbsp;entry.<br>
 entryBulk:&nbsp;The&nbsp;new&nbsp;<a href="#PWManEntryBulk">PWManEntryBulk</a>()&nbsp;instance&nbsp;to&nbsp;write&nbsp;to&nbsp;the&nbsp;database.<br>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
         index
-database /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+database /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
          database.py
 #
 # Simple password manager
 # Encrypted database
 #
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
@@ -28,27 +28,27 @@
              CryptSQL exception.
               
                  Method resolution order:
                      CSQLError
                      builtins.Exception
                      builtins.BaseException
                      builtins.object
-               ==============================================================================================
+               ===================================================================================================
                Data descriptors defined here:
                  __weakref__
                      list of weak references to the object (if defined)
-               ==============================================================================================
+               ===================================================================================================
                Methods inherited from builtins.Exception:
                  __init__(self, /, *args, **kwargs)
                      Initialize self.  See help(type(self)) for accurate signature.
-               ==============================================================================================
+               ===================================================================================================
                Static methods inherited from builtins.Exception:
                  __new__(*args, **kwargs) from builtins.type
                      Create and return a new object.  See help(type) for accurate signature.
-               ==============================================================================================
+               ===================================================================================================
                Methods inherited from builtins.BaseException:
                  __delattr__(self, name, /)
                      Implement delattr(self, name).
                  __getattribute__(self, name, /)
                   Return getattr(self, name).
                 __reduce__(...)
                      Helper for pickle.
@@ -61,15 +61,15 @@
                      Return str(self).
                  add_note(...)
                      Exception.add_note(note) --
                      add a note to the exception
                  with_traceback(...)
                      Exception.with_traceback(tb) --
                      set self.__traceback__ to tb and return self.
-               ==============================================================================================
+               ===================================================================================================
                Data descriptors inherited from builtins.BaseException:
                  __cause__
                      exception cause
                  __context__
                      exception context
                  __dict__
                  __suppress_context__
@@ -81,15 +81,15 @@
               
              Encrypted pwman database.
               
                  Method resolution order:
                      PWManDatabase
                      libpwman.cryptsql.CryptSQL
                      builtins.object
-               ==============================================================================================
+               ===================================================================================================
                Methods defined here:
                  __init__(self, filename, passphrase, key=None, readOnly=True, silent=False)
                      filename: Path to the database file.
                                   If it does not exist, a new file is created.
                      passphrase: The passphrase string for the database file.
                      key: An optional key to use instead of the passphrase. Don't use it.
                      readOnly: Open the filename read-only. Commits will raise an exception.
@@ -119,17 +119,17 @@
                  editEntry(self, entry)
                      Update the contents of an existing entry.
                      entry: A PWManEntry() containing the new data of the entry/
                  entryExists(self, category, title)
                      Returns True, if an entry exists in the database.
                      category: The name string of the category.
                      title: The title string of the entry.
-                 findEntries(self, pattern, useRegexp=False, search=True, inCategory=None,
-                 matchCategory=False, matchTitle=False, matchUser=False, matchPw=False, matchBulk=False,
-                 matchAttrName=False, matchAttrData=False)
+                 findEntries(self, pattern, useRegexp=False, search=True, inCategory=None, matchCategory=False,
+                 matchTitle=False, matchUser=False, matchPw=False, matchBulk=False, matchAttrName=False,
+                 matchAttrData=False)
                      Search the database for entries that match a pattern.
                      useRegexp: If True, then the pattern is a regular expression string.
                                 If False, then the pattern is a SQL LIKE pattern string.
                      inCategory: If specified as non-zero length string, then only search
                                  the category with this name.
                      matchCategory: Match the pattern to the category name string of an entry.
                      matchTitle: Match the pattern to the title string of an entry.
@@ -166,62 +166,66 @@
                      Returns a PWManEntryBulk() instance or None, if there is no bulk data.
                  getEntryTitles(self, category)
                      Get all titles from one category in the database.
                      category: The category name string.
                      Returns a sorted list of strings.
                  getEntryTotp(self, entry)
                      Get the TOTP parameters associated with an entry.
-                  entry: The PWManEntry() to get the TOTP parameters for.
+                     entry: The PWManEntry() to get the TOTP parameters for.
                      Returns a PWManEntryTOTP() instance, or None if there is no TOTP data.
-                getGlobalAttr(self, name)
+              getGlobalAttr(self, name)
                      Get a global attribute.
-                     A global attribute is not associated with an entry.
+                    A global attribute is not associated with an entry.
                      Returns None, if the attribute does not exist.
                  getOnDiskDb(self)
                      Get a read-only instance of PWManDatabase that contains
                      the current on-disk data. The on-disk data is the data
                      at the last commit.
                  importSqlScript(self, *args, **kwargs)
                      Imports a plain text dump into the database.
                      script: The script string to import.
                      clear: If True, drop all tables from the database before importing.
                  isDirty(self)
                      Returns True, if the database contains uncommitted data.
-                 moveEntries(self, fromCategory, toCategory)
-                     Move all entries from one category to another category.
+                 moveEntries(self, fromCategory, toCategory, toDb=None, copy=False)
+                     Move or copy all entries from one category to another category.
                      fromCategory: The category to move all entries from.
                      toCategory: The (new) category to move all entries to.
-                 moveEntry(self, entry, newCategory, newTitle)
-                     Move an existing entry to a new category and/or set a new entry title.
-                     entry: The PWManEntry() instance to move.
-                     newCategory: The new category name string.
-                     newTitle: The new title string.
+                     toDb: The target database. Defaults to self.
+                     copy: If False, then move. If True, then copy.
+                 moveEntry(self, entry, newCategory, newTitle, toDb=None, copy=False)
+                     Move or copy an existing entry to a new category and/or set a new entry title.
+                     entry: The PWManEntry() instance to move/copy.
+                     newCategory: The target category name string.
+                     newTitle: The target title string.
+                     toDb: The target database. Defaults to self.
+                     copy: If False, then move. If True, then copy.
                  setEntryAttr(self, entryAttr)
                      Set an attribute associated with an entry.
                      entryAttr: The new PWManEntryAttr() instance to write to the database.
                                 If entryAttr.data is None, then the attribute is deleted.
                  setEntryBulk(self, entryBulk)
                      Set the bulk data associated with an entry.
                      entryBulk: The new PWManEntryBulk() instance to write to the database.
                                 If entryBulk.data is None, then the bulk data is deleted.
                  setEntryTotp(self, entryTotp)
                      Set the TOTP data associated with an entry.
                      entryTotp: The new PWManEntryTOTP() instance to write to the database.
                                 If entryTotp.key is None, then the TOTP data is deleted.
                  setGlobalAttr(self, name, data, setDirty=True)
-                     Set a global attribute.
+   �             Set a global attribute.
                      A global attribute is not associated with an entry.
                      If data is None or empty, the attribute is deleted from the database.
                  setPassphrase(self, passphrase)
                      Set a new passphrase string for encryption and decryption.
-   �       ==============================================================================================
+               ===================================================================================================
                Data and other attributes defined here:
                  DB_TYPE = 'PWMan database'
                  DB_VER = ('0', '1')
-               ==============================================================================================
+               ===================================================================================================
                Methods inherited from libpwman.cryptsql.CryptSQL:
                  close(self)
                      Close the currently opened database.
                      This does not commit. All uncommitted changes are lost.
                  dropAllTables(self)
                      Drop all tables from the database.
                  getFilename(self)
@@ -255,15 +259,15 @@
                  sqlPlainDump(self)
                      Get a plain text dump of the database.
                      Returns a string.
                  sqlVacuum(self)
                      Run the SQL VACUUM statement.
                      This also commits all changes to the SQL database,
                      but not to the database file.
-               ==============================================================================================
+               ===================================================================================================
                Data descriptors inherited from libpwman.cryptsql.CryptSQL:
                  __dict__
                      dictionary for instance variables (if defined)
                  __weakref__
                      list of weak references to the object (if defined)
           
          class PWManEntry(builtins.object)
@@ -274,69 +278,64 @@
                Methods defined here:
                  __eq__(self, other)
                      Return self==value.
                  __init__(self, category: str, title: str, user: str = None, pw: str = None, entryId: int = None) -> None
                      Initialize self.  See help(type(self)) for accurate signature.
                  __repr__(self)
                      Return repr(self).
-               ===========================================================================================================
+               =====================================================================================================================
                Data descriptors defined here:
                  __dict__
                      dictionary for instance variables (if defined)
                  __weakref__
                   list of weak references to the object (if defined)
-               ===========================================================================================================
+               =====================================================================================================================
               Data and other attributes defined here:
-                 __annotations__ = {'category': <class 'str'>, 'entryId': <class 'int'>, 'pw': <class 'str'>, 'title':
-                 <class 'str'>, 'user': <class 'str'>}
+                 __annotations__ = {'category': <class 'str'>, 'entryId': <class 'int'>, 'pw': <class 'str'>, 'title': <class
+                 'str'>, 'user': <class 'str'>}
                  __dataclass_fields__ = {'category': Field(name='category',type=<class 'str'>,default...appingproxy(
-                 {}),kw_only=False,_field_type=_FIELD), 'entryId': Field(name='entryId',type=<class
-                 'int'>,default=...appingproxy({}),kw_only=False,_field_type=_FIELD), 'pw': Field(name='pw',type=<class
-                 'str'>,default=None,...appingproxy({}),kw_only=False,_field_type=_FIELD), 'title': Field
-                 (name='title',type=<class 'str'>,default=<d...appingproxy({}),kw_only=False,_field_type=_FIELD), 'user':
-                 Field(name='user',type=<class 'str'>,default=Non...appingproxy({}),kw_only=False,_field_type=_FIELD)}
-                 __dataclass_params__ = _DataclassParams
-                 (init=True,repr=True,eq=True,order=False,unsafe_hash=False,frozen=False)
+                 {}),kw_only=False,_field_type=_FIELD), 'entryId': Field(name='entryId',type=<class 'int'>,default=...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD), 'pw': Field(name='pw',type=<class 'str'>,default=None,...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD), 'title': Field(name='title',type=<class 'str'>,default=<d...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD), 'user': Field(name='user',type=<class 'str'>,default=Non...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD)}
+                 __dataclass_params__ = _DataclassParams(init=True,repr=True,eq=True,order=False,unsafe_hash=False,frozen=False)
                  __hash__ = None
                  __match_args__ = ('category', 'title', 'user', 'pw', 'entryId')
                  entryId = None
                  pw = None
                  user = None
           
          class PWManEntryAttr(builtins.object)
-             PWManEntryAttr(name: str, data: str = None, entry: database.PWManEntry = None, attrId:
-              int = None) -&gt; None
+             PWManEntryAttr(name: str, data: str = None, entry: database.PWManEntry = None, attrId: int = None) -&gt; None
               
              Entry attribute data structure.
               
                Methods defined here:
                  __eq__(self, other)
                      Return self==value.
-                 __init__(self, name: str, data: str = None, entry: database.PWManEntry = None, attrId: int =
-                 None) -> None
+                 __init__(self, name: str, data: str = None, entry: database.PWManEntry = None, attrId: int = None) -> None
                      Initialize self.  See help(type(self)) for accurate signature.
                  __repr__(self)
                      Return repr(self).
-               ==============================================================================================
+               ===============================================================================================================
                Data descriptors defined here:
                  __dict__
                      dictionary for instance variables (if defined)
                  __weakref__
                   list of weak references to the object (if defined)
-               ==============================================================================================
+               ===============================================================================================================
               Data and other attributes defined here:
-                 __annotations__ = {'attrId': <class 'int'>, 'data': <class 'str'>, 'entry': <class
-                 'database.PWManEntry'>, 'name': <class 'str'>}
-                 __dataclass_fields__ = {'attrId': Field(name='attrId',type=<class
-                 'int'>,default=N...appingproxy({}),kw_only=False,_field_type=_FIELD), 'data': Field
-                 (name='data',type=<class 'str'>,default=Non...appingproxy(
-                 {}),kw_only=False,_field_type=_FIELD), 'entry': Field(name='entry',type=<class
-                 'database.PWManEn...appingproxy({}),kw_only=False,_field_type=_FIELD), 'name': Field
-                 (name='name',type=<class 'str'>,default=<da...appingproxy(
-                 {}),kw_only=False,_field_type=_FIELD)}
+                 __annotations__ = {'attrId': <class 'int'>, 'data': <class 'str'>, 'entry': <class 'database.PWManEntry'>,
+                 'name': <class 'str'>}
+                 __dataclass_fields__ = {'attrId': Field(name='attrId',type=<class 'int'>,default=N...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD), 'data': Field(name='data',type=<class 'str'>,default=Non...appingproxy
+                 ({}),kw_only=False,_field_type=_FIELD), 'entry': Field(name='entry',type=<class
+                 'database.PWManEn...appingproxy({}),kw_only=False,_field_type=_FIELD), 'name': Field(name='name',type=<class
+                 'str'>,default=<da...appingproxy({}),kw_only=False,_field_type=_FIELD)}
                  __dataclass_params__ = _DataclassParams
                  (init=True,repr=True,eq=True,order=False,unsafe_hash=False,frozen=False)
                  __hash__ = None
                  __match_args__ = ('name', 'data', 'entry', 'attrId')
                  attrId = None
                  data = None
                  entry = None
@@ -379,35 +378,34 @@
               database.PWManEntry = None, totpId: int = None) -&gt; None
               
              Entry TOTP-data data structure.
               
                Methods defined here:
                  __eq__(self, other)
                      Return self==value.
-                 __init__(self, key: str, digits: int = 6, hmacHash: str = 'SHA1', entry: database.PWManEntry
-                 = None, totpId: int = None) -> None
+                 __init__(self, key: str, digits: int = 6, hmacHash: str = 'SHA1', entry: database.PWManEntry =
+                 None, totpId: int = None) -> None
                      Initialize self.  See help(type(self)) for accurate signature.
                  __repr__(self)
                      Return repr(self).
-               ==============================================================================================
+               ===================================================================================================
                Data descriptors defined here:
                  __dict__
                      dictionary for instance variables (if defined)
                  __weakref__
-                     list of weak references to the object (if defined)
-            ==============================================================================================
+                  list of weak references to the object (if defined)
+               ===================================================================================================
                Data and other attributes defined here:
-                __annotations__ = {'digits': <class 'int'>, 'entry': <class 'database.PWManEntry'>,
-                 'hmacHash': <class 'str'>, 'key': <class 'str'>, 'totpId': <class 'int'>}
-                 __dataclass_fields__ = {'digits': Field(name='digits',type=<class
-                 'int'>,default=6...appingproxy({}),kw_only=False,_field_type=_FIELD), 'entry': Field
-                 (name='entry',type=<class 'database.PWManEn...appingproxy(
-                 {}),kw_only=False,_field_type=_FIELD), 'hmacHash': Field(name='hmacHash',type=<class
-                 'str'>,default...appingproxy({}),kw_only=False,_field_type=_FIELD), 'key': Field
-                 (name='key',type=<class 'str'>,default=<dat...appingproxy(
+                __annotations__ = {'digits': <class 'int'>, 'entry': <class 'database.PWManEntry'>, 'hmacHash':
+                 <class 'str'>, 'key': <class 'str'>, 'totpId': <class 'int'>}
+                 __dataclass_fields__ = {'digits': Field(name='digits',type=<class 'int'>,default=6...appingproxy(
+                 {}),kw_only=False,_field_type=_FIELD), 'entry': Field(name='entry',type=<class
+                 'database.PWManEn...appingproxy({}),kw_only=False,_field_type=_FIELD), 'hmacHash': Field
+                 (name='hmacHash',type=<class 'str'>,default...appingproxy({}),kw_only=False,_field_type=_FIELD),
+                 'key': Field(name='key',type=<class 'str'>,default=<dat...appingproxy(
                  {}),kw_only=False,_field_type=_FIELD), 'totpId': Field(name='totpId',type=<class
                  'int'>,default=N...appingproxy({}),kw_only=False,_field_type=_FIELD)}
                  __dataclass_params__ = _DataclassParams
                  (init=True,repr=True,eq=True,order=False,unsafe_hash=False,frozen=False)
                  __hash__ = None
                  __match_args__ = ('key', 'digits', 'hmacHash', 'entry', 'totpId')
                  digits = 6
```

### Comparing `pwman-python-2.8/doc/api/libpwman/dbdiff.html` & `pwman-python-2.9/doc/api/libpwman/dbdiff.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module dbdiff</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">dbdiff</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/dbdiff.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/dbdiff.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/dbdiff.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/dbdiff.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
       index
-dbdiff /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+dbdiff /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
        dbdiff.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � difflib
```

### Comparing `pwman-python-2.8/doc/api/libpwman/exception.html` & `pwman-python-2.9/doc/api/libpwman/exception.html`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module exception</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">exception</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/exception.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/exception.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/exception.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/exception.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor index-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Classes</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
          index
-exception /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+exception /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
           exception.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Classes
            builtins.Exception(builtins.BaseException)
```

### Comparing `pwman-python-2.8/doc/api/libpwman/fileobj.html` & `pwman-python-2.9/doc/api/libpwman/fileobj.html`

 * *Files 5% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module fileobj</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">fileobj</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/fileobj.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/fileobj.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/fileobj.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/fileobj.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;<a href="builtins.html#object">object</a>&nbsp;file&nbsp;format.<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
@@ -55,63 +55,45 @@
 name:&nbsp;The&nbsp;<a href="builtins.html#object">object</a>&nbsp;name.&nbsp;Must&nbsp;be&nbsp;bytes-like.<br>
 data:&nbsp;The&nbsp;<a href="builtins.html#object">object</a>&nbsp;payload.&nbsp;Must&nbsp;be&nbsp;bytes-like.</span></dd></dl>
 
 <dl><dt><a name="FileObj-getData"><strong>getData</strong></a>(self)</dt></dl>
 
 <dl><dt><a name="FileObj-getName"><strong>getName</strong></a>(self)</dt></dl>
 
-<dl><dt><a name="FileObj-getRaw"><strong>getRaw</strong></a>(self)</dt></dl>
+<dl><dt><a name="FileObj-getRaw"><strong>getRaw</strong></a>(self, buffer)</dt></dl>
 
 <hr>
 Class methods defined here:<br>
 <dl><dt><a name="FileObj-parseRaw"><strong>parseRaw</strong></a>(raw)<span class="grey"><span class="heading-text"> from <a href="builtins.html#type">builtins.type</a></span></span></dt></dl>
 
-<hr>
-Data descriptors defined here:<br>
-<dl><dt><strong>__dict__</strong></dt>
-<dd><span class="code">dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</span></dd>
-</dl>
-<dl><dt><strong>__weakref__</strong></dt>
-<dd><span class="code">list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</span></dd>
-</dl>
 </td></tr></table> <p>
 <table class="section">
 <tr class="decor title-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><a name="FileObjCollection">class <strong>FileObjCollection</strong></a>(<a href="builtins.html#object">builtins.object</a>)</td></tr>
     
 <tr><td class="decor title-decor" rowspan=2><span class="code">&nbsp;&nbsp;&nbsp;</span></td>
-<td class="decor title-decor" colspan=2><span class="code"><a href="#FileObjCollection">FileObjCollection</a>(*objects)<br>
+<td class="decor title-decor" colspan=2><span class="code"><a href="#FileObjCollection">FileObjCollection</a>(objects)<br>
 &nbsp;<br>
 <br>&nbsp;</span></td></tr>
 <tr><td>&nbsp;</td>
 <td class="singlecolumn">Methods defined here:<br>
-<dl><dt><a name="FileObjCollection-__init__"><strong>__init__</strong></a>(self, *objects)</dt><dd><span class="code">Initialize&nbsp;self.&nbsp;&nbsp;See&nbsp;help(type(self))&nbsp;for&nbsp;accurate&nbsp;signature.</span></dd></dl>
-
-<dl><dt><a name="FileObjCollection-get"><strong>get</strong></a>(self, name)</dt></dl>
+<dl><dt><a name="FileObjCollection-__init__"><strong>__init__</strong></a>(self, objects)</dt><dd><span class="code">Initialize&nbsp;self.&nbsp;&nbsp;See&nbsp;help(type(self))&nbsp;for&nbsp;accurate&nbsp;signature.</span></dd></dl>
 
-<dl><dt><a name="FileObjCollection-getOne"><strong>getOne</strong></a>(self, name, errorMsg=None, default=None)</dt></dl>
+<dl><dt><a name="FileObjCollection-get"><strong>get</strong></a>(self, name, errorMsg=None, default=None)</dt></dl>
 
 <dl><dt><a name="FileObjCollection-getRaw"><strong>getRaw</strong></a>(self)</dt></dl>
 
 <dl><dt><a name="FileObjCollection-writeFile"><strong>writeFile</strong></a>(self, filepath)</dt></dl>
 
 <hr>
 Class methods defined here:<br>
 <dl><dt><a name="FileObjCollection-parseFile"><strong>parseFile</strong></a>(filepath)<span class="grey"><span class="heading-text"> from <a href="builtins.html#type">builtins.type</a></span></span></dt></dl>
 
 <dl><dt><a name="FileObjCollection-parseRaw"><strong>parseRaw</strong></a>(raw)<span class="grey"><span class="heading-text"> from <a href="builtins.html#type">builtins.type</a></span></span></dt></dl>
 
-<hr>
-Data descriptors defined here:<br>
-<dl><dt><strong>__dict__</strong></dt>
-<dd><span class="code">dictionary&nbsp;for&nbsp;instance&nbsp;variables&nbsp;(if&nbsp;defined)</span></dd>
-</dl>
-<dl><dt><strong>__weakref__</strong></dt>
-<dd><span class="code">list&nbsp;of&nbsp;weak&nbsp;references&nbsp;to&nbsp;the&nbsp;object&nbsp;(if&nbsp;defined)</span></dd>
-</dl>
 </td></tr></table> <p>
 <table class="section">
 <tr class="decor title-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><a name="FileObjError">class <strong>FileObjError</strong></a>(<a href="builtins.html#Exception">builtins.Exception</a>)</td></tr>
     
 <tr><td class="decor title-decor"><span class="code">&nbsp;&nbsp;&nbsp;</span></td><td>&nbsp;</td>
 <td class="singlecolumn"><dl><dt>Method resolution order:</dt>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
        index
-fileobj /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+fileobj /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
         fileobj.py
 # Simple object file format.
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � errno
@@ -19,57 +19,44 @@
              FileObj(name, data)
               
 
               
                Methods defined here:
                  __init__(self, name, data)
                      Construct FileObj().
-                     name: The object name. Must be bytes-like.
+                  name: The object name. Must be bytes-like.
                      data: The object payload. Must be bytes-like.
-                 getData(self)
-              getName(self)
-                 getRaw(self)
-              ===========================================================================
+                getData(self)
+                 getName(self)
+                 getRaw(self, buffer)
+               ===========================================================================
                Class methods defined here:
                  parseRaw(raw) from builtins.type
-               ===========================================================================
-               Data descriptors defined here:
-                 __dict__
-                     dictionary for instance variables (if defined)
-                 __weakref__
-                     list of weak references to the object (if defined)
           
          class FileObjCollection(builtins.object)
-             FileObjCollection(*objects)
+             FileObjCollection(objects)
               
 
               
                Methods defined here:
-                 __init__(self, *objects)
-                     Initialize self.  See help(type(self)) for accurate signature.
-                 get(self, name)
-                 getOne(self, name, errorMsg=None, default=None)
-                 getRaw(self)
-              writeFile(self, filepath)
+                 __init__(self, objects)
+                  Initialize self.  See help(type(self)) for accurate signature.
+                 get(self, name, errorMsg=None, default=None)
+                getRaw(self)
+                 writeFile(self, filepath)
                ===========================================================================
-              Class methods defined here:
+               Class methods defined here:
                  parseFile(filepath) from builtins.type
                  parseRaw(raw) from builtins.type
-               ===========================================================================
-               Data descriptors defined here:
-                 __dict__
-                     dictionary for instance variables (if defined)
-                 __weakref__
-   �             list of weak references to the object (if defined)
           
          class FileObjError(builtins.Exception)
                  Method resolution order:
                      FileObjError
                      builtins.Exception
-                     builtins.BaseException
+   �             builtins.BaseException
                      builtins.object
                ========================================================================================
                Data descriptors defined here:
                  __weakref__
                      list of weak references to the object (if defined)
                ========================================================================================
                Methods inherited from builtins.Exception:
```

### Comparing `pwman-python-2.8/doc/api/libpwman/mlock.html` & `pwman-python-2.9/doc/api/libpwman/mlock.html`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module mlock</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">mlock</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/mlock.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/mlock.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/mlock.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/mlock.py</a></td></tr></table>
     <p><span class="code">#&nbsp;mlock&nbsp;support<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2019-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
      index
-mlock /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/mlock.py
+mlock /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/mlock.py
 # mlock support
 # Copyright (c) 2019-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � os platform sys
```

### Comparing `pwman-python-2.8/doc/api/libpwman/otp.html` & `pwman-python-2.9/doc/api/libpwman/otp.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module otp</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">otp</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/otp.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/otp.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/otp.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/otp.py</a></td></tr></table>
     <p><span class="code">#&nbsp;HOTP/TOTP&nbsp;support<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2019-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
    index
-otp /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/otp.py
+otp /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/otp.py
 # HOTP/TOTP support
 # Copyright (c) 2019-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � binascii hashlib hmac time
```

### Comparing `pwman-python-2.8/doc/api/libpwman/ui.html` & `pwman-python-2.9/doc/api/libpwman/ui.html`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module ui</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">ui</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/ui.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/ui.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/ui.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/ui.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
@@ -79,17 +79,17 @@
 
 <dl><dt><a name="__classcell__-complete_cat"><strong>complete_cat</strong></a> = __complete_category_title_item(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_close"><strong>complete_close</strong></a>(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_commit"><strong>complete_commit</strong></a>(self, text, line, begidx, endidx)</dt></dl>
 
-<dl><dt><a name="__classcell__-complete_copy"><strong>complete_copy</strong></a> = <a href="#__classcell__-complete_move">complete_move</a>(self, text, line, begidx, endidx)</dt></dl>
+<dl><dt><a name="__classcell__-complete_copy"><strong>complete_copy</strong></a> = __complete_move_copy(self, text, line, begidx, endidx)</dt></dl>
 
-<dl><dt><a name="__classcell__-complete_cp"><strong>complete_cp</strong></a> = <a href="#__classcell__-complete_move">complete_move</a>(self, text, line, begidx, endidx)</dt></dl>
+<dl><dt><a name="__classcell__-complete_cp"><strong>complete_cp</strong></a> = __complete_move_copy(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_database"><strong>complete_database</strong></a>(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_db"><strong>complete_db</strong></a> = <a href="#__classcell__-complete_database">complete_database</a>(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_dbdump"><strong>complete_dbdump</strong></a>(self, text, line, begidx, endidx)</dt></dl>
 
@@ -123,25 +123,25 @@
 
 <dl><dt><a name="__classcell__-complete_find"><strong>complete_find</strong></a>(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_list"><strong>complete_list</strong></a> = __complete_category_title_item(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_ls"><strong>complete_ls</strong></a> = __complete_category_title_item(self, text, line, begidx, endidx)</dt></dl>
 
-<dl><dt><a name="__classcell__-complete_move"><strong>complete_move</strong></a>(self, text, line, begidx, endidx)</dt></dl>
+<dl><dt><a name="__classcell__-complete_move"><strong>complete_move</strong></a> = __complete_move_copy(self, text, line, begidx, endidx)</dt></dl>
 
-<dl><dt><a name="__classcell__-complete_mv"><strong>complete_mv</strong></a> = <a href="#__classcell__-complete_move">complete_move</a>(self, text, line, begidx, endidx)</dt></dl>
+<dl><dt><a name="__classcell__-complete_mv"><strong>complete_mv</strong></a> = __complete_move_copy(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_n"><strong>complete_n</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_new"><strong>complete_new</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_remove"><strong>complete_remove</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
 
-<dl><dt><a name="__classcell__-complete_rename"><strong>complete_rename</strong></a> = <a href="#__classcell__-complete_move">complete_move</a>(self, text, line, begidx, endidx)</dt></dl>
+<dl><dt><a name="__classcell__-complete_rename"><strong>complete_rename</strong></a> = __complete_move_copy(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_rm"><strong>complete_rm</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_t"><strong>complete_t</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
 
 <dl><dt><a name="__classcell__-complete_totp"><strong>complete_totp</strong></a> = __complete_category_title(self, text, line, begidx, endidx)</dt></dl>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
   index
-ui /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/ui.py
+ui /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/ui.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
          functools re       sys
    � os        readline time
@@ -36,16 +36,16 @@
                      specify alternate input and output file objects; if not specified,
                      sys.stdin and sys.stdout are used.
                  complete_add = __complete_category_title(self, text, line, begidx, endidx)
                  complete_c = complete_commit(self, text, line, begidx, endidx)
                  complete_cat = __complete_category_title_item(self, text, line, begidx, endidx)
                  complete_close(self, text, line, begidx, endidx)
                  complete_commit(self, text, line, begidx, endidx)
-                 complete_copy = complete_move(self, text, line, begidx, endidx)
-                 complete_cp = complete_move(self, text, line, begidx, endidx)
+                 complete_copy = __complete_move_copy(self, text, line, begidx, endidx)
+                 complete_cp = __complete_move_copy(self, text, line, begidx, endidx)
                  complete_database(self, text, line, begidx, endidx)
                  complete_db = complete_database(self, text, line, begidx, endidx)
                  complete_dbdump(self, text, line, begidx, endidx)
                  complete_dbimport(self, text, line, begidx, endidx)
                  complete_del = __complete_category_title(self, text, line, begidx, endidx)
                  complete_diff(self, text, line, begidx, endidx)
                  complete_ea = complete_edit_attr(self, text, line, begidx, endidx)
@@ -58,20 +58,20 @@
                  complete_ep = complete_edit_pw(self, text, line, begidx, endidx)
                  complete_et = complete_edit_totp(self, text, line, begidx, endidx)
                  complete_eu = complete_edit_user(self, text, line, begidx, endidx)
                  complete_f = complete_find(self, text, line, begidx, endidx)
                  complete_find(self, text, line, begidx, endidx)
                  complete_list = __complete_category_title_item(self, text, line, begidx, endidx)
                  complete_ls = __complete_category_title_item(self, text, line, begidx, endidx)
-                 complete_move(self, text, line, begidx, endidx)
-                 complete_mv = complete_move(self, text, line, begidx, endidx)
+                 complete_move = __complete_move_copy(self, text, line, begidx, endidx)
+                 complete_mv = __complete_move_copy(self, text, line, begidx, endidx)
                  complete_n = __complete_category_title(self, text, line, begidx, endidx)
                  complete_new = __complete_category_title(self, text, line, begidx, endidx)
                  complete_remove = __complete_category_title(self, text, line, begidx, endidx)
-                 complete_rename = complete_move(self, text, line, begidx, endidx)
+                 complete_rename = __complete_move_copy(self, text, line, begidx, endidx)
                  complete_rm = __complete_category_title(self, text, line, begidx, endidx)
                  complete_t = __complete_category_title(self, text, line, begidx, endidx)
                  complete_totp = __complete_category_title(self, text, line, begidx, endidx)
                  complete_w = complete_commit(self, text, line, begidx, endidx)
                  default(self, line)
                      Called on an input line when the command prefix is not recognized.
```

### Comparing `pwman-python-2.8/doc/api/libpwman/ui_escape.html` & `pwman-python-2.9/doc/api/libpwman/ui_escape.html`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module ui_escape</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">ui_escape</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/ui_escape.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/ui_escape.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/ui_escape.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/ui_escape.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor index-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Classes</strong></td></tr>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
          index
-ui_escape /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+ui_escape /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
           ui_escape.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Classes
            builtins.Exception(builtins.BaseException)
```

### Comparing `pwman-python-2.8/doc/api/libpwman/util.html` & `pwman-python-2.9/doc/api/libpwman/util.html`

 * *Files 3% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 <meta charset="utf-8">
 <title>Python: module util</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">util</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/util.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/util.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/util.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/util.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor pkg-content-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Modules</strong></td></tr>
@@ -28,18 +28,17 @@
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Functions</strong></td></tr>
     
 <tr><td class="decor functions-decor"><span class="code">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span></td><td>&nbsp;</td>
 <td class="singlecolumn"><dl><dt><a name="-clearScreen"><strong>clearScreen</strong></a>()</dt></dl>
  <dl><dt><a name="-readPassphrase"><strong>readPassphrase</strong></a>(prompt, verify=False)</dt></dl>
  <dl><dt><a name="-stdout"><strong>stdout</strong></a>(text, flush=True)</dt></dl>
  <dl><dt><a name="-str2bool"><strong>str2bool</strong></a>(string, default=False)</dt></dl>
- <dl><dt><a name="-uniq"><strong>uniq</strong></a>(l, sort=True)</dt></dl>
 </td></tr></table><p>
 <table class="section">
 <tr class="decor data-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Data</strong></td></tr>
     
 <tr><td class="decor data-decor"><span class="code">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span></td><td>&nbsp;</td>
-<td class="singlecolumn"><strong>__all__</strong> = ['str2bool', 'osIsWindows', 'osIsPosix', 'uniq', 'stdout', 'clearScreen', 'readPassphrase']<br>
+<td class="singlecolumn"><strong>__all__</strong> = ['str2bool', 'osIsWindows', 'osIsPosix', 'stdout', 'clearScreen', 'readPassphrase']<br>
 <strong>osIsPosix</strong> = True<br>
 <strong>osIsWindows</strong> = False</td></tr></table>
 </body></html>
```

#### html2text {}

```diff
@@ -1,21 +1,20 @@
     index
-util /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/util.py
+util /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/util.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Modules
    � curses getpass os sys
  
 Functions
            clearScreen()
-           readPassphrase(prompt, verify=False)
-   �   stdout(text, flush=True)
+   �   readPassphrase(prompt, verify=False)
+           stdout(text, flush=True)
            str2bool(string, default=False)
-           uniq(l, sort=True)
  
 Data
-         __all__ = ['str2bool', 'osIsWindows', 'osIsPosix', 'uniq', 'stdout',
+         __all__ = ['str2bool', 'osIsWindows', 'osIsPosix', 'stdout',
    � 'clearScreen', 'readPassphrase']
          osIsPosix = True
          osIsWindows = False
```

### Comparing `pwman-python-2.8/doc/api/libpwman/version.html` & `pwman-python-2.9/doc/api/libpwman/version.html`

 * *Files 7% similar despite different names*

```diff
@@ -4,23 +4,23 @@
 <meta charset="utf-8">
 <title>Python: module version</title>
 </head><body>
 
 <table class="heading">
 <tr class="heading-text decor">
 <td class="title">&nbsp;<br><strong class="title">version</strong></td>
-<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/version.py">/tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/version.py</a></td></tr></table>
+<td class="extra"><a href=".">index</a><br><a href="file:/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/version.py">/tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/version.py</a></td></tr></table>
     <p><span class="code">#&nbsp;Simple&nbsp;password&nbsp;manager<br>
 #&nbsp;Copyright&nbsp;(c)&nbsp;2011-2023&nbsp;Michael&nbsp;Büsch&nbsp;&lt;m@bues.ch&gt;<br>
 #&nbsp;Licensed&nbsp;under&nbsp;the&nbsp;GNU/GPL&nbsp;version&nbsp;2&nbsp;or&nbsp;later.</span></p>
 <p>
 <table class="section">
 <tr class="decor data-decor heading-text">
 <td class="section-title" colspan=3>&nbsp;<br><strong class="bigsection">Data</strong></td></tr>
     
 <tr><td class="decor data-decor"><span class="code">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span></td><td>&nbsp;</td>
 <td class="singlecolumn"><strong>VERSION_EXTRA</strong> = ''<br>
 <strong>VERSION_MAJOR</strong> = 2<br>
-<strong>VERSION_MINOR</strong> = 8<br>
-<strong>VERSION_STRING</strong> = '2.8'<br>
+<strong>VERSION_MINOR</strong> = 9<br>
+<strong>VERSION_STRING</strong> = '2.9'<br>
 <strong>__all__</strong> = ['VERSION_MAJOR', 'VERSION_MINOR', 'VERSION_EXTRA', 'VERSION_STRING']</td></tr></table>
 </body></html>
```

#### html2text {}

```diff
@@ -1,14 +1,14 @@
        index
-version /tmp/makerelease-pwman-python.NVQhFLFA/pwman-python-2.8/libpwman/
+version /tmp/makerelease-pwman-python.bxOnk765/pwman-python-2.9/libpwman/
         version.py
 # Simple password manager
 # Copyright (c) 2011-2023 Michael BÃ¼sch <m@bues.ch>
 # Licensed under the GNU/GPL version 2 or later.
  
 Data
          VERSION_EXTRA = ''
          VERSION_MAJOR = 2
-   � VERSION_MINOR = 8
-         VERSION_STRING = '2.8'
+   � VERSION_MINOR = 9
+         VERSION_STRING = '2.9'
          __all__ = ['VERSION_MAJOR', 'VERSION_MINOR', 'VERSION_EXTRA',
          'VERSION_STRING']
```

### Comparing `pwman-python-2.8/doc/foreign-licenses/PYTHON-LICENSE.txt` & `pwman-python-2.9/doc/foreign-licenses/PYTHON-LICENSE.txt`

 * *Files 4% similar despite different names*

```diff
@@ -1,29 +1,29 @@
 A. HISTORY OF THE SOFTWARE
 ==========================
 
 Python was created in the early 1990s by Guido van Rossum at Stichting
-Mathematisch Centrum (CWI, see http://www.cwi.nl) in the Netherlands
+Mathematisch Centrum (CWI, see https://www.cwi.nl) in the Netherlands
 as a successor of a language called ABC.  Guido remains Python's
 principal author, although it includes many contributions from others.
 
 In 1995, Guido continued his work on Python at the Corporation for
-National Research Initiatives (CNRI, see http://www.cnri.reston.va.us)
+National Research Initiatives (CNRI, see https://www.cnri.reston.va.us)
 in Reston, Virginia where he released several versions of the
 software.
 
 In May 2000, Guido and the Python core development team moved to
 BeOpen.com to form the BeOpen PythonLabs team.  In October of the same
 year, the PythonLabs team moved to Digital Creations, which became
 Zope Corporation.  In 2001, the Python Software Foundation (PSF, see
 https://www.python.org/psf/) was formed, a non-profit organization
 created specifically to own Python-related Intellectual Property.
 Zope Corporation was a sponsoring member of the PSF.
 
-All Python releases are Open Source (see http://www.opensource.org for
+All Python releases are Open Source (see https://opensource.org for
 the Open Source Definition).  Historically, most, but not all, Python
 releases have also been GPL-compatible; the table below summarizes
 the various releases.
 
     Release         Derived     Year        Owner       GPL-
                     from                                compatible? (1)
 
@@ -55,29 +55,40 @@
 Thanks to the many outside volunteers who have worked under Guido's
 direction to make these releases possible.
 
 
 B. TERMS AND CONDITIONS FOR ACCESSING OR OTHERWISE USING PYTHON
 ===============================================================
 
+Python software and documentation are licensed under the
+Python Software Foundation License Version 2.
+
+Starting with Python 3.8.6, examples, recipes, and other code in
+the documentation are dual licensed under the PSF License Version 2
+and the Zero-Clause BSD license.
+
+Some software incorporated into Python is under different licenses.
+The licenses are listed with code falling under that license.
+
+
 PYTHON SOFTWARE FOUNDATION LICENSE VERSION 2
 --------------------------------------------
 
 1. This LICENSE AGREEMENT is between the Python Software Foundation
 ("PSF"), and the Individual or Organization ("Licensee") accessing and
 otherwise using this software ("Python") in source or binary form and
 its associated documentation.
 
 2. Subject to the terms and conditions of this License Agreement, PSF hereby
 grants Licensee a nonexclusive, royalty-free, world-wide license to reproduce,
 analyze, test, perform and/or display publicly, prepare derivative works,
 distribute, and otherwise use Python alone or in any derivative version,
 provided, however, that PSF's License Agreement and PSF's notice of copyright,
 i.e., "Copyright (c) 2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009, 2010,
-2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019 Python Software Foundation;
+2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023 Python Software Foundation;
 All Rights Reserved" are retained in Python alone or in any derivative version
 prepared by Licensee.
 
 3. In the event Licensee prepares a derivative work that is based on
 or incorporates Python or any part thereof, and wants to make
 the derivative work available to others as provided herein, then
 Licensee hereby agrees to include in any such work a brief summary of
@@ -176,17 +187,17 @@
 License Agreement and CNRI's notice of copyright, i.e., "Copyright (c)
 1995-2001 Corporation for National Research Initiatives; All Rights
 Reserved" are retained in Python 1.6.1 alone or in any derivative
 version prepared by Licensee.  Alternately, in lieu of CNRI's License
 Agreement, Licensee may substitute the following text (omitting the
 quotes): "Python 1.6.1 is made available subject to the terms and
 conditions in CNRI's License Agreement.  This Agreement together with
-Python 1.6.1 may be located on the Internet using the following
+Python 1.6.1 may be located on the internet using the following
 unique, persistent identifier (known as a handle): 1895.22/1013.  This
-Agreement may also be obtained from a proxy server on the Internet
+Agreement may also be obtained from a proxy server on the internet
 using the following URL: http://hdl.handle.net/1895.22/1013".
 
 3. In the event Licensee prepares a derivative work that is based on
 or incorporates Python 1.6.1 or any part thereof, and wants to make
 the derivative work available to others as provided herein, then
 Licensee hereby agrees to include in any such work a brief summary of
 the changes made to Python 1.6.1.
@@ -248,7 +259,21 @@
 STICHTING MATHEMATISCH CENTRUM DISCLAIMS ALL WARRANTIES WITH REGARD TO
 THIS SOFTWARE, INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
 FITNESS, IN NO EVENT SHALL STICHTING MATHEMATISCH CENTRUM BE LIABLE
 FOR ANY SPECIAL, INDIRECT OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
 WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
 ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT
 OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
+
+ZERO-CLAUSE BSD LICENSE FOR CODE IN THE PYTHON DOCUMENTATION
+----------------------------------------------------------------------
+
+Permission to use, copy, modify, and/or distribute this software for any
+purpose with or without fee is hereby granted.
+
+THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
+REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY
+AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
+INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM
+LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR
+OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
+PERFORMANCE OF THIS SOFTWARE.
```

### Comparing `pwman-python-2.8/examplescript.py` & `pwman-python-2.9/examplescript.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/install_to_venv.sh` & `pwman-python-2.9/install_to_venv.sh`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/__main__.py` & `pwman-python-2.9/libpwman/__main__.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/aes.py` & `pwman-python-2.9/libpwman/aes.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/cryptsql.py` & `pwman-python-2.9/libpwman/cryptsql.py`

 * *Files 3% similar despite different names*

```diff
@@ -138,29 +138,29 @@
 		"""
 		try:
 			fc = FileObjCollection.parseFile(filename)
 			if fc is None:
 				return
 
 			# Get the file fields.
-			head = fc.getOne(b"HEAD", "Invalid file header object")
+			head = fc.get(b"HEAD", "Invalid file header object")
 			if head != CSQL_HEADER:
 				raise CSQLError("Invalid file header")
-			cipher = fc.getOne(b"CIPHER", "Invalid CYPHER object")
-			cipherMode = fc.getOne(b"CIPHER_MODE", "Invalid CYPHER_MODE object")
-			cipherIV = fc.getOne(b"CIPHER_IV", "Invalid CIPHER_IV object")
-			keyLen = fc.getOne(b"KEY_LEN", "Invalid KEY_LEN object")
-			kdfMethod = fc.getOne(b"KDF_METHOD", "Invalid KDF_METHOD object")
-			kdfSalt = fc.getOne(b"KDF_SALT", "Invalid KDF_SALT object")
-			kdfIter = fc.getOne(b"KDF_ITER", "Invalid KDF_ITER object")
-			kdfHash = fc.getOne(b"KDF_HASH", "Invalid KDF_HASH object")
-			kdfMac = fc.getOne(b"KDF_MAC", "Invalid KDF_MAC object")
-			compress = fc.getOne(b"COMPRESS", default=b"NONE")
-			paddingMethod = fc.getOne(b"PADDING", default=b"PWMAN")
-			payload = fc.getOne(b"PAYLOAD", "Invalid PAYLOAD object")
+			cipher = fc.get(b"CIPHER", "Invalid CIPHER object")
+			cipherMode = fc.get(b"CIPHER_MODE", "Invalid CIPHER_MODE object")
+			cipherIV = fc.get(b"CIPHER_IV", "Invalid CIPHER_IV object")
+			keyLen = fc.get(b"KEY_LEN", "Invalid KEY_LEN object")
+			kdfMethod = fc.get(b"KDF_METHOD", "Invalid KDF_METHOD object")
+			kdfSalt = fc.get(b"KDF_SALT", "Invalid KDF_SALT object")
+			kdfIter = fc.get(b"KDF_ITER", "Invalid KDF_ITER object")
+			kdfHash = fc.get(b"KDF_HASH", "Invalid KDF_HASH object")
+			kdfMac = fc.get(b"KDF_MAC", "Invalid KDF_MAC object")
+			compress = fc.get(b"COMPRESS", default=b"NONE")
+			paddingMethod = fc.get(b"PADDING", default=b"PWMAN")
+			payload = fc.get(b"PAYLOAD", "Invalid PAYLOAD object")
 
 			# Check the padding method.
 			if paddingMethod not in (b"PWMAN", b"PKCS7"):
 				raise CSQLError("Unknown padding: %s" % (
 						paddingMethod.decode("UTF-8", "ignore")))
 
 			# Check the cipher.
@@ -338,29 +338,29 @@
 			cipherIV = self.__random(AES.BLOCK_SIZE)
 			payload = AES.get().encrypt(key=key, iv=cipherIV, data=payload)
 		except Exception as e:
 			raise CSQLError("Failed to encrypt: %s" % str(e))
 
 		try:
 			# Assemble file objects
-			fc = FileObjCollection(
+			fc = FileObjCollection((
 				FileObj(b"HEAD", CSQL_HEADER),
 				FileObj(b"CIPHER", b"AES"),
 				FileObj(b"CIPHER_MODE", b"CBC"),
 				FileObj(b"CIPHER_IV", cipherIV),
 				FileObj(b"KEY_LEN", str(keyLen * 8).encode("UTF-8")),
 				FileObj(b"KDF_METHOD", b"PBKDF2"),
 				FileObj(b"KDF_SALT", kdfSalt),
 				FileObj(b"KDF_ITER", str(kdfIter).encode("UTF-8")),
 				FileObj(b"KDF_HASH", kdfHash.encode("UTF-8")),
 				FileObj(b"KDF_MAC", b"HMAC"),
 				FileObj(b"COMPRESS", b"NONE"), # compat for older versions.
 				FileObj(b"PADDING", b"PKCS7"),
 				FileObj(b"PAYLOAD", payload),
-			)
+			))
 
 			# Write to the file
 			self.__key = None
 			fc.writeFile(self.__filename)
 			self.__key = key
 
 		except FileObjError as e:
```

### Comparing `pwman-python-2.8/libpwman/database.py` & `pwman-python-2.9/libpwman/database.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 from libpwman.util import *
 
 import csv
 import io
 import os
 import pathlib
 import sys
+from copy import deepcopy
 from dataclasses import dataclass
 
 __all__ = [
 	"CSQLError",
 	"PWManDatabase",
 	"PWManEntry",
 	"PWManEntryAttr",
@@ -141,40 +142,41 @@
 			if not self.__silent:
 				print("Migrating database from version %s to version %s..." % (
 				      dbVer, self.DB_VER[-1]),
 				      file=sys.stderr)
 
 			self.__initTables()
 
-			c = self.sqlExec("SELECT category FROM pw;")
+			c = self.sqlExec("SELECT DISTINCT category FROM pw ORDER BY category;")
 			categories = c.fetchAll()
-			categories = uniq(c[0] for c in categories)
-			for category in categories:
-				c = self.sqlExec("SELECT title FROM pw WHERE category=?;",
+			for (category, ) in categories:
+				c = self.sqlExec("SELECT title FROM pw WHERE category=? ORDER BY title;",
 						 (category,))
 				titles = c.fetchAll()
-				titles = sorted(t[0] for t in titles)
-				for title in titles:
+				for (title, ) in titles:
 					c = self.sqlExec("SELECT category, title, user, pw, bulk FROM pw "
-							 "WHERE category=? AND title=?;",
+							 "WHERE category=? AND title=? "
+							 "LIMIT 1;",
 							 (category, title))
 					data = c.fetchOne()
+					if not data:
+						continue
 					c = self.sqlExec("INSERT INTO entries(category, title, user, pw) "
 							 "VALUES(?,?,?,?);",
 							 (data[0], data[1], data[2], data[3]))
 					entryId = c.lastRowID()
 					if data[4]:
 						c = self.sqlExec("INSERT INTO bulk(entry, data) "
 								 "VALUES(?,?);",
 								 (entryId, data[4]))
 			c = self.sqlExec("SELECT name, data FROM info;")
 			infos = c.fetchAll()
-			for info in infos:
+			for name, data in infos:
 				c = self.sqlExec("INSERT INTO globalattr(name, data) VALUES(?,?);",
-						 (info[0], info[1]))
+						 (name, data))
 			c = self.sqlExec("DROP TABLE IF EXISTS pw;")
 			c = self.sqlExec("DROP TABLE IF EXISTS info;")
 			self.sqlVacuum()
 		else:
 			assert(0)
 
 	def __initTables(self):
@@ -214,47 +216,49 @@
 		super().setPassphrase(passphrase)
 		self.__setDirty()
 
 	def categoryExists(self, category):
 		"""Returns True, if a category exists in the database.
 		category: The name string of the category.
 		"""
-		return category in self.getCategoryNames()
+		c = self.sqlExec("SELECT EXISTS(SELECT 1 FROM entries "
+				 "WHERE category=? "
+				 "LIMIT 1);",
+				 (category,))
+		data = c.fetchOne()
+		return data and data[0]
 
 	def getCategoryNames(self):
 		"""Get all category names in the database.
 		Returns a sorted list of strings.
 		"""
-		c = self.sqlExec("SELECT category FROM entries;")
-		categories = c.fetchAll()
-		if not categories:
-			return []
-		return uniq(c[0] for c in categories)
+		c = self.sqlExec("SELECT DISTINCT category FROM entries "
+				 "ORDER BY category;")
+		return [ data[0] for data in c.fetchAll() ]
 
 	def getEntryTitles(self, category):
 		"""Get all titles from one category in the database.
 		category: The category name string.
 		Returns a sorted list of strings.
 		"""
-		c = self.sqlExec("SELECT title FROM entries WHERE category=?;",
+		c = self.sqlExec("SELECT title FROM entries "
+				 "WHERE category=? "
+				 "ORDER BY title;",
 				 (category,))
-		titles = c.fetchAll()
-		if not titles:
-			return []
-		titles = sorted(t[0] for t in titles)
-		return titles
+		return [ data[0] for data in c.fetchAll() ]
 
 	def getEntry(self, category, title):
 		"""Get an entry from the database.
 		category: The name string of the category to get an entry from.
 		title: The title string of the entry to get.
 		Returns a PWManEntry() instance.
 		"""
 		c = self.sqlExec("SELECT id, category, title, user, pw FROM entries "
-				 "WHERE category=? AND title=?;",
+				 "WHERE category=? AND title=? "
+				 "LIMIT 1;",
 				 (category,
 				  title))
 		data = c.fetchOne()
 		if not data:
 			return None
 		return PWManEntry(category=data[1],
 				  title=data[2],
@@ -386,15 +390,21 @@
 			 for data in dataSet ]
 
 	def entryExists(self, category, title):
 		"""Returns True, if an entry exists in the database.
 		category: The name string of the category.
 		title: The title string of the entry.
 		"""
-		return self.getEntry(category, title) is not None
+		c = self.sqlExec("SELECT EXISTS(SELECT 1 FROM entries "
+				 "WHERE category=? AND title=? "
+				 "LIMIT 1);",
+				 (category,
+				  title))
+		data = c.fetchOne()
+		return data and data[0]
 
 	def addEntry(self, entry):
 		"""Create a new entry in the database.
 		entry: A PWManEntry() instance.
 		"""
 		if self.entryExists(entry.category, entry.title):
 			raise PWManError("Entry does already exist")
@@ -427,53 +437,115 @@
 				 (entry.category,
 				  entry.title,
 				  entry.user,
 				  entry.pw,
 				  entry.entryId))
 		self.__setDirty()
 
-	def moveEntry(self, entry, newCategory, newTitle):
-		"""Move an existing entry to a new category and/or set a new entry title.
-		entry: The PWManEntry() instance to move.
-		newCategory: The new category name string.
-		newTitle: The new title string.
+	def moveEntry(self, entry, newCategory, newTitle, toDb=None, copy=False):
+		"""Move or copy an existing entry to a new category and/or set a new entry title.
+		entry: The PWManEntry() instance to move/copy.
+		newCategory: The target category name string.
+		newTitle: The target title string.
+		toDb: The target database. Defaults to self.
+		copy: If False, then move. If True, then copy.
 		"""
-		if self.entryExists(newCategory, newTitle):
+		toDb = toDb or self
+		if toDb.entryExists(newCategory, newTitle):
 			raise PWManError("Entry does already exist.")
 		oldEntry = self.getEntry(entry.category, entry.title)
 		if not oldEntry:
 			raise PWManError("Entry does not exist.")
-		entry.category = newCategory
-		entry.title = newTitle
-		c = self.sqlExec("UPDATE entries SET "
-				 "category=?, title=? "
-				 "WHERE id=?;",
-				 (entry.category,
-				  entry.title,
-				  oldEntry.entryId))
-		self.__setDirty()
+		if toDb is self and not copy:
+			entry.category = newCategory
+			entry.title = newTitle
+			c = self.sqlExec("UPDATE entries SET "
+					 "category=?, title=? "
+					 "WHERE id=?;",
+					 (entry.category,
+					  entry.title,
+					  oldEntry.entryId))
+			self.__setDirty()
+		else:
+			newEntry = deepcopy(oldEntry)
+			bulk = self.getEntryBulk(newEntry)
+			attrs = self.getEntryAttrs(newEntry)
+			totp = self.getEntryTotp(newEntry)
+			newEntry.entryId = None
+			newEntry.category = newCategory
+			newEntry.title = newTitle
+			toDb.addEntry(newEntry)
+			if bulk:
+				bulk.bulkId = None
+				toDb.setEntryBulk(bulk)
+			for attr in attrs:
+				attr.attrId = None
+				toDb.setEntryAttr(attr)
+			if totp:
+				totp.totpId = None
+				toDb.setEntryTotp(totp)
+			if not copy:
+				entry.entryId = newEntry.entryId
+				entry.category = newEntry.category
+				entry.title = newEntry.title
+				self.delEntry(oldEntry)
 
-	def moveEntries(self, fromCategory, toCategory):
-		"""Move all entries from one category to another category.
+	def moveEntries(self, fromCategory, toCategory, toDb=None, copy=False):
+		"""Move or copy all entries from one category to another category.
 		fromCategory: The category to move all entries from.
 		toCategory: The (new) category to move all entries to.
+		toDb: The target database. Defaults to self.
+		copy: If False, then move. If True, then copy.
 		"""
+		toDb = toDb or self
 		if not self.categoryExists(fromCategory):
 			raise PWManError("Source category does not exist.")
-		c = self.sqlExec("UPDATE entries SET category=? "
-				 "WHERE category=?;",
-				 (toCategory,
-				  fromCategory))
-		self.__setDirty()
+		if toDb is self and fromCategory == toCategory:
+			return
+		fromTitles = self.getEntryTitles(fromCategory)
+		for fromTitle in fromTitles:
+			if toDb.entryExists(toCategory, fromTitle):
+				raise PWManError("Target entry %s/%s does already exist." % (
+						 toCategory, fromTitle))
+		if toDb is self and not copy:
+			c = self.sqlExec("UPDATE entries SET category=? "
+					 "WHERE category=?;",
+					 (toCategory,
+					  fromCategory))
+			self.__setDirty()
+		else:
+			for fromTitle in fromTitles:
+				entry = self.getEntry(fromCategory, fromTitle)
+				bulk = self.getEntryBulk(entry)
+				attrs = self.getEntryAttrs(entry)
+				totp = self.getEntryTotp(entry)
+				entry.entryId = None
+				entry.category = toCategory
+				toDb.addEntry(entry)
+				if bulk:
+					bulk.bulkId = None
+					toDb.setEntryBulk(bulk)
+				for attr in attrs:
+					attr.attrId = None
+					toDb.setEntryAttr(attr)
+				if totp:
+					totp.totpId = None
+					toDb.setEntryTotp(totp)
+			if not copy:
+				for fromTitle in fromTitles:
+					entry = self.getEntry(fromCategory, fromTitle)
+					self.delEntry(entry)
 
 	def delEntry(self, entry):
 		"""Delete an existing entry from the database.
 		entry: The PWManEntry() instance to delete from the database.
 		"""
-		c = self.sqlExec("SELECT id FROM entries WHERE category=? AND title=?;",
+		c = self.sqlExec("SELECT id FROM entries "
+				 "WHERE category=? AND title=? "
+				 "LIMIT 1;",
 				 (entry.category,
 				  entry.title))
 		entryId = c.fetchOne()
 		if entryId is None:
 			raise PWManError("Entry does not exist")
 		entryId = entryId[0]
 		c = self.sqlExec("DELETE FROM entries WHERE id=?;",
@@ -485,15 +557,16 @@
 		"""Get the bulk data associated with an entry.
 		entry: The PWManEntry() to get the bulk data for.
 		Returns a PWManEntryBulk() instance or None, if there is no bulk data.
 		"""
 		c = self.sqlExec("SELECT bulk.id, bulk.data "
 				 "FROM bulk, entries "
 				 "WHERE entries.category=? AND entries.title=? AND "
-				 "bulk.entry = entries.id;",
+				 "bulk.entry = entries.id "
+				 "LIMIT 1;",
 				 (entry.category,
 				  entry.title))
 		data = c.fetchOne()
 		if not data:
 			return None
 		return PWManEntryBulk(data=data[1],
 				      entry=entry,
@@ -504,15 +577,15 @@
 		entryBulk: The new PWManEntryBulk() instance to write to the database.
 		           If entryBulk.data is None, then the bulk data is deleted.
 		"""
 		entry = entryBulk.entry
 		if not entry or entry.entryId is None:
 			raise PWManError("Bulk: Entry does not exist.")
 		if entryBulk.data:
-			c = self.sqlExec("SELECT id FROM bulk WHERE entry=?;",
+			c = self.sqlExec("SELECT id FROM bulk WHERE entry=? LIMIT 1;",
 					 (entry.entryId, ))
 			bulkId = c.fetchOne()
 			if bulkId is None:
 				c = self.sqlExec("INSERT INTO bulk(entry, data) "
 						 "VALUES(?,?);",
 						 (entry.entryId,
 						  entryBulk.data))
@@ -533,15 +606,16 @@
 		"""Get the TOTP parameters associated with an entry.
 		entry: The PWManEntry() to get the TOTP parameters for.
 		Returns a PWManEntryTOTP() instance, or None if there is no TOTP data.
 		"""
 		c = self.sqlExec("SELECT totp.id, totp.key, totp.digits, totp.hash "
 				 "FROM totp, entries "
 				 "WHERE entries.category=? AND entries.title=? AND "
-				 "totp.entry = entries.id;",
+				 "totp.entry = entries.id "
+				 "LIMIT 1;",
 				 (entry.category,
 				  entry.title))
 		data = c.fetchOne()
 		if not data:
 			return None
 		return PWManEntryTOTP(key=data[1],
 				      digits=data[2],
@@ -554,15 +628,15 @@
 		entryTotp: The new PWManEntryTOTP() instance to write to the database.
 		           If entryTotp.key is None, then the TOTP data is deleted.
 		"""
 		entry = entryTotp.entry
 		if not entry or entry.entryId is None:
 			raise PWManError("TOTP: Entry does not exist.")
 		if entryTotp.key:
-			c = self.sqlExec("SELECT id FROM totp WHERE entry=?;",
+			c = self.sqlExec("SELECT id FROM totp WHERE entry=? LIMIT 1;",
 					 (entry.entryId, ))
 			totpId = c.fetchOne()
 			if totpId is None:
 				c = self.sqlExec("INSERT INTO totp(entry, key, digits, hash) "
 						 "VALUES(?,?,?,?);",
 						 (entry.entryId,
 						  entryTotp.key,
@@ -588,15 +662,16 @@
 		entry: The PWManEntry() to get the attribute for.
 		attrName: The name string of the attribute to get.
 		Returns a PWManEntryAttr() instance, or None if there is such attribute.
 		"""
 		c = self.sqlExec("SELECT entryattr.id, entryattr.name, entryattr.data "
 				 "FROM entryattr, entries "
 				 "WHERE entries.category=? AND entries.title=? AND "
-				 "entryattr.entry = entries.id AND entryattr.name=?;",
+				 "entryattr.entry = entries.id AND entryattr.name=? "
+				 "LIMIT 1;",
 				 (entry.category,
 				  entry.title,
 				  attrName))
 		data = c.fetchOne()
 		if not data:
 			return None
 		return PWManEntryAttr(name=data[1],
@@ -631,15 +706,16 @@
 		           If entryAttr.data is None, then the attribute is deleted.
 		"""
 		entry = entryAttr.entry
 		if not entry or entry.entryId is None:
 			raise PWManError("Attr: Entry does not exist.")
 		if entryAttr.data:
 			c = self.sqlExec("SELECT id FROM entryattr "
-					 "WHERE entry=? AND name=?;",
+					 "WHERE entry=? AND name=? "
+					 "LIMIT 1;",
 					 (entry.entryId,
 					  entryAttr.name))
 			attrId = c.fetchOne()
 			if attrId is None:
 				c = self.sqlExec("INSERT INTO entryattr(entry, name, data) "
 						 "VALUES(?,?,?);",
 						 (entry.entryId,
@@ -661,29 +737,32 @@
 
 	def getGlobalAttr(self, name):
 		"""Get a global attribute.
 		A global attribute is not associated with an entry.
 		Returns None, if the attribute does not exist.
 		"""
 		try:
-			c = self.sqlExec("SELECT id, data FROM globalattr WHERE name=?;",
+			c = self.sqlExec("SELECT id, data FROM globalattr "
+					 "WHERE name=? "
+					 "LIMIT 1;",
 					 (name,))
 			data = c.fetchOne()
 			return data[1] if data else None
 		except (CSQLError) as e:
 			return None
 
 	def setGlobalAttr(self, name, data, setDirty=True):
 		"""Set a global attribute.
 		A global attribute is not associated with an entry.
 		If data is None or empty, the attribute is deleted from the database.
 		"""
 		if data:
 			c = self.sqlExec("SELECT id FROM globalattr "
-					 "WHERE name=?;",
+					 "WHERE name=? "
+					 "LIMIT 1;",
 					 (name,))
 			attrId = c.fetchOne()
 			if attrId is None:
 				c = self.sqlExec("INSERT INTO globalattr(name, data) "
 						 "VALUES(?,?);",
 						 (name, data))
 			else:
```

### Comparing `pwman-python-2.8/libpwman/dbdiff.py` & `pwman-python-2.9/libpwman/dbdiff.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/fileobj.py` & `pwman-python-2.9/libpwman/fileobj.py`

 * *Files 26% similar despite different names*

```diff
@@ -19,55 +19,59 @@
 class FileObj:
 	# Raw object layout:
 	#   [ 1 byte  ] => Name length
 	#   [ x bytes ] => Name
 	#   [ 4 bytes ] => Payload data length
 	#   [ x bytes ] => Payload data
 
+	__slots__ = (
+		"__name",
+		"__data",
+	)
+
 	def __init__(self, name, data):
 		"""Construct FileObj().
 		name: The object name. Must be bytes-like.
 		data: The object payload. Must be bytes-like.
 		"""
-		assert isinstance(name, (bytes, bytearray)),\
+		assert isinstance(name, (bytes, bytearray, memoryview)),\
 		       "FileObj: Invalid 'name' type."
-		assert isinstance(data, (bytes, bytearray)),\
+		assert isinstance(data, (bytes, bytearray, memoryview)),\
 		       "FileObj: Invalid 'data' type."
-		if len(name) > 0x7F:
+		self.__name = memoryview(name)
+		self.__data = memoryview(data)
+		if len(self.__name) > 0x7F:
 			raise FileObjError("FileObj: Name too long")
-		self.__name = name
-		if len(data) > 0x7FFFFFFF:
+		if len(self.__data) > 0x7FFFFFFF:
 			raise FileObjError("FileObj: Data too long")
-		self.__data = data
 
 	def getName(self):
 		return self.__name
 
 	def getData(self):
 		return self.__data
 
-	def getRaw(self):
-		r = bytearray()
+	def getRaw(self, buffer):
 		nameLen = len(self.__name)
 		assert nameLen <= 0x7F
-		r += b"%c" % (nameLen & 0xFF)
-		r += self.__name
+		buffer += b"%c" % (nameLen & 0xFF)
+		buffer += self.__name
 		dataLen = len(self.__data)
 		assert dataLen <= 0x7FFFFFFF
-		r += b"%c" % (dataLen & 0xFF)
-		r += b"%c" % ((dataLen >> 8) & 0xFF)
-		r += b"%c" % ((dataLen >> 16) & 0xFF)
-		r += b"%c" % ((dataLen >> 24) & 0xFF)
-		r += self.__data
-		return r
+		buffer += b"%c" % (dataLen & 0xFF)
+		buffer += b"%c" % ((dataLen >> 8) & 0xFF)
+		buffer += b"%c" % ((dataLen >> 16) & 0xFF)
+		buffer += b"%c" % ((dataLen >> 24) & 0xFF)
+		buffer += self.__data
 
 	@classmethod
 	def parseRaw(cls, raw):
-		assert isinstance(raw, (bytes, bytearray)),\
+		assert isinstance(raw, (bytes, bytearray, memoryview)),\
 		       "FileObj: Invalid 'raw' type."
+		raw = memoryview(raw)
 		try:
 			off = 0
 			nameLen = raw[off]
 			if nameLen & 0x80:
 				raise FileObjError("FileObj: Name length extension bit is set, "
 						   "but not supported by this pwman version.")
 			off += 1
@@ -84,55 +88,60 @@
 			data = raw[off : off + dataLen]
 			off += dataLen
 		except (IndexError, KeyError) as e:
 			raise FileObjError("Failed to parse file object")
 		return (cls(name, data), off)
 
 class FileObjCollection:
-	def __init__(self, *objects):
-		self.objects = objects
+	__slots__ = (
+		"__objects",
+	)
+
+	def __init__(self, objects):
+		if isinstance(objects, dict):
+			self.__objects = objects
+		elif isinstance(objects, (list, tuple)):
+			self.__objects = { obj.getName() : obj for obj in objects }
+		else:
+			assert False
 
 	def writeFile(self, filepath):
 		try:
 			with open(filepath, "wb") as f:
 				f.write(self.getRaw())
 				f.flush()
 		except IOError as e:
 			raise FileObjError("Failed to write file: %s" % e.strerror)
 
 	def getRaw(self):
 		raw = bytearray()
-		for obj in self.objects:
-			raw += obj.getRaw()
+		for obj in self.__objects.values():
+			obj.getRaw(raw)
 		return raw
 
-	def get(self, name):
-		return [ o.getData()
-			 for o in self.objects
-			 if o.getName() == name ]
-
-	def getOne(self, name, errorMsg=None, default=None):
-		objs = self.get(name)
-		if len(objs) != 1:
+	def get(self, name, errorMsg=None, default=None):
+		obj = self.__objects.get(name, None)
+		if obj is None:
 			if errorMsg:
 				raise FileObjError(errorMsg)
 			return default
-		return objs[0]
+		return bytes(obj.getData())
 
 	@classmethod
 	def parseRaw(cls, raw):
-		assert isinstance(raw, (bytes, bytearray)),\
+		assert isinstance(raw, (bytes, bytearray, memoryview)),\
 		       "FileObjCollection: Invalid 'raw' type."
+		raw = memoryview(raw)
 		offset = 0
-		objects = []
+		objects = {}
 		while offset < len(raw):
 			obj, objLen = FileObj.parseRaw(raw[offset:])
-			objects.append(obj)
+			objects[obj.getName()] = obj
 			offset += objLen
-		return cls(*objects)
+		return cls(objects)
 
 	@classmethod
 	def parseFile(cls, filepath):
 		try:
 			with open(filepath, "rb") as f:
 				rawData = f.read()
 		except IOError as e:
```

### Comparing `pwman-python-2.8/libpwman/mlock.py` & `pwman-python-2.9/libpwman/mlock.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/otp.py` & `pwman-python-2.9/libpwman/otp.py`

 * *Files 20% similar despite different names*

```diff
@@ -34,42 +34,32 @@
 			key = b32decode(key.encode("UTF-8"), casefold=True)
 		except (binascii.Error, UnicodeError):
 			raise OtpError("Invalid key.")
 	if not (0 <= counter <= (2 ** 64) - 1):
 		raise OtpError("Invalid counter.")
 	if not (1 <= nrDigits <= 8):
 		raise OtpError("Invalid number of digits.")
-
 	try:
 		hmacHash = hmacHash.replace("-", "")
 		hmacHash = hmacHash.replace("_", "")
 		hmacHash = hmacHash.replace(" ", "")
 		hmacHash = hmacHash.upper().strip()
 		hmacHash = {
 			"SHA1"   : hashlib.sha1,
 			"SHA256" : hashlib.sha256,
 			"SHA512" : hashlib.sha512,
 		}[hmacHash]
 	except KeyError:
 		raise OtpError("Invalid HMAC hash type.")
 
-	counter = bytes(((counter >> 56) & 0xFF,
-			 (counter >> 48) & 0xFF,
-			 (counter >> 40) & 0xFF,
-			 (counter >> 32) & 0xFF,
-			 (counter >> 24) & 0xFF,
-			 (counter >> 16) & 0xFF,
-			 (counter >> 8) & 0xFF,
-			 (counter >> 0) & 0xFF))
-	h = hmac.new(key, counter, hmacHash).digest()
+	counter = counter.to_bytes(length=8, byteorder="big", signed=False)
+	h = bytearray(hmac.new(key, counter, hmacHash).digest())
 	offset = h[19] & 0xF
-	hSlice = (((h[offset + 0] & 0x7F) << 24) |
-		  ((h[offset + 1] & 0xFF) << 16) |
-		  ((h[offset + 2] & 0xFF) << 8) |
-		  ((h[offset + 3] & 0xFF) << 0))
+	h[offset] &= 0x7F
+	hSlice = int.from_bytes(h[offset:offset+4], byteorder="big", signed=False)
 	otp = hSlice % (10 ** nrDigits)
 	fmt = "%0" + str(nrDigits) + "d"
 	return fmt % otp
 
 def totp(key, nrDigits=6, hmacHash="SHA1", t=None):
 	"""TOTP - Time-Based One-Time Password Algorithm.
 	nrDigits: The number of digits to return. Can be 1 to 8.
```

### Comparing `pwman-python-2.8/libpwman/ui.py` & `pwman-python-2.9/libpwman/ui.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 import pathlib
 import re
 import readline
 import sys
 import time
 import traceback
 from cmd import Cmd
-from copy import copy, deepcopy
+from copy import copy
 from dataclasses import dataclass, field
 from typing import Optional, Tuple
 
 if osIsPosix:
 	import signal
 
 __all__ = [
@@ -362,15 +362,18 @@
 
 		self.__updatePrompt()
 
 		self._timeout = PWManTimeout(timeout)
 
 	@property
 	def __db(self):
-		return self.__dbs[self.__selDbName]
+		return self._getDb(self.__selDbName)
+
+	def _getDb(self, name):
+		return self.__dbs.get(name, None)
 
 	def __updatePrompt(self):
 		if len(self.__dbs) > 1:
 			dbName = self.__selDbName
 			lim = 20
 			if len(dbName) > lim - 3:
 				dbName = dbName[:lim-3] + "..."
@@ -906,133 +909,81 @@
 	do_rm = do_remove
 	do_del = do_remove
 
 	complete_remove = __complete_category_title
 	complete_rm = complete_remove
 	complete_del = complete_remove
 
-	__move_opts = ("-s:", "-d:")
-	def do_move(self, params):
-		"""--- Move/rename an existing entry or a category ---
-
-		Move/rename an existing entry:
-		Command: move CATEGORY TITLE TO_CATEGORY [NEW_TITLE]
-		(NEW_TITLE defaults to TITLE)
-
-		Move all entries from one category into another category.
-		Command: move FROM_CATEGORY TO_CATEGORY
-
-		Move an entry from one database to another:
-		Command: move -s main -d other CATEGORY TITLE TO_CATEGORY [NEW_TITLE]
-		(NEW_TITLE defaults to TITLE)
-
-		Move all entries from a category from one database into another database:
-		Command: move -s main -d other FROM_CATEGORY [TO_CATEGORY]
-		(TO_CATEGORY defaults to FROM_CATEGORY)
-
-		Options:
-		  -s SOURCE_DATABASE_NAME
-		  -d DESTINATION_DATABASE_NAME
-		  Databases default to the currently selected database.
-		  The named databases must be open. See 'database' command.
-
-		Aliases: mv rename
-		"""
-		opts = PWManOpts.parse(params, self.__move_opts)
+	__move_copy_opts = ("-s:", "-d:")
+	def __do_move_copy(self, command, params):
+		opts = PWManOpts.parse(params, self.__move_copy_opts)
 
 		sourceDbName = opts.getOpt("-s", default=self.__selDbName)
-		sourceDb = self.__dbs.get(sourceDbName, None)
+		sourceDb = self._getDb(sourceDbName)
 		if sourceDb is None:
-			self._err("move", "Source database '%s' does not exist" % sourceDbName)
+			self._err(command, "Source database '%s' does not exist" % sourceDbName)
 		destDbName = opts.getOpt("-d", default=self.__selDbName)
-		destDb = self.__dbs.get(destDbName, None)
+		destDb = self._getDb(destDbName)
 		if destDb is None:
-			self._err("move", "Destination database '%s' does not exist" % destDbName)
+			self._err(command, "Destination database '%s' does not exist" % destDbName)
 
 		if opts.nrParams in (3, 4):
-			# Entry rename/move
+			# Entry rename/move or copy
 			fromCategory, fromTitle, toCategory, toTitle =\
 				(opts.getParam(0), opts.getParam(1),
 				 opts.getParam(2), opts.getParam(3))
 			toTitle = toTitle or fromTitle
-			if sourceDb is destDb and fromCategory == toCategory and fromTitle == toTitle:
-				self._info("move", "Nothing changed. Not moving anything.")
-				return
 			entry = sourceDb.getEntry(fromCategory, fromTitle)
-			oldEntry = deepcopy(entry)
 			if not entry:
-				self._err("move", "Source entry does not exist.")
+				self._err(command, "Source entry does not exist.")
+			if sourceDb is destDb and fromCategory == toCategory and fromTitle == toTitle:
+				return
 			try:
-				if sourceDb is destDb:
-					# Move in one DB.
-					sourceDb.moveEntry(entry, toCategory, toTitle)
-				else:
-					# Move between different DBs.
-					entry.entryId = None
-					entry.category = toCategory
-					entry.title = toTitle
-					destDb.addEntry(entry)
-					sourceDb.delEntry(oldEntry)
+				sourceDb.moveEntry(entry, toCategory, toTitle,
+						   toDb=destDb,
+						   copy=(command == "copy"))
 			except (PWManError) as e:
-				self._err("move", str(e))
+				self._err(command, str(e))
 		elif (sourceDb is destDb and opts.nrParams == 2) or\
 		     (sourceDb is not destDb and opts.nrParams in (1, 2)):
-			# Whole category move.
+			# Whole category move or copy.
 			fromCategory, toCategory = opts.getParam(0), opts.getParam(1)
 			toCategory = toCategory or fromCategory
 			try:
-				if sourceDb is destDb:
-					# Category move in one DB.
-					sourceDb.moveEntries(fromCategory, toCategory)
-				else:
-					# Category move between DBs.
-					if not sourceDb.categoryExists(fromCategory):
-						self._err("move", "Source category does not exist.")
-					for fromTitle in sourceDb.getEntryTitles(fromCategory):
-						self._info("move",
-							"running command: move -s %s -d %s %s %s %s %s" % (
-							escapeCmd(sourceDbName), escapeCmd(destDbName),
-							escapeCmd(fromCategory), escapeCmd(fromTitle),
-							escapeCmd(toCategory), escapeCmd(fromTitle)))
-						entry = sourceDb.getEntry(fromCategory, fromTitle)
-						oldEntry = deepcopy(entry)
-						entry.entryId = None
-						entry.category = toCategory
-						destDb.addEntry(entry)
-						sourceDb.delEntry(oldEntry)
+				sourceDb.moveEntries(fromCategory, toCategory,
+						     toDb=destDb,
+						     copy=(command == "copy"))
 			except (PWManError) as e:
-				self._err("move", str(e))
+				self._err(command, str(e))
 		else:
-			self._err("move", "Invalid parameters.")
-	do_mv = do_move
-	do_rename = do_move
+			self._err(command, "Invalid parameters.")
 
 	@completion
-	def complete_move(self, text, line, begidx, endidx):
+	def __complete_move_copy(self, text, line, begidx, endidx):
 		if text == "-":
-			return PWManOpts.rawOptTemplates(self.__move_opts)
+			return PWManOpts.rawOptTemplates(self.__move_copy_opts)
 		if len(text) == 2 and text.startswith("-"):
 			return [ text + " " ]
 		dbOpts = ("-s", "-d")
-		opts = PWManOpts.parse(line, self.__move_opts, ignoreFirst=True, softFail=True)
+		opts = PWManOpts.parse(line, self.__move_copy_opts, ignoreFirst=True, softFail=True)
 		if opts.error:
 			opt, error = opts.error
 			if error == "no_arg" and opt in dbOpts:
 				return self.__getDatabaseCompletions(text)
 			return []
 		optName, value = opts.atCmdIndex(PWManOpts.calcParamIndex(line, endidx))
 		if optName in dbOpts:
 			return self.__getDatabaseCompletions(text)
 
 		sourceDbName = opts.getOpt("-s", default=self.__selDbName)
-		sourceDb = self.__dbs.get(sourceDbName, None)
+		sourceDb = self._getDb(sourceDbName)
 		if sourceDb is None:
 			return []
 		destDbName = opts.getOpt("-d", default=self.__selDbName)
-		destDb = self.__dbs.get(destDbName, None)
+		destDb = self._getDb(destDbName)
 		if destDb is None:
 			return []
 
 		paramIdx = opts.getComplParamIdx(text)
 		if paramIdx == 0:
 			# Category completion
 			return self.__getCategoryCompletions(text, db=sourceDb)
@@ -1050,14 +1001,46 @@
 			return self.__getCategoryCompletions(text, db=destDb)
 		elif paramIdx == 3:
 			# Entry title completion
 			category = opts.getParam(2)
 			if category:
 				return self.__getEntryTitleCompletions(category, text, db=destDb)
 		return []
+
+	def do_move(self, params):
+		"""--- Move/rename an existing entry or a category ---
+
+		Move/rename an existing entry:
+		Command: move CATEGORY TITLE TO_CATEGORY [NEW_TITLE]
+		(NEW_TITLE defaults to TITLE)
+
+		Move all entries from one category into another category.
+		Command: move FROM_CATEGORY TO_CATEGORY
+
+		Move an entry from one database to another:
+		Command: move -s main -d other CATEGORY TITLE TO_CATEGORY [NEW_TITLE]
+		(NEW_TITLE defaults to TITLE)
+
+		Move all entries from a category from one database into another database:
+		Command: move -s main -d other FROM_CATEGORY [TO_CATEGORY]
+		(TO_CATEGORY defaults to FROM_CATEGORY)
+
+		Options:
+		  -s SOURCE_DATABASE_NAME
+		  -d DESTINATION_DATABASE_NAME
+		  Databases default to the currently selected database.
+		  The named databases must be open. See 'database' command.
+
+		Aliases: mv rename
+		"""
+		self.__do_move_copy("move", params)
+	do_mv = do_move
+	do_rename = do_move
+
+	complete_move = __complete_move_copy
 	complete_mv = complete_move
 	complete_rename = complete_move
 
 	__copy_opts = ("-s:", "-d:")
 	def do_copy(self, params):
 		"""--- Copy an entry or a category ---
 
@@ -1080,69 +1063,18 @@
 		  -s SOURCE_DATABASE_NAME
 		  -d DESTINATION_DATABASE_NAME
 		  Databases default to the currently selected database.
 		  The named databases must be open. See 'database' command.
 
 		Aliases: cp
 		"""
-		opts = PWManOpts.parse(params, self.__copy_opts)
-
-		sourceDbName = opts.getOpt("-s", default=self.__selDbName)
-		sourceDb = self.__dbs.get(sourceDbName, None)
-		if sourceDb is None:
-			self._err("copy", "Source database '%s' does not exist" % sourceDbName)
-		destDbName = opts.getOpt("-d", default=self.__selDbName)
-		destDb = self.__dbs.get(destDbName, None)
-		if destDb is None:
-			self._err("copy", "Destination database '%s' does not exist" % destDbName)
-
-		if opts.nrParams in (3, 4):
-			# Entry copy
-			fromCategory, fromTitle, toCategory, toTitle =\
-				(opts.getParam(0), opts.getParam(1),
-				 opts.getParam(2), opts.getParam(3))
-			toTitle = toTitle or fromTitle
-			if sourceDb is destDb and fromCategory == toCategory and fromTitle == toTitle:
-				self._info("copy", "Copy source and target are identical.")
-				return
-			entry = sourceDb.getEntry(fromCategory, fromTitle)
-			if not entry:
-				self._err("copy", "Source entry does not exist.")
-			try:
-				entry.entryId = None
-				entry.category = toCategory
-				entry.title = toTitle
-				destDb.addEntry(entry)
-			except (PWManError) as e:
-				self._err("copy", str(e))
-		elif (sourceDb is destDb and opts.nrParams == 2) or\
-		     (sourceDb is not destDb and opts.nrParams in (1, 2)):
-			# Category copy
-			fromCategory, toCategory = opts.getParam(0), opts.getParam(1)
-			toCategory = toCategory or fromCategory
-			try:
-				if not sourceDb.categoryExists(fromCategory):
-					self._err("copy", "Source category does not exist.")
-				for fromTitle in sourceDb.getEntryTitles(fromCategory):
-					self._info("copy",
-						"running command: copy -s %s -d %s %s %s %s %s" % (
-						escapeCmd(sourceDbName), escapeCmd(destDbName),
-						escapeCmd(fromCategory), escapeCmd(fromTitle),
-						escapeCmd(toCategory), escapeCmd(fromTitle)))
-					entry = sourceDb.getEntry(fromCategory, fromTitle)
-					entry.entryId = None
-					entry.category = toCategory
-					destDb.addEntry(entry)
-			except (PWManError) as e:
-				self._err("copy", str(e))
-		else:
-			self._err("copy", "Invalid parameters.")
+		self.__do_move_copy("copy", params)
 	do_cp = do_copy
 
-	complete_copy = complete_move # copy and move are equal w.r.t. completion
+	complete_copy = __complete_move_copy
 	complete_cp = complete_copy
 
 	__database_opts = ("-f:",)
 	def do_database(self, params):
 		"""--- Open a database or switch to an already opened database ---
 		Command: database [-f FILEPATH] [NAME]
 
@@ -1351,15 +1283,15 @@
 		"""
 		flunk = params.startswith("!")
 		if flunk:
 			params = params[1:].strip()
 		name = params if params else self.__selDbName
 		if name == "main" and len(self.__dbs) > 1:
 			self._err("close", "The 'main' database can only be closed last")
-		db = self.__dbs.get(name, None)
+		db = self._getDb(name)
 		if db is None:
 			self._err("close", "The database '%s' does not exist" % name)
 		if db.isDirty():
 			if not flunk:
 				self._err("close", "The database '%s' contains "
 					  "uncommitted changes" % name)
 			db.flunkDirty()
```

### Comparing `pwman-python-2.8/libpwman/ui_escape.py` & `pwman-python-2.9/libpwman/ui_escape.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/libpwman/util.py` & `pwman-python-2.9/libpwman/util.py`

 * *Files 9% similar despite different names*

```diff
@@ -10,15 +10,14 @@
 import os
 import sys
 
 __all__ = [
 	"str2bool",
 	"osIsWindows",
 	"osIsPosix",
-	"uniq",
 	"stdout",
 	"clearScreen",
 	"readPassphrase",
 ]
 
 osIsWindows = os.name == "nt" or os.name == "ce"
 osIsPosix = os.name == "posix"
@@ -32,20 +31,14 @@
 	if s in ("false", "no", "off", "0"):
 		return False
 	try:
 		return bool(int(s))
 	except ValueError:
 		return default
 
-def uniq(l, sort=True):
-	l = list(set(l))
-	if sort:
-		l.sort()
-	return l
-
 def stdout(text, flush=True):
 	if isinstance(text, str):
 		stream = sys.stdout
 	else:
 		stream = getattr(sys.stdout, "buffer", None)
 		if stream is None:
 			stream = sys.stdout
```

### Comparing `pwman-python-2.8/maintenance/gen-doc.sh` & `pwman-python-2.9/maintenance/gen-doc.sh`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/maintenance/win-install-dependencies.cmd` & `pwman-python-2.9/maintenance/win-install-dependencies.cmd`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/maintenance/win-standalone-build.cmd` & `pwman-python-2.9/maintenance/win-standalone-build.cmd`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/pwman.cmd` & `pwman-python-2.9/pwman.cmd`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/pwman_python.egg-info/PKG-INFO` & `pwman-python-2.9/pwman_python.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pwman-python
-Version: 2.8
+Version: 2.9
 Summary: Commandline password manager
 Home-page: https://bues.ch/h/pwman
 Author: Michael Büsch
 Author-email: m@bues.ch
 Keywords: password manager command line TOTP 2FA
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `pwman-python-2.8/pwman_python.egg-info/SOURCES.txt` & `pwman-python-2.9/pwman_python.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/setup.py` & `pwman-python-2.9/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,24 +3,21 @@
 
 from setuptools import setup
 try:
 	from cx_Freeze import setup, Executable
 	cx_Freeze = True
 except ImportError:
 	cx_Freeze = False
-import os
 import sys
-
+from pathlib import Path
 from libpwman import __version__
 
-basedir = os.path.abspath(os.path.dirname(__file__))
-for base in (os.getcwd(), basedir):
-	sys.path.insert(0, base)
+basedir = Path(__file__).parent.absolute()
+sys.path.insert(0, basedir)
 
-# Create freeze executable list.
 extraKeywords = {}
 if cx_Freeze:
 	extraKeywords["executables"] = [ Executable(script="pwman") ]
 	extraKeywords["options"] = {
 		"build_exe" : {
 			"packages" : [ "readline",
 				       "pyreadline3",
@@ -28,15 +25,15 @@
 				       "_curses",
 				       "sqlite3",
 				       "sqlite3.dump", ],
 			"excludes" : [ "tkinter", ],
 		}
 	}
 
-with open(os.path.join(basedir, "README.rst"), "rb") as fd:
+with open(basedir / "README.rst", "rb") as fd:
 	readmeText = fd.read().decode("UTF-8")
 
 setup(
 	name		= "pwman-python",
 	version		= __version__,
 	description	= "Commandline password manager",
 	author		= "Michael Büsch",
@@ -58,7 +55,9 @@
 		"Operating System :: OS Independent",
 		"Programming Language :: Python :: 3",
 	],
 	long_description=readmeText,
 	long_description_content_type="text/x-rst",
 	**extraKeywords
 )
+
+# vim: ts=8 sw=8 noexpandtab
```

### Comparing `pwman-python-2.8/tests/run.sh` & `pwman-python-2.9/tests/run.sh`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/tests/test_database_v0.db` & `pwman-python-2.9/tests/test_database_v0.db`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/tests/test_database_v0.py` & `pwman-python-2.9/tests/test_database_v0.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/tests/test_database_v1.db` & `pwman-python-2.9/tests/test_database_v1.db`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/tests/test_database_v1.py` & `pwman-python-2.9/tests/test_database_v1.py`

 * *Files identical despite different names*

### Comparing `pwman-python-2.8/tests/test_otp.py` & `pwman-python-2.9/tests/test_otp.py`

 * *Files identical despite different names*

